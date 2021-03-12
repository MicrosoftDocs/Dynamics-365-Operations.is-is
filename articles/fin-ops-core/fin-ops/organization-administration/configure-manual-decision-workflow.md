---
title: Skilgreina handvirkar ákvarðanir í verkflæði
description: Þetta efnisatriði útskýrir hvernig skilgreina á eiginleika handvirkrar ákvörðunar.
author: ChrisGarty
manager: AnnBe
ms.date: 06/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 192101
ms.assetid: 0bccad77-1a44-4f08-967b-12c62c02afc7
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d351facbce02355ddb4bdf91d43d9df561e4f3b5
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/19/2020
ms.locfileid: "4798853"
---
# <a name="configure-manual-decisions-in-a-workflow"></a><span data-ttu-id="23b5c-103">Skilgreina handvirkar ákvarðanir í verkflæði</span><span class="sxs-lookup"><span data-stu-id="23b5c-103">Configure manual decisions in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="23b5c-104">Þetta efnisatriði útskýrir hvernig skilgreina á eiginleika handvirkrar ákvörðunar.</span><span class="sxs-lookup"><span data-stu-id="23b5c-104">This topic explains how to configure the properties of a manual decision.</span></span>

<span data-ttu-id="23b5c-105">Til að skilgreina handvirka ákvörðun í verkflæðisritlinum, hægrismellt er á handvirk ákvörðun og smellið síðan á **Eiginleika** til að opna **Eiginleika** síðu.</span><span class="sxs-lookup"><span data-stu-id="23b5c-105">To configure a manual decision in the workflow editor, right-click the manual decision, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="23b5c-106">Notið síðan eftirfarandi ferli til að stilla eiginleika fyrir handvirk ákvörðun.</span><span class="sxs-lookup"><span data-stu-id="23b5c-106">Then use the following procedures to configure the properties of the manual decision.</span></span>

## <a name="name-the-decision"></a><span data-ttu-id="23b5c-107">Heiti ákvörðunar.</span><span class="sxs-lookup"><span data-stu-id="23b5c-107">Name the decision</span></span>

<span data-ttu-id="23b5c-108">Fylgið þessum skrefum til að færa inn heiti á handvirk ákvörðun.</span><span class="sxs-lookup"><span data-stu-id="23b5c-108">Follow these steps to enter a name for the manual decision.</span></span>

1. <span data-ttu-id="23b5c-109">Í vinstri glugganum, smelltu á **grunnstillingar**.</span><span class="sxs-lookup"><span data-stu-id="23b5c-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="23b5c-110">Á svæðinu **Heiti** skal færa inn einkvæmt heiti fyrir handvirk ákvörðun</span><span class="sxs-lookup"><span data-stu-id="23b5c-110">In the **Name** field, enter a unique name for the manual decision.</span></span>

## <a name="enter-a-subject-line-and-instructions"></a><span data-ttu-id="23b5c-111">Slá inn efnislínu og fyrirmæli</span><span class="sxs-lookup"><span data-stu-id="23b5c-111">Enter a subject line and instructions</span></span>

<span data-ttu-id="23b5c-112">Veita verður þeim notendum, sem úthlutað er þetta handvirk ákvörðun, efnislínu og fyrirmæli.</span><span class="sxs-lookup"><span data-stu-id="23b5c-112">You must provide a subject line and instructions to users who are assigned to the manual decision.</span></span> <span data-ttu-id="23b5c-113">Til dæmis, ef verið er að skilgreina ákvörðun fyrir innkaupabeiðnir, mun notanda sem er úthlutað á ákvörðun sjá efnislínuna og fyrirmælin á **Innkaupabeiðnir** síðunni.</span><span class="sxs-lookup"><span data-stu-id="23b5c-113">For example, if you're configuring a decision for purchase requisitions, the user who is assigned to the decision sees the subject line and instructions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="23b5c-114">Efnislínuna birtist á skilaboðaslánni á síðunni.</span><span class="sxs-lookup"><span data-stu-id="23b5c-114">The subject line appears in a message bar on the page.</span></span> <span data-ttu-id="23b5c-115">Notandinn getur síðan smellt á teiknið á skilaboðaslánni til að sjá leiðbeiningar.</span><span class="sxs-lookup"><span data-stu-id="23b5c-115">The user can then click the icon in the message bar to view the instructions.</span></span> <span data-ttu-id="23b5c-116">Fylgið eftirfarandi skrefum til að slá inn efnislínu og fyrirmæli.</span><span class="sxs-lookup"><span data-stu-id="23b5c-116">Follow these steps to enter a subject line and instructions.</span></span>

1. <span data-ttu-id="23b5c-117">Í vinstri glugganum, smelltu á **grunnstillingar**.</span><span class="sxs-lookup"><span data-stu-id="23b5c-117">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="23b5c-118">Í flipanum **leiðbeiningar** í reitnum **efni vinnuliðs** svæðinu, færið inn efnislínuna.</span><span class="sxs-lookup"><span data-stu-id="23b5c-118">On the **Instructions** tab, in the **Work item subject** field, enter the subject line.</span></span>
3. <span data-ttu-id="23b5c-119">Til að sérsníða efnislínuna, er hægt að færa inn staðgengla.</span><span class="sxs-lookup"><span data-stu-id="23b5c-119">To personalize the subject line, you can insert placeholders.</span></span> <span data-ttu-id="23b5c-120">Staðgenglar eru settir í stað viðeigandi gagna þegar efnislínan birtist notendum.</span><span class="sxs-lookup"><span data-stu-id="23b5c-120">Placeholders are replaced with appropriate data when the subject line is shown to users.</span></span> <span data-ttu-id="23b5c-121">Fylgið eftirfarandi skrefum til að færa inn staðgengil:</span><span class="sxs-lookup"><span data-stu-id="23b5c-121">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="23b5c-122">Smellið á textahólfið þar sem staðgengillinn á að birtast.</span><span class="sxs-lookup"><span data-stu-id="23b5c-122">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="23b5c-123">Smella á **Setja inn staðgengil**</span><span class="sxs-lookup"><span data-stu-id="23b5c-123">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="23b5c-124">Í listanum sem birtist skal velja staðgengilinn til að setja inn.</span><span class="sxs-lookup"><span data-stu-id="23b5c-124">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="23b5c-125">Smellt er á **Setja inn**.</span><span class="sxs-lookup"><span data-stu-id="23b5c-125">Click **Insert**.</span></span>

