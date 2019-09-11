---
title: Stjórnun vinnustunda
description: Þetta efni útskýrir stjórnun vinnustunda í eignastýringu.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
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
ms.openlocfilehash: 916e7b8d5d494dbae0659504957f7f0798a6834b
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918373"
---
# <a name="work-hour-control"></a><span data-ttu-id="57b5a-103">Stjórnun vinnustunda</span><span class="sxs-lookup"><span data-stu-id="57b5a-103">Work hour control</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="57b5a-104">Í eignastýringu er hægt að reikna út stundir til að fá yfirlit yfir raunverulegar stundir miðað við áætlaðar stundir á eignum, virkum staðsetningum eða verkbeiðnum.</span><span class="sxs-lookup"><span data-stu-id="57b5a-104">In Asset Management, you can calculate hours to get an overview of actual hours compared to budget hours on assets, functional locations, or work orders.</span></span> <span data-ttu-id="57b5a-105">Raunstundir byggjast á bókfærðum færslum.</span><span class="sxs-lookup"><span data-stu-id="57b5a-105">Actual hours are based on posted transactions.</span></span>

## <a name="work-hour-control-for-assets-functional-locations-and-work-orders"></a><span data-ttu-id="57b5a-106">Stjórnun vinnustunda á eignum, virkum staðssetningum og verkbeiðnum</span><span class="sxs-lookup"><span data-stu-id="57b5a-106">Work hour control for assets, functional locations, and work orders</span></span>

<span data-ttu-id="57b5a-107">Útreikningar á eignum, starfrænum stöðum og vinnupöntunum eru nánast eins.</span><span class="sxs-lookup"><span data-stu-id="57b5a-107">The calculations made for assets, functional locations, and work orders are almost identical.</span></span> <span data-ttu-id="57b5a-108">Eini munurinn er sá að fyrir eignir og virkar staðsetningar geturðu einnig haft undireignir og undirstaði með í útreikningum.</span><span class="sxs-lookup"><span data-stu-id="57b5a-108">Only difference is that for assets and functional locations, you can also include sub assets and sub locations in your calculation.</span></span> <span data-ttu-id="57b5a-109">Dagsetningin er færsludagsetningin þegar skráningin var skráð.</span><span class="sxs-lookup"><span data-stu-id="57b5a-109">The date is the transaction date when the registration was recorded.</span></span>

1. <span data-ttu-id="57b5a-110">Smelltu á **Eignastýringu** > **Fyrirspurnir** > **Eignir** > **Stjórnun eignastunda** eða **Vinnustundastjórnun virkra staðsetninga**, eða **Eignastýring** > **Fyrirspurnir** > **Verkbeiðnir** > **Vinnustundastjórnun verkbeiðni**.</span><span class="sxs-lookup"><span data-stu-id="57b5a-110">Click **Asset management** > **Inquiries** > **Assets** > **Asset hour control** or **Functional location hour control**, or **Asset management** > **Inquiries** > **Work orders** > **Work order hour control**.</span></span>

2. <span data-ttu-id="57b5a-111">Í valmyndinni **Vinnustundastjórnun eigna**, .</span><span class="sxs-lookup"><span data-stu-id="57b5a-111">In the **Asset hour control** dialog, .</span></span>

3. <span data-ttu-id="57b5a-112">Í glugganum **Stjórnun eignastunda** / **Stjórnun stunda virka staðsetninga** / **Stjórnun stunda verkbeiðni** velurðu tímabil sem á að reikna út í reitunum **Frá dagsetningu** og **Til dags.**.</span><span class="sxs-lookup"><span data-stu-id="57b5a-112">In the **Asset hour control** / **Functional location hour control** / **Work order hour control** dialog, select a period to be calculated in the **From date** and **To date** fields.</span></span>

4. <span data-ttu-id="57b5a-113">Ef þörf krefur velurðu **Sett fjárhagsvídda** sem sett er inn í útreikninginn.</span><span class="sxs-lookup"><span data-stu-id="57b5a-113">If required, select a **Financial dimension set** to be included in the calculation.</span></span>

5. <span data-ttu-id="57b5a-114">Veldu „Já“ á skiptihnappnum **Sleppa núlli** ef þú vilt ekki sýna niðurstöður með núlltímum.</span><span class="sxs-lookup"><span data-stu-id="57b5a-114">Select "Yes" on the **Skip zero** toggle button if you don't want to show results containing zero hours.</span></span>

6. <span data-ttu-id="57b5a-115">Þú getur notað reitinn **Stig** til að gefa til kynna hversu ítarlegar þú vilt að stjórnunarlínur stunda séu varðandi virkar staðsetningar.</span><span class="sxs-lookup"><span data-stu-id="57b5a-115">You can use the **Level** field to indicate how detailed you want the hour control lines to be regarding functional locations.</span></span> <span data-ttu-id="57b5a-116">Til dæmis, ef þú setur inn töluna "1" í reitinn, og þú ert með fjölþrepa skipulag virkrar staðsetningar, verða allar stjórnunarlínur stunda fyrir virka staðsetningu sýndar á efsta stigi og því er hægt að leggja saman klukkustundirnar á línu frá virkum staðsetningum á lægra stigi.</span><span class="sxs-lookup"><span data-stu-id="57b5a-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location hierarchy, all hour control lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="57b5a-117">Ef þú setur töluna „0“ inn í reitinn **Stig** muntu sjá ítarlega niðurstöður sem sýna allar stjórnunarlínur stunda á öllum virkum staðsetningarstigum sem þær tengjast.</span><span class="sxs-lookup"><span data-stu-id="57b5a-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all hour control lines on all the functional location levels to which they are related.</span></span>

