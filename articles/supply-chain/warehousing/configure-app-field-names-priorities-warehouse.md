---
title: Skilgreining svæðaheita í vöruhúsaforriti
description: Þetta efnisatriði lýsir því hvernig á að skilgreina og grunnstilla svæðaheiti og forgang vöruhúsaforriti í Dynamics 365 Supply Chain Management.
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileAppField, WHSMobileAppFieldPriority
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269434
ms.assetid: 6cf3d7da-29bb-4d3d-aaf5-544ca9cc2980
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 0390900d97e74bb9fd8deac913b1606cb775aa7c
ms.sourcegitcommit: ffd845d4230646499b6f074cb43e69ab95787671
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/07/2020
ms.locfileid: "3346400"
---
# <a name="configure-app-field-names-in-warehousing-app"></a><span data-ttu-id="afc6f-103">Skilgreining svæðaheita í vöruhúsaforriti</span><span class="sxs-lookup"><span data-stu-id="afc6f-103">Configure app field names in Warehousing app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="afc6f-104">Þetta efnisatriði lýsir því hvernig á að skilgreina og grunnstilla svæðaheiti og forgang vöruhúsaforriti í Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="afc6f-104">This topic describes how to define and configure warehousing app field names and priorities in Dynamics 365 Supply Chain Management.</span></span> 

> [!NOTE]
> <span data-ttu-id="afc6f-105">Þetta efnisatriði á við aðgerðir í vöruhúsakerfi.</span><span class="sxs-lookup"><span data-stu-id="afc6f-105">This topic applies to features in Warehouse management.</span></span> <span data-ttu-id="afc6f-106">Það á ekki við um aðgerðir í birgðastjórnun.</span><span class="sxs-lookup"><span data-stu-id="afc6f-106">It doesn’t apply to features in Inventory management.</span></span> <span data-ttu-id="afc6f-107">Warehousing er forrit sem hægt er að nota í framkvæmd vöruhúsaverkefna.</span><span class="sxs-lookup"><span data-stu-id="afc6f-107">Warehousing is an application that you can use to perform warehouse tasks.</span></span> <span data-ttu-id="afc6f-108">Hægt er að skilgreina og grunnstilla reitarheiti sem eru notuð í forritinu, ásamt því að grunnstilla forgang sem reitarheitum ætti að vera úthlutað eftir.</span><span class="sxs-lookup"><span data-stu-id="afc6f-108">You can define and configure the field names that are used in the app, as well as configure the priority to which the field names should be assigned.</span></span> <span data-ttu-id="afc6f-109">Þetta efnisatriði útskýrir því hvernig á að skilgreina og grunnstilla svæðaheiti og forgang vöruhúsaforriti og hvernig þau eru notuð í Warehousing.</span><span class="sxs-lookup"><span data-stu-id="afc6f-109">This topic explains how to define and configure these warehousing app field names and priorities, and how they are used in Warehousing.</span></span> <span data-ttu-id="afc6f-110">Nákvæmar upplýsingar um hvernig á að skilgreina tengingu við FWarehousing má sjá í sýnidæminu [Setja upp og skilgreina forritið Warehousing](install-configure-warehousing-app.md).</span><span class="sxs-lookup"><span data-stu-id="afc6f-110">For detailed information about how to configure the connection to FWarehousing, refer to the tutorial [Install and configure the Warehousing app overview](install-configure-warehousing-app.md).</span></span>

## <a name="configure-warehousing-app-field-names"></a><span data-ttu-id="afc6f-111">Grunnstilla reitarheiti vöruhúsaforrits</span><span class="sxs-lookup"><span data-stu-id="afc6f-111">Configure warehousing app field names</span></span>

