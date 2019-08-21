---
title: Stigskiptar eignir
description: Þetta efni útskýrir hvernig á að búa til og eyða eignum í mörgum stigum.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0f38253317ed8f06318fc501511ca5263a614e20
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783345"
---
# <a name="multi-level-assets"></a><span data-ttu-id="b6123-103">Stigskiptar eignir</span><span class="sxs-lookup"><span data-stu-id="b6123-103">Multi-level assets</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="b6123-104">Þetta efni útskýrir hvernig á að búa til og eyða eignum í mörgum stigum.</span><span class="sxs-lookup"><span data-stu-id="b6123-104">This topic explains how to create and delete multi-level assets.</span></span> <span data-ttu-id="b6123-105">Þú getur búið til eignir og tengdar undireignir í stigskiptri trjábyggingu.</span><span class="sxs-lookup"><span data-stu-id="b6123-105">You can create assets and related sub-assets in a hierarchical tree structure.</span></span> <span data-ttu-id="b6123-106">Á þennan hátt geturðu sýnt sambönd og ósjálfstæði meðal eigna.</span><span class="sxs-lookup"><span data-stu-id="b6123-106">In this way, you can show relations and dependencies among assets.</span></span> <span data-ttu-id="b6123-107">Viðhaldsstörf geta tengst öllum stigum trébyggingarinnar.</span><span class="sxs-lookup"><span data-stu-id="b6123-107">Maintenance jobs can be related to all levels of the tree structure.</span></span> <span data-ttu-id="b6123-108">Einnig er hægt að búa til tölfræði fyrir einstaklingstig eða sem summa af öllum undireignarstigum.</span><span class="sxs-lookup"><span data-stu-id="b6123-108">Statistics can also be created for an individual level or as a sum of all sub-asset levels.</span></span>

<span data-ttu-id="b6123-109">Á listasíðunni **Allar eignir** (**Eignastýring** \> **Sameiginlegt** \> **Eignir** \> **Allar eignir**), sýnir dálkurinn **Eignir** eignir í stigveldi.</span><span class="sxs-lookup"><span data-stu-id="b6123-109">On the **All Assets** list page (**Asset management** \> **Common** \> **Assets** \> **All assets**), the **Asset** column lists assets in hierarchical order.</span></span> <span data-ttu-id="b6123-110">Dálkurinn **Yfireining** sýnar tengdar yfireiningar.</span><span class="sxs-lookup"><span data-stu-id="b6123-110">The **Parent** column shows the related parent.</span></span> <span data-ttu-id="b6123-111">Að auki, ef eignir og undireignir hafa þegar verið stofnaðar sýnir hlutinn **Eignatré** í glugganum **Tengdar upplýsingar** eignirnar í trjábyggingu.</span><span class="sxs-lookup"><span data-stu-id="b6123-111">Additionally, if assets and sub-assets have already been created, the **Asset tree** section in the **Related information** pane shows the assets in a tree structure.</span></span>

