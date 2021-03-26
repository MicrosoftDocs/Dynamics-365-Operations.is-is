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
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3a4bc0a91ee2215dcde2f18575d58ab1ef2f5581
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5207944"
---
# <a name="create-an-excel-workbook-to-edit-retail-transactions"></a><span data-ttu-id="07c60-103">Stofna Excel-vinnubók til að breyta smásölufærslum</span><span class="sxs-lookup"><span data-stu-id="07c60-103">Create an Excel workbook to edit retail transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="07c60-104">Þetta efnisatriði lýsir því hvernig á að bæta svæðum við Excel-vinnubók til að hægt sé að breyta smásölufærslum í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="07c60-104">This topic describes how to create an Excel workbook so that you can edit retail transactions in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="07c60-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="07c60-105">Overview</span></span>

<span data-ttu-id="07c60-106">Í boði er fyrirframskilgreint Excel-sniðmát sem viðskiptavinir geta opnað í ólíkum hlutum kerfisins og bæði notað til að breyta og endurskoða smásölufærslur.</span><span class="sxs-lookup"><span data-stu-id="07c60-106">There is a predefined Excel template that customers can access from different parts of the system and use to edit and audit retail transactions.</span></span> <span data-ttu-id="07c60-107">Viðskiptavinir hafa einnig kost á að stofna sérstillta Excel-vinnubók í þessum tilgangi.</span><span class="sxs-lookup"><span data-stu-id="07c60-107">However, customers can also create a custom Excel workbook for this purpose.</span></span>

## <a name="create-and-configure-an-excel-workbook"></a><span data-ttu-id="07c60-108">Stofna og grunnstilla Excel-vinnubók</span><span class="sxs-lookup"><span data-stu-id="07c60-108">Create and configure an Excel workbook</span></span>

<span data-ttu-id="07c60-109">Fylgið eftirfarandi skrefum til að stofna Excel-vinnubók til að hægt sé að breyta smásölufærslum.</span><span class="sxs-lookup"><span data-stu-id="07c60-109">To create and configure an Excel workbook so that you can edit retail transactions, follow these steps.</span></span>

1. <span data-ttu-id="07c60-110">Opnið Excel og stofnið auða vinnubók.</span><span class="sxs-lookup"><span data-stu-id="07c60-110">Open Excel, and create a blank workbook.</span></span>
1. <span data-ttu-id="07c60-111">Á flipanum **Setja inn** skal smella á **Innbæturnar mínar**.</span><span class="sxs-lookup"><span data-stu-id="07c60-111">On the **Insert** tab, select **My add-ins**.</span></span>
1. <span data-ttu-id="07c60-112">Á svæðinu til vinstri skal velja tengilinn **Bæta við upplýsingum um þjón**.</span><span class="sxs-lookup"><span data-stu-id="07c60-112">In the right pane, select the **Add server information** link.</span></span>
1. <span data-ttu-id="07c60-113">Sláið inn vefslóðina og smellið síðan á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="07c60-113">Enter the server URL, and then select **OK**.</span></span>
1. <span data-ttu-id="07c60-114">Fylgja skal eftirfarandi skrefum til að lagfæra vandamálið ef villuboðin „Engar skráningar smáforrita“ birtast:</span><span class="sxs-lookup"><span data-stu-id="07c60-114">If you receive a "No applet registrations found" error message, follow these steps to resolve the issue:</span></span>

    1. <span data-ttu-id="07c60-115">Opnið Commerce, **Kerfisstjórnun \> Uppsetning \> Færibreytur Office-forrits**.</span><span class="sxs-lookup"><span data-stu-id="07c60-115">In Commerce, go to **System administration \> Setup \> Office app parameters**.</span></span>
    1. <span data-ttu-id="07c60-116">Á flýtiflipanum **Færibreytur forrits** er smellt á **Frumstilla færibreytur forrits**.</span><span class="sxs-lookup"><span data-stu-id="07c60-116">On the **App parameters** FastTab, select **Initialize app parameters**.</span></span>
    1. <span data-ttu-id="07c60-117">Smellið á **Í lagi** í svarglugga staðfestingarboðanna.</span><span class="sxs-lookup"><span data-stu-id="07c60-117">In the confirmation message box, select **OK**.</span></span>
    1. <span data-ttu-id="07c60-118">Á flýtiflipanum **Skráð smáforrit** skal smella á **Frumstilla skráningu smáforrits**.</span><span class="sxs-lookup"><span data-stu-id="07c60-118">On the **Registered applets** FastTab, select **Initialize applet registration**.</span></span>
    1. <span data-ttu-id="07c60-119">Endurtakið fyrri þrjú skrefin eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="07c60-119">Repeat the previous three steps as required.</span></span>

