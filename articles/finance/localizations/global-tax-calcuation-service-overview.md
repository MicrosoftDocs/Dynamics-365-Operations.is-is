---
title: Skattaútreikningur (forskoðun)
description: Þetta efnisatriði skýrir heildarumfang og eiginleika skattaútreikningsgetu.
author: wangchen
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 9daa6e001200d03a2639974fb6de618d77ddf09d
ms.sourcegitcommit: cb282e8d2306ab71adf80a84346a6863d2d019e8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2021
ms.locfileid: "6184102"
---
# <a name="tax-calculation-preview"></a><span data-ttu-id="08719-103">Skattaútreikningur (forskoðun)</span><span class="sxs-lookup"><span data-stu-id="08719-103">Tax Calculation (Preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="08719-104">Skattaútreikningur er þjónusta með stillanlegri þjónustu fyrir marga notendur sem gerir altæku skattkerfi kleift að einfalda skattaákvörðun og útreikning og gera það sjálfvirkt.</span><span class="sxs-lookup"><span data-stu-id="08719-104">Tax Calculation is a hyper-scalable multitenant service that enables the global tax engine to automate and simplify the tax determination and calculation process.</span></span> <span data-ttu-id="08719-105">Skattvélin er fullkomlega stillanleg.</span><span class="sxs-lookup"><span data-stu-id="08719-105">The tax engine is fully configurable.</span></span> <span data-ttu-id="08719-106">Einingarnar sem hægt er að stilla fela í sér, en takmarkast ekki við, skattalega gagnalíkansins, skattkóða, fylkisins fyrir skattskyldu og formúlu skattútreiknings.</span><span class="sxs-lookup"><span data-stu-id="08719-106">The elements that can be configured include, but aren't limited to, the taxable data model, tax code, tax applicability matrix, and tax calculation formula.</span></span> <span data-ttu-id="08719-107">Skattkerfið keyrir á Microsoft Azure verkvangi og býður upp á nútímatækni og sveigjanleika.</span><span class="sxs-lookup"><span data-stu-id="08719-107">The tax engine runs on the Microsoft Azure core services platform, and offers modern technology and exponential scalability.</span></span>

