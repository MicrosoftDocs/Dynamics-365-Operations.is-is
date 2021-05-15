---
title: Þyngdarreitirnir í farmlínum passa ekki við þyngdarreitina í farminum
description: Þyngdarreitirnir í farmlínum passa ekki við þyngdarreitina í farminum
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSShipmentDetails_WHSShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 639b82a9d46b74f179d6904d2c3b8e7dfb813b58
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924352"
---
# <a name="the-weight-fields-on-load-lines-dont-match-the-weight-fields-on-the-load"></a><span data-ttu-id="760c5-103">Þyngdarreitirnir í farmlínum passa ekki við þyngdarreitina í farminum</span><span class="sxs-lookup"><span data-stu-id="760c5-103">The weight fields on load lines don't match the weight fields on the load</span></span>

<span data-ttu-id="760c5-104">Villukóðar: WHSLoadWeightOnLinesDoNotMatchLoadWarning</span><span class="sxs-lookup"><span data-stu-id="760c5-104">Error codes: WHSLoadWeightOnLinesDoNotMatchLoadWarning</span></span>

## <a name="symptoms"></a><span data-ttu-id="760c5-105">Einkenni</span><span class="sxs-lookup"><span data-stu-id="760c5-105">Symptoms</span></span>

<span data-ttu-id="760c5-106">Kerfið sýnir eftirfarandi villuboð:</span><span class="sxs-lookup"><span data-stu-id="760c5-106">The system shows the following error message:</span></span>

> <span data-ttu-id="760c5-107">Þyngdarreitirnir í hleðslulínum stemma ekki við þyngdarreitina í hleðslu %1.</span><span class="sxs-lookup"><span data-stu-id="760c5-107">The weight fields on load lines do not match the weight fields on load %1.</span></span> <span data-ttu-id="760c5-108">Keyra samræmisathugun hleðsluþyngdar vöruhúss til að endurreikna þyngdarreiti.</span><span class="sxs-lookup"><span data-stu-id="760c5-108">Run the Warehouse load weight consistency check to recalculate the weight fields.</span></span>

## <a name="cause"></a><span data-ttu-id="760c5-109">Orsök</span><span class="sxs-lookup"><span data-stu-id="760c5-109">Cause</span></span>

<span data-ttu-id="760c5-110">Reitirnir **Nettóþyngd** og **Töruþyngd** eru stilltir á *0* (núll) í hleðslulínunni.</span><span class="sxs-lookup"><span data-stu-id="760c5-110">The **Net weight** and **Tara weight** fields are set to *0* (zero) on the load line.</span></span> <span data-ttu-id="760c5-111">Þyngdarreitir eru þó ekki stilltir á *0* fyrir þyngdarmælingar á vörunni.</span><span class="sxs-lookup"><span data-stu-id="760c5-111">However, the weight fields aren't set to *0* for the weight measurements on the product.</span></span> <span data-ttu-id="760c5-112">Þegar þyngdarreitir eru ekki stilltir í hleðslulínunni geta allar leiðréttingar á magninu á hleðslulínunni valdið röngum þyngdarútreikningi á hleðslunni.</span><span class="sxs-lookup"><span data-stu-id="760c5-112">When weight fields aren't set on the load line, any corrections of the quantity on the load line might cause incorrect weight calculation on the load.</span></span> <span data-ttu-id="760c5-113">Þetta vandamál gæti komið upp ef þyngd vörunnar hefur verið breytt síðan hleðslulínan var stofnuð.</span><span class="sxs-lookup"><span data-stu-id="760c5-113">This issue might occur if the weights on the product have been changed since the load line was created.</span></span>

## <a name="resolution"></a><span data-ttu-id="760c5-114">Upplausn</span><span class="sxs-lookup"><span data-stu-id="760c5-114">Resolution</span></span>

<span data-ttu-id="760c5-115">Sjálfgefið er að þegar hleðslulína er stofnuð eru þyngdarreitir vörunnar færðir inn á hana.</span><span class="sxs-lookup"><span data-stu-id="760c5-115">By default, when a load line is created, the weight fields from the product are entered on it.</span></span> <span data-ttu-id="760c5-116">Ef þyngdin er núll er hægt að endurreikna hana með virkninni *Samræmisathugun á hleðsluþyngd vöruhúss*.</span><span class="sxs-lookup"><span data-stu-id="760c5-116">If the weight is zero, you can recalculate it by using the *Warehouse load weight consistency check* functionality.</span></span>