4. <span data-ttu-id="23b5c-126">Til að bæta þýðingum við efnislínuna skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="23b5c-126">To add translations of the subject line, follow these steps:</span></span>

    1. <span data-ttu-id="23b5c-127">Smellt er á **Þýðingar**.</span><span class="sxs-lookup"><span data-stu-id="23b5c-127">Click **Translations**.</span></span>
    2. <span data-ttu-id="23b5c-128">Á síðunni sem birtist er smellt á **bæta við**.</span><span class="sxs-lookup"><span data-stu-id="23b5c-128">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="23b5c-129">Í listanum sem birtist skal velja tungumálið sem verið er að færa inn í textanum.</span><span class="sxs-lookup"><span data-stu-id="23b5c-129">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="23b5c-130">Í svæðið **þýddur texti** skal færa inn textann.</span><span class="sxs-lookup"><span data-stu-id="23b5c-130">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="23b5c-131">Til að sérsníða textann geturðu sett inn staðgengla eins og lýst er í skrefi 3.</span><span class="sxs-lookup"><span data-stu-id="23b5c-131">To personalize the text, you can insert placeholders as described in step 3.</span></span>
    6. <span data-ttu-id="23b5c-132">Smellið á **Loka**.</span><span class="sxs-lookup"><span data-stu-id="23b5c-132">Click **Close**.</span></span>

5. <span data-ttu-id="23b5c-133">Í **leiðbeiningar vinnuliðs** svæðinu, færið inn leiðbeiningar.</span><span class="sxs-lookup"><span data-stu-id="23b5c-133">In the **Work item instructions** field, enter the instructions.</span></span>
6. <span data-ttu-id="23b5c-134">Hægt er að sérsníða leiðbeiningarnar með því að færa inn staðgengla.</span><span class="sxs-lookup"><span data-stu-id="23b5c-134">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="23b5c-135">Staðgenglar eru settir í stað viðeigandi gagna þegar leiðbeiningar birtist notendum.</span><span class="sxs-lookup"><span data-stu-id="23b5c-135">Placeholders are replaced with appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="23b5c-136">Fylgið eftirfarandi skrefum til að færa inn staðgengil:</span><span class="sxs-lookup"><span data-stu-id="23b5c-136">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="23b5c-137">Smellið á textahólfið þar sem staðgengillinn á að birtast.</span><span class="sxs-lookup"><span data-stu-id="23b5c-137">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="23b5c-138">Smella á **Setja inn staðgengil**</span><span class="sxs-lookup"><span data-stu-id="23b5c-138">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="23b5c-139">Í listanum sem birtist skal velja staðgengilinn til að setja inn.</span><span class="sxs-lookup"><span data-stu-id="23b5c-139">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="23b5c-140">Smellt er á **Setja inn**.</span><span class="sxs-lookup"><span data-stu-id="23b5c-140">Click **Insert**.</span></span>

7. <span data-ttu-id="23b5c-141">Til að bæta þýðingum við leiðbeiningar skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="23b5c-141">To add translations of the instructions, follow these steps:</span></span>

    1. <span data-ttu-id="23b5c-142">Smellt er á **Þýðingar**.</span><span class="sxs-lookup"><span data-stu-id="23b5c-142">Click **Translations**.</span></span>
    2. <span data-ttu-id="23b5c-143">Á síðunni sem birtist er smellt á **bæta við**.</span><span class="sxs-lookup"><span data-stu-id="23b5c-143">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="23b5c-144">Í listanum sem birtist skal velja tungumálið sem verið er að færa inn í textanum.</span><span class="sxs-lookup"><span data-stu-id="23b5c-144">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="23b5c-145">Í svæðið **þýddur texti** skal færa inn textann.</span><span class="sxs-lookup"><span data-stu-id="23b5c-145">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="23b5c-146">Til að sérsníða textann geturðu sett inn staðgengla eins og lýst er í skrefi 6.</span><span class="sxs-lookup"><span data-stu-id="23b5c-146">To personalize the text, you can insert placeholders as described in step 6.</span></span>
    6. <span data-ttu-id="23b5c-147">Smellið á **Loka**.</span><span class="sxs-lookup"><span data-stu-id="23b5c-147">Click **Close**.</span></span>

## <a name="specify-the-possible-outcomes-of-a-decision"></a><span data-ttu-id="23b5c-148">Tilgreina mögulega niðurstöðu ákvörðunar</span><span class="sxs-lookup"><span data-stu-id="23b5c-148">Specify the possible outcomes of a decision</span></span>

<span data-ttu-id="23b5c-149">Yfirleitt þegar skjal er tengt þeim sem tekur ákvörðun, fær sá sem tekur ákvörðun spurningu.</span><span class="sxs-lookup"><span data-stu-id="23b5c-149">Typically, when a document is assigned to a decision maker, the decision maker is asked a question.</span></span> <span data-ttu-id="23b5c-150">Svar við spurningunni er yfirleitt **Já** eða **Nei**, eða **Satt** eða **Ósatt**.</span><span class="sxs-lookup"><span data-stu-id="23b5c-150">The answer to this question is usually **Yes** or **No**, or **True** or **False**.</span></span> <span data-ttu-id="23b5c-151">Fylgið eftirfarandi skrefum til að tilgreina mögulega niðurstöðu handvirku ákvörðuninni.</span><span class="sxs-lookup"><span data-stu-id="23b5c-151">Follow these steps to specify the possible outcomes of the manual decision.</span></span>

1. <span data-ttu-id="23b5c-152">Í vinstri glugganum, smelltu á **grunnstillingar**.</span><span class="sxs-lookup"><span data-stu-id="23b5c-152">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="23b5c-153">Á flipanum **Niðurstöður** , á **Niðurstaða 1** skal færa inn heiti niðurstöðu eða valkostinn.</span><span class="sxs-lookup"><span data-stu-id="23b5c-153">On the **Outcomes** tab, in the **Outcome 1** field, enter the name of the outcome, or the option.</span></span>
3. <span data-ttu-id="23b5c-154">Til að bæta þýðingum við útkomuna skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="23b5c-154">To add translations of the outcome, follow these steps:</span></span>

    1. <span data-ttu-id="23b5c-155">Smellt er á **Þýðingar**.</span><span class="sxs-lookup"><span data-stu-id="23b5c-155">Click **Translations**.</span></span>
    2. <span data-ttu-id="23b5c-156">Á síðunni sem birtist er smellt á **bæta við**.</span><span class="sxs-lookup"><span data-stu-id="23b5c-156">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="23b5c-157">Í listanum sem birtist skal velja tungumálið sem verið er að færa inn í textanum.</span><span class="sxs-lookup"><span data-stu-id="23b5c-157">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="23b5c-158">Í svæðið **þýddur texti** skal færa inn textann.</span><span class="sxs-lookup"><span data-stu-id="23b5c-158">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="23b5c-159">Smellið á **Loka**.</span><span class="sxs-lookup"><span data-stu-id="23b5c-159">Click **Close**.</span></span>

