---
title: Skilgreina handvirkar ákvarðanir í verkflæði
description: Þetta efnisatriði útskýrir hvernig skilgreina á eiginleika handvirkrar ákvörðunar.
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 192101
ms.assetid: 0bccad77-1a44-4f08-967b-12c62c02afc7
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f46b875f52d3d3e7c755ee92dcd5faddf0d94356
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178376"
---
# <a name="configure-manual-decisions-in-a-workflow"></a><span data-ttu-id="8ecf4-103">Skilgreina handvirkar ákvarðanir í verkflæði</span><span class="sxs-lookup"><span data-stu-id="8ecf4-103">Configure manual decisions in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8ecf4-104">Þetta efnisatriði útskýrir hvernig skilgreina á eiginleika handvirkrar ákvörðunar.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-104">This topic explains how to configure the properties of a manual decision.</span></span>

<span data-ttu-id="8ecf4-105">Til að skilgreina handvirka ákvörðun í verkflæðisritlinum, hægrismellt er á handvirk ákvörðun og smellið síðan á **Eiginleika** til að opna **Eiginleika** síðu.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-105">To configure a manual decision in the workflow editor, right-click the manual decision, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="8ecf4-106">Notið síðan eftirfarandi ferli til að stilla eiginleika fyrir handvirk ákvörðun.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-106">Then use the following procedures to configure the properties of the manual decision.</span></span>

## <a name="name-the-decision"></a><span data-ttu-id="8ecf4-107">Heiti ákvörðunar.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-107">Name the decision</span></span>

<span data-ttu-id="8ecf4-108">Fylgið þessum skrefum til að færa inn heiti á handvirk ákvörðun.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-108">Follow these steps to enter a name for the manual decision.</span></span>

1. <span data-ttu-id="8ecf4-109">Í vinstri glugganum, smelltu á **grunnstillingar**.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="8ecf4-110">Á svæðinu **Heiti** skal færa inn einkvæmt heiti fyrir handvirk ákvörðun</span><span class="sxs-lookup"><span data-stu-id="8ecf4-110">In the **Name** field, enter a unique name for the manual decision.</span></span>

## <a name="enter-a-subject-line-and-instructions"></a><span data-ttu-id="8ecf4-111">Slá inn efnislínu og fyrirmæli</span><span class="sxs-lookup"><span data-stu-id="8ecf4-111">Enter a subject line and instructions</span></span>

<span data-ttu-id="8ecf4-112">Veita verður þeim notendum, sem úthlutað er þetta handvirk ákvörðun, efnislínu og fyrirmæli.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-112">You must provide a subject line and instructions to users who are assigned to the manual decision.</span></span> <span data-ttu-id="8ecf4-113">Til dæmis, ef verið er að skilgreina ákvörðun fyrir innkaupabeiðnir, mun notanda sem er úthlutað á ákvörðun sjá efnislínuna og fyrirmælin á **Innkaupabeiðnir** síðunni.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-113">For example, if you're configuring a decision for purchase requisitions, the user who is assigned to the decision sees the subject line and instructions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="8ecf4-114">Efnislínuna birtist á skilaboðaslánni á síðunni.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-114">The subject line appears in a message bar on the page.</span></span> <span data-ttu-id="8ecf4-115">Notandinn getur síðan smellt á teiknið á skilaboðaslánni til að sjá leiðbeiningar.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-115">The user can then click the icon in the message bar to view the instructions.</span></span> <span data-ttu-id="8ecf4-116">Fylgið eftirfarandi skrefum til að slá inn efnislínu og fyrirmæli.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-116">Follow these steps to enter a subject line and instructions.</span></span>

1. <span data-ttu-id="8ecf4-117">Í vinstri glugganum, smelltu á **grunnstillingar**.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-117">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="8ecf4-118">Í flipanum **leiðbeiningar** í reitnum **efni vinnuliðs** svæðinu, færið inn efnislínuna.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-118">On the **Instructions** tab, in the **Work item subject** field, enter the subject line.</span></span>
3. <span data-ttu-id="8ecf4-119">Til að sérsníða efnislínuna, er hægt að færa inn staðgengla.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-119">To personalize the subject line, you can insert placeholders.</span></span> <span data-ttu-id="8ecf4-120">Staðgenglar eru settir í stað viðeigandi gagna þegar efnislínan birtist notendum.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-120">Placeholders are replaced with appropriate data when the subject line is shown to users.</span></span> <span data-ttu-id="8ecf4-121">Fylgið eftirfarandi skrefum til að færa inn staðgengil:</span><span class="sxs-lookup"><span data-stu-id="8ecf4-121">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="8ecf4-122">Smellið á textahólfið þar sem staðgengillinn á að birtast.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-122">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="8ecf4-123">Smella á **Setja inn staðgengil**</span><span class="sxs-lookup"><span data-stu-id="8ecf4-123">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="8ecf4-124">Í listanum sem birtist skal velja staðgengilinn til að setja inn.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-124">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="8ecf4-125">Smellt er á **Setja inn**.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-125">Click **Insert**.</span></span>

4. <span data-ttu-id="8ecf4-126">Til að bæta þýðingum við efnislínuna skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="8ecf4-126">To add translations of the subject line, follow these steps:</span></span>

    1. <span data-ttu-id="8ecf4-127">Smellt er á **Þýðingar**.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-127">Click **Translations**.</span></span>
    2. <span data-ttu-id="8ecf4-128">Á síðunni sem birtist er smellt á **bæta við**.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-128">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="8ecf4-129">Í listanum sem birtist skal velja tungumálið sem verið er að færa inn í textanum.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-129">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="8ecf4-130">Í svæðið **þýddur texti** skal færa inn textann.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-130">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="8ecf4-131">Til að sérsníða textann geturðu sett inn staðgengla eins og lýst er í skrefi 3.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-131">To personalize the text, you can insert placeholders as described in step 3.</span></span>
    6. <span data-ttu-id="8ecf4-132">Smellið á **Loka**.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-132">Click **Close**.</span></span>

