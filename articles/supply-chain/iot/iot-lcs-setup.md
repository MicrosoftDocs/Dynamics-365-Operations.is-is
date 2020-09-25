---
title: Setja upp IoT-gervigreindarinnbótina í LCS
description: Þetta efnisatriði útskýrir hvernig á að setja upp IoT-gervigreind viðbótina í Microsoft Dynamics Lifecycle Services (LCS).
author: robinarh
manager: tfehr
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ae6b36c40d2f2f9e5266dfb3e2d1cbbb57755222
ms.sourcegitcommit: 5bb36b74935ffe140367fd6ecf956b4857ad12e5
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/14/2020
ms.locfileid: "3803092"
---
# <a name="install-the-iot-intelligence-add-in-in-lcs"></a><span data-ttu-id="fc2af-103">Setja upp IoT-gervigreindarinnbótina í LCS</span><span class="sxs-lookup"><span data-stu-id="fc2af-103">Install the IoT Intelligence add-in in LCS</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fc2af-104">Þetta efnisatriði útskýrir hvernig á að setja upp IoT-gervigreind viðbótina í Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="fc2af-104">This topic explains how to install the IoT Intelligence add-in in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="fc2af-105">Athugaðu að ekki er hægt að setja innbætur í kynningu/prufuumhverfi.</span><span class="sxs-lookup"><span data-stu-id="fc2af-105">Note that add-ins cannot be installed on a demo/trial environment.</span></span> <span data-ttu-id="fc2af-106">Áður en hægt er að setja upp viðbótina þarf [að stofna Azure tilföng](iot-azure-setup.md).</span><span class="sxs-lookup"><span data-stu-id="fc2af-106">Before you can install the add-in, you must [create the Azure resources](iot-azure-setup.md).</span></span>

## <a name="set-up-the-lcs-environment"></a><span data-ttu-id="fc2af-107">Setja upp LCS-umhverfi</span><span class="sxs-lookup"><span data-stu-id="fc2af-107">Set up the LCS environment</span></span>

1. <span data-ttu-id="fc2af-108">Opnaðu LCS og farðu í Microsoft Dynamics 365 Supply Chain Management umhverfið.</span><span class="sxs-lookup"><span data-stu-id="fc2af-108">Open LCS, and go to your Microsoft Dynamics 365 Supply Chain Management environment.</span></span>
2. <span data-ttu-id="fc2af-109">Flettu að hlutanum **Innbætur umhverfis**.</span><span class="sxs-lookup"><span data-stu-id="fc2af-109">Scroll to the **Environment add-ins** section.</span></span>
3. <span data-ttu-id="fc2af-110">Veldu **Setja upp nýja innbót** til að sýna lista yfir innbætur sem hafa verið virkjaðar fyrir umhverfið.</span><span class="sxs-lookup"><span data-stu-id="fc2af-110">Select **Install a new add-in** to show the list of add-ins that have been enabled for the environment.</span></span>
4. <span data-ttu-id="fc2af-111">Í glugganum **Velja innbót til að setja upp** skal velja **IoT-gervigreind**.</span><span class="sxs-lookup"><span data-stu-id="fc2af-111">In the **Select an add-in to install** dialog box, select **IoT Intelligence**.</span></span>
5. <span data-ttu-id="fc2af-112">Í svarglugganum **Uppsetning á innbót** skal veita upplýsingar um IoT gátt og skyndiminni Redis.</span><span class="sxs-lookup"><span data-stu-id="fc2af-112">In the **Setup add-in** dialog box, provide the details of your IoT hub and Redis cache.</span></span> <span data-ttu-id="fc2af-113">Hægt er að finna nauðsynleg gildi í lyklageymslunni sem stofnuð var í [Stofna Azure-tilföng](iot-azure-setup.md).</span><span class="sxs-lookup"><span data-stu-id="fc2af-113">You can find the required values in the key vault that you created in [Create Azure resources](iot-azure-setup.md).</span></span>

    + <span data-ttu-id="fc2af-114">**Auðkenni leigjanda** – í Azure-gátt skal fara í lyklageymslu og velja síðan **Yfirlit** á vinstra yfirlitssvæði og afrita gildið **Skráasafnskenni**.</span><span class="sxs-lookup"><span data-stu-id="fc2af-114">**Tenant ID** – In the Azure portal, go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **Directory ID** value.</span></span> <span data-ttu-id="fc2af-115">Límið gildið í svarglugganum **Uppsetning á innbót**.</span><span class="sxs-lookup"><span data-stu-id="fc2af-115">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="fc2af-116">**Í samhæfri URI lyklageymslu endapunkts IoT miðstöðvar** – Farðu í lyklageymslu og veldu á vinstra yfirlitssvæðinu **Yfirlit** og afritaðu gildið **DNS-heiti**.</span><span class="sxs-lookup"><span data-stu-id="fc2af-116">**IoT Event Hub-compatible endpoint Key Vault URI** – Go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **DNS name** value.</span></span> <span data-ttu-id="fc2af-117">Límið gildið í svarglugganum **Uppsetning á innbót**.</span><span class="sxs-lookup"><span data-stu-id="fc2af-117">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="fc2af-118">**Samhæft leyniorð fyrir IoT Event Hub** – Opnaðu lyklageymsluna og á vinstra yfirlitssvæðinu velurðu **Leyniorð** og afritar leyniheiti þar sem tengistrengur IoT miðstöðvar er vistaður.</span><span class="sxs-lookup"><span data-stu-id="fc2af-118">**IoT Event Hub-compatible endpoint secret name** – Go to the key vault, and then, in the left navigation pane, select **Secrets**, and copy the name of the secret where the event hub connection string for the IoT hub is stored.</span></span> <span data-ttu-id="fc2af-119">Límið gildið í svarglugganum **Uppsetning á innbót**.</span><span class="sxs-lookup"><span data-stu-id="fc2af-119">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="fc2af-120">**URI lyklageymslu Redis skyndiminnis** – Farðu í lyklageymslu og veldu á vinstra yfirlitssvæðinu **Yfirlit** og afritaðu gildið **DNS-heiti**.</span><span class="sxs-lookup"><span data-stu-id="fc2af-120">**Redis cache key vault URI** – Go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **DNS name** value.</span></span> <span data-ttu-id="fc2af-121">Límið gildið í svarglugganum **Uppsetning á innbót**.</span><span class="sxs-lookup"><span data-stu-id="fc2af-121">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="fc2af-122">**Leyniorð endapunkts fyrir Redis skyndiminni** – Opnaðu lyklageymsluna og á vinstra yfirlitssvæðinu velurðu **Leyniorð** og afritar leyniheitið þar sem tengistrengur Redis skyndiminnis er vistaður.</span><span class="sxs-lookup"><span data-stu-id="fc2af-122">**Redis cache endpoint secret name** – Go to the key vault, and then, in the left navigation pane, select **Secrets**, and copy the name of the secret where the connection string for the Redis cache is stored.</span></span> <span data-ttu-id="fc2af-123">Límið gildið í svarglugganum **Uppsetning á innbót**.</span><span class="sxs-lookup"><span data-stu-id="fc2af-123">Paste that value in the **Setup add-in** dialog box.</span></span>

