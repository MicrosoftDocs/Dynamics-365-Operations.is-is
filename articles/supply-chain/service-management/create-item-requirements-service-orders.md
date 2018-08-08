---
title: "Stofna vöruþörf fyrir þjónustupantanir"
description: "Ef nauðsynlegt er að taka til ákveðnar vörur fyrir þjónustupöntunina, hægt er að stofna birgðavöruþörf fyrir hana."
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
ms.openlocfilehash: a5a730ae945af15c7bd4020c734bac971d8186e2
ms.contentlocale: is-is
ms.lasthandoff: 08/07/2018

---

# <a name="create-item-requirements-for-service-orders"></a><span data-ttu-id="57c6c-103">Stofna vöruþörf fyrir þjónustupantanir</span><span class="sxs-lookup"><span data-stu-id="57c6c-103">Create item requirements for service orders</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="57c6c-104">Þú getur búið til þjónustupöntun til að fylgjast með og stjórna þjónustu sem þú veitir viðskiptavinum þínum.</span><span class="sxs-lookup"><span data-stu-id="57c6c-104">You can create a service order to track and manage services that you provide to your customers.</span></span> <span data-ttu-id="57c6c-105">Ef nauðsynlegt er að taka til ákveðnar vörur fyrir þjónustupöntunina, hægt er að stofna birgðavöruþörf fyrir hana.</span><span class="sxs-lookup"><span data-stu-id="57c6c-105">If you need to reserve specific items for a service order, you can create inventory item requirements for it.</span></span> <span data-ttu-id="57c6c-106">Hægt er að neyta vörukröfu strax úr birgðum, eða hún getur hafið framleiðslupöntun fyrir vöruna.</span><span class="sxs-lookup"><span data-stu-id="57c6c-106">An item requirement can be immediately consumed from inventory, or it can initiate a production order for the item.</span></span>

<span data-ttu-id="57c6c-107">Með því að nota vörukröfu í staðinn fyrir vörufærsla, geturðu áætlað afhendingu rétt áður en vara er raunverulega notuð, stofnað innkaupapöntun, haft vöruna með í ramma viðskiptasamkomulags og innifalið vörukröfuna í framleiðsluáætlun.</span><span class="sxs-lookup"><span data-stu-id="57c6c-107">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span>

<span data-ttu-id="57c6c-108">Liður kröfur um þjónustu pantanir eru unnin í gegnum verkefni.</span><span class="sxs-lookup"><span data-stu-id="57c6c-108">Item requirements for service orders are processed through a project.</span></span> <span data-ttu-id="57c6c-109">Til að stofna vöruþörf í þjónustupöntun verður að úthluta þjónustupöntunina við verk.</span><span class="sxs-lookup"><span data-stu-id="57c6c-109">To create an item requirement on a service order, the service order must be assigned to a project.</span></span> <span data-ttu-id="57c6c-110">Eftir að þú hefur búið til vörukröfu fyrir þjónustupöntun getur þú skoðað vörukröfuna í skjámynd **Verkefni** fyrir verkefnið sem er valið.</span><span class="sxs-lookup"><span data-stu-id="57c6c-110">After you create an item requirement for a service order, you can view the item requirement in the **Projects** form for the selected project.</span></span>

## <a name="create-an-item-requirement-for-a-service-order"></a><span data-ttu-id="57c6c-111">Stofna vöruþörf fyrir þjónustupöntun</span><span class="sxs-lookup"><span data-stu-id="57c6c-111">Create an item requirement for a service order</span></span>

1.  <span data-ttu-id="57c6c-112">Smelltu á **Þjónustustjórnun** \> **Almennt** \> **Þjónustupantanir** \> **Þjónustupantanir**.</span><span class="sxs-lookup"><span data-stu-id="57c6c-112">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="57c6c-113">Valin þjónustupöntunin sem útbúa á vöruþörf fyrir.</span><span class="sxs-lookup"><span data-stu-id="57c6c-113">Select the service order that you want to create an item requirement for.</span></span>

