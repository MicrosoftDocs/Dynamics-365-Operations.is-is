---
title: fjárhagslegar og efnislegar uppfærslur
description: Þetta efnisatriði veitir yfirlit yfir hvaða gerðir færslna auka eða minnka birgðamagn.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTrans, InventTransVoucher
audience: Application User
ms.reviewer: kamaybac
ms.custom: 75023
ms.assetid: 128340e1-c573-48e6-b835-6c350d8dd0fb
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3c7b354a7524a6e96da8e2a9eeca0d4f21b9fb0a6d515620ab3fe446425af17c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6734380"
---
# <a name="physical-and-financial-updates"></a>fjárhagslegar og efnislegar uppfærslur

[!include [banner](../includes/banner.md)]

Þetta efnisatriði veitir yfirlit yfir hvaða gerðir færslna auka eða minnka birgðamagn. 

Birgðafærslur er hægt að uppfæra efnislega og fjárhagslega í Dynamics 365 Supply Chain Management. Sumar gerðir efnislegra og fjárhagsfærslna auka birgðamagn, á meðan aðrar draga úr magninu.

## <a name="physical-increases"></a>Efnisleg aukning
Þegar efnisleg færsla er bókuð er staða færsluskránnar **"Móttekið"**. Eftirfarandi færslur skoðast sem efnisleg aukning:

-   Móttaka innkaupapöntunar
-   Skil á fylgiseðli sölupöntunar
-   Skrá framleiðslupöntun sem lokið
-   Aukaafurð á tiltektarlista framleiðslupöntunar

## <a name="financial-increases"></a>Fjárhagsleg aukning
Þegar fjárhagsleg innhreyfingarfærsla er bókuð, er staða færsluskránnar sem eykur magnið **"Innkeypt".** Eftirfarandi færslur skoðast sem fjárhagsleg aukning:

-   Reikningur lánardrottins
-   Sölupöntunarreikningur vegna skila
-   Kostnaður framleiðslupöntunar
-   Birgðabækur með jákvæðu magni, svo sem hreyfing, hagnaður/tap, talningabækur, uppskriftir og flutningur

## <a name="transactions-that-increase-quantity"></a>Færslur sem auka magn
Færslur sem auka magn eru bókaðar á gildandi meðalkostnaðarverði. Útreiknað gildandi meðalkostnaðarverð sem er byggt á kostnaði hverrar slíkrar færslu fyrir hverja birgðavídd sem er fjárhagslega rakin. Sjá upplýsingar um hvernig keyra á meðalkostnaðarverð sjá [keyrsla á meðalkostnaðarverði](running-average-cost-price.md).

## <a name="transactions-that-decrease-quantity"></a>Færslur sem minnka magn
Útreiknað meðalkostnaðarverð er notað þegar hreyfing sem minnkar magn er bókuð án tillits til hver birgðalíkan er í félagi með því birgðir. Þetta krefst þess að færslan sem minnkar magn var ekki áður merkt annarri færslu fyrir bókun. Ef efnislegar lagerbirgðir verða neikvæðar er birgðakostnaðurinn sem er skilgreindur fyrir vöruna á síðunni **Vara** notaður. 

> [!NOTE]
> Ef virkni fjölsíðna er virkjuð verður þessi kostnaður í staðinn vera birgðakostnaður sem er skilgreint fyrir síðuna í síðunni **Sjálfgefnar pöntunarstillingar**.

## <a name="physical-issues-vs-financial-issues"></a>Efnislegar úthreyfingar miðað við fjárhagslegar úthreyfingar
Þegar efnisleg úthreyfingarfærsla er bókuð er staða færsluskránnar **"Dregið frá"**. Eftirfarandi færslur skoðast sem efnislegar úthreyfingar:

-   Tiltektarlistabók framleiðslupöntunar
-   Fylgiseðill sölupöntunar
-   Skil á fylgiseðli innkaupapöntunar

Þegar fjárhagsfærsla er bókuð, er staða færsluskránnar **"Selt"**. Eftirfarandi færslur skoðast sem fjárhagslegar úthreyfingar:

-   Ljúka framleiðslupöntun.
-   Sölupöntunarreikningur
-   Endursending reiknings lánardrottins
-   Birgðabækur með neikvæðu magni, svo sem hreyfing, hagnaður/tap, talningabækur, uppskriftir og flutningur

Færslur sem minnka magn eru bókaðar á hlaupandi meðaltal kostnaðarverðs. Þannig að birgðalokunarferlið þarf til að jafna úthreyfingarfærslur á innhreyfingarfærslur í samræmi við birgðalíkan sem tengt er við hverja vöru.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]