4. <span data-ttu-id="23b5c-160">Á flipanum **Niðurstaða 2** skal færa inn heiti niðurstöðu eða valkostinn.</span><span class="sxs-lookup"><span data-stu-id="23b5c-160">In the **Outcome 2** field, enter the name of the outcome, or the option.</span></span>
5. <span data-ttu-id="23b5c-161">Til að bæta þýðingum við útkomuna skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="23b5c-161">To add translations of the outcome, follow these steps:</span></span>

    1. <span data-ttu-id="23b5c-162">Smellt er á **Þýðingar**.</span><span class="sxs-lookup"><span data-stu-id="23b5c-162">Click **Translations**.</span></span>
    2. <span data-ttu-id="23b5c-163">Á síðunni sem birtist er smellt á **bæta við**.</span><span class="sxs-lookup"><span data-stu-id="23b5c-163">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="23b5c-164">Í listanum sem birtist skal velja tungumálið sem verið er að færa inn í textanum.</span><span class="sxs-lookup"><span data-stu-id="23b5c-164">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="23b5c-165">Í svæðið **þýddur texti** skal færa inn textann.</span><span class="sxs-lookup"><span data-stu-id="23b5c-165">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="23b5c-166">Smellið á **Loka**.</span><span class="sxs-lookup"><span data-stu-id="23b5c-166">Click **Close**.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="23b5c-167">Tilgreinið hvenær tilkynningar eru sendar út</span><span class="sxs-lookup"><span data-stu-id="23b5c-167">Specify when notifications are sent</span></span>

<span data-ttu-id="23b5c-168">Hægt er að senda tilkynningar til fólks þegar ákvörðun hefur verið tekin, framseld eða stigmögnuð.</span><span class="sxs-lookup"><span data-stu-id="23b5c-168">You can send notifications to people when a decision has been made, delegated, or escalated.</span></span> <span data-ttu-id="23b5c-169">Fylgið eftirfarandi skrefum til að tilgreina hvenær senda á út tilkynningar og til hvers tilkynningar eru sendar.</span><span class="sxs-lookup"><span data-stu-id="23b5c-169">Follow these steps to specify when notifications are sent, and who the notifications are sent to.</span></span>

1. <span data-ttu-id="23b5c-170">Á svæðinu vinstra megin, smella á **tilkynningar**.</span><span class="sxs-lookup"><span data-stu-id="23b5c-170">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="23b5c-171">Veldu gátreitinn sem er við hliðina á tilvikunum sem tilkynningar eiga að vera senda vegna.</span><span class="sxs-lookup"><span data-stu-id="23b5c-171">Select the check box next to the events that notifications should be sent for:</span></span>

    - <span data-ttu-id="23b5c-172">**\[Val 1\]** – Úthlutaður notandi hefur valið **\[Val 1\]**.</span><span class="sxs-lookup"><span data-stu-id="23b5c-172">**\[Choice 1\]** – The assigned user has selected **\[Choice 1\]**.</span></span>
    - <span data-ttu-id="23b5c-173">**\[Val 2\]** – Úthlutaður notandi hefur valið **\[Val 2\]**.</span><span class="sxs-lookup"><span data-stu-id="23b5c-173">**\[Choice 2\]** – The assigned user has selected **\[Choice 2\]**.</span></span>
    - <span data-ttu-id="23b5c-174">**Framselja** – úthlutaður notandi hefur úthlutað ákvörðuninni til annars notanda.</span><span class="sxs-lookup"><span data-stu-id="23b5c-174">**Delegate** – The assigned user has assigned the decision to another user.</span></span>
    - <span data-ttu-id="23b5c-175">**Stigmagna** – úthlutaður notandi hefur ekki tekið ákvörðun innan tímarammans.</span><span class="sxs-lookup"><span data-stu-id="23b5c-175">**Escalate** – The assigned user hasn't made the decision in the allotted time.</span></span>

3. <span data-ttu-id="23b5c-176">Veljið línu fyrir tilvik sem þú valdir í skrefi 2.</span><span class="sxs-lookup"><span data-stu-id="23b5c-176">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="23b5c-177">Á **tilkynningartexti** flipanum í textareitinn, færa inn texta tilkynningarinnar.</span><span class="sxs-lookup"><span data-stu-id="23b5c-177">On the **Notification text** tab, in the text box, enter the text of the notification.</span></span>
5. <span data-ttu-id="23b5c-178">Hægt er að sérsníða tilkynningu með því að færa inn staðgengla.</span><span class="sxs-lookup"><span data-stu-id="23b5c-178">To personalize the notification, you can insert placeholders.</span></span> <span data-ttu-id="23b5c-179">Staðgenglar eru settir í stað viðeigandi gagna þegar tilkynning birtist notendum.</span><span class="sxs-lookup"><span data-stu-id="23b5c-179">Placeholders are replaced with appropriate data when the notification is show to users.</span></span> <span data-ttu-id="23b5c-180">Fylgið eftirfarandi skrefum til að færa inn staðgengil:</span><span class="sxs-lookup"><span data-stu-id="23b5c-180">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="23b5c-181">Smellið á textahólfið þar sem staðgengillinn á að birtast.</span><span class="sxs-lookup"><span data-stu-id="23b5c-181">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="23b5c-182">Smella á **Setja inn staðgengil**</span><span class="sxs-lookup"><span data-stu-id="23b5c-182">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="23b5c-183">Í listanum sem birtist skal velja staðgengilinn til að setja inn.</span><span class="sxs-lookup"><span data-stu-id="23b5c-183">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="23b5c-184">Smellt er á **Setja inn**.</span><span class="sxs-lookup"><span data-stu-id="23b5c-184">Click **Insert**.</span></span>

6. <span data-ttu-id="23b5c-185">Til að bæta þýðingum við Tilkynningar skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="23b5c-185">To add translations of the notification, follow these steps:</span></span>

    1. <span data-ttu-id="23b5c-186">Smellt er á **Þýðingar**.</span><span class="sxs-lookup"><span data-stu-id="23b5c-186">Click **Translations**.</span></span>
    2. <span data-ttu-id="23b5c-187">Á síðunni sem birtist er smellt á **bæta við**.</span><span class="sxs-lookup"><span data-stu-id="23b5c-187">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="23b5c-188">Í listanum sem birtist skal velja tungumálið sem verið er að færa inn í textanum.</span><span class="sxs-lookup"><span data-stu-id="23b5c-188">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="23b5c-189">Í svæðið **þýddur texti** skal færa inn textann.</span><span class="sxs-lookup"><span data-stu-id="23b5c-189">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="23b5c-190">Til að sérsníða textann geturðu sett inn staðgengla eins og lýst er í skrefi 5.</span><span class="sxs-lookup"><span data-stu-id="23b5c-190">To personalize the text, you can insert placeholders as described in step 5.</span></span>
    6. <span data-ttu-id="23b5c-191">Smellið á **Loka**.</span><span class="sxs-lookup"><span data-stu-id="23b5c-191">Click **Close**.</span></span>

