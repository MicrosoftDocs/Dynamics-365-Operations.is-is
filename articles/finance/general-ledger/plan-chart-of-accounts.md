---
title: Yfirlit yfir bókhaldslykil
description: Þessi efnisatriði veita upplýsingar sem hjálpa til við að áætla bókhaldslykla fyrir fyrirtækið.
author: aprilolson
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, LedgerChartOfAccounts
audience: Application User
ms.reviewer: roschlom
ms.custom: 14051
ms.assetid: 10edb129-33f0-4cf9-b2a7-4b7ffa09b229
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 29e5328043a4259b464b272983e11061ade1724c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5230371"
---
# <a name="plan-your-chart-of-accounts"></a><span data-ttu-id="7ca53-103">Yfirlit yfir bókhaldslykil</span><span class="sxs-lookup"><span data-stu-id="7ca53-103">Plan your chart of accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7ca53-104">Þetta efnisatriði veitir upplýsingar sem hjálpa til við að áætla bókhaldslykla fyrir fyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="7ca53-104">This topic provides information that will help you plan the chart of accounts for your organization.</span></span>

<span data-ttu-id="7ca53-105">Til að rekja og vinna með fjárhagslegar upplýsingar í fyrirtæki er hægt að setja upp bókhaldslykil</span><span class="sxs-lookup"><span data-stu-id="7ca53-105">To track and maintain financial information in an organization, you can set up a chart of accounts.</span></span> <span data-ttu-id="7ca53-106">bókhaldslykil er safn af lyklum sem skilgreina fjárhagsramma.</span><span class="sxs-lookup"><span data-stu-id="7ca53-106">A chart of accounts is a collection of accounts that define a financial framework.</span></span> <span data-ttu-id="7ca53-107">Til að rekja enn frekar færslurnar í þessum lyklum er hægt að bæta við hluta.</span><span class="sxs-lookup"><span data-stu-id="7ca53-107">To further track the transactions in these accounts, you can add segments.</span></span> <span data-ttu-id="7ca53-108">Þessir hlutar eru þekktir sem fjárhagsvíddir.</span><span class="sxs-lookup"><span data-stu-id="7ca53-108">These segments are known as financial dimensions.</span></span> <span data-ttu-id="7ca53-109">Til dæmis gæti kostnaðarlykil hafa fjárhagsvíddir með heitinu Deild, kostnaðarstað og tilgang.</span><span class="sxs-lookup"><span data-stu-id="7ca53-109">For example, an expense account might include financial dimensions that are named Department, Cost center, and Purpose.</span></span> <span data-ttu-id="7ca53-110">Notandaskilgreindar reglur ákvarða hvernig þessar fjárhagsvíddir eru tengdar við aðallykla og aðrar fjárhagsvíddir og hvernig hægt að færa inn færslur.</span><span class="sxs-lookup"><span data-stu-id="7ca53-110">User-defined rules determine how financial dimensions are attached to the main accounts and to other financial dimensions, and also how transactions are entered.</span></span> <span data-ttu-id="7ca53-111">Þessar notandaskilgreindu reglur eru þekktar sem lykilskipulag og ítarlegar reglur.</span><span class="sxs-lookup"><span data-stu-id="7ca53-111">These user-defined rules are known as account structures and advanced rules.</span></span>

<span data-ttu-id="7ca53-112">Bókhaldslykillinn er skipulagður listi yfir fjárhagslykla lögaðila.</span><span class="sxs-lookup"><span data-stu-id="7ca53-112">The chart of accounts is a structured list of a legal entity's general ledger accounts.</span></span> <span data-ttu-id="7ca53-113">Listinn er notaður til að útbúa fjárhagsskýrslur fyrir yfirvöld og eigendur.</span><span class="sxs-lookup"><span data-stu-id="7ca53-113">The list is used to prepare financial reports for authorities and owners.</span></span> <span data-ttu-id="7ca53-114">Lyklarnir eru fyrst flokkaðir eftir gerðum þeirra og síðan lagðir saman í stærri tegundir.</span><span class="sxs-lookup"><span data-stu-id="7ca53-114">The accounts are first grouped into types of accounts and then further aggregated into larger categories.</span></span> <span data-ttu-id="7ca53-115">Á almennasta stiginu eru lyklar flokkaðir sem tekjur og kostnaður (rekstrarlykill) og eignir og skuldbindingar (stöðulykill).</span><span class="sxs-lookup"><span data-stu-id="7ca53-115">At the most general level, the accounts are grouped as revenues and costs (operating accounts), and assets and liabilities (balance accounts).</span></span>

