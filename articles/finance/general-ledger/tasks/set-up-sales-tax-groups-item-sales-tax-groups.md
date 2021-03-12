---
title: Setja upp VSK-flokka og VSK-flokka vöru
description: Þessi verkskráningu fer í gegnum uppsetningu á vsk og VSK-flokkur vöru.
author: twheeloc
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxGroup,  TaxItemGroup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e35f98de715af95b0bec2b2ca5d7e7570aa8fdba
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994491"
---
# <a name="set-up-sales-tax-groups-and-item-sales-tax-groups"></a><span data-ttu-id="831d0-103">Setja upp VSK-flokka og VSK-flokka vöru</span><span class="sxs-lookup"><span data-stu-id="831d0-103">Set up sales tax groups and item sales tax groups</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="831d0-104">Þessi verkskráningu fer í gegnum uppsetningu á vsk og VSK-flokkur vöru.</span><span class="sxs-lookup"><span data-stu-id="831d0-104">This task recording walks you through the setup of Sales tax and Item sales tax groups.</span></span> <span data-ttu-id="831d0-105">Vsk-flokkar eru flokkar vsk-kóðana sem eru tengdir við viðskiptavini og lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="831d0-105">Sales tax groups are groups of sales tax codes that are attached to customers and vendors.</span></span> <span data-ttu-id="831d0-106">Þær eru einnig tengdar fjárhagslyklum fyrir færslurnar sem eru ekki bókaðar á tiltekinn lánardrottin eða viðskiptavin.</span><span class="sxs-lookup"><span data-stu-id="831d0-106">They are also attached to ledger accounts for transactions that are not posted to a particular vendor or customer.</span></span>  <span data-ttu-id="831d0-107">VSK-flokkur vöru eru flokkar vsk-kóðana sem eru tengd tilföng eins og afurðir.</span><span class="sxs-lookup"><span data-stu-id="831d0-107">Item sales tax groups are groups of sales tax codes that are attached to resources like products.</span></span>  <span data-ttu-id="831d0-108">Virðisaukaskattur sem gildir um tiltekna færslu er ákvörðuð af VSK-kóða sem er innifalinn bæði í VSK-flokkur og í VSK-flokkur vöru færslunnar.</span><span class="sxs-lookup"><span data-stu-id="831d0-108">The sales taxes that apply to a particular transaction are determined by the sales tax codes that are included both in the sales tax group and in the item sales tax group of the transaction.</span></span>  <span data-ttu-id="831d0-109">Virðisaukaskattur má reikna aðeins ef VSK-flokkur og VSK-flokkur vöru eru valin fyrir hverja færsla sem virðisaukaskattur þarf að vera reiknaður eða skráður.</span><span class="sxs-lookup"><span data-stu-id="831d0-109">Sales tax can be calculated only if a sales tax group and an item sales tax group are selected for each transaction for which sales tax must be calculated or recorded.</span></span>  

1. <span data-ttu-id="831d0-110">Farðu í **Skoðunarrúða > Kerfiseiningar > Skattur > Óbeinir skattar > Virðisaukaskattur- > Vsk-flokkar**.</span><span class="sxs-lookup"><span data-stu-id="831d0-110">Go to **Navigation pane > Modules > Tax > Indirect taxes > Sales tax > Sales tax groups**.</span></span>
2. <span data-ttu-id="831d0-111">Smellt er á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="831d0-111">Click **New**.</span></span>
3. <span data-ttu-id="831d0-112">Færa inn gildi í svæðinu **VSK-flokkur**.</span><span class="sxs-lookup"><span data-stu-id="831d0-112">In the **Sales tax group** field, type a value.</span></span>
4. <span data-ttu-id="831d0-113">Í reitinn **Lýsing** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="831d0-113">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="831d0-114">Víxla útvíkkun á liðnum **Uppsetning**.</span><span class="sxs-lookup"><span data-stu-id="831d0-114">Toggle the expansion of the **Setup** section.</span></span>
6. <span data-ttu-id="831d0-115">Smelltu á **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="831d0-115">Click **Add**.</span></span>
7. <span data-ttu-id="831d0-116">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="831d0-116">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="831d0-117">Í reitnum **VSK-kóði** skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="831d0-117">In the **Sales tax code** field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="831d0-118">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="831d0-118">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="831d0-119">Smellt er á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="831d0-119">Click **Save**.</span></span>
11. <span data-ttu-id="831d0-120">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="831d0-120">Close the page.</span></span>
12. <span data-ttu-id="831d0-121">Fara í **Skattur > Óbeinir skattar > VSK- > Vsk-flokkar vöru**.</span><span class="sxs-lookup"><span data-stu-id="831d0-121">Go to **Tax > Indirect taxes > Sales tax > Item sales tax groups**.</span></span>
13. <span data-ttu-id="831d0-122">Smellt er á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="831d0-122">Click **New**.</span></span>
14. <span data-ttu-id="831d0-123">Færa inn gildi í reitnum **VSK-flokkur vöru**.</span><span class="sxs-lookup"><span data-stu-id="831d0-123">In the **Item sales tax group** field, type a value.</span></span>
15. <span data-ttu-id="831d0-124">Í reitinn **Lýsing** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="831d0-124">In the **Description** field, type a value.</span></span>
16. <span data-ttu-id="831d0-125">Smelltu á **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="831d0-125">Click **Add**.</span></span>
17. <span data-ttu-id="831d0-126">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="831d0-126">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="831d0-127">Í reitnum **VSK-kóði** skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="831d0-127">In the **Sales tax code** field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="831d0-128">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="831d0-128">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="831d0-129">Smellt er á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="831d0-129">Click **Save**.</span></span>

