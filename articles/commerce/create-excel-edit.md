---
title: Stofna Excel-vinnubók til að breyta smásölufærslum
description: Þetta efnisatriði lýsir því hvernig á að bæta svæðum við Excel-vinnubók til að hægt sé að breyta smásölufærslum í Microsoft Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: b2b6e98db54e7747912aad26f4b8ae24b9ad5a6d
ms.sourcegitcommit: ce51ff2b6099c75dceb99de6dea9d53baf99772d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/04/2020
ms.locfileid: "4459281"
---
# <a name="create-an-excel-workbook-to-edit-retail-transactions"></a><span data-ttu-id="c5066-103">Stofna Excel-vinnubók til að breyta smásölufærslum</span><span class="sxs-lookup"><span data-stu-id="c5066-103">Create an Excel workbook to edit retail transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c5066-104">Þetta efnisatriði lýsir því hvernig á að bæta svæðum við Excel-vinnubók til að hægt sé að breyta smásölufærslum í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c5066-104">This topic describes how to create an Excel workbook so that you can edit retail transactions in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c5066-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="c5066-105">Overview</span></span>

<span data-ttu-id="c5066-106">Í boði er fyrirframskilgreint Excel-sniðmát sem viðskiptavinir geta opnað í ólíkum hlutum kerfisins og bæði notað til að breyta og endurskoða smásölufærslur.</span><span class="sxs-lookup"><span data-stu-id="c5066-106">There is a predefined Excel template that customers can access from different parts of the system and use to edit and audit retail transactions.</span></span> <span data-ttu-id="c5066-107">Viðskiptavinir hafa einnig kost á að stofna sérstillta Excel-vinnubók í þessum tilgangi.</span><span class="sxs-lookup"><span data-stu-id="c5066-107">However, customers can also create a custom Excel workbook for this purpose.</span></span>

## <a name="create-and-configure-an-excel-workbook"></a><span data-ttu-id="c5066-108">Stofna og grunnstilla Excel-vinnubók</span><span class="sxs-lookup"><span data-stu-id="c5066-108">Create and configure an Excel workbook</span></span>

<span data-ttu-id="c5066-109">Fylgið eftirfarandi skrefum til að stofna Excel-vinnubók til að hægt sé að breyta smásölufærslum.</span><span class="sxs-lookup"><span data-stu-id="c5066-109">To create and configure an Excel workbook so that you can edit retail transactions, follow these steps.</span></span>

1. <span data-ttu-id="c5066-110">Opnið Excel og stofnið auða vinnubók.</span><span class="sxs-lookup"><span data-stu-id="c5066-110">Open Excel, and create a blank workbook.</span></span>
1. <span data-ttu-id="c5066-111">Á flipanum **Setja inn** skal smella á **Innbæturnar mínar**.</span><span class="sxs-lookup"><span data-stu-id="c5066-111">On the **Insert** tab, select **My add-ins**.</span></span>
1. <span data-ttu-id="c5066-112">Á svæðinu til vinstri skal velja tengilinn **Bæta við upplýsingum um þjón**.</span><span class="sxs-lookup"><span data-stu-id="c5066-112">In the right pane, select the **Add server information** link.</span></span>
1. <span data-ttu-id="c5066-113">Sláið inn vefslóðina og smellið síðan á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="c5066-113">Enter the server URL, and then select **OK**.</span></span>
1. <span data-ttu-id="c5066-114">Fylgja skal eftirfarandi skrefum til að lagfæra vandamálið ef villuboðin „Engar skráningar smáforrita“ birtast:</span><span class="sxs-lookup"><span data-stu-id="c5066-114">If you receive a "No applet registrations found" error message, follow these steps to resolve the issue:</span></span>

    1. <span data-ttu-id="c5066-115">Opnið Commerce, **Kerfisstjórnun \> Uppsetning \> Færibreytur Office-forrits**.</span><span class="sxs-lookup"><span data-stu-id="c5066-115">In Commerce, go to **System administration \> Setup \> Office app parameters**.</span></span>
    1. <span data-ttu-id="c5066-116">Á flýtiflipanum **Færibreytur forrits** er smellt á **Frumstilla færibreytur forrits**.</span><span class="sxs-lookup"><span data-stu-id="c5066-116">On the **App parameters** FastTab, select **Initialize app parameters**.</span></span>
    1. <span data-ttu-id="c5066-117">Smellið á **Í lagi** í svarglugga staðfestingarboðanna.</span><span class="sxs-lookup"><span data-stu-id="c5066-117">In the confirmation message box, select **OK**.</span></span>
    1. <span data-ttu-id="c5066-118">Á flýtiflipanum **Skráð smáforrit** skal smella á **Frumstilla skráningu smáforrits**.</span><span class="sxs-lookup"><span data-stu-id="c5066-118">On the **Registered applets** FastTab, select **Initialize applet registration**.</span></span>
    1. <span data-ttu-id="c5066-119">Endurtakið fyrri þrjú skrefin eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="c5066-119">Repeat the previous three steps as required.</span></span>

