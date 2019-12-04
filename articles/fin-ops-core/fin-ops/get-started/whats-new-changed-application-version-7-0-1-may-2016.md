---
title: Hvað er nýtt og hvað hefur breyst í Dynamics AX forritaútgáfa 7.0.1 (maí 2016)
description: Þessi grein lýsir eiginleikum sem eru annað hvort nýjar eða breyttar í Microsoft Dynamics AX umsókn útgáfu 7.0.1. Þessi útgáfa var losuð í Maí 2016 og byggingarnúmer af 7.0.1265.23014.
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ROBOTS: NOINDEX, NOFOLLOW
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Operations
ms.custom: 91213
ms.assetid: f0bbc78f-87fc-40e9-b46a-6655893f69be
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 715e0f8d08c6abbde35eb917cddc4ecf4b7b67ed
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811457"
---
# <a name="whats-new-or-changed-in-dynamics-ax-application-version-701-may-2016"></a><span data-ttu-id="6be4f-104">Hvað er nýtt og hvað hefur breyst í Dynamics AX forritaútgáfa 7.0.1 (maí 2016)</span><span class="sxs-lookup"><span data-stu-id="6be4f-104">What's new or changed in Dynamics AX application version 7.0.1 (May 2016)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6be4f-105">Þessi grein lýsir eiginleikum sem eru annað hvort nýjar eða breyttar í Microsoft Dynamics AX umsókn útgáfu 7.0.1.</span><span class="sxs-lookup"><span data-stu-id="6be4f-105">This article describes features that are either new or changed in Microsoft Dynamics AX application version 7.0.1.</span></span> <span data-ttu-id="6be4f-106">Þessi útgáfa var losuð í Maí 2016 og byggingarnúmer af 7.0.1265.23014.</span><span class="sxs-lookup"><span data-stu-id="6be4f-106">This version was released in May 2016 and has a build number of 7.0.1265.23014.</span></span>

## <a name="electronic-reporting-er"></a><span data-ttu-id="6be4f-107">Rafræn skýrslugerð (ER)</span><span class="sxs-lookup"><span data-stu-id="6be4f-107">Electronic reporting (ER)</span></span>

