---
title: Gæðaskoðun
description: Þetta efnisatriði veitir upplýsingar um eiginleika gæðastjórnunar. Þessi eiginleiki gerir starfsmönnum vöruhúss kleift að gera stuttar skoðanir á staðnum á meðan þeir taka á móti vörum á svæði innhliðs.
author: mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: c270426a228ac58652f1f60d6fe99d4886071fa6
ms.sourcegitcommit: 4a981ee4be6d7e6c0e55541535d386bce2565cba
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/27/2020
ms.locfileid: "3621439"
---
# <a name="quality-check"></a><span data-ttu-id="a455a-104">Gæðaskoðun</span><span class="sxs-lookup"><span data-stu-id="a455a-104">Quality check</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a455a-105">Eiginleikinn *Gæðaskoðun* gerir starfsmönnum vöruhúss kleift að gera flýtiskoðanir á staðnum á meðan þeir taka á móti vörum á svæði innhliðs.</span><span class="sxs-lookup"><span data-stu-id="a455a-105">The *Quality check* feature lets warehouse workers do quick spot checks for quality while they receive items to the inbound dock area.</span></span> <span data-ttu-id="a455a-106">Þessar skoðanir á staðnum eru gagnlegar þegar starfsmenn skoða pakkningar eða aðra hluta vöru sem auðvelt er að skoða.</span><span class="sxs-lookup"><span data-stu-id="a455a-106">These spot checks are beneficial when workers inspect packaging or other easily recognizable parts of an item.</span></span> <span data-ttu-id="a455a-107">Eiginleikinn biður starfsmenn um að gera stutta skoðun til að sjá hvort eitthvað er augljóslega ekki í lagi eða skemmt áður en birgðunum er komið fyrir á lager í frágangsstaðsetningunni.</span><span class="sxs-lookup"><span data-stu-id="a455a-107">The feature guides workers to take a quick look to see whether anything is obviously faulty or damaged before they stock the inventory in its putaway location.</span></span>

<span data-ttu-id="a455a-108">Þessi eiginleiki getur komið í stað hefðbundins gæðaskoðunarferlis.</span><span class="sxs-lookup"><span data-stu-id="a455a-108">This feature is an alternative to the standard quality check process.</span></span> <span data-ttu-id="a455a-109">Hann býður upp á meiri sveigjanleika og hraðari úrvinnslu.</span><span class="sxs-lookup"><span data-stu-id="a455a-109">It offers more flexibility and faster processing.</span></span>

<span data-ttu-id="a455a-110">Þegar þessi eiginleiki er notaður fer koman og gæðaskoðun fram á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="a455a-110">When you use this feature, the arrival and quality check occur in the following way:</span></span>

1. <span data-ttu-id="a455a-111">Þegar sending kemur, mun starfkraftur í vöruhúsi skrá komuna.</span><span class="sxs-lookup"><span data-stu-id="a455a-111">When a shipment arrives, a warehouse worker registers the arrival.</span></span> <span data-ttu-id="a455a-112">Starfsmaðurinn skannar einnig númeraplötu til að skrá staðsetninguna.</span><span class="sxs-lookup"><span data-stu-id="a455a-112">The worker also scans a license plate to register the location.</span></span>
1. <span data-ttu-id="a455a-113">Starfsmaðurinn gerir stutta gæðaskoðun og skráir niðurstöðuna (stóðst eða stóðst ekki) fyrir þessa númeraplötu.</span><span class="sxs-lookup"><span data-stu-id="a455a-113">The worker does a quick quality check and records the result (pass or fail) for that license plate.</span></span>
1. <span data-ttu-id="a455a-114">Ein af eftirfarandi aðgerðum á sér stað:</span><span class="sxs-lookup"><span data-stu-id="a455a-114">One of the following actions occurs:</span></span>

    - <span data-ttu-id="a455a-115">Ef gæðaskoðunin var í lagi er númeraplatan samþykkt og henni beint á móttökustaðsetningu eins og venjulega.</span><span class="sxs-lookup"><span data-stu-id="a455a-115">If the quality check is passed, the license plate is accepted and guided to a receiving location, as usual.</span></span>
    - <span data-ttu-id="a455a-116">Ef gæðaskoðun var ekki í lagi er númeraplötunni hafnað og fyrirliggjandi frágangsvinna hennar er framsend á aðra staðsetningu til að gangast undir frekara eftirlit.</span><span class="sxs-lookup"><span data-stu-id="a455a-116">If the quality check is failed, the license plate is rejected, and existing putaway work for it is redirected to an alternate location for further inspection.</span></span> <span data-ttu-id="a455a-117">Ný gæðapöntun er stofnuð.</span><span class="sxs-lookup"><span data-stu-id="a455a-117">A new quality order is created.</span></span> <span data-ttu-id="a455a-118">Til að skoða gæðapöntunina sem stofnuð er út frá gæðaskoðuninni sem var ekki í lagi er farið í **Birgðastjórnun \> Reglubundin verk \> Gæðastjórnun \> Gæðapantanir**.</span><span class="sxs-lookup"><span data-stu-id="a455a-118">To view the quality order that is created from the failed quality check, go to **Inventory management \> Periodic tasks \> Quality management \> Quality orders**.</span></span>

<span data-ttu-id="a455a-119">Einnig er hægt að setja þetta ferli upp þannig að allar skannaðar númeraplötur séu fluttar á staðsetningu gæðaskoðunar.</span><span class="sxs-lookup"><span data-stu-id="a455a-119">This process can also be set up so that all scanned license plates are immediately diverted to the quality check location.</span></span>

## <a name="turn-on-the-quality-check-feature"></a><span data-ttu-id="a455a-120">Kveikja á eiginleika gæðaskoðunar</span><span class="sxs-lookup"><span data-stu-id="a455a-120">Turn on the Quality check feature</span></span>

