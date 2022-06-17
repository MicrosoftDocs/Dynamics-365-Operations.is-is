---
title: Gera reglur sem notaðar eru í villuleitarferli færslu óvirkar
description: Þessi grein lýsir virkni til að gera villuleitarreglur færslu óvirkar í Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 7d566aa3b829dad281528925a341382f9637fdba
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8884877"
---
# <a name="disable-rules-used-in-the-transaction-validation-process"></a>Gera reglur sem notaðar eru í villuleitarferli færslu óvirkar

[!include [banner](../includes/banner.md)]

Smásöluaðilar geta verið með viðskiptasviðsmyndir og -ferli sem eru einstök fyrir þá. Þess vegna eiga ekki allar reglur sem teknar eru með í villuleitarferli viðskiptafærslunnar við fyrir alla smásöluaðila. Microsoft Dynamics 365 Commerce býður upp á virkni sem hægt er að nota til að gera reglur sem eiga ekki við óvirkar til að koma til móts við mismunandi þarfir.

Til að skoða listann yfir reglur sem eru tiltækar í villuleitarferli færslunnar í viðkomandi umhverfi og til að sjá stöðu hverrar reglu skal fara í **Retail og Commerce \> Uppsetning höfuðstöðva \> Færibreytur \> Færibreytur í Commerce** og velja flipann **Villuleit færslu**. Allar virkar reglur eru notaðar til að villuleita færslur í ferlinu **Villuleita í færslum verslunar** og þær þurfa að standast til að færslum sé safnað og þær birtar á færsluuppgjöri.

Sjálfgefið er að staða hverrar reglu sé stillt á **virk**. Því eru allar reglurnar notaðar til að villuleita færslur áður en þær eru teknar inn í færsluuppgjör viðskipta. Til að gera reglu óvirka skal breyta stöðu hennar í **óvirk**. Óvirkar reglur eru ekki teknar með við villuleit færslna í ferlinu **Villuleita í færslum verslunar**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
