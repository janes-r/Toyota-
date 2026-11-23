# Android Auto sur Toyota C-HR 2018 (Toyota Touch 2) : rapport de faisabilité logicielle

*Date : 23/11/2026. Unité étudiée : audio VE3947 / ID appareil 13TFDAEU-CA04 ; navigation 6.11.0WH / NA530 / carte 2018 v1.*

Légende : **[FAIT]** vérifié dans une source · **[HYP]** hypothèse raisonnée · **[NV]** piste non vérifiée.

---

## 1. Identification de votre système

| Élément | Valeur | Statut |
|---|---|---|
| Unité audio/écran (DCU) | Model ID `13TFDAEU-CA04`, logiciel VE3947 | [FAIT] relevé véhicule |
| Module navigation (MEU « Go/Go Plus ») | `NA530`, logiciel 6.11.0WH | [FAIT] relevé véhicule |
| Famille | Toyota Touch 2 (1re génération de plateforme, « CY13 ») | [HYP] voir ci-dessous |

**Lecture du Model ID.** Sur les unités qui ont reçu Android Auto/CarPlay, Toyota utilise des Model IDs du type `17TDT2EU-DA01` (DCU Panasonic) et `17TMT2EU-FA00` (MEU Harman). Le préfixe `17` correspond à l'année-plateforme (CY17 / « 17MM »), `EU` à la région, et le suffixe à la variante [FAIT, source 1]. Votre `13TFDAEU` suit la même logique et désigne donc **une plateforme 2013 (CY13)**, **différente de la plateforme CY17**, pas une variante de celle-ci [HYP forte]. Le C-HR 1re génération (2016–2019) a gardé cette ancienne architecture Touch 2.

**Ce qui reste inconnu** (aucune source publique trouvée pour `13TFDAEU` ou `NA530`) : le fabricant exact de la carte (Panasonic, Fujitsu Ten/Denso Ten ou Harman), le SoC, l'OS, le type de mémoire flash et le bootloader. Comment l'obtenir :
1. **Sans démontage** : faire relever au concessionnaire (Techstream/GTS) les références pièce `86140-xxxxx` (DCU) et `86840-xxxxx` (MEU).
2. **Démontage de la façade** (clips, 4 vis) : lire l'étiquette du boîtier (fabricant, part number, n° de série).
3. **Ouverture du boîtier**, en dernier recours : photographier la carte pour identifier le SoC et les puces eMMC/NAND et repérer les ports UART/JTAG.

