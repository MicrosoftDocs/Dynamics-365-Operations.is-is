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
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 21baf3692cbcb87f6ed37459848376a1fa87a438
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178260"
---
# <a name="change-depreciation-conventions-for-multiple-fixed-assets"></a><span data-ttu-id="ee5db-103">Breyta afskriftarvenjum fyrir margar eignir</span><span class="sxs-lookup"><span data-stu-id="ee5db-103">Change depreciation conventions for multiple fixed assets</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ee5db-104">Þetta verkefni uppfærir afskriftarreglu fyrir tilgreindan eignaflokk.</span><span class="sxs-lookup"><span data-stu-id="ee5db-104">This task updates the depreciation convention for a specified fixed asset group.</span></span> <span data-ttu-id="ee5db-105">Þessi leiðarvísi fyrir verk notar sýnigögn USMF fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="ee5db-105">This task guide uses the USMF demo company.</span></span>

1. <span data-ttu-id="ee5db-106">Fara í Eignir > Reglubundin verkefni > Fjöldauppfærsla</span><span class="sxs-lookup"><span data-stu-id="ee5db-106">Go to Fixed assets > Periodic tasks > Mass update</span></span>
2. <span data-ttu-id="ee5db-107">Í reitnum Afskriftabók skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="ee5db-107">In the Depreciation book field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="ee5db-108">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="ee5db-108">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="ee5db-109">Í reitinn Sett í upphaf þjónustu skal færa inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="ee5db-109">In the Placed in service start field, enter a date.</span></span>
5. <span data-ttu-id="ee5db-110">Í reitinn Sett í lok þjónustu skal færa inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="ee5db-110">In the Placed in service end field, enter a date.</span></span>
    * <span data-ttu-id="ee5db-111">Aðeins Eignir sem tilheyra valdri afskriftarbók og sem hafa verið teknar í notkun á tilgreindu tímabili verða uppfærðar.</span><span class="sxs-lookup"><span data-stu-id="ee5db-111">Only assets that are a part of the select depreciation book and that have been placed in service between these dates will be updated.</span></span>  
6. <span data-ttu-id="ee5db-112">Veljið valkost í núverandi afskriftarregla svæðið.</span><span class="sxs-lookup"><span data-stu-id="ee5db-112">In the Current depreciation convention field, select an option.</span></span>
    * <span data-ttu-id="ee5db-113">Aðeins eignir sem hafa gildandi afskriftarreglu verða uppfærðar.</span><span class="sxs-lookup"><span data-stu-id="ee5db-113">Only assets that have the current depreciation convention will be updated.</span></span>  
7. <span data-ttu-id="ee5db-114">Veljið valkost í Nýja afskriftarregla svæðið.</span><span class="sxs-lookup"><span data-stu-id="ee5db-114">In the New depreciation convention field, select an option.</span></span>
    * <span data-ttu-id="ee5db-115">Staðfestið að prenta skýrsluna á áfangastaðinn.</span><span class="sxs-lookup"><span data-stu-id="ee5db-115">Verify the report will print to the desired destination.</span></span>  
8. <span data-ttu-id="ee5db-116">Útvíkka Færslur til að taka hluta.</span><span class="sxs-lookup"><span data-stu-id="ee5db-116">Expand the Records to include section.</span></span>
9. <span data-ttu-id="ee5db-117">Smellt er á Síu.</span><span class="sxs-lookup"><span data-stu-id="ee5db-117">Click Filter.</span></span>
10. <span data-ttu-id="ee5db-118">Á listanum, veljið eignaflokkur.</span><span class="sxs-lookup"><span data-stu-id="ee5db-118">In the list, select the Fixed asset group.</span></span>
11. <span data-ttu-id="ee5db-119">Í reitnum skilyrði skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="ee5db-119">In the Criteria field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="ee5db-120">Veljið æskilega eignaflokk.</span><span class="sxs-lookup"><span data-stu-id="ee5db-120">Select the desired Fixed asset group.</span></span>
13. <span data-ttu-id="ee5db-121">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="ee5db-121">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="ee5db-122">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="ee5db-122">Click OK.</span></span>
15. <span data-ttu-id="ee5db-123">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="ee5db-123">Click OK.</span></span>
    *  <span data-ttu-id="ee5db-124">Niðurstöðu ferlisins eru sýndar í skýrslunni Margar uppfærslu.</span><span class="sxs-lookup"><span data-stu-id="ee5db-124">Results of the process are shown on the Mass update report.</span></span>     

