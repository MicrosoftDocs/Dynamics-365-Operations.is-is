---
title: Fjárhagsjafnanir
description: Þetta efnisatriði útskýrir hvernig á að nota síðu fjárhagsjafnana til að jafna fjárhagsfærslur og bakfærslur.
author: mikefalkner
manager: aolson
ms.date: 09/28/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransSettlement
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-11-30
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: d41a69bed3d1340736cc7df35aa3ded032d4d79d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4444293"
---
# <a name="ledger-settlements"></a><span data-ttu-id="8aef1-103">Fjárhagsjafnanir</span><span class="sxs-lookup"><span data-stu-id="8aef1-103">Ledger settlements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8aef1-104">Fjárhagsjafnanir gerir þér kleift að samsvara debet- og kreditfærslur í fjárhagnum og merkja þau sem jöfnuð.</span><span class="sxs-lookup"><span data-stu-id="8aef1-104">Ledger settlements let you match debit and credit transactions in the general ledger, and mark them as settled.</span></span> <span data-ttu-id="8aef1-105">Þannig geturðu tryggt að tengdar færslur hafi verið hreinsaðar.</span><span class="sxs-lookup"><span data-stu-id="8aef1-105">In this way, you can make sure that related transactions have been cleared.</span></span> <span data-ttu-id="8aef1-106">Þú getur einnig bakfært ef þær voru gerðar fyrir mistök.</span><span class="sxs-lookup"><span data-stu-id="8aef1-106">You can also reverse settlements if they were made by mistake.</span></span>

## <a name="enable-advanced-ledger-settlements"></a><span data-ttu-id="8aef1-107">Virkja ítarleg fjárhagsuppgjör</span><span class="sxs-lookup"><span data-stu-id="8aef1-107">Enable advanced ledger settlements</span></span>

<span data-ttu-id="8aef1-108">Síða ítarlegs fjárhagsuppgjörs veitir frekari getu til að sía og velja færslur.</span><span class="sxs-lookup"><span data-stu-id="8aef1-108">The advanced ledger settlements page provides additional capabilities for filtering and selecting transactions.</span></span> <span data-ttu-id="8aef1-109">Til að virkja síðu ítarlegs fjárhagsuppgjörs skaltu fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="8aef1-109">To enable advanced ledger settlements page, follow these steps.</span></span>

1. <span data-ttu-id="8aef1-110">Veldu **Fjárhagur** \> **Fjárhagsuppsetning** \> **Færibreytur fyrir fjárhag**.</span><span class="sxs-lookup"><span data-stu-id="8aef1-110">Select **General ledger** \> **Ledger setup** \> **General ledger parameters**.</span></span> 
2. <span data-ttu-id="8aef1-111">Á **Fjárhagsuppgjörs** flipanum skaltu stilla **Ítarlegt fjárhagsuppgjör** á **Já** til að kveikja á virkni ítarlega fjárhagsuppgjörsins.</span><span class="sxs-lookup"><span data-stu-id="8aef1-111">On the **Ledger settlements** tab, set the **Advanced ledger settlement** option to **Yes** to turn on the advanced ledger settlement functionality.</span></span> <span data-ttu-id="8aef1-112">Ítarlega **Fjárhagsuppgjör** síðu verður notaður þegar þú velur **Fjárhagsuppgjör** í **Reglubundin verkefni**.</span><span class="sxs-lookup"><span data-stu-id="8aef1-112">The advanced **Ledger settlements** page will be used when you select **Ledger settlements** in the **Periodic tasks**.</span></span> 
3. <span data-ttu-id="8aef1-113">Þú verður að slá inn lista yfir reikninga til að nota fyrir fjárhagsuppgjör fyrir hvern bókhaldslykil.</span><span class="sxs-lookup"><span data-stu-id="8aef1-113">You must enter the list of accounts to use for ledger settlements for each chart of accounts.</span></span> <span data-ttu-id="8aef1-114">Þessi listi er notaður til að sía lista yfir færslur sem birtast á **Fjárhagsuppgjör** síðu.</span><span class="sxs-lookup"><span data-stu-id="8aef1-114">This list is used to filter the list of transactions that appears on the **Ledger settlements** page.</span></span> <span data-ttu-id="8aef1-115">Í **Listi yfir reikninga** skaltu velja bókhaldslykil og velja síðan **Nýr** til að bæta við nýjum reikningum á listann.</span><span class="sxs-lookup"><span data-stu-id="8aef1-115">In the **Chart of accounts** list, select a chart of accounts, and then select **New** to add new accounts to the list.</span></span>

