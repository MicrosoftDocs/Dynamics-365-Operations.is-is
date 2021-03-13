---
title: Viðteknar reglur eignarleigu
description: Þetta efnisatriði lýsir viðteknum reglum fyrir leigðar eignir.
author: moaamer
manager: Ann Beebe
ms.date: 1/14/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetLease
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2021-1-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: ea89d54f1ce3a1e971d41623bf44f909f7dfdf09
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/06/2021
ms.locfileid: "5131289"
---
# <a name="asset-leasing-conventions"></a><span data-ttu-id="0b386-103">Viðteknar reglur eignarleigu</span><span class="sxs-lookup"><span data-stu-id="0b386-103">Asset leasing conventions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0b386-104">Þetta efnisatriði lýsir viðteknum reglum fyrir leigðar eignir.</span><span class="sxs-lookup"><span data-stu-id="0b386-104">This topic describes conventions for leased assets.</span></span> <span data-ttu-id="0b386-105">Viðteknar reglur leigusamninga eru notaðar til að ákvarða upphafsdag leigubókar.</span><span class="sxs-lookup"><span data-stu-id="0b386-105">Leasing conventions are used to determine the commencement date of a lease book.</span></span> <span data-ttu-id="0b386-106">Ef viðtekin regla leigusamnings er stillt á **Engin** er upphafsdagurinn sá sami og upphafsdagsetning leigusamningsins (þ.e. gildið í reitnum **Upphafsdagsetning leigusamnings**).</span><span class="sxs-lookup"><span data-stu-id="0b386-106">If the leasing convention is set to **None**, the commencement date is the same as the start date for the lease (that is, the value of the **Lease start date** field).</span></span> <span data-ttu-id="0b386-107">Ef viðtekin regla leigusamnings er stillt á **Heill mánuður** er upphafsdagurinn fyrsti dagur mánaðarins sem upphafsdagsetning leigusamningings fellur undir.</span><span class="sxs-lookup"><span data-stu-id="0b386-107">If the leasing convention is set to **Full month**, the commencement date is the first day of the month that the lease's start date falls in.</span></span>

<span data-ttu-id="0b386-108">Upphafsdagurinn ákvarðar upphafsdagsetningu tímabilsins fyrir afskriftaráætlun leiguskuldbindingar og eignar.</span><span class="sxs-lookup"><span data-stu-id="0b386-108">The commencement date determines the start date of the period for the liability amortization and asset depreciation schedules.</span></span> <span data-ttu-id="0b386-109">Vaxtakostnaður og afskriftakostnaður eru bókaðir á lokadagsetningu tímabils samsvarandi áætlana.</span><span class="sxs-lookup"><span data-stu-id="0b386-109">Interest expenses and depreciation expenses are posted on the period end date of the corresponding schedules.</span></span> <span data-ttu-id="0b386-110">Upphafleg skráningarfærsla og færsla í leiðréttingabók eru bókaðar á upphafsdeginum.</span><span class="sxs-lookup"><span data-stu-id="0b386-110">The initial recognition and adjustment journal entry are posted on the commencement date.</span></span>

> [!NOTE]
> <span data-ttu-id="0b386-111">Það verður að kveikja á eiginleikanum fyrir viðteknar reglur leigusamninga í gegnum eiginleikastjórnun.</span><span class="sxs-lookup"><span data-stu-id="0b386-111">The feature for leasing conventions must be turned on through Feature Management.</span></span> <span data-ttu-id="0b386-112">Á vinnusvæðinu **Eiginleikastjórnun** skal finna og velja eiginleikann sem heitir **Viðtekin regla leigusamnings fyrir eignarleigu** og velja því næst **Virkja núna**.</span><span class="sxs-lookup"><span data-stu-id="0b386-112">In the **Feature management** workspace, find and select the feature that is named **Leasing convention for asset leasing** feature, and then select **Enable now**.</span></span>

