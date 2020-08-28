---
title: Skilgreina handvirk verk í verkflæði
description: Þetta efnisatriði útskýrir hvernig skilgreina á eiginleika handvirks verks.
author: ChrisGarty
manager: AnnBe
ms.date: 08/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 192191
ms.assetid: 27f1afde-ff26-4b6f-8c11-27ec49130bbb
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2cae815bede98df7e5b937f6ffda99fa4ffed937
ms.sourcegitcommit: e55efd2f62bf60f678108c09ad4701a76b20cc68
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/17/2020
ms.locfileid: "3698220"
---
# <a name="configure-manual-tasks-in-a-workflow"></a><span data-ttu-id="f1360-103">Skilgreina handvirk verk í verkflæði</span><span class="sxs-lookup"><span data-stu-id="f1360-103">Configure manual tasks in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f1360-104">Þetta efnisatriði útskýrir hvernig skilgreina á eiginleika handvirks verks.</span><span class="sxs-lookup"><span data-stu-id="f1360-104">This topic explains how to configure the properties for a manual task.</span></span>

<span data-ttu-id="f1360-105">Til að skilgreina handvirkt verk í verkflæðisritlinum, hægrismellt er á verkið og smellið síðan á **Eiginleika** til að opna **Eiginleika** síðu.</span><span class="sxs-lookup"><span data-stu-id="f1360-105">To configure a manual task in the workflow editor, right-click the task, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="f1360-106">Notið síðan eftirfarandi ferli til að stilla eiginleika fyrir handvirkt verk.</span><span class="sxs-lookup"><span data-stu-id="f1360-106">Then use the following procedures to configure the properties for the manual task.</span></span>

## <a name="name-the-task"></a><span data-ttu-id="f1360-107">Gefa verkinu heiti</span><span class="sxs-lookup"><span data-stu-id="f1360-107">Name the task</span></span>

<span data-ttu-id="f1360-108">Fylgið þessum skrefum til að færa inn heiti á handvirku verki.</span><span class="sxs-lookup"><span data-stu-id="f1360-108">Follow these steps to enter a name for the manual task.</span></span>

1. <span data-ttu-id="f1360-109">Í vinstri glugganum, smelltu á **grunnstillingar**.</span><span class="sxs-lookup"><span data-stu-id="f1360-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="f1360-110">Á svæðinu **Heiti** skal færa inn einkvæmt heiti fyrir verkið.</span><span class="sxs-lookup"><span data-stu-id="f1360-110">In the **Name** field, enter a unique name for the task.</span></span>

## <a name="enter-a-subject-line-and-instructions"></a><span data-ttu-id="f1360-111">Slá inn efnislínu og fyrirmæli</span><span class="sxs-lookup"><span data-stu-id="f1360-111">Enter a subject line and instructions</span></span>

<span data-ttu-id="f1360-112">Veita verður þeim notendum, sem úthlutað er þetta verk, efnislínu og fyrirmæli.</span><span class="sxs-lookup"><span data-stu-id="f1360-112">You must provide a subject line and instructions to users who are assigned to the task.</span></span> <span data-ttu-id="f1360-113">Til dæmis, ef verið er að skilgreina verk fyrir innkaupabeiðnir, mun notanda sem er úthlutað á verkið sjá efnislínuna og fyrirmælin á **Innkaupabeiðnir** síðunni.</span><span class="sxs-lookup"><span data-stu-id="f1360-113">For example, if you're configuring a task for purchase requisitions, the user who is assigned to the task sees the subject line and instructions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="f1360-114">Efnislínuna birtist á skilaboðaslánni á síðunni.</span><span class="sxs-lookup"><span data-stu-id="f1360-114">The subject line appears in a message bar on the page.</span></span> <span data-ttu-id="f1360-115">Notandinn getur síðan smellt á teiknið á skilaboðaslánni til að sjá leiðbeiningar.</span><span class="sxs-lookup"><span data-stu-id="f1360-115">The user can then click the icon in the message bar to view the instructions.</span></span> <span data-ttu-id="f1360-116">Fylgið eftirfarandi skrefum til að slá inn efnislínu og fyrirmæli.</span><span class="sxs-lookup"><span data-stu-id="f1360-116">Follow these steps to enter a subject line and instructions.</span></span>

1. <span data-ttu-id="f1360-117">Í vinstri glugganum, smelltu á **grunnstillingar**.</span><span class="sxs-lookup"><span data-stu-id="f1360-117">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="f1360-118">Í **efni vinnuliðs** svæðinu, færið inn efnislínuna.</span><span class="sxs-lookup"><span data-stu-id="f1360-118">In the **Work item subject** field, enter the subject line.</span></span>
3. <span data-ttu-id="f1360-119">Til að sérsníða efnislínuna, er hægt að færa inn staðgengla.</span><span class="sxs-lookup"><span data-stu-id="f1360-119">To personalize the subject line, you can insert placeholders.</span></span> <span data-ttu-id="f1360-120">Staðgenglar eru settir í stað viðeigandi gagna þegar efnislínan birtist notendum.</span><span class="sxs-lookup"><span data-stu-id="f1360-120">Placeholders are replaced with appropriate data when the subject line is shown to users.</span></span> <span data-ttu-id="f1360-121">Fylgið eftirfarandi skrefum til að færa inn staðgengil:</span><span class="sxs-lookup"><span data-stu-id="f1360-121">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="f1360-122">Smellið á textahólfið þar sem staðgengillinn á að birtast.</span><span class="sxs-lookup"><span data-stu-id="f1360-122">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="f1360-123">Smella á **Setja inn staðgengil**</span><span class="sxs-lookup"><span data-stu-id="f1360-123">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="f1360-124">Í listanum sem birtist skal velja staðgengilinn til að setja inn.</span><span class="sxs-lookup"><span data-stu-id="f1360-124">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="f1360-125">Smellt er á **Setja inn**.</span><span class="sxs-lookup"><span data-stu-id="f1360-125">Click **Insert**.</span></span>

4. <span data-ttu-id="f1360-126">Til að bæta þýðingum við efnislínuna skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="f1360-126">To add translations of the subject line, follow these steps:</span></span>

    1. <span data-ttu-id="f1360-127">Smellt er á **Þýðingar**.</span><span class="sxs-lookup"><span data-stu-id="f1360-127">Click **Translations**.</span></span>
    2. <span data-ttu-id="f1360-128">Á síðunni sem birtist er smellt á **bæta við**.</span><span class="sxs-lookup"><span data-stu-id="f1360-128">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="f1360-129">Í listanum sem birtist skal velja tungumálið sem verið er að færa inn í textanum.</span><span class="sxs-lookup"><span data-stu-id="f1360-129">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="f1360-130">Í svæðið **þýddur texti** skal færa inn textann.</span><span class="sxs-lookup"><span data-stu-id="f1360-130">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="f1360-131">Til að sérsníða textann geturðu sett inn staðgengla eins og lýst er í skrefi 3.</span><span class="sxs-lookup"><span data-stu-id="f1360-131">To personalize the text, you can insert placeholders as described in step 3.</span></span>
    6. <span data-ttu-id="f1360-132">Smellið á **Loka**.</span><span class="sxs-lookup"><span data-stu-id="f1360-132">Click **Close**.</span></span>

