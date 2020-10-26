---
title: Veita starfsfólki í framleiðslu leiðarvísa með blönduðum veruleika
description: Þetta efnisatriði útskýrir hvernig á að samþætta framleiðslustýringareininguna í Microsoft Dynamics 365 Supply Chain Management við Dynamics 365 Guides.
author: cabeln
manager: tfehr
ms.date: 09/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkGuidesManufacturing
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 61943
ms.assetid: a3847f07-fca4-4140-a26f-d83c6ac68dde
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: cabeln
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.15
ms.openlocfilehash: d8c2da17d4e3df37c55844f0aad00f883725f741
ms.sourcegitcommit: c55fecae96b4bb27bc313ba10a97eddb9c91350a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/12/2020
ms.locfileid: "3989278"
---
# <a name="provide-mixed-reality-guides-for-workers-in-production"></a><span data-ttu-id="269fa-103">Veita starfsfólki í framleiðslu leiðarvísa með blönduðum veruleika</span><span class="sxs-lookup"><span data-stu-id="269fa-103">Provide mixed-reality Guides for workers in production</span></span>

<span data-ttu-id="269fa-104">Starfsmenn í framleiðsluferli munu hagnast á viðeigandi leiðbeiningum sem eru veittar á réttum tíma í samhengi við verk þeirra.</span><span class="sxs-lookup"><span data-stu-id="269fa-104">Workers in production processes will benefit from relevant instructions that are provided at the right time in the context of their work.</span></span> <span data-ttu-id="269fa-105">*Leiðbeiningar* eiga við í nokkrum þáttum vinnunnar, þar á meðal: samsetningu, þjónustu, aðgerðum, vottunum og öryggi.</span><span class="sxs-lookup"><span data-stu-id="269fa-105">*Instructions* apply in several domains of work, including: assembly, service, operations, certification, and safety.</span></span> <span data-ttu-id="269fa-106">Í öllum þessum meginaðgerðum rekstursins geta virkar leiðbeiningar hjálpað starfsmönnum að ná meiri árangri og skila betri vinnu.</span><span class="sxs-lookup"><span data-stu-id="269fa-106">Across all of these core business functions, ongoing training instructions can help empower workers to achieve more and work better.</span></span>

## <a name="introduction"></a><span data-ttu-id="269fa-107">Inngangur</span><span class="sxs-lookup"><span data-stu-id="269fa-107">Introduction</span></span>

