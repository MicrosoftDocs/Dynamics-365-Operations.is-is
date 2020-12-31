---
title: Stigveldi fyrirtækis í Dataverse
description: Þetta efni lýsir samþættingu fyrirtækjaupplýsinga milli forrita Finance and Operations og Dataverse.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: e2b652f11db62eb58ffc2ec2fc4322149e7d45d1
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680073"
---
# <a name="organization-hierarchy-in-dataverse"></a><span data-ttu-id="93c33-103">Stigveldi fyrirtækis í Dataverse</span><span class="sxs-lookup"><span data-stu-id="93c33-103">Organization hierarchy in Dataverse</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="93c33-104">Vegna þess að Dynamics 365 Finance er fjármálakerfi er *fyrirtæki* kjarnahugtak og kerfisuppsetning byrjar með stillingu fyrirtækisstigveldis.</span><span class="sxs-lookup"><span data-stu-id="93c33-104">Because Dynamics 365 Finance is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="93c33-105">Síðan er hægt að rekja fjárhag fyrirtækja á fyrirtækjastigi og einnig á hvaða stigi sem er í fyrirtækjastigveldinu.</span><span class="sxs-lookup"><span data-stu-id="93c33-105">Business financials can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="93c33-106">Þó að Dataverse sé ekki með hugtak fyrirtækjastigveldis er það með nokkur laus hugtök, svo sem heildarsölutekjur.</span><span class="sxs-lookup"><span data-stu-id="93c33-106">Although Dataverse doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="93c33-107">Sem hluti af samþættingu Dataverse er gagnaskipulag stigveldis fyrirtækis er bætt við Dataverse.</span><span class="sxs-lookup"><span data-stu-id="93c33-107">As part of Dataverse integration, the organization hierarchy data structure is added to Dataverse.</span></span>

## <a name="data-flow"></a><span data-ttu-id="93c33-108">Gagnaflæði</span><span class="sxs-lookup"><span data-stu-id="93c33-108">Data flow</span></span>

<span data-ttu-id="93c33-109">Vistkerfi fyrirtækja sem samanstendur af forritum Finance and Operations og Dataverse mun halda áfram að hafa stigveldi fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="93c33-109">A business ecosystem that consists of Finance and Operations apps and Dataverse will continue to have an organization hierarchy.</span></span> <span data-ttu-id="93c33-110">Þetta stigveldi fyrirtækis er byggt á forritum Finance and Operations, en það er útsett í Dataverse í upplýsinga- og stækkunarlegum tilgangi.</span><span class="sxs-lookup"><span data-stu-id="93c33-110">This organization hierarchy is built on Finance and Operations apps, but it's exposed in Dataverse for informational and extensibility purposes.</span></span> <span data-ttu-id="93c33-111">Eftirfarandi mynd sýnir upplýsingar um stigveldi fyrirtækis sem birtast í Dataverse sem einstefnugagnaflæði úr forritum Finance and Operations til Dataverse.</span><span class="sxs-lookup"><span data-stu-id="93c33-111">The following illustration shows the organization hierarchy information that is exposed in Dataverse as a one-way data flow from Finance and Operations apps to Dataverse.</span></span>

![Skipulagsmynd](media/dual-write-data-flow.png)

<span data-ttu-id="93c33-113">Töflukort fyrirtækjastigveldis eru tiltæk fyrir einstefnusamstillingu gagna frá Finance and Operations -forritum til Dataverse.</span><span class="sxs-lookup"><span data-stu-id="93c33-113">Organization hierarchy table maps are available for one-way synchronization of data from Finance and Operations apps to Dataverse.</span></span>

## <a name="templates"></a><span data-ttu-id="93c33-114">Sniðmát</span><span class="sxs-lookup"><span data-stu-id="93c33-114">Templates</span></span>

<span data-ttu-id="93c33-115">Afurðarupplýsingar innihalda allar upplýsingar sem tengjast vörunni og skilgreiningu hennar, svo sem afurðarvíddir eða mælingar og geymsluvíddir.</span><span class="sxs-lookup"><span data-stu-id="93c33-115">Product information contains all the information related to the product and its definition, such as the product dimensions or the tracking and storage dimensions.</span></span> <span data-ttu-id="93c33-116">Eins og eftirfarandi tafla sýnir er búið að stofna safn af töflukortum til að samstilla afurðir og tengdar upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="93c33-116">As the following table shows, a collection of table maps is created to sync products and related information.</span></span>

