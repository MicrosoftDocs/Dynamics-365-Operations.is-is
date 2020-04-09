---
title: Uppsetning númeraraða með leiðsögn
description: Þetta efni útskýrir hvernig á að setja upp allar nauðsynlegar númeraraðir á sama tíma með því að nota leiðsagnarforrit.
author: sericks007
manager: AnnBe
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: NumberSequenceTableListPage, NumberSequenceWizard
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 76dc32f2254ffd2a2e33eef594d6e602092bcb6f
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140500"
---
# <a name="set-up-number-sequences-using-a-wizard"></a><span data-ttu-id="d2c97-103">Uppsetning númeraraða með leiðsögn</span><span class="sxs-lookup"><span data-stu-id="d2c97-103">Set up number sequences using a wizard</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d2c97-104">Númeraraðir eru notaðar til að mynda lesanleg, einkvæm kenni fyrir skýrslur aðalgagna og færslur sem krefjast þeirra.</span><span class="sxs-lookup"><span data-stu-id="d2c97-104">Number sequences are used to generate readable, unique identifiers for master data records and transaction records that require them.</span></span> <span data-ttu-id="d2c97-105">Skýrsla aðalgagna eða færslu sem krefst kennis er kölluð Tilvísun.</span><span class="sxs-lookup"><span data-stu-id="d2c97-105">A master data or transaction record that requires an identifier is referred to as a reference.</span></span> <span data-ttu-id="d2c97-106">Áður en hægt er að stofna nýjar færslur fyrir tilvísun verður að setja upp númeraröð og tengja hana við tilvísunina.</span><span class="sxs-lookup"><span data-stu-id="d2c97-106">Before you can create new records for a reference, you must set up a number sequence and associate it with the reference.</span></span> <span data-ttu-id="d2c97-107">Þetta efni útskýrir hvernig á að setja upp allar nauðsynlegar númeraraðir á sama tíma með því að nota leiðsagnarforrit.</span><span class="sxs-lookup"><span data-stu-id="d2c97-107">This topic explains how to set up all required number sequences at the same time by using a wizard.</span></span> <span data-ttu-id="d2c97-108">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="d2c97-108">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="d2c97-109">Farðu í **Skoðunarrúða > Kerfiseiningar > Fyrirtækjastjórnun > Númeraraðir > Númeraraðir**.</span><span class="sxs-lookup"><span data-stu-id="d2c97-109">Go to **Navigation > Modules > Organization administration > Number sequences > Number sequences**.</span></span>
2. <span data-ttu-id="d2c97-110">Veldu **Stofna**.</span><span class="sxs-lookup"><span data-stu-id="d2c97-110">Select **Generate**.</span></span>
3. <span data-ttu-id="d2c97-111">Veljið **Næst**.</span><span class="sxs-lookup"><span data-stu-id="d2c97-111">Select **Next**.</span></span>

   - <span data-ttu-id="d2c97-112">Á þessari síðu er hægt að breyta kennikóðanum, lægsta gildi og hæsta gildi.</span><span class="sxs-lookup"><span data-stu-id="d2c97-112">On this page, you can modify the identification code, the lowest value, and the highest value.</span></span> <span data-ttu-id="d2c97-113">Auk þess er hægt að gefa til kynna hvort númeraröðin verður að vera samfelld.</span><span class="sxs-lookup"><span data-stu-id="d2c97-113">In addition, you can indicate whether the number sequence must be continuous.</span></span>   
   - <span data-ttu-id="d2c97-114">Ekki skal velja valkostinn **Viðvarandi** ef það þarf að forúthluta tölum fyrir númeraröð.</span><span class="sxs-lookup"><span data-stu-id="d2c97-114">Do not select the **Continuous** option if you must preallocate numbers for the number sequence.</span></span> <span data-ttu-id="d2c97-115">Til að bæta sviðshluta við í snið númeraraðar velurðu sniðið í listanum og velur síðan **Hafa umfang með í sniði**.</span><span class="sxs-lookup"><span data-stu-id="d2c97-115">To add a scope segment to the format of a number sequence, select the format in the list, and then select **Include scope in format**.</span></span> <span data-ttu-id="d2c97-116">Til að fjarlægja sviðshluta úr sniði númeraraðar velurðu sniðið í listanum og velur síðan **Fjarlægja umfang úr sniði**.</span><span class="sxs-lookup"><span data-stu-id="d2c97-116">To remove a scope segment from the format of a number sequence, select the format in the list, and then select **Remove scope from format**.</span></span> <span data-ttu-id="d2c97-117">Til að undanskilja númeraröð úr sjálfvirkri myndun velurðu númeraröð í listanum og velur síðan **Eyða**.</span><span class="sxs-lookup"><span data-stu-id="d2c97-117">To exclude a number sequence from automatic generation, select the number sequence in the list, and then select **Delete**.</span></span>  

4. <span data-ttu-id="d2c97-118">Veljið **Næst**.</span><span class="sxs-lookup"><span data-stu-id="d2c97-118">Select **Next**.</span></span>
5. <span data-ttu-id="d2c97-119">Veljið **Ljúka**.</span><span class="sxs-lookup"><span data-stu-id="d2c97-119">Select **Finish**.</span></span>

