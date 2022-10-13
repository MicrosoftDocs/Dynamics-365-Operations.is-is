---
title: Samanburður á skýi og eiginleikum á staðnum
description: Greinin sýnir hvaða eiginleikar eru studdir í Cloud og á staðnum.
author: sericks007
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 89563
ms.assetid: ''
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2017-11-29
ms.dyn365.ops.version: Platform update 9
ms.openlocfilehash: e3b200186096a49f800d5b650ac81a45fe5e9e30
ms.sourcegitcommit: c5f2cba3c2b0758e536eeaaa40506659a53085e1
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/12/2022
ms.locfileid: "9644142"
---
# <a name="comparison-of-cloud-and-on-premises-features"></a>Samanburður á skýi og eiginleikum á staðnum

[!include [banner](../includes/banner.md)]

Þessi grein sýnir samanburð á eiginleikum sem eru tiltækir í skýi á móti innanhúss fyrir eftirfarandi forrit:

- [Dynamics 365 Finance](cloud-prem-comparison.md#dynamics-365-finance)
- [Dynamics 365 Supply Chain Management](cloud-prem-comparison.md#dynamics-365-supply-chain-management)
- [Dynamics 365 Commerce](cloud-prem-comparison.md#dynamics-365-commerce)
- [Dynamics 365 Human Resources](cloud-prem-comparison.md#dynamics-365-human-resources)

Upplýsingar um [þróun og stjórnunaraðgerðir](cloud-prem-comparison.md#development-and-administration-features) eru einnig innifaldar.

Í eftirfarandi töflu er listi yfir forritasvæðin. Stuðningur fyrir ský og staðbundna notkun er talinn upp í heild fyrir þennan eiginleika. Ef tilteknir eiginleikar eru frábrugðnir því sem er á heildarsviðinu eru eiginleikarnir skráðir í aðskilinni línu í dálkinum eiginleikar.

## <a name="dynamics-365-finance"></a>Dynamics 365 Finance

| **Svæði**             | **Eiginleiki**                | **Ský** | **Innanhúss** |
|---------------------|-----------------------------|-----------|-----------------|
| Samræmi og Vottun        |                                                                                           | Já       | Já             |
|                                      | SOC 1 gerð 1 vottun                                                                | Já       | Nei              |
| Gagnastjórnun og samþætting      |                                                                                           | Já       | Já             |
|                                      | Flytja út gögn í eigin gagnavöruhús                                                    | Já       | Já             |
|                                      | Virkja útflutning á stigvaxandi uppfærslum á gagnaeiningu                                 | Já       | Já             |
|                                      | Gagnasamþættingar                                                                         | Já       | Já             |
| Skjalastjórnun                  |                                                                                           | Já       | Já             |
| Fjármálastjórnun                 |                                                                                           | Já       | Já             |
| Hjálp                                 |                                                                                           | Já       | Nei              |
| Mannauður                      |                                                                                           | Já       | Já             |
| Greind                         |                                                                                           | Já       | Já             |
|                                      | Rafræn skýrslugerð (ER)                                                                 | Já       | Já             |
|                                      | Rafræn skýrslugerð: Samþætting við LCS                                                                  | Já       | Nei              |
|                                      | Rafræn skýrslugerð: Samþætting við SharePoint                                                           | Já       | Nei              |
|                                      | Rafræn skýrslugerð: Regluskilgreiningarþjónusta (RCS)                              | Já       | Nei              |
|                                      | Rafræn skýrslugerð: Notar staðbundið skráarkerfi sem geymslu á skilgreiningum rafrænnar skýrslugerðar sem er aðgengileg í gegnum gagnasafn rafrænnar skýrslugerðar | Nei        | Já             |
|                                      | Sameining með PowerBI.com                                                              | Já       | Nei              |
|                                      | Samþætting við PowerBI Desktop                                                          | Nei        | Já             |
|                                      | Greiningarvinnusvæði                                                                     | Já       | Nei              |
|                                      | Snjallrekstrarferlar: Ráðleggingar´                                             | Já       | Nei              |
|                                      | Skrifa Power BI skýrslur með OData með því að nota Power BI skjáborð eða Excel PowerQuery verkfæri    | Já       | Nei              |
|                                      | SQL Server Reporting Services (SSRS) styður kvörðun út                                 | Já       | Já             |
|                                      | Telemetry er flutt í skýið                                                   | Já       | Nei              |
| Lifecycle Services                   |                                                                                           | Já       | Já             |
|                                      | Skilgreinanlegir rekstrarferlar                                                           | Já       | Nei              |
| Staðfæringar                        |                                                                                           | Já       | Já             |
| Fartækjaforrit, vinnusvæði og kerfi |                                                                                           | Já       | Já             |
| Office-samþætting                   |                                                                                           | Já       | Já             |
| Fyrirtækisstjórnun          |                                                                                           | Já       | Já             |
| Laun                              |                                                                                           | Já       | Já             |
|                                      | Beingreiðsla                                                                            | Já       | Nei              |
| Verkefnastjórnun og bókhald    |                                                                                           | Já       | Já             |
| Öryggi                             |                                                                                           | Já       | Já             |
| Þjónustustjórnun                   |                                                                                           | Já       | Já             |
| Vefbiðlari                           |                                                                                           | Já       | Já             |
|                                      | Verkskráning - Vista eða sækja verkskráningar úr BPM-safni                         | Já       | Nei              |
| Stuðningur                              |                                                                                           | Já       | Já             |
|                                      | Aðgangur að stuðningi gegnum valmynd fyrir Hjálp og stuðning                                             | Já       | Nei              |
|                                      | Viðskiptatilvik                                                                           | Já       | Já (annaðhvort er internetsamband áskilið eða sérsniðnar endastöðvar verða að vera innleiddar til að senda/taka á móti viðskiptatilvikum á innra neti)              |

## <a name="dynamics-365-supply-chain-management"></a>Dynamics 365 Supply Chain Management 

| **Svæði**                | **Eiginleiki**             | **Ský** | **Innanhúss** |
|-------------------------|-------------------|-----------|-----------------|
| Eignastýring                     |                                                                                           | Já       | Já             |
| Samræmi og Vottun        |                                                                                           | Já       | Já             |
|                                      | SOC 1 gerð 1 vottun                                                                | Já       | Nei              |
| Kostnaðarbókhald                      |                                                                                           | Já       | Já             |
|                                      | Efnispakki fyrir kostnaðarbókhald fyrir Power BI                                                 | Já       | Nei              |
|                                      | Vinnusvæði kostnaðarbókhalds fyrir fartækjaforrit                                                  | Já       | Nei              |
| Kostnaðarstýring                      |                                                                                           | Já       | Já             |
|                                      | Kostnaðarstjórnunar-efnispakki fyrir Power BI                                                 | Já       | Nei              |
| Gagnastjórnun og samþætting      |                                                                                           | Já       | Já             |
|                                      | Skilgreiningastýrð viðbót                                                            | Já       | Nei              |
|                                      | Flytja út gögn í eigin gagnavöruhús                                                    | Já       | Já             |
|                                      | Virkja útflutning á stigvaxandi uppfærslum á gagnaeiningu                                 | Já       | Já             |
|                                      | Gagnasamþættingar                                                                         | Já       | Já             |
| Skjalastjórnun                  |                                                                                           | Já       | Já             |
| Hjálp                                 |                                                                                           | Já       | Nei              |
| Greind                         |                                                                                           | Já       | Já             |
|                                      | Rafræn skýrslugerð (ER)                                                                 | Já       | Já             |
|                                      | Rafræn skýrslugerð: Samþætting við LCS                                                                  | Já       | Nei              |
|                                      | Rafræn skýrslugerð: Samþætting við SharePoint                                                           | Já       | Nei              |
|                                      | Rafræn skýrslugerð: Regluskilgreiningarþjónusta (RCS)                              | Já       | Nei              |
|                                      | Rafræn skýrslugerð: Notar staðbundið skráarkerfi sem geymslu á skilgreiningum rafrænnar skýrslugerðar sem er aðgengileg í gegnum gagnasafn rafrænnar skýrslugerðar | Nei        | Já             |
|                                      | Sameining með PowerBI.com                                                              | Já       | Nei              |
|                                      | Samþætting við PowerBI Desktop                                                          | Nei        | Já             |
|                                      | Greiningarvinnusvæði                                                                     | Já       | Nei              |
|                                      | Snjallrekstrarferlar: Ráðleggingar´                                             | Já       | Nei              |
|                                      | Skrifa Power BI skýrslur með OData með því að nota Power BI skjáborð eða Excel PowerQuery verkfæri    | Já       | Nei              |
|                                      | SQL Server Reporting Services (SSRS) styður kvörðun út                                 | Já       | Já             |
|                                      | Telemetry er flutt í skýið                                                   | Já       | Nei              |
| Birgðir                 |                                                                                           | Já       | Já             |
| Lifecycle Services                   |                                                                                           | Já       | Já             |
|                                      | Skilgreinanlegir rekstrarferlar                                                           | Já       | Nei              |
| Staðfæringar                        |                                                                                           | Já       | Já             |
| Framleiðsla                        |                                                                                           | Já       | Já             |
| Aðaláætlanagerð og spár      |                                                                                           | Já       | Já             |
|                                      | Fínstilling áætlanagerðar                                                                     | Já       | Nr.              |
|                                      | Eftirspurnarspá                                                                        | Já       | Nr.              |
| Fartækjaforrit, vinnusvæði og kerfi |                                                                                           | Já       | Já             |
| Office-samþætting                   |                                                                                           | Já       | Já             |
| Fyrirtækisstjórnun          |                                                                                           | Já       | Já             |
| Innkaup og aðföng             |                                                                                           | Já       | Já             |
|                                      | Aðgangur að ytri vörulista úr innkaupabeiðni                                   | Já       | Nei              |
|                                      | Eyðslugreining innkaupa Power BI skýrslur                                                  | Já       | Nei              |
| Vöruupplýsingastjórnun       |                                                                                           | Já       | Já             |
| Afurðarsniðmát                  |                                                                                           | Já       | Já             |
| Framleiðsla                           |                                                                                           | Já       | Já             |
|                                      | Framleiðsluafköst Power BI skýrslur                                                   | Já       | Nei              |
| Verkefnastjórnun og bókhald    |                                                                                           | Já       | Já             |
| Sala                                |                                                                                           | Já       | Já             |
|                                      | Sölu- og arðsemisframmistaða Power BI skýrslur                                      | Já       | Nei              |
| Öryggi                             |                                                                                           | Já       | Já             |
| Þjónustustjórnun                   |                                                                                           | Já       | Já             |
| Stjórnun aðfangakeðju              |                                                                                           | Já       | Já             |
| Flutningsstjórnun            |                                                                                           | Já       | Já             |
| Samstarf lánardrottna                 |                                                                                           | Já       | Nei              |
| Vöruhúsakerfi                 |                                                                                           | Já       | Já             |
|                                      | Fartækjaforrit fyrir vöruhús                                                                      | Já       | Já             |
|                                      | Vörhús Power BI skýrslur                                                              | Já       | Nei              |
| Vefbiðlari                           |                                                                                           | Já       | Já             |
|                                      | Verkskráning - Vista eða sækja verkskráningar úr BPM-safni                         | Já       | Nei              |
| Stuðningur                              |                                                                                           | Já       | Já             |
|                                      | Aðgangur að stuðningi gegnum valmynd fyrir Hjálp og stuðning                                             | Já       | Nei              |

## <a name="dynamics-365-commerce"></a>Dynamics 365 Commerce 

Til að sjá lista yfir eiginleika sem eru tiltækir í uppsetningu á staðnum skal skoða [Commerce-eiginleikar sem eru í boði í uppsetningu á staðnum](../../../commerce/retail-onprem.md).

## <a name="dynamics-365-human-resources"></a>Dynamics 365 Human Resources 

| **Svæði**         | **Eiginleiki**         | **Ský** | **Innanhúss** |
|------------------|---------------------|-----------|-----------------|
| Öll svæði Mannauðs | Allir eiginleikar Mannauðs | Já       | Nei              |

## <a name="development-and-administration-features"></a>Þróunar- og stjórnunareiginleikar

| **Svæði**                   | **Eiginleiki**                               | **Ský** | **Innanhúss** |
|----------------------------|-------------------------------------------|-----------|-----------------|
| Bygging og prófun             |                                           | Já       | Já             |
| Stækkunarhæfni              |                                           | Já       | Já             |
| Eftirlit og fjarmælingar   |                                           | Já       | Já             |
| Samhæfi kerfa     |                                           | Já       | Já             |
| Þjónusta                  |                                           | Já       | Já             |
|                            | Þjónustuumhverfi                    | Já       | Nei              |
| Rakningarþáttari               |                                           | Já       | Já             |
| PerfTimer                  |                                           | Já       | Já\*           |
| Uppfæra                    |                                           | Já       | Já             |
|                            | Uppfæra                                   | Já       | Nei              |
|                            | Uppfærsla og stuðningur fyrir fyrri útgáfur | Já       | Nei              |
| Visual Studio þróun  |                                           | Já       | Já             |

\* Í umhverfi á staðnum sýnir PerfTimer aðeins niðurstöður fyrir biðlarann.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
