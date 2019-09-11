---
title: " Skilgreiningar verslunar fyrir smásöluyfirlit"
description: Þetta ferli fer í gegnum skilgreiningar fyrir smásöluverslun sem hafa áhrif á hvernig smásöluuppgjör eru stofnuð og bókuð.
author: jashanno
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dbedcda59f503b103d5448e59038e4ed8ca0b51d
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916531"
---
# <a name="store-configurations-for-retail-statements"></a><span data-ttu-id="617a0-103"> Skilgreiningar verslunar fyrir smásöluyfirlit</span><span class="sxs-lookup"><span data-stu-id="617a0-103">Store configurations for Retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="617a0-104">Þetta ferli fer í gegnum skilgreiningar fyrir smásöluverslun sem hafa áhrif á hvernig smásöluuppgjör eru stofnuð og bókuð.</span><span class="sxs-lookup"><span data-stu-id="617a0-104">This procedure walks through configurations for the Retail store that affect how Retail statements get created and posted.</span></span> <span data-ttu-id="617a0-105">Fjárhagsvíddir í smásöluverslunum eru til umfjöllunar í öðru ferli.</span><span class="sxs-lookup"><span data-stu-id="617a0-105">Financial dimensions on Retail stores are covered in another procedure.</span></span> <span data-ttu-id="617a0-106">Þessi aðferð notar sýnigögn USRT fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="617a0-106">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="617a0-107">Í **Skoðunarrúðunni** ferðu í **Einingar > Smásala og viðskipti > Rásir > Smásöluverslanir > Allar smásöluverslanir**.</span><span class="sxs-lookup"><span data-stu-id="617a0-107">In the **Navgiation pane**, go to **Modules > Retail and commerce > Channels > Retail stores > All retail stores**.</span></span>
2. <span data-ttu-id="617a0-108">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="617a0-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="617a0-109">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="617a0-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="617a0-110">Smellið á **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="617a0-110">Click **Edit**.</span></span>
5. <span data-ttu-id="617a0-111">Stillingar í flýtiflipanum **Uppgjör/lokun** hafa áhrif á stofnun yfirlits, villuleit og bókun fyrir verslunina.</span><span class="sxs-lookup"><span data-stu-id="617a0-111">The settings in the **Statement/closing** fastTab affect the statement creation, validation, and posting for the store.</span></span> <span data-ttu-id="617a0-112">Stækkaðu flýtiflipann **Yfirlýsing/lokun**.</span><span class="sxs-lookup"><span data-stu-id="617a0-112">Expand the **Statement/closing** fastTab.</span></span>  
6. <span data-ttu-id="617a0-113">Í reitnum **Uppgjörsaðferð** skal velja aðferðina sem á að nota til að flokka línur yfirlits eftir.</span><span class="sxs-lookup"><span data-stu-id="617a0-113">In the **Statement method** field, select the method you want to use to to group the statement lines by.</span></span>  
7. <span data-ttu-id="617a0-114">Veljið "Já" í **Eitt uppgjör á dag** eigi aðeins að stofna eitt uppgjör á dag þegar stofnað er yfirlits frá runuvinnslu stofnunar uppgjörs.</span><span class="sxs-lookup"><span data-stu-id="617a0-114">Select "Yes" in **One statement per day** if there should only be one statement created per day when creating statements from the statement creation batch job.</span></span>  
8. <span data-ttu-id="617a0-115">Reiturinn **Útreikningur á talningu skiptimyntar** tilgreinir hvort talning skiptimyntar eigi að leggja saman eða hvort nota eigi það síðasta.</span><span class="sxs-lookup"><span data-stu-id="617a0-115">The **Tender declaration calculation** field defines whether tender declarations should be added together or if the last one should be used.</span></span>  
9. <span data-ttu-id="617a0-116">Í reitnum **Sléttun** skal velja fjárhagslykil til að bóka sléttunarmun í.</span><span class="sxs-lookup"><span data-stu-id="617a0-116">In the **Rounding** field, select the ledger account to post rounding differences into.</span></span>  
10. <span data-ttu-id="617a0-117">Í reitinn **Hámark sléttunarmismunar** er hægt að færa inn hæstan leyfilegan sléttunarmismun.</span><span class="sxs-lookup"><span data-stu-id="617a0-117">In the **Maximum rounding difference** field, enter the maximum rounding difference allowed.</span></span>
11. <span data-ttu-id="617a0-118">Í reitnum **Bókun** færirðu inn hámarkssamtölu bókunarmismunar sem er leyfð fyrir yfirlit.</span><span class="sxs-lookup"><span data-stu-id="617a0-118">In the **Posting** field, enter the maximum total posting difference allowed for a statement.</span></span>
12. <span data-ttu-id="617a0-119">Í reitnum **Vakt** skal færa inn hámarkssamtölu mismunar á vakt innan yfirlits.</span><span class="sxs-lookup"><span data-stu-id="617a0-119">In the **Shift** field, enter the maximum total difference within a shift in a statement.</span></span>  
13. <span data-ttu-id="617a0-120">Í reitnum **Færsla** færirðu inn hámarkssamtölu mismunur í uppgjörslínu.</span><span class="sxs-lookup"><span data-stu-id="617a0-120">In the **Transaction** field, enter the maximum total difference in a statement line.</span></span>  
14. <span data-ttu-id="617a0-121">Í reitnum **Lokunaraðferð** skilgreinirðu hvort færslur sem verða teknar með í uppgjör ætti að vera hluti af lokuð vakt eða hvort þau má hafa með í færslur innan marka skilgreinda dagsetning/tími.</span><span class="sxs-lookup"><span data-stu-id="617a0-121">In the **Closing method** field, define whether transactions that will be included in a statement should be part of a closed shift or if they can be any transactions within the defined date/time range.</span></span>  
15. <span data-ttu-id="617a0-122">Í reitnum **Lok viðskiptadags** færirðu inn tíma ef bóka eigi færslur eftir miðnætti með deginum á undan.</span><span class="sxs-lookup"><span data-stu-id="617a0-122">In the **End of business day** field, enter a time if transactions that happen after midnight should be posted with the previous day.</span></span>  
16. <span data-ttu-id="617a0-123">Veljið "Já" í **Bóka sem viðskiptadag** ef bóka skal færslur eftir miðnætti sem hluta af deginum á undan.</span><span class="sxs-lookup"><span data-stu-id="617a0-123">Select "Yes" in **Post as business day** if transactions that happen after midnight should be posted as part of the previous day.</span></span>  
17. <span data-ttu-id="617a0-124">Veljið "Já" í **Skipta eftir uppgjörsaðferð** til að fá yfirlit sem stofnuð voru fyrir hverja uppgjörsaðferð sem var skilgreind.</span><span class="sxs-lookup"><span data-stu-id="617a0-124">Select "Yes" in **Split by Statement method** to get statements created for each statement method defined.</span></span> <span data-ttu-id="617a0-125">Þetta getur verið gagnlegt ef afköst við bókun þarf að vera endurbætt fyrir verslana með margar færslur, þar sem það stofnar mörg minni yfirlit sem má vinna samhliða.</span><span class="sxs-lookup"><span data-stu-id="617a0-125">This can be useful if the performance of the posting needs to be improved for stores with high transaction volumes since it will create many smaller statements that can be processed in parallel.</span></span>  
18. <span data-ttu-id="617a0-126">Á flýtiflipanum **Almennt** í reitnum **Sjálfgefinn viðskiptavinur** er hægt að velja viðskiptavinalykillinn sem á að nota fyrir sölu til viðskiptavina sem koma af götunni.</span><span class="sxs-lookup"><span data-stu-id="617a0-126">In the **General** fastTab, in the **Default customer** field, you can select the customer account to use for sales to walk-in customers.</span></span>  

