---
title: Stofna og viðhalda á birgðalæsing
description: Í þessu efnisatriði er lýst hvernig birgðalæsing er notuð til að koma í veg fyrir að efnislegar lagerbirgðir verði teknar frá af öðrum upprunaskjölum á útleið.
author: perlynne
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventBlocking, InventItemIdLookupSimple, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e9aa38ca52da577fff258bb330922ad7f4044330
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956159"
---
# <a name="create-and-maintain-an-inventory-blocking"></a><span data-ttu-id="b3caf-103">Stofna og viðhalda á birgðalæsing</span><span class="sxs-lookup"><span data-stu-id="b3caf-103">Create and maintain an inventory blocking</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b3caf-104">Í þessu efnisatriði er lýst hvernig birgðalæsing er notuð til að koma í veg fyrir að efnislegar lagerbirgðir verði teknar frá af öðrum upprunaskjölum á útleið.</span><span class="sxs-lookup"><span data-stu-id="b3caf-104">This topic describes how to use an inventory blocking to prevent physical on-hand inventory from being reserved by other outbound source documents.</span></span> <span data-ttu-id="b3caf-105">Áður en hafist er handa við ferlin í þessu efnisatriði verður þú að vera með vöru þar sem efnislegar lagerbirgðir eru í boði.</span><span class="sxs-lookup"><span data-stu-id="b3caf-105">Before you start the procedures in this topic, you must have an item that physical on-hand inventory is available for.</span></span>

## <a name="block-inventory"></a><span data-ttu-id="b3caf-106">Birgðum læst</span><span class="sxs-lookup"><span data-stu-id="b3caf-106">Block inventory</span></span>

<span data-ttu-id="b3caf-107">Fylgið eftirfarandi skrefum til að stofna birgðalokunarskrá svo birgðir séu lokaðar.</span><span class="sxs-lookup"><span data-stu-id="b3caf-107">To create an inventory blocking record so that inventory is blocked, follow these steps.</span></span>

1. <span data-ttu-id="b3caf-108">Farið í **Birgðastjórnun \> Reglubundin verk \> Birgðalæsing**.</span><span class="sxs-lookup"><span data-stu-id="b3caf-108">Go to **Inventory management \> Periodic tasks \> Inventory blocking**.</span></span>
1. <span data-ttu-id="b3caf-109">Í aðgerðarúðunni velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="b3caf-109">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="b3caf-110">Í haus nýju lokunarfærslunnar á að setja **Vörunúmer** reitinn á vöruna sem á að loka á og slá inn lýsingu.</span><span class="sxs-lookup"><span data-stu-id="b3caf-110">On the header of the new blocking record, set the **Item number** field to the item that you want to block, and enter a description.</span></span>
1. <span data-ttu-id="b3caf-111">Í flýtiflipanum **Almennt**, í reitnum **Magn**, skal færa inn vörufjöldann sem á að læsa.</span><span class="sxs-lookup"><span data-stu-id="b3caf-111">On the **General** FastTab, in the **Quantity** field, enter the number of items to block.</span></span>
1. <span data-ttu-id="b3caf-112">Í flýtiflipanum **Birgðavíddir** skal tilgreina svæðið og vöruhúsið þar sem vörurnar sem á að læsa eru staðsettar.</span><span class="sxs-lookup"><span data-stu-id="b3caf-112">On the **Inventory dimensions** FastTab, specify the site and warehouse where the items that you want to block are currently located.</span></span>
1. <span data-ttu-id="b3caf-113">Í aðgerðarúðunni skal velja **Vista**.</span><span class="sxs-lookup"><span data-stu-id="b3caf-113">On the Action Pane, select **Save**.</span></span>

## <a name="update-the-conditions-of-the-inventory-blocking"></a><span data-ttu-id="b3caf-114">Uppfæra skilyrðum fyrir birgðalæsing</span><span class="sxs-lookup"><span data-stu-id="b3caf-114">Update the conditions of the inventory blocking</span></span>

