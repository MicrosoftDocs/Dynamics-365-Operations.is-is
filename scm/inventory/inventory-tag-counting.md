---
title: "Birgðamerkjatalning"
description: "Þessari grein veitir upplýsingar um birgðamerkjatalningu, sem þú notar til að bera saman rauninnihald vöruhúss við lagerbirgðir."
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventJournalCount, InventJournalCountTag
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 11594
ms.assetid: 03772d0e-5c37-454c-ab85-82bc8b60a76d
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 0e7f66cccd76e5326fce75d1a13aff294c16fb9b
ms.openlocfilehash: 9e129fda638cfd8cff0e40079747f7ca70fa7531
ms.contentlocale: is-is
ms.lasthandoff: 09/12/2017

---

# <a name="inventory-tag-counting"></a><span data-ttu-id="072c4-103">Birgðamerkjatalning</span><span class="sxs-lookup"><span data-stu-id="072c4-103">Inventory tag counting</span></span>

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]


<span data-ttu-id="072c4-104">Þessari grein veitir upplýsingar um birgðamerkjatalningu, sem þú notar til að bera saman rauninnihald vöruhúss við lagerbirgðir.</span><span class="sxs-lookup"><span data-stu-id="072c4-104">This article provides information about tag counting, which you use to compare the actual contents of a warehouse with the on-hand inventory.</span></span>

<span data-ttu-id="072c4-105">Með því að stofna línur á **Merkjatalning** síðunni er sett merkjanúmer á hverja birgðavöru t.d. númer frá 1 upp í 500.</span><span class="sxs-lookup"><span data-stu-id="072c4-105">By creating lines on the **Tag counting** page, you place a tag number on each inventory item, such as a number from 1 to 500.</span></span> <span data-ttu-id="072c4-106">Meðan á talningu stendur eru°færð inn vörunúmer og magn á tilheyrandi merki.</span><span class="sxs-lookup"><span data-stu-id="072c4-106">During the count, you enter the item number and the quantity on a corresponding tag.</span></span> <span data-ttu-id="072c4-107">Síðan er hægt að nota þetta merki sem grunn fyrir innlegg í merkjatalningarbók.</span><span class="sxs-lookup"><span data-stu-id="072c4-107">This tag can then be used as the basis for input in the tag counting journal.</span></span> <span data-ttu-id="072c4-108">Þegar merkjatalningarbók er bókuð er ný talningarbók stofnuð á síðunni **Talning**.</span><span class="sxs-lookup"><span data-stu-id="072c4-108">After you post the tag counting journal, a new counting journal is created on the **Counting** page.</span></span> <span data-ttu-id="072c4-109">Ný færslubók er byggt á merkjatalningu í færslubókarlínum sem voru stofnaðar.</span><span class="sxs-lookup"><span data-stu-id="072c4-109">The new journal is based on the tag counting journal lines that you created.</span></span> <span data-ttu-id="072c4-110">Til að framkvæma merkjatalningu á vörum eftir tiltekinni birgðavídd, veljið víddina á°**Birta vídd**°síðunni sem birtist þegar merkjatalningarbókin er stofnuð.</span><span class="sxs-lookup"><span data-stu-id="072c4-110">To tag-count items by a specific inventory dimension, select the dimension on the **Display dimension** page that is displayed when you create the tag counting journal.</span></span> <span data-ttu-id="072c4-111">Til dæmis, til að telja vörur í ákveðnu vöruhúsi, veljið gátreitinn **Vöruhús**.</span><span class="sxs-lookup"><span data-stu-id="072c4-111">For example, to count items in a specific warehouse, select the **Warehouse** check box.</span></span> <span data-ttu-id="072c4-112">Ef sleðinn°**Læsa vörum meðan á talningu stendur** á°síðunni **Birgða- og vöruhúsastjórnunar færibreytur** er valinn er ekki hægt að uppfæra vörur efnislega meðan á talningu stendur.</span><span class="sxs-lookup"><span data-stu-id="072c4-112">If the **Lock items during count** slider on the **Inventory and warehouse management parameters** page is selected, items can't be physically updated during counting.</span></span> <span data-ttu-id="072c4-113">Hins vegar eru vörur í merkjatalningarbókum ekki læstar meðan á talningu stendur.</span><span class="sxs-lookup"><span data-stu-id="072c4-113">However, items in tag counting journals aren't locked during counting.</span></span> <span data-ttu-id="072c4-114">Birgðafærslur eru ekki stofnaðar þar til merkjatalningarlínur eru bókaðar og fluttar í talningarbók.</span><span class="sxs-lookup"><span data-stu-id="072c4-114">Inventory transactions aren't created until the tag counting lines are posted and transferred to a counting journal.</span></span> <span data-ttu-id="072c4-115">Ef seðlar eru færðir inn af handahófi og óskað er eftir að skilgreina merki sem vantar, er smellt á dálkhausinn **Merki** til að raða línum eftir merki.</span><span class="sxs-lookup"><span data-stu-id="072c4-115">If tags are entered randomly, and you want to identify missing tags, click the **Tag** column header to sort the lines by tag.</span></span>

<a name="see-also"></a><span data-ttu-id="072c4-116">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="072c4-116">See also</span></span>
--------

[<span data-ttu-id="072c4-117">Regluleg talning</span><span class="sxs-lookup"><span data-stu-id="072c4-117">Cycle counting</span></span>](../warehousing/cycle-counting.md)

