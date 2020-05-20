---
title: Stofna spárlíkön fyrir fjárhagsáætlanir verks
description: Í þessu efnisatriði er lýst hvernig á að stofna spárlíkön og eftirstöðvar fjárhagsáætlunar.
author: RadhikaRS
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 07e540f23a668b40a54906a67d87552fe991825a
ms.sourcegitcommit: 5de75c61c33e57c813944f1ab6100aceb020d432
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/29/2020
ms.locfileid: "3321780"
---
# <a name="create-forecast-models-for-project-budgets"></a><span data-ttu-id="bc91e-103">Stofna spárlíkön fyrir fjárhagsáætlanir verks</span><span class="sxs-lookup"><span data-stu-id="bc91e-103">Create forecast models for project budgets</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bc91e-104">Í þessu efnisatriði er lýst hvernig á að stofna spárlíkön og eftirstöðvar fjárhagsáætlunar.</span><span class="sxs-lookup"><span data-stu-id="bc91e-104">This topic describes how to create a forecast model for remaining budgets.</span></span> <span data-ttu-id="bc91e-105">Verk sem er háð fjárhagsáætlunarstýringu notar tvær gerðir áætlana: upprunaleg og eftirstöðvar.</span><span class="sxs-lookup"><span data-stu-id="bc91e-105">A project that is subject to budget control uses two types of budgets: original and remaining.</span></span> <span data-ttu-id="bc91e-106">Þegar fjárhagsáætlun verks er stofnuð verður fyrst að tilgreina upprunalegu fjárhagsáætlunina og spálíkön eftirstöðva fjárhagsáætlunar sem voru stofnaðar á síðunni **Spárlíkön**.</span><span class="sxs-lookup"><span data-stu-id="bc91e-106">When you create a project budget, you must specify the original and remaining budget forecast models that were created in the **Forecast models** page.</span></span> <span data-ttu-id="bc91e-107">Fjárhagsáætlanir verks sem byggjast á tilteknum líkönum eru stofnaðar þegar verkáætlun er staðfest.</span><span class="sxs-lookup"><span data-stu-id="bc91e-107">Project budgets based on the specified models are created when you commit the project budget.</span></span>

> [!NOTE]
> <span data-ttu-id="bc91e-108">Spárlíkan sem er notað fyrir fjárhagsáætlunarstýringu getur ekki haft undirlíkan og ekki er hægt að nota það sem undirlíkan.</span><span class="sxs-lookup"><span data-stu-id="bc91e-108">A forecast model that is used for budget control can’t have a submodel or be used as a submodel.</span></span>

