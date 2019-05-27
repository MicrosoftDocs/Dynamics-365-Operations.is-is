---
title: Afskriftir eigna
description: Þetta efnisatriði veitir yfirlit yfir afskriftir eigna.
author: ShylaThompson
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBonus, AssetBookTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 3121
ms.assetid: 98ff891f-e0e2-4184-b618-28107a50851f
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a82e14e12cbde29e5619518481d0c22f6fa1a37a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569610"
---
# <a name="fixed-asset-depreciation"></a><span data-ttu-id="3ecae-103">Afskriftir eigna</span><span class="sxs-lookup"><span data-stu-id="3ecae-103">Fixed asset depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3ecae-104">Þetta efnisatriði veitir yfirlit yfir afskriftir eigna.</span><span class="sxs-lookup"><span data-stu-id="3ecae-104">This topic provides an overview of depreciation for fixed assets.</span></span>

<span data-ttu-id="3ecae-105">Afskriftir eru tímabilsfærsla sem vanalega minnkar virði eigna í efnahagslykli og er gjaldfærð á rekstrarlykla sem útgjöld.</span><span class="sxs-lookup"><span data-stu-id="3ecae-105">Depreciation is a periodic transaction that typically reduces the value of the fixed asset on the balance sheet, and is charged as an expenditure to a profit and loss account.</span></span> <span data-ttu-id="3ecae-106">Þess vegna er aðallykil yfirleitt notaður til að kreditfæra reglubundnar afskriftir í efnahagslykli.</span><span class="sxs-lookup"><span data-stu-id="3ecae-106">Therefore, a main account is typically used to credit the periodic depreciation on the balance sheet.</span></span> <span data-ttu-id="3ecae-107">Mótlykill er lykill í hagnaðar- og taphluta bókhaldslykilsins.</span><span class="sxs-lookup"><span data-stu-id="3ecae-107">An offset account is an account in the profit and loss part of the chart of accounts.</span></span>

## <a name="depreciation-adjustment"></a><span data-ttu-id="3ecae-108">Leiðrétting afskriftar</span><span class="sxs-lookup"><span data-stu-id="3ecae-108">Depreciation adjustment</span></span>
<span data-ttu-id="3ecae-109">Yfirleitt er einungis leiðrétting á bókaðri afskriftafærslu bókuð sem afskriftaleiðrétting.</span><span class="sxs-lookup"><span data-stu-id="3ecae-109">Usually, only a correction to a posted depreciation transaction is posted as a depreciation adjustment.</span></span> <span data-ttu-id="3ecae-110">Þess vegna eru bæði aðallykill og mótlykill settir upp á sama hátt og lyklar afskrifta.</span><span class="sxs-lookup"><span data-stu-id="3ecae-110">Therefore, both the main account and the offset account are set up just like the accounts for depreciation.</span></span> <span data-ttu-id="3ecae-111">Leiðrétting afskriftar getur annaðhvort verið jákvæð upphæð eða neikvæð upphæð en aðgerðir aðallykils (sem efnahagslykill) og virkni mótlykils (yfirleitt sem rekstrarlykill) eru enn þær sömu.</span><span class="sxs-lookup"><span data-stu-id="3ecae-111">A depreciation adjustment can be either a positive amount or a negative amount, but the functionality of the main account (as a balance sheet account) and the functionality of the offset account (usually as a profit and loss account) remain the same.</span></span>

## <a name="extraordinary-depreciation"></a><span data-ttu-id="3ecae-112">Óreglulegar afskriftir</span><span class="sxs-lookup"><span data-stu-id="3ecae-112">Extraordinary depreciation</span></span>
<span data-ttu-id="3ecae-113">Óreglulegar afskriftir virkar eins og grunnafskriftinni.</span><span class="sxs-lookup"><span data-stu-id="3ecae-113">Extraordinary depreciation works like basic depreciation.</span></span> <span data-ttu-id="3ecae-114">Það þýðir að aðallykill er notaður til að kreditfæra afskriftaupphæðina á efnahagslykilinn og minnka virði eignar.</span><span class="sxs-lookup"><span data-stu-id="3ecae-114">Therefore, a main account is used to credit the depreciation amount to the balance sheet and reduce the value of the fixed asset.</span></span> <span data-ttu-id="3ecae-115">Mótlykill er lykill hagnaðar og taps, þar sem afskrift sem er reiknuð fyrir fjárhagstímabil er gjaldfærð sem útgjöld.</span><span class="sxs-lookup"><span data-stu-id="3ecae-115">An offset account is a profit and loss account, where the depreciation that is calculated for the fiscal period is charged as an expenditure.</span></span> 

<span data-ttu-id="3ecae-116">Óreglulegar afskriftir virkar sjálfstætt fyrir grunnafskriftinni.</span><span class="sxs-lookup"><span data-stu-id="3ecae-116">Extraordinary depreciation works independently of basic depreciation.</span></span> <span data-ttu-id="3ecae-117">Með því að hafa óreglulegar afskriftir sem aðskilda færslugerð er hægt að bóka og tilkynna óreglulegu afskriftirnar óháð venjulegu grunnafskriftunum.</span><span class="sxs-lookup"><span data-stu-id="3ecae-117">By having extraordinary depreciation as a separate transaction type, you can post and report the extraordinary depreciation separately from the basic depreciation.</span></span>

