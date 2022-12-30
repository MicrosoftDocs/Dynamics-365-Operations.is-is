---
title: Stofna innkaupapöntun sem stjórnast af fjárhagsáætlun
description: Nota þetta ferli til að stofna innkaupapöntun sem er athuguð í tiltækri fjárhagsáætlun.
author: JennySong-SH
ms.date: 06/15/2020
ms.topic: business-process
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: aa9777ad3aa487dfb558879335f93f347b8ac749
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016189"
---
# <a name="create-a-purchase-order-governed-by-budget"></a>Stofna innkaupapöntun sem stjórnast af fjárhagsáætlun

[!include [banner](../../includes/banner.md)]

Nota þetta ferli til að stofna innkaupapöntun sem er athuguð í tiltækri fjárhagsáætlun.

## <a name="review-the-budget-control-configuration"></a>Yfirfara skilgreiningu fjárhagsáætlunarstýringar

1. Fara í **Fjárhagsáætlun > Uppsetning > fjárhagsáætlunarstýring > uppsetning fjárhagsáætlunarstýringa** r.
1. Veljið flipann **Tiltækt fjármagn úr fjárhagsáætlun**.
1. Veljið flipann **Skjöl og færslubækur**.
1. Veljið flipann **Skilgreina reglur fjárhagsáætlunarstýringar**.
1. Veljið flipann **Skilgreina fjárhagsáætlunarflokka**.
1. Lokið síðunni.

## <a name="create-a-purchase-order"></a>Stofna innkaupapöntun

1. Fara í **innkaup og aðföng > innkaupapöntun > allar innkaupapantanir**.
1. Veljið **Nýtt**.
1. Í reitinn **Lánardrottnalykill** skal færa inn eða velja gildi.
1. Útvíkka **Almennt** flýtiflipa.
1. Í reitnum **Dagsetning reikningsskila** skal stilla dagsetninguna.
1. Veldu **Í lagi** til að loka glugganum og opna nýju innkaupapöntunina.
1. Í flýtiflipanum **Innkaupapöntunarlínur** skal velja **Bæta við línu** úr tækjastikunni til að bæta við nýrri línu og síðan fylla út línuna eftir þörfum til að bæta vöru við pöntunina.
1. Á **Innkaupapöntunarlínur** velur þú **Financials \> Dreifa upphæðum**.
1. Í reitnum **Fjárhagslykill** skal tilgreina reikning.
1. Lokið síðunni.

## <a name="perform-budget-checking"></a>Framkvæma athugun á fjárhagsáætlun

1. Haltu áfram að vinna með innkaupapöntunina sem þú varst að bæta línu við.
1. Í flýtiflipanum **Innkaupapöntunarlínur** skal velja **Fjárhagur \> Framkvæma athugun á fjárhagsáætlun**.
1. Í flýtiflipanum **Innkaupapöntunarlínur** skal velja **Fjárhagur \> Villur eða viðvaranir í athugunum á fjárhagsáætlunum**.
1. Svarglugginn **Villur eða viðvaranir í athugunum á fjárhagsáætlunum** opnast. Athugaðu niðurstöður athugunar og veldu síðan **Loka** til að loka svarglugganum.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]