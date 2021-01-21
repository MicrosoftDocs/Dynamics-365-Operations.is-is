---
title: Setja upp leigubókunarlykla
description: Þetta efnisatriði birtir lista yfir áskilda bókunarlykla fyrir eignarleigufærslur og útskýrir hvernig á að skilgreina bókunarlykla á síðunni færibreytur leigubókunar.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 8ca1c6eea854577e5aa34b1a9b9d1731b209527b
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/28/2020
ms.locfileid: "4444570"
---
# <a name="set-up-lease-posting-accounts"></a>Setja upp leigubókunarlykla

[!include [banner](../includes/banner.md)]

Þetta efnisatriði birtir lista yfir áskilda bókunarlykla fyrir eignarleigufærslur og útskýrir hvernig á að skilgreina bókunarlykla á síðunni **Færibreytur leigubókunar**.

Til að uppfylla skilyrði efnisatriðis um skráningarkerfi reikningsskilastaðla 842 (ASC 842) og alþjóðlegan reikningsskilastaðal 16 (IFRS 16) verður þú hugsanlega að stofan reikninga í bókhaldslyklum þínum. Hins vegar eru allir lyklar sem eru stofnaðir til að uppfylla skilyrði ASC og IFRS-staðla ekki eignalyklar. Samkvæmt ASC 842 er afnotaréttur af eign bæði fyrir fjármagnsleigusamninga og rekstrarleigusamninga. Þessir leigusamningar eru aðskildir frá eignum. (Enn er hægt að vinna með afnotarétt af eign með því að nota eignir.)

Frekari upplýsingar um hvernig á að stofna lykilskipulag er að finna í [Stofna lykilskipulög](../general-ledger/tasks/create-account-structures.md). Frekari upplýsingar um hvernig á að stofna aðallykil er að finna í [Stofna aðallykil](../general-ledger/tasks/create-main-account.md).

Eftirfarandi tafla sýnir dæmi um lykla sem þarf að stofna fyrir færslur leigðar eignar, ef þær hafa ekki þegar verið stofnaðar. Samkvæmt IFRS 16 eru rekstrarleigusamningar enn notaðir fyrir lágvirðiskeðjur og verðlitla leigusamninga og skammtímaleigusamninga.

| Númer fjárhagslykils | Lykilgerð  | Heiti lykils                                          |
|-----------------------|---------------|-------------------------------------------------------|
| 180150                | Eign         | Afnotaréttur af eign, ökutæki                                     |
| 180160                | Eign         | Afnotaréttur af eign, bygging                                    |
| 180250                | Eign         | Uppsafnaðar afskriftir - ökutæki                   |
| 180260                | Eign         | Uppsafnaðar afskriftir - byggingar                  |
| 222300                | Skuld     | Skammtímaskuldbinding - fjármögnunarleigusamningar                |
| 222310                | Efnahagsreikningur | Skammtímaskuldbinding - rekstrarleigusamningar              |
| 250200                | Skuld     | Víxilskuldir                                         |
| 250601                | Efnahagsreikningur | Langtímaskuldbinding - fjármögnunarleigusamningar                 |
| 250602                | Efnahagsreikningur | Langtímaskuldbinding - rekstrarleigusamningar               |
| 250606                | Efnahagsreikningur | Frestaðar leigugreiðslur                                         |
| 300160                | Efnahagsreikningur | Óráðstafað eigið fé                                     |
| 604500                | Expense       | Leigukostnaður                                         |
| 604501                | Expense       | Rekstrarleigukostnaður ökutækis - uppsöfnun vaxta  |
| 604502                | Expense       | Rekstrarleigukostnaður ökutækis - afskrift        |
| 605200                | Expense       | Rekstrarleigukostnaður byggingar - uppsöfnun vaxta |
| 605201                | Expense       | Rekstrarleigukostnaður byggingar - afskrift       |
| 607101                | Expense       | Kostnaður afskriftar leigusamnings ökutækis                    |
| 607102                | Expense       | Kostnaður afskriftar leigusamnings byggingar                   |
| 607103                | Expense       | Kostnaður virðisrýrnunar - fjármögnunarleigusamningar                   |
| 607104                | Expense       | Kostnaður virðisrýrnunar - rekstrarleigusamningar                 |
| 618910                | Expense       | Leigukostnaður - fjármögnunarleigusamningar                        |
| 618920                | Expense       | Breytilegar greiðslur - fjármögnunarleigusamningar                    |
| 618930                | Expense       | Breytilegar greiðslur - rekstrarleigusamningar                  |
| 800600                | Expense       | Vaxtakostnaður leigusamnings ökutækis                        |
| 800601                | Expense       | Vaxtakostnaður leigusamnings byggingar                       |
| 801201                | Efnahagsreikningur | Hagnaður og tap - leiðréttingar á leigusamningi                      |

## <a name="configure-posting-accounts"></a>Skilgreina bókunarlykil

Til að úthluta lyklum á leigubækur og-flokka sem hafa verið stofnaðir verður að skilgreina færibreytur fyrir eignarleigu.

1. Opnið **Eignarleiga \> Uppsetning \> Færibreytur leigubókunar**.
2. Á flipanum **Lyklar** skal opna flipann **Leigulyklar**. Veldu aðallykla fyrir fjármögnunar- og rekstrarleigusamninga í viðeigandi **Bókunargerð**. Taflan hér á undan sýnir lykla sem tengjast fjármögnunar- og rekstrarleigusamningum.

    > [!NOTE]
    > Þetta skref krefst þess að settir sé upp aðskildir lyklar bæði fyrir fjármögnunar- og rekstrarleigusamnina fyrir hverja bókunargerð nema **Jöfnun leigukostnaðar** og **Hækkun/lækkun leigu**. Fyrirtæki sem vinna samkvæmt IFRS 16 bókhaldsrammanum verða að bæta við aðallykli fyrir rekstrarleigusamning. Kerfið notar ekki þennan lykil þrátt fyrir að um áskilið svæði sé að ræða vegna þess að allir leigusamningar samkvæmt IFRS 16 eru flokkaðir sem fjármögnunarleigusamningar.
    >[!NOTE]
    > **Hækkun/lækkun leigu** verður notað sem bókunargerð fyrir önnur atriði varðandi eign, þar á meðal **Stofnkostnaður, leiguhvati, fyrirframgreiðslur leigu og kostnaður sundurhlutunar**, en ekki er hægt að bóka á aðallykil afnotaréttar af eign sem sjálfgefið er stilltur á **Leigja eign**.        
    
3. Til að velja tiltekinn leigusamningsflokk sem samsvarar aðallykli í svæðinu **Kóði lykils** skal velja **Flokk**. Síðan í svæðinu **Númer lykils/flokks** skal velja leigusamningsflokkinn sem á að úthluta á aðallykilinn.
4. Til að úthluta kóðum lykla á stjórnsýslukostnaðinn sem hefur verið settur upp í kerfinu skal velja kostnað á flýtiflipanum **Rekstrarkostnaður** á svæðinu **Kostnaðargerð**. Úthlutaðu síðan fjármögnunar- og rekstrarleigusamningum sem skal nota fyrir hverja bók.

    > [!NOTE]
    > Valinn fjármögnunar- eða rekstralykill verður debetfærður þegar reikningur fyrir áætluð útgjöld er bókaður.
    > **Jöfnun leigukostnaðar** er notuð sem bókunargerð fyrir færslur rekstrarkostnaðar en bókað er á skilgreinda **Mótlykilinn** í **Greiðsluáætlunarlínur rekstrarkostnaðar** í upplýsingum um leigusamning eða eyðublað leigubókar.   