<span data-ttu-id="a455a-121">Áður en hægt er að nota eiginleikann *Gæðaskoðun* verður að vera kveikt á honum í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="a455a-121">Before you can use the *Quality check* feature, it must be turned on in your system.</span></span> <span data-ttu-id="a455a-122">Stjórnendur geta notað stillingarnar [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikt á honum ef þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="a455a-122">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="a455a-123">Á vinnusvæðinu **Eiginleikastjórnun** er eiginleikinn tilgreindur á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="a455a-123">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="a455a-124">**Eining:** *Vöruhúsakerfi*</span><span class="sxs-lookup"><span data-stu-id="a455a-124">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="a455a-125">**Heiti eiginleika:** *Gæðaskoðun*</span><span class="sxs-lookup"><span data-stu-id="a455a-125">**Feature name:** *Quality check*</span></span>

## <a name="set-up-the-feature-for-the-example-scenario"></a><span data-ttu-id="a455a-126">Setja upp eiginleikann fyrir þetta sýnidæmi</span><span class="sxs-lookup"><span data-stu-id="a455a-126">Set up the feature for the example scenario</span></span>

<span data-ttu-id="a455a-127">Í þessum hluta eru leiðbeiningar og dæmi sem sýna hvernig á að setja upp eiginleikann *Gæðaskoðun* og undirbúa sýnigögn fyrir sýnidæmið sem kemur fyrir seinna í þessu efnisatriði.</span><span class="sxs-lookup"><span data-stu-id="a455a-127">This section provides guidelines and an example that shows how to set up the *Quality check* feature and prepare sample data for the example scenario that is provided later in this topic.</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="a455a-128">Gera sýnigögn tiltæk</span><span class="sxs-lookup"><span data-stu-id="a455a-128">Make sample data available</span></span>

<span data-ttu-id="a455a-129">Til að vinna í gegnum [sýniaðstæðurnar](#example-scenario) með því að nota sýnskrárnar og sýnigildin sem eru kynnt í þessu efnisatriði verður þú að vinna á kerfi þar sem venjulegu [sýnigögnin](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) eru sett upp.</span><span class="sxs-lookup"><span data-stu-id="a455a-129">To work through the [example scenario](#example-scenario) by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="a455a-130">Þar að auki verður þú að velja **USMF**-lögaðila áður en þú byrjar.</span><span class="sxs-lookup"><span data-stu-id="a455a-130">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

### <a name="quality-check-template"></a><a name="quality-template"></a><span data-ttu-id="a455a-131">Sniðmát gæðaskoðunar</span><span class="sxs-lookup"><span data-stu-id="a455a-131">Quality check template</span></span>

<span data-ttu-id="a455a-132">Sniðmát gæðaskoðunar skilgreinir reglurnar fyrir gæðaskoðun á staðnum við móttöku.</span><span class="sxs-lookup"><span data-stu-id="a455a-132">The quality check template defines the rules for doing quick spot checks for quality at the time of receiving.</span></span>

1. <span data-ttu-id="a455a-133">Farið í **Vöruhúsakerfi \> Uppsetning \> Vinna \> Sniðmát gæðaskoðunar**.</span><span class="sxs-lookup"><span data-stu-id="a455a-133">Go to **Warehouse management \> Setup \> Work \> Quality check template**.</span></span>
1. <span data-ttu-id="a455a-134">Veljið **Nýtt** til að bæta sniðmáti við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="a455a-134">Select **New** to add a template to the grid.</span></span>
1. <span data-ttu-id="a455a-135">Stillið eftirfarandi gildi til að skilgreina nýja sniðmátið:</span><span class="sxs-lookup"><span data-stu-id="a455a-135">Set the following values to define the new template:</span></span>

    - <span data-ttu-id="a455a-136">**Heiti sniðmáts gæðaskoðunar:** *Móttökuskoðun*</span><span class="sxs-lookup"><span data-stu-id="a455a-136">**Quality check template name:** *Dock check*</span></span>

        <span data-ttu-id="a455a-137">Sláið inn heiti sem auðkennir reglurnar sem eru notaðar fyrir þetta sniðmát.</span><span class="sxs-lookup"><span data-stu-id="a455a-137">Enter a name that identifies the policies applied for this template.</span></span>

    - <span data-ttu-id="a455a-138">**Samþykktarregla:** *Birta notanda kvaðningu*</span><span class="sxs-lookup"><span data-stu-id="a455a-138">**Acceptance policy:** *Prompt user*</span></span>

        <span data-ttu-id="a455a-139">Tilgreinið hvort notendur eigi að fá kvaðningu um að samþykkja eða hafna gæðum birgða meðan þeir vinna verkið eða hvort gæðunum skuli sjálfkrafa hafnað.</span><span class="sxs-lookup"><span data-stu-id="a455a-139">Specify whether users should be prompted to accept or reject the quality of the inventory while they process the work, or whether the quality should automatically be rejected.</span></span> <span data-ttu-id="a455a-140">Tiltækir valmöguleikar eru *Sjálfvirk höfnun* og *Birta notanda kvaðningu*.</span><span class="sxs-lookup"><span data-stu-id="a455a-140">The available options are *Auto reject* and *Prompt user*.</span></span>

    - <span data-ttu-id="a455a-141">**Vinnuregla gæðamála:** *Stofna gæðapöntun*</span><span class="sxs-lookup"><span data-stu-id="a455a-141">**Quality processing policy:** *Create quality order*</span></span>

        <span data-ttu-id="a455a-142">Veljið regluna sem á að nota þegar gæðum birgða er hafnað.</span><span class="sxs-lookup"><span data-stu-id="a455a-142">Select the policy that should be used when the quality of the inventory is rejected.</span></span> <span data-ttu-id="a455a-143">Eftirtaldir valkostir eru í boði:</span><span class="sxs-lookup"><span data-stu-id="a455a-143">The following options are available:</span></span>

        - <span data-ttu-id="a455a-144">*Stofna vinnu eingöngu* – Eingöngu stofna vinnu til að auðvelda birgðahreyfingu.</span><span class="sxs-lookup"><span data-stu-id="a455a-144">*Create work only* – Just create work to facilitate inventory movement.</span></span>
        - <span data-ttu-id="a455a-145">*Stofna gæðapöntun* – Stofna gæðapöntun til að auðvelda gæðaprófanir.</span><span class="sxs-lookup"><span data-stu-id="a455a-145">*Create quality order* – Create a quality order to facilitate quality tests.</span></span>

    - <span data-ttu-id="a455a-146">**Prófunarflokkur:** *Lokað rými*</span><span class="sxs-lookup"><span data-stu-id="a455a-146">**Test group:** *Enclosure*</span></span>

        <span data-ttu-id="a455a-147">Tilgreinið prófunarflokkinn sem á að nota í gæðapöntun sem er stofnuð.</span><span class="sxs-lookup"><span data-stu-id="a455a-147">Specify the test group that should be used in the quality order that is created.</span></span> <span data-ttu-id="a455a-148">Prófunarflokkar eru settir upp í einingunni **Birgðastjórnun**.</span><span class="sxs-lookup"><span data-stu-id="a455a-148">Test groups are set up in the **Inventory management** module.</span></span>

        <span data-ttu-id="a455a-149">Hafið slökkt á valkostinum **Förgunartexti** fyrir prófunarflokkinn.</span><span class="sxs-lookup"><span data-stu-id="a455a-149">Leave the **Destructive text** option turned off for the test group.</span></span> <span data-ttu-id="a455a-150">Þessi valkostur skilgreinir hvort farga skuli sýninu sem hluti af prófunum innan prófunarflokksins.</span><span class="sxs-lookup"><span data-stu-id="a455a-150">This option defines whether the sample will be destroyed as part of the tests in the test group.</span></span> <span data-ttu-id="a455a-151">Ef prófun með förgun er notuð býr kerfið til birgðafærslu þegar gæðapöntun er stofnuð fyrir vöru.</span><span class="sxs-lookup"><span data-stu-id="a455a-151">If a destructive test is used, the system generates an inventory transaction when a quality order is created for an item.</span></span> <span data-ttu-id="a455a-152">Ný birgðafærslu spáir fyrir um birgðalækkun fyrir prófunarmagnið.</span><span class="sxs-lookup"><span data-stu-id="a455a-152">The new inventory transaction predicts the inventory reduction for the test quantity.</span></span> <span data-ttu-id="a455a-153">Birgðaminnkun á sér stað þegar gæðapöntun lýkur í gegnum staðfestingarskrefið.</span><span class="sxs-lookup"><span data-stu-id="a455a-153">The inventory reduction occurs when the quality order is completed through the validation step.</span></span> <span data-ttu-id="a455a-154">Birgðafærslan er auðkennd sem gæðapöntun.</span><span class="sxs-lookup"><span data-stu-id="a455a-154">The inventory transaction is identified as a quality order.</span></span>

### <a name="work-class--quality-check"></a><a name="work-class"></a><span data-ttu-id="a455a-155">Vinnuklasi – Gæðaskoðun</span><span class="sxs-lookup"><span data-stu-id="a455a-155">Work class – Quality check</span></span>

<span data-ttu-id="a455a-156">Vinnuklasar eru notaðir til að beina og/eða takmarka gerð vinnupöntunarlína sem starfskraftur í vöruhúsi getur unnið í farsíma.</span><span class="sxs-lookup"><span data-stu-id="a455a-156">Work classes are used to direct and/or limit the type of work order lines that warehouse workers can process on a mobile device.</span></span>

1. <span data-ttu-id="a455a-157">Fara í **Vöruhúsastjórnun \> Uppsetning \> Vinna \> Vinnuklasar**.</span><span class="sxs-lookup"><span data-stu-id="a455a-157">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="a455a-158">Veljið **Nýr** til að búa til vinnuklasa.</span><span class="sxs-lookup"><span data-stu-id="a455a-158">Select **New** to create a work class.</span></span>
1. <span data-ttu-id="a455a-159">Stilla eftirfarandi gildi í hausnum:</span><span class="sxs-lookup"><span data-stu-id="a455a-159">In the header, set the following values:</span></span>

    - <span data-ttu-id="a455a-160">**Auðkenni vinnuklasa:** *Gæðaeftirlit*</span><span class="sxs-lookup"><span data-stu-id="a455a-160">**Work class ID:** *QC Check*</span></span>

        <span data-ttu-id="a455a-161">Sláið inn heiti sem auðkennir vinnuklasann.</span><span class="sxs-lookup"><span data-stu-id="a455a-161">Enter a name that identifies the work class.</span></span>

    - <span data-ttu-id="a455a-162">**Lýsing:** *Gæðaeftirlit*</span><span class="sxs-lookup"><span data-stu-id="a455a-162">**Description:** *QC Check*</span></span>

        <span data-ttu-id="a455a-163">Færið inn stutta lýsingu sem gefur til kynna hvað vinnuklasinn er notaður fyrir.</span><span class="sxs-lookup"><span data-stu-id="a455a-163">Enter a short description that indicates what the work class is used for.</span></span>

    - <span data-ttu-id="a455a-164">**Gerð verkbeiðni:** *Gæði í gæðaskoðun*</span><span class="sxs-lookup"><span data-stu-id="a455a-164">**Work order type:** *Quality in quality check*</span></span>

        <span data-ttu-id="a455a-165">Veljið gerð verkbeiðni sem vinnuklasinn stofnar.</span><span class="sxs-lookup"><span data-stu-id="a455a-165">Select the type of work order that is created by the work class.</span></span> <span data-ttu-id="a455a-166">Þegar gæðastjórnunarvinna er sett upp skal alltaf velja *Gæði í gæðaskoðun*.</span><span class="sxs-lookup"><span data-stu-id="a455a-166">When you set up quality control work, always select *Quality in quality check*.</span></span>

1. <span data-ttu-id="a455a-167">Í flýtiflipanum **Gildar gerðir frágangsstaðsetningar** skal skilja reitinn **Gerð staðsetningar** eftir auðan.</span><span class="sxs-lookup"><span data-stu-id="a455a-167">On the **Valid put location types** FastTab, leave the **Location type** field blank.</span></span>

    <span data-ttu-id="a455a-168">Ef valin er staðsetningargerð, eru staðsetningarnar takmarkaðar þar sem hægt er að setja vörur eftir að þær hafa verið tíndar.</span><span class="sxs-lookup"><span data-stu-id="a455a-168">If you select a location type, you limit the locations where items can be put after they are picked.</span></span> <span data-ttu-id="a455a-169">Þessi reitur er notaður þegar staðsetningarleiðbeiningar reynir að leysa úr staðsetningu, eða ef starfsmaður vöruhússins tilgreinir staðsetningu handvirkt fyrir valmyndaratriði fartækis.</span><span class="sxs-lookup"><span data-stu-id="a455a-169">This field is used when a location directive tries to resolve the location, or when a warehouse worker manually specifies the location for the mobile device menu item.</span></span>

<span data-ttu-id="a455a-170">Frekari upplýsingar um vinnuklasa og hvernig á að stofna þá er að finna í [Stofna vinnuklasa](tasks/create-work-class.md).</span><span class="sxs-lookup"><span data-stu-id="a455a-170">For more information about work classes and how to create them, see [Create a work class](tasks/create-work-class.md).</span></span>

### <a name="work-template"></a><span data-ttu-id="a455a-171">Vinnusniðmát</span><span class="sxs-lookup"><span data-stu-id="a455a-171">Work template</span></span>

<span data-ttu-id="a455a-172">Vinnusniðmát gerir það mögulegt að skilgreina vinnsluaðgerðir sem þarf að framkvæma í vöruhúsinu.</span><span class="sxs-lookup"><span data-stu-id="a455a-172">Work templates let you define the work operations that must be performed in the warehouse.</span></span> <span data-ttu-id="a455a-173">Yfirleitt samanstanda vinnsluaðgerðir vöruhúss af aðgerðarpari: starfsmanns í vöruhúsi tekur til lagerbirgðir á einni staðsetningu og setur síðan tíndu birgðirnar niður á annarri staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="a455a-173">Typically, warehouse work operations consist of a pair of actions: a warehouse worker picks on-hand inventory up in one location and then puts the picked inventory down in another location.</span></span> <span data-ttu-id="a455a-174">Vinnusniðmát fyrir gæðastjórnun skilgreinir vinnuaðgerðir fyrir athugun á gæðum.</span><span class="sxs-lookup"><span data-stu-id="a455a-174">A work template for quality control defines the work operations for doing quality checks.</span></span>

#### <a name="purchase-orders"></a><span data-ttu-id="a455a-175">Innkaupapantanir</span><span class="sxs-lookup"><span data-stu-id="a455a-175">Purchase orders</span></span>

1. <span data-ttu-id="a455a-176">Farðu í **Vöruhúsakerfi \> Uppsetning \> Vinna \> Vinnusniðmát**.</span><span class="sxs-lookup"><span data-stu-id="a455a-176">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="a455a-177">Í hausnum skal stilla reitinn **Gerð verkbeiðni** á *Innkaupapantanir*.</span><span class="sxs-lookup"><span data-stu-id="a455a-177">In the header, set the **Work order type** field to *Purchase orders*.</span></span>
1. <span data-ttu-id="a455a-178">Á aðgerðarúðunni skal velja **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="a455a-178">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="a455a-179">Veljið vinnusniðmát sem á að innihalda skref gæðaskoðunar.</span><span class="sxs-lookup"><span data-stu-id="a455a-179">Select a work template that should include a quality check step.</span></span> <span data-ttu-id="a455a-180">Í hlutanum **Yfirlit**, í reitnum **Vinnusniðmát**, skal velja *51 Innhreyfing innkaupapöntunar*.</span><span class="sxs-lookup"><span data-stu-id="a455a-180">In the **Overview** section, in the **Work template** field, select *51 PO Receipt*.</span></span>
1. <span data-ttu-id="a455a-181">Athugið að í hlutanum **Upplýsingar vinnusniðmáts** er hnitanetið með tvær línur fyrir: eina fyrir *Tiltekt* og hina fyrir *Frágang*.</span><span class="sxs-lookup"><span data-stu-id="a455a-181">In the **Work template details** section, notice that the grid has two existing lines: one for *Pick* and one for *Put*.</span></span>
1. <span data-ttu-id="a455a-182">Í hlutanum **Upplýsingar vinnusniðmáts** skal velja **Ný** til að bæta línu fyrir gæðastjórnun við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="a455a-182">In the **Work template details** section, select **New** to add a row for quality control to the grid.</span></span> <span data-ttu-id="a455a-183">Takið eftir að reiturinn **Línunúmer** fyrir nýju línuna er stilltur á *3*.</span><span class="sxs-lookup"><span data-stu-id="a455a-183">Notice that the **Line number** field for the new line is set to *3*.</span></span>
1. <span data-ttu-id="a455a-184">Stilltu eftirfarandi gildi á nýju línunni.</span><span class="sxs-lookup"><span data-stu-id="a455a-184">On the new line, set the following values.</span></span> <span data-ttu-id="a455a-185">Samþykkið sjálfgefin gildi fyrir reitina sem eftir eru.</span><span class="sxs-lookup"><span data-stu-id="a455a-185">Accept the default values for the remaining fields.</span></span>

    - <span data-ttu-id="a455a-186">**Vinnugerð:** *Gæðaskoðun*</span><span class="sxs-lookup"><span data-stu-id="a455a-186">**Work type:** *Quality check*</span></span>
    - <span data-ttu-id="a455a-187">**Auðkenni vinnuklasa:** *Innkaup*</span><span class="sxs-lookup"><span data-stu-id="a455a-187">**Work class ID:** *Purchase*</span></span>
    - <span data-ttu-id="a455a-188">**Heiti sniðmáts gæðaskoðunar:** *Móttökuskoðun*</span><span class="sxs-lookup"><span data-stu-id="a455a-188">**Quality check template name:** *Dock check*</span></span>

        <span data-ttu-id="a455a-189">Veljið einkvæmt auðkenni fyrir vinnuklasann.</span><span class="sxs-lookup"><span data-stu-id="a455a-189">Select the unique ID for the work class.</span></span> <span data-ttu-id="a455a-190">Nota þetta gildi til að skilgreina valmyndaratriðin á fartækið og gerðir vinnu sem hægt er að vinna þessar valmyndaratriði.</span><span class="sxs-lookup"><span data-stu-id="a455a-190">You use this value to configure the menu items on the mobile device and the types of work that those menu items can process.</span></span>

1. <span data-ttu-id="a455a-191">Á aðgerðasvæðinu skal velja **Vista** til að vista vinnuna sem er komin.</span><span class="sxs-lookup"><span data-stu-id="a455a-191">On the Action Pane, select **Save** to save your work so far.</span></span>

    <span data-ttu-id="a455a-192">Upplýsingaboð birtast þar sem stendur: „Ógilt - Gæðaskoðun verður að koma strax á eftir tiltekt.“</span><span class="sxs-lookup"><span data-stu-id="a455a-192">You receive an informational message that states, "Invalid - Quality check must come directly after a pick."</span></span> <span data-ttu-id="a455a-193">Þess vegna þarf að breyta gildinu fyrir **Línunúmer** fyrir línuna sem var bætt við.</span><span class="sxs-lookup"><span data-stu-id="a455a-193">Therefore, you must change the **Line number** value for the line that you just added.</span></span>

1. <span data-ttu-id="a455a-194">Fylgið þessum skrefum til að breyta gildinu fyrir **Línunúmer** fyrir nýju línuna:</span><span class="sxs-lookup"><span data-stu-id="a455a-194">Follow these steps to change the **Line number** value for the new line:</span></span>

    1. <span data-ttu-id="a455a-195">Í hlutanum **Upplýsingar vinnusniðmáts** skal velja línuna þar sem reiturinn **Vinnugerð** er stilltur á *Gæðaskoðun*.</span><span class="sxs-lookup"><span data-stu-id="a455a-195">In the **Work template details** section, select the line where the **Work type** field is set to *Quality check*.</span></span>
    2. <span data-ttu-id="a455a-196">Veljið hnappinn **Færa upp** eða **Færa niður** til að færa línuna *Gæðaskoðun* þannig að hún komi á eftir línu *Tiltektar*.</span><span class="sxs-lookup"><span data-stu-id="a455a-196">Select the **Move up** or **Move down** button to move the *Quality check* line so that it's after the *Pick* line.</span></span>

1. <span data-ttu-id="a455a-197">Í aðgerðarúðunni skal velja **Vista**.</span><span class="sxs-lookup"><span data-stu-id="a455a-197">On the Action Pane, select **Save**.</span></span>

#### <a name="quality-in-quality-check"></a><span data-ttu-id="a455a-198">Gæði í gæðaskoðun</span><span class="sxs-lookup"><span data-stu-id="a455a-198">Quality in quality check</span></span>

<span data-ttu-id="a455a-199">Næst skal stofna vinnusniðmát fyrir gæðaskoðun.</span><span class="sxs-lookup"><span data-stu-id="a455a-199">Next, create a work template for the quality check.</span></span>

1. <span data-ttu-id="a455a-200">Í haus síðunnar **Vinnusniðmát** skal breyta gildinu í reitnum **Gerð verkbeiðni** í *Gæði í gæðaskoðun*.</span><span class="sxs-lookup"><span data-stu-id="a455a-200">In the header of the **Work templates** page, change the value of the **Work order type** field to *Quality in quality check*.</span></span>
1. <span data-ttu-id="a455a-201">Á aðgerðasvæðinu skal velja **Ný** til að bæta línu við hnitanetið í hlutanum **Yfirlit**.</span><span class="sxs-lookup"><span data-stu-id="a455a-201">On the Action Pane, select **New** to add a row to the grid in the **Overview** section.</span></span>
1. <span data-ttu-id="a455a-202">Í nýju línunni skal stilla eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="a455a-202">In the new row, set the following values:</span></span>

    - <span data-ttu-id="a455a-203">**Vinnusniðmát:** *51 Gæðaskoðun*</span><span class="sxs-lookup"><span data-stu-id="a455a-203">**Work template:** *51 Quality Check*</span></span>

        <span data-ttu-id="a455a-204">Færa skal inn heiti á sniðmátið.</span><span class="sxs-lookup"><span data-stu-id="a455a-204">Enter a name for the template.</span></span>

    - <span data-ttu-id="a455a-205">**Lýsing á vinnusniðmáti:** *51 Gæðaskoðun*</span><span class="sxs-lookup"><span data-stu-id="a455a-205">**Work template description:** *51 Quality Check*</span></span>

1. <span data-ttu-id="a455a-206">Á aðgerðasvæðinu skal velja **Vista** til að gera hlutann **Upplýsingar um vinnusniðmát** tiltækan.</span><span class="sxs-lookup"><span data-stu-id="a455a-206">On the Action Pane, select **Save** to make the **Work template details** section available.</span></span>
1. <span data-ttu-id="a455a-207">Á meðan nýja sniðmátið er enn valið í hlutanum **Yfirlit**, skal velja **Ný** í hlutanum **Upplýsingar um vinnusniðmát** til að bæta línu við hnitanetið þar.</span><span class="sxs-lookup"><span data-stu-id="a455a-207">While the new template is still selected in the **Overview** section, select **New** in the **Work template details** section to add a row to the grid there.</span></span>
1. <span data-ttu-id="a455a-208">Í nýju línunni skal stilla eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="a455a-208">In the new row, set the following values:</span></span>

    - <span data-ttu-id="a455a-209">**Verkgerð:** *Tiltekt*</span><span class="sxs-lookup"><span data-stu-id="a455a-209">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="a455a-210">**Auðkenni vinnuklasa:** *Gæðaeftirlit*</span><span class="sxs-lookup"><span data-stu-id="a455a-210">**Work class ID:** *QC Check*</span></span>

        <span data-ttu-id="a455a-211">Veljið heiti [vinnuklasans](#work-class) sem var stofnaður hér á undan fyrir vinnu gæðastjórnunar.</span><span class="sxs-lookup"><span data-stu-id="a455a-211">Select the name of the [work class](#work-class) that you created earlier for quality control work.</span></span>

1. <span data-ttu-id="a455a-212">Í hlutanum **Upplýsingar um vinnusniðmát** skal aftur velja **Ný** til að bæta við annarri línu.</span><span class="sxs-lookup"><span data-stu-id="a455a-212">In the **Work template details** section, select **New** again to add another row.</span></span>
1. <span data-ttu-id="a455a-213">Í nýju línunni skal stilla eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="a455a-213">In the new row, set the following values:</span></span>

    - <span data-ttu-id="a455a-214">**Tegund vinnu:** *Frágangur*</span><span class="sxs-lookup"><span data-stu-id="a455a-214">**Work type:** *Put*</span></span>
    - <span data-ttu-id="a455a-215">**Auðkenni vinnuklasa:** *Gæðaeftirlit*</span><span class="sxs-lookup"><span data-stu-id="a455a-215">**Work class ID:** *QC Check*</span></span>

        <span data-ttu-id="a455a-216">Veljið heiti [vinnuklasans](#work-class) sem var stofnaður hér á undan fyrir vinnu gæðastjórnunar.</span><span class="sxs-lookup"><span data-stu-id="a455a-216">Select the name of the [work class](#work-class) that you created earlier for quality control work.</span></span>

1. <span data-ttu-id="a455a-217">Í aðgerðarúðunni skal velja **Vista**.</span><span class="sxs-lookup"><span data-stu-id="a455a-217">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="a455a-218">Frekari upplýsingar um vinnusniðmát er að finna í [Stýra vöruhúsavinnu með vinnusniðmátum og staðsetningarleiðbeiningum](control-warehouse-location-directives.md)</span><span class="sxs-lookup"><span data-stu-id="a455a-218">For more information about work templates, see [Control warehouse work by using work templates and location directives](control-warehouse-location-directives.md)</span></span>

### <a name="location-directive--quality-failures"></a><span data-ttu-id="a455a-219">Staðsetningarleiðbeining – Stenst ekki gæði</span><span class="sxs-lookup"><span data-stu-id="a455a-219">Location directive – Quality failures</span></span>

<span data-ttu-id="a455a-220">Staðsetningarleiðbeiningar eru reglur sem hjálpa við auðkenningu tiltektar- og frágangsstaðsetninga fyrir birgðahreyfingar.</span><span class="sxs-lookup"><span data-stu-id="a455a-220">Location directives are rules that help identify pick and put locations for inventory movement.</span></span> <span data-ttu-id="a455a-221">Til dæmis, í sölupöntunarfærslu, ákvarða staðsetningarleiðbeiningar hvar vörurnar verða teknar til og hvar tilteknar vörur verða að setja.</span><span class="sxs-lookup"><span data-stu-id="a455a-221">For example, in a sales order transaction, a location directive determines where the items will be picked and where the picked items will be put.</span></span> <span data-ttu-id="a455a-222">Setja þarf á reglu staðsetningarleiðbeiningar til að skilgreina hvernig meðhöndla á það sem stenst ekki gæðaskoðun.</span><span class="sxs-lookup"><span data-stu-id="a455a-222">You must configure a location directive rule to define how failed quality checks will be handled.</span></span>

1. <span data-ttu-id="a455a-223">Fara í **Vöruhúsakerfi \> Uppsetning \> Staðsetningarleiðbeiningar**.</span><span class="sxs-lookup"><span data-stu-id="a455a-223">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="a455a-224">Á svæðinu vinstra megin skal stilla reitinn **Gerð verkbeiðni** á *Innkaupapantanir* til að vinna með staðsetningarleiðbeiningar af þeirri gerð.</span><span class="sxs-lookup"><span data-stu-id="a455a-224">In the left pane, set the **Work order type** field to *Purchase orders* to work with location directives of that type.</span></span>
1. <span data-ttu-id="a455a-225">Á aðgerðasvæðinu skal velja **Ný** til að búa til staðsetningarleiðbeiningu fyrir gæðaskoðanir.</span><span class="sxs-lookup"><span data-stu-id="a455a-225">On the Action Pane, select **New** to create a location directive for quality checks.</span></span>
1. <span data-ttu-id="a455a-226">Stilla eftirfarandi gildi í hausnum:</span><span class="sxs-lookup"><span data-stu-id="a455a-226">In the header, set the following values:</span></span>

    - <span data-ttu-id="a455a-227">**Raðnúmer:** Samþykkja sjálfgildið.</span><span class="sxs-lookup"><span data-stu-id="a455a-227">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="a455a-228">**Heiti:** *51 til gæðaskoðunar*</span><span class="sxs-lookup"><span data-stu-id="a455a-228">**Name:** *51 To Quality*</span></span>

1. <span data-ttu-id="a455a-229">Stilltu eftirfarandi gildi á flýtiflipanum **staðsetningarleiðbeiningar**.</span><span class="sxs-lookup"><span data-stu-id="a455a-229">On the **Location directives** FastTab, set the following values.</span></span> <span data-ttu-id="a455a-230">Samþykkið sjálfgefin gildi fyrir reitina sem eftir eru.</span><span class="sxs-lookup"><span data-stu-id="a455a-230">Accept the default values for the remaining fields.</span></span>

    - <span data-ttu-id="a455a-231">**Tegund vinnu:** *Frágangur*</span><span class="sxs-lookup"><span data-stu-id="a455a-231">**Work type:** *Put*</span></span>
    - <span data-ttu-id="a455a-232">**Svæði:** *5*</span><span class="sxs-lookup"><span data-stu-id="a455a-232">**Site:** *5*</span></span>
    - <span data-ttu-id="a455a-233">**Vöruhús:** *51*</span><span class="sxs-lookup"><span data-stu-id="a455a-233">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="a455a-234">Í aðgerðasvæðinu skal velja **Vista** til að vista leiðbeininguna og gera flýtiflipann **Línur** tiltækan.</span><span class="sxs-lookup"><span data-stu-id="a455a-234">On the Action Pane select **Save** to save your directive and make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="a455a-235">Á flýtiflipanum **Línur** velur þú **Ný** til að bæta línu við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="a455a-235">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="a455a-236">Stilltu eftirfarandi gildi á nýju línunni.</span><span class="sxs-lookup"><span data-stu-id="a455a-236">On the new line, set the following values.</span></span> <span data-ttu-id="a455a-237">Samþykkið sjálfgefin gildi fyrir reitina sem eftir eru.</span><span class="sxs-lookup"><span data-stu-id="a455a-237">Accept the default values for the remaining fields.</span></span>

    - <span data-ttu-id="a455a-238">**Frá-magn:** *1*</span><span class="sxs-lookup"><span data-stu-id="a455a-238">**From quantity:** *1*</span></span>
    - <span data-ttu-id="a455a-239">**Til magn:** *1000000*</span><span class="sxs-lookup"><span data-stu-id="a455a-239">**To quantity:** *1000000*</span></span>

1. <span data-ttu-id="a455a-240">Á aðgerðasvæðinu skal velja **Vista** til að vista nýju línuna og gera flýtiflipann **Aðgerðir í staðsetningarleiðbeiningum** tiltækan.</span><span class="sxs-lookup"><span data-stu-id="a455a-240">On the Action Pane, select **Save** to save the new line and make the **Location directive actions** FastTab available.</span></span>
1. <span data-ttu-id="a455a-241">Á meðan nýja línan er enn valin í flýtiflipanum **Línur**, skal velja **Ný** í flýtiflipanum **Aðgerðir í staðsetningarleiðbeiningum** til að bæta línu við hnitanetið þar, þannig að hægt sé að setja upp aðgerð fyrir línuna.</span><span class="sxs-lookup"><span data-stu-id="a455a-241">While the new line is still selected on the **Lines** FastTab, select **New** on the **Location directive actions** FastTab to add a row to the grid there, so that you can set up an action for the line.</span></span>
1. <span data-ttu-id="a455a-242">Í nýju línunni skal stilla reitinn **Heiti** á *Gæði*.</span><span class="sxs-lookup"><span data-stu-id="a455a-242">In the new row, set the **Name** field to *Quality*.</span></span> <span data-ttu-id="a455a-243">Samþykkið sjálfgefin gildi fyrir reitina sem eftir eru.</span><span class="sxs-lookup"><span data-stu-id="a455a-243">Accept the default values for the remaining fields.</span></span>
1. <span data-ttu-id="a455a-244">Á aðgerðasvæðinu skal velja **Vista** til að gera hnappinn **Breyta fyrirspurn** í flýtiflipanum **Aðgerðir í staðsetningarleiðbeiningum** tiltækan.</span><span class="sxs-lookup"><span data-stu-id="a455a-244">On the Action Pane, select **Save** to make the **Edit query** button on the **Location directive actions** FastTab available.</span></span>
1. <span data-ttu-id="a455a-245">Á meðan línan sem var bætt við er enn valin í flýtiflipanum **Aðgerðir í staðsetningarleiðbeiningum**, skal velja **Breyta fyrirspurn** til að opna svarglugga þar sem hægt er að breyta fyrirspurninni fyrir aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="a455a-245">While the line that you just added is still selected on the **Location directive actions** FastTab, select **Edit query** to open a dialog box where you can edit the query for the action.</span></span>
1. <span data-ttu-id="a455a-246">Í flipanum **Svið** skal velja **Bæta við** til að bæta línu við fyrirspurnina.</span><span class="sxs-lookup"><span data-stu-id="a455a-246">On the **Range** tab, select **Add** to add a row to the query.</span></span>
1. <span data-ttu-id="a455a-247">Í nýju línunni skal stilla eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="a455a-247">In the new row, set the following values:</span></span>

    - <span data-ttu-id="a455a-248">**Tafla:** *Staðir*</span><span class="sxs-lookup"><span data-stu-id="a455a-248">**Table:** *Locations*</span></span>
    - <span data-ttu-id="a455a-249">**Afleidd tafla:** *Staðsetningar*</span><span class="sxs-lookup"><span data-stu-id="a455a-249">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="a455a-250">**Svæði:** *Staðsetning*</span><span class="sxs-lookup"><span data-stu-id="a455a-250">**Field:** *Location*</span></span>
    - <span data-ttu-id="a455a-251">**Skilyrði:** *QMS*</span><span class="sxs-lookup"><span data-stu-id="a455a-251">**Criteria:** *QMS*</span></span>

    <span data-ttu-id="a455a-252">Staðsetning *QMS* er vöruhúsastaðsetning fyrir gæði.</span><span class="sxs-lookup"><span data-stu-id="a455a-252">The *QMS* location is a warehouse location for quality.</span></span>

1. <span data-ttu-id="a455a-253">Veldu **Í lagi** til að loka svarglugganum.</span><span class="sxs-lookup"><span data-stu-id="a455a-253">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="a455a-254">Nú þarf að breyta röðinni á staðsetningarleiðbeiningum innkaupapöntunar fyrir vöruhús *51*.</span><span class="sxs-lookup"><span data-stu-id="a455a-254">You must now change the sequence of purchase order location directives for warehouse *51*.</span></span> <span data-ttu-id="a455a-255">Vistið nýju staðsetningarleiðbeininguna *51 Til gæðaskoðunar*, uppfærið síðuna, og veljið staðsetningarleiðbeininguna í listanum.</span><span class="sxs-lookup"><span data-stu-id="a455a-255">Save the new *51 To Quality* location directive, refresh the page, and select the location directive in the list.</span></span> <span data-ttu-id="a455a-256">Notið síðan hnappana **Færa upp** og **Færa niður** á aðgerðasvæðinu til að ganga frá staðsetningarleiðbeiningunni fyrir vöruhús *51* í eftirfarandi röð.</span><span class="sxs-lookup"><span data-stu-id="a455a-256">Then use the **Move up** and **Move down** buttons on the Action Pane to put the location directive for warehouse *51* in the following order.</span></span> <span data-ttu-id="a455a-257">(Áður en valið er **Færa upp** eða **Færa niður** þarf að velja staðsetningarleiðbeiningu í listanum.)</span><span class="sxs-lookup"><span data-stu-id="a455a-257">(Before you select **Move up** or **Move down**, you must select a location directive in the list.)</span></span>

    1. <span data-ttu-id="a455a-258">51 Til gæðaskoðunar</span><span class="sxs-lookup"><span data-stu-id="a455a-258">51 To Quality</span></span>
    2. <span data-ttu-id="a455a-259">51 PO Direct</span><span class="sxs-lookup"><span data-stu-id="a455a-259">51 PO Direct</span></span>
    3. <span data-ttu-id="a455a-260">51 QMS</span><span class="sxs-lookup"><span data-stu-id="a455a-260">51 QMS</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="a455a-261">Valmyndaratriði fartækis</span><span class="sxs-lookup"><span data-stu-id="a455a-261">Mobile device menu items</span></span>

<span data-ttu-id="a455a-262">Skilgreinið valmyndaratriði þannig að fartæki geti framkvæmt aðgerðina **Gæðaskoðun**.</span><span class="sxs-lookup"><span data-stu-id="a455a-262">Configure a menu item so that mobile devices can perform the **Quality Check** function.</span></span>

#### <a name="purchase-putaway"></a><span data-ttu-id="a455a-263">Frágangur innkaupa</span><span class="sxs-lookup"><span data-stu-id="a455a-263">Purchase putaway</span></span>

1. <span data-ttu-id="a455a-264">Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmyndaratriði fartækis**.</span><span class="sxs-lookup"><span data-stu-id="a455a-264">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="a455a-265">Í listanum skal velja valmyndaratriðið **Frágangur innkaupa**.</span><span class="sxs-lookup"><span data-stu-id="a455a-265">In the list, select the **Purchase put-away** menu item.</span></span>
1. <span data-ttu-id="a455a-266">Á aðgerðarúðunni skal velja **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="a455a-266">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="a455a-267">Í hlutanum **Vinnuklasar** skal velja **Ný** til að bæta línu við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="a455a-267">In the **Work classes** section, select **New** to add a row to the grid.</span></span>
1. <span data-ttu-id="a455a-268">Í nýju línunni skal stilla eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="a455a-268">In the new row, set the following values:</span></span>

    - <span data-ttu-id="a455a-269">**Auðkenni vinnuklasa:** *Gæðaeftirlit*</span><span class="sxs-lookup"><span data-stu-id="a455a-269">**Work class ID:** *QC Check*</span></span>

        <span data-ttu-id="a455a-270">Færið inn heiti [vinnuklasans](#work-class) sem var stofnaður hér á undan fyrir vinnu gæðastjórnunar.</span><span class="sxs-lookup"><span data-stu-id="a455a-270">Enter the name of the [work class](#work-class) that you created earlier for quality control work.</span></span>

    - <span data-ttu-id="a455a-271">**Gerð verkbeiðni:** *Gæði í gæðaskoðun*</span><span class="sxs-lookup"><span data-stu-id="a455a-271">**Work order type:** *Quality in quality check*</span></span>

1. <span data-ttu-id="a455a-272">Í aðgerðarúðunni skal velja **Vista**.</span><span class="sxs-lookup"><span data-stu-id="a455a-272">On the Action Pane, select **Save**.</span></span>

#### <a name="purchase-order-line-receiving"></a><span data-ttu-id="a455a-273">Móttaka innkaupapöntunarlínu</span><span class="sxs-lookup"><span data-stu-id="a455a-273">Purchase order line receiving</span></span>

1. <span data-ttu-id="a455a-274">Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmyndaratriði fartækis**.</span><span class="sxs-lookup"><span data-stu-id="a455a-274">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="a455a-275">Í aðgerðarúðunni velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="a455a-275">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="a455a-276">Stilla eftirfarandi gildi í hausnum:</span><span class="sxs-lookup"><span data-stu-id="a455a-276">In the header, set the following values:</span></span>

    - <span data-ttu-id="a455a-277">**Heiti valmyndaratriðis:** *Móttaka innkaupapöntunarlínu*</span><span class="sxs-lookup"><span data-stu-id="a455a-277">**Menu item name:** *PO line receiving*</span></span>
    - <span data-ttu-id="a455a-278">**Titill:** *Móttaka innkaupapöntunarlínu*</span><span class="sxs-lookup"><span data-stu-id="a455a-278">**Title:** *PO line receiving*</span></span>
    - <span data-ttu-id="a455a-279">**Máti:** *Vinna*</span><span class="sxs-lookup"><span data-stu-id="a455a-279">**Mode:** *Work*</span></span>
    - <span data-ttu-id="a455a-280">**Nota fyrirliggjandi vinnu:** *Nei*</span><span class="sxs-lookup"><span data-stu-id="a455a-280">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="a455a-281">Stilltu eftirfarandi gildi á flýtiflipanum **Almennt**.</span><span class="sxs-lookup"><span data-stu-id="a455a-281">On the **General** FastTab, set the following values.</span></span> <span data-ttu-id="a455a-282">Samþykkið sjálfgefin gildi fyrir reitina sem eftir eru.</span><span class="sxs-lookup"><span data-stu-id="a455a-282">Accept the default values for the remaining fields.</span></span>

    - <span data-ttu-id="a455a-283">**Stofnunarferli vinnu:** *Móttaka og frágangur innkaupapöntunarlínu*</span><span class="sxs-lookup"><span data-stu-id="a455a-283">**Work creation process:** *Purchase order line receiving and put away*</span></span>
    - <span data-ttu-id="a455a-284">**Mynda númeraplötu:** *Já*</span><span class="sxs-lookup"><span data-stu-id="a455a-284">**Generate license plate:** *Yes*</span></span>
    - <span data-ttu-id="a455a-285">**Vinnusniðmát:** *51 Innhreyfing innkaupapöntunar*</span><span class="sxs-lookup"><span data-stu-id="a455a-285">**Work template:** *51 PO Receipt*</span></span>

1. <span data-ttu-id="a455a-286">Í aðgerðarúðunni skal velja **Vista**.</span><span class="sxs-lookup"><span data-stu-id="a455a-286">On the Action Pane, select **Save**.</span></span>

#### <a name="add-the-menu-item-to-a-mobile-device-menu"></a><span data-ttu-id="a455a-287">Bæta valmyndaratriði við valmynd fartækis</span><span class="sxs-lookup"><span data-stu-id="a455a-287">Add the menu item to a mobile device menu</span></span>

1. <span data-ttu-id="a455a-288">Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmynd fartækis**.</span><span class="sxs-lookup"><span data-stu-id="a455a-288">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="a455a-289">Á svæðinu vinstra megin skal velja valmyndina **Á innleið**.</span><span class="sxs-lookup"><span data-stu-id="a455a-289">In the left pane, select the **Inbound** menu.</span></span>
1. <span data-ttu-id="a455a-290">Á aðgerðarúðunni skal velja **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="a455a-290">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="a455a-291">Í dálknum **Tiltækar valmyndir og valmyndaratriði** skal velja nýja valmyndaratriðið **Móttaka innkaupapöntunarlínu**.</span><span class="sxs-lookup"><span data-stu-id="a455a-291">In the **Available menus and menu items** column, select the new **PO line receiving** menu item.</span></span>
1. <span data-ttu-id="a455a-292">Smellið á hægri örvarhnappinn til að færa **Móttaka innkaupapöntunarlínu** yfir í dálkinn **Valmyndarskipan**.</span><span class="sxs-lookup"><span data-stu-id="a455a-292">Select the right arrow button to move **PO line receiving** to the **Menu structure** column.</span></span>
1. <span data-ttu-id="a455a-293">Í dálknum **Valmyndaskipan** skal velja **Móttaka innkaupapöntunarlínu** og síðan velja uppörina eða niðurörina til að færa valmyndaratriðið á æskilega staðsetningu í valmynd fartækisins.</span><span class="sxs-lookup"><span data-stu-id="a455a-293">In the **Menu structure** column, select **PO line receiving**, and then select the up arrow or down arrow button to move the menu item to the desired position on the mobile device menu.</span></span>
1. <span data-ttu-id="a455a-294">Í aðgerðarúðunni skal velja **Vista**.</span><span class="sxs-lookup"><span data-stu-id="a455a-294">On the Action Pane, select **Save**.</span></span>

## <a name="example-scenario"></a><a name="example-scenario"></a><span data-ttu-id="a455a-295">Dæmi</span><span class="sxs-lookup"><span data-stu-id="a455a-295">Example scenario</span></span>

<span data-ttu-id="a455a-296">Þegar búið er að gera öll sýnigögnin hér á undan tiltæk og setja þau upp, er hægt að fara í gegnum þetta sýnidæmi til að prófa eiginleikann *Gæðaskoðun*.</span><span class="sxs-lookup"><span data-stu-id="a455a-296">After you've made all the previously described sample data available and set it up, you can work through this scenario to try out the *Quality check* feature.</span></span> <span data-ttu-id="a455a-297">Gildin sem eru sýnd í þessu sýnidæmi gera ráð fyrir því að verið sé að vinna með stöðluð sýnigögn, að lögaðilinn **USMF** hafi verið valinn og að sýniskrárnar sem lýst var fyrr í þessu efnisatriði hafi verið undirbúnar.</span><span class="sxs-lookup"><span data-stu-id="a455a-297">The values that are shown in this scenario assume that you're working with the standard demo data, that you selected the **USMF** legal entity, and that you prepared the sample records that are described earlier in this topic.</span></span> <span data-ttu-id="a455a-298">Þetta sýnidæmi er einnig dæmi um hvernig hægt er að nota eiginleikann í framleiðsluumhverfi.</span><span class="sxs-lookup"><span data-stu-id="a455a-298">This scenario also serves as an example that shows how the feature can be used in a production setting.</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="a455a-299">Stofna innkaupapöntun</span><span class="sxs-lookup"><span data-stu-id="a455a-299">Create a purchase order</span></span>

1. <span data-ttu-id="a455a-300">Farðu í **Innkaup og aðföng \> Innkaupapantanir \> Allar innkaupapantanir**.</span><span class="sxs-lookup"><span data-stu-id="a455a-300">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="a455a-301">Í aðgerðarúðunni velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="a455a-301">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="a455a-302">Sláðu inn eftirfarandi gildi í svarglugganum **Búa til innkaupapöntun**:</span><span class="sxs-lookup"><span data-stu-id="a455a-302">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="a455a-303">**Lánardrottnalykill:** *104*</span><span class="sxs-lookup"><span data-stu-id="a455a-303">**Vendor account:** *104*</span></span>
    - <span data-ttu-id="a455a-304">**Vöruhús:** *51*</span><span class="sxs-lookup"><span data-stu-id="a455a-304">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="a455a-305">Veljið **Í lagi** til að loka svarglugganum og opnið nýju innkaupapöntunina.</span><span class="sxs-lookup"><span data-stu-id="a455a-305">Select **OK** to close the dialog box and open the new purchase order.</span></span>
1. <span data-ttu-id="a455a-306">Í flýtiflipanum **Innkaupapöntunarlínur** inniheldur hnitanetið nýja, auða línu.</span><span class="sxs-lookup"><span data-stu-id="a455a-306">On the **Purchase order lines** FastTab, the grid contains a new, blank line.</span></span> <span data-ttu-id="a455a-307">Stilltu eftirfarandi gildi á þessari línu:</span><span class="sxs-lookup"><span data-stu-id="a455a-307">On this line, set the following values:</span></span>

    - <span data-ttu-id="a455a-308">**Vörunúmer:** *M9203*</span><span class="sxs-lookup"><span data-stu-id="a455a-308">**Item number:** *M9203*</span></span>
    - <span data-ttu-id="a455a-309">**Magn:** *3*</span><span class="sxs-lookup"><span data-stu-id="a455a-309">**Quantity:** *3*</span></span>
    - <span data-ttu-id="a455a-310">**Eining:** *VÖRUBRETTI*</span><span class="sxs-lookup"><span data-stu-id="a455a-310">**Unit:** *PL*</span></span>

1. <span data-ttu-id="a455a-311">Í aðgerðarúðunni skal velja **Vista**.</span><span class="sxs-lookup"><span data-stu-id="a455a-311">On the Action Pane, select **Save**.</span></span>

### <a name="process-quality-check-receiving"></a><span data-ttu-id="a455a-312">Vinna úr gæðaskoðun móttöku</span><span class="sxs-lookup"><span data-stu-id="a455a-312">Process quality check receiving</span></span>

<span data-ttu-id="a455a-313">Þegar innkaupapöntunin hefur verið stofnuð er hægt að taka á móti henni með því að nota valmyndaratriðið **Móttaka innkaupapöntunarlínu** og virknina fyrir eiginleikann *Gæðaskoðun*.</span><span class="sxs-lookup"><span data-stu-id="a455a-313">After the purchase order has been created, it can be received by using the **PO line receiving** menu item and the functionality of the *Quality check* feature.</span></span>

#### <a name="receive-pallet-1"></a><span data-ttu-id="a455a-314">Móttaka vörubrettis 1</span><span class="sxs-lookup"><span data-stu-id="a455a-314">Receive pallet 1</span></span>

1. <span data-ttu-id="a455a-315">Skráðu þig inn í vöruhúsaforritið sem notandi fyrir vöruhús *51*.</span><span class="sxs-lookup"><span data-stu-id="a455a-315">Sign in to the warehouse app as a user for warehouse *51*.</span></span> <span data-ttu-id="a455a-316">(Sláið inn *51* sem notandakennið og *1* sem aðgangsorðið.)</span><span class="sxs-lookup"><span data-stu-id="a455a-316">(Enter *51* as the user ID and *1* as the password.)</span></span>
1. <span data-ttu-id="a455a-317">Farið í **Á innleið \> móttaka innkaupapöntunarlínu**.</span><span class="sxs-lookup"><span data-stu-id="a455a-317">Go to **Inbound \> PO line receiving**.</span></span>
1. <span data-ttu-id="a455a-318">Í reitinn **PONUM** skal slá inn innkaupapöntunarnúmerið.</span><span class="sxs-lookup"><span data-stu-id="a455a-318">In the **PONUM** field, enter the purchase order number.</span></span>
1. <span data-ttu-id="a455a-319">Staðfestið innkaupapöntunarnúmerið.</span><span class="sxs-lookup"><span data-stu-id="a455a-319">Confirm the purchase order number.</span></span>
1. <span data-ttu-id="a455a-320">Í reitinn **LINENUM** skal slá inn fjölda innkaupapöntunarlína sem tekið er á móti.</span><span class="sxs-lookup"><span data-stu-id="a455a-320">In the **LINENUM** field, enter the number of the purchase order line that is being received.</span></span> <span data-ttu-id="a455a-321">Þar sem pöntunin er aðeins með eina línu í þessu sýnidæmi, skal slá inn *1* í reitinn **LINENUM** fyrir hvert móttökuskref.</span><span class="sxs-lookup"><span data-stu-id="a455a-321">Because the order has only one line in this scenario, you will enter *1* in the **LINENUM** field for each receiving step.</span></span>
1. <span data-ttu-id="a455a-322">Staðfestið línunúmerið.</span><span class="sxs-lookup"><span data-stu-id="a455a-322">Confirm the line number.</span></span>
1. <span data-ttu-id="a455a-323">Í reitinn **Magn** skal slá inn magnið sem á að móttaka.</span><span class="sxs-lookup"><span data-stu-id="a455a-323">In the **QTY** field, enter the quantity to receive.</span></span> <span data-ttu-id="a455a-324">Þar sem innkaupapöntunin er fyrir þrjú bretti (*PL*) í þessu sýnidæmi og það eru þrjú móttökuskref, skal slá inn *1* í reitinn **Magn** fyrir hvert móttökuskref.</span><span class="sxs-lookup"><span data-stu-id="a455a-324">Because the purchase order is for three pallets (*PL*) in this scenario, and there are three receiving steps, you will enter *1* in the **QTY** field for each receiving step.</span></span>
1. <span data-ttu-id="a455a-325">Staðfestu magnið.</span><span class="sxs-lookup"><span data-stu-id="a455a-325">Confirm the quantity.</span></span>

    <span data-ttu-id="a455a-326">Síðan **Gæðaskoðun** sem birtist er með enga innsláttarreiti.</span><span class="sxs-lookup"><span data-stu-id="a455a-326">The **Quality check** page that appears has no entry fields.</span></span> <span data-ttu-id="a455a-327">Hún er aðeins með staðfestingarhnappinn (gátmerki) neðst og valmyndarhnappinn (**≡**) efst.</span><span class="sxs-lookup"><span data-stu-id="a455a-327">It has only the confirmation (check mark) button at the bottom and the Menu button (**≡**) at the top.</span></span> <span data-ttu-id="a455a-328">(Valmyndarhnappurinn er stundum kallaður hamborgari eða hamborgarahnappur.) Til að flýta fyrir gæðaskoðunarferlinu, þegar brettið stenst gæðaskoðun, staðfestir notandinn bara síðuna **Gæðaskoðun**.</span><span class="sxs-lookup"><span data-stu-id="a455a-328">(The Menu button is sometimes referred to as the hamburger or the hamburger button.) To expedite the quality check process, when the pallet passes the quality check, the user just confirms the **Quality check** page.</span></span>

    <span data-ttu-id="a455a-329">![Gæðaskoðunarsíða](media/quality-check.png "Gæðaskoðunarsíða")</span><span class="sxs-lookup"><span data-stu-id="a455a-329">![Quality check page](media/quality-check.png "Quality check page")</span></span>

1. <span data-ttu-id="a455a-330">Veljið staðfestingarhnappinn til að samþykkja gæðaskoðun fyrir bretti 1 úr línu 1.</span><span class="sxs-lookup"><span data-stu-id="a455a-330">Select the confirmation button to pass the quality check for pallet 1 from line 1.</span></span>

    <span data-ttu-id="a455a-331">Síðan **Innkaupapantanir: Frágangur** sem birtist sýnir upplýsingar um frágangsvinnuna:</span><span class="sxs-lookup"><span data-stu-id="a455a-331">The **Purchase orders: Put** page that appears shows details of the put work:</span></span>

    - <span data-ttu-id="a455a-332">**STAÐ:** Staðsetning sem kerfið ákveður</span><span class="sxs-lookup"><span data-stu-id="a455a-332">**LOC:** The system determined location</span></span>

        <span data-ttu-id="a455a-333">Þessi staðsetning er útnefnd frágangsstaðsetning fyrir móttöku innkaupapöntunar.</span><span class="sxs-lookup"><span data-stu-id="a455a-333">This location is the designated putaway location for purchase order receiving.</span></span>

    - <span data-ttu-id="a455a-334">**NP:** Kenni númeraplötu sem kerfið býr til</span><span class="sxs-lookup"><span data-stu-id="a455a-334">**LP:** The system-generated License plate ID</span></span>
    - <span data-ttu-id="a455a-335">**Vara:** *M9203*</span><span class="sxs-lookup"><span data-stu-id="a455a-335">**Item:** *M9203*</span></span>
    - <span data-ttu-id="a455a-336">**Magn:** *1 NP: 100 ea*</span><span class="sxs-lookup"><span data-stu-id="a455a-336">**Qty:** *1 PL: 100 ea*</span></span>

    <span data-ttu-id="a455a-337">Vörulýsingin er einnig sýnd.</span><span class="sxs-lookup"><span data-stu-id="a455a-337">The item description is also shown.</span></span>

1. <span data-ttu-id="a455a-338">Staðfestið frágangsvinnuna.</span><span class="sxs-lookup"><span data-stu-id="a455a-338">Confirm the putaway work.</span></span>

    <span data-ttu-id="a455a-339">Á síðunni **Verk** fyrir móttöku innkaupapöntunarlínu birtast skilaboðin „Vinnu lokið“.</span><span class="sxs-lookup"><span data-stu-id="a455a-339">On the **Task** page for purchase order line receiving, you receive a "Work Completed" message.</span></span> <span data-ttu-id="a455a-340">Reiturinn **LINENUM** er tiltækur þannig að hægt sé að taka á móti næsta bretti.</span><span class="sxs-lookup"><span data-stu-id="a455a-340">The **LINENUM** field is available so that you can start to receive the next pallet.</span></span>

#### <a name="receive-pallet-2"></a><span data-ttu-id="a455a-341">Móttaka vörubrettis 2</span><span class="sxs-lookup"><span data-stu-id="a455a-341">Receive pallet 2</span></span>

<span data-ttu-id="a455a-342">Í þessu sýnidæmi verður bretti 2 hafnað.</span><span class="sxs-lookup"><span data-stu-id="a455a-342">For this scenario, pallet 2 will be rejected.</span></span>

1. <span data-ttu-id="a455a-343">Í reitinn **LINENUM** skal slá inn *1* og staðfesta línunúmerið.</span><span class="sxs-lookup"><span data-stu-id="a455a-343">In the **LINENUM** field, enter *1*, and confirm the line number.</span></span>
1. <span data-ttu-id="a455a-344">Reiturinn **Magn** er nú tiltækur.</span><span class="sxs-lookup"><span data-stu-id="a455a-344">The **QTY** field is now available.</span></span> <span data-ttu-id="a455a-345">Sláið inn *1* og staðfestið magnið.</span><span class="sxs-lookup"><span data-stu-id="a455a-345">Enter *1*, and confirm the quantity.</span></span>

    <span data-ttu-id="a455a-346">Síðan **Gæðaskoðun** birtist.</span><span class="sxs-lookup"><span data-stu-id="a455a-346">The **Quality check** page appears.</span></span> <span data-ttu-id="a455a-347">Fyrir þessa innhreyfingu verður brettinu hafnað vegna gæða og því komið fyrir á gæðastaðsetningunni *QMS*.</span><span class="sxs-lookup"><span data-stu-id="a455a-347">For this receipt, the pallet will be rejected for quality, and it will be put into the *QMS* quality location.</span></span>

1. <span data-ttu-id="a455a-348">Veljið valmyndarhnappinn (**≡**) efst á síðunni og síðan, í valmyndinni, skal velja **Hafna**.</span><span class="sxs-lookup"><span data-stu-id="a455a-348">Select the Menu button (**≡**) at the top of the page, and then, on the menu, select **Reject**.</span></span>
1. <span data-ttu-id="a455a-349">Á síðunni **Verk** sem birtist skal slá inn **QMS** sem staðsetningu *Frágangs* þar sem senda á brettið til að gangast undir frekara eftirlit.</span><span class="sxs-lookup"><span data-stu-id="a455a-349">On the **Task** page that appears, enter **QMS** as the *Put* location to send the pallet to for further inspection.</span></span>

    <span data-ttu-id="a455a-350">Síðan **Gæði í gæðaskoðun: Frágangur** sem birtist sýnir upplýsingar um frágangsvinnuna:</span><span class="sxs-lookup"><span data-stu-id="a455a-350">The **Quality in quality check: Put** page that appears shows details of the put work:</span></span>

    - <span data-ttu-id="a455a-351">**STAÐ:** *QMS*</span><span class="sxs-lookup"><span data-stu-id="a455a-351">**LOC:** *QMS*</span></span>

        <span data-ttu-id="a455a-352">Þessi staðsetning er útnefnd frágangsstaðsetning fyrir móttöku á því sem gæðaskoðun hafnar.</span><span class="sxs-lookup"><span data-stu-id="a455a-352">This location is the designated putaway location for rejected quality receiving.</span></span>

    - <span data-ttu-id="a455a-353">**NP:** Kenni númeraplötu sem kerfið býr til</span><span class="sxs-lookup"><span data-stu-id="a455a-353">**LP:** The system-generated License plate ID</span></span>
    - <span data-ttu-id="a455a-354">**Vara:** *M9203*</span><span class="sxs-lookup"><span data-stu-id="a455a-354">**Item:** *M9203*</span></span>
    - <span data-ttu-id="a455a-355">**Magn:** *1 NP: 100 ea*</span><span class="sxs-lookup"><span data-stu-id="a455a-355">**Qty:** *1 PL: 100 ea*</span></span>

    <span data-ttu-id="a455a-356">Vörulýsingin er einnig sýnd.</span><span class="sxs-lookup"><span data-stu-id="a455a-356">The item description is also shown.</span></span>

1. <span data-ttu-id="a455a-357">Staðfestið frágangsvinnuna.</span><span class="sxs-lookup"><span data-stu-id="a455a-357">Confirm the putaway work.</span></span>

    <span data-ttu-id="a455a-358">Á síðunni **Verk** fyrir móttöku innkaupapöntunarlínu birtast skilaboðin „Vinnu lokið“.</span><span class="sxs-lookup"><span data-stu-id="a455a-358">On the **Task** page for purchase order line receiving, you receive a "Work Completed" message.</span></span> <span data-ttu-id="a455a-359">Reiturinn **LINENUM** er tiltækur þannig að hægt sé að taka á móti næsta bretti.</span><span class="sxs-lookup"><span data-stu-id="a455a-359">The **LINENUM** field is available so that you can start to receive the next pallet.</span></span>

<span data-ttu-id="a455a-360">Gæðaskoðuninni hefur nú verið lokið og gæðapöntun stofnuð fyrir hafnaða brettið.</span><span class="sxs-lookup"><span data-stu-id="a455a-360">You've now completed the quality check and created a quality order for the rejected pallet.</span></span> <span data-ttu-id="a455a-361">Til að skoða pöntuina sem var stofnuð skal fara í **Birgðastjórnun \> Reglubundin verk \> Gæðastjórnun \> Gæðapantanir**.</span><span class="sxs-lookup"><span data-stu-id="a455a-361">To view the order that was created, go to **Inventory management \> Periodic tasks \> Quality management \> Quality orders**.</span></span>

<span data-ttu-id="a455a-362">Nú er hægt að vinna úr prófun gæðapöntunar.</span><span class="sxs-lookup"><span data-stu-id="a455a-362">Quality order testing can now be processed.</span></span> <span data-ttu-id="a455a-363">Ekki er fjallað um gæðaprófun í þessu efnisatriði.</span><span class="sxs-lookup"><span data-stu-id="a455a-363">Quality testing isn't covered in this topic.</span></span>

<span data-ttu-id="a455a-364">Frekari upplýsingar um gæðastjórnun má finna í [Gæðastjórnunaryfirlit](../inventory/enable-quality-management.md)</span><span class="sxs-lookup"><span data-stu-id="a455a-364">For more information about quality management, see [Quality management overview](../inventory/enable-quality-management.md)</span></span>

#### <a name="receive-pallet-3"></a><span data-ttu-id="a455a-365">Móttaka vörubrettis 3</span><span class="sxs-lookup"><span data-stu-id="a455a-365">Receive pallet 3</span></span>

<span data-ttu-id="a455a-366">Í þessu sýnidæmi verður bretti 3 samþykkt.</span><span class="sxs-lookup"><span data-stu-id="a455a-366">For this scenario, pallet 3 will be accepted.</span></span>

1. <span data-ttu-id="a455a-367">Í reitinn **LINENUM** skal slá inn *1* og staðfesta línunúmerið.</span><span class="sxs-lookup"><span data-stu-id="a455a-367">In the **LINENUM** field, enter *1*, and confirm the line number.</span></span>
1. <span data-ttu-id="a455a-368">Reiturinn **Magn** er nú tiltækur.</span><span class="sxs-lookup"><span data-stu-id="a455a-368">The **QTY** field is now available.</span></span> <span data-ttu-id="a455a-369">Sláið inn *1* og staðfestið magnið.</span><span class="sxs-lookup"><span data-stu-id="a455a-369">Enter *1*, and confirm the quantity.</span></span>

    <span data-ttu-id="a455a-370">Síðan **Gæðaskoðun** birtist.</span><span class="sxs-lookup"><span data-stu-id="a455a-370">The **Quality check** page appears.</span></span> <span data-ttu-id="a455a-371">Fyrir þessa innhreyfingu verður brettið samþykkt í gæðaskoðun og því komið fyrir magnstaðsetningu frágangs.</span><span class="sxs-lookup"><span data-stu-id="a455a-371">For this receipt, the pallet will be accepted for quality, and it will be put into a bulk putaway location.</span></span>

1. <span data-ttu-id="a455a-372">Veljið staðfestingarhnappinn til að samþykkja gæðaskoðun.</span><span class="sxs-lookup"><span data-stu-id="a455a-372">Select the confirmation button to pass the quality check.</span></span>

    <span data-ttu-id="a455a-373">Síðan **Innkaupapantanir: Frágangur** sem birtist sýnir upplýsingar um frágangsvinnuna:</span><span class="sxs-lookup"><span data-stu-id="a455a-373">The **Purchase orders: Put** page that appears shows details of the put work:</span></span>

    - <span data-ttu-id="a455a-374">**STAÐ:** Staðsetning sem kerfið ákveður</span><span class="sxs-lookup"><span data-stu-id="a455a-374">**LOC:** The system determined location</span></span>

        <span data-ttu-id="a455a-375">Þessi staðsetning er útnefnd frágangsstaðsetning fyrir móttöku innkaupapöntunar.</span><span class="sxs-lookup"><span data-stu-id="a455a-375">This location is the designated putaway location for purchase order receiving.</span></span>

    - <span data-ttu-id="a455a-376">**NP:** Kenni númeraplötu sem kerfið býr til</span><span class="sxs-lookup"><span data-stu-id="a455a-376">**LP:** The system-generated License plate ID</span></span>
    - <span data-ttu-id="a455a-377">**Vara:** *M9203*</span><span class="sxs-lookup"><span data-stu-id="a455a-377">**Item:** *M9203*</span></span>
    - <span data-ttu-id="a455a-378">**Magn:** *1 NP: 100 ea*</span><span class="sxs-lookup"><span data-stu-id="a455a-378">**Qty:** *1 PL: 100 ea*</span></span>

    <span data-ttu-id="a455a-379">Vörulýsingin er einnig sýnd.</span><span class="sxs-lookup"><span data-stu-id="a455a-379">The item description is also shown.</span></span>

1. <span data-ttu-id="a455a-380">Staðfestið frágangsvinnuna.</span><span class="sxs-lookup"><span data-stu-id="a455a-380">Confirm the putaway work.</span></span>

    <span data-ttu-id="a455a-381">Á síðunni **Verk** fyrir móttöku innkaupapöntunarlínu birtast skilaboðin „Vinnu lokið“.</span><span class="sxs-lookup"><span data-stu-id="a455a-381">On the **Task** page for purchase order line receiving, you receive a "Work Completed" message.</span></span> <span data-ttu-id="a455a-382">Reiturinn **LINENUM** er tiltækur þannig að hægt sé að taka á móti næsta bretti.</span><span class="sxs-lookup"><span data-stu-id="a455a-382">The **LINENUM** field is available so that you can start to receive the next pallet.</span></span>

1. <span data-ttu-id="a455a-383">Veljið valmyndarhnappinn (**≡**) efst á síðunni og síðan, í valmyndinni, skal velja **Hætta við** til að fara aftur í valmyndina.</span><span class="sxs-lookup"><span data-stu-id="a455a-383">Select the Menu button (**≡**) at the top of the page, and then, on the menu, select **Cancel** to return to the menu.</span></span>

<span data-ttu-id="a455a-384">Nú má loka fartækjaforritinu.</span><span class="sxs-lookup"><span data-stu-id="a455a-384">You can now close the mobile app.</span></span>
