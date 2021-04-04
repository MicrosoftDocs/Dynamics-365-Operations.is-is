---
title: Skilgreina SQL Server Reporting Services fyrir staðbundna uppsetningu
description: Þetta efnisatriði veitir upplýsingar um grunnstillingu á SQL Server Reporting Services (SSRS) fyrir virkjun á staðnum.
author: PeterRFriis
manager: AnnBe
ms.date: 06/23/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 55651
ms.assetid: ''
ms.search.region: Global
ms.author: peterfriis
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.openlocfilehash: cc8bb6c3a993274f70316145f2ec8a6217e6886c
ms.sourcegitcommit: d7c18228256daeefbf6518c3ef82fed4f7dbc161
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5571705"
---
# <a name="configure-sql-server-reporting-services-for-on-premises-deployments"></a><span data-ttu-id="06ad3-103">Skilgreina SQL Server Reporting Services fyrir staðbundna uppsetningu</span><span class="sxs-lookup"><span data-stu-id="06ad3-103">Configure SQL Server Reporting Services for on-premises deployments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="06ad3-104">Notið skrefin í þessu efnisatriði til að grunnstilla SQL Server Reporting Services (SSRS) fyrir virkjun Microsoft Dynamics 365 Finance + Operations (á staðnum).</span><span class="sxs-lookup"><span data-stu-id="06ad3-104">Use the steps in this topic to configure SQL Server Reporting Services (SSRS) for your Microsoft Dynamics 365 Finance + Operations (on-premises) deployment.</span></span>

1. <span data-ttu-id="06ad3-105">Opnaðu grunnstillingarstjóra skýrslugerðarþjónustu.</span><span class="sxs-lookup"><span data-stu-id="06ad3-105">Open the Reporting Services Configuration Manager application.</span></span>
2. <span data-ttu-id="06ad3-106">Skildu eftir sjálfgefið **Þjónsnafn**, sem ætti að vera nafn vélarinnar sem er í notkun, og **Heiti skýrsluþjónstilviks**, **MSSQLSERVER**.</span><span class="sxs-lookup"><span data-stu-id="06ad3-106">Leave the default **Server name**, which should be the name of the current machine, and the **Report Server Instance**, **MSSQLSERVER**.</span></span>
3. <span data-ttu-id="06ad3-107">Smelltu á **Tengja**.</span><span class="sxs-lookup"><span data-stu-id="06ad3-107">Click **Connect**.</span></span>

    <span data-ttu-id="06ad3-108">[![Grunnstillingartenging skýrslugerðarþjónustu](./media/ssrs-config-manager-01.png)](./media/ssrs-config-manager-01.png)</span><span class="sxs-lookup"><span data-stu-id="06ad3-108">[![Reporting services configuration connection](./media/ssrs-config-manager-01.png)](./media/ssrs-config-manager-01.png)</span></span>

4. <span data-ttu-id="06ad3-109">Smellið á flipann **Þjónustureikningur** og sannreynið að stillingarnar passi við eftirfarandi mynd.</span><span class="sxs-lookup"><span data-stu-id="06ad3-109">Click the **Service Account** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="06ad3-110">[![Þjónustureikningsflipi](./media/ssrs-config-manager-02.png)](./media/ssrs-config-manager-02.png)</span><span class="sxs-lookup"><span data-stu-id="06ad3-110">[![Service account tab](./media/ssrs-config-manager-02.png)](./media/ssrs-config-manager-02.png)</span></span>

5. <span data-ttu-id="06ad3-111">Smellið á flipann **Vefþjónustuslóð** og sannreynið að stillingarnar passi við eftirfarandi mynd.</span><span class="sxs-lookup"><span data-stu-id="06ad3-111">Click the **Web Service URL** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="06ad3-112">[![Flipi vefþjónustuslóðar](./media/ssrs-config-manager-03.png)](./media/ssrs-config-manager-03.png)</span><span class="sxs-lookup"><span data-stu-id="06ad3-112">[![Web service URL tab](./media/ssrs-config-manager-03.png)](./media/ssrs-config-manager-03.png)</span></span>

