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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 42f93e6d8fcf62babc3e3244bc1fe76d1efd9d13
ms.contentlocale: is-is
ms.lasthandoff: 08/29/2017

---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a><span data-ttu-id="0e51d-103">Skrá reikning lánardrottins í reikningabók</span><span class="sxs-lookup"><span data-stu-id="0e51d-103">Record a vendor invoice in the invoice journal</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0e51d-104">Þessi leiðarvísi mun sýna hvernig á að skrá reikninga lánardrottins sem eru ekki tengdar við innkaupapantanir.</span><span class="sxs-lookup"><span data-stu-id="0e51d-104">This task guide will show how to record vendor invoices that are not associated with purchase orders.</span></span> <span data-ttu-id="0e51d-105">Dæmi um þessa gerð reiknings innihalda kostnað fyrir vörur eða þjónustu.</span><span class="sxs-lookup"><span data-stu-id="0e51d-105">Examples of this type of invoice include expenses for supplies or services.</span></span>  <span data-ttu-id="0e51d-106">Þessi skráning notar sýnigögn USMF fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="0e51d-106">This recording uses the USMF demo company.</span></span>

1. <span data-ttu-id="0e51d-107">Fara í Viðskiptaskuldir > Vinnusvæði > Færsla fyrir reikning lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="0e51d-107">Go to Accounts payable > Workspaces > Vendor invoice entry.</span></span>
2. <span data-ttu-id="0e51d-108">Smellt er á Ný reikningabók.</span><span class="sxs-lookup"><span data-stu-id="0e51d-108">Click New invoice journal.</span></span>
3. <span data-ttu-id="0e51d-109">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="0e51d-109">Click New.</span></span>
4. <span data-ttu-id="0e51d-110">Færið inn heiti færslubókar eða smellið á fellilistahnappinn til að opna leitina, í svæðið Heiti.</span><span class="sxs-lookup"><span data-stu-id="0e51d-110">In the Name field, enter the journal name or click the drop down button to open the lookup.</span></span>
5. <span data-ttu-id="0e51d-111">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="0e51d-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="0e51d-112">Smellið á „Línur“.</span><span class="sxs-lookup"><span data-stu-id="0e51d-112">Click Lines.</span></span>
    * <span data-ttu-id="0e51d-113">Færa inn bókunardagsetningu sem mun uppfæra Fjárhag, í svæði Dagsetning.</span><span class="sxs-lookup"><span data-stu-id="0e51d-113">In the Date field, enter the posting date that will update General Ledger.</span></span>  
7. <span data-ttu-id="0e51d-114">Í reitnum Lykill skal færa inn Lánardrottnalykil.</span><span class="sxs-lookup"><span data-stu-id="0e51d-114">In the Account field, specify the Vendor account.</span></span>
8. <span data-ttu-id="0e51d-115">Í reitnum Reikningur færirðu inn númer reiknings.</span><span class="sxs-lookup"><span data-stu-id="0e51d-115">In the Invoice field, enter the invoice number.</span></span>
9. <span data-ttu-id="0e51d-116">Í reitinn Lýsing skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="0e51d-116">In the Description field, type a value.</span></span>
10. <span data-ttu-id="0e51d-117">Í reitnum Kredit skal slá inn tölu.</span><span class="sxs-lookup"><span data-stu-id="0e51d-117">In the Credit field, enter a number.</span></span>
11. <span data-ttu-id="0e51d-118">Í svæðinu Mótlykill, færið inn lykilnúmer eða smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="0e51d-118">In the Offset account field, enter the account number or click the drop down button to open the lookup</span></span>
    * <span data-ttu-id="0e51d-119">Vsk-flokkinn eru sjálfgefnar úr lykli lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="0e51d-119">The Sales tax group will default from the vendor account.</span></span>  
    * <span data-ttu-id="0e51d-120">Vsk-flokkur Vöru eru sjálfgefnar úr aðallykillinn sem tilgreindur er í svæðinu Mótlykil.</span><span class="sxs-lookup"><span data-stu-id="0e51d-120">The Item sales tax group will default from the main account specified in the Offset account field.</span></span>  
    * <span data-ttu-id="0e51d-121">Gjalddagi er reiknuð út á grundvelli Greiðsluskilmála.</span><span class="sxs-lookup"><span data-stu-id="0e51d-121">The Due date will be calculated based on the Terms of payment.</span></span>  
    * <span data-ttu-id="0e51d-122">Staðgreiðsluafsláttur mun vera sjálfgefið úr lykli Lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="0e51d-122">The Cash discount will default from the Vendor account.</span></span>  
12. <span data-ttu-id="0e51d-123">Smellið á „Bóka“.</span><span class="sxs-lookup"><span data-stu-id="0e51d-123">Click Post.</span></span>
13. <span data-ttu-id="0e51d-124">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="0e51d-124">Close the page.</span></span>


