---
title: Úrræðaleit fyrir afurðaafbrigðastilli
description: Þetta efnisatriði lýsir því hvernig á að leysa vandamál sem kunna að koma upp á meðan unnið er með afurðarafbrigðastilli.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: e6cfeb6a2b4166dfa9a5a5cc1b7d3d913b865ce2
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4999607"
---
# <a name="troubleshoot-the-product-configurator"></a><span data-ttu-id="d11aa-103">Úrræðaleit fyrir afurðaafbrigðastilli</span><span class="sxs-lookup"><span data-stu-id="d11aa-103">Troubleshoot the product configurator</span></span>

<span data-ttu-id="d11aa-104">Í þessu efnisatriði er því lýst hvernig á að laga vandamál sem kunna að koma upp þegar unnið er með afurðarafbrigðisstilli.</span><span class="sxs-lookup"><span data-stu-id="d11aa-104">This topic describes how to fix issues that you might encounter while you work with the product configurator.</span></span>

## <a name="item-text-is-overwritten-when-i-configure-a-product-on-a-sales-order-line"></a><span data-ttu-id="d11aa-105">Skrifað er yfir vörutexta þegar ég skilgreini afurð á sölupöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="d11aa-105">Item text is overwritten when I configure a product on a sales order line.</span></span>

### <a name="issue-description"></a><span data-ttu-id="d11aa-106">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="d11aa-106">Issue description</span></span>

<span data-ttu-id="d11aa-107">Þetta vandamál á sér stað þegar sölupöntunarlína er stofnuð fyrir skilgreinanlega vöru og textanum er svo breytt.</span><span class="sxs-lookup"><span data-stu-id="d11aa-107">This issue occurs when you create a sales order line for a configurable item and then modify the item text.</span></span> <span data-ttu-id="d11aa-108">Þegar varan er grunnstillt og **Í lagi** er svo valið skrifað yfir textann með staðlaða textanum.</span><span class="sxs-lookup"><span data-stu-id="d11aa-108">When you configure the item and then select **OK**, the text is overwritten with the standard text.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="d11aa-109">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="d11aa-109">Issue resolution</span></span>

<span data-ttu-id="d11aa-110">Búist er við þessari hegðun.</span><span class="sxs-lookup"><span data-stu-id="d11aa-110">This behavior is expected.</span></span> <span data-ttu-id="d11aa-111">Textasvæðið inniheldur heiti vöruvíddasamsetningar sem er aðeins fyllt út eftir að lína hefur verið skilgreind.</span><span class="sxs-lookup"><span data-stu-id="d11aa-111">The text field includes the variant name, which is filled in only after you configure the line.</span></span> <span data-ttu-id="d11aa-112">Þess vegna verður að breyta textanum eftir að lína hefur verið skilgreind og ekki áður.</span><span class="sxs-lookup"><span data-stu-id="d11aa-112">Therefore, you must change the text after you've configured the line, not before.</span></span>

## <a name="integer-attributes-are-incorrectly-rounded-when-product-configuration-models-are-calculated"></a><span data-ttu-id="d11aa-113">Heiltölueigindir eru rangt sléttaðar þegar afbrigðalíkan afurðar er reiknað út.</span><span class="sxs-lookup"><span data-stu-id="d11aa-113">Integer attributes are incorrectly rounded when product configuration models are calculated.</span></span>

### <a name="issue-description"></a><span data-ttu-id="d11aa-114">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="d11aa-114">Issue description</span></span>

<span data-ttu-id="d11aa-115">Þetta vandamál getur komið upp þegar eftirfarandi röð aðgerða er framkvæmd:</span><span class="sxs-lookup"><span data-stu-id="d11aa-115">This issue can occur when you perform the following series of actions:</span></span>

1. <span data-ttu-id="d11aa-116">Setja upp eftirfarandi eigindir í afbrigðalíkani framleiðslu:</span><span class="sxs-lookup"><span data-stu-id="d11aa-116">Set up the following attributes on a production configuration model:</span></span>

    - <span data-ttu-id="d11aa-117">Innsláttur (heiltala)</span><span class="sxs-lookup"><span data-stu-id="d11aa-117">Input (integer)</span></span>
    - <span data-ttu-id="d11aa-118">Prósenta (tugabrot)</span><span class="sxs-lookup"><span data-stu-id="d11aa-118">Percent (decimal)</span></span>
    - <span data-ttu-id="d11aa-119">Niðurstaða (heiltala)</span><span class="sxs-lookup"><span data-stu-id="d11aa-119">Result (integer)</span></span>

2. <span data-ttu-id="d11aa-120">Stofna útreikning sem hefur eftirfarandi segð:</span><span class="sxs-lookup"><span data-stu-id="d11aa-120">Create a calculation that has the following expression:</span></span>

    <span data-ttu-id="d11aa-121">*Niðurstaða* = *Inntak* × *Prósenta* ÷ 100</span><span class="sxs-lookup"><span data-stu-id="d11aa-121">*Result* = *Input* × *Percent* ÷ 100</span></span>

