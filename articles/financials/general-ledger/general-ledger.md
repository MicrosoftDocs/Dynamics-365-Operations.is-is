---
title: Fjárhagur og Fjárhagsleg skýrslugerð heimasíða
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
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 65431
ms.assetid: d2c604df-daae-42cd-82d9-c80e3dee4a60
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 85afebcc88ad1c087d5f1dabaac56f694534cf98
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "363362"
---
# <a name="general-ledger"></a><span data-ttu-id="9a4da-103">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="9a4da-103">General ledger</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9a4da-104">Fjárhagur er notaður til að skilgreina og stjórna fjárhagslegum færslum í lögaðila.</span><span class="sxs-lookup"><span data-stu-id="9a4da-104">Use General ledger to define and manage the legal entity’s financial records.</span></span> <span data-ttu-id="9a4da-105">Í fjárhag er skrá fyrir debet og kredit færslur.</span><span class="sxs-lookup"><span data-stu-id="9a4da-105">The general ledger is a register of debit and credit entries.</span></span> <span data-ttu-id="9a4da-106">Þessar færslur eru flokkaðar með lyklarnir sem taldir eru upp í línuriti yfir lykla.</span><span class="sxs-lookup"><span data-stu-id="9a4da-106">These entries are classified using the accounts that are listed in a chart of accounts.</span></span> 

 - [<span data-ttu-id="9a4da-107">Yfirlit yfir bókhaldslykil</span><span class="sxs-lookup"><span data-stu-id="9a4da-107">Plan your chart of accounts</span></span>](plan-chart-of-accounts.md)
 - [<span data-ttu-id="9a4da-108">Aðallykilgerðir</span><span class="sxs-lookup"><span data-stu-id="9a4da-108">Main account types</span></span>](main-account-types.md)

<span data-ttu-id="9a4da-109">Hægt er að úthluta eða dreifa peningarupphæðum  á einn eða fleiri reikninga eða reikning og samsetningar reikningsvídda byggt á úthlutunarreglum.</span><span class="sxs-lookup"><span data-stu-id="9a4da-109">You can allocate, or distribute, monetary amounts to one or more accounts or account and dimension combinations based on allocation rules.</span></span> <span data-ttu-id="9a4da-110">Til eru tvær gerðir úthlutunar: föst og breytileg.</span><span class="sxs-lookup"><span data-stu-id="9a4da-110">There are two types of allocations: fixed and variable.</span></span> <span data-ttu-id="9a4da-111">Einnig er hægt að jafna færslur á milli fjárhagslykla og endurmeta upphæðir gjaldmiðla.</span><span class="sxs-lookup"><span data-stu-id="9a4da-111">You can also settle transactions between ledger accounts and revalue currency amounts.</span></span> <span data-ttu-id="9a4da-112">Við lok fjárhagsársins þarf að undirbúa lyklana fyrir næsta fjárhagsár og loka núverandi fjárhagsárunum.</span><span class="sxs-lookup"><span data-stu-id="9a4da-112">At the end of a fiscal year, you must generate closing transactions and prepare your accounts for the next fiscal year.</span></span> <span data-ttu-id="9a4da-113">Hægt er að nota sameiningaraðgerðin til að sameina fjárhagsniðurstöður nokkurra dótturfyrirtækja lögaðila í niðurstöðum eina, sameinað fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="9a4da-113">You can use the consolidation functionality to combine the financial results for several subsidiary legal entities into results for a single, consolidated organization.</span></span> <span data-ttu-id="9a4da-114">Dótturfyrirtækin geta verið í sama Microsoft Dynamics 365 for Finance and Operations gagnagrunni eða aðskildum gagnagrunnum.</span><span class="sxs-lookup"><span data-stu-id="9a4da-114">The subsidiaries can be in the same Microsoft Dynamics 365 for Finance and Operations database or in separate databases.</span></span>

