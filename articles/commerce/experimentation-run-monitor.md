---
title: Keyra og fylgjast með tilraun
description: Þetta efnisatriði lýsir því hvernig á að keyra og fylgjast með tilraun í þjónustu þriðja aðila. Þar er einnig lýst því hvernig á að gera breytingar á afbrigðum eftir að tilraunin hófst.
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
ms.openlocfilehash: 956a9168ed7bf9282d9eeec39587d8e1f2d1856c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5224883"
---
# <a name="run-and-monitor-an-experiment"></a><span data-ttu-id="feccb-104">Keyra og fylgjast með tilraun</span><span class="sxs-lookup"><span data-stu-id="feccb-104">Run and monitor an experiment</span></span>

<span data-ttu-id="feccb-105">Þetta efnisatriði lýsir því hvernig á að keyra og fylgjast með tilraun í forriti þriðja aðila og breyta afbrigðum eftir því sem þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="feccb-105">This topic describes how to run and monitor your experiment in a third-party app, and change variations if needed.</span></span> <span data-ttu-id="feccb-106">Áður en þú klárar skrefin í þessu efnisatriði þarftu fyrst að [birta](experimentation-preview-publish.md) tilraunina þína í Commerce.</span><span class="sxs-lookup"><span data-stu-id="feccb-106">Before you complete the steps in this topic, you'll first need to [publish](experimentation-preview-publish.md) your experiment in Commerce.</span></span> 

