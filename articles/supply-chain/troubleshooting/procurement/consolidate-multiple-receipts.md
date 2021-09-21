---
title: Ekki er hægt að sameina mörg innhreyfingarskjöl í eina innkaupapöntun
description: Ekki er hægt að sameina mörg innhreyfingarskjöl í eina innkaupapöntun ef mismunandi línur innhreyfingarskjals eru með mismunandi dagsetningar reikningsskila.
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
ms.openlocfilehash: 485306279281ceb55a140526f4216af35574af42
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476629"
---
# <a name="you-cant-consolidate-multiple-product-receipts-into-a-single-purchase-order"></a>Ekki er hægt að sameina mörg innhreyfingarskjöl í eina innkaupapöntun

## <a name="symptoms"></a>Einkenni

Ekki er hægt að sameina mörg innhreyfingarskjöl í eina innkaupapöntun ef mismunandi línur innhreyfingarskjals eru með mismunandi dagsetningar reikningsskila.

## <a name="resolution"></a>Lausn

Í fyrri útgáfum af Dynamics 365 Supply Chain Management var sameining leyfð í þessum aðstæðum. Hins vegar komu oft upp villur þegar það var gert. Dagsetning reikningsskila á innkaupapöntunarlínunum sem eru stofnaðar ættu ekki að vera frábrugðnar dagsetningu reikningsskila í línum innhreyfingarskjals sem þessar innkaupapöntunarlínur voru stofnaðar úr. (Dagsetning reikningsskila á innkaupapöntunarlínum samsvarar dagsetningu reikningsskila í haus innkaupapöntunarinnar.) Þess vegna er sameining margra innhreyfingarskjala í eina innkaupapöntun ekki lengur leyfð.

Dagsetning reikningsskila er notuð, til dæmis fyrir frátektir fjárhagsáætlunar og fjárúthlutunar. Því ætti að halda henni við umbreytingu úr innhreyfingarskjali í innkaupapöntun.
