---
title: Breyta og endurskoða netpöntun og ósamstilltum færslum pöntunar viðskiptavinar
description: Þetta efnisatriði lýsir því hvernig á að breyta og endurskoða netpöntun og ósamstilltar færslur pöntunar viðskiptavinar í Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: b9f2db25c8897662baa177752d0c5fc4ac6178a4
ms.sourcegitcommit: ce51ff2b6099c75dceb99de6dea9d53baf99772d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/04/2020
ms.locfileid: "4459279"
---
# <a name="edit-and-audit-online-order-and-asynchronous-customer-order-transactions"></a><span data-ttu-id="63d0b-103">Breyta og endurskoða netpöntun og ósamstilltum færslum pöntunar viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="63d0b-103">Edit and audit online order and asynchronous customer order transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="63d0b-104">Þetta efnisatriði lýsir því hvernig á að breyta og endurskoða netpöntun og ósamstilltar færslur pöntunar viðskiptavinar í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="63d0b-104">This topic describes how to edit and audit online order and asynchronous customer order transactions in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="63d0b-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="63d0b-105">Overview</span></span>

<span data-ttu-id="63d0b-106">Stuðningi var bætt við Commerce-útgáfur 10.0.5 og 10.0.6 til að gera breytingar á staðgreiddum færslum (eins og sölu og vöruskilum) og reiðufjárstjórnunarfærslum (eins og skiptimyntarfærslum og að fjarlægja skiptimynt).</span><span class="sxs-lookup"><span data-stu-id="63d0b-106">Between Commerce versions 10.0.5 and 10.0.6, support was added for editing cash and carry transactions (such as sales and returns) and cash management transactions (such as float entry and tender removal).</span></span> <span data-ttu-id="63d0b-107">Stuðningi var bætt við Commerce-útgáfu 10.0.7 fyrir breytingar á pöntunarfærslum á netinu og ósamstilltum pöntunum viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="63d0b-107">In Commerce version 10.0.7, support was added for editing online order transactions and asynchronous customer order transactions.</span></span>

## <a name="edit-and-audit-order-transactions"></a><span data-ttu-id="63d0b-108">Breyta og endurskoða pöntunarfærslur</span><span class="sxs-lookup"><span data-stu-id="63d0b-108">Edit and audit order transactions</span></span>

