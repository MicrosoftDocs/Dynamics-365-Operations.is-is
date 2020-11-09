---
title: Sameina sendingar þegar samstæðureglu sendingar hefur verið hnekkt á síðunni „Losa í vöruhús“
description: Þetta efnisatriði sýnir aðstæður þar sem losa þarf handvirkt eina eða fleiri sölulínur í vöruhúsið af síðunni „Losa í vöruhús“ og hnekkja þarf kerfisskilgreindri samstæðureglu sendingar áður en hún er losuð.
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, WHSShipConsolidationSetShipment, WHSShipmentConsolidation, WHSFilterGenerallyAvail, WHSReleaseToWarehouse
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 96f994e9f3440721105545f96d7d8475fcab2b6b
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016794"
---
# <a name="consolidate-shipments-when-the-shipment-consolidation-policy-is-overridden-from-the-release-to-warehouse-page"></a><span data-ttu-id="21997-103">Sameina sendingar þegar samstæðureglu sendingar hefur verið hnekkt á síðunni „Losa í vöruhús“</span><span class="sxs-lookup"><span data-stu-id="21997-103">Consolidate shipments when the shipment consolidation policy is overridden from the Release to warehouse page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="21997-104">Þetta efnisatriði sýnir aðstæður þar sem losa þarf handvirkt eina eða fleiri sölulínur í vöruhúsið af síðunni **Losa í vöruhús** og hnekkja þarf kerfisskilgreindri samstæðureglu sendingar áður en hún er losuð.</span><span class="sxs-lookup"><span data-stu-id="21997-104">This topic presents a scenario where one or more sales lines must be manually released to the warehouse from the **Release to warehouse** page, and the system-defined shipment consolidation policy must be overridden before the release.</span></span> <span data-ttu-id="21997-105">Hugsanlega þarf að hnekkja samstæðureglu sendingar, t.d. ef sameina þarf pöntun sem er ekki vanalega sameinuð með opnum sendingum við opnar sendingar.</span><span class="sxs-lookup"><span data-stu-id="21997-105">An override of the shipment consolidation policy might be required if, for example, an order that isn't usually consolidated with open shipments must be consolidated with open shipments.</span></span>

<span data-ttu-id="21997-106">Við aðstæðurnar er stofnarðu sölupantanir og hnekkir svo sjálfgefinni samstæðureglu sendingar áður en pöntunum er sleppt í vöruhúsið.</span><span class="sxs-lookup"><span data-stu-id="21997-106">During the scenario, you will create a set of sales orders and then override the default shipment consolidation policy before you release the orders to the warehouse.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="21997-107">Bjóða upp á sýnigögn</span><span class="sxs-lookup"><span data-stu-id="21997-107">Make demo data available</span></span>

<span data-ttu-id="21997-108">Aðstæður í þessu efnisatriði vísa í gildi og færslur sem eru innifaldar í stöðluðum sýnigögnum fyrir Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="21997-108">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="21997-109">Ef nota á gildin sem er boðið upp á hér eins og í æfingunum skal gæta þess að vinna í umhverfi þar sem sýnigögnin eru uppsett og stilla lögaðilann á **USMF** áður en hafist er handa.</span><span class="sxs-lookup"><span data-stu-id="21997-109">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="21997-110">Setja upp samstæðureglur sendingar og afurðarsíur</span><span class="sxs-lookup"><span data-stu-id="21997-110">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="21997-111">Aðstæðurnar sem hér er lýst gera ráð fyrir að þegar hafi verið kveikt á eiginleikanum, farið hafi verið í gegnum æfingarnar í [Skilgreina samstæðureglur sendingar](configure-shipment-consolidation-policies.md) og reglur og aðrar færslur sem þar er lýst stofnaðar.</span><span class="sxs-lookup"><span data-stu-id="21997-111">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="21997-112">Gætið þess að gera þessar æfingar áður en haldið er áfram með þessar aðstæður.</span><span class="sxs-lookup"><span data-stu-id="21997-112">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="21997-113">Búa til sölupantanir fyrir þessar aðstæður</span><span class="sxs-lookup"><span data-stu-id="21997-113">Create the sales orders for this scenario</span></span>

