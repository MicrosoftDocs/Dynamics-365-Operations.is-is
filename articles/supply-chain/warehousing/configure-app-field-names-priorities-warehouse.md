---
title: Skilgreina reiti fyrir farsímaforrit vöruhúsakerfis
description: Þetta efnisatriði lýsir því hvernig á að skilgreina og grunnstilla heiti og forgangsröð reita sem sýndir eru í farsímaforrit vöruhúsakerfis.
author: MarkusFogelberg
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileAppField, WHSMobileAppFieldPriority
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269434
ms.assetid: 6cf3d7da-29bb-4d3d-aaf5-544ca9cc2980
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: c6ed726536085b836f4014c59ea8df4755577ab5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808823"
---
# <a name="configure-fields-for-the-warehouse-management-mobile-app"></a><span data-ttu-id="343e2-103">Skilgreina reiti fyrir farsímaforrit vöruhúsakerfis</span><span class="sxs-lookup"><span data-stu-id="343e2-103">Configure fields for the Warehouse Management mobile app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="343e2-104">Þetta efnisatriði lýsir því hvernig á að skilgreina og grunnstilla heiti og forgangsröð reita sem sýndir eru í farsímaforrit vöruhúsakerfis.</span><span class="sxs-lookup"><span data-stu-id="343e2-104">This topic describes how to define and configure names and priorities of fields shown in the Warehouse Management mobile app.</span></span>

> [!NOTE]
> <span data-ttu-id="343e2-105">Þetta efnisatriði á við aðgerðir í vöruhúsakerfi.</span><span class="sxs-lookup"><span data-stu-id="343e2-105">This topic applies to features in Warehouse management.</span></span> <span data-ttu-id="343e2-106">Það á ekki við um aðgerðir í birgðastjórnun.</span><span class="sxs-lookup"><span data-stu-id="343e2-106">It doesn’t apply to features in Inventory management.</span></span> <span data-ttu-id="343e2-107">Farsímaforrit vöruhúsakerfis er forrit sem hægt er að nota í framkvæmd vöruhúsaverkefna.</span><span class="sxs-lookup"><span data-stu-id="343e2-107">The Warehouse Management mobile app is an application that you can use to perform warehouse tasks.</span></span> <span data-ttu-id="343e2-108">Hægt er að skilgreina og grunnstilla reitarheiti sem eru notuð í forritinu, ásamt því að grunnstilla forgang sem reitarheitum ætti að vera úthlutað eftir.</span><span class="sxs-lookup"><span data-stu-id="343e2-108">You can define and configure the field names that are used in the app, as well as configure the priority to which the field names should be assigned.</span></span> <span data-ttu-id="343e2-109">Þetta efnisatriði útskýrir því hvernig á að skilgreina og grunnstilla svæðaheiti og forgang farsímaforrit vöruhúsakerfis og hvernig þau eru notuð í Warehousing.</span><span class="sxs-lookup"><span data-stu-id="343e2-109">This topic explains how to define and configure these Warehouse Management mobile app field names and priorities, and how they are used.</span></span>

## <a name="configure-warehouse-app-field-names"></a><span data-ttu-id="343e2-110">Grunnstilla reitarheiti vöruhúsaforrits</span><span class="sxs-lookup"><span data-stu-id="343e2-110">Configure warehouse app field names</span></span>

