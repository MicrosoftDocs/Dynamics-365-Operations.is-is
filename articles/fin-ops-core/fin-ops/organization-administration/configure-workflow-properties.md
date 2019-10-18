---
title: Skilgreining verkflæðiseiginleika
description: Þetta efnisatriði útskýrir hvernig skilgreina á mismunandi eiginleika verkflæðis.
author: sericks007
manager: AnnBe
ms.date: 07/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 196083
ms.assetid: 192b7a98-7d04-4c7a-a986-29d797a8a837
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 76d44c472989a73d71c2edd19f1187ecd09827ae
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2190121"
---
# <a name="configure-workflow-properties"></a><span data-ttu-id="2049c-103">Skilgreining verkflæðiseiginleika</span><span class="sxs-lookup"><span data-stu-id="2049c-103">Configure workflow properties</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2049c-104">Þetta efnisatriði útskýrir hvernig skilgreina á mismunandi eiginleika verkflæðis.</span><span class="sxs-lookup"><span data-stu-id="2049c-104">This topic explains how to configure the various properties of a workflow.</span></span>

<span data-ttu-id="2049c-105">Opna verkflæðið í verkflæðisritlinum til að skilgreina eiginleika verkflæðis.</span><span class="sxs-lookup"><span data-stu-id="2049c-105">To configure the properties of a workflow, open the workflow in the workflow editor.</span></span> <span data-ttu-id="2049c-106">Smellið á vinnusvæði verkflæðisritlinum, og smellið síðan á **Eiginleika** til að opna **Eiginleika** síðu.</span><span class="sxs-lookup"><span data-stu-id="2049c-106">Click the canvas of the workflow editor, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="2049c-107">Notið síðan eftirfarandi ferli til að stilla mismunandi eiginleika fyrir verkflæðið.</span><span class="sxs-lookup"><span data-stu-id="2049c-107">You can then use the following procedures to configure the various properties of the workflow.</span></span>

## <a name="name-the-workflow"></a><span data-ttu-id="2049c-108">Verkflæðinu er gefið heiti</span><span class="sxs-lookup"><span data-stu-id="2049c-108">Name the workflow</span></span>

<span data-ttu-id="2049c-109">Fylgið þessum skrefum til að færa inn heiti á verkflæðinu.</span><span class="sxs-lookup"><span data-stu-id="2049c-109">Follow these steps to enter a name for the workflow.</span></span>

1. <span data-ttu-id="2049c-110">Í vinstri glugganum, smelltu á **grunnstillingar**.</span><span class="sxs-lookup"><span data-stu-id="2049c-110">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="2049c-111">Á svæðinu **Heiti** skal færa inn einkvæmt heiti fyrir Verkflæðið</span><span class="sxs-lookup"><span data-stu-id="2049c-111">In the **Name** field, enter a unique name for the workflow.</span></span> <span data-ttu-id="2049c-112">Til dæmis, gefum okkur að stofna ætti verkflæði innkaupabeiðna fyrir hvert land eða svæði starfseminnar, gefa mætti verkflæði innkaupabeiðninnar heitið **Innkaupabeiðni Danmörk** eða **Innkaupabeiðni Spánn**.</span><span class="sxs-lookup"><span data-stu-id="2049c-112">For example, if you create a purchase requisition workflow for each country/region that you operate in, you can name the purchase requisition workflow **Purchase Requisitions Denmark** or **Purchase Requisitions Spain**.</span></span>

## <a name="specify-the-workflow-owner"></a><span data-ttu-id="2049c-113">Tilgreinið eiganda verkflæðis</span><span class="sxs-lookup"><span data-stu-id="2049c-113">Specify the workflow owner</span></span>

<span data-ttu-id="2049c-114">Eigandi verkflæðis er sá aðili sem stjórnar og viðheldur verkflæðinu.</span><span class="sxs-lookup"><span data-stu-id="2049c-114">The workflow owner is the person who manages and maintains the workflow.</span></span> <span data-ttu-id="2049c-115">Fylgið skrefum ef tilgreina á eiganda verkflæðis.</span><span class="sxs-lookup"><span data-stu-id="2049c-115">Follow these steps to specify the workflow owner.</span></span>

