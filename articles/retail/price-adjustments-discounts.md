---
title: Verðleiðréttingar og afslættir
description: Þessi grein gefur upplýsingar um verðleiðréttingar og afslætti í Microsoft Dynamics 365 for Retail.
author: scott-tucker
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters, RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15891
ms.assetid: bab5adf3-ddf0-4c22-a2eb-b4d25b88de99
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 61ac8e5fbdc4d91bb5bc5372a7fb96633043473a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "350965"
---
# <a name="price-adjustments-and-discounts"></a>Verðleiðréttingar og afslættir

[!include [banner](includes/banner.md)]

Þessi grein gefur upplýsingar um verðleiðréttingar og afslætti í Microsoft Dynamics 365 for Retail.

Í Dynamics 365 for Retail, er hægt að gera verðleiðréttingar afurða og einnig að setja upp afslátt sem er notaður á línu eða færslu á sölustað (POS) í sölupöntun vinnustöðvar símtalalista eða í pöntun á netinu. Hægt er að tengja verðleiðréttingar og afslátt við sérstaka verðflokka. Fyrir bæði verðleiðréttingar og afslátt er hægt að tilgreina eina upphafsdagsetningu og lokadag eða endurtekið tímabil, afsláttarkóða og nokkrar aðrar eigindir. Hægt er að nota verðleiðréttingar og afslátt á vörur, vöruvíddasamsetningar eða flokka. Ef fleiri en einn afslætti er beitt á afurð, gæti viðskiptavinur fengið annaðhvort einn afslátt eða samanlagðan afslátt eftir skilgreiningu á afslættinum. Dynamics 365 for Retail beitir afslætti sjálfkrafa eða samsetningu afsláttar sem veitir viðskiptavini besta verð. Þegar verðleiðrétting er sett upp eða afsláttur, þarf að tryggja að staðfest sé að verðflokkar séu tengdir við réttar rásir, vörulista, tengsl eða vildarkerfi sem óskað er eftir að afslátturinn gildi á. Einnig, ef þú vilt mynda afsláttarkenni sjálfkrafa getur þú sett upp númeraraðir á síðunni **Smásölufæribreytur** áður en þú skilgreinir nýjan afslátt eða verðleiðréttingu.

> [!NOTE]
> Ekki er hægt að eyða verðleiðréttingu eða afslætti. Hins vegar munu talnagögn glatast.

## <a name="types-of-discounts"></a>Gerðir afsláttar

Til eru fjórar gerðir af smásöluafslætti:

- **Einfaldur afsláttur** - eitt hlutfall eða upphæð.
- **Magnafsláttur** – Afsláttar sem er notaður þegar tvær eða fleiri vörur eru keyptar.
- **Afsláttur blandaðs tilboðs** - Afsláttur sem er notaður þegar sérstök samsetning af vörum er keypt.
- **Þröskuldur afsláttar** - Afsláttur sem er notaður þegar færslusamtala er hærri en tilgreind upphæð.

Hægt er að tengja bæði verðleiðréttingar og afslátt við sérstaka verðflokka. Síðan er hægt að tengja verðflokka við rásir, vörulista, tengsl og vildarkerfi.