1. <span data-ttu-id="07c60-120">Smellið á **Hönnun** og síðan á **Bæta við töflu**.</span><span class="sxs-lookup"><span data-stu-id="07c60-120">Select **Design**, and then select **Add table**.</span></span>
1. <span data-ttu-id="07c60-121">Veljið einingarnar sem verður bæta við Excel-vinnubókina til breytinga miðað við gögnin sem skal breyta.</span><span class="sxs-lookup"><span data-stu-id="07c60-121">Based on the data that has to be modified, select the entities that must be added to the Excel workbook for editing.</span></span> <span data-ttu-id="07c60-122">Notið töfluna hér á eftir til viðmiðunar.</span><span class="sxs-lookup"><span data-stu-id="07c60-122">Use the following table as a reference.</span></span>

    | <span data-ttu-id="07c60-123">Færslugerð</span><span class="sxs-lookup"><span data-stu-id="07c60-123">Transaction type</span></span> | <span data-ttu-id="07c60-124">Gagnaeiningar sem skal nota</span><span class="sxs-lookup"><span data-stu-id="07c60-124">Data entities to use</span></span> |
    |------------------|----------------------|
    | <span data-ttu-id="07c60-125">Staðgreiddar færslur, pantanir á netinu, ósamstilltar pantanir viðskiptavinar, ósamstillt tilboð viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="07c60-125">Cash and carry transactions, Online orders, Async customer orders, Async customer quotes</span></span> | <span data-ttu-id="07c60-126">Færsla (sannprófanleg), sölufærsla (sannprófanleg), greiðslufærslur (sannprófanlegar), skattfærslur (sannprófanlegar), afsláttarfærslur (sannprófanlegar), greiðslufærslur (sannprófanlegar)</span><span class="sxs-lookup"><span data-stu-id="07c60-126">Transaction (auditable), Sales transaction (auditable), Payment transactions (auditable), Tax transactions (auditable), Discount transactions (auditable), Charge transactions (auditable)</span></span> |
    | <span data-ttu-id="07c60-127">Peningaflutningur í banka</span><span class="sxs-lookup"><span data-stu-id="07c60-127">Bank drop</span></span> | <span data-ttu-id="07c60-128">Færsla (sannprófanleg), greiðslufærslur á vörslureikningi (sannprófanlegar)</span><span class="sxs-lookup"><span data-stu-id="07c60-128">Transaction (auditable), Banked tender transactions (auditable)</span></span> |
    | <span data-ttu-id="07c60-129">Peningaflutningur í öryggisskáp</span><span class="sxs-lookup"><span data-stu-id="07c60-129">Safe drop</span></span> | <span data-ttu-id="07c60-130">Færsla (sannprófanleg), greiðslufærslur í öryggisskáp (sannprófanlegar)</span><span class="sxs-lookup"><span data-stu-id="07c60-130">Transaction (auditable), Safe tender transactions (auditable)</span></span> |
    | <span data-ttu-id="07c60-131">Talning skiptimyntar</span><span class="sxs-lookup"><span data-stu-id="07c60-131">Tender declaration</span></span> | <span data-ttu-id="07c60-132">Færsla (sannprófanleg), talningarfærslur skiptimyntar (sannprófanlegar)</span><span class="sxs-lookup"><span data-stu-id="07c60-132">Transaction (auditable), Tender declaration transactions (auditable)</span></span> |
    | <span data-ttu-id="07c60-133">Tekjur, útgjöld</span><span class="sxs-lookup"><span data-stu-id="07c60-133">Income, Expense</span></span> | <span data-ttu-id="07c60-134">Færsla (sannprófanleg), tekju-/kostnaðarfærslur (sannprófanlegar), greiðslufærslur (sannprófanlegar)</span><span class="sxs-lookup"><span data-stu-id="07c60-134">Transaction (auditable), Income/Expense transactions (auditable), Payment transactions (auditable)</span></span> |
    | <span data-ttu-id="07c60-135">Skilgreina upphafsupphæð, skiptimynt fjarlægð, skiptimyntarfærsla, greiðslumáti skiptimyntar, greiðsla reiknings, innistæða viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="07c60-135">Declare starting amount, Tender removal, Float entry, Change tender, Invoice payment, Customer deposit</span></span> | <span data-ttu-id="07c60-136">Færsla (sannprófanleg), greiðslufærslur (sannprófanlegar)</span><span class="sxs-lookup"><span data-stu-id="07c60-136">Transaction (auditable), Payment transactions (auditable)</span></span> |

    > [!NOTE]
    > <span data-ttu-id="07c60-137">Gætið þess að bæta einungis einni gagnaeiningu við hverja Excel-vinnubók.</span><span class="sxs-lookup"><span data-stu-id="07c60-137">It's important that you add only one data entity to each Excel workbook.</span></span> <span data-ttu-id="07c60-138">Þar að auki verður að bæta öllum svæðum merktum með lykiltákni við viðeigandi Excel-vinnubók.</span><span class="sxs-lookup"><span data-stu-id="07c60-138">Additionally, all fields that are marked by a key symbol must be added to the relevant workbook.</span></span>

