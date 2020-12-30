---
title: Færa, skipta út og setja upp eignir
description: Þetta efni útskýrir hvernig á að færa, skipta út og setja upp eignir í eignastýringu.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectReplace, EntAssetObjectInstallLookup, EntAssetObjectMove, EntAssetObjectTableEditSubObjects
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ec150adb35eb0600844245b14cbec9e9632ab337
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430390"
---
# <a name="move-replace-and-install-assets"></a><span data-ttu-id="167b1-103">Færa, skipta út og setja upp eignir</span><span class="sxs-lookup"><span data-stu-id="167b1-103">Move, replace, and install assets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="167b1-104">Þetta efni útskýrir hvernig á að færa, skipta út og setja upp eignir í eignastýringu.</span><span class="sxs-lookup"><span data-stu-id="167b1-104">This topic explains how to move, replace, and install assets in Asset Management.</span></span> <span data-ttu-id="167b1-105">Þú getur búið til einstakar eignir sem hafa engin tengsl við aðrar eignir, eða þú getur búið til eignaskipulag sem felur í sér yfireign (efsta eign) og tengdar undireignir (undireignir).</span><span class="sxs-lookup"><span data-stu-id="167b1-105">You can create individual assets that have no relations to other assets, or you can create an asset structure that includes a parent asset (top-level asset) and related child assets (sub-assets).</span></span> <span data-ttu-id="167b1-106">Í eignastýringu eru þrjár leiðir til að færa og breyta staðsetningu eignar:</span><span class="sxs-lookup"><span data-stu-id="167b1-106">In Asset Management, there are three approaches to moving and changing the location of an asset:</span></span>

- <span data-ttu-id="167b1-107">**Færa** - Færa eign annaðhvort í aðra eignaskipan eða á annan stað í sömu eignaskipan.</span><span class="sxs-lookup"><span data-stu-id="167b1-107">**Move** – Move an asset either to another asset structure or to another location in the same asset structure.</span></span>
- <span data-ttu-id="167b1-108">**Skipta út** - Fjarlægðu eign tímabundið úr eignaskipan svo hægt sé að gera við eða endurnýja hana og bæta síðan endurnýjuðu eigninni aftur við eignaskipan síðar.</span><span class="sxs-lookup"><span data-stu-id="167b1-108">**Replace** – Temporarily remove an asset from an asset structure so that it can be repaired or refurbished, and then add the refurbished asset back to the asset structure later.</span></span> <span data-ttu-id="167b1-109">Að öðrum kosti, skipta varanlega notuðu eign út fyrir nýja eign.</span><span class="sxs-lookup"><span data-stu-id="167b1-109">Alternatively, permanently replace a used asset with a new asset.</span></span>
- <span data-ttu-id="167b1-110">**Setja upp** - Settu upp yfireign og allar tengdar undireignir á virkum stað.</span><span class="sxs-lookup"><span data-stu-id="167b1-110">**Install** – Install a parent asset and any related child assets on a functional location.</span></span>

> [!NOTE]
> <span data-ttu-id="167b1-111">Eignin sem þú flytur, skiptir út eða setur upp gæti tengst annarri virkri staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="167b1-111">The asset that you move, replace, or install might be related to another functional location.</span></span> <span data-ttu-id="167b1-112">Í því tilfelli gæti eignin notað fjárhagsvíddir á virkri staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="167b1-112">In that case, the asset might use financial dimensions of the functional location.</span></span> <span data-ttu-id="167b1-113">Á síðunni **Gerðir virkra staðsetninga** setur þú upp meðhöndlun fjárhagsvíddar á virkum staðsetningum.</span><span class="sxs-lookup"><span data-stu-id="167b1-113">On the **Functional location types** page, you set up the handling of financial dimensions on functional locations.</span></span>

## <a name="move-asset"></a><span data-ttu-id="167b1-114">Færa eign</span><span class="sxs-lookup"><span data-stu-id="167b1-114">Move asset</span></span>

