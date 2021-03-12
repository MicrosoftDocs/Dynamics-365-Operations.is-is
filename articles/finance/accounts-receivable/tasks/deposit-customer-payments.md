---
title: Leggja inn greiðslur viðskiptavina
description: Innborgun á greiðslum viðskiptavina.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransCustPaym, CustTableLookup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9221101581a6a130889b7c941ca228070a000c56
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003157"
---
# <a name="deposit-customer-payments"></a><span data-ttu-id="abdde-103">Leggja inn greiðslur viðskiptavina</span><span class="sxs-lookup"><span data-stu-id="abdde-103">Deposit customer payments</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="abdde-104">Innborgun á greiðslum viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="abdde-104">Deposit customer payments.</span></span> <span data-ttu-id="abdde-105">Þetta verkefni notar USMF-sýnifyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="abdde-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="abdde-106">Farðu í **Skoðunarrúðu > Kerfiseiningar > Viðskiptakröfur > Greiðslur > Greiðslubók**.</span><span class="sxs-lookup"><span data-stu-id="abdde-106">Go to **Navigation pane > Modules > Accounts receivable > Payments > Payment journal**.</span></span>
2. <span data-ttu-id="abdde-107">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="abdde-107">Select **New**.</span></span>
3. <span data-ttu-id="abdde-108">Í reitnum **Heiti** velurðu **CustPay** í fellivalmyndinni.</span><span class="sxs-lookup"><span data-stu-id="abdde-108">In the **Name** field, select **CustPay** in the drop-down menu.</span></span>
4. <span data-ttu-id="abdde-109">Veldu **Línur**.</span><span class="sxs-lookup"><span data-stu-id="abdde-109">Select **Lines**.</span></span>
5. <span data-ttu-id="abdde-110">Í svæðinu **Lykill** velurðu þann viðskiptavin sem verið er að skrá greiðsluna fyrir.</span><span class="sxs-lookup"><span data-stu-id="abdde-110">In the **Account** field, select the customer for whom you are recording the payment.</span></span>
6. <span data-ttu-id="abdde-111">Í reitinn **Kredit** skal færa inn upphæð greiðslunnar.</span><span class="sxs-lookup"><span data-stu-id="abdde-111">In the **Credit** field, enter the amount of the payment.</span></span> <span data-ttu-id="abdde-112">Hægt er að velja að hafa upphæð autt, og láta kerfið reikna hann með því að velja þá reikninga sem voru greiddir.</span><span class="sxs-lookup"><span data-stu-id="abdde-112">You can choose to leave the amount blank, and have the system calculate it by selecting the invoices which were paid.</span></span>  
7. <span data-ttu-id="abdde-113">Í reitinn **Greiðslutilvísun** ritarðu gildi.</span><span class="sxs-lookup"><span data-stu-id="abdde-113">In the **Payment reference** field, type a value.</span></span> <span data-ttu-id="abdde-114">Greiðslutilvísun gætu vero‘ ávísunarnúmer fyrir greiðslu sem eru færðar inn.</span><span class="sxs-lookup"><span data-stu-id="abdde-114">The payment reference could be the check number for the payment you are entering.</span></span> <span data-ttu-id="abdde-115">Greiðslutilvísun er krafist til að taka með greiðslu á innborgunarseðli.</span><span class="sxs-lookup"><span data-stu-id="abdde-115">The payment reference is required in order to include the payment on a deposit slip.</span></span>  
8. <span data-ttu-id="abdde-116">Merkja í reitinn Nota innborgunarseðil.</span><span class="sxs-lookup"><span data-stu-id="abdde-116">Mark the box Use a deposit slip.</span></span> <span data-ttu-id="abdde-117">Breyta þessari stillingu á Já ef greiðslan skuli vera með í innborgun.</span><span class="sxs-lookup"><span data-stu-id="abdde-117">If the payment should be included in the deposit, change this setting to Yes.</span></span>  
9. <span data-ttu-id="abdde-118">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="abdde-118">Select **New**.</span></span>
10. <span data-ttu-id="abdde-119">Í reitinn **Lykill** velurðu viðskiptavin fyrir næstu greiðslu.</span><span class="sxs-lookup"><span data-stu-id="abdde-119">In the **Account** field, select the customer for the next payment.</span></span>
11. <span data-ttu-id="abdde-120">Í reitinn **Kredit** skal færa inn greiðsluupphæðina.</span><span class="sxs-lookup"><span data-stu-id="abdde-120">In the **Credit** field, enter the payment amount.</span></span>
12. <span data-ttu-id="abdde-121">Í reitinn **Greiðslutilvísun** ritarðu gildi.</span><span class="sxs-lookup"><span data-stu-id="abdde-121">In the **Payment reference** field, type a value.</span></span>
13. <span data-ttu-id="abdde-122">Merktu í reitinn **Nota innborgunarseðil**.</span><span class="sxs-lookup"><span data-stu-id="abdde-122">Mark the box **Use a deposit slip**.</span></span>
14. <span data-ttu-id="abdde-123">Veldu **Bóka**.</span><span class="sxs-lookup"><span data-stu-id="abdde-123">Select **Post**.</span></span> <span data-ttu-id="abdde-124">Verður að bóka greiðslur áður en hægt er að mynda innborgunarseðli.</span><span class="sxs-lookup"><span data-stu-id="abdde-124">Payments must be posted before the deposit slip can be generated.</span></span> <span data-ttu-id="abdde-125">Þetta er til að tryggja að greiðslurnar ekki breytast eftir innborgunarseðils er mynduð.</span><span class="sxs-lookup"><span data-stu-id="abdde-125">This is to ensure that the payments don't change after the deposit slip is generated.</span></span>  
15. <span data-ttu-id="abdde-126">Veljið **Aðgerðir**.</span><span class="sxs-lookup"><span data-stu-id="abdde-126">Select **Functions**.</span></span>
16. <span data-ttu-id="abdde-127">Veldu **Innborgunarseðil**.</span><span class="sxs-lookup"><span data-stu-id="abdde-127">Select **Deposit slip**.</span></span>
17. <span data-ttu-id="abdde-128">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="abdde-128">Select **OK**.</span></span> <span data-ttu-id="abdde-129">Fyrsta síða er notuð til að stofna innborgunarseðil.</span><span class="sxs-lookup"><span data-stu-id="abdde-129">The first page is used to create the deposit slip.</span></span>  
18. <span data-ttu-id="abdde-130">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="abdde-130">Select **OK**.</span></span> <span data-ttu-id="abdde-131">Önnur skrefið er að prenta innborgunarseðil en þetta skref er ekki nauðsynlegt.</span><span class="sxs-lookup"><span data-stu-id="abdde-131">The second step is to print the deposit slip, but this step is not required.</span></span>  

