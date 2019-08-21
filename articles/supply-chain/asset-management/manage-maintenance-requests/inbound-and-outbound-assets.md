---
title: Eignir á innleið og útleið
description: Þetta efni útskýrir hvernig á að eignir á innleið og útleið í eignastýringu.
author: josaw1
manager: AnnBe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 62998da7f541379296d5ac325ae29f24a42f9b7c
ms.sourcegitcommit: 871b76f8808a48d282f151144829323258ffc912
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/02/2019
ms.locfileid: "1847552"
---
# <a name="inbound-and-outbound-assets"></a><span data-ttu-id="f9c17-103">Eignir á innleið og útleið</span><span class="sxs-lookup"><span data-stu-id="f9c17-103">Inbound and outbound assets</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="f9c17-104">Ef fyrirtæki þitt sinnir viðgerðarstörfum eða viðhaldsstörfum á eignum sem eru mótteknar frá öðrum stöðum eða viðskiptavinum, þá getur eignastýring rakið bæði eignir á innleið sem eru á leið til þíns fyrirtækis og eignir á útleið sem er skilað.</span><span class="sxs-lookup"><span data-stu-id="f9c17-104">If your company does repair jobs or maintenance jobs on assets that are received from other locations or customers, Asset Management can track both inbound assets that are on their way to your company and outbound assets that are being returned.</span></span>

> [!NOTE]
> <span data-ttu-id="f9c17-105">Ef þú vilt nota líftímastöður á innleið og útleið til að stjórna eignum sem eru að koma inn og verða skilað, verður þú að setja upp viðhaldsbeiðni um líftímastöður og líftímalíkön til að styðja þessar aðgerðir.</span><span class="sxs-lookup"><span data-stu-id="f9c17-105">If you want to use inbound and outbound lifecycle states to manage assets that are coming in and being returned, you must set up maintenance request lifecycle states and lifecycle models to support these actions.</span></span> <span data-ttu-id="f9c17-106">Nánari upplýsingar er að finna í [Uppsetning á viðhaldsbeiðnum](../setup-for-maintenance-requests/requests.md).</span><span class="sxs-lookup"><span data-stu-id="f9c17-106">For more information, see [Setup for maintenance requests](../setup-for-maintenance-requests/requests.md).</span></span>

<span data-ttu-id="f9c17-107">Uppsetning eignastýringar ákvarðar hvort þú getur unnið eignir á innleið og útleið.</span><span class="sxs-lookup"><span data-stu-id="f9c17-107">The setup of Asset Management determines whether you can work with inbound and outbound assets.</span></span>

## <a name="register-assets-as-inbound"></a><span data-ttu-id="f9c17-108">Skráðu eignir sem á innleið</span><span class="sxs-lookup"><span data-stu-id="f9c17-108">Register assets as inbound</span></span>

