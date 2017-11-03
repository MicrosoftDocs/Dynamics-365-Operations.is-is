---
title: "Stilla SQL Server Reporting Services fyrir staðbundna uppsetningu"
description: "Þetta efnisatriði veitir upplýsingar um grunnstillingu á SQL Server Reporting Services (SSRS) fyrir virkjun á staðnum."
author: sarvanisathish
manager: AnnBe
ms.date: 06/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core
ms.custom: 55651
ms.assetid: 
ms.search.region: Global
ms.author: sarvanis
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 2a1f11641a2ec055cfaa0157ac9a40525daa4006
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---
# <a name="configure-sql-server-reporting-services-for-an-on-premises-deployment"></a><span data-ttu-id="99b57-103">Stilla SQL Server Reporting Services fyrir staðbundna uppsetningu</span><span class="sxs-lookup"><span data-stu-id="99b57-103">Configure SQL Server Reporting Services for an on-premises deployment</span></span>

<span data-ttu-id="99b57-104">Fylgið skrefunumm í þessu efnisatriði til að grunnstilla virkjun SQL Server Reporting Services (SSRS) fyrir Microsoft Dynamics 365 for Finance and Operations, Enterprise útgáfu (á staðnum).</span><span class="sxs-lookup"><span data-stu-id="99b57-104">Use the steps in this topic to configure SQL Server Reporting Services (SSRS) for your Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (on-premises) deployment.</span></span>

1. <span data-ttu-id="99b57-105">Opnaðu grunnstillingarstjóra skýrslugerðarþjónustu.</span><span class="sxs-lookup"><span data-stu-id="99b57-105">Open the Reporting Services Configuration Manager application.</span></span>
2. <span data-ttu-id="99b57-106">Skildu eftir sjálfgefið **Þjónsnafn**, sem ætti að vera nafn vélarinnar sem er í notkun, og **Heiti skýrsluþjónstilviks**, **MSSQLSERVER**.</span><span class="sxs-lookup"><span data-stu-id="99b57-106">Leave the default **Server name**, which should be the name of the current machine, and the **Report Server Instance**, **MSSQLSERVER**.</span></span> 
3. <span data-ttu-id="99b57-107">Smelltu á **Tengja**.</span><span class="sxs-lookup"><span data-stu-id="99b57-107">Click **Connect**.</span></span>
   
   <span data-ttu-id="99b57-108">[![Grunnstillingartenging skýrslugerðarþjónustu](./media/ssrs-config-manager-01.png)](./media/ssrs-config-manager-01.png)</span><span class="sxs-lookup"><span data-stu-id="99b57-108">[![Reporting services configuration connection](./media/ssrs-config-manager-01.png)](./media/ssrs-config-manager-01.png)</span></span>
   
4. <span data-ttu-id="99b57-109">Smellið á flipann **Þjónustureikningur** og sannreynið að stillingarnar passi við eftirfarandi mynd.</span><span class="sxs-lookup"><span data-stu-id="99b57-109">Click the **Service Account** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="99b57-110">[![Þjónustureikningsflipi](./media/ssrs-config-manager-02.png)](./media/ssrs-config-manager-02.png)</span><span class="sxs-lookup"><span data-stu-id="99b57-110">[![Service account tab](./media/ssrs-config-manager-02.png)](./media/ssrs-config-manager-02.png)</span></span>
    
5. <span data-ttu-id="99b57-111">Smellið á flipann **Vefþjónustuslóð** og sannreynið að stillingarnar passi við eftirfarandi mynd.</span><span class="sxs-lookup"><span data-stu-id="99b57-111">Click the **Web Service URL** tab and verify that the settings match the following graphic.</span></span> 

    <span data-ttu-id="99b57-112">[![Flipi vefþjónustuslóðar](./media/ssrs-config-manager-03.png)](./media/ssrs-config-manager-03.png)</span><span class="sxs-lookup"><span data-stu-id="99b57-112">[![Web service URL tab](./media/ssrs-config-manager-03.png)](./media/ssrs-config-manager-03.png)</span></span> 
    