## <a name="special-depreciation-allowance"></a><span data-ttu-id="3ecae-118">Sérstök heimild til afskriftar</span><span class="sxs-lookup"><span data-stu-id="3ecae-118">Special depreciation allowance</span></span>
<span data-ttu-id="3ecae-119">Hægt er að nota sérstök heimild til afskriftar til að gera aukalegar afskriftaupphæðir fyrsta árið sem eign er í þjónustu og afskrifuð.</span><span class="sxs-lookup"><span data-stu-id="3ecae-119">You can use special depreciation allowances to take extra depreciation amounts during the first year that an asset is put in service and depreciated.</span></span> <span data-ttu-id="3ecae-120">Sérstök heimild til afskriftar verður gerð á undan öðrum afskriftaútreikningum.</span><span class="sxs-lookup"><span data-stu-id="3ecae-120">Special depreciation allowances must be taken before any other depreciation calculations.</span></span> <span data-ttu-id="3ecae-121">Þar sem sérstakar heimildir til afskrifta eru oft óþekkt fyrr en síðar í líftíma eignar, er best að nota þessa gerð afskriftar með bók sem ekki bókar í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="3ecae-121">Because special depreciation allowances are often unknown until later in the service life of the fixed asset, it's best to use this type of depreciation with a book that doesn't post to the general ledger.</span></span> <span data-ttu-id="3ecae-122">Hægt er að nota Eyða færslum sem eru ekki bókaðar í fjárhag valkost til að eyða færsluferli fyrir þessar bækur.</span><span class="sxs-lookup"><span data-stu-id="3ecae-122">You can use the Delete transactions not posted to general ledger periodic function to delete the transaction history for these books.</span></span> <span data-ttu-id="3ecae-123">Svo er hægt að eyða afskriftarsögu fyrir eignabókina, bóka sérstök heimild til afskriftar þegar hún er þekkt, og bóka svo eftirstandandi afskriftarfærslum fyrir árið.</span><span class="sxs-lookup"><span data-stu-id="3ecae-123">You can then delete the depreciation history for the fixed asset book, post the special depreciation allowance when it's known, and then post the remaining depreciation transactions for the year.</span></span> 

<span data-ttu-id="3ecae-124">Hægt er að stofna ótakmarkaðan fjölda af sérstök heimild til afskriftar.</span><span class="sxs-lookup"><span data-stu-id="3ecae-124">You can create an unlimited number of special depreciation allowance records.</span></span> <span data-ttu-id="3ecae-125">Eftir að þessum færslum hefur verið úthlutað á eignaflokka eru þær notaðar í eignabók.</span><span class="sxs-lookup"><span data-stu-id="3ecae-125">After you assign those records to an asset group book, they are applied to the asset book.</span></span> 

<span data-ttu-id="3ecae-126">Sérstök heimild til afskriftar eru færðar inn sem prósenta eða föst upphæð.</span><span class="sxs-lookup"><span data-stu-id="3ecae-126">A special depreciation allowance is entered as either a percentage or a fixed amount.</span></span> <span data-ttu-id="3ecae-127">Þegar þú bókar afskriftartillögur eru bókaðar afskriftafærslur sérstakrar heimildar í bókina sem aðskildar færslur frá afskriftarfærslum.</span><span class="sxs-lookup"><span data-stu-id="3ecae-127">When you post depreciation proposals, special depreciation allowance transactions are posted to the book as transactions that are separate from the depreciation transactions.</span></span>

## <a name="depreciation-calendars"></a><span data-ttu-id="3ecae-128">Afskriftardagatöl</span><span class="sxs-lookup"><span data-stu-id="3ecae-128">Depreciation calendars</span></span>
<span data-ttu-id="3ecae-129">Hver bók hefur dagatalið sem notað er við afskriftir eigna.</span><span class="sxs-lookup"><span data-stu-id="3ecae-129">Each book has a calendar that is used when you depreciate fixed assets.</span></span> <span data-ttu-id="3ecae-130">Bókin notar fjárhagsdagatal sjálfgefið ef þú tiltekur ekki dagatal.</span><span class="sxs-lookup"><span data-stu-id="3ecae-130">By default, if you don't indicate a calendar on the book, the book uses the ledger fiscal calendar.</span></span> <span data-ttu-id="3ecae-131">Einnig þarf að velja fjárhagsdagatal fyrir bók þegar tengd afskriftarregla bókar notar fjárhagslegt afskriftaár.</span><span class="sxs-lookup"><span data-stu-id="3ecae-131">You must select a fiscal calendar for a book when the depreciation profile that is associated with the book uses a fiscal depreciation year.</span></span> 

<span data-ttu-id="3ecae-132">Hægt er að stofna samnýtt dagatöl með síðunni **Fjárhagsdagatöl**í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="3ecae-132">You can create shared calendars by using the **Fiscal calendars** page in General ledger.</span></span>

<span data-ttu-id="3ecae-133">Frekari upplýsingar eru í [Afskriftaaðferðir og hefðir](depreciation-methods-conventions.md)</span><span class="sxs-lookup"><span data-stu-id="3ecae-133">For more information, see [Depreciation methods and conventions](depreciation-methods-conventions.md).</span></span>



