---
title: Setja upp valmyndaratriði fartækis til að ljúka vinnu af gerðinni innkaupapöntun
description: Þessi verklýsing sýnir hvernig á að setja upp valmyndaratriði fartækis.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem, WHSRFAutoConfirm, WHSRFMenu
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 707fc9c798da8eac30cc9f56c158be3d96b271d6
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/01/2019
ms.locfileid: "1847112"
---
# <a name="set-up-a-mobile-device-menu-item-for-completing-work-of-type-purchase-order"></a><span data-ttu-id="de203-103">Setja upp valmyndaratriði fartækis til að ljúka vinnu af gerðinni innkaupapöntun</span><span class="sxs-lookup"><span data-stu-id="de203-103">Set up a mobile device menu item for completing work of type Purchase order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="de203-104">Þessi verklýsing sýnir hvernig á að setja upp valmyndaratriði fartækis.</span><span class="sxs-lookup"><span data-stu-id="de203-104">This procedure shows how to set up a Mobile device menu item.</span></span> <span data-ttu-id="de203-105">Í þessu dæmi er Þetta valmyndaratriði notuð til að framkvæma vinnu með gerðinni innkaupapöntun.</span><span class="sxs-lookup"><span data-stu-id="de203-105">In this example, the menu item is used for performing work of type Purchase order.</span></span> <span data-ttu-id="de203-106">Vinnuklasi sem er tengdur við valmyndaratriði ákvarðar hvaða vinna er gild.</span><span class="sxs-lookup"><span data-stu-id="de203-106">The work class that’s associated with the menu item determines which work is valid.</span></span> <span data-ttu-id="de203-107">Hægt er að nota þessar leiðbeiningar í sýnifyrirtækinu USMF.</span><span class="sxs-lookup"><span data-stu-id="de203-107">You can use this guide in demo data company USMF.</span></span> <span data-ttu-id="de203-108">Þetta ferli er yfirleitt framkvæmt af stjórnandi vöruhúss.</span><span class="sxs-lookup"><span data-stu-id="de203-108">This procedure is typically carried out by a warehouse manager.</span></span>


## <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="de203-109">Stofna valmyndaratriði fartækis</span><span class="sxs-lookup"><span data-stu-id="de203-109">Create a mobile device menu item</span></span>
1. <span data-ttu-id="de203-110">Fara í valmyndaratriði fartækis</span><span class="sxs-lookup"><span data-stu-id="de203-110">Go to Mobile device menu items.</span></span>
2. <span data-ttu-id="de203-111">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="de203-111">Click New.</span></span>
3. <span data-ttu-id="de203-112">Í svæðið heiti valmyndaratriðis, færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="de203-112">In the Menu item name field, type a value.</span></span>
    * <span data-ttu-id="de203-113">Færa skal inn einkvæmt gildi.</span><span class="sxs-lookup"><span data-stu-id="de203-113">Enter a unique value.</span></span> <span data-ttu-id="de203-114">Til dæmis væri hægt að slá inn flutningur pöntunar.</span><span class="sxs-lookup"><span data-stu-id="de203-114">For example, you could type POMove.</span></span> <span data-ttu-id="de203-115">Muna skal gildi, Þú þarft það síðar.</span><span class="sxs-lookup"><span data-stu-id="de203-115">Remember the value, you'll need it later.</span></span>  
4. <span data-ttu-id="de203-116">Í reitinn Titill skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="de203-116">In the Title field, type a value.</span></span>
    * <span data-ttu-id="de203-117">Þetta er titillinn sem birtist í fartækinu.</span><span class="sxs-lookup"><span data-stu-id="de203-117">This is the title which will be displayed on the mobile device.</span></span> <span data-ttu-id="de203-118">Til dæmis væri hægt að slá inn ‚flutningur pöntunar‘.</span><span class="sxs-lookup"><span data-stu-id="de203-118">For example, you could type PO Move.</span></span>  
