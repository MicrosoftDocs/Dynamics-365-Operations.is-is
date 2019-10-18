---
title: Yfirlit yfir Fjárhag og Fjárhagsskýrslugerð
description: Fjárhagur er notaður til að skilgreina og stjórna fjárhagslegum færslum í lögaðila.
author: ShylaThompson
manager: AnnBe
ms.date: 08/31/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: GeneralJournalEntryWorkspace
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 65431
ms.assetid: d2c604df-daae-42cd-82d9-c80e3dee4a60
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c0e795e641314b4ef81f8972aadf597721995fcc
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186533"
---
# <a name="general-ledger-overview"></a><span data-ttu-id="b7ce8-103">Fjárhagsyfirlit</span><span class="sxs-lookup"><span data-stu-id="b7ce8-103">General ledger overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b7ce8-104">Fjárhagur er notaður til að skilgreina og stjórna fjárhagslegum færslum í lögaðila.</span><span class="sxs-lookup"><span data-stu-id="b7ce8-104">Use General ledger to define and manage the legal entity’s financial records.</span></span> <span data-ttu-id="b7ce8-105">Í fjárhag er skrá fyrir debet og kredit færslur.</span><span class="sxs-lookup"><span data-stu-id="b7ce8-105">The general ledger is a register of debit and credit entries.</span></span> <span data-ttu-id="b7ce8-106">Þessar færslur eru flokkaðar með lyklarnir sem taldir eru upp í línuriti yfir lykla.</span><span class="sxs-lookup"><span data-stu-id="b7ce8-106">These entries are classified using the accounts that are listed in a chart of accounts.</span></span> 

 - [<span data-ttu-id="b7ce8-107">Yfirlit yfir bókhaldslykil</span><span class="sxs-lookup"><span data-stu-id="b7ce8-107">Plan your chart of accounts</span></span>](plan-chart-of-accounts.md)
 - [<span data-ttu-id="b7ce8-108">Aðallykilgerðir</span><span class="sxs-lookup"><span data-stu-id="b7ce8-108">Main account types</span></span>](main-account-types.md)

<span data-ttu-id="b7ce8-109">Hægt er að úthluta eða dreifa peningarupphæðum á einn eða fleiri reikninga eða reikning og samsetningar reikningsvídda byggt á úthlutunarreglum.</span><span class="sxs-lookup"><span data-stu-id="b7ce8-109">You can allocate, or distribute, monetary amounts to one or more accounts or account and dimension combinations based on allocation rules.</span></span> <span data-ttu-id="b7ce8-110">Til eru tvær gerðir úthlutunar: föst og breytileg.</span><span class="sxs-lookup"><span data-stu-id="b7ce8-110">There are two types of allocations: fixed and variable.</span></span> <span data-ttu-id="b7ce8-111">Einnig er hægt að jafna færslur á milli fjárhagslykla og endurmeta upphæðir gjaldmiðla.</span><span class="sxs-lookup"><span data-stu-id="b7ce8-111">You can also settle transactions between ledger accounts and revalue currency amounts.</span></span> <span data-ttu-id="b7ce8-112">Við lok fjárhagsársins þarf að undirbúa lyklana fyrir næsta fjárhagsár og loka núverandi fjárhagsárunum.</span><span class="sxs-lookup"><span data-stu-id="b7ce8-112">At the end of a fiscal year, you must generate closing transactions and prepare your accounts for the next fiscal year.</span></span> <span data-ttu-id="b7ce8-113">Hægt er að nota sameiningaraðgerðin til að sameina fjárhagsniðurstöður nokkurra dótturfyrirtækja lögaðila í niðurstöðum eina, sameinað fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="b7ce8-113">You can use the consolidation functionality to combine the financial results for several subsidiary legal entities into results for a single, consolidated organization.</span></span> <span data-ttu-id="b7ce8-114">Dótturfyrirtækin geta verið í sama gagnagrunni eða aðskildum gagnagrunnum.</span><span class="sxs-lookup"><span data-stu-id="b7ce8-114">The subsidiaries can be in the same database or in separate databases.</span></span>

