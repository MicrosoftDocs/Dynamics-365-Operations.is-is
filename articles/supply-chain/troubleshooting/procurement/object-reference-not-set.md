---
title: Villan „Tilvísun hlutar ekki stillt“ kemur upp við staðfestingu á innkaupapöntun
description: Villan „Tilvísun hlutar ekki stillt“ kemur upp við staðfestingu á innkaupapöntun
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 78e5e365f7197c1a0c25bf6eb63bcd5bd0f482ed
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476681"
---
# <a name="error-object-reference-not-set-occurs-during-purchase-order-confirmation"></a>Villan „Tilvísun hlutar ekki stillt“ kemur upp við staðfestingu á innkaupapöntun

## <a name="symptoms"></a>Einkenni

Eftirfarandi undantekning kemur upp þegar innkaupapöntun er staðfest:

> Tilvísun hlutar ekki stillt

## <a name="cause"></a>Orsök

Þetta vandamál getur komið upp vegna ósamræmis í dreifingum innkaupapantana.

## <a name="resolution"></a>Lausn

Til að afblokka þetta vandamál og endurstilla innkaupapöntunina á stöðuna *Drög* skal fara í **Innkaup og aðföng \> Reglubundnar vinnslur \> Hreinsun \> Endurstilling á dreifingu innkaupapöntunar**. Frekari upplýsingar er að finna í eftirfarandi bloggfærslu: [Leysa úr dreifingarvillum innkaupapöntunar í Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).
