---
title: Þjónustupöntunarstig
description: Með því að skilgreina stig fyrir þjónustupöntun og úthluta þeim til starfsmanna, stjórnarðu flæði þjónustupantana með þeim verkefnum sem ýmsir einstaklingar sinna í þjónustufyrirtækinu.
author: ShylaThompson
manager: tfehr
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAStageTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7eab1b10e8c8782306c1c2d892f965dc0795c69a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5224403"
---
# <a name="service-order-stages"></a>Þjónustupöntunarstig   

[!include [banner](../includes/banner.md)]


Þú getur sett upp stig fyrir þjónustupöntun til þess að skilgreina verkefni sem þarf að ljúka, í hvaða röð þeim er lokið og starfsmenn sem bera ábyrgð á því að ljúka þeim. Með því að skilgreina í stiganna fyrir þjónustupöntun og úthlutun þess á starfsmönnum, hægt að stýra flæði þjónustupöntunar gegnum verkefnum sem mismunandi unnin þjónustufyrirtækið. Röð stiga verður að innihalda frumstig.

Einnig er hægt að skilgreina aðgerðir sem eru leyfðar á hverju stigi. Til dæmis, ef þú hreinsar gátreitinn **Bóka** fyrir öll stig nema síðasta stigið, er komið í veg fyrir að þjónustupantanir séu bókaðar áður en þjónustupantanir eru unnar í gegnum öll stigin.

## <a name="branching-in-service-order-stages"></a>Leiðaskil í þjónustupantanastig

Þegar sett er upp þjónustustig, er hægt að stofna marga valkosti eða greinar, til að velja úr fyrir næsta stig þjónustupöntunar. Öll útibú sem þú stofnar eru til að velja úr þegar fyrsta áfanga er lokið. T.d. setja upp **Áætlanagerð** sem frumstig. Stofna stigin með heitinu **í vinnslu** og **hætta Við**, og veljið síðan **Áætlanagerðar** sem yfirstig fyrir þær. Þú úthlutar stiginu **Áætlanagerð** til sölupöntunarinnar. Þegar stig fjárhagsáætlunargerðar fyrir sölupöntunina er lokið er hægt að velja á **í vinnslu** áfangi ef sölupöntunin er tilbúið til að vinna eða er hægt að velja á **hætta Við** áfangi ef hætt er við sölupöntun.

## <a name="see-also"></a>Sjá einnig

[Setja upp stig þjónustupantana](set-up-service-order-stages.md)

[Breyta þjónustupöntunarstigi](change-service-order-stage.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]