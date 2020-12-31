---
title: Bóka eignafærslur í bókunalög
description: Þessi grein gefur yfirlit yfir virkni bókunarlags fyrir eignafærslur.
author: moaamer
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3001
ms.assetid: 7dabde57-0843-47c3-85ef-f36b6f472e30
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a80e4d1a081b5bd8c58238b0f154f8fbdc660ccb
ms.sourcegitcommit: f80819c67c0a7475315fc68ce1cb568831e2c0e7
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/10/2020
ms.locfileid: "4493673"
---
# <a name="post-fixed-asset-transactions-to-posting-layers"></a><span data-ttu-id="99825-103">Bóka eignafærslur í bókunalög</span><span class="sxs-lookup"><span data-stu-id="99825-103">Post fixed asset transactions to posting layers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="99825-104">Þessi grein gefur yfirlit yfir virkni bókunarlags fyrir eignafærslur.</span><span class="sxs-lookup"><span data-stu-id="99825-104">This article gives an overview of posting layer functionality for fixed asset transactions.</span></span>

<span data-ttu-id="99825-105">Eign er oft afskrifuð á mismunandi hátt í mismunandi tilgangi.</span><span class="sxs-lookup"><span data-stu-id="99825-105">A fixed asset is often depreciated in different ways for different purposes.</span></span> <span data-ttu-id="99825-106">Afskriftir fyrir skatta eru reiknaðar út eftir gildandi skattareglum til að ná sem mestum afskriftum fyrir skatta, en afskriftir fyrir skýrslugerð er reiknaðar eftir bókhaldslögum og stöðlum.</span><span class="sxs-lookup"><span data-stu-id="99825-106">Depreciation for tax purposes is calculated by using current tax rules to achieve the highest possible depreciation before taxes, but depreciation for reporting purposes is calculated according to accounting laws and standards.</span></span> <span data-ttu-id="99825-107">Útreikningum og skráningum mismunandi afskrifta er haldið aðskildum í bókunarlögunum.</span><span class="sxs-lookup"><span data-stu-id="99825-107">The various kinds of depreciation are calculated and recorded separately in the posting layers.</span></span>

<span data-ttu-id="99825-108">Hvert bók sem er tengt eign er uppsett fyrir ákveðið bókunarlag sem hefur heildarafskriftarviðfang.</span><span class="sxs-lookup"><span data-stu-id="99825-108">Each book that is attached to a fixed asset is set up for a particular posting layer that has an overall depreciation objective.</span></span> <span data-ttu-id="99825-109">Bókunarlögin eru Tíu: Gildandi, Aðgerðir, Skatt og sjö Sérsniðna lögum.</span><span class="sxs-lookup"><span data-stu-id="99825-109">There are ten posting layers: Current, Operations, Tax, and seven Custom layers.</span></span> <span data-ttu-id="99825-110">Hægt er að gera bókun í fjárhag fyrir bók óvirka með því að stilla reitinn Bóka í fjárhag á nei.</span><span class="sxs-lookup"><span data-stu-id="99825-110">You can also disable posting to the general ledger for the book by setting the Post to general ledger field to No.</span></span> <span data-ttu-id="99825-111">Á Bókunarlag reit er þá sjálfvirkt stillt á Ekkert.</span><span class="sxs-lookup"><span data-stu-id="99825-111">The Posting layer field is then automatically set to None.</span></span> <span data-ttu-id="99825-112">Yfirleitt eru bækur sem bóka ekki í fjárhag notaðar fyrir skattskýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="99825-112">Typically, books that don’t post to the general ledger are used for tax reporting purposes.</span></span> <span data-ttu-id="99825-113">Þessi nálgun gefur viðbótar sveigjanleika til að eyða sögulegum færslum fyrir eignabók þar sem þær hafa ekki verið bundnar í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="99825-113">This approach gives you the additional flexibility to delete historical transactions for the asset book, because they haven’t been committed to the general ledger.</span></span>