6. <span data-ttu-id="06ad3-113">Smellið á flipann **Gagnagrunnur** og sannreynið að **Gagnagrunnsnafn** og **Skilríkjastillingar** passi við eftirfarandi mynd.</span><span class="sxs-lookup"><span data-stu-id="06ad3-113">Click the **Database** tab and verify that the **Database Name** and **Credential settings** match the following graphic.</span></span>

    > [!NOTE]
    > <span data-ttu-id="06ad3-114">Þú þarft að búa til nýjan gagnagrunn.</span><span class="sxs-lookup"><span data-stu-id="06ad3-114">You will need to create a new database.</span></span> <span data-ttu-id="06ad3-115">Til að gera það skal smella á **Breyta gagnagrunni** og staðfest að nýja gagnagrunnsnafnið sé: **DynamicsAxReportServer**.</span><span class="sxs-lookup"><span data-stu-id="06ad3-115">To do this, click **Change Database**, and then verify that the new database name is: **DynamicsAxReportServer**.</span></span>

    <span data-ttu-id="06ad3-116">[![gagnagrunnsflipi](./media/ssrs-config-manager-04.png)](./media/ssrs-config-manager-04.png)</span><span class="sxs-lookup"><span data-stu-id="06ad3-116">[![database tab](./media/ssrs-config-manager-04.png)](./media/ssrs-config-manager-04.png)</span></span>

7. <span data-ttu-id="06ad3-117">Smellið á flipann **Vefgáttarslóð** og sannreynið að stillingarnar passi við eftirfarandi mynd.</span><span class="sxs-lookup"><span data-stu-id="06ad3-117">Click the **Web Portal URL** tab and verify that the settings match the following graphic.</span></span>

    > [!NOTE]
    > <span data-ttu-id="06ad3-118">Nauðsynlegt er að smella á **Nota** til að búa til og skilgreina gáttina almennilega.</span><span class="sxs-lookup"><span data-stu-id="06ad3-118">You must click **Apply** to create and properly configure the Portal.</span></span>

    <span data-ttu-id="06ad3-119">[![flipi vefgáttarslóðar](./media/ssrs-config-manager-05.png)](./media/ssrs-config-manager-05.png)</span><span class="sxs-lookup"><span data-stu-id="06ad3-119">[![web portal url tab](./media/ssrs-config-manager-05.png)](./media/ssrs-config-manager-05.png)</span></span>

    <span data-ttu-id="06ad3-120">Eftir að gáttin er grunnstillt passar flipinn **Vefgátt** við eftirfarandi mynd.</span><span class="sxs-lookup"><span data-stu-id="06ad3-120">After the Portal is configured, the **Web Portal** tab will match the following graphic.</span></span>

    <span data-ttu-id="06ad3-121">[![vefgáttarflipi](./media/ssrs-config-manager-06.png)](./media/ssrs-config-manager-06.png)</span><span class="sxs-lookup"><span data-stu-id="06ad3-121">[![web portal tab](./media/ssrs-config-manager-06.png)](./media/ssrs-config-manager-06.png)</span></span>

8. <span data-ttu-id="06ad3-122">Smelltu á skýrsluvefslóðina til að skoða vefgátt SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="06ad3-122">Click the reports URL to view the SQL Server Reporting Services web portal.</span></span>
9. <span data-ttu-id="06ad3-123">Í gáttinni skal stofna nýja möppu með nafninu **Dynamics**.</span><span class="sxs-lookup"><span data-stu-id="06ad3-123">When you are in the portal, create a new folder named **Dynamics**.</span></span>

    <span data-ttu-id="06ad3-124">[![dynamics mappa](./media/ssrs-config-manager-07.png)](./media/ssrs-config-manager-07.png)</span><span class="sxs-lookup"><span data-stu-id="06ad3-124">[![dynamics folder](./media/ssrs-config-manager-07.png)](./media/ssrs-config-manager-07.png)</span></span>

10. <span data-ttu-id="06ad3-125">Í **grunnstillingarstjóra skýrslugerðarþjónustu** skal smella á flipann **tölvupóststillingar** og sannreyna að stillingarnar passi við eftirfarandi mynd.</span><span class="sxs-lookup"><span data-stu-id="06ad3-125">In the **Reporting Services Configuration Manager**, click the **E-mail Settings** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="06ad3-126">[![tölvupóststillingaflipi](./media/ssrs-config-manager-08.png)](./media/ssrs-config-manager-08.png)</span><span class="sxs-lookup"><span data-stu-id="06ad3-126">[![email settings tab](./media/ssrs-config-manager-08.png)](./media/ssrs-config-manager-08.png)</span></span>