5. <span data-ttu-id="8ecf4-133">Í **leiðbeiningar vinnuliðs** svæðinu, færið inn leiðbeiningar.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-133">In the **Work item instructions** field, enter the instructions.</span></span>
6. <span data-ttu-id="8ecf4-134">Hægt er að sérsníða leiðbeiningarnar með því að færa inn staðgengla.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-134">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="8ecf4-135">Staðgenglar eru settir í stað viðeigandi gagna þegar leiðbeiningar birtist notendum.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-135">Placeholders are replaced with appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="8ecf4-136">Fylgið eftirfarandi skrefum til að færa inn staðgengil:</span><span class="sxs-lookup"><span data-stu-id="8ecf4-136">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="8ecf4-137">Smellið á textahólfið þar sem staðgengillinn á að birtast.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-137">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="8ecf4-138">Smella á **Setja inn staðgengil**</span><span class="sxs-lookup"><span data-stu-id="8ecf4-138">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="8ecf4-139">Í listanum sem birtist skal velja staðgengilinn til að setja inn.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-139">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="8ecf4-140">Smellt er á **Setja inn**.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-140">Click **Insert**.</span></span>

7. <span data-ttu-id="8ecf4-141">Til að bæta þýðingum við leiðbeiningar skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="8ecf4-141">To add translations of the instructions, follow these steps:</span></span>

    1. <span data-ttu-id="8ecf4-142">Smellt er á **Þýðingar**.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-142">Click **Translations**.</span></span>
    2. <span data-ttu-id="8ecf4-143">Á síðunni sem birtist er smellt á **bæta við**.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-143">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="8ecf4-144">Í listanum sem birtist skal velja tungumálið sem verið er að færa inn í textanum.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-144">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="8ecf4-145">Í svæðið **þýddur texti** skal færa inn textann.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-145">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="8ecf4-146">Til að sérsníða textann geturðu sett inn staðgengla eins og lýst er í skrefi 6.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-146">To personalize the text, you can insert placeholders as described in step 6.</span></span>
    6. <span data-ttu-id="8ecf4-147">Smellið á **Loka**.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-147">Click **Close**.</span></span>

## <a name="specify-the-possible-outcomes-of-a-decision"></a><span data-ttu-id="8ecf4-148">Tilgreina mögulega niðurstöðu ákvörðunar</span><span class="sxs-lookup"><span data-stu-id="8ecf4-148">Specify the possible outcomes of a decision</span></span>

<span data-ttu-id="8ecf4-149">Yfirleitt þegar skjal er tengt þeim sem tekur ákvörðun, fær sá sem tekur ákvörðun spurningu.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-149">Typically, when a document is assigned to a decision maker, the decision maker is asked a question.</span></span> <span data-ttu-id="8ecf4-150">Svar við spurningunni er yfirleitt **Já** eða **Nei**, eða **Satt** eða **Ósatt**.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-150">The answer to this question is usually **Yes** or **No**, or **True** or **False**.</span></span> <span data-ttu-id="8ecf4-151">Fylgið eftirfarandi skrefum til að tilgreina mögulega niðurstöðu handvirku ákvörðuninni.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-151">Follow these steps to specify the possible outcomes of the manual decision.</span></span>

1. <span data-ttu-id="8ecf4-152">Í vinstri glugganum, smelltu á **grunnstillingar**.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-152">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="8ecf4-153">Á flipanum **Niðurstöður** , á **Niðurstaða 1** skal færa inn heiti niðurstöðu eða valkostinn.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-153">On the **Outcomes** tab, in the **Outcome 1** field, enter the name of the outcome, or the option.</span></span>
3. <span data-ttu-id="8ecf4-154">Til að bæta þýðingum við útkomuna skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="8ecf4-154">To add translations of the outcome, follow these steps:</span></span>

    1. <span data-ttu-id="8ecf4-155">Smellt er á **Þýðingar**.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-155">Click **Translations**.</span></span>
    2. <span data-ttu-id="8ecf4-156">Á síðunni sem birtist er smellt á **bæta við**.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-156">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="8ecf4-157">Í listanum sem birtist skal velja tungumálið sem verið er að færa inn í textanum.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-157">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="8ecf4-158">Í svæðið **þýddur texti** skal færa inn textann.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-158">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="8ecf4-159">Smellið á **Loka**.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-159">Click **Close**.</span></span>

4. <span data-ttu-id="8ecf4-160">Á flipanum **Niðurstaða 2** skal færa inn heiti niðurstöðu eða valkostinn.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-160">In the **Outcome 2** field, enter the name of the outcome, or the option.</span></span>
5. <span data-ttu-id="8ecf4-161">Til að bæta þýðingum við útkomuna skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="8ecf4-161">To add translations of the outcome, follow these steps:</span></span>

    1. <span data-ttu-id="8ecf4-162">Smellt er á **Þýðingar**.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-162">Click **Translations**.</span></span>
    2. <span data-ttu-id="8ecf4-163">Á síðunni sem birtist er smellt á **bæta við**.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-163">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="8ecf4-164">Í listanum sem birtist skal velja tungumálið sem verið er að færa inn í textanum.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-164">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="8ecf4-165">Í svæðið **þýddur texti** skal færa inn textann.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-165">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="8ecf4-166">Smellið á **Loka**.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-166">Click **Close**.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="8ecf4-167">Tilgreinið hvenær tilkynningar eru sendar út</span><span class="sxs-lookup"><span data-stu-id="8ecf4-167">Specify when notifications are sent</span></span>

<span data-ttu-id="8ecf4-168">Hægt er að senda tilkynningar til fólks þegar ákvörðun hefur verið tekin, framseld eða stigmögnuð.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-168">You can send notifications to people when a decision has been made, delegated, or escalated.</span></span> <span data-ttu-id="8ecf4-169">Fylgið eftirfarandi skrefum til að tilgreina hvenær senda á út tilkynningar og til hvers tilkynningar eru sendar.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-169">Follow these steps to specify when notifications are sent, and who the notifications are sent to.</span></span>

