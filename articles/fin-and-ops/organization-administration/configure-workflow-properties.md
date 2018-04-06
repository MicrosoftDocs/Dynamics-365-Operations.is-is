---
title: "Skilgreining verkflæðiseiginleika"
description: "Þetta efnisatriði útskýrir hvernig skilgreina á mismunandi eiginleika verkflæðis."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 196083
ms.assetid: 192b7a98-7d04-4c7a-a986-29d797a8a837
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 19cc8f92b5bb6d9ddfdc77785e48de17ed005703
ms.openlocfilehash: 7ea35d851613a19889392400e31cf8492d5dc799
ms.contentlocale: is-is
ms.lasthandoff: 03/23/2018

---

# <a name="configure-workflow-properties"></a><span data-ttu-id="82cfa-103">Skilgreining verkflæðiseiginleika</span><span class="sxs-lookup"><span data-stu-id="82cfa-103">Configure workflow properties</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="82cfa-104">Þetta efnisatriði útskýrir hvernig skilgreina á mismunandi eiginleika verkflæðis.</span><span class="sxs-lookup"><span data-stu-id="82cfa-104">This topic explains how to configure the various properties of a workflow.</span></span>

<span data-ttu-id="82cfa-105">Opna verkflæðið í verkflæðisritlinum til að skilgreina eiginleika verkflæðis.</span><span class="sxs-lookup"><span data-stu-id="82cfa-105">To configure the properties of a workflow, open the workflow in the workflow editor.</span></span> <span data-ttu-id="82cfa-106">Smellið á vinnusvæði verkflæðisritlinum, og smellið síðan á **Eiginleika** til að opna **Eiginleika** síðu.</span><span class="sxs-lookup"><span data-stu-id="82cfa-106">Click the canvas of the workflow editor, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="82cfa-107">Notið síðan eftirfarandi ferli til að stilla mismunandi eiginleika fyrir verkflæðið.</span><span class="sxs-lookup"><span data-stu-id="82cfa-107">You can then use the following procedures to configure the various properties of the workflow.</span></span>

## <a name="name-the-workflow"></a><span data-ttu-id="82cfa-108">Verkflæðinu er gefið heiti</span><span class="sxs-lookup"><span data-stu-id="82cfa-108">Name the workflow</span></span>
<span data-ttu-id="82cfa-109">Fylgið þessum skrefum til að færa inn heiti á verkflæðinu.</span><span class="sxs-lookup"><span data-stu-id="82cfa-109">Follow these steps to enter a name for the workflow.</span></span>

1.  <span data-ttu-id="82cfa-110">Í vinstri glugganum, smelltu á **grunnstillingar**.</span><span class="sxs-lookup"><span data-stu-id="82cfa-110">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="82cfa-111">Á svæðinu **Heiti** skal færa inn einkvæmt heiti fyrir Verkflæðið</span><span class="sxs-lookup"><span data-stu-id="82cfa-111">In the **Name** field, enter a unique name for the workflow.</span></span> <span data-ttu-id="82cfa-112">Til dæmis, gefum okkur að stofna ætti verkflæði innkaupabeiðna fyrir hvert land eða svæði starfseminnar, gefa mætti verkflæði innkaupabeiðninnar heitið **Innkaupabeiðni Danmörk** eða **Innkaupabeiðni Spánn**.</span><span class="sxs-lookup"><span data-stu-id="82cfa-112">For example, if you create a purchase requisition workflow for each country/region that you operate in, you can name the purchase requisition workflow **Purchase Requisitions Denmark** or **Purchase Requisitions Spain**.</span></span>

