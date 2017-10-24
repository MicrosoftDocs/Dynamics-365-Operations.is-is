---
title: "Áætlun bókhaldslykila"
description: "Þessi skrá upplýsingar sem hjálpa þér áætla bókhaldslykla fyrir fyrirtæki þitt."
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DimensionConfigureAccountStructure, LedgerChartOfAccounts
audience: Application User
ms.reviewer: robinr
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14051
ms.assetid: 10edb129-33f0-4cf9-b2a7-4b7ffa09b229
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 848da7ec8f4a7915f3b78945b808b564f4510434
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---

# <a name="plan-your-chart-of-accounts"></a><span data-ttu-id="f2ed4-103">Áætlun bókhaldslykila</span><span class="sxs-lookup"><span data-stu-id="f2ed4-103">Plan your chart of accounts</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="f2ed4-104">Þessi skrá upplýsingar sem hjálpa þér áætla bókhaldslykla fyrir fyrirtæki þitt.</span><span class="sxs-lookup"><span data-stu-id="f2ed4-104">This article provides information that will help you plan the chart of accounts for your organization.</span></span>

<span data-ttu-id="f2ed4-105">Til að rekja og vinna með fjárhagslegar upplýsingar í fyrirtæki er hægt að setja upp bókhaldslykil</span><span class="sxs-lookup"><span data-stu-id="f2ed4-105">To track and maintain financial information in an organization, you can set up a chart of accounts.</span></span> <span data-ttu-id="f2ed4-106">bókhaldslykil er safn af lyklum sem skilgreina fjárhagsramma.</span><span class="sxs-lookup"><span data-stu-id="f2ed4-106">A chart of accounts is a collection of accounts that define a financial framework.</span></span> <span data-ttu-id="f2ed4-107">Til að rekja frekar færslurnar í þessara lykla er hlutum, sem kallast fjárhagsvíddir, bætt við aðallyklana.</span><span class="sxs-lookup"><span data-stu-id="f2ed4-107">To further track the transactions in these accounts, you can add segments, which are known as financial dimensions.</span></span> <span data-ttu-id="f2ed4-108">Til dæmis gæti kostnaðarlykil hafa fjárhagsvíddir með heitinu Deild, kostnaðarstað og tilgang.</span><span class="sxs-lookup"><span data-stu-id="f2ed4-108">For example, an expense account might include financial dimensions that are named Department, Cost center, and Purpose.</span></span> <span data-ttu-id="f2ed4-109">Notandaskilgreind reglur, sem kallast ítarlegar reglur, ákvarða hvernig þessar fjárhagsvíddir eru tengdar við aðallykla og aðrar fjárhagsvíddir og hvernig hægt að færa inn færslur saman.</span><span class="sxs-lookup"><span data-stu-id="f2ed4-109">User-defined rules, which are known as account structures and advanced rules, determine how financial dimensions are attached to the main accounts and other financial dimensions, and also how transactions are entered.</span></span> 

<span data-ttu-id="f2ed4-110">Bókhaldslykillinn er skipulagður listi yfir fjárhagslykla lögaðila.</span><span class="sxs-lookup"><span data-stu-id="f2ed4-110">The chart of accounts is a structured list of a legal entity’s general ledger accounts.</span></span> <span data-ttu-id="f2ed4-111">Listinn er notaður til að útbúa fjárhagsskýrslur fyrir yfirvöld og eigendur.</span><span class="sxs-lookup"><span data-stu-id="f2ed4-111">The list is used to prepare financial reports for authorities and owners.</span></span> <span data-ttu-id="f2ed4-112">Lyklarnir eru flokkaðir eftir gerðum og síðan lagðir saman í stærri tegundir.</span><span class="sxs-lookup"><span data-stu-id="f2ed4-112">The accounts are grouped into types of accounts and then further aggregated into larger categories.</span></span> <span data-ttu-id="f2ed4-113">Á almennasta stiginu eru lyklar flokkaðir sem tekjur og kostnaður (rekstrarlykill) og eignir og skuldbindingar (stöðulykill).</span><span class="sxs-lookup"><span data-stu-id="f2ed4-113">At the most general level, the accounts are grouped as revenues and costs (operating accounts), and assets and liabilities (balance accounts).</span></span> 

<span data-ttu-id="f2ed4-114">Bókhaldslykla getur verið samnýtt og notuð af hvaða lögaðila sem er í fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="f2ed4-114">A chart of accounts can be shared and used by any legal entity in an organization.</span></span> <span data-ttu-id="f2ed4-115">Bókhaldslyklar sem eru notaðir hjá lögaðila eru skilgreindir á síðunni **Fjárhagur**.</span><span class="sxs-lookup"><span data-stu-id="f2ed4-115">The chart of accounts that is used by a legal entity is defined on the **Ledger** page.</span></span> 

<span data-ttu-id="f2ed4-116">Nokkra þætti þarf að hafa í huga þegar skipulag bókhaldslykla er ákveðið fyrir fyrirtækið, þar á meðal:</span><span class="sxs-lookup"><span data-stu-id="f2ed4-116">Here are some of the factors that you must consider when you plan the structure of the chart of accounts for your organization:</span></span>

-   <span data-ttu-id="f2ed4-117">skýrslukrafa lands/svæðis þar sem fyrirtæki þitt er staðsett.</span><span class="sxs-lookup"><span data-stu-id="f2ed4-117">The reporting requirements of the country/region where your organization is based</span></span>
-   <span data-ttu-id="f2ed4-118">Tilkynningarskyldur við lögaðila</span><span class="sxs-lookup"><span data-stu-id="f2ed4-118">The reporting requirements of your legal entity</span></span>
-   <span data-ttu-id="f2ed4-119">Sérhæfingarstig sem þörf er á, bæði fyrir ytri fyrirtæki og þitt fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="f2ed4-119">The degree of specification that is required, both for both external organizations and for your organization</span></span>

