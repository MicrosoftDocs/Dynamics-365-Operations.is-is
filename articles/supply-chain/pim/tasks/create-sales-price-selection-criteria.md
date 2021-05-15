---
title: Stofna valskilyrði fyrir söluverð
description: Þessi verklýsing sýnir hvernig á að stofna valskilyrði söluverðs fyrir eigindabyggð söluverðslíkön.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelSelectionCriteria, SysQueryForm, SysQueryTableLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 69d22c3321beaa2667ee20bff00acd746714b993
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920532"
---
# <a name="create-sales-price-selection-criteria"></a><span data-ttu-id="01675-103">Stofna valskilyrði fyrir söluverð</span><span class="sxs-lookup"><span data-stu-id="01675-103">Create sales price selection criteria</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="01675-104">Þessi verklýsing sýnir hvernig á að stofna valskilyrði söluverðs fyrir eigindabyggð söluverðslíkön.</span><span class="sxs-lookup"><span data-stu-id="01675-104">This procedure shows how to create a sales price selection criterion for attribute-based sales price models.</span></span> <span data-ttu-id="01675-105">Þetta ferli krefst þess að að minnsta kosti eitt afbrigðalíkan afurðar sé tiltækt.</span><span class="sxs-lookup"><span data-stu-id="01675-105">This procedure requires that at least one sales price model be available.</span></span> <span data-ttu-id="01675-106">Þetta dæmi notar verðlíkanið fyrir söluverðslíkan hátalaralausnar í sýnigagnafyrirtækinu USMF.</span><span class="sxs-lookup"><span data-stu-id="01675-106">This example uses the price model for the Speaker solution sales price model in the USMF demo data company.</span></span> <span data-ttu-id="01675-107">Venjulega notar framleiðslustjóri þetta ferli.</span><span class="sxs-lookup"><span data-stu-id="01675-107">Typically, a product manager uses this procedure.</span></span>

## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a><span data-ttu-id="01675-108">Bæta við nýju skilyrði fyrir fyrirliggjandi söluverðlíkan</span><span class="sxs-lookup"><span data-stu-id="01675-108">Add a new criterion for an existing sales price model</span></span>

1. <span data-ttu-id="01675-109">Farið í **Afurðarupplýsingastjórnun \> Afurðir \> Afbrigðalíkön afurða**.</span><span class="sxs-lookup"><span data-stu-id="01675-109">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="01675-110">Á listanum velurðu línuna fyrir vörulíkan hátalaralausnar, en smelltu ekki á tengilinn fyrir heiti líkans.</span><span class="sxs-lookup"><span data-stu-id="01675-110">In the list, select the row for the Speaker solution product model, but don't select the link for the model name.</span></span>
1. <span data-ttu-id="01675-111">Í aðgerðarúðunni skal velja **Tegund**.</span><span class="sxs-lookup"><span data-stu-id="01675-111">On the Action Pane, select **Model**.</span></span>
1. <span data-ttu-id="01675-112">Veljið **Skilyrði verðlíkans.**</span><span class="sxs-lookup"><span data-stu-id="01675-112">Select **Price model criteria**.</span></span>
1. <span data-ttu-id="01675-113">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="01675-113">Select **New**.</span></span>
1. <span data-ttu-id="01675-114">Í svæðið **Heiti**, slærðu inn Viðskiptavinaflokkur 10.</span><span class="sxs-lookup"><span data-stu-id="01675-114">In the **Name** field, type 'Customer group 10'.</span></span>
    * <span data-ttu-id="01675-115">Heiti verðlíkans er notað til að finna undirliggjandi valskilyrði.</span><span class="sxs-lookup"><span data-stu-id="01675-115">The name of the price model criterion is used to help identify the underlying selection criteria.</span></span>  
1. <span data-ttu-id="01675-116">Í reitinn **Verðlíkan** skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="01675-116">In the **Price model** field, enter or select a value.</span></span>
1. <span data-ttu-id="01675-117">Í reitnum **Gerð pöntunar** velurðu *Sölupöntun*.</span><span class="sxs-lookup"><span data-stu-id="01675-117">In the **Order type** field, select *Sales order*.</span></span>
    * <span data-ttu-id="01675-118">Gerð pöntunar ákvarðar gagnagrunnsvæði sem eru tiltæk fyrir valfyrirspurn.</span><span class="sxs-lookup"><span data-stu-id="01675-118">The order type determines the database fields that will be available for the selection query.</span></span>  
1. <span data-ttu-id="01675-119">Færa skal inn dagsetningu í svæðinu **Gildir frá**.</span><span class="sxs-lookup"><span data-stu-id="01675-119">In the **Valid from** field, enter a date.</span></span>
1. <span data-ttu-id="01675-120">Í reitinn **Fella úr gildi**, skal færa inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="01675-120">In the **Expire by** field, enter a date.</span></span>
1. <span data-ttu-id="01675-121">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="01675-121">Select **Save**.</span></span>

## <a name="create-the-query-for-the-selection-criteria"></a><span data-ttu-id="01675-122">Búa til fyrirspurn fyrir valskilyrði</span><span class="sxs-lookup"><span data-stu-id="01675-122">Create the query for the selection criteria</span></span>

1. <span data-ttu-id="01675-123">Veljið **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="01675-123">Select **Edit**.</span></span>
2. <span data-ttu-id="01675-124">Í reitnum **Tafla** skal velja *Viðskiptavinir*.</span><span class="sxs-lookup"><span data-stu-id="01675-124">In the **Table** field, select *Customers*.</span></span>
3. <span data-ttu-id="01675-125">Í reitnum **Reitur** er valið *Viðskiptavinaflokkur*.</span><span class="sxs-lookup"><span data-stu-id="01675-125">In the **Field** field, select *Customer group*.</span></span>
    * <span data-ttu-id="01675-126">Í þessu dæmi notum við tiltekinn viðskiptavinaflokk fyrir valskilyrði.</span><span class="sxs-lookup"><span data-stu-id="01675-126">In this example, we will use a specific customer group for the selection criteria.</span></span>  
4. <span data-ttu-id="01675-127">Í reitnum **Skilyrði** er valið *Viðskiptavinaflokkur 10*.</span><span class="sxs-lookup"><span data-stu-id="01675-127">In the **Criteria** field, select *Customer group 10*.</span></span>
5. <span data-ttu-id="01675-128">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="01675-128">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]