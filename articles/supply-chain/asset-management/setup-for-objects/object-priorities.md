---
title: Þjónustustig eigna
description: Þetta efni skýrir eignaþjónustustig í eignastýringu.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f079e6899a2e3949eff5945f867472c801d9e95c
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783356"
---
# <a name="asset-service-levels"></a><span data-ttu-id="723bf-103">Þjónustustig eigna</span><span class="sxs-lookup"><span data-stu-id="723bf-103">Asset service levels</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="723bf-104">Þetta efni skýrir eignaþjónustustig í eignastýringu.</span><span class="sxs-lookup"><span data-stu-id="723bf-104">This topic explains asset service levels in Asset Management.</span></span> <span data-ttu-id="723bf-105">Stig eignaþjónustunnar eru tengd eignum og eru færð yfir í viðhaldsbeiðnir og verkbeiðnir.</span><span class="sxs-lookup"><span data-stu-id="723bf-105">Asset service levels are related to assets, and are transferred to maintenance requests and work orders.</span></span> <span data-ttu-id="723bf-106">Þau eru notuð til að reikna út forgang verkbeiðna við tímasetningu verkbeiðna.</span><span class="sxs-lookup"><span data-stu-id="723bf-106">They are used to calculate the priority of work orders during work order scheduling.</span></span> <span data-ttu-id="723bf-107">Hægt er að breyta þjónustustigum eigna ef þörf er á.</span><span class="sxs-lookup"><span data-stu-id="723bf-107">Asset service levels can be changed, if changes are required.</span></span>

