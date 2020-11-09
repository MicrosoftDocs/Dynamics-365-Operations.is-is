---
title: Runueigindir
description: Þetta efnisatriði gefur upplýsingar um runueigindir. Runueigindi eru einkenni hráefnis og fullunninna afurða sem birgðakeyrslur samanstanda af. Þetta efnisatriði útskýrir einnig hvernig á að úthluta runueigindum, og hvernig hægt er að leita í þeim þegar runur eru teknar frá.
author: ShylaThompson
manager: tfehr
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PdsBatchAttrib, PdsBatchAttribAssociate, PdsBatchAttribByAttribGroup, PdsBatchAttribByItem, PdsBatchAttribByitemCustomer, PdsBatchAttribGroup, WHSBatchAttribReserve
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19271
ms.assetid: 41de0250-4a96-412e-a412-aa06615b6b1d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 370893e415a79091404f1c4eb0404ba8fd5b9ff2
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017529"
---
# <a name="batch-attributes"></a><span data-ttu-id="60e3d-105">Runueigindir</span><span class="sxs-lookup"><span data-stu-id="60e3d-105">Batch attributes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="60e3d-106">Þetta efnisatriði gefur upplýsingar um runueigindir.</span><span class="sxs-lookup"><span data-stu-id="60e3d-106">This topic provides information about batch attributes.</span></span> <span data-ttu-id="60e3d-107">Runueigindi eru einkenni hráefnis og fullunninna afurða sem birgðakeyrslur samanstanda af.</span><span class="sxs-lookup"><span data-stu-id="60e3d-107">Batch attributes are characteristics of raw materials and finished products that make up inventory batches.</span></span> <span data-ttu-id="60e3d-108">Þetta efnisatriði útskýrir einnig hvernig á að úthluta runueigindum, og hvernig hægt er að leita í þeim þegar runur eru teknar frá.</span><span class="sxs-lookup"><span data-stu-id="60e3d-108">The topic also explains how to assign batch attributes, and how you can search on them when you reserve batches.</span></span>

<span data-ttu-id="60e3d-109">Runueigindi eru einkenni hráefnis og fullunninna afurða sem birgðakeyrslur samanstanda af.</span><span class="sxs-lookup"><span data-stu-id="60e3d-109">Batch attributes are characteristics of raw materials and finished products that make up inventory batches.</span></span> <span data-ttu-id="60e3d-110">Runueigindir geta verið mismunandi, eftir þáttum eins og umhverfisþáttum, gæðum hráefna sem eru notuð til að framleiða rununa eða niðurstöðu endanlegrar afurðar.</span><span class="sxs-lookup"><span data-stu-id="60e3d-110">Batch attributes can vary, depending on factors such as environmental conditions, the quality of the raw materials that are used to produce the batch, or the outcome of the finished product.</span></span> <span data-ttu-id="60e3d-111">Númer og gerðir runueiginda sem eru notaðar geta verið afar mismunandi frá einni atvinnugrein til annarrar.</span><span class="sxs-lookup"><span data-stu-id="60e3d-111">The number and types of batch attributes that are used can vary widely from one industry to another.</span></span> <span data-ttu-id="60e3d-112">Hér eru tvö dæmi sem sýna hvernig á að nota runueigindir:</span><span class="sxs-lookup"><span data-stu-id="60e3d-112">Here are two examples that show how to use batch attributes:</span></span>

-   <span data-ttu-id="60e3d-113">Á sviði ostagerðar getur mjólk, sem er eitt af þeim hráefnum sem eru notuð til að framleiða ost, haft eigindirnar eins og fituinnihald og prósentuþyngd.</span><span class="sxs-lookup"><span data-stu-id="60e3d-113">In the cheese industry, milk, which is one of the raw materials that are used to produce the cheese, can have attributes such as fat content and percentage weight.</span></span> <span data-ttu-id="60e3d-114">Ostur sem er framleiddur úr mjólk getur haft aðrar eiginleika, eins og rakastig og aldur.</span><span class="sxs-lookup"><span data-stu-id="60e3d-114">The cheese that is produced from the milk can have other attributes, such as moisture and age.</span></span>
-   <span data-ttu-id="60e3d-115">Í stáliðnaðinum getur járn sem er framleitt gæti hafa eigindir eins og prósentur magnesíuminnihalds, silfurinnihalds og sinkinnihalds.</span><span class="sxs-lookup"><span data-stu-id="60e3d-115">In the steel industry, the iron that is produced might have attributes such as the percentages of magnesium content, silver content, and zinc content.</span></span>

<span data-ttu-id="60e3d-116">Til að stjórna númer og gerðir eiginda, er hægt að nota runueigindaflokkar.</span><span class="sxs-lookup"><span data-stu-id="60e3d-116">To better manage the number and types of attributes, you can use batch attribute groups.</span></span> <span data-ttu-id="60e3d-117">Á þennan hátt þarf ekki að bæta hverri eigind sérstaklega við.</span><span class="sxs-lookup"><span data-stu-id="60e3d-117">In this way, you don't have to add each attribute individually.</span></span>

