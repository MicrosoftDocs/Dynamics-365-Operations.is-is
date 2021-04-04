---
title: Flytja inn notendur úr Azure Active Directory
description: Þetta ferli geta kerfisstjórar notað til að flytja handvirkt inn valda notendur eða inn stóra hópa notenda frá Azure Active Directory.
author: peakerbl
manager: AnnBe
ms.date: 07/07/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0c2600ad8f441e6b73b143c27afa08ad0a5c2748
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5571006"
---
# <a name="import-users-from-azure-active-directory"></a><span data-ttu-id="a9eb0-103">Flytja inn notendur úr Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="a9eb0-103">Import users from Azure Active Directory</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="import-select-users"></a><span data-ttu-id="a9eb0-104">Flytja inn val á notendum</span><span class="sxs-lookup"><span data-stu-id="a9eb0-104">Import select users</span></span>

<span data-ttu-id="a9eb0-105">Þetta ferli geta kerfisstjórar notað til að flytja inn val notenda úr Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="a9eb0-105">This procedure can be used by system administrators to import select users from Azure Active Directory (Azure AD).</span></span>

1. <span data-ttu-id="a9eb0-106">Notandi verður fluttur inn með núgildandi lotufyrirtæki sem sjálfgefnu fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="a9eb0-106">User will be imported with the current session company as their default company.</span></span> <span data-ttu-id="a9eb0-107">Breytið núverandi fyrirtæki ef við á áður en notendur eru fluttir inn.</span><span class="sxs-lookup"><span data-stu-id="a9eb0-107">Change current company if applicable before importing users.</span></span>
2. <span data-ttu-id="a9eb0-108">Farið í **Kerfisstjórnun > Notendur > Notendur**.</span><span class="sxs-lookup"><span data-stu-id="a9eb0-108">Go to **System administration > Users > User** s.</span></span>
3. <span data-ttu-id="a9eb0-109">Smelltu á **Flytja inn notendur**.</span><span class="sxs-lookup"><span data-stu-id="a9eb0-109">Click **Import users**.</span></span>
4. <span data-ttu-id="a9eb0-110">Veljið notendur sem á að flytja inn og veljið **Flytja inn notendur**.</span><span class="sxs-lookup"><span data-stu-id="a9eb0-110">Select the users that should be imported and select **Import users**.</span></span>

<span data-ttu-id="a9eb0-111">Eftir að innflutningi er lokið þarf að úthluta hlutverkum á notendur.</span><span class="sxs-lookup"><span data-stu-id="a9eb0-111">After import is completed it will be required to assign roles to users.</span></span>

## <a name="import-users-in-bulk"></a><span data-ttu-id="a9eb0-112">Flytja inn marga notendur í einu</span><span class="sxs-lookup"><span data-stu-id="a9eb0-112">Import users in bulk</span></span>

<span data-ttu-id="a9eb0-113">Þetta ferli geta kerfisstjórar notað til að flytja inn stóra hópa notenda frá Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a9eb0-113">This procedure can be used by system administrators to import a large number of users from Azure Active Directory.</span></span>
<span data-ttu-id="a9eb0-114">Athugið að ekki er hægt að velja notendur þegar valkosturinn Runuinnflutningur er notaður.</span><span class="sxs-lookup"><span data-stu-id="a9eb0-114">Note that it is not possible to select users when using the Batch import option.</span></span>

## <a name="run-the-import-as-a-batch-job"></a><span data-ttu-id="a9eb0-115">Keyra innflutning sem runuverk</span><span class="sxs-lookup"><span data-stu-id="a9eb0-115">Run the import as a batch job</span></span>
1. <span data-ttu-id="a9eb0-116">Notandi verður fluttur inn með núgildandi lotufyrirtæki sem sjálfgefnu fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="a9eb0-116">User will be imported with the current session company as their default company.</span></span> <span data-ttu-id="a9eb0-117">Breytið núverandi fyrirtæki ef við á áður en notendur eru fluttir inn.</span><span class="sxs-lookup"><span data-stu-id="a9eb0-117">Change current company if applicable before importing users.</span></span>
2. <span data-ttu-id="a9eb0-118">Farið í **Kerfisstjórnun > Notendur > Notendur**.</span><span class="sxs-lookup"><span data-stu-id="a9eb0-118">Go to **System administration > Users > Users**.</span></span>
3. <span data-ttu-id="a9eb0-119">Smellt er á **Runuinnflutningur**.</span><span class="sxs-lookup"><span data-stu-id="a9eb0-119">Click **Batch import**.</span></span>
4. <span data-ttu-id="a9eb0-120">Stækkaðu hlutann **Keyra í bakgrunni**.</span><span class="sxs-lookup"><span data-stu-id="a9eb0-120">Expand the **Run in the background** section.</span></span>
4. <span data-ttu-id="a9eb0-121">Veldu **Já** í reitnum **Runuvinnsla**.</span><span class="sxs-lookup"><span data-stu-id="a9eb0-121">Select **Yes** in the **Batch processing** field.</span></span>
6. <span data-ttu-id="a9eb0-122">Sláið inn eða veldu gildi í reitnum **Runuflokkur**.</span><span class="sxs-lookup"><span data-stu-id="a9eb0-122">In the **Batch group** field, enter or select a value.</span></span> <span data-ttu-id="a9eb0-123">Þetta skref er valfrjálst.</span><span class="sxs-lookup"><span data-stu-id="a9eb0-123">This is an optional step.</span></span>  
7. <span data-ttu-id="a9eb0-124">Veljið **Já** í reitnum **Einka**.</span><span class="sxs-lookup"><span data-stu-id="a9eb0-124">Select **Yes** in the **Private** field.</span></span> <span data-ttu-id="a9eb0-125">Þetta skref er valfrjálst.</span><span class="sxs-lookup"><span data-stu-id="a9eb0-125">This is an optional step.</span></span>  
8. <span data-ttu-id="a9eb0-126">Veljið **Já** í svæðinu **Mikilvægt starf**.</span><span class="sxs-lookup"><span data-stu-id="a9eb0-126">Select **Yes** in the **Critical job** field.</span></span> <span data-ttu-id="a9eb0-127">Þetta skref er valfrjálst.</span><span class="sxs-lookup"><span data-stu-id="a9eb0-127">This is an optional step.</span></span>  
9. <span data-ttu-id="a9eb0-128">Í reitnum **Fylgjast með flokki** skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="a9eb0-128">In the **Monitoring category** field, select an option.</span></span>
10. <span data-ttu-id="a9eb0-129">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="a9eb0-129">Click **OK**.</span></span>

<span data-ttu-id="a9eb0-130">Eftir að innflutningi er lokið þarf að úthluta hlutverkum á notendur.</span><span class="sxs-lookup"><span data-stu-id="a9eb0-130">After import is completed, it will be required to assign roles to users.</span></span>

## <a name="run-in-a-sandbox-environment"></a><span data-ttu-id="a9eb0-131">Keyrsla í sandkassaumhverfi</span><span class="sxs-lookup"><span data-stu-id="a9eb0-131">Run in a sandbox environment</span></span>
1. <span data-ttu-id="a9eb0-132">Veljið **Runuinnflutningur**.</span><span class="sxs-lookup"><span data-stu-id="a9eb0-132">Select **Batch import**.</span></span>
2. <span data-ttu-id="a9eb0-133">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="a9eb0-133">Select **OK**.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]