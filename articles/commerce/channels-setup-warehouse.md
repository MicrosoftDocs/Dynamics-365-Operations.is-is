---
title: Setja upp vöruhús
description: Þetta efni lýsir því hvernig á að setja upp vöruhús til að nota með nýrri rás í Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 67c0bb169bee8a7ea90edb4db7233111a8ee6e34
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993654"
---
# <a name="warehouse-set-up"></a>Uppsetning vöruhúss


[!include [banner](includes/banner.md)]

Þetta efni lýsir því hvernig á að setja upp vöruhús til að nota með nýrri rás í Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Hver Commerce-rás þarf að vera með stillt vöruhús tengt. Eftirfarandi ferli veita lágmarksstillingu sem þarf til að setja upp vöruhús fyrir Commerce-rás. Nánari upplýsingar um skipulag vöruhúsa er að finna í [Yfirlit vöruhúsastjórnunar](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json).

## <a name="configure-a-warehouse-site"></a>Stilla svæði vöruhúss

Áður en vöruhús er sett upp þarftu að stilla vöruhússíðu.

Fylgdu þessum skrefum til að stilla vöruhús.

1. Í yfirlitsglugganum ferðu í **Einingar \> Retail og Commerce \> Uppsetning rásar \> Svæði**.
1. Í aðgerðaglugganum velurðu **Nýtt**.
1. Í reitinn **Svæði** skal slá inn gildi.
1. Í reitinn **Heiti** skal slá inn gildi.
1. Í kaflanum **Almennt** stillirðu viðeigandi **Tímabelti**.
1. Í hlutanum **Aðsetur** færirðu inn heimilisfang.
1. Í aðgerðaglugganum velurðu **Vista.**

Eftirfarandi mynd sýnir dæmi um vöruhússvæði.

![Dæmi um vöruhússvæði](media/warehouse-site.png)

## <a name="set-up-a-warehouse"></a>Setja upp vöruhús

Til að setja upp vöruhús skal fylgja þessum skrefum.

1. Í yfirlitsglugganum ferðu í **Einingar \> Retail og Commerce \> Uppsetning rásar \> Vöruhús**.
1. Í aðgerðaglugganum velurðu **Nýtt**.
1. Í reitnum **Vöruhús** slærðu inn gildi.  Ef þetta er 1:1 vörpun í verslun skaltu íhuga að nota heiti verslunarinnar eða nafn svæðisbundinnar dreifingarmiðstöðvar.
1. Í reitinn **Heiti** skal slá inn gildi.
1. Í fellivalmyndinni **Vefsvæði** velurðu vörugeymslusíðuna sem áður var búin til.
1. Í reitnum **Tegund** velurðu **Sjálfgildi**.
    - Ef þú vilt stilla **Biðgeymsluvöruhús** þarftu fyrst að fylgja þessum skrefum til að búa til viðbótar vöruhús þar sem **Gerð** er stillt á **Biðgeymslu**.
    - Ef þú vilt stilla **Flutningsvöruhús** þarftu fyrst að fylgja þessum skrefum til að búa til viðbótar vöruhús þar sem **Gerð** er stillt á **Flutning**.
1. Í aðgerðaglugganum velurðu **Vista.**

## <a name="set-up-inventory-aisles"></a>Setja upp birgðaganga

Til að setja upp birgðaganga skal fylgja þessum skrefum.

1. Í yfirlitsglugganum ferðu í **Einingar \> Retail og Commerce \> Uppsetning rásar \> Uppsetning staðetningar \> Birgðagangar**.
1. Í aðgerðaglugganum velurðu **Nýtt**.
1. Í fellivalmyndinni **Vöruhús** velurðu vöruhúsið sem áður var búið til.
1. Í reitnum **Gangur** skaltu slá inn nafn (til dæmis „Sjálfg“).
1. Í reitnum **Heiti** skaltu slá inn nafn (til dæmis „Sjálfgefinn gangur“).
1. Í aðgerðaglugganum velurðu **Vista.**

## <a name="set-up-warehouse-inventory-locations"></a>Setja upp birgðastaðsetningar vöruhúsa

