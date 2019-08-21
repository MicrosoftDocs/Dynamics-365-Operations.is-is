---
title: Stigveldi fyrirtækis í Common Data Service
description: Þetta efni lýsir samþættingu stigveldisgagna milli Finance and Operations og Common Data Service.
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
ms.openlocfilehash: ca2ac0f9dbb8544b12f23a271423a43b0e601272
ms.sourcegitcommit: 02c223b44ac7196df675afac61c6783f467d1983
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/24/2019
ms.locfileid: "1789203"
---
## <a name="organization-hierarchy-in-common-data-service"></a><span data-ttu-id="0a801-103">Stigveldi fyrirtækis í Common Data Service</span><span class="sxs-lookup"><span data-stu-id="0a801-103">Organization hierarchy in Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="0a801-104">Vegna þess að Microsoft Dynamics 365 for Finance and Operations er fjármálakerfi er *fyrirtæki* kjarnahugtak og kerfisuppsetning byrjar með stillingu fyrirtækisstigveldis.</span><span class="sxs-lookup"><span data-stu-id="0a801-104">Because Microsoft Dynamics 365 for Finance and Operations is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="0a801-105">Síðan er hægt að rekja fjárhag og rekstur fyrirtækja á fyrirtækjastigi og einnig á hvaða stigi sem er í fyrirtækjastigveldinu.</span><span class="sxs-lookup"><span data-stu-id="0a801-105">Business financials and operations can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="0a801-106">Þó að Common Data Service sé ekki með hugtak fyrirtækjastigveldis er það með nokkur laus hugtök, svo sem heildarsölutekjur.</span><span class="sxs-lookup"><span data-stu-id="0a801-106">Although Common Data Service doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="0a801-107">Sem hluti af samþættingu Common Data Service er gagnaskipulag stigveldis fyrirtækis er bætt við Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="0a801-107">As part of Common Data Service integration, the organization hierarchy data structure is added to Common Data Service.</span></span>

## <a name="data-flow"></a><span data-ttu-id="0a801-108">Gagnaflæði</span><span class="sxs-lookup"><span data-stu-id="0a801-108">Data flow</span></span>

<span data-ttu-id="0a801-109">Vistkerfi fyrirtækja sem samanstendur af Finance and Operations og Common Data Service mun halda áfram að hafa stigveldi fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="0a801-109">A business ecosystem that consists of Finance and Operations and Common Data Service will continue to have an organization hierarchy.</span></span> <span data-ttu-id="0a801-110">Þetta stigveldi fyrirtækis er byggt á Finance and Operations, en það er útsett í Common Data Service í upplýsinga- og stækkunarlegum tilgangi.</span><span class="sxs-lookup"><span data-stu-id="0a801-110">This organization hierarchy is built on Finance and Operations, but it's exposed in Common Data Service for informational and extensibility purposes.</span></span> <span data-ttu-id="0a801-111">Eftirfarandi mynd sýnir upplýsingar um stigveldi fyrirtækis sem birtast í Common Data Service sem einstefnugagnaflæði úr Finance and Operations til Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="0a801-111">The following illustration shows the organization hierarchy information that is exposed in Common Data Service as a one-way data flow from Finance and Operations to Common Data Service.</span></span>

![Skipulagsmynd](media/dual-write-data-flow.png)

## <a name="templates"></a><span data-ttu-id="0a801-113">Sniðmát</span><span class="sxs-lookup"><span data-stu-id="0a801-113">Templates</span></span>

<span data-ttu-id="0a801-114">Einingakort yfir stigveldi fyrirtækis eru tiltæk fyrir samstillingu á einstefnu gagna úr Finance and Operations til Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="0a801-114">Organization hierarchy entity maps are available for one-way synchronization of data from Finance and Operations to Common Data Service.</span></span>

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="internal-organization-hierarchy-purpose"></a><span data-ttu-id="0a801-115">Innri tilgangur í stigveldi fyrirtækja</span><span class="sxs-lookup"><span data-stu-id="0a801-115">Internal Organization Hierarchy Purpose</span></span>

<span data-ttu-id="0a801-116">Þetta sniðmát veitir aðra leiðina til samstillingar á tilgangseiningu fyrirtækjaskipulags úr Finance and Operations til Dynamics 365 fyrir Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="0a801-116">This template provides one-way synchronization of the Organization Hierarchy Purpose entity from Finance and Operations to Dynamics 365 for Customer Engagement.</span></span>

<!-- ![architecture image](media/dual-write-purpose.png) -->

