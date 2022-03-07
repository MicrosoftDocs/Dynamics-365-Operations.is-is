---
title: Fylgiskjalsnúmer innhreyfingarskjals er notað þótt fylgiskjal sé ekki myndað
description: Fylgiskjalsnúmer innhreyfingarskjals er notað þótt ekkert fjárhagsskjal sé búið til við móttöku afurðar
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
ms.openlocfilehash: 0556969950c45e80d177a0e96096c4157d690ae3
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476654"
---
# <a name="a-product-receipt-voucher-number-is-consumed-even-when-not-generating-a-voucher"></a>Fylgiskjalsnúmer innhreyfingarskjals er notað þótt fylgiskjal sé ekki myndað

## <a name="symptoms"></a>Einkenni

Fylgiskjalsnúmer innhreyfingarskjals er notað þótt ekkert fjárhagsskjal sé búið til við móttöku afurðar.

## <a name="resolution"></a>Lausn

Ef valkosturinn **Safna upp skuld á innhreyfingarskjali** er stilltur á *Nei* fyrir vörulíkanaflokkinn, munu engar bókanir á fjárhagnum eiga sér stað. Efnislegt tilvik verður hins vegar skráð af bókhaldsástæðum í undirbók og þetta tilvik þarf fylgiskjalsnúmer. Þetta fylgiskjalsnúmer er það fylgiskjalsnúmer sem vísað er til í birgðafærslum.

Mælt er með því að valkosturinn **Safna upp skuld á innhreyfingarskjali** sé stilltur á *Já* eins og lýst er í eftirfarandi bloggfærslu: [Bóka ýmis gjöld þegar afurð er móttekin](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).