## <a name="specify-the-workflow-owner"></a><span data-ttu-id="82cfa-113">Tilgreinið eiganda verkflæðis</span><span class="sxs-lookup"><span data-stu-id="82cfa-113">Specify the workflow owner</span></span>
<span data-ttu-id="82cfa-114">Eigandi verkflæðis er sá aðili sem stjórnar og viðheldur verkflæðinu.</span><span class="sxs-lookup"><span data-stu-id="82cfa-114">The workflow owner is the person who manages and maintains the workflow.</span></span> <span data-ttu-id="82cfa-115">Fylgið skrefum ef tilgreina á eiganda verkflæðis.</span><span class="sxs-lookup"><span data-stu-id="82cfa-115">Follow these steps to specify the workflow owner.</span></span>

1.  <span data-ttu-id="82cfa-116">Í vinstri glugganum, smelltu á **grunnstillingar**.</span><span class="sxs-lookup"><span data-stu-id="82cfa-116">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="82cfa-117">Á listanum **Eigandi** skal velja nafn þess aðila sem á að stjórna verkflæðinu.</span><span class="sxs-lookup"><span data-stu-id="82cfa-117">In the **Owner** list, select the name of the person who will manage the workflow.</span></span>

## <a name="select-an-email-template"></a><span data-ttu-id="82cfa-118">Velja tölvupóstssniðmát</span><span class="sxs-lookup"><span data-stu-id="82cfa-118">Select an email template</span></span>
<span data-ttu-id="82cfa-119">Fylgið eftirfarandi skrefum til að velja sniðmát fyrir tölvupóst sem er notuð til að mynda skilaboð tilkynningar um verkflæðið.</span><span class="sxs-lookup"><span data-stu-id="82cfa-119">Follow these steps to select the email template that is used to generate notification messages about the workflow.</span></span>

1.  <span data-ttu-id="82cfa-120">Í vinstri glugganum, smelltu á **grunnstillingar**.</span><span class="sxs-lookup"><span data-stu-id="82cfa-120">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="82cfa-121">Í **sniðmát fyrir Tölvupóst fyrir verkflæðistilkynningar** skal velja sniðmát.</span><span class="sxs-lookup"><span data-stu-id="82cfa-121">In the **Email template for workflow notifications** list, select the template.</span></span>

## <a name="enter-instructions-for-users"></a><span data-ttu-id="82cfa-122">Færa skal inn notendaleiðbeiningar</span><span class="sxs-lookup"><span data-stu-id="82cfa-122">Enter instructions for users</span></span>
<span data-ttu-id="82cfa-123">Hægt er að veita þeim notendum leiðbeiningar sem senda skjöl til vinnslu og samþykktar.</span><span class="sxs-lookup"><span data-stu-id="82cfa-123">You can provide instructions to users who submit documents for processing and approval.</span></span> <span data-ttu-id="82cfa-124">Þessar Notendur eru einnig nefndar *upphafsmenn*.</span><span class="sxs-lookup"><span data-stu-id="82cfa-124">These users are also referred to as *originators*.</span></span> <span data-ttu-id="82cfa-125">Gefum okkur til dæmis að verið sé að búa til verkflæði fyrir innkaupabeiðni, og þú færir inn leiðbeiningar.</span><span class="sxs-lookup"><span data-stu-id="82cfa-125">For example, you're creating a purchase requisition workflow, and you enter instructions.</span></span> <span data-ttu-id="82cfa-126">Notendur sem færa inn innkaupabeiðnir geta skoðað leiðbeiningar á síðunni **Innkaupabeiðnir** .</span><span class="sxs-lookup"><span data-stu-id="82cfa-126">Those instructions can then be viewed by users who enter purchase requisitions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="82cfa-127">TIL að skoða leiðbeiningarnar, smellir upphafsmaðurinn á táknið á skilaboðastikunni.</span><span class="sxs-lookup"><span data-stu-id="82cfa-127">To view instructions, the originator clicks the icon in the workflow message bar.</span></span> <span data-ttu-id="82cfa-128">Fylgið eftirfarandi skrefum til að bæta við leiðbeiningum fyrir notendur.</span><span class="sxs-lookup"><span data-stu-id="82cfa-128">Follow these steps to enter instructions for users.</span></span>

