---
title: Tilgreina þarf númeraplötu fyrir þessa staðsetningu
description: Ef þú færð þessa villu eftir að hafa búið til flutningspöntun fyrir vöruhús virkjað af vöruhúsakerfi er sjálfgefin staðsetning innhreyfingar auð fyrir flutningsvöruhús.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 2e562ad2b41dd149f215adc83bd2d54e55dccc05
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476627"
---
# <a name="license-plate-specification-error-when-confirming-shipment-for-a-transfer-order"></a>Villa við skilgreiningu á númeraplötu við staðfestingu á sendingu fyrir flutningspöntun

## <a name="symptoms"></a>Einkenni

Ef flutningspöntun er stofnuð með því að nota vöruhús sem er virkt fyrir ítarlega vöruhúsastjórnun (WMS), og svo er reynt að staðfesta sendinguna eftir að vinnu er lokið, gætir þú fengið eftirfarandi villuboð:

> Tilgreina þarf númeraplötu fyrir þessa staðsetningu.

## <a name="cause"></a>Orsök

Þetta gerist vegna þess að reiturinn **Sjálfgefin staðsetning innhreyfinga** er auður fyrir flutningsvöruhús „úr“ vöruhúsi.

## <a name="resolution"></a>Lausn

Til að laga þetta vandamál þarf að tilgreina sjálfgefna staðsetningu móttöku í flutningsvöruhúsinu. Ganga skal úr skugga um að þessi staðsetning sé númeraplötustýrð.
