---
title: Rafræn skýrslugerð nota skrár skjalastjórnunar í sniðsúttökum (Hluti 4 - keyra snið)
description: Í þessu efni er útskýrt hvernig á að skilgreina snið rafrænnar skýrslugerðar til að nota skrár skjalastjórnunar í úttaki rafrænnar skýrslugerðar. (Hluti 4)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustOpenInvoicesListPage, CustInvoiceJournal, SalesTable, ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d437b31b8a55f345ebc3567bc8c6a2c5ecfd2eec
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092517"
---
# <a name="er-use-document-management-files-in-format-outputs-part-4---run-format"></a><span data-ttu-id="1c4bf-104">Rafræn skýrslugerð nota skrár skjalastjórnunar í sniðsúttökum (Hluti 4 - keyra snið)</span><span class="sxs-lookup"><span data-stu-id="1c4bf-104">ER Use Document Management files in format outputs (Part 4 - Run format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1c4bf-105">Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt snið rafrænnar skýrslugerðar (ER) svo það noti skrár skjalastjórnunar (viðhengi) í rafrænar skýrslur.</span><span class="sxs-lookup"><span data-stu-id="1c4bf-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="1c4bf-106">Hægt er að framkvæma þessum skrefum í DEMF fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="1c4bf-106">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="1c4bf-107">Til að ljúka þessum skrefum, verður fyrst að ljúka við skrefin í ferlinu „Rafræn skýrslugerð nota skrár skjalastjórnunar í sniðsúttökum (Hluti 3: stofna snið)”.</span><span class="sxs-lookup"><span data-stu-id="1c4bf-107">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 3: Create format)" procedure.</span></span>

<span data-ttu-id="1c4bf-108">Þetta ferli er fyrir eiginleika sem var bætt við í Dynamics 365 for Operations, útgáfu 1611.</span><span class="sxs-lookup"><span data-stu-id="1c4bf-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="add-necessary-attachments-for-sales-order-of-a-single-invoice"></a><span data-ttu-id="1c4bf-109">Bæta þarf við nauðsynlegum viðhengi fyrir sölupöntun eins reiknings</span><span class="sxs-lookup"><span data-stu-id="1c4bf-109">Add necessary attachments for sales order of a single invoice</span></span>
1. <span data-ttu-id="1c4bf-110">Farið í Viðskiptakröfur > Reikningar > Opna reikninga viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="1c4bf-110">Go to Accounts receivable > Invoices > Open customer invoices.</span></span>
2. <span data-ttu-id="1c4bf-111">Nota flýtiafmörkun til að finna færslur</span><span class="sxs-lookup"><span data-stu-id="1c4bf-111">Use the Quick Filter to find records.</span></span> <span data-ttu-id="1c4bf-112">Til dæmis sía á reitnum reikningur með gildinu 'CIV-000148'.</span><span class="sxs-lookup"><span data-stu-id="1c4bf-112">For example, filter on the Invoice field with a value of 'CIV-000148'.</span></span>
    * <span data-ttu-id="1c4bf-113">CIV-000148</span><span class="sxs-lookup"><span data-stu-id="1c4bf-113">CIV-000148</span></span>  
3. <span data-ttu-id="1c4bf-114">Smellið til að fylgja tengli í valdinn reikning.</span><span class="sxs-lookup"><span data-stu-id="1c4bf-114">Click to follow the selected invoice's link.</span></span>
    * <span data-ttu-id="1c4bf-115">CIV-000148</span><span class="sxs-lookup"><span data-stu-id="1c4bf-115">CIV-000148</span></span>  
4. <span data-ttu-id="1c4bf-116">Smellið til að velja tengilinn í reitnum sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="1c4bf-116">Click to follow the link in the Sales order field.</span></span>
    * <span data-ttu-id="1c4bf-117">000148</span><span class="sxs-lookup"><span data-stu-id="1c4bf-117">000148</span></span>  
5. <span data-ttu-id="1c4bf-118">Í reitnum Línur eða haus skal velja valkostinn haus.</span><span class="sxs-lookup"><span data-stu-id="1c4bf-118">In the Lines or header field, select the option of Header.</span></span>
    * <span data-ttu-id="1c4bf-119">Veljið Haus til að gefa til kynna að þetta verði markið til að bæta við viðhengjum.</span><span class="sxs-lookup"><span data-stu-id="1c4bf-119">Select Header to indicate that this will be the target for adding attachments.</span></span>  
