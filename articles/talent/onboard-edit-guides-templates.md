---
title: Breyta nýliðakynnngu og -sniðmátum í Dynamics 365 Talent - Onboard
description: Þetta efni útskýrir hvernig á að bæta við verkþáttum og öðrum upplýsingum við þjálfunarleiðbeiningar og sniðmát í Microsoft Dynamics 365 Talent - Onboard.
author: andreabichsel
manager: ''
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-06-19
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 7803c7cd2c58b8544d2c8dd711c295d6882f9fca
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/23/2019
ms.locfileid: "2010799"
---
# <a name="edit-onboarding-guides-and-templates"></a><span data-ttu-id="94b10-103">Breyta nýliðakynnngu og -sniðmátum</span><span class="sxs-lookup"><span data-stu-id="94b10-103">Edit onboarding guides and templates</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="94b10-104">Eftir að þú hefur búið til leiðbeiningar eða sniðmát um borð í Microsoft Dynamics 365 Talent: Onboard verður þú að bæta við kynningu, verkþáttum, tengiliðum og úrræðum.</span><span class="sxs-lookup"><span data-stu-id="94b10-104">After you create an onboarding guide or template in Microsoft Dynamics 365 Talent: Onboard, you must add an introduction, activities, contacts, and resources.</span></span> <span data-ttu-id="94b10-105">Onboard gerir þér kleift að innifela ríkulegt efni í þjálfunarleiðbeiningunum þínum, þar á meðal:</span><span class="sxs-lookup"><span data-stu-id="94b10-105">Onboard lets you include rich content in your onboarding guides, including:</span></span>

- <span data-ttu-id="94b10-106">YouTube-myndbönd</span><span class="sxs-lookup"><span data-stu-id="94b10-106">YouTube videos</span></span>
- <span data-ttu-id="94b10-107">Microsoft Sway-kynningar</span><span class="sxs-lookup"><span data-stu-id="94b10-107">Microsoft Sway presentations</span></span>
- <span data-ttu-id="94b10-108">Microsoft PowerApps-smáforrit</span><span class="sxs-lookup"><span data-stu-id="94b10-108">Microsoft PowerApps apps</span></span>
- <span data-ttu-id="94b10-109">Microsoft Stream-myndbönd</span><span class="sxs-lookup"><span data-stu-id="94b10-109">Microsoft Stream videos</span></span>
- <span data-ttu-id="94b10-110">Microsoft Forms-skjámyndir</span><span class="sxs-lookup"><span data-stu-id="94b10-110">Microsoft Forms forms</span></span>
- <span data-ttu-id="94b10-111">Iframes sem inniheldur efni á vefnum</span><span class="sxs-lookup"><span data-stu-id="94b10-111">Iframes that contains web content</span></span>

## <a name="edit-introductions-or-activities-imported-from-a-template"></a><span data-ttu-id="94b10-112">Breyta kynningum eða verkþáttum sem voru fluttir inn úr sniðmáti</span><span class="sxs-lookup"><span data-stu-id="94b10-112">Edit introductions or activities imported from a template</span></span>

<span data-ttu-id="94b10-113">Ef þú býrð til þjálfunarleiðbeiningar úr sniðmáti eða ef þú flytur verkþætti úr einu sniðmáti yfir í annað, muntu taka eftir hnappnum **Læsa** á innfluttum verkþáttum.</span><span class="sxs-lookup"><span data-stu-id="94b10-113">If you create an onboarding guide from a template, or if you import activities from one template into another, you'll notice a **Lock** button on the imported activities.</span></span> <span data-ttu-id="94b10-114">Þetta er kallað *stjórnaðir verkþættir*.</span><span class="sxs-lookup"><span data-stu-id="94b10-114">These are called *managed activities*.</span></span>

<span data-ttu-id="94b10-115">[![Stjórnaðir verkþættir](./media/onboard-edit-guide-managed-activities.png)](./media/onboard-edit-guide-managed-activities.png)</span><span class="sxs-lookup"><span data-stu-id="94b10-115">[![Managed activities](./media/onboard-edit-guide-managed-activities.png)](./media/onboard-edit-guide-managed-activities.png)</span></span>

<span data-ttu-id="94b10-116">Þegar þú velur stýrðan verkþátt geturðu séð upprunasniðmátið efst í verkþættinum.</span><span class="sxs-lookup"><span data-stu-id="94b10-116">When you select a managed activity, you can see the source template at the top of the activity.</span></span>

