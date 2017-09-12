---
title: "Brot á endurskoðun og tilvik"
description: "Þessi grein útskýrir hvernig endurskoðunarmál eru stofnuð vegna brota á reglum endurskoðunarstefnu Þetta felur einnig í sér upplýsingar um mismunandi leiðir sem endurskoðunarstefnur nota dagsetningabil skjalavals."
author: ryansandness
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AuditPolicyAdditionalOption, AuditPolicyRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13091
ms.assetid: e0e66c6d-c396-4a9d-b3b6-3641d130fdc0
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 24ee0dbf01208f8decc167e11e84191eaae03edf
ms.contentlocale: is-is
ms.lasthandoff: 08/29/2017

---

# <a name="audit-policy-violations-and-cases"></a><span data-ttu-id="5438c-104">Brot á endurskoðun og tilvik</span><span class="sxs-lookup"><span data-stu-id="5438c-104">Audit policy violations and cases</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="5438c-105">Þessi grein útskýrir hvernig endurskoðunarmál eru stofnuð vegna brota á reglum endurskoðunarstefnu</span><span class="sxs-lookup"><span data-stu-id="5438c-105">The article explains how audit cases are generated from violations of audit policy rules.</span></span> <span data-ttu-id="5438c-106">Þetta felur einnig í sér upplýsingar um mismunandi leiðir sem endurskoðunarstefnur nota dagsetningabil skjalavals.</span><span class="sxs-lookup"><span data-stu-id="5438c-106">It also includes information about the various ways that audit policies use the document selection date range.</span></span>

<a name="how-audit-cases-are-generated"></a><span data-ttu-id="5438c-107">Hvernig endurskoðunarmál eru stofnuð</span><span class="sxs-lookup"><span data-stu-id="5438c-107">How audit cases are generated</span></span>
-----------------------------

<span data-ttu-id="5438c-108">Endurskoðunarstefnur eru notaðar til að auðkenna kostnaðarskýrslur, innkaupapantanir og reikninga lánardrottna sem ekki samræmast viðskiptareglum sem þú tilgreinir og skilgreina sem reglur endurskoðunarstefnu.</span><span class="sxs-lookup"><span data-stu-id="5438c-108">Audit policies are used to identify expense reports, purchase orders, and vendor invoices that don't comply with business rules that you define and configure as audit policy rules.</span></span> 

<span data-ttu-id="5438c-109">Endurskoðunarreglur eru keyrðar í runuham.</span><span class="sxs-lookup"><span data-stu-id="5438c-109">Audit policies are run in batch mode.</span></span> <span data-ttu-id="5438c-110">Þegar endurskoðunarregla er keyrð eru allar stefnureglur sem eru hluti þeirrar reglu keyrðar á sama tíma.</span><span class="sxs-lookup"><span data-stu-id="5438c-110">When you run an audit policy, all the policy rules that are part of that policy are run at the same time.</span></span>

<span data-ttu-id="5438c-111">Hver stefnuregla metur safn skjala.</span><span class="sxs-lookup"><span data-stu-id="5438c-111">Each policy rule evaluates a set of documents.</span></span> <span data-ttu-id="5438c-112">Stefnureglan velur skjöl sem eru í dagsetningabili skjalavals og sem samsvara tilgreindum skilyrðum.</span><span class="sxs-lookup"><span data-stu-id="5438c-112">The policy rule selects documents that are in the document selection date range and that match the specified criteria.</span></span> <span data-ttu-id="5438c-113">Til dæmis gæti ein stefnuregla valið kostnaðarskýrslur sem hafa máltíðir sem fara fram yfir 50,00.</span><span class="sxs-lookup"><span data-stu-id="5438c-113">For example, one policy rule might select expense reports that have meals that exceed 50.00.</span></span> <span data-ttu-id="5438c-114">Önnur stefnuregla gæti valið reikninga lánardrottna sem eru til greiðslu til tiltekins lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="5438c-114">Another policy rule might select vendor invoices that are payable to a specific vendor.</span></span> <span data-ttu-id="5438c-115">Fyrir hvert skjal sem er valið í safninu er brot myndað.</span><span class="sxs-lookup"><span data-stu-id="5438c-115">For each document that is selected in the set, a violation is generated.</span></span> <span data-ttu-id="5438c-116">Það brot er færsla um að tiltekið skjal, eins og reikningur 12345, samræmist ekki stefnureglunni.</span><span class="sxs-lookup"><span data-stu-id="5438c-116">That violation is a record that a particular document, such as invoice 12345, doesn't comply with the policy rule.</span></span> 

