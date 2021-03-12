---
title: Hlaða sniðmáti hleðslu
description: Þetta efnisatriði útskýrir hvernig á að vinna með vinnusvæði hleðsluáætlunar.
author: Henrikan
manager: ''
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSLoadBuildWorkbench,TMSLoadBuildTemplateCreate,TMSLoadBuildStrategy,TMSLoadBuildTemplateApply
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: d1ed91adba5c7accf9a18d7a754d33b2b35b848f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974227"
---
# <a name="load-building-workbench"></a><span data-ttu-id="24117-103">Hlaða sniðmáti hleðslu</span><span class="sxs-lookup"><span data-stu-id="24117-103">Load building workbench</span></span>

<span data-ttu-id="24117-104">Vinnusvæði hleðslunnar er hægt að nota flutningshleðsluáætlanir þegar búið er að búa til hleðslu.</span><span class="sxs-lookup"><span data-stu-id="24117-104">The load building workbench lets you apply load building strategies when you create loads.</span></span>

## <a name="create-a-load-building-strategy"></a><span data-ttu-id="24117-105">Stofna hleðsluáætlunarstefnu</span><span class="sxs-lookup"><span data-stu-id="24117-105">Create a load building strategy</span></span>

<span data-ttu-id="24117-106">Hleðsluáætlanir eru notaðar til að byggja hleðslur sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="24117-106">You use load building strategies to automatically build loads.</span></span> <span data-ttu-id="24117-107">Þessi eiginleiki getur verið gagnlegur við eftirfarandi aðstæður:</span><span class="sxs-lookup"><span data-stu-id="24117-107">This capability can be beneficial in the following situations:</span></span>

- <span data-ttu-id="24117-108">Ef þú sendir reglulega tiltekið safn af afurðum, spara hleðsluáætlanir tíma, því að ekki þarf að búa til sömu hleðsluna í hvert skipti.</span><span class="sxs-lookup"><span data-stu-id="24117-108">If you regularly ship a specific set of products, load strategies help save time, because you don't have to build the same load every time.</span></span>
- <span data-ttu-id="24117-109">Ef ætlunin er að forðast hálffullar hleðslur til að hámarka skilvirkni, geta hleðsluáætlanir hjálpað til við að fylla hverja hleðslu eins og mögulegt er.</span><span class="sxs-lookup"><span data-stu-id="24117-109">If you want to avoid half-full loads to maximize efficiency, load strategies can help fill each load as much as possible.</span></span>

<span data-ttu-id="24117-110">Flutningshleðsluáætlun sem kallast `TMSLoadBuildingVolumeStrategy` býður upp á hleðsluáætlun sem nefnist *Hleðsluáætlun byggð á rúmmáli*.</span><span class="sxs-lookup"><span data-stu-id="24117-110">A load building strategy class that is named `TMSLoadBuildingVolumeStrategy` provides a load building strategy that is named *Volume-based load building strategy*.</span></span> <span data-ttu-id="24117-111">Þessi aðferð gerir kleift að nota hámarks gildi sem eru tilgreind fyrir hæð og þyngd í hleðslusniðmátinu eða hnekkja stillingum með því að færa inn ný gildi.</span><span class="sxs-lookup"><span data-stu-id="24117-111">This strategy lets you use the maximum values that are specified for height and weight in the load template, or you can override the settings by entering new values.</span></span> <span data-ttu-id="24117-112">Þessi stefna er eina stefna sem er tilbúin til notkunar.</span><span class="sxs-lookup"><span data-stu-id="24117-112">This strategy is the only strategy that is included out of the box.</span></span> <span data-ttu-id="24117-113">(Hins vegar er hægt að hafa einhverjar sérsniðnar aðferðir.)</span><span class="sxs-lookup"><span data-stu-id="24117-113">(However, you might have some custom strategies.)</span></span>

<span data-ttu-id="24117-114">Til að nota þessa tilbúnu áætlun *Hleðsluáætlun byggð á magni* skal velja hana í reitnum **Hleðsluáætlun** á síðunni **Vinnusvæði hleðsluáætlunar** (**Flutningsstjórnun &gt; Áætlanagerð &gt; Vinnusvæði hleðsluáætlunar**).</span><span class="sxs-lookup"><span data-stu-id="24117-114">To use the out-of-box *Volume-based load building strategy* strategy, select it in the **Load building strategy** field on the **Load building workbench** page (**Transportation management &gt; Planning &gt; Load building workbench**).</span></span>

