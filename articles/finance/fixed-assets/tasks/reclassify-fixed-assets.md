---
title: Endurflokka eignir
description: Til að endurflokka eign verður að færa hana í nýjan eignaflokk eða að úthluta henni nýju eignanúmeri innan sama flokks.
author: saraschi2
manager: AnnBe
ms.date: 05/14/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4cfc1425aca7a62205e0c7c50237f206a179a0e7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968855"
---
# <a name="reclassify-fixed-assets"></a><span data-ttu-id="18bcc-103">Endurflokka eignir</span><span class="sxs-lookup"><span data-stu-id="18bcc-103">Reclassify fixed assets</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="18bcc-104">Til að endurflokka eign verður að færa hana í nýjan eignaflokk eða að úthluta henni nýju eignanúmeri innan sama flokks.</span><span class="sxs-lookup"><span data-stu-id="18bcc-104">To reclassify a fixed asset, you must transfer it to a new fixed asset group or assign a new fixed asset number to it in the same group.</span></span> 

<span data-ttu-id="18bcc-105">Þegar eign er endurflokkuð:</span><span class="sxs-lookup"><span data-stu-id="18bcc-105">When a fixed asset is reclassified:</span></span>

* <span data-ttu-id="18bcc-106">Allar bækur fyrirliggjandi eigna eru stofnaðar fyrir nýju eignina.</span><span class="sxs-lookup"><span data-stu-id="18bcc-106">All books for the existing fixed asset are created for the new fixed asset.</span></span> <span data-ttu-id="18bcc-107">Allar upplýsingar sem voru settar upp fyrir upprunalegu eignina eru afritaðar í nýju eignina.</span><span class="sxs-lookup"><span data-stu-id="18bcc-107">Any information that was set up for the original fixed asset is copied to the new fixed asset.</span></span> <span data-ttu-id="18bcc-108">Staða bókanna fyrir upprunalegu eignina er Lokað.</span><span class="sxs-lookup"><span data-stu-id="18bcc-108">The status of the books for the original fixed asset is Closed.</span></span> 

* <span data-ttu-id="18bcc-109">Nýju bækur nýju eignarinnar innihalda dagsetningu endurflokkunarinnar í reitnum **Kaupdagsetning**.</span><span class="sxs-lookup"><span data-stu-id="18bcc-109">The new books of the new fixed asset contain the date of the reclassification in the **Acquisition date** field.</span></span> <span data-ttu-id="18bcc-110">Dagsetningin í svæði **Dagsetning afskriftarkeyrslu** er afrituð úr upprunalegu eignaupplýsingunum.</span><span class="sxs-lookup"><span data-stu-id="18bcc-110">The date in the **Depreciation run date** field is copied from the original asset information.</span></span> <span data-ttu-id="18bcc-111">Ef afskriftir eru þegar hafnar sýnir svæðið **Dagsetningin þegar afskriftir voru síðast keyrðar** dagsetningu endurflokkunarinnar.</span><span class="sxs-lookup"><span data-stu-id="18bcc-111">If the depreciation has already started, the **Date when depreciation was last run** field displays the date of the reclassification.</span></span> 

* <span data-ttu-id="18bcc-112">Hætt er við fyrirliggjandi eignafærslur upprunalegu eignarinnar og þær myndaðar aftur fyrir nýju eignina.</span><span class="sxs-lookup"><span data-stu-id="18bcc-112">The existing fixed asset transactions for the original fixed asset are canceled and regenerated for the new fixed asset.</span></span>

<span data-ttu-id="18bcc-113">Fylgið þessum skrefum til að endurflokka eign:</span><span class="sxs-lookup"><span data-stu-id="18bcc-113">Follow these steps to reclassify a fixed asset:</span></span>

1. <span data-ttu-id="18bcc-114">Fara í **Eignir > Reglubundin verkefni > Endurflokkun.**</span><span class="sxs-lookup"><span data-stu-id="18bcc-114">Go to **Fixed assets > Periodic tasks > Reclassification.**</span></span>
2. <span data-ttu-id="18bcc-115">Í svæðinu **Eignaflokkur** skal velja flokk til að endurflokka.</span><span class="sxs-lookup"><span data-stu-id="18bcc-115">In the **Fixed asset group** field, select the group to reclassify.</span></span>
3. <span data-ttu-id="18bcc-116">Í svæði **Eignanúmer** skal velja eign sem endurflokka.</span><span class="sxs-lookup"><span data-stu-id="18bcc-116">In the **Fixed asset number** field, select the fixed asset to reclassify.</span></span>
4. <span data-ttu-id="18bcc-117">Í reitnum **Nýr eignaflokkur** skal velja flokk til að flytja eign í.</span><span class="sxs-lookup"><span data-stu-id="18bcc-117">In the **New fixed asset group** field, select a group to transfer the fixed asset to.</span></span>
    * <span data-ttu-id="18bcc-118">Ef nýr eignaflokkur er festur við númeraröð er svæði **Nýtt eignanúmer** uppfærður með númer úr númeraröð nýtt eignaflokkur.</span><span class="sxs-lookup"><span data-stu-id="18bcc-118">If the new fixed asset group is attached to a number sequence, the **New fixed asset number** field is updated with the number from the new fixed asset group number sequence.</span></span> <span data-ttu-id="18bcc-119">Annars er svæðið **Nýtt eignanúmer** uppfært með númeri úr númeraröð sem er sett upp á síðunni **Færibreytur eigna**.</span><span class="sxs-lookup"><span data-stu-id="18bcc-119">Otherwise, the **New fixed asset number** field is updated with the number from the number sequence that is set up on the **Fixed asset parameters** page.</span></span> <span data-ttu-id="18bcc-120">Ef númeraröð er ekki sett upp á síðunni **Færibreytur eigna** skal slá inn númerið í svæðinu **Nýtt eignanúmer**.</span><span class="sxs-lookup"><span data-stu-id="18bcc-120">If a number sequence is not set up on the **Fixed asset parameters** page, enter a number in the **New fixed asset number** field.</span></span>  
5. <span data-ttu-id="18bcc-121">Í svæði **Dagsetning endurflokkunar** skal slá inn dagsetning.</span><span class="sxs-lookup"><span data-stu-id="18bcc-121">In the **Reclassification date** field, enter a date.</span></span>
6. <span data-ttu-id="18bcc-122">Í reitinn **fylgiskjalaruna** skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="18bcc-122">In the **Voucher series** field, enter or select a value.</span></span>
7. <span data-ttu-id="18bcc-123">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="18bcc-123">Click **OK**.</span></span>
