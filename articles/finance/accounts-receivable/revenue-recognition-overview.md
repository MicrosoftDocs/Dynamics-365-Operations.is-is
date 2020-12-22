---
title: Yfirlit tekjuskráningar
description: Í þessu efnisatriði er að finna upplýsingar um tekjuskráningareiginleikann. Þessi eiginleiki veitir sveigjanlega umgjörð sem gerir það kleift að skilgreina sérstakar reglur fyrir fyrirtækið um greiningu bæði verðlags og tekjuáætlunar fyrir pantanir með mörgum vörutegundum.
author: kweekley
manager: aolson
ms.date: 11/11/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 92af567499c1a8a23cd4d51e5bab48eaab2d8422
ms.sourcegitcommit: e544c51a68ad5daf748c0e877bdbde094ad40bd2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/03/2020
ms.locfileid: "4459273"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="1b8c7-104">Yfirlit tekjuskráningar</span><span class="sxs-lookup"><span data-stu-id="1b8c7-104">Revenue recognition overview</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="1b8c7-105">Ekki er hægt að kveikja á tekjuskráningareiginleikanum í gegnum eiginleikastjórnun.</span><span class="sxs-lookup"><span data-stu-id="1b8c7-105">The Revenue recognition feature can't be turned on through Feature management.</span></span> <span data-ttu-id="1b8c7-106">Nota verður skilgreiningarlykil til að kveikja á honum.</span><span class="sxs-lookup"><span data-stu-id="1b8c7-106">Currently, you must use configuration keys to turn it on.</span></span>

<span data-ttu-id="1b8c7-107">Fyrirtæki í atvinnugrein þar sem margar vörutegundir eru seldar, svo sem vörur, þjónusta, áskriftir og svo framvegis, verða að geta sundurgreint pantanir með mörgum vörutegundum svo hægt sé að greina tekjur á grundvelli sérstakra viðmiðunarregla fyrir fyrirtækið og atvinnugreinina.</span><span class="sxs-lookup"><span data-stu-id="1b8c7-107">Companies in industries that sell multiple elements, such as products, services, subscriptions, and so on, must be able to break out multi-element orders so that revenue can be recognized based on a set of company-specific and industry-specific guidelines.</span></span>

<span data-ttu-id="1b8c7-108">Almennt séð má nota tekjuskráningarferlið til að framkvæma þessi verk:</span><span class="sxs-lookup"><span data-stu-id="1b8c7-108">In general, the revenue recognition process can be used to perform these tasks:</span></span>

* <span data-ttu-id="1b8c7-109">Úthluta tekjum til að tryggja að viðeigandi verðlag greinist á grundvelli virðist hluta í pöntunum með mörgum vörutegundum.</span><span class="sxs-lookup"><span data-stu-id="1b8c7-109">Allocate revenue, to help guarantee that the appropriate revenue price is recognized, based on the value of the components on multi-element orders.</span></span>
* <span data-ttu-id="1b8c7-110">Fresta tekjum í samræmi við tekjuáætlun sem endurspeglar samningsbundinn tímaramma og hlutfall fyrir greiningu á tekjum yfir tímann.</span><span class="sxs-lookup"><span data-stu-id="1b8c7-110">Defer revenue, based on a revenue schedule that represents the contractual time frame and percentages for recognizing revenue over time.</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE44iER]

