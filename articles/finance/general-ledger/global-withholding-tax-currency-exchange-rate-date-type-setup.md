---
title: Virkjaðu uppsetningu alþjóðlegrar staðgreiðslu gjaldmiðils gengis og dagsetningargerðar
description: Þessi grein útskýrir hvernig á að virkja alþjóðlega uppsetningu gjaldmiðils staðgreiðslugjaldmiðils og dagsetningargerðar.
author: kailiang
ms.date: 08/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 13131
ms.assetid: 08fd46ef-2eb8-4942-985d-40fd757b74a8
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 41f12a33651c14439f3a59c5c2f2d34019dada2d
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/06/2022
ms.locfileid: "9229980"
---
# <a name="enable-the-global-withholding-tax-currency-exchange-rate-type-and-date-type-setup"></a>Virkjaðu uppsetningu alþjóðlegrar staðgreiðslu gjaldmiðils gengis og dagsetningargerðar

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

Þessi grein útskýrir hvernig á að virkja alþjóðlega uppsetningu gjaldmiðils staðgreiðslugjaldmiðils og dagsetningargerðar. Þú getur nú valið sérstaka gengistegund og gengisútreikningsdagsetningu fyrir staðgreiðslugjaldmiðilinn. Þetta val ákvarðar gengi erlends gjaldmiðils sem er notað til að reikna út staðgreiðsluupphæð, í staðgreiðslugjaldmiðli, í greiðsluviðskiptum.

Þessi virkni er fáanleg í Microsoft Dynamics 365 Finance útgáfa 10.0.29 og síðar.

1. Fara til **Skattur** \> **Uppsetning** \> **Færibreytur** \> **Fjárhagsfæribreytur**.
2. Á **Staðgreiðsla skatts** flipann, stilltu **Virkja háþróaðan staðgreiðslugjaldmiðil** valmöguleika til **Já**.
3. Í **Gengistegund** reit, veldu gengistegund fyrir staðgreiðslugjaldmiðilinn.
4. Í **Tegund dagsetningar útreiknings** reit, veldu tegund útreikningsdagsetningar sem ákvarðar gengi staðgreiðslugjaldmiðils:

    - **Greiðsludagur** – Ákvarða gengi miðað við bókunardagsetningu greiðslubókar.
    - **Dagsetning reiknings** – Ákveðið gengi miðað við reikningsdagsetningu reikningsbókar. Ef reikningsdagsetning fylgiskjalsins er auð, verður bókunardagsetning reiknings notuð. 
    - **Dagsetning skjals** – Ákvarða gengi miðað við skjaladagsetningu greiðslubókar. Ef skjalsdagsetning fylgiskjalsins er auð, verður greiðsludagsetningin notuð.

5. Veldu **Vista**.

Ef færslugjaldmiðillinn er frábrugðinn staðgreiðslugjaldmiðlinum sem er skilgreindur í staðgreiðslugjaldmiðlinum, verður upphæðin í staðgreiðslugjaldmiðlinum reiknuð út frá færslugjaldmiðlinum, byggt á fyrri stillingum, og verður skráð í bókaðar staðgreiðslufærslur. .