6. <span data-ttu-id="1c4bf-120">Smellt er á Hengja við.</span><span class="sxs-lookup"><span data-stu-id="1c4bf-120">Click Attach.</span></span>
    * <span data-ttu-id="1c4bf-121">Bæta nokkrar skrár við sem viðhengi fyrir þessa sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="1c4bf-121">Add a few files as attachments for this sales order.</span></span> <span data-ttu-id="1c4bf-122">Nota skrár af skjalagerðir sem eru studdar af Skjalastjórnun (með skráarendingar DOCX, DPF XML, JPG, o.s.frv.).</span><span class="sxs-lookup"><span data-stu-id="1c4bf-122">Use the files of the document types that are supported by the Document Management (with file extensions DOCX, DPF, XML, JPG, etc.).</span></span> <span data-ttu-id="1c4bf-123">Flettið og veljið skrár til að hengja við og vinna meira með tengdum reikningi í rafræn skilaboð rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="1c4bf-123">Browse and select files to be attached and further processed with the related invoice in the ER electronic message.</span></span>  
7. <span data-ttu-id="1c4bf-124">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="1c4bf-124">Click New.</span></span>
8. <span data-ttu-id="1c4bf-125">Smella á Skrá</span><span class="sxs-lookup"><span data-stu-id="1c4bf-125">Click File.</span></span>
9. <span data-ttu-id="1c4bf-126">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="1c4bf-126">Click New.</span></span>
10. <span data-ttu-id="1c4bf-127">Smella á Skrá</span><span class="sxs-lookup"><span data-stu-id="1c4bf-127">Click File.</span></span>
11. <span data-ttu-id="1c4bf-128">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="1c4bf-128">Close the page.</span></span>
12. <span data-ttu-id="1c4bf-129">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="1c4bf-129">Close the page.</span></span>
13. <span data-ttu-id="1c4bf-130">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="1c4bf-130">Close the page.</span></span>
14. <span data-ttu-id="1c4bf-131">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="1c4bf-131">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="1c4bf-132">Keyra viðkomandi skýrslu fyrir valinn reikning</span><span class="sxs-lookup"><span data-stu-id="1c4bf-132">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="1c4bf-133">Fara í Fyrirtækisstjórnun > Rafræn skýrslugerð > Grunnstillingar.</span><span class="sxs-lookup"><span data-stu-id="1c4bf-133">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="1c4bf-134">Í trénu, veljið 'Customer invoice model'.</span><span class="sxs-lookup"><span data-stu-id="1c4bf-134">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="1c4bf-135">Í trénu skal víkka út 'Customer invoice model\Customer invoice model (custom)'.</span><span class="sxs-lookup"><span data-stu-id="1c4bf-135">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="1c4bf-136">Í trénu, veljið 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span><span class="sxs-lookup"><span data-stu-id="1c4bf-136">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="1c4bf-137">Smellið á „Keyra“.</span><span class="sxs-lookup"><span data-stu-id="1c4bf-137">Click Run.</span></span>
6. <span data-ttu-id="1c4bf-138">Útvíkka Færslur til að taka () hluta.</span><span class="sxs-lookup"><span data-stu-id="1c4bf-138">Expand the Records to include () section.</span></span>
7. <span data-ttu-id="1c4bf-139">Smellt er á Síu.</span><span class="sxs-lookup"><span data-stu-id="1c4bf-139">Click Filter.</span></span>
8. <span data-ttu-id="1c4bf-140">Velja línu reikningabókar viðskiptavinar og reitinn sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="1c4bf-140">Select the row of the Customer invoice journal and the Sales order field.</span></span>
9. <span data-ttu-id="1c4bf-141">Í svæðinu Skilyrði skal færa inn '000148'.</span><span class="sxs-lookup"><span data-stu-id="1c4bf-141">In the Criteria field, type '000148'.</span></span>
    * <span data-ttu-id="1c4bf-142">Í forsendusvæðinu „sölupöntun” skal færa inn pöntunarnúmer 000148.</span><span class="sxs-lookup"><span data-stu-id="1c4bf-142">In the criteria "Sales order" field, type the order number 000148.</span></span>  
10. <span data-ttu-id="1c4bf-143">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="1c4bf-143">Click OK.</span></span>
11. <span data-ttu-id="1c4bf-144">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="1c4bf-144">Click OK.</span></span>
    * <span data-ttu-id="1c4bf-145">Fara yfir myndað úttak.</span><span class="sxs-lookup"><span data-stu-id="1c4bf-145">Review the generated output.</span></span> <span data-ttu-id="1c4bf-146">Athugið að fyrir hvert viðhengi hefur verið stofnað einu xml-hnútur.</span><span class="sxs-lookup"><span data-stu-id="1c4bf-146">Note that for each attachment a single XML node has been created.</span></span> <span data-ttu-id="1c4bf-147">Innihald viðhengis er notað til að fylla út í úttak XML í MIME (base64) textasnið.</span><span class="sxs-lookup"><span data-stu-id="1c4bf-147">The attachment's content is populated to the XML output in MIME (base64) text format.</span></span>  

