---
title: Grunnstilla samþykktarskref í verkflæði
description: Þetta efnisatriði útskýrir hvernig skilgreina á eiginleika samþykktarskrefs.
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
ms.custom: 192161
ms.assetid: 8b478e3d-d6b4-403b-aae0-f639a71ca36c
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 69035be84d489d6ea2342c6974cfa9a31531f1c7
ms.sourcegitcommit: e55efd2f62bf60f678108c09ad4701a76b20cc68
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/17/2020
ms.locfileid: "3698072"
---
# <a name="configure-approval-steps-in-a-workflow"></a><span data-ttu-id="72ae3-103">Grunnstilla samþykktarskref í verkflæði</span><span class="sxs-lookup"><span data-stu-id="72ae3-103">Configure approval steps in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="72ae3-104">Þetta efnisatriði útskýrir hvernig skilgreina á eiginleika samþykktarskrefs.</span><span class="sxs-lookup"><span data-stu-id="72ae3-104">This topic explains how to configure the properties of an approval step.</span></span>

<span data-ttu-id="72ae3-105">Til að skilgreina samþykktarskref í verkflæðisritlinum, er hægrismellt á samþykktarskrefið og smellið síðan á **Eiginleika** til að opna í **Eiginleika** síðu.</span><span class="sxs-lookup"><span data-stu-id="72ae3-105">To configure an approval step in the workflow editor, right-click the approval step, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="72ae3-106">Notið síðan eftirfarandi ferli til að stilla eiginleika fyrir samþykktarskref.</span><span class="sxs-lookup"><span data-stu-id="72ae3-106">Then use the following procedures to configure the properties of the approval step.</span></span>

## <a name="name-the-step"></a><span data-ttu-id="72ae3-107">Gefa skrefinu heiti</span><span class="sxs-lookup"><span data-stu-id="72ae3-107">Name the step</span></span>
<span data-ttu-id="72ae3-108">Fylgið þessum skrefum til að færa inn heiti á samþykktarskrefinu.</span><span class="sxs-lookup"><span data-stu-id="72ae3-108">Follow these steps to enter a name for the approval step.</span></span>

1. <span data-ttu-id="72ae3-109">Í vinstri glugganum, smelltu á **grunnstillingar**.</span><span class="sxs-lookup"><span data-stu-id="72ae3-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="72ae3-110">Á svæðinu **Heiti** skal færa inn einkvæmt heiti fyrir samþykktarskref</span><span class="sxs-lookup"><span data-stu-id="72ae3-110">In the **Name** field, enter a unique name for the approval step.</span></span>

## <a name="enter-a-subject-line-and-instructions"></a><span data-ttu-id="72ae3-111">Slá inn efnislínu og fyrirmæli</span><span class="sxs-lookup"><span data-stu-id="72ae3-111">Enter a subject line and instructions</span></span>

<span data-ttu-id="72ae3-112">Veita verður þeim notendum, sem úthlutað er þessu samþykktarskref, efnislínu og fyrirmæli.</span><span class="sxs-lookup"><span data-stu-id="72ae3-112">You must provide a subject line and instructions to users who are assigned to the approval step.</span></span> <span data-ttu-id="72ae3-113">Til dæmis, ef verið er að skilgreina samþykktarskref fyrir innkaupabeiðnir, mun notanda er úthlutað á skrefið sjá efnislínuna og fyrirmælin á **Innkaupabeiðnir** síðunni.</span><span class="sxs-lookup"><span data-stu-id="72ae3-113">For example, if you're configuring an approval step for purchase requisitions, the user who is assigned to the step sees the subject line and instructions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="72ae3-114">Efnislínuna birtist á skilaboðaslánni á síðunni.</span><span class="sxs-lookup"><span data-stu-id="72ae3-114">The subject line appears in a message bar on the page.</span></span> <span data-ttu-id="72ae3-115">Notandinn getur síðan smellt á teiknið á skilaboðaslánni til að sjá leiðbeiningar.</span><span class="sxs-lookup"><span data-stu-id="72ae3-115">The user can then click the icon in the message bar to see the instructions.</span></span> <span data-ttu-id="72ae3-116">Fylgið eftirfarandi skrefum til að slá inn efnislínu og fyrirmæli.</span><span class="sxs-lookup"><span data-stu-id="72ae3-116">Follow these steps to enter a subject line and instructions.</span></span>

1. <span data-ttu-id="72ae3-117">Í vinstri glugganum, smelltu á **grunnstillingar**.</span><span class="sxs-lookup"><span data-stu-id="72ae3-117">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="72ae3-118">Í **efni vinnuliðs** svæðinu, færið inn efnislínuna.</span><span class="sxs-lookup"><span data-stu-id="72ae3-118">In the **Work item subject** field, enter the subject line.</span></span>
3. <span data-ttu-id="72ae3-119">Til að sérsníða efnislínuna, er hægt að færa inn staðgengla.</span><span class="sxs-lookup"><span data-stu-id="72ae3-119">To personalize the subject line, you can insert placeholders.</span></span> <span data-ttu-id="72ae3-120">Staðgenglar eru settir í stað viðeigandi gagna þegar efnislínan birtist notendum.</span><span class="sxs-lookup"><span data-stu-id="72ae3-120">Placeholders are replaced with appropriate data when the subject line is shown to users.</span></span> <span data-ttu-id="72ae3-121">Fylgið eftirfarandi skrefum til að færa inn staðgengil:</span><span class="sxs-lookup"><span data-stu-id="72ae3-121">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="72ae3-122">Smellið á textahólfið þar sem staðgengillinn á að birtast.</span><span class="sxs-lookup"><span data-stu-id="72ae3-122">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="72ae3-123">Smella á **Setja inn staðgengil**</span><span class="sxs-lookup"><span data-stu-id="72ae3-123">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="72ae3-124">Í listanum sem birtist skal velja staðgengilinn til að setja inn.</span><span class="sxs-lookup"><span data-stu-id="72ae3-124">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="72ae3-125">Smellt er á **Setja inn**.</span><span class="sxs-lookup"><span data-stu-id="72ae3-125">Click **Insert**.</span></span>

