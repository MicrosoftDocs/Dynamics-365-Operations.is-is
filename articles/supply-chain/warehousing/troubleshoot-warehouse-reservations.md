---
title: Úrræðaleit fyrir frátekningar í vöruhúsastjórnun
description: Í þessu efnisatriði er því lýst hvernig á að laga vandamál sem kunna að koma upp þegar unnið er með vöruhúsafrátektir í Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 6151797001b1ccdb7e371c70b90c304a5ab422d8
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645121"
---
# <a name="troubleshoot-reservations-in-warehouse-management"></a><span data-ttu-id="eebfb-103">Úrræðaleit fyrir frátekningar í vöruhúsastjórnun</span><span class="sxs-lookup"><span data-stu-id="eebfb-103">Troubleshoot reservations in warehouse management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eebfb-104">Í þessu efnisatriði er því lýst hvernig á að laga vandamál sem kunna að koma upp þegar unnið er með vöruhúsafrátektir í Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="eebfb-104">This topic describes how to fix common issues that you might encounter while you work with warehouse reservations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations"></a><span data-ttu-id="eebfb-105">Ég fæ eftirfarandi villuboð: „Ekki er hægt að fjarlægja frátekningar vegna þess að búið er að stofna vinnu sem byggir á frátekningunum.“</span><span class="sxs-lookup"><span data-stu-id="eebfb-105">I receive the following error message: "Reservations cannot be removed because there is work created which relies on the reservations."</span></span>

### <a name="issue-description"></a><span data-ttu-id="eebfb-106">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="eebfb-106">Issue description</span></span>

<span data-ttu-id="eebfb-107">Ekki er hægt að taka frá birgðir á sölulínu, þar sem það er opin vinna á móti línunni.</span><span class="sxs-lookup"><span data-stu-id="eebfb-107">You can't unreserve inventory on a sales line, because there is open work against the line.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="eebfb-108">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="eebfb-108">Issue resolution</span></span>

<span data-ttu-id="eebfb-109">Kanna hvort opin pökkunarhópvinna er til staðar til að koma vörunni úr pökkunarstöð á aðra staðsetningu (t.d. *útskot*).</span><span class="sxs-lookup"><span data-stu-id="eebfb-109">Investigate whether open packing group work exists to bring the item from a packing station to another location (such as *Baydoor*).</span></span> <span data-ttu-id="eebfb-110">Farið yfir færslurnar í **Ferilannál vinnustofnunar** og **Upplýsingar um verk** til að ákvarða hvað er efnislega verið að taka frá í birgðum og ljúka því eða eyða vinnu til að losa frátektina.</span><span class="sxs-lookup"><span data-stu-id="eebfb-110">Review the records on the **Work creation history log** and **Work details** pages to determine what is physically reserving the inventory, and then complete or delete the work to free up the reservation.</span></span>

## <a name="i-receive-the-following-error-message-inventory-quantity--1-could-not-be-updated-due-to-insufficient-inventory-transactions-for-item-2"></a><span data-ttu-id="eebfb-111">Ég fæ eftirfarandi villuboð: „Ekki var hægt að uppfæra birgðamagnið %1 vegna þess að ekki voru nógu margar birgðafærslur fyrir vöruna %2...“</span><span class="sxs-lookup"><span data-stu-id="eebfb-111">I receive the following error message: "Inventory quantity -%1 could not be updated due to insufficient inventory transactions for item %2...."</span></span>

### <a name="issue-description"></a><span data-ttu-id="eebfb-112">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="eebfb-112">Issue description</span></span>

<span data-ttu-id="eebfb-113">Þetta vandamál getur komið upp ef kerfið getur ekki að uppfært birgðamagn vegna þess að það eru ekki nægar birgðafærslur sem eru með tilgreindar stærðir.</span><span class="sxs-lookup"><span data-stu-id="eebfb-113">This issue can occur if the system can't update an inventory quantity because there aren't enough inventory transactions that have the specified dimensions.</span></span> <span data-ttu-id="eebfb-114">Hér er allur texti villuskilaboða:</span><span class="sxs-lookup"><span data-stu-id="eebfb-114">Here is the full text of the full error message:</span></span>

