---
title: Rafræn skýrslugerð nota skrár skjalastjórnunar í sniðsúttökum(Hluti 2 - framlengja gagnalíkan)
description: Í þessu efni er útskýrt hvernig á að skilgreina snið rafrænnar skýrslugerðar til að nota skrár skjalastjórnunar (viðhengi) í úttaki rafrænnar skýrslugerðar. (Hluti 2)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9cd06cdfd9bae57577c2e3ec97848e319b197f41
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092592"
---
# <a name="er-use-document-management-files-in-format-outputs-part-2---extend-data-model"></a><span data-ttu-id="b92a5-104">Rafræn skýrslugerð nota skrár skjalastjórnunar í sniðsúttökum(Hluti 2 - framlengja gagnalíkan)</span><span class="sxs-lookup"><span data-stu-id="b92a5-104">ER Use Document Management files in format outputs (Part 2 - Extend data model)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b92a5-105">Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt snið rafrænnar skýrslugerðar (ER) svo það noti skrár skjalastjórnunar (viðhengi) í rafrænar skýrslur.</span><span class="sxs-lookup"><span data-stu-id="b92a5-105">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="b92a5-106">Hægt er að framkvæma þessum skrefum í Hvaða fyrirtæki sem er.</span><span class="sxs-lookup"><span data-stu-id="b92a5-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="b92a5-107">Til að ljúka þessum skrefum, verður fyrst að ljúka við skrefin í verkleiðbeiningunum „Rafræn skýrslugerð nota skrár skjalastjórnunar í sniðsúttökum (Hluti 1: undirbúa gagnalíkan)”.</span><span class="sxs-lookup"><span data-stu-id="b92a5-107">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 1: Prepare data model)" task guide.</span></span>

<span data-ttu-id="b92a5-108">Þetta ferli er fyrir eiginleika sem var bætt við í Dynamics 365 for Operations, útgáfu 1611.</span><span class="sxs-lookup"><span data-stu-id="b92a5-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a><span data-ttu-id="b92a5-109">Framlengja gagnalíkan til að birta skrár Skjalastjórnunar í því</span><span class="sxs-lookup"><span data-stu-id="b92a5-109">Extend data model to present the Document Management files in it</span></span>
1. <span data-ttu-id="b92a5-110">Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="b92a5-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="b92a5-111">Smelltu á Grunnstillingar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="b92a5-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="b92a5-112">Í trénu, veljið 'Customer invoice model'.</span><span class="sxs-lookup"><span data-stu-id="b92a5-112">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="b92a5-113">Í trénu, veljið 'Customer invoice model\Customer invoice model (custom)'.</span><span class="sxs-lookup"><span data-stu-id="b92a5-113">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
5. <span data-ttu-id="b92a5-114">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="b92a5-114">Click Designer.</span></span>
6. <span data-ttu-id="b92a5-115">Í trénu skal velja select 'Customer invoice(InvoiceCustomer)'.</span><span class="sxs-lookup"><span data-stu-id="b92a5-115">In the tree, select 'Customer invoice(InvoiceCustomer)'.</span></span>
    * <span data-ttu-id="b92a5-116">Við munum útvíkka þetta gagnalíkan til að birta það í öllum skrám sem hafa verið tengdar við sölupöntun sem er tengt við rafrænt unninn reikning.</span><span class="sxs-lookup"><span data-stu-id="b92a5-116">We will extend this data model to expose in it any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
7. <span data-ttu-id="b92a5-117">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="b92a5-117">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="b92a5-118">Í svæðið Heiti, færðu inn 'viðhengi reiknings'.</span><span class="sxs-lookup"><span data-stu-id="b92a5-118">In the Name field, type 'Invoice attachments'.</span></span>
    * <span data-ttu-id="b92a5-119">Viðhengi reiknings</span><span class="sxs-lookup"><span data-stu-id="b92a5-119">Invoice attachments</span></span>  
9. <span data-ttu-id="b92a5-120">Veljið í svæðinu gerð Vöru „Skrárlisti".</span><span class="sxs-lookup"><span data-stu-id="b92a5-120">In the Item type field, select 'Record list'.</span></span>
10. <span data-ttu-id="b92a5-121">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="b92a5-121">Click Add.</span></span>
11. <span data-ttu-id="b92a5-122">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="b92a5-122">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="b92a5-123">Í svæðið Heiti, færðu inn 'innihald skráa'.</span><span class="sxs-lookup"><span data-stu-id="b92a5-123">In the Name field, type 'File content'.</span></span>
    * <span data-ttu-id="b92a5-124">Innihald skráar</span><span class="sxs-lookup"><span data-stu-id="b92a5-124">File content</span></span>  
13. <span data-ttu-id="b92a5-125">Velja 'geymir' í svæðinu gerð Vöru.</span><span class="sxs-lookup"><span data-stu-id="b92a5-125">In the Item type field, select 'Container'.</span></span>
14. <span data-ttu-id="b92a5-126">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="b92a5-126">Click Add.</span></span>
15. <span data-ttu-id="b92a5-127">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="b92a5-127">Click New to open the drop dialog.</span></span>
16. <span data-ttu-id="b92a5-128">Í svæðið Heiti, færðu inn 'skrárnafn'.</span><span class="sxs-lookup"><span data-stu-id="b92a5-128">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="b92a5-129">Skrárnafn</span><span class="sxs-lookup"><span data-stu-id="b92a5-129">File name</span></span>  
17. <span data-ttu-id="b92a5-130">Veljið 'Strengur' í svæðinu Vöru.</span><span class="sxs-lookup"><span data-stu-id="b92a5-130">In the Item type field, select 'String'.</span></span>
18. <span data-ttu-id="b92a5-131">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="b92a5-131">Click Add.</span></span>