4. <span data-ttu-id="72ae3-126">Til að bæta þýðingum við efnislínuna skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="72ae3-126">To add translations of the subject line, follow these steps:</span></span>

    1. <span data-ttu-id="72ae3-127">Smellt er á **Þýðingar**.</span><span class="sxs-lookup"><span data-stu-id="72ae3-127">Click **Translations**.</span></span>
    2. <span data-ttu-id="72ae3-128">Á síðunni sem birtist er smellt á **bæta við**.</span><span class="sxs-lookup"><span data-stu-id="72ae3-128">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="72ae3-129">Í listanum sem birtist skal velja tungumálið sem verið er að færa inn í textanum.</span><span class="sxs-lookup"><span data-stu-id="72ae3-129">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="72ae3-130">Í svæðið **þýddur texti** skal færa inn textann.</span><span class="sxs-lookup"><span data-stu-id="72ae3-130">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="72ae3-131">Til að sérsníða textann geturðu sett inn staðgengla eins og lýst er í skrefi 3.</span><span class="sxs-lookup"><span data-stu-id="72ae3-131">To personalize the text, you can insert placeholders as described in step 3.</span></span>
    6. <span data-ttu-id="72ae3-132">Smellið á **Loka**.</span><span class="sxs-lookup"><span data-stu-id="72ae3-132">Click **Close**.</span></span>

5. <span data-ttu-id="72ae3-133">Í **leiðbeiningar vinnuliðs** svæðinu, færið inn leiðbeiningar.</span><span class="sxs-lookup"><span data-stu-id="72ae3-133">In the **Work item instructions** field, enter the instructions.</span></span>
6. <span data-ttu-id="72ae3-134">Hægt er að sérsníða leiðbeiningarnar með því að færa inn staðgengla.</span><span class="sxs-lookup"><span data-stu-id="72ae3-134">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="72ae3-135">Staðgenglar eru settir í stað viðeigandi gagna þegar leiðbeiningar birtist notendum.</span><span class="sxs-lookup"><span data-stu-id="72ae3-135">Placeholders are replaced with appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="72ae3-136">Fylgið eftirfarandi skrefum til að færa inn staðgengil:</span><span class="sxs-lookup"><span data-stu-id="72ae3-136">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="72ae3-137">Smellið á textahólfið þar sem staðgengillinn á að birtast.</span><span class="sxs-lookup"><span data-stu-id="72ae3-137">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="72ae3-138">Smella á **Setja inn staðgengil**</span><span class="sxs-lookup"><span data-stu-id="72ae3-138">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="72ae3-139">Í listanum sem birtist skal velja staðgengilinn til að setja inn.</span><span class="sxs-lookup"><span data-stu-id="72ae3-139">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="72ae3-140">Smellt er á **Setja inn**.</span><span class="sxs-lookup"><span data-stu-id="72ae3-140">Click **Insert**.</span></span>

7. <span data-ttu-id="72ae3-141">Til að bæta þýðingum við leiðbeiningar skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="72ae3-141">To add translations of the instructions, follow these steps:</span></span>

    1. <span data-ttu-id="72ae3-142">Smellt er á **Þýðingar**.</span><span class="sxs-lookup"><span data-stu-id="72ae3-142">Click **Translations**.</span></span>
    2. <span data-ttu-id="72ae3-143">Á síðunni sem birtist er smellt á **bæta við**.</span><span class="sxs-lookup"><span data-stu-id="72ae3-143">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="72ae3-144">Í listanum sem birtist skal velja tungumálið sem verið er að færa inn í textanum.</span><span class="sxs-lookup"><span data-stu-id="72ae3-144">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="72ae3-145">Í svæðið **þýddur texti** skal færa inn textann.</span><span class="sxs-lookup"><span data-stu-id="72ae3-145">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="72ae3-146">Til að sérsníða textann geturðu sett inn staðgengla eins og lýst er í skrefi 6.</span><span class="sxs-lookup"><span data-stu-id="72ae3-146">To personalize the text, you can insert placeholders as described in step 6.</span></span>
    6. <span data-ttu-id="72ae3-147">Smellið á **Loka**.</span><span class="sxs-lookup"><span data-stu-id="72ae3-147">Click **Close**.</span></span>

## <a name="assign-the-approval-step"></a><span data-ttu-id="72ae3-148">Úthluta þessu samþykktarskrefi</span><span class="sxs-lookup"><span data-stu-id="72ae3-148">Assign the approval step</span></span>

<span data-ttu-id="72ae3-149">Farið að þessum skrefum til að tilgreina á hvern skal úthluta samþykktarskref.</span><span class="sxs-lookup"><span data-stu-id="72ae3-149">Follow these steps to specify who the approval step should be assigned to.</span></span>

