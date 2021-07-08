---
title: Algengar spurningar um endurstillingar gagnaskemmu
description: Þetta efnisatriði veitir svör við nokkrum algengum spurningum um endurstillingar gagnaskemmu.
author: jinniew
ms.date: 06/09/2021
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
ms.openlocfilehash: 7cd96c7bc698986ef1ef07ca88479a3d49f22924
ms.sourcegitcommit: ecabf43282a3e55f1db40341aa3f3c7950b9e94c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/16/2021
ms.locfileid: "6266610"
---
# <a name="data-mart-resets-faq"></a><span data-ttu-id="25016-103">Algengar spurningar um endurstillingar gagnaskemmu</span><span class="sxs-lookup"><span data-stu-id="25016-103">Data mart resets FAQ</span></span>

<span data-ttu-id="25016-104">Þetta efnisatriði veitir svör við nokkrum algengum spurningum um endurstillingar gagnaskemmu.</span><span class="sxs-lookup"><span data-stu-id="25016-104">This topic provides answers to some frequently asked questions about data mart resets.</span></span> <span data-ttu-id="25016-105">Endurstilling á gagnaskemmunni getur verið tímafrekt ferli og það fer eftir aðstæðum hvort það sé rétta lausnin.</span><span class="sxs-lookup"><span data-stu-id="25016-105">A reset of the data mart can be a time-consuming process and, depending on the circumstances, might not be the solution that is required.</span></span> <span data-ttu-id="25016-106">Í þessu efnisatriði er því að finna upplýsingar um aðstæður þar sem endurstilling gagnaskemmu gæti hjálpað og einnig aðstæður þar sem ólíklegt er að hún komi að gagni.</span><span class="sxs-lookup"><span data-stu-id="25016-106">Therefore, this topic includes information about circumstances where a data mart reset might help and also circumstances where it's unlikely to help.</span></span>

## <a name="what-is-a-data-mart-reset"></a><span data-ttu-id="25016-107">Hvað er endurstilling gagnaskemma?</span><span class="sxs-lookup"><span data-stu-id="25016-107">What is a data mart reset?</span></span>

<span data-ttu-id="25016-108">Endurstilling gagnaskemmu mun slökkva á samþættingarverkum, eyða öllum gögnum gagnaskemmu og síðan virkja samþættingu aftur.</span><span class="sxs-lookup"><span data-stu-id="25016-108">A data mart reset will disable the integration tasks, delete all the data mart data, and then re-enable integration.</span></span>

<span data-ttu-id="25016-109">Til að tryggja að gömul gögn séu ekki sett inn er aðeins hægt að hefja endurstillingu gagnaskemmu eftir að núverandi verkefnum er lokið.</span><span class="sxs-lookup"><span data-stu-id="25016-109">To ensure that old data isn't inserted, a data mart reset can be started only after existing tasks are completed.</span></span> <span data-ttu-id="25016-110">Ef reynt er að endurstilla gagnaskemmuna áður en öllum verkum er lokið gætu komið upp skilaboð á borð við „Ekki var hægt að endurstilla gagnaskemmu út af virku verki.</span><span class="sxs-lookup"><span data-stu-id="25016-110">If you try to reset the data mart before all tasks are completed, you might receive a message such as, "The data mart reset was unable to be processed because of an active task.</span></span> <span data-ttu-id="25016-111">Reyna skal aftur síðar.</span><span class="sxs-lookup"><span data-stu-id="25016-111">Please try again later."</span></span>

## <a name="when-do-i-have-to-do-a-data-mart-reset"></a><span data-ttu-id="25016-112">Hvenær þarf að endurstilla gagnaskemmu?</span><span class="sxs-lookup"><span data-stu-id="25016-112">When do I have to do a data mart reset?</span></span>

<span data-ttu-id="25016-113">Ef ein eða fleiri eftirfarandi fullyrðinga eiga við um aðstæður þínar getur fyrirtækið þitt notið góðs af endurstillingu gagnaskemmu:</span><span class="sxs-lookup"><span data-stu-id="25016-113">If one or more of the following statements apply to your situation, your organization can benefit from a data mart reset:</span></span>

- <span data-ttu-id="25016-114">Gagnagrunnur forritsins var endurheimtur.</span><span class="sxs-lookup"><span data-stu-id="25016-114">The application database was restored.</span></span>
- <span data-ttu-id="25016-115">Þjónustubeiðni var opnuð og tæknimaður hjá notendaþjónustu hefur sagt þér að endurstilla gagnaskemmuna sem hluti af skrefi úrræðaleitar.</span><span class="sxs-lookup"><span data-stu-id="25016-115">You opened a support ticket, and a Support engineer instructed you to reset the data mart as part of a troubleshooting step.</span></span>
 
## <a name="when-is-a-data-mart-reset-inappropriate"></a><span data-ttu-id="25016-116">Hvenær á ekki að endurstilla gagnaskemmu?</span><span class="sxs-lookup"><span data-stu-id="25016-116">When is a data mart reset inappropriate?</span></span>

