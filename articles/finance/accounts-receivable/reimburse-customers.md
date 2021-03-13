---
title: Endurgreiða viðskiptavini
description: Í þessu grein útskýrt hvernig stofna endurgreiðslufærslurnar fyrir flokk af viðskiptavinum. Ef viðskiptavinur hefur kreditstöðu er hægt er að endurgreiða viðskiptavininum upphæð stöðunnar.
author: JodiChristiansen
manager: AnnBe
ms.date: 09/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransCustPaym, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: roschlom
ms.custom: 14191
ms.assetid: 53533ee3-470e-458a-ac8b-3815aa4cb502
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ae6a3078743fc9cd43c71bc1d4531c0553ee53bb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "5012140"
---
# <a name="reimburse-customers"></a><span data-ttu-id="cdeda-104">Endurgreiða viðskiptavini</span><span class="sxs-lookup"><span data-stu-id="cdeda-104">Reimburse customers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cdeda-105">Í þessu grein útskýrt hvernig stofna endurgreiðslufærslurnar fyrir flokk af viðskiptavinum.</span><span class="sxs-lookup"><span data-stu-id="cdeda-105">This article explains how to create reimbursement transactions for a group of customers.</span></span> <span data-ttu-id="cdeda-106">Ef viðskiptavinur hefur kreditstöðu er hægt er að endurgreiða viðskiptavininum upphæð stöðunnar.</span><span class="sxs-lookup"><span data-stu-id="cdeda-106">If a customer has a credit balance, you can reimburse the customer for the amount of the balance.</span></span> 

<span data-ttu-id="cdeda-107">Eftirfarandi tafla sýnir forkröfur sem verður að vera til staðar áður en byrjað er.</span><span class="sxs-lookup"><span data-stu-id="cdeda-107">The following table shows the prerequisites that must be in place before you start.</span></span>

| <span data-ttu-id="cdeda-108">Skilyrði</span><span class="sxs-lookup"><span data-stu-id="cdeda-108">Prerequisite</span></span>                                                            | <span data-ttu-id="cdeda-109">Lýsing</span><span class="sxs-lookup"><span data-stu-id="cdeda-109">Description</span></span> |
|-------------------------------------------------------------------------|-------------|
| <span data-ttu-id="cdeda-110">Tilgreina lágmarks endurgreiðsluupphæð fyrir lögaðilann</span><span class="sxs-lookup"><span data-stu-id="cdeda-110">Specify the minimum reimbursement amount for the legal entity.</span></span>          | <span data-ttu-id="cdeda-111">Á **Færibreytur viðskiptakrafna** síðunni, á svæðinu **Almennt** á **Lágmarks endurgreiðsla** svæðinu, færið inn lágmarksupphæð sem hægt er að endurgreiða fyrir°ofgreiðslu viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="cdeda-111">On the **Accounts receivable parameters** page, in the **General** area, in the **Minimum reimbursement** field, enter the minimum amount that can be reimbursed for customer overpayments.</span></span> |
| <span data-ttu-id="cdeda-112">Valfrjálst: Bæta lánardrottnareikningi við hvern viðskiptavin sem er hægt að endurgreiða.</span><span class="sxs-lookup"><span data-stu-id="cdeda-112">Optional: Add a vendor account to each customer that can be reimbursed.</span></span> | <span data-ttu-id="cdeda-113">Á°síðunni **Viðskiptavinir** í flýtiflipanum **Ýmsar upplýsingar** á svæðinu **Lánardrottnalykill** skal°velja lánardrottnalykilinn fyrir viðskiptavin.</span><span class="sxs-lookup"><span data-stu-id="cdeda-113">On the **Customers** page, on the **Miscellaneous details** FastTab, in the **Vendor account** field, select the vendor account for the customer.</span></span> |

<span data-ttu-id="cdeda-114">Þegar endurgreiðslufærslur eru stofnaðar, er reikningur lánardrottins stofnaður fyrir upphæð kreditstöðunnar.</span><span class="sxs-lookup"><span data-stu-id="cdeda-114">When you create reimbursement transactions, a vendor invoice is created for the amount of the credit balance.</span></span> <span data-ttu-id="cdeda-115">Endurgreiðsluferlið°fjarlægir kreditstöðu fyrir viðskiptavinalykilinn og stofnar stöðu greiðslu fyrir lykil lánardrottins sem samsvarar viðskiptavininum.</span><span class="sxs-lookup"><span data-stu-id="cdeda-115">The reimbursement process removes the credit balance for the customer account and creates a balance due for the vendor account that corresponds to the customer.</span></span>

