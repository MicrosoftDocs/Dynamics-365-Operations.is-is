---
title: Skattaútreikningsþjónusta (forskoðun)
description: Þetta efnisatriði skýrir heildarumfang og eiginleika skattaútreikningaþjónustunnar.
author: wangchen
ms.date: 03/02/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 518d3fda7b97e55d23beea6a1ba0e50b44a7aa0e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818225"
---
# <a name="tax-calculation-service-preview"></a><span data-ttu-id="0bae6-103">Skattaútreikningsþjónusta (forskoðun)</span><span class="sxs-lookup"><span data-stu-id="0bae6-103">Tax calculation service (Preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="0bae6-104">Skattaútreikningsþjónustan er þjónusta með stillanlegri þjónustu fyrir marga notendur sem gerir altæku skattkerfi kleift að einfalda skattaákvörðun og útreikning og gera það sjálfvirkt.</span><span class="sxs-lookup"><span data-stu-id="0bae6-104">The tax calculation service is a hyper-scalable multitenant service that enables the global tax engine to automate and simplify the tax determination and calculation process.</span></span> <span data-ttu-id="0bae6-105">Skattvélin er fullkomlega stillanleg.</span><span class="sxs-lookup"><span data-stu-id="0bae6-105">The tax engine is fully configurable.</span></span> <span data-ttu-id="0bae6-106">Einingarnar sem hægt er að stilla fela í sér, en takmarkast ekki við, skattalega gagnalíkansins, skattkóða, fylkisins fyrir skattskyldu og formúlu skattútreiknings.</span><span class="sxs-lookup"><span data-stu-id="0bae6-106">The elements that can be configured include, but aren't limited to, the taxable data model, tax code, tax applicability matrix, and tax calculation formula.</span></span> <span data-ttu-id="0bae6-107">Skattkerfið keyrir á Microsoft Azure verkvangi og býður upp á nútímatækni og sveigjanleika.</span><span class="sxs-lookup"><span data-stu-id="0bae6-107">The tax engine runs on the Microsoft Azure core services platform, and offers modern technology and exponential scalability.</span></span>

<span data-ttu-id="0bae6-108">Skattútreikningaþjónustan er samþætt við Dynamics 365 Finance og Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="0bae6-108">The tax calculation service integrates with Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="0bae6-109">Að lokum verður hún einnig samþætt við Dynamics 365 Project Operations, Dynamics 365 Commerce og önnur forrit frá fyrstu og þriðju aðilum.</span><span class="sxs-lookup"><span data-stu-id="0bae6-109">Eventually, it will also integrate with Dynamics 365 Project Operations, Dynamics 365 Commerce, and other first-party and third-party applications.</span></span>

<span data-ttu-id="0bae6-110">Skattaútreikningsþjónustan er skattakerfi frá Microsoft sem býður upp á mikinn sveigjanleika.</span><span class="sxs-lookup"><span data-stu-id="0bae6-110">The tax calculation service is a Microsoft-based tax engine that offers exponential scalability.</span></span> <span data-ttu-id="0bae6-111">Það getur hjálpað þér að framkvæma eftirfarandi verk:</span><span class="sxs-lookup"><span data-stu-id="0bae6-111">It can help you perform the following tasks:</span></span>

- <span data-ttu-id="0bae6-112">Grunnstilla skattaútreikningsþjónustu með Regulatory Configuration Service (RCS).</span><span class="sxs-lookup"><span data-stu-id="0bae6-112">Configure the tax calculation service through Regulatory Configuration Service (RCS).</span></span> <span data-ttu-id="0bae6-113">RCS er endurbætt útgáfa af hönnuði rafrænnar útgáfu og er fáanleg sem sjálfstæð þjónusta.</span><span class="sxs-lookup"><span data-stu-id="0bae6-113">RCS is an enhanced version of the Electronic reporting (ER) designer and is available as a standalone service.</span></span>
- <span data-ttu-id="0bae6-114">Grunnstilla skattafylki til að ákvarða sjálfkrafa skattkóða og taxta.</span><span class="sxs-lookup"><span data-stu-id="0bae6-114">Configure the tax matrix to automatically determine tax codes and rates.</span></span>
- <span data-ttu-id="0bae6-115">Grunnstilla skattafylki til að ákvarða sjálfkrafa skattskráningarnúmerið.</span><span class="sxs-lookup"><span data-stu-id="0bae6-115">Configure the tax matrix to automatically determine the tax registration number.</span></span>
- <span data-ttu-id="0bae6-116">Grunnstilla hönnuð skattaútreiknings til að skilgreina formúlur og skilyrði.</span><span class="sxs-lookup"><span data-stu-id="0bae6-116">Configure the tax calculation designer to define formulas and conditions.</span></span>
- <span data-ttu-id="0bae6-117">Deildu skattákvörðun og útreikningslausn á milli lögaðila.</span><span class="sxs-lookup"><span data-stu-id="0bae6-117">Share the tax determination and calculation solution across legal entities.</span></span>