5. <span data-ttu-id="de203-119">Í reitnum Stilling velurðu „Vinna“.</span><span class="sxs-lookup"><span data-stu-id="de203-119">In the Mode field, select 'Work'.</span></span>
6. <span data-ttu-id="de203-120">Velja skal Já í Nota fyrirliggjandi vinnu svæðinu.</span><span class="sxs-lookup"><span data-stu-id="de203-120">Select Yes in the Use existing work field.</span></span>
    * <span data-ttu-id="de203-121">Valmyndaratriði fartækis er notuð til að framkvæma fyrirliggjandi vinnu.</span><span class="sxs-lookup"><span data-stu-id="de203-121">This mobile device menu item is used to perform existing work.</span></span> <span data-ttu-id="de203-122">Þess vegna verður að setja þetta gildi á Já.</span><span class="sxs-lookup"><span data-stu-id="de203-122">Therefore you must set this value to Yes.</span></span>  
    * <span data-ttu-id="de203-123">Birta stöðusvæði birgða ákvarðar hvort birgðastöðu á lager birtist vöruhús starfsmann í fartækinu.</span><span class="sxs-lookup"><span data-stu-id="de203-123">The Display inventory status field determines whether the inventory status of the on-hand inventory will be displayed to the warehouse worker on the mobile device.</span></span>  
7. <span data-ttu-id="de203-124">Í svæðinu Stýrt af, velja 'Kerfisflokkun'.</span><span class="sxs-lookup"><span data-stu-id="de203-124">In the Directed by field, select 'System grouping'.</span></span>
    * <span data-ttu-id="de203-125">Þegar eitthvað er valið í reitnum Stýrt af, birtast viðbótarreitir í hlutanum Almennt á þessari síðu.</span><span class="sxs-lookup"><span data-stu-id="de203-125">When you select something in the Directed by field, additional fields appear in the General section on this page.</span></span> <span data-ttu-id="de203-126">Svæði sem birtast velta á því hvað er var valið.</span><span class="sxs-lookup"><span data-stu-id="de203-126">The fields that appear depend on what you selected.</span></span> <span data-ttu-id="de203-127">Þegar er valið Kerfisflokkun, er bætt við tvö ný svæði.</span><span class="sxs-lookup"><span data-stu-id="de203-127">When you select System grouping, two new fields are added.</span></span> <span data-ttu-id="de203-128">Þær eru útskýrt hér að neðan</span><span class="sxs-lookup"><span data-stu-id="de203-128">These are explained below.</span></span>  
8. <span data-ttu-id="de203-129">Í kerfisflokkunarsvæði, veljið 'WorkPoolId'.</span><span class="sxs-lookup"><span data-stu-id="de203-129">In the System grouping field, select 'WorkPoolId'.</span></span>
    * <span data-ttu-id="de203-130">Þegar starfsmenn vöruhúss þetta valmyndaratriði opnar, þær verður beðnir um að skanna auðkenni vinnuhóps.</span><span class="sxs-lookup"><span data-stu-id="de203-130">When warehouse workers open this menu item, they’ll be asked to scan a Work pool ID.</span></span> <span data-ttu-id="de203-131">Öll vinna pantanir með þetta Auðkenni vinnuhóps og opna vinnupöntunar línur með einni af vinnuklösum sem bætt er við þetta valmyndaratriði verður ýtt til notanda.</span><span class="sxs-lookup"><span data-stu-id="de203-131">All work orders with this Work pool ID and open work order lines with one of the work classes added to this menu item will be pushed to the user.</span></span>  
9. <span data-ttu-id="de203-132">Færa inn gildi í svæði merki kerfisflokkunar.</span><span class="sxs-lookup"><span data-stu-id="de203-132">In the System grouping label field, type a value.</span></span>
    * <span data-ttu-id="de203-133">Textinn sem birtist fartækjanotandanum</span><span class="sxs-lookup"><span data-stu-id="de203-133">This is the text displayed to the user on the mobile device.</span></span> <span data-ttu-id="de203-134">Til dæmis væri hægt að slá inn vinnuhópur.</span><span class="sxs-lookup"><span data-stu-id="de203-134">For example, you could type Work pool.</span></span>  