1.  <span data-ttu-id="82cfa-129">Í vinstri glugganum, smelltu á **grunnstillingar**.</span><span class="sxs-lookup"><span data-stu-id="82cfa-129">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="82cfa-130">Í **leiðbeiningar við framlagningu** svæðinu, færið inn leiðbeiningar.</span><span class="sxs-lookup"><span data-stu-id="82cfa-130">In the **Submission instructions** field, enter the instructions.</span></span>
3.  <span data-ttu-id="82cfa-131">Hægt er að sérsníða leiðbeiningarnar með því að færa inn staðgengla.</span><span class="sxs-lookup"><span data-stu-id="82cfa-131">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="82cfa-132">Staðgenglar eru settir í stað viðeigandi gagna þegar leiðbeiningar birtist notendum.</span><span class="sxs-lookup"><span data-stu-id="82cfa-132">Placeholders are replaced with the appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="82cfa-133">Fylgið eftirfarandi skrefum til að færa inn staðgengil:</span><span class="sxs-lookup"><span data-stu-id="82cfa-133">To insert a placeholder, follow these steps:</span></span>
    1.  <span data-ttu-id="82cfa-134">Smellið á **leiðbeiningar við framlagningu** til þess að tilgreina hvar staðgengill á að birtast.</span><span class="sxs-lookup"><span data-stu-id="82cfa-134">Click in the **Submission instructions** field to specify where the placeholder should appear.</span></span>
    2.  <span data-ttu-id="82cfa-135">Smella á **Setja inn staðgengil**</span><span class="sxs-lookup"><span data-stu-id="82cfa-135">Click **Insert placeholder**.</span></span>
    3.  <span data-ttu-id="82cfa-136">Í listanum sem birtist skal velja staðgengilinn til að setja inn.</span><span class="sxs-lookup"><span data-stu-id="82cfa-136">In the list that appears, select the placeholder to insert.</span></span>
    4.  <span data-ttu-id="82cfa-137">Smellt er á **Setja inn**.</span><span class="sxs-lookup"><span data-stu-id="82cfa-137">Click **Insert**.</span></span>

4.  <span data-ttu-id="82cfa-138">Til að bæta þýðingum við leiðbeiningar skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="82cfa-138">To add translations of the instructions, follow these steps:</span></span>
    1.  <span data-ttu-id="82cfa-139">Smellt er á **Þýðingar**.</span><span class="sxs-lookup"><span data-stu-id="82cfa-139">Click **Translations**.</span></span>
    2.  <span data-ttu-id="82cfa-140">Á síðunni sem birtist er smellt á **bæta við**.</span><span class="sxs-lookup"><span data-stu-id="82cfa-140">On the page that appears, click **Add**.</span></span>
    3.  <span data-ttu-id="82cfa-141">Í listanum sem birtist skal velja tungumálið sem á að færa inn í textanum.</span><span class="sxs-lookup"><span data-stu-id="82cfa-141">In the list that appears, select the language that you will enter the text in.</span></span>
    4.  <span data-ttu-id="82cfa-142">Í svæðið **þýddur texti** skal færa inn textann.</span><span class="sxs-lookup"><span data-stu-id="82cfa-142">In the **Translated text** field, enter the text.</span></span>
    5.  <span data-ttu-id="82cfa-143">Hægt er að sérsníða texta með því að færa inn staðgengla.</span><span class="sxs-lookup"><span data-stu-id="82cfa-143">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="82cfa-144">Sjá skref 3 til að fá leiðbeiningar um hvernig á að færa inn staðgengill.</span><span class="sxs-lookup"><span data-stu-id="82cfa-144">For instructions about how to enter a placeholder, see step 3.</span></span>
    6.  <span data-ttu-id="82cfa-145">Smellið á **Loka**.</span><span class="sxs-lookup"><span data-stu-id="82cfa-145">Click **Close**.</span></span>

