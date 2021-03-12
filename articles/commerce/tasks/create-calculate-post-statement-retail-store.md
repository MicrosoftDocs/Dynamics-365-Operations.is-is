---
title: Stofna, reikna og bóka yfirlit fyrir smásöluverslun
description: Þetta efni lýsir handvirkum skrefum fyrir stofnun, útreikning og bókun á uppgjöri fyrir verslun.
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailStatementTable
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0ef31bc02fe1761a587ff6bcbecf4a0f34daea9b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4964871"
---
# <a name="create-calculate-and-post-statements-for-a-retail-store"></a><span data-ttu-id="09949-103">Stofna, reikna og bóka yfirlit fyrir smásöluverslun</span><span class="sxs-lookup"><span data-stu-id="09949-103">Create, calculate, and post statements for a retail store</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="09949-104">Þetta efni lýsir handvirkum skrefum fyrir stofnun, útreikning og bókun á uppgjöri fyrir verslun.</span><span class="sxs-lookup"><span data-stu-id="09949-104">This topic describes the manual steps for creating, calculating, and posting a statement for a store.</span></span> <span data-ttu-id="09949-105">Einnig eru runuvinnslur sem hægt er að skilgreina fyrir sama verk.</span><span class="sxs-lookup"><span data-stu-id="09949-105">There are also batch jobs that can be configured for the same tasks.</span></span> <span data-ttu-id="09949-106">Skrefin til að skilgreina og keyra sem runuvinnslur er að finna í öðrum efnisatriði.</span><span class="sxs-lookup"><span data-stu-id="09949-106">The steps for configuring and running the batch jobs can be found in other topics.</span></span> <span data-ttu-id="09949-107">Til að ljúka þessu ferli, verður að hafa færslur sem voru fylltir út á sölustað og draga þær síðan inn í Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="09949-107">To complete this procedure, you must have transactions that were completed in POS and then pulled into Dynamics 365 Commerce.</span></span> <span data-ttu-id="09949-108">Þessi skráning notar sýnigögn fyrirtæki USRT .</span><span class="sxs-lookup"><span data-stu-id="09949-108">This recording uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="09949-109">Veldu **Fjárhagur verslunar** af heimasíðunni.</span><span class="sxs-lookup"><span data-stu-id="09949-109">Select **Store financials** from the home page.</span></span>
2. <span data-ttu-id="09949-110">Veldu **Nýtt yfirlit**.</span><span class="sxs-lookup"><span data-stu-id="09949-110">Select **New statement**.</span></span>
3. <span data-ttu-id="09949-111">Í reitnum **Verslunarnúmer** reitinn velurðu valkost úr fellivalmyndinni.</span><span class="sxs-lookup"><span data-stu-id="09949-111">In the **Store number** field, select a option from the drop-down.</span></span>
4. <span data-ttu-id="09949-112">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="09949-112">Select **OK**.</span></span>
5. <span data-ttu-id="09949-113">Hópurinn **Uppsetning** hefur stillingarnar sem stýra hvaða færslur eru teknar með í uppgjörinu og hvernig þau eru flokkuð í uppgjörslínunum.</span><span class="sxs-lookup"><span data-stu-id="09949-113">The **Setup** group has the settings that control what transactions are included in the statement and how they are grouped into statement lines.</span></span> <span data-ttu-id="09949-114">Hægt er að opna hópinn **Uppsetningu** og breyta þessum stillingum, eða hægt er að nota sem sjálfgildi.</span><span class="sxs-lookup"><span data-stu-id="09949-114">You can open the **Setup** group and change these settings, or you can use the defaults.</span></span>  
    - <span data-ttu-id="09949-115">Reiturinn **uppgjörsaðferð** skilgreinir hvernig uppgjörslínurnar verða flokkaðar.</span><span class="sxs-lookup"><span data-stu-id="09949-115">The **Statement method** field defines how the statement lines will be grouped.</span></span>  
    - <span data-ttu-id="09949-116">Veljið starfsmann eða afgreiðslukassa í reitnum **Starfsmaður/afgreiðslukassi** ef þú vilt reikna uppgjör aðeins fyrir tiltekinn starfsmann eða afgreiðslukassa.</span><span class="sxs-lookup"><span data-stu-id="09949-116">Select a staff member or a register in the **staff/register** field if you want to calculate a statement only for the specific staff member or register.</span></span>  
6. <span data-ttu-id="09949-117">Í reitnum **Lokunaraðferð** skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="09949-117">In the **Closing method** field, select an option.</span></span>
7. <span data-ttu-id="09949-118">Veldu **Reikna uppgjör** úr aðgerðarglugganum.</span><span class="sxs-lookup"><span data-stu-id="09949-118">Select **Calculate statement** from the Action Pane.</span></span>
8. <span data-ttu-id="09949-119">Velja skal **Já**.</span><span class="sxs-lookup"><span data-stu-id="09949-119">Select **Yes**.</span></span>
    - <span data-ttu-id="09949-120">Eftir að reikna uppgjör, ætti að vera eru stofnaðar línur með heildarupphæðir fyrir hvern greiðslumáta og uppgjörsaðferð sem var notaður.</span><span class="sxs-lookup"><span data-stu-id="09949-120">After calculating the statement, there should be lines created with total amounts for each payment method and statement method that was used.</span></span>  
    - <span data-ttu-id="09949-121">Færa inn talda upphæð í hverja línu ef það þarf að færa inn eða uppfæra.</span><span class="sxs-lookup"><span data-stu-id="09949-121">Enter a counted amount in each line if it needs to be entered or updated.</span></span> <span data-ttu-id="09949-122">Talið svæði er fyllt út með upphæðir frá í talning skiptimyntar gert í sölustaður.</span><span class="sxs-lookup"><span data-stu-id="09949-122">The counted field is populated with amounts from tender declarations done in POS.</span></span>  
9. <span data-ttu-id="09949-123">Veldu **Bóka uppgjör** úr aðgerðarglugganum.</span><span class="sxs-lookup"><span data-stu-id="09949-123">Select **Post statement** from the Action Pane.</span></span>
10. <span data-ttu-id="09949-124">Veljið **Loka**.</span><span class="sxs-lookup"><span data-stu-id="09949-124">Select **Close**.</span></span>
11. <span data-ttu-id="09949-125">Lokið glugganum.</span><span class="sxs-lookup"><span data-stu-id="09949-125">Close the pane.</span></span>
12. <span data-ttu-id="09949-126">Á heimasíðunni velurðu **Fjárhagur verslunar**.</span><span class="sxs-lookup"><span data-stu-id="09949-126">At the home page, select **Store financials**.</span></span>
13. <span data-ttu-id="09949-127">Veldu flipann **Bókuð uppgjör**.</span><span class="sxs-lookup"><span data-stu-id="09949-127">Select the **Posted statements** tab.</span></span>