<span data-ttu-id="24117-115">Fylgið þessum skrefum til að búa til flutningshleðsluáætlanir.</span><span class="sxs-lookup"><span data-stu-id="24117-115">To create a load building strategy, follow these steps.</span></span>

1. <span data-ttu-id="24117-116">Farið í **-flutningsstjórnun &gt; Uppsetning &gt; Hleðsluáætlun &gt; Hleðsluáætlanir**.</span><span class="sxs-lookup"><span data-stu-id="24117-116">Go to **Transportation management &gt; Setup &gt; Load building &gt; Load building strategies**.</span></span>
1. <span data-ttu-id="24117-117">Á aðgerðasvæðinu skal velja **Mynda klasalista** til að ganga úr skugga um þú sért með nýjustu útgáfurnar af öllum aðgengilegum klösum.</span><span class="sxs-lookup"><span data-stu-id="24117-117">On the Action Pane, select **Generate class list** to make sure that you have the latest versions of all available classes.</span></span>
1. <span data-ttu-id="24117-118">Í aðgerðarúðunni velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="24117-118">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="24117-119">Færið inn einkvæmt heiti áætlunar, veljið klasa hleðsluáætlunar fyrir hana og færið inn lýsingu.</span><span class="sxs-lookup"><span data-stu-id="24117-119">Enter a unique name for the strategy, select the load building strategy class for it, and enter a description.</span></span>
1. <span data-ttu-id="24117-120">Í aðgerðarúðunni skal velja **Vista**.</span><span class="sxs-lookup"><span data-stu-id="24117-120">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="24117-121">Á aðgerðasvæðinu skal velja **Færibreytur**.</span><span class="sxs-lookup"><span data-stu-id="24117-121">On the Action Pane, select **Parameters**.</span></span>
1. <span data-ttu-id="24117-122">Á síðunni **Færibreytur fyrir hleðsluáætlun** skal velja **Rúmmálsgeta** og síðan í reitinn **Gildi** skal slá inn prósentu fyrir afkastagetu heildarrúmmáls hleðslunnar sem á að nota fyrir nýju hleðsluáætlunina.</span><span class="sxs-lookup"><span data-stu-id="24117-122">On the **Load building strategy parameters** page, select **Volume capacity** in the list, and then, in the **Value** field, enter the percentage of the load's total volume capacity that should be applied for the new load building strategy.</span></span>
1. <span data-ttu-id="24117-123">Veljið **Þyngdargeta** og síðan í reitinn **Gildi** skal slá inn prósentu fyrir afkastagetu heildarþyngdar hleðslunnar sem á að nota fyrir nýju hleðsluáætlunina.</span><span class="sxs-lookup"><span data-stu-id="24117-123">Select **Weight capacity** in the list, and then, in the **Value** field, enter the percentage of the load's total weight capacity that should be applied for the new load building strategy.</span></span>
1. <span data-ttu-id="24117-124">Lokið síðunni **Færibreytur fyrir hleðsluáætlun**.</span><span class="sxs-lookup"><span data-stu-id="24117-124">Close the **Load building strategy parameters** page.</span></span>
1. <span data-ttu-id="24117-125">Lokið síðunni **Hleðsluáætlanir**.</span><span class="sxs-lookup"><span data-stu-id="24117-125">Close the **Load building strategies** page.</span></span>

<span data-ttu-id="24117-126">Nú er hægt að úthluta hleðsluáætlanir fyrir hleðslusniðmát.</span><span class="sxs-lookup"><span data-stu-id="24117-126">You can now assign the load building strategy to a load building template.</span></span> <span data-ttu-id="24117-127">Einnig er hægt að nota hann beint í vinnusvæði hleðsluáætlunar.</span><span class="sxs-lookup"><span data-stu-id="24117-127">Alternatively, you can use it directly in the load planning workbench.</span></span>

