---
title: "Smásölustigveldi"
description: "Þessi grein lýsir smásölustigveldi í Microsoft Dynamics 365 for Retail."
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 15851
ms.assetid: dfa11d41-2a0c-4cde-99b6-058c49176c94
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 817696566473bc5f31a7ff11c04291351dfd4764
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---

# <a name="retail-hierarchies"></a><span data-ttu-id="42e5f-103">Smásölustigveldi</span><span class="sxs-lookup"><span data-stu-id="42e5f-103">Retail hierarchies</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="42e5f-104">Þessi grein lýsir smásölustigveldi í Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="42e5f-104">This article describes retail hierarchies in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="42e5f-105">Hægt er að stofna smásöluflokkastigveldi til að skipuleggja afurðirnar sem seldar eru í gegnum smásölurásir.</span><span class="sxs-lookup"><span data-stu-id="42e5f-105">You can create a retail category hierarchy to organize the products that you sell through your retail channels.</span></span> <span data-ttu-id="42e5f-106">Hægt er að nota smásölustigveldi afurðar til að flokka eða flokka afurðir.</span><span class="sxs-lookup"><span data-stu-id="42e5f-106">You can use retail product hierarchies to categorize or group products.</span></span> <span data-ttu-id="42e5f-107">Síðan er hægt að nota þessar afurðir til að stofna afurðaúrval og vildarkerfi viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="42e5f-107">You can then use these products to create product assortments and customer loyalty programs.</span></span> <span data-ttu-id="42e5f-108">Einnig er hægt úthluta afurðareigindum og eiginleikum, úthluta uppbyggingu verðlagningar, taka með afurðir í kynningartilboð afurða og nota afurðir fyrir skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="42e5f-108">You can also assign product attributes and properties, assign a pricing structure, include the products in product promotions, and use the products for reporting.</span></span> <span data-ttu-id="42e5f-109">Hægt er að stofna eitt tegundastigveldi til að tákna allar afurðir og tegundir í fyrirtækjasamstæðunni, og nota síðan tegundastigveldi fyrir margan tilgang.</span><span class="sxs-lookup"><span data-stu-id="42e5f-109">You can create one retail category hierarchy to represent all the products and categories in your organization, and then use that category hierarchy for multiple purposes.</span></span> <span data-ttu-id="42e5f-110">Einnig er hægt að stofna mörg tegundastigveldi í sérstökum tilgangi, t. d. til kynningar á afurð.</span><span class="sxs-lookup"><span data-stu-id="42e5f-110">Alternatively, you can create multiple retail category hierarchies for special purposes, such as product promotions.</span></span> <span data-ttu-id="42e5f-111">Þegar stofnað er stigveldi smásöluafurða verður að úthluta tegundastigveldisgerð til að auðkenna tilgang tegundastigveldisins.</span><span class="sxs-lookup"><span data-stu-id="42e5f-111">When you create a retail product hierarchy, you must assign a category hierarchy type to identify the purpose of the category hierarchy.</span></span> <span data-ttu-id="42e5f-112">Til dæmis er aðeins vísað í afurðastigveldi sem er úthlutað á **Yfirlitsstigveldi smásölu** þegar flett er í afurðum eftir tegund á netinu eða á sölustað (POS).</span><span class="sxs-lookup"><span data-stu-id="42e5f-112">For example, only product hierarchies that are assigned the **Retail navigation hierarchy** type are referenced when you browse products by category online or in point of sale (POS).</span></span>

## <a name="retail-hierarchy-types"></a><span data-ttu-id="42e5f-113">Gerðir smásölustigvelda</span><span class="sxs-lookup"><span data-stu-id="42e5f-113">Retail hierarchy types</span></span>
<span data-ttu-id="42e5f-114">Eftirfarandi tafla sýnir þær gerðir tegundastigvelda sem eru tiltækar og almennan tilgang hverrar gerðar.</span><span class="sxs-lookup"><span data-stu-id="42e5f-114">The following table lists the types of retail category hierarchies that are available and the general purpose of each type.</span></span>