<span data-ttu-id="b6123-112">Nánari upplýsingar um hvernig stofna eigi eign, sjá [Stofna eign](../objects/create-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="b6123-112">For information about how to create an asset, see [Create an asset](../objects/create-an-object.md).</span></span> <span data-ttu-id="b6123-113">Til að búa til undireign skal velja yfireignina í reitnum **Yfireining** á flýtiflipanum **Almennt**.</span><span class="sxs-lookup"><span data-stu-id="b6123-113">To create a sub-asset, select the parent asset in the **Parent** field on the **General** FastTab.</span></span>

## <a name="copy-an-asset-or-asset-structure"></a><span data-ttu-id="b6123-114">Afritaðu eign eða uppbyggingu eigna</span><span class="sxs-lookup"><span data-stu-id="b6123-114">Copy an asset or asset structure</span></span>

<span data-ttu-id="b6123-115">Ef fyrirtæki þitt hefur nokkra svipaða eignaskipulag geturðu notað afritunaraðgerðina í eignastjórnun til að búa þau fljótt til.</span><span class="sxs-lookup"><span data-stu-id="b6123-115">If your company has several similar asset structures, you can use the Copy function in Asset Management to quickly create them.</span></span>

1. <span data-ttu-id="b6123-116">Veldu **Eignastýring** \> **Sameiginlegt** \> **Eignir** \> **Allar eignir**.</span><span class="sxs-lookup"><span data-stu-id="b6123-116">Select **Asset management** \> **Common** \> **Assets** \> **All assets**.</span></span>
2. <span data-ttu-id="b6123-117">Á listasíðunni **Allar eignir**, veldu eignina sem á að afrita.</span><span class="sxs-lookup"><span data-stu-id="b6123-117">On the **All assets** list page, select the asset to copy.</span></span> <span data-ttu-id="b6123-118">Til dæmis, ef þú vilt afrita alla eignaskipulagið, þar á meðal undireignir, skaltu velja yfireign.</span><span class="sxs-lookup"><span data-stu-id="b6123-118">For example, if you want to copy the whole asset structure, including sub-assets, select a parent asset.</span></span>
3. <span data-ttu-id="b6123-119">Veldu **Afrita eign**.</span><span class="sxs-lookup"><span data-stu-id="b6123-119">Select **Copy asset**.</span></span> <span data-ttu-id="b6123-120">Í hlutanum **Afrita frá** er reiturinn **Eignir** stilltur á eignina sem þú valdir á listasíðunni.</span><span class="sxs-lookup"><span data-stu-id="b6123-120">In the **Copy from** section, the **Asset** field is set to the asset that you selected on the list page.</span></span>
4. <span data-ttu-id="b6123-121">Í hlutanum **Afrita í** í reitnum **Eignir** slærðu inn nafn nýju eignarinnar.</span><span class="sxs-lookup"><span data-stu-id="b6123-121">In the **Copy to** section, in the **Asset** field, enter the name of the new asset.</span></span>
5. <span data-ttu-id="b6123-122">Ef eignin sem þú ert að búa til ætti að vera hluti af núverandi eignaskipan, skaltu velja fyrirkenni í hlutanum **Yfireign** í retinum **Eignir**.</span><span class="sxs-lookup"><span data-stu-id="b6123-122">If the asset that you're creating should be part of an existing asset structure, in the **Parent asset** section, in the **Asset** field, select a parent ID.</span></span>
6. <span data-ttu-id="b6123-123">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="b6123-123">Select **OK**.</span></span> <span data-ttu-id="b6123-124">Nýja eignaskipan er sýnd á **Allar eignir** listasíðu.</span><span class="sxs-lookup"><span data-stu-id="b6123-124">The new asset structure is shown on the **All assets** list page.</span></span> <span data-ttu-id="b6123-125">Allir eignareiginleikar, viðhaldsáætlanir og viðhaldsumferðir sem tengjast eigninni sem þú afritaðir eru fluttar yfir í nýju eignina eða eignaskipan.</span><span class="sxs-lookup"><span data-stu-id="b6123-125">All asset attributes, maintenance plans, and maintenance rounds that are related to the asset that you copied are transferred to the new asset or asset structure.</span></span>

<span data-ttu-id="b6123-126">Þegar þú afritar eignaskipulag hafa undireignirnar í nýju skipulaginu sama nafn og undireignirnar sem þú afritaðir.</span><span class="sxs-lookup"><span data-stu-id="b6123-126">When you copy an asset structure, the sub-assets in the new structure have the same name as the sub-assets that you copied.</span></span> <span data-ttu-id="b6123-127">Eftir að afritunarferlinu er lokið geturðu auðveldlega breytt nafni og öðrum stillingum fyrir eign.</span><span class="sxs-lookup"><span data-stu-id="b6123-127">After the copy procedure is completed, you can easily change the name and other settings for an asset.</span></span> <span data-ttu-id="b6123-128">Veldu eignina á listasíðunni **Allar eignir** og veldu síðan hnappinn **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="b6123-128">Select the asset on the **All assets** list page, and then select the **Edit** button.</span></span>

> [!NOTE]
> <span data-ttu-id="b6123-129">Þegar þú afritar eign eða eignaskipulag er líftíma hinna nýju eigna endurstillt í það ástand sem þú skilgreindir sem upphafsástand lífsins fyrir eignir.</span><span class="sxs-lookup"><span data-stu-id="b6123-129">When you copy an asset or asset structure, the lifecycle state of the new assets is reset to whatever state you defined as the initial lifecycle state for assets.</span></span> <span data-ttu-id="b6123-130">Virka staðsetningin er núllstillt á sjálfgefna virka staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="b6123-130">The functional location is reset to the default functional location.</span></span>

## <a name="delete-an-asset-or-asset-structure"></a><span data-ttu-id="b6123-131">Eyða eign eða uppbyggingu eigna</span><span class="sxs-lookup"><span data-stu-id="b6123-131">Delete an asset or asset structure</span></span>

<span data-ttu-id="b6123-132">Ef eign hefur tengdar undireignir geturðu eingöngu eytt henni ef engar viðhaldsbeiðnir, verkbeiðnastörf, bilunarskráningar eða ástandsmat eru skráð á einhverja af eignunum.</span><span class="sxs-lookup"><span data-stu-id="b6123-132">If an asset has related sub-assets, you can delete it only if no maintenance requests, work order jobs, fault registrations, or condition assessments are registered on any of the assets.</span></span>

1. <span data-ttu-id="b6123-133">Á listasíðunni **Allar eignir**, veldu eignina sem á að eyða.</span><span class="sxs-lookup"><span data-stu-id="b6123-133">On the **All assets** list page, select the asset to delete.</span></span>
2. <span data-ttu-id="b6123-134">Veljið **Eyða**.</span><span class="sxs-lookup"><span data-stu-id="b6123-134">Select **Delete**.</span></span>

> [!NOTE]
> <span data-ttu-id="b6123-135">Ef þú getur ekki eytt eign með því að nota þessa aðferð, er önnur leið til að takast á við eyðingu að setja upp eignatíma í þessu skyni.</span><span class="sxs-lookup"><span data-stu-id="b6123-135">If you can't delete an asset by using this procedure, another way to handle deletion is to set up an asset lifecycle state for this purpose.</span></span> <span data-ttu-id="b6123-136">Til dæmis er hægt að setja upp líftímastöðuna **Hent** eða **Eytt** á síðunni **Líftímastaða eigna**.</span><span class="sxs-lookup"><span data-stu-id="b6123-136">For example, you can set up a **Scrapped** or **Deleted** lifecycle state on the **Asset lifecycle states** page.</span></span>
