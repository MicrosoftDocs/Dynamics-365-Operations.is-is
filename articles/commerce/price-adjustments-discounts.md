---
title: Verðleiðréttingar og afslættir
description: Þessi grein gefur upplýsingar um verðleiðréttingar og afslætti í Dynamics 365 Commerce.
author: josaw1
ms.date: 06/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.custom: 15891
ms.assetid: bab5adf3-ddf0-4c22-a2eb-b4d25b88de99
ms.search.industry: Retail
ms.search.form: RetailParameters, RetailPeriodicDiscount
ms.openlocfilehash: ff90df814d6930b5cf92772e430625943e0ae983
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279090"
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

> [!NOTE]
> Afsláttur blandaðs tilboðs og þröskuldsafsláttur eru með eiginleika sem heita „Telja vörur sem ekki er veittur afsláttur af“ og „Telja vörur sem ekki er veittur afsláttur af fram að þröskuldi“. Ef þessir eiginleikar eru virkjaðir getur vara sem ekki er veittur afsláttur á samt hjálpað til við að færsla fái afslátt, en ekki verður gefinn afsláttur af þeirri vöru. 
> 
> Ef til dæmis búinn er til afsláttur blandaðs tilboðs með tveimur línum, A og B, þar sem viðskiptavinur á að fá 10% afslátt af báðum vörum, en vara A er með hakað í skilgreininguna „Koma í veg fyrir alla afslætti“, þá mun þetta yfirleitt stöðva vöru A frá því að vera með í afslættinum. En ef eiginleikinn „Telja vörur sem ekki er veittur afsláttur af“ er virkjaður, þá er hægt að nota vöru A í afslætti blandaðs tilboðs, en 10% afslátturinn verður aðeins notaður á vöru B. Svipuð rök eiga við um þröskuldsafslátt. 
>
> Eiginleikinn „Telja vörur sem ekki er veittur afsláttur af fram að þröskuldi“ er með viðbótarmöguleika í samanburði við eiginleikann „Telja vörur sem ekki er veittur afsláttur af“ í afsláttum blandaðs tilboðs. Ef þröskuldsafslátturinn er virkur og ef það er vara til með núverandi afslætti sem kæmi í veg fyrir að varan fengi aðra afslætti, þá myndi verðið sem greitt er fyrir þessa vöru uppfylla skilyrði varðandi að ná þröskuldinum, en þessi vara fengi ekki viðbótarafsláttinn.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
