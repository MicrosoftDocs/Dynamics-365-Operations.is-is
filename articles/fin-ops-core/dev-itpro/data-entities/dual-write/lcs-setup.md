---
title: Uppsetning tvöfaldra skrifa úr Lifecycle Services
description: Í þessu efnisatriði er útskýrt hvernig á að setja upp tengingu tvöfaldrar skráningar úr Microsoft Dynamics Lifecycle Services (LCS).
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
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
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 6971c8e2d5fa03c2991b9a3054c638cff6322c8b
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567721"
---
# <a name="dual-write-setup-from-lifecycle-services"></a><span data-ttu-id="119ce-103">Uppsetning tvöfaldra skrifa úr Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="119ce-103">Dual-write setup from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="119ce-104">Þetta efni útskýrir hvernig á að setja upp tvískipt tengsl milli nýs umhverfis Finance and Operations og nýs umhverfis Dataverse úr Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="119ce-104">This topic explains how to set up a dual-write connection between a new Finance and Operations environment and a new Dataverse environment from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="119ce-105">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="119ce-105">Prerequisites</span></span>

<span data-ttu-id="119ce-106">Þú verður að vera stjórnandi til að setja upp tvískipt tengingu.</span><span class="sxs-lookup"><span data-stu-id="119ce-106">You must be an admin to set up a dual-write connection.</span></span>

+ <span data-ttu-id="119ce-107">Þú verður að hafa aðgang að leigjandanum.</span><span class="sxs-lookup"><span data-stu-id="119ce-107">You must have access to the tenant.</span></span>
+ <span data-ttu-id="119ce-108">Þú verður að vera stjórnandi í bæði umhverfi Finance and Operations og umhverfi Dataverse.</span><span class="sxs-lookup"><span data-stu-id="119ce-108">You must be an admin in both Finance and Operations environments and Dataverse environments.</span></span>

## <a name="set-up-a-dual-write-connection"></a><span data-ttu-id="119ce-109">Setja upp tvískipt tengingu</span><span class="sxs-lookup"><span data-stu-id="119ce-109">Set up a dual-write connection</span></span>

<span data-ttu-id="119ce-110">Fylgið eftirfarandi skrefum til að setja tvískipta tengingu.</span><span class="sxs-lookup"><span data-stu-id="119ce-110">Follow these steps to set up the dual-write connection.</span></span>

1. <span data-ttu-id="119ce-111">Í LCS skaltu fara í verkið.</span><span class="sxs-lookup"><span data-stu-id="119ce-111">In LCS, go to your project.</span></span>
2. <span data-ttu-id="119ce-112">Veldu **Stilla** til að beita nýju umhverfi.</span><span class="sxs-lookup"><span data-stu-id="119ce-112">Select **Configure** to deploy a new environment.</span></span>
3. <span data-ttu-id="119ce-113">Veldu útgáfuna.</span><span class="sxs-lookup"><span data-stu-id="119ce-113">Select the version.</span></span> 
4. <span data-ttu-id="119ce-114">Veldu grannfræði.</span><span class="sxs-lookup"><span data-stu-id="119ce-114">Select the topology.</span></span> <span data-ttu-id="119ce-115">Ef aðeins ein grannfræði er tiltæk er hún sjálfkrafa valin.</span><span class="sxs-lookup"><span data-stu-id="119ce-115">If only one topology is available, it's automatically selected.</span></span>
5. <span data-ttu-id="119ce-116">Ljúktu við fyrstu skrefin í leiðsagnarforritinu **Uppsetningarstillingar**.</span><span class="sxs-lookup"><span data-stu-id="119ce-116">Complete the first steps in the **Deployment settings** wizard.</span></span>
6. <span data-ttu-id="119ce-117">Á flipaum **Dataverse** fylgirðu einu af eftirfarandi skrefum:</span><span class="sxs-lookup"><span data-stu-id="119ce-117">On the **Dataverse** tab, follow one of these steps:</span></span>

    - <span data-ttu-id="119ce-118">Ef umhverfið Dataverse er þegar veitt fyrir leigjanda þinn getur þú valið það.</span><span class="sxs-lookup"><span data-stu-id="119ce-118">If a Dataverse environment is already provisioned for your tenant, you can select it.</span></span>

        1. <span data-ttu-id="119ce-119">Stillið valkostinn **Stilla Dataverse** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="119ce-119">Set the **Configure Dataverse** option to **Yes**.</span></span>
        2. <span data-ttu-id="119ce-120">Í dálkinum **Tiltæk umhverfi** skal velja umhverfið sem á að samþætta við Finance and Operations gögnin.</span><span class="sxs-lookup"><span data-stu-id="119ce-120">In the **Available environments** column, select the environment to integrate with your Finance and Operations data.</span></span> <span data-ttu-id="119ce-121">Listinn inniheldur öll umhverfi þar sem þú hefur stjórnunarréttindi.</span><span class="sxs-lookup"><span data-stu-id="119ce-121">The list includes all environments where you have admin privileges.</span></span>
        3. <span data-ttu-id="119ce-122">Veldu gátreitinn **Samþykki** til að gefa til kynna að þú samþykkir skilmálana.</span><span class="sxs-lookup"><span data-stu-id="119ce-122">Select the **Agree** check box to indicate that you agree to the terms and conditions.</span></span>

        ![Flipinn Dataverse þegar umhverfið Dataverse er þegar veitt fyrir leigjandann](../dual-write/media/lcs_setup_1.png)

    - <span data-ttu-id="119ce-124">Ef leigjandi þinn er ekki þegar með Dataverse umhverfi verður nýtt umhverfi veitt.</span><span class="sxs-lookup"><span data-stu-id="119ce-124">If your tenant doesn't already have a Dataverse environment, a new environment will be provisioned.</span></span>

        1. <span data-ttu-id="119ce-125">Stillið valkostinn **Stilla Dataverse** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="119ce-125">Set the **Configure Dataverse** option to **Yes**.</span></span>
        2. <span data-ttu-id="119ce-126">Slá inn heiti fyrir umhverfi Dataverse.</span><span class="sxs-lookup"><span data-stu-id="119ce-126">Enter a name for the Dataverse environment.</span></span>
        3. <span data-ttu-id="119ce-127">Veldu svæðið til að dreifa umhverfinu á.</span><span class="sxs-lookup"><span data-stu-id="119ce-127">Select the region to deploy the environment in.</span></span>
        4. <span data-ttu-id="119ce-128">Veldu sjálfgefið tungumál og gjaldmiðil fyrir umhverfið.</span><span class="sxs-lookup"><span data-stu-id="119ce-128">Select the default language and currency for the environment.</span></span>

            > [!NOTE]
            > <span data-ttu-id="119ce-129">Þú getur ekki breytt tungumálinu og gjaldmiðlinum seinna.</span><span class="sxs-lookup"><span data-stu-id="119ce-129">You can't change the language and currency later.</span></span>

        5. <span data-ttu-id="119ce-130">Veldu gátreitinn **Samþykki** til að gefa til kynna að þú samþykkir skilmálana.</span><span class="sxs-lookup"><span data-stu-id="119ce-130">Select the **Agree** check box to indicate that you agree to the terms and conditions.</span></span>

        ![Dataverse flipann þegar leigjandi þinn er ekki þegar með Dataverse umhverfi](../dual-write/media/lcs_setup_2.png)

