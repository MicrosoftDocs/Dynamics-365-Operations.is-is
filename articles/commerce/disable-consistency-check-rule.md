---
title: Gera reglur sem notaðar eru í villuleitarferli færslu óvirkar
description: Þetta efnisatriði lýsir virkni til að gera villuleitarreglur færslu óvirkar í Microsoft Dynamics 365 Commerce.
author: analpert
ms.date: 12/11/2021
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
ms.openlocfilehash: cdaea51b4c84e6a62f0eb9412315ae77b4c11503
ms.sourcegitcommit: 9c2bc045eafc05b39ed1a6b601ccef48bd62ec55
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/14/2021
ms.locfileid: "7919526"
---
# <a name="disable-rules-used-in-the-transaction-validation-process"></a>Gera reglur sem notaðar eru í villuleitarferli færslu óvirkar

[!include [banner](../includes/banner.md)]

Smásöluaðilar geta verið með viðskiptasviðsmyndir og -ferli sem eru einstök fyrir þá. Þess vegna eiga ekki allar reglur sem teknar eru með í villuleitarferli viðskiptafærslunnar við fyrir alla smásöluaðila. Microsoft Dynamics 365 Commerce býður upp á virkni sem hægt er að nota til að gera reglur sem eiga ekki við óvirkar til að koma til móts við mismunandi þarfir.

Til að skoða listann yfir reglur sem eru tiltækar í villuleitarferli færslunnar í viðkomandi umhverfi og til að sjá stöðu hverrar reglu skal fara í **Retail og Commerce \> Uppsetning höfuðstöðva \> Færibreytur \> Færibreytur í Commerce** og velja flipann **Villuleit færslu**. Allar virkar reglur eru notaðar til að villuleita færslur í ferlinu **Villuleita í færslum verslunar** og þær þurfa að standast til að færslum sé safnað og þær birtar á færsluuppgjöri.

Sjálfgefið er að staða hverrar reglu sé stillt á **virk**. Því eru allar reglurnar notaðar til að villuleita færslur áður en þær eru teknar inn í færsluuppgjör viðskipta. Til að gera reglu óvirka skal breyta stöðu hennar í **óvirk**. Óvirkar reglur eru ekki teknar með við villuleit færslna í ferlinu **Villuleita í færslum verslunar**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