<span data-ttu-id="94b10-117">[![Stýrður verkþáttaruppruni](./media/onboard-edit-guide-managed-activity-source.png)](./media/onboard-edit-guide-managed-activity-source.png)</span><span class="sxs-lookup"><span data-stu-id="94b10-117">[![Managed activity source](./media/onboard-edit-guide-managed-activity-source.png)](./media/onboard-edit-guide-managed-activity-source.png)</span></span>

<span data-ttu-id="94b10-118">Ef þú breytir verkþætti í sniðmáti mun Onboard senda breytingarnar á öll sniðmátum og ósendar leiðbeiningar sem byggjast á því sniðmáti.</span><span class="sxs-lookup"><span data-stu-id="94b10-118">If you edit an activity in a template, Onboard will push the changes to all templates and unsent guides that are based on that template.</span></span> <span data-ttu-id="94b10-119">Ef þú velur ósendar leiðbeiningar úr sniðmáti sem þú breyttir og velur síðan flipann **Starfsemi** í leiðbeiningunum muntu sjá tilkynningu um að leiðbeiningunum hafi verið breytt.</span><span class="sxs-lookup"><span data-stu-id="94b10-119">If you select an unsent guide based on a template you edited and then select the **Activities** tab in the guide, you will see a notice that your guide has changed.</span></span> <span data-ttu-id="94b10-120">Til að hafna tilkynningunni velurðu **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="94b10-120">To dismiss the notification, select **OK**.</span></span> 

<span data-ttu-id="94b10-121">[![Breyta tilkynningu](./media/onboard-edit-guide-change-notification.png)](./media/onboard-edit-guide-change-notification.png)</span><span class="sxs-lookup"><span data-stu-id="94b10-121">[![Change notification](./media/onboard-edit-guide-change-notification.png)](./media/onboard-edit-guide-change-notification.png)</span></span>

<span data-ttu-id="94b10-122">Þú munt sjá svartan punkt við hliðina á uppfærðum verkþáttum.</span><span class="sxs-lookup"><span data-stu-id="94b10-122">You'll see a black dot next to the updated activities.</span></span>

<span data-ttu-id="94b10-123">[![Breytur verkþáttur](./media/onboard-edit-guide-changed-activity.png)](./media/onboard-edit-guide-changed-activity.png)</span><span class="sxs-lookup"><span data-stu-id="94b10-123">[![Changed activity](./media/onboard-edit-guide-changed-activity.png)](./media/onboard-edit-guide-changed-activity.png)</span></span>

<span data-ttu-id="94b10-124">Þú getur ekki breytt stýrðum aðgerðum utan upphaflega sniðmátsins nema til að bæta við viðtakanda, gjalddaga eða öðrum upplýsingum í hægri hluta verkþáttarins.</span><span class="sxs-lookup"><span data-stu-id="94b10-124">You can't edit managed activities outside of the original template, except to add an assignee, due date, or other information in the right-hand section of the activity.</span></span>

<span data-ttu-id="94b10-125">Ef þú vilt breyta stýrðum verkþætti, eða ef þú vilt ekki að verkþáttur fái uppfærslur úr sniðmátinu sem hann kom úr skaltu velja hnappinn **Læsa** fyrir þann verkþátt.</span><span class="sxs-lookup"><span data-stu-id="94b10-125">If you want to edit a managed activity, or if you don't want an activity to receive updates from the template it came from, select the **Lock** button for that activity.</span></span> <span data-ttu-id="94b10-126">Hnappurinn **Læsa** mun hverfa.</span><span class="sxs-lookup"><span data-stu-id="94b10-126">The **Lock** button will disappear.</span></span> <span data-ttu-id="94b10-127">Verkþættinum verður ekki lengur stjórnað af upprunalega sniðmátinu og hann mun ekki lengur fá uppfærslur úr því sniðmáti.</span><span class="sxs-lookup"><span data-stu-id="94b10-127">The activity will no longer be managed by the original template, and it will no longer receive updates from that template.</span></span> <span data-ttu-id="94b10-128">Uppfærslur sem þú gerir á verkþætti hafa ekki áhrif á upphaflega sniðmátið.</span><span class="sxs-lookup"><span data-stu-id="94b10-128">Updates you make to an activity do not affect the original template.</span></span>

<span data-ttu-id="94b10-129">Ef þú eyðir verkþætti úr leiðbeiningum og sendir breytingar úr því sniðmáti leiðbeininganna verður verkþættinum áfram eytt í leiðbeiningunum.</span><span class="sxs-lookup"><span data-stu-id="94b10-129">If you delete an activity from a guide and push changes from that guide's template, the activity will remain deleted in the guide.</span></span>