<span data-ttu-id="feccb-107">Eftirfarandi skýringarmynd sýnir öll skrefin sem taka þátt í uppsetningu og vinnslu á tilraun á vefsvæði rafrænna viðskipta í Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="feccb-107">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="feccb-108">Önnur skref eru afgreidd í aðskildum efnisatriðum.</span><span class="sxs-lookup"><span data-stu-id="feccb-108">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="feccb-109">[ ![Ferli tilraunanotanda - Keyra og fylgjast með](./media/experimentation_run_monitor.svg) ](./media/experimentation_run_monitor.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="feccb-109">[ ![Experimentation user journey - Run & Monitor](./media/experimentation_run_monitor.svg) ](./media/experimentation_run_monitor.svg#lightbox)</span></span>

<span data-ttu-id="feccb-110">Þegar afbrigðin hafa verið birt þarf að fara í gegnum öll skrefin sem þú þarft að gera í Commerce til að keyra tilraunina þína.</span><span class="sxs-lookup"><span data-stu-id="feccb-110">After you publish your variations, all of the steps you need to do in Commerce to run your experiment are complete.</span></span> <span data-ttu-id="feccb-111">Næsta skref er að ákvarða hvaða afbrigði eru sýnd hverjum notanda þegar þeir óska eftir síðu.</span><span class="sxs-lookup"><span data-stu-id="feccb-111">The next step is determining which variation to show to each user when they request a page.</span></span> <span data-ttu-id="feccb-112">Þjónusta þriðja aðila tekur þá ákvörðun en fyrst þarf að virkja tilraunina innan þjónustunnar.</span><span class="sxs-lookup"><span data-stu-id="feccb-112">The third-party service makes that determination, but first you have to activate the experiment within the service.</span></span> <span data-ttu-id="feccb-113">Þar sem skrefin til að virkja tilraun eru breytileg frá þjónustu til þjónustu þarf að fylgja leiðbeiningunum sem eru innifaldar í þjónustunni eða veitunni.</span><span class="sxs-lookup"><span data-stu-id="feccb-113">Since the steps for activating an experiment vary from service to service, you'll need to follow the instructions included with your service or provider.</span></span> <span data-ttu-id="feccb-114">Ef tilraunin er ekki virkjuð munu notendur aðeins sjá sjálfgefna útgáfu síðunnar (engin afbrigði verða birt).</span><span class="sxs-lookup"><span data-stu-id="feccb-114">If the experiment is not activated, users will only see the default version of the page (no variations will be displayed).</span></span>

<span data-ttu-id="feccb-115">Þú þarft að halda tilrauninni nógu lengi í gangi til að safna gögnum fyrir tölfræðilega gildar niðurstöður.</span><span class="sxs-lookup"><span data-stu-id="feccb-115">You'll need to keep the experiment running long enough to gather data for statistically valid results.</span></span> <span data-ttu-id="feccb-116">Notið þjónustu þriðja aðila til að fylgjast með gögnum sem tengjast tilraunum og greiningu á meðan tilraunin er í gangi.</span><span class="sxs-lookup"><span data-stu-id="feccb-116">Use the third-party service to monitor the experiment-related data and analytics while the experiment is running.</span></span>

## <a name="adjust-your-variations"></a><span data-ttu-id="feccb-117">Leiðrétta afbrigði</span><span class="sxs-lookup"><span data-stu-id="feccb-117">Adjust your variations</span></span>
<span data-ttu-id="feccb-118">Ef þú þarft að breyta afbrigðunum af einhverjum ástæðum skaltu fylgja skrefunum hér að neðan.</span><span class="sxs-lookup"><span data-stu-id="feccb-118">If for any reason you need to modify your variations, follow the steps below.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="feccb-119">Ef gerðar eru breytingar á virkri tilraun í Commerce eða þjónustu þriðja aðila getur það haft umtalsverð áhrif á niðurstöðurnar.</span><span class="sxs-lookup"><span data-stu-id="feccb-119">If you make changes to a live experiment in Commerce or the third-party service, your results may be significantly impacted.</span></span> <span data-ttu-id="feccb-120">Íhugið að láta tilraunina hafa sinn gang og búa síðan til nýja tilraun fyrir stórar breytingar.</span><span class="sxs-lookup"><span data-stu-id="feccb-120">Consider letting the experiment run its course and then creating a new experiment for major changes.</span></span>

1. <span data-ttu-id="feccb-121">Í vefsmið Commerce skal velja **Tilraunir** á vinstra yfirlitssvæðinu og síðan velja tilraunina.</span><span class="sxs-lookup"><span data-stu-id="feccb-121">In Commerce site builder, select **Experiments** in the left navigation pane, and then select the experiment.</span></span> 
1. <span data-ttu-id="feccb-122">Veljið afbrigðið sem á að uppfæra úr fellivalmyndinni.</span><span class="sxs-lookup"><span data-stu-id="feccb-122">Select the variation you want to update from the drop-down menu.</span></span>
1. <span data-ttu-id="feccb-123">Gerið nauðsynlegar breytingar, forskoðið og birtið síðan afbrigðin.</span><span class="sxs-lookup"><span data-stu-id="feccb-123">Make any needed changes, and then preview and publish the variations.</span></span> <span data-ttu-id="feccb-124">Frekari upplýsingar er að finna í [Forskoða og birta tilraun](experimentation-preview-publish.md).</span><span class="sxs-lookup"><span data-stu-id="feccb-124">For more information, see [Preview and publish an experiment](experimentation-preview-publish.md).</span></span>
1. <span data-ttu-id="feccb-125">Farið í þjónustu þriðja aðila til að gera breytingar á uppsetningu tilraunar.</span><span class="sxs-lookup"><span data-stu-id="feccb-125">Go to the third-party service to make any experiment setup-related changes.</span></span>
    
## <a name="previous-step"></a><span data-ttu-id="feccb-126">Fyrra skref</span><span class="sxs-lookup"><span data-stu-id="feccb-126">Previous step</span></span>
[<span data-ttu-id="feccb-127">Forskoða og birta tilraun</span><span class="sxs-lookup"><span data-stu-id="feccb-127">Preview and publish an experiment</span></span>](experimentation-preview-publish.md)

## <a name="next-step"></a><span data-ttu-id="feccb-128">Næsta skref</span><span class="sxs-lookup"><span data-stu-id="feccb-128">Next step</span></span>
[<span data-ttu-id="feccb-129">Kynna afbrigði og ljúka tilraun</span><span class="sxs-lookup"><span data-stu-id="feccb-129">Promote a variation and complete an experiment</span></span>](experimentation-review-complete.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]