# Community and commercial mods adding Android Auto / CarPlay to the original Toyota Touch 2 (with Go): applicability to a pre-facelift C-HR (13TFDAEU-CA04 / NA530)

Research date: 23 Nov 2026. Owner's unit: audio software VE3947, audio device ID 13TFDAEU-CA04, nav software 6.11.0WH, nav device NA530, map 2018 v1.

Method note (applies to every section): in this session, full-page fetches to hybridlife.org, toyotaownersclub.com, youtube.com and latestsatnav.co.uk were blocked by the network sandbox. Only github.com could be read in full. Everything else below comes from search-engine extracts of those pages: short quotes and summaries, without post dates, usernames or attached images. Quotes from forum pages are therefore "as indexed", and evidential strength is rated conservatively. Evidence scale used: **A** = primary technical evidence (part numbers + versions + reproducible procedure or photos); **B** = first-hand owner report with identifiers; **C** = first-hand claim without identifiers or proof; **D** = second-hand, vendor marketing, or anonymous claim.

## 1. The "Hybrid Life" thread(s): what was actually described

### Takeaway
No thread on a site called "hybrid-life.co.uk" could be found. The description matches one post in the **French HybridLife forum (hybridlife.org)**, in the long thread "Tutoriel de mise à jour de Toyota Touch & Go 2". The post is a single unattributed, hearsay-style description: the unit is removed, the memory chip desoldered and a "homemade" firmware flashed. It gives no car, no part number, no firmware version, no photos and no named service, and the same thread's administrators say CarPlay/AA cannot be added to these units (evidence: **D**).

