---
title: "Þekjustillingar"
description: "Aðalröðun notar þekjustillingar til þess að reikna vöruþarfir."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: fb11a470d98a9742749daaac3244a5bb0d3a689c
ms.contentlocale: is-is
ms.lasthandoff: 08/29/2017

---

# <a name="coverage-settings"></a><span data-ttu-id="e7fa3-103">Þekjustillingar</span><span class="sxs-lookup"><span data-stu-id="e7fa3-103">Coverage settings</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="e7fa3-104">Aðalröðun notar þekjustillingar til þess að reikna vöruþarfir.</span><span class="sxs-lookup"><span data-stu-id="e7fa3-104">Master scheduling uses coverage settings to calculate item requirements.</span></span> 

<span data-ttu-id="e7fa3-105">Hægt er að tilgreina þekjustillingar með nokkrum aðferðum:</span><span class="sxs-lookup"><span data-stu-id="e7fa3-105">You can specify coverage settings in several ways:</span></span>

-   <span data-ttu-id="e7fa3-106">Tilgreina þekjustillingar fyrir þekjuflokk.</span><span class="sxs-lookup"><span data-stu-id="e7fa3-106">Specify coverage settings for a coverage group.</span></span> <span data-ttu-id="e7fa3-107">Hægt er að stofna þekjuflokk sem inniheldur stillingar fyrir allar afurðir sem eru tengdar við þekjuflokkinn.</span><span class="sxs-lookup"><span data-stu-id="e7fa3-107">You can create a coverage group that contains settings for all products that are linked to the coverage group.</span></span> <span data-ttu-id="e7fa3-108">Smellið á **Aðaláætlanagerð &gt; Uppsetning &gt; Trygging &gt; Þekjuflokkar** til að stofna þekjuflokk.</span><span class="sxs-lookup"><span data-stu-id="e7fa3-108">Click **Master planning &gt; Setup &gt; Coverage &gt; Coverage groups** to create a coverage group.</span></span> <span data-ttu-id="e7fa3-109">Hægt er að tengja þekjuflokk við vöru.</span><span class="sxs-lookup"><span data-stu-id="e7fa3-109">You can link a coverage group to a product.</span></span> <span data-ttu-id="e7fa3-110">Ef tengillinn er tilgreindur fyrir svæði, vöruhús eða afurðarvídd skal nota reitinn **Þekjuflokk** á síðunni **Vöruþekja**.</span><span class="sxs-lookup"><span data-stu-id="e7fa3-110">If the link is specific to a site, warehouse, or product dimension, use the **Coverage group** field on the **Item coverage** page.</span></span> <span data-ttu-id="e7fa3-111">Sé tengillinn almennur, án tillits til afurðarvídda, skal nota **Þekjuflokk** á flýtiflipanum **Áætlun** á síðunni **Afurðarupplýsingar**.</span><span class="sxs-lookup"><span data-stu-id="e7fa3-111">If the link is generic, regardless of the product dimensions, use the **Coverage group** on the **Plan** FastTab on the **Product details** page.</span></span> <span data-ttu-id="e7fa3-112">Ef þú tengir ekki þekjuflokk við afurð notar aðaláætlanagerð **Almennan þekjuflokk** sem tilgreindur er á síðunni **Færibreytur áætlanagerðar** sem sjálfgildi.</span><span class="sxs-lookup"><span data-stu-id="e7fa3-112">If you do not link a coverage group to a product, master planning uses the **General coverage group** that is specified on the **Master planning parameters** page as the default.</span></span>

