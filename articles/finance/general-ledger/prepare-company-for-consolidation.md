---
title: Undirbúa lögaðila fyrir sameiningarferlið
description: Við sameiningu er færslum safnað saman úr nokkrum settum af lyklum lögaðila í eitt sett af lyklum lögaðila. Þetta efnisatriði útskýrir hvernig á að undirbúa lögaðila undir sameiningu.
author: jinniew
manager: AnnBe
ms.date: 10/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2018-10-30
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: f6fce69724945448f961769dd383d1047a5d13c4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990306"
---
# <a name="prepare-a-legal-entity-for-the-consolidation-process"></a><span data-ttu-id="23376-104">Undirbúa lögaðila fyrir sameiningarferlið</span><span class="sxs-lookup"><span data-stu-id="23376-104">Prepare a legal entity for the consolidation process</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="23376-105">Við sameiningu er færslum safnað saman úr nokkrum settum af lyklum lögaðila í eitt sett af lyklum lögaðila.</span><span class="sxs-lookup"><span data-stu-id="23376-105">During a consolidation, you gather transactions from several sets of legal entity accounts into a single set of legal entity accounts.</span></span> <span data-ttu-id="23376-106">Þetta efnisatriði útskýrir hvernig á að undirbúa lögaðila undir sameiningu.</span><span class="sxs-lookup"><span data-stu-id="23376-106">This topic explains how to prepare a legal entity for a consolidation.</span></span>

> [!NOTE]
> <span data-ttu-id="23376-107">Mælt er með því að nota Management reporter fyrir Microsoft Dynamics 365 Finance til að sameina fjárhagsniðurstöður fyrir marga lögaðila á sameinuðu sniði.</span><span class="sxs-lookup"><span data-stu-id="23376-107">We recommend that you use Management Reporter for Microsoft Dynamics 365 Finance to combine the financial results for multiple legal entities in a consolidated format.</span></span> <span data-ttu-id="23376-108">Management Reporter gerir kleift að stofna sameinaðar fjárhagsskýrslur yfir alla lögaðila, nota Excel til að flytja inn samstæðugögn frá öðrum upprunum og umbreyta upphæðum í hvaða fjölda skýrslugjaldmiðla sem er án þess að þurfa að keyra sameiningarferlið í Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="23376-108">Management Reporter lets you create consolidated financial reports across legal entities, use Excel to import consolidation data from other sources, and translate amounts into any number of reporting currencies without having to run the consolidation process in Dynamics 365 Finance.</span></span>

<span data-ttu-id="23376-109">Hægt er að prenta skýrslur, t.d. fjárhagsskýrslur, úr sameinuðum lögaðila.</span><span class="sxs-lookup"><span data-stu-id="23376-109">You can print reports, such as financial statements, from the consolidated legal entity.</span></span> <span data-ttu-id="23376-110">Hins vegar er ekki hægt að nota sameinaðan lögaðila fyrir daglegar færslur.</span><span class="sxs-lookup"><span data-stu-id="23376-110">However, you can't use the consolidated legal entity for daily transactions.</span></span>

<span data-ttu-id="23376-111">Hægt er að sameina gögn úr lögaðila sem nota aðra gagnagrunna en þann fyrir sameinaða lögaðilann.</span><span class="sxs-lookup"><span data-stu-id="23376-111">You can consolidate data from legal entities that use different databases than the consolidated legal entity.</span></span> <span data-ttu-id="23376-112">Þessi sameiningarferli kallast *innflutnings-sameining*.</span><span class="sxs-lookup"><span data-stu-id="23376-112">This consolidation process is referred to as an *import consolidation*.</span></span> <span data-ttu-id="23376-113">Að öðrum kosti geta lögaðilar notað sama gagnagrunn og samsteypulögaðili.</span><span class="sxs-lookup"><span data-stu-id="23376-113">Alternatively, the legal entities can use the same database as the consolidated legal entity.</span></span> <span data-ttu-id="23376-114">Þessi sameiningarferli kallast *sameining á neti*.</span><span class="sxs-lookup"><span data-stu-id="23376-114">This consolidation process is referred to as an *online consolidation*.</span></span>

