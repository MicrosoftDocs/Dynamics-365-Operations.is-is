---
title: Undantekning á sér stað þegar reikningur lánardrottins er bókaður
description: Undantekningin „Exception has been thrown by the target of an invocation“ kemur upp við bókun lánardrottnareiknings.
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
ms.openlocfilehash: ecc63cb7d0d2392105d8e4290f8e837945ae0781
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476656"
---
# <a name="an-exception-occurs-during-vendor-invoice-posting"></a>Undantekning á sér stað þegar reikningur lánardrottins er bókaður


## <a name="symptoms"></a>Einkenni

Þú færð eftirfarandi undantekningu þegar lánardrottnareikningur er bókaður:

> Undantekning hefur verið sett fram af markhluta sem var ræstur

## <a name="cause"></a>Orsök

Þetta vandamál getur komið upp vegna ósamræmis í dreifingum innkaupapantana.

## <a name="resolution"></a>Lausn

Til að afblokka þetta vandamál og endurstilla innkaupapöntunina á stöðuna *Drög* skal fara í **Innkaup og aðföng \> Reglubundnar vinnslur \> Hreinsun \> Endurstilling á dreifingu innkaupapöntunar**. Frekari upplýsingar er að finna í eftirfarandi bloggfærslu: [Leysa úr dreifingarvillum innkaupapöntunar í Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).
