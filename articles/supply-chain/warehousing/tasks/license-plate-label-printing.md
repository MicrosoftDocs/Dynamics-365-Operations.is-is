--- 
title: "Virkja prentun merkis á númeraplötu"
description: "Þetta ferli gerir sjálfvirka prentun Raðnúmerskóða fyrir sendingu gáms (SSCC) merki eftir að síðasta vara er tekin úr birgðum í tiltektarferli sölu."
author: perlynne
manager: AnnBe
ms.date: 11/03/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 6d186bf7e4aee8cfa97adbd90b9090085e842f9b
ms.contentlocale: is-is
ms.lasthandoff: 08/29/2017

---
# <a name="enable-license-plate-label-printing"></a><span data-ttu-id="b5aa6-103">Virkja prentun merkis á númeraplötu</span><span class="sxs-lookup"><span data-stu-id="b5aa6-103">Enable license plate label printing</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b5aa6-104">Þetta ferli gerir sjálfvirka prentun Raðnúmerskóða fyrir sendingu gáms (SSCC) merki eftir að síðasta vara er tekin úr birgðum í tiltektarferli sölu.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-104">This procedure enables the automatic printing of a Serial shipping container code (SSCC) label after the last item is picked from inventory in a sales picking work process.</span></span> <span data-ttu-id="b5aa6-105">Hægt er að keyra þetta ferli fyrir sýnigögn fyrirtækisins USMF.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-105">You can run this procedure in demo data company USMF.</span></span> <span data-ttu-id="b5aa6-106">Ef verið er að keyra hana með eigin gögn, þarf að hafa sett upp númeraröð fyrir númeraplötur.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-106">If you’re run it using your own data, you need to have a number sequence set up for license plates.</span></span> <span data-ttu-id="b5aa6-107">Þarf að setja upp merkimiði prentarinn áður en byrjað er að þetta verkefni.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-107">You need to set up a label printer before you begin this task.</span></span> <span data-ttu-id="b5aa6-108">Fara á fyrirtækisstjórnun > Uppsetning > Prentarar á neti.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-108">Go to Organization administration > Setup > Network printers.</span></span> <span data-ttu-id="b5aa6-109">Á aðgerðasvæðinu skal smellt er á Valkostum og smella svo á uppsetningarhnapp fyrir niðurhal skjals leiðarfulltrúa.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-109">On the Action pane, click Options, and then click the Download document routing agent installer button.</span></span> <span data-ttu-id="b5aa6-110">Keyra uppsetningarforritið og gangið úr skugga um að þú hefur virkan prentara á neti stilltan áður en haldið er áfram með ferlið.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-110">Run the installer and make sure that you have a working network printer set to Active before you continue with the procedure.</span></span>


## <a name="set-up-the-gs1-company-prefix"></a><span data-ttu-id="b5aa6-111">Setja upp GS1-fyrirtækjaforskeyti</span><span class="sxs-lookup"><span data-stu-id="b5aa6-111">Set up the GS1 company prefix</span></span>
1. <span data-ttu-id="b5aa6-112">Fara í vöruhúsakerfi > Uppsetning > Færibreytur vöruhúsakerfis.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-112">Go to Warehouse management > Setup > Warehouse management parameters.</span></span>
2. <span data-ttu-id="b5aa6-113">Í svæðinu fyrir forskeyti GS1 fyrirtækis, færið inn 7 tölur fyrir GS1 númer fyrirtækis þíns .</span><span class="sxs-lookup"><span data-stu-id="b5aa6-113">In the GS1 company prefix field, enter the 7 numbers for your GS1 company number.</span></span>
3. <span data-ttu-id="b5aa6-114">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-114">Click Save.</span></span>
4. <span data-ttu-id="b5aa6-115">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-115">Close the page.</span></span>

