---
title: aðgerðaleit
description: Þessi grein lýsir aðgerðaleit í Microsoft Dynamics 365 for Finance and Operations. Aðgerðleit hjálpar þér að finna og keyra aðgerðir á síðu.
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 62303
ms.assetid: 62c70de0-fdde-4417-8e08-0583fb095a40
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 960c715c487fbda5d93630327f07380e6d8fbd3c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1547032"
---
# <a name="action-search"></a><span data-ttu-id="9a821-104">Aðgerðaleit</span><span class="sxs-lookup"><span data-stu-id="9a821-104">Action search</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9a821-105">Þessi grein lýsir aðgerðaleit í Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9a821-105">This article describes the action search functionality in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="9a821-106">Aðgerðleit hjálpar þér að finna og keyra aðgerðir á síðu.</span><span class="sxs-lookup"><span data-stu-id="9a821-106">Action search will help you find and run actions on a page.</span></span>

## <a name="introduction"></a><span data-ttu-id="9a821-107">Inngangur</span><span class="sxs-lookup"><span data-stu-id="9a821-107">Introduction</span></span>

<span data-ttu-id="9a821-108">Síður í Microsoft Dynamics 365 for Finance and Operations birta fyrst og fremst skipanir í aðgerðarúðum, bæði í staðlaðri aðgerðarúðu sem birtist efst á síðunni og á verkfærastikum sem birtast í ýmsum köflum síðunnar.</span><span class="sxs-lookup"><span data-stu-id="9a821-108">Pages in Microsoft Dynamics 365 for Finance and Operations primarily expose commands on Action Panes, both the standard Action Pane that appears at the top of a page and the toolbars that appear in various sections of the page.</span></span> <span data-ttu-id="9a821-109">Í fyrri útgáfum leyfir Lykillábending þér að fá aðgang fljótt á einhvern hnappinn á aðgerðarúðum með því að ýta á Alt-takkann og síðan röð af stöfum.</span><span class="sxs-lookup"><span data-stu-id="9a821-109">In previous versions, a Key Tips feature let you quickly access any button on an Action Pane by pressing the Alt key and then a series of letters.</span></span>

<span data-ttu-id="9a821-110">[![keyTipsAX6](./media/keytipsax6.png)](./media/keytipsax6.png)</span><span class="sxs-lookup"><span data-stu-id="9a821-110">[![keyTipsAX6](./media/keytipsax6.png)](./media/keytipsax6.png)</span></span>

<span data-ttu-id="9a821-111">Hins vegar eru Ábendingar fyrir lykla í gildandi útgáfu Finance and Operations ekki lengur tiltækar, en þeim hefur verið skipt út fyrir eiginleikann aðgerðaleit.</span><span class="sxs-lookup"><span data-stu-id="9a821-111">However, in the current version of Finance and Operations, Key Tips are no longer available but have been replaced by the action search feature.</span></span> <span data-ttu-id="9a821-112">Þessi nýi eiginleiki gerir þér kleift að leita fljótt og keyra hnapp af einhverju af sýnilegu aðgerðarúðunum.</span><span class="sxs-lookup"><span data-stu-id="9a821-112">This new feature lets you quickly search for and run a button from any visible Action Pane.</span></span>

## <a name="using-action-search"></a><span data-ttu-id="9a821-113">Notkun Aðgerðaleitar</span><span class="sxs-lookup"><span data-stu-id="9a821-113">Using action search</span></span>

<span data-ttu-id="9a821-114">Til að nota eiginleikann aðgerðaleið, fylgið þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="9a821-114">To use the action search feature, follow these steps.</span></span>

1. <span data-ttu-id="9a821-115">Á Aðgerðasvæðinu skal smella á **aðgerðaleit** svæði.</span><span class="sxs-lookup"><span data-stu-id="9a821-115">On the Action Pane, click in the **action search** field.</span></span> <span data-ttu-id="9a821-116">(**aðgerðaleit** inniheldur stækkunarglerstákn.)</span><span class="sxs-lookup"><span data-stu-id="9a821-116">(The **action search** field contains a magnifying glass icon.)</span></span>
2. <span data-ttu-id="9a821-117">Slá öllum eða hluta af nafni hnapps sem þú vilt keyra.</span><span class="sxs-lookup"><span data-stu-id="9a821-117">Type all or part of the name of the button that you want to run.</span></span> <span data-ttu-id="9a821-118">Þú getur einnig leitað með því að nota orð úr leið hnappsins.</span><span class="sxs-lookup"><span data-stu-id="9a821-118">You can also search by using words from the button's "path."</span></span> <span data-ttu-id="9a821-119">(Nánari upplýsingar má nálgast í næsta kafla þessarar greinar.) Yfirleitt, hnappur birtist ofarlega á lista yfir niðurstöður þegar búið er að slá inn tvo til fjóra stafi.</span><span class="sxs-lookup"><span data-stu-id="9a821-119">(For more information, see the next section of this article.) Typically, a button will appear near the top of the results list after you've typed two to four characters.</span></span>
3. <span data-ttu-id="9a821-120">Finna og keyra hnappurinn í lista yfir niðurstöður (með því að nota músina eða lyklaborð).</span><span class="sxs-lookup"><span data-stu-id="9a821-120">Find and run the button in the results list (by using your mouse or keyboard).</span></span>