5. <span data-ttu-id="f1360-133">Í **leiðbeiningar vinnuliðs** svæðinu, færið inn leiðbeiningar.</span><span class="sxs-lookup"><span data-stu-id="f1360-133">In the **Work item instructions** field, enter the instructions.</span></span>
6. <span data-ttu-id="f1360-134">Hægt er að sérsníða leiðbeiningarnar með því að færa inn staðgengla.</span><span class="sxs-lookup"><span data-stu-id="f1360-134">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="f1360-135">Staðgenglar eru settir í stað viðeigandi gagna þegar leiðbeiningar birtist notendum.</span><span class="sxs-lookup"><span data-stu-id="f1360-135">Placeholders are replaced with appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="f1360-136">Fylgið eftirfarandi skrefum til að færa inn staðgengil:</span><span class="sxs-lookup"><span data-stu-id="f1360-136">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="f1360-137">Smellið á textahólfið þar sem staðgengillinn á að birtast.</span><span class="sxs-lookup"><span data-stu-id="f1360-137">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="f1360-138">Smella á **Setja inn staðgengil**</span><span class="sxs-lookup"><span data-stu-id="f1360-138">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="f1360-139">Í listanum sem birtist skal velja staðgengilinn til að setja inn.</span><span class="sxs-lookup"><span data-stu-id="f1360-139">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="f1360-140">Smellt er á **Setja inn**.</span><span class="sxs-lookup"><span data-stu-id="f1360-140">Click **Insert**.</span></span>

7. <span data-ttu-id="f1360-141">Til að bæta þýðingum við leiðbeiningar skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="f1360-141">To add translations of the instructions, follow these steps:</span></span>

    1. <span data-ttu-id="f1360-142">Smellt er á **Þýðingar**.</span><span class="sxs-lookup"><span data-stu-id="f1360-142">Click **Translations**.</span></span>
    2. <span data-ttu-id="f1360-143">Á síðunni sem birtist er smellt á **bæta við**.</span><span class="sxs-lookup"><span data-stu-id="f1360-143">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="f1360-144">Í listanum sem birtist skal velja tungumálið sem verið er að færa inn í textanum.</span><span class="sxs-lookup"><span data-stu-id="f1360-144">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="f1360-145">Í svæðið **þýddur texti** skal færa inn textann.</span><span class="sxs-lookup"><span data-stu-id="f1360-145">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="f1360-146">Til að sérsníða textann geturðu sett inn staðgengla eins og lýst er í skrefi 6.</span><span class="sxs-lookup"><span data-stu-id="f1360-146">To personalize the text, you can insert placeholders as described in step 6.</span></span>
    6. <span data-ttu-id="f1360-147">Smellið á **Loka**.</span><span class="sxs-lookup"><span data-stu-id="f1360-147">Click **Close**.</span></span>

## <a name="assign-the-task"></a><span data-ttu-id="f1360-148">Verkinu úthlutað</span><span class="sxs-lookup"><span data-stu-id="f1360-148">Assign the task</span></span>

<span data-ttu-id="f1360-149">Farið að þessum skrefum til að tilgreina á hvern skal úthluta Handvirk verk.</span><span class="sxs-lookup"><span data-stu-id="f1360-149">Follow these steps to specify who the manual task should be assigned to.</span></span>

