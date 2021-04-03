---
title: Stofnun sjálfvirks viðskiptavinar
description: Þetta efnisatriði lýsir því hvernig á að stofna sjálfgefinn viðskiptavin til að nota þegar rás er stofnuð í Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: f988732549ce82919f02c87b320623d8d4218735
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477901"
---
# <a name="create-a-default-customer"></a><span data-ttu-id="3763f-103">Stofnun sjálfvirks viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="3763f-103">Create a default customer</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3763f-104">Þetta efnisatriði lýsir því hvernig á að stofna sjálfgefinn viðskiptavin til að nota þegar rás er stofnuð í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="3763f-104">This topic describes how to create a default customer to use when creating a channel in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="3763f-105">Þegar þú býrð til rás þarftu að bjóða upp á sjálfgefinn viðskiptavin.</span><span class="sxs-lookup"><span data-stu-id="3763f-105">When creating a channel, you will need to provide a default customer.</span></span> <span data-ttu-id="3763f-106">Auðvelt er að búa til sjálfgefinn viðskiptavin eftir að hafa búið til viðskiptavinahópinn og aðsetursbók viðskiptavinarins.</span><span class="sxs-lookup"><span data-stu-id="3763f-106">A default customer can easily be created after first creating the customer group and customer address book.</span></span>

## <a name="create-a-customer-group"></a><span data-ttu-id="3763f-107">Viðskiptavinaflokkur stofnaður</span><span class="sxs-lookup"><span data-stu-id="3763f-107">Create a customer group</span></span>

<span data-ttu-id="3763f-108">Ef engir viðskiptavinahópar hafa verið búnir til geturðu búið til einn.</span><span class="sxs-lookup"><span data-stu-id="3763f-108">If no customer groups exist yet, you can create one.</span></span> <span data-ttu-id="3763f-109">Dæmi geta verið hópar til að tákna mismunandi viðskiptavinahópa, svo sem heildsölu, smásölu, internet, starfsmenn, osfrv.</span><span class="sxs-lookup"><span data-stu-id="3763f-109">Examples may be groups to represent different customer groups, such as wholesale, retail, Internet, Employees, etc.</span></span>

<span data-ttu-id="3763f-110">Til að stofna viðskiptavinaflokk, skal fylgja eftirfarandi skrefum.</span><span class="sxs-lookup"><span data-stu-id="3763f-110">To create a customer group, follow these steps.</span></span>

1. <span data-ttu-id="3763f-111">Í yfirlitsglugganum ferðu í **Einingar \> Retail og Commerce \> Viðskiptavinir \> Viðskiptavinaflokkar**.</span><span class="sxs-lookup"><span data-stu-id="3763f-111">In the navigation pane, go to **Modules \> Retail and commerce \> Customers \> Customer groups**.</span></span>
1. <span data-ttu-id="3763f-112">Í aðgerðaglugganum velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="3763f-112">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="3763f-113">Í reitnum **Viðskiptavinaflokkur** slærðu inn kenni viðskiptavinahópsins.</span><span class="sxs-lookup"><span data-stu-id="3763f-113">In the **Customer group** box, enter a customer group ID.</span></span>
1. <span data-ttu-id="3763f-114">Í reitinn **Lýsing** ritarðu viðeigandi lýsingu.</span><span class="sxs-lookup"><span data-stu-id="3763f-114">In the **Description** box, enter an appropriate description.</span></span>
1. <span data-ttu-id="3763f-115">Í reitinn **Greiðsluskilmálar** ritarðu viðeigandi gildi.</span><span class="sxs-lookup"><span data-stu-id="3763f-115">In the **Terms of payment** box, enter an appropriate value.</span></span>
1. <span data-ttu-id="3763f-116">Í reitinn **Tími milli gjalddaga reiknings og greiðsludags** slærðu inn viðeigandi gildi.</span><span class="sxs-lookup"><span data-stu-id="3763f-116">In the **Time between invoice due date and payment date** box, enter an appropriate value.</span></span>
1. <span data-ttu-id="3763f-117">Í reitinn **Sjálfgefinn skattahópur** slærðu inn skattahóp ef við á.</span><span class="sxs-lookup"><span data-stu-id="3763f-117">In the **Default tax group** box, enter a tax group if applicable.</span></span>
1. <span data-ttu-id="3763f-118">Veldu gátreitinn **Verð eru með virðisaukaskatti** ef við á.</span><span class="sxs-lookup"><span data-stu-id="3763f-118">Select the **Prices include sales tax** check box if applicable.</span></span>
1. <span data-ttu-id="3763f-119">Í reitinn **Sjálfgefin ástæða afskrifta** slærðu inn viðeigandi gildi, ef við á.</span><span class="sxs-lookup"><span data-stu-id="3763f-119">In the **Default write-off reason** box, enter an appropriate value, if applicable.</span></span>

