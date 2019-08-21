---
title: Stinga upp á eignakaupum
description: Þetta efni lýsir hvernig á að kaupa eignir með því að nota kauptillögu í færslubók eigna.
author: saraschi2
manager: AnnBe
ms.date: 07/22/2019
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
ms.openlocfilehash: 4b35b13dc266fd5bccde437526400832d394b9aa
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839906"
---
# <a name="propose-fixed-asset-acquisitions"></a><span data-ttu-id="6c446-103">Stinga upp á eignakaupum</span><span class="sxs-lookup"><span data-stu-id="6c446-103">Propose fixed asset acquisitions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6c446-104">Þetta efni lýsir hvernig á að kaupa eignir með því að nota kauptillögu í færslubók eigna.</span><span class="sxs-lookup"><span data-stu-id="6c446-104">This topic describes how to acquire a fixed asset using the acquisition proposal in the Fixed assets journal.</span></span> <span data-ttu-id="6c446-105">Það notar Bókari hlutverk og sýnigögn fyrir USMF lögaðila.</span><span class="sxs-lookup"><span data-stu-id="6c446-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="6c446-106">Í skoðunarrúðnni ferðu í **Kerfseiningar > Fastafjármunir > Dagbókarfærslur > Dagbók fastafjármuna**.</span><span class="sxs-lookup"><span data-stu-id="6c446-106">In the Navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="6c446-107">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="6c446-107">Select **New**.</span></span>
3. <span data-ttu-id="6c446-108">Sláið inn eða veldu gildi í reitnum **Heiti**.</span><span class="sxs-lookup"><span data-stu-id="6c446-108">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="6c446-109">Í aðgerðarúðunni velurðu **Línur**.</span><span class="sxs-lookup"><span data-stu-id="6c446-109">In the action pane, select **Lines**.</span></span>
5. <span data-ttu-id="6c446-110">Veldu **Tillögur**.</span><span class="sxs-lookup"><span data-stu-id="6c446-110">Select **Proposals**.</span></span>
6. <span data-ttu-id="6c446-111">Veldu **Kauptillaga**.</span><span class="sxs-lookup"><span data-stu-id="6c446-111">Select **Acquisition proposal**.</span></span>
7. <span data-ttu-id="6c446-112">Velja **Síu**.</span><span class="sxs-lookup"><span data-stu-id="6c446-112">Select **Filter**.</span></span> <span data-ttu-id="6c446-113">Veldu **Endurstilla** til að hreinsa út fyrri gildi.</span><span class="sxs-lookup"><span data-stu-id="6c446-113">Select **Reset** to clear out previous values.</span></span>
8. <span data-ttu-id="6c446-114">Veljið línuna **Númer eignar**.</span><span class="sxs-lookup"><span data-stu-id="6c446-114">Select the **Fixed asset number** row.</span></span>
9. <span data-ttu-id="6c446-115">Í reitinn **Skilyrði** skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="6c446-115">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="6c446-116">Stilla eftirstandandi skilyrði eigna sem óskað er að öðlast með þessari greiðslutillögu.</span><span class="sxs-lookup"><span data-stu-id="6c446-116">Set the remaining criteria for the fixed assets that you want to acquire with this proposal.</span></span>  
10. <span data-ttu-id="6c446-117">Veldu **Í lagi** tvisvar til að fara út úr rúðunni.</span><span class="sxs-lookup"><span data-stu-id="6c446-117">Select **OK** twice to exit out of the pane.</span></span>
- <span data-ttu-id="6c446-118">Staðfesta færslulínurnar stofnaðar.</span><span class="sxs-lookup"><span data-stu-id="6c446-118">Verify the transaction lines created.</span></span>  
- <span data-ttu-id="6c446-119">Aðeins eignir með kaupdag og kaupverðið settar á bókinni verða teknar með í kauptillögu.</span><span class="sxs-lookup"><span data-stu-id="6c446-119">Only fixed assets with the acquisition date and acquisition price set on the book will be included in the acquisition proposal.</span></span>  
11. <span data-ttu-id="6c446-120">Á síðunni velurðu flipann **Bækur**.</span><span class="sxs-lookup"><span data-stu-id="6c446-120">On the page, select the **Books** tab.</span></span>
12. <span data-ttu-id="6c446-121">Veldu **Bóka**.</span><span class="sxs-lookup"><span data-stu-id="6c446-121">Select **Post**.</span></span>

