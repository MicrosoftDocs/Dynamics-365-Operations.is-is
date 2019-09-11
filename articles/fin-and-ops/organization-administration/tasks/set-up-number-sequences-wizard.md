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
ms.openlocfilehash: f97c4cd6cdb117ebdd67a155478bb6f8d1703541
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867392"
---
# <a name="set-up-number-sequences-using-a-wizard"></a><span data-ttu-id="7e9da-103">Uppsetning númeraraða með leiðsögn</span><span class="sxs-lookup"><span data-stu-id="7e9da-103">Set up number sequences using a wizard</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7e9da-104">Númeraraðir eru notaðar til að mynda lesanleg, einkvæm kenni fyrir skýrslur aðalgagna og færslur sem krefjast þeirra.</span><span class="sxs-lookup"><span data-stu-id="7e9da-104">Number sequences are used to generate readable, unique identifiers for master data records and transaction records that require them.</span></span> <span data-ttu-id="7e9da-105">Skýrsla aðalgagna eða færslu sem krefst kennis er kölluð Tilvísun.</span><span class="sxs-lookup"><span data-stu-id="7e9da-105">A master data or transaction record that requires an identifier is referred to as a reference.</span></span> <span data-ttu-id="7e9da-106">Áður en hægt er að stofna nýjar færslur fyrir tilvísun verður að setja upp númeraröð og tengja hana við tilvísunina.</span><span class="sxs-lookup"><span data-stu-id="7e9da-106">Before you can create new records for a reference, you must set up a number sequence and associate it with the reference.</span></span> <span data-ttu-id="7e9da-107">Þetta efni útskýrir hvernig á að setja upp allar nauðsynlegar númeraraðir á sama tíma með því að nota leiðsagnarforrit.</span><span class="sxs-lookup"><span data-stu-id="7e9da-107">This topic explains how to set up all required number sequences at the same time by using a wizard.</span></span> <span data-ttu-id="7e9da-108">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="7e9da-108">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="7e9da-109">Farðu í **Skoðunarrúða > Kerfiseiningar > Fyrirtækjastjórnun > Númeraraðir > Númeraraðir**.</span><span class="sxs-lookup"><span data-stu-id="7e9da-109">Go to **Navigation > Modules > Organization administration > Number sequences > Number sequences**.</span></span>
2. <span data-ttu-id="7e9da-110">Veldu **Stofna**.</span><span class="sxs-lookup"><span data-stu-id="7e9da-110">Select **Generate**.</span></span>
3. <span data-ttu-id="7e9da-111">Veljið **Næst**.</span><span class="sxs-lookup"><span data-stu-id="7e9da-111">Select **Next**.</span></span>

   - <span data-ttu-id="7e9da-112">Á þessari síðu er hægt að breyta kennikóðanum, lægsta gildi og hæsta gildi.</span><span class="sxs-lookup"><span data-stu-id="7e9da-112">On this page, you can modify the identification code, the lowest value, and the highest value.</span></span> <span data-ttu-id="7e9da-113">Auk þess er hægt að gefa til kynna hvort númeraröðin verður að vera samfelld.</span><span class="sxs-lookup"><span data-stu-id="7e9da-113">In addition, you can indicate whether the number sequence must be continuous.</span></span>   
   - <span data-ttu-id="7e9da-114">Ekki skal velja valkostinn **Viðvarandi** ef það þarf að forúthluta tölum fyrir númeraröð.</span><span class="sxs-lookup"><span data-stu-id="7e9da-114">Do not select the **Continuous** option if you must preallocate numbers for the number sequence.</span></span> <span data-ttu-id="7e9da-115">Til að bæta sviðshluta við í snið númeraraðar velurðu sniðið í listanum og velur síðan **Hafa umfang með í sniði**.</span><span class="sxs-lookup"><span data-stu-id="7e9da-115">To add a scope segment to the format of a number sequence, select the format in the list, and then select **Include scope in format**.</span></span> <span data-ttu-id="7e9da-116">Til að fjarlægja sviðshluta úr sniði númeraraðar velurðu sniðið í listanum og velur síðan **Fjarlægja umfang úr sniði**.</span><span class="sxs-lookup"><span data-stu-id="7e9da-116">To remove a scope segment from the format of a number sequence, select the format in the list, and then select **Remove scope from format**.</span></span> <span data-ttu-id="7e9da-117">Til að undanskilja númeraröð úr sjálfvirkri myndun velurðu númeraröð í listanum og velur síðan **Eyða**.</span><span class="sxs-lookup"><span data-stu-id="7e9da-117">To exclude a number sequence from automatic generation, select the number sequence in the list, and then select **Delete**.</span></span>  

4. <span data-ttu-id="7e9da-118">Veljið **Næst**.</span><span class="sxs-lookup"><span data-stu-id="7e9da-118">Select **Next**.</span></span>
5. <span data-ttu-id="7e9da-119">Veljið **Ljúka**.</span><span class="sxs-lookup"><span data-stu-id="7e9da-119">Select **Finish**.</span></span>