| <span data-ttu-id="6be4f-108">Hvað hægt er að gera?</span><span class="sxs-lookup"><span data-stu-id="6be4f-108">What can you do?</span></span> | <span data-ttu-id="6be4f-109">Hví er þetta mikilvægt?</span><span class="sxs-lookup"><span data-stu-id="6be4f-109">Why is this important?</span></span> |
|------------------|------------------------|
| <span data-ttu-id="6be4f-110">Skilgreina keyrslu tími svarglugga til að búa til Rafræna skýrslugerð skýrslur (ER), þannig að notendur geta valið fjárhagsvíddirnar sem þær vilja.</span><span class="sxs-lookup"><span data-stu-id="6be4f-110">Configure a run-time dialog box for designing Electronic reporting (ER) reports, so that users can select the financial dimensions that they want.</span></span> | <span data-ttu-id="6be4f-111">Í keyrslutíma, í svarglugganum fyrir keyrð ER skýrslan notendur geta valið margar fjárhagsvíddir.</span><span class="sxs-lookup"><span data-stu-id="6be4f-111">At run time, in the dialog box for running an ER report, users can select multiple financial dimensions.</span></span> <span data-ttu-id="6be4f-112">Upplýsingar um valda fjárhagsvíddir verður birt í rafræna skjalið sem er mynduð.</span><span class="sxs-lookup"><span data-stu-id="6be4f-112">The details of the selected financial dimensions will be displayed in the electronic document that is generated.</span></span> |
| <span data-ttu-id="6be4f-113">Skilgreina aðgang að mörgum fjárhagsvíddir meðan hönnun ER skýrsla með einni vörpun í æskilega gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="6be4f-113">Configure access to multiple financial dimensions during the design of an ER report, via a single mapping to the desired data source.</span></span> | <span data-ttu-id="6be4f-114">Hægt er að nota sama skýrsluskilgreiningar ER til að mynda rafræn skjöl sem sýna færslugögnum með upplýsingar um fjárhagsvíddir, burtséð frá fjölda fjárhagsvíddirnar sem eru valdar af notandanum eða skilgreind fyrir núgildandi lögaðila eða tilvik.</span><span class="sxs-lookup"><span data-stu-id="6be4f-114">The same ER report configuration can be used to generate electronic documents that present transactional data together with details of financial dimensions, regardless of the number of financial dimensions that are either selected by the user or configured for the current legal entity or instance.</span></span> |
| <span data-ttu-id="6be4f-115">Stilla skýrslu ER að færa gögn í dálkum sjálfvirkt myndað af rafræna skjalið sem er stofnun í OPENXML vinnublaði.</span><span class="sxs-lookup"><span data-stu-id="6be4f-115">Configure an ER report to enter data in dynamically generated columns of an electronic document that is created in OPENXML worksheet format.</span></span> | <span data-ttu-id="6be4f-116">ER skýrslan hægt að færa inn gögn í OPENXML vinnublaðs sem er mynduð með gagnaspeglun láréttur dálka.</span><span class="sxs-lookup"><span data-stu-id="6be4f-116">An ER report can enter data in an OPENXML worksheet that is generated, via horizontally replicating columns.</span></span> <span data-ttu-id="6be4f-117">Þess vegna er hægt að endurnota sama skýrsluskilgreiningar ER til að mynda rafrænu skjölin sem hafa mismunandi fjölda dálka sem sjálfvirkt myndaðan.</span><span class="sxs-lookup"><span data-stu-id="6be4f-117">Therefore, the same ER report configuration can be reused to generate electronic documents that have a different number of dynamically generated columns.</span></span> |
| <span data-ttu-id="6be4f-118">Skilgreina ER áfangastaði sem úttaks niðurstaða snið beint er til ákveðna áfangastað: skráin, tölvupósti eða safn (Microsoft SharePoint-möppu eða Geymslu Microsoft Azure).</span><span class="sxs-lookup"><span data-stu-id="6be4f-118">Configure ER destinations so that the output result of a format is directed to specific destination: file, email, or archive (Microsoft SharePoint folder or Microsoft Azure Storage).</span></span> | <span data-ttu-id="6be4f-119">Áður þegar ER skilgreining sem keyrði skilaboðagluggi birtist sem aðgerð notanda sem þarf til að vista eða opna skrá.</span><span class="sxs-lookup"><span data-stu-id="6be4f-119">Previously, when you ran an ER configuration, a message box appeared that required user action to save or open a file.</span></span> <span data-ttu-id="6be4f-120">Hægt er að forskilgreina áfangastað fyrir hverja skilgreiningarsnið og íhlut úttaks þess (möppu eða í skrá) sér.</span><span class="sxs-lookup"><span data-stu-id="6be4f-120">You can now pre-configure a destination for each format configuration and for each output component (a folder or a file) separately.</span></span> <span data-ttu-id="6be4f-121">Notendur sem eru veittar viðeigandi aðgangsheimildir einnig er hægt að breyta stillingar fyrir áfangastað á keyrslutíma.</span><span class="sxs-lookup"><span data-stu-id="6be4f-121">Users who have appropriate access rights can also modify destination settings at run time.</span></span> |

## <a name="pos--microsoft-dynamics-ax-retail"></a><span data-ttu-id="6be4f-122">POS - Microsoft Dynamics AX smásala</span><span class="sxs-lookup"><span data-stu-id="6be4f-122">POS – Microsoft Dynamics AX Retail</span></span>

| <span data-ttu-id="6be4f-123">Hvað hægt er að gera?</span><span class="sxs-lookup"><span data-stu-id="6be4f-123">What can you do?</span></span> | <span data-ttu-id="6be4f-124">Hví er þetta mikilvægt?</span><span class="sxs-lookup"><span data-stu-id="6be4f-124">Why is this important?</span></span> |
|------------------|------------------------|
| <span data-ttu-id="6be4f-125">Nota Google Chrome vafra.</span><span class="sxs-lookup"><span data-stu-id="6be4f-125">Use the Google Chrome browser.</span></span> | <span data-ttu-id="6be4f-126">Smásala nú hægt að hefja Sölukerfi úr skýi úr vafra Chrome og getur reynslu allar aðgerðir sem er tiltækt í Microsoft Edge og Internet Explorer útgáfu sölukerfi í skýinu.</span><span class="sxs-lookup"><span data-stu-id="6be4f-126">Retailers can now start Cloud POS from the Chrome browser, and can experience all the functionality that is available in the Microsoft Edge and Internet Explorer version of Cloud POS.</span></span> |