7. <span data-ttu-id="23b5c-192">Á **Viðtakanda** flipanum, tilgreinið hverjum tilkynningar eru sendar.</span><span class="sxs-lookup"><span data-stu-id="23b5c-192">On the **Recipient** tab, specify who the notifications are sent to.</span></span> <span data-ttu-id="23b5c-193">Veljið einn af valkostum í eftirfarandi töflu, og fylgið svo viðbótarskref fyrir valkostinn áður en farið er í skrefi 8.</span><span class="sxs-lookup"><span data-stu-id="23b5c-193">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 8.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="23b5c-194">Valkostur</span><span class="sxs-lookup"><span data-stu-id="23b5c-194">Option</span></span></th>
    <th><span data-ttu-id="23b5c-195">Viðtakendur tilkynninga.</span><span class="sxs-lookup"><span data-stu-id="23b5c-195">Notification recipients</span></span></th>
    <th><span data-ttu-id="23b5c-196">Viðbótarskref</span><span class="sxs-lookup"><span data-stu-id="23b5c-196">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="23b5c-197">Þátttakendur</span><span class="sxs-lookup"><span data-stu-id="23b5c-197">Participant</span></span></td>
    <td><span data-ttu-id="23b5c-198">Notendur sem tilheyra tilteknum hópi eða hlutverki</span><span class="sxs-lookup"><span data-stu-id="23b5c-198">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="23b5c-199">Eftor að þú velur <strong>viðtakanda</strong>, Á flipanum <strong>Hlutverkamiðað</strong> , á listanum <strong>Gerð þátttakanda</strong> skal velja gerð hóps eða hlutverks til að senda tilkynningu á.</span><span class="sxs-lookup"><span data-stu-id="23b5c-199">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="23b5c-200">Í listanum <strong>Þátttakanda</strong> skal velja hópi til að senda tilkynningar til.</span><span class="sxs-lookup"><span data-stu-id="23b5c-200">In the <strong>Participant</strong> list, select the group or to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="23b5c-201">Verkflæðisnotandi</span><span class="sxs-lookup"><span data-stu-id="23b5c-201">Workflow user</span></span></td>
    <td><span data-ttu-id="23b5c-202">Notendur í núverandi verkflæði</span><span class="sxs-lookup"><span data-stu-id="23b5c-202">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="23b5c-203">Eftir að þú velur <strong>verkflæðisnotandi</strong>, á <strong>verkflæðisnotandi</strong> flipanum, á <strong>verkflæðisnotandi</strong> listanum, veldu notandann sem tekur þátt í verkflæði.</span><span class="sxs-lookup"><span data-stu-id="23b5c-203">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="23b5c-204">Notandi</span><span class="sxs-lookup"><span data-stu-id="23b5c-204">User</span></span></td>
    <td><span data-ttu-id="23b5c-205">Tilteknir notendur</span><span class="sxs-lookup"><span data-stu-id="23b5c-205">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="23b5c-206">Eftir að þú velur <strong>Notanda</strong>, skal smellið á <strong>Notanda</strong> flipa.</span><span class="sxs-lookup"><span data-stu-id="23b5c-206">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="23b5c-207">Listinn <strong>Tiltækir notendur</strong> inniheldur alla notendur.</span><span class="sxs-lookup"><span data-stu-id="23b5c-207">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="23b5c-208">Veldu Notendur til að senda tilkynningar til, og færðu síðan þessa notendur í <strong>Valdir notendur</strong> lista.</span><span class="sxs-lookup"><span data-stu-id="23b5c-208">Select the users to send notifications to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. <span data-ttu-id="23b5c-209">Endurtakið skref 3 til 7 hvert tilvik sem valin var í skrefi 2.</span><span class="sxs-lookup"><span data-stu-id="23b5c-209">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="assign-a-decision"></a><span data-ttu-id="23b5c-210">Úthluta ákvörðun</span><span class="sxs-lookup"><span data-stu-id="23b5c-210">Assign a decision</span></span>

<span data-ttu-id="23b5c-211">Farið að þessum skrefum til að tilgreina á hvern skal úthluta Handvirk Ákvörðun.</span><span class="sxs-lookup"><span data-stu-id="23b5c-211">Follow these steps to specify who a manual decision should be assigned to.</span></span>

