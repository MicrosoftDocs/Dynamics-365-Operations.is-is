---
title: Vinnusvæði bankakerfis
description: Í þessu efnisatriði er að finna upplýsingar um vinnusvæði bankakerfis. Þetta vinnusvæði sýnir upplýsingar sem tengjast bankareikningum fyrirtækis og felur í sér samtöluyfirlit og greiningarsíðu. Samtöluyfirlitið sýnir samantektarreiti, upplýsingar um bankareikninga, myndrit og tengdar upplýsingar. Greiningarsíðan notar getu Microsoft Power BI til að sýna myndefni sem tengjast stöðum bankareikninga.
author: saraschi2
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankTreasurerWorkspace
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 7fcb56440adf86194e9ae05957349dd5ebe89ce7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985487"
---
# <a name="bank-management-workspace"></a><span data-ttu-id="940f7-106">Vinnusvæði bankakerfis</span><span class="sxs-lookup"><span data-stu-id="940f7-106">Bank management workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="940f7-107">Vinnusvæðið **Bankakerfi** birtir upplýsingar sem tengjast bankareikningum fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="940f7-107">The **Bank management** workspace shows information that is related to company bank accounts.</span></span> <span data-ttu-id="940f7-108">Í þessu vinnusvæði er yfirlitið **Samtölur** og síðan **Greiningar**.</span><span class="sxs-lookup"><span data-stu-id="940f7-108">This workspace includes a **Summary** view and an **Analytics** page.</span></span> <span data-ttu-id="940f7-109">Yfirlitið **Samtölur** sýnir samantektarreiti, upplýsingar um bankareikninga, myndrit og tengdar upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="940f7-109">The **Summary** view shows summary tiles, bank account information, a balance chart, and related information.</span></span> <span data-ttu-id="940f7-110">Síðan **Greiningar** notar getu Microsoft Power BI til að sýna myndefni sem tengjast stöðum bankareikninga.</span><span class="sxs-lookup"><span data-stu-id="940f7-110">The **Analytics** page uses the capabilities of Microsoft Power BI to show visuals that are related to bank account balances.</span></span>

## <a name="summary-view"></a><span data-ttu-id="940f7-111">Samtöluyfirlit</span><span class="sxs-lookup"><span data-stu-id="940f7-111">Summary view</span></span>

### <a name="summary"></a><span data-ttu-id="940f7-112">Samantekt</span><span class="sxs-lookup"><span data-stu-id="940f7-112">Summary</span></span>

<span data-ttu-id="940f7-113">Reitirnir í hlutanum **Samantekt** sýna yfirlit yfir bankareikninga og veita skjótan aðgang að þeim síðum sem oftast eru notaðar.</span><span class="sxs-lookup"><span data-stu-id="940f7-113">The tiles in the **Summary** section give an overview of your bank accounts and provide quick access to the pages that you most often have to use.</span></span> <span data-ttu-id="940f7-114">Upplýsingar um bankaafstemmingu eru bundnar við virkni ítarlegrar bankaafstemmingar.</span><span class="sxs-lookup"><span data-stu-id="940f7-114">The bank reconciliation information is specific to the Advanced bank reconciliation functionality.</span></span> <span data-ttu-id="940f7-115">Upplýsingar eru aðeins í boði fyrir þá bankareikninga þar sem valmöguleikinn **Ítarleg bankaafstemming** er stilltur á **Já** á síðunni **Bankareikningur**.</span><span class="sxs-lookup"><span data-stu-id="940f7-115">Information is included only for those bank accounts that have the **Advanced bank reconciliation** option set to **Yes** on the **Bank account** page.</span></span> <span data-ttu-id="940f7-116">Hægt er að flytja rafrænar bankaskrár bankareikninga fyrir alla lögaðila úr hlutanum **Samantekt**.</span><span class="sxs-lookup"><span data-stu-id="940f7-116">From the **Summary** section, you can import electronic bank files for bank accounts across all legal entities.</span></span>

