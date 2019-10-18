---
title: Búa til og uppfæra afgreiðslutíma verslunar
description: Þetta efni lýsir því hvernig á að búa til og uppfæra verslunartíma í höfuðstöðvum verslunarinnar.
author: josaw1
manager: AnnBe
ms.date: 7/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Retail 10.0.1 update
ms.openlocfilehash: 811d499a3eb8133e5ffd29bb4ae6a0c57708accd
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/24/2019
ms.locfileid: "2023443"
---
# <a name="create-and-update-store-hours"></a><span data-ttu-id="5eb7d-103">Búa til og uppfæra afgreiðslutíma verslunar</span><span class="sxs-lookup"><span data-stu-id="5eb7d-103">Create and update store hours</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="5eb7d-104">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="5eb7d-104">Overview</span></span>

<span data-ttu-id="5eb7d-105">Frá einum stað geta smásalar stofnað, viðhaldið og stjórnað verslunarstundum fyrir mismunandi verslanir á landsvæðum.</span><span class="sxs-lookup"><span data-stu-id="5eb7d-105">From a single place, retailers can create, maintain, and manage the store hours for different stores across geographic regions.</span></span> <span data-ttu-id="5eb7d-106">Þá er hægt að sýna verslunartímann á afgreiðslukössum.</span><span class="sxs-lookup"><span data-stu-id="5eb7d-106">The store hours can then be shown on point of sale (POS) terminals.</span></span> <span data-ttu-id="5eb7d-107">Á þennan hátt geta gjaldkerar deilt verslunartímum með viðskiptavinum og veitt betri þjónustu þeim kaupendum sem hafa áhuga á birgðum í öðrum verslunum.</span><span class="sxs-lookup"><span data-stu-id="5eb7d-107">In this way, cashiers can share store hours with customers and better help shoppers who are interested in inventory in other stores.</span></span> <span data-ttu-id="5eb7d-108">Einnig er hægt að prenta út verslunartímann á kvittunum, ef viðskiptavinir vilja fara aftur í búðina seinna.</span><span class="sxs-lookup"><span data-stu-id="5eb7d-108">The store hours can also be printed on receipts, in case customers want to return to the store later.</span></span>

<span data-ttu-id="5eb7d-109">Hægt er að stilla marga verslunartíma á mismunandi rásum.</span><span class="sxs-lookup"><span data-stu-id="5eb7d-109">Multiple store hours can be configured across different channels.</span></span> <span data-ttu-id="5eb7d-110">Þessar rásir innihalda verslanir á staðnum, símaver, farsíma og netverslunarsíður.</span><span class="sxs-lookup"><span data-stu-id="5eb7d-110">These channels include brick-and-mortar stores, call centers, mobile devices, and e-Commerce sites.</span></span>

<span data-ttu-id="5eb7d-111">Ef viðskiptavinur er með tínslupöntun fyrir aðra verslun getur gjaldkerinn valið dagsetningar þegar tínslan verður tiltæk í þeirri verslun.</span><span class="sxs-lookup"><span data-stu-id="5eb7d-111">If a customer has a pickup order for a different store, the cashier can select dates when the pickup will be available in that store.</span></span> <span data-ttu-id="5eb7d-112">Uppfletting verslunarinnar mun veita tilvísun í dagsetningar og tíma verslana.</span><span class="sxs-lookup"><span data-stu-id="5eb7d-112">The store lookup will provide a reference to the dates and store times.</span></span> <span data-ttu-id="5eb7d-113">Gjaldkeri getur valið dagsetningu og staðsetningu og getur einnig prentað afhendingarkvittun sem felur í sér opnunartíma verslunarinnar.</span><span class="sxs-lookup"><span data-stu-id="5eb7d-113">The cashier can select a date and location, and can also print a pickup receipt that includes the store hours.</span></span>

<span data-ttu-id="5eb7d-114">Þessi aðgerð er fáanleg í Microsoft Dynamics 365 Retail útgáfum 8.1.2 og nýrri.</span><span class="sxs-lookup"><span data-stu-id="5eb7d-114">This functionality is available in Microsoft Dynamics 365 Retail versions 8.1.2 and later.</span></span>

## <a name="configure-store-hours"></a><span data-ttu-id="5eb7d-115">Skilgreina afgreiðslutíma</span><span class="sxs-lookup"><span data-stu-id="5eb7d-115">Configure store hours</span></span>

