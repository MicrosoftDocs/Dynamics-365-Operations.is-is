---
title: Magn í biðgeymslupöntun í vinnslu uppfærist ekki þegar pöntuninni er skipt
description: Þegar biðgeymslupöntun er stofnuð og reynt að skipta henni er pöntunarmagnið ekki uppfært í það magn sem eftir er af pöntuninni.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: shawan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: a8af535257ce217629d5ba92e624623c3ea39345
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026622"
---
# <a name="quantity-on-a-started-quarantine-order-isnt-updated-when-the-order-is-split"></a>Magn í biðgeymslupöntun í vinnslu uppfærist ekki þegar pöntuninni er skipt

KB númer: 4613113

## <a name="symptoms"></a>Einkenni

Þegar biðgeymslupöntun er stofnuð og reynt að skipta henni er pöntunarmagnið ekki uppfært í eftirstöðvarnar eftir skiptinguna.

## <a name="resolution"></a>Upplausn

Kerfið breytir ekki upprunalegu magni úr biðgeymslupöntun til að tryggja að hægt sé að rekja upprunalegt magn sem búið var til fyrir þá biðgeymslupöntun. Kerfið fylgist hins vegar ekki með magninu sem skipt er úr biðgeymslupöntun. Þetta er gert með gagnagrunnsreit sem kallast `QuantityThatHasSplitIntoOtherQuarantineOrders`. Þessi reitur er þó ekki sýnilegur í notandaviðmótinu.
