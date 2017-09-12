---
title: "Bæta fjárhagsvíddum við CFO vinnusvæðið"
description: "Þetta efnisatriði útskýrir hvernig skal bæta fjárhagsvíddum við CFO vinnusvæðið, svo hægt sé að nota þær fyrir fjárhags- og fjárhagáætlunarskýrslurnar."
author: aolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.2.0
ms.translationtype: HT
ms.sourcegitcommit: 9953d2f29a67b35f4bb43f577df1c4d910e379a1
ms.openlocfilehash: 05fd7ce5293b3a300aabc073a6e492c5804d1897
ms.contentlocale: is-is
ms.lasthandoff: 08/03/2017

---

# <a name="add-financial-dimensions-to-the-cfo-workspace"></a><span data-ttu-id="87d78-103">Bæta fjárhagsvíddum við CFO vinnusvæðið</span><span class="sxs-lookup"><span data-stu-id="87d78-103">Add financial dimensions to the CFO workspace</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="87d78-104">Þetta efnisatriði útskýrir hvernig skal bæta fjárhagsvíddum við Fjármálastjóra (CFO) vinnusvæðið, svo hægt sé að nota þær fyrir fjárhags- og fjárhagáætlunarskýrslurnar.</span><span class="sxs-lookup"><span data-stu-id="87d78-104">This topic explains how to add financial dimensions to the Chief Financial Officer (CFO) workspace, so that they can be used for the ledger and budget reports.</span></span> <span data-ttu-id="87d78-105">CFO vinnusvæðið er með **Yfirlit** flipa og **Fjármála** flipa.</span><span class="sxs-lookup"><span data-stu-id="87d78-105">The CFO workspace has an **Overview** tab and a **Financial** tab.</span></span> <span data-ttu-id="87d78-106">Skýrslurnar á þessum tveimur flipum eru studdar með tveimur mælingum: LedgerActivityMeasure og BudgetActivityMeasure.</span><span class="sxs-lookup"><span data-stu-id="87d78-106">The reports on these two tabs are backed by two measures: LedgerActivityMeasure and BudgetActivityMeasure.</span></span> <span data-ttu-id="87d78-107">Í júlí 2017 uppfærslunni af Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition er tenging á milli þessara tveggja mælinga og DimensionCombinationEntity einingarinnar.</span><span class="sxs-lookup"><span data-stu-id="87d78-107">In Microsoft Dynamics 365 for Finance and Operations, Enterprise edition July 2017 update, there is a relation between those two measures and the DimensionCombinationEntity entity.</span></span> <span data-ttu-id="87d78-108">Þar af leiðandi geturðu valið víddir.</span><span class="sxs-lookup"><span data-stu-id="87d78-108">Therefore, you can select dimensions.</span></span>

1. <span data-ttu-id="87d78-109">Í Finance and Operations, á **Eining verslun** síðunni skal uppfæra **LedgerActivityMeasure** og **BudgetActivityMeasure** mælingarnar.</span><span class="sxs-lookup"><span data-stu-id="87d78-109">In Finance and Operations, on the **Entity Store** page, update the **LedgerActivityMeasure** and the **BudgetActivityMeasure** measures.</span></span>
2. <span data-ttu-id="87d78-110">Í Microsoft Visual Studio skal opna Application Explorer og leita að **LedgerCFO**.</span><span class="sxs-lookup"><span data-stu-id="87d78-110">In Microsoft Visual Studio, open Application Explorer, and search for **LedgerCFO**.</span></span>
3. <span data-ttu-id="87d78-111">Undir **Forði** skal opna **LedgerCFOWorkspacePBIX**.</span><span class="sxs-lookup"><span data-stu-id="87d78-111">Under **Resources**, open **LedgerCFOWorkspacePBIX**.</span></span>
4. <span data-ttu-id="87d78-112">Þegar forðinn opnast í Microsoft Power BI skjáborð, skal velja **Sækja gögn**, velja **SQL Server gagnagrunnur**, og velja svo **Tengja**.</span><span class="sxs-lookup"><span data-stu-id="87d78-112">When the resource opens in Microsoft Power BI desktop, select **Get Data**, select **SQL Server database**, and then select **Connect**.</span></span>
5. <span data-ttu-id="87d78-113">Færa inn heiti þjóns og færa inn **AxDW** sem gagnagrunninn.</span><span class="sxs-lookup"><span data-stu-id="87d78-113">Enter the server name, and enter **AxDW** as the database.</span></span> <span data-ttu-id="87d78-114">Velja skal **DirectQuery** og svo **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="87d78-114">Select **DirectQuery**, and then select **OK**.</span></span>
6. <span data-ttu-id="87d78-115">Leita að og velja **LedgerActivityMeasure\_DimensionCombination** og velja svo **Hlaða**.</span><span class="sxs-lookup"><span data-stu-id="87d78-115">Search for and select **LedgerActivityMeasure\_DimensionCombination**, and then select **Load**.</span></span>

    > [!TIP]
    > <span data-ttu-id="87d78-116">Í listanum **Reitir** skal endurnefna töfluna **Fjármálavíddir** svo það sé auðvelt að finna hana.</span><span class="sxs-lookup"><span data-stu-id="87d78-116">In the **Fields** list, rename the table **Financial dimensions**, so that it's easy to identify.</span></span>