> [!NOTE]
> <span data-ttu-id="94b10-130">Sniðmátum er ekki stjórnað af tengiliðum og tilföngum.</span><span class="sxs-lookup"><span data-stu-id="94b10-130">Contacts and resources aren't managed by templates.</span></span> <span data-ttu-id="94b10-131">Að auki er hlutum ekki stjórnað, þannig að ef þú bætir við eða breytir hluta í sniðmáti verða breytingarnar ekki sendar á neinar leiðbeiningar eða sniðmát sem nota það sniðmát.</span><span class="sxs-lookup"><span data-stu-id="94b10-131">In addition, sections aren't managed, so if you add or edit a section in a template, the changes won't be pushed to any guides or templates that use that template.</span></span>
> 
> <span data-ttu-id="94b10-132">Ef þú bætir nýjum verkþáttum við sniðmát eru nýju verkþættirnir sendir í leiðbeiningar og sniðmát sem byggjast á því sniðmáti og nýju verkþættirnir birtast efst.</span><span class="sxs-lookup"><span data-stu-id="94b10-132">If you add new activities to a template, the new activities are pushed to guides and templates based on that template, and the new activities display at the top.</span></span>

## <a name="import-activities-from-another-template"></a><span data-ttu-id="94b10-133">Flytja inn verkþætti úr öðru sniðmáti</span><span class="sxs-lookup"><span data-stu-id="94b10-133">Import activities from another template</span></span>

<span data-ttu-id="94b10-134">Þú getur flutt inn verkþætti úr einu eða fleiri sniðmátum í leiðbeiningar eða sniðmát.</span><span class="sxs-lookup"><span data-stu-id="94b10-134">You can import activities from one or more templates into a guide or template.</span></span>

1. <span data-ttu-id="94b10-135">Velja skal leiðbeiningarnar eða sniðmátið sem á að breyta.</span><span class="sxs-lookup"><span data-stu-id="94b10-135">Select the guide or template you want to edit.</span></span>

2. <span data-ttu-id="94b10-136">Veldu flipann **Verkþættir**.</span><span class="sxs-lookup"><span data-stu-id="94b10-136">Select the **Activities** tab.</span></span>

3. <span data-ttu-id="94b10-137">Veldu flipann **Flytja inn** í hlutanum til hægri.</span><span class="sxs-lookup"><span data-stu-id="94b10-137">Select the **Import** tab in the section on the right.</span></span>

   <span data-ttu-id="94b10-138">[![Flytja inn verkþætti](./media/onboard-edit-guide-import-activities.png)](./media/onboard-edit-guide-import-activities.png)</span><span class="sxs-lookup"><span data-stu-id="94b10-138">[![Import activities](./media/onboard-edit-guide-import-activities.png)](./media/onboard-edit-guide-import-activities.png)</span></span>

4. <span data-ttu-id="94b10-139">Til að forskoða verkefnin á nýjum flipa í vafranum þínum skaltu velja hnappinn **Opna í nýjum flipa** á hvaða sniðmát sem er.</span><span class="sxs-lookup"><span data-stu-id="94b10-139">To preview the tasks in a new tab in your browser, select the **Open in new tab** button on any template.</span></span>

   <span data-ttu-id="94b10-140">[![Flytja inn verkþætti](./media/onboard-edit-guide-preview-activities.png)](./media/onboard-edit-guide-preview-activities.png)</span><span class="sxs-lookup"><span data-stu-id="94b10-140">[![Import activities](./media/onboard-edit-guide-preview-activities.png)](./media/onboard-edit-guide-preview-activities.png)</span></span>

5. <span data-ttu-id="94b10-141">Dragðu og slepptu viðeigandi sniðmáti á þann stað í leiðbeiningasniðmátinu sem þú vilt að verkþættirnir birtist.</span><span class="sxs-lookup"><span data-stu-id="94b10-141">Drag and drop the desired template to the place in your guide template where you want the activities to appear.</span></span> <span data-ttu-id="94b10-142">Haltu áfram að breyta leiðbeiningunum eða sniðmátinu.</span><span class="sxs-lookup"><span data-stu-id="94b10-142">Continue editing your guide or template.</span></span>