1. <span data-ttu-id="2049c-116">Í vinstri glugganum, smelltu á **grunnstillingar**.</span><span class="sxs-lookup"><span data-stu-id="2049c-116">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="2049c-117">Á listanum **Eigandi** skal velja nafn þess aðila sem á að stjórna verkflæðinu.</span><span class="sxs-lookup"><span data-stu-id="2049c-117">In the **Owner** list, select the name of the person who will manage the workflow.</span></span>

## <a name="select-an-email-template"></a><span data-ttu-id="2049c-118">Velja tölvupóstssniðmát</span><span class="sxs-lookup"><span data-stu-id="2049c-118">Select an email template</span></span>

<span data-ttu-id="2049c-119">Fylgið eftirfarandi skrefum til að velja sniðmát fyrir tölvupóst sem er notuð til að mynda skilaboð tilkynningar um verkflæðið.</span><span class="sxs-lookup"><span data-stu-id="2049c-119">Follow these steps to select the email template that is used to generate notification messages about the workflow.</span></span>

1. <span data-ttu-id="2049c-120">Í vinstri glugganum, smelltu á **grunnstillingar**.</span><span class="sxs-lookup"><span data-stu-id="2049c-120">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="2049c-121">Í **sniðmát fyrir Tölvupóst fyrir verkflæðistilkynningar** skal velja sniðmát.</span><span class="sxs-lookup"><span data-stu-id="2049c-121">In the **Email template for workflow notifications** list, select the template.</span></span>

## <a name="enter-instructions-for-users"></a><span data-ttu-id="2049c-122">Færa skal inn notendaleiðbeiningar</span><span class="sxs-lookup"><span data-stu-id="2049c-122">Enter instructions for users</span></span>

<span data-ttu-id="2049c-123">Hægt er að veita þeim notendum leiðbeiningar sem senda skjöl til vinnslu og samþykktar.</span><span class="sxs-lookup"><span data-stu-id="2049c-123">You can provide instructions to users who submit documents for processing and approval.</span></span> <span data-ttu-id="2049c-124">Þessar Notendur eru einnig nefndar *upphafsmenn*.</span><span class="sxs-lookup"><span data-stu-id="2049c-124">These users are also referred to as *originators*.</span></span> <span data-ttu-id="2049c-125">Gefum okkur til dæmis að verið sé að búa til verkflæði fyrir innkaupabeiðni, og þú færir inn leiðbeiningar.</span><span class="sxs-lookup"><span data-stu-id="2049c-125">For example, you're creating a purchase requisition workflow, and you enter instructions.</span></span> <span data-ttu-id="2049c-126">Notendur sem færa inn innkaupabeiðnir geta skoðað leiðbeiningar á síðunni **Innkaupabeiðnir** .</span><span class="sxs-lookup"><span data-stu-id="2049c-126">Those instructions can then be viewed by users who enter purchase requisitions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="2049c-127">TIL að skoða leiðbeiningarnar, smellir upphafsmaðurinn á táknið á skilaboðastikunni.</span><span class="sxs-lookup"><span data-stu-id="2049c-127">To view instructions, the originator clicks the icon in the workflow message bar.</span></span> <span data-ttu-id="2049c-128">Fylgið eftirfarandi skrefum til að bæta við leiðbeiningum fyrir notendur.</span><span class="sxs-lookup"><span data-stu-id="2049c-128">Follow these steps to enter instructions for users.</span></span>

1. <span data-ttu-id="2049c-129">Í vinstri glugganum, smelltu á **grunnstillingar**.</span><span class="sxs-lookup"><span data-stu-id="2049c-129">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="2049c-130">Í **leiðbeiningar við framlagningu** svæðinu, færið inn leiðbeiningar.</span><span class="sxs-lookup"><span data-stu-id="2049c-130">In the **Submission instructions** field, enter the instructions.</span></span>
3. <span data-ttu-id="2049c-131">Hægt er að sérsníða leiðbeiningarnar með því að færa inn staðgengla.</span><span class="sxs-lookup"><span data-stu-id="2049c-131">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="2049c-132">Staðgenglar eru settir í stað viðeigandi gagna þegar leiðbeiningar birtist notendum.</span><span class="sxs-lookup"><span data-stu-id="2049c-132">Placeholders are replaced with the appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="2049c-133">Fylgið eftirfarandi skrefum til að færa inn staðgengil:</span><span class="sxs-lookup"><span data-stu-id="2049c-133">To insert a placeholder, follow these steps:</span></span>

    1. <span data-ttu-id="2049c-134">Smellið á **leiðbeiningar við framlagningu** til þess að tilgreina hvar staðgengill á að birtast.</span><span class="sxs-lookup"><span data-stu-id="2049c-134">Click in the **Submission instructions** field to specify where the placeholder should appear.</span></span>
    2. <span data-ttu-id="2049c-135">Smella á **Setja inn staðgengil**</span><span class="sxs-lookup"><span data-stu-id="2049c-135">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="2049c-136">Í listanum sem birtist skal velja staðgengilinn til að setja inn.</span><span class="sxs-lookup"><span data-stu-id="2049c-136">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="2049c-137">Smellt er á **Setja inn**.</span><span class="sxs-lookup"><span data-stu-id="2049c-137">Click **Insert**.</span></span>

