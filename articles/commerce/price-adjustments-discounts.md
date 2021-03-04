---
title: Verðleiðréttingar og afslættir
description: Þessi grein gefur upplýsingar um verðleiðréttingar og afslætti í Dynamics 365 Commerce.
author: scott-tucker
manager: AnnBe
ms.date: 11/16/2020
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
ms.openlocfilehash: 0c2adaa5cd935d5b593bfbb3215d3466fcafab7b
ms.sourcegitcommit: 1d74636bf9db5fb33e998322899504b709b4f89f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/19/2020
ms.locfileid: "4584316"
---
# <a name="price-adjustments-and-discounts"></a>Verðleiðréttingar og afslættir

[!include [banner](includes/banner.md)]

Þessi grein gefur upplýsingar um verðleiðréttingar og afslætti í Dynamics 365 Commerce.

Í Commerce, er hægt að gera verðleiðréttingar afurða og einnig að setja upp afslátt sem er notaður á línu eða færslu á sölustað (POS) í sölupöntun vinnustöðvar símtalalista eða í pöntun á netinu. Hægt er að tengja verðleiðréttingar og afslátt við sérstaka verðflokka. Fyrir bæði verðleiðréttingar og afslátt er hægt að tilgreina eina upphafsdagsetningu og lokadag eða endurtekið tímabil, afsláttarkóða og nokkrar aðrar eigindir. 

Hægt er að nota verðleiðréttingar og afslátt á vörur, vöruvíddasamsetningar eða flokka. Ef fleiri en einn afslætti er beitt á afurð, gæti viðskiptavinur fengið annaðhvort einn afslátt eða samanlagðan afslátt eftir skilgreiningu á afslættinum. Commerce beitir afslætti sjálfkrafa eða samsetningu afsláttar sem veitir viðskiptavini besta verð. Þegar verðleiðrétting er sett upp eða afsláttur, þarf að tryggja að staðfest sé að verðflokkar séu tengdir við réttar rásir, vörulista, tengsl eða vildarkerfi sem óskað er eftir að afslátturinn gildi á. Einnig, ef þú vilt mynda afsláttarkenni sjálfkrafa getur þú sett upp númeraraðir á síðunni **Færibreytur Commerce** áður en þú skilgreinir nýjan afslátt eða verðleiðréttingu.

> [!NOTE]
> Ekki er hægt að eyða verðleiðréttingu eða afslætti. Hins vegar munu talnagögn glatast.

## <a name="types-of-discounts"></a>Gerðir afsláttar

Það eru margar gerðir afslátta:

- **Einfaldur afsláttur** - eitt hlutfall eða upphæð.
- **Magnafsláttur** – Afsláttar sem er notaður þegar tvær eða fleiri vörur eru keyptar.
- **Afsláttur blandaðs tilboðs** - Afsláttur sem er notaður þegar sérstök samsetning af vörum er keypt.
- **Þröskuldur afsláttar** - Afsláttur sem er notaður þegar færslusamtala er hærri en tilgreind upphæð.
- **Afslættir eftir greiðslumáta** - Afsláttur sem er notaður þegar færslusamtala er hærri en tilgreind upphæð og tilgreind greiðslugerð (t.d. reiðufé, kredit eða debetkort) er notað fyrir greiðslu.
- **Sendingarafsláttur** – Afsláttur sem er notaður þegar heildarfærsla er hærri en tilgreind upphæð og tiltekinn afhendingarmáti (til dæmis tveggja daga sending eða sending yfir nótt) er notað á pöntuninni.

Hægt er að tengja bæði verðleiðréttingar og afslátt við sérstaka verðflokka. Síðan er hægt að tengja verðflokka við rásir, vörulista, tengsl og vildarkerfi.


[!INCLUDE[footer-include](../includes/footer-banner.md)]