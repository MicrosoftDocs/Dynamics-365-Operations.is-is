---
title: Fletta upp gildandi verði og afslætti
description: Þessi ferli sýnir hvernig á að finna verð og/eða afsláttur fyrir afurð sem er gild fyrir ákveðinn viðskiptavin, án þess að stofna sölupöntun.
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ba95e651898da0e0fbd1221f61436ffac59db09e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "359866"
---
# <a name="look-up-applicable-prices-and-discounts"></a><span data-ttu-id="a7ca2-103">Fletta upp gildandi verði og afslætti</span><span class="sxs-lookup"><span data-stu-id="a7ca2-103">Look up applicable prices and discounts</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a7ca2-104">Þessi ferli sýnir hvernig á að finna verð og/eða afsláttur fyrir afurð sem er gild fyrir ákveðinn viðskiptavin, án þess að stofna sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="a7ca2-104">This procedure shows how to find the price and/or discount for a product which is currently valid for a specific customer, without creating a sales order.</span></span> <span data-ttu-id="a7ca2-105">Ferlið fer í gegnum tiltekið dæmi og þú þarft að fylgja dæminu sem notar USMF sýnigögn fyrirtæki til að velja nauðsynleg gildi.</span><span class="sxs-lookup"><span data-stu-id="a7ca2-105">The procedure walks through a specific example, and you need follow the example using the USMF demo company in order to select the necessary values.</span></span>


## <a name="find-the-applicable-price"></a><span data-ttu-id="a7ca2-106">Finna viðeigandi verð</span><span class="sxs-lookup"><span data-stu-id="a7ca2-106">Find the applicable price</span></span>
1. <span data-ttu-id="a7ca2-107">Fara í Sölu og markaðssetningu > Verð og afslætti > Finna verð.</span><span class="sxs-lookup"><span data-stu-id="a7ca2-107">Go to Sales and marketing > Prices and discounts > Find prices.</span></span>
2. <span data-ttu-id="a7ca2-108">Í reitnum Reikningur viðskiptavina skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="a7ca2-108">In the Customer account field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="a7ca2-109">Á listanum finna og velja viðskiptavin US-001.</span><span class="sxs-lookup"><span data-stu-id="a7ca2-109">In the list, find and select customer US-001.</span></span>
4. <span data-ttu-id="a7ca2-110">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="a7ca2-110">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="a7ca2-111">Sláið inn „T0004“ á svæðinu „Vörunúmer“.</span><span class="sxs-lookup"><span data-stu-id="a7ca2-111">In the Item number field, type 'T0004'.</span></span>
    * <span data-ttu-id="a7ca2-112">Að sjálfgefnu er svæðið Magn er stillt á 1.</span><span class="sxs-lookup"><span data-stu-id="a7ca2-112">By default, the Quantity field is set to 1.</span></span> <span data-ttu-id="a7ca2-113">Hins vegar ef vitað er um stærð pöntunarinnar sem viðskiptavinurinn ætlar að panta fyrir viðkomandi afurð, færið þá þetta gildi í staðinn.</span><span class="sxs-lookup"><span data-stu-id="a7ca2-113">However, if you know the size of the order that the customer intends to place for the product in question, then enter this value instead.</span></span> <span data-ttu-id="a7ca2-114">Þessar upplýsingar skipta máli ef verðsamninga við viðskiptavininn hefur hlé í magni, það er, verð afurðarinnar er háð lágmarksmagni sem keypt er.</span><span class="sxs-lookup"><span data-stu-id="a7ca2-114">This information is relevant if the trade agreements with the customer have quantity breaks, that is, the product's price depends on the minimum quantity purchased.</span></span>  
6. <span data-ttu-id="a7ca2-115">Í svæði Dagsetningar, Færið inn dagsetningu þegar viðskiptavinurinn reiknar með að panta</span><span class="sxs-lookup"><span data-stu-id="a7ca2-115">In the Date field, enter a date for when the customer expects to place an order.</span></span> 
    * <span data-ttu-id="a7ca2-116">Dagsetningin getur verið dagurinn í dag eða hvaða dagsetningu í framtíðinni.</span><span class="sxs-lookup"><span data-stu-id="a7ca2-116">The date can be today's date or any date in the future.</span></span>  
    * <span data-ttu-id="a7ca2-117">Nú skilar kerfið verði sem er gild fyrir valda afurð þegar hún er keypt af valinn viðskiptavinur á valinni dagsetningu með tilgreindu magni.</span><span class="sxs-lookup"><span data-stu-id="a7ca2-117">The system now returns the price that is valid for the selected product when bought by the selected customer on the selected date with a specified quantity.</span></span> <span data-ttu-id="a7ca2-118">Í þessu dæmi, ef viðskiptavinur US-001 keypti 1 einingu af afurð T0004 í dag væri hann rukkaður um 350 CAD á einingu.</span><span class="sxs-lookup"><span data-stu-id="a7ca2-118">In this example, if the customer US-001 bought 1 unit of product T0004 today, they would be charged 350 CAD a unit.</span></span> <span data-ttu-id="a7ca2-119">Verðið kemur úr fyrirliggjandi og virkum viðskiptasamningi við viðskiptavininn.</span><span class="sxs-lookup"><span data-stu-id="a7ca2-119">This price comes from an existing and active trade agreement with the customer.</span></span>      <span data-ttu-id="a7ca2-120">Önnur svæði á síðunni veita frekari upplýsingar um afurðarverð og -kostnað (ef sett er upp á afurðarsniðmáti), og arðsemi er reiknuð út.</span><span class="sxs-lookup"><span data-stu-id="a7ca2-120">Other fields on the page provide more details about the product price and product cost (if set up on the product master), and calculated profitability.</span></span>  
    * <span data-ttu-id="a7ca2-121">Ef valkosturinn Sýna tengda afurðarafbrigði er valinn, merkir það að til eru viðbótar verðsamninga fyrir afurðarafbrigðin.</span><span class="sxs-lookup"><span data-stu-id="a7ca2-121">If the Show related product variants option is selected, it means that there are additional trade agreements for product's variants.</span></span>  
