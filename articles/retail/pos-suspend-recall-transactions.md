---
title: "Gera hlé á og halda áfram með færslu á sölustaðnum (POS)"
description: "Þetta efnisatriði útskýrir hvernig notendur geta gert hlé á færslum í vinnslu og síðan haldið áfram með þær seinna eða á öðrum afgreiðslukassa með því að nota Microsoft Dynamics 365 for Retail."
author: jblucher
manager: AnnBe
ms.date: 11/27/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 261234
ms.assetid: 7cd68ecc-cc09-48ab-8cb8-48d5c304effa
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: ffb04609318c7de4b9ef729a8e03a7f9395806b8
ms.contentlocale: is-is
ms.lasthandoff: 01/04/2019

---

# <a name="suspend-and-resume-transactions-in-the-point-of-sale-pos"></a><span data-ttu-id="15cc0-103">Gera hlé á og halda áfram með færslur á sölustaðnum (POS)</span><span class="sxs-lookup"><span data-stu-id="15cc0-103">Suspend and resume transactions in the point of sale (POS)</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="15cc0-104">Notendur sölustaðar (POS) geta gert hlé á færslum í vinnslu og síðan haldið áfram með þær seinna eða á öðrum afgreiðslukassa.</span><span class="sxs-lookup"><span data-stu-id="15cc0-104">Point of sale (POS) users can suspend in-progress transactions, and then resume them later or on a different register.</span></span> <span data-ttu-id="15cc0-105">Oft er gert hlé á færslum til að losa afgreiðslukassa á fljótlegan hátt fyrir annað verk án þess að glata núverandi færslu.</span><span class="sxs-lookup"><span data-stu-id="15cc0-105">Transactions are often suspended to quickly free up a register for a different task without losing any progress on the current transaction.</span></span> <span data-ttu-id="15cc0-106">Til dæmis byrjar aðili tengdur verslun að vinna með færslu viðskiptavinar á fartæki en verður að klára færsluna á afgreiðslukassa sem er með peningaskúffu.</span><span class="sxs-lookup"><span data-stu-id="15cc0-106">For example, a store associate starts to process a customer's transaction on a mobile device but must complete it on a register that has a cash drawer.</span></span> <span data-ttu-id="15cc0-107">Í þessu tilfelli getur aðili tengdur verslun gert hlé á færslunni á fartækinu og síðan kallað hana aftur fram og haldið áfram með hana á afgreiðslukassa.</span><span class="sxs-lookup"><span data-stu-id="15cc0-107">In this case, the store associate can suspend the transaction on the mobile device, and then recall and resume it on a register.</span></span>

## <a name="configure-suspend-and-resume-functionality"></a><span data-ttu-id="15cc0-108">Skilgreina virkni frestunar og áframhalds</span><span class="sxs-lookup"><span data-stu-id="15cc0-108">Configure suspend and resume functionality</span></span>

### <a name="pos-operations"></a><span data-ttu-id="15cc0-109">POS-aðgerðir</span><span class="sxs-lookup"><span data-stu-id="15cc0-109">POS operations</span></span>

<span data-ttu-id="15cc0-110">Tvær [POS-aðgerðir](pos-operations.md) leyfa sölustað að styðja við atburðarásir frestunar og áframhalds.</span><span class="sxs-lookup"><span data-stu-id="15cc0-110">Two [POS operations](pos-operations.md) let the POS support suspend and resume scenarios.</span></span> <span data-ttu-id="15cc0-111">Þú getur úthlutað þessum aðgerðum til [hnappahnita](pos-screen-layouts.md) á færslusíðunni eða upphafssíðunni.</span><span class="sxs-lookup"><span data-stu-id="15cc0-111">You can assign these operations to [button grids](pos-screen-layouts.md) on the transaction page or the welcome page.</span></span>

- <span data-ttu-id="15cc0-112">503: Fresta færslu</span><span class="sxs-lookup"><span data-stu-id="15cc0-112">503: Suspend transaction</span></span>
- <span data-ttu-id="15cc0-113">504: Endurheimta færslu</span><span class="sxs-lookup"><span data-stu-id="15cc0-113">504: Recall transaction</span></span>

### <a name="receipt-template"></a><span data-ttu-id="15cc0-114">Sniðmát kvittunar</span><span class="sxs-lookup"><span data-stu-id="15cc0-114">Receipt template</span></span>

<span data-ttu-id="15cc0-115">Hægt er að grunnstilla sölustaðinn til að búa til prentaðan strimil þegar færslu er frestað.</span><span class="sxs-lookup"><span data-stu-id="15cc0-115">The POS can be configured to generate a printed slip when a transaction is suspended.</span></span> <span data-ttu-id="15cc0-116">Þennan strimil er hægt að nota til að bera strax kennsl á og endurheimta færslu seinna meir.</span><span class="sxs-lookup"><span data-stu-id="15cc0-116">That slip can then be used to quickly identify and recall the transaction later.</span></span>