## <a name="specify-when-this-workflow-is-used"></a><span data-ttu-id="82cfa-146">Tilgreina skal hvenær á að nota þetta verkflæði</span><span class="sxs-lookup"><span data-stu-id="82cfa-146">Specify when this workflow is used</span></span>
<span data-ttu-id="82cfa-147">Hægt er að stofna mörg verkflæði á grundvelli sama gerð.</span><span class="sxs-lookup"><span data-stu-id="82cfa-147">You can create multiple workflows that are based on the same type.</span></span> <span data-ttu-id="82cfa-148">Til dæmis er hægt að stofna innkaupabeiðniverkflæði fyrir hvert land eða svæði starfseminnar, eins og Innkaupabeiðni Danmörk og Innkaupabeiðni Spánn.</span><span class="sxs-lookup"><span data-stu-id="82cfa-148">For example, you can create a purchase requisition workflow for each country/region that you operate in, such as Purchase Requisitions Denmark and Purchase Requisitions Spain.</span></span> <span data-ttu-id="82cfa-149">Þegar búið er að stofna mörg verkflæði á grundvelli sama gerðar, verður að tilgreina hvenær á nota hvert verkflæði.</span><span class="sxs-lookup"><span data-stu-id="82cfa-149">When you have multiple workflows that are based on the same type, you must specify when each workflow is used.</span></span> <span data-ttu-id="82cfa-150">Fyrir dæmið hér á undan, tilgreinið eftirfarandi skilyrði:</span><span class="sxs-lookup"><span data-stu-id="82cfa-150">For the preceding example, you specify the following conditions:</span></span>

-   <span data-ttu-id="82cfa-151">Innkaupabeiðni Danmörk er notað þegar: landið/svæðið er = DK.</span><span class="sxs-lookup"><span data-stu-id="82cfa-151">Purchase Requisitions Denmark is used when: country/region = DK</span></span>
-   <span data-ttu-id="82cfa-152">Innkaupabeiðni spánn er notað þegar: landið/svæðið er = ES.</span><span class="sxs-lookup"><span data-stu-id="82cfa-152">Purchase Requisitions Spain is used when: country/region = ES</span></span>

<span data-ttu-id="82cfa-153">Fylgið eftirfarandi skrefum til að tilgreina hvenær á að nota skilgreint verkflæði.</span><span class="sxs-lookup"><span data-stu-id="82cfa-153">Follow these steps to specify when the workflow that you're configuring is used.</span></span>

