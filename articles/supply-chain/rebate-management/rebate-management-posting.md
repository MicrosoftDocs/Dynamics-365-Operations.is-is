---
title: Uppsetning bókunar fyrir stjórnun eftirágreidds afsláttar
description: Þessi grein lýsir því hvernig á að setja upp færslusnið. Bókunarreglur eru notaðar til að ákvarða bókunarfærslur fyrir útreikningslínur í stjórnun eftirágreidds afsláttar.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 7a519b7153b307bf7d8cc9093572ca2711432970
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8873580"
---
# <a name="rebate-management-posting-setup"></a>Uppsetning bókunar fyrir stjórnun eftirágreidds afsláttar

[!include [banner](../includes/banner.md)]

Bókunarreglur í stjórnun eftirágreidds afsláttar eru notaðar til að ákvarða bókunarfærslur fyrir útreikningslínur í stjórnun eftirágreidds afsláttar. Þegar bókunarregla er valin í tilboðshausnum á hún við um allar tilboðslínur.

Þessi eiginleiki virkar á milli fyrirtækja (lögaðila). Hægt er að tilgreina fyrirtækið sem úthlutunum verður safnað í og kröfur greiddar frá. Einnig er hægt að stilla mismunandi debetlykla úthlutunar og kreditlykla afskriftar fyrir hvert fyrirtæki upprunabókunar.

Til að setja upp bókunarreglur í stjórnun eftirágreidds afsláttar fyrir viðskiptavini og lánardrottna skal fara í **Stjórnun eftirágreidds afsláttar \> Uppsetning bókunar fyrir stjórnun eftirágreidds afsláttar \> Bókunarreglur fyrir stjórnun eftirágreidds afsláttar**. Síðan **Bókunarreglur fyrir stjórnun eftirágreidds afsláttar** inniheldur listasvæði sem sýnir allar fyrirliggjandi reglur. Hægt er að nota hnappana í aðgerðarúðunni til að bæta sniðmátum við listann eða fjarlægja þau.

Hlutarnir sem eftir eru af þessari grein lýsa því hvernig á að nota tiltæka reiti þegar þú býrð til eða breytir prófíl.

## <a name="posting-profile-header"></a>Haus bókunarreglu

Eftirfarandi tafla lýsir stillingunum sem eru í boði í haushluta hverrar bókunarreglu fyrir stjórnun eftirágreidds afsláttar.

