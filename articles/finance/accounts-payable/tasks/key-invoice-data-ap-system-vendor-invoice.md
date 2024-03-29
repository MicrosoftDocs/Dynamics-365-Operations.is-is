---
title: Lykilgögn reiknings í AP með því að nota reikning lánardrottins
description: Þessar verkefnaleiðbeiningar hjálpa notandanum að stofna reikning lánardrottins og skoða niðurstöður jöfnunar á innkaupapöntun, kvittun og reikningi (þríhliða jöfnun).
author: abruer
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines, VendEditInvoice, InventItemIdLookupSimple, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4c441d197957674d68c4c92b454a9dca91d76ea0
ms.sourcegitcommit: 9740f9b41a7dcf1821c6baccb2e05b9865ac2966
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/15/2022
ms.locfileid: "9775189"
---
# <a name="key-invoice-data-in-ap-using-a-vendor-invoice"></a>Lykilgögn reiknings í AP með því að nota reikning lánardrottins

[!include [banner](../../includes/banner.md)]

Þessar verkefnaleiðbeiningar hjálpa notandanum að stofna reikning lánardrottins og skoða niðurstöður jöfnunar á innkaupapöntun, kvittun og reikningi (þríhliða jöfnun).


## <a name="create-a-purchase-order"></a>Stofna innkaupapöntun
1. Í skoðunarrúðunni ferðu í **Kerfiseiningar > Viðskiptaskuldir > Innkaupapantanir > Allar innkaupapantanir**.
2. Smellt er á **Nýtt**.
3. Í reitnum **Lánardrottnalykill** skal smella á fellilistahnappinn til að opna leitina.
4. Finna lánardrottin til að velja. Til dæmis fletta niður að US-104.
5. Velja lánardrottin US-104
6. Smellt er á **OK**.
7. Í reitnum **Vörunúmer** skal smella á fellilistahnappinn til að opna leitina.
8. Velja birgðavöru. Til dæmis, veljið vörunúmerið 1000.
9. Útvíkkaðu flýtiflipann **Upplýsingar um línur**.
10. Smelltu á flipann **Uppsetning**. Hægt er að hnekkja jöfnunarreglunni til að nota enga jöfnun, tvíhliða jöfnun eða þríhliða jöfnun.  
11. Í aðgerðasvæðinu skal smella á **Innkaup**.
12. Smellið á **Staðfesta**.

## <a name="receive-the-products"></a>Taka við vörunum
1. Í aðgerðasvæðinu skal smella á **Móttaka**.
2. Smellið á **Innhreyfingarskjal afurða**.
3. Færið inn innhreyfingarskjalsnúmerið í reitnum **Innhreyfingarskjal**. Til dæmis er slegið inn „PR123“.
4. Smellið á **Í lagi** til að bóka innhreyfingarskjalið.
5. Lokið síðunni.

## <a name="create-a-vendor-invoice"></a>Stofna reikning lánardrottins
1. Í skoðunarrúðunni ferðu í **Kerfiseiningar > Viðskiptaskuldir > Innkaupapantanir > Mótteknar óreikningsfærðar innkaupapantanir**.
2. Velja innkaupapöntun sem var stofnuð.
3. Í aðgerðasvæðinu smellirðu á **Reikningur.**
4. Smelltu á **Reikningur**.
5. Færið inn númer reiknings í **Númer**.
6. Sláið inn gildi í reitinn **Reikningslýsing**.
7. Í retinum **Reikningsdagsetning** slærðu inn dagsetningu.
8. Í reitnum **einingarverð** er fært inn 1200.
9. Smella á **Bæta við línu**.
10. Í reitnum **Vörunúmer** skal smella á fellilistahnappinn til að opna leitina.
11. Finna vörunúmer uppsetningargjalda á listanum. Til dæmis S0001
12. Veljið vörunúmer uppsetningargjalda. Athugið að jöfnun hefur ekki verið framkvæmd síðan breytingarnar voru gerðar.  
13. Smelltu á **Uppfæra samsvörunarstöðu**.
14. Í aðgerðasvæðinu skal smella á **Yfirfara**.
15. Smellið á **Samsvörunarupplýsingar**. Ný lína með þjónustu þarf ekki að vera jafnað svo staðan segi "Ekki framkvæmt".  
16. Velja innhreyfingarskjal afurða fyrir birgðavöruna sem er móttekin. Línan með innhreyfingarskjalinu var jöfnuð en ósamræmi er í magni eða verði svo það mistókst.  
17. Í reitnum **Einingarverð** skal slá inn tölu. Þegar einingaverðið hefur verið jafnað uppfærist staðan í „Stóðst“. Ef reglan leyfir misræmi eða ef jöfnun er aðeins viðvörun er samt hægt að bóka reikninginn.  
18. Lokið síðunni.
19. Smelltu á **Bóka**.
20. Lokið síðunni. 

>[!Note] 
>Innkaupapöntunin er ekki lengur skráð sem móttekin en ekki reikningsfærð.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
