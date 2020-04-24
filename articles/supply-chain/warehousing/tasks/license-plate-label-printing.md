---
title: Virkja prentun merkis á númeraplötu
description: Þetta efni sýnir hvernig á að virkja sjálfvirka prentun raðnúmerskóða fyrir sendingu gáms (SSCC) merki eftir að síðasta vara er tekin úr birgðum í tiltektarferli sölu.
author: perlynne
manager: tfehr
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysCorpNetPrinterList, WHSParameters, NumberSequenceTableListPage, NumberSequenceDetails, WHSDocumentRoutingLayout, WHSDocumentRouting, WHSRFMenuItem, WHSRFMenu, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 484a1465dd41429fe201de18aac55f118a483cab
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3217012"
---
# <a name="enable-license-plate-label-printing"></a><span data-ttu-id="06ef3-103">Virkja prentun merkis á númeraplötu</span><span class="sxs-lookup"><span data-stu-id="06ef3-103">Enable license plate label printing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="06ef3-104">Þetta efni sýnir hvernig á að virkja sjálfvirka prentun raðnúmerskóða fyrir sendingu gáms (SSCC) merki eftir að síðasta vara er tekin úr birgðum í tiltektarferli sölu.</span><span class="sxs-lookup"><span data-stu-id="06ef3-104">This topic shows how to enable the automatic printing of a Serial shipping container code (SSCC) label after the last item is picked from inventory in a sales picking work process.</span></span> <span data-ttu-id="06ef3-105">Hægt er að keyra þetta ferli fyrir sýnigögn fyrirtækisins USMF.</span><span class="sxs-lookup"><span data-stu-id="06ef3-105">You can run this procedure in demo data company USMF.</span></span> <span data-ttu-id="06ef3-106">Ef verið er að keyra hana með eigin gögn, þarf að hafa sett upp númeraröð fyrir númeraplötur.</span><span class="sxs-lookup"><span data-stu-id="06ef3-106">If you're run it using your own data, you need to have a number sequence set up for license plates.</span></span> <span data-ttu-id="06ef3-107">Þarf að setja upp merkimiði prentarinn áður en byrjað er að þetta verkefni.</span><span class="sxs-lookup"><span data-stu-id="06ef3-107">You need to set up a label printer before you begin this task.</span></span> <span data-ttu-id="06ef3-108">Fara á fyrirtækisstjórnun > Uppsetning > Prentarar á neti.</span><span class="sxs-lookup"><span data-stu-id="06ef3-108">Go to Organization administration > Setup > Network printers.</span></span> <span data-ttu-id="06ef3-109">Á aðgerðasvæðinu skal smellt er á Valkostum og smella svo á uppsetningarhnapp fyrir niðurhal skjals leiðarfulltrúa.</span><span class="sxs-lookup"><span data-stu-id="06ef3-109">On the Action pane, click Options, and then click the Download document routing agent installer button.</span></span> <span data-ttu-id="06ef3-110">Keyra uppsetningarforritið og gangið úr skugga um að þú hefur virkan prentara á neti stilltan áður en haldið er áfram með ferlið.</span><span class="sxs-lookup"><span data-stu-id="06ef3-110">Run the installer and make sure that you have a working network printer set to Active before you continue with the procedure.</span></span>


## <a name="set-up-the-gs1-company-prefix"></a><span data-ttu-id="06ef3-111">Setja upp GS1-fyrirtækjaforskeyti</span><span class="sxs-lookup"><span data-stu-id="06ef3-111">Set up the GS1 company prefix</span></span>
1. <span data-ttu-id="06ef3-112">Farðu í **Skoðunarrúðu > Kerfi > Vöruhúsakerfi > Uppsetning > Vöruhús > Færibreytur vöruhúsakerfis**.</span><span class="sxs-lookup"><span data-stu-id="06ef3-112">Go to **Navigation pane > Modules > Warehouse management > Setup > Warehouse management parameters**.</span></span>
2. <span data-ttu-id="06ef3-113">Í svæðinu **Forskeyti GS1 fyrirtækis** skaltu færa inn 7 tölur fyrir GS1 númer fyrirtækis þíns .</span><span class="sxs-lookup"><span data-stu-id="06ef3-113">In the **GS1 company prefix** field, enter the 7 numbers for your GS1 company number.</span></span>
3. <span data-ttu-id="06ef3-114">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="06ef3-114">Select **Save**.</span></span>
4. <span data-ttu-id="06ef3-115">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="06ef3-115">Close the page.</span></span>