1. <span data-ttu-id="f1360-150">Á vinstra svæðinu er smellt á **úthlutun**.</span><span class="sxs-lookup"><span data-stu-id="f1360-150">In the left pane, click **Assignment**.</span></span>
2. <span data-ttu-id="f1360-151">Á flipanum **úthlutunargerð** , veljið einn af valkostum í eftirfarandi töflu, og fylgið svo viðbótarskref fyrir valkostinn áður en farið er í skrefi 3.</span><span class="sxs-lookup"><span data-stu-id="f1360-151">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 3.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="f1360-152">Valkostur</span><span class="sxs-lookup"><span data-stu-id="f1360-152">Option</span></span></th>
    <th><span data-ttu-id="f1360-153">Notandi sem verkið er úthlutað á.</span><span class="sxs-lookup"><span data-stu-id="f1360-153">Users that the task is assigned to</span></span></th>
    <th><span data-ttu-id="f1360-154">Viðbótarskref</span><span class="sxs-lookup"><span data-stu-id="f1360-154">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="f1360-155">Þátttakendur</span><span class="sxs-lookup"><span data-stu-id="f1360-155">Participant</span></span></td>
    <td><span data-ttu-id="f1360-156">Notendur sem tilheyra tilteknum hópi eða hlutverki</span><span class="sxs-lookup"><span data-stu-id="f1360-156">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="f1360-157">Eftir að þú velur <strong>Þátttakanda</strong>á flipanum <strong>Hlutverkamiðað</strong> , á listanum <strong>Gerð þátttakanda</strong> skal velja gerð hóps eða hlutverks til að úthluta Verk á.</span><span class="sxs-lookup"><span data-stu-id="f1360-157">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to assign the task to.</span></span></li>
    <li><span data-ttu-id="f1360-158">Í listanum <strong>Þátttakanda</strong> skal velja hópi eða hlutverki til að úthluta Verk á.</span><span class="sxs-lookup"><span data-stu-id="f1360-158">In the <strong>Participant</strong> list, select the group or role to assign the task to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="f1360-159">Stigveldi</span><span class="sxs-lookup"><span data-stu-id="f1360-159">Hierarchy</span></span></td>
    <td><span data-ttu-id="f1360-160">Notendur í tilteknu stigveldi fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="f1360-160">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="f1360-161">Eftir að þú velur <strong>stigveldi</strong>, á <strong>stigveldishluti</strong> flipanum, á listanum <strong>gerð stigveldis</strong> skal velja gerð stigveldis til að úthluta verk á.</span><span class="sxs-lookup"><span data-stu-id="f1360-161">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to assign the task to.</span></span></li>
    <li><span data-ttu-id="f1360-162">Kerfið verður að sækja svið notendanafna úr stigveldinu.</span><span class="sxs-lookup"><span data-stu-id="f1360-162">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="f1360-163">Þessi nöfn standa fyrir notendur sem hægt er að úthluta verk á.</span><span class="sxs-lookup"><span data-stu-id="f1360-163">These names represent users that the task can be assigned to.</span></span> <span data-ttu-id="f1360-164">Farðu að þessum skrefum til að tilgreina upphafspunkt og lokapunkt sviðs notendanafna sem kerfið sækir.</span><span class="sxs-lookup"><span data-stu-id="f1360-164">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="f1360-165">Þegar tilgreina á upphafspunkt skal velja aðila af listanum <strong>Byrja frá og með</strong>.</span><span class="sxs-lookup"><span data-stu-id="f1360-165">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="f1360-166">Hægt er að tilgreina endapunkt með því að smella á <strong>bæta við skilyrði</strong>.</span><span class="sxs-lookup"><span data-stu-id="f1360-166">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="f1360-167">Til að færa inn skilyrðu sem ákvarðar hvar í stigveldinu kerfið eigi að hætta að sækja nöfn.</span><span class="sxs-lookup"><span data-stu-id="f1360-167">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="f1360-168">Á <strong>stigveldisvalkostir</strong> flipanum skal tilgreina hvaða notendur á sviðinu verki skal úthlutað á:</span><span class="sxs-lookup"><span data-stu-id="f1360-168">On the <strong>Hierarchy options</strong> tab, specify which users in the range the task should be assigned to:</span></span> <ul>
    <li><span data-ttu-id="f1360-169"><strong>Úthluta til allra sóttra notenda</strong> - þá er verkinu úthlutað til allra notenda á sviðinu.</span><span class="sxs-lookup"><span data-stu-id="f1360-169"><strong>Assign to all users retrieved</strong> – The task is assigned to all users in the range.</span></span></li>
    <li><span data-ttu-id="f1360-170"><strong>Úthluta eingöngu til síðasta sótta notanda</strong> - þá er verkinu aðeins úthlutað til síðasta notanda á sviðinu.</span><span class="sxs-lookup"><span data-stu-id="f1360-170"><strong>Assign only to last user retrieved</strong> – The task is assigned to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="f1360-171"><strong>Sleppa notendum með eftirfarandi skilyrði</strong> – verkið er ekki úthlutað á notendur innan sviðsins sem uppfylla ákveðið skilyrði.</span><span class="sxs-lookup"><span data-stu-id="f1360-171"><strong>Exclude users with the following condition</strong> – The task isn't assigned to users in the range who meet a specific condition.</span></span> <span data-ttu-id="f1360-172">Smellið á <strong>bæta við skilyrði</strong> til að skilgreina skilyrðin.</span><span class="sxs-lookup"><span data-stu-id="f1360-172">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="f1360-173">Verkflæðisnotandi</span><span class="sxs-lookup"><span data-stu-id="f1360-173">Workflow user</span></span></td>
    <td><span data-ttu-id="f1360-174">Notendur í núverandi verkflæði</span><span class="sxs-lookup"><span data-stu-id="f1360-174">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="f1360-175">Eftir að þú velur <strong>verkflæðisnotandi</strong>, á <strong>verkflæðisnotandi</strong> flipanum, á <strong>verkflæðisnotandi</strong> listanum, veldu notandann sem tekur þátt í verkflæði.</span><span class="sxs-lookup"><span data-stu-id="f1360-175">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="f1360-176">Notandi</span><span class="sxs-lookup"><span data-stu-id="f1360-176">User</span></span></td>
    <td><span data-ttu-id="f1360-177">Tilteknir notendur</span><span class="sxs-lookup"><span data-stu-id="f1360-177">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="f1360-178">Eftir að þú velur <strong>Notanda</strong>, skal smellið á <strong>Notanda</strong> flipa.</span><span class="sxs-lookup"><span data-stu-id="f1360-178">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="f1360-179">Listinn <strong>Tiltækir notendur</strong> inniheldur alla notendur.</span><span class="sxs-lookup"><span data-stu-id="f1360-179">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="f1360-180">Veldu Notendur til að úthluta verki á, og færa síðan þessa notendur í <strong>Valdir notendur</strong> lista.</span><span class="sxs-lookup"><span data-stu-id="f1360-180">Select the users to assign the task to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="f1360-181">Biðröð</span><span class="sxs-lookup"><span data-stu-id="f1360-181">Queue</span></span></td>
    <td><span data-ttu-id="f1360-182">Vinnuliðalisti</span><span class="sxs-lookup"><span data-stu-id="f1360-182">A work item queue</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="f1360-183">Eftir að <strong>Biðröð</strong> er valin, smellið á <strong>byggt á Biðröð</strong> flipa.</span><span class="sxs-lookup"><span data-stu-id="f1360-183">After you select <strong>Queue</strong>, click the <strong>Queue based</strong> tab.</span></span></li>
    <li><span data-ttu-id="f1360-184">Fylgið eftirfarandi skrefum til að úthluta verki á tiltekna biðröð:</span><span class="sxs-lookup"><span data-stu-id="f1360-184">To assign the task to a specific queue, follow these steps:</span></span> <ol>
    <li><span data-ttu-id="f1360-185">Í listanum <strong>gerð biðraðar</strong> skal velja <strong>vinnuliðalisti</strong></span><span class="sxs-lookup"><span data-stu-id="f1360-185">In the <strong>Queue type</strong> list, select <strong>Work item queues</strong>.</span></span></li>
    <li><span data-ttu-id="f1360-186">Í <strong>heiti biðraðar</strong> listanum skal velja biðröðinni.</span><span class="sxs-lookup"><span data-stu-id="f1360-186">In the <strong>Queue name</strong> list, select the queue.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="f1360-187">Ef tiltekin skilyrði ætti að ákvarða hvaða biðröð verki er úthlutað á, skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="f1360-187">If a specific condition should determine which queue the task is assigned to, follow these steps:</span></span> <ol>
    <li><span data-ttu-id="f1360-188">Í listanum <strong>gerð biðraðar</strong> skal velja <strong>skilyrtir vinnuliðalistar</strong></span><span class="sxs-lookup"><span data-stu-id="f1360-188">In the <strong>Queue type</strong> list, select <strong>Conditional work item queues</strong>.</span></span></li>
    <li><span data-ttu-id="f1360-189">Í <strong>heiti biðraðar</strong> listanum skal velja <strong>skilyrt biðröð</strong>.</span><span class="sxs-lookup"><span data-stu-id="f1360-189">In the <strong>Queue name</strong> list, select <strong>Conditional queue</strong>.</span></span></li>
    </ol>
    </li>
    </ol>
    <blockquote>[!NOTE] <span data-ttu-id="f1360-190">Þessi valkostur er notaður fyrir aðeins nokkur verkflæði, á borð við Málastjórnun.</span><span class="sxs-lookup"><span data-stu-id="f1360-190">This option is used for only a few workflows, such as Case management.</span></span></blockquote>
    </td>
    </tr>
    </tbody>
    </table>

3. <span data-ttu-id="f1360-191">Á **tímamörk** flipanum, á svæðinu **Tímalengd** , tilgreinið hve mikinn tíma notandi hefur til að klára verkið.</span><span class="sxs-lookup"><span data-stu-id="f1360-191">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to complete the task.</span></span> <span data-ttu-id="f1360-192">Veldu einn af eftirfarandi valkostum:</span><span class="sxs-lookup"><span data-stu-id="f1360-192">Select one of the following options:</span></span>

    - <span data-ttu-id="f1360-193">**Klukkustundir** – færið Inn fjölda klukkustunda sem notandi hefur til að klára verkið.</span><span class="sxs-lookup"><span data-stu-id="f1360-193">**Hours** – Enter the number of hours that the user has to complete the task.</span></span> <span data-ttu-id="f1360-194">Þá velja dagatalið sem fyrirtækið notar og færa inn upplýsingar um vinnuviku fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="f1360-194">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="f1360-195">**Dagar** – færið Inn fjölda daga sem notandi hefur til að klára verkið.</span><span class="sxs-lookup"><span data-stu-id="f1360-195">**Days** – Enter the number of days that the user has to complete the task.</span></span> <span data-ttu-id="f1360-196">Þá velja dagatalið sem fyrirtækið notar og færa inn upplýsingar um vinnuviku fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="f1360-196">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="f1360-197">**Vikur** – færið Inn fjölda vikna sem notandi hefur til að klára verkið.</span><span class="sxs-lookup"><span data-stu-id="f1360-197">**Weeks** – Enter the number of weeks that the user has to complete the task.</span></span>
    - <span data-ttu-id="f1360-198">**Mánuðir** — velja daginn og vikuna sem notandinn verður að vera búinn að klára verkið fyrir.</span><span class="sxs-lookup"><span data-stu-id="f1360-198">**Months** – Select the day and week that the user must complete the task by.</span></span> <span data-ttu-id="f1360-199">Til dæmis getur notandinn átt að vera búinn að ljúka verkinu fyrir föstudaginn í þriðju viku mánaðarins.</span><span class="sxs-lookup"><span data-stu-id="f1360-199">For example, you might want the user to complete the task by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="f1360-200">**Ár** — velja daginn, vikuna og mánuðinn sem notandinn verður að vera búinn að klára verkið fyrir.</span><span class="sxs-lookup"><span data-stu-id="f1360-200">**Years** – Select the day, week, and month that the user must complete the task by.</span></span> <span data-ttu-id="f1360-201">Til dæmis getur notandinn átt að vera búinn að ljúka verkinu fyrir föstudaginn í þriðju viku desembermánaðar.</span><span class="sxs-lookup"><span data-stu-id="f1360-201">For example, you might want the user to complete the task by Friday of the third week of December.</span></span>

    <span data-ttu-id="f1360-202">Ef notandinn klárar ekki verkið innan tímarammans, er verkið komið fram yfir á tíma.</span><span class="sxs-lookup"><span data-stu-id="f1360-202">If the user doesn't complete the task in the allotted time, the task is overdue.</span></span> <span data-ttu-id="f1360-203">Verk sem er komið fram yfir á tíma er hægt að stigmagna, á grundvelli valkostanna sem þú valdir í **stigmögnun** svæðið á síðunni.</span><span class="sxs-lookup"><span data-stu-id="f1360-203">A task that is overdue can be escalated, based on the options that you select in the **Escalation** area of the page.</span></span>

