---
title: "Færa inn samsetningu fyrir lykil og vídd (sundurliðað innfærslustýring)"
description: "Þessi grein lýsir því hvenir eigi að færa inn samsetningar reiknings og vídda eða fjárhagslykil. Framkvæmd innfærslunnar er oft kölluð sundurliðuð innfærslustýring"
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DimensionConfigureAccountStructure
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14071
ms.assetid: e6fce826-c403-4d91-a78b-e9a58c44ac03
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 120a28cc9ae8685895400e872cc03e7b6a1c6642
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---

# <a name="enter-account-and-dimension-combinations-segmented-entry-control"></a><span data-ttu-id="9013a-104">Færa inn samsetningu fyrir lykil og vídd (sundurliðað innfærslustýring)</span><span class="sxs-lookup"><span data-stu-id="9013a-104">Enter account and dimension combinations (segmented entry control)</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="9013a-105">Þessi grein lýsir því hvenir eigi að færa inn samsetningar reiknings og vídda eða fjárhagslykil.</span><span class="sxs-lookup"><span data-stu-id="9013a-105">This article describes how to enter account and dimension combinations or ledger accounts.</span></span> <span data-ttu-id="9013a-106">Framkvæmd innfærslunnar er oft kölluð sundurliðuð innfærslustýring</span><span class="sxs-lookup"><span data-stu-id="9013a-106">The entry experience is often referred to as segmented entry control.</span></span>

<span data-ttu-id="9013a-107">Notendur færa inn samsetningu fyrir lykil og vídd á mismunandi síðum, eins og  síðum fyrir almennar færslubækur, fjárhagsáætlanir og bókunarskilgreiningar.</span><span class="sxs-lookup"><span data-stu-id="9013a-107">Users enter account and dimension combinations on various pages, such as pages for general journals, budgeting, and posting definitions.</span></span> <span data-ttu-id="9013a-108">Gildar samsetningar fyrir lykil og vídd eru háðar lykilskipulagi sem úthlutað er til fjárhags og ítarlegum reglum sem eru úthlutaðar fyrir lykilskipulagið.</span><span class="sxs-lookup"><span data-stu-id="9013a-108">The valid account and dimension combinations depend on the account structures that are assigned to the ledger and the advanced rules that are assigned to the account structures.</span></span> <span data-ttu-id="9013a-109">Þegar notendur færa inn samsetninga geta þeir annaðhvort slegið gildin inn handvirkt eða nýtt sér fjölskrúðuga uppflettingarupplifun.</span><span class="sxs-lookup"><span data-stu-id="9013a-109">When users enter a combination, they can either manually type the values or take advantage of a rich, lookup experience.</span></span> <span data-ttu-id="9013a-110">Þegar þú færið inn svæði, geturðu byrjað slá inn og þá leitar að gildi og lýsingu.</span><span class="sxs-lookup"><span data-stu-id="9013a-110">When you enter the field, you can start to type and it will search the value and the description.</span></span> <span data-ttu-id="9013a-111">Til dæmis ef slegið inn 180 mun leita að öllum gildi sem byrja með því númerasamsetning.</span><span class="sxs-lookup"><span data-stu-id="9013a-111">For example, if you type 180 it will search any value that begins with that number combination.</span></span> <span data-ttu-id="9013a-112">Eða slá inn Reiðufé og þá leitar að öll gildi sem er með lýsing sem byrjar á Reiðufé.</span><span class="sxs-lookup"><span data-stu-id="9013a-112">Or you may type Cash and it will search any value that has a description that begins with Cash.</span></span> <span data-ttu-id="9013a-113">Einnig hægt að nota algildisstaf, t.d. \*Reiðufé eða \*180 til að leita ef gildi eða lýsing innihalda leitarskilyrði.</span><span class="sxs-lookup"><span data-stu-id="9013a-113">You can also use a wildcard, such as \*Cash or \*180 to search if the value or description contain the search criteria.</span></span> 

