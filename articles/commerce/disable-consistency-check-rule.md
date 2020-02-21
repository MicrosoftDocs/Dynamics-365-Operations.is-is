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
# <a name="disable-rules-in-the-retail-transaction-consistency-checker"></a><span data-ttu-id="62d0f-103">Gera reglur óvirkar í samræmisathugun smásölufærslunnar</span><span class="sxs-lookup"><span data-stu-id="62d0f-103">Disable rules in the retail transaction consistency checker</span></span> 

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="62d0f-104">Smásöluaðilar geta verið með viðskiptasviðsmyndir og -ferli sem eru einstök fyrir þá.</span><span class="sxs-lookup"><span data-stu-id="62d0f-104">Retailers can have business scenarios and processes that are unique to them.</span></span> <span data-ttu-id="62d0f-105">Þess vegna eiga ekki allar reglur sem teknar eru með sjálfgefið í samræmisathugun viðskiptafærslunnar við fyrir alla smásöluaðila.</span><span class="sxs-lookup"><span data-stu-id="62d0f-105">Therefore, not all the rules that are included by default in the commerce transaction consistency checker are applicable to all retailers.</span></span> <span data-ttu-id="62d0f-106">Microsoft Dynamics 365 Commerce býður upp á virkni sem hægt er að nota til að gera reglurnar sem eiga ekki við óvirkar til að koma til móts við mismunandi þarfir.</span><span class="sxs-lookup"><span data-stu-id="62d0f-106">To accommodate differences, Microsoft Dynamics 365 Commerce provides functionality that can be used to disable the rules that aren't applicable.</span></span>

<span data-ttu-id="62d0f-107">Til að skoða listann yfir reglur sem eru tiltækar í samræmisathugun færslunnar í viðkomandi umhverfi og til að sjá stöðu hverrar reglu skal fara í **Smásala og viðskipti \> Uppsetning höfuðstöðva \> Færibreytur \> Viðskiptafæribreytur** og velja flipann **Villuleit færslu**.</span><span class="sxs-lookup"><span data-stu-id="62d0f-107">To view the list of rules that are available in the transaction consistency checker in your environment, and to see the status of each rule, go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce parameters**, and select the **Transaction validation** tab.</span></span>

<span data-ttu-id="62d0f-108">Sjálfgefið er að staða hverrar reglu sé stillt á **virk**.</span><span class="sxs-lookup"><span data-stu-id="62d0f-108">By default, the status of every rule is set to **Enabled**.</span></span> <span data-ttu-id="62d0f-109">Því eru allar reglurnar notaðar til að villuleita færslur áður en þær eru teknar inn í uppgjör viðskipta.</span><span class="sxs-lookup"><span data-stu-id="62d0f-109">Therefore, all the rules are used to validate transactions before they are pulled into the commerce statements.</span></span> <span data-ttu-id="62d0f-110">Til að gera reglu óvirka skal breyta stöðu hennar í **óvirk**.</span><span class="sxs-lookup"><span data-stu-id="62d0f-110">To disable a rule, change its status to **Disabled**.</span></span> <span data-ttu-id="62d0f-111">Óvirkar reglur eru ekki teknar með við villuleit færslna í útreikningaferli uppgjörsins.</span><span class="sxs-lookup"><span data-stu-id="62d0f-111">Disabled rules aren't considered when transactions are validated during the statement calculation process.</span></span>

<span data-ttu-id="62d0f-112">Til að sniðganga allt villuleitarferlið, óháð virkum reglum, skal fara í **Smásala og viðskipti \> Uppsetning höfuðstöðva \> Færibreytur \> Viðskiptafæribreytur**, fara svo í flipann **Villuleit færslu** og stilla valkostinn **Gera samræmisathugun fyrir viðskiptafærslur óvirka** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="62d0f-112">To bypass the whole validation process, regardless of the rules that are enabled, go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce parameters**, and then, on the **Transaction validation** tab, set the **Disable consistency checker for Commerce transactions** option to **Yes**.</span></span> <span data-ttu-id="62d0f-113">Þegar þessi valkostur hefur verið stilltur á **Nei** er ekki hægt að stilla hann aftur á **Já** úr notandaviðmótinu.</span><span class="sxs-lookup"><span data-stu-id="62d0f-113">After this option is set to **No**, it can't be set back to **Yes** from the user interface (UI).</span></span>
