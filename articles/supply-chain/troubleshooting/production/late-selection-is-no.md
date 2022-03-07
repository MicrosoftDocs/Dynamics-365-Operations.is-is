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
ms.openlocfilehash: 8800ec411ddd7ae73c5ac159592620a07b50c1e87938f823274ec24062c9a71a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6741957"
---
# <a name="late-selection-isnt-respected-when-production-orders-are-reset-via-a-batch-job"></a>Seint val er ekki virt þegar framleiðslupantanir eru endurstilltar í runuvinnslu

KB númer: 4614634

## <a name="symptoms"></a>Einkenni

Þegar þú notar endurtekna runuvinnslu til að endurstilla stöðu framleiðslupöntunar eru seint val ekki virt.

## <a name="resolution"></a>Upplausn

Núgildandi hönnun styður ekki notkun síðara vals fyrir ferlið *Endurstilla stöðuna*.
