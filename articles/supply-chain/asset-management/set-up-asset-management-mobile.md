---
title: Nota fartækjavinnusvæði eignastýringar
description: Þetta efnisatriði lýsir því hvernig setja á upp Microsoft Dynamics 365 Supply Chain Management og Finance and Operations (Dynamics 365) farsímaforritið til að keyra fartækjavinnusvæði eignastýringar sem starfsmenn geta notað til að framkvæma verk eignastýringar.
author: johanhoffmann
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-22
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: bc170df2fc58ae6b42fbc8834caad0bb7cd16f69
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837778"
---
# <a name="set-up-the-asset-management-mobile-workspace"></a><span data-ttu-id="4e8f6-103">Nota fartækjavinnusvæði eignastýringar</span><span class="sxs-lookup"><span data-stu-id="4e8f6-103">Set up the Asset management mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4e8f6-104">Þetta efnisatriði lýsir því hvernig setja á upp Microsoft Dynamics 365 Supply Chain Management og Finance and Operations (Dynamics 365) farsímaforritið til að keyra fartækjavinnusvæði **Eignastýringar** sem starfsmenn geta notað til að framkvæma verk eignastýringar.</span><span class="sxs-lookup"><span data-stu-id="4e8f6-104">This topic describes how to set up Microsoft Dynamics 365 Supply Chain Management and the Finance and Operations (Dynamics 365) mobile app to run an **Asset management** mobile workspace that workers can use to perform asset management tasks.</span></span>

## <a name="set-up-maintenance-worker-users-in-supply-chain-management"></a><span data-ttu-id="4e8f6-105">Setja upp notendur viðhaldsstarfskrafta í Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="4e8f6-105">Set up maintenance worker users in Supply Chain Management</span></span>

<span data-ttu-id="4e8f6-106">Fyrir hvern notanda sem þarf aðgang að fartækjavinnusvæðinu **Eignastýring** skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="4e8f6-106">For each user that requires access to the **Asset management** mobile workspace, follow these steps.</span></span>

1. <span data-ttu-id="4e8f6-107">Í Supply Chain Management skal fara í **Human Resources \> Starfskraftar** og ganga úr skugga um skrá starfsmanns sé til fyrir notandann sem á að setja upp.</span><span class="sxs-lookup"><span data-stu-id="4e8f6-107">In Supply Chain Management, go to **Human resources \> Workers**, and make sure that a worker record exists for the user that you want to set up.</span></span> <span data-ttu-id="4e8f6-108">Búið til nýja skrá starfsmanns eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="4e8f6-108">Create a new worker record as required.</span></span>
1. <span data-ttu-id="4e8f6-109">Farið í **Eignastýring \> Uppsetning \> Starfskraftar \> Starfskraftar** og gangið úr skugga um skrá starfsmanns sem gerð var grein fyrir (eða var stofnaður) í skrefinu á undan sé varpað í skrá viðhaldsstarfskrafts.</span><span class="sxs-lookup"><span data-stu-id="4e8f6-109">Go to **Asset management \> Setup \> Workers \> Workers**, and make sure that the worker record that you identified (or created) in the previous step is mapped to a maintenance worker record.</span></span> <span data-ttu-id="4e8f6-110">Stofnið nýja skrá viðhaldsstarfskrafts eftir þörfum og stillið reitinn **Starfskraftur** á skrá starfsmanns úr fyrra skrefinu.</span><span class="sxs-lookup"><span data-stu-id="4e8f6-110">Create a new maintenance worker record as required, and set the **Worker** field to the worker record from the previous step.</span></span>
1. <span data-ttu-id="4e8f6-111">Farið í **Eignastýring \> Uppsetning \> Starfskraftar \> Hópar viðhaldsstarfskrafta** og gangið úr skugga um að skrá viðhaldsstarfskrafts sem gerð var grein fyrir (eða var stofnaður) í fyrra skrefi tilheyri hópi viðhaldsstarfskrafta.</span><span class="sxs-lookup"><span data-stu-id="4e8f6-111">Go to **Asset management \> Setup \> Workers \> Maintenance worker groups**, and make sure that the maintenance worker record that you identified (or created) in the previous step belongs to a maintenance worker group.</span></span>
1. <span data-ttu-id="4e8f6-112">Farið í **Kerfisstjórnun \> Notendur**.</span><span class="sxs-lookup"><span data-stu-id="4e8f6-112">Go to **System administration \> Users**.</span></span>
1. <span data-ttu-id="4e8f6-113">Veljið viðeigandi notanda í hnitanetinu.</span><span class="sxs-lookup"><span data-stu-id="4e8f6-113">Select the relevant user in the grid.</span></span>
1. <span data-ttu-id="4e8f6-114">Í flýtiflipanum **Upplýsingar um notanda** skal stilla reitinn **Einstaklingur** á starfsmannareikninginn sem á að tengja við núverandi notandareikning.</span><span class="sxs-lookup"><span data-stu-id="4e8f6-114">On the **User Details** FastTab, set the **Person** field to the worker account that you want to associate with the current user account.</span></span> <span data-ttu-id="4e8f6-115">Þessi starfsmannareikningur ætti að vera starfsmannaskráin sem gerð var grein fyrir (eða stofnuð) í skrefi 1 og varpað í skrá viðhaldsstarfskrafts í skrefi 2.</span><span class="sxs-lookup"><span data-stu-id="4e8f6-115">This worker account should be the worker record that you identified (or created) in step 1 and mapped to a maintenance worker record in step 2.</span></span>

