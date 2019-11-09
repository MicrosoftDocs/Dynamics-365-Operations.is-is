---
title: Stjórna villuleit á reikningi með alþjóðlegt bankareikningsnúmer (IBAN)
description: Þetta efnisatriði útskýrir hvernig á að stjórna villuleit á reikningi með alþjóðlegt bankareikningsnúmer (IBAN).
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 2aaccd7c09d6daf8a237a433cc22ac1bfc3c1541
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551258"
---
# <a name="manage-international-bank-account-number-iban-account-validation"></a><span data-ttu-id="401aa-103">Stjórna villuleit á reikningi með alþjóðlegt bankareikningsnúmer (IBAN)</span><span class="sxs-lookup"><span data-stu-id="401aa-103">Manage International Bank Account Number (IBAN) account validation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="401aa-104">Villuleit með alþjóðlegu bankareikningsnúmeri (IBAN) eykur fjölda villuleita sem gerðar eru þegar þú bætir IBAN við bankareikning.</span><span class="sxs-lookup"><span data-stu-id="401aa-104">International Bank Account Number (IBAN) validation increases the amount of validation that is done when you add an IBAN to a bank account.</span></span>

<span data-ttu-id="401aa-105">Upplýsingar um skipulag IBAN er geymd í Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="401aa-105">Information about the structure of the IBAN is stored in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="401aa-106">Þessar upplýsingar eru sjálfkrafa hlaðnir þegar þú notar IBAN fyrst á bankareikningum.</span><span class="sxs-lookup"><span data-stu-id="401aa-106">That information is automatically loaded when you first use the IBAN on bank accounts.</span></span> <span data-ttu-id="401aa-107">Það inniheldur lengd IBAN, upphafsstöðu bankareikningsrnúmers og leiðarrnúmer og lengd bankareikningsnúmersins og leiðarrnúmersins.</span><span class="sxs-lookup"><span data-stu-id="401aa-107">It contains the length of the IBAN, the starting positions of the bank account number and the routing number, and the length of the bank account number and routing number.</span></span>

## <a name="set-up-iban-structures"></a><span data-ttu-id="401aa-108">Setja upp IBAN-skipulag</span><span class="sxs-lookup"><span data-stu-id="401aa-108">Set up IBAN structures</span></span>

1. <span data-ttu-id="401aa-109">Farðu í **Reiðufjár- og bankastjórnun \> Uppsetning \> IBAN-skipulag**.</span><span class="sxs-lookup"><span data-stu-id="401aa-109">Go to **Cash and bank management \> Setup \> IBAN structures**.</span></span>
2. <span data-ttu-id="401aa-110">Takið eftir að IBAN-skipulagið fyrir hvert land eða hvert svæði hefur verið sett upp sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="401aa-110">Notice that the IBAN structures for each country or region have been set up automatically.</span></span>
3. <span data-ttu-id="401aa-111">Ef þú vilt aðlaga skipulagið að tiltekið land eða svæði, getur þú breytt þeim.</span><span class="sxs-lookup"><span data-stu-id="401aa-111">If you want to customize the structures for a specific country or region, you can edit them.</span></span>
4. <span data-ttu-id="401aa-112">Skilgreiningar skipulags verða hluti af öllum nýjum útgáfum.</span><span class="sxs-lookup"><span data-stu-id="401aa-112">The structure definitions will be a part of each new release.</span></span> <span data-ttu-id="401aa-113">Þú getur notað valmyndina **Endurstilla skipulag** til að hlaða niður nýjustu skilgreiningunum eftir hverja uppfærslu.</span><span class="sxs-lookup"><span data-stu-id="401aa-113">You can use the **Reset structures** menu to load the latest definitions after each update.</span></span>

## <a name="validate-the-iban-structure-in-a-bank-account"></a><span data-ttu-id="401aa-114">Villuleita IBAN-skipulag á bankareikningi</span><span class="sxs-lookup"><span data-stu-id="401aa-114">Validate the IBAN structure in a bank account</span></span>

