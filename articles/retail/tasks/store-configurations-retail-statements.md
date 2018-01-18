--- 
title: " Skilgreiningar verslunar fyrir smásöluyfirlit"
description: "Þetta ferli fer í gegnum skilgreiningar fyrir smásöluverslun sem hafa áhrif á hvernig smásöluuppgjör eru stofnuð og bókuð."
author: jashanno
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9b080ff46a0fbc73ed4f8fa3f03d71e9d758cc2
ms.openlocfilehash: 96aff33904c1de4a8b2642890eba7bf854d8e0c1
ms.contentlocale: is-is
ms.lasthandoff: 01/17/2018

---
# <a name="store-configurations-for-retail-statements"></a><span data-ttu-id="43248-103"> Skilgreiningar verslunar fyrir smásöluyfirlit</span><span class="sxs-lookup"><span data-stu-id="43248-103">Store configurations for Retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="43248-104">Þetta ferli fer í gegnum skilgreiningar fyrir smásöluverslun sem hafa áhrif á hvernig smásöluuppgjör eru stofnuð og bókuð.</span><span class="sxs-lookup"><span data-stu-id="43248-104">This procedure walks through configurations for the Retail store that affect how Retail statements get created and posted.</span></span> <span data-ttu-id="43248-105">Fjárhagsvíddir í smásöluverslunum eru til umfjöllunar í öðru ferli.</span><span class="sxs-lookup"><span data-stu-id="43248-105">Financial dimensions on Retail stores are covered in another procedure.</span></span> <span data-ttu-id="43248-106">Þessi aðferð notar sýnigögn USRT fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="43248-106">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="43248-107">Fara í Smásölu og viðskipti > rásir > smásöluverslanir > allar smásöluverslanir.</span><span class="sxs-lookup"><span data-stu-id="43248-107">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
2. <span data-ttu-id="43248-108">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="43248-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="43248-109">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="43248-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="43248-110">Stillingar í hlutanum Uppgjör/lokun hafa áhrif á stofnun yfirlits, villuleit og bókun fyrir verslunina.</span><span class="sxs-lookup"><span data-stu-id="43248-110">The settings in the Statement/closing section affect the statement creation, validation, and posting for the store.</span></span>  <span data-ttu-id="43248-111">Opna hlutann Uppgjör/lokun.</span><span class="sxs-lookup"><span data-stu-id="43248-111">Open the Statement/closing section.</span></span>  
    * <span data-ttu-id="43248-112">Veljið aðferðina sem á að nota til að flokka línur yfirlits eftir.</span><span class="sxs-lookup"><span data-stu-id="43248-112">Select the method you want to use to group the statement lines by.</span></span>  
    * <span data-ttu-id="43248-113">Veljið "Já" eigi aðeins að stofnað eitt uppgjör á dag þegar stofnað er yfirlits frá runuvinnslu stofnunar uppgjörs.</span><span class="sxs-lookup"><span data-stu-id="43248-113">Select "Yes" if there should only be one statement created per day when creating statements from the statement creation batch job.</span></span>  
    * <span data-ttu-id="43248-114">útreikningssvæði fyrir talning skiptimyntar tilgreinir hvort talning skiptimyntar eigi að leggja saman eða hvort nota eigi það síðasta .</span><span class="sxs-lookup"><span data-stu-id="43248-114">The Tender declaration calculation field defines whether tender declarations should be added together or if the last one should be used.</span></span>  
    * <span data-ttu-id="43248-115">Veljið fjárhagslykil til að bóka sléttunarmun í.</span><span class="sxs-lookup"><span data-stu-id="43248-115">Select the ledger account to post rounding differences into.</span></span>  
    * <span data-ttu-id="43248-116">Í svæðið Hámark sléttunarmismunar er hægt að færa inn hæstan leyfilegan sléttunarmismun.</span><span class="sxs-lookup"><span data-stu-id="43248-116">In the Maximum rounding difference field, you can enter the maximum rounding difference allowed.</span></span>  
    * <span data-ttu-id="43248-117">Í bókunarsvæðinu, er hægt að færa inn hámarkssamtala hámarksbókunarmismun leyfð fyrir yfirlit.</span><span class="sxs-lookup"><span data-stu-id="43248-117">In the Posting field, you can enter the maximum total posting difference allowed for a statement.</span></span>  
    * <span data-ttu-id="43248-118">Í svæðið Vakt er hægt að færa inn hámarks heildarmismunur á vakt innan yfirlits.</span><span class="sxs-lookup"><span data-stu-id="43248-118">In the Shift field, you can enter the maximum total difference within a shift in a statement.</span></span>  
    * <span data-ttu-id="43248-119">Í svæðið færsla, er hægt að færa inn hámarks heildarmismunur í uppgjörslínu.</span><span class="sxs-lookup"><span data-stu-id="43248-119">In the Transaction field, you can enter the maximum total difference in a statement line.</span></span>  
    * <span data-ttu-id="43248-120">Í svæðið aðferð Lokunar er hægt að skilgreina hvort færslur sem verða teknar með í uppgjör ætti að vera hluti af lokuð vakt eða hvort þau má hafa með í færslur innan marka skilgreinda dagsetning/tími.</span><span class="sxs-lookup"><span data-stu-id="43248-120">In the Closing method field, you can define whether transactions that will be included in a statement should be part of a closed shift or if they can be any transactions within the defined date/time range.</span></span>  
    * <span data-ttu-id="43248-121">Í reitnum Lok viðskiptadags , er hægt að færa inn tíma ef bóka eigi færslur eftir miðnætti með fyrri dag.</span><span class="sxs-lookup"><span data-stu-id="43248-121">In the End of business day field, you can enter a time if transactions that happen after midnight should be posted with the previous day.</span></span>  
    * <span data-ttu-id="43248-122">Veljið "Já" ef bóka eigi færslur eftir miðnætti sem hluti af fyrri dag.</span><span class="sxs-lookup"><span data-stu-id="43248-122">Select "Yes" if transactions that happen after midnight should be posted as part of the previous day.</span></span>  
    * <span data-ttu-id="43248-123">Veljið "Já" til að fá yfirlit sem stofnuð voru fyrir hverja uppgjörsaðferð sem var skilgreind.</span><span class="sxs-lookup"><span data-stu-id="43248-123">Select "Yes" to get statements created for each statement method defined.</span></span> <span data-ttu-id="43248-124">Þetta getur verið gagnlegt ef afköst við bókun þarf að vera endurbætt fyrir verslana með margar færslur, þar sem það stofnar mörg minni yfirlit sem má vinna samhliða.</span><span class="sxs-lookup"><span data-stu-id="43248-124">This can be useful if the performance of the posting needs to be improved for stores with high transaction volumes since it will create many smaller statements that can be processed in parallel.</span></span>  
    * <span data-ttu-id="43248-125">Í svæðinu Sjálfgefinn viðskiptavin hægt er að velja viðskiptavinalykillinn sem á að nota fyrir sölu til viðskiptavina sem koma af götunni.</span><span class="sxs-lookup"><span data-stu-id="43248-125">In the Default customer field, you can select the customer account to use for sales to walk-in customers.</span></span>  


