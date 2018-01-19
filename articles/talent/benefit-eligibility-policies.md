---
title: "Hæfnireglur fríðinda"
description: "Þessari grein veitir upplýsingar um skilyrði fyrir veitingu fríðinda, sem hjálpar þér að skilgreina hver er hæfur til að fá tilgreind fríðindi."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmBenefitEligibilityDetail, SysPolicyListPage, SysPolicySourceDocumentRuleType
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: 5c0af3d9446b4f8ae80eeb44494f1ef1e6667e55
ms.contentlocale: is-is
ms.lasthandoff: 01/19/2018

---

# <a name="benefit-eligibility-policies"></a><span data-ttu-id="9c5d2-103">Hæfnireglur fríðinda</span><span class="sxs-lookup"><span data-stu-id="9c5d2-103">Benefit eligibility policies</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="9c5d2-104">Þetta efnisatriði veitir upplýsingar um skilyrði fyrir veitingu fríðinda, sem hjálpar þér að skilgreina hver er hæfur til að fá tilgreind fríðindi.</span><span class="sxs-lookup"><span data-stu-id="9c5d2-104">This topic provides information about benefit eligibility policies, which help you define who is eligible for specific benefits.</span></span>

<span data-ttu-id="9c5d2-105">Þegar fríðindi eru stofnuð þarf að ákveða hvaða fríðindi verða tiltæk fyrir hvaða starfsmenn.</span><span class="sxs-lookup"><span data-stu-id="9c5d2-105">When you create benefits, you decide which benefits will be available to which employees.</span></span> <span data-ttu-id="9c5d2-106">Eftirfarandi tafla sýnir dæmi um fríðindi sem gætu verið gerð tiltæk fyrir ákveðna starfsmenn.</span><span class="sxs-lookup"><span data-stu-id="9c5d2-106">The following table shows examples of benefits that you might make available to specific employees.</span></span>

| <span data-ttu-id="9c5d2-107">Fríðindi</span><span class="sxs-lookup"><span data-stu-id="9c5d2-107">Benefit</span></span>          | <span data-ttu-id="9c5d2-108">Hverjir geta fengið fríðindin</span><span class="sxs-lookup"><span data-stu-id="9c5d2-108">Who the benefit is available to</span></span> |
|------------------|---------------------------------|
| <span data-ttu-id="9c5d2-109">Sjúkratryggingar</span><span class="sxs-lookup"><span data-stu-id="9c5d2-109">Health insurance</span></span> | <span data-ttu-id="9c5d2-110">Allir starfsmenn</span><span class="sxs-lookup"><span data-stu-id="9c5d2-110">All employees</span></span>                   |
| <span data-ttu-id="9c5d2-111">Farsími</span><span class="sxs-lookup"><span data-stu-id="9c5d2-111">Mobile phone</span></span>     | <span data-ttu-id="9c5d2-112">Starfsfólk í sölu, yfirmenn</span><span class="sxs-lookup"><span data-stu-id="9c5d2-112">Sales staff, executives</span></span>         |
| <span data-ttu-id="9c5d2-113">Bílastæðapassar</span><span class="sxs-lookup"><span data-stu-id="9c5d2-113">Parking passes</span></span>   | <span data-ttu-id="9c5d2-114">Yfirmenn</span><span class="sxs-lookup"><span data-stu-id="9c5d2-114">Executives</span></span>                      |

<span data-ttu-id="9c5d2-115">Eftirfarandi íhlutir eru notaðir til að stofna hæfnireglur:</span><span class="sxs-lookup"><span data-stu-id="9c5d2-115">The following components in are used to create eligibility policies:</span></span>

-   <span data-ttu-id="9c5d2-116">Stefnureglugerðir</span><span class="sxs-lookup"><span data-stu-id="9c5d2-116">Policy rule types</span></span>
-   <span data-ttu-id="9c5d2-117">Hæfnireglur fríðinda</span><span class="sxs-lookup"><span data-stu-id="9c5d2-117">Benefit eligibility policies</span></span>

<span data-ttu-id="9c5d2-118">Stefnureglugerðir skilgreina fyrirspurnafæribreytur sem eru notaðar þegar sértækar stefnureglur eru þróaðar.</span><span class="sxs-lookup"><span data-stu-id="9c5d2-118">Policy rule types define the query parameters that are used when you develop specific policy rules.</span></span> <span data-ttu-id="9c5d2-119">Eftir að stefnureglugerðir eru stofnaðar er hægt að stofna hæfnireglur fríðinda.</span><span class="sxs-lookup"><span data-stu-id="9c5d2-119">After you create policy rule types, you can create benefit eligibility policies.</span></span> <span data-ttu-id="9c5d2-120">Reglurnar gera mögulegt að stofna safn reglna sem eiga við einn eða fleiri lögaðila.</span><span class="sxs-lookup"><span data-stu-id="9c5d2-120">The policies let you create a collection of rules that apply to one or more legal entities.</span></span> <span data-ttu-id="9c5d2-121">Innan hverrar reglu er hægt að skoða allar stefnureglugerðir sem varða hæfnireglur fríðinda sem voru stofnaðar áður.</span><span class="sxs-lookup"><span data-stu-id="9c5d2-121">Within each policy, you can view any of the benefit eligibility policy rule types that you created earlier.</span></span> 

<span data-ttu-id="9c5d2-122">Þú skilgreinir umfang reglunnar innan stefnunnar.</span><span class="sxs-lookup"><span data-stu-id="9c5d2-122">You define the scope of the rule within the policy.</span></span> <span data-ttu-id="9c5d2-123">Til dæmis, ef þú stofnar stefnureglugerð sem varðar hæfnireglur fríðinda sem kallast **Stjórnandi**, er°hægt að tilgreina hvaða regla er innan þeirrar stefnu.</span><span class="sxs-lookup"><span data-stu-id="9c5d2-123">For example, if you create a benefit eligibility policy rule type that is named **Executive**, you can specify what the rule is within that policy.</span></span> <span data-ttu-id="9c5d2-124">Í þessu dæmi gæti reglan sagt að öll starfsheiti sem innihalda orðið „stjórnandi“ ættu að vera í reglunni.</span><span class="sxs-lookup"><span data-stu-id="9c5d2-124">In this example, the rule might state that any job title that contains the word “executive” should be included in the rule.</span></span> <span data-ttu-id="9c5d2-125">Eftir að færibreytur reglu eða reglna sem eru°innifaldar í stefnunni hafa verið skilgreindar er hægt að tengja tiltekna reglu við fríðindin.</span><span class="sxs-lookup"><span data-stu-id="9c5d2-125">After you've defined the parameters of the rule or rules that are included in the policy, you can assign a specific rule to the benefit.</span></span>

<a name="see-also"></a><span data-ttu-id="9c5d2-126">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="9c5d2-126">See also</span></span>
--------

[<span data-ttu-id="9c5d2-127">Skilgreina og stjórna fríðindaáætlun</span><span class="sxs-lookup"><span data-stu-id="9c5d2-127">Defining and managing a benefit program</span></span>](manage-benefit-program.md)




