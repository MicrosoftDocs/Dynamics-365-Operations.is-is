---
title: Stigveldi fyrirtækis í Common Data Service
description: Þetta efni lýsir samþættingu stigveldisgagna milli forrita Finance and Operations og Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 9a12ab249129dce24cdca5e29d737fa9f68c0eac
ms.sourcegitcommit: 6e0909e95f38b7487a4b7f68cc62b723f8b59bd4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/10/2019
ms.locfileid: "2572450"
---
# <a name="organization-hierarchy-in-common-data-service"></a><span data-ttu-id="8222d-103">Stigveldi fyrirtækis í Common Data Service</span><span class="sxs-lookup"><span data-stu-id="8222d-103">Organization hierarchy in Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="8222d-104">Vegna þess að Dynamics 365 Finance er fjármálakerfi er *fyrirtæki* kjarnahugtak og kerfisuppsetning byrjar með stillingu fyrirtækisstigveldis.</span><span class="sxs-lookup"><span data-stu-id="8222d-104">Because Dynamics 365 Finance is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="8222d-105">Síðan er hægt að rekja fjárhag fyrirtækja á fyrirtækjastigi og einnig á hvaða stigi sem er í fyrirtækjastigveldinu.</span><span class="sxs-lookup"><span data-stu-id="8222d-105">Business financials can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="8222d-106">Þó að Common Data Service sé ekki með hugtak fyrirtækjastigveldis er það með nokkur laus hugtök, svo sem heildarsölutekjur.</span><span class="sxs-lookup"><span data-stu-id="8222d-106">Although Common Data Service doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="8222d-107">Sem hluti af samþættingu Common Data Service er gagnaskipulag stigveldis fyrirtækis er bætt við Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="8222d-107">As part of Common Data Service integration, the organization hierarchy data structure is added to Common Data Service.</span></span>

## <a name="data-flow"></a><span data-ttu-id="8222d-108">Gagnaflæði</span><span class="sxs-lookup"><span data-stu-id="8222d-108">Data flow</span></span>

<span data-ttu-id="8222d-109">Vistkerfi fyrirtækja sem samanstendur af forritum Finance and Operations og Common Data Service mun halda áfram að hafa stigveldi fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="8222d-109">A business ecosystem that consists of Finance and Operations apps and Common Data Service will continue to have an organization hierarchy.</span></span> <span data-ttu-id="8222d-110">Þetta stigveldi fyrirtækis er byggt á forritum Finance and Operations, en það er útsett í Common Data Service í upplýsinga- og stækkunarlegum tilgangi.</span><span class="sxs-lookup"><span data-stu-id="8222d-110">This organization hierarchy is built on Finance and Operations apps, but it's exposed in Common Data Service for informational and extensibility purposes.</span></span> <span data-ttu-id="8222d-111">Eftirfarandi mynd sýnir upplýsingar um stigveldi fyrirtækis sem birtast í Common Data Service sem einstefnugagnaflæði úr forritum Finance and Operations til Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="8222d-111">The following illustration shows the organization hierarchy information that is exposed in Common Data Service as a one-way data flow from Finance and Operations apps to Common Data Service.</span></span>

![Skipulagsmynd](media/dual-write-data-flow.png)

## <a name="templates"></a><span data-ttu-id="8222d-113">Sniðmát</span><span class="sxs-lookup"><span data-stu-id="8222d-113">Templates</span></span>

<span data-ttu-id="8222d-114">Einingakort yfir stigveldi fyrirtækis eru tiltæk fyrir samstillingu á einstefnu gagna úr forritum Finance and Operations til Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="8222d-114">Organization hierarchy entity maps are available for one-way synchronization of data from Finance and Operations apps to Common Data Service.</span></span>

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="internal-organization-hierarchy-purpose"></a><span data-ttu-id="8222d-115">Innri tilgangur í stigveldi fyrirtækja</span><span class="sxs-lookup"><span data-stu-id="8222d-115">Internal Organization Hierarchy Purpose</span></span>

<span data-ttu-id="8222d-116">Þetta sniðmát veitir aðra leiðina til samstillingar á tilgangseiningu fyrirtækjaskipulags úr Finance and Operations til annarra forrita Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="8222d-116">This template provides one-way synchronization of the Organization Hierarchy Purpose entity from Finance and Operations to other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-purpose.png) -->

