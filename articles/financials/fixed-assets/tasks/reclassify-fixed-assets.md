--- 
title: Endurflokka eignir
description: "Til að endurflokka eign verður að færa hana í nýjan eignaflokk eða að úthluta henni nýju eignanúmeri innan sama flokks."
author: saraschi2
manager: AnnBe
ms.date: 06/26/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: fda4d71b050edde2752536985b18ebcad203d078
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="reclassify-fixed-assets"></a><span data-ttu-id="bd2a4-103">Endurflokka eignir</span><span class="sxs-lookup"><span data-stu-id="bd2a4-103">Reclassify fixed assets</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bd2a4-104">Til að endurflokka eign verður að færa hana í nýjan eignaflokk eða að úthluta henni nýju eignanúmeri innan sama flokks.</span><span class="sxs-lookup"><span data-stu-id="bd2a4-104">To reclassify a fixed asset, you must transfer it to a new fixed asset group or assign a new fixed asset number to it in the same group.</span></span> 

<span data-ttu-id="bd2a4-105">Þegar eign er endurflokkuð:</span><span class="sxs-lookup"><span data-stu-id="bd2a4-105">When a fixed asset is reclassified:</span></span>

<span data-ttu-id="bd2a4-106">• Öll virðislíkön fyrirliggjandi eigna eru stofnuð fyrir nýju eignina.</span><span class="sxs-lookup"><span data-stu-id="bd2a4-106">• All value models for the existing fixed asset are created for the new fixed asset.</span></span> <span data-ttu-id="bd2a4-107">Allar upplýsingar sem voru settar upp fyrir upprunalegu eignina eru afritaðar í nýju eignina.</span><span class="sxs-lookup"><span data-stu-id="bd2a4-107">Any information that was set up for the original fixed asset is copied to the new fixed asset.</span></span> <span data-ttu-id="bd2a4-108">Staða virðislíkana fyrir upprunalegu eignina er Lokað.</span><span class="sxs-lookup"><span data-stu-id="bd2a4-108">The status of the value models for the original fixed asset is Closed.</span></span> 

<span data-ttu-id="bd2a4-109">• Nýju virðislíkön nýju eignarinnar innihalda dagsetningu endurflokkunarinnar í svæðinu Kaupdagsetning.</span><span class="sxs-lookup"><span data-stu-id="bd2a4-109">• The new value models of the new fixed asset contain the date of the reclassification in the Acquisition date field.</span></span> <span data-ttu-id="bd2a4-110">Dagsetningin í svæði Dagsetning afskriftarkeyrslu er afrituð úr upprunalegu eignaupplýsingunum.</span><span class="sxs-lookup"><span data-stu-id="bd2a4-110">The date in the Depreciation run date field is copied from the original asset information.</span></span> <span data-ttu-id="bd2a4-111">Ef afskriftir eru þegar hafnar sýnir svæðið Dagsetningin þegar afskriftir voru síðast keyrðar dagsetningu endurflokkunarinnar.</span><span class="sxs-lookup"><span data-stu-id="bd2a4-111">If the depreciation has already started, the Date when depreciation was last run field displays the date of the reclassification.</span></span> 

<span data-ttu-id="bd2a4-112">• Hætt er við fyrirliggjandi eignafærslur upprunalegu eignarinnar og þær myndaðar aftur fyrir nýju eignina.</span><span class="sxs-lookup"><span data-stu-id="bd2a4-112">• The existing fixed asset transactions for the original fixed asset are canceled and regenerated for the new fixed asset.</span></span>

1. <span data-ttu-id="bd2a4-113">Fara í Eignir > Reglubundin verkefni > Endurflokkun.</span><span class="sxs-lookup"><span data-stu-id="bd2a4-113">Go to Fixed assets > Periodic tasks > Reclassification.</span></span>
2. <span data-ttu-id="bd2a4-114">Í svæði Eignaflokkur, velja flokk til að endurflokka.</span><span class="sxs-lookup"><span data-stu-id="bd2a4-114">In the Fixed asset group field, selet the group to reclassify.</span></span>
3. <span data-ttu-id="bd2a4-115">Í svæði Eignanúmer, velja eign sem endurflokka.</span><span class="sxs-lookup"><span data-stu-id="bd2a4-115">In the Fixed asset number field, select the fixed asset to reclassify.</span></span>
4. <span data-ttu-id="bd2a4-116">Í svæði  Nýr eignaflokkur, velja flokk til að flytja eign í.</span><span class="sxs-lookup"><span data-stu-id="bd2a4-116">In the New fixed asset group field, select a group to transfer the fixed asset to.</span></span>
    * <span data-ttu-id="bd2a4-117">Ef nýr eignaflokkur er festur við númeraröð er svæði Nýtt eignanúmer uppfærður með númer úr númeraröð nýtt eignaflokkur.</span><span class="sxs-lookup"><span data-stu-id="bd2a4-117">If the new fixed asset group is attached to a number sequence, the New fixed asset number field is updated with the number from the new fixed asset group number sequence.</span></span> <span data-ttu-id="bd2a4-118">Annars er svæði Nýtt eignanúmer uppfærður með númer úr númeraröð sem er sett upp á síðu Færibreytur eigna.</span><span class="sxs-lookup"><span data-stu-id="bd2a4-118">Otherwise, the New fixed asset number field is updated with the number from the number sequence that is set up in the Fixed asset parameters page.</span></span> <span data-ttu-id="bd2a4-119">Ef númeraröð er ekki sett upp á síðu Færibreytur eigna skal slá inn númer í svæði Nýtt eignanúmer.</span><span class="sxs-lookup"><span data-stu-id="bd2a4-119">If a number sequence is not set up in the Fixed asset parameters page, enter a number in the New fixed asset number field.</span></span>  
5. <span data-ttu-id="bd2a4-120">Í svæði Dagsetning endurflokkunar slá inn dagsetning.</span><span class="sxs-lookup"><span data-stu-id="bd2a4-120">In the Reclassification date field, enter a date.</span></span>
6. <span data-ttu-id="bd2a4-121">Í reitinn fylgiskjalaruna skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="bd2a4-121">In the Voucher series field, enter or select a value.</span></span>
7. <span data-ttu-id="bd2a4-122">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="bd2a4-122">Click OK.</span></span>