1. <span data-ttu-id="8ecf4-170">Á svæðinu vinstra megin, smella á **tilkynningar**.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-170">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="8ecf4-171">Veldu gátreitinn sem er við hliðina á tilvikunum sem tilkynningar eiga að vera senda vegna.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-171">Select the check box next to the events that notifications should be sent for:</span></span>

    - <span data-ttu-id="8ecf4-172">**\[Val 1\]** – Úthlutaður notandi hefur valið **\[Val 1\]**.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-172">**\[Choice 1\]** – The assigned user has selected **\[Choice 1\]**.</span></span>
    - <span data-ttu-id="8ecf4-173">**\[Val 2\]** – Úthlutaður notandi hefur valið **\[Val 2\]**.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-173">**\[Choice 2\]** – The assigned user has selected **\[Choice 2\]**.</span></span>
    - <span data-ttu-id="8ecf4-174">**Framselja** – úthlutaður notandi hefur úthlutað ákvörðuninni til annars notanda.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-174">**Delegate** – The assigned user has assigned the decision to another user.</span></span>
    - <span data-ttu-id="8ecf4-175">**Stigmagna** – úthlutaður notandi hefur ekki tekið ákvörðun innan tímarammans.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-175">**Escalate** – The assigned user hasn't made the decision in the allotted time.</span></span>

3. <span data-ttu-id="8ecf4-176">Veljið línu fyrir tilvik sem þú valdir í skrefi 2.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-176">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="8ecf4-177">Á **tilkynningartexti** flipanum í textareitinn, færa inn texta tilkynningarinnar.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-177">On the **Notification text** tab, in the text box, enter the text of the notification.</span></span>
5. <span data-ttu-id="8ecf4-178">Hægt er að sérsníða tilkynningu með því að færa inn staðgengla.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-178">To personalize the notification, you can insert placeholders.</span></span> <span data-ttu-id="8ecf4-179">Staðgenglar eru settir í stað viðeigandi gagna þegar tilkynning birtist notendum.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-179">Placeholders are replaced with appropriate data when the notification is show to users.</span></span> <span data-ttu-id="8ecf4-180">Fylgið eftirfarandi skrefum til að færa inn staðgengil:</span><span class="sxs-lookup"><span data-stu-id="8ecf4-180">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="8ecf4-181">Smellið á textahólfið þar sem staðgengillinn á að birtast.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-181">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="8ecf4-182">Smella á **Setja inn staðgengil**</span><span class="sxs-lookup"><span data-stu-id="8ecf4-182">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="8ecf4-183">Í listanum sem birtist skal velja staðgengilinn til að setja inn.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-183">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="8ecf4-184">Smellt er á **Setja inn**.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-184">Click **Insert**.</span></span>

6. <span data-ttu-id="8ecf4-185">Til að bæta þýðingum við Tilkynningar skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="8ecf4-185">To add translations of the notification, follow these steps:</span></span>

    1. <span data-ttu-id="8ecf4-186">Smellt er á **Þýðingar**.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-186">Click **Translations**.</span></span>
    2. <span data-ttu-id="8ecf4-187">Á síðunni sem birtist er smellt á **bæta við**.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-187">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="8ecf4-188">Í listanum sem birtist skal velja tungumálið sem verið er að færa inn í textanum.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-188">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="8ecf4-189">Í svæðið **þýddur texti** skal færa inn textann.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-189">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="8ecf4-190">Til að sérsníða textann geturðu sett inn staðgengla eins og lýst er í skrefi 5.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-190">To personalize the text, you can insert placeholders as described in step 5.</span></span>
    6. <span data-ttu-id="8ecf4-191">Smellið á **Loka**.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-191">Click **Close**.</span></span>

7. <span data-ttu-id="8ecf4-192">Á **Viðtakanda** flipanum, tilgreinið hverjum tilkynningar eru sendar.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-192">On the **Recipient** tab, specify who the notifications are sent to.</span></span> <span data-ttu-id="8ecf4-193">Veljið einn af valkostum í eftirfarandi töflu, og fylgið svo viðbótarskref fyrir valkostinn áður en farið er í skrefi 8.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-193">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 8.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="8ecf4-194">Valkostur</span><span class="sxs-lookup"><span data-stu-id="8ecf4-194">Option</span></span></th>
    <th><span data-ttu-id="8ecf4-195">Viðtakendur tilkynninga.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-195">Notification recipients</span></span></th>
    <th><span data-ttu-id="8ecf4-196">Viðbótarskref</span><span class="sxs-lookup"><span data-stu-id="8ecf4-196">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="8ecf4-197">Þátttakendur</span><span class="sxs-lookup"><span data-stu-id="8ecf4-197">Participant</span></span></td>
    <td><span data-ttu-id="8ecf4-198">Notendur sem tilheyra tilteknum hópi eða hlutverki</span><span class="sxs-lookup"><span data-stu-id="8ecf4-198">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="8ecf4-199">Eftor að þú velur <strong>viðtakanda</strong>, Á flipanum <strong>Hlutverkamiðað</strong> , á listanum <strong>Gerð þátttakanda</strong> skal velja gerð hóps eða hlutverks til að senda tilkynningu á.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-199">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="8ecf4-200">Í listanum <strong>Þátttakanda</strong> skal velja hópi til að senda tilkynningar til.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-200">In the <strong>Participant</strong> list, select the group or to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="8ecf4-201">Verkflæðisnotandi</span><span class="sxs-lookup"><span data-stu-id="8ecf4-201">Workflow user</span></span></td>
    <td><span data-ttu-id="8ecf4-202">Notendur í núverandi verkflæði</span><span class="sxs-lookup"><span data-stu-id="8ecf4-202">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="8ecf4-203">Eftir að þú velur <strong>verkflæðisnotandi</strong>, á <strong>verkflæðisnotandi</strong> flipanum, á <strong>verkflæðisnotandi</strong> listanum, veldu notandann sem tekur þátt í verkflæði.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-203">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="8ecf4-204">Notandi</span><span class="sxs-lookup"><span data-stu-id="8ecf4-204">User</span></span></td>
    <td><span data-ttu-id="8ecf4-205">Tilteknir notendur</span><span class="sxs-lookup"><span data-stu-id="8ecf4-205">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="8ecf4-206">Eftir að þú velur <strong>Notanda</strong>, skal smellið á <strong>Notanda</strong> flipa.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-206">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="8ecf4-207">Listinn <strong>Tiltækir notendur</strong> inniheldur alla notendur.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-207">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="8ecf4-208">Veldu Notendur til að senda tilkynningar til, og færðu síðan þessa notendur í <strong>Valdir notendur</strong> lista.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-208">Select the users to send notifications to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. <span data-ttu-id="8ecf4-209">Endurtakið skref 3 til 7 hvert tilvik sem valin var í skrefi 2.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-209">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="assign-a-decision"></a><span data-ttu-id="8ecf4-210">Úthluta ákvörðun</span><span class="sxs-lookup"><span data-stu-id="8ecf4-210">Assign a decision</span></span>

