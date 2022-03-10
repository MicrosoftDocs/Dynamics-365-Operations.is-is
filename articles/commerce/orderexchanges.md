---
title: Skilgreina og vinna úr skiptum á skilapöntun
description: Þetta efnisatriði útskýrir hvernig skilgreina á skipti á skilum í Dynamics 365 Commerce.
author: josaw1
ms.date: 07/28/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 488f6fb5af6451bc462566a9714054b49eb1a80b8264528778797f6a39647764
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6758337"
---
# <a name="configure-and-process-an-exchange-on-a-return-order"></a>Skilgreina og vinna úr skiptum á skilapöntun

[!include [banner](includes/banner.md)]

Í eldri útgáfum af Dynamics 365 Commerce var notað skjal vöruskilapöntunar í höfuðstöðvum við úrvinnslu á skilum sem tengdust pöntunum viðskiptavina. Hins vegar er aðeins hægt að nota skjal skilapöntunar til að vinna úr afurðum sem verið er að skila. Afurðir sem hefur verið skilað eru sýndar með neikvæðu magni á línum skilapöntunar. Aftur á móti eru sölur sýndar með jákvæðu magni. Skjal vöruskilapöntunar styður hins vegar ekki jákvætt magn. Vegna þessarar takmörkunar studdu eldri útgáfur af forritinu ekki atburðarásir þar sem skil afurða eru gerð með því að nota skjal skilapöntunar.

Hins vegar er búið að bæta við virkni sem styður kringumstæður þar sem gerð eru skipti á vöruskilapöntunum. Commerce notar nú sölupöntunarskjalið í stað vöruskilapöntunarskjalsins til að vinna úr þess konar færslugerðum.

## <a name="configure-commerce-to-support-exchanges-on-return-orders"></a>Skilgreina Commerce til að styðja skipti á vöruskilapöntunum

> [!NOTE]
> Í Commerce útgáfu 10.0.20 og síðari er nýr eiginleiki sem kallast „Upplifun samræmdra vinnsluferla skila á sölustað“ í boði. Ef þessi eiginleiki er virkjaður er ekki þörf á uppsetningarskrefunum hér að neðan. **Vinna úr vöruskilum sem sölupantanir** verður varanlega skilgreind stilling sem ekki verður hægt að afturkalla.

Fylgið þessum skrefum til að skilgreina kerfið svo það styðji skipti á vöruskilapöntunum (ef eiginleikinn **Upplifun samræmdra vinnsluferla skila á sölustað** hefur ekki verið virkjaður).

1. Opnið **Retail og Commerce \> Uppsetning höfuðstöðva \> færibreytur \> Færibreytur Commerce**. Á flýtiflipanum **Pantanir viðskiptavinar** skal stilla valkostinn **Vinna úr skilapöntunum eins og sölupöntunum** á **Já**.
2. Keyrið verkið **Dreifingaráætlun altækrar skilgreiningar** (**1110**).

## <a name="make-an-exchange"></a>Skipti gerð

Eftir að kerfið hefur verið skilgreint samkvæmt lýsingu í kaflanum hér á undan, heldur notandi sölustaðar áfram að velja sölupöntun eða sölureikning til að vinna úr skilum eins og í eldri útgáfum af forritinu. Eftir að skilavörum er bætt við körfuna getur notandinn hins vegar bætt nýjum sölulínum við hana.

Notandi verður að skilgreina allar nauðsynlegar eigindir fyrir þessar nýju sölulínur til að geta unnið úr pöntunarlínu viðskiptavinar. Þessar eigindir fela í sér afhendingaraðferð og uppfyllingarstaðsetningu. Greiðslan sem þarf að inna af hendi fyrir færsluna verður nettó af línum vöruskilapöntunar og línum sölupöntunar. Þegar greiðsla er gerð upp fyrir færsluna verður skilapöntunin bókuð sem sölupöntunarskjal í höfuðstöðvum og kerfið reikningsfærir um leið skilalínurnar.

Til að bjóða upp á aukinn sýnileika á hinum ýmsu upphæðum fyrir körfuna hefur þremur nýjum upphæðareitum verið bætt við hana. Hægt er að nota skjáhönnuðinn til að gera þessa nýju reiti tiltæka í notandaviðmóti sölustaðar.

- **Innborgun notuð** – Upphæð innborgunar sem er notuð í færslu þegar notandi velur að pöntun viðskiptavinar verði sótt. Ef engin hnekking innborgunar er til staðar, og 10% innborgun er skilgreind, er upphæðin í þessum reit 90% af heildarupphæð pöntunar viðskiptavinar.
- **Taka með upphæð** – Heildarupphæð fyrir línur þar sem afhendingarmátinn var stilltur á **Taka með** þegar pöntun viðskiptavinar var stofnuð eða breytt, eða við skipti á pöntun viðskiptavinar. Upphæðin í þessum reit inniheldur skatta og gjöld.
- **Upphæð skila** – Heildarfjöldi lína sem eru með neikvætt magn við skipti á pöntun viðskiptavinar. Upphæðin í þessum reit inniheldur skatta og gjöld.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