<span data-ttu-id="723bf-108">Nánari upplýsingar um uppsetninguna sem er tengd útreikningi á matseinkunnum fyrir tímasetningar verkbeiðni, sjá [Færibreytur eignastýringar](../setup-for-objects/enterprise-asset-management-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="723bf-108">For more information about the setup that is related to the calculation of rating scores for work order scheduling, see [Asset management parameters](../setup-for-objects/enterprise-asset-management-parameters.md).</span></span> <span data-ttu-id="723bf-109">Þú verður að setja upp að minnsta kosti eina sjálfgefna skrá fyrir þjónustustig eigna.</span><span class="sxs-lookup"><span data-stu-id="723bf-109">You must set up at least one default record for the asset service level.</span></span> <span data-ttu-id="723bf-110">Þessi sjálfgefna skrá er notuð ef engin önnur samsvörun finnst við tímasetningu verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="723bf-110">This default record is used if no other match is found during work order scheduling.</span></span>

<span data-ttu-id="723bf-111">**Dæmi 1:** Sjálfgefið þjónustustig sem er notað ef engin önnur samsvörun er að finna.</span><span class="sxs-lookup"><span data-stu-id="723bf-111">**Example 1:** The default service level that is used if no other match is found.</span></span> <span data-ttu-id="723bf-112">Í þessari skrá velurðu aðeins þjónustustig.</span><span class="sxs-lookup"><span data-stu-id="723bf-112">In this record, you select only a service level.</span></span>

<span data-ttu-id="723bf-113">**Dæmi 2:** Hátt þjónustustig sem notað er til að skipuleggja störf fyrir Volvo vörubifreiðarvél.</span><span class="sxs-lookup"><span data-stu-id="723bf-113">**Example 2:** A high service level that is used to schedule jobs for a Volvo truck engine.</span></span> <span data-ttu-id="723bf-114">Í þessari skrá velurðu viðeigandi eignategund (svo sem **Vél í vörubíl**), framleiðandi (**Volvo**), og þjónustustig.</span><span class="sxs-lookup"><span data-stu-id="723bf-114">In this record, you select a relevant asset type (such as **Truck Engine**), a manufacturer (**Volvo**), and a service level.</span></span>

## <a name="set-up-asset-service-levels"></a><span data-ttu-id="723bf-115">Setja upp þjónustustig eigna</span><span class="sxs-lookup"><span data-stu-id="723bf-115">Set up asset service levels</span></span>

1. <span data-ttu-id="723bf-116">Veldu **Eignastýring** \> **Uppsetning** \> **Eignaþjónustustig**.</span><span class="sxs-lookup"><span data-stu-id="723bf-116">Select **Asset management** \> **Setup** \> **Asset service levels**.</span></span>
2. <span data-ttu-id="723bf-117">Veljið **Ný** til að stofna nýja skrá.</span><span class="sxs-lookup"><span data-stu-id="723bf-117">Select **New** to create a record.</span></span>
3. <span data-ttu-id="723bf-118">Taktu viðeigandi val í háð því smáatriðum sem krafist er fyrir þjónustustig eigna í reitunum **Virk staðsetning**, **Gerð eigna**, **Framleiðandi**, **Fyrirmynd**, **Eignir**, **Gerð verkbeiðni**, og **Þjónustustig**.</span><span class="sxs-lookup"><span data-stu-id="723bf-118">Depending on the detail level that is required for the asset service level, make relevant selections in the **Functional location**, **Asset type**, **Manufacturer**, **Model**, **Asset**, **Work order type**, and **Service level** fields.</span></span>

    > [!NOTE]
    > <span data-ttu-id="723bf-119">Þegar eignaþjónustustigið er notað við viðhaldsbeiðnir og verkbeiðnir fer Eignastjórn í gegnum allar færslur þjónustustigsins til að athuga hvort mögulegt sé samsvörun.</span><span class="sxs-lookup"><span data-stu-id="723bf-119">When the asset service level is used for maintenance requests and work orders, Asset Management goes through all asset service level records to check for a possible match.</span></span> <span data-ttu-id="723bf-120">Það athugar alltaf sértækustu samsetninguna fyrst.</span><span class="sxs-lookup"><span data-stu-id="723bf-120">It always checks the most specific combination first.</span></span> <span data-ttu-id="723bf-121">Með öðrum orðum, Eignastjórnun kannar fyrst hvort samsvörun finnist fyrir reitinn **Gerð verkbeiðni**.</span><span class="sxs-lookup"><span data-stu-id="723bf-121">In other words, Asset Management first checks for a match for the **Work order type** field.</span></span> <span data-ttu-id="723bf-122">Ef engin samsvörun er fundin, skoðar hún hvort samsvörun sé fyrir reitinn **Eignir**, og svo framvegis.</span><span class="sxs-lookup"><span data-stu-id="723bf-122">If no match is found, it checks for a match for the **Asset** field, and so on.</span></span> <span data-ttu-id="723bf-123">Eins og þú sérð á skipulagi síðunnar **Þjónustustig eigna** þýðir þessi hegðun að til að finna sértækustu samsetninguna, þá velur eignastjórnun hverja skrá frá hægri til vinstri fyrir leik.</span><span class="sxs-lookup"><span data-stu-id="723bf-123">As you can see in the layout of the **Asset service levels** page, this behavior means that, to find the most specific combination, Asset Management checks each record from right to left for a match.</span></span> <span data-ttu-id="723bf-124">Ef engin samsvörun er notuð er sjálfgefna skráin sem hefur ekkert val í þeim reitum notuð.</span><span class="sxs-lookup"><span data-stu-id="723bf-124">If no match is found, the default record that has no selections in those fields is used.</span></span>

4. <span data-ttu-id="723bf-125">Í reitnum **Þjónustustig** velurðu tölu sem gefur til kynna þjónustustigið (forgang).</span><span class="sxs-lookup"><span data-stu-id="723bf-125">In the **Service level** field, select a number that indicates the service level (priority).</span></span>


> [!NOTE]
> <span data-ttu-id="723bf-126">Ef þú breytir færslu eignaþjónustustigs á **Þjónustustig** síðu eftir að þú hefur þegar notað það í verkbeiðni, þjónustustig fyrir viðhaldsbeiðnir og verkbeiðnir er ekki uppfært í samræmi við það.</span><span class="sxs-lookup"><span data-stu-id="723bf-126">If you change an asset service level record on the **Asset service levels** page after you've already used it on a work order, the service level on maintenance requests and work orders isn't updated accordingly.</span></span>
