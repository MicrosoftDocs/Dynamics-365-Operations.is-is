---
title: Yfirlit yfir afurðarráðleggingar
description: Þetta efnisatriði veitir almennar upplýsingar um afurðatillögur. Afurðatillögur auðvelda viðskiptavinum að finna vörur sem þeir vilja á fljótlegan hátt og jafnvel vörur sem þeir ætluðu ekki upphaflega að kaupa.
author: Moonma
manager: AnnBe
ms.date: 10/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: moonma
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: eb369e6d1356ba13a2310d523b671ac57b9642bf
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770048"
---
# <a name="product-recommendations-overview"></a><span data-ttu-id="183a3-104">Yfirlit yfir afurðarráðleggingar</span><span class="sxs-lookup"><span data-stu-id="183a3-104">Product recommendations overview</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="183a3-105">Microsoft Dynamics 365 Commerce má nota til að sýna afurðatillögur á vefsíðu netverslunar og sölustað (POS) tækinu.</span><span class="sxs-lookup"><span data-stu-id="183a3-105">Microsoft Dynamics 365 Commerce can be used to show product recommendations on the e-Commerce website and point of sale (POS) device.</span></span> <span data-ttu-id="183a3-106">Afurðatillögur eru vörur sem viðskiptavinur gæti haft áhuga á.</span><span class="sxs-lookup"><span data-stu-id="183a3-106">Product recommendations are items that a customer might be interested in.</span></span> <span data-ttu-id="183a3-107">Ráðleggingarnar eru byggðar á kaupþróun annarra viðskiptavina í verslunum á netinu og verslunum sjálfum.</span><span class="sxs-lookup"><span data-stu-id="183a3-107">The recommendations are based on the purchase trends of other customers in online and brick-and-mortar stores.</span></span>

<span data-ttu-id="183a3-108">Afurðatillögur gera viðskiptavinum auðveldlega og fljótt að finna vörur sem þeir vilja á meðan þeir hafa reynslu sem þjónar þeim vel.</span><span class="sxs-lookup"><span data-stu-id="183a3-108">Product recommendations let customers easily and quickly find products that they want while they have an experience that serves them well.</span></span> <span data-ttu-id="183a3-109">Krosssölu og uppsölu er jafnvel hægt að nota til að hjálpa viðskiptavinum að finna fleiri vörur en þeir ætluðu upphaflega ekki að kaupa.</span><span class="sxs-lookup"><span data-stu-id="183a3-109">Cross-selling and upselling can even be used to help customers find additional products than they didn't originally intend to buy.</span></span> <span data-ttu-id="183a3-110">Þegar ráðleggingar eru notaðar til að hjálpa við uppgötvun vöru geta þau skapað fleiri viðskiptatækifæri, hjálpað til við að auka sölutekjur og jafnvel hjálpað til við að auka ánægju viðskiptavina og varðveisla.</span><span class="sxs-lookup"><span data-stu-id="183a3-110">When recommendations are used to help with product discovery, they can create more conversion opportunities, help increase sales revenue, and even help enhance customer satisfaction and retention.</span></span>

<span data-ttu-id="183a3-111">Í Commerce eru afurðatillögur knúnar af vélanámstækni Microsoft tilmæla í stórum stíl.</span><span class="sxs-lookup"><span data-stu-id="183a3-111">In Commerce, product recommendations are powered by Microsoft Recommendations machine learning technologies on a large scale.</span></span>


## <a name="scenarios"></a><span data-ttu-id="183a3-112">Sviðsmyndir</span><span class="sxs-lookup"><span data-stu-id="183a3-112">Scenarios</span></span>

<span data-ttu-id="183a3-113">Afurðatillögur eru í boði fyrir eftirfarandi aðstæður:</span><span class="sxs-lookup"><span data-stu-id="183a3-113">Product recommendations are available for the following scenarios:</span></span>

