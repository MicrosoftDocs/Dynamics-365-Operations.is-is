---
title: Aðskilinn Dual-Write Application Orchestration pakki
description: Dual-write Application Orchestration pakkinn er ekki lengur einn pakki heldur hefur hann verið aðskilinn í smærri pakka. Þetta efnisatriði útskýrir lausnirnar og kortin sem hver pakki inniheldur og hversu háður hann er öðrum pakka.
author: RamaKrishnamoorthy
ms.date: 11/29/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.custom: separate-solution
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-11-29
ms.openlocfilehash: 3fe1b7707df72927fba78ee9659502cc62471799
ms.sourcegitcommit: 70ac76be31bab7ed5e93f92f4683e65031fbdf85
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 12/16/2021
ms.locfileid: "7924982"
---
# <a name="separated-dual-write-application-orchestration-package"></a>Aðskilinn Dual-Write Application Orchestration pakki

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Áður var Dual-write Application Orchestration pakkinn einn pakki sem innihélt eftirfarandi lausnir:

- Dynamics 365 Notes
- Dynamics 365 Finance and Operations Sameiginlegt akkeri
- Dynamics 365 Finance and Operations Tvöfalt skrifa einingakort
- Dynamics 365 eignastýringarforrit
- Dynamics 365 eignastýring
- HCM Common
- Dynamics 365 birgðakeðja framlengd
- Dynamics 365 Finance Extended
- Dynamics 365 Finance and Operations Sameiginlegt
- Dynamics 365 fyrirtæki
- Gengi gjaldmiðla
- Field Service Common

Vegna þess að þetta var einn pakki skapaði þessi pakki „allt eða ekkert“ aðstæður fyrir viðskiptavini. Hins vegar hefur Microsoft nú aðskilið það í smærri pakka. Þess vegna getur viðskiptavinur valið bara pakkana fyrir þær lausnir sem þeir þurfa. Til dæmis, ef þú ert Microsoft Dynamics 365 Supply Chain Management viðskiptavinur, og þurfa ekki samþættingu við Dynamics 365 Human Resources, athugasemdum og eignastýringu geturðu útilokað þessar lausnir frá þeim lausnum sem eru uppsettar. Vegna þess að undirliggjandi nöfn lausna, útgefanda og kortaútgáfu eru þau sömu, er þessi breyting órofa. Núverandi innsetningar verða uppfærðar.

![Aðskilinn pakki.](media/separated-package-1.png)

Þetta efnisatriði útskýrir lausnirnar og kortin sem hver pakki inniheldur og hversu háður hann er öðrum pakka.

## <a name="dual-write-application-core"></a>Tvöfaldur-skrifa umsóknarkjarna

Dual-write Application Core pakkinn gerir notendum kleift að setja upp og stilla dual-write án nokkurs viðskiptavinaforrits. Það inniheldur eftirfarandi fimm lausnir.

| Einstakt nafn                           | Heiti til birtingar                               |
|---------------------------------------|--------------------------------------------|
| Dynamics365Company                    | Dynamics 365 fyrirtæki                       |
| Dynamics365FinanceAndOperationsCommon | Dynamics 365 Finance and Operations Sameiginlegt |
| CurrencyExchangeRates                 | Gengi gjaldmiðla                    |
| msdyn_DualWriteAppCoreMaps            | Dual-write forrit kjarnaeiningakort   |
| msdyn_DualWriteAppCoreAnchor          | Dual-write forrit kjarna akkeri        |

Eftirfarandi kort eru fáanleg í þessum pakka.

