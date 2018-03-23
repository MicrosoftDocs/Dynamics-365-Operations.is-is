---
title: "Stjórnun afurðategundar"
description: "Í þessu efnisatriði er því lýst hvernig vörustjórar geta notað tegundir Retail afurða til að stjórna tengslum milli stigveldis Retail afurðar og upplýsinga um losaðar afurðir."
author: ashishmsft
manager: AnnBe
ms.date: 10/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 
ms.assetid: c7ed2ba5-87c6-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 25fa39dc81fc721d7593a25a102ce47041ebc5f0
ms.openlocfilehash: 4b7ef962b777a31e1da238a8ec1be9a42ec5bb5f
ms.contentlocale: is-is
ms.lasthandoff: 03/13/2018

---


# <a name="enhanced-product-and-category-management"></a><span data-ttu-id="d62a1-103">Betri stjórnun afurða og tegunda</span><span class="sxs-lookup"><span data-stu-id="d62a1-103">Enhanced product and category management</span></span>

[!include[banner](./includes/banner.md)]

<span data-ttu-id="d62a1-104">Þetta efnisatriði lýsir betri leið til að stjórna tegundum Retail afurða og afurða í Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="d62a1-104">This topic describes an enhanced way to manage Retail product categories and products in Dynamics 365 for Retail.</span></span> <span data-ttu-id="d62a1-105">Þessar viðbætur gera vörustjórum kleift að skoða algenga byggingu á eiginleikum afurðar milli stigveldis Retail afurðar og upplýsinga um losaðar afurðir.</span><span class="sxs-lookup"><span data-stu-id="d62a1-105">These enhancements let merchandising managers view a common structure of product properties between Retail product hierarchy and released product details.</span></span>

<span data-ttu-id="d62a1-106">Til að læra meira um stjórnun á tegundum Retail afurða skal fara í **Stigveldi Retail afurðar** frá vinnusvæðinu **Flokka- og afurðastjórnun** og athuga aukna byggingu á síðunni **Tegund Retail afurðar**.</span><span class="sxs-lookup"><span data-stu-id="d62a1-106">To learn more about managing Retail product categories, go to **Retail product hierarchy** from the **Category and product management** workspace, and note the enhanced structure of the **Retail product category** page.</span></span>

![Vinnusvæði fyrir stjórnun tegunda og afurða](media/LaunchRetailProductHierarchy.png)

<span data-ttu-id="d62a1-108">Í fyrri útgáfum var eiginleikum afurða skipt í **Grunneiginleika afurðar** og **Eiginleika Retail afurðar** byggt á hæfi þeirra.</span><span class="sxs-lookup"><span data-stu-id="d62a1-108">In previous versions, product properties were divided into **Basic product properties** and **Retail product properties**, based on the scope of their applicability.</span></span> <span data-ttu-id="d62a1-109">**Eiginleikar Retail afurðar** voru *altækir* út frá notkunareiginleikum þeirra sem þýðir að fyrir tiltekinn **Eiginleika Retail afurðar** er sama gildinu deilt þvert yfir alla lögaðila.</span><span class="sxs-lookup"><span data-stu-id="d62a1-109">**Retail product properties** were *global* by scope of applicability, which means that for a given **Retail product property**, the same value is shared across all legal entities.</span></span> <span data-ttu-id="d62a1-110">**Grunneiginleikar afurðar** eru *sértæk lögaðila*.</span><span class="sxs-lookup"><span data-stu-id="d62a1-110">**Basic product properties** are *legal entity specific*.</span></span> <span data-ttu-id="d62a1-111">M.ö.o., fyrir tiltekinn **Grunneiginleika afurðar** getur gildið verið mismunandi þvert yfir lögaðila, byggt á einstökum viðskiptakröfum.</span><span class="sxs-lookup"><span data-stu-id="d62a1-111">In other words, for a given **Basic product property** the value can differ across legal entities, based on individual business requirements.</span></span>