| <span data-ttu-id="42e5f-115">Gerð tegundastigveldis</span><span class="sxs-lookup"><span data-stu-id="42e5f-115">Category hierarchy type</span></span>       | <span data-ttu-id="42e5f-116">Tilgangur</span><span class="sxs-lookup"><span data-stu-id="42e5f-116">Purpose</span></span>                                                                                                                                                                                                                                                                                                            |
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42e5f-117">Stigveldi smásöluafurða</span><span class="sxs-lookup"><span data-stu-id="42e5f-117">Retail product hierarchy</span></span>      | <span data-ttu-id="42e5f-118">Veljið þessa stigveldisgerð til að skilgreina aðalstigveldi smásöluafurða fyrir fyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="42e5f-118">Use this hierarchy type to define the overall product hierarchy for your organization.</span></span> <span data-ttu-id="42e5f-119">Hægt er að nota þessa gerð stigveldis fyrir smásölu, verðlagningu og kynningartilboð, skýrslugerð og skipulagningu úrvals.</span><span class="sxs-lookup"><span data-stu-id="42e5f-119">You can use this hierarchy type for merchandising, pricing and promotions, reporting, and assortment planning.</span></span> <span data-ttu-id="42e5f-120">Aðeins er hægt að úthluta einu stigveldi smásöluafurða þessu stigveldi.</span><span class="sxs-lookup"><span data-stu-id="42e5f-120">Only one retail product hierarchy can be assigned this hierarchy type.</span></span>                                       |
| <span data-ttu-id="42e5f-121">Viðbótarstigveldi smásölu</span><span class="sxs-lookup"><span data-stu-id="42e5f-121">Supplemental retail hierarchy</span></span> | <span data-ttu-id="42e5f-122">Notið þessa gerð stigveldis fyrir allar frekari tegundir smásölustigveldis sem á að stofna.</span><span class="sxs-lookup"><span data-stu-id="42e5f-122">Use this hierarchy type for any additional retail category hierarchies that you want to create.</span></span> <span data-ttu-id="42e5f-123">Til dæmis á vorin þarf kynningartilboð fyrir sundföt.</span><span class="sxs-lookup"><span data-stu-id="42e5f-123">For example, in the spring, you have a promotion for swimwear.</span></span> <span data-ttu-id="42e5f-124">Þess vegna hefurðu sundfataafurðirnar í aðskildu tegundastigveldi og beita verðlagningu kynningartilboðs á mismunandi tegundir afurða.</span><span class="sxs-lookup"><span data-stu-id="42e5f-124">Therefore, you include your swimwear products in a separate category hierarchy and apply the promotional pricing to the various product categories.</span></span> |
| <span data-ttu-id="42e5f-125">Skoðunarstigveldi smásölu</span><span class="sxs-lookup"><span data-stu-id="42e5f-125">Retail navigation hierarchy</span></span>   | <span data-ttu-id="42e5f-126">Notið þessa gerð stigveldis til að flokka og raða afurðum í tegundum svo að hægt sé að skoða afurðir á netinu eða á söllustað.</span><span class="sxs-lookup"><span data-stu-id="42e5f-126">Use this hierarchy type to group and organize products into categories so that the products can be browsed online or in POS.</span></span>                                                                                                                                                                                       |

<span data-ttu-id="42e5f-127">Með tegundastigveldi smásölu til að skipuleggja vörur er hægt að setja upp og viðhalda afurðareigindum og eiginleikum tegundastigs.</span><span class="sxs-lookup"><span data-stu-id="42e5f-127">By using a retail category hierarchy to structure your products, you can set up and maintain product attributes and properties at the category level.</span></span> <span data-ttu-id="42e5f-128">Þessi eigindir og eiginleikar hafa stillingar fyrir afurðavíddir og stillingar á Sölustað.</span><span class="sxs-lookup"><span data-stu-id="42e5f-128">These attributes and properties include settings for product dimensions and POS settings.</span></span> <span data-ttu-id="42e5f-129">Allar afurðir sem er úthlutað á tegundirnar erfa sjálfkrafa þær eigindir og eiginleika sem eru skilgreindir.</span><span class="sxs-lookup"><span data-stu-id="42e5f-129">Any products that you assign to the categories automatically inherit the attributes and properties that you define.</span></span> <span data-ttu-id="42e5f-130">Einnig er hægt að afrita stillingar eiginleika fyrir afurðir í margar afurðir í valinni tegund á sama tíma.</span><span class="sxs-lookup"><span data-stu-id="42e5f-130">You can also copy the property settings for any product to multiple products in a selected category at the same time.</span></span>




