---
title: "Skýrsla fyrir framlengingu eigna"
description: "Þetta efni útskýrir hvernig á að nota skýrslu fyrir framlengingu eigna."
author: saraschi2
manager: 
ms.date: 01/08/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 23021
ms.assetid: d7e86f72-95db-4423-9b04-761e9536a959
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-12-20
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: 8075abccdcdde21df967dcc9948a738895f35cef
ms.openlocfilehash: 0a78df4ede8fd57afbc3e9a7e5a38b840f479cdf
ms.contentlocale: is-is
ms.lasthandoff: 01/25/2018

---
# <a name="fixed-assets-roll-forward-report"></a>Skýrsla fyrir framlengingu eigna

[!include[banner](../includes/banner.md)]

**Framlenging eigna** skýrslan veitir á auðlesanlegu Microsoft Excel snið nákvæmar upplýsingar um gögn á eignum sem þú þarfnast fyrir tímabil lokunar, fjárhagsskýrslna og skattaskýrslna. Í skýrslunni eru upphafs- og lokastaða á eignum ásamt verðmætaskiptum á tímabilinu og öll ný eignakaup og afskráningar sem áttu sér stað á tímabilinu. Gögn eru tilkynnt um einstaka eignir og einnig er virði tekið saman fyrir eignaflokka og lögaðila.

**Framlenging eigna** skýrslan notar ramma rafrænnar skýrslugerðar (ER). Áður en hægt er að keyra skýrsluna verður að flytja inn skilgreiningar á eignalíkaninu og framlangingu eigna frá Microsoft Dynamics Lifecycle Services (LCS). Hægt er að skoða leiðbeiningar í [Niðurhal skilgreininga fyrir rafræna skýrslugerð af Lifecycle Services](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs)

Þessi skýrsla er fáanleg í Microsoft Dynamics 365 fyrir Finance and Operations, Enterprise edition 7.3 eða sem bráðabót fyrir Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (July 2017). Það verður að beita þremur bráðabótum á umhverfi sem er með júlí 2017 útgáfuna:

- **KB 4041754:** Ekki er hægt að hlaða niður skilgreiningum rafrænnar skýrslugerðar (ER) frá LCS, passar ekki við núverandi útgáfu forrits eftir að hafa sótt uppfærslupakkann
- **KB 4056107:** Rafræn skýrslugerð (GER) heildaruppfærsla 5
- **KB 4056353:** Yfirlitsskýrsla og athugasemdir á eignirstöðu uppfyllir ekki skilyrði GAAP og IFRS

Eftirfarandi tafla lýsir svæðunum sem eru tiltæk í skýrslunni.

| Svæði                                       | lýsing |
|---------------------------------------------|-------------|
| Staða: Opnun                           | Bókað nettóvirði eignar samkvæmt "frá" dagsetningunni sem er tilgreind í skýrslunni. |
| Staða: Lokun                           | Bókað nettóvirði eignar samkvæmt "til" dagsetningunni sem er tilgreind í skýrslunni. |
| Kaup: Opnunargildi                 | Summan af öllum færslum af gerðinni **Kaup** og **Leiðrétting kaupa** að "frá" dagsetningunni sem er tilgreind í skýrslunni. |
| Kaup: Kauptímabil           | Summan af öllum færslum af gerðinni **Kaup** og **Leiðrétting kaupa** sem voru settar fram á dagsetningabili skýrslunnar. |
| Kaup: Afskráningartímabil              | Summan af öllum bakfærðum kaupum sem voru settar fram sem höfðu afskráningarfærslu á dagsetningabili skýrslunnar. |
| Kaup: Lokunargildi                 | Summan af öllum færslum af gerðinni **Kaup** og **Leiðrétting kaupa** upp að "til" dagsetningunni sem er tilgreind í skýrslunni. |
| Afskriftir: Opnunargildi                | Summan af öllum færslum af gerðinni **Afskriftir**, **Leiðrétting afskrifta**, **Sérstök heimild til afskriftar** og **Óreglulegar afskriftir** upp að "frá" dagsetningunni sem er tilgreind í skýrslunni. |
| Afskriftir: Afskriftartímabil         | Summan af öllum færlsum af gerðinni **Afskriftir**, **Leiðrétting afskrifta** og **Óreglulegar afskriftir** sem voru settar fram á dagsetningabili skýrslunnar. |
| Afskriftir: Tímabil sérstakra afskrifta | Summan af öllum færslum af gerðinni **Sérstök heimild til afskriftar** sem voru settar fram á dagsetningabili skýrslunnar. |
| Afskriftir: Afskráningartímabil             | Summan af öllum bakfærðum afskriftum sem voru settar fram sem höfðu afskráningarfærslu á dagsetningabili skýrslunnar. |
| Afskriftir: Lokunargildi                | Summan af öllum færslum af gerðinni **Afskriftir**, **Leiðrétting afskrifta**, **Sérstök heimild afskriftar** og **Óreglulegar afskriftir** upp að "til" dagsetningu sem er tilgreind í skýrslunni. |
| Skrifa-upp/skrifa-niður: Opnunargildi        | Summan af öllum færslum af gerðinni **Skrifa upp leiðrétting**, **Skrifa niður leiðrétting** og **Endurmat** upp að "frá" dagsetningunni sem er tilgreind í skýrslunni. |
| Skrifa-upp/skrifa-niður: Skrifa upp tímabil     | Summan af öllum færslum af gerðinni **Skrifa upp leiðrétting** sem voru settar fram á dagsetningabili skýrslunnar. |
| Skrifa-upp/Skrifa-niður: Skrifa niður tímabil   | Summan af öllum færslum af gerðinni **Skrifa niður leiðrétting** sem voru settar fram á dagsetningabili skýrslunnar. |
| Skrifa-upp/Skrifa-niður: Tímabil endurmats  | Summan af öllum færslum af gerðinni **Endurmat** sem voru settar fram á dagsetningabili skýrslunnar. |
| Skrifa-upp/Skrifa-niður: Afskráningartímabil     | Summan af öllum skrifa-upp, skrifa-niður og bakfærðu endurmati sem voru settar sem höfðu afskráningarfærslu í rekstrarreikningi á dagsetningabili skýrslunnar. |
| Skrifa-upp/skrifa-niður: Lokunargildi        | Summan af öllum færslum af gerðinni **Skrifa upp leiðrétting**, **Skrifa niður leiðrétting** og **Endurmat** upp að "til" dagsetningunni sem er tilgreind í skýrslunni. |
| Afskráningar: Afskráningardagur                    | Afskráningardagurinn fyrir eignabókina. |
| Afskráningar: Bókað nettóvirði til afskráningar       | Bókað nettóvirði á eignabókinni á tíma afskráningar. |
| Afskráningar: Söluvirði                       | Söluvirði eignabókarinnar með afskráningu - sölufærsla. |
| Afskráningar: Hrakvirði                      | Hrakvirði eignabókarinnar með afskráningu - hrakfærslur. |
| Afskráningar: Hagnaður/tap                      | Hagnaðurinn eða tapið sem er reiknað sem hluti af afskráningarfærslu fyrir eignabókina. |
