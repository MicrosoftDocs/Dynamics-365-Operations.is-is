---
title: Gera reglur óvirkar í samræmisathugun smásölufærslunnar
description: Þetta efnisatriði lýsir virkni til að gera reglur samræmisathugunar smásölufærslunnar óvirkar í Microsoft Dynamics 365 Retail.
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
ms.openlocfilehash: 4bf8df2fb9f8f5c33ceb13eb012fb6879f81ec66
ms.sourcegitcommit: bdbca89bd9b328c282ebfb681f75b8f1ed96e7a8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/14/2019
ms.locfileid: "2586298"
---
# <a name="disable-rules-in-the-retail-transaction-consistency-checker"></a><span data-ttu-id="bcf6a-103">Gera reglur óvirkar í samræmisathugun smásölufærslunnar</span><span class="sxs-lookup"><span data-stu-id="bcf6a-103">Disable rules in the retail transaction consistency checker</span></span> 

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="bcf6a-104">Smásöluaðilar geta verið með viðskiptasviðsmyndir og -ferli sem eru einstök fyrir þá.</span><span class="sxs-lookup"><span data-stu-id="bcf6a-104">Retailers can have business scenarios and processes that are unique to them.</span></span> <span data-ttu-id="bcf6a-105">Þess vegna eiga ekki allar reglur sem teknar eru með sjálfgefið í samræmisathugun smásölufærslunnar við fyrir alla smásöluaðila.</span><span class="sxs-lookup"><span data-stu-id="bcf6a-105">Therefore, not all the rules that are included by default in the retail transaction consistency checker are applicable to all retailers.</span></span> <span data-ttu-id="bcf6a-106">Microsoft Dynamics 365 Retail býður upp á virkni sem hægt er að nota til að gera reglurnar sem eiga ekki við óvirkar til að koma til móts við mismunandi þarfir.</span><span class="sxs-lookup"><span data-stu-id="bcf6a-106">To accommodate differences, Microsoft Dynamics 365 Retail provides functionality that can be used to disable the rules that aren't applicable.</span></span>

<span data-ttu-id="bcf6a-107">Til að skoða listann yfir reglur sem eru tiltækar í samræmisathugun smásölufærslunnar í viðkomandi umhverfi og til að sjá stöðu hverrar reglu skal fara í **Retail \> Uppsetning höfuðstöðva \> Færibreytur \> Smásölufæribreytur** og velja flipann **Villuleit færslu**.</span><span class="sxs-lookup"><span data-stu-id="bcf6a-107">To view the list of rules that are available in the retail transaction consistency checker in your environment, and to see the status of each rule, go to **Retail \> Headquarters setup \> Parameters \> Retail parameters**, and select the **Transaction validation** tab.</span></span>

<span data-ttu-id="bcf6a-108">Sjálfgefið er að staða hverrar reglu sé stillt á **virk**.</span><span class="sxs-lookup"><span data-stu-id="bcf6a-108">By default, the status of every rule is set to **Enabled**.</span></span> <span data-ttu-id="bcf6a-109">Því eru allar reglurnar notaðar til að villuleita smásölufærslur áður en þær eru teknar inn í smásöluuppgjörin.</span><span class="sxs-lookup"><span data-stu-id="bcf6a-109">Therefore, all the rules are used to validate retail transactions before they are pulled into the retail statements.</span></span> <span data-ttu-id="bcf6a-110">Til að gera reglu óvirka skal breyta stöðu hennar í **óvirk**.</span><span class="sxs-lookup"><span data-stu-id="bcf6a-110">To disable a rule, change its status to **Disabled**.</span></span> <span data-ttu-id="bcf6a-111">Óvirkar reglur eru ekki teknar með við villuleit smásölufærslna í útreikningaferli uppgjörsins.</span><span class="sxs-lookup"><span data-stu-id="bcf6a-111">Disabled rules aren't considered when retail transactions are validated during the statement calculation process.</span></span>

<span data-ttu-id="bcf6a-112">Til að sniðganga allt villuleitarferlið, óháð virkum reglum, skal fara í **Retail \> Uppsetning höfuðstöðva \> Færibreytur \> Smásölufæribreytur**, fara svo í flipann **Villuleit færslu** og stilla valkostinn **Gera samræmisathugun fyrir smásölufærslur óvirka** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="bcf6a-112">To bypass the whole validation process, regardless of the rules that are enabled, go to **Retail \> Headquarters setup \> Parameters \> Retail parameters**, and then, on the **Transaction validation** tab, set the **Disable consistency checker for Retail transactions** option to **Yes**.</span></span> <span data-ttu-id="bcf6a-113">Þegar þessi valkostur hefur verið stilltur á **Nei** er ekki hægt að stilla hann aftur á **Já** úr notandaviðmótinu.</span><span class="sxs-lookup"><span data-stu-id="bcf6a-113">After this option is set to **No**, it can't be set back to **Yes** from the user interface (UI).</span></span>
