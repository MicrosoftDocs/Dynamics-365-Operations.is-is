---
title: Sjálfvirk uppfærsla á eignateljurum
description: Þetta efni lýsir sjálfvirkri uppfærslu á eignateljurum í eignastýringu.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: fcc46fad8d57b7d4d57edfa4f2ae06de923d1c14
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430155"
---
# <a name="automatic-update-of-asset-counters"></a><span data-ttu-id="342ef-103">Sjálfvirk uppfærsla á eignateljurum</span><span class="sxs-lookup"><span data-stu-id="342ef-103">Automatic update of asset counters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="342ef-104">Nánari upplýsingar um handvirka skráningu á eignateljurum er að finna í [Handvirk uppfærsla á eignateljurum](../work-orders/manual-update-of-asset-counters.md).</span><span class="sxs-lookup"><span data-stu-id="342ef-104">For information about manual registration of asset counters, see [Manual update of asset counters](../work-orders/manual-update-of-asset-counters.md).</span></span> <span data-ttu-id="342ef-105">Sjá upplýsingar um hvernig á að setja upp eignateljara í [Teljarar](../setup-for-objects/counters.md).</span><span class="sxs-lookup"><span data-stu-id="342ef-105">For information on how to set up asset counters, see [Counters](../setup-for-objects/counters.md).</span></span>

<span data-ttu-id="342ef-106">Einnig er hægt að uppfæra teljaragildi sjálfkrafa úr framleiðsluskráningum, byggt á framleiðslutíma eða framleiðslumagni (það er að segja, því magni sem er framleitt).</span><span class="sxs-lookup"><span data-stu-id="342ef-106">Counter values can also be automatically updated from production registrations, based on the production hours or production quantity (that is, the quantity that is produced).</span></span> <span data-ttu-id="342ef-107">Þessi uppfærsla er gerð á síðunni **Uppfæra eignateljara**.</span><span class="sxs-lookup"><span data-stu-id="342ef-107">This update is done on the **Update asset counters** page.</span></span> <span data-ttu-id="342ef-108">Þú getur uppfært eina eða fleiri eignir með því að stilla eina færibreytu, **Frá dagsetningu**.</span><span class="sxs-lookup"><span data-stu-id="342ef-108">You can update one or several assets by setting one parameter, **From date**.</span></span> <span data-ttu-id="342ef-109">Þessi færibreyta tilgreinir upphafsdagsetningu framleiðsluskráninga (framleiðslutíma eða framleiðslumagn).</span><span class="sxs-lookup"><span data-stu-id="342ef-109">This parameter specifies the start date for production registrations (production hours or production quantities).</span></span> <span data-ttu-id="342ef-110">Með öðrum orðum tilgreinir hún dagsetninguna sem uppfæra skal teljaragildi frá.</span><span class="sxs-lookup"><span data-stu-id="342ef-110">In other words, it specifies the date that counter values should be updated from.</span></span>

<span data-ttu-id="342ef-111">Allar eignir sem tengjast tilföngum *og* hafa eignateljara, sem eru settar upp til uppfærslu miðað við framleiðslutíma eða framleiðslumagn, verða með í sjálfvirkri uppfærslu og ný teljaragildi verða til.</span><span class="sxs-lookup"><span data-stu-id="342ef-111">All assets that are related to a resource, *and* that have asset counters that are set up to be updated based on the production hours or production quantity, will be included in an automatic update.</span></span> <span data-ttu-id="342ef-112">Ný teljagildi verða til.</span><span class="sxs-lookup"><span data-stu-id="342ef-112">New counter values will be created.</span></span>

<span data-ttu-id="342ef-113">Fyrir teljara sem byggjast á framleiðslumagni samanstendur talan bæði af gallalausu magni og villumagni sem er skráð.</span><span class="sxs-lookup"><span data-stu-id="342ef-113">For counters that are based on the production quantity, the count includes both the good quantity and the error quantity that are registered.</span></span> <span data-ttu-id="342ef-114">Ef einingin sem er notuð fyrir skráningu á framleiðslumagni er frábrugðin einingunni sem notuð er í teljaranum er magninu breytt til að samsvara teljaraeiningunni.</span><span class="sxs-lookup"><span data-stu-id="342ef-114">If the unit that is used for production quantity registration differs from the unit that is used for the counter, the quantity is converted so that it corresponds to the counter unit.</span></span>

