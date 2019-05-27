---
title: Breyta afskriftarvenjum fyrir margar eignir
description: Þetta verkefni uppfærir afskriftarreglu fyrir tilgreindan eignaflokk.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysQueryForm, SrsReportViewerForm
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a7a79b2edf64f0063253d3f2a23b0020eceb87c0
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1561500"
---
# <a name="change-depreciation-conventions-for-multiple-fixed-assets"></a><span data-ttu-id="003e1-103">Breyta afskriftarvenjum fyrir margar eignir</span><span class="sxs-lookup"><span data-stu-id="003e1-103">Change depreciation conventions for multiple fixed assets</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="003e1-104">Þetta verkefni uppfærir afskriftarreglu fyrir tilgreindan eignaflokk.</span><span class="sxs-lookup"><span data-stu-id="003e1-104">This task updates the depreciation convention for a specified fixed asset group.</span></span> <span data-ttu-id="003e1-105">Þessi leiðarvísi fyrir verk notar sýnigögn USMF fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="003e1-105">This task guide uses the USMF demo company.</span></span>

1. <span data-ttu-id="003e1-106">Fara í Eignir > Reglubundin verkefni > Fjöldauppfærsla</span><span class="sxs-lookup"><span data-stu-id="003e1-106">Go to Fixed assets > Periodic tasks > Mass update</span></span>
2. <span data-ttu-id="003e1-107">Í reitnum Afskriftabók skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="003e1-107">In the Depreciation book field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="003e1-108">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="003e1-108">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="003e1-109">Í reitinn sett í upphaf þjónustu skal færa inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="003e1-109">In the Placed in service start field, enter a date.</span></span>
5. <span data-ttu-id="003e1-110">Í reitinn Sett í lok þjónustu skal færa inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="003e1-110">In the Placed in service end field, enter a date.</span></span>
    * <span data-ttu-id="003e1-111">Aðeins Eignir sem tilheyra valdri afskriftarbók og sem hafa verið teknar í notkun á tilgreindu tímabili verða uppfærðar.</span><span class="sxs-lookup"><span data-stu-id="003e1-111">Only assets that are a part of the select depreciation book and that have been placed in service between these dates will be updated.</span></span>  
6. <span data-ttu-id="003e1-112">Veljið valkost í núverandi afskriftarregla svæðið.</span><span class="sxs-lookup"><span data-stu-id="003e1-112">In the Current depreciation convention field, select an option.</span></span>
    * <span data-ttu-id="003e1-113">Aðeins eignir sem hafa gildandi afskriftarreglu verða uppfærðar.</span><span class="sxs-lookup"><span data-stu-id="003e1-113">Only assets that have the current depreciation convention will be updated.</span></span>  
7. <span data-ttu-id="003e1-114">Veljið valkost í Nýja afskriftarregla svæðið.</span><span class="sxs-lookup"><span data-stu-id="003e1-114">In the New depreciation convention field, select an option.</span></span>
    * <span data-ttu-id="003e1-115">Staðfestið að prenta skýrsluna á áfangastaðinn.</span><span class="sxs-lookup"><span data-stu-id="003e1-115">Verify the report will print to the desired destination.</span></span>  
8. <span data-ttu-id="003e1-116">Útvíkka Færslur til að taka hluta.</span><span class="sxs-lookup"><span data-stu-id="003e1-116">Expand the Records to include section.</span></span>
9. <span data-ttu-id="003e1-117">Smellt er á Síu.</span><span class="sxs-lookup"><span data-stu-id="003e1-117">Click Filter.</span></span>
10. <span data-ttu-id="003e1-118">Á listanum, veljið eignaflokkur.</span><span class="sxs-lookup"><span data-stu-id="003e1-118">In the list, select the Fixed asset group.</span></span>
11. <span data-ttu-id="003e1-119">Í reitnum skilyrði skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="003e1-119">In the Criteria field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="003e1-120">Veljið æskilega eignaflokk.</span><span class="sxs-lookup"><span data-stu-id="003e1-120">Select the desired Fixed asset group.</span></span>
13. <span data-ttu-id="003e1-121">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="003e1-121">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="003e1-122">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="003e1-122">Click OK.</span></span>
15. <span data-ttu-id="003e1-123">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="003e1-123">Click OK.</span></span>
    *  <span data-ttu-id="003e1-124">Niðurstöðu ferlisins eru sýndar í skýrslunni Margar uppfærslu.</span><span class="sxs-lookup"><span data-stu-id="003e1-124">Results of the process are shown on the Mass update report.</span></span>     

