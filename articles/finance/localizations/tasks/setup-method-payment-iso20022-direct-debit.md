---
title: Setja upp greiðsluhátt fyrir ISO20022-beingreiðsla
description: Þessi verklýsing sýnir hvernig á að setja upp greiðsluhátt viðskiptavinar fyrir ISO20022 beingreiðsla eða hvers kyns aðra greiðslugerð sem notar rafræn skýrslugerð.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPaymMode
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a2ce4e1e960e04c0033990f99eb71897c7ea730f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208408"
---
# <a name="setup-method-of-payment-for-iso20022-direct-debit"></a><span data-ttu-id="38414-103">Setja upp greiðsluhátt fyrir ISO20022-beingreiðsla</span><span class="sxs-lookup"><span data-stu-id="38414-103">Setup method of payment for ISO20022 direct debit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="38414-104">Þessi verklýsing sýnir hvernig á að setja upp greiðsluhátt viðskiptavinar fyrir ISO20022 beingreiðsla eða hvers kyns aðra greiðslugerð sem notar rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="38414-104">This procedure shows how to set up the customer method of payment for ISO20022 direct debit or any other payment type using electronic reporting.</span></span> 



<span data-ttu-id="38414-105">Áður en lokið er við þetta verkefni verður að hafa skilgreiningu útflutningssniðs og greiðslulyklar sett upp.</span><span class="sxs-lookup"><span data-stu-id="38414-105">Before you complete this task, you must set up export format configurations and payment accounts.</span></span>



<span data-ttu-id="38414-106">Þetta ferli var stofnuð með því að nota sýnigögn fyrirtækisins DEMF.</span><span class="sxs-lookup"><span data-stu-id="38414-106">This procedure was created using the demo data company DEMF.</span></span>



<span data-ttu-id="38414-107">Þetta er þriðja af fimm ferlum sem lýsa greiðsluferlinu viðskiptavinar með grunnstillingar fyrir rafræna skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="38414-107">This is the third of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>

1. <span data-ttu-id="38414-108">Farðu í Viðskiptakröfur > Greiðsluuppsetning > Greiðsluhættir.</span><span class="sxs-lookup"><span data-stu-id="38414-108">Go to Accounts receivable > Payments setup > Methods of payment.</span></span>
2. <span data-ttu-id="38414-109">Nota flýtiafmörkun til að finna færslur</span><span class="sxs-lookup"><span data-stu-id="38414-109">Use the Quick Filter to find records.</span></span> <span data-ttu-id="38414-110">Til dæmis síu á í Greiðsluaðferðarsvæðinu með gildið 'RAFRÆNA'.</span><span class="sxs-lookup"><span data-stu-id="38414-110">For example, filter on the Method of payment field with a value of 'ELECTRONIC'.</span></span>
3. <span data-ttu-id="38414-111">Smella á Breyta.</span><span class="sxs-lookup"><span data-stu-id="38414-111">Click Edit.</span></span>
4. <span data-ttu-id="38414-112">Tilgreindu gildi 'DEMF OPER' í svæði greiðslulykils.</span><span class="sxs-lookup"><span data-stu-id="38414-112">In the Payment account field, specify the values 'DEMF OPER'.</span></span>
5. <span data-ttu-id="38414-113">Útvíkka hlutann Skráarsnið.</span><span class="sxs-lookup"><span data-stu-id="38414-113">Expand the File formats section.</span></span>
6. <span data-ttu-id="38414-114">Velja skal Já í Almennan rafræna skýrslugerð svæði.</span><span class="sxs-lookup"><span data-stu-id="38414-114">Select Yes in the Generic electronic reporting field.</span></span>
7. <span data-ttu-id="38414-115">Færa inn eða velja gildi í reitnum skilgreiningu útflutningssniðs.</span><span class="sxs-lookup"><span data-stu-id="38414-115">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="38414-116">Á listanum, veljið ISO20022 beingreiðsla (DE).</span><span class="sxs-lookup"><span data-stu-id="38414-116">In the list, select ISO20022 Direct debit (DE).</span></span>  <span data-ttu-id="38414-117">Ef listi er auður er skilgreining greiðsluútflutnings viðskiptavinar ekki innfluttu og virkt.</span><span class="sxs-lookup"><span data-stu-id="38414-117">If the list is empty, the customer payment export format configuration has not been imported and active.</span></span>  
8. <span data-ttu-id="38414-118">Velja skal Já í svæðinu krefjast umboðs.</span><span class="sxs-lookup"><span data-stu-id="38414-118">Select Yes in the Require mandate field.</span></span>
    * <span data-ttu-id="38414-119">Veljið færibreyturna krefjarst umboðs fyrir greiðslusnið viðskiptavinar, sem krefjast þess að innifela upplýsingar um umboð í greiðskuskilaboðunum, eins og Sepa-beingreiðsla.</span><span class="sxs-lookup"><span data-stu-id="38414-119">Select the Require mandate parameter for customer payment formats, which require including mandate information in the payment message, like SEPA direct debit.</span></span>  
9. <span data-ttu-id="38414-120">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="38414-120">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]