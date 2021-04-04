---
title: Smásöluverslun birtist ekki í listanum yfir verslanir til að sækja úr
description: Þetta efnisatriði býður upp á leiðsögn úrræðaleitar sem getur reynst hjálpleg þegar smásöluverslun birtist ekki í listanum yfir verslanir þar sem hægt er að sækja vörur.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 652f5f1a779a412c21c18814071ba0fb7dd2e155
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585382"
---
# <a name="retail-store-doesnt-appear-in-the-list-of-stores-to-pick-up-from"></a><span data-ttu-id="b3bad-103">Smásöluverslun birtist ekki í listanum yfir verslanir til að sækja úr</span><span class="sxs-lookup"><span data-stu-id="b3bad-103">Retail store doesn't appear in the list of stores to pick up from</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b3bad-104">Þetta efnisatriði býður upp á leiðsögn úrræðaleitar sem getur reynst hjálpleg þegar smásöluverslun birtist ekki í listanum yfir verslanir þar sem hægt er að sækja vörur.</span><span class="sxs-lookup"><span data-stu-id="b3bad-104">This topic provides troubleshooting guidance that can help when a retail store doesn't appear in the list of stores where items can be picked up.</span></span>

## <a name="description"></a><span data-ttu-id="b3bad-105">lýsing</span><span class="sxs-lookup"><span data-stu-id="b3bad-105">Description</span></span>

<span data-ttu-id="b3bad-106">Smásöluverslun birtist ekki í listanum yfir verslanir þar sem hægt er að sækja vörur.</span><span class="sxs-lookup"><span data-stu-id="b3bad-106">A retail store doesn't appear in the list of stores where items can be picked up.</span></span>

## <a name="resolution"></a><span data-ttu-id="b3bad-107">Upplausn</span><span class="sxs-lookup"><span data-stu-id="b3bad-107">Resolution</span></span>

### <a name="configure-the-longitude-and-latitude-for-the-store-address-in-commerce-headquarters"></a><span data-ttu-id="b3bad-108">Skilgreina lengdar- og breiddargráðu fyrir aðsetur verslunar í Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="b3bad-108">Configure the longitude and latitude for the store address in Commerce headquarters</span></span>

<span data-ttu-id="b3bad-109">Til að skilgreina lengdar- og breiddargráðu fyrir aðsetur verslunar í Commerce Headquarters skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="b3bad-109">To configure the longitude and latitude for the store address in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="b3bad-110">Farið í **Smásala og viðskipti \> Rásir \> Verslanir \> Allar verslanir**.</span><span class="sxs-lookup"><span data-stu-id="b3bad-110">Go to **Retail and Commerce \> Channels \> Stores \> All stores**.</span></span>
1. <span data-ttu-id="b3bad-111">Finnið verslunina sem á að birtast í valkostum fyrir sótt á svæði rafrænna viðskipta.</span><span class="sxs-lookup"><span data-stu-id="b3bad-111">Find the store that you want to appear among the pickup options on the e-commerce site.</span></span> <span data-ttu-id="b3bad-112">Skráið hjá ykkur gildið fyrir **Númer rekstrareiningar**.</span><span class="sxs-lookup"><span data-stu-id="b3bad-112">Make a note of its **Operating unit number** value.</span></span>
1. <span data-ttu-id="b3bad-113">Farið í **Fyrirtækisstjórnun \> Fyrirtæki \> Rekstrareiningar**.</span><span class="sxs-lookup"><span data-stu-id="b3bad-113">Go to **Organization administration \> Organizations \> Operating units**.</span></span>
1. <span data-ttu-id="b3bad-114">Leitið að númeri rekstrareiningarinnar sem var skráð niður hér á undan og veljið síðan rekstrareininguna í leitarniðurstöðunum.</span><span class="sxs-lookup"><span data-stu-id="b3bad-114">Search for the operating unit number that you noted earlier, and then select the operating unit in the search results.</span></span>
1. <span data-ttu-id="b3bad-115">Í flýtiflipanum **Aðsetur** skal velja **Fleiri valkostir** og síðan velja **Ítarlegt**.</span><span class="sxs-lookup"><span data-stu-id="b3bad-115">On the **Addresses** FastTab, select **More options**, and then select **Advanced**.</span></span>
1. <span data-ttu-id="b3bad-116">Í flýtiflipanum **Almennt** skal ganga úr skugga um reitirnir **Lengdargráða** og **Breiddargráða** séu rétt stilltir.</span><span class="sxs-lookup"><span data-stu-id="b3bad-116">On the **General** FastTab, make sure that the **Longitude** and **Latitude** fields are correctly set.</span></span> <span data-ttu-id="b3bad-117">Sem hluti af þessu skrefi skal ganga úr skugga um að gildin séu rétt tilgreind sem jákvæðar og neikvæðar tölur.</span><span class="sxs-lookup"><span data-stu-id="b3bad-117">As part of this step, make sure that the values are correctly specified as positive or negative numbers.</span></span>

### <a name="configure-fulfillment-groups-in-commerce-headquarters"></a><span data-ttu-id="b3bad-118">Skilgreina uppfyllingarflokka í Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="b3bad-118">Configure fulfillment groups in Commerce headquarters</span></span>

<span data-ttu-id="b3bad-119">Til að skilgreina uppfyllingarflokka í Commerce Headquarters skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="b3bad-119">To configure fulfillment groups in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="b3bad-120">Farið í **Smásala og viðskipti \> Rásir \> Netverslanir**.</span><span class="sxs-lookup"><span data-stu-id="b3bad-120">Go to **Retail and Commerce \> Channels \> Online stores**.</span></span>
1. <span data-ttu-id="b3bad-121">Veljið netverslunina sem á að skilgreina.</span><span class="sxs-lookup"><span data-stu-id="b3bad-121">Select the online store to configure.</span></span>
1. <span data-ttu-id="b3bad-122">Í aðgerðaglugganum skal velja **Setja upp** og því næst velja **Úthlutun uppfyllingarflokks**.</span><span class="sxs-lookup"><span data-stu-id="b3bad-122">On the Action Pane, select **Set up**, and then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="b3bad-123">Á síðunni **Úthlutun uppfyllingarflokks** skal velja uppfyllingarflokkinn fyrir netverslunina.</span><span class="sxs-lookup"><span data-stu-id="b3bad-123">On the **Fulfillment group assignment** page, select the fulfillment group for the online store.</span></span>
1. <span data-ttu-id="b3bad-124">Undir **Uppsetning** skal ganga úr skugga um smásöluverslunin sé rétt skilgreind fyrir uppfyllingarflokkinn.</span><span class="sxs-lookup"><span data-stu-id="b3bad-124">Under **Setup**, make sure that the retail store is correctly configured for the fulfillment group.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b3bad-125">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="b3bad-125">Additional resources</span></span> 

[<span data-ttu-id="b3bad-126">Stofna rekstrareiningu</span><span class="sxs-lookup"><span data-stu-id="b3bad-126">Create an operating unit</span></span>](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit)

[<span data-ttu-id="b3bad-127">Setja upp netrás</span><span class="sxs-lookup"><span data-stu-id="b3bad-127">Set up an online channel</span></span>](../channel-setup-online.md)
