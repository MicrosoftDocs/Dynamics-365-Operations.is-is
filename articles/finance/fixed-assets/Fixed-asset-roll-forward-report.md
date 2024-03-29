---
title: Skýrsla fyrir framlengingu eigna
description: Þessi grein útskýrir hvernig á að nota skýrslu fyrir framlengingu eigna.
author: moaamer
ms.date: 01/08/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 23021
ms.assetid: d7e86f72-95db-4423-9b04-761e9536a959
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2017-12-20
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: a4d423b149957e624269231aede510190f0c14c7
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/29/2022
ms.locfileid: "9068781"
---
# <a name="fixed-assets-roll-forward-report"></a>Skýrsla fyrir framlengingu eigna

[!include [banner](../includes/banner.md)]

**Framlenging eigna** skýrslan veitir á auðlesanlegu Microsoft Excel snið nákvæmar upplýsingar um gögn á eignum sem þú þarfnast fyrir tímabil lokunar, fjárhagsskýrslna og skattaskýrslna. Í skýrslunni eru upphafs- og lokastaða á eignum ásamt verðmætaskiptum á tímabilinu og öll ný eignakaup og afskráningar sem áttu sér stað á tímabilinu. Gögn eru tilkynnt um einstaka eignir og einnig er virði tekið saman fyrir eignaflokka og lögaðila.

**Framlenging eigna** skýrslan notar ramma rafrænnar skýrslugerðar (ER). Áður en hægt er að keyra skýrsluna verður að flytja inn skilgreiningar á eignalíkaninu og framlagningu eigna frá Microsoft Dynamics Lifecycle Services (LCS). Hægt er að skoða leiðbeiningar í [Niðurhal skilgreininga fyrir rafræna skýrslugerð af Lifecycle Services](/dynamics365/unified-operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs)

Þessi skýrsla er fáanleg í Microsoft Dynamics 365 Finance, Enterprise Edition 7.3 eða sem bráðabót fyrir Microsoft Dynamics 365 Finance, Enterprise Edition (júlí 2017). Það verður að beita þremur bráðabótum á umhverfi sem er með júlí 2017 útgáfuna:

- **KB 4041754:** Ekki er hægt að hlaða niður skilgreiningum rafrænnar skýrslugerðar (ER) frá LCS, passar ekki við núverandi útgáfu eftir að hafa sótt uppfærslupakkann
- **KB 4056107:** Rafræn skýrslugerð (GER) heildaruppfærsla 5
- **KB 4056353:** Yfirlitsskýrsla og athugasemdir á eignirstöðu uppfyllir ekki skilyrði GAAP og IFRS

Eftirfarandi tafla lýsir svæðunum sem eru tiltæk í skýrslunni.