<span data-ttu-id="8ecf4-211">Farið að þessum skrefum til að tilgreina á hvern skal úthluta Handvirk Ákvörðun.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-211">Follow these steps to specify who a manual decision should be assigned to.</span></span>

1. <span data-ttu-id="8ecf4-212">Á vinstra svæðinu er smellt á **úthlutun**.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-212">In the left pane, click **Assignment**.</span></span>
2. <span data-ttu-id="8ecf4-213">Á flipanum **úthlutunargerð** , veljið einn af valkostum í eftirfarandi töflu, og fylgið svo viðbótarskref fyrir valkostinn áður en farið er í skrefi 3.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-213">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 3.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="8ecf4-214">Valkostur</span><span class="sxs-lookup"><span data-stu-id="8ecf4-214">Option</span></span></th>
    <th><span data-ttu-id="8ecf4-215">Notendur sem er úthlutað er ákvörðuninni</span><span class="sxs-lookup"><span data-stu-id="8ecf4-215">Users that the decision is assigned to</span></span></th>
    <th><span data-ttu-id="8ecf4-216">Viðbótarskref</span><span class="sxs-lookup"><span data-stu-id="8ecf4-216">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="8ecf4-217">Þátttakendur</span><span class="sxs-lookup"><span data-stu-id="8ecf4-217">Participant</span></span></td>
    <td><span data-ttu-id="8ecf4-218">Notendur sem tilheyra tilteknum hópi eða hlutverki</span><span class="sxs-lookup"><span data-stu-id="8ecf4-218">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="8ecf4-219">Eftir að þú velur <strong>Þátttakanda</strong>á flipanum <strong>Hlutverkamiðað</strong> , á listanum <strong>Gerð þátttakanda</strong> skal velja gerð hóps eða hlutverks til að úthluta ákvörðun á.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-219">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to assign the decision to.</span></span></li>
    <li><span data-ttu-id="8ecf4-220">Í listanum <strong>Þátttakanda</strong> skal velja hópi eða hlutverki til að úthluta ákvörðun á.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-220">In the <strong>Participant</strong> list, select the group or role to assign the decision to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="8ecf4-221">Stigveldi</span><span class="sxs-lookup"><span data-stu-id="8ecf4-221">Hierarchy</span></span></td>
    <td><span data-ttu-id="8ecf4-222">Notendur í tilteknu stigveldi fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="8ecf4-222">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="8ecf4-223">Eftir að þú velur <strong>stigveldi</strong>, á <strong>stigveldishluti</strong> flipanum, á listanum <strong>gerð stigveldis</strong> skal velja gerð stigveldis til að úthluta ákvörðun á.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-223">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to assign the decision to.</span></span></li>
    <li><span data-ttu-id="8ecf4-224">Kerfið verður að sækja svið notendanafna úr stigveldinu.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-224">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="8ecf4-225">Þessi nöfn standa fyrir notendur sem hægt er að úthluta ákvörðun á.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-225">These names represent users that the decision can be assigned to.</span></span> <span data-ttu-id="8ecf4-226">Farðu að þessum skrefum til að tilgreina upphafspunkt og lokapunkt sviðs notendanafna sem kerfið sækir.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-226">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="8ecf4-227">Þegar tilgreina á upphafspunkt skal velja aðila af listanum <strong>Byrja frá og með</strong>.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-227">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="8ecf4-228">Hægt er að tilgreina endapunkt með því að smella á <strong>bæta við skilyrði</strong>.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-228">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="8ecf4-229">Til að færa inn skilyrðu sem ákvarðar hvar í stigveldinu kerfið eigi að hætta að sækja nöfn.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-229">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="8ecf4-230">Á <strong>stigveldisvalkostir</strong> flipanum skal tilgreina hvaða notendur á sviðinu ákvörðun skal úthlutað á:</span><span class="sxs-lookup"><span data-stu-id="8ecf4-230">On the <strong>Hierarchy options</strong> tab, specify which users in the range the decision should be assigned to:</span></span> <ul>
    <li><span data-ttu-id="8ecf4-231"><strong>Úthluta til allra sóttra notenda</strong> - þá er Ákvörðun úthlutað til allra notenda á sviðinu.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-231"><strong>Assign to all users retrieved</strong> – The decision is assigned to all users in the range.</span></span></li>
    <li><span data-ttu-id="8ecf4-232"><strong>Úthluta eingöngu til síðasta sótta notanda</strong> - þá er ákvörðun aðeins úthlutað til síðasta notanda á sviðinu.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-232"><strong>Assign only to last user retrieved</strong> – The decision is assigned to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="8ecf4-233"><strong>Sleppa notendum með eftirfarandi skilyrði</strong> – Ákvörðun er ekki úthlutað á notendur innan sviðsins sem uppfylla ákveðið skilyrði.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-233"><strong>Exclude users with the following condition</strong> – The decision isn't assigned to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="8ecf4-234">Smellið á <strong>bæta við skilyrði</strong> til að skilgreina skilyrðin.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-234">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="8ecf4-235">Verkflæðisnotandi</span><span class="sxs-lookup"><span data-stu-id="8ecf4-235">Workflow user</span></span></td>
    <td><span data-ttu-id="8ecf4-236">Notendur í núverandi verkflæði</span><span class="sxs-lookup"><span data-stu-id="8ecf4-236">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="8ecf4-237">Eftir að þú velur <strong>verkflæðisnotandi</strong>, á <strong>verkflæðisnotandi</strong> flipanum, á <strong>verkflæðisnotandi</strong> listanum, veldu notandann sem tekur þátt í verkflæði.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-237">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="8ecf4-238">Notandi</span><span class="sxs-lookup"><span data-stu-id="8ecf4-238">User</span></span></td>
    <td><span data-ttu-id="8ecf4-239">Tilteknir notendur</span><span class="sxs-lookup"><span data-stu-id="8ecf4-239">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="8ecf4-240">Eftir að þú velur <strong>Notanda</strong>, skal smellið á <strong>Notanda</strong> flipa.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-240">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="8ecf4-241">Listinn <strong>Tiltækir notendur</strong> inniheldur alla notendur.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-241">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="8ecf4-242">Veldu Notendur til að úthluta Ákvörðun á, og færa síðan þessa notendur í <strong>Valdir notendur</strong> lista.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-242">Select the users to assign the decision to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="8ecf4-243">Biðröð</span><span class="sxs-lookup"><span data-stu-id="8ecf4-243">Queue</span></span></td>
    <td><span data-ttu-id="8ecf4-244">Vinnuliðalisti</span><span class="sxs-lookup"><span data-stu-id="8ecf4-244">A work item queue</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="8ecf4-245">Eftir að <strong>Biðröð</strong> er valin, smellið á <strong>byggt á Biðröð</strong> flipa.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-245">After you select <strong>Queue</strong>, click the <strong>Queue based</strong> tab.</span></span></li>
    <li><span data-ttu-id="8ecf4-246">Fylgið eftirfarandi skrefum til að úthluta Ákvörðun á tiltekna biðröð:</span><span class="sxs-lookup"><span data-stu-id="8ecf4-246">To assign the decision to a specific queue, follow these steps:</span></span> <ol>
    <li><span data-ttu-id="8ecf4-247">Í listanum <strong>gerð biðraðar</strong> skal velja <strong>vinnuliðalisti</strong></span><span class="sxs-lookup"><span data-stu-id="8ecf4-247">In the <strong>Queue type</strong> list, select <strong>Work item queues</strong>.</span></span></li>
    <li><span data-ttu-id="8ecf4-248">Í <strong>heiti biðraðar</strong> listanum skal velja biðröðinni.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-248">In the <strong>Queue name</strong> list, select the queue.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="8ecf4-249">Ef tiltekin skilyrði ætti að ákvarða hvaða biðröð Ákvörðun er úthlutað á, skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="8ecf4-249">If a specific condition should determine which queue the decision is assigned to, follow these steps:</span></span> <ol>
    <li><span data-ttu-id="8ecf4-250">Í listanum <strong>gerð biðraðar</strong> skal velja <strong>skilyrtir vinnuliðalistar</strong></span><span class="sxs-lookup"><span data-stu-id="8ecf4-250">In the <strong>Queue type</strong> list, select <strong>Conditional work item queues</strong>.</span></span></li>
    <li><span data-ttu-id="8ecf4-251">Í <strong>heiti biðraðar</strong> listanum skal velja <strong>skilyrt biðröð</strong>.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-251">In the <strong>Queue name</strong> list, select <strong>Conditional queue</strong>.</span></span></li>
    </ol>
    </li>
    </ol>
    <blockquote>[!NOTE] <span data-ttu-id="8ecf4-252">Þessi valkostur er notaður fyrir aðeins nokkur verkflæði, á borð við Málastjórnun.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-252">This option is used for only a few workflows, such as Case management.</span></span></blockquote>
    </td>
    </tr>
    </tbody>
    </table>

