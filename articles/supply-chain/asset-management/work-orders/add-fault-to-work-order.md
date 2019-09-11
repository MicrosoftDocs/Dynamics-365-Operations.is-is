---
title: Bættu bilun við verkbeiðnina
description: Þetta efni lýsir því hvernig bæta má bilanaskráningum við verkbeiðnir í eignastýringu.
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
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7c86973ca44d9113d14e180e27cc51343da5d2c0
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875719"
---
# <a name="add-fault-to-work-order"></a><span data-ttu-id="4adc1-103">Bættu bilun við verkbeiðnina</span><span class="sxs-lookup"><span data-stu-id="4adc1-103">Add fault to work order</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="4adc1-104">Þú getur bætt bilunum sem eru settar upp í bilunarhönnuðinni við verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="4adc1-104">You can add faults set up in the fault designer to a work order.</span></span> <span data-ttu-id="4adc1-105">Eignin sem valin er í verkbeiðninni verður að innihalda eignagerðir sem hafa eina eða fleiri bilaskrár tengdar henni.</span><span class="sxs-lookup"><span data-stu-id="4adc1-105">The asset selected in the work order must contain asset types that have one or more fault records connected to it.</span></span> <span data-ttu-id="4adc1-106">Lestu meira um uppsetningu í kaflanum [Bilanastjórnun](../setup-for-work-orders/fault-management.md).</span><span class="sxs-lookup"><span data-stu-id="4adc1-106">Read more about setup in the [Fault management](../setup-for-work-orders/fault-management.md) section.</span></span>

1. <span data-ttu-id="4adc1-107">Smelltu á **Eignastýringu** > **Sameiginlegt** > **Vinnufyrirmæli** > **Allar vinnupantanir** eða **Virkar vinnupantanir**.</span><span class="sxs-lookup"><span data-stu-id="4adc1-107">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="4adc1-108">Veldu listann á verkbeiðnina sem þú vilt gera villuskráningu á og smelltu á **Bilun í eignum**.</span><span class="sxs-lookup"><span data-stu-id="4adc1-108">In the list, select the work order on which you want to make a fault registration and click **Asset fault**.</span></span>

3. <span data-ttu-id="4adc1-109">Á flýtiflipanum **Einkenni** er smellt á **Bæta við línu**.</span><span class="sxs-lookup"><span data-stu-id="4adc1-109">On the **Symptoms** FastTab, click **Add line**.</span></span> <span data-ttu-id="4adc1-110">Raðnúmer fyrir bilun er sjálfkrafa sett inn í reitinn **Bilun**.</span><span class="sxs-lookup"><span data-stu-id="4adc1-110">A sequential fault number is automatically inserted in the **Fault** field.</span></span>

4. <span data-ttu-id="4adc1-111">Veldu viðeigandi einkenni í reitnum **Bilunareinkenni**.</span><span class="sxs-lookup"><span data-stu-id="4adc1-111">Select the relevant symptom in the **Fault symptom** field.</span></span>

5. <span data-ttu-id="4adc1-112">Veldu **Bilunarsvæði** og **Bilunartegund**.</span><span class="sxs-lookup"><span data-stu-id="4adc1-112">Select **Fault area** and **Fault type**.</span></span>

6. <span data-ttu-id="4adc1-113">Í reitnum **Dagsetning bilunar** er núverandi dagsetning sjálfkrafa sett inn.</span><span class="sxs-lookup"><span data-stu-id="4adc1-113">In the **Fault date** field, the current date is automatically inserted.</span></span> <span data-ttu-id="4adc1-114">Hægt er að velja aðra dagsetningu ef þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="4adc1-114">You can select another date, if necessary.</span></span>

7. <span data-ttu-id="4adc1-115">Á flýtiflipanum **Orsakir fyrir valið einkenni** bætirðu við línu sem lýsir orsökum vandans.</span><span class="sxs-lookup"><span data-stu-id="4adc1-115">On the **Causes for selected symptom** FastTab, add a line describing the cause of the problem.</span></span>

