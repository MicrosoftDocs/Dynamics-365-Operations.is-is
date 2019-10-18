---
title: Virkja frestun skattaútreiknings á dagbók
description: Þetta efni útskýrir hvernig á að nota eiginleikann **Virkja frestun skattaútreiknings á dagbók** til að bæta afköst skattaútreikninga þegar magn dagbókarlína er mikið.
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
ms.openlocfilehash: 5a8ae30a007d3e2b8b7a9bc9eb7786f6e58246d0
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178245"
---
# <a name="enable-delayed-tax-calculation-on-journal"></a><span data-ttu-id="fb5c0-103">Virkja frestun skattaútreiknings á dagbók</span><span class="sxs-lookup"><span data-stu-id="fb5c0-103">Enable delayed tax calculation on journal</span></span>
[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="fb5c0-104">Þetta efni útskýrir hvernig á að nota eiginleikann **Virkja frestun skattaútreiknings á dagbók** til að bæta afköst skattaútreikninga þegar magn dagbókarlína er mikið.</span><span class="sxs-lookup"><span data-stu-id="fb5c0-104">This topic explains how to use the **Enable delayed tax calculation on journal** feature to improve tax calculation performance when the volume of journal lines is huge.</span></span>

<span data-ttu-id="fb5c0-105">Núverandi hegðun útreiknings á söluskatti á dagbók virkjast í rauntíma þegar notandi uppfærir skattskylda reiti, t.d. VSK-skattshóp/VSK-skattshóp vöru.</span><span class="sxs-lookup"><span data-stu-id="fb5c0-105">Current sales tax calculation behavior on journal is real-time triggered when user updates tax related fields, e.g. sales tax group/item sales tax group.</span></span> <span data-ttu-id="fb5c0-106">Sérhver uppfærsla á dagbókarlínustigi reiknar skattfjárhæð á alla dagbókarlínur.</span><span class="sxs-lookup"><span data-stu-id="fb5c0-106">Any update at journal line level will re-calculate tax amount on all journal lines.</span></span> <span data-ttu-id="fb5c0-107">Það hjálpar notendum að sjá reiknaðan skattfjárhæð í rauntíma, en það gæti einnig leitt af sér vandamál með afköst ef magn dagbókarlína er mikið.</span><span class="sxs-lookup"><span data-stu-id="fb5c0-107">It helps user to see real-time calculated tax amount but it could also bring performance issue if  the volume of journal lines is huge.</span></span>

<span data-ttu-id="fb5c0-108">Þessi eiginleiki veitir möguleika á að fresta útreikningi skatta til að leysa vandamál með afköst.</span><span class="sxs-lookup"><span data-stu-id="fb5c0-108">This feature provides an option to delay tax calculation to solve performance issue.</span></span> <span data-ttu-id="fb5c0-109">Ef kveikt er á þessum eiginleika verður skattafjárhæð einungis reiknuð þegar notandi smellir á skipunina „Virðisaukaskatt“ eða bókar færslubókina.</span><span class="sxs-lookup"><span data-stu-id="fb5c0-109">If this feature is turned on, tax amount will only be calculated when user clicks "Sales Tax" command or posts the journal.</span></span>

<span data-ttu-id="fb5c0-110">Notandi getur kveikt/slökkt á færibreytunni á þremur stigum:</span><span class="sxs-lookup"><span data-stu-id="fb5c0-110">User can turn on/off the parameter at three levels:</span></span>
- <span data-ttu-id="fb5c0-111">Eftir lögaðila</span><span class="sxs-lookup"><span data-stu-id="fb5c0-111">By legal entity</span></span>
- <span data-ttu-id="fb5c0-112">Eftir heiti færslubókar</span><span class="sxs-lookup"><span data-stu-id="fb5c0-112">By journal name</span></span>
- <span data-ttu-id="fb5c0-113">Eftir færslubókarhaus</span><span class="sxs-lookup"><span data-stu-id="fb5c0-113">By journal header</span></span>

<span data-ttu-id="fb5c0-114">Kerfið mun taka færibreytugildið á færslubókarhaus sem endanlegt.</span><span class="sxs-lookup"><span data-stu-id="fb5c0-114">System will take the parameter value on journal header as final.</span></span> <span data-ttu-id="fb5c0-115">Færibreytugildi á færslubókarhaus er sjálfgefið frá nafni færslubókar.</span><span class="sxs-lookup"><span data-stu-id="fb5c0-115">Parameter value on journal header will be defaulted from journal name.</span></span> <span data-ttu-id="fb5c0-116">Færibreytugildi á færslubókarheiti verður sjálfgefið frá aðalbókarbreytunni þegar færslubókarheitið er búið til.</span><span class="sxs-lookup"><span data-stu-id="fb5c0-116">Parameter value on journal name will be defaulted from general ledger parameter when the journal name is created.</span></span>

<span data-ttu-id="fb5c0-117">Reitirnir „Eiginleg virðisaukaskattsupphæð“ og „Reiknuð virðisaukaupphæð“ í færslubókinni verða faldir ef kveikt er á þessari færibreytu.</span><span class="sxs-lookup"><span data-stu-id="fb5c0-117">"Actual sales tax amount" and "Calculated sales tax amount" fields on journal will be hided if this parameter is turned on.</span></span> <span data-ttu-id="fb5c0-118">Tilgangurinn er ekki að rugla notanda þar sem gildi þessara tveggja reita mun alltaf sýna 0 áður en notandi kveikir á skattútreikningi.</span><span class="sxs-lookup"><span data-stu-id="fb5c0-118">The purpose is not to confuse user because the value of these two fields will always show 0 before user trigger the tax calculation.</span></span>

## <a name="enable-delayed-tax-calculation-by-legal-entity"></a><span data-ttu-id="fb5c0-119">Virkja frestun skattaútreikninga af lögaðila</span><span class="sxs-lookup"><span data-stu-id="fb5c0-119">Enable delayed tax calculation by legal entity</span></span>

1. <span data-ttu-id="fb5c0-120">Farðu í **Fjárhagur > Fjárhagsuppsetning > Færibreytur fyrir fjárhag**</span><span class="sxs-lookup"><span data-stu-id="fb5c0-120">Go to **General ledger > Ledger setup > General ledger parameters**</span></span>
2. <span data-ttu-id="fb5c0-121">Smelltu á flipann **Vsk.**</span><span class="sxs-lookup"><span data-stu-id="fb5c0-121">Click **Sales tax** tab</span></span>
3. <span data-ttu-id="fb5c0-122">Undir flýtiflipanum **Almennt** finnurðu færibreytuna **Frestun skattaútreikings** og kveikir/slekkur á henni</span><span class="sxs-lookup"><span data-stu-id="fb5c0-122">Under **General** fast tab, find parameter **Delayed tax calculation**, turn on/off it</span></span>

![](media/delayed-tax-calculation-gl.png)



## <a name="enable-delayed-tax-calculation-by-journal-name"></a><span data-ttu-id="fb5c0-123">Virkja frestun skattaútreiknings eftir heiti færslubókar</span><span class="sxs-lookup"><span data-stu-id="fb5c0-123">Enable delayed tax calculation by journal name</span></span>

1. <span data-ttu-id="fb5c0-124">Farðu í **Fjárhag > Færslubókaruppsetning > Heiti færslubókar**</span><span class="sxs-lookup"><span data-stu-id="fb5c0-124">Go to **General ledger > Journal setup > Journal names**</span></span>
2. <span data-ttu-id="fb5c0-125">Undir flýtiflipanum **Almennt** finnurðu færibreytuna **Frestun skattaútreikings** og kveikir/slekkur á henni</span><span class="sxs-lookup"><span data-stu-id="fb5c0-125">Under **General** fast tab, find parameter **Delayed tax calculation**, turn on/off it</span></span>

![](media/delayed-tax-calculation-journal-name.png)

## <a name="enable-delayed-tax-calculation-by-journal"></a><span data-ttu-id="fb5c0-126">Virkja frestun skattaútreiknings eftir færslubók</span><span class="sxs-lookup"><span data-stu-id="fb5c0-126">Enable delayed tax calculation by journal</span></span>

1. <span data-ttu-id="fb5c0-127">Farðu í **Fjárhag > Færslubókarfærslur > Almennar færslubækur**</span><span class="sxs-lookup"><span data-stu-id="fb5c0-127">Go to **General ledger > Journal entries > General journals**</span></span>
2. <span data-ttu-id="fb5c0-128">Smelltu á **Nýtt**</span><span class="sxs-lookup"><span data-stu-id="fb5c0-128">Click **New**</span></span>
3. <span data-ttu-id="fb5c0-129">Veldu heiti færslubókar</span><span class="sxs-lookup"><span data-stu-id="fb5c0-129">Select a journal name</span></span>
4. <span data-ttu-id="fb5c0-130">Smelltu á **Uppsetningu**</span><span class="sxs-lookup"><span data-stu-id="fb5c0-130">Click **Setup**</span></span>
5. <span data-ttu-id="fb5c0-131">Finndu færibreytuna **Frestun skattaútreiknings**, kveiktu/slökktu á henni</span><span class="sxs-lookup"><span data-stu-id="fb5c0-131">Find parameter **Delayed tax calculation**, turn on/off it</span></span>

![](media/delayed-tax-calculation-journal-header.png)
