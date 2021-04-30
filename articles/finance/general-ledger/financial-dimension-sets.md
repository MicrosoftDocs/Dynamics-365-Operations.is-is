---
title: Fjárhagsvíddasamstæður
description: Í þessu efnisatriði eru fjárhagsvíddasamstæður útskýrðar og ábendingar gefnar um hvernig hægt er að nýta þær sem best.
author: yukonpeegs
manager: AnnBe
ms.date: 03/23/2021
ms.topic: article
ems.prod: ''
ms.technology: ''
ms.search.form: DimensionFocus, LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: roschlom
ms.custom: 25871
ms.search.region: Global
ms.author: epegors
ms.search.validFrom: 2021-03-23
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: b719d8eb868cb1722b470be4443d01181078ce21
ms.sourcegitcommit: 97ada5d52ed1829dcf030dad254096cd8df25da8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/06/2021
ms.locfileid: "5864413"
---
# <a name="financial-dimension-sets"></a><span data-ttu-id="f687b-103">Fjárhagsvíddasamstæður</span><span class="sxs-lookup"><span data-stu-id="f687b-103">Financial dimension sets</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f687b-104">Í þessu efnisatriði eru fjárhagsvíddasamstæður útskýrðar og ábendingar gefnar um hvernig hægt er að nýta þær sem best.</span><span class="sxs-lookup"><span data-stu-id="f687b-104">This topic describes financial dimension sets and provides some tips for optimizing their use.</span></span>

<span data-ttu-id="f687b-105">Víddasamstæða er raðaður listi yfir fjárhagsvíddir sem hægt er að nota til að taka saman fjárhagsgögn á hátt sem notandi skilgreinir.</span><span class="sxs-lookup"><span data-stu-id="f687b-105">A dimension set is an ordered list of financial dimensions that can be used to summarize General ledger data in a user-defined way.</span></span> <span data-ttu-id="f687b-106">Helsta notkun víddasamstæða felst í að skilgreina prófjöfnuð.</span><span class="sxs-lookup"><span data-stu-id="f687b-106">A primary use of dimension sets is to define a trial balance.</span></span>

<span data-ttu-id="f687b-107">Eina staðlaða víddasamstæðan er sú sem inniheldur eingöngu aðallykilinn.</span><span class="sxs-lookup"><span data-stu-id="f687b-107">The only standard dimension set is the dimension set that contains only the main account.</span></span>

<span data-ttu-id="f687b-108">Síðan **Fjárhagsvíddasamstæður** er notuð til að búa til og stjórna fjárhagsvíddasamstæðum.</span><span class="sxs-lookup"><span data-stu-id="f687b-108">You use the **Financial dimension sets** page to create and manage financial dimension sets.</span></span>

## <a name="dimension-set-balances"></a><span data-ttu-id="f687b-109">Stöður víddasamstæðu</span><span class="sxs-lookup"><span data-stu-id="f687b-109">Dimension set balances</span></span>

<span data-ttu-id="f687b-110">Víddasamstæða sem verið með stöður sem byggja á fjárhagsvíddum hennar.</span><span class="sxs-lookup"><span data-stu-id="f687b-110">A dimension set can have balances that are based on its financial dimensions.</span></span> <span data-ttu-id="f687b-111">Stöðurnar eru til í fjárhag og byggja á skilgreningu víddasamstæðunnar.</span><span class="sxs-lookup"><span data-stu-id="f687b-111">The balances exist in General ledger and are based on the dimension set definition.</span></span> <span data-ttu-id="f687b-112">Stöðurnar eru teknar saman úr fjárhagsgögnum til að stuðla að betri afköstum þegar þær eru sóttar (t.d. þegar prófjöfnuður er búinn til).</span><span class="sxs-lookup"><span data-stu-id="f687b-112">The balances are summarized from the General ledger data to help improve performance when they are retrieved (for example, when a trial balance is generated).</span></span>

## <a name="create-balances"></a><span data-ttu-id="f687b-113">Stofna stöður</span><span class="sxs-lookup"><span data-stu-id="f687b-113">Create balances</span></span>

<span data-ttu-id="f687b-114">Notið hnappinn **Stofna stöður** til að frumstilla stöðurnar fyrir víddasamstæðu sem er ekki komin með stöður.</span><span class="sxs-lookup"><span data-stu-id="f687b-114">Use the **Create balances** button to initialize the balances for a dimension set that doesn't currently have balances.</span></span>

> [!NOTE]
> <span data-ttu-id="f687b-115">Mælt er með að takmarka fjölda víddasamstæða sem eru með stöður vegna þess að uppfærslur á stöðum hefur áhrif á allar aðgerðir fjárhagsbókunar.</span><span class="sxs-lookup"><span data-stu-id="f687b-115">We recommend that you limit the number of dimension sets that have balances, because balance updates affect all General ledger posting activities.</span></span>