## <a name="use-a-load-building-strategy-in-the-load-building-workbench"></a><span data-ttu-id="24117-128">Nota hleðsluáætlunarstefnu í vinnusvæði hleðsluáætlunar</span><span class="sxs-lookup"><span data-stu-id="24117-128">Use a load building strategy in the load building workbench</span></span>

1. <span data-ttu-id="24117-129">Farið í **Flutningsstjórnun &gt; Áætlanagerð &gt; Hlaða sniðmáti hleðslu**.</span><span class="sxs-lookup"><span data-stu-id="24117-129">Go to **Transportation management &gt; Planning &gt; Load building workbench**.</span></span>
1. <span data-ttu-id="24117-130">Fylgið einu af eftirfarandi skrefum:</span><span class="sxs-lookup"><span data-stu-id="24117-130">Follow one of these steps:</span></span>

    - <span data-ttu-id="24117-131">Velja þarf stefnu í svæðinu **Hleðsluáætlun**.</span><span class="sxs-lookup"><span data-stu-id="24117-131">Select a strategy in the **Load building strategy** field.</span></span>
    - <span data-ttu-id="24117-132">Ef búið er að skilgreina sniðmát hleðsluáætlunar og því verið úthlutað á hleðsluáætlunina skal á aðgerðasvæðinu í flipanum **Umsjón sniðmáta** velja **Nota sniðmát**.</span><span class="sxs-lookup"><span data-stu-id="24117-132">If you've defined a load building template and assigned the load building strategy to it, on the Action Pane, on the **Manage templates** tab, select **Apply template**.</span></span> <span data-ttu-id="24117-133">Síðan, í fellilistaglugganum **Nota sniðmát hleðsluáætlunar**, skal velja sniðmát í reitnum **Heiti sniðmáts hleðslu**.</span><span class="sxs-lookup"><span data-stu-id="24117-133">Then, in the **Apply load building template** drop-down dialog box, select a template in the **Load building template name** field.</span></span>

1. <span data-ttu-id="24117-134">Á flipanum **Hlaða sniðmátsröð** skal velja eitt eða fleiri [hleðslusniðmát](load-template.md).</span><span class="sxs-lookup"><span data-stu-id="24117-134">On the **Load templates sequence** FastTab, select one or more [load templates](load-template.md).</span></span> <span data-ttu-id="24117-135">Vinnusvæðið reynir að koma hleðslunni fyrir í þessum gerðum af gámum í röðinni sem er tilgreind hér.</span><span class="sxs-lookup"><span data-stu-id="24117-135">The workbench will try to fit the load into these types of containers, in the sequence that is specified here.</span></span> <span data-ttu-id="24117-136">Yfirleitt ætti að setja minnstu gámana efst í listann til að tryggja að minnsti mögulegi gámurinn sé valinn fyrst.</span><span class="sxs-lookup"><span data-stu-id="24117-136">Typically, you should put the smallest containers at the top of the list to ensure that the smallest possible container is selected first.</span></span>
1. <span data-ttu-id="24117-137">Á aðgerðasvæðinu skal velja **Fyrirhugaður farmur**.</span><span class="sxs-lookup"><span data-stu-id="24117-137">On the Action Pane, select **Propose loads**.</span></span>
1. <span data-ttu-id="24117-138">Yfirfara tillögur að hleðslum og tillögur að farmlínum.</span><span class="sxs-lookup"><span data-stu-id="24117-138">Review the proposed loads and proposed load lines.</span></span>
1. <span data-ttu-id="24117-139">Á aðgerðasvæðinu skal velja **Stofna hleðslur** til að stofna hleðslur sem byggja á upprunaskjalslínum í flýtiflipanum **Fyrirhugaðar farmlínur**.</span><span class="sxs-lookup"><span data-stu-id="24117-139">On the Action Pane, select **Create loads** to create loads that are based on the source document lines on the **Proposed load lines** FastTab.</span></span>
1. <span data-ttu-id="24117-140">Lokið síðunni **Hlaða sniðmáti hleðslu**.</span><span class="sxs-lookup"><span data-stu-id="24117-140">Close the **Load building workbench** page.</span></span>