1. <span data-ttu-id="760c5-117">Farið í **Kerfisstjórnun \> Reglubundin verkefni \> Gagnagrunnur \> Samræmisathugun**.</span><span class="sxs-lookup"><span data-stu-id="760c5-117">Go to **System administration \> Periodic tasks \> Database \> Consistency check**.</span></span>
1. <span data-ttu-id="760c5-118">Í **Samræmisathugun** glugganum skal stilla **Eining** á *Vöruhúsastjórnun*.</span><span class="sxs-lookup"><span data-stu-id="760c5-118">In the **Consistency check** dialog box, set the **Module** field to *Warehouse management*.</span></span>
1. <span data-ttu-id="760c5-119">Stillið reitinn **Athuga/Laga** á *Laga villu*.</span><span class="sxs-lookup"><span data-stu-id="760c5-119">Set the **Check/Fix** field to *Fix error*.</span></span>
1. <span data-ttu-id="760c5-120">Í lista yfir gátreiti skal velja gátreitinn **Samræmisathugun á hleðsluþyngd vöruhúss** og ganga úr skugga um að aðeins línan fyrir þennan gátreit sé auðkennd.</span><span class="sxs-lookup"><span data-stu-id="760c5-120">In the checkbox list, select the **Warehouse load weight consistency check** checkbox, and make sure that only the row for this checkbox is highlighted.</span></span>
1. <span data-ttu-id="760c5-121">Efst á gátreitinum skal velja úrfellingarhnappinn (**...**) og velja svo **Svargluggi** á valmyndinni.</span><span class="sxs-lookup"><span data-stu-id="760c5-121">At the top of the checkbox list, select the ellipsis button (**...**), and then select **Dialog** on the menu.</span></span>
1. <span data-ttu-id="760c5-122">Veljið eftirtalda reiti í glugganum **Samræmisathugun á hleðsluþyngd vöruhúss** til að tilgreina viðmiðin sem samræmisathugun á að kanna:</span><span class="sxs-lookup"><span data-stu-id="760c5-122">In the **Warehouse load weight consistency check** dialog box, set the following fields to specify the criteria that the consistency check should run for:</span></span>

    - <span data-ttu-id="760c5-123">**Hleðslukenni:** Tilgreindu hleðslukenni.</span><span class="sxs-lookup"><span data-stu-id="760c5-123">**Load ID:** Specify a load ID.</span></span> <span data-ttu-id="760c5-124">Skiljið þetta eftir autt til að athuga öll kenni hleðslu.</span><span class="sxs-lookup"><span data-stu-id="760c5-124">Leave this blank to check all load IDs.</span></span>
    - <span data-ttu-id="760c5-125">**Vörunúmer:** Tilgreindu vörunúmer.</span><span class="sxs-lookup"><span data-stu-id="760c5-125">**Item number:** Specify an item number.</span></span> <span data-ttu-id="760c5-126">Skildu þetta eftir autt til að athuga allar vörur.</span><span class="sxs-lookup"><span data-stu-id="760c5-126">Leave this blank to check all items.</span></span>
    - <span data-ttu-id="760c5-127">**Alltaf endurreikna þyngd á hleðslum:** Stilltu þennan valkost á *Já*</span><span class="sxs-lookup"><span data-stu-id="760c5-127">**Always recalculate weight on loads:** Set this option to *Yes*.</span></span>
    - <span data-ttu-id="760c5-128">**Leyfa að skrifa yfir þyngd á hleðslulínum:** Stillið þennan valkost á *Já*.</span><span class="sxs-lookup"><span data-stu-id="760c5-128">**Allow overwrite of weight on load lines:** Set this option to *Yes*.</span></span>

1. <span data-ttu-id="760c5-129">Velja skal **Í lagi** til að loka glugganum **Samræmisathugun á hleðsluþyngd vöruhúss**.</span><span class="sxs-lookup"><span data-stu-id="760c5-129">Select **OK** to close the **Warehouse load weight consistency check** dialog box.</span></span>
1. <span data-ttu-id="760c5-130">Veljið úrfellingarhnappinn og veljið **Keyra** í valmyndinni.</span><span class="sxs-lookup"><span data-stu-id="760c5-130">Select the ellipsis button, and then select **Execute** on the menu.</span></span>

<span data-ttu-id="760c5-131">Þyngdin er endurreiknuð á grundvelli skilyrðanna sem tilgreind voru.</span><span class="sxs-lookup"><span data-stu-id="760c5-131">The weight is recalculated based on the criteria that you specified.</span></span> <span data-ttu-id="760c5-132">Veljið tengilinn **Skilaboðaupplýsingar** til að skoða niðurstöður samræmiskoðunarinnar.</span><span class="sxs-lookup"><span data-stu-id="760c5-132">Select the **Message details** link to view the result of the consistency check.</span></span>
