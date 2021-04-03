---
title: Skattar á pöntunum á netinu eru ekki rétt reiknaðir
description: Þetta efnisatriði býður upp á leiðsögn úrræðaleitar sem getur hjálpað til þegar skattar á pöntunum á netinu eru ekki rétt reiknaðir eða þegar skattflokkur sölulínu er ekki rétt stilltur.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 421df7545e285950ef8a3c4b753c8c6dc5f26422
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585371"
---
# <a name="taxes-on-online-orders-are-incorrectly-calculated"></a><span data-ttu-id="8efca-103">Skattar á pöntunum á netinu eru ekki rétt reiknaðir</span><span class="sxs-lookup"><span data-stu-id="8efca-103">Taxes on online orders are incorrectly calculated</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8efca-104">Þetta efnisatriði býður upp á leiðsögn úrræðaleitar sem getur hjálpað til þegar skattar á pöntunum á netinu eru ekki rétt reiknaðir eða þegar skattflokkur sölulínu er ekki rétt stilltur.</span><span class="sxs-lookup"><span data-stu-id="8efca-104">This topic provides troubleshooting guidance that can help when taxes on online orders are incorrectly calculated, or when the tax group on the sales line isn't correctly set.</span></span>

## <a name="description"></a><span data-ttu-id="8efca-105">lýsing</span><span class="sxs-lookup"><span data-stu-id="8efca-105">Description</span></span>

<span data-ttu-id="8efca-106">Þegar pöntun rafrænna viðskipta er gerð eru skattarnir rangt reiknaðir eða skattflokkur í sölulínunum er ekki rétt stilltur.</span><span class="sxs-lookup"><span data-stu-id="8efca-106">When an e-commerce order is placed, the taxes are incorrectly calculated, or the tax group on the sales line is incorrectly set.</span></span>

## <a name="resolution"></a><span data-ttu-id="8efca-107">Upplausn</span><span class="sxs-lookup"><span data-stu-id="8efca-107">Resolution</span></span>

### <a name="configure-the-sales-tax-for-a-retail-store-in-commerce-headquarters"></a><span data-ttu-id="8efca-108">Skilgreina söluskatt fyrir smásöluverslun í Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="8efca-108">Configure the sales tax for a retail store in Commerce headquarters</span></span>

<span data-ttu-id="8efca-109">Til að skilgreina söluskatt fyrir smásöluverslun í Commerce Headquarters skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="8efca-109">To configure the sales tax for a retail store in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="8efca-110">Farið í **Smásala og viðskipti \> Rásir \> Allar verslanir**.</span><span class="sxs-lookup"><span data-stu-id="8efca-110">Go to **Retail and Commerce \> Channels \> All stores**.</span></span>
1. <span data-ttu-id="8efca-111">Veljið verslunina þar sem á að skilgreina söluskattinn.</span><span class="sxs-lookup"><span data-stu-id="8efca-111">Select the store to configure sales tax for.</span></span>
1. <span data-ttu-id="8efca-112">Í flipanum **Almennt**, í hlutanum **Söluskattur**, skal skilgreina upplýsingar söluskatts fyrir verslunina.</span><span class="sxs-lookup"><span data-stu-id="8efca-112">On the **General** FastTab, in the **Sales tax** section, configure the sales tax information for the store.</span></span>

> [!NOTE]
> <span data-ttu-id="8efca-113">Fyrir afurð sem sótt er í verslun er notaður skattflokkur verslunarinnar sem er valin til að vera sótt úr.</span><span class="sxs-lookup"><span data-stu-id="8efca-113">For product pickup from a store, the tax group comes from the store that is selected for pickup.</span></span> <span data-ttu-id="8efca-114">Frekari upplýsingar er að finna í [Stilla aðra skattvalkosti fyrir verslanir](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).</span><span class="sxs-lookup"><span data-stu-id="8efca-114">For more information, see [Set other tax options for stores](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).</span></span>

### <a name="configure-the-sales-tax-for-a-customers-address-in-commerce-headquarters"></a><span data-ttu-id="8efca-115">Skilgreina söluskatt fyrir aðsetur viðskiptavinar í Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="8efca-115">Configure the sales tax for a customer's address in Commerce headquarters</span></span>

