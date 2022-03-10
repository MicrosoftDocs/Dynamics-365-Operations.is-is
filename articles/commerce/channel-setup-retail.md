---
title: Setja upp smásölurás
description: Í þessu efnisatriði er lýst hvernig eigi að stofna nýja smásölurás í Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 6a8db8bb4b42c7ad6c0c0e0c257bc03e356de7d525f524c22eab46e38c018d49
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6745407"
---
# <a name="set-up-a-retail-channel"></a>Setja upp smásölurás

[!include [banner](includes/banner.md)]

Í þessu efnisatriði er lýst hvernig eigi að stofna nýja smásölurás í Microsoft Dynamics 365 Commerce.

Dynamics 365 Commerce styður margar smásölurásir. Meðal þessara smásölurásir eru netverslanir, símaver, og smásöluverslanir (einnig kallað hefðbundnar verslanir). Hvert smásöluverslunarrás getur haft sína eigin greiðsluhætti, verðflokka, sölustað (POS) afgreiðslukassa, tekjulykla og kostnaðarlykla og starfsfólk. Setja verður upp allar þessar einingar áður en hægt er að stofna smásöluverslunarrás. 

Áður en smásölurás er búin til skaltu ganga úr skugga um að þú fylgir [forsendur rásar](channels-prerequisites.md).

## <a name="create-and-configure-a-new-retail-channel"></a>Stofna og stilla nýja smásölurás

1. Í yfirlitsglugganum ferðu í **Einingar \> Rásir \> Verslanir \> Allar smásöluverslanir**.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Í reitnum **Heiti** slærðu inn heiti fyrir nýju rásina.
1. Í svæðinu **Verslunarnúmer** skal gefa upp einkvæmt verslunarnúmer. Talan getur verið bók- eða tölustafir og að hámarki 10 stafir.
1. Í fellivallistanum **Lögaðili** skal slá inn viðeigandi lögaðila.
1. Í fellivallistanum **Vöruhús** slærðu inn viðeigandi vöruhús.
1. Í reitnum **Tímabelti verslunar** velurðu viðeigandi tímabelti.
1. Í fellilistanum **VSK-flokkur** velurðu viðeigandi VSK-flokk fyrir verslunina.
1. Í reitnum **Gjaldmiðill** velurðu viðeigandi gjaldmiðil.
1. Í reitnum **Heimilisfangabók viðskiptavina** gefurðu upp gilda aðsetursbók.
1. Í reitnum **Sjálfgefinn viðskiptavinur** gefurðu upp gildan sjálfgefinn viðskiptavin.
1. Í reitnum **Virkniregla** velurðu virknireglu ef við á.
1. Í reitinn **Forstilling tilkynningar í tölvupósti** gefurðu upp gilt tilkynningarsnið fyrir tölvupóst.
1. Í aðgerðarúðunni skal velja **Vista**.

Eftirfarandi mynd sýnir stofnun nýrrar smásölurásar.

![Ný smásölurás.](media/channel-setup-retail-1.png)

Eftirfarandi mynd sýnir dæmi um smásölurás.

![Dæmi um smásölurás.](media/channel-setup-retail-2.png)

## <a name="other-settings"></a>Aðrar stillingar

Það eru fjölmargar aðrar valkvæðar stillingar sem hægt er að stilla í hlutunum **Yfirlýsing/lokun** og **Ýmislegt**, miðað við þarfir smásöluverslunarinnar.

Að auki, sjá [Skjáupplýsingar fyrir sölustað (POS)](pos-screen-layouts.md) til að fá upplýsingar um uppsetningu á sjálfgefinni skjáuppsetningu í hlutanum **Skjáskipulag** og [Stilla og setja upp Retail vélbúnaðarstöð](retail-hardware-station-configuration-installation.md) fyrir uppsetningarupplýsingar um hlutann **Vélbúnaðarstöðvar**.

Eftirfarandi mynd sýnir dæmi um uppsetningarstillingu smásölurásar.

![Dæmi um stillingu smásölurásar.](media/channel-setup-retail-3.png)

## <a name="additional-channel-set-up"></a>Viðbótaruppsetning grunnrásar

Það eru fleiri hlutir sem þarf að setja upp fyrir rás sem er að finna í aðgerðaglugganum undir kaflanum **Setja upp**.

