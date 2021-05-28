---
title: Hvenær á að endurstilla gagnaskemma
description: Í þessu efnisatriði er farið yfir þær aðstæður sem hugsanlega þarf að bæta með því að endurstilla gagnaskemmu og aðstæður þar sem gagnaskemma er ólíkleg til að hjálpa.
author: jinniew
ms.date: 05/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-05-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: bc2c4ee490f3bebd6e7c91609a06f8dfedfcb628
ms.sourcegitcommit: 5916ea2a94ab9af7aac21f0fc44e194d5ce82917
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/07/2021
ms.locfileid: "5988993"
---
# <a name="when-to-reset-a-data-mart"></a><span data-ttu-id="eb8f7-103">Hvenær á að endurstilla gagnaskemma</span><span class="sxs-lookup"><span data-stu-id="eb8f7-103">When to reset a data mart</span></span>

<span data-ttu-id="eb8f7-104">Að endurstilla gagnaskemmu getur tekið sinn tíma.</span><span class="sxs-lookup"><span data-stu-id="eb8f7-104">Resetting a data mart can be time consuming.</span></span> <span data-ttu-id="eb8f7-105">Í einhverjum kringumstæðum gæti þessi aðgerð ekki verið rétta lausnin.</span><span class="sxs-lookup"><span data-stu-id="eb8f7-105">Depending on the circumstances, this action may not be the solution that's needed.</span></span> <span data-ttu-id="eb8f7-106">Í þessu efnisatriði er farið yfir þær aðstæður sem hugsanlega þarf að bæta með því að endurstilla gagnaskemmu, auk aðstæðna þar sem gagnaskemma er ólíkleg til að hjálpa.</span><span class="sxs-lookup"><span data-stu-id="eb8f7-106">This topic lists the circumstances that might be improved by resetting a data mart, as well as circumstances in which resetting your data mart is unlikely to help.</span></span>  

## <a name="when-do-i-need-to-do-a-data-mart-reset"></a><span data-ttu-id="eb8f7-107">Hvenær þarf að endurstilla gagnaskemmu?</span><span class="sxs-lookup"><span data-stu-id="eb8f7-107">When do I need to do a data mart reset?</span></span>
<span data-ttu-id="eb8f7-108">Íhugið eftirfarandi spurningar áður en gagnaskemma er endurstillt.</span><span class="sxs-lookup"><span data-stu-id="eb8f7-108">Consider the following questions before resetting a data mart.</span></span> <span data-ttu-id="eb8f7-109">Ef einni eða fleiri spurningum var svarað játandi gæti það bent til þess að fyrirtækið gæti hagnast á því að láta endurstilla gagnaskemmuna.</span><span class="sxs-lookup"><span data-stu-id="eb8f7-109">Answering yes to one or more questions might indicate that your organization can benefit by resetting the data mart.</span></span>

- <span data-ttu-id="eb8f7-110">Var gagnagrunnur forritsins endurheimtur?</span><span class="sxs-lookup"><span data-stu-id="eb8f7-110">Was the application database restored?</span></span>
- <span data-ttu-id="eb8f7-111">Ef þú opnaðir þjónustutilvik og tæknimaður hjá notendaþjónustu hefur sagt þér að endurstilla gagnaskemmuna sem hluti af skrefi úrræðaleitar.</span><span class="sxs-lookup"><span data-stu-id="eb8f7-111">If you've opened a support incident that and a support engineer has instructed you to reset the data mart as part of a troubleshooting step?</span></span>
 
## <a name="when-is-it-not-appropriate-to-reset-a-data-mart"></a><span data-ttu-id="eb8f7-112">Hvenær borgar sig ekki að endurstilla gagnaskemmu?</span><span class="sxs-lookup"><span data-stu-id="eb8f7-112">When is it not appropriate to reset a data mart?</span></span>
<span data-ttu-id="eb8f7-113">Undir sumum kringumstæðum viljum við ekki endurstilla gagnaskemmu.</span><span class="sxs-lookup"><span data-stu-id="eb8f7-113">There are some circumstances when we don't recommend resetting a data mart.</span></span> <span data-ttu-id="eb8f7-114">Eftirfarandi eru með:</span><span class="sxs-lookup"><span data-stu-id="eb8f7-114">These include the following.</span></span> 

- <span data-ttu-id="eb8f7-115">Þú finnur fyrir vandamálum varðandi afköst sem tengjast gagnasamstillingu.</span><span class="sxs-lookup"><span data-stu-id="eb8f7-115">You're experiencing performance issues that are associated with a data sync.</span></span> 
- <span data-ttu-id="eb8f7-116">Ef upp koma endurtekin endurstillingarmynstur vegna einhverra af eftirfarandi ástæðum:</span><span class="sxs-lookup"><span data-stu-id="eb8f7-116">If you have a recurring reset pattern due to any of the following reasons:</span></span> 
  - <span data-ttu-id="eb8f7-117">**Gögn vantar**</span><span class="sxs-lookup"><span data-stu-id="eb8f7-117">**Missing data**</span></span> 
  - <span data-ttu-id="eb8f7-118">**Föst samþættingarstaða**</span><span class="sxs-lookup"><span data-stu-id="eb8f7-118">**Stuck integration state**</span></span> 
  - <span data-ttu-id="eb8f7-119">**Útrunnar skrár** - Útrunnar skrár einar og sér réttlæta ekki endilega endurstillingu gagnaskemmunnar.</span><span class="sxs-lookup"><span data-stu-id="eb8f7-119">**Stale records** - Stale records by themselves don't necessarily justify resetting the data mart.</span></span> <span data-ttu-id="eb8f7-120">Ef um er að ræða stórt gagnasafn mun endurstillingarferlið taka sinn tíma, en ólíklegt er að það lagi stöðuna.</span><span class="sxs-lookup"><span data-stu-id="eb8f7-120">If you have a large data set, the reset process will take some time to run, but is unlikely to result in improvement.</span></span>
 
