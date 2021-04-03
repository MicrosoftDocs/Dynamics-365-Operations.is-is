---
title: Flýtiskoðunareining
description: Þetta efnisatriði fjallar um flýtiskoðunareiningar og útskýrir hvernig á að bæta þeim við svæðissíður í Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2020-01-08
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 07fbf8d4115561808b7c61489b343e1c72dd1b6d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5243794"
---
# <a name="quick-view-module"></a><span data-ttu-id="f1e69-103">Flýtiskoðunareining</span><span class="sxs-lookup"><span data-stu-id="f1e69-103">Quick view module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="f1e69-104">Þetta efnisatriði fjallar um flýtiskoðunareiningar og útskýrir hvernig á að bæta þeim við svæðissíður í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f1e69-104">This topic covers quick view modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="f1e69-105">Flýtiskoðunareiningin gerir notendum kleift að skoða afurðarupplýsingar á fljótlegan hátt þegar þeir fletta upp afurðum á listasíðu og bæta einni eða fleiri afurðum við körfuna úr listasíðunni án þess að þurfa að fara á upplýsingasíðu afurðar.</span><span class="sxs-lookup"><span data-stu-id="f1e69-105">The quick view module lets users quickly view product information when they browse products on a list page, and add one or more products to the cart from the list page, without having to go to the product details page (PDP).</span></span> <span data-ttu-id="f1e69-106">Flýtiskoðunareiningin veitir yfirlit afurðarupplýsinga sem notandi þurfa til að geta tekið ákvörðun um „bæta við körfu“.</span><span class="sxs-lookup"><span data-stu-id="f1e69-106">The quick view module provides an overview of the product information that users require to make an "add to cart" decision.</span></span> <span data-ttu-id="f1e69-107">Hún býður einnig upp á tengil á upplýsingasíðu afurðar þannig að notendur geta skoðað frekari upplýsingar um afurð og kaupmöguleika.</span><span class="sxs-lookup"><span data-stu-id="f1e69-107">It also provides a link to the PDP, so that users can view additional product details and purchase options.</span></span>

<span data-ttu-id="f1e69-108">Flýtiskoðunareiningin er studd af einingum [vörusafns](product-collection-module-overview.md) og [leitarniðurstaðna](search-result-module.md).</span><span class="sxs-lookup"><span data-stu-id="f1e69-108">The quick view module is supported by the [product collection](product-collection-module-overview.md) and [search results](search-result-module.md) modules.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f1e69-109">Flýtiskoðunareiningin er í boði frá og með Commerce-útgáfu 10.0.17.</span><span class="sxs-lookup"><span data-stu-id="f1e69-109">The quick view module is available as of the Commerce version 10.0.17 release.</span></span>

<span data-ttu-id="f1e69-110">Eftirfarandi mynd sýnir dæmi um flýtiskoðunareiningu á listasíðu afurða.</span><span class="sxs-lookup"><span data-stu-id="f1e69-110">The following illustration shows an example of a quick view module on a product list page.</span></span>

![Dæmi um flýtiskoðunareiningu á listasíðu afurða](./media/ecommerce-quickview.PNG)

## <a name="module-properties"></a><span data-ttu-id="f1e69-112">Eiginleikar einingar</span><span class="sxs-lookup"><span data-stu-id="f1e69-112">Module properties</span></span>

<span data-ttu-id="f1e69-113">Flýtiskoðunareiningin styður sumar af sömu aðgerðum kaupgluggaeiningarinnar.</span><span class="sxs-lookup"><span data-stu-id="f1e69-113">The quick view module supports some of the same functions as the buy box module.</span></span> <span data-ttu-id="f1e69-114">Þess vegna líkjast eiginleikar flýtiskoðunareiningar eiginleikum kaupgluggaeiningar.</span><span class="sxs-lookup"><span data-stu-id="f1e69-114">Therefore, the properties of a quick view module resemble the properties of a buy box module.</span></span>