<span data-ttu-id="3763f-120">Eftirfarandi mynd sýnir nokkra stillta viðskiptavinahópa.</span><span class="sxs-lookup"><span data-stu-id="3763f-120">The following image shows several configured customer groups.</span></span>

![Viðskiptavinaflokkar](media/customer-groups.png)

## <a name="create-a-customer-address-book"></a><span data-ttu-id="3763f-122">Stofna aðsetursbók viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="3763f-122">Create a customer address book</span></span>

<span data-ttu-id="3763f-123">Viðskiptavinur þarf að tengjast heimilisfangaskrá.</span><span class="sxs-lookup"><span data-stu-id="3763f-123">A customer needs to be associated with an address book.</span></span> <span data-ttu-id="3763f-124">Ef hún hefur ekki enn verið stofnuð verður þú að stofna hana.</span><span class="sxs-lookup"><span data-stu-id="3763f-124">If one has not yet been created, then you will need to create one.</span></span>

<span data-ttu-id="3763f-125">Til að stofna aðsetursbók viðskiptavina skal fylgja eftirfarandi skrefum.</span><span class="sxs-lookup"><span data-stu-id="3763f-125">To create a customer address book, follow these steps.</span></span>

1. <span data-ttu-id="3763f-126">Í yfirlitsglugganum ferðu í **Einingar \> Retail og Commerce \> Uppsetning rásar \> Aðsetursbækur**.</span><span class="sxs-lookup"><span data-stu-id="3763f-126">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Address Books**.</span></span>
1. <span data-ttu-id="3763f-127">Í aðgerðaglugganum velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="3763f-127">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="3763f-128">Í reitnum **Heiti** færirðu inn heiti.</span><span class="sxs-lookup"><span data-stu-id="3763f-128">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="3763f-129">Í reitinn **Lýsing** skal færa inn lýsingu.</span><span class="sxs-lookup"><span data-stu-id="3763f-129">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="3763f-130">Í aðgerðaglugganum velurðu **Vista.**</span><span class="sxs-lookup"><span data-stu-id="3763f-130">On the action pane, select **Save**.</span></span>

<span data-ttu-id="3763f-131">Eftirfarandi mynd sýnir dæmi um aðsetursbók.</span><span class="sxs-lookup"><span data-stu-id="3763f-131">The following image shows an example address book.</span></span>

![Aðsetursbók](media/address-book.png)

## <a name="create-a-default-customer"></a><span data-ttu-id="3763f-133">Stofnun sjálfvirks viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="3763f-133">Create a default customer</span></span>

<span data-ttu-id="3763f-134">Til að stofna sjálfgefinn viðskiptavin skal fylgja eftirfarandi skrefum.</span><span class="sxs-lookup"><span data-stu-id="3763f-134">To create a default customer, follow these steps.</span></span>