3. <span data-ttu-id="8ecf4-253">Á **tímamörk** flipanum, á svæðinu **Tímalengd** , tilgreinið hve mikinn tíma notandi hefur til að taka ákvörðunina.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-253">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to make the decision.</span></span> <span data-ttu-id="8ecf4-254">Veldu einn af eftirfarandi valkostum:</span><span class="sxs-lookup"><span data-stu-id="8ecf4-254">Select one of the following options:</span></span>

    - <span data-ttu-id="8ecf4-255">**Klukkustundir** – færið Inn fjölda klukkustunda sem notandi hefur til að taka ákvörðunina.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-255">**Hours** – Enter the number of hours that the user has to make the decision.</span></span> <span data-ttu-id="8ecf4-256">Þá velja dagatalið sem fyrirtækið notar og færa inn upplýsingar um vinnuviku fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-256">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="8ecf4-257">**Dagar** – færið Inn fjölda daga sem notandi hefur til að taka ákvörðunina.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-257">**Days** – Enter the number of days that the user has to make the decision.</span></span> <span data-ttu-id="8ecf4-258">Þá velja dagatalið sem fyrirtækið notar og færa inn upplýsingar um vinnuviku fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-258">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="8ecf4-259">**Vikur** – færið Inn fjölda vikna sem notandi hefur til að taka ákvörðunina.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-259">**Weeks** – Enter the number of weeks that the user has to make the decision.</span></span>
    - <span data-ttu-id="8ecf4-260">**Mánuðir** — velja daginn og vikuna sem notandinn verður að vera búinn að taka ákvörðunina fyrir.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-260">**Months** – Select the day and week that the user must make the decision by.</span></span> <span data-ttu-id="8ecf4-261">Til dæmis, notandi getur óskað þess að annar notandi taka ákvörðunina fyrir föstudag í þriðju viku mánaðarins.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-261">For example, you might want the user to make the decision by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="8ecf4-262">**Ár** — velja daginn, vikuna og mánuðinn sem notandinn verður að vera búinn að taka ákvörðunina fyrir.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-262">**Years** – Select the day, week, and month that the user must make the decision by.</span></span> <span data-ttu-id="8ecf4-263">Til dæmis, notandi getur óskað þess að annar notandi taka ákvörðunina fyrir föstudag í þriðju viku desembermánaðar.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-263">For example, you might want the user to make the decision by Friday of the third week of December.</span></span>

    <span data-ttu-id="8ecf4-264">Ef notandinn tekur ekki ákvörðunina innan tímarammans, er ákvörðunin komið fram yfir á tíma.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-264">If the user doesn't make the decision in the allotted time, the decision is overdue.</span></span> <span data-ttu-id="8ecf4-265">Ákvörðun sem er komið fram yfir á tíma er stigmagnað, á grundvelli valkostanna sem þú valdir í **stigmögnun** svæðið á síðunni.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-265">A decision that is overdue is escalated, based on the options that you select in the **Escalation** area of the page.</span></span>

