---
title: Varpa verslunum og teymum ef fyrirliggjandi teymi eru í Microsoft Teams
description: Þetta efnisatriði fjallar um hvernig á að varpa verslunum og samsvarandi teymum í Dynamics 365 Commerce höfuðstöðvar ef fyrirtækið hefur þegar stofnað teymi í Microsoft Teams á undan Commerce-samþættingu.
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: ccc2cbf11e405facf310d93e5458cfe12a43146d
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020220"
---
# <a name="map-stores-and-teams-if-there-are-pre-existing-teams-in-microsoft-teams"></a><span data-ttu-id="c59d9-103">Varpa verslunum og teymum ef fyrirliggjandi teymi eru í Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="c59d9-103">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c59d9-104">Þetta efnisatriði fjallar um hvernig á að varpa verslunum og samsvarandi teymum í Dynamics 365 Commerce höfuðstöðvar ef fyrirtækið hefur þegar stofnað teymi í Microsoft Teams á undan Commerce-samþættingu.</span><span class="sxs-lookup"><span data-stu-id="c59d9-104">This topic covers how to map stores and corresponding teams in Dynamics 365 Commerce headquarters if your organization has already created teams in Microsoft Teams before Commerce integration.</span></span>

<span data-ttu-id="c59d9-105">Fyrirtækið gæti stofnað teymi fyrir sumar eða allar verslanirnar áður en Dynamics 365 Commerce og Microsoft Teams er samþætt.</span><span class="sxs-lookup"><span data-stu-id="c59d9-105">Your organization may have teams created for some or all of your stores before integrating Dynamics 365 Commerce and Microsoft Teams.</span></span> <span data-ttu-id="c59d9-106">Ef svo er þarf að gefa upp vörpun verslana og samsvarandi teymis í Commerce Headquarters til að koma á samstillingu verks milli sölustaðar Commerce og Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="c59d9-106">If this is the case, to establish task synchronization between Commerce POS and Microsoft Teams you must provide the mapping of stores and corresponding team in Commerce headquarters.</span></span>

## <a name="map-stores-and-corresponding-teams-in-commerce-headquarters"></a><span data-ttu-id="c59d9-107">Varpa verslunum og samsvarandi teymum í Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="c59d9-107">Map stores and corresponding teams in Commerce headquarters</span></span> 