<span data-ttu-id="5438c-117">Margar endurskoðunarfærslur eru flokkaðar saman og tengdar endurskoðunarmálum.</span><span class="sxs-lookup"><span data-stu-id="5438c-117">Multiple audit violation records are grouped together and associated with audit cases.</span></span> <span data-ttu-id="5438c-118">Að sjálfgefnu eru mál fyrir hverja endurskoðunarreglu flokkuð eftir reglu endurskoðunarstefnu.</span><span class="sxs-lookup"><span data-stu-id="5438c-118">By default, cases for each audit policy are grouped by audit policy rule.</span></span> <span data-ttu-id="5438c-119">Ef þess er óskað er hægt að velja önnur flokkunarskilyrði með því að nota síðuna **Flokkunarskilyrði tilvika**.</span><span class="sxs-lookup"><span data-stu-id="5438c-119">If you prefer, you can select other grouping criteria by using the **Case grouping criteria** page.</span></span> <span data-ttu-id="5438c-120">Til dæmis er hægt að flokka kostnaðarhausa eftir verkkenni og reikningum lánardrottna eftir lánardrottnalykli.</span><span class="sxs-lookup"><span data-stu-id="5438c-120">For example, you can group expense headers by project ID and vendor invoices by vendor account.</span></span> <span data-ttu-id="5438c-121">Í þessu tilfelli verða öll brot á kostnaðarhaus sem hafa sama verkkennið flokkuð í sama tilvikið og allir reikningar lánardrottins sem hafa sama lánardrottnalykil verða flokkaðar í sama tilvikið.</span><span class="sxs-lookup"><span data-stu-id="5438c-121">In this case, all expense header violations that have the same project ID will be grouped in the same case, and all vendor invoices that have the same vendor account will be grouped in the same case.</span></span> 

> [!NOTE]
> <span data-ttu-id="5438c-122">Fyrir reglur endurskoðunarstefnu sem byggja á fyrirspurnartegundinni **Tvítekning** eru brot ekki flokkuð eftir stefnureglu eða skilyrðunum sem eru tilgreind á síðunni **Flokkunarskilyrði tilvika**.</span><span class="sxs-lookup"><span data-stu-id="5438c-122">For audit policy rules that are based on a **Duplicate** query type, violations aren't grouped by policy rule or by the criteria that are specified on the **Case grouping criteria** page.</span></span> <span data-ttu-id="5438c-123">Þessi í stað eru þau flokkuð eftir þeim skilyrðum sem eru búin til í reglu endurskoðunarstefnu.</span><span class="sxs-lookup"><span data-stu-id="5438c-123">Instead, they are grouped by the criteria that are built into the audit policy rule.</span></span> <span data-ttu-id="5438c-124">Til dæmis, ef stefnureglan metur kostnaðarskýrslur fyrir tvítekinn kostnað upp á sömu upphæð, kenni söluaðila og dagsetningu, verður allur kostnaður sem hefur sama gildi í þessum reitum eitt tilvik.</span><span class="sxs-lookup"><span data-stu-id="5438c-124">For example, if a policy rule evaluates expense reports for duplicate expenses of the same amount, merchant ID, and date, all expenses that have the same values in those fields will be one case.</span></span> <span data-ttu-id="5438c-125">Öll útgjöld sem hafa mismunandi gildi verða aðskilin tilvik.</span><span class="sxs-lookup"><span data-stu-id="5438c-125">Any expenses that have different values will be a separate case.</span></span>

