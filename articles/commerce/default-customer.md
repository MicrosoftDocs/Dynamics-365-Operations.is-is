---
title: Stofnun sjálfvirks viðskiptavinar
description: Þetta efni lýsir því hvernig á að búa til sjálfgefinn viðskiptavin til að nota þegar stofnuð er rás í Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 1dd4dfc5b8ca7af66941d081b4c20be0f5d6001d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993401"
---
# <a name="create-a-default-customer"></a><span data-ttu-id="4a87d-103">Stofnun sjálfvirks viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="4a87d-103">Create a default customer</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="4a87d-104">Þetta efni lýsir því hvernig á að búa til sjálfgefinn viðskiptavin til að nota þegar stofnuð er rás í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="4a87d-104">This topic describes how to create a default customer to use when creating a channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="4a87d-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="4a87d-105">Overview</span></span>

<span data-ttu-id="4a87d-106">Þegar þú býrð til rás þarftu að bjóða upp á sjálfgefinn viðskiptavin.</span><span class="sxs-lookup"><span data-stu-id="4a87d-106">When creating a channel, you will need to provide a default customer.</span></span> <span data-ttu-id="4a87d-107">Auðvelt er að búa til sjálfgefinn viðskiptavin eftir að hafa búið til viðskiptavinahópinn og aðsetursbók viðskiptavinarins.</span><span class="sxs-lookup"><span data-stu-id="4a87d-107">A default customer can easily be created after first creating the customer group and customer address book.</span></span>

## <a name="create-a-customer-group"></a><span data-ttu-id="4a87d-108">Viðskiptavinaflokkur stofnaður</span><span class="sxs-lookup"><span data-stu-id="4a87d-108">Create a customer group</span></span>

<span data-ttu-id="4a87d-109">Ef engir viðskiptavinahópar hafa verið búnir til geturðu búið til einn.</span><span class="sxs-lookup"><span data-stu-id="4a87d-109">If no customer groups exist yet, you can create one.</span></span> <span data-ttu-id="4a87d-110">Dæmi geta verið hópar til að tákna mismunandi viðskiptavinahópa, svo sem heildsölu, smásölu, internet, starfsmenn, osfrv.</span><span class="sxs-lookup"><span data-stu-id="4a87d-110">Examples may be groups to represent different customer groups, such as wholesale, retail, Internet, Employees, etc.</span></span>

<span data-ttu-id="4a87d-111">Til að stofna viðskiptavinaflokk, skal fylgja eftirfarandi skrefum.</span><span class="sxs-lookup"><span data-stu-id="4a87d-111">To create a customer group, follow these steps.</span></span>

1. <span data-ttu-id="4a87d-112">Í yfirlitsglugganum ferðu í **Einingar \> Retail og Commerce \> Viðskiptavinir \> Viðskiptavinaflokkar**.</span><span class="sxs-lookup"><span data-stu-id="4a87d-112">In the navigation pane, go to **Modules \> Retail and commerce \> Customers \> Customer groups**.</span></span>
1. <span data-ttu-id="4a87d-113">Í aðgerðaglugganum velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="4a87d-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="4a87d-114">Í reitnum **Viðskiptavinaflokkur** slærðu inn kenni viðskiptavinahópsins.</span><span class="sxs-lookup"><span data-stu-id="4a87d-114">In the **Customer group** box, enter a customer group ID.</span></span>
1. <span data-ttu-id="4a87d-115">Í reitinn **Lýsing** ritarðu viðeigandi lýsingu.</span><span class="sxs-lookup"><span data-stu-id="4a87d-115">In the **Description** box, enter an appropriate description.</span></span>
1. <span data-ttu-id="4a87d-116">Í reitinn **Greiðsluskilmálar** ritarðu viðeigandi gildi.</span><span class="sxs-lookup"><span data-stu-id="4a87d-116">In the **Terms of payment** box, enter an appropriate value.</span></span>
1. <span data-ttu-id="4a87d-117">Í reitinn **Tími milli gjalddaga reiknings og greiðsludags** slærðu inn viðeigandi gildi.</span><span class="sxs-lookup"><span data-stu-id="4a87d-117">In the **Time between invoice due date and payment date** box, enter an appropriate value.</span></span>
1. <span data-ttu-id="4a87d-118">Í reitinn **Sjálfgefinn skattahópur** slærðu inn skattahóp ef við á.</span><span class="sxs-lookup"><span data-stu-id="4a87d-118">In the **Default tax group** box, enter a tax group if applicable.</span></span>
1. <span data-ttu-id="4a87d-119">Veldu gátreitinn **Verð eru með virðisaukaskatti** ef við á.</span><span class="sxs-lookup"><span data-stu-id="4a87d-119">Select the **Prices include sales tax** check box if applicable.</span></span>
1. <span data-ttu-id="4a87d-120">Í reitinn **Sjálfgefin ástæða afskrifta** slærðu inn viðeigandi gildi, ef við á.</span><span class="sxs-lookup"><span data-stu-id="4a87d-120">In the **Default write-off reason** box, enter an appropriate value, if applicable.</span></span>