## <a name="setup-the-sscc-license-plate-number-sequence"></a><span data-ttu-id="06ef3-116">Setja upp númeraröð SSCC númeraplötu</span><span class="sxs-lookup"><span data-stu-id="06ef3-116">Setup the SSCC license plate number sequence</span></span>
1. <span data-ttu-id="06ef3-117">Farðu í **Skoðunarrúða > Kerfiseiningar > Fyrirtækjastjórnun > Númeraraðir > Númeraraðir**.</span><span class="sxs-lookup"><span data-stu-id="06ef3-117">Go to **Navigation pane > Modules > Organization administration > Number sequences > Number sequences**.</span></span>
2. <span data-ttu-id="06ef3-118">Í reitnum **Svæði** skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="06ef3-118">In the **Area** field, select an option.</span></span>
3. <span data-ttu-id="06ef3-119">Í reitnum **Tilvísun** skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="06ef3-119">In the **Reference** field, select an option.</span></span>
4. <span data-ttu-id="06ef3-120">Í reitinn **Fyrirtæki** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="06ef3-120">In the **Company** field, type a value.</span></span>
5. <span data-ttu-id="06ef3-121">Stækkaðu hlutann **Hlutar**.</span><span class="sxs-lookup"><span data-stu-id="06ef3-121">Expand the **Segments** section.</span></span>
6. <span data-ttu-id="06ef3-122">Veljið **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="06ef3-122">Select **Edit**.</span></span>
7. <span data-ttu-id="06ef3-123">Í töflunni **Hlutar** skal velja fyrstu línuna</span><span class="sxs-lookup"><span data-stu-id="06ef3-123">In the **Segments** table, select the first row</span></span>
8. <span data-ttu-id="06ef3-124">Veldu **Fjarlægja**.</span><span class="sxs-lookup"><span data-stu-id="06ef3-124">Select **Remove**.</span></span>
9. <span data-ttu-id="06ef3-125">Veldu **Fjarlægja**.</span><span class="sxs-lookup"><span data-stu-id="06ef3-125">Select **Remove**.</span></span>
10. <span data-ttu-id="06ef3-126">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="06ef3-126">Select **Save**.</span></span>
11. <span data-ttu-id="06ef3-127">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="06ef3-127">Close the page.</span></span>

## <a name="create-the-document-route-layout"></a><span data-ttu-id="06ef3-128">Stofna útlit leið skjals</span><span class="sxs-lookup"><span data-stu-id="06ef3-128">Create the document route layout</span></span>
1. <span data-ttu-id="06ef3-129">Farðu í **Skoðunarrúðu > Kerfiseiningar > Vöruhúsakerfi > Uppsetning > Skjalaleið > Útlit skjalaleiðar**.</span><span class="sxs-lookup"><span data-stu-id="06ef3-129">Go to **Navigation pane > Modules > Warehouse management > Setup > Document routing > Document routing layouts**.</span></span> <span data-ttu-id="06ef3-130">Virkja SSCC útlit.</span><span class="sxs-lookup"><span data-stu-id="06ef3-130">Enable the SSCC layout.</span></span>  
2. <span data-ttu-id="06ef3-131">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="06ef3-131">Select **New**.</span></span>
3. <span data-ttu-id="06ef3-132">Í reitnum **Kenni útlits** skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="06ef3-132">In the **Layout ID** field, type a value.</span></span>
4. <span data-ttu-id="06ef3-133">Í reitinn **Lýsing** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="06ef3-133">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="06ef3-134">Veldu **Setja inn aftan við texta**.</span><span class="sxs-lookup"><span data-stu-id="06ef3-134">Select **Insert at end of text**.</span></span>
6. <span data-ttu-id="06ef3-135">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="06ef3-135">Select **Save**.</span></span>
7. <span data-ttu-id="06ef3-136">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="06ef3-136">Close the page.</span></span>