3.  <span data-ttu-id="57c6c-114">Á **Aðgerðarúða**, á flipanum **Afgreiða**, skal smella á **Vörukrafa**.</span><span class="sxs-lookup"><span data-stu-id="57c6c-114">On the **Action Pane**, on the **Dispatch** tab, click **Item requirement**.</span></span>

4.  <span data-ttu-id="57c6c-115">Í **Vörukröfur** skjámynd, sláðu inn upplýsingar um vöruna sem krafist er.</span><span class="sxs-lookup"><span data-stu-id="57c6c-115">In the **Item requirements** form, enter information for the required item.</span></span> <span data-ttu-id="57c6c-116">Fyrir frekari upplýsingar um tiltekna reiti, sjá [Vörukröfur (skjámynd)](https://technet.microsoft.com/en-us/library/aa552021\(v=ax.60\)).</span><span class="sxs-lookup"><span data-stu-id="57c6c-116">For more information about the specific fields, see [Item requirements (form)](https://technet.microsoft.com/en-us/library/aa552021\(v=ax.60\)).</span></span>

## <a name="create-an-item-requirement-for-a-service-agreement"></a><span data-ttu-id="57c6c-117">Stofna vöruþörf fyrir þjónustusamning</span><span class="sxs-lookup"><span data-stu-id="57c6c-117">Create an item requirement for a service agreement</span></span>

1.  <span data-ttu-id="57c6c-118">Smellið á **Þjónustustjórnun** \> **Almennt** \> **Þjónustusamningar** \> **þjónustusamningar**.</span><span class="sxs-lookup"><span data-stu-id="57c6c-118">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="57c6c-119">Opnaðu þjónustusamninginn sem stofna á vörukröfu fyrir.</span><span class="sxs-lookup"><span data-stu-id="57c6c-119">Open the service agreement for which you want to create an item requirement.</span></span>

3.  <span data-ttu-id="57c6c-120">Á **Línur** Flýtiflipanum skaltu smella á **Bæta við** til að búa til nýja línu.</span><span class="sxs-lookup"><span data-stu-id="57c6c-120">On the **Lines** FastTab, click **Add** to create a new line.</span></span>

4.  <span data-ttu-id="57c6c-121">Í **Færslugerð** reitnum skaltu velja **Vara**.</span><span class="sxs-lookup"><span data-stu-id="57c6c-121">In the **Transaction type** field, select **Item**.</span></span>

5.  <span data-ttu-id="57c6c-122">Í **Uppsetning vöru** reitnum, veldu **Vörukrafa**.</span><span class="sxs-lookup"><span data-stu-id="57c6c-122">In the **Item setup** field, select **Item requirement**.</span></span>

6.  <span data-ttu-id="57c6c-123">Í **vörunúmer** reitnum, velja vöruna sem þjónustusamningurinn krefst.</span><span class="sxs-lookup"><span data-stu-id="57c6c-123">In the **Item number** field, select the item that is required for the service agreement.</span></span>

7.  <span data-ttu-id="57c6c-124">Á **Upplýsingar um línu** flýtiflipanum á flipanum **Afurðavídd** í reitnum **Svæði** skaltu velja birgðasvæði fyrir vöruna.</span><span class="sxs-lookup"><span data-stu-id="57c6c-124">On the **Line details** FastTab, on the **Product dimensions** tab, in the **Site** field, select the inventory site for the item.</span></span>

8.  <span data-ttu-id="57c6c-125">Til að búa til þjónustupöntun frá samningslínunni skaltu smella á **Línur** Flýtiflipi, **Búa til þjónustupantanir** og sláðu síðan inn viðeigandi upplýsingar í **Búa til þjónustupantanir** skjámynd.</span><span class="sxs-lookup"><span data-stu-id="57c6c-125">To create a service order from the agreement line, on the **Lines** FastTab, click **Create service orders**, and then enter the relevant information in the **Create service orders** form.</span></span> 


## <a name="see-also"></a><span data-ttu-id="57c6c-126">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="57c6c-126">See also</span></span>

<span data-ttu-id="57c6c-127">[Stofna þjónustupantanir sjálfkrafa](create-service-orders-automatically.md).</span><span class="sxs-lookup"><span data-stu-id="57c6c-127">[Create service orders automatically](create-service-orders-automatically.md).</span></span>

  