<span data-ttu-id="15cc0-117">Til að gera sölustað kleift að prenta strimil verður þú að bæta kvittunarsniðinu **Frestuð færsla** við forstillingu kvittunar fyrir verslun.</span><span class="sxs-lookup"><span data-stu-id="15cc0-117">To enable the POS to print a slip, you must add the **Suspended transaction** receipt format to the store's receipt profile.</span></span> <span data-ttu-id="15cc0-118">Þú getur hannað kvittunarsniðið þannig að það innihaldi eða útiloki tilteknar upplýsingar um færsluna.</span><span class="sxs-lookup"><span data-stu-id="15cc0-118">You can design the receipt format so that it includes or excludes specific details about the transaction.</span></span> <span data-ttu-id="15cc0-119">Til dæmis getur sniðið innihaldið strikamerki til að bjóða upp á skönnun.</span><span class="sxs-lookup"><span data-stu-id="15cc0-119">For example, the format can include a barcode to support scanning.</span></span>

### <a name="receipt-numbering"></a><span data-ttu-id="15cc0-120">Númer kvittunar</span><span class="sxs-lookup"><span data-stu-id="15cc0-120">Receipt numbering</span></span>

<span data-ttu-id="15cc0-121">Hvað varðar aðrar POS-færslugerðir sem búa til prentaða kvittun, getur þú skilgreint númeraröð fyrir frestaðar færslur í hlutanum **Númerun kvittana** í virknireglu verslunar.</span><span class="sxs-lookup"><span data-stu-id="15cc0-121">As for other POS transaction types that generate a printed receipt, you can define a number sequence for suspended transactions in the **Receipt numbering** section of the store's functionality profile.</span></span>

### <a name="void-when-closing-shift"></a><span data-ttu-id="15cc0-122">Ógild við lok vaktar</span><span class="sxs-lookup"><span data-stu-id="15cc0-122">Void when closing shift</span></span>

<span data-ttu-id="15cc0-123">Þú getur notað valkostinn **Ógilda við lok vaktar** svo notendur verði að ljúka við eða ógilda allar frestaðar færslur áður en þeir loka vaktinni.</span><span class="sxs-lookup"><span data-stu-id="15cc0-123">You can use the **Void when closing shift** option to require that users either complete or void any suspended transactions before they close their shift.</span></span> <span data-ttu-id="15cc0-124">Á meðan aðgerðin **Loka vakt** stendur yfir mun sölustaðurinn biðja notendur um að annaðhvort skoða eða ógilda allar útistandandi frestaðar færslur.</span><span class="sxs-lookup"><span data-stu-id="15cc0-124">During the **Close shift** operation, the POS will prompt users to either view or void any outstanding suspended transactions.</span></span>

## <a name="suspend-and-resume-a-transaction"></a><span data-ttu-id="15cc0-125">Fresta og endurheimta færslu</span><span class="sxs-lookup"><span data-stu-id="15cc0-125">Suspend and resume a transaction</span></span>

### <a name="suspend-a-transaction"></a><span data-ttu-id="15cc0-126">Fresta færslu</span><span class="sxs-lookup"><span data-stu-id="15cc0-126">Suspend a transaction</span></span>

<span data-ttu-id="15cc0-127">Notendur sem hafa nægar heimildir og sem eru með skjáútlit sem felur í sér aðgerðina **Fresta færslu** geta frestað færslu þannig að hægt sé að endurheimta hana seinna eða ná í hana á öðrum afgreiðslukassa.</span><span class="sxs-lookup"><span data-stu-id="15cc0-127">Users who have sufficient privileges, and who have a screen layout that includes the **Suspend transaction** operation, can suspend a transaction so that it can be recalled later or on a different register.</span></span>

<span data-ttu-id="15cc0-128">Aðeins er hægt að fresta færslum ef þær innihalda **ekki** eftirfarandi gerðir af línum:</span><span class="sxs-lookup"><span data-stu-id="15cc0-128">Transactions can be suspended only if they do **not** contain the following types of lines:</span></span>

- <span data-ttu-id="15cc0-129">Virkar greiðslulínur</span><span class="sxs-lookup"><span data-stu-id="15cc0-129">Active payment lines</span></span>
- <span data-ttu-id="15cc0-130">Línur gjafakorts (annaðhvort til að gefa út gjafakort eða bæta á stöðu gjafakorts)</span><span class="sxs-lookup"><span data-stu-id="15cc0-130">Gift card lines (either to issue a gift card or to add to the gift card balance)</span></span>

<span data-ttu-id="15cc0-131">Frestuð færsla hefur ekki áhrif á söluupplýsingar eða upplýsingar um birgðaframboð fyrir verslunina.</span><span class="sxs-lookup"><span data-stu-id="15cc0-131">A suspended transaction doesn't affect sales information or inventory availability information for the store.</span></span>

