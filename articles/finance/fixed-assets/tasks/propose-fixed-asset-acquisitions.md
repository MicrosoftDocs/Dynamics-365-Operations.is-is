---
title: Stinga upp á eignakaupum
description: Þetta efni lýsir hvernig á að kaupa eignir með því að nota kauptillögu í færslubók eigna.
author: saraschi2
ms.date: 03/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d529cd53b41827a78b282afd4d2c69d2f2db555e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817168"
---
# <a name="propose-fixed-asset-acquisitions"></a><span data-ttu-id="c1b12-103">Stinga upp á eignakaupum</span><span class="sxs-lookup"><span data-stu-id="c1b12-103">Propose fixed asset acquisitions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c1b12-104">Þetta efni lýsir hvernig á að kaupa eignir með því að nota kauptillögu í færslubók eigna.</span><span class="sxs-lookup"><span data-stu-id="c1b12-104">This topic describes how to acquire a fixed asset using the acquisition proposal in the Fixed assets journal.</span></span> <span data-ttu-id="c1b12-105">Það notar Bókari hlutverk og sýnigögn fyrir USMF lögaðila.</span><span class="sxs-lookup"><span data-stu-id="c1b12-105">It uses the accountant role and demo data for the USMF legal entity.</span></span> <span data-ttu-id="c1b12-106">Til að komast yfir eign í gegnum tillögubók eignar, þarf fyrst að stofna eignafærsluna og síðan skilgreina kaupverð í eignabókinni.</span><span class="sxs-lookup"><span data-stu-id="c1b12-106">To acquire a fixed asset through a fixed asset proposal journal, you must first create the fixed asset record, and then define the acquisition price in the asset book.</span></span>

## <a name="create-an-asset-acquisition-proposal"></a><span data-ttu-id="c1b12-107">Stofna tillögu að eignakaupum</span><span class="sxs-lookup"><span data-stu-id="c1b12-107">Create an asset acquisition proposal</span></span>

<span data-ttu-id="c1b12-108">Ljúkið eftirfarandi skrefum til að búa til eignaskiptatillögu.</span><span class="sxs-lookup"><span data-stu-id="c1b12-108">Complete the following steps to create an asset acquisition proposal.</span></span> 

1. <span data-ttu-id="c1b12-109">Í skoðunarrúðnni ferðu í **Kerfseiningar > Fastafjármunir > Dagbókarfærslur > Dagbók fastafjármuna**.</span><span class="sxs-lookup"><span data-stu-id="c1b12-109">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="c1b12-110">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="c1b12-110">Select **New**.</span></span>
3. <span data-ttu-id="c1b12-111">Sláið inn eða veldu gildi í reitnum **Heiti**.</span><span class="sxs-lookup"><span data-stu-id="c1b12-111">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="c1b12-112">Í aðgerðarúðunni velurðu **Línur**.</span><span class="sxs-lookup"><span data-stu-id="c1b12-112">In the Action Pane, select **Lines**.</span></span>
5. <span data-ttu-id="c1b12-113">Veldu **Tillögur**.</span><span class="sxs-lookup"><span data-stu-id="c1b12-113">Select **Proposals**.</span></span>
6. <span data-ttu-id="c1b12-114">Veldu **Kauptillaga**.</span><span class="sxs-lookup"><span data-stu-id="c1b12-114">Select **Acquisition proposal**.</span></span>
7. <span data-ttu-id="c1b12-115">Velja **Síu**.</span><span class="sxs-lookup"><span data-stu-id="c1b12-115">Select **Filter**.</span></span> <span data-ttu-id="c1b12-116">Veljið **Endurstilla** til að hreinsa út fyrri gildi.</span><span class="sxs-lookup"><span data-stu-id="c1b12-116">Select **Reset** to clear previous values.</span></span>
8. <span data-ttu-id="c1b12-117">Veljið línuna **Númer eignar**.</span><span class="sxs-lookup"><span data-stu-id="c1b12-117">Select the **Fixed asset number** row.</span></span>
9. <span data-ttu-id="c1b12-118">Í reitinn **Skilyrði** skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="c1b12-118">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="c1b12-119">Stilla eftirstandandi skilyrði eigna sem óskað er að öðlast með þessari greiðslutillögu.</span><span class="sxs-lookup"><span data-stu-id="c1b12-119">Set the remaining criteria for the fixed assets that you want to acquire with this proposal.</span></span>  
10. <span data-ttu-id="c1b12-120">Veldu **Í lagi** tvisvar til að fara út úr rúðunni.</span><span class="sxs-lookup"><span data-stu-id="c1b12-120">Select **OK** twice to exit out of the pane.</span></span>
- <span data-ttu-id="c1b12-121">Ganga skal úr skugga um að færslulínurnar séu stofnaðar.</span><span class="sxs-lookup"><span data-stu-id="c1b12-121">Verify that the transaction lines are created.</span></span>  
- <span data-ttu-id="c1b12-122">Aðeins eignir með kaupdag og kaupverðið settar á bókinni verða teknar með í kauptillögu.</span><span class="sxs-lookup"><span data-stu-id="c1b12-122">Only fixed assets with the acquisition date and acquisition price set on the book will be included in the acquisition proposal.</span></span>  
11. <span data-ttu-id="c1b12-123">Á síðunni velurðu flipann **Bækur**.</span><span class="sxs-lookup"><span data-stu-id="c1b12-123">On the page, select the **Books** tab.</span></span>
12. <span data-ttu-id="c1b12-124">Veldu **Bóka**.</span><span class="sxs-lookup"><span data-stu-id="c1b12-124">Select **Post**.</span></span>

