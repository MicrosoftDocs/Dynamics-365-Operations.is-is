---
title: Ábyrgðir á eignum og eignagerðum
description: Þetta efni útskýrir hvernig á að setja upp ábyrgðir á eignum og eignagerðum í eignastjórnun.
author: josaw1
manager: tfehr
ms.date: 08/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 78ac93b1e681fca7d7eefd921f282a8496aa9d0a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5245324"
---
# <a name="warranties-on-assets-and-asset-types"></a><span data-ttu-id="dc55a-103">Ábyrgðir á eignum og eignagerðum</span><span class="sxs-lookup"><span data-stu-id="dc55a-103">Warranties on assets and asset types</span></span>

[!include [banner](../../includes/banner.md)]

 


<span data-ttu-id="dc55a-104">Þetta efni útskýrir hvernig á að setja upp ábyrgðir á eignum og eignagerðum í eignastjórnun.</span><span class="sxs-lookup"><span data-stu-id="dc55a-104">This topic explains how to set up warranties on assets and asset types in Asset Management.</span></span>

## <a name="set-up-a-warranty-on-an-asset-type"></a><span data-ttu-id="dc55a-105">Settu upp ábyrgð á eignagerð</span><span class="sxs-lookup"><span data-stu-id="dc55a-105">Set up a warranty on an asset type</span></span>

1. <span data-ttu-id="dc55a-106">Veldu **Eignastýring** \> **Uppsetning** \> **Eignagerðir** \> **Eignagerðir**.</span><span class="sxs-lookup"><span data-stu-id="dc55a-106">Select **Asset management** \> **Setup** \> **Asset types** \> **Asset types**.</span></span>
2. <span data-ttu-id="dc55a-107">Í vinstri glugganum velurðu eignategundina sem á að festa ábyrgðarsamning lánardrottins við og velur síðan **Sjálfgefin tegund eigna**.</span><span class="sxs-lookup"><span data-stu-id="dc55a-107">In the left pane, select the asset type to attach a vendor warranty agreement to, and then select **Asset type defaults**.</span></span>
3. <span data-ttu-id="dc55a-108">Á flýtiflipanum **Almennt**, í reitnum **Ábyrgð lánardrottins** velurðu samninginn.</span><span class="sxs-lookup"><span data-stu-id="dc55a-108">On the **General** FastTab, in the **Vendor warranty** field, select the agreement.</span></span>

## <a name="set-up-a-warranty-on-an-asset"></a><span data-ttu-id="dc55a-109">Settu upp ábyrgð á eign</span><span class="sxs-lookup"><span data-stu-id="dc55a-109">Set up a warranty on an asset</span></span>

1. <span data-ttu-id="dc55a-110">Veldu **Eignastýring** \> **Sameiginlegt** \> **Eignir** \> **Allar eignir**.</span><span class="sxs-lookup"><span data-stu-id="dc55a-110">Select **Asset management** \> **Common** \> **Assets** \> **All assets**.</span></span>
2. <span data-ttu-id="dc55a-111">Veldu eignina og veldu síðan **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="dc55a-111">Select the asset, and then select **Edit**.</span></span>
3. <span data-ttu-id="dc55a-112">Á flýtflipanum **Lánardrottinn** í hlutanum **Ábyrgð lánardrottins** í reitnum **Ábyrgð** velurðu ábyrgðarsamninginn.</span><span class="sxs-lookup"><span data-stu-id="dc55a-112">On the **Vendor** FastTab, in the **Vendor warranty** section, in the **Warranty** field, select the warranty agreement.</span></span>
4. <span data-ttu-id="dc55a-113">Í reitunum **Upphafð ábyrgðar** og **Lok ábyrgðar** velurðu upphafs- og lokadagsetningar.</span><span class="sxs-lookup"><span data-stu-id="dc55a-113">In the **Warranty start** and **Warranty end** fields, select the start and end dates.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="dc55a-114">Ef dagsetning er valin í reitnum **Upphaf ábyrgðar** í verkbeiðni gildir ábyrgðin fyrir verkbeiðnina á þeim degi.</span><span class="sxs-lookup"><span data-stu-id="dc55a-114">If a date is selected in the **Warranty start** field on a work order, the warranty becomes valid for the work order on that date.</span></span> <span data-ttu-id="dc55a-115">Þegar þú býrð til verkbeiðni er reiturinn **Upphaf ábyrgðar** sjálfvirkt stilltur á dagsetningu stofnunar.</span><span class="sxs-lookup"><span data-stu-id="dc55a-115">When you create a work order, the **Warranty start** field is automatically set to the date of creation.</span></span> <span data-ttu-id="dc55a-116">Hins vegar er hægt að breyta dagsetningunni þannig að hún samsvari til dæmis upphafsdagsetningu ábyrgðarsamnings.</span><span class="sxs-lookup"><span data-stu-id="dc55a-116">However, you can change the date so that it corresponds to, for example, the start date of a warranty agreement.</span></span>
    >
    > ![Verkbeiðnasíða](media/02-warranty.png)

> [!NOTE]
> <span data-ttu-id="dc55a-118">Þegar þú býrð til verkbeiðni fyrir eign sem fellur undir ábyrgð lánardrottins, ef verkbeiðnin er með áætlaðan upphafsdag á ábyrgðartímabilinu, færðu tilkynningu um ábyrgðarsamninginn.</span><span class="sxs-lookup"><span data-stu-id="dc55a-118">When you create a work order for an asset that is covered by a vendor warranty, if the work order has an expected start date during the warranty period, you receive a notification about the warranty agreement.</span></span> <span data-ttu-id="dc55a-119">Þú getur síðan sagt upp verkbeiðninni eins og þú þarft.</span><span class="sxs-lookup"><span data-stu-id="dc55a-119">You can then cancel the work order, as you require.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]