> [!NOTE]
> <span data-ttu-id="4e8f6-116">Heimildir og öryggishlutverk notanda eiga við um eiginleika á fartækjavinnusvæðinu **Eignastýring** rétt eins og þau eiga við um eiginleika í notandaviðmóti Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="4e8f6-116">User permissions and security roles apply to the features of the **Asset management** mobile workspace just as they apply to the features of the Supply Chain Management user interface.</span></span> <span data-ttu-id="4e8f6-117">Þess vegna verður sérhver notandi sem settur er upp til að fá aðgang að fartækjavinnusvæðinu **Eignastýring** að vera með öryggishlutverkin sem þarf til að framkvæma svipaðar aðgerðir beint í Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="4e8f6-117">Therefore, every user that you set up to access the **Asset management** mobile workspace must have the security roles that are required to perform similar operations directly in Supply Chain Management.</span></span>

## <a name="publish-the-asset-management-mobile-workspace"></a><span data-ttu-id="4e8f6-118">Birta fartækjavinnusvæði eignastýringar</span><span class="sxs-lookup"><span data-stu-id="4e8f6-118">Publish the Asset management mobile workspace</span></span>

<span data-ttu-id="4e8f6-119">Til að gera eiginleika eignastýringar tiltæka í Finance and Operations (Dynamics 365) fartækjaforritinu þarf að birta fartækjavinnusvæðið **Eignastýring**.</span><span class="sxs-lookup"><span data-stu-id="4e8f6-119">To make asset management features available in the Finance and Operations (Dynamics 365) mobile app, you must publish the **Asset management** mobile workspace.</span></span>

1. <span data-ttu-id="4e8f6-120">Í Supply Chain Management skal velja hnappinn **Stillingar** (tannhjólið efst í hægra horninu) og síðan velja **Fartækjaforrit** í valmyndinni.</span><span class="sxs-lookup"><span data-stu-id="4e8f6-120">In Supply Chain Management, select the **Settings** button (the gear symbol in upper-right corner), and then select **Mobile app** on the menu.</span></span>
1. <span data-ttu-id="4e8f6-121">Í svarglugganum **Stjórna fartækjaforriti** skal finna reitinn **Eignastýring**.</span><span class="sxs-lookup"><span data-stu-id="4e8f6-121">In the **Manage mobile app** dialog box, find the **Asset Management** tile.</span></span> <span data-ttu-id="4e8f6-122">Ef hann inniheldur textann „Í lýsigögnum - ekki birt“ hefur vinnusvæðið ekki enn verið birt.</span><span class="sxs-lookup"><span data-stu-id="4e8f6-122">If it contains the text "In metadata - not published," the workspace hasn't yet been published.</span></span> <span data-ttu-id="4e8f6-123">Ef hann inniheldur textann „Í lýsigögnum - birt“ hefur vinnusvæðið þegar verið birt og hægt er að sleppa því sem eftir er af þessu ferli.</span><span class="sxs-lookup"><span data-stu-id="4e8f6-123">If it contains the text "In metadata - published," the workspace has already been published, and you can skip the rest of this procedure.</span></span>

    <span data-ttu-id="4e8f6-124">![Stjórna svarglugga fyrir farsímaforrit](media/mobile-workspaces.png "Stjórna svarglugga fyrir farsímaforrit")</span><span class="sxs-lookup"><span data-stu-id="4e8f6-124">![Manage mobile app dialog box](media/mobile-workspaces.png "Manage mobile app dialog box")</span></span>

