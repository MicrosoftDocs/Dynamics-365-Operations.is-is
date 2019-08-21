---
title: Leiðbeiningar úrræðaleitar gagnasamþættingar
description: Þetta efni veitir úrræðaleitarupplýsingar um samþættingu gagna á milli Microsoft Dynamics 365 for Finance and Operations og Common Data Service.
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
ms.openlocfilehash: ca62a6b3aa64ec2383ee3ded3b7bbf4650a41166
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797276"
---
# <a name="troubleshooting-guide-for-data-integration"></a><span data-ttu-id="4841c-103">Leiðbeiningar úrræðaleitar gagnasamþættingar</span><span class="sxs-lookup"><span data-stu-id="4841c-103">Troubleshooting guide for data integration</span></span>

## <a name="enable-plugin-trace-in-common-data-service-and-check-the-dual-write-plugin-error-details"></a><span data-ttu-id="4841c-104">Kveiktu á viðbótarsporun í Common Data Service og athugaðu upplýsingar um villuleiðbeiningar við tvískipta viðbót</span><span class="sxs-lookup"><span data-stu-id="4841c-104">Enable Plugin Trace in Common Data Service and check the dual-write Plugin error details</span></span>

<span data-ttu-id="4841c-105">Ef þú ert í vandræðum eða villu með tvískiptri samstillingu, geturðu skoðað villurnar í rakningarkladdanum:</span><span class="sxs-lookup"><span data-stu-id="4841c-105">If you are facing an issue or error with dual-write synchronization, you can inspect the errors in the trace log:</span></span>

