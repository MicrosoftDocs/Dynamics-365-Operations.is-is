---
title: Stofna kostnaðareiningar
description: Það eru nokkrar aðferðir til að stofna kostnaðareiningar í kostnaðarbókhaldi.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMAXMainAccountDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 87f93fd7c1c42045274d6b89847b27e93614d9a4
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/10/2020
ms.locfileid: "3976140"
---
# <a name="create-cost-elements"></a><span data-ttu-id="5edb4-103">Stofna kostnaðareiningar</span><span class="sxs-lookup"><span data-stu-id="5edb4-103">Create cost elements</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5edb4-104">Það eru nokkrar aðferðir til að stofna kostnaðareiningar í kostnaðarbókhaldi.</span><span class="sxs-lookup"><span data-stu-id="5edb4-104">There are several ways to create cost elements in Cost accounting.</span></span> <span data-ttu-id="5edb4-105">Þessi verklýsing sýnir hvernig stofna á kostnaðareiningum með því að flytja inn aðallykla gegnum gagnatengi.</span><span class="sxs-lookup"><span data-stu-id="5edb4-105">This procedure shows how to create cost elements by importing main accounts via a data connector.</span></span> <span data-ttu-id="5edb4-106">USMF sýnifyrirtækið var notað til að stofna þetta ferli.</span><span class="sxs-lookup"><span data-stu-id="5edb4-106">The USMF demo company was used to create this procedure.</span></span> <span data-ttu-id="5edb4-107">Þetta ferli er fyrir eiginleika kostnaðarbókhalds sem var bætt við í Dynamics 365 for Operations 1611 útgáfu.</span><span class="sxs-lookup"><span data-stu-id="5edb4-107">This procedure is for a Cost accounting feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="create-new-cost-elements"></a><span data-ttu-id="5edb4-108">Stofna nýtt kostnaðareiningar</span><span class="sxs-lookup"><span data-stu-id="5edb4-108">Create new cost elements</span></span>
1. <span data-ttu-id="5edb4-109">Fara í kostnaðarbókhald > Víddir > Víddir kostnaðareininga.</span><span class="sxs-lookup"><span data-stu-id="5edb4-109">Go to Cost accounting > Dimensions > Cost element dimensions.</span></span>
2. <span data-ttu-id="5edb4-110">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="5edb4-110">Click New.</span></span>
3. <span data-ttu-id="5edb4-111">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="5edb4-111">In the Name field, type a value.</span></span>
4. <span data-ttu-id="5edb4-112">Í reitinn gagnatengi fyrir víddarstök skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="5edb4-112">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="5edb4-113">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="5edb4-113">In the Description field, type a value.</span></span>
6. <span data-ttu-id="5edb4-114">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="5edb4-114">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="5edb4-115">Stilla gagnatengi</span><span class="sxs-lookup"><span data-stu-id="5edb4-115">Configure the data connector</span></span>
1. <span data-ttu-id="5edb4-116">Smelltu á Skilgreina víddarstakaveitu</span><span class="sxs-lookup"><span data-stu-id="5edb4-116">Click Configure dimension member provider.</span></span>
2. <span data-ttu-id="5edb4-117">Sláið inn eða veljið gildi í reitnum Bókhaldslykill.</span><span class="sxs-lookup"><span data-stu-id="5edb4-117">In the Chart of accounts field, enter or select a value.</span></span>
    * <span data-ttu-id="5edb4-118">Velja samnýtt til að nota samnýttar bókhaldslykla.</span><span class="sxs-lookup"><span data-stu-id="5edb4-118">Select Shared to use the shared chart of accounts.</span></span>  
3. <span data-ttu-id="5edb4-119">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="5edb4-119">Click New.</span></span>
4. <span data-ttu-id="5edb4-120">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="5edb4-120">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="5edb4-121">Hægt er að nota síur á lykla sem uppfylla skilyrðin.</span><span class="sxs-lookup"><span data-stu-id="5edb4-121">You can apply filters to accounts to meet your criteria.</span></span>  
5. <span data-ttu-id="5edb4-122">Sláið inn eða veljið gildi í reitnum úr aðallykli.</span><span class="sxs-lookup"><span data-stu-id="5edb4-122">In the From main account field, enter or select a value.</span></span>
6. <span data-ttu-id="5edb4-123">Sláið inn eða veljið gildi í reitnum Til aðallykils.</span><span class="sxs-lookup"><span data-stu-id="5edb4-123">In the To main account field, enter or select a value.</span></span>
7. <span data-ttu-id="5edb4-124">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="5edb4-124">Click OK.</span></span>

## <a name="import-main-accounts"></a><span data-ttu-id="5edb4-125">Flytja inn aðallykla</span><span class="sxs-lookup"><span data-stu-id="5edb4-125">Import main accounts</span></span>
1. <span data-ttu-id="5edb4-126">Smelltu á Flytja inn víddarstök.</span><span class="sxs-lookup"><span data-stu-id="5edb4-126">Click Import dimension members.</span></span>
    * <span data-ttu-id="5edb4-127">Aðallyklar verða fluttir inn í kostnaðarbókhald og notað sem kostnaðareiningar.</span><span class="sxs-lookup"><span data-stu-id="5edb4-127">Main accounts will be imported into Cost accounting and used as cost elements.</span></span>  
2. <span data-ttu-id="5edb4-128">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="5edb4-128">Click OK.</span></span>

## <a name="view-the-imported-accounts-as-cost-elements"></a><span data-ttu-id="5edb4-129">Skoða innflutta lykla sem kostnaðareiningar</span><span class="sxs-lookup"><span data-stu-id="5edb4-129">View the imported accounts as cost elements</span></span>
1. <span data-ttu-id="5edb4-130">Smelltu á Skoða víddarstök.</span><span class="sxs-lookup"><span data-stu-id="5edb4-130">Click View dimension members.</span></span>
    * <span data-ttu-id="5edb4-131">Lítið á innflutt fjárhagslykla sem kostnaðareiningar í fyrirtækinu sem kostnaður getur streymt inn í.</span><span class="sxs-lookup"><span data-stu-id="5edb4-131">View the imported ledger accounts as cost elements in your business that costs can flow to.</span></span>  

