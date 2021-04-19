---
title: Skipta vinnu
description: Þetta efnisatriði veitir upplýsingar um virkni vinnuskiptingar. Þessi virkni gerir þér kleift að skipta stórum verkbeiðnum niður í nokkrar smærri verkbeiðnir sem síðan er hægt að úthluta á marga vöruhúsastarfskrafta. Á þennan hátt er hægt að velja sömu vinnu samtímis af nokkrum starfskröftum í vöruhúsi.
author: mirzaab
ms.date: 10/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: WHSWorkTableListPage
ms.author: mirzaab
ms.search.validFrom: 2020-10-15
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: eae1e722a7c4d819cbca398eb14a2b36fa04eec5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830763"
---
# <a name="work-split"></a><span data-ttu-id="94322-105">Skipta vinnu</span><span class="sxs-lookup"><span data-stu-id="94322-105">Work split</span></span>

<span data-ttu-id="94322-106">Virkni vinnuskiptingar gerir þér kleift að skipta stórum vinnukennum (þ.e. verkbeiðnum sem eru með margar línur) niður í nokkur smærri vinnukenni sem síðan er hægt að úthluta á marga vöruhúsastarfskrafta.</span><span class="sxs-lookup"><span data-stu-id="94322-106">Work split functionality lets you split large work IDs (that is, work orders that have several lines) into several smaller work IDs that you can then assign to multiple warehouse workers.</span></span> <span data-ttu-id="94322-107">Á þennan hátt er hægt að velja sama stofnnúmer vinnu samtímis af nokkrum starfskröftum í vöruhúsi.</span><span class="sxs-lookup"><span data-stu-id="94322-107">In this way, the same work creation number can be picked simultaneously by several warehouse workers.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="94322-108">Aðeins er hægt að skipta verkbeiðnum sem eru með stöðuna *Opin* eða *Í gangi*.</span><span class="sxs-lookup"><span data-stu-id="94322-108">You can split only work orders that have a status of *Open* or *In-progress*.</span></span>

## <a name="turn-on-the-work-split-functionality"></a><span data-ttu-id="94322-109">Kveikja á virkni vinnuskiptingar</span><span class="sxs-lookup"><span data-stu-id="94322-109">Turn on the work split functionality</span></span>

