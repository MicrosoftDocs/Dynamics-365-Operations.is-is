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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 1a5325dc3a97b9e205b41fe8dae18f43e430daeb
ms.contentlocale: is-is
ms.lasthandoff: 08/29/2017

---
# <a name="extend-data-model-to-use-document-management-files-in-format-outputs-for-electronic-reporting-er"></a><span data-ttu-id="01b37-103">Víkka gagnalíkan til að nota skjalastjórnunarskrár fyrir snið frálags í rafrænni skýrslugerð (ER)</span><span class="sxs-lookup"><span data-stu-id="01b37-103">Extend data model to use Document Management files in format outputs for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="01b37-104">Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt snið rafrænnar skýrslugerðar (ER) svo það noti skrár skjalastjórnunar (viðhengi) í rafrænar skýrslur.</span><span class="sxs-lookup"><span data-stu-id="01b37-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="01b37-105">Hægt er að framkvæma þessum skrefum í Hvaða fyrirtæki sem er.</span><span class="sxs-lookup"><span data-stu-id="01b37-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="01b37-106">Til að ljúka þessum skrefum, verður fyrst að ljúka við skrefin í á “Rafræn skýrslugerð nota skrár skjalastjórnunar í sniðsúttökum (Hluti 1: undirbúa gagnalíkans” verkefnaleiðbeiningar.</span><span class="sxs-lookup"><span data-stu-id="01b37-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 1: Prepare data model)” task guide.</span></span>

<span data-ttu-id="01b37-107">Þetta ferli er fyrir eiginleika sem var bætt við í Dynamics 365 for Operations, útgáfu 1611.</span><span class="sxs-lookup"><span data-stu-id="01b37-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a><span data-ttu-id="01b37-108">Framlengja gagnalíkan til að birta skrár Skjalastjórnunar í því</span><span class="sxs-lookup"><span data-stu-id="01b37-108">Extend data model to present the Document Management files in it</span></span>
1. <span data-ttu-id="01b37-109">Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="01b37-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="01b37-110">Smelltu á Grunnstillingar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="01b37-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="01b37-111">Í trénu, veljið 'Customer invoice model'.</span><span class="sxs-lookup"><span data-stu-id="01b37-111">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="01b37-112">Í trénu, veljið 'Customer invoice model\Customer invoice model (custom)'.</span><span class="sxs-lookup"><span data-stu-id="01b37-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
5. <span data-ttu-id="01b37-113">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="01b37-113">Click Designer.</span></span>
6. <span data-ttu-id="01b37-114">Í trénu skal velja select 'Customer invoice(InvoiceCustomer)'.</span><span class="sxs-lookup"><span data-stu-id="01b37-114">In the tree, select 'Customer invoice(InvoiceCustomer)'.</span></span>
    * <span data-ttu-id="01b37-115">Við munum útvíkka þetta gagnalíkan til að birta það í öllum skrám sem hafa verið tengdar við sölupöntun sem er tengt við rafrænt unninn reikning.</span><span class="sxs-lookup"><span data-stu-id="01b37-115">We will extend this data model to expose in it any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
7. <span data-ttu-id="01b37-116">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="01b37-116">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="01b37-117">Í svæðið Heiti, færðu inn 'viðhengi reiknings'.</span><span class="sxs-lookup"><span data-stu-id="01b37-117">In the Name field, type 'Invoice attachments'.</span></span>
    * <span data-ttu-id="01b37-118">Viðhengi reiknings</span><span class="sxs-lookup"><span data-stu-id="01b37-118">Invoice attachments</span></span>  
9. <span data-ttu-id="01b37-119">Veljið í svæðinu gerð Vöru „Skrárlisti".</span><span class="sxs-lookup"><span data-stu-id="01b37-119">In the Item type field, select 'Record list'.</span></span>
10. <span data-ttu-id="01b37-120">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="01b37-120">Click Add.</span></span>
11. <span data-ttu-id="01b37-121">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="01b37-121">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="01b37-122">Í svæðið Heiti, færðu inn 'innihald skráa'.</span><span class="sxs-lookup"><span data-stu-id="01b37-122">In the Name field, type 'File content'.</span></span>
    * <span data-ttu-id="01b37-123">Innihald skráar</span><span class="sxs-lookup"><span data-stu-id="01b37-123">File content</span></span>  
13. <span data-ttu-id="01b37-124">Velja 'geymir' í svæðinu gerð Vöru.</span><span class="sxs-lookup"><span data-stu-id="01b37-124">In the Item type field, select 'Container'.</span></span>
14. <span data-ttu-id="01b37-125">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="01b37-125">Click Add.</span></span>
15. <span data-ttu-id="01b37-126">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="01b37-126">Click New to open the drop dialog.</span></span>
16. <span data-ttu-id="01b37-127">Í svæðið Heiti, færðu inn 'skrárnafn'.</span><span class="sxs-lookup"><span data-stu-id="01b37-127">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="01b37-128">Skrárnafn</span><span class="sxs-lookup"><span data-stu-id="01b37-128">File name</span></span>  
17. <span data-ttu-id="01b37-129">Veljið 'Strengur' í svæðinu Vöru.</span><span class="sxs-lookup"><span data-stu-id="01b37-129">In the Item type field, select 'String'.</span></span>
18. <span data-ttu-id="01b37-130">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="01b37-130">Click Add.</span></span>

