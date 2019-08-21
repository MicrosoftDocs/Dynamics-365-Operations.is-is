---
title: Stofna skilgreiningarveitendur og merkja þá sem virka
description: Þetta efni útskýrir hvernig notandi sem er úthlutað á hlutverk kerfisstjóra eða þróunaraðila rafrænnar skýrslulausnar getur stofnað skilgreiningarveitu fyrir rafræna skýrslugerð (ER) í Dynamics 365 for Finance and Operations.
author: NickSelin
manager: AnnBe
ms.date: 07/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERVendorTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0dfbcf70493a43320e17d4d2734fe6343d43eaf3
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/02/2019
ms.locfileid: "1850328"
---
# <a name="create-configuration-providers-and-mark-them-as-active"></a><span data-ttu-id="cd9b7-103">Stofna skilgreiningarveitendur og merkja þá sem virka</span><span class="sxs-lookup"><span data-stu-id="cd9b7-103">Create configuration providers and mark them as active</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cd9b7-104">Þetta efni útskýrir hvernig notandi sem er úthlutað á hlutverk kerfisstjóra eða þróunaraðila rafrænnar skýrslulausnar getur stofnað skilgreiningarveitu fyrir rafræna skýrslugerð (ER) í Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="cd9b7-104">This topic explains how a user assigned to the System Administrator or Electronic Reporting Developer role can create a configuration provider for Electronic reporting (ER) in Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="cd9b7-105">Hverja skilgreiningu rafrænnar skýrslugerðar vísar til veitu sem höfund skilgreiningar.</span><span class="sxs-lookup"><span data-stu-id="cd9b7-105">Each ER configuration will refer to the provider as the author of the configuration.</span></span> <span data-ttu-id="cd9b7-106">Í þessu dæmi, verður að stofna skilgreiningu fyrir dæmi um fyrirtæki, Litware, Inc. Þessi skref má framkvæma í hvaða fyrirtæki sem er þar sem ER skilgreiningar eru samnýttar á milli fyrirtækja.</span><span class="sxs-lookup"><span data-stu-id="cd9b7-106">In this example, you will create a configuration provider for sample company, Litware, Inc. These steps can be performed in any company as ER configuration providers are shared among all companies.</span></span>

## <a name="create-a-provider"></a><span data-ttu-id="cd9b7-107">Búa til veitu</span><span class="sxs-lookup"><span data-stu-id="cd9b7-107">Create a provider</span></span>
1. <span data-ttu-id="cd9b7-108">Farðu í **skoðunarrúðu** efst í vinstra horninu og veldu **Fyrirtækisstjórnun**.</span><span class="sxs-lookup"><span data-stu-id="cd9b7-108">Go to the **navigation pane** in the upper left corner and select **Organization administration**.</span></span>
2. <span data-ttu-id="cd9b7-109">Farðu í **Vinnusvæði > Rafræn skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="cd9b7-109">Go to **Workspaces > Electronic reporting**.</span></span>
3. <span data-ttu-id="cd9b7-110">Farðu í **Skyldir tenglar> Skilgreiningarveitur**.</span><span class="sxs-lookup"><span data-stu-id="cd9b7-110">Go to **Related links > Configuration providers**.</span></span>
4. <span data-ttu-id="cd9b7-111">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="cd9b7-111">Select **New**.</span></span>
    - <span data-ttu-id="cd9b7-112">Skrá veitu er einkvæmt hvað varðar heiti og vefslóð.</span><span class="sxs-lookup"><span data-stu-id="cd9b7-112">A provider record has a unique name and URL.</span></span> <span data-ttu-id="cd9b7-113">Yfirfarið innihald þessarar síðu og sleppið ferlinu ef færsla fyrir Litware, Inc. (https://www.litware.com) er þegar til.</span><span class="sxs-lookup"><span data-stu-id="cd9b7-113">Review the content of this page and skip this procedure if a record for Litware, Inc. (https://www.litware.com) already exists.</span></span>  
5. <span data-ttu-id="cd9b7-114">Í svæðið Heiti skaltu færa inn `Litware, Inc.`.</span><span class="sxs-lookup"><span data-stu-id="cd9b7-114">In the Name field, type `Litware, Inc.`.</span></span>
6. <span data-ttu-id="cd9b7-115">Í reitinn Vefsvæði skal slá inn `https://www.litware.com`.</span><span class="sxs-lookup"><span data-stu-id="cd9b7-115">In the Internet address field, type `https://www.litware.com`.</span></span>
7. <span data-ttu-id="cd9b7-116">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="cd9b7-116">Select **Save**.</span></span>
8. <span data-ttu-id="cd9b7-117">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="cd9b7-117">Close the page.</span></span>

## <a name="select-as-an-active-provider"></a><span data-ttu-id="cd9b7-118">Veljið sem virka veitu</span><span class="sxs-lookup"><span data-stu-id="cd9b7-118">Select as an active provider</span></span>
1. <span data-ttu-id="cd9b7-119">Velja “Litware, Inc.” veitu</span><span class="sxs-lookup"><span data-stu-id="cd9b7-119">Select the Litware, Inc. provider.</span></span>
2. <span data-ttu-id="cd9b7-120">Veldu **Stilla sem virkt**.</span><span class="sxs-lookup"><span data-stu-id="cd9b7-120">Select **Set active**.</span></span>