<span data-ttu-id="94b10-143">Innfluttar aðgerðir innihalda hnappinn **Læsa**, sem gefur til kynna að þessum aðgerðum sé stjórnað af sniðmátinu sem þú fluttir inn úr.</span><span class="sxs-lookup"><span data-stu-id="94b10-143">The imported activities will contain a **Lock** button, which indicates those activities are managed by the template you imported from.</span></span> <span data-ttu-id="94b10-144">Þegar þú gerir breytingar á sniðmátinu sem þú fluttir inn uppfærast þessir verkþættir í sniðmátinu sem þú fluttir inn í þá.</span><span class="sxs-lookup"><span data-stu-id="94b10-144">When you make changes to the template you imported, those activities will update in the template you imported them to.</span></span> <span data-ttu-id="94b10-145">Breytingarnar verða þó ekki sendar sjálfkrafa í neinar leiðbeiningar sem eru búnar til úr sniðmátinu sem þú fluttir inn í.</span><span class="sxs-lookup"><span data-stu-id="94b10-145">However, the changes will not be pushed automatically to any guides created from the template you imported to.</span></span>

## <a name="push-changes-from-a-template-to-other-templates-or-guides"></a><span data-ttu-id="94b10-146">Sendu breytingar úr sniðmáti yfir í önnur sniðmát eða leiðbeiningar</span><span class="sxs-lookup"><span data-stu-id="94b10-146">Push changes from a template to other templates or guides</span></span>

<span data-ttu-id="94b10-147">Ef þú breytir sniðmáti sem inniheldur verkþætti sem notaðir eru í öðrum sniðmátum eða leiðbeiningum verðurðu að senda breytingarnar ef þú vilt að þær birtist í hinum sniðmátunum eða leiðbeiningunum.</span><span class="sxs-lookup"><span data-stu-id="94b10-147">If you edit a template that contains activities that are used in other templates or guides, you must push the changes if you want them to appear in the other templates or guides.</span></span>

<span data-ttu-id="94b10-148">Ef þú ert ekki viss um hvort verkþættir sniðmátsins séu notaðir í öðrum sniðmátum eða leiðbeiningum skaltu velja flipann **Notað í** til að skoða hvar þessir verkþættir birtast.</span><span class="sxs-lookup"><span data-stu-id="94b10-148">If you're not sure whether your template's activities are used in other templates or guides, select the **Used in** tab to view where those activities appear.</span></span>

   <span data-ttu-id="94b10-149">[![Skoðaðar leiðbeiningar og sniðmát eru notuð í](./media/onboard-edit-guide-view-used-in.png)](./media/onboard-edit-guide-view-used-in.png)</span><span class="sxs-lookup"><span data-stu-id="94b10-149">[![View guides and templates activities are used in](./media/onboard-edit-guide-view-used-in.png)](./media/onboard-edit-guide-view-used-in.png)</span></span>

<span data-ttu-id="94b10-150">Til að senda breytingarnar þínar:</span><span class="sxs-lookup"><span data-stu-id="94b10-150">To push your changes:</span></span>

1. <span data-ttu-id="94b10-151">Vistaðu breytingarnar þínar með því að velja hnappinn **Vista**.</span><span class="sxs-lookup"><span data-stu-id="94b10-151">Save your changes by selecting the **Save** button.</span></span> <span data-ttu-id="94b10-152">Ef þú gerir það ekki færðu kvaðninguu m að vista breytingarnar þínar í næsta skrefi.</span><span class="sxs-lookup"><span data-stu-id="94b10-152">If you don't do this, you'll be prompted to save your changes in the next step.</span></span>

2. <span data-ttu-id="94b10-153">Veldu **Senda þessar breytingar**.</span><span class="sxs-lookup"><span data-stu-id="94b10-153">Select **Push these changes**.</span></span>

   
## <a name="add-or-edit-an-introduction"></a><span data-ttu-id="94b10-154">Bættu við eða breyttu kynningu</span><span class="sxs-lookup"><span data-stu-id="94b10-154">Add or edit an introduction</span></span>

1. <span data-ttu-id="94b10-155">Á flipanum **Kynning** slærðu inn titil fyrir leiðbeiningarnar og opnunarskilaboð.</span><span class="sxs-lookup"><span data-stu-id="94b10-155">On the **Introduction** tab, enter a title for your guide and an opening message.</span></span> <span data-ttu-id="94b10-156">Veldu til að nota sýnishornatexta **Nota þessi skilaboð**.</span><span class="sxs-lookup"><span data-stu-id="94b10-156">To use the sample text, select **Use this message**.</span></span>

    <span data-ttu-id="94b10-157">[![Inngangsflipi í Onboard-sniðmáti](./media/onboard-template-introduction.png)](./media/onboard-template-introduction.png)</span><span class="sxs-lookup"><span data-stu-id="94b10-157">[![Introduction tab in an Onboard template](./media/onboard-template-introduction.png)](./media/onboard-template-introduction.png)</span></span>

