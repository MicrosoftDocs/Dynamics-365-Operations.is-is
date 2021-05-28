---
title: Skýrslan „Óbeinn kostnaður í vinnslu“ inniheldur framleiðslupantanir sem var eytt
description: Óbeinn kostnaður í ferli skýrslan birtir upplýsingar um framleiðslupantanir sem voru unnin að hluta til og síðar eytt.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdIndirectCostInProgress
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 707fa9bb30129c3656e10c6756dee770a7712e65
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026610"
---
# <a name="the-indirect-costs-in-process-report-includes-deleted-production-orders"></a>Skýrslan „Óbeinn kostnaður í vinnslu“ inniheldur framleiðslupantanir sem var eytt

KB númer: 4612748

## <a name="symptoms"></a>Einkenni

**Óbeinn kostnaður í ferli** skýrslan birtir upplýsingar um framleiðslupantanir sem voru unnin að hluta til og síðar eytt.

## <a name="resolution"></a>Upplausn

Þegar framleiðslupöntun er afturkölluð eru allar færslur framleiðslupöntunar einnig afturkallaðar. Þegar framleiðslupöntuninni er eytt eru allar töflur undirbókar og fjárhags áfram til staðar. Skýrslurnar sýna færslurnar í töflum undirbókar. Nettóverðmætið ætti að vera 0,00 fyrir tilteknu framleiðslupöntunina.