<span data-ttu-id="5eb7d-116">Fylgja skal þessum skrefum til að skilgreina afgreiðslutíma.</span><span class="sxs-lookup"><span data-stu-id="5eb7d-116">Follow these steps to configure store hours.</span></span>

1. <span data-ttu-id="5eb7d-117">Opnið **Retail** \> **Uppsetning rásar** \> **Afgreiðslutímar**.</span><span class="sxs-lookup"><span data-stu-id="5eb7d-117">Go to **Retail** \> **Channel Setup** \> **Store hours**.</span></span>
2. <span data-ttu-id="5eb7d-118">Veldu **Nýtt** til að búa til nýtt sniðmát afgreiðslutíma.</span><span class="sxs-lookup"><span data-stu-id="5eb7d-118">Select **New** to create a new store hours template.</span></span> <span data-ttu-id="5eb7d-119">Veldu sniðmátið í vinstri glugganum til að nota sniðmát sem fyrir er.</span><span class="sxs-lookup"><span data-stu-id="5eb7d-119">To use an existing template, select the template in the left pane.</span></span>
3. <span data-ttu-id="5eb7d-120">Í glugganum **Bæta við sviði** skaltu tilgreina tímabilið, afgreiðslutímann og alla frídaga sem þarf.</span><span class="sxs-lookup"><span data-stu-id="5eb7d-120">In the **Add range** dialog box, define the date range, the store hours, and any holidays that are required.</span></span>

    - <span data-ttu-id="5eb7d-121">Ef afgreiðslutími breytist ekki skaltu velja **Lýkur aldrei** í reitnum **Lokadagsetning**.</span><span class="sxs-lookup"><span data-stu-id="5eb7d-121">If store hours don't change, select **Never ends** in the **End date** field.</span></span>
    - <span data-ttu-id="5eb7d-122">Ef afgreiðslutíminn er fyrir tiltekinn mánuð, viku eða dag, stillirðu viðeigandi dagsetningar í reitunum **Upphafsdagur** og **Lokadagsetning**.</span><span class="sxs-lookup"><span data-stu-id="5eb7d-122">If the store hours are for a specific month, week, or day, set the appropriate dates in the **Start Date** and **End date** fields.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5eb7d-123">Þú getur búið til mörg sniðmát sem hafa skarandi upphafs- og lokadagsetningar.</span><span class="sxs-lookup"><span data-stu-id="5eb7d-123">You can create multiple templates that have overlapping start and end dates.</span></span> <span data-ttu-id="5eb7d-124">Þess vegna getur þú til dæmis skilgreint afgreiðslutíma fyrir verslanir á mismunandi tímabeltum.</span><span class="sxs-lookup"><span data-stu-id="5eb7d-124">Therefore, you can, for example, define store hours for stores in different time zones.</span></span>

    <span data-ttu-id="5eb7d-125">![Bæta við sviðsglugga](../dev-itpro/media/Storehours1.png "Bæta við sviðsglugga")</span><span class="sxs-lookup"><span data-stu-id="5eb7d-125">![Add range dialog box](../dev-itpro/media/Storehours1.png "Add range dialog box")</span></span>

4. <span data-ttu-id="5eb7d-126">Tengdu sniðmát afgreiðslutíma við verslanirnar þar sem það verður notað.</span><span class="sxs-lookup"><span data-stu-id="5eb7d-126">Associate the store hours template with the stores where it will be used.</span></span> <span data-ttu-id="5eb7d-127">Í glugganum **Velja fyrirtækjahnúta** velurðu verslanir, svæði og fyrirtæki sem sniðmátið ætti að vera tengt við.</span><span class="sxs-lookup"><span data-stu-id="5eb7d-127">In the **Choose organization nodes** dialog box, select the stores, regions, and organizations that the template should be associated with.</span></span>

    - <span data-ttu-id="5eb7d-128">Aðeins er hægt að tengja eitt sniðmát afgreiðslutíma við hverja verslun.</span><span class="sxs-lookup"><span data-stu-id="5eb7d-128">Only one store hours template can be associated with each store.</span></span>
    - <span data-ttu-id="5eb7d-129">Notaðu örvahnappana til að velja verslanir, svæði eða fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="5eb7d-129">Use the arrow buttons to select stores, regions, or organizations.</span></span> <span data-ttu-id="5eb7d-130">Dagatalið verður aðgengilegt í verslunum eða verslunarhópum og það verður sýnilegt á sölustað til viðmiðunar.</span><span class="sxs-lookup"><span data-stu-id="5eb7d-130">The calendar will be available to the stores or store groups, and it will be visible at the POS for reference.</span></span>

    <span data-ttu-id="5eb7d-131">![Glugginn Veljið fyrirtækjahnúta](../dev-itpro/media/Storehours2.png "Glugginn Veljið fyrirtækjahnúta")</span><span class="sxs-lookup"><span data-stu-id="5eb7d-131">![Choose organization nodes dialog box](../dev-itpro/media/Storehours2.png "Choose organization nodes dialog box")</span></span>

