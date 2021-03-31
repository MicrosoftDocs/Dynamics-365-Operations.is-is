---
title: Þægilegur rofi án nettengingar fyrir gjafakorta- og kreditreikningsaðgerðir
description: Þetta efni veitir yfirlit yfir úrbætur sem bjóða upp á þægilegan rofa án nettengingar fyrir tilteknar tegundir greiðslu.
author: rubendel
manager: AnnBe
ms.date: 02/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 20120-02-28
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 1ea46ae90dedcc3ad3c3b305bddeb4d98827353a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5230669"
---
# <a name="seamless-offline-switch-for-gift-card-and-credit-memo-operations"></a><span data-ttu-id="2fc15-103">Þægilegur rofi án nettengingar fyrir gjafakorta- og kreditreikningsaðgerðir</span><span class="sxs-lookup"><span data-stu-id="2fc15-103">Seamless offline switch for gift card and credit memo operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2fc15-104">Ef sölustaður (POS) tæki missir tengingu sína við rásagagnagrunninn geta flestar POS aðgerðir og færslur sem voru í gangi haldið áfram eftir að gjaldkerinn fær viðvörunarskilaboð um tap tengingarinnar.</span><span class="sxs-lookup"><span data-stu-id="2fc15-104">If a point of sale (POS) device loses its connection to the channel database, most POS operations and transactions that were in progress can proceed after the cashier receives a warning message about the loss of connectivity.</span></span> <span data-ttu-id="2fc15-105">Í sumum tilvikum hafa færslur þó þætti sem treysta á rauntímaþjónustuna og þeir þættir eru ekki studdir þegar POS er ekki tengt.</span><span class="sxs-lookup"><span data-stu-id="2fc15-105">However, in some cases, transactions have elements that rely on the real-time service, and those elements aren't supported when the POS is offline.</span></span> <span data-ttu-id="2fc15-106">Þetta efni lýsir nokkurri virkni sem hjálpar til við að draga úr áhrifum týndrar tengingar í þessum atburðarásum.</span><span class="sxs-lookup"><span data-stu-id="2fc15-106">This topic describes some functionality that helps reduce the impact of lost connectivity in these scenarios.</span></span>

## <a name="completing-gift-card-transactions-in-offline-mode"></a><span data-ttu-id="2fc15-107">Lokið við gjafakortafærslur án tengingar</span><span class="sxs-lookup"><span data-stu-id="2fc15-107">Completing gift card transactions in offline mode</span></span>

<span data-ttu-id="2fc15-108">Innri gjafakort eru háð rauntímaþjónustu þar sem nauðsynlegt er að viðhalda stöðunni fyrir gjafakortin í Microsoft Dynamics 365 Commerce höfuðstöðvum.</span><span class="sxs-lookup"><span data-stu-id="2fc15-108">Internal gift cards depend on the real-time service, because the balance for the gift cards must be centrally maintained in Microsoft Dynamics 365 Commerce Headquarters.</span></span> <span data-ttu-id="2fc15-109">Til að koma í veg fyrir svik eða önnur vandamál varðandi samstillingu er gjafakortum læst um leið og þeim er bætt við færslu.</span><span class="sxs-lookup"><span data-stu-id="2fc15-109">To help prevent fraud or other synchronization issues, gift cards are locked as soon as they are added to a transaction.</span></span> <span data-ttu-id="2fc15-110">Lásaraðgerðin tryggir að ekki er hægt að nota gjafakort á mörgum útstöðvum á sama tíma.</span><span class="sxs-lookup"><span data-stu-id="2fc15-110">The locking function ensures that a gift card can't be used on multiple terminals at the same time.</span></span> <span data-ttu-id="2fc15-111">Þegar færslunni lýkur er gjafakortið uppfært og aflæst.</span><span class="sxs-lookup"><span data-stu-id="2fc15-111">When a transaction is completed, the gift card is updated and unlocked.</span></span>

