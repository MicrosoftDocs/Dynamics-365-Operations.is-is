---
title: Skipuleggja þarf áætluðu framleiðslupöntunina áður en hægt er að staðfesta hana.
description: Þegar reynt er að festa áætlaða pöntun berast villuboð sem segja að áætla þurfi pöntunina áður en hægt er að staðfesta hana.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a89f5f98895be5b934dbdc1194fa58b9af34f9cbc7f5e2092f6f47791dd52400
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6777744"
---
# <a name="planned-production-order-must-be-scheduled-before-it-can-be-firmed"></a>Skipuleggja þarf áætluðu framleiðslupöntunina áður en hægt er að staðfesta hana.

Villukóði SYS309802

## <a name="symptoms"></a>Einkenni

Þegar reynt er að fastsetja áætlaða pöntun berast eftirfarandi villuboð:

> Skipuleggja þarf áætluðu framleiðslupöntunina áður en hægt er að staðfesta hana.

## <a name="cause"></a>Orsök

Áætlaðar upphafs- og lokadagsetningar mega ekki vera auðar.

## <a name="resolution"></a>Lausn

Til að tilgreina upphafs- og lokadagsetningu áætlaðrar pöntunar skal fylgja þessum skrefum.

1. Fara í **Áætlanagerð \> Aðaláætlanagerð \> Áætlaðar pantanir**.
1. Opnið viðeigandi áætlaða pöntun.
1. Í flýtiflipanum **Almennt**, í hlutanum **Á áætlun**, skal tilgreina dagsetningar í reitunum **Upphafsdagsetning** og **Lokadagsetning**.