<span data-ttu-id="d11aa-122">Í þessu tilvikum er niðurstaðan í heilli tölu ekki alltaf rétt sléttuð.</span><span class="sxs-lookup"><span data-stu-id="d11aa-122">In this case, the integer result isn't always correctly rounded.</span></span> <span data-ttu-id="d11aa-123">Til dæmis er inntak 1.000 og prósenta er 2,40.</span><span class="sxs-lookup"><span data-stu-id="d11aa-123">For example, the input is 1,000, and the percentage is 2.40.</span></span> <span data-ttu-id="d11aa-124">Þess vegna er búist við að heiltalan verði 24, þar sem 2,40 prósent af 1.000 er 24 (eða 24,00 á tugabrotssniði).</span><span class="sxs-lookup"><span data-stu-id="d11aa-124">Therefore, you expect the integer result to be 24, because 2.40 percent of 1,000 is 24 (or 24.00 in decimal form).</span></span> <span data-ttu-id="d11aa-125">Þess í stað er útkoman sýnd sem 23.</span><span class="sxs-lookup"><span data-stu-id="d11aa-125">Instead, the result is shown as 23.</span></span> <span data-ttu-id="d11aa-126">Þegar prósentan er hins vegar 2,39 er útreikningurinn sléttaður í 24 í stað 23.</span><span class="sxs-lookup"><span data-stu-id="d11aa-126">However, when the percentage is 2.39, the calculation is rounded to 24 instead of 23.</span></span> <span data-ttu-id="d11aa-127">Þegar prósenta er 2,50 er útreikningurinn sléttaður í 25, eins og búist er við.</span><span class="sxs-lookup"><span data-stu-id="d11aa-127">When the percentage is 2.50, the calculation is rounded to 25, as expected.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="d11aa-128">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="d11aa-128">Issue resolution</span></span>

<span data-ttu-id="d11aa-129">Þetta vandamál kemur upp vegna þess hvernig Microsoft Solver Foundation táknar tölur í innra skipulagi með brotum.</span><span class="sxs-lookup"><span data-stu-id="d11aa-129">This issue occurs because of the way that Microsoft Solver Foundation internally represents numbers by using fractions.</span></span> <span data-ttu-id="d11aa-130">Fyrir dæmið á undan er niðurstaða útreikningsins þar sem prósentutalan er 2,40 er táknuð sem 27021597764222975 ÷ 1125899906842624 = 23.99999999999999911182158029987476766109466552734375.</span><span class="sxs-lookup"><span data-stu-id="d11aa-130">For the preceding example, the result of the calculation where the percentage is 2.40 is represented as 27021597764222975 ÷ 1125899906842624 = 23.99999999999999911182158029987476766109466552734375.</span></span> <span data-ttu-id="d11aa-131">Þegar .NET endurgerir þetta gildi sem heiltölu er það aftur 23.</span><span class="sxs-lookup"><span data-stu-id="d11aa-131">When .NET casts this value as an integer, it will return 23.</span></span>

<span data-ttu-id="d11aa-132">Þessari hegðun verður ekki breytt vegna þess að aðrar aðstæður eru háðar henni.</span><span class="sxs-lookup"><span data-stu-id="d11aa-132">This behavior won't be changed, because other scenarios depend on it.</span></span> <span data-ttu-id="d11aa-133">Í dæminu á undan er hægt að lagfæra vandamálið með því að nota aðra aukastafaeigind og útreikning.</span><span class="sxs-lookup"><span data-stu-id="d11aa-133">For the preceding example, you can fix the issue by introducing an additional decimal attribute and a calculation.</span></span>

<span data-ttu-id="d11aa-134">Þú getur til dæmis sett upp eftirfarandi eigindir í afbrigðalíkan framleiðslu:</span><span class="sxs-lookup"><span data-stu-id="d11aa-134">For example, you can set up the following attributes on a production configuration model:</span></span>

- <span data-ttu-id="d11aa-135">Innsláttur (heiltala)</span><span class="sxs-lookup"><span data-stu-id="d11aa-135">Input (integer)</span></span>
- <span data-ttu-id="d11aa-136">Prósenta (tugabrot)</span><span class="sxs-lookup"><span data-stu-id="d11aa-136">Percent (decimal)</span></span>
- <span data-ttu-id="d11aa-137">ResultDecimal (tugir)</span><span class="sxs-lookup"><span data-stu-id="d11aa-137">ResultDecimal (decimal)</span></span>
- <span data-ttu-id="d11aa-138">ResultInteger (heiltala)</span><span class="sxs-lookup"><span data-stu-id="d11aa-138">ResultInteger (integer)</span></span>

<span data-ttu-id="d11aa-139">Síðan er hægt að bæta við eftirfarandi útreikningum:</span><span class="sxs-lookup"><span data-stu-id="d11aa-139">You can then add the following calculations:</span></span>

- <span data-ttu-id="d11aa-140">*ResultDecimal* = *Inntak* × *Prósenta* ÷ 100</span><span class="sxs-lookup"><span data-stu-id="d11aa-140">*ResultDecimal* = *Input* × *Percent* ÷ 100</span></span>
- <span data-ttu-id="d11aa-141">*ResultInteger* = *ResultDecimal*</span><span class="sxs-lookup"><span data-stu-id="d11aa-141">*ResultInteger* = *ResultDecimal*</span></span>
