---
title: Skilgreina söluskatt fyrir pantanir á netinu
description: Þetta efnisatriði veitir yfirlit yfir val á VSK-flokki fyrir mismunandi gerðir pantana á netinu í Dynamics 365 Commerce.
author: gvrmohanreddy
manager: AnnBe
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: gmohanv
ms.search.validFrom: 2020-11-01
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 40c20bf13779f73289e43df21b763e1b864686a7
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/17/2020
ms.locfileid: "4530198"
---
# <a name="configure-sales-tax-for-online-orders"></a><span data-ttu-id="f336f-103">Skilgreina söluskatt fyrir pantanir á netinu</span><span class="sxs-lookup"><span data-stu-id="f336f-103">Configure sales tax for online orders</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="f336f-104">Þetta efnisatriði veitir yfirlit yfir val á VSK-flokki fyrir mismunandi gerðir pantana á netinu.</span><span class="sxs-lookup"><span data-stu-id="f336f-104">This topic provides an overview of sales tax group selection for different online order types.</span></span> 

<span data-ttu-id="f336f-105">Hugsanlega skal e-Commerce-rásin styðja valkosti eins og sendingu eða afhendingu pantana á netinu.</span><span class="sxs-lookup"><span data-stu-id="f336f-105">Your e-commerce channel may want to support options like delivery or pickup for online orders.</span></span> <span data-ttu-id="f336f-106">Notkun virðisaukaskatts miðast við val notenda þinna á netinu.</span><span class="sxs-lookup"><span data-stu-id="f336f-106">The sales tax applicability is based on the option selected by your online users.</span></span> <span data-ttu-id="f336f-107">Þegar viðskiptavinur vefsvæðis kýs að kaupa vöru á netinu og fær hana senda á heimilisfang, miðast virðisaukaskatturinn við VSK-flokk heimilisfangs viðtakanda viðskiptavinarins.</span><span class="sxs-lookup"><span data-stu-id="f336f-107">When a site customer chooses to buy an item online and gets it shipped to an address, the sales tax is determined based on the customer's shipping address tax group setting.</span></span> <span data-ttu-id="f336f-108">Þegar viðskiptavinur ákveður að sækja keypta vöru í verslun miðast virðisaukaskattur við VSK-flokk verslunarinnar þar sem varan er sótt.</span><span class="sxs-lookup"><span data-stu-id="f336f-108">When a customer opts to pick up a purchased item at a store, the sales tax is determined based on the pickup store's tax group setting.</span></span> 

## <a name="orders-shipped-to-a-customer-address"></a><span data-ttu-id="f336f-109">Pantanir sendar á heimilisfang viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="f336f-109">Orders shipped to a customer address</span></span> 

<span data-ttu-id="f336f-110">Almennt séð miðast skattar fyrir pantanir á netinu sem senda á heimilisföng viðskiptavinar við áfangastaðinn.</span><span class="sxs-lookup"><span data-stu-id="f336f-110">In general, taxes for online orders that ship to customer addresses are defined by the destination.</span></span> <span data-ttu-id="f336f-111">Sérhver VSK-flokkur inniheldur skattaskilgreiningu miðað við áfangastað smásölu þar sem fyrirtækið þitt getur skilgreint upplýsingar um áfangastað, eins og hérað/svæði, ríki, land og borg á stigveldisformi.</span><span class="sxs-lookup"><span data-stu-id="f336f-111">Every sales tax group has a retail destination-based tax configuration in which your business can define destination details such as county/region, state, county, and city in a hierarchical form.</span></span> <span data-ttu-id="f336f-112">Þegar pöntun á netinu berst notar Commerce-skattakerfið afhendingaraðsetur hvers línuatriðis pöntunarinnar og finnur VSK-flokka með samsvarandi skattaviðmið miðað við ákvörðunarstað.</span><span class="sxs-lookup"><span data-stu-id="f336f-112">When an online order is placed, the Commerce tax engine uses the delivery address of every line item in the order, and finds sales tax groups with matching destination-based tax criteria.</span></span> <span data-ttu-id="f336f-113">Þegar t.d. pöntun er gerð á netinu með afhendingaraðsetur línuatriðis í San Francisco Kaliforníu, finnur skattakerfið VSK-flokkinn og VSK-kóðann fyrir Kaliforníu og reiknar síðan út skattinn fyrir hvert línuatriði samkvæmt því.</span><span class="sxs-lookup"><span data-stu-id="f336f-113">For example, for an online order with a line item delivery address to San Francisco, California, the tax engine will find the sales tax group and sales tax code for California and then calculate tax for each line item accordingly.</span></span>  

