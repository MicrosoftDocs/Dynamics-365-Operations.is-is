---
title: Endurflokka eignir
description: Til að endurflokka eign verður að færa hana í nýjan eignaflokk eða að úthluta henni nýju eignanúmeri innan sama flokks.
author: saraschi2
manager: AnnBe
ms.date: 10/30/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d8e289e2c18fd28829fb4b749933ae1d84e0b631
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "323296"
---
# <a name="reclassify-fixed-assets"></a><span data-ttu-id="c9e23-103">Endurflokka eignir</span><span class="sxs-lookup"><span data-stu-id="c9e23-103">Reclassify fixed assets</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c9e23-104">Til að endurflokka eign verður að færa hana í nýjan eignaflokk eða að úthluta henni nýju eignanúmeri innan sama flokks.</span><span class="sxs-lookup"><span data-stu-id="c9e23-104">To reclassify a fixed asset, you must transfer it to a new fixed asset group or assign a new fixed asset number to it in the same group.</span></span> 

<span data-ttu-id="c9e23-105">Þegar eign er endurflokkuð:</span><span class="sxs-lookup"><span data-stu-id="c9e23-105">When a fixed asset is reclassified:</span></span>

<span data-ttu-id="c9e23-106">• Öll virðislíkön fyrirliggjandi eigna eru stofnuð fyrir nýju eignina.</span><span class="sxs-lookup"><span data-stu-id="c9e23-106">• All value models for the existing fixed asset are created for the new fixed asset.</span></span> <span data-ttu-id="c9e23-107">Allar upplýsingar sem voru settar upp fyrir upprunalegu eignina eru afritaðar í nýju eignina.</span><span class="sxs-lookup"><span data-stu-id="c9e23-107">Any information that was set up for the original fixed asset is copied to the new fixed asset.</span></span> <span data-ttu-id="c9e23-108">Staða virðislíkana fyrir upprunalegu eignina er Lokað.</span><span class="sxs-lookup"><span data-stu-id="c9e23-108">The status of the value models for the original fixed asset is Closed.</span></span> 

<span data-ttu-id="c9e23-109">• Nýju virðislíkön nýju eignarinnar innihalda dagsetningu endurflokkunarinnar í svæðinu Kaupdagsetning.</span><span class="sxs-lookup"><span data-stu-id="c9e23-109">• The new value models of the new fixed asset contain the date of the reclassification in the Acquisition date field.</span></span> <span data-ttu-id="c9e23-110">Dagsetningin í svæði Dagsetning afskriftarkeyrslu er afrituð úr upprunalegu eignaupplýsingunum.</span><span class="sxs-lookup"><span data-stu-id="c9e23-110">The date in the Depreciation run date field is copied from the original asset information.</span></span> <span data-ttu-id="c9e23-111">Ef afskriftir eru þegar hafnar sýnir svæðið Dagsetningin þegar afskriftir voru síðast keyrðar dagsetningu endurflokkunarinnar.</span><span class="sxs-lookup"><span data-stu-id="c9e23-111">If the depreciation has already started, the Date when depreciation was last run field displays the date of the reclassification.</span></span> 

<span data-ttu-id="c9e23-112">• Hætt er við fyrirliggjandi eignafærslur upprunalegu eignarinnar og þær myndaðar aftur fyrir nýju eignina.</span><span class="sxs-lookup"><span data-stu-id="c9e23-112">• The existing fixed asset transactions for the original fixed asset are canceled and regenerated for the new fixed asset.</span></span>

1. <span data-ttu-id="c9e23-113">Fara í Eignir > Reglubundin verkefni > Endurflokkun.</span><span class="sxs-lookup"><span data-stu-id="c9e23-113">Go to Fixed assets > Periodic tasks > Reclassification.</span></span>
2. <span data-ttu-id="c9e23-114">Í svæði Eignaflokkur, velja flokk til að endurflokka.</span><span class="sxs-lookup"><span data-stu-id="c9e23-114">In the Fixed asset group field, select the group to reclassify.</span></span>
3. <span data-ttu-id="c9e23-115">Í svæði Eignanúmer, velja eign sem endurflokka.</span><span class="sxs-lookup"><span data-stu-id="c9e23-115">In the Fixed asset number field, select the fixed asset to reclassify.</span></span>
4. <span data-ttu-id="c9e23-116">Í svæði  Nýr eignaflokkur, velja flokk til að flytja eign í.</span><span class="sxs-lookup"><span data-stu-id="c9e23-116">In the New fixed asset group field, select a group to transfer the fixed asset to.</span></span>
    * <span data-ttu-id="c9e23-117">Ef nýr eignaflokkur er festur við númeraröð er svæði Nýtt eignanúmer uppfærður með númer úr númeraröð nýtt eignaflokkur.</span><span class="sxs-lookup"><span data-stu-id="c9e23-117">If the new fixed asset group is attached to a number sequence, the New fixed asset number field is updated with the number from the new fixed asset group number sequence.</span></span> <span data-ttu-id="c9e23-118">Annars er svæði Nýtt eignanúmer uppfærður með númer úr númeraröð sem er sett upp á síðu Færibreytur eigna.</span><span class="sxs-lookup"><span data-stu-id="c9e23-118">Otherwise, the New fixed asset number field is updated with the number from the number sequence that is set up in the Fixed asset parameters page.</span></span> <span data-ttu-id="c9e23-119">Ef númeraröð er ekki sett upp á síðu Færibreytur eigna skal slá inn númer í svæði Nýtt eignanúmer.</span><span class="sxs-lookup"><span data-stu-id="c9e23-119">If a number sequence is not set up in the Fixed asset parameters page, enter a number in the New fixed asset number field.</span></span>  
5. <span data-ttu-id="c9e23-120">Í svæði Dagsetning endurflokkunar slá inn dagsetning.</span><span class="sxs-lookup"><span data-stu-id="c9e23-120">In the Reclassification date field, enter a date.</span></span>
6. <span data-ttu-id="c9e23-121">Í reitinn fylgiskjalaruna skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="c9e23-121">In the Voucher series field, enter or select a value.</span></span>
7. <span data-ttu-id="c9e23-122">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="c9e23-122">Click OK.</span></span>