## <a name="specify-what-happens-when-the-task-is-overdue"></a><span data-ttu-id="f1360-204">Tilgreina hvað ætti að gerast þegar verk er komið fram yfir á tíma.</span><span class="sxs-lookup"><span data-stu-id="f1360-204">Specify what happens when the task is overdue</span></span>

<span data-ttu-id="f1360-205">Ef notandinn klárar ekki handvirka verkið innan tímarammans, er verkið komið fram yfir á tíma.</span><span class="sxs-lookup"><span data-stu-id="f1360-205">If a user doesn't complete the manual task in the allotted time, the task is overdue.</span></span> <span data-ttu-id="f1360-206">Verk sem er komið fram yfir á tíma má stigmagna, eða úthluta sjálfkrafa á annan notanda.</span><span class="sxs-lookup"><span data-stu-id="f1360-206">A task that is overdue can be escalated, or automatically assigned to another user.</span></span> <span data-ttu-id="f1360-207">Fylgið eftirfarandi skrefum til að stigmagna Verk ef það er komið fram yfir á tíma.</span><span class="sxs-lookup"><span data-stu-id="f1360-207">Follow these steps to escalate the task if it's overdue.</span></span>

1. <span data-ttu-id="f1360-208">Á vinstra svæðinu skaltu Smellt á **Stigmagna**.</span><span class="sxs-lookup"><span data-stu-id="f1360-208">In the left pane, click **Escalation**.</span></span>
2. <span data-ttu-id="f1360-209">Velja skal **Nota stigmögnunarslóð** gátreit til að stofna stigmögnunarslóð.</span><span class="sxs-lookup"><span data-stu-id="f1360-209">Select the **Use escalation path** check box to create an escalation path.</span></span> <span data-ttu-id="f1360-210">Kerfið mun sjálfkrafa úthluta verk til notendanna sem skráðir eru í stigmögnunarslóðinni.</span><span class="sxs-lookup"><span data-stu-id="f1360-210">The system automatically assigns the task to the users who are listed in the escalation path.</span></span> <span data-ttu-id="f1360-211">Til dæmis, eftirfarandi töflu sýnir stigmögnunarslóð.</span><span class="sxs-lookup"><span data-stu-id="f1360-211">For example, the following table represents an escalation path.</span></span>

    | <span data-ttu-id="f1360-212">Röð</span><span class="sxs-lookup"><span data-stu-id="f1360-212">Sequence</span></span> | <span data-ttu-id="f1360-213">stigmögnunarslóð</span><span class="sxs-lookup"><span data-stu-id="f1360-213">Escalation path</span></span>      |
    |----------|----------------------|
    | <span data-ttu-id="f1360-214">1</span><span class="sxs-lookup"><span data-stu-id="f1360-214">1</span></span>        | <span data-ttu-id="f1360-215">Úthluta til: Dísu</span><span class="sxs-lookup"><span data-stu-id="f1360-215">Assign to: Donna</span></span>     |
    | <span data-ttu-id="f1360-216">2</span><span class="sxs-lookup"><span data-stu-id="f1360-216">2</span></span>        | <span data-ttu-id="f1360-217">Úthluta til: Erlu</span><span class="sxs-lookup"><span data-stu-id="f1360-217">Assign to: Erin</span></span>      |
    | <span data-ttu-id="f1360-218">3</span><span class="sxs-lookup"><span data-stu-id="f1360-218">3</span></span>        | <span data-ttu-id="f1360-219">Endanleg aðgerð: Hafna</span><span class="sxs-lookup"><span data-stu-id="f1360-219">Final action: Reject</span></span> |

    <span data-ttu-id="f1360-220">Í þessu dæmi mun kerfið sjálfkrafa úthluta verki sem er komið fram yfir á tíma til Dísu.</span><span class="sxs-lookup"><span data-stu-id="f1360-220">In this example, the system assigns the overdue task to Donna.</span></span> <span data-ttu-id="f1360-221">Ef Dísu klárar ekki verkið innan tímarammans, úthlutar kerfið verkinu til Erlu.</span><span class="sxs-lookup"><span data-stu-id="f1360-221">If Donna doesn't complete the task in the allotted time, the system assigns the task to Erin.</span></span> <span data-ttu-id="f1360-222">Ef Erla ekki klárar ekki verkið innan tímarammans, hafnar kerfið skjalinu sem var sent inn til vinnslu.</span><span class="sxs-lookup"><span data-stu-id="f1360-222">If Erin doesn't complete the task in the allotted time, the system rejects the document that was submitted for processing.</span></span>

