---
title: "Greiðslur lánardrottna fyrir hlutaupphæð"
description: "Stundum þarf að framkvæma greiðslu til lánardrottins sem er minni en upphæð reiknings. Þessi grein lýsir mismunandi valkostum til að meðhöndla þær aðstæður. Valkostirnir sem eru tiltækir fyrir þig fara eftir viðskiptaþörfum og skilgreiningum fyrirtækisins."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14321
ms.assetid: 9a17075e-5325-4d55-a1e5-1791b8c460a0
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 2cb439e871d57f74c296697cfc42705fb0121bb7
ms.openlocfilehash: 4d243e6a9a68b69a6b32748344fc606ff3f2d965
ms.lasthandoff: 03/31/2017


---

# <a name="vendor-payments-for-a-partial-amount"></a>Greiðslur lánardrottna fyrir hlutaupphæð

Stundum þarf að framkvæma greiðslu til lánardrottins sem er minni en upphæð reiknings. Þessi grein lýsir mismunandi valkostum til að meðhöndla þær aðstæður. Valkostirnir sem eru tiltækir fyrir þig fara eftir viðskiptaþörfum og skilgreiningum fyrirtækisins. 

<a name="cash-discount-amounts"></a>Upphæðir staðgreiðsluafsláttar
---------------------

Lánardrottinn getur boðið þér staðgreiðsluafslátt fyrir greiðslu á reikning fyrir gjalddaga. Til dæmis færður er inn reikningur fyrir 100,00 sem tilgreinir 2 prósent staðgreiðsluafslátt ef reikningurinn er greiddur innan 10 daga. Skilmálar gjalddaga eru 30 dagar. Ef greiðslutillaga notar staðgreiðsluafslátt sem skilyrði fyrir því að velja reikning og ef tillagan er keyrð á undan dagsetningu staðgreiðsluafsláttar reikninginn er valinn fyrir greiðslu og greiðsla er stofnuð fyrir 98.00. Einnig er hægt að taka staðgreiðsluafslátt one-off greiðslu sem var stofnuð handvirkt.

## <a name="partial-payments-with-cash-discounts"></a>hlutagreiðslur með staðgreiðsluafslætti
Þegar þú reiðir fram hlutagreiðslu gætiðu gert áætlun um að gera frekari hlutagreiðslu til að jafna reikninginn að fullu. Að veita staðgreiðsluafslátt við hlutagreiðslu, verður að setja í ** Reikna staðgreiðsluafslætti fyrir hlutagreiðslur ** valkostur til að **Já** á á **Lykill færibreytur viðskiptaskulda** síðu. 

Til dæmis færðu 2 prósent staðgreiðsluafslátt ef reikningurinn er greiddur innan 10 daga eftir það hann er gefinn út. Bókaður er reikningur fyrir 100,00. Ef greiðsla 49.00 innan 10 daga, færa inn debet-49.00 í greiðslubók. Þegar hlutagreiðsla er jafnaður á í **Jafna opnar færslur** síðu **1,00** birtist í á **upphæð staðgreiðsluafsláttar sem á að taka** svæði. 

> [!NOTE] 
> Ef hlutagreiðslu til að færa inn og skiljið fullt reikningsupphæð í á **Upphæðin til jöfnunar** svæði í **upphæð staðgreiðsluafsláttar sem á að taka** svæði breytist sjálfkrafa þegar bókaðar eru í færslur.

## <a name="credit-notes-with-cash-discounts"></a>Kreditnótur með staðgreiðsluafslætti
Þú gætir skilað sumum af vörunum á reikningi og fengið kreditnótu. Ef staðgreiðsluafsláttur var tekinn á upphaflega reikningnum er hægt að draga virði afsláttar og fá endurgreiðslu fyrir rétta upphæð. Ef í ** Reikna staðgreiðsluafslætti fyrir kreditnótur ** valkostur er stilltur á **Já** á í **Færibreytur viðskiptaskulda** síðu afslátturinn er sjálfkrafa reiknaður út fyrir kreditnótu. 

Til dæmis færðu 2 prósent staðgreiðsluafslátt ef reikningurinn er greiddur innan 10 daga eftir það hann er gefinn út. Bókaður er reikningur fyrir 100,00. Ef skila á vörum og fá kreditnóta er hægt að færa inn kreditnótu fyrir heildarupphæðina á upphaflega reikninginn 100,00 með 2 prósent staðgreiðsluafslátt sem er einnig skilgreint í kreditreikninginn.  Þegar kreditnótan skoða á í **Jafna færslur** síðu **98.00** birtist í á **Upphæðin til jöfnunar** svæði, og **-2.00** birtist í á **upphæð staðgreiðsluafsláttar** svæði. Afsláttarupphæðin er bókuð á lykil fyrir staðgreiðsluafslátt.

## <a name="overpaymentunderpayment-amounts"></a>Upphæðir ofgreiðslu eða vangreiðslu
Þú getur reitt fram hlutagreiðslu þar sem upphæðin sem þarf að jafna er mjög lág. Til dæmis, reikningur lánardrottins er upp á 1.000,00 og þú greiðir 999,90. Ef eftirstandandi upphæð er lægri en upphæðin sem er tilgreind fyrir ofgreiðslu eða vangreiðslu á síðunni **Færibreytur viðskiptaskulda** er mismunur sjálfkrafa bókaður í fjárhagslykil ofgreiðslu/vangreiðslu.


