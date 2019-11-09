---
title: Viðbót við eign færð inn
description: Þessi verklýsing sýnir hvernig á að bæta viðbót við eign.
author: saraschi2
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetAddition
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fe1a1d4db696ac013afee05b697b301383232134
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186947"
---
# <a name="enter-an-addition-to-a-fixed-asset"></a><span data-ttu-id="2290e-103">Viðbót við eign færð inn</span><span class="sxs-lookup"><span data-stu-id="2290e-103">Enter an addition to a fixed asset</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2290e-104">Þessi verklýsing sýnir hvernig á að bæta viðbót við eign.</span><span class="sxs-lookup"><span data-stu-id="2290e-104">This procedure shows how to add an addition to an existing fixed asset.</span></span> <span data-ttu-id="2290e-105">Tilgangur eignaviðbætur er til að rekja viðbætur vöru, viðhalds eða lagfæringar fyrir eign og er einungis til upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="2290e-105">The purpose of Fixed asset additions is to track item additions, maintenance, or improvements for an asset, and is informational only.</span></span> <span data-ttu-id="2290e-106">Verða vera gerðar breytingar á eign gildi þjónustu eða líftíma sérstaklega.</span><span class="sxs-lookup"><span data-stu-id="2290e-106">Any changes to the fixed asset value or service life must be made separately.</span></span>   

<span data-ttu-id="2290e-107">Ferlið notar Bókari hlutverk og sýnigögn gögn fyrir USMF lögaðila.</span><span class="sxs-lookup"><span data-stu-id="2290e-107">The procedure uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="2290e-108">Í skoðunarrúðnni ferðu í **Kerfseiningar > Fastafjármunir > Fastafjármunir > Fastafjármunir**.</span><span class="sxs-lookup"><span data-stu-id="2290e-108">In the Navigation pane, go to **Modules > Fixed assets > Fixed assets > Fixed assets**.</span></span>
2. <span data-ttu-id="2290e-109">Finna og velja eign fyrir viðbótar af listanum.</span><span class="sxs-lookup"><span data-stu-id="2290e-109">In the list, find and select the fixed asset for the addition.</span></span>
3. <span data-ttu-id="2290e-110">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="2290e-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="2290e-111">Á aðgerðasvæðinu skal smellt á **Fastafjármuni**.</span><span class="sxs-lookup"><span data-stu-id="2290e-111">On the Action Pane, click **Fixed asset**.</span></span>
5. <span data-ttu-id="2290e-112">Smelltu á **Eignaviðbætur**.</span><span class="sxs-lookup"><span data-stu-id="2290e-112">Click **Fixed asset additions**.</span></span>
6. <span data-ttu-id="2290e-113">Smellt er á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="2290e-113">Click **New**.</span></span>
7. <span data-ttu-id="2290e-114">Í reitinn **Heiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="2290e-114">In the **Name** field, type a value.</span></span>
8. <span data-ttu-id="2290e-115">Í reitinn **Kaupdagsetning** reitinn, stilltu dagsetningu viðbótarkaupsins eða þjónustunnar.</span><span class="sxs-lookup"><span data-stu-id="2290e-115">In the **Acquisition date** field, set the date of the addition purchase or service.</span></span>
9. <span data-ttu-id="2290e-116">Í reitinn **Einingakostnaður** skal færa inn kostnað vöru, viðhald eða aðrar umbætur á eigninni.</span><span class="sxs-lookup"><span data-stu-id="2290e-116">In the **Unit cost** field, enter the cost of the item, maintenance, or other improvement for the asset.</span></span>
10. <span data-ttu-id="2290e-117">Í reitnum **Magn** slærðu inn tölu.</span><span class="sxs-lookup"><span data-stu-id="2290e-117">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="2290e-118">Heildarkostnað hafa engin áhrif á virði eignarinnar og er fyrir rakningu og upplýsinga aðeins.</span><span class="sxs-lookup"><span data-stu-id="2290e-118">The total cost will have no impact on the value of the fixed asset and is for tracking and informational purposes only.</span></span> <span data-ttu-id="2290e-119">Ef kostnaður verður eignfærður, síðan verður að bóka uppskrifaða sérleiðréttingarfærslu .</span><span class="sxs-lookup"><span data-stu-id="2290e-119">If the cost will be capitalized, then a write-up adjustment transaction must be posted separately.</span></span>  
11. <span data-ttu-id="2290e-120">Smelltu á flipann **Almennt**.</span><span class="sxs-lookup"><span data-stu-id="2290e-120">Click the **General** tab.</span></span>

    * <span data-ttu-id="2290e-121">Stilltu **Eykur líftíma** á **Já** ef viðbótin eykur líftíma eignarinnar.</span><span class="sxs-lookup"><span data-stu-id="2290e-121">Set **Increases service life** to **Yes** if the addition increases the service life of the asset.</span></span>  
    * <span data-ttu-id="2290e-122">Þetta svæði er einungis til upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="2290e-122">This field is informational only.</span></span> <span data-ttu-id="2290e-123">Til að auka líftíma skal breyta líftíma á virðislíkön og/eða afskriftarbókum fyrir eignina.</span><span class="sxs-lookup"><span data-stu-id="2290e-123">To increase the service life, modify the Service life on the Value models and/or Depreciation books for the asset.</span></span>  
