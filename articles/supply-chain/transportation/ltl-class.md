---
title: Klasar sem eru minni en fullhlaðinn trukkur (LTL)
description: Í þessu efnisatriði er gerð grein fyrir klösum sem eru minna en fullhlaðinn trukkur (LTL) og útskýrt hvernig á að setja þá upp í Microsoft Dynamics 365 Supply Chain Management.
author: Henrikan
ms.date: 04/05/2021
ms.topic: article
ms.search.form: WHSLTLClass
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-05
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 295006cac0a67cd577809a1b62566de043ea55fb
ms.sourcegitcommit: 636c1bf096a8666a551b67e898da1f48feb9a187
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/26/2021
ms.locfileid: "5941811"
---
# <a name="less-than-truckload-ltl-classes"></a><span data-ttu-id="10715-103">Klasar sem eru minni en fullhlaðinn trukkur (LTL)</span><span class="sxs-lookup"><span data-stu-id="10715-103">Less than truckload (LTL) classes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="10715-104">Klasi sem er minna en fullhlaðinn trukkur (LTL) er klasi farmsendingar sem er notaður til að flokka vörur sem hægt er að senda.</span><span class="sxs-lookup"><span data-stu-id="10715-104">A less than truckload (LTL) class is a freight shipping class that is used to classify items that can be shipped.</span></span> <span data-ttu-id="10715-105">Almennt eru allar gerðir afurða eða vöru með kóða fyrir innlenda flokkun farmflutnings með ökutækjum (NMFC) sem samsvarar tilteknu númeri farmklasa fyrir LTL-sendingar.</span><span class="sxs-lookup"><span data-stu-id="10715-105">Generally, every type of product or commodity has a National Motor Freight Classification (NMFC) code that corresponds to a specific freight class number for LTL shipments.</span></span> <span data-ttu-id="10715-106">LTL-farmklasar standa fyrir flokka af vörum þar sem NMFC-kóðar tengjast tilteknum varningi í hverjum þessarar 18 farmklasa.</span><span class="sxs-lookup"><span data-stu-id="10715-106">LTL freight classes represent categories of items, whereas NMFC codes are related to specific commodities in each of the 18 freight classes.</span></span>

<span data-ttu-id="10715-107">Þessi eiginleiki gerir þér kleift að nota kerfið til að framkvæma eftirfarandi verk:</span><span class="sxs-lookup"><span data-stu-id="10715-107">This feature lets you use your system to perform the following tasks:</span></span>

- <span data-ttu-id="10715-108">Skilgreinið klasa LTL-farms sem eru notaðir í fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="10715-108">Define the LTL freight classes that are used at your company.</span></span>
- <span data-ttu-id="10715-109">Úthlutið hverjum LTL-klasa NMFC-kóða á síðunni **NMFC-kóðar**.</span><span class="sxs-lookup"><span data-stu-id="10715-109">Assign each LTL class to an NMFC code on the **NMFC Codes** page.</span></span> <span data-ttu-id="10715-110">Frekari upplýsingar er að finna í [Kóðar fyrir innlenda flokkun farmflutnings með ökutækjum (NMFC)](nmfc-codes.md).</span><span class="sxs-lookup"><span data-stu-id="10715-110">For more information, see [National Motor Freight Classification (NMFC) codes](nmfc-codes.md).</span></span>
- <span data-ttu-id="10715-111">Úthlutið NMFC-kóða (og þar af leiðandi tengdan LTL-kóða) á hverja afurð á síðunni **Afurðir**.</span><span class="sxs-lookup"><span data-stu-id="10715-111">Assign an NMFC code (and therefore its associated LTL code) to each product on the **Products** page.</span></span>
- <span data-ttu-id="10715-112">Leggðu nákvæmt mat á LTL-klasa hverrar afurðar sem NMFC-kóðanum er úthlutað til.</span><span class="sxs-lookup"><span data-stu-id="10715-112">Accurately assess the LTL class of each product that an NMFC code is assigned to.</span></span>
- <span data-ttu-id="10715-113">Takið ákvörðun um kröfur pökkunar fyrir hvern LTL-klasa með því að athuga alþjóðlega LTL-staðla.</span><span class="sxs-lookup"><span data-stu-id="10715-113">Determine packing requirements for each LTL class by checking the international LTL standards.</span></span> <span data-ttu-id="10715-114">Á þennan hátt er tryggt að vörurnar séu vel varðar og sendar á öruggan hátt.</span><span class="sxs-lookup"><span data-stu-id="10715-114">In this way, you ensure that your products will be well protected and safely shipped.</span></span>
- <span data-ttu-id="10715-115">Fáið nákvæmt mát á sendingu út frá LTL-farmklasa hverrar afurðar.</span><span class="sxs-lookup"><span data-stu-id="10715-115">Get accurate shipping estimates, based on the LTL freight class for each product.</span></span>

