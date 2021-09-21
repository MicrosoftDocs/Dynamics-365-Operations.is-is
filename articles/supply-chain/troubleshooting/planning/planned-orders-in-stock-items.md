---
title: Áætlaðar pantanir eru myndaðar fyrir vörur á lager með framleiðslupöntunum
description: Áætlaðar pantanir eru myndaðar þrátt fyrir að vörur séu á lager og framleiðslupantanir séu þegar til fyrir þær
author: ChristianRytt
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: aa803bcd7d43aa36675596050ccbe06831f1724d
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476709"
---
# <a name="planned-orders-are-generated-for-in-stock-with-production-orders"></a>Áætlaðar pantanir eru myndaðar fyrir vörur á lager með framleiðslupöntunum

## <a name="symptoms"></a>Einkenni

Áætlaðar pantanir eru myndaðar þrátt fyrir að vörur séu á lager og framleiðslupantanir séu þegar til fyrir þær.

## <a name="resolution"></a>Lausn

Hugsanlega er hægt að laga vandamálið með því að auka gildið **Jákvæðir dagar** fyrir viðeigandi flokka á síðunni **Þekjuflokkur**. Þessi breyting veldur því að kerfið ákveður hvort hægt er að nota lagerbirgðir til að anna eftirspurn. Þá verður ný áætluð pöntun ekki mynduð fyrir vörurnar sem eru í birgðum.