6. <span data-ttu-id="99b57-113">Smellið á flipann **Gagnagrunnur** og sannreynið að **Gagnagrunnsnafn** og **Skilríkjastillingar** passi við eftirfarandi mynd.</span><span class="sxs-lookup"><span data-stu-id="99b57-113">Click the **Database** tab and verify that the **Database Name** and **Credential settings** match the following graphic.</span></span> <span data-ttu-id="99b57-114">**Athugið:** Það þarf að stofna nýjan gagnagrunn.</span><span class="sxs-lookup"><span data-stu-id="99b57-114">**Note:** You will need to create a new database.</span></span> <span data-ttu-id="99b57-115">Til að gera það skal smella á **Breyta gagnagrunni** og staðfest að nýja gagnagrunnsnafnið sé: **DynamicsAxReportServer**.</span><span class="sxs-lookup"><span data-stu-id="99b57-115">To do this, click **Change Database**, and then verify that the new database name is: **DynamicsAxReportServer**.</span></span>

    <span data-ttu-id="99b57-116">[![gagnagrunnsflipi](./media/ssrs-config-manager-04.png)](./media/ssrs-config-manager-04.png)</span><span class="sxs-lookup"><span data-stu-id="99b57-116">[![database tab](./media/ssrs-config-manager-04.png)](./media/ssrs-config-manager-04.png)</span></span>
    
7. <span data-ttu-id="99b57-117">Smellið á flipann **Vefgáttarslóð** og sannreynið að stillingarnar passi við eftirfarandi mynd.</span><span class="sxs-lookup"><span data-stu-id="99b57-117">Click the **Web Portal URL** tab and verify that the settings match the following graphic.</span></span> <span data-ttu-id="99b57-118">**Athugið:** Það þarf að smella á **Nota** til að stofna og grunnstilla gáttina rétt.</span><span class="sxs-lookup"><span data-stu-id="99b57-118">**Note:** You must click **Apply** to create and properly configure the Portal.</span></span>

    <span data-ttu-id="99b57-119">[![flipi vefgáttarslóðar](./media/ssrs-config-manager-05.png)](./media/ssrs-config-manager-05.png)</span><span class="sxs-lookup"><span data-stu-id="99b57-119">[![web portal url tab](./media/ssrs-config-manager-05.png)](./media/ssrs-config-manager-05.png)</span></span>
    
  <span data-ttu-id="99b57-120">Eftir að gáttin er grunnstillt passar flipinn **Vefgátt** við eftirfarandi mynd.</span><span class="sxs-lookup"><span data-stu-id="99b57-120">After the Portal is configured, the **Web Portal** tab will match the following graphic.</span></span>
    <span data-ttu-id="99b57-121">[![vefgáttarflipi](./media/ssrs-config-manager-06.png)](./media/ssrs-config-manager-06.png)</span><span class="sxs-lookup"><span data-stu-id="99b57-121">[![web portal tab](./media/ssrs-config-manager-06.png)](./media/ssrs-config-manager-06.png)</span></span>
    
8. <span data-ttu-id="99b57-122">Smelltu á skýrsluvefslóðina til að skoða vefgátt SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="99b57-122">Click the reports URL to view the SQL Server Reporting Services web portal.</span></span> 
9.  <span data-ttu-id="99b57-123">Í gáttinni skal stofna nýja möppu með nafninu **Dynamics**.</span><span class="sxs-lookup"><span data-stu-id="99b57-123">When you are in the portal, create a new folder named **Dynamics**.</span></span>

    <span data-ttu-id="99b57-124">[![dynamics mappa](./media/ssrs-config-manager-07.png)](./media/ssrs-config-manager-07.png)</span><span class="sxs-lookup"><span data-stu-id="99b57-124">[![dynamics folder](./media/ssrs-config-manager-07.png)](./media/ssrs-config-manager-07.png)</span></span>
    
