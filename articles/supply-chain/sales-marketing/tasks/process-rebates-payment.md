--- 
title: "Vinna úr eftirágreiddum afslætti fyrir greiðslu"
description: "Þetta ferli sýnir hvernig á að umbreyta unnar og samþykktar eftirágreiddir kreditnótur."
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 791ec304b9ea7c49fbea506d73c4daffd4478739
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="process-rebates-for-payment"></a><span data-ttu-id="239af-103">Vinna úr eftirágreiddum afslætti fyrir greiðslu</span><span class="sxs-lookup"><span data-stu-id="239af-103">Process rebates for payment</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="239af-104">Þetta ferli sýnir hvernig á að umbreyta unnar og samþykktar eftirágreiddir kreditnótur.</span><span class="sxs-lookup"><span data-stu-id="239af-104">This procedure demonstrates how to convert approved and processed customer rebates to credit notes.</span></span> <span data-ttu-id="239af-105">Hægt er að nota þessari handbók USMF sýnifyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="239af-105">You can use this guide in the USMF demo company.</span></span> <span data-ttu-id="239af-106">Forsenda fyrir þessari handbók er að hafa eina eða fleiri kröfur um eftirágreiddan afslátt sem hafa stöðuna Merkja.</span><span class="sxs-lookup"><span data-stu-id="239af-106">The precondition for this guide is to have one or more rebate claims which have a status of Mark.</span></span> <span data-ttu-id="239af-107">Ef verið er að nota USMF ættirðu að keyra sem "Mynda og vinna eftirágreidds afsláttar viðskiptavinar" leiðbeiningar áður en byrjað er að þessari handbók.</span><span class="sxs-lookup"><span data-stu-id="239af-107">If you’re using USMF you should run the "Generate and process customer rebates" guide before you start this guide.</span></span>


## <a name="convert-rebate-claims-to-credit-note"></a><span data-ttu-id="239af-108">Umbreyta eftirágreiddur afsláttur í kreditnótu</span><span class="sxs-lookup"><span data-stu-id="239af-108">Convert rebate claims to credit note</span></span>
1. <span data-ttu-id="239af-109">Fara á Alla viðskiptavini.</span><span class="sxs-lookup"><span data-stu-id="239af-109">Go to All customers.</span></span>
2. <span data-ttu-id="239af-110">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="239af-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="239af-111">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="239af-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="239af-112">Í aðgerðasvæðinu er smellt á innheimta.</span><span class="sxs-lookup"><span data-stu-id="239af-112">On the Action Pane, click Collect.</span></span>
5. <span data-ttu-id="239af-113">Smellt er á Gera upp færslur.</span><span class="sxs-lookup"><span data-stu-id="239af-113">Click Settle transactions.</span></span>
6. <span data-ttu-id="239af-114">Smellið á Aðgerðir.</span><span class="sxs-lookup"><span data-stu-id="239af-114">Click Functions.</span></span>
7. <span data-ttu-id="239af-115">Smellt er á áætlun fyrir eftirágreiddan afslátt</span><span class="sxs-lookup"><span data-stu-id="239af-115">Click Rebate program.</span></span>
    * <span data-ttu-id="239af-116">síða Eftirágreidds Afsláttar birtir kröfur um eftirágreiddan afslátt þú vannst í vinnusvæði eftirágreidds afsláttar viðskiptavinar og eru með stöðuna Merkja.</span><span class="sxs-lookup"><span data-stu-id="239af-116">The Rebate page lists the rebate claims that you have processed in the customer rebate workbench and that are in status Mark.</span></span>    
8. <span data-ttu-id="239af-117">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="239af-117">Click Edit.</span></span>
    * <span data-ttu-id="239af-118">Setja gátmerki í svæðinu Merkja fyrir kröfur sem á að hafa með í kreditnótu.</span><span class="sxs-lookup"><span data-stu-id="239af-118">Set checkmarks in the Mark field for the claims that you want to include into credit note.</span></span>   
9. <span data-ttu-id="239af-119">Smellið á Aðgerðir.</span><span class="sxs-lookup"><span data-stu-id="239af-119">Click Functions.</span></span>
10. <span data-ttu-id="239af-120">Smellt er á Stofna kreditnótu.</span><span class="sxs-lookup"><span data-stu-id="239af-120">Click Create credit note.</span></span>
    * <span data-ttu-id="239af-121">Skilaboð birtast sem tilkynna að færslubókin hefur verið bókuð (Þetta er í notkunarbók viðskiptakrafa eins og tilgreint er á síðunni færibreytna fyrir viðskiptakröfur).</span><span class="sxs-lookup"><span data-stu-id="239af-121">A message appears to inform you that a journal has been posted (This is the Accounts receivable consumption journal, as specified in the Accounts receivable parameters page).</span></span> <span data-ttu-id="239af-122">Þetta veldur upphæð raunverulegrar skuldar (lánsfé) flyst á stöðu viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="239af-122">This causes the real liability (credit) amount to be moved to the customer balance.</span></span> <span data-ttu-id="239af-123">Það þýðir að kreditfært hefur verið á lykil viðskiptamanns og skuldfært hefur verið á uppsöfnunarlykil eftirágreidds afsláttar.</span><span class="sxs-lookup"><span data-stu-id="239af-123">This means that the customer’s account has been credited, and the Rebate accrual account has been debited.</span></span>  
11. <span data-ttu-id="239af-124">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="239af-124">Close the page.</span></span>
12. <span data-ttu-id="239af-125">Smellið á Hætta við.</span><span class="sxs-lookup"><span data-stu-id="239af-125">Click Cancel.</span></span>
    * <span data-ttu-id="239af-126">Þetta endurnýjar síðan þannig að hægt er að finna uppfærslur.</span><span class="sxs-lookup"><span data-stu-id="239af-126">This refreshes the page so that you can see the updates.</span></span>  
13. <span data-ttu-id="239af-127">Í aðgerðasvæðinu er smellt á innheimta.</span><span class="sxs-lookup"><span data-stu-id="239af-127">On the Action Pane, click Collect.</span></span>
14. <span data-ttu-id="239af-128">Smellt er á Gera upp færslur.</span><span class="sxs-lookup"><span data-stu-id="239af-128">Click Settle transactions.</span></span>
    * <span data-ttu-id="239af-129">Athugið að færsla fyrir mínustölu, sem stendur fyrir heildarupphæð eftirágreidds afsláttar, án tilvísunar reiknings hefur verið bætt við stöðu viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="239af-129">Note that a transaction for negative amount, representing the total rebate amount, without invoice reference has been added to the customer balance.</span></span>   
15. <span data-ttu-id="239af-130">Smellið á Hætta við.</span><span class="sxs-lookup"><span data-stu-id="239af-130">Click Cancel.</span></span>