<span data-ttu-id="2fc15-112">Hins vegar, ef POS tapar tengingu eftir að gjafakorti hefur verið bætt við færslu getur gjafakortið orðið ónothæft.</span><span class="sxs-lookup"><span data-stu-id="2fc15-112">However, if the POS loses connectivity after a gift card has been added to a transaction, the gift card can become unusable.</span></span> <span data-ttu-id="2fc15-113">Til að koma í veg fyrir þetta ástand er Dynamics 365 Commerce með færibreytu sem gerir kleift að ljúka færslum sem innihalda gjafakortslínu sem má ljúka meðan POS er ótengdur.</span><span class="sxs-lookup"><span data-stu-id="2fc15-113">To help prevent this situation, Dynamics 365 Commerce has a parameter that enables transactions that include a gift card line to be completed while the POS is offline.</span></span> <span data-ttu-id="2fc15-114">Þegar kveikt er á þessari færibreytu verða gjafakortafærslur sem eru þvingaðar án nettengingar vistaðar ásamt færslum án nettengingar og þær verða samstilltar við Commerce Headquarters þegar færslur án nettengingar eru samstilltar.</span><span class="sxs-lookup"><span data-stu-id="2fc15-114">When this parameter is turned on, gift card transactions that are forced offline will be saved together with offline transactions, and they will be synced to Commerce Headquarters when the offline transactions are synced.</span></span> <span data-ttu-id="2fc15-115">Samstillingin mun einnig opna gjafakortið þannig að hægt sé að nota það í annarri afgreiðslustöð.</span><span class="sxs-lookup"><span data-stu-id="2fc15-115">The synchronization will also unlock the gift card so that it can be used at another terminal.</span></span>

<span data-ttu-id="2fc15-116">Til að virkja virknina að ljúka gjafakortafærslum þegar skipt hefur verið í stillingu án nettengingar ferðu í flipann **Bókun** á síðunni **Færibreytur Commerce**.</span><span class="sxs-lookup"><span data-stu-id="2fc15-116">To enable the functionality to conclude gift card transactions after switching to offline mode, go to the **Posting** tab on the **Commerce parameters** page.</span></span> <span data-ttu-id="2fc15-117">Á þeim flipa finnurðu flýtiflipann **Gjafakort** og stillir **Leyfa að vinna úr færslum á gjafakorti án tengingar** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="2fc15-117">On that tab, locate the **Gift card** fasttab and set **Allow concluding gift card transactions in offline mode** to **Yes**.</span></span>

![Gjafakortastilling án nettengingar](../media/gift.png)

<span data-ttu-id="2fc15-119">Færibreytur Commerce eru venjulega í skyndiminni.</span><span class="sxs-lookup"><span data-stu-id="2fc15-119">Commerce parameters are typically cached.</span></span> <span data-ttu-id="2fc15-120">Þess vegna getur þetta tekið allt að sólarhring að taka gildi eftir að stilling þessa stika er uppfærð og dreifingaráætlunin er hafin til að samstilla breytinguna við rásina.</span><span class="sxs-lookup"><span data-stu-id="2fc15-120">Therefore, after the setting of this parameter is updated, and the distribution schedule is initiated to sync the change to the channel, the change can take up to 24 hours to take effect.</span></span> <span data-ttu-id="2fc15-121">Til að virkja breytinguna strax skaltu endurstilla Microsoft Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="2fc15-121">To make the change effective immediately, reset Microsoft Internet Information Services (IIS).</span></span>

## <a name="completing-credit-memo-transactions-in-offline-mode"></a><span data-ttu-id="2fc15-122">Lokið við kreditreikningsfærslur án tengingar</span><span class="sxs-lookup"><span data-stu-id="2fc15-122">Completing credit memo transactions in offline mode</span></span>

