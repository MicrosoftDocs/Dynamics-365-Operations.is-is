---
title: Samstilla dagsetningu og tíma í innflutningsvinnslum
description: Notið UTC-tíma í innflutningsverkum til að forðast vandamál varðandi umreikning tímabelta.
author: Sunil-Garg
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 41c0ec805a20a525989e0133e5dffb29ce3fed39
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748670"
---
# <a name="synchronize-date-and-time-in-import-jobs"></a>Samstilla dagsetningu og tíma í innflutningsvinnslum

[!include [banner](../includes/banner.md)]

Mikilvægt er að stilla tímabelti fyrir innflutningsverkið á samræmdan heimstíma (UTC). Óvæntar dagsetningar og tímar gætu sést í innfluttum gögnum ef önnur stilling er notuð. Án réttrar stillingar mun innflutningsferlið umbreyta UTC-dagsetningunni í staðbundna sniðið og kerfisstillingarnar umbreyta því síðan aftur.

Þessi tvöfaldi umreikningur veldur því að dagsetningar breytast milli forrita. Til dæmis gæti tvöfaldur umreikningur valdið því að upphafsdagsetning starfsmanns verði mismunandi á milli Dynamics 365 Human Resources og Dynamics 365 Finance vegna mismunar í staðbundnum tímabeltum. Að stilla innflutningsverkið á UTC leysir úr þessum vanda.

1. Í Dynamics 365 Finance and Operations skal velja **Gagnastjórnun**.

2. Veljið **Flytja inn verk** og veljið síðan verkið.

3. Undir **Dagsetningarsnið uppruna** skal velja **CSV-Unicode**.

   [![Breyta dagsetningarsniði uppruna í UTC](./media/data-source-date-format.png)](./media/data-source-date-format.png)

4. Breytið **Tímabelti** í **Samræmdan heimstíma** og breytið **Tungumáli** í **En-Us**.




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]