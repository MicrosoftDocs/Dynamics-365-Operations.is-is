---
title: Pöntun lofað
description: Í þessu efnisatriði er að finna upplýsingar um lofaðar pantanir. Pöntun lofað hjálpar þér lofa áreiðanlegum afhendingartíma til viðskiptavina þinna og gefur þér sveigjanleika þannig að þú getur staðið við þessar dagsetningar.
author: ShylaThompson
manager: tfehr
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesATP, SalesAvailableDlvDates
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 193933
ms.assetid: 676fc53a-fa25-4688-9f26-1005316763b8
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ccb7ef432553c0516eb49013eaad68dd21bf752c
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/17/2020
ms.locfileid: "3270028"
---
# <a name="order-promising"></a>Pöntun lofað

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er að finna upplýsingar um lofaðar pantanir. Pöntun lofað hjálpar þér lofa áreiðanlegum afhendingartíma til viðskiptavina þinna og gefur þér sveigjanleika þannig að þú getur staðið við þessar dagsetningar.

Pöntun lofað reiknar fyrstu sendingar- og innhreyfingardagsetningu, og er byggð á stýringaraðgerð afhendingardags og flutningsdaga. Hægt er að velja á milli fjögurra stýringaraðferða afhendingardags

-   **Afhendingartími sölu** – afhendingartími sölu er tíminn milli stofnunar sölupöntunarinnar og sendingu vara. Útreikningur afhendingardags er á grundvelli sjálfgefinn fjölda daga, og tekur ekki tillit til birgðastöðu, , þekktrar eftirspurnar eða áætlað framboð.
-   **ATP (tiltækt-til-loforðs)** – ATP er magn vöru sem er tiltækur og hægt er að lofa viðskiptavini á tiltekinni dagsetningu. ATP útreikningur felur í sér óstaðfestar birgðir, afhendingartími , áætlaðar innhreyfingar og úthreyfingar.
-   **ATP + mörk úthreyfinga**, sendingardagsetning er sú sama og dagsetning sem er tiltækt-til-loforðs (ATP) auk marka úthreyfinga fyrir vöruna. Mörk úthreyfinga er sá tími sem þarf að undirbúa þær vörur sem á að senda.
-   **Ctp-Afhendingargetu (óhætt að lofa)**– Framboð er reiknað í gegnum niðurbrot.

## <a name="atp-calculations"></a>ATP útreikninguar
ATP-magn er reiknað út með því að nota aðferðarinnar “uppsafnað ATP með framsýni”. Helsti kostur þessa ATP reikniaðferðin er að hún getur meðhöndlað tilvik þar sem heildartala úthreyfinga á meðal innhreyfinga er meira en síðasta innhreyfing (til dæmis þegar verður að nota magn úr eldri innhreyfingu til að uppfylla kröfu). Útreikningsaðferð "uppsafnað ATP með framsýni" inniheldur allar úthreyfingar þar til uppsafnað magn til innhreyfingar er orðin meiri en uppsafnað magn til úthreyfingar. Þar af leiðandi metur ATP reikniaðferðin hvort hægt er að nota sumt magn úr eldri tímabilum í seinni tímabilum.  

Atp-magn er óráðstafað birgðajafnvægi í fyrsta tímabilinu. Yfirleitt er hún er reiknuð fyrir hvert tímabil þar sem innhreyfing er áætluð. Forritið reiknar út ATP-tímabilið í dögum, og reiknar gildandi dagsetningu sem fyrstu dagsetninguna fyrir ATP-magn. Í fyrsta tímabilinu inniheldur ATP birgðir á lager mínus pantanir viðskiptavina sem eru á gjalddaga eða komnir fram yfir hann.  

ATP er reiknað út með því að nota eftirfarandi formúlu:  

ATP = ATP fyrir undangengið tímabil + innhreyfingarnar fyrir gildandi tímabil - úthreyfingarnar fyrir gildandi tímabil - magn netúthreyfinga fyrir hvert tímabil í framtíðinni þar til að tímabilinu þegar heild innhreyfinga fyrir öll tímabil í framtíðinni, upp að og með framtíðartímabilinu, er umfram heild úthreyfinga, upp að og með framtíðartímabilinu.  

