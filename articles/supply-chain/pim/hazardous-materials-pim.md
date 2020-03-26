---
title: Hættuleg efni
description: Þetta efni veitir upplýsingar um skjöl um hættuleg efni og upplýsingar sem eru geymdar í umhverfinu þínu.
author: lachlancashMS
manager: AnnBe
ms.date: 01/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations, Retail
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: conradv
ms.search.validFrom: 2019-10-14
ms.dyn365.ops.version: ''
ms.openlocfilehash: 443d2eb545b2b7592e27ae037009720db0a71997
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092546"
---
# <a name="hazardous-materials"></a>Hættuleg efni

[!include [banner](../includes/banner.md)]

Upplýsingar um hættuleg efni eru sett upp í upplýsingastjórnun afuðar. Þessi eining veitir einnig skjöl sem hægt er að prenta með vörugeymslu.

Þegar þú sendir efni sem eru flokkuð sem hættuleg vara verður að fylgja viðbótar pappírsvinnu með sendingum. Virkni hættulegra efna skulum við geyma viðskiptavini um flokkunarupplýsingar og tengjast þeim til að gefa út hluti. Þessar upplýsingar er síðan hægt að nota til að undirbúa flutningsgögn.

> [!IMPORTANT]
> Til að hjálpa til við að stjórna sendingum af hættulegum varningi, Microsoft Dynamics 365 Supply Chain Management gerir þér kleift að setja upp viðbótarviðmiðunarupplýsingar sem tengjast vörum. Þú getur einnig sett upp fleiri sendingar skjöl. Hins vegar er kerfið ekki sjálfkrafa í samræmi við reglugerðir lands eða lands. Í staðinn er það tæki sem getur hjálpað heildarforritinu þínu.

Áður en þú getur notað þessa aðgerð er eftirfarandi uppsetning nauðsynleg:

- **Vöruupplýsingastjórnun:** Settu upp kóða sem hægt er að nota á útgefnar vörur.
- **Vöruhúsastjórnun:** Notaðu viðbótar sendingargögn til að prenta upplýsingar um sendingu.

## <a name="product-information-management"></a>Afurðaupplýsingastjórnun

Í vöruupplýsingastjórnun er að finna úrval af uppsetningarborðum þar sem þú getur bætt viðmiðunarupplýsingunum sem eru að finna í lista yfir hættulegan varning fyrir flutninga á vegum, í lofti og á sjó.

Hér eru sumar reglurgerðir sem oft er vísað í:

- **ADR** - Reglugerðir sem tengjast alþjóðlegum flutningi á hættulegum farmi á vegum
- **CFR 49** - Reglugerðir í Sameinuðu þjóðunum um flutning hættulegs vara
- **IMDG** - Alþjóðlega sjávarhættulegu vörurnar (IMDG) kóðinn
- **IATA** - Alþjóðlega flugsamgöngusamtökin (IATA) reglugerðir um hættulegan varning

Hver þessara reglugerða hefur lista yfir hættulegan varning sem inniheldur tilvísunarnúmer. Listarnir fyrir hverja tegund flutninga eru sameinaðir í sameiginlegum alþjóðlegum flokkunum. Supply Chain Management veitir tilvísunartöflu fyrir sameiginlega kóða í þessum listum. Hver listi hefur einnig nokkra einstaka kóða sem hægt er að skilgreina.

Til að byrja að stilla þessar upplýsingar skaltu búa til reglugerð sem þú getur notað til að stilla upphafsbreyturnar.

## <a name="warehouse-management"></a>Vöruhúsakerfi

Þegar sending er unnin er hægt að prenta nokkrar nýjar skýrslur. Þessar skýrslur nota upplýsingarnar sem þú settir upp í stjórnun vöruupplýsinga.
