---
title: Eignamælingar
description: Umræðuefnið útskýrir hvernig á að stofna eignamælingar í eignastýringu.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9c445832a649c4f6a6642036ecab325e8aa2079
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783357"
---
# <a name="asset-measures"></a><span data-ttu-id="cad31-103">Eignamælingar</span><span class="sxs-lookup"><span data-stu-id="cad31-103">Asset measures</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="cad31-104">Umræðuefnið útskýrir hvernig á að stofna eignamælingar í eignastýringu.</span><span class="sxs-lookup"><span data-stu-id="cad31-104">The topic explains how to create asset measure types in Asset Management.</span></span> <span data-ttu-id="cad31-105">Gerðir eignamælinga eru notaðar til að skrá mælingar á eignir, til dæmis varðandi fjölda framleiðslutíma eða magn framleitt á eigninni.</span><span class="sxs-lookup"><span data-stu-id="cad31-105">Asset measure types are used to make measurement registrations on assets, for example, regarding number of production hours, or quantity produced on the asset.</span></span> <span data-ttu-id="cad31-106">Tegundir eigna eru tengdar tegundum eignamats.</span><span class="sxs-lookup"><span data-stu-id="cad31-106">Asset types are related to the asset measure types.</span></span> <span data-ttu-id="cad31-107">Þetta þýðir að einungis er hægt að nota eignamæli á eign ef eignamælingin er sett upp á eignategundinni sem notuð er á eigninni.</span><span class="sxs-lookup"><span data-stu-id="cad31-107">This means that an asset measure can only be used on an asset if the asset measure is set up on the asset type used on the asset.</span></span>

<span data-ttu-id="cad31-108">Áður en þú getur gert skráningar á eignir þarf fyrst að stofna þær tegundir eigna sem þú vilt nota í **Teljendur**.</span><span class="sxs-lookup"><span data-stu-id="cad31-108">Before you can make measurement registrations on assets, you first create the asset measure types you want to use in **Counters**.</span></span> <span data-ttu-id="cad31-109">Næst geturðu búið til skráningar á eignum í **Eignamælingar**.</span><span class="sxs-lookup"><span data-stu-id="cad31-109">Next, you can create measurement registrations on assets in **Asset measures**.</span></span> 

<span data-ttu-id="cad31-110">Hægt er að nota eignir í viðhaldsáætlunum.</span><span class="sxs-lookup"><span data-stu-id="cad31-110">Asset measures can be used on maintenance plans.</span></span> <span data-ttu-id="cad31-111">Viðhaldsáætlunarlína getur verið af gerðinni „Teljari“, til dæmis varðandi fjölda framleiðslutíma eða framleitt magn.</span><span class="sxs-lookup"><span data-stu-id="cad31-111">A maintenance plan line can be of type "Counter", for example, relating to number of production hours or quantity produced.</span></span> 

<span data-ttu-id="cad31-112">Hægt er að uppfæra eignamælingaskráningu handvirkt eða sjálfkrafa út frá framleiðslutíma eða framleiddu magni.</span><span class="sxs-lookup"><span data-stu-id="cad31-112">An asset measurement registration can be updated manually or automatically based on production hours or quantity produced.</span></span> <span data-ttu-id="cad31-113">Hægt er að setja upp eignamæli til að nota eina af þremur uppfærsluaðferðum (valið í reitnum **Uppfæra** í **Teljendur**):</span><span class="sxs-lookup"><span data-stu-id="cad31-113">An asset measure can be set up to use one of three update methods (selected in the **Update** field in **Counters**):</span></span>
  
- <span data-ttu-id="cad31-114">Handvirkt - þú verður að skrá eignamælingargildi handvirkt.</span><span class="sxs-lookup"><span data-stu-id="cad31-114">Manual - you must manually register asset measurement values.</span></span>  
- <span data-ttu-id="cad31-115">Framleiðslutímar - teljarinn er sjálfkrafa uppfærður út frá fjölda framleiðslutíma.</span><span class="sxs-lookup"><span data-stu-id="cad31-115">Production hours - the counter is automatically updated based on number of production hours.</span></span>  
- <span data-ttu-id="cad31-116">Framleiðslumagn - teljarinn er sjálfkrafa uppfærður út frá framleiddu magni.</span><span class="sxs-lookup"><span data-stu-id="cad31-116">Production quantity - the counter is automatically updated based on number of quantity produced.</span></span>  

