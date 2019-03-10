---
title: Skilgreina og vinna úr skiptum á skilapöntun
description: Þetta efnisatriði útskýrir hvernig skilgreina á skipti á skilum í Microsoft Dynamics 365 for Retail.
author: josaw1
manager: AnnBe
ms.date: 11/12/2018
ms.topic: index-page
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
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 45b628376a483d3d639e5c018dd93570ed8ce7af
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "302423"
---
# <a name="configure-and-process-an-exchange-on-a-return-order"></a>Skilgreina og vinna úr skiptum á skilapöntun

[!include [banner](includes/banner.md)]

Í eldri útgáfum af Microsoft Dynamics 365 for Retail var notað skjal vöruskilapöntunar í Retail headquarters við úrvinnslu á skilum sem tengdust pöntunum viðskiptavina. Hins vegar er aðeins hægt að nota skjal skilapöntunar til að vinna úr afurðum sem verið er að skila. Afurðir sem hefur verið skilað eru sýndar með neikvæðu magni á línum skilapöntunar. Aftur á móti eru sölur sýndar með jákvæðu magni. Skjal vöruskilapöntunar styður hins vegar ekki jákvætt magn. Út af þessari takmörkun studdu eldri útgáfur af Retail ekki kringumstæður þar sem skil afurða eru gerð með því að nota skjal skilapöntunar.

Hins vegar er búið að bæta við virkni sem styður kringumstæður þar sem gerð eru skipti á vöruskilapöntunum. Retail notar nú sölupöntunarskjalið í stað skjals vöruskilapöntunar til að vinna úr þess konar færslugerðum.

## <a name="configure-retail-to-support-exchanges-on-return-orders"></a>Skilgreina Retail til að styðja skipti á vöruskilapöntunum

Fylgið þessum skrefum til að skilgreina kerfið svo það styðji skipti á vöruskilapöntunum.

1. Opnið **Retail \> Uppsetning höfuðstöðva \> Færibreytur \> Smásölufæribreytur**. Á flýtiflipanum **Pantanir viðskiptavinar** skal stilla valkostinn **Vinna úr skilapöntunum eins og sölupöntunum** á **Já**.
2. Keyrið verkið **Dreifingaráætlun altækrar skilgreiningar** (**1110**).

## <a name="make-an-exchange"></a>Skipti gerð

Eftir að kerfið hefur verið skilgreint samkvæmt lýsingu í kaflanum hér á undan, heldur notandi sölustaðar áfram að velja sölupöntun eða sölureikning til að vinna úr skilum eins og í eldri útgáfum af Retail. Eftir að skilavörum er bætt við körfuna getur notandinn hins vegar bætt nýjum sölulínum við hana.

Notandi verður að skilgreina allar nauðsynlegar eigindir fyrir þessar nýju sölulínur til að geta unnið úr pöntunarlínu viðskiptavinar. Þessar eigindir fela í sér afhendingaraðferð og uppfyllingarstaðsetningu. Greiðslan sem þarf að inna af hendi fyrir færsluna verður nettó af línum vöruskilapöntunar og línum sölupöntunar. Þegar greiðsla er gerð upp fyrir færsluna verður skilapöntunin bókuð sem sölupöntunarskjal í höfuðstöðvum Retail og kerfið reikningsfærir um leið skilalínurnar.

Til að bjóða upp á aukinn sýnileika á hinum ýmsu upphæðum fyrir körfuna hefur þremur nýjum upphæðareitum verið bætt við hana. Hægt er að nota skjáhönnuðinn til að gera þessa nýju reiti tiltæka í notandaviðmóti sölustaðar.

- **Innborgun notuð** – Upphæð innborgunar sem er notuð í færslu þegar notandi velur að pöntun viðskiptavinar verði sótt. Ef engin hnekking innborgunar er til staðar, og 10% innborgun er skilgreind, er upphæðin í þessum reit 90% af heildarupphæð pöntunar viðskiptavinar.
- **Taka með upphæð** – Heildarupphæð fyrir línur þar sem afhendingarmátinn var stilltur á **Taka með** þegar pöntun viðskiptavinar var stofnuð eða breytt, eða við skipti á pöntun viðskiptavinar. Upphæðin í þessum reit inniheldur skatta og gjöld.
- **Upphæð skila** – Heildarfjöldi lína sem eru með neikvætt magn við skipti á pöntun viðskiptavinar. Upphæðin í þessum reit inniheldur skatta og gjöld.