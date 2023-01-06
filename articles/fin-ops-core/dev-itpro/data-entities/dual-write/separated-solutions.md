---
title: Sérstakur pakki fyrir tvöfalda skráningu forrita
description: Pakki fyrir tvöfalda skráningu forrita er ekki lengur einn pakki heldur hefur verið skipt niður í smærri pakka. Þessi grein útskýrir lausnir og varpanir sem hver pakki inniheldur og tengsl þeirra við aðra pakka.
author: RamaKrishnamoorthy
ms.date: 04/25/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: separate-solution
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-11-29
ms.openlocfilehash: 28c321ee2815b2886c07bfb0996870e536458145
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111661"
---
# <a name="separated-dual-write-application-orchestration-package"></a>Sérstakur pakki fyrir tvöfalda skráningu forrita

[!include [banner](../../includes/banner.md)]



Áður var pakki fyrir tvöfalda skráningu forrita einn pakki sem innihélt eftirfarandi lausnir:

- Dynamics 365 Notes
- Dynamics 365 fjármála- og reksturs Common Anchor
- Dynamics 365 fjármála- og reksturs Dual Write Entity Maps
- Dynamics 365 Eignastýringarforrit
- Dynamics 365 eignastýring
- HCM sameiginlegt
- Dynamics 365 Supply Chain Extended
- Dynamics 365 Finance Extended
- Dynamics 365 fjármál- og rekstur Common
- Dynamics 365 Company
- Gengi gjaldmiðils
- Field Service Common

Þar sem hann var einn pakki er þessi pakki búinn til í „allt eða ekkert“ aðstæðum fyrir viðskiptavini. Hins vegar hefur Microsoft nú aðskilið það í smærri pakka. Því geta viðskiptavinir valið bara pakkana fyrir þær lausnir sem þeir þurfa á að halda. Ef þú ert til dæmis Microsoft Dynamics 365 Supply Chain Management viðskiptavinur og þarft ekki samþættingu við Dynamics 365 Human Resources, athugasemdir og eignastýringu er hægt að útiloka þær lausnir frá þeim lausnum sem eru settar upp. Þessi breyting er ekki skiptanlega vegna þess að undirliggjandi heiti, útgefandi og vörpunarútgáfur lausnar haldast eins. Fyrirliggjandi uppsetningar uppfærðar.

![Aðskildur pakki.](media/separated-package-1.png)

Þessi grein útskýrir lausnir og varpanir sem hver pakki inniheldur og tengsl þeirra við aðra pakka.

## <a name="dual-write-application-core"></a>Tvöföld skrif forritskjarna

Pakki fyrir tvöfalda skráningu forrita gerir notendum kleift að setja upp og skilgreina tvöfalda skráningu án viðskiptavinaforrits. Það inniheldur eftirfarandi fimm lausnir.

| Einkvæmt heiti                           | Heiti til birtingar                               |
|---------------------------------------|--------------------------------------------|
| Dynamics365Company                    | Dynamics 365 Company                       |
| Dynamics365FinanceAndOperationsCommon | Dynamics 365 fjármál- og rekstur Common |
| CurrencyExchangeRates                 | Gengi gjaldmiðils                    |
| msdyn_DualWriteAppCoreMaps            | Kjarnaeiningavarpanir forrita með tvöfaldri skráningu   |
| msdyn_DualWriteAppCoreAnchor          | Grunnakkeri forrita með tvöfölda skráningu        |

Eftirfarandi varpanir eru í þessum pakka.

| Forrit fyrir fjármál- og rekstur     | Forrit viðskiptavinatengsla                    |
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

**Tengslaupplýsingar**

Pakki fyrir tvöfalda skráningu forrita er ekki með nein tengsl við aðra pakka.

## <a name="dual-write-human-resources"></a>Human Resources, tvöföld skráning

Pakki fyrir tvöfalda skráningu mannauðs inniheldur lausnir og varpanir sem þarf til að samstilla mannauðsgögn. Það inniheldur eftirfarandi þrjár lausnir.

