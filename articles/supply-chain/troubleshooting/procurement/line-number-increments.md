---
title: Innfluttar innkaupapantanir sýna röng línunúmer
description: Þegar innkaupapantanir eru fluttar inn í gegnum gagnastjórnun, fylgja númer innkaupapöntunarlínu ekki hækkun sem er skilgreint í kerfisfæribreytum
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
ms.openlocfilehash: e1cf5cf1d04824213f495ac3ebf556796c96611a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476615"
---
# <a name="imported-purchase-orders-show-incorrect-line-numbers"></a>Innfluttar innkaupapantanir sýna röng línunúmer

## <a name="symptoms"></a>Einkenni

Sjálfgefið er að línunúmer sem eru búin til sjálfkrafa fyrir innkaupapöntunarlínur sem eru fluttar inn í gegnum gagnaeininguna *Innkaupapöntunarlínur V2* noti ekki línunúmerahækkun kerfisins sem er tilgreind í kerfisfæribreytum. Ef innkaupapöntun er búin til handvirkt og línum bætt við í gegnum notandaviðmótið, hækka línunúmerin á réttan hátt. Hins vegar ef gagnastjórnunarramminn (DMF) er notaður, hækka þau ekki á réttan hátt.

Þetta vandamál á sér stað vegna þess að þegar innflutningslínur eru fluttar inn í gegnum DMF, ef línunúmerum hefur ekki þegar verið úthlutað á innflutta einingu, notar kerfið DMF-aðferð til að úthluta þeim. Línunúmer hækka alltaf um einn með þessari aðferð.

## <a name="workaround"></a>Hjáleið

Gangið úr skugga um að æskileg línunúmer séu þegar gefin upp í línunúmerareitum gagnaeiningarinnar þegar innkaupapöntunarlínurnar eru fluttar inn. Í þessu tilfelli skrifar DMF ekki yfir línunúmerin.
