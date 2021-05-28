---
title: Staðsetningarforstilling leyfir ekki neikvæða birgðaskráningu en neikvæð birgðastaða er leyfð
description: Valkosturinn Leyfa neikvæða birgðir fyrir staðsetningarforstillinguna er stilltur á Nei, en kerfið leyfir samt neikvæðar birgðir.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WHSLocationProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: shawan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 356d2dd7853bf93250e14eb9bd28a8a145794584
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026607"
---
# <a name="location-profile-disallows-negative-inventory-but-negative-on-hand-inventory-is-permitted"></a><span data-ttu-id="13784-103">Staðsetningarforstilling leyfir ekki neikvæða birgðaskráningu en neikvæð birgðastaða er leyfð</span><span class="sxs-lookup"><span data-stu-id="13784-103">Location profile disallows negative inventory, but negative on-hand inventory is permitted</span></span>

<span data-ttu-id="13784-104">KB númer: 4613622</span><span class="sxs-lookup"><span data-stu-id="13784-104">KB number: 4613622</span></span>

## <a name="symptoms"></a><span data-ttu-id="13784-105">Einkenni</span><span class="sxs-lookup"><span data-stu-id="13784-105">Symptoms</span></span>

<span data-ttu-id="13784-106">Valkosturinn **Leyfa neikvæða birgðir** fyrir staðsetningarforstillinguna er stilltur á *Nei*, en kerfið leyfir samt neikvæðar birgðir.</span><span class="sxs-lookup"><span data-stu-id="13784-106">The **Allow negative inventory** option for the location profile is set to *No*, but the system still allows negative on-hand inventory.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="13784-107">Dæmi</span><span class="sxs-lookup"><span data-stu-id="13784-107">Example scenario</span></span>

<span data-ttu-id="13784-108">Við færslur við opinbera aðila þarf kerfið að geta skráð neikvæðar birgðir til að bókfæra tap.</span><span class="sxs-lookup"><span data-stu-id="13784-108">For government-regulated transactions, the system must be able to record negative inventory to book losses.</span></span> <span data-ttu-id="13784-109">Þú vilt að hlutur geti sýnt neikvæða birgðir, en aðeins á tilgreindum stöðum, svo sem geymum.</span><span class="sxs-lookup"><span data-stu-id="13784-109">You want an item to be able to show negative inventory, but only in designated locations, such as tanks.</span></span> <span data-ttu-id="13784-110">Ef vörulíkanahópurinn leyfir hins vegar neikvæðar birgðir kemur í ljós að það skiptir ekki máli hvort staðsetningin er stillt til að leyfa neikvæðar birgðir.</span><span class="sxs-lookup"><span data-stu-id="13784-110">However, if the item model group allows negative inventory, you find that it doesn't matter whether the location is set to allow negative inventory.</span></span> <span data-ttu-id="13784-111">Ef varan er sett upp þannig að neikvæð birgðastaða er ekki leyfð skiptir ekki máli hvernig staðsetningarlýsingin er sett upp.</span><span class="sxs-lookup"><span data-stu-id="13784-111">If the item is set up so that negative inventory isn't allowed, it doesn't matter how the location profile is set up.</span></span>

## <a name="resolution"></a><span data-ttu-id="13784-112">Upplausn</span><span class="sxs-lookup"><span data-stu-id="13784-112">Resolution</span></span>

<span data-ttu-id="13784-113">**Leyfa neikvæða birgðir** frá staðsetningarforstillingunni á aðeins við um vöruhúsferli, svo sem tínslu.</span><span class="sxs-lookup"><span data-stu-id="13784-113">The **Allow negative inventory** setting from the location profile applies only to warehouse processes, such as picking.</span></span> <span data-ttu-id="13784-114">Vörulíkanaflokkar sem eru hins vegar stilltir til að leyfa neikvæðar birgðir hafa hins vegar áhrif á öll ferli úr einingum birgðastjórnunar og lagerstjórnunar og staðsetningarforstillingin mun ekki víkja frá stillingunni.</span><span class="sxs-lookup"><span data-stu-id="13784-114">However, item model groups that are set to allow negative inventory affect all processes from the Inventory management and Warehouse management modules, and the location profile won't override the setting.</span></span>

<span data-ttu-id="13784-115">Þú getur stýrt því hvort vöruhús megi hafa neikvæðar birgðir.</span><span class="sxs-lookup"><span data-stu-id="13784-115">You can control whether a warehouse is allowed to carry negative inventory.</span></span> <span data-ttu-id="13784-116">Stillið vörulíkanaflokkana á að leyfa ekki neikvæðar efnislegar birgðir og stillið aðeins viðkomandi vöruhús á að leyfa neikvæðar birgðir.</span><span class="sxs-lookup"><span data-stu-id="13784-116">Set your item model groups to disallow negative physical inventory, and set only the relevant warehouse to allow negative inventory.</span></span>
