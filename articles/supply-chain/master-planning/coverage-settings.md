---
title: Þekjustillingar
description: Þetta efnisatriði veitir upplýsingar um þekjustillingar sem aðalröðun notar til að reikna út vöruþarfir.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 99e094a7131b6d3a299fc72abd0141529908ddd2
ms.sourcegitcommit: 9e50bee6a67f0fe2fa6f86e02c7e8de16d0e2482
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/08/2019
ms.locfileid: "1538895"
---
# <a name="coverage-settings"></a><span data-ttu-id="8f43f-103">Þekjustillingar</span><span class="sxs-lookup"><span data-stu-id="8f43f-103">Coverage settings</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8f43f-104">Aðalröðun notar þekjustillingar til þess að reikna vöruþarfir.</span><span class="sxs-lookup"><span data-stu-id="8f43f-104">Master scheduling uses coverage settings to calculate item requirements.</span></span>

<span data-ttu-id="8f43f-105">Hægt er að tilgreina þekjustillingar með nokkrum aðferðum:</span><span class="sxs-lookup"><span data-stu-id="8f43f-105">You can specify coverage settings in several ways:</span></span>

- <span data-ttu-id="8f43f-106">Tilgreina þekjustillingar fyrir þekjuflokk.</span><span class="sxs-lookup"><span data-stu-id="8f43f-106">Specify coverage settings for a coverage group.</span></span>

    <span data-ttu-id="8f43f-107">Hægt er að stofna þekjuflokk sem inniheldur stillingar fyrir allar afurðir sem eru tengdar við þekjuflokkinn.</span><span class="sxs-lookup"><span data-stu-id="8f43f-107">You can create a coverage group that contains settings for all products that are linked to the coverage group.</span></span> <span data-ttu-id="8f43f-108">Til að stofna þekjuflokk skal opna **Aðaláætlanagerð &gt; Uppsetning &gt; Þekja &gt; Þekjuflokkar**.</span><span class="sxs-lookup"><span data-stu-id="8f43f-108">To create a coverage group, go to **Master planning &gt; Setup &gt; Coverage &gt; Coverage groups**.</span></span> <span data-ttu-id="8f43f-109">Hægt er að tengja þekjuflokk við vöru.</span><span class="sxs-lookup"><span data-stu-id="8f43f-109">You can link a coverage group to a product.</span></span> <span data-ttu-id="8f43f-110">Ef tengillinn er tilgreindur fyrir svæði, vöruhús eða afurðarvídd skal nota reitinn **Þekjuflokk** á síðunni **Vöruþekja**.</span><span class="sxs-lookup"><span data-stu-id="8f43f-110">If the link is specific to a site, warehouse, or product dimension, use the **Coverage group** field on the **Item coverage** page.</span></span> <span data-ttu-id="8f43f-111">Sé tengillinn almennur, án tillits til afurðarvídda, skal nota reitinn **Þekjuflokk** á flýtiflipanum **Áætlun** á síðunni **Afurðarupplýsingar**.</span><span class="sxs-lookup"><span data-stu-id="8f43f-111">If the link is generic, regardless of the product dimensions, use the **Coverage group** field on the **Plan** FastTab of the **Product details** page.</span></span> <span data-ttu-id="8f43f-112">Ef þú tengir ekki þekjuflokk við afurð notar aðaláætlanagerð sem sjálfgildi almennan þekjuflokk sem tilgreindur er á síðunni **Færibreytur áætlanagerðar**.</span><span class="sxs-lookup"><span data-stu-id="8f43f-112">By default, if you don't link a coverage group to a product, master planning uses the general coverage group that is specified on the **Master planning parameters** page.</span></span>

