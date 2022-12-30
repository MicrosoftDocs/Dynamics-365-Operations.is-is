---
title: Setja upp færibreytur til að bóka samstæðupöntun
description: Þessi grein útskýrir hvernig á að setja upp færibreytur til að bóka samstæðupöntun
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 97ea0061d57beede6350eecfd497c12dd37aea31
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900797"
---
# <a name="set-up-parameters-to-post-an-intercompany-order"></a>Setja upp færibreytur til að bóka samstæðupöntun

[!include [banner](../../includes/banner.md)]

Þegar samstæðureikningur viðskiptavinar er bókaður er hægt að hafa uppsetninguna þannig að bæði innkaupapöntun samstæðu og upprunalegur reikningur viðskiptavinar eru bókuð sjálfvirkt.

> [!NOTE]
> Áður en þessi aðgerð er framkvæmd skal setja upp prentstýringuna í fyrirtækinu til að benda á réttan prentara reiknings. Þetta tryggir að reikningurinn fyrir upphaflegu sölupöntunina prentist í réttum prentara.

Eftirfarandi færibreytur verður að setja upp:

1. Farðu í **Sölu og markaðssetningu \> Sölupöntun \> Allar sölupantanir**. Veldu sölupöntunina sem á að vinna við.
1. Í sölupöntuninni á aðgerðasvæðinu skal velja **Hausyfirlit** og því næst velja flýtiflipann **Samstæðustillingar** og opna þær.
1. Farðu á aðgerðasvæðið, í flipann **Sölupöntun**, og veldu því næst **Breyta**.
1. Farðu aftur í flýtiflipann **Samstæðustillingar** og veldu **Beina afhendingu** til að virkja beina afhendingu í gegnum samstæðukeðjuna (allar pantanir).
1. Veldu **Vista** til að vista sölupöntunina með nýju stillingunni. Því næst skal velja **Loka** til að loka sölupöntuninni.
1. Farið í **Innkaup og aðföng \> Lánardrottnar \> Allir lánardrottnar**. Í flipanum **Almennt** skal velja **Innan samstæðu**.
1. Á síðunni **Innan samstæðu** skal velja tengilinn **Innkaupapöntunarreglur**. Í reitahópnum **Samstæðuinnkaupapöntun (bein afhending)** skal velja **Bóka reikning sjálfvirkt** og fjarlægja gátmerkið úr reitnum **Prenta reikning sjálfvirkt**.
1. Í reitahópnum **Upphafleg sölupöntun (bein afhending)** skal velja reitinn **Bóka reikning sjálfvirkt** og reitinn **Prenta reikning sjálfvirkt**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
