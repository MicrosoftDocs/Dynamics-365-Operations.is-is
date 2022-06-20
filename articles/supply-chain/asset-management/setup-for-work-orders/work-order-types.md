---
title: Gerðir vinnupöntunar
description: Þessi grein útskýrir gerðir verkbeiðna í eignastýringu.
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderType
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 12745960f903ebc14208f2c8a01f076ed27a38d3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8891177"
---
# <a name="work-order-types"></a>Gerðir vinnupöntunar

[!include [banner](../../includes/banner.md)]

 

Verkbeiðnagerðir eru notaðar til að flokka verkbeiðnir. Til dæmis gætir þú verið með verkbeiðnir sem tengjast fyrirbyggjandi viðhaldi eða leiðréttandi viðhaldi.

Gerð verkbeiðni skilgreinir tengsl við líftímalíkan verkbeiðni. Líftímalíkan verkbeiðni skilgreinir þá líftímastöðu verkbeiðni sem er hægt að stilla á verkbeiðni. (Dæmi um líftímastöður verkbeiðna eru **Stofnað**, **Í ferli** og **Lokið**.)

Nánari upplýsingar um líftímastöður verkbeiðna og verkefnastig, sjá [Líftímastöður verkbeiðna](work-order-lifecycle-states.md).

1. Veldu **Eignastjórnun** \> **Uppsetning** \> **Verkbeiðnir** \> **Gerðir verkbeiðna**.
2. Smellið á **Nýtt** til að stofna nýja gerð verkbeiðni.
3. Í reitnum **Gerð verkbeiðni** skal slá inn auðkenni fyrir gerð verkbeiðni.
4. Færið inn lýsandi nafn í reitinn **Heiti**.
5. Í reitnum **Líftímalíkan verkbeiðni** skaltu velja líftímalíkan.
5. Stilltu valkostinn **Einn viðhaldsstarfsmaður** á **Já** ef öll verkbeiðniverk sem tengjast verkbeiðni af þessari gerð ættu að vera áætluð til sama viðhaldsstarfsmanns.
6. Í reitnum **Gerð kostnaðar** velurðu **Leiðrétting**, **Fyrirbyggjandi** eða **Fjárfesting**, eftir því sem við á. Öll verkbeiðniverk í verkbeiðni verða að hafa sömu kostnaðartegund.
7. Í hlutanum **Skylda** stillirðu viðeigandi valkosti á **Já** til að tilgreina hvaða bilanatengdar eða niðurtíma vegna viðhalds-tengdar upplýsingar er bætt við verkbeiðni af þessari gerð.

    > [!NOTE]
    > Valkostirnir í hlutanum **Skylda** tengjast valkostunum á flýtiflipanum **Staðfesta** á síðunni **Líftími verkbeiðna** (**Eignastýring** \> **Uppsetning** \> **Verkbeiðnir** \> **Líftímastöður**).

8. Veldu **Vista**.

![Verkbeiðnigerðir.](media/16-setup-for-work-orders.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]