1.  <span data-ttu-id="82cfa-154">Á vinstra svæðinu er smellt á **virkja**.</span><span class="sxs-lookup"><span data-stu-id="82cfa-154">In the left pane, click **Activation**.</span></span>
2.  <span data-ttu-id="82cfa-155">Veldu gátreitinn **Tilgreina skilyrði fyrir keyrslu verkflæðisins**</span><span class="sxs-lookup"><span data-stu-id="82cfa-155">Select the **Set the conditions for running this workflow** check box.</span></span>
3.  <span data-ttu-id="82cfa-156">Smellt er á **Bæta við Skilyrði**.</span><span class="sxs-lookup"><span data-stu-id="82cfa-156">Click **Add condition**.</span></span>
4.  <span data-ttu-id="82cfa-157">Færið inn skilyrði.</span><span class="sxs-lookup"><span data-stu-id="82cfa-157">Enter a condition.</span></span>
5.  <span data-ttu-id="82cfa-158">Færið inn öll önnur skilyrði sem krafist er.</span><span class="sxs-lookup"><span data-stu-id="82cfa-158">Enter any additional conditions that are required.</span></span>
6.  <span data-ttu-id="82cfa-159">Til að sannreyna að skilyrðin sem voru færð hafi verið stilllt rétt, skal fylgja eftirfarandi skrefum:</span><span class="sxs-lookup"><span data-stu-id="82cfa-159">To verify that the conditions that you entered are set correctly, follow these steps:</span></span>
    1.  <span data-ttu-id="82cfa-160">Smellið á **Prófun**.</span><span class="sxs-lookup"><span data-stu-id="82cfa-160">Click **Test**.</span></span>
    2.  <span data-ttu-id="82cfa-161">Á síðunni **Kanna verkflæðisskilyrði** , í **Villuleita skilyrði** svæði, velja færslu.</span><span class="sxs-lookup"><span data-stu-id="82cfa-161">On the **Test workflow condition** page, in the **Validate condition** area, select a record.</span></span>
    3.  <span data-ttu-id="82cfa-162">Smellið á **Prófun**.</span><span class="sxs-lookup"><span data-stu-id="82cfa-162">Click **Test**.</span></span> <span data-ttu-id="82cfa-163">Kerfið metur færsluna og ákveður hvort hún standist skilyrði sem þú skilgreindir.</span><span class="sxs-lookup"><span data-stu-id="82cfa-163">The system evaluates the record to determine whether it meets the conditions that you specified.</span></span> <span data-ttu-id="82cfa-164">Til dæmis, ef verið er að búa til verkflæði fyrir innkaupabeiðni á Spáni sýnir svæðið **Villuleita skilyrði** á síðunni lista yfir innkaupabeiðnir.</span><span class="sxs-lookup"><span data-stu-id="82cfa-164">For example, if you're creating a purchase requisition workflow for Spain, the **Validate condition** area of the page shows a list of purchase requisitions.</span></span> <span data-ttu-id="82cfa-165">Þegar smellt er á **Prófun** mun kerfið meta valdar innkaupabeiðnir og ákveða hvort Land/svæði er ES.</span><span class="sxs-lookup"><span data-stu-id="82cfa-165">When you click **Test**, the system evaluates the selected purchase requisition to determine whether the country/region is ES.</span></span>
    4.  <span data-ttu-id="82cfa-166">Smelltu á **Í lagi** eða **hætta við** til að fara aftur síðuna **forstillingar**.</span><span class="sxs-lookup"><span data-stu-id="82cfa-166">Click **OK** or **Cancel** to return to the **Properties** page.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="82cfa-167">Tilgreinið hvenær tilkynningar eru sendar út</span><span class="sxs-lookup"><span data-stu-id="82cfa-167">Specify when notifications are sent</span></span>
<span data-ttu-id="82cfa-168">Þegar skjal er sent í vinnslu þá er verkflæðistilvik stofnað.</span><span class="sxs-lookup"><span data-stu-id="82cfa-168">When a document is submitted for processing, a workflow instance is created.</span></span> <span data-ttu-id="82cfa-169">Hægt er að senda tilkynningar til notenda þegar verkflæðistilvik á grundvelli verkflæðisins, eru sett af stað, lokið við þau, eytt, eða þau stöðvuð út af villu.</span><span class="sxs-lookup"><span data-stu-id="82cfa-169">You can send notifications to users when workflow instances that are based on the workflow are started, completed, terminated, or stopped because of an error.</span></span> <span data-ttu-id="82cfa-170">Fylgið eftirfarandi skrefum til að tilgreina hvenær senda á út tilkynningar.</span><span class="sxs-lookup"><span data-stu-id="82cfa-170">Follow these steps to specify when notifications are sent.</span></span>

