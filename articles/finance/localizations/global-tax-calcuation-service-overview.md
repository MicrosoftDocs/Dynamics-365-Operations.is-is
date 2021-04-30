---
title: Skattaútreikningur (forskoðun)
description: Þetta efnisatriði skýrir heildarumfang og eiginleika skattaútreikningsgetu.
author: wangchen
ms.date: 04/12/2021
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
ms.openlocfilehash: 3df952e0632807e55f176e63dc2047be5e622ec2
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/13/2021
ms.locfileid: "5892350"
---
# <a name="tax-calculation-preview"></a><span data-ttu-id="6c128-103">Skattaútreikningur (forskoðun)</span><span class="sxs-lookup"><span data-stu-id="6c128-103">Tax Calculation (Preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="6c128-104">Skattaútreikningur er þjónusta með stillanlegri þjónustu fyrir marga notendur sem gerir altæku skattkerfi kleift að einfalda skattaákvörðun og útreikning og gera það sjálfvirkt.</span><span class="sxs-lookup"><span data-stu-id="6c128-104">Tax Calculation is a hyper-scalable multitenant service that enables the global tax engine to automate and simplify the tax determination and calculation process.</span></span> <span data-ttu-id="6c128-105">Skattvélin er fullkomlega stillanleg.</span><span class="sxs-lookup"><span data-stu-id="6c128-105">The tax engine is fully configurable.</span></span> <span data-ttu-id="6c128-106">Einingarnar sem hægt er að stilla fela í sér, en takmarkast ekki við, skattalega gagnalíkansins, skattkóða, fylkisins fyrir skattskyldu og formúlu skattútreiknings.</span><span class="sxs-lookup"><span data-stu-id="6c128-106">The elements that can be configured include, but aren't limited to, the taxable data model, tax code, tax applicability matrix, and tax calculation formula.</span></span> <span data-ttu-id="6c128-107">Skattkerfið keyrir á Microsoft Azure verkvangi og býður upp á nútímatækni og sveigjanleika.</span><span class="sxs-lookup"><span data-stu-id="6c128-107">The tax engine runs on the Microsoft Azure core services platform, and offers modern technology and exponential scalability.</span></span>

<span data-ttu-id="6c128-108">Skattútreikningur er samþættur við Dynamics 365 Finance og Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="6c128-108">Tax Calculation integrates with Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="6c128-109">Að lokum verður hún einnig samþætt við Dynamics 365 Project Operations, Dynamics 365 Commerce og önnur forrit frá fyrstu og þriðju aðilum.</span><span class="sxs-lookup"><span data-stu-id="6c128-109">Eventually, it will also integrate with Dynamics 365 Project Operations, Dynamics 365 Commerce, and other first-party and third-party applications.</span></span>

<span data-ttu-id="6c128-110">Skattaútreikningur er skattakerfi frá Microsoft sem býður upp á mikinn sveigjanleika.</span><span class="sxs-lookup"><span data-stu-id="6c128-110">Tax Calculation is a microservice-based tax engine that offers exponential scalability.</span></span> <span data-ttu-id="6c128-111">Það getur hjálpað þér að framkvæma eftirfarandi verk:</span><span class="sxs-lookup"><span data-stu-id="6c128-111">It can help you perform the following tasks:</span></span>

- <span data-ttu-id="6c128-112">Grunnstilla skattaútreikning með Regulatory Configuration Service (RCS).</span><span class="sxs-lookup"><span data-stu-id="6c128-112">Configure Tax Calculation through Regulatory Configuration Service (RCS).</span></span> <span data-ttu-id="6c128-113">RCS er endurbætt útgáfa af hönnuði rafrænnar útgáfu og er fáanleg sem sjálfstæð þjónusta.</span><span class="sxs-lookup"><span data-stu-id="6c128-113">RCS is an enhanced version of the Electronic reporting (ER) designer and is available as a standalone service.</span></span>
- <span data-ttu-id="6c128-114">Grunnstilla skattafylki til að ákvarða sjálfkrafa skattkóða og taxta.</span><span class="sxs-lookup"><span data-stu-id="6c128-114">Configure the tax matrix to automatically determine tax codes and rates.</span></span>
- <span data-ttu-id="6c128-115">Grunnstilla skattafylki til að ákvarða sjálfkrafa skattskráningarnúmerið.</span><span class="sxs-lookup"><span data-stu-id="6c128-115">Configure the tax matrix to automatically determine the tax registration number.</span></span>
- <span data-ttu-id="6c128-116">Grunnstilla hönnuð skattaútreiknings til að skilgreina formúlur og skilyrði.</span><span class="sxs-lookup"><span data-stu-id="6c128-116">Configure the tax calculation designer to define formulas and conditions.</span></span>
- <span data-ttu-id="6c128-117">Deildu skattákvörðun og útreikningslausn á milli lögaðila.</span><span class="sxs-lookup"><span data-stu-id="6c128-117">Share the tax determination and calculation solution across legal entities.</span></span>