1. <span data-ttu-id="bc91e-109">Veljið **Verkefnastjórnun og bókhald** > **Uppsetning** > **Spár**  > **Spárlíkön**.</span><span class="sxs-lookup"><span data-stu-id="bc91e-109">Select **Project management and accounting** > **Setup** > **Forecasts**  > **Forecast models**.</span></span>
2. <span data-ttu-id="bc91e-110">Veldu **Nýtt** til að stofna nýtt spárlíkan og færðu inn kenninúmer líkans og heiti þess.</span><span class="sxs-lookup"><span data-stu-id="bc91e-110">Select **New** to create a new forecast model, and then enter a model ID number and name for the new model.</span></span> 
3. <span data-ttu-id="bc91e-111">Stilltu valkostinn **Stöðvað** á **Já** til að koma i veg fyrir breytingar á spárlínum fyrir spárlíkanið.</span><span class="sxs-lookup"><span data-stu-id="bc91e-111">Set the **Stopped** option to **Yes** to prevent any changes to the forecast lines for the forecast model.</span></span> 
4. <span data-ttu-id="bc91e-112">Ef spálínurnar sem líkanið tengist mynda sjóðsstreymisspá í fjárhagnum skal stilla **Telja með í sjóðsstreymisspám** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="bc91e-112">If the forecast lines that the model is associated with should generate cash flow forecasts in the general ledger, set **Include in Cash flow forecasts** to **Yes.**</span></span> 
5. <span data-ttu-id="bc91e-113">Til að nota verkdagsetningu sem reikningsdagsetningu skal stilla **Reikningsdagsetning í spá** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="bc91e-113">To use the project date as the invoice date, set **Forecast Invoice date** to **Yes**.</span></span> 
6. <span data-ttu-id="bc91e-114">Í **Gerð fjárhagsáætlunar** skal velja eina eftirfarandi líkanagerð:</span><span class="sxs-lookup"><span data-stu-id="bc91e-114">In the **Budget type** field, select one of the following model types:</span></span>

   - <span data-ttu-id="bc91e-115">**Upprunaleg fjárhagsáætlun**: Notið þetta fyrir upprunalegar upphæðir áætlana sem hefur verið ráðstafað þegar upphaflega fjárhagsáætlunin er stofnuð og samþykkt.</span><span class="sxs-lookup"><span data-stu-id="bc91e-115">**Original budget**: Use the original budget amounts that are committed when the initial budget is created and approved.</span></span>
   - <span data-ttu-id="bc91e-116">**Eftirstöðvar fjárhagsáætlunar**: Notið þetta fyrir upphæðir eftirstöðvar fjárhagsáætlunar á líftíma verksins.</span><span class="sxs-lookup"><span data-stu-id="bc91e-116">**Remaining budget**: Use the remaining budget amounts during the life of the project.</span></span> <span data-ttu-id="bc91e-117">Staðan í þessu spárlíkani er lækkuð með raunverulegum færslum og aukin eða minnkuð með endurskoðun fjárhagsáætlunar.</span><span class="sxs-lookup"><span data-stu-id="bc91e-117">The balances in this forecast model are reduced by actual transactions and increased or decreased by budget revisions.</span></span>
   - <span data-ttu-id="bc91e-118">**Yfirfæra**: Nota upphæð fjárhagsáætlunar frá fyrra tímabili fyrir verkið.</span><span class="sxs-lookup"><span data-stu-id="bc91e-118">**Carry-forward**: Use the carry-forward budget amounts for the project.</span></span> <span data-ttu-id="bc91e-119">Yfirfærsla er valfrjálst ferli sem hægt er að keyra til að flytja ónotaðar upphæðir fjárhagsáætlana frá einu fjárhagsári til annars.</span><span class="sxs-lookup"><span data-stu-id="bc91e-119">Carry-forward is an optional process that can be run to transfer unused budget amounts from one fiscal year to another.</span></span>

7. <span data-ttu-id="bc91e-120">Stillið eftirfarandi valmöguleika eins og krafist er:</span><span class="sxs-lookup"><span data-stu-id="bc91e-120">Set the following options as required:</span></span>

   - <span data-ttu-id="bc91e-121">Virkið **Reikningsdagsetning í spá** til að nota dagsetningu verksins sem dagsetningu reiknings.</span><span class="sxs-lookup"><span data-stu-id="bc91e-121">Enable **Forecast invoice date** to use the project date as the invoice date.</span></span>
   - <span data-ttu-id="bc91e-122">Virkjaðu **Spá með VÍV** til að spá með verkum í vinnslu (VÍV) og velja svo VÍV-gerðina.</span><span class="sxs-lookup"><span data-stu-id="bc91e-122">Enable **Forecast with WIP** to forecast based on work in progress (WIP), and then select the type of WIP.</span></span> 
   - <span data-ttu-id="bc91e-123">Hægt er að halda sjálfgefinni **Gerð fjárhagsáætlunar** sem **Engin** eða slá inn nýja gerð.</span><span class="sxs-lookup"><span data-stu-id="bc91e-123">You can keep the default **Budget type** as **None** or enter a new type.</span></span> <span data-ttu-id="bc91e-124">Ekki er hægt að breyta gerð fjárhagsáætlunar eftir að færslu er breytt.</span><span class="sxs-lookup"><span data-stu-id="bc91e-124">The budget type can't be changed after you change a record.</span></span>     
    > [!NOTE]
    > <span data-ttu-id="bc91e-125">Ef sjálfgefinni fjárhagsáætlunargerð er breytt verða allir aðrir valmöguleikar óaðgengilegir fyrir uppfærslur og ekki er hægt að endurnýta spárlíkanið.</span><span class="sxs-lookup"><span data-stu-id="bc91e-125">If you change the default budget type, all other options will become unavailable for updates, and you can't reuse this forecast model.</span></span> 
   


 