10. <span data-ttu-id="de203-135">Velja Já í Hnekkingu númeraplötu við frágang svæðið .</span><span class="sxs-lookup"><span data-stu-id="de203-135">Select Yes in the Override license plate during put field.</span></span>
    * <span data-ttu-id="de203-136">Þessi valkostur gerir starfsmenn vöruhúss kleift að hnekkja marknúmeraplötunni þegar vörur eru settar á staðsetningu númeraplötustýrða.</span><span class="sxs-lookup"><span data-stu-id="de203-136">This option allows warehouse workers to override the target license plate when items are put down on a license plate controlled location.</span></span>  
11. <span data-ttu-id="de203-137">Velja skal Já í svæði frágangur Hóps.</span><span class="sxs-lookup"><span data-stu-id="de203-137">Select Yes in the Group put away field.</span></span>
    * <span data-ttu-id="de203-138">Ef allar línur fyrir Frágangur á vinnupöntun deila sama staðsetningu, fær notandi einn sameinað Frágangur fyrirmæli fyrir allar línur.</span><span class="sxs-lookup"><span data-stu-id="de203-138">If all the Put lines on the work order share the same location, the user will receive one combined Put instruction for all lines.</span></span>  
    * <span data-ttu-id="de203-139">Endurskoðunarsniðmátskennið: endurskoðunarsniðmát fyrir vinnu gerir kleift að tilgreina að vinnuferli fyrir valmyndaratriði ætti að rjúfa þannig að annað aðgerð hægt að keyra.</span><span class="sxs-lookup"><span data-stu-id="de203-139">Audit template ID: A work audit template allows you to specify that the work process for a menu item should be interrupted so that another operation can be performed.</span></span> <span data-ttu-id="de203-140">Til dæmis, ef þetta valmyndaratriði er fyrir vinnu á innleið gæti endurskoðunarsniðmátið krafist að starfsmaður athugi hitastig.</span><span class="sxs-lookup"><span data-stu-id="de203-140">For example, if this menu item is for inbound work, the audit template might require that the worker checks the temperature.</span></span> <span data-ttu-id="de203-141">Punktur ferlið rofin er tilgreindur fyrir endurskoðunarsniðmátið og getur til dæmis þegar vinna er hafin eða er lokið, eða þegar breytir stöðu hennar.</span><span class="sxs-lookup"><span data-stu-id="de203-141">The point at which the process is interrupted is specified on the audit template and can be, for example, when work is started or completed, or when its status changes.</span></span>  
12. <span data-ttu-id="de203-142">Útvíkka hlutann vinnuklasar.</span><span class="sxs-lookup"><span data-stu-id="de203-142">Expand the Work classes section.</span></span>
13. <span data-ttu-id="de203-143">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="de203-143">Click New.</span></span>
14. <span data-ttu-id="de203-144">Í svæðinu auðkenni vinnuklasa, færðu inn 'innkaup'.</span><span class="sxs-lookup"><span data-stu-id="de203-144">In the Work class ID field, type 'Purchase'.</span></span>
    * <span data-ttu-id="de203-145">Vinnuhópinn takmarkar vinnu sem hægt er að nota valmyndaratriði fyrir.</span><span class="sxs-lookup"><span data-stu-id="de203-145">The work pool restricts the work that the menu item can be used for.</span></span> <span data-ttu-id="de203-146">Í þessu tilfelli verður að nota hana fyrir opnar vinnupöntunarlínur sem hafa Innkaup vinnuklasi kenni.</span><span class="sxs-lookup"><span data-stu-id="de203-146">In this case it will be used for open work order lines that have the Purchase work class ID.</span></span>  
15. <span data-ttu-id="de203-147">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="de203-147">Click Save.</span></span>

