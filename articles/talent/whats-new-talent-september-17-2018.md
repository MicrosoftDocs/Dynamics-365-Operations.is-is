---
title: Nýjungar eða breytingar í Dynamics 365 for Talent Core HR (17. september 2018)
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 for Talent Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 09/17/2018
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
ms.search.validFrom: 2018-09-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 6586761fc62c13c701e8a8f61e15eedc66e2f751
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "304859"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-september-17-2018"></a><span data-ttu-id="c3884-103">Nýjungar eða breytingar í Dynamics 365 for Talent Core HR (17. september 2018)</span><span class="sxs-lookup"><span data-stu-id="c3884-103">What's new or changed in Dynamics 365 for Talent Core HR (September 17, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c3884-104">**Smíði 8.1.154.0**</span><span class="sxs-lookup"><span data-stu-id="c3884-104">**Build 8.1.154.0**</span></span>

<span data-ttu-id="c3884-105">Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Core HR.</span><span class="sxs-lookup"><span data-stu-id="c3884-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="leave-and-absence--accrue-time-based-on-hours-worked"></a><span data-ttu-id="c3884-106">Leyfi og fjarvistir - Uppsöfnun tíma sem byggist á vinnustundum</span><span class="sxs-lookup"><span data-stu-id="c3884-106">Leave and Absence – Accrue time based on hours worked</span></span>

<span data-ttu-id="c3884-107">Nýrri gerð uppsöfnunar var bætt við Leyfisáætlanir.</span><span class="sxs-lookup"><span data-stu-id="c3884-107">A new accrual type has been added to Leave plans.</span></span> <span data-ttu-id="c3884-108">Uppsöfnunaráætlunin getur nú byggst á starfsaldri í mánuðum eða vinnustundum.</span><span class="sxs-lookup"><span data-stu-id="c3884-108">The accrual schedule can now be based on months of service or hours worked.</span></span> <span data-ttu-id="c3884-109">Nánari upplýsingar er að finna í [Uppsöfnun frís sem byggist á vinnustundum](leave-accrue-hours-worked.md).</span><span class="sxs-lookup"><span data-stu-id="c3884-109">For more information, see [Accrue time off based on hours worked](leave-accrue-hours-worked.md).</span></span>

## <a name="platform-update-18"></a><span data-ttu-id="c3884-110">Update 18 fyrir verkvang</span><span class="sxs-lookup"><span data-stu-id="c3884-110">Platform update 18</span></span>

<span data-ttu-id="c3884-111">Verkvangsuppfærsla 18 er nú hluti af Talent-útgáfunni.</span><span class="sxs-lookup"><span data-stu-id="c3884-111">Platform update 18 is now part of the Talent release.</span></span> 

-   <span data-ttu-id="c3884-112">Hægt er að fela áskilda reiti og aðra reiti í gegnum sérstillingar.</span><span class="sxs-lookup"><span data-stu-id="c3884-112">Mandatory and other fields can be hidden via personalization.</span></span> <span data-ttu-id="c3884-113">Þetta gerir notanda kleift að búa til einfaldaða upplifun þar sem áskildir reitir sem viðskiptagrunnur gerir sjálfgefna eru ekki sýndir.</span><span class="sxs-lookup"><span data-stu-id="c3884-113">This allows a user to create a simplified experience where mandatory fields that are defaulted by business logic are not shown.</span></span> <span data-ttu-id="c3884-114">Faldir áskildir reitir eru einnig gerðir sýnilegir tímabundið ef þeir eru tómir þegar reynt er að vista.</span><span class="sxs-lookup"><span data-stu-id="c3884-114">Hidden mandatory fields are also temporarily made visible if they are empty when a save is attempted.</span></span>

-   <span data-ttu-id="c3884-115">Í verkvangsuppfærslu 18 stillir Talent-vefbiðlarinn nú myndefni sitt við Microsoft Fluent Design.</span><span class="sxs-lookup"><span data-stu-id="c3884-115">In Platform update 18, the Talent web client now aligns its visuals with Microsoft Fluent Design.</span></span>

    -   <span data-ttu-id="c3884-116">Þegar reitir eru í „lestrarstillingu“ er einfaldlega hægt að velja breytingarvalkostinn í reitunum svo hægt sé að breyta skjámyndinni.</span><span class="sxs-lookup"><span data-stu-id="c3884-116">When fields are in “read mode”, you can simply select the edit option in the fields to switch the form to edit.</span></span>

    -   <span data-ttu-id="c3884-117">Breytingar á því hvernig reitir birtast þegar þeir eru lestrarstillingu.</span><span class="sxs-lookup"><span data-stu-id="c3884-117">Changes in how fields display when in read mode.</span></span>

    -   <span data-ttu-id="c3884-118">Fyrirsagnir í vinnusvæðum og síðum eru feitletraðar.</span><span class="sxs-lookup"><span data-stu-id="c3884-118">Headings in workspaces and pages are bold.</span></span>

-   <span data-ttu-id="c3884-119">Hegðun óútskiptanlegra uppflettinga hefur verið bætt.</span><span class="sxs-lookup"><span data-stu-id="c3884-119">The behavior of non-replacing lookups has been improved.</span></span> <span data-ttu-id="c3884-120">Nánari upplýsingar er að finna í [Endurbætur á hegðun fyrir óútskiptanlegar flettingar](https://na01.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fbusiness-applications-release-notes%2FOctober18%2Fdynamics365-finance-operations%2Fnon-replacing-lookups&data=02%7C01%7C%7Ce0b3b3bee47b4424aaa208d619ce86f2%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C636724772137980342&sdata=RN1qjtZSLtS010zgs0KlcwFrrB8Z7uWWGtFjdxdaamg%3D&reserved=0).</span><span class="sxs-lookup"><span data-stu-id="c3884-120">For more information, see [Improved behavior for non-replacing lookups](https://na01.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fbusiness-applications-release-notes%2FOctober18%2Fdynamics365-finance-operations%2Fnon-replacing-lookups&data=02%7C01%7C%7Ce0b3b3bee47b4424aaa208d619ce86f2%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C636724772137980342&sdata=RN1qjtZSLtS010zgs0KlcwFrrB8Z7uWWGtFjdxdaamg%3D&reserved=0).</span></span>

## <a name="bug-fixes"></a><span data-ttu-id="c3884-121">Villuleiðréttingar</span><span class="sxs-lookup"><span data-stu-id="c3884-121">Bug fixes</span></span>

<span data-ttu-id="c3884-122">Þessi útgáfa inniheldur nokkrar villuleiðréttingar í viðbót, þar á meðal tilvísanir í ACA, ADA, og I9 og verða nú aðeins gerðar virkar í bandarískum fyrirtækjum.</span><span class="sxs-lookup"><span data-stu-id="c3884-122">This release includes several additional bug fixes, including references to ACA, ADA, and I9 now will only be enabled in US companies.</span></span>
