---
title: Staðsetning víddar má ekki vera auð ef raðnúmer er stillt
description: Ef þú færð þessa villu þegar sending er staðfest eftir að hafa búið til flutningspöntun fyrir vöru með raðnúmeri verður reiturinn Sjálfgefin staðsetning innhreyfingar auður.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 6f58c72438d5d1d93e59e46525debd65d44d9a76
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476696"
---
# <a name="error-when-confirming-shipment-after-creating-a-transfer-order-for-a-serial-item"></a>Villa við staðfestingu á sendingu eftir að hafa búið til flutningspöntun fyrir vöru með raðnúmer

## <a name="symptoms"></a>Einkenni

Ef flutningspöntun fyrir vöru með raðnúmeri er stofnuð með því að nota vöruhús sem er virkt fyrir ítarlega vöruhúsastjórnun (WMS), og svo eftir að vinnu er lokið skaltu reyna að staðfesta sendinguna, færðu eftirfarandi villuboð:

> Víddarstaðsetning má ekki vera skilin eftir auð ef raðnúmersvídd er stillt.

## <a name="cause"></a>Orsök

Þetta gerist vegna þess að reiturinn **Sjálfgefin staðsetning innhreyfinga** er auður fyrir flutningsvöruhús „úr“ vöruhúsi.

## <a name="resolution"></a>Lausn

Til að laga þetta vandamál þarf að tilgreina sjálfgefna staðsetningu móttöku í flutningsvöruhúsinu. Ganga skal úr skugga um að þessi staðsetning sé númeraplötustýrð.