4. <span data-ttu-id="2049c-138">Til að bæta þýðingum við leiðbeiningar skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="2049c-138">To add translations of the instructions, follow these steps:</span></span>

    1. <span data-ttu-id="2049c-139">Smellt er á **Þýðingar**.</span><span class="sxs-lookup"><span data-stu-id="2049c-139">Click **Translations**.</span></span>
    2. <span data-ttu-id="2049c-140">Á síðunni sem birtist er smellt á **bæta við**.</span><span class="sxs-lookup"><span data-stu-id="2049c-140">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="2049c-141">Í listanum sem birtist skal velja tungumálið sem á að færa inn í textanum.</span><span class="sxs-lookup"><span data-stu-id="2049c-141">In the list that appears, select the language that you will enter the text in.</span></span>
    4. <span data-ttu-id="2049c-142">Í svæðið **þýddur texti** skal færa inn textann.</span><span class="sxs-lookup"><span data-stu-id="2049c-142">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="2049c-143">Hægt er að sérsníða texta með því að færa inn staðgengla.</span><span class="sxs-lookup"><span data-stu-id="2049c-143">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="2049c-144">Sjá skref 3 til að fá leiðbeiningar um hvernig á að færa inn staðgengill.</span><span class="sxs-lookup"><span data-stu-id="2049c-144">For instructions about how to enter a placeholder, see step 3.</span></span>
    6. <span data-ttu-id="2049c-145">Smellið á **Loka**.</span><span class="sxs-lookup"><span data-stu-id="2049c-145">Click **Close**.</span></span>

## <a name="specify-when-this-workflow-is-used"></a><span data-ttu-id="2049c-146">Tilgreina skal hvenær á að nota þetta verkflæði</span><span class="sxs-lookup"><span data-stu-id="2049c-146">Specify when this workflow is used</span></span>

<span data-ttu-id="2049c-147">Hægt er að stofna mörg verkflæði á grundvelli sama gerð.</span><span class="sxs-lookup"><span data-stu-id="2049c-147">You can create multiple workflows that are based on the same type.</span></span> <span data-ttu-id="2049c-148">Til dæmis er hægt að stofna innkaupabeiðniverkflæði fyrir hvert land eða svæði starfseminnar, eins og Innkaupabeiðni Danmörk og Innkaupabeiðni Spánn.</span><span class="sxs-lookup"><span data-stu-id="2049c-148">For example, you can create a purchase requisition workflow for each country/region that you operate in, such as Purchase Requisitions Denmark and Purchase Requisitions Spain.</span></span> <span data-ttu-id="2049c-149">Þegar búið er að stofna mörg verkflæði á grundvelli sama gerðar, verður að tilgreina hvenær á nota hvert verkflæði.</span><span class="sxs-lookup"><span data-stu-id="2049c-149">When you have multiple workflows that are based on the same type, you must specify when each workflow is used.</span></span> <span data-ttu-id="2049c-150">Fyrir dæmið hér á undan, tilgreinið eftirfarandi skilyrði:</span><span class="sxs-lookup"><span data-stu-id="2049c-150">For the preceding example, you specify the following conditions:</span></span>

- <span data-ttu-id="2049c-151">Innkaupabeiðni Danmörk er notað þegar: landið/svæðið er = DK.</span><span class="sxs-lookup"><span data-stu-id="2049c-151">Purchase Requisitions Denmark is used when: country/region = DK</span></span>
- <span data-ttu-id="2049c-152">Innkaupabeiðni spánn er notað þegar: landið/svæðið er = ES.</span><span class="sxs-lookup"><span data-stu-id="2049c-152">Purchase Requisitions Spain is used when: country/region = ES</span></span>

