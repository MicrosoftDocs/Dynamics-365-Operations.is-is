---
title: Endurgreiða viðskiptavini
description: Í þessu grein útskýrt hvernig stofna endurgreiðslufærslurnar fyrir flokk af viðskiptavinum. Ef viðskiptavinur hefur kreditstöðu er hægt er að endurgreiða viðskiptavininum upphæð stöðunnar.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransCustPaym, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14191
ms.assetid: 53533ee3-470e-458a-ac8b-3815aa4cb502
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 97982dec140ed440682ae507f40557670ebccd3e
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836635"
---
# <a name="reimburse-customers"></a><span data-ttu-id="0a139-104">Endurgreiða viðskiptavini</span><span class="sxs-lookup"><span data-stu-id="0a139-104">Reimburse customers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0a139-105">Í þessu grein útskýrt hvernig stofna endurgreiðslufærslurnar fyrir flokk af viðskiptavinum.</span><span class="sxs-lookup"><span data-stu-id="0a139-105">This article explains how to create reimbursement transactions for a group of customers.</span></span> <span data-ttu-id="0a139-106">Ef viðskiptavinur hefur kreditstöðu er hægt er að endurgreiða viðskiptavininum upphæð stöðunnar.</span><span class="sxs-lookup"><span data-stu-id="0a139-106">If a customer has a credit balance, you can reimburse the customer for the amount of the balance.</span></span> 

<span data-ttu-id="0a139-107">Eftirfarandi tafla sýnir forkröfur sem verður að vera til staðar áður en byrjað er.</span><span class="sxs-lookup"><span data-stu-id="0a139-107">The following table shows the prerequisites that must be in place before you start.</span></span>

| <span data-ttu-id="0a139-108">Skilyrði</span><span class="sxs-lookup"><span data-stu-id="0a139-108">Prerequisite</span></span>                                                            | <span data-ttu-id="0a139-109">Lýsing</span><span class="sxs-lookup"><span data-stu-id="0a139-109">Description</span></span>                                                                                                                                                                                 |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a139-110">Tilgreina lágmarks endurgreiðsluupphæð fyrir lögaðilann</span><span class="sxs-lookup"><span data-stu-id="0a139-110">Specify the minimum reimbursement amount for the legal entity.</span></span>          | <span data-ttu-id="0a139-111">Á **Færibreytur viðskiptakrafna** síðunni, á svæðinu **Almennt** á **Lágmarks endurgreiðsla** svæðinu, færið inn lágmarksupphæð sem hægt er að endurgreiða fyrir°ofgreiðslu viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="0a139-111">On the **Accounts receivable parameters** page, in the **General** area, in the **Minimum reimbursement** field, enter the minimum amount that can be reimbursed for customer overpayments.</span></span> |
| <span data-ttu-id="0a139-112">Valfrjálst: Bæta lánardrottnareikningi við hvern viðskiptavin sem er hægt að endurgreiða.</span><span class="sxs-lookup"><span data-stu-id="0a139-112">Optional: Add a vendor account to each customer that can be reimbursed.</span></span> | <span data-ttu-id="0a139-113">Á°síðunni **Viðskiptavinir** í flýtiflipanum **Ýmsar upplýsingar** á svæðinu **Lánardrottnalykill** skal°velja lánardrottnalykilinn fyrir viðskiptavin.</span><span class="sxs-lookup"><span data-stu-id="0a139-113">On the **Customers** page, on the **Miscellaneous details** FastTab, in the **Vendor account** field, select the vendor account for the customer.</span></span>                                           |

<span data-ttu-id="0a139-114">Þegar endurgreiðslufærslur eru stofnaðar, er reikningur lánardrottins stofnaður fyrir upphæð kreditstöðunnar.</span><span class="sxs-lookup"><span data-stu-id="0a139-114">When you create reimbursement transactions, a vendor invoice is created for the amount of the credit balance.</span></span> <span data-ttu-id="0a139-115">Endurgreiðsluferlið°fjarlægir kreditstöðu fyrir viðskiptavinalykilinn og stofnar stöðu greiðslu fyrir lykil lánardrottins sem samsvarar viðskiptavininum.</span><span class="sxs-lookup"><span data-stu-id="0a139-115">The reimbursement process removes the credit balance for the customer account and creates a balance due for the vendor account that corresponds to the customer.</span></span>

1.  <span data-ttu-id="0a139-116">Í Viðskiptakröfur, keyrið ferlið **Endurgreiðsla**.</span><span class="sxs-lookup"><span data-stu-id="0a139-116">In Accounts receivable, run the **Reimbursement** process.</span></span>
2.  <span data-ttu-id="0a139-117">Fylgið einu af eftirfarandi skrefum:</span><span class="sxs-lookup"><span data-stu-id="0a139-117">Follow one of these steps:</span></span>
    -   <span data-ttu-id="0a139-118">Til þess að endurgreiða tilteknum viðskiptavini er smellt á **Velja** og reikningar viðskiptavina tilgreindir í fyrirspurn.</span><span class="sxs-lookup"><span data-stu-id="0a139-118">To reimburse specific customer accounts, click **Select**, and specify the customer accounts in the query.</span></span>
    -   <span data-ttu-id="0a139-119">Til þess að endurgreiða öllum viðskiptavinum er smellt á **OK**.</span><span class="sxs-lookup"><span data-stu-id="0a139-119">To reimburse all customer accounts, click **OK**.</span></span>

    <span data-ttu-id="0a139-120">Kreditupphæðir eru fluttar í lánardrottnarlykla viðskiptavinar og eru unnar eins og venjulegar greiðslur.</span><span class="sxs-lookup"><span data-stu-id="0a139-120">The credit amounts are transferred to the vendor accounts of the customers and are processed as ordinary payments.</span></span> <span data-ttu-id="0a139-121">Ef viðskiptamaður er ekki með lánardrottnarlykil er sjálfkrafa búið til númer einsskiptislánardrottins handa viðskiptamanninum.</span><span class="sxs-lookup"><span data-stu-id="0a139-121">If a customer doesn't have a vendor account, a one-time vendor account is automatically created for the customer.</span></span>
3.  <span data-ttu-id="0a139-122">Til að skoða færslur endurgreiðslna sem voru stofnaðar, notið síðuna **Endurgreiðslur**.</span><span class="sxs-lookup"><span data-stu-id="0a139-122">To view the reimbursement transactions that were created, use the **Reimbursement** page.</span></span>
4.  <span data-ttu-id="0a139-123">Í Viðskiptaskuldir, stofnið greiðslu fyrir reikninga lánardrottins sem voru stofnaðir sem afleiðing af endurgreiðsluferlinu.</span><span class="sxs-lookup"><span data-stu-id="0a139-123">In Accounts payable, create a payment for the vendor invoices that were created by the reimbursement process.</span></span>




