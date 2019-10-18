---
title: Sölupantanir verks
description: Þetta efnisatriði útskýrir hvernig á að stofna verkmiðaðar sölupantanir fyrir tíma- og efnisverk.
author: KimANelson
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 1d54c98a08dc7cccb5cafbbe401d0ce25a276c25
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185498"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a><span data-ttu-id="7038e-103">Sölupantanir verks fyrir tíma- og efnisverk</span><span class="sxs-lookup"><span data-stu-id="7038e-103">Project sales orders for time and material projects</span></span>

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

<span data-ttu-id="7038e-104">Þetta efnisatriði útskýrir hvernig á að stofna sölupöntun fyrir verk.</span><span class="sxs-lookup"><span data-stu-id="7038e-104">This topic describes how to create a sales order for a project.</span></span> <span data-ttu-id="7038e-105">Aðeins er hægt að stofna sölupantanir fyrir verk af gerðinni **tími og efni**.</span><span class="sxs-lookup"><span data-stu-id="7038e-105">Sales orders can only be created for projects of type **time and material**.</span></span>

<span data-ttu-id="7038e-106">Ef tíma- og efnisverk er með marga fjármögnunaraðila í verksamningi er nauðsynlegt að virkja færibreytuna **Leyfa sölupantanir fyrir verk með mörgum fjármögnunaraðilum** á síðunni **Verkefnastjórnun og bókhaldsfæribreytur**.</span><span class="sxs-lookup"><span data-stu-id="7038e-106">If a time and material project has multiple funding sources on the project contract, you must enable the **Allow sales orders for projects with multiple funding sources** parameter on the **Project management and accounting parameters** page.</span></span> 

> [!NOTE]
> - <span data-ttu-id="7038e-107">Stuðningur fyrir sölupantanir verks með marga fjármögnunaraðila er í boði frá og með útgáfu 10.0.2 og nýrri af forritinu.</span><span class="sxs-lookup"><span data-stu-id="7038e-107">Support for project sales orders with multiple funding sources is available starting with application release 10.0.2 and higher.</span></span>
> - <span data-ttu-id="7038e-108">Færibreytan til að virkja stuðning fyrir sölupantanir verks með marga fjármögnunaraðila verður fjarlægð í útgáfulotu í apríl 2020 og virknin verður eftir það alltaf virk.</span><span class="sxs-lookup"><span data-stu-id="7038e-108">The parameter to enable the support for project sales orders with multiple funding sources will be removed in the April 2020 release wave, after which the functionality will always be enabled.</span></span>

<span data-ttu-id="7038e-109">Hægt er að stofna verkmiðaðar sölupantanir á tvo vegu:</span><span class="sxs-lookup"><span data-stu-id="7038e-109">You can create project-based sales orders in two ways:</span></span>

- <span data-ttu-id="7038e-110">Opna sjálft verkið.</span><span class="sxs-lookup"><span data-stu-id="7038e-110">Go to the project itself.</span></span> <span data-ttu-id="7038e-111">Á aðgerðasvæðinu skal velja **Stjórna > Verkliðir > Sölupöntun**.</span><span class="sxs-lookup"><span data-stu-id="7038e-111">On the Action Pane, select **Manage > Item tasks > Sales order**.</span></span> <span data-ttu-id="7038e-112">Verkupplýsingarnar verða sjálfgefnar fyrir sölupöntunina úr verkinu.</span><span class="sxs-lookup"><span data-stu-id="7038e-112">The project information will default to the sales order from the project.</span></span> <span data-ttu-id="7038e-113">Ef verksamningurinn er með fleiri en einn fjármögnunaraðila er nauðsynlegt að velja fjármögnunaraðilann til að setja á viðskiptavininn fyrir sölupöntunina.</span><span class="sxs-lookup"><span data-stu-id="7038e-113">If the project contract has more than one funding source, you will need to select the funding source to set the customer for the sales order.</span></span> <span data-ttu-id="7038e-114">Ef aðeins einn fjármögnunaraðili er fyrir verkið verður viðskiptavinurinn settur sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="7038e-114">If there is only one funding source for the project, the customer will be automatically set.</span></span>
- <span data-ttu-id="7038e-115">Opna skal listasíðuna **Allar sölupantanir** og stofna nýja sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="7038e-115">Go to the **All sales order** list page and create a new sales order.</span></span> <span data-ttu-id="7038e-116">Velja þarf verkið fyrir sölupöntunina.</span><span class="sxs-lookup"><span data-stu-id="7038e-116">You will need to select the project for the sales order.</span></span> <span data-ttu-id="7038e-117">Eftir að verkið er valið verður viðskiptavinur settur úr fjármögnunaraðilum eða þú þarft að velja fjármögnunaraðilann ef verksamningurinn er með marga fjármögnunaraðila.</span><span class="sxs-lookup"><span data-stu-id="7038e-117">After the project is selected, the customer will be set from the funding source or you will need to select the funding source if the project contract has multiple funding sources.</span></span>