1. <span data-ttu-id="72ae3-150">Á vinstra svæðinu er smellt á **úthlutun**.</span><span class="sxs-lookup"><span data-stu-id="72ae3-150">In the left pane, click **Assignment**.</span></span>
2. <span data-ttu-id="72ae3-151">Á flipanum **úthlutunargerð** , veljið einn af valkostum í eftirfarandi töflu, og fylgið svo viðbótarskref fyrir valkostinn áður en farið er í skrefi 3.</span><span class="sxs-lookup"><span data-stu-id="72ae3-151">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 3.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="72ae3-152">Valkostur</span><span class="sxs-lookup"><span data-stu-id="72ae3-152">Option</span></span></th>
    <th><span data-ttu-id="72ae3-153">Notandi sem samþykktarskref er úthlutað á.</span><span class="sxs-lookup"><span data-stu-id="72ae3-153">Users that the approval step is assigned to</span></span></th>
    <th><span data-ttu-id="72ae3-154">Viðbótarskref</span><span class="sxs-lookup"><span data-stu-id="72ae3-154">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="72ae3-155">Þátttakendur</span><span class="sxs-lookup"><span data-stu-id="72ae3-155">Participant</span></span></td>
    <td><span data-ttu-id="72ae3-156">Notendur sem tilheyra tilteknum hópi eða hlutverki</span><span class="sxs-lookup"><span data-stu-id="72ae3-156">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="72ae3-157">Eftir að þú velur <strong>Þátttakanda</strong>á flipanum <strong>Hlutverkamiðað</strong> , á listanum <strong>Gerð þátttakanda</strong> skal velja gerð hóps eða hlutverks til að úthluta skrefinu á.</span><span class="sxs-lookup"><span data-stu-id="72ae3-157">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to assign the step to.</span></span></li>
    <li><span data-ttu-id="72ae3-158">Í listanum <strong>Þátttakanda</strong> skal velja hópi eða hlutverki til að úthluta skrefinu á.</span><span class="sxs-lookup"><span data-stu-id="72ae3-158">In the <strong>Participant</strong> list, select the group or role to assign the step to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="72ae3-159">Stigveldi</span><span class="sxs-lookup"><span data-stu-id="72ae3-159">Hierarchy</span></span></td>
    <td><span data-ttu-id="72ae3-160">Notendur í tilteknu stigveldi fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="72ae3-160">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="72ae3-161">Eftir að þú velur <strong>stigveldi</strong>, á <strong>stigveldishluti</strong> flipanum, á listanum <strong>gerð stigveldis</strong> skal velja gerð stigveldis til að úthluta skrefinu á.</span><span class="sxs-lookup"><span data-stu-id="72ae3-161">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to assign the step to.</span></span></li>
    <li><span data-ttu-id="72ae3-162">Kerfið verður að sækja svið notendanafna úr stigveldinu.</span><span class="sxs-lookup"><span data-stu-id="72ae3-162">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="72ae3-163">Þessi nöfn standa fyrir notendur sem hægt er að úthluta skrefinu á.</span><span class="sxs-lookup"><span data-stu-id="72ae3-163">These names represent users that the step can be assigned to.</span></span> <span data-ttu-id="72ae3-164">Farðu að þessum skrefum til að tilgreina upphafspunkt og lokapunkt sviðs notendanafna sem kerfið sækir.</span><span class="sxs-lookup"><span data-stu-id="72ae3-164">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="72ae3-165">Þegar tilgreina á upphafspunkt skal velja aðila af listanum <strong>Byrja frá og með</strong>.</span><span class="sxs-lookup"><span data-stu-id="72ae3-165">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="72ae3-166">Hægt er að tilgreina endapunkt með því að smella á <strong>bæta við skilyrði</strong>.</span><span class="sxs-lookup"><span data-stu-id="72ae3-166">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="72ae3-167">Til að færa inn skilyrðu sem ákvarðar hvar í stigveldinu kerfið eigi að hætta að sækja nöfn.</span><span class="sxs-lookup"><span data-stu-id="72ae3-167">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="72ae3-168">Á <strong>stigveldisvalkostir</strong> flipanum skal tilgreina hvaða notendur á sviðinu skrefinu skal úthlutað á:</span><span class="sxs-lookup"><span data-stu-id="72ae3-168">On the <strong>Hierarchy options</strong> tab, specify which users in the range the step should be assigned to:</span></span> <ul>
    <li><span data-ttu-id="72ae3-169"><strong>Úthluta til allra sóttra notenda</strong> - þá er samþykktarskrefið úthlutað til allra notenda á sviðinu.</span><span class="sxs-lookup"><span data-stu-id="72ae3-169"><strong>Assign to all users retrieved</strong> – The step is assigned to all users in the range.</span></span></li>
    <li><span data-ttu-id="72ae3-170"><strong>Úthluta eingöngu til síðasta sótta notanda</strong> - þá er skrefið aðeins úthlutað til síðasta notanda á sviðinu.</span><span class="sxs-lookup"><span data-stu-id="72ae3-170"><strong>Assign only to last user retrieved</strong> – The step is assigned to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="72ae3-171"><strong>Sleppa notendum með eftirfarandi skilyrði</strong> – skrefið er ekki úthlutað á notendur innan sviðsins sem uppfylla ákveðið skilyrði.</span><span class="sxs-lookup"><span data-stu-id="72ae3-171"><strong>Exclude users with the following condition</strong> – The step isn't assigned to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="72ae3-172">Smellið á <strong>bæta við skilyrði</strong> til að skilgreina skilyrðin.</span><span class="sxs-lookup"><span data-stu-id="72ae3-172">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="72ae3-173">Verkflæðisnotandi</span><span class="sxs-lookup"><span data-stu-id="72ae3-173">Workflow user</span></span></td>
    <td><span data-ttu-id="72ae3-174">Notendur í núverandi verkflæði</span><span class="sxs-lookup"><span data-stu-id="72ae3-174">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="72ae3-175">Eftir að þú velur <strong>verkflæðisnotandi</strong>, á <strong>verkflæðisnotandi</strong> flipanum, á <strong>verkflæðisnotandi</strong> listanum, veldu notandann sem tekur þátt í verkflæði.</span><span class="sxs-lookup"><span data-stu-id="72ae3-175">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="72ae3-176">Notandi</span><span class="sxs-lookup"><span data-stu-id="72ae3-176">User</span></span></td>
    <td><span data-ttu-id="72ae3-177">Tilteknir notendur</span><span class="sxs-lookup"><span data-stu-id="72ae3-177">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="72ae3-178">Eftir að þú velur <strong>Notanda</strong>, skal smellið á <strong>Notanda</strong> flipa.</span><span class="sxs-lookup"><span data-stu-id="72ae3-178">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="72ae3-179">Listinn <strong>Tiltækir notendur</strong> inniheldur alla kerfisnotendur.</span><span class="sxs-lookup"><span data-stu-id="72ae3-179">The <strong>Available users</strong> list includes all system users.</span></span> <span data-ttu-id="72ae3-180">Veldu Notendur til að úthluta skrefi á, og færsa íðan þessa notendur í <strong>Valdir notendur</strong> lista.</span><span class="sxs-lookup"><span data-stu-id="72ae3-180">Select the users to assign the step to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

