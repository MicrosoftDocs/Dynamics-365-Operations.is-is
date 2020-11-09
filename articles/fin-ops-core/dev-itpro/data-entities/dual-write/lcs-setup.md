---
title: Tvöfaldur skrifa uppsetning frá Lifecycle Services
description: Þetta efni útskýrir hvernig á að setja upp tvískipt tengsl milli nýs umhverfis Finance and Operations og nýs umhverfis Common Data Service úr Microsoft Dynamics Lifecycle Services (LCS).
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: f49eba1748861af6ee3353a6c58005ee84ccae23
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "3998109"
---
# <a name="dual-write-setup-from-lifecycle-services"></a><span data-ttu-id="84e53-103">Tvöfaldur skrifa uppsetning frá Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="84e53-103">Dual-write setup from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="84e53-104">Þetta efni útskýrir hvernig á að setja upp tvískipt tengsl milli nýs umhverfis Finance and Operations og nýs umhverfis Common Data Service úr Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="84e53-104">This topic explains how to set up a dual-write connection between a new Finance and Operations environment and a new Common Data Service environment from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="84e53-105">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="84e53-105">Prerequisites</span></span>

<span data-ttu-id="84e53-106">Þú verður að vera stjórnandi til að setja upp tvískipt tengingu.</span><span class="sxs-lookup"><span data-stu-id="84e53-106">You must be an admin to set up a dual-write connection.</span></span>

+ <span data-ttu-id="84e53-107">Þú verður að hafa aðgang að leigjandanum.</span><span class="sxs-lookup"><span data-stu-id="84e53-107">You must have access to the tenant.</span></span>
+ <span data-ttu-id="84e53-108">Þú verður að vera stjórnandi í bæði umhverfi Finance and Operations og umhverfi Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="84e53-108">You must be an admin in both Finance and Operations environments and Common Data Service environments.</span></span>

## <a name="set-up-a-dual-write-connection"></a><span data-ttu-id="84e53-109">Setja upp tvískipt tengingu</span><span class="sxs-lookup"><span data-stu-id="84e53-109">Set up a dual-write connection</span></span>

<span data-ttu-id="84e53-110">Fylgið eftirfarandi skrefum til að setja tvískipta tengingu.</span><span class="sxs-lookup"><span data-stu-id="84e53-110">Follow these steps to set up the dual-write connection.</span></span>

1. <span data-ttu-id="84e53-111">Í LCS skaltu fara í verkið.</span><span class="sxs-lookup"><span data-stu-id="84e53-111">In LCS, go to your project.</span></span>
2. <span data-ttu-id="84e53-112">Veldu **Stilla** til að beita nýju umhverfi.</span><span class="sxs-lookup"><span data-stu-id="84e53-112">Select **Configure** to deploy a new environment.</span></span>
3. <span data-ttu-id="84e53-113">Veldu útgáfuna.</span><span class="sxs-lookup"><span data-stu-id="84e53-113">Select the version.</span></span> 
4. <span data-ttu-id="84e53-114">Veldu grannfræði.</span><span class="sxs-lookup"><span data-stu-id="84e53-114">Select the topology.</span></span> <span data-ttu-id="84e53-115">Ef aðeins ein grannfræði er tiltæk er hún sjálfkrafa valin.</span><span class="sxs-lookup"><span data-stu-id="84e53-115">If only one topology is available, it's automatically selected.</span></span>
5. <span data-ttu-id="84e53-116">Ljúktu við fyrstu skrefin í leiðsagnarforritinu **Uppsetningarstillingar**.</span><span class="sxs-lookup"><span data-stu-id="84e53-116">Complete the first steps in the **Deployment settings** wizard.</span></span>
6. <span data-ttu-id="84e53-117">Á flipaum **Common Data Service** fylgirðu einu af eftirfarandi skrefum:</span><span class="sxs-lookup"><span data-stu-id="84e53-117">On the **Common Data Service** tab, follow one of these steps:</span></span>

    - <span data-ttu-id="84e53-118">Ef umhverfið Common Data Service er þegar veitt fyrir leigjanda þinn getur þú valið það.</span><span class="sxs-lookup"><span data-stu-id="84e53-118">If a Common Data Service environment is already provisioned for your tenant, you can select it.</span></span>

        1. <span data-ttu-id="84e53-119">Stillið valkostinn **Stilla Common Data Service** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="84e53-119">Set the **Configure Common Data Service** option to **Yes**.</span></span>
        2. <span data-ttu-id="84e53-120">Í reitnum **Aðgengilegt umhverfi** velurðu umhverfið sem á að samþætta við Finance and Operations-gögnin þín.</span><span class="sxs-lookup"><span data-stu-id="84e53-120">In the **Available environments** field, select the environment to integrate with your Finance and Operations data.</span></span> <span data-ttu-id="84e53-121">Listinn inniheldur öll umhverfi þar sem þú hefur stjórnunarréttindi.</span><span class="sxs-lookup"><span data-stu-id="84e53-121">The list includes all environments where you have admin privileges.</span></span>
        3. <span data-ttu-id="84e53-122">Veldu gátreitinn **Samþykki** til að gefa til kynna að þú samþykkir skilmálana.</span><span class="sxs-lookup"><span data-stu-id="84e53-122">Select the **Agree** check box to indicate that you agree to the terms and conditions.</span></span>

        ![Flipinn Common Data Service þegar umhverfið Common Data Service er þegar veitt fyrir leigjandann](../dual-write/media/lcs_setup_1.png)

    - <span data-ttu-id="84e53-124">Ef leigjandi þinn er ekki þegar með Common Data Service umhverfi verður nýtt umhverfi veitt.</span><span class="sxs-lookup"><span data-stu-id="84e53-124">If your tenant doesn't already have a Common Data Service environment, a new environment will be provisioned.</span></span>

        1. <span data-ttu-id="84e53-125">Stillið valkostinn **Stilla Common Data Service** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="84e53-125">Set the **Configure Common Data Service** option to **Yes**.</span></span>
        2. <span data-ttu-id="84e53-126">Slá inn heiti fyrir umhverfi Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="84e53-126">Enter a name for the Common Data Service environment.</span></span>
        3. <span data-ttu-id="84e53-127">Veldu svæðið til að dreifa umhverfinu á.</span><span class="sxs-lookup"><span data-stu-id="84e53-127">Select the region to deploy the environment in.</span></span>
        4. <span data-ttu-id="84e53-128">Veldu sjálfgefið tungumál og gjaldmiðil fyrir umhverfið.</span><span class="sxs-lookup"><span data-stu-id="84e53-128">Select the default language and currency for the environment.</span></span>

            > [!NOTE]
            > <span data-ttu-id="84e53-129">Þú getur ekki breytt tungumálinu og gjaldmiðlinum seinna.</span><span class="sxs-lookup"><span data-stu-id="84e53-129">You can't change the language and currency later.</span></span>

        5. <span data-ttu-id="84e53-130">Veldu gátreitinn **Samþykki** til að gefa til kynna að þú samþykkir skilmálana.</span><span class="sxs-lookup"><span data-stu-id="84e53-130">Select the **Agree** check box to indicate that you agree to the terms and conditions.</span></span>

        ![Common Data Service flipann þegar leigjandi þinn er ekki þegar með Common Data Service umhverfi](../dual-write/media/lcs_setup_2.png)

