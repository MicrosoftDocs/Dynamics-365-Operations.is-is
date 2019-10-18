---
title: Stofna og flytja út greiðslur lánardrottna með ISO20022-greiðslusniði
description: Þetta ferli sýnir hvernig á að stofna greiðslulínur í greiðslubók lánardrottins og mynda greiðsluskrá lánardrottins með því að nota dæmi um ISO2022 millifærsla fjármuna.
author: mrolecki
manager: AnnBe
ms.date: 01/17/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendPaym, SysQueryForm, VendPaymProposalEdit, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b70ad94014587ba8e55735192dbe0ab2e4adf4ee
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185820"
---
# <a name="create-and-export-vendor-payments-using-iso20022-payment-format"></a><span data-ttu-id="04e24-103">Stofna og flytja út greiðslur lánardrottna með ISO20022-greiðslusniði</span><span class="sxs-lookup"><span data-stu-id="04e24-103">Create and export vendor payments using ISO20022 payment format</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="04e24-104">Þetta efnisatriði sýnir hvernig á að stofna greiðslulínur í greiðslubók lánardrottins og mynda greiðsluskrá lánardrottins með því að nota dæmi um ISO2022 millifærsla fjármuna.</span><span class="sxs-lookup"><span data-stu-id="04e24-104">This topic explains how to create payment lines in the vendor payment journal and generate a vendor payment file using ISO2022 Credit transfer example.</span></span>

<span data-ttu-id="04e24-105">Þetta fimmta ferli af fimm sem sýna greiðsluferlinu lánardrottins með því að nota grunnstillingar fyrir rafræna skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="04e24-105">This is the fifth procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="04e24-106">Notaðu DEMF-sýnigögnin til að ljúka þessu dæmi.</span><span class="sxs-lookup"><span data-stu-id="04e24-106">Use the DEMF demo data to complete this example.</span></span>

## <a name="example"></a><span data-ttu-id="04e24-107">Dæmi</span><span class="sxs-lookup"><span data-stu-id="04e24-107">Example</span></span>

1.  <span data-ttu-id="04e24-108">Fara í **Viðskiptaskuldir > Greiðslur > Greiðslubók**.</span><span class="sxs-lookup"><span data-stu-id="04e24-108">Go to **Accounts payable > Payments > Payment journal**.</span></span>
2.  <span data-ttu-id="04e24-109">Smellt er á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="04e24-109">Click **New**.</span></span>
3.  <span data-ttu-id="04e24-110">Sláið inn eða veldu gildi í reitnum **Heiti**.</span><span class="sxs-lookup"><span data-stu-id="04e24-110">In the **Name** field, enter or select a value.</span></span>
4.  <span data-ttu-id="04e24-111">Smelltu á **Línur > Greiðslutillaga > Stofna greiðslutillögu**.</span><span class="sxs-lookup"><span data-stu-id="04e24-111">Click **Lines > Payment proposal > Create payment proposal**.</span></span>
5.  <span data-ttu-id="04e24-112">Útvíkka **Færslur til að taka með** hlutann.</span><span class="sxs-lookup"><span data-stu-id="04e24-112">Expand the **Records to include** section.</span></span>
6.  <span data-ttu-id="04e24-113">Smella á **Sía**.</span><span class="sxs-lookup"><span data-stu-id="04e24-113">Click **Filter**.</span></span>
7.  <span data-ttu-id="04e24-114">Á listanum skal velja línuna fyrir töflu **Lánardrottna** og reitinn fyrir **Lánardrottnalykil**.</span><span class="sxs-lookup"><span data-stu-id="04e24-114">In the list, select the row for **Vendors table** and **Vendor account field**.</span></span>
8.  <span data-ttu-id="04e24-115">Í reitinn **Skilyrði** skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="04e24-115">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="04e24-116">Þú getur notað hvaða skilyrði sem er til að velja lánardrottnafærslur til að greiða, í þessu dæmi notaðu DE-001 sem lánardrottnalykil.</span><span class="sxs-lookup"><span data-stu-id="04e24-116">You can apply any criteria for selecting vendor transactions to pay, for this example, use DE-001 as a vendor account.</span></span>
12. <span data-ttu-id="04e24-117">Smellið á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="04e24-117">Click **OK**.</span></span>
13. <span data-ttu-id="04e24-118">Smellið á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="04e24-118">Click **OK**.</span></span>
14. <span data-ttu-id="04e24-119">Smellt er á **Stofna greiðslur**.</span><span class="sxs-lookup"><span data-stu-id="04e24-119">Click **Create payments**.</span></span>
15. <span data-ttu-id="04e24-120">Mynda ISO20022-greiðsluskrá.</span><span class="sxs-lookup"><span data-stu-id="04e24-120">Generate an ISO20022 payment file.</span></span>
    1.  <span data-ttu-id="04e24-121">Smelltu á **Mynda greiðslur**.</span><span class="sxs-lookup"><span data-stu-id="04e24-121">Click **Generate payments**.</span></span>
    2.  <span data-ttu-id="04e24-122">Færa inn eða velja gildi í reitnum **Greiðsluaðferð**.</span><span class="sxs-lookup"><span data-stu-id="04e24-122">In the **Method of payment** field, enter or select a value.</span></span>
    3.  <span data-ttu-id="04e24-123">Í reitinn **Skráarheiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="04e24-123">In the **File name** field, type a value.</span></span> <span data-ttu-id="04e24-124">Fyrir þetta dæmi, vegna EUR greiðslu, verður myndaða skráin samhæf SEPA.</span><span class="sxs-lookup"><span data-stu-id="04e24-124">For this example, because of the EUR payment, the generated file will be SEPA compliant.</span></span> <span data-ttu-id="04e24-125">Einnig er hægt að nota ISO20022 kreditfærslur ásamt öðrum greiðslusniðum lánardrottins til að búa til greiðslur í öðrum gjaldmiðlum.</span><span class="sxs-lookup"><span data-stu-id="04e24-125">ISO20022 credit transfer as well as other vendor payment formats can also be used for generating payments in other currencies.</span></span>
    4.  <span data-ttu-id="04e24-126">Færa inn eða veljið gildi í svæðinu **Bankareikningur**.</span><span class="sxs-lookup"><span data-stu-id="04e24-126">In the **Bank account** field, enter or select a value.</span></span>

