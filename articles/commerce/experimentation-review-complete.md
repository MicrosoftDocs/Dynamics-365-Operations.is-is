---
title: Kynna afbrigði og ljúka tilraun
description: Þetta efnisatriði lýsir því hvernig á að koma vel heppnuðu afbrigði á framfæri og ljúka tilraun í Dynamics 365 Commerce.
author: sushma-rao
manager: AnnBe
ms.date: 09/15/2020
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
ms.openlocfilehash: 2e011f10e908d6a2efe2e928fc5e0abc7659cb8b
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930216"
---
# <a name="promote-a-variation-and-complete-an-experiment"></a><span data-ttu-id="ca58d-103">Kynna afbrigði og ljúka tilraun</span><span class="sxs-lookup"><span data-stu-id="ca58d-103">Promote a variation and complete an experiment</span></span>

<span data-ttu-id="ca58d-104">Þetta efnisatriði lýsir því hvernig á að koma afbrigðum á framfæri sem skiluðu bestum árangri í tilrauninni og hvernig á að ljúka við tilraunina.</span><span class="sxs-lookup"><span data-stu-id="ca58d-104">This topic describes how to promote the variation that produced the best results in your experiment, and how to complete the experiment.</span></span> <span data-ttu-id="ca58d-105">Eftirfarandi skýringarmynd sýnir öll skrefin sem taka þátt í uppsetningu og vinnslu á tilraun á vefsvæði rafrænna viðskipta í Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ca58d-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="ca58d-106">Önnur skref eru afgreidd í aðskildum efnisatriðum.</span><span class="sxs-lookup"><span data-stu-id="ca58d-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="ca58d-107">[ ![Ferli tilraunanotanda - Yfirfara og ljúka](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="ca58d-107">[ ![Experimentation user journey - Review & Complete](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)</span></span>

<span data-ttu-id="ca58d-108">Þegar þú hefur [keyrt tilraunina þína](experimentation-run-monitor.md) og safnað fullnægjandi gögnum til að ákveða hvaða afbrigði þú vilt nota á virka vefsvæðinu þínu, munt þú koma afbrigðinu á framfæri og ljúka við tilraunina.</span><span class="sxs-lookup"><span data-stu-id="ca58d-108">After you've [run your experiment](experimentation-run-monitor.md) and collected sufficient data to determine which variation you want to use on your live site, you'll promote the variation and end the experiment.</span></span>

## <a name="promote-a-variation"></a><span data-ttu-id="ca58d-109">Koma afbrigði á framfæri</span><span class="sxs-lookup"><span data-stu-id="ca58d-109">Promote a variation</span></span>
<span data-ttu-id="ca58d-110">Notið gögn og greiningar sem tengjast tilrauninni í þjónustu þriðja aðila til að ákveða hvaða afbrigði skilaði bestum árangri.</span><span class="sxs-lookup"><span data-stu-id="ca58d-110">Use the data and analytics related to the experiment in the third-party service to decide which variation produced the best results.</span></span> <span data-ttu-id="ca58d-111">Til að skipta út núverandi efni á virka vefsvæðinu fyrir afbrigðið sem stóð upp úr þannig að það sé tiltækt öllum notendum vefsvæðisins, skal gera eftirfarandi.</span><span class="sxs-lookup"><span data-stu-id="ca58d-111">To replace the current content on the live site with the winning variation so that it's available to all users of your website, do the following.</span></span> 