<span data-ttu-id="0a801-117">Upprunasvæði</span><span class="sxs-lookup"><span data-stu-id="0a801-117">Source field</span></span> | <span data-ttu-id="0a801-118">Gerð vörpunar</span><span class="sxs-lookup"><span data-stu-id="0a801-118">Map type</span></span> | <span data-ttu-id="0a801-119">Áfangasvæði</span><span class="sxs-lookup"><span data-stu-id="0a801-119">Destination field</span></span>
---|---|---
<span data-ttu-id="0a801-120">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="0a801-120">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="0a801-121">msdyn\_hierarchypurposetypename</span><span class="sxs-lookup"><span data-stu-id="0a801-121">msdyn\_hierarchypurposetypename</span></span>
<span data-ttu-id="0a801-122">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="0a801-122">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="0a801-123">msdyn\_hierarchytype.msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="0a801-123">msdyn\_hierarchytype.msdyn\_name</span></span>
<span data-ttu-id="0a801-124">HIERARCHYPURPOSE</span><span class="sxs-lookup"><span data-stu-id="0a801-124">HIERARCHYPURPOSE</span></span> | \>\> | <span data-ttu-id="0a801-125">msdyn\_hierarchypurpose</span><span class="sxs-lookup"><span data-stu-id="0a801-125">msdyn\_hierarchypurpose</span></span>
<span data-ttu-id="0a801-126">IMMUTABLE</span><span class="sxs-lookup"><span data-stu-id="0a801-126">IMMUTABLE</span></span> | \>\> | <span data-ttu-id="0a801-127">msdyn\_immutable</span><span class="sxs-lookup"><span data-stu-id="0a801-127">msdyn\_immutable</span></span>
<span data-ttu-id="0a801-128">SETASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="0a801-128">SETASDEFAULT</span></span> | \>\> | <span data-ttu-id="0a801-129">msdyn\_setasdefault</span><span class="sxs-lookup"><span data-stu-id="0a801-129">msdyn\_setasdefault</span></span>

## <a name="internal-organization-hierarchy-type"></a><span data-ttu-id="0a801-130">Innri gerð fyrirtækisstigveldis</span><span class="sxs-lookup"><span data-stu-id="0a801-130">Internal Organization Hierarchy Type</span></span>

<span data-ttu-id="0a801-131">Þetta sniðmát veitir aðra leiðina til samstillingar á gerðareiningu fyrirtækjaskipulags úr Finance and Operations til Dynamics 365 fyrir Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="0a801-131">Tihs template provides one-way synchronization of the Organization Hierarchy Type entity from Finance and Operations to Customer Engagement.</span></span>

<!-- ![architecture image](media/dual-write-type.png) -->

<span data-ttu-id="0a801-132">Upprunasvæði</span><span class="sxs-lookup"><span data-stu-id="0a801-132">Source field</span></span> | <span data-ttu-id="0a801-133">Gerð vörpunar</span><span class="sxs-lookup"><span data-stu-id="0a801-133">Map type</span></span> | <span data-ttu-id="0a801-134">Áfangasvæði</span><span class="sxs-lookup"><span data-stu-id="0a801-134">Destination field</span></span>
---|---|---
<span data-ttu-id="0a801-135">HEITI</span><span class="sxs-lookup"><span data-stu-id="0a801-135">NAME</span></span> | \> | <span data-ttu-id="0a801-136">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="0a801-136">msdyn\_name</span></span>

## <a name="internal-organization-hierarchy"></a><span data-ttu-id="0a801-137">Innra fyrirtækisstigveldi</span><span class="sxs-lookup"><span data-stu-id="0a801-137">Internal Organization Hierarchy</span></span>

<span data-ttu-id="0a801-138">Þetta sniðmát veitir aðra leiðina til samstillingar á útgefna einingu fyrirtækjaskipulags úr Finance and Operations til Dynamics 365 fyrir Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="0a801-138">This template provides one-way synchronization of the Organization Hierarchy Published entity from Finance and Operations to Customer Engagement.</span></span>

<!-- ![architecture image](media/dual-write-organization.png) -->