### <a name="bank-accounts"></a><span data-ttu-id="940f7-117">Bankareikningar</span><span class="sxs-lookup"><span data-stu-id="940f7-117">Bank accounts</span></span>

<span data-ttu-id="940f7-118">Hver bankareikningur lögaðila er sýndur með spjaldi í hlutanum **Bankareikningar**.</span><span class="sxs-lookup"><span data-stu-id="940f7-118">Each bank account in the legal entity is represented by a card in the **Bank accounts** section.</span></span> <span data-ttu-id="940f7-119">Núverandi staða er sýnd og hægt er að kafa niður í færslurnar sem mynda heildarstöðuna.</span><span class="sxs-lookup"><span data-stu-id="940f7-119">The current balance is shown, and you can drill down to the transactions that make up that summary balance amount.</span></span> <span data-ttu-id="940f7-120">Í upphæðinni í **Færslur á millilykil** er einnig hægt að kafa niður í færslurnar sem mynda heildarupphæðina.</span><span class="sxs-lookup"><span data-stu-id="940f7-120">The **Bridged transactions** amount also lets you drill down to the transactions that make up that summary amount.</span></span> <span data-ttu-id="940f7-121">Færslur á millilykil eru allar færslur í bið sem hafa verið bókaðar með milliaðgerðum, en hafa ekki enn verið afstemmdar.</span><span class="sxs-lookup"><span data-stu-id="940f7-121">Bridged transactions are any pending transactions that have been posted by using bridging functionality, but that haven't yet been cleared.</span></span> <span data-ttu-id="940f7-122">Upphæðin í **Ógreidd staða** er núverandi staða að frádregnum færslum á millilykil eða færslum í bið.</span><span class="sxs-lookup"><span data-stu-id="940f7-122">The **Pending balance** amount is the current balance minus the bridged, or pending, transactions.</span></span>

<span data-ttu-id="940f7-123">Spjaldið sýnir einnig hvenær bankareikningurinn var síðast afstemmdur.</span><span class="sxs-lookup"><span data-stu-id="940f7-123">The card also shows when the bank account was last reconciled.</span></span> <span data-ttu-id="940f7-124">Þessar upplýsingar birtast aðeins ef ítarleg bankaafstemming er virkjuð fyrir bankareikninginn.</span><span class="sxs-lookup"><span data-stu-id="940f7-124">This information is shown only if Advanced bank reconciliation is enabled for the bank account.</span></span>

### <a name="balance"></a><span data-ttu-id="940f7-125">Efnahagur</span><span class="sxs-lookup"><span data-stu-id="940f7-125">Balance</span></span>

<span data-ttu-id="940f7-126">Myndritið **Staða** sýnir annaðhvort sögulegar stöðuupplýsingar fyrir bankareikninginn sem er valinn í hlutanum **Bankareikningar** eða samantekt á sögulegum stöðuupplýsingum fyrir alla bankareikninga lögaðilans.</span><span class="sxs-lookup"><span data-stu-id="940f7-126">The **Balance** chart shows either historic balance information for the bank account that is selected in the **Bank accounts** section or a summary of historic balance information for all bank accounts in the legal entity.</span></span> <span data-ttu-id="940f7-127">Þessar upplýsingar eru tiltækar fyrir ýmis tímabil, núverandi viku, núverandi mánuð, núverandi ár, síðustu fimm ár og öll tímabil (saga bankareiknings frá upphafi).</span><span class="sxs-lookup"><span data-stu-id="940f7-127">This information is available for various periods: the current week, the current month, the current year, the last five years, and all periods (the full history of the bank account).</span></span> 

<span data-ttu-id="940f7-128">Sé verið að skoða myndritið **Staða** fyrir einn bankareikning birtast sögulegar stöðuupplýsingar í gjaldmiðli bankareikningsins.</span><span class="sxs-lookup"><span data-stu-id="940f7-128">If you're viewing the **Balance** chart for a single bank account, the historic balances are shown in the bank account currency.</span></span> <span data-ttu-id="940f7-129">Sé verið að skoða myndritið fyrir alla bankareikninga lögaðilans birtast sögulegar stöðuupplýsingar í bókhaldsgjaldmiðli.</span><span class="sxs-lookup"><span data-stu-id="940f7-129">If you're viewing the chart for all bank accounts in the legal entity, the historic balances are shown in the accounting currency.</span></span>

