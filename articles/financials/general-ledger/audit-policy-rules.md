---
title: "Reglur endurskoðunarstefnu"
description: "Hægt er að nota endurskoðunarreglur til að meta kostnaðarskýrslur, reikninga lánardrottna og innkaupapantanir til að tryggja að þeir samræmast stefnureglur sem eru stofnaðar. Allar reglur sem eru tengd við endurskoðunarstefnu eru rekin í runuham, samkvæmt áætlun sem þú tilgreinir.  Hver stefnuregla er tilvik af stefnureglugerð. Fyrir hverja stefnureglugerð aðeins einn stefnureglu getur verið virk í einu."
author: ryansandness
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AuditPolicyAdditionalOption, AuditPolicyRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 12991
ms.assetid: 8d787017-71dc-418f-b8c2-4ea9763d9978
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 6bebe9ce83c4b979ffbb7c86ef67ad03a650e0c2
ms.contentlocale: is-is
ms.lasthandoff: 05/08/2018

---

# <a name="audit-policy-rules"></a><span data-ttu-id="d1268-106">Reglur endurskoðunarstefnu</span><span class="sxs-lookup"><span data-stu-id="d1268-106">Audit policy rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d1268-107">Hægt er að nota endurskoðunarreglur til að meta kostnaðarskýrslur, reikninga lánardrottna og innkaupapantanir til að tryggja að þeir samræmast stefnureglur sem eru stofnaðar.</span><span class="sxs-lookup"><span data-stu-id="d1268-107">You can use audit policies to evaluate expense reports, vendor invoices, and purchase orders to make sure that they comply with policy rules that you create.</span></span> <span data-ttu-id="d1268-108">Allar reglur sem eru tengd við endurskoðunarstefnu eru rekin í runuham, samkvæmt áætlun sem þú tilgreinir.</span><span class="sxs-lookup"><span data-stu-id="d1268-108">All of the rules that are associated with an audit policy are run in batch mode, according to a schedule that you specify.</span></span>  <span data-ttu-id="d1268-109">Hver stefnuregla er tilvik af stefnureglugerð.</span><span class="sxs-lookup"><span data-stu-id="d1268-109">Each policy rule is an instance of a policy rule type.</span></span> <span data-ttu-id="d1268-110">Fyrir hverja stefnureglugerð aðeins einn stefnureglu getur verið virk í einu.</span><span class="sxs-lookup"><span data-stu-id="d1268-110">For each policy rule type, only one policy rule can be active at a time.</span></span> 

<a name="queries-and-query-types"></a><span data-ttu-id="d1268-111">Fyrirspurnir og gerðir fyrirspurna</span><span class="sxs-lookup"><span data-stu-id="d1268-111">Queries and query types</span></span>
-----------------------

