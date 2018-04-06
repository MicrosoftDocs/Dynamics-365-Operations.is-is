--- 
title: "Víkka gagnalíkan til að nota skjalastjórnunarskrár fyrir snið frálags í rafrænni skýrslugerð (ER)"
description: "Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt snið rafrænnar skýrslugerðar (ER) svo það noti skrár skjalastjórnunar (viðhengi) í rafrænar skýrslur."
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
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: ebbd442c9f69290dc995c05462ca70b554f7d9f2
ms.contentlocale: is-is
ms.lasthandoff: 03/26/2018

---
# <a name="extend-data-model-to-use-document-management-files-in-format-outputs-for-electronic-reporting-er"></a><span data-ttu-id="25c81-103">Víkka gagnalíkan til að nota skjalastjórnunarskrár fyrir snið frálags í rafrænni skýrslugerð (ER)</span><span class="sxs-lookup"><span data-stu-id="25c81-103">Extend data model to use Document Management files in format outputs for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="25c81-104">Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt snið rafrænnar skýrslugerðar (ER) svo það noti skrár skjalastjórnunar (viðhengi) í rafrænar skýrslur.</span><span class="sxs-lookup"><span data-stu-id="25c81-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="25c81-105">Hægt er að framkvæma þessum skrefum í Hvaða fyrirtæki sem er.</span><span class="sxs-lookup"><span data-stu-id="25c81-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="25c81-106">Til að ljúka þessum skrefum, verður fyrst að ljúka við skrefin í á “Rafræn skýrslugerð nota skrár skjalastjórnunar í sniðsúttökum (Hluti 1: undirbúa gagnalíkans” verkefnaleiðbeiningar.</span><span class="sxs-lookup"><span data-stu-id="25c81-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 1: Prepare data model)” task guide.</span></span>

<span data-ttu-id="25c81-107">Þetta ferli er fyrir eiginleika sem var bætt við í Dynamics 365 for Operations, útgáfu 1611.</span><span class="sxs-lookup"><span data-stu-id="25c81-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a><span data-ttu-id="25c81-108">Framlengja gagnalíkan til að birta skrár Skjalastjórnunar í því</span><span class="sxs-lookup"><span data-stu-id="25c81-108">Extend data model to present the Document Management files in it</span></span>
1. <span data-ttu-id="25c81-109">Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="25c81-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="25c81-110">Smelltu á Grunnstillingar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="25c81-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="25c81-111">Í trénu, veljið 'Customer invoice model'.</span><span class="sxs-lookup"><span data-stu-id="25c81-111">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="25c81-112">Í trénu, veljið 'Customer invoice model\Customer invoice model (custom)'.</span><span class="sxs-lookup"><span data-stu-id="25c81-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
5. <span data-ttu-id="25c81-113">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="25c81-113">Click Designer.</span></span>
6. <span data-ttu-id="25c81-114">Í trénu skal velja select 'Customer invoice(InvoiceCustomer)'.</span><span class="sxs-lookup"><span data-stu-id="25c81-114">In the tree, select 'Customer invoice(InvoiceCustomer)'.</span></span>
    * <span data-ttu-id="25c81-115">Við munum útvíkka þetta gagnalíkan til að birta það í öllum skrám sem hafa verið tengdar við sölupöntun sem er tengt við rafrænt unninn reikning.</span><span class="sxs-lookup"><span data-stu-id="25c81-115">We will extend this data model to expose in it any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
7. <span data-ttu-id="25c81-116">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="25c81-116">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="25c81-117">Í svæðið Heiti, færðu inn 'viðhengi reiknings'.</span><span class="sxs-lookup"><span data-stu-id="25c81-117">In the Name field, type 'Invoice attachments'.</span></span>
    * <span data-ttu-id="25c81-118">Viðhengi reiknings</span><span class="sxs-lookup"><span data-stu-id="25c81-118">Invoice attachments</span></span>  
9. <span data-ttu-id="25c81-119">Veljið í svæðinu gerð Vöru „Skrárlisti".</span><span class="sxs-lookup"><span data-stu-id="25c81-119">In the Item type field, select 'Record list'.</span></span>
10. <span data-ttu-id="25c81-120">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="25c81-120">Click Add.</span></span>
11. <span data-ttu-id="25c81-121">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="25c81-121">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="25c81-122">Í svæðið Heiti, færðu inn 'innihald skráa'.</span><span class="sxs-lookup"><span data-stu-id="25c81-122">In the Name field, type 'File content'.</span></span>
    * <span data-ttu-id="25c81-123">Innihald skráar</span><span class="sxs-lookup"><span data-stu-id="25c81-123">File content</span></span>  
13. <span data-ttu-id="25c81-124">Velja 'geymir' í svæðinu gerð Vöru.</span><span class="sxs-lookup"><span data-stu-id="25c81-124">In the Item type field, select 'Container'.</span></span>
14. <span data-ttu-id="25c81-125">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="25c81-125">Click Add.</span></span>
15. <span data-ttu-id="25c81-126">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="25c81-126">Click New to open the drop dialog.</span></span>
16. <span data-ttu-id="25c81-127">Í svæðið Heiti, færðu inn 'skrárnafn'.</span><span class="sxs-lookup"><span data-stu-id="25c81-127">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="25c81-128">Skrárnafn</span><span class="sxs-lookup"><span data-stu-id="25c81-128">File name</span></span>  
17. <span data-ttu-id="25c81-129">Veljið 'Strengur' í svæðinu Vöru.</span><span class="sxs-lookup"><span data-stu-id="25c81-129">In the Item type field, select 'String'.</span></span>
18. <span data-ttu-id="25c81-130">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="25c81-130">Click Add.</span></span>

