---
title: Ekki er hægt að losa farm fyrir hlutamagn með stigveldi runu fyrir ofan
description: Þegar notuð er vara með lotubundið frátekningastigveldi verða farmlínur að tilgreina víddir fyrir ofan staðsetningu til að hægt sé að úthluta birgðum.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: eb7e71cc271903cb689c33777b72862246f2dd42
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476635"
---
# <a name="cant-release-a-load-for-partial-quantity-with-batch-above-reservation-hierarchy"></a>Ekki er hægt að losa farm fyrir hlutamagn með frátekningastigveldi runu fyrir ofan

## <a name="symptoms"></a>Einkenni

Þegar notuð er vara með *runa fyrir ofan* frátekningastigveldi mun skipunin **Losa í vöruhús** á síðunni **Vinnusvæði hleðsluáætlunar** ekki virka ef reynt er að losa hleðslu fyrir hlutamagn. Eftirfarandi villuboð berast:

> Til að úthluta bylgju verða hleðslulínur að tilgreina víddirnar fyrir ofan staðsetninguna. Til að úthluta þessum víddum skal taka hleðslulínuna frá og endurgera hana.

Hins vegar, þegar notuð er vara sem er með *runa fyrir neðan* frátekningastigveldi, er hægt að losa hleðslu fyrir hlutamagn á síðunni **Vinnusvæði hleðsluáætlunar**.

## <a name="cause"></a>Orsök

Þegar vídd er fyrir ofan víddina **Staðsetning** er sett upp í frátekningarstigveldi verður að tilgreina hana áður en hún er losuð í vöruhúsið. Aðeins er hægt að úthluta birgðum ef engar eyður eru í víddunum fyrir ofan staðsetningu.

## <a name="resolution"></a>Lausn

Gakktu úr skugga um að öllum víddum fyrir ofan **staðsetningu** hafi verið úthlutað með því að taka farmlínuna frá og gera hana aftur.
