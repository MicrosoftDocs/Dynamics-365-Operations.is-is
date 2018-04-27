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
ms.search.scope: Core, Operations
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 591b1cd739bb3be61299f33f180ca7c264d21a35
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---

# <a name="coverage-settings"></a><span data-ttu-id="84f4e-103">Þekjustillingar</span><span class="sxs-lookup"><span data-stu-id="84f4e-103">Coverage settings</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="84f4e-104">Aðalröðun notar þekjustillingar til þess að reikna vöruþarfir.</span><span class="sxs-lookup"><span data-stu-id="84f4e-104">Master scheduling uses coverage settings to calculate item requirements.</span></span> 

<span data-ttu-id="84f4e-105">Hægt er að tilgreina þekjustillingar með nokkrum aðferðum:</span><span class="sxs-lookup"><span data-stu-id="84f4e-105">You can specify coverage settings in several ways:</span></span>

-   <span data-ttu-id="84f4e-106">Tilgreina þekjustillingar fyrir þekjuflokk.</span><span class="sxs-lookup"><span data-stu-id="84f4e-106">Specify coverage settings for a coverage group.</span></span> <span data-ttu-id="84f4e-107">Hægt er að stofna þekjuflokk sem inniheldur stillingar fyrir allar afurðir sem eru tengdar við þekjuflokkinn.</span><span class="sxs-lookup"><span data-stu-id="84f4e-107">You can create a coverage group that contains settings for all products that are linked to the coverage group.</span></span> <span data-ttu-id="84f4e-108">Smellið á **Aðaláætlanagerð &gt; Uppsetning &gt; Trygging &gt; Þekjuflokkar** til að stofna þekjuflokk.</span><span class="sxs-lookup"><span data-stu-id="84f4e-108">Click **Master planning &gt; Setup &gt; Coverage &gt; Coverage groups** to create a coverage group.</span></span> <span data-ttu-id="84f4e-109">Hægt er að tengja þekjuflokk við vöru.</span><span class="sxs-lookup"><span data-stu-id="84f4e-109">You can link a coverage group to a product.</span></span> <span data-ttu-id="84f4e-110">Ef tengillinn er tilgreindur fyrir svæði, vöruhús eða afurðarvídd skal nota reitinn **Þekjuflokk** á síðunni **Vöruþekja**.</span><span class="sxs-lookup"><span data-stu-id="84f4e-110">If the link is specific to a site, warehouse, or product dimension, use the **Coverage group** field on the **Item coverage** page.</span></span> <span data-ttu-id="84f4e-111">Sé tengillinn almennur, án tillits til afurðarvídda, skal nota **Þekjuflokk** á flýtiflipanum **Áætlun** á síðunni **Afurðarupplýsingar**.</span><span class="sxs-lookup"><span data-stu-id="84f4e-111">If the link is generic, regardless of the product dimensions, use the **Coverage group** on the **Plan** FastTab on the **Product details** page.</span></span> <span data-ttu-id="84f4e-112">Ef þú tengir ekki þekjuflokk við afurð notar aðaláætlanagerð **Almennan þekjuflokk** sem tilgreindur er á síðunni **Færibreytur áætlanagerðar** sem sjálfgildi.</span><span class="sxs-lookup"><span data-stu-id="84f4e-112">If you do not link a coverage group to a product, master planning uses the **General coverage group** that is specified on the **Master planning parameters** page as the default.</span></span>