1. <span data-ttu-id="23b5c-212">Á vinstra svæðinu er smellt á **úthlutun**.</span><span class="sxs-lookup"><span data-stu-id="23b5c-212">In the left pane, click **Assignment**.</span></span>
2. <span data-ttu-id="23b5c-213">Á flipanum **úthlutunargerð** , veljið einn af valkostum í eftirfarandi töflu, og fylgið svo viðbótarskref fyrir valkostinn áður en farið er í skrefi 3.</span><span class="sxs-lookup"><span data-stu-id="23b5c-213">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 3.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="23b5c-214">Valkostur</span><span class="sxs-lookup"><span data-stu-id="23b5c-214">Option</span></span></th>
    <th><span data-ttu-id="23b5c-215">Notendur sem er úthlutað er ákvörðuninni</span><span class="sxs-lookup"><span data-stu-id="23b5c-215">Users that the decision is assigned to</span></span></th>
    <th><span data-ttu-id="23b5c-216">Viðbótarskref</span><span class="sxs-lookup"><span data-stu-id="23b5c-216">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="23b5c-217">Þátttakendur</span><span class="sxs-lookup"><span data-stu-id="23b5c-217">Participant</span></span></td>
    <td><span data-ttu-id="23b5c-218">Notendur sem tilheyra tilteknum hópi eða hlutverki</span><span class="sxs-lookup"><span data-stu-id="23b5c-218">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="23b5c-219">Eftir að þú velur <strong>Þátttakanda</strong>á flipanum <strong>Hlutverkamiðað</strong> , á listanum <strong>Gerð þátttakanda</strong> skal velja gerð hóps eða hlutverks til að úthluta ákvörðun á.</span><span class="sxs-lookup"><span data-stu-id="23b5c-219">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to assign the decision to.</span></span></li>
    <li><span data-ttu-id="23b5c-220">Í listanum <strong>Þátttakanda</strong> skal velja hópi eða hlutverki til að úthluta ákvörðun á.</span><span class="sxs-lookup"><span data-stu-id="23b5c-220">In the <strong>Participant</strong> list, select the group or role to assign the decision to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="23b5c-221">Stigveldi</span><span class="sxs-lookup"><span data-stu-id="23b5c-221">Hierarchy</span></span></td>
    <td><span data-ttu-id="23b5c-222">Notendur í tilteknu stigveldi fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="23b5c-222">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="23b5c-223">Eftir að þú velur <strong>stigveldi</strong>, á <strong>stigveldishluti</strong> flipanum, á listanum <strong>gerð stigveldis</strong> skal velja gerð stigveldis til að úthluta ákvörðun á.</span><span class="sxs-lookup"><span data-stu-id="23b5c-223">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to assign the decision to.</span></span></li>
    <li><span data-ttu-id="23b5c-224">Kerfið verður að sækja svið notendanafna úr stigveldinu.</span><span class="sxs-lookup"><span data-stu-id="23b5c-224">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="23b5c-225">Þessi nöfn standa fyrir notendur sem hægt er að úthluta ákvörðun á.</span><span class="sxs-lookup"><span data-stu-id="23b5c-225">These names represent users that the decision can be assigned to.</span></span> <span data-ttu-id="23b5c-226">Farðu að þessum skrefum til að tilgreina upphafspunkt og lokapunkt sviðs notendanafna sem kerfið sækir.</span><span class="sxs-lookup"><span data-stu-id="23b5c-226">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="23b5c-227">Þegar tilgreina á upphafspunkt skal velja aðila af listanum <strong>Byrja frá og með</strong>.</span><span class="sxs-lookup"><span data-stu-id="23b5c-227">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="23b5c-228">Hægt er að tilgreina endapunkt með því að smella á <strong>bæta við skilyrði</strong>.</span><span class="sxs-lookup"><span data-stu-id="23b5c-228">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="23b5c-229">Til að færa inn skilyrðu sem ákvarðar hvar í stigveldinu kerfið eigi að hætta að sækja nöfn.</span><span class="sxs-lookup"><span data-stu-id="23b5c-229">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="23b5c-230">Á <strong>stigveldisvalkostir</strong> flipanum skal tilgreina hvaða notendur á sviðinu ákvörðun skal úthlutað á:</span><span class="sxs-lookup"><span data-stu-id="23b5c-230">On the <strong>Hierarchy options</strong> tab, specify which users in the range the decision should be assigned to:</span></span> <ul>
    <li><span data-ttu-id="23b5c-231"><strong>Úthluta til allra sóttra notenda</strong> - þá er Ákvörðun úthlutað til allra notenda á sviðinu.</span><span class="sxs-lookup"><span data-stu-id="23b5c-231"><strong>Assign to all users retrieved</strong> – The decision is assigned to all users in the range.</span></span></li>
    <li><span data-ttu-id="23b5c-232"><strong>Úthluta eingöngu til síðasta sótta notanda</strong> - þá er ákvörðun aðeins úthlutað til síðasta notanda á sviðinu.</span><span class="sxs-lookup"><span data-stu-id="23b5c-232"><strong>Assign only to last user retrieved</strong> – The decision is assigned to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="23b5c-233"><strong>Sleppa notendum með eftirfarandi skilyrði</strong> – Ákvörðun er ekki úthlutað á notendur innan sviðsins sem uppfylla ákveðið skilyrði.</span><span class="sxs-lookup"><span data-stu-id="23b5c-233"><strong>Exclude users with the following condition</strong> – The decision isn't assigned to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="23b5c-234">Smellið á <strong>bæta við skilyrði</strong> til að skilgreina skilyrðin.</span><span class="sxs-lookup"><span data-stu-id="23b5c-234">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="23b5c-235">Verkflæðisnotandi</span><span class="sxs-lookup"><span data-stu-id="23b5c-235">Workflow user</span></span></td>
    <td><span data-ttu-id="23b5c-236">Notendur í núverandi verkflæði</span><span class="sxs-lookup"><span data-stu-id="23b5c-236">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="23b5c-237">Eftir að þú velur <strong>verkflæðisnotandi</strong>, á <strong>verkflæðisnotandi</strong> flipanum, á <strong>verkflæðisnotandi</strong> listanum, veldu notandann sem tekur þátt í verkflæði.</span><span class="sxs-lookup"><span data-stu-id="23b5c-237">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="23b5c-238">Notandi</span><span class="sxs-lookup"><span data-stu-id="23b5c-238">User</span></span></td>
    <td><span data-ttu-id="23b5c-239">Tilteknir notendur</span><span class="sxs-lookup"><span data-stu-id="23b5c-239">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="23b5c-240">Eftir að þú velur <strong>Notanda</strong>, skal smellið á <strong>Notanda</strong> flipa.</span><span class="sxs-lookup"><span data-stu-id="23b5c-240">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="23b5c-241">Listinn <strong>Tiltækir notendur</strong> inniheldur alla notendur.</span><span class="sxs-lookup"><span data-stu-id="23b5c-241">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="23b5c-242">Veldu Notendur til að úthluta Ákvörðun á, og færa síðan þessa notendur í <strong>Valdir notendur</strong> lista.</span><span class="sxs-lookup"><span data-stu-id="23b5c-242">Select the users to assign the decision to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

3. <span data-ttu-id="23b5c-243">Á **tímamörk** flipanum, á svæðinu **Tímalengd** , tilgreinið hve mikinn tíma notandi hefur til að taka ákvörðunina.</span><span class="sxs-lookup"><span data-stu-id="23b5c-243">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to make the decision.</span></span> <span data-ttu-id="23b5c-244">Veldu einn af eftirfarandi valkostum:</span><span class="sxs-lookup"><span data-stu-id="23b5c-244">Select one of the following options:</span></span>

    - <span data-ttu-id="23b5c-245">**Klukkustundir** – færið Inn fjölda klukkustunda sem notandi hefur til að taka ákvörðunina.</span><span class="sxs-lookup"><span data-stu-id="23b5c-245">**Hours** – Enter the number of hours that the user has to make the decision.</span></span> <span data-ttu-id="23b5c-246">Þá velja dagatalið sem fyrirtækið notar og færa inn upplýsingar um vinnuviku fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="23b5c-246">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="23b5c-247">**Dagar** – færið Inn fjölda daga sem notandi hefur til að taka ákvörðunina.</span><span class="sxs-lookup"><span data-stu-id="23b5c-247">**Days** – Enter the number of days that the user has to make the decision.</span></span> <span data-ttu-id="23b5c-248">Þá velja dagatalið sem fyrirtækið notar og færa inn upplýsingar um vinnuviku fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="23b5c-248">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="23b5c-249">**Vikur** – færið Inn fjölda vikna sem notandi hefur til að taka ákvörðunina.</span><span class="sxs-lookup"><span data-stu-id="23b5c-249">**Weeks** – Enter the number of weeks that the user has to make the decision.</span></span>
    - <span data-ttu-id="23b5c-250">**Mánuðir** — velja daginn og vikuna sem notandinn verður að vera búinn að taka ákvörðunina fyrir.</span><span class="sxs-lookup"><span data-stu-id="23b5c-250">**Months** – Select the day and week that the user must make the decision by.</span></span> <span data-ttu-id="23b5c-251">Til dæmis, notandi getur óskað þess að annar notandi taka ákvörðunina fyrir föstudag í þriðju viku mánaðarins.</span><span class="sxs-lookup"><span data-stu-id="23b5c-251">For example, you might want the user to make the decision by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="23b5c-252">**Ár** — velja daginn, vikuna og mánuðinn sem notandinn verður að vera búinn að taka ákvörðunina fyrir.</span><span class="sxs-lookup"><span data-stu-id="23b5c-252">**Years** – Select the day, week, and month that the user must make the decision by.</span></span> <span data-ttu-id="23b5c-253">Til dæmis, notandi getur óskað þess að annar notandi taka ákvörðunina fyrir föstudag í þriðju viku desembermánaðar.</span><span class="sxs-lookup"><span data-stu-id="23b5c-253">For example, you might want the user to make the decision by Friday of the third week of December.</span></span>

    <span data-ttu-id="23b5c-254">Ef notandinn tekur ekki ákvörðunina innan tímarammans, er ákvörðunin komið fram yfir á tíma.</span><span class="sxs-lookup"><span data-stu-id="23b5c-254">If the user doesn't make the decision in the allotted time, the decision is overdue.</span></span> <span data-ttu-id="23b5c-255">Ákvörðun sem er komið fram yfir á tíma er stigmagnað, á grundvelli valkostanna sem þú valdir í **stigmögnun** svæðið á síðunni.</span><span class="sxs-lookup"><span data-stu-id="23b5c-255">A decision that is overdue is escalated, based on the options that you select in the **Escalation** area of the page.</span></span>

