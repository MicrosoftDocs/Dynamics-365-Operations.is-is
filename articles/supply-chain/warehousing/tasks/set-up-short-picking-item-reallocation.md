---
title: Setja upp endurúthlutun fyrir stutta vörutiltekt
description: Í þessu efnisatriði er sýnt hvernig á að gera starfsmönnum vöruhúss kleift að finna aðrar staðsetningar á fljótlegan hátt ef ekki eru nægar birgðir á staðsetningunni sem þeim var vísað á.
author: ShylaThompson
manager: tfehr
ms.date: 06/29/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkException, WHSWorker, WHSLocationWithWorkException
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4e8f5c23f82e96145f411ec993f766a90137b5b8
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4015965"
---
# <a name="set-up-short-picking-item-reallocation"></a><span data-ttu-id="35b6d-103">Setja upp endurúthlutun fyrir stutta vörutiltekt</span><span class="sxs-lookup"><span data-stu-id="35b6d-103">Set up short picking item reallocation</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="35b6d-104">Þessi verklýsing sýnir hvernig starfsmenn vöruhúss geta fundið aðrar staðsetningar fljótt ef það eru ekki nægilegar birgðir á staðsetningunni þangað sem þeim var beint.</span><span class="sxs-lookup"><span data-stu-id="35b6d-104">This procedure shows how to enable warehouse workers to quickly find alternative locations if there isn’t sufficient inventory at the location they’ve been directed to.</span></span> 

<span data-ttu-id="35b6d-105">Endurúthlutunarferlinu er stjórnað af **Vinnuundantekningu** og notað af **starfsmanni** vöruhúss.</span><span class="sxs-lookup"><span data-stu-id="35b6d-105">The reallocation process is controlled by a **Work exception** and used by the warehouse **worker.**</span></span>

<span data-ttu-id="35b6d-106">Mögulegt er að nota sjálfvirka, handvirka eða bæði endurúthlutunarferlin:</span><span class="sxs-lookup"><span data-stu-id="35b6d-106">It is possible to use Automatic, Manual, or both reallocation processes:</span></span>

- <span data-ttu-id="35b6d-107">Sjálfvirk endurúthlutun - Staðsetningarleiðbeiningar eru notaðar til að ákvarða hvort vörur eru tiltækar á annarri staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="35b6d-107">Automatic reallocation - Location directives are used to determine if the goods are available at another location.</span></span> <span data-ttu-id="35b6d-108">Ef það er hægt verður vinnan uppfærð og notanda vöruhúss verður vísað á hina staðsetninguna.</span><span class="sxs-lookup"><span data-stu-id="35b6d-108">If possible, the work will be updated and the warehouse user will be directed to the alternative location.</span></span>
- <span data-ttu-id="35b6d-109">Handvirk endurúthlutun - Gerir notanda vöruhúss kleift að velja úr einni eða fleiri staðsetningum með ófráteknu magni af vörum.</span><span class="sxs-lookup"><span data-stu-id="35b6d-109">Manual reallocation - Allows the warehouse user to select from one or more locations with unreserved quantities of goods.</span></span> 
- <span data-ttu-id="35b6d-110">Sjálfvirkt og handvirkt - Ef kerfið getur ekki framkvæmt sjálfvirka endurúthlutun og staðsetningar eru tiltækar fyrir ófrátekið magn, verður notandinn beðinn um að velja staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="35b6d-110">Automatic and manual - If the system is unable to perform an automatic reallocation, and locations are available with unreserved quantities, the user will be prompted to select a location.</span></span>

## <a name="set-up-work-exceptions"></a><span data-ttu-id="35b6d-111">Setja upp vinnuundantekningar</span><span class="sxs-lookup"><span data-stu-id="35b6d-111">Set up work exceptions</span></span>
<span data-ttu-id="35b6d-112">Það er hægt að skilgreina margar vinnuundantekningar ásamt mismunandi endurúthlutunarreglum til að gera starfsmaður í vöruhúsi mögulegt að velja eitt á grundvelli þess sem sendingin sem verið er að vinna þarf.</span><span class="sxs-lookup"><span data-stu-id="35b6d-112">It's possible to define several work exceptions with different item reallocation policies to enable the warehouse worker to choose one based on the needs of the shipment that they are processing.</span></span>

<span data-ttu-id="35b6d-113">USMF sýniútgáfu fyrirtækis notað til að stofna þetta ferli.</span><span class="sxs-lookup"><span data-stu-id="35b6d-113">The USMF demo data company was used to create this procedure.</span></span>