3. <span data-ttu-id="72ae3-181">Á **tímamörk** flipanum, á svæðinu **Tímalengd** , tilgreinið hve mikinn tíma notandi hefur til að bregðast við eða svara skjölum sem ná samþykktarskrefi.</span><span class="sxs-lookup"><span data-stu-id="72ae3-181">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to take action on, or respond to, documents that reach the approval step.</span></span> <span data-ttu-id="72ae3-182">Veldu einn af eftirfarandi valkostum:</span><span class="sxs-lookup"><span data-stu-id="72ae3-182">Select one of the following options:</span></span>

    - <span data-ttu-id="72ae3-183">**Klukkustundir** – færið Inn fjölda klukkustunda sem notandi hefur til að bregðast við.</span><span class="sxs-lookup"><span data-stu-id="72ae3-183">**Hours** – Enter the number of hours that the user has to respond.</span></span> <span data-ttu-id="72ae3-184">Þá velja dagatalið sem fyrirtækið notar og færa inn upplýsingar um vinnuviku fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="72ae3-184">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="72ae3-185">**Dagar** – færið Inn fjölda daga sem notandi hefur til að bregðast við.</span><span class="sxs-lookup"><span data-stu-id="72ae3-185">**Days** – Enter the number of days that the user has to respond.</span></span> <span data-ttu-id="72ae3-186">Þá velja dagatalið sem fyrirtækið notar og færa inn upplýsingar um vinnuviku fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="72ae3-186">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="72ae3-187">**Vikur** – færið Inn fjölda vikna sem notandi hefur til að bregðast við.</span><span class="sxs-lookup"><span data-stu-id="72ae3-187">**Weeks** – Enter the number of weeks that the user has to respond.</span></span>
    - <span data-ttu-id="72ae3-188">**Mánuðir** — velja daginn og vikuna sem notandinn verður að vera búinn að bregðast við fyrir.</span><span class="sxs-lookup"><span data-stu-id="72ae3-188">**Months** – Select the day and week that the user must respond by.</span></span> <span data-ttu-id="72ae3-189">Til dæmis, notandi getur óskað þess að annar notandi bregðist við á föstudegi í þriðju viku mánaðarins.</span><span class="sxs-lookup"><span data-stu-id="72ae3-189">For example, you might want the user to respond by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="72ae3-190">**Ár** — velja daginn, vikuna og mánuðinn sem notandinn verður að vera búinn að bregðast við fyrir.</span><span class="sxs-lookup"><span data-stu-id="72ae3-190">**Years** – Select the day, week, and month that the user must respond by.</span></span> <span data-ttu-id="72ae3-191">Til dæmis, notandi getur óskað þess að annar notandi bregðist við á föstudegi í þriðju viku desembermánaðar.</span><span class="sxs-lookup"><span data-stu-id="72ae3-191">For example, you might want the user to respond by Friday of the third week of December.</span></span>

    <span data-ttu-id="72ae3-192">Ef notandinn bregst ekki við skjalinu á tilgreindum tíma, er skjalið komið fram yfir á tíma.</span><span class="sxs-lookup"><span data-stu-id="72ae3-192">If the user doesn't take action on the document in the allotted time, the document is overdue.</span></span> <span data-ttu-id="72ae3-193">Skjal sem er komið fram yfir á tíma er stigmagnað, á grundvelli valkostanna sem þú valdir í **stigmögnun** svæðið á síðunni.</span><span class="sxs-lookup"><span data-stu-id="72ae3-193">A document that is overdue is escalated, based on the options that you select in the **Escalation** area of the page.</span></span>