Viðbótarupplýsingar sem krafist er fyrir uppsetningu netrásar fela í sér uppsetningu á greiðslumáta, skilgreiningu reiðufjár, afhendingaraðferðum, tekju-/útgjaldalykli, hlutum, úthlutun uppfyllingarflokks og öryggishólfa.

Eftirfarandi mynd sýnir ýmsa viðbótaruppsetningarvalkosti smásölurásar á flipanum **Setja upp**.

![Setja upp rás.](media/channel-setup-retail-4.png)

### <a name="set-up-payment-methods"></a>Setja upp greiðsluhætti

Fylgdu þessum skrefum til að setja upp greiðslumáta fyrir hverja greiðslugerð sem er studd á þessari rás.

1. Í aðgerðaglugganum velurðu flipann **Setja upp** og velur síðan **Greiðslumátar**.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Í yfirlitsglugganum velurðu óskaðan greiðslumáta.
1. Í kaflanum **Almennt** skaltu gefa upp **Heiti aðgerðar** og stilla allar aðrar stillingar sem óskað er.
1. Stilltu allar viðbótarstillingar eins og krafist er fyrir greiðslugerð.
1. Í aðgerðarúðunni skal velja **Vista**.

Eftirfarandi mynd sýnir dæmi um greiðsluaðferð í reiðufé.

![Dæmi um greiðslumáta.](media/channel-setup-retail-5.png)

### <a name="set-up-cash-declaration"></a>Setja upp skilgreiningar reiðufjár

1. Í aðgerðaglugganum velurðu flipann **Setja upp** og velur síðan **Skilgreining reiðufjár**.
1. Í aðgerðaglugganum velurðu **Nýtt** og síðan stofnarður öll gildi **myntar** og **seðla** sem eiga við.

Eftirfarandi mynd sýnir dæmi um skilgreingingu reiðufjár.

![Uppsetning á skilgreiningu reiðufjár.](media/channel-setup-retail-6.png)

### <a name="set-up-modes-of-delivery"></a>Setja upp afhendingarmáta

Þú getur séð stillta afhendingarmáta með því að velja **Afhendingarmáta** af flipanum **Setja upp** í Aðgerðarglugganum.  

Fylgdu þessum skrefum til að breyta eða bæta við afhendingarmáta.

1. Í yfirlitsglugganum ferðu í **Einingar \> Birgðastjórnun \> Afhendingmáti**.
1. Í aðgerðaglugganum velurðu **Nýtt** til að stofna nýjan flutningsmáta eða velur núverandi stillingu.
1. Í kaflanum **Smásölurásir** velurðu **Bæta við línu** til að bæta við rásinni. Að bæta við rásum með fyrirtækjahnútum í stað þess að bæta hverri rás fyrir sig getur auðveldað að rásum sé bætt við.

Eftirfarandi mynd sýnir dæmi um afhendingarmáta.

![Setja upp afhendingarmáta.](media/channel-setup-retail-7.png)

### <a name="set-up-incomeexpense-account"></a>Setja upp tekju-/útgjaldalykil

Til að setja upp tekju-/útgjaldalykil skal fylgja þessum skrefum.

1. Í aðgerðaglugganum velurðu flipann **Setja upp** og velur síðan **Tekju-/útgjaldalykil**.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Undir **Heiti** slærðu inn nafn.
1. Undir **Leitarheiti** slærðu inn leitarheiti.
1. Undir **Lykilgerð** færirðu inn lykilgerð.
1. Sláðu inn texta fyrir **Skilaboðalínu 1**, **Skilaboðalínu 2**, **Seðiltexta 1** og **Seðiltexta 2** eftir þörfum.
1. Undir **Bókun** slærðu inn upplýsingar um bókun.
1. Í aðgerðarúðunni skal velja **Vista**.

Eftirfarandi mynd sýnir dæmi um tekju-/útgjaldalykil.

![Setja upp tekju-/útgjaldalykla.](media/channel-setup-retail-8.png)

### <a name="set-up-sections"></a>Setja upp hluta

Til að setja upp hluta skal fylgja þessum skrefum.

1. Í aðgerðaglugganum velurðu flipann **Setja upp** og smellir á **Hlutar**.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Undir **Hlutanúmer** slærðu inn hlutanúmer.
1. Undir **Lýsing** skal færa inn lýsingu.
1. Undir **Hlutastærð** slærðu inn hlutastærð.
1. Stilla viðbótarstillingar fyrir **Almennt** og **Söluupplýsingar** eftir þörfum.
1. Í aðgerðarúðunni skal velja **Vista**.