- [<span data-ttu-id="9a4da-115">Yfirlit yfir samstæðu og niðurfellingu</span><span class="sxs-lookup"><span data-stu-id="9a4da-115">Consolidation and elimination overview</span></span>](../budgeting/consolidation-elimination-overview.md)
- [<span data-ttu-id="9a4da-116">Fjárhagslykilstöður</span><span class="sxs-lookup"><span data-stu-id="9a4da-116">General ledger account balances</span></span>](general-ledger-account-balances.md)
- [<span data-ttu-id="9a4da-117">Fjárhagsvíddir</span><span class="sxs-lookup"><span data-stu-id="9a4da-117">Financial dimensions</span></span>](financial-dimensions.md)

<span data-ttu-id="9a4da-118">[![Viðskiptaferli](./media/GL-process.PNG)](./media/GL-process.PNG)</span><span class="sxs-lookup"><span data-stu-id="9a4da-118">[![Business process](./media/GL-process.PNG)](./media/GL-process.PNG)</span></span>

## <a name="sales-tax"></a><span data-ttu-id="9a4da-119">Virðisaukaskattur</span><span class="sxs-lookup"><span data-stu-id="9a4da-119">Sales tax</span></span>
<span data-ttu-id="9a4da-120">Hvert fyrirtæki innheimtir og greiðir skatta til ýmissa skattyfirvalda.</span><span class="sxs-lookup"><span data-stu-id="9a4da-120">Every company collects and pays taxes to various tax authorities.</span></span> <span data-ttu-id="9a4da-121">Reglur og taxtar eru mismunandi eftir landi/svæði, fylki, sýslu og borg.</span><span class="sxs-lookup"><span data-stu-id="9a4da-121">The rules and rates vary by country/region, state, county, and city.</span></span>
<span data-ttu-id="9a4da-122">Þar að auki þarf að uppfæra reglur reglulega þegar kröfur skattyfirvalda breytast.</span><span class="sxs-lookup"><span data-stu-id="9a4da-122">In addition, the rules must be updated periodically when tax authorities change their requirements.</span></span> <span data-ttu-id="9a4da-123">Í VSK-kóða eru grunnupplýsingar um hversu mikið er innheimt og greitt til yfirvalda.</span><span class="sxs-lookup"><span data-stu-id="9a4da-123">Sales tax codes contain the basic information about how much you collect and pay to the authorities.</span></span> <span data-ttu-id="9a4da-124">Þegar settur er upp vsk-kóði, skilgreinirðu upphæðirnar og prósentur sem þarf að innheimta.</span><span class="sxs-lookup"><span data-stu-id="9a4da-124">When you set up sales tax codes, you define the amounts or percentages that must be collected.</span></span> <span data-ttu-id="9a4da-125">Einnig skilgreinirðu ýmsar aðferðir sem notaðar eru þegar þessum upphæðum eða prósentum er beitt á færsluupphæðir.</span><span class="sxs-lookup"><span data-stu-id="9a4da-125">You also define the various methods by which those amounts or percentages are applied to transaction amounts.</span></span> <span data-ttu-id="9a4da-126">Efnisatriðin í þessum hluta veita upplýsingar um hvernig setja á upp VSK-kóða fyrir aðferðirnar og taxtana sem skattyfirvöld krefjast.</span><span class="sxs-lookup"><span data-stu-id="9a4da-126">The topics in this section provide information about how to set up sales tax codes for the methods and rates that your tax authorities require.</span></span>

 - [<span data-ttu-id="9a4da-127">Yfirlit virðisaukaskatts</span><span class="sxs-lookup"><span data-stu-id="9a4da-127">Sales tax overview</span></span>](indirect-taxes-overview.md)
 - [<span data-ttu-id="9a4da-128">Virðisaukaskattur byggður á jaðargrunns- og útreikningsaðferðum</span><span class="sxs-lookup"><span data-stu-id="9a4da-128">Sales tax rates based on the Marginal base and Calculation methods</span></span>](marginal-base-field.md)
 - [<span data-ttu-id="9a4da-129">VSK-greiðslur og sléttunarreglur</span><span class="sxs-lookup"><span data-stu-id="9a4da-129">Sales tax payments and rounding rules</span></span>](round-sales-tax-payments.md)