## <a name="update-balances"></a><span data-ttu-id="f687b-116">Uppfæra stöður</span><span class="sxs-lookup"><span data-stu-id="f687b-116">Update balances</span></span>

<span data-ttu-id="f687b-117">Notið hnappinn **Uppfæra stöður** til að hafa með nýjustu aðgerð fjárhagsbókunar í stöðunum.</span><span class="sxs-lookup"><span data-stu-id="f687b-117">Use the **Update balances** button to include the latest General ledger posting activity in the balances.</span></span> <span data-ttu-id="f687b-118">Uppfærslur á stöðum eru léttar aðgerðir.</span><span class="sxs-lookup"><span data-stu-id="f687b-118">Balance updates are light operations.</span></span> <span data-ttu-id="f687b-119">Þær mega aðeins vinna úr aðgerð fjárhagsbókunar sem hefur átt sér stað frá síðustu uppfærslu.</span><span class="sxs-lookup"><span data-stu-id="f687b-119">They must process only the General ledger posting activity that has occurred since the last update.</span></span>

> [!NOTE]
> <span data-ttu-id="f687b-120">Birting prófjöfnuðar þvingar fram uppfærslu til að tryggja að stöðurnar sem eru sýndar séu núgildandi.</span><span class="sxs-lookup"><span data-stu-id="f687b-120">Display of the trial balance forces an update, to ensure that the balances that are shown are current.</span></span> <span data-ttu-id="f687b-121">Íhugið að nota endurtekna runuvinnslu þannig að uppfærslur á mest notuðu víddasamstæðunum gangi hratt fyrir sig.</span><span class="sxs-lookup"><span data-stu-id="f687b-121">Consider using a recurring batch job so that updates to your most frequently used dimension sets are quick.</span></span> <span data-ttu-id="f687b-122">Þannig stuðlar þú að því að lágmarka tímann sem notendur prófjöfnuðar þurfa að bíða.</span><span class="sxs-lookup"><span data-stu-id="f687b-122">In this way, you help minimize the time that trial balance users must wait.</span></span>

## <a name="rebuild-balances"></a><span data-ttu-id="f687b-123">Endurbyggja stöður</span><span class="sxs-lookup"><span data-stu-id="f687b-123">Rebuild balances</span></span>

<span data-ttu-id="f687b-124">Notið hnappinn **Endurbyggja stöður** til að stofna stöðurnar aftur frá grunni.</span><span class="sxs-lookup"><span data-stu-id="f687b-124">Use the **Rebuild balances** button to re-create the balances from scratch.</span></span> <span data-ttu-id="f687b-125">Þannig tryggir þú að þær stemmi við gögnin í fjárhagnum.</span><span class="sxs-lookup"><span data-stu-id="f687b-125">In this way, you help ensure that they match the data in General ledger.</span></span> <span data-ttu-id="f687b-126">Endurbygging á stöðum krefst mikillar úrvinnslu og ætti oftast ekki að þurfa.</span><span class="sxs-lookup"><span data-stu-id="f687b-126">A rebuild of balances requires lots of processing and should not usually be required.</span></span>

> [!NOTE]
> <span data-ttu-id="f687b-127">Ef aðstæður koma upp sem krefjast endurbyggingar á stöðum með reglulegu millibili mælum við með að þú hafir samband við notendaþjónustu.</span><span class="sxs-lookup"><span data-stu-id="f687b-127">If you have a scenario that regularly requires a rebuild of balances, we recommend that you contact customer support.</span></span> <span data-ttu-id="f687b-128">Notendaþjónustan getur hjálpað þér að finna út hvers vegna stöður stemma ekki við gögn í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="f687b-128">Customer support can help you determine why balances don't match the data in General ledger.</span></span>

## <a name="clear-balances"></a><span data-ttu-id="f687b-129">Hreinsa stöður</span><span class="sxs-lookup"><span data-stu-id="f687b-129">Clear balances</span></span>

<span data-ttu-id="f687b-130">Notið hnappinn **Hreinsa stöður** til að fjarlægja stöðurnar og stöðva frekari uppfærslur.</span><span class="sxs-lookup"><span data-stu-id="f687b-130">Use the **Clear balances** button to remove the balances and stop any further updates.</span></span> <span data-ttu-id="f687b-131">Víddasamstæðan hefur ekki lengur áhrif á aðgerðir fjárhagsbókunar.</span><span class="sxs-lookup"><span data-stu-id="f687b-131">The dimension set will no longer have an impact on General ledger posting activities.</span></span>

<span data-ttu-id="f687b-132">Frekari upplýsingar eru í [Fjárhagsvíddir](financial-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="f687b-132">For more information, see [Financial dimensions](financial-dimensions.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