<span data-ttu-id="940f7-130">Upplýsingar um hvenær gögn voru síðast uppfærð birtast efst í myndritinu.</span><span class="sxs-lookup"><span data-stu-id="940f7-130">Information about when the data was last updated appears at the top of the chart.</span></span> <span data-ttu-id="940f7-131">Hægt er að uppfæra gögn eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="940f7-131">You can update the data as you require.</span></span>

### <a name="related-information"></a><span data-ttu-id="940f7-132">Tengdar upplýsingar</span><span class="sxs-lookup"><span data-stu-id="940f7-132">Related information</span></span>

<span data-ttu-id="940f7-133">Úr hlutanum **Tengdar upplýsingar** er hægt að opna síðuna **Almenn færslubók** til að framkvæma bankamillifærslur.</span><span class="sxs-lookup"><span data-stu-id="940f7-133">From the **Related information** section, you can open the **General journal** page to complete bank transfers.</span></span> <span data-ttu-id="940f7-134">Einnig er á fljótlegan hátt hægt að opna síðurnar **Bankafærslur** og **Færslur á millilykil**.</span><span class="sxs-lookup"><span data-stu-id="940f7-134">You can also quickly open the **Bank transactions** and **Bridged transactions** pages.</span></span>

## <a name="analytics-view"></a><span data-ttu-id="940f7-135">Greiningaryfirlit</span><span class="sxs-lookup"><span data-stu-id="940f7-135">Analytics view</span></span>

<span data-ttu-id="940f7-136">Síðan **Greiningar** hefur að geyma mikilvæga mælikvarða um bankareikninga í núverandi fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="940f7-136">The **Analytics** page provides important metrics about the bank accounts in the current company.</span></span> <span data-ttu-id="940f7-137">Eftirfarandi myndræn framsetning er tiltæk á síðunni:</span><span class="sxs-lookup"><span data-stu-id="940f7-137">The following visualizations are available on the page:</span></span>

-   <span data-ttu-id="940f7-138">Heildarupphæð bankainnistæðu í gjaldmiðli kerfisins</span><span class="sxs-lookup"><span data-stu-id="940f7-138">Total bank balance in system currency</span></span>
-   <span data-ttu-id="940f7-139">Staða eftir lögaðila</span><span class="sxs-lookup"><span data-stu-id="940f7-139">Balance by legal entity</span></span>
-   <span data-ttu-id="940f7-140">Raunstaða samanborið við áætlaða stöðu dagsins í gjaldmiðli bankareikningsins</span><span class="sxs-lookup"><span data-stu-id="940f7-140">Today’s actual vs forecasted balance in bank account currency</span></span>
-   <span data-ttu-id="940f7-141">Staða eftir bankareikningi</span><span class="sxs-lookup"><span data-stu-id="940f7-141">Balance by bank account</span></span>
-   <span data-ttu-id="940f7-142">Staða eftir gjaldmiðlum</span><span class="sxs-lookup"><span data-stu-id="940f7-142">Balance by currency</span></span>

<span data-ttu-id="940f7-143">Hægt er að skoða bankagreiningu fyrir öll fyrirtæki á vinnusvæðinu **Yfirlit yfir reiðufé - öll fyrirtæki**.</span><span class="sxs-lookup"><span data-stu-id="940f7-143">You can view bank analytics across all companies from the **Cash overview – all companies** workspace.</span></span> <span data-ttu-id="940f7-144">Frekari upplýsingar má finna á [Yfirlit yfir reiðufé Power BI efni](Cash-Overview-Power-BI-content.md).</span><span class="sxs-lookup"><span data-stu-id="940f7-144">For more information, see [Cash overview Power BI content](Cash-Overview-Power-BI-content.md).</span></span>
