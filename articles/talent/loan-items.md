---
title: "Stjórna vörum sem eru lánaðar til starfsmanna"
description: "Lánshlutir eru færslur sem aðstoða stjórnendur við að rekja efnislegu vörurnar sem fyrirtækið lánar til starfsmanna."
author: kherr75
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmLoanItem, HcmLoanType, HcmPersonLoan
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 3581
ms.assetid: b14bdddb-f10e-4619-9f91-8c88439da862
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 17fb54c07f817b6f4a65c01cd0277c8d677e2e78
ms.contentlocale: is-is
ms.lasthandoff: 08/29/2017

---

# <a name="manage-items-lent-to-workers"></a><span data-ttu-id="a0681-103">Stjórna vörum sem eru lánaðar til starfsmanna</span><span class="sxs-lookup"><span data-stu-id="a0681-103">Manage items lent to workers</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="a0681-104">Lánshlutir eru færslur sem aðstoða stjórnendur við að rekja efnislegu vörurnar sem fyrirtækið lánar til starfsmanna.</span><span class="sxs-lookup"><span data-stu-id="a0681-104">Loan items are records that help managers track the physical items that your company lends to its workers.</span></span> 

<span data-ttu-id="a0681-105">Eftirfarandi atriði eru dæmi um vörur sem fyrirtæki gæti verið að lána starfsmönnum:</span><span class="sxs-lookup"><span data-stu-id="a0681-105">The following points list examples of items that a company might lend to workers:</span></span>
-   <span data-ttu-id="a0681-106">Farsímar</span><span class="sxs-lookup"><span data-stu-id="a0681-106">Mobile telephones</span></span>
-   <span data-ttu-id="a0681-107">Bifreiðar</span><span class="sxs-lookup"><span data-stu-id="a0681-107">Automobiles</span></span>
-   <span data-ttu-id="a0681-108">Tölvubúnaður</span><span class="sxs-lookup"><span data-stu-id="a0681-108">Computer equipment</span></span>

<span data-ttu-id="a0681-109">Hver efnislegt vara verður að hafa samsvarandi lánshlut.</span><span class="sxs-lookup"><span data-stu-id="a0681-109">Each physical item must have a corresponding loan item.</span></span> <span data-ttu-id="a0681-110">Hvert skrá yfir lánshluts ætti að lýsa hvað er verið að lána, hver er ábyrgur fyrir láni og fjölda daga sem hlutur getur°verið í láni hjá starfsmanni.</span><span class="sxs-lookup"><span data-stu-id="a0681-110">Each loan item record should describe what is being loaned, who is responsible for the loan, and the number of days the item can loaned to a worker.</span></span> <span data-ttu-id="a0681-111">Hægt er að stofna marga lánshluti, eins og lykla, aðgangskort eða einkennisbúninga, á sama tíma.</span><span class="sxs-lookup"><span data-stu-id="a0681-111">You can create multiple loan items, for items such as keys, access cards or uniforms, at the same time.</span></span> 

<span data-ttu-id="a0681-112">Þegar hlutur er lánaður, skráið útlánsdagsetningu ásamt áætluðum skiladegi.</span><span class="sxs-lookup"><span data-stu-id="a0681-112">When loaning an item, enter the date that the item was loaned, and the planned return date.</span></span> <span data-ttu-id="a0681-113">Þegar hlut er skilað skal skrá raunverulegan skiladag.</span><span class="sxs-lookup"><span data-stu-id="a0681-113">When the item is returned, enter the actual return date.</span></span>

<span data-ttu-id="a0681-114">Starfsmenn geta skoðað°færslur fyrir vörur sem þeir hafa fengið lánaðar með°sjálfsafgreiðsla vinnusvæði starfsmanna.</span><span class="sxs-lookup"><span data-stu-id="a0681-114">Employees can view the records of the items that have been loaned to them using the Employee self-service workspace.</span></span> <span data-ttu-id="a0681-115">Þeir geta einnig breytt fyrirliggjandi færslum°eða fært inn°nýja lánshluti°ef þeir hafa fengið efnislegar viðbótarvörur.</span><span class="sxs-lookup"><span data-stu-id="a0681-115">They can also edit the existing records or enter new loan items, if they've received additional physical items.</span></span>  <span data-ttu-id="a0681-116">Hægt er að setja upp verkflæði til að rekja breytingar á nýjum eða fyrirliggjandi lánshlutum gegnum samþykktarferli.</span><span class="sxs-lookup"><span data-stu-id="a0681-116">Workflow can be set up to route changes to new or existing loan items through an approval process.</span></span> 

<span data-ttu-id="a0681-117">Stjórnendur geta skoðað°lánshluti fyrir beinar skýrslur þeirra.</span><span class="sxs-lookup"><span data-stu-id="a0681-117">Managers can view loaned items for their direct reports.</span></span> <span data-ttu-id="a0681-118">Þeir geta einnig fengið heimild til að bæta við nýjum lánshlutum fyrir hönd starfsmanna sinna.</span><span class="sxs-lookup"><span data-stu-id="a0681-118">They can also be granted permission to add new loan items on behalf of their employees.</span></span>

 <a name="account-for-lost-or-misplaced-loan-items"></a><span data-ttu-id="a0681-119">Lykill fyrir týnda eða tapaða lánshluti</span><span class="sxs-lookup"><span data-stu-id="a0681-119">Account for lost or misplaced loan items</span></span>
-----------------------------------------

<span data-ttu-id="a0681-120">Eyðileggist hlutur eða hann týnist skal skrá gerviskil.</span><span class="sxs-lookup"><span data-stu-id="a0681-120">If an item becomes damaged or misplaced, enter a fictitious return record.</span></span> <span data-ttu-id="a0681-121">Þá er hægt að eyða hlutnum úr skrá eða gefa það til kynna í lýsingu að hann sé týndur.</span><span class="sxs-lookup"><span data-stu-id="a0681-121">Then either delete the item or keep it in the overview and change the description to indicate that the item is not available.</span></span>

 
<a name="see-also"></a><span data-ttu-id="a0681-122">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="a0681-122">See also</span></span>
--------

[<span data-ttu-id="a0681-123">Mannauður</span><span class="sxs-lookup"><span data-stu-id="a0681-123">Human resources</span></span>](index.md)




