---
title: Tegundir viðhaldseiginda
description: Þetta efni útskýrir hvernig á að stofna eigindagerðir í eignastýringu.
author: josaw1
manager: tfehr
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetFunctionalLocationTypeCopy, EntAssetAttributeType, EntAssetAttributeTypeValue, EntAssetFunctionalLocationType
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b93c2ab284d5746f4ecd48cd8b8ffe59aea9f90
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5217246"
---
# <a name="maintenance-attribute-types"></a><span data-ttu-id="802fc-103">Tegundir viðhaldseiginda</span><span class="sxs-lookup"><span data-stu-id="802fc-103">Maintenance attribute types</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="802fc-104">Þetta efni útskýrir hvernig á að stofna eigindagerðir í eignastýringu.</span><span class="sxs-lookup"><span data-stu-id="802fc-104">This topic explains how to create attribute types in Asset Management.</span></span> <span data-ttu-id="802fc-105">Eiginleikar eru notaðir til að lýsa eiginleikum ýmissa þátta.</span><span class="sxs-lookup"><span data-stu-id="802fc-105">Attributes are used to describe the properties of various elements.</span></span> <span data-ttu-id="802fc-106">Hægt er að setja upp eigindi á eftirfarandi færibreytur:</span><span class="sxs-lookup"><span data-stu-id="802fc-106">You can set up attributes on the following elements:</span></span>

- [<span data-ttu-id="802fc-107">Gerðir virkra staðsetninga</span><span class="sxs-lookup"><span data-stu-id="802fc-107">Functional location types</span></span>](../setup-for-functional-locations/functional-location-types.md)
- [<span data-ttu-id="802fc-108">Stofna virkar staðsetningar</span><span class="sxs-lookup"><span data-stu-id="802fc-108">Create functional locations</span></span>](../functional-locations/create-functional-locations.md)
- [<span data-ttu-id="802fc-109">Eignagerðir</span><span class="sxs-lookup"><span data-stu-id="802fc-109">Asset types</span></span>](../setup-for-objects/object-types.md)
- <span data-ttu-id="802fc-110">Eignir</span><span class="sxs-lookup"><span data-stu-id="802fc-110">Assets</span></span>

<span data-ttu-id="802fc-111">Eiginleikarnir sem þú getur sett upp eru mismunandi eftir því hvaða þáttur er.</span><span class="sxs-lookup"><span data-stu-id="802fc-111">The attributes that you can set up vary, depending on the element.</span></span> <span data-ttu-id="802fc-112">Til dæmis, fyrir hagnýta staðsetningu, getur þú sett upp eiginleika fyrir stillingar og líkamlega stærð staðsetningarinnar.</span><span class="sxs-lookup"><span data-stu-id="802fc-112">For example, for a functional location, you can set up attributes for the configuration and physical size of the location.</span></span> <span data-ttu-id="802fc-113">Fyrir eignategund eða eign geturðu sett upp eiginleika fyrir magn vélarinnar, orkunotkun og hámarks burðargetu við mismunandi aðstæður.</span><span class="sxs-lookup"><span data-stu-id="802fc-113">For an asset type or an asset, you can set up attributes for engine volume, power consumption, and maximum load capacity under different conditions.</span></span>

## <a name="create-attribute-types"></a><span data-ttu-id="802fc-114">Búa til eigindargerðir</span><span class="sxs-lookup"><span data-stu-id="802fc-114">Create attribute types</span></span>

<span data-ttu-id="802fc-115">Þú getur búið til þínar eigin tegundir.</span><span class="sxs-lookup"><span data-stu-id="802fc-115">You can create your own attribute types.</span></span> <span data-ttu-id="802fc-116">Að auki geturðu flutt vöruvíddir á síðuna **Eigindagerðir**.</span><span class="sxs-lookup"><span data-stu-id="802fc-116">Additionally, you can transfer product dimensions to the **Attribute types** page.</span></span>

