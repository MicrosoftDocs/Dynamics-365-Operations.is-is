---
title: Setja upp VSK-flokka og VSK-flokka vöru
description: Þessi verkskráningu fer í gegnum uppsetningu á vsk og VSK-flokkur vöru.
author: twheeloc
manager: AnnBe
ms.date: 07-01-2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxGroup,  TaxItemGroup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 12bbeaa4e0e2f6ee4874cf72863624a871ba87ea
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175471"
---
# <a name="set-up-sales-tax-groups-and-item-sales-tax-groups"></a><span data-ttu-id="d4538-103">Setja upp VSK-flokka og VSK-flokka vöru</span><span class="sxs-lookup"><span data-stu-id="d4538-103">Set up sales tax groups and item sales tax groups</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d4538-104">Þessi verkskráningu fer í gegnum uppsetningu á vsk og VSK-flokkur vöru.</span><span class="sxs-lookup"><span data-stu-id="d4538-104">This task recording walks you through the setup of Sales tax and Item sales tax groups.</span></span> <span data-ttu-id="d4538-105">Vsk-flokkar eru flokkar vsk-kóðana sem eru tengdir við viðskiptavini og lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="d4538-105">Sales tax groups are groups of sales tax codes that are attached to customers and vendors.</span></span> <span data-ttu-id="d4538-106">Þær eru einnig tengdar fjárhagslyklum fyrir færslurnar sem eru ekki bókaðar á tiltekinn lánardrottin eða viðskiptavin.</span><span class="sxs-lookup"><span data-stu-id="d4538-106">They are also attached to ledger accounts for transactions that are not posted to a particular vendor or customer.</span></span>  <span data-ttu-id="d4538-107">VSK-flokkur vöru eru flokkar vsk-kóðana sem eru tengd tilföng eins og afurðir.</span><span class="sxs-lookup"><span data-stu-id="d4538-107">Item sales tax groups are groups of sales tax codes that are attached to resources like products.</span></span>  <span data-ttu-id="d4538-108">Virðisaukaskattur sem gildir um tiltekna færslu er ákvörðuð af VSK-kóða sem er innifalinn bæði í VSK-flokkur og í VSK-flokkur vöru færslunnar.</span><span class="sxs-lookup"><span data-stu-id="d4538-108">The sales taxes that apply to a particular transaction are determined by the sales tax codes that are included both in the sales tax group and in the item sales tax group of the transaction.</span></span>  <span data-ttu-id="d4538-109">Virðisaukaskattur má reikna aðeins ef VSK-flokkur og VSK-flokkur vöru eru valin fyrir hverja færsla sem virðisaukaskattur þarf að vera reiknaður eða skráður.</span><span class="sxs-lookup"><span data-stu-id="d4538-109">Sales tax can be calculated only if a sales tax group and an item sales tax group are selected for each transaction for which sales tax must be calculated or recorded.</span></span>  

1. <span data-ttu-id="d4538-110">Farðu í **Skoðunarrúða > Kerfiseiningar > Skattur > Óbeinir skattar > Virðisaukaskattur- > Vsk-flokkar**.</span><span class="sxs-lookup"><span data-stu-id="d4538-110">Go to **Navigation pane > Modules > Tax > Indirect taxes > Sales tax > Sales tax groups**.</span></span>
2. <span data-ttu-id="d4538-111">Smellt er á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="d4538-111">Click **New**.</span></span>
3. <span data-ttu-id="d4538-112">Færa inn gildi í svæðinu **VSK-flokkur**.</span><span class="sxs-lookup"><span data-stu-id="d4538-112">In the **Sales tax group** field, type a value.</span></span>
4. <span data-ttu-id="d4538-113">Í reitinn **Lýsing** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="d4538-113">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="d4538-114">Víxla útvíkkun á liðnum **Uppsetning**.</span><span class="sxs-lookup"><span data-stu-id="d4538-114">Toggle the expansion of the **Setup** section.</span></span>
6. <span data-ttu-id="d4538-115">Smelltu á **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="d4538-115">Click **Add**.</span></span>
7. <span data-ttu-id="d4538-116">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="d4538-116">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="d4538-117">Í reitnum **VSK-kóði** skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="d4538-117">In the **Sales tax code** field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="d4538-118">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="d4538-118">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="d4538-119">Smellt er á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="d4538-119">Click **Save**.</span></span>
11. <span data-ttu-id="d4538-120">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="d4538-120">Close the page.</span></span>
12. <span data-ttu-id="d4538-121">Fara í **Skattur > Óbeinir skattar > VSK- > Vsk-flokkar vöru**.</span><span class="sxs-lookup"><span data-stu-id="d4538-121">Go to **Tax > Indirect taxes > Sales tax > Item sales tax groups**.</span></span>
13. <span data-ttu-id="d4538-122">Smellt er á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="d4538-122">Click **New**.</span></span>
14. <span data-ttu-id="d4538-123">Færa inn gildi í reitnum **VSK-flokkur vöru**.</span><span class="sxs-lookup"><span data-stu-id="d4538-123">In the **Item sales tax group** field, type a value.</span></span>
15. <span data-ttu-id="d4538-124">Í reitinn **Lýsing** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="d4538-124">In the **Description** field, type a value.</span></span>
16. <span data-ttu-id="d4538-125">Smelltu á **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="d4538-125">Click **Add**.</span></span>
17. <span data-ttu-id="d4538-126">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="d4538-126">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="d4538-127">Í reitnum **VSK-kóði** skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="d4538-127">In the **Sales tax code** field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="d4538-128">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="d4538-128">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="d4538-129">Smellt er á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="d4538-129">Click **Save**.</span></span>