## <a name="map-new-data-model-elements-to-dynamics-365-for-finance-and-operations-enterprise-edition-data-sources"></a><span data-ttu-id="01b37-131">Varpa nýjum einingum gagnalíkans til Dynamics 365 for Finance and Operations, Enterprise edition gagnaveitur.</span><span class="sxs-lookup"><span data-stu-id="01b37-131">Map new data model elements to Dynamics 365 for Finance and Operations, Enterprise edition data sources</span></span>
1. <span data-ttu-id="01b37-132">Smellt er á Varpa líkani á gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="01b37-132">Click Map model to datasource.</span></span>
2. <span data-ttu-id="01b37-133">Nota flýtiafmörkun á skilgreiningarreit með gildið 'InvoiceCustomer'.</span><span class="sxs-lookup"><span data-stu-id="01b37-133">Use the Quick Filter to filter on the Definition field with a value of 'InvoiceCustomer'.</span></span>
    * <span data-ttu-id="01b37-134">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="01b37-134">InvoiceCustomer</span></span>  
    * <span data-ttu-id="01b37-135">Við vörpum nýjum líkanaeiningum á viðkomandi gagnaveitur.</span><span class="sxs-lookup"><span data-stu-id="01b37-135">We will map new model elements to appropriate data sources.</span></span>  
3. <span data-ttu-id="01b37-136">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="01b37-136">Click Designer.</span></span>
4. <span data-ttu-id="01b37-137">Í trénu skal velja „viðhengi reiknings“.</span><span class="sxs-lookup"><span data-stu-id="01b37-137">In the tree, select 'Invoice attachments'.</span></span>
5. <span data-ttu-id="01b37-138">Í trénu skal víkka út "viðhengi reiknings".</span><span class="sxs-lookup"><span data-stu-id="01b37-138">In the tree, expand 'Invoice attachments'.</span></span>
6. <span data-ttu-id="01b37-139">Í trénu skal velja 'Invoice attachments\File name'.</span><span class="sxs-lookup"><span data-stu-id="01b37-139">In the tree, select 'Invoice attachments\File name'.</span></span>
7. <span data-ttu-id="01b37-140">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="01b37-140">Click Edit.</span></span>
8. <span data-ttu-id="01b37-141">Í svæði Formúla slá inn „CustInvoiceJour.„>Relations“.SalesTable.„<Relations“.„<Documents“.„originalFileName()““.</span><span class="sxs-lookup"><span data-stu-id="01b37-141">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span></span>
    * <span data-ttu-id="01b37-142">CustInvoiceJour.„>Relations“.SalesTable.„<Relations“.„<Documents“.„originalFileName()“</span><span class="sxs-lookup"><span data-stu-id="01b37-142">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span></span>  
9. <span data-ttu-id="01b37-143">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="01b37-143">Click Save.</span></span>
10. <span data-ttu-id="01b37-144">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="01b37-144">Close the page.</span></span>
11. <span data-ttu-id="01b37-145">Í trénu skal velja 'Invoice attachments\File content'.</span><span class="sxs-lookup"><span data-stu-id="01b37-145">In the tree, select 'Invoice attachments\File content'.</span></span>
12. <span data-ttu-id="01b37-146">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="01b37-146">Click Edit.</span></span>
13. <span data-ttu-id="01b37-147">Í svæði Formúla slá inn „CustInvoiceJour.„>Relations“.SalesTable.„<Relations“.„<Documents“.„getFileContentAsContainer()““.</span><span class="sxs-lookup"><span data-stu-id="01b37-147">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span></span>
    * <span data-ttu-id="01b37-148">CustInvoiceJour.„>Relations“.SalesTable.„<Relations“.„<Documents“.„getFileContentAsContainer()“</span><span class="sxs-lookup"><span data-stu-id="01b37-148">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span></span>  
14. <span data-ttu-id="01b37-149">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="01b37-149">Click Save.</span></span>
15. <span data-ttu-id="01b37-150">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="01b37-150">Close the page.</span></span>
16. <span data-ttu-id="01b37-151">Í trénu skal velja „viðhengi reiknings“.</span><span class="sxs-lookup"><span data-stu-id="01b37-151">In the tree, select 'Invoice attachments'.</span></span>
17. <span data-ttu-id="01b37-152">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="01b37-152">Click Edit.</span></span>
18. <span data-ttu-id="01b37-153">Í Formúlureitinn skal slá inn „CustInvoiceJour.“>Relations“.SalesTable.„<Relations“.„<Documents““.</span><span class="sxs-lookup"><span data-stu-id="01b37-153">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span></span>
    * <span data-ttu-id="01b37-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span><span class="sxs-lookup"><span data-stu-id="01b37-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span></span>  
19. <span data-ttu-id="01b37-155">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="01b37-155">Click Save.</span></span>
20. <span data-ttu-id="01b37-156">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="01b37-156">Close the page.</span></span>
21. <span data-ttu-id="01b37-157">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="01b37-157">Click Save.</span></span>
22. <span data-ttu-id="01b37-158">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="01b37-158">Close the page.</span></span>
23. <span data-ttu-id="01b37-159">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="01b37-159">Close the page.</span></span>
24. <span data-ttu-id="01b37-160">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="01b37-160">Close the page.</span></span>
25. <span data-ttu-id="01b37-161">Smellið á „Breyta stöðu“.</span><span class="sxs-lookup"><span data-stu-id="01b37-161">Click Change status.</span></span>
26. <span data-ttu-id="01b37-162">Smelltu á Ljúka.</span><span class="sxs-lookup"><span data-stu-id="01b37-162">Click Complete.</span></span>
27. <span data-ttu-id="01b37-163">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="01b37-163">Click OK.</span></span>