1. <span data-ttu-id="802fc-117">Veldu **Eignastýring** \> **Uppsetning** \> **Eigindagerðir**.</span><span class="sxs-lookup"><span data-stu-id="802fc-117">Select **Asset management** \> **Setup** \> **Attribute types**.</span></span>
2. <span data-ttu-id="802fc-118">Veldu í fyrsta skipti sem þú setur upp eigindategundir **Stofna vöruvíddir** til að flytja sjálfkrafa staðlaðar víddir.</span><span class="sxs-lookup"><span data-stu-id="802fc-118">The first time that you set up attribute types, select **Create product dimensions** to automatically transfer standard product dimensions.</span></span>
3. <span data-ttu-id="802fc-119">Veldu **Nýr** til að stofna nýja eigindagerð.</span><span class="sxs-lookup"><span data-stu-id="802fc-119">Select **New** to create a new attribute type.</span></span>
4. <span data-ttu-id="802fc-120">Í svæðinu **Eigindagerð** er fært inn nafn fyrir eigindagerðina.</span><span class="sxs-lookup"><span data-stu-id="802fc-120">In the **Attribute type** field, enter a name for the attribute type.</span></span>
5. <span data-ttu-id="802fc-121">Í reitnum **Lýsing** skal færa inn lýsingu.</span><span class="sxs-lookup"><span data-stu-id="802fc-121">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="802fc-122">Í reitinn **Eining** reitinn, veldu viðeigandi eigindareining, eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="802fc-122">In the **Unit** field, select the relevant attribute unit, as required.</span></span>
7. <span data-ttu-id="802fc-123">Í reitnum **Gagnagerð** skal velja gagnagerð fyrir eininguna.</span><span class="sxs-lookup"><span data-stu-id="802fc-123">In the **Data type** field, select a data type for the unit.</span></span>
8. <span data-ttu-id="802fc-124">Ef þú valdir **Strengur** sem gagnagerð, fylgdu þessum skrefum til að búa til gildi fyrir eigindategundina:</span><span class="sxs-lookup"><span data-stu-id="802fc-124">If you selected **String** as the data type, follow these steps to create values for the attribute type:</span></span>

    1. <span data-ttu-id="802fc-125">Veldu eigindagerðina og veldu síðan **Gildi**.</span><span class="sxs-lookup"><span data-stu-id="802fc-125">Select the attribute type, and then select **Values**.</span></span>
    2. <span data-ttu-id="802fc-126">Í **Eigindagildi** reit, veldu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="802fc-126">In the **Attribute values** field, select **New**.</span></span>
    3. <span data-ttu-id="802fc-127">Í reitnum **Eigindategund** velurðu tegund eiginda (vídd).</span><span class="sxs-lookup"><span data-stu-id="802fc-127">In the **Attribute type** field, select an attribute type (dimension).</span></span>
    4. <span data-ttu-id="802fc-128">Sláið inn eða veldu gildi í **Gildi** reitnum.</span><span class="sxs-lookup"><span data-stu-id="802fc-128">In the **Value** field, enter a related value.</span></span>
    5. <span data-ttu-id="802fc-129">Í reitnum **Lýsing** skal færa inn lýsingu.</span><span class="sxs-lookup"><span data-stu-id="802fc-129">In the **Description** field, enter a description.</span></span>
    6. <span data-ttu-id="802fc-130">Vistaðu færsluna.</span><span class="sxs-lookup"><span data-stu-id="802fc-130">Save the record.</span></span>
    7. <span data-ttu-id="802fc-131">Fara aftur í **Eigindagerðir** síðu.</span><span class="sxs-lookup"><span data-stu-id="802fc-131">Return to the **Attribute types** page.</span></span>

9. <span data-ttu-id="802fc-132">Vistaðu færsluna.</span><span class="sxs-lookup"><span data-stu-id="802fc-132">Save the record.</span></span>

    <span data-ttu-id="802fc-133">Reiturinn **Gerðir virkra staðsetninga** sýnir fjölda virkra staðsetninga sem eru að nota eigindagerðina.</span><span class="sxs-lookup"><span data-stu-id="802fc-133">The **Functional location types** field shows the number of functional locations that are using the attribute type.</span></span> <span data-ttu-id="802fc-134">Reiturinn **Gerðir eigna** sýnir fjölda eignagerða sem eru að nota hann.</span><span class="sxs-lookup"><span data-stu-id="802fc-134">The **Asset types** field shows the number of asset types that are using it.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]