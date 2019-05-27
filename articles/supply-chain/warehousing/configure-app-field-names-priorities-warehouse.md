---
title: Skilgreining svæðaheita í vöruhúsaforriti
description: Þetta efnisatriði lýsir því hvernig á að skilgreina og grunnstilla svæðaheiti og forgang í vöruhúsaforriti í Finance and Operations.
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileAppField, WHSMobileAppFieldPriority
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269434
ms.assetid: 6cf3d7da-29bb-4d3d-aaf5-544ca9cc2980
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 0162014189ed6bffb17e6718a67eecfd55c334a5
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1548930"
---
# <a name="configure-app-field-names-in-warehousing-app"></a><span data-ttu-id="2722f-103">Skilgreining svæðaheita í vöruhúsaforriti</span><span class="sxs-lookup"><span data-stu-id="2722f-103">Configure app field names in Warehousing app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2722f-104">Þetta efnisatriði lýsir því hvernig á að skilgreina og grunnstilla svæðaheiti og forgang í vöruhúsaforriti í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="2722f-104">This topic describes how to define and configure warehouse app field names and priorities in Finance and Operations.</span></span> 

<span data-ttu-id="2722f-105">**Ábending:** Þetta efnisatriði á við aðgerðir í vöruhúsakerfi.</span><span class="sxs-lookup"><span data-stu-id="2722f-105">**Note:** This topic applies to features in Warehouse management.</span></span> <span data-ttu-id="2722f-106">Það á ekki við um aðgerðir í birgðastjórnun.</span><span class="sxs-lookup"><span data-stu-id="2722f-106">It doesn’t apply to features in Inventory management.</span></span> <span data-ttu-id="2722f-107">Finance and Operations - Warehousing er forrit sem hægt er að nota í framkvæmd vöruhúsaverkefna.</span><span class="sxs-lookup"><span data-stu-id="2722f-107">Finance and Operations - Warehousing is an application that you can use to perform warehouse tasks.</span></span> <span data-ttu-id="2722f-108">Hægt er að skilgreina og grunnstilla reitarheiti sem eru notuð í forritinu, ásamt því að grunnstilla forgang sem reitarheitum ætti að vera úthlutað eftir.</span><span class="sxs-lookup"><span data-stu-id="2722f-108">You can define and configure the field names that are used in the app, as well as configure the priority to which the field names should be assigned.</span></span> <span data-ttu-id="2722f-109">Þetta efnisatriði útskýrir því hvernig á að skilgreina og grunnstilla svæðaheiti og forgang í vöruhúsaforriti og hvernig þau eru notuð í Finance and Operations - Warehousing.</span><span class="sxs-lookup"><span data-stu-id="2722f-109">This topic explains how to define and configure these warehouse app field names and priorities, and how they are used in Finance and Operations - Warehousing.</span></span> <span data-ttu-id="2722f-110">Nákvæmar upplýsingar um hvernig á að skilgreina tengingu við Finance and Operations - Warehousing má sjá í sýnidæminu [Setja upp og skilgreina Finance and Operations - Warehousing](install-configure-warehousing-app.md).</span><span class="sxs-lookup"><span data-stu-id="2722f-110">For detailed information about how to configure the connection to Finance and Operations  - Warehousing, refer to the tutorial [Install and configure Finance and Operations - Warehousing](install-configure-warehousing-app.md).</span></span>

## <a name="configure-warehouse-app-field-names"></a><span data-ttu-id="2722f-111">Grunnstilla reitarheiti vöruhúsaforrits</span><span class="sxs-lookup"><span data-stu-id="2722f-111">Configure warehouse app field names</span></span>

