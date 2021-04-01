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
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 11107993fe91e39409ccf06615a21574ad51d079
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5236819"
---
# <a name="create-cost-elements"></a><span data-ttu-id="21d91-103">Stofna kostnaðareiningar</span><span class="sxs-lookup"><span data-stu-id="21d91-103">Create cost elements</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="21d91-104">Það eru nokkrar aðferðir til að stofna kostnaðareiningar í kostnaðarbókhaldi.</span><span class="sxs-lookup"><span data-stu-id="21d91-104">There are several ways to create cost elements in Cost accounting.</span></span> <span data-ttu-id="21d91-105">Þessi verklýsing sýnir hvernig stofna á kostnaðareiningum með því að flytja inn aðallykla gegnum gagnatengi.</span><span class="sxs-lookup"><span data-stu-id="21d91-105">This procedure shows how to create cost elements by importing main accounts via a data connector.</span></span> <span data-ttu-id="21d91-106">USMF sýnifyrirtækið var notað til að stofna þetta ferli.</span><span class="sxs-lookup"><span data-stu-id="21d91-106">The USMF demo company was used to create this procedure.</span></span> <span data-ttu-id="21d91-107">Þetta ferli er fyrir eiginleika kostnaðarbókhalds sem var bætt við í Dynamics 365 for Operations 1611 útgáfu.</span><span class="sxs-lookup"><span data-stu-id="21d91-107">This procedure is for a Cost accounting feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="create-new-cost-elements"></a><span data-ttu-id="21d91-108">Stofna nýtt kostnaðareiningar</span><span class="sxs-lookup"><span data-stu-id="21d91-108">Create new cost elements</span></span>
1. <span data-ttu-id="21d91-109">Fara í kostnaðarbókhald > Víddir > Víddir kostnaðareininga.</span><span class="sxs-lookup"><span data-stu-id="21d91-109">Go to Cost accounting > Dimensions > Cost element dimensions.</span></span>
2. <span data-ttu-id="21d91-110">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="21d91-110">Click New.</span></span>
3. <span data-ttu-id="21d91-111">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="21d91-111">In the Name field, type a value.</span></span>
4. <span data-ttu-id="21d91-112">Í reitinn gagnatengi fyrir víddarstök skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="21d91-112">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="21d91-113">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="21d91-113">In the Description field, type a value.</span></span>
6. <span data-ttu-id="21d91-114">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="21d91-114">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="21d91-115">Stilla gagnatengi</span><span class="sxs-lookup"><span data-stu-id="21d91-115">Configure the data connector</span></span>
1. <span data-ttu-id="21d91-116">Smelltu á Skilgreina víddarstakaveitu</span><span class="sxs-lookup"><span data-stu-id="21d91-116">Click Configure dimension member provider.</span></span>
2. <span data-ttu-id="21d91-117">Sláið inn eða veljið gildi í reitnum Bókhaldslykill.</span><span class="sxs-lookup"><span data-stu-id="21d91-117">In the Chart of accounts field, enter or select a value.</span></span>
    * <span data-ttu-id="21d91-118">Velja samnýtt til að nota samnýttar bókhaldslykla.</span><span class="sxs-lookup"><span data-stu-id="21d91-118">Select Shared to use the shared chart of accounts.</span></span>  
3. <span data-ttu-id="21d91-119">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="21d91-119">Click New.</span></span>
4. <span data-ttu-id="21d91-120">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="21d91-120">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="21d91-121">Hægt er að nota síur á lykla sem uppfylla skilyrðin.</span><span class="sxs-lookup"><span data-stu-id="21d91-121">You can apply filters to accounts to meet your criteria.</span></span>  
5. <span data-ttu-id="21d91-122">Sláið inn eða veljið gildi í reitnum úr aðallykli.</span><span class="sxs-lookup"><span data-stu-id="21d91-122">In the From main account field, enter or select a value.</span></span>
6. <span data-ttu-id="21d91-123">Sláið inn eða veljið gildi í reitnum Til aðallykils.</span><span class="sxs-lookup"><span data-stu-id="21d91-123">In the To main account field, enter or select a value.</span></span>
7. <span data-ttu-id="21d91-124">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="21d91-124">Click OK.</span></span>

## <a name="import-main-accounts"></a><span data-ttu-id="21d91-125">Flytja inn aðallykla</span><span class="sxs-lookup"><span data-stu-id="21d91-125">Import main accounts</span></span>
1. <span data-ttu-id="21d91-126">Smelltu á Flytja inn víddarstök.</span><span class="sxs-lookup"><span data-stu-id="21d91-126">Click Import dimension members.</span></span>
    * <span data-ttu-id="21d91-127">Aðallyklar verða fluttir inn í kostnaðarbókhald og notað sem kostnaðareiningar.</span><span class="sxs-lookup"><span data-stu-id="21d91-127">Main accounts will be imported into Cost accounting and used as cost elements.</span></span>  
2. <span data-ttu-id="21d91-128">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="21d91-128">Click OK.</span></span>

## <a name="view-the-imported-accounts-as-cost-elements"></a><span data-ttu-id="21d91-129">Skoða innflutta lykla sem kostnaðareiningar</span><span class="sxs-lookup"><span data-stu-id="21d91-129">View the imported accounts as cost elements</span></span>
1. <span data-ttu-id="21d91-130">Smelltu á Skoða víddarstök.</span><span class="sxs-lookup"><span data-stu-id="21d91-130">Click View dimension members.</span></span>
    * <span data-ttu-id="21d91-131">Lítið á innflutt fjárhagslykla sem kostnaðareiningar í fyrirtækinu sem kostnaður getur streymt inn í.</span><span class="sxs-lookup"><span data-stu-id="21d91-131">View the imported ledger accounts as cost elements in your business that costs can flow to.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]