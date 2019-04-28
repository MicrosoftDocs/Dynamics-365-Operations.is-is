---
title: Stjórna atriðum sem eru lánaðar til starfskrafta
description: Lánshlutir eru færslur sem aðstoða stjórnendur við að rekja efnislegu vörurnar sem fyrirtækið lánar til starfsmanna.
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmLoanItem, HcmLoanType, HcmPersonLoan
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 3581
ms.assetid: b14bdddb-f10e-4619-9f91-8c88439da862
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: 5942016374eb2c681e65b2d6151824924f290dc2
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/19/2019
ms.locfileid: "859023"
---
# <a name="manage-items-that-are-lent-to-workers"></a><span data-ttu-id="0976f-103">Stjórna atriðum sem eru lánaðar til starfskrafta</span><span class="sxs-lookup"><span data-stu-id="0976f-103">Manage items that are lent to workers</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0976f-104">Lánshlutir eru færslur sem aðstoða stjórnendur við að rekja efnislegu vörurnar sem fyrirtækið lánar til starfsmanna.</span><span class="sxs-lookup"><span data-stu-id="0976f-104">Loan items are records that help managers track the physical items that your company lends to its workers.</span></span> 

<span data-ttu-id="0976f-105">Eftirfarandi atriði eru dæmi um vörur sem fyrirtæki gæti verið að lána starfsmönnum:</span><span class="sxs-lookup"><span data-stu-id="0976f-105">The following points list examples of items that a company might lend to workers:</span></span>
-   <span data-ttu-id="0976f-106">Farsímar</span><span class="sxs-lookup"><span data-stu-id="0976f-106">Mobile telephones</span></span>
-   <span data-ttu-id="0976f-107">Bifreiðar</span><span class="sxs-lookup"><span data-stu-id="0976f-107">Automobiles</span></span>
-   <span data-ttu-id="0976f-108">Tölvubúnaður</span><span class="sxs-lookup"><span data-stu-id="0976f-108">Computer equipment</span></span>

<span data-ttu-id="0976f-109">Hver efnislegt vara verður að hafa samsvarandi lánshlut.</span><span class="sxs-lookup"><span data-stu-id="0976f-109">Each physical item must have a corresponding loan item.</span></span> <span data-ttu-id="0976f-110">Hvert skrá yfir lánshluts ætti að lýsa hvað er verið að lána, hver er ábyrgur fyrir láni og fjölda daga sem hlutur getur°verið í láni hjá starfsmanni.</span><span class="sxs-lookup"><span data-stu-id="0976f-110">Each loan item record should describe what is being loaned, who is responsible for the loan, and the number of days the item can loaned to a worker.</span></span> <span data-ttu-id="0976f-111">Hægt er að stofna marga lánshluti, eins og lykla, aðgangskort eða einkennisbúninga, á sama tíma.</span><span class="sxs-lookup"><span data-stu-id="0976f-111">You can create multiple loan items, for items such as keys, access cards or uniforms, at the same time.</span></span> 

<span data-ttu-id="0976f-112">Þegar hlutur er lánaður, skráið útlánsdagsetningu ásamt áætluðum skiladegi.</span><span class="sxs-lookup"><span data-stu-id="0976f-112">When loaning an item, enter the date that the item was loaned, and the planned return date.</span></span> <span data-ttu-id="0976f-113">Þegar hlut er skilað skal skrá raunverulegan skiladag.</span><span class="sxs-lookup"><span data-stu-id="0976f-113">When the item is returned, enter the actual return date.</span></span>

<span data-ttu-id="0976f-114">Starfsmenn geta skoðað°færslur fyrir vörur sem þeir hafa fengið lánaðar með°sjálfsafgreiðsla vinnusvæði starfsmanna.</span><span class="sxs-lookup"><span data-stu-id="0976f-114">Employees can view the records of the items that have been loaned to them using the Employee self-service workspace.</span></span> <span data-ttu-id="0976f-115">Þeir geta einnig breytt fyrirliggjandi færslum°eða fært inn°nýja lánshluti°ef þeir hafa fengið efnislegar viðbótarvörur.</span><span class="sxs-lookup"><span data-stu-id="0976f-115">They can also edit the existing records or enter new loan items, if they've received additional physical items.</span></span>  <span data-ttu-id="0976f-116">Hægt er að setja upp verkflæði til að rekja breytingar á nýjum eða fyrirliggjandi lánshlutum gegnum samþykktarferli.</span><span class="sxs-lookup"><span data-stu-id="0976f-116">Workflow can be set up to route changes to new or existing loan items through an approval process.</span></span> 

<span data-ttu-id="0976f-117">Stjórnendur geta skoðað°lánshluti fyrir beinar skýrslur þeirra.</span><span class="sxs-lookup"><span data-stu-id="0976f-117">Managers can view loaned items for their direct reports.</span></span> <span data-ttu-id="0976f-118">Þeir geta einnig fengið heimild til að bæta við nýjum lánshlutum fyrir hönd starfsmanna sinna.</span><span class="sxs-lookup"><span data-stu-id="0976f-118">They can also be granted permission to add new loan items on behalf of their employees.</span></span>

 <a name="account-for-lost-or-misplaced-loan-items"></a><span data-ttu-id="0976f-119">Lykill fyrir týnda eða tapaða lánshluti</span><span class="sxs-lookup"><span data-stu-id="0976f-119">Account for lost or misplaced loan items</span></span>
-----------------------------------------

<span data-ttu-id="0976f-120">Eyðileggist hlutur eða hann týnist skal skrá gerviskil.</span><span class="sxs-lookup"><span data-stu-id="0976f-120">If an item becomes damaged or misplaced, enter a fictitious return record.</span></span> <span data-ttu-id="0976f-121">Þá er hægt að eyða hlutnum úr skrá eða gefa það til kynna í lýsingu að hann sé týndur.</span><span class="sxs-lookup"><span data-stu-id="0976f-121">Then either delete the item or keep it in the overview and change the description to indicate that the item is not available.</span></span>


<a name="additional-resources"></a><span data-ttu-id="0976f-122">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="0976f-122">Additional resources</span></span>
--------

[<span data-ttu-id="0976f-123">Mannauður</span><span class="sxs-lookup"><span data-stu-id="0976f-123">Human resources</span></span>](index.md)



