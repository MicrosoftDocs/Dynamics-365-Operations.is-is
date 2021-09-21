---
title: Afturkallaðar innkaupapantanir birtast í listanum yfir drög á vinnusvæðinu
description: Afturkallaðar innkaupapantanir birtast í listanum yfir drög á undirbúningssvæði innkaupapöntunar
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
ms.openlocfilehash: f1dc23cd7e5b4b99cb7a9440d7d4666d8396511f
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476682"
---
# <a name="canceled-purchase-orders-appear-in-the-draft-list-in-the-workspace"></a>Afturkallaðar innkaupapantanir birtast í listanum yfir drög á vinnusvæðinu

## <a name="symptoms"></a>Einkenni

Þegar búið er að hætta við innkaupapantanir sem voru með stöðuna *Staðfest*, sjást afturkölluðu innkaupapantanir ennþá í listanum yfir drög að innkaupapöntunum á vinnusvæðinu **Undirbúningur innkaupapöntunar**.

## <a name="resolution"></a>Lausn

Þetta vandamál á sér aðeins stað fyrir innkaupapantanir sem heyra undir breytingastjórnun. Það á sér stað vegna þess að afturköllunin er talin breyta sem þarf að samþykkja. Hægt er að framkvæma samþykkið sjálfkrafa af kerfinu. Þess vegna gengur ferlið út á að senda afturkallaða innkaupapöntun til samþykktarverkflæðis þannig að hún geti fengið stöðuna *Samþykkt*. Á þessu stigi sést innkaupapöntunin ekki lengur í listanum yfir drög að innkaupapöntunum á vinnusvæðinu **Undirbúningur innkaupapöntunar**.