6. <span data-ttu-id="fc2af-124">Velja þarf gátreitinn til að samþykkja skilmálana.</span><span class="sxs-lookup"><span data-stu-id="fc2af-124">Select the check box to accept the terms and conditions.</span></span>
7. <span data-ttu-id="fc2af-125">Velja **Setja upp**.</span><span class="sxs-lookup"><span data-stu-id="fc2af-125">Select **Install**.</span></span>
8. <span data-ttu-id="fc2af-126">Skilaboðagluggi með skilaboðunum „Innbótin var sett í gang fyrir uppsetningu“ birtist.</span><span class="sxs-lookup"><span data-stu-id="fc2af-126">A message box appears that states, "Add-in has been successfully triggered for installation."</span></span> <span data-ttu-id="fc2af-127">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="fc2af-127">Select **OK**.</span></span>

<span data-ttu-id="fc2af-128">LCS uppsetningu er nú lokið.</span><span class="sxs-lookup"><span data-stu-id="fc2af-128">LCS setup is now completed.</span></span> <span data-ttu-id="fc2af-129">Næsta skrefið er að [setja upp aðstæður](iot-scenario-setup.md).</span><span class="sxs-lookup"><span data-stu-id="fc2af-129">The next step is to [set up the scenarios](iot-scenario-setup.md).</span></span>

## <a name="uninstall-the-add-in"></a><a id="uninstall-addin"></a><span data-ttu-id="fc2af-130">Fjarlægja innbótina</span><span class="sxs-lookup"><span data-stu-id="fc2af-130">Uninstall the add-in</span></span>

1. <span data-ttu-id="fc2af-131">Í Supply Chain Management skal [gera umhverfið óvirkt](iot-scenario-setup.md#how-to-disable-a-scenario).</span><span class="sxs-lookup"><span data-stu-id="fc2af-131">In Supply Chain Management, [disable the scenarios](iot-scenario-setup.md#how-to-disable-a-scenario).</span></span>
2. <span data-ttu-id="fc2af-132">Opnið upplýsingar umhverfis Supply Chain Management í LCS.</span><span class="sxs-lookup"><span data-stu-id="fc2af-132">In LCS, go to your Supply Chain Management environment details.</span></span>
3. <span data-ttu-id="fc2af-133">Flettu að hlutanum **Innbætur umhverfis**.</span><span class="sxs-lookup"><span data-stu-id="fc2af-133">Scroll to the **Environment add-ins** section.</span></span>
4. <span data-ttu-id="fc2af-134">Veljið **Fjarlægja** fyrir innbótina IoT-gervigreind.</span><span class="sxs-lookup"><span data-stu-id="fc2af-134">Select **Uninstall** for the IoT Intelligence add-in.</span></span>