## <a name="what-is-a-data-mart-reset"></a><span data-ttu-id="eb8f7-121">Hvað er endurstilling gagnaskemma?</span><span class="sxs-lookup"><span data-stu-id="eb8f7-121">What is a data mart reset?</span></span>
- <span data-ttu-id="eb8f7-122">Endurstilling hefst aðeins þegar fyrirliggjandi verkum er lokið.</span><span class="sxs-lookup"><span data-stu-id="eb8f7-122">A reset will only start when existing tasks are complete.</span></span> <span data-ttu-id="eb8f7-123">Þetta tryggir að gömul gögn eru ekki sett inn.</span><span class="sxs-lookup"><span data-stu-id="eb8f7-123">This ensures that old data is not inserted.</span></span> <span data-ttu-id="eb8f7-124">Á þessu stigi gætu birst skilaboð á borð við: „Ekki var hægt að setja í gang endurstillingu gagnaskemmunnar vegna verks sem er í gangi.</span><span class="sxs-lookup"><span data-stu-id="eb8f7-124">At this point you may see a message such as, “The data mart reset was unable to be processed because of an active task.</span></span> <span data-ttu-id="eb8f7-125">Reyna skal aftur síðar.</span><span class="sxs-lookup"><span data-stu-id="eb8f7-125">Please try again later.”</span></span>
- <span data-ttu-id="eb8f7-126">Endurstillingin gerir samþættingarverkin óvirk og eyðir öllum gögnum gagnaskemmunnar.</span><span class="sxs-lookup"><span data-stu-id="eb8f7-126">The reset will disable the integration tasks and delete all the data mart data.</span></span> <span data-ttu-id="eb8f7-127">Samþætting er virkjuð aftur.</span><span class="sxs-lookup"><span data-stu-id="eb8f7-127">The integration is re-enabled.</span></span>

## <a name="if-i-reset-the-data-mart-will-i-lose-reports-that-ive-already-designed"></a><span data-ttu-id="eb8f7-128">Ef ég endurstilli gagnaskemmu missi ég þá skýrslur sem ég hef þegar hannað?</span><span class="sxs-lookup"><span data-stu-id="eb8f7-128">If I reset the data mart, will I lose reports that I've already designed?</span></span> 
<span data-ttu-id="eb8f7-129">Nei, skýrslurnar þínar eru vistaðar í SQL-töflum sem hafa ekki áhrif á endurstillingu gagnaskemma.</span><span class="sxs-lookup"><span data-stu-id="eb8f7-129">No, your reports are stored in SQL tables that are not impacted by a reset of the data mart.</span></span> <span data-ttu-id="eb8f7-130">Ef þú hefur áhyggjur af að missa skýrslur sem þú hefur hannað geturðu tekið afrit af hönnuninni sem þú vilt ekki missa.</span><span class="sxs-lookup"><span data-stu-id="eb8f7-130">If you are concerned about losing any reports you've designed, you can back up the designs that you don't want to lose.</span></span> <span data-ttu-id="eb8f7-131">Opnið Skýrsluhönnun og farið í **Fyrirtæki > Fyrirtæki > Einingar > Útflutningur** til að afrita þau.</span><span class="sxs-lookup"><span data-stu-id="eb8f7-131">To back them up, open Report Designer and go to **Company > Companies > Building Blocks > Export**.</span></span>
 
## <a name="is-it-necessary-for-all-users-to-exit-the-system-to-reset-the-data-mart"></a><span data-ttu-id="eb8f7-132">Er nauðsynlegt að allir notendur fari úr kerfinu til að endurstilla gagnaskemma?</span><span class="sxs-lookup"><span data-stu-id="eb8f7-132">Is it necessary for all users to exit the system to reset the data mart?</span></span>
<span data-ttu-id="eb8f7-133">Nei, notendur geta haldið áfram að vinna í kerfinu við endurstillingu gagnaskemma.</span><span class="sxs-lookup"><span data-stu-id="eb8f7-133">No, users can continue working in the system during the data mart reset.</span></span> <span data-ttu-id="eb8f7-134">Þeir geta þó ekki fengið aðgang að skýrslum sem búnar voru til með Financial Reporter fyrr en endurstillingunni er lokið.</span><span class="sxs-lookup"><span data-stu-id="eb8f7-134">However, they won’t be able to access any reports that were created with Financial Reporter until the reset is finished.</span></span> 

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