<span data-ttu-id="23376-115">Sameinaði lögaðilinn safnar saman niðurstöðum og stöðum dótturfyrirtækjanna.</span><span class="sxs-lookup"><span data-stu-id="23376-115">The consolidated legal entity collects the results and balances of the subsidiaries.</span></span> <span data-ttu-id="23376-116">Til að undirbúa sameinaðan lögaðila fyrir sameiningu skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="23376-116">To prepare a consolidated legal entity for a consolidation, follow these steps.</span></span>

1. <span data-ttu-id="23376-117">Farið í **Fjárhagur \> Uppsetning \> Fyrirtæki \> Lögaðilar**.</span><span class="sxs-lookup"><span data-stu-id="23376-117">Go to **General ledger \> Setup \> Organization \> Legal entities**.</span></span>
2. <span data-ttu-id="23376-118">Veljið **Nýr** til að stofna lögaðilann sem verður sameinaður lögaðili.</span><span class="sxs-lookup"><span data-stu-id="23376-118">Select **New** to create the legal entity that will be the consolidated legal entity.</span></span>
3. <span data-ttu-id="23376-119">Veljið gátreitinn **Nota fyrir sameiningarferli fjárhags** og færið síðan inn upplýsingar um sameinaðan lögaðila.</span><span class="sxs-lookup"><span data-stu-id="23376-119">Select the **Use for financial consolidation process** check box, and then enter information about the consolidated legal entity.</span></span> <span data-ttu-id="23376-120">Verið viss um að færa inn þessar upplýsingar nákvæmlega eins og þær eiga að birtast í fjárhagsskýrslum fyrir sameinaðan lögaðila.</span><span class="sxs-lookup"><span data-stu-id="23376-120">Be sure to enter this information exactly as you want it to appear on financial statements for the consolidated legal entity.</span></span>
4. <span data-ttu-id="23376-121">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="23376-121">Close the page.</span></span>
5. <span data-ttu-id="23376-122">Veljið sameinaðan lögaðila í reitnum efst í hægra horni síðunnar og veljið því næst **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="23376-122">Select the consolidated legal entity in the field in the upper-right corner of the page, and then select **OK**.</span></span>
6. <span data-ttu-id="23376-123">Farið í **Almennur fjárhagur \> Uppsetning \> Fjárhagur**.</span><span class="sxs-lookup"><span data-stu-id="23376-123">Go to **General ledger \> Setup \> Ledger**.</span></span>
7. <span data-ttu-id="23376-124">Veljið bókhaldslykilinn, fjárhagsdagatalið, bókhaldsgjaldmiðlinn, valfrjálsan skýrslugjaldmiðil og sjálfgefna gerð gengis fyrir sameinaðan lögaðila.</span><span class="sxs-lookup"><span data-stu-id="23376-124">Select the chart of accounts, the fiscal calendar, the accounting currency, an optional reporting currency, and the default type of exchange rate for the consolidated legal entity.</span></span> 
8. <span data-ttu-id="23376-125">Farið í **Almennur fjárhagur \> Uppsetning \> Gjaldmiðill \> Gengi gjaldmiðils**.</span><span class="sxs-lookup"><span data-stu-id="23376-125">Go to **General ledger \> Setup \> Currency \> Currency exchange rates**.</span></span>
9. <span data-ttu-id="23376-126">Setja upp gengi gjaldmiðla í viðeigandi tímabila fyrir gjaldmiðla dótturfyrirtækis lögaðila.</span><span class="sxs-lookup"><span data-stu-id="23376-126">Set up currency exchange rates in relevant periods for the currencies of the subsidiary legal entities.</span></span>
10. <span data-ttu-id="23376-127">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="23376-127">Close the page.</span></span>
11. <span data-ttu-id="23376-128">Ef sameinaður lögaðili er með dótturfyrirtæki sem nota erlenda gjaldmiðla skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="23376-128">If the consolidated legal entity has subsidiaries that use foreign currencies, follow these steps:</span></span>

    1. <span data-ttu-id="23376-129">Farið í **Almennur fjárhagur \> Uppsetning \> Bókun \> Lyklar fyrir sjálfvirkar færslur**.</span><span class="sxs-lookup"><span data-stu-id="23376-129">Go to **General ledger \> Setup \> Posting \> Accounts for automatic transactions**.</span></span>
    2. <span data-ttu-id="23376-130">Í reitnum **Bókunargerð** skal velja viðeigandi lykil:</span><span class="sxs-lookup"><span data-stu-id="23376-130">In the **Posting type** field, select an appropriate account:</span></span>

        - <span data-ttu-id="23376-131">Ef lögaðili er með erlend dótturfyrirtæki sem eru fjárhagslega og rekstrarlega háð yfirlögaðilanum skal velja viðeigandi lykil fyrir bókunargerðina **Rekstrarreikningur fyrir samstæðumismun**.</span><span class="sxs-lookup"><span data-stu-id="23376-131">If the legal entity has foreign subsidiaries that are financially or operationally interdependent with the parent legal entity, select an appropriate account for the **Profit and loss account for consolidation differences** posting type.</span></span>
        - <span data-ttu-id="23376-132">Ef verið er að sameina dótturfyrirtæki sem er fjárhagslega og rekstarlega óháð yfirlögaðila eða lögaðila sem inniheldur niðurstöður nokkur dótturfyrirtæki sem eru fjárhagslega og rekstrarlega óháð yfirlögaðila, og ef verið er að nota umreikningsaðgerðir til að sameina gögnin, skal velja viðeigandi lykil fyrir bókunargerðina **Efnahagslykill fyrir samstæðumismun**.</span><span class="sxs-lookup"><span data-stu-id="23376-132">If you're consolidating a subsidiary that is financially and operationally independent of the parent legal entity, or a legal entity that contains the results of several subsidiaries that are financially and operationally independent of the parent legal entity, and if you're using translation methods to consolidate the data, select an appropriate account for the **Balance account for consolidation differences** posting type.</span></span>

    3. <span data-ttu-id="23376-133">Í reitnum **Aðallykill** skal velja aðallyklana sem á að nota fyrir breytingar á endurmati erlends gjaldmiðils.</span><span class="sxs-lookup"><span data-stu-id="23376-133">In the **Main account** field, select the main accounts that should be used for foreign currency revaluation adjustments.</span></span>
    4. <span data-ttu-id="23376-134">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="23376-134">Close the page.</span></span>

    <span data-ttu-id="23376-135">Ef sameinaður lögaðili er stofnaður snemma á tímabili er hægt að endurmeta upphæði í erlendum gjaldmiðli þar sem gengi breytist á samstæðutímabilinu.</span><span class="sxs-lookup"><span data-stu-id="23376-135">If you create the consolidated legal entity early in a period, you can revalue foreign currency amounts as exchange rates change during the consolidation period.</span></span>