## <a name="specify-what-happens-when-a-decision-is-overdue"></a><span data-ttu-id="23b5c-256">Tilgreina hvað gerist þegar ákvörðun er komið fram yfir á tíma</span><span class="sxs-lookup"><span data-stu-id="23b5c-256">Specify what happens when a decision is overdue</span></span>

<span data-ttu-id="23b5c-257">Ef notandinn tekur ekki ákvörðunina innan tímarammans, er ákvörðunin komið fram yfir á tíma.</span><span class="sxs-lookup"><span data-stu-id="23b5c-257">If a user doesn't make the decision in the allotted time, the decision is overdue.</span></span> <span data-ttu-id="23b5c-258">Ákvörðun sem er komið fram yfir á tíma má stigmagna, eða úthluta sjálfkrafa á annan notanda.</span><span class="sxs-lookup"><span data-stu-id="23b5c-258">A decision that is overdue can be escalated, or automatically assigned to another user.</span></span> <span data-ttu-id="23b5c-259">Fylgið eftirfarandi skrefum til að stigmagna Ákvörðun ef það er komið fram yfir á tíma.</span><span class="sxs-lookup"><span data-stu-id="23b5c-259">Follow these steps to escalate the decision if it's overdue.</span></span>

1. <span data-ttu-id="23b5c-260">Á vinstra svæðinu skaltu Smellt á **Stigmagna**.</span><span class="sxs-lookup"><span data-stu-id="23b5c-260">In the left pane, click **Escalation**.</span></span>
2. <span data-ttu-id="23b5c-261">Velja skal **Nota stigmögnunarslóð** gátreit til að stofna stigmögnunarslóð.</span><span class="sxs-lookup"><span data-stu-id="23b5c-261">Select the **Use escalation path** check box to create an escalation path.</span></span> <span data-ttu-id="23b5c-262">Kerfið mun sjálfkrafa úthluta Ákvörðun til notendanna sem skráðir eru í stigmögnunarslóðinni.</span><span class="sxs-lookup"><span data-stu-id="23b5c-262">The system automatically assigns the decision to the users who are listed in the escalation path.</span></span> <span data-ttu-id="23b5c-263">Til dæmis, eftirfarandi töflu sýnir stigmögnunarslóð.</span><span class="sxs-lookup"><span data-stu-id="23b5c-263">For example, the following table represents an escalation path.</span></span>

    | <span data-ttu-id="23b5c-264">Röð</span><span class="sxs-lookup"><span data-stu-id="23b5c-264">Sequence</span></span> | <span data-ttu-id="23b5c-265">stigmögnunarslóð</span><span class="sxs-lookup"><span data-stu-id="23b5c-265">Escalation path</span></span>            |
    |----------|----------------------------|
    | <span data-ttu-id="23b5c-266">1</span><span class="sxs-lookup"><span data-stu-id="23b5c-266">1</span></span>        | <span data-ttu-id="23b5c-267">Úthluta til: Dísu</span><span class="sxs-lookup"><span data-stu-id="23b5c-267">Assign to: Donna</span></span>           |
    | <span data-ttu-id="23b5c-268">2</span><span class="sxs-lookup"><span data-stu-id="23b5c-268">2</span></span>        | <span data-ttu-id="23b5c-269">Úthluta til: Erlu</span><span class="sxs-lookup"><span data-stu-id="23b5c-269">Assign to: Erin</span></span>            |
    | <span data-ttu-id="23b5c-270">3</span><span class="sxs-lookup"><span data-stu-id="23b5c-270">3</span></span>        | <span data-ttu-id="23b5c-271">Endanleg aðgerð: \[Val 1\]</span><span class="sxs-lookup"><span data-stu-id="23b5c-271">Final action: \[Choice 1\]</span></span> |

    <span data-ttu-id="23b5c-272">Í þessu dæmi mun kerfið sjálfkrafa úthluta Ákvörðun sem er komið fram yfir á tíma til Dísu.</span><span class="sxs-lookup"><span data-stu-id="23b5c-272">In this example, the system assigns the overdue decision to Donna.</span></span> <span data-ttu-id="23b5c-273">Ef Dísu tekur ekki ákvörðun innan tímarammans, úthlutar kerfið ákvörðuninni til Erlu.</span><span class="sxs-lookup"><span data-stu-id="23b5c-273">If Donna doesn't make the decision in the allotted time, the system assigns the decision to Erin.</span></span> <span data-ttu-id="23b5c-274">Ef Erla tekur ekki ákvörðun innan tímarammans, Velur kerfið **\[Val 1\]** sem ákvörðun.</span><span class="sxs-lookup"><span data-stu-id="23b5c-274">If Erin doesn't make the decision in the allotted time, the system selects **\[Choice 1\]** as the decision.</span></span>