1. <span data-ttu-id="07c60-139">Notið áskildar síur þegar lokið er við að grunnstilla vinnubókina.</span><span class="sxs-lookup"><span data-stu-id="07c60-139">After the workbook is configured, apply the required filters.</span></span> <span data-ttu-id="07c60-140">Gætið þess að nota sömu síur í öllum vinnublöðum skráarinnar.</span><span class="sxs-lookup"><span data-stu-id="07c60-140">Be sure to apply the same filters to all the worksheets in the file.</span></span> <span data-ttu-id="07c60-141">Ekki hlaða miklu magni af gögnum inn í Excel-skrána.</span><span class="sxs-lookup"><span data-stu-id="07c60-141">Avoid loading very large amounts of data into the Excel file.</span></span> <span data-ttu-id="07c60-142">Að öðrum kosti kann að draga úr afköstum og Excel og kerfið kann að verða hægara.</span><span class="sxs-lookup"><span data-stu-id="07c60-142">Otherwise, performance might be affected, and Excel and your system might slow down.</span></span> <span data-ttu-id="07c60-143">Mælt er með því að „fyrirtæki“ og annað hvort „númer uppgjörs“ eða „færslunúmer“ sé alltaf notað sem síur fyrir viðkomandi skrá.</span><span class="sxs-lookup"><span data-stu-id="07c60-143">We recommend that you always use "Company" and either "Statement Number" or "Transaction Number" as filters for your file.</span></span>
1. <span data-ttu-id="07c60-144">Smellið á **Uppfæra** til að hlaða gögnunum inn eftir að grunnstillingu síanna er lokið.</span><span class="sxs-lookup"><span data-stu-id="07c60-144">After the filters are configured, select **Refresh** to load the data.</span></span>
1. <span data-ttu-id="07c60-145">Sláið inn áskilin gögn og birtið.</span><span class="sxs-lookup"><span data-stu-id="07c60-145">Edit the required data, and then publish it.</span></span> <span data-ttu-id="07c60-146">Ef hnappurinn **Birta** er ekki tiltækur var lykilsvæðum líklega ekki bætt í Excel-vinnubókina.</span><span class="sxs-lookup"><span data-stu-id="07c60-146">If the **Publish** button is unavailable, some key fields probably weren't added to the Excel workbook.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="07c60-147">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="07c60-147">Additional resources</span></span>

[<span data-ttu-id="07c60-148">Breyta og endurskoða færslur staðgreiðslu við afhendingu og stjórnun reiðufjár</span><span class="sxs-lookup"><span data-stu-id="07c60-148">Edit and audit cash and carry and cash management transactions</span></span>](edit-cash-trans.md)

[<span data-ttu-id="07c60-149">Breyta og endurskoða netpöntun og ósamstilltar færslur pöntunar viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="07c60-149">Edit and audit online order and asynchronous customer order transactions</span></span>](edit-order-trans.md)

[<span data-ttu-id="07c60-150">Breyta fjárhagsvíddum fyrir smásölufærslur</span><span class="sxs-lookup"><span data-stu-id="07c60-150">Edit financial dimensions for retail transactions</span></span>](edit-financial-dim.md)

[<span data-ttu-id="07c60-151">Bæta svæðum við Excel-vinnubók til að breyta smásölufærslum</span><span class="sxs-lookup"><span data-stu-id="07c60-151">Add fields to an Excel workbook to edit retail transactions</span></span>](add-fields-excel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]