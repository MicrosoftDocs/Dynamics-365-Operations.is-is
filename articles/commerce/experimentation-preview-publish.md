---
title: Forskoða og birta tilraun
description: Þetta efnisatriði lýsir því hvernig á að forskoða og birta tilraun úr Dynamics 365 Commerce.
author: sushma-rao
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 91e2e4840a2d53f195d881279050b6415d48b070
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930221"
---
# <a name="preview-and-publish-an-experiment"></a><span data-ttu-id="d021f-103">Forskoða og birta tilraun</span><span class="sxs-lookup"><span data-stu-id="d021f-103">Preview and publish an experiment</span></span>

<span data-ttu-id="d021f-104">Þetta efnisatriði lýsir því hvernig á að forskoða og birta tilraunir þínar í Dynamics 365 Commerce eftir að þú hefur [tengt tilraunina þína og breytt afbrigðunum](experimentation-connect-edit.md).</span><span class="sxs-lookup"><span data-stu-id="d021f-104">This topic describes how to preview and publish your experiment in Dynamics 365 Commerce after you've [connected your experiment and edited your variations](experimentation-connect-edit.md).</span></span> <span data-ttu-id="d021f-105">Eftirfarandi skýringarmynd sýnir öll skrefin sem taka þátt í uppsetningu og vinnslu á tilraun á vefsvæði rafrænna viðskipta í Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d021f-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="d021f-106">Önnur skref eru afgreidd í aðskildum efnisatriðum.</span><span class="sxs-lookup"><span data-stu-id="d021f-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="d021f-107">[ ![Ferli tilraunanotanda - Forskoða og birta](./media/experimentation_preview_publish.svg) ](./media/experimentation_preview_publish.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="d021f-107">[ ![Experimentation user journey - Preview & Publish](./media/experimentation_preview_publish.svg) ](./media/experimentation_preview_publish.svg#lightbox)</span></span>

## <a name="preview-your-experiment-variations"></a><span data-ttu-id="d021f-108">Skoða afbrigði tilrauna</span><span class="sxs-lookup"><span data-stu-id="d021f-108">Preview your experiment variations</span></span>
<span data-ttu-id="d021f-109">Hægt er að skoða afbrigðin og halda áfram að breyta þeim þar til þau líta út eins og til er ætlast.</span><span class="sxs-lookup"><span data-stu-id="d021f-109">You can preview your variations and continue editing them until they look the way you want them to.</span></span>

1. <span data-ttu-id="d021f-110">Í vefsmiðnum skal nota fellivalmynd afbrigða fyrir neðan skipanastikuna til að velja efnið sem á að forskoða.</span><span class="sxs-lookup"><span data-stu-id="d021f-110">In site builder, use the variations drop-down menu below the command bar to select the content you want to preview.</span></span> 
1. <span data-ttu-id="d021f-111">Veljið **Forskoða** í efstu stikunni.</span><span class="sxs-lookup"><span data-stu-id="d021f-111">Select **Preview** in the top bar.</span></span> <span data-ttu-id="d021f-112">Forskoðun á því hvernig efnið mun líta út þegar það verður birt.</span><span class="sxs-lookup"><span data-stu-id="d021f-112">A preview of what the content will look like when it's published is displayed.</span></span>
1. <span data-ttu-id="d021f-113">Til að forskoða annað afbrigði skal velja það úr fellilista afbrigða og velja **Forskoða** aftur.</span><span class="sxs-lookup"><span data-stu-id="d021f-113">To preview a different variation, select it from the variation drop-down and select **Preview** again.</span></span>

## <a name="publish-your-experiment"></a><span data-ttu-id="d021f-114">Birta tilraun</span><span class="sxs-lookup"><span data-stu-id="d021f-114">Publish your experiment</span></span>
<span data-ttu-id="d021f-115">Ef ekki er notaður birtingarhópur til að tímasetja hvenær tilraunin á að fara á netið og ætlunin er að birta hana strax, skal velja **Birta** í skipanastikunni.</span><span class="sxs-lookup"><span data-stu-id="d021f-115">If you aren't using a publish group to schedule when your experiment goes live and you want to publish immediately, select **Publish** in the command bar.</span></span> <span data-ttu-id="d021f-116">Öll afbrigði sem tilheyra tilrauninni verða birt.</span><span class="sxs-lookup"><span data-stu-id="d021f-116">All variations that belong to the experiment will be published.</span></span>
    
> [!IMPORTANT]
> <span data-ttu-id="d021f-117">Ef síðan er með óbirta vefslóð þarf fyrst að birta vefslóðina, annars verður hún ekki sýnileg notendum vefsvæðisins.</span><span class="sxs-lookup"><span data-stu-id="d021f-117">If the page has an unpublished URL, you must first publish the URL or it won't be visible to your website users.</span></span> <span data-ttu-id="d021f-118">Frekari upplýsingar er að finna í [Vista, forskoða og birta síðu](save-preview-publish-page.md).</span><span class="sxs-lookup"><span data-stu-id="d021f-118">For details, see [Save, preview, and publish a page](save-preview-publish-page.md).</span></span>
    