## <a name="setup-the-sscc-license-plate-number-sequence"></a><span data-ttu-id="b5aa6-116">Setja upp númeraröð SSCC númeraplötu</span><span class="sxs-lookup"><span data-stu-id="b5aa6-116">Setup the SSCC license plate number sequence</span></span>
1. <span data-ttu-id="b5aa6-117">Fara í Fyrirtækisstjórnun > Númeraröð > Númeraröð.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-117">Go to Organization administration > Number sequences > Number sequences.</span></span>
2. <span data-ttu-id="b5aa6-118">Í reitnum Svæði skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-118">In the Area field, select an option.</span></span>
3. <span data-ttu-id="b5aa6-119">Í reitnum Tilvísun skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-119">In the Reference field, select an option.</span></span>
4. <span data-ttu-id="b5aa6-120">Í reitinn Fyrirtæki skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-120">In the Company field, type a value.</span></span>
5. <span data-ttu-id="b5aa6-121">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-121">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="b5aa6-122">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-122">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="b5aa6-123">Stækka the hlutann hlutir.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-123">Expand the Segments section.</span></span>
8. <span data-ttu-id="b5aa6-124">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-124">Click Edit.</span></span>
9. <span data-ttu-id="b5aa6-125">Veljið fyrstu línu í töflunni Hlutar</span><span class="sxs-lookup"><span data-stu-id="b5aa6-125">In the Segments table, select the first row</span></span>
10. <span data-ttu-id="b5aa6-126">Smella á Fjarlægja.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-126">Click Remove.</span></span>
11. <span data-ttu-id="b5aa6-127">Smella á Fjarlægja.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-127">Click Remove.</span></span>
12. <span data-ttu-id="b5aa6-128">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-128">Click Save.</span></span>
13. <span data-ttu-id="b5aa6-129">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-129">Close the page.</span></span>

## <a name="create-the-document-route-layout"></a><span data-ttu-id="b5aa6-130">Stofna útlit leið skjals </span><span class="sxs-lookup"><span data-stu-id="b5aa6-130">Create the document route layout</span></span>
1. <span data-ttu-id="b5aa6-131">Fara í vöruhúsakerfi > Uppsetning > Skjalaleið > Útlit skjalaleiðar.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-131">Go to Warehouse management > Setup > Document routing > Document routing layouts.</span></span>
    * <span data-ttu-id="b5aa6-132">Virkja SSCC útlit.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-132">Enable the SSCC layout.</span></span>  
2. <span data-ttu-id="b5aa6-133">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-133">Click New.</span></span>
3. <span data-ttu-id="b5aa6-134">Færa inn gildi í reitnum Kenni útlits.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-134">In the Layout ID field, type a value.</span></span>
4. <span data-ttu-id="b5aa6-135">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-135">In the Description field, type a value.</span></span>
5. <span data-ttu-id="b5aa6-136">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-136">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="b5aa6-137">Smella á Setja inn aftan við texta</span><span class="sxs-lookup"><span data-stu-id="b5aa6-137">Click Insert at end of text.</span></span>
7. <span data-ttu-id="b5aa6-138">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-138">Click Save.</span></span>
8. <span data-ttu-id="b5aa6-139">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-139">Close the page.</span></span>

## <a name="set-up-the-document-routing"></a><span data-ttu-id="b5aa6-140">Setja upp skjalaleið</span><span class="sxs-lookup"><span data-stu-id="b5aa6-140">Set up the document routing</span></span>
1. <span data-ttu-id="b5aa6-141">Fara í vöruhúsakerfi > Uppsetning >  Skjalaleið > Skjalaleið.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-141">Go to Warehouse management > Setup > Document routing > Document routing.</span></span>
2. <span data-ttu-id="b5aa6-142">Í svæðinu gerð vinnupöntunar, skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-142">In the Work order type field, select an option.</span></span>
3. <span data-ttu-id="b5aa6-143">Smellt er á Nýtt.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-143">Click New.</span></span>
4. <span data-ttu-id="b5aa6-144">Í reitinn vöruhús skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-144">In the Warehouse field, type a value.</span></span>
5. <span data-ttu-id="b5aa6-145">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-145">In the Name field, type a value.</span></span>
6. <span data-ttu-id="b5aa6-146">Smellt er á Nýtt.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-146">Click New.</span></span>
7. <span data-ttu-id="b5aa6-147">Í reitinn útlit kennis skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-147">In the Layout ID field, enter or select a value.</span></span>
8. <span data-ttu-id="b5aa6-148">Í reitnum Heiti, Færið inn heiti prentara sem á að nota.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-148">In the Name field, enter the printer name that you want to use..</span></span>
9. <span data-ttu-id="b5aa6-149">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-149">Click Save.</span></span>
10. <span data-ttu-id="b5aa6-150">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-150">Close the page.</span></span>