<span data-ttu-id="d62a1-112">Með aukinni byggingu á tegundum Retail afurðar eru eiginleikar afurða röklega greindir í sundur eftir notkunareiginleikum þeirra innan hóps til að endurspegla byggingu skjámyndar fyrir upplýsingar um losaðar afurðir.</span><span class="sxs-lookup"><span data-stu-id="d62a1-112">In the enhanced Retail product category structure, product properties are logically separated based on their applicability within a group, to reflect the released product details form structure.</span></span>

![Flokkun svæða byggt á gildissviði þeirra](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

<span data-ttu-id="d62a1-114">Hægt er að skipta á milli stjórnunar á eiginleikum tiltekinna lögaðila sem eiga við alla lögaðila og stjórnunar eiginleika sem eru sértækir fyrir tiltekinn lögaðila.</span><span class="sxs-lookup"><span data-stu-id="d62a1-114">You can switch between managing legal-entity specific properties across all legal entities and managing them for a specific legal entity.</span></span> <span data-ttu-id="d62a1-115">Til að gera þetta skal velja annað hvort **Skoða/breyta fyrir alla lögaðila** eða **Skoða/breyta fyrir tiltekinn lögaðila**.</span><span class="sxs-lookup"><span data-stu-id="d62a1-115">To do this, select either **View/Edit for all legal entities** or **View/Edit for a specific legal entity**.</span></span>

![Víxlaðu á milli yfirlits á einstaklingi og öllum lögaðilum](media/ToggleBackToEditForSpecificLegalEntity.PNG)

![Víxlaðu á milli yfirlits á einstaklingi og öllum lögaðilum](media/ToggleToEditForAllLegalEntities.PNG)  

<span data-ttu-id="d62a1-118">Í samanburði við fyrri útgáfur getur vörustjóri í nýju byggingunni á tegundum Retail afurðar einnig skilgreint sjálfgildi fyrir viðbótarsett af eiginleikum afurðar á stigi einstakra tegunda.</span><span class="sxs-lookup"><span data-stu-id="d62a1-118">Compared to previous versions, in the new Retail product category structure a merchandising manager can also define default values for an additional set of product properties at an individual category level.</span></span> <span data-ttu-id="d62a1-119">Við stofnun afurðar erfir afurð þessi sjálfgefnu eiginleikagildi afurða, byggt á tengslum þeirra við einstaka tegund í stigveldi Retail afurðar.</span><span class="sxs-lookup"><span data-stu-id="d62a1-119">At the time of product creation, these default product property values are inherited by a product, based on their association with an individual category from Retail product hierarchy.</span></span> <span data-ttu-id="d62a1-120">Þessar erfðu eiginleikar afurðar er einnig hægt að breyta fyrir hverja afurð til að mæta einstökum viðskiptakröfum.</span><span class="sxs-lookup"><span data-stu-id="d62a1-120">These inherited product properties can also be modified for each product, to meet individual business requirements.</span></span>

## <a name="select-properties-to-update-products-from-the-retail-product-category-form"></a><span data-ttu-id="d62a1-121">Veldu eiginleika til að uppfæra afurðir af skjámyndinni tegund smásöluafurðar</span><span class="sxs-lookup"><span data-stu-id="d62a1-121">Select properties to update products from the Retail product category form</span></span> 
 
<span data-ttu-id="d62a1-122">Hægt er að nota þessa nýju betrumbættu byggingu fyrir eiginleika afurðar til að velja hvaða uppfærðu eiginleikar afurðar á að flytja til tengdra afurða.</span><span class="sxs-lookup"><span data-stu-id="d62a1-122">You can use this new enhanced structure for product properties to select which updated product properties must be pushed to associated products.</span></span> 

![Nýtt betrumbætt yfirlit á uppfærðum afurðum](media/NewUpdateProductsEnhancedView.PNG) 

<span data-ttu-id="d62a1-124">Stjórnendur smásölu geta breytt þessum arfgengu eiginleikum afurða fyrir hverja afurð til að mæta tilteknum viðskiptakröfum.</span><span class="sxs-lookup"><span data-stu-id="d62a1-124">Merchandising managers can modify these inherited product properties for each product, to meet individual business requirements.</span></span>