1. <span data-ttu-id="c5066-120">Smellið á **Hönnun** og síðan á **Bæta við töflu**.</span><span class="sxs-lookup"><span data-stu-id="c5066-120">Select **Design**, and then select **Add table**.</span></span>
1. <span data-ttu-id="c5066-121">Veljið einingarnar sem verður bæta við Excel-vinnubókina til breytinga miðað við gögnin sem skal breyta.</span><span class="sxs-lookup"><span data-stu-id="c5066-121">Based on the data that has to be modified, select the entities that must be added to the Excel workbook for editing.</span></span> <span data-ttu-id="c5066-122">Notið töfluna hér á eftir til viðmiðunar.</span><span class="sxs-lookup"><span data-stu-id="c5066-122">Use the following table as a reference.</span></span>

    | <span data-ttu-id="c5066-123">Færslugerð</span><span class="sxs-lookup"><span data-stu-id="c5066-123">Transaction type</span></span> | <span data-ttu-id="c5066-124">Gagnaeiningar sem skal nota</span><span class="sxs-lookup"><span data-stu-id="c5066-124">Data entities to use</span></span> |
    |------------------|----------------------|
    | <span data-ttu-id="c5066-125">Staðgreiddar færslur, pantanir á netinu, ósamstilltar pantanir viðskiptavinar, ósamstillt tilboð viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="c5066-125">Cash and carry transactions, Online orders, Async customer orders, Async customer quotes</span></span> | <span data-ttu-id="c5066-126">Færsla (sannprófanleg), sölufærsla (sannprófanleg), greiðslufærslur (sannprófanlegar), skattfærslur (sannprófanlegar), afsláttarfærslur (sannprófanlegar), greiðslufærslur (sannprófanlegar)</span><span class="sxs-lookup"><span data-stu-id="c5066-126">Transaction (auditable), Sales transaction (auditable), Payment transactions (auditable), Tax transactions (auditable), Discount transactions (auditable), Charge transactions (auditable)</span></span> |
    | <span data-ttu-id="c5066-127">Peningaflutningur í banka</span><span class="sxs-lookup"><span data-stu-id="c5066-127">Bank drop</span></span> | <span data-ttu-id="c5066-128">Færsla (sannprófanleg), greiðslufærslur á vörslureikningi (sannprófanlegar)</span><span class="sxs-lookup"><span data-stu-id="c5066-128">Transaction (auditable), Banked tender transactions (auditable)</span></span> |
    | <span data-ttu-id="c5066-129">Peningaflutningur í öryggisskáp</span><span class="sxs-lookup"><span data-stu-id="c5066-129">Safe drop</span></span> | <span data-ttu-id="c5066-130">Færsla (sannprófanleg), greiðslufærslur í öryggisskáp (sannprófanlegar)</span><span class="sxs-lookup"><span data-stu-id="c5066-130">Transaction (auditable), Safe tender transactions (auditable)</span></span> |
    | <span data-ttu-id="c5066-131">Talning skiptimyntar</span><span class="sxs-lookup"><span data-stu-id="c5066-131">Tender declaration</span></span> | <span data-ttu-id="c5066-132">Færsla (sannprófanleg), talningarfærslur skiptimyntar (sannprófanlegar)</span><span class="sxs-lookup"><span data-stu-id="c5066-132">Transaction (auditable), Tender declaration transactions (auditable)</span></span> |
    | <span data-ttu-id="c5066-133">Tekjur, útgjöld</span><span class="sxs-lookup"><span data-stu-id="c5066-133">Income, Expense</span></span> | <span data-ttu-id="c5066-134">Færsla (sannprófanleg), tekju-/kostnaðarfærslur (sannprófanlegar), greiðslufærslur (sannprófanlegar)</span><span class="sxs-lookup"><span data-stu-id="c5066-134">Transaction (auditable), Income/Expense transactions (auditable), Payment transactions (auditable)</span></span> |
    | <span data-ttu-id="c5066-135">Skilgreina upphafsupphæð, skiptimynt fjarlægð, skiptimyntarfærsla, greiðslumáti skiptimyntar, greiðsla reiknings, innistæða viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="c5066-135">Declare starting amount, Tender removal, Float entry, Change tender, Invoice payment, Customer deposit</span></span> | <span data-ttu-id="c5066-136">Færsla (sannprófanleg), greiðslufærslur (sannprófanlegar)</span><span class="sxs-lookup"><span data-stu-id="c5066-136">Transaction (auditable), Payment transactions (auditable)</span></span> |

    > [!NOTE]
    > <span data-ttu-id="c5066-137">Gætið þess að bæta einungis einni gagnaeiningu við hverja Excel-vinnubók.</span><span class="sxs-lookup"><span data-stu-id="c5066-137">It's important that you add only one data entity to each Excel workbook.</span></span> <span data-ttu-id="c5066-138">Þar að auki verður að bæta öllum svæðum merktum með lykiltákni við viðeigandi Excel-vinnubók.</span><span class="sxs-lookup"><span data-stu-id="c5066-138">Additionally, all fields that are marked by a key symbol must be added to the relevant workbook.</span></span>