## <a name="customer-based-tax-groups"></a><span data-ttu-id="f336f-114">Skattflokkar miðað við viðskiptavin</span><span class="sxs-lookup"><span data-stu-id="f336f-114">Customer-based tax groups</span></span>

<span data-ttu-id="f336f-115">Hægt er að grunnstilla skattflokka viðskiptavinar á tveimur stöðum í Commerce Headquarters:</span><span class="sxs-lookup"><span data-stu-id="f336f-115">In Commerce headquarters, there are two places where customer tax groups are configured:</span></span>

- <span data-ttu-id="f336f-116">**Prófíll viðskiptavinar**</span><span class="sxs-lookup"><span data-stu-id="f336f-116">**Customer's profile**</span></span>
- <span data-ttu-id="f336f-117">**Heimilisfang viðtakanda viðskiptavinar**</span><span class="sxs-lookup"><span data-stu-id="f336f-117">**Customer's shipping address**</span></span>

### <a name="if-a-customers-profile-has-a-tax-group-configured"></a><span data-ttu-id="f336f-118">Þegar skattflokkur er grunnstilltur í prófíl viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="f336f-118">If a customer's profile has a tax group configured</span></span>

<span data-ttu-id="f336f-119">Hugsanlega er skattaflokkur grunnstilltur fyrir færslu í prófíl viðskiptavinar í Commerce Headquarters, hins vegar notar skattakerfið ekki grunnstilltan skattaflokk í prófíl viðskiptavinarins fyrir pantanir á netinu.</span><span class="sxs-lookup"><span data-stu-id="f336f-119">A customer's profile record in headquarters may have a sales tax group configured, however for online orders the sales tax group configured in a customer's profile will not be used by the tax engine.</span></span> 

### <a name="if-a-customers-shipping-address-has-a-tax-group-configured"></a><span data-ttu-id="f336f-120">Þegar skattflokkur er grunnstilltur í heimilisfangi viðtakanda viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="f336f-120">If a customer's shipping address has a tax group configured</span></span>

<span data-ttu-id="f336f-121">Þegar aðsetursfærsla viðskiptavinar er með grunnstilltan skattflokk og pöntun á netinu (eða línuatriði) er sent til heimilisfangs viðtakanda viðskiptavinar, notar skattakerfið grunnstillta skattflokkinn í aðsetursfærslunni við skattaútreikninga.</span><span class="sxs-lookup"><span data-stu-id="f336f-121">If a customer's shipping address record has a tax group configured and an online order (or line item) is shipped to the customer's shipping address, the tax group configured in the customer's address record will be used by the tax engine for tax calculations.</span></span>

#### <a name="configure-a-tax-group-for-a-customers-shipping-address-record"></a><span data-ttu-id="f336f-122">Skilgreina skattflokk fyrir aðsetursfærslu viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="f336f-122">Configure a tax group for a customer's shipping address record</span></span>

<span data-ttu-id="f336f-123">Fylgdu eftirfarandi skrefum til að grunnstilla skattflokk fyrir aðsetursfærslu viðskiptavinar í Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="f336f-123">To configure a tax group for a customer's shipping address record in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="f336f-124">Opnaðu **Allir viðskiptavinir** og smelltu síðan á viðkomandi viðskiptavin.</span><span class="sxs-lookup"><span data-stu-id="f336f-124">Go to **All customers**, and then select the desired customer.</span></span> 
1. <span data-ttu-id="f336f-125">Á flýtiflipanum **Heimilisföng** er viðkomandi heimilisfang valið og síðan er smellt á **Fleiri valkostir \> Ítarlegt**.</span><span class="sxs-lookup"><span data-stu-id="f336f-125">On the **Addresses** FastTab, select the desired address, and then select **More options \> Advanced**.</span></span> 
1. <span data-ttu-id="f336f-126">Á flipanum **Almennt** á síðunni **Stjórna heimilisföngum** skal stilla VSK-gildið eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="f336f-126">Under the **General** tab on the **Manage addresses** page, set the sales tax value as needed.</span></span>

