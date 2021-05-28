---
title: Seint val er ekki virt þegar framleiðslupantanir eru endurstilltar í runuvinnslu
description: Þegar þú notar endurtekna runuvinnslu til að endurstilla stöðu framleiðslupöntunar eru seint val ekki virt.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: e53198f427f4060421a4f0078277682c43db1320
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026603"
---
# <a name="late-selection-isnt-respected-when-production-orders-are-reset-via-a-batch-job"></a>Seint val er ekki virt þegar framleiðslupantanir eru endurstilltar í runuvinnslu

KB númer: 4614634

## <a name="symptoms"></a>Einkenni

Þegar þú notar endurtekna runuvinnslu til að endurstilla stöðu framleiðslupöntunar eru seint val ekki virt.

## <a name="resolution"></a>Upplausn

Núgildandi hönnun styður ekki notkun síðara vals fyrir ferlið *Endurstilla stöðuna*.
