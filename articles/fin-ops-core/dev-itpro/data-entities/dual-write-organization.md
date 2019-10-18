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
ms.openlocfilehash: fd159b38f69305dcaecb364ba0ccb3befabb3582
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182026"
---
## <a name="organization-hierarchy-in-common-data-service"></a><span data-ttu-id="d75b3-103">Stigveldi fyrirtækis í Common Data Service</span><span class="sxs-lookup"><span data-stu-id="d75b3-103">Organization hierarchy in Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="d75b3-104">Vegna þess að Dynamics 365 Finance er fjármálakerfi er *fyrirtæki* kjarnahugtak og kerfisuppsetning byrjar með stillingu fyrirtækisstigveldis.</span><span class="sxs-lookup"><span data-stu-id="d75b3-104">Because Dynamics 365 Finance is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="d75b3-105">Síðan er hægt að rekja fjárhag fyrirtækja á fyrirtækjastigi og einnig á hvaða stigi sem er í fyrirtækjastigveldinu.</span><span class="sxs-lookup"><span data-stu-id="d75b3-105">Business financials can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="d75b3-106">Þó að Common Data Service sé ekki með hugtak fyrirtækjastigveldis er það með nokkur laus hugtök, svo sem heildarsölutekjur.</span><span class="sxs-lookup"><span data-stu-id="d75b3-106">Although Common Data Service doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="d75b3-107">Sem hluti af samþættingu Common Data Service er gagnaskipulag stigveldis fyrirtækis er bætt við Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="d75b3-107">As part of Common Data Service integration, the organization hierarchy data structure is added to Common Data Service.</span></span>

## <a name="data-flow"></a><span data-ttu-id="d75b3-108">Gagnaflæði</span><span class="sxs-lookup"><span data-stu-id="d75b3-108">Data flow</span></span>

<span data-ttu-id="d75b3-109">Vistkerfi fyrirtækja sem samanstendur af forritum Finance and Operations og Common Data Service mun halda áfram að hafa stigveldi fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="d75b3-109">A business ecosystem that consists of Finance and Operations apps and Common Data Service will continue to have an organization hierarchy.</span></span> <span data-ttu-id="d75b3-110">Þetta stigveldi fyrirtækis er byggt á forritum Finance and Operations, en það er útsett í Common Data Service í upplýsinga- og stækkunarlegum tilgangi.</span><span class="sxs-lookup"><span data-stu-id="d75b3-110">This organization hierarchy is built on Finance and Operations apps, but it's exposed in Common Data Service for informational and extensibility purposes.</span></span> <span data-ttu-id="d75b3-111">Eftirfarandi mynd sýnir upplýsingar um stigveldi fyrirtækis sem birtast í Common Data Service sem einstefnugagnaflæði úr forritum Finance and Operations til Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="d75b3-111">The following illustration shows the organization hierarchy information that is exposed in Common Data Service as a one-way data flow from Finance and Operations apps to Common Data Service.</span></span>

![Skipulagsmynd](media/dual-write-data-flow.png)

## <a name="templates"></a><span data-ttu-id="d75b3-113">Sniðmát</span><span class="sxs-lookup"><span data-stu-id="d75b3-113">Templates</span></span>

<span data-ttu-id="d75b3-114">Einingakort yfir stigveldi fyrirtækis eru tiltæk fyrir samstillingu á einstefnu gagna úr forritum Finance and Operations til Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="d75b3-114">Organization hierarchy entity maps are available for one-way synchronization of data from Finance and Operations apps to Common Data Service.</span></span>

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="internal-organization-hierarchy-purpose"></a><span data-ttu-id="d75b3-115">Innri tilgangur í stigveldi fyrirtækja</span><span class="sxs-lookup"><span data-stu-id="d75b3-115">Internal Organization Hierarchy Purpose</span></span>

<span data-ttu-id="d75b3-116">Þetta sniðmát veitir aðra leiðina til samstillingar á tilgangseiningu fyrirtækjaskipulags úr Finance and Operations til annarra forrita Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="d75b3-116">This template provides one-way synchronization of the Organization Hierarchy Purpose entity from Finance and Operations to other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-purpose.png) -->