<span data-ttu-id="2722f-112">Þegar þú notar Finance and Operations - Warehousing í fartækinu geturðu skilgreint hvernig lýsigögn skulu birt í tækinu á síðunni **Reitarheiti vöruhúsaforrits**.</span><span class="sxs-lookup"><span data-stu-id="2722f-112">When you use Finance and Operations - Warehousing on your mobile device, you can configure how metadata should be displayed on your device on the **Warehouse app field names** page.</span></span> <span data-ttu-id="2722f-113">Í nýju fyrirtæki í Finance and Operations skal velja **Stofna sjálfgefna uppsetningu** til að mynda öll reitarheiti sem verða notuð í verkflæðum vöruhússfartækja og svo úthluta æskilegan ílagsham og ílagsgerð á þau.</span><span class="sxs-lookup"><span data-stu-id="2722f-113">In a new company in Finance and Operations, select **Create default setup** to generate all field names that will be used in the warehouse mobile device workflows, and then assign a preferred input mode and input type to them.</span></span> <span data-ttu-id="2722f-114">Eftir að þú hefur myndað öll reitarheiti, geturðu valið eftirfarandi ílagsvalkosti.</span><span class="sxs-lookup"><span data-stu-id="2722f-114">After you have generated all field names, you can select the following input options.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2722f-115">Valkostur</span><span class="sxs-lookup"><span data-stu-id="2722f-115">Option</span></span></th>
<th><span data-ttu-id="2722f-116">lýsing</span><span class="sxs-lookup"><span data-stu-id="2722f-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2722f-117">Æskilegur ílagshamur</span><span class="sxs-lookup"><span data-stu-id="2722f-117">Preferred input mode</span></span></td>
<td><span data-ttu-id="2722f-118">Þessi valkostur skilgreinir hvort sýna eigi skönnunarreit eða ílagsreit fyrir handvirka færslu fyrir valið heiti reitar.</span><span class="sxs-lookup"><span data-stu-id="2722f-118">This option defines whether a scanning field or a manual entry input field should be shown for the selected field name.</span></span> <span data-ttu-id="2722f-119">Þetta er gagnlegt til að auðkenna reiti eftir því hvort strikamerki eru notuð fyrir reitinn.</span><span class="sxs-lookup"><span data-stu-id="2722f-119">This is useful to distinguish fields depending on if barcodes are used for the field.</span></span> <span data-ttu-id="2722f-120"><strong>Athugasemd:</strong> Fyrir reitarheiti með æskilegan ílagsham stilltan á <strong>Skönnun</strong> er hægt að færa inn upplýsingar handvirkt ef strikamerkið er ólæsilegt eða skemmt.</span><span class="sxs-lookup"><span data-stu-id="2722f-120"><strong>Note:</strong> For field names with preferred input mode set to <strong>Scanning</strong>, you can enter information manually if the barcode is unreadable or damaged.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2722f-121">Inntaksgerð</span><span class="sxs-lookup"><span data-stu-id="2722f-121">Input type</span></span></td>
<td><span data-ttu-id="2722f-122">Þessi valkostur skilgreinir hvaða innsláttargerð ætti að vera notuð fyrir valið reitarheiti.</span><span class="sxs-lookup"><span data-stu-id="2722f-122">This option defines what input type should be used for the selected field name.</span></span> <span data-ttu-id="2722f-123">Fjórir valkostir eru í boði.</span><span class="sxs-lookup"><span data-stu-id="2722f-123">Four options are available:</span></span>
<ul>
<li><span data-ttu-id="2722f-124"><strong>Val</strong>- Inniheldur lista yfir tiltæka valkosti til að velja úr.</span><span class="sxs-lookup"><span data-stu-id="2722f-124"><strong>Selection</strong> - Contains a list of options to choose from.</span></span> <span data-ttu-id="2722f-125">Reitaheitum með þennan valkostur er ekki hægt að breyta.</span><span class="sxs-lookup"><span data-stu-id="2722f-125">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="2722f-126"><strong>Dagsetning</strong>- Reitarheiti sem eru skilgreind sem dagsetning munu sýna dagsetningarsnið með merkinu.</span><span class="sxs-lookup"><span data-stu-id="2722f-126"><strong>Date</strong> - Field names specified as date will show a date format with the label.</span></span> <span data-ttu-id="2722f-127">Þetta hjálpar starfsmanni í vöruhúsi að sjá á hvaða sniði eigi að færa inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="2722f-127">This helps warehouse workers see in which format to enter the date.</span></span> <span data-ttu-id="2722f-128">Reitaheitum með þennan valkostur er ekki hægt að breyta.</span><span class="sxs-lookup"><span data-stu-id="2722f-128">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="2722f-129"><strong>Stafir</strong>- Ef valið verður lyklaborð tækisins notað þegar upplýsingar eru færðar handvirkt í forritið.</span><span class="sxs-lookup"><span data-stu-id="2722f-129"><strong>Alpha</strong> - If selected, the device keyboard will be used when entering information manually in the app.</span></span> <span data-ttu-id="2722f-130">Hægt er að breyta lyklaborðsupplifun eftir því hvaða tæki er notað.</span><span class="sxs-lookup"><span data-stu-id="2722f-130">The keyboard experience can be changed depending on which device is used.</span></span></li>
<li><span data-ttu-id="2722f-131"><strong>Tölustafir</strong>- Fyrir reitarheiti sem nota aðeins tölustafir sem ílag geturðu valið þennan valkost til að birta sérsniðið talnatakkaborð með ílagssvæðinu í stað lyklaborðs tækis.</span><span class="sxs-lookup"><span data-stu-id="2722f-131"><strong>Numeric</strong> - For field names that use numeric input only, you can select this option to display a custom numeric keypad with the input field instead of the device keyboard.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="configure-warehouse-app-field-priority"></a><span data-ttu-id="2722f-132">Grunnstilla reitaforgang vöruhúsaforrits</span><span class="sxs-lookup"><span data-stu-id="2722f-132">Configure warehouse app field priority</span></span>

