---
title: Hvað er nýtt eða breytt í Dynamics 365 for Talent (7. febrúar 2019)
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 02/07/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-02-07
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 23386d04fac5a41682d3ced448ce07e6729def3c
ms.sourcegitcommit: b3b21795f36e5852ffe18200d6fe0b93363b1cbd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/08/2019
ms.locfileid: "377741"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-february-7-2019"></a><span data-ttu-id="b596a-103">Hvað er nýtt eða breytt í Dynamics 365 for Talent (7. febrúar 2019)</span><span class="sxs-lookup"><span data-stu-id="b596a-103">What's new or changed in Dynamics 365 for Talent (February 7, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b596a-104">Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Talent.</span><span class="sxs-lookup"><span data-stu-id="b596a-104">This topic describes features that are either new or changed in Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="b596a-105">Breytingar í Attract</span><span class="sxs-lookup"><span data-stu-id="b596a-105">Changes in Attract</span></span>

### <a name="interview-scheduling-enhancements"></a><span data-ttu-id="b596a-106">Endurbætur á viðtalsáætlun</span><span class="sxs-lookup"><span data-stu-id="b596a-106">Interview scheduling enhancements</span></span>
<span data-ttu-id="b596a-107">Endurbætur hafa verið gerðar á allri upplifun viðtalsáætlunar.</span><span class="sxs-lookup"><span data-stu-id="b596a-107">Improvements have been made to the end-to-end interview scheduling experience.</span></span> <span data-ttu-id="b596a-108">Þú getur nú séð lausa tíma á dagatali fyrir umsækjanda innan fyrirtækisins og notað dagatalið hans til að stinga upp á tímasetningu.</span><span class="sxs-lookup"><span data-stu-id="b596a-108">You can now see the calendar availability of an internal candidate and use the internal candidate’s calendar for schedule recommendations.</span></span> <span data-ttu-id="b596a-109">Nánari upplýsingar er að finna í [Viðtalsáætlun og endurgjöf](interview-scheduling-feedback.md).</span><span class="sxs-lookup"><span data-stu-id="b596a-109">For more information, see [Interview scheduling and feedback](interview-scheduling-feedback.md).</span></span>

### <a name="job-posting-to-linkedin--company-mismatch-issue-fixed"></a><span data-ttu-id="b596a-110">Starfsauglýsing á LinkedIn - skekkja fyrirtækis lagfærð</span><span class="sxs-lookup"><span data-stu-id="b596a-110">Job posting to LinkedIn – company mismatch issue fixed</span></span>
<span data-ttu-id="b596a-111">Vandamál hefur verið lagað þar sem störf auglýst á LinkedIn úr Attract birtust undir röngu fyrirtækisheiti.</span><span class="sxs-lookup"><span data-stu-id="b596a-111">An issue has been fixed where jobs posted to LinkedIn from Attract were appearing under the wrong company name.</span></span> <span data-ttu-id="b596a-112">Nánari upplýsingar er að finna í [Búðu til, samþykkja og auglýsa störf í Attract](creating-jobs-attract.md).</span><span class="sxs-lookup"><span data-stu-id="b596a-112">For more information, see [Create, approve, and post jobs in Attract](creating-jobs-attract.md).</span></span>

### <a name="career-site-url-displayed-in-admin-settings"></a><span data-ttu-id="b596a-113">Vefslóð starfatorgsins sýnd í stjórnandastillingum</span><span class="sxs-lookup"><span data-stu-id="b596a-113">Career site URL displayed in Admin settings</span></span>
<span data-ttu-id="b596a-114">Vefslóð á heimasíðu starfatorgsins er nú sýnd í **Stjórnandastillingar** undir **Stjórnun starfatorgs**.</span><span class="sxs-lookup"><span data-stu-id="b596a-114">The career site home page URL is now displayed in **Admin Settings** under **Career Site management**.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="b596a-115">Breytingar í Core HR</span><span class="sxs-lookup"><span data-stu-id="b596a-115">Changes in Core HR</span></span>

<span data-ttu-id="b596a-116">**Smíði 8.1.2134**</span><span class="sxs-lookup"><span data-stu-id="b596a-116">**Build 8.1.2134**</span></span>

### <a name="multiple-compensation-levels-supported-on-jobs"></a><span data-ttu-id="b596a-117">Mörg launastig studd í störfum</span><span class="sxs-lookup"><span data-stu-id="b596a-117">Multiple compensation levels supported on jobs</span></span>
<span data-ttu-id="b596a-118">Þessi breyting gerir kleift að skilgreina fleiri en eitt launastig í starfi, sem virkjar bil á föstum launum starfsmanns sem kunna að vera mismunandi milli áætlana þegar sama starfið er notað.</span><span class="sxs-lookup"><span data-stu-id="b596a-118">This change allows for more than one compensation level to be defined on a job, enabling employee fixed compensation ranges which may differ between plans when using the same job.</span></span> 