| Finance and Operations-smáforrit     | Forrit viðskiptavinatengsla                    |
|---------------------------------|---------------------------------------------|
| Rekstrareining                  | msdyn_internalorganizations                 |
| Stigveldi fyrirtækis          | msdyn_internalorganizationhierarchies       |
| Lögaðilar                  | msdyn_internalorganizations                 |
| Lögaðilar                  | cdm_companies                               |
| Tilgangur fyrir stigveldi fyrirtækis | msdyn_internalorganizationhierarchypurposes |
| Gjaldmiðlapar gengis     | msdyn_currencyexchangeratepairs             |
| Viðskeyti nafna                    | msdyn_nameaffixes                           |
| Gerð gengis              | msdyn_exchangeratetypes                     |
| Gengi gjaldmiðla frá CDS              | msdyn_currencyexchangerates                 |
| Gerð fyrirtækisstigveldis     | msdyn_internalorganizationhierarchytypes    |
| Gjaldmiðlar                      | transactioncurrencies                       |
| Leiðarvísiseining blandaðs veruleika     | msmrw_guides                                |

**Upplýsingar um ósjálfstæði**

Dual-write Application Core pakkinn er ekki háður öðrum pakka.

## <a name="dual-write-human-resources"></a>Tvöfalt skrifa mannauð

Dual-write mannauðspakkinn inniheldur lausnir og kort sem þarf til að samstilla mannauðsgögn. Það inniheldur eftirfarandi þrjár lausnir.

| Einstakt nafn                | Heiti til birtingar                             |
|----------------------------|------------------------------------------|
| HCM Common                  | HCM Common                               |
| msdyn_Dynamics365HCMMaps   | Dynamics 365 Human Resources einingakort |
| msdyn_Dynamics365HCMAnchor | Dynamics 365 Human Resources akkeri      |

Eftirfarandi kort eru fáanleg í þessum pakka.

| Finance and Operations-smáforrit | Forrit viðskiptavinatengsla         |
|-----------------------------|----------------------------------|
| Þjóðernisuppruni              | cdm_ethnicorigins                |
| Starfshlutverk launa   | cdm_jobfunctions                 |
| Stöður V2                | cdm_jobpositions                 |
| Störf                        | cdm_jobs                         |
| Starfsgerð launa       | cdm_jobtypes                     |
| Tungumálakóðar              | cdm_tungumál                    |
| Gerð stöðu               | cdm_positiontypes                |
| Starfskraftsúthlutanir stöðu | cdm_positionworkerassignmentmaps |
| Uppgjafahermennskustaða              | cdm_veteranstatuses              |
| Starfsmaður                      | cdm_workers                      |
| Atvinna eftir fyrirtækjum      | cdm_employments                  |

**Upplýsingar um ósjálfstæði**

Dual-write mannauðspakkinn fer eftir Dual-write Application Core pakkanum. Þess vegna ættir þú að setja upp Dual-write Application Core pakkann áður en þú setur upp Dual-write Human Resources pakkann.

## <a name="dual-write-supply-chain"></a>Aðfangakeðja með tvöföldum skrifum

Dual-write Supply Chain pakkinn inniheldur lausnir og kort sem þarf til að samstilla Supply Chain Management gögn. Það inniheldur eftirfarandi þrjár lausnir.

| Einstakt nafn                                | Heiti til birtingar                                              |
|--------------------------------------------|-----------------------------------------------------------|
| Dynamics365SupplyChainExtended             | Dynamics 365 birgðakeðja framlengd                        |
| msdyn_Dynamics365SupplyChainExtended Maps   | Dynamics 365 Supply Chain Management útvíkkuð einingakort |
| msdyn_Dynamics365SupplyChainExtendedAnchor | Dynamics 365 Supply Chain Management framlengt akkeri      |

Eftirfarandi kort eru fáanleg í þessum pakka.

