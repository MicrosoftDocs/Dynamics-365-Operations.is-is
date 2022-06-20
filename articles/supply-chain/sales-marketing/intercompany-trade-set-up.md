---
title: Setja upp viðskipti innan samstæðu
description: Þessi grein útskýrir hvernig á að setja upp viðskipti milli fyrirtækja
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: CustTable, VendTable, EcoResProductListPage, InterCompanyTradingRelationSetupCustomer
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 8d956c60db9f3acf2f1759dc3e1922da40d8a514
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905632"
---
# <a name="set-up-intercompany-trade"></a>Setja upp viðskipti innan samstæðu

[!include [banner](../../includes/banner.md)]

Til þess að Microsoft Dynamics 365 Supply Chain Management geti keyrt viðskipti innan samstæðu þarf að láta viðskiptavini og lánardrottna framkvæma samstæðuviðskipti. Einnig þarf að setja upp viðskiptaskuldir, viðskiptakröfur, innkaup og aðföng og sölu og markaðssetningu.

## <a name="before-you-set-up-intercompany-trade"></a>Áður en samstæðuviðskipti eru sett upp

Áður en samstæðuviðskipti eru sett upp verður að ákveða hverjir viðskiptavinanna eru viðskiptavinir innan samstæðu og hverjir lánardrottnana eru lánardrottnar innan samstæðu. Fyrir hvern lögaðila í Microsoft Dynamics 365 Supply Chain Management þarf að ákveða hvaða viðskiptareglur eiga við um viðskiptavensl innan samstæðu fyrir tiltekinn samstæðuviðskiptavin eða samstæðulánardrottin.

Við mælum sérstaklega með því að þú og fyrirtækið þitt kynnið ykkur samstæðufæribreyturnar.

- Ræðið áhrif uppsetningarinnar við stjórnendur sem bera ábyrgð á samstæðuviðskiptum í hverjum lögaðila fyrir sig.
- Settu upp viðeigandi gildi fyrir hvern lögaðila.

## <a name="set-up-trading-relations"></a>Setja upp viðskiptatengsl

Til að setja upp samstæðuviðskipti fyrir viðskiptavini og lánardrottna skal fylgja þessum skrefum.

1. Farðu í **Viðskiptakröfur \> Viðskiptavinir \> Alla viðskiptavini**.
1. Veljið viðskiptavinalykil.
1. Í aðgerðasvæðinu, á flipanum **Almennt**, skal velja **Innan samstæðu**.
1. Tilgreindu uppsetningarfæribreytur innan samstæðu fyrir viðskiptavinalykilinn. Þessar færibreytur fela í sér lögaðila sem inniheldur samsvarandi lánardrottin og lánardrottnalykil. Færibreyturnar fela einnig í sér reglur innkaupapöntunar, reglur sölupöntunar, gildisvörpun og reglur sölusamninga og innkaupasamninga. Þú tilgreinir einnig hvort nota eigi gildi grunngagna úr viðskiptavinalyklinum eða úr lánardrottnalyklinum í hinum lögaðilanum.
1. Endurtakið skref 1 til 4 fyrir hina samstæðuviðskiptavinina í lögaðilanum.
1. Farið í **Viðskiptaskuldir \> Lánardrottnar \> Allir lánardrottnar**.
1. Veljið lánardrottinslykil.
1. Í aðgerðasvæðinu, á flipanum **Almennt**, skal velja **Innan samstæðu**.
1. Tilgreindu uppsetningarfæribreytur innan samstæðu fyrir lánardrottnalykilinn. Þessar færibreytur fela í sér lögaðila sem inniheldur samsvarandi viðskiptavin og viðskiptavinalykil. Færibreyturnar fela einnig í sér reglur sölupöntunar, reglur innkaupapöntunar, gildisvörpun og reglur sölusamninga og innkaupasamninga. Þú tilgreinir einnig hvort nota eigi gildi grunngagna úr lánardrottnalyklinum eða úr viðskiptavinalyklinum í hinum lögaðilanum.
1. Endurtakið skref 6 til 9 fyrir hina samstæðulánardrottnana í lögaðilanum.

## <a name="set-up-products"></a>Setja upp afurðir

Til að setja upp samstæðuviðskipti fyrir viðskiptavini og lánardrottna skal fylgja þessum skrefum.

1. Opnið **Upplýsingastjórnun afurða \> Afurðir \> Allar afurðir og afurðarsniðmát**.
1. Skilgreindu afurðirnar sem eru gefnar út í lögaðilanum þar sem á að stunda samstæðuviðskipti.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
