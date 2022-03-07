---
title: Breyta pöntunum innan samstæðu
description: Í þessu efnisatriði er útskýrt hvernig á að breyta pöntunarvirkni innan samstæðu
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
ms.openlocfilehash: 1129794bf0ac6513770f8b2a0eeb7fb6154d7942
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548342"
---
# <a name="change-intercompany-orders"></a>Breyta pöntunum innan samstæðu

[!include [banner](../../includes/banner.md)]

Ef sölupöntun innan samstæðu eða innkaupapöntun er breytt endurspegla samsvarandi sölu- eða innkaupapantanir í samsvarandi fyrirtæki líka þá breytingu.

## <a name="adding-new-lines"></a>Bæta nýjum línum við

Hægt er að bæta nýjum línum við sölupantanir og innkaupapantanir innan samstæðu ef upprunaleg sölupöntun er hluti af pöntunarkeðju innan samstæðu. Einnig er hægt að bæta við nýjum línum ef upprunaleg sölupöntun er ekki bein afhending. Ef upprunalega sölupöntunin er bein afhending er bara hægt að bæta nýjum pöntunarlínum við sölu- eða innkaupapöntunina innan samstæðunnar ef reiturinn **Leyfa óbeina stofnun** er valinn í flýtiflipanum **Samstæðustillingar** í upprunalegu sölupöntuninni.

## <a name="changing-prices-and-discounts"></a>Breyta verðum og afsláttum

Þú getur breytt verðum og afsláttum ef gátreitirnir **Leyfa breytingar á verði** og **Leyfa breytingar á afslætti** eru valdir á síðunni **Innan samstæðu**.

Ef einingarverði einnar af línunum sem til eru á sölupöntunarlínunni innan samstæðunnar er breytt er einingarverðinu á innkaupapöntuninni innan samstæðunnar líka breytt.

Ef nokkrum af afsláttarsvæðunum á sölupöntunarlínunni innan samstæðunnar er breytt eru viðeigandi afsláttarsvæði á innkaupapöntuninni innan samstæðunnar uppfærð.

## <a name="changing-and-adding-new-charges"></a>Breyta og bæta við nýjum gjöldum

Þú getur breytt gjöldum ef gátreitirnir **Leyfa breytingar á verði** og **Leyfa breytingar á afslætti** eru valdir á síðunni **Innan samstæðu**.

Ef nýju gjaldi er bætt við sölupöntunarhaus innan samstæðunnar og nýju gjaldi er bætt við sölulínu innan samstæðunnar eru bæði gjöldin afrituð í innkaupapöntun innan samstæðunnar. Þar af leiðandi eru samstæðusölupöntun og samstæðuinnkaupapöntun með sömu heildarupphæðina. Gjöldin eru aldrei afrituð yfir í upprunalegu sölupöntunina.

## <a name="copying-a-fee"></a>Afrita þóknun

Til að afrita þóknun yfir í upprunalegu sölupöntunina þarf að stofna hana sem nýja sölulínu sem er með vöru af gerðinni **Þjónusta**.

## <a name="changing-quantities-and-deleting-intercompany-purchases-and-sales-order-lines"></a>Breyta magni og eyða innkaupa- og sölupöntunarlínum innan samstæðu

Hægt er að breyta magninu eða eyða innkaupapöntunarlínu eða sölupöntunarlínu innan samstæðu aðeins ef línan hefur verið stofnuð beint af skjámyndinni **Sölupöntun** eða **innkaupapöntun**. Þessi breyting gerir annaðhvort innkaupapöntun eða sölupöntun eða pöntunarlínur innan samstæðu að upprunastað.

## <a name="origins-of-orders-and-order-lines"></a>Uppruni pantana og pöntunarlína

Pantanir og pöntunarlínur innan samstæðu geta haft einn af tveimur upprunastöðum:

- **Afleiddur** – Pöntunin var búin til sjálfkrafa úr pöntunarkeðju innan samstæðu.
- **Upprunastaður** – Notandi stofnaði pöntunina handvirkt.

Upprunastaðurinn er gefinn til kynna í pöntunarhaus innkaupapöntunar og sölupöntunar innan samstæðu í reitnum **Uppruni**. Þessi reitur er staðsettur í flýtiflipanum **Samstæðustillingar** í sölupöntuninni og í flýtiflipanum **Uppsetning** í innkaupapöntuninni.

Upprunar **Afleitt** og **Upprunastaður** eiga aðeins við um samstæðupantanir. Reiturinn **Uppruni** er auður fyrir allar sölupantanir, innkaupapantanir og pöntunarlínur. Þessi reitur er einnig auður í upprunalegu sölupöntuninni.

## <a name="example-derived-origin"></a>Dæmi: Afleiddur uppruni

Upprunaleg stofnun er stofnuð fyrir ytri viðskiptavin. Þessi sölupöntun inniheldur eina pöntunarlínu. Þessi upprunalega sölupöntun stofnar innkaupapöntun innan samstæðu sem inniheldur eina pöntunarlínu, sem stofnar sölupöntun sem inniheldur eina pöntunarlínu. Innkaupapöntunarhausinn innan samstæðunnar og pöntunarlínan eru sjálfkrafa stofnaðar úr upprunalegu sölupöntuninni.

Gildið í reitnum **Uppruni** í flýtiflipanum **Uppsetning** fyrir innkaupapöntun innan samstæðu og flýtiflipanum **Samstæðustillingar** fyrir sölupöntunarhausa innan samstæðu er **Afleiddur**. Gildið í reitnum **Uppruni** í flipanum **Upplýsingar um línu** fyrir innkaupapöntunar- og sölupöntunarlínur er einnig **Afleitt**.

Ef pöntunarlína er með upprunann **Afleitt** er ekki hægt að eyða pöntunarlínunni beint. Aðeins er hægt að eyða pöntunarlínunni úr upprunanum sem stofnaði pöntunarlínuna. Einnig er aðeins hægt að breyta pantaða magninu úr upprunanum sem stofnaði pöntunarlínuna.

Ef upprunaleg sölupöntun og upprunaleg sölupöntunarlína eru hluti af pöntunarkeðjunni innan samstæðunnar er hægt að breyta pantaða magninu úr upprunalegu sölupöntuninni og hægt er að eyða pöntunarlínum úr upprunalegu sölupöntuninni.

## <a name="example-source-origin"></a>Dæmi: Uppruni upprunastaðar

Hægt er að stofna innkaupapöntun fyrir samstæðulánardrottinn. Innkaupapöntun og pöntunarlína innan samstæðunnar eru bæði með upprunastaðinn **Uppruni**. Þar af leiðandi er þessi samstæðuinnkaupapöntun stýringin og samstæðusölupöntunin sem er stofnuð sjálfkrafa í fyrirtæki lánardrottins með upprunastaðinn **Afleitt**.

Þar að auki er ekki hægt að breyta pöntuðu magni í pöntunarlínu sem er stofnuð í innkaupapöntuninni innan samstæðunnar á sölupöntuninni innan samstæðunnar. Aðeins er hægt að eyða pöntunarlínunni úr samstæðuinnkaupapöntuninni. Ef nýrri línu er bætt við samstæðusölupöntunina verður sölupöntunarlína samstæðunnar þá með upprunastaðinn **Uppruni**.

Þegar upprunaleg sölupöntun er hluti af pöntunarkeðjunni innan samstæðunnar er alltaf hægt að stjórna pöntununum innan samstæðunnar og pöntunarlínunum innan samstæðunnar úr upprunalegu sölupöntuninni.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
