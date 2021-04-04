---
title: Stigveldi verslunar
description: Þessi grein lýsir stigveldi í Dynamics 365 Commerce.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: OMHierarchyManager, EcoResCategoryHierarchyFactbox
audience: Application User
ms.reviewer: josaw
ms.custom: 15851
ms.assetid: dfa11d41-2a0c-4cde-99b6-058c49176c94
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: a2cc766b0fd358d82187a5c0368005896fbb7769
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5251378"
---
# <a name="commerce-hierarchies"></a><span data-ttu-id="f547d-103">Stigveldi verslunar</span><span class="sxs-lookup"><span data-stu-id="f547d-103">Commerce hierarchies</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f547d-104">Þessi grein lýsir stigveldi í Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f547d-104">This article describes hierarchies in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="f547d-105">Hægt er að stofna tegundastigveldi til að skipuleggja afurðirnar sem seldar eru í gegnum rásir.</span><span class="sxs-lookup"><span data-stu-id="f547d-105">You can create a category hierarchy to organize the products that you sell through your channels.</span></span> <span data-ttu-id="f547d-106">Hægt er að nota stigveldi afurðar til að flokka eða flokka afurðir.</span><span class="sxs-lookup"><span data-stu-id="f547d-106">You can use product hierarchies to categorize or group products.</span></span> <span data-ttu-id="f547d-107">Síðan er hægt að nota þessar afurðir til að stofna afurðaúrval og vildarkerfi viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="f547d-107">You can then use these products to create product assortments and customer loyalty programs.</span></span> <span data-ttu-id="f547d-108">Einnig er hægt úthluta afurðareigindum og eiginleikum, úthluta uppbyggingu verðlagningar, taka með afurðir í kynningartilboð afurða og nota afurðir fyrir skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="f547d-108">You can also assign product attributes and properties, assign a pricing structure, include the products in product promotions, and use the products for reporting.</span></span> <span data-ttu-id="f547d-109">Hægt er að stofna eitt tegundastigveldi til að tákna allar afurðirnir og tegundir í fyrirtækjasamstæðunni, og nota síðan tegundastigveldi fyrir marga.</span><span class="sxs-lookup"><span data-stu-id="f547d-109">You can create one category hierarchy to represent all the products and categories in your organization, and then use that category hierarchy for multiple purposes.</span></span> <span data-ttu-id="f547d-110">Einnig er hægt að stofna mörg tegundastigveldi í sérstökum tilgangi, t. d. til kynningar á afurð.</span><span class="sxs-lookup"><span data-stu-id="f547d-110">Alternatively, you can create multiple category hierarchies for special purposes, such as product promotions.</span></span> <span data-ttu-id="f547d-111">Þegar stofnað er stigveldi afurða verður að úthluta tegundastigveldisgerð til að auðkenna tilgang tegundastigveldisins.</span><span class="sxs-lookup"><span data-stu-id="f547d-111">When you create a product hierarchy, you must assign a category hierarchy type to identify the purpose of the category hierarchy.</span></span> <span data-ttu-id="f547d-112">Til dæmis er aðeins vísað í afurðastigveldi sem er úthlutað á **Yfirlitsstigveldi Commerce** þegar flett er í afurðum eftir tegund á netinu eða á sölustað (POS).</span><span class="sxs-lookup"><span data-stu-id="f547d-112">For example, only product hierarchies that are assigned the **Commerce navigation hierarchy** type are referenced when you browse products by category online or in point of sale (POS).</span></span>

## <a name="hierarchy-types"></a><span data-ttu-id="f547d-113">Gerðir stigveldis</span><span class="sxs-lookup"><span data-stu-id="f547d-113">Hierarchy types</span></span>

<span data-ttu-id="f547d-114">Eftirfarandi tafla sýnir þær gerðir tegundastigvelda sem eru tiltækar og almennan tilgang hverrar gerðar.</span><span class="sxs-lookup"><span data-stu-id="f547d-114">The following table lists the types of category hierarchies that are available and the general purpose of each type.</span></span>