<span data-ttu-id="8222d-117">Upprunasvæði</span><span class="sxs-lookup"><span data-stu-id="8222d-117">Source field</span></span> | <span data-ttu-id="8222d-118">Gerð vörpunar</span><span class="sxs-lookup"><span data-stu-id="8222d-118">Map type</span></span> | <span data-ttu-id="8222d-119">Áfangasvæði</span><span class="sxs-lookup"><span data-stu-id="8222d-119">Destination field</span></span>
---|---|---
<span data-ttu-id="8222d-120">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="8222d-120">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="8222d-121">msdyn\_hierarchypurposetypename</span><span class="sxs-lookup"><span data-stu-id="8222d-121">msdyn\_hierarchypurposetypename</span></span>
<span data-ttu-id="8222d-122">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="8222d-122">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="8222d-123">msdyn\_hierarchytype.msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="8222d-123">msdyn\_hierarchytype.msdyn\_name</span></span>
<span data-ttu-id="8222d-124">HIERARCHYPURPOSE</span><span class="sxs-lookup"><span data-stu-id="8222d-124">HIERARCHYPURPOSE</span></span> | \>\> | <span data-ttu-id="8222d-125">msdyn\_hierarchypurpose</span><span class="sxs-lookup"><span data-stu-id="8222d-125">msdyn\_hierarchypurpose</span></span>
<span data-ttu-id="8222d-126">IMMUTABLE</span><span class="sxs-lookup"><span data-stu-id="8222d-126">IMMUTABLE</span></span> | \>\> | <span data-ttu-id="8222d-127">msdyn\_immutable</span><span class="sxs-lookup"><span data-stu-id="8222d-127">msdyn\_immutable</span></span>
<span data-ttu-id="8222d-128">SETASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="8222d-128">SETASDEFAULT</span></span> | \>\> | <span data-ttu-id="8222d-129">msdyn\_setasdefault</span><span class="sxs-lookup"><span data-stu-id="8222d-129">msdyn\_setasdefault</span></span>

## <a name="internal-organization-hierarchy-type"></a><span data-ttu-id="8222d-130">Innri gerð fyrirtækisstigveldis</span><span class="sxs-lookup"><span data-stu-id="8222d-130">Internal Organization Hierarchy Type</span></span>

<span data-ttu-id="8222d-131">Þetta sniðmát veitir aðra leiðina til samstillingar á tilgangseiningu fyrirtækjaskipulags úr Finance and Operations til annarra forrita Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="8222d-131">Tihs template provides one-way synchronization of the Organization Hierarchy Type entity from Finance and Operations to other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-type.png) -->

<span data-ttu-id="8222d-132">Upprunasvæði</span><span class="sxs-lookup"><span data-stu-id="8222d-132">Source field</span></span> | <span data-ttu-id="8222d-133">Gerð vörpunar</span><span class="sxs-lookup"><span data-stu-id="8222d-133">Map type</span></span> | <span data-ttu-id="8222d-134">Áfangasvæði</span><span class="sxs-lookup"><span data-stu-id="8222d-134">Destination field</span></span>
---|---|---
<span data-ttu-id="8222d-135">HEITI</span><span class="sxs-lookup"><span data-stu-id="8222d-135">NAME</span></span> | \> | <span data-ttu-id="8222d-136">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="8222d-136">msdyn\_name</span></span>

## <a name="internal-organization-hierarchy"></a><span data-ttu-id="8222d-137">Innra fyrirtækisstigveldi</span><span class="sxs-lookup"><span data-stu-id="8222d-137">Internal Organization Hierarchy</span></span>

<span data-ttu-id="8222d-138">Þetta sniðmát veitir aðra leiðina til samstillingar á birtri einingu fyrirtækjaskipulags úr Finance and Operations til annarra forrita Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="8222d-138">This template provides one-way synchronization of the Organization Hierarchy Published entity from Finance and Operations to other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-organization.png) -->

