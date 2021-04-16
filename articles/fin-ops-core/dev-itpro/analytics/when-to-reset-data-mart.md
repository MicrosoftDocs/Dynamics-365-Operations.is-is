---
title: Hvenær á að endurstilla gagnaskemma
description: Í þessu efnisatriði er farið yfir þær aðstæður sem hugsanlega þarf að bæta með því að endurstilla gagnaskemmu og aðstæður þar sem gagnaskemma er ólíkleg til að hjálpa.
author: jinniew
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2020-12-15
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: c88994a336528650bf8ab6e239c873fa6cd36c46
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5754145"
---
# <a name="when-to-reset-a-data-mart"></a><span data-ttu-id="ca97b-103">Hvenær á að endurstilla gagnaskemma</span><span class="sxs-lookup"><span data-stu-id="ca97b-103">When to reset a data mart</span></span>

<span data-ttu-id="ca97b-104">Að endurstilla gagnaskemmu getur tekið sinn tíma.</span><span class="sxs-lookup"><span data-stu-id="ca97b-104">Resetting a data mart can be time consuming.</span></span> <span data-ttu-id="ca97b-105">Í einhverjum kringumstæðum gæti þessi aðgerð ekki verið rétta lausnin.</span><span class="sxs-lookup"><span data-stu-id="ca97b-105">Depending on the circumstances, this action may not be the solution that's needed.</span></span> <span data-ttu-id="ca97b-106">Í þessu efnisatriði er farið yfir þær aðstæður sem hugsanlega þarf að bæta með því að endurstilla gagnaskemmu, auk aðstæðna þar sem gagnaskemma er ólíkleg til að hjálpa.</span><span class="sxs-lookup"><span data-stu-id="ca97b-106">This topic lists the circumstances that might be improved by resetting a data mart, as well as circumstances in which resetting your data mart is unlikely to help.</span></span>  

## <a name="when-do-you-need-to-do-a-data-mart-reset"></a><span data-ttu-id="ca97b-107">Hvenær þarf að endurstilla gagnaskemmu?</span><span class="sxs-lookup"><span data-stu-id="ca97b-107">When do you need to do a data mart reset?</span></span>
<span data-ttu-id="ca97b-108">Íhugið eftirfarandi spurningar áður en gagnaskemma er endurstillt.</span><span class="sxs-lookup"><span data-stu-id="ca97b-108">Consider the following questions before resetting a data mart.</span></span> <span data-ttu-id="ca97b-109">Ef einni eða fleiri spurningum var svarað játandi gæti það bent til þess að fyrirtækið gæti hagnast á því að láta endurstilla gagnaskemmuna.</span><span class="sxs-lookup"><span data-stu-id="ca97b-109">Answering yes to one or more questions might indicate that your organization can benefit by resetting the data mart.</span></span>

- <span data-ttu-id="ca97b-110">Gagnagrunnur hugbúnaðarins var endurheimtur en gagnagrunnur gagnaskemma var ekki endurheimtur.</span><span class="sxs-lookup"><span data-stu-id="ca97b-110">The application database was restored, but the data mart database was not restored.</span></span>
- <span data-ttu-id="ca97b-111">Þú sérð röng gögn fyrir reikningstímabil sem koma ekki til vegna vandamála varðandi hönnun skýrslunnar.</span><span class="sxs-lookup"><span data-stu-id="ca97b-111">You see incorrect data for an accounting period, which isn't the result of an issue with the report design.</span></span>
- <span data-ttu-id="ca97b-112">Þú sérð röng gögn fyrir reikningstímabil og færslur eru skráðar undir samþættingartilraunir á síðunni **Staða samþættingar** í skýrsluhönnun (ræsið skýrsluhönnun og veljið **Verkfæri > Staða samþættingar**).</span><span class="sxs-lookup"><span data-stu-id="ca97b-112">You see incorrect data for an accounting period, and records are listed under Integration attempts on the **Integration status** page in Report Designer (start the Report Designer and select **Tools > Integration status**).</span></span>
- <span data-ttu-id="ca97b-113">Þjónustutilvik var opnað og tæknimaður hjá notendaþjónustu hefur sagt þér að endurstilla gagnaskemmuna sem hluti af skrefi úrræðaleitar.</span><span class="sxs-lookup"><span data-stu-id="ca97b-113">You've opened a support incident and a support engineer has instructed you to reset the data mart as part of a troubleshooting step.</span></span>
 
## <a name="when-its-not-appropriate-to-reset-a-data-mart"></a><span data-ttu-id="ca97b-114">Hvenær borgar sig ekki að endurstilla gagnaskemmu?</span><span class="sxs-lookup"><span data-stu-id="ca97b-114">When it's not appropriate to reset a data mart?</span></span>
<span data-ttu-id="ca97b-115">Undir sumum kringumstæðum viljum við ekki endurstilla gagnaskemmu.</span><span class="sxs-lookup"><span data-stu-id="ca97b-115">There are some circumstances when we don't recommend resetting a data mart.</span></span> <span data-ttu-id="ca97b-116">Eftirfarandi eru með:</span><span class="sxs-lookup"><span data-stu-id="ca97b-116">These include the following.</span></span> 