| <span data-ttu-id="f1e69-115">Eiginleiki</span><span class="sxs-lookup"><span data-stu-id="f1e69-115">Property</span></span> | <span data-ttu-id="f1e69-116">Gildi</span><span class="sxs-lookup"><span data-stu-id="f1e69-116">Values</span></span> | <span data-ttu-id="f1e69-117">lýsing</span><span class="sxs-lookup"><span data-stu-id="f1e69-117">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="f1e69-118">Merki fyrirsagnar</span><span class="sxs-lookup"><span data-stu-id="f1e69-118">Heading tag</span></span> | <span data-ttu-id="f1e69-119">**H1**, **H2**, **H3**, **H4**, **H5** eða **H6**</span><span class="sxs-lookup"><span data-stu-id="f1e69-119">**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**</span></span> | <span data-ttu-id="f1e69-120">Þessi eiginleiki skilgreinir merki fyrirsagna fyrir afurðarheitið.</span><span class="sxs-lookup"><span data-stu-id="f1e69-120">This property defines the heading tag for the product title.</span></span> <span data-ttu-id="f1e69-121">Ef flýtiskoðunareiningin er efst á síðunni ætti að stilla þennan eiginleika á **H1** til að uppfylla aðgengisstaðla.</span><span class="sxs-lookup"><span data-stu-id="f1e69-121">If the quick view module is at the top of the page, this property should be set to **H1** to meet accessibility standards.</span></span> |
| <span data-ttu-id="f1e69-122">Leyfa sérsniðið verð</span><span class="sxs-lookup"><span data-stu-id="f1e69-122">Allow custom price</span></span> | <span data-ttu-id="f1e69-123">**Satt** eða **Ósatt**</span><span class="sxs-lookup"><span data-stu-id="f1e69-123">**True** or **False**</span></span> | <span data-ttu-id="f1e69-124">Ef þessi eiginleiki er stilltur á **Satt** getur notandinn fært inn sérsniðið verð.</span><span class="sxs-lookup"><span data-stu-id="f1e69-124">If this property is set to **True**, the user can enter a custom price.</span></span> |
| <span data-ttu-id="f1e69-125">Lágmarksverð</span><span class="sxs-lookup"><span data-stu-id="f1e69-125">Minimum price</span></span> | <span data-ttu-id="f1e69-126">Heiltala</span><span class="sxs-lookup"><span data-stu-id="f1e69-126">Integer</span></span> | <span data-ttu-id="f1e69-127">Þessi eiginleiki gildir aðeins ef eiginleikinn **Leyfa sérsniðið verð** er stilltur á **Satt**.</span><span class="sxs-lookup"><span data-stu-id="f1e69-127">This property is applicable only if the **Allow custom price** property is set to **True**.</span></span> <span data-ttu-id="f1e69-128">Hann skilgreinir lágmarksverðið sem notandi getur slegið inn (t.d. $1).</span><span class="sxs-lookup"><span data-stu-id="f1e69-128">It defines the minimum price that the user can enter (for example, $1).</span></span> |
| <span data-ttu-id="f1e69-129">Hámarksverð</span><span class="sxs-lookup"><span data-stu-id="f1e69-129">Maximum price</span></span> | <span data-ttu-id="f1e69-130">Heiltala</span><span class="sxs-lookup"><span data-stu-id="f1e69-130">Integer</span></span> | <span data-ttu-id="f1e69-131">Þessi eiginleiki gildir aðeins ef eiginleikinn **Leyfa sérsniðið verð** er stilltur á **Satt**.</span><span class="sxs-lookup"><span data-stu-id="f1e69-131">This property is applicable only if the **Allow custom price** property is set to **True**.</span></span> <span data-ttu-id="f1e69-132">Hann skilgreinir hámarksverðið sem notandi getur slegið inn (t.d. $1000).</span><span class="sxs-lookup"><span data-stu-id="f1e69-132">It defines the maximum price that the user can enter (for example, $1,000).</span></span> |

## <a name="commerce-site-builder-settings"></a><span data-ttu-id="f1e69-133">Stillingar Commerce-vefsmiðs</span><span class="sxs-lookup"><span data-stu-id="f1e69-133">Commerce site builder settings</span></span>

