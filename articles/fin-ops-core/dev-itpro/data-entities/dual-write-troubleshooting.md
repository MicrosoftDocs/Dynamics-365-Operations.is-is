---
title: Leiðbeiningar úrræðaleitar gagnasamþættingar
description: Þetta efni veitir úrræðaleitarupplýsingar um samþættingu gagna á milli forrita Finance and Operations og Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 35c0a1e6342008bc2ee6ff25a1663e199c8cb985
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771026"
---
# <a name="troubleshooting-guide-for-data-integration"></a><span data-ttu-id="dae05-103">Leiðbeiningar úrræðaleitar gagnasamþættingar</span><span class="sxs-lookup"><span data-stu-id="dae05-103">Troubleshooting guide for data integration</span></span>

## <a name="enable-plug-in-trace-logs-in-common-data-service-and-inspect-the-dual-write-plug-in-error-details"></a><span data-ttu-id="dae05-104">Kveiktu á viðbótarrakningarklöddum í Common Data Service og athugaðu upplýsingar um villuleiðbeiningar við tvískipta viðbót</span><span class="sxs-lookup"><span data-stu-id="dae05-104">Enable plug-in trace logs in Common Data Service and inspect the dual-write plug-in error details</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dae05-105">Ef þú lendir í vandræðum eða villum við samstillingu við tvískipta skrifun skaltu fylgja þessum skrefum til að skoða villurnar í rakningakladdanum.</span><span class="sxs-lookup"><span data-stu-id="dae05-105">If you experience an issue or error during dual-write synchronization, follow these steps to inspect the errors in the trace log.</span></span>

