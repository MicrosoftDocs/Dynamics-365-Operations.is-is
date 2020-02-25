---
title: Grunnstilla færibreytur sem hafa áhrif á smásöluuppgjör
description: Þetta efni sýnir skilgreiningar fyrir færibreytur Commerce sem hafa áhrif á hvernig uppgjör eru stofnuð og bókuð.
author: josaw1
manager: AnnBe
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d8cae6d2fa7c469f50fa92141a6cb5a0af1df4b0
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022897"
---
# <a name="configure-parameters-that-affect-retail-statements"></a><span data-ttu-id="e7628-103">Grunnstilla færibreytur sem hafa áhrif á smásöluuppgjör</span><span class="sxs-lookup"><span data-stu-id="e7628-103">Configure parameters that affect retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="e7628-104">Þetta efni sýnir skilgreiningar fyrir færibreytur Commerce sem hafa áhrif á hvernig uppgjör eru stofnuð og bókuð.</span><span class="sxs-lookup"><span data-stu-id="e7628-104">This topic demonstrates configurations for Commerce parameters that affect how statements get created and posted.</span></span> <span data-ttu-id="e7628-105">Þessi aðferð notar sýnigögn USRT fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="e7628-105">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="e7628-106">Í skoðunarrúðunni ferðu í **Einingar > Retail og Commerce > Uppsetning höfuðstöðva > Færibreytur > Færibreytur Commerce**.</span><span class="sxs-lookup"><span data-stu-id="e7628-106">In the navigation pane, go to **Modules > Retail and Commerce > Headquarters setup  > Parameters > Commerce parameters**.</span></span>
2. <span data-ttu-id="e7628-107">Veldu flipann **Bókun**.</span><span class="sxs-lookup"><span data-stu-id="e7628-107">Select the **Posting** tab.</span></span>
    - <span data-ttu-id="e7628-108">Veljið **Já** ef óskað er að bóka upphæðir tímabundins afsláttar sérstaklega.</span><span class="sxs-lookup"><span data-stu-id="e7628-108">Select **Yes** if you want to post the periodic discount amounts specifically.</span></span>  
    - <span data-ttu-id="e7628-109">Veldu **Staðlað** til að nota sjálfgefna fjárhagslykla eða veldu **Reglubundið** ef óskað er að skilgreina hvaða lykil á að nota fyrir hvern tímabundinn afslátt.</span><span class="sxs-lookup"><span data-stu-id="e7628-109">Select **Standard** to use default accounts, or select **Periodic** if you want to define which account to use for each periodic discount.</span></span>  
      - <span data-ttu-id="e7628-110">Veldu **Samantekt** ef leggja skal saman birgðalínur alltaf þegar það er hægt.</span><span class="sxs-lookup"><span data-stu-id="e7628-110">Select **Summary** if inventory lines should get aggregated whenever possible.</span></span>  
      - <span data-ttu-id="e7628-111">Veldu **Já** ef reikningar og greiðslur skulu sjálfkrafa jafnaðar sem hluti af uppgjörsbókunarferli.</span><span class="sxs-lookup"><span data-stu-id="e7628-111">Select **Yes** if Invoices and Payments should get automatically settled as part of the Statement posting process.</span></span>  
      - <span data-ttu-id="e7628-112">Veldu **Já** ef safna skal saman öruggum flutningsfærslum.</span><span class="sxs-lookup"><span data-stu-id="e7628-112">Select **Yes** if Safe drop transactions should get aggregated.</span></span>  
      - <span data-ttu-id="e7628-113">Veldu **Já** ef leggja skal saman peningaflutningsfærslur.</span><span class="sxs-lookup"><span data-stu-id="e7628-113">Select **Yes** if Bank drop transactions should get aggregated.</span></span>  
      - <span data-ttu-id="e7628-114">Veldu **Já** til að kveikja á uppsöfnun fyrir bókun uppgjörs.</span><span class="sxs-lookup"><span data-stu-id="e7628-114">Select **Yes** to turn aggregation on for Statement posting.</span></span>  
      - <span data-ttu-id="e7628-115">Veldu **Já** til að stofna og vinna sölupantanir samhliða þegar yfirlit eru bókaðar.</span><span class="sxs-lookup"><span data-stu-id="e7628-115">Select **Yes** to create and process orders in parallel when statements are posted.</span></span>  
      - <span data-ttu-id="e7628-116">Færið inn hámark pantana sem þarf að vinna í hverri runuvinnslu.</span><span class="sxs-lookup"><span data-stu-id="e7628-116">Enter the maximum orders to be processed in each batch job task.</span></span>  
3. <span data-ttu-id="e7628-117">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="e7628-117">Select **Save**.</span></span>

