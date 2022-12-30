---
title: Afkastavísar (KPI) eignar
description: Þessi grein útskýrir afkastavísa í Eignastýringu.
author: johanhoffmann
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetObjectKPI
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ef0df92edaa2ee33bd75e01a666086e32c8101af
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870872"
---
# <a name="asset-kpis"></a>Afkastavísar (KPI) eignar

[!include [banner](../../includes/banner.md)]

 

Í eignastjórnun geturðu reiknað út ýmsa afkastavísa fyrir eignir og eignategundir. Þú notar afkastavísa til að fá yfirsýn yfir afkomu eigna í tengslum við t.d. uppitíma, niðritíma, viðgerðartíma og meðaltíma milli bilana (MTBF).

1. Smelltu á **Eignastýringu** > **Fyrirspurnir** > **Eignir** > **Afkastavísi eigna**.

2. Í valmyndinni **Reikna afkastavísi eigna** velurðu **Tímakvarði** til að nota við útreikning og tímabil í reitunum **Frá dagsetningu** og **Til dagsetningar**. 

3. Á flýtiflipanum **Færslur til að taka með** er hægt að velja sérstakar eignir og eignategundir sem eiga að vera með í útreikningnum, ef þess þarf.

4. Smellið á **Í lagi** til að byrja að reikna.

5. Á flýtiflipanum **Yfirlit** eru niðurstöður útreikningsins birtar í töfluyfirliti. Hver eign er sýnd á sérstakri línu.

6. Á flýtiflipanum **Afkastavísir fyrir valda línu** sérðu útreikninga fyrir eignina sem var valin á flýtiflipanum **Yfirlit**. Afkastavísisgildin eru flokkuð varðandi **Tíma**, **Framboð**, **Verkbeiðnir**, **Viðhald**, **Bilanir**, **Niðurtíma vegna viðhalds** og **Kostnað**.

Í töflunni hér að neðan finnur þú lýsingu á reitunum á síðunni **Afkastavísar eigna**.

