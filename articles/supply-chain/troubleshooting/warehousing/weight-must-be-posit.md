---
title: Þyngd verður að vera jákvæð
description: Þyngd verður að vera jákvæð
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSContainerCloseDiag_canClose
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: dcbcde3143cb509b68b277cb7c709263e2659b5b
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924304"
---
# <a name="weight-must-be-positive"></a>Þyngd verður að vera jákvæð

Villukóði: WeightMustBePositive

## <a name="symptoms"></a>Einkenni

Kerfið sýnir eftirfarandi villuboð:

> Þyngd verður að vera jákvæð tala.

## <a name="cause"></a>Orsök

Reiturinn **Brúttóþyngd** er stilltur á *0* (núll) eða neikvætt gildi.

## <a name="resolution"></a>Upplausn

Fylgið einu af eftirfarandi skrefum til að tilgreina þyngd.

- Stillið gildi á reitnum **Brúttóþyngd**. Veljið síðan einingu í fellilistanum.
- Veldu **Sækja kerfisþyngd** til að reikna út **Brúttóþyngd**.
