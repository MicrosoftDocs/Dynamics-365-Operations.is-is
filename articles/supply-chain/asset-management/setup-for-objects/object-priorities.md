---
title: Þjónustustig eigna
description: Þetta efni skýrir eignaþjónustustig í eignastýringu.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4163d059fda4ae0120d5c989e744c5a5fe0f5892
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808292"
---
# <a name="asset-service-levels"></a><span data-ttu-id="ca772-103">Þjónustustig eigna</span><span class="sxs-lookup"><span data-stu-id="ca772-103">Asset service levels</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="ca772-104">Þetta efni skýrir eignaþjónustustig í eignastýringu.</span><span class="sxs-lookup"><span data-stu-id="ca772-104">This topic explains asset service levels in Asset Management.</span></span> <span data-ttu-id="ca772-105">Stig eignaþjónustunnar eru tengd eignum og eru færð yfir í viðhaldsbeiðnir og verkbeiðnir.</span><span class="sxs-lookup"><span data-stu-id="ca772-105">Asset service levels are related to assets, and are transferred to maintenance requests and work orders.</span></span> <span data-ttu-id="ca772-106">Þau eru notuð til að reikna út forgang verkbeiðna við tímasetningu verkbeiðna.</span><span class="sxs-lookup"><span data-stu-id="ca772-106">They are used to calculate the priority of work orders during work order scheduling.</span></span> <span data-ttu-id="ca772-107">Hægt er að breyta þjónustustigum eigna ef þörf er á.</span><span class="sxs-lookup"><span data-stu-id="ca772-107">Asset service levels can be changed, if changes are required.</span></span>