> <span data-ttu-id="eebfb-115">Ekki var hægt að uppfæra birgðamagnið -%1 vegna þess að ekki voru nógu margar birgðafærslur fyrir vöruna %2 með málin Stærð=%3, Litur=%4, Viðbætur=%5, Staður=%6, Vöruhús=%7, Staðsetning=%8, Birgðastaða=Tiltækar, Leyfisplata=%9, Lotunúmer=%10 tilvísunarauðkenni %11 á lotukenni %12.</span><span class="sxs-lookup"><span data-stu-id="eebfb-115">Inventory quantity -%1 could not be updated due to insufficient inventory transactions for item %2 with dimensions Size=%3, Color=%4, Additions=%5, Site=%6, Warehouse=%7, Location=%8, Inventory status=Available, License plate=%9, Batch number=%10 for reference ID %11 on Lot ID %12.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="eebfb-116">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="eebfb-116">Issue resolution</span></span>

<span data-ttu-id="eebfb-117">Ganga skal úr skugga um að engar birgðafærslur séu efnislega í frátekt á móti magninu.</span><span class="sxs-lookup"><span data-stu-id="eebfb-117">Make sure that no inventory transactions are physically reserving the quantity.</span></span> <span data-ttu-id="eebfb-118">Til dæmis gætu þessar færslur opnað gæðapantanir, birgðalokunarfærslur eða úttakspantanir.</span><span class="sxs-lookup"><span data-stu-id="eebfb-118">For example, these transactions might open quality orders, inventory blocking records, or output orders.</span></span>

## <a name="i-receive-the-following-error-message-physical-on-handcannot-be-reserved-because-only-000-are-available-in-the-inventory"></a><span data-ttu-id="eebfb-119">Ég fæ eftirfarandi villuboð: „Efnislega á lager... Ekki er hægt að taka frá vegna þess að aðeins 0,00 eru tiltæk í birgðum.“</span><span class="sxs-lookup"><span data-stu-id="eebfb-119">I receive the following error message: "Physical on-hand...cannot be reserved because only 0.00 are available in the inventory."</span></span>

### <a name="issue-description"></a><span data-ttu-id="eebfb-120">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="eebfb-120">Issue description</span></span>

<span data-ttu-id="eebfb-121">Þetta vandamál getur komið upp ef kerfið getur ekki að uppfært birgðamagn vegna þess að það eru ekki nægar birgðafærslur sem eru með tilgreindar stærðir.</span><span class="sxs-lookup"><span data-stu-id="eebfb-121">This issue can occur if the system can't update an inventory quantity because there aren't enough inventory transactions that have the specified dimensions.</span></span> <span data-ttu-id="eebfb-122">Hér er allur texti villuskilaboða:</span><span class="sxs-lookup"><span data-stu-id="eebfb-122">Here is the full text of the full error message:</span></span>

> <span data-ttu-id="eebfb-123">Efnislegt lagersvæði =%1, Vöruhús=%2, Birgðastaða =Tiltækt, Rununúmer=%3, Eigandi=%4: %5 er ekki hægt að taka frá vegna þess að aðeins 0,00 eru tiltæk í birgðum.</span><span class="sxs-lookup"><span data-stu-id="eebfb-123">Physical on-hand Site=%1, Warehouse=%2, Inventory status=Available, Batch number=%3, Owner=%4: %5 cannot be reserved because only 0.00 are available in the inventory.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="eebfb-124">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="eebfb-124">Issue resolution</span></span>

<span data-ttu-id="eebfb-125">Þetta vandamál stafar líklega af opinni vinnu.</span><span class="sxs-lookup"><span data-stu-id="eebfb-125">This issue is probably caused by open work.</span></span> <span data-ttu-id="eebfb-126">Annaðhvort skal ljúka vinnu eða taka við án þess að stofna vinnu.</span><span class="sxs-lookup"><span data-stu-id="eebfb-126">Either complete the work or receive without work creation.</span></span> <span data-ttu-id="eebfb-127">Ganga skal úr skugga um að engar birgðafærslur séu efnislega í frátekt á móti magninu.</span><span class="sxs-lookup"><span data-stu-id="eebfb-127">Make sure that no inventory transactions are physically reserving the quantity.</span></span> <span data-ttu-id="eebfb-128">Til dæmis gætu þessar færslur verið opnar gæðapantanir, birgðalokunarfærslur eða úttakspantanir.</span><span class="sxs-lookup"><span data-stu-id="eebfb-128">For example, these transactions might be open quality orders, inventory blocking records, or output orders.</span></span>

