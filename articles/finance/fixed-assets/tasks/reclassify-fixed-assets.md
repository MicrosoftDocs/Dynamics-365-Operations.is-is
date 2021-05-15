---
title: Endurflokka eignir
description: Til að endurflokka eign verður að færa hana í nýjan eignaflokk eða að úthluta henni nýju eignanúmeri innan sama flokks.
author: saraschi2
ms.date: 05/14/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fbfb754459fad1f3b1509f4f9c65c20e0385b013
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944714"
---
# <a name="reclassify-fixed-assets"></a><span data-ttu-id="63d22-103">Endurflokka eignir</span><span class="sxs-lookup"><span data-stu-id="63d22-103">Reclassify fixed assets</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="63d22-104">Til að endurflokka eign verður að færa hana í nýjan eignaflokk eða að úthluta henni nýju eignanúmeri innan sama flokks.</span><span class="sxs-lookup"><span data-stu-id="63d22-104">To reclassify a fixed asset, you must transfer it to a new fixed asset group or assign a new fixed asset number to it in the same group.</span></span> 

<span data-ttu-id="63d22-105">Þegar eign er endurflokkuð:</span><span class="sxs-lookup"><span data-stu-id="63d22-105">When a fixed asset is reclassified:</span></span>

- <span data-ttu-id="63d22-106">Allar bækur fyrirliggjandi eigna eru stofnaðar fyrir nýju eignina.</span><span class="sxs-lookup"><span data-stu-id="63d22-106">All books for the existing fixed asset are created for the new fixed asset.</span></span> <span data-ttu-id="63d22-107">Allar upplýsingar sem voru settar upp fyrir upprunalegu eignina eru afritaðar í nýju eignina.</span><span class="sxs-lookup"><span data-stu-id="63d22-107">Any information that was set up for the original fixed asset is copied to the new fixed asset.</span></span> <span data-ttu-id="63d22-108">Staða bókanna fyrir upprunalegu eignina er Lokað.</span><span class="sxs-lookup"><span data-stu-id="63d22-108">The status of the books for the original fixed asset is Closed.</span></span> 

- <span data-ttu-id="63d22-109">Nýju bækur nýju eignarinnar innihalda dagsetningu endurflokkunarinnar í reitnum **Kaupdagsetning**.</span><span class="sxs-lookup"><span data-stu-id="63d22-109">The new books for the new fixed asset contain the date of the reclassification in the **Acquisition date** field.</span></span> <span data-ttu-id="63d22-110">Dagsetningin í svæði **Dagsetning afskriftarkeyrslu** er afrituð úr upprunalegu eignaupplýsingunum.</span><span class="sxs-lookup"><span data-stu-id="63d22-110">The date in the **Depreciation run date** field is copied from the original asset information.</span></span> <span data-ttu-id="63d22-111">Ef afskriftir eru þegar hafnar sýnir svæðið **Dagsetningin þegar afskriftir voru síðast keyrðar** dagsetningu endurflokkunarinnar.</span><span class="sxs-lookup"><span data-stu-id="63d22-111">If the depreciation has already started, the **Date when depreciation was last run** field displays the date of the reclassification.</span></span> 

- <span data-ttu-id="63d22-112">Hætt er við fyrirliggjandi eignafærslur upprunalegu eignarinnar og þær myndaðar aftur fyrir nýju eignina.</span><span class="sxs-lookup"><span data-stu-id="63d22-112">The existing fixed asset transactions for the original fixed asset are canceled and regenerated for the new fixed asset.</span></span>

- <span data-ttu-id="63d22-113">Þegar eign með færslu hefur verið endurflokkuð birtir kerfið skilaboð í **aðgerðamiðstöðinni** um að millifærslu hafi ekki verið lokið meðan á endurflokkunarferlinu stóð.</span><span class="sxs-lookup"><span data-stu-id="63d22-113">When an asset that has a transfer transaction has been reclassified, the system will display a message in the **Action center** to indicate that a transfer transaction wasn't completed during the reclassification process.</span></span> <span data-ttu-id="63d22-114">Nauðsynlegt er að ljúka flutningsfærslu til að færa fyrirliggjandi endurflokkunarfærslu í viðeigandi fjárhagsvídd.</span><span class="sxs-lookup"><span data-stu-id="63d22-114">It's necessary to complete a transfer transaction to move the existing reclassification transactions to the appropriate financial dimensions.</span></span> 

   <span data-ttu-id="63d22-115">Meðan á endurflokkunarferlinu stendur keyrir kerfið eftirfarandi aðgerðir til að endurflokka eignastöðuna frá upprunalegu eigninni yfir á nýju eignina.</span><span class="sxs-lookup"><span data-stu-id="63d22-115">During the reclassification process, the system runs the following actions to reclassify the asset balance from the original asset to the new asset.</span></span> 
   
   - <span data-ttu-id="63d22-116">Endurflokkunarferlið afritar gögnin úr upprunalegu eignabókinni í nýju eignabókina.</span><span class="sxs-lookup"><span data-stu-id="63d22-116">The reclassification process copies the data from the original fixed asset book to the new fixed asset book.</span></span>

   - <span data-ttu-id="63d22-117">Í endurflokkunarfærslunni eru notaðar upplýsingar úr upprunalegu bókuðu kaupunum sem innihalda upplýsingar um fjárhagsvídd sem eru innifaldar í eignaflutningsfærslunni.</span><span class="sxs-lookup"><span data-stu-id="63d22-117">The reclassification transaction uses information from the original posted acquisition that includes financial dimension information that is included in the acquisition transaction.</span></span>  
   
   - <span data-ttu-id="63d22-118">Á sama tíma snýr endurflokkunarferlið við upphaflegu eignakaupunum og eignaflutningsfærslunni.</span><span class="sxs-lookup"><span data-stu-id="63d22-118">At the same time, the reclassification process reverses the original asset acquisition and asset transfer transaction.</span></span> 