>[!NOTE]
><span data-ttu-id="cad31-117">Ef framleitt magn er notað eru *allir* skráðir hlutir með í mælingaskráningu, gott magn sem og villumagn.</span><span class="sxs-lookup"><span data-stu-id="cad31-117">If quantity produced is used, *all* registered items are included in the measurement registration, good quantity as well as error quantity.</span></span> <span data-ttu-id="cad31-118">Það er alltaf mögulegt að gera handvirkar skráningar á eignamati, ef þess þarf.</span><span class="sxs-lookup"><span data-stu-id="cad31-118">It is always possible to make manual asset measurement registrations, if required.</span></span>

## <a name="create-counter-types-for-asset-counter-registrations"></a><span data-ttu-id="cad31-119">Búðu til gagnategundir fyrir skráningar eignateljara</span><span class="sxs-lookup"><span data-stu-id="cad31-119">Create counter types for asset counter registrations</span></span>

1. <span data-ttu-id="cad31-120">Veldu **Eignastýring** > **Uppsetning** > **Eignagerðir** > **Teljarar**.</span><span class="sxs-lookup"><span data-stu-id="cad31-120">Select **Asset management** > **Setup** > **Asset types** > **Counters**.</span></span>
2. <span data-ttu-id="cad31-121">Veldu **Nýr** til að stofna nýja gerð eignamælingar.</span><span class="sxs-lookup"><span data-stu-id="cad31-121">Select **New** to create a new asset measure type.</span></span>
3. <span data-ttu-id="cad31-122">Settu inn auðkenni í reitinn **Teljari** og teljaraheiti í reitinn **Heiti**.</span><span class="sxs-lookup"><span data-stu-id="cad31-122">Insert an ID in the **Counter** field, and a counter name in the **Name** field.</span></span>
4. <span data-ttu-id="cad31-123">Á flýtiflipanum **Almennt** velurðu mælieiningu í reitnum **Eining**.</span><span class="sxs-lookup"><span data-stu-id="cad31-123">On the **General** FastTab, select a measurement unit in the **Unit** field.</span></span>
5. <span data-ttu-id="cad31-124">Í retinum **Uppfæra** velurðu uppfærsluaðferðina sem á að nota fyrir eignamælinguna.</span><span class="sxs-lookup"><span data-stu-id="cad31-124">In the **Update** field, select the update method to be used for the asset measure.</span></span>
6. <span data-ttu-id="cad31-125">Veldu „Já“ á skiptihnappnum **Erfa teljaragildi** ef undireignir í eignaskipan ættu sjálfkrafa að erfa eignamælingarskráningar sem gerðar eru á yfireigninni.</span><span class="sxs-lookup"><span data-stu-id="cad31-125">Select "Yes" on the **Inherit counter values** toggle button if child assets in an asset structure should automatically inherit asset measure registrations made on the parent asset.</span></span>
7. <span data-ttu-id="cad31-126">Í retinum **Samtals samanlagt** velurðu samantektaraðferðina sem á að nota fyrir eignamælingu með þessari eignamælingargerð.</span><span class="sxs-lookup"><span data-stu-id="cad31-126">In the **Total aggregate** field, select the summation method to be used for an asset measure using this asset measure type.</span></span> <span data-ttu-id="cad31-127">„Summa“ er staðalvalið sem notað er til að bæta skráðum gildi stöðugt við heildargildið.</span><span class="sxs-lookup"><span data-stu-id="cad31-127">"Sum" is the standard selection used to continuously add registered values to the total value.</span></span> <span data-ttu-id="cad31-128">Hægt er að nota „meðaltal“ ef eignamæling er sett upp til að fylgjast með þröskuldi, til dæmis varðandi hitastig, titring eða slit á eign.</span><span class="sxs-lookup"><span data-stu-id="cad31-128">"Average" can be used if an asset measure is set up to monitor a threshold, for example, regarding temperature, vibrations, or wear and tear on an asset.</span></span> 
8. <span data-ttu-id="cad31-129">Í reitnum **Frávik yfir** seturðu efra stigið inn í prósentu til að sannprófa hvort handvirkar eignaskráningar séu innan áætlaðs sviðs.</span><span class="sxs-lookup"><span data-stu-id="cad31-129">In the **Deviation over** field, insert the upper level in percent for validating if manual asset measure registrations are within an expected range.</span></span> <span data-ttu-id="cad31-130">Sannprófunin er byggð á línulegri aukningu á núverandi eignamælingaskráningum.</span><span class="sxs-lookup"><span data-stu-id="cad31-130">The validation is based on a linear increase in existing asset measure registrations.</span></span>
9. <span data-ttu-id="cad31-131">Í reitnum **Frávik undir** seturðu neðra stigið inn í prósentu til að sannprófa hvort handvirkar eignaskráningar séu innan áætlaðs sviðs.</span><span class="sxs-lookup"><span data-stu-id="cad31-131">In the **Deviation under** field, insert the lower level in percent for validating if manual asset measure registrations are within an expected range.</span></span> <span data-ttu-id="cad31-132">Sannprófunin er byggð á línulegri lækkun á núverandi eignamælingaskráningum.</span><span class="sxs-lookup"><span data-stu-id="cad31-132">The validation is based on a linear decrease in existing asset measure registrations.</span></span>
10. <span data-ttu-id="cad31-133">Í reitnum **Tegund** velurðu gerð skilaboðanna (upplýsingar, viðvörun, villu) sem á að sýna ef frávik utan skilgreinds sviðs eiga sér stað þegar þú gerir handvirkar skráningar á eignamati.</span><span class="sxs-lookup"><span data-stu-id="cad31-133">In the **Type** field, select the type of message (information, warning, error) to be shown if deviations outside the defined range occur when you make manual asset measure registrations.</span></span>
11. <span data-ttu-id="cad31-134">Á flýtiflipanum **Eignagerðir** bætirðu við eignagerðum sem ættu að geta notað eignamælinguna.</span><span class="sxs-lookup"><span data-stu-id="cad31-134">On the **Asset types** FastTab, add the asset types that should be able to use the asset measure.</span></span>
12. <span data-ttu-id="cad31-135">Á flýtiflipanum **Tengdar eignamælingar** bætirðu við eignamælingunum sem þú vilt að uppfærist sjálfkrafa þegar þessi eignamæling er uppfærð.</span><span class="sxs-lookup"><span data-stu-id="cad31-135">On the **Related asset measures** FastTab, add the asset measures that you want to be automatically updated when this asset measure is updated.</span></span>