## <a name="specify-what-happens-when-a-decision-is-overdue"></a><span data-ttu-id="8ecf4-266">Tilgreina hvað gerist þegar ákvörðun er komið fram yfir á tíma</span><span class="sxs-lookup"><span data-stu-id="8ecf4-266">Specify what happens when a decision is overdue</span></span>

<span data-ttu-id="8ecf4-267">Ef notandinn tekur ekki ákvörðunina innan tímarammans, er ákvörðunin komið fram yfir á tíma.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-267">If a user doesn't make the decision in the allotted time, the decision is overdue.</span></span> <span data-ttu-id="8ecf4-268">Ákvörðun sem er komið fram yfir á tíma má stigmagna, eða úthluta sjálfkrafa á annan notanda.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-268">A decision that is overdue can be escalated, or automatically assigned to another user.</span></span> <span data-ttu-id="8ecf4-269">Fylgið eftirfarandi skrefum til að stigmagna Ákvörðun ef það er komið fram yfir á tíma.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-269">Follow these steps to escalate the decision if it's overdue.</span></span>

1. <span data-ttu-id="8ecf4-270">Á vinstra svæðinu skaltu Smellt á **Stigmagna**.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-270">In the left pane, click **Escalation**.</span></span>
2. <span data-ttu-id="8ecf4-271">Velja skal **Nota stigmögnunarslóð** gátreit til að stofna stigmögnunarslóð.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-271">Select the **Use escalation path** check box to create an escalation path.</span></span> <span data-ttu-id="8ecf4-272">Kerfið mun sjálfkrafa úthluta Ákvörðun til notendanna sem skráðir eru í stigmögnunarslóðinni.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-272">The system automatically assigns the decision to the users who are listed in the escalation path.</span></span> <span data-ttu-id="8ecf4-273">Til dæmis, eftirfarandi töflu sýnir stigmögnunarslóð.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-273">For example, the following table represents an escalation path.</span></span>

    | <span data-ttu-id="8ecf4-274">Röð</span><span class="sxs-lookup"><span data-stu-id="8ecf4-274">Sequence</span></span> | <span data-ttu-id="8ecf4-275">stigmögnunarslóð</span><span class="sxs-lookup"><span data-stu-id="8ecf4-275">Escalation path</span></span>            |
    |----------|----------------------------|
    | <span data-ttu-id="8ecf4-276">1</span><span class="sxs-lookup"><span data-stu-id="8ecf4-276">1</span></span>        | <span data-ttu-id="8ecf4-277">Úthluta til: Dísu</span><span class="sxs-lookup"><span data-stu-id="8ecf4-277">Assign to: Donna</span></span>           |
    | <span data-ttu-id="8ecf4-278">2</span><span class="sxs-lookup"><span data-stu-id="8ecf4-278">2</span></span>        | <span data-ttu-id="8ecf4-279">Úthluta til: Erlu</span><span class="sxs-lookup"><span data-stu-id="8ecf4-279">Assign to: Erin</span></span>            |
    | <span data-ttu-id="8ecf4-280">3</span><span class="sxs-lookup"><span data-stu-id="8ecf4-280">3</span></span>        | <span data-ttu-id="8ecf4-281">Endanleg aðgerð: \[Val 1\]</span><span class="sxs-lookup"><span data-stu-id="8ecf4-281">Final action: \[Choice 1\]</span></span> |

    <span data-ttu-id="8ecf4-282">Í þessu dæmi mun kerfið sjálfkrafa úthluta Ákvörðun sem er komið fram yfir á tíma til Dísu.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-282">In this example, the system assigns the overdue decision to Donna.</span></span> <span data-ttu-id="8ecf4-283">Ef Dísu tekur ekki ákvörðun innan tímarammans, úthlutar kerfið ákvörðuninni til Erlu.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-283">If Donna doesn't make the decision in the allotted time, the system assigns the decision to Erin.</span></span> <span data-ttu-id="8ecf4-284">Ef Erla tekur ekki ákvörðun innan tímarammans, Velur kerfið **\[Val 1\]** sem ákvörðun.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-284">If Erin doesn't make the decision in the allotted time, the system selects **\[Choice 1\]** as the decision.</span></span>