À titre de comparaison, la DCU CY17 (RAV4/Corolla 2019-2020) qui accepte CarPlay utilise un **NXP i.MX6Q**, Linux Yocto/AGL et U-Boot 2009.08, avec un HABv4 possiblement actif [FAIT d'après source 1, non vérifié indépendamment].

## 2. Firmwares compatibles connus

- **Pour 13TFDAEU-CA04 / VE3947** : aucun fichier de firmware public, aucun bulletin et aucun dépôt trouvé. Seules des mises à jour de cartographie existent pour NA530 (l'« ID Carte 2018 v1 » relève de la carte, pas du firmware).
- **CY17 → CY17Plus** (bulletin Toyota **BE-00439T-TME v4, 18/09/2020**) : migration par 3 clés USB, MEU FA00→FA10 et audio build 1020→1023 (fichiers `17TDT2EU-DA01_7910.kwi` / `DA31_7910.kwi`) [FAIT, source 1]. Ce bulletin **ne concerne que les DCU 17TDT2EU**. Le C-HR n'est pas dans la liste des véhicules éligibles.

## 3. Possibilités de mise à jour officielle

**[FAIT] Toyota UK l'écrit publiquement et le répète** : le système multimédia des C-HR de génération précédente est « incompatible with the Apple CarPlay/Android Auto software so retrofit will not be available » (source 2). Une mise à jour concessionnaire de VE3947 peut corriger des bugs, mais n'apportera pas Android Auto.

## 4. Firmwares alternatifs / communautaires

- **OpenTouch2** (GitHub, source 1) : il fiabilise le rétrofit **officiel** CY17. Il ne force pas les signatures et ne cible pas les C-HR 2016-2018. Le seul résultat confirmé est **CarPlay** filaire sur un RAV4 2020 ; Android Auto n'a pas été testé. Inapplicable à 13TFDAEU.
- **Piste Hybrid Life** (Corolla/RAV4 flashés sur puce) : aucune trace technique vérifiable retrouvée. Les firmwares évoqués sont ceux de la plateforme CY17 (autre carte, autre SoC probable) [NV].
- **Vidéos « C-HR 2018 Touch 2 → CarPlay »** (YouTube, source 3) : ce sont des **interfaces/boîtiers vidéo** ajoutés derrière l'écran, pas du logiciel. Elles sont exclues par vos contraintes.

## 5. Témoignages de modification réussie sur votre matériel

**Aucun trouvé.** Aucun cas documenté d'Android Auto activé par le seul logiciel sur une unité `13TFDAEU` (C-HR, Auris, Yaris ou RAV4 d'avant 2019).

## 6. Faisabilité d'un portage depuis Corolla/RAV4

| Obstacle | Évaluation |
|---|---|
| Matériel différent (CY13 vs CY17 : SoC, RAM, carte, pilotes écran/tactile/caméra/CAN) | Un firmware CY17 ne démarrera pas tel quel [HYP forte] |
| Android Auto exige un stack Google certifié (AAP + licence/certificats OEM) et un décodeur H.264 matériel | Le firmware de votre unité ne contient pas ce stack. Il faudrait l'extraire du CY17 (binaires ARM liés à leur OS) et l'adapter [HYP] |
| Signature des paquets `.kwi`, HABv4 possible, Model ID vérifié par l'installateur | Le changement de nom de fichier ne fonctionne qu'entre variantes d'un même Model ID (DA01↔DA31) [FAIT source 1] |
| Mémoire et puissance d'un SoC de 2013 | Possiblement insuffisantes pour la projection H.264 [HYP] |

Un portage serait **un projet de reverse engineering complet** (dump de la flash, analyse de l'OS, portage du stack AAP, pilotes). Personne ne l'a réalisé publiquement. Le dump d'origine permet de le tenter sans risque, mais rien ne garantit l'aboutissement.

## 7. Procédure technique potentielle (recherche uniquement, aucun flash)

1. Identifier la DCU (§1), puis ouvrir le boîtier et noter le SoC et la flash.
2. **Sauvegarder** : dump de l'eMMC/NAND, en lecture seule (adaptateur eMMC ISP ou programmateur type XGecu T48/RT809H, sur fils soudés) ; sinon via la console UART si un shell U-Boot est accessible.
3. Analyser le dump (binwalk, partitions, OS, présence d'un module « smartphone integration » désactivé, flags de configuration).
4. Ne tenter une écriture que si : la restauration du dump est validée, le format de signature est compris et le stack AA est présent ou portable.

Matériel : outils de démontage de garnitures, fer à souder fin, adaptateur UART 3,3 V, lecteur eMMC, alimentation 12 V d'établi. Logiciels : binwalk, Ghidra, flashrom/éditeur hexadécimal.

## 8. Risques et restauration

- Brick de la DCU : elle commande l'écran, la radio, le Bluetooth, la **caméra de recul** (obligation légale/sécurité), les commandes au volant et les réglages véhicule.
- Une restauration n'est possible **que** si un dump brut complet a été fait au préalable. Le concessionnaire ne reflashe généralement pas une DCU corrompue : il remplace l'unité (coût élevé).
- Désynchronisation possible DCU/MEU (navigation), perte d'appairages, codes défaut CAN.

## 9. Conclusion

| Niveau | Solution |
|---|---|
| Confirmée et reproductible | **Aucune** pour 13TFDAEU-CA04 |
| Documentée mais non vérifiée sur votre matériel | Rétrofit officiel CY17Plus / OpenTouch2. **Ne s'applique pas** : autre plateforme (17TDT2EU) |
| Techniquement plausible | Aucune identifiée. Une fonction AA « cachée » dans VE3947 n'a jamais été signalée |
| Nécessite du reverse engineering | Dump de la flash et portage du stack Android Auto CY17 vers CY13 : effort très élevé, réussite incertaine |
| Impossible en l'état | Mise à jour officielle Toyota apportant AA ; flash direct d'un firmware Corolla/RAV4 |

**Verdict :** avec les éléments vérifiables à ce jour, **aucune voie purement logicielle n'existe pour ajouter Android Auto à votre Touch 2 (13TFDAEU-CA04)**. Toyota le confirme officiellement, et les seuls succès logiciels documentés concernent une autre plateforme (CY17, 2019+). La seule piste restante est un projet de reverse engineering de type recherche, qui commence par une identification matérielle et un dump complet de la flash. Elle n'est pas raisonnable à court terme sur un véhicule utilisé au quotidien.

Prochaine action utile : obtenir les part numbers `86140-…` et `86840-…` (concessionnaire ou étiquette). Avec eux, la recherche pourra être relancée de façon ciblée.

## Sources
1. OpenTouch2, CarPlay retrofit fix pour DCU Panasonic CY17 : https://github.com/edgardavey/toyota-touch2-dcu-carplay-fix
2. Toyota UK Magazine, réponses officielles sur le rétrofit CarPlay/AA (C-HR exclu) : https://mag.toyota.co.uk/toyota-apple-carplay-and-android-auto-upgrade/comment-page-24 (et pages 25, 30, 31…)
3. Vidéo « Toyota C-HR 2018 Touch 2 → CarPlay » (interface matérielle) : https://www.youtube.com/watch?v=2KGO-XjYgb4
4. Toyota UK, Touch & Go vs Touch 2 : https://mag.toyota.co.uk/toyota-touch-2-faq/comment-page-1/
5. Harman, fournisseur multimédia Toyota Europe : https://www.marklines.com/en/news/4970
