---
title: Setja upp lánardrottna og bankareikninga lánardrottna fyrir ISO20022-tmillifærslur
description: Þetta ferli sýnir hvernig á að setja upp lánardrottins og bankareikningsupplýsingar fyrir lánardrottinn sem þarf fyrir myndun ISO20022-greiðsluskrár fyrir millifærsla fjármuna eða hvers kyns aðra greiðsluskrá lánardrottins.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ab8c52b9b457505c2cf2bfca46cb938e73c0142e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174907"
---
# <a name="set-up-vendors-and-vendor-bank-accounts-for-iso20022-credit-transfers"></a><span data-ttu-id="28a7e-103">Setja upp lánardrottna og bankareikninga lánardrottna fyrir ISO20022-tmillifærslur</span><span class="sxs-lookup"><span data-stu-id="28a7e-103">Set up vendors and vendor bank accounts for ISO20022 credit transfers</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="28a7e-104">Þetta ferli sýnir hvernig á að setja upp lánardrottins og bankareikningsupplýsingar fyrir lánardrottinn sem þarf fyrir myndun ISO20022-greiðsluskrár fyrir millifærsla fjármuna eða hvers kyns aðra greiðsluskrá lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="28a7e-104">This procedure demonstrates how to set up the vendor and vendor specific bank account information required for ISO20022 Credit transfer or any other vendor payment file generation.</span></span> 

<span data-ttu-id="28a7e-105">Sýnigögn fyrirtækisins til að stofna þetta ferli er DEMF.</span><span class="sxs-lookup"><span data-stu-id="28a7e-105">The demo data company used to create this procedure is DEMF.</span></span>
<span data-ttu-id="28a7e-106">Þetta fjórða ferli af fimm sem sýna greiðsluferlinu lánardrottins með því að nota grunnstillingar fyrir rafræna skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="28a7e-106">This is the fourth procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="28a7e-107">Þetta ferli er fyrir eiginleika sem var bætt við í Dynamics 365 for Operations, útgáfu 1611.</span><span class="sxs-lookup"><span data-stu-id="28a7e-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="set-up-bank-details"></a><span data-ttu-id="28a7e-108">Setja upp upplýsingar um banka</span><span class="sxs-lookup"><span data-stu-id="28a7e-108">Set up bank details</span></span>
1. <span data-ttu-id="28a7e-109">Farið í Viðskiptaskuldir > Lánardrottnar > Allir lánardrottnar.</span><span class="sxs-lookup"><span data-stu-id="28a7e-109">Go to Accounts payable > Vendors > All vendors.</span></span>
2. <span data-ttu-id="28a7e-110">Nota flýtiafmörkun til að finna færslur</span><span class="sxs-lookup"><span data-stu-id="28a7e-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="28a7e-111">Til dæmis, sía svæðið Lánardrottins með gildið 'DE-001'.</span><span class="sxs-lookup"><span data-stu-id="28a7e-111">For example, filter on the Vendor account field with a value of 'DE-001'.</span></span>
3. <span data-ttu-id="28a7e-112">Smellt er á DE-001 til að opna upplýsingar um lánardrottin.</span><span class="sxs-lookup"><span data-stu-id="28a7e-112">Click DE-001 to open vendor details.</span></span>
4. <span data-ttu-id="28a7e-113">Í aðgerðasvæðinu er smellt á lánardrottinn.</span><span class="sxs-lookup"><span data-stu-id="28a7e-113">On the Action Pane, click Vendor.</span></span>
5. <span data-ttu-id="28a7e-114">Smellt er á bankareikninga.</span><span class="sxs-lookup"><span data-stu-id="28a7e-114">Click Bank accounts.</span></span>
6. <span data-ttu-id="28a7e-115">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="28a7e-115">Click Edit.</span></span>
    * <span data-ttu-id="28a7e-116">Ef engin bankareikningurinn er tiltækur, þarf að stofna nýja.</span><span class="sxs-lookup"><span data-stu-id="28a7e-116">If there is no bank account available, you need to create a new one.</span></span>  
7. <span data-ttu-id="28a7e-117">Í svæðinu swift-kóði færðu inn 'COBADEFFXXX' .</span><span class="sxs-lookup"><span data-stu-id="28a7e-117">In the SWIFT code field, type 'COBADEFFXXX'.</span></span>
8. <span data-ttu-id="28a7e-118">Í reitinn IBAN skal slá inn 'DE36200400000628808808'.</span><span class="sxs-lookup"><span data-stu-id="28a7e-118">In the IBAN field, type 'DE36200400000628808808'.</span></span>
9. <span data-ttu-id="28a7e-119">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="28a7e-119">Close the page.</span></span>

## <a name="set-up-a-method-of-payment-for-the-vendor"></a><span data-ttu-id="28a7e-120">Setja upp greiðsluhátt fyrir lánardrottinn</span><span class="sxs-lookup"><span data-stu-id="28a7e-120">Set up a method of payment for the vendor</span></span>
1. <span data-ttu-id="28a7e-121">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="28a7e-121">Click Edit.</span></span>
2. <span data-ttu-id="28a7e-122">Stækka eða fella saman hlutann Greiðsla.</span><span class="sxs-lookup"><span data-stu-id="28a7e-122">Expand or collapse the Payment section.</span></span>
3. <span data-ttu-id="28a7e-123">Í reitnum greiðsluaðferð skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="28a7e-123">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="28a7e-124">Í listanum skal smella á tengilinn í SEPA CT línu.</span><span class="sxs-lookup"><span data-stu-id="28a7e-124">In the list, click the link in the SEPA CT row.</span></span>
5. <span data-ttu-id="28a7e-125">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="28a7e-125">Click Save.</span></span>

