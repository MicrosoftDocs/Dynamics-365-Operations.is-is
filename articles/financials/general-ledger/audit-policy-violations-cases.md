---
title: Brot á endurskoðun og tilvik
description: Þessi grein útskýrir hvernig endurskoðunarmál eru stofnuð vegna brota á reglum endurskoðunarstefnu Þetta felur einnig í sér upplýsingar um mismunandi leiðir sem endurskoðunarstefnur nota dagsetningabil skjalavals.
author: ryansandness
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AuditPolicyAdditionalOption, AuditPolicyRule
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13091
ms.assetid: e0e66c6d-c396-4a9d-b3b6-3641d130fdc0
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3ed72f829ca4060fe0a4c03b6d4a47a98cdebd6
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "352529"
---
# <a name="audit-policy-violations-and-cases"></a><span data-ttu-id="b4f6e-104">Brot á endurskoðun og tilvik</span><span class="sxs-lookup"><span data-stu-id="b4f6e-104">Audit policy violations and cases</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b4f6e-105">Þessi grein útskýrir hvernig endurskoðunarmál eru stofnuð vegna brota á reglum endurskoðunarstefnu</span><span class="sxs-lookup"><span data-stu-id="b4f6e-105">The article explains how audit cases are generated from violations of audit policy rules.</span></span> <span data-ttu-id="b4f6e-106">Þetta felur einnig í sér upplýsingar um mismunandi leiðir sem endurskoðunarstefnur nota dagsetningabil skjalavals.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-106">It also includes information about the various ways that audit policies use the document selection date range.</span></span>

<a name="how-audit-cases-are-generated"></a><span data-ttu-id="b4f6e-107">Hvernig endurskoðunarmál eru stofnuð</span><span class="sxs-lookup"><span data-stu-id="b4f6e-107">How audit cases are generated</span></span>
-----------------------------

<span data-ttu-id="b4f6e-108">Endurskoðunarstefnur eru notaðar til að auðkenna kostnaðarskýrslur, innkaupapantanir og reikninga lánardrottna sem ekki samræmast viðskiptareglum sem þú tilgreinir og skilgreina sem reglur endurskoðunarstefnu.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-108">Audit policies are used to identify expense reports, purchase orders, and vendor invoices that don't comply with business rules that you define and configure as audit policy rules.</span></span> 

<span data-ttu-id="b4f6e-109">Endurskoðunarreglur eru keyrðar í runuham.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-109">Audit policies are run in batch mode.</span></span> <span data-ttu-id="b4f6e-110">Þegar endurskoðunarregla er keyrð eru allar stefnureglur sem eru hluti þeirrar reglu keyrðar á sama tíma.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-110">When you run an audit policy, all the policy rules that are part of that policy are run at the same time.</span></span>

<span data-ttu-id="b4f6e-111">Hver stefnuregla metur safn skjala.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-111">Each policy rule evaluates a set of documents.</span></span> <span data-ttu-id="b4f6e-112">Stefnureglan velur skjöl sem eru í dagsetningabili skjalavals og sem samsvara tilgreindum skilyrðum.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-112">The policy rule selects documents that are in the document selection date range and that match the specified criteria.</span></span> <span data-ttu-id="b4f6e-113">Til dæmis gæti ein stefnuregla valið kostnaðarskýrslur sem hafa máltíðir sem fara fram yfir 50,00.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-113">For example, one policy rule might select expense reports that have meals that exceed 50.00.</span></span> <span data-ttu-id="b4f6e-114">Önnur stefnuregla gæti valið reikninga lánardrottna sem eru til greiðslu til tiltekins lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-114">Another policy rule might select vendor invoices that are payable to a specific vendor.</span></span> <span data-ttu-id="b4f6e-115">Fyrir hvert skjal sem er valið í safninu er brot myndað.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-115">For each document that is selected in the set, a violation is generated.</span></span> <span data-ttu-id="b4f6e-116">Það brot er færsla um að tiltekið skjal, eins og reikningur 12345, samræmist ekki stefnureglunni.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-116">That violation is a record that a particular document, such as invoice 12345, doesn't comply with the policy rule.</span></span> 

<span data-ttu-id="b4f6e-117">Margar endurskoðunarfærslur eru flokkaðar saman og tengdar endurskoðunarmálum.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-117">Multiple audit violation records are grouped together and associated with audit cases.</span></span> <span data-ttu-id="b4f6e-118">Að sjálfgefnu eru mál fyrir hverja endurskoðunarreglu flokkuð eftir reglu endurskoðunarstefnu.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-118">By default, cases for each audit policy are grouped by audit policy rule.</span></span> <span data-ttu-id="b4f6e-119">Ef þess er óskað er hægt að velja önnur flokkunarskilyrði með því að nota síðuna **Flokkunarskilyrði tilvika**.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-119">If you prefer, you can select other grouping criteria by using the **Case grouping criteria** page.</span></span> <span data-ttu-id="b4f6e-120">Til dæmis er hægt að flokka kostnaðarhausa eftir verkkenni og reikningum lánardrottna eftir lánardrottnalykli.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-120">For example, you can group expense headers by project ID and vendor invoices by vendor account.</span></span> <span data-ttu-id="b4f6e-121">Í þessu tilfelli verða öll brot á kostnaðarhaus sem hafa sama verkkennið flokkuð í sama tilvikið og allir reikningar lánardrottins sem hafa sama lánardrottnalykil verða flokkaðar í sama tilvikið.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-121">In this case, all expense header violations that have the same project ID will be grouped in the same case, and all vendor invoices that have the same vendor account will be grouped in the same case.</span></span> 

