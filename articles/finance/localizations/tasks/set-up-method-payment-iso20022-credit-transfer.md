---
title: Setja upp greiðslumáta fyrir ISO20022-kreditfærslu
description: Þessi verklýsing sýnir hvernig á að setja upp greiðsluhátt lánardrottins fyrir ISO20022 millifærsla fjármuna eða hvers kyns aðra greiðslugerð sem notar rafræn skýrslugerð til að mynda skrá.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPaymMode
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8bb54864c8d0a57510b4d47b00aed60c5be95512
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174909"
---
# <a name="set-up-method-of-payment-for-iso20022-credit-transfer"></a><span data-ttu-id="6f981-103">Setja upp greiðslumáta fyrir ISO20022-kreditfærslu</span><span class="sxs-lookup"><span data-stu-id="6f981-103">Set up method of payment for ISO20022 credit transfer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6f981-104">Þessi verklýsing sýnir hvernig á að setja upp greiðsluhátt lánardrottins fyrir ISO20022 millifærsla fjármuna eða hvers kyns aðra greiðslugerð sem notar rafræn skýrslugerð til að mynda skrá.</span><span class="sxs-lookup"><span data-stu-id="6f981-104">This procedure shows how to set up the vendor method of payment for ISO20022 credit transfer or any other payment type using electronic reporting to generate a file.</span></span> 

<span data-ttu-id="6f981-105">Áður en lokið er við þetta verkefni verður að flytja út skilgreiningu útflutningssniðs og setja upp greiðslulykla.</span><span class="sxs-lookup"><span data-stu-id="6f981-105">Before you complete this task, you must export format configurations and set up payment accounts.</span></span>

<span data-ttu-id="6f981-106">Þetta verkefni var stofnuð með DEMF sýnigögn fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="6f981-106">This task was created using the DEMF demo data company.</span></span>

<span data-ttu-id="6f981-107">Þetta þriðja ferli af fimm sem sýna greiðsluferlinu lánardrottins með því að nota grunnstillingar fyrir rafræna skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="6f981-107">This is the third procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="6f981-108">Þetta ferli er fyrir eiginleika sem var bætt við í Dynamics 365 for Operations, útgáfu 1611.</span><span class="sxs-lookup"><span data-stu-id="6f981-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="6f981-109">Fara í Viðskiptakröfur > Greiðsluuppsetning > Greiðsluhættir.</span><span class="sxs-lookup"><span data-stu-id="6f981-109">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
2. <span data-ttu-id="6f981-110">Nota flýtiafmörkun til að finna færslur</span><span class="sxs-lookup"><span data-stu-id="6f981-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="6f981-111">Til dæmis síu á í Greiðsluaðferðarsvæðinu með gildið 'SEPA CT'.</span><span class="sxs-lookup"><span data-stu-id="6f981-111">For example, filter on the Method of payment field with a value of 'SEPA CT'.</span></span>
3. <span data-ttu-id="6f981-112">Smella á Breyta.</span><span class="sxs-lookup"><span data-stu-id="6f981-112">Click Edit.</span></span>
4. <span data-ttu-id="6f981-113">Í svæðinu tímabil skal velja ‚samtala'.</span><span class="sxs-lookup"><span data-stu-id="6f981-113">In the Period field, select 'Total'.</span></span>
5. <span data-ttu-id="6f981-114">Veljið 'Rafræna greiðslu' í svæðinu Greiðslu.</span><span class="sxs-lookup"><span data-stu-id="6f981-114">In the Payment type field, select 'Electronic payment'.</span></span>
6. <span data-ttu-id="6f981-115">Útvíkka hlutann Skráarsnið.</span><span class="sxs-lookup"><span data-stu-id="6f981-115">Expand the File formats section.</span></span>
7. <span data-ttu-id="6f981-116">Velja skal Já í Almennan rafræna skýrslugerð svæði.</span><span class="sxs-lookup"><span data-stu-id="6f981-116">Select Yes in the Generic electronic reporting field.</span></span>
8. <span data-ttu-id="6f981-117">Færa inn eða velja gildi í reitnum skilgreiningu útflutningssniðs.</span><span class="sxs-lookup"><span data-stu-id="6f981-117">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="6f981-118">Á listanum, veljið gildi ISO20022 kreditfærsla (DE).</span><span class="sxs-lookup"><span data-stu-id="6f981-118">In the list, select the value ISO20022 Credit transfer (DE).</span></span> <span data-ttu-id="6f981-119">Ef listi er auður er skilgreining greiðsluútflutnings lánardrottins ekki innfluttu og virkt.</span><span class="sxs-lookup"><span data-stu-id="6f981-119">If the list is empty, the vendor payment export format configuration is not imported and active.</span></span>  
9. <span data-ttu-id="6f981-120">Veljið 'Banki' í svæðinu gerð lykils.</span><span class="sxs-lookup"><span data-stu-id="6f981-120">In the Account type field, select 'Bank'.</span></span>
10. <span data-ttu-id="6f981-121">Tilgreindu gildi 'DEMF OPER' í svæði greiðslulykils.</span><span class="sxs-lookup"><span data-stu-id="6f981-121">In the Payment account field, specify the values 'DEMF OPER'.</span></span>
11. <span data-ttu-id="6f981-122">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="6f981-122">Click Save.</span></span>