-   <span data-ttu-id="e7fa3-113">Tilgreinið þekjustillingar fyrir afurð.</span><span class="sxs-lookup"><span data-stu-id="e7fa3-113">Specify coverage settings for a product.</span></span> <span data-ttu-id="e7fa3-114">Hægt er að breyta stillingunni fyrir ákveðna framleiðslupöntun hvenær sem er.</span><span class="sxs-lookup"><span data-stu-id="e7fa3-114">You can create coverage settings for a specific product.</span></span> <span data-ttu-id="e7fa3-115">Smellið á **Upplýsingastjórnun afurða &gt; Afurðir &gt; Losaðar afurðir**.</span><span class="sxs-lookup"><span data-stu-id="e7fa3-115">Click **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="e7fa3-116">Veljið afurðina og síðan í **Aðgerðarrúðu** á flipanum **Áætlun**, í **Þekjuflokkur** er smellt á **Vöruþekja** til að opna síðuna **Vöruþekja**.</span><span class="sxs-lookup"><span data-stu-id="e7fa3-116">Select the product, on the **Action Pane**, on the **Plan** tab, in the **Coverage group**, click **Item coverage** to open the **Item coverage** page.</span></span> <span data-ttu-id="e7fa3-117">Ef afurð er tengd þekjuflokki er hægt að hnekkja þekjuflokksstillingum með því að nota reitinn **Hnekkja**.</span><span class="sxs-lookup"><span data-stu-id="e7fa3-117">If the product is already linked to a coverage group, you can override the coverage group settings by using the **Override** field.</span></span> <span data-ttu-id="e7fa3-118">Þekjustillingar á síðunni**Vöruþekja** taka forgang yfir stillingar á síðunni **Þekjuflokkur**.</span><span class="sxs-lookup"><span data-stu-id="e7fa3-118">The coverage settings on the **Item coverage** page take precedence over the settings on the **Coverage group** page.</span></span>

<!-- -->

-   <span data-ttu-id="e7fa3-119">Tilgreinið þekjustillingar fyrir afurð með því að nota leiðsagnarforrit.</span><span class="sxs-lookup"><span data-stu-id="e7fa3-119">Specify coverage settings for a product by using a wizard.</span></span> <span data-ttu-id="e7fa3-120">Leiðsagnarforritið er leiðsögn skref fyrir skref til að hjálpa þér að setja upp færibreytur fyrir vörutryggingu.</span><span class="sxs-lookup"><span data-stu-id="e7fa3-120">The wizard is a step-by-step guide to help you set up the primary item coverage parameters.</span></span> <span data-ttu-id="e7fa3-121">Á síðunni **Vöruþekja** er smellt á **Leiðsagnarforrit** til að opna **Leiðsagnarforrit vöruþekju**.</span><span class="sxs-lookup"><span data-stu-id="e7fa3-121">On the **Item coverage** page, click **Wizard** to open the **Item Coverage Wizard**.</span></span>

<!-- -->

-   <span data-ttu-id="e7fa3-122">Tilgreinið þekjustillingar fyrir víddarflokk.</span><span class="sxs-lookup"><span data-stu-id="e7fa3-122">Specify coverage settings for a dimension group.</span></span> <span data-ttu-id="e7fa3-123">Smellið á **Upplýsingastjórnun afurða &gt; Algengt &gt; Losaðar afurðir**.</span><span class="sxs-lookup"><span data-stu-id="e7fa3-123">Click **Product information management &gt; Common &gt; Released products**.</span></span> <span data-ttu-id="e7fa3-124">Á **síðunni **Upplýsingar um losaða afurð á flipanum **Almennt** í flokknum **Stjórnun** er smellt á tengilinn **Geymsluvíddaflokkur**.</span><span class="sxs-lookup"><span data-stu-id="e7fa3-124">On the **Released product detail **page, on the **General** tab, in the **Administration** group, click the **Storage dimension group** link.</span></span> <span data-ttu-id="e7fa3-125">Á síðunni **Geymsluvíddarflokkur** skal velja **Þekjuáætlun eftir vídd** til að stofna þekjustillingar fyrir vídd í geymsluvíddarflokknum.</span><span class="sxs-lookup"><span data-stu-id="e7fa3-125">On the **Storage dimension group** page, select the **Coverage plan by dimension** field to create the coverage settings for a dimension in the storage dimension group.</span></span> <span data-ttu-id="e7fa3-126">Allar afurðavíddir, eins og skilgreining, litur, stærð, stíll, verða að hafa reitinn **Þekjuáætlun eftir vídd** valinn.</span><span class="sxs-lookup"><span data-stu-id="e7fa3-126">All product dimensions, such as configuration, color, size, style, must have the **Coverage plan by dimension** field selected.</span></span>



<a name="see-also"></a><span data-ttu-id="e7fa3-127">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="e7fa3-127">See also</span></span>
--------

[<span data-ttu-id="e7fa3-128">Aðaláætlanir</span><span class="sxs-lookup"><span data-stu-id="e7fa3-128">Master plans</span></span>](master-plans.md)




