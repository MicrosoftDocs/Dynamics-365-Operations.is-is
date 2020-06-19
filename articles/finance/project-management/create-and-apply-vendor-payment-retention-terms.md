---
title: Stofna og nota varðveisluskilmála greiðslu lánardrottins
description: Í þessu efnisatriði eru upplýsingar um hvernig á að setja upp og vinna með varðveisluskilmála fyrir lánardrottnagreiðslur.
author: kfend
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 0e14050a79220b5d02763a025040edb934489d00
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410233"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a><span data-ttu-id="4e965-103">Stofna og nota varðveisluskilmála greiðslu lánardrottins</span><span class="sxs-lookup"><span data-stu-id="4e965-103">Create and apply vendor payment retention terms</span></span>

[!include [banner](../includes/banner.md)] 

<span data-ttu-id="4e965-104">Uppsetning varðveisluskilmála lánardrottnagreiðslu fyrir verk er gagnlegt þegar fyrirtækið vill halda eftir hluta af greiðslunum sem greiddar eru lánardrottni.</span><span class="sxs-lookup"><span data-stu-id="4e965-104">Setting up vendor payment retention terms for a project is useful when your organization wants to retain part of the payments made to a vendor.</span></span> <span data-ttu-id="4e965-105">Til dæmis þegar óskað er eftir að bíða með greiðslu til lánardrottins þangað til afurðirnar sem afhentar eru uppfylla væntingar þínar.</span><span class="sxs-lookup"><span data-stu-id="4e965-105">For example, when you want to hold payment to a vendor until the products delivered meet your expectations.</span></span> <span data-ttu-id="4e965-106">Hægt er að tilgreina varðveisluskilmála lánardrottnagreiðslu þegar samið er um lánardrottnasamning.</span><span class="sxs-lookup"><span data-stu-id="4e965-106">Vendor payment retention terms can be specified when you negotiate a vendor contract.</span></span>

## <a name="create-vendor-payment-retention-terms"></a><span data-ttu-id="4e965-107">Búa til varðveisluskilmála lánardrottnagreiðslu</span><span class="sxs-lookup"><span data-stu-id="4e965-107">Create vendor payment retention terms</span></span>

<span data-ttu-id="4e965-108">Hægt er að færa inn það hlutfall af greiðslu til lánardrottins sem varðveita á og hlutfall áður viðhaldinna upphæða sem losa á.</span><span class="sxs-lookup"><span data-stu-id="4e965-108">You can enter the percentage of vendor payment for retention and the percentage of the previously retained amounts to be released.</span></span> <span data-ttu-id="4e965-109">Upphæðir eru varðveittar sjálfkrafa á reikningum lánardrottna þar til samningur nær tilgreindri stöðu samningsloka.</span><span class="sxs-lookup"><span data-stu-id="4e965-109">Amounts are automatically retained on vendor invoices until the contract reaches the specified state of completion.</span></span> <span data-ttu-id="4e965-110">Eftir að varðveisluskilmálarnir eru settir upp er hægt að nota þá í hvaða verki sem er fyrir þennan lánardrottin.</span><span class="sxs-lookup"><span data-stu-id="4e965-110">After you set up the retention terms, you can apply them to any project for that vendor.</span></span>

<span data-ttu-id="4e965-111">Notið eftirfarandi skref til að setja upp og vinna með varðveisluskilmála fyrir lánardrottnagreiðslur.</span><span class="sxs-lookup"><span data-stu-id="4e965-111">Use the following steps to set up and maintain retention terms for vendor payments.</span></span> 

