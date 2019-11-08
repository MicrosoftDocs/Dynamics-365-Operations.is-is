---
title: Stofna viðhaldsbeiðnir
description: Þetta efni útskýrir hvernig á að stofna viðhaldsbeiðni í eignastjórnun.
author: josaw1
manager: AnnBe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7fc9ec2f6a9a8a11d824e4b5c13d5aa173541454
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571922"
---
# <a name="create-maintenance-requests"></a><span data-ttu-id="faed4-103">Stofna viðhaldsbeiðnir</span><span class="sxs-lookup"><span data-stu-id="faed4-103">Create maintenance requests</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="faed4-104">Hægt er að nota viðhaldsbeiðnir ef viðhaldsstarfsmenn eða framleiðsluaðilar uppgötva að búnaður þarfnast viðgerðar, en ekki er hægt að gera viðgerðirnar strax.</span><span class="sxs-lookup"><span data-stu-id="faed4-104">Maintenance requests can be used if maintenance workers or production workers discover that equipment requires repair, but the repair job can't be done right away.</span></span>

<span data-ttu-id="faed4-105">**Dæmi:** Á meðan viðhaldsstarfsmaður er að gera við, uppgötvar hún að þjónusta verður aðra eign á sama stað.</span><span class="sxs-lookup"><span data-stu-id="faed4-105">**Example:** While a maintenance worker is making a repair, she discovers that another asset at the same location must be serviced.</span></span> <span data-ttu-id="faed4-106">Viðhaldsstarfsmaðurinn hefur þó ekki tíma eða nauðsynlega varahluti til að framkvæma viðgerðarstarfið.</span><span class="sxs-lookup"><span data-stu-id="faed4-106">However, the maintenance worker doesn't have the time or the required spare parts to do the repair job.</span></span> <span data-ttu-id="faed4-107">Þess vegna býr hún til viðhaldsbeiðni um eignina og slærð inn stutta lýsingu á vandamálinu.</span><span class="sxs-lookup"><span data-stu-id="faed4-107">Therefore, she creates a maintenance request on the asset and enters a short description of the issue.</span></span>

<span data-ttu-id="faed4-108">Hlutinn **Virkar viðhaldsbeiðnir** á rúðunni **Tengdar upplýsingar** hægra megin við síðuna **Allar eignir** eða **Virkar eignir** (**Eignastýring** \> **Sameiginlegt** \> **Eignir** \> **Allar eignir** eða **Virkar eignir**) sýnir virkar viðhaldsbeiðnir sem eru tengdar við valda eign.</span><span class="sxs-lookup"><span data-stu-id="faed4-108">The **Active maintenance requests** section of the **Related information** pane on the right side of the **All assets** or **Active assets** page (**Asset management** \> **Common** \> **Assets** \> **All assets** or **Active assets**) shows the active maintenance requests that are attached to the selected asset.</span></span>

