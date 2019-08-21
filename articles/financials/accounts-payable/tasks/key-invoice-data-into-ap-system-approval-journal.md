---
title: Lykilgögn reiknings í AP kerfið með því að nota færslubókarsamþykkt
description: Þessi leiðarvísi fyrir verk sýnir hvernig á að nota komubók til að stofna reikninga og nota síðan færslubókarsamþykkt til að uppfæra kostnaðarlykla.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransInvoiceRegister, HcmWorkerLookUp, LedgerJournalTransApprove, LedgerJournalTransApproveFetchVouchers, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0faece510cc85fd86113d8b62d54b71f3014b1db
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/01/2019
ms.locfileid: "1837041"
---
# <a name="key-invoice-data-into-ap-system-using-approval-journal"></a><span data-ttu-id="bd4ce-103">Lykilgögn reiknings í AP kerfið með því að nota færslubókarsamþykkt</span><span class="sxs-lookup"><span data-stu-id="bd4ce-103">Key invoice data into AP system using approval journal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bd4ce-104">Þessi leiðarvísi fyrir verk sýnir hvernig á að nota komubók til að stofna reikninga og nota síðan færslubókarsamþykkt til að uppfæra kostnaðarlykla.</span><span class="sxs-lookup"><span data-stu-id="bd4ce-104">This task guide will show you how to use the invoice register to create invoices and then use the approval journal to update the expense accounts.</span></span>


## <a name="create-and-post-and-invoice"></a><span data-ttu-id="bd4ce-105">Stofna og bóka og reikningsfæra</span><span class="sxs-lookup"><span data-stu-id="bd4ce-105">Create and post and invoice</span></span>
1. <span data-ttu-id="bd4ce-106">Fara í Viðskiptaskuldir > Reikningar > Komubók.</span><span class="sxs-lookup"><span data-stu-id="bd4ce-106">Go to Accounts payable > Invoices > Invoice register.</span></span>
2. <span data-ttu-id="bd4ce-107">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="bd4ce-107">Click New.</span></span>
3. <span data-ttu-id="bd4ce-108">Veldu heiti komubókarinnar sem þú vilt nota.</span><span class="sxs-lookup"><span data-stu-id="bd4ce-108">Select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="bd4ce-109">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="bd4ce-109">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="bd4ce-110">Smellið á Línur til að opna afgreiðslukassann og færa inn kostnaðarlínur.</span><span class="sxs-lookup"><span data-stu-id="bd4ce-110">Click on Lines to open the register and enter expense lines.</span></span>
6. <span data-ttu-id="bd4ce-111">Veljið lánardrottin.</span><span class="sxs-lookup"><span data-stu-id="bd4ce-111">Select a vendor.</span></span> <span data-ttu-id="bd4ce-112">Til dæmis færirðu inn eða velur US-104</span><span class="sxs-lookup"><span data-stu-id="bd4ce-112">For example, enter or select US-104</span></span>
7. <span data-ttu-id="bd4ce-113">Í reitinn Reikningur skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="bd4ce-113">In the Invoice field, type a value.</span></span>
8. <span data-ttu-id="bd4ce-114">Í reitinn Lýsing skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="bd4ce-114">In the Description field, type a value.</span></span>
9. <span data-ttu-id="bd4ce-115">Í reitnum Kredit skal slá inn tölu.</span><span class="sxs-lookup"><span data-stu-id="bd4ce-115">In the Credit field, enter a number.</span></span>
10. <span data-ttu-id="bd4ce-116">Í reitnum Samþykkt skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="bd4ce-116">In the Approved by field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="bd4ce-117">Merkið samþykkjanda og smelltu á Velja til að velja þann samþykkjanda.</span><span class="sxs-lookup"><span data-stu-id="bd4ce-117">Highlight an approver and click Select to select that approver.</span></span>
12. <span data-ttu-id="bd4ce-118">Smellið á „Bóka“.</span><span class="sxs-lookup"><span data-stu-id="bd4ce-118">Click Post.</span></span>
13. <span data-ttu-id="bd4ce-119">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="bd4ce-119">Close the page.</span></span>
14. <span data-ttu-id="bd4ce-120">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="bd4ce-120">Close the page.</span></span>

