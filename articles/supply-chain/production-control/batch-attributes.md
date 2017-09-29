---
title: Runueigindir
description: "Þessi grein gefur upplýsingar um runueigindir. Runueigindi eru einkenni hráefnis og fullunninna afurða sem birgðakeyrslur samanstanda af. Greinin útskýrir einnig hvernig á að úthluta runueigindum, og hvernig hægt er að leita í þeim þegar runur eru teknar frá."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PdsBatchAttrib, PdsBatchAttribAssociate, PdsBatchAttribByAttribGroup, PdsBatchAttribByItem, PdsBatchAttribByitemCustomer, PdsBatchAttribGroup
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19271
ms.assetid: 41de0250-4a96-412e-a412-aa06615b6b1d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 0c3f5115377178941984e53749c18cc1c9179812
ms.contentlocale: is-is
ms.lasthandoff: 07/18/2017

---

# <a name="batch-attributes"></a><span data-ttu-id="8281a-105">Runueigindir</span><span class="sxs-lookup"><span data-stu-id="8281a-105">Batch attributes</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="8281a-106">Þessi grein gefur upplýsingar um runueigindir.</span><span class="sxs-lookup"><span data-stu-id="8281a-106">This article provides information about batch attributes.</span></span> <span data-ttu-id="8281a-107">Runueigindi eru einkenni hráefnis og fullunninna afurða sem birgðakeyrslur samanstanda af.</span><span class="sxs-lookup"><span data-stu-id="8281a-107">Batch attributes are characteristics of raw materials and finished products that make up inventory batches.</span></span> <span data-ttu-id="8281a-108">Greinin útskýrir einnig hvernig á að úthluta runueigindum, og hvernig hægt er að leita í þeim þegar runur eru teknar frá.</span><span class="sxs-lookup"><span data-stu-id="8281a-108">The article also explains how to assign batch attributes, and how you can search on them when you reserve batches.</span></span>

<span data-ttu-id="8281a-109">Runueigindi eru einkenni hráefnis og fullunninna afurða sem birgðakeyrslur samanstanda af.</span><span class="sxs-lookup"><span data-stu-id="8281a-109">Batch attributes are characteristics of raw materials and finished products that make up inventory batches.</span></span> <span data-ttu-id="8281a-110">Runueigindir geta verið mismunandi, eftir þáttum eins og umhverfisþáttum, gæðum hráefna sem eru notuð til að framleiða rununa eða niðurstöðu endanlegrar afurðar.</span><span class="sxs-lookup"><span data-stu-id="8281a-110">Batch attributes can vary, depending on factors such as environmental conditions, the quality of the raw materials that are used to produce the batch, or the outcome of the finished product.</span></span> <span data-ttu-id="8281a-111">Númer og gerðir runueiginda sem eru notaðar geta verið afar mismunandi frá einni atvinnugrein til annarrar.</span><span class="sxs-lookup"><span data-stu-id="8281a-111">The number and types of batch attributes that are used can vary widely from one industry to another.</span></span> <span data-ttu-id="8281a-112">Hér eru tvö dæmi sem sýna hvernig á að nota runueigindir:</span><span class="sxs-lookup"><span data-stu-id="8281a-112">Here are two examples that show how to use batch attributes:</span></span>

-   <span data-ttu-id="8281a-113">Á sviði ostagerðar getur mjólk, sem er eitt af þeim hráefnum sem eru notuð til að framleiða ost, haft eigindirnar eins og fituinnihald og prósentuþyngd.</span><span class="sxs-lookup"><span data-stu-id="8281a-113">In the cheese industry, milk, which is one of the raw materials that are used to produce the cheese, can have attributes such as fat content and percentage weight.</span></span> <span data-ttu-id="8281a-114">Ostur sem er framleiddur úr mjólk getur haft aðrar eiginleika, eins og rakastig og aldur.</span><span class="sxs-lookup"><span data-stu-id="8281a-114">The cheese that is produced from the milk can have other attributes, such as moisture and age.</span></span>
-   <span data-ttu-id="8281a-115">Í stáliðnaðinum getur járn sem er framleitt gæti hafa eigindir eins og prósentur magnesíuminnihalds, silfurinnihalds og sinkinnihalds.</span><span class="sxs-lookup"><span data-stu-id="8281a-115">In the steel industry, the iron that is produced might have attributes such as the percentages of magnesium content, silver content, and zinc content.</span></span>

<span data-ttu-id="8281a-116">Til að stjórna númer og gerðir eiginda, er hægt að nota runueigindaflokkar.</span><span class="sxs-lookup"><span data-stu-id="8281a-116">To better manage the number and types of attributes, you can use batch attribute groups.</span></span> <span data-ttu-id="8281a-117">Á þennan hátt þarf ekki að bæta hverri eigind sérstaklega við.</span><span class="sxs-lookup"><span data-stu-id="8281a-117">In this way, you don't have to add each attribute individually.</span></span>