7. <span data-ttu-id="87d78-117">Smellið á **Stjórna venslum** og veljið síðan **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="87d78-117">Select **Manage Relationships**, and then select **New**.</span></span>
8. <span data-ttu-id="87d78-118">Í fyrsta reitnum skal velja **Fjárhagsvirkni** og velja svo **Fjárhagsvídd**.</span><span class="sxs-lookup"><span data-stu-id="87d78-118">In the first field, select **General Ledger Activities**, and then select **LedgerDimension**.</span></span>
9. <span data-ttu-id="87d78-119">Í öðrum reitnum skal velja **LedgerActivityMeasure\_DimensionCombination** (eða **Fjármálavíddir** ef þú endurnefndir töfluna).</span><span class="sxs-lookup"><span data-stu-id="87d78-119">In the second field, select **LedgerActivityMeasure\_DimensionCombination** (or **Financial dimensions** if you renamed the table).</span></span> <span data-ttu-id="87d78-120">Velja **DimensionCombinationRECID** hausinn.</span><span class="sxs-lookup"><span data-stu-id="87d78-120">Select the  **DimensionCombinationRECID** header.</span></span>
10. <span data-ttu-id="87d78-121">Í reitnum **Línufjöldi** skal velja **Margar til ein**.</span><span class="sxs-lookup"><span data-stu-id="87d78-121">In the **Cardinality** field, select **Many to One**.</span></span>
11. <span data-ttu-id="87d78-122">Breyta **Þverlæg afmörkun leið** gildinu í **Stakur**.</span><span class="sxs-lookup"><span data-stu-id="87d78-122">Change the **Cross filter direction** value to **Single**.</span></span>
12. <span data-ttu-id="87d78-123">Velja bæði **Virkja þessi vensl** og **Gera ráð fyrir tilvísandi áreiðanleika**, veljið **Í lagi** og veljið síðan **Loka**.</span><span class="sxs-lookup"><span data-stu-id="87d78-123">Select both **Make this relationship active** and **Assume referential integrity**, select **OK**, and then select **Close**.</span></span>

    <span data-ttu-id="87d78-124">[![Stofna vensl](./media/Create-relationship.png)](./media/Create-relationship.png)</span><span class="sxs-lookup"><span data-stu-id="87d78-124">[![Create a relationship](./media/Create-relationship.png)](./media/Create-relationship.png)</span></span>

13. <span data-ttu-id="87d78-125">Í listanum **Reitir** ættirðu að sjá töfluna og tiltækar fjármálavíddir.</span><span class="sxs-lookup"><span data-stu-id="87d78-125">In the **Fields** list, you should see the table and the available financial dimensions.</span></span> <span data-ttu-id="87d78-126">Dragðu fjárhagsvíddirnar sem þú vilt yfir í skýrsla-stig afmarkanirnar.</span><span class="sxs-lookup"><span data-stu-id="87d78-126">Drag the financial dimensions that you want to the report-level filters.</span></span>
14. <span data-ttu-id="87d78-127">Vista breytingarnar.</span><span class="sxs-lookup"><span data-stu-id="87d78-127">Save your changes.</span></span>
15. <span data-ttu-id="87d78-128">Í Hugbúnaðarhlutatrénu (AOT) skal hægri-smella á þitt verkefni og velja síðan **Samstilla**.</span><span class="sxs-lookup"><span data-stu-id="87d78-128">In the Application Object Tree (AOT), right-click your project, and then select **Synchronize**.</span></span>
16. <span data-ttu-id="87d78-129">Smíðaðu þitt verkefni og opnaðu svo forritið til að skoða niðurstöðurnar.</span><span class="sxs-lookup"><span data-stu-id="87d78-129">Build your project, and then open the application to view the results.</span></span>

    <span data-ttu-id="87d78-130">[![Vinnusvæði lokið](./media/workspace.png)](./media/workspace.png)</span><span class="sxs-lookup"><span data-stu-id="87d78-130">[![Completed workspace](./media/workspace.png)](./media/workspace.png)</span></span>

