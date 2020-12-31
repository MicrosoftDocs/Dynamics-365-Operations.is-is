---
title: Stofna verk til að setja upp samþættingu gagna (forskoðun)
description: Þetta efnisatriði útskýrir hvernig á að stofna erk til að setja upp samþættingu gagna.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: fb17d5e82709a34ff088774d9e9034adb714b58c
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646254"
---
# <a name="create-a-data-integrator-project-preview"></a><span data-ttu-id="4038a-103">Stofna verk til að setja upp samþættingu gagna (forskoðun)</span><span class="sxs-lookup"><span data-stu-id="4038a-103">Create a data integrator project (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="4038a-104">Þetta efnisatriði útskýrir hvernig á að stofna erk til að setja upp samþættingu gagna.</span><span class="sxs-lookup"><span data-stu-id="4038a-104">This topic explains how to create a data integrator project.</span></span>

1. <span data-ttu-id="4038a-105">Skrá inn á Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="4038a-105">Sign in to Microsoft Dynamics 365 Finance.</span></span>
2. <span data-ttu-id="4038a-106">Farið á **Vinnusvæði\> Gagnastjórnun** og veljið **Gagnaeiningar**.</span><span class="sxs-lookup"><span data-stu-id="4038a-106">Go to **Workspaces \> Data management**, and select **Data entities**.</span></span> <span data-ttu-id="4038a-107">Bíða skal þar til allir gagnaeiningarnar hafa verið uppfærðar áður en farið er í næsta skref.</span><span class="sxs-lookup"><span data-stu-id="4038a-107">Wait until all the data entities have been refreshed before you move on to the next step.</span></span>
3. <span data-ttu-id="4038a-108">Opnaðu [Power Apps gáttina](https://make.powerapps.com/) og fylgdu eftirfarandi skrefum:</span><span class="sxs-lookup"><span data-stu-id="4038a-108">Open the [Power Apps portal](https://make.powerapps.com/), and follow these steps:</span></span>

    1. <span data-ttu-id="4038a-109">Veljið viðeigandi umhverfi.</span><span class="sxs-lookup"><span data-stu-id="4038a-109">Select the appropriate environment.</span></span>
    2. <span data-ttu-id="4038a-110">Á vinstra yfirlitssvæðinu skal velja **Gagna \> Tengingar**.</span><span class="sxs-lookup"><span data-stu-id="4038a-110">In the left navigation pane, select **Data \> Connections**.</span></span>
    3. <span data-ttu-id="4038a-111">Tengjast við viðeigandi tilvik eftirfarandi atriða:</span><span class="sxs-lookup"><span data-stu-id="4038a-111">Connect to appropriate instances of the following items:</span></span>

        - <span data-ttu-id="4038a-112">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="4038a-112">Dynamics 365</span></span>
        - <span data-ttu-id="4038a-113">Dynamics 365 fyrir fin & Ops</span><span class="sxs-lookup"><span data-stu-id="4038a-113">Dynamics 365 for Fin & Ops</span></span>

4. <span data-ttu-id="4038a-114">Opnið [Power Apps umhverfi](https://admin.powerapps.com/environments) og fylgið eftirfarandi skrefum:</span><span class="sxs-lookup"><span data-stu-id="4038a-114">Open the [Power Apps environments](https://admin.powerapps.com/environments), and follow these steps:</span></span>

    1. <span data-ttu-id="4038a-115">Veljið **Data Integrator**.</span><span class="sxs-lookup"><span data-stu-id="4038a-115">Select **Data Integrator**.</span></span>
    2. <span data-ttu-id="4038a-116">Veljið **Tengingasett**.</span><span class="sxs-lookup"><span data-stu-id="4038a-116">Select **Connection sets**.</span></span>
    3. <span data-ttu-id="4038a-117">Veljið **Nýtt tengingasett**.</span><span class="sxs-lookup"><span data-stu-id="4038a-117">Select **New connection set**.</span></span>
    4. <span data-ttu-id="4038a-118">Færa skal inn heiti fyrir tenginguna.</span><span class="sxs-lookup"><span data-stu-id="4038a-118">Enter a name for the connection.</span></span>
    5. <span data-ttu-id="4038a-119">Velja viðeigandi tengingar fyrir eftirfarandi atriði:</span><span class="sxs-lookup"><span data-stu-id="4038a-119">Select the appropriate connections for the following items:</span></span>

        - <span data-ttu-id="4038a-120">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="4038a-120">Dynamics 365</span></span>
        - <span data-ttu-id="4038a-121">Dynamics 365 fyrir fin & Ops</span><span class="sxs-lookup"><span data-stu-id="4038a-121">Dynamics 365 for Fin & Ops</span></span>

    6. <span data-ttu-id="4038a-122">Veljið viðeigandi fyrirtækjavörpun.</span><span class="sxs-lookup"><span data-stu-id="4038a-122">Select the appropriate organization mapping.</span></span>
    7. <span data-ttu-id="4038a-123">Velja **Stofna**.</span><span class="sxs-lookup"><span data-stu-id="4038a-123">Select **Create**.</span></span>

5. <span data-ttu-id="4038a-124">Opnið [Power Apps umhverfi](https://admin.powerapps.com/environments) og fylgið eftirfarandi skrefum:</span><span class="sxs-lookup"><span data-stu-id="4038a-124">Open the [Power Apps environments](https://admin.powerapps.com/environments), and follow these steps:</span></span>  

    1. <span data-ttu-id="4038a-125">Stofna gagnasamþættingarverk fyrir eftirfarandi sniðmát með því að nota tengingarsett sem var verið að stofna:</span><span class="sxs-lookup"><span data-stu-id="4038a-125">Create data integration projects for the following templates by using the connection set that you just created:</span></span>

        - <span data-ttu-id="4038a-126">Niðurstöður innsýnar í greiðslur viðskiptavinar (CDS til Fin og Ops)</span><span class="sxs-lookup"><span data-stu-id="4038a-126">Customer payment insights results (CDS to Fin and Ops)</span></span>
        - <span data-ttu-id="4038a-127">Niðurstöður úr tímaröð sjóðsstreymis (CDS til Fin og Ops)</span><span class="sxs-lookup"><span data-stu-id="4038a-127">Cash flow time series results (CDS to Fin and Ops)</span></span>
        - <span data-ttu-id="4038a-128">Niðurstöður tímaraðar fjárhagsáætlunar (CDS til Fin og Ops)</span><span class="sxs-lookup"><span data-stu-id="4038a-128">Budget time series results (CDS to Fin and Ops)</span></span>

    2. <span data-ttu-id="4038a-129">Stillið viðeigandi áætlanagerð fyrir hvert verk.</span><span class="sxs-lookup"><span data-stu-id="4038a-129">Set the appropriate scheduling for each project.</span></span>

> [!NOTE]
> <span data-ttu-id="4038a-130">Ef áskildar einingar eru ekki til staðar í CDS skal fara í **Skuldir og innheimta > Uppsetning > Fjármálainnsýn > Færibreytur fjármálainnsýnar**, virkja eiginleikann „Greiðsluspár viðskiptavinar“ og smella á hnappinn **Búa til spárlíkan**.</span><span class="sxs-lookup"><span data-stu-id="4038a-130">If you do not see the required entities in CDS, please go to **Credit and collections > Setup > Finance Insights > Finance insights parameters**, enable Customer payment predictions feature and click on **Create prediction model** button.</span></span> <span data-ttu-id="4038a-131">Þegar innleiðingu á AI-líkani er lokið (tókst eða mistókst) eru CDS-einingarnar sem nauðsynlegar eru fyrir samþættingu settar upp í í CDS.</span><span class="sxs-lookup"><span data-stu-id="4038a-131">When the deployment of AI model is completed (successful or failed), the CDS entities needed to create integration will be deployed in CDS.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="4038a-132">Tilkynning um persónuvernd</span><span class="sxs-lookup"><span data-stu-id="4038a-132">Privacy notice</span></span>

<span data-ttu-id="4038a-133">Forútgáfur (1) kunna að nota minni persónuverndar- og öryggisráðstafanir og þjónusta Dynamics 365 Finance and Operations, (2) eru ekki hluti af þjónustustigssamningi fyrir þessa þjónustu, (3) ættu ekki að vera notaðar til að vinna úr persónulegum gögnum eða öðrum gögnum sem falla undir lögboðnar kröfur eða reglur um samræmi og (4) hafa takmarkaðan stuðning.</span><span class="sxs-lookup"><span data-stu-id="4038a-133">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>
