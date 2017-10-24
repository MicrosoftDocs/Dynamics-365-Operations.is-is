--- 
title: "Setja upp númeraraðir með því að nota leiðsagnarforrit"
description: "Númeraraðir eru notaðar til að mynda lesanleg, einkvæm kenni fyrir skýrslur aðalgagna og færslur sem krefjast þeirra."
author: sericks007
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 96c1bc711350b447611977c3f2070fbc08fbae0f
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-number-sequences-by-using-a-wizard"></a><span data-ttu-id="260e1-103">Setja upp númeraraðir með því að nota leiðsagnarforrit</span><span class="sxs-lookup"><span data-stu-id="260e1-103">Set up number sequences by using a wizard</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="260e1-104">Númeraraðir eru notaðar til að mynda lesanleg, einkvæm kenni fyrir skýrslur aðalgagna og færslur sem krefjast þeirra.</span><span class="sxs-lookup"><span data-stu-id="260e1-104">Number sequences are used to generate readable, unique identifiers for master data records and transaction records that require them.</span></span> <span data-ttu-id="260e1-105">Skýrsla aðalgagna eða færslu sem krefst kennis er kölluð Tilvísun.</span><span class="sxs-lookup"><span data-stu-id="260e1-105">A master data or transaction record that requires an identifier is referred to as a reference.</span></span> <span data-ttu-id="260e1-106">Áður en hægt er að stofna nýjar færslur fyrir tilvísun verður að setja upp númeraröð og tengja hana við tilvísunina.</span><span class="sxs-lookup"><span data-stu-id="260e1-106">Before you can create new records for a reference, you must set up a number sequence and associate it with the reference.</span></span> <span data-ttu-id="260e1-107">Þessu ferli er útskýrt hvernig á að setja upp allar nauðsynlegar númeraraðir á sama tíma með því að nota leiðsagnarforrit.</span><span class="sxs-lookup"><span data-stu-id="260e1-107">This procedure explains how to set up all required number sequences at the same time by using a wizard.</span></span> <span data-ttu-id="260e1-108">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="260e1-108">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="260e1-109">Fara í Fyrirtækisstjórnun > Númeraröð > Númeraröð.</span><span class="sxs-lookup"><span data-stu-id="260e1-109">Go to Organization administration > Number sequences > Number sequences.</span></span>
2. <span data-ttu-id="260e1-110">Smellt er á Mynda.</span><span class="sxs-lookup"><span data-stu-id="260e1-110">Click Generate.</span></span>
3. <span data-ttu-id="260e1-111">Smelltu á Næsta.</span><span class="sxs-lookup"><span data-stu-id="260e1-111">Click Next.</span></span>
    * <span data-ttu-id="260e1-112">Á þessari síðu er hægt að breyta kennikóðanum, lægsta gildi og hæsta gildi.</span><span class="sxs-lookup"><span data-stu-id="260e1-112">On this page, you can modify the identification code, the lowest value, and the highest value.</span></span> <span data-ttu-id="260e1-113">Auk þess er hægt að gefa til kynna hvort númeraröðin verður að vera samfelld.</span><span class="sxs-lookup"><span data-stu-id="260e1-113">In addition, you can indicate whether the number sequence must be continuous.</span></span>   
    * <span data-ttu-id="260e1-114">Ekki skal velja valkostinn Viðvarandi ef það þarf að forúthluta tölum fyrir númeraröð.</span><span class="sxs-lookup"><span data-stu-id="260e1-114">Do not select the Continuous option if you must preallocate numbers for the number sequence.</span></span>     <span data-ttu-id="260e1-115">Til að bæta sviðshluta við í snið númeraraðar velurðu sniðið í listanum og smellir síðan á Hafa umfang með í sniði.</span><span class="sxs-lookup"><span data-stu-id="260e1-115">To add a scope segment to the format of a number sequence, select the format in the list, and then click Include scope in format.</span></span>     <span data-ttu-id="260e1-116">Til að fjarlægja sviðshluta úr sniði númeraraðar velurðu sniðið í listanum og smellir síðan á Fjarlægja umfang úr sniði.</span><span class="sxs-lookup"><span data-stu-id="260e1-116">To remove a scope segment from the format of a number sequence, select the format in the list, and then click Remove scope from format.</span></span>     <span data-ttu-id="260e1-117">Til að undanskilja númeraröð úr sjálfvirkri myndun velurðu númeraröð í listanum og smellir svo á Eyða.</span><span class="sxs-lookup"><span data-stu-id="260e1-117">To exclude a number sequence from automatic generation, select the number sequence in the list, and then click Delete.</span></span>  
4. <span data-ttu-id="260e1-118">Smelltu á Næsta.</span><span class="sxs-lookup"><span data-stu-id="260e1-118">Click Next.</span></span>
5. <span data-ttu-id="260e1-119">Smellt er á Ljúka.</span><span class="sxs-lookup"><span data-stu-id="260e1-119">Click Finish.</span></span>