<span data-ttu-id="343e2-111">Þegar þú notar Warehousing í fartækinu geturðu skilgreint hvernig lýsigögn skulu birt í tækinu á síðunni **Reitarheiti vöruhúsaforrits**.</span><span class="sxs-lookup"><span data-stu-id="343e2-111">When you use Warehousing on your mobile device, you can configure how metadata should be displayed on your device on the **Warehouse app field names** page.</span></span> <span data-ttu-id="343e2-112">Í nýju fyrirtæki skal velja **Stofna sjálfgefna uppsetningu** til að mynda öll reitaheiti sem verða notuð í verkflæðum vöruhússfartækja og svo úthluta æskilegan ílagsham og ílagsgerð á þau.</span><span class="sxs-lookup"><span data-stu-id="343e2-112">In a new company, select **Create default setup** to generate all field names that will be used in the warehouse mobile device workflows, and then assign a preferred input mode and input type to them.</span></span> <span data-ttu-id="343e2-113">Eftir að þú hefur myndað öll reitarheiti, geturðu valið eftirfarandi ílagsvalkosti.</span><span class="sxs-lookup"><span data-stu-id="343e2-113">After you have generated all field names, you can select the following input options.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="343e2-114">Valkostur</span><span class="sxs-lookup"><span data-stu-id="343e2-114">Option</span></span></th>
<th><span data-ttu-id="343e2-115">lýsing</span><span class="sxs-lookup"><span data-stu-id="343e2-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="343e2-116">Æskilegur ílagshamur</span><span class="sxs-lookup"><span data-stu-id="343e2-116">Preferred input mode</span></span></td>
<td><span data-ttu-id="343e2-117">Þessi valkostur skilgreinir hvort sýna eigi skönnunarreit eða ílagsreit fyrir handvirka færslu fyrir valið heiti reitar.</span><span class="sxs-lookup"><span data-stu-id="343e2-117">This option defines whether a scanning field or a manual entry input field should be shown for the selected field name.</span></span> <span data-ttu-id="343e2-118">Þetta er gagnlegt til að auðkenna reiti eftir því hvort strikamerki eru notuð fyrir reitinn.</span><span class="sxs-lookup"><span data-stu-id="343e2-118">This is useful to distinguish fields depending on if barcodes are used for the field.</span></span> <span data-ttu-id="343e2-119"><strong>Athugasemd:</strong> Fyrir reitarheiti með æskilegan ílagsham stilltan á <strong>Skönnun</strong> er hægt að færa inn upplýsingar handvirkt ef strikamerkið er ólæsilegt eða skemmt.</span><span class="sxs-lookup"><span data-stu-id="343e2-119"><strong>Note:</strong> For field names with preferred input mode set to <strong>Scanning</strong>, you can enter information manually if the barcode is unreadable or damaged.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="343e2-120">Inntaksgerð</span><span class="sxs-lookup"><span data-stu-id="343e2-120">Input type</span></span></td>
<td><span data-ttu-id="343e2-121">Þessi valkostur skilgreinir hvaða innsláttargerð ætti að vera notuð fyrir valið reitarheiti.</span><span class="sxs-lookup"><span data-stu-id="343e2-121">This option defines what input type should be used for the selected field name.</span></span> <span data-ttu-id="343e2-122">Fjórir valkostir eru í boði.</span><span class="sxs-lookup"><span data-stu-id="343e2-122">Four options are available:</span></span>
<ul>
<li><span data-ttu-id="343e2-123"><strong>Val</strong> - Inniheldur lista yfir tiltæka valkosti til að velja úr.</span><span class="sxs-lookup"><span data-stu-id="343e2-123"><strong>Selection</strong> - Contains a list of options to choose from.</span></span> <span data-ttu-id="343e2-124">Reitaheitum með þennan valkostur er ekki hægt að breyta.</span><span class="sxs-lookup"><span data-stu-id="343e2-124">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="343e2-125"><strong>Dagsetning</strong> - Reitaheiti sem eru skilgreind sem dagsetning munu sýna dagsetningarsnið með merkinu.</span><span class="sxs-lookup"><span data-stu-id="343e2-125"><strong>Date</strong> - Field names specified as date will show a date format with the label.</span></span> <span data-ttu-id="343e2-126">Þetta hjálpar starfsmanni í vöruhúsi að sjá á hvaða sniði eigi að færa inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="343e2-126">This helps warehouse workers see in which format to enter the date.</span></span> <span data-ttu-id="343e2-127">Reitaheitum með þennan valkostur er ekki hægt að breyta.</span><span class="sxs-lookup"><span data-stu-id="343e2-127">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="343e2-128"><strong>Stafir</strong> - Ef valið verður lyklaborð tækisins notað þegar upplýsingar eru færðar handvirkt í forritið.</span><span class="sxs-lookup"><span data-stu-id="343e2-128"><strong>Alpha</strong> - If selected, the device keyboard will be used when entering information manually in the app.</span></span> <span data-ttu-id="343e2-129">Hægt er að breyta lyklaborðsupplifun eftir því hvaða tæki er notað.</span><span class="sxs-lookup"><span data-stu-id="343e2-129">The keyboard experience can be changed depending on which device is used.</span></span></li>
<li><span data-ttu-id="343e2-130"><strong>Tölustafir</strong> - Fyrir reitaheiti sem nota aðeins tölustafi sem ílag geturðu valið þennan valkost til að birta sérsniðið talnalyklaborð með ílagssvæðinu í stað lyklaborðs tækis.</span><span class="sxs-lookup"><span data-stu-id="343e2-130"><strong>Numeric</strong> - For field names that use numeric input only, you can select this option to display a custom numeric keypad with the input field instead of the device keyboard.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="configure-warehouse-app-field-priority"></a><span data-ttu-id="343e2-131">Grunnstilla reitaforgang vöruhúsaforrits</span><span class="sxs-lookup"><span data-stu-id="343e2-131">Configure warehouse app field priority</span></span>