<span data-ttu-id="0bae6-118">Til að nota skattaútreikningsþjónustu skal setja upp innbótina fyrir skattaútreikningsþjónustu ur verkefninu í Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="0bae6-118">To use the tax calculation service, install the tax calculation service add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="0bae6-119">Ljúkið síðan uppsetningunni í RCS og virkið skattútreikningaþjónustuna í Finance and Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="0bae6-119">Then complete the setup in RCS, and enable the tax calculation service in Finance and Supply Chain Management.</span></span> <span data-ttu-id="0bae6-120">Frekari upplýsingar eru í [Hafist handa með skattþjónustu](https://go.microsoft.com/fwlink/?linkid=2138482).</span><span class="sxs-lookup"><span data-stu-id="0bae6-120">For more information, see [Get started with tax service](https://go.microsoft.com/fwlink/?linkid=2138482).</span></span>

## <a name="availability"></a><span data-ttu-id="0bae6-121">Til ráðstöfunar</span><span class="sxs-lookup"><span data-stu-id="0bae6-121">Availability</span></span>

<span data-ttu-id="0bae6-122">Skattaútreikningaþjónustan er aðeins í boði í sandkassaumhverfi og til valinna viðskiptavina í gegnum almenna forútgáfu.</span><span class="sxs-lookup"><span data-stu-id="0bae6-122">The tax calculation service is available only in sandbox environments and to selected customers, through a public preview program.</span></span> <span data-ttu-id="0bae6-123">Að lokum mun hún verða aðgengileg öllum viðskiptavinum og í framleiðsluferli.</span><span class="sxs-lookup"><span data-stu-id="0bae6-123">Eventually, it will become generally available to all customers and in production environments.</span></span>

<span data-ttu-id="0bae6-124">Áfram verður boðið upp á nýja eiginleika í skattaútreikningsþjónustu.</span><span class="sxs-lookup"><span data-stu-id="0bae6-124">New features will continue to be delivered in the tax calculation service.</span></span> <span data-ttu-id="0bae6-125">Þess vegna þarf að gæta þess að skoða nýjustu fylgiskjöl til að fá upplýsingar um umfang studdra eiginleika.</span><span class="sxs-lookup"><span data-stu-id="0bae6-125">Therefore, be sure to check the most up-to-date documentation often to learn about the coverage and scope of supported features.</span></span>

<span data-ttu-id="0bae6-126">Skattaútreikningsþjónustan er í boði á eftirfarandi staðsetningum Azure.</span><span class="sxs-lookup"><span data-stu-id="0bae6-126">The tax calculation service is deployed in the following Azure geographies.</span></span> <span data-ttu-id="0bae6-127">Hún verður einnig í boði á fleiri Azure-landsvæðum í samræmi við þarfir viðskiptavina:</span><span class="sxs-lookup"><span data-stu-id="0bae6-127">It will also be deployed to more Azure geographies, based on customer needs:</span></span>

- <span data-ttu-id="0bae6-128">Bandaríkin</span><span class="sxs-lookup"><span data-stu-id="0bae6-128">United States</span></span>
- <span data-ttu-id="0bae6-129">Evrópa</span><span class="sxs-lookup"><span data-stu-id="0bae6-129">Europe</span></span>
- <span data-ttu-id="0bae6-130">Frakkland</span><span class="sxs-lookup"><span data-stu-id="0bae6-130">France</span></span>
- <span data-ttu-id="0bae6-131">Bretland</span><span class="sxs-lookup"><span data-stu-id="0bae6-131">United Kingdom</span></span>

> [!NOTE]
> <span data-ttu-id="0bae6-132">Útreikningaþjónustan styður ekki uppsetningu Dynamics 365 á staðnum.</span><span class="sxs-lookup"><span data-stu-id="0bae6-132">The tax calculation service doesn't support on-premises deployments of Dynamics 365.</span></span> <span data-ttu-id="0bae6-133">Hún styður einnig ekki fyrri útgáfur, eins og Dynamics AX 2012.</span><span class="sxs-lookup"><span data-stu-id="0bae6-133">It also doesn't support earlier versions, such as Dynamics AX 2012.</span></span>

## <a name="feature-highlights"></a><span data-ttu-id="0bae6-134">Helstu atriði eiginleika</span><span class="sxs-lookup"><span data-stu-id="0bae6-134">Feature highlights</span></span>

- <span data-ttu-id="0bae6-135">Stillanlegt skattafylki til að ákvarða og reikna út skatt sjálfkrafa</span><span class="sxs-lookup"><span data-stu-id="0bae6-135">A configurable tax matrix to automatically determine and calculate tax</span></span>
- <span data-ttu-id="0bae6-136">Stuðningur fyrir mörg virðisaukaskattsnúmer (VSK)</span><span class="sxs-lookup"><span data-stu-id="0bae6-136">Support for multiple value-added tax (VAT) registration numbers</span></span>
- <span data-ttu-id="0bae6-137">Stuðningur flutningspöntunar fyrir skattákvörðun og útreikning</span><span class="sxs-lookup"><span data-stu-id="0bae6-137">Transfer order support for tax determination and calculation</span></span>
- <span data-ttu-id="0bae6-138">Stuðningur flutningspöntunar fyrir ákvörðun margra VSK-númera</span><span class="sxs-lookup"><span data-stu-id="0bae6-138">Transfer order support for determination of multiple VAT registration numbers</span></span>

## <a name="supported-transactions"></a><span data-ttu-id="0bae6-139">Studdar færslur</span><span class="sxs-lookup"><span data-stu-id="0bae6-139">Supported transactions</span></span>

<span data-ttu-id="0bae6-140">Lögaðili og færsluhirðir getur gert skattalíkanið virkt.</span><span class="sxs-lookup"><span data-stu-id="0bae6-140">The tax calculation service can be enabled by legal entity and transaction.</span></span> <span data-ttu-id="0bae6-141">Eftirfarandi færslur eru studdar:</span><span class="sxs-lookup"><span data-stu-id="0bae6-141">The following transactions are supported:</span></span>

- <span data-ttu-id="0bae6-142">Söluferli</span><span class="sxs-lookup"><span data-stu-id="0bae6-142">Sales process</span></span>

    - <span data-ttu-id="0bae6-143">Sölutilboð</span><span class="sxs-lookup"><span data-stu-id="0bae6-143">Sales quotation</span></span>
    - <span data-ttu-id="0bae6-144">Sölupöntun</span><span class="sxs-lookup"><span data-stu-id="0bae6-144">Sales order</span></span>
    - <span data-ttu-id="0bae6-145">Staðfesting</span><span class="sxs-lookup"><span data-stu-id="0bae6-145">Confirmation</span></span>
    - <span data-ttu-id="0bae6-146">Tiltektarlisti</span><span class="sxs-lookup"><span data-stu-id="0bae6-146">Picking list</span></span>
    - <span data-ttu-id="0bae6-147">Fylgiseðill</span><span class="sxs-lookup"><span data-stu-id="0bae6-147">Packing slip</span></span>
    - <span data-ttu-id="0bae6-148">Sölureikningur</span><span class="sxs-lookup"><span data-stu-id="0bae6-148">Sales invoice</span></span>
    - <span data-ttu-id="0bae6-149">Kreditnóta</span><span class="sxs-lookup"><span data-stu-id="0bae6-149">Credit note</span></span>
    - <span data-ttu-id="0bae6-150">Skila pöntun</span><span class="sxs-lookup"><span data-stu-id="0bae6-150">Return order</span></span>
    - <span data-ttu-id="0bae6-151">Ýmis hausgjöld</span><span class="sxs-lookup"><span data-stu-id="0bae6-151">Header miscellaneous charge</span></span>
    - <span data-ttu-id="0bae6-152">Ýmis línugjöld</span><span class="sxs-lookup"><span data-stu-id="0bae6-152">Line miscellaneous charge</span></span>

- <span data-ttu-id="0bae6-153">Innkaupaferli</span><span class="sxs-lookup"><span data-stu-id="0bae6-153">Purchase process</span></span>

    - <span data-ttu-id="0bae6-154">Innkaupapöntun</span><span class="sxs-lookup"><span data-stu-id="0bae6-154">Purchase order</span></span>
    - <span data-ttu-id="0bae6-155">Staðfesting</span><span class="sxs-lookup"><span data-stu-id="0bae6-155">Confirmation</span></span>
    - <span data-ttu-id="0bae6-156">Komulisti</span><span class="sxs-lookup"><span data-stu-id="0bae6-156">Receipts list</span></span>
    - <span data-ttu-id="0bae6-157">Innhreyfingarskjal afurða</span><span class="sxs-lookup"><span data-stu-id="0bae6-157">Product receipt</span></span>
    - <span data-ttu-id="0bae6-158">Innkaupareikningur</span><span class="sxs-lookup"><span data-stu-id="0bae6-158">Purchase invoice</span></span>
    - <span data-ttu-id="0bae6-159">Ýmis hausgjöld</span><span class="sxs-lookup"><span data-stu-id="0bae6-159">Header miscellaneous charge</span></span>
    - <span data-ttu-id="0bae6-160">Ýmis línugjöld</span><span class="sxs-lookup"><span data-stu-id="0bae6-160">Line miscellaneous charge</span></span>
    - <span data-ttu-id="0bae6-161">Kreditnóta</span><span class="sxs-lookup"><span data-stu-id="0bae6-161">Credit note</span></span>
    - <span data-ttu-id="0bae6-162">Skila pöntun</span><span class="sxs-lookup"><span data-stu-id="0bae6-162">Return order</span></span>
    - <span data-ttu-id="0bae6-163">Innkaupabeiðni</span><span class="sxs-lookup"><span data-stu-id="0bae6-163">Purchase requisition</span></span>
    - <span data-ttu-id="0bae6-164">Ýmis gjöld innkaupabeiðnilínu</span><span class="sxs-lookup"><span data-stu-id="0bae6-164">Purchase requisition line miscellaneous charge</span></span>
    - <span data-ttu-id="0bae6-165">Beiðni um tilboð</span><span class="sxs-lookup"><span data-stu-id="0bae6-165">Request for quotation</span></span>
    - <span data-ttu-id="0bae6-166">Ýmis hausgjöld fyrir beiðni um tilboð</span><span class="sxs-lookup"><span data-stu-id="0bae6-166">Request for quotation header miscellaneous charge</span></span>
    - <span data-ttu-id="0bae6-167">Ýmis línugjöld fyrir beiðni um tilboð</span><span class="sxs-lookup"><span data-stu-id="0bae6-167">Request for quotation line miscellaneous charge</span></span>

- <span data-ttu-id="0bae6-168">Birgðavinnsla</span><span class="sxs-lookup"><span data-stu-id="0bae6-168">Inventory process</span></span>

    - <span data-ttu-id="0bae6-169">Flutningspantanir - senda</span><span class="sxs-lookup"><span data-stu-id="0bae6-169">Transfer order – ship</span></span>
    - <span data-ttu-id="0bae6-170">Móttaka flutningspöntunar</span><span class="sxs-lookup"><span data-stu-id="0bae6-170">Transfer order – receive</span></span>

## <a name="related-resources"></a><span data-ttu-id="0bae6-171">Tengd tilföng</span><span class="sxs-lookup"><span data-stu-id="0bae6-171">Related resources</span></span>

[<span data-ttu-id="0bae6-172">Hafist handa með skattþjónustu</span><span class="sxs-lookup"><span data-stu-id="0bae6-172">Get started with tax service</span></span>](https://go.microsoft.com/fwlink/?linkid=2138482)

[<span data-ttu-id="0bae6-173">Mörg VSK-skráningarnúmer</span><span class="sxs-lookup"><span data-stu-id="0bae6-173">Multiple VAT registration number</span></span>](https://go.microsoft.com/fwlink/?linkid=2153387)

[<span data-ttu-id="0bae6-174">Stuðningur skattaeiginleika fyrir flutningspöntun</span><span class="sxs-lookup"><span data-stu-id="0bae6-174">Tax feature support for transfer order</span></span>](https://go.microsoft.com/fwlink/?linkid=2153388)

[<span data-ttu-id="0bae6-175">Hvernig á að byggja upp viðbót í skattsþjónustu</span><span class="sxs-lookup"><span data-stu-id="0bae6-175">How to build extension in tax service</span></span>](https://go.microsoft.com/fwlink/?linkid=2138483)
