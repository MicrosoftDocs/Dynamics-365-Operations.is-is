---
title: Yfirlit yfir áskriftargreiðslur
description: Í þessari grein er lýst áskriftarreikningi í Microsoft Dynamics 365 Finance.
author: JodiChristiansen
ms.date: 04/13/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, CustVendExternalItem
audience: Application User
ms.reviewer: twheeloc
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2022-02-09
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 10302e9ae7dff3d018897b666caaf4d4289b4866
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8856742"
---
# <a name="subscription-billing-overview"></a>Yfirlit yfir áskriftargreiðslur

[!include [banner](../includes/banner.md)]

Áskriftargreiðslur gera fyrirtækjum kleift að stjórna tekjumöguleikum áskriftar og endurteknum greiðslum með greiðsluáætlunum. Auðvelt er að stjórna flóknum verðlagningarlíkönum og tekjuúthlutun og eru innheimt og skráð á línustigi. Fjölþátta tekjuúthlutun gerir kleift að úthluta tekjum til að uppfylla alþjóðlega reikningsskilastaðla (International Financial Reporting Standard 15 \[IFRS 15\]) og almennt samþykktum bókhaldsreglum (US GAAP) (reikningsskilastaðli 606 \[ASC 606\]).

Lausnin hefur þrjár einingar sem hægt er að nota sjálfstætt. Einnig er hægt að nota allar þrjár einingarnar saman.

- **Endurteknar samningsgreiðslur** – Þessi eining gerir endurtekinni greiðslu og verðstjórnun kleift að stjórna verðlagningar- og greiðslufæribreytum, samningsendurnýjunum og sameinaðri reikningsfærslu.
- **Tekju- og kostnaðarfrestanir** – Þessi eining útilokar handvirka ferla og tengsl við ytri kerfi með því að stjórna tekjum og gefa rauntímainnsýn í mánaðarlegar endurteknar tekjur.
- **Margþátta tekjuúthlutun** – Þessi eining hjálpar til við reglufylgni við tekjur með því að meðhöndla verðlagningu og tekjuúthlutun á mörgum vörum.

Frekari upplýsingar um áskriftargreiðslu er að finna í [Áskriftargreiðslur Power BI efni](sub-bill-power-bi.md).

Áskriftarreikningur er virkur í gegnum **Eiginleikastjórnun**. Hins vegar er ekki hægt að nota hana með eiginleikanum **Tekjuskráning**. Þú verður því að gera þennan eiginleika óvirkan áður en þú virkjar áskriftargreiðslur.

1. Á vinnusvæðinu **Eiginleikastjórnun**, í flipanum **Allt**, skal færa inn **Tekjuskráningu** í síðuna og síðan velja heiti eiginleikans sem síuna.
2. Veldu eiginleikann **Tekjuskráning** og veldu síðan **Gera óvirkt**.
3. Í síuna **Heiti eiginleika** skal færa inn **Áskriftargreiðslur** og velja síðan síueininguna.
4. Veldu eiginleikann **Áskriftargreiðslur** og veldu síðan **Virkja**.
5. Veldu eina af þremur einingum úr fyrri listanum og veldu svo **Virkja**. Endurtakið þetta skref fyrir hverja af hinum tveimur einingunum.

    > [!IMPORTANT]
    > Virkja þarf eiginleikann **Áskriftargreiðslur** áður en hægt verður að virkja einingarnar þrjár.