| Einkvæmt heiti                | Heiti til birtingar                             |
|----------------------------|------------------------------------------|
| HCMCommon                  | HCM sameiginlegt                               |
| msdyn_Dynamics365HCMMaps   | Dynamics 365 Human Resources einingakort |
| msdyn_Dynamics365HCMAnchor | Dynamics 365 Human Resources akkeri      |

Eftirfarandi varpanir eru í þessum pakka.

| Forrit fyrir fjármál- og rekstur | Forrit viðskiptavinatengsla         |
|-----------------------------|----------------------------------|
| Þjóðernisuppruni              | cdm_ethnicorigins                |
| Starfshlutverk launa   | cdm_jobfunctions                 |
| Stöður V2                | cdm_jobpositions                 |
| Störf                        | cdm_jobs                         |
| Starfsgerð launa       | cdm_jobtypes                     |
| Tungumálakóðar              | cdm_languages                    |
| Gerð stöðu               | cdm_positiontypes                |
| Starfskraftsúthlutanir stöðu | cdm_positionworkerassignmentmaps |
| Uppgjafahermennskustaða              | cdm_veteranstatuses              |
| Starfskraftur                      | cdm_workers                      |
| Atvinna eftir fyrirtækjum      | cdm_employments                  |

**Tengslaupplýsingar**

Pakki fyrir tvöfalda skráningu mannauðs fer eftir kjarnapakka fyrir tvöfalda skráningu forrita. Því ætti að setja upp kjarnapakka fyrir tvöfalda skráningu forrita áður en pakki fyrir tvöfalda skráningu forrita er settur upp.

## <a name="dual-write-supply-chain"></a>Aðfangakeðja með tvöfölda skráningu

Pakki fyrir tvöfalda skráningu Supply Chain inniheldur lausnir og varpanir sem þarf til að samstilla gögn Supply Chain Management. Það inniheldur eftirfarandi þrjár lausnir.

| Einkvæmt heiti                                | Heiti til birtingar                                              |
|--------------------------------------------|-----------------------------------------------------------|
| Dynamics365SupplyChainExtended             | Dynamics 365 Supply Chain Extended                        |
| msdyn_Dynamics365SupplyChainExtendedMaps   | Dynamics 365 Supply Chain Management extended entity maps |
| msdyn_Dynamics365SupplyChainExtendedAnchor | Dynamics 365 Supply Chain Management extended anchor      |

Eftirfarandi varpanir eru í þessum pakka.

| Forrit fyrir fjármál- og rekstur                 | Forrit viðskiptavinatengsla                      |
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
| Haus afurðarkvittunar                      | msdyn_purchaseorderreceipts                   |
| Lína innhreyfingarskjals                        | msdyn_purchaseorderreceiptproducts            |
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
| CDS-birgðir á                            | msdyn_inventoryonhandentries                  |
| Afurðartegundir                          | msdyn_productcategories                       |
| CDS-birgðir á                            | msdyn_inventoryonhandrequests                 |
| Afurðarnúmer sem eru auðkennd með strikamerki           | msdyn_productbarcodes                         |
| Vildarkort                                | msdyn_loyaltycards                            |
| Vildarpunktar                       | msdyn_loyaltyrewardpoints                     |
| Viðskiptavinaflokkar verðs                       | msdyn_pricecustomergroups                     |
| Svæði                                       | msdyn_operationalsites                        |
| CDS-sölutilboðslínur                   | quotedetails                                  |
| CDS sölupöntunarlínur                       | salesorderdetails                             |

**Tengslaupplýsingar**

Pakki fyrir tvöfalda skráningu Supply Chain fer eftir eftirfarandi þremur pökkum. Því ætti að setja upp þessa pakka áður en pakkinn fyrir tvöfalda skráningu Supply Chain er settur upp.

- Kjarnapakki forrits með tvöfalda skráningu
- Finance-pakki með tvöfaldri skráningu
- Human Resources-pakki, tvöföld skráning

