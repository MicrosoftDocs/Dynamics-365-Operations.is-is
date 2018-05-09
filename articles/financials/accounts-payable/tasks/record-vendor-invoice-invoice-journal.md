--- 
title: "Skrá reikning lánardrottins í reikningabók"
description: "Þessi leiðarvísi mun sýna hvernig á að skrá reikninga lánardrottins sem eru ekki tengdar við innkaupapantanir."
author: abruer
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 26515140b020d824f99441b9f1ee560a44e28f8f
ms.contentlocale: is-is
ms.lasthandoff: 05/08/2018

---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a><span data-ttu-id="c2f9f-103">Skrá reikning lánardrottins í reikningabók</span><span class="sxs-lookup"><span data-stu-id="c2f9f-103">Record a vendor invoice in the invoice journal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c2f9f-104">Þessi leiðarvísi mun sýna hvernig á að skrá reikninga lánardrottins sem eru ekki tengdar við innkaupapantanir.</span><span class="sxs-lookup"><span data-stu-id="c2f9f-104">This task guide will show how to record vendor invoices that are not associated with purchase orders.</span></span> <span data-ttu-id="c2f9f-105">Dæmi um þessa gerð reiknings innihalda kostnað fyrir vörur eða þjónustu.</span><span class="sxs-lookup"><span data-stu-id="c2f9f-105">Examples of this type of invoice include expenses for supplies or services.</span></span>  <span data-ttu-id="c2f9f-106">Þessi skráning notar sýnigögn USMF fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="c2f9f-106">This recording uses the USMF demo company.</span></span>

1. <span data-ttu-id="c2f9f-107">Fara í Viðskiptaskuldir > Vinnusvæði > Færsla fyrir reikning lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="c2f9f-107">Go to Accounts payable > Workspaces > Vendor invoice entry.</span></span>
2. <span data-ttu-id="c2f9f-108">Smellt er á Ný reikningabók.</span><span class="sxs-lookup"><span data-stu-id="c2f9f-108">Click New invoice journal.</span></span>
3. <span data-ttu-id="c2f9f-109">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="c2f9f-109">Click New.</span></span>
4. <span data-ttu-id="c2f9f-110">Færið inn heiti færslubókar eða smellið á fellilistahnappinn til að opna leitina, í svæðið Heiti.</span><span class="sxs-lookup"><span data-stu-id="c2f9f-110">In the Name field, enter the journal name or click the drop down button to open the lookup.</span></span>
5. <span data-ttu-id="c2f9f-111">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="c2f9f-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="c2f9f-112">Smellið á „Línur“.</span><span class="sxs-lookup"><span data-stu-id="c2f9f-112">Click Lines.</span></span>
    * <span data-ttu-id="c2f9f-113">Færa inn bókunardagsetningu sem mun uppfæra Fjárhag, í svæði Dagsetning.</span><span class="sxs-lookup"><span data-stu-id="c2f9f-113">In the Date field, enter the posting date that will update General Ledger.</span></span>  
7. <span data-ttu-id="c2f9f-114">Í reitnum Lykill skal færa inn Lánardrottnalykil.</span><span class="sxs-lookup"><span data-stu-id="c2f9f-114">In the Account field, specify the Vendor account.</span></span>
8. <span data-ttu-id="c2f9f-115">Í reitnum Reikningur færirðu inn númer reiknings.</span><span class="sxs-lookup"><span data-stu-id="c2f9f-115">In the Invoice field, enter the invoice number.</span></span>
9. <span data-ttu-id="c2f9f-116">Í reitinn Lýsing skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="c2f9f-116">In the Description field, type a value.</span></span>
10. <span data-ttu-id="c2f9f-117">Í reitnum Kredit skal slá inn tölu.</span><span class="sxs-lookup"><span data-stu-id="c2f9f-117">In the Credit field, enter a number.</span></span>
11. <span data-ttu-id="c2f9f-118">Í svæðinu Mótlykill, færið inn lykilnúmer eða smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="c2f9f-118">In the Offset account field, enter the account number or click the drop down button to open the lookup</span></span>
    * <span data-ttu-id="c2f9f-119">Vsk-flokkinn eru sjálfgefnar úr lykli lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="c2f9f-119">The Sales tax group will default from the vendor account.</span></span>  
    * <span data-ttu-id="c2f9f-120">Vsk-flokkur Vöru eru sjálfgefnar úr aðallykillinn sem tilgreindur er í svæðinu Mótlykil.</span><span class="sxs-lookup"><span data-stu-id="c2f9f-120">The Item sales tax group will default from the main account specified in the Offset account field.</span></span>  
    * <span data-ttu-id="c2f9f-121">Gjalddagi er reiknuð út á grundvelli Greiðsluskilmála.</span><span class="sxs-lookup"><span data-stu-id="c2f9f-121">The Due date will be calculated based on the Terms of payment.</span></span>  
    * <span data-ttu-id="c2f9f-122">Staðgreiðsluafsláttur mun vera sjálfgefið úr lykli Lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="c2f9f-122">The Cash discount will default from the Vendor account.</span></span>  
12. <span data-ttu-id="c2f9f-123">Smellið á „Bóka“.</span><span class="sxs-lookup"><span data-stu-id="c2f9f-123">Click Post.</span></span>
13. <span data-ttu-id="c2f9f-124">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="c2f9f-124">Close the page.</span></span>


