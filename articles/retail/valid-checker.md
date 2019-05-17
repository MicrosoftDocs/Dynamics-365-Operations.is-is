---
title: Samræmisprófun smásölufærslna
description: Þetta efnisatriði lýsir virkni samræmisprófunar smásölufærslna í Microsoft Dynamics 365 for Retail.
author: josaw1
manager: AnnBe
ms.date: 01/08/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: 972c4d6b244eebc85cc801353ce8fb25ecbc0655
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517090"
---
# <a name="retail-transaction-consistency-checker"></a><span data-ttu-id="67ce1-103">Samræmisprófun smásölufærslna</span><span class="sxs-lookup"><span data-stu-id="67ce1-103">Retail transaction consistency checker</span></span>


[!include [banner](includes/banner.md)]
[!include [preview banner](includes/preview-banner.md)]

<span data-ttu-id="67ce1-104">Þetta efnisatriði lýsir virkni samræmisprófunar smásölufærslna sem kynnt var til sögunnar í Microsoft Dynamics 365 for Finance and Operations útgáfu 8.1.3.</span><span class="sxs-lookup"><span data-stu-id="67ce1-104">This topic describes the retail transaction consistency checker functionality introduced in Microsoft Dynamics 365 for Finance and Operations version 8.1.3.</span></span> <span data-ttu-id="67ce1-105">Í samræmisprófuninni eru færslur með ósamræmi greindar og einangraðar áður en þær eru teknar inn í bókunarferlið.</span><span class="sxs-lookup"><span data-stu-id="67ce1-105">The consistency checker identifies and isolates inconsistent transactions before they are picked up by the statement posting process.</span></span>

<span data-ttu-id="67ce1-106">Þegar uppgjör er bókað í Retail getur birtingin mistekist vegna ósamstæðra gagna í færslutöflum.</span><span class="sxs-lookup"><span data-stu-id="67ce1-106">When a statement is posted in Retail, posting can fail due to inconsistent data in the retail transaction tables.</span></span> <span data-ttu-id="67ce1-107">Gagnavillan getur orðið vegna ófyrirséðra vandamála í forritinu á sölustað (POS) eða vegna villu í flutningi færslna úr sölustaðarkerfi þriðju aðila.</span><span class="sxs-lookup"><span data-stu-id="67ce1-107">The data issue may be caused by by unforeseen issues in the point of sale (POS) application, or if transactions were incorrectly imported from third-party POS systems.</span></span> <span data-ttu-id="67ce1-108">Dæmi um þessi ósamræmi eru meðal annars:</span><span class="sxs-lookup"><span data-stu-id="67ce1-108">Examples of how these inconsistencies may appear include:</span></span> 

  - <span data-ttu-id="67ce1-109">Heildarfærsla í haustöflu er ekki í samræmi við heildarfærslu í línunum.</span><span class="sxs-lookup"><span data-stu-id="67ce1-109">The transaction total on the header table does not match the transaction total on the lines.</span></span>
  - <span data-ttu-id="67ce1-110">Línufjöldi í haustöflu er ekki í samræmi við fjölda lína í færslutöflunni.</span><span class="sxs-lookup"><span data-stu-id="67ce1-110">The line count on the header table does not match with the number of lines in the transaction table.</span></span>
  - <span data-ttu-id="67ce1-111">Skattar í haustöflu eru ekki í samræmi við skattupphæð í línunum.</span><span class="sxs-lookup"><span data-stu-id="67ce1-111">Taxes on the header table do not match the tax amount on the lines.</span></span> 
  
<span data-ttu-id="67ce1-112">Þegar færslur með ósamræmi eru teknar inn í bókunarferlið verða til sölureikningar og greiðslubækur með ósamræmi og villa kemur upp í öllu bókunarferlinu.</span><span class="sxs-lookup"><span data-stu-id="67ce1-112">When inconsistent transactions are picked up by the statement posting process, inconsistent sales invoices and payment journals are created, and the entire statement posting process fails as a result.</span></span> <span data-ttu-id="67ce1-113">Í því tilfelli þarf flóknar gagnaleiðréttingar í mörgum færslutöflum til að endurheimta færslurnar.</span><span class="sxs-lookup"><span data-stu-id="67ce1-113">Recovering the statements from such a state involves complex data fixes across multiple transaction tables.</span></span> <span data-ttu-id="67ce1-114">Samræmisprófun smásölufærslna kemur í veg fyrir slík vandamál.</span><span class="sxs-lookup"><span data-stu-id="67ce1-114">The retail transaction consistency checker prevents such issues.</span></span>

<span data-ttu-id="67ce1-115">Eftirfarandi tafla sýnir bókunarferli með samræmisprófun smásölufærslna.</span><span class="sxs-lookup"><span data-stu-id="67ce1-115">The following chart illustrates the posting process with the transaction consistency checker.</span></span>

<span data-ttu-id="67ce1-116">![Bókunarferli uppgjörs með samræmisprófun smásölufærslna](./media/validchecker.png "Bókunarferli uppgjörs með samræmisprófun smásölufærslna")</span><span class="sxs-lookup"><span data-stu-id="67ce1-116">![Statement posting process with retail transaction consistency checker](./media/validchecker.png "Statement posting process with retail transaction consistency checker")</span></span>

<span data-ttu-id="67ce1-117">Með runuvinnslunni **Villuleita í færslum verslunar** er samræmi smásölufærslutaflna athugað við eftirfarandi aðstæður.</span><span class="sxs-lookup"><span data-stu-id="67ce1-117">The **Validate store transactions** batch process checks the consistency of the retail transaction tables for the following scenarios.</span></span>

