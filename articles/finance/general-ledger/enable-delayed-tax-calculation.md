---
title: Virkja frestun skattaútreiknings á dagbókum
description: Þetta efni útskýrir hvernig á að kveikja á eiginleikanum Frestun skattaútreiknings að bæta afköst skattaútreikninga þegar fjöldi dagbókarlína er afar mikið.
author: ericwang
manager: Ann Beebe
ms.date: 09/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2019-09-18
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: ed8e5f930bbb6b0fb570ba1eb23c0816210c1814
ms.sourcegitcommit: bfd6142569196a060e3f37893c78f00c40a2a18c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/09/2020
ms.locfileid: "2946167"
---
# <a name="enable-delayed-tax-calculation-on-journals"></a><span data-ttu-id="90573-103">Virkja frestun skattaútreiknings á dagbókum</span><span class="sxs-lookup"><span data-stu-id="90573-103">Enable delayed tax calculation on journals</span></span>
[!include [banner](../includes/banner.md)]


<span data-ttu-id="90573-104">Þetta efni útskýrir hvernig þú getur seinkað útreikningi á söluskatti í færslubókum.</span><span class="sxs-lookup"><span data-stu-id="90573-104">This topic explains how you can delay sales tax calculation on journals.</span></span> <span data-ttu-id="90573-105">Þessi geta hjálpar til við að bæta afköst skattaútreikninga þegar margar færslubókarlínur eru til staðar.</span><span class="sxs-lookup"><span data-stu-id="90573-105">This capability helps improve the performance of tax calculations when there are many journal lines.</span></span>

<span data-ttu-id="90573-106">Sjálfgefið er að fjárhæðir söluskatts í færslubókarlínum eru reiknaðar út í hvert skipti sem skattatengdir reitir eru uppfærðir.</span><span class="sxs-lookup"><span data-stu-id="90573-106">By default, sales tax amounts on journal lines are calculated whenever tax-related fields are updated.</span></span> <span data-ttu-id="90573-107">Þessir reitir innihalda reiti fyrir VSK-flokka og VSK-flokka vöru.</span><span class="sxs-lookup"><span data-stu-id="90573-107">These fields include the fields for sales tax groups and item sales tax groups.</span></span> <span data-ttu-id="90573-108">Sérhver uppfærsla á færslubókarlínu veldur því að skattfjárhæðir eru endurreiknaðar fyrir allar dagbókarlínur.</span><span class="sxs-lookup"><span data-stu-id="90573-108">Any update to a journal line causes tax amounts to be recalculated for all journal lines.</span></span> <span data-ttu-id="90573-109">Þrátt fyrir að þessi hegðun hjálpi notendum að sjá skattaupphæðir reiknaðar í rauntíma getur það einnig haft áhrif á afköst ef fjöldi færslubókarlína er mjög mikill.</span><span class="sxs-lookup"><span data-stu-id="90573-109">Although this behavior helps user see tax amounts calculated in real time, it can also affect performance if the number of journal lines is very large.</span></span>

<span data-ttu-id="90573-110">Aðgerðin fyrir útreikning á sköttum gerir kleift að fresta skattaútreikningi á færslubókum og hjálpar því til við að laga afkastavandamál.</span><span class="sxs-lookup"><span data-stu-id="90573-110">The Delayed tax calculation feature lets you delay tax calculation on journals and therefore helps fix performance issues.</span></span> <span data-ttu-id="90573-111">Þegar kveikt er á þessum eiginleika verða skattaupphæðir aðeins reiknaðar þegar notandi velur **Virðisaukaskatt** eða bókar færslubókina.</span><span class="sxs-lookup"><span data-stu-id="90573-111">When this feature is turned on, tax amounts are calculated only when a user selects **Sales Tax** or posts the journal.</span></span>

<span data-ttu-id="90573-112">Þú getur tafið útreikning á VSK-skatti á þremur stigum:</span><span class="sxs-lookup"><span data-stu-id="90573-112">You can delay the calculation of sales taxes at three levels:</span></span>

- <span data-ttu-id="90573-113">Lögaðili</span><span class="sxs-lookup"><span data-stu-id="90573-113">Legal entity</span></span>
- <span data-ttu-id="90573-114">Heiti færslubókar</span><span class="sxs-lookup"><span data-stu-id="90573-114">Journal name</span></span>
- <span data-ttu-id="90573-115">Færslubókarhaus</span><span class="sxs-lookup"><span data-stu-id="90573-115">Journal header</span></span>