### <a name="set-up-a-fulfillment-group-assignment"></a>Setja upp úthlutun uppfyllingarflokks

Til að setja upp úthlutun uppfyllingarflokks skal fylgja þessum skrefum.

1. Í aðgerðaglugganum velurðu flipann **Setja upp** og velur síðan **Úthlutun uppfyllingarflokks**.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Í fellilistanum **Uppfyllingarhópur** velurðu uppfyllingarhóp.
1. Í fellilistanum **Lýsing** skal færa inn lýsingu.
1. Í aðgerðaglugganum velurðu **Vista**.

Eftirfarandi mynd sýnir dæmi um uppstillingu úthlutunar uppfyllingarflokks.

![Setja upp úthlutanir uppfyllingarflokks.](media/channel-setup-retail-9.png)

### <a name="set-up-safes"></a>Setja upp öryggishólf

Til að setja upp öryggishólf skal fylgja þessum skrefum.

1. Í aðgerðaglugganum velurðu flipann **Setja upp** og smellir á **Öryggishólf**.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Sláðu inn heiti fyrir öryggishólfið.
1. Í aðgerðarúðunni skal velja **Vista**.

### <a name="ensure-unique-transaction-ids"></a>Tryggja einkvæm færslukenni

Frá og með Commerce-útgáfu 10.0.18 verða færslukenni fyrri sölustaðinn í samfelldri röð og innihalda eftirfarandi hluta:

- Fastur hluti, sem er samsetning verslunarkennis og kennis afgreiðslustöðvar. 
- Samfelldur hluti, sem er númeraröð. 

Nánar tiltekið er sniðið *{store}-{terminal}-{numbersequence}*. 

Þar sem hægt er að mynda færslukenni með og án nettengingar hafa komið upp tilvik þar sem sama færslukennið hefur verið búið til oftar en einu sinni. Mikil handvirk lagfæring gagna felst í að fjarlægja tvítekin færslukenni. 

Með Commerce-útgáfu 10.0.19 hefur snið færslukennis verið uppfært til að fjarlægja samfellda hlutann og í staðinn notað 13 stafa tölu sem búin er til með því að reikna tímann í millisekúndum frá árinu 1970. Með þessari breytingu er nýja snið færslukennisins orðið *{store}-{terminal}-{millisecondsSince1970}*. Með þessari uppfærslu verður færslukennið í ósamfelldri röð og tryggir að færslukennin verði alltaf einkvæm. 

> [!NOTE]
> Færslukenni eru eingöngu ætluð til nota í innra kerfinu og þurfa því ekki að vera í samfelldri röð. Mörg lönd gera hins vegar kröfu um að kenni innhreyfingarskjala séu í samfelldri röð.

Nýja eiginleikann fyrir snið færslukennis er hægt að virkja á vinnusvæðinu **Eiginleikastjórnun**. 

Til að virkja notkun nýrra færsluauðkenna skal fylgja þessum skrefum:

1. Í Commerce Headquarters skal fara í **Kerfisstjórnun \> Vinnusvæði \> Eiginleikastjórnun**.
1. Síið fyrir eininguna „smásala og viðskipti“.
1. Leitið að eiginleikaheitinu **Virkja nýtt færslukenni til að forðast tvítekin færslukenni**.
1. Veljið eiginleikann og veljið svo **Virkja núna** á hægra svæðinu.  
1. Farðu í **Retail og Commerce \> Upplýsingatækni í Retail og Commerce \> Dreifingaráætlun**.
1. Keyrið vinnslurnar **1070 Stilling rásar** og **1170 Verkskráning sölustaðar** til að samstilla virkjaðan eiginleika við verslanirnar.
1. Þegar breytingarnar hafa verið sendar í verslanirnar þarf að loka og opna aftur afgreiðslukössum verslunar til að nota nýtt snið færslukennis. 

> [!NOTE]
> Þegar nýr eiginleiki fyrir snið færslukennis hefur verið gerður virkur verður ekki hægt að slökkva á þessum eiginleika. Hafðu samband við Commerce Support ef hún þarf að vera óvirk.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit rása](channels-overview.md)

[Skilyrði fyrir uppsetningu rásar](channels-prerequisites.md)

[Setja upp netrás](channel-setup-online.md)

[Setja upp rás símavers](channel-setup-callcenter.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