4. <span data-ttu-id="72ae3-194">Ef samþykktarskrefið var úthlutað til margra notenda eða flokk af notendum, á **regla um lok** flipanum, veljið einn af eftirfarandi valkostum:</span><span class="sxs-lookup"><span data-stu-id="72ae3-194">If you assigned the approval step to multiple users or a group of users, on the **Completion policy** tab, select one of the following options:</span></span>

    - <span data-ttu-id="72ae3-195">**Stakur samþykktaraðili** - aðgerðin fyrir skjalið ákveðin af fyrsta aðilanum sem bregst við.</span><span class="sxs-lookup"><span data-stu-id="72ae3-195">**Single approver** – The action that is applied to the document is determined by the first person who responds.</span></span> <span data-ttu-id="72ae3-196">Til dæmis hefur Samúel sent kostnaðarskýrslu upp á $15.000.</span><span class="sxs-lookup"><span data-stu-id="72ae3-196">For example, Sam has submitted an expense report for USD 15,000.</span></span> <span data-ttu-id="72ae3-197">Kostnaðarskýrslu er í augnablikinu úthlutað á Brynju, Guðrúnu og Gísla.</span><span class="sxs-lookup"><span data-stu-id="72ae3-197">The expense report is currently assigned to Sue, Jo, and Bill.</span></span> <span data-ttu-id="72ae3-198">Ef Brynja er sú fyrsta sem bregst við skjalinu þá er hennar aðgerð notuð fyrir skjalið.</span><span class="sxs-lookup"><span data-stu-id="72ae3-198">If Sue is the first person who responds to the document, the action that she takes is applied to the document.</span></span> <span data-ttu-id="72ae3-199">Ef Brynja hafnar skjalinu þá er því hafnað og sent tilbaka til Samúels.</span><span class="sxs-lookup"><span data-stu-id="72ae3-199">If Sue rejects the document, it's rejected and sent back to Sam.</span></span> <span data-ttu-id="72ae3-200">Þegar Brynja samþykkir skjalið er það sent til Önnu til samþykktar.</span><span class="sxs-lookup"><span data-stu-id="72ae3-200">If Sue approves the document, it's sent to Ann for approval.</span></span>

        ![Verkflæði sem er með samþykktarferli](./media/workflow_multipleusersinstep.gif)

    - <span data-ttu-id="72ae3-202">**Meirihluti samþykkjenda** - aðgerðin fyrir skjalið ákveðin þegar flestir af samþykktaraðilum bregðast við.</span><span class="sxs-lookup"><span data-stu-id="72ae3-202">**Majority of approvers** – The action that is applied to the document is determined when most of the approvers respond.</span></span> <span data-ttu-id="72ae3-203">Til dæmis hefur Samúel sent kostnaðarskýrslu upp á $15.000.</span><span class="sxs-lookup"><span data-stu-id="72ae3-203">For example, Sam has submitted an expense report for USD 15,000.</span></span> <span data-ttu-id="72ae3-204">Kostnaðarskýrslu er í augnablikinu úthlutað á Brynju, Guðrúnu og Gísla.</span><span class="sxs-lookup"><span data-stu-id="72ae3-204">The expense report is currently assigned to Sue, Jo, and Bill.</span></span> <span data-ttu-id="72ae3-205">Ef Brynja og Guðrún eru fyrstu tveir samþykktaraðilar sem svara, er aðgerðin sem þær grípa til beitt fyrir skjalið.</span><span class="sxs-lookup"><span data-stu-id="72ae3-205">If Sue and Jo are the first two approvers who respond, the action that they take is applied to the document.</span></span>

        - <span data-ttu-id="72ae3-206">Ef Brynja samþykkir skjalið og Guðrún hafnar því þá er því hafnað og sent tilbaka til Samúels.</span><span class="sxs-lookup"><span data-stu-id="72ae3-206">If Sue approves the document, but Jo rejects it, the document is rejected and sent back to Sam.</span></span>
        - <span data-ttu-id="72ae3-207">Ef Brynja og Guðrún samþykkja skjalið þá er skjalið sent til Önnu til samþykktar.</span><span class="sxs-lookup"><span data-stu-id="72ae3-207">If both Sue and Jo approve the document, it's sent to Ann for approval.</span></span>

    - <span data-ttu-id="72ae3-208">**Hlutfall samþykkjenda** - aðgerðin fyrir skjalið ákveðin þegar ákveðið hlutfall af samþykktaraðilum svara.</span><span class="sxs-lookup"><span data-stu-id="72ae3-208">**Percentage of approvers** – The action that is applied to the document is determined when a specific percentage of the approvers respond.</span></span> <span data-ttu-id="72ae3-209">Til dæmis hefur Samúel sent kostnaðarskýrslu upp á $15.000.</span><span class="sxs-lookup"><span data-stu-id="72ae3-209">For example, Sam has submitted an expense report for USD 15,000.</span></span> <span data-ttu-id="72ae3-210">Kostnaðarskýrslu er í augnablikinu úthlutað á Brynju, Guðrúnu og Gísla, og þú færðir inn **50** sem hlutfall.</span><span class="sxs-lookup"><span data-stu-id="72ae3-210">The expense report is currently assigned to Sue, Jo, and Bill, and you entered **50** as the percentage.</span></span> <span data-ttu-id="72ae3-211">Ef Brynja og Guðrún eru fyrstu tveir samþykktaraðilar sem svara, er aðgerðin sem þær grípa til beitt fyrir skjalið, af því að þær uppfylla kröfurnar um 50 prósent samþykktaraðila.</span><span class="sxs-lookup"><span data-stu-id="72ae3-211">If Sue and Jo are the first two approvers who respond, the action that they take is applied to the document, because they meet the requirement for 50 percent of approvers.</span></span>

        - <span data-ttu-id="72ae3-212">Ef Brynja samþykkir skjalið og Guðrún hafnar því þá er því hafnað og sent tilbaka til Samúels.</span><span class="sxs-lookup"><span data-stu-id="72ae3-212">If Sue approves the document, but Jo rejects it, the document is rejected and sent back to Sam.</span></span>
        - <span data-ttu-id="72ae3-213">Ef Brynja og Guðrún samþykkja skjalið þá er skjalið sent til Önnu til samþykktar.</span><span class="sxs-lookup"><span data-stu-id="72ae3-213">If both Sue and Jo approve the document, it's sent to Ann for approval.</span></span>

    - <span data-ttu-id="72ae3-214">**Allir samþykkjendur** – Allir samþykkjendur verða að samþykkja skjalið.</span><span class="sxs-lookup"><span data-stu-id="72ae3-214">**All approvers** – All the approvers must approve the document.</span></span> <span data-ttu-id="72ae3-215">Annars getur verkflæði ekki haldið áfram.</span><span class="sxs-lookup"><span data-stu-id="72ae3-215">Otherwise, the workflow can't continue.</span></span> <span data-ttu-id="72ae3-216">Til dæmis hefur Samúel sent kostnaðarskýrslu upp á $15.000.</span><span class="sxs-lookup"><span data-stu-id="72ae3-216">For example, Sam has submitted an expense report for USD 15,000.</span></span> <span data-ttu-id="72ae3-217">Kostnaðarskýrslu er í augnablikinu úthlutað á Brynju, Guðrúnu og Gísla.</span><span class="sxs-lookup"><span data-stu-id="72ae3-217">The expense report is currently assigned to Sue, Jo, and Bill.</span></span> <span data-ttu-id="72ae3-218">Ef Brynja og Guðrún samþykkja skjalið og Gísli hafnar því þá er því hafnað og sent tilbaka til Samúels.</span><span class="sxs-lookup"><span data-stu-id="72ae3-218">If Sue and Joe approve the document, but Bill rejects it, the document is rejected and sent back to Sam.</span></span> <span data-ttu-id="72ae3-219">Ef Brynja og Guðrún samþykkja skjalið þá er skjalið sent til Önnu til samþykktar.</span><span class="sxs-lookup"><span data-stu-id="72ae3-219">If Sue, Jo, and Bill all approve the document, it's sent to Ann for approval.</span></span>

## <a name="specify-when-the-approval-step-is-required"></a><span data-ttu-id="72ae3-220">Tilgreina hvenær samþykktarskrefið er nauðsynlegt</span><span class="sxs-lookup"><span data-stu-id="72ae3-220">Specify when the approval step is required</span></span>

<span data-ttu-id="72ae3-221">Hægt er að tilgreina hvenær samþykktarskrefið er nauðsynlegt.</span><span class="sxs-lookup"><span data-stu-id="72ae3-221">You can specify when the approval step is required.</span></span> <span data-ttu-id="72ae3-222">Samþykktarskrefið getur alltaf verið nauðsynlegt eða það getur verið nauðsynlegt aðeins ef tiltekin skilyrði eru uppfyllt.</span><span class="sxs-lookup"><span data-stu-id="72ae3-222">The approval step can always be required, or it can be required only if specific conditions are met.</span></span>

### <a name="the-approval-step-is-always-required"></a><span data-ttu-id="72ae3-223">Þetta samþykktarskref er alltaf nauðsynlegt</span><span class="sxs-lookup"><span data-stu-id="72ae3-223">The approval step is always required</span></span>

<span data-ttu-id="72ae3-224">Fylgið eftirfarandi skrefum ef samþykktarskrefið er alltaf nauðsynleg.</span><span class="sxs-lookup"><span data-stu-id="72ae3-224">Follow these steps if the approval step is always required.</span></span>

1. <span data-ttu-id="72ae3-225">Á vinstra svæðinu er smellt á **Skilyrði**.</span><span class="sxs-lookup"><span data-stu-id="72ae3-225">In the left pane, click **Condition**.</span></span>
2. <span data-ttu-id="72ae3-226">Veljið valkostinn **Alltaf að keyra þetta skref**.</span><span class="sxs-lookup"><span data-stu-id="72ae3-226">Select the **Always run this step** option.</span></span>

