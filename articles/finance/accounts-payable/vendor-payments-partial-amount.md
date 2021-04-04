---
title: Greiðslur lánardrottna fyrir hlutaupphæð
description: Stundum þarf að framkvæma greiðslu til lánardrottins sem er minni en upphæð reiknings. Þessi skrá lýsir mismunandi valkosti fyrir meðhöndlun þessar aðstæður.
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.custom: 14321
ms.assetid: 9a17075e-5325-4d55-a1e5-1791b8c460a0
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 43b0f4f6a6988f659c957664b140c4b9907ef3d3
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5255694"
---
# <a name="vendor-payments-for-a-partial-amount"></a>Greiðslur lánardrottins fyrir hlutaupphæð

[!include [banner](../includes/banner.md)]

Stundum þarf að framkvæma greiðslu til lánardrottins sem er minni en upphæð reiknings. Þessi grein lýsir mismunandi valkostum til að meðhöndla þær aðstæður. Valkostirnir sem eru tiltækir fyrir þig fara eftir viðskiptaþörfum og skilgreiningum fyrirtækisins. 

<a name="cash-discount-amounts"></a>Upphæðir staðgreiðsluafsláttar
---------------------

Lánardrottinn getur boðið þér staðgreiðsluafslátt fyrir greiðslu á reikning fyrir gjalddaga. Til dæmis færður er inn reikningur fyrir 100,00 sem tilgreinir 2 prósent staðgreiðsluafslátt ef reikningurinn er greiddur innan 10 daga. Skilmálar gjalddaga eru 30 dagar. Ef greiðslutillaga notar staðgreiðsluafslátt sem skilyrði fyrir því að velja reikning og ef tillagan er keyrð á eða á undan dagsetningu staðgreiðsluafsláttar er reikningurinn valinn til greiðslu og greiðsla er stofnuð fyrir 98,00. Einnig er hægt að taka staðgreiðsluafslátt fyrir eingreiðslu sem var stofnuð handvirkt.

## <a name="partial-payments-with-cash-discounts"></a>hlutagreiðslur með staðgreiðsluafslætti
Þegar þú reiðir fram hlutagreiðslu gætiðu gert áætlun um að gera frekari hlutagreiðslu til að jafna reikninginn að fullu. Til að taka staðgreiðsluafslátt fyrir hlutagreiðslu, verður að stilla valkostinn **Reikna staðgreiðsluafslætti fyrir hlutagreiðslur** á **Já** á síðunni **Færibreytur viðskiptakrafna**. 

Til dæmis færðu 2 prósent staðgreiðsluafslátt ef reikningurinn er greiddur innan 10 daga eftir það hann er gefinn út. Bókaður er reikningur fyrir 100,00. Ef greitt er 49,00 innan 10 daga er fært inn debet uppá 49,00 í greiðslubók. Þegar hlutagreiðsla er jöfnuð á síðunni **Jafna opnar færslur** birtist **1,00** í svæðinu **upphæð staðgreiðsluafsláttar sem á að taka**. 

> [!NOTE] 
> Ef hlutagreiðsla er færð inn og full reikningsupphæð er látin vera í reitnum **Upphæðin til jöfnunar** er **upphæð staðgreiðsluafsláttar sem á að taka** svæði sjálfkrafa endurreiknað þegar þú bókar færslur.

## <a name="credit-notes-with-cash-discounts"></a>Kreditnótur með staðgreiðsluafslætti
Þú gætir skilað sumum af vörunum á reikningi og fengið kreditnótu. Ef staðgreiðsluafsláttur var tekinn á upphaflega reikningnum er hægt að draga virði afsláttar og fá endurgreiðslu fyrir rétta upphæð. Ef valkosturinn **Reikna staðgreiðsluafslátt fyrir kreditnótur** er stilltur á **Já** á síðunni **Færibreytur viðskiptaskulda**, er afslátturinn sjálfkrafa reiknaður út fyrir kreditnótu. 

Til dæmis færðu 2 prósent staðgreiðsluafslátt ef reikningurinn er greiddur innan 10 daga eftir það hann er gefinn út. Bókaður er reikningur fyrir 100,00. Ef þú skilar vörunum og færð kreditnótu geturðu fært inn kreditnótu fyrir fulla upphæð upprunalegs reiknings, 100,00, ásamt 2 prósent staðgreiðsluafslætti sem er einnig skilgreindur í kreditnótunni.  Þegar kreditnótan er skoðuð á **Jafna færslur** síðu birtist **98.00** í svæðinu **Upphæðin til jöfnunar** og **-2,00** birtist í á **upphæð staðgreiðsluafsláttar** svæði. Afsláttarupphæðin er bókuð á lykil fyrir staðgreiðsluafslátt.

## <a name="overpaymentunderpayment-amounts"></a>Upphæðir ofgreiðslu eða vangreiðslu
Þú getur reitt fram hlutagreiðslu þar sem upphæðin sem þarf að jafna er mjög lág. Til dæmis, reikningur lánardrottins er upp á 1.000,00 og þú greiðir 999,90. Ef eftirstandandi upphæð er lægri en upphæðin sem er tilgreind fyrir ofgreiðslu eða vangreiðslu á síðunni **Færibreytur viðskiptaskulda** er mismunur sjálfkrafa bókaður í fjárhagslykil ofgreiðslu/vangreiðslu.


Frekari upplýsingar eru í [Yfirlit greiðslur lánardrottins](../cash-bank-management/tasks/vendor-payment-overview.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]