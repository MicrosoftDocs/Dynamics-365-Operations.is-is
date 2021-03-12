---
title: Skrá reikning lánardrottins í reikningabók
description: Þessi leiðarvísi mun sýna hvernig á að skrá reikninga lánardrottins sem eru ekki tengdar við innkaupapantanir.
author: abruer
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendInvoiceWorkspace, LedgerJournalTable, LedgerJournalTransVendInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 18d8b74bd8783c23e548a3185414d1461bc1d869
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971829"
---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a><span data-ttu-id="b079e-103">Skrá reikning lánardrottins í reikningabók</span><span class="sxs-lookup"><span data-stu-id="b079e-103">Record a vendor invoice in the invoice journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b079e-104">Þessi leiðarvísi mun sýna hvernig á að skrá reikninga lánardrottins sem eru ekki tengdar við innkaupapantanir.</span><span class="sxs-lookup"><span data-stu-id="b079e-104">This task guide will show how to record vendor invoices that are not associated with purchase orders.</span></span> <span data-ttu-id="b079e-105">Dæmi um þessa gerð reiknings innihalda kostnað fyrir vörur eða þjónustu.</span><span class="sxs-lookup"><span data-stu-id="b079e-105">Examples of this type of invoice include expenses for supplies or services.</span></span>  <span data-ttu-id="b079e-106">Þessi skráning notar sýnigögn USMF fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="b079e-106">This recording uses the USMF demo company.</span></span>

1. <span data-ttu-id="b079e-107">Farðu Í **Skoðunarrúðu > Einingar > Viðskiptaskuldir > Vinnusvæði > Reikningsfærsla lánardrottins**.</span><span class="sxs-lookup"><span data-stu-id="b079e-107">Go to **Navigation pane > Modules > Accounts payable > Workspaces > Vendor invoice entry**.</span></span>
2. <span data-ttu-id="b079e-108">Í **aðgerðasvæðinu** er smellt á **Ný reikningsbók**.</span><span class="sxs-lookup"><span data-stu-id="b079e-108">On the **Action pane**, click **New invoice journal**.</span></span>
3. <span data-ttu-id="b079e-109">Smellt er á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="b079e-109">Click **New**.</span></span>
4. <span data-ttu-id="b079e-110">Í reitinn **Heiti** færirðu inn heiti færslubókar eða smellir á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="b079e-110">In the **Name** field, enter the journal name or click the drop down button to open the lookup.</span></span>
5. <span data-ttu-id="b079e-111">Í reitinn **Lýsing** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="b079e-111">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="b079e-112">Í **Aðgerðasvæðinu**, smellirðu á **Línur**.</span><span class="sxs-lookup"><span data-stu-id="b079e-112">On the **Action pane**, click **Lines**.</span></span> <span data-ttu-id="b079e-113">Færa inn bókunardagsetningu sem mun uppfæra Fjárhag, í svæði **Dagsetning**.</span><span class="sxs-lookup"><span data-stu-id="b079e-113">In the **Date** field, enter the posting date that will update General Ledger.</span></span>  
7. <span data-ttu-id="b079e-114">Í reitnum **Lykill** skal færa inn **Lánardrottnalykil**.</span><span class="sxs-lookup"><span data-stu-id="b079e-114">In the **Account** field, specify the **Vendor account**.</span></span>
8. <span data-ttu-id="b079e-115">Í reitnum **Reikningur** færirðu inn númer reiknings.</span><span class="sxs-lookup"><span data-stu-id="b079e-115">In the **Invoice** field, enter the invoice number.</span></span>
9. <span data-ttu-id="b079e-116">Í reitinn **Lýsing** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="b079e-116">In the **Description** field, type a value.</span></span>
10. <span data-ttu-id="b079e-117">Í reitnum **Kredit** skal slá inn tölu.</span><span class="sxs-lookup"><span data-stu-id="b079e-117">In the **Credit** field, enter a number.</span></span>
11. <span data-ttu-id="b079e-118">Í svæðinu **Mótlykill**, færið inn lykilnúmer eða smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="b079e-118">In the **Offset account** field, enter the account number or click the drop down button to open the lookup</span></span>
    * <span data-ttu-id="b079e-119">**Vsk-flokkinn** verður sjálfgefnar úr lykli lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="b079e-119">The **Sales tax group** will be default from the vendor account.</span></span>  
    * <span data-ttu-id="b079e-120">**Vsk-flokkur Vöru** eru sjálfgefnar úr aðallykillinn sem tilgreindur er í svæðinu **Mótlykil**.</span><span class="sxs-lookup"><span data-stu-id="b079e-120">The **Item sales tax group** will be default from the main account specified in the **Offset account** field.</span></span>  
    * <span data-ttu-id="b079e-121">**Gjalddagi** er reiknuð út á grundvelli Greiðsluskilmála.</span><span class="sxs-lookup"><span data-stu-id="b079e-121">The **Due date** will be calculated based on the Terms of payment.</span></span>  
    * <span data-ttu-id="b079e-122">**Staðgreiðsluafsláttur** mun vera sjálfgefið úr lykli Lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="b079e-122">The **Cash discount** will default from the Vendor account.</span></span>
12. <span data-ttu-id="b079e-123">Ef verkflæði fyrir reikningsfærslu lánardrottins hefur verið virkjað er smellt á **Verkflæði > Senda**.</span><span class="sxs-lookup"><span data-stu-id="b079e-123">If you have enabled Vendor invoice journal workflow, click **Workflow > Submit**.</span></span>
    * <span data-ttu-id="b079e-124">Þegar sendingin er samþykkt verður dagsetningin færð á fyrsta dag næsta opna tímabils, ef bókunardagsetning færslunna fellur innan tímabils sem er Í bið eða Lokað fyrir fjárhagsbókun.</span><span class="sxs-lookup"><span data-stu-id="b079e-124">When your submission is approved, the date will be advanced to the first day of the next open period, if the transaction posting date falls within a period that is On hold or Closed for ledger posting.</span></span>
12. <span data-ttu-id="b079e-125">Smelltu á **Bóka**.</span><span class="sxs-lookup"><span data-stu-id="b079e-125">Click **Post**.</span></span>
13. <span data-ttu-id="b079e-126">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b079e-126">Close the page.</span></span>

