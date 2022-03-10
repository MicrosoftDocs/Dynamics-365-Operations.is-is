---
title: Færibreytur fyrir stjórnun eftirágreidds afsláttar
description: Þetta efnisatriði lýsir færibreytusíðu fyrir stjórnun eftirágreidds afsláttar. Þessi síða inniheldur stillingar sem hafa áhrif á bókanir, stöðuuppfærslur, númeraraðir og annars konar hegðun.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 0665ce41233308c814a514fccf3b73e20de64098
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7576689"
---
# <a name="rebate-management-parameters"></a>Færibreytur fyrir stjórnun eftirágreidds afsláttar

[!include [banner](../includes/banner.md)]

Síðan **Færibreytur fyrir stjórnun eftirágreidds afsláttar** er notuð til að skilgreina stillingar sem eiga við í einingunni **Stjórnun eftirágreidds afsláttar**. Þessar stillingar hafa áhrif á bókanir, stöðuuppfærslur, númeraraðir og annars konar hegðun. Uppsetningu þessarar síðu er deilt á meðal allra lögaðila og notendur sem eru með viðeigandi öryggisheimildir geta breytt henni.

Til að opna síðuna **Færibreytur fyrir stjórnun eftirágreidds afsláttar** skal fara í **Stjórnun eftirágreidds afsláttar \> Uppsetning \> Færibreytur fyrir stjórnun eftirágreidds afsláttar**. Því næst skal stilla reitina eins og lýst er í eftirfarandi undirköflum.

## <a name="rebate-management-tab"></a>Flipi fyrir stjórnun eftirágreidds afsláttar

Eftirfarandi tafla lýsir reitunum sem eru í boði í flipanum **Stjórnun eftirágreidds afsláttar** á síðunni **Færibreytur fyrir stjórnun eftirágreidds afsláttar**.

| Svæði | lýsing |
|---|---|
| Sjálfgefin staða | Veljið sjálfgefna stöðu fyrir öll ný tilboð. Til að skilgreina safn af stöðugildum sem hægt er að velja skal nota síðuna [**Stöður eftirágreidds afsláttar**](rebate-statuses.md). |
| Úrvinnsla eftir vídd | Veljið hvort vinna eigi úr færslum úthlutunar, eftirágreidds afsláttar og afskriftum eftir fjárhagsvídd. Þegar kveikt er á þessum valkosti notar kerfið fjárhagsvíddir úr upprunafærslunum í markfærslunum. |
| Athuga hvort áður hafi verið bókað | <p>Veljið hegðun kerfis ef unnið er oftar en einu sinni úr færslum eftirágreidds afsláttar fyrir sama tímabilið:</p><ul><li>**Viðvörun** – Kerfið gerir notendum kleift að hnekkja upprunalegum færslulínum, en viðvörun er sýnd.</li><li>**Villa** – Kerfið kemur í veg fyrir að notendur geti hnekkt upprunalegum færslulínum og villuboð eru sýnd. |
| Bókar sjálfkrafa færslubækur | Veljið hvort kerfið eigi að bóka framlagðar færslubækur sjálfkrafa. Þessar færslubækur innihalda daglegar færslubækur sem eru notaðar fyrir úthlutanir og frádrætti viðskiptavinar og einnig skattreikningabækur lánardrottins. |
| Bóka reikninga með frjálsum texta sjálfkrafa | Veljið hvort kerfið eigi að bóka reikninga með frjálsum texta sjálfkrafa. Þessi valkostur á aðeins við um reikninga með frjálsum texta þar sem greiðslugerðin er stillt á *Skattleggja frádrátt viðskiptavinareiknings*. |
| Tilvísun í vörupöntun eftirágreidds afsláttar | Veljið tilvísun eftirágreidds afsláttar til að nota í sölu- og innkaupapöntunum sem eru búnar til í ferli eftirágreidds afsláttar (*Ekkert*, *Tilboð fyrir stjórnun eftirágreidds afsláttar*, *Númer fyrir stjórnun eftirágreidds afsláttar*, *Færslunúmer eftirágreidds afsláttar* eða *Athugasemdir skjals*). |
| Nota kröfuferli | <p>Stillið þennan valkost á *Já* til að nota kröfuferli. Þannig er hægt að merkja færslur sem stjórnun eftirágreidds afsláttar stofnar sem annaðhvort innheimtar eða óinnheimtar og síðan bóka aðeins innheimtar færslur.</p><p>Til dæmis eru eftirágreiddir afslættir reiknaðir fyrir færslur yfir heilan mánuð, en viðskiptavinurinn hefur skilið tvo daga eftir óinnheimta. Í þessu tilviki verða óinnheimtar færslur stofnaðar aftur næst þegar aðgerðin *Úrvinnsla* er keyrð fyrir næsta tímabil.</p><p>Ef þessi valkostur er stilltur á *Nei* eru allar kröfufærslur bókaðar.</p> |
| Hafa með pöntunargerð færslubókar | Fyrir tilboð eða tilboðslínur þar sem færslugerðin er stillt á *Pöntun* stýrir þessi valkostur því hvort sölupöntun af gerðinni *Færslubók* eigi að vera með. Það eykur sveigjanleika ef þessar gerðir pantana eru notaðir í aðstæðum þar sem ekki á að nota eftirágreiddan afslátt. |