1.  <span data-ttu-id="82cfa-171">Á svæðinu vinstra megin, smella á **tilkynningar**.</span><span class="sxs-lookup"><span data-stu-id="82cfa-171">In the left pane, click **Notifications**.</span></span>
2.  <span data-ttu-id="82cfa-172">Veljið gátreit fyrir hvert tilvik sem á að virkja tilkynningar:</span><span class="sxs-lookup"><span data-stu-id="82cfa-172">Select the check box for each event that should trigger notifications:</span></span>
    -   <span data-ttu-id="82cfa-173">**Byrjað** — senda út tilkynningar þegar byrjað er á verkflæðistilviki.</span><span class="sxs-lookup"><span data-stu-id="82cfa-173">**Started** – Send notifications when a workflow instance is started.</span></span>
    -   <span data-ttu-id="82cfa-174">**Stöðvað (villa)** — senda út tilkynningar þegar verkflæðistilvik hefur verið stöðvað út af villu.</span><span class="sxs-lookup"><span data-stu-id="82cfa-174">**Stopped** – Send notifications when a workflow instance is stopped because of an error.</span></span>
    -   <span data-ttu-id="82cfa-175">**Byrjað** — senda út tilkynningar þegar verkflæðistilviki er lokið.</span><span class="sxs-lookup"><span data-stu-id="82cfa-175">**Completed** – Send notifications when a workflow instance is completed.</span></span>
    -   <span data-ttu-id="82cfa-176">**Óafturkræft** — senda út tilkynningar þegar verkflæðistilvik hefur verið stöðvað út af óafturkræfri villu.</span><span class="sxs-lookup"><span data-stu-id="82cfa-176">**Unrecoverable** – Send notifications when a workflow instance is stopped because of an unrecoverable error.</span></span>
    -   <span data-ttu-id="82cfa-177">**Slitið** — senda út tilkynningar þegar verkflæðistilviki er slitið.</span><span class="sxs-lookup"><span data-stu-id="82cfa-177">**Terminated** – Send notifications when a workflow instance is terminated.</span></span>

3.  <span data-ttu-id="82cfa-178">Veljið línu fyrir tilvik sem þú valdir í skrefi 2.</span><span class="sxs-lookup"><span data-stu-id="82cfa-178">Select the row for an event that you selected in step 2.</span></span>
4.  <span data-ttu-id="82cfa-179">Á **tilkynningartexti** flipanum í textareitinn, færa inn texta tilkynningarinnar.</span><span class="sxs-lookup"><span data-stu-id="82cfa-179">On the **Notification text** tab, enter the text of the notification.</span></span>
5.  <span data-ttu-id="82cfa-180">Hægt er að sérsníða texta með því að færa inn staðgengla.</span><span class="sxs-lookup"><span data-stu-id="82cfa-180">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="82cfa-181">Staðgenglar eru settir í stað viðeigandi gagna þegar textinn birtist notendum.</span><span class="sxs-lookup"><span data-stu-id="82cfa-181">Placeholders are replaced with the appropriate data when the text is shown to users.</span></span> <span data-ttu-id="82cfa-182">Fylgið eftirfarandi skrefum til að færa inn staðgengil:</span><span class="sxs-lookup"><span data-stu-id="82cfa-182">To insert a placeholder, follow these steps:</span></span>
    1.  <span data-ttu-id="82cfa-183">Smellið á reit til þess að tilgreina hvar staðgengill á að birtast.</span><span class="sxs-lookup"><span data-stu-id="82cfa-183">Click in the field to specify where the placeholder should appear.</span></span>
    2.  <span data-ttu-id="82cfa-184">Smella á **Setja inn staðgengil**</span><span class="sxs-lookup"><span data-stu-id="82cfa-184">Click **Insert placeholder**.</span></span>
    3.  <span data-ttu-id="82cfa-185">Í listanum sem birtist skal velja staðgengilinn til að setja inn.</span><span class="sxs-lookup"><span data-stu-id="82cfa-185">In the list that appears, select the placeholder to insert.</span></span>
    4.  <span data-ttu-id="82cfa-186">Smellt er á **Setja inn**.</span><span class="sxs-lookup"><span data-stu-id="82cfa-186">Click **Insert**.</span></span>