<span data-ttu-id="f2ed4-120">Stofnaðu bókhaldslykil í **Bókhaldslykill** síðu.</span><span class="sxs-lookup"><span data-stu-id="f2ed4-120">Create the chart of accounts on the **Chart of accounts** page.</span></span> <span data-ttu-id="f2ed4-121">Hægt er að stofna aðallykla úr  **Bókhaldslykil** síðu eða **aðallykla** síðu.</span><span class="sxs-lookup"><span data-stu-id="f2ed4-121">Main accounts can be created from the **Chart of accounts** page or the **Main accounts** page.</span></span> <span data-ttu-id="f2ed4-122">aðallyklar þínir ættu ekki að nota sérstaka stafi sem eru notaðar sem skiltákn bókhaldslykils.</span><span class="sxs-lookup"><span data-stu-id="f2ed4-122">Your main accounts shouldn't use any special characters that are used as chart of accounts delimiters.</span></span> <span data-ttu-id="f2ed4-123">Ef sérstaf er hjá þér sem er sú sama og við skiltákn bókhaldslykils, gæti orðið óstöðugleiki, eða þörf á til að nota alltaf uppflettingar eða hliðarglugga þegar verið er að færa inn reikning eða samsetningar víddar.</span><span class="sxs-lookup"><span data-stu-id="f2ed4-123">If you do have a special character that is the same as your chart of accounts delimiter, you may experience instability, or the need to always use lookups or the flyout when entering account and dimension combinations.</span></span> <span data-ttu-id="f2ed4-124">Nánari upplýsingar sjá [Stofna aðallykil](tasks/create-account-structures.md).</span><span class="sxs-lookup"><span data-stu-id="f2ed4-124">For more information, see [Create a main account](tasks/create-account-structures.md).</span></span>


<span data-ttu-id="f2ed4-125">Það er góð hugmynd að tengja við aðallykla tegundir aðallykils þannig er hægt nýta sjálfgefna fjárhagsskýrslur án þess að þurfa að gera neinar breytingar.</span><span class="sxs-lookup"><span data-stu-id="f2ed4-125">It's a good idea to link the main accounts to main account categories, so that you can take advantage of the default financial reports without having to make any modifications.</span></span> <span data-ttu-id="f2ed4-126">Þess vegna er hægt að hanna og viðhalda skýrslur á fljótari og auðveldari hátt.</span><span class="sxs-lookup"><span data-stu-id="f2ed4-126">Therefore, you can more quickly and easily design and maintain reports.</span></span> 

<span data-ttu-id="f2ed4-127">Notið síðunni **Skilgreina lykilskipulag** til að skilgreina lykilskipulag.</span><span class="sxs-lookup"><span data-stu-id="f2ed4-127">Use the **Configure account structures** page to create account structures.</span></span> <span data-ttu-id="f2ed4-128">Lykilskipulag tilgreina gildar samsetningar.</span><span class="sxs-lookup"><span data-stu-id="f2ed4-128">Account structures define valid combinations.</span></span> <span data-ttu-id="f2ed4-129">Samsetningar með aðallykla, skjámyndinni bókhaldslykla.</span><span class="sxs-lookup"><span data-stu-id="f2ed4-129">The combinations, together with main accounts, form a chart of accounts.</span></span>  <span data-ttu-id="f2ed4-130">Nánari upplýsingar sjá [Stofna lykilsskipulag](tasks/create-main-account.md).</span><span class="sxs-lookup"><span data-stu-id="f2ed4-130">For more information, see [Create account structures](tasks/create-main-account.md).</span></span>

<span data-ttu-id="f2ed4-131">**Lögaðili hnekkir**</span><span class="sxs-lookup"><span data-stu-id="f2ed4-131">**Legal entity overrides**</span></span> 

<span data-ttu-id="f2ed4-132">Ekki eru allir aðallyklar gildir fyrir alla lögaðila og sumir kunna aðeins að eiga við um ákveðið tímabil.</span><span class="sxs-lookup"><span data-stu-id="f2ed4-132">Not all main accounts are valid for all legal entities and some may only be relevant for a specific time period.</span></span> <span data-ttu-id="f2ed4-133">Í þessum aðstæðum Lögaðili hnekkir getur verið notað til að auðkenna hvaða fyrirtæki ætti ekki að nota aðallykil fyrir, hver er eigandi og tímabilið sem víddin er virk.</span><span class="sxs-lookup"><span data-stu-id="f2ed4-133">In this scenario the Legal entity overrides section can be used to identify which companies the main account should be suspended for, who the owner is and the time period the dimension is active.</span></span> <span data-ttu-id="f2ed4-134">Hnekkingar á samnýttu stigi má ekki vera meira takmarkandi en hnekking á stigi lögaðila.</span><span class="sxs-lookup"><span data-stu-id="f2ed4-134">The overrides at the shared level cannot be more restrictive than the overrides at the legal entity level.</span></span>

<span data-ttu-id="f2ed4-135">Nánari upplýsingar eru í eftirfarandi efnisatriðum: [Fjárhagsvíddir](financial-dimensions.md)
[Stofna og úthluta skipulagi um ítarlegar reglur](tasks/create-assign-advanced-rule-structures.md)</span><span class="sxs-lookup"><span data-stu-id="f2ed4-135">For more information, see the following topics: [Financial dimensions](financial-dimensions.md)
[Create and assign advanced rule structures](tasks/create-assign-advanced-rule-structures.md)</span></span>




