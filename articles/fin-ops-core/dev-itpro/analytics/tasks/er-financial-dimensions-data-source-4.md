---
title: Rafræn skýrslugerð Nota Fjárhagsvíddir sem gagnaveita (Hluti 4 - keyra skýrslu)
description: Þetta efni útskýrir hvernig á að skilgreina líkan rafrænnar skýrslugerðar til að nota fjárhagsvíddir sem gagnagjafa fyrir skýrslur rafrænnar skýrslugerðar. (Hluti 4)
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c1fe332de84339d3369ba495ca13f50c4901f366
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092276"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-4---run-the-report"></a><span data-ttu-id="fabf9-104">Rafræn skýrslugerð Nota Fjárhagsvíddir sem gagnaveita (Hluti 4 - keyra skýrslu)</span><span class="sxs-lookup"><span data-stu-id="fabf9-104">ER Use financial dimensions as a data source (Part 4 - Run the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fabf9-105">Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt líkan rafrænnar skýrslugerðar (ER) svo það noti fjárhagsvíddir sem gagnaveitu fyrir rafrænar skýrslur.</span><span class="sxs-lookup"><span data-stu-id="fabf9-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="fabf9-106">Hægt er að framkvæma þessum skrefum í DEMF fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="fabf9-106">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="fabf9-107">Til að ljúka þessum skrefum, verður fyrst að ljúka við skrefin í ferlinu „ER Nota fjárhagsvíddir sem gagnaveitu (Hluti 3: hanna skýrslu)”.</span><span class="sxs-lookup"><span data-stu-id="fabf9-107">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 3: Design the report)" procedure.</span></span> <span data-ttu-id="fabf9-108">Einnig þarf að skilgreina sjálfgefnar gerðir skjala á færibreytusíðu Rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="fabf9-108">You must also configure default document types on the Electronic reporting parameters page.</span></span> <span data-ttu-id="fabf9-109">Sjálfgefið gerðir skjala eru einnig stilltar þegar þú sækir og flytja inn hvers kyns grunnstillingar ræfrænna skýrslna (ER).</span><span class="sxs-lookup"><span data-stu-id="fabf9-109">Default document types are also set when you download and import any ER configuration.</span></span> 


## <a name="run-report"></a><span data-ttu-id="fabf9-110">Keyra skýrslu.</span><span class="sxs-lookup"><span data-stu-id="fabf9-110">Run report</span></span>
1. <span data-ttu-id="fabf9-111">Fara í Fyrirtækisstjórnun > Rafræn skýrslugerð > Grunnstillingar.</span><span class="sxs-lookup"><span data-stu-id="fabf9-111">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="fabf9-112">Í trénu skal víkka út 'Financial dimensions sample model'.</span><span class="sxs-lookup"><span data-stu-id="fabf9-112">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="fabf9-113">Í trénu skal velja 'Financial dimensions sample model\Ledger journal report'.</span><span class="sxs-lookup"><span data-stu-id="fabf9-113">In the tree, select 'Financial dimensions sample model\Ledger journal report'.</span></span>
4. <span data-ttu-id="fabf9-114">Smella á Keyra.</span><span class="sxs-lookup"><span data-stu-id="fabf9-114">Click Run.</span></span>
<span data-ttu-id="fabf9-115">![Skilgreiningarsíða í ER](../media/er-financial-dimensions-guides-run1.png)</span><span class="sxs-lookup"><span data-stu-id="fabf9-115">![ER configurations page](../media/er-financial-dimensions-guides-run1.png)</span></span>
5. <span data-ttu-id="fabf9-116">Sláið inn eða veljið gildi í reitnum heiti víddar.</span><span class="sxs-lookup"><span data-stu-id="fabf9-116">In the Dimension name field, enter or select a value.</span></span>
    * <span data-ttu-id="fabf9-117">Til að velja allar víddir í núverandi fyrirtæki skal færa inn eftirfarandi upplýsingar:</span><span class="sxs-lookup"><span data-stu-id="fabf9-117">To select all dimensions in the current company, enter the following information:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
![Skilgreiningarsíða í ER](../media/er-financial-dimensions-guides-run2.png)
6. <span data-ttu-id="fabf9-119">Útvíkka Færslur til að taka hluta.</span><span class="sxs-lookup"><span data-stu-id="fabf9-119">Expand the Records to include section.</span></span>
7. <span data-ttu-id="fabf9-120">Smellt er á Síu.</span><span class="sxs-lookup"><span data-stu-id="fabf9-120">Click Filter.</span></span>
8. <span data-ttu-id="fabf9-121">Velja línuna fyrir töflu færslubókar fjárhags og reitinn rununúmer bókarkeyrslu.</span><span class="sxs-lookup"><span data-stu-id="fabf9-121">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
9. <span data-ttu-id="fabf9-122">Í svæðinu Skilyrði skal færa inn '00057'.</span><span class="sxs-lookup"><span data-stu-id="fabf9-122">In the Criteria field, type '00057'.</span></span>
10. <span data-ttu-id="fabf9-123">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="fabf9-123">Click OK.</span></span>
11. <span data-ttu-id="fabf9-124">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="fabf9-124">Click OK.</span></span>
<span data-ttu-id="fabf9-125">![Skilgreiningarsíða í ER](../media/er-financial-dimensions-guides-run3.png)</span><span class="sxs-lookup"><span data-stu-id="fabf9-125">![ER configurations page](../media/er-financial-dimensions-guides-run3.png)</span></span>
    * <span data-ttu-id="fabf9-126">Fara yfir myndað úttak.</span><span class="sxs-lookup"><span data-stu-id="fabf9-126">Review the generated output.</span></span> <span data-ttu-id="fabf9-127">Fyrir hverja færslu fyrir valda runu eru birtar fjárhagsvíddir úr viðeigandi víddarmengjum.</span><span class="sxs-lookup"><span data-stu-id="fabf9-127">For each transaction of the selected batch, the financial dimensions from the corresponding dimensions set are presented.</span></span> <span data-ttu-id="fabf9-128">Keyra þessa skýrslu og veljið mismunandi víddir til að sjá að skýrslan er ekki háð fjölda valinna vídda eða fjölda vídda sem skilgreint er fyrir þetta tilvik.</span><span class="sxs-lookup"><span data-stu-id="fabf9-128">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this instance.</span></span>  
![Skilgreiningarsíða í ER](../media/er-financial-dimensions-guides-run4.png)
