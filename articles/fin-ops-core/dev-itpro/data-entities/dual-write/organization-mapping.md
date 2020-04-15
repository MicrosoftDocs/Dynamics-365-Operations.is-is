---
title: Stigveldi fyrirtækis í Common Data Service
description: Þetta efni lýsir samþættingu fyrirtækjaupplýsinga milli forrita Finance and Operations og Common Data Service.
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
ms.openlocfilehash: fc5db8d04a2860df0c917816e2910c6fbda941ff
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173155"
---
# <a name="organization-hierarchy-in-common-data-service"></a><span data-ttu-id="62c76-103">Stigveldi fyrirtækis í Common Data Service</span><span class="sxs-lookup"><span data-stu-id="62c76-103">Organization hierarchy in Common Data Service</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="62c76-104">Vegna þess að Dynamics 365 Finance er fjármálakerfi er *fyrirtæki* kjarnahugtak og kerfisuppsetning byrjar með stillingu fyrirtækisstigveldis.</span><span class="sxs-lookup"><span data-stu-id="62c76-104">Because Dynamics 365 Finance is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="62c76-105">Síðan er hægt að rekja fjárhag fyrirtækja á fyrirtækjastigi og einnig á hvaða stigi sem er í fyrirtækjastigveldinu.</span><span class="sxs-lookup"><span data-stu-id="62c76-105">Business financials can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="62c76-106">Þó að Common Data Service sé ekki með hugtak fyrirtækjastigveldis er það með nokkur laus hugtök, svo sem heildarsölutekjur.</span><span class="sxs-lookup"><span data-stu-id="62c76-106">Although Common Data Service doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="62c76-107">Sem hluti af samþættingu Common Data Service er gagnaskipulag stigveldis fyrirtækis er bætt við Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="62c76-107">As part of Common Data Service integration, the organization hierarchy data structure is added to Common Data Service.</span></span>

## <a name="data-flow"></a><span data-ttu-id="62c76-108">Gagnaflæði</span><span class="sxs-lookup"><span data-stu-id="62c76-108">Data flow</span></span>

<span data-ttu-id="62c76-109">Vistkerfi fyrirtækja sem samanstendur af forritum Finance and Operations og Common Data Service mun halda áfram að hafa stigveldi fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="62c76-109">A business ecosystem that consists of Finance and Operations apps and Common Data Service will continue to have an organization hierarchy.</span></span> <span data-ttu-id="62c76-110">Þetta stigveldi fyrirtækis er byggt á forritum Finance and Operations, en það er útsett í Common Data Service í upplýsinga- og stækkunarlegum tilgangi.</span><span class="sxs-lookup"><span data-stu-id="62c76-110">This organization hierarchy is built on Finance and Operations apps, but it's exposed in Common Data Service for informational and extensibility purposes.</span></span> <span data-ttu-id="62c76-111">Eftirfarandi mynd sýnir upplýsingar um stigveldi fyrirtækis sem birtast í Common Data Service sem einstefnugagnaflæði úr forritum Finance and Operations til Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="62c76-111">The following illustration shows the organization hierarchy information that is exposed in Common Data Service as a one-way data flow from Finance and Operations apps to Common Data Service.</span></span>

![Skipulagsmynd](media/dual-write-data-flow.png)

## <a name="templates"></a><span data-ttu-id="62c76-113">Sniðmát</span><span class="sxs-lookup"><span data-stu-id="62c76-113">Templates</span></span>

<span data-ttu-id="62c76-114">Einingakort yfir stigveldi fyrirtækis eru tiltæk fyrir samstillingu á einstefnu gagna úr forritum Finance and Operations til Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="62c76-114">Organization hierarchy entity maps are available for one-way synchronization of data from Finance and Operations apps to Common Data Service.</span></span>

## <a name="templates"></a><span data-ttu-id="62c76-115">Sniðmát</span><span class="sxs-lookup"><span data-stu-id="62c76-115">Templates</span></span>

<span data-ttu-id="62c76-116">Afurðarupplýsingar innihalda allar upplýsingar sem tengjast vörunni og skilgreiningu hennar, svo sem afurðarvíddir eða mælingar og geymsluvíddir.</span><span class="sxs-lookup"><span data-stu-id="62c76-116">Product information contains all the information related to the product and its definition, such as the product dimensions or the tracking and storage dimensions.</span></span> <span data-ttu-id="62c76-117">Eins og meðfylgjandi tafla sýnir, er safn af einingakortum búið til til að samstilla vörur og tengdar upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="62c76-117">As the following table shows, a collection of entity maps is created to sync products and related information.</span></span>