<span data-ttu-id="9a821-121">Eftir að hnappurinn er keyrður fer áhersla á síðustu stöðu á síðunni, þannig að hægt er að halda áfram að vinna.</span><span class="sxs-lookup"><span data-stu-id="9a821-121">After the button is run, the focus is returned to your last position on the page, so that you can continue to work.</span></span>

<span data-ttu-id="9a821-122">[![action-search-field](./media/action-search-field.png)](./media/action-search-field.png)</span><span class="sxs-lookup"><span data-stu-id="9a821-122">[![action-search-field](./media/action-search-field.png)](./media/action-search-field.png)</span></span>

<span data-ttu-id="9a821-123">Einnig er hægt að hefja aðgerðaleit með því að ýta á Ctrl +/ eða Alt + Q.</span><span class="sxs-lookup"><span data-stu-id="9a821-123">You can also start action search by pressing Ctrl+/ or Alt+Q.</span></span> <span data-ttu-id="9a821-124">Styðjið á flýtilykli aftur til að snúa aftur áherslu að síðasta stað á síðunni.</span><span class="sxs-lookup"><span data-stu-id="9a821-124">Press the keyboard shortcut again to return the focus to your last position on the page.</span></span>

## <a name="understanding-the-results-list"></a><span data-ttu-id="9a821-125">Skilningur á lista yfir niðurstöður</span><span class="sxs-lookup"><span data-stu-id="9a821-125">Understanding the results list</span></span>

<span data-ttu-id="9a821-126">Í Finance and Operations er oft nauðsynlegt að vita bæði staðsetningu og efni hnapps til að skilja tilgang þess hnapps til fulls.</span><span class="sxs-lookup"><span data-stu-id="9a821-126">Often, in Finance and Operations, you must know both the location and the context of a button to fully understand the purpose of that button.</span></span> <span data-ttu-id="9a821-127">Þess vegna birtast viðbótarupplýsingar fyrir hvern hlut í listanum, til að hjálpa þér að skilja nákvæmlega hvaða hnappar birtast í listanum.</span><span class="sxs-lookup"><span data-stu-id="9a821-127">Therefore, additional information is shown for each item in the results list, to help you understand exactly which buttons appear in the list.</span></span> <span data-ttu-id="9a821-128">Einkum er "slóð" hnappsins sýnd.</span><span class="sxs-lookup"><span data-stu-id="9a821-128">In particular, the "path" of the button is shown.</span></span> <span data-ttu-id="9a821-129">Þessa slóð gætu innihaldið merki eftirfarandi eininga notendaviðmóts, eins og:</span><span class="sxs-lookup"><span data-stu-id="9a821-129">This path might include the labels of the following UI elements, as relevant:</span></span>

- <span data-ttu-id="9a821-130">Flipinn aðgerðarúða.</span><span class="sxs-lookup"><span data-stu-id="9a821-130">Action Pane tab</span></span>
- <span data-ttu-id="9a821-131">Hnappaflokkur</span><span class="sxs-lookup"><span data-stu-id="9a821-131">Button group</span></span>
- <span data-ttu-id="9a821-132">Valmyndarhnapp (ef hnappurinn er inní valmyndarhnapp)</span><span class="sxs-lookup"><span data-stu-id="9a821-132">Menu button (if the button is inside a menu button)</span></span>
- <span data-ttu-id="9a821-133">Skiltákn valmyndar (sé hnappurinn innan nefnds flokks innan valmyndarhnapps)</span><span class="sxs-lookup"><span data-stu-id="9a821-133">Menu separator (if the button is inside a named group inside a menu button)</span></span>
- <span data-ttu-id="9a821-134">Flokkur eða flipa á síðu (til dæmis, heiti flýtiflipa)</span><span class="sxs-lookup"><span data-stu-id="9a821-134">Group or tab on the page (for example, the name of a FastTab)</span></span>