<span data-ttu-id="167b1-115">Notaðu virknina **Færa eign** til að færa eign annaðhvort í aðra eignaskipan eða á annan stað í sömu eignaskipan.</span><span class="sxs-lookup"><span data-stu-id="167b1-115">Use the **Move asset** function to move an asset either to another asset structure or to another location in the same asset structure.</span></span> <span data-ttu-id="167b1-116">Þú getur líka fært eign út úr eignaskipan þannig að hún verði sjálfstæða eign sem hefur engin tengsl við uppbyggingu.</span><span class="sxs-lookup"><span data-stu-id="167b1-116">You can also move an asset out of an asset structure so that it becomes a standalone asset that has no structure relations.</span></span>

> [!NOTE]
> <span data-ttu-id="167b1-117">Ekki nota þessa aðgerð ef verið er að gera við eignir eða skipta tímabundið út.</span><span class="sxs-lookup"><span data-stu-id="167b1-117">Don't use this function if assets are being repaired or temporarily replaced.</span></span> <span data-ttu-id="167b1-118">Notaðu í staðinn virknina **Skipta út eign** sem lýst er síðar í þessu efni.</span><span class="sxs-lookup"><span data-stu-id="167b1-118">Instead, use the **Replace asset** functionality that is described later in this topic.</span></span>

1. <span data-ttu-id="167b1-119">Veldu **Eignastýring** \> **Sameiginlegt** \> **Eignir** \> **Allar eignir** eða **Virkar eignir**.</span><span class="sxs-lookup"><span data-stu-id="167b1-119">Select **Asset management** \> **Common** \> **Assets** \> **All assets** or **Active assets**.</span></span>
2. <span data-ttu-id="167b1-120">Á listanum, veljið eign til að færa.</span><span class="sxs-lookup"><span data-stu-id="167b1-120">In the list, select the asset to move.</span></span> <span data-ttu-id="167b1-121">Ef eignin er með undireignir þá færir þú líka þessar eignir.</span><span class="sxs-lookup"><span data-stu-id="167b1-121">If the asset has child assets, you also move those assets.</span></span>
3. <span data-ttu-id="167b1-122">Velja **Færa eign**.</span><span class="sxs-lookup"><span data-stu-id="167b1-122">Select **Move asset**.</span></span>
4. <span data-ttu-id="167b1-123">Til að færa eignina þannig að hún verði hluti af eignaskipan skaltu velja nýju yfireignina í reitnum **Yfireign**.</span><span class="sxs-lookup"><span data-stu-id="167b1-123">To move the asset so that it becomes part of an asset structure, select the new parent asset in the **Parent asset** field.</span></span> <span data-ttu-id="167b1-124">Ef þú ert að flytja undireign, og þú vilt gera hana að sjálfstæða eign sem hefur engin tengsl við uppbyggingu, skaltu hafa reitinn **Yfireign** auður.</span><span class="sxs-lookup"><span data-stu-id="167b1-124">If you're moving a child asset, and you want to make it a standalone asset that has no structure relations, leave the **Parent asset** field blank.</span></span>
5. <span data-ttu-id="167b1-125">Sjálfgefið er að reiturinn **Virkt** sé sjálfkrafa stilltur á núverandi dagsetningu og tíma.</span><span class="sxs-lookup"><span data-stu-id="167b1-125">By default, the **Effective** field is set to the current date and time.</span></span> <span data-ttu-id="167b1-126">Hins vegar getur þú valið annan dag og tíma sem eignaflutningurinn gildir frá.</span><span class="sxs-lookup"><span data-stu-id="167b1-126">However, you can select a different date and time that the asset move is valid from.</span></span>
6. <span data-ttu-id="167b1-127">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="167b1-127">Select **OK**.</span></span>

## <a name="replace-asset"></a><span data-ttu-id="167b1-128">Skipta út eign</span><span class="sxs-lookup"><span data-stu-id="167b1-128">Replace asset</span></span>