1. <span data-ttu-id="4e965-112">Opnið **Verkefnastjórnun og bókhald** > **Varðveisla** > **Varðveisluskilmálar lánardrottnagreiðslu**.</span><span class="sxs-lookup"><span data-stu-id="4e965-112">Go to **Project management and accounting** > **Retention** > **Vendor payment retention terms**.</span></span>
2. <span data-ttu-id="4e965-113">Veljið **Nýr** til að bæta við nýjum varðveisluskilmála lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="4e965-113">Select **New** to add a new vendor retention term.</span></span> <span data-ttu-id="4e965-114">Gildið fyrir **Reglukenni** nýja hugtaksins er fært inn sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="4e965-114">The **Rule ID** value for the new term is automatically entered.</span></span> 
3. <span data-ttu-id="4e965-115">Sláið inn stutta lýsingu í reitnum **Lýsing** og í flýtiflipanum **Skilmálar** skal velja **Bæta við línu** til að færa inn gildi skilmála fyrir eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="4e965-115">Enter a brief description in the **Description** field, and on the **Terms** FastTab, select **Add line** to enter term values for the following:</span></span>

   - <span data-ttu-id="4e965-116">**Prósenta afhentra eininga**: Færið inn prósentu þess sem er lokið fyrir skilmálann.</span><span class="sxs-lookup"><span data-stu-id="4e965-116">**Percentage of units delivered**: Enter a percentage of completion for the term.</span></span> <span data-ttu-id="4e965-117">Upphæðir eru sjálfkrafa varðveittar á reikningum lánardrottna þar til verkstigi sem er lokið jafngildir tilgreindri prósentu.</span><span class="sxs-lookup"><span data-stu-id="4e965-117">Amounts are automatically retained on vendor invoices until the project stage of completion is equal to the specified percentage.</span></span> <span data-ttu-id="4e965-118">Til dæmis, ef fært er inn 50.00 eru upphæðir geymdar þar til 50 prósentum af verkinu er lokið.</span><span class="sxs-lookup"><span data-stu-id="4e965-118">For example, if you enter 50.00, amounts are retained until the project is 50 percent completed.</span></span>
   - <span data-ttu-id="4e965-119">**Prósenta til varðveislu**: Færa skal inn prósentu af reikningsupphæð lánardrottins sem á að varðveita.</span><span class="sxs-lookup"><span data-stu-id="4e965-119">**Percentage to retain**: Enter a percentage of the vendor invoice amount to be retained.</span></span> <span data-ttu-id="4e965-120">Til dæmis, ef fært er inn 10,00, þá eru 10 prósent upphæðarinnar á reikningi lánardrottins varðveitt þar til verkið nær yfir þá prósentu sem er lokið eins og það er stillt í reitnum **Prósenta afhentra eininga**.</span><span class="sxs-lookup"><span data-stu-id="4e965-120">For example, if you enter 10.00, then 10 percent of the amount on a vendor invoice is retained until the project reaches the percentage of completion as set in the **Percentage of units delivered field**.</span></span>
   - <span data-ttu-id="4e965-121">**Prósenta til losunar**: Veljið **Bæta við línu** til að færa inn prósentu af áður varðveittum upphæðum sem á að losa fyrir valið stig verks sem er lokið.</span><span class="sxs-lookup"><span data-stu-id="4e965-121">**Percentage to release**: Select **Add line** to enter a percentage of any previously retained amounts to be released for the selected level of project completion.</span></span>

> [!NOTE]
> <span data-ttu-id="4e965-122">Ef til eru fleiri en ein þáttaskil fyrir mismunandi stig verkloka skal færa inn sérstaka varðveisluskilmálalínu lánardrottins fyrir hverja varðveislureglu.</span><span class="sxs-lookup"><span data-stu-id="4e965-122">If you have more than one milestone for different levels of project completion, enter a separate vendor retention term line for each retention rule.</span></span> <span data-ttu-id="4e965-123">Hver lína getur tilgreint mismunandi varðveisluprósentu og mismunandi losunarprósentu fyrir hvert uppgefið stig verkloka.</span><span class="sxs-lookup"><span data-stu-id="4e965-123">Each line can specify a different retention percentage and a different release percentage for each designated level of project completion.</span></span>

<span data-ttu-id="4e965-124">Þegar varðveisluskilmálar lánardrottins er búnir til fyrir lánardrottin er hægt að nota skilmálana fyrir verk.</span><span class="sxs-lookup"><span data-stu-id="4e965-124">After you create vendor retention terms for a vendor, you can apply the terms to a project.</span></span>