## <a name="map-new-data-model-elements-to-dynamics-365-for-finance-and-operations-data-sources"></a><span data-ttu-id="25c81-131">Varpa nýjum einingum gagnalíkans á gagnaveitur Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="25c81-131">Map new data model elements to Dynamics 365 for Finance and Operations data sources</span></span>
1. <span data-ttu-id="25c81-132">Smellt er á Varpa líkani á gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="25c81-132">Click Map model to datasource.</span></span>
2. <span data-ttu-id="25c81-133">Nota flýtiafmörkun á skilgreiningarreit með gildið 'InvoiceCustomer'.</span><span class="sxs-lookup"><span data-stu-id="25c81-133">Use the Quick Filter to filter on the Definition field with a value of 'InvoiceCustomer'.</span></span>
    * <span data-ttu-id="25c81-134">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="25c81-134">InvoiceCustomer</span></span>  
    * <span data-ttu-id="25c81-135">Við vörpum nýjum líkanaeiningum á viðkomandi gagnaveitur.</span><span class="sxs-lookup"><span data-stu-id="25c81-135">We will map new model elements to appropriate data sources.</span></span>  
3. <span data-ttu-id="25c81-136">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="25c81-136">Click Designer.</span></span>
4. <span data-ttu-id="25c81-137">Í trénu skal velja „viðhengi reiknings“.</span><span class="sxs-lookup"><span data-stu-id="25c81-137">In the tree, select 'Invoice attachments'.</span></span>
5. <span data-ttu-id="25c81-138">Í trénu skal víkka út "viðhengi reiknings".</span><span class="sxs-lookup"><span data-stu-id="25c81-138">In the tree, expand 'Invoice attachments'.</span></span>
6. <span data-ttu-id="25c81-139">Í trénu skal velja 'Invoice attachments\File name'.</span><span class="sxs-lookup"><span data-stu-id="25c81-139">In the tree, select 'Invoice attachments\File name'.</span></span>
7. <span data-ttu-id="25c81-140">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="25c81-140">Click Edit.</span></span>
8. <span data-ttu-id="25c81-141">Í svæði Formúla slá inn „CustInvoiceJour.„>Relations“.SalesTable.„<Relations“.„<Documents“.„originalFileName()““.</span><span class="sxs-lookup"><span data-stu-id="25c81-141">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span></span>
    * <span data-ttu-id="25c81-142">CustInvoiceJour.„>Relations“.SalesTable.„<Relations“.„<Documents“.„originalFileName()“</span><span class="sxs-lookup"><span data-stu-id="25c81-142">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span></span>  
9. <span data-ttu-id="25c81-143">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="25c81-143">Click Save.</span></span>
10. <span data-ttu-id="25c81-144">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="25c81-144">Close the page.</span></span>
11. <span data-ttu-id="25c81-145">Í trénu skal velja 'Invoice attachments\File content'.</span><span class="sxs-lookup"><span data-stu-id="25c81-145">In the tree, select 'Invoice attachments\File content'.</span></span>
12. <span data-ttu-id="25c81-146">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="25c81-146">Click Edit.</span></span>
13. <span data-ttu-id="25c81-147">Í svæði Formúla slá inn „CustInvoiceJour.„>Relations“.SalesTable.„<Relations“.„<Documents“.„getFileContentAsContainer()““.</span><span class="sxs-lookup"><span data-stu-id="25c81-147">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span></span>
    * <span data-ttu-id="25c81-148">CustInvoiceJour.„>Relations“.SalesTable.„<Relations“.„<Documents“.„getFileContentAsContainer()“</span><span class="sxs-lookup"><span data-stu-id="25c81-148">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span></span>  
14. <span data-ttu-id="25c81-149">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="25c81-149">Click Save.</span></span>
15. <span data-ttu-id="25c81-150">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="25c81-150">Close the page.</span></span>
16. <span data-ttu-id="25c81-151">Í trénu skal velja „viðhengi reiknings“.</span><span class="sxs-lookup"><span data-stu-id="25c81-151">In the tree, select 'Invoice attachments'.</span></span>
17. <span data-ttu-id="25c81-152">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="25c81-152">Click Edit.</span></span>
18. <span data-ttu-id="25c81-153">Í Formúlureitinn skal slá inn „CustInvoiceJour.“>Relations“.SalesTable.„<Relations“.„<Documents““.</span><span class="sxs-lookup"><span data-stu-id="25c81-153">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span></span>
    * <span data-ttu-id="25c81-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span><span class="sxs-lookup"><span data-stu-id="25c81-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span></span>  
19. <span data-ttu-id="25c81-155">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="25c81-155">Click Save.</span></span>
20. <span data-ttu-id="25c81-156">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="25c81-156">Close the page.</span></span>
21. <span data-ttu-id="25c81-157">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="25c81-157">Click Save.</span></span>
22. <span data-ttu-id="25c81-158">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="25c81-158">Close the page.</span></span>
23. <span data-ttu-id="25c81-159">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="25c81-159">Close the page.</span></span>
24. <span data-ttu-id="25c81-160">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="25c81-160">Close the page.</span></span>
25. <span data-ttu-id="25c81-161">Smellið á „Breyta stöðu“.</span><span class="sxs-lookup"><span data-stu-id="25c81-161">Click Change status.</span></span>
26. <span data-ttu-id="25c81-162">Smelltu á Ljúka.</span><span class="sxs-lookup"><span data-stu-id="25c81-162">Click Complete.</span></span>
27. <span data-ttu-id="25c81-163">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="25c81-163">Click OK.</span></span>