3. <span data-ttu-id="23b5c-275">Til að bæta notanda við stigmögnunarslóð, smella **bæta við stigmögnun**.</span><span class="sxs-lookup"><span data-stu-id="23b5c-275">To add a user to the escalation path, click **Add escalation**.</span></span> <span data-ttu-id="23b5c-276">Veljið einn af valkostum í eftirfarandi töflu, og fylgið svo viðbótarskref fyrir valkostinn áður en farið er í skrefi 4.</span><span class="sxs-lookup"><span data-stu-id="23b5c-276">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 4.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="23b5c-277">Valkostur</span><span class="sxs-lookup"><span data-stu-id="23b5c-277">Option</span></span></th>
    <th><span data-ttu-id="23b5c-278">Notendur sem Ákvörðun er stigmagnað fyrir</span><span class="sxs-lookup"><span data-stu-id="23b5c-278">Users that the decision is escalated to</span></span></th>
    <th><span data-ttu-id="23b5c-279">Viðbótarskref</span><span class="sxs-lookup"><span data-stu-id="23b5c-279">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="23b5c-280">Stigveldi</span><span class="sxs-lookup"><span data-stu-id="23b5c-280">Hierarchy</span></span></td>
    <td><span data-ttu-id="23b5c-281">Notendur í tilteknu stigveldi fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="23b5c-281">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="23b5c-282">Eftir að þú velur <strong>stigveldi</strong>, á <strong>stigveldishluti</strong> flipanum, á listanum <strong>gerð stigveldis</strong> skal velja gerð stigveldis til að stigmagna ákvörðun fyrir.</span><span class="sxs-lookup"><span data-stu-id="23b5c-282">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to escalate the decision to.</span></span></li>
    <li><span data-ttu-id="23b5c-283">Kerfið verður að sækja svið notendanafna úr stigveldinu.</span><span class="sxs-lookup"><span data-stu-id="23b5c-283">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="23b5c-284">Þessi nöfn standa fyrir notendur sem hægt er stigmagna Ákvörðun fyrir.</span><span class="sxs-lookup"><span data-stu-id="23b5c-284">These names represent users that the decision can be escalated to.</span></span> <span data-ttu-id="23b5c-285">Farðu að þessum skrefum til að tilgreina upphafspunkt og lokapunkt sviðs notendanafna sem kerfið sækir.</span><span class="sxs-lookup"><span data-stu-id="23b5c-285">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="23b5c-286">Þegar tilgreina á upphafspunkt skal velja aðila af listanum <strong>Byrja frá og með</strong>.</span><span class="sxs-lookup"><span data-stu-id="23b5c-286">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="23b5c-287">Hægt er að tilgreina endapunkt með því að smella á <strong>bæta við skilyrði</strong>.</span><span class="sxs-lookup"><span data-stu-id="23b5c-287">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="23b5c-288">Til að færa inn skilyrðu sem ákvarðar hvar í stigveldinu kerfið eigi að hætta að sækja nöfn.</span><span class="sxs-lookup"><span data-stu-id="23b5c-288">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="23b5c-289">Á <strong>stigveldisvalkostir</strong> flipanum skal tilgreina hvaða notendur á sviðinu ákvörðun skal stigmagnað fyrir:</span><span class="sxs-lookup"><span data-stu-id="23b5c-289">On the <strong>Hierarchy options</strong> tab, specify which users in the range the decision should be escalated to:</span></span> <ul>
    <li><span data-ttu-id="23b5c-290"><strong>Úthluta til allra sóttra notenda</strong> - þá er ákvörðun stigmagnað fyrir allra notenda á sviðinu.</span><span class="sxs-lookup"><span data-stu-id="23b5c-290"><strong>Assign to all users retrieved</strong> – The decision is escalated to all users in the range.</span></span></li>
    <li><span data-ttu-id="23b5c-291"><strong>Úthluta eingöngu til síðasta sótta notanda</strong> - þá er ákvörðun stigmagnað aðeins til síðasta notanda á sviðinu.</span><span class="sxs-lookup"><span data-stu-id="23b5c-291"><strong>Assign only to last user retrieved</strong> – The decision is escalated to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="23b5c-292"><strong>Sleppa notendum með eftirfarandi skilyrði</strong> – Ákvörðun er ekki stigmagnað fyrir neina notendur innan sviðsins sem uppfylla ákveðið skilyrði.</span><span class="sxs-lookup"><span data-stu-id="23b5c-292"><strong>Exclude users with the following condition:</strong> – The decision isn't escalated to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="23b5c-293">Smellið á <strong>bæta við skilyrði</strong> til að skilgreina skilyrðin.</span><span class="sxs-lookup"><span data-stu-id="23b5c-293">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="23b5c-294">Verkflæðisnotandi</span><span class="sxs-lookup"><span data-stu-id="23b5c-294">Workflow user</span></span></td>
    <td><span data-ttu-id="23b5c-295">Notendur í núverandi verkflæði</span><span class="sxs-lookup"><span data-stu-id="23b5c-295">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="23b5c-296">Eftir að þú velur <strong>verkflæðisnotandi</strong>, á <strong>verkflæðisnotandi</strong> flipanum, á <strong>verkflæðisnotandi</strong> listanum, veldu notandann sem tekur þátt í verkflæði.</span><span class="sxs-lookup"><span data-stu-id="23b5c-296">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="23b5c-297">Notandi</span><span class="sxs-lookup"><span data-stu-id="23b5c-297">User</span></span></td>
    <td><span data-ttu-id="23b5c-298">Tilteknir notendur</span><span class="sxs-lookup"><span data-stu-id="23b5c-298">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="23b5c-299">Eftir að þú velur <strong>Notanda</strong>, skal smellið á <strong>Notanda</strong> flipa.</span><span class="sxs-lookup"><span data-stu-id="23b5c-299">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="23b5c-300">Listinn <strong>Tiltækir notendur</strong> inniheldur alla notendur.</span><span class="sxs-lookup"><span data-stu-id="23b5c-300">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="23b5c-301">Veldu Notendur til að stigmagna Ákvörðun fyrir, og færðu síðan þessa notendur í <strong>Valdir notendur</strong> lista.</span><span class="sxs-lookup"><span data-stu-id="23b5c-301">Select the users to escalate the decision to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

4. <span data-ttu-id="23b5c-302">Á **tímamörk** flipanum, á svæðinu **Tímalengd** , tilgreinið hve mikinn tíma notandi hefur til að taka ákvörðunina.</span><span class="sxs-lookup"><span data-stu-id="23b5c-302">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to make the decision.</span></span> <span data-ttu-id="23b5c-303">Veldu einn af eftirfarandi valkostum:</span><span class="sxs-lookup"><span data-stu-id="23b5c-303">Select one of the following options:</span></span>

    - <span data-ttu-id="23b5c-304">**Klukkustundir** – færið Inn fjölda klukkustunda sem notandi hefur til að taka ákvörðunina.</span><span class="sxs-lookup"><span data-stu-id="23b5c-304">**Hours** – Enter the number of hours that the user has to make the decision.</span></span> <span data-ttu-id="23b5c-305">Þá velja dagatalið sem fyrirtækið notar og færa inn upplýsingar um vinnuviku fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="23b5c-305">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="23b5c-306">**Dagar** – færið Inn fjölda daga sem notandi hefur til að taka ákvörðunina.</span><span class="sxs-lookup"><span data-stu-id="23b5c-306">**Days** – Enter the number of days that the user has to make the decision.</span></span> <span data-ttu-id="23b5c-307">Þá velja dagatalið sem fyrirtækið notar og færa inn upplýsingar um vinnuviku fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="23b5c-307">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="23b5c-308">**Vikur** – færið Inn fjölda vikna sem notandi hefur til að taka ákvörðunina.</span><span class="sxs-lookup"><span data-stu-id="23b5c-308">**Weeks** – Enter the number of weeks that the user has to make the decision.</span></span>
    - <span data-ttu-id="23b5c-309">**Mánuðir** — velja daginn og vikuna sem notandinn verður að vera búinn að taka ákvörðunina fyrir.</span><span class="sxs-lookup"><span data-stu-id="23b5c-309">**Months** – Select the day and week that the user must make the decision by.</span></span> <span data-ttu-id="23b5c-310">Til dæmis, notandi getur óskað þess að annar notandi taka ákvörðunina fyrir föstudag í þriðju viku mánaðarins.</span><span class="sxs-lookup"><span data-stu-id="23b5c-310">For example, you might want the user to make the decision by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="23b5c-311">**Ár** — velja daginn, vikuna og mánuðinn sem notandinn verður að vera búinn að taka ákvörðunina fyrir.</span><span class="sxs-lookup"><span data-stu-id="23b5c-311">**Years** – Select the day, week, and month that the user must make the decision by.</span></span> <span data-ttu-id="23b5c-312">Til dæmis, notandi getur óskað þess að annar notandi taka ákvörðunina fyrir föstudag í þriðju viku desembermánaðar.</span><span class="sxs-lookup"><span data-stu-id="23b5c-312">For example, you might want the user to make the decision by Friday of the third week of December.</span></span>