<span data-ttu-id="d75b3-117">Upprunasvæði</span><span class="sxs-lookup"><span data-stu-id="d75b3-117">Source field</span></span> | <span data-ttu-id="d75b3-118">Gerð vörpunar</span><span class="sxs-lookup"><span data-stu-id="d75b3-118">Map type</span></span> | <span data-ttu-id="d75b3-119">Áfangasvæði</span><span class="sxs-lookup"><span data-stu-id="d75b3-119">Destination field</span></span>
---|---|---
<span data-ttu-id="d75b3-120">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="d75b3-120">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="d75b3-121">msdyn\_hierarchypurposetypename</span><span class="sxs-lookup"><span data-stu-id="d75b3-121">msdyn\_hierarchypurposetypename</span></span>
<span data-ttu-id="d75b3-122">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="d75b3-122">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="d75b3-123">msdyn\_hierarchytype.msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="d75b3-123">msdyn\_hierarchytype.msdyn\_name</span></span>
<span data-ttu-id="d75b3-124">HIERARCHYPURPOSE</span><span class="sxs-lookup"><span data-stu-id="d75b3-124">HIERARCHYPURPOSE</span></span> | \>\> | <span data-ttu-id="d75b3-125">msdyn\_hierarchypurpose</span><span class="sxs-lookup"><span data-stu-id="d75b3-125">msdyn\_hierarchypurpose</span></span>
<span data-ttu-id="d75b3-126">IMMUTABLE</span><span class="sxs-lookup"><span data-stu-id="d75b3-126">IMMUTABLE</span></span> | \>\> | <span data-ttu-id="d75b3-127">msdyn\_immutable</span><span class="sxs-lookup"><span data-stu-id="d75b3-127">msdyn\_immutable</span></span>
<span data-ttu-id="d75b3-128">SETASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="d75b3-128">SETASDEFAULT</span></span> | \>\> | <span data-ttu-id="d75b3-129">msdyn\_setasdefault</span><span class="sxs-lookup"><span data-stu-id="d75b3-129">msdyn\_setasdefault</span></span>

## <a name="internal-organization-hierarchy-type"></a><span data-ttu-id="d75b3-130">Innri gerð fyrirtækisstigveldis</span><span class="sxs-lookup"><span data-stu-id="d75b3-130">Internal Organization Hierarchy Type</span></span>

<span data-ttu-id="d75b3-131">Þetta sniðmát veitir aðra leiðina til samstillingar á tilgangseiningu fyrirtækjaskipulags úr Finance and Operations til annarra forrita Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="d75b3-131">Tihs template provides one-way synchronization of the Organization Hierarchy Type entity from Finance and Operations to other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-type.png) -->

<span data-ttu-id="d75b3-132">Upprunasvæði</span><span class="sxs-lookup"><span data-stu-id="d75b3-132">Source field</span></span> | <span data-ttu-id="d75b3-133">Gerð vörpunar</span><span class="sxs-lookup"><span data-stu-id="d75b3-133">Map type</span></span> | <span data-ttu-id="d75b3-134">Áfangasvæði</span><span class="sxs-lookup"><span data-stu-id="d75b3-134">Destination field</span></span>
---|---|---
<span data-ttu-id="d75b3-135">HEITI</span><span class="sxs-lookup"><span data-stu-id="d75b3-135">NAME</span></span> | \> | <span data-ttu-id="d75b3-136">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="d75b3-136">msdyn\_name</span></span>

## <a name="internal-organization-hierarchy"></a><span data-ttu-id="d75b3-137">Innra fyrirtækisstigveldi</span><span class="sxs-lookup"><span data-stu-id="d75b3-137">Internal Organization Hierarchy</span></span>

<span data-ttu-id="d75b3-138">Þetta sniðmát veitir aðra leiðina til samstillingar á birtri einingu fyrirtækjaskipulags úr Finance and Operations til annarra forrita Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="d75b3-138">This template provides one-way synchronization of the Organization Hierarchy Published entity from Finance and Operations to other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-organization.png) -->