<span data-ttu-id="63d22-119">Eftirfarandi mynd og aðferð gefur dæmi um endurflokkunarferlið.</span><span class="sxs-lookup"><span data-stu-id="63d22-119">The following diagram and procedure provide an example of the reclassification process.</span></span> 

<span data-ttu-id="63d22-120">[![Mynd sem sýnir endurflokkunarferlið](../media/reclassification-process-01.png)](../media/reclassification-process-01.png)</span><span class="sxs-lookup"><span data-stu-id="63d22-120">[![Diagram showing the reclassicification process](../media/reclassification-process-01.png)](../media/reclassification-process-01.png)</span></span>

<span data-ttu-id="63d22-121">Fylgið þessum skrefum til að endurflokka eign:</span><span class="sxs-lookup"><span data-stu-id="63d22-121">Follow these steps to reclassify a fixed asset:</span></span>

1. <span data-ttu-id="63d22-122">Fara í **Eignir > Reglubundin verkefni > Endurflokkun.**</span><span class="sxs-lookup"><span data-stu-id="63d22-122">Go to **Fixed assets > Periodic tasks > Reclassification.**</span></span>
2. <span data-ttu-id="63d22-123">Í svæðinu **Eignaflokkur** skal velja flokk til að endurflokka.</span><span class="sxs-lookup"><span data-stu-id="63d22-123">In the **Fixed asset group** field, select the group to reclassify.</span></span>
3. <span data-ttu-id="63d22-124">Í svæði **Eignanúmer** skal velja eign sem endurflokka.</span><span class="sxs-lookup"><span data-stu-id="63d22-124">In the **Fixed asset number** field, select the fixed asset to reclassify.</span></span>
4. <span data-ttu-id="63d22-125">Í reitnum **Nýr eignaflokkur** skal velja flokk til að flytja eign í.</span><span class="sxs-lookup"><span data-stu-id="63d22-125">In the **New fixed asset group** field, select a group to transfer the fixed asset to.</span></span>
    * <span data-ttu-id="63d22-126">Ef nýr eignaflokkur er festur við númeraröð er svæði **Nýtt eignanúmer** uppfærður með númer úr númeraröð nýtt eignaflokkur.</span><span class="sxs-lookup"><span data-stu-id="63d22-126">If the new fixed asset group is attached to a number sequence, the **New fixed asset number** field is updated with the number from the new fixed asset group number sequence.</span></span> <span data-ttu-id="63d22-127">Annars er svæðið **Nýtt eignanúmer** uppfært með númeri úr númeraröð sem er sett upp á síðunni **Færibreytur eigna**.</span><span class="sxs-lookup"><span data-stu-id="63d22-127">Otherwise, the **New fixed asset number** field is updated with the number from the number sequence that is set up on the **Fixed asset parameters** page.</span></span> <span data-ttu-id="63d22-128">Ef númeraröð er ekki sett upp á síðunni **Færibreytur eigna** skal slá inn númerið í svæðinu **Nýtt eignanúmer**.</span><span class="sxs-lookup"><span data-stu-id="63d22-128">If a number sequence is not set up on the **Fixed asset parameters** page, enter a number in the **New fixed asset number** field.</span></span>  
5. <span data-ttu-id="63d22-129">Í svæði **Dagsetning endurflokkunar** skal slá inn dagsetning.</span><span class="sxs-lookup"><span data-stu-id="63d22-129">In the **Reclassification date** field, enter a date.</span></span>
6. <span data-ttu-id="63d22-130">Í reitinn **fylgiskjalaruna** skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="63d22-130">In the **Voucher series** field, enter or select a value.</span></span>
7. <span data-ttu-id="63d22-131">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="63d22-131">Select **OK**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