<span data-ttu-id="f1e69-134">Líkt og kaupgluggaeiningin fer flýtiskoðunareiningin eftir stillingunum á **Stillingar svæðis \> Viðbætur \> Bæta afurð við körfu**.</span><span class="sxs-lookup"><span data-stu-id="f1e69-134">Like the buy box module, the quick view module respects the settings at **Site Settings \> Extensions \> Add product to cart**.</span></span> <span data-ttu-id="f1e69-135">Hins vegar er stillingin **Fara á körfusíðu** hunsuð vegna þess að hún er ekki í samræmi við tilgang flýtiskoðunareiningarinnar, sem er að gera notendum kleift að fletta í mörgum afurðum á listasíðu og bæta þeim við körfuna án þess að fara af listasíðunni.</span><span class="sxs-lookup"><span data-stu-id="f1e69-135">However, the **Navigate to cart page** setting is ignored, because it's inconsistent with the purpose of the quick view module, which is to enable users to browse multiple products on a list page and add them to the cart without moving away from the list page.</span></span>

## <a name="add-a-quick-view-module-to-a-product-collection-module"></a><span data-ttu-id="f1e69-136">Bæta flýtiskoðunareiningu við vörusafnseiningu</span><span class="sxs-lookup"><span data-stu-id="f1e69-136">Add a quick view module to a product collection module</span></span>

<span data-ttu-id="f1e69-137">Hægt er að bæta flýtiskoðunareiningu við einingar vörusafns og leitarniðurstaðna.</span><span class="sxs-lookup"><span data-stu-id="f1e69-137">A quick view module can be added to the product collection and search results modules.</span></span>

<span data-ttu-id="f1e69-138">Til að bæta flýtiskoðunareiningu við vörusafnseiningu í Commerce-vefsmið skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="f1e69-138">To add a quick view module to a product collection module in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="f1e69-139">Opnið **Síður** og veljið síðan heimasíðuna fyrir Fabrikam-svæðið.</span><span class="sxs-lookup"><span data-stu-id="f1e69-139">Go to **Pages**, and then select the home page for the Fabrikam site.</span></span>
1. <span data-ttu-id="f1e69-140">Farið í einhverja einingu **Vörusafns** á heimasíðunni, veljið úrfellingarmerkið (**...**) og veljið síðan **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="f1e69-140">Go to any **Product Collection** module on the homepage, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="f1e69-141">Í glugganum **Bæta við einingu** skal velja eininguna **Flýtiskoðun** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="f1e69-141">In the **Add Module** dialog box, select the **Quick View** module, and then select **OK**.</span></span>
1. <span data-ttu-id="f1e69-142">Á aðgerðasvæði einingarinnar **Flýtiskoðun** skal velja **Fyrirsögn**.</span><span class="sxs-lookup"><span data-stu-id="f1e69-142">In the properties pane of the **Quick View** module, select **Heading**.</span></span> <span data-ttu-id="f1e69-143">Í svarglugganum **Fyrirsögn** skal stilla reitinn **Fyrirsagnarstig** á **H2** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="f1e69-143">In the **Heading** dialog box, set the **Heading Level** field to **H2**, and then select **OK**.</span></span>
1. <span data-ttu-id="f1e69-144">Veldu **Vista**, síðan **Ljúka við breytingar** til að skila síðunni og veldu síðan **Birta** til að birta hana.</span><span class="sxs-lookup"><span data-stu-id="f1e69-144">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f1e69-145">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="f1e69-145">Additional resources</span></span>

[<span data-ttu-id="f1e69-146">Yfirlit einingasafns</span><span class="sxs-lookup"><span data-stu-id="f1e69-146">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="f1e69-147">Kaupgluggaeining</span><span class="sxs-lookup"><span data-stu-id="f1e69-147">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="f1e69-148">Afurðasafnseining</span><span class="sxs-lookup"><span data-stu-id="f1e69-148">Product collection module</span></span>](product-collection-module-overview.md)

[<span data-ttu-id="f1e69-149">Leitarniðurstöðueining</span><span class="sxs-lookup"><span data-stu-id="f1e69-149">Search results module</span></span>](search-result-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]