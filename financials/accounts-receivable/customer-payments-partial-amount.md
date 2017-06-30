---
title: "greiðsla viðskiptavinar fyrir hlutaupphæð"
description: "Stundum gera viðskiptavinur greiðslu sem er minni en upphæð reiknings. Þessi skrá lýsir mismunandi valkosti fyrir meðhöndlun þessar aðstæður. Valkostirnir sem eru tiltækir fyrir þig fara eftir viðskiptaþörfum og skilgreiningum fyrirtækisins."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13011
ms.assetid: 20423a2d-6997-4e1c-a596-a77016600071
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 795d13a07065a125a750970beaff85b59307f623
ms.contentlocale: is-is
ms.lasthandoff: 05/25/2017


---

# <a name="customer-payments-for-a-partial-amount"></a>greiðsla viðskiptavinar fyrir hlutaupphæð

[!include[banner](../includes/banner.md)]


Stundum gera viðskiptavinur greiðslu sem er minni en upphæð reiknings. Þessi skrá lýsir mismunandi valkosti fyrir meðhöndlun þessar aðstæður. Valkostirnir sem eru tiltækir fyrir þig fara eftir viðskiptaþörfum og skilgreiningum fyrirtækisins.

<a name="partial-payment-with-no-discount"></a>Hlutagreiðsla með engum afsláttur
--------------------------------

Viðskiptavinir gætu reott fra, hlutagreiðslu því var ekki nægilegt reiðufé til staðar til að greiða reikninginn að fullu, eða vegna ágreinings um vöru á reikningnum. Í þessum aðstæðum er hægt að jafna reikninginn að hluta með greiðslu. Reikningur verða áfram opnar og sýna stöðu.

## <a name="discount-amounts"></a>Afsláttarupphæðir
Hægt er að bjóða viðskiptavinum staðgreiðsluafslátt fyrir greiðslu á reikning fyrir gjalddaga. Til dæmis færður er inn reikningur fyrir 100,00 sem tilgreinir 2 prósent staðgreiðsluafslátt ef reikningurinn er greidd innan 10 daga. Skilmálar gjalddaga eru 30 daga. Ef tekið er við greiðslu uppá 98.00 innan 10 daga er færð inn greiðsla fyrir 98.00. Síðan, þegar reikningur er merkt til jöfnunar, er  staðgreiðsluafsláttar telomm sjálfkrafa.

## <a name="partial-payments-with-cash-discounts"></a>hlutagreiðslur með staðgreiðsluafslætti
Þegar viðskiptavinir reiða fram hlutagreiðslu, gætu þeir gert áætlun um að gera frekari hlutagreiðslu til að jafna reikninginn að fullu. Til að taka staðgreiðsluafslátt fyrir hlutagreiðslu, verður að stilla valkostinn **Reikna staðgreiðsluafslætti **fyrir hlutagreiðslur á **Já** á síðunni **Færibreytur viðskiptakrafna**. 

Til dæmis þú býður 2 prósent staðgreiðsluafslátt ef reikningurinn er greidd innan 10 daga eftir það hann er gefinn út. Bókaður er reikningur fyrir 100,00. Ef tekið er við greiðslu uppá 49.00 innan 10 daga er fært inn kredit uppá 49.00 í greiðslubók. Þegar hlutagreiðsla er jafnaður á í **Jafna færslur** síðu, birtist **1,00** í á **upphæð staðgreiðsluafsláttar sem á að taka** svæði. Afsláttarupphæðin er bókuð á lykil fyrir staðgreiðsluafslátt. 

> [!NOTE] 
> Ef hlutagreiðsla er færð inn og full reikningsupphæð er látin vera í reitnum **Upphæðin til jöfnunar** er **upphæð staðgreiðsluafsláttar sem á að taka** svæði sjálfkrafa endurreiknað þegar þú bókar færslur.

## <a name="credit-notes-with-discounts"></a>Kreditnótur með afslætti
Ef viðskiptavinir skila sumum af vörunum á reikningi, gætir þú gefið út kreditnótu. Ef staðgreiðsluafsláttur var tekin af upprunalega reikningi, ætti kreditreikning til viðskiptavinar að vera nettó staðgreiðsluafsláttar sem var tekinn af viðskiptavini. Ef **Reikna staðgreiðsluafslætti fyrir kreditnótur** valkostur er stilltur á **Já** í **Færibreytur viðskiptakrafna** síðu, er afslátturinn sjálfkrafa reiknaður út fyrir kreditnótu. 

Til dæmis þú býður greiðsluskilmálar sem tiltaka 2 prósent staðgreiðsluafslátt ef reikningurinn er greidd innan 10 daga eftir það hann er gefinn út. Reikningur fyrir 100,00 var bókuð og viðskiptavinur tók staðgreiðsluafsláttinn. Ef viðskiptavinur skilar vörur og kreditnóta er gefin út, er hægt að færa inn kreditnótu fyrir -100.00. Þegar kreditnótan er skoðuð á **Jafna opnar færslur** síðu birtist **98,00** í **Upphæðin til jöfnunar** svæðinu, og **-2,00** birtist í **upphæð staðgreiðsluafsláttar** svæðinu. Afsláttarupphæðin er bókuð á lykil fyrir staðgreiðsluafslátt.

## <a name="overpaymentunderpayment-amounts"></a>Upphæðir Ofgreiðslu eða vangreiðslu
Þegar viðskiptavinir greiða greiðslu, gæti verið mjög lágar upphæð sem þarf samt enn að jafna. Til dæmis reikningsfærir þú viðskiptavininn fyrir 1.000,00 og viðskiptavinur greiðir 999,90. Ef eftirstandandi upphæð er lægri en upphæðin sem tilgreindur er fyrir ofgreiðslu eða vangreiðslu á í**Færibreytur viðskiptakrafna** síðu, er mismunur sjálfkrafa bókuð í fjárhagslykil ofgreiðslu/vangreiðslu.

## <a name="full-settlement"></a>Full jöfnun
Viðskiptavinir gæti reitt fram hlutagreiðslu þar sem eftirstöðvar upphæðarinnar sem verður ekki greidd er hærri en upphæð vangreiðslu sem tilgreind er í á **færibreytur viðskiptaskulda** síðu. Ef óskað er að merkja reikning sem að fullu jafnaðan, er hægt að nota **Full jöfnun** valkostinn á **Jafna færsluna** síðu. (Hægt er að virkja aðgerðir fullrar jöfnunar með því að nota skilgreiningarlykil.) Til dæmis er reikningur bókaður fyrir 1.000,00 og viðskiptavinur greiðir inn á 990,00. Samþykkt hefur verið að viðskiptavinurinn þarf ekki að greiða eftirstandandi 10,00. Eftir að reikningur er merktur fyrir jöfnun, er einnig hægt að merkja velja **Full jöfnun**. Reikningur teljst svo að fullu jafnaður. mismunurinn 10,00 er bókaður í staðgreiðsluafsláttarlykill sem upphæð viðbótarstaðgreiðsluafsláttar.




