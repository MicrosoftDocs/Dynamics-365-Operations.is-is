---
title: Prófunarbreytur gæðastjórnunar
description: Í þessu efnisatriði er lýst hvernig eigi að stofna prufubreytur sem hægt er að nota til eðlisbundinna prófana á gæðapöntunum í Microsoft Dynamics 365 Supply Chain Management.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1e94972b41baf3f59a633fa7bbc7434abfb90460
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956699"
---
# <a name="quality-management-test-variables"></a><span data-ttu-id="60883-103">Prófunarbreytur gæðastjórnunar</span><span class="sxs-lookup"><span data-stu-id="60883-103">Quality management test variables</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="60883-104">Í þessu efnisatriði er lýst hvernig eigi að stofna prufubreytur sem hægt er að nota til eðlisbundinna prófana á gæðapöntunum í Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="60883-104">This topic describes how to create test variables that can be used for qualitative tests on quality orders in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="60883-105">Fyrir hvert gæðapróf sem er skilgreint á síðunni **Prófanir** þarf að skilgreina prófunarbreytu og mögulegar útkomur hennar (niðurstöður).</span><span class="sxs-lookup"><span data-stu-id="60883-105">For every qualitative test that is defined on the **Tests** page, you must define a test variable and its possible outcomes (results).</span></span> <span data-ttu-id="60883-106">(Fyrir gæðaprófanir er reiturinn **Gerð** á síðunni **Prófanir** stilltur á *Valkostur*.)</span><span class="sxs-lookup"><span data-stu-id="60883-106">(For qualitative tests, the **Type** field on the **Tests** page is set to *Option*.)</span></span>

<span data-ttu-id="60883-107">Þú notar síðuna **Prófunarbreytur** til að setja upp, breyta, og skoða mögulegar útkomur fyrir prófunarbreytu sem er tengd gæðaprófun.</span><span class="sxs-lookup"><span data-stu-id="60883-107">You use the **Test variables** page to set up, edit, and view the possible outcomes for a test variable that is associated with a qualitative test.</span></span> <span data-ttu-id="60883-108">Fyrir hverja útkomu úthlutar þú stöðu útkomu sem annaðhvort *Staðið* eða *Fallið* til að gefa til kynna hvort prófið sé staðið eða fallið þegar sú útkoma er valin sem niðurstaða prófunar.</span><span class="sxs-lookup"><span data-stu-id="60883-108">For each outcome, you assign an outcome status of either *Pass* or *Fail* to indicate whether the test is passed or failed when that outcome is selected as a test result.</span></span> <span data-ttu-id="60883-109">Síðan **Prófunarflokkar** er notuð til að úthluta breytu á prófun og sjálfvirkri niðurstöðu á staka eigindlega prófun.</span><span class="sxs-lookup"><span data-stu-id="60883-109">You use the **Test groups** page to assign a test variable and a default outcome for it to an individual qualitative test.</span></span>

<span data-ttu-id="60883-110">Fyrir hverja prófunarbreytur er mælt með að skilgreina a.m.k. tvær útkomur: ein sem er með stöðu útkomu sem *Staðið* og hin með stöðu útkomu sem *Fallið*.</span><span class="sxs-lookup"><span data-stu-id="60883-110">For every test variable, we recommend that you define at least two outcomes: one that has an outcome status of *Pass* and one that has an outcome status of *Fail*.</span></span> <span data-ttu-id="60883-111">Engin takmörk eru á heildarfjölda breytna eða niðurstaðna sem hægt er að skilgreina.</span><span class="sxs-lookup"><span data-stu-id="60883-111">There is no limit on the total number of variables or outcomes that can be defined.</span></span> <span data-ttu-id="60883-112">Auk þess geta mörg próf notað sömu prófbreytur til að skrá niðurstöður.</span><span class="sxs-lookup"><span data-stu-id="60883-112">Additionally, multiple tests can use the same test variables to record results.</span></span>

## <a name="examples-of-test-variables"></a><span data-ttu-id="60883-113">Dæmi um prófunarbreytur</span><span class="sxs-lookup"><span data-stu-id="60883-113">Examples of test variables</span></span>

### <a name="example-1"></a><span data-ttu-id="60883-114">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="60883-114">Example 1</span></span>

<span data-ttu-id="60883-115">Framleiðslufyrirtæki framkvæmir tvö próf á framleiddum efnum.</span><span class="sxs-lookup"><span data-stu-id="60883-115">A manufacturing company performs two tests on manufactured materials.</span></span> <span data-ttu-id="60883-116">Í einu prófi er sýrustigið tengt litaræmu.</span><span class="sxs-lookup"><span data-stu-id="60883-116">In one test, the pH level is associated with a color strip.</span></span> <span data-ttu-id="60883-117">Áættanlegt sýrustig er í ljósari litum og óásættanlegt sýrustig er í dekkri litum.</span><span class="sxs-lookup"><span data-stu-id="60883-117">Acceptable pH levels are in lighter colors, and unacceptable pH levels are in darker colors.</span></span> <span data-ttu-id="60883-118">Í öðru prófi eru framkvæmdar margar sjónrænar skoðanir og gæðastarfsmenn nota eigin dómgreind til að ákveða hvort varan stenst eða fellur á slíkri skoðun.</span><span class="sxs-lookup"><span data-stu-id="60883-118">In another test, multiple visual inspections are performed, and quality workers use their judgement to determine whether the item passes or fails the visual inspection.</span></span>

### <a name="example-2"></a><span data-ttu-id="60883-119">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="60883-119">Example 2</span></span>