6.  <span data-ttu-id="82cfa-187">Til að bæta þýðingum við textann, skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="82cfa-187">To add translations of the text, follow these steps:</span></span>
    1.  <span data-ttu-id="82cfa-188">Smellt er á **Þýðingar**.</span><span class="sxs-lookup"><span data-stu-id="82cfa-188">Click **Translations**.</span></span>
    2.  <span data-ttu-id="82cfa-189">Á síðunni sem birtist er smellt á **bæta við**.</span><span class="sxs-lookup"><span data-stu-id="82cfa-189">On the page that appears, Click **Add**.</span></span>
    3.  <span data-ttu-id="82cfa-190">Í listanum sem birtist skal velja tungumálið sem á að færa inn í textanum.</span><span class="sxs-lookup"><span data-stu-id="82cfa-190">In the list that appears, select the language that you will enter the text in.</span></span>
    4.  <span data-ttu-id="82cfa-191">Í svæðið **þýddur texti** skal færa inn textann.</span><span class="sxs-lookup"><span data-stu-id="82cfa-191">In the **Translated text** field, enter the text.</span></span>
    5.  <span data-ttu-id="82cfa-192">Hægt er að sérsníða texta með því að færa inn staðgengla.</span><span class="sxs-lookup"><span data-stu-id="82cfa-192">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="82cfa-193">Sjá skref 5 til að fá leiðbeiningar um hvernig á að færa inn staðgengill.</span><span class="sxs-lookup"><span data-stu-id="82cfa-193">For instructions about how to enter a placeholder, see step 5.</span></span>
    6.  <span data-ttu-id="82cfa-194">Smellið á **Loka**.</span><span class="sxs-lookup"><span data-stu-id="82cfa-194">Click **Close**.</span></span>

7.  <span data-ttu-id="82cfa-195">Á **Viðtakanda** flipanum skal nota eftirfarandi valkosti til að tilgreina hver eigi að fá tilkynningar.</span><span class="sxs-lookup"><span data-stu-id="82cfa-195">On the **Recipient** tab, use the following options to specify who should receive the notifications.</span></span>
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="82cfa-196">Valkostur</span><span class="sxs-lookup"><span data-stu-id="82cfa-196">Option</span></span></th>
    <th><span data-ttu-id="82cfa-197">Tilkynningar eru sendar þessum notendum.</span><span class="sxs-lookup"><span data-stu-id="82cfa-197">Notifications are sent to these users</span></span></th>
    <th><span data-ttu-id="82cfa-198">Fylgið eftirfarandi skrefum til að senda tilkynningar,</span><span class="sxs-lookup"><span data-stu-id="82cfa-198">To send notifications, follow these steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="82cfa-199">Þátttakendur</span><span class="sxs-lookup"><span data-stu-id="82cfa-199">Participant</span></span></td>
    <td><span data-ttu-id="82cfa-200">Notendur sem tilheyra tilteknum hópi eða hlutverki</span><span class="sxs-lookup"><span data-stu-id="82cfa-200">Users who are assigned to a specific group or role</span></span></td>
    <td><ol>
    <li><span data-ttu-id="82cfa-201">Á <strong>Viðtakanda</strong> flipanum, smellið <strong>Þátttakanda</strong>.</span><span class="sxs-lookup"><span data-stu-id="82cfa-201">On the <strong>Recipient</strong> tab, click <strong>Participant</strong>.</span></span></li>
    <li><span data-ttu-id="82cfa-202">Á flipanum <strong>Hlutverkamiðað</strong> , á listanum <strong>Gerð þátttakanda</strong> skal velja gerð hóps eða hlutverks til að senda tilkynningu á.</span><span class="sxs-lookup"><span data-stu-id="82cfa-202">On the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="82cfa-203">Í listanum <strong>Þátttakanda</strong> skal velja hópi eða hlutverk til að senda tilkynningar til.</span><span class="sxs-lookup"><span data-stu-id="82cfa-203">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="82cfa-204">Verkflæðisnotandi</span><span class="sxs-lookup"><span data-stu-id="82cfa-204">Workflow user</span></span></td>
    <td><span data-ttu-id="82cfa-205">Notendur sem eru þáttakendur í þessu verkflæði</span><span class="sxs-lookup"><span data-stu-id="82cfa-205">Users who are participants in this workflow</span></span></td>
    <td><ol>
    <li><span data-ttu-id="82cfa-206">Á <strong>Viðtakanda</strong> flipanum, smellið <strong>verkflæðisnotandi</strong>.</span><span class="sxs-lookup"><span data-stu-id="82cfa-206">On the <strong>Recipient</strong> tab, click <strong>Workflow user</strong>.</span></span></li>
    <li><span data-ttu-id="82cfa-207">Á <strong>verkflæðisnotandi </strong> flipanum, á <strong>verkflæðisnotandi </strong>listanum, veldu notandann sem tekur þátt í verkflæði.</span><span class="sxs-lookup"><span data-stu-id="82cfa-207">On the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a participant in this workflow.</span></span></li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="82cfa-208">Notandi</span><span class="sxs-lookup"><span data-stu-id="82cfa-208">User</span></span></td>
    <td><span data-ttu-id="82cfa-209">Sértækir notendur Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="82cfa-209">Specific Finance and Operations users</span></span></td>
    <td><ol>
    <li><span data-ttu-id="82cfa-210">Á <strong>Viðtakanda</strong> flipanum, smellið <strong>notandi</strong>.</span><span class="sxs-lookup"><span data-stu-id="82cfa-210">On the <strong>Recipient</strong> tab, click <strong>User</strong>.</span></span></li>
    <li><span data-ttu-id="82cfa-211">Á flipanum <strong>Notendur</strong> inniheldur listinn <strong>Tiltækir notendur</strong> alla notendur í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="82cfa-211">On the <strong>User</strong> tab, the <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="82cfa-212">Veldu Notendur til að senda tilkynningar á , og færðu síðan þessa notendur í <strong>Valdir notendur</strong> lista.</span><span class="sxs-lookup"><span data-stu-id="82cfa-212">Select the users to send notifications to, and move those users into the <strong>Selected users</strong> list.</span></span></li>
    </ol></td>
    </tr>
    </tbody>
    </table>