- [<span data-ttu-id="b7ce8-115">Yfirlit yfir samstæðu og niðurfellingu</span><span class="sxs-lookup"><span data-stu-id="b7ce8-115">Consolidation and elimination overview</span></span>](../budgeting/consolidation-elimination-overview.md)
- [<span data-ttu-id="b7ce8-116">Fjárhagslykilstöður</span><span class="sxs-lookup"><span data-stu-id="b7ce8-116">General ledger account balances</span></span>](general-ledger-account-balances.md)
- [<span data-ttu-id="b7ce8-117">Fjárhagsvíddir</span><span class="sxs-lookup"><span data-stu-id="b7ce8-117">Financial dimensions</span></span>](financial-dimensions.md)

<span data-ttu-id="b7ce8-118">[![Viðskiptaferli](./media/GL-process.PNG)](./media/GL-process.PNG)</span><span class="sxs-lookup"><span data-stu-id="b7ce8-118">[![Business process](./media/GL-process.PNG)](./media/GL-process.PNG)</span></span>

## <a name="sales-tax"></a><span data-ttu-id="b7ce8-119">Virðisaukaskattur</span><span class="sxs-lookup"><span data-stu-id="b7ce8-119">Sales tax</span></span>
<span data-ttu-id="b7ce8-120">Hvert fyrirtæki innheimtir og greiðir skatta til ýmissa skattyfirvalda.</span><span class="sxs-lookup"><span data-stu-id="b7ce8-120">Every company collects and pays taxes to various tax authorities.</span></span> <span data-ttu-id="b7ce8-121">Reglur og taxtar eru mismunandi eftir landi/svæði, fylki, sýslu og borg.</span><span class="sxs-lookup"><span data-stu-id="b7ce8-121">The rules and rates vary by country/region, state, county, and city.</span></span>
<span data-ttu-id="b7ce8-122">Þar að auki þarf að uppfæra reglur reglulega þegar kröfur skattyfirvalda breytast.</span><span class="sxs-lookup"><span data-stu-id="b7ce8-122">In addition, the rules must be updated periodically when tax authorities change their requirements.</span></span> <span data-ttu-id="b7ce8-123">Í VSK-kóða eru grunnupplýsingar um hversu mikið er innheimt og greitt til yfirvalda.</span><span class="sxs-lookup"><span data-stu-id="b7ce8-123">Sales tax codes contain the basic information about how much you collect and pay to the authorities.</span></span> <span data-ttu-id="b7ce8-124">Þegar settur er upp vsk-kóði, skilgreinirðu upphæðirnar og prósentur sem þarf að innheimta.</span><span class="sxs-lookup"><span data-stu-id="b7ce8-124">When you set up sales tax codes, you define the amounts or percentages that must be collected.</span></span> <span data-ttu-id="b7ce8-125">Einnig skilgreinirðu ýmsar aðferðir sem notaðar eru þegar þessum upphæðum eða prósentum er beitt á færsluupphæðir.</span><span class="sxs-lookup"><span data-stu-id="b7ce8-125">You also define the various methods by which those amounts or percentages are applied to transaction amounts.</span></span> <span data-ttu-id="b7ce8-126">Efnisatriðin í þessum hluta veita upplýsingar um hvernig setja á upp VSK-kóða fyrir aðferðirnar og taxtana sem skattyfirvöld krefjast.</span><span class="sxs-lookup"><span data-stu-id="b7ce8-126">The topics in this section provide information about how to set up sales tax codes for the methods and rates that your tax authorities require.</span></span>

 - [<span data-ttu-id="b7ce8-127">Yfirlit virðisaukaskatts</span><span class="sxs-lookup"><span data-stu-id="b7ce8-127">Sales tax overview</span></span>](indirect-taxes-overview.md)
 - [<span data-ttu-id="b7ce8-128">Virðisaukaskattur byggður á jaðargrunns- og útreikningsaðferðum</span><span class="sxs-lookup"><span data-stu-id="b7ce8-128">Sales tax rates based on the Marginal base and Calculation methods</span></span>](marginal-base-field.md)
 - [<span data-ttu-id="b7ce8-129">VSK-greiðslur og sléttunarreglur</span><span class="sxs-lookup"><span data-stu-id="b7ce8-129">Sales tax payments and rounding rules</span></span>](round-sales-tax-payments.md)