<span data-ttu-id="9a821-135">Til dæmis, var fært inn **tot** í **aðgerðaleit** svæðinu og ert nú að skoða niðurstöður lista.</span><span class="sxs-lookup"><span data-stu-id="9a821-135">For example, you typed **tot** in the **action search** field and are now examining the results list.</span></span> <span data-ttu-id="9a821-136">Fyrsta færslan, fyrir hnapp sem er kallast **Samtala**, er upplýst.</span><span class="sxs-lookup"><span data-stu-id="9a821-136">The first entry, for a button that is named **Totals**, is highlighted.</span></span> <span data-ttu-id="9a821-137">Hnappaslóðin **Sölupöntun** &gt; **Skoða** er einnig sýnd.</span><span class="sxs-lookup"><span data-stu-id="9a821-137">A button path of **Sales order** &gt; **View** is also shown.</span></span> <span data-ttu-id="9a821-138">Í hlutanum **Sölupöntun** af slóðinni sem samsvarar flipanum **Sölupöntun** í Aðgerðarúðunni, og **Skoða** hluti slóðar samsvarar **Skoða** flokk á þeim flipa. Á svipaðan hátt tilkynnir slóðin fyrir hnappinn **Heildarafsláttur** (**Selja** &gt; **Reikna út**) þér að hnappurinn sé staðsettur í flokknum **Reikna út** á flipanum **Selja** í aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="9a821-138">The **Sales order** part of the path corresponds to the **Sales order** tab on the Action Pane, and the **View** part of the path corresponds to the **View** group on that tab. Similarly, the path of the **Total discount** button (**Sell** &gt; **Calculate**) informs you that this button is located in the **Calculate** group on the **Sell** tab of the Action Pane.</span></span> <span data-ttu-id="9a821-139">Þess vegna hjálpa þessar upplýsingar til við að skilja nákvæmlega hvaða hnappur verður ræstur af leitaraðgerð (ef valið er sá hnappur í lista yfir niðurstöður).</span><span class="sxs-lookup"><span data-stu-id="9a821-139">Therefore, this information helps you understand exactly which button will be triggered by action search (if you select that button in the results list).</span></span>

<span data-ttu-id="9a821-140">[![action-search-field-with-data](./media/action-search-field-with-data.png)](./media/action-search-field-with-data.png)</span><span class="sxs-lookup"><span data-stu-id="9a821-140">[![action-search-field-with-data](./media/action-search-field-with-data.png)](./media/action-search-field-with-data.png)</span></span>

<span data-ttu-id="9a821-141">Í fyrri dæmi sýna sýndi leitaraðgerð niðurstöðum úr staðlaða Aðgerðarúðu efst síðu.</span><span class="sxs-lookup"><span data-stu-id="9a821-141">In the previous example, action search showed results from the standard Action Pane at the top of a page.</span></span> <span data-ttu-id="9a821-142">Hins vegar sýnir aðgerðaleit einnig niðurstöður úr sýnilegri verkfæraslám sem eru staðsettir í öðrum hlutum á síðu.</span><span class="sxs-lookup"><span data-stu-id="9a821-142">However, action search also shows results from visible toolbars that are located in other places on the page.</span></span> <span data-ttu-id="9a821-143">Til dæmis er verið að leita að **lagerbirgðir** hnappi sem er staðsettur í **sölupantanalínum** flýtiflipa.</span><span class="sxs-lookup"><span data-stu-id="9a821-143">For example, you're searching for the **On-hand inventory** button that is located on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="9a821-144">Í þessu tilfelli tilkynnir slóð hnappsins í lista yfir niðurstöður (**sölupantanalínur** &gt; **Birgðir** &gt; **Skoða**) að þessi hnappur er staðsettur undir **Skoða** fyrirsögn á **Birgðir** valmyndarhnapp á í **sölupantanalínur** flýtiflipa.</span><span class="sxs-lookup"><span data-stu-id="9a821-144">In this case, the button path in the results list (**Sales order lines** &gt; **Inventory** &gt; **View**) informs you that this button is located under the **View** heading on the **Inventory** menu button on the **Sales order lines** FastTab.</span></span>

<span data-ttu-id="9a821-145">[![on-hand-inventory](./media/on-hand-inventory.png)](./media/on-hand-inventory.png)</span><span class="sxs-lookup"><span data-stu-id="9a821-145">[![on-hand-inventory](./media/on-hand-inventory.png)](./media/on-hand-inventory.png)</span></span>

## <a name="action-search-vs-navigation-search"></a><span data-ttu-id="9a821-146">Aðgerðaleita samanborið við flettingaleit</span><span class="sxs-lookup"><span data-stu-id="9a821-146">Action search vs. Navigation search</span></span>

<span data-ttu-id="9a821-147">Aðgerðaleit er ætlað að finna og keyra aðgerðir á síðu, en sérstakt leitarkerfi er til að finna og fletta á síður í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9a821-147">Whereas action search is intended to find and run actions on a page, there is a separate search mechanism for finding and navigating to pages in Finance and Operations.</span></span> <span data-ttu-id="9a821-148">Fyrir frekari upplýsingar um þann möguleika, að sjá greinina [Flettingaleit](navigation-search.md).</span><span class="sxs-lookup"><span data-stu-id="9a821-148">For more information about that feature, see the [Navigation search](navigation-search.md) article.</span></span>