7. <span data-ttu-id="119ce-132">Ljúktu við eftirstandandi skrefin í leiðsagnarforritinu **Uppsetningarstillingar**.</span><span class="sxs-lookup"><span data-stu-id="119ce-132">Complete the remaining steps in the **Deployment settings** wizard.</span></span>
8. <span data-ttu-id="119ce-133">Þegar umhverfið hefur stöðuna **Uppsett** skaltu opna síðuna umhverfisupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="119ce-133">After the environment has a status of **Deployed**, open the environment details page.</span></span> <span data-ttu-id="119ce-134">Kaflinn **Power Platform Samþætting** sýnir heiti Finance and Operations umhverfisins og Dataverse umhverfis sem er tengt.</span><span class="sxs-lookup"><span data-stu-id="119ce-134">The **Power Platform Integration** section shows the names of the Finance and Operations environment and the Dataverse environment that are linked.</span></span>

    ![Power Platform Hluti samþættingar](../dual-write/media/lcs_setup_3.png)

9. <span data-ttu-id="119ce-136">Stjórnandi í Finance and Operations umhverfi verður að skrá sig inn á LCS og velja **Hlekkur á CDS fyrir forrit** til að ljúka við tengilinn.</span><span class="sxs-lookup"><span data-stu-id="119ce-136">An admin of the Finance and Operations environment must sign in to LCS and select **Link to CDS for Apps** to complete the link.</span></span> <span data-ttu-id="119ce-137">Umhverfisupplýsingasíðan sýnir upplýsingar um tengilið stjórnanda.</span><span class="sxs-lookup"><span data-stu-id="119ce-137">The environment details page shows the admin's contact information.</span></span>

    <span data-ttu-id="119ce-138">Eftir að hlekknum er lokið er staðan uppfærð til **Umhverfistengingu lokið**.</span><span class="sxs-lookup"><span data-stu-id="119ce-138">After the link is completed, the status is updated to **Environment linking successfully completed**.</span></span>

10. <span data-ttu-id="119ce-139">Til að opna vinnusvæðið **Sameining gagna** í Finance and Operations umhverfi og stjórna sniðmátunum sem eru í boði, veldu **Hlekkur á CDS fyrir forrit**.</span><span class="sxs-lookup"><span data-stu-id="119ce-139">To open the **Data integration** workspace in the Finance and Operations environment and control the templates that are available, select **Link to CDS for Apps**.</span></span>

    ![Tengill á CDS fyrir forritahnapp í Power Platform samþættingarhlutanum](../dual-write/media/lcs_setup_4.png)

> [!NOTE]
> <span data-ttu-id="119ce-141">Þú getur ekki aftengt umhverfi með því að nota LCS.</span><span class="sxs-lookup"><span data-stu-id="119ce-141">You can't unlink environments by using LCS.</span></span> <span data-ttu-id="119ce-142">Til að aftengja umhverfi skaltu opna vinnusvæðið **Gagnasamþætting** í Finance and Operations umhverfi og veldu síðan **Aftengja**.</span><span class="sxs-lookup"><span data-stu-id="119ce-142">To unlink an environment, open the **Data integration** workspace in the Finance and Operations environment, and then select **Unlink**.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]