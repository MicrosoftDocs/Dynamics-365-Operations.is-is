---
title: "Stofna þjónustupantanir sjálfkrafa"
description: "Þú getur búið til þjónustupantanir fyrir eina þjónustusamning eða fyrir nokkra þjónustusamninga."
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: ee68190b117b974ff4131f5d2237d138cac1fda3
ms.contentlocale: is-is
ms.lasthandoff: 08/07/2018

---

# <a name="create-service-orders-automatically"></a><span data-ttu-id="d6801-103">Stofna þjónustupantanir sjálfkrafa</span><span class="sxs-lookup"><span data-stu-id="d6801-103">Create service orders automatically</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="d6801-104">Þú getur búið til þjónustupantanir fyrir eina þjónustusamning eða fyrir nokkra þjónustusamninga.</span><span class="sxs-lookup"><span data-stu-id="d6801-104">You can create service orders for one service agreement or for several service agreements.</span></span> <span data-ttu-id="d6801-105">Þegar þær eru búnar til, er hægt að skoða þjónustupantanir þínar í **þjónustupantanir** skjámynd.</span><span class="sxs-lookup"><span data-stu-id="d6801-105">When they are created, you can view your service orders in the **Service orders** form.</span></span>

<span data-ttu-id="d6801-106">Þjónustupantanir eru aðeins búnar til fyrir gildistíma þjónustusamningsins.</span><span class="sxs-lookup"><span data-stu-id="d6801-106">Service orders are created only for the valid period of the service agreement.</span></span> <span data-ttu-id="d6801-107">Ef bilið sem þú tilgreinir í **Búa til þjónustupantanir** er fyrir upphafsdag eða eftir lokadag þjónustusamningsins eru þjónustupantanir aðeins búnar til fyrir þann hluta bilsins sem er innan dagsetningar þjónustusamningsins.</span><span class="sxs-lookup"><span data-stu-id="d6801-107">If the interval that you specify in the **Create service orders** form is before the starting date or after the ending date of the service agreement, service orders are created only for the part of the interval that is within the service agreement dates.</span></span>

<span data-ttu-id="d6801-108">Þegar þú stofnar þjónustupantanir handvirkt eða sjálfvirkt úr þjónustusamningslínu, verður þjónustupöntunin að vera á því tímabili sem er skilgreint af upphafs- og lokadagsetningu línunnar nema þú setir ekki lokadag á línu.</span><span class="sxs-lookup"><span data-stu-id="d6801-108">When you create service orders manually or automatically from the service agreement line, the service order must be in the time interval that is defined by the starting and ending dates for the line, unless you do not specify an ending date on the line.</span></span>

## <a name="create-service-orders-automatically-for-a-service-agreement"></a><span data-ttu-id="d6801-109">Stofna þjónustupantanir fyrir þjónustusamning sjálfvirkt</span><span class="sxs-lookup"><span data-stu-id="d6801-109">Create service orders automatically for a service agreement</span></span>

1.  <span data-ttu-id="d6801-110">Smellið á **Þjónustustjórnun** \> **Almennt** \> **Þjónustusamningar** \> **þjónustusamningar**.</span><span class="sxs-lookup"><span data-stu-id="d6801-110">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="d6801-111">Velja þjónustusamning.</span><span class="sxs-lookup"><span data-stu-id="d6801-111">Select a service agreement.</span></span>

3.  <span data-ttu-id="d6801-112">Smelltu á **Afhenda** flipann og smelltu síðan **Áætlað þjónustupantanir**.</span><span class="sxs-lookup"><span data-stu-id="d6801-112">Click the **Deliver** tab, and then click **Planned service orders**.</span></span>

4.  <span data-ttu-id="d6801-113">Tilgreindu dagsetningar í **Frá dagsetningu** og **Til dagsetningar** reitum til að skilgreina þjónustutímabilið.</span><span class="sxs-lookup"><span data-stu-id="d6801-113">Specify dates in the **From date** and **To date** fields to define the service period.</span></span>

5.  <span data-ttu-id="d6801-114">Veldu **Sýna upplýsingaskrá** gátreitur til að birta lista yfir þjónustupantanir sem eru búin til.</span><span class="sxs-lookup"><span data-stu-id="d6801-114">Select the **Show Infolog** check box to display a list of the service orders that are created.</span></span>

6.  <span data-ttu-id="d6801-115">Veldu færslugerðir í reitahópnum **Nær yfir færslugerðir**.</span><span class="sxs-lookup"><span data-stu-id="d6801-115">Select transaction types in the **Include transaction types** field group.</span></span> <span data-ttu-id="d6801-116">Færslugerðirnar tákna línurnar sem eru búnar til í þjónustusamningnum og hver færslugerð sem þú velur býr til nokkrar þjónustupantanir, allt eftir því þjónustutímabili sem er tilgreint á þjónustusamningslínu.</span><span class="sxs-lookup"><span data-stu-id="d6801-116">The transaction types represent the lines that are created in the service agreement, and each transaction type that you select generates several service orders, depending on the service interval that is specified on the service agreement line.</span></span>

7.  <span data-ttu-id="d6801-117">Til að búa til einhverjar þjónustupantanir sem vantar í samfelldri röð þjónustupantana skaltu velja gátreitur **Samfellt**.</span><span class="sxs-lookup"><span data-stu-id="d6801-117">To create any service orders that are missing from continuous series of service orders, select the **Continuous** check box.</span></span>

8.  <span data-ttu-id="d6801-118">Smellið á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="d6801-118">Click **OK**.</span></span>

## <a name="create-service-orders-automatically-for-several-service-agreements"></a><span data-ttu-id="d6801-119">Stofna þjónustupantanir fyrir marga þjónustusamninga sjálfvirkt</span><span class="sxs-lookup"><span data-stu-id="d6801-119">Create service orders automatically for several service agreements</span></span>

1.  <span data-ttu-id="d6801-120">Smelltu á **þjónustukerfi** \> **Reglubundið** \> **þjónustupantanir** \> **Búa til þjónustupantanir**.</span><span class="sxs-lookup"><span data-stu-id="d6801-120">Click **Service management** \> **Periodic** \> **Service orders** \> **Create service orders**.</span></span>

2.  <span data-ttu-id="d6801-121">Smelltu á **Velja** til að velja að bæta við eða fjarlægja viðmiðanir til að nota til að búa til þjónustupantanir.</span><span class="sxs-lookup"><span data-stu-id="d6801-121">Click **Select** to make selections to add or remove criteria to use to create service orders.</span></span>

3.  <span data-ttu-id="d6801-122">Smellið á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="d6801-122">Click **OK**.</span></span>

## <a name="see-also"></a><span data-ttu-id="d6801-123">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="d6801-123">See also</span></span>

[<span data-ttu-id="d6801-124">Þjónustupantanir</span><span class="sxs-lookup"><span data-stu-id="d6801-124">Service orders</span></span>](service-orders.md)

[<span data-ttu-id="d6801-125">Býr til þjónustupantanir sjálfvirkt</span><span class="sxs-lookup"><span data-stu-id="d6801-125">Automatically creating service orders</span></span>](auto-create-service-orders.md)

  