<span data-ttu-id="23376-136">Sameinaður lögaðili er nú uppsettur fyrir reglubundnu vinnsluna **Sameina**.</span><span class="sxs-lookup"><span data-stu-id="23376-136">The consolidated legal entity is now set up for the **Consolidate** periodic job.</span></span> <span data-ttu-id="23376-137">Hægt er að framkvæma annaðhvort innflutningssameiningu eða sameiningu á netinu.</span><span class="sxs-lookup"><span data-stu-id="23376-137">You can do either an import consolidation or an online consolidation.</span></span>

- <span data-ttu-id="23376-138">Til að framkvæma innflutningssameiningu skal fara í **Almennur fjárhagur \> Reglubundið \> Sameina \> Sameina \[Flytja inn úr\]**.</span><span class="sxs-lookup"><span data-stu-id="23376-138">To do an import consolidation, go to **General ledger \> Periodic \> Consolidate \> Consolidate \[Import from\]**.</span></span>
- <span data-ttu-id="23376-139">Til að framkvæma sameiningu á netinu skal fara í **Almennur fjárhagur \> Reglubundið \> Sameina \> Sameina \[Á netinu\]**.</span><span class="sxs-lookup"><span data-stu-id="23376-139">To do an online consolidation, go to **General ledger \> Periodic \> Consolidate \> Consolidate \[Online\]**.</span></span>

> [!NOTE]
> <span data-ttu-id="23376-140">Áður en hægt er að keyra sameininguna þarf að undirbúa lögaðila dótturfyrirtækis fyrir sameiningu.</span><span class="sxs-lookup"><span data-stu-id="23376-140">Before you can process the consolidation, you must prepare the subsidiary legal entities for consolidation.</span></span> <span data-ttu-id="23376-141">Frekari upplýsingar er að finna í [Setja upp dótturfyrirtæki lögaðila fyrir sameiningu](set-up-subsidiary-company-for-consolidation.md).</span><span class="sxs-lookup"><span data-stu-id="23376-141">For more information, see [Set up a subsidiary legal entity for consolidation](set-up-subsidiary-company-for-consolidation.md).</span></span>