<span data-ttu-id="8222d-139">Upprunasvæði</span><span class="sxs-lookup"><span data-stu-id="8222d-139">Source field</span></span> | <span data-ttu-id="8222d-140">Gerð vörpunar</span><span class="sxs-lookup"><span data-stu-id="8222d-140">Map type</span></span> | <span data-ttu-id="8222d-141">Áfangasvæði</span><span class="sxs-lookup"><span data-stu-id="8222d-141">Destination field</span></span>
---|---|---
<span data-ttu-id="8222d-142">VALIDTO</span><span class="sxs-lookup"><span data-stu-id="8222d-142">VALIDTO</span></span> | \> | <span data-ttu-id="8222d-143">msdyn\_validto</span><span class="sxs-lookup"><span data-stu-id="8222d-143">msdyn\_validto</span></span>
<span data-ttu-id="8222d-144">VALIDFROM</span><span class="sxs-lookup"><span data-stu-id="8222d-144">VALIDFROM</span></span> | \> | <span data-ttu-id="8222d-145">msdyn\_validfrom</span><span class="sxs-lookup"><span data-stu-id="8222d-145">msdyn\_validfrom</span></span>
<span data-ttu-id="8222d-146">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="8222d-146">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="8222d-147">msdyn\_hierarchytypename</span><span class="sxs-lookup"><span data-stu-id="8222d-147">msdyn\_hierarchytypename</span></span>
<span data-ttu-id="8222d-148">PARENTORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="8222d-148">PARENTORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="8222d-149">msdyn\_parentpartyid</span><span class="sxs-lookup"><span data-stu-id="8222d-149">msdyn\_parentpartyid</span></span>
<span data-ttu-id="8222d-150">CHILDORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="8222d-150">CHILDORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="8222d-151">msdyn\_childpartyid</span><span class="sxs-lookup"><span data-stu-id="8222d-151">msdyn\_childpartyid</span></span>
<span data-ttu-id="8222d-152">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="8222d-152">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="8222d-153">msdyn\_hierarchytypeid.msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="8222d-153">msdyn\_hierarchytypeid.msdyn\_name</span></span>
<span data-ttu-id="8222d-154">CHILDORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="8222d-154">CHILDORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="8222d-155">msdyn\_childid.msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="8222d-155">msdyn\_childid.msdyn\_partynumber</span></span>
<span data-ttu-id="8222d-156">PARENTORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="8222d-156">PARENTORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="8222d-157">msdyn\_parentid.msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="8222d-157">msdyn\_parentid.msdyn\_partynumber</span></span>

## <a name="internal-organization"></a><span data-ttu-id="8222d-158">Innra fyrirtæki</span><span class="sxs-lookup"><span data-stu-id="8222d-158">Internal Organization</span></span>

<span data-ttu-id="8222d-159">Upplýsingar um innra skipulag í Common Data Service koma úr tveimur einingum, **rekstrareiningu** og **lögaðilum**.</span><span class="sxs-lookup"><span data-stu-id="8222d-159">Internal organization information in Common Data Service comes from two entities, **operating unit** and **legal entities**.</span></span>

<!-- ![architecture image](media/dual-write-operating-unit.png) -->

<!-- ![architecture image](media/dual-write-legal-entities.png) -->

### <a name="operating-unit"></a><span data-ttu-id="8222d-160">Rekstrareining</span><span class="sxs-lookup"><span data-stu-id="8222d-160">Operating unit</span></span>

<span data-ttu-id="8222d-161">Upprunasvæði</span><span class="sxs-lookup"><span data-stu-id="8222d-161">Source field</span></span> | <span data-ttu-id="8222d-162">Gerð vörpunar</span><span class="sxs-lookup"><span data-stu-id="8222d-162">Map type</span></span> | <span data-ttu-id="8222d-163">Áfangasvæði</span><span class="sxs-lookup"><span data-stu-id="8222d-163">Destination field</span></span>
---|---|---
<span data-ttu-id="8222d-164">LANGUAGEID</span><span class="sxs-lookup"><span data-stu-id="8222d-164">LANGUAGEID</span></span> | \> | <span data-ttu-id="8222d-165">msdyn\_languageid</span><span class="sxs-lookup"><span data-stu-id="8222d-165">msdyn\_languageid</span></span>
<span data-ttu-id="8222d-166">NAMEALIAS</span><span class="sxs-lookup"><span data-stu-id="8222d-166">NAMEALIAS</span></span> | \> | <span data-ttu-id="8222d-167">msdyn\_namealias</span><span class="sxs-lookup"><span data-stu-id="8222d-167">msdyn\_namealias</span></span>
<span data-ttu-id="8222d-168">HEITI</span><span class="sxs-lookup"><span data-stu-id="8222d-168">NAME</span></span> | \> | <span data-ttu-id="8222d-169">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="8222d-169">msdyn\_name</span></span>
<span data-ttu-id="8222d-170">PARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="8222d-170">PARTYNUMBER</span></span> | \> | <span data-ttu-id="8222d-171">msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="8222d-171">msdyn\_partynumber</span></span>
<span data-ttu-id="8222d-172">OPERATINGUNITTYPE</span><span class="sxs-lookup"><span data-stu-id="8222d-172">OPERATINGUNITTYPE</span></span> | \>\> | <span data-ttu-id="8222d-173">msdyn\_type</span><span class="sxs-lookup"><span data-stu-id="8222d-173">msdyn\_type</span></span>

