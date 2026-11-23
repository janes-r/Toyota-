# Hardware identity of the Toyota Touch 2 (with Go) unit in a European C-HR (first registered July 2018)

Research notes by a research subagent. Date of research: 2026-11-23.

Identifiers from the car: Navigation info = SW 6.11.0WH, map "2018 v1", device ID "NA530 / 98D1 / S5jJ / 2KcW / yeM0g / 8212"; Audio info = SW VE3947, device ID 13TFDAEU-CA04; VIN NMTKZ3BX20R188882; physical buttons and rotary knobs; original Toyota reversing camera.

Evidence labels used below:
- VERIFIED = official Toyota/Harman source, or several independent sources that agree.
- COMMUNITY = owner forums, sellers or a community GitHub project; plausible but not official.
- HYPOTHESIS = my own inference; must be checked on the car.

Access caveat for the report writer: in this session, WebFetch could not reach manuals.plus, toyotaownersclub.com or forum.toyotaklub.org.pl (DNS blocked by the sandbox network policy). For those sites the content below comes only from search-engine summaries and snippets, not full-page reads. github.com and raw.githubusercontent.com were readable in full.

## 1. Who makes this unit: Display Audio (DA) versus navigation module

### Takeaway
The European Touch 2 has two parts. The base "Display Audio" (DA) unit, with the screen, buttons, knobs, radio and audio, is made by Panasonic; the audio device ID 13TFDAEU-CA04 and the software VE3947 belong to it. The "Go" navigation is a separate Harman "Extension Box" (module) bolted to the DA; the navigation software 6.11.0WH and the 26-character device ID belong to it. Toyota's own repair documentation and a Harman press release support this split. Neither Denso Ten/Fujitsu Ten nor Aisin appears for the EU Touch 2.

