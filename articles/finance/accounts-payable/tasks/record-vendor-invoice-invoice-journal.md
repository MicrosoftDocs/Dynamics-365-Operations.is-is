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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5277081d9f7adcc43c30d30208d13c7e39d76118
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140376"
---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a><span data-ttu-id="86c61-103">Skrá reikning lánardrottins í reikningabók</span><span class="sxs-lookup"><span data-stu-id="86c61-103">Record a vendor invoice in the invoice journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="86c61-104">Þessi leiðarvísi mun sýna hvernig á að skrá reikninga lánardrottins sem eru ekki tengdar við innkaupapantanir.</span><span class="sxs-lookup"><span data-stu-id="86c61-104">This task guide will show how to record vendor invoices that are not associated with purchase orders.</span></span> <span data-ttu-id="86c61-105">Dæmi um þessa gerð reiknings innihalda kostnað fyrir vörur eða þjónustu.</span><span class="sxs-lookup"><span data-stu-id="86c61-105">Examples of this type of invoice include expenses for supplies or services.</span></span>  <span data-ttu-id="86c61-106">Þessi skráning notar sýnigögn USMF fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="86c61-106">This recording uses the USMF demo company.</span></span>

1. <span data-ttu-id="86c61-107">Farðu Í **Skoðunarrúðu > Einingar > Viðskiptaskuldir > Vinnusvæði > Reikningsfærsla lánardrottins**.</span><span class="sxs-lookup"><span data-stu-id="86c61-107">Go to **Navigation pane > Modules > Accounts payable > Workspaces > Vendor invoice entry**.</span></span>
2. <span data-ttu-id="86c61-108">Í **aðgerðasvæðinu** er smellt á **Ný reikningsbók**.</span><span class="sxs-lookup"><span data-stu-id="86c61-108">On the **Action pane**, click **New invoice journal**.</span></span>
3. <span data-ttu-id="86c61-109">Smellt er á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="86c61-109">Click **New**.</span></span>
4. <span data-ttu-id="86c61-110">Í reitinn **Heiti** færirðu inn heiti færslubókar eða smellir á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="86c61-110">In the **Name** field, enter the journal name or click the drop down button to open the lookup.</span></span>
5. <span data-ttu-id="86c61-111">Í reitinn **Lýsing** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="86c61-111">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="86c61-112">Í **Aðgerðasvæðinu**, smellirðu á **Línur**.</span><span class="sxs-lookup"><span data-stu-id="86c61-112">On the **Action pane**, click **Lines**.</span></span> <span data-ttu-id="86c61-113">Færa inn bókunardagsetningu sem mun uppfæra Fjárhag, í svæði **Dagsetning**.</span><span class="sxs-lookup"><span data-stu-id="86c61-113">In the **Date** field, enter the posting date that will update General Ledger.</span></span>  
7. <span data-ttu-id="86c61-114">Í reitnum **Lykill** skal færa inn **Lánardrottnalykil**.</span><span class="sxs-lookup"><span data-stu-id="86c61-114">In the **Account** field, specify the **Vendor account**.</span></span>
8. <span data-ttu-id="86c61-115">Í reitnum **Reikningur** færirðu inn númer reiknings.</span><span class="sxs-lookup"><span data-stu-id="86c61-115">In the **Invoice** field, enter the invoice number.</span></span>
9. <span data-ttu-id="86c61-116">Í reitinn **Lýsing** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="86c61-116">In the **Description** field, type a value.</span></span>
10. <span data-ttu-id="86c61-117">Í reitnum **Kredit** skal slá inn tölu.</span><span class="sxs-lookup"><span data-stu-id="86c61-117">In the **Credit** field, enter a number.</span></span>
11. <span data-ttu-id="86c61-118">Í svæðinu **Mótlykill**, færið inn lykilnúmer eða smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="86c61-118">In the **Offset account** field, enter the account number or click the drop down button to open the lookup</span></span>
    * <span data-ttu-id="86c61-119">**Vsk-flokkinn** verður sjálfgefnar úr lykli lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="86c61-119">The **Sales tax group** will be default from the vendor account.</span></span>  
    * <span data-ttu-id="86c61-120">**Vsk-flokkur Vöru** eru sjálfgefnar úr aðallykillinn sem tilgreindur er í svæðinu **Mótlykil**.</span><span class="sxs-lookup"><span data-stu-id="86c61-120">The **Item sales tax group** will be default from the main account specified in the **Offset account** field.</span></span>  
    * <span data-ttu-id="86c61-121">**Gjalddagi** er reiknuð út á grundvelli Greiðsluskilmála.</span><span class="sxs-lookup"><span data-stu-id="86c61-121">The **Due date** will be calculated based on the Terms of payment.</span></span>  
    * <span data-ttu-id="86c61-122">**Staðgreiðsluafsláttur** mun vera sjálfgefið úr lykli Lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="86c61-122">The **Cash discount** will default from the Vendor account.</span></span>  
12. <span data-ttu-id="86c61-123">Smelltu á **Bóka**.</span><span class="sxs-lookup"><span data-stu-id="86c61-123">Click **Post**.</span></span>
13. <span data-ttu-id="86c61-124">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="86c61-124">Close the page.</span></span>

