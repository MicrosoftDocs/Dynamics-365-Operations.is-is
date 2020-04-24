---
title: Eignayfirlit
description: Þetta efnisatriði lýsir eignasýn í eignastjórnun.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 14dc2cd95a47931ae4941b87205f2104891af404
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208226"
---
# <a name="asset-view"></a><span data-ttu-id="4759d-103">Eignayfirlit</span><span class="sxs-lookup"><span data-stu-id="4759d-103">Asset view</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="4759d-104">Þetta efnisatriði lýsir eignasýn í eignastjórnun.</span><span class="sxs-lookup"><span data-stu-id="4759d-104">This topic describes the asset view in Asset Management.</span></span> <span data-ttu-id="4759d-105">Síðan **Eignasýn** sýnir virkar eignir og virkar staðsetningar í trjáskoðun.</span><span class="sxs-lookup"><span data-stu-id="4759d-105">The **Asset view** page shows active assets and functional locations in a tree view.</span></span> <span data-ttu-id="4759d-106">Þess vegna geturðu auðveldlega fengið yfirlit yfir eignatengsl við virka staði.</span><span class="sxs-lookup"><span data-stu-id="4759d-106">Therefore, you can easily get an overview of asset relations to functional locations.</span></span> <span data-ttu-id="4759d-107">Að auki geturðu skoðað nákvæmar upplýsingar um virka staði, eignir og tengda uppskriftir (BOMs).</span><span class="sxs-lookup"><span data-stu-id="4759d-107">Additionally, you can view detailed information about functional locations, assets, and related bills of materials (BOMs).</span></span> <span data-ttu-id="4759d-108">Þú getur líka fengið fljótt yfirlit yfir virkar viðhaldsbeiðnir og verkbeiðnir sem tengjast eign.</span><span class="sxs-lookup"><span data-stu-id="4759d-108">You can also get a quick overview of active maintenance requests and work orders that are related to an asset.</span></span>

1. <span data-ttu-id="4759d-109">Veldu **Eignastýring** \> **Sameiginlegt** \> **Eignir** \> **Eignasýn**.</span><span class="sxs-lookup"><span data-stu-id="4759d-109">Select **Asset management** \> **Common** \> **Assets** \> **Asset view**.</span></span>
2. <span data-ttu-id="4759d-110">Til að breyta skjánum sem sést á síðunni velurðu nýtt gildi í reitnum **Skoða**.</span><span class="sxs-lookup"><span data-stu-id="4759d-110">To change the view that is shown on the page, select a new value in the **View** field.</span></span>

    > [!NOTE]
    > <span data-ttu-id="4759d-111">Sjálfgefna sýnin sem birtist þegar þú opnar **Eignamat** síðu fer eftir gildi sem er valið í **Skoða** reit á **Eignir** flipanum **Breytur eignastýringar** síðu (**Eignastýring** \> **Uppsetning** \> **Breytur eignastýringar**).</span><span class="sxs-lookup"><span data-stu-id="4759d-111">The default view that is shown when you open the **Asset view** page depends on the value that is selected in the **View** field on the **Assets** tab of the **Asset management parameters** page (**Asset management** \> **Setup** \> **Asset management parameters**).</span></span>

<span data-ttu-id="4759d-112">Hægra megin á síðunni sýnir flýtiflipar upplýsingar um valinn skjá.</span><span class="sxs-lookup"><span data-stu-id="4759d-112">On the right side of the page, FastTabs shows details of the selected view.</span></span>

<span data-ttu-id="4759d-113">Brauðmylsnuslóðin sem birtist fyrir ofan trjáskjáinn sýnir núverandi val í trjásýninni.</span><span class="sxs-lookup"><span data-stu-id="4759d-113">The breadcrumb trail that appears above the tree view shows the current selection in the tree view.</span></span> <span data-ttu-id="4759d-114">Þessi brauðmylsnuslóð notar eftirfarandi snið:</span><span class="sxs-lookup"><span data-stu-id="4759d-114">This breadcrumb trail uses the following format:</span></span>

<span data-ttu-id="4759d-115">Kenni virkrar staðsetningar / Kenni virkar staðsetningar (ef það eru fleiri en einn virkar staðsetningar) \> Eignakenni / Eignakenni (ef það eru fleiri en ein eign) - Vörunúmer.</span><span class="sxs-lookup"><span data-stu-id="4759d-115">Functional location ID / Functional location ID (if there is more than one functional location) \> Asset ID / Asset ID (if there is more than one asset) - Item number.</span></span>

<span data-ttu-id="4759d-116">Ef þú hefur valið eign í trjáskjánum geturðu valið **Virkar beiðnir** eða **Virkar vinnupantanir** til að skoða viðhaldsbeiðnir eða verkbeiðnir sem tengjast eigninni.</span><span class="sxs-lookup"><span data-stu-id="4759d-116">If you've selected an asset in the tree view, you can select **Active requests** or **Active work orders** to view the maintenance requests or work orders that are related to the asset.</span></span> <span data-ttu-id="4759d-117">Þú getur líka valið **Opið** \> **Virk staðsetning**, **Eignir**, eða **Uppskrift eignar** til að opna tengda sýn.</span><span class="sxs-lookup"><span data-stu-id="4759d-117">You can also select **Open** \> **Functional location**, **Asset**, or **Asset BOM** to open the related view.</span></span>

<span data-ttu-id="4759d-118">Valkosturinn **Virkar staðsetningar eigna** sem þú getur valið í **Skoða** reiturinn er einnig fáanlegur í hvaða eignaleit þar sem þú getur valið eign.</span><span class="sxs-lookup"><span data-stu-id="4759d-118">The **Asset functional locations** option that you can select in the **View** field is also available in any asset lookup where you can select an asset.</span></span> <span data-ttu-id="4759d-119">Trjásýnin er sýnt á **Eignamat** flipann, til dæmis þar sem þú [stofnar eign](../objects/create-an-object.md), búðu til viðhaldsbeiðni eða stofnaðu verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="4759d-119">The tree view is shown on an **Asset view** tab, for example, where you [create an asset](../objects/create-an-object.md), create a maintenance request, or create a work order.</span></span>