<span data-ttu-id="afc6f-112">Þegar þú notar Warehousing í fartækinu geturðu skilgreint hvernig lýsigögn skulu birt í tækinu á síðunni **Reitarheiti vöruhúsaforrits**.</span><span class="sxs-lookup"><span data-stu-id="afc6f-112">When you use Warehousing on your mobile device, you can configure how metadata should be displayed on your device on the **Warehouse app field names** page.</span></span> <span data-ttu-id="afc6f-113">Í nýju fyrirtæki skal velja **Stofna sjálfgefna uppsetningu** til að mynda öll reitaheiti sem verða notuð í verkflæðum vöruhússfartækja og svo úthluta æskilegan ílagsham og ílagsgerð á þau.</span><span class="sxs-lookup"><span data-stu-id="afc6f-113">In a new company, select **Create default setup** to generate all field names that will be used in the warehouse mobile device workflows, and then assign a preferred input mode and input type to them.</span></span> <span data-ttu-id="afc6f-114">Eftir að þú hefur myndað öll reitarheiti, geturðu valið eftirfarandi ílagsvalkosti.</span><span class="sxs-lookup"><span data-stu-id="afc6f-114">After you have generated all field names, you can select the following input options.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="afc6f-115">Valkostur</span><span class="sxs-lookup"><span data-stu-id="afc6f-115">Option</span></span></th>
<th><span data-ttu-id="afc6f-116">lýsing</span><span class="sxs-lookup"><span data-stu-id="afc6f-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="afc6f-117">Æskilegur ílagshamur</span><span class="sxs-lookup"><span data-stu-id="afc6f-117">Preferred input mode</span></span></td>
<td><span data-ttu-id="afc6f-118">Þessi valkostur skilgreinir hvort sýna eigi skönnunarreit eða ílagsreit fyrir handvirka færslu fyrir valið heiti reitar.</span><span class="sxs-lookup"><span data-stu-id="afc6f-118">This option defines whether a scanning field or a manual entry input field should be shown for the selected field name.</span></span> <span data-ttu-id="afc6f-119">Þetta er gagnlegt til að auðkenna reiti eftir því hvort strikamerki eru notuð fyrir reitinn.</span><span class="sxs-lookup"><span data-stu-id="afc6f-119">This is useful to distinguish fields depending on if barcodes are used for the field.</span></span> <span data-ttu-id="afc6f-120"><strong>Athugasemd:</strong> Fyrir reitarheiti með æskilegan ílagsham stilltan á <strong>Skönnun</strong> er hægt að færa inn upplýsingar handvirkt ef strikamerkið er ólæsilegt eða skemmt.</span><span class="sxs-lookup"><span data-stu-id="afc6f-120"><strong>Note:</strong> For field names with preferred input mode set to <strong>Scanning</strong>, you can enter information manually if the barcode is unreadable or damaged.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="afc6f-121">Inntaksgerð</span><span class="sxs-lookup"><span data-stu-id="afc6f-121">Input type</span></span></td>
<td><span data-ttu-id="afc6f-122">Þessi valkostur skilgreinir hvaða innsláttargerð ætti að vera notuð fyrir valið reitarheiti.</span><span class="sxs-lookup"><span data-stu-id="afc6f-122">This option defines what input type should be used for the selected field name.</span></span> <span data-ttu-id="afc6f-123">Fjórir valkostir eru í boði.</span><span class="sxs-lookup"><span data-stu-id="afc6f-123">Four options are available:</span></span>
<ul>
<li><span data-ttu-id="afc6f-124"><strong>Val</strong> - Inniheldur lista yfir tiltæka valkosti til að velja úr.</span><span class="sxs-lookup"><span data-stu-id="afc6f-124"><strong>Selection</strong> - Contains a list of options to choose from.</span></span> <span data-ttu-id="afc6f-125">Reitaheitum með þennan valkostur er ekki hægt að breyta.</span><span class="sxs-lookup"><span data-stu-id="afc6f-125">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="afc6f-126"><strong>Dagsetning</strong> - Reitaheiti sem eru skilgreind sem dagsetning munu sýna dagsetningarsnið með merkinu.</span><span class="sxs-lookup"><span data-stu-id="afc6f-126"><strong>Date</strong> - Field names specified as date will show a date format with the label.</span></span> <span data-ttu-id="afc6f-127">Þetta hjálpar starfsmanni í vöruhúsi að sjá á hvaða sniði eigi að færa inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="afc6f-127">This helps warehouse workers see in which format to enter the date.</span></span> <span data-ttu-id="afc6f-128">Reitaheitum með þennan valkostur er ekki hægt að breyta.</span><span class="sxs-lookup"><span data-stu-id="afc6f-128">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="afc6f-129"><strong>Stafir</strong> - Ef valið verður lyklaborð tækisins notað þegar upplýsingar eru færðar handvirkt í forritið.</span><span class="sxs-lookup"><span data-stu-id="afc6f-129"><strong>Alpha</strong> - If selected, the device keyboard will be used when entering information manually in the app.</span></span> <span data-ttu-id="afc6f-130">Hægt er að breyta lyklaborðsupplifun eftir því hvaða tæki er notað.</span><span class="sxs-lookup"><span data-stu-id="afc6f-130">The keyboard experience can be changed depending on which device is used.</span></span></li>
<li><span data-ttu-id="afc6f-131"><strong>Tölustafir</strong> - Fyrir reitaheiti sem nota aðeins tölustafi sem ílag geturðu valið þennan valkost til að birta sérsniðið talnalyklaborð með ílagssvæðinu í stað lyklaborðs tækis.</span><span class="sxs-lookup"><span data-stu-id="afc6f-131"><strong>Numeric</strong> - For field names that use numeric input only, you can select this option to display a custom numeric keypad with the input field instead of the device keyboard.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="configure-warehousing-app-field-priority"></a><span data-ttu-id="afc6f-132">Grunnstilla reitaforgang vöruhúsaforrits</span><span class="sxs-lookup"><span data-stu-id="afc6f-132">Configure warehousing app field priority</span></span>