<span data-ttu-id="343e2-132">Á síðunni **Svæðisforgangur vöruhúsaforrits** síða, geturðu sett reitarheiti inn í mismunandi forgangsflokka.</span><span class="sxs-lookup"><span data-stu-id="343e2-132">On the **Warehouse app field priority** page, you can put field names into different priority groups.</span></span> <span data-ttu-id="343e2-133">Þetta gerir kleift að ákveða hvaða upplýsingar ætti að birta á aðalverkefnasíðunni þegar starfsmaður í vöruhúsi framkvæmir verkefni með notkun forritsins.</span><span class="sxs-lookup"><span data-stu-id="343e2-133">This makes it possible to decide what information should be displayed on the main task page when warehouse workers perform tasks using the app.</span></span> <span data-ttu-id="343e2-134">Ef smellt er á **Stofna sjálfgefna uppsetningu**, verður sjálfgefinn hópur forgangsflokks myndaður.</span><span class="sxs-lookup"><span data-stu-id="343e2-134">If you click **Create default setup**, a default set of priority groups will be generated.</span></span> <span data-ttu-id="343e2-135">Hægt er að stofna eins marga forgangsflokka og þörf er á, en aðeins þrír forgangsflokkar verða sýndir á verkefnasíðunni.</span><span class="sxs-lookup"><span data-stu-id="343e2-135">It is possible to create as many priority groups as needed, but only three priority groups will be shown on the task page.</span></span> <span data-ttu-id="343e2-136">Þegar kerfið sendir lýsigögn í forritið mun það úthluta hverju svæði hlutfallslegum forgangi eftir forgangsflokki og forritið mun birta fyrstu þrjá forgangsflokkana sem eru birtir í lýsigögnunum á verkefnasíðu.</span><span class="sxs-lookup"><span data-stu-id="343e2-136">When the system sends metadata to the app, it will assign each field a relative priority depending on its priority group, and the app will display the first three priority groups contained in the metadata on the task page.</span></span> <span data-ttu-id="343e2-137">Afgangurinn af yfirfylltum lýsigögnum verða birt á síðu með aukaupplýsingum.</span><span class="sxs-lookup"><span data-stu-id="343e2-137">The rest of the overflowing metadata will be displayed on a secondary details page.</span></span> <span data-ttu-id="343e2-138">Eftirfarandi tafla sýnir dæmi um fimm forgangsflokka.</span><span class="sxs-lookup"><span data-stu-id="343e2-138">The following table shows an example of five priority groups.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="343e2-139">Forgangsflokkur</span><span class="sxs-lookup"><span data-stu-id="343e2-139">Priority group</span></span></th>
<th><span data-ttu-id="343e2-140">Úthlutuð svæði</span><span class="sxs-lookup"><span data-stu-id="343e2-140">Assigned fields</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> <span data-ttu-id="343e2-141">Forgangur 10</span><span class="sxs-lookup"><span data-stu-id="343e2-141">Priority 10</span></span></td>
<td><ul>
<li><span data-ttu-id="343e2-142">vara</span><span class="sxs-lookup"><span data-stu-id="343e2-142">Item</span></span></li>
<li><span data-ttu-id="343e2-143">Magn</span><span class="sxs-lookup"><span data-stu-id="343e2-143">Quantity</span></span></li>
<li><span data-ttu-id="343e2-144">Mælieining</span><span class="sxs-lookup"><span data-stu-id="343e2-144">Unit of measure</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="343e2-145">Forgangur 20</span><span class="sxs-lookup"><span data-stu-id="343e2-145">Priority 20</span></span></td>
<td><ul>
<li><span data-ttu-id="343e2-146">Staðsetning klasa:</span><span class="sxs-lookup"><span data-stu-id="343e2-146">Cluster position</span></span></li>
<li><span data-ttu-id="343e2-147">Klasi</span><span class="sxs-lookup"><span data-stu-id="343e2-147">Cluster</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="343e2-148">Forgangur 30</span><span class="sxs-lookup"><span data-stu-id="343e2-148">Priority 30</span></span></td>
<td><ul>
<li><span data-ttu-id="343e2-149">Vörulýsing</span><span class="sxs-lookup"><span data-stu-id="343e2-149">Item description</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="343e2-150">Forgangur 40</span><span class="sxs-lookup"><span data-stu-id="343e2-150">Priority 40</span></span></td>
<td><ul>
<li><span data-ttu-id="343e2-151">Grunnstilling</span><span class="sxs-lookup"><span data-stu-id="343e2-151">Configuration</span></span></li>
<li><span data-ttu-id="343e2-152">Litur</span><span class="sxs-lookup"><span data-stu-id="343e2-152">Color</span></span></li>
<li><span data-ttu-id="343e2-153">Stærð</span><span class="sxs-lookup"><span data-stu-id="343e2-153">Size</span></span></li>
<li><span data-ttu-id="343e2-154">Stíll</span><span class="sxs-lookup"><span data-stu-id="343e2-154">Style</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="343e2-155">Forgangur 50</span><span class="sxs-lookup"><span data-stu-id="343e2-155">Priority 50</span></span></td>
<td><ul>
<li><span data-ttu-id="343e2-156">Staður</span><span class="sxs-lookup"><span data-stu-id="343e2-156">Location</span></span></li>
<li><span data-ttu-id="343e2-157">Númeraplata</span><span class="sxs-lookup"><span data-stu-id="343e2-157">License plate</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="343e2-158">Til dæmis þegar starfsmaður í vöruhúsi framkvæmir verk á fartæki, ef lýsigögnin sem verða birt í forritinu samanstanda af eftirfarandi svæði:</span><span class="sxs-lookup"><span data-stu-id="343e2-158">For example, when a warehouse worker is performing a task on a mobile device, if the metadata that will be displayed in the app consists of the following fields:</span></span>

