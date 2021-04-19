---
title: Skrá vörumóttöku í innkaupapöntun
description: Þetta efni útskýrir hvernig á að skrá móttöku á vörum beint á innkaupapöntun.
author: kamaybac
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a030de902915d25d1b309e53a2af5d8b7ec32125
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811967"
---
# <a name="record-the-receipt-of-goods-on-the-purchase-order"></a>Skrá vörumóttöku í innkaupapöntun

[!include [banner](../../includes/banner.md)]

Þetta efni útskýrir hvernig á að skrá móttöku á vörum beint á innkaupapöntun. Einnig er hægt að skrá innhreyfingu afurða í vöruhúsinu og síðan síðar skrá hana í innkaupapöntun. Þetta verk er yfirleitt gert af innkaupaaðila eða af samræmingaraðila viðskiptaskulda. Dæmi sem eru sýnd í þessari handbók er hægt að nota sýnigögn USMF-fyrirtækisins. Dæmin inniheldur skref til að stofna einfalda innkaupapöntun, þannig að hægt er að spila ferlið sem leiðarvísi fyrir verk. Ef þú værir að nota ferlið á þín eigin gögn, myndirðu byrgja á undirverkinu **Færsla innhreyfingar á vörum**.


## <a name="prepare-a-new-purchase-order-for-receipt-of-goods"></a>Undirbúa nýja innkaupapöntun vegna móttöku afurða.
1. Farðu í **Skoðunarrúðu > Kerfiseiningar > Innkaup og aðföng > Innkaupapantanir > Allar innkaupapantanir**.
2. Veljið **Nýtt**.
3. Í svæðinu **Lánardrottnalykill** skal slá inn `US-101`.
4. Veljið **Í lagi**.
5. Í reitinn **Vörunúmer** slærðu inn `M0001`.
6. Í reitinn **Magn** skal slá inn `5`.
7. Í aðgerðasvæðinu velurðu **Innkaup**.
8. Veldu **Staðfesta**.

## <a name="record-receipt-of-goods"></a>Skrásetja viðtöku varnings
1. Í aðgerðasvæðinu velurðu **Móttaka**.
2. Velja **Innhreyfingarskjal afurða**. Reiturinn **Magn** leyfir þér að velja mismunandi valkosti fyrir það magn sem á að taka á móti. Til dæmis, ef áður hefur verið skráð magn í vöruhúsi, er hægt að velja **Skráð magn**. Í þessu dæmis, notaðu gildið **Pantað magn**.
3. Víkkið út hlutann **Yfirlit**.
4. Í reitinn **Móttaka afurða** skal slá inn gildi. Þetta svæði er notað til að færa inn tilvísun sem verður notað sem fylgiskjal fyrir færslubók innhreyfingarskjala afurða.  
5. Stækka hlutann **Línur**.
6. Stillið **Magn** á „4“. Hér er hægt að tilgreina handvirkt magn sem fæst fyrir hverja línu í pöntun.  
7. Veljið **Í lagi**. Vörurnar hafa nú verið skráð sem móttekið á innkaupapöntuninni og búið er að stofna færslubók fyrir innhreyfingarskjal afurða sem endurspegla þetta. Hægt er að nota aðgerðina innhreyfing afurðar til að fara yfir færslubækur sem stofnaðar eru með innkaupapöntuninni og sjá hvað var móttekið og hvenær.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]