1. <span data-ttu-id="cdeda-116">Í viðskiptakröfur, keyrið ferlið **Endurgreiðsla**. (**Vinna úr viðskiptakröfur \> Reglubundin verkefni \> Endurgreiðsla**).</span><span class="sxs-lookup"><span data-stu-id="cdeda-116">In Accounts receivable, run the **Reimbursement** process (**Accounts receivable \> Periodic tasks \> Reimbursement**).</span></span>
2. <span data-ttu-id="cdeda-117">Til að flokka allar færslur, án tillits til fjárhagsvíddar, skal stilla valkostinn **Taka saman fyrir viðskiptavin** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="cdeda-117">To group all transactions, regardless of ledger dimensions, set the **Summarize customer** option to **Yes**.</span></span> <span data-ttu-id="cdeda-118">Til að flokka aðeins færslur sem eru með svipaðar fjárhagsvíddir skal stilla valkostinn á **Nei**.</span><span class="sxs-lookup"><span data-stu-id="cdeda-118">To group only transactions that have similar ledger dimensions, set the option to **No**.</span></span>
3. <span data-ttu-id="cdeda-119">Veljið **Hafa með viðskiptavini með útistandandi debetfærslur** til að velja viðskiptamenn sem eru með ójafnaðar debetupphæðir.</span><span class="sxs-lookup"><span data-stu-id="cdeda-119">Select **Include customers with outstanding debit transactions** to select customers who have unsettled debit amounts.</span></span>
4. <span data-ttu-id="cdeda-120">Til að endurgreiða tiltekna viðskiptavinalykla skal opna flýtiflipann **Færslur til að taka með** og velja **Sía** og tilgreina síðan viðskiptavinalykla í fyrirspurninni.</span><span class="sxs-lookup"><span data-stu-id="cdeda-120">To reimburse specific customer accounts, on the **Records to include** FastTab, select **Filter**, and then specify the customer accounts in the query.</span></span>

    <span data-ttu-id="cdeda-121">Kreditupphæðir eru fluttar í lánardrottnarlykla viðskiptavinar og eru unnar eins og venjulegar greiðslur.</span><span class="sxs-lookup"><span data-stu-id="cdeda-121">The credit amounts are transferred to the vendor accounts of the customers and are processed as ordinary payments.</span></span> <span data-ttu-id="cdeda-122">Ef viðskiptamaður er ekki með lánardrottnarlykil er sjálfkrafa búið til númer einsskiptislánardrottins handa viðskiptamanninum.</span><span class="sxs-lookup"><span data-stu-id="cdeda-122">If a customer doesn't have a vendor account, a one-time vendor account is automatically created for the customer.</span></span>

5. <span data-ttu-id="cdeda-123">Til að skoða endurgreiðslufærslur sem voru stofnaðar, skal nota skýrsluna **Endurgreiðsla** (**Viðskiptakröfur \> Fyrirspurnir og skýrslur \> Endurgreiðsluskýrsla**).</span><span class="sxs-lookup"><span data-stu-id="cdeda-123">To view the reimbursement transactions that were created, use the **Reimbursement** report (**Accounts Receivable \> Inquiries and reports \> Reimbursement report**).</span></span>
6. <span data-ttu-id="cdeda-124">Í Viðskiptaskuldir, stofnið greiðslu fyrir reikninga lánardrottins sem voru stofnaðir sem afleiðing af endurgreiðsluferlinu.</span><span class="sxs-lookup"><span data-stu-id="cdeda-124">In Accounts payable, create a payment for the vendor invoices that were created by the reimbursement process.</span></span> <span data-ttu-id="cdeda-125">Upplýsingar um hvernig greiða á lánardrottnum er að finna í [Yfirlit yfir greiðslu lánardrottins](../accounts-payable/Vendor-payments-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="cdeda-125">For information about how to pay vendors, see [Vendor payment overview](../accounts-payable/Vendor-payments-workspace.md).</span></span>
