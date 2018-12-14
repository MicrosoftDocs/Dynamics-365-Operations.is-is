---
title: "Eiginleikar sem hafa verið fjarlægðir eða úreltir"
description: "Þetta efnisatriði lýsir eiginleikum sem hafa verið fjarlægðir eða sem verða fjarlægðir."
author: sericks007
manager: AnnBe
ms.date: 12/10/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 21821
ms.assetid: 31019808-4cbf-47d7-b1ba-d791db4281ae
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 48e2eea2cc986edc49d5192945c3d913c3bb9756
ms.openlocfilehash: 8a3405c434e402af68e59950f1e4d1a31cbf2813
ms.contentlocale: is-is
ms.lasthandoff: 12/04/2018

---

# <a name="removed-or-deprecated-features"></a>Fjarlægðir eða úreltir eiginleikar

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir eiginleikum sem hafa verið fjarlægðir eða úreltir fyrir Dynamics 365 for Finance and Operations.

- *Fjarlægður* eiginleiki er ekki lengur tiltækur í vörunni.
- *Úreltur* eiginleiki er ekki í virkri þróun og getur verið fjarlægður úr uppfærslum í framtíðinni.

Þessi listi er ætlað að hjálpa þér að íhuga þessar fjarlægingar og úreldingar fyrir eigin áætlanagerð. 

> [!Note]
> Frá og með útgáfu Microsoft Dynamics 365 for Finance and Operations, júlí 2017 með verkvangsuppfærslu 8, eru uppsetningargerðir merktar út frá sérhverjum eiginleika sem hefur verið fjarlægður eða úreltur. Allar fyrri útgáfur sem nefndar eru í þessu efnisatriði studdu aðeins dreifingar til skýjanna.

> [!Note]
> Ítarlegar upplýsingar um hluti í Finance and Operations má finna í [Tæknileg tilvísunarskjöl](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep). Hægt er að bera saman mismunandi útgáfur þessara skýrslna til að fá upplýsingar um hluti sem hefur verið breytt eða hafa verið fjarlægðir í hverri útgáfu Finance and Operations.

## <a name="dynamics-365-for-finance-and-operations-81-with-platform-update-20"></a>Dynamics 365 for Finance and Operations 8.1 með verkvangsuppfærslu 20

### <a name="batch-transfer-rules-for-subledger-journal-account-entries"></a>Runuflutningsreglur fyrir lyklafærslur undirbókar
Samstillta flutningsstillingin er felld úr gildi í færibreytum fjárhags.  Þessari stillingu er aðeins skipt út fyrir ósamstillta og áætlaða runu, sem þegar er til staðar sem valkostir fyrir flutning. 

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Við fjarlægjum samstillingarvalkostinn vegna þess að hann hefur áhrif á frammistöðu kerfisins. |
| **Skipt út fyrir aðra eiginleika?**   | Ósamstillt og áætluð runa eru valkostir til að nota í stað samstilltrar.   |
| **Afurðasvæði sem haft er áhrif á**         | Fjárhagur, Viðskiptaskuldir, Viðskiptakröfur, Innkaup, Kostnaður    |
| **Dreifingarvalkostur**              | Allir  |
| **Staða**                         | Úrelt: Tímarammi markmiðs um fjarlægingu á virkni er útgáfa 10.0.|

### <a name="electronic-reporting-for-russia"></a>Rafræn skýrslugerð fyrir Rússland
Eiginleiki til að stilla .txt- og .xml-skráarsnið yfirlýsinga. 

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Skipt út fyrir rafræna skýrslugerð. |
| **Skipt út fyrir aðra eiginleika?**   | Já. |
| **Afurðasvæði sem haft er áhrif á**         | Fjárhagur |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Fjarlægt frá og með Dynamics 365 for Finance and Operations 8.1 með verkvangsuppfærslu 20. |

### <a name="financial-reports-generator-for-russia"></a>Fjárhagsskýrslugerðarforrit fyrir Rússland
Verkfæri til að setja upp gagnasöfnun fyrir bókhald og skattaskýrslur og flytja út gögn í XLS- og DOC-skýrslusniðmát. Virkir hlutar: Flytja út gögn í XLS- og DOC-skýrslusniðmát, fyrirspurnir, föst skilyrði eru fjarlægð. 

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Fjarlægðum hlutum er skipt út fyrir rafræna skýrslugerð. |
| **Skipt út fyrir aðra eiginleika?**   | Já. Notandaviðmót fyrir uppsetningu á fjárhagsskýrslum ætti að nota til að setja upp gagnasöfnunarreglur með fjárhagslyklum eða skattskrám. Flytja út gögn í ýmisar skáargerðir, föst skilyrði og fyrirspurnir eins og gagnasöfnunarreglur ættu að vera stilltar í rafrænni skýrslugerð. |
| **Afurðasvæði sem haft er áhrif á**         | Fjárhagur. |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Fjarlægt frá og með Dynamics 365 for Finance and Operations 8.1 með verkvangsuppfærslu 20. |

### <a name="integration-with-external-providers-for-sending-electronic-reporting-through-communication-channels-for-russia"></a>Samþætting við ytri þjónustuveitendur við að senda rafræna skýrslugerð í gegnum samskiptarásir fyrir Rússland
Eiginleiki flytur út myndaðar rafrænar skrár yfirlýsinga í möppu til frekari sendingar til opinberra veitenda rafrænna skýrslugerða auk þess að flytja inn stöðu til baka.

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Skipt út fyrir stillanlega eiginleika rafrænna skilaboða. |
| **Skipt út fyrir aðra eiginleika?**   | Já.  |
| **Afurðasvæði sem haft er áhrif á**         | Fjárhagur, Skattur |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Fjarlægt frá og með Dynamics 365 for Finance and Operations 8.1 með verkvangsuppfærslu 20. |


### <a name="profit-tax-register-wizard"></a>Leiðsagnarforrit fyrir skattskrá hagnaðar
Eiginleiki til að búa til sniðmát fyrir nýjar skattskrár hagnaðar. Þessi eiginleiki býr til X++ hluti fyrir nýjar skrár, sem eru síðan búnar til sem sniðmát þar sem viðeigandi reiknireglum er bætt við.

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Eiginleiki er ekki samhæfur við stækkunarhæfnislíkan Dynamics 365 for Finance and Operations. |
| **Skipt út fyrir aðra eiginleika?**   | Númer |
| **Afurðasvæði sem haft er áhrif á**         | Skattur |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Fjarlægt frá og með Dynamics 365 for Finance and Operations 8.1 með verkvangsuppfærslu 20. |


## <a name="dynamics-365-for-finance-and-operations-80-with-platform-update-15"></a>Dynamics 365 for Finance and Operations 8.0 með verkvangsuppfærslu 15
Engir eiginleikar hafa verið fjarlægðir eða úreltir með þessari útgáfu. Verkvangsuppfærsla 15 er uppsöfnuð og inniheldur nýja eða breytta eiginleika frá verkvangsuppfærslu 13, verkvangsuppfærslu 14 og verkvangsuppfærslu 15.

## <a name="dynamics-365-for-finance-and-operations-enterprise-edition-73-with-platform-update-12"></a>Dynamics 365 for Finance and Operations, Enterprise Edition 7.3 með verkvangsuppfærslu 12

### <a name="personalized-product-recommendations"></a>Sérsniðiðnar vöruráðleggingar 
Frá og með 15. febrúar, 2018, munu smásalar ekki lengur geta birt sérsniðnar vöruráðleggingar á sölustaðartæki. Nánari upplýsingar eru í [Sérsniðnar vöruráðleggingar](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/personalized-product-recommendations).  

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Núverandi útgáfa af ráðleggingaþjónustu vörunnar verður fjarlægð og eiginleikinn endurhannaður með betra reikniriti og nýrri smásölumiðuðum möguleikum.  |
| **Skipt út fyrir aðra eiginleika?**   | Nei. Þó eru áform um að fá þennan eiginleika aftur inn sem vægi við nýja ráðleggingarþjónustu eftir haustið 2018.   |
| **Afurðasvæði sem haft er áhrif á**         | Sérsniðnar vöruráðleggingar á sölustað.                                                    |
| **Dreifingarvalkostur**              | Allir                                                                                      |
| **Staða**                         |Fjarlægt þann 15. febrúar, 2018. Þetta hefur áhrif á viðskiptavini sem keyra Dynamics 365 for Operations 1611 og eldri útgáfur.  |

### <a name="extension-of-the-list-of-electronic-reporting-er-functions"></a>Útvíkkun listans yfir aðgerðir Rafrænnar skýrslugerðar
Möguleikinn á að kynna sérsniðnar aðgerðir sem notaðar eru í ER-tjáningarbyggingu (til að fá frekari upplýsingar, sjá [Útvíkka lista yfir aðgerðir Rafrænnar skýrslugerðar](../../dev-itpro/analytics/general-electronic-reporting-formulas-list-extension.md)) er ekki studdur lengur. Vegna breytinga á ER API, varð API til að kalla innbyggðar aðgerðir frá ER tjáningarbyggingu innra API og ekki hægt að útvíkka lengur.

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Frumkvæðis innsiglun kóða  |
| **Skipt út fyrir aðra eiginleika?**   | Ekkert. Í hvert skipti sem þörf er á nýrri innbyggðu aðgerð verður að senda nýtt framlengingarbeiðni til ER rammahópsins.<br><br>Sem tímabundið verk um það leyti sem umbeðin aðgerð er í þróun hjá ER teyminu er hægt að forrita nauðsynlega rökfræði sem aðferð sérsniðins umsóknarflokks. Þessa aðferð er hægt að nálgast í ER-tjáningu sem eiginleika viðbætts ER-gagnasafns af **Umsókn/Flokkur** gerðinni sem vísar til þessa sérsniðna umsóknarflokks.  |
| **Afurðasvæði sem haft er áhrif á**         | Umgjörð rafrænnar skýrslugerðar                                                      |
| **Dreifingarvalkostur**              | Allir                                                                                      |
| **Staða**                         | Fjarlægt frá og með Dynamics 365 for Finance and Operations, Enterprise Edition 7.3.    |