## <a name="settle-transactions-by-using-the-advanced-ledger-settlements-page"></a><span data-ttu-id="8aef1-116">Settu upp færslur með því að nota síðu ítarlega fjárhagsuppgjörsins</span><span class="sxs-lookup"><span data-stu-id="8aef1-116">Settle transactions by using the advanced ledger settlements page</span></span>

<span data-ttu-id="8aef1-117">Til að jafn fjárhagsfærslur skaltu fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="8aef1-117">To settle ledger transactions, follow these steps.</span></span>

1. <span data-ttu-id="8aef1-118">Veldu **Fjárhagur** \> **Reglubundin verkefni** \> **Fjárhagsuppgjör**.</span><span class="sxs-lookup"><span data-stu-id="8aef1-118">Select **General ledger** \> **Periodic tasks** \> **Ledger settlements**.</span></span>
2. <span data-ttu-id="8aef1-119">Stilltu síurnar efst á síðunni:</span><span class="sxs-lookup"><span data-stu-id="8aef1-119">Set the filters at the top of the page:</span></span>

    - <span data-ttu-id="8aef1-120">Veldu dagsetningarbil, eða veldu **Kóða dagsetningarbils** til að fylla sjálfkrafa inn tímabilið.</span><span class="sxs-lookup"><span data-stu-id="8aef1-120">Select a date range, or select **Date interval code** to automatically fill in the date range.</span></span>
    - <span data-ttu-id="8aef1-121">Breyttu bókunarlaginu eins og þú þarfnast.</span><span class="sxs-lookup"><span data-stu-id="8aef1-121">Change the posting layer as you require.</span></span>
    - <span data-ttu-id="8aef1-122">Til að birta fjárhagslykil og víddir sér skaltu velja fjárhagsvíddarsamstæðu.</span><span class="sxs-lookup"><span data-stu-id="8aef1-122">To show the ledger account and dimensions separately, select a financial dimension set.</span></span>

3. <span data-ttu-id="8aef1-123">Veldu **Birta færslur** til að sýna allar færslur sem samsvara síunum sem þú stillir og lista yfir reikninga sem þú tilgreindir þegar þú settir upp bókhaldslykilinn í fyrri hlutanum.</span><span class="sxs-lookup"><span data-stu-id="8aef1-123">Select **Display transactions** to show all the transactions that match the filters that you set and the list of accounts that you specified when you set up the chart of accounts list in the previous section.</span></span> <span data-ttu-id="8aef1-124">Ef þú breytir einhverjum síum eða víddarsamstæðum þarftu að velja **Birta færslur** aftur.</span><span class="sxs-lookup"><span data-stu-id="8aef1-124">If you change any of the filters or the dimension sets, you must select **Display transactions** again.</span></span>
4. <span data-ttu-id="8aef1-125">Veldu eina eða fleiri línur sem þú ert að íhuga fyrir jöfnun.</span><span class="sxs-lookup"><span data-stu-id="8aef1-125">Select one or more lines that you're considering for settlement.</span></span> <span data-ttu-id="8aef1-126">Virði **Valin upphæð** reitinn efst á síðunni eykst eða lækkar með heildarupphæðinni á línum sem þú valdir.</span><span class="sxs-lookup"><span data-stu-id="8aef1-126">The value of the **Selected amount** field at the top of the page increases or decreases by the total amount on the lines that you selected.</span></span>
5. <span data-ttu-id="8aef1-127">Þegar þú hefur lokið við að velja færslur skaltu velja **Merkja sem valið**.</span><span class="sxs-lookup"><span data-stu-id="8aef1-127">After you've finished selecting transactions, select **Mark selected**.</span></span> <span data-ttu-id="8aef1-128">Gátmerki birtist í **Merkta** dálknum fyrir hverja færslu sem þú valdir.</span><span class="sxs-lookup"><span data-stu-id="8aef1-128">A check mark appears in the **Marked** column for each transaction that you selected.</span></span> <span data-ttu-id="8aef1-129">Auk þess eykst gildið **Valin upphæð** svæðisins fyrir ofan hnitanetið eða lækkar með heildarupphæðinni á línunum sem þú merktir.</span><span class="sxs-lookup"><span data-stu-id="8aef1-129">Additionally, the value of the **Marked amount** field above the grid increases or decreases by the total amount on the lines that you marked.</span></span>
6. <span data-ttu-id="8aef1-130">Þegar **Valin upphæð** gildi er **0** (núll) skaltu velja **Jafna valdar færslur**.</span><span class="sxs-lookup"><span data-stu-id="8aef1-130">When the **Marked amount** value is **0** (zero), select **Settle marked transactions**.</span></span> <span data-ttu-id="8aef1-131">Staða valinna færslna er uppfært í **Jafnað**.</span><span class="sxs-lookup"><span data-stu-id="8aef1-131">The status of the marked transactions is updated to **Settled**.</span></span>