>[!NOTE]
><span data-ttu-id="cad31-136">Tengd eignamæling er sjálfkrafa uppfærð ef viðkomandi eignamæling hefur eignagerðina sem hún er tengd við í uppsetningu eignaáætlunarinnar.</span><span class="sxs-lookup"><span data-stu-id="cad31-136">A related asset measure is automatically updated only if the related asset measure has the asset type, to which it is related, in the asset measure setup.</span></span> <span data-ttu-id="cad31-137">Til dæmis: Þú setur upp eignamælikvarða fyrir „Framleiðslutíma“ og bætir við eignategundinni „Truck Engine“.</span><span class="sxs-lookup"><span data-stu-id="cad31-137">For example: You set up an asset measure for "Production hours" and add the asset type "Truck Engine".</span></span> <span data-ttu-id="cad31-138">Þegar sú eignamæling er uppfærð er tengdur teljari „Olía“ einnig uppfærður með sömu eignamælingargildum.</span><span class="sxs-lookup"><span data-stu-id="cad31-138">When that asset measure is updated, a related counter "Oil" is also updated with the same asset measure values.</span></span> <span data-ttu-id="cad31-139">Uppsetningin í **Teljendur** felur í sér uppsetningu á „Klukkutímum“.</span><span class="sxs-lookup"><span data-stu-id="cad31-139">The setup in **Counters** includes the setup on "Hours".</span></span> <span data-ttu-id="cad31-140">Einnig, í eignamælingunni „Olía“ ætti að bæta eignagerðinni „Truck Engine“ við á flýtiflipanum **Eignagerðir** til að tryggja tengsl eignamælingar.</span><span class="sxs-lookup"><span data-stu-id="cad31-140">Also, on the "Oil" asset measure, the asset type "Truck Engine" should be added to the **Asset types** FastTab to ensure the asset measure relation.</span></span> <span data-ttu-id="cad31-141">Sjá skjámyndirnar hér að neðan til að sjá dæmi um skipulag á eignamælingunum Tímar og Olía.</span><span class="sxs-lookup"><span data-stu-id="cad31-141">See the screenshots below for an example of the setup on the Hours and Oil asset measures.</span></span>

<span data-ttu-id="cad31-142">Þegar eignagerðum er bætt við í eignamælingagerð í **Teljarar** er þeirri eignamælingu sjálfvirkt bætt við eignagerðirnar á flýtiflipanum **Teljarar** í [Eignagerðir](../setup-for-objects/object-types.md).</span><span class="sxs-lookup"><span data-stu-id="cad31-142">When asset types are added to an asset measure type in **Counters**, that asset measure is automatically added to the asset types on the **Counters** FastTab in [Asset types](../setup-for-objects/object-types.md).</span></span>

![Mynd 1](media/071-setup-for-objects.png)