7. <span data-ttu-id="57b5a-118">Veldu „Já“ á skiptihnappnuum **Hafa undireignir með** til að sýna kostnað sem tengist undireignum sem aðskildar línur.</span><span class="sxs-lookup"><span data-stu-id="57b5a-118">Select "Yes" on the **Include sub assets** toggle button to show costs related to sub assets as separate lines.</span></span>

8. <span data-ttu-id="57b5a-119">Ef þú vilt takmarka leitina geturðu valið sérstakar eignir / virkar staðsetningar / verkbeiðnum á flýtiflipanum **Færslur til að taka með**.</span><span class="sxs-lookup"><span data-stu-id="57b5a-119">If you want to limit the search, you can select specific assets / functional locations / work orders on the **Records to include** FastTab.</span></span>

9. <span data-ttu-id="57b5a-120">Smellið á **Í lagi** til að byrja að reikna.</span><span class="sxs-lookup"><span data-stu-id="57b5a-120">Click **OK** to start the calculation.</span></span>

10. <span data-ttu-id="57b5a-121">Á síðunni **Stjórnun eignastunda**, í aðgerðagluggahópunum **Flokka eftir...**, smellirðu á viðeigandi hnappa til að sýna umbeðið upplýsingastig útreiknings.</span><span class="sxs-lookup"><span data-stu-id="57b5a-121">On the **Asset hour control** page, in the **Group by...** action pane groups, click the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="57b5a-122">Valdir aðgerðarrúðahnappar eru auðkenndir.</span><span class="sxs-lookup"><span data-stu-id="57b5a-122">The selected action pane buttons are highlighted.</span></span> <span data-ttu-id="57b5a-123">Smelltu á hnappinn til að virkjaðu eða afvirkjaðu hann.</span><span class="sxs-lookup"><span data-stu-id="57b5a-123">Click on a button to activate or deactivate it.</span></span>

<span data-ttu-id="57b5a-124">Myndin hér að neðan sýnir dæmi um útreikning á **Stjórnun eignastunda**.</span><span class="sxs-lookup"><span data-stu-id="57b5a-124">The figure below shows an example of an **Asset hour control** calculation.</span></span>

![Mynd 1](media/04-controlling-and-reporting.png)

<span data-ttu-id="57b5a-126">Önnur leið til að gera stundaútreikning er að velja margar eignir í **Allar eignir** eða **Virkar eignir**.</span><span class="sxs-lookup"><span data-stu-id="57b5a-126">Another way of making an hour calculation is to multi-select assets in **All assets** or **Active assets**.</span></span> <span data-ttu-id="57b5a-127">Smelltu síðan á hnappinn **Stundastjórnun** á flýtiflipanum **Almennt**.</span><span class="sxs-lookup"><span data-stu-id="57b5a-127">Then, you click the **Hour control** button on the **General** FastTab.</span></span> <span data-ttu-id="57b5a-128">Valdar eignir eru sjálfkrafa settar inn í reitnum **Eignir** á flýtiflipanum **Færslur til að taka með**.</span><span class="sxs-lookup"><span data-stu-id="57b5a-128">The selected assets are automatically inserted in the **Asset** field on the **Records to include** FastTab.</span></span> <span data-ttu-id="57b5a-129">Smelltu á **Í lagi** í glugganum **Stjórnun eignastunda** og útreikningur fyrir valdar eignir er sýndur.</span><span class="sxs-lookup"><span data-stu-id="57b5a-129">Click **OK** in the **Asset hour control** dialog, and the calculation for the selected assets is shown.</span></span> <span data-ttu-id="57b5a-130">Sama ferli er hægt að gera fyrir virkar staðsetningar í **Allar virkar staðsetningar** eða **Virkar virkar staðsetningar**, og vegna verkbeiðna í **Allar verkbeiðnir** eða **Virkar vinnupantanir**.</span><span class="sxs-lookup"><span data-stu-id="57b5a-130">The same procedure can be done for functional locations in **All functional locations** or **Active functional locations**, and for work orders in **All work orders** or **Active work orders**.</span></span>

>[!NOTE]
><span data-ttu-id="57b5a-131">Reiturinn **Upprunaleg fjárhagsáætlun** sýnir fjárhagsáætlunarstundir frá spá um verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="57b5a-131">The **Original budget** field shows budget hours from the work order forecast.</span></span> <span data-ttu-id="57b5a-132">Reiturinn **Raunverulegar stundir** sýnir bókaðar stundir vegna verkbeiðna.</span><span class="sxs-lookup"><span data-stu-id="57b5a-132">The **Actual hours** field shows posted hours on work orders.</span></span> <span data-ttu-id="57b5a-133">Reiturinn **Ráðstafaðar stundir** sýnir heildarmagn stunda sem fyrirtækið þitt skuldbindur sig til vegna verkbeiðna.</span><span class="sxs-lookup"><span data-stu-id="57b5a-133">The **Committed hours** field shows total amount of hours that your company is committed to in relation to work orders.</span></span>