### <a name="resume-a-suspended-transaction"></a><span data-ttu-id="15cc0-132">Halda áfram með frestaða færsla</span><span class="sxs-lookup"><span data-stu-id="15cc0-132">Resume a suspended transaction</span></span>

<span data-ttu-id="15cc0-133">Hvaða notandi sem er með nægar heimildir getur endurheimt og haldið áfram með frestaðar færslur í sömu verslun, og sem er einnig með útlit sem inniheldur aðgerðina **Endurheimta færslu**.</span><span class="sxs-lookup"><span data-stu-id="15cc0-133">Suspended transactions can be recalled and resumed in the same store by any user who has sufficient privileges, and who also has a layout that includes the **Recall transaction** operation.</span></span>

<span data-ttu-id="15cc0-134">Til að auðveldlega endurheimta frestaða færslu skal skanna strikamerkið á prentaða strimlinum þegar listi yfir færslur er skoðaður úr aðgerðinni **Endurheimta færslu**.</span><span class="sxs-lookup"><span data-stu-id="15cc0-134">To quickly and easily recall a suspended transaction, scan the barcode on the printed slip while you're viewing the list of transactions from the **Recall transaction** operation.</span></span>

### <a name="considerations-for-offline-mode"></a><span data-ttu-id="15cc0-135">Hvað skal hafa í huga ef utan nets</span><span class="sxs-lookup"><span data-stu-id="15cc0-135">Considerations for offline mode</span></span>

- <span data-ttu-id="15cc0-136">Öllum þeim færslum sem er frestað í sölustað með nettengingu er ekki hægt að halda áfram með utan nets vegna þess að gögnin eru ekki samstillt við ótengdan gagnagrunn.</span><span class="sxs-lookup"><span data-stu-id="15cc0-136">Any transaction that is suspended while the POS is in online mode can't be resumed in offline mode, because the data isn't synced to the offline database.</span></span>
- <span data-ttu-id="15cc0-137">Ef þú frestar færslu í sölustað utan nets er hægt að ná í hana aftur án nettengingar, svo lengi sem sölustaðurinn hafi ekki verið færður aftur í nettengdan ham einhvern tímann eftir að færslunni var frestað.</span><span class="sxs-lookup"><span data-stu-id="15cc0-137">If you suspend a transaction while the POS is in offline mode, you can recall it in offline mode, provided that the POS wasn't switched back to online mode at any time since you suspended the transaction.</span></span> <span data-ttu-id="15cc0-138">Þegar sölustaðurinn er færður aftur í nettengdan ham er gögn um frestaðar færslur flutt aftur í nettengdan gagnagrunn og þeim eytt úr ótengdum gagnagrunni.</span><span class="sxs-lookup"><span data-stu-id="15cc0-138">When the POS is switched back to online mode, data about suspended transactions is moved to the online database and removed from the offline database.</span></span> <span data-ttu-id="15cc0-139">Þar af leiðandi er aðeins hægt að halda áfram með færslur í nettengdum ham.</span><span class="sxs-lookup"><span data-stu-id="15cc0-139">Therefore, the transactions can be resumed only in online mode.</span></span> <span data-ttu-id="15cc0-140">Ef sölustaðurinn er færður aftur í ótengdan ham verður ekki hægt að halda áfram með þessar frestuðu færslur vegna þess að þær hafa þegar verið fjarlægðar úr ótengda gagnagrunninum.</span><span class="sxs-lookup"><span data-stu-id="15cc0-140">If you switch the POS back to offline mode, you won't be able to resume those suspended transaction, because they have already been removed from the offline database.</span></span>

### <a name="void-a-suspended-transaction"></a><span data-ttu-id="15cc0-141">Ógilda frestaða færslu</span><span class="sxs-lookup"><span data-stu-id="15cc0-141">Void a suspended transaction</span></span>

<span data-ttu-id="15cc0-142">Hægt er að ógilda frestaðar færslur annaðhvort með því að endurheimta færsluna og framkvæma síðan aðgerðina **Ógilda færslu** eða með því að velja færsluna í listanum **Endurheimta færslu** og velja **Ógilda** á forritastikunni.</span><span class="sxs-lookup"><span data-stu-id="15cc0-142">You can void suspended transactions either by recalling the transaction and then performing the **Void transaction** operation, or by selecting the transaction in the **Recall transaction** list and selecting **Void** on the app bar.</span></span> <span data-ttu-id="15cc0-143">Að öðrum kosti er hægt að stilla verslunina til að biðja notendur um ógilda frestaðar færslur þegar þeir loka vaktinni.</span><span class="sxs-lookup"><span data-stu-id="15cc0-143">Alternatively, the store can be configured to prompt users to void suspended transactions when they close their shift.</span></span>

