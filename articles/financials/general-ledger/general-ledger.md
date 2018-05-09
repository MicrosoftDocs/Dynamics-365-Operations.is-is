---
title: "Fjárhagur og Fjárhagsleg skýrslugerð heimasíða"
description: "Fjárhagur er notaður til að skilgreina og stjórna fjárhagslegum færslum í lögaðila."
author: twheeloc
manager: AnnBe
ms.date: 08/31/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: GeneralJournalEntryWorkspace
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 65431
ms.assetid: d2c604df-daae-42cd-82d9-c80e3dee4a60
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: cc01f7d2cec25d754263e361e5de9ad1499d9523
ms.contentlocale: is-is
ms.lasthandoff: 05/08/2018

---

# <a name="general-ledger"></a><span data-ttu-id="04823-103">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="04823-103">General ledger</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="04823-104">Fjárhagur er notaður til að skilgreina og stjórna fjárhagslegum færslum í lögaðila.</span><span class="sxs-lookup"><span data-stu-id="04823-104">Use General ledger to define and manage the legal entity’s financial records.</span></span> <span data-ttu-id="04823-105">Í fjárhag er skrá fyrir debet og kredit færslur.</span><span class="sxs-lookup"><span data-stu-id="04823-105">The general ledger is a register of debit and credit entries.</span></span> <span data-ttu-id="04823-106">Þessar færslur eru flokkaðar með lyklarnir sem taldir eru upp í línuriti yfir lykla.</span><span class="sxs-lookup"><span data-stu-id="04823-106">These entries are classified using the accounts that are listed in a chart of accounts.</span></span> 

 - [<span data-ttu-id="04823-107">Yfirlit yfir bókhaldslykil</span><span class="sxs-lookup"><span data-stu-id="04823-107">Plan your chart of accounts</span></span>](plan-chart-of-accounts.md)
 - [<span data-ttu-id="04823-108">Aðallykilgerðir</span><span class="sxs-lookup"><span data-stu-id="04823-108">Main account types</span></span>](main-account-types.md)

<span data-ttu-id="04823-109">Hægt er að úthluta eða dreifa peningarupphæðum  á einn eða fleiri reikninga eða reikning og samsetningar reikningsvídda byggt á úthlutunarreglum.</span><span class="sxs-lookup"><span data-stu-id="04823-109">You can allocate, or distribute, monetary amounts to one or more accounts or account and dimension combinations based on allocation rules.</span></span> <span data-ttu-id="04823-110">Til eru tvær gerðir úthlutunar: föst og breytileg.</span><span class="sxs-lookup"><span data-stu-id="04823-110">There are two types of allocations: fixed and variable.</span></span> <span data-ttu-id="04823-111">Einnig er hægt að jafna færslur á milli fjárhagslykla og endurmeta upphæðir gjaldmiðla.</span><span class="sxs-lookup"><span data-stu-id="04823-111">You can also settle transactions between ledger accounts and revalue currency amounts.</span></span> <span data-ttu-id="04823-112">Við lok fjárhagsársins þarf að undirbúa lyklana fyrir næsta fjárhagsár og loka núverandi fjárhagsárunum.</span><span class="sxs-lookup"><span data-stu-id="04823-112">At the end of a fiscal year, you must generate closing transactions and prepare your accounts for the next fiscal year.</span></span> <span data-ttu-id="04823-113">Hægt er að nota sameiningaraðgerðin til að sameina fjárhagsniðurstöður nokkurra dótturfyrirtækja lögaðila í niðurstöðum eina, sameinað fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="04823-113">You can use the consolidation functionality to combine the financial results for several subsidiary legal entities into results for a single, consolidated organization.</span></span> <span data-ttu-id="04823-114">Dótturfyrirtækin geta verið í sama Microsoft Dynamics 365 for Finance and Operations gagnagrunni eða aðskildum gagnagrunnum.</span><span class="sxs-lookup"><span data-stu-id="04823-114">The subsidiaries can be in the same Microsoft Dynamics 365 for Finance and Operations database or in separate databases.</span></span>