## <a name="assign-batch-attributes"></a><span data-ttu-id="60e3d-118">Úthluta runueigindum</span><span class="sxs-lookup"><span data-stu-id="60e3d-118">Assign batch attributes</span></span>
<span data-ttu-id="60e3d-119">Hægt er að úthluta runueigindum á stakar afurðir sem eru í birgðarunum, eða hægt er að úthluta þeim á afurðir sem tengjast ákveðnum viðskiptavinum.</span><span class="sxs-lookup"><span data-stu-id="60e3d-119">You can assign batch attributes to individual products that are held in inventory batches, or you can assign them to products that are associated with specific customers.</span></span> <span data-ttu-id="60e3d-120">Áður en hægt er að úthluta runueigind á stigi viðskiptavinar verður að úthluta henni á stigi afurðar.</span><span class="sxs-lookup"><span data-stu-id="60e3d-120">Before you can assign a batch attribute at the customer level, you must assign it at the product level.</span></span> <span data-ttu-id="60e3d-121">Afurðin verður að hafa runuvíddina stillta á **Virka** í rakningarvíddarflokknum.</span><span class="sxs-lookup"><span data-stu-id="60e3d-121">The product must have the batch dimension set to **Active** in the tracking dimension group.</span></span> <span data-ttu-id="60e3d-122">Til að úthluta runueigind á staka vöru skal nota afurðabundna síðu.</span><span class="sxs-lookup"><span data-stu-id="60e3d-122">To assign a batch attribute to an individual product, use the product-specific page.</span></span> <span data-ttu-id="60e3d-123">Ef eigindin er bundin við afurð fyrir viðskiptavin skal nota síðu tiltekins viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="60e3d-123">If the attribute is specific to a product for a customer, use the customer-specific page.</span></span> <span data-ttu-id="60e3d-124">Þegar eigind er bætt við vöru þarf einnig að skilgreina aðrar færibreytur.</span><span class="sxs-lookup"><span data-stu-id="60e3d-124">When you add an attribute to a product, you also define other parameters.</span></span> <span data-ttu-id="60e3d-125">Hér eru nokkur dæmi:</span><span class="sxs-lookup"><span data-stu-id="60e3d-125">Here are some examples:</span></span>

-   <span data-ttu-id="60e3d-126">Færið inn lágmarksgildi á bilinu fyrir eigindagerðirnar **Heiltala** eða **Brot**.</span><span class="sxs-lookup"><span data-stu-id="60e3d-126">The minimum and maximum ranges for an attribute of the **Integer** or **Fraction** type.</span></span>
-   <span data-ttu-id="60e3d-127">Vikmarkaaðgerðir fyrir eigindagerðirnar **Heiltala** eða **Brot**.</span><span class="sxs-lookup"><span data-stu-id="60e3d-127">The tolerance actions for an attribute of the **Integer** or **Fraction** type.</span></span> <span data-ttu-id="60e3d-128">Ef gildi eigindarinnar er utan marka lágmarks- og hámarksbils getur aðgerðin verið annaðhvort viðvörun eða villuboð.</span><span class="sxs-lookup"><span data-stu-id="60e3d-128">If the value of the attribute falls outside the minimum and maximum range, the action can be either a warning message or an error message.</span></span>
-   <span data-ttu-id="60e3d-129">Markgildi fyrir eigindina.</span><span class="sxs-lookup"><span data-stu-id="60e3d-129">The target value for the attribute.</span></span> <span data-ttu-id="60e3d-130">Þetta gildi er kjörgildi eigindarinnar og það á við um allar gerðir eiginda.</span><span class="sxs-lookup"><span data-stu-id="60e3d-130">This value is the optimal value of the attribute, and it applies to all attribute types.</span></span>

<span data-ttu-id="60e3d-131">Hægt er að opna síður fyrir afurðir sem eru valdar á síðunni **Útgefnar afurðir** í afurðastjórnun upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="60e3d-131">You can access the pages for products that you select on the **Released products** page in Product information management.</span></span> <span data-ttu-id="60e3d-132">Eftir runueigindum er úthlutað á afurð er hægt að bæta tilteknu gildi við eigindir á síðunni **Birgðarunueigindir**.</span><span class="sxs-lookup"><span data-stu-id="60e3d-132">After you assign batch attributes to a product, you can add specific values to the attributes on the **Inventory batch attributes** page.</span></span>

## <a name="reserve-batches"></a><span data-ttu-id="60e3d-133">Taka frá runur</span><span class="sxs-lookup"><span data-stu-id="60e3d-133">Reserve batches</span></span>
<span data-ttu-id="60e3d-134">Hægt er að leita í runueigindum þegar gerðar eru runufrátekningar fyrir sölupöntun til að framfylgja pöntun viðskiptavinar, eða þegar runur eru tíndar og teknar frá fyrir framleiðslupöntun.</span><span class="sxs-lookup"><span data-stu-id="60e3d-134">You can search on batch attributes when you do batch reservations for a sales order to fulfill a customer's order, or when you pick and reserve batches for a production order.</span></span> <span data-ttu-id="60e3d-135">Leitin hjálpar til við að staðsetja birgðarunu sem inniheldur afurðina sem hefur þá runueigind sem óskað er.</span><span class="sxs-lookup"><span data-stu-id="60e3d-135">The search helps locate an inventory batch that contains the product that has the batch attribute that you want.</span></span> <span data-ttu-id="60e3d-136">Þegar búið er að finna runu eða runur er hægt að taka frá afurð fyrir upphaflega færslulínu birgða.</span><span class="sxs-lookup"><span data-stu-id="60e3d-136">After you locate the batch or batches, you can reserve the product to the originating inventory transaction line.</span></span>



