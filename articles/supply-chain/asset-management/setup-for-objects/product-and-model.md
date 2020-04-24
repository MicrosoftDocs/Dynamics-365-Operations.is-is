---
title: Eignaframleiðendur og líkön
description: Þetta efni útskýrir hvernig á að setja upp eignaframleiðendur og skyld líkön í eignastjórnun.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f2ef8a9afc007ce7e453f5e9cadfb912490545c0
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205116"
---
# <a name="asset-manufacturers-and-models"></a><span data-ttu-id="5d05d-103">Eignaframleiðendur og líkön</span><span class="sxs-lookup"><span data-stu-id="5d05d-103">Asset manufacturers and models</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="5d05d-104">Þetta efni útskýrir hvernig á að setja upp eignaframleiðendur og skyld líkön í eignastjórnun.</span><span class="sxs-lookup"><span data-stu-id="5d05d-104">This topic explains how to set up asset manufacturers and related models in Asset Management.</span></span> <span data-ttu-id="5d05d-105">Líkön geta verið tengd eignategundum.</span><span class="sxs-lookup"><span data-stu-id="5d05d-105">Models can be related to asset types.</span></span>

## <a name="set-up-product-model-relations"></a><span data-ttu-id="5d05d-106">Setja upp afurða-líkanavensl</span><span class="sxs-lookup"><span data-stu-id="5d05d-106">Set up product-model relations</span></span>

1. <span data-ttu-id="5d05d-107">Veldu **Eignastýring** \> **Uppsetning** \> **Eignir** \> **Framleiðandi og líkan**.</span><span class="sxs-lookup"><span data-stu-id="5d05d-107">Select **Asset management** \> **Setup** \> **Assets** \> **Manufacturer and model**.</span></span>
2. <span data-ttu-id="5d05d-108">Veldu **Nýr** til að stofna nýja afurð.</span><span class="sxs-lookup"><span data-stu-id="5d05d-108">Select **New** to create a new product.</span></span>
3. <span data-ttu-id="5d05d-109">Í **Framleiðandi** reitinn, sláðu inn nafn fyrir eignaframleiðandann.</span><span class="sxs-lookup"><span data-stu-id="5d05d-109">In the **Manufacturer** field, enter a name for the asset manufacturer.</span></span>
4. <span data-ttu-id="5d05d-110">Í reitnum **Lýsing** skal færa inn lýsingu.</span><span class="sxs-lookup"><span data-stu-id="5d05d-110">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="5d05d-111">Á flýtiflipanum **Líkön**, veldu **Bæta við** til að búa til eignalíkan sem ætti að tengjast eignaframleiðandanum.</span><span class="sxs-lookup"><span data-stu-id="5d05d-111">On the **Models** FastTab, select **Add** to create an asset model that should be related to the asset manufacturer.</span></span>
6. <span data-ttu-id="5d05d-112">Í **Líkan** reitinn, sláðu inn nafn fyrir eignalíkanið.</span><span class="sxs-lookup"><span data-stu-id="5d05d-112">In the **Model** field, enter a name for the asset model.</span></span>
7. <span data-ttu-id="5d05d-113">Í reitnum **Lýsing** skal færa inn lýsingu.</span><span class="sxs-lookup"><span data-stu-id="5d05d-113">In the **Description** field, enter a description.</span></span>
8. <span data-ttu-id="5d05d-114">Í **Tegund eigna** reit, veldu þá eignategund sem framleiðandamódelið ætti að tengjast.</span><span class="sxs-lookup"><span data-stu-id="5d05d-114">In the **Asset type** field, select the asset type that the manufacturer model should be related to.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5d05d-115">Þú getur einnig sett upp sambönd fyrir eignategundir, framleiðendur og gerðir í uppflettingunni **Gerðir eigna**.</span><span class="sxs-lookup"><span data-stu-id="5d05d-115">You can also set up relations for asset types, manufacturers, and models in the **Asset types** lookup.</span></span> <span data-ttu-id="5d05d-116">Nánari upplýsingar sjá [Eignagerðir](../setup-for-objects/object-types.md).</span><span class="sxs-lookup"><span data-stu-id="5d05d-116">For more information, see [Asset types](../setup-for-objects/object-types.md).</span></span>

    <span data-ttu-id="5d05d-117">Í flýtiflipanum **Upplýsingar** sýnir reiturinn **Líkön** fjölda eignalíkana sem eru settir upp á völdum eignaframleiðanda.</span><span class="sxs-lookup"><span data-stu-id="5d05d-117">In the **Details** FastTab, the **Models** field shows the number of asset models that are set up on the selected asset manufacturer.</span></span> <span data-ttu-id="5d05d-118">Reiturinn **Eignir** sýnir fjölda eigna sem eru að nota valda framleiðanda.</span><span class="sxs-lookup"><span data-stu-id="5d05d-118">The **Assets** field shows the number of assets that are using the selected manufacturer.</span></span>
    
    <span data-ttu-id="5d05d-119">Reiturinn **Eignir** sýnir fjölda hluta sem eru að nota líkan framleiðanda.</span><span class="sxs-lookup"><span data-stu-id="5d05d-119">The **Assets** field shows the number of objects that are using the manufacturer model.</span></span>