- [<span data-ttu-id="04823-115">Yfirlit yfir samstæðu og niðurfellingu</span><span class="sxs-lookup"><span data-stu-id="04823-115">Consolidation and elimination overview</span></span>](../budgeting/consolidation-elimination-overview.md)
- [<span data-ttu-id="04823-116">Fjárhagslykilstöður</span><span class="sxs-lookup"><span data-stu-id="04823-116">General ledger account balances</span></span>](general-ledger-account-balances.md)
- [<span data-ttu-id="04823-117">Fjárhagsvíddir</span><span class="sxs-lookup"><span data-stu-id="04823-117">Financial dimensions</span></span>](financial-dimensions.md)

<span data-ttu-id="04823-118">[![Viðskiptaferli](./media/GL-process.PNG)](./media/GL-process.PNG)</span><span class="sxs-lookup"><span data-stu-id="04823-118">[![Business process](./media/GL-process.PNG)](./media/GL-process.PNG)</span></span>

## <a name="sales-tax"></a><span data-ttu-id="04823-119">Virðisaukaskattur</span><span class="sxs-lookup"><span data-stu-id="04823-119">Sales tax</span></span>
<span data-ttu-id="04823-120">Hvert fyrirtæki innheimtir og greiðir skatta til ýmissa skattyfirvalda.</span><span class="sxs-lookup"><span data-stu-id="04823-120">Every company collects and pays taxes to various tax authorities.</span></span> <span data-ttu-id="04823-121">Reglur og taxtar eru mismunandi eftir landi/svæði, fylki, sýslu og borg.</span><span class="sxs-lookup"><span data-stu-id="04823-121">The rules and rates vary by country/region, state, county, and city.</span></span>
<span data-ttu-id="04823-122">Þar að auki þarf að uppfæra reglur reglulega þegar kröfur skattyfirvalda breytast.</span><span class="sxs-lookup"><span data-stu-id="04823-122">In addition, the rules must be updated periodically when tax authorities change their requirements.</span></span> <span data-ttu-id="04823-123">Í VSK-kóða eru grunnupplýsingar um hversu mikið er innheimt og greitt til yfirvalda.</span><span class="sxs-lookup"><span data-stu-id="04823-123">Sales tax codes contain the basic information about how much you collect and pay to the authorities.</span></span> <span data-ttu-id="04823-124">Þegar settur er upp vsk-kóði, skilgreinirðu upphæðirnar og prósentur sem þarf að innheimta.</span><span class="sxs-lookup"><span data-stu-id="04823-124">When you set up sales tax codes, you define the amounts or percentages that must be collected.</span></span> <span data-ttu-id="04823-125">Einnig skilgreinirðu ýmsar aðferðir sem notaðar eru þegar þessum upphæðum eða prósentum er beitt á færsluupphæðir.</span><span class="sxs-lookup"><span data-stu-id="04823-125">You also define the various methods by which those amounts or percentages are applied to transaction amounts.</span></span> <span data-ttu-id="04823-126">Efnisatriðin í þessum hluta veita upplýsingar um hvernig setja á upp VSK-kóða fyrir aðferðirnar og taxtana sem skattyfirvöld krefjast.</span><span class="sxs-lookup"><span data-stu-id="04823-126">The topics in this section provide information about how to set up sales tax codes for the methods and rates that your tax authorities require.</span></span>

 - [<span data-ttu-id="04823-127">Yfirlit virðisaukaskatts</span><span class="sxs-lookup"><span data-stu-id="04823-127">Sales tax overview</span></span>](indirect-taxes-overview.md)
 - [<span data-ttu-id="04823-128">Virðisaukaskattur byggður á jaðargrunns- og útreikningsaðferðum</span><span class="sxs-lookup"><span data-stu-id="04823-128">Sales tax rates based on the Marginal base and Calculation methods</span></span>](marginal-base-field.md)
 - [<span data-ttu-id="04823-129">VSK-greiðslur og sléttunarreglur</span><span class="sxs-lookup"><span data-stu-id="04823-129">Sales tax payments and rounding rules</span></span>](round-sales-tax-payments.md)