2. <span data-ttu-id="94b10-158">Notaðu sniðhnappana til að kalla fram texta eins og þú vilt eða til að bæta við myndum eða tenglum.</span><span class="sxs-lookup"><span data-stu-id="94b10-158">Use the formatting buttons to call out text as you require, or to add images or links.</span></span>
3. <span data-ttu-id="94b10-159">Veldu **Vista** til að vista vinnuna.</span><span class="sxs-lookup"><span data-stu-id="94b10-159">Select **Save** to save your work.</span></span>

## <a name="add-or-edit-activities"></a><span data-ttu-id="94b10-160">Bæta við eða breyta verkþáttum</span><span class="sxs-lookup"><span data-stu-id="94b10-160">Add or edit activities</span></span>

1. <span data-ttu-id="94b10-161">Á flipanum **Verkþættir** skaltu draga hluti frá hægri yfir á klippusvæðið.</span><span class="sxs-lookup"><span data-stu-id="94b10-161">On the **Activities** tab, drag items from the right to the editing area.</span></span>
2. <span data-ttu-id="94b10-162">Dragðu hnappinn til að skipuleggja leiðbeiningarnar í hluta skaltu draga liðinn **Nýr hluti** yfir á klippusvæðið og slá inn heiti og valfrjálsa lýsingu fyrir hlutann.</span><span class="sxs-lookup"><span data-stu-id="94b10-162">To organize your guide into sections, drag the **New section** item to the editing area, and enter a name and an optional description for the section.</span></span>

    ![[<span data-ttu-id="94b10-163">Nýjum hluta bætt við þjálfunarleiðbeiningar eða -sniðmát</span><span class="sxs-lookup"><span data-stu-id="94b10-163">Adding a new section to an onboarding guide or template</span></span>](./media/onboard-edit-add-section.png)](./media/onboard-edit-add-section.png)

3. <span data-ttu-id="94b10-164">Til að bæta verkþáttum við svo að nýliðar geti lokið þeim skaltu draga liðinn **Nýr verkþáttur** yfir á klippusvæðið og slá inn nafn og lýsingu fyrir verkþáttinn.</span><span class="sxs-lookup"><span data-stu-id="94b10-164">To add activities for your new hire to complete, drag the **New activity** item to the editing area, and enter a name and description for the activity.</span></span>

    ![[<span data-ttu-id="94b10-165">Nýjum verkþætti bætt við þjálfunarleiðbeiningar eða -sniðmát</span><span class="sxs-lookup"><span data-stu-id="94b10-165">Adding a new activity to an onboarding guide or template</span></span>](./media/onboard-edit-add-activity.png)](./media/onboard-edit-add-activity.png)