1. <span data-ttu-id="4841c-106">Áður en þú getur skoðað villurnar verður þú að virkja viðbótarsporun með því að nota leiðbeiningarnar í [Skráðu viðbót](https://docs.microsoft.com/en-us/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs) til að virkja viðbótarsporunina.</span><span class="sxs-lookup"><span data-stu-id="4841c-106">Before you can inspect the errors, you must enable Plugin trace using the instructions in [Register plug-in](https://docs.microsoft.com/en-us/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs) to enable Plugin trace.</span></span> <span data-ttu-id="4841c-107">Nú geturðu skoðað villurnar.</span><span class="sxs-lookup"><span data-stu-id="4841c-107">Now you can inspect the errors.</span></span>
2. <span data-ttu-id="4841c-108">Skrá inn á Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="4841c-108">Login to Dynamics 365 for Sales.</span></span>
3. <span data-ttu-id="4841c-109">Smelltu á stillingartáknið (gír) og veldu **Ítarlegar stillingar**.</span><span class="sxs-lookup"><span data-stu-id="4841c-109">Click on the Settings icon (a gear), and select **Advanced Settings**.</span></span>
4. <span data-ttu-id="4841c-110">Í valmyndinni **Stillingar** velurðu **Sérstillingar > Rakningarkladdi viðbótarsporunar**.</span><span class="sxs-lookup"><span data-stu-id="4841c-110">In the **Settings** menu, choose **Customization > Plug-In Trace Log**.</span></span>
5. <span data-ttu-id="4841c-111">Smelltu á tegundarheitið **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** til að birta villuupplýsingarnar.</span><span class="sxs-lookup"><span data-stu-id="4841c-111">Click the type name **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** to display the error details.</span></span>

## <a name="check-dual-write-synchronization-errors-in-finance-and-operations"></a><span data-ttu-id="4841c-112">Athugaðu tvískiptar samstillingarvillur í Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="4841c-112">Check dual-write synchronization errors in Finance and Operations</span></span>

<span data-ttu-id="4841c-113">Þú getur athugað villurnar við prófun með því að fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="4841c-113">You can check the errors during testing by following these steps:</span></span>

+ <span data-ttu-id="4841c-114">Skráðu þig inn í Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="4841c-114">Login to LifeCycle Services (LCS).</span></span>
+ <span data-ttu-id="4841c-115">Opnaðu LCS-verkið sem þú valdir til að framkvæma tvískipt próf.</span><span class="sxs-lookup"><span data-stu-id="4841c-115">Open the LCS project that you chose to perform dual-write testing.</span></span>
+ <span data-ttu-id="4841c-116">Farðu í Umhverfi í skýi.</span><span class="sxs-lookup"><span data-stu-id="4841c-116">Go to Cloud Hosted Environments.</span></span>
+ <span data-ttu-id="4841c-117">Fjartengt skjáborð til Finance and Operations VM með staðbundnum lykli sem birtist í LCS.</span><span class="sxs-lookup"><span data-stu-id="4841c-117">Remote desktop to Finance and Operations VM using local account that is displayed in LCS.</span></span>
+ <span data-ttu-id="4841c-118">Opnaðu tilvikayfirlit.</span><span class="sxs-lookup"><span data-stu-id="4841c-118">Open the event viewer.</span></span> 
+ <span data-ttu-id="4841c-119">Farðu í **Forrit og þjónustukladdar > Microsoft > Dynamics > AX -DualWriteSync > Virkt**.</span><span class="sxs-lookup"><span data-stu-id="4841c-119">Navigate to **Applications and Services logs > Microsoft > Dynamics > AX-DualWriteSync > Operational**.</span></span> <span data-ttu-id="4841c-120">Villurnar og smáatriðin birtast.</span><span class="sxs-lookup"><span data-stu-id="4841c-120">The errors and details are displayed.</span></span>

## <a name="how-to-unlink-and-link-another-common-data-service-environment-from-finance-and-operations"></a><span data-ttu-id="4841c-121">Hvernig á að aftengja og tengja annað Common Data Service umhverfi frá Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="4841c-121">How to unlink and link another Common Data Service environment from Finance and Operations</span></span>

<span data-ttu-id="4841c-122">Þú getur uppfært tengla með því að fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="4841c-122">You can update links by following these steps:</span></span>

+ <span data-ttu-id="4841c-123">Farðu í Finance and Operations umhverfið.</span><span class="sxs-lookup"><span data-stu-id="4841c-123">Navigate to the Finance and Operations environment.</span></span>
+ <span data-ttu-id="4841c-124">Opnaðu Gagnastýringu.</span><span class="sxs-lookup"><span data-stu-id="4841c-124">Open Data Management.</span></span>
+ <span data-ttu-id="4841c-125">Smelltu á **Tengil við CDS fyrir forrit**.</span><span class="sxs-lookup"><span data-stu-id="4841c-125">Click on **Link to CDS for apps**.</span></span>
+ <span data-ttu-id="4841c-126">Veldu allar keyrandi kortlagningar og smelltu á **Hætta**.</span><span class="sxs-lookup"><span data-stu-id="4841c-126">Select all the running mappings and click **Stop**.</span></span> 
+ <span data-ttu-id="4841c-127">Veldu allar kortlagningar og smelltu á **Eyða**.</span><span class="sxs-lookup"><span data-stu-id="4841c-127">Select all the mappings and click **Delete**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="4841c-128">Valkosturinn **Eyða** birtist ekki ef sniðmátið **ViðskiptavinurV3-lykill** er valið.</span><span class="sxs-lookup"><span data-stu-id="4841c-128">The **Delete** option will not appear if **CustomerV3-Account** template is selected.</span></span> <span data-ttu-id="4841c-129">Afturkallaðu það ef þörf er á.</span><span class="sxs-lookup"><span data-stu-id="4841c-129">Unselect it if needed.</span></span> <span data-ttu-id="4841c-130">**ViðskiptavinurV3-lykill** er eldra útvegað sniðmát og vinnur með lausninni Prospect to Cash.</span><span class="sxs-lookup"><span data-stu-id="4841c-130">**CustomerV3-Account** is an older provisioned template and works with the Prospect to Cash solution.</span></span> <span data-ttu-id="4841c-131">Vegna þess að það er gefið út á heimsvísu birtist það undir öllum sniðmátum.</span><span class="sxs-lookup"><span data-stu-id="4841c-131">Because it is globally released, it shows up under all templates.</span></span>

+ <span data-ttu-id="4841c-132">Smelltu á **Aftengja umhverfi**.</span><span class="sxs-lookup"><span data-stu-id="4841c-132">Click **Unlink environment**.</span></span>
+ <span data-ttu-id="4841c-133">Smelltu á **Já** til staðfestingar.</span><span class="sxs-lookup"><span data-stu-id="4841c-133">Click **Yes** for confirmation.</span></span>
+ <span data-ttu-id="4841c-134">Til að tengja nýja umhverfið skaltu fylgja skrefunum í [uppsetningarhandbók](https://aka.ms/dualwrite-docs).</span><span class="sxs-lookup"><span data-stu-id="4841c-134">To link the new environment, follow the steps in the [installation guide](https://aka.ms/dualwrite-docs).</span></span>

