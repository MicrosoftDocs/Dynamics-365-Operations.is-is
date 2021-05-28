---
title: Aðeins er hægt að bæta aðallyklinum við sem kreditlykli vegna afstemmingar
description: Þegar afstemmingarástæða er sett upp í flutningsstjórnun er aðeins hægt að bæta aðalreikningnum við sem inneignarreikningi.
author: Henrikan
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: TMSFBDetailReconcile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 708081370b27fd51ef9a2329d8392f4515353dcb
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026595"
---
# <a name="you-can-add-only-the-main-account-as-the-credit-account-for-reconciliation-reasons"></a><span data-ttu-id="1051f-103">Aðeins er hægt að bæta aðallyklinum við sem kreditlykli vegna afstemmingar</span><span class="sxs-lookup"><span data-stu-id="1051f-103">You can add only the main account as the credit account for reconciliation reasons</span></span>

<span data-ttu-id="1051f-104">KB númer: 4603538</span><span class="sxs-lookup"><span data-stu-id="1051f-104">KB number: 4603538</span></span>

## <a name="symptoms"></a><span data-ttu-id="1051f-105">Einkenni</span><span class="sxs-lookup"><span data-stu-id="1051f-105">Symptoms</span></span>

<span data-ttu-id="1051f-106">Þegar afstemmingarástæða er sett upp í flutningsstjórnun er aðeins hægt að bæta aðalreikningnum við sem inneignarreikningi.</span><span class="sxs-lookup"><span data-stu-id="1051f-106">When you set up a reconciliation reason in Transportation management, you can add only the main account as the credit account.</span></span> <span data-ttu-id="1051f-107">Þú getur ekki bætt við kostnaðarstað eða neinum öðrum víddum sem kreditreikninginn.</span><span class="sxs-lookup"><span data-stu-id="1051f-107">You can't add a cost center or any other dimension as the credit account.</span></span> <span data-ttu-id="1051f-108">En debetreikningurinn gerir þér kleift að velja aðrar víddir.</span><span class="sxs-lookup"><span data-stu-id="1051f-108">However, the debit account lets you select other dimensions.</span></span>

## <a name="resolution"></a><span data-ttu-id="1051f-109">Upplausn</span><span class="sxs-lookup"><span data-stu-id="1051f-109">Resolution</span></span>

<span data-ttu-id="1051f-110">Ef afstemmingin er ekki gerð til að greiða lánardrottinum heldur til að lána tilteknum aðalreikningi leyfir kerfið þér ekki að velja fjárhagsvídd lánareikningsins þegar ástæðan fyrir afstemmingunni er sett upp.</span><span class="sxs-lookup"><span data-stu-id="1051f-110">If the reconciliation isn't done to pay the vendor but to credit a specific main account, the system doesn't allow you to select a financial dimension for the credit account when you set up the reconciliation reason.</span></span>

<span data-ttu-id="1051f-111">Ef lykilskipulagið krefst tiltekins fjárhagsvíddargildis fyrir aðalreikninginn inneignar er ekki hægt að færa sjálfkrafa inn færslubók lánardrottins þar sem fjárhagsvíddargildið vantar.</span><span class="sxs-lookup"><span data-stu-id="1051f-111">If the account structure requires a specific financial dimension value for the credit main account, the resulting vendor journal can't be posted automatically, because the financial dimension value is missing.</span></span> <span data-ttu-id="1051f-112">Því verður fyrst að tilgreina kreditreikninginn handvirkt með því að nota síðuna **Reikningabók**.</span><span class="sxs-lookup"><span data-stu-id="1051f-112">Therefore, you must first manually specify the credit account by using the **Invoice journal** page.</span></span>

<span data-ttu-id="1051f-113">Ekki er hægt að bóka reikningsbók lánardrottins sjálfkrafa vegna þess að víddargildi er nauðsynlegt fyrir lánareikninginn.</span><span class="sxs-lookup"><span data-stu-id="1051f-113">Because a dimension value is required for the credit account, the vendor invoice journal can't be automatically posted.</span></span> <span data-ttu-id="1051f-114">Þú verður að bóka þetta handvirkt eftir að þú hefur bætt víddargildinu handvirkt við aðalreikning fyrir lánalínuna.</span><span class="sxs-lookup"><span data-stu-id="1051f-114">You must manually post it after you manually add the dimension value to the main account for the credit line.</span></span>