| Svæði | lýsing |
|---|---|
| Bókunarregla |  Slá inn einkvæmt heiti fyrir forstillinguna. |
| lýsing | Færið inn lýsingu á reglunni. |
| Kerfiseining | Veljið eininguna sem eftirágreiddir afslættir og afnotagreiðslur prófílsins eru tengd við (*Viðskiptavinur* eða *Lánardrottinn*). |
| Gerð | Veljið tegund reglu (*Eftirágreiddur afsláttur* eða *Afnotagreiðsla*). |
| Greiðslugerð | <p>Þessi reitur ákvarðar sniðið á úttaki bókaðs eftirágreidds afsláttar.<p><p>Þegar reiturinn **Gerð** er stilltur á *Eftirágreiddur afsláttur* eru eftirfarandi gildi í boði:</p><ul><li>*Greiða með viðskiptaskuldum* – Þegar eftirágreiddur afsláttur er bókaður verður lánardrottnareikningur fyrir lánardrottin greiðslunnar sem er settur upp í viðskiptavini eftirágreidds afsláttar stofnaður. Þegar eftirágreiddur afsláttur lánardrottins er bókaður verður lánardrottnareikningur fyrir lánardrottnalykil eftirágreidds afsláttar stofnaður.</li><li>*Frádráttur viðskiptavinar* – Þegar eftirágreiddur afsláttur er bókaður verður frádráttarbók viðskiptavinar fyrir viðskiptavin eftirágreidds afsláttar stofnuð.</li><li>*Skattleggja frádrátt viðskiptavinareiknings* – Þegar eftirágreiddur afsláttur er bókaður verður stofnaður reikningur með frjálsum texta fyrir viðskiptavin eftirágreidds afsláttar.</li><li>*Kostnaður við vörumerki* – Þegar eftirágreiddur afsláttur er bókaður verður frádráttarbók viðskiptavinar fyrir viðskiptavin eftirágreidds afsláttar stofnuð.</li><li>*Skýrslugjöf* – Þegar eftirágreiddur afsláttur er bókaður verður frádráttarbók viðskiptavinar fyrir viðskiptavin eftirágreidds afsláttar stofnuð.</li></ul><p>Þegar reiturinn **Gerð** er stilltur á *Afnotagreiðsla* eru eftirfarandi gildi í boði:</p><ul><li>*Greiða með viðskiptaskuldum* – Þegar eftirágreiddur afsláttur er bókaður verður lánardrottnareikningur fyrir lánardrottnalykil eftirágreidds afsláttar stofnaður.</li><li>*Skýrslugjöf* – Þegar eftirágreiddur afsláttur er bókaður verður lánardrottnareikningur fyrir lánardrottnalykil eftirágreidds afsláttar stofnaður.</li></ul><p>Frekari upplýsingar eru í hlutanum [Greiðslugerðir](#payment-types) sem kemur í kjölfarið. |
| Fyrirt.   | Veljið fyrirtækið (lögaðilann) sem úthlutunum verður safnað í og kröfur greiddar frá. |

### <a name="payment-types"></a>Greiðslugerðir

Í eftirfarandi töflu er samantekt á því hvernig mismunandi stillingar á reitnum **Greiðslugerð** hafa áhrif á hvar greiðslur eru bókaðar. Hægt er að bóka greiðslur á viðskiptavinalykli, lánardrottnalykli eða greiðslulykli eftir því hver markfærslan og gerð eftirágreidds afsláttar er.

| Greiðslugerð | Gerð markfærslu | Gerð eftirágreidds afsláttar | Greiðsla á (reikningslykil) |
|---|---|---|---|
| Greiða með viðskiptaskuldum | Reikningabók lánardrottins | Eftirágreiddur afsláttur viðskiptavinar | Lánardrottnalykill vegna greiðslu viðskiptavinar |
| Greiða með viðskiptaskuldum | Reikningabók lánardrottins | Afnotagreiðsla viðskiptavinar | Lykill lánardrottins |
| Greiða með viðskiptaskuldum | Reikningabók lánardrottins | Eftirágreiddur afsláttur lánardrottins | Lykill lánardrottins |
| Frádráttur viðskiptavinar | Dagleg færslubók | Eftirágreiddur afsláttur viðskiptavinar | Viðskiptavinalykill |
| Skattleggja frádrátt viðskiptavinareiknings | Textareikningur | Eftirágreiddur afsláttur viðskiptavinar | Viðskiptavinalykill |
| Kostnaður við vörumerki | Dagleg færslubók | Eftirágreiddur afsláttur viðskiptavinar | Viðskiptavinalykill |
| Skýrslugerð | Dagleg færslubók | Eftirágreiddur afsláttur viðskiptavinar | Viðskiptavinalykill |
| Skýrslugerð | Reikningabók lánardrottins | Afnotagreiðsla viðskiptavinar | Lykill lánardrottins |
| Skýrslugerð | Reikningabók lánardrottins | Eftirágreiddur afsláttur lánardrottins | Lykill lánardrottins |

> [!NOTE]
> Hafið eftirfarandi punkta í huga þegar [Tilboð fyrir stjórnun eftirágreidds afsláttar](rebate-management-deals.md) er sett upp:
>
> - Fyrir tilboð þar sem reiturinn **Afstemma eftir** er stilltur á *Tilboð* er ekki hægt að nota kvikan tilboðslykil við bókun. Þú verður að nota tilgreindan reikning viðskiptamanns eða lánardrottins.
> - Fyrir tilboð þar sem reiturinn **Afstemma eftir** er stilltur á *Lína* er hægt að nota bókunarreglu sem jafnast inn á kvikan tilboðslykil í tilboðslínunni vegna þess að viðskiptavinurinn eða lánardrottinn er stilltur fyrir hverja tilboðslínu.

## <a name="posting-fasttab"></a>Flýtiflipinn Bókun

Eftirfarandi tafla lýsir reitunum sem eru tiltækir í flýtiflipanum **Bókun** í hverri bókunarreglu fyrir stjórnun eftirágreidds afsláttar.

| Svæði | lýsing |
|---|---|
| Kredit gerð | Veljið hvort kreditfæra eigi fjárhagslykil eða viðskiptavin. Ef reiturinn **Greiðslugerð** í hausnum er stilltur á *Skattleggja frádrátt viðskiptavinareiknings* verður þessi reitur stilltur á *Fjárhagslykill*. Fyrir eftirágreidda afslætti lánardrottins er þessi reitur stilltur á *Fjárhagslykill*. |
| Kreditreikningur | Veldu lykilinn þar sem kreditupphæðir eru bókaðar á þegar úthlutanir á eftirágreiddum afslætti fara fram. Þessi lykill verður einnig notaður sem mótlykill þegar eftirágreiddur afsláttur er bókaður til að kreditfæra viðskiptavininn eða debetfæra lánardrottin. |
| Nafn færslubókar<br>(Í hlutanum **Úthlutun**) | Veljið heiti færslubókar sem á að nota til að skrá bókaða úthlutun. |
| Gerð | Veljið hvort eigi að bóka eftirágreiddan afslátt á fjárhagslykil, eða viðskiptavin eða lánardrottin. Ef reiturinn **Greiðslugerð** í hausnum er stilltur á *Skattleggja frádrátt viðskiptavinareiknings* verður þessi reitur stilltur á *Viðskiptavinur/Lánardrottinn*. |
| Nota uppruna lykils | <p>Veljið eitt af eftirfarandi gildum:</p><ul><li>*Fastur lykill* – Ef þetta gildi er valið þarf að tilgreina lykil í reitnum **Lykill eftirágreidds afsláttar**.</li><li>*Lykill tilboðslínu* – Notið viðskiptavina- eða lánardrottnalykil sem er tilgreindur í línu eftirágreidds afsláttar. Þetta gildi er aðeins hægt að velja fyrir tilboð þar sem reiturinn **Afstemma eftir** er stilltur á *Lína* og tilboðslínurnar þar sem reiturinn **Kóði lykils** er stilltur á *Tafla*. Það gildir ekki um bókunarreglur vegna afnotagreiðslu viðskiptavinar eða eftirágreiddra afslátta lánardrottins sem byggja á sölupöntunum.</li></ul> |
| Lykill eftirágreidds afsláttar | Lykillinn þar sem raunverulegur kostnaður eftirágreiddra afslátta verður bókaður. |
| Nafn færslubókar<br>(Í reitahópnum **Stjórnun eftirágreidds afsláttar**) | Veljið heiti færslubókar sem á að nota til að bóka kreditnótu fyrir upphæð eftirágreidds afsláttar fyrir viðskiptavininn eða lánardrottinn. Þessi reitur er ekki í boði þegar reiturinn **Greiðslugerð** í hausnum er stilltur á *Skattleggja frádrátt viðskiptavinareiknings*. Fyrir eftirágreidda afslætti viðskiptavinar verða færslubókarheiti af færslubókargerðinni *Daglegt* í boði. Fyrir afnotagreiðslur viðskiptavinar og eftirágreidda afslætti lánardrottins verða færslubókarheiti af færslubókargerðinni *Skráning reiknings frá lánardrottni* í boði. |
| VSK-flokkur vöru | Tilgreinið hvort eftirágreiddur afsláttur sé skattskyldur. |
| Nafn færslubókar<br>(Í reitahópnum **Afskrifa**) | Ef eftirágreiddur afsláttur sem er bókaður jafngildir ekki úthlutuninni verður hægt að afskrifa mismuninn. Veljið heiti færslubókar sem á að nota til að skrá bókaða afskrift. |

## <a name="posting-by-company-fasttab"></a>Flýtiflipi bókunar eftir fyrirtæki

Flýtiflipinn **Bókun eftir fyrirtæki** í hverri bókunarreglu eftirágreidds afsláttar gerir kleift að tilgreina bókunarlykilinn sem er notaður af hverju fyrirtæki (lögaðila) í hnitanetinu.

Notið hnappana á tækjastikunni til að bæta fyrirtækjum við hnitanetið eða til að fjarlægja þau. Í hvert sinn sem línu er bætt við hnitanetið skal nota reitinn **Fyrirtæki** til að tilgreina lögaðilann fyrir þá línu. Reiturinn **Heiti** er þá stilltur sjálfkrafa.

Veljið línuna fyrir hvert fyrirtæki og færið svo inn eftirfarandi upplýsingar með því að nota reitina fyrir neðan hnitanetið:

- **Debetgerð** – Veljið hvort skuldfæra eigi fjárhagslykil eða lánardrottin. Fyrir eftirágreidda afslætti viðskiptavinar er þessi reitur stilltur á *Fjárhagslykil*.
- **Debetlykill** – Færið inn lykilinn sem debetupphæðin er bókuð á þegar úthlutanir eftirágreidds afsláttar fara fram.
- **Aðallykill** – Veljið aðallykil fyrir afskriftir.
