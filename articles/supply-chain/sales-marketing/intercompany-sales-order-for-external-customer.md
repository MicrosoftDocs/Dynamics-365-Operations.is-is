---
title: Stofna og reikningsfæra samstæðusölupöntun fyrir ytri viðskiptavin
description: Þetta efnisatriði útskýrir hvernig á að stofna og reikningsfæra samstæðusölupöntun fyrir ytri viðskiptavin
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 72273a125da2e6c4a2fc16b449cd5077f3d767df
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548326"
---
# <a name="create-and-invoice-an-intercompany-sales-order-for-an-external-customer"></a>Stofna og reikningsfæra samstæðusölupöntun fyrir ytri viðskiptavin

[!include [banner](../../includes/banner.md)]

Hægt er að nota samstæðuviðskipti til að skrá sölu á vöru úr einum lögaðila við annan lögaðila sem er í sömu samstæðu.

Þegar stofnuð er upprunalega sölupöntun geturðu sjálfkrafa stofnað samstæðuinnkaupapöntun fyrir samstæðulánardrottinn. Þetta stofnar sjálfkrafa stofna sölupöntun innan samstæðu hjá lögaðila samstæðulánardrottins.

Eftirfarandi mynd sýnir flæði yfir færslurnar þegar sölupöntun er stofnuð fyrir ytri viðskiptavin, en afurðin verður að vera pöntuð frá mismunandi lögaðila í fyrirtækinu þínu áður en þú getur afhent viðskiptavininum afurðina. Í þessu tilfelli er samstæðuinnkaupapöntun búin til fyrir lánardrottnareikning sem sýnir hin lögaðilann. Á móti er samstæðusölupöntun stofnuð í hinum lögaðilanum fyrir reikning viðskiptavinar sem stendur fyrir lögaðila þína. Þegar samstæðuinnkaupapöntunin er reikningsfærð er reikningurinn fyrir upprunalega sölupöntun sjálfkrafa reikningsfærður, ef það er bein afhending.

![Ytra söluferli innan samstæðu](media/intercompanyexternalsalesprocess.png)

Ef notuð er bein afhending og **Fylgiseðill** er valinn í reitnum **Magn** á síðunni **Bókun reiknings**, byggir reikningur samstæðulánardrottins á innhreyfingarskjali afurðar innan samstæðu sem var bókað áður.

## <a name="prerequisites"></a>Forkröfur

Áður en þú byrjar skaltu ganga úr skugga um að eftirfarandi forsendum sé mætt til að sjálfkrafa bóka og prenta samstæðureikninga.

1. Opnið **Sölu og markaðssetning \> Viðskiptavinir \> Allir viðskiptavinir**.
1. Í aðgerðasvæðinu, á flipanum **Almennt**, skal velja **Innan samstæðu**.
1. Farið í **Innkaup og aðföng \> Lánardrottnar \> Allir lánardrottnar**.
1. Í aðgerðasvæðinu, á flipanum **Almennt**, skal velja **Innan samstæðu**.
1. Á síðunni **Innan samstæðu** fyrir annaðhvort lánardrottin eða viðskiptavin á svæðinu **Innkaupapöntunarreglur** í reitahópnum **Samstæðuinnkaupapöntun (bein afhending)** skal velja gátreitinn **Bóka reikning sjálfvirkt**.
1. Á svæðinu **Innkaupapöntunarreglur**, í reitahópnum **Upphafleg sölupöntun (bein afhending)**, skal velja gátreitinn **Bóka reikning sjálfvirkt**. Veljið þennan gátreit ef óskað er eftir að reikningurinn fyrir upphaflegu sölupöntunina prentist sjálfkrafa þegar lánardrottinsreikning innan samstæðu er bókaður.

> [!NOTE]
> Prentstillingar fyrir reikninginn eru ákveðnar eftir uppsetningunni fyrir eininguna, skjalið eða færsluna á síðunni **Uppsetning á prentstýringu**.

## <a name="create-an-original-sales-order-for-an-external-customer"></a>Stofna upprunasölupöntun fyrir ytri viðskiptavin

Gerðu þessi skref í lögaðila A. Þetta ferli samsvarar reitnum sem er merktur 1 í skýringarmynd.

1. Farðu í **Viðskiptakröfur \> Sölupantanir \> Allar sölupantanir**.
1. Á listasíðunni **Allar sölupantanir** skal stofna upprunalegu sölupöntunina. Reitagildi eru afrituð frá viðskiptavinalykill í sölupöntunina.
1. Á síðunni **Sölupöntun** skal velja **Hausyfirlit** á aðgerðasvæðinu.
1. Í flýtiflipanum **Samstæðustillingar** skal velja gátreitinn **Stofna samstæðupantanir sjálfvirkt**.
1. Ef þú vilt samstæðulánardrottinn til að afhenda vöruna beint til ytri viðskiptavinar, veljið gátreitinn **Bein afhending**.
1. Þegar lokið hefur verið við að færa inn sölupöntun skal loka síðunni **Sölupöntun**.

Samstæðuinnkaupapöntun er stofnuð sjálfkrafa fyrir allar vörur sem úthlutað er á samstæðulánardrottinn og svo er samstæðusölupöntun stofnuð. Upplýsingaskilaboð í upplýsingakladda sem tilkynna að samstæðuinnkaupapöntun og samstæðusölupöntun hafi verið stofnaðar. Skilaboðin innihalda einnig tengla á þessar pantanir. Hafi vara ekki fundist birtist rauð viðvörun sem þýðir að stofnun pöntunar hafi ekki klárast.

> [!NOTE]
> Ef þú ert að búa nokkrar pantanir í mismunandi lögaðila, og hlutir voru ekki að finna í einu af lögaðila, sköpun þess hættir, jafnvel fyrir lögaðila sem gæti uppfylla pantanir þeirra.

## <a name="invoice-an-intercompany-sales-order"></a>Reikningsfæra sölupöntun innan samstæðu

Þegar samstæðusölupöntunin er reikningsfærð er reikningurinn fyrir upprunalega samstæðuinnkaupapöntun sjálfkrafa reikningsfærður. Svo ef upprunalega sölupöntunin er bein afhending, er upprunalegrar sölupöntunar sjálfkrafa reikningsfærð.

Gerðu þessi skref í lögaðila B. Þetta ferli samsvarar reitnum sem er merktur 2 í skýringarmynd.

1. Farðu í **Viðskiptakröfur \> Sölupantanir \> Allar sölupantanir**.
1. Á listasíðunni **Allar sölupantanir** skal velja samstæðusölupantanir.
1. Á aðgerðasvæðinu skal velja flipann **Reikningur** og síðan velja **Reikningur**.
1. Veldu gátreitinn **Bókun**.
1. Veldu sölupöntunina og því næst **Í lagi**.

Reikningur viðskiptavinar fyrir samstæðusölupöntunina er sjálfkrafa bókaður í lögaðila B. Reikningur samstæðulánardrottins er þá sjálfkrafa stofnaður og bókaður í lögaðila A. Ef upprunaleg sölupöntun er sett upp sem bein afhending er reikningur viðskiptavinar stofnaður fyrir upprunalegu sölupöntunina í lögaðila A.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