| Svæði                   | Lýsing                                                                                                                                                                                                                                                                                           |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Eign                   | Kenni eignar.                                                                                                                                                                                                                                                                                             |
| Heildartími              | Heildartími settur upp í dagatalinu sem notað er við útreikninginn. Ef eignin er tengd tilföngum er tengt tilfangadagatal notað. Ef eignin tengist ekki tilföngum er dagatalið sem valið er í reitnum **Staðlað dagatal** í **Færibreytur eignastýringar** notað. |
| Upptími                  | Heildartími að frádregnum niðritíma.                                                                                                                                                                                                                                                                            |
| Niðurtími                | Skráningar á niðurtíma vegna viðhalds sem gerðar hafa verið á eigninni á völdu tímabili.                                                                                                                                                                                                                              |
| Viðgerðartími             | Heildarfjöldi vinnustunda sem eru nýttar í verkbeiðnir um viðgerðir.                                                                                                                                                                                                                                            |
| Framboð %          | Spennutími deilt með heildartíma og margfaldað með 100.                                                                                                                                                                                                                                                   |
| Fjöldi bilana        | Fjöldi skráðra bilunarástæðna á bilunareinkennum á eigninni á völdu tímabili.                                                                                                                                                                                                             |
| MTBF                    | Meðaltími milli bilana, sem er heildartími deilt með fjölda bilana sem skráðar eru á eignina á völdu tímabili. Ef fjöldi bilana er núll er meðaltími milli bilana stilltur á heildartíma.                                                                                                                   |
| Bilanatíðni               | 1 deilt með meðaltíma milli bilana.                                                                                                                                                                                                                                                                                    |
| MRT                     | Meðaltími milli viðgerða, sem er viðgerðartími deilt með fjölda bilana sem skráðar eru á eignina á völdu tímabili. Ef fjöldi bilana er núll er meðaltími milli viðgerða stilltur á heildartíma.                                                                                                                           |
| Fjöldi stöðvana         | Fjöldi skráninga niðurtíma vegna viðhalds sem er stofnaður á eigninni.                                                                                                                                                                                                                                     |
| MTBS                    | Meðaltími milli stöðvana, sem er heildartími deilt með fjölda skráninga á niðurtíma vegna viðhalds. Ef fjöldi skráninga niðurtíma vegna viðhalds er núll á völdu tímabili er gildi meðaltíma á milli stöðvana stillt á heildartíma.                                                                                      |
| Fyrirbyggjandi kostnaður         | Kostnaður bókfærður á eignina sem tengist kostnaðartegundinni „Forvarnir“ á völdu tímabili. Kostnaðartegundir eru settar upp eftir tegundum verkbeiðni.                                                                                                                                                                       |
| Leiðréttandi kostnaður         | Kostnaður bókfærður á eignina sem tengist kostnaðartegundinni „Leiðréttandi“ á völdu tímabili. Kostnaðartegundir eru settar upp eftir tegundum verkbeiðni.                                                                                                                                                                       |
| Gildi útskiptingar       | Gildi skilgreint á eigninni sem endurnýjunarkostnaður.                                                                                                                                                                                                                                                  |
| Gerð eignar             | Auðkenni á eignategundinni sem er valin á eigninni.                                                                                                                                                                                                                                             |
| Framleiðandi           | Auðkenni á framleiðandanum sem er valinn á eigninni.                                                                                                                                                                                                                                                 |
| Tegund                   | Auðkenni á framleiðslulíkaninu sem er valið á eigninni.                                                                                                                                                                                                                                           |
| Upphafsdagsetning               | Upphafsdagsetning afkastaútreiknings. Ef eignin var stofnuð eftir upphafsdaginn sem valinn var fyrir útreikninginn er upphafsdagur eignarinnar sýndur í þessum reit.                                                                                                                                  |
| Lokadagsetning                 | Lokadagsetning útreiknings afkastavísis. Ef eignin var skráð sem óvirk á undan lokadagsetningunni sem valin var fyrir útreikninginn, birtist dagsetningin sem eignin var ekki lengur virk frá í þessum reit.                                                                                               |
| Tímakvarði              | Við útreikning á afkastavísunum velurðu tímakvarða sem á að nota: Klukkutímar, dagar eða vikur.                                                                                                                                                                                                            |
| Til ráðstöfunar            | Uppitími deilt með heildartíma.                                                                                                                                                                                                                                                                         |
| Verkbeiðnir             | Heildarfjöldi verkbeiðna sem eru hafðar með í útreikningi á afkastavísi.                                                                                                                                                                                                                                          |
| Tími verkbeiðni         | Heildarfjöldi vinnustunda sem eru nýttar í verkbeiðnirnar.                                                                                                                                                                                                                                               |
| Helstu verkbeiðnir     | Fjöldi aðalverkbeiðna sem eru hafðar með í útreikningi á afkastavísi.                                                                                                                                                                                                                                        |
| Aðrar verkbeiðnir   | Fjöldi annars flokks verkbeiðna sem eru hafðar með í útreikningi á afkastavísi.                                                                                                                                                                                                                                      |
| Verkbeiðnir viðhalds | Fjöldi viðhaldsverkbeiðna sem eru hafðar með í útreikningi á afkastavísi. Viðhaldsverkbeiðni er verkbeiðni án skyldra orsaka bilana.                                                                                                                                                             |
| Viðhaldstími        | Heildarfjöldi vinnustunda sem eru nýttar í viðhaldsverkbeiðnir.                                                                                                                                                                                                                                       |
| Lagfæra verkbeiðnir      | Fjöldi verkbeiðna um viðgerðir sem eru hafðar með í útreikningi á afkastavísi. Verkbeiðni um viðgerð er verkbeiðni með skyldar orsakir bilana.                                                                                                                                                                        |
| Áreiðanleiki %           | Útreikningur byggist á áætlaðri veldisþróun í bilanaskráningum á eign sem þýðir að með tímanum minnkar áreiðanleiki eignarinnar vegna slits. Útreikningur á þessum afkastavísi byggist á meðaltíma milli bilana og heildartíma.                                                            |
| MTPS                    | Meðaltími milli framleiðslustöðvana, sem er niðurtími vegna viðhalds deilt með fjölda skráninga á niðurtíma vegna viðhalds. Ef fjöldi skráninga á niðurtíma vegna viðhalds er núll á völdu tímabili er gildi meðaltíma á milli stöðvana stillt á núll.                                                                               |
| Heildarkostnaður              | Heildarkostnaður bókfærður á eignina á völdu tímabili.                                                                                                                                                                                                                                              |
| Fjárfestingarkostnaður         | Kostnaður bókfærður á eignina sem tengist kostnaðartegundinni „Fjárfesting“ á völdu tímabili. Kostnaðartegundir eru settar upp eftir tegundum verkbeiðni.                                                                                                                                                                       |

Myndin hér að neðan sýnir skjámynd af útreikningi afkastavísis fyrir fjórar eignir.

![Skjáskot af KPI-útreikningi á fjórum eignum.](media/11-controlling-and-reporting.png)

- Þú getur valið margar eignir í **Allar eignir** og smellt á hnappinn **Afkastavísir eigna** á flipanum **Almennt**. Síðan smellirðu á **Í lagi** í valmyndinni **Reikna afkastavísi eigna** til að reikna út afkastavísi fyrir valdar eignir.  
- Niðurstöður úr útreikningi á afkastavísi kunna að innihalda eða ekki [skráningar á niðurtíma vegna viðhalds](../work-orders/maintenance-downtime.md), allt eftir uppsetningu og notkun á ástæðukóða fyrir niðurtíma vegna viðhalds. 



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]