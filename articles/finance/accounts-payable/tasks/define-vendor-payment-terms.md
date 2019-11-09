---
title: Skilgreina greiðsluskilmála lánardrottna
description: Í þessu efnisatriði er útskýrt hvernig á að setja upp greiðsluskilmála fyrir lánardrottnareikninga.
author: abruer
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PaymTerm, CashDisc
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6432d04aa821e76d67e2c430e514f4b9056d8228
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178346"
---
# <a name="define-vendor-payment-terms"></a><span data-ttu-id="c0c57-103">Skilgreina greiðsluskilmála lánardrottna</span><span class="sxs-lookup"><span data-stu-id="c0c57-103">Define vendor payment terms</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c0c57-104">Í þessu efnisatriði er útskýrt hvernig á að setja upp greiðsluskilmála fyrir lánardrottnareikninga.</span><span class="sxs-lookup"><span data-stu-id="c0c57-104">This topic explains how to set up payment terms for vendor invoices.</span></span> <span data-ttu-id="c0c57-105">Þetta verkefni notar USMF-sýnifyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="c0c57-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="c0c57-106">Farðu í **Skoðunarrúðu > Kerfiseiningar > Viðskiptaskuldir > Greiðsluuppsetning > Greiðsluskilmálar**.</span><span class="sxs-lookup"><span data-stu-id="c0c57-106">Go to **Navigation pane > Modules > Accounts payable > Payment setup > Terms of payment**.</span></span>
2. <span data-ttu-id="c0c57-107">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="c0c57-107">Select **New**.</span></span> <span data-ttu-id="c0c57-108">Skilmála greiðslu síða er notuð til að skilgreina hvernig verður að reikna út gjalddaga.</span><span class="sxs-lookup"><span data-stu-id="c0c57-108">The Terms of payment page is used to define how the due date will be calculated.</span></span> <span data-ttu-id="c0c57-109">Það er ekki notuð til að skilgreina hvernig dagsetning staðgreiðsluafsláttar reiknaðar.</span><span class="sxs-lookup"><span data-stu-id="c0c57-109">It is not used to define how the cash discount date will be calculated.</span></span>  
3. <span data-ttu-id="c0c57-110">Færðu inn gildi í reitnum **greiðsluskilmálar**.</span><span class="sxs-lookup"><span data-stu-id="c0c57-110">In the **Terms of payment** field, type a value.</span></span>
4. <span data-ttu-id="c0c57-111">Í reitinn **Lýsing** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="c0c57-111">In the **Description field**, type a value.</span></span>
5. <span data-ttu-id="c0c57-112">Í reitinn **Dagar** skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="c0c57-112">In the **Days** field, enter a number.</span></span> <span data-ttu-id="c0c57-113">Númerið sem fært er inn hér verður notað til að bæta við gjalddaga eða við lok tímabils sem skilgreind er í greiðsluaðferðina.</span><span class="sxs-lookup"><span data-stu-id="c0c57-113">The number entered here will be used to add to the due date, or to the end of the period identified in the Payment method.</span></span> <span data-ttu-id="c0c57-114">Til dæmis, ef **Nettó** er valið, verður tölunni bætt við gjalddaga.</span><span class="sxs-lookup"><span data-stu-id="c0c57-114">For example, if you select **Net**, the number will be added to the due date.</span></span> <span data-ttu-id="c0c57-115">Ef valið er **Gildandi mánuður**, bætir það tölunni við síðasta dag núverandi mánaðar til að reikna út gjalddaga.</span><span class="sxs-lookup"><span data-stu-id="c0c57-115">If you select **Current month**, it will add the number to the last day of the current month to calculate the due date.</span></span>  
6. <span data-ttu-id="c0c57-116">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="c0c57-116">Select **Save**.</span></span>
7. <span data-ttu-id="c0c57-117">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="c0c57-117">Close the page.</span></span>
8. <span data-ttu-id="c0c57-118">Farðu í **Viðskiptaskuldir > Greiðsluuppsetning > Staðgreiðsluafsláttur**.</span><span class="sxs-lookup"><span data-stu-id="c0c57-118">Go to **Accounts payable > Payment setup > Cash discounts**.</span></span>
9. <span data-ttu-id="c0c57-119">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="c0c57-119">Select **New**.</span></span>
10. <span data-ttu-id="c0c57-120">Færið inn kenni í reitnum **Staðgreiðsluafsláttur**.</span><span class="sxs-lookup"><span data-stu-id="c0c57-120">In the **Cash discount** field, enter an ID.</span></span>
11. <span data-ttu-id="c0c57-121">Í reitinn **Lýsing** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="c0c57-121">In the **Description** field, type a value.</span></span>
12. <span data-ttu-id="c0c57-122">Ef lánardrottinn býður upp á lagskipt afslátt, velja næsta staðgreiðsluafsláttinn eftir að sá gildandi er útrunnið.</span><span class="sxs-lookup"><span data-stu-id="c0c57-122">If the vendor offers a tiered discount, select the next cash discount after the current one is expired.</span></span>
13. <span data-ttu-id="c0c57-123">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="c0c57-123">Close the page.</span></span>
14. <span data-ttu-id="c0c57-124">Í reitinn **Dagar** skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="c0c57-124">In the **Days** field, enter a number.</span></span> <span data-ttu-id="c0c57-125">Magnið sem er fært inn í reitinn **Dagar** verður notað til að reikna út dagsetningu staðgreiðsluafsláttar, á grundvelli hvaða valkostur var valinn í reitnum **Nettó/Gildandi**.</span><span class="sxs-lookup"><span data-stu-id="c0c57-125">The quantity entered in the **Days** field will be used to calculate the Cash discount date, based on what option was selected in the **Net/Current** field.</span></span> <span data-ttu-id="c0c57-126">Ef **Nettó** var valinn er magni bætt við dagsetningu reiknings til að ákvarða dagsetningu staðgreiðsluafsláttar.</span><span class="sxs-lookup"><span data-stu-id="c0c57-126">If **Net** was selected, the quantity will be added to the invoice date to determine the cash discount date.</span></span> <span data-ttu-id="c0c57-127">Ef **Núverandi mánuður** var valinn er magn verður bætt við lok gjaldmiðilsmánaðar til að ákvarða dagsetningu staðgreiðsluafsláttar.</span><span class="sxs-lookup"><span data-stu-id="c0c57-127">If **Current month** was selected, the quantity will be added to the end of the currency month to determine the cash discount date.</span></span>  
15. <span data-ttu-id="c0c57-128">Færið inn hlutfall staðgreiðsluafslátt í reitnum **Afsláttur**.</span><span class="sxs-lookup"><span data-stu-id="c0c57-128">Enter the percentage of the cash discount in the **Discount** field.</span></span> 
16. <span data-ttu-id="c0c57-129">Sláðu inn aðalreikninginn sem staðgreiðsluafslátturinn verður bókaður fyrir reikninga viðskiptavina og sláðu síðan inn aðalreikninginn sem staðgreiðsluafslátturinn verður bókaður fyrir reikninga lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="c0c57-129">Enter the main account to which the cash discount will be posted for customer invoices, then enter the main account to which the cash discount will be posted for vendor invoices.</span></span> <span data-ttu-id="c0c57-130">Ef **Afsláttarmótlyklar** er stillt til að **Nota aðallykill fyrir afslátt lánardrottins**, þá verður aðallykill notaður.</span><span class="sxs-lookup"><span data-stu-id="c0c57-130">If **Discount offset accounts** is set to **Use main account for vendor discount**, then the Main account will be used.</span></span> <span data-ttu-id="c0c57-131">Ef valkosturinn er stillt á **Lyklana á reikningslínum**, verður staðgreiðsluafslátturinn bókaður á eignar/kostnaðarlykla í línum á reikningi.</span><span class="sxs-lookup"><span data-stu-id="c0c57-131">If the option is set to **Accounts on the invoice lines**, the cash discount will be posted to the asset/expense accounts on the invoice's lines.</span></span>  
17. <span data-ttu-id="c0c57-132">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="c0c57-132">Select **Save**.</span></span>