- <span data-ttu-id="ca97b-117">Hvenær sem ástæða er ekki tiltekin í þessu efnisatriði.</span><span class="sxs-lookup"><span data-stu-id="ca97b-117">Anytime the reason isn’t listed in this topic.</span></span>
- <span data-ttu-id="ca97b-118">Þú finnur fyrir vandamálum varðandi afköst sem tengjast gagnasamstillingu. Við þessar kringumstæður mun endurstilling gagnaskemmu líklega ekki koma að neinu gagni.</span><span class="sxs-lookup"><span data-stu-id="ca97b-118">You're experiencing performance issues that are associated with a data sync. In this circumstance, resetting the data mart probably won't help.</span></span>
- <span data-ttu-id="ca97b-119">Ef upp koma endurtekin endurstillingarmynstur vegna einhverra af eftirfarandi ástæðum:</span><span class="sxs-lookup"><span data-stu-id="ca97b-119">If you have a recurring reset pattern due to any of the following reasons:</span></span> 
  - <span data-ttu-id="ca97b-120">**Vantar gögn** - Fyrst skal útiloka vandamál varðandi skýrsluhönnun og tímasetningu gagnasamstillingar; til að mynda tekurðu eftir því að staðfestingarvörpun hafi ekki verið keyrð frá því að týnd gögn voru bókuð.</span><span class="sxs-lookup"><span data-stu-id="ca97b-120">**Missing data** - First, eliminate report design issues and data sync timing issues, for example, you observe that the fact map hasn’t run since missing data was posted.</span></span>
  - <span data-ttu-id="ca97b-121">**Föst samþættingarstaða** - Ef samþættingin er hæg eða virðist föst er ólíklegt að endurstilling gagnaskemmunnar muni leysa vandamálið.</span><span class="sxs-lookup"><span data-stu-id="ca97b-121">**Stuck integration state** - If the integration is slow or seems stuck, resetting the data mart is unlikely to resolve the issue.</span></span>
  - <span data-ttu-id="ca97b-122">**Tilraunir til endurstillingar hafa ekki tekist** - Ef margar tilraunir til að ljúka endurstillingu hafa verið reyndar og hafa ekki tekist vegna þess að gögn vantar er mælt með því að opna þjónustutilvik og vinna með tæknimanni hjá notendaþjónustu til að átta sig á vandanum áður en reynt er að endurstilla gagnaskemmuna aftur.</span><span class="sxs-lookup"><span data-stu-id="ca97b-122">**Attempts to reset have been unsuccessful** - If a number of attempts to complete a reset have been made, and have been unsuccessful because of missing data, we recommend opening a support incident and working with a support engineer to analyze your situation before attempting to reset the data mart again.</span></span>
  - <span data-ttu-id="ca97b-123">**Útrunnar skrár** - Útrunnar skrár einar og sér réttlæta ekki endilega endurstillingu gagnaskemmunnar.</span><span class="sxs-lookup"><span data-stu-id="ca97b-123">**Stale records** - Stale records by themselves don't necessarily justify resetting the data mart.</span></span> <span data-ttu-id="ca97b-124">Ef um er að ræða stórt gagnasafn mun endurstillingarferlið taka sinn tíma, en ólíklegt er að það lagi stöðuna.</span><span class="sxs-lookup"><span data-stu-id="ca97b-124">If you have a large data set, the reset process will take some time to run, but is unlikely to result in improvement.</span></span>
 
## <a name="what-a-data-mart-reset-does-not-do"></a><span data-ttu-id="ca97b-125">Það sem endurstilling gagnaskemmu gerir ekki</span><span class="sxs-lookup"><span data-stu-id="ca97b-125">What a data mart reset does not do</span></span>  
- <span data-ttu-id="ca97b-126">Endurstilling hefst aðeins þegar fyrirliggjandi verkum er lokið.</span><span class="sxs-lookup"><span data-stu-id="ca97b-126">A reset will only start when existing tasks are complete.</span></span> <span data-ttu-id="ca97b-127">Þetta tryggir að gömul gögn eru ekki sett inn.</span><span class="sxs-lookup"><span data-stu-id="ca97b-127">This ensures that old data is not inserted.</span></span> <span data-ttu-id="ca97b-128">Á þessu stigi gætu birst skilaboð á borð við: „Ekki var hægt að setja í gang endurstillingu gagnaskemmunnar vegna verks sem er í gangi.</span><span class="sxs-lookup"><span data-stu-id="ca97b-128">At this point you may see a message such as, “The data mart reset was unable to be processed because of an active task.</span></span> <span data-ttu-id="ca97b-129">Reyna skal aftur síðar.</span><span class="sxs-lookup"><span data-stu-id="ca97b-129">Please try again later.”</span></span>
- <span data-ttu-id="ca97b-130">Endurstillingin gerir samþættingarverkin óvirk og eyðir öllum gögnum gagnaskemmunnar.</span><span class="sxs-lookup"><span data-stu-id="ca97b-130">The reset will disable the integration tasks and delete all the data mart data.</span></span> <span data-ttu-id="ca97b-131">Samþætting er virkjuð aftur.</span><span class="sxs-lookup"><span data-stu-id="ca97b-131">The integration is re-enabled.</span></span>

> [!NOTE]
> <span data-ttu-id="ca97b-132">Eftirfarandi punktar tilgreina tvö atriði sem endurstilling gagnaskemmunnar mun *ekki* gera.</span><span class="sxs-lookup"><span data-stu-id="ca97b-132">The following points specify two things that resetting a data mart will *not* do.</span></span> <br>
> - <span data-ttu-id="ca97b-133">Endurstillingar hreinsa ekki hönnun skýrslu.</span><span class="sxs-lookup"><span data-stu-id="ca97b-133">Resets do not clear report designs.</span></span> <br>
> - <span data-ttu-id="ca97b-134">Endurstillingar hreinsa ekki fyrirtækisgögn eða notendagögn nema þau séu valin.</span><span class="sxs-lookup"><span data-stu-id="ca97b-134">Resets do not clear company data or user data unless selected.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]