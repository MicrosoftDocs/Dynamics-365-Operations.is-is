---
title: Setja upp ástæðukóða
description: Dynamics 365 Human Resources notar ástæðukóða til að útskýra hvers vegna fríðindi starfsmanns er að breytast.
author: andreabichsel
manager: tfehr
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c799a81f38a5dbd5996afbda9529fa83d7fe5cf9
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/17/2021
ms.locfileid: "5468396"
---
# <a name="set-up-reason-codes"></a><span data-ttu-id="a9f61-103">Setja upp ástæðukóða</span><span class="sxs-lookup"><span data-stu-id="a9f61-103">Set up reason codes</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="a9f61-104">Dynamics 365 Human Resources notar ástæðukóða til að útskýra hvers vegna fríðindi starfsmanns er að breytast.</span><span class="sxs-lookup"><span data-stu-id="a9f61-104">Dynamics 365 Human Resources uses reason codes to explain why an employee’s benefits are changing.</span></span>

> [!NOTE]
> <span data-ttu-id="a9f61-105">Frá og með janúar 2021 flytjast ástæðukóðar yfir á vinnusvæðið **Starfsmannastjórnun** í staðinn fyrir vinnusvæðið **Fríðindastjórnun**.</span><span class="sxs-lookup"><span data-stu-id="a9f61-105">As of January 2021, reason codes are migrating to the **Personnel management** workspace instead of the **Benefits management** workspace.</span></span> <span data-ttu-id="a9f61-106">Frekari upplýsingar er að finna í [Flytja ástæðukóða handvirkt yfir í starfsmannastjórnun](hr-benefits-setup-reason-codes.md#manually-migrate-reason-codes-to-personnel-management).</span><span class="sxs-lookup"><span data-stu-id="a9f61-106">For more information, see [Manually migrate reason codes to Personnel management](hr-benefits-setup-reason-codes.md#manually-migrate-reason-codes-to-personnel-management).</span></span>

## <a name="create-reason-codes"></a><span data-ttu-id="a9f61-107">Stofna ástæðukóða</span><span class="sxs-lookup"><span data-stu-id="a9f61-107">Create reason codes</span></span>

1. <span data-ttu-id="a9f61-108">Á vinnusvæðinu **Starfsmannastjórnun** (eða vinnusvæðinu **Fríðindastjórnun** ef ástæðukóðarnir hafa ekki verið fluttir enn) skal velja **Tenglar** og síðan velja **Ástæðukóðar**.</span><span class="sxs-lookup"><span data-stu-id="a9f61-108">In the **Personnel management** workspace (or **Benefits management** workspace if your reason codes haven't yet migrated), select **Links**, and then select **Reason codes**.</span></span>

2. <span data-ttu-id="a9f61-109">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="a9f61-109">Select **New**.</span></span>

3. <span data-ttu-id="a9f61-110">Tilgreina gildi fyrir eftirfarandi reiti:</span><span class="sxs-lookup"><span data-stu-id="a9f61-110">Specify values for the following fields:</span></span>

   | <span data-ttu-id="a9f61-111">Svæði</span><span class="sxs-lookup"><span data-stu-id="a9f61-111">Field</span></span> | <span data-ttu-id="a9f61-112">Lýsing</span><span class="sxs-lookup"><span data-stu-id="a9f61-112">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="a9f61-113">**Ástæðukóði**</span><span class="sxs-lookup"><span data-stu-id="a9f61-113">**Reason code**</span></span> | <span data-ttu-id="a9f61-114">Einstakt nafn til að bera kennsl á ástæðu þess að starfsmaður myndi breyta skráningu í fríðindaáætlun.</span><span class="sxs-lookup"><span data-stu-id="a9f61-114">A unique name to identify the reason an employee would change a benefit plan enrollment.</span></span> |
   | <span data-ttu-id="a9f61-115">**Lýsing**</span><span class="sxs-lookup"><span data-stu-id="a9f61-115">**Description**</span></span> | <span data-ttu-id="a9f61-116">Lýsing á ástæðukóðanum.</span><span class="sxs-lookup"><span data-stu-id="a9f61-116">A description of the reason code.</span></span> |

4. <span data-ttu-id="a9f61-117">Undir **Aðstæður sem eiga við** skal stilla **Fríðindastjórnun** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="a9f61-117">Under **Applicable scenarios**, set **Benefits management** to **Yes**.</span></span> <span data-ttu-id="a9f61-118">(Á ekki við ef ástæðukóðar hafa ekki enn verið yfirfærðir á vinnusvæðið **Starfsmannastjórnun**.)</span><span class="sxs-lookup"><span data-stu-id="a9f61-118">(Not applicable if your reason codes haven't yet migrated to the **Personnel management** workspace.)</span></span>

5. <span data-ttu-id="a9f61-119">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="a9f61-119">Select **Save**.</span></span>

## <a name="manually-migrate-reason-codes-to-personnel-management"></a><span data-ttu-id="a9f61-120">Flytja ástæðukóða handvirkt yfir í starfsmannastjórnun</span><span class="sxs-lookup"><span data-stu-id="a9f61-120">Manually migrate reason codes to Personnel management</span></span>

<span data-ttu-id="a9f61-121">Í janúar 2021 verða ástæðukóðar fluttir yfir á vinnusvæðið **Starfsmannastjórnun** í staðinn fyrir vinnusvæðið **Fríðindastjórnun**.</span><span class="sxs-lookup"><span data-stu-id="a9f61-121">In January 2021, reason codes are migrating to the **Personnel management** workspace instead of the **Benefits management** workspace.</span></span> <span data-ttu-id="a9f61-122">Flest gögn ástæðukóða munu flytjast sjálfkrafa yfir í umhverfið.</span><span class="sxs-lookup"><span data-stu-id="a9f61-122">Most reason code data will automatically migrate in your environment.</span></span> <span data-ttu-id="a9f61-123">Hugsanlega flytjast ekki sum gögn ástæðukóða.</span><span class="sxs-lookup"><span data-stu-id="a9f61-123">Some reason code data might not migrate.</span></span> <span data-ttu-id="a9f61-124">Sem dæmi þá eru ástæðukóðar nú með 15 stafi að hámarki, þannig að ástæðukóðar sem eru lengri en 15 stafir munu ekki flytjast sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="a9f61-124">For example, reason codes now have a 15-character maximum, so any reason codes longer than 15 characters won't migrate automatically.</span></span>

<span data-ttu-id="a9f61-125">Borði birtist á síðunni **Tenglar** á vinnusvæðinu **Fríðindastjórnun** sem gefur flutninginn til kynna og hvort einhverjir ástæðukóðar flytjist ekki.</span><span class="sxs-lookup"><span data-stu-id="a9f61-125">You'll see a banner on the **Links** page of the **Benefits management** workspace informing you about the migration and whether any reason codes didn't migrate.</span></span>

1. <span data-ttu-id="a9f61-126">Veljið **Ástæðukóðar** fyrir upplýsingar um stöðu flutnings.</span><span class="sxs-lookup"><span data-stu-id="a9f61-126">Select **Reason codes** for details about migration status.</span></span>

   <span data-ttu-id="a9f61-127">[![Ástæðukóðar](./media/hr-benefits-setup-reason-codes-link.png)](./media/hr-benefits-setup-reason-codes-link.png)</span><span class="sxs-lookup"><span data-stu-id="a9f61-127">[![Reason codes](./media/hr-benefits-setup-reason-codes-link.png)](./media/hr-benefits-setup-reason-codes-link.png)</span></span>

2. <span data-ttu-id="a9f61-128">Veljið ástæðukóða sem ekki tókst að flytja.</span><span class="sxs-lookup"><span data-stu-id="a9f61-128">Select a reason code that failed to migrate.</span></span>

   <span data-ttu-id="a9f61-129">[![Staða á flutningi ástæðukóða](./media/hr-benefits-setup-reason-codes-status.png)](./media/hr-benefits-setup-reason-codes-status.png)</span><span class="sxs-lookup"><span data-stu-id="a9f61-129">[![Reason code migration status](./media/hr-benefits-setup-reason-codes-status.png)](./media/hr-benefits-setup-reason-codes-status.png)</span></span>

3. <span data-ttu-id="a9f61-130">Veljið **Yfirfæra ástæðukóða**.</span><span class="sxs-lookup"><span data-stu-id="a9f61-130">Select **Migrate reason code**.</span></span>

   <span data-ttu-id="a9f61-131">[![Yfirfæra ástæðukóða](./media/hr-benefits-setup-reason-codes-migrate.png)](./media/hr-benefits-setup-reason-codes-migrate.png)</span><span class="sxs-lookup"><span data-stu-id="a9f61-131">[![Migrate reason code](./media/hr-benefits-setup-reason-codes-migrate.png)](./media/hr-benefits-setup-reason-codes-migrate.png)</span></span>

4. <span data-ttu-id="a9f61-132">Í glugganum **Yfirfærsla ástæðukóða fríðinda** eru tvær möguleikar á vörpun í ástæðukóða starfsmannastjórnunar:</span><span class="sxs-lookup"><span data-stu-id="a9f61-132">In the **Benefit reason code migration** pane, you have two options for mapping to a Personnel management reason code:</span></span>

   - <span data-ttu-id="a9f61-133">Til að nota fyrirliggjandi ástæðukóða í starfsmannastjórnun skal velja einn úr fellilistanum **Nota fyrirliggjandi ástæðukóða**.</span><span class="sxs-lookup"><span data-stu-id="a9f61-133">To use an existing reason code in Personnel management, choose one from the **Use existing reason code** dropdown.</span></span>
     > [!NOTE]
     > <span data-ttu-id="a9f61-134">Aðeins er hægt að nota fyrirliggjandi ástæðukóða í starfsmannastjórnun ef annar ástæðukóði fríðindastjórnunar hefur ekki enn verið færður í hana.</span><span class="sxs-lookup"><span data-stu-id="a9f61-134">You can only use an existing reason code in Personnel management if another Benefits management reason code hasn't already migrated to it.</span></span>
   - <span data-ttu-id="a9f61-135">Til að stofna nýjan ástæðukóða í starfsmannastjórnun skal slá nýjan inn í **Nýr ástæðukóði** og síðan færa inn lýsingu í **Ný lýsing**.</span><span class="sxs-lookup"><span data-stu-id="a9f61-135">To create a new reason code in Personnel management, enter a new one in **New reason code**, and then enter a description in **New description**.</span></span>

   <span data-ttu-id="a9f61-136">[![Varpa í ástæðukóða starfsmannastjórnunar](./media/hr-benefits-setup-reason-codes-mapping.png)](./media/hr-benefits-setup-reason-codes-mapping.png)</span><span class="sxs-lookup"><span data-stu-id="a9f61-136">[![Map to a Personnel management reason code](./media/hr-benefits-setup-reason-codes-mapping.png)](./media/hr-benefits-setup-reason-codes-mapping.png)</span></span>

<span data-ttu-id="a9f61-137">Þegar ástæðukóðar hafa verið fluttir yfir í starfsmannastjórnun er möguleikinn á að nota þá í fríðindastjórnun sjálfkrafa stilltur á **Já**.</span><span class="sxs-lookup"><span data-stu-id="a9f61-137">After reason codes migrate to Personnel management, the option for using them in Benefits management is automatically set to **Yes**.</span></span>

<span data-ttu-id="a9f61-138">[![Nota ástæðukóða í fríðindastjórnun](./media/hr-benefits-setup-reason-codes-use.png)](./media/hr-benefits-setup-reason-codes-use.png)</span><span class="sxs-lookup"><span data-stu-id="a9f61-138">[![Use reason code in Benefits management](./media/hr-benefits-setup-reason-codes-use.png)](./media/hr-benefits-setup-reason-codes-use.png)</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]