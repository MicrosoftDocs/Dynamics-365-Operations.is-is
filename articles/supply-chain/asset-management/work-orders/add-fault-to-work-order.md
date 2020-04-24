---
title: Bættu bilun við verkbeiðnina
description: Þetta efni lýsir því hvernig bæta má bilanaskráningum við verkbeiðnir í eignastýringu.
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
ms.openlocfilehash: e82026f1d73e7368d93109bc0b895b7368ac84d4
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215195"
---
# <a name="add-fault-to-work-order"></a><span data-ttu-id="60720-103">Bæta villu við verkbeiðni</span><span class="sxs-lookup"><span data-stu-id="60720-103">Add fault to work order</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="60720-104">Þú getur bætt bilunum sem voru settar upp í bilunarhönnuðinni við verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="60720-104">You can add faults that were set up in the fault designer to a work order.</span></span> <span data-ttu-id="60720-105">Ein eða fleiri bilanaskrár verða að vera tengdar eignagerðunum sem eru notaðar fyrir eignina sem er valin í verkbeiðninni.</span><span class="sxs-lookup"><span data-stu-id="60720-105">One or more fault records must be connected to the asset types that are used for the asset that is selected in the work order.</span></span> <span data-ttu-id="60720-106">Nánari upplýsingar um uppsetninguna er að finna í [Villustjórnun](../setup-for-work-orders/fault-management.md).</span><span class="sxs-lookup"><span data-stu-id="60720-106">For more information about the setup, see [Fault management](../setup-for-work-orders/fault-management.md).</span></span>

1. <span data-ttu-id="60720-107">Veldu **Eignastýringu** > **Sameiginlegt** > **Verkbeiðnir** > **Allar verkbeiðnir** eða **Virkar verkbeiðnir**.</span><span class="sxs-lookup"><span data-stu-id="60720-107">Select **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="60720-108">Veldu verkbeiðnina til að skrá bilun á og síðan í aðgerðarglugganum á flipanum **Verkbeiðni**, í hópnum **Eignir**, velurðu **Bilun eignar**.</span><span class="sxs-lookup"><span data-stu-id="60720-108">Select the work order to make a fault registration on, and then, on the Action Pane, on the **Work order** tab, in the **Asset** group, select **Asset fault**.</span></span>

3. <span data-ttu-id="60720-109">Á flýtiflipanum **Einkenni** velurðu **Bæta við línu**.</span><span class="sxs-lookup"><span data-stu-id="60720-109">On the **Symptoms** FastTab, select **Add line**.</span></span> <span data-ttu-id="60720-110">Raðnúmer fyrir bilun er sjálfkrafa skráð í reitinn **Bilun**.</span><span class="sxs-lookup"><span data-stu-id="60720-110">A sequential fault number is automatically entered in the **Fault** field.</span></span>

4. <span data-ttu-id="60720-111">Í reitnum **Bilunareinkenni** velurður viðeigandi einkenni.</span><span class="sxs-lookup"><span data-stu-id="60720-111">In the **Fault symptom** field, select the relevant symptom.</span></span>

5. <span data-ttu-id="60720-112">Í reitunum **Bilunarsvæði** og **Bilunartegund** velurðu viðeigandi gildi.</span><span class="sxs-lookup"><span data-stu-id="60720-112">In the **Fault area** and **Fault type** fields, select the appropriate values.</span></span>

6. <span data-ttu-id="60720-113">Í reitnum **Dagsetning bilunar** er núverandi dagsetning sjálfkrafa sett inn.</span><span class="sxs-lookup"><span data-stu-id="60720-113">In the **Fault date** field, the current date is automatically inserted.</span></span> <span data-ttu-id="60720-114">Þú getur valið aðra dagsetningu eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="60720-114">You can select a different date as you require.</span></span>

7. <span data-ttu-id="60720-115">Á flýtiflipanum **Orsakir fyrir valið einkenni** bætirðu við línu til að lýsa orsökum vandans.</span><span class="sxs-lookup"><span data-stu-id="60720-115">On the **Causes for selected symptom** FastTab, add a line to describe the cause of the issue.</span></span>

