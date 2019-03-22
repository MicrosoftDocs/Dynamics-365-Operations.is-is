---
title: Algengar spurningar um verkflæði
description: Þetta efnisatriði svarar algengum spurningum um verkflæðiskerfið í Microsoft Dynamics 365 for Finance and Operations.
author: ChrisGarty
manager: AnnBe
ms.date: 02/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f058a450eb18e688efbc5306a42b4efef6aa91e7
ms.sourcegitcommit: 9a723737565ac78c884e40f7129d0f5aad747524
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/01/2019
ms.locfileid: "773215"
---
# <a name="workflow-system"></a><span data-ttu-id="64290-103">Verkflæðiskerfi</span><span class="sxs-lookup"><span data-stu-id="64290-103">Workflow system</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="64290-104">Þetta efnisatriði svarar algengum spurningum um verkflæðiskerfið í Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="64290-104">This topic answers frequently asked questions about the workflow system in Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="notifications"></a><span data-ttu-id="64290-105">Tilkynningar</span><span class="sxs-lookup"><span data-stu-id="64290-105">Notifications</span></span>

### <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a><span data-ttu-id="64290-106">Hvers vegna koma margar tilkynningar þegar vinnulið er hafnað?</span><span class="sxs-lookup"><span data-stu-id="64290-106">Why are multiple notifications received when a work item is rejected?</span></span>
<span data-ttu-id="64290-107">Þegar vinnulið er hafnað er honum lokið sem höfnuðum.</span><span class="sxs-lookup"><span data-stu-id="64290-107">When a work item is rejected, that work item is completed as rejected.</span></span> <span data-ttu-id="64290-108">Annar vinnuliður er stofnaður og honum er úthlutað á upphaflegan aðila.</span><span class="sxs-lookup"><span data-stu-id="64290-108">Another work item is created and assigned to the originator.</span></span> <span data-ttu-id="64290-109">Þetta þýðir að tilkynning er send á upphaflegan aðila vegna hafnaðs vinnuliðar og aðskilin tilkynning send á notandann sem fær úthlutaðan nýja vinnuliðinn „beiðni um breytingu“.</span><span class="sxs-lookup"><span data-stu-id="64290-109">This means that there is a notification to the originator for the rejected work item, and a separate notification to the user assigned to the new "change requested" work item.</span></span> 

<span data-ttu-id="64290-110">Hver tilkynning er fyrir mismunandi vinnulið, en líkindin geta valdið ruglingi.</span><span class="sxs-lookup"><span data-stu-id="64290-110">Each notification is for a different work item, but the similarity can cause confusion.</span></span> <span data-ttu-id="64290-111">Við erum að skoða leiðir til að bæta þetta í framtíðarútgáfu.</span><span class="sxs-lookup"><span data-stu-id="64290-111">We are looking at ways to improve this in a future release.</span></span>