### <a name="inventory-by-item-group-and-inventory-by-inventory-dimension-aging-reports"></a>Birgðir eftir vöruflokki og birgðir eftir aldursskýrslum birgðavídda

Þessar tvær skýrslur eru ekki lengur studdar í Finance and Operations. Í staðinn er hægt að nota skýrslu **Aldur birgða** til að bæta notandaupplifunina.

|   |  |
|--------------|-----------------------|
| **Ástæða afskrifta**       | Afrituð virkni  |
| **Skipt út fyrir aðra eiginleika?** | Já. Þessar skýrslur hafa verið skipt út fyrir skýrslu **Aldur birgða**.     |
| **Afurðasvæði sem haft er áhrif á**       | Birgðastjórnun, Kostnaðarstjórnun        |
| **Dreifingarvalkostur**        | Allir|
| **Staða**                       | Úrelt: Valmyndaratriði þessara tveggja skýrslna hafa verið fjarlægðar í útgáfu 7.3. Kóðann fyrir skýrslurnar er samt sem áður enn að finna í afurðinni. Áætlað er að fjarlægja kóðann í framtíðarútgáfu. |

### <a name="power-bi-content-packs-available-on-appsource"></a>Power BI efnispakkar eru tiltækar á AppSource
Efnispakkarnir **Kostnaðarstjórnun**, **Fjárhagsleg frammistaða** og **Afköst smásölurásar** sem eru í boði á [Microsoft AppSource](https://appsource.microsoft.com) síðuna, eru úreltir vegna uppfærslur á vöru í Microsoft Power BI. Kerfisstjórnunareyðublöð sem notuð eru til að dreifa þessum efnispökkum til PowerBI.com eru einnig úreltir í Finance and Operations.

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Vöruuppfærslur í Microsoft Power BI. |
| **Skipt út fyrir aðra eiginleika?**   | Efnispakkarnir **Kostnaðarstjórnun**, **Fjárhagsleg frammistaða** og **Afköst smásölurásar**, sem eru í boði á [AppSource](https://appsource.microsoft.com) síða, er skipt út fyrir greiningarforrit sem leyfa lausnasamþættingu á gagnagrunni stigi. Frekari upplýsingar um greiningarforrit, sjá [Innfellt Power BI í vinnusvæði](../../dev-itpro/analytics/embed-power-bi-workspaces.md).    |
| **Afurðasvæði sem haft er áhrif á**         | Kostnaðarstjórnun, Fjármál og Smásala                                                                                               |
| **Dreifingarvalkostur**              | Einungis ský (Samþætting við PowerBI.com er ekki studd við dreifingu á staðnum.)                                                                                                            |
| **Staða**                         | Úrelt: Tímarammi markmiðs um að fjarlægja virknina er Q2 2018.    |

### <a name="standard-ui-in-data-management-workspace"></a>Staðlað Notendaviðmót í vinnusvæði gagnastjórnunar

Staðlað notendaviðmót í gagnastjórnun er Legacy-UI, sem er sjálfgefna notendaviðmótið sem birtist notendum þegar þeir heimsækja vinnusvæði gagnastjórnunar.

|   |  |
|------------------|-------------------------|
| **Ástæða úreldingar/fjarlægingar** | Við erum að fjárfesta í veitingu nýrrar notendaupplifunar í nýja notendaviðmótinu.             |
| **Skipt út fyrir aðra eiginleika?**   | Nýja notendaviðmótið, sem kallast *Aukið yfirlit*, kemur í stað gamla notendaviðmótsins.            |
| **Afurðasvæði sem haft er áhrif á**         | Vinnusvæði gagnastjórnunar                                                     |
| **Dreifingarvalkostur**              | Allir                                                                           |
| **Staða**                         | Úrelt: Tímarammi markmiðs um að fjarlægja virknina er Q2 2018. |

### <a name="excise-sales-tax-service-tax-for-india"></a>Vörugjald, Virðisaukaskattur, Þjónustuskattur fyrir Indland

Þessar skattar hafa verið felldar inn í Vöru- og þjónustuskatt á Indlandi.

|                                             |                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------|
| **Ástæða úreldingar eða fjarlægingar**       | Þessar skattar hafa verið felldar inn í Vöru- og þjónustuskatt á Indlandi.                          |
| **Skipt út fyrir aðra eiginleika?**            | Indverskur vöru- og þjónustuskattur                                                              |
| **Afurðasvæði sem haft er áhrif á**                  | Skattur                                                                     |
| **Dreifingarvalkostur**                       | Allar einingar                                                   |
| **Staða**                                  | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika. |    

### <a name="file-validation-utility-fvu-for-india"></a>Villuleitarhjálparforrit (FVU) fyrir Indland

|                                             |                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------|
| **Ástæða úreldingar eða fjarlægingar**       | Of lítil notkun viðskiptavina.                                                  |
| **Skipt út fyrir aðra eiginleika?**            | Númer                                                                      |
| **Afurðasvæði sem haft er áhrif á**                  | Staðgreiðsluskattur á Indlandi                                                  |
| **Dreifingarvalkostur**                       | Allar einingar                                                                    |
| **Staða**                                  | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika.   |        

### <a name="tdstcs-certificate-for-india"></a>TDS/TCS vottorð fyrir Indland

Notendur geta sótt þetta frá ríkisstjórnargáttinni.

|                                             |                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------|
| **Ástæða úreldingar eða fjarlægingar**       | Of lítil notkun viðskiptavina.                                                  |
| **Skipt út fyrir aðra eiginleika?**            | Númer                                                                      |
| **Afurðasvæði sem haft er áhrif á**                  | Staðgreiðsluskattur á Indlandi                                                  |
| **Dreifingarvalkostur**                       | Allar einingar                                                                   |
| **Staða**                                  | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika.     |    

### <a name="exportimport-exim-incentive-scheme-for-india"></a>Útflutningur/Innflutningur (EXIM) hvatningarkerfi fyrir Indland


|                                             |                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------|
| **Ástæða úreldingar eða fjarlægingar**       | Of lítil notkun viðskiptavina.                                                  |
| **Skipt út fyrir aðra eiginleika?**            | Númer                                                                      |
| **Afurðasvæði sem haft er áhrif á**                  | Flytja inn og flytja út                                                       |
| **Dreifingarvalkostur**                       | Allar einingar                                                                    |
| **Staða**                                  | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika.  |    


## <a name="dynamics-365-for-retail-72"></a>Dynamics 365 for Retail 7.2

### <a name="personalized-product-recommendations"></a>Sérsniðiðnar vöruráðleggingar 
Frá og með 15. febrúar, 2018, munu smásalar ekki lengur geta birt sérsniðnar vöruráðleggingar á sölustaðartæki. Nánari upplýsingar eru í [Sérsniðnar vöruráðleggingar](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/personalized-product-recommendations).  

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Núverandi útgáfa af ráðleggingaþjónustu vörunnar verður fjarlægð og eiginleikinn endurhannaður með betra reikniriti og nýrri smásölumiðuðum möguleikum.  |
| **Skipt út fyrir aðra eiginleika?**   | Nei. Þó eru áform um að fá þennan eiginleika aftur inn sem vægi við nýja ráðleggingarþjónustu eftir haustið 2018.   |
| **Afurðasvæði sem haft er áhrif á**         | Sérsniðnar vöruráðleggingar á sölustað.                                                    |
| **Dreifingarvalkostur**              | Allir                                                                                      |
| **Staða**                         |Fjarlægt þann 15. febrúar, 2018. Þetta hefur áhrif á viðskiptavini sem keyra Dynamics 365 for Retail 7.2 og eldri útgáfur. |


## <a name="dynamics-365-for-finance-and-operations-enterprise-edition-july-2017-with-platform-update-8"></a>Dynamics 365 for Finance and Operations, Enterprise Edition júlí 2017 með Verkvangsuppfærslu 8

### <a name="currency-conversion-for-accounting-and-reporting-currencies"></a>Umreikningur gjaldmiðils fyrir bókhald og skýrslugjaldmiðla

Umreikningur gjaldmiðils fyrir bókhald og skýrslugjaldmiðla var kynntur þegar evran var kynnt.

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Takmarkaður notkun og viðbót við afrita lögaðila sem virkni í staðinn.      |
| **Skipt út fyrir aðra eiginleika?**   | Nei, en eiginleikunum „Afrita lögaðila“ og „Skilgreiningar“ var bætt við til að auðvelda flutning til fyrirtækis sem hefur breyttar grunnkröfur. |
| **Afurðasvæði sem haft er áhrif á**         | Fjármálastjórnun     |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika.   |


### <a name="warehouse-mobile-devices-portal"></a>Gátt fyrir fartæki vöruhúss

Vöruhús fjarskiptatæki portal (WMDP) var sjálfstæður þáttur sem var gert ráð fyrir verslunarsvæðis á sjálfnýtingu. Þessi hluti er ekki lengur studdur í Finance and Operations. Upprunalegt smáforrit sem bætir notandaupplifunina hefur komið í stað virkni WMDP.

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Afrituð virkni.       |
| **Skipt út fyrir aðra eiginleika?**   | Já. Þessari aðgerð hefur verið skipt út fyrir Finance and Operations - Warehousing. Sjá frekari upplýsingar um uppsetningu og forkröfur [sett Upp og skilgreina Microsoft Dynamics 365 til Finance and Operations - Warehousing](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/warehousing/install-configure-warehousing-app). |
| **Afurðasvæði sem haft er áhrif á**         | Vöruhúsastjórnun, flutningsstjórnun     |
| **Dreifingarvalkostur**              | Vöruhús fjarskiptatæki portal (WMDP) var sjálfstæður þáttur sem var gert ráð fyrir verslunarsvæðis á sjálfnýtingu.               |
| **Staða**                         | Úrelt: Tímarammi markmiðs um að fjarlægja virknina er Q4 2019.   |

### <a name="advanced-bank-reconciliation-matching-rule-for-manual-matching"></a>Jöfnunarregla ítarlegrar afstemmingar banka fyrir handvirka jöfnun

Jöfnunarregla var notuð til að velja og merkja bankaskjal við handvirka jöfnun skjala í afstemmingarvinnublaðinu

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Takmörkuð notkun.                                                                         |
| **Skipt út fyrir aðra eiginleika?**   | Nei. Síunarskilyrði dálka ætti að nota til að finna skjöl fyrir afstemmingu. |
| **Afurðasvæði sem haft er áhrif á**         | Reiðufjár- og bankastjórnun                                                               |
| **Dreifingarvalkostur**              | Allir                                                                                    |
| **Staða**                         | Fjarlægt frá og með júlí 2017.                                                               |

## <a name="dynamics-365-for-operations-1611-with-platform-update-3"></a>Dynamics 365 for Operations 1611 með verkvangsuppfærslu 3

### <a name="aeb-payment-formats-for-spain"></a>AEB-greiðslusnið fyrir Spán

Consejo Superior Bancario-greiðslusnið voru notuð til að senda greiðsluskrár til bankans fyrir viðskiptavina- og lánardrottnagreiðslur. Innihald þessara sniða var ákvarðað af Asociación Española de Banca. Það tekur á Cuaderno 19, 32, 58, 34.

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Þau greiðslusnið eru ekki lengur notaður.                                  |
| **Skipt út fyrir aðra eiginleika?**   | Já, ISO20022 millifærsla fjármuna og snið beingreiðslu fyrir Spán |
| **Afurðasvæði sem haft er áhrif á**         | Viðskiptakröfur, viðskiptaskuldir                                    |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika.           |

### <a name="bank-payments-transfer-for-lithuania"></a>Flutningar bankagreiðslur fyrir Litháen

Greiðslufærslur banka voru prentaðar og myndaðar með útflutningssniði greiðslufærslna (LT) fyrir Litháen. Litháíska markaðinn hóf að nota LITAS, sameinuðum rafræna bankakerfinu, 2005.

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Þau greiðslusnið eru ekki lengur notaður.                        |
| **Skipt út fyrir aðra eiginleika?**   | Já, ISO20022 greiðslusnið millifærsla fjármuna fyrir Litháen     |
| **Afurðasvæði sem haft er áhrif á**         | Viðskiptaskuldir                                               |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika. |

### <a name="bbs-direkte-remittering-payment-formats-for-norway"></a>BBS Direkte Remittering greiðslusnið fyrir Noreg

Greiðslusnið BBS Direkte Remittering innihalda útflutning innheimtu fyrir greiðsla viðskiptavinar (beingreiðsla) og innflutning svarskilaboða.

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Þau greiðslusnið eru ekki lengur notaður.  |
| **Skipt út fyrir aðra eiginleika?**   | Greiðslusnið viðskiptavinar AvtaleGiro fyrir noregs má nota til að mynda skilaboð beingreiðslu. Innflutningur svarskilaboða verða innleidd í síðari útgáfum. |
| **Afurðasvæði sem haft er áhrif á**         | Viðskiptakröfur, viðskiptaskuldir   |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika.                                                                                                 |

### <a name="chart-of-accounts-tool-for-spain"></a>Bókhaldslykill fyrir Spán

Þessa verkfæris er notaður þegar bókhaldslyklum á Spáni krefst meiriháttar breytingar. Notendur geta flytja nýja bókhaldslykla í Microsoft Excel eða textasnið og einnig er hægt að flytja inn fjárhagsskýrslur.

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Takmörkuð notkun                                                  |
| **Skipt út fyrir aðra eiginleika?**   | Númer                                                             |
| **Afurðasvæði sem haft er áhrif á**         | Fjárhagur                                                 |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika. |

### <a name="dom80-payment-format-for-belgium"></a>Dom80 greiðslusnið fyrir Belgíu

Eldra belgískt Greiðslusnið fyrir innheimtu (beingreiðsla).

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Þau greiðslusnið eru ekki lengur notaður.                          |
| **Skipt út fyrir aðra eiginleika?**   | Já, ISO 20022 beingreiðslusnið fyrir Belgíu.         |
| **Afurðasvæði sem haft er áhrif á**         | Viðskiptakröfur                                            |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika. |

### <a name="dtaezag-payment-formats-for-switzerland"></a>DTA/EZAG greiðslusnið fyrir Sviss

DTA/EZAG snið eru samþætta í ESR-kerfinu því þeau geta borið áfram tilvísunarnúmer. Þar sem tilvísunarnúmerið er ekki tilskilinn, má nota sniðin til að vinna allar lánardrottnagreiðslur. Þessara sniða eru notaður af fyrirtækjum sem hafa á bankareikning í staðsetningu annars staðar en “Postfinance”.

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Þau greiðslusnið eru ekki lengur notaður.                        |
| **Skipt út fyrir aðra eiginleika?**   | Já, ISO20022 greiðslusnið millifærsla fjármuna fyrir Sviss   |
| **Afurðasvæði sem haft er áhrif á**         | Viðskiptaskuldir                                               |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika. |

### <a name="edifact-dirdeb-payment-format-for-austria"></a>EDIFACT-DIRDEB greiðslusnið fyrir Austurríki

EDIFACT-DIRDEB Greiðslusnið innheimtu (beingreiðsla).

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Þau greiðslusnið eru ekki lengur notaður.                          |
| **Skipt út fyrir aðra eiginleika?**   | Já, ISO 20022 beingreiðslusnið fyrir Austurríki.         |
| **Afurðasvæði sem haft er áhrif á**         | Viðskiptakröfur                                            |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika. |

### <a name="edivat-for-belgium"></a>EDIVAT fyrir Belgíu

EDIVAT er úreltum Belgískar staðal fyrir rafræna skattskýrslu sent með öruggum pósti. Microsoft Dynamics AX 2012 heldur áfram skrifvarið lausn til að virkja aðgang að söguleg gögn.

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Þau eiginleiki eru ekki lengur notaður.                           |
| **Skipt út fyrir aðra eiginleika?**   | Númer                                                             |
| **Afurðasvæði sem haft er áhrif á**         | Fjárhagur                                                 |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika. |

### <a name="egiro-edifact-cremul-payment-import-format-for-norway"></a>innflutningssnið greiðslu eGiro EDIFACT fyrir Noreg

eGiro byggir á alþjóðlegum staðli Sameinuðu þjóðanna EDIFACT CREMUL, (Multiple Credit Advice Message), notaður fyrir sjálfvirka bókun á greiðslum viðskiptavina. Í Microsoft Dynamics AX er eGiro er innleitt sem innflutningssnið greiðslu viðskiptavinar.

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Þau greiðslusnið eru ekki lengur notaður.                                                     |
| **Skipt út fyrir aðra eiginleika?**   | Nei. Snið verður skipt út af ISO 20022 innflutningssniði fyrir yfirlit í síðari útgáfum. |
| **Afurðasvæði sem haft er áhrif á**         | Viðskiptakröfur                                                                       |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika.                            |

### <a name="external-inventory-for-poland"></a>Ytri birgðir fyrir Pólland

Sönnun um að vörur teknar frá lánardrottni fyrir sölur án kaupa. Vörur sem eru meðhöndlaðar í ytri birgðir hafa ekki áhrif á staðalaðar birgðir, og má selja þær og síðan kaupa sjálfkrafa. Ferlið stofnar raunverulegum birgðahreyfingar.

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Skipt út fyrir aðra eiginleika                                    |
| **Skipt út fyrir aðra eiginleika?**   | Já, kjarnaaðgerðir vörusendingar á Innleið                |
| **Afurðasvæði sem haft er áhrif á**         | Viðskiptaskuldir, birgðastjórnun                         |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika. |

### <a name="financial-reports-generator-for-eastern-europe"></a>Myndun fjárhagsskýrslna fyrir austur-Evrópa

Verkfæri er notað til að setja upp gagnasöfnun fyrir bókhald og skattaskýrslur og flytja út gögn í sniðmát skýrslu XLS og DOC.

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Takmörkuð notkun                                                                            |
| **Skipt út fyrir aðra eiginleika?**   | Nei. Forritið verður skipt út af skilgreiningar Rafræna skýrslugerð í framtíðinni. |
| **Afurðasvæði sem haft er áhrif á**         | Fjárhagur                                                                           |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika.                           |

### <a name="import-of-customer-payment-transactions-for-finland"></a>Flytja inn greiðslufærslur viðskiptavinar fyrir Finnland

Hægt er að velja innflutningssnið fyrir finnskar greiðslur sem flytur inn greiðslufærslur viðskiptavinar úr ytri skrá frá bankanum.

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Þau greiðslusnið eru ekki lengur notaður.                                                     |
| **Skipt út fyrir aðra eiginleika?**   | Nei. Snið verður skipt út af ISO 20022 innflutningssniði fyrir yfirlit í síðari útgáfum. |
| **Afurðasvæði sem haft er áhrif á**         | Viðskiptakröfur                                                                       |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika.                            |

### <a name="import-of-payment-transactions-into-a-general-ledger-journal-for-finland"></a>Innflutningur greiðslufærsla í færslubók fjárhags fyrir Finnland

Sniðið sem er tiltekið fyrir Finnland er notað til að flytja inn bókhaldsfærslur í fjárhag.

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Þau greiðslusnið eru ekki lengur notaður.                                                     |
| **Skipt út fyrir aðra eiginleika?**   | Nei. Snið verður skipt út af ISO 20022 innflutningssniði fyrir yfirlit í síðari útgáfum. |
| **Afurðasvæði sem haft er áhrif á**         | Viðskiptakröfur                                                                       |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika.                            |

### <a name="integration-with-isabel-synchronized-cis-for-belgium"></a>Samþætting við Isabel samstillt (CIS) fyrir Belgíu

Isabel er ramma fyrir rafræn bankaviðskipti í Evrópu og de-facto staðall í Belgíu.

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Hætt hefur verið samþætting við Isabel-biðlara.   |
| **Skipt út fyrir aðra eiginleika?**   | Nei. Greiðslusnið sem eru ekki lengur notaður er skipt fyrir ISO20022 greiðslusnið millifærsla fjármuna fyrir Belgíu. |
| **Afurðasvæði sem haft er áhrif á**         | Viðskiptaskuldir     |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika.    |

### <a name="modifications-in-the-chart-of-accounts-and-accounting-rules-for-spain"></a>Breytingar á bókhaldslykill og bókhaldsreglur fyrir Spán

Þessir eiginleikar eru notaðir fyrir Breytingar á bókhaldslykill og bókhaldsreglur fyrir Spán Það varpar lyklum til að aðstoða við að umbreyta gamla bókhaldslykilinn í nýja bókhaldslykil og ber saman fyrra fjárhagsárið með nýja fjárhagsárið, jafnvel þó þær voru bókaðar á mismunandi lykilnúmer.

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Takmörkuð notkun                                                  |
| **Skipt út fyrir aðra eiginleika?**   | Númer                                                             |
| **Afurðasvæði sem haft er áhrif á**         | Fjárhagur                                                 |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika. |

### <a name="pagamento-fornittori-vendor-payment-format"></a>Greiðslusnið lánardrottins Pagamento Fornittori

Eldri Ítölsk greiðslusnið fyrir millifærsla fjármuna.

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Þau greiðslusnið eru ekki lengur notaður.                          |
| **Skipt út fyrir aðra eiginleika?**   | Já, ISO20022 greiðslusnið millifærsla fjármuna fyrir Ítalía         |
| **Afurðasvæði sem haft er áhrif á**         | Viðskiptaskuldir                                               |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika. |

### <a name="payment-export-formats-for-estonia"></a>Greiðsluútflutningssnið fyrir Eistland

Telehansa og Teleservice-snið notuð til að flytja út greiðslu banka.

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Þau greiðslusnið eru ekki lengur notaður.                        |
| **Skipt út fyrir aðra eiginleika?**   | Já, ISO20022 greiðslusnið millifærsla fjármuna fyrir Eistland       |
| **Afurðasvæði sem haft er áhrif á**         | Viðskiptaskuldir                                               |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika. |

### <a name="payment-file-archive-for-norway"></a>Greiðsluskrársafn fyrir Noreg

Þegar greiðsluskrár eru myndaðar, geymir í skráasafn sjálfkrafa allar skrár sem eru stofnaðar, jafnvel skrár sem voru áður skrifuð eða lesa.

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Skipt út fyrir aðra eiginleika                                        |
| **Skipt út fyrir aðra eiginleika?**   | Já, Safnvistaðar vinnslur í Rafrænni skýrslugerð                            |
| **Afurðasvæði sem haft er áhrif á**         | Viðskiptakröfur, viðskiptaskuldir, fyrirtækisstjórnun |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika.     |

### <a name="payment-import-formats-for-estonia"></a>Greiðsluinnflutningssnið fyrir Eistland

Telehansa og TeleTeenus-snið notuð til að flytja inn greiðslu banka.

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Þau greiðslusnið eru ekki lengur notaður.                                                    |
| **Skipt út fyrir aðra eiginleika?**   | Nei. Sniðum verður skipt út af ISO 20022 innflutningssniði fyrir yfirlit í síðari útgáfum. |
| **Afurðasvæði sem haft er áhrif á**         | Viðskiptakröfur                                                                        |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika.                             |

### <a name="payroll-information-in-human-resources"></a>Launaupplýsingar í Mannauði

Mannauður, launaupplýsingar

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Þessi aðgerð hefur verið skipt fyrir síðurnar Laun og Mannauður.  |
| **Skipt út fyrir aðra eiginleika?**   | **Fríðindi**, **Tekjur**, og aðrar tengdar síður sem voru áður í BNA Laun hafa verið endurskilgreind, og eru nú hluti kjarnauppsetning Mannauðs til að styðja við ytri launavinnslu. Þessi virkni er opnuð með því að nota **Mannauður 1** \> **Laun** skilgreiningarlykillinn. |
| **Afurðasvæði sem haft er áhrif á**         | Mannauður, Laun   |
| **Staða**                         | Fjarlægt frá og með Dynamics 365 for Operations útgáfu 1611.    |

### <a name="performance-management-goal-workflow"></a>Verkflæði markmiðs frammistöðustjórnunar

Frammistöðustjórnun inniheldur markmiðastjórnun og samþættingu við yfirferðir frammistöðu.

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Frammistöðustjórnun var endurhönnuð og blaðsíðufjöldi var minnkað til að einfalda ferlið.                 |
| **Skipt út fyrir aðra eiginleika?**   | Nei. Markmið eru sýnileg stjórnendum gegnum gátt fyrir Sjálfsafgreiðsla stjórnanda og hægt er að breyta og skoða af stjórnanda. |
| **Afurðasvæði sem haft er áhrif á**         | Mannauðsstjórnun       |
| **Staða**                         | Fjarlægt frá og með Dynamics 365 for Operations útgáfu 1611.    |

### <a name="postgirot-and-postgirot-utland-payment-formats-for-sweden"></a>Postgirot og Postgirot Utland greiðslusnið fyrir Svíþjóð

Postgirot og Postgirot Utland greiðslusnið fyrir Svíþjóð

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Þau greiðslusnið eru ekki lengur notaður.                        |
| **Skipt út fyrir aðra eiginleika?**   | Já, ISO20022 greiðslusnið millifærsla fjármuna fyrir Svíþjóð        |
| **Afurðasvæði sem haft er áhrif á**         | Viðskiptaskuldir                                               |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika. |

### <a name="radio-frequency-identifier"></a>Rafmerki

Rafmerki (RFID) er gagnasöfnunartækni sem notar Rafræn tög til að geyma auðkennisgögn og no-line-of-sight requirement reader til að grípa auðkenni gögn.

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Lítil notkun viðskiptavina og takmörkuðum eiginleikum.   |
| **Skipt út fyrir aðra eiginleika?**   | Númer                                              |
| **Afurðasvæði sem haft er áhrif á**         | Birgðir                            |
| **Staða**                         | Fjarlægt frá og með Dynamics 365 for Operations 1611. |

### <a name="report-about-state-invoices-numbering-for-latvia"></a>Skýrsla um opinbera tölusetningu reikninga í Lettlandi.

Lettneskt löggjöf veitir tilteknar reglur um hvernig sölureikninga skulu númeraðir. Eiginleikinn leyfir þér að úthluta tilteknum númer á sölureikninga, byggt á notanda eða notendaflokk. Síðan er hægt að mynda skýrslu eða xml-skrá. Einnig er hægt að prenta skýrslu um reikningsnúmera sem eru notaðar.

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Í opinber tölusetning reikninga þarf ekki lengur að halda við. Skýrslu um notuð reikningsnúmer er ekki lengur þörf. |
| **Skipt út fyrir aðra eiginleika?**   | Númer       |
| **Afurðasvæði sem haft er áhrif á**         | Viðskiptakröfur    |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika.  |

### <a name="set-up-the-names-of-the-manager-and-general-accountant-of-a-company-for-lithuania"></a>Setja upp nöfn stjórnanda og aðalbókari fyrirtækis fyrir Litháen

Nöfn stjórnanda og aðalbókari fyrirtækis má tilgreina í upplýsingar um fyrirtækið og notaðar í útprentunum mismunandi staðbundna skýrslu.

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Skipt út fyrir aðra eiginleika                                     |
| **Skipt út fyrir aðra eiginleika?**   | Já, er hægt að nota uppsetningu embættismanna í sama tilgangi.   |
| **Afurðasvæði sem haft er áhrif á**         | Viðskiptaskuldir, viðskiptakröfur, reiðufjár- og bankastjórnunar |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika.  |

### <a name="shipping-carrier-interface"></a>Viðmót farmflytjanda

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Afrituð virkni   |
| **Skipt út fyrir aðra eiginleika?**   | Að hluta til skipt út fyrir Flutningsstjórnun |
| **Afurðasvæði sem haft er áhrif á**         | Sala og markaðssetning, Birgðastjórnun  |
| **Staða**                         | Fjarlægt frá og með Dynamics 365 for Operations útgáfu 1611.  |

### <a name="telepay-payment-formats-for-norway"></a>Telepay greiðslusnið fyrir Noreg

Greiðslusnið Telepay innihalda útflutning greiðsla lánardrottins (millifærsla fjármuna) og innheimtubréf (beingreiðsla) til viðskiptavina.

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Þau greiðslusnið eru ekki lengur notaður.                                                        |
| **Skipt út fyrir aðra eiginleika?**   | Já, ISO20022 greiðslusnið millifærsla fjármuna og greiðslusnið viðskiptavinar AvtaleGiro fyrir Svíþjóð |
| **Afurðasvæði sem haft er áhrif á**         | Viðskiptakröfur, viðskiptaskuldir                                                          |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika.                                 |

### <a name="vendor-payment-export-formats-for-finland"></a>Útflutningssnið lánardrottnagreiðslu fyrir Finnland

Tvö snið fyrir útflutning á greiðslum eru tiltækar fyrir Finnland. LM02 (FI) er notuð fyrir innanlandsgreiðslur og LUM2 (FI) er notað fyrir erlendar greiðslur.

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Þau greiðslusnið eru ekki lengur notaður.                        |
| **Skipt út fyrir aðra eiginleika?**   | Já, ISO20022 greiðslusnið millifærsla fjármuna fyrir Finnland       |
| **Afurðasvæði sem haft er áhrif á**         | Viðskiptaskuldir                                               |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika. |

### <a name="warehouse-management-ii"></a>Vöruhúsakerfi II

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Vöruhúsakerfi II-lausn (WMS II) sem var tiltækt í virkni tvíteknu kerfiseininga **Birgðastjórnunar** sem er í **vöruhúsakerfinu** sem var gefin út í Microsoft Dynamics AX 2012 R3.                                                                         |
| **Skipt út fyrir aðra eiginleika?**   | **Vöruhúsakerfinu** sem var gefið út í AX 2012 R3, Microsoft Dynamics AX 2012 R3 CU8 og Dynamics AX 2012 R3 CU9 kemur í stað virkni vöruhúsakerfis II. Nýja kerfið hefur fleiri ítarlegar aðgerðir og sveigjanlegri vöruhúsakerfisferli en vöruhúsakerfi II. |
| **Afurðasvæði sem haft er áhrif á**         | Birgðastjórnun, sölu og markaðssetningu, innkaup og uppruni   |
| **Staða**                         | Fjarlægt frá og með Dynamics 365 for Operations útgáfu 1611.    |

### <a name="worker-reminders-in-human-resources"></a>Áminningar starfsmanna í mannauði

Mannauður, launaupplýsingar

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Lítil notkun                                                           |
| **Skipt út fyrir aðra eiginleika?**   | Númer                                                                  |
| **Afurðasvæði sem haft er áhrif á**         | Mannauður                                                     |
| **Staða**                         | Fjarlægt frá og með Dynamics 365 for Operations útgáfu 1611 |

### <a name="workflow-for-creating-goals"></a>Verkflæði til að stofna markmið

Verkflæði til að stjórna stofnun starfsmannamarkmiða er eitt af nokkrum verkflæði sem voru tiltæk til að auðvelda skipulag fyrir ferlið við frammistöðustjórnun.

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Frammistöðustjórnun hefur verið algerlega endurhönnuð í Microsoft Dynamics 365 for Finance and Operations.     |
| **Skipt út fyrir aðra eiginleika?**   | Endurhannaður Eiginleiki frammistöðustjórnunar gefur meiri stjórn yfir markmið, mælingar sem notaðar eru til að rekja framvindu, og að hengja við frekari gögn. Markmið má geyma sem sniðmát og síðan endurnotuð. Þessi eiginleiki getur hjálpað við að setja upp viðbótar markmið fyrir starfsmennina fljótlegri hátt. |
| **Afurðasvæði sem haft er áhrif á**         | Mannauðsstjórnun                 |
| **Staða**                         | Fjarlægt frá og með Dynamics 365 for Operations útgáfu 1611. |

## <a name="dynamics-ax-70"></a>Dynamics AX 7.0 


### <a name="ability-to-cancel-changes-to-a-vendor-invoice"></a>Möguleika á að hætta við breytingar á reikningi lánardrottins

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Bætt frammistaða.        |
| **Skipt út fyrir aðra eiginleika?**   | Númer                             |
| **Afurðasvæði sem haft er áhrif á**         | Viðskiptaskuldir               |
| **Staða**                         | Fjarlægt frá og með Dynamics AX 7.0. |

### <a name="aif-axd-and-axbc-integrations"></a>AIF AxD og AxBC samþættingar

Í samþættingarramma Kerfa (AIF), er hægt að skiptast á gögnum við ytri kerfi gegnum viðskiptagrunninn með viðskiptagrunn sem er sem þjónustu. Dynamics AX felur í sér þjónustu sem byggir á skjölum og .NET Business Connector (AxBC). Skjal er stofnað með notkun XML. XML inniheldur hausupplýsingar sem bætt er við til að stofna *skilaboð* sem hægt er að flytja inn eða út úr Dynamics AX. Dæmi um skjöl fela í sér sölupantanir og innkaupapantanir. Hins vegar getur skjal staðið fyrir nánast hvaða einingu sem er, eins og viðskiptavin. Þjónustur sem byggja á skjölum nota **Axd \<Skjal\>** klasana.

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Ekki tókst að laga uppbyggingu AIF og AxDs að skýjaþjónustu. Upp komu afkastavandamálí tengslum við fjöldainnflutning.                                        |
| **Skipt út fyrir aðra eiginleika?**   | Þessum eiginleika er skipt út fyrir ramma innflutning/útflutning gagna, sem styður endurtekinn magninnflutning/útflutning gagna. Mælt er með því að raunverulegar töflur sé notað AxBC. |
| **Afurðasvæði sem haft er áhrif á**         | AxD AxBC og AIF   |
| **Staða**                         | Fjarlægt frá og með Dynamics AX 7.0.   |

### <a name="boms-without-bom-versions"></a>Uppskriftir án uppskriftaútgáfa

Þegar á skilgreiningarlykill **uppskriftaútgáfur** var gerður óvirkur voru uppskriftarútgáfur falin í öllum skjámyndum og kerfið þvingaði fram 1:1 vensl milli útgefnar afurðir og Uppskrifta. Skilgreiningarlykillinn **Uppskriftaútgáfur** má ekki vera óvirkur í þessari útgáfu af Dynamics AX.

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Notkun skilgreiningarlykils til að stjórna uppskriftaútgáfur lagast ekki að skýjaumhverfi. |
| **Skipt út fyrir aðra eiginleika?**   | Númer                                                                                      |
| **Afurðasvæði sem haft er áhrif á**         | Upplýsingar um afurðarstjórnun, Birgðastjórnun                                    |
| **Staða**                         | Fjarlægt frá og með Dynamics AX 7.0.                                                          |

### <a name="brazilian-bordero"></a>Brazilian Bordero

Tiltekin greiðsluhátt fyrir Brasilískt fyrirtæki

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Stuðning fyrir greiðsluaðferð Brasilískt Bordero Hefur verið lagðar af úr Brasilískt staðfærslu |
| **Skipt út fyrir aðra eiginleika?**   | Númer   |
| **Afurðasvæði sem haft er áhrif á**         | Viðskiptaskuldir   |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika. |

### <a name="brazilian-sintegra-statement"></a>Brasilískt Sintegra yfirlit

Alríkisskattframtal fyrir ICMS-skatt

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Þetta yfirlit á ekki lengur við sum Brasilískt fylki. |
| **Skipt út fyrir aðra eiginleika?**   | Nei. Notendur geta notað verkfærið Almennan Rafræna skýrslugerð til að skilgreina uppgjör ef nauðsynlegt við tilteknar aðstæður. |
| **Afurðasvæði sem haft er áhrif á**         | Skattabækur    |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika.   |

### <a name="brazilian-scan-contingency-mode-for-nf-e"></a>Brasilísk SCAN viðbúnaðarstilling fyrir NF-e

(SCAN) aðstæður viðbúnaðar er notað til að mynda, flytja út og inn stöðu á Nota Fiscal eletrônica (NF-e) þegar aðstæður Secretaria da Fazenda (SEFAZ) er ekki tiltækt.

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Viðbúnaðarháttur er á ekki lengur við í öllum brasilískum fylkjum |
| **Skipt út fyrir aðra eiginleika?**   | Númer                                                                          |
| **Afurðasvæði sem haft er áhrif á**         | Viðskiptakröfur                                                         |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika.              |

### <a name="business-analyzer"></a>Viðskiptagreining

Þessi fartækjaforrit leyfa notendum að yfirfara lykil viðskiptaviðmið.

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Aðgerðinni hefur verið skipt út fyrir aðra eiginleika.   |
| **Skipt út fyrir aðra eiginleika?**   | Fylgjast með fjárhagslegri frammistöðu efnispakki fyrir Microsoft Power BI mun innihalda lykil viðskiptaviðmiða sem voru áður tiltæk í Viðskiptagreiningu. |
| **Afurðasvæði sem haft er áhrif á**         | Fjárhagur      |
| **Staða**                         | Úrelt: Notkun Viðskiptagreiningar hefur verið gerð úrelt.    |

### <a name="business-statistics"></a>Viðskiptatalnagögn

Uppsetning fyrirspurnir um viðskiptatalnagögn sem geta auðveldað greiningu á afköstum í fyrirtækinu

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Eldri nálgun á viðskiptagreind (BI), Lítil notkun viðskiptavina og takmörkuðum eiginleikum. |
| **Skipt út fyrir aðra eiginleika?**   | Ný Lausnir fyrir BI fyrir þessa útgáfu af Dynamics AX.                                      |
| **Afurðasvæði sem haft er áhrif á**         | Innkaup og uppruni, viðskiptaskuldir, sala og markaðssetning, viðskiptakröfur         |
| **Staða**                         | Fjarlægt frá og með Dynamics AX 7.0.                                                               |

### <a name="change-document-date-function-in-invoice-approval-journal"></a>Breyta virkni dagsetningu skjals í færslubókarsamþykkt reiknings

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Lítil notkun                                                               |
| **Skipt út fyrir aðra eiginleika?**   | Já. Hægt er að breyta dagsetningu skjals á bókuðum lánardrottnafærslu. |
| **Afurðasvæði sem haft er áhrif á**         | Viðskiptaskuldir                                                        |
| **Staða**                         | Fjarlægt frá og með Dynamics AX 7.0.                                          |

### <a name="clieop03-payment-format-for-the-netherlands"></a>ClieOp03 greiðslusnið fyrir holland

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Snið gildir ekki lengur í Hollandi, þar sem því hefur verið skipt út fyrir SEPA-virkni. |
| **Skipt út fyrir aðra eiginleika?**   | SEPA greiðsluútflutningur  |
| **Afurðasvæði sem haft er áhrif á**         | Allar einingar     |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika.   |

### <a name="compliance-center"></a>Samræmismiðstöð

Samræmismiðstöðinni var Enterprise Portal-setur til að hafa umsjón með kröfum um fylgiskjöl fyrir vegna samræmis við framtaksverkefni í tengslum við Sarbanes Oxley lög.

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Of lítil notkun viðskiptavina. Microsoft SharePoint inniheldur sömu getu sem voru tiltæk í Samræmismiðstöð. |
| **Skipt út fyrir aðra eiginleika?**   | Númer   |
| **Afurðasvæði sem haft er áhrif á**         | Samræmi og innra eftirlit  |
| **Staða**                         | Fjarlægt frá og með Dynamics AX 7.0.    |

### <a name="connector-for-microsoft-dynamics"></a>Tengill fyrir Microsoft Dynamics

Þessa verkfæris var notuð til að samþætta lykilgögn úr Microsoft Dynamics CRM í Microsoft Dynamics ERP forritin.

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Aðgerðinni hefur verið skipt út fyrir aðra eiginleika. |
| **Skipt út fyrir aðra eiginleika?**   | Common data service                                      |
| **Afurðasvæði sem haft er áhrif á**         | Tengill fyrir Microsoft Dynamics                         |
| **Staða**                         | Fjarlægt frá og með Dynamics AX 7.0.                           |

### <a name="container-unit-and-multi-dimension-on-hand"></a>Geymslueining og fjölvídd á lager

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Afrituð virkni |
| **Skipt út fyrir aðra eiginleika?**   | Já. Síðan AX 2012 hefur þessi virkni verið skipt út fyrir eiginleikasetti sameinuðum runupöntunum. Þetta eiginleikasett er með samantekið yfirlit á lager. |
| **Afurðasvæði sem haft er áhrif á**         | Stjórnun á upplýsingum um afurðir, framleiðslustýring, Birgðastjórnun, Sölu og markaðssetning  |
| **Staða**                         | Fjarlægt frá og með Dynamics AX 7.0. |

### <a name="cue-group-metadata"></a>Bunkaflokkar Lýsigagna

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Bunkaflokkar voru notaðar til að birta eina eða fleiri bunka í svæði Upplýsingakassa . Takmörkuð geta til að meðtaka hlutina einnig komu upp vandamál hvað varðar afköst, vegna þess að breyting á skrá í yfirskjámyndar orsökuðu að ein fyrirspurnin varð til fyrir bunka í bunkaflokknum. |
| **Skipt út fyrir aðra eiginleika?**   | Númer      |
| **Afurðasvæði sem haft er áhrif á**         | Allar einingar    |
| **Staða**                         | Fjarlægt frá og með Dynamics AX 7.0.  |

### <a name="cue-metadata"></a>Bunka Lýsigögn

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Bunka lýsigögn hafa verið takmarkað til að telja eða taka saman upplýsingar.    |
| **Skipt út fyrir aðra eiginleika?**   | Reitar Lýsigögn var kynnt til sögunnar til að veita sveigjanlegri fyrir líkön. Til dæmis, er hægt að breyta gildandi talningar, flettingum og afkastavísar (KPI). Reitar Lýsigögn Talningar er bein útskipting bunka lýsigagna. |
| **Afurðasvæði sem haft er áhrif á**         | Allar einingar           |
| **Staða**                         | Fjarlægt frá og með Dynamics AX 7.0      |

### <a name="danish-check-format"></a>Danskt ávísunarsnið

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Stuðningur við danskt snið ávísana hefur verið lagður af og skýrslan hefur verið fjarlægð úr DK staðfærslu. |
| **Skipt út fyrir aðra eiginleika?**   | Númer    |
| **Afurðasvæði sem haft er áhrif á**         | Allar einingar    |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika.  |

### <a name="data-partitions"></a>Deildaskiptingar gagna

Gögn deildaskiptingar veita röklegt aðskilnaðinn gagna í gagnagrunn Microsoft Dynamics AX.

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Gögn deildaskiptingar voru kynnt í Microsoft Dynamics AX 2012 R2 til að virkja einangrun gagna. Í almennum aðstæðum, er Fyrirtæki með dótturfyrirtæki og gögn úr eitt dótturfyrirtæki ætti ekki að vera sýnileg fyrir aðra dótturfyrirtæki, jafnvel þótt bæði dótturfyrirtækjum er stjórnað af sömu tæknideild. Hins vegar var þörf á aukalegar forskriftir og sameiginlegur kostnaður í forritinu til að stofna nýja deildaskiptingar og færa inn í þær gög, og afrita deildaskiptingar gagna. Í skýið, þar sem við höfum aðgang að verkvangur sem þjónusta (PaaS) gagnagrunnsþjónustu (Microsoft Azure SQL Gagnagrunnur), er mikið áhrifaríkara að nota í gagnagrunninn sem einangrunargeymi en að framkvæma einangrunina í forritinu. Óháð því hvort deildaskipting gagna er krafist fyrir dótturfyrirtæki, fyrir marga leigjendur, eða einfaldlega fyrir kvörðun, trúum við því að aðstæður megi meðhöndla betur með mörgum tilvikum af Finance and Operations. |
| **Skipt út fyrir aðra eiginleika?**   | Viðskiptavinir sem nota deildaskiptingu gagna verða að nota mörg tilvik af Finance and Operations ef aðskilnaður gagnasafnsstiga er mikilvægt mál.    |
| **Afurðasvæði sem haft er áhrif á**         | Allar einingar  |
| **Staða**                         | Fjarlægt frá og með Dynamics AX 7.0.  |


### <a name="database-and-file-share-storage-for-attachments"></a>Gagnagrunnur og geymsla fyrir samnýttar skár fyrir viðhengi

Microsoft Dynamics AX 2012 leyfð geymsla viðhengja í gagnagrunninum og samnýttum skrám. Báðir valkostirnir eru ekki lengur studdir.

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Geymsla samnýttra skráa er ekki lengur studd því umhverfi í skýi geta ekki átt samskipti við staðbundnar samnýttar skrár. Gagnagrunnsgeymsla hefur verið gerð úrelt og í staðinn er komin Azure Blob geymsla. Azure Blob geymsla er sambærileg við geymslu í gagnagrunninum, þar sem aðeins er hægt að fá aðgang að skjölum í gegnum biðlaraskjámyndir Dynamics 365 for Finance and Operations. Þessu fylgir sá viðbótarkostur að bjóða upp á geymslu sem hefur ekki neikvæð áhrif á afköst gagnagrunnsins. Blob geymsla er sjálfgefið geymslukerfi fyrir Skjalastjórnum og virkar tafarlaust. |
| **Skipt út fyrir aðra eiginleika?**   | Gagnagrunnsgeymsla hefur verið gerð úrelt og í staðinn er komin Azure Blob geymsla.   |
| **Afurðasvæði sem haft er áhrif á**         | Allar einingar  |
| **Staða**                         | Fjarlægt frá og með Dynamics AX 7.0.   |

### <a name="delimitation"></a>Afmörkun

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Engin Notkun á þessari virkni fannst. |
| **Skipt út fyrir aðra eiginleika?**   | Númer                                     |
| **Afurðasvæði sem haft er áhrif á**         | Tími og mæting                    |
| **Staða**                         | Fjarlægt frá og með Dynamics AX 7.0.         |

### <a name="desktop-client"></a>Fjartengingarforrit

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Dynamics AX biðlarann Hefur verið endurhönnuð til að auka notkunargetu yfir marga vettvanga og tæki.                      |
| **Skipt út fyrir aðra eiginleika?**   | Nýr vefbiðlari er byggð á lýsigögnum skjáborðsmyndar og forritunarlíkans sem hefur verið breytt til að veita ríkulegan vefvettvang. |
| **Afurðasvæði sem haft er áhrif á**         | Allar einingar  |
| **Staða**                         | Fjarlægt frá og með Dynamics AX 7.0.   |

### <a name="direct-database-connection"></a>Bein gagnagrunnstenging

Í Dynamics AX 2012 R3, getur Retail Modern POS tengst beint í Channel DB á svipaðan hátt og við Enterprise POS. Það var auk staðlaðar samskiptaaðferðar Retail Modern POS sem átti samskipti í gegnum Retail-þjón.

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Bein gagnagrunns tengingarnar krefst minna öryggis samskiptareglu og var fyrst og fremst notuð til að ná hæsta stig afköst. Vegna frammistöðu og öryggi endurbætur sem hafa orðið í Dynamics 365 fyrir Finance and Operations, býr aðgerðin nú til fleiri vandamál en lausnir. |
| **Skipt út fyrir aðra eiginleika?**   | Nei. Aðeins stöðluðum Retail-þjónn samskipti eru studd núna.  |
| **Afurðasvæði sem haft er áhrif á**         | Channel DB/Retail Modern POS   |
| **Staða**                         | Fjarlægt frá og með Dynamics AX 7.0.  |

### <a name="dutch-swift-mt940"></a>Hollenska SWIFT MT940

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Almenn virkni er nú notaðar í stað staðfært virkni.                    |
| **Skipt út fyrir aðra eiginleika?**   | Já, þessum eiginleika hefur verið skipt út af ítarlega virkni fyrir bankaafstemmingu. |
| **Afurðasvæði sem haft er áhrif á**         | Allar einingar                                                                              |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika.                           |

### <a name="ebilanz-xbrl-for-germany"></a>eBilanz (XBRL fyrir Þýskaland)

Þessi virkni veitti úttak fyrir eXtensible Business Reporting Language (XBRL) sem er sérstaklega ætlað fyrir Þýska eBilanz-flokkunina.

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Of lítil notkun viðskiptavina.  |
| **Skipt út fyrir aðra eiginleika?**   | Þessum eiginleika hefur ekki verið skipt út fyrir annan eiginleika, en marga sérhæfða XBRL-pakka sem veita ríkulega xbrl-virkni eru tiltækar fyrir Þýsk markaði. |
| **Afurðasvæði sem haft er áhrif á**         | Management Reporter      |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika.  |

### <a name="enterprise-portal-client"></a>Enterprise Portal biðlari

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Eins biðlaravettvangur hefur verið stofnað.  |
| **Skipt út fyrir aðra eiginleika?**   | Nýr vefbiðlari er byggð á lýsigögnum skjáborðsmyndar og forritunarlíkans sem hefur verið breytt til að veita ríkulegan vefvettvang. |
| **Afurðasvæði sem haft er áhrif á**         | Allar einingar  |
| **Staða**                         | Fjarlægt frá og með Dynamics AX 7.0.   |

### <a name="environmental-sustainability"></a>Sjálfbær þróun

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Lítil notkun viðskiptavina og takmörkuðum eiginleikum.  |
| **Skipt út fyrir aðra eiginleika?**   | Númer              |
| **Afurðasvæði sem haft er áhrif á**         | Samræmi og innra eftirlit, viðskiptaskuldir  |
| **Staða**                         | Fjarlægt frá og með Dynamics AX 7.0. |

### <a name="form-activex-and-managed-host-controls"></a>Skjámynd ActiveX og stjórntæki hýsils með umsjón

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Skjámynd ActiveX og stjórntæki hýsils með umsjón byggjast á afskrifaða fjartengiforritinu. |
| **Skipt út fyrir aðra eiginleika?**   | Umfangsmikill Rammi fjárhagsáætlunarstýringar styður uppbyggingu nýja stýringar sem er byggt á HTML, CSS og JavaScript og er fyrsta flokks stýring í Microsoft Visual Studio Tooling umhverfinu. |
| **Afurðasvæði sem haft er áhrif á**         | Allar einingar     |
| **Staða**                         | Fjarlægt frá og með Dynamics AX 7.0.       |

### <a name="generate-prenotes-by-using-a-batch"></a>Mynda fyrirframkvittanir með runu

Myndun fyrirframkvittunar er ekki hægt að gera með því að nota runu en samt er hægt að gera af notanda.

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Engin skjámynd er til staðar til að staðfesta og birta fyrirframkvittunarskrá sem verður til þegar hún er mynduð með því að nota runuvinnslu. |
| **Skipt út fyrir aðra eiginleika?**   | Enn er hægt að mynda fyrirframkvittanir og notandi hefur stjórn á staðsetningunni þar sem skráin er vistuð.   |
| **Afurðasvæði sem haft er áhrif á**         | Viðskiptaskuldir, viðskiptakröfur, reiðufjár- og bankastjórnunar  |
| **Staða**                         | Fjarlægð frá og með AX 7.0.    |

### <a name="german-dtaus-payment-export-and-account-statement-import-totals-and-transactions"></a>Þýska DTAUS útflutningur og greiðslu og innflutningur lyklayfirlits (samtölur og færslur)

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Snið gildir ekki lengur í Þýskalandi, þar sem því hefur verið skipt út fyrir virkni sameiginlegs evrópsks greiðslusvæðis (SEPA).                    |
| **Skipt út fyrir aðra eiginleika?**   | Já, þessum eiginleika hefur verið skipt út af greiðsluútflutningur SEPA og ítarlega virkni fyrir bankaafstemming fyrir innflutning reikningsyfirlita. |
| **Afurðasvæði sem haft er áhrif á**         | Allar einingar  |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika. |

### <a name="german-dtazv-payment-format"></a>Þýska dtazv greiðslusnið

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Snið gildir ekki lengur í þýskalandi, þar sem því hefur verið skipt út fyrir SEPA-virkni. |
| **Skipt út fyrir aðra eiginleika?**   | SEPA greiðsluútflutningur    |
| **Afurðasvæði sem haft er áhrif á**         | Allar einingar   |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika.    |

### <a name="german-mt940-import"></a>Flytja inn Þýska MT940

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Almenn virkni er nú notaðar í stað staðfært virkni.                    |
| **Skipt út fyrir aðra eiginleika?**   | Já, þessum eiginleika hefur verið skipt út af ítarlega virkni fyrir bankaafstemmingu. |
| **Afurðasvæði sem haft er áhrif á**         | Allar einingar                                                                              |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika.                           |

### <a name="german-xml-eu-sales-list"></a>Þýskur XML ESB-sölulisti

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Xml-snið fyrir þýska skýrslugerð esb-Sölulista er ekki studd lengur. Hægt er að nota aðeins ELMA5 Snið textaskrár til að senda skýrslu esb-Sölulista til þýska skattstjórans. |
| **Skipt út fyrir aðra eiginleika?**   | Númer         |
| **Afurðasvæði sem haft er áhrif á**         | Skattur        |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika.   |

### <a name="gl-ssrs-reports"></a>GL SSRS-skýrslur

Skýrslur sem innihalda eftirfarandi valmyndaratriði hafa verið fjarlægð: **Samantekt á prófjöfnuði**, **Ítarlegur prófjöfnuður**, **Bókhaldslykil**, **Endurskoðunarslóð**, **Stöður**, og **stöðulisti**.

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Skýrslur fyrir Microsoft SQL Server Reporting Services (SSRS) hefur verið skipt út fyrir eiginleika Management Reporter og sjálfgefnar skýrslur. |
| **Skipt út fyrir aðra eiginleika?**   | Management Reporter (merktur **fjárhagsskýrslugerð** í þessari útgáfu af Dynamics AX)    |
| **Afurðasvæði sem haft er áhrif á**         | Fjárhagur   |
| **Staða**                         | Fjarlægt frá og með Dynamics AX 7.0.   |

### <a name="infopart-and-formpart-metadata"></a>InfoPart og FormPart lýsigögn

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | InfoPart og FormPart lýsigögn virkja stofnun upplýsingareita fyrir tvo mismunandi biðlara. |
| **Skipt út fyrir aðra eiginleika?**   | InfoPart lýsigögn sem var einfaldaður skilgreining skjámyndar, er breytt í Skjámynd með uppfærsluverkfærum. FormPart lýsigögn sem vísaí Skjámynd, er skipt út fyrir beinni tilvísun sem er stofnað af uppfærsluverkfærum. |
| **Afurðasvæði sem haft er áhrif á**         | Allar einingar    |
| **Staða**                         | Fjarlægt frá og með Dynamics AX 7.0.        |

### <a name="main-account-list-page"></a>Listasíða Aðallykils

Listi yfir lykla fyrir lögaðilann og tengdar stöðuupplýsingar

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Upplýsingar um Stöðu er tiltæk á í **prófjöfnuð** listasíðu eftir lykils og víddar.  |
| **Skipt út fyrir aðra eiginleika?**   | **Aðallyklar** inniheldur sömu lista með lyklum sem listasíðu **aðallykils** innihélt . Sýn hnitanets í **aðallykla** sýnir einnig enn minni, yfirlit í hnitaneti . |
| **Afurðasvæði sem haft er áhrif á**         | Fjárhagur      |
| **Staða**                         | Fjarlægt frá og með Dynamics AX 7.0.    |

### <a name="malaysia-and-singapore-bank-cash-flow-report"></a>Malasíu og Singapúr sjóðstreymiskýrsla banka

Þessi eiginleiki gefur notanda kost á að Prenta sjóðstreymisskýrslu sem sýnir færslur og upplýsingar sjóðinnstreymis og útstreymis fyrir tilteknar dagsetningar á völdum bankareikningum.

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Hægt er að fá sömu upplýsingar úr fyrirspurn Um bankafærslu. |
| **Skipt út fyrir aðra eiginleika?**   | Fyrirspurn Um bankafærslu.                                            |
| **Afurðasvæði sem haft er áhrif á**         | Reiðufjár- og bankastjórnun                                                |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika.          |

### <a name="mexican-cfd-electronic-invoice"></a>Mexíkóskur CFD rafrænn reikningur

Þessi eiginleiki virkjaði myndun Mexíkósk rafræna reikninga með því að nota aðferðina Comprobante Fiscal Digital (CFD), þar sem fyrirtækið skrifar undir reikninginn með því að biðja um viðkomandi heimild frá yfirvalda. Þessi eiginleiki veitir einnig mánaðarleg skýrsla sem inniheldur alla rafræna reikninga sem voru gefnir út á tímabilinu.

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Aðferð er ekki lengur gild. Myndun rafrænna reikninga með því að nota aðferðina CFD var afskrifuð af skattyfirvöldum og skipt út fyrir Comprobante Fiscal Digital a través de Internet (CFDI) -aðferð, þar sem undirritun er framvísað til þriðja aðila þjónustuaðila (PAC). Mánaðarleg skýrsla hefur verið fjarlægt og fyrirspurnarvalkostur gerir notendum kleift að spyrjast fyrir um sögulegar færslur. |
| **Skipt út fyrir aðra eiginleika?**   | Númer    |
| **Afurðasvæði sem haft er áhrif á**         | Viðskiptakröfur, verk   |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika. |

### <a name="mexico-realized-and-unrealized-vat"></a>Mexíkó innleyst og óinnleystur VSK

Microsoft Dynamics AX 2012 vann úr óinnleysta virðisaukaskattinum (VSK) með því að nota aðgerðir sem eru sérstaklega notaðar fyrir Mexíkó fyrir óinnleystan skatt.

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Afrituð virkni  |
| **Skipt út fyrir aðra eiginleika?**   | Já, þessari virkni hefur verið skipt út fyrir virkni staðlaðs skilyrts söluskatts sem Core veitir. |
| **Afurðasvæði sem haft er áhrif á**         | Skattur   |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika. |

### <a name="microsoft-outlook-integration"></a>Microsoft Outlook-samþætting


|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Aðgerðinni hefur verið skipt út fyrir samþættingu Microsoft Exchange Server. |
| **Skipt út fyrir aðra eiginleika?**   | Já                                                                            |
| **Afurðasvæði sem haft er áhrif á**         | Sala og markaðsstarf                                                            |
| **Staða**                         | Fjarlægt frá og með Dynamics AX 7.0.                                                 |

### <a name="private-blocking-of-inventory-and-warehouse-management-journals"></a>Einka lokun á færslubókum birgða- og vöruhúsastjórnunar

Færslubók birgða og vöruhúss hafa ekki lengur möguleikann á að merkja færslubók sem einka fyrir valinn notanda. Aðeins ferlið við lokun færslubóka sem einka fyrir notendaflokka og lokunar við breytingar er studd.

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Engin Notkun á þessari virkni fannst. |
| **Skipt út fyrir aðra eiginleika?**   | Númer                                     |
| **Afurðasvæði sem haft er áhrif á**         | Birgðir                   |
| **Staða**                         | Fjarlægt frá og með Dynamics AX 7.0.         |

### <a name="product-builder"></a>Vörusamsetning

Vörusamsetning (Product builder) var notaður til að setja saman á lifandi hátt vörur úr sölupöntun, innkaupapöntun, framleiðslupöntun, sölutilboð, verktilboð eða vöruþörf. Samkvæmt vörulíkani sem var með líkanabreytum gat notandinn velja gildi til að uppfylla kröfur viðskiptavinar og sækja einkvæmt afurðarafbrigði sem höfðu Uppskrift og leið.

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Product builder birti X ++ kóða til að endanotenda og er ekki studdur í þessari útgáfu af Dynamics AX. Það hefur verið fjarlægð til að koma í veg fyrir tvíteknar viðhaldsvinnu á kóðagrunnum sem skarast.  |
| **Skipt út fyrir aðra eiginleika?**   | Já. Skorðuskilgreiningin var kynnt í Dynamics AX 2012 þar sem úrelding Vörusamsetningar í framtíðarútgáfum var þegar tilkynnt. Skorðuskilgreiningartæknin valin á vörustjórunum til að virkja grunnstillingarnar. Frekari upplýsingar, sjá [Byggja líkan vöruskilgreiningar](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/pim/build-product-configuration-model). |
| **Afurðasvæði sem haft er áhrif á**         | Stjórnun á upplýsingum um afurðir, Sölu og markaðssetningu  |
| **Staða**                         | Fjarlægt frá og með Dynamics AX 7.0.      |

### <a name="production-floor-app"></a>Forrit framleiðslugólfs
Þetta er forritið fyrir spjaldtölvur sem keyra Windows 8.1 RT og Windows 8.1 Pro.

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Með breytingunni á biðlara á netinu er hægt að skila svipaðri virkni í gegnum biðlara Dynamics AX 7.0 á staðnum. Verkspjaldstækið býður upp á notandaviðmót fyrir framleiðslugólf sem er fínstillt inn á snertieiginleika og skjámynd spjaldtölvu. |
| **Skipt út fyrir aðra eiginleika?**   | Já. Verkspjaldstækið, sem er staðbundinn hluti Dynamics AX 7.0.                                                                           |
| **Afurðasvæði sem haft er áhrif á**         | Framleiðslustýring                                                |
| **Staða**                         | Úrelt: Fjarlægingardagsetning frá verslun Microsoft hefur enn ekki verið stillt fyrir þennan eiginleika.                                                |


### <a name="rename-product-dimension"></a>Endurnefna afurðarvídd

Þessi eiginleiki leyfði þér að breyta heiti á einn af þremur staðlaða afurðarvíddum (stærð, lit eða stíl) í nafn sem hentaði betur þínu fyrirtæki. Endurnefning innifalið allar merki þar sem nöfn afurðarvídda voru notuð.

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Þessi útgáfu af Dynamics AX styður ekki merkingabreytingar á keyrslutíma. |
| **Skipt út fyrir aðra eiginleika?**   | Númer                                                                            |
| **Afurðasvæði sem haft er áhrif á**         | Afurðarupplýsingastjórnun                                                |
| **Staða**                         | Fjarlægt frá og með Dynamics AX 7.0.                                                |

### <a name="retail-server-connectivity-using-http"></a>Tengigeta Retail-þjóns athuguð

Í Dynamics AX 2012 R3, gæti Retail-þjónn virkað með HTTP samskiptaaðferðar (ekki-öryggisvörðum). Þetta var til viðbótar við stöðluð samskipti með HTTPS.

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Vegna nýrra öryggisþarfa, aðeins öryggisvörðum samskipti með TLS 1,2 (eða ofan, sé það til staðar) er nú studd. Sjálfsafgreiðslu uppsetningarforritið mun sjálfkrafa skilgreina tölvunni þessu samskiptaaðferðar. |
| **Skipt út fyrir aðra eiginleika?**   | Nei. Aðeins stöðluðum HTTPS samskipti eru studd núna. |
| **Afurðasvæði sem haft er áhrif á**         | Retail-þjónn  |
| **Staða**                         | Fjarlægt frá og með Dynamics AX 7.0. |

### <a name="role-center-pages"></a>Hlutverkamiðstöðvarsíður

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Síður hlutverkamiðstöðvar voru byggðar á afskrifuðum Enterprise Portal verkvangi, sem hefur verið skipt út fyrir nýtt vefbiðlaravettvang í þessari útgáfu af Dynamics AX. |
| **Skipt út fyrir aðra eiginleika?**   | Nýtt skjámyndarmynstur Vinnusvæðis veitir notendum hönnun sem er vinnslumiðuð og veitir auðveldan aðgang að almennum verkum innan þessu ferli.                       |
| **Afurðasvæði sem haft er áhrif á**         | Allar einingar    |
| **Staða**                         | Fjarlægt frá og með Dynamics AX 7.0   |

### <a name="sales-tax-jurisdictions"></a>Skattaumdæmi

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Lítil notkun viðskiptavina og takmörkuðum eiginleikum. |
| **Skipt út fyrir aðra eiginleika?**   | Númer                                           |
| **Afurðasvæði sem haft er áhrif á**         | Bandarískur virðisaukaskattur                                 |
| **Staða**                         | Fjarlægt frá og með Dynamics AX 7.0.               |

### <a name="sites-services"></a>Svæðaþjónusta

Sites Services gerir þér kleift að búa til vefsíður sem framlengja viðskiptaferlum þínum til internetsins án stuðnings við upplýsingatækni.

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Grunngerð Microsoft Azure sem notað er í Dynamics AX hefur nýja getu sem hægt er að nota í staðinn (til dæmis Azure setur). |
| **Skipt út fyrir aðra eiginleika?**   | Númer   |
| **Afurðasvæði sem haft er áhrif á**         | Ráðningaferli tengd mannauði, Málastjórnun, Tilboðsbeiðnir, Skráning lánardrottins, Sameiginleg vinnusvæði fyrir tækifæri og herferðir  |
| **Staða**                         | Fjarlægt frá og með Dynamics AX 7.0.    |

### <a name="ssas-demand-forecasting-strategy"></a>SSAS stefna eftirspurnarspár

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Hönnun á eiginleikanum getur ekki verið studd í nýrri skýjahögun. |
| **Skipt út fyrir aðra eiginleika?**   | Azure Machine Learning stefna eftirspurnarspár                           |
| **Afurðasvæði sem haft er áhrif á**         | Aðaláætlanagerð                                                              |
| **Staða**                         | Fjarlægt frá og með Dynamics AX 7.0.                                               |

### <a name="vendor-invoice-pool-excluding-posting-details"></a>Reikningahópur lánardrottins án bókunarupplýsinga

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Lítil notkun. Aðgerðinni hefur verið skipt út af reikningabók sem hefur virknina verkflæði. |
| **Skipt út fyrir aðra eiginleika?**   | Verkflæðigeta reikningsbókar.     |
| **Afurðasvæði sem haft er áhrif á**         | Viðskiptaskuldir |
| **Staða**                         | Fjarlægt frá og með Dynamics AX 7.0.    |


### <a name="virtual-company-accounts"></a>Sýndarreikningsskil

Sýndarfyrirtækjaeiginleiki er ekki lengur studd í Dynamics AX. Eiginleikinn sýndarfyrirtæki gerði notendum mögulegt að setja upp töflur sem mátti deila með hóp fyrirtækja. Fyrir lýsingu á aðgerðinni sjá [reikningsskil og sýndarreikningsskil](https://msdn.microsoft.com/en-us/library/aa834382(v=ax.10).aspx). Eiginleikinn vinnur með því að flokka töflur í söfn sem tilheyra sýndarfyrirtæki, sem eru hópar af fyrirliggjandi "raunverulegum" fyrirtæki. Fyrirspurnir eru stofnaðar svo að öll fyrirtæki í sýndarfyrirtækinu hafi aðgang að gögnum í töflum tengdra töflusafna.

|   |  | 
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | - Sýndarfyrirtæki verður að vera uppsett áður en gögn eru geymd í töflum. Að bæta sýndarfyrirtæki eftirá við yfir fyrirliggjandi framkvæmd er mjög erfitt.<br><br>- Þar sem hefur verið svo mikið um stöðlun gagna í gildandi útgáfu af Dynamics AX, er orðið mjög erfitt að vita hvað skuli bæta við töflusöfn. Til dæmis er erfitt að vita hvaða töflum eigi að deila. Allar töflur sem vísað er til úr töflum sem eru í sýndarfyrirtæki verður að bæta við. Vegna Stöðlun Tafla verða jafnvel einfalt aðalgögn sem er dreift yfir margar töflur að vera hluti af sýndarfyrirtækinu. Öll mistök sem gerð eru hér munu valda virknivandamálum.<br><br>- Þegar tafla er hluti af sýndarfyrirtæki, tapar það upplýsingar um uppruna gagnanna, og aðeins sýndarfyrirtæki er skráð.   |
| **Skipt út fyrir aðra eiginleika?** | Altækar töflur er hægt að nota til að gera töflur aðgengilegar frá öllum fyrirtækjum. Það er engin útskipting sem stendur. |   
| **Afurðasvæði sem haft er áhrif á**       | Allar einingar |   
| **Staða**                       | Fjarlægt frá og með Dynamics AX 7.0.   |   

### <a name="windows-8-tablet-app"></a>Windows 8 spjaldtölvuforrit

Windows 8 spjaldtölvuforrit veittu aðgerðir fyrir kostnaðarfærslu og -samþykkt.

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Finance and Operations er samhæft við spjaldtölvur. Spjaldtölvuforrita er ekki lengur þörf.    |
| **Skipt út fyrir aðra eiginleika?**   | Nei.          |
| **Afurðasvæði sem haft er áhrif á**         | Útgjaldastýring   |
| **Staða**                         | Fjarlægt: Þessi virkni er aðeins tiltækur fyrir Dynamics AX 2012 R3. |

### <a name="workplanner"></a>Vinnuáætlun

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Lítil notkun |
| **Skipt út fyrir aðra eiginleika?**   | Nei, en **Forstillingarvensl** síðu sem er opnuð á **forstillingarflokks** síðu, styður sömu viðskiptaaðstæður og í hinu úrelta **vinnuáætlun** síðu. |
| **Afurðasvæði sem haft er áhrif á**         | Tími og mæting     |
| **Staða**                         | Kóðinn hefur ekki verið fjarlægður. Hins vegar var formið JmgWorkPlanner ekki flutt.    |

### <a name="x-financial-statements"></a>X++ fjárhagsskýrslur

|                                                 |                                                                                                          |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <strong>Ástæða úreldingar/fjarlægingar</strong> |                         Aðgerðinni hefur verið skipt út fyrir aðra eiginleika.                         |
|  <strong>Skipt út fyrir aðra eiginleika?</strong>  | Management Reporter (merktur <strong>fjárhagsskýrslugerð</strong> í þessari útgáfu af Dynamics AX) |
|     <strong>Afurðasvæði sem haft er áhrif á</strong>     |                                              Fjárhagur                                              |
|             <strong>Staða</strong>             |                                      Fjarlægt frá og með Dynamics AX 2012                                      |


