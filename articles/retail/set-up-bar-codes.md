---
title: Setja upp strikamerki
description: "Þessi grein lýsir hvernig nota á strikamerki í Microsoft Dynamics 365 for Retail."
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15971
ms.assetid: 6b4b2ac2-0344-41aa-8818-62c30017d5ac
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: bfb47e653cc3ef36135fd7c4f60771a354699af7
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-bar-codes"></a><span data-ttu-id="e4b60-103">Uppsetning strikamerkja</span><span class="sxs-lookup"><span data-stu-id="e4b60-103">Set up bar codes</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="e4b60-104">Þessi grein lýsir hvernig nota á strikamerki í Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="e4b60-104">This article describes how to use bar codes in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="e4b60-105">Hægt er að nota strikamerki til að kaupa og selja vörur, rekja afurðarafbrigði og setja upp viðskiptavini og starfsfólk.</span><span class="sxs-lookup"><span data-stu-id="e4b60-105">You can use bar codes to purchase and sell products, track product variants, and set up customers and employees.</span></span> <span data-ttu-id="e4b60-106">Einnig er hægt að nota strikamerki til að gefa út og framselja afsláttarmiða, gjafakort, og kreditfæra minnisblöð.</span><span class="sxs-lookup"><span data-stu-id="e4b60-106">You can also use bar codes to issue and endorse coupons, gift cards, and credit memos.</span></span> <span data-ttu-id="e4b60-107">Hægt er að setja upp smásöluvörur með stöðluð strikamerki eða sérsniðin innanhúss-strikamerki.</span><span class="sxs-lookup"><span data-stu-id="e4b60-107">You can set up retail products so that they have standard bar codes or custom, in-house bar codes.</span></span> <span data-ttu-id="e4b60-108">Vörur geta haft fleiri en eitt strikamerki.</span><span class="sxs-lookup"><span data-stu-id="e4b60-108">Products can have more than one bar code.</span></span> <span data-ttu-id="e4b60-109">Til dæmis getur afurð haft mörg strikamerki ef hún kemur frá mismunandi framleiðendum eða ef hún hefur afbrigði sem eru byggð á stærð, stílum eða litum.</span><span class="sxs-lookup"><span data-stu-id="e4b60-109">For example, a product might have multiple bar codes if it comes from various manufacturers, or if it has variants that are based on size, style, or color.</span></span> <span data-ttu-id="e4b60-110">Strikamerki geta innihaldið þyngd vöru eða verð.</span><span class="sxs-lookup"><span data-stu-id="e4b60-110">Bar codes can include the weight or price of the product.</span></span> <span data-ttu-id="e4b60-111">Sniðmát fyrir strikamerki eru sniðmátin sem eru notuð til að búa til strikamerki.</span><span class="sxs-lookup"><span data-stu-id="e4b60-111">Bar code masks are templates that are used to create bar codes.</span></span> <span data-ttu-id="e4b60-112">**Athugið:** Þegar einstakt strikamerki er gefið hverri vöruvíddasamsetningu er hægt að skanna strikamerkið á afgreiðslukassa og leyfa forritinu að finna afbrigði afurðarinnar sem er seld.</span><span class="sxs-lookup"><span data-stu-id="e4b60-112">**Note:** If you assign a unique bar code to each variant combination, you can scan the bar code at the register and let the program determine which variant of the product is being sold.</span></span> <span data-ttu-id="e4b60-113">Einnig er hægt að halda utan um og skoða talnagögn um sölu eftir vöruvíddasamsetningu.</span><span class="sxs-lookup"><span data-stu-id="e4b60-113">You can also collect and view statistics about sales by variant.</span></span> <span data-ttu-id="e4b60-114">Hægt er að tengja hvern flokk stærðar, litar og stíls við einstakt númer sem auðkennir viðkomandi flokk í strikamerkinu.</span><span class="sxs-lookup"><span data-stu-id="e4b60-114">Each size, color, and style group can be assigned a unique number that identifies that group in the bar code.</span></span> <span data-ttu-id="e4b60-115">Dynamics 365 for Retail notar sniðmát strikamerkja til að búa sjálfkrafa til strikamerki fyrir hverja afbrigðissamsetningu.</span><span class="sxs-lookup"><span data-stu-id="e4b60-115">Dynamics 365 for Retail uses the bar code mask to automatically generate bar codes for each variant combination.</span></span> <span data-ttu-id="e4b60-116">Þetta getur verið afar gagnlegt þegar stærðir, litir og stílar eru mismunandi, þar sem samsetningum fjölgar umtalsvert með hverjum afbrigðiskóða sem bætt er við.</span><span class="sxs-lookup"><span data-stu-id="e4b60-116">This functionality can be useful if there are many sizes, colors, and styles, because the number of combinations increases significantly as each variant code is added.</span></span> <span data-ttu-id="e4b60-117">Ef þetta er ekki gert þarf að gefa hverri samsetningu strikamerki sem stendur fyrir afbrigði vöru.</span><span class="sxs-lookup"><span data-stu-id="e4b60-117">If this functionality isn't used, bar codes must be manually assigned to each combination that represents a product variant.</span></span> <span data-ttu-id="e4b60-118">Hægt er að búa til strikamerki handvirkt eða sjálfvirkt.</span><span class="sxs-lookup"><span data-stu-id="e4b60-118">You can create bar codes manually or automatically.</span></span> <span data-ttu-id="e4b60-119">Til að búa til strikamerki, ljúkið eftirfarandi verkefnum í þeirri röð sem þau eru talin upp.</span><span class="sxs-lookup"><span data-stu-id="e4b60-119">To create bar codes, complete the following tasks in the order in which they are listed.</span></span>

1.  <span data-ttu-id="e4b60-120">[Setja upp stafi fyrir sniðmát strikamerkja](set-up-bar-code-masks.md).</span><span class="sxs-lookup"><span data-stu-id="e4b60-120">[Set up bar code mask characters](set-up-bar-code-masks.md).</span></span>
2.  <span data-ttu-id="e4b60-121">[Setja upp sniðmát fyrir strikamerki](set-up-bar-code-masks.md).</span><span class="sxs-lookup"><span data-stu-id="e4b60-121">[Set up bar code masks](set-up-bar-code-masks.md).</span></span>
3.  <span data-ttu-id="e4b60-122">Skilgreina uppsetningar fyrir strikamerki.</span><span class="sxs-lookup"><span data-stu-id="e4b60-122">Configure bar code setups.</span></span>
4.  <span data-ttu-id="e4b60-123">Stofna strikamerki fyrir afurðir.</span><span class="sxs-lookup"><span data-stu-id="e4b60-123">Create bar codes for products.</span></span>


<a name="see-also"></a><span data-ttu-id="e4b60-124">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="e4b60-124">See also</span></span>
--------

[<span data-ttu-id="e4b60-125">Setja upp sniðmát fyrir strikamerki</span><span class="sxs-lookup"><span data-stu-id="e4b60-125">Set up bar code masks</span></span>](set-up-bar-code-masks.md)