3. <span data-ttu-id="f1360-223">Til að bæta notanda við stigmögnunarslóð, smella **bæta við stigmögnun**.</span><span class="sxs-lookup"><span data-stu-id="f1360-223">To add a user to the escalation path, click **Add escalation**.</span></span> <span data-ttu-id="f1360-224">Á flipanum **úthlutunargerð** , veljið einn af valkostum í eftirfarandi töflu, og fylgið svo viðbótarskref fyrir valkostinn áður en farið er í skrefi 4.</span><span class="sxs-lookup"><span data-stu-id="f1360-224">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 4.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="f1360-225">Valkostur</span><span class="sxs-lookup"><span data-stu-id="f1360-225">Option</span></span></th>
    <th><span data-ttu-id="f1360-226">Notendur sem verkið er stigmagnað fyrir</span><span class="sxs-lookup"><span data-stu-id="f1360-226">Users that the task is escalated to</span></span></th>
    <th><span data-ttu-id="f1360-227">Viðbótarskref</span><span class="sxs-lookup"><span data-stu-id="f1360-227">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="f1360-228">Stigveldi</span><span class="sxs-lookup"><span data-stu-id="f1360-228">Hierarchy</span></span></td>
    <td><span data-ttu-id="f1360-229">Notendur í tilteknu stigveldi fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="f1360-229">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="f1360-230">Eftir að þú velur <strong>stigveldi</strong>, á <strong>stigveldishluti</strong> flipanum, á listanum <strong>gerð stigveldis</strong> skal velja gerð stigveldis til stigmagna verk fyrir.</span><span class="sxs-lookup"><span data-stu-id="f1360-230">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to escalate the task to.</span></span></li>
    <li><span data-ttu-id="f1360-231">Kerfið verður að sækja svið notendanafna úr stigveldinu.</span><span class="sxs-lookup"><span data-stu-id="f1360-231">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="f1360-232">Þessi nöfn standa fyrir notendur sem hægt er stigmagna verk fyrir.</span><span class="sxs-lookup"><span data-stu-id="f1360-232">These names represent users that the task can be escalated to.</span></span> <span data-ttu-id="f1360-233">Farðu að þessum skrefum til að tilgreina upphafspunkt og lokapunkt sviðs notendanafna sem kerfið sækir.</span><span class="sxs-lookup"><span data-stu-id="f1360-233">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="f1360-234">Þegar tilgreina á upphafspunkt skal velja aðila af listanum <strong>Byrja frá og með</strong>.</span><span class="sxs-lookup"><span data-stu-id="f1360-234">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="f1360-235">Hægt er að tilgreina endapunkt með því að smella á <strong>bæta við skilyrði</strong>.</span><span class="sxs-lookup"><span data-stu-id="f1360-235">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="f1360-236">Til að færa inn skilyrðu sem ákvarðar hvar í stigveldinu kerfið eigi að hætta að sækja nöfn.</span><span class="sxs-lookup"><span data-stu-id="f1360-236">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="f1360-237">Á <strong>stigveldisvalkostir</strong> flipanum skal tilgreina hvaða notendur á sviðinu verk skal vera stigmagnað fyrir.</span><span class="sxs-lookup"><span data-stu-id="f1360-237">On the <strong>Hierarchy options</strong> tab, specify which users in the range the task should be escalated to:</span></span> <ul>
    <li><span data-ttu-id="f1360-238"><strong>Úthluta til allra sóttra notenda</strong> - þá er verk stigmagnað fyrir allra notenda á sviðinu.</span><span class="sxs-lookup"><span data-stu-id="f1360-238"><strong>Assign to all users retrieved</strong> – The task is escalated to all users in the range.</span></span></li>
    <li><span data-ttu-id="f1360-239"><strong>Úthluta eingöngu til síðasta sótta notanda</strong> - þá er verk stigmagnað aðeins til síðasta notanda á sviðinu.</span><span class="sxs-lookup"><span data-stu-id="f1360-239"><strong>Assign only to last user retrieved</strong> – The task is escalated to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="f1360-240"><strong>Sleppa notendum með eftirfarandi skilyrði</strong> – verkið er ekki stigmagnað fyrir notendur innan sviðsins sem uppfylla ákveðið skilyrði.</span><span class="sxs-lookup"><span data-stu-id="f1360-240"><strong>Exclude users with the following condition</strong> – This task isn't escalated to users in the range who meet a specific condition.</span></span> <span data-ttu-id="f1360-241">Smellið á <strong>bæta við skilyrði</strong> til að skilgreina skilyrðin.</span><span class="sxs-lookup"><span data-stu-id="f1360-241">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="f1360-242">Verkflæðisnotandi</span><span class="sxs-lookup"><span data-stu-id="f1360-242">Workflow user</span></span></td>
    <td><span data-ttu-id="f1360-243">Notendur í núverandi verkflæði</span><span class="sxs-lookup"><span data-stu-id="f1360-243">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="f1360-244">Eftir að þú velur <strong>verkflæðisnotandi</strong>, á <strong>verkflæðisnotandi</strong> flipanum, á <strong>verkflæðisnotandi</strong> listanum, veldu notandann sem tekur þátt í verkflæði.</span><span class="sxs-lookup"><span data-stu-id="f1360-244">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="f1360-245">Notandi</span><span class="sxs-lookup"><span data-stu-id="f1360-245">User</span></span></td>
    <td><span data-ttu-id="f1360-246">Tilteknir notendur</span><span class="sxs-lookup"><span data-stu-id="f1360-246">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="f1360-247">Eftir að þú velur <strong>Notanda</strong>, skal smellið á <strong>Notanda</strong> flipa.</span><span class="sxs-lookup"><span data-stu-id="f1360-247">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="f1360-248">Listinn <strong>Tiltækir notendur</strong> inniheldur alla notendur.</span><span class="sxs-lookup"><span data-stu-id="f1360-248">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="f1360-249">Veldu Notendur til að stigmagna verk fyrir, og færðu síðan þessa notendur í <strong>Valdir notendur</strong> lista.</span><span class="sxs-lookup"><span data-stu-id="f1360-249">Select the users to escalate the task to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

4. <span data-ttu-id="f1360-250">Á **tímamörk** flipanum, á svæðinu **Tímalengd** , tilgreinið hve mikinn tíma notandi hefur til að klára verkið.</span><span class="sxs-lookup"><span data-stu-id="f1360-250">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to complete the task.</span></span> <span data-ttu-id="f1360-251">Veldu einn af eftirfarandi valkostum:</span><span class="sxs-lookup"><span data-stu-id="f1360-251">Select one of the following options:</span></span>

    - <span data-ttu-id="f1360-252">**Klukkustundir** – færið Inn fjölda klukkustunda sem notandi hefur til að klára verkið.</span><span class="sxs-lookup"><span data-stu-id="f1360-252">**Hours** – Enter the number of hours that the user has to complete the task.</span></span> <span data-ttu-id="f1360-253">Þá velja dagatalið sem fyrirtækið notar og færa inn upplýsingar um vinnuviku fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="f1360-253">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="f1360-254">**Dagar** – færið Inn fjölda daga sem notandi hefur til að klára verkið.</span><span class="sxs-lookup"><span data-stu-id="f1360-254">**Days** – Enter the number of days that the user has to complete the task.</span></span> <span data-ttu-id="f1360-255">Þá velja dagatalið sem fyrirtækið notar og færa inn upplýsingar um vinnuviku fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="f1360-255">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="f1360-256">**Vikur** – færið Inn fjölda vikna sem notandi hefur til að klára verkið.</span><span class="sxs-lookup"><span data-stu-id="f1360-256">**Weeks** – Enter the number of weeks that the user has to complete the task.</span></span>
    - <span data-ttu-id="f1360-257">**Mánuðir** — velja daginn og vikuna sem notandinn verður að vera búinn að klára verkið fyrir.</span><span class="sxs-lookup"><span data-stu-id="f1360-257">**Months** – Select the day and week that the user must complete the task by.</span></span> <span data-ttu-id="f1360-258">Til dæmis getur notandinn átt að vera búinn að ljúka verkinu fyrir föstudaginn í þriðju viku mánaðarins.</span><span class="sxs-lookup"><span data-stu-id="f1360-258">For example, you might want the user to complete the task by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="f1360-259">**Ár** — velja daginn, vikuna og mánuðinn sem notandinn verður að vera búinn að klára verkið fyrir.</span><span class="sxs-lookup"><span data-stu-id="f1360-259">**Years** – Select the day, week, and month that the user must complete the task by.</span></span> <span data-ttu-id="f1360-260">Til dæmis getur notandinn átt að vera búinn að ljúka verkinu fyrir föstudaginn í þriðju viku desembermánaðar.</span><span class="sxs-lookup"><span data-stu-id="f1360-260">For example, you might want the user to complete the task by Friday of the third week of December.</span></span>

5. <span data-ttu-id="f1360-261">Endurtakið skref 3 til 4 fyrir hvern notanda sem á að bæta við stigmögnunarslóð.</span><span class="sxs-lookup"><span data-stu-id="f1360-261">Repeat steps 3 through 4 for each user that should be added to the escalation path.</span></span> <span data-ttu-id="f1360-262">Hægt er að breyta röðun notenda.</span><span class="sxs-lookup"><span data-stu-id="f1360-262">You can change the order of the users.</span></span>
6. <span data-ttu-id="f1360-263">Ef notendunum í stigmögnunarslóðinni klára ekki verkefni innan tímarammans, grípur kerfið til aðgerða varðandi verkið.</span><span class="sxs-lookup"><span data-stu-id="f1360-263">If the users in the escalation path don't complete the task in the allotted time, the system takes action on the task.</span></span> <span data-ttu-id="f1360-264">Til að tilgreina aðgerðina sem kerfið grípur til, veldu línuna **Aðgerð** , og síðan á **Ljúka aðgerð** flipanum, veljið aðgerð.</span><span class="sxs-lookup"><span data-stu-id="f1360-264">To specify the action that the system takes, select the **Action** row, and then, on the **End action** tab, select an action.</span></span>