Taktu eftir að ATP-útreikningurinn inniheldur ekki upplýsingar um lokadag og fram yfir ATP-tímamörkin sem kerfið gerir ráð fyrir þegar hægt er að lofa einhverju magni.

Þegar það eru engar innhreyfingar eða úthreyfingar að athuga, er ATP-magnið fyrir eftirfarandi dagsetningar það sama og ATP-magnið sem var reiknað út síðast.  

Ef að allar víddirnar sem eru notaðar fyrir vöru eru ekki gefnar upp þegar athugun ATP er lokið, gætu þær enn verið tilgreindar á innhreyfingum og úthreyfingum. Í því tilfelli, í ATP-útreikningi, verður að leggja saman innhreyfingarnar og úthreyfingarnar í fyrirliggjandi víddir til að draga úr fjölda innhreyfinga- og úthreyfingalína sem notaður eru í ATP-útreikningi.  

Atp-magnið sem er sýnt er alltaf meira en eða jafnt og 0 (núll). Ef útreikningur skilar neikvæðu ATP-magni (til dæmis ef að meira magn en tiltæku magni hafði verið lofað áður), stillir magnið sjálfkrafa stillt á 0.

### <a name="example"></a>Dæmi

Í **atp-tímamörk eftirspurnar afturábak** svæði stýrir hversu langt aftur í tíma á að leita að frestuðum eftirspurnarpöntunum eða birgðaúthreyfingum. Í **atp-tímamörk eftirspurnar afturábak** svæði stýrir hversu langt aftur í tíma á að leita að frestuðum birgðapöntunum eða innhreyfingum birgða. Til dæmis, ef pantanir eru seinkaðar aðeins sjö dögum ætti að fara í atp-útreikningi, bæði svæðin ætti að stilla sem **7**.  

Reitirnir **ATP mótfærður tími seinkaðrar eftirspurnar** og **ATP mótfærður tími seinkaðs framboðs** stjórna þegar seinkaðar eftirspurn eða seinkað framboð eru teknar með í atp-útreikningi. Til dæmis, ef seinkuð framboð og eftirspurn ætti að fara í atp-útreikning daginn eftir daginn á morgun ætti báðir reitir að vera stillt á **2**. Gildið **2** þýðir að magn af vöru á seinkuðum innkaupapöntun sem ætti að hafa í huga í útreikningi ATP verður að álíta tiltæk tveimur dögum eftir núgildandi dagsetningu.  

Fyrir Eftirfarandi dæmi er **7** færð inn í á **atp-tímamörk eftirspurnar afturábak** og **atp-tímamörk framboðs afturábak** svæði, og **1** er færð inn í á **ATP mótfærður tími seinkaðrar eftirspurnar** og **ATP mótfærður tími seinkaðs framboðs** svæði.  

Enn hefur ekki verið móttekin innkaupapöntun fyrir 200 stykki af vöru sem á að hafa verið mótteknar fyrir þremur dögum. Þess vegna sölupöntunarlínu fyrir 75 stykki á sömu afurð sem á að hafa verið sendar gær hefur ekki verið sent.  

Viðskiptavinur hringir og vill panta 150 stykki af sömu afurð. Þegar framboð afurðar er athuguð sérðu aðra innkaupapöntun upp á 100 stykki af sömu afurðar sem á að afhenda 10 dögum síðar.  

Stofna sölupöntunarlínu fyrir afurðina og færa inn **150** sem magn.  

Þar sem stýring fyrir afhendingardagsetningu er aðferðin ATP , eru ATP gögnin reiknuð til að finna fyrstu hugsanlegu sendingardagsetningu. Byggt á stillingum, er tekið tillit til seinkaðar innkaupapöntunar og sölupöntunar, og atp-magnið sem fæst út úr þessu fyrir gildandi dagsetningu er 0. Á Morgun, þegar búist er við að seinkaðar innkaupapöntun sé móttekin, er atp-magnið reiknað sem meira en 0 (í þessu tilfelli er hann reiknaður sem 125). Hins vegar 10 dögum frá núna, þegar viðbótar innkaupapöntun upp á 100 stykki er búist við að vera móttekin, verður atp-magn meira en 150.  

Þess vegna sendingardagsetningin er stillt á 10 daga frá núna, samkvæmt atp-útreikningi. Þess vegna er viðskiptavin sem bað um magnið sagt að hægt er að afhenda 10 dögum frá nú.