1. <span data-ttu-id="4e8f6-125">Velja skal reitinn **Eignastýring** og síðan velja **Birta** í tækjastikunni.</span><span class="sxs-lookup"><span data-stu-id="4e8f6-125">Select the **Asset Management** tile, and then select **Publish** on the toolbar.</span></span> <span data-ttu-id="4e8f6-126">Eftir nokkrar sekúndur ætti að berast tilkynning sem segir til um að vinnusvæði hafi verið birt.</span><span class="sxs-lookup"><span data-stu-id="4e8f6-126">After a few seconds, you should receive a notification that states that the workspace has been successfully published.</span></span> <span data-ttu-id="4e8f6-127">Þar að auki ætti textinn í reitnum að breytast í „Í lýsigögnum - birt.“</span><span class="sxs-lookup"><span data-stu-id="4e8f6-127">Additionally, the text on the tile should change to "In metadata - published."</span></span>

## <a name="install-and-set-up-the-finance-and-operations-dynamics-365-mobile-app"></a><span data-ttu-id="4e8f6-128">Setja upp Finance and Operations (Dynamics 365) farsímaforrit</span><span class="sxs-lookup"><span data-stu-id="4e8f6-128">Install and set up the Finance and Operations (Dynamics 365) mobile app</span></span>

1. <span data-ttu-id="4e8f6-129">Farið í eina af eftirfarandi forritaverslunum til að setja upp forritið **Microsoft Finance and Operations (Dynamics 365)** í fartækinu:</span><span class="sxs-lookup"><span data-stu-id="4e8f6-129">Go to one of the following app stores to install the **Microsoft Finance and Operations (Dynamics 365)** app on your mobile device:</span></span>

    - [<span data-ttu-id="4e8f6-130">Fyrir Google Android-tæki</span><span class="sxs-lookup"><span data-stu-id="4e8f6-130">For Google Android devices</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
    - [<span data-ttu-id="4e8f6-131">Fyrir Apple iOS-tæki</span><span class="sxs-lookup"><span data-stu-id="4e8f6-131">For Apple iOS devices</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

1. <span data-ttu-id="4e8f6-132">Opnið forritið Finance and Operations (Dynamics 365).</span><span class="sxs-lookup"><span data-stu-id="4e8f6-132">Open the Finance and Operations (Dynamics 365) app.</span></span> <span data-ttu-id="4e8f6-133">Innskráningarsíðan ætti að birtast.</span><span class="sxs-lookup"><span data-stu-id="4e8f6-133">The sign-in page should appear.</span></span> <span data-ttu-id="4e8f6-134">Í reitinn **Innskráning** skal færa inn vefslóð Supply Chain Management eða velja nýlega vefslóð úr listanum **Nýleg umhverfi** og síðan pikka á **Tengja**.</span><span class="sxs-lookup"><span data-stu-id="4e8f6-134">In the **Sign in** field, enter your Supply Chain Management URL, or select a recent URL in the **Recent environments** list, and then tap **Connect**.</span></span>

    <span data-ttu-id="4e8f6-135">![Innskráningarsíða](media/mobile-app-sign-in.png "Innskráningarsíða")</span><span class="sxs-lookup"><span data-stu-id="4e8f6-135">![Sign-in page](media/mobile-app-sign-in.png "Sign-in page")</span></span>

1. <span data-ttu-id="4e8f6-136">Ef notandi er beðinn um að staðfesta tenginguna skal velja gátreitinn **Ég skil** og síðan flipann **Tengja**.</span><span class="sxs-lookup"><span data-stu-id="4e8f6-136">If you're prompted to confirm the connection, select the **I understand** check box, and then tap **Connect**.</span></span>
1. <span data-ttu-id="4e8f6-137">Á síðunni **Velja reikning** skal nota Microsoft-reikninginn til að skrá sig inn í farsímaforritið.</span><span class="sxs-lookup"><span data-stu-id="4e8f6-137">On the **Pick an account** page, use your Microsoft account to sign in to the mobile application.</span></span>

    <span data-ttu-id="4e8f6-138">Síðan **Vinnusvæði** birtist.</span><span class="sxs-lookup"><span data-stu-id="4e8f6-138">The **Workspaces** page appears.</span></span> <span data-ttu-id="4e8f6-139">Hún sýnir öll fartækjavinnusvæði sem hafa verið gefin út af tilviki Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="4e8f6-139">It lists every mobile workspace that has been published by your Supply Chain Management instance.</span></span>

    <span data-ttu-id="4e8f6-140">![Listi vinnusvæða](media/mobile-app-workspaces.png "Listi vinnusvæða")</span><span class="sxs-lookup"><span data-stu-id="4e8f6-140">![List of workspaces](media/mobile-app-workspaces.png "List of workspaces")</span></span>

1. <span data-ttu-id="4e8f6-141">Ef breyta þarf lögaðilanum (fyrirtækinu) skal pikka á valmyndarhnappinn (stundum kallaður hamborgarinn eða hamborgarahnappurinn) efst í vinstra horninu og síðan pikka á **Breyta fyrirtæki**.</span><span class="sxs-lookup"><span data-stu-id="4e8f6-141">If you must change the legal entity (company), tap the Menu button (sometimes referred to as the hamburger or the hamburger button) in the upper-left corner, and then tap **Change company**.</span></span>

    <span data-ttu-id="4e8f6-142">![Lögaðila breytt](media/mobile-app-change-comp.png "Breying lögaðila")</span><span class="sxs-lookup"><span data-stu-id="4e8f6-142">![Changing the legal entity](media/mobile-app-change-comp.png "Changing the legal entity")</span></span>

1. <span data-ttu-id="4e8f6-143">Á síðunni **Vinnusvæði** skal velja vinnusvæðið sem ætlunin er að vinna með til að opna það.</span><span class="sxs-lookup"><span data-stu-id="4e8f6-143">On the **Workspaces** page, select the workspace that you want to work with to open it.</span></span>

    <span data-ttu-id="4e8f6-144">![Fartækjavinnusvæði eignastýringar](media/mobile-app-asset-workspace.png "Fartækjavinnusvæði eignastýringar")</span><span class="sxs-lookup"><span data-stu-id="4e8f6-144">![Asset management mobile workspace](media/mobile-app-asset-workspace.png "Asset management mobile workspace")</span></span>

## <a name="work-with-the-asset-management-mobile-workspace"></a><span data-ttu-id="4e8f6-145">Vinna með fartækjavinnusvæði eignastýringar</span><span class="sxs-lookup"><span data-stu-id="4e8f6-145">Work with the Asset management mobile workspace</span></span>

<span data-ttu-id="4e8f6-146">Frekari upplýsingar um hvernig á að vinna með fartækjavinnusvæðið **Eignastýring** er að finna í [Nota fartækjavinnusvæði eignastýringar](asset-management-mobile-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="4e8f6-146">For more information about how to work with the **Asset management** mobile workspace, see [Use the Asset management mobile workspace](asset-management-mobile-workspace.md).</span></span>

<span data-ttu-id="4e8f6-147">Frekari upplýsingar um fartækjaforritið Finance and Operations (Dynamics 365) er að finna í [Heimasíða fartækjaforrits](../../fin-ops-core/dev-itpro/mobile-apps/Mobile-app-home-page.md).</span><span class="sxs-lookup"><span data-stu-id="4e8f6-147">For more information about the Finance and Operations (Dynamics 365) mobile app, see the [Mobile app home page](../../fin-ops-core/dev-itpro/mobile-apps/Mobile-app-home-page.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]