7. <span data-ttu-id="a7ca2-122">smellt á Sýna tengd afurðarafbrigði gátreitinn.</span><span class="sxs-lookup"><span data-stu-id="a7ca2-122">Click the Show related product variants checkbox.</span></span>
    * <span data-ttu-id="a7ca2-123">Listi yfir afurðarafbrigði er sýndur, með upplýsingum um víddir þeirra.</span><span class="sxs-lookup"><span data-stu-id="a7ca2-123">A list of the product variants is shown, with information about their dimensions.</span></span>  
8. <span data-ttu-id="a7ca2-124">Merkja línuna sem táknar Hvítan lit, á listanum.</span><span class="sxs-lookup"><span data-stu-id="a7ca2-124">In the list, mark the line representing color White.</span></span>
    * <span data-ttu-id="a7ca2-125">Athugið að vöruverðið er nú annað en það sem hefur áður verið birt þegar það var ekki tilgreint eftir vídd.</span><span class="sxs-lookup"><span data-stu-id="a7ca2-125">Notice, that the product price is now different from the one displayed previously when it was not specified per dimension.</span></span>  
9. <span data-ttu-id="a7ca2-126">Smellt er á Skoða söluverð.</span><span class="sxs-lookup"><span data-stu-id="a7ca2-126">Click View sales prices.</span></span>
    * <span data-ttu-id="a7ca2-127">Síðan Verð (sala) birtir alla verðsamninga sem gilda um afurð, þ.m.t. afbrigði hennar.</span><span class="sxs-lookup"><span data-stu-id="a7ca2-127">The Price (sales) page displays all the trade agreements applicable to the product, including its variants.</span></span>  
10. <span data-ttu-id="a7ca2-128">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="a7ca2-128">Close the page.</span></span>

## <a name="find-the-applicable-discount"></a><span data-ttu-id="a7ca2-129">Finna viðeigandi afsláttur</span><span class="sxs-lookup"><span data-stu-id="a7ca2-129">Find the applicable discount</span></span>
    * <span data-ttu-id="a7ca2-130">Gangið úr skugga um að svæðið viðskiptavinalykill innihaldi númer viðskiptavinar US-001 </span><span class="sxs-lookup"><span data-stu-id="a7ca2-130">Make sure the Customer account field contains customer number US-001</span></span>   
1. <span data-ttu-id="a7ca2-131">Sláið inn „T0012“ á svæðinu „Vörunúmer“.</span><span class="sxs-lookup"><span data-stu-id="a7ca2-131">In the Item number field, type 'T0012'.</span></span>
    * <span data-ttu-id="a7ca2-132">Gangið úr skugga um að svæðið Magn er stillt á 1.</span><span class="sxs-lookup"><span data-stu-id="a7ca2-132">Make sure the Quantity field is set to 1.</span></span>  
    * <span data-ttu-id="a7ca2-133">Eftirfarandi verðupplýsingum sem sýnd eru fyrir afurð T0012 koma úr einni eða fleiri verðsamninga: einingarverð er 1.000 CAD og afsláttarprósentan er 5.</span><span class="sxs-lookup"><span data-stu-id="a7ca2-133">The following pricing details shown for product T0012 come from one or more trade agreements: The unit price is 1,000 CAD and the discount percentage is 5.</span></span>  
2. <span data-ttu-id="a7ca2-134">Stillið magn á „20“.</span><span class="sxs-lookup"><span data-stu-id="a7ca2-134">Set Quantity to '20'.</span></span>
    * <span data-ttu-id="a7ca2-135">Aukinn pöntunarmagn veldur línuafslátt sem er boðið viðskiptavini til að breyta úr 5 til 7 prósent.</span><span class="sxs-lookup"><span data-stu-id="a7ca2-135">The increased order quantity causes the line discount that will be offered to the customer to change from 5 to 7 percent.</span></span>  
    * <span data-ttu-id="a7ca2-136">Nettó upphæð er reiknuð á grundvelli á einingaverðs, afslætti og heildarmagni.</span><span class="sxs-lookup"><span data-stu-id="a7ca2-136">The Net amount is calculated based on the unit price, discount and the total quantity.</span></span>  
3. <span data-ttu-id="a7ca2-137">Smellt er á Skoða línuafslátt.</span><span class="sxs-lookup"><span data-stu-id="a7ca2-137">Click View line discount.</span></span>
    * <span data-ttu-id="a7ca2-138">Það eru tvær línuafsláttarsamninga fyrir afurða T0012, sem tilgreina 5 prósent afslátt í fyrir pöntunarmagn línu frá 1 til 10, og 7 prósent afsláttur fyrir magn yfir 10.</span><span class="sxs-lookup"><span data-stu-id="a7ca2-138">There are two line discount agreements for product T0012, specifying a 5 percent discount for an order line quantity from 1 to 10, and 7 percent discount for order quantities above 10.</span></span> <span data-ttu-id="a7ca2-139">Athugaðu að afslættir gilda um hóp afurða, í þessu dæmi, flokkskóði 01 sem afurðin T0012 tilheyrir.</span><span class="sxs-lookup"><span data-stu-id="a7ca2-139">Note that the discounts are applied to a group of products, in this example, Group code 01, of which product T0012 is a member.</span></span>  
4. <span data-ttu-id="a7ca2-140">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="a7ca2-140">Close the page.</span></span>