## <a name="financial-reporting"></a><span data-ttu-id="6be4f-127">Fjárhagsskýrslugerð</span><span class="sxs-lookup"><span data-stu-id="6be4f-127">Financial reporting</span></span>

| <span data-ttu-id="6be4f-128">Hvað hægt er að gera?</span><span class="sxs-lookup"><span data-stu-id="6be4f-128">What can you do?</span></span> | <span data-ttu-id="6be4f-129">Hví er þetta mikilvægt?</span><span class="sxs-lookup"><span data-stu-id="6be4f-129">Why is this important?</span></span> |
|------------------|------------------------|
| <span data-ttu-id="6be4f-130">Endurbyggja Fjárhagslegar skýrslugerðar gögn torg.</span><span class="sxs-lookup"><span data-stu-id="6be4f-130">Rebuild the Financial reporting data mart.</span></span> | <span data-ttu-id="6be4f-131">Þegar Dynamics AX gagnagrunnar eru færðir á milli umhverfa eða aðrar breytingar gerðar á umhverfinu gæti þurft að endurbyggja gagnagrunn Fjárhagslegar skýrslu.</span><span class="sxs-lookup"><span data-stu-id="6be4f-131">When you move Dynamics AX databases between environments or make other invasive changes to the environment, the Financial reporting database might have to be rebuilt.</span></span> <span data-ttu-id="6be4f-132">Windows PowerShell forskrift er nú veitt til að endurbyggja gagnagrunninum fyrir þig.</span><span class="sxs-lookup"><span data-stu-id="6be4f-132">A Windows PowerShell script is now provided to rebuild the database for you.</span></span> |
| <span data-ttu-id="6be4f-133">Ekki lengur hægt að velja skýrsluhönnun valkostina sem ekki eru gilda.</span><span class="sxs-lookup"><span data-stu-id="6be4f-133">You can no longer select report designer options that aren't valid.</span></span> | <span data-ttu-id="6be4f-134">Nokkrar skýrsluhönnun valkostina sem voru notaðir í útgáfur markaðinn í Management reporter ekki nota í þessari útgáfu Dynamics AX.</span><span class="sxs-lookup"><span data-stu-id="6be4f-134">Several report designer options that were used in the in-market versions of Management reporter don't apply to this version of Dynamics AX.</span></span> <span data-ttu-id="6be4f-135">Þessir valkostir voru tengdir fjárhagslega skýrsluhönnun, úttak og tengingu.</span><span class="sxs-lookup"><span data-stu-id="6be4f-135">These options were related to financial report design, output, and linking.</span></span> <span data-ttu-id="6be4f-136">Þessir valkostir hafa verið fjarlægðir úr fjárhagsskýrsluhönnuði til að koma í veg fyrir að notandavillur.</span><span class="sxs-lookup"><span data-stu-id="6be4f-136">These options have been removed from the financial report designer to prevent user errors.</span></span> |

## <a name="financial-management"></a><span data-ttu-id="6be4f-137">Fjármálastjórnun</span><span class="sxs-lookup"><span data-stu-id="6be4f-137">Financial management</span></span>

| <span data-ttu-id="6be4f-138">Hvað hægt er að gera?</span><span class="sxs-lookup"><span data-stu-id="6be4f-138">What can you do?</span></span> | <span data-ttu-id="6be4f-139">Hví er þetta mikilvægt?</span><span class="sxs-lookup"><span data-stu-id="6be4f-139">Why is this important?</span></span> |
|------------------|------------------------|
| <span data-ttu-id="6be4f-140">Mynda jákvæðar greiðsluskrár fyrir greiðslur viðskiptaskuldir.</span><span class="sxs-lookup"><span data-stu-id="6be4f-140">Generate positive pay files for accounts payable payments.</span></span> | <span data-ttu-id="6be4f-141">Mynda jákvæðar skrár til að hjálpa að koma í veg fyrir ávísanafals.</span><span class="sxs-lookup"><span data-stu-id="6be4f-141">Positive pay files can be generated to help prevent check fraud.</span></span> |