### <a name="use-publish-groups-to-schedule-when-your-experiment-goes-live"></a><span data-ttu-id="d021f-119">Nota birtingarhópa til að tímasetja hvenær tilraunin á að fara á netið</span><span class="sxs-lookup"><span data-stu-id="d021f-119">Use publish groups to schedule when your experiment goes live</span></span>
<span data-ttu-id="d021f-120">Hægt er að tímasetja afbrigði til birtingar sem búin eru til í vefsmiðnum með því að nota birtingarhóp.</span><span class="sxs-lookup"><span data-stu-id="d021f-120">Variations created in site builder can be scheduled for publishing by using a publish group.</span></span> <span data-ttu-id="d021f-121">Innan birtingarhóps er hægt að tengja síðu eða brot við tilraunina með því að fara í flipann **Tilraunir** eða **Síður** eða **Brot**. Frekari upplýsingar er að finna í efnisatriðinu [Tengja tilraun og breyta afbrigðum](experimentation-connect-edit.md).</span><span class="sxs-lookup"><span data-stu-id="d021f-121">Within a publish group, you can connect a page or fragment to your experiment by going to the **Experiments** tab or the **Pages** or **Fragments** tab. For more information, see [Connect an experiment and edit variations](experimentation-connect-edit.md) topic.</span></span> <span data-ttu-id="d021f-122">Upplýsingar um birtingarhópa er að finna í [Vinna með birtingarhópa](publish-groups.md).</span><span class="sxs-lookup"><span data-stu-id="d021f-122">For information about publish groups, see [Work with publish groups](publish-groups.md).</span></span>

<span data-ttu-id="d021f-123">Þegar birtingarhópar eru notaður með tilraunum, þarf að huga að nokkrum mikilvægum atriðum.</span><span class="sxs-lookup"><span data-stu-id="d021f-123">When using publish groups with experiments, there are some important considerations to be aware of.</span></span>
- <span data-ttu-id="d021f-124">Þegar síðu eða broti, sem er með tilraun í gangi, er bætt við birtingarhóp, verður tilraunin fjarlægð af síðunni eða brotinu í birtingarhópnum.</span><span class="sxs-lookup"><span data-stu-id="d021f-124">When you add a page or fragment that has an experiment running on it to a publish group, the experiment will be removed from the page or fragment in the publish group.</span></span>
- <span data-ttu-id="d021f-125">Tilraunir sem eru tengdar við síður á virku vefsvæði eru ekki í boði fyrir síður innan birtingarhópa og öfugt.</span><span class="sxs-lookup"><span data-stu-id="d021f-125">Experiments that are connected to pages in a live site aren't available to pages within publish groups and vice-versa.</span></span> <span data-ttu-id="d021f-126">Á sama hátt verða síður sem eru með tilraunir í gangi á virku vefsvæði ekki í boði fyrir aðrar tilraunir í birtingarhópnum og öfugt.</span><span class="sxs-lookup"><span data-stu-id="d021f-126">Similarly, pages that have experiments running on them in a live site aren't available to other experiments in publish groups and vice versa.</span></span>
- <span data-ttu-id="d021f-127">Þegar birtingarhópur er birtur eða tímasettur, verður allt efni í birtingarhópnum birt, óháð því hvort tilraun er tengd við birtingarhópinn.</span><span class="sxs-lookup"><span data-stu-id="d021f-127">When you publish or schedule a publish group, all content in the publish group is published, regardless of whether there's an experiment associated with the publish group.</span></span>
- <span data-ttu-id="d021f-128">Vegna þess að birtingarhópur verður áfram til eftir að hann hefur verið birtur á virku vefsvæði, halda tilraunir í birtingarhópnum áfram að vera til.</span><span class="sxs-lookup"><span data-stu-id="d021f-128">Because a publish group continues to persist after it's been published to a live site, experiments in the publish group will also persist.</span></span> <span data-ttu-id="d021f-129">Þess vegna er ekki hægt að tengja aðrar tilraunir við sömu síðu eða brot.</span><span class="sxs-lookup"><span data-stu-id="d021f-129">Therefore, you won't be able to associate other experiments with the same page or fragment.</span></span> <span data-ttu-id="d021f-130">Til að koma í veg fyrir þessa takmörkun skal eyða öllum birtingarhópum með viðvarandi tilraunum.</span><span class="sxs-lookup"><span data-stu-id="d021f-130">To avoid this limitation, delete any publish groups with persisting experiments.</span></span> <span data-ttu-id="d021f-131">Á sama hátt, ef eyða á tilraun á virku svæði sem einnig er til í birtingarhóp, skal eyða henni úr birtingarhópnum fyrst.</span><span class="sxs-lookup"><span data-stu-id="d021f-131">Similarly, if you want to delete an experiment in a live site that also exists in a publish group, delete it from the publish group first.</span></span>

## <a name="previous-step"></a><span data-ttu-id="d021f-132">Fyrra skref</span><span class="sxs-lookup"><span data-stu-id="d021f-132">Previous step</span></span>
[<span data-ttu-id="d021f-133">Tengja og breyta tilraun</span><span class="sxs-lookup"><span data-stu-id="d021f-133">Connect and edit an experiment</span></span>](experimentation-connect-edit.md)

## <a name="next-step"></a><span data-ttu-id="d021f-134">Næsta skref</span><span class="sxs-lookup"><span data-stu-id="d021f-134">Next step</span></span>
[<span data-ttu-id="d021f-135">Keyra og fylgjast með tilraun</span><span class="sxs-lookup"><span data-stu-id="d021f-135">Run and monitor an experiment</span></span>](experimentation-run-monitor.md)