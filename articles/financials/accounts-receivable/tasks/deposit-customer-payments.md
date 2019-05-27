---
title: Leggja inn greiðslur viðskiptavina
description: Innborgun á greiðslum viðskiptavina.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransCustPaym, CustTableLookup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f58cebce20e8516dc918e0bad1e020ffd7f791ee
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565486"
---
# <a name="deposit-customer-payments"></a><span data-ttu-id="acaa0-103">Leggja inn greiðslur viðskiptavina</span><span class="sxs-lookup"><span data-stu-id="acaa0-103">Deposit customer payments</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="acaa0-104">Innborgun á greiðslum viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="acaa0-104">Deposit customer payments.</span></span> <span data-ttu-id="acaa0-105">Þetta verkefni notar USMF-sýnifyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="acaa0-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="acaa0-106">Fara í Viðskiptakröfur > Greiðslur > Greiðslubók.</span><span class="sxs-lookup"><span data-stu-id="acaa0-106">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="acaa0-107">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="acaa0-107">Click New.</span></span>
3. <span data-ttu-id="acaa0-108">Í reitnum Heiti skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="acaa0-108">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="acaa0-109">Veldu greiðslubók</span><span class="sxs-lookup"><span data-stu-id="acaa0-109">Select the payment journal.</span></span> 
5. <span data-ttu-id="acaa0-110">Smellið á Línur.</span><span class="sxs-lookup"><span data-stu-id="acaa0-110">Click Lines.</span></span>
6. <span data-ttu-id="acaa0-111">Í svæðinu lykill, veljið þann Viðskiptavin sem verið er að skrá greiðsluna fyrir.</span><span class="sxs-lookup"><span data-stu-id="acaa0-111">In the Account field, select the Customer for whom you are recording the payment.</span></span>
7. <span data-ttu-id="acaa0-112">Færið inn upphæð greiðslunnar í svæðinu Kredit.</span><span class="sxs-lookup"><span data-stu-id="acaa0-112">In the Credit field, enter the amount of the payment.</span></span>
    * <span data-ttu-id="acaa0-113">Hægt er að velja að hafa upphæð autt, og láta kerfið reikna hann með því að velja þá reikninga sem voru greiddir.</span><span class="sxs-lookup"><span data-stu-id="acaa0-113">You can choose to leave the amount blank, and have the system calculate it by selecting the invoices which were paid.</span></span>  
8. <span data-ttu-id="acaa0-114">Færa inn gildi í greiðslutilvísunarsvæðið.</span><span class="sxs-lookup"><span data-stu-id="acaa0-114">In the Payment reference field, type a value.</span></span>
    * <span data-ttu-id="acaa0-115">Greiðslutilvísun gætu vero‘ ávísunarnúmer fyrir greiðslu sem eru færðar inn.</span><span class="sxs-lookup"><span data-stu-id="acaa0-115">The payment reference could be the check number for the payment you are entering.</span></span> <span data-ttu-id="acaa0-116">Greiðslutilvísun er krafist til að taka með greiðslu á innborgunarseðli.</span><span class="sxs-lookup"><span data-stu-id="acaa0-116">The payment reference is required in order to include the payment on a deposit slip.</span></span>  
9. <span data-ttu-id="acaa0-117">Merkja í reitinn Nota innborgunarseðil.</span><span class="sxs-lookup"><span data-stu-id="acaa0-117">Mark the box Use a deposit slip.</span></span>
    * <span data-ttu-id="acaa0-118">Breyta þessari stillingu á Já ef greiðslan skuli vera með í innborgun.</span><span class="sxs-lookup"><span data-stu-id="acaa0-118">If the payment should be included in the deposit, change this setting to Yes.</span></span>  
10. <span data-ttu-id="acaa0-119">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="acaa0-119">Click New.</span></span>
11. <span data-ttu-id="acaa0-120">Í svæðinu lykill, veljið þann Viðskiptavin fyrir næstu greiðsluna.</span><span class="sxs-lookup"><span data-stu-id="acaa0-120">In the Account field, select the Customer for the next payment.</span></span>
12. <span data-ttu-id="acaa0-121">Færið inn upphæð greiðslunnar í svæðinu Kredit.</span><span class="sxs-lookup"><span data-stu-id="acaa0-121">In the Credit field, enter the payment amount.</span></span>
13. <span data-ttu-id="acaa0-122">Færa inn gildi í greiðslutilvísunarsvæðið.</span><span class="sxs-lookup"><span data-stu-id="acaa0-122">In the Payment reference field, type a value.</span></span>
14. <span data-ttu-id="acaa0-123">Merkja í reitinn Nota innborgunarseðil.</span><span class="sxs-lookup"><span data-stu-id="acaa0-123">Mark the box Use a deposit slip.</span></span>
15. <span data-ttu-id="acaa0-124">Smellið á „Bóka“.</span><span class="sxs-lookup"><span data-stu-id="acaa0-124">Click Post.</span></span>
    * <span data-ttu-id="acaa0-125">Verður að bóka greiðslur áður en hægt er að mynda innborgunarseðli.</span><span class="sxs-lookup"><span data-stu-id="acaa0-125">Payments must be posted before the deposit slip can be generated.</span></span> <span data-ttu-id="acaa0-126">Þetta er til að tryggja að greiðslurnar ekki breytast eftir innborgunarseðils er mynduð.</span><span class="sxs-lookup"><span data-stu-id="acaa0-126">This is to ensure that the payments don't change after the deposit slip is generated.</span></span>  
16. <span data-ttu-id="acaa0-127">Smellið á Aðgerðir.</span><span class="sxs-lookup"><span data-stu-id="acaa0-127">Click Functions.</span></span>
17. <span data-ttu-id="acaa0-128">Smellt er á innborgunarseðli.</span><span class="sxs-lookup"><span data-stu-id="acaa0-128">Click Deposit slip.</span></span>
18. <span data-ttu-id="acaa0-129">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="acaa0-129">Click OK.</span></span>
    * <span data-ttu-id="acaa0-130">Fyrsta síða er notuð til að stofna innborgunarseðil.</span><span class="sxs-lookup"><span data-stu-id="acaa0-130">The first page is used to create the deposit slip.</span></span>  
19. <span data-ttu-id="acaa0-131">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="acaa0-131">Click OK.</span></span>
    * <span data-ttu-id="acaa0-132">Önnur skrefið er að prenta innborgunarseðil en þetta skref er ekki nauðsynlegt.</span><span class="sxs-lookup"><span data-stu-id="acaa0-132">The second step is to print the deposit slip, but this step is not required.</span></span>  

