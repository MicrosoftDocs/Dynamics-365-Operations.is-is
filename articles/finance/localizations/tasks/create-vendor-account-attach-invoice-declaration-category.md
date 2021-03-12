---
title: Stofna lánardrottnalykil og festa verktakamiða
description: Þetta ferli fer í gegnum stofnun á reikningi lánardrottins með grunnstillingu fyrir verktakamiða.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, DirPartyLookup
audience: Application User
ms.reviewer: kfend
ms.search.region: Iceland
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: beeccef06b7de6c07b58da4137af224cdd262822
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4984875"
---
# <a name="create-a-vendor-account-and-attach-the-invoice-declaration-category"></a><span data-ttu-id="02e6e-103">Stofna lánardrottnalykil og festa verktakamiða</span><span class="sxs-lookup"><span data-stu-id="02e6e-103">Create a vendor account and attach the invoice declaration category</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="02e6e-104">Þetta ferli fer í gegnum stofnun á reikningi lánardrottins með grunnstillingu fyrir verktakamiða.</span><span class="sxs-lookup"><span data-stu-id="02e6e-104">This procedure walks you through creating a vendor with configuration for an invoice declaration.</span></span> <span data-ttu-id="02e6e-105">Sýnigögn fyrirtækisins til að stofna þetta ferli er DEMF með land aðalaðsetur lögaðila uppfært í Ísland.</span><span class="sxs-lookup"><span data-stu-id="02e6e-105">The demo data company used to create this procedure is DEMF with the country of legal entity primary address updated to Iceland.</span></span>


## <a name="create-a-vendor"></a><span data-ttu-id="02e6e-106">Stofna lánardrottinn</span><span class="sxs-lookup"><span data-stu-id="02e6e-106">Create a vendor</span></span>
1. <span data-ttu-id="02e6e-107">Farið í Viðskiptaskuldir > Lánardrottnar > Allir lánardrottnar.</span><span class="sxs-lookup"><span data-stu-id="02e6e-107">Go to Accounts payable > Vendors > All vendors.</span></span>
2. <span data-ttu-id="02e6e-108">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="02e6e-108">Click New.</span></span>
3. <span data-ttu-id="02e6e-109">Í svæðinu Lánardrottnalykill skal slá inn 'IS-001'.</span><span class="sxs-lookup"><span data-stu-id="02e6e-109">In the Vendor account field, type 'IS-001'.</span></span>
4. <span data-ttu-id="02e6e-110">Í reitnum Heiti skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="02e6e-110">In the Name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="02e6e-111">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="02e6e-111">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="02e6e-112">Smellið á Velja.</span><span class="sxs-lookup"><span data-stu-id="02e6e-112">Click Select.</span></span>
7. <span data-ttu-id="02e6e-113">Í reitnum Flokkur skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="02e6e-113">In the Group field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="02e6e-114">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="02e6e-114">In the list, click the link in the selected row.</span></span>

## <a name="set-invoice-declaration-category-for-the-vendor"></a><span data-ttu-id="02e6e-115">Stilla flokk verktakamiða fyrir lánardrottinn</span><span class="sxs-lookup"><span data-stu-id="02e6e-115">Set invoice declaration category for the vendor</span></span>
1. <span data-ttu-id="02e6e-116">Stækka eða fella saman hlutann Reikningur og afhending.</span><span class="sxs-lookup"><span data-stu-id="02e6e-116">Expand or collapse the Invoice and delivery section.</span></span>
2. <span data-ttu-id="02e6e-117">Í reitnum Verktakamiðar skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="02e6e-117">In the Invoice declaration field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="02e6e-118">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="02e6e-118">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="02e6e-119">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="02e6e-119">Click Save.</span></span>

