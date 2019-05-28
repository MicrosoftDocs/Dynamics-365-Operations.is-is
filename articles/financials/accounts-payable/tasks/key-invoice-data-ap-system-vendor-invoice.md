---
title: Lykilgögn reiknings í AP kerfið með því að nota reikning lánardrottins
description: Þessar verkefnaleiðbeiningar hjálpa notandanum að stofna reikning lánardrottins og skoða niðurstöður jöfnunar á innkaupapöntun, kvittun og reikningi (þríhliða jöfnun).
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines, VendEditInvoice, InventItemIdLookupSimple, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e1d2e31a5de7cefd20996c18bf4771296a587997
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569633"
---
# <a name="key-invoice-data-in-ap-system-using-vendor-invoice"></a>Lykilgögn reiknings í AP kerfið með því að nota reikning lánardrottins

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þessar verkefnaleiðbeiningar hjálpa notandanum að stofna reikning lánardrottins og skoða niðurstöður jöfnunar á innkaupapöntun, kvittun og reikningi (þríhliða jöfnun).


## <a name="create-a-purchase-order"></a>Stofna innkaupapöntun
1. Fara í Viðskiptaskuldir > Innkaupapantanir > Allar innkaupapantanir.
2. Smellið á „Nýtt“.
3. Í reitnum Lánardrottnalykill skal smella á fellilistahnappinn til að opna leitina.
4. Finna lánardrottin til að velja. Til dæmis fletta niður að US-104.
5. Velja lánardrottin US-104
6. Smellt er á Í lagi.
7. Í reitnum Vörunúmer skal smella á fellilistahnappinn til að opna leitina.
8. Velja birgðavöru. Til dæmis, veljið vörunúmerið 1000.
9. Útvíkka eða draga saman hluta upplýsingar Línu.
10. Smellið á flipann „Setja upp“.
    * Hægt er að hnekkja jöfnunarreglunni til að nota enga jöfnun, tvíhliða jöfnun eða þríhliða jöfnun.  
11. Útvíkka eða draga saman hluta upplýsingar Línu.
12. Smellið á „Innkaup“ á aðgerðarúðunni.
13. Smellið á „Staðfesta“.

## <a name="receive-the-products"></a>Taka við vörunum
1. Smellið á „Móttaka“ á aðgerðarúðunni.
2. Smellið á „Innhreyfingarskjal“.
3. Færið inn innhreyfingarskjalsnúmerið á svæðinu „Innhreyfingarskjal“. Til dæmis er slegið inn „PR123“.
4. Smellið á „Í lagi“ til að bóka innhreyfingarskjalið.
5. Lokið síðunni.

## <a name="create-a-vendor-invoice"></a>Stofna reikning lánardrottins
1. Farið í Viðskiptaskuldir > Innkaupapantanir > Mótteknar óreikningsfærðar innkaupapantanir.
2. Velja innkaupapöntun sem var stofnuð.
3. Í aðgerðasvæðinu er smellt á reikningur.
4. Smellt er á Reikningnum.
5. Færið inn númer reiknings á númerasvæðinu.
6. Sláið inn gildi á svæðinu „Reikningslýsing“.
7. Færið inn dagsetningu á svæðinu „Reikningsdagsetning“.
8. Í reitnum einingarverð er fært inn 1200.
9. Smella á bæta Við línu.
10. Í reitnum Vörunúmer skal smella á fellilistahnappinn til að opna leitina.
11. Finna vörunúmer uppsetningargjalda á listanum. Til dæmis S0001
12. Veljið vörunúmer uppsetningargjalda.
    * Athugið að jöfnun hefur ekki verið framkvæmd síðan breytingarnar voru gerðar.  
13. Smellið á „Uppfæra samsvörunarstöðu“.
14. Smellið á „Yfirfara“ á aðgerðarúðunni.
15. Smellið á „Samsvörunarupplýsingar“.
    * Ný lína með þjónustu þarf ekki að vera jafnað svo staðan segi "Ekki framkvæmt".  
16. Velja innhreyfingarskjal afurða fyrir birgðavöruna sem er móttekin.
    * Línan með innhreyfingarskjalinu var jöfnuð en ósamræmi er í magni eða verði svo það mistókst.  
17. Færið inn númer í reitnum „Einingarverð“.
    * Þegar einingaverðið hefur verið jafnað uppfærist staðan í „Stóðst“. Ef reglan leyfir misræmi eða ef jöfnun er aðeins viðvörun er samt hægt að bóka reikninginn.  
18. Lokið síðunni.
19. Smellið á „Bóka“.
20. Lokaðu skjámyndinni.
    * Athugið að innkaupapöntunin er ekki lengur skráð sem móttekin en ekki reikningsfærð.  