<span data-ttu-id="25016-117">Hér eru nokkrar aðstæður þar sem við mælum ekki með því að þú endurstillir gagnaskemmuna:</span><span class="sxs-lookup"><span data-stu-id="25016-117">Here are some of the circumstances where we don't recommend that you reset the data mart:</span></span>

- <span data-ttu-id="25016-118">Þú lendir í vandræðum með afköst sem tengjast gagnasamstillingu.</span><span class="sxs-lookup"><span data-stu-id="25016-118">You're experiencing performance issues that are associated with data synchronization.</span></span>
- <span data-ttu-id="25016-119">Mynstur endurtekinnar endurstillingar á sér stað af einhverjum eftirfarandi ástæðum:</span><span class="sxs-lookup"><span data-stu-id="25016-119">You have a recurring reset pattern for any of the following reasons:</span></span>

    - <span data-ttu-id="25016-120">**Gögn vantar** – Ef þú tekur eftir því að gögn vantar skaltu opna þjónustubeiðni hjá Microsoft til að fara yfir skýrslusniðið þitt og möguleg vandamál varðandi samstillingu gagna.</span><span class="sxs-lookup"><span data-stu-id="25016-120">**Missing data** – If you notice that data is missing, open a support ticket with Microsoft to review your report format and possible data synchronization issues.</span></span>
    - <span data-ttu-id="25016-121">**Föst samþættingarstaða**</span><span class="sxs-lookup"><span data-stu-id="25016-121">**Stuck integration state**</span></span>
    - <span data-ttu-id="25016-122">**Útrunnar skrár** - Útrunnar skrár einar og sér réttlæta ekki endilega endurstillingu gagnaskemmu.</span><span class="sxs-lookup"><span data-stu-id="25016-122">**Stale records** – Stale records by themselves don't necessarily justify a data mart reset.</span></span> <span data-ttu-id="25016-123">Ef um er að ræða stórt gagnasafn mun endurstillingarferlið taka sinn tíma, en ólíklegt er að það lagi stöðuna.</span><span class="sxs-lookup"><span data-stu-id="25016-123">If you have a large data set, the reset process will take some time to run but is unlikely to lead to any improvement.</span></span>

## <a name="if-i-reset-the-data-mart-will-i-lose-reports-that-ive-already-designed"></a><span data-ttu-id="25016-124">Ef ég endurstilli gagnaskemmu missi ég þá skýrslur sem ég hef þegar hannað?</span><span class="sxs-lookup"><span data-stu-id="25016-124">If I reset the data mart, will I lose reports that I've already designed?</span></span>

<span data-ttu-id="25016-125">Nr.</span><span class="sxs-lookup"><span data-stu-id="25016-125">No.</span></span> <span data-ttu-id="25016-126">Skýrslurnar þínar eru geymdar í SQL-töflum sem verða ekki fyrir áhrifum af endurstillingu gagnaskemmu.</span><span class="sxs-lookup"><span data-stu-id="25016-126">Your reports are stored in SQL tables that aren't affected by a data mart reset.</span></span> <span data-ttu-id="25016-127">Ef þú hefur áhyggjur af að glata skýrslum sem þú hefur hannað geturðu tekið afrit af þeim hönnunum sem þú vilt ekki týna.</span><span class="sxs-lookup"><span data-stu-id="25016-127">If you're concerned about losing reports that you've designed, you can back up the designs that you don't want to lose.</span></span> <span data-ttu-id="25016-128">Til að taka öryggisafrit af hönnun skal opna skýrsluhönnuð og fara í **Fyrirtæki \> Fyrirtæki \> Einingar \> Útflutningur**.</span><span class="sxs-lookup"><span data-stu-id="25016-128">To back up designs, open Report Designer, and go to **Company \> Companies \> Building Blocks \> Export**.</span></span>
 
## <a name="do-all-users-have-to-exit-the-system-before-i-can-reset-the-data-mart"></a><span data-ttu-id="25016-129">Þurfa allir notendur að fara úr kerfinu áður en ég get endurstillt gagnaskemmuna?</span><span class="sxs-lookup"><span data-stu-id="25016-129">Do all users have to exit the system before I can reset the data mart?</span></span>

<span data-ttu-id="25016-130">Nr.</span><span class="sxs-lookup"><span data-stu-id="25016-130">No.</span></span> <span data-ttu-id="25016-131">Notendur geta haldið áfram að vinna í kerfinu á meðan endurstilling gagnaskemmu er í gangi.</span><span class="sxs-lookup"><span data-stu-id="25016-131">Users can continue to work in the system during a data mart reset.</span></span> <span data-ttu-id="25016-132">Notendur geta þó ekki nálgast skýrslur sem voru stofnaðar með því að nota Financial Reporter fyrr en endurstillingu lýkur.</span><span class="sxs-lookup"><span data-stu-id="25016-132">However, until the reset is completed, users won't be able to access any reports that were created by using Financial Reporter.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
