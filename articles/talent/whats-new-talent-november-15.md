---
title: "Nýjungar eða breytingar í Dynamics 365 for Talent Core HR (15. nóvember 2018)"
description: "Í þessu efnisatriði er lýst nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 for Talent Core HR."
author: Darinkramer
manager: AnnBe
ms.date: 11/15/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: 3cc19a8e5f726495e698a3a2f4ccce7460a61657
ms.openlocfilehash: 0e9de5e36e67941ab09c773a63b0e7045105a07e
ms.contentlocale: is-is
ms.lasthandoff: 12/04/2018

---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-november-15-2018"></a><span data-ttu-id="41f1d-103">Nýjungar eða breytingar í Dynamics 365 for Talent Core HR (15. nóvember 2018)</span><span class="sxs-lookup"><span data-stu-id="41f1d-103">What's new or changed in Dynamics 365 for Talent Core HR (November 15, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="41f1d-104">**Smíði 8.1.2045**</span><span class="sxs-lookup"><span data-stu-id="41f1d-104">**Build 8.1.2045**</span></span>

<span data-ttu-id="41f1d-105">Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Core HR.</span><span class="sxs-lookup"><span data-stu-id="41f1d-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="other-changesfixes"></a><span data-ttu-id="41f1d-106">Aðrar breytingar/lagfæringar</span><span class="sxs-lookup"><span data-stu-id="41f1d-106">Other changes/fixes</span></span>

### <a name="unable-to-change-employees-current-position-to-a-future-open-position"></a><span data-ttu-id="41f1d-107">Ekki er hægt að breyta núverandi stöðu starfsmanns í opna stöðu í framtíðinni</span><span class="sxs-lookup"><span data-stu-id="41f1d-107">Unable to change employee´s current position to a future open position</span></span>

<span data-ttu-id="41f1d-108">Breyting hefur verið gerð til að virkja flutninga á stöðu þegar staðan er aðeins í boði í framtíðinni.</span><span class="sxs-lookup"><span data-stu-id="41f1d-108">A change has been made to enable position transfers when the position is only available in the future.</span></span> 

### <a name="position-does-not-display-when-creating-a-new-employee"></a><span data-ttu-id="41f1d-109">Staða birtist ekki þegar nýr starfsmaður er búinn til</span><span class="sxs-lookup"><span data-stu-id="41f1d-109">Position does not display when creating a new employee</span></span>

<span data-ttu-id="41f1d-110">Breytingar hafa verið gerðar til að birta allar opnar stöður sem eru tiltækar til úthlutunar þegar nýir starfsmenn eru ráðnir í Talent.</span><span class="sxs-lookup"><span data-stu-id="41f1d-110">A change has been made to display all open positions that are available for assignment when hiring new employees in Talent.</span></span> <span data-ttu-id="41f1d-111">Þetta felur í sér eldri stöður eða ef stöðurnar hafa verið í dagsettar fram í tímann.</span><span class="sxs-lookup"><span data-stu-id="41f1d-111">This includes historical positions or if the postitions have been future dated.</span></span> <span data-ttu-id="41f1d-112">Stöður birtast nú rétt á grundvelli upphafsdags ráðningar.</span><span class="sxs-lookup"><span data-stu-id="41f1d-112">Positions will now appear correctly based on the employment start date.</span></span> 

### <a name="termination-date-is-displaying-based-on-user-settings"></a><span data-ttu-id="41f1d-113">Dagur starfsloka er birtur á grundvelli notandastillinga</span><span class="sxs-lookup"><span data-stu-id="41f1d-113">Termination date is displaying based on user settings</span></span>

<span data-ttu-id="41f1d-114">Breyting hefur verið gerð á lista fyrri starfsmanna til að taka tillit til tímamismunar út af æskilegu tímabelti starfsmanna þegar starfslokadagar eru skoðaðir.</span><span class="sxs-lookup"><span data-stu-id="41f1d-114">A change has been made to the past employees list to account for any time zone offsets for the employees preferred time zone when viewing the termination date.</span></span>

### <a name="work-items-assigned-to-me-links-not-displaying-the-correct-information"></a><span data-ttu-id="41f1d-115">Tenglar fyrir vinnuliði sem mér eru úthlutaðir birta ekki réttar upplýsingar</span><span class="sxs-lookup"><span data-stu-id="41f1d-115">Work items assigned to me links not displaying the correct information</span></span>

<span data-ttu-id="41f1d-116">Með þessari breytingu mun fletting í upplýsingar einstakra vinnuliða í listanum birta réttar upplýsingar fyrir valinn lið.</span><span class="sxs-lookup"><span data-stu-id="41f1d-116">With this change, navigation to the details of the individual work items in the list will display the correct information for the item selected.</span></span> <span data-ttu-id="41f1d-117">Þetta vandamál átti sér aðeins stað með ítarlegum öryggisvalkostum.</span><span class="sxs-lookup"><span data-stu-id="41f1d-117">This issue only occurred with advanced security options.</span></span>


## <a name="known-issue"></a><span data-ttu-id="41f1d-118">Þekkt vandamál</span><span class="sxs-lookup"><span data-stu-id="41f1d-118">Known issue</span></span>

- <span data-ttu-id="41f1d-119">**Vandamál**: Þegar nýtt viðhengi er bætt við starfsmann eru hnapparnir **Nýtt** og **Breyta** skyggðir.</span><span class="sxs-lookup"><span data-stu-id="41f1d-119">**Issue**: When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out.</span></span> 
- <span data-ttu-id="41f1d-120">**Hjáleið:** Áður en þú opnar viðhengissíðu skaltu ganga úr skugga um að FactBoxes á síðunni **Starfsmenn** séu lokaðir.</span><span class="sxs-lookup"><span data-stu-id="41f1d-120">**Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="41f1d-121">Ef upplýsingareitirnir eru lokaðir þegar síðan **Starfskraftar** er hlaðið inn verða viðhengishnapparnir gerðir virkir.</span><span class="sxs-lookup"><span data-stu-id="41f1d-121">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="41f1d-122">(Þetta vandamál verður lagað í næstu verkvangsuppfærslu.)</span><span class="sxs-lookup"><span data-stu-id="41f1d-122">(This issue will be fixed in the next platform update.)</span></span>