<span data-ttu-id="7ca53-116">Bókhaldslykla getur verið samnýtt og notuð af hvaða lögaðila sem er í fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="7ca53-116">A chart of accounts can be shared and used by any legal entity in an organization.</span></span> <span data-ttu-id="7ca53-117">Bókhaldslyklar sem eru notaðir hjá lögaðila eru skilgreindir á síðunni **Fjárhagur**.</span><span class="sxs-lookup"><span data-stu-id="7ca53-117">The chart of accounts that is used by a legal entity is defined on the **Ledger** page.</span></span>

<span data-ttu-id="7ca53-118">Nokkra þætti þarf að hafa í huga þegar skipulag bókhaldslykla er ákveðið fyrir fyrirtækið, þar á meðal:</span><span class="sxs-lookup"><span data-stu-id="7ca53-118">Here are some of the factors that you must consider when you plan the structure of the chart of accounts for your organization:</span></span>

- <span data-ttu-id="7ca53-119">Skýrslukrafa lands eða svæðis þar sem fyrirtæki þitt er staðsett</span><span class="sxs-lookup"><span data-stu-id="7ca53-119">The reporting requirements of the country or region where your organization is based</span></span>
- <span data-ttu-id="7ca53-120">Tilkynningarskyldur við lögaðila</span><span class="sxs-lookup"><span data-stu-id="7ca53-120">The reporting requirements of your legal entity</span></span>
- <span data-ttu-id="7ca53-121">Sérhæfingarstig sem þörf er á, bæði fyrir ytri fyrirtæki og þitt fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="7ca53-121">The degree of specification that is required, both for both external organizations and for your organization</span></span>

<span data-ttu-id="7ca53-122">Þú stofnar bókhaldslykil á síðunni **Bókhaldslykill**.</span><span class="sxs-lookup"><span data-stu-id="7ca53-122">You create the chart of accounts on the **Chart of accounts** page.</span></span> <span data-ttu-id="7ca53-123">Þú getur búið til aðallykla á síðunni **Bókhaldslykill** eða á síðunni **Aðallyklar**.</span><span class="sxs-lookup"><span data-stu-id="7ca53-123">You can create main accounts from the **Chart of accounts** page or the **Main accounts** page.</span></span> <span data-ttu-id="7ca53-124">Aðallyklar þínir ættu ekki að nota sérstafi sem eru notaðar sem skiltákn bókhaldslykils.</span><span class="sxs-lookup"><span data-stu-id="7ca53-124">Your main accounts shouldn't use any special characters that are used as delimiters for chart of accounts.</span></span> <span data-ttu-id="7ca53-125">Annars gætir þú fundið fyrir óstöðugleika, eða þú gætir þurft að nota uppflettingar eða svarglugga þegar þú slærð inn samsetningar lykla og vídda.</span><span class="sxs-lookup"><span data-stu-id="7ca53-125">Otherwise, you might experience instability, or you might always have to use lookups or the dialog box when you enter combinations of accounts and dimensions.</span></span> <span data-ttu-id="7ca53-126">Nánari upplýsingar sjá [Stofna aðallykil](tasks/create-main-account.md).</span><span class="sxs-lookup"><span data-stu-id="7ca53-126">For more information, see [Create a main account](tasks/create-main-account.md).</span></span>

> [!NOTE]
> <span data-ttu-id="7ca53-127">Í Dynamics 365 for Finance and Operations útgáfu 8.0 (apríl 2018) er hægt að breyta skiltákni bókhaldslykils á síðunni **Færibreytur fjárhags**.</span><span class="sxs-lookup"><span data-stu-id="7ca53-127">In Dynamics 365 for Finance and Operations version 8.0 (April 2018), you can modify the chart of accounts delimiter from the **General ledger parameters** page.</span></span>

