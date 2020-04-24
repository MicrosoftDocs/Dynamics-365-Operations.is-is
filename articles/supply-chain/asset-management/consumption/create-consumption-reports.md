---
title: Stofna notkunarskýrslur
description: Þetta efni útskýrir hvernig á að stofna notkunarskýrslur í eignastjórnun.
author: josaw1
manager: tfehr
ms.date: 08/21/2019
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
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d28acbccc35b3f59f9cca7236dd721a1d9bdead8
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216437"
---
# <a name="create-consumption-reports"></a><span data-ttu-id="07732-103">Stofna notkunarskýrslur</span><span class="sxs-lookup"><span data-stu-id="07732-103">Create consumption reports</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="07732-104">Þegar þú hefur búið til og sent notkunarskráningar í verkbeiðnum í eignastýringu eru tvær skýrslur tiltækar til að birta notkunarupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="07732-104">When you've created and posted consumption registrations on work orders in Asset Management, two reports are available to display consumption details.</span></span>


## <a name="asset-consumption-report"></a><span data-ttu-id="07732-105">Eignanotkunarskýrsla</span><span class="sxs-lookup"><span data-stu-id="07732-105">Asset consumption report</span></span>

<span data-ttu-id="07732-106">Þegar þú hefur bókað notkun á verkbeiðnir geturðu prentað eignanotkunarskýrslu.</span><span class="sxs-lookup"><span data-stu-id="07732-106">When you have posted consumption on work orders, you can print an asset consumption report.</span></span> <span data-ttu-id="07732-107">Skýrslan sýnir klukkustundir, tímakostnað, vörukostnað og útgjöld sem er bókaður á eignir.</span><span class="sxs-lookup"><span data-stu-id="07732-107">The report displays hours, hour costs, item costs, and expenses posted on assets.</span></span>

1. <span data-ttu-id="07732-108">Smelltu á **Eignastýringu** > **Skýrslur** > **Eignir** > **Eignanotkun**.</span><span class="sxs-lookup"><span data-stu-id="07732-108">Click **Asset management** > **Reports** > **Assets** > **Asset consumption**.</span></span>

2. <span data-ttu-id="07732-109">Í glugganum **Eignanotkun** velurðu færibreytu- og upplýsingastig sem þú vilt sjá með því að velja **Já** á viðeigandi skiptihnöppum og setja inn virkt staðsetningarstig í kaflanum **Sýna**.</span><span class="sxs-lookup"><span data-stu-id="07732-109">In the **Asset consumption** dialog, select the parameters and detail level you want to see by selecting **Yes** on the relevant toggle buttons, and inserting a functional location level in the **Show** section.</span></span>
    - <span data-ttu-id="07732-110">Þú getur notað reitinn **Stig** til að gefa til kynna hversu ítarlegar þú vilt að eignalínur séu varðandi virkar staðsetningar.</span><span class="sxs-lookup"><span data-stu-id="07732-110">You can use the **Levels** field to indicate how detailed you want the asset lines to be regarding functional locations.</span></span> 
    
        <span data-ttu-id="07732-111">Til dæmis, ef þú setur inn töluna „1“ í reitinn, og þú ert með fjölþrepa skipulag virkra staðsetninga, verða allar eignir fyrir virka staðsetningu sýndar á efsta stigi og því er hægt að bæta línu við af virkum staðsetningum sem eru staðsettar á lægra stigi.</span><span class="sxs-lookup"><span data-stu-id="07732-111">For example, if you enter the number "1" in the field, and you have a multi-level functional location structure, all assets for a functional location will be shown on the top level, and therefore a line may be added up from functional locations located at a lower level.</span></span> 
        
        <span data-ttu-id="07732-112">Ef þú setur töluna „0“ inn í reitinn **Stig** muntu sjá ítarlega niðurstöður sem sýna allar eignalínur á öllum virkum staðsetningarstigum sem þær tengjast.</span><span class="sxs-lookup"><span data-stu-id="07732-112">If you enter the number "0" in the **Levels** field, you will see a detailed result showing all assets on all the functional location levels to which they are related.</span></span> 
        
    - <span data-ttu-id="07732-113">Veldu **Já** á skiptihnappnum **Summa á öllum undireignum** til að sjá fjárhæðir fyrir hverja undireign í skýrslunni.</span><span class="sxs-lookup"><span data-stu-id="07732-113">Select **Yes** on the **Sum on all sub assets** toggle button to see sums for each sub asset in the report.</span></span>

3. <span data-ttu-id="07732-114">Veldu dagsetningartíma í kaflanum **Dagsetningar**.</span><span class="sxs-lookup"><span data-stu-id="07732-114">Select a date interval in the **Dates** section.</span></span>