## <a name="map-new-data-model-elements-to-data-sources"></a><span data-ttu-id="b92a5-132">Varpa nýjum einingum gagnalíkans við gagnaveitur</span><span class="sxs-lookup"><span data-stu-id="b92a5-132">Map new data model elements to data sources</span></span>
1. <span data-ttu-id="b92a5-133">Smellt er á Varpa líkani á gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="b92a5-133">Click Map model to datasource.</span></span>
2. <span data-ttu-id="b92a5-134">Nota flýtiafmörkun á skilgreiningarreit með gildið 'InvoiceCustomer'.</span><span class="sxs-lookup"><span data-stu-id="b92a5-134">Use the Quick Filter to filter on the Definition field with a value of 'InvoiceCustomer'.</span></span>
    * <span data-ttu-id="b92a5-135">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="b92a5-135">InvoiceCustomer</span></span>  
    * <span data-ttu-id="b92a5-136">Við vörpum nýjum líkanaeiningum á viðkomandi gagnaveitur.</span><span class="sxs-lookup"><span data-stu-id="b92a5-136">We will map new model elements to appropriate data sources.</span></span>  
3. <span data-ttu-id="b92a5-137">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="b92a5-137">Click Designer.</span></span>
4. <span data-ttu-id="b92a5-138">Í trénu skal velja „viðhengi reiknings“.</span><span class="sxs-lookup"><span data-stu-id="b92a5-138">In the tree, select 'Invoice attachments'.</span></span>
5. <span data-ttu-id="b92a5-139">Í trénu skal víkka út "viðhengi reiknings".</span><span class="sxs-lookup"><span data-stu-id="b92a5-139">In the tree, expand 'Invoice attachments'.</span></span>
6. <span data-ttu-id="b92a5-140">Í trénu skal velja 'Invoice attachments\File name'.</span><span class="sxs-lookup"><span data-stu-id="b92a5-140">In the tree, select 'Invoice attachments\File name'.</span></span>
7. <span data-ttu-id="b92a5-141">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="b92a5-141">Click Edit.</span></span>
8. <span data-ttu-id="b92a5-142">Í svæði Formúla slá inn „CustInvoiceJour.„>Relations“.SalesTable.„<Relations“.„<Documents“.„originalFileName()““.</span><span class="sxs-lookup"><span data-stu-id="b92a5-142">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span></span>
    * <span data-ttu-id="b92a5-143">CustInvoiceJour.„>Relations“.SalesTable.„<Relations“.„<Documents“.„originalFileName()“</span><span class="sxs-lookup"><span data-stu-id="b92a5-143">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span></span>  
9. <span data-ttu-id="b92a5-144">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="b92a5-144">Click Save.</span></span>
10. <span data-ttu-id="b92a5-145">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b92a5-145">Close the page.</span></span>
11. <span data-ttu-id="b92a5-146">Í trénu skal velja 'Invoice attachments\File content'.</span><span class="sxs-lookup"><span data-stu-id="b92a5-146">In the tree, select 'Invoice attachments\File content'.</span></span>
12. <span data-ttu-id="b92a5-147">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="b92a5-147">Click Edit.</span></span>
13. <span data-ttu-id="b92a5-148">Í svæði Formúla slá inn „CustInvoiceJour.„>Relations“.SalesTable.„<Relations“.„<Documents“.„getFileContentAsContainer()““.</span><span class="sxs-lookup"><span data-stu-id="b92a5-148">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span></span>
    * <span data-ttu-id="b92a5-149">CustInvoiceJour.„>Relations“.SalesTable.„<Relations“.„<Documents“.„getFileContentAsContainer()“</span><span class="sxs-lookup"><span data-stu-id="b92a5-149">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span></span>  
14. <span data-ttu-id="b92a5-150">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="b92a5-150">Click Save.</span></span>
15. <span data-ttu-id="b92a5-151">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b92a5-151">Close the page.</span></span>
16. <span data-ttu-id="b92a5-152">Í trénu skal velja „viðhengi reiknings“.</span><span class="sxs-lookup"><span data-stu-id="b92a5-152">In the tree, select 'Invoice attachments'.</span></span>
17. <span data-ttu-id="b92a5-153">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="b92a5-153">Click Edit.</span></span>
18. <span data-ttu-id="b92a5-154">Í Formúlureitinn skal slá inn „CustInvoiceJour.“>Relations“.SalesTable.„<Relations“.„<Documents““.</span><span class="sxs-lookup"><span data-stu-id="b92a5-154">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span></span>
    * <span data-ttu-id="b92a5-155">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span><span class="sxs-lookup"><span data-stu-id="b92a5-155">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span></span>  
19. <span data-ttu-id="b92a5-156">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="b92a5-156">Click Save.</span></span>
20. <span data-ttu-id="b92a5-157">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b92a5-157">Close the page.</span></span>
21. <span data-ttu-id="b92a5-158">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="b92a5-158">Click Save.</span></span>
22. <span data-ttu-id="b92a5-159">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b92a5-159">Close the page.</span></span>
23. <span data-ttu-id="b92a5-160">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b92a5-160">Close the page.</span></span>
24. <span data-ttu-id="b92a5-161">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b92a5-161">Close the page.</span></span>
25. <span data-ttu-id="b92a5-162">Smellið á „Breyta stöðu“.</span><span class="sxs-lookup"><span data-stu-id="b92a5-162">Click Change status.</span></span>
26. <span data-ttu-id="b92a5-163">Smelltu á Ljúka.</span><span class="sxs-lookup"><span data-stu-id="b92a5-163">Click Complete.</span></span>
27. <span data-ttu-id="b92a5-164">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="b92a5-164">Click OK.</span></span>