## <a name="set-up-work-confirmation"></a><span data-ttu-id="de203-148">Setja upp vinnustaðfestingu</span><span class="sxs-lookup"><span data-stu-id="de203-148">Set up work confirmation</span></span>
1. <span data-ttu-id="de203-149">Smellt er á Uppsetning verkstaðfestingar</span><span class="sxs-lookup"><span data-stu-id="de203-149">Click Work confirmation setup.</span></span>
2. <span data-ttu-id="de203-150">Veljið í svæðinu vinnutegund 'Taka'.</span><span class="sxs-lookup"><span data-stu-id="de203-150">In the Work type field, select 'Pick'.</span></span>
3. <span data-ttu-id="de203-151">Velja Sjálfvirkt staðfesta gátreitinn.</span><span class="sxs-lookup"><span data-stu-id="de203-151">Select the Auto confirm check box.</span></span>
    * <span data-ttu-id="de203-152">Leiðbeining fyrir vinnu með vinnugerð Tiltekt verður sjálfkrafa staðfestar.</span><span class="sxs-lookup"><span data-stu-id="de203-152">The work instruction with work type Pick will be auto-confirmed.</span></span> <span data-ttu-id="de203-153">Þessi fyrirmæli verða ekki sýnd notandanum.</span><span class="sxs-lookup"><span data-stu-id="de203-153">This instruction will not be presented to the user.</span></span>  
4. <span data-ttu-id="de203-154">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="de203-154">Click New.</span></span>
5. <span data-ttu-id="de203-155">Í reitnum Vinnutegund velurðu ‚Frágangur‘.</span><span class="sxs-lookup"><span data-stu-id="de203-155">In the Work type field, select 'Put'.</span></span>
6. <span data-ttu-id="de203-156">Veljið gátreitinn fyrir staðfestingu á Staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="de203-156">Select the Location confirmation check box.</span></span>
    * <span data-ttu-id="de203-157">Starfsmaður í vöruhúsi er beðinn um að framkvæma staðfestingu skönnun staðsetningu þegar varan er sett niður.</span><span class="sxs-lookup"><span data-stu-id="de203-157">The warehouse worker will be asked to perform a confirmation scan of the location, when the item is put down.</span></span>  
7. <span data-ttu-id="de203-158">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="de203-158">Click Save.</span></span>
8. <span data-ttu-id="de203-159">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="de203-159">Close the page.</span></span>
9. <span data-ttu-id="de203-160">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="de203-160">Close the page.</span></span>

## <a name="add-the-menu-item-to-a-mobile-device-menu"></a><span data-ttu-id="de203-161">Bæta valmyndaratriði við valmynd fartækis</span><span class="sxs-lookup"><span data-stu-id="de203-161">Add the menu item to a mobile device menu</span></span>
1. <span data-ttu-id="de203-162">Fara í valmyndina Fartæki</span><span class="sxs-lookup"><span data-stu-id="de203-162">Go to Mobile device menu.</span></span>
2. <span data-ttu-id="de203-163">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="de203-163">Click Edit.</span></span>
3. <span data-ttu-id="de203-164">Nota flýtiafmörkun til að finna færslur</span><span class="sxs-lookup"><span data-stu-id="de203-164">Use the Quick Filter to find records.</span></span> <span data-ttu-id="de203-165">Til dæmis, sía svæðið Heiti með gildinu 'á innleið'.</span><span class="sxs-lookup"><span data-stu-id="de203-165">For example, filter on the Name field with a value of 'inbound'.</span></span>
    * <span data-ttu-id="de203-166">Óskað er að finna valmynd að nota fyrir valmyndaratriði á innleið.</span><span class="sxs-lookup"><span data-stu-id="de203-166">You want to find the menu you use for inbound menu items.</span></span> <span data-ttu-id="de203-167">Í USMF, þessi reitur er kallaður á innleið.</span><span class="sxs-lookup"><span data-stu-id="de203-167">In USMF this is called Inbound.</span></span>  
4. <span data-ttu-id="de203-168">Í trénu skal velja „gildi“.</span><span class="sxs-lookup"><span data-stu-id="de203-168">In the tree, select 'a value'.</span></span>
5. <span data-ttu-id="de203-169">Smella á ör sem vísar til hægri.</span><span class="sxs-lookup"><span data-stu-id="de203-169">Click on the arrow that points to the right.</span></span>
6. <span data-ttu-id="de203-170">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="de203-170">Click Save.</span></span>
7. <span data-ttu-id="de203-171">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="de203-171">Close the page.</span></span>

