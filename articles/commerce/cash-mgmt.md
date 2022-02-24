---
title: Endurbætur á reiðufjárstjórnun
description: Þetta efnisatriði útskýrir endurbætur á reiðufjárstjórnun á sölustað fyrir Dynamics 365 Commerce.
author: anpurush
manager: AnnBe
ms.date: 05/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-21
ms.dyn365.ops.version: ''
ms.openlocfilehash: 0c561c39dfcbfa739c5a22394c05191e7f9bc107
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413124"
---
# <a name="cash-management-improvements"></a>Endurbætur á reiðufjárstjórnun

[!include [banner](includes/banner.md)]


Reiðufjárstjórnun er lykilvirkni fyrir söluaðila í sjálfum verslununum. Söluaðilar vilja að verslanir þeirra séu með kerfi sem auðveldar að bjóða upp á rekjanleika og ábyrgð á reiðufé og færslu þess milli mismunandi afgreiðslukassa og gjaldkera í verslun. Þeir verða að geta afstemmt allan mismun og ákvarðað ábyrgð.


Microsoft Dynamics 365 Commerce er með möguleikann á reiðufjárstjórnun í forriti sölustaðar (POS). Hinsvegar, í útgáfum Retail sem eru eldri en útgáfa 10.0.3, er virkni reiðufjárstjórnunar ekki nægjanlega góð til að bjóða upp á fullan rekjanleika á færslu reiðufjár í verslunum. Þótt söluaðilar geti afstemmt reiðuféð fyrir verslun, geta þeir ekki ákvarðað nákvæmlega ábyrgð í tilfellum þar sem reiðufé stemmir ekki.


Í Retail, útgáfu 10.0.3 og síðar, fá söluaðilar rekjanleika fyrir meðhöndlun á reiðufé. Sem hluti af þessum reikjanleika, geta söluaðilar skilgreint öryggishólf, gert tvíhliða peningagreiðslur og afstemmt færslur reiðufjárstjórnunar.

## <a name="set-up-traceability-and-define-safes"></a>Setja upp rekjanleika og skilgreina öryggishólf

Til að setja upp nýja virkni reiðufjárstjórnunar skal fylgja þessum skrefum til að skilgreina virkniregluna fyrir verslanir.

1. Opnið **Retail og Commerce \> Uppsetning rásar \> Uppsetning sölustaðar \> Forstillingar sölustaðar \> Virknireglur** og veljið virknireglu sem tengd er við verslanirnar sem á að gera endurbætur á fyrir tiltæka reiðufjárstjórnun.
2. Í flýtiflipanum **Virknir** fyrir virknireglu, undir **Ítarleg reiðufjárstjórnun**, skal stilla valkostinn **Virkja rekjanleika reiðufjár** á **Já**.
3. Til að setja upp öryggishólf skal opna **Retail og Commerce \> Verslanir \> Smásöluverslanir \> Allar smásöluverslanir** og velja verslun.
4. Á síðunni **Verslanir**, í aðgerðarúðunni, í flipanum **Setja upp**, í flokknum **Setja upp**, skal velja **Öryggishólf**. Með því að nota þennan valkost geturðu skilgreint og viðhaldið mörgum öryggishólfum fyrir verslun.
4. Áður en hægt er að nota virknina verðurðu að keyra vinnslu dreifingaráætlunarinnar **1070 Stilling rásar** til að samstilla þessar skilgreiningar við gagnagrunn rásar.

## <a name="additional-cash-management-changes"></a>Viðbótarbreytingar á reiðufjárstjórnun

Í smásöluútgáfu 10.0.3 og síðar eru einnig boðið upp á eftirfarandi aðgerðir sem tengjast peningagreiðslum:

- Notandi sem er beðinn um að „gefa upp upphafsupphæð“ verður að færa inn uppruna reiðufjár. Notandinn getur leitað að tiltækum öryggishólfum sem eru skilgreind í versluninni og valið öryggishólfið sem reiðuféð er tekið úr svo hægt sé að setja það í afgreiðslukassann.
- Notandi sem notar aðgerðina „skiptimynt fjarlægð“ er beðinn um að velja, úr lista með opinni „skiptimyntafærslu“, færsluna sem aðgerðin er notuð fyrir. Ef samsvarandi skiptimyntafærsla er ekki til í kerfinu getur notandinn búið til ótengda aðgerð fyrir fjarlægingu á skiptimynt.
- Aðgerð „skiptimyntafærslu“ biður notanda um að velja, úr lista með opnum færslum fyrir „skiptimynt fjarlægð“, færsluna sem aðgerð skiptimyntafærslu er notuð fyrir. Ef samsvarandi fjarlæging skiptimyntar er ekki til í kerfinu getur notandinn búið til ótengda aðgerð fyrir skiptimyntafærslu.
- Notandi sem gerir „peningaflutning í öryggisskáp“ er beðinn um að velja öryggishólfið sem á að flytja peningana í.
- Fyrir öryggishólf sem eru skilgreind í verslun geta notendur stjórnað aðgerðum á borð við að gefa upp upphafsupphæðina, gera skiptimyntafærslu, fjarlægja skiptimynt og flytja peninga í banka.
- Fyrir notendur sem eru með viðeigandi réttindi notanda, aðgerðirnar „stjórna vöktum“ sýna peningastöður á vöktum sem eru virkar, frestaðar og lokað blint.
- Til að afstemma peningagreiðslur innan vaktar eða fyrir margar vaktir skal velja vaktina sem á að afstemma og síðan velja **Afstemma**. Yfirlitið sem opnast sýnir listann yfir afstemmdar og óafstemmdar færslur á aðskildum flipum. Úr þessu yfirliti geta notendur annaðhvort valið óafstemmdar færslur og afstemmt þær, eða valið fyrri afstemmdar færslur og óafstemmt þær.
- Við afstemmingu, ef valin færsla stemmir ekki, verður notandinn að færa inn lýsingu á því af hverju afstemmingin stemmir ekki. Notendur geta valið staka færslu og afstemmt hana með viðeigandi lýsing á ástæðu þess eftir þörfum.
- Notendur geta haldið áfram að afstemma og óafstemma færslur þar til vaktinni er lokið. Eftir að vakt er lokað er ekki hægt að afstemma færslurnar.
- Þegar notandi velur að loka vakt, staðfestir Commerce að engar óafstemmdar færslur reiðufjárstjórnunar séu til staðar á vaktinni. Notendur geta ekki lokað vakt ef óafstemmdar færslur eru til staðar.
