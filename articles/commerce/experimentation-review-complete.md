---
title: Kynna afbrigði og ljúka tilraun
description: Þetta efnisatriði lýsir því hvernig á að koma vel heppnuðu afbrigði á framfæri og ljúka tilraun í Dynamics 365 Commerce.
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 25cccbeae5c263a3032eeebf2fc5335e22c1415a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009926"
---
# <a name="promote-a-variation-and-complete-an-experiment"></a><span data-ttu-id="13c29-103">Kynna afbrigði og ljúka tilraun</span><span class="sxs-lookup"><span data-stu-id="13c29-103">Promote a variation and complete an experiment</span></span>

<span data-ttu-id="13c29-104">Þetta efnisatriði lýsir því hvernig á að koma afbrigðum á framfæri sem skiluðu bestum árangri í tilrauninni og hvernig á að ljúka við tilraunina.</span><span class="sxs-lookup"><span data-stu-id="13c29-104">This topic describes how to promote the variation that produced the best results in your experiment, and how to complete the experiment.</span></span> <span data-ttu-id="13c29-105">Eftirfarandi skýringarmynd sýnir öll skrefin sem taka þátt í uppsetningu og vinnslu á tilraun á vefsvæði rafrænna viðskipta í Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="13c29-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="13c29-106">Önnur skref eru afgreidd í aðskildum efnisatriðum.</span><span class="sxs-lookup"><span data-stu-id="13c29-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="13c29-107">[ ![Ferli tilraunanotanda - Yfirfara og ljúka](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="13c29-107">[ ![Experimentation user journey - Review & Complete](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)</span></span>

<span data-ttu-id="13c29-108">Þegar þú hefur [keyrt tilraunina þína](experimentation-run-monitor.md) og safnað fullnægjandi gögnum til að ákveða hvaða afbrigði þú vilt nota á virka vefsvæðinu þínu, munt þú koma afbrigðinu á framfæri og ljúka við tilraunina.</span><span class="sxs-lookup"><span data-stu-id="13c29-108">After you've [run your experiment](experimentation-run-monitor.md) and collected sufficient data to determine which variation you want to use on your live site, you'll promote the variation and end the experiment.</span></span>

## <a name="promote-a-variation"></a><span data-ttu-id="13c29-109">Koma afbrigði á framfæri</span><span class="sxs-lookup"><span data-stu-id="13c29-109">Promote a variation</span></span>
<span data-ttu-id="13c29-110">Notið gögn og greiningar sem tengjast tilrauninni í þjónustu þriðja aðila til að ákveða hvaða afbrigði skilaði bestum árangri.</span><span class="sxs-lookup"><span data-stu-id="13c29-110">Use the data and analytics related to the experiment in the third-party service to decide which variation produced the best results.</span></span> <span data-ttu-id="13c29-111">Svo er hægt að kynna það með því að skipta út núverandi efni á virka vefsvæðinu fyrir afbrigðið sem stóð upp úr þannig að það sé tiltækt öllum notendum vefsvæðisins.</span><span class="sxs-lookup"><span data-stu-id="13c29-111">You can then promote it by replacing the current content on the live site with the winning variation so that it's available to all users of your website.</span></span>

<span data-ttu-id="13c29-112">Til að stuðla fá bestan árangur skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="13c29-112">To promote the winning variation, follow these steps.</span></span> 

1. <span data-ttu-id="13c29-113">Í vefsmið Commerce skal velja **Tilraunir** á vinstra yfirlitssvæðinu og síðan velja tilraunina.</span><span class="sxs-lookup"><span data-stu-id="13c29-113">In Commerce site builder, select **Experiments** in the left navigation pane, and then select the experiment.</span></span>
1. <span data-ttu-id="13c29-114">Á skipanastikunni skal velja **Ljúka tilraun**.</span><span class="sxs-lookup"><span data-stu-id="13c29-114">On the command bar, select **Complete experiment**.</span></span>
1. <span data-ttu-id="13c29-115">Í svarreitnum **Ljúka tilrauninni** skal velja **Yfirfara gögn tilraunar**.</span><span class="sxs-lookup"><span data-stu-id="13c29-115">In the **Complete the experiment** dialog box, select **Review the experiment data**.</span></span> <span data-ttu-id="13c29-116">Þjónusta þriðja aðila opnast þar sem hægt er að sannprófa mælingarnar og ákveða hvaða afbrigði skilaði bestum árangri.</span><span class="sxs-lookup"><span data-stu-id="13c29-116">The third-party service opens where you can validate the metrics and determine which variation performed the best.</span></span>
1. <span data-ttu-id="13c29-117">Í svarglugganum **Ljúka tilrauninni** skal velja afbrigðið sem stóð upp úr og velja síðan **Næst**.</span><span class="sxs-lookup"><span data-stu-id="13c29-117">In the **Complete the experiment** dialog box, select the winning variation, and then select **Next**.</span></span>
1. <span data-ttu-id="13c29-118">Opnaðu þjónustu þriðja aðila og stöðvaðu tilraunina.</span><span class="sxs-lookup"><span data-stu-id="13c29-118">Open the third-party service and stop the experiment.</span></span>
1. <span data-ttu-id="13c29-119">Í vefsmiðnum skal velja **Ljúka** til að skrifa yfir upprunalegu virku síðuna og birta afbrigðið sem stóð upp úr þannig að hann sé aðgengilegt öllum notendum vefsvæðisins.</span><span class="sxs-lookup"><span data-stu-id="13c29-119">In site builder, select **Complete** to overwrite the original live page and publish the winning variation so that it's available to all users of your website.</span></span> 

> [!NOTE]
> <span data-ttu-id="13c29-120">Ef valið er að halda núverandi virkri síðu og birta ekki afbrigði skal velja **Endurbirta upprunalegu síðuna**.</span><span class="sxs-lookup"><span data-stu-id="13c29-120">If you choose to keep the current live page and not publish a variation, select **Republish the original page**.</span></span>

## <a name="delete-your-experiment"></a><span data-ttu-id="13c29-121">Eyða tilraun</span><span class="sxs-lookup"><span data-stu-id="13c29-121">Delete your experiment</span></span>
<span data-ttu-id="13c29-122">Þess er ekki krafist að fullbúinni tilraun sé eytt í Commerce, en það má samt sem áður eyða henni til að spara pláss eða hreinsa vinnusvæðið.</span><span class="sxs-lookup"><span data-stu-id="13c29-122">While it's not required that you delete a completed experiment in Commerce, you may choose to delete it to save space or clean up your workspace.</span></span> 

<span data-ttu-id="13c29-123">Til að eyða tilraun vefsmið Commerce skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="13c29-123">To delete an experiment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="13c29-124">Veljið **Tilraunir** í vinstri yfirlitssvæði og veljið svo tilraunina.</span><span class="sxs-lookup"><span data-stu-id="13c29-124">Select **Experiments** in the left navigation pane, and then select the experiment.</span></span> 
    > [!NOTE]
    > <span data-ttu-id="13c29-125">Ef tilraunin er enn virk skal stöðva hana í þjónustu þriðja aðilans áður en haldið er áfram.</span><span class="sxs-lookup"><span data-stu-id="13c29-125">If the experiment is still active, stop the experiment in the third-party service before proceeding.</span></span>
1. <span data-ttu-id="13c29-126">Veljið **Taka úr birtingu** í skipanastikunni til að fjarlægja efni afbrigðisins af virka vefsvæðinu.</span><span class="sxs-lookup"><span data-stu-id="13c29-126">On the command bar, select **Unpublish**  to remove the variation content from the live site.</span></span>
1. <span data-ttu-id="13c29-127">Veljið **Eyða** til að eyða tilrauninni.</span><span class="sxs-lookup"><span data-stu-id="13c29-127">Select **Delete** to delete the experiment.</span></span>

## <a name="previous-step"></a><span data-ttu-id="13c29-128">Fyrra skref</span><span class="sxs-lookup"><span data-stu-id="13c29-128">Previous step</span></span>
[<span data-ttu-id="13c29-129">Keyra og fylgjast með tilraun</span><span class="sxs-lookup"><span data-stu-id="13c29-129">Run and monitor an experiment</span></span>](experimentation-run-monitor.md)