<span data-ttu-id="d1268-112">Þegar regla endurskoðunarstefnu er stofnuð þarf fyrst að velja stefnureglugerð.</span><span class="sxs-lookup"><span data-stu-id="d1268-112">When you create an audit policy rule, you first select a policy rule type.</span></span> <span data-ttu-id="d1268-113">Gerð reglu tilgreinir fyrirspurn Hugbúnaðarhlutatrénu (AOT) til að nota sem upphafspunkt fyrir þá reglu.</span><span class="sxs-lookup"><span data-stu-id="d1268-113">The policy rule type specifies the Application Object Tree (AOT) query to use as the starting point for creating the policy rule.</span></span> <span data-ttu-id="d1268-114">Það skilgreinir einnig fyrirspurn ferðar til nota fyrir stefnureglu.</span><span class="sxs-lookup"><span data-stu-id="d1268-114">It also specifies the query type to use for the policy rule.</span></span> <span data-ttu-id="d1268-115">Fyrirspurnin ákvarðar upprunaskjalið sem metur síðan til stefnuregluna.</span><span class="sxs-lookup"><span data-stu-id="d1268-115">The query determines the source document that the policy rule evaluates.</span></span> <span data-ttu-id="d1268-116">Það skilgreinir einnig reiti í upprunaskjali sem auðkenna bæði lögaðila og dagsetningu til að nota þegar skjöl eru valin til endurskoðunar.</span><span class="sxs-lookup"><span data-stu-id="d1268-116">It also specifies the fields in the source document that identify both the legal entity and the date to use when documents are selected for audit.</span></span> <span data-ttu-id="d1268-117">Gerð fyrirspurnar stýrir sjálfgefið svæði í fyrirspurnarskjámynd og í síðunni regla endurskoðunarstefnu.</span><span class="sxs-lookup"><span data-stu-id="d1268-117">The query type controls the default fields in the query page and in the Audit policy rule page.</span></span> <span data-ttu-id="d1268-118">Eftirfarandi tafla sýnir gerðir fyrirspurn sem er tiltækt fyrir reglur endurskoðunarstefnu.</span><span class="sxs-lookup"><span data-stu-id="d1268-118">The following table shows the query types that are available for audit policy rules.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d1268-119">Gerð fyrirspurnar</span><span class="sxs-lookup"><span data-stu-id="d1268-119">Query type</span></span></th>
<th><span data-ttu-id="d1268-120">Tilgangur</span><span class="sxs-lookup"><span data-stu-id="d1268-120">Purpose</span></span></th>
<th><span data-ttu-id="d1268-121">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="d1268-121">More information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d1268-122">Skilyrðisbundið</span><span class="sxs-lookup"><span data-stu-id="d1268-122">Conditional</span></span></td>
<td><span data-ttu-id="d1268-123">Meta uppruna eigindir skjals gagnvart tilgreindum gildum.</span><span class="sxs-lookup"><span data-stu-id="d1268-123">Evaluate source document attributes against specified values.</span></span></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d1268-124">Samanlagt</span><span class="sxs-lookup"><span data-stu-id="d1268-124">Aggregate</span></span></td>
<td><span data-ttu-id="d1268-125">Meta margar upprunaskjöl eða línur upprunaskjals gagnvart stefnureglu með söfnun tölulegt gildi.</span><span class="sxs-lookup"><span data-stu-id="d1268-125">Evaluate multiple source documents or source document lines against a policy rule by aggregating numeric values.</span></span></td>
<td></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d1268-126">Sýnishorn</span><span class="sxs-lookup"><span data-stu-id="d1268-126">Sampling</span></span></td>
<td><span data-ttu-id="d1268-127">Veljið handahófi tilgreindri prósentu af upprunaskjöl til að meta brot á reglum.</span><span class="sxs-lookup"><span data-stu-id="d1268-127">Randomly select a specified percentage of the source documents to evaluate for policy violations.</span></span></td>
<td><span data-ttu-id="d1268-128">Þegar þessi valkostur er valinn, skaltu nota síðuna regla endurskoðunarstefnu til að tilgreina hlutfall skjala til að velja af handahófi fyrir endurskoðun.</span><span class="sxs-lookup"><span data-stu-id="d1268-128">When you select this option, use the Audit policy rule page to specify the percentage of documents to randomly select for audit.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d1268-129">Afrita</span><span class="sxs-lookup"><span data-stu-id="d1268-129">Duplicate</span></span></td>
<td><span data-ttu-id="d1268-130">Meta upprunaskjöl til að ákvarða hvort þau innihalda tvíteknar færslur í tilgreindu svæðin.</span><span class="sxs-lookup"><span data-stu-id="d1268-130">Evaluate source documents to determine whether they contain duplicate entries in specified fields.</span></span></td>
<td><span data-ttu-id="d1268-131">Þegar þessi valkostur er valinn, skaltu nota síðuna regla endurskoðunarstefnu til að tilgreina fjölda daga til að bæta við upphaf dagsetningabils skjalavals þegar skjöl eru metin fyrir tvíteknar færslur.</span><span class="sxs-lookup"><span data-stu-id="d1268-131">When you select this option, use the Audit policy rule page to specify the number of days to add to the start of the document selection date range when documents are evaluated for duplicate entries.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d1268-132">Listaleit</span><span class="sxs-lookup"><span data-stu-id="d1268-132">List search</span></span></td>
<td><span data-ttu-id="d1268-133">Meta upprunaskjöl fyrir tilteknar einingar.</span><span class="sxs-lookup"><span data-stu-id="d1268-133">Evaluate source documents for specific entities.</span></span></td>
<td><span data-ttu-id="d1268-134">Rót skjalið fyrirspurnarinnar tilgreinir skjalið sem er endurskoðuð.</span><span class="sxs-lookup"><span data-stu-id="d1268-134">The root document of the query defines the document that is being audited.</span></span> <span data-ttu-id="d1268-135">Fyrirspurnin verður að vera listafyrirspurn sem inniheldur tilvísun í the dirpartytable-töflu.</span><span class="sxs-lookup"><span data-stu-id="d1268-135">The query must be a list query that includes a reference to the dirpartytable table.</span></span> <span data-ttu-id="d1268-136">Hægt er að nota þennan valkost aðeins með eftirfarandi fyrirspurnir AOT:</span><span class="sxs-lookup"><span data-stu-id="d1268-136">This option can be used only with the following AOT queries:</span></span>
<ul>
<li><span data-ttu-id="d1268-137"><span class="ui">AuditPolicyExpenseList</span> (Kostnaðarskýrsla vaktaðra starfsmanna)</span><span class="sxs-lookup"><span data-stu-id="d1268-137"><span class="ui">AuditPolicyExpenseList</span> (Expense report monitored employees)</span></span></li>
<li><span data-ttu-id="d1268-138"><span class="ui">AuditPolicyPurchList</span> (Innkaupapöntun vaktaðra lánardrottna)</span><span class="sxs-lookup"><span data-stu-id="d1268-138"><span class="ui">AuditPolicyPurchList</span> (Purchase order monitored vendors)</span></span></li>
<li><span data-ttu-id="d1268-139"><span class="ui">AuditPolicyVendInvoiceList</span> (reikningur vaktaðra lánardrottna)</span><span class="sxs-lookup"><span data-stu-id="d1268-139"><span class="ui">AuditPolicyVendInvoiceList</span> (Vendor invoice monitored vendors)</span></span></li>
</ul>
<span data-ttu-id="d1268-140">Þegar þessi valkostur er valinn skal tilgreina vaktaðar einingar í síðunni regla endurskoðunarstefnu.</span><span class="sxs-lookup"><span data-stu-id="d1268-140">When you select this option, specify the monitored entities in the Audit policy rule page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d1268-141">Lykilorðaleit</span><span class="sxs-lookup"><span data-stu-id="d1268-141">Keyword search</span></span></td>
<td><span data-ttu-id="d1268-142">Meta upprunaskjöl til að ákvarða hvort þau innihalda tiltekin orð.</span><span class="sxs-lookup"><span data-stu-id="d1268-142">Evaluate source documents to determine whether they contain certain words.</span></span></td>
<td><span data-ttu-id="d1268-143">Þegar þessi valkostur er valinn skal færa inn orð til að leita að í regla endurskoðunarstefnu síða.</span><span class="sxs-lookup"><span data-stu-id="d1268-143">When you select this option, enter the words to look for in the Audit policy rule page.</span></span> <span data-ttu-id="d1268-144">regla endurskoðunarstefnu síða  inniheldur einnig valkosti sem leyfa þér að tilgreina töflur og reiti til að meta fyrir orð sem þú slóst inn.</span><span class="sxs-lookup"><span data-stu-id="d1268-144">The Audit policy rule page also includes options that let you specify the tables and fields to evaluate for the words you entered.</span></span></td>
</tr>
</tbody>
</table>

