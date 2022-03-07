---
title: Gera reglur óvirkar í samræmisathugun smásölufærslunnar
description: Þetta efnisatriði lýsir virkni til að gera reglur samræmisathugunar færslu óvirkar í Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 10/15/2019
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 381bc8534d4b0a06a50c8c18b3f78aba9d43a1f497bfd271361216ed1dee9197
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6746662"
---
# <a name="disable-rules-in-the-retail-transaction-consistency-checker"></a>Gera reglur óvirkar í samræmisathugun smásölufærslunnar 

[!include [banner](../includes/banner.md)]

Smásöluaðilar geta verið með viðskiptasviðsmyndir og -ferli sem eru einstök fyrir þá. Þess vegna eiga ekki allar reglur sem teknar eru með sjálfgefið í samræmisathugun viðskiptafærslunnar við fyrir alla smásöluaðila. Microsoft Dynamics 365 Commerce býður upp á virkni sem hægt er að nota til að gera reglurnar sem eiga ekki við óvirkar til að koma til móts við mismunandi þarfir.

Til að skoða listann yfir reglur sem eru tiltækar í samræmisathugun færslunnar í viðkomandi umhverfi og til að sjá stöðu hverrar reglu skal fara í **Retail and Commerce \> Uppsetning höfuðstöðva \> Færibreytur \> Commerce færibreytur** og velja flipann **Villuleit færslu**.

Sjálfgefið er að staða hverrar reglu sé stillt á **virk**. Því eru allar reglurnar notaðar til að villuleita færslur áður en þær eru teknar inn í uppgjör viðskipta. Til að gera reglu óvirka skal breyta stöðu hennar í **óvirk**. Óvirkar reglur eru ekki teknar með við villuleit færslna í útreikningaferli uppgjörsins.

Til að sniðganga allt villuleitarferlið, óháð virkum reglum, skal fara í **Retail and Commerce \> Uppsetning höfuðstöðva \> Færibreytur \> Commerce færibreytur**, fara svo í flipann **Villuleit færslu** og stilla valkostinn **Gera samræmisathugun fyrir viðskiptafærslur óvirka** á **Já**. Þegar þessi valkostur hefur verið stilltur á **Nei** er ekki hægt að stilla hann aftur á **Já** úr notandaviðmótinu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]