<span data-ttu-id="afc6f-133">Á síðunni **Svæðisforgangur vöruhúsaforrits** síða, geturðu sett reitarheiti inn í mismunandi forgangsflokka.</span><span class="sxs-lookup"><span data-stu-id="afc6f-133">On the **Warehouse app field priority** page, you can put field names into different priority groups.</span></span> <span data-ttu-id="afc6f-134">Þetta gerir kleift að ákveða hvaða upplýsingar ætti að birta á aðalverkefnasíðunni þegar starfsmaður í vöruhúsi framkvæmir verkefni með notkun forritsins.</span><span class="sxs-lookup"><span data-stu-id="afc6f-134">This makes it possible to decide what information should be displayed on the main task page when warehouse workers perform tasks using the app.</span></span> <span data-ttu-id="afc6f-135">Ef smellt er á **Stofna sjálfgefna uppsetningu**, verður sjálfgefinn hópur forgangsflokks myndaður.</span><span class="sxs-lookup"><span data-stu-id="afc6f-135">If you click **Create default setup**, a default set of priority groups will be generated.</span></span> <span data-ttu-id="afc6f-136">Hægt er að stofna eins marga forgangsflokka og þörf er á, en aðeins þrír forgangsflokkar verða sýndir á verkefnasíðunni.</span><span class="sxs-lookup"><span data-stu-id="afc6f-136">It is possible to create as many priority groups as needed, but only three priority groups will be shown on the task page.</span></span> <span data-ttu-id="afc6f-137">Þegar kerfið sendir lýsigögn í forritið mun það úthluta hverju svæði hlutfallslegum forgangi eftir forgangsflokki og forritið mun birta fyrstu þrjá forgangsflokkana sem eru birtir í lýsigögnunum á verkefnasíðu.</span><span class="sxs-lookup"><span data-stu-id="afc6f-137">When the system sends metadata to the app, it will assign each field a relative priority depending on its priority group, and the app will display the first three priority groups contained in the metadata on the task page.</span></span> <span data-ttu-id="afc6f-138">Afgangurinn af yfirfylltum lýsigögnum verða birt á síðu með aukaupplýsingum.</span><span class="sxs-lookup"><span data-stu-id="afc6f-138">The rest of the overflowing metadata will be displayed on a secondary details page.</span></span> <span data-ttu-id="afc6f-139">Eftirfarandi tafla sýnir dæmi um fimm forgangsflokka.</span><span class="sxs-lookup"><span data-stu-id="afc6f-139">The following table shows an example of five priority groups.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="afc6f-140">Forgangsflokkur</span><span class="sxs-lookup"><span data-stu-id="afc6f-140">Priority group</span></span></th>
<th><span data-ttu-id="afc6f-141">Úthlutuð svæði</span><span class="sxs-lookup"><span data-stu-id="afc6f-141">Assigned fields</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> <span data-ttu-id="afc6f-142">Forgangur 10</span><span class="sxs-lookup"><span data-stu-id="afc6f-142">Priority 10</span></span></td>
<td><ul>
<li><span data-ttu-id="afc6f-143">vara</span><span class="sxs-lookup"><span data-stu-id="afc6f-143">Item</span></span></li>
<li><span data-ttu-id="afc6f-144">Magn</span><span class="sxs-lookup"><span data-stu-id="afc6f-144">Quantity</span></span></li>
<li><span data-ttu-id="afc6f-145">Mælieining</span><span class="sxs-lookup"><span data-stu-id="afc6f-145">Unit of measure</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="afc6f-146">Forgangur 20</span><span class="sxs-lookup"><span data-stu-id="afc6f-146">Priority 20</span></span></td>
<td><ul>
<li><span data-ttu-id="afc6f-147">Staðsetning klasa:</span><span class="sxs-lookup"><span data-stu-id="afc6f-147">Cluster position</span></span></li>
<li><span data-ttu-id="afc6f-148">Klasi</span><span class="sxs-lookup"><span data-stu-id="afc6f-148">Cluster</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="afc6f-149">Forgangur 30</span><span class="sxs-lookup"><span data-stu-id="afc6f-149">Priority 30</span></span></td>
<td><ul>
<li><span data-ttu-id="afc6f-150">Vörulýsing</span><span class="sxs-lookup"><span data-stu-id="afc6f-150">Item description</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="afc6f-151">Forgangur 40</span><span class="sxs-lookup"><span data-stu-id="afc6f-151">Priority 40</span></span></td>
<td><ul>
<li><span data-ttu-id="afc6f-152">Grunnstilling</span><span class="sxs-lookup"><span data-stu-id="afc6f-152">Configuration</span></span></li>
<li><span data-ttu-id="afc6f-153">Litur</span><span class="sxs-lookup"><span data-stu-id="afc6f-153">Color</span></span></li>
<li><span data-ttu-id="afc6f-154">Stærð</span><span class="sxs-lookup"><span data-stu-id="afc6f-154">Size</span></span></li>
<li><span data-ttu-id="afc6f-155">Stíll</span><span class="sxs-lookup"><span data-stu-id="afc6f-155">Style</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="afc6f-156">Forgangur 50</span><span class="sxs-lookup"><span data-stu-id="afc6f-156">Priority 50</span></span></td>
<td><ul>
<li><span data-ttu-id="afc6f-157">Staður</span><span class="sxs-lookup"><span data-stu-id="afc6f-157">Location</span></span></li>
<li><span data-ttu-id="afc6f-158">Númeraplata</span><span class="sxs-lookup"><span data-stu-id="afc6f-158">License plate</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="afc6f-159">Til dæmis þegar starfsmaður í vöruhúsi framkvæmir verk á fartæki, ef lýsigögnin sem verða birt í forritinu samanstanda af eftirfarandi svæði:</span><span class="sxs-lookup"><span data-stu-id="afc6f-159">For example, when a warehouse worker is performing a task on a mobile device, if the metadata that will be displayed in the app consists of the following fields:</span></span>

