---
title: Vörur án birgðastöðu er hægt að skrá út
description: Þetta efnisatriði býður upp á leiðsögn úrræðaleitar sem getur reynst hjálpleg þegar viðskiptavinir geta bætt vörum sem ekki eru til í birgðum við körfuna sína og farið á greiðslusíðuna.
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
ms.openlocfilehash: 6df9c77248c7f4e16765b98327fe5838f0fce7e4
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585373"
---
# <a name="items-without-inventory-can-be-checked-out"></a><span data-ttu-id="df8ad-103">Vörur án birgðastöðu er hægt að skrá út</span><span class="sxs-lookup"><span data-stu-id="df8ad-103">Items without inventory can be checked out</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="df8ad-104">Þetta efnisatriði býður upp á leiðsögn úrræðaleitar sem getur reynst hjálpleg þegar viðskiptavinir geta bætt vörum sem ekki eru til í birgðum við körfuna sína og farið á greiðslusíðuna.</span><span class="sxs-lookup"><span data-stu-id="df8ad-104">This topic provides troubleshooting guidance that can help when customers can add out-of-stock items to their cart and proceed to checkout.</span></span>

## <a name="description"></a><span data-ttu-id="df8ad-105">lýsing</span><span class="sxs-lookup"><span data-stu-id="df8ad-105">Description</span></span>

<span data-ttu-id="df8ad-106">Notendur geta bætt vöru við körfuna sína þótt engar birgðir eru til í versluninni og síðan farið á greiðslusíðuna.</span><span class="sxs-lookup"><span data-stu-id="df8ad-106">Users can add an item to their cart, even though there is no on-hand inventory in the store, and then proceed to the checkout page.</span></span>

## <a name="resolution"></a><span data-ttu-id="df8ad-107">Upplausn</span><span class="sxs-lookup"><span data-stu-id="df8ad-107">Resolution</span></span>

### <a name="enable-the-show-out-of-stock-errors-property-in-commerce-site-builder"></a><span data-ttu-id="df8ad-108">Virkja eiginleikann Sýna villuboðin Ekki til á lager í vefsmið Commerce</span><span class="sxs-lookup"><span data-stu-id="df8ad-108">Enable the Show Out Of Stock Errors property in Commerce site builder</span></span>

<span data-ttu-id="df8ad-109">Til að virkja eiginleikann **Sýna villuboðin Ekki til á lager** í vefsmið Commerce skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="df8ad-109">To enable the **Show Out Of Stock Errors** property in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="df8ad-110">Veljið svæðið sem unnið er á.</span><span class="sxs-lookup"><span data-stu-id="df8ad-110">Select the site that you're working on.</span></span>
1. <span data-ttu-id="df8ad-111">Í vinstri flettingunni skal velja **Síður**.</span><span class="sxs-lookup"><span data-stu-id="df8ad-111">In the left navigation, select **Pages**.</span></span>
1. <span data-ttu-id="df8ad-112">Veljið **CartPage** til að opna hana.</span><span class="sxs-lookup"><span data-stu-id="df8ad-112">Select **CartPage** to open it.</span></span>
1. <span data-ttu-id="df8ad-113">Veljið hólfið **Karfa 1**, veljið **Breyta** og síðan í eiginleikaglugganum skal velja gátreitinn **Sýna villuboðin Ekki til á lager**.</span><span class="sxs-lookup"><span data-stu-id="df8ad-113">Select the **Cart 1** slot, select **Edit**, and then, in the properties pane, select the **Show Out Of Stock Errors** check box.</span></span>
1. <span data-ttu-id="df8ad-114">Vista og birta síðuna.</span><span class="sxs-lookup"><span data-stu-id="df8ad-114">Save and publish the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="df8ad-115">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="df8ad-115">Additional resources</span></span>

[<span data-ttu-id="df8ad-116">Nota birgðastillingar</span><span class="sxs-lookup"><span data-stu-id="df8ad-116">Apply inventory settings</span></span>](../inventory-settings.md)

[<span data-ttu-id="df8ad-117">Reikna tiltækar birgðir fyrir smásölurásir</span><span class="sxs-lookup"><span data-stu-id="df8ad-117">Calculate inventory availability for retail channels</span></span>](../calculated-inventory-retail-channels.md)

[<span data-ttu-id="df8ad-118">Skilgreina birgðabiðminni og birgðastöðu</span><span class="sxs-lookup"><span data-stu-id="df8ad-118">Configure inventory buffers and inventory levels</span></span>](../inventory-buffers-levels.md)
