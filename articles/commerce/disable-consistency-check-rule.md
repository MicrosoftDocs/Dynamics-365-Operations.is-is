---
title: Gera reglur óvirkar í samræmisathugun smásölufærslunnar
description: Þetta efnisatriði lýsir virkni til að gera reglur samræmisathugunar smásölufærslunnar óvirkar í Microsoft Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 10/15/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: b11b901fafc3907e9d3cae5cd554cc9a868a414c
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004344"
---
# <a name="disable-rules-in-the-retail-transaction-consistency-checker"></a>Gera reglur óvirkar í samræmisathugun smásölufærslunnar 

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Smásöluaðilar geta verið með viðskiptasviðsmyndir og -ferli sem eru einstök fyrir þá. Þess vegna eiga ekki allar reglur sem teknar eru með sjálfgefið í samræmisathugun viðskiptafærslunnar við fyrir alla smásöluaðila. Microsoft Dynamics 365 Commerce býður upp á virkni sem hægt er að nota til að gera reglurnar sem eiga ekki við óvirkar til að koma til móts við mismunandi þarfir.

Til að skoða listann yfir reglur sem eru tiltækar í samræmisathugun færslunnar í viðkomandi umhverfi og til að sjá stöðu hverrar reglu skal fara í **Smásala og viðskipti \> Uppsetning höfuðstöðva \> Færibreytur \> Viðskiptafæribreytur** og velja flipann **Villuleit færslu**.

Sjálfgefið er að staða hverrar reglu sé stillt á **virk**. Því eru allar reglurnar notaðar til að villuleita færslur áður en þær eru teknar inn í uppgjör viðskipta. Til að gera reglu óvirka skal breyta stöðu hennar í **óvirk**. Óvirkar reglur eru ekki teknar með við villuleit færslna í útreikningaferli uppgjörsins.

Til að sniðganga allt villuleitarferlið, óháð virkum reglum, skal fara í **Smásala og viðskipti \> Uppsetning höfuðstöðva \> Færibreytur \> Viðskiptafæribreytur**, fara svo í flipann **Villuleit færslu** og stilla valkostinn **Gera samræmisathugun fyrir viðskiptafærslur óvirka** á **Já**. Þegar þessi valkostur hefur verið stilltur á **Nei** er ekki hægt að stilla hann aftur á **Já** úr notandaviðmótinu.
