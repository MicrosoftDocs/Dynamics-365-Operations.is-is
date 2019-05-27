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
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Iceland
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5b693e2c4a36e9aa01d65e06ea17823ab5e9e21c
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537992"
---
# <a name="create-a-vendor-account-and-attach-the-invoice-declaration-category"></a><span data-ttu-id="5ffea-103">Stofna lánardrottnalykil og festa verktakamiða</span><span class="sxs-lookup"><span data-stu-id="5ffea-103">Create a vendor account and attach the invoice declaration category</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5ffea-104">Þetta ferli fer í gegnum stofnun á reikningi lánardrottins með grunnstillingu fyrir verktakamiða.</span><span class="sxs-lookup"><span data-stu-id="5ffea-104">This procedure walks you through creating a vendor with configuration for an invoice declaration.</span></span> <span data-ttu-id="5ffea-105">Sýnigögn fyrirtækisins til að stofna þetta ferli er DEMF með land aðalaðsetur lögaðila uppfært í Ísland.</span><span class="sxs-lookup"><span data-stu-id="5ffea-105">The demo data company used to create this procedure is DEMF with the country of legal entity primary address updated to Iceland.</span></span>


## <a name="create-a-vendor"></a><span data-ttu-id="5ffea-106">Stofna lánardrottinn</span><span class="sxs-lookup"><span data-stu-id="5ffea-106">Create a vendor</span></span>
1. <span data-ttu-id="5ffea-107">Farið í Viðskiptaskuldir > Lánardrottnar > Allir lánardrottnar.</span><span class="sxs-lookup"><span data-stu-id="5ffea-107">Go to Accounts payable > Vendors > All vendors.</span></span>
2. <span data-ttu-id="5ffea-108">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="5ffea-108">Click New.</span></span>
3. <span data-ttu-id="5ffea-109">Í svæðinu Lánardrottnalykill skal slá inn 'IS-001'.</span><span class="sxs-lookup"><span data-stu-id="5ffea-109">In the Vendor account field, type 'IS-001'.</span></span>
4. <span data-ttu-id="5ffea-110">Í reitnum Heiti skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="5ffea-110">In the Name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="5ffea-111">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="5ffea-111">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="5ffea-112">Smellið á Velja.</span><span class="sxs-lookup"><span data-stu-id="5ffea-112">Click Select.</span></span>
7. <span data-ttu-id="5ffea-113">Í reitnum Flokkur skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="5ffea-113">In the Group field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="5ffea-114">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="5ffea-114">In the list, click the link in the selected row.</span></span>

## <a name="set-invoice-declaration-category-for-the-vendor"></a><span data-ttu-id="5ffea-115">Stilla flokk verktakamiða fyrir lánardrottinn</span><span class="sxs-lookup"><span data-stu-id="5ffea-115">Set invoice declaration category for the vendor</span></span>
1. <span data-ttu-id="5ffea-116">Stækka eða fella saman hlutann Reikningur og afhending.</span><span class="sxs-lookup"><span data-stu-id="5ffea-116">Expand or collapse the Invoice and delivery section.</span></span>
2. <span data-ttu-id="5ffea-117">Í reitnum Verktakamiðar skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="5ffea-117">In the Invoice declaration field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="5ffea-118">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="5ffea-118">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="5ffea-119">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="5ffea-119">Click Save.</span></span>