| Finance and Operations-smáforrit                 | Forrit viðskiptavinatengsla                      |
|---------------------------------------------|-----------------------------------------------|
| Einingar                                       | uoms                                          |
| Hausar CDS-sölupöntunar                     | salesorders                                   |
| CDS sölupöntunarlínur                       | salesorderdetails                             |
| CDS-sölutilboðshaus                  | tilboð                                        |
| CDS-sölutilboðslínur                   | quotedetails                                  |
| CDS-útgefnar einkvæmar afurðir              | afurðir                                      |
| Vöruhúsastaðir                             | msdyn_warehousezones                          |
| Vöruhúsastaðaflokkar                       | msdyn_warehousezonegroups                     |
| Vinnulínur vöruhúss                        | msdyn_warehouseworklines                      |
| Vinnuhausar vöruhúss                      | msdyn_warehouseworkheaders                    |
| Vöruhús                                  | msdyn_warehouses                              |
| Birgðagangur                             | msdyn_warehouseaisles                         |
| Umreikningur eininga                            | msdyn_unitofmeasureconversions                |
| Afhendingarskilmálar                           | msdyn_termsofdeliveries                       |
| Afhendingarmátar                           | msdyn_shipvias                                |
| Stílar afurðarsniðmáts                       | msdyn_sharedproductstyles                     |
| Sölureikningslínur V2                      | invoicedetails                                |
| Sölureikningshausar V2                    | reikningar                                      |
| Stærðir afurðarsniðmáts                        | msdyn_sharedproductsizes                      |
| Útgefnar afurðir V2                        | msdyn_sharedproductdetails                    |
| Skilgreiningar afurðarsniðmáts               | msdyn_sharedproductconfigurations             |
| Litir afurðarsniðmáts.                       | msdyn_sharedproductcolors                     |
| Upprunakóðar sölupantana                    | msdyn_salesorderorigins                       |
| Haus afurðarkvittunar                      | msdyn_purchaseorder receipts                   |
| Lína innhreyfingarskjals                        | msdyn_purchaseorder receiptproducts            |
| Hausar innkaupapöntunar V2                   | msdyn_purchaseorders                          |
| Eining CDS-innkaupapantanalínu með mjúkeyðingu | msdyn_purchaseorderproducts                   |
| Eining innkaupapantanalínu með skuldatryggingu              | msdyn_purchaseorderproducts                   |
| Rakningarvíddarflokkar                   | msdyn_producttrackingdimensiongroups          |
| Stílar                                      | msdyn_productstyles                           |
| Geymsluvíddarflokkar                    | msdyn_productstoragedimensiongroups           |
| Afurðartengdur umreikningur eininga           | msdyn_productspecificunitofmeasureconversions |
| Sjálfgefnar vörupöntunarstillingar V2           | msdyn_productspecificdefaultordersettings     |
| Stærðir                                       | msdyn_productsizes                            |
| Afurðavíddaflokkar                    | msdyn_productdimensiongroups                  |
| Sjálfgefnar pöntunarstillingar                      | msdyn_productdefaultordersettings             |
| Afbrigði                              | msdyn_productconfigurations                   |
| Allar afurðir                                | msdyn_globalproducts                          |
| Litir                                      | msdyn_productcolors                           |
| Hlutverk tegundastigveldis afurðar            | msdyn_productcategoryhierarchyroles           |
| Tegundastigveldi afurðar                | msdyn_productcategoryhierarchies              |
| Úthlutanir afurðategundar                | msdyn_productcategoryassignments              |
| Afurðartegundir                          | msdyn_productcategories                       |
| Staðsetningar vöruhúsa                         | msdyn_inventorylocations                      |
| CDS birgðahald á                            | msdyn_inventoryonhandentries                  |
| Afurðartegundir                          | msdyn_productcategories                       |
| CDS birgðahald á                            | msdyn_inventoryonhandrequests                 |
| Afurðarnúmer sem eru auðkennd með strikamerki           | msdyn_productbarcodes                         |
| Vildarkort                                | msdyn_loyaltycards                            |
| Vildarpunktar                       | msdyn_loyaltyrewardpoints                     |
| Viðskiptavinaflokkar verðs                       | msdyn_pricecustomergroups                     |
| Svæði                                       | msdyn_operationalsites                        |
| CDS-sölutilboðslínur                   | quotedetails                                  |
| CDS sölupöntunarlínur                       | salesorderdetails                             |

**Upplýsingar um ósjálfstæði**

Dual-write Supply Chain pakkinn fer eftir eftirfarandi þremur pakkningum. Þess vegna ættir þú að setja þessa pakka upp áður en þú setur upp Dual-write Supply Chain pakkann.