- <span data-ttu-id="183a3-114">**Á hvaða verslunarsíðu sem er til að vafra eða áfangasíðu í netverslun:** Ef viðskiptavinir eða starfsfólk verslunarinnar heimsækja verslunarsíðu getur meðmælavélin lagt til vörur í listunum **Nýtt**, **Mest selt** og **Vinsælt**.</span><span class="sxs-lookup"><span data-stu-id="183a3-114">**On any store page for browsing or landing page in e-Commerce:** If customers or store associates visit a store page, the recommendation engine can suggest products in the **New**, **Best Selling**, and **Trending** lists.</span></span>
- <span data-ttu-id="183a3-115">**Á síðu vöruupplýsinga:** Ef viðskiptavinir eða starfsfólk verslunar fer á síðuna **Upplýsingar um vöru** mælir tillöguvélin með viðbótarvörum sem einnig er líklegt að verði keyptar.</span><span class="sxs-lookup"><span data-stu-id="183a3-115">**On the Product details page:** If customers or store associates visit a **Product details** page, the recommendation engine suggests additional items that are also likely to be purchased.</span></span> <span data-ttu-id="183a3-116">Þessar vörur birtast á listanum **Fólki líkar einnig**.</span><span class="sxs-lookup"><span data-stu-id="183a3-116">These items appear in the **People also like** list.</span></span>
- <span data-ttu-id="183a3-117">**Á færslusíðunni eða greiðslusíðunni:** Tillöguvélin leggur til vörur, byggðar á öllum listanum yfir vörur í körfunni.</span><span class="sxs-lookup"><span data-stu-id="183a3-117">**On the Transaction page or the checkout page:** The recommendation engine suggests items, based on the whole list of items in the basket.</span></span> <span data-ttu-id="183a3-118">Þessir vörur birtast á listanum **Oft keypt saman**.</span><span class="sxs-lookup"><span data-stu-id="183a3-118">These items appear in the **Frequently bought together** list.</span></span>

## <a name="recommendation-service"></a><span data-ttu-id="183a3-119">Tillöguþjónusta</span><span class="sxs-lookup"><span data-stu-id="183a3-119">Recommendation service</span></span>

<span data-ttu-id="183a3-120">Afurðatillögur nota námstækni tilmælavélanna á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="183a3-120">Product recommendations use the Recommendations machine learning technologies in the following way:</span></span>

- <span data-ttu-id="183a3-121">Gögn á sniðinu sem tillöguþjónustan krefst eru fengin úr virknigagnagrunni Commerce og send í einingaverslunina.</span><span class="sxs-lookup"><span data-stu-id="183a3-121">Data in the format that the Recommendation service requires is extracted from the Commerce operational database and sent to the Entity store.</span></span>
- <span data-ttu-id="183a3-122">Tilmælaþjónustan notar gögnin til að þjálfa tillögulíkön fyrir listana **Fólki líkar einnig**, **Oft keypt saman**, **Nýtt**, **Mest selt** og **Vinsælt**.</span><span class="sxs-lookup"><span data-stu-id="183a3-122">The Recommendation service uses the data to train recommendation models for the **People also like**, **Frequently bought together**, **New**, **Best selling**, and **Trending** lists.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="183a3-123">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="183a3-123">Additional resources</span></span>

[<span data-ttu-id="183a3-124">Virkja ráðleggingar um afurðir</span><span class="sxs-lookup"><span data-stu-id="183a3-124">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="183a3-125">Búa til lista með sérvöldum afurðartillögum</span><span class="sxs-lookup"><span data-stu-id="183a3-125">Create curated product recommendation lists</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="183a3-126">Stjórna niðurstöðum afurðartillagna sem byggjast á AI-ML</span><span class="sxs-lookup"><span data-stu-id="183a3-126">Manage AI-ML-based product recommendation results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="183a3-127">Bæta við listum með afurðartillögum við síður</span><span class="sxs-lookup"><span data-stu-id="183a3-127">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)