## <a name="include-default-financial-dimensions-in-an-acquisition-proposal"></a><span data-ttu-id="c1b12-125">Hafa sjálfgefnar fjárhagsvídd með í kauptillögu</span><span class="sxs-lookup"><span data-stu-id="c1b12-125">Include default financial dimensions in an acquisition proposal</span></span>

<span data-ttu-id="c1b12-126">Hægt er að búa til kaupfærsluna með því að nota Excel-innbætur með því að fara í **Eignir > Bókarfærslur > Eignabók**.</span><span class="sxs-lookup"><span data-stu-id="c1b12-126">The acquisition transaction can be created using Excel add-ins, by going to **Fixed assets > Journal entries > Fixed asset journal**.</span></span> <span data-ttu-id="c1b12-127">Stofnið nýja færslubók og færið í **Línur** hlutann á síðunni og veljið Excel-táknið og síðan eignabókarlínu.</span><span class="sxs-lookup"><span data-stu-id="c1b12-127">Create a new journal and move to the **Lines** section on the page and select the Excel icon, and then select a Fixed asset journal line.</span></span> <span data-ttu-id="c1b12-128">Kerfið býr til og opnar Excel-sniðmát sem táknar færslubókarlínur.</span><span class="sxs-lookup"><span data-stu-id="c1b12-128">The system will create and open an Excel template representing journal lines.</span></span> <span data-ttu-id="c1b12-129">Hægt er að bæta við gögnum fyrir færslubókarlínurnar sem verið er að bæta við sniðmátið og birta svo upplýsingarnar aftur í kerfið.</span><span class="sxs-lookup"><span data-stu-id="c1b12-129">You can add data for the journal lines you're adding into the template, and then publish that information back into the system.</span></span> 

<span data-ttu-id="c1b12-130">Ef sjálfgefnar víddir hafa verið settar upp fyrir valda eignabók og samsvarandi eignir sem voru færðar inn í Excel-sniðmátið, verða sjálfgefnar fjárhagsvíddir sóttar úr aðalgögnum eignabókar þegar færslubókin er birt úr Excel í kerfið.</span><span class="sxs-lookup"><span data-stu-id="c1b12-130">If default dimensions have been set up for the selected asset book and the corresponding fixed assets that were entered in the Excel template, the default financial dimensions will be called from the asset book master data when the journal is published from the Excel to the system.</span></span> <span data-ttu-id="c1b12-131">Til að taka sjálfkrafa með fjárhagsvídd í eignabók við birtingu á færslubók eigna úr Excel-innbótinni verður að setja upp sjálfgefnar víddir fyrirfram.</span><span class="sxs-lookup"><span data-stu-id="c1b12-131">To include financial dimensions on an asset book automatically while publishing the fixed asset journal from the Excel add-in, the default dimensions must be set up in advance.</span></span>  


[!INCLUDE [footer-include](../../../includes/footer-banner.md)]
