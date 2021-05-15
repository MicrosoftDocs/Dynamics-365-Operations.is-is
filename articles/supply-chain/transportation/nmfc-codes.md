---
title: Kóðar fyrir innlenda flokkun farmflutnings með ökutækjum (NMFC)
description: Í þessu efnisatriði er lýst hvernig á að vinna með kóða fyrir innlenda flokkun farmflutnings með ökutækjum (NMFC) í Microsoft Dynamics 365 Supply Chain Management
author: Henrikan
ms.date: 04/22/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-22
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 0307437d3868f7ac34fa16a0913907a046ac14d4
ms.sourcegitcommit: 636c1bf096a8666a551b67e898da1f48feb9a187
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/26/2021
ms.locfileid: "5941883"
---
# <a name="national-motor-freight-classification-nmfc-codes"></a><span data-ttu-id="3afaf-103">Kóðar fyrir innlenda flokkun farmflutnings með ökutækjum (NMFC)</span><span class="sxs-lookup"><span data-stu-id="3afaf-103">National Motor Freight Classification (NMFC) codes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3afaf-104">Kóðar fyrir innlenda flokkun farmflutnings með ökutækjum (NMFC) auðvelda þér að flokka vörur sem hægt er að senda.</span><span class="sxs-lookup"><span data-stu-id="3afaf-104">National Motor Freight Classification (NMFC) codes help you classify items that can be shipped.</span></span> <span data-ttu-id="3afaf-105">NMFC-kóðinn er merking sem er notuð til að flokka vörur.</span><span class="sxs-lookup"><span data-stu-id="3afaf-105">The NMFC code is a designation that is used to group commodities.</span></span> <span data-ttu-id="3afaf-106">Þeir gera flutningafyrirtækjum kleift að meta vörur fyrir sendingu með því að flokka vörur út frá þáttum eins og hvort passi í vörubíl, vandamál með hleðsluna, vandamál með meðhöndlun og lítið geymsluþol.</span><span class="sxs-lookup"><span data-stu-id="3afaf-106">It enables transport companies to evaluate goods for shipment by classifying items based on considerations such as truck fit, loading issues, handling issues, and perishability.</span></span> <span data-ttu-id="3afaf-107">Varningi er flokkað í einn af 18 farmklösum með því að nota talnasvið frá 50 til 500.</span><span class="sxs-lookup"><span data-stu-id="3afaf-107">Commodities are grouped into one of 18 freight classes by using a range of numbers from 50 to 500.</span></span> <span data-ttu-id="3afaf-108">Klasinn sem varningurinn er flokkaður í byggir á mati á fjórum einkennandi þáttum flutninga: þéttleika, hleðslumöguleika, meðhöndlun og ábyrgð.</span><span class="sxs-lookup"><span data-stu-id="3afaf-108">The class that a commodity is grouped into is based on an evaluation of four transportation characteristics: density, stowability, handling, and liability.</span></span> <span data-ttu-id="3afaf-109">Saman staðfesta þessir eiginleikar flutningshæfni vörunnar.</span><span class="sxs-lookup"><span data-stu-id="3afaf-109">Together, these characteristics establish the commodity's transportability.</span></span>

<span data-ttu-id="3afaf-110">NMFC-kóði er tengdur við allar vörur sem eru minna en fullhlaðinn trukkur.</span><span class="sxs-lookup"><span data-stu-id="3afaf-110">An NMFC code is associated with every less than truckload (LTL) shipping item.</span></span> <span data-ttu-id="3afaf-111">Til dæmis gæti fartölvu verið úthlutað NMFC sem er flokkað sem 2,5 en rafmagnssnúrum gætu aftur á móti verið úthlutað NMFC sem er flokkað sem 65.</span><span class="sxs-lookup"><span data-stu-id="3afaf-111">For example, a laptop might be assigned an NMFC that is classed at 2.5, whereas electrical cords might be assigned an NMFC that is classed at 65.</span></span>

<span data-ttu-id="3afaf-112">Þessi eiginleiki getur hjálpað starfsmönnum að nota NMFC-kóða til að flokka LTL-sendingarhluti.</span><span class="sxs-lookup"><span data-stu-id="3afaf-112">This feature can help workers use NMFC codes to classify LTL shipping items.</span></span> <span data-ttu-id="3afaf-113">Hér eru nokkur dæmi:</span><span class="sxs-lookup"><span data-stu-id="3afaf-113">Here are some examples:</span></span>

