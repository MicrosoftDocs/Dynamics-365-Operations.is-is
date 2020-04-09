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
ms.openlocfilehash: dc1e13863ae13daaa641f52f7a55e01fc1353dc1
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142755"
---
# <a name="enter-an-addition-to-a-fixed-asset"></a><span data-ttu-id="64c82-103">Viðbót við eign færð inn</span><span class="sxs-lookup"><span data-stu-id="64c82-103">Enter an addition to a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="64c82-104">Þessi verklýsing sýnir hvernig á að bæta viðbót við eign.</span><span class="sxs-lookup"><span data-stu-id="64c82-104">This procedure shows how to add an addition to an existing fixed asset.</span></span> <span data-ttu-id="64c82-105">Tilgangur eignaviðbætur er til að rekja viðbætur vöru, viðhalds eða lagfæringar fyrir eign og er einungis til upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="64c82-105">The purpose of Fixed asset additions is to track item additions, maintenance, or improvements for an asset, and is informational only.</span></span> <span data-ttu-id="64c82-106">Verða vera gerðar breytingar á eign gildi þjónustu eða líftíma sérstaklega.</span><span class="sxs-lookup"><span data-stu-id="64c82-106">Any changes to the fixed asset value or service life must be made separately.</span></span>   

<span data-ttu-id="64c82-107">Ferlið notar Bókari hlutverk og sýnigögn gögn fyrir USMF lögaðila.</span><span class="sxs-lookup"><span data-stu-id="64c82-107">The procedure uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="64c82-108">Í skoðunarrúðnni ferðu í **Kerfseiningar > Fastafjármunir > Fastafjármunir > Fastafjármunir**.</span><span class="sxs-lookup"><span data-stu-id="64c82-108">In the Navigation pane, go to **Modules > Fixed assets > Fixed assets > Fixed assets**.</span></span>
2. <span data-ttu-id="64c82-109">Finna og velja eign fyrir viðbótar af listanum.</span><span class="sxs-lookup"><span data-stu-id="64c82-109">In the list, find and select the fixed asset for the addition.</span></span>
3. <span data-ttu-id="64c82-110">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="64c82-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="64c82-111">Á aðgerðasvæðinu skal smellt á **Fastafjármuni**.</span><span class="sxs-lookup"><span data-stu-id="64c82-111">On the Action Pane, click **Fixed asset**.</span></span>
5. <span data-ttu-id="64c82-112">Smelltu á **Eignaviðbætur**.</span><span class="sxs-lookup"><span data-stu-id="64c82-112">Click **Fixed asset additions**.</span></span>
6. <span data-ttu-id="64c82-113">Smellt er á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="64c82-113">Click **New**.</span></span>
7. <span data-ttu-id="64c82-114">Í reitinn **Heiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="64c82-114">In the **Name** field, type a value.</span></span>
8. <span data-ttu-id="64c82-115">Í reitinn **Kaupdagsetning** reitinn, stilltu dagsetningu viðbótarkaupsins eða þjónustunnar.</span><span class="sxs-lookup"><span data-stu-id="64c82-115">In the **Acquisition date** field, set the date of the addition purchase or service.</span></span>
9. <span data-ttu-id="64c82-116">Í reitinn **Einingakostnaður** skal færa inn kostnað vöru, viðhald eða aðrar umbætur á eigninni.</span><span class="sxs-lookup"><span data-stu-id="64c82-116">In the **Unit cost** field, enter the cost of the item, maintenance, or other improvement for the asset.</span></span>
10. <span data-ttu-id="64c82-117">Í reitnum **Magn** slærðu inn tölu.</span><span class="sxs-lookup"><span data-stu-id="64c82-117">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="64c82-118">Heildarkostnað hafa engin áhrif á virði eignarinnar og er fyrir rakningu og upplýsinga aðeins.</span><span class="sxs-lookup"><span data-stu-id="64c82-118">The total cost will have no impact on the value of the fixed asset and is for tracking and informational purposes only.</span></span> <span data-ttu-id="64c82-119">Ef kostnaður verður eignfærður, síðan verður að bóka uppskrifaða sérleiðréttingarfærslu .</span><span class="sxs-lookup"><span data-stu-id="64c82-119">If the cost will be capitalized, then a write-up adjustment transaction must be posted separately.</span></span>  
11. <span data-ttu-id="64c82-120">Smelltu á flipann **Almennt**.</span><span class="sxs-lookup"><span data-stu-id="64c82-120">Click the **General** tab.</span></span>

    * <span data-ttu-id="64c82-121">Stilltu **Eykur líftíma** á **Já** ef viðbótin eykur líftíma eignarinnar.</span><span class="sxs-lookup"><span data-stu-id="64c82-121">Set **Increases service life** to **Yes** if the addition increases the service life of the asset.</span></span>  
    * <span data-ttu-id="64c82-122">Þetta svæði er einungis til upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="64c82-122">This field is informational only.</span></span> <span data-ttu-id="64c82-123">Til að auka líftíma skal breyta líftíma á virðislíkön og/eða afskriftarbókum fyrir eignina.</span><span class="sxs-lookup"><span data-stu-id="64c82-123">To increase the service life, modify the Service life on the Value models and/or Depreciation books for the asset.</span></span>  