## <a name="create-mobile-device-menu"></a><span data-ttu-id="b5aa6-151">Stofna Valmynd fartækja</span><span class="sxs-lookup"><span data-stu-id="b5aa6-151">Create mobile device menu</span></span>
1. <span data-ttu-id="b5aa6-152">Fara í vöruhúsakerfi > Uppsetning > fartækis > Valmyndaratriði fartækis</span><span class="sxs-lookup"><span data-stu-id="b5aa6-152">Go to Warehouse management > Setup > Mobile device > Mobile device menu items.</span></span>
2. <span data-ttu-id="b5aa6-153">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-153">Click New.</span></span>
3. <span data-ttu-id="b5aa6-154">Í svæðið heiti valmyndaratriðis, færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-154">In the Menu item name field, type a value.</span></span>
4. <span data-ttu-id="b5aa6-155">Í reitinn Titill skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-155">In the Title field, type a value.</span></span>
5. <span data-ttu-id="b5aa6-156">Í reitnum hamur velurðu valkost.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-156">In the Mode field, select an option.</span></span>
6. <span data-ttu-id="b5aa6-157">Velja skal Já í Nota fyrirliggjandi vinnu svæðinu.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-157">Select Yes in the Use existing work field.</span></span>
7. <span data-ttu-id="b5aa6-158">Velja skal Já í svæðinu Mynda númeraplötu.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-158">Select Yes in the Generate license plate field.</span></span>
8. <span data-ttu-id="b5aa6-159">Útvíkka hlutann vinnuklasar.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-159">Expand the Work classes section.</span></span>
9. <span data-ttu-id="b5aa6-160">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-160">Click New.</span></span>
10. <span data-ttu-id="b5aa6-161">Færa inn gildi í reitnum Kenni Vinnuklasa .</span><span class="sxs-lookup"><span data-stu-id="b5aa6-161">In the Work class ID field, type a value.</span></span>
11. <span data-ttu-id="b5aa6-162">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-162">Click Save.</span></span>
12. <span data-ttu-id="b5aa6-163">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-163">Close the page.</span></span>
13. <span data-ttu-id="b5aa6-164">Fara í vöruhúsakerfi > Uppsetning > fartækis > Valmynd fartækis</span><span class="sxs-lookup"><span data-stu-id="b5aa6-164">Go to Warehouse management > Setup > Mobile device > Mobile device menu.</span></span>
14. <span data-ttu-id="b5aa6-165">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-165">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="b5aa6-166">Veljið, í trénu ', í trénu veldu valmyndaratriði sem var stofnuð áður.'.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-166">In the tree, select 'In the tree, select the menu item that you created before.'.</span></span>
16. <span data-ttu-id="b5aa6-167">Smella á Breyta.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-167">Click Edit.</span></span>
17. <span data-ttu-id="b5aa6-168">Smellt er á örina til að bæta valmyndaratriði við valmynd.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-168">Click on the arrow to add the menu item to the menu.</span></span>
18. <span data-ttu-id="b5aa6-169">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-169">Click Save.</span></span>
19. <span data-ttu-id="b5aa6-170">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-170">Close the page.</span></span>

## <a name="update-a-work-template"></a><span data-ttu-id="b5aa6-171">Uppfæra sniðmát verks</span><span class="sxs-lookup"><span data-stu-id="b5aa6-171">Update a work template</span></span>
1. <span data-ttu-id="b5aa6-172">Fara í vöruhúsakerfi  > Uppsetning  > Vinna  > Vinnusniðmát.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-172">Go to Warehouse management > Setup > Work > Work templates.</span></span>
2. <span data-ttu-id="b5aa6-173">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-173">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="b5aa6-174">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-174">Click Edit.</span></span>
4. <span data-ttu-id="b5aa6-175">Smellt er á Nýtt.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-175">Click New.</span></span>
5. <span data-ttu-id="b5aa6-176">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-176">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="b5aa6-177">Veljið í svæðinu vinnutegund "Prenta".</span><span class="sxs-lookup"><span data-stu-id="b5aa6-177">In the Work type field, select 'Print'.</span></span>
7. <span data-ttu-id="b5aa6-178">Færa inn eða velja gildi í reitnum Kenni Vinnuklasa.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-178">In the Work class ID field, enter or select a value.</span></span>
8. <span data-ttu-id="b5aa6-179">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-179">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="b5aa6-180">Smelltu á Flytja upp.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-180">Click Move up.</span></span>
10. <span data-ttu-id="b5aa6-181">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-181">Click Save.</span></span>
11. <span data-ttu-id="b5aa6-182">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-182">Close the page.</span></span>