3. <span data-ttu-id="8ecf4-285">Til að bæta notanda við stigmögnunarslóð, smella **bæta við stigmögnun**.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-285">To add a user to the escalation path, click **Add escalation**.</span></span> <span data-ttu-id="8ecf4-286">Veljið einn af valkostum í eftirfarandi töflu, og fylgið svo viðbótarskref fyrir valkostinn áður en farið er í skrefi 4.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-286">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 4.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="8ecf4-287">Valkostur</span><span class="sxs-lookup"><span data-stu-id="8ecf4-287">Option</span></span></th>
    <th><span data-ttu-id="8ecf4-288">Notendur sem Ákvörðun er stigmagnað fyrir</span><span class="sxs-lookup"><span data-stu-id="8ecf4-288">Users that the decision is escalated to</span></span></th>
    <th><span data-ttu-id="8ecf4-289">Viðbótarskref</span><span class="sxs-lookup"><span data-stu-id="8ecf4-289">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="8ecf4-290">Stigveldi</span><span class="sxs-lookup"><span data-stu-id="8ecf4-290">Hierarchy</span></span></td>
    <td><span data-ttu-id="8ecf4-291">Notendur í tilteknu stigveldi fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="8ecf4-291">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="8ecf4-292">Eftir að þú velur <strong>stigveldi</strong>, á <strong>stigveldishluti</strong> flipanum, á listanum <strong>gerð stigveldis</strong> skal velja gerð stigveldis til að stigmagna ákvörðun fyrir.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-292">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to escalate the decision to.</span></span></li>
    <li><span data-ttu-id="8ecf4-293">Kerfið verður að sækja svið notendanafna úr stigveldinu.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-293">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="8ecf4-294">Þessi nöfn standa fyrir notendur sem hægt er stigmagna Ákvörðun fyrir.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-294">These names represent users that the decision can be escalated to.</span></span> <span data-ttu-id="8ecf4-295">Farðu að þessum skrefum til að tilgreina upphafspunkt og lokapunkt sviðs notendanafna sem kerfið sækir.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-295">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="8ecf4-296">Þegar tilgreina á upphafspunkt skal velja aðila af listanum <strong>Byrja frá og með</strong>.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-296">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="8ecf4-297">Hægt er að tilgreina endapunkt með því að smella á <strong>bæta við skilyrði</strong>.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-297">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="8ecf4-298">Til að færa inn skilyrðu sem ákvarðar hvar í stigveldinu kerfið eigi að hætta að sækja nöfn.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-298">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="8ecf4-299">Á <strong>stigveldisvalkostir</strong> flipanum skal tilgreina hvaða notendur á sviðinu ákvörðun skal stigmagnað fyrir:</span><span class="sxs-lookup"><span data-stu-id="8ecf4-299">On the <strong>Hierarchy options</strong> tab, specify which users in the range the decision should be escalated to:</span></span> <ul>
    <li><span data-ttu-id="8ecf4-300"><strong>Úthluta til allra sóttra notenda</strong> - þá er ákvörðun stigmagnað fyrir allra notenda á sviðinu.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-300"><strong>Assign to all users retrieved</strong> – The decision is escalated to all users in the range.</span></span></li>
    <li><span data-ttu-id="8ecf4-301"><strong>Úthluta eingöngu til síðasta sótta notanda</strong> - þá er ákvörðun stigmagnað aðeins til síðasta notanda á sviðinu.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-301"><strong>Assign only to last user retrieved</strong> – The decision is escalated to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="8ecf4-302"><strong>Sleppa notendum með eftirfarandi skilyrði</strong> – Ákvörðun er ekki stigmagnað fyrir neina notendur innan sviðsins sem uppfylla ákveðið skilyrði.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-302"><strong>Exclude users with the following condition:</strong> – The decision isn't escalated to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="8ecf4-303">Smellið á <strong>bæta við skilyrði</strong> til að skilgreina skilyrðin.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-303">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="8ecf4-304">Verkflæðisnotandi</span><span class="sxs-lookup"><span data-stu-id="8ecf4-304">Workflow user</span></span></td>
    <td><span data-ttu-id="8ecf4-305">Notendur í núverandi verkflæði</span><span class="sxs-lookup"><span data-stu-id="8ecf4-305">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="8ecf4-306">Eftir að þú velur <strong>verkflæðisnotandi</strong>, á <strong>verkflæðisnotandi</strong> flipanum, á <strong>verkflæðisnotandi</strong> listanum, veldu notandann sem tekur þátt í verkflæði.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-306">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="8ecf4-307">Notandi</span><span class="sxs-lookup"><span data-stu-id="8ecf4-307">User</span></span></td>
    <td><span data-ttu-id="8ecf4-308">Tilteknir notendur</span><span class="sxs-lookup"><span data-stu-id="8ecf4-308">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="8ecf4-309">Eftir að þú velur <strong>Notanda</strong>, skal smellið á <strong>Notanda</strong> flipa.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-309">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="8ecf4-310">Listinn <strong>Tiltækir notendur</strong> inniheldur alla notendur.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-310">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="8ecf4-311">Veldu Notendur til að stigmagna Ákvörðun fyrir, og færðu síðan þessa notendur í <strong>Valdir notendur</strong> lista.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-311">Select the users to escalate the decision to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