> [!NOTE]
> <span data-ttu-id="b4f6e-122">Fyrir reglur endurskoðunarstefnu sem byggja á fyrirspurnartegundinni **Tvítekning** eru brot ekki flokkuð eftir stefnureglu eða skilyrðunum sem eru tilgreind á síðunni **Flokkunarskilyrði tilvika**.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-122">For audit policy rules that are based on a **Duplicate** query type, violations aren't grouped by policy rule or by the criteria that are specified on the **Case grouping criteria** page.</span></span> <span data-ttu-id="b4f6e-123">Þessi í stað eru þau flokkuð eftir þeim skilyrðum sem eru búin til í reglu endurskoðunarstefnu.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-123">Instead, they are grouped by the criteria that are built into the audit policy rule.</span></span> <span data-ttu-id="b4f6e-124">Til dæmis, ef stefnureglan metur kostnaðarskýrslur fyrir tvítekinn kostnað upp á sömu upphæð, kenni söluaðila og dagsetningu, verður allur kostnaður sem hefur sama gildi í þessum reitum eitt tilvik.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-124">For example, if a policy rule evaluates expense reports for duplicate expenses of the same amount, merchant ID, and date, all expenses that have the same values in those fields will be one case.</span></span> <span data-ttu-id="b4f6e-125">Öll útgjöld sem hafa mismunandi gildi verða aðskilin tilvik.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-125">Any expenses that have different values will be a separate case.</span></span>

<span data-ttu-id="b4f6e-126">Þegar endurskoðunarmál hafa verið mynduð eru þau meðhöndluð með því að nota dæmigert ferli málastjórnunar.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-126">After the audit cases have been generated, they are handled by using the typical processes for case management.</span></span>

## <a name="document-selection-date-ranges"></a><span data-ttu-id="b4f6e-127">Dagsetningabil skjalavals</span><span class="sxs-lookup"><span data-stu-id="b4f6e-127">Document selection date ranges</span></span>
<span data-ttu-id="b4f6e-128">Þegar endurskoðunarstefna er keyrð velur hver regla skjöl af þeirri tilgreindu gerð sem hefur dagsetningu sem er í dagsetningabili skjalavals.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-128">When an audit policy is run, each policy rule selects documents of the specified type that have a date that is in the document selection date range.</span></span> <span data-ttu-id="b4f6e-129">Dagsetningabil skjalavals er tilgreint á síðunni **Aukavalkostir**.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-129">The document selection date range is specified on the **Additional options** page.</span></span> <span data-ttu-id="b4f6e-130">Mörg skjöl hafa fleiri en eina dagsetningu sem tengjast þeim.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-130">Many documents have more than one date associated with them.</span></span> <span data-ttu-id="b4f6e-131">Dagsetningareiturinn sem regla endurskoðunarstefnu notar er tilgreindur á síðunni **Stefnureglugerð**.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-131">The date field that the audit policy rule uses is specified on the **Policy rule type** page.</span></span>

<span data-ttu-id="b4f6e-132">Hér eru nokkrar aðrar leiðir þar sem endurskoðunarreglan notar dagsetningabil skjalavals:</span><span class="sxs-lookup"><span data-stu-id="b4f6e-132">Here are some other ways that an audit policy uses the document selection date range:</span></span>

-   <span data-ttu-id="b4f6e-133">Regla notar útgáfu hverrar stefnureglu sem gildir á síðasta degi dagsetningabils skjalavals.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-133">The policy uses the version of each policy rule that is effective on the last day of the document selection date range.</span></span> <span data-ttu-id="b4f6e-134">Hægt er að skoða virku dagsetningarnar fyrir hverja stefnureglu á listasíðunni **Endurskoðunarstefnur**.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-134">You can view the effective dates for each policy rule on the **Audit policies** list page.</span></span>
-   <span data-ttu-id="b4f6e-135">Stefnan notar fyrirtækishnúta sem eru tengdir reglunni síðasta daginn í dagsetningabili skjalavals.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-135">The policy uses the organization nodes that are associated with the policy on the last day of the document selection date range.</span></span> <span data-ttu-id="b4f6e-136">Aðeins fyrirtækishnútar sem eru tengdir við regluna birtast á listasíðunni **Endurskoðunarstefnur**.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-136">Only the organization nodes that are currently associated with the policy appear on the **Audit policies** list page.</span></span>
-   <span data-ttu-id="b4f6e-137">Fyrir stefnureglur sem eru byggðar á fyrirspurnargerðinni **Listaleit** metur stefnan skjöl fryir vaktaðar einingar sem eru virkar á síðasta degi dagsetningabils skjalavals.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-137">For policy rules that are based on a **List search** query type, the policy evaluates documents for monitored entities that are effective on the last day of the document selection date range.</span></span>


<span data-ttu-id="b4f6e-138">Frekari upplýsingar eru í [Reglur endurskoðunarstefnu](audit-policy-rules.md).</span><span class="sxs-lookup"><span data-stu-id="b4f6e-138">For more information, see [Audit policy rules](audit-policy-rules.md)</span></span>