10. <span data-ttu-id="99b57-125">Í **grunnstillingarstjóra skýrslugerðarþjónustu** skal smella á flipann **tölvupóststillingar** og sannreyna að stillingarnar passi við eftirfarandi mynd.</span><span class="sxs-lookup"><span data-stu-id="99b57-125">In the **Reporting Services Configuration Manager**, click the **E-mail Settings** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="99b57-126">[![tölvupóststillingaflipi](./media/ssrs-config-manager-08.png)](./media/ssrs-config-manager-08.png)</span><span class="sxs-lookup"><span data-stu-id="99b57-126">[![email settings tab](./media/ssrs-config-manager-08.png)](./media/ssrs-config-manager-08.png)</span></span>
    
11. <span data-ttu-id="99b57-127">Smellið á flipann **Keyrslureikningur** og sannreynið að stillingarnar passi við eftirfarandi mynd.</span><span class="sxs-lookup"><span data-stu-id="99b57-127">Click the **Execution Account** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="99b57-128">[![keyrslureikningsflipi](./media/ssrs-config-manager-09.png)](./media/ssrs-config-manager-09.png)</span><span class="sxs-lookup"><span data-stu-id="99b57-128">[![execution account tab](./media/ssrs-config-manager-09.png)](./media/ssrs-config-manager-09.png)</span></span>
    
  <span data-ttu-id="99b57-129">Ekki breyta sjálfgefnum stillingum á flipanum **Dulritunarlyklar**. [![flipinn dulritunarlyklar](./media/ssrs-config-manager-10.png)](./media/ssrs-config-manager-10.png)</span><span class="sxs-lookup"><span data-stu-id="99b57-129">Don’t change the default settings on the **Encryption Keys** tab. [![encryption keys tab](./media/ssrs-config-manager-10.png)](./media/ssrs-config-manager-10.png)</span></span>
    
12. <span data-ttu-id="99b57-130">Smellið á flipann **Áskriftarstillingar** og sannreynið að stillingarnar passi við eftirfarandi mynd.</span><span class="sxs-lookup"><span data-stu-id="99b57-130">Click the **Subscription Settings** tab, and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="99b57-131">[![áskriftarstillingaflipi](./media/ssrs-config-manager-11.png)](./media/ssrs-config-manager-11.png)</span><span class="sxs-lookup"><span data-stu-id="99b57-131">[![subscription settings tab](./media/ssrs-config-manager-11.png)](./media/ssrs-config-manager-11.png)</span></span>
    
  <span data-ttu-id="99b57-132">Ekki breyta sjálfgefnum stillingum á flipanum **Uppsetning útvíkkunar**. [![flipinn uppsetning útvíkkunar](./media/ssrs-config-manager-12.png)](./media/ssrs-config-manager-12.png)</span><span class="sxs-lookup"><span data-stu-id="99b57-132">Don’t change the default settings on the **Scale-out Deployment** tab. [![scale-out deployment tab](./media/ssrs-config-manager-12.png)](./media/ssrs-config-manager-12.png)</span></span>
    
  <span data-ttu-id="99b57-133">Ekki breyta sjálfgefnum stillingum á flipanum **Power BI samþætting**. [![flipinn Power BI samþætting](./media/ssrs-config-manager-13.png)](./media/ssrs-config-manager-13.png)</span><span class="sxs-lookup"><span data-stu-id="99b57-133">Don’t change the default settings on the **Power BI Integration** tab. [![power bi integration tab](./media/ssrs-config-manager-13.png)](./media/ssrs-config-manager-13.png)</span></span> 
    
13. <span data-ttu-id="99b57-134">Smelltu á **Hætta** til að loka **grunnstillingarstjóra skýrslugerðarþjónustu.**.</span><span class="sxs-lookup"><span data-stu-id="99b57-134">Click **Exit** to close the **Reporting Services Configuration Manager**.</span></span>

    <span data-ttu-id="99b57-135">[![loka grunnstillingarstjóra skýrslugerðarþjónustu](./media/ssrs-config-manager-14.png)](./media/ssrs-config-manager-14.png)</span><span class="sxs-lookup"><span data-stu-id="99b57-135">[![close reporting services configuration manager](./media/ssrs-config-manager-14.png)](./media/ssrs-config-manager-14.png)</span></span>
    