- Dual-write Application Core pakki
- Tvískrifað fjármálapakki
- Tvöfaldur-skrifa mannauðspakki

## <a name="dual-write-finance"></a>Tvískrifuð fjármál

Dual-write Finance pakkinn inniheldur lausnir og kort sem þarf til að samstilla Dynamics 365 Finance gögn. Það inniheldur eftirfarandi fjórar lausnir.

| Einstakt nafn                            | Heiti til birtingar                               |
|----------------------------------------|-------------------------------------------|
| Dynamics365FinanceExtended             | Dynamics 365 Finance Extended             |
| msdyn_Dynamics365FinanceExtended Maps   | Dynamics 365 Finance útvíkkuð einingakort |
| Field Service Common                     | Field Service Common                      |
| msdyn_Dynamics365FinanceExtendedAnchor | Dynamics 365 Finance framlengt akkeri      |

Eftirfarandi kort eru fáanleg í þessum pakka.

| Finance and Operations-smáforrit             | Forrit viðskiptavinatengsla        |
|-----------------------------------------|---------------------------------|
| Staðgreiðsluskattsflokkar                  | msdyn_withholdingtaxgroups      |
| CDS Contacts V2 (viðskiptavinur)              | tengiliðir                        |
| CDS tengiliðir V2 (seljandi)                | tengiliðir                        |
| Viðskiptavinir V3                            | tengiliðir                        |
| Staðgreiðsluskattskóðar                   | msdyn_withholdingtaxcodes       |
| Lánardrottnar V2                              | msdyn_vendors                   |
| Greiðsluháttur lánardrottins                   | msdyn_vendorpaymentmethods      |
| Lánardrottnaflokkar                           | msdyn_vendorgroups              |
| Bókhaldslykill                       | msdyn_chartofaccountses         |
| Fjárhagsbókunarflokkar virðisaukaskatts V2      | msdyn_taxpostinggroups          |
| VSK-flokkur vöru                    | msdyn_taxitemgroups             |
| VSK-flokkar                        | msdyn_taxgroups                 |
| Eining undanþágukóða virðisaukaskatts fyrir CDS        | msdyn_taxexemptcodes            |
| Viðskiptavinaflokkar                         | msdyn_customergroups            |
| Greiðslumáti viðskiptavinar                 | msdyn_customerpaymentmethods    |
| Fjárhagsvíddir                    | msdyn_dimensionattributes       |
| Skattayfirvöld                   | msdyn_taxauthorities            |
| Snið fjárhagsvíddar              | msdyn_financialdimensionformats |
| Tímabil fjárhagsdagatals                  | msdyn_fiscalcalendarperiods     |
| Samþættingareining fjárhagsdagatals      | msdyn_fiscalcalendars           |
| Samþættingareining fjárhagsdagatalsárs | msdyn_fiscalcalendaryears       |
| Greiðsluskilmálar                        | msdyn_paymentterms              |
| Greiðsluáætlun                        | msdyn_paymentschedules          |
| Greiðsluáætlunarlínur                  | msdyn_paymentschedulelines      |
| Greiðsludagar CDS                        | msdyn_paymentdays               |
| Greiðsludagalínur CDS V2                | msdyn_paymentdaylines           |
| Aðallykill                            | msdyn_mainaccounts              |
| Tegundir aðallykils                 | msdyn_mainaccountcategories     |
| Ledger                                  | msdyn_ledgers                   |
| Viðskiptavinir V3                            | lyklar                        |

**Upplýsingar um ósjálfstæði**

Dual-write Finance pakkinn fer eftir Dual-write Application Core pakkanum. Þess vegna ættir þú að setja upp Dual-write Application Core pakkann áður en þú setur upp Dual-write Finance pakkann.

## <a name="dual-write-notes"></a>Tvöfalt skrifa athugasemdir

Dual-write Notes pakkinn inniheldur lausnir og kort sem þarf til að samstilla athugasemdir eða athugasemdagögn. Það inniheldur eftirfarandi fjórar lausnir.