7. <span data-ttu-id="84e53-132">Ljúktu við eftirstandandi skrefin í leiðsagnarforritinu **Uppsetningarstillingar**.</span><span class="sxs-lookup"><span data-stu-id="84e53-132">Complete the remaining steps in the **Deployment settings** wizard.</span></span>
8. <span data-ttu-id="84e53-133">Þegar umhverfið hefur stöðuna **Uppsett** skaltu opna síðuna umhverfisupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="84e53-133">After the environment has a status of **Deployed** , open the environment details page.</span></span> <span data-ttu-id="84e53-134">Hlutinn **Common Data Service upplýsingar um umhverfi** sýnir nöfn í Finance and Operations umhverfi og Common Data Service umhverfi sem eru tengd.</span><span class="sxs-lookup"><span data-stu-id="84e53-134">The **Common Data Service environment information** section shows the names of the Finance and Operations environment and the Common Data Service environment that are linked.</span></span>

    ![Common Data Service kafla um umhverfisupplýsingar](../dual-write/media/lcs_setup_3.png)

9. <span data-ttu-id="84e53-136">Stjórnandi í Finance and Operations umhverfi verður að skrá sig inn á LCS og velja **Hlekkur á CDS fyrir forrit** til að ljúka við tengilinn.</span><span class="sxs-lookup"><span data-stu-id="84e53-136">An admin of the Finance and Operations environment must sign in to LCS and select **Link to CDS for Apps** to complete the link.</span></span> <span data-ttu-id="84e53-137">Umhverfisupplýsingasíðan sýnir upplýsingar um tengilið stjórnanda.</span><span class="sxs-lookup"><span data-stu-id="84e53-137">The environment details page shows the admin's contact information.</span></span>

    <span data-ttu-id="84e53-138">Eftir að hlekknum er lokið er staðan uppfærð til **Umhverfistengingu lokið**.</span><span class="sxs-lookup"><span data-stu-id="84e53-138">After the link is completed, the status is updated to **Environment linking successfully completed**.</span></span>

10. <span data-ttu-id="84e53-139">Til að opna vinnusvæðið **Sameining gagna** í Finance and Operations umhverfi og stjórna sniðmátunum sem eru í boði, veldu **Hlekkur á CDS fyrir forrit**.</span><span class="sxs-lookup"><span data-stu-id="84e53-139">To open the **Data integration** workspace in the Finance and Operations environment and control the templates that are available, select **Link to CDS for Apps**.</span></span>

    ![Hlekkur á hnappinn CDS for Apps í Common Data Service kafla um umhverfisupplýsingar](../dual-write/media/lcs_setup_4.png)

> [!NOTE]
> <span data-ttu-id="84e53-141">Þú getur ekki aftengt umhverfi með því að nota LCS.</span><span class="sxs-lookup"><span data-stu-id="84e53-141">You can't unlink environments by using LCS.</span></span> <span data-ttu-id="84e53-142">Til að aftengja umhverfi skaltu opna vinnusvæðið **Gagnasamþætting** í Finance and Operations umhverfi og veldu síðan **Aftengja**.</span><span class="sxs-lookup"><span data-stu-id="84e53-142">To unlink an environment, open the **Data integration** workspace in the Finance and Operations environment, and then select **Unlink**.</span></span>