<span data-ttu-id="6c128-118">Til að nota skattaútreikningsþjónustu skal setja upp innbótina fyrir skattaútreikningsþjónustu ur verkefninu í Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="6c128-118">To use the tax calculation service, install the tax calculation service add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="6c128-119">Ljúkið síðan uppsetningunni í RCS og virkið skattútreikningaþjónustuna í Finance and Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="6c128-119">Then complete the setup in RCS, and enable the tax calculation service in Finance and Supply Chain Management.</span></span> <span data-ttu-id="6c128-120">Frekari upplýsingar eru í [Hafist handa með skattþjónustu](./global-get-started-with-tax-calculation-service.md).</span><span class="sxs-lookup"><span data-stu-id="6c128-120">For more information, see [Get started with tax service](./global-get-started-with-tax-calculation-service.md).</span></span>

## <a name="availability"></a><span data-ttu-id="6c128-121">Til ráðstöfunar</span><span class="sxs-lookup"><span data-stu-id="6c128-121">Availability</span></span>

<span data-ttu-id="6c128-122">Skattaútreikningur er aðeins í boði í sandkassaumhverfi og til valinna viðskiptavina í gegnum almenna forútgáfu.</span><span class="sxs-lookup"><span data-stu-id="6c128-122">Tax Calculation is available only in sandbox environments and to selected customers, through a public preview program.</span></span> <span data-ttu-id="6c128-123">Að lokum mun hún verða aðgengileg öllum viðskiptavinum og í framleiðsluferli.</span><span class="sxs-lookup"><span data-stu-id="6c128-123">Eventually, it will become generally available to all customers and in production environments.</span></span>

<span data-ttu-id="6c128-124">Nýjir eiginleikar verða áfram kynntir til sögunnar og þess vegna þarf að gæta þess að skoða nýjustu fylgiskjöl til að fá upplýsingar um umfang studdra eiginleika.</span><span class="sxs-lookup"><span data-stu-id="6c128-124">New features will continue to be delivered, so be sure to check the most up-to-date documentation often to learn about the coverage and scope of supported features.</span></span>

<span data-ttu-id="6c128-125">Skattaútreikningur er í boði á eftirfarandi staðsetningum Azure.</span><span class="sxs-lookup"><span data-stu-id="6c128-125">Tax Calculation is deployed in the following Azure geographies.</span></span> <span data-ttu-id="6c128-126">Hún verður einnig í boði á fleiri Azure-landsvæðum í samræmi við þarfir viðskiptavina:</span><span class="sxs-lookup"><span data-stu-id="6c128-126">It will also be deployed to more Azure geographies, based on customer needs:</span></span>

- <span data-ttu-id="6c128-127">Bandaríkin</span><span class="sxs-lookup"><span data-stu-id="6c128-127">United States</span></span>
- <span data-ttu-id="6c128-128">Evrópa</span><span class="sxs-lookup"><span data-stu-id="6c128-128">Europe</span></span>

> [!NOTE]
> <span data-ttu-id="6c128-129">Skattaútreikningur styður ekki uppsetningu Dynamics 365 á staðnum.</span><span class="sxs-lookup"><span data-stu-id="6c128-129">Tax Calculation doesn't support on-premises deployments of Dynamics 365.</span></span> <span data-ttu-id="6c128-130">Hún styður einnig ekki fyrri útgáfur, eins og Dynamics AX 2012.</span><span class="sxs-lookup"><span data-stu-id="6c128-130">It also doesn't support earlier versions, such as Dynamics AX 2012.</span></span>