> [!NOTE]
> <span data-ttu-id="f336f-127">Skattflokkurinn er skilgreindur með því að nota afhendingaraðsetur pöntunarlínunnar og skattar miðað áfangastað eru grunnstilltir í skattflokknum sjálfum.</span><span class="sxs-lookup"><span data-stu-id="f336f-127">The tax group is defined using the delivery address of the order line and the destination-based taxes are configured at the tax group itself.</span></span> <span data-ttu-id="f336f-128">Frekari upplýsingar er að finna í [Setja upp skatta fyrir netverslanir á grundvelli áfangastaðar](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).</span><span class="sxs-lookup"><span data-stu-id="f336f-128">For more information, see [Set up taxes for online stores based on destination](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).</span></span>

## <a name="order-pickup-in-store"></a><span data-ttu-id="f336f-129">Pöntun sótt í verslun</span><span class="sxs-lookup"><span data-stu-id="f336f-129">Order pickup in store</span></span>

<span data-ttu-id="f336f-130">Þegar pöntun er skilgreind í pöntunarlínu sem sótt í verslun eða afhent í bíl, verður notaður skattflokkur verslunarinnar þar sem pöntunin er sótt.</span><span class="sxs-lookup"><span data-stu-id="f336f-130">For order lines with pickup in store or curbside pickup specified, the tax group from the selected pickup store will be applied.</span></span> <span data-ttu-id="f336f-131">Frekari upplýsingar um hvernig skal grunnstilla skattflokk fyrir tiltekna verslun er að finna í [Stilla aðra skattvalkosti fyrir verslanir](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).</span><span class="sxs-lookup"><span data-stu-id="f336f-131">For details about how to configure the tax group for a given store, see [Set other tax options for stores](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).</span></span>

> [!NOTE]
> <span data-ttu-id="f336f-132">Þegar pöntunarlína er grunnstillt sem sótt í verslun eru skattstillingar heimilisfangs viðskiptavinar (ef slíkar eru grunnstilltar) hunsaðar af skattkerfinu og notuð verður skattaskilgreining verslunarinnar þar sem pöntunin er sótt.</span><span class="sxs-lookup"><span data-stu-id="f336f-132">When an order line is picked up at a store, a customer's address tax settings (if set up) will be ignored by the tax engine and the pickup store's tax configuration will be applied.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="f336f-133">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="f336f-133">Additional resources</span></span>

[<span data-ttu-id="f336f-134">Yfirlit virðisaukaskatts</span><span class="sxs-lookup"><span data-stu-id="f336f-134">Sales tax overview</span></span>](https://docs.microsoft.com/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=/dynamics365/commerce/toc.json) 

[<span data-ttu-id="f336f-135">Útreikningsaðferðir VSK í upprunareitnum</span><span class="sxs-lookup"><span data-stu-id="f336f-135">Sales tax calculation methods in the Origin field</span></span>](https://docs.microsoft.com/dynamics365/finance/general-ledger/sales-tax-calculation-methods-origin-field?toc=/dynamics365/commerce/toc.json) 

[<span data-ttu-id="f336f-136"> Úthlutun og hnekking virðisaukaskatts</span><span class="sxs-lookup"><span data-stu-id="f336f-136">Sales tax assignment and overrides</span></span>](https://docs.microsoft.com/dynamics365/supply-chain/procurement/tasks/sales-tax-assignment-overrides?toc=/dynamics365/commerce/toc.json) 

[<span data-ttu-id="f336f-137">Valkostir heildarupphæðar og tímabilsútreikninga fyrir VSK-kóða</span><span class="sxs-lookup"><span data-stu-id="f336f-137">Whole amount and Interval calculation options for sales tax codes</span></span>](https://docs.microsoft.com/dynamics365/finance/general-ledger/whole-amount-interval-options-sales-tax-codes?toc=/dynamics365/commerce/toc.json) 

[<span data-ttu-id="f336f-138">Reikna út skattundanþágu</span><span class="sxs-lookup"><span data-stu-id="f336f-138">Calculation of tax exemption</span></span>](tax-exempt-price-inclusive.md) 