## <a name="assign-batch-attributes"></a><span data-ttu-id="8281a-118">Úthluta runueigindum</span><span class="sxs-lookup"><span data-stu-id="8281a-118">Assign batch attributes</span></span>
<span data-ttu-id="8281a-119">Hægt er að úthluta runueigindum á stakar afurðir sem eru í birgðarunum, eða hægt er að úthluta þeim á afurðir sem tengjast ákveðnum viðskiptavinum.</span><span class="sxs-lookup"><span data-stu-id="8281a-119">You can assign batch attributes to individual products that are held in inventory batches, or you can assign them to products that are associated with specific customers.</span></span> <span data-ttu-id="8281a-120">Áður en hægt er að úthluta runueigind á stigi viðskiptavinar verður að úthluta henni á stigi afurðar.</span><span class="sxs-lookup"><span data-stu-id="8281a-120">Before you can assign a batch attribute at the customer level, you must assign it at the product level.</span></span> <span data-ttu-id="8281a-121">Afurðin verður að hafa runuvíddina stillta á **Virka** í rakningarvíddarflokknum.</span><span class="sxs-lookup"><span data-stu-id="8281a-121">The product must have the batch dimension set to **Active** in the tracking dimension group.</span></span> <span data-ttu-id="8281a-122">Til að úthluta runueigind á staka vöru skal nota afurðabundna síðu.</span><span class="sxs-lookup"><span data-stu-id="8281a-122">To assign a batch attribute to an individual product, use the product-specific page.</span></span> <span data-ttu-id="8281a-123">Ef eigindin er bundin við afurð fyrir viðskiptavin skal nota síðu tiltekins viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="8281a-123">If the attribute is specific to a product for a customer, use the customer-specific page.</span></span> <span data-ttu-id="8281a-124">Þegar eigind er bætt við vöru þarf einnig að skilgreina aðrar færibreytur.</span><span class="sxs-lookup"><span data-stu-id="8281a-124">When you add an attribute to a product, you also define other parameters.</span></span> <span data-ttu-id="8281a-125">Hér eru nokkur dæmi:</span><span class="sxs-lookup"><span data-stu-id="8281a-125">Here are some examples:</span></span>

-   <span data-ttu-id="8281a-126">Færið inn lágmarksgildi á bilinu fyrir eigindagerðirnar **Heiltala** eða **Brot**.</span><span class="sxs-lookup"><span data-stu-id="8281a-126">The minimum and maximum ranges for an attribute of the **Integer** or **Fraction** type.</span></span>
-   <span data-ttu-id="8281a-127">Vikmarkaaðgerðir fyrir eigindagerðirnar **Heiltala** eða **Brot**.</span><span class="sxs-lookup"><span data-stu-id="8281a-127">The tolerance actions for an attribute of the **Integer** or **Fraction** type.</span></span> <span data-ttu-id="8281a-128">Ef gildi eigindarinnar er utan marka lágmarks- og hámarksbils getur aðgerðin verið annaðhvort viðvörun eða villuboð.</span><span class="sxs-lookup"><span data-stu-id="8281a-128">If the value of the attribute falls outside the minimum and maximum range, the action can be either a warning message or an error message.</span></span>
-   <span data-ttu-id="8281a-129">Markgildi fyrir eigindina.</span><span class="sxs-lookup"><span data-stu-id="8281a-129">The target value for the attribute.</span></span> <span data-ttu-id="8281a-130">Þetta gildi er kjörgildi eigindarinnar og það á við um allar gerðir eiginda.</span><span class="sxs-lookup"><span data-stu-id="8281a-130">This value is the optimal value of the attribute, and it applies to all attribute types.</span></span>

<span data-ttu-id="8281a-131">Hægt er að opna síður fyrir afurðir sem eru valdar á síðunni **Útgefnar afurðir** í afurðastjórnun upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="8281a-131">You can access the pages for products that you select on the **Released products** page in Product information management.</span></span> <span data-ttu-id="8281a-132">Eftir runueigindum er úthlutað á afurð er hægt að bæta tilteknu gildi við eigindir á síðunni **Birgðarunueigindir**.</span><span class="sxs-lookup"><span data-stu-id="8281a-132">After you assign batch attributes to a product, you can add specific values to the attributes on the **Inventory batch attributes** page.</span></span>

## <a name="reserve-batches"></a><span data-ttu-id="8281a-133">Taka frá runur</span><span class="sxs-lookup"><span data-stu-id="8281a-133">Reserve batches</span></span>
<span data-ttu-id="8281a-134">Hægt er að leita í runueigindum þegar gerðar eru runufrátekningar fyrir sölupöntun til að framfylgja pöntun viðskiptavinar, eða þegar runur eru tíndar og teknar frá fyrir framleiðslupöntun.</span><span class="sxs-lookup"><span data-stu-id="8281a-134">You can search on batch attributes when you do batch reservations for a sales order to fullfill a customer's order, or when you pick and reserve batches for a production order.</span></span> <span data-ttu-id="8281a-135">Leitin hjálpar til við að staðsetja birgðarunu sem inniheldur afurðina sem hefur þá runueigind sem óskað er.</span><span class="sxs-lookup"><span data-stu-id="8281a-135">The search helps locate an inventory batch that contains the product that has the batch attribute that you want.</span></span> <span data-ttu-id="8281a-136">Þegar búið er að finna runu eða runur er hægt að taka frá afurð fyrir upphaflega færslulínu birgða.</span><span class="sxs-lookup"><span data-stu-id="8281a-136">After you locate the batch or batches, you can reserve the product to the originating inventory transaction line.</span></span>