## <a name="set-up-the-document-routing"></a><span data-ttu-id="06ef3-137">Setja upp skjalaleið</span><span class="sxs-lookup"><span data-stu-id="06ef3-137">Set up the document routing</span></span>
1. <span data-ttu-id="06ef3-138">Farðu í **Skoðunarrúðu > Kerfiseiningar > Vöruhúsakerfi > Uppsetning > Skjalaleið > Skjalaleið**.</span><span class="sxs-lookup"><span data-stu-id="06ef3-138">Go to **Navigation pane > Modules > Warehouse management > Setup > Document routing > Document routing**.</span></span>
2. <span data-ttu-id="06ef3-139">Í reitnum **Gerð verkbeiðni** skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="06ef3-139">In the **Work order type** field, select an option.</span></span>
3. <span data-ttu-id="06ef3-140">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="06ef3-140">Select **New**.</span></span>
4. <span data-ttu-id="06ef3-141">Í reitinn **Vöruhús** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="06ef3-141">In the **Warehouse** field, type a value.</span></span>
5. <span data-ttu-id="06ef3-142">Í reitinn **Heiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="06ef3-142">In the **Name** field, type a value.</span></span>
6. <span data-ttu-id="06ef3-143">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="06ef3-143">Select **New**.</span></span>
7. <span data-ttu-id="06ef3-144">Í reitinn **Útlit kennis** skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="06ef3-144">In the **Layout ID** field, enter or select a value.</span></span>
8. <span data-ttu-id="06ef3-145">Í reitnum **Heiti** skal færa inn heiti prentarans sem á að nota.</span><span class="sxs-lookup"><span data-stu-id="06ef3-145">In the **Name** field, enter the printer name that you want to use.</span></span>
9. <span data-ttu-id="06ef3-146">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="06ef3-146">Select **Save**.</span></span>
10. <span data-ttu-id="06ef3-147">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="06ef3-147">Close the page.</span></span>