## <a name="dual-write-finance"></a>Finance, tvöföld skráning

Pakki fyrir tvöfalda skráningu Finance inniheldur lausnir og varpanir sem þarf til að samstilla gögn Dynamics 365 Finance. Það inniheldur eftirfarandi fjórar lausnir.

| Einkvæmt heiti                            | Heiti til birtingar                               |
|----------------------------------------|-------------------------------------------|
| Dynamics365FinanceExtended             | Dynamics 365 Finance Extended             |
| msdyn_Dynamics365FinanceExtendedMaps   | Dynamics 365 Finance extended entity maps |
| FieldServiceCommon                     | Field Service Common                      |
| msdyn_Dynamics365FinanceExtendedAnchor | Dynamics 365 Finance extended anchor      |

Eftirfarandi varpanir eru í þessum pakka.

| Forrit fyrir fjármál- og rekstur             | Forrit viðskiptavinatengsla        |
|-----------------------------------------|---------------------------------|
| Staðgreiðsluskattsflokkar                  | msdyn_withholdingtaxgroups      |
| Tengiliðir fyrir skuldatryggingu V2 (viðskiptavinur)              | tengiliðir                        |
| Tengiliðir fyrir skuldatryggingu V2 (lánardrottinn)                | tengiliðir                        |
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
| Fjárhagur                                  | msdyn_ledgers                   |
| Viðskiptavinir V3                            | lyklar                        |

**Tengslaupplýsingar**

Pakki fyrir tvöfalda skráningu Finance fer eftir kjarnapakka fyrir tvöfalda skráningu forrita. Því ætti að setja upp kjarnapakka fyrir tvöfalda skráningu forrita áður en pakki fyrir tvöfalda skráningu Finance er settur upp.

## <a name="dual-write-notes"></a>Glósur, tvöföld skráning

Pakki fyrir tvöfalda skráningu Notes inniheldur lausnir og varpanir sem þarf til að samstilla athugasemda- eða skýringargögn. Það inniheldur eftirfarandi fjórar lausnir.

| Einkvæmt heiti                  | Heiti til birtingar                   |
|------------------------------|--------------------------------|
| Dynamics365Notes             | Dynamics 365 Notes             |
| Dynamics365NotesExtended     | Dynamics 365 notes extended    |
| msdyn_Dynamics365NotesMaps   | Dynamics 365 notes entity maps |
| msdyn_Dynamics365NotesAnchor | Dynamics 365 notes anchor      |

Eftirfarandi varpanir eru í þessum pakka.

| Fjármál- og rekstur                     | Customer Engagement |
|--------------------------------------------|---------------------|
| Viðhengt skjal fyrir sölupöntunarhaus    | skýringar         |
| Fylgiskjöl viðskiptamanns                       | skýringar         |
| Viðhengd skjöl lánardrottins                | skýringar         |
| Viðhengd skjöl fyrir haus innkaupapöntunar | skýringar         |

**Tengslaupplýsingar**

Notes-pakki með tvöfaldri skráningu er háður eftirfarandi tveimur pökkum. Því ætti að setja upp þessa pakka áður en pakki fyrir tvöfalda skráningu Notes er settur upp.

- Kjarnapakki forrits með tvöfalda skráningu
- Finance-pakki með tvöfaldri skráningu

## <a name="dual-write-asset-management"></a>Tvöföld skráning eignastjórnunar

Pakki fyrir tvöfalda skráningu eignastýringar inniheldur lausnir og varpanir sem þarf til að samstilla eignagögn úr Supply Chain Management eða Dynamics 365 Field Service. Það inniheldur eftirfarandi fjórar lausnir.

| Einkvæmt heiti                          | Heiti til birtingar                              |
|--------------------------------------|-------------------------------------------|
| Dynamics365AssetManagement           | Dynamics 365 eignastýring             |
| Dynamics365AssetManagementApp        | Dynamics365 Eignastýringarforrit          |
| msdyn_DualWriteAssetManagementMaps   | Dynamics 365 Eignastýringareiningakort |
| msdyn_DualWriteAssetManagementAnchor | Dynamics 365 Eignastýringarfesti      |