## <a name="common-parameters"></a><span data-ttu-id="d1268-145">Algengar færibreytur</span><span class="sxs-lookup"><span data-stu-id="d1268-145">Common parameters</span></span>
<span data-ttu-id="d1268-146">Allar stefnureglur um tiltekna endurskoðunarstefnu deila sömu runufæribreytur og sama dagsetningarbil skjalavals.</span><span class="sxs-lookup"><span data-stu-id="d1268-146">All of the policy rules for a particular audit policy share the same batch parameters and the same document selection date range.</span></span> <span data-ttu-id="d1268-147">Þessar færibreytur eru tilgreindar fyrir reglu í á Aukavalkostir síða.</span><span class="sxs-lookup"><span data-stu-id="d1268-147">These parameters are specified for the policy in the Additional options page.</span></span>



<a name="additional-resources"></a><span data-ttu-id="d1268-148">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="d1268-148">Additional resources</span></span>
--------

<span data-ttu-id="d1268-149">[Brot á endurskoðunarstefnu og tilvik](audit-policy-violations-cases.md)
[Skilgreina endurskoðunarstefnu fyrir upprunaskjöl](tasks/define-audit-policies-source-documents.md)</span><span class="sxs-lookup"><span data-stu-id="d1268-149">[Audit policy violations and cases](audit-policy-violations-cases.md)
[Define audit policies for source documents](tasks/define-audit-policies-source-documents.md)</span></span>