1. <span data-ttu-id="f9c17-109">Veldu **Eignastýring** \> **Sameiginlegt** \> **Viðhaldsbeiðnir** \> **Virkar viðhaldsbeiðnir**.</span><span class="sxs-lookup"><span data-stu-id="f9c17-109">Select **Asset management** \> **Common** \> **Maintenance requests** \> **Active maintenance requests**.</span></span>
2. <span data-ttu-id="f9c17-110">Veljið viðhaldsbeiðnina.</span><span class="sxs-lookup"><span data-stu-id="f9c17-110">Select the maintenance request.</span></span>
3. <span data-ttu-id="f9c17-111">Veldu **Uppfæra stöðu viðhaldsbeiðni**.</span><span class="sxs-lookup"><span data-stu-id="f9c17-111">Select **Update maintenance request state**.</span></span>
4. <span data-ttu-id="f9c17-112">Veldu **Á innleið** (eða aðra líftímastöðu sem þú hefur búið til fyrir eignir á innleið) og veldu síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="f9c17-112">Select **Inbound** (or another lifecycle state that you've created for inbound assets), and then select **OK**.</span></span>

![Mynd 1](media/07-manage-maintenance-requests.png)

## <a name="register-inbound-assets-as-received"></a><span data-ttu-id="f9c17-114">Skrá eignir á innleið sem mótteknar</span><span class="sxs-lookup"><span data-stu-id="f9c17-114">Register inbound assets as received</span></span>

1. <span data-ttu-id="f9c17-115">Veldu **Eignastýring** \> **Sameiginlegt** \> **Innleið/útleið** \> **Eignir á innleið**.</span><span class="sxs-lookup"><span data-stu-id="f9c17-115">Select **Asset management** \> **Common** \> **Inbound/outbound** \> **Inbound assets**.</span></span>
2. <span data-ttu-id="f9c17-116">Veljið eignina eða viðhaldsbeiðnina.</span><span class="sxs-lookup"><span data-stu-id="f9c17-116">Select the asset or maintenance request.</span></span>
3. <span data-ttu-id="f9c17-117">Veldu **Taka á móti eignum**.</span><span class="sxs-lookup"><span data-stu-id="f9c17-117">Select **Receive assets**.</span></span>
4. <span data-ttu-id="f9c17-118">Í reitnum **Móttekið** skaltu slá inn dagsetningu og tíma.</span><span class="sxs-lookup"><span data-stu-id="f9c17-118">In the **Received** field, enter the date and time.</span></span> <span data-ttu-id="f9c17-119">Veljið síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="f9c17-119">Then select **OK**.</span></span> <span data-ttu-id="f9c17-120">Gögnin eru tekin af listasíðunni **Eignir á innleið**.</span><span class="sxs-lookup"><span data-stu-id="f9c17-120">The record is removed from the **Inbound assets** list page.</span></span>

![Mynd 2](media/08-manage-maintenance-requests.png)

## <a name="register-assets-as-outbound"></a><span data-ttu-id="f9c17-122">Skráðu eignir sem á útleið</span><span class="sxs-lookup"><span data-stu-id="f9c17-122">Register assets as outbound</span></span>

<span data-ttu-id="f9c17-123">Þegar þú hefur lokið viðhalds- eða viðgerðarstörfum geturðu skráð eignina sem skilað.</span><span class="sxs-lookup"><span data-stu-id="f9c17-123">When you've completed the maintenance or repair job, you can register the asset as returned.</span></span>

1. <span data-ttu-id="f9c17-124">Veldu **Eignastýring** \> **Sameiginlegt** \> **Viðhaldsbeiðnir** \> **Virkar viðhaldsbeiðnir**.</span><span class="sxs-lookup"><span data-stu-id="f9c17-124">Select **Asset management** \> **Common** \> **Maintenance requests** \> **Active maintenance requests**.</span></span>
2. <span data-ttu-id="f9c17-125">Veljið viðhaldsbeiðnina.</span><span class="sxs-lookup"><span data-stu-id="f9c17-125">Select the maintenance request.</span></span>
3. <span data-ttu-id="f9c17-126">Veldu **Uppfæra stöðu viðhaldsbeiðni**.</span><span class="sxs-lookup"><span data-stu-id="f9c17-126">Select **Update maintenance request state**.</span></span>
4. <span data-ttu-id="f9c17-127">Veldu **Á útleið** (eða aðra líftímastöðu sem þú hefur búið til fyrir eignir á útleið) og veldu síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="f9c17-127">Select **Outbound** (or another lifecycle state that you've created for outbound assets), and then select **OK**.</span></span>

## <a name="register-outbound-assets-as-delivered"></a><span data-ttu-id="f9c17-128">Skráðu eignir á útleið sem afhentar</span><span class="sxs-lookup"><span data-stu-id="f9c17-128">Register outbound assets as delivered</span></span>

1. <span data-ttu-id="f9c17-129">Veldu **Eignastýring** \> **Sameiginlegt** \> **Innleið/útleið** \> **Eignir á útleið**.</span><span class="sxs-lookup"><span data-stu-id="f9c17-129">Select **Asset management** \> **Common** \> **Inbound/outbound** \> **Outbound assets**.</span></span>
2. <span data-ttu-id="f9c17-130">Veljið eignina eða viðhaldsbeiðnina.</span><span class="sxs-lookup"><span data-stu-id="f9c17-130">Select the asset or maintenance request.</span></span>
3. <span data-ttu-id="f9c17-131">Veldu **Skila eignum**.</span><span class="sxs-lookup"><span data-stu-id="f9c17-131">Select **Deliver assets**.</span></span>
4. <span data-ttu-id="f9c17-132">Í reitnum **Afhent** skaltu slá inn dagsetningu og tíma.</span><span class="sxs-lookup"><span data-stu-id="f9c17-132">In the **Delivered** field, enter the date and time.</span></span> <span data-ttu-id="f9c17-133">Veljið síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="f9c17-133">Then select **OK**.</span></span> <span data-ttu-id="f9c17-134">Gögnin eru tekin af listasíðunni **Eignir á útleið**.</span><span class="sxs-lookup"><span data-stu-id="f9c17-134">The record is removed from the **Outbound assets** list page.</span></span>