### Cited Findings
- Search for hybrid-life.co.uk content returned nothing from that domain. Results came from toyotaownersclub.com, mag.toyota.co.uk and the French hybridlife.org instead. — [Search results incl. Toyota Owners Club 204281](https://www.toyotaownersclub.com/forums/topic/204281-android-auto-retrofit/); [hybridlife.org thread p.24](https://hybridlife.org/threads/tutoriel-de-mise-%C3%A0-jour-de-toyota-touch-go-2.3945/page-24)
- The key post, as indexed on hybridlife.org thread 3945 (page 62): "La procédure est la suivante : L'autoradio lui-même est démonté et le microcircuit est dessoudé. Un programmeur spécial flashe le firmware modifié, qui contient CarPlay et AndroidAuto. Ce n'est pas un firmware officiel, c'est fait maison." — [hybridlife.org, Tutoriel de mise à jour de Toyota Touch & Go 2, page 62](https://hybridlife.org/threads/tutoriel-de-mise-%C3%A0-jour-de-toyota-touch-go-2.3945/page-62)
- The search-engine summary of the same thread says the modified firmware is described as **converted from other Toyota models' firmware (RAV4, Corolla)**. The exact wording, poster and date could not be retrieved. — [hybridlife.org thread 3945, p.62](https://hybridlife.org/threads/tutoriel-de-mise-%C3%A0-jour-de-toyota-touch-go-2.3945/page-62)
- The same thread contains firm denials from administrators and members:
  - "non, pas possible d'ajouter CarPlay par mise à jour du software" (admin)
  - "il n'y a aucun moyen d'activer AndroidAuto sur ces systèmes"
  - "Android Auto est impossible à implémenter ici", with 6.16.0H then cited as the latest firmware (post roughly 3,100 days old, i.e. about 2018)

  — [hybridlife.org p.24](https://hybridlife.org/threads/tutoriel-de-mise-%C3%A0-jour-de-toyota-touch-go-2.3945/page-24); [p.39](https://hybridlife.org/threads/tutoriel-de-mise-%C3%A0-jour-de-toyota-touch-go-2.3945/page-39); [p.62](https://hybridlife.org/threads/tutoriel-de-mise-%C3%A0-jour-de-toyota-touch-go-2.3945/page-62)
- A HybridLife administrator states that Toyota provides nothing for CarPlay on this system, and that the official CarPlay update is compatible only with Touch 3 from 2021. — [hybridlife.org p.62 (search extract)](https://hybridlife.org/threads/tutoriel-de-mise-%C3%A0-jour-de-toyota-touch-go-2.3945/page-62)
- The thread also says that on these units only the maps and firmware can be updated, without CarPlay: "mettre à jour la carte vers la version 2024v2 et firmware jusqu'à la version 6.24.0WH". This is relevant because the owner is on 6.11.0WH with map 2018 v1. — [hybridlife.org thread 3945 (search extract)](https://hybridlife.org/threads/tutoriel-de-mise-%C3%A0-jour-de-toyota-touch-go-2.3945/page-62)
- One member warns that audio firmware and maps should be updated before any "modernisation", "sinon vous pouvez casser le système". — [hybridlife.org thread 3945](https://hybridlife.org/threads/tutoriel-de-mise-%C3%A0-jour-de-toyota-touch-go-2.3945/page-62)
- One HybridLife post says DCU **17TDT2EU-DA01 cannot** be updated to CarPlay/AA while **17TDT2EU-DA02 can**. This is contradicted by the GitHub OpenTouch2 project, which got CarPlay working on a DA01 unit (see section 4). — [hybridlife.org thread (search extract)](https://hybridlife.org/threads/tutoriel-de-mise-%C3%A0-jour-de-toyota-touch-go-2.3945/page-53); contradicted by [GitHub OpenTouch2](https://github.com/edgardavey/toyota-touch2-dcu-carplay-fix)
- One HybridLife member, totolito44, reports a **Toyota C-HR 03/2017, "TOYOTA TOUCH 2 WHITH GO", software VE3937, device ID 13TFDAEU-CA04**. This is the same hardware ID as the owner's unit, on an earlier software version. — [hybridlife.org Touch & Go 2 thread p.45](https://hybridlife.org/threads/tutoriel-de-mise-%C3%A0-jour-de-toyota-touch-go-2.3945/page-45) / [Touch & Go Plus thread p.14](https://hybridlife.org/threads/mise-%C3%A0-jour-du-syst%C3%A8me-toyota-touch-go-plus-comment-faire.206/page-14) (search engine did not disambiguate which page)

### Inferences
- The "Hybrid Life" source the owner heard about is almost certainly hybridlife.org (French), not a UK site. The claimed procedure (remove unit, desolder chip, programmer, firmware "from Corolla/RAV4") rests on one indexed post. It names no car, no DCU part number, no before/after version screen and no service. That makes it a **D-grade** claim.
- The wording ("microcircuit", "programmeur spécial") reads like a translation of a Russian/Ukrainian service description ("микросхема выпаивается… программатор"). This suggests the poster was relaying an Eastern European workshop's advert rather than describing their own work. This is speculative.
- Even if real, "firmware from Corolla/RAV4" would come from the CY17/17MM generation (17TDT*), a different hardware platform from the owner's 13TFDAEU (CY13 generation). See section 6.

### Gaps
- Poster's username, post date, car model and unit part number for the desoldering post could not be retrieved, because the hybridlife.org fetch was blocked.
- No photos, videos or follow-up "it works / it bricked" replies were found for that post.
- Whether any hybrid-life.co.uk forum exists at all is unconfirmed; none was indexed.

## 2. Commercial services advertising Touch 2 CarPlay / Android Auto "activation"

### Takeaway
All software-activation services found (UK, Poland, Russia, Ukraine) target the **2019+ "CY17 / 17MM" Touch 2 units**:
- Panasonic 17TDT1EU-DA*/17TDT2EU-DA*
- Denso/Fujitsu Ten 17TDT1EU-CA*

These are found in MY19+ Corolla, RAV4 and Camry, and possibly the facelift C-HR. **None lists any 13T* unit (13TFDAEU)**, and Toyota's official retrofit pages restrict eligibility to 17MM/CY17 units. Everything sold "for C-HR 2016-2019 Touch 2" is a hardware interface box (category e).

### Cited Findings
**Official Toyota retrofit (the basis for most "activations"):**
- Toyota UK: the CarPlay/AA upgrade is for **MY19 Corolla (all bodies/grades) and MY19 and MY20 RAV4 (all grades excluding Icon)**, installed by dealer appointment. — [Toyota UK Magazine](https://mag.toyota.co.uk/toyota-apple-carplay-and-android-auto-upgrade/)
- Toyota UK staff replies in the comments repeatedly told 2017-2019 C-HR owners that the C-HR was not supplied with CarPlay and cannot be retrofitted, and that the car is "not compatible with the Android Auto upgrade". Yaris, Auris and Hilux were refused similarly; a few replies conflict. — [Toyota UK Magazine comments, e.g. page 20](https://mag.toyota.co.uk/toyota-apple-carplay-and-android-auto-upgrade/comment-page-20/); [page 47](https://mag.toyota.co.uk/toyota-apple-carplay-and-android-auto-upgrade/comment-page-47/)
- Toyota Greece: the retrofit applies to Touch 2 / Touch 2 & Go units **labelled 17MM or CY17**, on Corolla and RAV4 produced from November 2018, performed by trained dealers. — [Toyota Greece retrofit page](https://www.toyota.gr/owners/retrofit)
- Toyota Estonia/Latvia: the CarPlay update applies to RAV4/Corolla with Touch 2 & Go marked "17, 17MM, CY17, 17CY". — [Toyota Estonia (RU)](https://ru.toyota.ee/owners/myt-connected-services/multimedia); [Toyota Latvia (RU)](https://ru.toyota.lv/owners/myt-connected-services/multimedia)
- Bulletin **BE-00439T-TME v4 (18 Sep 2020)**, as described by the GitHub project, converts "CY17 → CY17Plus (17MM → 19MM)" with three USB drives. — [GitHub OpenTouch2](https://github.com/edgardavey/toyota-touch2-dcu-carplay-fix)
- Toyota UK on self-installing software: "We would not recommend this. Any attempts to install software yourself may damage your multimedia system and invalidate your warranty." — [Toyota UK Magazine, Touch2 with Go software upgrade article](https://mag.toyota.co.uk/toyota-touch2-with-go-receives-major-software-upgrade/) (quote via search extract)

**Third-party software-activation services:**
- **125coding (UK)** sells "Toyota CH-R Apple CarPlay Android Auto Activation Software Update 2019 - 2021" and an equivalent Corolla product.
  - Compatible DCUs listed: **17TDT1EU-CA01, 17TDT1EU-CA02 (Denso/Fujitsu); 17TDT1EU-DA01, -DA02, -DA30; 17TDT2EU-DA01, -DA02, -DA30 (Panasonic)**.
  - "Please check your DCU model number before booking."
  - No 13T* units listed. Price and warranty not retrieved.

  — [125coding C-HR product](https://www.125coding.co.uk/product-page/toyota-ch-r-apple-carplay-android-auto-activation-software-update-2019-2021); [125coding Corolla product](https://www.125coding.co.uk/product-page/toyota-corolla-apple-carplay-android-auto-activation-software-update-2019-2021)
- **Latest Satnav (UK)** has a "Toyota CarPlay & Android Auto Activation" category. Its content could not be fetched. A search summary says a UK activation vendor lists the same 17TDT1EU/17TDT2EU DCU list. — [latestsatnav.co.uk category](https://www.latestsatnav.co.uk/carplay--android-auto-68-c.asp) (unverified)
- **Navi-World** sells a Touch 3 / Gen.10 CarPlay/AA OEM activation that requires "Navigation database should be 2024v1 or higher". It also sells separate Touch 2 wireless CarPlay hardware modules. — [Navi-World Touch 3](https://navi-world.com/product/toyota-wireless-carplay-android-auto-toyota-touch-3-gen-10/); [Navi-World Touch2 category](https://navi-world.com/product-category/carplay-android-auto/toyota-wireless-carplay-android-auto-integration/)
- **fabryczne.pl (Poland)**: "Aktywacja CarPlay / Android Auto Toyota Corolla RAV4 bez wymiany" at **500 (PLN implied)**. It covers Corolla/RAV4 only; method and unit list were not retrieved. — [fabryczne.pl](https://fabryczne.pl/Aktywacja-CarPlay-Android-Auto-Toyota-Corolla-RAV4-bez-wymiany-p172)
- **navi174.ru (Russia)**: "Активация CarPlay Toyota RAV-4".
  - Lists compatible codes such as **17TDT2EU-DA01, 17TDT1EU-DA01**, and tells buyers to check the model code in MENU > Настройки > Обновление программы.
  - Delivered by remote update, workshop install or USB stick.

  — [navi174.ru](https://navi174.ru/index.php?route=product%2Fproduct&product_id=321)
- **mda-tech.ru (Russia)**: an update for **RAV4 and Corolla 2018-2021** activating CarPlay/AA via the standard USB port, without disassembly. — [mda-tech.ru](https://mda-tech.ru/shop/%D0%9E%D0%B1%D0%BD%D0%BE%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D0%B5-Toyota-RAV4-%D0%B8-Corolla-%D0%B4%D0%BB%D1%8F-%D0%B0%D0%BA%D1%82%D0%B8%D0%B2%D0%B0%D1%86%D0%B8%D0%B8-%D1%84%D1%83%D0%BD%D0%BA%D1%86%D0%B8%D0%B9-CarPlay-%D0%B8-Android-Auto-p242314096)
- **xa50.com.ua (Ukraine, RAV4 XA50 club)** hosts Touch 2 firmware archives with CarPlay/AA, e.g. for **17TDT1EU-CA01 and -CA32**. — [xa50.com.ua firmwares](https://xa50.com.ua/firmwares/)

**Hardware "retrofit" kits sold for C-HR 2016-2019 Touch 2 (category e, out of scope but often mistaken for firmware mods):**
- Integrated Automotive (UK): retrofit adding wired/wireless CarPlay and AA to the C-HR "factory screen", keeping factory controls; compatibility checked from a photo of the dash. — [integratedautomotive.co.uk](https://integratedautomotive.co.uk/toyota-c-hr-carplay-retrofit/)
- MAK Coding (UK) "Toyota Wireless Carplay & Android Auto Box - Entune2 / Touch2". — [makcoding.co.uk](https://www.makcoding.co.uk/product/toyota-carplay-android-box-entune2-touch2/)
- Bavarian Automotive (UK) Touch 2 / Entune 2.0 retrofit MMI kit. — [bavarian-automotive.co.uk](https://bavarian-automotive.co.uk/products/toyota-wireless-apple-carplay-android-auto-retrofit-mmi)
- Car Sound Security "Plug & Play CarPlay for Toyota C-HR 2016-2023". — [carsoundsecurity.com](https://www.carsoundsecurity.com/product/wireless-carplay-toyota-c-hr-2016-2023/)
- Euro Premium Parts "Wireless Apple Carplay Retrofit Kit for Toyota C-HR - 2018 to 2021". — [europremiumparts.com](https://europremiumparts.com/products/wireless-apple-carplay-retrofit-kit-for-toyota-c-hr-2018-to-2021)
- Polish prices for the same type of box:
  - Kaufland.pl from 560 zł
  - Sklep Adron 1,099.01 PLN (for "Toyota CHR Auris RAV4 z Touch 2")
  - nawigacje.net 1,799 zł

  — [kaufland.pl](https://www.kaufland.pl/product/542674401/); [sklephadron.pl](https://sklephadron.pl/toyota/6791-modul-android-auto-i-carplay-ip-do-toyoty-z-touch-2.html); [nawigacje.net](https://nawigacje.net/produkt/toyota-bezprzewodowy-carplay-android-corolla-auris-avensis-camry-prius-c-hr/)
- Other listings: Incarsolution "CarPlay Android Auto Mirrorlink Toyota Touch 2 & Entune 2.0" at €349; Carlinklife module at $179.99; eBay modules around $189.99 with a 1-year warranty. — [incarsolution.com](https://incarsolution.com/en/camera-interfaces/14596-carplay-android-auto-mirrorlink-toyota-touch-2-entune-20.html); [carlinklife.com](https://carlinklife.com/products/wireless-apple-carplay-android-auto-module-for-toyota-touch2-entune2-0-highlander-tundra-sienna-prius-yaris-camry-chr); [eBay](https://www.ebay.com/itm/235147727259)
- Romanian vendor autoextra.ro lists a Touch 2 CarPlay/AA/MirrorLink integration kit for 2013-2018 Toyotas including the C-HR. It is discussed on chrforums.uk (thread from January 2023). — [chrforums.uk thread 4413](https://www.chrforums.uk/threads/apple-carplay-for-toyota-touch-2.4413/)
- French installer guide: a CarPlay/AA box for C-HR installs behind the original screen. — [goautoradio-gps.fr](https://goautoradio-gps.fr/blogs/tutoriels-installation/boitier-carplay-android-auto-toyota-chr-installation)
- Autodoc (FR) says that for 2016-2019 C-HR with the original Touch 2, "aucune mise à jour logicielle par clé USB réalisable soi-même ne permet d'activer Apple CarPlay". It also says native activation on 2017 models is impossible because of hardware incompatibility. — [auto-doc.fr](https://www.auto-doc.fr/info/apple-carplay-pour-la-toyota-c-hr-tutoriel-et-mise-a-jour-du-systeme)

### Inferences
- The "activation" services are resellers or automators of Toyota's own CY17→CY17Plus USB retrofit, or distribute the same firmware files. They depend on CarPlay/AA code that exists in Toyota's signed firmware for 17TDT* DCUs. No such code exists for the 13T generation, so none of them can apply to 13TFDAEU-CA04.
- 125coding's "C-HR 2019-2021" product most likely targets the **facelift** C-HR's 17TDT1EU-CA0x (Denso/Fujitsu) DCU, not the pre-facelift 13TFDAEU unit. This is an inference from its DCU list.
- No service found in Lithuania, the Netherlands, France or Israel advertising a software CarPlay/AA unlock for 13T-generation Touch 2.

### Gaps
- 125coding and Latest Satnav prices, warranties and the exact text of exclusions could not be read (fetch blocked or not retrieved).
- No vendor was found that explicitly writes "13TFDAEU not supported". The exclusion is inferred from positive-only compatibility lists.
- No commercial service offering an eMMC/NAND reflash of a 13T unit was found in any language.

## 3. Russian / Ukrainian / Polish sources (4pda, drive2, toyota-club, elektroda, toyotaklub.org.pl)

### Takeaway
Eastern European sources document routine **official** Touch 2 firmware updates and CY17 CarPlay activations (RAV4/Corolla). None of them documents an eMMC-reflash or desoldering procedure that adds CarPlay/AA to a 13T-generation unit. One Russian source is directly relevant to the owner's exact ID: it reports that on a **13TFDAEU-CA04** unit, updating to VE3934 made **MirrorLink stop being detected**.

### Cited Findings
- toyotacamry.ru (Russian Camry club, "Обновление ПО для головных устройств Touch and Go2"): a 2016 car with firmware **VE3881 and ID 13TFDAEU-CA04** was updated to **VE3934** (same CA04 suffix). The owner reports that MirrorLink stopped being detected. — [toyotacamry.ru thread 12140, p.41](https://toyotacamry.ru/showthread.php?page=41&t=12140)
- The same Russian community circulates unofficial USB update files such as **"13TFDAEU-CA43_9999.kwi"**. Owners say newer versions fix bugs but add no features. — [toyotacamry.ru thread 12140](https://toyotacamry.ru/showthread.php?t=12140)
- drive2.ru entries document ordinary Touch / Touch and Go2 firmware updates (Corolla 160 2013; Camry XV50 2014). There is no CarPlay/AA content. — [drive2 Corolla](https://www.drive2.ru/l/740488097032055772/); [drive2 Camry XV50](https://www.drive2.ru/l/8648068/)
- toyota_update (LiveJournal, Russian commercial blog):
  - Offers C-HR head-unit firmware updates for gen 1 2016-2019, the facelift 2019-2023 and gen 2.
  - One post mentions fixes for "ошибки работы Apple Carplay" (which only apply to units that have CarPlay).
  - Another describes side-effects: AA voice prompts losing sound, error B15FE, CarPlay call transfer failing.
  - Nothing claims to add CarPlay to the 2016-2019 Touch 2.

  — [toyota-update.livejournal.com/24962](https://toyota-update.livejournal.com/24962.html); [29961](https://toyota-update.livejournal.com/29961.html)
- Polish Toyota Klub forum: long "Toyota Touch 2 - firmware update" threads list per-ID versions (e.g. "13TFDAEU-DA07: 0101AF -> 0101B9"). There are no CarPlay/AA unlocks for 13T units. — [forum.toyotaklub.org.pl topic 45711](https://forum.toyotaklub.org.pl/index.php?topic=45711.0); [topic 47458](https://forum.toyotaklub.org.pl/index.php?topic=47458.480)
- A 13TFDAEU-DA06 unit is reported on software 01013B. "DA" = Panasonic-family variant of the same 13T ID family. — [search extract, Toyota Owners Club / Polish forum](https://www.forum.toyotaklub.org.pl/index.php?topic=45711.165)
- Russian activation shops (navi174.ru, mda-tech.ru) only advertise RAV4/Corolla 2018/2019-2021 with 17TDT* codes (see section 2). — [navi174.ru](https://navi174.ru/index.php?route=product%2Fproduct&product_id=321); [mda-tech.ru](https://mda-tech.ru/shop/%D0%9E%D0%B1%D0%BD%D0%BE%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D0%B5-Toyota-RAV4-%D0%B8-Corolla-%D0%B4%D0%BB%D1%8F-%D0%B0%D0%BA%D1%82%D0%B8%D0%B2%D0%B0%D1%86%D0%B8%D0%B8-%D1%84%D1%83%D0%BD%D0%BA%D1%86%D0%B8%D0%B9-CarPlay-%D0%B8-Android-Auto-p242314096)
- The Ukrainian xa50.com.ua (RAV4 XA50) firmware page provides CarPlay-enabled archives for 17TDT1EU-CA01/CA32, not for 13T units. — [xa50.com.ua](https://xa50.com.ua/firmwares/)
- Searches for 4pda and elektroda.pl returned no indexed threads on CarPlay/AA for Touch 2 or C-HR. — (negative result; no URL)

### Inferences
- The desoldering/"homemade firmware" story in section 1 has no traceable origin in the Russian/Ukrainian/Polish communities that would normally document such work. If such a service exists, it is not publicly documented with photos, part numbers or results.
- The MirrorLink loss reported on 13TFDAEU-CA04 after VE3934 matters for the MirrorLink-based dongles in section 4. The owner is on **VE3947** (later than VE3934), so MirrorLink may already be absent or broken on the owner's unit. This is single-source and unconfirmed.

### Gaps
- 4pda.to, toyota-club.net and elektroda.pl content could not be retrieved or indexed; there are no results in Lithuanian or Hebrew.
- No Russian or Ukrainian source with photos of a desoldered Touch 2 eMMC/NAND for CarPlay was found.

## 4. XDA / GitHub / Reddit / YouTube: genuine firmware mods vs external boxes

### Takeaway
The only rigorous public technical work is the GitHub **OpenTouch2** project (grade **A** for its own scope). It covers **Panasonic DCU 17TDT2EU-DA01 (part 86140-42571) on a 2020 RAV4 EU**, not the C-HR 13T unit. It is a USB-level file fix to Toyota's official retrofit, not an eMMC reflash. It also documents that this platform uses NXP i.MX6 HABv4 secure boot, which blocks custom images unless the fuses are open. A C-HR forum attempt at modifying Touch 2 (13T-era) update images got telnet/D-Bus enabled, but the modified image failed at install reboot, and no CarPlay/AA came out of it. Every C-HR "CarPlay on the original screen" video/seller found is an external box or a MirrorLink-to-CarPlay USB dongle.

### Cited Findings
**GitHub edgardavey/toyota-touch2-dcu-carplay-fix ("OpenTouch2"), read in full:**
- Hardware: Panasonic DCU **17TDT2EU-DA01, part 86140-42571**; Harman MEU **17TMT2EU-FA00 → FA10, part 86840-06041 → 86840-K0010**; tested car **2020 RAV4 Hybrid FWD (EU)**. Chassis listed: RAV4 AXAH52/54, MXAA52/54; Corolla ZRE210, ZWE211. — [GitHub OpenTouch2](https://github.com/edgardavey/toyota-touch2-dcu-carplay-fix)
- Method: the official BE-00439T-TME (v4, 18 Sep 2020) 3-USB sequence, plus two fixes:
  1. Delete the 0-byte `phaseup.dat` from the USB3 root, which otherwise causes error 001 at 99%.
  2. Replace the contents of `17TDT2EU-DA01_7910.kwi` with the **DA31** file's contents while keeping the DA01 filename.
  - Result: audio version **1020 (no CarPlay) → 1023 (CarPlay)**; "full CarPlay, confirmed working"; a "Delete personal data" reset was needed; wireless CarPlay untested.

  — [GitHub OpenTouch2](https://github.com/edgardavey/toyota-touch2-dcu-carplay-fix)
- Security and risks:
  - Platform identified as **NXP i.MX6Q, U-Boot 2009.08, Yocto/AGL base, HABv4 secure boot**; whether it is "actually fused closed on this specific DCU" is unknown: "Nobody has checked this for the Panasonic Touch 2 DCU yet."
  - The USB1 package's `intervention_script.sh` performs "a direct write to the eMMC's bootloader region"; the author warns not to experiment on a working unit.
  - "No units were bricked in the making of this guide."

  — [OpenTouch2 README](https://raw.githubusercontent.com/edgardavey/toyota-touch2-dcu-carplay-fix/main/README.md)
- The project does **not** mention C-HR, 13TFDAEU, NA530, MM13/CY13, desoldering or NAND/eMMC reflashing. Evidence is text plus file-size tables, with no photos; the repo had 1 star and 6 commits at time of reading. — [GitHub OpenTouch2](https://github.com/edgardavey/toyota-touch2-dcu-carplay-fix)

**Firmware-modding attempts on the older Touch 2:**
- chrforums.uk "Modifying Touch 2 updates" (about 1,400 days old, roughly early 2023), mirrored on Toyota Owners Club:
  - The poster modified, rebuilt and signed Touch 2 update files.
  - They were "able to enable Dbus, telnet, and increase the amount of information written to the logdump" and could not find the root password, though "there is a workaround".
  - The modified update "passes validation" but stops when the unit reboots to install it.
  - No CarPlay/AA.

  — [chrforums.uk thread 4415](https://www.chrforums.uk/threads/modifying-touch-2-updates.4415/); [Toyota Owners Club topic 211605](https://toyotaownersclub.com/forums/topic/211605-modifying-touch-2-updates)
- haxor.fi write-up on Toyota Touch & Go updates (search extract): an open telnet service on port 23 with a root login prompt; "without one of Toyota's private signing keys, custom firmware images are impractical to make". — [haxor.fi](https://haxor.fi/posts/how-the-firmware-updates-work-on-toyota-touch-go/) (exact unit generation not confirmed)
- XDA has only a "Toyota Map Update Hacking Help" thread; nothing on CarPlay/AA on Touch 2. — [xdaforums.com 4534131](https://xdaforums.com/t/toyota-map-update-hacking-help.4534131/)

**MirrorLink → CarPlay USB converters (a borderline case: no box behind the screen, but still external hardware):**
- chrforums.uk "Enable CarPlay Without Replacing Your Touch2 Head Unit" and rav4world "Touch 2 CarPlay Upgrade – MirrorLink to CarPlay converter": "The Touch2 hardware supports MirrorLink, and I used a MirrorLink → CarPlay protocol conversion method. The entire process doesn't require disassembling the center console or flashing the firmware; only a USB adapter is needed." The poster says "the user experience is still being refined, so I cannot disclose too many details at present." — [chrforums.uk 5493](https://www.chrforums.uk/threads/enable-carplay-without-replacing-your-touch2-head-unit.5493/); [rav4world 343771](https://www.rav4world.com/threads/touch-2-carplay-upgrade-%E2%80%93-mirrorlink-to-carplay-converter.343771/); [rav4world 343789](https://www.rav4world.com/threads/2014-2018-touch2-carplay-upgrade.343789/)
- A vendor post on toyotaenthusiasts.com: "our team developed a wireless adapter that enables CarPlay functionality through MirrorLink—completely plug-and-play, provided your head unit supports MirrorLink. Our prototype has now been successfully tested on the touch2 head unit". — [toyotaenthusiasts.com thread 72](https://www.toyotaenthusiasts.com/forum/threads/activate-carplay-on-your-toyota-touch2-no-head-unit-replacement-needed.72/)
- Related YouTube titles (not viewable here): "Toyota Touch 2 2014–2019 CarPlay Upgrade" and "Toyota Yaris Touch 2(2014–2019) CarPlay Upgrade". — [YouTube pWjvfAlKW_0](https://www.youtube.com/watch?v=pWjvfAlKW_0); [YouTube Mo5nAvKY1e4](https://www.youtube.com/watch?v=Mo5nAvKY1e4)
- chrforums.uk "Got MirrorLink (Google Maps/YT/etc) working on 2018 Touch 2 Go!": "The Sony Xperia Z2 or Z3 are the safest bets as they are MirrorLink compatible, which our 2016-2019 CHR Touch 2 Go (TTG) support." — [chrforums.uk 4209](https://www.chrforums.uk/threads/got-mirrorlink-google-maps-yt-etc-working-on-2018-touch-2-go.4209/)
- Touch 2's MirrorLink is old (1.0/1.1); French C-HR forum users report connection problems. — [forum-auto.caradisiac.com 133112](https://forum-auto.caradisiac.com/topic/133112-mirror-link-sur-touch-2-touch-and-go/); [forum-c-hr-passion.com](https://www.forum-c-hr-passion.com/t509p125-mirrorlink)

**YouTube C-HR videos, titles only (full pages not viewable here):**
- "Apple Carplay/Android Auto for Toyota C-HR" — [YouTube MvzVyqOEUDg](https://www.youtube.com/watch?v=MvzVyqOEUDg)
- "Upgrade Toyota C-HR to use wireless carplay function" — [YouTube _yqvETdAFhU](https://www.youtube.com/watch?v=_yqvETdAFhU)
- "CarPlay в Toyota CH-R (Toyota Touch 2) 2016-2020 г.в." — [YouTube EZo8PqGO9ag](https://www.youtube.com/watch?v=EZo8PqGO9ag)
- "Toyota C-HR 2018 Touch 2 -> Apple CarPlay Upgrade, Factory Screen Transformation!" — [YouTube 2KGO-XjYgb4](https://www.youtube.com/watch?v=2KGO-XjYgb4)

**Reddit:** no relevant r/Toyota, r/AndroidAuto, r/CHR or r/CarHacking thread was indexed for a firmware-level AA mod on Touch 2. — (negative result)

### Inferences
- The YouTube titles match the marketing language of box sellers ("Factory Screen Transformation", "2014-2019", "2016-2020") and of the MirrorLink-converter campaign (same "Touch 2 2014–2019 CarPlay Upgrade" phrasing across rav4world, chrforums and YouTube). They should be treated as **category (e)** demonstrations until shown otherwise.
- The MirrorLink-converter posts look like a coordinated vendor seeding campaign: same text on several forums, a "prototype", and "cannot disclose details". Grade **D**.
- The 13T-era modding attempt (chrforums 4415) shows the update-signing chain is not trivially bypassable: the modified image fails at install reboot. Writing a converted CY17 image to a 13T unit's flash chip would also face different hardware (the CY17 DCU is an i.MX6Q platform with a separate Harman MEU). Hardware details of the 13T board were not found.

### Gaps
- No YouTube video description or comments could be read to confirm which of them are boxes.
- No public eMMC/NAND dump, teardown or chip identification of a 13TFDAEU-CA04 board was found, so the "rewrite a memory chip" claim cannot be assessed technically.
- The product name, price and real-world reports for the MirrorLink→CarPlay USB converter were not found.

## 5. Cases on a 2016-2019 pre-facelift C-HR specifically, and reports of bricks or failures

### Takeaway
No documented case was found of anyone obtaining CarPlay or Android Auto on a pre-facelift C-HR's original Touch 2 (with Go) through software, reflash or board swap. Every first-hand C-HR success involves an external interface box or adapter, or replacing the whole head unit with a later one. Bricking reports are found only for the CY17 Corolla/RAV4 retrofit (error 006/001) and for corrupted 13T units showing a "000000" software version.

### Cited Findings
- Toyota Owners Club "Android auto retrofit" (C-HR Club):
  - "Touch 2 multimedia units pre-dating MM17" are not compatible with AA/CarPlay; AA was offered as an upgrade only on MM17 units in MY19/20 Corolla and RAV4.
  - A Romanian interface box was considered.
  - "earlier Touch 2 head units aren't compatible" with a third-party box marketed for 2013-2018 units.

  — [Toyota Owners Club topic 204281](https://www.toyotaownersclub.com/forums/topic/204281-android-auto-retrofit/)
- Toyota Owners Club "Android auto" (C-HR Club): October 2019 onwards facelift C-HRs have AA/CarPlay fitted; earlier 2019 cars do not. — [Toyota Owners Club topic 230350](https://www.toyotaownersclub.com/forums/topic/230350-android-auto/)
- chrforums.uk "Definitive answer on Apple Carplay?": Toyota Customer Relations stated that Apple's list is the US list and "Apple CarPlay is NOT available on UK CHR 2019". — [chrforums.uk 2615](https://www.chrforums.uk/threads/definitive-answer-on-apple-carplay.2615/)
- chrforums.uk "Touch2 with Go Replacement options?": a member has CarPlay in a **67-plate (late 2017) C-HR via an aftermarket device**, but "the screen can be very unresponsive", "audio keeps dropping" and "maps lags quite a bit over Bluetooth". — [chrforums.uk 4528](https://www.chrforums.uk/threads/touch2-with-go-replacement-options.4528/)
- chrforums.uk "Head unit 2017 to 2019 with Carplay/Android Auto": discusses fitting a later head unit (whole-unit swap, needs rewiring). — [chrforums.uk 5141](https://www.chrforums.uk/threads/head-unit-2017-to-2019-with-carplay-android-auto.5141/)
- Toyota Owners Club "SUCCESS: CarPlay/Android Auto fitted in Mk3 with original Touch 2 stereo":
  - The owner used an off-the-shelf "autokit dongle" for wireless/wired CarPlay and wired AA, keeping touch and the reverse camera. The car is a Mk3 model, not a C-HR.
  - Another member notes that "all touch2's have AUX in, it just isn't wired on some models", and that "the Touch 2 is the DA (display audio) its only the Nav module that makes it 'GO'".

  — [Toyota Owners Club topic 203364](https://toyotaownersclub.com/forums/topic/203364-success-carplayandroid-auto-fitted-in-mk3-with-original-touch-2-stereo)
- Other C-HR owner threads asking the same question with no software solution: [toyotachrforum.com 6163](https://www.toyotachrforum.com/threads/can-i-install-use-android-auto-on-my-2017-2018-c-hr.6163/); [toyotachrforum.com 5342 (CarPlay dongle)](https://www.toyotachrforum.com/threads/apple-carplay-dongle.5342/); [chrforums.uk 4026](https://www.chrforums.uk/threads/android-auto-retrofit.4026/)

**Failures and bricks:**
- Corolla CY17 retrofit: the dealer hit **error 006** and "just gave up". Another owner got "error Code 006" while uploading the new firmware. Per a forum member, bulletin BE-00439T-TME states that if customers attempt the retrofit themselves and break the head unit, replacement is not covered under warranty. — [Toyota Owners Club 195353 p.17](https://www.toyotaownersclub.com/forums/topic/195353-retro-fit-apple-carplay-android-auto/page/17/); [p.18](https://www.toyotaownersclub.com/forums/topic/195353-retro-fit-apple-carplay-android-auto/page/18/)
- US 2018 Camry/Lexus CarPlay update thread: bricking is attributed to the car being switched off during writing. — [toyotanation 1652876 p.68](https://www.toyotanation.com/threads/apple-carplay-update-files-18-toyota-camry-sienna-18-19-lexus-models.1652876/page-68)
- 13T-family failure: a **13TFDAEU-DA00** unit showing version "000000" threw error 006 on "13TFDAEU-DA00_0001.kwi", and the owner could not find a recovery file. Bulletin **BE-0003T-0116** is cited as the patch for "00000000" software version. — [Toyota Owners Club 181735 p.2](https://www.toyotaownersclub.com/forums/topic/181735-touch-2-freezing-then-rebooting/page/2/); [Buschtaxi.net](https://forum.buschtaxi.org/update-toyota-touch-2-fehlerbehebung-t54384-75.html)
- The OpenTouch2 author got error 001 at 99%, recovered by power-cycle and retry, and had no bricks. — [GitHub OpenTouch2](https://github.com/edgardavey/toyota-touch2-dcu-carplay-fix)
- No report (success or brick) was found of a desoldered or reflashed 13T C-HR unit. — (negative result)

### Inferences
- The pre-facelift C-HR record consists only of box installs (with reported lag and audio drop-outs over Bluetooth-audio designs), unit swaps, and official refusals. This strongly suggests no working firmware-level method exists in the public domain for 13TFDAEU-CA04.
- Even Toyota's own signed CY17 retrofit fails regularly (error 006) on supported hardware. A cross-platform "converted" image written by chip programmer onto a 13T board would carry a far higher brick risk, plus loss of warranty and resale value.

### Gaps
- No bricking statistics exist; the reports are anecdotal.
- Whether the 13TFDAEU-CA04 board has a removable or desolderable eMMC/NAND, and its SoC, is not documented in any source found.

## 6. Classification of methods (a–e) and applicability to the owner's unit (13TFDAEU-CA04 / NA530)

### Takeaway
For the owner's 13TFDAEU-CA04 + NA530:
- (a) pure software unlock: **does not apply**. No CarPlay/AA code is known to exist in 13T firmware, and the official and commercial unlocks are CY17/17MM-only.
- (b) reflash with Corolla/RAV4 firmware: **only one unverified D-grade forum claim, technically implausible** given platform and signing differences.
- (c) internal board swap: **no documented case**.
- (d) facelift OEM unit swap: possible but out of scope; requires rewiring.
- (e) external interface boxes: the **only proven route on the original screen**. A MirrorLink→CarPlay USB dongle is a lighter variant, but it depends on MirrorLink still working on VE3947, which is doubtful.

### Cited Findings
**Identifier comparison:**

| Unit | Generation | Example | Software CarPlay/AA unlock? |
|---|---|---|---|
| Owner's C-HR | 13T* | 13TFDAEU-CA04 (same as totolito44's 03/2017 C-HR on VE3937) | None found |
| Eligible units | 17TDT1EU / 17TDT2EU, "17MM/CY17" | Panasonic DA01/DA02/DA30, Denso/Fujitsu CA01/CA02 | Official retrofit (UK, GR, EE, LV) and vendors |

— [hybridlife.org](https://hybridlife.org/threads/tutoriel-de-mise-%C3%A0-jour-de-toyota-touch-go-2.3945/page-45); [125coding](https://www.125coding.co.uk/product-page/toyota-ch-r-apple-carplay-android-auto-activation-software-update-2019-2021); [Toyota Greece](https://www.toyota.gr/owners/retrofit); [Toyota Estonia](https://ru.toyota.ee/owners/myt-connected-services/multimedia)

**Per category:**
- **(a) Pure software unlock of a present-but-disabled feature:** documented only for CY17 units, e.g. DA01 1020 → DA31 1023 on a 2020 RAV4. — [GitHub OpenTouch2](https://github.com/edgardavey/toyota-touch2-dcu-carplay-fix)
- **(b) Reflash with another Toyota unit's firmware:** one indexed hearsay post (hybridlife.org p.62) — [hybridlife.org](https://hybridlife.org/threads/tutoriel-de-mise-%C3%A0-jour-de-toyota-touch-go-2.3945/page-62). Countervailing technical evidence:
  - CY17 DCU uses HABv4 secure boot — [OpenTouch2 README](https://raw.githubusercontent.com/edgardavey/toyota-touch2-dcu-carplay-fix/main/README.md)
  - Modified older Touch 2 update images fail at install reboot — [chrforums.uk 4415](https://www.chrforums.uk/threads/modifying-touch-2-updates.4415/)
  - Signing keys make custom images "impractical" — [haxor.fi](https://haxor.fi/posts/how-the-firmware-updates-work-on-toyota-touch-go/)
- **(c) Internal board/module swap:** no source found. — (negative result)
- **(d) Whole-unit facelift swap:** discussed for 2017-2019 C-HR — [chrforums.uk 5141](https://www.chrforums.uk/threads/head-unit-2017-to-2019-with-carplay-android-auto.5141/). Toyota UK notes paying for part plus labour — [chrforums.uk 2615](https://www.chrforums.uk/threads/definitive-answer-on-apple-carplay.2615/)
- **(e) External boxes:** many vendors, roughly €349 / 560–1,799 PLN / about $73–$190 (see section 2). One 2017 C-HR owner reports lag and audio drops — [chrforums.uk 4528](https://www.chrforums.uk/threads/touch2-with-go-replacement-options.4528/)
- **MirrorLink-based USB converter:** vendor claims only — [toyotaenthusiasts.com](https://www.toyotaenthusiasts.com/forum/threads/activate-carplay-on-your-toyota-touch2-no-head-unit-replacement-needed.72/). MirrorLink reportedly stopped working on 13TFDAEU-CA04 after VE3934 — [toyotacamry.ru](https://toyotacamry.ru/showthread.php?page=41&t=12140)
- **Updates without CarPlay:** HybridLife indicates maps up to 2024v2 and nav firmware up to 6.24.0WH are installable on these units; the owner is on 6.11.0WH / map 2018 v1. — [hybridlife.org thread 3945](https://hybridlife.org/threads/tutoriel-de-mise-%C3%A0-jour-de-toyota-touch-go-2.3945/page-62)

**Evidence-strength summary:**

| Source | Grade | Basis |
|---|---|---|
| GitHub OpenTouch2 | A | For a RAV4 CY17 DCU; not applicable to the owner's unit |
| Toyota UK / GR / EE / LV official pages | A | Eligibility; exclude the owner's unit by omission and by staff replies |
| 125coding, navi174, mda-tech, fabryczne.pl | D | Vendor claims, but consistent with the CY17-only scope |
| toyotacamry.ru MirrorLink-loss report | B | Exact ID, versions given; single source |
| chrforums 4415 modding attempt | B/C | |
| chrforums 4528 box experience | C | |
| hybridlife.org desoldering post | D | |
| MirrorLink converter posts and YouTube C-HR videos | D | Titles only |

### Inferences
- "13T" vs "17T" in the device ID most likely marks the 2013-platform (CY13) versus 2017-platform (CY17) DCU generation. The "CA" suffix likely marks the Denso/Fujitsu Ten-built variant, by analogy with 125coding's "17TDT1EU-CA01 (Denso/Fujitsu)" labelling. This is inferred from naming, not confirmed by a Toyota document.
- NA530 / 6.x.xWH is the older "Go" navigation module. The OpenTouch2-documented CY17 path requires a different Harman MEU (17TMT2EU-FA00/FA10). The owner's nav hardware is therefore also outside the CY17 retrofit chain (inference).
- Practical conclusion for the owner:
  - No credible, documented way exists to add AA/CarPlay to the original 13TFDAEU-CA04 unit by software or reflash.
  - Anyone offering a "chip reprogramming with Corolla/RAV4 firmware" should be asked for before/after photos of the unit's version screen (device ID 13TFDAEU-CA04 shown) and a refund or brick guarantee.
  - The realistic choices are an interface box (e), a MirrorLink USB converter (test MirrorLink on VE3947 first), or a whole-unit swap (d).

### Gaps
- No Toyota document was found that explicitly decodes "13TFDAEU" or "CA04", or states "CY13 units excluded" in words.
- Whether VE3947 still exposes MirrorLink on 13TFDAEU-CA04 is unverified. The owner can check this on the unit (Settings, phone or apps menu).
- No hands-on reports were found for the MirrorLink→CarPlay converter on a C-HR.
- Blocked fetches (hybridlife.org, toyotaownersclub.com, youtube.com, latestsatnav.co.uk) mean post dates, usernames, images and full context could not be verified. A follow-up with those hosts allowed could confirm the page-62 post author, date and car.