8. <span data-ttu-id="60720-116">Á flýtiflipanum **Úrræði fyrir valið einkenni** bætirðu við línu til að lýsa hugsanlegri lausn við vandanum.</span><span class="sxs-lookup"><span data-stu-id="60720-116">On the **Remedies for selected symptom** FastTab, add a line to describe a possible solution to the issue.</span></span>

9. <span data-ttu-id="60720-117">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="60720-117">Select **Save**.</span></span>

<span data-ttu-id="60720-118">Eftirfarandi skýringarmynd hér að neðan sýnir dæmi um bilanaskráningu.</span><span class="sxs-lookup"><span data-stu-id="60720-118">The illustration below shows an example of a fault registration.</span></span>

![Mynd 1](media/19-work-orders.png)


## <a name="view-asset-faults"></a><span data-ttu-id="60720-120">Skoða eignabilanir</span><span class="sxs-lookup"><span data-stu-id="60720-120">View asset faults</span></span>

<span data-ttu-id="60720-121">Í listanum **Eignabilanir** er hægt að fá yfirlit yfir allar bilanir sem eru skráðar á eignum.</span><span class="sxs-lookup"><span data-stu-id="60720-121">In the **Asset faults** list, you can get an overview of all faults registered on assets.</span></span>

<span data-ttu-id="60720-122">Á listasíðunni **Eignabilanir** er hægt að fá yfirlit yfir allar bilanir sem hafa verið skráðar á eignum.</span><span class="sxs-lookup"><span data-stu-id="60720-122">On the **Asset faults** list page, you can get an overview of all faults that have been registered on assets.</span></span> <span data-ttu-id="60720-123">Til að opna síðuna velurðu **Eignastýringu** > **Fyrirspurnir** > **Bilun eignar** > **Bilanir eigna**.</span><span class="sxs-lookup"><span data-stu-id="60720-123">To open the page, select **Asset management** > **Inquiries** > **Asset fault** > **Asset faults**.</span></span>


## <a name="print-asset-fault-report"></a><span data-ttu-id="60720-124">Prenta eignabilanaskýrslur</span><span class="sxs-lookup"><span data-stu-id="60720-124">Print asset fault report</span></span>

<span data-ttu-id="60720-125">Af listasíðunni **Allar eignir** er hægt að prenta eignabilanaskýrslu sem sýnir allar bilanaskráningar og myndrænt yfirlit yfir tölfræðilegar bilanir.</span><span class="sxs-lookup"><span data-stu-id="60720-125">From the **All assets** list page, you can print an asset fault report that shows all fault registrations and a graphical overview of fault statistics.</span></span>

1. <span data-ttu-id="60720-126">Veldu **Eignastýring** > **Sameiginlegt** > **Eignir** > **Allar eignir**.</span><span class="sxs-lookup"><span data-stu-id="60720-126">Select **Asset management** > **Common** > **Assets** > **All assets**.</span></span>

2. <span data-ttu-id="60720-127">Veldu eignina sem á að prenta bilanaskýrslu fyrir.</span><span class="sxs-lookup"><span data-stu-id="60720-127">Select the asset to print a fault report for.</span></span>

3. <span data-ttu-id="60720-128">Í Aðgerðasvæði, á flipanum **Almennt** í flokknum **Skýrslur** velurðu **Bilun eignar**.</span><span class="sxs-lookup"><span data-stu-id="60720-128">On the Action Pane, on the **General** tab, in the **Reports** group, select **Asset fault**.</span></span>

4. <span data-ttu-id="60720-129">Skráðu ákveðið tímabil eða veldu bilanagerð.</span><span class="sxs-lookup"><span data-stu-id="60720-129">Enter a specific period, or select a fault type.</span></span>

5. <span data-ttu-id="60720-130">Veldu **Í lagi** til að prenta skýrsluna.</span><span class="sxs-lookup"><span data-stu-id="60720-130">Select **OK** to print the report.</span></span>

>[!NOTE]
><span data-ttu-id="60720-131">Til að prenta bilanaskýrslu fyrir nokkrar eignir eða eignagerðir velurðu **Eignastýringu** > **Skýrslur** > **Eignir** > **Bilun eigna**.</span><span class="sxs-lookup"><span data-stu-id="60720-131">To print a fault report for several assets or asset types, select **Asset management** > **Reports** > **Assets** > **Asset fault**.</span></span>

