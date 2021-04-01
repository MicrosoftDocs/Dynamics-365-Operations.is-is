---
title: Skilgreiningar verslunar fyrir smásöluyfirlit
description: Þetta ferli fer í gegnum skilgreiningar fyrir verslun sem hafa áhrif á hvernig uppgjör í Commerce eru stofnuð og bókuð.
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
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e1670a1a102f9288cdbd0e4cc981e3aa927d1ad9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232666"
---
# <a name="store-configurations-for-retail-statements"></a><span data-ttu-id="feafe-103">Skilgreiningar verslunar fyrir smásöluyfirlit</span><span class="sxs-lookup"><span data-stu-id="feafe-103">Store configurations for Retail statements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="feafe-104">Þetta ferli fer í gegnum skilgreiningar fyrir verslun sem hafa áhrif á hvernig uppgjör í Commerce eru stofnuð og bókuð.</span><span class="sxs-lookup"><span data-stu-id="feafe-104">This procedure walks through configurations for the store that affect how Commerce statements get created and posted.</span></span> <span data-ttu-id="feafe-105">Fjárhagsvíddir í verslunum eru til umfjöllunar í öðru ferli.</span><span class="sxs-lookup"><span data-stu-id="feafe-105">Financial dimensions on stores are covered in another procedure.</span></span> <span data-ttu-id="feafe-106">Þessi aðferð notar sýnigögn USRT fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="feafe-106">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="feafe-107">Í **Skoðunarrúðunni** ferðu í **Einingar > Retail og Commerce > Rásir > Verslanir > Allar smásöluverslanir**.</span><span class="sxs-lookup"><span data-stu-id="feafe-107">In the **Navigation pane**, go to **Modules > Retail and Commerce > Channels > Stores > All stores**.</span></span>
2. <span data-ttu-id="feafe-108">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="feafe-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="feafe-109">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="feafe-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="feafe-110">Smellið á **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="feafe-110">Click **Edit**.</span></span>
5. <span data-ttu-id="feafe-111">Stillingar í flýtiflipanum **Uppgjör/lokun** hafa áhrif á stofnun yfirlits, villuleit og bókun fyrir verslunina.</span><span class="sxs-lookup"><span data-stu-id="feafe-111">The settings in the **Statement/closing** FastTab affect the statement creation, validation, and posting for the store.</span></span> <span data-ttu-id="feafe-112">Víkkið flýtiflipann **Uppgjör/lokun**.</span><span class="sxs-lookup"><span data-stu-id="feafe-112">Expand the **Statement/closing** FastTab.</span></span>  
6. <span data-ttu-id="feafe-113">Í reitnum **Uppgjörsaðferð** skal velja aðferðina sem á að nota til að flokka línur yfirlits eftir.</span><span class="sxs-lookup"><span data-stu-id="feafe-113">In the **Statement method** field, select the method you want to use to group the statement lines by.</span></span>  
7. <span data-ttu-id="feafe-114">Veljið "Já" í **Eitt uppgjör á dag** eigi aðeins að stofna eitt uppgjör á dag þegar stofnað er yfirlits frá runuvinnslu stofnunar uppgjörs.</span><span class="sxs-lookup"><span data-stu-id="feafe-114">Select "Yes" in **One statement per day** if there should only be one statement created per day when creating statements from the statement creation batch job.</span></span>  
8. <span data-ttu-id="feafe-115">Reiturinn **Útreikningur á talningu skiptimyntar** tilgreinir hvort talning skiptimyntar eigi að leggja saman eða hvort nota eigi það síðasta.</span><span class="sxs-lookup"><span data-stu-id="feafe-115">The **Tender declaration calculation** field defines whether tender declarations should be added together or if the last one should be used.</span></span>  
9. <span data-ttu-id="feafe-116">Í reitnum **Sléttun** skal velja fjárhagslykil til að bóka sléttunarmun í.</span><span class="sxs-lookup"><span data-stu-id="feafe-116">In the **Rounding** field, select the ledger account to post rounding differences into.</span></span>  
10. <span data-ttu-id="feafe-117">Í reitinn **Hámark sléttunarmismunar** er hægt að færa inn hæstan leyfilegan sléttunarmismun.</span><span class="sxs-lookup"><span data-stu-id="feafe-117">In the **Maximum rounding difference** field, enter the maximum rounding difference allowed.</span></span>
11. <span data-ttu-id="feafe-118">Í reitnum **Bókun** færirðu inn hámarkssamtölu bókunarmismunar sem er leyfð fyrir yfirlit.</span><span class="sxs-lookup"><span data-stu-id="feafe-118">In the **Posting** field, enter the maximum total posting difference allowed for a statement.</span></span>
12. <span data-ttu-id="feafe-119">Í reitnum **Vakt** skal færa inn hámarkssamtölu mismunar á vakt innan yfirlits.</span><span class="sxs-lookup"><span data-stu-id="feafe-119">In the **Shift** field, enter the maximum total difference within a shift in a statement.</span></span>  
13. <span data-ttu-id="feafe-120">Í reitnum **Færsla** færirðu inn hámarkssamtölu mismunur í uppgjörslínu.</span><span class="sxs-lookup"><span data-stu-id="feafe-120">In the **Transaction** field, enter the maximum total difference in a statement line.</span></span>  
14. <span data-ttu-id="feafe-121">Í reitnum **Lokunaraðferð** skilgreinirðu hvort færslur sem verða teknar með í uppgjör ætti að vera hluti af lokuð vakt eða hvort þau má hafa með í færslur innan marka skilgreinda dagsetning/tími.</span><span class="sxs-lookup"><span data-stu-id="feafe-121">In the **Closing method** field, define whether transactions that will be included in a statement should be part of a closed shift or if they can be any transactions within the defined date/time range.</span></span>  
15. <span data-ttu-id="feafe-122">Í reitnum **Lok viðskiptadags** færirðu inn tíma ef bóka eigi færslur eftir miðnætti með deginum á undan.</span><span class="sxs-lookup"><span data-stu-id="feafe-122">In the **End of business day** field, enter a time if transactions that happen after midnight should be posted with the previous day.</span></span>  
16. <span data-ttu-id="feafe-123">Veljið "Já" í **Bóka sem viðskiptadag** ef bóka skal færslur eftir miðnætti sem hluta af deginum á undan.</span><span class="sxs-lookup"><span data-stu-id="feafe-123">Select "Yes" in **Post as business day** if transactions that happen after midnight should be posted as part of the previous day.</span></span>  
17. <span data-ttu-id="feafe-124">Veljið "Já" í **Skipta eftir uppgjörsaðferð** til að fá yfirlit sem stofnuð voru fyrir hverja uppgjörsaðferð sem var skilgreind.</span><span class="sxs-lookup"><span data-stu-id="feafe-124">Select "Yes" in **Split by Statement method** to get statements created for each statement method defined.</span></span> <span data-ttu-id="feafe-125">Þessi aðgerð getur verið gagnleg ef afköst við bókun þarf að vera endurbætt fyrir verslana með margar færslur, þar sem það stofnar mörg minni yfirlit sem má vinna samhliða.</span><span class="sxs-lookup"><span data-stu-id="feafe-125">This action can be useful if the performance of the posting needs to be improved for stores with high transaction volumes since it will create many smaller statements that can be processed in parallel.</span></span>  
18. <span data-ttu-id="feafe-126">Í flýtiflipanum **Almennt** í svæðinu **Sjálfgefinn viðskiptavinur** hægt er að velja viðskiptavinalykillinn sem á að nota fyrir sölu til viðskiptavina sem koma af götunni.</span><span class="sxs-lookup"><span data-stu-id="feafe-126">In the **General** FastTab, in the **Default customer** field, you can select the customer account to use for sales to walk-in customers.</span></span>  



[!INCLUDE[footer-include](../../includes/footer-banner.md)]