---
title: "Fjárhagur og Fjárhagsleg skýrslugerð heimasíða"
description: "Fjárhagur er notaður til að skilgreina og stjórna fjárhagslegum færslum í lögaðila. Í fjárhag er skrá fyrir debet og kredit færslur. Þessar færslur eru flokkaðar með lyklarnir sem taldir eru upp í línuriti yfir lykla."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 65431
ms.assetid: d2c604df-daae-42cd-82d9-c80e3dee4a60
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 78f3d9c27767c089ac686f333cae3cb50c03ee18
ms.contentlocale: is-is
ms.lasthandoff: 07/18/2017

---

# <a name="general-ledger"></a><span data-ttu-id="b50d1-105">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="b50d1-105">General ledger</span></span> 

[!include[banner](../includes/banner.md)]


<span data-ttu-id="b50d1-106">Fjárhagur er notaður til að skilgreina og stjórna fjárhagslegum færslum í lögaðila.</span><span class="sxs-lookup"><span data-stu-id="b50d1-106">Use General ledger to define and manage the legal entity’s financial records.</span></span> <span data-ttu-id="b50d1-107">Í fjárhag er skrá fyrir debet og kredit færslur.</span><span class="sxs-lookup"><span data-stu-id="b50d1-107">The general ledger is a register of debit and credit entries.</span></span> <span data-ttu-id="b50d1-108">Þessar færslur eru flokkaðar með lyklarnir sem taldir eru upp í línuriti yfir lykla.</span><span class="sxs-lookup"><span data-stu-id="b50d1-108">These entries are classified using the accounts that are listed in a chart of accounts.</span></span> 

<span data-ttu-id="b50d1-109">Hægt er að úthluta eða dreifa peningarupphæðum  á einn eða fleiri reikninga eða reikning og samsetningar reikningsvídda byggt á úthlutunarreglum.</span><span class="sxs-lookup"><span data-stu-id="b50d1-109">You can allocate, or distribute, monetary amounts to one or more accounts or account and dimension combinations based on allocation rules.</span></span> <span data-ttu-id="b50d1-110">Til eru tvær gerðir úthlutunar: föst og breytileg.</span><span class="sxs-lookup"><span data-stu-id="b50d1-110">There are two types of allocations: fixed and variable.</span></span> <span data-ttu-id="b50d1-111">Einnig er hægt að jafna færslur á milli fjárhagslykla og endurmeta upphæðir gjaldmiðla.</span><span class="sxs-lookup"><span data-stu-id="b50d1-111">You can also settle transactions between ledger accounts and revalue currency amounts.</span></span> <span data-ttu-id="b50d1-112">Við lok fjárhagsársins þarf að undirbúa lyklana fyrir næsta fjárhagsár og loka núverandi fjárhagsárunum.</span><span class="sxs-lookup"><span data-stu-id="b50d1-112">At the end of a fiscal year, you must generate closing transactions and prepare your accounts for the next fiscal year.</span></span> <span data-ttu-id="b50d1-113">Hægt er að nota sameiningaraðgerðin til að sameina fjárhagsniðurstöður nokkurra dótturfyrirtækja lögaðila í niðurstöðum eina, sameinað fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="b50d1-113">You can use the consolidation functionality to combine the financial results for several subsidiary legal entities into results for a single, consolidated organization.</span></span> <span data-ttu-id="b50d1-114">Dótturfyrirtækin geta verið í sama Microsoft Dynamics 365 for Finance and Operations gagnagrunni eða aðskildum gagnagrunnum.</span><span class="sxs-lookup"><span data-stu-id="b50d1-114">The subsidiaries can be in the same Microsoft Dynamics 365 for Finance and Operations database or in separate databases.</span></span>

# <a name="sales-tax"></a><span data-ttu-id="b50d1-115">Virðisaukaskattur</span><span class="sxs-lookup"><span data-stu-id="b50d1-115">Sales tax</span></span>
<span data-ttu-id="b50d1-116">Hvert fyrirtæki innheimtir og greiðir skatta til ýmissa skattyfirvalda.</span><span class="sxs-lookup"><span data-stu-id="b50d1-116">Every company collects and pays taxes to various tax authorities.</span></span> <span data-ttu-id="b50d1-117">Reglur og taxtar eru mismunandi eftir landi/svæði, fylki, sýslu og borg.</span><span class="sxs-lookup"><span data-stu-id="b50d1-117">The rules and rates vary by country/region, state, county, and city.</span></span> <span data-ttu-id="b50d1-118">Þar að auki þarf að uppfæra reglur reglulega þegar kröfur skattyfirvalda breytast.</span><span class="sxs-lookup"><span data-stu-id="b50d1-118">In addition, the rules must be updated periodically when tax authorities change their requirements.</span></span> <span data-ttu-id="b50d1-119">Í VSK-kóða eru grunnupplýsingar um hversu mikið er innheimt og greitt til yfirvalda.</span><span class="sxs-lookup"><span data-stu-id="b50d1-119">Sales tax codes contain the basic information about how much you collect and pay to the authorities.</span></span> <span data-ttu-id="b50d1-120">Þegar settur er upp vsk-kóði, skilgreinirðu upphæðirnar og prósentur sem þarf að innheimta.</span><span class="sxs-lookup"><span data-stu-id="b50d1-120">When you set up sales tax codes, you define the amounts or percentages that must be collected.</span></span> <span data-ttu-id="b50d1-121">Einnig skilgreinirðu ýmsar aðferðir sem notaðar eru þegar þessum upphæðum eða prósentum er beitt á færsluupphæðir.</span><span class="sxs-lookup"><span data-stu-id="b50d1-121">You also define the various methods by which those amounts or percentages are applied to transaction amounts.</span></span> <span data-ttu-id="b50d1-122">Efnisatriðin í þessum hluta veita upplýsingar um hvernig setja á upp VSK-kóða fyrir aðferðirnar og taxtana sem skattyfirvöld krefjast.</span><span class="sxs-lookup"><span data-stu-id="b50d1-122">The topics in this section provide information about how to set up sales tax codes for the methods and rates that your tax authorities require.</span></span>