### <a name="the-approval-step-is-required-in-specific-conditions"></a><span data-ttu-id="72ae3-227">Þetta samþykktarskref er nauðsynlegt við sérstök skilyrði.</span><span class="sxs-lookup"><span data-stu-id="72ae3-227">The approval step is required in specific conditions</span></span>

<span data-ttu-id="72ae3-228">Það getur verið að samþykktarskrefið sem verið er að skilgreina sé aðeins nauðsynlegt við sérstök skilyrði.</span><span class="sxs-lookup"><span data-stu-id="72ae3-228">The approval step that you're configuring might be required only if specific conditions are met.</span></span> <span data-ttu-id="72ae3-229">T.d. ef verið er að skilgreina samþykktarskref fyrir verkflæði innkaupabeiðna, viltu kannski að þetta samþykktarskref komi aðeins upp ef upphæð innkaupabeiðni er meira en 10.000 USD.</span><span class="sxs-lookup"><span data-stu-id="72ae3-229">For example, if you're configuring an approval step for a purchase requisition workflow, you might want the approval step to occur only if the amount of the purchase requisition is more than USD 10,000.</span></span> <span data-ttu-id="72ae3-230">Fylgið eftirfarandi skrefum til að tilgreina hvenær krafist er samþykktarskrefið.</span><span class="sxs-lookup"><span data-stu-id="72ae3-230">Follow these steps to specify when the approval step is required.</span></span>

1. <span data-ttu-id="72ae3-231">Á vinstra svæðinu er smellt á **Skilyrði**.</span><span class="sxs-lookup"><span data-stu-id="72ae3-231">In the left pane, click **Condition**.</span></span>
2. <span data-ttu-id="72ae3-232">Veljið valkostinn **Keyra á þessu þrepi aðeins þegar eftirfarandi skilyrði eru í gildi**.</span><span class="sxs-lookup"><span data-stu-id="72ae3-232">Select the **Run this step only when the following condition is met** option.</span></span>
3. <span data-ttu-id="72ae3-233">Færið inn skilyrði.</span><span class="sxs-lookup"><span data-stu-id="72ae3-233">Enter a condition.</span></span>
4. <span data-ttu-id="72ae3-234">Færið inn öll önnur skilyrði sem krafist er.</span><span class="sxs-lookup"><span data-stu-id="72ae3-234">Enter any additional conditions that are required.</span></span>
5. <span data-ttu-id="72ae3-235">Til að sannreyna að skilyrðin sem voru færð hafi verið sett upp rétt, skal fylgja eftirfarandi skrefum:</span><span class="sxs-lookup"><span data-stu-id="72ae3-235">To verify that the conditions that you entered are configured correctly, follow these steps:</span></span>

    1. <span data-ttu-id="72ae3-236">Smellið á **Prófun**.</span><span class="sxs-lookup"><span data-stu-id="72ae3-236">Click **Test**.</span></span>
    2. <span data-ttu-id="72ae3-237">Á síðunni **Kanna verkflæðisskilyrði** , í **Villuleita skilyrði** svæði, velja færslu.</span><span class="sxs-lookup"><span data-stu-id="72ae3-237">On the **Test workflow condition** page, in the **Validate condition** area, select a record.</span></span>
    3. <span data-ttu-id="72ae3-238">Smellið á **Prófun**.</span><span class="sxs-lookup"><span data-stu-id="72ae3-238">Click **Test**.</span></span> <span data-ttu-id="72ae3-239">Kerfið metur færsluna og ákveður hvort hún standist skilyrði sem þú tiltókst.</span><span class="sxs-lookup"><span data-stu-id="72ae3-239">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4. <span data-ttu-id="72ae3-240">Smelltu á **Í lagi** eða **hætta við** til að fara aftur síðuna **forstillingar**.</span><span class="sxs-lookup"><span data-stu-id="72ae3-240">Click **OK** or **Cancel** to return to the **Properties** page.</span></span>

## <a name="specify-what-happens-when-the-document-is-overdue"></a><span data-ttu-id="72ae3-241">Tilgreina hvað gerist þegar skjal er í vanskilum</span><span class="sxs-lookup"><span data-stu-id="72ae3-241">Specify what happens when the document is overdue</span></span>

<span data-ttu-id="72ae3-242">Ef notandinn bregst ekki við skjalinu á tilgreindum tíma, er skjalið komið fram yfir á tíma.</span><span class="sxs-lookup"><span data-stu-id="72ae3-242">If a user doesn't take action on a document in the allotted time, the document is overdue.</span></span> <span data-ttu-id="72ae3-243">Skjal sem er komið fram yfir á tíma getur verið stigmagnað eða sjálfkrafa úthlutað til annars notanda til samþykkis.</span><span class="sxs-lookup"><span data-stu-id="72ae3-243">A document that is overdue can be escalated, or automatically assigned to another user for approval.</span></span> <span data-ttu-id="72ae3-244">Fylgið eftirfarandi skrefum til að stigmagna skjalið ef það er komið fram yfir á tíma.</span><span class="sxs-lookup"><span data-stu-id="72ae3-244">Follow these steps to escalate the document if it's overdue.</span></span>