8.  <span data-ttu-id="82cfa-213">Endurtakið skref 3 til 7 hvert tilvik sem valin var í skrefi 2.</span><span class="sxs-lookup"><span data-stu-id="82cfa-213">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="enter-comments-about-the-changes-that-you-made-to-the-workflow"></a><span data-ttu-id="82cfa-214">Færðu inn athugasemdir um þær breytingar sem þú hefur gert á verkflæðinu.</span><span class="sxs-lookup"><span data-stu-id="82cfa-214">Enter comments about the changes that you made to the workflow</span></span>
<span data-ttu-id="82cfa-215">Til að færa inn athugasemdir um þær breytingar sem þú hefur gert á verkflæðinu, fylgdu þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="82cfa-215">To enter comments about the changes that you made to the workflow, follow these steps.</span></span>

1.  <span data-ttu-id="82cfa-216">Á vinstra svæðinu er smellt á **Athugasemdir**.</span><span class="sxs-lookup"><span data-stu-id="82cfa-216">In the left pane, click **Notes**.</span></span>
2.  <span data-ttu-id="82cfa-217">Í svæðinu **færa Inn athugasemdir um verkflæðið** , færið inn athugasemdir.</span><span class="sxs-lookup"><span data-stu-id="82cfa-217">In the **Enter comments about the workflow** field, enter your comments.</span></span>
3.  <span data-ttu-id="82cfa-218">Farðu aftur yfir Athugasemdir þitt.</span><span class="sxs-lookup"><span data-stu-id="82cfa-218">Review your comments.</span></span> <span data-ttu-id="82cfa-219">Þegar búið er að bæta við athugasemd er ekki hægt að breyta henni.</span><span class="sxs-lookup"><span data-stu-id="82cfa-219">After you add comments, you can't modify them.</span></span>
4.  <span data-ttu-id="82cfa-220">Smellið á **Bæta við** til að bæta athugasemdir við **ferill Athugasemda** svæði.</span><span class="sxs-lookup"><span data-stu-id="82cfa-220">Click **Add** to add your comments to the **Comment history** area.</span></span>