<span data-ttu-id="342ef-115">Eins og getið er hér að ofan er hægt að uppfæra sjálfvirka teljara úr framleiðsluskráningum.</span><span class="sxs-lookup"><span data-stu-id="342ef-115">As mentioned above, automatic counters can be updated from production registrations.</span></span> <span data-ttu-id="342ef-116">Þess vegna verður eignin sem þú vilt uppfæra teljara sjálfkrafa fyrir að tengjast tilföngum (vél).</span><span class="sxs-lookup"><span data-stu-id="342ef-116">Therefore, the asset for which you want to automatically update counters must be related to a resource (machine).</span></span> <span data-ttu-id="342ef-117">Þegar framleitt magn eða framleiðslutími hefur verið skráður á tilföngin geturðu uppfært tengda eignateljara.</span><span class="sxs-lookup"><span data-stu-id="342ef-117">When produced quantities or production hours have been registered on the resource, you can update the related asset counters.</span></span>

1. <span data-ttu-id="342ef-118">Veldu **Eignastýring** > **Reglubundið** > **Eignir** > **Uppfæra eignateljara**.</span><span class="sxs-lookup"><span data-stu-id="342ef-118">Select **Asset management** > **Periodic** > **Assets** > **Update asset counters**.</span></span>

2. <span data-ttu-id="342ef-119">Í reitnum **Frá dagsetningu** velurðu upphafsdagsetningu sjálfvirku uppfærslunnar.</span><span class="sxs-lookup"><span data-stu-id="342ef-119">In the **From date** field, select the start date of the automatic update.</span></span>

    >[!NOTE]
    ><span data-ttu-id="342ef-120">Dagsetningin í þessum reit er dagsetningin „verk í vinnslu“ frá og með **Leiðarfærslur** (reiturinn **Framleiðslustýring** > **Fyrirspurnir og skýrslur** > **Framleiðsla** > **Leiðarfærslur** > **Efnisleg dagsetning**).</span><span class="sxs-lookup"><span data-stu-id="342ef-120">The date in this field is the "work in progress" date from **Route transactions** (**Production control** > **Inquiries and reports** > **Production** > **Route transactions** > **Physical date** field).</span></span>

3. <span data-ttu-id="342ef-121">Á flýtiflipanum **Færslur til að taka með** er hægt að velja tilteknar eignir, eignategundir eða tilföng fyrir sjálfvirka uppfærslu.</span><span class="sxs-lookup"><span data-stu-id="342ef-121">On the **Records to include** FastTab, you can select specific assets, asset types, or resources for the automatic update.</span></span> <span data-ttu-id="342ef-122">Veldu **Sía** og gerðu viðeigandi val.</span><span class="sxs-lookup"><span data-stu-id="342ef-122">Select **Filter**, and make the relevant selections.</span></span>

4. <span data-ttu-id="342ef-123">Á flýtiflipanum **Keyra í bakgrunni** geturðu sett upp sjálfvirka uppfærslu sem runuvinnslu, eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="342ef-123">On the **Run in the background** FastTab, you can set up the automatic update as a batch job, as you require.</span></span>

    <span data-ttu-id="342ef-124">Myndin hér að neðan sýnir dæmi um gluggann **Uppfæra eignateljara**.</span><span class="sxs-lookup"><span data-stu-id="342ef-124">The illustration below shows an example of the **Update asset counters** dialog.</span></span>

    ![Mynd 1](media/12-work-orders.png)

5. <span data-ttu-id="342ef-126">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="342ef-126">Select **OK**.</span></span> 