<span data-ttu-id="8efca-116">Til að skilgreina söluskatt fyrir aðsetur viðskiptavinar í Commerce Headquarters skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="8efca-116">To configure the sales tax for a customer's address in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="8efca-117">Farðu í **Viðskiptakröfur \> Viðskiptavinir \> Alla viðskiptavini**.</span><span class="sxs-lookup"><span data-stu-id="8efca-117">Go to **Accounts receivable \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="8efca-118">Veljið viðskiptavin þar sem á að skilgreina söluskatt.</span><span class="sxs-lookup"><span data-stu-id="8efca-118">Select the customer to configure sales taxes for.</span></span>
1. <span data-ttu-id="8efca-119">Í flýtiflipanum **Aðsetur** skal velja aðsetrið sem skilgreina á söluskatta fyrir, velja **Fleiri valkostir** og síðan velja **Ítarlegt**.</span><span class="sxs-lookup"><span data-stu-id="8efca-119">On the **Addresses** FastTab, select the address to configure sales taxes for, select **More options**, and then select **Advanced**.</span></span>
1. <span data-ttu-id="8efca-120">Í flýtiflipanum **Almennt** skal velja **Skattflokkinn**.</span><span class="sxs-lookup"><span data-stu-id="8efca-120">On the **General** FastTab, select the **Tax group**.</span></span>
1. <span data-ttu-id="8efca-121">Í reitnum **Söluskattur** skal velja viðeigandi gildi.</span><span class="sxs-lookup"><span data-stu-id="8efca-121">In the **Sales tax** field, select the appropriate value.</span></span>

> [!NOTE]
> <span data-ttu-id="8efca-122">Fyrir sendingar sem fela í sér söluskatt á aðsetri viðskiptavinar mun afhendingaraðsetur línunnar ákvarða skattflokk fyrir línuna.</span><span class="sxs-lookup"><span data-stu-id="8efca-122">For shipping that involves sales tax on the customer's address, the delivery address of the line determines the tax group for the line.</span></span> <span data-ttu-id="8efca-123">Ef viðskiptavinur er að senda til fyrirliggjandi aðseturs sem er með skattflokk sem búið er að skilgreina verður fyrirliggjandi skattflokkur notaður.</span><span class="sxs-lookup"><span data-stu-id="8efca-123">If the customer is shipping to an existing address that has a tax group that is already configured, the existing tax group will be used.</span></span> <span data-ttu-id="8efca-124">Sjálfgefið er að aðsetur eru ekki með skattflokk þegar þau eru búin til.</span><span class="sxs-lookup"><span data-stu-id="8efca-124">By default, addresses don't have a tax group when they are created.</span></span>

### <a name="configure-general-sales-tax-groups-in-commerce-headquarters"></a><span data-ttu-id="8efca-125">Skilgreina almenna söluskattflokka í Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="8efca-125">Configure general sales tax groups in Commerce headquarters</span></span>

<span data-ttu-id="8efca-126">Til að skilgreina almenna söluskattflokka í Commerce Headquarters skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="8efca-126">To configure general sales tax groups in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="8efca-127">Farið í **Skattur \> Óbeinir skattar \> Söluskattur \> Söluskattflokkur**.</span><span class="sxs-lookup"><span data-stu-id="8efca-127">Go to **Tax \> Indirect taxes \> Sales tax \> Sales tax group**.</span></span>
1. <span data-ttu-id="8efca-128">Í vinstri flettingunni skal velja skattflokkinn sem á að skilgreina.</span><span class="sxs-lookup"><span data-stu-id="8efca-128">In the left navigation, select the tax group to configure.</span></span>
1. <span data-ttu-id="8efca-129">Í flipanum **Skattur byggður á áfangastað smásölu** skal skilgreina skatta fyrir söluskattflokkinn.</span><span class="sxs-lookup"><span data-stu-id="8efca-129">On the **Retail destination based tax** FastTab, configure the taxes for the sales tax group.</span></span>

> [!NOTE]
> <span data-ttu-id="8efca-130">Fyrir sendingu sem felur ekki í sér söluskatt á aðsetri viðskiptavinar munu afhendingaraðsetur línunnar og skattur byggður á áfangastað sem er skilgreint fyrir skattflokkinn ákvarða skattflokkinn.</span><span class="sxs-lookup"><span data-stu-id="8efca-130">For shipping that doesn't involve sales tax on the customer's address, the delivery address of the line and the destination-based taxes that are configured for the tax group determine the tax group.</span></span> <span data-ttu-id="8efca-131">Frekari upplýsingar er að finna í [Setja upp skatta fyrir netverslanir á grundvelli áfangastaðar](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).</span><span class="sxs-lookup"><span data-stu-id="8efca-131">For more information, see [Set up taxes for online stores based on destination](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8efca-132">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="8efca-132">Additional resources</span></span>

[<span data-ttu-id="8efca-133">Skilgreina söluskatt fyrir pantanir á netinu</span><span class="sxs-lookup"><span data-stu-id="8efca-133">Configure sales tax for online orders</span></span>](../sales-tax-config.md)