4. <span data-ttu-id="8ecf4-312">Á **tímamörk** flipanum, á svæðinu **Tímalengd** , tilgreinið hve mikinn tíma notandi hefur til að taka ákvörðunina.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-312">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to make the decision.</span></span> <span data-ttu-id="8ecf4-313">Veldu einn af eftirfarandi valkostum:</span><span class="sxs-lookup"><span data-stu-id="8ecf4-313">Select one of the following options:</span></span>

    - <span data-ttu-id="8ecf4-314">**Klukkustundir** – færið Inn fjölda klukkustunda sem notandi hefur til að taka ákvörðunina.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-314">**Hours** – Enter the number of hours that the user has to make the decision.</span></span> <span data-ttu-id="8ecf4-315">Þá velja dagatalið sem fyrirtækið notar og færa inn upplýsingar um vinnuviku fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-315">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="8ecf4-316">**Dagar** – færið Inn fjölda daga sem notandi hefur til að taka ákvörðunina.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-316">**Days** – Enter the number of days that the user has to make the decision.</span></span> <span data-ttu-id="8ecf4-317">Þá velja dagatalið sem fyrirtækið notar og færa inn upplýsingar um vinnuviku fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-317">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="8ecf4-318">**Vikur** – færið Inn fjölda vikna sem notandi hefur til að taka ákvörðunina.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-318">**Weeks** – Enter the number of weeks that the user has to make the decision.</span></span>
    - <span data-ttu-id="8ecf4-319">**Mánuðir** — velja daginn og vikuna sem notandinn verður að vera búinn að taka ákvörðunina fyrir.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-319">**Months** – Select the day and week that the user must make the decision by.</span></span> <span data-ttu-id="8ecf4-320">Til dæmis, notandi getur óskað þess að annar notandi taka ákvörðunina fyrir föstudag í þriðju viku mánaðarins.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-320">For example, you might want the user to make the decision by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="8ecf4-321">**Ár** — velja daginn, vikuna og mánuðinn sem notandinn verður að vera búinn að taka ákvörðunina fyrir.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-321">**Years** – Select the day, week, and month that the user must make the decision by.</span></span> <span data-ttu-id="8ecf4-322">Til dæmis, notandi getur óskað þess að annar notandi taka ákvörðunina fyrir föstudag í þriðju viku desembermánaðar.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-322">For example, you might want the user to make the decision by Friday of the third week of December.</span></span>

5. <span data-ttu-id="8ecf4-323">Endurtakið skref 3 til 4 fyrir hvern notanda sem á að bæta við stigmögnunarslóð.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-323">Repeat steps 3 through 4 for each user that should be added to the escalation path.</span></span> <span data-ttu-id="8ecf4-324">Hægt er að breyta röðun notenda.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-324">You can change the order of the users.</span></span>
6. <span data-ttu-id="8ecf4-325">Ef notendunum í hækkunarslóðinni taka ekki ákvörðun innan tímarammans, tekur kerfið ákvörðunina.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-325">If the users in the escalation path don't make the decision in the allotted time, the system makes the decision.</span></span> <span data-ttu-id="8ecf4-326">Til að tilgreina valkostinn sem kerfið velur , veldu línuna **Aðgerð** , og síðan á **Ljúka aðgerð** flipanum, veljið valkost.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-326">To specify the option that the system selects, select the **Action** row, and then, on the **End action** tab, select an option.</span></span>

## <a name="set-a-time-limit"></a><span data-ttu-id="8ecf4-327">Setja upp tímamörk</span><span class="sxs-lookup"><span data-stu-id="8ecf4-327">Set a time limit</span></span>

<span data-ttu-id="8ecf4-328">Fylgið eftirfarandi skrefum ef verður að taka ákvörðunina innan tiltekins tíma.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-328">Follow these steps if the decision must be made in a specific time.</span></span>

> [!NOTE]
> <span data-ttu-id="8ecf4-329">Valkostirnir sem valdir eru í þessu ferli munu hnekkja valkostunum sem valdir voru í svæðunum **Úthlutun** og **Stigmögnun** á síðunni.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-329">The options that you select in this procedure override the options that you selected in the **Assignment** and **Escalation** areas of the page.</span></span>

1. <span data-ttu-id="8ecf4-330">Í vinstri glugganum, smelltu á **ítarlegar stillingar**.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-330">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="8ecf4-331">Veldu gátreitinn **Stilla tímamörk verkflæðiseiningar**</span><span class="sxs-lookup"><span data-stu-id="8ecf4-331">Select the **Set a time limit for the workflow element** check box.</span></span>
3. <span data-ttu-id="8ecf4-332">Í reitnum **tímalengd** tilgreinið þegar Ákvörðun á að vera tekin.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-332">In the **Duration** field, specify when the decision must be made.</span></span> <span data-ttu-id="8ecf4-333">Veldu einn af eftirfarandi valkostum:</span><span class="sxs-lookup"><span data-stu-id="8ecf4-333">Select one of the following options:</span></span>

    - <span data-ttu-id="8ecf4-334">**Klukkustundir** - Færa þarf inn fjölda klukkustunda.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-334">**Hours** – Enter the number of hours.</span></span> <span data-ttu-id="8ecf4-335">Þá velja dagatalið sem fyrirtækið notar og færa inn upplýsingar um vinnuviku fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-335">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="8ecf4-336">**Dagar** - Færið inn fjölda daga.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-336">**Days** – Enter the number of days.</span></span> <span data-ttu-id="8ecf4-337">Þá velja dagatalið sem fyrirtækið notar og færa inn upplýsingar um vinnuviku fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-337">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="8ecf4-338">**Vikur** - Færið inn fjölda vikna.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-338">**Weeks** – Enter the number of weeks.</span></span>
    - <span data-ttu-id="8ecf4-339">**Mánuðir** — velja daginn og vikuna sem verður að vera búið að taka ákvörðunina fyrir.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-339">**Months** – Select the day and week that the decision must be made by.</span></span> <span data-ttu-id="8ecf4-340">Til dæmis getur átt að vera búið að taka ákvörðunina fyrir föstudaginn í þriðju viku mánaðarins.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-340">For example, you might want the decision to be made by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="8ecf4-341">**Ár** — velja daginn, vikuna og mánuðinn sem verður að vera búið að taka ákvörðunina fyrir.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-341">**Years** – Select the day, week, and month that the decision must be made by.</span></span> <span data-ttu-id="8ecf4-342">Til dæmis getur átt að vera búið að taka ákvörðunina fyrir föstudaginn í þriðju viku desembermánaðar.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-342">For example, you might want the decision to be made by Friday of the third week of December.</span></span>

4. <span data-ttu-id="8ecf4-343">Ef farið er yfir tímamörkin mun kerfið taka ákvörðunina vegna verksins.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-343">If the time limit is exceeded, the system makes the decision.</span></span> <span data-ttu-id="8ecf4-344">Veljið Valkost, sem kerfið á að velja, í listanum **Aðgerðir**.</span><span class="sxs-lookup"><span data-stu-id="8ecf4-344">In the **Action** list, select the option that the system should select.</span></span>