1. <span data-ttu-id="72ae3-245">Á vinstra svæðinu skaltu Smellt á **Stigmagna**.</span><span class="sxs-lookup"><span data-stu-id="72ae3-245">In the left pane, click **Escalation**.</span></span>
2. <span data-ttu-id="72ae3-246">Velja skal **Nota stigmögnunarslóð** gátreit til að stofna stigmögnunarslóð.</span><span class="sxs-lookup"><span data-stu-id="72ae3-246">Select the **Use escalation path** check box to create an escalation path.</span></span> <span data-ttu-id="72ae3-247">Kerfið mun sjálfkrafa úthluta skjalinu til notendanna sem skráðir eru í stigmögnunarslóðinni.</span><span class="sxs-lookup"><span data-stu-id="72ae3-247">The system automatically assigns the document to the users who are listed in the escalation path.</span></span> <span data-ttu-id="72ae3-248">Til dæmis, eftirfarandi töflu sýnir stigmögnunarslóð.</span><span class="sxs-lookup"><span data-stu-id="72ae3-248">For example, the following table represents an escalation path.</span></span>

    | <span data-ttu-id="72ae3-249">Röð</span><span class="sxs-lookup"><span data-stu-id="72ae3-249">Sequence</span></span> | <span data-ttu-id="72ae3-250">stigmögnunarslóð</span><span class="sxs-lookup"><span data-stu-id="72ae3-250">Escalation path</span></span>      |
    |----------|----------------------|
    | <span data-ttu-id="72ae3-251">1</span><span class="sxs-lookup"><span data-stu-id="72ae3-251">1</span></span>        | <span data-ttu-id="72ae3-252">Úthluta til: Dísu</span><span class="sxs-lookup"><span data-stu-id="72ae3-252">Assign to: Donna</span></span>     |
    | <span data-ttu-id="72ae3-253">2</span><span class="sxs-lookup"><span data-stu-id="72ae3-253">2</span></span>        | <span data-ttu-id="72ae3-254">Úthluta til: Erlu</span><span class="sxs-lookup"><span data-stu-id="72ae3-254">Assign to: Erin</span></span>      |
    | <span data-ttu-id="72ae3-255">3</span><span class="sxs-lookup"><span data-stu-id="72ae3-255">3</span></span>        | <span data-ttu-id="72ae3-256">Endanleg aðgerð: Hafna</span><span class="sxs-lookup"><span data-stu-id="72ae3-256">Final action: Reject</span></span> |

    <span data-ttu-id="72ae3-257">Í þessu dæmi mun kerfið sjálfkrafa úthluta skjalinu sem er komið fram yfir á tíma til Dísu.</span><span class="sxs-lookup"><span data-stu-id="72ae3-257">In this example, the system assigns the overdue document to Donna.</span></span> <span data-ttu-id="72ae3-258">Ef Dísu ekki svarar innan tímarammans, úthlutar kerfið skjalinu til Erlu.</span><span class="sxs-lookup"><span data-stu-id="72ae3-258">If Donna doesn't respond in the allotted time, the system assigns the document to Erin.</span></span> <span data-ttu-id="72ae3-259">Ef Erla ekki svarar innan tímarammans, hafnar kerfið skjalinu.</span><span class="sxs-lookup"><span data-stu-id="72ae3-259">If Erin doesn't respond in the allotted time, the system rejects the document.</span></span>

3. <span data-ttu-id="72ae3-260">Til að bæta notanda við stigmögnunarslóð, smella **bæta við stigmögnun**.</span><span class="sxs-lookup"><span data-stu-id="72ae3-260">To add a user to the escalation path, click **Add escalation**.</span></span> <span data-ttu-id="72ae3-261">Á flipanum **úthlutunargerð** , veljið einn af valkostum í eftirfarandi töflu, og fylgið svo viðbótarskref fyrir valkostinn áður en farið er í skrefi 4.</span><span class="sxs-lookup"><span data-stu-id="72ae3-261">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 4.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="72ae3-262">Valkostur</span><span class="sxs-lookup"><span data-stu-id="72ae3-262">Option</span></span></th>
    <th><span data-ttu-id="72ae3-263">Notendur sem skjalið er stigmagnað fyrir</span><span class="sxs-lookup"><span data-stu-id="72ae3-263">Users that the document is escalated to</span></span></th>
    <th><span data-ttu-id="72ae3-264">Viðbótarskref</span><span class="sxs-lookup"><span data-stu-id="72ae3-264">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="72ae3-265">Stigveldi</span><span class="sxs-lookup"><span data-stu-id="72ae3-265">Hierarchy</span></span></td>
    <td><span data-ttu-id="72ae3-266">Notendur í tilteknu stigveldi fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="72ae3-266">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="72ae3-267">Eftir að þú velur <strong>stigveldi</strong>, á <strong>stigveldishluti</strong> flipanum, á listanum <strong>gerð stigveldis</strong> skal velja gerð stigveldis til stigmagna skjalinu fyrir.</span><span class="sxs-lookup"><span data-stu-id="72ae3-267">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to escalate the document to.</span></span></li>
    <li><span data-ttu-id="72ae3-268">Kerfið verður að sækja svið notendanafna úr stigveldinu.</span><span class="sxs-lookup"><span data-stu-id="72ae3-268">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="72ae3-269">Þessi nöfn standa fyrir notendur sem hægt er stigmagna skjalið fyrir.</span><span class="sxs-lookup"><span data-stu-id="72ae3-269">These names represent users that the document can be escalated to.</span></span> <span data-ttu-id="72ae3-270">Farðu að þessum skrefum til að tilgreina upphafspunkt og lokapunkt sviðs notendanafna sem kerfið sækir.</span><span class="sxs-lookup"><span data-stu-id="72ae3-270">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="72ae3-271">Þegar tilgreina á upphafspunkt skal velja aðila af listanum <strong>Byrja frá og með</strong>.</span><span class="sxs-lookup"><span data-stu-id="72ae3-271">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="72ae3-272">Hægt er að tilgreina endapunkt með því að smella á <strong>bæta við skilyrði</strong>.</span><span class="sxs-lookup"><span data-stu-id="72ae3-272">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="72ae3-273">Til að færa inn skilyrðu sem ákvarðar hvar í stigveldinu kerfið eigi að hætta að sækja nöfn.</span><span class="sxs-lookup"><span data-stu-id="72ae3-273">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="72ae3-274">Á <strong>stigveldisvalkostir</strong> flipanum skal tilgreina hvaða notendur á sviðinu skjalið skal vera stigmagnað fyrir.</span><span class="sxs-lookup"><span data-stu-id="72ae3-274">On the <strong>Hierarchy options</strong> tab, specify which users in the range the document should be escalated to:</span></span> <ul>
    <li><span data-ttu-id="72ae3-275"><strong>Úthluta til allra sóttra notenda</strong> - þá er skjalið stigmagnað fyrir allra notenda á sviðinu.</span><span class="sxs-lookup"><span data-stu-id="72ae3-275"><strong>Assign to all users retrieved</strong> – The document is escalated to all users in the range.</span></span></li>
    <li><span data-ttu-id="72ae3-276"><strong>Úthluta eingöngu til síðasta sótta notanda</strong> - þá er skjalið stigmagnað aðeins til síðasta notanda á sviðinu.</span><span class="sxs-lookup"><span data-stu-id="72ae3-276"><strong>Assign only to last user retrieved</strong> – The document is escalated to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="72ae3-277"><strong>Sleppa notendum með eftirfarandi skilyrði</strong> – skjalið er ekki stigmagnað fyrir neina notendur innan sviðsins sem uppfylla ákveðið skilyrði.</span><span class="sxs-lookup"><span data-stu-id="72ae3-277"><strong>Exclude users with the following condition</strong> – The document isn't escalated to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="72ae3-278">Smellið á <strong>bæta við skilyrði</strong> til að skilgreina skilyrðin.</span><span class="sxs-lookup"><span data-stu-id="72ae3-278">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="72ae3-279">Verkflæðisnotandi</span><span class="sxs-lookup"><span data-stu-id="72ae3-279">Workflow user</span></span></td>
    <td><span data-ttu-id="72ae3-280">Notendur í núverandi verkflæði</span><span class="sxs-lookup"><span data-stu-id="72ae3-280">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="72ae3-281">Eftir að þú velur <strong>verkflæðisnotandi</strong>, á <strong>verkflæðisnotandi</strong> flipanum, á <strong>verkflæðisnotandi</strong> listanum, veldu notandann sem tekur þátt í verkflæði.</span><span class="sxs-lookup"><span data-stu-id="72ae3-281">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="72ae3-282">Notandi</span><span class="sxs-lookup"><span data-stu-id="72ae3-282">User</span></span></td>
    <td><span data-ttu-id="72ae3-283">Tilteknir notendur</span><span class="sxs-lookup"><span data-stu-id="72ae3-283">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="72ae3-284">Eftir að þú velur <strong>Notanda</strong>, skal smellið á <strong>Notanda</strong> flipa.</span><span class="sxs-lookup"><span data-stu-id="72ae3-284">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="72ae3-285">Listinn <strong>Tiltækir notendur</strong> inniheldur alla notendur.</span><span class="sxs-lookup"><span data-stu-id="72ae3-285">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="72ae3-286">Veldu Notendur til að stigmagna skjali fyrir, og færðu síðan þessa notendur í <strong>Valdir notendur</strong> lista.</span><span class="sxs-lookup"><span data-stu-id="72ae3-286">Select the users to escalate the document to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