1. <span data-ttu-id="21997-114">Opnaðu **Viðskiptakröfur \> Pantanir \> Allar sölupantanir** og búðu til þrjár eins sölupantanir með eftirfarandi stillingum:</span><span class="sxs-lookup"><span data-stu-id="21997-114">Go to **Accounts receivable \> Orders \> All sales orders** , and create three identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="21997-115">**Viðskiptavinalykill:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="21997-115">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="21997-116">Bættu við pöntunarlínu sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="21997-116">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="21997-117">**Vörunúmer:** *A0001* (vara sem engin sía fyrir **kóða 4** er úthlutað á)</span><span class="sxs-lookup"><span data-stu-id="21997-117">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="21997-118">**Magn:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="21997-118">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="21997-119">Veljið **Birgðir \> Frátekning** og síðan, á aðgerðasvæðinu, veljið **Frátektarlota** til að taka frá pöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="21997-119">Select **Inventory \> Reservation** , and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="release-the-sales-orders-from-the-release-to-warehouse-page"></a><span data-ttu-id="21997-120">Losa sölupantanir af síðunni Losa í vöruhús</span><span class="sxs-lookup"><span data-stu-id="21997-120">Release the sales orders from the Release to warehouse page</span></span>

<span data-ttu-id="21997-121">Fylgið eftirfarandi skrefum til að hnekkja samstæðureglu sendingar við losun í vöruhúsið.</span><span class="sxs-lookup"><span data-stu-id="21997-121">Follow these steps to override the shipment consolidation policy during the release to the warehouse.</span></span>

1. <span data-ttu-id="21997-122">Opnaðu **Vöruhúsakerfi \> Losa í vöruhús \> Losa í vöruhús**.</span><span class="sxs-lookup"><span data-stu-id="21997-122">Go to **Warehouse management \> Release to warehouse \> Release to warehouse**.</span></span>
1. <span data-ttu-id="21997-123">Í efri rúðu skal velja fyrstu sölupöntunina sem var stofnuð fyrir þessar aðstæður.</span><span class="sxs-lookup"><span data-stu-id="21997-123">In the upper pane, select the first sales order that you created for this scenario.</span></span>
1. <span data-ttu-id="21997-124">Veljið **Bæta við** til að bæta línunni við losun í vöruhúsið.</span><span class="sxs-lookup"><span data-stu-id="21997-124">Select **Add** to add the line to the release to the warehouse.</span></span> <span data-ttu-id="21997-125">Takið eftir að *Sjálfgefið* samstæðureglu sendingar er beitt í neðstu rúðu.</span><span class="sxs-lookup"><span data-stu-id="21997-125">Notice that the *Default* shipment consolidation policy is applied in the bottom pane.</span></span>
1. <span data-ttu-id="21997-126">Á neðsta svæðinu skal velja **Velja nýja samstæðureglu sendingar**.</span><span class="sxs-lookup"><span data-stu-id="21997-126">In the bottom pane, select **Select new shipment consolidation policy**.</span></span>
1. <span data-ttu-id="21997-127">Veljið reglu sem leyfir samstæðu við aðrar opnar sendingar sömu reglu.</span><span class="sxs-lookup"><span data-stu-id="21997-127">Select a policy that allows for consolidation with other open shipments of the same policy.</span></span> <span data-ttu-id="21997-128">Veljið til dæmis regluna *CustomerOrderNo*.</span><span class="sxs-lookup"><span data-stu-id="21997-128">For example, select the *CustomerOrderNo* policy.</span></span>
1. <span data-ttu-id="21997-129">Velja **Losa í vöruhús**.</span><span class="sxs-lookup"><span data-stu-id="21997-129">Select **Release to warehouse**.</span></span>
1. <span data-ttu-id="21997-130">Velja skal aðra og þriðju sölupöntun sem voru stofnaðar fyrir þessar aðstæður.</span><span class="sxs-lookup"><span data-stu-id="21997-130">Select the second and third sales orders that you created for this scenario.</span></span>
1. <span data-ttu-id="21997-131">Veljið **Bæta við** til að bæta línunum við losunina í vöruhúsið.</span><span class="sxs-lookup"><span data-stu-id="21997-131">Select **Add** to add the lines to the release to the warehouse.</span></span> <span data-ttu-id="21997-132">Takið eftir að *Sjálfgefið* reglunni er beitt í neðstu rúðu.</span><span class="sxs-lookup"><span data-stu-id="21997-132">Notice that the *Default* policy is applied in the bottom pane.</span></span>
1. <span data-ttu-id="21997-133">Velja skal aðra línuna og síðan, í **Velja nýja samstæðureglu sendingar** , velja *CustomerOrderNo* regluna.</span><span class="sxs-lookup"><span data-stu-id="21997-133">Select the second line, and then, in the **Select new shipment consolidation policy** field, select the *CustomerOrderNo* policy.</span></span>
1. <span data-ttu-id="21997-134">Veljið **Losa í vöruhús** fyrir báðar línurnar.</span><span class="sxs-lookup"><span data-stu-id="21997-134">Select **Release to warehouse** for both lines.</span></span>