| Einstakt nafn                  | Heiti til birtingar                   |
|------------------------------|--------------------------------|
| Dynamics365 Notes             | Dynamics 365 Notes             |
| Dynamics365NotesExtended     | Dynamics 365 glósur framlengdar    |
| msdyn_Dynamics365NotesMaps   | Dynamics 365 glósur einingakort |
| msdyn_Dynamics365NotesAnchor | Dynamics 365 glósuakkeri      |

Eftirfarandi kort eru fáanleg í þessum pakka.

| Finance and Operations                     | Customer Engagement |
|--------------------------------------------|---------------------|
| Viðhengt skjal fyrir sölupöntunarhaus    | athugasemdir         |
| Fylgiskjöl viðskiptamanns                       | athugasemdir         |
| Viðhengd skjöl lánardrottins                | athugasemdir         |
| Viðhengd skjöl fyrir haus innkaupapöntunar | athugasemdir         |

**Upplýsingar um ósjálfstæði**

Dual-write Notes pakkinn fer eftir eftirfarandi tveimur pökkum. Þess vegna ættir þú að setja þessa pakka upp áður en þú setur upp Dual-write Notes pakkann.

- Dual-write Application Core pakki
- Tvískrifað fjármálapakki

## <a name="dual-write-asset-management"></a>Tvöföld skrif eignastýring

Dual-write Asset Management pakkinn inniheldur lausnir og kort sem þarf til að samstilla eignagögn frá Supply Chain Management eða Dynamics 365 Field Service. Það inniheldur eftirfarandi fjórar lausnir.

| Einstakt nafn                          | Heiti til birtingar                              |
|--------------------------------------|-------------------------------------------|
| Dynamics365 AssetManagement           | Dynamics 365 eignastýring             |
| Dynamics365 AssetManagementApp        | Dynamics365 eignastýringarforrit          |
| msdyn_DualWriteAssetManagement Maps   | Dynamics 365 Asset Management einingakort |
| msdyn_DualWriteAssetManagementAnchor | Dynamics 365 Asset Management akkeri      |

Eftirfarandi kort eru fáanleg í þessum pakka.

| Finance and Operations-smáforrit                           | Forrit viðskiptavinatengsla                |
|-------------------------------------------------------|-----------------------------------------|
| Ábyrgð eignastýringar                             | msdyn_warranties                        |
| Líkön eignastýringar                               | msdyn_models                            |
| Framleiðendur eignastýringar                        | msdyn_manufacturers                     |
| Virkar staðsetningagerðir eignastýringar            | msdyn_functionallocationtypes           |
| Virkar staðsetningar eignastýringar                 | msdyn_functionallocations               |
| Líftímastöður virkra staðsetninga eignastýringar | msdyn_functionallocationlifecyclestates |
| Líftímalíkön virkra staðsetninga eignastýringar | msdyn_functionallocationlifecyclemodels |
| Eignir eignastýringar                               | msdyn_customerassets                    |
| Eignagerðir eignastýringar                          | msdyn_customerassetcategories           |
| Líftímastöður eigna í eignastýringu               | msdyn_assetlifecyclestates              |
| Líftímalíkön eigna í eignastýringu               | msdyn_assetlifecyclemodels              |

**Upplýsingar um ósjálfstæði**

Dual-write Asset Management pakkinn fer eftir Dual-write Application Core pakkanum. Þess vegna ættir þú að setja upp Dual-write Application Core pakkann áður en þú setur upp Dual-write Asset Management pakkann.

## <a name="packages-required-for-project-operations"></a>Pakkar sem krafist er fyrir verkefnarekstur
Project Operations fer eftir eftirfarandi pakka. Þess vegna ættir þú að setja upp þessa pakka áður en þú setur upp Project Operations.

- Dual-write Application Core pakki
- Tvískrifað fjármálapakki
- Tvöfaldur-skrifa framboð Keðju pakki
- Tvöfaldur-skrifa eignastýringarpakki
- Tvöfaldur-skrifa mannauðspakki
