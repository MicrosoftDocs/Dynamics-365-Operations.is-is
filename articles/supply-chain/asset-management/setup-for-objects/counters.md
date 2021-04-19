---
title: Eignamælingar
description: Umræðuefnið útskýrir hvernig á að stofna eignamælingar í eignastýringu.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetObjectCounterPart, EntAssetObjectCounterLookup, EntAssetCounterType, EntAssetObjectCounterTotals
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e119eee82b1438dd8c3ccbaf2d54962b59fe6ae3
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808401"
---
# <a name="counters"></a><span data-ttu-id="22f00-103">Teljarar</span><span class="sxs-lookup"><span data-stu-id="22f00-103">Counters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="22f00-104">Umræðuefnið útskýrir hvernig á að stofna teljaramælingar í eignastýringu.</span><span class="sxs-lookup"><span data-stu-id="22f00-104">The topic explains how to create counter types in Asset Management.</span></span> <span data-ttu-id="22f00-105">Gerðir teljaramælinga eru notaðar til að gera teljaraskráningar á eignir, til dæmis varðandi fjölda framleiðslutíma eða magn framleitt á eigninni.</span><span class="sxs-lookup"><span data-stu-id="22f00-105">Counter types are used to make counter registrations on assets, for example, regarding number of production hours, or quantity produced on the asset.</span></span> <span data-ttu-id="22f00-106">Tegundir eigna eru tengdar gerðum teljara.</span><span class="sxs-lookup"><span data-stu-id="22f00-106">Asset types are related to the counter types.</span></span> <span data-ttu-id="22f00-107">Þetta þýðir að einungis er hægt að nota teljara á eign ef teljarinn er sett upp á eignategundinni sem notuð er á eigninni.</span><span class="sxs-lookup"><span data-stu-id="22f00-107">This means that a counter can only be used on an asset if the counter is set up on the asset type used on the asset.</span></span>

<span data-ttu-id="22f00-108">Áður en þú getur gert teljaraskráningar á eignir þarf fyrst að stofna þær teljaragerðir sem þú vilt nota í **Teljarar**.</span><span class="sxs-lookup"><span data-stu-id="22f00-108">Before you can make counter registrations on assets, you first create the counter types you want to use in **Counters**.</span></span> <span data-ttu-id="22f00-109">Næst geturðu búið til teljaraskráningar á eignum í **Teljarar**.</span><span class="sxs-lookup"><span data-stu-id="22f00-109">Next, you can create counter registrations on assets in **Counters**.</span></span> 

<span data-ttu-id="22f00-110">Hægt er að nota teljara í viðhaldsáætlunum.</span><span class="sxs-lookup"><span data-stu-id="22f00-110">Counters can be used on maintenance plans.</span></span> <span data-ttu-id="22f00-111">Viðhaldsáætlunarlína getur verið af gerðinni „Teljari“, til dæmis varðandi fjölda framleiðslutíma eða framleitt magn.</span><span class="sxs-lookup"><span data-stu-id="22f00-111">A maintenance plan line can be of type "Counter", for example, relating to number of production hours or quantity produced.</span></span> 

<span data-ttu-id="22f00-112">Hægt er að uppfæra teljaraskráningu handvirkt eða sjálfkrafa út frá framleiðslutíma eða framleiddu magni.</span><span class="sxs-lookup"><span data-stu-id="22f00-112">A counter registration can be updated manually or automatically based on production hours or quantity produced.</span></span> <span data-ttu-id="22f00-113">Hægt er að setja upp teljara til að nota eina af þremur uppfærsluaðferðum (valið í reitnum **Uppfæra** í **Teljarar**):</span><span class="sxs-lookup"><span data-stu-id="22f00-113">A counter can be set up to use one of three update methods (selected in the **Update** field in **Counters**):</span></span>
  
- <span data-ttu-id="22f00-114">Handvirkt - þú verður að skrá teljaragildi handvirkt.</span><span class="sxs-lookup"><span data-stu-id="22f00-114">Manual - you must manually register counter values.</span></span>  
- <span data-ttu-id="22f00-115">Framleiðslutímar - teljarinn er sjálfkrafa uppfærður út frá fjölda framleiðslutíma.</span><span class="sxs-lookup"><span data-stu-id="22f00-115">Production hours - the counter is automatically updated based on number of production hours.</span></span>  
- <span data-ttu-id="22f00-116">Framleiðslumagn - teljarinn er sjálfkrafa uppfærður út frá framleiddu magni.</span><span class="sxs-lookup"><span data-stu-id="22f00-116">Production quantity - the counter is automatically updated based on number of quantity produced.</span></span>  

