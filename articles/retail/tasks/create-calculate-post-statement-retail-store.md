--- 
title: " Búa til, reikna og bóka yfirlit fyrir smásöluverslun"
description: "Þetta ferli fer í gegnum handvirkar skref til að stofna, reikna út og bóka uppgjör fyrir verslun."
author: jashanno
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: RetailChannelOperationsWorkspace, RetailStatementTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: d949cf46857992d5f16d349862ff67cccf417fed
ms.contentlocale: is-is
ms.lasthandoff: 09/11/2018

---
# <a name="create-calculate-and-post-a-statement-for-a-retail-store"></a><span data-ttu-id="b0ff3-103"> Búa til, reikna og bóka yfirlit fyrir smásöluverslun</span><span class="sxs-lookup"><span data-stu-id="b0ff3-103">Create, calculate, and post a statement for a retail store</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="b0ff3-104">Þetta ferli fer í gegnum handvirkar skref til að stofna, reikna út og bóka uppgjör fyrir verslun.</span><span class="sxs-lookup"><span data-stu-id="b0ff3-104">This procedure walks through the manual steps for creating, calculating, and posting a statement for a store.</span></span> <span data-ttu-id="b0ff3-105">Einnig eru runuvinnslur sem hægt er að skilgreina fyrir sama verk.</span><span class="sxs-lookup"><span data-stu-id="b0ff3-105">There are also batch jobs that can be configured for the same tasks.</span></span> <span data-ttu-id="b0ff3-106">Skrefin til að skilgreina og keyra sem runuvinnslur er að finna í öðrum efnisatriði.</span><span class="sxs-lookup"><span data-stu-id="b0ff3-106">The steps for configuring and running the batch jobs can be found in other topics.</span></span> <span data-ttu-id="b0ff3-107">Til að ljúka þessu ferli, verður að hafa færslur sem voru fylltir út í sölustaður og síðan dregin inn í Dynamics AX.</span><span class="sxs-lookup"><span data-stu-id="b0ff3-107">To complete this procedure, you must have transactions that were completed in POS and then pulled into Dynamics AX.</span></span> <span data-ttu-id="b0ff3-108">Þessi skráning notar sýnigögn fyrirtæki USRT .</span><span class="sxs-lookup"><span data-stu-id="b0ff3-108">This recording uses the USRT company in demo data.</span></span> <span data-ttu-id="b0ff3-109">Þetta ferli gæti vísað til Microsoft Dynamics AX.</span><span class="sxs-lookup"><span data-stu-id="b0ff3-109">This procedure may refer to Microsoft Dynamics AX.</span></span> <span data-ttu-id="b0ff3-110">Athugaðu að Dynamics AX er nú kallað Microsoft Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="b0ff3-110">Please note that Dynamics AX is now called Microsoft Dynamics 365 for Operations.</span></span>

1. <span data-ttu-id="b0ff3-111">Fara í Öll vinnusvæði > ..</span><span class="sxs-lookup"><span data-stu-id="b0ff3-111">Go to All workspaces > ..</span></span> <span data-ttu-id="b0ff3-112">> Fjárhagur smásöluverslunar</span><span class="sxs-lookup"><span data-stu-id="b0ff3-112">> Retail store financials.</span></span>
2. <span data-ttu-id="b0ff3-113">Smella á Nýtt uppgjör.</span><span class="sxs-lookup"><span data-stu-id="b0ff3-113">Click New statement.</span></span>
3. <span data-ttu-id="b0ff3-114">Í reitnum verslunarnúmer skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="b0ff3-114">In the Store number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="b0ff3-115">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="b0ff3-115">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="b0ff3-116">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="b0ff3-116">Click OK.</span></span>
    * <span data-ttu-id="b0ff3-117">Uppsetning flokka hefur stillingarnar sem stýra hvaða færslur eru teknar með í uppgjörinu og hvernig þau eru flokkuð í uppgjörslínunum.</span><span class="sxs-lookup"><span data-stu-id="b0ff3-117">The Setup group has the settings that control what transactions are included in the statement and how they are grouped into statement lines.</span></span> <span data-ttu-id="b0ff3-118">Hægt er að opna Uppsetningu flokka og breyta þessum stillingum, eða hægt er að nota sem sjálfgildi.</span><span class="sxs-lookup"><span data-stu-id="b0ff3-118">You can open the Setup group and change these settings, or you can use the defaults.</span></span>  
    * <span data-ttu-id="b0ff3-119">svæðið uppgjörsaðferð skilgreinir hvernig uppgjörslínurnar verða flokkaðar.</span><span class="sxs-lookup"><span data-stu-id="b0ff3-119">The Statement method field defines how the statement lines will be grouped.</span></span>  
    * <span data-ttu-id="b0ff3-120">Veljið afgreiðslukassa eða starfsmaður eigi að reikna uppgjör aðeins fyrir tiltekinn starfsmaður eða afgreiðslukassa.</span><span class="sxs-lookup"><span data-stu-id="b0ff3-120">Select a staff member or a register if you want to calculate a statement only for the specific staff member or register.</span></span>  
6. <span data-ttu-id="b0ff3-121">Í reitnum lokunaraðferð skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="b0ff3-121">In the Closing method field, select an option.</span></span>
7. <span data-ttu-id="b0ff3-122">Smellt er á Reikna út uppgjör.</span><span class="sxs-lookup"><span data-stu-id="b0ff3-122">Click Calculate statement.</span></span>
8. <span data-ttu-id="b0ff3-123">Smella á Já.</span><span class="sxs-lookup"><span data-stu-id="b0ff3-123">Click Yes.</span></span>
    * <span data-ttu-id="b0ff3-124">Eftir að reikna uppgjör, ætti að vera eru stofnaðar línur með heildarupphæðir fyrir hvern greiðslumáta og uppgjörsaðferð sem var notaður.</span><span class="sxs-lookup"><span data-stu-id="b0ff3-124">After calculating the statement, there should be lines created with total amounts for each payment method and statement method that was used.</span></span>  
    * <span data-ttu-id="b0ff3-125">Færa inn talda upphæð í hverja línu ef það þarf að færa inn eða uppfæra.</span><span class="sxs-lookup"><span data-stu-id="b0ff3-125">Enter a counted amount in each line if it needs to be entered or updated.</span></span> <span data-ttu-id="b0ff3-126">Talið svæði er fyllt út með upphæðir frá í talning skiptimyntar gert í sölustaður.</span><span class="sxs-lookup"><span data-stu-id="b0ff3-126">The counted field is populated with amounts from tender declarations done in POS.</span></span>  
9. <span data-ttu-id="b0ff3-127">Smellt er á Bóka uppgjör.</span><span class="sxs-lookup"><span data-stu-id="b0ff3-127">Click Post statement.</span></span>
10. <span data-ttu-id="b0ff3-128">Smellið á „Loka“.</span><span class="sxs-lookup"><span data-stu-id="b0ff3-128">Click Close.</span></span>
11. <span data-ttu-id="b0ff3-129">Fara í Smásala og viðskipti > Rásir > Efnahagur smásöluverslunar.</span><span class="sxs-lookup"><span data-stu-id="b0ff3-129">Go to Retail and commerce > Channels > Retail store financials.</span></span>
12. <span data-ttu-id="b0ff3-130">Smellið á flipann Bókað uppgjör.</span><span class="sxs-lookup"><span data-stu-id="b0ff3-130">Click the Posted statements tab.</span></span>