### Cited Findings
- Toyota's Touch 2 repair/diagnostic manual describes two possible configurations: "Display Audio only (Touch 2)" and "Display Audio + Extension Box (Touch 2 With Go)". It names Panasonic as the supplier of the Display Audio and Harman as the supplier of the Extension Box. The manual covers "all Toyota vehicles equipped Touch 2 or Touch 2 with Go except Aygo, ProAce and Land Cruiser 200". (COMMUNITY mirror of an official Toyota document.) — [ManualsLib: Toyota Touch 2 Repair Manual](https://www.manualslib.com/manual/1813654/Toyota-Touch-2.html); [Scribd: Touch 2 with Go Diagnostic Manual EN](https://www.scribd.com/document/527123336/Touch-2-with-Go-Diagnostic-Manual-EN)
- The same repair manual notes that the "Touch2 with go navigation extension box" brings a hardware fix for a Display-Audio-only issue on certain models, naming Hilux, C-HR and Yaris. — [ManualsLib Toyota Touch 2 Repair Manual](https://www.manualslib.com/manual/1813654/Toyota-Touch-2.html) (search-snippet level)
- VERIFIED: Harman's 2014 press release says Harman provides "enhanced navigation and connected services as an add-on module for the Touch 2 on-board infotainment system in the new Toyota Yaris" (the "Go" module). — [HARMAN newsroom: HARMAN On Board New Toyota Yaris in 2014](https://news.harman.com/releases/harman-on-board-new-toyota-yaris-in-2014); [Automotive World copy](https://www.automotiveworld.com/news-releases/harman-board-new-toyota-yaris-2014/)
- An owner's technical blog says the "Touch&Go 2" is the same base unit as the Touch 2, "but with an extra processor and software module stuck on its back". On cars with the Go module, the car's USB port is wired to that module, not to the base unit. — [blog.mbirth.uk: Toyota Touch 2 Firmware Update (2017)](https://blog.mbirth.uk/2017/10/21/toyota-touch-2-firmware-update.html)
- Toyota UK owners' forum: adding Go is "not a software change, It's a physical add on module or replacement stereo". (COMMUNITY) — [Toyota Owners Club: Technical: Touch2 and Touch2 and/with Go](https://www.toyotaownersclub.com/forums/topic/189515-technicaltouch2-and-touch2-andwith-go/)
- A map/equipment seller lists the original Harman extension modules for Touch 2 as "Extension Module by HARMAN (Touch 2 with Go)" and "High Module (BE 7720) by HARMAN" (Go Plus). (COMMUNITY/seller) — [toyotamaps.online: Harman Go](https://toyotamaps.online/equipment/original-extension-box-for-toyota-touch-2-(harman-go)); [toyotamaps.online: Harman Go Plus High Module BE 7720](https://toyotamaps.online/equipment/original-extension-box-for-toyota-touch-2-(harman-go-plus))
- Other region / other generation: the 2019+ "new Touch 2" in EU RAV4 and Corolla keeps the same split, with a Panasonic DCU (17TDT2EU-DA01) and a Harman MEU (17TMT2EU-FA00/FA10). (COMMUNITY) — [GitHub edgardavey/toyota-touch2-dcu-carplay-fix](https://github.com/edgardavey/toyota-touch2-dcu-carplay-fix)
- Other region (USA): Toyota's US TSB T-SB-0043-21 is titled "Audio Head Unit Software Update (Panasonic)", which shows that Panasonic also supplies Toyota's US Entune head units. — [NHTSA: T-SB-0043-21 (PDF)](https://static.nhtsa.gov/odi/tsbs/2022/MC-10207940-9999.pdf)
- A Russian forum participant says the same model can have units from "denso, Panasonic, fujitsu, pioneer" with different firmware. The post is general and does not concern the EU Touch 2 specifically. — [autoprogs.ru: Обновления для ШГУ Toyota Touch 2](https://autoprogs.ru/diagnostika-toyota-lexus-remont-elektroniki-151/obnovleniya-dlya-shgu-toyota-touch-2-a-27176/index19.html) (search summary)

### Inferences
- HYPOTHESIS (strong): in this C-HR, "Audio info" (VE3947 / 13TFDAEU-CA04) is read from the Panasonic DA, and "Navigation info" (6.11.0WH / 26-character device ID / map 2018 v1) is read from the Harman extension box. Two independent software trees and version schemes (VExxxx versus 6.x.x) support this.
- HYPOTHESIS: if the mbirth description holds for the C-HR, the car's USB socket goes to the Harman box, not to the Panasonic DA. This matters for any Android Auto or USB-based plan.
- I found no source linking Denso Ten (Fujitsu Ten), Aisin or Pioneer to the European 2016-2019 C-HR Touch 2.

### Gaps
- No physical label photo of a C-HR 13TFDAEU unit was found that confirms "Panasonic" on the chassis label. Proposed check: remove the unit and photograph the label (see section 7).
- I could not confirm where the Harman box sits in the C-HR (on the back of the DA versus elsewhere), or its exact part number.

## 2. Decoding the on-screen identifiers (13TFDAEU-CA04, VE3947, 6.11.0WH, NA530..., 2018 v1)

### Takeaway
No official decoding table was found. The structure can still be pinned down from many examples. "13TFDAEU-CA04" is the Panasonic DA's model/firmware-compatibility ID: 13 = MM13/CY2013 hardware generation, T = Toyota, FDA = a Display Audio variant code, EU = Europe, CA04 = sub-variant. "VE3947" is the DA firmware version. "6.11.0WH" is Harman Go software 6.11.0, where "H" most likely means the High (Go Plus) module. The six "extra IDs" are not separate IDs: together with "NA530" they make one 26-character, case-sensitive map-registration device ID.

### Cited Findings
**13TFDAEU-xxxx (Audio device ID)**
- The string 13TFDAEU-DAxx (DA00 to DA08) appears in many owner threads as the "device ID" of Touch 2 DA units in Auris and Corolla (2014-2018). DA04 is described as a non-navigation unit, and a Polish thread lists DA02 and DA03 as targets of a given firmware package. (COMMUNITY) — [Toyota Owners Club: Touch 2 freezing then rebooting p.2](https://www.toyotaownersclub.com/forums/topic/181735-touch-2-freezing-then-rebooting/page/2/); [toyotaklub.org.pl: Toyota Touch 2 firmware update (Display Audio Software)](https://www.forum.toyotaklub.org.pl/index.php?topic=45711.165)
- Firmware files are named after this ID, with the suffix acting as a compatibility key. Examples: "13TFDAEU-CA43_9999.kwi" (Russian Corolla forum), "13TFDAEU-DA02_0141.kwi" (French Hybrid Life forum), "13TXDAEU-CA42_9999.kwi" (mbirth blog, Yaris-family unit). — [corolla-club.ru p.18](https://corolla-club.ru/showthread.php?t=93&page=18); [hybridlife.org tutorial p.50](https://hybridlife.org/threads/tutoriel-de-mise-%C3%A0-jour-de-toyota-touch-go-2.3945/page-50); [blog.mbirth.uk](https://blog.mbirth.uk/2017/10/21/toyota-touch-2-firmware-update.html)
- Files for DA01 and DA04 "are not recognized by DA00 units", and with a different ID the update does not start. This shows the unit's updater checks the suffix. (COMMUNITY) — [corolla-club.ru p.18](https://corolla-club.ru/showthread.php?t=93&page=18)
- A Spanish C-HR owner reports exactly "VE3947" with "13TFDAEU-CA04". The forum reply says that car has no navigation module (no nav device ID in settings). The CA04 suffix therefore occurs on C-HRs with and without Go. — [clubtoyotachr.com: Device ID y Navegador](https://www.clubtoyotachr.com/threads/device-id-y-navegador.12830/)
- The sister ID "13TXDAEU-CA02 / CA04" is reported on Yaris, C-HR and Hilux units, paired with software versions "XE3864" and "HE3945". — [Toyota Owners Club: How to update software on 2015 Excel Hybrid 1.5](https://www.toyotaownersclub.com/forums/topic/181676-how-to-update-software-on-2015-excel-hybrid-15/); [Toyota Owners Club: Firmware upgrade p.10](https://www.toyotaownersclub.com/forums/topic/189278-firmware-upgrade/page/10/)
- A third-party guide to Toyota's "How to identify T2wG and Device ID" document states that DA-only units (Touch 2 without Extension Box) have device IDs starting with 13, 14 or 16, and that Touch 2 with Go software versions are 3.x.x, 4.x.x and 6.x.x, matching generations "MM13-14-16". (COMMUNITY copy of a Toyota document; read only via search summary) — [manuals.plus: DA & Ext. Box – How to Identify T2wG and Device ID – How to access the Service](https://manuals.plus/m/dbcc4aa12f48c082de538094557d54ae2edc6f1eca4b23e5e000fd166c5fc68c.pdf)
- Related ID family from other generations and regions: "17TDT2EU-DA01" (2019+ EU Panasonic DCU) and "17TMT2EU-FA00/FA10" (2019+ EU Harman MEU), firmware files such as "17TDT2EU-DA01_7910.kwi" — [GitHub edgardavey/toyota-touch2-dcu-carplay-fix](https://github.com/edgardavey/toyota-touch2-dcu-carplay-fix). US Entune: "15TBDANA-CA01_1116.kwi" is said to install "version UU.11.16" Entune device driver and audio — [fileinfo.com .KWI](https://fileinfo.com/extension/kwi); [filext.com KWI](https://filext.com/file-extension/KWI) (file-extension reference sites; low authority)
- Owners also report that Touch 2 DA firmware updates are distributed as .kwi files on a FAT32 USB stick. — [blog.mbirth.uk](https://blog.mbirth.uk/2017/10/21/toyota-touch-2-firmware-update.html); [autoprogs.ru](https://autoprogs.ru/diagnostika-toyota-lexus-remont-elektroniki-151/obnovleniya-dlya-shgu-toyota-touch-2-a-27176/index19.html)
- Background on ".kwi": "KIWI" is a Japanese-proposed format for car-navigation map data storage (ISO TC204/WG3). Denso began producing KIWI-based navigation in 1999. Whether Toyota's .kwi firmware packages actually use KIWI is unverified. — [SWOV: World wide vehicle navigation system using KIWI format](https://swov.nl/en/publicatie/world-wide-vehicle-navigation-system-using-kiwi-format)

**VE3947 (Audio software version)**
- A C-HR owner thread quotes "My version is VE3947 Nav version is 6.11.0WH Map ID is 2018 v1", matching this car's identifiers exactly. — [chrforums.uk: Touch 2 Software Update](https://www.chrforums.uk/threads/touch-2-software-update.2622/); see also [Toyota Owners Club: 6.11 Touch and go update](https://www.toyotaownersclub.com/forums/topic/184462-611-touch-and-go-update/) (search snippet; which of these two threads the quote comes from was not confirmed)
- No document explaining the "VE" prefix or the "3947" number was found.

**6.11.0WH (navigation software, Harman box)**
- Owners report 6.11.0WH as the correct update for the UK C-HR Excel. A file ending in "H" instead of "WH" produced an activation-key error. — [chrforums.uk: Touch 2 Software Update](https://www.chrforums.uk/threads/touch-2-software-update.2622/) / [Toyota Owners Club: 6.11 Touch and go update](https://www.toyotaownersclub.com/forums/topic/184462-611-touch-and-go-update/) (search snippets)
- Suffix meaning, per COMMUNITY sources: "L" = low version (Touch 2 with Go) and "H" = high version (Touch 2 with Go Plus), according to a German Prius forum citing an Avensis forum. A Russian update seller states "WL" = Low (Touch 2 with Go) and "WH" = Touch 2 with Go Plus. — [priusfreunde.de: Meine Software Version steht nicht in My Toyota](https://www.priusfreunde.de/portal/index.php?option=com_kunena&Itemid=117&func=view&catid=55&id=552985); [navi174.ru product page](https://navi174.ru/index.php?route=product%2Fproduct&product_id=142)
- "6.11.0.WL / Map ID 2018 V1 came out in the early part of the year (April-ish)" [2018]. — [Toyota Owners Club: 6.11 Touch and go update](https://www.toyotaownersclub.com/forums/topic/184462-611-touch-and-go-update/); also [toyotamaps.online: Toyota Touch 2018 update is out (2018 v1)](https://toyotamaps.online/blog/news/toyota-touch-2018-update-is-out-(2018-v1))
- "6.11.2H" was a patch for 6.11.0 (August 2018). — [drive2.ru: Toyota Touch 2 with Go (High) map 2018v1](https://www.drive2.ru/l/499879218746753493/)
- Current latest for this family: "6.24.0WH, cartes 2024v2", and "AndroidAuto ne peut pas être officiellement activé sur ce système" (Android Auto cannot be officially enabled on this system). The 6.11.0WH package is about 7.2 GB and needs a USB 2.0 stick larger than 8 GB. — [hybridlife.org: Tutoriel de mise à jour de Toyota Touch & Go 2](https://hybridlife.org/threads/tutoriel-de-mise-%C3%A0-jour-de-toyota-touch-go-2.3945/page-67); [chrforums.uk](https://www.chrforums.uk/threads/touch-2-software-update.2622/) (search snippets)
- VERIFIED (Toyota): the 2016 Touch 2 with Go (the MM16 software generation, "6.x.x") introduced a tile-based menu, split screen and auto-navigation. "A higher grade Touch 2 with Go system further features voice recognition, a text-to-speech function and 3D navigation mapping." "Brand new models such as the Toyota C-HR will have this latest generation system from the start of production." — [Toyota UK Magazine: 2016 Toyota Touch 2 with Go multimedia system](https://mag.toyota.co.uk/2016-toyota-touch-2-with-go-multimedia-system/); [Toyota Europe newsroom: Toyota Touch 2 with Go](https://newsroom.toyota.eu/toyota-touch-2-with-go/)

**NA530 98D1 S5jJ 2KcW yeM0g 8212 (navigation device ID)**
- VERIFIED (Toyota UK FAQ): the Touch & Go / Go Plus device ID is "a 26-digit code" made of numbers, letters and symbols. It is case-sensitive and must be entered exactly, without spaces, for My Toyota map registration (with the VIN). It is shown under Setup > General > System information. — [Toyota UK Magazine: Touch & Go, Touch & Go+ and Touch Pro FAQs](https://mag.toyota.co.uk/toyota-touch-go-touch-go-and-toyota-touch-pro-faqs/); [Toyota UK Magazine: How to register your Touch & Go system](https://mag.toyota.co.uk/toyota-touch-go-how-to-register-your-touch-go-system/)
- A Toyota-reported case: a Touch-only unit with no sat-nav has no device ID / System information, and "you only get a device ID when Satnav is installed". — [Toyota Owners Club: Touch And Go Device Id](https://www.toyotaownersclub.com/forums/topic/163068-touch-and-go-device-id/) (search summary)

### Inferences
- VERIFIED BY CALCULATION (my own): "NA530" + "98D1" + "S5jJ" + "2KcW" + "yeM0g" + "8212" = exactly 26 characters, which matches Toyota's stated 26-character device-ID format. The "extra IDs" are therefore the rest of a single device ID that wraps over several lines: `NA53098D1S5jJ2KcWyeM0g8212`. It is a per-unit activation/registration token for the Harman navigation module and map licensing. No public decoding exists, and "NA530" should not be read as a model number. Treat it as semi-private, because it is tied to map entitlements.
- HYPOTHESIS (structure of 13TFDAEU-CA04), based on comparing 13TFDAEU / 13TXDAEU / 15TBDANA / 17TDT2EU / 17TMT2EU:
  - `13` = hardware platform generation/year (CY2013, "MM13"). This fits Toyota's "MM13/14/16" naming, and "17T..." is the CY17 successor. The C-HR (launched 2016) still carries 13-generation DA hardware with MM16 software.
  - `T` = Toyota brand.
  - `FDA` = unit type: "DA" = Display Audio (Toyota's term in the repair manual); "F" (versus X, B) = a hardware/vehicle-family variant letter whose meaning is unknown. "DT2" (DCU Touch 2) and "MT2" (MEU Touch 2) are the 2017-generation equivalents.
  - `EU` = Europe; compare `NA` = North America in 15TBDANA.
  - `-CA04` = sub-variant / firmware compatibility index checked by the updater. "CA" versus "DA" probably marks a different hardware or software branch, and "04" is the variant index. CA04 does not encode whether Go is fitted (it appears on non-Go C-HRs too).
  - Nothing here supports "FDA" meaning anything regulatory.
- HYPOTHESIS: the DA software version may be built as [variant letter][region letter "E"][4-digit build], since XE3864, HE3945 and VE3947 all have "E" second. The "X" in XE3864 matches the "X" in 13TXDAEU, but "V" does not match the "F" in 13TFDAEU, so this mapping is unproven.
- HYPOTHESIS (important for the owner): by the community "L = Go / H = Go Plus" convention, "6.11.0WH" means this car's Harman module is probably the High (Go Plus) variant, not the basic Go. Toyota's description of the higher grade gives a simple test on the car: if the unit offers voice recognition, text-to-speech and 3D map rendering, it is the High (Go Plus) module. The meaning of "W" is unknown (possibly the 2016+ wide/MM16 build family).

### Gaps
- No official Toyota/Panasonic table decoding 13TFDAEU, CA/DA suffixes or the VE prefix was found. The Toyota document "How to Identify T2wG and Device ID" (mirrored on manuals.plus) could not be fetched in full; it may contain the official table.
- I could not determine whether "CA04" corresponds to a specific screen size (C-HR 8") or the camera/button variant.

## 3. VIN NMTKZ3BX20R188882 decoded

### Takeaway
A Toyota C-HR built by Toyota Motor Manufacturing Turkey (Sakarya), almost certainly the 1.8 hybrid (ZYX10, 2ZR-FXE). The European VIN does not encode model year; position 10 is "0". Position 9 is a valid check digit.

### Cited Findings
- Positions 1-3 `NMT` = Toyota Motor Manufacturing Turkey (WMI), per Toyota's own C-HR VIN coding document filed with NHTSA and the Wikibooks Toyota VIN table. — [NHTSA vPIC: Toyota C-HR VIN coding system 22MY](https://vpic.nhtsa.dot.gov/mid/home/displayfile/78ed23ee-b376-496d-b51e-a7c5e5c7edde); [Wikibooks: Toyota VIN codes](https://en.wikibooks.org/wiki/Vehicle_Identification_Numbers_(VIN_codes)/Toyota/VIN_Codes)
- Position 11 `R` = TMMT plant, Adapazarı/Arifiye, Sakarya, Turkey. — [Wikibooks: Toyota VIN codes](https://en.wikibooks.org/wiki/Vehicle_Identification_Numbers_(VIN_codes)/Toyota/VIN_Codes); [automobilisto.de Toyota VIN decoder](https://automobilisto.de/en/tools/vin-decoder/toyota)
- Position 4 `K` corresponds to the C-HR line, per a commercial decoder; the US-market Turkish C-HR uses the prefix "NMTKHMBX". — [bumper.com C-HR VIN decoder](https://bumper.com/vin-decoder/toyota/c-hr); [forcar.org NMTKHMBX… example](https://forcar.org/vin-check/NMTKHMBX3JR029329/)
- Position 5: in the US C-HR VIN coding, position 5 "H" = 3ZR-FAE (2.0 petrol), so position 5 is the engine field in that scheme. A decoder site maps "NMTKZ3BX" to ZYX10 / 2ZR-FXE (1.8 hybrid); not confirmed from an official EU source. — [NHTSA vPIC C-HR coding doc](https://vpic.nhtsa.dot.gov/mid/home/displayfile/78ed23ee-b376-496d-b51e-a7c5e5c7edde); [automobilisto.de](https://automobilisto.de/en/tools/vin-decoder/toyota) (search summary)
- Every used-car listing found with the "NMTKZ3BX" prefix was a C-HR 1.8 Hybrid (90 kW / 122 PS), model years about 2016-2022. — search results for "NMTKZ3BX", e.g. [autobazar.eu C-HR 1.8 Hybrid](https://www.autobazar.eu/en/detail/toyota-c-hr-18-hybrid-neon-lime-powered-by-jbl/AbIr49O2utX/), [otomoto.pl C-HR 1.8 Hybrid](https://www.otomoto.pl/osobowe/toyota/c-hr/ver-1-8-hybrid-dynamic)
- The European C-HR (ZYX10) uses the 2ZR-FXE 1.8 L hybrid; NGX10 is the 1.2T petrol. — [Wikipedia: Toyota C-HR](https://en.wikipedia.org/wiki/Toyota_C-HR)
- In the North American scheme, position 10 is the model year (J = 2018, K = 2019); "0" is not a valid year code there. — [bumper.com C-HR VIN decoder](https://bumper.com/vin-decoder/toyota/c-hr)

### Inferences
- VERIFIED BY CALCULATION (my own, ISO 3779/North American weighted check-digit algorithm): sum = 442, 442 mod 11 = 2, which equals position 9 = "2". The VIN is internally consistent and was read correctly.
- Full decode (HYPOTHESIS where marked): NMT = TMMT Turkey | K = C-HR line | Z = 2ZR-FXE 1.8 hybrid (strongly supported by listings; not official) | 3, B, X = grade/body/restraint descriptors (meaning not found for the EU scheme) | 2 = check digit | 0 = no model year encoded (EU practice) | R = Sakarya plant | 188882 = serial.
- With first registration in July 2018, the car is MY2018 pre-facelift (AX10, first generation), which fits the 13T-generation DA plus MM16 Harman software.

### Gaps
- An official EU Toyota VIN coding table for positions 6-8 ("3BX") was not found. The exact production date, grade and option codes (e.g. Go versus Go Plus, JBL or not) can be read from a Toyota EPC/dealer VIN lookup or the VIN plate / B-pillar label.

## 4. Toyota part numbers (86140 / 86100 / 86840) for the C-HR 2016-2019 EU unit

### Takeaway
Only seller-level evidence exists. 2017-2019 C-HR head units are sold used as 86140-F4010 / 86140-F4011. 2020+ facelift units use 86140-F4090 / F4220 / F4221 / F4530. No source maps a part number to "13TFDAEU-CA04" or to the C-HR's Harman Go box. 86100-YY050/YY060 Harman extension boxes appear in US/other-model listings.

### Cited Findings
- eBay: "Toyota CHR 2017 2019 OEM head unit stereo radio touch screen 86140F4010 4011" (manufacturer part number 86140F4011). (COMMUNITY/seller, unverified) — [eBay UK 404960270198](https://www.ebay.co.uk/itm/404960270198); [eBay CA same listing](https://www.ebay.ca/itm/404960270198)
- Facelift (2020+) C-HR units: 86140-F4220 / F4221 (hybrid, with nav), 86140-F4530 (hybrid, with nav) and 86140-F4090 (2020-2023 "Design"). These are the "new Touch 2" generation, not this car's unit. — [eBay 404951252268](https://www.ebay.co.uk/itm/404951252268); [eBay 406191750858](https://www.ebay.com/itm/406191750858); [eBay 405157765720](https://www.ebay.com/itm/405157765720); [eBay 187711296432](https://www.ebay.co.uk/itm/187711296432)
- Harman "Extension Box" 86100-YY050 / YY060 (Harman PT296-47120) is listed for Highlander, Prius and Camry. These are mostly US/other-market listings; none mention the C-HR. — [eBay product 3023155550](https://www.ebay.com/p/3023155550); [eBay 327059111839](https://www.ebay.com/itm/327059111839); [PriusChat: Compatibility of Extension Module versions (86100-YY050)](https://priuschat.com/threads/compatibility-of-extension-module-versions-86100-yy050.219132/)
- 2019+ EU "new Touch 2" (RAV4/Corolla): DCU 86140-42571 (17TDT2EU-DA01); MEU 86840-06041 → 86840-K0010 after the CarPlay conversion (Toyota bulletin BE-00439T-TME, "Toyota RAV4 with navigation system, Corolla SD/HB/TS... (with Panasonic, Harman) - Retrofit", v4, 18 Sep 2020). (COMMUNITY) — [GitHub edgardavey/toyota-touch2-dcu-carplay-fix README](https://raw.githubusercontent.com/edgardavey/toyota-touch2-dcu-carplay-fix/main/README.md)

### Inferences
- HYPOTHESIS: 86140-F4010/F4011 are the 2016-2019 C-HR DA (Panasonic, 13TFDAEU family), probably with the -F4011 supersession. Whether the Go box is part of that number or a separate 86100/86840 number is unknown. Do not treat this as confirmed.

### Gaps
- No Toyota EPC extract or label photo tying 86140-F40xx to 13TFDAEU-CA04 was found, and no part number was found for the C-HR Harman Go / Go Plus module. Proposed ways to obtain them: a Toyota dealer EPC lookup by VIN (group 8614 "Radio receiver/Navigation" and 8610); or remove the unit and read the label (section 7).

## 5. SoC, RAM, flash, OS, bootloader, debug ports

### Takeaway
For the 2014-2018 "13T" Panasonic DA and its Harman Go box, I found no source naming the SoC, RAM, flash chip or operating system. This is the biggest gap. Community evidence only says that the DA has two boards (DAB on the upper one), JTAG, SDIO and UART on board, and a 224-ball BGA storage ("SD") chip. Firm data exists only for neighbouring generations: the 2010-2013 first-generation Touch & Go (QNX on a TI DM3730, inferred) and the 2019+ "new Touch 2" Panasonic DCU (NXP i.MX6Q, eMMC, U-Boot 2009.08, Yocto/AGL Linux, NXP HABv4; community, partly unverified).

### Cited Findings
**This generation (13T DA, 2014-2018, EU) – COMMUNITY only**
- An owner probing a Touch 2: "there is jtag, SDIO and Uart on board". He wanted to read "the SD chip" directly, which is a 224-pin BGA. "The touch 2 has 2 boards the DAB is on the upper board." Chip vendors were not named. — [Toyota Owners Club: Technical: Touch2 and Touch2 and/with Go](https://www.toyotaownersclub.com/forums/topic/189515-technicaltouch2-and-touch2-andwith-go/) (search summary)
- A Yaris forum user notes there is "little to no information on the structure or how its extracted for newer Touch 2 .kwi files". — [Toyota Owners Club: Firmware upgrade p.2](https://www.toyotaownersclub.com/forums/topic/189278-firmware-upgrade/page/2/) (search summary)
- No teardown naming the SoC of the Touch 2 DA was found in English, Russian or Polish sources (searches on drive2.ru, autoprogs.ru, corolla-club.ru and toyotaklub.org.pl found only firmware threads). — e.g. [autoprogs.ru thread](https://autoprogs.ru/diagnostika-toyota-lexus-remont-elektroniki-151/obnovleniya-dlya-shgu-toyota-touch-2-a-27176/index44.html)
- Allwinner (A31S) and MediaTek CPUs mentioned in Touch 2 contexts belong to aftermarket Android navigation boxes, not the factory unit. — [car-solutions.com: Navigation system for Toyota Touch 2](https://car-solutions.com/en/navigation-system-for-toyota-touch-2/); [toyotamaps.online Trendcar NAV-RDL01](https://toyotamaps.online/equipment/nav-rdl01-android-8-navigation-unit-for-toyota-touch-2)

**Previous generation: Toyota Touch & Go (2010-2013), not this unit**
- A reverse-engineering write-up says the head unit runs QNX Neutrino on a board that "appears" to use a TI DM3730 (OMAP3, ARMv7). Radio and navigation are handled by a Toyota-specific extension box that "may" use a Renesas V850. The updater expects swdl.iso on USB, flashes IPL/IFS images and ETFS/MMC filesystems, and the images are signed. (Inferred by the author.) — [haxor.fi: How the firmware updates work on Toyota Touch & Go](https://haxor.fi/posts/how-the-firmware-updates-work-on-toyota-touch-go/); [jkry.org Oulu hack page](https://www.jkry.org/ouluhack/Toyota%20Touch%20&%20Go)

**Next generation: "new Touch 2" Panasonic DCU 17TDT2EU (2019+ RAV4/Corolla EU), not this unit, COMMUNITY**
- "NXP i.MX6Q, confirmed", "SABRE-SD reference board, U-Boot 2009.08, Yocto/Automotive-Grade-Linux-based". The intervention script writes "to the eMMC's bootloader region"; the system has A/B kernel and rootfs banks; the update script logs to /dev/ttymxc0 (i.MX UART, header presumed but not confirmed). It boots "via NXP's HABv4 secure boot", but "Nobody has checked this for the Panasonic Touch 2 DCU yet". Update modules are named AMIGO, SYS, CAN, NOR, UBOOT, SECURE and MAIN. The README gives no method for the "confirmed" platform claims; its fixes came from "inspecting the files on the official USB packages". — [GitHub edgardavey/toyota-touch2-dcu-carplay-fix README](https://raw.githubusercontent.com/edgardavey/toyota-touch2-dcu-carplay-fix/main/README.md)
- Other OEM context: Renesas R-Car H3/M3 were adopted by Toyota for next-generation (2021+) Toyota/Lexus multimedia, which is not relevant to the 2018 C-HR. — [Business Wire / Renesas 2021](https://www.businesswire.com/news/home/20211025005878/en)
- Panasonic Automotive publishes GPL/LGPL source for some Toyota products (e.g. a "Wireless Receiver" for Toyota Motor Sales USA, with Linux/GPLv2 components). No Touch 2 (EU) OSS notice was found. — [Panasonic Automotive OSS: Toyota Motor Sales USA wireless receiver](https://automotive.panasonic.com/en/corporate/about/officelist/pasa/license/toyota-motor-sales-usa-wireless-receiver); [car.panasonic.jp OSS index example](https://car.panasonic.jp/oss/k01nfs91/)

### Inferences
- HYPOTHESIS (unverified, medium/low confidence): Panasonic's 2019 DCU (i.MX6Q + U-Boot 2009.08 + Linux) carries an old Freescale-BSP-era bootloader, which suggests a platform lineage from the early-2010s Freescale i.MX ecosystem. The 2013-generation Panasonic DA might therefore also be Freescale/NXP i.MX-based (i.MX5x or i.MX6) running embedded Linux, but no evidence of this was found. An SoC from Renesas (SH-Navi / R-Car E1/M1) or TI cannot be ruled out. The 224-BGA "SD chip" fits a managed-NAND/eMMC-style storage package better than SPI NOR; also unverified.
- HYPOTHESIS: the Harman Go module, as a separate navigation computer with its own 6.x software, signed activation (activationCode.xml mentioned by owners) and its own device ID, is a separate embedded system. Its OS (QNX is common in Harman products of that era, but this is not evidenced) and SoC are unknown.
- Practical implication: without a teardown, any claim about this unit's chips must be presented as unknown.

### Gaps
- SoC, RAM, flash part, OS and bootloader of the 13TFDAEU DA and of the C-HR Harman Go module: not found. Proposed ways to obtain them: (a) a teardown photo of the main board (read the BGA top markings: CPU, DDR, eMMC/NAND); (b) in the service menu (section 7), look for version strings that name a kernel, QNX or U-Boot; (c) unpack a 13TFDAEU .kwi package and look for magic bytes or strings (e.g. "U-Boot", "Linux version", "QNX", "IFS", "UBI", "squashfs"); (d) look for a Panasonic or Toyota OSS/licence screen in Setup > General (an "Open source licences" item would name Linux/GPL components); (e) request the GPL source from Panasonic Automotive if a licence notice is shown.
- UART/JTAG pinouts are not documented publicly (the forum poster had not found schematics).

## 6. Generational differences: Touch & Go → Touch 2 → Touch 2 with Go / Go Plus → "new Touch 2" (CarPlay/AA)

### Takeaway
- Touch & Go (gen 1, ~2010-2013): QNX/DM3730 (inferred).
- Touch 2 (2014+, "MM13" hardware, 13T IDs): Panasonic DA plus an optional Harman Go (Low) or Go Plus (High) extension box. Software families 3.x (MM13), 4.x (MM14) and 6.x (MM16). This C-HR unit is in this family.
- "New Touch 2" (CY17/"17MM", 2019 Corolla E210 / RAV4 XA50): a new Panasonic DCU (17TDT2EU, i.MX6Q/Linux per community) plus a Harman MEU (17TMT2EU). CarPlay/Android Auto came through the 19MM software, retrofit or factory MY2020.

The pre-facelift C-HR is excluded from the official CarPlay retrofit. Hardware specifics (USB host controller, video decoder, microphones) of each generation were not documented in the sources found.

### Cited Findings
- Go-module software generations: Touch 2 with Go versions 3.x.x, 4.x.x and 6.x.x = "MM13-14-16". — [manuals.plus Toyota T2wG identification doc](https://manuals.plus/m/dbcc4aa12f48c082de538094557d54ae2edc6f1eca4b23e5e000fd166c5fc68c.pdf) (search summary)
- VERIFIED: 2016 Touch 2 with Go (MM16) adds a tile menu, split screen, auto-navigation, on-screen My Toyota account creation and 3 years of map care. The higher grade (Go Plus) adds voice recognition, TTS and 3D maps. The C-HR has had it from start of production, and the software was offered to existing owners. — [Toyota UK Magazine 2016](https://mag.toyota.co.uk/2016-toyota-touch-2-with-go-multimedia-system/); [Toyota Europe newsroom](https://newsroom.toyota.eu/toyota-touch-2-with-go/); [Toyota UK media site](https://media.toyota.co.uk/toyota-touch-2-with-go/)
- "Android Auto & Apple Carplay were only available as an upgrade on the later version of Touch 2 (known as MM17)." — [Toyota Owners Club: Technical: Touch2 and/with Go](https://www.toyotaownersclub.com/forums/topic/189515-technicaltouch2-and-touch2-andwith-go/) (search summary)
- VERIFIED: Toyota UK offered a dealer software upgrade adding Apple CarPlay to MY19 Corolla (all body styles/grades) and MY19/MY20 RAV4 (excluding Icon). The enhanced multimedia with CarPlay/AA has been standard from the 2020 model year. Toyota UK replies in the comments say the C-HR cannot have CarPlay retrofitted. — [Toyota UK Magazine: Apple CarPlay and Android Auto upgrade](https://mag.toyota.co.uk/toyota-apple-carplay-and-android-auto-upgrade/); [comments page 3](https://mag.toyota.co.uk/toyota-apple-carplay-and-android-auto-upgrade/comment-page-3/)
- 2019+ hardware: Panasonic DCU 17TDT2EU-DA01 (86140-42571) + Harman MEU 17TMT2EU-FA00→FA10 (86840-06041→86840-K0010). The conversion is "CY17 → CY17Plus (17MM → 19MM)" via three USB drives; the platform is i.MX6Q/eMMC/U-Boot 2009.08/Yocto-AGL. The README covers RAV4 AXAH52/54 and MXAA52/54 and Corolla ZRE210/ZWE211 only, with no mention of the C-HR. (COMMUNITY) — [GitHub README](https://raw.githubusercontent.com/edgardavey/toyota-touch2-dcu-carplay-fix/main/README.md)
- French C-HR owners: the latest firmware for this family is 6.24.0WH with 2024v2 maps; "AndroidAuto ne peut pas être officiellement activé sur ce système" (Android Auto cannot be officially enabled on this system). — [hybridlife.org tutorial](https://hybridlife.org/threads/tutoriel-de-mise-%C3%A0-jour-de-toyota-touch-go-2.3945/page-67) (search snippet)
- Facelift C-HR (2020+) units carry different part numbers (86140-F4090/F4220/F4221/F4530). — eBay listings cited in section 4.
- Previous generation (Touch & Go, 2010-2013): QNX Neutrino + TI DM3730 (inferred), extension box possibly with a Renesas V850. — [haxor.fi](https://haxor.fi/posts/how-the-firmware-updates-work-on-toyota-touch-go/)

### Inferences
- HYPOTHESIS: the jump from 13T (DA + Harman extension box) to 17T (DCU + MEU) was a real hardware change, not only software. New part numbers, new device-ID families and the fact that Toyota limited CarPlay retrofit to 17T-generation cars all point that way. The pre-facelift C-HR's 13TFDAEU DA therefore cannot receive the official CarPlay/AA software.
- HYPOTHESIS: the unit has a microphone for Bluetooth hands-free (all Touch 2 units have HFP) and accepts a camera input (the original reversing camera). The C-HR's USB port is likely routed to the Harman box (per mbirth). None of this was documented for the C-HR specifically.

### Gaps
- No source compares SoC, RAM, USB host, video decoder or microphone hardware across MM13, MM16 and 17MM/19MM, and no source gives the C-HR facelift (2020) unit's hardware.

## 7. How the owner can read more identifiers from the unit

### Takeaway
Three routes: (1) the on-screen System information already used; (2) the hidden service and diagnostic menu (with ignition ON, hold the CAR hard key, or SETUP on some units, and switch the headlights on/off three times quickly), which shows software versions and runs a system check; (3) remove the unit and read the chassis labels (Toyota 86140-xxxxx, supplier, serial) on both the Panasonic DA and the Harman box. Techstream/GTS readout of the multimedia ECUs was not documented in the sources found.

### Cited Findings
- Toyota Touch 2 repair manual, "Service Menu Access": with the ignition ON, "press and hold the CAR hard key, then switch the headlights on and off three times". From there the Diagnostic Menu can run a system check, and the software version can be read in the Service Menu. An alternative route exists for cars with daytime running lights, using the audio On/Off button and Setup > Display > "Screen off" (exact sequence not legible in the snippet). — [ManualsLib Toyota Touch 2 Repair Manual, p.131 "Service Menu Access"](https://www.manualslib.com/manual/1813654/Toyota-Touch-2.html?page=131)
- Owner variants: hold SETUP (older Toyota Touch) or MEDIA for another hidden menu; sidelights or tail lights instead of headlights; on some cars, the handbrake pulled up/down three times. Exiting may need the ignition switched off. — [pleasedonttouchthescreen.blogspot.com: Toyota Touch hidden menu (2012)](http://pleasedonttouchthescreen.blogspot.com/2012/10/toyota-touch-hidden-menu.html); [Toyota Owners Club: Touch2 Secret Hidden Menu](https://www.toyotaownersclub.com/forums/topic/219939-touch2-secret-hidden-menu/); [Toyota Owners Club: Auris touch2](https://www.toyotaownersclub.com/forums/topic/197063-auris-touch2/)
- Device ID and system configuration are at Setup > General > System information. — [Toyota UK FAQs](https://mag.toyota.co.uk/toyota-touch-go-touch-go-and-toyota-touch-pro-faqs/); [manuals.plus T2wG doc](https://manuals.plus/m/dbcc4aa12f48c082de538094557d54ae2edc6f1eca4b23e5e000fd166c5fc68c.pdf)
- A dealer/Toyota VIN-based parts lookup is the recommended way to confirm the exact part number. — [eBay seller and search guidance; see section 4 sources](https://www.ebay.co.uk/itm/404960270198)

### Inferences
- HYPOTHESIS: the service menu is the most promising non-invasive way to get more hardware identity. Look for pages listing each module's (DA, Extension Box, DAB tuner, Bluetooth) hardware/software part numbers, bootloader version and possibly a serial number. Photograph every page.
- HYPOTHESIS: on removal, expect at least two labels: the Panasonic DA label (Toyota 86140-F40xx, supplier code, serial, date code) and the Harman extension-box label (Toyota 8610x/8684x-number, Harman "PTxxx" style code like the PT296-47120 seen on US boxes, serial). Photograph both, and the board markings if the case is opened.
- HYPOTHESIS: Techstream/GTS may list "Navigation", "Audio" or "Multi-display" ECUs with calibration/part IDs over CAN/AVC-LAN, but this was not confirmed for the EU Touch 2.

### Gaps
- The exact C-HR service-menu contents (which identifiers appear) were not found, nor any Techstream/GTS readout example for 13TFDAEU units.
- The full Toyota document "DA & Ext. Box – How to Identify T2wG and Device ID – How to access the Service" (manuals.plus mirror) could not be fetched from this sandbox; it should be read directly, since it probably contains the official identification table and service-menu procedure for this exact generation.
