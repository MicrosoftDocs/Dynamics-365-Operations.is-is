---
title: Hægt er að bóka færslur á frestaðan fjárhagslykil
description: Ef hætt er við innhreyfingarskjal, gerir kerfið kleift að bóka færslur á frestaða fjárhagslykla jafnvel þótt aðallyklum sé frestað
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 20df0ee4107ad62bec0dd9a683660fe2375a3dd1
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476708"
---
# <a name="transactions-can-be-posted-to-a-suspended-ledger-account"></a>Hægt er að bóka færslur á frestaðan fjárhagslykil

## <a name="symptoms"></a>Einkenni

Ef hætt er við innhreyfingarskjal, gerir kerfið kleift að bóka færslur á frestaða fjárhagslykla jafnvel þótt aðallyklum sé frestað.

## <a name="reproduce-the-issue"></a>Framkallaðu vandamálið

Eftirfarandi ferli sýnir eina leið til að endurtaka málið.

1. Á síðunni **Færibreytur viðskiptaskulda**, í flipanum **Almennt**, skal ganga úr skugga um að valkosturinn **Bóka innhreyfingarskjal afurða í fjárhag** sé stilltur á *Já*.
1. Stofnið innkaupapöntun og bætið við pöntunarlínu sem er með magnið *1000* fyrir afurð.
1. Staðfesta innkaupapöntun.
1. Bókið innhreyfingarskjalið og athugið fylgiskjölin.
1. Frestið viðkomandi aðallyklum, *200140* og *140200*.
1. Hættið við bókað innhreyfingarskjal afurðar.
1. Takið eftir að hægt er að bóka færslur á frestaða fjárhagslykla.

## <a name="resolution"></a>Lausn

Hægt er að bóka færslur á frestaða fjárhagslykla þegar hætt er við innhreyfingarskjöl vegna þess að þessi hegðun leyfir réttar bókanir.
