---
title: Keyra snið til að nota skjalastjórnunarskrár í sniðsúttökum rafrænnar skýrslugerðar
description: Eftirfarandi skref útskýra hvernig notandi með hlutverk kerfisstjóra eða þróunaraðila rafrænnar skýrslugerðar getur stillg snið rafrænnar skýrslugerðar til að nota skjalastjórnunarskrár í rafrænum skýrslum.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustOpenInvoicesListPage, CustInvoiceJournal, SalesTable, ERSolutionTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e87dbb0fa890f4d554c3e2ff09566fb2b1f3206b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "364788"
---
# <a name="run-formats-to-use-document-management-files-in-er-output"></a><span data-ttu-id="ca11d-103">Keyra snið til að nota skjalastjórnunarskrár í sniðsúttökum rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="ca11d-103">Run formats to use Document Management files in ER output</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ca11d-104">Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt snið rafrænnar skýrslugerðar (ER) svo það noti skrár skjalastjórnunar (viðhengi) í rafrænar skýrslur.</span><span class="sxs-lookup"><span data-stu-id="ca11d-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="ca11d-105">Hægt er að framkvæma þessum skrefum í DEMF fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="ca11d-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="ca11d-106">Til að ljúka þessum skrefum, verður fyrst að ljúka við skrefin í á “Rafræn skýrslugerð nota skrár skjalastjórnunar í sniðsúttökum (Hluti 3: stofna snið)” ferli.</span><span class="sxs-lookup"><span data-stu-id="ca11d-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 3: Create format)” procedure.</span></span>

<span data-ttu-id="ca11d-107">Þetta ferli er fyrir eiginleika sem var bætt við í Dynamics 365 for Operations, útgáfu 1611.</span><span class="sxs-lookup"><span data-stu-id="ca11d-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="add-necessary-attachments-for-sales-order-of-a-single-invoice"></a><span data-ttu-id="ca11d-108">Bæta þarf við nauðsynlegum viðhengi fyrir sölupöntun eins reiknings</span><span class="sxs-lookup"><span data-stu-id="ca11d-108">Add necessary attachments for sales order of a single invoice</span></span>
1. <span data-ttu-id="ca11d-109">Farið í Viðskiptakröfur > Reikningar > Opna reikninga viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="ca11d-109">Go to Accounts receivable > Invoices > Open customer invoices.</span></span>
2. <span data-ttu-id="ca11d-110">Nota flýtiafmörkun til að finna færslur</span><span class="sxs-lookup"><span data-stu-id="ca11d-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="ca11d-111">Til dæmis sía á reitnum reikningur með gildinu 'CIV-000148'.</span><span class="sxs-lookup"><span data-stu-id="ca11d-111">For example, filter on the Invoice field with a value of 'CIV-000148'.</span></span>
    * <span data-ttu-id="ca11d-112">CIV-000148</span><span class="sxs-lookup"><span data-stu-id="ca11d-112">CIV-000148</span></span>  
3. <span data-ttu-id="ca11d-113">Smellið til að fylgja tenglinum í valdan reikning.</span><span class="sxs-lookup"><span data-stu-id="ca11d-113">Click to follow the selected invoice’s link.</span></span>
    * <span data-ttu-id="ca11d-114">CIV-000148</span><span class="sxs-lookup"><span data-stu-id="ca11d-114">CIV-000148</span></span>  
4. <span data-ttu-id="ca11d-115">Smellið til að velja tengilinn í reitnum sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="ca11d-115">Click to follow the link in the Sales order field.</span></span>
    * <span data-ttu-id="ca11d-116">000148</span><span class="sxs-lookup"><span data-stu-id="ca11d-116">000148</span></span>  
5. <span data-ttu-id="ca11d-117">Í reitnum Línur eða haus skal velja valkostinn haus.</span><span class="sxs-lookup"><span data-stu-id="ca11d-117">In the Lines or header field, select the option of Header.</span></span>
    * <span data-ttu-id="ca11d-118">Veljið Haus til að gefa til kynna að þetta verði markið til að bæta við viðhengjum.</span><span class="sxs-lookup"><span data-stu-id="ca11d-118">Select Header to indicate that this will be the target for adding attachments.</span></span>  
