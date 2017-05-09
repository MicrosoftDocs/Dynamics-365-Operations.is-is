---
title: "fjárhagslegar og efnislegar uppfærslur"
description: "Þetta efnisatriði veitir yfirlit yfir hvaða gerðir færslna auka eða minnka birgðamagn."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventTrans, InventTransVoucher
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 75023
ms.assetid: 128340e1-c573-48e6-b835-6c350d8dd0fb
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: d68006c756f6b29804cad1d05db9ced2bd33897d
ms.lasthandoff: 03/31/2017


---

# <a name="physical-and-financial-updates"></a>fjárhagslegar og efnislegar uppfærslur

[!include[banner](../includes/banner.md)]


Þetta efnisatriði veitir yfirlit yfir hvaða gerðir færslna auka eða minnka birgðamagn. 

Birgðafærslur er hægt að uppfæra efnislega og fjárhagslega í Microsoft Dynamics 365 for Operations. Sumar gerðir efnislegra og fjárhagsfærslna auka birgðamagn, á meðan aðrar draga úr magninu.

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
Færslur sem auka magn eru bókaðar á gildandi meðalkostnaðarverði. Dynamics 365 for Operations reiknar út gildandi meðalkostnaðarverð sem er byggt á kostnaði hverrar slíkrar færslu fyrir hverja birgðavídd sem er fjárhagslega rakin. Sjá upplýsingar um hvernig keyra á meðalkostnaðarverð sjá [keyrsla á meðalkostnaðarverði](running-average-cost-price.md).

## <a name="transactions-that-decrease-quantity"></a>Færslur sem minnka magn
Dynamics 365 for Operations notar reiknaða keyrslu á meðalkostnaðarverði þegar hreyfing sem minnkar magn er bókuð án tillits til hver birgðalíkan er í félagi með því birgðir. Þetta krefst þess að færslan sem minnkar magn var ekki áður merkt annarri færslu fyrir bókun. Ef efnislegar lagerbirgðir verða neikvæðar notar Dynamics 365 for Operations birgðakostnað sem er skilgreindur fyrir vöruna á síðunni **afurð**. **Athugasemd** Ef virkni fjölsíðna er virkjuð verður þessi kostnaður í staðinn vera birgðakostnaður sem er skilgreint fyrir síðuna í síðunni **sjálfgefnar pöntunarstillingar**.

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