1. <span data-ttu-id="dae05-106">Áður en þú getur skoðað villurnar verður þú að virkja viðbótarrakningarkladda fyrst.</span><span class="sxs-lookup"><span data-stu-id="dae05-106">Before you can inspect the errors, you must enable plug-in trace logs.</span></span> <span data-ttu-id="dae05-107">Fyrir leiðbeiningar skal sjá kaflann „Rakningarkladda“ í [Kennsluefni: Skrifaðu og skráðu viðbót](https://docs.microsoft.com/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs).</span><span class="sxs-lookup"><span data-stu-id="dae05-107">For instructions, see the "View trace logs" section of [Tutorial: Write and register a plug-in](https://docs.microsoft.com/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs).</span></span>

    <span data-ttu-id="dae05-108">Núna geturðu skoðað villurnar.</span><span class="sxs-lookup"><span data-stu-id="dae05-108">You can now inspect the errors.</span></span>

2. <span data-ttu-id="dae05-109">Skrá inn á Microsoft Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="dae05-109">Sign in to Microsoft Dynamics 365 Sales.</span></span>
3. <span data-ttu-id="dae05-110">Veldu hnappinn **Stillingar** (gírtáknið) og síðan **Ítarlegar stillingar**.</span><span class="sxs-lookup"><span data-stu-id="dae05-110">Select the **Settings** button (the gear symbol), and then select **Advanced Settings**.</span></span>
4. <span data-ttu-id="dae05-111">Í valmyndinni **Stillingar** velurðu **Sérstillingar \> Rakningarkladdi viðbótar**.</span><span class="sxs-lookup"><span data-stu-id="dae05-111">On the **Settings** menu, select **Customization \> Plug-In Trace Log**.</span></span>
5. <span data-ttu-id="dae05-112">Veldu **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** sem tegundarheiti til að sýna villuupplýsingarnar.</span><span class="sxs-lookup"><span data-stu-id="dae05-112">Select **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** as the type name to show the error details.</span></span>

## <a name="inspect-dual-write-synchronization-errors"></a><span data-ttu-id="dae05-113">Skoðaðu villur í tvöföldum skrifum við samstillingu</span><span class="sxs-lookup"><span data-stu-id="dae05-113">Inspect dual-write synchronization errors</span></span>

<span data-ttu-id="dae05-114">Fylgdu þessum skrefum til að skoða villur við prófun.</span><span class="sxs-lookup"><span data-stu-id="dae05-114">Follow these steps to inspect errors during testing.</span></span>

1. <span data-ttu-id="dae05-115">Skráðu þig inn í Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="dae05-115">Sign in to Microsoft Dynamics Lifecycle Services (LCS).</span></span>
2. <span data-ttu-id="dae05-116">Opnaðu LCS verkefnið til að gera tvískipt próf fyrir.</span><span class="sxs-lookup"><span data-stu-id="dae05-116">Open the LCS project to do dual-write testing for.</span></span>
3. <span data-ttu-id="dae05-117">Veldu **Umhverfi í skýi**.</span><span class="sxs-lookup"><span data-stu-id="dae05-117">Select **Cloud-hosted environments**.</span></span>
4. <span data-ttu-id="dae05-118">Búðu til tengingu fjartengds skjáborðs við sýndarvél (VM) forritsins með því að nota staðbundinn reikning sem er sýndur í LCS.</span><span class="sxs-lookup"><span data-stu-id="dae05-118">Make a Remote desktop connection to the application virtual machine (VM) by using local account that is shown in LCS.</span></span>
5. <span data-ttu-id="dae05-119">Opnaðu tilvikayfirlit.</span><span class="sxs-lookup"><span data-stu-id="dae05-119">Open Event Viewer.</span></span> 
6. <span data-ttu-id="dae05-120">Farðu í **Forrit og þjónustukladdar \> Microsoft \> Dynamics \> AX -DualWriteSync \> Virkt**.</span><span class="sxs-lookup"><span data-stu-id="dae05-120">Go to **Applications and Services Logs \> Microsoft \> Dynamics \> AX-DualWriteSync \> Operational**.</span></span> <span data-ttu-id="dae05-121">Villurnar og smáatriðin eru sýnd.</span><span class="sxs-lookup"><span data-stu-id="dae05-121">The errors and details are shown.</span></span>

## <a name="unlink-one-common-data-service-environment-from-the-application-and-link-another-environment"></a><span data-ttu-id="dae05-122">Aftengdu eitt Common Data Service umhverfi úr forritinu og tengdu annað umhverfi</span><span class="sxs-lookup"><span data-stu-id="dae05-122">Unlink one Common Data Service environment from the application and link another environment</span></span>

<span data-ttu-id="dae05-123">Fylgið eftirfarandi skrefum til að uppfæra tengla:</span><span class="sxs-lookup"><span data-stu-id="dae05-123">Follow these steps to update links.</span></span>

1. <span data-ttu-id="dae05-124">Farðu í umhverfi forritsins.</span><span class="sxs-lookup"><span data-stu-id="dae05-124">Go to the application environment.</span></span>
2. <span data-ttu-id="dae05-125">Opnaðu Gagnastýringu.</span><span class="sxs-lookup"><span data-stu-id="dae05-125">Open Data Management.</span></span>
3. <span data-ttu-id="dae05-126">Veldu **Tengil við CDS fyrir forrit**.</span><span class="sxs-lookup"><span data-stu-id="dae05-126">Select **Link to CDS for apps**.</span></span>
4. <span data-ttu-id="dae05-127">Veldu allar varpanir sem eru í gangi og veldu síðan **Hætta**.</span><span class="sxs-lookup"><span data-stu-id="dae05-127">Select all the mappings that are running, and then select **Stop**.</span></span>
5. <span data-ttu-id="dae05-128">Veldu allar varpanir og smelltu svo á **Eyða**.</span><span class="sxs-lookup"><span data-stu-id="dae05-128">Select all the mappings, and then select **Delete**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="dae05-129">Valkosturinn **Eyða** er ekki tiltækur ef sniðmátið **ViðskiptavinurV3-lykill** er valið.</span><span class="sxs-lookup"><span data-stu-id="dae05-129">The **Delete** option isn't available if the **CustomerV3-Account** template is selected.</span></span> <span data-ttu-id="dae05-130">Hreinsaðu valið á þessu sniðmáti eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="dae05-130">Clear the selection of this template as required.</span></span> <span data-ttu-id="dae05-131">**ViðskiptavinurV3-lykill** er eldra útvegað sniðmát og vinnur með lausninni Prospect to Cash.</span><span class="sxs-lookup"><span data-stu-id="dae05-131">**CustomerV3-Account** is an older provisioned template and works with the Prospect to Cash solution.</span></span> <span data-ttu-id="dae05-132">Þar sem það er gefið út á heimsvísu birtist það undir öllum sniðmátum.</span><span class="sxs-lookup"><span data-stu-id="dae05-132">Because it's globally released, it appears under all templates.</span></span>

6. <span data-ttu-id="dae05-133">Veldu **Aftengja umhverfi**.</span><span class="sxs-lookup"><span data-stu-id="dae05-133">Select **Unlink environment**.</span></span>
7. <span data-ttu-id="dae05-134">Veldu **Já** til að staðfesta aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="dae05-134">Select **Yes** to confirm the operation.</span></span>
8. <span data-ttu-id="dae05-135">Til að tengja nýja umhverfið skaltu fylgja skrefunum í [uppsetningarhandbók](https://aka.ms/dualwrite-docs).</span><span class="sxs-lookup"><span data-stu-id="dae05-135">To link the new environment, follow the steps in the [installation guide](https://aka.ms/dualwrite-docs).</span></span>