<span data-ttu-id="0a801-139">Upprunasvæði</span><span class="sxs-lookup"><span data-stu-id="0a801-139">Source field</span></span> | <span data-ttu-id="0a801-140">Gerð vörpunar</span><span class="sxs-lookup"><span data-stu-id="0a801-140">Map type</span></span> | <span data-ttu-id="0a801-141">Áfangasvæði</span><span class="sxs-lookup"><span data-stu-id="0a801-141">Destination field</span></span>
---|---|---
<span data-ttu-id="0a801-142">VALIDTO</span><span class="sxs-lookup"><span data-stu-id="0a801-142">VALIDTO</span></span> | \> | <span data-ttu-id="0a801-143">msdyn\_validto</span><span class="sxs-lookup"><span data-stu-id="0a801-143">msdyn\_validto</span></span>
<span data-ttu-id="0a801-144">VALIDFROM</span><span class="sxs-lookup"><span data-stu-id="0a801-144">VALIDFROM</span></span> | \> | <span data-ttu-id="0a801-145">msdyn\_validfrom</span><span class="sxs-lookup"><span data-stu-id="0a801-145">msdyn\_validfrom</span></span>
<span data-ttu-id="0a801-146">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="0a801-146">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="0a801-147">msdyn\_hierarchytypename</span><span class="sxs-lookup"><span data-stu-id="0a801-147">msdyn\_hierarchytypename</span></span>
<span data-ttu-id="0a801-148">PARENTORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="0a801-148">PARENTORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="0a801-149">msdyn\_parentpartyid</span><span class="sxs-lookup"><span data-stu-id="0a801-149">msdyn\_parentpartyid</span></span>
<span data-ttu-id="0a801-150">CHILDORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="0a801-150">CHILDORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="0a801-151">msdyn\_childpartyid</span><span class="sxs-lookup"><span data-stu-id="0a801-151">msdyn\_childpartyid</span></span>
<span data-ttu-id="0a801-152">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="0a801-152">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="0a801-153">msdyn\_hierarchytypeid.msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="0a801-153">msdyn\_hierarchytypeid.msdyn\_name</span></span>
<span data-ttu-id="0a801-154">CHILDORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="0a801-154">CHILDORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="0a801-155">msdyn\_childid.msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="0a801-155">msdyn\_childid.msdyn\_partynumber</span></span>
<span data-ttu-id="0a801-156">PARENTORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="0a801-156">PARENTORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="0a801-157">msdyn\_parentid.msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="0a801-157">msdyn\_parentid.msdyn\_partynumber</span></span>

## <a name="internal-organization"></a><span data-ttu-id="0a801-158">Innra fyrirtæki</span><span class="sxs-lookup"><span data-stu-id="0a801-158">Internal Organization</span></span>

<span data-ttu-id="0a801-159">Upplýsingar um innra skipulag í Common Data Service kemur úr tveimur einingum Finance and Operations, **rekstrareining** og **lögaðilar**.</span><span class="sxs-lookup"><span data-stu-id="0a801-159">Internal organization information in Common Data Service comes from two Finance and Operations entities, **operating unit** and **legal entities**.</span></span>

<!-- ![architecture image](media/dual-write-operating-unit.png) -->

<!-- ![architecture image](media/dual-write-legal-entities.png) -->

### <a name="operating-unit"></a><span data-ttu-id="0a801-160">Rekstrareining</span><span class="sxs-lookup"><span data-stu-id="0a801-160">Operating unit</span></span>

<span data-ttu-id="0a801-161">Upprunasvæði</span><span class="sxs-lookup"><span data-stu-id="0a801-161">Source field</span></span> | <span data-ttu-id="0a801-162">Gerð vörpunar</span><span class="sxs-lookup"><span data-stu-id="0a801-162">Map type</span></span> | <span data-ttu-id="0a801-163">Áfangasvæði</span><span class="sxs-lookup"><span data-stu-id="0a801-163">Destination field</span></span>
---|---|---
<span data-ttu-id="0a801-164">LANGUAGEID</span><span class="sxs-lookup"><span data-stu-id="0a801-164">LANGUAGEID</span></span> | \> | <span data-ttu-id="0a801-165">msdyn\_languageid</span><span class="sxs-lookup"><span data-stu-id="0a801-165">msdyn\_languageid</span></span>
<span data-ttu-id="0a801-166">NAMEALIAS</span><span class="sxs-lookup"><span data-stu-id="0a801-166">NAMEALIAS</span></span> | \> | <span data-ttu-id="0a801-167">msdyn\_namealias</span><span class="sxs-lookup"><span data-stu-id="0a801-167">msdyn\_namealias</span></span>
<span data-ttu-id="0a801-168">HEITI</span><span class="sxs-lookup"><span data-stu-id="0a801-168">NAME</span></span> | \> | <span data-ttu-id="0a801-169">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="0a801-169">msdyn\_name</span></span>
<span data-ttu-id="0a801-170">PARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="0a801-170">PARTYNUMBER</span></span> | \> | <span data-ttu-id="0a801-171">msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="0a801-171">msdyn\_partynumber</span></span>
<span data-ttu-id="0a801-172">OPERATINGUNITTYPE</span><span class="sxs-lookup"><span data-stu-id="0a801-172">OPERATINGUNITTYPE</span></span> | \>\> | <span data-ttu-id="0a801-173">msdyn\_type</span><span class="sxs-lookup"><span data-stu-id="0a801-173">msdyn\_type</span></span>

