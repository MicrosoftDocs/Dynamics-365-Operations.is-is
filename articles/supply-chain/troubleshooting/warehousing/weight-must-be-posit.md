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
ms.openlocfilehash: 27ec37e0c0644ff10ece4626d5c136bca3c52ef12f1c6de947afd03003a5368a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6776777"
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