<span data-ttu-id="167b1-129">Notaðu virknina **Skipta út eign** í tengslum við viðgerðir, endurbætur eða varanlega skipti á slitinni eign með nýrri eign.</span><span class="sxs-lookup"><span data-stu-id="167b1-129">Use the **Replace asset** function in connection with repairs, refurbishment, or permanent replacement of a worn-out asset by a new asset.</span></span> <span data-ttu-id="167b1-130">Þessi aðgerð er notuð til að skipta út undireignum í eignaskipan.</span><span class="sxs-lookup"><span data-stu-id="167b1-130">This function is used to replace child assets in an asset structure.</span></span> <span data-ttu-id="167b1-131">Fyrir yfireignir (það er að segja eignir sem ekki eru með yfireign eins og er) er þessi skipti gerð á virkan stað.</span><span class="sxs-lookup"><span data-stu-id="167b1-131">For parent assets (that is, assets that don't currently have a parent asset), this replacement is done on a functional location.</span></span> <span data-ttu-id="167b1-132">Nánari upplýsingar um hvernig á að skipta um yfireignir á virkum stað, sjá [Setja upp eignir á virkum staðsetningum](../functional-locations/install-objects-on-functional-locations.md).</span><span class="sxs-lookup"><span data-stu-id="167b1-132">For more information about how to replace parent assets on a functional location, see [Install assets on functional locations](../functional-locations/install-objects-on-functional-locations.md).</span></span>

> [!NOTE]
> <span data-ttu-id="167b1-133">Ef viðgerðarverkstæði er tengd framleiðsludeildinni þinni geturðu búið til virkar staðsetningar eins og **Viðger**, **Rusl**, og **Geymsla** til að sjá um viðgerðir og skipti á eignum.</span><span class="sxs-lookup"><span data-stu-id="167b1-133">If a repair shop is related to your production department, you can create functional locations such as **Repair**, **Scrap**, and **Storage** to handle the repair and replacement of assets.</span></span>

1. <span data-ttu-id="167b1-134">Veldu **Eignastýring** \> **Sameiginlegt** \> **Eignir** \> **Allar eignir** eða **Virkar eignir**.</span><span class="sxs-lookup"><span data-stu-id="167b1-134">Select **Asset management** \> **Common** \> **Assets** \> **All assets** or **Active assets**.</span></span>
2. <span data-ttu-id="167b1-135">Á listanum, veljið undireign til að skipta út.</span><span class="sxs-lookup"><span data-stu-id="167b1-135">In the list, select the child asset to replace.</span></span> <span data-ttu-id="167b1-136">Ef eignin er með undireignir þá skiptir þú um þessar eignir.</span><span class="sxs-lookup"><span data-stu-id="167b1-136">If the asset has child assets, you also replace those assets.</span></span>
3. <span data-ttu-id="167b1-137">Veldu **Skipta út eign**.</span><span class="sxs-lookup"><span data-stu-id="167b1-137">Select **Replace asset**.</span></span>

    <span data-ttu-id="167b1-138">Reiturinn **Breytt skipulag** sýnir síðustu dagsetningu og tíma sem valin eign og tengdar undireignir voru færð í eignaskipan.</span><span class="sxs-lookup"><span data-stu-id="167b1-138">The **Structure change** field shows the last date and time that the selected asset and related child assets were moved in the asset structure.</span></span>

4. <span data-ttu-id="167b1-139">Í lutanum **Valin eign** í reitnum **Virk markstaðsetning** veldu hagnýta staðsetningu til að færa eignina til.</span><span class="sxs-lookup"><span data-stu-id="167b1-139">In the **Selected asset** section, in the **Target functional location** field, select the functional location to move the asset to.</span></span> <span data-ttu-id="167b1-140">Veldu til dæmis staðsetninguna **Viðgerð** eða **Rusl**.</span><span class="sxs-lookup"><span data-stu-id="167b1-140">For example, select the **Repair** or **Scrap** location.</span></span>

    <span data-ttu-id="167b1-141">Í hlutanum **Yfireign** sýnir reiturinn **Virkt** síðustu dagsetningu og tíma sem yfireignin og tengdar undireignir voru settar upp eða fluttar á núverandi virka staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="167b1-141">In the **Parent asset** section, the **Effective** field shows the last date and time that the parent asset and related child assets were installed or moved on the current functional location.</span></span>

5. <span data-ttu-id="167b1-142">Í hlutanum **Ný eign** velurðu í reitnum **Eignir** eignina sem á að setja inn sem tímabundin eða varanleg skipti fyrir valda eign.</span><span class="sxs-lookup"><span data-stu-id="167b1-142">In the **New asset** section, in the **Asset** field, select the asset to insert as a temporary or permanent replacement for the selected asset.</span></span> <span data-ttu-id="167b1-143">Þessi eign gæti nú verið staðsett á öðrum virkum stað, svo sem **Geymsla**.</span><span class="sxs-lookup"><span data-stu-id="167b1-143">This asset might currently be located on another functional location, such as **Storage**.</span></span>
7. <span data-ttu-id="167b1-144">Í hlutanum **Virkt frá** er reiturinn **Virkt** sjálfkrafa stilltur á núverandi dagsetningu og tíma.</span><span class="sxs-lookup"><span data-stu-id="167b1-144">In the **Effective from** section, the **Effective** field is set to the current date and time by default.</span></span> <span data-ttu-id="167b1-145">Hins vegar getur þú valið annan dag og tíma sem eignaskiptin gildir frá.</span><span class="sxs-lookup"><span data-stu-id="167b1-145">However, you can select a different date and time that the asset replacement is valid from.</span></span>
8. <span data-ttu-id="167b1-146">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="167b1-146">Select **OK**.</span></span>

## <a name="install-asset"></a><span data-ttu-id="167b1-147">Settu upp eign</span><span class="sxs-lookup"><span data-stu-id="167b1-147">Install asset</span></span>

<span data-ttu-id="167b1-148">Notaðu aðgerðina **Setja upp eign** til að setja upp eignaskipulag á virkan stað.</span><span class="sxs-lookup"><span data-stu-id="167b1-148">Use the **Install asset** function to install an asset structure on a functional location.</span></span>

> [!NOTE]
> <span data-ttu-id="167b1-149">Veldu alltaf yfireign.</span><span class="sxs-lookup"><span data-stu-id="167b1-149">Always select a parent asset.</span></span> <span data-ttu-id="167b1-150">Yfireignin og tengdar undireignir verða færðar á valda staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="167b1-150">The parent asset and related child assets will be moved to the selected functional location.</span></span>

1. <span data-ttu-id="167b1-151">Veldu **Eignastýring** \> **Sameiginlegt** \> **Eignir** \> **Allar eignir** eða **Virkar eignir**.</span><span class="sxs-lookup"><span data-stu-id="167b1-151">Select **Asset management** \> **Common** \> **Assets** \> **All assets** or **Active assets**.</span></span>
2. <span data-ttu-id="167b1-152">Veldu listann á yfireignina sem á að setja upp á öðrum virkum stað.</span><span class="sxs-lookup"><span data-stu-id="167b1-152">In the list, select the parent asset to install on another functional location.</span></span>
3. <span data-ttu-id="167b1-153">Velja **Setja upp eign**.</span><span class="sxs-lookup"><span data-stu-id="167b1-153">Select **Install asset**.</span></span>

    <span data-ttu-id="167b1-154">Hlutinn **Eigindi** sýnir þær eignaeigindir sem eru settar upp á yfireigninni.</span><span class="sxs-lookup"><span data-stu-id="167b1-154">The **Attributes** section shows the asset attributes that are set up on the parent asset.</span></span>

4. <span data-ttu-id="167b1-155">Í reitnum **Virk staðsetning** skal velja nýja staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="167b1-155">In the **Functional location** field, select the new location.</span></span>
5. <span data-ttu-id="167b1-156">Sjálfgefið er að reiturinn **Virkt** sé sjálfkrafa stilltur á núverandi dagsetningu og tíma.</span><span class="sxs-lookup"><span data-stu-id="167b1-156">By default, the **Effective** field is set to the current date and time.</span></span> <span data-ttu-id="167b1-157">Hins vegar getur þú valið annan dag og tíma sem uppsetning á eignaskipulaginu gildir frá.</span><span class="sxs-lookup"><span data-stu-id="167b1-157">However, you can select a different date and time that the installation on the asset structure is valid from.</span></span>
6. <span data-ttu-id="167b1-158">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="167b1-158">Select **OK**.</span></span>
