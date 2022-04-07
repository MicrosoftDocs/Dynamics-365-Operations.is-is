---
title: Ekki er hægt að bóka fylgiseðil fyrir stöðvaða sölupöntunarlínu
description: Ekki er hægt að bóka fylgiseðil fyrir stöðvaða sölupöntunarlínu
author: smithanataraj
ms.date: 03/07/2022
ms.topic: article
ms.search.form: WHSLoadTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mfp
ms.search.validFrom: 2022-03-07
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: 115cfe79e075eb36f73203818acdbb5e31fc0bad
ms.sourcegitcommit: c0f7ee7f8837fec881e97b2a3f12e7f63cf96882
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/22/2022
ms.locfileid: "8462920"
---
# <a name="cant-post-packing-slip-for-a-stopped-a-sales-order-line"></a>Ekki er hægt að bóka fylgiseðil fyrir stöðvaða sölupöntunarlínu

Villukóði SYS13203

## <a name="symptoms"></a>Einkenni

Þegar þú ert að reyna að senda fylgiseðil fyrir farm sýnir kerfið eftirfarandi villuboð:

> Ekki hægt að bóka fylgiseðil þegar sölupöntunarlína er stöðvuð eftir staðfestingu á útsendingu Ekki er hægt að tína magn.

## <a name="cause"></a>Orsök

Ein eða fleiri tengdar sölupöntunarlínur kunna að vera stöðvaðar, sem þýðir að kerfið kemur í veg fyrir frekari vinnslu þeirrar sölupöntunar. Þetta þýðir meðal annars að kerfið birtir ekki fylgiseðil fyrir pöntunina.

Til dæmis gæti notandi hafa ákveðið að stöðva eina eða fleiri pöntunarlínur vegna þess að viðskiptavinurinn hringdi til baka og hætti við pöntunina. Hins vegar, ef sending á útleið hefði þegar verið staðfest, þá hefði sendingin sem inniheldur sölupöntunina þegar farið líkamlega út úr vöruhúsinu, sem þýðir að stöðvun sölupöntunarlínanna hefur engin áhrif. Vegna þess að það er ekki lengur hægt að stöðva sendinguna líkamlega, geturðu líka stöðvað línur svo þú getir sent fylgiseðilinn. Þú þarft þá að meðhöndla niðurfellda pöntun sem skil.

## <a name="resolution"></a>Upplausn

Til að geta bókað fylgiseðilinn skaltu ganga úr skugga um að engin af viðkomandi sölupöntunarlínum sé stöðvuð með því að gera eftirfarandi skref.

1. Fara til **Allar sölupantanir \> Sala og markaðssetning \> Allar sölupantanir**.
1. Finndu og opnaðu sölupöntunina sem þú átt í vandræðum með.
1. Í flýtiflipanum **Sölupöntunarlínur** skal velja sölupöntunarlínu.
1. Á **Upplýsingar um línu** flýtiflipann, opnaðu **Almennt** flipann og vertu viss um að **Hætt** reiturinn er stilltur á *Nei*.
1. Haltu áfram að vinna þar til allar viðeigandi sölulínur eru ekki lengur stöðvaðar.
1. Reyndu aftur að bóka fylgiseðil fyrir farm eða sölupöntun.