-   <span data-ttu-id="afc6f-160">vara</span><span class="sxs-lookup"><span data-stu-id="afc6f-160">Item</span></span>
-   <span data-ttu-id="afc6f-161">Magn</span><span class="sxs-lookup"><span data-stu-id="afc6f-161">Quantity</span></span>
-   <span data-ttu-id="afc6f-162">Mælieining</span><span class="sxs-lookup"><span data-stu-id="afc6f-162">Unit of measure</span></span>
-   <span data-ttu-id="afc6f-163">Vörulýsing</span><span class="sxs-lookup"><span data-stu-id="afc6f-163">Item description</span></span>
-   <span data-ttu-id="afc6f-164">Stærð og staðsetning</span><span class="sxs-lookup"><span data-stu-id="afc6f-164">Size and Location</span></span>

<span data-ttu-id="afc6f-165">Á grunni reitaforgangs í vöruhúsaforritinu sem var settur upp í töflunni hér að ofan, verða eftirfarandi 3 línur upplýsinga birtar á verkefnasíðunni:</span><span class="sxs-lookup"><span data-stu-id="afc6f-165">Based on the warehousing app field priority set up in the table above, the following 3 rows of information will be displayed on the task page:</span></span>

-   <span data-ttu-id="afc6f-166">Lína 1: Vara, Magn, Mælieining</span><span class="sxs-lookup"><span data-stu-id="afc6f-166">Row 1: Item, Quantity, Unit of measure</span></span>
-   <span data-ttu-id="afc6f-167">Lína 2: Vörulýsing</span><span class="sxs-lookup"><span data-stu-id="afc6f-167">Row 2: Item description</span></span>
-   <span data-ttu-id="afc6f-168">Lína 3: Stærð</span><span class="sxs-lookup"><span data-stu-id="afc6f-168">Row 3: Size</span></span>

<span data-ttu-id="afc6f-169">Eftirstandandi lýsigögn, til dæmis, Staðsetning, verða ekki birt á verkefnasíðunni heldur verða þau birt á upplýsingasíða.</span><span class="sxs-lookup"><span data-stu-id="afc6f-169">The remaining metadata, for example, Location, will not be displayed on the task page, but will be displayed on a details page.</span></span> <span data-ttu-id="afc6f-170">Frekari upplýsingar um þetta og dæmi um notandaviðmót má sjá í bloggfærslunni [Announcing Finance and Operations - Warehousing](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).</span><span class="sxs-lookup"><span data-stu-id="afc6f-170">To learn more and see examples of the user interface, refer to the blog post [Announcing Finance and Operations - Warehousing](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).</span></span>

<a name="additional-resources"></a><span data-ttu-id="afc6f-171">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="afc6f-171">Additional resources</span></span>
--------

[<span data-ttu-id="afc6f-172">Yfirlit yfir uppsetningu og skilgreiningu vöruhúsaforrits</span><span class="sxs-lookup"><span data-stu-id="afc6f-172">Install and configure the Warehousing app overview</span></span>](install-configure-warehousing-app.md)