1. <span data-ttu-id="401aa-115">Farið í **Reiðufjár- og bankastjórnun \> Bankareikningar \> Bankareikningar**.</span><span class="sxs-lookup"><span data-stu-id="401aa-115">Go to **Cash and bank management \> Bank accounts \> Bank accounts**.</span></span>
2. <span data-ttu-id="401aa-116">Stofna bankareikning.</span><span class="sxs-lookup"><span data-stu-id="401aa-116">Create a bank account.</span></span>
3. <span data-ttu-id="401aa-117">Í flýtiflipanum **Viðbótarupplýsingar** skal slá inn IBAN-númeri.</span><span class="sxs-lookup"><span data-stu-id="401aa-117">On the **Additional information** FastTab, enter an IBAN.</span></span>

    <span data-ttu-id="401aa-118">Ef lengd IBAN er ekki í samræmi við lengd sem er skilgreind fyrir hvert land eða svæði, færðu viðvörunarskilaboð.</span><span class="sxs-lookup"><span data-stu-id="401aa-118">If the length of the IBAN doesn't match the length that is defined for each country or region, you will receive a warning message.</span></span> <span data-ttu-id="401aa-119">Þú getur ekki haldið áfram ef lengd IBAN passar ekki lengdina sem tilgreind er í IBAN uppbyggingu.</span><span class="sxs-lookup"><span data-stu-id="401aa-119">You can't continue if the length of the IBAN doesn't match the length specified in the IBAN structure.</span></span>

    <span data-ttu-id="401aa-120">Villuleitin staðfestir einnig að bankareikningsnúmerið samsvarar þeim hluta IBAN-númersins sem táknar bankareikningsnúmerið.</span><span class="sxs-lookup"><span data-stu-id="401aa-120">The validation also verifies that the bank account number matches the part of the IBAN that represents the bank account number.</span></span> <span data-ttu-id="401aa-121">Ef bankareikningsrnúmerið passar ekki, færðu viðvörunarskilaboð.</span><span class="sxs-lookup"><span data-stu-id="401aa-121">If the bank account number doesn't match, you will receive a warning message.</span></span> <span data-ttu-id="401aa-122">Þessi skilaboð eru aðeins viðvörun.</span><span class="sxs-lookup"><span data-stu-id="401aa-122">This message is only a warning.</span></span> <span data-ttu-id="401aa-123">Þú getur haldið áfram, jafnvel þótt bankareikningsnúmerið passi ekki.</span><span class="sxs-lookup"><span data-stu-id="401aa-123">You can continue even if the bank account number doesn't match.</span></span>

    <span data-ttu-id="401aa-124">Villuleitin staðfestir einnig að leiðarnúmer bankans samsvari þeim hluta IBAN sem táknar leiðarnúmer bankans.</span><span class="sxs-lookup"><span data-stu-id="401aa-124">The validation also verifies that the bank routing number matches the part of the IBAN that represents the bank routing number.</span></span> <span data-ttu-id="401aa-125">Leiðarnúmerið inniheldur bankanúmer og oft viðbótarútibú bankans.</span><span class="sxs-lookup"><span data-stu-id="401aa-125">The routing number includes a bank number and often an additional bank branch.</span></span> <span data-ttu-id="401aa-126">Ef leiðarnúmer bankans passar ekki, færðu viðvörunarskilaboð.</span><span class="sxs-lookup"><span data-stu-id="401aa-126">If the bank routing number doesn't match, you will receive a warning message.</span></span> <span data-ttu-id="401aa-127">Þessi skilaboð eru aðeins viðvörun.</span><span class="sxs-lookup"><span data-stu-id="401aa-127">This message is only a warning.</span></span> <span data-ttu-id="401aa-128">Þú getur haldið áfram, jafnvel þótt leiðarnúmer bankans passi ekki saman.</span><span class="sxs-lookup"><span data-stu-id="401aa-128">You can continue even if the bank routing number doesn't match.</span></span>