-   <span data-ttu-id="84f4e-113">Tilgreinið þekjustillingar fyrir afurð.</span><span class="sxs-lookup"><span data-stu-id="84f4e-113">Specify coverage settings for a product.</span></span> <span data-ttu-id="84f4e-114">Hægt er að breyta stillingunni fyrir ákveðna framleiðslupöntun hvenær sem er.</span><span class="sxs-lookup"><span data-stu-id="84f4e-114">You can create coverage settings for a specific product.</span></span> <span data-ttu-id="84f4e-115">Smellið á **Upplýsingastjórnun afurða &gt; Afurðir &gt; Losaðar afurðir**.</span><span class="sxs-lookup"><span data-stu-id="84f4e-115">Click **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="84f4e-116">Veljið afurðina og síðan í **Aðgerðarrúðu** á flipanum **Áætlun**, í **Þekjuflokkur** er smellt á **Vöruþekja** til að opna síðuna **Vöruþekja**.</span><span class="sxs-lookup"><span data-stu-id="84f4e-116">Select the product, on the **Action Pane**, on the **Plan** tab, in the **Coverage group**, click **Item coverage** to open the **Item coverage** page.</span></span> <span data-ttu-id="84f4e-117">Ef afurð er tengd þekjuflokki er hægt að hnekkja þekjuflokksstillingum með því að nota reitinn **Hnekkja**.</span><span class="sxs-lookup"><span data-stu-id="84f4e-117">If the product is already linked to a coverage group, you can override the coverage group settings by using the **Override** field.</span></span> <span data-ttu-id="84f4e-118">Þekjustillingar á síðunni**Vöruþekja** taka forgang yfir stillingar á síðunni **Þekjuflokkur**.</span><span class="sxs-lookup"><span data-stu-id="84f4e-118">The coverage settings on the **Item coverage** page take precedence over the settings on the **Coverage group** page.</span></span>

<!-- -->

-   <span data-ttu-id="84f4e-119">Tilgreinið þekjustillingar fyrir afurð með því að nota leiðsagnarforrit.</span><span class="sxs-lookup"><span data-stu-id="84f4e-119">Specify coverage settings for a product by using a wizard.</span></span> <span data-ttu-id="84f4e-120">Leiðsagnarforritið er leiðsögn skref fyrir skref til að hjálpa þér að setja upp færibreytur fyrir vörutryggingu.</span><span class="sxs-lookup"><span data-stu-id="84f4e-120">The wizard is a step-by-step guide to help you set up the primary item coverage parameters.</span></span> <span data-ttu-id="84f4e-121">Á síðunni **Vöruþekja** er smellt á **Leiðsagnarforrit** til að opna **Leiðsagnarforrit vöruþekju**.</span><span class="sxs-lookup"><span data-stu-id="84f4e-121">On the **Item coverage** page, click **Wizard** to open the **Item Coverage Wizard**.</span></span>

<!-- -->

- <span data-ttu-id="84f4e-122">Tilgreinið þekjustillingar fyrir víddarflokk.</span><span class="sxs-lookup"><span data-stu-id="84f4e-122">Specify coverage settings for a dimension group.</span></span> <span data-ttu-id="84f4e-123">Smellið á <strong>Upplýsingastjórnun afurða &gt; Algengt &gt; Losaðar afurðir</strong>.</span><span class="sxs-lookup"><span data-stu-id="84f4e-123">Click <strong>Product information management &gt; Common &gt; Released products</strong>.</span></span> <span data-ttu-id="84f4e-124">Á flipanum <strong>Upplýsingar um útgefna afurð **síðu, á **Almennt</strong> í flokknum <strong>Stjórnun</strong> skal smella á tengilinn <strong>Flokkur geymsluvíddar</strong>.</span><span class="sxs-lookup"><span data-stu-id="84f4e-124">On the <strong>Released product detail **page, on the **General</strong> tab, in the <strong>Administration</strong> group, click the <strong>Storage dimension group</strong> link.</span></span> <span data-ttu-id="84f4e-125">Á síðunni <strong>Geymsluvíddarflokkur</strong> skal velja <strong>Þekjuáætlun eftir vídd</strong> til að stofna þekjustillingar fyrir vídd í geymsluvíddarflokknum.</span><span class="sxs-lookup"><span data-stu-id="84f4e-125">On the <strong>Storage dimension group</strong> page, select the <strong>Coverage plan by dimension</strong> field to create the coverage settings for a dimension in the storage dimension group.</span></span> <span data-ttu-id="84f4e-126">Allar afurðavíddir, eins og skilgreining, litur, stærð, stíll, verða að hafa reitinn <strong>Þekjuáætlun eftir vídd</strong> valinn.</span><span class="sxs-lookup"><span data-stu-id="84f4e-126">All product dimensions, such as configuration, color, size, style, must have the <strong>Coverage plan by dimension</strong> field selected.</span></span>



<a name="see-also"></a><span data-ttu-id="84f4e-127">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="84f4e-127">See also</span></span>
--------

[<span data-ttu-id="84f4e-128">Aðaláætlanir</span><span class="sxs-lookup"><span data-stu-id="84f4e-128">Master plans</span></span>](master-plans.md)




