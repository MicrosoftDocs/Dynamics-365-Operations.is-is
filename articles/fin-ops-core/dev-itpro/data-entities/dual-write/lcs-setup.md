---
title: Uppsetning tvöfaldra skrifa úr Lifecycle Services
description: Í þessu efnisatriði er útskýrt hvernig á að setja upp tengingu tvöfaldrar skráningar úr Microsoft Dynamics Lifecycle Services (LCS).
author: RamaKrishnamoorthy
ms.date: 05/11/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: eb4170ef6cb09c862f6a4163670c519d5d8077fb
ms.sourcegitcommit: 365092f735310990e82516110141d42aaf04e654
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/27/2021
ms.locfileid: "6103570"
---
# <a name="dual-write-setup-from-lifecycle-services"></a><span data-ttu-id="ffcdb-103">Uppsetning tvöfaldra skrifa úr Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="ffcdb-103">Dual-write setup from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="ffcdb-104">Í þessu efnisatriði er útskýrt hvernig á að virkja tvöfalda skráningu úr Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="ffcdb-104">This topic explains how to enable dual-write from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ffcdb-105">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="ffcdb-105">Prerequisites</span></span>

<span data-ttu-id="ffcdb-106">Ljúka verður við Power Platform samþættinguna eins og lýst er í eftirfarandi efnum:</span><span class="sxs-lookup"><span data-stu-id="ffcdb-106">You must complete the Power Platform integration as described in the following topics:</span></span>