<span data-ttu-id="c59d9-108">Til að varpa verslunum og samsvarandi teymum í Commerce Headquarters skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="c59d9-108">To map stores and corresponding teams in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="c59d9-109">Opnið **Kerfisstjórnun \> Vinnusvæði \> Gagnastjórnun**.</span><span class="sxs-lookup"><span data-stu-id="c59d9-109">Go to **System Administration \> Workspace \> Data management**.</span></span>
1. <span data-ttu-id="c59d9-110">Velja **Flytja út**.</span><span class="sxs-lookup"><span data-stu-id="c59d9-110">Select **Export**.</span></span> 
1. <span data-ttu-id="c59d9-111">Í aðgerðarúðunni velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="c59d9-111">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="c59d9-112">Undir **Heiti hóps** skal slá inn „Flytja út Teams vörpun“.</span><span class="sxs-lookup"><span data-stu-id="c59d9-112">Under **Group name**, enter "Export Teams mapping".</span></span>
1. <span data-ttu-id="c59d9-113">Á flýtiflipanum **Valdar einingar** skal velja **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="c59d9-113">On the **Selected entities** FastTab, select **Add entity**.</span></span> <span data-ttu-id="c59d9-114">Svarglugginn **Bæta við einingu** birtist.</span><span class="sxs-lookup"><span data-stu-id="c59d9-114">The **Add entity** dialog box appears.</span></span>  
1. <span data-ttu-id="c59d9-115">Í fellilistanum **Heiti einingar** skal velja **Vörpun Teams milli uppruna og teymis**.</span><span class="sxs-lookup"><span data-stu-id="c59d9-115">In the **Entity name** drop-down list, select **Teams mapping between source and team**.</span></span>
1. <span data-ttu-id="c59d9-116">Í fellilistanum **Markgagnasnið** skal velja **CSV**.</span><span class="sxs-lookup"><span data-stu-id="c59d9-116">In the **Target data format** drop-down list, select **CSV**.</span></span>
1. <span data-ttu-id="c59d9-117">Veljið **Bæta við** og síðan **Loka**.</span><span class="sxs-lookup"><span data-stu-id="c59d9-117">Select **Add**, and then select **Close**.</span></span>
1. <span data-ttu-id="c59d9-118">Efst til vinstri undir Aðgerðarsvæðinu skal velja **Flytja út núna**.</span><span class="sxs-lookup"><span data-stu-id="c59d9-118">On the top left under the Action Pane, select **Export now**.</span></span>
1. <span data-ttu-id="c59d9-119">Undir **Vinnslustaða einingar** skal velja **Sækja skrá**.</span><span class="sxs-lookup"><span data-stu-id="c59d9-119">Under **Entity processing status**, select **Download file**.</span></span>
1. <span data-ttu-id="c59d9-120">Í útfluttri CSV-skrá skal slá inn gildi fyrir **SOURCETYPE**, **SOURCEID** og **TEAMID** á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="c59d9-120">In the exported CSV file, enter values for **SOURCETYPE**, **SOURCEID**, and **TEAMID** as follows:</span></span>
    - <span data-ttu-id="c59d9-121">Fyrir **SOURCETYPE** skal slá inn „RetailStore“.</span><span class="sxs-lookup"><span data-stu-id="c59d9-121">For **SOURCETYPE**, enter "RetailStore".</span></span> 
    - <span data-ttu-id="c59d9-122">Fyrir **SOURCEID** skal slá inn númer verslunar (til dæmis „000135“ fyrir verslun í San Francisco).</span><span class="sxs-lookup"><span data-stu-id="c59d9-122">For **SOURCEID**, enter the store number (for example, "000135" for the San Francisco store).</span></span> <span data-ttu-id="c59d9-123">Hægt er að finna verslunarnúmer í **Smásala og viðskipti \> Rásir \> Verslanir**.</span><span class="sxs-lookup"><span data-stu-id="c59d9-123">You can find store numbers at **Retail and Commerce \> Channels \> Stores**.</span></span>
    - <span data-ttu-id="c59d9-124">Fyrir **TEAMID** skal slá inn samsvarandi kenni teymis úr Microsoft Teams (til dæmis „5f8bc92b-6aa8-451e-85d1-3949c01ddc6c“).</span><span class="sxs-lookup"><span data-stu-id="c59d9-124">For **TEAMID**, enter the corresponding team ID from Microsoft Teams (for example, "5f8bc92b-6aa8-451e-85d1-3949c01ddc6c").</span></span> <span data-ttu-id="c59d9-125">Kenni fyrir upplýsingar teymis má finna á [admin.teams.microsoft.com](https://admin.teams.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="c59d9-125">You can find team ID information at [admin.teams.microsoft.com](https://admin.teams.microsoft.com).</span></span>
1. <span data-ttu-id="c59d9-126">Vistið CSV-skrána á staðbundinni vél.</span><span class="sxs-lookup"><span data-stu-id="c59d9-126">Save the CSV file to your local machine.</span></span>
1. <span data-ttu-id="c59d9-127">Opnið **Kerfisstjórnun \> Vinnusvæði \> Gagnastjórnun** og veljið síðan **Flytja inn**.</span><span class="sxs-lookup"><span data-stu-id="c59d9-127">Go to **System Administration \> Workspace \> Data management**, and then select **Import**.</span></span>
1. <span data-ttu-id="c59d9-128">Á flýtiflipanum **Valdar einingar** skal velja **Bæta við skrá**.</span><span class="sxs-lookup"><span data-stu-id="c59d9-128">On the **Selected entities** FastTab, select **Add file**.</span></span> <span data-ttu-id="c59d9-129">Svarglugginn **Bæta við skrá** birtist.</span><span class="sxs-lookup"><span data-stu-id="c59d9-129">The **Add file** dialog box appears.</span></span>
1. <span data-ttu-id="c59d9-130">Í fellilistanum **Heiti einingar** skal velja **Vörpun Teams milli uppruna og teymis**.</span><span class="sxs-lookup"><span data-stu-id="c59d9-130">In the **Entity name** drop-down list, select **Teams mapping between source and team**.</span></span>
1. <span data-ttu-id="c59d9-131">Í fellilistanum **Snið upprunagagna** skal velja **CSV**.</span><span class="sxs-lookup"><span data-stu-id="c59d9-131">In the **Source data format** drop-down list, select **CSV**.</span></span>
1. <span data-ttu-id="c59d9-132">Veljið **Hlaða upp og bæta við**, veljið CSV-skrána sem var vistuð áður og veljið síðan **Opna**.</span><span class="sxs-lookup"><span data-stu-id="c59d9-132">Select **Upload and add**, select the CSV file that you saved previously, and then select **Open**.</span></span>
1. <span data-ttu-id="c59d9-133">Í svarglugganum **Bæta við skrá** skal velja **Loka**.</span><span class="sxs-lookup"><span data-stu-id="c59d9-133">In the **Add file** dialog box, select **Close**.</span></span>
1. <span data-ttu-id="c59d9-134">Á aðgerðasvæðinu skal velja **Vista** og síðan **Flytja inn**.</span><span class="sxs-lookup"><span data-stu-id="c59d9-134">On the Action Pane, select **Save** , and then select **Import**.</span></span>

<span data-ttu-id="c59d9-135">Eftirfarandi myndadæmi sýnir flokkinn **Flytja út vörpun teymis** í Commerce með einingarnar **Bæta við einingu** og útfluttan haus CSV-skráar auðkennd.</span><span class="sxs-lookup"><span data-stu-id="c59d9-135">The following example image shows the **Export teams mapping** group in Commerce with **Add entity** elements and the exported CSV file headers highlighted.</span></span>

![Flytja út vörpun teymis í Commerce með einingarnar Bæta við einingu og útfluttan haus CSV-skráar auðkennd](media/d365-commerce-data-mgmt-export-entity.png)

> [!NOTE]
> <span data-ttu-id="c59d9-137">Þegar ofangreindum skrefum er lokið skal fylgja skrefunum í [Samstilla verkstjórnun á milli Microsoft Teams og sölustaðar](synchronize-tasks-teams-pos.md) til að samstilla verkstjórnun.</span><span class="sxs-lookup"><span data-stu-id="c59d9-137">After you complete the preceeding steps, follow the steps in [Synchronize task management between Microsoft Teams and POS](synchronize-tasks-teams-pos.md) to synchronize task management.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="c59d9-138">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="c59d9-138">Additional resources</span></span>

[<span data-ttu-id="c59d9-139">Dynamics 365 Commerce og Microsoft Teams samþættingaryfirlit</span><span class="sxs-lookup"><span data-stu-id="c59d9-139">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="c59d9-140">Gera Dynamics 365 Commerce og Microsoft Teams samþættingu virka</span><span class="sxs-lookup"><span data-stu-id="c59d9-140">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="c59d9-141">Ákvæði Microsoft Teams frá Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="c59d9-141">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="c59d9-142">Samstilla verkstjórnun á milli Microsoft Teams og Dynamics 365 Commerce sölustaðar</span><span class="sxs-lookup"><span data-stu-id="c59d9-142">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="c59d9-143">Stjórna notandahlutverkum í Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="c59d9-143">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="c59d9-144">Algengar spurningar um samþættingu Dynamics 365 Commerce og Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="c59d9-144">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)
