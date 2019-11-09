---
title: Færa reikningsgögn inn í viðskiptaskuldir með færslubókarsamþykkt
description: Þetta efni útskýrir sýnir hvernig á að nota komubók til að stofna reikninga og nota síðan færslubókarsamþykkt til að uppfæra kostnaðarlykla.
author: abruer
manager: AnnBe
ms.date: 08/08/2019
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
ms.openlocfilehash: fb690769a33f88e63ab8f54cec69a5e927fd324c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178347"
---
# <a name="key-invoice-data-into-accounts-payable-using-an-approval-journal"></a><span data-ttu-id="8d0e6-103">Færa reikningsgögn inn í viðskiptaskuldir með færslubókarsamþykkt</span><span class="sxs-lookup"><span data-stu-id="8d0e6-103">Key invoice data into accounts payable using an approval journal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8d0e6-104">Þetta efni útskýrir sýnir hvernig á að nota komubók til að stofna reikninga og nota síðan færslubókarsamþykkt til að uppfæra kostnaðarlykla.</span><span class="sxs-lookup"><span data-stu-id="8d0e6-104">This topic explains how to use the invoice register to create invoices and then use the approval journal to update the expense accounts.</span></span>

## <a name="create-and-post-and-invoice"></a><span data-ttu-id="8d0e6-105">Stofna og bóka og reikningsfæra</span><span class="sxs-lookup"><span data-stu-id="8d0e6-105">Create and post and invoice</span></span>
1. <span data-ttu-id="8d0e6-106">Í skoðunarrúðunni ferðu í **Einingar > Viðskiptaskuldir > Reikningar > Komubók**.</span><span class="sxs-lookup"><span data-stu-id="8d0e6-106">In the navigation pan, go to **Modules > Accounts payable > Invoices > Invoice register**.</span></span>
2. <span data-ttu-id="8d0e6-107">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="8d0e6-107">Select **New**.</span></span>
3. <span data-ttu-id="8d0e6-108">Veldu heiti komubókarinnar sem þú vilt nota.</span><span class="sxs-lookup"><span data-stu-id="8d0e6-108">Select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="8d0e6-109">Veldu **Línur** til að opna skrána og færa inn kostnaðarlínur.</span><span class="sxs-lookup"><span data-stu-id="8d0e6-109">Select **Lines** to open the register and enter expense lines.</span></span>
5. <span data-ttu-id="8d0e6-110">Veljið lánardrottin.</span><span class="sxs-lookup"><span data-stu-id="8d0e6-110">Select a vendor.</span></span> <span data-ttu-id="8d0e6-111">Til dæmis færirðu inn eða velur `US-104`.</span><span class="sxs-lookup"><span data-stu-id="8d0e6-111">For example, enter or select `US-104`.</span></span>
6. <span data-ttu-id="8d0e6-112">Í reitnum **Reikningur** færirðu inn gildi.</span><span class="sxs-lookup"><span data-stu-id="8d0e6-112">In the **Invoice** field, type a value.</span></span>
7. <span data-ttu-id="8d0e6-113">Í reitinn **Lýsing** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="8d0e6-113">In the **Description** field, type a value.</span></span>
8. <span data-ttu-id="8d0e6-114">Í reitnum **Kredit** skal slá inn tölu.</span><span class="sxs-lookup"><span data-stu-id="8d0e6-114">In the **Credit** field, enter a number.</span></span>
9. <span data-ttu-id="8d0e6-115">Í reitnum **Samþykkt af** velurðu samþykktaraðila úr fellivalmyndinni.</span><span class="sxs-lookup"><span data-stu-id="8d0e6-115">In the **Approved by** field, select an approver from the drop-down menu.</span></span>
10. <span data-ttu-id="8d0e6-116">Veldu **Bóka**.</span><span class="sxs-lookup"><span data-stu-id="8d0e6-116">Select **Post**.</span></span>

## <a name="approve-an-invoice"></a><span data-ttu-id="8d0e6-117">Samþykkja reikning</span><span class="sxs-lookup"><span data-stu-id="8d0e6-117">Approve an invoice</span></span>
1. <span data-ttu-id="8d0e6-118">Í skoðunarrúðunni ferðu í **Einingar > Viðskiptaskuldir > Reikningar > Reikningssamþykki**.</span><span class="sxs-lookup"><span data-stu-id="8d0e6-118">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice approval**.</span></span>
2. <span data-ttu-id="8d0e6-119">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="8d0e6-119">Select **New**.</span></span>
3. <span data-ttu-id="8d0e6-120">Veldu heiti færslubókarsamþykkt reiknings sem þú vilt nota.</span><span class="sxs-lookup"><span data-stu-id="8d0e6-120">Select the name of the invoice approval journal that you want to use.</span></span>
4. <span data-ttu-id="8d0e6-121">Veldu **Línur** til að birta síðu þar sem er hægt að velja reikninga sem á að samþykkja.</span><span class="sxs-lookup"><span data-stu-id="8d0e6-121">Select **Lines** to display a page where you will be able to select the invoices that you want to approve.</span></span>
5. <span data-ttu-id="8d0e6-122">Veljið **Finna fylgiskjöl** til að birta alla reikninga sem eru tilbúnar til samþykkis.</span><span class="sxs-lookup"><span data-stu-id="8d0e6-122">Select **Find Vouchers** to display all of the invoices that are ready for approval.</span></span>
6. <span data-ttu-id="8d0e6-123">Merktu við reikninginn sem þú bjóst til og smelltu síðan á **Velja**.</span><span class="sxs-lookup"><span data-stu-id="8d0e6-123">Mark the invoice that you created, then click **Select**.</span></span> <span data-ttu-id="8d0e6-124">Fylgiskjala sem valinn er fyrir ofan eru fluttar yfir á þessum lista eftir að þeim var valið.</span><span class="sxs-lookup"><span data-stu-id="8d0e6-124">The vouchers that you selected above are moved to this list after you select them.</span></span>  
7. <span data-ttu-id="8d0e6-125">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="8d0e6-125">Select **OK**.</span></span>
8. <span data-ttu-id="8d0e6-126">Veldu reitinn **Lykilnúmer** til að bæta kostnaðarlykli við reikning.</span><span class="sxs-lookup"><span data-stu-id="8d0e6-126">Select the **account number** field to add an expense account to the invoice.</span></span>
9. <span data-ttu-id="8d0e6-127">Færið inn lykilnúmer og flipinn við svæðið.</span><span class="sxs-lookup"><span data-stu-id="8d0e6-127">Enter an account number and tab off of the field.</span></span> <span data-ttu-id="8d0e6-128">Til dæmis er slegið inn `600120`.</span><span class="sxs-lookup"><span data-stu-id="8d0e6-128">For example, enter `600120`.</span></span>
10. <span data-ttu-id="8d0e6-129">Veldu **Bóka**.</span><span class="sxs-lookup"><span data-stu-id="8d0e6-129">Select **Post**.</span></span>
11. <span data-ttu-id="8d0e6-130">Veldu **Fylgiskjal** til að skoða færslur sem voru bókaðar.</span><span class="sxs-lookup"><span data-stu-id="8d0e6-130">Select **Voucher** to view the entries that were posted.</span></span> <span data-ttu-id="8d0e6-131">Lykill Reiknings sem bíður samþykkist er bakfærður og skipt út fyrir raunverulega kostnaðarlykil.</span><span class="sxs-lookup"><span data-stu-id="8d0e6-131">The Invoice Pending Approval account is reversed and replaced with the actual expense account.</span></span>  