|                    Svæði                    |                                                                                                                                lýsing                                                                                                                                |
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|              Staða: Opnun              |                                                                                           Bókað nettóvirði eignar samkvæmt "frá" dagsetningunni sem er tilgreind í skýrslunni.                                                                                           |
|              Staða: Lokun              |                                                                                            Bókað nettóvirði eignar samkvæmt "til" dagsetningunni sem er tilgreind í skýrslunni.                                                                                            |
|         Kaup: Opnunargildi         |                                                 Summan af öllum færslum af gerðinni <strong>Kaup</strong> og <strong>Leiðrétting kaupa</strong> að "frá" dagsetningunni sem er tilgreind í skýrslunni.                                                  |
|      Kaup: Kauptímabil      |                                                 Summan af öllum færslum af gerðinni <strong>Kaup</strong> og <strong>Leiðrétting kaupa</strong> sem voru settar fram á dagsetningabili skýrslunnar.                                                  |
|       Kaup: Afskráningartímabil        |                                                                        Summan af öllum bakfærðum kaupum sem voru settar fram sem höfðu afskráningarfærslu á dagsetningabili skýrslunnar.                                                                        |
|         Kaup: Lokunargildi         |                                                  Summan af öllum færslum af gerðinni <strong>Kaup</strong> og <strong>Leiðrétting kaupa</strong> upp að "til" dagsetningunni sem er tilgreind í skýrslunni.                                                   |
|        Afskriftir: Opnunargildi         | Summan af öllum færslum af gerðinni <strong>Afskriftir</strong>, <strong>Leiðrétting afskrifta</strong>, <strong>Sérstök heimild til afskriftar</strong> og <strong>Óreglulegar afskriftir</strong> upp að "frá" dagsetningunni sem er tilgreind í skýrslunni. |
|     Afskriftir: Afskriftartímabil     |                         Summan af öllum færlsum af gerðinni <strong>Afskriftir</strong>, <strong>Leiðrétting afskrifta</strong> og <strong>Óreglulegar afskriftir</strong> sem voru settar fram á dagsetningabili skýrslunnar.                          |
| Afskriftir: Tímabil sérstakra afskrifta |                                                              Summan af öllum færslum af gerðinni <strong>Sérstök heimild til afskriftar</strong> sem voru settar fram á dagsetningabili skýrslunnar.                                                               |
|       Afskriftir: Afskráningartímabil       |                                                                       Summan af öllum bakfærðum afskriftum sem voru settar fram sem höfðu afskráningarfærslu á dagsetningabili skýrslunnar.                                                                        |
|        Afskriftir: Lokunargildi         |  Summan af öllum færslum af gerðinni <strong>Afskriftir</strong>, <strong>Leiðrétting afskrifta</strong>, <strong>Sérstök heimild afskriftar</strong> og <strong>Óreglulegar afskriftir</strong> upp að "til" dagsetningu sem er tilgreind í skýrslunni.  |
|    Skrifa-upp/skrifa-niður: Opnunargildi     |                              Summan af öllum færslum af gerðinni <strong>Skrifa upp leiðrétting</strong>, <strong>Skrifa niður leiðrétting</strong> og <strong>Endurmat</strong> upp að "frá" dagsetningunni sem er tilgreind í skýrslunni.                               |
|   Skrifa-upp/skrifa-niður: Skrifa upp tímabil   |                                                                    Summan af öllum færslum af gerðinni <strong>Skrifa upp leiðrétting</strong> sem voru settar fram á dagsetningabili skýrslunnar.                                                                    |
|  Skrifa-upp/Skrifa-niður: Skrifa niður tímabil  |                                                                   Summan af öllum færslum af gerðinni <strong>Skrifa niður leiðrétting</strong> sem voru settar fram á dagsetningabili skýrslunnar.                                                                   |
| Skrifa-upp/Skrifa-niður: Tímabil endurmats  |                                                                        Summan af öllum færslum af gerðinni <strong>Endurmat</strong> sem voru settar fram á dagsetningabili skýrslunnar.                                                                        |
|   Skrifa-upp/Skrifa-niður: Afskráningartímabil   |                                                           Summan af öllum skrifa-upp, skrifa-niður og bakfærðu endurmati sem voru settar sem höfðu afskráningarfærslu í rekstrarreikningi á dagsetningabili skýrslunnar.                                                           |
|    Skrifa-upp/skrifa-niður: Lokunargildi     |                               Summan af öllum færslum af gerðinni <strong>Skrifa upp leiðrétting</strong>, <strong>Skrifa niður leiðrétting</strong> og <strong>Endurmat</strong> upp að "til" dagsetningunni sem er tilgreind í skýrslunni.                                |
|          Afskráningar: Afskráningardagur           |                                                                                                                Afskráningardagurinn fyrir eignabókina.                                                                                                                |
|    Afskráningar: Bókað nettóvirði til afskráningar    |                                                                                                    Bókað nettóvirði á eignabókinni á tíma afskráningar.                                                                                                    |
|            Afskráningar: Söluvirði            |                                                                                               Söluvirði eignabókarinnar með afskráningu - sölufærsla.                                                                                                |
|           Afskráningar: Hrakvirði            |                                                                                               Hrakvirði eignabókarinnar með afskráningu - hrakfærslur.                                                                                               |
|           Afskráningar: Hagnaður/tap            |                                                                                 Hagnaðurinn eða tapið sem er reiknað sem hluti af afskráningarfærslu fyrir eignabókina.                                                                                 |



[!INCLUDE[footer-include](../../includes/footer-banner.md)]