<span data-ttu-id="4a87d-121">Eftirfarandi mynd sýnir nokkra stillta viðskiptavinahópa.</span><span class="sxs-lookup"><span data-stu-id="4a87d-121">The following image shows several configured customer groups.</span></span>

![Viðskiptavinaflokkar](media/customer-groups.png)

## <a name="create-a-customer-address-book"></a><span data-ttu-id="4a87d-123">Stofna aðsetursbók viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="4a87d-123">Create a customer address book</span></span>

<span data-ttu-id="4a87d-124">Viðskiptavinur þarf að tengjast heimilisfangaskrá.</span><span class="sxs-lookup"><span data-stu-id="4a87d-124">A customer needs to be associated with an address book.</span></span> <span data-ttu-id="4a87d-125">Ef hún hefur ekki enn verið stofnuð verður þú að stofna hana.</span><span class="sxs-lookup"><span data-stu-id="4a87d-125">If one has not yet been created, then you will need to create one.</span></span>

<span data-ttu-id="4a87d-126">Til að stofna aðsetursbók viðskiptavina skal fylgja eftirfarandi skrefum.</span><span class="sxs-lookup"><span data-stu-id="4a87d-126">To create a customer address book, follow these steps.</span></span>

1. <span data-ttu-id="4a87d-127">Í yfirlitsglugganum ferðu í **Einingar \> Retail og Commerce \> Uppsetning rásar \> Aðsetursbækur**.</span><span class="sxs-lookup"><span data-stu-id="4a87d-127">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Address Books**.</span></span>
1. <span data-ttu-id="4a87d-128">Í aðgerðaglugganum velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="4a87d-128">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="4a87d-129">Í reitnum **Heiti** færirðu inn heiti.</span><span class="sxs-lookup"><span data-stu-id="4a87d-129">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="4a87d-130">Í reitinn **Lýsing** skal færa inn lýsingu.</span><span class="sxs-lookup"><span data-stu-id="4a87d-130">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="4a87d-131">Í aðgerðaglugganum velurðu **Vista.**</span><span class="sxs-lookup"><span data-stu-id="4a87d-131">On the action pane, select **Save**.</span></span>

<span data-ttu-id="4a87d-132">Eftirfarandi mynd sýnir dæmi um aðsetursbók.</span><span class="sxs-lookup"><span data-stu-id="4a87d-132">The following image shows an example address book.</span></span>

![Aðsetursbók](media/address-book.png)

## <a name="create-a-default-customer"></a><span data-ttu-id="4a87d-134">Stofnun sjálfvirks viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="4a87d-134">Create a default customer</span></span>

<span data-ttu-id="4a87d-135">Til að stofna sjálfgefinn viðskiptavin skal fylgja eftirfarandi skrefum.</span><span class="sxs-lookup"><span data-stu-id="4a87d-135">To create a default customer, follow these steps.</span></span>

