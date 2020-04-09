---
title: Flytja inn marga notendur í einu
description: Þetta ferli geta kerfisstjórar notað til að flytja inn stóra hópa notenda frá Azure Active Directory.
author: maertenm
manager: AnnBe
ms.date: 07/07/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7d8b55895c9dfaf1c69cd319697f1e0da5990daf
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144088"
---
# <a name="import-users-in-bulk"></a><span data-ttu-id="c325c-103">Flytja inn marga notendur í einu</span><span class="sxs-lookup"><span data-stu-id="c325c-103">Import users in bulk</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c325c-104">Þetta ferli geta kerfisstjórar notað til að flytja inn stóra hópa notenda frá Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c325c-104">This procedure can be used by system administrators to import a large number of users from Azure Active Directory.</span></span>


## <a name="run-as-a-batch-job"></a><span data-ttu-id="c325c-105">Keyra sem runuvinnslu</span><span class="sxs-lookup"><span data-stu-id="c325c-105">Run as a batch job</span></span>
1. <span data-ttu-id="c325c-106">Farið í Kerfisstjórnun > Notendur > Notendur.</span><span class="sxs-lookup"><span data-stu-id="c325c-106">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="c325c-107">Smellt er á Runuinnflutningur.</span><span class="sxs-lookup"><span data-stu-id="c325c-107">Click Batch import.</span></span>
3. <span data-ttu-id="c325c-108">Stækka útvíkkun á liðnum Keyra í bakgrunni.</span><span class="sxs-lookup"><span data-stu-id="c325c-108">Expand the Run in the background section.</span></span>
4. <span data-ttu-id="c325c-109">Veljið Já í svæðinu runuvinnsla.</span><span class="sxs-lookup"><span data-stu-id="c325c-109">Select Yes in the Batch processing field.</span></span>
5. <span data-ttu-id="c325c-110">Slá inn gildi í reitinn Verklýsing.</span><span class="sxs-lookup"><span data-stu-id="c325c-110">In the Task description field, type a value.</span></span>
6. <span data-ttu-id="c325c-111">Sláið inn eða veldu gildi í reitnum Runuflokkur.</span><span class="sxs-lookup"><span data-stu-id="c325c-111">In the Batch group field, enter or select a value.</span></span>
    * <span data-ttu-id="c325c-112">Þetta skref er valfrjálst.</span><span class="sxs-lookup"><span data-stu-id="c325c-112">This is an optional step.</span></span>  
7. <span data-ttu-id="c325c-113">Veljið Já í reitnum Einka.</span><span class="sxs-lookup"><span data-stu-id="c325c-113">Select Yes in the Private field.</span></span>
    * <span data-ttu-id="c325c-114">Þetta skref er valfrjálst.</span><span class="sxs-lookup"><span data-stu-id="c325c-114">This is an optional step.</span></span>  
8. <span data-ttu-id="c325c-115">Veljið Já í svæðinu Mikilvægt starf.</span><span class="sxs-lookup"><span data-stu-id="c325c-115">Select Yes in the Critical Job field.</span></span>
    * <span data-ttu-id="c325c-116">Þetta skref er valfrjálst.</span><span class="sxs-lookup"><span data-stu-id="c325c-116">This is an optional step.</span></span>  
9. <span data-ttu-id="c325c-117">Í reitnum Fylgjast með flokki skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="c325c-117">In the Monitoring category field, select an option.</span></span>
10. <span data-ttu-id="c325c-118">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="c325c-118">Click OK.</span></span>

## <a name="run-in-a-sandbox-environment"></a><span data-ttu-id="c325c-119">Keyrsla í sandkassaumhverfi</span><span class="sxs-lookup"><span data-stu-id="c325c-119">Run in a sandbox environment</span></span>
1. <span data-ttu-id="c325c-120">Smellt er á Runuinnflutningur.</span><span class="sxs-lookup"><span data-stu-id="c325c-120">Click Batch import.</span></span>
2. <span data-ttu-id="c325c-121">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="c325c-121">Click OK.</span></span>