## <a name="warehouse-and-production"></a><span data-ttu-id="6be4f-142">Vöruhús og framleiðsla</span><span class="sxs-lookup"><span data-stu-id="6be4f-142">Warehouse and production</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6be4f-143">Hvað hægt er að gera?</span><span class="sxs-lookup"><span data-stu-id="6be4f-143">What can you do?</span></span></th>
<th><span data-ttu-id="6be4f-144">Hví er þetta mikilvægt?</span><span class="sxs-lookup"><span data-stu-id="6be4f-144">Why is this important?</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6be4f-145">Skilgreina vöruhús vinnu reglu sem stýrir stofnun vinnu fyrir safn af afurðum á tiltekna staði.</span><span class="sxs-lookup"><span data-stu-id="6be4f-145">Define a warehouse work policy that controls the creation of work for a set of products at specific locations.</span></span></td>
<td><span data-ttu-id="6be4f-146">Ferli vöruhúsa innihalda ekki alltaf vinnu.</span><span class="sxs-lookup"><span data-stu-id="6be4f-146">Warehouse processes don't always include work.</span></span> <span data-ttu-id="6be4f-147">Með því að nota nýju vinnustefnu vöruhúss , getur komið í veg fyrir stofnun vinnu fyrir tiltekt hráefnis og frágangur fullbúinna vara fyrir safn af afurðum á tiltekna staði.</span><span class="sxs-lookup"><span data-stu-id="6be4f-147">By using the new warehouse work policy, you can prevent work from being created for raw material picking and put-away of finished goods for a set of products at specific locations.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6be4f-148">Tilgreina að staðsetningu framleiðslufrálags ekki númeraplötustýrð.</span><span class="sxs-lookup"><span data-stu-id="6be4f-148">Specify that a production output location isn't license plate–controlled.</span></span></td>
<td><span data-ttu-id="6be4f-149">Getur tilgreina að staðsetningu framleiðslufrálags ekki númeraplötustýrð.</span><span class="sxs-lookup"><span data-stu-id="6be4f-149">You can now specify that a product output location isn't license plate–controlled.</span></span> <span data-ttu-id="6be4f-150">Til dæmis er þessi eiginleiki gagnlegt þegar þarfarakningu framleiðslupöntun skráir sem tilbúna beint á staðsetningu sem er eins og staðsetning framleiðsluinntaks framleiðslupöntunar niður á við vörur.</span><span class="sxs-lookup"><span data-stu-id="6be4f-150">For example, this feature is useful when an upstream production order reports items as finished directly to a location that acts as production input location for a downstream production order.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6be4f-151">Styðja Uppskriftir sem innihalda vörur með mismunandi afurðavíddir fyrir sömu vöruna.</span><span class="sxs-lookup"><span data-stu-id="6be4f-151">Support BOMs that include items with different product dimensions of the same item.</span></span></td>
<td><span data-ttu-id="6be4f-152">Þegar ein eða margar afurðarvíddum í framleiðslu er hægt að láta aðstæðum þar sem óskað er að framleiða vöru, annan vöruvíddasamsetning sömu vöru á grundvelli.</span><span class="sxs-lookup"><span data-stu-id="6be4f-152">When using one or multiple of the product dimensions in production, you can have situations where you would like to produce an item, based on a different variant of the same item.</span></span> <span data-ttu-id="6be4f-153">Nánari upplýsingar er að finna í <a href="https://blogs.msdn.microsoft.com/axmfg/2015/12/22/support-for-boms-that-includes-items-with-different-product-dimensions-of-the-same-item/">þessari blogg</a>.</span><span class="sxs-lookup"><span data-stu-id="6be4f-153">For more information, see <a href="https://blogs.msdn.microsoft.com/axmfg/2015/12/22/support-for-boms-that-includes-items-with-different-product-dimensions-of-the-same-item/">this blog</a>.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6be4f-154">Framleiðslupantanir með hringvirkni á fyrsta stigi um Uppskriftir þeirra eru undanskildar úr útreikning Uppskriftar fyrir efni eftirspurnarstjórnunar stigs.</span><span class="sxs-lookup"><span data-stu-id="6be4f-154">Production orders with circular structures at the first level of their BOMs are excluded from BOM level calculation for material resource planning.</span></span></td>
<td><span data-ttu-id="6be4f-155">Ekki er hægt að úthluta rétt uppskriftarstig afurðarafbrigði fyrir framleiðslupantanir sem veldur hringvirkni í stigveldi Uppskriftalínunnar.</span><span class="sxs-lookup"><span data-stu-id="6be4f-155">It is not possible to assign correct BOM levels to product variants for production orders that cause circularity in the BOM hierarchy.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6be4f-156">Reikna uppskriftarstig aðskildar fyrir áætlun tilfanga efni og kostnaður útreiknings:</span><span class="sxs-lookup"><span data-stu-id="6be4f-156">Calculate separate BOM levels for material resource planning and cost calculation:</span></span>
<ul>
<li><span data-ttu-id="6be4f-157">Fyrir áætlun efnistilfanga eru uppskriftarstig reiknuð út í nýju töflunni <strong>ReqItemLevel</strong>.</span><span class="sxs-lookup"><span data-stu-id="6be4f-157">For material resource planning, BOM levels are calculated in the new <strong>ReqItemLevel</strong> table.</span></span> <span data-ttu-id="6be4f-158">Framleiðslupantanir sem lokið eru hunsaðar við útreikning.</span><span class="sxs-lookup"><span data-stu-id="6be4f-158">Ended production orders are ignored in the calculation.</span></span></li>
<li><span data-ttu-id="6be4f-159">Fyrir útreikning framleiðslukostnaðar eru uppskriftarstig reiknuð út í <strong>InventTable</strong>.</span><span class="sxs-lookup"><span data-stu-id="6be4f-159">For production cost calculation, BOM levels are calculated in the <strong>InventTable</strong>.</span></span> <span data-ttu-id="6be4f-160">Framleiðslupantanir sem lokið eru teknar með við útreikning.</span><span class="sxs-lookup"><span data-stu-id="6be4f-160">Ended production orders are included in the calculation.</span></span></li>
</ul>
</td>
<td>
<ul>
<li><span data-ttu-id="6be4f-161">Þegar áætlun efnistilfanga er keyrð, til dæmis áætlun röðunar og niðurbrots á aðaláætlanagerð, þarf einungis að endurreikna uppskriftarstig sem eru notuð fyrir áætlun efnistilfanga.</span><span class="sxs-lookup"><span data-stu-id="6be4f-161">When running material resource planning, for example, master planning plan scheduling and explosion, only BOM levels used for material resource planning need to be recalculated.</span></span> <span data-ttu-id="6be4f-162">Með öðrum orðum, það er engin þörf á að reikna uppskriftarstig er notað fyrir útreikning kostnaðar.</span><span class="sxs-lookup"><span data-stu-id="6be4f-162">In other words, there is no need to calculate BOM levels used for production costing calculation.</span></span></li>
<li><span data-ttu-id="6be4f-163">Þegar keyrðar eru aðgerðir kostnaðarútreiknings, til dæmis birgðalokunar, þarf einungis að endurreikna uppskriftarstig sem eru notuð við útreikning framleiðslukostnaðar.</span><span class="sxs-lookup"><span data-stu-id="6be4f-163">When running costing operations, for example, inventory closing, only BOM levels used for production costing calculation need to be recalculated.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="6be4f-164">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="6be4f-164">Additional resources</span></span>

[<span data-ttu-id="6be4f-165">Nýjungar eða breytingar á heimasíðu Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="6be4f-165">What's new or changed in Finance and Operations home page</span></span>](whats-new-changed.md)

[<span data-ttu-id="6be4f-166">Nýjar eða uppfærðar verkefnaleiðbeiningar (maí 2016)</span><span class="sxs-lookup"><span data-stu-id="6be4f-166">New or updated task guides (May 2016)</span></span>](new-updated-task-guides-available-may-2016.md)