1. <span data-ttu-id="c5066-139">Notið áskildar síur þegar lokið er við að grunnstilla vinnubókina.</span><span class="sxs-lookup"><span data-stu-id="c5066-139">After the workbook is configured, apply the required filters.</span></span> <span data-ttu-id="c5066-140">Gætið þess að nota sömu síur í öllum vinnublöðum skráarinnar.</span><span class="sxs-lookup"><span data-stu-id="c5066-140">Be sure to apply the same filters to all the worksheets in the file.</span></span> <span data-ttu-id="c5066-141">Ekki hlaða miklu magni af gögnum inn í Excel-skrána.</span><span class="sxs-lookup"><span data-stu-id="c5066-141">Avoid loading very large amounts of data into the Excel file.</span></span> <span data-ttu-id="c5066-142">Að öðrum kosti kann að draga úr afköstum og Excel og kerfið kann að verða hægara.</span><span class="sxs-lookup"><span data-stu-id="c5066-142">Otherwise, performance might be affected, and Excel and your system might slow down.</span></span> <span data-ttu-id="c5066-143">Mælt er með því að „fyrirtæki“ og annað hvort „númer uppgjörs“ eða „færslunúmer“ sé alltaf notað sem síur fyrir viðkomandi skrá.</span><span class="sxs-lookup"><span data-stu-id="c5066-143">We recommend that you always use "Company" and either "Statement Number" or "Transaction Number" as filters for your file.</span></span>
1. <span data-ttu-id="c5066-144">Smellið á **Uppfæra** til að hlaða gögnunum inn eftir að grunnstillingu síanna er lokið.</span><span class="sxs-lookup"><span data-stu-id="c5066-144">After the filters are configured, select **Refresh** to load the data.</span></span>
1. <span data-ttu-id="c5066-145">Sláið inn áskilin gögn og birtið.</span><span class="sxs-lookup"><span data-stu-id="c5066-145">Edit the required data, and then publish it.</span></span> <span data-ttu-id="c5066-146">Ef hnappurinn **Birta** er ekki tiltækur var lykilsvæðum líklega ekki bætt í Excel-vinnubókina.</span><span class="sxs-lookup"><span data-stu-id="c5066-146">If the **Publish** button is unavailable, some key fields probably weren't added to the Excel workbook.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c5066-147">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="c5066-147">Additional resources</span></span>

[<span data-ttu-id="c5066-148">Breyta og endurskoða færslur staðgreiðslu við afhendingu og stjórnun reiðufjár</span><span class="sxs-lookup"><span data-stu-id="c5066-148">Edit and audit cash and carry and cash management transactions</span></span>](edit-cash-trans.md)

[<span data-ttu-id="c5066-149">Breyta og endurskoða netpöntun og ósamstilltar færslur pöntunar viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="c5066-149">Edit and audit online order and asynchronous customer order transactions</span></span>](edit-order-trans.md)

[<span data-ttu-id="c5066-150">Breyta fjárhagsvíddum fyrir smásölufærslur</span><span class="sxs-lookup"><span data-stu-id="c5066-150">Edit financial dimensions for retail transactions</span></span>](edit-financial-dim.md)

[<span data-ttu-id="c5066-151">Bæta svæðum við Excel-vinnubók til að breyta smásölufærslum</span><span class="sxs-lookup"><span data-stu-id="c5066-151">Add fields to an Excel workbook to edit retail transactions</span></span>](add-fields-excel.md)