- <span data-ttu-id="3afaf-114">Ef fyrirtækið þitt setur vörulýsingu á farmbréf (BOL) mun flutningsfyrirtækið hafa einhverja hugmynd um hver farmurinn er.</span><span class="sxs-lookup"><span data-stu-id="3afaf-114">If your company includes a freight description on the bill of lading (BOL), the carrier will have some idea what the freight is.</span></span> <span data-ttu-id="3afaf-115">Farmur er mikilvæg flokkun vegna þess að mörg flutningsfyrirtæki byggja allt viðskiptalíkan sitt á farmgerðirnar sem þau senda.</span><span class="sxs-lookup"><span data-stu-id="3afaf-115">Freight is an important classification because many transportation companies base their whole business model on the types of freight that they ship.</span></span>
- <span data-ttu-id="3afaf-116">Þessi flokkun gæti verið nauðsynleg fyrir fyrirtækið þitt þar sem hún er notuð til að ákvarða kostnað við tiltekinn farm.</span><span class="sxs-lookup"><span data-stu-id="3afaf-116">This classification might be essential to your company because it's used to determine the cost of a given load.</span></span>
- <span data-ttu-id="3afaf-117">Fyrirtækið þitt getur greint arðsemi LTL-vörustjórnunar og flutningafyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="3afaf-117">Your company can identify the profitability of an LTL logistics and transportation company.</span></span>

<span data-ttu-id="3afaf-118">Í þessu efnisatriði er lýst hvernig á að vinna með NMFC-kóða í Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="3afaf-118">This topic describes how to work with NMFC codes in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="3afaf-119">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="3afaf-119">Prerequisites</span></span>

<span data-ttu-id="3afaf-120">Áður en hægt er að stofna NMFC-kóða þarf að setja upp alla LTL-farmklasa sem þarf að varpa í þá.</span><span class="sxs-lookup"><span data-stu-id="3afaf-120">Before you can create NMFC codes, you must set up all the LTL freight classes that must be mapped to them.</span></span> <span data-ttu-id="3afaf-121">LTL-farmklasar standa fyrir flokka af vörum þar sem NMFC-kóðar tengjast tilteknum varningi í hverjum þessarar 18 farmklasa.</span><span class="sxs-lookup"><span data-stu-id="3afaf-121">LTL freight classes represent categories of items, whereas NMFC codes are related to specific commodities in each of the 18 freight classes.</span></span> <span data-ttu-id="3afaf-122">Frekari upplýsingar um hvernig á að vinna með LTL-klasa er að finna í [Klasar sem eru minni en fullhlaðinn trukkur (LTL)](ltl-class.md).</span><span class="sxs-lookup"><span data-stu-id="3afaf-122">For more information about how to work with LTL classes, see [Less than truckload (LTL) classes](ltl-class.md).</span></span>

## <a name="create-an-nmfc-code"></a><span data-ttu-id="3afaf-123">Búa til NMFC-kóða</span><span class="sxs-lookup"><span data-stu-id="3afaf-123">Create an NMFC code</span></span>

<span data-ttu-id="3afaf-124">Til að búa til NMFC-kóða skal fylgja eftirfarandi skrefum.</span><span class="sxs-lookup"><span data-stu-id="3afaf-124">To create an NMFC code, follow these steps.</span></span>

1. <span data-ttu-id="3afaf-125">Fylgið einu af eftirfarandi skrefum:</span><span class="sxs-lookup"><span data-stu-id="3afaf-125">Follow one of these steps:</span></span>

    - <span data-ttu-id="3afaf-126">Farið í **Vöruhúsakerfi \> Uppsetning \> Birgðir \> NMFC-kóðar**.</span><span class="sxs-lookup"><span data-stu-id="3afaf-126">Go to **Warehouse management \> Setup \> Inventory \> NMFC codes**.</span></span>
    - <span data-ttu-id="3afaf-127">Farið í **Flutningsstjórnun \> Uppsetning \> Flutningsstaðlar \> NMFC-kóðar**.</span><span class="sxs-lookup"><span data-stu-id="3afaf-127">Go to **Transportation management \> Setup \> Transportation standards \> NMFC codes**.</span></span>

1. <span data-ttu-id="3afaf-128">Veljið **Nýr** til að stofna NMFC-kóða.</span><span class="sxs-lookup"><span data-stu-id="3afaf-128">Select **New** to create an NMFC code.</span></span> <span data-ttu-id="3afaf-129">Stillið svo eftirfarandi reiti:</span><span class="sxs-lookup"><span data-stu-id="3afaf-129">Then set the following fields:</span></span>

    - <span data-ttu-id="3afaf-130">**NMFC-kóði** – Færið inn NMFC-kóða vörutegundarinnar.</span><span class="sxs-lookup"><span data-stu-id="3afaf-130">**NMFC code** – Enter the NMFC code for the commodity type.</span></span>
    - <span data-ttu-id="3afaf-131">**Heiti** – Færið inn heiti fyrir NMFC-kóðann.</span><span class="sxs-lookup"><span data-stu-id="3afaf-131">**Name** – Enter a name for the NMFC code.</span></span>
    - <span data-ttu-id="3afaf-132">**LTL-flokkur** – Veljið LTL flokkinn sem tengist NMFC kóðanum.</span><span class="sxs-lookup"><span data-stu-id="3afaf-132">**LTL class** – Select the LTL class that is associated with the NMFC code.</span></span>
    - <span data-ttu-id="3afaf-133">**Afgreiðslueining farmbréfs** – Skilgreinið sjálfgefna gerð meðhöndlunar fyrir sendinguna.</span><span class="sxs-lookup"><span data-stu-id="3afaf-133">**BOL handling unit** – Define the default handling type for the shipment.</span></span>

