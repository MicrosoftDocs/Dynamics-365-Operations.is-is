---
title: "Bæta fjárhagsvíddum við CFO vinnusvæðið"
description: "Þetta efnisatriði útskýrir hvernig skal bæta fjárhagsvíddum við CFO vinnusvæðið, svo hægt sé að nota þær fyrir fjárhags- og fjárhagáætlunarskýrslurnar."
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 04643d4d9e3c0a21f2dac3ce27a7398f7be4f775
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---

# <a name="add-financial-dimensions-to-the-cfo-workspace"></a><span data-ttu-id="ae464-103">Bæta fjárhagsvíddum við CFO vinnusvæðið</span><span class="sxs-lookup"><span data-stu-id="ae464-103">Add financial dimensions to the CFO workspace</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="ae464-104">Þetta efnisatriði útskýrir hvernig skal bæta fjárhagsvíddum við Fjármálastjóra (CFO) vinnusvæðið, svo hægt sé að nota þær fyrir fjárhags- og fjárhagáætlunarskýrslurnar.</span><span class="sxs-lookup"><span data-stu-id="ae464-104">This topic explains how to add financial dimensions to the Chief Financial Officer (CFO) workspace, so that they can be used for the ledger and budget reports.</span></span> <span data-ttu-id="ae464-105">CFO vinnusvæðið er með **Yfirlit** flipa og **Fjármála** flipa. Skýrslurnar á þessum tveimur flipum eru studdar með tveimur mælingum: LedgerActivityMeasure and BudgetActivityMeasure.</span><span class="sxs-lookup"><span data-stu-id="ae464-105">The CFO workspace has an **Overview** tab and a **Financial** tab. The reports on these two tabs are backed by two measures: LedgerActivityMeasure and BudgetActivityMeasure.</span></span> <span data-ttu-id="ae464-106">Í júlí 2017 uppfærslunni af Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition er tenging á milli þessara tveggja mælinga og DimensionCombinationEntity einingarinnar.</span><span class="sxs-lookup"><span data-stu-id="ae464-106">In Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017), there is a relation between those two measures and the DimensionCombinationEntity entity.</span></span> <span data-ttu-id="ae464-107">Þar af leiðandi geturðu valið víddir.</span><span class="sxs-lookup"><span data-stu-id="ae464-107">Therefore, you can select dimensions.</span></span>

1. <span data-ttu-id="ae464-108">Í Finance and Operations, á **Eining verslun** síðunni skal uppfæra **LedgerActivityMeasure** og **BudgetActivityMeasure** mælingarnar.</span><span class="sxs-lookup"><span data-stu-id="ae464-108">In Finance and Operations, on the **Entity Store** page, update the **LedgerActivityMeasure** and the **BudgetActivityMeasure** measures.</span></span>
2. <span data-ttu-id="ae464-109">Í Microsoft Visual Studio skal opna Application Explorer og leita að **LedgerCFO**.</span><span class="sxs-lookup"><span data-stu-id="ae464-109">In Microsoft Visual Studio, open Application Explorer, and search for **LedgerCFO**.</span></span>
3. <span data-ttu-id="ae464-110">Undir **Forði** skal opna **LedgerCFOWorkspacePBIX**.</span><span class="sxs-lookup"><span data-stu-id="ae464-110">Under **Resources**, open **LedgerCFOWorkspacePBIX**.</span></span>
4. <span data-ttu-id="ae464-111">Þegar forðinn opnast í Microsoft Power BI skjáborð, skal velja **Sækja gögn**, velja **SQL Server gagnagrunnur**, og velja svo **Tengja**.</span><span class="sxs-lookup"><span data-stu-id="ae464-111">When the resource opens in Microsoft Power BI desktop, select **Get Data**, select **SQL Server database**, and then select **Connect**.</span></span>
5. <span data-ttu-id="ae464-112">Færa inn heiti þjóns og færa inn **AxDW** sem gagnagrunninn.</span><span class="sxs-lookup"><span data-stu-id="ae464-112">Enter the server name, and enter **AxDW** as the database.</span></span> <span data-ttu-id="ae464-113">Velja skal **DirectQuery** og svo **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="ae464-113">Select **DirectQuery**, and then select **OK**.</span></span>
6. <span data-ttu-id="ae464-114">Leita að og velja **LedgerActivityMeasure\_DimensionCombination** og velja svo **Hlaða**.</span><span class="sxs-lookup"><span data-stu-id="ae464-114">Search for and select **LedgerActivityMeasure\_DimensionCombination**, and then select **Load**.</span></span>

    > [!TIP]
    > <span data-ttu-id="ae464-115">Í listanum **Reitir** skal endurnefna töfluna **Fjármálavíddir** svo það sé auðvelt að finna hana.</span><span class="sxs-lookup"><span data-stu-id="ae464-115">In the **Fields** list, rename the table **Financial dimensions**, so that it's easy to identify.</span></span>