## <a name="feature-highlights"></a><span data-ttu-id="6c128-131">Helstu atriði eiginleika</span><span class="sxs-lookup"><span data-stu-id="6c128-131">Feature highlights</span></span>

- <span data-ttu-id="6c128-132">Stillanlegt skattafylki til að ákvarða og reikna út skatt sjálfkrafa</span><span class="sxs-lookup"><span data-stu-id="6c128-132">A configurable tax matrix to automatically determine and calculate tax</span></span>
- <span data-ttu-id="6c128-133">Stuðningur fyrir mörg skattskráningarnúmer</span><span class="sxs-lookup"><span data-stu-id="6c128-133">Support for multiple tax registration numbers</span></span>
- <span data-ttu-id="6c128-134">Stuðningur flutningspöntunar fyrir skattákvörðun og útreikning</span><span class="sxs-lookup"><span data-stu-id="6c128-134">Transfer order support for tax determination and calculation</span></span>
- <span data-ttu-id="6c128-135">Stuðningur flutningspöntunar fyrir ákvörðun margra skattnúmera</span><span class="sxs-lookup"><span data-stu-id="6c128-135">Transfer order support for determination of multiple tax registration numbers</span></span>

## <a name="supported-transactions"></a><span data-ttu-id="6c128-136">Studdar færslur</span><span class="sxs-lookup"><span data-stu-id="6c128-136">Supported transactions</span></span>

<span data-ttu-id="6c128-137">Lögaðili og færsluhirðir geta gert skattaútreikning virkan.</span><span class="sxs-lookup"><span data-stu-id="6c128-137">Tax Calculation can be enabled by legal entity and transaction.</span></span> <span data-ttu-id="6c128-138">Eftirfarandi færslur eru studdar:</span><span class="sxs-lookup"><span data-stu-id="6c128-138">The following transactions are supported:</span></span>

- <span data-ttu-id="6c128-139">Söluferli</span><span class="sxs-lookup"><span data-stu-id="6c128-139">Sales process</span></span>

    - <span data-ttu-id="6c128-140">Sölutilboð</span><span class="sxs-lookup"><span data-stu-id="6c128-140">Sales quotation</span></span>
    - <span data-ttu-id="6c128-141">Sölupöntun</span><span class="sxs-lookup"><span data-stu-id="6c128-141">Sales order</span></span>
    - <span data-ttu-id="6c128-142">Staðfesting</span><span class="sxs-lookup"><span data-stu-id="6c128-142">Confirmation</span></span>
    - <span data-ttu-id="6c128-143">Tiltektarlisti</span><span class="sxs-lookup"><span data-stu-id="6c128-143">Picking list</span></span>
    - <span data-ttu-id="6c128-144">Fylgiseðill</span><span class="sxs-lookup"><span data-stu-id="6c128-144">Packing slip</span></span>
    - <span data-ttu-id="6c128-145">Sölureikningur</span><span class="sxs-lookup"><span data-stu-id="6c128-145">Sales invoice</span></span>
    - <span data-ttu-id="6c128-146">Kreditnóta</span><span class="sxs-lookup"><span data-stu-id="6c128-146">Credit note</span></span>
    - <span data-ttu-id="6c128-147">Skila pöntun</span><span class="sxs-lookup"><span data-stu-id="6c128-147">Return order</span></span>
    - <span data-ttu-id="6c128-148">Ýmis hausgjöld</span><span class="sxs-lookup"><span data-stu-id="6c128-148">Header miscellaneous charge</span></span>
    - <span data-ttu-id="6c128-149">Ýmis línugjöld</span><span class="sxs-lookup"><span data-stu-id="6c128-149">Line miscellaneous charge</span></span>

