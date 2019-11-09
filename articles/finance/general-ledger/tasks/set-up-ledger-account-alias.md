---
title: Setja upp auknefni fjárhagslykla
description: Þetta ferli sýnir hvernig á að stofna auknefni fjárhagslykils sem veitir flýtivísun til að færa inn lykilnúmer.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAccountAlias
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 142ff6f968e695da9f4a93be6950529a718e160b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186050"
---
# <a name="set-up-a-ledger-account-alias"></a><span data-ttu-id="d9371-103">Setja upp auknefni fjárhagslykla</span><span class="sxs-lookup"><span data-stu-id="d9371-103">Set up a ledger account alias</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d9371-104">Þetta ferli sýnir hvernig á að stofna auknefni fjárhagslykils sem veitir flýtivísun til að færa inn lykilnúmer.</span><span class="sxs-lookup"><span data-stu-id="d9371-104">This procedure shows how to create an account alias that provides a shortcut for entering an account number.</span></span> <span data-ttu-id="d9371-105">Þetta ferli notar sýnifyrirtækið USMF.</span><span class="sxs-lookup"><span data-stu-id="d9371-105">This procedure users demo data company USMF.</span></span>

1. <span data-ttu-id="d9371-106">Fara í Fjárhagur > Bókhaldslyklar > Lyklar > Auknefni fjárhagslykils.</span><span class="sxs-lookup"><span data-stu-id="d9371-106">Go to General ledger > Chart of accounts > Accounts > Ledger account alias.</span></span>
2. <span data-ttu-id="d9371-107">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="d9371-107">Click New.</span></span>
3. <span data-ttu-id="d9371-108">Í reitnum Auknefni fjárhagslykils skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="d9371-108">In the Ledger account alias field, type a value.</span></span>
4. <span data-ttu-id="d9371-109">Í reitnum Lykilskipulagi skal velja lykilskipulag sem lykillinn og víddirnar tilheyra.</span><span class="sxs-lookup"><span data-stu-id="d9371-109">In the Account structure field, select the structure the account and dimensions belong to.</span></span>
5. <span data-ttu-id="d9371-110">Í reitnum Fyrirtæki skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="d9371-110">In the Company field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="d9371-111">Í listanum skal finna og velja fyrirtækið sem auknefnið á við.</span><span class="sxs-lookup"><span data-stu-id="d9371-111">In the list, find and select the company that the alias applies to.</span></span>
7. <span data-ttu-id="d9371-112">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="d9371-112">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="d9371-113">Í reitnum Skilgreining auknefnis fjárhagslykils skal tilgreina lykla og víddir.</span><span class="sxs-lookup"><span data-stu-id="d9371-113">In the Ledger account alias definition field, specify the account and dimensions.</span></span>
    * <span data-ttu-id="d9371-114">Lykillinn og víddirnar verða fylltar út þegar flýtileiðin er notuð.</span><span class="sxs-lookup"><span data-stu-id="d9371-114">The account and dimensions will be populated when using the shortcut.</span></span>  
9. <span data-ttu-id="d9371-115">Í reitnum Upphafleg áhersla skal velja víddina sem hefur skilgreinda áherslu þegar auknefni er notað.</span><span class="sxs-lookup"><span data-stu-id="d9371-115">In the Initial focus field, select the dimension that will have focus when the alias is used.</span></span>
    * <span data-ttu-id="d9371-116">Eftir að þú slærð inn flýtileiðina og lykillinn og víddirnar eru útfylltar verður reiturinn Upphafleg áhersla þar sem bendillinn eða áherslan flyst í.</span><span class="sxs-lookup"><span data-stu-id="d9371-116">After you type the shortcut, and the account and dimensions are populated, the Initial focus field is where the cursor or focus will move to.</span></span>  