## <a name="apply-vendor-retention-terms-to-a-project"></a><span data-ttu-id="4e965-125">Nota varðveisluskilmála lánardrottins í verk</span><span class="sxs-lookup"><span data-stu-id="4e965-125">Apply vendor retention terms to a project</span></span>

1. <span data-ttu-id="4e965-126">Opnið **Verkefnastjórnun og bókhald** > **Verk** > **Öll verk** og opnið verk á listasíðu verksins.</span><span class="sxs-lookup"><span data-stu-id="4e965-126">Go to **Project management and accounting** > **Projects** > **All projects** and open a project from the project list page.</span></span>
2. <span data-ttu-id="4e965-127">Á flýtiflipanum **Samningar lánardrottins** velurðu **Bæta við línu**.</span><span class="sxs-lookup"><span data-stu-id="4e965-127">On the **Vendor agreements** FastTab, select **Add line**.</span></span>
3. <span data-ttu-id="4e965-128">Veljið einn eftirfarandi valkosta í svæðinu **Lykilkóði**:</span><span class="sxs-lookup"><span data-stu-id="4e965-128">In the **Account code field**, select one of the following options:</span></span> 

   - <span data-ttu-id="4e965-129">**Tafla**: Varðveisluskilmálar lánardrottins eiga við um einn stakan lánardrottinn.</span><span class="sxs-lookup"><span data-stu-id="4e965-129">**Table**: The vendor retention terms apply to a single vendor.</span></span>
   - <span data-ttu-id="4e965-130">**Flokka** – Varðveisluskilmálar lánardrottins eiga við um alla lánardrottna í lánardrottnaflokki.</span><span class="sxs-lookup"><span data-stu-id="4e965-130">**Group**: The vendor retention terms apply to all vendors in a vendor group.</span></span>
   - <span data-ttu-id="4e965-131">**Allt** – Varðveisluskilmálar lánardrottins eiga við um alla lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="4e965-131">**All**: The vendor retention terms apply to all vendors.</span></span>

4. <span data-ttu-id="4e965-132">Á svæðinu **Lánardrottinn/lánardrottnaflokkur** er valinn sá lánardrottinn eða lánardrottnaflokkur sem varðveisluskilmálar lánardrottins eiga við um.</span><span class="sxs-lookup"><span data-stu-id="4e965-132">In the **Vendor/Vendor group field**, select the vendor or vendor group to which the vendor retention terms apply.</span></span> <span data-ttu-id="4e965-133">Ef **Allir** var valið í skrefinu á undan er þetta svæði ekki tiltækt.</span><span class="sxs-lookup"><span data-stu-id="4e965-133">If you selected **All** in the previous step, this field is unavailable.</span></span>
5. <span data-ttu-id="4e965-134">Í reitnum **Varðveisluskilmálar lánardrottins** skal velja varðveisluskilmálana sem voru búnir til í ferlinu á undan.</span><span class="sxs-lookup"><span data-stu-id="4e965-134">In the **Vendor retention terms** field, select the retention terms that you created in the previous procedure.</span></span>
6. <span data-ttu-id="4e965-135">Ef „greiðist-þegar-greitt“-skilmálar (GÞG) hafa einnig verið settir upp fyrir lánardrottin skal færa inn þröskuldsprósentuna fyrir verkið í reitinn **GÞG-þröskuldsprósenta**.</span><span class="sxs-lookup"><span data-stu-id="4e965-135">If the project also has pay-when-paid (PWP) terms set up for the vendor, enter the threshold percentage for the project in the **PWP threshold percentage** field.</span></span>

<span data-ttu-id="4e965-136">Varðveisluskilmálar lánardrottins birtast einnig á innkaupapöntunum sem gerðar eru fyrir lánardrottininn.</span><span class="sxs-lookup"><span data-stu-id="4e965-136">The vendor retention terms are also displayed on purchase orders that you create for the vendor.</span></span>