<span data-ttu-id="2049c-153">Fylgið eftirfarandi skrefum til að tilgreina hvenær á að nota skilgreint verkflæði.</span><span class="sxs-lookup"><span data-stu-id="2049c-153">Follow these steps to specify when the workflow that you're configuring is used.</span></span>

1. <span data-ttu-id="2049c-154">Á vinstra svæðinu er smellt á **virkja**.</span><span class="sxs-lookup"><span data-stu-id="2049c-154">In the left pane, click **Activation**.</span></span>
2. <span data-ttu-id="2049c-155">Veldu gátreitinn **Tilgreina skilyrði fyrir keyrslu verkflæðisins**</span><span class="sxs-lookup"><span data-stu-id="2049c-155">Select the **Set the conditions for running this workflow** check box.</span></span>
3. <span data-ttu-id="2049c-156">Smellt er á **Bæta við Skilyrði**.</span><span class="sxs-lookup"><span data-stu-id="2049c-156">Click **Add condition**.</span></span>
4. <span data-ttu-id="2049c-157">Færið inn skilyrði.</span><span class="sxs-lookup"><span data-stu-id="2049c-157">Enter a condition.</span></span>
5. <span data-ttu-id="2049c-158">Færið inn öll önnur skilyrði sem krafist er.</span><span class="sxs-lookup"><span data-stu-id="2049c-158">Enter any additional conditions that are required.</span></span>
6. <span data-ttu-id="2049c-159">Til að sannreyna að skilyrðin sem voru færð hafi verið stilllt rétt, skal fylgja eftirfarandi skrefum:</span><span class="sxs-lookup"><span data-stu-id="2049c-159">To verify that the conditions that you entered are set correctly, follow these steps:</span></span>

    1. <span data-ttu-id="2049c-160">Smellið á **Prófun**.</span><span class="sxs-lookup"><span data-stu-id="2049c-160">Click **Test**.</span></span>
    2. <span data-ttu-id="2049c-161">Á síðunni **Kanna verkflæðisskilyrði** , í **Villuleita skilyrði** svæði, velja færslu.</span><span class="sxs-lookup"><span data-stu-id="2049c-161">On the **Test workflow condition** page, in the **Validate condition** area, select a record.</span></span>
    3. <span data-ttu-id="2049c-162">Smellið á **Prófun**.</span><span class="sxs-lookup"><span data-stu-id="2049c-162">Click **Test**.</span></span> <span data-ttu-id="2049c-163">Kerfið metur færsluna og ákveður hvort hún standist skilyrði sem þú skilgreindir.</span><span class="sxs-lookup"><span data-stu-id="2049c-163">The system evaluates the record to determine whether it meets the conditions that you specified.</span></span> <span data-ttu-id="2049c-164">Til dæmis, ef verið er að búa til verkflæði fyrir innkaupabeiðni á Spáni sýnir svæðið **Villuleita skilyrði** á síðunni lista yfir innkaupabeiðnir.</span><span class="sxs-lookup"><span data-stu-id="2049c-164">For example, if you're creating a purchase requisition workflow for Spain, the **Validate condition** area of the page shows a list of purchase requisitions.</span></span> <span data-ttu-id="2049c-165">Þegar smellt er á **Prófun** mun kerfið meta valdar innkaupabeiðnir og ákveða hvort Land/svæði er ES.</span><span class="sxs-lookup"><span data-stu-id="2049c-165">When you click **Test**, the system evaluates the selected purchase requisition to determine whether the country/region is ES.</span></span>
    4. <span data-ttu-id="2049c-166">Smelltu á **Í lagi** eða **hætta við** til að fara aftur síðuna **forstillingar**.</span><span class="sxs-lookup"><span data-stu-id="2049c-166">Click **OK** or **Cancel** to return to the **Properties** page.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="2049c-167">Tilgreinið hvenær tilkynningar eru sendar út</span><span class="sxs-lookup"><span data-stu-id="2049c-167">Specify when notifications are sent</span></span>