## <a name="example-set-up-nmfc-codes"></a><span data-ttu-id="3afaf-134">Dæmi: setja upp NMFC-kóða</span><span class="sxs-lookup"><span data-stu-id="3afaf-134">Example: Set up NMFC codes</span></span>

<span data-ttu-id="3afaf-135">Eftirfarandi dæmi sýnir hvernig á að setja upp tvo mismunandi NMFC-kóða sem hægt er að nota með mismunandi vörum.</span><span class="sxs-lookup"><span data-stu-id="3afaf-135">The following example shows how to set up two different NMFC codes that can be used with different products.</span></span>

1. <span data-ttu-id="3afaf-136">Farið í **Vöruhúsakerfi \> Uppsetning \> Birgðir \> NMFC-kóðar**.</span><span class="sxs-lookup"><span data-stu-id="3afaf-136">Go to **Warehouse management \> Setup \> Inventory \> NMFC codes**.</span></span>
1. <span data-ttu-id="3afaf-137">Í aðgerðarúðunni velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="3afaf-137">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="3afaf-138">Stilltu eftirfarandi gildi á nýju línunni:</span><span class="sxs-lookup"><span data-stu-id="3afaf-138">On the new line, set the following values:</span></span>

    - <span data-ttu-id="3afaf-139">**NMFC-kóði**: *92.5*</span><span class="sxs-lookup"><span data-stu-id="3afaf-139">**NMFC code:** *92.5*</span></span>
    - <span data-ttu-id="3afaf-140">**Heiti:** *Tölvur*</span><span class="sxs-lookup"><span data-stu-id="3afaf-140">**Name:** *Computers*</span></span>
    - <span data-ttu-id="3afaf-141">**LTL-flokkur:** *92.5*</span><span class="sxs-lookup"><span data-stu-id="3afaf-141">**LTL class:** *92.5*</span></span>
    - <span data-ttu-id="3afaf-142">**Afgreiðslueining farmbréfs:** *Eining*</span><span class="sxs-lookup"><span data-stu-id="3afaf-142">**BOL handling unit:** *Unit*</span></span>

1. <span data-ttu-id="3afaf-143">Í aðgerðarúðunni skal velja **Vista**.</span><span class="sxs-lookup"><span data-stu-id="3afaf-143">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="3afaf-144">Í aðgerðarúðunni velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="3afaf-144">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="3afaf-145">Stilltu eftirfarandi gildi á nýju línunni:</span><span class="sxs-lookup"><span data-stu-id="3afaf-145">On the new line, set the following values:</span></span>

    - <span data-ttu-id="3afaf-146">**NMFC-kóði:** *125*</span><span class="sxs-lookup"><span data-stu-id="3afaf-146">**NMFC code:** *125*</span></span>
    - <span data-ttu-id="3afaf-147">**Heiti:** *Símar*</span><span class="sxs-lookup"><span data-stu-id="3afaf-147">**Name:** *Phones*</span></span>
    - <span data-ttu-id="3afaf-148">**LTL-klasi:** *125*</span><span class="sxs-lookup"><span data-stu-id="3afaf-148">**LTL class:** *125*</span></span>
    - <span data-ttu-id="3afaf-149">**Afgreiðslueining farmbréfs:** *Eining*</span><span class="sxs-lookup"><span data-stu-id="3afaf-149">**BOL handling unit:** *Unit*</span></span>

1. <span data-ttu-id="3afaf-150">Í aðgerðarúðunni skal velja **Vista**.</span><span class="sxs-lookup"><span data-stu-id="3afaf-150">On the Action Pane, select **Save**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3afaf-151">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="3afaf-151">Additional resources</span></span>

- [<span data-ttu-id="3afaf-152">Klasar sem eru minni en fullhlaðinn trukkur (LTL)</span><span class="sxs-lookup"><span data-stu-id="3afaf-152">Less than truckload (LTL) classes</span></span>](ltl-class.md)
- [<span data-ttu-id="3afaf-153">Stofnun farmbréfs</span><span class="sxs-lookup"><span data-stu-id="3afaf-153">Create a bill of landing</span></span>](create-bill-of-lading.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