1. <span data-ttu-id="faed4-109">Veldu **Eignastýring** \> **Sameiginlegt** \> **Viðhaldsbeiðnir** \> **Allar viðhaldsbeiðnir** eða **Virkar viðhaldsbeiðnir**.</span><span class="sxs-lookup"><span data-stu-id="faed4-109">Select **Asset management** \> **Common** \> **Maintenance requests** \> **All maintenance requests** or **Active maintenance requests**.</span></span>
2. <span data-ttu-id="faed4-110">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="faed4-110">Select **New**.</span></span>
3. <span data-ttu-id="faed4-111">Í svarglugganum **Stofna beiðni** í reitnum **Gerð viðhaldsbeiðni** velurðu gerð viðhaldsbeiðni.</span><span class="sxs-lookup"><span data-stu-id="faed4-111">In the **Create request** dialog box, in the **Maintenance request type** field, select the type of maintenance request.</span></span> <span data-ttu-id="faed4-112">Mælt er með sjálfgefinni gerð.</span><span class="sxs-lookup"><span data-stu-id="faed4-112">A default type is suggested.</span></span>
4. <span data-ttu-id="faed4-113">Í reitnum **Lýsing** slærðu inn heiti eða titil sem lýsir viðhaldsbeiðninni stuttlega.</span><span class="sxs-lookup"><span data-stu-id="faed4-113">In the **Description** field, enter a name or title that briefly describes the maintenance request.</span></span>
5. <span data-ttu-id="faed4-114">Í reitunum **Virk staðsetning** og **Eignir** velurðu virka staðsetningu eða eign eða sambland af virkri staðsetningu og eign, eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="faed4-114">In the **Functional location** and **Asset** fields, select a functional location or an asset, or a combination of a functional location and an asset, as you require.</span></span> <span data-ttu-id="faed4-115">Þú getur stofnað viðhaldsbeiðni án þess að velja eign og hægt er að bæta eigninni við viðhaldsbeiðnina seinna.</span><span class="sxs-lookup"><span data-stu-id="faed4-115">You can create a maintenance request without selecting an asset, and the asset can be added to the maintenance request later.</span></span> <span data-ttu-id="faed4-116">Ef viðhaldsstarfsmaðurinn sem er skráður inn í tengist auðlind sem er tengd eign er reiturinn **Eignir** er sjálfkrafa stilltur.</span><span class="sxs-lookup"><span data-stu-id="faed4-116">If the maintenance worker who is signed in is related to a resource that is related to an asset, the **Asset** field is automatically set.</span></span>

    <span data-ttu-id="faed4-117">Ef viðhaldsbeiðni er þegar fest við valda eign birtist skilaboðastika efst í valmyndinni **Stofna beiðni** til að láta þig vita um auðkenni núverandi viðhaldsbeiðni.</span><span class="sxs-lookup"><span data-stu-id="faed4-117">If a maintenance request is already attached to the selected asset, a message bar appears at the top of the **Create request** dialog box to notify you about the ID of the existing maintenance request.</span></span> <span data-ttu-id="faed4-118">Skilaboðastika tilkynnir þér einnig ef eignin fellur undir ábyrgðarsamning.</span><span class="sxs-lookup"><span data-stu-id="faed4-118">A message bar also notifies you if the asset is covered by a warranty agreement.</span></span>

6. <span data-ttu-id="faed4-119">Í reitnum **Þjónustustig** velurðu þjónustustig sem gefur til kynna hversu brýn beiðnin er.</span><span class="sxs-lookup"><span data-stu-id="faed4-119">In the **Service level** field, select a service level that indicates the urgency of the request.</span></span>
7. <span data-ttu-id="faed4-120">Ef þú valdir eign í þrepi 5 geturðu notað reitina **Bilunareinkenni**, **Bilunarsvæði** og **Bilunartegund** til að búa til villuskráningu.</span><span class="sxs-lookup"><span data-stu-id="faed4-120">If you selected an asset in step 5, you can use the **Fault symptom**, **Fault area**, and **Fault type** fields to create a fault registration.</span></span>
8. <span data-ttu-id="faed4-121">Ef viðhaldsbeiðnin hefur valdið niðurtíma vegna viðhalds skaltu slá inn upphafsdagsetningu og -tíma niðurtímans.</span><span class="sxs-lookup"><span data-stu-id="faed4-121">If the maintenance request has caused maintenance downtime, enter the start date and time of the downtime.</span></span>

    <span data-ttu-id="faed4-122">Reiturnn **Sett af stað af** er sjálfkrafa stilltur á nafnið þitt.</span><span class="sxs-lookup"><span data-stu-id="faed4-122">The **Started by** field is automatically set to your name.</span></span>

10. <span data-ttu-id="faed4-123">Reiturinn **Raunverulegt upphaf** er sjálfkrafa stilltur á núverandi dagsetningu og tíma.</span><span class="sxs-lookup"><span data-stu-id="faed4-123">The **Actual start** field is automatically set to the current date and time.</span></span> <span data-ttu-id="faed4-124">Þó er hægt að breyta gildinu eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="faed4-124">However, you can change the value as you require.</span></span>
11. <span data-ttu-id="faed4-125">Í reitnum **Athugasemdir** slærðu inn allar viðbótar athugasemdir sem þarf.</span><span class="sxs-lookup"><span data-stu-id="faed4-125">In the **Notes** field, enter any additional notes that are required.</span></span>
12. <span data-ttu-id="faed4-126">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="faed4-126">Select **OK**.</span></span>

![Stofna viðhaldsbeiðni](media/03-manage-maintenance-requests.png)

## <a name="subsequent-processing-of-maintenance-requests"></a><span data-ttu-id="faed4-128">Síðari afgreiðsla beiðna um viðhald</span><span class="sxs-lookup"><span data-stu-id="faed4-128">Subsequent processing of maintenance requests</span></span>