<span data-ttu-id="0b386-113">Viðteknum reglum leigusamninga er úthlutað á uppsetninguna fyrir leigubók leigusamnings.</span><span class="sxs-lookup"><span data-stu-id="0b386-113">Leasing conventions are assigned to the setup for a lease asset book.</span></span>

<span data-ttu-id="0b386-114">Til að skoða eða úthluta viðtekinni reglu leigusamnings skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="0b386-114">To view or assign the leasing convention, follow these steps.</span></span>

1. <span data-ttu-id="0b386-115">Opnið **Eignarleiga \> Uppsetning \> Leigubækur**.</span><span class="sxs-lookup"><span data-stu-id="0b386-115">Go to **Asset leasing \> Setup \> Lease books**.</span></span>
2. <span data-ttu-id="0b386-116">Í reitnum **Viðtekin regla leigusamnings** skal velja eitt af eftirfarandi gildum.</span><span class="sxs-lookup"><span data-stu-id="0b386-116">In the **Leasing convention** field, select one of the following values.</span></span>

    | <span data-ttu-id="0b386-117">Reglur leigusamnings</span><span class="sxs-lookup"><span data-stu-id="0b386-117">Leasing convention</span></span> | <span data-ttu-id="0b386-118">lýsing</span><span class="sxs-lookup"><span data-stu-id="0b386-118">Description</span></span> |
    |--------------------|-------------|
    | <span data-ttu-id="0b386-119">Engum</span><span class="sxs-lookup"><span data-stu-id="0b386-119">None</span></span>               | <span data-ttu-id="0b386-120">Afskiftaráætlanir leiguskuldbindingar og eignar hefjast á upphafsdagsetningu leigusamningsins vegna þess að upphafsdagurinn jafngildir upphafsdagsetningu leigusamningsins.</span><span class="sxs-lookup"><span data-stu-id="0b386-120">The liability amortization and asset depreciation schedules start on the lease's start date, because the commencement date equals the lease's start date.</span></span> <span data-ttu-id="0b386-121">Lokadagsetningin er einum mánuði síðar.</span><span class="sxs-lookup"><span data-stu-id="0b386-121">The end date is one month later.</span></span> <span data-ttu-id="0b386-122">Þessi viðtekna regla leigusamnings tryggir ekki að vextirnir verði bókaðir á síðasta degi hvers mánaðar.</span><span class="sxs-lookup"><span data-stu-id="0b386-122">This leasing convention doesn't guarantee that the interest will be posted on the last day of each month.</span></span> |
    | <span data-ttu-id="0b386-123">Heill mánuður</span><span class="sxs-lookup"><span data-stu-id="0b386-123">Full month</span></span>         | <span data-ttu-id="0b386-124">Fyrir leigusamninga sem eru með upphafsdagsetningu sem kemur upp einhvern tímann í mánuðinum byrja afskriftaráætlanir leiguskuldbindingar og eignar að safna saman kostnaði á fyrsta degi þess mánaðar.</span><span class="sxs-lookup"><span data-stu-id="0b386-124">For leases that have a start date that occurs at any time during the month, the liability amortization and asset depreciation schedules start to accrue expenses on the first day of that month.</span></span> <span data-ttu-id="0b386-125">Þessi viðtekna regla leigusamnings tryggir að vöxtum er safnað saman á síðasta degi hvers mánaðar fyrir allan mánuðinn.</span><span class="sxs-lookup"><span data-stu-id="0b386-125">This leasing convention ensures that interest is accrued on the last day of each month for the whole month.</span></span> |

3. <span data-ttu-id="0b386-126">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="0b386-126">Select **Save**.</span></span>

<span data-ttu-id="0b386-127">Þegar leigusamningur er stofnaður er upphafsdagur hverrar bókar sjálfkrafa færður inn samkvæmt upphafsdagsetningunni sem er færð inn fyrir leigusamninginn og viðteknu reglu hans sem er tilgreind fyrir bókina.</span><span class="sxs-lookup"><span data-stu-id="0b386-127">When a lease is created, the commencement date of each book is automatically entered based on the start date that is entered for the lease and the leasing convention that is specified for the book.</span></span>
