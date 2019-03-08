---
title: Nýjungar eða breytingar í Dynamics 365 for Talent Core HR (16. október 2018)
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 for Talent Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 10/22/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-22
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 7da597a682006cddb44ff9354813b07c15c1a449
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "304893"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-october-19-2018"></a><span data-ttu-id="af5a4-103">Nýjungar eða breytingar í Dynamics 365 for Talent Core HR (19. október 2018)</span><span class="sxs-lookup"><span data-stu-id="af5a4-103">What's new or changed in Dynamics 365 for Talent Core HR (October 19, 2018)</span></span>

[!include[banner](includes/banner.md)]

<span data-ttu-id="af5a4-104">**Smíði 8.1.1067**</span><span class="sxs-lookup"><span data-stu-id="af5a4-104">**Build 8.1.1067**</span></span>

<span data-ttu-id="af5a4-105">Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Core HR.</span><span class="sxs-lookup"><span data-stu-id="af5a4-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="allow-managers-to-update-time-off-requests"></a><span data-ttu-id="af5a4-106">Leyfa stjórnendum að uppfæra beiðnir um frí</span><span class="sxs-lookup"><span data-stu-id="af5a4-106">Allow managers to update time off requests</span></span>

<span data-ttu-id="af5a4-107">Hugsanlega verður að uppfæra beiðnir um frí frá starfsmönnum þegar þeir eru samþykktir í gegnum vinnuflæði.</span><span class="sxs-lookup"><span data-stu-id="af5a4-107">Employee time off requests may need to be updated after they are approved through the workflow.</span></span> <span data-ttu-id="af5a4-108">Í mörgum tilvikum framkvæmir stjórnandi þessar uppfærslur fyrir hönd starfsmannsins.</span><span class="sxs-lookup"><span data-stu-id="af5a4-108">In many cases, the manager makes these updates on the employee’s behalf.</span></span> <span data-ttu-id="af5a4-109">Þessi nýi eiginleiki veitir stjórnendum kleift að uppfæra beiðnir um frí eða hætta við beiðnir um frí fyrir hönd starfsmanna sinna.</span><span class="sxs-lookup"><span data-stu-id="af5a4-109">This new feature provides the ability for managers to update time off or cancel time off requests on behalf of their employees.</span></span> <span data-ttu-id="af5a4-110">Þessum eiginleika er stjórnað af **Störf fyrir hönd annarra** færibreytu sem hægt er að stilla á **Mannauðsfæribreytum** síðu.</span><span class="sxs-lookup"><span data-stu-id="af5a4-110">This capability is controlled by the **Work on behalf** parameter that can be set on the **Human Resource Parameters** page.</span></span> 
 
## <a name="allow-hr-to-update-time-off-requests"></a><span data-ttu-id="af5a4-111">Leyfa mannauði að uppfæra beiðnir um frí</span><span class="sxs-lookup"><span data-stu-id="af5a4-111">Allow HR to update time off requests</span></span>

<span data-ttu-id="af5a4-112">Líkt og eiginleikinn hér að framan, kann mannauður að þurfa að uppfæra beiðnir starfsmanna um frí eftir að þær hafa verið samþykktar í gegnum vinnuflæði.</span><span class="sxs-lookup"><span data-stu-id="af5a4-112">Similar to the feature above, employee time off requests may need to be updated by HR after they have been previously approved through the workflow.</span></span> <span data-ttu-id="af5a4-113">Þessi eiginleiki gerir mannauðsnotendum kleift að uppfæra beiðnir um frí.</span><span class="sxs-lookup"><span data-stu-id="af5a4-113">This feature provides the ability for HR users to update time off requests.</span></span> <span data-ttu-id="af5a4-114">Eiginleikinn er virkjaður í **Starfsfólk** vinnumiðstöðinni og á **Starfskraftur** síðunni, með nýjum valkosti sem heitir **Skoða frí**.</span><span class="sxs-lookup"><span data-stu-id="af5a4-114">The capability is enabled in the **People** workspace and on the **Worker** page, using a new option called **View time off**.</span></span> <span data-ttu-id="af5a4-115">Á þessum síðum geta mannauðsnotendur skoðað beiðnir og uppfært beiðnir um frí, svipað og hvernig stjórnendur geta framkvæmt þessar aðgerðir.</span><span class="sxs-lookup"><span data-stu-id="af5a4-115">On those pages, HR users can view requests and update time off transactions, similar to how managers can perform these actions.</span></span>

