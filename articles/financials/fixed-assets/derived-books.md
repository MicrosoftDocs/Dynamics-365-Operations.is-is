---
title: "Afleiddar bækur"
description: "Þessi grein veitir yfirlit yfir notagildi afleidds Bók."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetBookTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 3401
ms.assetid: 862d6450-187b-497f-9822-cce45f2c65a9
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 23b17c577fd2e0dfa6183929c86ed1950db8c50b
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---

# <a name="derived-books"></a><span data-ttu-id="92eb5-103">Afleiddar bækur</span><span class="sxs-lookup"><span data-stu-id="92eb5-103">Derived books</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="92eb5-104">Þessi grein veitir yfirlit yfir notagildi afleidds Bók.</span><span class="sxs-lookup"><span data-stu-id="92eb5-104">This article provides an overview of derived book functionality.</span></span>

<span data-ttu-id="92eb5-105">Tilgangur afleiddra bóka er að einfalda bókun á færslum bóka fasta eigna sem eru áætlaðar með reglulegu millibili.</span><span class="sxs-lookup"><span data-stu-id="92eb5-105">The purpose of derived books is to simplify the posting of fixed asset book transactions that are planned for regular intervals.</span></span>  <span data-ttu-id="92eb5-106">Eitt bók er valið sem aðalbók.</span><span class="sxs-lookup"><span data-stu-id="92eb5-106">You choose one book as the primary book.</span></span> <span data-ttu-id="92eb5-107">Þetta er venjulega bókin sem er notað fyrir bókhaldslegar afskriftir.</span><span class="sxs-lookup"><span data-stu-id="92eb5-107">This usually is the book that is used for accounting depreciation.</span></span> <span data-ttu-id="92eb5-108">Síðan er það tengt við önnur bækur sem eru sett upp til að bóka færslur á sömu tímabilum og bóka.</span><span class="sxs-lookup"><span data-stu-id="92eb5-108">You then attach to it other books that are set up to post transactions in the same intervals as the primary book.</span></span> <span data-ttu-id="92eb5-109">Bækur skattaafskrifta eru oft uppsett sem afleidd bækur.</span><span class="sxs-lookup"><span data-stu-id="92eb5-109">Tax depreciation books are often set up as derived books.</span></span> 

<span data-ttu-id="92eb5-110">Algengustu færslurnar sem eru settar upp til að bóka á afleiddar bækur eru kaup, leiðréttingar kaupa og losanir.</span><span class="sxs-lookup"><span data-stu-id="92eb5-110">The most common transactions to set up to post to derived books are acquisitions, acquisition adjustments, and disposals.</span></span> 

## <a name="example"></a><span data-ttu-id="92eb5-111">Dæmi</span><span class="sxs-lookup"><span data-stu-id="92eb5-111">Example</span></span>

<span data-ttu-id="92eb5-112">Bók B og bók C eru uppsett sem afleidd bækur fyrir bók A fyrir kaupfærslugerð.</span><span class="sxs-lookup"><span data-stu-id="92eb5-112">Book B and book C are set up as derived books for book A for the Acquisition transaction type.</span></span> <span data-ttu-id="92eb5-113">Fyrir Bók A er færð inn kaupfærsla fyrir eign 123 upp á 1.500,00.</span><span class="sxs-lookup"><span data-stu-id="92eb5-113">In book A, you enter an acquisition transaction for asset 123 for 1,500.00.</span></span> 

<span data-ttu-id="92eb5-114">Þegar færslan er bókuð er kaupfærsla mynduð og bókuð í eign 123 í fyrir bók B og í eign 123 fyrir bók C upp á 1.500,00.</span><span class="sxs-lookup"><span data-stu-id="92eb5-114">When the transaction is posted, an acquisition transaction is generated and posted in asset 123 for book B and in asset 123 for book C for 1,500.00.</span></span> <span data-ttu-id="92eb5-115">Þegar færslur aðalbókar eru búnar til fyrir bókun í eignabók, er einnig hægt að skoða og breyta færslum fyrir afleidd bækur.</span><span class="sxs-lookup"><span data-stu-id="92eb5-115">When you prepare the transactions of the primary book for posting in the fixed asset journal, you can also view and modify the transactions of the derived books.</span></span> <span data-ttu-id="92eb5-116">Þegar færslur aðalbókar eru búnar til í annarri bók, er ekki hægt að skoða færslur fyrir afleidd virðislíkön.</span><span class="sxs-lookup"><span data-stu-id="92eb5-116">If you prepare the primary book transactions in another journal, the transactions of the derived value are not displayed.</span></span> <span data-ttu-id="92eb5-117">Hins vegar eru þær bókaðar á viðeigandi lykla og bókunarlög þegar færslur aðalbókar eru bókaðar.</span><span class="sxs-lookup"><span data-stu-id="92eb5-117">However, they are posted to the appropriate accounts and posting layers when you post the primary book transactions.</span></span>

> [!NOTE]                                                                                                                               
> <span data-ttu-id="92eb5-118">Bækur sem eru uppsett til að bóka færslur með öðrum millibilum en aðalbókar verða að vera tengd eigninni sem aðskilin bækur en ekki sem afleidd bækur.</span><span class="sxs-lookup"><span data-stu-id="92eb5-118">Books that are set up to post transactions at intervals other than the primary book intervals must be attached to the fixed asset as separate books and not as derived books.</span></span>  

<span data-ttu-id="92eb5-119">Nánari upplýsingar eru í [Bókað í afleiddar bækur](post-derived-value-models.md).</span><span class="sxs-lookup"><span data-stu-id="92eb5-119">For more information, see [Posting with derived books](post-derived-value-models.md).</span></span>