## <a name="number-sequences-tab"></a>Flipinn Númeraraðir

Notið flipann **Númeraraðir** á síðunni **Færibreytur fyrir stjórnun eftirágreidds afsláttar** til að úthluta kóðum númeraraðar á mismunandi númeraraðir sem stjórnun eftirágreidds afsláttar notar. Eftirfarandi tafla lýsir tilgangi hverrar númeraraðar. Nánari upplýsingar um númeraraðir er að finna í [Yfirlit númeraraða](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md) og í tengdu efnisatriði.

| Tilvísun | lýsing |
|---|---|
| Tilboð fyrir stjórnun eftirágreidds afsláttar | Númeraröðin úthlutar hverju tilboð eftirágreidds afsláttar gildi einkvæms lykils. Þessi lykill er notaður þegar tilboð eru búin til. |
| Númer fyrir stjórnun eftirágreidds afsláttar | Númeraröðin úthlutar hverjum eftirágreiddum afslætti einkvæmu gildi lykils. Þessi lykill er notaður til að auðkenna vensl eftirágreidds afsláttar. |
| Færslunúmer eftirágreidds afsláttar | Númeraröðin úthlutar hverri færslu eftirágreidds afsláttar einkvæmu gildi lykils. Þessi lykill er notaður til að auðkenna færslur eftirágreidds afsláttar. |
| Skattareikningur | Númeraröðin úthlutar hverjum reikningi eftirágreidds afsláttar einkvæmu gildi lykils. Þessi lykill er notaður þegar færslubækur fyrir eftirágreiddan afslátt eru bókaðar sjálfkrafa. |

## <a name="feature-visibility-tab"></a>Flipi fyrir sýnileiki eiginleika

Stjórnun eftirágreidds afsláttar bætir eiginleikum (reitum og aðgerðum) við nokkrar algengar síður í Microsoft Dynamics 365 Supply Chain Management. Þessar síður innihalda síður sem tengjast sölupöntunum og sölutilboðum. Ef verið er að nota stjórnun eftirágreidds afsláttar verður að gera þessa eiginleika sýnilega allstaðar áður en hægt er að nota þá. Ef stjórnun eftirágreidds afsláttar er ekki notaður er hægt að fela eiginleikana svo þeir þvælist ekki fyrir.

Í flipanum **Sýnileiki eiginleika** á síðunni **Færibreytur eftirágreidds afsláttar** skal stilla valkostinn **Virkja** á *Já* til að gera eiginleika fyrir stjórnun eftirágreidds afsláttar sýnilega þar sem þeir eru í boði. Stillið það á *Nei* til að fela eiginleikana á algengum síðum utan einingarinnar **Stjórnun endurgreidds afsláttar** . Hins vegar, jafnvel þegar valkosturinn er stilltur á *Nei*, mun sjálf einingin, þ.m.t. síðan **Færibreytur eftirágreidds afsláttar**, vera áfram tiltæk notendum sem eru með tilheyrandi aðgangsheimildir.