### <a name="legal-entity"></a><span data-ttu-id="8222d-174">Lögaðili</span><span class="sxs-lookup"><span data-stu-id="8222d-174">Legal entity</span></span>

<span data-ttu-id="8222d-175">Upprunasvæði</span><span class="sxs-lookup"><span data-stu-id="8222d-175">Source field</span></span> | <span data-ttu-id="8222d-176">Gerð vörpunar</span><span class="sxs-lookup"><span data-stu-id="8222d-176">Map type</span></span> | <span data-ttu-id="8222d-177">Áfangasvæði</span><span class="sxs-lookup"><span data-stu-id="8222d-177">Destination field</span></span>
---|---|---
<span data-ttu-id="8222d-178">NAMEALIAS</span><span class="sxs-lookup"><span data-stu-id="8222d-178">NAMEALIAS</span></span> | \> | <span data-ttu-id="8222d-179">msdyn\_namealias</span><span class="sxs-lookup"><span data-stu-id="8222d-179">msdyn\_namealias</span></span>
<span data-ttu-id="8222d-180">LANGUAGEID</span><span class="sxs-lookup"><span data-stu-id="8222d-180">LANGUAGEID</span></span> | \> | <span data-ttu-id="8222d-181">msdyn\_languageid</span><span class="sxs-lookup"><span data-stu-id="8222d-181">msdyn\_languageid</span></span>
<span data-ttu-id="8222d-182">HEITI</span><span class="sxs-lookup"><span data-stu-id="8222d-182">NAME</span></span> | \> | <span data-ttu-id="8222d-183">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="8222d-183">msdyn\_name</span></span>
<span data-ttu-id="8222d-184">PARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="8222d-184">PARTYNUMBER</span></span> | \> | <span data-ttu-id="8222d-185">msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="8222d-185">msdyn\_partynumber</span></span>
<span data-ttu-id="8222d-186">none</span><span class="sxs-lookup"><span data-stu-id="8222d-186">none</span></span> | \>\> | <span data-ttu-id="8222d-187">msdyn\_type</span><span class="sxs-lookup"><span data-stu-id="8222d-187">msdyn\_type</span></span>
<span data-ttu-id="8222d-188">LEGALENTITYID</span><span class="sxs-lookup"><span data-stu-id="8222d-188">LEGALENTITYID</span></span> | \> | <span data-ttu-id="8222d-189">msdyn\_companycode</span><span class="sxs-lookup"><span data-stu-id="8222d-189">msdyn\_companycode</span></span>

## <a name="company"></a><span data-ttu-id="8222d-190">Fyrirt.</span><span class="sxs-lookup"><span data-stu-id="8222d-190">Company</span></span>

<span data-ttu-id="8222d-191">Veitir tvíátta samstillingu upplýsinga um lögaðila (fyrirtæki) milli Finance and Operations og annarra forrita Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="8222d-191">Provides bidirectional synchronization of legal entity (company) information between Finance and Operations and other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-company.png) -->

<span data-ttu-id="8222d-192">Upprunasvæði</span><span class="sxs-lookup"><span data-stu-id="8222d-192">Source field</span></span> | <span data-ttu-id="8222d-193">Gerð vörpunar</span><span class="sxs-lookup"><span data-stu-id="8222d-193">Map type</span></span> | <span data-ttu-id="8222d-194">Áfangasvæði</span><span class="sxs-lookup"><span data-stu-id="8222d-194">Destination field</span></span>
---|---|---
<span data-ttu-id="8222d-195">HEITI</span><span class="sxs-lookup"><span data-stu-id="8222d-195">NAME</span></span> | = | <span data-ttu-id="8222d-196">cdm\_name</span><span class="sxs-lookup"><span data-stu-id="8222d-196">cdm\_name</span></span>
<span data-ttu-id="8222d-197">LEGALENTITYID</span><span class="sxs-lookup"><span data-stu-id="8222d-197">LEGALENTITYID</span></span> | = | <span data-ttu-id="8222d-198">cdm\_companycode</span><span class="sxs-lookup"><span data-stu-id="8222d-198">cdm\_companycode</span></span>