4. <span data-ttu-id="94b10-166">Bæta ríkulegu efni við þjálfunarleiðbeiningarnar:</span><span class="sxs-lookup"><span data-stu-id="94b10-166">Add rich content to your onboarding guide:</span></span>

    - <span data-ttu-id="94b10-167">Til að bæta myndbandi við á YouTube skaltu draga **YouTube** liðinn yfir á klippusvæðið, slá inn heiti og lýsingu á verkþættinum og slá inn slóðina fyrir YouTube myndbandið.</span><span class="sxs-lookup"><span data-stu-id="94b10-167">To add a YouTube video, drag the **YouTube** item to the editing area, enter a name and description for the activity, and enter the URL for the YouTube video.</span></span>
    - <span data-ttu-id="94b10-168">Til að bæta við Sway-kynningu eða -fréttabréfi dregurðu **Sway**-liðinn yfir á klippusvæðið, slærð inn heiti og lýsingu á verkþættinum og slærð inn ívafna slóð fyrir Sway-kynninguna eða -fréttabréfið.</span><span class="sxs-lookup"><span data-stu-id="94b10-168">To add a Sway presentation or newsletter, drag the **Sway** item to the editing area, enter a name and description for the activity, and enter the embedded URL for the Sway presentation or newsletter.</span></span>
    - <span data-ttu-id="94b10-169">Til að bæta við PowerApps-forriti skaltu draga **PowerApps**-liðinn yfir á klippusvæðið, slá inn heiti og lýsingu á verkþættinum og annaðhvort velja PowerApps-forritið eða slá inn PowerApps-forritsauðkenni.</span><span class="sxs-lookup"><span data-stu-id="94b10-169">To add a PowerApps app, drag the **PowerApps** item to the editing area, enter a name and description for the activity, and either select the PowerApps app or enter the PowerApps app ID.</span></span>
    - <span data-ttu-id="94b10-170">Til að bæta myndbandi við á Microsoft Stream skaltu draga **Microsoft Stream** liðinn yfir á klippusvæðið, slá inn heiti og lýsingu á verkþættinum og slá inn slóðina fyrir Microsoft Stream myndbandið.</span><span class="sxs-lookup"><span data-stu-id="94b10-170">To add a Microsoft Stream video, drag the **Microsoft Stream** item to the editing area, enter a name and description for the activity, and enter the URL for the Microsoft Stream video.</span></span>
    - <span data-ttu-id="94b10-171">Til að bæta við Microsoft Forms-skjámynd skaltu draga **Microsoft Forms**-liðinn yfir á klippusvæðið, slá inn heiti og lýsingu á verkþættinum, slá inn slóðina fyrir Microsoft Forms-skjámyndina og tilgreina stærð skjásvæðisins.</span><span class="sxs-lookup"><span data-stu-id="94b10-171">To add a Microsoft Forms form, drag the **Microsoft Forms** item to the editing area, enter a name and description for the activity, enter the URL for the Microsoft Forms form, and specify the size of the screen area.</span></span>
    - <span data-ttu-id="94b10-172">Til að bæta við iframe sem inniheldur vefefni skaltu draga liðinn **Vefefni (iframe)** yfir á klippusvæðið, slá inn heiti og lýsingu á verkþættinum, slá inn slóðina fyrir Microsoft Forms-skjámyndina og tilgreina stærð skjásvæðisins.</span><span class="sxs-lookup"><span data-stu-id="94b10-172">To add an iframe that contains web content, drag the **Web Content (iframe)** item to the editing area, enter a name and description for the activity, enter the URL for the web content, and specify the size of the screen area.</span></span>

    ![[<span data-ttu-id="94b10-173">Nýju ríkulegu efni bætt við þjálfunarleiðbeiningar eða -sniðmát</span><span class="sxs-lookup"><span data-stu-id="94b10-173">Adding rich content to an onboarding guide or template</span></span>](./media/onboard-edit-rich-content.png)](./media/onboard-edit-add-rich-content.png)

2. <span data-ttu-id="94b10-174">Valfrjálst: Á svæðinu hægra megin við hvern verkþátt skal úthluta verkþættinum á ákveðinn aðila eða hlutverk, bæta við gjalddaga og tengilið og úthluta lit á flokkinn.</span><span class="sxs-lookup"><span data-stu-id="94b10-174">Optional: In the area on the right of each activity, assign the activity to a specific person or role, add a due date and contact person, and assign a category color.</span></span> <span data-ttu-id="94b10-175">Þegar þú úthlutar verkþætti á annan einstakling eða hlutverk er verkefni stofnað fyrir hvern einstakling.</span><span class="sxs-lookup"><span data-stu-id="94b10-175">When you assign an activity to a person or role, a task is created for each individual.</span></span> <span data-ttu-id="94b10-176">Þetta verkefni birtist á valmyndinni **Verk** í Onboard.</span><span class="sxs-lookup"><span data-stu-id="94b10-176">This task appears on the **Tasks** menu in Onboard.</span></span>

    <span data-ttu-id="94b10-177">[![Úthlutun verkþátta í þjálfunarleiðbeiningum eða -sniðmáti](./media/onboard-assign-activity.png)](./media/onboard-assign-activity.png)</span><span class="sxs-lookup"><span data-stu-id="94b10-177">[![Assigning an activity in an onboarding guide or template](./media/onboard-assign-activity.png)](./media/onboard-assign-activity.png)</span></span>

3. <span data-ttu-id="94b10-178">Veldu **Vista** til að vista vinnuna.</span><span class="sxs-lookup"><span data-stu-id="94b10-178">Select **Save** to save your work.</span></span>

<span data-ttu-id="94b10-179">Til að eyða verkþætti eða hluta velurðu hnappinn **Eyða** (ruslatunnutáknið) í efra hægra horninu í verkþættinum eða hlutanum.</span><span class="sxs-lookup"><span data-stu-id="94b10-179">To delete an activity or section, select the **Delete** button (the trash can symbol) in the upper-right corner of the activity or section.</span></span>

