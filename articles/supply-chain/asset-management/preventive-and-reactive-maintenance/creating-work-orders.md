---
title: Verkbeiðnir stofnaðar
description: Þetta efni útskýrir hvernig á að stofna verkbeiðnir í eignastýringu.
author: josaw1
manager: tfehr
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f94f8bc20753e38ce1cb6eccdfbc85c2e491ffad
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206128"
---
# <a name="creating-work-orders"></a><span data-ttu-id="9ae6a-103">Verkbeiðnir stofnaðar</span><span class="sxs-lookup"><span data-stu-id="9ae6a-103">Creating work orders</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="9ae6a-104">Þegar þú hefur skipulagt forvirk viðhaldsstörf er næsta skref að búa til verkbeiðnir fyrir vinnslurnar.</span><span class="sxs-lookup"><span data-stu-id="9ae6a-104">When you have scheduled preventive maintenance jobs, next step is to create work orders for the jobs.</span></span> <span data-ttu-id="9ae6a-105">Þetta er gert í einum af viðhaldsskemunum.</span><span class="sxs-lookup"><span data-stu-id="9ae6a-105">This is done in one of the maintenance schedules.</span></span> <span data-ttu-id="9ae6a-106">Skipulagðar vinnslur í viðhaldsskema geta verið með mismunandi tilvísunargerðir:</span><span class="sxs-lookup"><span data-stu-id="9ae6a-106">The scheduled jobs in a maintenance schedule can have different reference types:</span></span>

| <span data-ttu-id="9ae6a-107">Gerð tilvísunar</span><span class="sxs-lookup"><span data-stu-id="9ae6a-107">Reference type</span></span> | <span data-ttu-id="9ae6a-108">Lýsing</span><span class="sxs-lookup"><span data-stu-id="9ae6a-108">Description</span></span>                    |
|-----------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ae6a-109">Viðhaldsáætlanir</span><span class="sxs-lookup"><span data-stu-id="9ae6a-109">Maintenance plans</span></span>     | <span data-ttu-id="9ae6a-110">Forvirk viðhaldsverk byggð á gerðum viðhaldsáætlana „Tími“ eða „Teljari“.</span><span class="sxs-lookup"><span data-stu-id="9ae6a-110">Preventive maintenance jobs based on maintenance plan types "Time" or "Counter".</span></span>                       |
| <span data-ttu-id="9ae6a-111">Viðhaldslotur</span><span class="sxs-lookup"><span data-stu-id="9ae6a-111">Maintenance rounds</span></span>    | <span data-ttu-id="9ae6a-112">Forvirk viðhaldsverk sem innihalda nokkrar eignir sem þurfa svipaða gerð viðhalds.</span><span class="sxs-lookup"><span data-stu-id="9ae6a-112">Preventive maintenance jobs containing several assets that require a similar type of maintenance.</span></span>           |
| <span data-ttu-id="9ae6a-113">Viðhaldsbeiðni</span><span class="sxs-lookup"><span data-stu-id="9ae6a-113">Maintenance request</span></span>   | <span data-ttu-id="9ae6a-114">Búið til handvirka beiðni um viðhald eða viðgerð á eign, sem hægt er að breyta í verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="9ae6a-114">Manually created request for maintenance or repair of an asset, which can be converted into a work order.</span></span> |


1. <span data-ttu-id="9ae6a-115">Smelltu á **Eignastýringu** > **Sameiginlegt** > **Allar viðhaldsáætlanir** eða **Opna viðhaldsáætlunarlínur** eða **Opna söfn viðhaldsáætlana**.</span><span class="sxs-lookup"><span data-stu-id="9ae6a-115">Click **Asset management** > **Common** > **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools**.</span></span>

2. <span data-ttu-id="9ae6a-116">Veldu áætluð viðhaldsverk sem þú vilt búa til verkbeiðni fyrir og smelltu á **Verkbeiðni**.</span><span class="sxs-lookup"><span data-stu-id="9ae6a-116">Select the scheduled maintenance jobs for which you want to create a work order and click **Work order**.</span></span> <span data-ttu-id="9ae6a-117">Í gluggann **Stofna verkbeiðnir** er heildarfjöldi spátíma fyrir valdar línur sýndur í reitnum **Tímar viðhaldsspár**.</span><span class="sxs-lookup"><span data-stu-id="9ae6a-117">In the **Create work orders** dialog, the total number of forecast hours for the selected lines is shown in the **Maintenance forecast hours** field.</span></span>

3. <span data-ttu-id="9ae6a-118">Í kaflanum **Færibreytur** skal velja hversu margar verkbeiðnir á að búa til.</span><span class="sxs-lookup"><span data-stu-id="9ae6a-118">In the **Parameters** section, select how many work orders should be created.</span></span> <span data-ttu-id="9ae6a-119">Þú getur búið til eina verkbeiðni á hverja viðhaldsáætlunarlínu, eða fjölda verkbeiðna miðað við val þitt í kaflanum **Ein verkbeiðni á**.</span><span class="sxs-lookup"><span data-stu-id="9ae6a-119">You can create one work order per maintenance schedule line, or a number of work orders based on your selections in the **One work order per** section.</span></span>

4. <span data-ttu-id="9ae6a-120">Veldu **Gerð verkbeiðni** sem verður notuð í öllum verkbeiðnum sem þú býrð til.</span><span class="sxs-lookup"><span data-stu-id="9ae6a-120">Select a **Work order type** that will be used on all the work orders you create.</span></span> <span data-ttu-id="9ae6a-121">Myndin hér að neðan sýnir dæmi um gluggann **Stofna verkbeiðnir**.</span><span class="sxs-lookup"><span data-stu-id="9ae6a-121">The illustration below shows an example of the **Create work orders** dialog.</span></span>

![Mynd 1](media/18-preventive-maintenance.png)

5. <span data-ttu-id="9ae6a-123">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="9ae6a-123">Click **OK**.</span></span> <span data-ttu-id="9ae6a-124">Ein eða fleiri verkbeiðnir eru búnar til.</span><span class="sxs-lookup"><span data-stu-id="9ae6a-124">One or more work orders are created.</span></span>