## <a name="i-receive-the-following-error-message-to-be-assigned-to-wave-load-lines-must-specify-the-dimensions-above-the-location-to-assign-these-dimensions-reserve-and-recreate-the-load-line"></a><span data-ttu-id="eebfb-129">Ég fæ eftirfarandi villuboð: „Til að úthluta bylgju verða hleðslulínur að tilgreina víddirnar fyrir ofan staðsetninguna.</span><span class="sxs-lookup"><span data-stu-id="eebfb-129">I receive the following error message: "To be assigned to wave, load lines must specify the dimensions above the location.</span></span> <span data-ttu-id="eebfb-130">Til að úthluta þessum víddum skal taka hleðslulínuna frá og endurgera hana.“</span><span class="sxs-lookup"><span data-stu-id="eebfb-130">To assign these dimensions, reserve and recreate the load line."</span></span>

### <a name="issue-description"></a><span data-ttu-id="eebfb-131">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="eebfb-131">Issue description</span></span>

<span data-ttu-id="eebfb-132">Þegar vara með "runu fyrir ofan" frátekningarstigveldi er notuð (með **rununúmeri** vídd sem er sett *fyrir ofan* vídd **staðsetningar**) mun skipunin **Losa í vöruhús** á síðunni **Áætlunarvinnusvæði** fyrir hlutamagn ekki virka.</span><span class="sxs-lookup"><span data-stu-id="eebfb-132">When you use an item that has a "batch above" reservation hierarchy (with the **Batch number** dimension placed *above* the **Location** dimension), the **Release to warehouse** command on the **Load planning workbench** page for a partial quantity doesn't work.</span></span> <span data-ttu-id="eebfb-133">Þessi villuskilaboð berast og engin vinna er stofnuð fyrir hlutamagnið.</span><span class="sxs-lookup"><span data-stu-id="eebfb-133">You receive this error message, and no work is created for the partial quantity.</span></span>

<span data-ttu-id="eebfb-134">Hins vegar, ef notuð er vara sem inniheldur "runu fyrir neðan" frátekningarstigveldi (með **Rununúmer** vídd sem er sett fyrir *neðan* vídd **Staðsetning**), er hægt að losa úr síðunni **Áætlunarvinnusvæði** fyrir hlutamagn.</span><span class="sxs-lookup"><span data-stu-id="eebfb-134">However, if you use an item that has a "batch below" reservation hierarchy (with the **Batch number** dimension placed *below* the **Location** dimension), you can release a load from the **Load planning workbench** page for a partial quantity.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="eebfb-135">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="eebfb-135">Issue resolution</span></span>

<span data-ttu-id="eebfb-136">Þessi hegðun er samkvæmt hönnuninni.</span><span class="sxs-lookup"><span data-stu-id="eebfb-136">This behavior is by design.</span></span> <span data-ttu-id="eebfb-137">Ef vídd fyrir ofan víddina **Staðsetning** er sett upp í frátekningarstigveldi verður að tilgreina hana áður en hún er losuð í vöruhúsið.</span><span class="sxs-lookup"><span data-stu-id="eebfb-137">If you put a dimension above the **Location** dimension in the reservation hierarchy, it must be specified before the release to the warehouse.</span></span> <span data-ttu-id="eebfb-138">Microsoft hefur metið þetta vandamál og hefur ákvarðað að takmörkun á eiginleika við losanir í vöruhúsi frá áætlunarvinnusvæði hleðsluáætlunar sé til staðar.</span><span class="sxs-lookup"><span data-stu-id="eebfb-138">Microsoft has evaluated this issue and has determined that it's a feature limitation during releases to the warehouse from the load planning workbench.</span></span> <span data-ttu-id="eebfb-139">Ekki er hægt að losa hlutamagn ef ein eða fleiri vídd fyrir ofan **Staðsetning** eru ekki tilgreindar.</span><span class="sxs-lookup"><span data-stu-id="eebfb-139">Partial quantities can't be released if one or more dimensions above **Location** aren't specified.</span></span>

<span data-ttu-id="eebfb-140">Frekari upplýsingar er að finna í [Sveigjanleg frátektarregla á vídd vöruhúsastigs](flexible-warehouse-level-dimension-reservation.md).</span><span class="sxs-lookup"><span data-stu-id="eebfb-140">For more information, see [Flexible warehouse-level dimension reservation policy](flexible-warehouse-level-dimension-reservation.md).</span></span>