## <a name="make-transactions-easier-to-find"></a><span data-ttu-id="8aef1-132">Gera það auðveldara að finna færslur</span><span class="sxs-lookup"><span data-stu-id="8aef1-132">Make transactions easier to find</span></span>

<span data-ttu-id="8aef1-133">**Fjárhagsuppgjör** síðan inniheldur aðgerðir sem auðveldar að sjá færslurnar sem þarf að jafna.</span><span class="sxs-lookup"><span data-stu-id="8aef1-133">The **Ledger settlements** page includes capabilities that make it easier to see the transactions that you need for settlement.</span></span>

- <span data-ttu-id="8aef1-134">**Fjarlægja val** hnappinn hreinsar **Valið** reitinn fyrir allar línur sem eru valdir.</span><span class="sxs-lookup"><span data-stu-id="8aef1-134">The **Unmark selected** button clears the **Marked** field for all lines that are selected.</span></span>
- <span data-ttu-id="8aef1-135">**Valið** sían gerir þér kleift að sía færslur miðað við hvort **Valið** reitinn fyrir þá sé valinn eða hreinsaður.</span><span class="sxs-lookup"><span data-stu-id="8aef1-135">The **Marked** filter lets you filter transactions based on whether the **Marked** field for them is selected or cleared.</span></span>
- <span data-ttu-id="8aef1-136">**Staða** sía gerir þér kleift að sía færslur eftir því hvort staða þeirra er **Jöfnuð** eða **Ekki jöfnuð**.</span><span class="sxs-lookup"><span data-stu-id="8aef1-136">The **Status** filter lets you filter transactions based on whether their status is **Settled** or **Not settled**.</span></span>
- <span data-ttu-id="8aef1-137">Með **Raða eftir algildri upphæð** hnappur er hægt að raða upphæðunum eftir algildri upphæð, þannig að þú getur sameinað debet og kredit að sömu upphæð.</span><span class="sxs-lookup"><span data-stu-id="8aef1-137">The **Sort by absolute amount** button lets you sort the amounts by absolute value, so that you can group together debits and credits that have the same amount.</span></span>

## <a name="reverse-a-settlement"></a><span data-ttu-id="8aef1-138">Bakfæra jöfnun</span><span class="sxs-lookup"><span data-stu-id="8aef1-138">Reverse a settlement</span></span>

<span data-ttu-id="8aef1-139">Þú getur bakfært jöfnun sem var gerð fyrir mistök.</span><span class="sxs-lookup"><span data-stu-id="8aef1-139">You can reverse a settlement that was made by mistake.</span></span>