- <span data-ttu-id="67ce1-118">Viðskiptavinalykill - Staðfestir að viðskiptavinalykillinn í smásölufærslutöflunum sé til staðar í HQ-aðalgögnum viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="67ce1-118">Customer account - Validates that the customer account in the retail transaction tables exists in the HQ customer master.</span></span>
- <span data-ttu-id="67ce1-119">Línufjöldi - Staðfestir að línufjöldi, samkvæmt haustöflu færslna, sé í samræmi við fjölda lína í sölufærslutöflunum.</span><span class="sxs-lookup"><span data-stu-id="67ce1-119">Line count - Validates that the number of lines, as captured on the transaction header table, matches the number of lines in the sales transaction tables.</span></span>

## <a name="set-up-the-consistency-checker"></a><span data-ttu-id="67ce1-120">Setja upp samræmisprófun</span><span class="sxs-lookup"><span data-stu-id="67ce1-120">Set up the consistency checker</span></span>
<span data-ttu-id="67ce1-121">Skilgreina skal runuvinnsluna „Villuleita í færslum verslunar“ í **Smásölu \> Upplýsingatækni smásölu \> Sölustaðarbókun** til að keyra vinnsluna reglulega.</span><span class="sxs-lookup"><span data-stu-id="67ce1-121">Configure the "Validate store transactions" batch process, at **Retail \> Retail IT \> POS posting**, for periodic runs.</span></span> <span data-ttu-id="67ce1-122">Hægt er að skipuleggja runuvinnsluna á grundvelli stigveldis verslunarinnar, svipað því hvernig ferlin „Reikna uppgjör í runu“ og „Bóka uppgjör í runu“ eru sett upp.</span><span class="sxs-lookup"><span data-stu-id="67ce1-122">The batch job can be scheduled based on store organization hierarchy, similar to how the "Calculate statement in batch" and "Post statement in batch" processes are set up.</span></span> <span data-ttu-id="67ce1-123">Við mælum með að þú stillir runuvinnsluna þannig að hún sé keyrð oft á dag og að loknu hverju P-verki.</span><span class="sxs-lookup"><span data-stu-id="67ce1-123">We recommend that you configure this batch process to run multiple times in a day and schedule it so that it runs at the end of every P-job execution.</span></span>

## <a name="results-of-validation-process"></a><span data-ttu-id="67ce1-124">Niðurstöður villuleitar</span><span class="sxs-lookup"><span data-stu-id="67ce1-124">Results of validation process</span></span>
<span data-ttu-id="67ce1-125">Niðurstöðum villuleitar er bætt við viðkomandi smásölufærslu.</span><span class="sxs-lookup"><span data-stu-id="67ce1-125">The results of the validation check by the batch process are tagged on the appropriate retail transaction.</span></span> <span data-ttu-id="67ce1-126">Svæðið **Staða villuleitar** í viðkomandi uppgjörsfærslu er ýmist stillt á **Lokið** eða **Villa** og dagsetning síðustu villuleitar birtist á svæðinu **Tími síðustu villuleitar**.</span><span class="sxs-lookup"><span data-stu-id="67ce1-126">The **Validation status** field on the retail transaction record is either set to **Successful** or **Error**, and the date of the last validation run appears on the **Last validation time** field.</span></span>

<span data-ttu-id="67ce1-127">Til að sjá nákvæmari villuboðatexta sem tengist villu í villuleit skal velja viðkomandi færsluskrá smásöluverslunar og smella á hnappinn **Villur við villuleit**.</span><span class="sxs-lookup"><span data-stu-id="67ce1-127">To view more descriptive error text relating to a validation failure, select the relevant retail store transaction record and click the **Validation errors** button.</span></span>

<span data-ttu-id="67ce1-128">Færslur sem standast ekki villuleit og færslur sem enn á eftir að villuleita í eru ekki teknar inn í uppgjör.</span><span class="sxs-lookup"><span data-stu-id="67ce1-128">Transactions that fail the validation check and transactions that have not yet been validated will not be pulled into statements.</span></span> <span data-ttu-id="67ce1-129">Í ferlinu „Reikna uppgjör“ fá notendur tilkynningu um færslur sem eru ekki með í uppgjörinu en hefðu getað verið það.</span><span class="sxs-lookup"><span data-stu-id="67ce1-129">During the "Calculate statement" process, users will be notified if there are transactions that could have been included in the statement but weren't.</span></span>

<span data-ttu-id="67ce1-130">Ef villa finnst við villuleit er einungis hægt að lagfæra hana með því að hafa samband við notendaþjónustu Microsoft.</span><span class="sxs-lookup"><span data-stu-id="67ce1-130">If a validation error is found, the only way to fix the error is to contact Microsoft Support.</span></span> <span data-ttu-id="67ce1-131">Í síðari útgáfu munu notendur geta lagfært skrár með villum í notendaviðmótinu.</span><span class="sxs-lookup"><span data-stu-id="67ce1-131">In a future release, capability will be added so that users can fix the records that failed through the user interface.</span></span> <span data-ttu-id="67ce1-132">Einnig bætast við endurskoðunar- og skráningareiginleikar til að rekja breytingarsöguna.</span><span class="sxs-lookup"><span data-stu-id="67ce1-132">Logging and auditing capabilities will also be made available to trace the history of the modifications.</span></span>

> [!NOTE]
> <span data-ttu-id="67ce1-133">Frekari villuleitarreglum til að styðja við fleiri aðstæður verður bætt við í síðari útgáfu.</span><span class="sxs-lookup"><span data-stu-id="67ce1-133">Additional validation rules to support more scenarios will be added in a future release.</span></span>