5. <span data-ttu-id="23b5c-313">Endurtakið skref 3 til 4 fyrir hvern notanda sem á að bæta við stigmögnunarslóð.</span><span class="sxs-lookup"><span data-stu-id="23b5c-313">Repeat steps 3 through 4 for each user that should be added to the escalation path.</span></span> <span data-ttu-id="23b5c-314">Hægt er að breyta röðun notenda.</span><span class="sxs-lookup"><span data-stu-id="23b5c-314">You can change the order of the users.</span></span>
6. <span data-ttu-id="23b5c-315">Ef notendunum í hækkunarslóðinni taka ekki ákvörðun innan tímarammans, tekur kerfið ákvörðunina.</span><span class="sxs-lookup"><span data-stu-id="23b5c-315">If the users in the escalation path don't make the decision in the allotted time, the system makes the decision.</span></span> <span data-ttu-id="23b5c-316">Til að tilgreina valkostinn sem kerfið velur , veldu línuna **Aðgerð** , og síðan á **Ljúka aðgerð** flipanum, veljið valkost.</span><span class="sxs-lookup"><span data-stu-id="23b5c-316">To specify the option that the system selects, select the **Action** row, and then, on the **End action** tab, select an option.</span></span>

## <a name="set-a-time-limit"></a><span data-ttu-id="23b5c-317">Setja upp tímamörk</span><span class="sxs-lookup"><span data-stu-id="23b5c-317">Set a time limit</span></span>

<span data-ttu-id="23b5c-318">Fylgið eftirfarandi skrefum ef verður að taka ákvörðunina innan tiltekins tíma.</span><span class="sxs-lookup"><span data-stu-id="23b5c-318">Follow these steps if the decision must be made in a specific time.</span></span>

> [!NOTE]
> <span data-ttu-id="23b5c-319">Valkostirnir sem valdir eru í þessu ferli munu hnekkja valkostunum sem valdir voru í svæðunum **Úthlutun** og **Stigmögnun** á síðunni.</span><span class="sxs-lookup"><span data-stu-id="23b5c-319">The options that you select in this procedure override the options that you selected in the **Assignment** and **Escalation** areas of the page.</span></span>

1. <span data-ttu-id="23b5c-320">Í vinstri glugganum, smelltu á **ítarlegar stillingar**.</span><span class="sxs-lookup"><span data-stu-id="23b5c-320">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="23b5c-321">Veldu gátreitinn **Stilla tímamörk verkflæðiseiningar**</span><span class="sxs-lookup"><span data-stu-id="23b5c-321">Select the **Set a time limit for the workflow element** check box.</span></span>
3. <span data-ttu-id="23b5c-322">Í reitnum **tímalengd** tilgreinið þegar Ákvörðun á að vera tekin.</span><span class="sxs-lookup"><span data-stu-id="23b5c-322">In the **Duration** field, specify when the decision must be made.</span></span> <span data-ttu-id="23b5c-323">Veldu einn af eftirfarandi valkostum:</span><span class="sxs-lookup"><span data-stu-id="23b5c-323">Select one of the following options:</span></span>

    - <span data-ttu-id="23b5c-324">**Klukkustundir** - Færa þarf inn fjölda klukkustunda.</span><span class="sxs-lookup"><span data-stu-id="23b5c-324">**Hours** – Enter the number of hours.</span></span> <span data-ttu-id="23b5c-325">Þá velja dagatalið sem fyrirtækið notar og færa inn upplýsingar um vinnuviku fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="23b5c-325">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="23b5c-326">**Dagar** - Færið inn fjölda daga.</span><span class="sxs-lookup"><span data-stu-id="23b5c-326">**Days** – Enter the number of days.</span></span> <span data-ttu-id="23b5c-327">Þá velja dagatalið sem fyrirtækið notar og færa inn upplýsingar um vinnuviku fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="23b5c-327">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="23b5c-328">**Vikur** - Færið inn fjölda vikna.</span><span class="sxs-lookup"><span data-stu-id="23b5c-328">**Weeks** – Enter the number of weeks.</span></span>
    - <span data-ttu-id="23b5c-329">**Mánuðir** — velja daginn og vikuna sem verður að vera búið að taka ákvörðunina fyrir.</span><span class="sxs-lookup"><span data-stu-id="23b5c-329">**Months** – Select the day and week that the decision must be made by.</span></span> <span data-ttu-id="23b5c-330">Til dæmis getur átt að vera búið að taka ákvörðunina fyrir föstudaginn í þriðju viku mánaðarins.</span><span class="sxs-lookup"><span data-stu-id="23b5c-330">For example, you might want the decision to be made by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="23b5c-331">**Ár** — velja daginn, vikuna og mánuðinn sem verður að vera búið að taka ákvörðunina fyrir.</span><span class="sxs-lookup"><span data-stu-id="23b5c-331">**Years** – Select the day, week, and month that the decision must be made by.</span></span> <span data-ttu-id="23b5c-332">Til dæmis getur átt að vera búið að taka ákvörðunina fyrir föstudaginn í þriðju viku desembermánaðar.</span><span class="sxs-lookup"><span data-stu-id="23b5c-332">For example, you might want the decision to be made by Friday of the third week of December.</span></span>

4. <span data-ttu-id="23b5c-333">Ef farið er yfir tímamörkin mun kerfið taka ákvörðunina vegna verksins.</span><span class="sxs-lookup"><span data-stu-id="23b5c-333">If the time limit is exceeded, the system makes the decision.</span></span> <span data-ttu-id="23b5c-334">Veljið Valkost, sem kerfið á að velja, í listanum **Aðgerðir**.</span><span class="sxs-lookup"><span data-stu-id="23b5c-334">In the **Action** list, select the option that the system should select.</span></span>