<span data-ttu-id="94322-110">Áður en hægt er að nota virkni vinnuskiptingar þarf að kveikja á eiginleikanum og eiginleika forsendanna í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="94322-110">Before you can use the work split functionality, you must turn on the feature and its prerequisite feature in your system.</span></span> <span data-ttu-id="94322-111">Stjórnendur geta notað stillingar [eiginleikastjórnunar](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikanna og kveikja á þeim ef þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="94322-111">Administrators can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the features and turn them on as required.</span></span>

<span data-ttu-id="94322-112">Fyrst skal kveikja á forsendueiginleikanum *Vinnulokun fyrir allt fyrirtækið* ef ekki er nú þegar kveikt á honum.</span><span class="sxs-lookup"><span data-stu-id="94322-112">First, turn on the prerequisite *Organization-wide work blocking* feature if it isn't already turned on.</span></span> <span data-ttu-id="94322-113">Í vinnusvæðinu **Stjórnun eiginleika** er þessi eiginleiki skráður á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="94322-113">In the **Feature management** workspace, this feature is listed in the following way:</span></span>

- <span data-ttu-id="94322-114">**Eining:** *Vöruhúsakerfi*</span><span class="sxs-lookup"><span data-stu-id="94322-114">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="94322-115">**Heiti eiginleika:** *Vinnulokun fyrir allt fyrirtækið*</span><span class="sxs-lookup"><span data-stu-id="94322-115">**Feature name:** *Organization-wide work blocking*</span></span>

> [!NOTE]
> <span data-ttu-id="94322-116">Þegar þessi eiginleiki er virkjaður er gagnauppfærsla sjálfkrafa notuð þegar búið er að kveikja á eiginleikann yfir alla lögaðila.</span><span class="sxs-lookup"><span data-stu-id="94322-116">When this feature is activated, a data upgrade is automatically applied after the feature is turned on across all legal entities.</span></span>

<span data-ttu-id="94322-117">Næst er kveikt á eiginleikanum *Skipta verki* sem er sýndur á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="94322-117">Next, turn on the *Work split* feature, which is listed in the following way:</span></span>

- <span data-ttu-id="94322-118">**Eining:** *Vöruhúsakerfi*</span><span class="sxs-lookup"><span data-stu-id="94322-118">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="94322-119">**Heiti eiginleika:** *Skipta verki*</span><span class="sxs-lookup"><span data-stu-id="94322-119">**Feature name:** *Work split*</span></span>

## <a name="enhancements-to-the-work-details-and-all-work-pages"></a><span data-ttu-id="94322-120">Viðbætur á síðum verkupplýsinga og öllum verkum</span><span class="sxs-lookup"><span data-stu-id="94322-120">Enhancements to the Work details and All work pages</span></span>

<span data-ttu-id="94322-121">Eiginleikinn *Skipta verki* bætir eftirfarandi tveimur hnöppum við flipann **Verk** á aðgerðasvæðinu á síðunum **Upplýsingar um verk** og **Öll verk**:</span><span class="sxs-lookup"><span data-stu-id="94322-121">The *Work split* feature adds the following two buttons to the **Work** tab on the Action Pane of the **Work details** and **All work** pages:</span></span>

- <span data-ttu-id="94322-122">**Skipta verki** – Skipta núverandi vinnukenni niður í mörg smærri vinnukenni sem mismunandi starfskraftar geta unnið úr.</span><span class="sxs-lookup"><span data-stu-id="94322-122">**Split work** – Split the current work ID into multiple smaller work IDs that can be processed by separate workers.</span></span>
- <span data-ttu-id="94322-123">**Hætta við lotu verkskiptingar** - Hættir við lotu verkskiptingar og gerir verk tiltækt fyrir úrvinnslu.</span><span class="sxs-lookup"><span data-stu-id="94322-123">**Cancel work split session** – Cancel the work split session, and make the work available for processing.</span></span>

<span data-ttu-id="94322-124">![Hnappar fyrir Skipta verki og Hætta við lotu verkskiptingar](media/Work_split_buttons.png "Hnappar fyrir Skipta verki og Hætta við lotu verkskiptingar")</span><span class="sxs-lookup"><span data-stu-id="94322-124">![Split work and Cancel work split session buttons](media/Work_split_buttons.png "Split work and Cancel work split session buttons")</span></span>

> [!IMPORTANT]
> <span data-ttu-id="94322-125">Hnappurinn **Skipta verki** verður ekki í boði ef einhver eftirfarandi skilyrða eru uppfyllt:</span><span class="sxs-lookup"><span data-stu-id="94322-125">The **Split work** button won't be available if any of the following conditions are met:</span></span>
>
> - <span data-ttu-id="94322-126">Verkstaðan er eitthvað annað en *Opin* eða *Í gangi*.</span><span class="sxs-lookup"><span data-stu-id="94322-126">The work status is something other than *Open* or *In progress*.</span></span>
> - <span data-ttu-id="94322-127">Gámagerðarauðkenni tengist vinnukenninu.</span><span class="sxs-lookup"><span data-stu-id="94322-127">A container ID is associated with the work ID.</span></span> <span data-ttu-id="94322-128">(Ekki er hægt að skipta hólfi kerfisbundið vegna þess að það krefst líkamlegrar aðgerðar.)</span><span class="sxs-lookup"><span data-stu-id="94322-128">(A container can't be systematically split, because it requires physical actions.)</span></span>
> - <span data-ttu-id="94322-129">Vinnan tengist klasa.</span><span class="sxs-lookup"><span data-stu-id="94322-129">The work is associated with a cluster.</span></span>
> - <span data-ttu-id="94322-130">Gerð verkbeiðni er einhver önnur en ein af eftirfarandi gerðum:</span><span class="sxs-lookup"><span data-stu-id="94322-130">The work order type is something other than one of the following types:</span></span>
>
>    - <span data-ttu-id="94322-131">Sölupantanir</span><span class="sxs-lookup"><span data-stu-id="94322-131">Sales orders</span></span>
>    - <span data-ttu-id="94322-132">Tiltekt hráefnis</span><span class="sxs-lookup"><span data-stu-id="94322-132">Raw material picking</span></span>
>    - <span data-ttu-id="94322-133">Flutningsútgáfa</span><span class="sxs-lookup"><span data-stu-id="94322-133">Transfer issue</span></span>
>
> - <span data-ttu-id="94322-134">Annar notandi er að skipta vinnunni.</span><span class="sxs-lookup"><span data-stu-id="94322-134">The work is currently being split by another user.</span></span> <span data-ttu-id="94322-135">Ef reynt er að opna síðu skiptingar fyrir verk sem þegar verið að skipta af hálfu annars notanda, færðu eftirfarandi villuboð: „Verið er að skipta niður vinnu með auðkennið \#\#\#\#.</span><span class="sxs-lookup"><span data-stu-id="94322-135">If you try to open the splitting page for work that is already being split by another user, you receive the following error message: "The work with ID \#\#\#\# is currently being split.</span></span> <span data-ttu-id="94322-136">Reyna skal aftur eftir smástund.</span><span class="sxs-lookup"><span data-stu-id="94322-136">Retry in a few minutes.</span></span> <span data-ttu-id="94322-137">Ef þessi skilaboð halda áfram að birtast skal hafa samband við yfirmann.</span><span class="sxs-lookup"><span data-stu-id="94322-137">If you continue to receive this message, contact a supervisor."</span></span>

<span data-ttu-id="94322-138">Ný ástæða verklokunar, *Skipta verki*, gefur til kynna þegar verið er að skipta niður verkkenninu.</span><span class="sxs-lookup"><span data-stu-id="94322-138">A new work blocking reason, *Split work*, indicates when the work ID is in the process of being split.</span></span> <span data-ttu-id="94322-139">Hún er sýnd bæði á síðunni **Skipta verki** og í farsímaforrit vöruhúsakerfis ef notandi reynir að keyra vinnu.</span><span class="sxs-lookup"><span data-stu-id="94322-139">It's shown both on the **Split work** page and in the Warehouse Management mobile app if a user tries to run the work.</span></span> <span data-ttu-id="94322-140">Þegar lokunarástæður eru notaðar verður heiti reitsins **Lokuð bylgja** fyrir verkkennið breytt í **Lokað fyrir**.</span><span class="sxs-lookup"><span data-stu-id="94322-140">When blocking reasons are used, the name of the **Blocked wave** field from the work ID is changed to **Blocked**.</span></span>

## <a name="initiate-a-work-split"></a><span data-ttu-id="94322-141">Hefja vinnuskipti</span><span class="sxs-lookup"><span data-stu-id="94322-141">Initiate a work split</span></span>

<span data-ttu-id="94322-142">Þessi eiginleiki bætir við nýrri **Skipta vinnu** síðu sem gerir notendum kleift að skipta vinnulínum úr vinnukenninu.</span><span class="sxs-lookup"><span data-stu-id="94322-142">The feature adds a new **Split work** page that lets users split work lines from the work ID.</span></span> <span data-ttu-id="94322-143">Þegar síðan er fyrst opnuð sýnir hún línur sem eru með verkstöðuna *Opin* og eru tiltækar til skiptingar.</span><span class="sxs-lookup"><span data-stu-id="94322-143">When the page is first opened, it shows lines that have a work status of *Open* and that are available to be split.</span></span> <span data-ttu-id="94322-144">Í aðgerðasvæði skal velja **Skipta vinnu** til að skipta valinni vinnu.</span><span class="sxs-lookup"><span data-stu-id="94322-144">On the Action Pane, select **Split work** to process the selected work.</span></span>

<span data-ttu-id="94322-145">Til að skipta vinnu skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="94322-145">To split work, follow these steps.</span></span>

1. <span data-ttu-id="94322-146">Opnið eina af eftirfarandi vinnusíðum:</span><span class="sxs-lookup"><span data-stu-id="94322-146">Open one of the following work pages:</span></span>

    - <span data-ttu-id="94322-147">**Upplýsingar um verk** (**Vöruhúsakerfi \> Verk \> Upplýsingar um verk**)</span><span class="sxs-lookup"><span data-stu-id="94322-147">**Work details** (**Warehouse management \> Work \> Work details**)</span></span>
    - <span data-ttu-id="94322-148">**Öll verk** (**Vöruhúsakerfi \> Verk \> Öll verk**)</span><span class="sxs-lookup"><span data-stu-id="94322-148">**All work** (**Warehouse management \> Work \> All work**)</span></span>

1. <span data-ttu-id="94322-149">Í hnitanetinu skal velja vinnukennið sem á að skipta.</span><span class="sxs-lookup"><span data-stu-id="94322-149">In the grid, select a work ID to split.</span></span> <span data-ttu-id="94322-150">Stilla verður reitinn **Gerð verkbeiðni** á eitt af eftirfarandi gildum:</span><span class="sxs-lookup"><span data-stu-id="94322-150">The **Work order type** field must be set to one of the following values:</span></span>

    - <span data-ttu-id="94322-151">Sölupantanir</span><span class="sxs-lookup"><span data-stu-id="94322-151">Sales orders</span></span>
    - <span data-ttu-id="94322-152">Tiltekt hráefnis</span><span class="sxs-lookup"><span data-stu-id="94322-152">Raw material picking</span></span>
    - <span data-ttu-id="94322-153">Flutningsútgáfa</span><span class="sxs-lookup"><span data-stu-id="94322-153">Transfer issue</span></span>

1. <span data-ttu-id="94322-154">Á aðgerðasvæðinu, í flipanum **Verk**, í flokknum **Verk**, skal velja **Skipta verki**.</span><span class="sxs-lookup"><span data-stu-id="94322-154">On the Action Pane, on the **Work** tab, in the **Work** group, select **Split work**.</span></span>

    <span data-ttu-id="94322-155">Síðan **Skipta verki** opnast og sýnir vinnulínurnar sem eru opnar og má skipta.</span><span class="sxs-lookup"><span data-stu-id="94322-155">The **Split work** page appears and shows the work lines that are open and available to be split.</span></span> <span data-ttu-id="94322-156">Aðeins lausar vinnulínur eru sýndar sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="94322-156">By default, only available work lines are shown.</span></span> <span data-ttu-id="94322-157">Til að skoða allar línur fyrir verkkennið (t.d. línur sem eru af verkgerðinni *Frágangur*) skal velja gátreitinn **Sýna allar línur** fyrir ofan hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="94322-157">To view all lines for the work ID (for example, lines that have a work type of *Put*), select the **Show all lines** check box above the grid.</span></span>

    <span data-ttu-id="94322-158">Eftirfarandi skilaboð birtast: „Notendur geta ekki unnið úr línum fyrir vinnu fyrr en lokið er við skiptingu og þessari síðu er lokað.“</span><span class="sxs-lookup"><span data-stu-id="94322-158">The following message is shown: "Users can't process lines of the work until you finish splitting and close this page."</span></span>

    <span data-ttu-id="94322-159">Reiturinn **Ástæða fyrir vinnulokun** fyrir núverandi vinnu verður stilltur á *Skipta vinnu* og lokað verður fyrir vinnuna.</span><span class="sxs-lookup"><span data-stu-id="94322-159">The **Work blocking reason** field for the current work will be set to *Split work*, and the work will be blocked.</span></span>

    <span data-ttu-id="94322-160">![Ástæða lokunar](media/Blocking_reason.png "Ástæða lokunar")</span><span class="sxs-lookup"><span data-stu-id="94322-160">![Blocking reason](media/Blocking_reason.png "Blocking reason")</span></span>

1. <span data-ttu-id="94322-161">Veljið línurnar sem á að fjarlægja úr núverandi vinnukenni og bætið við nýtt vinnunkenni.</span><span class="sxs-lookup"><span data-stu-id="94322-161">Select the lines to remove from the current work ID and add to a new work ID.</span></span> <span data-ttu-id="94322-162">Eftirfarandi tilvik gerast:</span><span class="sxs-lookup"><span data-stu-id="94322-162">The following events occur:</span></span>

    - <span data-ttu-id="94322-163">Þegar vinnu er skipt er hætt við valda línu eða línur úr upprunalegu vinnukenninu og síðan afritaðar í nýtt vinnukenni.</span><span class="sxs-lookup"><span data-stu-id="94322-163">When you split the work, the selected line or lines from the original work ID are canceled and then copied to a new work ID.</span></span>
    - <span data-ttu-id="94322-164">Fyrirliggjandi skipulag vinnusniðmáts og staðsetningin á fráganginum (og líka tiltektar/frágangsparanir í framtíðinni) er geymt.</span><span class="sxs-lookup"><span data-stu-id="94322-164">The existing work template structure and the location of the put (and also future pick/put pairs) are preserved.</span></span> <span data-ttu-id="94322-165">Gildi fyrir eftirfarandi reiti vinnukennis eru afritaðir úr upprunalegri vinnu og yfir í nýju vinnuna:</span><span class="sxs-lookup"><span data-stu-id="94322-165">Values for the following work ID fields are copied from the original work to the new work:</span></span>

        - <span data-ttu-id="94322-166">Hleðsluauðkenni</span><span class="sxs-lookup"><span data-stu-id="94322-166">Load ID</span></span>
        - <span data-ttu-id="94322-167">Auðkenni sendingar</span><span class="sxs-lookup"><span data-stu-id="94322-167">Shipment ID</span></span>
        - <span data-ttu-id="94322-168">Gerð verkbeiðni</span><span class="sxs-lookup"><span data-stu-id="94322-168">Work order type</span></span>
        - <span data-ttu-id="94322-169">Pöntunarnúmer</span><span class="sxs-lookup"><span data-stu-id="94322-169">Order number</span></span>
        - <span data-ttu-id="94322-170">Vefsvæði</span><span class="sxs-lookup"><span data-stu-id="94322-170">Site</span></span>
        - <span data-ttu-id="94322-171">Vöruhús</span><span class="sxs-lookup"><span data-stu-id="94322-171">Warehouse</span></span>
        - <span data-ttu-id="94322-172">Forgangur vinnu</span><span class="sxs-lookup"><span data-stu-id="94322-172">Work priority</span></span>
        - <span data-ttu-id="94322-173">Auðkenni vinnuhóps</span><span class="sxs-lookup"><span data-stu-id="94322-173">Work pool ID</span></span>
        - <span data-ttu-id="94322-174">Bylgjuauðkenni</span><span class="sxs-lookup"><span data-stu-id="94322-174">Wave ID</span></span>
        - <span data-ttu-id="94322-175">Stofnnúmer vinnu</span><span class="sxs-lookup"><span data-stu-id="94322-175">Work creation number</span></span>

    - <span data-ttu-id="94322-176">Eftirfarandi reitir eru ekki afritaðir í nýja verkkennið:</span><span class="sxs-lookup"><span data-stu-id="94322-176">The following fields aren't copied to the new work ID:</span></span>

        - <span data-ttu-id="94322-177">**Verkkenni** – Nýtt verkkenni er búið til úr tilheyrandi númeraröð.</span><span class="sxs-lookup"><span data-stu-id="94322-177">**Work ID** – A new work ID is generated from the appropriate number sequence.</span></span>
        - <span data-ttu-id="94322-178">**Verkstaða** – Þessi reitur er stilltur á *Opin*.</span><span class="sxs-lookup"><span data-stu-id="94322-178">**Work status** – This field is set to *Open*.</span></span>
        - <span data-ttu-id="94322-179">**Læst af** – Þessi reitur er upphaflega skilinn eftir auður.</span><span class="sxs-lookup"><span data-stu-id="94322-179">**Locked by** – This field is initially set to blank.</span></span>
        - <span data-ttu-id="94322-180">**Auðkenni númeraplötu markmiðs** - Þessi reitur er skilinn eftir auður.</span><span class="sxs-lookup"><span data-stu-id="94322-180">**Target license plate ID** – This field is left blank.</span></span>
        - <span data-ttu-id="94322-181">**Stofnuð dagsetning og tími** - Þessi reitur er stilltur á núverandi dagsetningu og tíma.</span><span class="sxs-lookup"><span data-stu-id="94322-181">**Created date and time** – This field is set to the current date and time.</span></span>
        - <span data-ttu-id="94322-182">**Lokuð bylgja/frosin** - Þessi reitur er endurreiknaður fyrir upprunalega vinnukennið og nýja vinnukennið.</span><span class="sxs-lookup"><span data-stu-id="94322-182">**Blocked wave/frozen** – This field is recomputed for the original work ID and the new work ID.</span></span>

1. <span data-ttu-id="94322-183">Á aðgerðasvæðinu skal velja **Skipta vinnu**.</span><span class="sxs-lookup"><span data-stu-id="94322-183">On the Action Pane, select **Split work**.</span></span>

<span data-ttu-id="94322-184">Meðan verið er að skipta vinnu birtast eftirfarandi skilaboð: „Aðgerð í vinnslu - Skipta vinnu“.</span><span class="sxs-lookup"><span data-stu-id="94322-184">While the work is being split, the following message is shown: "Processing operation - Split work".</span></span> <span data-ttu-id="94322-185">Á meðan þessi skilaboð eru sýnileg er hægt að hætta við aðgerðina með því að velja **Hætta við** í skilaboðaglugganum.</span><span class="sxs-lookup"><span data-stu-id="94322-185">While this message is visible, you can cancel the operation by selecting **Cancel** in the message box.</span></span>

<span data-ttu-id="94322-186">Ef gátreiturinn **Sýna allar línur** er hreinsaður mun línan sem var skipt út og hætt við ekki sjást lengur í hnitanetinu.</span><span class="sxs-lookup"><span data-stu-id="94322-186">If the **Show all lines** check box is cleared, the line that was split off and canceled will no longer appear in the grid.</span></span> <span data-ttu-id="94322-187">Ef gátreiturinn er valinn er hægt að sjá að gildið á reitnum **Verkstaða** fyrir þá línu hefur breyst í *Hætt við*.</span><span class="sxs-lookup"><span data-stu-id="94322-187">If the check box is selected, you should see that the value of the **Work status** field for that line has changed to *Canceled*.</span></span>

<span data-ttu-id="94322-188">Eftirfarandi tilkynning er sýnd til að gefa til kynna að nýja verkkennið hafi verið búið til: „Vinnan \#\#\#\# var stofnuð sem hluti af skiptingu á upprunalegu vinnunni \#\#\#\#.“</span><span class="sxs-lookup"><span data-stu-id="94322-188">The following notification is shown to indicate that the new work ID has been created: "Work \#\#\#\# has been created by splitting off from original work \#\#\#\#."</span></span>

<span data-ttu-id="94322-189">Aðrar vinnulínur úr upprunalega verkkenninu (t.d. línur *Frágangs*) verða aðlagaðar eins og þörf er á til að endurspegla línurnar í vinnunni sem hætt var við.</span><span class="sxs-lookup"><span data-stu-id="94322-189">Other work lines from the original work ID (such as *Put* lines) will be adjusted as required to reflect the lines of work that have been canceled.</span></span> <span data-ttu-id="94322-190">Til dæmis, ef hætt var við upprunalega verkkennið sem var með *Frágangslínu* með magn upp á 15 og *Tiltektarlínu* sem var með heildarmagnið 10, verður nýja magn *Frágangs* í upprunalega verkkenninu núna 5.</span><span class="sxs-lookup"><span data-stu-id="94322-190">For example, if the original work ID had a *Put* line for a quantity of 15, and *Pick* lines that have a total quantity of 10 were canceled, the new *Put* quantity on the original work ID will now be 5.</span></span>

<span data-ttu-id="94322-191">Nýja verkinu verður ekki úthlutað á neinn notanda strax.</span><span class="sxs-lookup"><span data-stu-id="94322-191">The new work won't immediately be assigned to any user.</span></span> <span data-ttu-id="94322-192">Hins vegar er hægt að úthluta því á notanda eftir þörfum með því að nota stöðluðu virknina á síðunni **Upplýsingar um verk**.</span><span class="sxs-lookup"><span data-stu-id="94322-192">However, you can assign it to a user now, as required, by using the standard functionality of the **Work details** page.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="94322-193">Aðeins er hægt að skipta vinnukennum sem innihalda tvær eða fleiri lausar vinnulínur.</span><span class="sxs-lookup"><span data-stu-id="94322-193">You can split only work IDs that contain two or more available work lines.</span></span> <span data-ttu-id="94322-194">Ef **Skipta vinnu** er valið þegar aðeins ein vinnulína er til staðar, færðu eftirfarandi villuboð: „Að minnsta kosti ein vinnulína verður að vera eftir í upprunalegu verki.</span><span class="sxs-lookup"><span data-stu-id="94322-194">If you select **Split work** when there is only one work line, you will receive the following error message: "At least one work line must remain on initial work."</span></span> <span data-ttu-id="94322-195">Í þessu tilvikum kemur engin skipting fram.</span><span class="sxs-lookup"><span data-stu-id="94322-195">In this case, no splitting will occur.</span></span>

## <a name="finish-a-work-split"></a><span data-ttu-id="94322-196">Ljúka vinnuskiptum</span><span class="sxs-lookup"><span data-stu-id="94322-196">Finish a work split</span></span>

<span data-ttu-id="94322-197">Til að ljúka skiptingu vinnu þarf að fjarlægja lokunarástæðuna *Skipta vinnu*.</span><span class="sxs-lookup"><span data-stu-id="94322-197">To finish splitting work, the *Split work* blocking reason must be removed.</span></span> <span data-ttu-id="94322-198">Hægt er að ljúka þessu skrefi á tvennan hátt:</span><span class="sxs-lookup"><span data-stu-id="94322-198">There are two ways to complete this step:</span></span>

- <span data-ttu-id="94322-199">Notandinn sem er að skipta vinnunni lokar síðunni **Skipta vinnu** með því að velja hnappinn **Loka** (**X**) uppi í hægra horninu.</span><span class="sxs-lookup"><span data-stu-id="94322-199">The user who is splitting the work closes the **Split work** page by selecting the **Close** button (**X**) in the upper-right corner.</span></span> <span data-ttu-id="94322-200">Þegar síðunni er lokað verður lokunarástæðan *Skipta vinnu* fjarlægð.</span><span class="sxs-lookup"><span data-stu-id="94322-200">When the page is closed, the *Split Work* blocking reason will be removed.</span></span> <span data-ttu-id="94322-201">Staðan *Lokað fyrir* fyrir þessa vinnu verður endurreiknuð og ef engar eftirstandandi lokunarástæður eru til staðar fyrir þessa vinnu, verður opnað fyrir vinnuna aftur.</span><span class="sxs-lookup"><span data-stu-id="94322-201">The *Blocked* state of this work will be recomputed and, if there are no remaining blocking reasons for this work, the work will be unblocked.</span></span>
- <span data-ttu-id="94322-202">Hvaða notandi sem er opnar verkkennið og velur hnappinn **Hætta við lotu vinnuskiptingar** á aðgerðasvæðinu.</span><span class="sxs-lookup"><span data-stu-id="94322-202">Any user opens the work ID and selects the **Cancel work split session** button on the Action Pane.</span></span> <span data-ttu-id="94322-203">Lokunarástæðan *Skipta vinnu* verður fjarlægð og staðan *Lokað fyrir* fyrir þessa vinnu verður endurreiknuð rétt eins og þegar síðan **Skipta vinnu** er lokuð.</span><span class="sxs-lookup"><span data-stu-id="94322-203">The *Split work* blocking reason will be removed, and the *Blocked* state of this work will be recomputed, just as when the **Split work** page is closed.</span></span>

<span data-ttu-id="94322-204">Þegar lokunarástæðan *Skipta vinnu* hefur verið fjarlægð, verður hægt að keyra vinnuna í fartæki svo lengi sem staðan **Lokað fyrir** er stillt á *Nei* í verkkenninu.</span><span class="sxs-lookup"><span data-stu-id="94322-204">After the *Split work* blocking reason is removed, the work can be run on the mobile device, provided that the **Blocked** state is set to *No* on the work ID.</span></span>

## <a name="user-blocking-on-the-warehouse-management-mobile-app"></a><span data-ttu-id="94322-205">Lokun á notandan í farsímaforriti vöruhúsakerfis</span><span class="sxs-lookup"><span data-stu-id="94322-205">User blocking on the Warehouse Management mobile app</span></span>

<span data-ttu-id="94322-206">Ef reynt er að nota farsímaforrit vöruhúsakerfis til að keyra tiltekt fyrir verkkenni sem verið er að skipta, birtast eftirfarandi villuboð: „Verið er að skipta niður vinnu með auðkennið \#\#\#\#.“</span><span class="sxs-lookup"><span data-stu-id="94322-206">If you try to use the Warehouse Management mobile app to run picking work against a work ID that is being split, you will receive the following error message: "The work with ID \#\#\#\# is currently being split."</span></span> <span data-ttu-id="94322-207">Ef þessi skilaboð birtast skal velja **Hætta við**.</span><span class="sxs-lookup"><span data-stu-id="94322-207">If you receive this message, select **Cancel**.</span></span> <span data-ttu-id="94322-208">Síðan er hægt að halda áfram með aðra vinnu.</span><span class="sxs-lookup"><span data-stu-id="94322-208">You can then continue to process other work.</span></span>

## <a name="other-blocked-operations"></a><span data-ttu-id="94322-209">Aðrar lokaðar aðgerðir</span><span class="sxs-lookup"><span data-stu-id="94322-209">Other blocked operations</span></span>

<span data-ttu-id="94322-210">Allar aðgerðir sem breyta vinnulínum, birgðafærslum eða áfyllingartenglum sem tengjast vinnu sem verið er að skipta munu mistakast og eftirfarandi villuboð birtast: „Verið er að skipta niður vinnu með auðkennið \#\#\#\#.“</span><span class="sxs-lookup"><span data-stu-id="94322-210">Any operations that modify work lines, work inventory transactions, or replenishment links that are related to work that is being split will fail, and the following error message will be shown: "The work with ID \#\#\#\# is currently being split."</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]