6. <span data-ttu-id="ca11d-119">Smellt er á Hengja við.</span><span class="sxs-lookup"><span data-stu-id="ca11d-119">Click Attach.</span></span>
    * <span data-ttu-id="ca11d-120">Bæta nokkrar skrár við sem viðhengi fyrir þessa sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="ca11d-120">Add a few files as attachments for this sales order.</span></span> <span data-ttu-id="ca11d-121">Nota skrár af skjalagerðir sem eru studdar af Skjalastjórnun (með skráarendingar DOCX, DPF XML, JPG, o.s.frv.).</span><span class="sxs-lookup"><span data-stu-id="ca11d-121">Use the files of the document types that are supported by the Document Management (with file extensions DOCX, DPF, XML, JPG, etc.).</span></span> <span data-ttu-id="ca11d-122">Flettið og veljið skrár til að hengja við og vinna meira með tengdum reikningi í rafræn skilaboð rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="ca11d-122">Browse and select files to be attached and further processed with the related invoice in the ER electronic message.</span></span>  
7. <span data-ttu-id="ca11d-123">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="ca11d-123">Click New.</span></span>
8. <span data-ttu-id="ca11d-124">Smella á Skrá</span><span class="sxs-lookup"><span data-stu-id="ca11d-124">Click File.</span></span>
9. <span data-ttu-id="ca11d-125">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="ca11d-125">Click New.</span></span>
10. <span data-ttu-id="ca11d-126">Smella á Skrá</span><span class="sxs-lookup"><span data-stu-id="ca11d-126">Click File.</span></span>
11. <span data-ttu-id="ca11d-127">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="ca11d-127">Close the page.</span></span>
12. <span data-ttu-id="ca11d-128">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="ca11d-128">Close the page.</span></span>
13. <span data-ttu-id="ca11d-129">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="ca11d-129">Close the page.</span></span>
14. <span data-ttu-id="ca11d-130">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="ca11d-130">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="ca11d-131">Keyra viðkomandi skýrslu fyrir valinn reikning</span><span class="sxs-lookup"><span data-stu-id="ca11d-131">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="ca11d-132">Fara í Fyrirtækisstjórnun > Rafræn skýrslugerð > Grunnstillingar.</span><span class="sxs-lookup"><span data-stu-id="ca11d-132">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="ca11d-133">Í trénu, veljið 'Customer invoice model'.</span><span class="sxs-lookup"><span data-stu-id="ca11d-133">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="ca11d-134">Í trénu skal víkka út 'Customer invoice model\Customer invoice model (custom)'.</span><span class="sxs-lookup"><span data-stu-id="ca11d-134">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="ca11d-135">Í trénu, veljið 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span><span class="sxs-lookup"><span data-stu-id="ca11d-135">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="ca11d-136">Smellið á „Keyra“.</span><span class="sxs-lookup"><span data-stu-id="ca11d-136">Click Run.</span></span>
6. <span data-ttu-id="ca11d-137">Útvíkka Færslur til að taka () hluta.</span><span class="sxs-lookup"><span data-stu-id="ca11d-137">Expand the Records to include () section.</span></span>
7. <span data-ttu-id="ca11d-138">Smellt er á Síu.</span><span class="sxs-lookup"><span data-stu-id="ca11d-138">Click Filter.</span></span>
8. <span data-ttu-id="ca11d-139">Velja línu reikningabókar viðskiptavinar og reitinn sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="ca11d-139">Select the row of the Customer invoice journal and the Sales order field.</span></span>
9. <span data-ttu-id="ca11d-140">Í svæðinu Skilyrði skal færa inn '000148'.</span><span class="sxs-lookup"><span data-stu-id="ca11d-140">In the Criteria field, type '000148'.</span></span>
    * <span data-ttu-id="ca11d-141">Í forsendusvæðinu “sölupöntun”, skal færa inn pöntunarnúmer 000148.</span><span class="sxs-lookup"><span data-stu-id="ca11d-141">In the criteria “Sales order” field, type the order number 000148.</span></span>  
10. <span data-ttu-id="ca11d-142">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="ca11d-142">Click OK.</span></span>
11. <span data-ttu-id="ca11d-143">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="ca11d-143">Click OK.</span></span>
    * <span data-ttu-id="ca11d-144">Fara yfir myndað úttak.</span><span class="sxs-lookup"><span data-stu-id="ca11d-144">Review the generated output.</span></span> <span data-ttu-id="ca11d-145">Athugið að fyrir hvert viðhengi hefur verið stofnað einu xml-hnútur.</span><span class="sxs-lookup"><span data-stu-id="ca11d-145">Note that for each attachment a single XML node has been created.</span></span> <span data-ttu-id="ca11d-146">Innihald viðhengis er notað til að fylla út í úttak XML í MIME (base64) textasnið.</span><span class="sxs-lookup"><span data-stu-id="ca11d-146">The attachment’s content is populated to the XML output in MIME (base64) text format.</span></span>  

