---
title: Beðið er um að vista vöruþekjustillingar þrátt fyrir að þú hafir ekki gert neinar breytingar
description: Beðið er um vista vöruþekjustillingar þrátt fyrir að þú hafir ekki gert neinar breytingar.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: DataManagementWorkspace_
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: angarmas
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 3dfa974740420433af1e1b37630b22509510c91b
ms.sourcegitcommit: 3c15a26e9708adc9a75082dc551f0a3a0a7d89f4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049472"
---
# <a name="youre-prompted-to-save-item-coverage-settings-even-though-you-made-no-changes"></a><span data-ttu-id="7b127-103">Beðið er um að vista vöruþekjustillingar þrátt fyrir að þú hafir ekki gert neinar breytingar</span><span class="sxs-lookup"><span data-stu-id="7b127-103">You're prompted to save item coverage settings even though you made no changes</span></span>

<span data-ttu-id="7b127-104">KB númer: 4615588</span><span class="sxs-lookup"><span data-stu-id="7b127-104">KB number: 4615588</span></span>

## <a name="symptoms"></a><span data-ttu-id="7b127-105">Einkenni</span><span class="sxs-lookup"><span data-stu-id="7b127-105">Symptoms</span></span>

<span data-ttu-id="7b127-106">Í sumum tilvikum gætir þú fengið eftirfarandi skilaboð þegar þú opnar síðuna **Vöruþekja** eftir að hafa flutt inn vörur í gegnum eininguna *Vöruþekja V2*:</span><span class="sxs-lookup"><span data-stu-id="7b127-106">In some scenarios, you might receive the following message when you open the **Item coverage** page after you import items through the *Item coverage V2* entity:</span></span>

> <span data-ttu-id="7b127-107">Á að vista breytingarnar áður en lokað er?</span><span class="sxs-lookup"><span data-stu-id="7b127-107">Do you want to save your changes before closing?</span></span>

<span data-ttu-id="7b127-108">Þú færð þessi skilaboð jafnvel þótt þú hafir ekki gert neinar breytingar.</span><span class="sxs-lookup"><span data-stu-id="7b127-108">You receive this message even though you haven't made any changes.</span></span>

## <a name="resolution"></a><span data-ttu-id="7b127-109">Lausn</span><span class="sxs-lookup"><span data-stu-id="7b127-109">Resolution</span></span>

<span data-ttu-id="7b127-110">Síðan **Vöruþekja** inniheldur flókna sjálfgefna reglu sem gæti valdið því að skilaboðin birtist eftir að beinar breytingar hafa nýlega verið gerðar í gagnagrunninum, t.d. í gegnum innflutning einingar.</span><span class="sxs-lookup"><span data-stu-id="7b127-110">The **Item coverage** page includes complex defaulting logic that might cause the message to be shown after direct changes have recently been made in the database, such as through entity import.</span></span> <span data-ttu-id="7b127-111">Til dæmis er reitur `AREGENERALSETTINGSOVERRIDDEN` einingar stilltur á *Nei* en þú flytur inn skrá sem gefur upp ný eða breytt gildi fyrir reiti á borð við `PRODUCTCOVERAGEGROUPID` og/eða `VENDORACCOUNTNUMBER`.</span><span class="sxs-lookup"><span data-stu-id="7b127-111">For example, the `AREGENERALSETTINGSOVERRIDDEN` entity field is set to *No*, but you import a file that provides new or modified values for fields such as `PRODUCTCOVERAGEGROUPID` and/or `VENDORACCOUNTNUMBER`.</span></span> <span data-ttu-id="7b127-112">Í þessu tilfelli, vegna þess að reiturinn `AREGENERALSETTINGSOVERRIDDEN` er stilltur á *Nei*, eru gildin sjálfkrafa hreinsuð úr reitunum þegar þú opnar síðuna **Vöruþekja** í fyrsta skipti eftir innflutninginn.</span><span class="sxs-lookup"><span data-stu-id="7b127-112">In this case, because the `AREGENERALSETTINGSOVERRIDDEN` field is set to *No*, the values are automatically cleared from the fields when you open the **Item coverage** page for the first time after the import.</span></span> <span data-ttu-id="7b127-113">Ef þú vistar breytingarnar þegar skilaboðaglugginn biður um það, eru þær geymdar í gagnagrunninum.</span><span class="sxs-lookup"><span data-stu-id="7b127-113">If you save the changes as the message box prompts, they are stored in the database.</span></span> <span data-ttu-id="7b127-114">Annars færðu sömu skilaboðin næst þegar þú opnar síðuna.</span><span class="sxs-lookup"><span data-stu-id="7b127-114">Otherwise, you will receive the same message the next time that you open the page.</span></span>

<span data-ttu-id="7b127-115">Til að koma í veg fyrir þessa hegðun en einnig hafa með gildi fyrir reiti eins og `PRODUCTCOVERAGEGROUPID` í gegnum innflutning á einingu skal stilla `AREGENERALSETTINGSOVERRIDDEN` á *Já* þegar þú flytur inn.</span><span class="sxs-lookup"><span data-stu-id="7b127-115">To prevent this behavior but also include values for fields such as `PRODUCTCOVERAGEGROUPID` through entity import, set `AREGENERALSETTINGSOVERRIDDEN` to *Yes* when you import.</span></span>