11. <span data-ttu-id="06ad3-127">Smellið á flipann **Keyrslureikningur** og sannreynið að stillingarnar passi við eftirfarandi mynd.</span><span class="sxs-lookup"><span data-stu-id="06ad3-127">Click the **Execution Account** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="06ad3-128">[![keyrslureikningsflipi](./media/ssrs-config-manager-09.png)](./media/ssrs-config-manager-09.png)</span><span class="sxs-lookup"><span data-stu-id="06ad3-128">[![execution account tab](./media/ssrs-config-manager-09.png)](./media/ssrs-config-manager-09.png)</span></span>

    <span data-ttu-id="06ad3-129">Ekki breyta sjálfgefnum stillingum á flipanum **Dulritunarlyklar**.</span><span class="sxs-lookup"><span data-stu-id="06ad3-129">Don't change the default settings on the **Encryption Keys** tab.</span></span>

    <span data-ttu-id="06ad3-130">[![dulritunarlyklaflipi](./media/ssrs-config-manager-10.png)](./media/ssrs-config-manager-10.png)</span><span class="sxs-lookup"><span data-stu-id="06ad3-130">[![encryption keys tab](./media/ssrs-config-manager-10.png)](./media/ssrs-config-manager-10.png)</span></span>

12. <span data-ttu-id="06ad3-131">Smellið á flipann **Áskriftarstillingar** og sannreynið að stillingarnar passi við eftirfarandi mynd.</span><span class="sxs-lookup"><span data-stu-id="06ad3-131">Click the **Subscription Settings** tab, and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="06ad3-132">[![áskriftarstillingaflipi](./media/ssrs-config-manager-11.png)](./media/ssrs-config-manager-11.png)</span><span class="sxs-lookup"><span data-stu-id="06ad3-132">[![subscription settings tab](./media/ssrs-config-manager-11.png)](./media/ssrs-config-manager-11.png)</span></span>

    <span data-ttu-id="06ad3-133">Ekki breyta sjálfgefnum stillingum á flipanum **Uppsetning útvíkkunar** flipanum.</span><span class="sxs-lookup"><span data-stu-id="06ad3-133">Don't change the default settings on the **Scale-out Deployment** tab.</span></span>

    <span data-ttu-id="06ad3-134">[![flipi útskölunarvirkjunar](./media/ssrs-config-manager-12.png)](./media/ssrs-config-manager-12.png)</span><span class="sxs-lookup"><span data-stu-id="06ad3-134">[![scale-out deployment tab](./media/ssrs-config-manager-12.png)](./media/ssrs-config-manager-12.png)</span></span>

    <span data-ttu-id="06ad3-135">Ekki breyta sjálfgefnum stillingum á flipanum **Power BI-samþætting**.</span><span class="sxs-lookup"><span data-stu-id="06ad3-135">Don't change the default settings on the **Power BI Integration** tab.</span></span>

    <span data-ttu-id="06ad3-136">[![power bi-samþættingaflipi](./media/ssrs-config-manager-13.png)](./media/ssrs-config-manager-13.png)</span><span class="sxs-lookup"><span data-stu-id="06ad3-136">[![power bi integration tab](./media/ssrs-config-manager-13.png)](./media/ssrs-config-manager-13.png)</span></span>

13. <span data-ttu-id="06ad3-137">Smelltu á **Hætta** til að loka **grunnstillingarstjóra skýrslugerðarþjónustu.**.</span><span class="sxs-lookup"><span data-stu-id="06ad3-137">Click **Exit** to close the **Reporting Services Configuration Manager**.</span></span>

    <span data-ttu-id="06ad3-138">[![loka grunnstillingarstjóra skýrslugerðarþjónustu](./media/ssrs-config-manager-14.png)](./media/ssrs-config-manager-14.png)</span><span class="sxs-lookup"><span data-stu-id="06ad3-138">[![close reporting services configuration manager](./media/ssrs-config-manager-14.png)](./media/ssrs-config-manager-14.png)</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