<span data-ttu-id="af5a4-116">Öryggisskyldan sem stjórnar aðgangi að þessari virkni er:</span><span class="sxs-lookup"><span data-stu-id="af5a4-116">The security duty that controls access to this functionality is:</span></span>
- <span data-ttu-id="af5a4-117">Skylda: Vinna með leyfis- og fjarvistaferla tiltekinna starfsmanna.</span><span class="sxs-lookup"><span data-stu-id="af5a4-117">Duty: Maintain worker-specific leave and absence processes.</span></span>
- <span data-ttu-id="af5a4-118">Réttindi: Vinna með leyfis- og fjarvistabeiðnir fyrir allt starfsfólk.</span><span class="sxs-lookup"><span data-stu-id="af5a4-118">Privilege: Maintain leave and absence requests for all workers.</span></span>

## <a name="other-changes"></a><span data-ttu-id="af5a4-119">Aðrar breytingar</span><span class="sxs-lookup"><span data-stu-id="af5a4-119">Other changes</span></span>
<span data-ttu-id="af5a4-120">Eftirfarandi uppfærslur hafa verið gerðar í þessari útgáfu:</span><span class="sxs-lookup"><span data-stu-id="af5a4-120">The following updates have been made in this release:</span></span>
- <span data-ttu-id="af5a4-121">Breytingar á aðgerðum starfsmannaráðninga þannig að þeir séu ekki lengur „fastir“ í **Verkflæði lokið** ástandi.</span><span class="sxs-lookup"><span data-stu-id="af5a4-121">Changes to worker hire actions so that they are no longer "stuck" in **Workflow complete** state.</span></span>
- <span data-ttu-id="af5a4-122">Starfsferilsskrá er nú hægt að búa til án upphafsdags atvinnu.</span><span class="sxs-lookup"><span data-stu-id="af5a4-122">Employment record can now be created without an employment start date.</span></span>
- <span data-ttu-id="af5a4-123">Dynamics 365 Talent skráningardegi fyrir námskeið sem er sýnt í sjálfsafgreiðslusíðum starfsmanna gildir nú tímabeltið á móti þeim degi.</span><span class="sxs-lookup"><span data-stu-id="af5a4-123">The Dynamics 365 Talent registration date for a course shown in Employee self-service now applies the time zone offset to the date.</span></span>
- <span data-ttu-id="af5a4-124">Excel-skrár geta verið fluttar inn mörgum sinnum villulaust með **Starfsmannaeiningu**.</span><span class="sxs-lookup"><span data-stu-id="af5a4-124">Excel files can be imported multiple times without any errors using **Employee Entity**.</span></span>

## <a name="known-issue"></a><span data-ttu-id="af5a4-125">Þekkt vandamál</span><span class="sxs-lookup"><span data-stu-id="af5a4-125">Known issue</span></span>

- <span data-ttu-id="af5a4-126">**Vandamál**: Þegar nýtt viðhengi er bætt við starfsmann eru hnapparnir **Nýtt** og **Breyta** skyggðir.</span><span class="sxs-lookup"><span data-stu-id="af5a4-126">**Issue**: When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out.</span></span> 
- <span data-ttu-id="af5a4-127">**Hjáleið:** Áður en þú opnar viðhengissíðu skaltu ganga úr skugga um að FactBoxes á síðunni **Starfsmenn** séu lokaðir.</span><span class="sxs-lookup"><span data-stu-id="af5a4-127">**Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="af5a4-128">Ef upplýsingareitirnir eru lokaðir þegar síðan **Starfskraftar** er hlaðið inn verða viðhengishnapparnir gerðir virkir.</span><span class="sxs-lookup"><span data-stu-id="af5a4-128">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="af5a4-129">(Þetta vandamál verður lagað í næstu verkvangsuppfærslu.)</span><span class="sxs-lookup"><span data-stu-id="af5a4-129">(This issue will be fixed in the next platform update.)</span></span>