-   <span data-ttu-id="343e2-159">vara</span><span class="sxs-lookup"><span data-stu-id="343e2-159">Item</span></span>
-   <span data-ttu-id="343e2-160">Magn</span><span class="sxs-lookup"><span data-stu-id="343e2-160">Quantity</span></span>
-   <span data-ttu-id="343e2-161">Mælieining</span><span class="sxs-lookup"><span data-stu-id="343e2-161">Unit of measure</span></span>
-   <span data-ttu-id="343e2-162">Vörulýsing</span><span class="sxs-lookup"><span data-stu-id="343e2-162">Item description</span></span>
-   <span data-ttu-id="343e2-163">Stærð og staðsetning</span><span class="sxs-lookup"><span data-stu-id="343e2-163">Size and Location</span></span>

<span data-ttu-id="343e2-164">Á grunni reitaforgangs í vöruhúsaforritinu sem var settur upp í töflunni hér að ofan, verða eftirfarandi 3 línur upplýsinga birtar á verkefnasíðunni:</span><span class="sxs-lookup"><span data-stu-id="343e2-164">Based on the warehouse app field priority set up in the table above, the following 3 rows of information will be displayed on the task page:</span></span>

-   <span data-ttu-id="343e2-165">Lína 1: Vara, Magn, Mælieining</span><span class="sxs-lookup"><span data-stu-id="343e2-165">Row 1: Item, Quantity, Unit of measure</span></span>
-   <span data-ttu-id="343e2-166">Lína 2: Vörulýsing</span><span class="sxs-lookup"><span data-stu-id="343e2-166">Row 2: Item description</span></span>
-   <span data-ttu-id="343e2-167">Lína 3: Stærð</span><span class="sxs-lookup"><span data-stu-id="343e2-167">Row 3: Size</span></span>

<span data-ttu-id="343e2-168">Eftirstandandi lýsigögn, til dæmis, Staðsetning, verða ekki birt á verkefnasíðunni heldur verða þau birt á upplýsingasíða.</span><span class="sxs-lookup"><span data-stu-id="343e2-168">The remaining metadata, for example, Location, will not be displayed on the task page, but will be displayed on a details page.</span></span> <span data-ttu-id="343e2-169">Frekari upplýsingar um þetta og dæmi um notandaviðmót má sjá í bloggfærslunni [Announcing Finance and Operations - Warehousing](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).</span><span class="sxs-lookup"><span data-stu-id="343e2-169">To learn more and see examples of the user interface, refer to the blog post [Announcing Finance and Operations - Warehousing](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).</span></span>

<a name="additional-resources"></a><span data-ttu-id="343e2-170">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="343e2-170">Additional resources</span></span>
--------

[<span data-ttu-id="343e2-171">Setja upp og tengja farsímaforrit vöruhúsakerfis</span><span class="sxs-lookup"><span data-stu-id="343e2-171">Install and connect the Warehouse Management mobile app</span></span>](../warehousing/install-configure-warehouse-management-app.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]