---
title: Afleiddar bækur
description: Þessi grein veitir yfirlit yfir notagildi afleidds Bók.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBookTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3401
ms.assetid: 862d6450-187b-497f-9822-cce45f2c65a9
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4a649fdbc355b3382bc6c80be03f8b37a06d5226
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178267"
---
# <a name="derived-books"></a><span data-ttu-id="e315f-103">Afleiddar bækur</span><span class="sxs-lookup"><span data-stu-id="e315f-103">Derived books</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e315f-104">Þessi grein veitir yfirlit yfir notagildi afleidds Bók.</span><span class="sxs-lookup"><span data-stu-id="e315f-104">This article provides an overview of derived book functionality.</span></span>

<span data-ttu-id="e315f-105">Tilgangur afleiddra bóka er að einfalda bókun á færslum bóka fasta eigna sem eru áætlaðar með reglulegu millibili.</span><span class="sxs-lookup"><span data-stu-id="e315f-105">The purpose of derived books is to simplify the posting of fixed asset book transactions that are planned for regular intervals.</span></span>  <span data-ttu-id="e315f-106">Eitt bók er valið sem aðalbók.</span><span class="sxs-lookup"><span data-stu-id="e315f-106">You choose one book as the primary book.</span></span> <span data-ttu-id="e315f-107">Þetta er venjulega bókin sem er notað fyrir bókhaldslegar afskriftir.</span><span class="sxs-lookup"><span data-stu-id="e315f-107">This usually is the book that is used for accounting depreciation.</span></span> <span data-ttu-id="e315f-108">Síðan er það tengt við önnur bækur sem eru sett upp til að bóka færslur á sömu tímabilum og bóka.</span><span class="sxs-lookup"><span data-stu-id="e315f-108">You then attach to it other books that are set up to post transactions in the same intervals as the primary book.</span></span> <span data-ttu-id="e315f-109">Bækur skattaafskrifta eru oft uppsett sem afleidd bækur.</span><span class="sxs-lookup"><span data-stu-id="e315f-109">Tax depreciation books are often set up as derived books.</span></span> 

<span data-ttu-id="e315f-110">Algengustu færslurnar sem eru settar upp til að bóka á afleiddar bækur eru kaup, leiðréttingar kaupa og losanir.</span><span class="sxs-lookup"><span data-stu-id="e315f-110">The most common transactions to set up to post to derived books are acquisitions, acquisition adjustments, and disposals.</span></span> 

## <a name="example"></a><span data-ttu-id="e315f-111">Dæmi</span><span class="sxs-lookup"><span data-stu-id="e315f-111">Example</span></span>

<span data-ttu-id="e315f-112">Bók B og bók C eru uppsett sem afleidd bækur fyrir bók A fyrir kaupfærslugerð.</span><span class="sxs-lookup"><span data-stu-id="e315f-112">Book B and book C are set up as derived books for book A for the Acquisition transaction type.</span></span> <span data-ttu-id="e315f-113">Fyrir Bók A er færð inn kaupfærsla fyrir eign 123 upp á 1.500,00.</span><span class="sxs-lookup"><span data-stu-id="e315f-113">In book A, you enter an acquisition transaction for asset 123 for 1,500.00.</span></span> 

<span data-ttu-id="e315f-114">Þegar færslan er bókuð er kaupfærsla mynduð og bókuð í eign 123 í fyrir bók B og í eign 123 fyrir bók C upp á 1.500,00.</span><span class="sxs-lookup"><span data-stu-id="e315f-114">When the transaction is posted, an acquisition transaction is generated and posted in asset 123 for book B and in asset 123 for book C for 1,500.00.</span></span> <span data-ttu-id="e315f-115">Þegar færslur aðalbókar eru búnar til fyrir bókun í eignabók, er einnig hægt að skoða og breyta færslum fyrir afleidd bækur.</span><span class="sxs-lookup"><span data-stu-id="e315f-115">When you prepare the transactions of the primary book for posting in the fixed asset journal, you can also view and modify the transactions of the derived books.</span></span> <span data-ttu-id="e315f-116">Þegar færslur aðalbókar eru búnar til í annarri bók, er ekki hægt að skoða færslur fyrir afleidd virðislíkön.</span><span class="sxs-lookup"><span data-stu-id="e315f-116">If you prepare the primary book transactions in another journal, the transactions of the derived value are not displayed.</span></span> <span data-ttu-id="e315f-117">Hins vegar eru þær bókaðar á viðeigandi lykla og bókunarlög þegar færslur aðalbókar eru bókaðar.</span><span class="sxs-lookup"><span data-stu-id="e315f-117">However, they are posted to the appropriate accounts and posting layers when you post the primary book transactions.</span></span>

> [!NOTE]                                                                                                                               
> <span data-ttu-id="e315f-118">Bækur sem eru uppsett til að bóka færslur með öðrum millibilum en aðalbókar verða að vera tengd eigninni sem aðskilin bækur en ekki sem afleidd bækur.</span><span class="sxs-lookup"><span data-stu-id="e315f-118">Books that are set up to post transactions at intervals other than the primary book intervals must be attached to the fixed asset as separate books and not as derived books.</span></span>  

<span data-ttu-id="e315f-119">Nánari upplýsingar eru í [Bókað í afleiddar bækur](post-derived-value-models.md).</span><span class="sxs-lookup"><span data-stu-id="e315f-119">For more information, see [Posting with derived books](post-derived-value-models.md).</span></span>