4. <span data-ttu-id="72ae3-287">Á **tímamörk** flipanum, á svæðinu **Tímalengd** , tilgreinið hve mikinn tíma notandi hefur til að bregðast við eða svara skjölum.</span><span class="sxs-lookup"><span data-stu-id="72ae3-287">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to take action on, or respond to, documents.</span></span> <span data-ttu-id="72ae3-288">Veldu einn af eftirfarandi valkostum:</span><span class="sxs-lookup"><span data-stu-id="72ae3-288">Select one of the following options:</span></span>

    - <span data-ttu-id="72ae3-289">**Klukkustundir** – færið Inn fjölda klukkustunda sem notandi hefur til að bregðast við.</span><span class="sxs-lookup"><span data-stu-id="72ae3-289">**Hours** – Enter the number of hours that the user has to respond.</span></span> <span data-ttu-id="72ae3-290">Þá velja dagatalið sem fyrirtækið notar og færa inn upplýsingar um vinnuviku fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="72ae3-290">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="72ae3-291">**Dagar** – færið Inn fjölda daga sem notandi hefur til að bregðast við.</span><span class="sxs-lookup"><span data-stu-id="72ae3-291">**Days** – Enter the number of days that the user has to respond.</span></span> <span data-ttu-id="72ae3-292">Þá velja dagatalið sem fyrirtækið notar og færa inn upplýsingar um vinnuviku fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="72ae3-292">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="72ae3-293">**Vikur** – færið Inn fjölda vikna sem notandi hefur til að bregðast við.</span><span class="sxs-lookup"><span data-stu-id="72ae3-293">**Weeks** – Enter the number of weeks that the user has to respond.</span></span>
    - <span data-ttu-id="72ae3-294">**Mánuðir** — velja daginn og vikuna sem notandinn verður að vera búinn að bregðast við fyrir.</span><span class="sxs-lookup"><span data-stu-id="72ae3-294">**Months** – Select the day and week that the user must respond by.</span></span> <span data-ttu-id="72ae3-295">Til dæmis, notandi getur óskað þess að annar notandi bregðist við á föstudegi í þriðju viku mánaðarins.</span><span class="sxs-lookup"><span data-stu-id="72ae3-295">For example, you might want the user to respond by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="72ae3-296">**Ár** — velja daginn, vikuna og mánuðinn sem notandinn verður að vera búinn að bregðast við fyrir.</span><span class="sxs-lookup"><span data-stu-id="72ae3-296">**Years** – Select the day, week, and month that the user must respond by.</span></span> <span data-ttu-id="72ae3-297">Til dæmis, notandi getur óskað þess að annar notandi bregðist við á föstudegi í þriðju viku desembermánaðar.</span><span class="sxs-lookup"><span data-stu-id="72ae3-297">For example, you might want the user to respond by Friday of the third week of December.</span></span>

5. <span data-ttu-id="72ae3-298">Endurtakið skref 3 til 4 fyrir hvern notanda sem á að bæta við stigmögnunarslóð.</span><span class="sxs-lookup"><span data-stu-id="72ae3-298">Repeat steps 3 through 4 for each user that should be added to the escalation path.</span></span> <span data-ttu-id="72ae3-299">Hægt er að breyta röðun notenda.</span><span class="sxs-lookup"><span data-stu-id="72ae3-299">You can change the order of the users.</span></span>
6. <span data-ttu-id="72ae3-300">Ef notendunum í stigmögnunarslóðinni svara ekki innan tímarammans, grípur kerfið sjálfkrafa til aðgerða varðandi skjalið.</span><span class="sxs-lookup"><span data-stu-id="72ae3-300">If the users in the escalation path don't respond in the allotted time, the system automatically take action on the document.</span></span> <span data-ttu-id="72ae3-301">Til að tilgreina aðgerðina sem kerfið grípur til, veldu línuna **Aðgerð** , og síðan á **Ljúka aðgerð** flipanum, veljið aðgerð.</span><span class="sxs-lookup"><span data-stu-id="72ae3-301">To specify the action that the system takes, select the **Action** row, and then, on the **End action** tab, select an action.</span></span>
