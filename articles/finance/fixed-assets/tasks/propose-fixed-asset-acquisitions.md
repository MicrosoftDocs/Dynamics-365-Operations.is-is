---
title: Stinga upp á eignakaupum
description: Þetta efni lýsir hvernig á að kaupa eignir með því að nota kauptillögu í færslubók eigna.
author: saraschi2
manager: AnnBe
ms.date: 07/27/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0997af638c141661afb677e2407a90a883168aed
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4444236"
---
# <a name="propose-fixed-asset-acquisitions"></a><span data-ttu-id="b672e-103">Stinga upp á eignakaupum</span><span class="sxs-lookup"><span data-stu-id="b672e-103">Propose fixed asset acquisitions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b672e-104">Þetta efni lýsir hvernig á að kaupa eignir með því að nota kauptillögu í færslubók eigna.</span><span class="sxs-lookup"><span data-stu-id="b672e-104">This topic describes how to acquire a fixed asset using the acquisition proposal in the Fixed assets journal.</span></span> <span data-ttu-id="b672e-105">Það notar Bókari hlutverk og sýnigögn fyrir USMF lögaðila.</span><span class="sxs-lookup"><span data-stu-id="b672e-105">It uses the accountant role and demo data for the USMF legal entity.</span></span> <span data-ttu-id="b672e-106">Til að komast yfir eign í gegnum tillögubók eignar, þarf fyrst að stofna eignafærsluna og síðan skilgreina kaupverð í eignabókinni.</span><span class="sxs-lookup"><span data-stu-id="b672e-106">To acquire a fixed asset through a fixed asset proposal journal, you must first create the fixed asset record, and then define the acquisition price in the asset book.</span></span>

1. <span data-ttu-id="b672e-107">Í skoðunarrúðnni ferðu í **Kerfseiningar > Fastafjármunir > Dagbókarfærslur > Dagbók fastafjármuna**.</span><span class="sxs-lookup"><span data-stu-id="b672e-107">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="b672e-108">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="b672e-108">Select **New**.</span></span>
3. <span data-ttu-id="b672e-109">Sláið inn eða veldu gildi í reitnum **Heiti**.</span><span class="sxs-lookup"><span data-stu-id="b672e-109">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="b672e-110">Í aðgerðarúðunni velurðu **Línur**.</span><span class="sxs-lookup"><span data-stu-id="b672e-110">In the action pane, select **Lines**.</span></span>
5. <span data-ttu-id="b672e-111">Veldu **Tillögur**.</span><span class="sxs-lookup"><span data-stu-id="b672e-111">Select **Proposals**.</span></span>
6. <span data-ttu-id="b672e-112">Veldu **Kauptillaga**.</span><span class="sxs-lookup"><span data-stu-id="b672e-112">Select **Acquisition proposal**.</span></span>
7. <span data-ttu-id="b672e-113">Velja **Síu**.</span><span class="sxs-lookup"><span data-stu-id="b672e-113">Select **Filter**.</span></span> <span data-ttu-id="b672e-114">Veldu **Endurstilla** til að hreinsa út fyrri gildi.</span><span class="sxs-lookup"><span data-stu-id="b672e-114">Select **Reset** to clear out previous values.</span></span>
8. <span data-ttu-id="b672e-115">Veljið línuna **Númer eignar**.</span><span class="sxs-lookup"><span data-stu-id="b672e-115">Select the **Fixed asset number** row.</span></span>
9. <span data-ttu-id="b672e-116">Í reitinn **Skilyrði** skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="b672e-116">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="b672e-117">Stilla eftirstandandi skilyrði eigna sem óskað er að öðlast með þessari greiðslutillögu.</span><span class="sxs-lookup"><span data-stu-id="b672e-117">Set the remaining criteria for the fixed assets that you want to acquire with this proposal.</span></span>  
10. <span data-ttu-id="b672e-118">Veldu **Í lagi** tvisvar til að fara út úr rúðunni.</span><span class="sxs-lookup"><span data-stu-id="b672e-118">Select **OK** twice to exit out of the pane.</span></span>
- <span data-ttu-id="b672e-119">Staðfesta færslulínurnar stofnaðar.</span><span class="sxs-lookup"><span data-stu-id="b672e-119">Verify the transaction lines created.</span></span>  
- <span data-ttu-id="b672e-120">Aðeins eignir með kaupdag og kaupverðið settar á bókinni verða teknar með í kauptillögu.</span><span class="sxs-lookup"><span data-stu-id="b672e-120">Only fixed assets with the acquisition date and acquisition price set on the book will be included in the acquisition proposal.</span></span>  
11. <span data-ttu-id="b672e-121">Á síðunni velurðu flipann **Bækur**.</span><span class="sxs-lookup"><span data-stu-id="b672e-121">On the page, select the **Books** tab.</span></span>
12. <span data-ttu-id="b672e-122">Veldu **Bóka**.</span><span class="sxs-lookup"><span data-stu-id="b672e-122">Select **Post**.</span></span>