4. <span data-ttu-id="07732-115">Á flýtiflipanum **Áfangastaður** skaltu velja hvort þú vilt birta skýrsluna á skjánum, prenta hana eða vista hana sem skrá eða tölvupóst.</span><span class="sxs-lookup"><span data-stu-id="07732-115">On the **Destination** FastTab, select if you want to display the report on screen, print it, or save it as a file or email.</span></span>

5. <span data-ttu-id="07732-116">Ef þess er krafist geturðu valið sérstakar eignir sem birtast í skýrslunni.</span><span class="sxs-lookup"><span data-stu-id="07732-116">If required, you can select specific assets to be displayed in the report.</span></span> <span data-ttu-id="07732-117">Á flýtiflipanum **Færslur til að hafa með** smellirðu á **Sía** og bætir við eignunum sem þú vilt hafa með í skýrslunni.</span><span class="sxs-lookup"><span data-stu-id="07732-117">On the **Records to include** FastTab, click **Filter**, and add the assets you want to include in the report.</span></span>

6. <span data-ttu-id="07732-118">Smellið á **Í lagi** til að stofna skýrsluna.</span><span class="sxs-lookup"><span data-stu-id="07732-118">Click **OK** to generate the report.</span></span>


## <a name="work-order-consumption-report"></a><span data-ttu-id="07732-119">Notkunarskýrsla verkbeiðni</span><span class="sxs-lookup"><span data-stu-id="07732-119">Work order consumption report</span></span>

<span data-ttu-id="07732-120">Þegar þú hefur bókað notkun á verkbeiðnir geturðu prentað notkunarskýrslu verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="07732-120">When you have posted consumption on work orders, you can print a work order consumption report.</span></span> <span data-ttu-id="07732-121">Skýrslan sýnir klukkustundir, tímakostnað, vörukostnað og útgjöld sem er bókaður á verkbeiðnir.</span><span class="sxs-lookup"><span data-stu-id="07732-121">The report displays hours, hour costs, item costs, and expenses posted on work orders.</span></span>

1. <span data-ttu-id="07732-122">Smelltu á **Eignastýring** > **Skýrslur** > **Verkbeiðnir** > **Notkun verkbeiðni**.</span><span class="sxs-lookup"><span data-stu-id="07732-122">Click **Asset management** > **Reports** > **Work orders** > **Work order consumption**.</span></span>

2. <span data-ttu-id="07732-123">Í glugganum **Notkun verkbeiðni** velurðu þær færibreytur sem þú vilt láta fylgja með í skýrslunni með því að velja **Já** á viðeigandi skiptihnöppum í kaflanum **Sýna**.</span><span class="sxs-lookup"><span data-stu-id="07732-123">In the **Work order consumption** dialog, select the parameters you want to include in the report by selecting **Yes** on the relevant toggle buttons in the **Show** section.</span></span>

3. <span data-ttu-id="07732-124">Veldu dagsetningartíma í kaflanum **Dagsetningar**.</span><span class="sxs-lookup"><span data-stu-id="07732-124">Select a date interval in the **Dates** section.</span></span>

4. <span data-ttu-id="07732-125">Á flýtiflipanum **Áfangastaður** skaltu velja hvort þú vilt birta skýrsluna á skjánum, prenta hana eða vista hana sem skrá eða tölvupóst.</span><span class="sxs-lookup"><span data-stu-id="07732-125">On the **Destination** FastTab, select if you want to display the report on screen, print it, or save it as a file or email.</span></span>

5. <span data-ttu-id="07732-126">Ef þess er krafist geturðu valið sérstakar verkbeiðnir sem birtast í skýrslunni.</span><span class="sxs-lookup"><span data-stu-id="07732-126">If required, you can select specific work orders to be displayed in the report.</span></span> <span data-ttu-id="07732-127">Á flýtiflipanum **Færslur til að hafa með** smellirðu á **Sía** og bætir við verkbeiðnunum sem þú vilt hafa með í skýrslunni.</span><span class="sxs-lookup"><span data-stu-id="07732-127">On the **Records to include** FastTab, click **Filter**, and add the work orders you want to include in the report.</span></span>

6. <span data-ttu-id="07732-128">Smellið á **Í lagi** til að stofna skýrsluna.</span><span class="sxs-lookup"><span data-stu-id="07732-128">Click **OK** to generate the report.</span></span>


>[!NOTE]
><span data-ttu-id="07732-129">Þú getur líka búið til [verkbeiðnaskýrslu](../work-orders/work-order-report.md), sem inniheldur fleiri upplýsingar um verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="07732-129">You can also generate a [work order report](../work-orders/work-order-report.md), which contains more work order details.</span></span>