1. <span data-ttu-id="8aef1-140">Fylgdu skrefum 1 til 3 í „Jafna færslur með því að nota síðu fyrir ítarleg fjárhagsuppgjör“ til að sýna færslurnar sem þú ert að leita að.</span><span class="sxs-lookup"><span data-stu-id="8aef1-140">Follow steps 1 through 3 in the "Settle transactions by using advanced ledger settlements page" section to show the transactions that you're looking for.</span></span>
2. <span data-ttu-id="8aef1-141">Í **Staða** síu, veldu **Jöfnuð**.</span><span class="sxs-lookup"><span data-stu-id="8aef1-141">In the **Status** filter, select **Settled**.</span></span>
3. <span data-ttu-id="8aef1-142">Veldu eina eða fleiri línur sem þú ert að íhuga að bakfæra.</span><span class="sxs-lookup"><span data-stu-id="8aef1-142">Select one or more lines that you're considering for reversal.</span></span> <span data-ttu-id="8aef1-143">Virði **Valin upphæð** reitinn efst á síðunni eykst eða lækkar með heildarupphæðinni á línum sem þú valdir.</span><span class="sxs-lookup"><span data-stu-id="8aef1-143">The value of the **Selected amount** field at the top of the page increases or decreases by the total amount on the lines that you selected.</span></span>
4. <span data-ttu-id="8aef1-144">Þegar þú hefur lokið við að velja færslur skaltu velja **Merkja sem valið**.</span><span class="sxs-lookup"><span data-stu-id="8aef1-144">After you've finished selecting transactions, select **Mark selected**.</span></span> <span data-ttu-id="8aef1-145">Gátmerki birtist í **Merkta** dálknum fyrir hverja færslu sem þú valdir.</span><span class="sxs-lookup"><span data-stu-id="8aef1-145">A check mark appears in the **Marked** column for each transaction that you selected.</span></span> <span data-ttu-id="8aef1-146">Þar að auki virði **Valin upphæð** reitinn efst á síðunni eykst eða lækkar með heildarupphæðinni á línum sem þú valdir.</span><span class="sxs-lookup"><span data-stu-id="8aef1-146">Additionally, the value of the **Marked amount** field at the top of the page increases or decreases by the total amount on the lines that you marked.</span></span>
5. <span data-ttu-id="8aef1-147">Þegar **Valin upphæð** gildi er **0** (núll) skaltu velja **Bakfæra valdar færslur**.</span><span class="sxs-lookup"><span data-stu-id="8aef1-147">When the **Marked amount** value is **0** (zero), select **Reverse marked transactions**.</span></span> <span data-ttu-id="8aef1-148">Staða merktra færslna er uppfært í **Ekki uppgert**.</span><span class="sxs-lookup"><span data-stu-id="8aef1-148">The status of the marked transactions is updated to **Not settled**.</span></span>

## <a name="update-the-list-of-accounts-that-are-included-in-the-list-of-transactions"></a><span data-ttu-id="8aef1-149">Uppfærðu lista yfir reikninga sem eru í listanum yfir færslur</span><span class="sxs-lookup"><span data-stu-id="8aef1-149">Update the list of accounts that are included in the list of transactions</span></span>

<span data-ttu-id="8aef1-150">Veldu **Lyklar fjárhagsuppgjörs** til að opna svarglugga þar sem þú getur breytt reikningum sem eru innifalin í listanum yfir færslur.</span><span class="sxs-lookup"><span data-stu-id="8aef1-150">Select **Ledger settlement accounts** to open a dialog box where you can edit the accounts that are included in the list of transactions.</span></span> <span data-ttu-id="8aef1-151">Veldu **Nýr** til að bæta við nýjum reikningum á listann.</span><span class="sxs-lookup"><span data-stu-id="8aef1-151">Select **New** to add new accounts to the list.</span></span> <span data-ttu-id="8aef1-152">Þessi listi er notaður til að sía lista yfir færslur sem birtast á **Fjárhagsuppgjör** síðu.</span><span class="sxs-lookup"><span data-stu-id="8aef1-152">This list is used to filter the list of transactions that appears on the **Ledger settlements** page.</span></span>
