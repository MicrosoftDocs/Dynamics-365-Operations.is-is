---
title: Sjálfvirk uppfærsla á eignateljurum
description: Þetta efni lýsir sjálfvirkri uppfærslu á eignateljurum í eignastýringu.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 97e6912cd37d6f82d8bf022141f04645a3364ee1
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875721"
---
# <a name="automatic-update-of-asset-counters"></a><span data-ttu-id="fb566-103">Sjálfvirk uppfærsla á eignateljurum</span><span class="sxs-lookup"><span data-stu-id="fb566-103">Automatic update of asset counters</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="fb566-104">Í fyrri hlutanum er lýst handvirkri skráningu eignateljara.</span><span class="sxs-lookup"><span data-stu-id="fb566-104">In the previous section, manual registration of asset counters is described.</span></span> <span data-ttu-id="fb566-105">Uppsetning eignateljara er lýst í [Teljarar](../setup-for-objects/counters.md).</span><span class="sxs-lookup"><span data-stu-id="fb566-105">Setup of asset counters is described in [Counters](../setup-for-objects/counters.md).</span></span>

<span data-ttu-id="fb566-106">Einnig er hægt að uppfæra teljaragildi sjálfkrafa úr framleiðsluskráningum, byggt á framleiðslutíma eða framleiðslumagni.</span><span class="sxs-lookup"><span data-stu-id="fb566-106">Counter values can also be automatically updated from production registrations, based on production hours or production quantity.</span></span> <span data-ttu-id="fb566-107">Þetta er gert í **Uppfæra eignateljara**.</span><span class="sxs-lookup"><span data-stu-id="fb566-107">This is done in **Update asset counters**.</span></span> <span data-ttu-id="fb566-108">Þú getur uppfært eina eða fleiri eignir með því að setja eina færibreytu inn, **Frá dagsetningu**.</span><span class="sxs-lookup"><span data-stu-id="fb566-108">You can update one or several assets by inserting one parameter, **From date**.</span></span> <span data-ttu-id="fb566-109">Þessi færibreyta tilgreinir upphafsdagsetningu framleiðsluskráninga (klukkustundir eða magn framleitt), sem þýðir upphafsdagsetninguna sem uppfæra ætti teljaragildi frá.</span><span class="sxs-lookup"><span data-stu-id="fb566-109">This parameter specifies the start date for production registrations (hours or quantity produced), meaning the start date from which counter values should be updated.</span></span>

<span data-ttu-id="fb566-110">Allar eignir sem tengjast tilföngum *og* hafa eignateljara, sem eru settar upp til að uppfæra miðað við framleitt magn eða framleiðslutíma, verða með í sjálfvirkri uppfærslu og ný teljaragildi verða til.</span><span class="sxs-lookup"><span data-stu-id="fb566-110">All assets that are related to a resource *and* have asset counters, which are set up to be updated based on produced quantity or production hours, will be included in an automatic update, and new counter values will be created.</span></span>

<span data-ttu-id="fb566-111">Varðandi teljarana sem eru miðaðir við framleiðslumagn, þá er gallalaust magn sem og villumagn skráð með í talningunni.</span><span class="sxs-lookup"><span data-stu-id="fb566-111">Regarding counters based on production quantity, good quantity as well as error quantity registered are included in the count.</span></span> <span data-ttu-id="fb566-112">Ef einingin sem notuð er fyrir skráningu á framleiddu magni er frábrugðin einingunni sem notuð er í teljaranum er magni breytt til að samsvara teljaraeiningunni.</span><span class="sxs-lookup"><span data-stu-id="fb566-112">If the unit used for produced quantity registration is different from the unit used on the counter, quantity is converted to correspond with the counter unit.</span></span>

<span data-ttu-id="fb566-113">Eins og getið er hér að ofan er hægt að uppfæra sjálfvirka teljara úr framleiðsluskráningum.</span><span class="sxs-lookup"><span data-stu-id="fb566-113">As mentioned above, automatic counters can be updated from production registrations.</span></span> <span data-ttu-id="fb566-114">Þess vegna verður eignin sem þú vilt uppfæra teljara sjálfkrafa fyrir að tengjast tilföngum (vél).</span><span class="sxs-lookup"><span data-stu-id="fb566-114">Therefore, the asset for which you want to automatically update counters must be related to a resource (machine).</span></span> <span data-ttu-id="fb566-115">Eftirfarandi lýsingar veita yfirlit yfir uppsetningu og vinnslu framleiðslupantana (í einingunni **Framleiðslustýring**), sem er notuð sem grunnur fyrir sjálfvirka uppfærslu á teljurum á eign í einingunni **Eignastýring**.</span><span class="sxs-lookup"><span data-stu-id="fb566-115">The following descriptions provide an overview of the setup and processing of production orders (in the **Production control** module), which is used as a basis for automatic update of counters on an asset in the **Asset management** module.</span></span>

<span data-ttu-id="fb566-116">Þegar framleitt magn eða framleiðslutími hefur verið skráður á tilföngin geturðu uppfært tengda eignateljara.</span><span class="sxs-lookup"><span data-stu-id="fb566-116">When produced quantities or production hours have been registered on the resource, you can update the related asset counters.</span></span>