<span data-ttu-id="9013a-114">Eftirfarandi tafla lýsir flýtilyklum á lyklaborði sem hægt er að nota þegar uppflettisvæði er lokað.</span><span class="sxs-lookup"><span data-stu-id="9013a-114">The following table describes the keyboard shortcuts that can be used when the lookup is closed.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9013a-115">Flýtilykill</span><span class="sxs-lookup"><span data-stu-id="9013a-115">Keyboard shortcut</span></span></th>
<th><span data-ttu-id="9013a-116">Aðgerð</span><span class="sxs-lookup"><span data-stu-id="9013a-116">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9013a-117">Alt+Niðurör</span><span class="sxs-lookup"><span data-stu-id="9013a-117">Alt+Down Arrow</span></span></td>
<td><span data-ttu-id="9013a-118">Opna uppflettisvæðið.</span><span class="sxs-lookup"><span data-stu-id="9013a-118">Open the lookup.</span></span> <span data-ttu-id="9013a-119">Ef smellt er aftur á Alt + Niður Ör, færist áherslan á hlutana í hliðarglugganum.</span><span class="sxs-lookup"><span data-stu-id="9013a-119">If you press Alt+Down Arrow a second time, the focus moves to the segments in the flyout.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="9013a-120">Enter og Shift+Enter</span><span class="sxs-lookup"><span data-stu-id="9013a-120">Enter and Shift+Enter</span></span></li>
<li><span data-ttu-id="9013a-121">Afmarkari bókhaldslykils</span><span class="sxs-lookup"><span data-stu-id="9013a-121">Chart of accounts delimiter</span></span></li>
<li><span data-ttu-id="9013a-122">Hægri ör og vinstri ör</span><span class="sxs-lookup"><span data-stu-id="9013a-122">Right Arrow and Left Arrow</span></span></li>
</ul></td>
<td><span data-ttu-id="9013a-123">Fara yfir í næsta eða fyrri hluta.</span><span class="sxs-lookup"><span data-stu-id="9013a-123">Move to the next or previous segment.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9013a-124">Dálkalykill</span><span class="sxs-lookup"><span data-stu-id="9013a-124">Tab</span></span></td>
<td><span data-ttu-id="9013a-125">Fara á næsta svæði í hnitanetinu.</span><span class="sxs-lookup"><span data-stu-id="9013a-125">Move to the next field in the grid.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="9013a-126">Eftirfarandi tafla lýsir flýtivísum á lyklaborði sem hægt er að nota þegar uppflettisvæði er opið.</span><span class="sxs-lookup"><span data-stu-id="9013a-126">The following table describes the keyboard shortcuts that can be used when the lookup is open.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9013a-127">Flýtilykill</span><span class="sxs-lookup"><span data-stu-id="9013a-127">Keyboard shortcut</span></span></th>
<th><span data-ttu-id="9013a-128">Aðgerð</span><span class="sxs-lookup"><span data-stu-id="9013a-128">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9013a-129">Esc</span><span class="sxs-lookup"><span data-stu-id="9013a-129">Esc</span></span></td>
<td><span data-ttu-id="9013a-130">Loka uppflettisvæðinu.</span><span class="sxs-lookup"><span data-stu-id="9013a-130">Close the lookup.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="9013a-131">Upp-ör og niður-ör</span><span class="sxs-lookup"><span data-stu-id="9013a-131">Up Arrow and Down Arrow</span></span></li>
<li><span data-ttu-id="9013a-132">Síða upp og síða niður</span><span class="sxs-lookup"><span data-stu-id="9013a-132">Page Up and Page Down</span></span></li>
<li><span data-ttu-id="9013a-133">Heim og ljúka</span><span class="sxs-lookup"><span data-stu-id="9013a-133">Home and End</span></span></li>
</ul></td>
<td><span data-ttu-id="9013a-134">Flytja í næsta eða fyrra gildi í listum, í næsta eða fyrri hóp gilda eða í fyrstu eða síðustu einingu í uppflettisvæðinu.</span><span class="sxs-lookup"><span data-stu-id="9013a-134">Move to the previous or next value in the lists, to the previous or next group of values, or to the first or last element in the lookup.</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="9013a-135">Afmarkari bókhaldslykils</span><span class="sxs-lookup"><span data-stu-id="9013a-135">Chart of accounts delimiter</span></span></li>
<li><span data-ttu-id="9013a-136">Hægri ör° og vinstri ör</span><span class="sxs-lookup"><span data-stu-id="9013a-136">Right Arrow and Left Arrow</span></span></li>
</ul></td>
<td><span data-ttu-id="9013a-137">Fara yfir í næsta eða fyrri hluta.</span><span class="sxs-lookup"><span data-stu-id="9013a-137">Move to the next or previous segment.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9013a-138">Flipi</span><span class="sxs-lookup"><span data-stu-id="9013a-138">Tab</span></span></td>
<td><span data-ttu-id="9013a-139">Fara á næsta svæði í hnitanetinu.</span><span class="sxs-lookup"><span data-stu-id="9013a-139">Move to the next field in the grid.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9013a-140">Alt+W</span><span class="sxs-lookup"><span data-stu-id="9013a-140">Alt+W</span></span></td>
<td><span data-ttu-id="9013a-141">Víxla á milli <strong>Sýna allt</strong> og <strong>Sýna gilt</strong>.</span><span class="sxs-lookup"><span data-stu-id="9013a-141">Switch between <strong>Show all</strong> and <strong>Show valid</strong>.</span></span></td>
</tr>
</tbody>
</table>






