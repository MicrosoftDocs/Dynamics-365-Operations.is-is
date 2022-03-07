---
title: Það tekur langan tíma að uppfæra áætlaðar pantanir
description: Þegar þarfamagn og/eða afhendingardagsetning áætlaðrar pöntunar er uppfært tekur a.m.k. 30 sekúndur að vista uppfærsluna á pöntun
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
ms.openlocfilehash: ccf3305cc18ea0ccf2ac3e9ca0dd507fd12a9da7
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476673"
---
# <a name="planned-orders-take-a-long-time-to-update"></a>Það tekur langan tíma að uppfæra áætlaðar pantanir

## <a name="symptoms"></a>Einkenni

Þegar þarfamagn og/eða afhendingardagsetning áætlaðrar pöntunar er uppfært tekur a.m.k. 30 sekúndur að vista uppfærsluna á pöntun.

## <a name="resolution"></a>Lausn

Þetta er þekkt vandamál með innbyggðri aðaláætlunarvél. Slíkt stafar af undirliggjandi, sjálfvirku niðurbroti í skipulagi uppskriftarinnar á meðan breytingar eru gerðar. Slíkt vandamál er leyst með fínstillingu skipulagningar, þar sem áætlun getur uppfært og samþykkt viðeigandi pantanir og þegar þess er óskað, keyrt uppfærslu áætlaðra pantana fyrir undirliggjandi skipan uppskrifta.

Ein leið til að auka afköst með innbyggðri aðaláætlunarvél er að gera eftirfarandi skref:

1. Farið í **Aðaláætlanagerð \> Uppsetning \> Áætlanir \> Aðaláætlanir**.
1. Velja áætlun.
1. Víkka út flipann **Tímamörk í dögum**.
1. Stilltu **Niðurbrot** á *Já* og stilltu svæðið fyrir neðan þessa stillingu á 0 (núll).

> [!NOTE]
> Slíkt takmarkar framkvæmdartímabil niðurbrota fyrir þessa aðaláætlun við einn dag.