<span data-ttu-id="ca772-108">Nánari upplýsingar um uppsetninguna sem er tengd útreikningi á matseinkunnum fyrir tímasetningar verkbeiðni, sjá [Færibreytur eignastýringar](../setup-for-objects/enterprise-asset-management-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="ca772-108">For more information about the setup that is related to the calculation of rating scores for work order scheduling, see [Asset Management parameters](../setup-for-objects/enterprise-asset-management-parameters.md).</span></span> <span data-ttu-id="ca772-109">Þú verður að setja upp að minnsta kosti eina sjálfgefna skrá fyrir þjónustustig eigna.</span><span class="sxs-lookup"><span data-stu-id="ca772-109">You must set up at least one default record for the asset service level.</span></span> <span data-ttu-id="ca772-110">Þessi sjálfgefna skrá er notuð ef engin önnur samsvörun finnst við tímasetningu verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="ca772-110">This default record is used if no other match is found during work order scheduling.</span></span>

<span data-ttu-id="ca772-111">**Dæmi 1:** Sjálfgefið þjónustustig sem er notað ef engin önnur samsvörun er að finna.</span><span class="sxs-lookup"><span data-stu-id="ca772-111">**Example 1:** The default service level that is used if no other match is found.</span></span> <span data-ttu-id="ca772-112">Í þessari skrá velurðu aðeins þjónustustig.</span><span class="sxs-lookup"><span data-stu-id="ca772-112">In this record, you select only a service level.</span></span>

<span data-ttu-id="ca772-113">**Dæmi 2:** Hátt þjónustustig sem notað er til að skipuleggja störf fyrir Volvo vörubifreiðarvél.</span><span class="sxs-lookup"><span data-stu-id="ca772-113">**Example 2:** A high service level that is used to schedule jobs for a Volvo truck engine.</span></span> <span data-ttu-id="ca772-114">Í þessari skrá velurðu viðeigandi eignategund (svo sem **Vél í vörubíl**), framleiðandi (**Volvo**), og þjónustustig.</span><span class="sxs-lookup"><span data-stu-id="ca772-114">In this record, you select a relevant asset type (such as **Truck Engine**), a manufacturer (**Volvo**), and a service level.</span></span>

## <a name="set-up-asset-service-levels"></a><span data-ttu-id="ca772-115">Setja upp þjónustustig eigna</span><span class="sxs-lookup"><span data-stu-id="ca772-115">Set up asset service levels</span></span>

1. <span data-ttu-id="ca772-116">Veldu **Eignastýring** \> **Uppsetning** \> **Eignaþjónustustig**.</span><span class="sxs-lookup"><span data-stu-id="ca772-116">Select **Asset management** \> **Setup** \> **Asset service levels**.</span></span>
2. <span data-ttu-id="ca772-117">Veljið **Ný** til að stofna nýja skrá.</span><span class="sxs-lookup"><span data-stu-id="ca772-117">Select **New** to create a record.</span></span>
3. <span data-ttu-id="ca772-118">Taktu viðeigandi val í háð því smáatriðum sem krafist er fyrir þjónustustig eigna í reitunum **Virk staðsetning**, **Gerð eigna**, **Framleiðandi**, **Fyrirmynd**, **Eignir**, **Gerð verkbeiðni**, og **Þjónustustig**.</span><span class="sxs-lookup"><span data-stu-id="ca772-118">Depending on the detail level that is required for the asset service level, make relevant selections in the **Functional location**, **Asset type**, **Manufacturer**, **Model**, **Asset**, **Work order type**, and **Service level** fields.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ca772-119">Þegar eignaþjónustustigið er notað við viðhaldsbeiðnir og verkbeiðnir fer Eignastjórn í gegnum allar færslur þjónustustigsins til að athuga hvort mögulegt sé samsvörun.</span><span class="sxs-lookup"><span data-stu-id="ca772-119">When the asset service level is used for maintenance requests and work orders, Asset Management goes through all asset service level records to check for a possible match.</span></span> <span data-ttu-id="ca772-120">Það athugar alltaf sértækustu samsetninguna fyrst.</span><span class="sxs-lookup"><span data-stu-id="ca772-120">It always checks the most specific combination first.</span></span> <span data-ttu-id="ca772-121">Með öðrum orðum, Eignastjórnun kannar fyrst hvort samsvörun finnist fyrir reitinn **Gerð verkbeiðni**.</span><span class="sxs-lookup"><span data-stu-id="ca772-121">In other words, Asset Management first checks for a match for the **Work order type** field.</span></span> <span data-ttu-id="ca772-122">Ef engin samsvörun er fundin, skoðar hún hvort samsvörun sé fyrir reitinn **Eignir**, og svo framvegis.</span><span class="sxs-lookup"><span data-stu-id="ca772-122">If no match is found, it checks for a match for the **Asset** field, and so on.</span></span> <span data-ttu-id="ca772-123">Eins og þú sérð á skipulagi síðunnar **Þjónustustig eigna** þýðir þessi hegðun að til að finna sértækustu samsetninguna, þá velur eignastjórnun hverja skrá frá hægri til vinstri fyrir leik.</span><span class="sxs-lookup"><span data-stu-id="ca772-123">As you can see in the layout of the **Asset service levels** page, this behavior means that, to find the most specific combination, Asset Management checks each record from right to left for a match.</span></span> <span data-ttu-id="ca772-124">Ef engin samsvörun er notuð er sjálfgefna skráin sem hefur ekkert val í þeim reitum notuð.</span><span class="sxs-lookup"><span data-stu-id="ca772-124">If no match is found, the default record that has no selections in those fields is used.</span></span>

4. <span data-ttu-id="ca772-125">Í reitnum **Þjónustustig** velurðu tölu sem gefur til kynna þjónustustigið (forgang).</span><span class="sxs-lookup"><span data-stu-id="ca772-125">In the **Service level** field, select a number that indicates the service level (priority).</span></span>


> [!NOTE]
> <span data-ttu-id="ca772-126">Ef þú breytir færslu eignaþjónustustigs á **Þjónustustig** síðu eftir að þú hefur þegar notað það í verkbeiðni, þjónustustig fyrir viðhaldsbeiðnir og verkbeiðnir er ekki uppfært í samræmi við það.</span><span class="sxs-lookup"><span data-stu-id="ca772-126">If you change an asset service level record on the **Asset service levels** page after you've already used it on a work order, the service level on maintenance requests and work orders isn't updated accordingly.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]