<span data-ttu-id="99825-114">Eignabækur eru skilgreindir með því að nota í færslubókarheiti síðuna á fjárhags > færslubókaruppsetningu > færslubókarheiti.</span><span class="sxs-lookup"><span data-stu-id="99825-114">Fixed asset journals are defined by using the Journal names page at General ledger > Journal setup > Journal names.</span></span> <span data-ttu-id="99825-115">Hver færslubók, sem hægt er að bóka afskriftir í, er skilgreind með færslubókarheiti sínu fyrir einungis eitt bókunarlag.</span><span class="sxs-lookup"><span data-stu-id="99825-115">Each journal that you can post depreciations in is defined by its journal name for only one posting layer.</span></span> <span data-ttu-id="99825-116">Ekki er hægt að breyta bókunarlaginu í færslubók.</span><span class="sxs-lookup"><span data-stu-id="99825-116">The posting layer in the journal can’t be changed.</span></span> <span data-ttu-id="99825-117">Takmarkanir tryggir að færslum í hverju bókunarlagi er haldið aðskildum.</span><span class="sxs-lookup"><span data-stu-id="99825-117">This restriction helps guarantee that transactions for each posting layer are kept separate.</span></span> <span data-ttu-id="99825-118">Það verður að stofna að minnsta kosti eitt færslubókarheiti fyrir hvert bókunarlag.</span><span class="sxs-lookup"><span data-stu-id="99825-118">At least one journal name must be created for each posting layer.</span></span> <span data-ttu-id="99825-119">Ef verið er að nota bækur sem ekki bóka í fjárhag, verður einnig að stofna færslubók þar sem bókunarlag stillt á Engin.</span><span class="sxs-lookup"><span data-stu-id="99825-119">If you’re using books that don’t post to the general ledger, you must also create a journal where the posting layer is set to None.</span></span>

<span data-ttu-id="99825-120">Hægt er að tilnefna fjárhagsreikninga sem færslur eigna eru bókaðar í á síðunni Bókunarreglur eigna.</span><span class="sxs-lookup"><span data-stu-id="99825-120">You can designate ledger accounts for fixed asset transactions on the Fixed asset posting profiles page.</span></span> <span data-ttu-id="99825-121">Fyrir hverja bókunarreglu verður að velja viðeigandi færslugerð og bóka, og svo þarf að tilnefna fjárhagslyklana.</span><span class="sxs-lookup"><span data-stu-id="99825-121">For each posting profile, you must select the relevant transaction type and book, and then designate the ledger accounts.</span></span> <span data-ttu-id="99825-122">Setja upp færslu bókunarreglu fyrir hverja bók sem er bókuð í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="99825-122">Set up a posting profile record for each book that will post to the general ledger.</span></span>

<span data-ttu-id="99825-123">Hægt er að færa eignina inn í skjöl sem styðja aðeins **Núverandi** bókunarlag, eins og **innkaupapöntun**, **biðreikning lánardrottins**, **sölupöntun** eða **reikning með frjálsum texta**.</span><span class="sxs-lookup"><span data-stu-id="99825-123">The fixed asset can be entered in documents that only support the **Current** posting layer, like **Purchase order**, **Pending vendor invoice**, **Sales order**, or **Free text invoice**.</span></span> <span data-ttu-id="99825-124">Þegar búið er að velja auðkenni eignar í einhverju af þessum skjölum er eignabók síuð í bókina með **Núverandi** bókunarlagi, og verður fyllt út sjálfkrafa, við bókun þegar kerfið staðfestir að bókunarlag eignarinnar er **Núverandi**.</span><span class="sxs-lookup"><span data-stu-id="99825-124">While selecting a fixed asset ID in any of those documents the asset book is filtered to the book with **Current** posting layer, and will be filled in automatically, during posting when the system validates that the fixed asset posting layer is **Current**.</span></span> <span data-ttu-id="99825-125">Ef ekki er hægt að ljúka við staðfestingu er bókunarferlið stöðvað.</span><span class="sxs-lookup"><span data-stu-id="99825-125">If that validation can't be completed, the posting process will be stopped.</span></span> 

> [!NOTE] 
> <span data-ttu-id="99825-126">Með því að nota afleidd bækur er mögulegt að bóka færslur á mismunandi bókunarlög á sama tíma.</span><span class="sxs-lookup"><span data-stu-id="99825-126">By using derived books, you can post transactions to different posting layers at the same time.</span></span> <span data-ttu-id="99825-127">Færslur aðalbókar eru stofnaðar í færslubók eða upprunaskjali með bókunarlagi sem samsvarar bókunarlagi bókar.</span><span class="sxs-lookup"><span data-stu-id="99825-127">The transactions of the primary book are created in a journal or source document where the posting layer corresponds to the book posting layer.</span></span> <span data-ttu-id="99825-128">Á meðan á bókun stendur, verða færslur afleidda bóka bókaðar á þau bókunarlög sem tilheyra þeim.</span><span class="sxs-lookup"><span data-stu-id="99825-128">During posting, the derived book transactions will be posted to the appropriate posting layers.</span></span> 


<span data-ttu-id="99825-129">Nánari upplýsingar eru í [Afleiddar bækur](derived-books.md) og [Bóka í afleiddar bækur](post-derived-value-models.md).</span><span class="sxs-lookup"><span data-stu-id="99825-129">For more information see, [Derived books](derived-books.md) and [Post with derived books](post-derived-value-models.md).</span></span>