## <a name="approve-an-invoice"></a><span data-ttu-id="bd4ce-121">Samþykkja reikning</span><span class="sxs-lookup"><span data-stu-id="bd4ce-121">Approve an invoice</span></span>
1. <span data-ttu-id="bd4ce-122">Fara í Viðskiptaskuldir > Reikningar > Reikningssamþykki.</span><span class="sxs-lookup"><span data-stu-id="bd4ce-122">Go to Accounts payable > Invoices > Invoice approval.</span></span>
2. <span data-ttu-id="bd4ce-123">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="bd4ce-123">Click New.</span></span>
3. <span data-ttu-id="bd4ce-124">Veldu heiti færslubókarsamþykkt reiknings sem þú vilt nota.</span><span class="sxs-lookup"><span data-stu-id="bd4ce-124">Select the name of the invoice approval journal that you want to use.</span></span>
4. <span data-ttu-id="bd4ce-125">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="bd4ce-125">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="bd4ce-126">Smellið á línur til að birta síðu þar sem er hægt að velja reikninga sem á að samþykkja.</span><span class="sxs-lookup"><span data-stu-id="bd4ce-126">Click lines to display a page where you will be able to select the invoices that you want to approve.</span></span>
6. <span data-ttu-id="bd4ce-127">Veljið Finna Fylgiskjöl til að birta alla reikninga sem eru tilbúnar til samþykkis.</span><span class="sxs-lookup"><span data-stu-id="bd4ce-127">Select Find Vouchers to display all of the invoices that are ready for approval.</span></span>
7. <span data-ttu-id="bd4ce-128">Merkja reikninginn sem þú stofnaðir.</span><span class="sxs-lookup"><span data-stu-id="bd4ce-128">Mark the invoice that you created.</span></span>
8. <span data-ttu-id="bd4ce-129">Smellið á Velja.</span><span class="sxs-lookup"><span data-stu-id="bd4ce-129">Click Select.</span></span>
    * <span data-ttu-id="bd4ce-130">Fylgiskjala sem valinn er fyrir ofan eru fluttar yfir á þessum lista eftir að þeim var valið.</span><span class="sxs-lookup"><span data-stu-id="bd4ce-130">The vouchers that you selected above are moved to this list after you select them.</span></span>  
9. <span data-ttu-id="bd4ce-131">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="bd4ce-131">Click OK.</span></span>
10. <span data-ttu-id="bd4ce-132">Smella á svæðið lykilnúmers til að bæta kostnaðarlykli við reikning.</span><span class="sxs-lookup"><span data-stu-id="bd4ce-132">Click on the account number field to add an expense account to the invoice.</span></span>
11. <span data-ttu-id="bd4ce-133">Færið inn lykilnúmer og flipinn við svæðið.</span><span class="sxs-lookup"><span data-stu-id="bd4ce-133">Enter an account number and tab off of the field.</span></span> <span data-ttu-id="bd4ce-134">Til dæmis færirðu inn 600120.</span><span class="sxs-lookup"><span data-stu-id="bd4ce-134">For example, enter 600120.</span></span>
12. <span data-ttu-id="bd4ce-135">Smellið á „Bóka“.</span><span class="sxs-lookup"><span data-stu-id="bd4ce-135">Click Post.</span></span>
13. <span data-ttu-id="bd4ce-136">Smellt er á Fylgiskjal til að skoða færslur sem voru bókaðar.</span><span class="sxs-lookup"><span data-stu-id="bd4ce-136">Click Voucher to view the entries that were posted.</span></span>
    * <span data-ttu-id="bd4ce-137">Lykill Reiknings sem bíður samþykkist er bakfærður og skipt út fyrir raunverulega kostnaðarlykil.</span><span class="sxs-lookup"><span data-stu-id="bd4ce-137">The Invoice Pending Approval account is reversed and replaced with the actual expense account.</span></span>  

