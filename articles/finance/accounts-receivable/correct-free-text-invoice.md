---
title: Leiðrétting textareiknings
description: Þessi grein útskýrir hvernig á að leiðrétta reikningur með frjálsum texta sem hefur verið bókaður og endurútgefa hann sem leiðréttan reikning.
author: ShivamPandey-msft
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: roschlom
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f04e70c9afb66be015ce18cebebd711f00d764b7
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827579"
---
# <a name="correct-a-free-text-invoice"></a><span data-ttu-id="1a24b-103">Leiðrétting textareiknings</span><span class="sxs-lookup"><span data-stu-id="1a24b-103">Correct a free text invoice</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1a24b-104">Þessi grein útskýrir hvernig á að leiðrétta reikningur með frjálsum texta sem hefur verið bókaður og endurútgefa hann sem leiðréttan reikning.</span><span class="sxs-lookup"><span data-stu-id="1a24b-104">This article explains how to correct a free text invoice that has been posted and reissue it as a corrected invoice.</span></span>

<span data-ttu-id="1a24b-105">Til að leiðrétta textareikning sem þegar hefur verið bókaður, skal opna bókaðan textareikning.</span><span class="sxs-lookup"><span data-stu-id="1a24b-105">To correct a free text invoice that has already been posted, open the posted free text invoice.</span></span> <span data-ttu-id="1a24b-106">Á síðunni **Reikningur** skal velja **Hætta við**, og veljið síðan **Leiðrétta reikning**.</span><span class="sxs-lookup"><span data-stu-id="1a24b-106">On the **Invoice** page, select **Cancel**, and then select **Correct invoice**.</span></span> <span data-ttu-id="1a24b-107">Velja ástæðukóða, bæta við athugasemd og veljið°dagsetningu fyrir nýjan leiðréttan reikning.</span><span class="sxs-lookup"><span data-stu-id="1a24b-107">Select a reason code, add comments, and select the date for new corrected invoice.</span></span> <span data-ttu-id="1a24b-108">Hægt er að breyta leiðrétta reikningnum og bóka hann.</span><span class="sxs-lookup"><span data-stu-id="1a24b-108">You can modify the corrected invoice, and post it.</span></span> 

<span data-ttu-id="1a24b-109">Þegar leiðrétti reikningurinn er bókaður, er afturköllunarreikningur stofnaður fyrir kredit-upphæð sem er jöfn upphaflegri upphæð reikningsins.</span><span class="sxs-lookup"><span data-stu-id="1a24b-109">When you post the corrected invoice, a canceling invoice is created for a credit amount that equals the original invoice amount.</span></span> <span data-ttu-id="1a24b-110">Þess vegna er samanlögð staða upprunalega reikningsins og afturköllunarreikningsins 0 (núll).</span><span class="sxs-lookup"><span data-stu-id="1a24b-110">Therefore, the combined balance of the original invoice and the canceling invoice is 0 (zero).</span></span> <span data-ttu-id="1a24b-111">Afturköllunarreikningurinn er jafnaður á móti upprunalega reikningnum.</span><span class="sxs-lookup"><span data-stu-id="1a24b-111">The canceling invoice is settled against the original invoice.</span></span> 

<span data-ttu-id="1a24b-112">Eftir að leiðrétti reikningurinn er bókaður, verða þrír reikningar:</span><span class="sxs-lookup"><span data-stu-id="1a24b-112">After you post the corrected invoice, you will have three invoices:</span></span>

-   <span data-ttu-id="1a24b-113">**Upprunalegi reikningurinn** – reikningurinn sem inniheldur upplýsingarnar sem verið er að leiðrétta.</span><span class="sxs-lookup"><span data-stu-id="1a24b-113">**Original invoice** – The invoice that includes the information that you're correcting.</span></span>
-   <span data-ttu-id="1a24b-114">**Afturköllunarreikningur** – kerfismyndaður kreditreikningur sem var stofnaður til að hætta við reikninginn sem var síðast leiðréttur.</span><span class="sxs-lookup"><span data-stu-id="1a24b-114">**Canceling invoice** – The system-generated credit invoice that was created to cancel the invoice that was most recently corrected.</span></span>
-   <span data-ttu-id="1a24b-115">**Leiðréttur reikningur** – reikningurinn sem inniheldur leiðréttar reikningsupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="1a24b-115">**Corrected invoice** – The invoice that contains the corrected invoice information.</span></span>

<span data-ttu-id="1a24b-116">Hægt er að þekkja afturköllunarreikninga og leiðrétta reikninga á tvo vegu:</span><span class="sxs-lookup"><span data-stu-id="1a24b-116">You can identify canceling and correcting invoices in two ways:</span></span>

-   <span data-ttu-id="1a24b-117">Síðan **Allir reikningar með frjálsum texta** inniheldur **Leiðrétting** dálk,°þar sem hægt er að sjá hvaða reikningar eru afturköllunarreikningar og leiðréttir reikningar.</span><span class="sxs-lookup"><span data-stu-id="1a24b-117">The **All free text invoices** page includes a **Correction** column, where you can see which invoices are canceling invoices and corrected invoices.</span></span>
-   <span data-ttu-id="1a24b-118">Haus textareikningsins sýnir stöðuna **Afturköllunarreikningur ‚\[reikningsnúmer\]'** eða **Leiðréttur reikningur '\[reikningsnúmer\]'**.</span><span class="sxs-lookup"><span data-stu-id="1a24b-118">The header of the free text invoice shows a status of **Cancelling invoice '\[invoice number\]'** or **Corrected invoice '\[invoice number\]'**.</span></span>

> [!NOTE]
> <span data-ttu-id="1a24b-119">Þessi aðgerð er bara tiltæk ef **Leiðrétting á textareikningi** skilgreiningarlykill er valinn.</span><span class="sxs-lookup"><span data-stu-id="1a24b-119">This feature is available only if the **Free text invoice correction** configuration key is selected.</span></span> <span data-ttu-id="1a24b-120">Nánari upplýsingar um hvernig á að virkja stillingarlyklana er að finna í hlutanum Virkja (eða slökkva) á stillingarlyklum í efninu [Viðhaldsstilling](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span><span class="sxs-lookup"><span data-stu-id="1a24b-120">For more information on how to enable Configuration keys refer to the Enable (or disable) configuration keys section in the [Maintenance mode](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) topic.</span></span> 





[!INCLUDE[footer-include](../../includes/footer-banner.md)]