<span data-ttu-id="342ef-127">Eftir að sjálfvirkri uppfærslu á eignateljurum er lokið geturðu skoðað gagnaskráningar sem tengjast eigninni á síðunni **Eignateljarar**.</span><span class="sxs-lookup"><span data-stu-id="342ef-127">After the automatic asset counter update is done, you can view the counter registrations that are related to the asset on the **Asset counters** page.</span></span> <span data-ttu-id="342ef-128">Veldu **Eignastýring** > **Sameiginlegt** > **Eignir** > **Allar eignir**, veldu eignina og síðan á aðgerðarrúðunni, á flipanum **Eignir**, í hópnum **Fyrirbyggjandi**, velurðu **Teljarar**.</span><span class="sxs-lookup"><span data-stu-id="342ef-128">Select **Asset management** > **Common** > **Assets** > **All assets**, select the asset, and then, on the Action Pane, on the **Asset** tab, in the **Preventive** group, select **Counters**.</span></span>

<span data-ttu-id="342ef-129">Á síðunni **Samanlagt verðmæti eigna** er hægt að fá yfirlit yfir nýjustu skráningu sem hafa verið gerðar á öllum teljaragerðum á öllum eignum.</span><span class="sxs-lookup"><span data-stu-id="342ef-129">On the **Asset aggregated value** page, you can get an overview of the latest registration that have been made on all counter types on all assets.</span></span> <span data-ttu-id="342ef-130">Veldu **Eignastýringu** > **Fyrirspurnir** > **Eignir** > **Uppsafnað gildi eigna**.</span><span class="sxs-lookup"><span data-stu-id="342ef-130">Select **Asset management** > **Inquiries** > **Assets** > **Asset aggregated value**.</span></span> <span data-ttu-id="342ef-131">Þessi síða líkist síðunni **Eignateljar** en þú getur ekki bætt við eða breytt skráningum.</span><span class="sxs-lookup"><span data-stu-id="342ef-131">This page resembles the **Asset counters** page, but you can't add or edit registrations.</span></span> <span data-ttu-id="342ef-132">Hún er aðeins til yfirlits.</span><span class="sxs-lookup"><span data-stu-id="342ef-132">It's for overview only.</span></span>

<span data-ttu-id="342ef-133">Myndin hér að neðan sýnir dæmi um síðuna **Samanlagt verðmæti eigna**.</span><span class="sxs-lookup"><span data-stu-id="342ef-133">The illustration below shows an example of the **Asset aggregated value** page.</span></span>

![Mynd 2](media/13-work-orders.png)

<span data-ttu-id="342ef-135">Athugið eftirfarandi stig:</span><span class="sxs-lookup"><span data-stu-id="342ef-135">Note the following points:</span></span>

- <span data-ttu-id="342ef-136">Hægt er að búa til handvirkar teljaragildisskráningar fyrir teljaragerðir sem eru uppfærðar sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="342ef-136">You can still create manual counter value registrations for counter types that are automatically updated.</span></span> <span data-ttu-id="342ef-137">Nánari upplýsingar er að finna í [Handvirkri uppfærslu á eignateljurum](../work-orders/manual-update-of-asset-counters.md).</span><span class="sxs-lookup"><span data-stu-id="342ef-137">For more information, see [Manual update of asset counters](../work-orders/manual-update-of-asset-counters.md).</span></span>

- <span data-ttu-id="342ef-138">Þú getur sett upp teljara sem tengjast öðrum teljara.</span><span class="sxs-lookup"><span data-stu-id="342ef-138">You can set up counters that are related to another counter.</span></span> <span data-ttu-id="342ef-139">Í þessu tilfelli, þegar teljarinn er uppfærður, eru tengdir teljarar sjálfkrafa uppfærðir um leið.</span><span class="sxs-lookup"><span data-stu-id="342ef-139">In this case, when a counter is updated, related counters are automatically updated at the same time.</span></span> <span data-ttu-id="342ef-140">Nánari upplýsingar um hvernig setja skal upp tengda eignateljara er að finna í [Teljarar](../setup-for-objects/counters.md).</span><span class="sxs-lookup"><span data-stu-id="342ef-140">For more information about how to set up related counters, see [Counters](../setup-for-objects/counters.md).</span></span>