## <a name="verify-the-shipments"></a><span data-ttu-id="21997-135">Staðfesta skal sendingarnar</span><span class="sxs-lookup"><span data-stu-id="21997-135">Verify the shipments</span></span>

<span data-ttu-id="21997-136">Tvær sendingar ættu að hafa verið stofnaðar:</span><span class="sxs-lookup"><span data-stu-id="21997-136">Two shipments should have been created:</span></span>

- <span data-ttu-id="21997-137">Fyrsta sendingin inniheldur tvær línur og var búin til með því að nota samstæðureglu sendingar *CustomerOrderNo*.</span><span class="sxs-lookup"><span data-stu-id="21997-137">The first shipment contains two lines and was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>
- <span data-ttu-id="21997-138">Önnur sendingin inniheldur eina línu og var búin til með því að nota samstæðuregluna *Sjálfgefið*.</span><span class="sxs-lookup"><span data-stu-id="21997-138">The second shipment contains one line and was created by using the *Default* shipment consolidation policy.</span></span>

<span data-ttu-id="21997-139">Fylgdu þessum skrefum til að yfirfara sendingar sem voru stofnaðar.</span><span class="sxs-lookup"><span data-stu-id="21997-139">Follow these steps to review the shipments that were created.</span></span>

1. <span data-ttu-id="21997-140">Opnið **Vöruhúsakerfi \> Sendingar \> Allar sendingar**.</span><span class="sxs-lookup"><span data-stu-id="21997-140">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="21997-141">Finnið og veljið þá sendingu sem um ræðir.</span><span class="sxs-lookup"><span data-stu-id="21997-141">Find and select the required shipment.</span></span>
1. <span data-ttu-id="21997-142">Í svæðið **Samstæðuregla sendingar** skal fara yfir samstæðuregluna sem var notuð þegar sendingin var stofnuð.</span><span class="sxs-lookup"><span data-stu-id="21997-142">In the **Shipment consolidation policy** field, review the consolidation policy that was used when the shipment was created.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="21997-143">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="21997-143">Additional resources</span></span>

- [<span data-ttu-id="21997-144">Samstæðureglur sendingar</span><span class="sxs-lookup"><span data-stu-id="21997-144">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="21997-145">Skilgreina samstæðureglur sendingar</span><span class="sxs-lookup"><span data-stu-id="21997-145">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)