## <a name="specify-when-the-system-automatically-acts-on-the-task"></a><span data-ttu-id="f1360-265">Tilgreindu hvenær kerfið bregst sjálfkrafa við vegna verks.</span><span class="sxs-lookup"><span data-stu-id="f1360-265">Specify when the system automatically acts on the task</span></span>

<span data-ttu-id="f1360-266">Þú getur skilgreint krefið til að grípa til aðgerða vegna handvirka verksins þegar tilteknum skilyrðum er uppfyllt.</span><span class="sxs-lookup"><span data-stu-id="f1360-266">You can configure the system to take action on the manual task if specific conditions are met.</span></span> <span data-ttu-id="f1360-267">Til dæmis krefst verk að meðlimur kostnaðarskýrsludeildarinnar endurskoði innhreyfingarnar sem eru sendar með kostnaðarskýrslu.</span><span class="sxs-lookup"><span data-stu-id="f1360-267">For example, a task requires that a member of the Expense reports department review the receipts that are submitted together with an expense report.</span></span> <span data-ttu-id="f1360-268">Samkvæmt stefnu fyrirtækisins verður að framkvæma þetta verk ef heildarupphæð kostnaðarskýrslu er meiri en 100 USD.</span><span class="sxs-lookup"><span data-stu-id="f1360-268">According to company policy, this task must be performed if the total amount of the expense report is more than USD 100.</span></span> <span data-ttu-id="f1360-269">Í þessu dæmi, er hægt að skilgreina kerfið þannig að það merkir sjálfkrafa verkið sem **Lokið** þegar heildarupphæðin er lægri en 100.</span><span class="sxs-lookup"><span data-stu-id="f1360-269">In this scenario, you can configure the system to automatically mark the task as **Complete** when the total amount is less than 100.</span></span> <span data-ttu-id="f1360-270">Fylgið eftirfarandi skrefum til að tilgreina hvenær kerfið grípur til aðgerða vegna handvirks verks.</span><span class="sxs-lookup"><span data-stu-id="f1360-270">Follow these steps to specify when the system takes action on the manual task.</span></span>

1. <span data-ttu-id="f1360-271">Í vinstri glugganum, smelltu á **sjálfvirkar aðgerðir**.</span><span class="sxs-lookup"><span data-stu-id="f1360-271">In the left pane, click **Automatic actions**.</span></span>
2. <span data-ttu-id="f1360-272">Útvíkkið gátreitur **virkja sjálfvirkar aðgerðir** .</span><span class="sxs-lookup"><span data-stu-id="f1360-272">Select the **Enable automatic actions** check box.</span></span>
3. <span data-ttu-id="f1360-273">Smellt er á **Bæta við Skilyrði**.</span><span class="sxs-lookup"><span data-stu-id="f1360-273">Click **Add condition**.</span></span>
4. <span data-ttu-id="f1360-274">Færið inn skilyrði.</span><span class="sxs-lookup"><span data-stu-id="f1360-274">Enter a condition.</span></span>
5. <span data-ttu-id="f1360-275">Færið inn öll önnur skilyrði sem krafist er.</span><span class="sxs-lookup"><span data-stu-id="f1360-275">Enter any additional conditions that are required.</span></span>
6. <span data-ttu-id="f1360-276">Til að sannreyna að skilyrðin sem voru færð hafi verið sett upp rétt, skal fylgja eftirfarandi skrefum:</span><span class="sxs-lookup"><span data-stu-id="f1360-276">To verify that the conditions that you entered are configured correctly, follow these steps:</span></span>

    1. <span data-ttu-id="f1360-277">Smellið á **Prófun**.</span><span class="sxs-lookup"><span data-stu-id="f1360-277">Click **Test**.</span></span>
    2. <span data-ttu-id="f1360-278">Á síðunni **Kanna verkflæðisskilyrði** , í **Villuleita skilyrði** svæði, velja færslu.</span><span class="sxs-lookup"><span data-stu-id="f1360-278">On the **Test workflow condition** page, in the **Validate condition** area, select a record.</span></span>
    3. <span data-ttu-id="f1360-279">Smellið á **Prófun**.</span><span class="sxs-lookup"><span data-stu-id="f1360-279">Click **Test**.</span></span> <span data-ttu-id="f1360-280">Kerfið metur færsluna og ákveður hvort hún standist skilyrði sem þú tiltókst.</span><span class="sxs-lookup"><span data-stu-id="f1360-280">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4. <span data-ttu-id="f1360-281">Smelltu á **Í lagi** eða **hætta við** til að fara aftur síðuna **forstillingar**.</span><span class="sxs-lookup"><span data-stu-id="f1360-281">Click **OK** or **Cancel** to return to the **Properties** page.</span></span>

7. <span data-ttu-id="f1360-282">Í listanum **ljúka aðgerð sjálfvirkt** skal velja aðgerðina sem kerfið á að grípa til vegna verksins.</span><span class="sxs-lookup"><span data-stu-id="f1360-282">In the **Auto complete action** list, select the action that the system should take on the task.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="f1360-283">Tilgreinið hvenær tilkynningar eru sendar út</span><span class="sxs-lookup"><span data-stu-id="f1360-283">Specify when notifications are sent</span></span>

<span data-ttu-id="f1360-284">Hægt er að senda tilkynningar til fólks þegar handvirku verki hefur verið framselja, stigmagnað, lokið, eða hafnað, eða þegar beðið hefur verið um breytingu.</span><span class="sxs-lookup"><span data-stu-id="f1360-284">You can send notifications to people when a manual task has been delegated, escalated, completed, or rejected, or when a change has been requested.</span></span> <span data-ttu-id="f1360-285">Fylgið eftirfarandi skrefum til að tilgreina hvenær senda á út tilkynningar og til hvers tilkynningar eru sendar.</span><span class="sxs-lookup"><span data-stu-id="f1360-285">Follow these steps to specify when notifications are sent, and who the notifications are sent to.</span></span>

1. <span data-ttu-id="f1360-286">Á svæðinu vinstra megin, smella á **tilkynningar**.</span><span class="sxs-lookup"><span data-stu-id="f1360-286">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="f1360-287">Veldu gátreitinn sem er við hliðina á tilvikunum sem tilkynningar eiga að vera senda vegna.</span><span class="sxs-lookup"><span data-stu-id="f1360-287">Select the check box next to the events that notifications should be sent for:</span></span>

    - <span data-ttu-id="f1360-288">**Framselja** – verki hefur verið úthlutað til annars notanda.</span><span class="sxs-lookup"><span data-stu-id="f1360-288">**Delegate** – The task has been assigned to another user.</span></span>
    - <span data-ttu-id="f1360-289">**Stigmagna** – úthlutaður notandi hefur ekki lokið verkinu innan tímarammans.</span><span class="sxs-lookup"><span data-stu-id="f1360-289">**Escalate** – The assigned user hasn't completed the task in the allotted time.</span></span>
    - <span data-ttu-id="f1360-290">**Ljúka** – úthlutaður notandi hefur lokið verkinu.</span><span class="sxs-lookup"><span data-stu-id="f1360-290">**Complete** – The assigned user has completed the task.</span></span>
    - <span data-ttu-id="f1360-291">**Hafna** – úthlutaður notandi hefur hafnað skjalinu sem var sent.</span><span class="sxs-lookup"><span data-stu-id="f1360-291">**Reject** – The assigned user has rejected the document that was submitted.</span></span>
    - <span data-ttu-id="f1360-292">**Biðja um breytingu** – úthlutaður notandi hefur beðið um breytingu á skjalinu sem var sent.</span><span class="sxs-lookup"><span data-stu-id="f1360-292">**Request change** – The assigned user has requested a change to the document that was submitted.</span></span>