## <a name="additional-resources"></a><span data-ttu-id="b7ce8-130">Frekari tilföng</span><span class="sxs-lookup"><span data-stu-id="b7ce8-130">Additional resources</span></span>

#### <a name="whats-new-and-in-development"></a><span data-ttu-id="b7ce8-131">Nýjungar og eiginleikar á þróunarstigi</span><span class="sxs-lookup"><span data-stu-id="b7ce8-131">What's new and in development</span></span>

<span data-ttu-id="b7ce8-132">Í [útgáfuupplýsingum Microsoft Dynamics 365](https://go.microsoft.com/fwlink/?linkid=2010158) sérðu hvaða nýju eiginleikar hafa verið undirbúnir.</span><span class="sxs-lookup"><span data-stu-id="b7ce8-132">Go to the [Microsoft Dynamics 365 Release Notes](https://go.microsoft.com/fwlink/?linkid=2010158) to see what new features have been planned.</span></span> 

#### <a name="blogs"></a><span data-ttu-id="b7ce8-133">Blogg</span><span class="sxs-lookup"><span data-stu-id="b7ce8-133">Blogs</span></span>

<span data-ttu-id="b7ce8-134">Á [Microsoft Dynamics 365-blogginu](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise) og [Microsoft Dynamics 365 Finance and Operations - Financials-blogginu](https://community.dynamics.com/365/financeandoperations/b/financials) er að finna umfjöllun, fréttir og aðrar upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="b7ce8-134">You can find opinions, news, and other information on the [Microsoft Dynamics 365 blog](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise) and the [Microsoft Dynamics 365 Finance and Operations - Financials blog](https://community.dynamics.com/365/financeandoperations/b/financials).</span></span>

<span data-ttu-id="b7ce8-135">Blogg [Microsoft Dynamics Operations-samstarfsaðila](https://community.dynamics.com/partner/b/operationspartnercommunityblog) veitir samstarfsaðilum Microsoft Dynamics aðgang að tæmandi upplýsingum um nýjungar og vinsæla eiginleika MBS Operations á einum stað.</span><span class="sxs-lookup"><span data-stu-id="b7ce8-135">The [Microsoft Dynamics Operations Partner Community Blog](https://community.dynamics.com/partner/b/operationspartnercommunityblog) gives Microsoft Dynamics Partners a single resource where they can learn what is new and trending in MBS Operations.</span></span>

### <a name="videos"></a><span data-ttu-id="b7ce8-136">Myndbönd</span><span class="sxs-lookup"><span data-stu-id="b7ce8-136">Videos</span></span>

<span data-ttu-id="b7ce8-137">Kynnið ykkur kennslumyndböndin sem eru aðgengileg á [Microsoft Dynamics 365 YouTube-rásinni](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ).</span><span class="sxs-lookup"><span data-stu-id="b7ce8-137">Check out the how-to videos that are now available on the [Microsoft Dynamics 365 YouTube Channel](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ).</span></span>

#### <a name="community-blogs"></a><span data-ttu-id="b7ce8-138">Samfélagsblogg</span><span class="sxs-lookup"><span data-stu-id="b7ce8-138">Community blogs</span></span>

- [<span data-ttu-id="b7ce8-139">Það sem þú ættir að vita um fjárhag í Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b7ce8-139">What you should know about ledger in Dynamics 365 for Finance and Operations</span></span>](https://financefunction.tech/2018/04/29/what-you-should-know-about-ledger-in-dynamics-365-for-finance-and-operations)