<span data-ttu-id="b3caf-115">Fylgið eftirfarandi skrefum til að uppfæra birgðalokunarfærslu.</span><span class="sxs-lookup"><span data-stu-id="b3caf-115">To update an inventory blocking record, follow these steps.</span></span>

1. <span data-ttu-id="b3caf-116">Farið í **Birgðastjórnun \> Reglubundin verk \> Birgðalæsing**.</span><span class="sxs-lookup"><span data-stu-id="b3caf-116">Go to **Inventory management \> Periodic tasks \> Inventory blocking**.</span></span>
1. <span data-ttu-id="b3caf-117">Á listasvæðinu skal velja lokunarfærsluna sem á við.</span><span class="sxs-lookup"><span data-stu-id="b3caf-117">In the list pane, select the relevant blocking record.</span></span>
1. <span data-ttu-id="b3caf-118">Breyta færslunni eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="b3caf-118">Edit the record as required.</span></span> <span data-ttu-id="b3caf-119">Til dæmis væri hægt að breyta gildinu í reitnum **Væntanleg dagsetning** til að tilgreina hvenær læstar birgðir verða væntanlega aðgengilegar fyrir frátekningu.</span><span class="sxs-lookup"><span data-stu-id="b3caf-119">For example, you might change the value of the **Expected date** field to indicate when the blocked inventory is expected to become available for reservation.</span></span> <span data-ttu-id="b3caf-120">Ef valkosturinn **Áætluð innhreyfing** er valinn mun dagsetningin birtast á væntanlegri færslu.</span><span class="sxs-lookup"><span data-stu-id="b3caf-120">If the **Expected receipts** option is selected, the date will appear on the expected transaction.</span></span> <span data-ttu-id="b3caf-121">(Valkosturinn **Væntanlegar innhreyfingar** er sjálfgefið valinn þegar lokunarfærsla er stofnuð handvirkt.)</span><span class="sxs-lookup"><span data-stu-id="b3caf-121">(The **Expected receipts** option is selected by default when you manually create a blocking record.)</span></span>
1. <span data-ttu-id="b3caf-122">Í aðgerðarúðunni skal velja **Vista**.</span><span class="sxs-lookup"><span data-stu-id="b3caf-122">On the Action Pane, select **Save**.</span></span>

## <a name="unblock-inventory"></a><span data-ttu-id="b3caf-123">Birgðir opnaðar</span><span class="sxs-lookup"><span data-stu-id="b3caf-123">Unblock inventory</span></span>

<span data-ttu-id="b3caf-124">Fylgja skal eftirfarandi skrefum til að fjarlægja birgðalokunarfærslu þannig að birgðir séu opnaðar.</span><span class="sxs-lookup"><span data-stu-id="b3caf-124">To remove an inventory blocking record so that inventory is unblocked, follow these steps.</span></span>

1. <span data-ttu-id="b3caf-125">Farið í **Birgðastjórnun \> Reglubundin verk \> Birgðalæsing**.</span><span class="sxs-lookup"><span data-stu-id="b3caf-125">Go to **Inventory management \> Periodic tasks \> Inventory blocking**.</span></span>
1. <span data-ttu-id="b3caf-126">Á listasvæðinu skal velja lokunarfærsluna sem á við.</span><span class="sxs-lookup"><span data-stu-id="b3caf-126">In the list pane, select the relevant blocking record.</span></span>
1. <span data-ttu-id="b3caf-127">Á aðgerðasvæðinu skal velja **Eyða**.</span><span class="sxs-lookup"><span data-stu-id="b3caf-127">On the Action Pane, select **Delete**.</span></span>
1. <span data-ttu-id="b3caf-128">Þú færð kvaðningu um að staðfesta aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="b3caf-128">You're prompted to confirm the operation.</span></span> <span data-ttu-id="b3caf-129">Veldu **Já** til að halda áfram.</span><span class="sxs-lookup"><span data-stu-id="b3caf-129">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="b3caf-130">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b3caf-130">Close the page.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