<span data-ttu-id="94b10-180">Dragðu þær á nýjan stað til að endurraða verkþáttum og hlutum.</span><span class="sxs-lookup"><span data-stu-id="94b10-180">To rearrange activities and sections, drag them to a new location.</span></span>

## <a name="add-or-edit-contacts"></a><span data-ttu-id="94b10-181">Bæta við eða breyta tengiliðum</span><span class="sxs-lookup"><span data-stu-id="94b10-181">Add or edit contacts</span></span>

<span data-ttu-id="94b10-182">Hægt er að bæta við tengiliðum sem geta aðstoðað nýliða þína við að ná árangri frá fyrsta degi.</span><span class="sxs-lookup"><span data-stu-id="94b10-182">You can add contact people who can help your new hire succeed from day one.</span></span> <span data-ttu-id="94b10-183">Þessir tengiliðir geta verið ráðningaraðilar, teymisfélagar, félagar í starfsþjálfun, leiðbeinendur, kerfisstjórar og starfsfólk upplýsingatækni.</span><span class="sxs-lookup"><span data-stu-id="94b10-183">These contacts can be recruiters, teammates, onboarding buddies, mentors, admins, and IT support staff.</span></span>

1. <span data-ttu-id="94b10-184">Á flipanum **Tengiliðir** velurðu **Nýr tengiliður**.</span><span class="sxs-lookup"><span data-stu-id="94b10-184">On the **Contacts** tab, select **New contact**.</span></span>
2. <span data-ttu-id="94b10-185">Í valmyndinni **Bæta hópmeðlimi við** slærðu inn nafn tengiliðar eða netfang, slærð inn stutta lýsingu sem útskýrir hvernig tengiliðurinn getur hjálpað nýliðanum og velur síðan **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="94b10-185">In the **Add team member** dialog box, enter the contact person's name or email address, enter a short description that explains how the contact person can help the new hire, and then select **Add**.</span></span> 

    ![[<span data-ttu-id="94b10-186">Tengiliðum bætt við í þjálfunarleiðbeiningum eða -sniðmáti</span><span class="sxs-lookup"><span data-stu-id="94b10-186">Adding contacts to an onboarding guide or template</span></span>](./media/onboard-edit-add-contact.png)](./media/onboard-edit-add-contact.png)

    <span data-ttu-id="94b10-187">Einnig er hægt að velja einn eða fleiri tengiliði undir **Tillögum**.</span><span class="sxs-lookup"><span data-stu-id="94b10-187">Alternately, you can select one or more contacts under **Suggestions**.</span></span>

3. <span data-ttu-id="94b10-188">Veldu **Vista** til að vista vinnuna.</span><span class="sxs-lookup"><span data-stu-id="94b10-188">Select **Save** to save your work.</span></span>

<span data-ttu-id="94b10-189">Til að eyða tengilið velurðu hnappinn **Eyða** (ruslatunnutáknið) til hægri við tengiliðinn.</span><span class="sxs-lookup"><span data-stu-id="94b10-189">To delete a contact, select the **Delete** button (the trash can symbol) to the right of the contact.</span></span>

<span data-ttu-id="94b10-190">Til að breyta tengilið velurðu hnappinn **Breyta** (blýantstáknið) til hægri við tengiliðinn.</span><span class="sxs-lookup"><span data-stu-id="94b10-190">To edit a contact, select the **Edit** button (the pencil symbol) to the right of the contact.</span></span>

## <a name="add-or-edit-resources"></a><span data-ttu-id="94b10-191">Bæta við eða breyta tilföngum</span><span class="sxs-lookup"><span data-stu-id="94b10-191">Add or edit resources</span></span>

<span data-ttu-id="94b10-192">Þú getur bætt við gagnlegum skrám, kortum og tenglum í hlutann **Tilföng** í þjálfunarleiðbeiningunum.</span><span class="sxs-lookup"><span data-stu-id="94b10-192">You can add useful files, maps, and links to the **Resources** section of your onboarding guide.</span></span>