>[!NOTE]
><span data-ttu-id="22f00-117">Ef framleitt magn er notað eru *allir* skráðir hlutir með í teljaraskráningu, gott magn sem og villumagn.</span><span class="sxs-lookup"><span data-stu-id="22f00-117">If quantity produced is used, *all* registered items are included in the counter registration, good quantity as well as error quantity.</span></span> <span data-ttu-id="22f00-118">Það er alltaf mögulegt að gera handvirkar teljaraskráningar, ef þess þarf.</span><span class="sxs-lookup"><span data-stu-id="22f00-118">It is always possible to make manual counter registrations, if required.</span></span>

## <a name="create-counter-types-for-asset-counter-registrations"></a><span data-ttu-id="22f00-119">Búðu til gagnategundir fyrir skráningar eignateljara</span><span class="sxs-lookup"><span data-stu-id="22f00-119">Create counter types for asset counter registrations</span></span>

1. <span data-ttu-id="22f00-120">Veldu **Eignastýring** > **Uppsetning** > **Eignagerðir** > **Teljarar**.</span><span class="sxs-lookup"><span data-stu-id="22f00-120">Select **Asset management** > **Setup** > **Asset types** > **Counters**.</span></span>
2. <span data-ttu-id="22f00-121">Veldu **Nýr** til að stofna nýja teljaragerð.</span><span class="sxs-lookup"><span data-stu-id="22f00-121">Select **New** to create a new counter type.</span></span>
3. <span data-ttu-id="22f00-122">Settu inn auðkenni í reitinn **Teljari** og teljaraheiti í reitinn **Heiti**.</span><span class="sxs-lookup"><span data-stu-id="22f00-122">Insert an ID in the **Counter** field, and a counter name in the **Name** field.</span></span>
4. <span data-ttu-id="22f00-123">Á flýtiflipanum **Almennt** velurðu teljaraeiningu í reitnum **Eining**.</span><span class="sxs-lookup"><span data-stu-id="22f00-123">On the **General** FastTab, select a counter unit in the **Unit** field.</span></span>
5. <span data-ttu-id="22f00-124">Í retinum **Uppfæra** velurðu uppfærsluaðferðina sem á að nota fyrir teljarann.</span><span class="sxs-lookup"><span data-stu-id="22f00-124">In the **Update** field, select the update method to be used for the counter.</span></span>
6. <span data-ttu-id="22f00-125">Veldu „Já“ á skiptihnappnum **Erfa teljaragildi** ef undireignir í eignaskipan ættu sjálfkrafa að erfa teljaraskráningar sem gerðar eru á yfireigninni.</span><span class="sxs-lookup"><span data-stu-id="22f00-125">Select "Yes" on the **Inherit counter values** toggle button if child assets in an asset structure should automatically inherit counter registrations made on the parent asset.</span></span>
7. <span data-ttu-id="22f00-126">Í retinum **Samtals samanlagt** velurðu samantektaraðferðina sem á að nota fyrir teljara með þessari teljaragerð.</span><span class="sxs-lookup"><span data-stu-id="22f00-126">In the **Total aggregate** field, select the summation method to be used for a counter using this counter type.</span></span> <span data-ttu-id="22f00-127">„Summa“ er staðalvalið sem notað er til að bæta skráðum gildi stöðugt við heildargildið.</span><span class="sxs-lookup"><span data-stu-id="22f00-127">"Sum" is the standard selection used to continuously add registered values to the total value.</span></span> <span data-ttu-id="22f00-128">Hægt er að nota „meðaltal“ ef teljari er settur upp til að fylgjast með þröskuldi, til dæmis varðandi hitastig, titring eða slit á eign.</span><span class="sxs-lookup"><span data-stu-id="22f00-128">"Average" can be used if a counter is set up to monitor a threshold, for example, regarding temperature, vibrations, or wear and tear on an asset.</span></span> 
8. <span data-ttu-id="22f00-129">Í reitnum **Frávik yfir** seturðu efra stigið inn í prósentu til að sannprófa hvort handvirkar teljaraskráningar séu innan áætlaðs sviðs.</span><span class="sxs-lookup"><span data-stu-id="22f00-129">In the **Deviation over** field, insert the upper level in percent for validating if manual counter registrations are within an expected range.</span></span> <span data-ttu-id="22f00-130">Sannprófunin er byggð á línulegri aukningu á núverandi teljaraskráningum.</span><span class="sxs-lookup"><span data-stu-id="22f00-130">The validation is based on a linear increase in existing counter registrations.</span></span>
9. <span data-ttu-id="22f00-131">Í reitnum **Frávik undir** seturðu neðra stigið inn í prósentu til að sannprófa hvort handvirkar teljaraskráningar séu innan áætlaðs sviðs.</span><span class="sxs-lookup"><span data-stu-id="22f00-131">In the **Deviation under** field, insert the lower level in percent for validating if manual counter registrations are within an expected range.</span></span> <span data-ttu-id="22f00-132">Sannprófunin er byggð á línulegri lækkun á núverandi teljaraskráningum.</span><span class="sxs-lookup"><span data-stu-id="22f00-132">The validation is based on a linear decrease in existing counter registrations.</span></span>
10. <span data-ttu-id="22f00-133">Í reitnum **Tegund** velurðu gerð skilaboðanna (upplýsingar, viðvörun, villu) sem á að sýna ef frávik utan skilgreinds sviðs eiga sér stað þegar þú gerir handvirkar teljaraskráningar.</span><span class="sxs-lookup"><span data-stu-id="22f00-133">In the **Type** field, select the type of message (information, warning, error) to be shown if deviations outside the defined range occur when you make manual counter registrations.</span></span>
11. <span data-ttu-id="22f00-134">Á flýtiflipanum **Eignagerðir** bætirðu við eignagerðum sem ættu að geta notað teljarann.</span><span class="sxs-lookup"><span data-stu-id="22f00-134">On the **Asset types** FastTab, add the asset types that should be able to use the counter.</span></span>
12. <span data-ttu-id="22f00-135">Á flýtiflipanum **Tengdir eignateljarar** bætirðu við teljaranum sem þú vilt að uppfærist sjálfkrafa þegar þessi teljari er uppfærður.</span><span class="sxs-lookup"><span data-stu-id="22f00-135">On the **Related asset counters** FastTab, add the counter that you want to be automatically updated when this counter is updated.</span></span>