<span data-ttu-id="08719-108">Skattútreikningur er samþættur við Dynamics 365 Finance og Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="08719-108">Tax Calculation integrates with Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="08719-109">Að lokum verður hún einnig samþætt við Dynamics 365 Project Operations, Dynamics 365 Commerce og önnur forrit frá fyrstu og þriðju aðilum.</span><span class="sxs-lookup"><span data-stu-id="08719-109">Eventually, it will also integrate with Dynamics 365 Project Operations, Dynamics 365 Commerce, and other first-party and third-party applications.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="08719-110">Þegar skattaútreikningsþjónustan er virkjuð gætu sumar aðgerðir á tengdum gögnum verið framkvæmdar í gagnamiðstöð annarri en gagnamiðstöðinni sem heldur utan um þjónustugögnin.</span><span class="sxs-lookup"><span data-stu-id="08719-110">When you enable the Tax Calculation service, some operations on related data might be performed in a data center other than the data center that maintains your service data.</span></span> <span data-ttu-id="08719-111">Yfirfarið [Skilmálana](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md) áður en skattaútreikningsþjónustan er virkjuð.</span><span class="sxs-lookup"><span data-stu-id="08719-111">Review the [Terms and Conditions](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md) before you enable the Tax Calculation service.</span></span> <span data-ttu-id="08719-112">Persónuvernd þín er okkur mikilvæg.</span><span class="sxs-lookup"><span data-stu-id="08719-112">Your privacy is important to us.</span></span> <span data-ttu-id="08719-113">Frekari upplýsingar má finna í [tilkynningu okkar um persónuvernd](https://go.microsoft.com/fwlink/?LinkId=521839).</span><span class="sxs-lookup"><span data-stu-id="08719-113">To learn more, read our [Privacy Statement](https://go.microsoft.com/fwlink/?LinkId=521839).</span></span>

<span data-ttu-id="08719-114">Skattaútreikningur er skattakerfi frá Microsoft sem býður upp á mikinn sveigjanleika.</span><span class="sxs-lookup"><span data-stu-id="08719-114">Tax Calculation is a microservice-based tax engine that offers exponential scalability.</span></span> <span data-ttu-id="08719-115">Það getur hjálpað þér að framkvæma eftirfarandi verk:</span><span class="sxs-lookup"><span data-stu-id="08719-115">It can help you perform the following tasks:</span></span>

- <span data-ttu-id="08719-116">Grunnstilla skattaútreikning með Regulatory Configuration Service (RCS).</span><span class="sxs-lookup"><span data-stu-id="08719-116">Configure Tax Calculation through Regulatory Configuration Service (RCS).</span></span> <span data-ttu-id="08719-117">RCS er endurbætt útgáfa af hönnuði rafrænnar útgáfu og er fáanleg sem sjálfstæð þjónusta.</span><span class="sxs-lookup"><span data-stu-id="08719-117">RCS is an enhanced version of the Electronic reporting (ER) designer and is available as a standalone service.</span></span>
- <span data-ttu-id="08719-118">Grunnstilla skattafylki til að ákvarða sjálfkrafa skattkóða og taxta.</span><span class="sxs-lookup"><span data-stu-id="08719-118">Configure the tax matrix to automatically determine tax codes and rates.</span></span>
- <span data-ttu-id="08719-119">Grunnstilla skattafylki til að ákvarða sjálfkrafa skattskráningarnúmerið.</span><span class="sxs-lookup"><span data-stu-id="08719-119">Configure the tax matrix to automatically determine the tax registration number.</span></span>
- <span data-ttu-id="08719-120">Grunnstilla hönnuð skattaútreiknings til að skilgreina formúlur og skilyrði.</span><span class="sxs-lookup"><span data-stu-id="08719-120">Configure the tax calculation designer to define formulas and conditions.</span></span>
- <span data-ttu-id="08719-121">Deildu skattákvörðun og útreikningslausn á milli lögaðila.</span><span class="sxs-lookup"><span data-stu-id="08719-121">Share the tax determination and calculation solution across legal entities.</span></span>

<span data-ttu-id="08719-122">Til að nota skattaútreikningsþjónustu skal setja upp innbótina fyrir skattaútreikningsþjónustu ur verkefninu í Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="08719-122">To use the tax calculation service, install the tax calculation service add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="08719-123">Ljúkið síðan uppsetningunni í RCS og virkið skattútreikningaþjónustuna í Finance and Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="08719-123">Then complete the setup in RCS, and enable the tax calculation service in Finance and Supply Chain Management.</span></span> <span data-ttu-id="08719-124">Frekari upplýsingar eru í [Hafist handa með skattþjónustu](./global-get-started-with-tax-calculation-service.md).</span><span class="sxs-lookup"><span data-stu-id="08719-124">For more information, see [Get started with tax service](./global-get-started-with-tax-calculation-service.md).</span></span>

## <a name="availability"></a><span data-ttu-id="08719-125">Til ráðstöfunar</span><span class="sxs-lookup"><span data-stu-id="08719-125">Availability</span></span>

<span data-ttu-id="08719-126">Skattaútreikningur er aðeins í boði í sandkassaumhverfi og til valinna viðskiptavina í gegnum almenna forútgáfu.</span><span class="sxs-lookup"><span data-stu-id="08719-126">Tax Calculation is available only in sandbox environments and to selected customers, through a public preview program.</span></span> <span data-ttu-id="08719-127">Að lokum mun hún verða aðgengileg öllum viðskiptavinum og í framleiðsluferli.</span><span class="sxs-lookup"><span data-stu-id="08719-127">Eventually, it will become generally available to all customers and in production environments.</span></span>

<span data-ttu-id="08719-128">Nýjir eiginleikar verða áfram kynntir til sögunnar og þess vegna þarf að gæta þess að skoða nýjustu fylgiskjöl til að fá upplýsingar um umfang studdra eiginleika.</span><span class="sxs-lookup"><span data-stu-id="08719-128">New features will continue to be delivered, so be sure to check the most up-to-date documentation often to learn about the coverage and scope of supported features.</span></span>

<span data-ttu-id="08719-129">Skattaútreikningur er í boði á eftirfarandi staðsetningum Azure.</span><span class="sxs-lookup"><span data-stu-id="08719-129">Tax Calculation is deployed in the following Azure geographies.</span></span> <span data-ttu-id="08719-130">Hún verður einnig í boði á fleiri Azure-landsvæðum í samræmi við þarfir viðskiptavina:</span><span class="sxs-lookup"><span data-stu-id="08719-130">It will also be deployed to more Azure geographies, based on customer needs:</span></span>

- <span data-ttu-id="08719-131">Bandaríkin</span><span class="sxs-lookup"><span data-stu-id="08719-131">United States</span></span>
- <span data-ttu-id="08719-132">Evrópa</span><span class="sxs-lookup"><span data-stu-id="08719-132">Europe</span></span>

> [!NOTE]
> <span data-ttu-id="08719-133">Skattaútreikningur styður ekki uppsetningu Dynamics 365 á staðnum.</span><span class="sxs-lookup"><span data-stu-id="08719-133">Tax Calculation doesn't support on-premises deployments of Dynamics 365.</span></span> <span data-ttu-id="08719-134">Hún styður einnig ekki fyrri útgáfur, eins og Dynamics AX 2012.</span><span class="sxs-lookup"><span data-stu-id="08719-134">It also doesn't support earlier versions, such as Dynamics AX 2012.</span></span>

## <a name="feature-highlights"></a><span data-ttu-id="08719-135">Helstu atriði eiginleika</span><span class="sxs-lookup"><span data-stu-id="08719-135">Feature highlights</span></span>

- <span data-ttu-id="08719-136">Stillanlegt skattafylki til að ákvarða og reikna út skatt sjálfkrafa</span><span class="sxs-lookup"><span data-stu-id="08719-136">A configurable tax matrix to automatically determine and calculate tax</span></span>
- <span data-ttu-id="08719-137">Stuðningur fyrir mörg skattskráningarnúmer</span><span class="sxs-lookup"><span data-stu-id="08719-137">Support for multiple tax registration numbers</span></span>
- <span data-ttu-id="08719-138">Stuðningur flutningspöntunar fyrir skattákvörðun og útreikning</span><span class="sxs-lookup"><span data-stu-id="08719-138">Transfer order support for tax determination and calculation</span></span>
- <span data-ttu-id="08719-139">Stuðningur flutningspöntunar fyrir ákvörðun margra skattnúmera</span><span class="sxs-lookup"><span data-stu-id="08719-139">Transfer order support for determination of multiple tax registration numbers</span></span>

## <a name="supported-transactions"></a><span data-ttu-id="08719-140">Studdar færslur</span><span class="sxs-lookup"><span data-stu-id="08719-140">Supported transactions</span></span>

<span data-ttu-id="08719-141">Lögaðili og færsluhirðir geta gert skattaútreikning virkan.</span><span class="sxs-lookup"><span data-stu-id="08719-141">Tax Calculation can be enabled by legal entity and transaction.</span></span> <span data-ttu-id="08719-142">Eftirfarandi færslur eru studdar:</span><span class="sxs-lookup"><span data-stu-id="08719-142">The following transactions are supported:</span></span>

- <span data-ttu-id="08719-143">Söluferli</span><span class="sxs-lookup"><span data-stu-id="08719-143">Sales process</span></span>

    - <span data-ttu-id="08719-144">Sölutilboð</span><span class="sxs-lookup"><span data-stu-id="08719-144">Sales quotation</span></span>
    - <span data-ttu-id="08719-145">Sölupöntun</span><span class="sxs-lookup"><span data-stu-id="08719-145">Sales order</span></span>
    - <span data-ttu-id="08719-146">Staðfesting</span><span class="sxs-lookup"><span data-stu-id="08719-146">Confirmation</span></span>
    - <span data-ttu-id="08719-147">Tiltektarlisti</span><span class="sxs-lookup"><span data-stu-id="08719-147">Picking list</span></span>
    - <span data-ttu-id="08719-148">Fylgiseðill</span><span class="sxs-lookup"><span data-stu-id="08719-148">Packing slip</span></span>
    - <span data-ttu-id="08719-149">Sölureikningur</span><span class="sxs-lookup"><span data-stu-id="08719-149">Sales invoice</span></span>
    - <span data-ttu-id="08719-150">Kreditnóta</span><span class="sxs-lookup"><span data-stu-id="08719-150">Credit note</span></span>
    - <span data-ttu-id="08719-151">Skila pöntun</span><span class="sxs-lookup"><span data-stu-id="08719-151">Return order</span></span>
    - <span data-ttu-id="08719-152">Ýmis hausgjöld</span><span class="sxs-lookup"><span data-stu-id="08719-152">Header miscellaneous charge</span></span>
    - <span data-ttu-id="08719-153">Ýmis línugjöld</span><span class="sxs-lookup"><span data-stu-id="08719-153">Line miscellaneous charge</span></span>

- <span data-ttu-id="08719-154">Innkaupaferli</span><span class="sxs-lookup"><span data-stu-id="08719-154">Purchase process</span></span>

    - <span data-ttu-id="08719-155">Innkaupapöntun</span><span class="sxs-lookup"><span data-stu-id="08719-155">Purchase order</span></span>
    - <span data-ttu-id="08719-156">Staðfesting</span><span class="sxs-lookup"><span data-stu-id="08719-156">Confirmation</span></span>
    - <span data-ttu-id="08719-157">Komulisti</span><span class="sxs-lookup"><span data-stu-id="08719-157">Receipts list</span></span>
    - <span data-ttu-id="08719-158">Innhreyfingarskjal afurða</span><span class="sxs-lookup"><span data-stu-id="08719-158">Product receipt</span></span>
    - <span data-ttu-id="08719-159">Innkaupareikningur</span><span class="sxs-lookup"><span data-stu-id="08719-159">Purchase invoice</span></span>
    - <span data-ttu-id="08719-160">Ýmis hausgjöld</span><span class="sxs-lookup"><span data-stu-id="08719-160">Header miscellaneous charge</span></span>
    - <span data-ttu-id="08719-161">Ýmis línugjöld</span><span class="sxs-lookup"><span data-stu-id="08719-161">Line miscellaneous charge</span></span>
    - <span data-ttu-id="08719-162">Kreditnóta</span><span class="sxs-lookup"><span data-stu-id="08719-162">Credit note</span></span>
    - <span data-ttu-id="08719-163">Skila pöntun</span><span class="sxs-lookup"><span data-stu-id="08719-163">Return order</span></span>
    - <span data-ttu-id="08719-164">Innkaupabeiðni</span><span class="sxs-lookup"><span data-stu-id="08719-164">Purchase requisition</span></span>
    - <span data-ttu-id="08719-165">Ýmis gjöld innkaupabeiðnilínu</span><span class="sxs-lookup"><span data-stu-id="08719-165">Purchase requisition line miscellaneous charge</span></span>
    - <span data-ttu-id="08719-166">Beiðni um tilboð</span><span class="sxs-lookup"><span data-stu-id="08719-166">Request for quotation</span></span>
    - <span data-ttu-id="08719-167">Ýmis hausgjöld fyrir beiðni um tilboð</span><span class="sxs-lookup"><span data-stu-id="08719-167">Request for quotation header miscellaneous charge</span></span>
    - <span data-ttu-id="08719-168">Ýmis línugjöld fyrir beiðni um tilboð</span><span class="sxs-lookup"><span data-stu-id="08719-168">Request for quotation line miscellaneous charge</span></span>

- <span data-ttu-id="08719-169">Birgðavinnsla</span><span class="sxs-lookup"><span data-stu-id="08719-169">Inventory process</span></span>

    - <span data-ttu-id="08719-170">Flutningspantanir - senda</span><span class="sxs-lookup"><span data-stu-id="08719-170">Transfer order – ship</span></span>
    - <span data-ttu-id="08719-171">Móttaka flutningspöntunar</span><span class="sxs-lookup"><span data-stu-id="08719-171">Transfer order – receive</span></span>

## <a name="related-resources"></a><span data-ttu-id="08719-172">Tengd tilföng</span><span class="sxs-lookup"><span data-stu-id="08719-172">Related resources</span></span>

[<span data-ttu-id="08719-173">Hafist handa með skattþjónustu</span><span class="sxs-lookup"><span data-stu-id="08719-173">Get started with tax service</span></span>](./global-get-started-with-tax-calculation-service.md)

[<span data-ttu-id="08719-174">Mörg VSK-skráningarnúmer</span><span class="sxs-lookup"><span data-stu-id="08719-174">Multiple VAT registration number</span></span>](./emea-multiple-vat-registration-numbers.md)

[<span data-ttu-id="08719-175">Stuðningur skattaeiginleika fyrir flutningspöntun</span><span class="sxs-lookup"><span data-stu-id="08719-175">Tax feature support for transfer order</span></span>](./tasks/tax-feature-support-for-transfer-order.md)

[<span data-ttu-id="08719-176">Hvernig á að byggja upp viðbót í skattsþjónustu</span><span class="sxs-lookup"><span data-stu-id="08719-176">How to build extension in tax service</span></span>](./tax-service-add-data-fields-tax-integration-by-extension.md)
