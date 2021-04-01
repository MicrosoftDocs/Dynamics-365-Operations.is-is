---
title: Setja upp vaxtavísitölur
description: Í þessu efnisatriði er útskýrt hvernig á að setja upp vaxtavísitölu. Vaxtavísitölur eru áskildar ef fyrirtækið tengir upphæðir leigugreiðslna við safn af vaxtavísitölum.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: b6d201329996f23d94c0fc76a9635d3bb99c931e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5249678"
---
# <a name="set-up-index-rates"></a><span data-ttu-id="b45e3-104">Setja upp vaxtavísitölur</span><span class="sxs-lookup"><span data-stu-id="b45e3-104">Set up index rates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b45e3-105">Ef leigugreiðslur eru háðar vísitölu er hægt að bæta við gerðum vaxtavísitala vinna með þær í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="b45e3-105">If lease payments depend on an index, the index rate types can be added and maintained in the system.</span></span> <span data-ttu-id="b45e3-106">Til að endurmeta leigugeriðslur á síðunni **Gerð vaxtavísitölu** notar endurmatsferli vaxtavísitölu nýjustu vaxtavísitöluna frá endurmatsdagsetningunni.</span><span class="sxs-lookup"><span data-stu-id="b45e3-106">To revalue the lease payments from the **Index rate type** page, the index rate revaluation process uses the most recent index rate from the date of revaluation.</span></span>

<span data-ttu-id="b45e3-107">Fylgdu eftirfarandi skrefum til að bæta við gerðum vaxtarvísitala og vaxtarvísitölum.</span><span class="sxs-lookup"><span data-stu-id="b45e3-107">To add index rate types and index rates, follow these steps.</span></span>

1. <span data-ttu-id="b45e3-108">Opnið **Eignarleiga \> Uppsetning \> Gerðir vaxtavísitölu**.</span><span class="sxs-lookup"><span data-stu-id="b45e3-108">Go to **Asset leasing \> Setup \> Index rate type**.</span></span>
2. <span data-ttu-id="b45e3-109">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="b45e3-109">Select **New**.</span></span>
3. <span data-ttu-id="b45e3-110">Færið inn gerð vísitölunnar og heiti vaxtavísitölunnar í viðeigandi svæði.</span><span class="sxs-lookup"><span data-stu-id="b45e3-110">In the appropriate fields, enter the rate type and the name of the index rate.</span></span>
4. <span data-ttu-id="b45e3-111">Til að bæta við nýju gildi vaxtavísitölu skal velja gerð vaxtavísitölunnar og síðan valja **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="b45e3-111">To add a new index rate value, select the index rate type, and then select **Add**.</span></span>
5. <span data-ttu-id="b45e3-112">Veldu raunverulegan upphafsdag gildisins og veldu gildi vísitölunnar.</span><span class="sxs-lookup"><span data-stu-id="b45e3-112">Select the effective start date of the rate, and select the rate value.</span></span>

<span data-ttu-id="b45e3-113">Velja verður annað hvort **Gildismun vaxtavísitölu** eða **Gildi vaxtavísitölu** sem aðferð vaxtavísitölu.</span><span class="sxs-lookup"><span data-stu-id="b45e3-113">You must select either **Index rate value difference** or **Index rate value** as the index rate method.</span></span>

- <span data-ttu-id="b45e3-114">Veldu aðferðina **Gildismun vaxtavísitölu** til að reikna út nýja leigugreiðslu miðað við mismuninn á milli vaxtavísitölu á upphafsdeginum og nýjustu vaxtavísitölunni.</span><span class="sxs-lookup"><span data-stu-id="b45e3-114">Select the **Index rate value difference** method to calculate a new lease payment, based on the difference between the index rate on the start date and the most recent index rate.</span></span> <span data-ttu-id="b45e3-115">Vaxtavísitalan er skilgreind í svæðinu **Vaxtavísitala (%)**.</span><span class="sxs-lookup"><span data-stu-id="b45e3-115">The index rate is defined in the **Index rate (%)** field.</span></span>
- <span data-ttu-id="b45e3-116">Veldu aðferðina **Gildi vaxtavísitölu** til að reikna út leigugreiðsluna með því að nota prósentuhlutfallið sem er tilgreint í svæðinu **Vaxtavísitala (%)**.</span><span class="sxs-lookup"><span data-stu-id="b45e3-116">Select the **Index rate value** method to calculate the lease payment by using the percentage that is specified in the **Index rate (%)** field.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]