<span data-ttu-id="2722f-133">Á síðunni **Svæðisforgangur vöruhúsaforrits** síða, geturðu sett reitarheiti inn í mismunandi forgangsflokka.</span><span class="sxs-lookup"><span data-stu-id="2722f-133">On the **Warehouse app field priority** page, you can put field names into different priority groups.</span></span> <span data-ttu-id="2722f-134">Þetta gerir kleift að ákveða hvaða upplýsingar ætti að birta á aðalverkefnasíðunni þegar starfsmaður í vöruhúsi framkvæmir verkefni með notkun forritsins.</span><span class="sxs-lookup"><span data-stu-id="2722f-134">This makes it possible to decide what information should be displayed on the main task page when warehouse workers perform tasks using the app.</span></span> <span data-ttu-id="2722f-135">Ef smellt er á **Stofna sjálfgefna uppsetningu**, verður sjálfgefinn hópur forgangsflokks myndaður.</span><span class="sxs-lookup"><span data-stu-id="2722f-135">If you click **Create default setup**, a default set of priority groups will be generated.</span></span> <span data-ttu-id="2722f-136">Hægt er að stofna eins marga forgangsflokka og þörf er á, en aðeins þrír forgangsflokkar verða sýndir á verkefnasíðunni.</span><span class="sxs-lookup"><span data-stu-id="2722f-136">It is possible to create as many priority groups as needed, but only three priority groups will be shown on the task page.</span></span> <span data-ttu-id="2722f-137">Þegar Finance and Operations sendir lýsigögn í forritið mun það úthluta hverju svæði hlutfallslegum forgangi eftir forgangsflokki og forritið mun birta fyrstu þrjá forgangsflokkana sem eru birtir í lýsigögnunum á verkefnasíðu.</span><span class="sxs-lookup"><span data-stu-id="2722f-137">When Finance and Operations sends metadata to the app, it will assign each field a relative priority depending on its priority group, and the app will display the first three priority groups contained in the metadata on the task page.</span></span> <span data-ttu-id="2722f-138">Afgangurinn af yfirfylltum lýsigögnum verða birt á síðu með aukaupplýsingum.</span><span class="sxs-lookup"><span data-stu-id="2722f-138">The rest of the overflowing metadata will be displayed on a secondary details page.</span></span> <span data-ttu-id="2722f-139">Eftirfarandi tafla sýnir dæmi um fimm forgangsflokka.</span><span class="sxs-lookup"><span data-stu-id="2722f-139">The following table shows an example of five priority groups.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2722f-140">Forgangsflokkur</span><span class="sxs-lookup"><span data-stu-id="2722f-140">Priority group</span></span></th>
<th><span data-ttu-id="2722f-141">Úthlutuð svæði</span><span class="sxs-lookup"><span data-stu-id="2722f-141">Assigned fields</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> <span data-ttu-id="2722f-142">Forgangur 10</span><span class="sxs-lookup"><span data-stu-id="2722f-142">Priority 10</span></span></td>
<td><ul>
<li><span data-ttu-id="2722f-143">vara</span><span class="sxs-lookup"><span data-stu-id="2722f-143">Item</span></span></li>
<li><span data-ttu-id="2722f-144">Magn</span><span class="sxs-lookup"><span data-stu-id="2722f-144">Quantity</span></span></li>
<li><span data-ttu-id="2722f-145">Mælieining</span><span class="sxs-lookup"><span data-stu-id="2722f-145">Unit of measure</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="2722f-146">Forgangur 20</span><span class="sxs-lookup"><span data-stu-id="2722f-146">Priority 20</span></span></td>
<td><ul>
<li><span data-ttu-id="2722f-147">Staðsetning klasa:</span><span class="sxs-lookup"><span data-stu-id="2722f-147">Cluster position</span></span></li>
<li><span data-ttu-id="2722f-148">Klasi</span><span class="sxs-lookup"><span data-stu-id="2722f-148">Cluster</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="2722f-149">Forgangur 30</span><span class="sxs-lookup"><span data-stu-id="2722f-149">Priority 30</span></span></td>
<td><ul>
<li><span data-ttu-id="2722f-150">Vörulýsing</span><span class="sxs-lookup"><span data-stu-id="2722f-150">Item description</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="2722f-151">Forgangur 40</span><span class="sxs-lookup"><span data-stu-id="2722f-151">Priority 40</span></span></td>
<td><ul>
<li><span data-ttu-id="2722f-152">Grunnstilling</span><span class="sxs-lookup"><span data-stu-id="2722f-152">Configuration</span></span></li>
<li><span data-ttu-id="2722f-153">Litur</span><span class="sxs-lookup"><span data-stu-id="2722f-153">Color</span></span></li>
<li><span data-ttu-id="2722f-154">Stærð</span><span class="sxs-lookup"><span data-stu-id="2722f-154">Size</span></span></li>
<li><span data-ttu-id="2722f-155">Stíll</span><span class="sxs-lookup"><span data-stu-id="2722f-155">Style</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="2722f-156">Forgangur 50</span><span class="sxs-lookup"><span data-stu-id="2722f-156">Priority 50</span></span></td>
<td><ul>
<li><span data-ttu-id="2722f-157">Staður</span><span class="sxs-lookup"><span data-stu-id="2722f-157">Location</span></span></li>
<li><span data-ttu-id="2722f-158">Númeraplata</span><span class="sxs-lookup"><span data-stu-id="2722f-158">License plate</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="2722f-159">Til dæmis þegar starfsmaður í vöruhúsi framkvæmir verk á fartæki, ef lýsigögnin sem verða birt í forritinu samanstanda af eftirfarandi svæði:</span><span class="sxs-lookup"><span data-stu-id="2722f-159">For example, when a warehouse worker is performing a task on a mobile device, if the metadata that will be displayed in the app consists of the following fields:</span></span>

