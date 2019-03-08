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
ms.openlocfilehash: 339cc1d3bcdc1dc93b796c385d2165f45f8f7ecf
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "338729"
---
# <a name="import-users-in-bulk"></a><span data-ttu-id="c92af-103">Flytja inn marga notendur í einu</span><span class="sxs-lookup"><span data-stu-id="c92af-103">Import users in bulk</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c92af-104">Þetta ferli geta kerfisstjórar notað til að flytja inn stóra hópa notenda frá Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c92af-104">This procedure can be used by system administrators to import a large number of users from Azure Active Directory.</span></span>


## <a name="run-as-a-batch-job"></a><span data-ttu-id="c92af-105">Keyra sem runuvinnslu</span><span class="sxs-lookup"><span data-stu-id="c92af-105">Run as a batch job</span></span>
1. <span data-ttu-id="c92af-106">Farið í Kerfisstjórnun > Notendur > Notendur.</span><span class="sxs-lookup"><span data-stu-id="c92af-106">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="c92af-107">Smellt er á Runuinnflutningur.</span><span class="sxs-lookup"><span data-stu-id="c92af-107">Click Batch import.</span></span>
3. <span data-ttu-id="c92af-108">Stækka útvíkkun á liðnum Keyra í bakgrunni.</span><span class="sxs-lookup"><span data-stu-id="c92af-108">Expand the Run in the background section.</span></span>
4. <span data-ttu-id="c92af-109">Veljið Já í svæðinu runuvinnsla.</span><span class="sxs-lookup"><span data-stu-id="c92af-109">Select Yes in the Batch processing field.</span></span>
5. <span data-ttu-id="c92af-110">Slá inn gildi í reitinn Verklýsing.</span><span class="sxs-lookup"><span data-stu-id="c92af-110">In the Task description field, type a value.</span></span>
6. <span data-ttu-id="c92af-111">Sláið inn eða veldu gildi í reitnum Runuflokkur.</span><span class="sxs-lookup"><span data-stu-id="c92af-111">In the Batch group field, enter or select a value.</span></span>
    * <span data-ttu-id="c92af-112">Þetta skref er valfrjálst.</span><span class="sxs-lookup"><span data-stu-id="c92af-112">This is an optional step.</span></span>  
7. <span data-ttu-id="c92af-113">Veljið Já í reitnum Einka.</span><span class="sxs-lookup"><span data-stu-id="c92af-113">Select Yes in the Private field.</span></span>
    * <span data-ttu-id="c92af-114">Þetta skref er valfrjálst.</span><span class="sxs-lookup"><span data-stu-id="c92af-114">This is an optional step.</span></span>  
8. <span data-ttu-id="c92af-115">Veljið Já í svæðinu Mikilvægt starf.</span><span class="sxs-lookup"><span data-stu-id="c92af-115">Select Yes in the Critical Job field.</span></span>
    * <span data-ttu-id="c92af-116">Þetta skref er valfrjálst.</span><span class="sxs-lookup"><span data-stu-id="c92af-116">This is an optional step.</span></span>  
9. <span data-ttu-id="c92af-117">Í reitnum Fylgjast með flokki skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="c92af-117">In the Monitoring category field, select an option.</span></span>
10. <span data-ttu-id="c92af-118">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="c92af-118">Click OK.</span></span>

## <a name="run-in-a-sandbox-environment"></a><span data-ttu-id="c92af-119">Keyrsla í sandkassaumhverfi</span><span class="sxs-lookup"><span data-stu-id="c92af-119">Run in a sandbox environment</span></span>
1. <span data-ttu-id="c92af-120">Smellt er á Runuinnflutningur.</span><span class="sxs-lookup"><span data-stu-id="c92af-120">Click Batch import.</span></span>
2. <span data-ttu-id="c92af-121">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="c92af-121">Click OK.</span></span>

