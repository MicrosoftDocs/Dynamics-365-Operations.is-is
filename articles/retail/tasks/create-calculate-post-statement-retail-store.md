--- 
title: "Stofna, reikna og bóka yfirlit fyrir smásöluverslun"
description: "Þetta ferli fer í gegnum handvirkar skref til að stofna, reikna út og bóka uppgjör fyrir verslun."
author: jashanno
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 1c31c849c4c72762f0fdeb3f1d256cd3529394b2
ms.contentlocale: is-is
ms.lasthandoff: 08/09/2018

---
# <a name="create-calculate-and-post-statements-for-a-retail-store"></a><span data-ttu-id="69435-103">Stofna, reikna og bóka yfirlit fyrir smásöluverslun</span><span class="sxs-lookup"><span data-stu-id="69435-103">Create, calculate, and post statements for a retail store</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="69435-104">Þetta ferli fer í gegnum handvirkar skref til að stofna, reikna út og bóka uppgjör fyrir verslun.</span><span class="sxs-lookup"><span data-stu-id="69435-104">This procedure walks through the manual steps for creating, calculating, and posting a statement for a store.</span></span> <span data-ttu-id="69435-105">Einnig eru runuvinnslur sem hægt er að skilgreina fyrir sama verk.</span><span class="sxs-lookup"><span data-stu-id="69435-105">There are also batch jobs that can be configured for the same tasks.</span></span> <span data-ttu-id="69435-106">Skrefin til að skilgreina og keyra sem runuvinnslur er að finna í öðrum efnisatriði.</span><span class="sxs-lookup"><span data-stu-id="69435-106">The steps for configuring and running the batch jobs can be found in other topics.</span></span> <span data-ttu-id="69435-107">Til að ljúka þessu ferli, verður að hafa færslur sem voru fylltir út í sölustaður og síðan dregin inn í Dynamics AX.</span><span class="sxs-lookup"><span data-stu-id="69435-107">To complete this procedure, you must have transactions that were completed in POS and then pulled into Dynamics AX.</span></span> <span data-ttu-id="69435-108">Þessi skráning notar sýnigögn fyrirtæki USRT .</span><span class="sxs-lookup"><span data-stu-id="69435-108">This recording uses the USRT company in demo data.</span></span> <span data-ttu-id="69435-109">Þetta ferli gæti vísað til Microsoft Dynamics AX.</span><span class="sxs-lookup"><span data-stu-id="69435-109">This procedure may refer to Microsoft Dynamics AX.</span></span> <span data-ttu-id="69435-110">Athugaðu að Dynamics AX er nú kallað Microsoft Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="69435-110">Please note that Dynamics AX is now called Microsoft Dynamics 365 for Operations.</span></span>

1. <span data-ttu-id="69435-111">Fara í Öll vinnusvæði > ..</span><span class="sxs-lookup"><span data-stu-id="69435-111">Go to All workspaces > ..</span></span> <span data-ttu-id="69435-112">> Fjárhagur smásöluverslunar</span><span class="sxs-lookup"><span data-stu-id="69435-112">> Retail store financials.</span></span>
2. <span data-ttu-id="69435-113">Smella á Nýtt uppgjör.</span><span class="sxs-lookup"><span data-stu-id="69435-113">Click New statement.</span></span>
3. <span data-ttu-id="69435-114">Í reitnum verslunarnúmer skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="69435-114">In the Store number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="69435-115">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="69435-115">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="69435-116">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="69435-116">Click OK.</span></span>
    * <span data-ttu-id="69435-117">Uppsetning flokka hefur stillingarnar sem stýra hvaða færslur eru teknar með í uppgjörinu og hvernig þau eru flokkuð í uppgjörslínunum.</span><span class="sxs-lookup"><span data-stu-id="69435-117">The Setup group has the settings that control what transactions are included in the statement and how they are grouped into statement lines.</span></span> <span data-ttu-id="69435-118">Hægt er að opna Uppsetningu flokka og breyta þessum stillingum, eða hægt er að nota sem sjálfgildi.</span><span class="sxs-lookup"><span data-stu-id="69435-118">You can open the Setup group and change these settings, or you can use the defaults.</span></span>  
    * <span data-ttu-id="69435-119">svæðið uppgjörsaðferð skilgreinir hvernig uppgjörslínurnar verða flokkaðar.</span><span class="sxs-lookup"><span data-stu-id="69435-119">The Statement method field defines how the statement lines will be grouped.</span></span>  
    * <span data-ttu-id="69435-120">Veljið afgreiðslukassa eða starfsmaður eigi að reikna uppgjör aðeins fyrir tiltekinn starfsmaður eða afgreiðslukassa.</span><span class="sxs-lookup"><span data-stu-id="69435-120">Select a staff member or a register if you want to calculate a statement only for the specific staff member or register.</span></span>  
6. <span data-ttu-id="69435-121">Í reitnum lokunaraðferð skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="69435-121">In the Closing method field, select an option.</span></span>
7. <span data-ttu-id="69435-122">Smellt er á Reikna út uppgjör.</span><span class="sxs-lookup"><span data-stu-id="69435-122">Click Calculate statement.</span></span>
8. <span data-ttu-id="69435-123">Smella á Já.</span><span class="sxs-lookup"><span data-stu-id="69435-123">Click Yes.</span></span>
    * <span data-ttu-id="69435-124">Eftir að reikna uppgjör, ætti að vera eru stofnaðar línur með heildarupphæðir fyrir hvern greiðslumáta og uppgjörsaðferð sem var notaður.</span><span class="sxs-lookup"><span data-stu-id="69435-124">After calculating the statement, there should be lines created with total amounts for each payment method and statement method that was used.</span></span>  
    * <span data-ttu-id="69435-125">Færa inn talda upphæð í hverja línu ef það þarf að færa inn eða uppfæra.</span><span class="sxs-lookup"><span data-stu-id="69435-125">Enter a counted amount in each line if it needs to be entered or updated.</span></span> <span data-ttu-id="69435-126">Talið svæði er fyllt út með upphæðir frá í talning skiptimyntar gert í sölustaður.</span><span class="sxs-lookup"><span data-stu-id="69435-126">The counted field is populated with amounts from tender declarations done in POS.</span></span>  
9. <span data-ttu-id="69435-127">Smellt er á Bóka uppgjör.</span><span class="sxs-lookup"><span data-stu-id="69435-127">Click Post statement.</span></span>
10. <span data-ttu-id="69435-128">Smellið á „Loka“.</span><span class="sxs-lookup"><span data-stu-id="69435-128">Click Close.</span></span>
11. <span data-ttu-id="69435-129">Fara í Smásala og viðskipti > Rásir > Efnahagur smásöluverslunar.</span><span class="sxs-lookup"><span data-stu-id="69435-129">Go to Retail and commerce > Channels > Retail store financials.</span></span>
12. <span data-ttu-id="69435-130">Smellið á flipann Bókað uppgjör.</span><span class="sxs-lookup"><span data-stu-id="69435-130">Click the Posted statements tab.</span></span>