- <span data-ttu-id="8f43f-113">Tilgreinið þekjustillingar fyrir afurð.</span><span class="sxs-lookup"><span data-stu-id="8f43f-113">Specify coverage settings for a product.</span></span>

    <span data-ttu-id="8f43f-114">Hægt er að breyta stillingunni fyrir ákveðna framleiðslupöntun hvenær sem er.</span><span class="sxs-lookup"><span data-stu-id="8f43f-114">You can create coverage settings for a specific product.</span></span> <span data-ttu-id="8f43f-115">Opna **Afurðaupplýsingastjórnun &gt; Afurðir &gt; Útgefnar afurðir**.</span><span class="sxs-lookup"><span data-stu-id="8f43f-115">Go to **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="8f43f-116">Veljið afurðina og síðan í Aðgerðarrúðu á flipanum **Áætlun**, í flokknum **Þekja**, skal velja **Vöruþekja** til að opna síðuna **Vöruþekja**.</span><span class="sxs-lookup"><span data-stu-id="8f43f-116">Select the product, and then, on the Action Pane, on the **Plan** tab, in the **Coverage** group, select **Item coverage** to open the **Item coverage** page.</span></span> <span data-ttu-id="8f43f-117">Ef afurð er tengd þekjuflokki er hægt að hnekkja þekjuflokksstillingum með því að nota reitinn **Hnekkja**.</span><span class="sxs-lookup"><span data-stu-id="8f43f-117">If the product is already linked to a coverage group, you can override the coverage group settings by using the **Override** field.</span></span> <span data-ttu-id="8f43f-118">Þekjustillingar á síðunni**Vöruþekja** taka forgang yfir stillingar á síðunni **Þekjuflokkur**.</span><span class="sxs-lookup"><span data-stu-id="8f43f-118">The coverage settings on the **Item coverage** page take precedence over the settings on the **Coverage group** page.</span></span>

- <span data-ttu-id="8f43f-119">Tilgreinið þekjustillingar fyrir afurð með því að nota leiðsagnarforrit.</span><span class="sxs-lookup"><span data-stu-id="8f43f-119">Specify coverage settings for a product by using a wizard.</span></span>

    <span data-ttu-id="8f43f-120">Leiðsagnarforritið leiðir þig skref fyrir skref í gegnum ferlið við að setja upp færibreytur fyrir helstu vöruþekjuna.</span><span class="sxs-lookup"><span data-stu-id="8f43f-120">The wizard guides you step by step through the process of setting up the primary item coverage parameters.</span></span> <span data-ttu-id="8f43f-121">Á síðunni **Vöruþekja**, í aðgerðarúðunni, er valið **Leiðsagnarforrit** til að opna **Leiðsagnarforrit vöruþekju**.</span><span class="sxs-lookup"><span data-stu-id="8f43f-121">On the **Item coverage** page, on the Action Pane, select **Wizard** to open the **Item Coverage Wizard**.</span></span>

- <span data-ttu-id="8f43f-122">Tilgreinið þekjustillingar fyrir víddarflokk.</span><span class="sxs-lookup"><span data-stu-id="8f43f-122">Specify coverage settings for a dimension group.</span></span>

    <span data-ttu-id="8f43f-123">Opna **Afurðaupplýsingastjórnun &gt; Afurðir &gt; Útgefnar afurðir**.</span><span class="sxs-lookup"><span data-stu-id="8f43f-123">Go to **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="8f43f-124">Á síðunni **Upplýsingar um losaðar afurðir** á flýtiflipanum **Almennt**, í hlutanum **Stjórnun**, er smellt á tengilinn í reitnum **Geymsluvíddarflokkur**.</span><span class="sxs-lookup"><span data-stu-id="8f43f-124">On the **Released product details** page, on the **General** FastTab, in the **Administration** section, select the link in the **Storage dimension group** field.</span></span> <span data-ttu-id="8f43f-125">Á síðunni **Geymsluvíddarflokkur** skal velja gátreitinn **Þekjuáætlun eftir vídd** til að stofna þekjustillingar fyrir vídd í geymsluvíddarflokknum.</span><span class="sxs-lookup"><span data-stu-id="8f43f-125">On the **Storage dimension groups** page, select the **Coverage plan by dimension** check box to create the coverage settings for a dimension in the storage dimension group.</span></span> <span data-ttu-id="8f43f-126">Velja verður reitinn **Þekjuáætlun eftir vídd** fyrir allar afurðarvíddir, t.d. skilgreiningu, lit, stærð og stíl.</span><span class="sxs-lookup"><span data-stu-id="8f43f-126">The **Coverage plan by dimension** field must be selected for all product dimensions, such as configuration, color, size, and style.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8f43f-127">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="8f43f-127">Additional resources</span></span>

[<span data-ttu-id="8f43f-128">Aðaláætlanir</span><span class="sxs-lookup"><span data-stu-id="8f43f-128">Master plans</span></span>](master-plans.md)
