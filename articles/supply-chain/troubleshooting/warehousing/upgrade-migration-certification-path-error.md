---
title: Villa í vottunarslóð við að uppfæra eða flytja í WMS
description: Ef forritið sýnir villuna „Traustakkeri fyrir slóð vottorðs finnst ekki“ við uppfærslu eða flutning á vöruhúsakerfi veitir þessi síða upplýsingar um hvernig leysa má vandamálið.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 2cff41455268c43bdd99e285b9675f0c69be7de7
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476634"
---
 # <a name="trust-anchor-for-certification-path-not-found-when-updating-and-migrating-to-wms"></a>Traustakkeri fyrir slóð vottorðs fannst ekki við uppfærslu og flutning í vöruhúsakerfi

## <a name="symptoms"></a>Einkenni

Við uppfærslu og flutning yfir í háþróað vöruhúsakerfi kann vöruhúsastjórnunarforritið að sýna þér eftirfarandi villuboð:

> java.security.cert.certPathValidatorException: Traustakkeri fyrir slóð vottorðs finnst ekki.

## <a name="cause"></a>Orsök

Þetta gerist vegna þess að sjálfsafgreiddum skírteinum er ekki treyst á Android 8 + í innanhússumhverfi.

## <a name="resolution"></a>Lausn

Nota ytri (opinberan) útgefanda vottorðs (CA). Lausn fyrir þetta vandamál er í boði í útgáfu 1.9.0.0 af vöruhúsastjórnunarforritinu. Frekari upplýsingar um þetta vandamál og lausnir við því er að finna í [Traustakkeri fyrir slóð vottorðs finnst ekki þegar forritstenging er sett upp](certification-path-app-connection-error.md).