<span data-ttu-id="60883-120">Framleiðslufyrirtæki sem framleiðir kexkökur notar skoðunarpróf sem nær til nokkurra gerða af hinni framleiddu vöru.</span><span class="sxs-lookup"><span data-stu-id="60883-120">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="60883-121">Þessi prófun hefur nokkur breytur.</span><span class="sxs-lookup"><span data-stu-id="60883-121">This inspection test has several variables.</span></span> <span data-ttu-id="60883-122">Ein færibreyta er bragð, með hugsanlegri útkomu gott eða vont.</span><span class="sxs-lookup"><span data-stu-id="60883-122">One variable is taste, and the possible outcomes for it are good and bad.</span></span> <span data-ttu-id="60883-123">Önnur færibreyta er litur, með mögulega niðurstöðu of dökkur, of ljós, og í lagi.</span><span class="sxs-lookup"><span data-stu-id="60883-123">A second variable is color, and the possible outcomes for it are too dark, too light, and correct.</span></span>

## <a name="create-a-test-variable"></a><span data-ttu-id="60883-124">Stofna prófunarbreytu</span><span class="sxs-lookup"><span data-stu-id="60883-124">Create a test variable</span></span>

<span data-ttu-id="60883-125">Fylgið þessum skrefum til að stofna prófunarbreytu.</span><span class="sxs-lookup"><span data-stu-id="60883-125">Follow these steps to create a test variable.</span></span>

1. <span data-ttu-id="60883-126">Farið í **Birgðastjórnun \> Uppsetning \> Gæðastjórnun \> Prófunarbreytur**.</span><span class="sxs-lookup"><span data-stu-id="60883-126">Go to **Inventory management \> Setup \> Quality control \> Test variables**.</span></span>
1. <span data-ttu-id="60883-127">Á aðgerðasvæðinu skal velja **Ný** til að bæta línu við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="60883-127">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="60883-128">Stillið svo eftirfarandi reiti fyrir nýju línuna:</span><span class="sxs-lookup"><span data-stu-id="60883-128">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="60883-129">**Breyta** – Færið inn einkvæmt kenni eða heiti fyrir breytuna.</span><span class="sxs-lookup"><span data-stu-id="60883-129">**Variable** – Enter a unique ID or name for the variable.</span></span>
    - <span data-ttu-id="60883-130">**Lýsing** – Færið inn ítarlega lýsingu á breytunni.</span><span class="sxs-lookup"><span data-stu-id="60883-130">**Description** – Enter a detailed description of the variable.</span></span>

1. <span data-ttu-id="60883-131">While the new row is still selected, select **Niðurstöður** on the Action Pane.</span><span class="sxs-lookup"><span data-stu-id="60883-131">While the new row is still selected, select **Outcomes** on the Action Pane.</span></span>
1. <span data-ttu-id="60883-132">Á síðunni **Útkomur úr prófunarbreytum**, á aðgerðasvæðinu, skal velja **Ný** til að bæta línu við hnitið.</span><span class="sxs-lookup"><span data-stu-id="60883-132">On the **Test variable outcomes** page, on the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="60883-133">Stillið svo eftirfarandi reiti fyrir nýju línuna:</span><span class="sxs-lookup"><span data-stu-id="60883-133">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="60883-134">**Útkoma** – Færið inn einkvæmt kenni eða heiti fyrir útkomuna.</span><span class="sxs-lookup"><span data-stu-id="60883-134">**Outcome** – Enter a unique ID or name for the outcome.</span></span>
    - <span data-ttu-id="60883-135">**Lýsing** – Færið inn ítarlega lýsingu á útkomunni.</span><span class="sxs-lookup"><span data-stu-id="60883-135">**Description** – Enter a detailed description of the outcome.</span></span>
    - <span data-ttu-id="60883-136">**Staða útkomu** – Veljið annaðhvort *Staðið* eða *Fallið* til að gefa til kynna hvort prófið sé staðið eða fallið þegar sú útkoma er valin sem niðurstaða prófunar.</span><span class="sxs-lookup"><span data-stu-id="60883-136">**Outcome status** – Select either *Pass* or *Fail* to indicate whether the test is passed or failed when the outcome is selected as a test result.</span></span>

1. <span data-ttu-id="60883-137">Endurtakið fyrra skref fyrir hverja útkomu sem fylgir á eftir.</span><span class="sxs-lookup"><span data-stu-id="60883-137">Repeat the previous step for each additional outcome.</span></span> <span data-ttu-id="60883-138">Gangið úr skugga um að a.m.k. ein útkoma sé með stöðu útkomu sem *Staðið* og a.m.k. ein sé með stöðuna *Fallið*.</span><span class="sxs-lookup"><span data-stu-id="60883-138">Make sure that at least one outcome has an outcome status of *Pass* and at least one has an outcome status of *Fail*.</span></span>
1. <span data-ttu-id="60883-139">Lokaðu síðunum.</span><span class="sxs-lookup"><span data-stu-id="60883-139">Close the pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="60883-140">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="60883-140">Additional resources</span></span>

- [<span data-ttu-id="60883-141">Prófunartæki gæðastjórnunar</span><span class="sxs-lookup"><span data-stu-id="60883-141">Quality management test instruments</span></span>](quality-test-instruments.md)
- [<span data-ttu-id="60883-142">Prófanir gæðastjórnunar</span><span class="sxs-lookup"><span data-stu-id="60883-142">Quality management tests</span></span>](quality-tests.md)
- [<span data-ttu-id="60883-143">Prófunarflokkar gæðastjórnunar</span><span class="sxs-lookup"><span data-stu-id="60883-143">Quality management test groups</span></span>](quality-test-groups.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