## <a name="create-mobile-device-menu"></a><span data-ttu-id="06ef3-148">Stofna Valmynd fartækja</span><span class="sxs-lookup"><span data-stu-id="06ef3-148">Create mobile device menu</span></span>
1. <span data-ttu-id="06ef3-149">Farðu í **Skoðunarrúðuna > Kerfiseiningar > Vöruhúsakerfi > Uppsetning > Fartæki > Valmyndaratriði fartækis**.</span><span class="sxs-lookup"><span data-stu-id="06ef3-149">Go to **Navigation pane > Modules > Warehouse management > Setup > Mobile device > Mobile device menu items**.</span></span>
2. <span data-ttu-id="06ef3-150">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="06ef3-150">Select **New**.</span></span>
3. <span data-ttu-id="06ef3-151">Í reitinn **Heiti valmyndaratriðis** skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="06ef3-151">In the **Menu item name** field, type a value.</span></span>
4. <span data-ttu-id="06ef3-152">Í reitinn **Titill** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="06ef3-152">In the **Title** field, type a value.</span></span>
5. <span data-ttu-id="06ef3-153">Í reitnum **Hamur** velurðu valkost.</span><span class="sxs-lookup"><span data-stu-id="06ef3-153">In the **Mode** field, select an option.</span></span>
6. <span data-ttu-id="06ef3-154">Velja skal **Já** í reitnum **Nota fyrirliggjandi vinnu**.</span><span class="sxs-lookup"><span data-stu-id="06ef3-154">Select **Yes** in the **Use existing work** field.</span></span>
7. <span data-ttu-id="06ef3-155">Velja skal **Já** í reitnum **Mynda númeraplötu**.</span><span class="sxs-lookup"><span data-stu-id="06ef3-155">Select **Yes** in the **Generate license plate** field.</span></span>
8. <span data-ttu-id="06ef3-156">Útvíkkaðu hlutann **Vinnuklasar**.</span><span class="sxs-lookup"><span data-stu-id="06ef3-156">Expand the **Work classes** section.</span></span>
9. <span data-ttu-id="06ef3-157">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="06ef3-157">Select **New**.</span></span>
10. <span data-ttu-id="06ef3-158">Í reitinn **Kenni vinnuklasa** skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="06ef3-158">In the **Work class ID** field, type a value.</span></span>
11. <span data-ttu-id="06ef3-159">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="06ef3-159">Select **Save**.</span></span>
12. <span data-ttu-id="06ef3-160">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="06ef3-160">Close the page.</span></span>
13. <span data-ttu-id="06ef3-161">Farðu í **skoðunarrúðuna > Kerfiseiningar > Vöruhúsakerfi > Uppsetning > Fartæki > Valmynd fartækis**.</span><span class="sxs-lookup"><span data-stu-id="06ef3-161">Go to **navigation pane > Modules > Warehouse management > Setup > Mobile device > Mobile device menu**.</span></span>
14. <span data-ttu-id="06ef3-162">Í trénu, skal velja þau valmyndaratriði sem voru stofnuð áður.</span><span class="sxs-lookup"><span data-stu-id="06ef3-162">In the tree, select the menu item that you created before.</span></span>
15. <span data-ttu-id="06ef3-163">Veljið **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="06ef3-163">Select **Edit**.</span></span>
16. <span data-ttu-id="06ef3-164">Veldu örina til að bæta valmyndaratriði við valmyndina.</span><span class="sxs-lookup"><span data-stu-id="06ef3-164">Select the arrow to add the menu item to the menu.</span></span>
17. <span data-ttu-id="06ef3-165">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="06ef3-165">Select **Save**.</span></span>
18. <span data-ttu-id="06ef3-166">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="06ef3-166">Close the page.</span></span>

## <a name="update-a-work-template"></a><span data-ttu-id="06ef3-167">Uppfæra sniðmát verks</span><span class="sxs-lookup"><span data-stu-id="06ef3-167">Update a work template</span></span>
1. <span data-ttu-id="06ef3-168">Farðu í **Skoðunarrúðu > Kerfi > Vöruhúsakerfi > Uppsetning > Vinna > Vinnusniðmát**.</span><span class="sxs-lookup"><span data-stu-id="06ef3-168">Go to **Navigation pane > Modules > Warehouse management > Setup > Work > Work templates**.</span></span>
2. <span data-ttu-id="06ef3-169">Veljið **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="06ef3-169">Select **Edit**.</span></span>
3. <span data-ttu-id="06ef3-170">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="06ef3-170">Select **New**.</span></span>
4. <span data-ttu-id="06ef3-171">Í reitnum **Gerð vinnu** skal velja **Prenta**.</span><span class="sxs-lookup"><span data-stu-id="06ef3-171">In the **Work type** field, select **Print**.</span></span>
5. <span data-ttu-id="06ef3-172">Í reitnum **Kenni vinnuklasa** skal færa inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="06ef3-172">In the **Work class ID** field, enter or select a value.</span></span>
6. <span data-ttu-id="06ef3-173">Veldu **Færa upp**.</span><span class="sxs-lookup"><span data-stu-id="06ef3-173">Select **Move up**.</span></span>
7. <span data-ttu-id="06ef3-174">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="06ef3-174">Select **Save**.</span></span>
8. <span data-ttu-id="06ef3-175">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="06ef3-175">Close the page.</span></span>

