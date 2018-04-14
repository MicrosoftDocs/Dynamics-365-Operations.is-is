---
title: "Tilgreint verðgildi reiðufjár grunnstillt fyrir sölustað"
description: "Tilgreint verðgildi reiðufjár fyrir seðla og myntir er hægt að skilgreina í bakvinnslunni fyrir notkun gjaldkera, sölutengiliða og stjórnenda í versluninni innan sölustaðarins."
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailStoreTable, RetailStoreCashDeclarationTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16231
ms.assetid: f28a827c-3a50-4d5e-83eb-e5a768db70a1
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 4a7d80783368b6b39d48f80a3329d4053169c464
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---

# <a name="configure-cash-denominations-for-pos"></a><span data-ttu-id="03e77-103">Tilgreint verðgildi reiðufjár grunnstillt fyrir sölustað</span><span class="sxs-lookup"><span data-stu-id="03e77-103">Configure cash denominations for POS</span></span>

[!INCLUDE [banner](includes/banner.md)]

<span data-ttu-id="03e77-104">Tilgreint verðgildi reiðufjár fyrir seðla og myntir er hægt að skilgreina í bakvinnslunni fyrir notkun gjaldkera, sölutengiliða og stjórnenda í versluninni innan sölustaðarins.</span><span class="sxs-lookup"><span data-stu-id="03e77-104">Cash denominations for notes and coins can be defined in the back office to be used by cashiers, sales associates, and managers at the store from within the POS.</span></span> <span data-ttu-id="03e77-105">Tilgreint verðgildi má nota sem aðstoð við talningu reiðufjár fyrir talningu skiptimyntar í lok dags eða fyrir greiðslumáta við sölu.</span><span class="sxs-lookup"><span data-stu-id="03e77-105">These denominations can be used to aid in counting cash for end of day tender declarations or for quickly tendering a sale.</span></span>

## <a name="define-denominations"></a><span data-ttu-id="03e77-106">Skilgreina tilgreint verðgildi</span><span class="sxs-lookup"><span data-stu-id="03e77-106">Define denominations</span></span>
<span data-ttu-id="03e77-107">Tilgreint verðgildi er sett upp í hverri búð fyrir sig á **Uppsetning** > **Talning reiðufjár valmöguleiki frá eign verslunar** síðunni.</span><span class="sxs-lookup"><span data-stu-id="03e77-107">The denominations are set up per store on the **Set up** > **Cash declaration option from the store property** page.</span></span> 

![tilgreint verðgildi reiðufjár](./media/image1-denomination.png)

<span data-ttu-id="03e77-109">Að skilgreina tilgreint verðgildi:</span><span class="sxs-lookup"><span data-stu-id="03e77-109">To define a denomination:</span></span>
1. <span data-ttu-id="03e77-110">Smellt er á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="03e77-110">Click **New**.</span></span>
1. <span data-ttu-id="03e77-111">Tilgreina tegundina (mynt eða seðill).</span><span class="sxs-lookup"><span data-stu-id="03e77-111">Specify the type (coin or note).</span></span>
1. <span data-ttu-id="03e77-112">Tilgreina upphæðina (gildi).</span><span class="sxs-lookup"><span data-stu-id="03e77-112">Specify the amount (value).</span></span>

![tilgreint verðgildi reiðufjár](./media/image2-denomination.png)

## <a name="configure-the-functionality-profile"></a><span data-ttu-id="03e77-114">Grunnstilla virkniregluna</span><span class="sxs-lookup"><span data-stu-id="03e77-114">Configure the functionality profile</span></span>
<span data-ttu-id="03e77-115">Þegar borgað er með reiðufé á sölustað, getur notandinn notað tilgreint verðgildi seðils til að færa inn á fljótlegan máta upphæðina sem viðskiptavinurinn reiddi af hendi.</span><span class="sxs-lookup"><span data-stu-id="03e77-115">When paying by cash in POS, the user can use the note denominations to quickly enter the amount paid by the customer.</span></span> <span data-ttu-id="03e77-116">Í virknireglunni geturðu grunnstillt þá tvo valmöguleika sem sýna tilgreint verðgildi á sölustað.</span><span class="sxs-lookup"><span data-stu-id="03e77-116">In the functionality profile, you can configure the two options for showing the denomination in POS.</span></span>

<span data-ttu-id="03e77-117">**Hærra eða jafnt upphæð til greiðslu**: Að sjálfgefnu, sölustaður mun aðeins sýna tilgreint verðgildi seðils sem er hærra en upphæð til greiðslu, sem gerir einnar snertingar greiðslumáta mögulegan.</span><span class="sxs-lookup"><span data-stu-id="03e77-117">**Greater or equal to amount due**: By default, POS will only show the note denominations that are greater than the amount due, which allows for one-touch tendering.</span></span> <span data-ttu-id="03e77-118">Ef upphæðin til greiðslu er t.d. $7.50, myndi sölustaður sýna eftirfarandi tilgreint verðgildi: $10, $20, $50, og $100.</span><span class="sxs-lookup"><span data-stu-id="03e77-118">For example, if the amount due is $7.50, POS would show the following denominations: $10, $20, $50, and $100.</span></span> <span data-ttu-id="03e77-119">Snerting við allar þessar upphæðir mun sjálfvirkt setja upp greiðslumáta sölu fyrir þá upphæð.</span><span class="sxs-lookup"><span data-stu-id="03e77-119">Touching any of these amounts will automatically tender the sale for that amount.</span></span> <span data-ttu-id="03e77-120">$1 og $5 seðlarnir eru ekki sýndir þar sem þessar upphæðir eru minni en upphæð til greiðslu.</span><span class="sxs-lookup"><span data-stu-id="03e77-120">The $1 and $5 notes are not shown since these amounts are less than the amount due.</span></span>

<span data-ttu-id="03e77-121">**Öll tilgreind verðgildi**: Veljið þennan valkost til að sýna alltaf öll verðgildi seðils á sölustað, óháð upphæð til greiðslu.</span><span class="sxs-lookup"><span data-stu-id="03e77-121">**All denominations**: Select this option to always show all note denominations in POS, regardless of the amount due.</span></span> <span data-ttu-id="03e77-122">Þetta þýðir að notandinn getur notað samsetning seðla til að ná upphæð til greiðslu.</span><span class="sxs-lookup"><span data-stu-id="03e77-122">This means that the user can use a combination of notes to reach the amount due.</span></span> <span data-ttu-id="03e77-123">Ef upphæðin til greiðslu er t.d. $25.00, getur notandinn valið $20 og $5 til að ljúka sölunni.</span><span class="sxs-lookup"><span data-stu-id="03e77-123">For example, if the amount due is $25.00, the user can choose $20 and $5 to complete the sale.</span></span>