+ [<span data-ttu-id="ffcdb-107">Power Platform Samþætting - Virkja við uppsetningu umhverfis</span><span class="sxs-lookup"><span data-stu-id="ffcdb-107">Power Platform Integration - Enable during environment deployment</span></span>](../../power-platform/overview.md#enable-during-environment-deployment)
+ [<span data-ttu-id="ffcdb-108">Power Platform samþætting - Setja upp eftir uppsetningu umhverfis</span><span class="sxs-lookup"><span data-stu-id="ffcdb-108">Power Platform integration - Set up after environment deployment</span></span>](../../power-platform/overview.md#set-up-after-environment-deployment)

## <a name="set-up-dual-write-for-new-dataverse-environments"></a><span data-ttu-id="ffcdb-109">Setja upp tvöfalda skráningu fyrir ný Dataverse umhverfi</span><span class="sxs-lookup"><span data-stu-id="ffcdb-109">Set up dual-write for new Dataverse environments</span></span>

<span data-ttu-id="ffcdb-110">Fylgið þessum skrefum til að setja upp tvöfalda skráningu af LCS-síðunni **Upplýsingar um umhverfi**:</span><span class="sxs-lookup"><span data-stu-id="ffcdb-110">Follow these steps to set up dual-write from LCS **Environment Details** page:</span></span>

1. <span data-ttu-id="ffcdb-111">Á síðunni **Upplýsingar um umhverfi** skal stækka hlutann **Power Platform Samþætting**.</span><span class="sxs-lookup"><span data-stu-id="ffcdb-111">On the **Environment Details** page, expand the **Power Platform Integration** section.</span></span>

2. <span data-ttu-id="ffcdb-112">Veljið hnappinn **Notkun tvöfaldrar skráningar**.</span><span class="sxs-lookup"><span data-stu-id="ffcdb-112">Select the **Dual-write application** button.</span></span>

    ![Power Platform samþætting](media/powerplat_integration_step2.png)

3. <span data-ttu-id="ffcdb-114">Farið yfir skilmálana og veljið því næst **Skilgreina**.</span><span class="sxs-lookup"><span data-stu-id="ffcdb-114">Review the terms and conditions, and then select **Configure**.</span></span>

4. <span data-ttu-id="ffcdb-115">Veldu **Í lagi** til að halda áfram.</span><span class="sxs-lookup"><span data-stu-id="ffcdb-115">Select **OK** to continue.</span></span>

5. <span data-ttu-id="ffcdb-116">Hægt er að fylgjast með framvindunni með því að endurhlaða upplýsingasíðu umhverfis með reglulegu millibili.</span><span class="sxs-lookup"><span data-stu-id="ffcdb-116">You can monitor the progress by periodically refreshing the environment details page.</span></span> <span data-ttu-id="ffcdb-117">Uppsetning tekur yfirleitt innan við 30 mínútur.</span><span class="sxs-lookup"><span data-stu-id="ffcdb-117">Setup typically takes 30 minutes or less.</span></span>  

6. <span data-ttu-id="ffcdb-118">Þegar uppsetningunni er lokið koma upp skilaboð þar sem látið er vita hvort ferlið hafi tekist eða ef villa kom upp.</span><span class="sxs-lookup"><span data-stu-id="ffcdb-118">When the setup is complete, a message will inform you if the process was successful or if there was a failure.</span></span> <span data-ttu-id="ffcdb-119">Ef uppsetningin mistókst birtast tengd villuboð.</span><span class="sxs-lookup"><span data-stu-id="ffcdb-119">If the setup failed, then a related error message is displayed.</span></span> <span data-ttu-id="ffcdb-120">Þú verður að laga allar villur sem kunna að vera til staðar áður en þú ferð í næsta skref.</span><span class="sxs-lookup"><span data-stu-id="ffcdb-120">You must fix any errors before moving to the next step.</span></span>

7. <span data-ttu-id="ffcdb-121">Veljið **Tengja við Power Platform umhverfi** til að búa til tengingu milli Dataverse og núverandi gagnagrunna umhverfis.</span><span class="sxs-lookup"><span data-stu-id="ffcdb-121">Select **Link to Power Platform environment** to create a link between Dataverse and the current environment's databases.</span></span> <span data-ttu-id="ffcdb-122">Þetta tekur yfirleitt innan við 5 mínútur.</span><span class="sxs-lookup"><span data-stu-id="ffcdb-122">This typically takes less than 5 minutes.</span></span>

    :::image type="content" source="media/powerplat_integration_step3.png" alt-text="Tengill á Power Platform-umhverfið":::

8. <span data-ttu-id="ffcdb-124">Þegar tengingin er komin verður tengill sýndur.</span><span class="sxs-lookup"><span data-stu-id="ffcdb-124">When the linking is complete, a hyperlink is displayed.</span></span> <span data-ttu-id="ffcdb-125">Notið tengilinn til að skrá ykkur inn á stjórnunarsvæði tvöfaldrar skráningar í Finance and Operations umhverfinu.</span><span class="sxs-lookup"><span data-stu-id="ffcdb-125">Use the link to sign in to the dual-write administration area in the Finance and Operations environment.</span></span> <span data-ttu-id="ffcdb-126">Þaðan er hægt að setja upp einingavarpanir.</span><span class="sxs-lookup"><span data-stu-id="ffcdb-126">From there, you can set up entity mappings.</span></span>

## <a name="set-up-dual-write-for-an-existing-dataverse-environment"></a><span data-ttu-id="ffcdb-127">Setja upp tvöfalda skráningu fyrir fyrirliggjandi Dataverse umhverfi</span><span class="sxs-lookup"><span data-stu-id="ffcdb-127">Set up dual-write for an existing Dataverse environment</span></span>

<span data-ttu-id="ffcdb-128">Til að setja upp tvöfalda skráningu fyrir fyrirliggjandi Dataverse umhverfi þarf að stofna Microsoft [þjónustubeiðni](../../lifecycle-services/lcs-support.md).</span><span class="sxs-lookup"><span data-stu-id="ffcdb-128">To set up dual-write for an existing Dataverse environment, you must create a Microsoft [support ticket](../../lifecycle-services/lcs-support.md).</span></span> <span data-ttu-id="ffcdb-129">Beiðnin verður að innihalda:</span><span class="sxs-lookup"><span data-stu-id="ffcdb-129">The ticket must include:</span></span>

+ <span data-ttu-id="ffcdb-130">Finance and Operations umhverfiskennið.</span><span class="sxs-lookup"><span data-stu-id="ffcdb-130">Your Finance and Operations environment ID.</span></span>
+ <span data-ttu-id="ffcdb-131">Heiti umhverfis í Lifecycle Services.</span><span class="sxs-lookup"><span data-stu-id="ffcdb-131">Your environment name from Lifecycle Services.</span></span>
+ <span data-ttu-id="ffcdb-132">Fyrirtækiskennið Dataverse eða umhverfiskennið Power Platform úr Power Platform stjórnendamiðstöðinni.</span><span class="sxs-lookup"><span data-stu-id="ffcdb-132">The Dataverse organization ID or Power Platform Environment ID from Power Platform Admin Center.</span></span> <span data-ttu-id="ffcdb-133">Í beiðninni skal biðja um að kennið verði tilvikið sem notað er fyrir Power Platform samþættingu.</span><span class="sxs-lookup"><span data-stu-id="ffcdb-133">In your ticket, request that the ID be the instance used for Power Platform integration.</span></span>

> [!NOTE]
> <span data-ttu-id="ffcdb-134">Þú getur ekki aftengt umhverfi með því að nota LCS.</span><span class="sxs-lookup"><span data-stu-id="ffcdb-134">You can't unlink environments by using LCS.</span></span> <span data-ttu-id="ffcdb-135">Til að aftengja umhverfi skaltu opna vinnusvæðið **Gagnasamþætting** í Finance and Operations umhverfi og veldu síðan **Aftengja**.</span><span class="sxs-lookup"><span data-stu-id="ffcdb-135">To unlink an environment, open the **Data integration** workspace in the Finance and Operations environment, and then select **Unlink**.</span></span>

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