| <span data-ttu-id="f547d-115">Gerð tegundastigveldis</span><span class="sxs-lookup"><span data-stu-id="f547d-115">Category hierarchy type</span></span>       | <span data-ttu-id="f547d-116">Málefni</span><span class="sxs-lookup"><span data-stu-id="f547d-116">Purpose</span></span> |
|-------------------------------|---------|
| <span data-ttu-id="f547d-117">Afurðarstigveldi</span><span class="sxs-lookup"><span data-stu-id="f547d-117">Product hierarchy</span></span>      | <span data-ttu-id="f547d-118">Veljið þessa stigveldisgerð til að skilgreina aðalstigveldi smásöluafurða fyrir fyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="f547d-118">Use this hierarchy type to define the overall product hierarchy for your organization.</span></span> <span data-ttu-id="f547d-119">Hægt er að nota þessa gerð stigveldis fyrir smásölu, verðlagningu og kynningartilboð, skýrslugerð og skipulagningu úrvals.</span><span class="sxs-lookup"><span data-stu-id="f547d-119">You can use this hierarchy type for merchandising, pricing and promotions, reporting, and assortment planning.</span></span> <span data-ttu-id="f547d-120">Aðeins er hægt að úthluta einu stigveldi afurða þessu stigveldi.</span><span class="sxs-lookup"><span data-stu-id="f547d-120">Only one product hierarchy can be assigned this hierarchy type.</span></span> |
| <span data-ttu-id="f547d-121">Viðbótarstigveldi</span><span class="sxs-lookup"><span data-stu-id="f547d-121">Supplemental hierarchy</span></span> | <span data-ttu-id="f547d-122">Notið þessa gerð stigveldis fyrir allar frekari tegundir stigveldis sem á að stofna.</span><span class="sxs-lookup"><span data-stu-id="f547d-122">Use this hierarchy type for any additional category hierarchies that you want to create.</span></span> <span data-ttu-id="f547d-123">Til dæmis á vorin þarf kynningartilboð fyrir sundföt.</span><span class="sxs-lookup"><span data-stu-id="f547d-123">For example, in the spring, you have a promotion for swimwear.</span></span> <span data-ttu-id="f547d-124">Þess vegna hefurðu sundfataafurðirnar í aðskildu tegundastigveldi og beita verðlagningu kynningartilboðs á mismunandi tegundir afurða.</span><span class="sxs-lookup"><span data-stu-id="f547d-124">Therefore, you include your swimwear products in a separate category hierarchy and apply the promotional pricing to the various product categories.</span></span> |
| <span data-ttu-id="f547d-125">Valmyndarstigveldi</span><span class="sxs-lookup"><span data-stu-id="f547d-125">Navigation hierarchy</span></span>   | <span data-ttu-id="f547d-126">Notið þessa gerð stigveldis til að flokka og raða afurðum í tegundum svo að hægt sé að skoða afurðir á netinu eða á söllustað.</span><span class="sxs-lookup"><span data-stu-id="f547d-126">Use this hierarchy type to group and organize products into categories so that the products can be browsed online or in POS.</span></span> |

<span data-ttu-id="f547d-127">Með tegundastigveldi til að skipuleggja vörur er hægt að setja upp og viðhalda afurðareigindum og eiginleikum tegundastigs.</span><span class="sxs-lookup"><span data-stu-id="f547d-127">By using a category hierarchy to structure your products, you can set up and maintain product attributes and properties at the category level.</span></span> <span data-ttu-id="f547d-128">Þessi eigindir og eiginleikar hafa stillingar fyrir afurðavíddir og stillingar á Sölustað.</span><span class="sxs-lookup"><span data-stu-id="f547d-128">These attributes and properties include settings for product dimensions and POS settings.</span></span> <span data-ttu-id="f547d-129">Allar afurðir sem er úthlutað á tegundirnar erfa sjálfkrafa þær eigindir og eiginleika sem eru skilgreindir.</span><span class="sxs-lookup"><span data-stu-id="f547d-129">Any products that you assign to the categories automatically inherit the attributes and properties that you define.</span></span> <span data-ttu-id="f547d-130">Einnig er hægt að afrita stillingar eiginleika fyrir afurðir í margar afurðir í valinni tegund á sama tíma.</span><span class="sxs-lookup"><span data-stu-id="f547d-130">You can also copy the property settings for any product to multiple products in a selected category at the same time.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]