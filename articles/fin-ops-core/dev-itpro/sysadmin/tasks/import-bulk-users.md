---
title: Flytja inn notendur úr Azure Active Directory
description: Þetta ferli geta kerfisstjórar notað til að flytja handvirkt inn valda notendur eða inn stóra hópa notenda frá Azure Active Directory.
author: peakerbl
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
ms.openlocfilehash: e9f03ae7197790c1aac6ebf3cb94ff7963b1291e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745790"
---
# <a name="import-users-from-azure-active-directory"></a><span data-ttu-id="66181-103">Flytja inn notendur úr Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="66181-103">Import users from Azure Active Directory</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="import-select-users"></a><span data-ttu-id="66181-104">Flytja inn val á notendum</span><span class="sxs-lookup"><span data-stu-id="66181-104">Import select users</span></span>

<span data-ttu-id="66181-105">Þetta ferli geta kerfisstjórar notað til að flytja inn val notenda úr Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="66181-105">This procedure can be used by system administrators to import select users from Azure Active Directory (Azure AD).</span></span>

1. <span data-ttu-id="66181-106">Notandi verður fluttur inn með núgildandi lotufyrirtæki sem sjálfgefnu fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="66181-106">User will be imported with the current session company as their default company.</span></span> <span data-ttu-id="66181-107">Breytið núverandi fyrirtæki ef við á áður en notendur eru fluttir inn.</span><span class="sxs-lookup"><span data-stu-id="66181-107">Change current company if applicable before importing users.</span></span>
2. <span data-ttu-id="66181-108">Farið í **Kerfisstjórnun > Notendur > Notendur**.</span><span class="sxs-lookup"><span data-stu-id="66181-108">Go to **System administration > Users > User** s.</span></span>
3. <span data-ttu-id="66181-109">Smelltu á **Flytja inn notendur**.</span><span class="sxs-lookup"><span data-stu-id="66181-109">Click **Import users**.</span></span>
4. <span data-ttu-id="66181-110">Veljið notendur sem á að flytja inn og veljið **Flytja inn notendur**.</span><span class="sxs-lookup"><span data-stu-id="66181-110">Select the users that should be imported and select **Import users**.</span></span>

<span data-ttu-id="66181-111">Eftir að innflutningi er lokið þarf að úthluta hlutverkum á notendur.</span><span class="sxs-lookup"><span data-stu-id="66181-111">After import is completed it will be required to assign roles to users.</span></span>

## <a name="import-users-in-bulk"></a><span data-ttu-id="66181-112">Flytja inn marga notendur í einu</span><span class="sxs-lookup"><span data-stu-id="66181-112">Import users in bulk</span></span>

<span data-ttu-id="66181-113">Þetta ferli geta kerfisstjórar notað til að flytja inn stóra hópa notenda frá Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="66181-113">This procedure can be used by system administrators to import a large number of users from Azure Active Directory.</span></span>
<span data-ttu-id="66181-114">Athugið að ekki er hægt að velja notendur þegar valkosturinn Runuinnflutningur er notaður.</span><span class="sxs-lookup"><span data-stu-id="66181-114">Note that it is not possible to select users when using the Batch import option.</span></span>

## <a name="run-the-import-as-a-batch-job"></a><span data-ttu-id="66181-115">Keyra innflutning sem runuverk</span><span class="sxs-lookup"><span data-stu-id="66181-115">Run the import as a batch job</span></span>
1. <span data-ttu-id="66181-116">Notandi verður fluttur inn með núgildandi lotufyrirtæki sem sjálfgefnu fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="66181-116">User will be imported with the current session company as their default company.</span></span> <span data-ttu-id="66181-117">Breytið núverandi fyrirtæki ef við á áður en notendur eru fluttir inn.</span><span class="sxs-lookup"><span data-stu-id="66181-117">Change current company if applicable before importing users.</span></span>
2. <span data-ttu-id="66181-118">Farið í **Kerfisstjórnun > Notendur > Notendur**.</span><span class="sxs-lookup"><span data-stu-id="66181-118">Go to **System administration > Users > Users**.</span></span>
3. <span data-ttu-id="66181-119">Smellt er á **Runuinnflutningur**.</span><span class="sxs-lookup"><span data-stu-id="66181-119">Click **Batch import**.</span></span>
4. <span data-ttu-id="66181-120">Stækkaðu hlutann **Keyra í bakgrunni**.</span><span class="sxs-lookup"><span data-stu-id="66181-120">Expand the **Run in the background** section.</span></span>
4. <span data-ttu-id="66181-121">Veldu **Já** í reitnum **Runuvinnsla**.</span><span class="sxs-lookup"><span data-stu-id="66181-121">Select **Yes** in the **Batch processing** field.</span></span>
6. <span data-ttu-id="66181-122">Sláið inn eða veldu gildi í reitnum **Runuflokkur**.</span><span class="sxs-lookup"><span data-stu-id="66181-122">In the **Batch group** field, enter or select a value.</span></span> <span data-ttu-id="66181-123">Þetta skref er valfrjálst.</span><span class="sxs-lookup"><span data-stu-id="66181-123">This is an optional step.</span></span>  
7. <span data-ttu-id="66181-124">Veljið **Já** í reitnum **Einka**.</span><span class="sxs-lookup"><span data-stu-id="66181-124">Select **Yes** in the **Private** field.</span></span> <span data-ttu-id="66181-125">Þetta skref er valfrjálst.</span><span class="sxs-lookup"><span data-stu-id="66181-125">This is an optional step.</span></span>  
8. <span data-ttu-id="66181-126">Veljið **Já** í svæðinu **Mikilvægt starf**.</span><span class="sxs-lookup"><span data-stu-id="66181-126">Select **Yes** in the **Critical job** field.</span></span> <span data-ttu-id="66181-127">Þetta skref er valfrjálst.</span><span class="sxs-lookup"><span data-stu-id="66181-127">This is an optional step.</span></span>  
9. <span data-ttu-id="66181-128">Í reitnum **Fylgjast með flokki** skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="66181-128">In the **Monitoring category** field, select an option.</span></span>
10. <span data-ttu-id="66181-129">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="66181-129">Click **OK**.</span></span>

<span data-ttu-id="66181-130">Eftir að innflutningi er lokið þarf að úthluta hlutverkum á notendur.</span><span class="sxs-lookup"><span data-stu-id="66181-130">After import is completed, it will be required to assign roles to users.</span></span>

## <a name="run-in-a-sandbox-environment"></a><span data-ttu-id="66181-131">Keyrsla í sandkassaumhverfi</span><span class="sxs-lookup"><span data-stu-id="66181-131">Run in a sandbox environment</span></span>
1. <span data-ttu-id="66181-132">Veljið **Runuinnflutningur**.</span><span class="sxs-lookup"><span data-stu-id="66181-132">Select **Batch import**.</span></span>
2. <span data-ttu-id="66181-133">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="66181-133">Select **OK**.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]