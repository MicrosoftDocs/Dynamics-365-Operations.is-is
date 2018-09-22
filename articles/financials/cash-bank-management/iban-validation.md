---
title: "Stjórna villuleit á reikningi með alþjóðlegt bankareikningsnúmer (IBAN)"
description: "Þetta efnisatriði útskýrir hvernig á að stjórna villuleit á reikningi með alþjóðlegt bankareikningsnúmer (IBAN)."
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.translationtype: HT
ms.sourcegitcommit: 98ed3378ab05c0c69c9e5b2a82310113a81c2264
ms.openlocfilehash: e091aab70a98e0f4b96c41c1ee48926947539105
ms.contentlocale: is-is
ms.lasthandoff: 08/31/2018

---

# <a name="manage-international-bank-account-number-iban-account-validation"></a><span data-ttu-id="08908-103">Stjórna villuleit á reikningi með alþjóðlegt bankareikningsnúmer (IBAN)</span><span class="sxs-lookup"><span data-stu-id="08908-103">Manage International Bank Account Number (IBAN) account validation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="08908-104">Villuleit á reikningi með alþjóðlegt bankareikningsnúmer (IBAN) eykur fjölda villuleita sem gerðar eru þegar þú bætir IBAN við bankareikning.</span><span class="sxs-lookup"><span data-stu-id="08908-104">International Bank Account Number (IBAN) account validation increases the amount of validation that is done when you add an IBAN to a bank account.</span></span>

<span data-ttu-id="08908-105">Skipulag IBAN er geymt í Microsoft Dynamics 365 for Finance and Operation og er sjálfkrafa hlaðið upp þegar þú notar IBAN í fyrsta skipti fyrir bankareikning.</span><span class="sxs-lookup"><span data-stu-id="08908-105">The structure of the IBAN is stored in Microsoft Dynamics 365 for Finance and Operation, and is automatically loaded when you first use the IBAN on bank accounts.</span></span> <span data-ttu-id="08908-106">Bankareikningsnúmerið er hluti af skipulagi sem er skilgreint fyrir IBAN númer.</span><span class="sxs-lookup"><span data-stu-id="08908-106">The bank account number is part of the structure defined for an IBAN number.</span></span> <span data-ttu-id="08908-107">Byggt á því skipulagi, ef staða og lengd reikningsnúmersins í IBAN passar ekki við stöðuna sem er skilgreind í skipulaginu fyrir hvert land eða hvert svæði, færðu viðvörunarboð.</span><span class="sxs-lookup"><span data-stu-id="08908-107">Based on that structure, if the position and length of the account number in the IBAN don't match the position that is defined in the structure for each country or region, you will receive warning messages.</span></span>

## <a name="set-up-iban-structures"></a><span data-ttu-id="08908-108">Setja upp IBAN-skipulag</span><span class="sxs-lookup"><span data-stu-id="08908-108">Set up IBAN structures</span></span>

1. <span data-ttu-id="08908-109">Farðu í **Reiðufjár- og bankastjórnun \> Uppsetning \> IBAN-skipulag**.</span><span class="sxs-lookup"><span data-stu-id="08908-109">Go to **Cash and bank management \> Setup \> IBAN structures**.</span></span>
2. <span data-ttu-id="08908-110">Takið eftir að IBAN-skipulagið fyrir hvert land eða hvert svæði hefur verið sett upp sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="08908-110">Notice that the IBAN structures for each country or region have been set up automatically.</span></span>
3. <span data-ttu-id="08908-111">Ef þú verður að sérstilla skipulagið fyrir tiltekið land eða svæði, getur þú breytt því.</span><span class="sxs-lookup"><span data-stu-id="08908-111">If you must customize the structures for a specific country or region, you can edit them.</span></span>
4. <span data-ttu-id="08908-112">Skilgreiningar skipulags verða hluti af öllum nýjum útgáfum.</span><span class="sxs-lookup"><span data-stu-id="08908-112">The structure definitions will be a part of each new release.</span></span> <span data-ttu-id="08908-113">Þú getur notað valmyndina **Endurstilla skipulag** til að hlaða niður nýjustu skilgreiningunum eftir hverja uppfærslu.</span><span class="sxs-lookup"><span data-stu-id="08908-113">You can use the **Reset structures** menu to load the latest definitions after each update.</span></span>

## <a name="validate-the-iban-structure-in-a-bank-account"></a><span data-ttu-id="08908-114">Villuleita IBAN-skipulag á bankareikningi</span><span class="sxs-lookup"><span data-stu-id="08908-114">Validate the IBAN structure in a bank account</span></span>

1. <span data-ttu-id="08908-115">Farið í **Reiðufjár- og bankastjórnun \> Bankareikningar \> Bankareikningar**.</span><span class="sxs-lookup"><span data-stu-id="08908-115">Go to **Cash and bank management \> Bank accounts \> Bank accounts**.</span></span>
2. <span data-ttu-id="08908-116">Stofna bankareikning.</span><span class="sxs-lookup"><span data-stu-id="08908-116">Create a bank account.</span></span>
3. <span data-ttu-id="08908-117">Í flýtiflipanum **Viðbótarupplýsingar** skal slá inn IBAN-númeri.</span><span class="sxs-lookup"><span data-stu-id="08908-117">On the **Additional information** FastTab, enter an IBAN.</span></span>

    <span data-ttu-id="08908-118">Ef staða og lengd reikningsnúmersins í IBAN passar ekki við stöðuna sem er skilgreind í skipulaginu fyrir hvert land eða hvert svæði, færðu viðvörunarboð.</span><span class="sxs-lookup"><span data-stu-id="08908-118">If the position and length of the account number in the IBAN don't match the position that is defined in the structure for each country or region, you receive a message.</span></span> <span data-ttu-id="08908-119">Þú getur ekki haldið áfram ef lengd IBAN-númers passar ekki við lengdina í IBAN-skipulaginu.</span><span class="sxs-lookup"><span data-stu-id="08908-119">You can't continue if the length of the IBAN doesn't match the length in the IBAN structure.</span></span>

    <span data-ttu-id="08908-120">Villuleitin staðfestir einnig að bankareikningsnúmerið samsvarar þeim hluta IBAN-númersins sem táknar bankareikningsnúmerið.</span><span class="sxs-lookup"><span data-stu-id="08908-120">The validation also verifies that the bank account number matches the part of the IBAN that represents the bank account number.</span></span> <span data-ttu-id="08908-121">Ef bankareikningsnúmerið passar ekki, færðu viðvörunarboð.</span><span class="sxs-lookup"><span data-stu-id="08908-121">If the bank account number doesn't match, you receive a warning message.</span></span> <span data-ttu-id="08908-122">Þessi skilaboð eru aðeins viðvörun.</span><span class="sxs-lookup"><span data-stu-id="08908-122">This message is only a warning.</span></span> <span data-ttu-id="08908-123">Þú getur haldið áfram, jafnvel þótt bankareikningsnúmerið passi ekki.</span><span class="sxs-lookup"><span data-stu-id="08908-123">You can continue even if the bank account number doesn't match.</span></span>