3. <span data-ttu-id="f1360-293">Veljið línu fyrir tilvik sem þú valdir í skrefi 2.</span><span class="sxs-lookup"><span data-stu-id="f1360-293">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="f1360-294">Á **tilkynningartexti** flipanum í textareitinn, færa inn texta tilkynningarinnar.</span><span class="sxs-lookup"><span data-stu-id="f1360-294">On the **Notification text** tab, in the text box, enter the text of the notification.</span></span>
5. <span data-ttu-id="f1360-295">Hægt er að sérsníða tilkynningu með því að færa inn staðgengla.</span><span class="sxs-lookup"><span data-stu-id="f1360-295">To personalize the notification, you can insert placeholders.</span></span> <span data-ttu-id="f1360-296">Staðgenglar eru settir í stað viðeigandi upplýsinga þegar tilkynning birtist notanda.</span><span class="sxs-lookup"><span data-stu-id="f1360-296">Placeholders are replaced with appropriate information when the notification is shown to users.</span></span> <span data-ttu-id="f1360-297">Fylgið eftirfarandi skrefum til að færa inn staðgengil:</span><span class="sxs-lookup"><span data-stu-id="f1360-297">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="f1360-298">Smellið á textahólfið þar sem staðgengillinn á að birtast.</span><span class="sxs-lookup"><span data-stu-id="f1360-298">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="f1360-299">Smella á **Setja inn staðgengil**</span><span class="sxs-lookup"><span data-stu-id="f1360-299">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="f1360-300">Í listanum sem birtist skal velja staðgengilinn til að setja inn.</span><span class="sxs-lookup"><span data-stu-id="f1360-300">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="f1360-301">Smellt er á **Setja inn**.</span><span class="sxs-lookup"><span data-stu-id="f1360-301">Click **Insert**.</span></span>

6. <span data-ttu-id="f1360-302">Til að bæta þýðingum við Tilkynningar skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="f1360-302">To add translations of the notification, follow these steps:</span></span>

    1. <span data-ttu-id="f1360-303">Smellt er á **Þýðingar**.</span><span class="sxs-lookup"><span data-stu-id="f1360-303">Click **Translations**.</span></span>
    2. <span data-ttu-id="f1360-304">Á síðunni sem birtist er smellt á **bæta við**.</span><span class="sxs-lookup"><span data-stu-id="f1360-304">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="f1360-305">Í listanum sem birtist skal velja tungumálið sem verið er að færa inn í textanum.</span><span class="sxs-lookup"><span data-stu-id="f1360-305">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="f1360-306">Í svæðið **þýddur texti** skal færa inn textann.</span><span class="sxs-lookup"><span data-stu-id="f1360-306">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="f1360-307">Til að sérsníða textann geturðu sett inn staðgengla eins og lýst er í skrefi 5.</span><span class="sxs-lookup"><span data-stu-id="f1360-307">To personalize the text, you can insert placeholders as described in step 5.</span></span>
    6. <span data-ttu-id="f1360-308">Smellið á **Loka**.</span><span class="sxs-lookup"><span data-stu-id="f1360-308">Click **Close**.</span></span>

7. <span data-ttu-id="f1360-309">Á **Viðtakanda** flipanum, tilgreinið hverjum tilkynningar eru sendar.</span><span class="sxs-lookup"><span data-stu-id="f1360-309">On the **Recipient** tab, specify who the notifications are sent to.</span></span> <span data-ttu-id="f1360-310">Veljið einn af valkostum í eftirfarandi töflu, og fylgið svo viðbótarskref fyrir valkostinn áður en farið er í skrefi 8.</span><span class="sxs-lookup"><span data-stu-id="f1360-310">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 8.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="f1360-311">Valkostur</span><span class="sxs-lookup"><span data-stu-id="f1360-311">Option</span></span></th>
    <th><span data-ttu-id="f1360-312">Viðtakendur tilkynninga.</span><span class="sxs-lookup"><span data-stu-id="f1360-312">Notification recipients</span></span></th>
    <th><span data-ttu-id="f1360-313">Viðbótarskref</span><span class="sxs-lookup"><span data-stu-id="f1360-313">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="f1360-314">Þátttakendur</span><span class="sxs-lookup"><span data-stu-id="f1360-314">Participant</span></span></td>
    <td><span data-ttu-id="f1360-315">Notendur sem tilheyra tilteknum hópi eða hlutverki</span><span class="sxs-lookup"><span data-stu-id="f1360-315">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="f1360-316">Eftor að þú velur <strong>viðtakanda</strong>, Á flipanum <strong>Hlutverkamiðað</strong> , á listanum <strong>Gerð þátttakanda</strong> skal velja gerð hóps eða hlutverks til að senda tilkynningu á.</span><span class="sxs-lookup"><span data-stu-id="f1360-316">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="f1360-317">Í listanum <strong>Þátttakanda</strong> skal velja hópi eða hlutverk til að senda tilkynningar til.</span><span class="sxs-lookup"><span data-stu-id="f1360-317">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="f1360-318">Verkflæðisnotandi</span><span class="sxs-lookup"><span data-stu-id="f1360-318">Workflow user</span></span></td>
    <td><span data-ttu-id="f1360-319">Notendur í núverandi verkflæði</span><span class="sxs-lookup"><span data-stu-id="f1360-319">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="f1360-320">Eftir að þú velur <strong>verkflæðisnotandi</strong>, á <strong>verkflæðisnotandi</strong> flipanum, á <strong>verkflæðisnotandi</strong> listanum, veldu notandann sem tekur þátt í verkflæði.</span><span class="sxs-lookup"><span data-stu-id="f1360-320">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="f1360-321">Notandi</span><span class="sxs-lookup"><span data-stu-id="f1360-321">User</span></span></td>
    <td><span data-ttu-id="f1360-322">Tilteknir notendur</span><span class="sxs-lookup"><span data-stu-id="f1360-322">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="f1360-323">Eftir að þú velur <strong>Notanda</strong>, skal smellið á <strong>Notanda</strong> flipa.</span><span class="sxs-lookup"><span data-stu-id="f1360-323">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="f1360-324">Listinn <strong>Tiltækir notendur</strong> inniheldur alla notendur.</span><span class="sxs-lookup"><span data-stu-id="f1360-324">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="f1360-325">Veldu Notendur til að senda tilkynningar til, og færðu síðan þessa notendur í <strong>Valdir notendur</strong> lista.</span><span class="sxs-lookup"><span data-stu-id="f1360-325">Select the users to send notifications to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. <span data-ttu-id="f1360-326">Endurtakið skref 3 til 7 hvert tilvik sem valin var í skrefi 2.</span><span class="sxs-lookup"><span data-stu-id="f1360-326">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="set-a-time-limit"></a><span data-ttu-id="f1360-327">Setja upp tímamörk</span><span class="sxs-lookup"><span data-stu-id="f1360-327">Set a time limit</span></span>

<span data-ttu-id="f1360-328">Fylgið eftirfarandi skrefum ef verður að ljúka handvirku verki innan tiltekins tíma.</span><span class="sxs-lookup"><span data-stu-id="f1360-328">Follow these steps if the manual task must be completed in a specific time.</span></span>