<span data-ttu-id="d75b3-139">Upprunasvæði</span><span class="sxs-lookup"><span data-stu-id="d75b3-139">Source field</span></span> | <span data-ttu-id="d75b3-140">Gerð vörpunar</span><span class="sxs-lookup"><span data-stu-id="d75b3-140">Map type</span></span> | <span data-ttu-id="d75b3-141">Áfangasvæði</span><span class="sxs-lookup"><span data-stu-id="d75b3-141">Destination field</span></span>
---|---|---
<span data-ttu-id="d75b3-142">VALIDTO</span><span class="sxs-lookup"><span data-stu-id="d75b3-142">VALIDTO</span></span> | \> | <span data-ttu-id="d75b3-143">msdyn\_validto</span><span class="sxs-lookup"><span data-stu-id="d75b3-143">msdyn\_validto</span></span>
<span data-ttu-id="d75b3-144">VALIDFROM</span><span class="sxs-lookup"><span data-stu-id="d75b3-144">VALIDFROM</span></span> | \> | <span data-ttu-id="d75b3-145">msdyn\_validfrom</span><span class="sxs-lookup"><span data-stu-id="d75b3-145">msdyn\_validfrom</span></span>
<span data-ttu-id="d75b3-146">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="d75b3-146">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="d75b3-147">msdyn\_hierarchytypename</span><span class="sxs-lookup"><span data-stu-id="d75b3-147">msdyn\_hierarchytypename</span></span>
<span data-ttu-id="d75b3-148">PARENTORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="d75b3-148">PARENTORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="d75b3-149">msdyn\_parentpartyid</span><span class="sxs-lookup"><span data-stu-id="d75b3-149">msdyn\_parentpartyid</span></span>
<span data-ttu-id="d75b3-150">CHILDORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="d75b3-150">CHILDORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="d75b3-151">msdyn\_childpartyid</span><span class="sxs-lookup"><span data-stu-id="d75b3-151">msdyn\_childpartyid</span></span>
<span data-ttu-id="d75b3-152">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="d75b3-152">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="d75b3-153">msdyn\_hierarchytypeid.msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="d75b3-153">msdyn\_hierarchytypeid.msdyn\_name</span></span>
<span data-ttu-id="d75b3-154">CHILDORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="d75b3-154">CHILDORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="d75b3-155">msdyn\_childid.msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="d75b3-155">msdyn\_childid.msdyn\_partynumber</span></span>
<span data-ttu-id="d75b3-156">PARENTORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="d75b3-156">PARENTORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="d75b3-157">msdyn\_parentid.msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="d75b3-157">msdyn\_parentid.msdyn\_partynumber</span></span>

## <a name="internal-organization"></a><span data-ttu-id="d75b3-158">Innra fyrirtæki</span><span class="sxs-lookup"><span data-stu-id="d75b3-158">Internal Organization</span></span>

<span data-ttu-id="d75b3-159">Upplýsingar um innra skipulag í Common Data Service koma úr tveimur einingum, **rekstrareiningu** og **lögaðilum**.</span><span class="sxs-lookup"><span data-stu-id="d75b3-159">Internal organization information in Common Data Service comes from two entities, **operating unit** and **legal entities**.</span></span>

<!-- ![architecture image](media/dual-write-operating-unit.png) -->

<!-- ![architecture image](media/dual-write-legal-entities.png) -->

### <a name="operating-unit"></a><span data-ttu-id="d75b3-160">Rekstrareining</span><span class="sxs-lookup"><span data-stu-id="d75b3-160">Operating unit</span></span>

<span data-ttu-id="d75b3-161">Upprunasvæði</span><span class="sxs-lookup"><span data-stu-id="d75b3-161">Source field</span></span> | <span data-ttu-id="d75b3-162">Gerð vörpunar</span><span class="sxs-lookup"><span data-stu-id="d75b3-162">Map type</span></span> | <span data-ttu-id="d75b3-163">Áfangasvæði</span><span class="sxs-lookup"><span data-stu-id="d75b3-163">Destination field</span></span>
---|---|---
<span data-ttu-id="d75b3-164">LANGUAGEID</span><span class="sxs-lookup"><span data-stu-id="d75b3-164">LANGUAGEID</span></span> | \> | <span data-ttu-id="d75b3-165">msdyn\_languageid</span><span class="sxs-lookup"><span data-stu-id="d75b3-165">msdyn\_languageid</span></span>
<span data-ttu-id="d75b3-166">NAMEALIAS</span><span class="sxs-lookup"><span data-stu-id="d75b3-166">NAMEALIAS</span></span> | \> | <span data-ttu-id="d75b3-167">msdyn\_namealias</span><span class="sxs-lookup"><span data-stu-id="d75b3-167">msdyn\_namealias</span></span>
<span data-ttu-id="d75b3-168">HEITI</span><span class="sxs-lookup"><span data-stu-id="d75b3-168">NAME</span></span> | \> | <span data-ttu-id="d75b3-169">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="d75b3-169">msdyn\_name</span></span>
<span data-ttu-id="d75b3-170">PARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="d75b3-170">PARTYNUMBER</span></span> | \> | <span data-ttu-id="d75b3-171">msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="d75b3-171">msdyn\_partynumber</span></span>
<span data-ttu-id="d75b3-172">OPERATINGUNITTYPE</span><span class="sxs-lookup"><span data-stu-id="d75b3-172">OPERATINGUNITTYPE</span></span> | \>\> | <span data-ttu-id="d75b3-173">msdyn\_type</span><span class="sxs-lookup"><span data-stu-id="d75b3-173">msdyn\_type</span></span>