1. <span data-ttu-id="4a87d-136">Í yfirlitsglugganum ferðu í **Einingar \> Retail og Commerce \> Viðskiptavinir \> Allir viðskiptavinir**.</span><span class="sxs-lookup"><span data-stu-id="4a87d-136">In the navigation pane, go to **Modules \> Retail and commerce \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="4a87d-137">Í aðgerðaglugganum velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="4a87d-137">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="4a87d-138">Í fellilistanum **Gerð** velurðu „Einstaklingur”.</span><span class="sxs-lookup"><span data-stu-id="4a87d-138">In the **Type** drop-down list, select "Person".</span></span>
1. <span data-ttu-id="4a87d-139">Í fellilistanum **Viðskiptavinalykill** velurðu eða slærð inn lykilnúmer (til dæmis „100001“).</span><span class="sxs-lookup"><span data-stu-id="4a87d-139">In the **Customer account** drop-down list, select or enter an account number (for example, "100001").</span></span>
1. <span data-ttu-id="4a87d-140">Í fellilistanum **Fornafn** velurðu eða slærð inn nafn (til dæmis „Sjálfgefið“).</span><span class="sxs-lookup"><span data-stu-id="4a87d-140">In the **First name** drop-down list, select or enter a name (for example, "Default").</span></span>
1. <span data-ttu-id="4a87d-141">Í fellilistanum **Miðnafn** velurðu eða slærð inn nafn (til dæmis „Retail“).</span><span class="sxs-lookup"><span data-stu-id="4a87d-141">In the **Middle name** drop-down list, select or enter a name (for example, "Retail").</span></span>
1. <span data-ttu-id="4a87d-142">Í fellilistanum **Eftirnafn** velurðu eða slærð inn nafn (til dæmis „Customer“).</span><span class="sxs-lookup"><span data-stu-id="4a87d-142">In the **Last name** drop-down list, select or enter a name (for example, "Customer").</span></span>
1. <span data-ttu-id="4a87d-143">Í fellilistanum **Gjaldmiðill** velurðu eða slærð inn gjaldmiðil (til dæmis „USD“).</span><span class="sxs-lookup"><span data-stu-id="4a87d-143">In the **Currency** drop-down list, select or enter a currency (for example, "USD").</span></span>
1. <span data-ttu-id="4a87d-144">Í fellivalmyndinni **Gjaldmiðill** velurðu þann hóp viðskiptavina sem áður var stofnaður.</span><span class="sxs-lookup"><span data-stu-id="4a87d-144">In the **Currency** drop-down list, select the customer group created previously.</span></span>
1. <span data-ttu-id="4a87d-145">Í fellilistanum **Aðsetursbækur** velurðu fyrirliggjandi aðsetursbók viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="4a87d-145">In the **Address books**  drop-down list, select an existing customer address book.</span></span>
1. <span data-ttu-id="4a87d-146">Veldu **Vista** til að vista og fara aftur á upplýsingaskjá viðskiptavina fyrir nýja viðskiptavininn.</span><span class="sxs-lookup"><span data-stu-id="4a87d-146">Select **Save** to save and return to customer details screen for the new customer.</span></span>

> [!NOTE]
> <span data-ttu-id="4a87d-147">Það er ekki nauðsynlegt að bæta við heimilisfangi fyrir sjálfgefinn viðskiptavin.</span><span class="sxs-lookup"><span data-stu-id="4a87d-147">It is not necessary to add an address for a default customer.</span></span>

<span data-ttu-id="4a87d-148">Eftirfarandi mynd sýnir dæmi um stofnun viðskiptavinr.</span><span class="sxs-lookup"><span data-stu-id="4a87d-148">The following image shows an example of customer creation.</span></span>

![Stofnun sjálfvirks viðskiptavinar](media/default-customer-creation.png)

<span data-ttu-id="4a87d-150">Eftirfarandi mynd sýnir sjálfgefna stillingu viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="4a87d-150">The following image shows a default customer configuration.</span></span>

![Dæmi um stillingu viðskiptavinar](media/default-customer-configuration1.png)

<span data-ttu-id="4a87d-152">Flest sjálfgefin gildi á skjá viðskiptavinarins geta verið áfram, en tveimur gildum ætti að breyta.</span><span class="sxs-lookup"><span data-stu-id="4a87d-152">Most of the default values on the customer detials screen can remain, but two values should be changed.</span></span>

1. <span data-ttu-id="4a87d-153">Stækkaðu á upplýsingaskjá viðskiptavinarins **Sjálfgefin sölupöntun**.</span><span class="sxs-lookup"><span data-stu-id="4a87d-153">On the customer details screen, expand **Sales order defaults**.</span></span>
1. <span data-ttu-id="4a87d-154">Í fellilistanum **Vefsvæði** velurðu eða slærð inn fyrirframstillta síðu.</span><span class="sxs-lookup"><span data-stu-id="4a87d-154">In the **Site** drop-down list, select or enter a pre-configured site.</span></span>
1. <span data-ttu-id="4a87d-155">Í fellilistanum **Vöruhús** velurðu eða slærð inn fyrirframstillt vöruhús.</span><span class="sxs-lookup"><span data-stu-id="4a87d-155">In the **Warehouse** drop-down list, and select or enter a pre-configured warehouse.</span></span>

<span data-ttu-id="4a87d-156">Eftirfarandi mynd sýnir dæmi um stillingu viðskiptavinr.</span><span class="sxs-lookup"><span data-stu-id="4a87d-156">The following image shows an example customer configuration.</span></span>

![Dæmi um stillingu viðskiptavinar](media/default-customer-configuration2.png)

## <a name="additional-resources"></a><span data-ttu-id="4a87d-158">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="4a87d-158">Additional resources</span></span>

[<span data-ttu-id="4a87d-159">Yfirlit yfir rásir</span><span class="sxs-lookup"><span data-stu-id="4a87d-159">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="4a87d-160">Skilyrði fyrir rásauppsetningu</span><span class="sxs-lookup"><span data-stu-id="4a87d-160">Channel setup prerequisites</span></span>](channels-prerequisites.md)