<span data-ttu-id="63d0b-109">Fylgið eftirfarandi skrefum til að breyta og endurskoða pöntunarfærslur í Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="63d0b-109">To edit and audit order transactions in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="63d0b-110">Setjið upp [Microsoft Dynamics Office Add-in](https://appsource.microsoft.com/product/office/WA104379629?tab=Overview).</span><span class="sxs-lookup"><span data-stu-id="63d0b-110">Install the [Microsoft Dynamics Office Add-in](https://appsource.microsoft.com/product/office/WA104379629?tab=Overview).</span></span>
1. <span data-ttu-id="63d0b-111">Opnið síðuna **Færibreytur smásölu** á flipanum **Pantanir viðskiptavinar** á flýtiflipanum **Pöntun**, tilgreinið biðkóða fyrir **Biðkóði fyrir villur við samstillingu pöntunar**.</span><span class="sxs-lookup"><span data-stu-id="63d0b-111">On the **Retail parameters** page, on the **Customer orders** tab, on the **Order** FastTab, specify a hold code for **Hold code for order synchronization errors**.</span></span>
1. <span data-ttu-id="63d0b-112">Opnið vinnusvæðið **Fjármál verslunar**.</span><span class="sxs-lookup"><span data-stu-id="63d0b-112">Open the **Store financials** workspace.</span></span> <span data-ttu-id="63d0b-113">Reitirnir **Samstillingarvillur í pöntunum á netinu** og **Samstillingarvillur í pöntunum viðskiptavina** birta yfirlit af síðu smásölufærslna sem þegar hefur verið síað.</span><span class="sxs-lookup"><span data-stu-id="63d0b-113">The **Online order synchronization errors** and **Customer order synchronization errors** tiles provide a prefiltered view of the retail transaction page.</span></span> <span data-ttu-id="63d0b-114">Hver breyting birtir færsluskrár þar sem samstilling á samsvarandi pöntunargerð tókst ekki.</span><span class="sxs-lookup"><span data-stu-id="63d0b-114">Each shows the transaction records that have failed synchronization for the corresponding order type.</span></span>
1. <span data-ttu-id="63d0b-115">Opnið annað hvort síðuna **Samstillingarvillur í pöntunum á netinu** eða síðuna **Samstillingarvillur í pöntunum viðskiptavina**.</span><span class="sxs-lookup"><span data-stu-id="63d0b-115">Open either the **Online order synchronization errors** page or the **Customer order synchronization errors** page.</span></span> <span data-ttu-id="63d0b-116">Smellið á skrá til að skoða villuupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="63d0b-116">Select a record to view the synchronization error details.</span></span> <span data-ttu-id="63d0b-117">Flýtiflipinn **Staða samstillingar** veitir eftirfarandi upplýsingar um villuna:</span><span class="sxs-lookup"><span data-stu-id="63d0b-117">The **Synchronization status** FastTab provides the following error details:</span></span>

    - <span data-ttu-id="63d0b-118">Staða pöntunar í bið</span><span class="sxs-lookup"><span data-stu-id="63d0b-118">Pending order status</span></span>
    - <span data-ttu-id="63d0b-119">Upplýsingar um pöntunarvillu</span><span class="sxs-lookup"><span data-stu-id="63d0b-119">Order error details</span></span>
    - <span data-ttu-id="63d0b-120">Breytt dagsetning og tími</span><span class="sxs-lookup"><span data-stu-id="63d0b-120">Modified date and time</span></span>
    - <span data-ttu-id="63d0b-121">Fjöldi tilrauna</span><span class="sxs-lookup"><span data-stu-id="63d0b-121">Retry count</span></span>

1. <span data-ttu-id="63d0b-122">Þegar villuupplýsingarnar tilgreina að lagfæra skuli skrána skal velja **Office-viðbót** og síðan **Breyta valinni færslu**.</span><span class="sxs-lookup"><span data-stu-id="63d0b-122">If the error details indicate that the record must be fixed, select **Office Add in**, and then select **Edit selected transaction**.</span></span> <span data-ttu-id="63d0b-123">Excel-skrá með upplýsingum um valda færslu opnast.</span><span class="sxs-lookup"><span data-stu-id="63d0b-123">An Excel file that shows the details of the selected transaction is opened.</span></span>

    - <span data-ttu-id="63d0b-124">Excel-skráin inniheldur eftirfarandi vinnublöð ef færslan sem var breytt er pöntunarfærsla á netinu:</span><span class="sxs-lookup"><span data-stu-id="63d0b-124">If the transaction that is being edited is an online order transaction, the Excel file contains the following worksheets:</span></span>

        - <span data-ttu-id="63d0b-125">**Færsla** – Þetta vinnublað er með hausupplýsingar fyrir færsluna.</span><span class="sxs-lookup"><span data-stu-id="63d0b-125">**Transaction** – This worksheet has the header details for the transaction.</span></span>
        - <span data-ttu-id="63d0b-126">**Sölufærsla** – Þetta vinnublað er með línuupplýsingar fyrir færsluna.</span><span class="sxs-lookup"><span data-stu-id="63d0b-126">**Sales transaction** – This worksheet has the line details for the transaction.</span></span>
        - <span data-ttu-id="63d0b-127">**Greiðslufærslur** – Þetta vinnublað er með upplýsingar um greiðslulínur fyrir færsluna.</span><span class="sxs-lookup"><span data-stu-id="63d0b-127">**Payment transactions** – This worksheet has the details of the payment lines for the transaction.</span></span>
        - <span data-ttu-id="63d0b-128">**Afsláttarfærslur** – Þetta vinnublað er með afsláttartengdar upplýsingar fyrir færsluna.</span><span class="sxs-lookup"><span data-stu-id="63d0b-128">**Discount transactions** – This worksheet has the discount-related details for the transaction.</span></span>
        - <span data-ttu-id="63d0b-129">**Skattafærslur** – Þetta vinnublað er með skatttengdar upplýsingar fyrir færsluna.</span><span class="sxs-lookup"><span data-stu-id="63d0b-129">**Tax transactions** – This worksheet has the tax-related details for the transaction.</span></span>
        - <span data-ttu-id="63d0b-130">**Gjaldafærslur** – Þetta vinnublað er með gjaldtengdar upplýsingar fyrir færsluna.</span><span class="sxs-lookup"><span data-stu-id="63d0b-130">**Charges transactions** – This worksheet has the charges-related data for the transaction.</span></span>

    - <span data-ttu-id="63d0b-131">Excel-skráin inniheldur eftirfarandi vinnublöð ef færslan sem var breytt er ósamstillt pöntun viðskiptavinar:</span><span class="sxs-lookup"><span data-stu-id="63d0b-131">If the transaction that is being edited is an asynchronous customer order transaction, the Excel file contains the following worksheets:</span></span>

        - <span data-ttu-id="63d0b-132">**Línur** – Þetta vinnublað er með haus- og línuupplýsingar fyrir færsluna.</span><span class="sxs-lookup"><span data-stu-id="63d0b-132">**Lines** – This worksheet has the header and line details for the transaction.</span></span>
        - <span data-ttu-id="63d0b-133">**Greiðslur** – Þetta vinnublað er með upplýsingar um greiðslulínur fyrir færsluna.</span><span class="sxs-lookup"><span data-stu-id="63d0b-133">**Payments** – This worksheet has the details of the payment lines for the transaction.</span></span>
        - <span data-ttu-id="63d0b-134">**Afslættir** – Þetta vinnublað er með afsláttartengdar upplýsingar fyrir færsluna.</span><span class="sxs-lookup"><span data-stu-id="63d0b-134">**Discounts** – This worksheet has the discount-related details for the transaction.</span></span>
        - <span data-ttu-id="63d0b-135">**Skattar** – Þetta vinnublað er með upplýsingar um skatt sem tengist færslunni.</span><span class="sxs-lookup"><span data-stu-id="63d0b-135">**Taxes** – This worksheet has the tax-related details for the transaction.</span></span>
        - <span data-ttu-id="63d0b-136">**Gjöld** – Þetta vinnublað er með gjaldtengdar upplýsingar fyrir færsluna.</span><span class="sxs-lookup"><span data-stu-id="63d0b-136">**Charges** – This worksheet has the charges-related data for the transaction.</span></span>

1. <span data-ttu-id="63d0b-137">Opnið Excel-skrána, veljið svæðið **Staða pöntunar í bið**, sláið inn **Breyta** og birtið síðan breytinguna.</span><span class="sxs-lookup"><span data-stu-id="63d0b-137">In the Excel file, in the **Pending order status** field, enter **Editing**, and then publish the change.</span></span> <span data-ttu-id="63d0b-138">Þannig er komið í veg fyrir að verkið **Samstilla pöntun** sem er í keyrslu í runustillingu sleppi þessari skrá við úrvinnslu.</span><span class="sxs-lookup"><span data-stu-id="63d0b-138">In this way, you prevent the **Synchronize order** job that is running in batch mode from skipping this record during processing.</span></span>
1. <span data-ttu-id="63d0b-139">Í Excel-skránni er viðeigandi reitum breytt og gögnunum svo hlaðið aftur upp í Commerce Headquarters með birtingaraðgerð Excel-innbótarinnar í Dynamics.</span><span class="sxs-lookup"><span data-stu-id="63d0b-139">In the Excel file, modify the appropriate fields, and then upload the data back into Commerce headquarters by using the publishing functionality of the Dynamics Excel Add-in.</span></span> <span data-ttu-id="63d0b-140">Breytingarnar koma fram í kerfinu þegar búið er að birta gögnin.</span><span class="sxs-lookup"><span data-stu-id="63d0b-140">After the data is published, the changes will be reflected in the system.</span></span> <span data-ttu-id="63d0b-141">Meðan á birtingu stendur fer engin villuleit fram á breytingunum sem notendur gera.</span><span class="sxs-lookup"><span data-stu-id="63d0b-141">During publication, no validation is done for changes that users make.</span></span>
1. <span data-ttu-id="63d0b-142">Hægt er að skoða alla færsluslóð breytinganna með því að velja **Skoða slóð endurskoðunar** í hausnum **Smásölufærsla** til að sjá breytingar á haus og í viðeigandi hluta og færslu á viðeigandi færslusíðu.</span><span class="sxs-lookup"><span data-stu-id="63d0b-142">You can view a complete audit trail of the changes by selecting **View audit trail** in the **Retail transaction** header for the header-level changes, and in the relevant section and record on the appropriate transaction page.</span></span> <span data-ttu-id="63d0b-143">Til dæmis verða allar breytingar sem tengjast sölulínum sýnilegar á síðunni **Sölufærslur** og allar breytingar sem tengjast greiðslum verða sýnilegar á síðunni **Greiðslufærslur**.</span><span class="sxs-lookup"><span data-stu-id="63d0b-143">For example, all changes that are related to sales lines will be shown on the **Sales transactions** page, and all changes that are related to payments will be shown on the **Payment transactions** page.</span></span> <span data-ttu-id="63d0b-144">Eftirfarandi upplýsingum um endurskoðun er haldið við fyrir breytingarnar:</span><span class="sxs-lookup"><span data-stu-id="63d0b-144">The following audit details are maintained for the changes:</span></span>

    - <span data-ttu-id="63d0b-145">Breytt dagsetning og tími</span><span class="sxs-lookup"><span data-stu-id="63d0b-145">Modified date and time</span></span>
    - <span data-ttu-id="63d0b-146">Svæði</span><span class="sxs-lookup"><span data-stu-id="63d0b-146">Field</span></span>
    - <span data-ttu-id="63d0b-147">Gamalt gildi</span><span class="sxs-lookup"><span data-stu-id="63d0b-147">Old value</span></span>
    - <span data-ttu-id="63d0b-148">Nýtt gildi</span><span class="sxs-lookup"><span data-stu-id="63d0b-148">New value</span></span>
    - <span data-ttu-id="63d0b-149">Breytt af</span><span class="sxs-lookup"><span data-stu-id="63d0b-149">Modified by</span></span>

1. <span data-ttu-id="63d0b-150">Þegar lokið er við að gera breytingar og þær hafa verið birtar skal smella á **Samstilla pöntun** til að hefja samstillingarferlið strax.</span><span class="sxs-lookup"><span data-stu-id="63d0b-150">After you've made and published your changes, select **Synchronize order** to immediately start the synchronization process.</span></span> <span data-ttu-id="63d0b-151">Einnig er hægt að bíða eftir að samstillingarferlið sem er keyrt í runustillingu ljúki við að vinna úr færslunni.</span><span class="sxs-lookup"><span data-stu-id="63d0b-151">Alternatively, you can wait for the synchronization process that is running in batch mode to process the transaction.</span></span>

<span data-ttu-id="63d0b-152">Þegar samstillingu pantana er lokið eru þær sjálfgefið settar í biðstöðu, á grundvelli biðkóðans sem er skilgreindur í færibreytum Commerce.</span><span class="sxs-lookup"><span data-stu-id="63d0b-152">By default, after the orders are successfully synced, they are put in a hold status, based on the hold code that is defined in the Commerce parameters.</span></span> <span data-ttu-id="63d0b-153">Áður en hægt er að vinna úr pöntununum fyrir uppfyllingu eða aðrar aðgerðir þarf að taka pantanirnar úr biðstöðu.</span><span class="sxs-lookup"><span data-stu-id="63d0b-153">The hold on the orders must be removed before the orders can be processed further for fulfillment or other operations.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="63d0b-154">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="63d0b-154">Additional resources</span></span>

[<span data-ttu-id="63d0b-155">Breyta og endurskoða færslur staðgreiðslu við afhendingu og stjórnun reiðufjár</span><span class="sxs-lookup"><span data-stu-id="63d0b-155">Edit and audit cash and carry and cash management transactions</span></span>](edit-cash-trans.md)

[<span data-ttu-id="63d0b-156">Breyta fjárhagsvíddum fyrir smásölufærslur</span><span class="sxs-lookup"><span data-stu-id="63d0b-156">Edit financial dimensions for retail transactions</span></span>](edit-financial-dim.md)

[<span data-ttu-id="63d0b-157">Stofna Excel-vinnubók til að breyta smásölufærslum</span><span class="sxs-lookup"><span data-stu-id="63d0b-157">Create an Excel workbook to edit retail transactions</span></span>](create-excel-edit.md)

[<span data-ttu-id="63d0b-158">Bæta svæðum við Excel-vinnubók til að breyta smásölufærslum</span><span class="sxs-lookup"><span data-stu-id="63d0b-158">Add fields to an Excel workbook to edit retail transactions</span></span>](add-fields-excel.md)