<span data-ttu-id="10715-116">Í þessu efnisatriði er lýst hvernig á að stofna LTL-klasa í Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="10715-116">This topic describes how to create LTL classes in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="create-an-ltl-class"></a><span data-ttu-id="10715-117">Stofna LTL-klasa</span><span class="sxs-lookup"><span data-stu-id="10715-117">Create an LTL class</span></span>

<span data-ttu-id="10715-118">Til að stofna LTL-flokk skal fylgja eftirfarandi skrefum.</span><span class="sxs-lookup"><span data-stu-id="10715-118">To create an LTL class, follow these steps.</span></span>

1. <span data-ttu-id="10715-119">Fylgið einu af eftirfarandi skrefum:</span><span class="sxs-lookup"><span data-stu-id="10715-119">Follow one of these steps:</span></span>

    - <span data-ttu-id="10715-120">Farið í **Vöruhúsakerfi \> Uppsetning \> Birgðir \> LTL-klasar**.</span><span class="sxs-lookup"><span data-stu-id="10715-120">Go to **Warehouse management \> Setup \> Inventory \> LTL classes**.</span></span>
    - <span data-ttu-id="10715-121">Farið í **Flutningsstjórnun \> Uppsetning \> Flutningsstaðlar \> LTL-klasar**.</span><span class="sxs-lookup"><span data-stu-id="10715-121">Go to **Transportation management \> Setup \> Transportation standards \> LTL classes**.</span></span>

2. <span data-ttu-id="10715-122">Á aðgerðasvæðinu skal velja **Nýtt** til að búa til LTL-flokk.</span><span class="sxs-lookup"><span data-stu-id="10715-122">On the Action Pane, select **New** to create an LTL class.</span></span> <span data-ttu-id="10715-123">Stillið svo eftirfarandi reiti:</span><span class="sxs-lookup"><span data-stu-id="10715-123">Then set the following fields:</span></span>

    - <span data-ttu-id="10715-124">**LTL-klasi** – Sláið inn innra LTL-klasakenni fyrirtækisins fyrir vörutegundina.</span><span class="sxs-lookup"><span data-stu-id="10715-124">**LTL class** – Enter your company's internal LTL class identifier (ID) for the commodity type.</span></span> <span data-ttu-id="10715-125">Flest fyrirtæki nota alþjóðlegan staðal.</span><span class="sxs-lookup"><span data-stu-id="10715-125">Most companies use the international standard.</span></span> <span data-ttu-id="10715-126">Í slíku tilfelli mun gildi þessa svæðis samsvara gildi svæðisins **Flokkur**.</span><span class="sxs-lookup"><span data-stu-id="10715-126">In that case, the value of this field will match the value of the **Class** field.</span></span> <span data-ttu-id="10715-127">Ef fyrirtækið notar sinn eigin staðal er hins vegar færður inn kóði sem er í samræmi við þann staðal.</span><span class="sxs-lookup"><span data-stu-id="10715-127">However, if your company uses its own standard, enter a code that conforms to that standard.</span></span>
    - <span data-ttu-id="10715-128">**Heiti** – Færið inn lýsandi heiti sem hjálpar ykkur og öðrum notendum að velja réttan LTL-klasa fyrir hvern NMFC-kóða.</span><span class="sxs-lookup"><span data-stu-id="10715-128">**Name** – Enter a descriptive name that will help you and other users select the correct LTL class for each NMFC code.</span></span>
    - <span data-ttu-id="10715-129">**Klasi** – Færið inn alþjóðlegan staðal LTL-klasakennis fyrir vörutegundina.</span><span class="sxs-lookup"><span data-stu-id="10715-129">**Class** – Enter the international standard LTL class ID for the commodity type.</span></span> <span data-ttu-id="10715-130">Kóðinn sem færður er hér inn verður að vera í samræmi við opinberan staðal.</span><span class="sxs-lookup"><span data-stu-id="10715-130">The code that you enter here must conform to the official standard.</span></span>