<span data-ttu-id="62c76-118">Finance and Operations-smáforrit</span><span class="sxs-lookup"><span data-stu-id="62c76-118">Finance and Operations apps</span></span> | <span data-ttu-id="62c76-119">Önnur Dynamics 365 forrit</span><span class="sxs-lookup"><span data-stu-id="62c76-119">Other Dynamics 365 apps</span></span> | <span data-ttu-id="62c76-120">lýsing</span><span class="sxs-lookup"><span data-stu-id="62c76-120">Description</span></span>
-----------------------|--------------------------------|---
<span data-ttu-id="62c76-121">Tilgangur fyrir stigveldi fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="62c76-121">Organization hierarchy purposes</span></span> | <span data-ttu-id="62c76-122">msdyn_internalorganizationhierarchypurposes</span><span class="sxs-lookup"><span data-stu-id="62c76-122">msdyn_internalorganizationhierarchypurposes</span></span> | <span data-ttu-id="62c76-123">Þetta sniðmát veitir samstillingu í eina átt á einingunni tilgangi fyrirtækjaskipulags.</span><span class="sxs-lookup"><span data-stu-id="62c76-123">This template provides one-way synchronization of the Organization Hierarchy Purpose entity.</span></span>
<span data-ttu-id="62c76-124">Gerð fyrirtækisstigveldis</span><span class="sxs-lookup"><span data-stu-id="62c76-124">Organization hierarchy type</span></span> | <span data-ttu-id="62c76-125">msdyn_internalorganizationhierarchytypes</span><span class="sxs-lookup"><span data-stu-id="62c76-125">msdyn_internalorganizationhierarchytypes</span></span> | <span data-ttu-id="62c76-126">Þetta sniðmát veitir samstillingu í eina átt á einingunni Gerð fyrirtækjaskipulags.</span><span class="sxs-lookup"><span data-stu-id="62c76-126">This template provides one-way synchronization of the Organization Hierarchy Type entity.</span></span>
<span data-ttu-id="62c76-127">Stigveldi fyrirtækis - útgefið</span><span class="sxs-lookup"><span data-stu-id="62c76-127">Organization hierarchy - published</span></span> | <span data-ttu-id="62c76-128">msdyn_internalorganizationhierarchies</span><span class="sxs-lookup"><span data-stu-id="62c76-128">msdyn_internalorganizationhierarchies</span></span> | <span data-ttu-id="62c76-129">Þetta sniðmát veitir samstillingu í eina átt á einingunni Útgefið fyrirtækjaskipulag.</span><span class="sxs-lookup"><span data-stu-id="62c76-129">This template provides one-way synchronization of the Organization Hierarchy Published entity.</span></span>
<span data-ttu-id="62c76-130">Rekstrareining</span><span class="sxs-lookup"><span data-stu-id="62c76-130">Operating unit</span></span> | <span data-ttu-id="62c76-131">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="62c76-131">msdyn_internalorganizations</span></span> | 
<span data-ttu-id="62c76-132">Lögaðilar</span><span class="sxs-lookup"><span data-stu-id="62c76-132">Legal entities</span></span> | <span data-ttu-id="62c76-133">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="62c76-133">msdyn_internalorganizations</span></span> | 
<span data-ttu-id="62c76-134">Lögaðilar</span><span class="sxs-lookup"><span data-stu-id="62c76-134">Legal entities</span></span> | <span data-ttu-id="62c76-135">cdm_companies</span><span class="sxs-lookup"><span data-stu-id="62c76-135">cdm_companies</span></span> | <span data-ttu-id="62c76-136">Veitir tvíátta samstillingu upplýsinga um lögaðila (fyrirtæki).</span><span class="sxs-lookup"><span data-stu-id="62c76-136">Provides bidirectional synchronization of legal entity (company) information.</span></span>


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Organization hierarchy purposes](includes/OrganizationHierarchyPurpose-msdyn-internalorganizationhierarchypurposes.md)]

[!include [Organization hierarchy type](includes/OrganizationHierarchyType-msdyn-internalorganizationhierarchytypes.md)]

[!include [Organization hierarchy - published](includes/OrganizationHierarchyPublished-msdyn-internalorganizationhierarchies.md)]

## <a name="internal-organization"></a><span data-ttu-id="62c76-137">Innra fyrirtæki</span><span class="sxs-lookup"><span data-stu-id="62c76-137">Internal Organization</span></span>

<span data-ttu-id="62c76-138">Upplýsingar um innra skipulag í Common Data Service koma úr tveimur einingum, **rekstrareiningu** og **lögaðilum**.</span><span class="sxs-lookup"><span data-stu-id="62c76-138">Internal organization information in Common Data Service comes from two entities, **operating unit** and **legal entities**.</span></span>

[!include [Operating unit](includes/OperatingUnit-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-Companies.md)]