8. <span data-ttu-id="4adc1-116">Á flýtiflipanum **Úrræði fyrir valið einkenni** bætirðu við línu sem lýsir hugsanlegri lausn við vandanum.</span><span class="sxs-lookup"><span data-stu-id="4adc1-116">On the **Remedies for selected symptom** FastTab, add a line describing a possible solution to the problem.</span></span>

9. <span data-ttu-id="4adc1-117">Smellt er á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="4adc1-117">Click **Save**.</span></span>

![Mynd 1](media/19-work-orders.png)


## <a name="view-asset-faults"></a><span data-ttu-id="4adc1-119">Skoða eignabilanir</span><span class="sxs-lookup"><span data-stu-id="4adc1-119">View asset faults</span></span>

<span data-ttu-id="4adc1-120">Í listanum **Eignabilanir** er hægt að fá yfirlit yfir allar bilanir sem eru skráðar á eignum.</span><span class="sxs-lookup"><span data-stu-id="4adc1-120">In the **Asset faults** list, you can get an overview of all faults registered on assets.</span></span>

<span data-ttu-id="4adc1-121">Smelltu á **Eignastýringu** > **Fyrirspurnir** > **Bilun eignar** > **Bilanir eigna** til að opna listann.</span><span class="sxs-lookup"><span data-stu-id="4adc1-121">Click **Asset management** > **Inquiries** > **Asset fault** > **Asset faults** to open the list.</span></span>


## <a name="print-asset-fault-report"></a><span data-ttu-id="4adc1-122">Prenta eignabilanaskýrslur</span><span class="sxs-lookup"><span data-stu-id="4adc1-122">Print asset fault report</span></span>

<span data-ttu-id="4adc1-123">Af listasíðunni **Allar eignir** er hægt að prenta eignabilanaskýrslu sem sýnir allar bilanaskráningar auk myndræns yfirlits yfir tölfræðilegar bilanir.</span><span class="sxs-lookup"><span data-stu-id="4adc1-123">From the **All assets** list page, you can print an asset fault report displaying all fault registrations as well as a graphic overview of fault statistics.</span></span>

1. <span data-ttu-id="4adc1-124">Smelltu á **Eignastjórnun** > **Sameiginlegt** > **Eignir** > **Allar eignir**.</span><span class="sxs-lookup"><span data-stu-id="4adc1-124">Click **Asset management** > **Common** > **Assets** > **All assets**.</span></span>

2. <span data-ttu-id="4adc1-125">Á listanum **Eignir** velurðu eignina sem þú vilt prenta bilanaskýrslu fyrir.</span><span class="sxs-lookup"><span data-stu-id="4adc1-125">In the **Assets** list, select the asset for which you want to print a fault report.</span></span>

3. <span data-ttu-id="4adc1-126">Á flipanum **Almennt** > **Skýrsluhluti** smellirðu á **Bilun eigna**.</span><span class="sxs-lookup"><span data-stu-id="4adc1-126">On the **General** tab > **Reports section**, click **Asset fault**.</span></span>

4. <span data-ttu-id="4adc1-127">Settu inn ákveðið tímabil eða veldu bilanagerð.</span><span class="sxs-lookup"><span data-stu-id="4adc1-127">Insert a specific period, or select a fault type.</span></span>

5. <span data-ttu-id="4adc1-128">Smelltu á **Í lagi** til að prenta skýrsluna.</span><span class="sxs-lookup"><span data-stu-id="4adc1-128">Click **OK** to print the report.</span></span>

>[!NOTE]
><span data-ttu-id="4adc1-129">Þú getur líka prentað bilanaskýrslu fyrir nokkrar eignir eða eignagerðir með því að smella á **Eignastýringu** > **Skýrslur** > **Eignir** > **Bilun eigna**.</span><span class="sxs-lookup"><span data-stu-id="4adc1-129">You can also print a fault report for several assets or asset types by clicking **Asset management** > **Reports** > **Assets** > **Asset fault**.</span></span>