<span data-ttu-id="2049c-168">Þegar skjal er sent í vinnslu þá er verkflæðistilvik stofnað.</span><span class="sxs-lookup"><span data-stu-id="2049c-168">When a document is submitted for processing, a workflow instance is created.</span></span> <span data-ttu-id="2049c-169">Hægt er að senda tilkynningar til notenda þegar verkflæðistilvik á grundvelli verkflæðisins, eru sett af stað, lokið við þau, eytt, eða þau stöðvuð út af villu.</span><span class="sxs-lookup"><span data-stu-id="2049c-169">You can send notifications to users when workflow instances that are based on the workflow are started, completed, terminated, or stopped because of an error.</span></span> <span data-ttu-id="2049c-170">Fylgið eftirfarandi skrefum til að tilgreina hvenær senda á út tilkynningar.</span><span class="sxs-lookup"><span data-stu-id="2049c-170">Follow these steps to specify when notifications are sent.</span></span>

1. <span data-ttu-id="2049c-171">Á svæðinu vinstra megin, smella á **tilkynningar**.</span><span class="sxs-lookup"><span data-stu-id="2049c-171">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="2049c-172">Veljið gátreit fyrir hvert tilvik sem á að virkja tilkynningar:</span><span class="sxs-lookup"><span data-stu-id="2049c-172">Select the check box for each event that should trigger notifications:</span></span>

    - <span data-ttu-id="2049c-173">**Byrjað** — senda út tilkynningar þegar byrjað er á verkflæðistilviki.</span><span class="sxs-lookup"><span data-stu-id="2049c-173">**Started** – Send notifications when a workflow instance is started.</span></span>
    - <span data-ttu-id="2049c-174">**Stöðvað (villa)** — senda út tilkynningar þegar verkflæðistilvik hefur verið stöðvað út af villu.</span><span class="sxs-lookup"><span data-stu-id="2049c-174">**Stopped** – Send notifications when a workflow instance is stopped because of an error.</span></span>
    - <span data-ttu-id="2049c-175">**Byrjað** — senda út tilkynningar þegar verkflæðistilviki er lokið.</span><span class="sxs-lookup"><span data-stu-id="2049c-175">**Completed** – Send notifications when a workflow instance is completed.</span></span>
    - <span data-ttu-id="2049c-176">**Óafturkræft** — senda út tilkynningar þegar verkflæðistilvik hefur verið stöðvað út af óafturkræfri villu.</span><span class="sxs-lookup"><span data-stu-id="2049c-176">**Unrecoverable** – Send notifications when a workflow instance is stopped because of an unrecoverable error.</span></span>
    - <span data-ttu-id="2049c-177">**Slitið** — senda út tilkynningar þegar verkflæðistilviki er slitið.</span><span class="sxs-lookup"><span data-stu-id="2049c-177">**Terminated** – Send notifications when a workflow instance is terminated.</span></span>

3. <span data-ttu-id="2049c-178">Veljið línu fyrir tilvik sem þú valdir í skrefi 2.</span><span class="sxs-lookup"><span data-stu-id="2049c-178">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="2049c-179">Á **tilkynningartexti** flipanum í textareitinn, færa inn texta tilkynningarinnar.</span><span class="sxs-lookup"><span data-stu-id="2049c-179">On the **Notification text** tab, enter the text of the notification.</span></span>
5. <span data-ttu-id="2049c-180">Hægt er að sérsníða texta með því að færa inn staðgengla.</span><span class="sxs-lookup"><span data-stu-id="2049c-180">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="2049c-181">Staðgenglar eru settir í stað viðeigandi gagna þegar textinn birtist notendum.</span><span class="sxs-lookup"><span data-stu-id="2049c-181">Placeholders are replaced with the appropriate data when the text is shown to users.</span></span> <span data-ttu-id="2049c-182">Fylgið eftirfarandi skrefum til að færa inn staðgengil:</span><span class="sxs-lookup"><span data-stu-id="2049c-182">To insert a placeholder, follow these steps:</span></span>

    1. <span data-ttu-id="2049c-183">Smellið á reit til þess að tilgreina hvar staðgengill á að birtast.</span><span class="sxs-lookup"><span data-stu-id="2049c-183">Click in the field to specify where the placeholder should appear.</span></span>
    2. <span data-ttu-id="2049c-184">Smella á **Setja inn staðgengil**</span><span class="sxs-lookup"><span data-stu-id="2049c-184">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="2049c-185">Í listanum sem birtist skal velja staðgengilinn til að setja inn.</span><span class="sxs-lookup"><span data-stu-id="2049c-185">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="2049c-186">Smellt er á **Setja inn**.</span><span class="sxs-lookup"><span data-stu-id="2049c-186">Click **Insert**.</span></span>
    5. <span data-ttu-id="2049c-187">Algengur staðgengilstexti fyrir **Tilkynningatexti** til að hafa með er „Last Notes: %Workflow.Last note%“, sem birtir allar athugasemdir frá fyrra skrefi.</span><span class="sxs-lookup"><span data-stu-id="2049c-187">A common **Notification text** placeholder to include is "Last Notes: %Workflow.Last note%", which displays any comments from the previous step.</span></span>