<span data-ttu-id="5438c-126">Þegar endurskoðunarmál hafa verið mynduð eru þau meðhöndluð með því að nota dæmigert ferli málastjórnunar.</span><span class="sxs-lookup"><span data-stu-id="5438c-126">After the audit cases have been generated, they are handled by using the typical processes for case management.</span></span>

## <a name="document-selection-date-ranges"></a><span data-ttu-id="5438c-127">Dagsetningabil skjalavals</span><span class="sxs-lookup"><span data-stu-id="5438c-127">Document selection date ranges</span></span>
<span data-ttu-id="5438c-128">Þegar endurskoðunarstefna er keyrð velur hver regla skjöl af þeirri tilgreindu gerð sem hefur dagsetningu sem er í dagsetningabili skjalavals.</span><span class="sxs-lookup"><span data-stu-id="5438c-128">When an audit policy is run, each policy rule selects documents of the specified type that have a date that is in the document selection date range.</span></span> <span data-ttu-id="5438c-129">Dagsetningabil skjalavals er tilgreint á síðunni **Aukavalkostir**.</span><span class="sxs-lookup"><span data-stu-id="5438c-129">The document selection date range is specified on the **Additional options** page.</span></span> <span data-ttu-id="5438c-130">Mörg skjöl hafa fleiri en eina dagsetningu sem tengjast þeim.</span><span class="sxs-lookup"><span data-stu-id="5438c-130">Many documents have more than one date associated with them.</span></span> <span data-ttu-id="5438c-131">Dagsetningareiturinn sem regla endurskoðunarstefnu notar er tilgreindur á síðunni **Stefnureglugerð**.</span><span class="sxs-lookup"><span data-stu-id="5438c-131">The date field that the audit policy rule uses is specified on the **Policy rule type** page.</span></span>

<span data-ttu-id="5438c-132">Hér eru nokkrar aðrar leiðir þar sem endurskoðunarreglan notar dagsetningabil skjalavals:</span><span class="sxs-lookup"><span data-stu-id="5438c-132">Here are some other ways that an audit policy uses the document selection date range:</span></span>

-   <span data-ttu-id="5438c-133">Regla notar útgáfu hverrar stefnureglu sem gildir á síðasta degi dagsetningabils skjalavals.</span><span class="sxs-lookup"><span data-stu-id="5438c-133">The policy uses the version of each policy rule that is effective on the last day of the document selection date range.</span></span> <span data-ttu-id="5438c-134">Hægt er að skoða virku dagsetningarnar fyrir hverja stefnureglu á listasíðunni **Endurskoðunarstefnur**.</span><span class="sxs-lookup"><span data-stu-id="5438c-134">You can view the effective dates for each policy rule on the **Audit policies** list page.</span></span>
-   <span data-ttu-id="5438c-135">Stefnan notar fyrirtækishnúta sem eru tengdir reglunni síðasta daginn í dagsetningabili skjalavals.</span><span class="sxs-lookup"><span data-stu-id="5438c-135">The policy uses the organization nodes that are associated with the policy on the last day of the document selection date range.</span></span> <span data-ttu-id="5438c-136">Aðeins fyrirtækishnútar sem eru tengdir við regluna birtast á listasíðunni **Endurskoðunarstefnur**.</span><span class="sxs-lookup"><span data-stu-id="5438c-136">Only the organization nodes that are currently associated with the policy appear on the **Audit policies** list page.</span></span>
-   <span data-ttu-id="5438c-137">Fyrir stefnureglur sem eru byggðar á fyrirspurnargerðinni **Listaleit** metur stefnan skjöl fryir vaktaðar einingar sem eru virkar á síðasta degi dagsetningabils skjalavals.</span><span class="sxs-lookup"><span data-stu-id="5438c-137">For policy rules that are based on a **List search** query type, the policy evaluates documents for monitored entities that are effective on the last day of the document selection date range.</span></span>


<span data-ttu-id="5438c-138">Frekari upplýsingar eru í [Reglur endurskoðunarstefnu](audit-policy-rules.md).</span><span class="sxs-lookup"><span data-stu-id="5438c-138">For more information, see [Audit policy rules](audit-policy-rules.md)</span></span>




