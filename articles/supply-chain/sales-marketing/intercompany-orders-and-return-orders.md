---
title: Pantanir og skilapantanir innan samstæðu
description: Þetta efnisatriði útskýrir pantanir og skilapantanir innan samstæðu
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
ms.openlocfilehash: 103225595e82bdedec6d97e5ebe5b61498377065
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548340"
---
# <a name="intercompany-orders-and-return-orders"></a>Pantanir og skilapantanir innan samstæðu

[!include [banner](../../includes/banner.md)]

Þetta efnisatriði lýsir því hvernig innkaupapöntun innan samstæðu, sölupantanir, skilapantanir, innkaupasamninga og sölusamningar eru stofnaðir og uppfærð.

## <a name="about-intercompany-orders"></a>Um samstæðupantanir

Þegar samstæðusölupöntun er stofnuð, stofnar Microsoft Dynamics 365 Supply Chain Management samsvarandi innkaupapöntun sjálfkrafa. Að sama skapi stofnast samsvarandi samstæðusölupöntun sjálfkrafa þegar samstæðuinnkaupapöntun er stofnuð.

Þetta er rétt fyrir pantanir með tvo leggi (færslur á milli tveggja tengdra fyrirtækja) og fyrir flest fyrirtæki með þrjá leggi (þegar samstæðufærsla á uppruna í sölupöntun fyrir ytri viðskiptavin).

## <a name="intercompany-order-example"></a>Dæmi um pöntun innan samstæðu

Notandi er með tvö tengd fyrirtæki. Fyrirtæki A er  söludótturfyrirtæki og fyrirtæki B er dreifingareining. Samstæðusölupantanir og -innkaupapantanir stofnaðar sjálfvirkt við eftirfarandi kringumstæður:

- Þegar fyrirtæki A stofnar innkaupapöntun og lánardrottinn er fyrirtæki B, er samstæðusölupöntun stofnuð sjálfkrafa í fyrirtæki B. Tveggja liða pöntunarkeðjan felur í sér innkaupapöntun í fyrirtæki A og samstæðusölupöntun í fyrirtæki B.
- Þegar fyrirtæki B býr til sölupöntun og viðskiptamaðurinn er fyrirtæki A, er samstæðuinnkaupapöntun sjálfvirkt stofnuð í fyrirtæki A. Þessi tveggja leggja pöntunarkeðja samanstendur af sölupöntun í fyrirtæki B og samstæðusölupöntun í fyrirtæki A.
- Þegar fyrirtæki A býr fyrst til sölupöntun fyrir ytri viðskiptamann, er hægt að stofna sjálfvirkt innkaupapöntun í fyrirtæki A. Um leið knýr það sjálfvirka stofnun samstæðusölupöntunar í fyrirtæki B. Þessi þriggja leggja pöntunarkeðja samanstendur af sölupöntun og innkaupapöntun í fyrirtæki A og samstæðusölupöntun í fyrirtæki B.

## <a name="about-intercompany-return-orders"></a>Um samstæðuskilapantanir

Hægt er að skila samstæðuvörum, rétt eins í hefðbundnum skilum. Þegar um samstæðuvöruskil er hins vegar að ræða stofnar vöruskilapöntun frá ytri viðskiptavini innkaupapöntun samstæðu. Þetta á hinn bóginn leiðir til sjálfvirk stofnun söluvöruskilapöntuninnan samstæðu. Einnig er hægt að skila samstæðuvöru án vöruskilapöntunar frá ytri viðskiptavini.

Skilapantanir innan samstæðu, svipaðar venjulegum skilapöntunum, hefjast á síðunni **Stofna skilapöntun**.

Í Microsoft Dynamics 365 Supply Chain Management eru sölu og innkaupasamningar innan samstæðu uppfærðir sjálfkrafa til að endurspegla skilavöru. Sala- eða innkaupasamningur fyrir þessa vöru er sjálfvirkt leiðrétt til að endurspegla breytingarnar í magni eða upphæð þegar vöru er skilað.

## <a name="intercompany-return-order-example"></a>Dæmi um skilapöntun innan samstæðu

Fyrirtæki A stofnar innkaupapöntun sem er tengd við innkaupasamning fyrir vöru innan samstæðu. Samstæðusölupöntun er sjálfkrafa stofnuð í Fyrirtæki B sem er tengt við samsvarandi sölusamning. Innkaupasamningurinn og sölusamningurinn tengjast í gegnum samninga innan samstæðu.

Fyrirtæki A skilar innansamstæðuvöru til fyrirtækis B. Fyrirtæki B stofnar skilapöntun fyrir vöruna og innkaupaskilapöntun er sjálfkrafa stofnuð í fyrirtæki A. Skuldbindingar í bæði innkaupasamningnum og sölusamningnum sem tengjast upprunalegum pöntunum eru sjálfkrafa leiðréttar til að endurspegla breytingu á magni eða upphæð.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