>[!NOTE]
><span data-ttu-id="22f00-136">Tengdur teljari er sjálfkrafa uppfærður ef viðkomandi teljari hefur eignagerðina sem hún er tengd við í teljarauppsetningunni.</span><span class="sxs-lookup"><span data-stu-id="22f00-136">A related counter is automatically updated only if the related counter has the asset type, to which it is related, in the counter setup.</span></span> <span data-ttu-id="22f00-137">Til dæmis: Þú setur upp teljara fyrir „Framleiðslutíma“ og bætir við eignategundinni „Truck Engine“.</span><span class="sxs-lookup"><span data-stu-id="22f00-137">For example: You set up a counter for "Production hours" and add the asset type "Truck Engine".</span></span> <span data-ttu-id="22f00-138">Þegar sá teljari er uppfærður er tengdur teljari „Olía“ einnig uppfærður með sömu teljaragildum.</span><span class="sxs-lookup"><span data-stu-id="22f00-138">When that counter is updated, a related counter "Oil" is also updated with the same counter values.</span></span> <span data-ttu-id="22f00-139">Uppsetningin í **Teljendur** felur í sér uppsetningu á „Klukkutímum“.</span><span class="sxs-lookup"><span data-stu-id="22f00-139">The setup in **Counters** includes the setup on "Hours".</span></span> <span data-ttu-id="22f00-140">Einnig, í teljaranum „Olía“ ætti að bæta eignagerðinni „Truck Engine“ við á flýtiflipanum **Eignagerðir** til að tryggja teljaratengsl.</span><span class="sxs-lookup"><span data-stu-id="22f00-140">Also, on the "Oil" counter, the asset type "Truck Engine" should be added to the **Asset types** FastTab to ensure the counter relation.</span></span> <span data-ttu-id="22f00-141">Sjá skjámyndirnar hér að neðan til að sjá dæmi um skipulag á teljurunum Tímar og Olía.</span><span class="sxs-lookup"><span data-stu-id="22f00-141">See the screenshots below for an example of the setup on the Hours and Oil counters.</span></span>

<span data-ttu-id="22f00-142">Þegar eignagerðum er bætt við í teljaragerð í **Teljarar** er þeim teljara sjálfvirkt bætt við eignagerðirnar á flýtiflipanum **Teljarar** í [Eignagerðir](../setup-for-objects/object-types.md).</span><span class="sxs-lookup"><span data-stu-id="22f00-142">When asset types are added to a counter type in **Counters**, that counter is automatically added to the asset types on the **Counters** FastTab in [Asset types](../setup-for-objects/object-types.md).</span></span>

![Mynd 1](media/071-setup-for-objects.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]