- <span data-ttu-id="6c128-150">Innkaupaferli</span><span class="sxs-lookup"><span data-stu-id="6c128-150">Purchase process</span></span>

    - <span data-ttu-id="6c128-151">Innkaupapöntun</span><span class="sxs-lookup"><span data-stu-id="6c128-151">Purchase order</span></span>
    - <span data-ttu-id="6c128-152">Staðfesting</span><span class="sxs-lookup"><span data-stu-id="6c128-152">Confirmation</span></span>
    - <span data-ttu-id="6c128-153">Komulisti</span><span class="sxs-lookup"><span data-stu-id="6c128-153">Receipts list</span></span>
    - <span data-ttu-id="6c128-154">Innhreyfingarskjal afurða</span><span class="sxs-lookup"><span data-stu-id="6c128-154">Product receipt</span></span>
    - <span data-ttu-id="6c128-155">Innkaupareikningur</span><span class="sxs-lookup"><span data-stu-id="6c128-155">Purchase invoice</span></span>
    - <span data-ttu-id="6c128-156">Ýmis hausgjöld</span><span class="sxs-lookup"><span data-stu-id="6c128-156">Header miscellaneous charge</span></span>
    - <span data-ttu-id="6c128-157">Ýmis línugjöld</span><span class="sxs-lookup"><span data-stu-id="6c128-157">Line miscellaneous charge</span></span>
    - <span data-ttu-id="6c128-158">Kreditnóta</span><span class="sxs-lookup"><span data-stu-id="6c128-158">Credit note</span></span>
    - <span data-ttu-id="6c128-159">Skila pöntun</span><span class="sxs-lookup"><span data-stu-id="6c128-159">Return order</span></span>
    - <span data-ttu-id="6c128-160">Innkaupabeiðni</span><span class="sxs-lookup"><span data-stu-id="6c128-160">Purchase requisition</span></span>
    - <span data-ttu-id="6c128-161">Ýmis gjöld innkaupabeiðnilínu</span><span class="sxs-lookup"><span data-stu-id="6c128-161">Purchase requisition line miscellaneous charge</span></span>
    - <span data-ttu-id="6c128-162">Beiðni um tilboð</span><span class="sxs-lookup"><span data-stu-id="6c128-162">Request for quotation</span></span>
    - <span data-ttu-id="6c128-163">Ýmis hausgjöld fyrir beiðni um tilboð</span><span class="sxs-lookup"><span data-stu-id="6c128-163">Request for quotation header miscellaneous charge</span></span>
    - <span data-ttu-id="6c128-164">Ýmis línugjöld fyrir beiðni um tilboð</span><span class="sxs-lookup"><span data-stu-id="6c128-164">Request for quotation line miscellaneous charge</span></span>

- <span data-ttu-id="6c128-165">Birgðavinnsla</span><span class="sxs-lookup"><span data-stu-id="6c128-165">Inventory process</span></span>

    - <span data-ttu-id="6c128-166">Flutningspantanir - senda</span><span class="sxs-lookup"><span data-stu-id="6c128-166">Transfer order – ship</span></span>
    - <span data-ttu-id="6c128-167">Móttaka flutningspöntunar</span><span class="sxs-lookup"><span data-stu-id="6c128-167">Transfer order – receive</span></span>

## <a name="related-resources"></a><span data-ttu-id="6c128-168">Tengd tilföng</span><span class="sxs-lookup"><span data-stu-id="6c128-168">Related resources</span></span>

[<span data-ttu-id="6c128-169">Hafist handa með skattþjónustu</span><span class="sxs-lookup"><span data-stu-id="6c128-169">Get started with tax service</span></span>](./global-get-started-with-tax-calculation-service.md)

[<span data-ttu-id="6c128-170">Mörg VSK-skráningarnúmer</span><span class="sxs-lookup"><span data-stu-id="6c128-170">Multiple VAT registration number</span></span>](./emea-multiple-vat-registration-numbers.md)

[<span data-ttu-id="6c128-171">Stuðningur skattaeiginleika fyrir flutningspöntun</span><span class="sxs-lookup"><span data-stu-id="6c128-171">Tax feature support for transfer order</span></span>](./tasks/tax-feature-support-for-transfer-order.md)

[<span data-ttu-id="6c128-172">Hvernig á að byggja upp viðbót í skattsþjónustu</span><span class="sxs-lookup"><span data-stu-id="6c128-172">How to build extension in tax service</span></span>](./tax-service-add-data-fields-tax-integration-by-extension.md)