1. <span data-ttu-id="ca58d-112">Farið í flipann **Tilraunir** í vefsmiðnum og veljið tilraunina.</span><span class="sxs-lookup"><span data-stu-id="ca58d-112">Go to the **Experiments** tab in site builder and select the experiment.</span></span>
1. <span data-ttu-id="ca58d-113">Veljið **Ljúka tilraun** á efstu stikunni.</span><span class="sxs-lookup"><span data-stu-id="ca58d-113">Select **Complete experiment** on the top bar.</span></span>
1. <span data-ttu-id="ca58d-114">Í svarglugganum **Ljúka tilrauninni** skal velja **Yfirfara gögn tilraunar**.</span><span class="sxs-lookup"><span data-stu-id="ca58d-114">In the **Complete the experiment** dialog menu, select **Review the experiment data**.</span></span> <span data-ttu-id="ca58d-115">Þjónusta þriðja aðila opnast þar sem hægt er að sannprófa mælingarnar og ákveða hvaða afbrigði skilaði bestum árangri.</span><span class="sxs-lookup"><span data-stu-id="ca58d-115">The third-party service opens where you can validate the metrics and determine which variation performed the best.</span></span>
1. <span data-ttu-id="ca58d-116">Í svarglugganum **Ljúka tilrauninni** í vefsmiðnum, skal velja afbrigðið sem stóð upp úr og velja síðan **Næst**.</span><span class="sxs-lookup"><span data-stu-id="ca58d-116">In the **Complete the experiment** dialog menu in site builder, select the winning variation and then select **Next**.</span></span>
1. <span data-ttu-id="ca58d-117">Opnaðu þjónustu þriðja aðila og stöðvaðu tilraunina.</span><span class="sxs-lookup"><span data-stu-id="ca58d-117">Open the third-party service and stop the experiment.</span></span>
1. <span data-ttu-id="ca58d-118">Í vefsmiðnum skal velja **Ljúka** til að skrifa yfir upprunalegu virku síðuna og birta afbrigðið sem stóð upp úr þannig að hann sé aðgengilegt öllum notendum vefsvæðisins.</span><span class="sxs-lookup"><span data-stu-id="ca58d-118">In site builder, select **Complete** to overwrite the original live page and publish the winning variation so that it's available to all users of your website.</span></span> 

> [!NOTE]
> <span data-ttu-id="ca58d-119">Ef valið er að halda núverandi virkri síðu og birta ekki afbrigði skal velja **Endurbirta upprunalegu síðuna**.</span><span class="sxs-lookup"><span data-stu-id="ca58d-119">If you choose to keep the current live page and not publish a variation, select **Republish the original page**.</span></span>

## <a name="delete-your-experiment"></a><span data-ttu-id="ca58d-120">Eyða tilraun</span><span class="sxs-lookup"><span data-stu-id="ca58d-120">Delete your experiment</span></span>
<span data-ttu-id="ca58d-121">Þess er ekki krafist að fullbúinni tilraun sé eytt í Commerce, en það má samt sem áður eyða henni til að spara pláss eða hreinsa vinnusvæðið.</span><span class="sxs-lookup"><span data-stu-id="ca58d-121">While it's not required that you delete a completed experiment in Commerce, you may choose to delete it to save space or clean up your workspace.</span></span> <span data-ttu-id="ca58d-122">Til að eyða tilraun skaltu gera eftirfarandi.</span><span class="sxs-lookup"><span data-stu-id="ca58d-122">To delete an experiment, do the following.</span></span>

1. <span data-ttu-id="ca58d-123">Farið í flipann **Tilraunir** í vefsmiðnum og veljið tilraunina.</span><span class="sxs-lookup"><span data-stu-id="ca58d-123">Go to the **Experiments** tab in site builder and select the experiment.</span></span> 
    > [!NOTE]
    > <span data-ttu-id="ca58d-124">Ef tilraunin er enn virk skal stöðva hana í þjónustu þriðja aðilans áður en haldið er áfram.</span><span class="sxs-lookup"><span data-stu-id="ca58d-124">If the experiment is still active, stop the experiment in the third-party service before proceeding.</span></span>
1. <span data-ttu-id="ca58d-125">Veljið **Taka úr birtingu** í skipanastikunni til að fjarlægja efni afbrigðisins af virka vefsvæðinu.</span><span class="sxs-lookup"><span data-stu-id="ca58d-125">Select **Unpublish** in the command bar to remove the variation content from the live site.</span></span>
1. <span data-ttu-id="ca58d-126">Veljið **Eyða** í skipanastikunni til að eyða tilrauninni.</span><span class="sxs-lookup"><span data-stu-id="ca58d-126">Select **Delete** in the command bar to delete the experiment.</span></span>

## <a name="previous-step"></a><span data-ttu-id="ca58d-127">Fyrra skref</span><span class="sxs-lookup"><span data-stu-id="ca58d-127">Previous step</span></span>
[<span data-ttu-id="ca58d-128">Keyra og fylgjast með tilraun</span><span class="sxs-lookup"><span data-stu-id="ca58d-128">Run and monitor an experiment</span></span>](experimentation-run-monitor.md)