1. <span data-ttu-id="fb566-117">Smelltu á **Eignastýring** > **Reglubundið** > **Eignir** > **Uppfæra eignateljara**.</span><span class="sxs-lookup"><span data-stu-id="fb566-117">Click **Asset management** > **Periodic** > **Assets** > **Update asset counters**.</span></span>

2. <span data-ttu-id="fb566-118">Veldu upphafsdagsetningu sjálfvirku uppfærslunnar í reitnum **Frá dagsetningu**.</span><span class="sxs-lookup"><span data-stu-id="fb566-118">Select the start date of the automatic update in the **From date** field.</span></span>

>[!NOTE]
><span data-ttu-id="fb566-119">Dagsetningin í þessum reit er dagsetningin „verk í vinnslu“ frá og með **Leiðarfærslur** (reiturinn **Framleiðslustýring** > **Fyrirspurnir og skýrslur** > **Framleiðsla** > **Leiðarfærslur** > **Efnisleg dagsetning**).</span><span class="sxs-lookup"><span data-stu-id="fb566-119">The date in this field is the "work in progress" date from **Route transactions** (**Production control** > **Inquiries and reports** > **Production** > **Route transactions** > **Physical date** field).</span></span>

3. <span data-ttu-id="fb566-120">Ef þú vilt velja tilteknar eignir, eignategundir eða tilföng fyrir sjálfvirka uppfærslu skaltu smella á **Sía** á flýtiflipanum **Færslur til að hafa með** og gera viðeigandi val.</span><span class="sxs-lookup"><span data-stu-id="fb566-120">If you want to select specific assets, asset types, or resources for the automatic update, click **Filter** on the **Records to include** FastTab, and make the relevant selections.</span></span>

4. <span data-ttu-id="fb566-121">Ef með þarf er hægt að setja upp sjálfvirka uppfærslu sem runuvinnslu á flýtiflipanum **Keyra í bakgrunni**.</span><span class="sxs-lookup"><span data-stu-id="fb566-121">If required, you can set up the automatic update as a batch job on the **Run in the background** FastTab.</span></span>

![Mynd 1](media/12-work-orders.png)

5. <span data-ttu-id="fb566-123">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="fb566-123">Click **OK**.</span></span> <span data-ttu-id="fb566-124">Þegar sjálfvirka uppfærsla á eignateljara er lokið geturðu séð teljaraskráningar tengdar eigninni í **Eignateljar** (**Eignastýring** > **Sameiginlegt** > **Eignir** > **Allar eignir** > veldu eign > hnappurinn **Teljarar**).</span><span class="sxs-lookup"><span data-stu-id="fb566-124">When the automatic asset counter update is done, you can see the counter registrations related to the asset in **Asset counters** (**Asset management** > **Common** > **Assets** > **All assets** > select asset > **Counters** button).</span></span>

<span data-ttu-id="fb566-125">Í **Heildartala eigna** er hægt að fá yfirlit yfir nýjustu skráningu sem var gerð á öllum teljaragerðum á öllum eignum.</span><span class="sxs-lookup"><span data-stu-id="fb566-125">In **Asset counter totals**, you can get an overview of the latest registration made on all counter types on all assets.</span></span> <span data-ttu-id="fb566-126">Smelltu á **Eignastýringu** > **Fyrirspurnir** > **Eignir** > **Uppsafnað gildi eigna**.</span><span class="sxs-lookup"><span data-stu-id="fb566-126">Click **Asset management** > **Inquiries** > **Assets** > **Asset aggregated value**.</span></span> <span data-ttu-id="fb566-127">Yfirlitið er mjög svipað og **Eignateljar**, en þú getur ekki bætt við eða breytt skráningum í **Samanlagt verðmæti eigna**.</span><span class="sxs-lookup"><span data-stu-id="fb566-127">The view is very similar to **Asset counters**, but you cannot add or edit registrations in **Asset aggregated value**.</span></span> <span data-ttu-id="fb566-128">Það er aðeins til yfirlits.</span><span class="sxs-lookup"><span data-stu-id="fb566-128">It is for overview only.</span></span>

![Mynd 2](media/13-work-orders.png)


- <span data-ttu-id="fb566-130">Enn er hægt að búa til handvirkar teljaragildisskráningar fyrir teljaragerðir sem eru uppfærðar sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="fb566-130">It is still possible to create manual counter value registrations for counter types that are automatically updated.</span></span> <span data-ttu-id="fb566-131">Nánari upplýsingar er að finna í hlutanum „Handvirk uppfærsla á eignateljurum“.</span><span class="sxs-lookup"><span data-stu-id="fb566-131">Refer to the "Manual update of asset counters" section for more information.</span></span>
- <span data-ttu-id="fb566-132">Hægt er að setja upp teljara sem tengjast öðrum teljara, sem þýðir að þegar teljari er uppfærður eru skyldir teljarar uppfærðir sjálfkrafa um leið.</span><span class="sxs-lookup"><span data-stu-id="fb566-132">You can set up counters related to another counter, which means that when a counter is updated, related counters are automatically updated at the same time.</span></span> <span data-ttu-id="fb566-133">Sjá [Teljarar](../setup-for-objects/counters.md) varðandi uppsetningu á tengdum teljurum.</span><span class="sxs-lookup"><span data-stu-id="fb566-133">Refer to [Counters](../setup-for-objects/counters.md) regarding setup of related counters.</span></span>