## <a name="additional-resources"></a><span data-ttu-id="04823-130">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="04823-130">Additional resources</span></span>

### <a name="whats-new-and-in-development"></a><span data-ttu-id="04823-131">Nýjungar og eiginleikar á þróunarstigi</span><span class="sxs-lookup"><span data-stu-id="04823-131">What's new and in development</span></span>

<span data-ttu-id="04823-132">Á [Microsoft Dynamics 365 Roadmap](https://roadmap.dynamics.com/) eru upplýsingar um nýja eiginleika og eiginleika sem eru á þróunarstigi.</span><span class="sxs-lookup"><span data-stu-id="04823-132">Go to the [Microsoft Dynamics 365 Roadmap](https://roadmap.dynamics.com/) to see what new features have been released and what new features are in development.</span></span> 

### <a name="blogs"></a><span data-ttu-id="04823-133">Blogg</span><span class="sxs-lookup"><span data-stu-id="04823-133">Blogs</span></span>

<span data-ttu-id="04823-134">Á [Microsoft Dynamics 365-blogginu](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise) er að finna umfjöllun, fréttir og aðrar upplýsingar um Viðskiptaskuldir og aðrar hugbúnaðarlausnir.</span><span class="sxs-lookup"><span data-stu-id="04823-134">You can find opinions, news, and other information about Accounts payable and other solutions on the [Microsoft Dynamics 365 blog](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise).</span></span>

<span data-ttu-id="04823-135">Hægt er að finna margar færslur um fjárhag á [bloggi afurðarteymis Microsoft Dynamics AX](https://blogs.msdn.microsoft.com/dax/).</span><span class="sxs-lookup"><span data-stu-id="04823-135">There are many posts about General ledger on the [Microsoft Dynamics AX product team blog](https://blogs.msdn.microsoft.com/dax/).</span></span> <span data-ttu-id="04823-136">Þó svo sumar þessara færslna voru skrifaðar um eldri útgáfu fjárhagsins eiga sömu hugtök eiga enn við og ferlin eru svipuð í nýjustu útgáfunni.</span><span class="sxs-lookup"><span data-stu-id="04823-136">Although some of these posts were written for the previous version of General ledger, the same concepts still apply, and the procedures are also similar in the current version.</span></span>

<span data-ttu-id="04823-137">[Blogg Microsoft Dynamics Operations-samstarfsaðila](https://community.dynamics.com/partner/b/operationspartnercommunityblog) veitir Microsoft Dynamics-samstarfsaðilum aðgang að tæmandi upplýsingum um nýjungar og vinsæla eiginleika MBS Operations á einum stað.</span><span class="sxs-lookup"><span data-stu-id="04823-137">The [Microsoft Dynamics Operations Partner Community Blog](https://community.dynamics.com/partner/b/operationspartnercommunityblog) gives Microsoft Dynamics Partners a single resource where they can learn what is new and trending in MBS Operations.</span></span>

### <a name="task-guides"></a><span data-ttu-id="04823-138">Verkleiðbeiningar</span><span class="sxs-lookup"><span data-stu-id="04823-138">Task guides</span></span>
<span data-ttu-id="04823-139">Frekari hjálp er í boði sem verkleiðbeiningar í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="04823-139">Additional help is available as task guides inside Finance and Operations.</span></span> <span data-ttu-id="04823-140">Smellið á hnappinn Hjálp á hvaða síðu sem er til að fá aðgang að verkleiðbeiningum.</span><span class="sxs-lookup"><span data-stu-id="04823-140">To access task guides, click the Help button on any page.</span></span>

### <a name="videos"></a><span data-ttu-id="04823-141">Myndbönd</span><span class="sxs-lookup"><span data-stu-id="04823-141">Videos</span></span>

<span data-ttu-id="04823-142">Kynntu þér kennslumyndbönd sem eru aðgengileg á [YouuTube-rás Microsoft Dynamics 365](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ).</span><span class="sxs-lookup"><span data-stu-id="04823-142">Check out the how-to videos that are now available on the [Microsoft Dynamics 365 YouTube Channel](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ).</span></span>