## <a name="additional-resources"></a><span data-ttu-id="9a4da-130">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="9a4da-130">Additional resources</span></span>

### <a name="whats-new"></a><span data-ttu-id="9a4da-131">Nýjungar</span><span class="sxs-lookup"><span data-stu-id="9a4da-131">What's new</span></span>

<span data-ttu-id="9a4da-132">Farðu í [Útgáfuupplýsingar](https://docs.microsoft.com/en-us/business-applications-release-notes/) til að sjá hvaða nýju eiginleikar hafa verið gefnar út.</span><span class="sxs-lookup"><span data-stu-id="9a4da-132">Go to the [Release notes](https://docs.microsoft.com/en-us/business-applications-release-notes/) to see what new features have been released.</span></span> 

### <a name="videos"></a><span data-ttu-id="9a4da-133">Myndskeið</span><span class="sxs-lookup"><span data-stu-id="9a4da-133">Videos</span></span>

<span data-ttu-id="9a4da-134">Kynnið ykkur kennslumyndböndin sem eru aðgengileg á [Microsoft Dynamics 365 YouTube-rásinni ](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ).</span><span class="sxs-lookup"><span data-stu-id="9a4da-134">Check out the how-to videos that are now available on the [Microsoft Dynamics 365 YouTube Channel](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ).</span></span>

### <a name="blogs"></a><span data-ttu-id="9a4da-135">Blogg</span><span class="sxs-lookup"><span data-stu-id="9a4da-135">Blogs</span></span>

<span data-ttu-id="9a4da-136">Á [Microsoft Dynamics 365-blogginu](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise) er að finna umfjöllun, fréttir og aðrar upplýsingar um viðskiptaskuldir og aðrar lausnir.</span><span class="sxs-lookup"><span data-stu-id="9a4da-136">You can find opinions, news, and other information about Accounts payable and other solutions on the [Microsoft Dynamics 365 blog](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise).</span></span>

<span data-ttu-id="9a4da-137">Hægt er að finna margar færslur um fjárhag á [Microsoft Dynamics AX bloggi afurðarteymis](https://blogs.msdn.microsoft.com/dax/).</span><span class="sxs-lookup"><span data-stu-id="9a4da-137">There are many posts about General ledger on the [Microsoft Dynamics AX product team blog](https://blogs.msdn.microsoft.com/dax/).</span></span> <span data-ttu-id="9a4da-138">Þó svo sumar þessara færslna voru skrifaðar um eldri útgáfu fjárhagsins eiga sömu hugtök eiga enn við og ferlin eru svipuð í nýjustu útgáfunni.</span><span class="sxs-lookup"><span data-stu-id="9a4da-138">Although some of these posts were written for the previous version of General ledger, the same concepts still apply, and the procedures are also similar in the current version.</span></span>

<span data-ttu-id="9a4da-139">Blogg [Microsoft Dynamics Operations-samstarfsaðila](https://community.dynamics.com/partner/b/operationspartnercommunityblog) veitir samstarfsaðilum Microsoft Dynamics aðgang að tæmandi upplýsingum um nýjungar og vinsæla eiginleika MBS Operations á einum stað.</span><span class="sxs-lookup"><span data-stu-id="9a4da-139">The [Microsoft Dynamics Operations Partner Community Blog](https://community.dynamics.com/partner/b/operationspartnercommunityblog) gives Microsoft Dynamics Partners a single resource where they can learn what is new and trending in MBS Operations.</span></span>

#### <a name="community-blogs"></a><span data-ttu-id="9a4da-140">Samfélagsblogg</span><span class="sxs-lookup"><span data-stu-id="9a4da-140">Community blogs</span></span>

- [<span data-ttu-id="9a4da-141">Það sem þú ættir að vita um fjárhag í Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="9a4da-141">What you should know about ledger in Dynamics 365 for Finance and Operations</span></span>](https://financefunction.tech/2018/04/29/what-you-should-know-about-ledger-in-dynamics-365-for-finance-and-operations)