### <a name="legal-entity"></a><span data-ttu-id="d75b3-174">Lögaðili</span><span class="sxs-lookup"><span data-stu-id="d75b3-174">Legal entity</span></span>

<span data-ttu-id="d75b3-175">Upprunasvæði</span><span class="sxs-lookup"><span data-stu-id="d75b3-175">Source field</span></span> | <span data-ttu-id="d75b3-176">Gerð vörpunar</span><span class="sxs-lookup"><span data-stu-id="d75b3-176">Map type</span></span> | <span data-ttu-id="d75b3-177">Áfangasvæði</span><span class="sxs-lookup"><span data-stu-id="d75b3-177">Destination field</span></span>
---|---|---
<span data-ttu-id="d75b3-178">NAMEALIAS</span><span class="sxs-lookup"><span data-stu-id="d75b3-178">NAMEALIAS</span></span> | \> | <span data-ttu-id="d75b3-179">msdyn\_namealias</span><span class="sxs-lookup"><span data-stu-id="d75b3-179">msdyn\_namealias</span></span>
<span data-ttu-id="d75b3-180">LANGUAGEID</span><span class="sxs-lookup"><span data-stu-id="d75b3-180">LANGUAGEID</span></span> | \> | <span data-ttu-id="d75b3-181">msdyn\_languageid</span><span class="sxs-lookup"><span data-stu-id="d75b3-181">msdyn\_languageid</span></span>
<span data-ttu-id="d75b3-182">HEITI</span><span class="sxs-lookup"><span data-stu-id="d75b3-182">NAME</span></span> | \> | <span data-ttu-id="d75b3-183">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="d75b3-183">msdyn\_name</span></span>
<span data-ttu-id="d75b3-184">PARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="d75b3-184">PARTYNUMBER</span></span> | \> | <span data-ttu-id="d75b3-185">msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="d75b3-185">msdyn\_partynumber</span></span>
<span data-ttu-id="d75b3-186">none</span><span class="sxs-lookup"><span data-stu-id="d75b3-186">none</span></span> | \>\> | <span data-ttu-id="d75b3-187">msdyn\_type</span><span class="sxs-lookup"><span data-stu-id="d75b3-187">msdyn\_type</span></span>
<span data-ttu-id="d75b3-188">LEGALENTITYID</span><span class="sxs-lookup"><span data-stu-id="d75b3-188">LEGALENTITYID</span></span> | \> | <span data-ttu-id="d75b3-189">msdyn\_companycode</span><span class="sxs-lookup"><span data-stu-id="d75b3-189">msdyn\_companycode</span></span>

## <a name="company"></a><span data-ttu-id="d75b3-190">Fyrirt.</span><span class="sxs-lookup"><span data-stu-id="d75b3-190">Company</span></span>

<span data-ttu-id="d75b3-191">Veitir tvíátta samstillingu upplýsinga um lögaðila (fyrirtæki) milli Finance and Operations og annarra forrita Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="d75b3-191">Provides bidirectional synchronization of legal entity (company) information between Finance and Operations and other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-company.png) -->

<span data-ttu-id="d75b3-192">Upprunasvæði</span><span class="sxs-lookup"><span data-stu-id="d75b3-192">Source field</span></span> | <span data-ttu-id="d75b3-193">Gerð vörpunar</span><span class="sxs-lookup"><span data-stu-id="d75b3-193">Map type</span></span> | <span data-ttu-id="d75b3-194">Áfangasvæði</span><span class="sxs-lookup"><span data-stu-id="d75b3-194">Destination field</span></span>
---|---|---
<span data-ttu-id="d75b3-195">HEITI</span><span class="sxs-lookup"><span data-stu-id="d75b3-195">NAME</span></span> | = | <span data-ttu-id="d75b3-196">cdm\_name</span><span class="sxs-lookup"><span data-stu-id="d75b3-196">cdm\_name</span></span>
<span data-ttu-id="d75b3-197">LEGALENTITYID</span><span class="sxs-lookup"><span data-stu-id="d75b3-197">LEGALENTITYID</span></span> | = | <span data-ttu-id="d75b3-198">cdm\_companycode</span><span class="sxs-lookup"><span data-stu-id="d75b3-198">cdm\_companycode</span></span>
