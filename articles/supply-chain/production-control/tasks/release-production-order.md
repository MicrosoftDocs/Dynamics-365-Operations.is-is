--- 
title: "Gefa út framleiðslupöntun"
description: "Þetta ferli sýnir hvernig á að losa framleiðslupöntun."
author: johanhoffmann
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdTableListPage, ProdParmRelease, SrsReportViewerForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 917fe1ef826c9b112be29ebce78ebd750652db64
ms.contentlocale: is-is
ms.lasthandoff: 09/14/2018

---
# <a name="release-a-production-order"></a><span data-ttu-id="3a678-103">Gefa út framleiðslupöntun</span><span class="sxs-lookup"><span data-stu-id="3a678-103">Release a production order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3a678-104">Þetta ferli sýnir hvernig á að losa framleiðslupöntun.</span><span class="sxs-lookup"><span data-stu-id="3a678-104">This procedure shows how to release a production order.</span></span> <span data-ttu-id="3a678-105">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="3a678-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="3a678-106">Þetta er fjórða ferli af sjö sem útskýrir lífsferil framleiðslupöntunar.</span><span class="sxs-lookup"><span data-stu-id="3a678-106">This is the fourth procedure out of seven which explains the production order lifecycle.</span></span>

1. <span data-ttu-id="3a678-107">Fara í Framleiðslustýringar > Framleiðslupantanir > Allar framleiðslupantanir.</span><span class="sxs-lookup"><span data-stu-id="3a678-107">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="3a678-108">Í hnitanetinu er valin framleiðslupöntun sem hefur stöðuna Áætlað.</span><span class="sxs-lookup"><span data-stu-id="3a678-108">In the grid, select a production order that has the Scheduled status.</span></span>  
2. <span data-ttu-id="3a678-109">Smellið á „Framleiðslupöntun“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="3a678-109">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="3a678-110">Smellið á „Gefa út“.</span><span class="sxs-lookup"><span data-stu-id="3a678-110">Click Release.</span></span>
    * <span data-ttu-id="3a678-111">Á þessari síðu er hægt að staðfesta losun valið svið framleiðslupantanir.</span><span class="sxs-lookup"><span data-stu-id="3a678-111">On this page, you can confirm the release of the selected range of production orders.</span></span> <span data-ttu-id="3a678-112">Smelltu á Velja ef óskað er að bæta við pantanir.</span><span class="sxs-lookup"><span data-stu-id="3a678-112">Click Select if you want to add orders.</span></span>  
    * <span data-ttu-id="3a678-113">Losunarskref gefur til kynna þegar framleiðslupöntun er losuð í vinnusal framleiðslu þannig að virkjar vinnusals geta skráð vinnslu á framleiðsluverk.</span><span class="sxs-lookup"><span data-stu-id="3a678-113">The Release step indicates when the production order is released to the production shop floor so that the shop floor operators can report progress on the production jobs.</span></span> <span data-ttu-id="3a678-114">Framleiðsluskjöl sem inniheldur viðeigandi upplýsingar um vinnslu verka er hægt að gefa út.</span><span class="sxs-lookup"><span data-stu-id="3a678-114">Production papers that contain relevant information about processing the jobs can be issued.</span></span> <span data-ttu-id="3a678-115">Vinna í vöruhúss fyrir tiltekt hráefnis er myndaður fyrir vörur sem eru settir upp fyrir ferli vöruhúsa.</span><span class="sxs-lookup"><span data-stu-id="3a678-115">The warehouse work for raw material picking is generated for the items that are set up for the warehouse process.</span></span>  
4. <span data-ttu-id="3a678-116">Smellið á flipann „Almennt“.</span><span class="sxs-lookup"><span data-stu-id="3a678-116">Click the General tab.</span></span>
    * <span data-ttu-id="3a678-117">Velja hvaða framleiðsluskýrslur á að prenta .</span><span class="sxs-lookup"><span data-stu-id="3a678-117">Select which production reports should be printed.</span></span> <span data-ttu-id="3a678-118">Vinnsluspjaldsskýrslan prentar síðu fyrir hvert vinnsluröðunar og krefst þess að framleiðslupöntun sé raða á stigi vinnslu.</span><span class="sxs-lookup"><span data-stu-id="3a678-118">The Job card report prints a page for each scheduled job and requires the production order to be scheduled at the job level.</span></span> <span data-ttu-id="3a678-119">Skýrslan inniheldur upplýsingar um áætluðu upphafs- og lokatími, magn sem á að framleiða, og hvaða tilfanga vinnur vinnslunnar.</span><span class="sxs-lookup"><span data-stu-id="3a678-119">The report contains information about the scheduled start and end time, the quantity to produce, and which resource processes the job.</span></span> <span data-ttu-id="3a678-120">Leiðarvinnsluskýrslan safnar sömu upplýsingar á sömu síðu en prentar ekki síðu fyrir hvert verk.</span><span class="sxs-lookup"><span data-stu-id="3a678-120">The Route job report collects the same information on the same page, but does not print a page for each job.</span></span> <span data-ttu-id="3a678-121">Leiðarvinnsluskýrslan sýnir aðeins aðgerðir en ekki verk.</span><span class="sxs-lookup"><span data-stu-id="3a678-121">The Route card report only shows the operations but not the jobs.</span></span> <span data-ttu-id="3a678-122">Þess vegna þessa skýrslu þarfnast ekki vinnsluröðun, en hægt er að nota hana þegar framleiðslupöntunum er raðað á stigi aðgerð.</span><span class="sxs-lookup"><span data-stu-id="3a678-122">Therefore, this report does not require job scheduling, but can be used when production orders are scheduled at the operation level.</span></span>  
5. <span data-ttu-id="3a678-123">Smellt er á gátreitinn Prenta leiðarspjald.</span><span class="sxs-lookup"><span data-stu-id="3a678-123">Click the Print route card checkbox.</span></span>
6. <span data-ttu-id="3a678-124">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="3a678-124">Click OK.</span></span>
7. <span data-ttu-id="3a678-125">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="3a678-125">Close the page.</span></span>


