---
title: "Skrá framleiðslupöntun sem tilbúna"
description: "Bóka sem tilbúið er framleiðslustig. Á þessu stigi er endanleg vara skráð og flutt úr framleiðslupöntuninni í birgðir."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdJournalTransJob, ProdJournalTransProd, ProdJournalTransRoute, ProdParmReportFinished, ProdRouteOprOverview
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 27061
ms.assetid: 1c2dfc54-a293-49f2-9b96-5a912ac5762c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: fa40733e3f1310869ead8b0ac774bb621637e250
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---

# <a name="report-production-orders-as-finished"></a><span data-ttu-id="5d894-104">Skrá framleiðslupöntun sem tilbúna</span><span class="sxs-lookup"><span data-stu-id="5d894-104">Report production orders as finished</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="5d894-105">Bóka sem tilbúið er framleiðslustig.</span><span class="sxs-lookup"><span data-stu-id="5d894-105">Report as finished is a production stage.</span></span> <span data-ttu-id="5d894-106">Á þessu stigi er endanleg vara skráð og flutt úr framleiðslupöntuninni í birgðir.</span><span class="sxs-lookup"><span data-stu-id="5d894-106">At this stage, a finished product is reported and moved from the production order to the inventory.</span></span>

<span data-ttu-id="5d894-107">Þegar magn af tilbúnum vörum er tilkynnt sem lokið á framleiðslupöntun er það uppfært í birgðunum sem á lager.</span><span class="sxs-lookup"><span data-stu-id="5d894-107">When a quantity of the finished goods is reported as finished on a production order it is updated as on-hand in the inventory.</span></span> <span data-ttu-id="5d894-108">Hlutar af upphaflega áætluðu pöntunarmagni geta verið tilkynntir sem lokið.</span><span class="sxs-lookup"><span data-stu-id="5d894-108">Partial quantities of the originally planned order quantity can be reported as finished.</span></span> <span data-ttu-id="5d894-109">Einnig er mögulegt að tilkynna villumagn með tengdri villuástæðu þegar magn er tilkynnt sem lokið.</span><span class="sxs-lookup"><span data-stu-id="5d894-109">It is also possible to report error quantities with an associated error reason when reporting quantities as finished.</span></span> <span data-ttu-id="5d894-110">Þegar framleiðslupöntun nær stiginu Tilkynnt sem lokið gefur það til kynna að ekki á eftir að tilkynna meira magn á framleiðslupöntunina.</span><span class="sxs-lookup"><span data-stu-id="5d894-110">When the production order reach the stage Reported as finished it indicates that no more quantity is going to be reported at the production  order.</span></span>
<span data-ttu-id="5d894-111">Eftirfarandi einkenni eru einnig tengd við ferlið **Tilkynnt sem lokið**:</span><span class="sxs-lookup"><span data-stu-id="5d894-111">The following characteristics are also associated with the **Report as finished** process:</span></span>
-   <span data-ttu-id="5d894-112">Hægt er að setja upp notkun á hráefni og tíma sem eru í hlutfalli við tilkynnt magn (bakalosun)</span><span class="sxs-lookup"><span data-stu-id="5d894-112">It is possible to set up consumption of raw material and time that are proportional to the reported quantity (back-flushing)</span></span>
-   <span data-ttu-id="5d894-113">Frágangsvinna getur verið búin til fyrir hluti sem eru virkir fyrir ferli vöruhúsa.</span><span class="sxs-lookup"><span data-stu-id="5d894-113">Put-away work can be generated for items that are enabled for warehouse processes.</span></span>
-   <span data-ttu-id="5d894-114">Hægt er að setja upp áætlað eða staðlað kostnaðarvirði fullkláraðra vara sem tilkynna á á fjárhagslykla.</span><span class="sxs-lookup"><span data-stu-id="5d894-114">The planned or standard cost value of the finished goods can be set up to be reported to ledger accounts.</span></span>
-   <span data-ttu-id="5d894-115">Hægt er að stofna gæðapöntun fyrir skráða magnið byggt á uppsetningu gæðatengingar.</span><span class="sxs-lookup"><span data-stu-id="5d894-115">A quality order can be created for the reported quantity based on the setup of a quality association.</span></span>

<span data-ttu-id="5d894-116">Magnið er skráð á°frálagsstaðsetningu.</span><span class="sxs-lookup"><span data-stu-id="5d894-116">The quantity is reported to the output location.</span></span> <span data-ttu-id="5d894-117">Vöruhúsavinna er°þá°mynduð til að flytja magn úr staðsetningu°framleiðslufrálags á lokaáfangastaður skilgreint af staðsetningarleiðbeiningar fyrir°frágangsvinnu.</span><span class="sxs-lookup"><span data-stu-id="5d894-117">Warehouse work is then generated to move the quantity from the output location to its final destination defined by the location directive for the put-away work.</span></span>

-   <span data-ttu-id="5d894-118">Hægt er að stofna gæðapöntun er þegar framleiðslupöntun er tilkynnt sem tilbúin ef gæðatenging hefur verið sett upp.</span><span class="sxs-lookup"><span data-stu-id="5d894-118">A quality order can be created when a production order is reported as finished if a quality association has been set up.</span></span>

## <a name="set-a-production-order-to-reporting-as-finished"></a><span data-ttu-id="5d894-119">Stilla framleiðslupöntun sem°Tilkynnt sem lokið</span><span class="sxs-lookup"><span data-stu-id="5d894-119">Set a production order to Reporting as finished</span></span>
<span data-ttu-id="5d894-120">Hægt er að færa framleiðslupöntun í stöðuna **Tilkynnt sem lokið**með hefðbundinni uppfærsluaðgerð framleiðslupöntunar eða með leiðar- og vinnslupjaldsbókum eða í gegnum°færslubókina **Tilkynnt sem lokið**.</span><span class="sxs-lookup"><span data-stu-id="5d894-120">You can set a production order to **Report as finished** through the standard production order update function, or through the route and job card journals, or through the journal **Report as finished**.</span></span> <span data-ttu-id="5d894-121">Einnig er hægt að uppfæra stigið í°**Tilkynnt sem lokið** gegnum síðurnar afgreiðslustöð verkspjalda og verkspjaldssíðu í tæki°í síðustu vinnslu framleiðslupöntunar.</span><span class="sxs-lookup"><span data-stu-id="5d894-121">You can also update the stage to **Report as finished** through the job card terminal and job card device pages, when you report on the last job of the production order.</span></span> <span data-ttu-id="5d894-122">Loks er hægt að virkja valkostinn **Tilkynnt sem lokið** sem ferli fyrir vöruhúsalófatölvur.</span><span class="sxs-lookup"><span data-stu-id="5d894-122">Finally, you can enable the **Report as finished** option as a process for the handheld warehouse device solution.</span></span>  




