--- 
title: "Setja upp greiðslumáta fyrir ISO20022-beingreiðslur"
description: "Þessi verklýsing sýnir hvernig á að setja upp greiðsluhátt viðskiptavinar fyrir ISO20022 beingreiðsla eða hvers kyns aðra greiðslugerð sem notar rafræn skýrslugerð."
author: mrolecki
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: aa159fdf8a8ef543c338546a389d37e1644676a3
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---
# <a name="set-up-method-of-payment-for-iso20022-direct-debit"></a><span data-ttu-id="b753f-103">Setja upp greiðslumáta fyrir ISO20022-beingreiðslur</span><span class="sxs-lookup"><span data-stu-id="b753f-103">Set up method of payment for ISO20022 direct debit</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b753f-104">Þessi verklýsing sýnir hvernig á að setja upp greiðsluhátt viðskiptavinar fyrir ISO20022 beingreiðsla eða hvers kyns aðra greiðslugerð sem notar rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="b753f-104">This procedure shows how to set up the customer method of payment for ISO20022 direct debit or any other payment type using electronic reporting.</span></span> 



<span data-ttu-id="b753f-105">Áður en lokið er við þetta verkefni verður að hafa skilgreiningu útflutningssniðs og greiðslulyklar sett upp.</span><span class="sxs-lookup"><span data-stu-id="b753f-105">Before you complete this task, you must set up export format configurations and payment accounts.</span></span>



<span data-ttu-id="b753f-106">Þetta ferli var stofnuð með því að nota sýnigögn fyrirtækisins DEMF.</span><span class="sxs-lookup"><span data-stu-id="b753f-106">This procedure was created using the demo data company DEMF.</span></span>



<span data-ttu-id="b753f-107">Þetta er þriðja af fimm ferlum sem lýsa greiðsluferlinu viðskiptavinar með grunnstillingar fyrir rafræna skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="b753f-107">This is the third of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>

1. <span data-ttu-id="b753f-108">Farðu í Viðskiptakröfur > Greiðsluuppsetning > Greiðsluhættir.</span><span class="sxs-lookup"><span data-stu-id="b753f-108">Go to Accounts receivable > Payments setup > Methods of payment.</span></span>
2. <span data-ttu-id="b753f-109">Nota flýtiafmörkun til að finna færslur</span><span class="sxs-lookup"><span data-stu-id="b753f-109">Use the Quick Filter to find records.</span></span> <span data-ttu-id="b753f-110">Til dæmis síu á í Greiðsluaðferðarsvæðinu með gildið 'RAFRÆNA'.</span><span class="sxs-lookup"><span data-stu-id="b753f-110">For example, filter on the Method of payment field with a value of 'ELECTRONIC'.</span></span>
3. <span data-ttu-id="b753f-111">Smella á Breyta.</span><span class="sxs-lookup"><span data-stu-id="b753f-111">Click Edit.</span></span>
4. <span data-ttu-id="b753f-112">Tilgreindu gildi 'DEMF OPER' í svæði greiðslulykils.</span><span class="sxs-lookup"><span data-stu-id="b753f-112">In the Payment account field, specify the values 'DEMF OPER'.</span></span>
5. <span data-ttu-id="b753f-113">Útvíkka hlutann Skráarsnið.</span><span class="sxs-lookup"><span data-stu-id="b753f-113">Expand the File formats section.</span></span>
6. <span data-ttu-id="b753f-114">Velja skal Já í Almennan rafræna skýrslugerð svæði.</span><span class="sxs-lookup"><span data-stu-id="b753f-114">Select Yes in the Generic electronic reporting field.</span></span>
7. <span data-ttu-id="b753f-115">Færa inn eða velja gildi í reitnum skilgreiningu útflutningssniðs.</span><span class="sxs-lookup"><span data-stu-id="b753f-115">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="b753f-116">Á listanum, veljið ISO20022 beingreiðsla (DE).</span><span class="sxs-lookup"><span data-stu-id="b753f-116">In the list, select ISO20022 Direct debit (DE).</span></span>  <span data-ttu-id="b753f-117">Ef listi er auður er skilgreining greiðsluútflutnings viðskiptavinar ekki innfluttu og virkt.</span><span class="sxs-lookup"><span data-stu-id="b753f-117">If the list is empty, the customer payment export format configuration has not been imported and active.</span></span>  
8. <span data-ttu-id="b753f-118">Velja skal Já í svæðinu krefjast umboðs.</span><span class="sxs-lookup"><span data-stu-id="b753f-118">Select Yes in the Require mandate field.</span></span>
    * <span data-ttu-id="b753f-119">Veljið færibreyturna krefjarst umboðs fyrir greiðslusnið viðskiptavinar, sem krefjast þess að innifela upplýsingar um umboð í greiðskuskilaboðunum, eins og Sepa-beingreiðsla.</span><span class="sxs-lookup"><span data-stu-id="b753f-119">Select the Require mandate parameter for customer payment formats, which require including mandate information in the payment message, like SEPA direct debit.</span></span>  
9. <span data-ttu-id="b753f-120">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="b753f-120">Click Save.</span></span>