## <a name="example-set-up-ltl-classes"></a><span data-ttu-id="10715-131">Dæmi: setja upp LTL-flokka</span><span class="sxs-lookup"><span data-stu-id="10715-131">Example: Set up LTL classes</span></span>

<span data-ttu-id="10715-132">Eftirfarandi dæmi sýnir hvernig á að setja upp tvo mismunandi LTL-flokka sem hægt er að nota með mismunandi vörutegundum.</span><span class="sxs-lookup"><span data-stu-id="10715-132">The following example shows how to set up two different LTL classes that you can use with different types of products.</span></span>

1. <span data-ttu-id="10715-133">Farið í **Vöruhúsakerfi \> Uppsetning \> Birgðir \> LTL-klasar**.</span><span class="sxs-lookup"><span data-stu-id="10715-133">Go to **Warehouse management \> Setup \> Inventory \> LTL classes**.</span></span>
1. <span data-ttu-id="10715-134">Í aðgerðarúðunni velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="10715-134">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="10715-135">Stilltu eftirfarandi gildi á nýju línunni:</span><span class="sxs-lookup"><span data-stu-id="10715-135">On the new line, set the following values:</span></span>

    - <span data-ttu-id="10715-136">**LTL-flokkur:** *92.5*</span><span class="sxs-lookup"><span data-stu-id="10715-136">**LTL class:** *92.5*</span></span>
    - <span data-ttu-id="10715-137">**Heiti:** *Tölvur, skjáir, ísskápar*</span><span class="sxs-lookup"><span data-stu-id="10715-137">**Name:** *Computers, monitors, refrigerators*</span></span>
    - <span data-ttu-id="10715-138">**Flokkur:** *92.5*</span><span class="sxs-lookup"><span data-stu-id="10715-138">**Class:** *92.5*</span></span>

1. <span data-ttu-id="10715-139">Í aðgerðarúðunni skal velja **Vista**.</span><span class="sxs-lookup"><span data-stu-id="10715-139">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="10715-140">Í aðgerðarúðunni velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="10715-140">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="10715-141">Stilltu eftirfarandi gildi á nýju línunni:</span><span class="sxs-lookup"><span data-stu-id="10715-141">On the new line, set the following values:</span></span>

    - <span data-ttu-id="10715-142">**LTL-klasi:** *125*</span><span class="sxs-lookup"><span data-stu-id="10715-142">**LTL class:** *125*</span></span>
    - <span data-ttu-id="10715-143">**Heiti:** *Lítil heimilistæki*</span><span class="sxs-lookup"><span data-stu-id="10715-143">**Name:** *Small household appliances*</span></span>
    - <span data-ttu-id="10715-144">**Flokkur:** *125*</span><span class="sxs-lookup"><span data-stu-id="10715-144">**Class:** *125*</span></span>

1. <span data-ttu-id="10715-145">Í aðgerðarúðunni skal velja **Vista**.</span><span class="sxs-lookup"><span data-stu-id="10715-145">On the Action Pane, select **Save**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="10715-146">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="10715-146">Additional resources</span></span>

- [<span data-ttu-id="10715-147">Kóðar fyrir innlenda flokkun farmflutnings með ökutækjum (NMFC)</span><span class="sxs-lookup"><span data-stu-id="10715-147">National Motor Freight Classification (NMFC) codes</span></span>](nmfc-codes.md)
- [<span data-ttu-id="10715-148">Stofnun farmbréfs</span><span class="sxs-lookup"><span data-stu-id="10715-148">Create a bill of lading</span></span>](create-bill-of-lading.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
