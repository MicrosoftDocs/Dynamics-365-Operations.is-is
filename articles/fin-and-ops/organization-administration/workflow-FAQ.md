---
title: Algengar spurningar um verkflæði
description: Þetta efnisatriði svarar algengum spurningum um verkflæðiskerfið í Microsoft Dynamics 365 for Finance and Operations.
author: ChrisGarty
manager: AnnBe
ms.date: 05/07/2019
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
ms.openlocfilehash: f6240b1b5136937aa47f455547fed6f0c7c08e2c
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/07/2019
ms.locfileid: "1509292"
---
# <a name="workflow-system"></a><span data-ttu-id="1e878-103">Verkflæðiskerfi</span><span class="sxs-lookup"><span data-stu-id="1e878-103">Workflow system</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1e878-104">Þetta efnisatriði svarar algengum spurningum um verkflæðiskerfið í Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1e878-104">This topic answers frequently asked questions about the workflow system in Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="notifications"></a><span data-ttu-id="1e878-105">Tilkynningar</span><span class="sxs-lookup"><span data-stu-id="1e878-105">Notifications</span></span>

### <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a><span data-ttu-id="1e878-106">Hvers vegna koma margar tilkynningar þegar vinnulið er hafnað?</span><span class="sxs-lookup"><span data-stu-id="1e878-106">Why are multiple notifications received when a work item is rejected?</span></span>
<span data-ttu-id="1e878-107">Þegar vinnulið er hafnað er honum lokið sem höfnuðum.</span><span class="sxs-lookup"><span data-stu-id="1e878-107">When a work item is rejected, that work item is completed as rejected.</span></span> <span data-ttu-id="1e878-108">Annar vinnuliður er stofnaður og honum er úthlutað á upphaflegan aðila.</span><span class="sxs-lookup"><span data-stu-id="1e878-108">Another work item is created and assigned to the originator.</span></span> <span data-ttu-id="1e878-109">Þetta þýðir að tilkynning er send á upphaflegan aðila vegna hafnaðs vinnuliðar og aðskilin tilkynning send á notandann sem fær úthlutaðan nýja vinnuliðinn „beiðni um breytingu“.</span><span class="sxs-lookup"><span data-stu-id="1e878-109">This means that there is a notification to the originator for the rejected work item, and a separate notification to the user assigned to the new "change requested" work item.</span></span> 

<span data-ttu-id="1e878-110">Hver tilkynning er fyrir mismunandi vinnulið, en líkindin geta valdið ruglingi.</span><span class="sxs-lookup"><span data-stu-id="1e878-110">Each notification is for a different work item, but the similarity can cause confusion.</span></span> <span data-ttu-id="1e878-111">Við erum að skoða leiðir til að bæta þetta í framtíðarútgáfu.</span><span class="sxs-lookup"><span data-stu-id="1e878-111">We are looking at ways to improve this in a future release.</span></span>

### <a name="why-are-my-workflow-exports-failing"></a><span data-ttu-id="1e878-112">Afhverju eru útflutningar á verkflæðum að mistakast?</span><span class="sxs-lookup"><span data-stu-id="1e878-112">Why are my workflow exports failing?</span></span>
<span data-ttu-id="1e878-113">Sem stendur eru takmörk á eiginleikanum fyrir útflutning verkflæðis sem koma í veg fyrir að heiti verkflæða séu lengri en 48 stafir.</span><span class="sxs-lookup"><span data-stu-id="1e878-113">There is currently a limitation in the workflow export feature that prevents workflow names from exceeding 48 characters.</span></span> <span data-ttu-id="1e878-114">Að nota heiti sem er lengra en 48 stafir getur leitt til villunnar „Þjónn gat ekki sannvottað beiðnina“ og/eða komið í veg fyrir að skrá verði flutt út án skráargerðar.</span><span class="sxs-lookup"><span data-stu-id="1e878-114">Using a name that is longer than 48 characters can result in a "Server failed to authenticate the request" error and/or prevent a file to be exported  without a file type.</span></span> <span data-ttu-id="1e878-115">Eftirfarandi bloggfærsla veitir frekari upplýsingar [Úrræðaleit fyrir útflutning verkflæðis](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting).</span><span class="sxs-lookup"><span data-stu-id="1e878-115">The following blog post provides more details [Workflow Export Troubleshooting](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting).</span></span>