<span data-ttu-id="1b8c7-111">Myndbandið [Hvernig á að nota tekjuskráningu í Dynamics 365 Finance](https://youtu.be/v3amIsiqvoo) (sýnt hér að ofan) er innifalið í [Finance and Operations spilunarlistanum](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) á YouTube.</span><span class="sxs-lookup"><span data-stu-id="1b8c7-111">The [How to use revenue recognition in Dynamics 365 Finance](https://youtu.be/v3amIsiqvoo) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

<span data-ttu-id="1b8c7-112">Tekjuskráningareiginleikinn veitir sveigjanlega umgjörð sem gerir það kleift að skilgreina sérstakar reglur fyrir fyrirtækið um greiningu bæði verðlags og tekjuáætlunar.</span><span class="sxs-lookup"><span data-stu-id="1b8c7-112">The Revenue recognition feature provides a flexible framework that lets you define company-specific rules for recognizing both the revenue price and the revenue schedule.</span></span>

<span data-ttu-id="1b8c7-113">Útgefnar afurðir eru notaðar til að styðja við tekjuskráningu í fylgiskjölum sölupantana.</span><span class="sxs-lookup"><span data-stu-id="1b8c7-113">Released products are used to support revenue recognition on sales order documents.</span></span> <span data-ttu-id="1b8c7-114">Útgefnar afurðir innihalda uppsetninguna sem krafist er til að ákvarða verðlag og tekjuáætlun.</span><span class="sxs-lookup"><span data-stu-id="1b8c7-114">The released products contain the setup that is required to determine the revenue price and the revenue schedule.</span></span> <span data-ttu-id="1b8c7-115">Sölupöntunin getur átt uppruna sinn í tíma- og efnisverki.</span><span class="sxs-lookup"><span data-stu-id="1b8c7-115">The sales order can originate from a Time and materials project.</span></span>

<span data-ttu-id="1b8c7-116">Fyrirtæki geta notað tekjuáætlunareiginleikann án þess að nota verðlagseiginleikann.</span><span class="sxs-lookup"><span data-stu-id="1b8c7-116">Companies can use the revenue schedule functionality without using the revenue price functionality.</span></span> <span data-ttu-id="1b8c7-117">Því verður verðið í sölupöntunarlínum notað sem ýmist tekjur eða frestaðar tekjur.</span><span class="sxs-lookup"><span data-stu-id="1b8c7-117">Therefore, the price on the sales order lines will be used as either revenue or deferred revenue.</span></span> <span data-ttu-id="1b8c7-118">Ef tekjuáætlun er til fyrir sölupöntunarlínu verður verðinu í sölupöntunarlínunni frestað.</span><span class="sxs-lookup"><span data-stu-id="1b8c7-118">If a revenue schedule exists on the sales order line, the price on the sales order line will be deferred.</span></span> <span data-ttu-id="1b8c7-119">Ef tekjuáætlun er ekki til fyrir sölupöntunarlínu verður verðið í sölupöntunarlínunni bókað á tekjulykil við reikningsfærslu.</span><span class="sxs-lookup"><span data-stu-id="1b8c7-119">If a revenue schedule doesn't exist on the sales order line, the price on the sales order line will be posted to a revenue account when it's invoiced.</span></span>

<span data-ttu-id="1b8c7-120">Verðið er reiknað annaðhvort þegar sölupöntun er staðfest eða þegar reikningurinn er bókaður.</span><span class="sxs-lookup"><span data-stu-id="1b8c7-120">The revenue price is calculated either when the sales order is confirmed or when the invoice is posted.</span></span> <span data-ttu-id="1b8c7-121">Til að forskoða verðið áður en reikningur er bókaður verður þú að staðfesta sölupöntunina.</span><span class="sxs-lookup"><span data-stu-id="1b8c7-121">To preview the revenue price before the invoice is posted, you must confirm the sales order.</span></span>

<span data-ttu-id="1b8c7-122">Þegar sölupöntunin er staðfest er áætlun um væntanlegar tekjur einnig stofnuð ef einhver sölupöntunarlína hefur tekjuáætlun.</span><span class="sxs-lookup"><span data-stu-id="1b8c7-122">When the sales order is confirmed, an expected revenue schedule is also created if any sales order line has a revenue schedule.</span></span> <span data-ttu-id="1b8c7-123">Þegar sölupöntun er reikningsfærð er áætlun um væntanlegar tekjur eytt og áætlun um væntanlegar tekjur er skipt út fyrir raunverulega tekjuskráningaráætlun.</span><span class="sxs-lookup"><span data-stu-id="1b8c7-123">When the sales order is invoiced, the expected revenue schedule is deleted, and the expected revenue schedule is replaced with the actual revenue recognition schedule.</span></span>

<span data-ttu-id="1b8c7-124">Unnið er með upplýsingar úr tekjuskráningaráætlun fyrir hverja sölupöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="1b8c7-124">The details of the revenue recognition schedule are maintained for each sales order line.</span></span> <span data-ttu-id="1b8c7-125">Þar af leiðandi getur stjórnandi tekjuskráningar skoðað upplýsingarnar og losað línur í tekjur þegar samningsbundnum skyldum lýkur.</span><span class="sxs-lookup"><span data-stu-id="1b8c7-125">Therefore, the revenue recognition manager can view the details and can release lines to revenue when the contractual obligation has been completed.</span></span> <span data-ttu-id="1b8c7-126">Við lok hvers tímabils getur stjórnandi tekjuskráningar búið til færslubók fyrir tekjur til að losa allar áætlunarlínur sem eru á skilum á eða fyrir dagsetningu sem viðkomandi ákveður.</span><span class="sxs-lookup"><span data-stu-id="1b8c7-126">At the end of each period, the revenue recognition manager can create a revenue journal to release any schedule lines that are due on or before a date they define.</span></span> <span data-ttu-id="1b8c7-127">Þessi færslubók tekna er ekki bókuð strax.</span><span class="sxs-lookup"><span data-stu-id="1b8c7-127">This revenue journal isn't posted immediately.</span></span> <span data-ttu-id="1b8c7-128">Þar af leiðandi getur stjórnandi tekjuskráningar staðfest að rétt upphæð hafi verið losuð úr frestuðum tekjum í rauntekjur.</span><span class="sxs-lookup"><span data-stu-id="1b8c7-128">Therefore, the revenue recognition manager can verify that the correct amounts are being released from deferred revenue to actual revenue.</span></span>

<span data-ttu-id="1b8c7-129">Ef samningsbreytingar valda því að nýrri sölupöntunarlínu sé bætt við annaðhvort fyrirliggjandi sölupöntun eða nýja sölupöntun er hægt að keyra endurúthlutunarferli til að leiðrétta verðið á öllum línum sölupantana.</span><span class="sxs-lookup"><span data-stu-id="1b8c7-129">If a contractual change causes a new sales order line to be added either to the existing sales order or a new sales order, a reallocation process can be run to correct the revenue price across all lines on the sales orders.</span></span>
