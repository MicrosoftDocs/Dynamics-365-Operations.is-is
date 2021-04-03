---
title: Stofna lánshluti
description: Lánshlutir eru færslur sem aðstoða við að rekja efnislegu vörurnar, eins og símar eða tölvur sem fyrirtækið lánar til starfsmanna.
author: andreabichsel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmLoanType, DefaultDashboard, HcmLoanItem, HcmWorkerLookUp, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5b93f68790a72af28130d80ed189538f9c5c87ab
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467104"
---
# <a name="create-loan-items"></a><span data-ttu-id="fd436-103">Stofna lánshluti</span><span class="sxs-lookup"><span data-stu-id="fd436-103">Create loan items</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



<span data-ttu-id="fd436-104">Lánshlutir eru færslur sem aðstoða við að rekja efnislegu vörurnar, eins og símar eða tölvur sem fyrirtækið lánar til starfsmanna.</span><span class="sxs-lookup"><span data-stu-id="fd436-104">Loan items are records that help you track physical items, such as phones or computers, that your company lends to workers.</span></span> <span data-ttu-id="fd436-105">Hver efnislegt vara verður að hafa samsvarandi lánshlut.</span><span class="sxs-lookup"><span data-stu-id="fd436-105">Each physical item must have a corresponding loan item.</span></span> <span data-ttu-id="fd436-106">Hvert skrá lánshluts ætti að lýsa hvað er verið að lána, hver er ábyrgur fyrir láni og fjölda daga sem hlutur getur verið í láni.</span><span class="sxs-lookup"><span data-stu-id="fd436-106">Each loan item record should describe what is being loaned, who is responsible for the loan, and the number of days the item can be on loan.</span></span> <span data-ttu-id="fd436-107">Hægt er að stofna marga lánshluti, eins og lykla, aðgangskort eða einkennisbúninga, á sama tíma.</span><span class="sxs-lookup"><span data-stu-id="fd436-107">You can create multiple loan items, such as keys, access cards, or uniforms, at the same time.</span></span> <span data-ttu-id="fd436-108">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="fd436-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-loan-types"></a><span data-ttu-id="fd436-109">Stofna gerðir Lána</span><span class="sxs-lookup"><span data-stu-id="fd436-109">Create Loan types</span></span>
1. <span data-ttu-id="fd436-110">Farið í Mannauður > Starfsfólk > Lánshlutir > Gerðir lánshluta.</span><span class="sxs-lookup"><span data-stu-id="fd436-110">Go to Human resources > Workers > Loan items > Loan types.</span></span>
2. <span data-ttu-id="fd436-111">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="fd436-111">Click New.</span></span>
3. <span data-ttu-id="fd436-112">Í reitinn Gerð láns skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="fd436-112">In the Loan type field, type a value.</span></span>
4. <span data-ttu-id="fd436-113">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="fd436-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="fd436-114">Færið inn fjölda daga sem hlutir sem úthlutað er á þessa lánsgerð geta verið komið fram yfir á tíma.</span><span class="sxs-lookup"><span data-stu-id="fd436-114">Enter the number of days that items assigned to this loan type can be overdue.</span></span> 
6. <span data-ttu-id="fd436-115">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="fd436-115">Click Save.</span></span>
7. <span data-ttu-id="fd436-116">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="fd436-116">Close the page.</span></span>
8. <span data-ttu-id="fd436-117">Endurhlaðið síðuna.</span><span class="sxs-lookup"><span data-stu-id="fd436-117">Refresh the page.</span></span>

## <a name="create-loan-items"></a><span data-ttu-id="fd436-118">Stofna lánshluti</span><span class="sxs-lookup"><span data-stu-id="fd436-118">Create Loan items</span></span>
1. <span data-ttu-id="fd436-119">Farið í Mannauður > Starfsfólk > Lánshlutir > Lánshlutir.</span><span class="sxs-lookup"><span data-stu-id="fd436-119">Go to Human resources > Workers > Loan items > Loan items.</span></span>
2. <span data-ttu-id="fd436-120">Smellt er á stofna Lánshlutur</span><span class="sxs-lookup"><span data-stu-id="fd436-120">Click Create loan items.</span></span>
3. <span data-ttu-id="fd436-121">Í magn. færðu inn númer</span><span class="sxs-lookup"><span data-stu-id="fd436-121">In the Qty. field, enter a number.</span></span>
4. <span data-ttu-id="fd436-122">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="fd436-122">In the Description field, type a value.</span></span>
5. <span data-ttu-id="fd436-123">Í reitnum Gerð láns skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="fd436-123">In the Loan type field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="fd436-124">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="fd436-124">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="fd436-125">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="fd436-125">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="fd436-126">Færa inn fjölda daga sem hlutur getur verið í láni.</span><span class="sxs-lookup"><span data-stu-id="fd436-126">Enter the number of days the item can be on loan.</span></span>
    * <span data-ttu-id="fd436-127">Sjálfgefna gildið fyrir Áætlað skila svæði á síðunni Lánsbúnaður er reiknaður sem núgildandi dagsetning plús þessi tala.</span><span class="sxs-lookup"><span data-stu-id="fd436-127">The default value for the Planned return field on the Loaned equipment page is calculated as the current date plus this number.</span></span>  
9. <span data-ttu-id="fd436-128">Í reitnum Einstaklingur við stjórn skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="fd436-128">In the Person in charge field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="fd436-129">Smellið á Velja.</span><span class="sxs-lookup"><span data-stu-id="fd436-129">Click Select.</span></span>
11. <span data-ttu-id="fd436-130">Í reitinn upphafsgildi skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="fd436-130">In the Starting value field, enter a number.</span></span>
12. <span data-ttu-id="fd436-131">Í reitinn tímabil skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="fd436-131">In the Interval field, enter a number.</span></span>
13. <span data-ttu-id="fd436-132">Í reitinn snið skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="fd436-132">In the Format field, type a value.</span></span>
    * <span data-ttu-id="fd436-133">Til dæmis ef hæsta upphafsnúmer fyrir lánaða vöru er 10 þarf að færa inn tvö númeratákn í reitinn snið.</span><span class="sxs-lookup"><span data-stu-id="fd436-133">For example, if the starting number for a loan item is 10, enter two number symbols symbols in the Format field.</span></span>  
14. <span data-ttu-id="fd436-134">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="fd436-134">Click OK.</span></span>
15. <span data-ttu-id="fd436-135">Endurhlaðið síðuna.</span><span class="sxs-lookup"><span data-stu-id="fd436-135">Refresh the page.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]