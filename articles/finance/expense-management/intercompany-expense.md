---
title: Kostnaður innan samstæðu
description: Starfskraftur sem starfar hjá einum lögaðila í fyrirtæki kann að vinna verk fyrir annan lögaðila í sama fyrirtæki. Í þeim aðstæðum er hægt að nota valkost kostnaðar innan samstæðu til að úthluta kostnaði starfsmannsins á lögaðilann sem verkið var unnið fyrir.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 07e425707eb20730f10246a27799f4deeef93f97
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/21/2020
ms.locfileid: "3390885"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="5275f-104">Kostnaður innan samstæðu</span><span class="sxs-lookup"><span data-stu-id="5275f-104">Intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5275f-105">Starfskraftur sem starfar hjá einum lögaðila í fyrirtæki kann að vinna verk fyrir annan lögaðila í sama fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="5275f-105">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="5275f-106">Í þeim aðstæðum er hægt að nota valkost kostnaðar innan samstæðu til að úthluta kostnaði starfsmannsins á lögaðilann sem verkið var unnið fyrir.</span><span class="sxs-lookup"><span data-stu-id="5275f-106">In this situation, you can use the intercompany expense feature to assign the worker’s expenses to the legal entity for which the work was performed.</span></span> <span data-ttu-id="5275f-107">Lögaðilinn sem starfsmaðurinn vinnur hjá er kallaður lögaðili sem lánar.</span><span class="sxs-lookup"><span data-stu-id="5275f-107">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="5275f-108">Lögaðilinn sem starfskrafturinn stofnar til kostnaðarins fyrir kallast lögaðili sem fær lánað.</span><span class="sxs-lookup"><span data-stu-id="5275f-108">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="5275f-109">Áður en starfskraftur getur búið til og lagt fram kostnað vegna vinnu sem er framkvæmd fyrir annan lögaðilann, í lögaðila sem lánar, á **Færibreytur kostnaðarstjórnunar** síðunni skal velja **Leyfa kostnaðarlínur innan samstæðu**.</span><span class="sxs-lookup"><span data-stu-id="5275f-109">Before a worker can create and submit expenses for work that is performed for a different legal entity, in the loaning legal entity, on the **Expense management parameters** page, select the **Allow intercompany expense lines** option.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="5275f-110">Bókun skatts fyrir kostnað innan samstæðu</span><span class="sxs-lookup"><span data-stu-id="5275f-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5275f-111">Ef óskað er eftir að nota skattflokka sem tengjast lánaeiningunni (Uppruni) í stað þess að lána (viðtökustaður) lögaðila í kostnaðarskýrslu þarf að stilla það í VSK-uppsetningu fjárhags.</span><span class="sxs-lookup"><span data-stu-id="5275f-111">If you want to use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you will need to configure this in the General ledger sales tax set up.</span></span> <span data-ttu-id="5275f-112">Þegar fjárhagsfæribreytan **Lögaðili fyrir skattbókun innan samstæðu** er stillt á **Uppruna** og færibreytan **Nota skattareglur virðisaukaskatts** er stillt á **Nei**, verður að nota skattsamsetningu fyrir lögaðilann sem lánar.</span><span class="sxs-lookup"><span data-stu-id="5275f-112">When the General ledger parameter, **Legal entity for intercompany tax posting** is set to **Source** and **Apply sales tax taxation rules** is set to **No**, the tax combination for the loaning legal entity will be used.</span></span> <span data-ttu-id="5275f-113">Þegar sama færibreyta er stillt á **Áfangastað**, verður notuð skattsamsetning fyrir lögaðilann sem fær lánað.</span><span class="sxs-lookup"><span data-stu-id="5275f-113">When the same parameter is set to **Destination**, the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="5275f-114">Fyrir lögaðila í Bandaríkjunum, þegar færibreytan er stillt á **Uppruni**, verður einnig að skilgreina **Innskatt** á síðu nýrra **fjárhagsbókunarflokka**.</span><span class="sxs-lookup"><span data-stu-id="5275f-114">For legal entities in the United States, when the parameter is set to **Source**, the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="5275f-115">Bókhaldsvélin notar upplýsingarnar úr þessum reit fyrir skattatengda bókhaldsfærslu.</span><span class="sxs-lookup"><span data-stu-id="5275f-115">The accounting engine will use the information from this field for tax related accounting entry.</span></span>   
<span data-ttu-id="5275f-116">Hegðunin er í samræmi við kostnaðarlínur sem bókaðar eru með eða án verks.</span><span class="sxs-lookup"><span data-stu-id="5275f-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  