6. <span data-ttu-id="2049c-188">Til að bæta þýðingum við textann, skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="2049c-188">To add translations of the text, follow these steps:</span></span>

    1. <span data-ttu-id="2049c-189">Smellt er á **Þýðingar**.</span><span class="sxs-lookup"><span data-stu-id="2049c-189">Click **Translations**.</span></span>
    2. <span data-ttu-id="2049c-190">Á síðunni sem birtist er smellt á **bæta við**.</span><span class="sxs-lookup"><span data-stu-id="2049c-190">On the page that appears, Click **Add**.</span></span>
    3. <span data-ttu-id="2049c-191">Í listanum sem birtist skal velja tungumálið sem á að færa inn í textanum.</span><span class="sxs-lookup"><span data-stu-id="2049c-191">In the list that appears, select the language that you will enter the text in.</span></span>
    4. <span data-ttu-id="2049c-192">Í svæðið **þýddur texti** skal færa inn textann.</span><span class="sxs-lookup"><span data-stu-id="2049c-192">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="2049c-193">Hægt er að sérsníða texta með því að færa inn staðgengla.</span><span class="sxs-lookup"><span data-stu-id="2049c-193">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="2049c-194">Sjá skref 5 til að fá leiðbeiningar um hvernig á að færa inn staðgengill.</span><span class="sxs-lookup"><span data-stu-id="2049c-194">For instructions about how to enter a placeholder, see step 5.</span></span>
    6. <span data-ttu-id="2049c-195">Smellið á **Loka**.</span><span class="sxs-lookup"><span data-stu-id="2049c-195">Click **Close**.</span></span>