5. <span data-ttu-id="5eb7d-132">Á síðunni **Dreifingaráætlun** keyrirðu vinnslurnar **1070** og **1090** til að gera verslunartímann aðgengilegan sölustað.</span><span class="sxs-lookup"><span data-stu-id="5eb7d-132">On the **Distribution schedule** page, run the **1070** and **1090** jobs to make the store hours available to the POS.</span></span>

## <a name="add-store-hours-to-printed-receipts"></a><span data-ttu-id="5eb7d-133">Bættu afgreiðslutímum við prentaðar kvittanir</span><span class="sxs-lookup"><span data-stu-id="5eb7d-133">Add store hours to printed receipts</span></span>

<span data-ttu-id="5eb7d-134">Fylgdu þessum skrefum til að bæta afgreiðslutíma við prentuðu POS kvittanir.</span><span class="sxs-lookup"><span data-stu-id="5eb7d-134">Follow these steps to add store hours to the printed POS receipts.</span></span>

1. <span data-ttu-id="5eb7d-135">Opnaðu hönnuð kvittunar.</span><span class="sxs-lookup"><span data-stu-id="5eb7d-135">Open the receipt designer.</span></span>
2. <span data-ttu-id="5eb7d-136">Veldu **Fótur** í neðra vinstra horninu.</span><span class="sxs-lookup"><span data-stu-id="5eb7d-136">Select **Footer** in the lower-left corner.</span></span>
3. <span data-ttu-id="5eb7d-137">Dragðu einguna **Afgreiðslutími** úr vinstri glugganum að fætinum neðst á kvittunarsniðmátinu.</span><span class="sxs-lookup"><span data-stu-id="5eb7d-137">Drag the **Store hours** element from the left pane to the footer at the bottom of the receipt template.</span></span>
4. <span data-ttu-id="5eb7d-138">Þú getur breytt sjálfgefna merkimiðanum á eingunni **Afgreiðslutími** eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="5eb7d-138">You can edit the default label on the **Store hours** element as you require.</span></span>
5. <span data-ttu-id="5eb7d-139">Vistaðu kvittunina og lokaðu kvittunarhönnuðinum.</span><span class="sxs-lookup"><span data-stu-id="5eb7d-139">Save the receipt, and close the receipt designer.</span></span>
6. <span data-ttu-id="5eb7d-140">Á síðunni **Dreifingaráætlun** skaltu keyra vinnslurnar **1070** og **1090**.</span><span class="sxs-lookup"><span data-stu-id="5eb7d-140">On the **Distribution schedule** page, run the **1070** and **1090** jobs.</span></span>
7. <span data-ttu-id="5eb7d-141">Skráðu þig inn POS</span><span class="sxs-lookup"><span data-stu-id="5eb7d-141">Sign in to the POS.</span></span>
8. <span data-ttu-id="5eb7d-142">Ljúktu við sölu og veldu að prenta kvittun.</span><span class="sxs-lookup"><span data-stu-id="5eb7d-142">Complete a sale, and select to print a receipt.</span></span>

<span data-ttu-id="5eb7d-143">Kvittanir á sölustað innihalda nú afgreiðslutímann.</span><span class="sxs-lookup"><span data-stu-id="5eb7d-143">POS receipts now include the store hours.</span></span> <span data-ttu-id="5eb7d-144">Ef einhverjir frídagar voru með í sniðmátinu eru þeir sýndir á kvittuninni.</span><span class="sxs-lookup"><span data-stu-id="5eb7d-144">If any holidays were included in the template, they are shown on the receipt.</span></span>

<span data-ttu-id="5eb7d-145">![Kvittunardæmi](../dev-itpro/media/Storehours3.png "Kvittunardæmi")</span><span class="sxs-lookup"><span data-stu-id="5eb7d-145">![Receipt example](../dev-itpro/media/Storehours3.png "Receipt example")</span></span>