### <a name="legal-entity"></a><span data-ttu-id="0a801-174">Lögaðili</span><span class="sxs-lookup"><span data-stu-id="0a801-174">Legal entity</span></span>

<span data-ttu-id="0a801-175">Upprunasvæði</span><span class="sxs-lookup"><span data-stu-id="0a801-175">Source field</span></span> | <span data-ttu-id="0a801-176">Gerð vörpunar</span><span class="sxs-lookup"><span data-stu-id="0a801-176">Map type</span></span> | <span data-ttu-id="0a801-177">Áfangasvæði</span><span class="sxs-lookup"><span data-stu-id="0a801-177">Destination field</span></span>
---|---|---
<span data-ttu-id="0a801-178">NAMEALIAS</span><span class="sxs-lookup"><span data-stu-id="0a801-178">NAMEALIAS</span></span> | \> | <span data-ttu-id="0a801-179">msdyn\_namealias</span><span class="sxs-lookup"><span data-stu-id="0a801-179">msdyn\_namealias</span></span>
<span data-ttu-id="0a801-180">LANGUAGEID</span><span class="sxs-lookup"><span data-stu-id="0a801-180">LANGUAGEID</span></span> | \> | <span data-ttu-id="0a801-181">msdyn\_languageid</span><span class="sxs-lookup"><span data-stu-id="0a801-181">msdyn\_languageid</span></span>
<span data-ttu-id="0a801-182">HEITI</span><span class="sxs-lookup"><span data-stu-id="0a801-182">NAME</span></span> | \> | <span data-ttu-id="0a801-183">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="0a801-183">msdyn\_name</span></span>
<span data-ttu-id="0a801-184">PARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="0a801-184">PARTYNUMBER</span></span> | \> | <span data-ttu-id="0a801-185">msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="0a801-185">msdyn\_partynumber</span></span>
<span data-ttu-id="0a801-186">none</span><span class="sxs-lookup"><span data-stu-id="0a801-186">none</span></span> | \>\> | <span data-ttu-id="0a801-187">msdyn\_type</span><span class="sxs-lookup"><span data-stu-id="0a801-187">msdyn\_type</span></span>
<span data-ttu-id="0a801-188">LEGALENTITYID</span><span class="sxs-lookup"><span data-stu-id="0a801-188">LEGALENTITYID</span></span> | \> | <span data-ttu-id="0a801-189">msdyn\_companycode</span><span class="sxs-lookup"><span data-stu-id="0a801-189">msdyn\_companycode</span></span>

## <a name="company"></a><span data-ttu-id="0a801-190">Fyrirt.  </span><span class="sxs-lookup"><span data-stu-id="0a801-190">Company</span></span>

<span data-ttu-id="0a801-191">Veitir tvíátta samstillingu upplýsinga um lögaðila (fyrirtæki) milli Finance and Operations og Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="0a801-191">Provides bidirectional synchronization of legal entity (company) information between Finance and Operations and Customer Engagement.</span></span>

<!-- ![architecture image](media/dual-write-company.png) -->

<span data-ttu-id="0a801-192">Upprunasvæði</span><span class="sxs-lookup"><span data-stu-id="0a801-192">Source field</span></span> | <span data-ttu-id="0a801-193">Gerð vörpunar</span><span class="sxs-lookup"><span data-stu-id="0a801-193">Map type</span></span> | <span data-ttu-id="0a801-194">Áfangasvæði</span><span class="sxs-lookup"><span data-stu-id="0a801-194">Destination field</span></span>
---|---|---
<span data-ttu-id="0a801-195">HEITI</span><span class="sxs-lookup"><span data-stu-id="0a801-195">NAME</span></span> | = | <span data-ttu-id="0a801-196">cdm\_name</span><span class="sxs-lookup"><span data-stu-id="0a801-196">cdm\_name</span></span>
<span data-ttu-id="0a801-197">LEGALENTITYID</span><span class="sxs-lookup"><span data-stu-id="0a801-197">LEGALENTITYID</span></span> | = | <span data-ttu-id="0a801-198">cdm\_companycode</span><span class="sxs-lookup"><span data-stu-id="0a801-198">cdm\_companycode</span></span>
