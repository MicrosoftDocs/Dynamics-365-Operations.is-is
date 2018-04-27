--- 
title: "Keyra snið sem notar svæði sem hægt er að stækka lárétt til að bæta gagnvirkt við dálkum í Excel-skýrslur"
description: "Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt snið rafrænnar skýrslugerðar (ER) til að mynda skýrslur sem OPENXML-vinnublöð (Excel) skrár þar sem hægt er að stofna nauðsynlega dálka gagnvirkt sem svið sem má stækka lárétt."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 2d705d0d2803b5254adc27e6715c1eac311898a7
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---
# <a name="run-a-format-that-uses-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports"></a><span data-ttu-id="dea09-103">Keyra snið sem notar svæði sem hægt er að stækka lárétt til að bæta gagnvirkt við dálkum í Excel-skýrslur</span><span class="sxs-lookup"><span data-stu-id="dea09-103">Run a format that uses horizontally-expandable ranges to dynamically add columns in Excel reports</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="dea09-104">Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt snið rafrænnar skýrslugerðar (ER) til að mynda skýrslur sem OPENXML-vinnublöð (Excel) skrár þar sem hægt er að stofna nauðsynlega dálka gagnvirkt sem svið sem má stækka lárétt.</span><span class="sxs-lookup"><span data-stu-id="dea09-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to generate reports as OPENXML worksheets (Excel) files in which the required columns can be created dynamically as horizontally expandable ranges.</span></span> <span data-ttu-id="dea09-105">Hægt er að framkvæma þessum skrefum í DEMF fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="dea09-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="dea09-106">Til að ljúka þessum skrefum, verður fyrst að ljúka við skrefin í á "Rafræn skýrslugerð nota svið sem má stækka lárétt til að bæta við dálkum gagnvirkt við í Excel skýrslum (Hluti 1: hanna skjámynd)" ferli.</span><span class="sxs-lookup"><span data-stu-id="dea09-106">To complete these steps, you must first complete the steps in the “ER Use horizontally expandable ranges to dynamically add columns in Excel reports (Part 1: Design format)” procedure.</span></span>

<span data-ttu-id="dea09-107">Þetta ferli er fyrir eiginleika sem var bætt við í Dynamics 365 for Operations, útgáfu 1611.</span><span class="sxs-lookup"><span data-stu-id="dea09-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="find-created-format"></a><span data-ttu-id="dea09-108">Leita að stofnuðu sniði</span><span class="sxs-lookup"><span data-stu-id="dea09-108">Find created format</span></span>
1. <span data-ttu-id="dea09-109">Fara í Fyrirtækisstjórnun > Rafræn skýrslugerð > Grunnstillingar.</span><span class="sxs-lookup"><span data-stu-id="dea09-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="dea09-110">Í trénu skal víkka út 'Financial dimensions sample model'.</span><span class="sxs-lookup"><span data-stu-id="dea09-110">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="dea09-111">Í trénu skal velja 'Financial dimensions sample model\Sample report with horizontally expandable ranges'.</span><span class="sxs-lookup"><span data-stu-id="dea09-111">In the tree, select 'Financial dimensions sample model\Sample report with horizontally expandable ranges'.</span></span>

## <a name="execute-format-to-create-excel-output"></a><span data-ttu-id="dea09-112">Keyra snið til að stofna Excel-úttak</span><span class="sxs-lookup"><span data-stu-id="dea09-112">Execute format to create Excel output</span></span>
1. <span data-ttu-id="dea09-113">Smellið á „Keyra“.</span><span class="sxs-lookup"><span data-stu-id="dea09-113">Click Run.</span></span>
2. <span data-ttu-id="dea09-114">Í reitinn Heiti víddar skal slá inn 'BusinessUnit;CostCenter;Department'.</span><span class="sxs-lookup"><span data-stu-id="dea09-114">In the Dimension name field, type 'BusinessUnit;CostCenter;Department'.</span></span>
    * <span data-ttu-id="dea09-115">Sláið inn eða veljið gildi í reitnum heiti víddar.</span><span class="sxs-lookup"><span data-stu-id="dea09-115">In the Dimension name field, enter or select a value.</span></span>  <span data-ttu-id="dea09-116">Til að velja allar víddir í núverandi fyrirtæki skal færa inn eftirfarandi:BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="dea09-116">To select all dimensions for the current company, enter the following:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
3. <span data-ttu-id="dea09-117">Útvíkka Færslur til að taka hluta.</span><span class="sxs-lookup"><span data-stu-id="dea09-117">Expand the Records to include section.</span></span>
4. <span data-ttu-id="dea09-118">Smellt er á Síu.</span><span class="sxs-lookup"><span data-stu-id="dea09-118">Click Filter.</span></span>
5. <span data-ttu-id="dea09-119">Velja línuna fyrir töflu færslubókar fjárhags og reitinn rununúmer bókarkeyrslu.</span><span class="sxs-lookup"><span data-stu-id="dea09-119">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
6. <span data-ttu-id="dea09-120">Í svæðinu Skilyrði skal færa inn '00057..00058'.</span><span class="sxs-lookup"><span data-stu-id="dea09-120">In the Criteria field, type '00057..00058'.</span></span>
    * <span data-ttu-id="dea09-121">00057..00058</span><span class="sxs-lookup"><span data-stu-id="dea09-121">00057..00058</span></span>  
7. <span data-ttu-id="dea09-122">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="dea09-122">Click OK.</span></span>
8. <span data-ttu-id="dea09-123">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="dea09-123">Click OK.</span></span>
    * <span data-ttu-id="dea09-124">Fara yfir myndað úttak.</span><span class="sxs-lookup"><span data-stu-id="dea09-124">Review the generated output.</span></span> <span data-ttu-id="dea09-125">Athugið að nýstofnuð Excel-skráin inniheldur sama fjölda dálka sem voru valdar fyrir fjárhagsvíddir.</span><span class="sxs-lookup"><span data-stu-id="dea09-125">Note that the newly created Excel file contains the same number of columns that were selected for financial dimensions.</span></span> <span data-ttu-id="dea09-126">Haus í þeim dálkum táknar heiti fjárhagsvídda.</span><span class="sxs-lookup"><span data-stu-id="dea09-126">The report header in those columns represents financial dimensions’ names.</span></span> <span data-ttu-id="dea09-127">Línur færslanna í þessum dálkum tákna heiti fjárhagsvídda.</span><span class="sxs-lookup"><span data-stu-id="dea09-127">The transactions’ lines in those columns represent financial dimensions.</span></span> <span data-ttu-id="dea09-128">Keyrið þessa skýrslu og veljið mismunandi víddir til að sjá að skýrslan er ekki háð fjölda valinna vídda eða fjölda vídda sem eru grunnstilltar fyrir þetta tilvik Dynamics 365 for Finance and Operations instance.</span><span class="sxs-lookup"><span data-stu-id="dea09-128">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this Dynamics 365 for Finance and Operations instance.</span></span>  


