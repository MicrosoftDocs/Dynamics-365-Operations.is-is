---
title: Vinna úr leiðréttingum á vildarkerfispunktum
description: Þetta ferli sýnir hvernig til að fletta upp upplýsingar um vildarkort og leiðrétta vildarpunkta.
author: scott-tucker
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailLoyaltyCards, RetailLoyaltyCardRewardPointTrans, RetailLoyaltyCardRewardPointAdjustment, RetailAffiliationLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bdbd9fa60fe4d000359e4695a9fb034fae3ca1b0
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140731"
---
# <a name="process-loyalty-reward-point-adjustments"></a><span data-ttu-id="1ec06-103">Vinna úr leiðréttingum á vildarkerfispunktum</span><span class="sxs-lookup"><span data-stu-id="1ec06-103">Process loyalty reward point adjustments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1ec06-104">Þetta ferli sýnir hvernig til að fletta upp upplýsingar um vildarkort og leiðrétta vildarpunkta.</span><span class="sxs-lookup"><span data-stu-id="1ec06-104">This procedure demonstrates how to look up loyalty card information and adjust loyalty reward points.</span></span> <span data-ttu-id="1ec06-105">Sýnigögn fyrirtækisins til að stofna verkið er USRT.</span><span class="sxs-lookup"><span data-stu-id="1ec06-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="1ec06-106">Þetta verk er ætluð fyrir hlutverk stjórnanda Commerce aðgerðir eða hlutverk stjórnanda þjónustudeildar.</span><span class="sxs-lookup"><span data-stu-id="1ec06-106">This task is intended for the Commerce operations manager role or a Customer service manager role.</span></span>

1. <span data-ttu-id="1ec06-107">Fara í vildarkort</span><span class="sxs-lookup"><span data-stu-id="1ec06-107">Go to Loyalty cards.</span></span>
2. <span data-ttu-id="1ec06-108">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="1ec06-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="1ec06-109">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="1ec06-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="1ec06-110">Smellt er á kortafærslur</span><span class="sxs-lookup"><span data-stu-id="1ec06-110">Click Card transactions.</span></span>
    * <span data-ttu-id="1ec06-111">Á þessari síðu er hægt að skoða vildarkortafærsla valda vildarkort.</span><span class="sxs-lookup"><span data-stu-id="1ec06-111">On this page you can view all loyalty transactions for the selected loyalty card.</span></span>  
5. <span data-ttu-id="1ec06-112">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="1ec06-112">Close the page.</span></span>
6. <span data-ttu-id="1ec06-113">Smellt er á Kortaleiðréttingar</span><span class="sxs-lookup"><span data-stu-id="1ec06-113">Click Card adjustments.</span></span>
7. <span data-ttu-id="1ec06-114">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="1ec06-114">Click New.</span></span>
8. <span data-ttu-id="1ec06-115">Færa inn eða veljið gildi í svæðið umbun vildarkorts.</span><span class="sxs-lookup"><span data-stu-id="1ec06-115">In the Reward point field, enter or select a value.</span></span>
9. <span data-ttu-id="1ec06-116">Færið inn tölu í reitnum Upphæð eða magn.</span><span class="sxs-lookup"><span data-stu-id="1ec06-116">In the Amount or quantity field, enter a number.</span></span>
    * <span data-ttu-id="1ec06-117">Hægt er að bæta við eða fjarlægja punkta á vildarkorti með því að nota jákvæð eða neikvæð upphæð.</span><span class="sxs-lookup"><span data-stu-id="1ec06-117">You can add or remove points from the loyalty card by using positive or negative amounts.</span></span>  
10. <span data-ttu-id="1ec06-118">Færa inn eða veljið gildi í svæðinu vildarkerfi.</span><span class="sxs-lookup"><span data-stu-id="1ec06-118">In the Loyalty program field, enter or select a value.</span></span>
11. <span data-ttu-id="1ec06-119">Í reitinn Athugasemd skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="1ec06-119">In the Comment field, type a value.</span></span>
12. <span data-ttu-id="1ec06-120">Smellt er á Bóka leiðréttingu.</span><span class="sxs-lookup"><span data-stu-id="1ec06-120">Click Post adjustment.</span></span>
13. <span data-ttu-id="1ec06-121">Smella á Já.</span><span class="sxs-lookup"><span data-stu-id="1ec06-121">Click Yes.</span></span>
14. <span data-ttu-id="1ec06-122">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="1ec06-122">Close the page.</span></span>
    * <span data-ttu-id="1ec06-123">Vanalega á þessum tímapunkti er á endurnýja síðu til að sjá niðurstöður vildarpunkts leiðréttingu punkta í flipanum yfirlit Vildarpunkts. En ef verið er að keyra þetta sem leiðarvísi fyrir verk, ekki endurnýja núna því sé það gert, stöðvast leiðarvísi fyrir verk.</span><span class="sxs-lookup"><span data-stu-id="1ec06-123">Normally at this point you'd refresh the page to see the result of the reward points adjustment in the Reward point summary tab. But if you are running this as a task guide, don't refresh now because if you do, the task guide will stop.</span></span>  
15. <span data-ttu-id="1ec06-124">Smellt er á kortafærslur</span><span class="sxs-lookup"><span data-stu-id="1ec06-124">Click Card transactions.</span></span>
16. <span data-ttu-id="1ec06-125">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="1ec06-125">Close the page.</span></span>