7. <span data-ttu-id="ae464-116">Smellið á **Stjórna venslum** og veljið síðan **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="ae464-116">Select **Manage Relationships**, and then select **New**.</span></span>
8. <span data-ttu-id="ae464-117">Í fyrsta reitnum skal velja **Fjárhagsvirkni** og velja svo **Fjárhagsvídd**.</span><span class="sxs-lookup"><span data-stu-id="ae464-117">In the first field, select **General Ledger Activities**, and then select **LedgerDimension**.</span></span>
9. <span data-ttu-id="ae464-118">Í öðrum reitnum skal velja **LedgerActivityMeasure\_DimensionCombination** (eða **Fjármálavíddir** ef þú endurnefndir töfluna).</span><span class="sxs-lookup"><span data-stu-id="ae464-118">In the second field, select **LedgerActivityMeasure\_DimensionCombination** (or **Financial dimensions** if you renamed the table).</span></span> <span data-ttu-id="ae464-119">Velja **DimensionCombinationRECID** hausinn.</span><span class="sxs-lookup"><span data-stu-id="ae464-119">Select the  **DimensionCombinationRECID** header.</span></span>
10. <span data-ttu-id="ae464-120">Í reitnum **Línufjöldi** skal velja **Margar til ein**.</span><span class="sxs-lookup"><span data-stu-id="ae464-120">In the **Cardinality** field, select **Many to One**.</span></span>
11. <span data-ttu-id="ae464-121">Breyta **Þverlæg afmörkun leið** gildinu í **Stakur**.</span><span class="sxs-lookup"><span data-stu-id="ae464-121">Change the **Cross filter direction** value to **Single**.</span></span>
12. <span data-ttu-id="ae464-122">Velja bæði **Virkja þessi vensl** og **Gera ráð fyrir tilvísandi áreiðanleika**, veljið **Í lagi** og veljið síðan **Loka**.</span><span class="sxs-lookup"><span data-stu-id="ae464-122">Select both **Make this relationship active** and **Assume referential integrity**, select **OK**, and then select **Close**.</span></span>

    <span data-ttu-id="ae464-123">[![Stofna vensl](./media/Create-relationship.png)](./media/Create-relationship.png)</span><span class="sxs-lookup"><span data-stu-id="ae464-123">[![Create a relationship](./media/Create-relationship.png)](./media/Create-relationship.png)</span></span>

13. <span data-ttu-id="ae464-124">Í listanum **Reitir** ættirðu að sjá töfluna og tiltækar fjármálavíddir.</span><span class="sxs-lookup"><span data-stu-id="ae464-124">In the **Fields** list, you should see the table and the available financial dimensions.</span></span> <span data-ttu-id="ae464-125">Dragðu fjárhagsvíddirnar sem þú vilt yfir í skýrsla-stig afmarkanirnar.</span><span class="sxs-lookup"><span data-stu-id="ae464-125">Drag the financial dimensions that you want to the report-level filters.</span></span>
14. <span data-ttu-id="ae464-126">Vista breytingarnar.</span><span class="sxs-lookup"><span data-stu-id="ae464-126">Save your changes.</span></span>
15. <span data-ttu-id="ae464-127">Í Hugbúnaðarhlutatrénu (AOT) skal hægri-smella á þitt verkefni og velja síðan **Samstilla**.</span><span class="sxs-lookup"><span data-stu-id="ae464-127">In the Application Object Tree (AOT), right-click your project, and then select **Synchronize**.</span></span>
16. <span data-ttu-id="ae464-128">Smíðaðu þitt verkefni og opnaðu svo forritið til að skoða niðurstöðurnar.</span><span class="sxs-lookup"><span data-stu-id="ae464-128">Build your project, and then open the application to view the results.</span></span>

    <span data-ttu-id="ae464-129">[![Vinnusvæði lokið](./media/workspace.png)](./media/workspace.png)</span><span class="sxs-lookup"><span data-stu-id="ae464-129">[![Completed workspace](./media/workspace.png)](./media/workspace.png)</span></span>