<span data-ttu-id="93c33-117">Finance and Operations-smáforrit</span><span class="sxs-lookup"><span data-stu-id="93c33-117">Finance and Operations apps</span></span> | <span data-ttu-id="93c33-118">Önnur Dynamics 365 forrit</span><span class="sxs-lookup"><span data-stu-id="93c33-118">Other Dynamics 365 apps</span></span> | <span data-ttu-id="93c33-119">lýsing</span><span class="sxs-lookup"><span data-stu-id="93c33-119">Description</span></span>
-----------------------|--------------------------------|---
<span data-ttu-id="93c33-120">Tilgangur fyrir stigveldi fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="93c33-120">Organization hierarchy purposes</span></span> | <span data-ttu-id="93c33-121">msdyn_internalorganizationhierarchypurposes</span><span class="sxs-lookup"><span data-stu-id="93c33-121">msdyn_internalorganizationhierarchypurposes</span></span> | <span data-ttu-id="93c33-122">Þetta sniðmát veitir samstillingu í eina átt á einingunni tilgangi fyrirtækjaskipulags.</span><span class="sxs-lookup"><span data-stu-id="93c33-122">This template provides one-way synchronization of the Organization Hierarchy Purpose entity.</span></span>
<span data-ttu-id="93c33-123">Gerð fyrirtækisstigveldis</span><span class="sxs-lookup"><span data-stu-id="93c33-123">Organization hierarchy type</span></span> | <span data-ttu-id="93c33-124">msdyn_internalorganizationhierarchytypes</span><span class="sxs-lookup"><span data-stu-id="93c33-124">msdyn_internalorganizationhierarchytypes</span></span> | <span data-ttu-id="93c33-125">Þetta sniðmát veitir samstillingu í eina átt á einingunni Gerð fyrirtækjaskipulags.</span><span class="sxs-lookup"><span data-stu-id="93c33-125">This template provides one-way synchronization of the Organization Hierarchy Type entity.</span></span>
<span data-ttu-id="93c33-126">Stigveldi fyrirtækis - útgefið</span><span class="sxs-lookup"><span data-stu-id="93c33-126">Organization hierarchy - published</span></span> | <span data-ttu-id="93c33-127">msdyn_internalorganizationhierarchies</span><span class="sxs-lookup"><span data-stu-id="93c33-127">msdyn_internalorganizationhierarchies</span></span> | <span data-ttu-id="93c33-128">Þetta sniðmát veitir samstillingu í eina átt á einingunni Útgefið fyrirtækjaskipulag.</span><span class="sxs-lookup"><span data-stu-id="93c33-128">This template provides one-way synchronization of the Organization Hierarchy Published entity.</span></span>
<span data-ttu-id="93c33-129">Rekstrareining</span><span class="sxs-lookup"><span data-stu-id="93c33-129">Operating unit</span></span> | <span data-ttu-id="93c33-130">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="93c33-130">msdyn_internalorganizations</span></span> |
<span data-ttu-id="93c33-131">Lögaðilar</span><span class="sxs-lookup"><span data-stu-id="93c33-131">Legal entities</span></span> | <span data-ttu-id="93c33-132">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="93c33-132">msdyn_internalorganizations</span></span> |
<span data-ttu-id="93c33-133">Lögaðilar</span><span class="sxs-lookup"><span data-stu-id="93c33-133">Legal entities</span></span> | <span data-ttu-id="93c33-134">cdm_companies</span><span class="sxs-lookup"><span data-stu-id="93c33-134">cdm_companies</span></span> | <span data-ttu-id="93c33-135">Veitir tvíátta samstillingu upplýsinga um lögaðila (fyrirtæki).</span><span class="sxs-lookup"><span data-stu-id="93c33-135">Provides bidirectional synchronization of legal entity (company) information.</span></span>

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Organization hierarchy purposes](includes/OrganizationHierarchyPurpose-msdyn-internalorganizationhierarchypurposes.md)]

[!include [Organization hierarchy type](includes/OrganizationHierarchyType-msdyn-internalorganizationhierarchytypes.md)]

[!include [Organization hierarchy - published](includes/OrganizationHierarchyPublished-msdyn-internalorganizationhierarchies.md)]

## <a name="internal-organization"></a><span data-ttu-id="93c33-136">Innra fyrirtæki</span><span class="sxs-lookup"><span data-stu-id="93c33-136">Internal Organization</span></span>

<span data-ttu-id="93c33-137">Upplýsingar um samstæðufyrirtæki í Dataverse koma úr tveimur töflum, **rekstrareiningu** og **lögaðilum**.</span><span class="sxs-lookup"><span data-stu-id="93c33-137">Internal organization information in Dataverse comes from two tables, **operating unit** and **legal entities**.</span></span>

[!include [Operating unit](includes/OperatingUnit-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-Companies.md)]