<span data-ttu-id="faed4-129">Eftir að viðhaldsbeiðni er stofnuð, en áður en henni er breytt í vinnupöntun, ætti að uppfæra ýmsar upplýsingar um hana.</span><span class="sxs-lookup"><span data-stu-id="faed4-129">After a maintenance request is created, but before it's converted to a work order, various information should be updated on it.</span></span> <span data-ttu-id="faed4-130">Venjulega klárar skipuleggjandi eða annar stjórnandi starfsmaður þetta verkefni.</span><span class="sxs-lookup"><span data-stu-id="faed4-130">Typically, a planner or another administrative employee completes this task.</span></span>

- <span data-ttu-id="faed4-131">Á síðunni **Allar viðhaldsbeiðnir** eða **Virkar viðhaldsbeiðnir** velurðu beiðnina sem þú vilt vinna með og velur síðan **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="faed4-131">On the **All maintenance requests** or **Active maintenance requests** page, select the request to work with, and then select **Edit**.</span></span>

<span data-ttu-id="faed4-132">Í upplýsingayfirlitinu geturðu uppfært ýmsar upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="faed4-132">In the details view, you can update various information.</span></span> <span data-ttu-id="faed4-133">Hér eru nokkur dæmi:</span><span class="sxs-lookup"><span data-stu-id="faed4-133">Here are some examples:</span></span>

- <span data-ttu-id="faed4-134">Veldu og staðfestu eignina.</span><span class="sxs-lookup"><span data-stu-id="faed4-134">Select and verify the asset.</span></span> <span data-ttu-id="faed4-135">Ef þú verður að velja aðra eign seinna geturðu stillt valkostinn **Eignir staðfestar** á **Nei**.</span><span class="sxs-lookup"><span data-stu-id="faed4-135">If you must select a different asset later, you can set the **Asset verified** option to **No**.</span></span>
- <span data-ttu-id="faed4-136">Veldu ábyrgan starfsmannahóp og/eða ábyrgan viðhaldsstarfsmann.</span><span class="sxs-lookup"><span data-stu-id="faed4-136">Select a responsible maintenance worker group and/or a responsible maintenance worker.</span></span> <span data-ttu-id="faed4-137">Nánari upplýsingar um nauðsynlega uppsetningu, sjá [Ábyrgir viðhaldsstarfskraftar](../setup-for-maintenance-requests/responsible-workers.md).</span><span class="sxs-lookup"><span data-stu-id="faed4-137">For more information about the required setup, see [Responsible maintenance workers](../setup-for-maintenance-requests/responsible-workers.md).</span></span>
- <span data-ttu-id="faed4-138">Veldu gerð viðhaldsverks og, ef þessar upplýsingar eru viðeigandi, tengt afbrigði viðhaldsverks og ði og atvinnuverslun.</span><span class="sxs-lookup"><span data-stu-id="faed4-138">Select a maintenance job type and, if this information is relevant, a related maintenance job variant and a job trade.</span></span>
- <span data-ttu-id="faed4-139">Í reitunum **Breidd** og **Lengdargráða** slærðu inn landfræðileg hnit.</span><span class="sxs-lookup"><span data-stu-id="faed4-139">In the **Latitude** and **Longitude** fields, enter geographic coordinates.</span></span> <span data-ttu-id="faed4-140">Öll hnit sem er bætt við viðhaldsbeiðni eru sjálfkrafa færð yfir í tengda verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="faed4-140">Any coordinates that are added to a maintenance request are automatically transferred to a related work order.</span></span> 

![Uppfæra viðhaldsbeiðni](media/04-manage-maintenance-requests.png)

> [!NOTE]
> <span data-ttu-id="faed4-142">Ef þú velur eign þegar þú býrð til viðhaldsbeiðni geturðu bætt einni villu við eignina.</span><span class="sxs-lookup"><span data-stu-id="faed4-142">If you select an asset when you create a maintenance request, you can add one fault to the asset.</span></span> <span data-ttu-id="faed4-143">Eftir að viðhaldsbeiðnin hefur verið stofnuð geturðu bætt við fleiri göllum eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="faed4-143">After the maintenance request has been created, you can add more faults, as you require.</span></span> <span data-ttu-id="faed4-144">Til að bæta við göllum velurðu **Eignavilla** á síðunni **Allar viðhaldsbeiðnir**.</span><span class="sxs-lookup"><span data-stu-id="faed4-144">To add faults, select **Asset fault** on the **All maintenance requests** page.</span></span>