<span data-ttu-id="90573-116">Kerfið hefur forgang til stillingar fyrir færslubókarhaus.</span><span class="sxs-lookup"><span data-stu-id="90573-116">The system gives priority to the setting for the journal header.</span></span> <span data-ttu-id="90573-117">Sjálfgefið er að þessi stilling er tekin úr nafni færslubókarinnar.</span><span class="sxs-lookup"><span data-stu-id="90573-117">By default, this setting is taken from the journal name.</span></span> <span data-ttu-id="90573-118">Sjálfgefið er að stillingin fyrir færslubókarheitið sé tekin úr stillingunni á síðunni **Almennar fjárhagsbreytur** þegar færslubókarheitið er búið til.</span><span class="sxs-lookup"><span data-stu-id="90573-118">By default, the setting for the journal name is taken from the setting on the **General ledger parameters** page when the journal name is created.</span></span> <span data-ttu-id="90573-119">Eftirfarandi kaflar útskýra hvernig á að kveikja á seinkuðum útreikningum á skatti lögaðila, færslubókarheiti og færslubókarhausum.</span><span class="sxs-lookup"><span data-stu-id="90573-119">The following sections explain how to turn on delayed tax calculation for legal entities, journal names, and journal headers.</span></span>

## <a name="turn-on-delayed-tax-calculation-at-the-legal-entity-level"></a><span data-ttu-id="90573-120">Kveiktu á frestun skattaútreiknings á stigi lögaðila</span><span class="sxs-lookup"><span data-stu-id="90573-120">Turn on delayed tax calculation at the legal entity level</span></span>

1. <span data-ttu-id="90573-121">Farðu í **Fjárhag \> Fjárhagsuppsetning \> Fjárhagsfæribreytur**.</span><span class="sxs-lookup"><span data-stu-id="90573-121">Go to **General ledger \> Ledger setup \> General ledger parameters**.</span></span>
2. <span data-ttu-id="90573-122">Á flipanum **VSK-skattur** á flýtiflipanum **Almennt** skal stilla valkostinn **Frestun skattaútreiknings** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="90573-122">On the **Sales tax** tab, on the **General** FastTab, set the **Delayed tax calculation** option to **Yes**.</span></span>

![Mynd af almennum fjárhagsfæribreytum](media/delayed-tax-calculation-gl.png)

## <a name="turn-on-delayed-tax-calculation-at-the-journal-name-level"></a><span data-ttu-id="90573-124">Kveiktu á frestun skattaútreiknings á stigi færslubókarheitis</span><span class="sxs-lookup"><span data-stu-id="90573-124">Turn on delayed tax calculation at the journal name level</span></span>

1. <span data-ttu-id="90573-125">Farðu í **Fjárhag \> Færslubókaruppsetning \> Færslubókarheiti**.</span><span class="sxs-lookup"><span data-stu-id="90573-125">Go to **General ledger \> Journal setup \> Journal names**.</span></span>
2. <span data-ttu-id="90573-126">Á flýtiflipanum **Almennt**, í kaflanum **VSK-skattur**, skal stilla valkostinn **Frestun skattaútreiknings** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="90573-126">On the **General** FastTab, in the **Sales tax** section, set the **Delayed tax calculation** option to **Yes**.</span></span>

![Mynd af færslubókanöfnum](media/delayed-tax-calculation-journal-name.png)

## <a name="turn-on-delayed-tax-calculation-at-the-journal-header-level"></a><span data-ttu-id="90573-128">Kveiktu á frestun skattaútreiknings á stigi færslubókarhauss</span><span class="sxs-lookup"><span data-stu-id="90573-128">Turn on delayed tax calculation at the journal header level</span></span>

1. <span data-ttu-id="90573-129">Farðu í **Fjárhag \> Færslubókarfærslur \> Almennar færslubækur**.</span><span class="sxs-lookup"><span data-stu-id="90573-129">Go to **General ledger \> Journal entries \> General journals**.</span></span>
2. <span data-ttu-id="90573-130">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="90573-130">Select **New**.</span></span>
3. <span data-ttu-id="90573-131">Veldu heiti færslubókar.</span><span class="sxs-lookup"><span data-stu-id="90573-131">Select a journal name.</span></span>
4. <span data-ttu-id="90573-132">Á flipanum **Uppsetning** stillirðu valkostinn **Frestun skattaútreiknings** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="90573-132">On the **Setup** tab, set the **Delayed tax calculation** option to **Yes**.</span></span>

![Mynd af síðu almennrar færslubókar](media/delayed-tax-calculation-journal-header.png)