> [!NOTE]
> <span data-ttu-id="f1360-329">Valkostirnir sem valdir eru í þessu ferli munu hnekkja valkostunum sem valdir voru í svæðunum **Úthlutun** og **Stigmögnun** á síðunni.</span><span class="sxs-lookup"><span data-stu-id="f1360-329">The options that you select in this procedure override the options that you selected in the **Assignment** and **Escalation** areas of the page.</span></span>

1. <span data-ttu-id="f1360-330">Í vinstri glugganum, smelltu á **ítarlegar stillingar**.</span><span class="sxs-lookup"><span data-stu-id="f1360-330">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="f1360-331">Veldu gátreitinn **Stilla tímamörk verkflæðiseiningar**</span><span class="sxs-lookup"><span data-stu-id="f1360-331">Select the **Set a time limit for the workflow element** check box.</span></span>
3. <span data-ttu-id="f1360-332">Í reitnum **tímalengd** tilgreinið þegar Verk á að vera lokið.</span><span class="sxs-lookup"><span data-stu-id="f1360-332">In the **Duration** field, specify when the task must be completed.</span></span> <span data-ttu-id="f1360-333">Veldu einn af eftirfarandi valkostum:</span><span class="sxs-lookup"><span data-stu-id="f1360-333">Select one of the following options:</span></span>

    - <span data-ttu-id="f1360-334">**Klukkustundir** – færið Inn fjölda klukkustunda sem notandi hefur til að klára verkið.</span><span class="sxs-lookup"><span data-stu-id="f1360-334">**Hours** – Enter the number of hours that the task must be completed in.</span></span> <span data-ttu-id="f1360-335">Þá velja dagatalið sem fyrirtækið notar og færa inn upplýsingar um vinnuviku fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="f1360-335">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="f1360-336">**Dagar** – færið Inn fjölda daga sem notandi hefur til að klára verkið.</span><span class="sxs-lookup"><span data-stu-id="f1360-336">**Days** – Enter the number of days that the task must be completed in.</span></span> <span data-ttu-id="f1360-337">Þá velja dagatalið sem fyrirtækið notar og færa inn upplýsingar um vinnuviku fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="f1360-337">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="f1360-338">**Vikur** – færið Inn fjölda vikna sem notandi hefur til að klára verkið.</span><span class="sxs-lookup"><span data-stu-id="f1360-338">**Weeks** – Enter the number of weeks that the task must be completed in.</span></span>
    - <span data-ttu-id="f1360-339">**Mánuðir** — velja daginn og vikuna sem verður að vera búið að klára verkið fyrir.</span><span class="sxs-lookup"><span data-stu-id="f1360-339">**Months** – Select the day and week that the task must be completed by.</span></span> <span data-ttu-id="f1360-340">Til dæmis getur átt að vera búið að ljúka verkinu fyrir föstudaginn í þriðju viku mánaðarins.</span><span class="sxs-lookup"><span data-stu-id="f1360-340">For example, you might want the task to be completed by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="f1360-341">**Ár** — velja daginn, vikuna og mánuðinn sem verður að vera búið að klára verkið fyrir.</span><span class="sxs-lookup"><span data-stu-id="f1360-341">**Years** – Select the day, week, and month that the task must be completed by.</span></span> <span data-ttu-id="f1360-342">Til dæmis getur átt að vera búið að ljúka verkinu fyrir föstudaginn í þriðju viku desembermánaðar.</span><span class="sxs-lookup"><span data-stu-id="f1360-342">For example, you might want the task to be completed by Friday of the third week of December.</span></span>

4. <span data-ttu-id="f1360-343">Ef farið er yfir tímamörkin mun kerfið grípa til aðgerða vegna verksins.</span><span class="sxs-lookup"><span data-stu-id="f1360-343">If the time limit is exceeded, the system takes action on the task.</span></span> <span data-ttu-id="f1360-344">Veljið aðgerðina, sem kerfið á að framkvæma, í listanum **Aðgerðir**.</span><span class="sxs-lookup"><span data-stu-id="f1360-344">In the **Action** list, select the action that the system should take.</span></span>

## <a name="specify-which-actions-are-available-to-the-user"></a><span data-ttu-id="f1360-345">Tilgreina hvaða aðgerðir verða tiltækar notandanum.</span><span class="sxs-lookup"><span data-stu-id="f1360-345">Specify which actions are available to the user</span></span>

<span data-ttu-id="f1360-346">Þegar notandi fær handvirkt verk úthlutað verður hann að vinna að verkinu.</span><span class="sxs-lookup"><span data-stu-id="f1360-346">When the manual task is assigned to a user, the user must take action on the task.</span></span> <span data-ttu-id="f1360-347">Fylgið eftirfarandi skrefum til að tilgreina hvaða aðgerðir notandi getur gripið til vegna verksins.</span><span class="sxs-lookup"><span data-stu-id="f1360-347">Follow these steps to specify which actions the user can take on the task.</span></span>

> [!NOTE]
> <span data-ttu-id="f1360-348">Mismunandi aðgerðir eru í boði, fer eftir hönnun verksins.</span><span class="sxs-lookup"><span data-stu-id="f1360-348">The actions that are available vary, depending on the design of the task.</span></span>

1. <span data-ttu-id="f1360-349">Í vinstri glugganum, smelltu á **ítarlegar stillingar**.</span><span class="sxs-lookup"><span data-stu-id="f1360-349">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="f1360-350">Veljið gátreitinn **Lokið** ef notandinn á að geta merkt við verkið sem **lokið**.</span><span class="sxs-lookup"><span data-stu-id="f1360-350">Select the **Complete** check box if the user should be able to mark the task as **Complete**.</span></span>
3. <span data-ttu-id="f1360-351">Veljið gátreitinn **hafna** ef notandinn á að geta hafnað skjalinu sem var sent inn.</span><span class="sxs-lookup"><span data-stu-id="f1360-351">Select the **Reject** check box if the user should be able to reject the document that was submitted.</span></span>
4. <span data-ttu-id="f1360-352">Veljið gátreitinn **Biðja um breytingu** ef notandinn á að geta beðið um breytingar á skjalinu sem sent var inn.</span><span class="sxs-lookup"><span data-stu-id="f1360-352">Select the **Request change** check box if the user should be able to request changes to the document that was submitted.</span></span>
5. <span data-ttu-id="f1360-353">Veljið gátreitinn **framselja** ef notandinn á að geta framselt verkinu til annars notanda.</span><span class="sxs-lookup"><span data-stu-id="f1360-353">Select the **Delegate** check box if the user should be able to assign the task to another user.</span></span>
6. <span data-ttu-id="f1360-354">Veljið gátreitinn **endurúthluta** ef notandinn á að geta endurúthlutað verkinu til annars notanda í vinnuliðalistanum.</span><span class="sxs-lookup"><span data-stu-id="f1360-354">Select the **Reassign** check box if the user should be able to reassign the task to another user in the work item queue.</span></span>
7. <span data-ttu-id="f1360-355">Veljið gátreitinn **Losa** ef notandinn á að geta endurúthlutað verkinu til vinnuliðalista.</span><span class="sxs-lookup"><span data-stu-id="f1360-355">Select the **Release** check box if the user should be able to reassign the task to the work item queue.</span></span> <span data-ttu-id="f1360-356">Annar notandi getur þá ljúka verkefninu.</span><span class="sxs-lookup"><span data-stu-id="f1360-356">Another user can then complete the task.</span></span>