1. <span data-ttu-id="3763f-135">Í yfirlitsglugganum ferðu í **Einingar \> Retail og Commerce \> Viðskiptavinir \> Allir viðskiptavinir**.</span><span class="sxs-lookup"><span data-stu-id="3763f-135">In the navigation pane, go to **Modules \> Retail and commerce \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="3763f-136">Í aðgerðaglugganum velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="3763f-136">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="3763f-137">Í fellilistanum **Gerð** velurðu „Einstaklingur”.</span><span class="sxs-lookup"><span data-stu-id="3763f-137">In the **Type** drop-down list, select "Person".</span></span>
1. <span data-ttu-id="3763f-138">Í fellilistanum **Viðskiptavinalykill** velurðu eða slærð inn lykilnúmer (til dæmis „100001“).</span><span class="sxs-lookup"><span data-stu-id="3763f-138">In the **Customer account** drop-down list, select or enter an account number (for example, "100001").</span></span>
1. <span data-ttu-id="3763f-139">Í fellilistanum **Fornafn** velurðu eða slærð inn nafn (til dæmis „Sjálfgefið“).</span><span class="sxs-lookup"><span data-stu-id="3763f-139">In the **First name** drop-down list, select or enter a name (for example, "Default").</span></span>
1. <span data-ttu-id="3763f-140">Í fellilistanum **Miðnafn** velurðu eða slærð inn nafn (til dæmis „Retail“).</span><span class="sxs-lookup"><span data-stu-id="3763f-140">In the **Middle name** drop-down list, select or enter a name (for example, "Retail").</span></span>
1. <span data-ttu-id="3763f-141">Í fellilistanum **Eftirnafn** velurðu eða slærð inn nafn (til dæmis „Customer“).</span><span class="sxs-lookup"><span data-stu-id="3763f-141">In the **Last name** drop-down list, select or enter a name (for example, "Customer").</span></span>
1. <span data-ttu-id="3763f-142">Í fellilistanum **Gjaldmiðill** velurðu eða slærð inn gjaldmiðil (til dæmis „USD“).</span><span class="sxs-lookup"><span data-stu-id="3763f-142">In the **Currency** drop-down list, select or enter a currency (for example, "USD").</span></span>
1. <span data-ttu-id="3763f-143">Í fellivalmyndinni **Gjaldmiðill** velurðu þann hóp viðskiptavina sem áður var stofnaður.</span><span class="sxs-lookup"><span data-stu-id="3763f-143">In the **Currency** drop-down list, select the customer group created previously.</span></span>
1. <span data-ttu-id="3763f-144">Í fellilistanum **Aðsetursbækur** velurðu fyrirliggjandi aðsetursbók viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="3763f-144">In the **Address books**  drop-down list, select an existing customer address book.</span></span>
1. <span data-ttu-id="3763f-145">Veldu **Vista** til að vista og fara aftur á upplýsingaskjá viðskiptavina fyrir nýja viðskiptavininn.</span><span class="sxs-lookup"><span data-stu-id="3763f-145">Select **Save** to save and return to customer details screen for the new customer.</span></span>

> [!NOTE]
> <span data-ttu-id="3763f-146">Það er ekki nauðsynlegt að bæta við heimilisfangi fyrir sjálfgefinn viðskiptavin.</span><span class="sxs-lookup"><span data-stu-id="3763f-146">It is not necessary to add an address for a default customer.</span></span>

<span data-ttu-id="3763f-147">Eftirfarandi mynd sýnir dæmi um stofnun viðskiptavinr.</span><span class="sxs-lookup"><span data-stu-id="3763f-147">The following image shows an example of customer creation.</span></span>

![Stofnun sjálfvirks viðskiptavinar](media/default-customer-creation.png)

<span data-ttu-id="3763f-149">Eftirfarandi mynd sýnir sjálfgefna stillingu viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="3763f-149">The following image shows a default customer configuration.</span></span>

![Dæmi um stillingu viðskiptavinar](media/default-customer-configuration1.png)

<span data-ttu-id="3763f-151">Flest sjálfgefin gildi á skjá viðskiptavinarins geta verið áfram, en tveimur gildum ætti að breyta.</span><span class="sxs-lookup"><span data-stu-id="3763f-151">Most of the default values on the customer detials screen can remain, but two values should be changed.</span></span>

1. <span data-ttu-id="3763f-152">Stækkaðu á upplýsingaskjá viðskiptavinarins **Sjálfgefin sölupöntun**.</span><span class="sxs-lookup"><span data-stu-id="3763f-152">On the customer details screen, expand **Sales order defaults**.</span></span>
1. <span data-ttu-id="3763f-153">Í fellilistanum **Vefsvæði** velurðu eða slærð inn fyrirframstillta síðu.</span><span class="sxs-lookup"><span data-stu-id="3763f-153">In the **Site** drop-down list, select or enter a pre-configured site.</span></span>
1. <span data-ttu-id="3763f-154">Í fellilistanum **Vöruhús** velurðu eða slærð inn fyrirframstillt vöruhús.</span><span class="sxs-lookup"><span data-stu-id="3763f-154">In the **Warehouse** drop-down list, and select or enter a pre-configured warehouse.</span></span>

<span data-ttu-id="3763f-155">Eftirfarandi mynd sýnir dæmi um stillingu viðskiptavinr.</span><span class="sxs-lookup"><span data-stu-id="3763f-155">The following image shows an example customer configuration.</span></span>

![Dæmi um stillingu viðskiptavinar](media/default-customer-configuration2.png)

## <a name="additional-resources"></a><span data-ttu-id="3763f-157">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="3763f-157">Additional resources</span></span>

[<span data-ttu-id="3763f-158">Yfirlit yfir rásir</span><span class="sxs-lookup"><span data-stu-id="3763f-158">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="3763f-159">Skilyrði fyrir rásauppsetningu</span><span class="sxs-lookup"><span data-stu-id="3763f-159">Channel setup prerequisites</span></span>](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
