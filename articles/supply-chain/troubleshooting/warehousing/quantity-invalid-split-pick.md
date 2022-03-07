---
title: Magn er ekki gilt fyrir einingu %1 þegar tiltekt er skipt niður
description: Þegar framkvæmd er tiltekt sem hefur verið skipt niður í margar runur gætir þú fengið upp villu um að magnið sé ekki gilt fyrir einingu %1. Þessi síða hjálpar til við að leysa vandamálið.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 4627db7400d6ccd81f25f100de4696058ce35c42
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476617"
---
# <a name="quantity-is-not-valid-when-performing-a-split-pick-across-multiple-batches"></a>Magn er ekki gilt þegar tiltekt er skipt á milli margra runa

## <a name="symptoms"></a>Einkenni

Þegar þú reynir að framkvæma *skipta tiltekt* í mörgum runum færðu eftirfarandi villuboð:

> Magnið er ekki gilt fyrir einingu %1.

## <a name="resolution"></a>Lausn

Starfskraftur í vöruhúsi verður að nota ferlið *Stutt tiltekt* í Warehouse Management-farsímaforriti. Ef reynt er að taka til margar runur úr sömu staðsetningunni er einnig hægt að nota valkostinn **Full** í forritinu.
