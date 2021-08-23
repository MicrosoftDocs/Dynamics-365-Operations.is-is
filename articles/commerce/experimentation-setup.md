---
title: Setja upp tilraun
description: Í þessu efnisatriði er lýst hvernig á að setja upp tilraun í þjónustu þriðja aðila.
author: sushma-rao
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 870bcb9cc63fd4dbf6d7b40d730edfad7783540d5d943896e0129d29572fa875
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6769396"
---
# <a name="set-up-an-experiment"></a>Setja upp tilraun

Þegar búið er að [skilgreina og ákvarða hvaða árangursmælingar á að nota](experimentation-identify.md) þarf að setja upp tilraunina í þjónustu þriðja aðila. Eftirfarandi skýringarmynd sýnir öll skrefin sem taka þátt í uppsetningu og vinnslu á tilraun á vefsvæði rafrænna viðskipta í Dynamics 365 Commerce. Önnur skref eru afgreidd í aðskildum efnisatriðum.

[ ![Tilraunaferli notanda - Uppsetning.](./media/experimentation_setup.svg) ](./media/experimentation_setup.svg#lightbox)


## <a name="set-up-your-experiment-in-the-third-party-service"></a>Setja upp tilraun í þjónustu þriðja aðila
Nú ætti að vera búið að velja þjónustu þriðja aðila til að keyra og fylgjast með tilrauninni og setja upp tengil tilraunarinnar. Þessi skilyrði eru skráð í [Tilraunagerð í Dynamics 365 Commerce](experimentation-overview.md).

Fylgið skrefunum sem þarf til að búa til tilraunir í þjónustu þriðja aðila. Ef tengillinn er skilgreindur á réttan hátt verður fullbúinn listi yfir allar tilraunir sem settar eru upp í þjónustu þriðja birtur í vefsmið Commerce innan 5 mínútna.

## <a name="set-up-your-success-metrics"></a>Setja upp árangursmælingar
Sérhver tilraun þarf mælingar til að mæla áhrif afbrigðanna og til að sannprófa tilgátuna. Fylgið skrefunum hér að neðan til að virkja útreikning á mælingum í þjónustu þriðja aðila með virkum tilvikum fjarmælinga úr Dynamics 365 Commerce.

Til að setja upp árangursmælingar skaltu fylgja þessum skrefum.

1. Í vefsmið Commerce skal velja **Síður** á vinstra yfirlitssvæðinu og síðan velja síðuna sem á að safna mælingum fyrir. 
1. Farið í hlutann **Kenni tilvika til að fylgjast með** á eiginleikasvæðinu hægra megin á síðunni eða einingunni sem á að fylgjast með.
1. Velja **Skoða**. Listi yfir öll tilvikskenni birtist. Afritið tilvikið sem á að rekja, og límið tilvikslykilinn á tilgreindan stað í þjónustu þriðja aðila. Ef þörf er á fleiri en einu tilviki skal afrita lyklana einn í einu. 
    - Til að fá upplýsingar um öll tiltæk tilvik og eigindir, þar á meðal síðuyfirlit og tekjurakningu, skal skoða [Tilvik Commerce-íhluta fyrir greiningu og bilanaleit](dev-itpro/retail-component-events-diagnostics-troubleshooting.md).
1. Farið í gegnum öll önnur skref til að rekja mælingar eins og krafist er í þjónustu þriðja aðila.

## <a name="previous-step"></a>Fyrra skref
[Auðkenna tilgátu og ákvarða mælieiningar fyrir tilraun](experimentation-identify.md) 


## <a name="next-step"></a>Næsta skref
[Tengja og breyta tilraun](experimentation-connect-edit.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]