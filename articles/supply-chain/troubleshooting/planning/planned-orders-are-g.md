---
title: Aðaláætlanagerð býr til áætlaðar pantanir fyrir skuggaafurðir
description: Áætlaðar pantanir eru stofnaðar fyrir skuggaafurðir eftir að aðaláætlanagerð er keyrð.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: anderso
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: f3170bcb723e2d7483258bb0ecf786e62f2aa3d196745074c2ac554bc212ec55
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6742005"
---
# <a name="master-planning-generates-planned-orders-for-phantom-products"></a>Aðaláætlanagerð býr til áætlaðar pantanir fyrir skuggaafurðir

KB númer: 4614729

## <a name="symptoms"></a>Einkenni

Áætlaðar pantanir eru stofnaðar fyrir skuggaafurðir eftir að aðaláætlanagerð er keyrð.

## <a name="resolution"></a>Upplausn

Stilling **Phantom** valkostsins fyrir útgefnar vörur ákvarðar sjálfgefna línutegund á uppskriftinni. Þegar valkosturinn **Skuggi** er stilltur á *Já* mun kerfið enn búa til áætlaðar pantanir fyrir atriðið en valkosturinn **Beint afleidd þörf** fyrir hverja skipulagða pöntun verður stilltur á *Já*. Því er ekki hægt að staðfesta áætlaða framleiðslupöntun eina og sér. Þess í stað verður hann alltaf sjálfvirkt innifalinn þegar yfirframleiðslupöntun er staðfest. Að auki verða styttri línur fyrirhugaðrar skuggapöntunar teknar með í uppskrift yfirframleiðslupöntunar.