> [!NOTE]
> <span data-ttu-id="5d05d-120">Eignategund getur ekki haft nein sambönd eignaframleiðanda, hún getur tengst einni eignaframleiðslulíkani eða hún getur verið tengd fjölmörgum eignaframleiðanda.</span><span class="sxs-lookup"><span data-stu-id="5d05d-120">An asset type can have no asset manufacturer model relations, it can be related to one asset manufacturer model, or it can be related multiple asset manufacturer models.</span></span> <span data-ttu-id="5d05d-121">Ef eignategund tengist að minnsta kosti einni framleiðslulíkani, eru aðeins samsetningarnar sem settar eru upp í uppflettingunni **Framleiðandalíkan** hægt er að velja á þeim eignastýringarsíðum þar sem hægt er að setja upp samsetningu eigna, framleiðanda og líkans.</span><span class="sxs-lookup"><span data-stu-id="5d05d-121">If an asset type is related to at least one manufacturer model, only the combinations that are set up in the **Manufacturer model** lookup can be selected on those Asset Management pages where a combination of an asset type, manufacturer, and model can be set up.</span></span> <span data-ttu-id="5d05d-122">Þessar síður innihalda **Allar eignir**, **Eignaþjónustustig**, **Sjálfgefin starfstegund**, og **Viðhald fjárlagalínur**.</span><span class="sxs-lookup"><span data-stu-id="5d05d-122">These pages include **All assets**, **Asset service levels**, **Job type defaults**, and **Maintenance budget lines**.</span></span> <span data-ttu-id="5d05d-123">Ef sumar eignategundir eru ekki tengdar neinni framleiðslulíkani, eru aðeins þær eignategundir og framleiðendamódel sem hafa heldur ekki tengsl við eignategundir sýndar á síðunum.</span><span class="sxs-lookup"><span data-stu-id="5d05d-123">If some asset types aren't related to any manufacturer model, only those asset types, and manufacturer models that also have no relation to asset types, are shown on the pages.</span></span>

## <a name="select-a-manufacturer-and-model-on-an-object"></a><span data-ttu-id="5d05d-124">Veldu framleiðanda og gerð á hlut</span><span class="sxs-lookup"><span data-stu-id="5d05d-124">Select a manufacturer and model on an object</span></span>

1. <span data-ttu-id="5d05d-125">Veldu **Eignastýring** \> **Sameiginlegt** \> **Eignir** \> **Allar eignir**.</span><span class="sxs-lookup"><span data-stu-id="5d05d-125">Select **Asset management** \> **Common** \> **Assets** \> **All assets**.</span></span>
2. <span data-ttu-id="5d05d-126">Í **Eignir** dálki, veldu hlekkinn fyrir eignina.</span><span class="sxs-lookup"><span data-stu-id="5d05d-126">In the **Asset** column, select the link for the asset.</span></span> <span data-ttu-id="5d05d-127">Síðan **Upplýsingar** birtist.</span><span class="sxs-lookup"><span data-stu-id="5d05d-127">The **Details** page appears.</span></span>
3. <span data-ttu-id="5d05d-128">Veljið **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="5d05d-128">Select **Edit**.</span></span>
4. <span data-ttu-id="5d05d-129">Á flýtiflipanum **Almennt**, veldu gildi í reitunum **Framleiðandi** og **Líkan**.</span><span class="sxs-lookup"><span data-stu-id="5d05d-129">On the **General** FastTab, select values in the **Manufacturer** and **Model** fields.</span></span>
