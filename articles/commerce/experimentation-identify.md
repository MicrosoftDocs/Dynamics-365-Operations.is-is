---
title: Auðkenna tilgátu og ákvarða mælieiningar fyrir tilraun
description: Þessi grein lýsir því hvernig á að bera kennsl á tilgátu og árangursmælikvarða fyrir tilraun sem þú munt keyra á netverslunarvef í Dynamics 365 Commerce.
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
ms.openlocfilehash: 0b6bdf160522fc93e841ec2f8a4542ff80d8f67f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852787"
---
# <a name="identify-a-hypothesis-and-determine-success-metrics-for-an-experiment"></a>Auðkenna tilgátu og ákvarða árangursmælingar fyrir tilraun
Fyrsti áfangi í tilraunaferlinu felur í sér að auðkenna tilgátu tilraunarinnar og ákvarða mælieiningarnar sem fylgst verður með til að meta árangur. Eftirfarandi skýringarmynd sýnir öll skrefin sem taka þátt í [uppsetningu og vinnslu á tilraun](experimentation-overview.md) á vefsvæði rafrænna viðskipta í Dynamics 365 Commerce. Fjallað er um fleiri skref í aðskildum greinum. 

[ ![Tilraunaferli notanda - Auðkenna.](./media/experimentation_identify.svg) ](./media/experimentation_identify.svg#lightbox)

Tilgáta er yfirlýsing þar sem þú spáir fyrir um útkomu tilraunarinnar. Margir þættir koma við sögu þegar tilgáta er skilgreind, t.d. rannsóknir á hegðun notanda og gögn vefsvæðis sem safnað hefur verið saman. Með tilgátunni skilgreinir þú þá forsendu eða kenningu sem þú vilt sannprófa með tilrauninni. Dæmi um tilgátu fyrir tilraunina gæti verið að „*mynd af hvítum stuttermabol á heimasíðunni minni mun auka fjölda smella frekar en dökkblá peysa yfir sumarmánuðina vegna þess að fólk vill klæðast einhverju léttu og í ljósum litum yfir sumartímann.*“ Í slíku tilfelli býrðu til afbrigði sem innihalda hvítan stuttermabol og dökkbláa peysu og gefur bæði út á sama tíma.

Til að sannprófa tilgátu ætti velgengni eða mislukkun tilraunar að vera tengd beint við aðgerðir notanda; til dæmis hvort notandi vefsvæðisins smellir á tengil eða hnapp. Þessar aðgerðir verða að samsvara tilvikum sem þjónusta þriðja aðila sem fylgir tilrauninni eftur verður tilkynnt um. Með tímanum verður hlutfall notenda sem grípa til aðgerðarinnar gefið upp sem mælieining sem hægt er að nota til að búa til skýrslur og gera greiningar. Til að skoða öll tilvik og eiginleika skal skoða [Tilvik Commerce-íhluta fyrir greiningu og bilanaleit](dev-itpro/retail-component-events-diagnostics-troubleshooting.md).

## <a name="previous-step"></a>Fyrra skref
[Tilraunir í Dynamics 365 Commerce](experimentation-overview.md)


## <a name="next-step"></a>Næsta skref
[Setja upp tilraun](experimentation-setup.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]