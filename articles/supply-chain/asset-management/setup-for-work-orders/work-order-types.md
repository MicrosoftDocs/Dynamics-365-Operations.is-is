---
title: Gerðir verkbeiðni
description: Þetta efni útskýrir gerðir verkbeiðna í eignastýringu.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderType
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b8e43908e3f13c9e4fd6fab6f1e17a171866b803
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430437"
---
# <a name="work-order-types"></a>Gerðir verkbeiðni

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

8. Veljið **Vista**.

![Gerðir verkbeiðni](media/16-setup-for-work-orders.png)