1. <span data-ttu-id="35b6d-114">Í **Skoðunarrúðu** ferðu í **Vöruhúsakerfi > Uppsetning > Vinna > Undantekningar verks**.</span><span class="sxs-lookup"><span data-stu-id="35b6d-114">In the **Navigation pane** , go to **Warehouse management > Setup > Work > Work exceptions**.</span></span>
2. <span data-ttu-id="35b6d-115">Smelltu á **Nýtt**</span><span class="sxs-lookup"><span data-stu-id="35b6d-115">Click **New**</span></span> 
3. <span data-ttu-id="35b6d-116">Í reitinn **Kenni undantekningar verks** skaltu færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="35b6d-116">In the **Work exception code** field, type a value.</span></span> <span data-ttu-id="35b6d-117">Þetta verður titill þessarar undantekningar.</span><span class="sxs-lookup"><span data-stu-id="35b6d-117">This will be the title of this exception .</span></span> <span data-ttu-id="35b6d-118">Til dæmis, handbók fyrir of litla tiltekt.</span><span class="sxs-lookup"><span data-stu-id="35b6d-118">For example, Short picking manual.</span></span>
4. <span data-ttu-id="35b6d-119">Í reitinn **Lýsing** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="35b6d-119">In the **Description** field, type a value.</span></span> <span data-ttu-id="35b6d-120">Þetta verður stutt lýsing á notkun þessarar undantekningar.</span><span class="sxs-lookup"><span data-stu-id="35b6d-120">This will be a short description of the usage of this exception.</span></span> <span data-ttu-id="35b6d-121">Til dæmis, Of lítil tiltekt - vara ekki í boði.</span><span class="sxs-lookup"><span data-stu-id="35b6d-121">For example, Short picking - item not available.</span></span>
5. <span data-ttu-id="35b6d-122">Í reitnum **Undantekning** skal velja **Of lítil tiltekt**.</span><span class="sxs-lookup"><span data-stu-id="35b6d-122">In the **Exception** type field, select **Short pick**.</span></span>
6. <span data-ttu-id="35b6d-123">Veldu gátreitinn **Leiðrétta birgðir**.</span><span class="sxs-lookup"><span data-stu-id="35b6d-123">Select the **Adjust inventory** check box.</span></span> <span data-ttu-id="35b6d-124">Ef valinn, verða birgðir sjálfvirkt leiðréttar á 0 á staðsetningu þar sem tiltekt er of lítil.</span><span class="sxs-lookup"><span data-stu-id="35b6d-124">If selected, inventory will automatically be adjusted to 0 at the short picked location.</span></span>
7. <span data-ttu-id="35b6d-125">Í reitinn **Sjálfgefinn kóði leiðréttingargerðar** skal færa inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="35b6d-125">In the **Default adjustment type code** field, enter or select a value.</span></span> <span data-ttu-id="35b6d-126">Til dæmis í USMF er hægt að velja **Fjarlægja leiðrétta frátekt á útleið**. Hver kóði leiðréttingargerðar inniheldur fjóra eiginleika: heiti, lýsing, færslubókarheiti og **Fjarlægja frátekningar**.</span><span class="sxs-lookup"><span data-stu-id="35b6d-126">For example, in USMF you can select **Remove Res Adj Out**. Each Adjustment type code contains four characteristics: name, description, inventory journal name, and **Remove reservations**.</span></span> <span data-ttu-id="35b6d-127">Ef **Fjarlægja frátekningu** er virkjað verða frátekningar pöntunarlínu of lítillar tiltektar fjarlægðar.</span><span class="sxs-lookup"><span data-stu-id="35b6d-127">If **Remove reservations** is enabled, the short-picked order line's reservations will be removed.</span></span>  
8. <span data-ttu-id="35b6d-128">Í reitnum **Endurúthlutun vöru** skal velja gildi, t.d. handvirkt.</span><span class="sxs-lookup"><span data-stu-id="35b6d-128">In the **Item reallocation** field, select a value, such as Manual.</span></span> <span data-ttu-id="35b6d-129">Ef valið er Handvirkt, eða Sjálfvirkar og Handvirkar, þarf starfsmaður í vöruhúsi að geta notað handvirka endurúthlutun.</span><span class="sxs-lookup"><span data-stu-id="35b6d-129">If you select Manual, or Automatic and Manual, the warehouse worker needs to be enabled to use manual reallocation.</span></span>

## <a name="set-up-a-worker-to-use-manual-item-reallocation"></a><span data-ttu-id="35b6d-130">Setja upp starfsmann til að nota handvirka endurúthlutun vöru</span><span class="sxs-lookup"><span data-stu-id="35b6d-130">Set up a worker to use manual item reallocation</span></span>

<span data-ttu-id="35b6d-131">USMF sýniútgáfu fyrirtækis notað til að stofna þetta ferli.</span><span class="sxs-lookup"><span data-stu-id="35b6d-131">The USMF demo data company was used to create this procedure.</span></span>

1. <span data-ttu-id="35b6d-132">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="35b6d-132">Close the page.</span></span>
2. <span data-ttu-id="35b6d-133">Í **Skoðunarrúðu** ferðu í **Vöruhúsakerfi > Uppsetning > Vinna > Starfskraftur**.</span><span class="sxs-lookup"><span data-stu-id="35b6d-133">In the **Navigation pane** , go to **Warehouse management > Setup > Worker**.</span></span>
3. <span data-ttu-id="35b6d-134">Smellið á **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="35b6d-134">Click **Edit**.</span></span>
4. <span data-ttu-id="35b6d-135">Í listanum skal velja starfskraft.</span><span class="sxs-lookup"><span data-stu-id="35b6d-135">In the list, select worker.</span></span> <span data-ttu-id="35b6d-136">Til dæmis Julia Funderburk.</span><span class="sxs-lookup"><span data-stu-id="35b6d-136">For example, Julia Funderburk.</span></span>
5. <span data-ttu-id="35b6d-137">Stækkið flýtiflipann **Notendur**.</span><span class="sxs-lookup"><span data-stu-id="35b6d-137">Expand the **Users** FastTab.</span></span>
6. <span data-ttu-id="35b6d-138">Í listanum skal velja **Notandakenni**.</span><span class="sxs-lookup"><span data-stu-id="35b6d-138">In the list, select a **User ID**.</span></span> <span data-ttu-id="35b6d-139">Til dæmis 24.</span><span class="sxs-lookup"><span data-stu-id="35b6d-139">For example, 24.</span></span>
7. <span data-ttu-id="35b6d-140">Stækkið flýtiflipann **Verk**.</span><span class="sxs-lookup"><span data-stu-id="35b6d-140">Expand the **Work** FastTab.</span></span>
8. <span data-ttu-id="35b6d-141">Velja skal **Já** í svæðinu **Leyfa handvirka endurúthlutun vöru**.</span><span class="sxs-lookup"><span data-stu-id="35b6d-141">Select **Yes** in the **Allow manual item reallocation** field.</span></span>