<span data-ttu-id="2fc15-123">Eins og innri gjafakort er kreditreikningum miðlægt viðhaldið í Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="2fc15-123">Like internal gift cards, credit memos are centrally maintained in Commerce Headquarters.</span></span> <span data-ttu-id="2fc15-124">Commerce er með færibreytu sem gerir kleift að ljúka kreditreikningsfærslum meðan POS er ótengdur.</span><span class="sxs-lookup"><span data-stu-id="2fc15-124">Commerce has a parameter that enables credit memo transactions to be completed while the POS is offline.</span></span> <span data-ttu-id="2fc15-125">Þessi færibreyta virkar eins og gjafakortsbreytan sem nefnd var í fyrri hlutanum.</span><span class="sxs-lookup"><span data-stu-id="2fc15-125">This parameter works like the gift card parameter that was mentioned in the previous section.</span></span> <span data-ttu-id="2fc15-126">Þegar kveikt er á færibreytunni verða kreditreikningsfærslur sem eru þvingaðar án nettengingar samstilltar aftur við gagnagrunn rásarinnar ásamt öðrum færslum sem gerðar voru meðan POS var ekki tengdur.</span><span class="sxs-lookup"><span data-stu-id="2fc15-126">When the parameter is turned on, credit memo transactions that are forced offline will be synced back to the channel database, together with other transactions that were performed while the POS was offline.</span></span>

<span data-ttu-id="2fc15-127">Til að virkja virknina að ljúka kreditreikningsfærslum þegar skipt hefur verið í stillingu án nettengingar ferðu í flipann **Bókun** á síðunni **Færibreytur Commerce**.</span><span class="sxs-lookup"><span data-stu-id="2fc15-127">To enable the functionality to conclude credit memo transactions after switching to offline mode, go to the **Posting** tab on the **Commerce parameters** page.</span></span> <span data-ttu-id="2fc15-128">Á þeim flipa finnurðu flýtiflipann **Kreditreikningur** og stillir **Leyfa að vinna úr kreditreikningsfærslum án tengingar** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="2fc15-128">On that tab, locate the **Credit memo** fasttab and set **Allow concluding credit memo transactions in offline mode** to **Yes**.</span></span>

![Kreditreikningsstillingar án nettengingar](../media/creditmemo.png)

<span data-ttu-id="2fc15-130">Færibreytur Commerce eru venjulega í skyndiminni.</span><span class="sxs-lookup"><span data-stu-id="2fc15-130">Commerce parameters are typically cached.</span></span> <span data-ttu-id="2fc15-131">Þess vegna getur þetta tekið allt að sólarhring að taka gildi eftir að stilling þessa stika er uppfærð og dreifingaráætlunin er hafin til að samstilla breytinguna við rásina.</span><span class="sxs-lookup"><span data-stu-id="2fc15-131">Therefore, after the setting of this parameter is updated, and the distribution schedule is initiated to sync the change to the channel, the change can take up to 24 hours to take effect.</span></span> <span data-ttu-id="2fc15-132">Til að virkja breytinguna strax skaltu endurstilla IIS.</span><span class="sxs-lookup"><span data-stu-id="2fc15-132">To make the change effective immediately, reset IIS.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2fc15-133">Tengd efnisatriði</span><span class="sxs-lookup"><span data-stu-id="2fc15-133">Related topics</span></span>

- [<span data-ttu-id="2fc15-134">Virkni sölustaðar án nettengingar</span><span class="sxs-lookup"><span data-stu-id="2fc15-134">Offline point of sale (POS) functionality</span></span>](https://docs.microsoft.com/dynamics365/retail/pos-offline-functionality)
- [<span data-ttu-id="2fc15-135">Aðgerðir sölustaðar (POS) með og án nettengingar</span><span class="sxs-lookup"><span data-stu-id="2fc15-135">Online and offline point of sale (POS) operations</span></span>](https://docs.microsoft.com/dynamics365/retail/pos-operations)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]