Eftirfarandi varpanir eru í þessum pakka.

| Forrit fyrir fjármál- og rekstur                           | Forrit viðskiptavinatengsla                |
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

**Tengslaupplýsingar**

Pakki fyrir tvöfalda skráningu eignastýringar fer eftir kjarnapakka fyrir tvöfalda skráningu forrita. Því ætti að setja upp kjarnapakka fyrir tvöfalda skráningu forrita áður en pakki fyrir tvöfalda skráningu eignastýringar er settur upp.

## <a name="packages-required-for-project-operations"></a>Nauðsynlegir pakkar fyrir Project Operations
Project Operations fer eftir eftirfarandi pökkum. Því ætti þú að setja upp þessa pakka áður en Project Operations er sett upp.

- Kjarnapakki forrits með tvöfalda skráningu
- Finance-pakki með tvöfaldri skráningu
- Aðfangakeðjupakki með tvöfalda skráningu
- Eignastýringarpakki, tvöföld skráning
- Human Resources-pakki, tvöföld skráning

## <a name="dual-write-party-and-global-address-book-solutions"></a>Lausn tvöfaldrar skráningar á aðila og altækri aðsetursbók

Pakki fyrir tvöfalda skráningu aðila og altækrar aðsetursbókar inniheldur eftirfarandi lausnir og varpanir sem þarf til að samstilla gögn aðila og altækrar aðsetursbókar. 

| Einkvæmt heiti                       | Heiti til birtingar                            |
|-----------------------------------|-----------------------------------------|
| Aðili                             | Aðili                                   |
| Dynamics365GABExtended            | Dynamics 365 GAB Extended               |
| Dynamics365GABDualWriteEntityMaps | Dynamics 365 GAB Dual Write Entity Maps |
| Dynamics365GABParty_Anchor        | Dynamics 365 GAB og aðili              |

Eftirfarandi varpanir eru í þessum pakka.

| Forrit fyrir fjármál- og rekstur | Forrit viðskiptavinatengsla | 
|-----------------------------|--------------------------|
| CDS-aðilar | msdyn_parties | 
| Staðsetningar CDS-póstfanga | msdyn_postaladdresscollections | 
| CDS-póstfangsferill V2 | msdyn_postaladdresses | 
| Staðsetningar póstfanga CDS-aðila | msdyn_partypostaladdresses | 
| Tengiliðir aðila V3 | msdyn_partyelectronicaddresses | 
| Viðskiptavinir V3 | lyklar | 
| Viðskiptavinir V3 | tengiliðir | 
| Lánardrottnar V2 | msdyn_vendors | 
| Titlar tengiliðar | msdyn_salescontactpersontitles | 
| Kveðjuorð | msdyn_complimentaryclosings | 
| Ávörp | msdyn_salutations | 
| Hlutverk ákvarðanatöku | msdyn_decisionmakingroles | 
| Starfshlutverk | msdyn_employmentjobfunctions | 
| Stig viðskiptavildar | msdyn_loyaltylevels | 
| Persónubundnar manngerðir | msdyn_personalcharactertypes | 
| Tengiliðir V2 | msdyn_contactforparties | 
| CDS-sölutilboðshaus | tilboð | 
| Hausar CDS-sölupöntunar | salesorders | 
| Sölureikningshausar V2 | reikningar | 
| CDS-vistfangshlutverk | msdyn_addressroles |

**Tengslaupplýsingar**

Aðila- og altækrar aðsetursbókarlausnir með tvöfalda skráningu eru háðar eftirfarandi þremur pökkum. Því ætti að setja upp þessa pakka áður en pakki fyrir tvöfalda skráningu á lausnum aðila og altækrar aðsetursbókar er settur upp.

- Kjarnapakki forrits með tvöfalda skráningu
- Finance-pakki með tvöfaldri skráningu
- Aðfangakeðjupakki með tvöfalda skráningu