<span data-ttu-id="269fa-108">Hægt er að veita leiðbeiningar á mismunandi hátt.</span><span class="sxs-lookup"><span data-stu-id="269fa-108">You can provide instructions in different ways.</span></span> <span data-ttu-id="269fa-109">Eitt skilvirkt sendingarkerfi notar [Dynamics 365 Guides](https://dynamics.microsoft.com/mixed-reality/guides/).</span><span class="sxs-lookup"><span data-stu-id="269fa-109">One efficient system that ships out of the box uses [Dynamics 365 Guides](https://dynamics.microsoft.com/mixed-reality/guides/).</span></span>

<span data-ttu-id="269fa-110">Dynamics 365 Guides getur hjálpað starfsfólki með verklegri kennslu.</span><span class="sxs-lookup"><span data-stu-id="269fa-110">Dynamics 365 Guides can help empower your employees with hands-on learning.</span></span> <span data-ttu-id="269fa-111">Hægt er að skilgreina stöðluð ferli með ítarlegum leiðbeiningum sem leiðbeina starfsmönnum um verkfæri og hluta sem þeir þurfa á að halda og sýna starfsmönnum hvernig á að nota þessi verkfæri í raunverulegum aðstæðum í vinnunni.</span><span class="sxs-lookup"><span data-stu-id="269fa-111">You can define standardized processes with step-by-step instructions that guide your employees to the tools and parts they need and show employees how to use these tools in real work situations.</span></span>

<span data-ttu-id="269fa-112">Hægt er að hengja leiðarvísa við ýmsa þætti framleiðslustýringar, þar á meðal:</span><span class="sxs-lookup"><span data-stu-id="269fa-112">You can attach guides to various aspects of production control including:</span></span>

- [<span data-ttu-id="269fa-113">Forði</span><span class="sxs-lookup"><span data-stu-id="269fa-113">Resources</span></span>](#resources)
- [<span data-ttu-id="269fa-114">Tilfangaflokkar</span><span class="sxs-lookup"><span data-stu-id="269fa-114">Resource groups</span></span>](#resource-groups)
- [<span data-ttu-id="269fa-115">Útgefnar afurðir</span><span class="sxs-lookup"><span data-stu-id="269fa-115">Released products</span></span>](#released-products)
- [<span data-ttu-id="269fa-116">Formúlur</span><span class="sxs-lookup"><span data-stu-id="269fa-116">Formulas</span></span>](#formulas)
- [<span data-ttu-id="269fa-117">Formúluútgáfur</span><span class="sxs-lookup"><span data-stu-id="269fa-117">Formula versions</span></span>](#formula-versions)
- [<span data-ttu-id="269fa-118">Uppskriftir</span><span class="sxs-lookup"><span data-stu-id="269fa-118">Bills of material (BOMs)</span></span>](#bom)
- [<span data-ttu-id="269fa-119">Uppskriftaútgáfur</span><span class="sxs-lookup"><span data-stu-id="269fa-119">BOM versions</span></span>](#bom-versions)
- [<span data-ttu-id="269fa-120">Leiðir</span><span class="sxs-lookup"><span data-stu-id="269fa-120">Routes</span></span>](#routes)
- [<span data-ttu-id="269fa-121">Leiðarútgáfur</span><span class="sxs-lookup"><span data-stu-id="269fa-121">Route versions</span></span>](#route-versions)
- [<span data-ttu-id="269fa-122">Tengsl leiðaraðgerðar</span><span class="sxs-lookup"><span data-stu-id="269fa-122">Route operation relations</span></span>](#route-operation-relations)

> [!NOTE]
> <span data-ttu-id="269fa-123">Einnig er hægt að hengja leiðsagnir við Eignastýringu.</span><span class="sxs-lookup"><span data-stu-id="269fa-123">You can also attach Guides with Asset Management.</span></span> <span data-ttu-id="269fa-124">Sjá frekari upplýsingar í [Samþætta Dynamics 365 Supply Chain Management (Eignastýring) við Dynamics 365 Guides](../asset-management/asset-management-guides-integration.md).</span><span class="sxs-lookup"><span data-stu-id="269fa-124">For more information about that option, see [Integrate Dynamics 365 Supply Chain Management (Asset Management) with Dynamics 365 Guides](../asset-management/asset-management-guides-integration.md).</span></span>

<span data-ttu-id="269fa-125">Þegar fyrsti starfsmaður í ferlinu velur verk í vinnusal í gegnum Supply Chain Management, getur starfsmaðurinn séð [viðkomandi leiðarvísa](#logic) á verkspjaldinu.</span><span class="sxs-lookup"><span data-stu-id="269fa-125">When a first-line worker chooses a job on the shop floor through Supply Chain Management, the worker can see [the relevant guides](#logic) on the job card.</span></span> <span data-ttu-id="269fa-126">Þegar starfsmaðurinn velur tiltekna leiðsögn, birtist QR-kóði fyrir þann leiðarvísi á skjánum.</span><span class="sxs-lookup"><span data-stu-id="269fa-126">When the worker chooses a specific guide, a QR code for that guide is shown on the screen.</span></span> <span data-ttu-id="269fa-127">Starfsmaðurinn notar síðan HoloLens til að skanna QR-kóðann sem ræsir leiðsagnir og sýnir nauðsynlegar leiðbeiningar.</span><span class="sxs-lookup"><span data-stu-id="269fa-127">The worker then uses their HoloLens to scan the QR code, which launches Guides and shows the required instructions.</span></span>

<span data-ttu-id="269fa-128">Eftirfarandi undirkaflar lýsa nokkrum völdum aðstæðum þar sem fyrirtæki í ýmsum atvinnugreinum sjá mestan hag í því að nota leiðarvísa til að kynna leiðbeiningar fyrir framleiðslu.</span><span class="sxs-lookup"><span data-stu-id="269fa-128">The following subsections describe a few selected scenarios where companies across industries can see the biggest value when using Guides to present instructions for manufacturing.</span></span>

### <a name="assembly"></a><span data-ttu-id="269fa-129">Smölun</span><span class="sxs-lookup"><span data-stu-id="269fa-129">Assembly</span></span>

<span data-ttu-id="269fa-130">![Nota leiðbeiningar í samsetningarverkum](media/instruction-guides-hero-assembly.png "Nota leiðarvísa í þjónustuverkum")</span><span class="sxs-lookup"><span data-stu-id="269fa-130">![Use Guides in assembly tasks](media/instruction-guides-hero-assembly.png "Use Guides in service tasks")</span></span>

<span data-ttu-id="269fa-131">Leiðbeiningar í samsetningaraðgerðum sýna starfsmönnum þau verkfæri og hluta sem þeir þurfa á að halda og hvernig á að nota það í raunverulegum aðstæðum við vinnu.</span><span class="sxs-lookup"><span data-stu-id="269fa-131">Instructions in assembly operations show workers the tools and parts they need and how to use them in real work situations.</span></span>

<span data-ttu-id="269fa-132">Framleiðslustjórar geta búið til og úthlutað leiðsögn, til dæmis fyrir [framleiðsluleiðir](routes-operations.md), [aðgerðarvensl](routes-operations.md#operation-relations)eða [uppskrift](bill-of-material-bom.md).</span><span class="sxs-lookup"><span data-stu-id="269fa-132">Production managers can create and assign Guides, for example, for [production routes](routes-operations.md), [operation relations](routes-operations.md#operation-relations), or [bills of material](bill-of-material-bom.md).</span></span> <span data-ttu-id="269fa-133">Starfsmenn munu finna viðeigandi leiðbeiningar um viðkomandi vinnsluupplifun í vinnusalnum.</span><span class="sxs-lookup"><span data-stu-id="269fa-133">Workers will find the relevant instructions on the respective operation experience on the shop floor.</span></span>

### <a name="service"></a><span data-ttu-id="269fa-134">Þjónusta</span><span class="sxs-lookup"><span data-stu-id="269fa-134">Service</span></span>

<span data-ttu-id="269fa-135">![Nota leiðarvísa í þjónustuverkum](media/instruction-guides-hero-service.png "Nota leiðarvísa í þjónustuverkum")</span><span class="sxs-lookup"><span data-stu-id="269fa-135">![Use Guides in service tasks](media/instruction-guides-hero-service.png "Use Guides in service tasks")</span></span>

<span data-ttu-id="269fa-136">Bjóða tæknimönnum upp á leiðsagnir á vinnusvæðinu og koma þannig í veg fyrir þörfina á því að tímasetja frekari heimsóknir.</span><span class="sxs-lookup"><span data-stu-id="269fa-136">Equip technicians with guided instructions at the job site, eliminating the need to schedule additional visits.</span></span>

<span data-ttu-id="269fa-137">Þjónustustjórar geta úthlutað leiðbeiningum, t.d. á tilteknar [afurðir](../../commerce/product.md) sem fara í gegnum vanabundið gæðamat.</span><span class="sxs-lookup"><span data-stu-id="269fa-137">Service managers can assign Guides, for example, to specific [products](../../commerce/product.md) that walk through routines of quality assessment.</span></span>

### <a name="quality"></a><span data-ttu-id="269fa-138">Gæði</span><span class="sxs-lookup"><span data-stu-id="269fa-138">Quality</span></span>

<span data-ttu-id="269fa-139">![Nota leiðarvísa í vinnu gæðaeftirlits](media/instruction-guides-hero-quality.png "Nota leiðarvísa í vinnu gæðaeftirlits")</span><span class="sxs-lookup"><span data-stu-id="269fa-139">![Use Guides in quality assurance tasks](media/instruction-guides-hero-quality.png "Use Guides in quality assurance tasks")</span></span>

<span data-ttu-id="269fa-140">Komið með nýja ferla og tryggið aukið samræmi með því að breyta þekkingu starfsmanna í endurtekið verkfæri.</span><span class="sxs-lookup"><span data-stu-id="269fa-140">Rollout new processes and ensure increased consistency by turning employee knowledge into a repeatable tool.</span></span>

<span data-ttu-id="269fa-141">Gæðastjórar geta úthlutað leiðbeiningum, t.d. á [afurðir](../../commerce/product.md) sem fara í gegnum vanabundið gæðamat.</span><span class="sxs-lookup"><span data-stu-id="269fa-141">Quality assurance managers can assign guides, for example, to [products](../../commerce/product.md) that walk through routines of quality assessment.</span></span>

### <a name="certifications"></a><span data-ttu-id="269fa-142">Vottanir</span><span class="sxs-lookup"><span data-stu-id="269fa-142">Certifications</span></span>

<span data-ttu-id="269fa-143">![Nota leiðbeiningar fyrir verk sem tengjast vottun](media/instruction-guides-hero-certification.png "Nota leiðbeiningar fyrir verk sem tengjast vottun")</span><span class="sxs-lookup"><span data-stu-id="269fa-143">![Use Guides for certification related tasks](media/instruction-guides-hero-certification.png "Use Guides for certification related tasks")</span></span>

<span data-ttu-id="269fa-144">Gangið úr skugga um að sérhver starfsmaður uppfylli strangar kröfur með því að finna út hver þarf hjálp og hvar.</span><span class="sxs-lookup"><span data-stu-id="269fa-144">Ensure every employee meets high standards by quickly identifying who needs help and where.</span></span>

### <a name="safety"></a><span data-ttu-id="269fa-145">Öryggi</span><span class="sxs-lookup"><span data-stu-id="269fa-145">Safety</span></span>

<span data-ttu-id="269fa-146">![Nota leiðarvísa í öryggisleiðbeiningum](media/instruction-guides-hero-safety.png "Nota leiðarvísa í öryggisleiðbeiningum")</span><span class="sxs-lookup"><span data-stu-id="269fa-146">![Use Guides in work safety instructions](media/instruction-guides-hero-safety.png "Use Guides in work safety instructions")</span></span>

<span data-ttu-id="269fa-147">Gefið fyrirmæli sem fara í gegnum hættuleg ferli í sýnidæmi áður en það er reynt við raunverulegar aðstæður.</span><span class="sxs-lookup"><span data-stu-id="269fa-147">Provide instructions that walk through dangerous procedures virtually before attempting in the physical environment.</span></span> <span data-ttu-id="269fa-148">Með blönduðum veruleika geta starfsmenn öðlast reynslu af hættulegum ferlum í sýnidæmi.</span><span class="sxs-lookup"><span data-stu-id="269fa-148">With a mixed reality approach, workers can experience dangerous procedures virtually.</span></span>

<span data-ttu-id="269fa-149">Framleiðslustjórar geta veitt nákvæmar leiðbeiningar um meðhöndlun á hættulegum efnum eða ferla viðkvæmrar meðhöndlunar með því að úthluta leiðbeiningum á [vörur](../../commerce/product.md), [leiðir](routes-operations.md) og [aðgerðir](routes-operations.md#operation-relations).</span><span class="sxs-lookup"><span data-stu-id="269fa-149">Production managers can provide dedicated handling instructions for hazardous material handling or delicate handling procedures by assigning instructions to [product items](../../commerce/product.md), [routes](routes-operations.md), and [operations](routes-operations.md#operation-relations).</span></span>

## <a name="get-started-with-instructions-and-guides"></a><span data-ttu-id="269fa-150">Hafist handa með leiðbeiningar og leiðsögnum</span><span class="sxs-lookup"><span data-stu-id="269fa-150">Get started with instructions and Guides</span></span>

<span data-ttu-id="269fa-151">Til að virkja leiðbeiningar í framleiðsluferlum býður Supply Chain Management upp á tilbúna samþættingu við Dynamics 365 Guides.</span><span class="sxs-lookup"><span data-stu-id="269fa-151">To enable instructions in production processes, Supply Chain Management provides an out-of-the-box integration with Dynamics 365 Guides.</span></span> <span data-ttu-id="269fa-152">Heimilað og uppsett forritstilvik Guides er nauðsynlegt til að búa til, vinna með og úthluta leiðbeiningum blandaðs veruleika á framleiðslueignir og framleiðsluvinnu.</span><span class="sxs-lookup"><span data-stu-id="269fa-152">A licensed and installed application instance of Guides is required to build, maintain, and assign mixed reality instructions to production assets and work.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="269fa-153">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="269fa-153">Prerequisites</span></span>

<span data-ttu-id="269fa-154">Til að nota þennan eiginleika verður kerfið að innihalda eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="269fa-154">To use this feature, your system must include the following:</span></span>

- <span data-ttu-id="269fa-155">Dynamics 365 Supply Chain Management útgáfa 10.0.15 eða nýrri</span><span class="sxs-lookup"><span data-stu-id="269fa-155">Dynamics 365 Supply Chain Management version 10.0.15 or later</span></span>
- <span data-ttu-id="269fa-156">[Tvöföld skrif](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write) fyrir forrit Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="269fa-156">[Dual-write](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write) for Supply Chain Management apps.</span></span>
- <span data-ttu-id="269fa-157">[Dynamics 365 Guides](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) útgáfa 400.0.1.48 eða nýrri</span><span class="sxs-lookup"><span data-stu-id="269fa-157">[Dynamics 365 Guides](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) version 400.0.1.48 or later</span></span>

### <a name="turn-on-the-feature"></a><span data-ttu-id="269fa-158">Kveikja á eiginleikanum</span><span class="sxs-lookup"><span data-stu-id="269fa-158">Turn on the feature</span></span>

<span data-ttu-id="269fa-159">Til að bjóða upp á eiginleikann í kerfinu, þarf að virkja skilgreiningarlyklana.</span><span class="sxs-lookup"><span data-stu-id="269fa-159">To make the feature available on your system, you must enable its configuration keys.</span></span> <span data-ttu-id="269fa-160">Þetta þarf aðeins að gera einu sinni.</span><span class="sxs-lookup"><span data-stu-id="269fa-160">You only need to do this once.</span></span> <span data-ttu-id="269fa-161">Til að gera þetta verður stjórnandi að gera eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="269fa-161">To do this, an administrator must do the following:</span></span>

1. <span data-ttu-id="269fa-162">Setjið kerfið í viðhaldsstillingu eins og lýst er í [Viðhaldsstilling](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span><span class="sxs-lookup"><span data-stu-id="269fa-162">Place your system into maintenance mode as described in [Maintenance mode](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>
1. <span data-ttu-id="269fa-163">Opnið **Kerfisstjórnun \> Setja upp \> Skilgreining leyfis**.</span><span class="sxs-lookup"><span data-stu-id="269fa-163">Go to **System administration \> Setup \> License configuration**.</span></span>
1. <span data-ttu-id="269fa-164">Stækkið hlutann **Blandaður veruleiki** og veljið svo gátreitinn **Leiðarvísir fyrir blandaðan veruleika**.</span><span class="sxs-lookup"><span data-stu-id="269fa-164">Expand the **Mixed reality** section and then select the **Mixed reality guide** check box.</span></span>
1. <span data-ttu-id="269fa-165">Stækkið hlutann **Framleiðslustýring** og veljið svo gátreitinn **Leiðbeiningar fyrir framleiðslu**.</span><span class="sxs-lookup"><span data-stu-id="269fa-165">Expand the **Production management** section and then select the **Production instructions** check box.</span></span>
1. <span data-ttu-id="269fa-166">Slökkvið á viðhaldsstillingu eins og lýst er í [Viðhaldsstilling](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span><span class="sxs-lookup"><span data-stu-id="269fa-166">Turn off maintenance mode as described in [Maintenance mode](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>
  
## <a name="configure-how-guides-appear-on-the-shop-floor"></a><span data-ttu-id="269fa-167">Skilgreina hvernig leiðsagnir birtast í vinnusal</span><span class="sxs-lookup"><span data-stu-id="269fa-167">Configure how Guides appear on the shop floor</span></span>

<span data-ttu-id="269fa-168">Til skilgreina hvernig leiðsagnir birtast í vinnusal skal fara í **Blandaður veruleiki \> Dynamics 365 Guides \> Skilgreina samþættingu leiðsagna**.</span><span class="sxs-lookup"><span data-stu-id="269fa-168">To configure how Guides appear on the shop floor, go to **Mixed Reality \> Dynamics 365 Guides \> Configure Guides integration**.</span></span>

<span data-ttu-id="269fa-169">![Skilgreina samþættingu leiðsagna fyrir framleiðslu](media/instruction-guides-configure-integration.png "Skilgreina samþættingu leiðsagna fyrir framleiðslu")</span><span class="sxs-lookup"><span data-stu-id="269fa-169">![Configure Guide integration for manufacturing](media/instruction-guides-configure-integration.png "Configure Guide integration for manufacturing")</span></span>

<span data-ttu-id="269fa-170">Stilltu eftirfarandi reiti:</span><span class="sxs-lookup"><span data-stu-id="269fa-170">Set the following fields:</span></span>

- <span data-ttu-id="269fa-171">**Undirlén CDS-umhverfis** - Þessi reitur á þegar að sýna gildi.</span><span class="sxs-lookup"><span data-stu-id="269fa-171">**CDS environment subdomain** - This field should already show a value.</span></span> <span data-ttu-id="269fa-172">Þessi reitur inniheldur undirlén fyrir Common Data Service-umhverfið þar sem leiðsagnir eru búnar til.</span><span class="sxs-lookup"><span data-stu-id="269fa-172">This field holds the subdomain for the Common Data Service environment where you create your Guides.</span></span> <span data-ttu-id="269fa-173">Undirlénið er fyrsti hluti vefslóðarinnar og fær yfirleitt heiti fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="269fa-173">The subdomain is the first part of the URL and is typically named after your organization.</span></span> <span data-ttu-id="269fa-174">Til dæmis ef Common Data Service vefslóðin er „contoso.crm4.dynamics.com“, ætti að færa inn *contoso* hér.</span><span class="sxs-lookup"><span data-stu-id="269fa-174">For example, if your Common Data Service URL is "contoso.crm4.dynamics.com", you should enter *contoso* here.</span></span> <span data-ttu-id="269fa-175">Þetta gildi er notað til að setja saman slóð fyrir leiðsagnirnar og verður kóðað inn í QR-kóðana.</span><span class="sxs-lookup"><span data-stu-id="269fa-175">This value is used to compose addresses for your guides and will be encoded into the QR codes.</span></span>
- <span data-ttu-id="269fa-176">**Stærð QR-kóða** - Stillið myndastærð QR-kóðans.</span><span class="sxs-lookup"><span data-stu-id="269fa-176">**QR code size** - Set the size of the rendered QR code.</span></span> <span data-ttu-id="269fa-177">Við mælum með því að velja stærð sem fyllir stærstan hluta skjásins, en ekki meira.</span><span class="sxs-lookup"><span data-stu-id="269fa-177">We recommend choosing a size that will fill most of your display screen, but not more.</span></span> <span data-ttu-id="269fa-178">Oftast er *15* gott gildi.</span><span class="sxs-lookup"><span data-stu-id="269fa-178">Typically, *15* is a good value.</span></span>
- <span data-ttu-id="269fa-179">**Stig villuleiðréttingar QR-kóða** - Stillið uppskiptingu QR-kóðans.</span><span class="sxs-lookup"><span data-stu-id="269fa-179">**QR code error correction level** - Set the granularity of the QR code.</span></span> <span data-ttu-id="269fa-180">Hærri uppskipting getur aukið áreiðanleika kóðans, en **Stærð QR-kóðans** verður að vera nógu stór til að styðja nákvæmnina sem valið leiðréttingarstig þarf.</span><span class="sxs-lookup"><span data-stu-id="269fa-180">Higher granularity can help increase the code's reliability, but your **QR code size** must be large enough to support the level of detail required by your selected correction level.</span></span>


> [!TIP]
> - <span data-ttu-id="269fa-181">QR-kóðastærðir sem eru of stórar fyrir skjáinn taka lengri tíma að myndast og síðan vera skalaðar niður til að passa inn á skjáinn.</span><span class="sxs-lookup"><span data-stu-id="269fa-181">QR codes sizes that are too large for your display will take a bit longer to render and then be scaled down to fit your display.</span></span> <span data-ttu-id="269fa-182">Þetta hefur engan ávinning í för með sér.</span><span class="sxs-lookup"><span data-stu-id="269fa-182">These do not provide a benefit.</span></span>
> - <span data-ttu-id="269fa-183">QR-kóðastærðir sem eru of litlar geta dregið úr getu HoloLens til að lesa kóðann rétt í sumum umhverfum.</span><span class="sxs-lookup"><span data-stu-id="269fa-183">QR code sizes that are too small may decrease the ability of HoloLens to read the code properly in some environments.</span></span>
> - <span data-ttu-id="269fa-184">Við mælum með því að prófa stillingarnar fyrir hvert tæki sem mun birta QR-kóða fyrir HoloLens notendur.</span><span class="sxs-lookup"><span data-stu-id="269fa-184">We recommend that you test the settings for each device that will display QR codes for HoloLens users.</span></span> <span data-ttu-id="269fa-185">Veljið stillingar sem bjóða upp á nógu góðan læsileika í umhverfi vinnusalar.</span><span class="sxs-lookup"><span data-stu-id="269fa-185">Choose settings that provide sufficient readability in your shop floor environment.</span></span>  

## <a name="get-an-overview-of-all-guide-assignments"></a><span data-ttu-id="269fa-186">Fá yfirlit yfir allar úthlutanir leiðsagna</span><span class="sxs-lookup"><span data-stu-id="269fa-186">Get an overview of all Guide assignments</span></span>

<span data-ttu-id="269fa-187">Notið síðuna **Allar leiðsagnir** til að sjá lista yfir allar tiltækar leiðsagnir í fyrirtækinu og allar úthlutanir á framleiðsluferli og tilföng.</span><span class="sxs-lookup"><span data-stu-id="269fa-187">Use the **All Guides** page to see the list of all available Guides in your organization and all assignments to your production processes and resources.</span></span> <span data-ttu-id="269fa-188">Til að opna hana skal fara í **Blandaður veruleiki \> Leiðsagnir \> Allar leiðsagnir**.</span><span class="sxs-lookup"><span data-stu-id="269fa-188">To open it, go to **Mixed reality \> Guides \> All Guides**.</span></span> <span data-ttu-id="269fa-189">Efst í listanum eru allar tiltækar leiðsagnir sýndar og hægt er að nota reitinn hér til að sía listann.</span><span class="sxs-lookup"><span data-stu-id="269fa-189">The list at the top shows all the available Guides and you can use the field here to filter the list.</span></span> <span data-ttu-id="269fa-190">Neðst í listanum eru allar úthlutaðar leiðsagnir sýndar og tækjastika er í boði til að stjórna þeim.</span><span class="sxs-lookup"><span data-stu-id="269fa-190">The list at the bottom shows all Guide assignments and provides a toolbar for managing them.</span></span>

<span data-ttu-id="269fa-191">![Stjórna leiðarvísum](media/instruction-guides-allguides.png "Stjórna leiðarvísum")</span><span class="sxs-lookup"><span data-stu-id="269fa-191">![Manage Guides](media/instruction-guides-allguides.png "Manage Guides")</span></span>

<span data-ttu-id="269fa-192">Eftirfarandi kaflar lýsa þeim tegundum hluta sem hægt er að úthluta leiðarvísa á.</span><span class="sxs-lookup"><span data-stu-id="269fa-192">The following sections describe the types of objects that you can assign Guides to.</span></span> <span data-ttu-id="269fa-193">Í hverjum úthlutuðum leiðarvísi eru leiðbeiningar sem eru sjálfkrafa hengdar við viðeigandi framleiðsluverk sem verða í boði í vinnusalnum.</span><span class="sxs-lookup"><span data-stu-id="269fa-193">Each assigned guide provides instructions that are automatically attached to the respective production jobs and will be available on the shop floor.</span></span>

## <a name="associate-a-guide-to-a-resource"></a><a name="resources"></a><span data-ttu-id="269fa-194">Tengja leiðarvísi við tilfang</span><span class="sxs-lookup"><span data-stu-id="269fa-194">Associate a Guide to a resource</span></span>

<span data-ttu-id="269fa-195">Bætið leiðarvísi við [tilfang](operations-resources.md) til að bjóða upp á leiðarvísinn í samhengi við viðeigandi framleiðsluverk.</span><span class="sxs-lookup"><span data-stu-id="269fa-195">Add a Guide to a [resource](operations-resources.md) to offer the Guide in the context of relevant production jobs.</span></span>

### <a name="typical-scenario-using-resources"></a><span data-ttu-id="269fa-196">Dæmigerðar aðstæður sem nota tilföng</span><span class="sxs-lookup"><span data-stu-id="269fa-196">Typical scenario using resources</span></span>

<span data-ttu-id="269fa-197">Til dæmis væri hægt að hengja leiðarvísi með almennu vélaröryggi eða leiðbeiningum um meðhöndlun við tilfang af vélargerðinni.</span><span class="sxs-lookup"><span data-stu-id="269fa-197">For example, you could attach a Guide with general machine security or handling instructions to a resource of type machine.</span></span> <span data-ttu-id="269fa-198">Síðan verður leiðarvísirinn tiltækur fyrir hvert verk sem er framkvæmt á vélinni.</span><span class="sxs-lookup"><span data-stu-id="269fa-198">Then, the Guide will be available on every job that is performed on the machine.</span></span>

### <a name="add-a-guide-to-a-resource"></a><span data-ttu-id="269fa-199">Bæta leiðarvísi við tilfang</span><span class="sxs-lookup"><span data-stu-id="269fa-199">Add a Guide to a resource</span></span>

<span data-ttu-id="269fa-200">Leiðarvísi bætt við tilfang:</span><span class="sxs-lookup"><span data-stu-id="269fa-200">To add a Guide to a resource:</span></span>

1. <span data-ttu-id="269fa-201">Opnið **Framleiðslustýring \> Uppsetning \> Tilföng \> Tilföng**.</span><span class="sxs-lookup"><span data-stu-id="269fa-201">Go to **Production control \> Setup \> Resources \> Resources**.</span></span>
1. <span data-ttu-id="269fa-202">Í listasvæðinu skal velja tilfang sem á að úthluta leiðarvísi á.</span><span class="sxs-lookup"><span data-stu-id="269fa-202">From the list pane, select the resource you want to assign a Guide to.</span></span>
1. <span data-ttu-id="269fa-203">Stækkið flýtiflipann **Tengdir leiðarvísar**.</span><span class="sxs-lookup"><span data-stu-id="269fa-203">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="269fa-204">Veljið **Bæta við** úr tækjastikunni **Tengdir leiðarvísar**.</span><span class="sxs-lookup"><span data-stu-id="269fa-204">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="269fa-205">Nýrri línu er bætt við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="269fa-205">A new line is added to the grid.</span></span>
1. <span data-ttu-id="269fa-206">Fyrir nýju línuna skal nota fellilistann í dálkinum **Heiti** til að velja leiðarvísinn sem á að úthluta.</span><span class="sxs-lookup"><span data-stu-id="269fa-206">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span> <span data-ttu-id="269fa-207">Ef til er mikill fjöldi leiðarvísa, er hægt að sía listann til að finna þann sem verið er að leita að.</span><span class="sxs-lookup"><span data-stu-id="269fa-207">If you have a large number of Guides, then you can filter the list to find the one you are looking for.</span></span>
    <span data-ttu-id="269fa-208">![Stjórna leiðarvísum](media/instruction-guides-allguides.png "Stjórna leiðarvísum")</span><span class="sxs-lookup"><span data-stu-id="269fa-208">![Manage Guides](media/instruction-guides-allguides.png "Manage Guides")</span></span>

## <a name="associate-a-guide-to-a-resource-group"></a><a name="resource-groups"></a><span data-ttu-id="269fa-209">Tengja leiðarvísi við tilfangaflokk</span><span class="sxs-lookup"><span data-stu-id="269fa-209">Associate a Guide to a resource group</span></span>

<span data-ttu-id="269fa-210">Hægt er að bæta leiðarvísi við [tilfangaflokka](tasks/define-discrete-manufacturing-resource-group.md) ef þeir eru notaðir til að stjórna hópum af vélum, framleiðslulínum eða vinnuflokkum.</span><span class="sxs-lookup"><span data-stu-id="269fa-210">You can add a guide to [resource groups](tasks/define-discrete-manufacturing-resource-group.md) if you use them to manage groups of machines, production lines, or work cells.</span></span>

### <a name="typical-scenarios-using-resource-groups"></a><span data-ttu-id="269fa-211">Dæmigerðar aðstæður með tilfangaflokkum</span><span class="sxs-lookup"><span data-stu-id="269fa-211">Typical scenarios using resource groups</span></span>

<span data-ttu-id="269fa-212">**Dæmi 1:** Tilfangaflokkur hefur verið skilgreindur fyrir nokkrar vélar af sömu gerðinni.</span><span class="sxs-lookup"><span data-stu-id="269fa-212">**Example 1:** You have defined a resource group for several machines of the same model.</span></span> <span data-ttu-id="269fa-213">Í stað þess að úthluta viðeigandi leiðarvísi um meðhöndlun fyrir vélargerðina á öll viðeigandi tilföng, mætti þess í stað úthluta leiðarvísinum á tilfangaflokkinn sem endurspeglar þessa vélargerð.</span><span class="sxs-lookup"><span data-stu-id="269fa-213">Instead of assigning the relevant handling instruction guide for the machine model to every relevant resource, you could instead assign the Guide to the resource group that reflects that machine model.</span></span>

<span data-ttu-id="269fa-214">**Dæmi 2:** Tilfangaflokkur hefur verið skilgreindur fyrir vinnuflokk sem inniheldur mismunandi vélar og til er leiðarvísir sem veitir almennar leiðbeiningar um hvernig á að halda utan um vinnuflokkinn.</span><span class="sxs-lookup"><span data-stu-id="269fa-214">**Example 2:** You have defined a resource group for a work cell that contains different machines and you have a Guide that provides general instructions for how to maintain the work cell.</span></span> <span data-ttu-id="269fa-215">Leiðarvísirinn á við um hvers kyns framleiðsluaðgerðir í þessum vinnuflokki.</span><span class="sxs-lookup"><span data-stu-id="269fa-215">The Guide applies to any production activity in this work cell.</span></span>

### <a name="add-a-guide-to-a-resource-group"></a><span data-ttu-id="269fa-216">Bæta leiðarvísi við tilfangaflokk</span><span class="sxs-lookup"><span data-stu-id="269fa-216">Add a Guide to a resource group</span></span>

<span data-ttu-id="269fa-217">Til að bæta leiðarvísi við tilfangaflokk:</span><span class="sxs-lookup"><span data-stu-id="269fa-217">To add a Guide to a resource group:</span></span>

1. <span data-ttu-id="269fa-218">Farið í **Framleiðslustýringu \> Uppsetning \> Tilföng \> Tilfangaflokkar**.</span><span class="sxs-lookup"><span data-stu-id="269fa-218">Go to **Production control \> Setup \> Resources \> Resource groups**.</span></span>
1. <span data-ttu-id="269fa-219">Í listasvæðinu skal velja tilfangaflokkinn sem á að úthluta leiðarvísi á.</span><span class="sxs-lookup"><span data-stu-id="269fa-219">From the list pane, select the resource group you want to assign a Guide to.</span></span>
1. <span data-ttu-id="269fa-220">Stækkið flýtiflipann **Tengdir leiðarvísar**.</span><span class="sxs-lookup"><span data-stu-id="269fa-220">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="269fa-221">Veljið **Bæta við** úr tækjastikunni **Tengdir leiðarvísar**.</span><span class="sxs-lookup"><span data-stu-id="269fa-221">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="269fa-222">Nýrri línu er bætt við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="269fa-222">A new line is added to the grid.</span></span>
1. <span data-ttu-id="269fa-223">Fyrir nýju línuna skal nota fellilistann í dálkinum **Heiti** til að velja leiðarvísinn sem á að úthluta.</span><span class="sxs-lookup"><span data-stu-id="269fa-223">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span> <span data-ttu-id="269fa-224">Ef til er mikill fjöldi leiðarvísa, er hægt að sía listann til að finna þann sem verið er að leita að.</span><span class="sxs-lookup"><span data-stu-id="269fa-224">If you have a large number of Guides, then you can filter the list to find the one you are looking for.</span></span>
    <span data-ttu-id="269fa-225">![Leiðarvísi bætt við tilfangaflokk](media/instruction-guides-resourcegroup.png "Leiðarvísi bætt við tilfangaflokk")</span><span class="sxs-lookup"><span data-stu-id="269fa-225">![Adding a Guide to a resource group](media/instruction-guides-resourcegroup.png "Adding a Guide to a resource group")</span></span>

## <a name="associate-a-guide-to-a-released-product"></a><a name="released-products"></a><span data-ttu-id="269fa-226">Tengja leiðarvísi við útgefna afurð</span><span class="sxs-lookup"><span data-stu-id="269fa-226">Associate a Guide to a released product</span></span>

<span data-ttu-id="269fa-227">Hægt er að bæta leiðarvísi við hvaða [útgefna afurð](../pim/tasks/create-released-product-single-company.md) sem er.</span><span class="sxs-lookup"><span data-stu-id="269fa-227">You can add a guide to any [released product](../pim/tasks/create-released-product-single-company.md).</span></span>

### <a name="typical-scenario-using-released-products"></a><span data-ttu-id="269fa-228">Dæmigerðar aðstæður þar sem útgefnar afurðir eru notaðar</span><span class="sxs-lookup"><span data-stu-id="269fa-228">Typical scenario using released products</span></span>

<span data-ttu-id="269fa-229">Leiðarvísar á framleiðslustigi hjálpa starfsmönnum í vinnusal með leiðbeiningar sem tengjast stýringu eða meðhöndlun á tiltekinni útgefinni afurð eða vöru.</span><span class="sxs-lookup"><span data-stu-id="269fa-229">Product-level Guides help shop floor workers with instructions relevant to operating or handling a specific released product or item.</span></span>

### <a name="add-a-guide-to-a-released-product"></a><span data-ttu-id="269fa-230">Bæta leiðarvísi við útgefna afurð</span><span class="sxs-lookup"><span data-stu-id="269fa-230">Add a Guide to a released product</span></span>

<span data-ttu-id="269fa-231">Leiðarvísi bætt við útgefna afurð:</span><span class="sxs-lookup"><span data-stu-id="269fa-231">To add a Guide to a released product:</span></span>

1. <span data-ttu-id="269fa-232">Opna **Framleiðslustjórnun \> Afurðir \> Útgefnar afurðir**.</span><span class="sxs-lookup"><span data-stu-id="269fa-232">Go to **Production information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="269fa-233">Opnið afurðina sem á að úthluta leiðarvísi á.</span><span class="sxs-lookup"><span data-stu-id="269fa-233">Open the product you want to assign a Guide to.</span></span>
1. <span data-ttu-id="269fa-234">Á aðgerðasvæðinu skal opna flipann **Hönnuður** og í flokknum **Yfirlit** skal velja **Tengdir leiðarvísar**.</span><span class="sxs-lookup"><span data-stu-id="269fa-234">On the Action Pane, open the **Engineer** tab and from the **View** group, select **Associated Guides**.</span></span>
1. <span data-ttu-id="269fa-235">Síðan **Tengdir leiðarvísar** opnast fyrir valda afurð.</span><span class="sxs-lookup"><span data-stu-id="269fa-235">The **Associated Guides** page opens for your selected product.</span></span>
1. <span data-ttu-id="269fa-236">Veljið **Bæta við** á aðgerðasvæðinu til að bæta nýrri línu við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="269fa-236">Select **Add** on the Action Pane to add a new line to the grid.</span></span> 
1. <span data-ttu-id="269fa-237">Fyrir nýju línuna skal nota fellilistann í dálkinum **Heiti** til að velja leiðarvísinn sem á að úthluta.</span><span class="sxs-lookup"><span data-stu-id="269fa-237">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="269fa-238">![Leiðarvísi bætt við útgefna afurð](media/instruction-guides-ReleasedProduct-AddGuides.png "Leiðarvísi bætt við útgefna afurð")</span><span class="sxs-lookup"><span data-stu-id="269fa-238">![Adding a Guide to a released product](media/instruction-guides-ReleasedProduct-AddGuides.png "Adding a Guide to a released product")</span></span>

## <a name="associate-a-guide-to-a-formula"></a><a name="formulas"></a><span data-ttu-id="269fa-239">Tengja leiðarvísi við formúlu</span><span class="sxs-lookup"><span data-stu-id="269fa-239">Associate a Guide to a formula</span></span>

<span data-ttu-id="269fa-240">Hægt er að bæta leiðarvísi við hvaða [formúlu](bill-of-material-bom.md#formulas-co-products-and-by-products) sem er.</span><span class="sxs-lookup"><span data-stu-id="269fa-240">You can add a guide to any [formula](bill-of-material-bom.md#formulas-co-products-and-by-products).</span></span>

### <a name="typical-scenario-using-formulas"></a><span data-ttu-id="269fa-241">Dæmigerðar aðstæður með því að nota formúlur</span><span class="sxs-lookup"><span data-stu-id="269fa-241">Typical scenario using formulas</span></span>
  
<span data-ttu-id="269fa-242">Leiðarvísar á formúlustigi bjóða starfsmönnum í vinnusal upp á leiðarvísi fyrir meðhöndlun í samhengi við formúlu eða uppskrift.</span><span class="sxs-lookup"><span data-stu-id="269fa-242">Formula-level Guides provide shop floor workers with guided handling instructions in the context of a formula or recipe.</span></span> <span data-ttu-id="269fa-243">Einnig er hægt að úthluta leiðsögnum á útgáfur formúlu.</span><span class="sxs-lookup"><span data-stu-id="269fa-243">Guides can also be assigned to versions of a formula.</span></span>

> [!NOTE]
> <span data-ttu-id="269fa-244">Hægt er að úthluta leiðsögn sem tengist framleiðsluferlum sem byggja á formúlu eða leið, leiðarútgáfu, eða tengsl leiðarútgáfa.</span><span class="sxs-lookup"><span data-stu-id="269fa-244">You can assign guidance relevant for production processes based on a formula to a route, route version, or route operation relations.</span></span>  

> <span data-ttu-id="269fa-245">Ekki er hægt að tengja leiðarvísa við einstakar formúlulínur sem stendur.</span><span class="sxs-lookup"><span data-stu-id="269fa-245">Guides can't currently be attached to individual formula lines.</span></span>

### <a name="add-a-guide-to-a-formula"></a><span data-ttu-id="269fa-246">Bæta leiðarvísi við formúlu</span><span class="sxs-lookup"><span data-stu-id="269fa-246">Add a Guide to a formula</span></span>

<span data-ttu-id="269fa-247">Leiðarvísi bætt við formúlu:</span><span class="sxs-lookup"><span data-stu-id="269fa-247">To add a Guide to a formula:</span></span>

1. <span data-ttu-id="269fa-248">Farið í **Stjórnun framleiðsluupplýsinga \> Uppskriftir og formúlur \> Formúlur**.</span><span class="sxs-lookup"><span data-stu-id="269fa-248">Go to **Production information management \> Bills of materials and formulas \> Formulas**.</span></span>
1. <span data-ttu-id="269fa-249">Opnið formúluna sem á að úthluta leiðarvísi á.</span><span class="sxs-lookup"><span data-stu-id="269fa-249">Open the formula you want to assign a Guide to.</span></span>
1. <span data-ttu-id="269fa-250">Opnið flipann **Haus** fyrir ofan efsta flýtiflipann.</span><span class="sxs-lookup"><span data-stu-id="269fa-250">Open the **Header** tab above the top FastTab.</span></span>
1. <span data-ttu-id="269fa-251">Stækkið flýtiflipann **Tengdir leiðarvísar**.</span><span class="sxs-lookup"><span data-stu-id="269fa-251">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="269fa-252">Veljið **Bæta við** úr tækjastikunni **Tengdir leiðarvísar**.</span><span class="sxs-lookup"><span data-stu-id="269fa-252">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="269fa-253">Nýrri línu er bætt við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="269fa-253">A new line is added to the grid.</span></span>
1. <span data-ttu-id="269fa-254">Fyrir nýju línuna skal nota fellilistann í dálkinum **Heiti** til að velja leiðarvísinn sem á að úthluta.</span><span class="sxs-lookup"><span data-stu-id="269fa-254">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="269fa-255">![Leiðarvísi bætt við formúlu](media/instruction-guides-Formula.png "Leiðarvísi bætt við formúlu")</span><span class="sxs-lookup"><span data-stu-id="269fa-255">![Adding a Guide to a formula](media/instruction-guides-Formula.png "Adding a Guide to a formula")</span></span>

## <a name="associate-a-guide-to-a-formula-version"></a><a name="formula-versions"></a><span data-ttu-id="269fa-256">Tengja leiðarvísi við formúluútgáfu</span><span class="sxs-lookup"><span data-stu-id="269fa-256">Associate a Guide to a formula version</span></span>

<span data-ttu-id="269fa-257">Hægt er að bæta leiðarvísi við [formúluútgáfu](bill-of-material-bom.md#bom-and-formula-versions).</span><span class="sxs-lookup"><span data-stu-id="269fa-257">You can add a guide to any [formula version](bill-of-material-bom.md#bom-and-formula-versions).</span></span>

### <a name="typical-scenario-using-formula-versions"></a><span data-ttu-id="269fa-258">Dæmigerðar aðstæður þar sem formúluútgáfur eru notaðar</span><span class="sxs-lookup"><span data-stu-id="269fa-258">Typical scenario using formula versions</span></span>

<span data-ttu-id="269fa-259">Leiðarvísar sem eru hengdir við ákveðna útgáfu af formúlu veita starfsmönnum vinnusalar leiðbeiningar sem fara í gegnum framleiðslu þessarar útgáfu af formúluuppskriftinni.</span><span class="sxs-lookup"><span data-stu-id="269fa-259">Guides attached to an individual version of a formula provide shop floor workers with instructions that walk through the production of that version of the formula recipe.</span></span>

> [!TIP]
> <span data-ttu-id="269fa-260">Hægt er að úthluta leiðsögn sem tengist framleiðsluferlum sem byggja á þessari formúluútgáfu á leið, leiðarútgáfu, eða tengsl leiðarútgáfa.</span><span class="sxs-lookup"><span data-stu-id="269fa-260">You can assign guidance relevant for production processes based on this formula version to a route, route version, or route operation relations.</span></span>  

> [!NOTE]
> <span data-ttu-id="269fa-261">Ekki er hægt að tengja leiðarvísa við einstakar formúlulínur sem stendur.</span><span class="sxs-lookup"><span data-stu-id="269fa-261">Guides can't currently be attached to individual formula lines.</span></span>

### <a name="add-a-guide-to-a-formula-version"></a><span data-ttu-id="269fa-262">Bæta leiðarvísi við formúluútgáfu</span><span class="sxs-lookup"><span data-stu-id="269fa-262">Add a Guide to a formula version</span></span>

<span data-ttu-id="269fa-263">Leiðarvísi bætt við formúluútgáfu:</span><span class="sxs-lookup"><span data-stu-id="269fa-263">To add a Guide to a formula version:</span></span>

1. <span data-ttu-id="269fa-264">Farið í **Stjórnun framleiðsluupplýsinga \> Uppskriftir og formúlur \> Formúlur**.</span><span class="sxs-lookup"><span data-stu-id="269fa-264">Go to **Production information management \> Bills of materials and formulas \> Formulas**.</span></span>
1. <span data-ttu-id="269fa-265">Opnið formúluna sem inniheldur útgáfu sem úthluta á leiðarvísi á.</span><span class="sxs-lookup"><span data-stu-id="269fa-265">Open the formula that includes a version that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="269fa-266">Opnið flipann **Haus** fyrir ofan efsta flýtiflipann.</span><span class="sxs-lookup"><span data-stu-id="269fa-266">Open the **Header** tab above the top FastTab.</span></span>
1. <span data-ttu-id="269fa-267">Í flýtiflipanum **Formúluútgáfur** skal velja útgáfuna sem úthluta á leiðarvísi á.</span><span class="sxs-lookup"><span data-stu-id="269fa-267">On the **Formula versions** FastTab, select the version you want to assign a Guide to.</span></span>
1. <span data-ttu-id="269fa-268">Í tækjastikunni **Formúluútgáfur** skal velja **Tengdir leiðarvísar**.</span><span class="sxs-lookup"><span data-stu-id="269fa-268">On the **Formula versions** toolbar, select **Associated Guides**.</span></span>
    <span data-ttu-id="269fa-269">![Opna leiðarvísana sem tengjast valdri formúluútgáfu](media/instruction-guides-FormulaVersion.png "Opna leiðarvísana sem tengjast valdri formúluútgáfu")</span><span class="sxs-lookup"><span data-stu-id="269fa-269">![Open the Guides associated with a selected formula version](media/instruction-guides-FormulaVersion.png "Open the Guides associated with a selected formula version")</span></span>
1. <span data-ttu-id="269fa-270">Síðan **Tengdir leiðarvísar** opnast fyrir formúluútgáfuna.</span><span class="sxs-lookup"><span data-stu-id="269fa-270">The **Associated Guides** page opens for your formula version.</span></span>
1. <span data-ttu-id="269fa-271">Veljið **Bæta við** á aðgerðasvæðinu til að bæta nýrri línu við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="269fa-271">Select **Add** on the Action Pane to add a new line to the grid.</span></span> 
1. <span data-ttu-id="269fa-272">Fyrir nýju línuna skal nota fellilistann í dálkinum **Heiti** til að velja leiðarvísinn sem á að úthluta.</span><span class="sxs-lookup"><span data-stu-id="269fa-272">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="269fa-273">![Leiðarvísi bætt við formúluútgáfu](media/instruction-guides-FormulaVersionAddGuide.png "Leiðarvísi bætt við formúluútgáfu")</span><span class="sxs-lookup"><span data-stu-id="269fa-273">![Adding a Guide to a formula version](media/instruction-guides-FormulaVersionAddGuide.png "Adding a Guide to a formula version")</span></span>

## <a name="associate-a-guide-to-a-bill-of-materials"></a><a name="bom"></a><span data-ttu-id="269fa-274">Bæta leiðarvísi við uppskriftir</span><span class="sxs-lookup"><span data-stu-id="269fa-274">Associate a Guide to a bill of materials</span></span>

<span data-ttu-id="269fa-275">Hægt er að bæta leiðarvísi við [uppskriftir](bill-of-material-bom.md).</span><span class="sxs-lookup"><span data-stu-id="269fa-275">You can add a guide to any [bill of materials](bill-of-material-bom.md) (BOM).</span></span>

### <a name="typical-scenario-using-bills-of-materials"></a><span data-ttu-id="269fa-276">Dæmigerðar aðstæður með uppskriftum</span><span class="sxs-lookup"><span data-stu-id="269fa-276">Typical scenario using bills of materials</span></span>

<span data-ttu-id="269fa-277">Leiðarvísar sem tengjast uppskrift veita starfsmönnum vinnusalar leiðbeiningar sem útskýra hvernig á að undirbúa og meðhöndla efni úr uppskrift.</span><span class="sxs-lookup"><span data-stu-id="269fa-277">Guides attached to a BOM provide shop floor workers with instructions that explain how to prepare and handle material from a BOM.</span></span> <span data-ttu-id="269fa-278">Einnig er hægt að úthluta leiðarvísum á útgáfur uppskriftar.</span><span class="sxs-lookup"><span data-stu-id="269fa-278">Guides can also be assigned to versions of a BOM.</span></span>

> [!NOTE]
> <span data-ttu-id="269fa-279">Ekki er hægt að tengja leiðarvísa við einstakar uppskriftarlínur sem stendur.</span><span class="sxs-lookup"><span data-stu-id="269fa-279">Guides can't currently be attached to individual BOM lines.</span></span>

### <a name="add-a-guide-to-a-bill-of-materials"></a><span data-ttu-id="269fa-280">Bæta leiðarvísi við uppskriftir</span><span class="sxs-lookup"><span data-stu-id="269fa-280">Add a Guide to a bill of materials</span></span>

<span data-ttu-id="269fa-281">Leiðarvísi bætt við uppskrift:</span><span class="sxs-lookup"><span data-stu-id="269fa-281">To add a Guide to a bill of material:</span></span>

1. <span data-ttu-id="269fa-282">Farið í **Stjórnun framleiðsluupplýsinga \> Uppskriftir og formúlur \> Uppskriftir**.</span><span class="sxs-lookup"><span data-stu-id="269fa-282">Go to **Production information management \> Bills of materials and formulas \> Bills of materials**.</span></span>
1. <span data-ttu-id="269fa-283">Opnið uppskriftirnar sem á að úthluta leiðarvísi á.</span><span class="sxs-lookup"><span data-stu-id="269fa-283">Open the bill of materials that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="269fa-284">Opnið flipann **Haus** fyrir ofan efsta flýtiflipann.</span><span class="sxs-lookup"><span data-stu-id="269fa-284">Open the **Header** tab above the top FastTab.</span></span>
1. <span data-ttu-id="269fa-285">Stækkið flýtiflipann **Tengdir leiðarvísar**.</span><span class="sxs-lookup"><span data-stu-id="269fa-285">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="269fa-286">Veljið **Bæta við** úr tækjastikunni **Tengdir leiðarvísar**.</span><span class="sxs-lookup"><span data-stu-id="269fa-286">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="269fa-287">Nýrri línu er bætt við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="269fa-287">A new line is added to the grid.</span></span>
1. <span data-ttu-id="269fa-288">Fyrir nýju línuna skal nota fellilistann í dálkinum **Heiti** til að velja leiðarvísinn sem á að úthluta.</span><span class="sxs-lookup"><span data-stu-id="269fa-288">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="269fa-289">![Leiðarvísi bætt við uppskrift](media/instruction-guides-BOM.png "Leiðarvísi bætt við uppskrift")</span><span class="sxs-lookup"><span data-stu-id="269fa-289">![Adding a Guide to a BOM](media/instruction-guides-BOM.png "Adding a Guide to a BOM")</span></span>

## <a name="associate-a-guide-to-a-bill-of-materials-version"></a><a name="bom-versions"></a><span data-ttu-id="269fa-290">Bæta leiðarvísi við uppskriftarútgáfu</span><span class="sxs-lookup"><span data-stu-id="269fa-290">Associate a Guide to a bill of materials version</span></span>

<span data-ttu-id="269fa-291">Hægt er að bæta leiðarvísi við hvaða [uppskriftarútgáfu](bill-of-material-bom.md#bom-and-formula-versions) sem er.</span><span class="sxs-lookup"><span data-stu-id="269fa-291">You can add a guide to any [bill of materials version](bill-of-material-bom.md#bom-and-formula-versions).</span></span>

### <a name="typical-scenario-using-bill-of-materials-versions"></a><span data-ttu-id="269fa-292">Dæmigerðar aðstæður þar sem uppskriftarútgáfur eru notaðar</span><span class="sxs-lookup"><span data-stu-id="269fa-292">Typical scenario using bill of materials versions</span></span>

<span data-ttu-id="269fa-293">Leiðarvísar sem hengdir eru við staka uppskriftarútgáfu veita starfsmönnum vinnusalar leiðbeiningar sem útskýra hvernig á að undirbúa og meðhöndla efni fyrir útgáfu af uppskrift sem er frábrugðin almennu uppskriftinni eða öðrum útgáfum hennar.</span><span class="sxs-lookup"><span data-stu-id="269fa-293">Guides attached to an individual BOM version provide shop floor workers with instructions that explain how to prepare and handle material for a version of a BOM that is different from the generic BOM or other versions of it.</span></span>

> [!NOTE]
> <span data-ttu-id="269fa-294">Ekki er hægt að tengja leiðarvísa við einstakar uppskriftarlínur sem stendur.</span><span class="sxs-lookup"><span data-stu-id="269fa-294">Guides can't currently be attached to individual BOM lines.</span></span>

### <a name="add-a-guide-to-a-bill-of-materials-version"></a><span data-ttu-id="269fa-295">Bæta leiðarvísi við uppskriftarútgáfu</span><span class="sxs-lookup"><span data-stu-id="269fa-295">Add a Guide to a bill of materials version</span></span>

<span data-ttu-id="269fa-296">Til að bæta við leiðarvísinum fyrir uppskriftarútgáfu:</span><span class="sxs-lookup"><span data-stu-id="269fa-296">To add a Guide to a bill of materials version:</span></span>

1. <span data-ttu-id="269fa-297">Farið í **Stjórnun framleiðsluupplýsinga \> Uppskriftir og formúlur \> Uppskriftir**.</span><span class="sxs-lookup"><span data-stu-id="269fa-297">Go to **Production information management \> Bills of materials and formulas \> Bills of materials**.</span></span>
1. <span data-ttu-id="269fa-298">Opnið uppskriftina sem inniheldur útgáfu sem úthluta á leiðarvísi á.</span><span class="sxs-lookup"><span data-stu-id="269fa-298">Open the BOM that includes a version that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="269fa-299">Opnið flipann **Haus** fyrir ofan efsta flýtiflipann.</span><span class="sxs-lookup"><span data-stu-id="269fa-299">Open the **Header** tab above the top FastTab.</span></span>
1. <span data-ttu-id="269fa-300">Í flýtiflipanum **Uppskriftaútgáfur** skal velja útgáfuna sem úthluta á leiðarvísi á.</span><span class="sxs-lookup"><span data-stu-id="269fa-300">On the **BOM versions** FastTab, select the version you want to assign a Guide to.</span></span>
1. <span data-ttu-id="269fa-301">Í tækjastikunni **Uppskriftaútgáfur** skal velja **Tengdir leiðarvísar**.</span><span class="sxs-lookup"><span data-stu-id="269fa-301">On the **BOM versions** toolbar, select **Associated Guides**.</span></span>
    <span data-ttu-id="269fa-302">![Opna leiðarvísana sem tengjast valdri uppskriftarútgáfu](media/instruction-guides-BOMVersion.png "Opna leiðarvísana sem tengjast valdri uppskriftarútgáfu")</span><span class="sxs-lookup"><span data-stu-id="269fa-302">![Open the Guides associated with a selected BOM version](media/instruction-guides-BOMVersion.png "Open the Guides associated with a selected BOM version")</span></span>
1. <span data-ttu-id="269fa-303">Síðan **Tengdir leiðarvísar** opnast fyrir uppskriftarútgáfuna.</span><span class="sxs-lookup"><span data-stu-id="269fa-303">The **Associated Guides** page opens for your BOM version.</span></span>
1. <span data-ttu-id="269fa-304">Veljið **Bæta við** á aðgerðasvæðinu til að bæta nýrri línu við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="269fa-304">Select **Add** on the Action Pane to add a new line to the grid.</span></span>
1. <span data-ttu-id="269fa-305">Fyrir nýju línuna skal nota fellilistann í dálkinum **Heiti** til að velja leiðarvísinn sem á að úthluta.</span><span class="sxs-lookup"><span data-stu-id="269fa-305">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="269fa-306">![Leiðarvísi bætt við uppskriftarútgáfu](media/instruction-guides-BOMVersionAddGuide.png "Leiðarvísi bætt við uppskriftarútgáfu")</span><span class="sxs-lookup"><span data-stu-id="269fa-306">![Adding a Guide to a BOM version](media/instruction-guides-BOMVersionAddGuide.png "Adding a Guide to a BOM version")</span></span>

## <a name="associate-a-guide-to-a-route"></a><a name="routes"></a><span data-ttu-id="269fa-307">Tengja leiðarvísi við leið</span><span class="sxs-lookup"><span data-stu-id="269fa-307">Associate a Guide to a route</span></span>

<span data-ttu-id="269fa-308">Hægt er að bæta leiðarvísi við hvaða [leið](routes-operations.md) sem er.</span><span class="sxs-lookup"><span data-stu-id="269fa-308">You can add a guide to any [route](routes-operations.md).</span></span>

### <a name="typical-scenario-using-routes"></a><span data-ttu-id="269fa-309">Dæmigerðar aðstæður með leiðum</span><span class="sxs-lookup"><span data-stu-id="269fa-309">Typical scenario using routes</span></span>

<span data-ttu-id="269fa-310">Leiðir eru gjarnan notaðar til að segja til um hvernig á framleiða ákveðna útgefna afurð samkvæmt uppskrift eða uppskriftarútgáfu og með safn af tilföngum eða tilfangaflokkum.</span><span class="sxs-lookup"><span data-stu-id="269fa-310">Routes are typically used to specify how a certain released product shall be produced based on a BOM or BOM version and with a set of resources or resource groups.</span></span>

<span data-ttu-id="269fa-311">Úthlutið leiðarvísi á leið til að veita ítarlegar leiðbeiningar fyrir viðkomandi framleiðsluferli.</span><span class="sxs-lookup"><span data-stu-id="269fa-311">Assign a Guide to a route to provide step-by-step instructions for the respective production process.</span></span>

### <a name="add-a-guide-to-a-route"></a><span data-ttu-id="269fa-312">Bæta leiðarvísi við leið</span><span class="sxs-lookup"><span data-stu-id="269fa-312">Add a Guide to a route</span></span>

<span data-ttu-id="269fa-313">Leiðarvísi bætt við leið:</span><span class="sxs-lookup"><span data-stu-id="269fa-313">To add a Guide to a route:</span></span>

1. <span data-ttu-id="269fa-314">Farið í **Framleiðslustýring \> Allar leiðir**.</span><span class="sxs-lookup"><span data-stu-id="269fa-314">Go to **Production control \> All routes**.</span></span>
1. <span data-ttu-id="269fa-315">Opnið leiðina sem á að úthluta leiðarvísi á.</span><span class="sxs-lookup"><span data-stu-id="269fa-315">Open the route that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="269fa-316">Stækkið flýtiflipann **Tengdir leiðarvísar**.</span><span class="sxs-lookup"><span data-stu-id="269fa-316">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="269fa-317">Veljið **Bæta við** úr tækjastikunni **Tengdir leiðarvísar**.</span><span class="sxs-lookup"><span data-stu-id="269fa-317">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="269fa-318">Nýrri línu er bætt við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="269fa-318">A new line is added to the grid.</span></span>
1. <span data-ttu-id="269fa-319">Fyrir nýju línuna skal nota fellilistann í dálkinum **Heiti** til að velja leiðarvísinn sem á að úthluta.</span><span class="sxs-lookup"><span data-stu-id="269fa-319">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="269fa-320">![Leiðarvísi bætt við leið](media/instruction-guides-Route.png "Leiðarvísi bætt við leið")</span><span class="sxs-lookup"><span data-stu-id="269fa-320">![Adding a Guide to a route](media/instruction-guides-Route.png "Adding a Guide to a route")</span></span>

## <a name="associate-a-guide-to-a-route-version"></a><a name="route-versions"></a><span data-ttu-id="269fa-321">Tengja leiðarvísi við leiðarútgáfu</span><span class="sxs-lookup"><span data-stu-id="269fa-321">Associate a Guide to a route version</span></span>

<span data-ttu-id="269fa-322">Hægt er að bæta leiðarvísi við hvaða [leiðarútgáfu](routes-operations.md#route-versions) sem er.</span><span class="sxs-lookup"><span data-stu-id="269fa-322">You can add a guide to any [route version](routes-operations.md#route-versions).</span></span>

### <a name="typical-scenario-using-route-versions"></a><span data-ttu-id="269fa-323">Dæmigerðar aðstæður með leiðaútgáfum</span><span class="sxs-lookup"><span data-stu-id="269fa-323">Typical scenario using route versions</span></span>

<span data-ttu-id="269fa-324">Leiðarútgáfur eru yfirleitt notaðar til að tilgreina afbrigði af framleiðsluferlum sem byggja á fyrirliggjandi leið.</span><span class="sxs-lookup"><span data-stu-id="269fa-324">Routes versions are typically used to specify variants of production processes based on an existing route.</span></span> <span data-ttu-id="269fa-325">Hægt er að úthluta mismunandi leiðarvísum á hverja leiðarútgáfu.</span><span class="sxs-lookup"><span data-stu-id="269fa-325">You can assign different Guides to each route version.</span></span>

### <a name="add-a-guide-to-a-route-version"></a><span data-ttu-id="269fa-326">Bæta leiðarvísi við leiðarútgáfu</span><span class="sxs-lookup"><span data-stu-id="269fa-326">Add a Guide to a route version</span></span>

<span data-ttu-id="269fa-327">Leiðarvísi bætt við leiðarútgáfu:</span><span class="sxs-lookup"><span data-stu-id="269fa-327">To add a Guide to a route version:</span></span>

1. <span data-ttu-id="269fa-328">Farið í **Framleiðslustýring \> Allar leiðir**.</span><span class="sxs-lookup"><span data-stu-id="269fa-328">Go to **Production control \> All routes**.</span></span>
1. <span data-ttu-id="269fa-329">Opnið leiðina sem á að úthluta leiðarvísi á.</span><span class="sxs-lookup"><span data-stu-id="269fa-329">Open the route that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="269fa-330">Í flýtiflipanum **Útgáfur** skal velja útgáfuna sem úthluta á leiðarvísi á.</span><span class="sxs-lookup"><span data-stu-id="269fa-330">On the **Versions** FastTab, select the version you want to assign a Guide to.</span></span>
1. <span data-ttu-id="269fa-331">Í tækjastikunni **Útgáfur** skal velja **Tengdir leiðarvísar**.</span><span class="sxs-lookup"><span data-stu-id="269fa-331">On the **Versions** toolbar, select **Associated Guides**.</span></span>
    <span data-ttu-id="269fa-332">![Opna leiðarvísana sem tengjast valdri leiðarútgáfu](media/instruction-guides-RouteVersion.png "Opna leiðarvísana sem tengjast valdri leiðarútgáfu")</span><span class="sxs-lookup"><span data-stu-id="269fa-332">![Open the Guides associated with a selected route version](media/instruction-guides-RouteVersion.png "Open the Guides associated with a selected route version")</span></span>
1. <span data-ttu-id="269fa-333">Síðan **Tengdir leiðarvísar** opnast fyrir uppskriftarútgáfuna.</span><span class="sxs-lookup"><span data-stu-id="269fa-333">The **Associated Guides** page opens for your BOM version.</span></span>
1. <span data-ttu-id="269fa-334">Veljið **Bæta við** á aðgerðasvæðinu til að bæta nýrri línu við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="269fa-334">Select **Add** on the Action Pane to add a new line to the grid.</span></span>
1. <span data-ttu-id="269fa-335">Fyrir nýju línuna skal nota fellilistann í dálkinum **Heiti** til að velja leiðarvísinn sem á að úthluta.</span><span class="sxs-lookup"><span data-stu-id="269fa-335">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="269fa-336">![Leiðarvísi bætt við leiðarútgáfu](media/instruction-guides-RouteVersionAddGuide.png "Leiðarvísi bætt við leiðarútgáfu")</span><span class="sxs-lookup"><span data-stu-id="269fa-336">![Adding a Guide to a route version](media/instruction-guides-RouteVersionAddGuide.png "Adding a Guide to a route version")</span></span>

## <a name="associate-a-guide-to-a-route-operation-relation"></a><a name="route-operation-relations"></a><span data-ttu-id="269fa-337">Tengja leiðarvísi við tengsl leiðaraðgerðar</span><span class="sxs-lookup"><span data-stu-id="269fa-337">Associate a Guide to a route operation relation</span></span>

<span data-ttu-id="269fa-338">Hægt er að bæta við leiðarvísi á hvaða [tengsl leiðaraðgerðar](routes-operations.md#operation-relations) sem er.</span><span class="sxs-lookup"><span data-stu-id="269fa-338">You can add a guide to any [route operation relation](routes-operations.md#operation-relations).</span></span>

### <a name="typical-scenario-using-route-operation-relations"></a><span data-ttu-id="269fa-339">Dæmigerðar aðstæður þar sem tengsl leiðaraðgerðar eru notuð</span><span class="sxs-lookup"><span data-stu-id="269fa-339">Typical scenario using route operation relations</span></span>

<span data-ttu-id="269fa-340">Aðgerðatengsl eru sértækasta leiðin til að bæta leiðsögn við framleiðsluferli og tengdar aðgerðir.</span><span class="sxs-lookup"><span data-stu-id="269fa-340">Operation relations are the most specific way to add guidance to a product process and its related operations.</span></span> <span data-ttu-id="269fa-341">Hægt er að tilgreina leiðsögn fyrir hverja aðgerð í leið og tilgreina mismunandi leiðsagnir fyrir hvers kyns samhengi af tengslum sem tilgreind eru fyrir leið, t.d. fyrir tilteknar vörur, skilgreiningar o.m.fl.</span><span class="sxs-lookup"><span data-stu-id="269fa-341">You can specify guidance for each operation in a route and specify different guidance for any type of relation context specified for a route, such as for specific items, configurations, and more.</span></span> <span data-ttu-id="269fa-342">Einnig er hægt að tilgreina á hvaða stigum í aðgerðinni leiðsögnin gildir (svo sem uppsetningu, biðröð, ferli eða flutning).</span><span class="sxs-lookup"><span data-stu-id="269fa-342">You can also specify to which stages in the operation the guidance applies (such as setup, queueing, process, or transport).</span></span>

> [!NOTE]
> <span data-ttu-id="269fa-343">Ef leiðarvísar eru tilgreindir fyrir mörg aðgerðartengsl leiðar, þ.á.m. þessir leiðarvísar, verður aðeins leiðarvísirinn úr sértækustu tengslunum sýndur í vinnusal fyrir verkið sem er búið til.</span><span class="sxs-lookup"><span data-stu-id="269fa-343">If you specify guides for several operation relations of a route, among those guides, only the guide from the most specific relation will be show on the shop floor for the generated job.</span></span>

### <a name="add-a-guide-to-a-route-operation-relation"></a><span data-ttu-id="269fa-344">Bæta leiðarvísi við tengsl leiðaraðgerðar</span><span class="sxs-lookup"><span data-stu-id="269fa-344">Add a Guide to a route operation relation</span></span>

<span data-ttu-id="269fa-345">Leiðarvísi bætt við tengsl leiðaraðgerðar:</span><span class="sxs-lookup"><span data-stu-id="269fa-345">To add a Guide to a route operation relation:</span></span>

1. <span data-ttu-id="269fa-346">Farið í **Framleiðslustýring \> Allar leiðir**.</span><span class="sxs-lookup"><span data-stu-id="269fa-346">Go to **Production control \> All routes**.</span></span>
1. <span data-ttu-id="269fa-347">Opnið leiðina sem á að úthluta leiðarvísi á.</span><span class="sxs-lookup"><span data-stu-id="269fa-347">Open the route that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="269fa-348">Á aðgerðasvæðinu skal opna flipann **Leið** og í flokknum **Vinna með** skal velja **Upplýsingar um leið**.</span><span class="sxs-lookup"><span data-stu-id="269fa-348">On the Action Pane, open the **Route** tab and from the **Maintain** group, select **Route details**.</span></span>
1. <span data-ttu-id="269fa-349">Síðan **Upplýsingar um leið** opnast fyrir valda leið.</span><span class="sxs-lookup"><span data-stu-id="269fa-349">The **Route details** page opens for your selected rout.</span></span>
1. <span data-ttu-id="269fa-350">Í efsta hnitanetinu skal velja aðgerðina sem á að fá leiðsögn.</span><span class="sxs-lookup"><span data-stu-id="269fa-350">In the top grid, select the operation you want to provide guidance for.</span></span>
1. <span data-ttu-id="269fa-351">Í neðsta hnitanetinu skal velja sértæk tengsl (eða almennu tengslin **Allt**).</span><span class="sxs-lookup"><span data-stu-id="269fa-351">In the bottom grid, select a specific relation (or the generic **All** relation).</span></span>
    <span data-ttu-id="269fa-352">![Velja aðgerð og síðan tengsl](media/instruction-guides-RouteOperationRelation.png "Velja aðgerð og síðan tengsl")</span><span class="sxs-lookup"><span data-stu-id="269fa-352">![Select an operation and then a relation](media/instruction-guides-RouteOperationRelation.png "Select an operation and then a relation")</span></span>
1. <span data-ttu-id="269fa-353">Fyrir ofan neðsta hnitanetið skal opna flipann **Tengdir leiðarvísar**. ![Flipinn tengdir leiðarvísar](media/instruction-guides-RouteOperationRelation-AddGuide.png "Flipi tengdra leiðarvísa")</span><span class="sxs-lookup"><span data-stu-id="269fa-353">Above the bottom gird, open the **Associated Guides** tab.  ![The Associated Guides tab](media/instruction-guides-RouteOperationRelation-AddGuide.png "The Associated Guides tab")</span></span>
1. <span data-ttu-id="269fa-354">Veljið **Bæta við** í tækjastikunni efst í neðsta hnitanetinu til að bæta nýrri línu við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="269fa-354">Select **Add** from the toolbar at the top of the bottom grid to add a new line to the grid.</span></span>
1. <span data-ttu-id="269fa-355">Fyrir nýju línuna skal nota fellilistann í dálkinum **Heiti** til að velja leiðarvísinn sem á að úthluta.</span><span class="sxs-lookup"><span data-stu-id="269fa-355">For the new row, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span> <span data-ttu-id="269fa-356">Það sem eftir er af línunni skal velja gátreitinn fyrir hvert samhengi þar sem valinn leiðarvísir á að vera tiltækur.</span><span class="sxs-lookup"><span data-stu-id="269fa-356">In the rest of the row, select the check box for each context where the selected Guide should be available.</span></span>

> [!NOTE]
> <span data-ttu-id="269fa-357">Hægt er að bæta við einum eða fleiri leiðarvísum fyrir hvert stig af hverri aðgerð.</span><span class="sxs-lookup"><span data-stu-id="269fa-357">You can add one or more guides for each stage of each operation.</span></span>

## <a name="select-guides-from-the-shop-floor-execution-interface"></a><span data-ttu-id="269fa-358">Velja leiðarvísa úr keyrsluviðmóti vinnusalar</span><span class="sxs-lookup"><span data-stu-id="269fa-358">Select guides from the shop floor execution interface</span></span>

<span data-ttu-id="269fa-359">Þegar starfsmaður opnar verklista í keyrsluviðmóti vinnusalar, finnur Supply Chain Management viðeigandi leiðarvísa fyrir verkin sem sýnd eru.</span><span class="sxs-lookup"><span data-stu-id="269fa-359">When a worker opens a job list on the shop floor execution interface, Supply Chain Management finds the relevant guides for the jobs shown.</span></span> <span data-ttu-id="269fa-360">Notið hnappinn **Leiðarvísar** til að skoða viðeigandi leiðarvísa.</span><span class="sxs-lookup"><span data-stu-id="269fa-360">Use the **Guides** button to view the relevant guides.</span></span>

<span data-ttu-id="269fa-361">![Leiðarvísishnappur í keyrsluviðmóti vinnusalar](media/instruction-guides-Shopfloor1.png "Leiðarvísishnappur í keyrsluviðmóti vinnusalar")</span><span class="sxs-lookup"><span data-stu-id="269fa-361">![Guides button in the shop floor execution interface](media/instruction-guides-Shopfloor1.png "Guides button in the shop floor execution interface")</span></span>

<span data-ttu-id="269fa-362">Síðan skal setja á HoloLens og fá aðgang að viðkomandi leiðarvísi með því að skanna QR-kóðann og virkja leiðarvísinn.</span><span class="sxs-lookup"><span data-stu-id="269fa-362">Then put on a HoloLens and access the respective guide by glancing at the QR code and activating the respective Guide.</span></span>

<span data-ttu-id="269fa-363">![QR-kóði til að fá aðgang að leiðsögnum með því að nota HoloLens](media/instruction-guides-Shopfloor2.png "QR-kóði til að fá aðgang að leiðsögnum með því að nota HoloLens")</span><span class="sxs-lookup"><span data-stu-id="269fa-363">![QR code to access guides using a HoloLens](media/instruction-guides-Shopfloor2.png "QR code to access guides using a HoloLens")</span></span>

## <a name="resolving-the-logic-for-selecting-guides"></a><a name="logic"></a><span data-ttu-id="269fa-364">Að leysa úr reglunni fyrir val á leiðarvísum</span><span class="sxs-lookup"><span data-stu-id="269fa-364">Resolving the logic for selecting Guides</span></span>

<span data-ttu-id="269fa-365">Hægt er að bæta leiðarvísum við eftirfarandi framleiðslugögn:</span><span class="sxs-lookup"><span data-stu-id="269fa-365">You can add Guides to the following production data:</span></span>

- [<span data-ttu-id="269fa-366">Forði</span><span class="sxs-lookup"><span data-stu-id="269fa-366">Resources</span></span>](#resources)
- [<span data-ttu-id="269fa-367">Tilfangaflokkar</span><span class="sxs-lookup"><span data-stu-id="269fa-367">Resource groups</span></span>](#resource-groups)
- [<span data-ttu-id="269fa-368">Útgefnar afurðir</span><span class="sxs-lookup"><span data-stu-id="269fa-368">Released products</span></span>](#released-products)
- [<span data-ttu-id="269fa-369">Formúlur</span><span class="sxs-lookup"><span data-stu-id="269fa-369">Formulas</span></span>](#formulas)
- [<span data-ttu-id="269fa-370">Formúluútgáfur</span><span class="sxs-lookup"><span data-stu-id="269fa-370">Formula versions</span></span>](#formula-versions)
- [<span data-ttu-id="269fa-371">Uppskriftir</span><span class="sxs-lookup"><span data-stu-id="269fa-371">Bills of material (BOMs)</span></span>](#bom)
- [<span data-ttu-id="269fa-372">Uppskriftaútgáfur</span><span class="sxs-lookup"><span data-stu-id="269fa-372">BOM versions</span></span>](#bom-versions)
- [<span data-ttu-id="269fa-373">Leiðir</span><span class="sxs-lookup"><span data-stu-id="269fa-373">Routes</span></span>](#routes)
- [<span data-ttu-id="269fa-374">Leiðarútgáfur</span><span class="sxs-lookup"><span data-stu-id="269fa-374">Route versions</span></span>](#route-versions)
- [<span data-ttu-id="269fa-375">Tengsl leiðaraðgerðar</span><span class="sxs-lookup"><span data-stu-id="269fa-375">Route operation relations</span></span>](#route-operation-relations)

<span data-ttu-id="269fa-376">Þegar Supply Chain Management býr til verkin fyrir framleiðslugólfið, safnar það saman viðeigandi leiðarvísum úr þessum upprunastöðum.</span><span class="sxs-lookup"><span data-stu-id="269fa-376">When Supply Chain Management generates the jobs for the production floor, it will collect the relevant Guides from those sources.</span></span> <span data-ttu-id="269fa-377">Taka skal tillit til eftirfarandi mikilvægra reglna.</span><span class="sxs-lookup"><span data-stu-id="269fa-377">Take note of the following important rules.</span></span>

- <span data-ttu-id="269fa-378">Ef uppskriftarútgáfa eða formúluútgáfa er hengd við leið eða framleiðslupöntun, þá verða allir leiðarvísar sem hengdir eru við þessa útgáfu, og einnig leiðarvísar sem hengdir eru við yfiruppskrift eða -formúlu þessara útgáfu, sýndir í verkinu.</span><span class="sxs-lookup"><span data-stu-id="269fa-378">If you attach a BOM version or formula version to a route or production order, then any Guides attached to this version, and also the Guides attached to the parent BOM or formula of that version, will be shown on the job.</span></span>
- <span data-ttu-id="269fa-379">Ef leiðarútgáfa eða framleiðsluútgáfa er hengd við framleiðslupöntun, þá verða allir leiðarvísar sem hengdir eru við þessa útgáfu, og einnig leiðarvísar sem hengdir eru við yfirleið þessara útgáfu, sýndir í verkinu.</span><span class="sxs-lookup"><span data-stu-id="269fa-379">If you attach a route version to a production order, then any Guides attached to this version, and also the Guides attached to the parent route of that version, will be shown on the job.</span></span>
- <span data-ttu-id="269fa-380">Ef mörg tengsl leiðaraðgerða eru skilgreind sem innihalda tengslin *Allt* og leiðarvísum er úthlutað á þau, verða aðeins leiðarvísarnir úr sértækustu tengslunum sýndir fyrir verkið.</span><span class="sxs-lookup"><span data-stu-id="269fa-380">If you define several route operation relations that include the *All* relation and assign Guides to those, only the Guides from the most specific relation will be shown for the job.</span></span>  

<span data-ttu-id="269fa-381">![Skýringarmynd um úrlausn viðeigandi leiðarvísa](media/instruction-guides-Resolve.png "Skýringarmynd um úrlausn viðeigandi leiðarvísa")</span><span class="sxs-lookup"><span data-stu-id="269fa-381">![Diagram on resolving the relevant Guides](media/instruction-guides-Resolve.png "Diagram on resolving the relevant Guides")</span></span>