<span data-ttu-id="7ca53-128">Það er góð hugmynd að tengja við aðallykla tegundir aðallykils þannig er hægt nýta sjálfgefna fjárhagsskýrslur án þess að þurfa að gera neinar breytingar.</span><span class="sxs-lookup"><span data-stu-id="7ca53-128">It's a good idea to link the main accounts to main account categories, so that you can take advantage of the default financial reports without having to make any modifications.</span></span> <span data-ttu-id="7ca53-129">Þess vegna er hægt að hanna og viðhalda skýrslur á fljótari og auðveldari hátt.</span><span class="sxs-lookup"><span data-stu-id="7ca53-129">Therefore, you can more quickly and easily design and maintain reports.</span></span>

<span data-ttu-id="7ca53-130">Þú stofnar lykilskipulag á síðunni **Skilgreina lykilskipulag**.</span><span class="sxs-lookup"><span data-stu-id="7ca53-130">You create account structures on the **Configure account structures** page.</span></span> <span data-ttu-id="7ca53-131">Lykilskipulag tilgreina gildar samsetningar.</span><span class="sxs-lookup"><span data-stu-id="7ca53-131">Account structures define valid combinations.</span></span> <span data-ttu-id="7ca53-132">Þessar samsetningar, ásamt aðallyklum, mynda bókhaldslykla.</span><span class="sxs-lookup"><span data-stu-id="7ca53-132">These combinations, together with main accounts, form a chart of accounts.</span></span> <span data-ttu-id="7ca53-133">Nánari upplýsingar sjá [Stofna lykilsskipulag](tasks/create-account-structures.md).</span><span class="sxs-lookup"><span data-stu-id="7ca53-133">For more information, see [Create account structures](tasks/create-account-structures.md).</span></span>

<span data-ttu-id="7ca53-134">**Lögaðili hnekkir**</span><span class="sxs-lookup"><span data-stu-id="7ca53-134">**Legal entity overrides**</span></span>

<span data-ttu-id="7ca53-135">Ekki eru allir aðallyklar gildir fyrir alla lögaðila og sumir aðallyklar kunna aðeins að eiga við um ákveðið tímabil.</span><span class="sxs-lookup"><span data-stu-id="7ca53-135">Not all main accounts are valid for all legal entities, and some main account might be relevant only for a specific period.</span></span> <span data-ttu-id="7ca53-136">Í þessari atburðarás getur þú notað kaflann **Hnekkingar lögaðila** til að bera kennsl á fyrirtækin sem aðallykillinn ætti að vera lokaður fyrir, eigandinn og tímabilið þegar víddin er virk.</span><span class="sxs-lookup"><span data-stu-id="7ca53-136">In this scenario, you can use the **Legal entity overrides** section to identify the companies that the main account should be suspended for, the owner, and the period when the dimension is active.</span></span> <span data-ttu-id="7ca53-137">Hnekkingar á samnýttu stigi mega ekki vera meira takmarkandi en hnekkingar á stigi lögaðila.</span><span class="sxs-lookup"><span data-stu-id="7ca53-137">The overrides at the shared level can't be more restrictive than the overrides at the legal entity level.</span></span>

<span data-ttu-id="7ca53-138">Frekari upplýsingar er hægt að finna í eftirfarandi efni:</span><span class="sxs-lookup"><span data-stu-id="7ca53-138">For more information, see the following topics:</span></span>

- [<span data-ttu-id="7ca53-139">Fjárhagsvíddir</span><span class="sxs-lookup"><span data-stu-id="7ca53-139">Financial dimensions</span></span>](financial-dimensions.md)
- [<span data-ttu-id="7ca53-140">Stofna og úthluta ítarlegu regluskipulagi</span><span class="sxs-lookup"><span data-stu-id="7ca53-140">Create and assign advanced rule structures</span></span>](tasks/create-assign-advanced-rule-structures.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]