<span data-ttu-id="b596a-119">Dæmi:</span><span class="sxs-lookup"><span data-stu-id="b596a-119">For example:</span></span>    
<span data-ttu-id="b596a-120">*Starf* - Kerfisstjóri *Tengd launastig:* B1 og B2 - Hvert stig er með skilgreint bil fyrir gildin.</span><span class="sxs-lookup"><span data-stu-id="b596a-120">*Job* - Account Manager *Associated compensation levels:* B1 and B2 - Each level has a defined range of values.</span></span> <span data-ttu-id="b596a-121">B1 = Min 50.000, Mid 60.000, Max 75.000 og B2 = Min 65.000, Mid 74.000, Max 85.000.</span><span class="sxs-lookup"><span data-stu-id="b596a-121">B1 = Min 50,000, Mid 60,000, Max 75,000 and B2 = Min 65,000, Mid 74,000, Max 85,000.</span></span> <span data-ttu-id="b596a-122">Þegar föst laun eru búin til fyrir starfsmenn, byggt á skilgreindum hæfnisreglum, getur sérhver föst laun nú bent á sama starfið og mismunandi stig starfsins.</span><span class="sxs-lookup"><span data-stu-id="b596a-122">When creating fixed compensation for employees, based on the eligibility rules defined, each fixed plan can now point to the same job and to different levels on the job.</span></span> <span data-ttu-id="b596a-123">Þetta leyfir skilgreiningar á áætlunum á mismunandi svæðum/fyrirtækjum og að benda á sama starfið, en mismunandi bil, án þess að afrita störfin til að gera grein fyrir þessum mismun.</span><span class="sxs-lookup"><span data-stu-id="b596a-123">This allows for plans to be defined in different regions/companies and point to the same job but different ranges without duplicating jobs to account for these differences.</span></span>

### <a name="compensation-level-field-has-been-added-to-the-employee-fixed-compensation-entity"></a><span data-ttu-id="b596a-124">Svæði fyrir launastig hefur verið bætt við eininguna fyrir föst laun starfsmanns</span><span class="sxs-lookup"><span data-stu-id="b596a-124">Compensation level field has been added to the Employee fixed compensation entity</span></span> 
<span data-ttu-id="b596a-125">Með þessari uppfærslu hefur einingin fyrir föst laun starfsmanns verið uppfærð til að innihalda svæðið **Launastig**.</span><span class="sxs-lookup"><span data-stu-id="b596a-125">With this update, the employee fixed compensation entity has been updated to include the **Compensation level** field.</span></span> <span data-ttu-id="b596a-126">Þessi viðbót gerir það auðveldara að uppfæra fyrirkomulag fastra launa starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="b596a-126">This addition makes it easier to update employee fixed compensation plans.</span></span> 

### <a name="update-job-family-when-updating-and-creating-new-positions"></a><span data-ttu-id="b596a-127">Uppfærðu starfasafn þegar nýjar stöður eru uppfærðar eða búnar til</span><span class="sxs-lookup"><span data-stu-id="b596a-127">Update Job family when updating and creating new positions</span></span>
<span data-ttu-id="b596a-128">Þegar starfi er breytt fyrir stöðu, verður **Starfasafn** nú fá sjálfgildi byggt á völdu starfi.</span><span class="sxs-lookup"><span data-stu-id="b596a-128">When changing the job on a position, **Job family** will now default based on the job selected.</span></span>

### <a name="performance-improvements-when-rendering-workspaces"></a><span data-ttu-id="b596a-129">Bætt afköst þegar vinnusvæði birtast</span><span class="sxs-lookup"><span data-stu-id="b596a-129">Performance improvements when rendering workspaces</span></span>
<span data-ttu-id="b596a-130">Greiningarflipar á vinnusvæðum munu nú eingöngu hlaðast þegar þessar síður eru opnaðar.</span><span class="sxs-lookup"><span data-stu-id="b596a-130">Analytics tabs on workspaces will now load only when accessing those pages.</span></span> <span data-ttu-id="b596a-131">Vísir birtist meðan á fyrstu birtingu á síðunni efst í vinstra horni síðunnar.</span><span class="sxs-lookup"><span data-stu-id="b596a-131">An indicator will display during the initial rendering of the page in the upper-left corner of the page.</span></span>