1. <span data-ttu-id="94b10-193">Á flipanum **Tilföng** velurðu **Nýtt tilfang**.</span><span class="sxs-lookup"><span data-stu-id="94b10-193">On the **Resources** tab, select **New resource**.</span></span>
2. <span data-ttu-id="94b10-194">Fylgið einu af eftirfarandi skrefum:</span><span class="sxs-lookup"><span data-stu-id="94b10-194">Follow one of these steps:</span></span>

    - <span data-ttu-id="94b10-195">Til að bæta við skrá velurðu flipann **Skrá** og dregur skrána inn á afmarkað svæði.</span><span class="sxs-lookup"><span data-stu-id="94b10-195">To add a file, select the **File** tab, and drag the file into the designated area.</span></span> <span data-ttu-id="94b10-196">(Að öðrum kosti skaltu smella einhvers staðar á því svæði til að leita að skránni í tölvunni eða velja **Fletta OneDrive**.) Sláðu inn heiti fyrir skrána og veldu síðan **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="94b10-196">(Alternatively, click anywhere in that area to browse for the file on your computer, or select **Browse OneDrive**.) Enter a name for the file, and then select **Add**.</span></span>
    - <span data-ttu-id="94b10-197">Til að bæta við tengli velurðu flipann **Tengill**, slærð inn heiti og slóð fyrir tengilinn og velur síðan **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="94b10-197">To add a link, select the **Link** tab, enter a name and address for the link, and then select **Add**.</span></span>
    - <span data-ttu-id="94b10-198">Til að bæta við vörpun velurðu flipann **Vörpun**, slærð inn heiti og slóð fyrir vörpunina og velur síðan **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="94b10-198">To add a map, select the **Map** tab, enter a name and address for the map, and then select **Add**.</span></span> <span data-ttu-id="94b10-199">Onboard mun innihalda vörpun á slóðinni sem þú tilgreinir.</span><span class="sxs-lookup"><span data-stu-id="94b10-199">Onboard will include a map of the address that you specify.</span></span>

    ![[<span data-ttu-id="94b10-200">Tilföngum bætt við þjálfunarleiðbeiningar eða -sniðmát</span><span class="sxs-lookup"><span data-stu-id="94b10-200">Adding a resource to an onboarding guide or template</span></span>](./media/onboard-edit-add-resource.png)](./media/onboard-edit-add-resource.png)

3. <span data-ttu-id="94b10-201">Veldu **Vista** til að vista vinnuna.</span><span class="sxs-lookup"><span data-stu-id="94b10-201">Select **Save** to save your work.</span></span>

<span data-ttu-id="94b10-202">Til að eyða tilfangi velurðu hnappinn **Eyða** (ruslatunnutáknið) til hægri við tilfangið.</span><span class="sxs-lookup"><span data-stu-id="94b10-202">To delete a resource, select the **Delete** button (the trash can symbol) to the right of the resource.</span></span>

<span data-ttu-id="94b10-203">Til að breyta tengilið velurðu hnappinn **Breyta** (blýantstáknið) til hægri við tilfangið.</span><span class="sxs-lookup"><span data-stu-id="94b10-203">To edit a contact, select the **Edit** button (the pencil symbol) to the right of the resource.</span></span>

## <a name="next-steps"></a><span data-ttu-id="94b10-204">Næstu skref</span><span class="sxs-lookup"><span data-stu-id="94b10-204">Next steps</span></span>

- [<span data-ttu-id="94b10-205">Deildu efni með öðrum þátttakendum</span><span class="sxs-lookup"><span data-stu-id="94b10-205">Share content with other contributors</span></span>](./onboard-share-template.md)
- [<span data-ttu-id="94b10-206">Skoða stöðu verkefna og nýja starfsmenn</span><span class="sxs-lookup"><span data-stu-id="94b10-206">View the status of tasks and onboarding employees</span></span>](./onboard-view-status.md)
- [<span data-ttu-id="94b10-207">Stofna ráðningarteymi í Onboard</span><span class="sxs-lookup"><span data-stu-id="94b10-207">Create hiring teams in Onboard</span></span>](./onboard-create-team.md)

### <a name="see-also"></a><span data-ttu-id="94b10-208">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="94b10-208">See also</span></span>

- [<span data-ttu-id="94b10-209">Prófaðu eða keyptu Onboard-forritið</span><span class="sxs-lookup"><span data-stu-id="94b10-209">Try or buy the Onboard app</span></span>](https://dynamics.microsoft.com/talent/onboard/)
- [<span data-ttu-id="94b10-210">Nýjungar</span><span class="sxs-lookup"><span data-stu-id="94b10-210">What's new</span></span>](./whats-new.md)
- [<span data-ttu-id="94b10-211">Athugasemdir við útgáfu</span><span class="sxs-lookup"><span data-stu-id="94b10-211">Release notes</span></span>](https://docs.microsoft.com/business-applications-release-notes/index)
- [<span data-ttu-id="94b10-212">Fá aðstoð</span><span class="sxs-lookup"><span data-stu-id="94b10-212">Get support</span></span>](./talent-support.md)