Fylgdu þessum skrefum til að setja upp birgðastaðsetningar vöruhúss fyrir staðlaðar, skemmdar og skilaðar birgðir.

1. Í yfirlitsglugganum ferðu í **Einingar \> Retail og Commerce \> Uppsetning rásar \> Vöruhús**.
1. Veldu vöruhúsið sem búið var til áður.
1. Í aðgerðaglugganum velurðu **Breyta**.
1. Í aðgerðaglugganum velurðu **Vöruhús** og síðan velurðu **Bigðastaðsetning**.
1. Í aðgerðaglugganum velurðu **Nýtt**. Fellilistinn **Vöruhús** ætti að vera sjálfgefinn í nýja vöruhúsinu.
    1. Í reitinn **Gangur** slærðu inn heiti gangsins sem þú tilgreindir áður. 
    1. Stilltu **Handvirk uppfærsla** á **Já**
    1. Í reitinn **Staðsetning** færirðu heiti vöruhússins inn.
    1. Í aðgerðaglugganum velurðu **Vista.**
 1. Í aðgerðaglugganum velurðu **Nýtt**.  Fellilistinn **Vöruhús** ætti að vera sjálfgefinn í nýja vöruhúsinu.
    1. Í reitinn **Gangur** slærðu inn heiti gangsins sem þú tilgreindir áður.  
    1. Stilltu **Handvirk uppfærsla** á **Já**
    1. Í reitinn **Staðsetning** slærðu inn „Skemmdir“.
    1. Í aðgerðaglugganum velurðu **Vista.**
 1. Í aðgerðaglugganum velurðu **Nýtt**.  Fellilistinn **Vöruhús** ætti að vera sjálfgefinn í nýja vöruhúsinu.
    1. Í reitinn **Gangur** slærðu inn heiti gangsins sem þú tilgreindir áður. 
    1. Stilltu **Handvirk uppfærsla** á **Já**
    1. Í reitinn **Staðsetning** slærðu inn „Skil“.
    1. Í aðgerðaglugganum velurðu **Vista.**
    
Eftirfarandi mynd sýnir uppsetning birgðastaðsetningar vöruhúss í San Francisco.

![Dæmi um uppsetningu birgðastaðsetningar](media/warehouse-inventory-locations.png)
    
## <a name="complete-warehouse-setup"></a>Lokin uppsetning vöruhúss

Fylgið eftirfarandi skrefum til að ljúka uppsetningu vöruhúss.

1. Í yfirlitsglugganum ferðu í **Einingar \> Retail og Commerce \> Uppsetning rásar \> Vöruhús**.
1. Veldu vöruhúsið sem búið var til áður.
1. Í aðgerðaglugganum velurðu **Breyta**.
1. Undir **Birgða- og vöruhúsakerfi**:
    1. Setja **Sjálfgefin staðsetning innhreyfinga** í sjálfgefna staðinn búinn til hér að ofan.
    1. Veldu **Sjálfgefin staðsetning úthreyfinga** í sjálfgefna staðinn búinn til hér að ofan.
1. Undir hlutann **Heimilisföng** slærðu inn heimilisfang vöruhúss.
1. Undir hlutanum **Retail**: 
    1. Í reitinn **Sjálfgefin skilastaðsetning** slærðu inn skilastaðsetningu sem áður var búin til.
    1. Stilltu **Verslun** á **Já**.
    1. Stilltu **þyngd** á **1,00**. 
    1. Í reitinn **Geymsluvídd** slærðu inn sjálfgefna staðsetningu sem áður var búin til.
1. Undir hlutanum **Vöruhús** stillirðu **Efnislega neikvæð birgðastaða** að **Já**.
1. Í aðgerðaglugganum velurðu **Vista.**

Eftirfarandi mynd sýnir upplýsingar um stillt vöruhús.

![Dæmi stillt vöruhús](media/warehouse-sample.png)

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir vöruhúsakerfi](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json)

[Yfirlit yfir rásir](channels-overview.md)

[Skilyrði fyrir rásauppsetningu](channels-prerequisites.md)

[Setja upp smásölurás](channel-setup-retail.md)
    
[Setja upp netrás](channel-setup-online.md)

[Setja upp rás símavers](channel-setup-callcenter.md)