7. <span data-ttu-id="2049c-196">Á **Viðtakanda** flipanum skal nota eftirfarandi valkosti til að tilgreina hver eigi að fá tilkynningar.</span><span class="sxs-lookup"><span data-stu-id="2049c-196">On the **Recipient** tab, use the following options to specify who should receive the notifications.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="2049c-197">Valkostur</span><span class="sxs-lookup"><span data-stu-id="2049c-197">Option</span></span></th>
    <th><span data-ttu-id="2049c-198">Tilkynningar eru sendar þessum notendum.</span><span class="sxs-lookup"><span data-stu-id="2049c-198">Notifications are sent to these users</span></span></th>
    <th><span data-ttu-id="2049c-199">Fylgið eftirfarandi skrefum til að senda tilkynningar,</span><span class="sxs-lookup"><span data-stu-id="2049c-199">To send notifications, follow these steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="2049c-200">Þátttakendur</span><span class="sxs-lookup"><span data-stu-id="2049c-200">Participant</span></span></td>
    <td><span data-ttu-id="2049c-201">Notendur sem tilheyra tilteknum hópi eða hlutverki</span><span class="sxs-lookup"><span data-stu-id="2049c-201">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="2049c-202">Á <strong>Viðtakanda</strong> flipanum, smellið <strong>Þátttakanda</strong>.</span><span class="sxs-lookup"><span data-stu-id="2049c-202">On the <strong>Recipient</strong> tab, click <strong>Participant</strong>.</span></span></li>
    <li><span data-ttu-id="2049c-203">Á flipanum <strong>Hlutverkamiðað</strong> , á listanum <strong>Gerð þátttakanda</strong> skal velja gerð hóps eða hlutverks til að senda tilkynningu á.</span><span class="sxs-lookup"><span data-stu-id="2049c-203">On the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="2049c-204">Í listanum <strong>Þátttakanda</strong> skal velja hópi eða hlutverk til að senda tilkynningar til.</span><span class="sxs-lookup"><span data-stu-id="2049c-204">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="2049c-205">Verkflæðisnotandi</span><span class="sxs-lookup"><span data-stu-id="2049c-205">Workflow user</span></span></td>
    <td><span data-ttu-id="2049c-206">Notendur sem eru þáttakendur í þessu verkflæði</span><span class="sxs-lookup"><span data-stu-id="2049c-206">Users who are participants in this workflow</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="2049c-207">Á <strong>Viðtakanda</strong> flipanum, smellið <strong>verkflæðisnotandi</strong>.</span><span class="sxs-lookup"><span data-stu-id="2049c-207">On the <strong>Recipient</strong> tab, click <strong>Workflow user</strong>.</span></span></li>
    <li><span data-ttu-id="2049c-208">Á flipanum <strong>verkflæðisnotandi</strong>, á listanum <strong>verkflæðisnotandi</strong>, veldu notandann sem tekur þátt í verkflæði.</span><span class="sxs-lookup"><span data-stu-id="2049c-208">On the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a participant in this workflow.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="2049c-209">Notandi</span><span class="sxs-lookup"><span data-stu-id="2049c-209">User</span></span></td>
    <td><span data-ttu-id="2049c-210">Tilteknir notendur</span><span class="sxs-lookup"><span data-stu-id="2049c-210">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="2049c-211">Á <strong>Viðtakanda</strong> flipanum, smellið <strong>notandi</strong>.</span><span class="sxs-lookup"><span data-stu-id="2049c-211">On the <strong>Recipient</strong> tab, click <strong>User</strong>.</span></span></li>
    <li><span data-ttu-id="2049c-212">Á flitapnum <strong>notendur</strong> inniheldur listinn <strong>Tiltækir notendur</strong> alla notendur.</span><span class="sxs-lookup"><span data-stu-id="2049c-212">On the <strong>User</strong> tab, the <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="2049c-213">Veldu Notendur til að senda tilkynningar á , og færðu síðan þessa notendur í <strong>Valdir notendur</strong> lista.</span><span class="sxs-lookup"><span data-stu-id="2049c-213">Select the users to send notifications to, and move those users into the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. <span data-ttu-id="2049c-214">Endurtakið skref 3 til 7 hvert tilvik sem valin var í skrefi 2.</span><span class="sxs-lookup"><span data-stu-id="2049c-214">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="enter-comments-about-the-changes-that-you-made-to-the-workflow"></a><span data-ttu-id="2049c-215">Færðu inn athugasemdir um þær breytingar sem þú hefur gert á verkflæðinu.</span><span class="sxs-lookup"><span data-stu-id="2049c-215">Enter comments about the changes that you made to the workflow</span></span>

<span data-ttu-id="2049c-216">Til að færa inn athugasemdir um þær breytingar sem þú hefur gert á verkflæðinu, fylgdu þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="2049c-216">To enter comments about the changes that you made to the workflow, follow these steps.</span></span>

1. <span data-ttu-id="2049c-217">Á vinstra svæðinu er smellt á **Athugasemdir**.</span><span class="sxs-lookup"><span data-stu-id="2049c-217">In the left pane, click **Notes**.</span></span>
2. <span data-ttu-id="2049c-218">Í svæðinu **færa Inn athugasemdir um verkflæðið** , færið inn athugasemdir.</span><span class="sxs-lookup"><span data-stu-id="2049c-218">In the **Enter comments about the workflow** field, enter your comments.</span></span>
3. <span data-ttu-id="2049c-219">Farðu aftur yfir Athugasemdir þitt.</span><span class="sxs-lookup"><span data-stu-id="2049c-219">Review your comments.</span></span> <span data-ttu-id="2049c-220">Þegar búið er að bæta við athugasemd er ekki hægt að breyta henni.</span><span class="sxs-lookup"><span data-stu-id="2049c-220">After you add comments, you can't modify them.</span></span>
4. <span data-ttu-id="2049c-221">Smellið á **Bæta við** til að bæta athugasemdir við **ferill Athugasemda** svæði.</span><span class="sxs-lookup"><span data-stu-id="2049c-221">Click **Add** to add your comments to the **Comment history** area.</span></span>