-   <span data-ttu-id="2722f-160">vara</span><span class="sxs-lookup"><span data-stu-id="2722f-160">Item</span></span>
-   <span data-ttu-id="2722f-161">Magn</span><span class="sxs-lookup"><span data-stu-id="2722f-161">Quantity</span></span>
-   <span data-ttu-id="2722f-162">Mælieining</span><span class="sxs-lookup"><span data-stu-id="2722f-162">Unit of measure</span></span>
-   <span data-ttu-id="2722f-163">Vörulýsing</span><span class="sxs-lookup"><span data-stu-id="2722f-163">Item description</span></span>
-   <span data-ttu-id="2722f-164">Stærð og staðsetning</span><span class="sxs-lookup"><span data-stu-id="2722f-164">Size and Location</span></span>

<span data-ttu-id="2722f-165">Á grunni reitaforgangs í vöruhúsaforritinu sem var settur upp í töflunni hér að ofan, verða eftirfarandi 3 línur upplýsinga birtar á verkefnasíðunni:</span><span class="sxs-lookup"><span data-stu-id="2722f-165">Based on the warehouse app field priority set up in the table above, the following 3 rows of information will be displayed on the task page:</span></span>

-   <span data-ttu-id="2722f-166">Lína 1: Vara, Magn, Mælieining</span><span class="sxs-lookup"><span data-stu-id="2722f-166">Row 1: Item, Quantity, Unit of measure</span></span>
-   <span data-ttu-id="2722f-167">Lína 2: Vörulýsing</span><span class="sxs-lookup"><span data-stu-id="2722f-167">Row 2: Item description</span></span>
-   <span data-ttu-id="2722f-168">Lína 3: Stærð</span><span class="sxs-lookup"><span data-stu-id="2722f-168">Row 3: Size</span></span>

<span data-ttu-id="2722f-169">Eftirstandandi lýsigögn, til dæmis, Staðsetning, verða ekki birt á verkefnasíðunni heldur verða þau birt á upplýsingasíða.</span><span class="sxs-lookup"><span data-stu-id="2722f-169">The remaining metadata, for example, Location, will not be displayed on the task page, but will be displayed on a details page.</span></span> <span data-ttu-id="2722f-170">Frekari upplýsingar um þetta og dæmi um notandaviðmót má sjá í bloggfærslunni [Announcing Finance and Operations - Warehousing](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).</span><span class="sxs-lookup"><span data-stu-id="2722f-170">To learn more and see examples of the user interface, refer to the blog post [Announcing Finance and Operations - Warehousing](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).</span></span>

<a name="additional-resources"></a><span data-ttu-id="2722f-171">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="2722f-171">Additional resources</span></span>
--------

[<span data-ttu-id="2722f-172">Setja upp og skilgreina Microsoft Dynamics 365 for Finance and Operations – Vörugeymslu</span><span class="sxs-lookup"><span data-stu-id="2722f-172">Install and configure Microsoft Dynamics 365 for Finance and Operations – Warehousing</span></span>](install-configure-warehousing-app.md)



