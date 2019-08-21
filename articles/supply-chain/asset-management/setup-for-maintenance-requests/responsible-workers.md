---
title: Ábyrgir viðhaldsstarfskraftar
description: Þetta efni útskýrir hvernig á að setja upp gerðir ábyrgðaraðila viðhaldsstarfskrafta í eignastjórnun.
author: josaw1
manager: AnnBe
ms.date: 07/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 432a235668bbd969f497003a98b7f66390e5308f
ms.sourcegitcommit: 2c73749779274e0b0abbcb4041bbc1df0fb6d6e4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/26/2019
ms.locfileid: "1790504"
---
# <a name="responsible-maintenance-workers"></a><span data-ttu-id="b446a-103">Ábyrgir viðhaldsstarfskraftar</span><span class="sxs-lookup"><span data-stu-id="b446a-103">Responsible maintenance workers</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="b446a-104">Ábyrgir starfsmenn viðhalds geta tengst eignategundum, eignum, starfrænum stöðum, tegundum viðhaldsstétta, viðhaldsstörfum, afbrigði af viðhaldsstörfum og viðskiptum.</span><span class="sxs-lookup"><span data-stu-id="b446a-104">Responsible maintenance workers can be related to asset types, assets, functional locations, maintenance job type categories, maintenance job types, maintenance job type variants, and trades.</span></span> <span data-ttu-id="b446a-105">Hægt er að nota þær í vinnupöntunum og viðhaldsbeiðnum til að gefa til kynna val á viðhaldsstarfsmönnunum sem ættu að vera ábyrgir fyrir verkbeiðninni.</span><span class="sxs-lookup"><span data-stu-id="b446a-105">They can be used on work orders and maintenance requests to indicate a preference about the maintenance workers who should be responsible for a work order.</span></span> <span data-ttu-id="b446a-106">(Samt sem áður eru þessir viðhaldsstarfsmenn ekki endilega sömu starfsmenn og áætlað er að framkvæma verkbeiðnina.) Notkun þessarar aðgerðar er valkvæð.</span><span class="sxs-lookup"><span data-stu-id="b446a-106">(However, those maintenance workers aren't necessarily the same workers who are scheduled to carry out the work order.) Use of this functionality is optional.</span></span> <span data-ttu-id="b446a-107">Til dæmis er hægt að nota það til að velja ábyrga starfsmenn eða starfsmannahópa fyrir ákveðnar vinnutegundir eða vinnusvæði.</span><span class="sxs-lookup"><span data-stu-id="b446a-107">For example, it can be used to select responsible workers or worker groups for specific work types or work areas.</span></span>

<span data-ttu-id="b446a-108">Meðan á líftíma verkbeiðni stendur eða líftíma viðhaldsbeiðni er hægt að breyta eða uppfæra ábyrga starfsmenn viðhalds.</span><span class="sxs-lookup"><span data-stu-id="b446a-108">During a work order lifecycle or a maintenance request lifecycle, responsible maintenance workers can be changed or updated.</span></span> <span data-ttu-id="b446a-109">Þessi breyting eða uppfærsla gæti tengst til dæmis breytingu á líftíma viðhaldsbeiðni eða líftíma verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="b446a-109">This change or update might be related to, for example, a change in the maintenance request lifecycle state or the work order lifecycle state.</span></span>

<span data-ttu-id="b446a-110">Uppsetningin á **Ábyrgir starfsmenn viðhalds** síðu er *ekki* notuð við tímasetningar verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="b446a-110">The setup on the **Responsible maintenance workers** page is *not* used during work order scheduling.</span></span>

> [!NOTE]
> <span data-ttu-id="b446a-111">Í eignastjórnun geturðu einnig sett upp *valinn* viðhaldsstarfsmenn sem gætu verið úthlutaðir til vinnupantana við tímasetningar verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="b446a-111">In Asset Management, you can also set up *preferred* maintenance workers who might be allocated to work orders during work order scheduling.</span></span>

<span data-ttu-id="b446a-112">Áður en þú getur sett upp ábyrga starfsmenn viðhalds verður þú að setja upp starfsmenn og hópa starfsmanna viðhalds sem ættu að vera tiltækir fyrir val.</span><span class="sxs-lookup"><span data-stu-id="b446a-112">Before you can set up responsible maintenance workers, you must set up the workers and maintenance worker groups that should be available for selection.</span></span> <span data-ttu-id="b446a-113">(Sjá upplýsingar um hvernig á að setja upp starfskrafta og viðhaldsstarfsmannahóps [Viðhaldsstarfsmenn og starfsmannahópar](../setup-for-objects/workers-and-worker-groups.md) .)</span><span class="sxs-lookup"><span data-stu-id="b446a-113">For information about how to set up workers and maintenance worker groups, see [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).</span></span>

## <a name="set-up-responsible-maintenance-workers"></a><span data-ttu-id="b446a-114">Setja upp ábyrga viðhaldsstarfskrafta</span><span class="sxs-lookup"><span data-stu-id="b446a-114">Set up responsible maintenance workers</span></span>

1. <span data-ttu-id="b446a-115">Veldu **Eignastýring** \> **Uppsetning** \> **Starfskraftar** \> **Ábyrgir starfsmenn viðhalds**.</span><span class="sxs-lookup"><span data-stu-id="b446a-115">Select **Asset management** \> **Setup** \> **Workers** \> **Responsible maintenance workers**.</span></span>
2. <span data-ttu-id="b446a-116">Veljið **Ný** til að stofna nýja skrá.</span><span class="sxs-lookup"><span data-stu-id="b446a-116">Select **New** to create a record.</span></span>
3. <span data-ttu-id="b446a-117">Búðu fyrst til sjálfgefinn viðhaldsstarfsmann eða skipulag ábyrgan viðhaldsstarfsmannahóp þar sem þú stillir aðeins **Ábyrgur hópur viðhaldsstarfsmanna** reit og/eða retiinn **Ábyrgðarmaður**.</span><span class="sxs-lookup"><span data-stu-id="b446a-117">First create a default responsible maintenance worker or responsible maintenance worker group setup, where you set only the **Responsible maintenance worker group** field and/or the **Responsible worker** field.</span></span> <span data-ttu-id="b446a-118">Skildu reitina sem eftir eru auðir.</span><span class="sxs-lookup"><span data-stu-id="b446a-118">Leave the remaining fields blank.</span></span> <span data-ttu-id="b446a-119">Þessi sjálfgefna uppsetning verður notuð við tímasetningu verkbeiðni ef engin önnur, sértækari samsetning passar við innihald verkbeiðninnar.</span><span class="sxs-lookup"><span data-stu-id="b446a-119">This default setup will be used during work order scheduling if no other, more specific combination matches the contents of the work order.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b446a-120">Þegar stofnað er til viðhaldsbeiðni, þegar ábyrgur viðhaldsstarfsmaður eða ábyrgur viðhaldsstarfsmannahópur er gerður tiltækur fyrir val á **Allar viðhaldsbeiðnir** síðu, Eignastjórn fer í gegnum allar ábyrgar skrár starfsmanna viðhalds til að athuga hvort mögulegt sé samsvörun.</span><span class="sxs-lookup"><span data-stu-id="b446a-120">During creation of a maintenance request, when a responsible maintenance worker or responsible maintenance worker group is made available for selection on the **All maintenance requests** page, Asset Management goes through all responsible maintenance worker records to check for a possible match.</span></span> <span data-ttu-id="b446a-121">Það athugar alltaf sértækustu samsetninguna fyrst.</span><span class="sxs-lookup"><span data-stu-id="b446a-121">It always checks the most specific combination first.</span></span> <span data-ttu-id="b446a-122">Með öðrum orðum, Eignastjórnun kannar fyrst hvort samsvörun finnist fyrir reitinn **Viðskipti**.</span><span class="sxs-lookup"><span data-stu-id="b446a-122">In other words, Asset Management first checks for a match for the **Trade** field.</span></span> <span data-ttu-id="b446a-123">Ef engin samsvörun er fundin, skoðar hún hvort samsvörun sé fyrir reitinn **Afbrigði af viðhaldsstörfum**.</span><span class="sxs-lookup"><span data-stu-id="b446a-123">If no match is found, it checks for a match for the **Maintenance job type variant** field.</span></span> <span data-ttu-id="b446a-124">Ef engin samsvörun er fundin, skoðar hún hvort samsvörun sé fyrir reitinn **Afbrigði af viðhaldsstörfum** og svo framvegis.</span><span class="sxs-lookup"><span data-stu-id="b446a-124">If no match is found, it checks for a match for the **Maintenance job type** field, and so on.</span></span> <span data-ttu-id="b446a-125">Eins og þú sérð á skipulagi síðunnar þýðir þessi hegðun að til að finna sértækustu samsetninguna, þá hefur Eignastýring athugað hverja skrá frá hægri til vinstri fyrir leik (fyrst **Viðskipti**, síðan **Afbrigði af viðhaldsstörfum**, síðan **Tegund viðhalds**, síðan **Flokkur um viðhaldsstörf**, síðan **Virk staðsetning**, síðan **Eignir**, og að lokum **Tegund eigna**).</span><span class="sxs-lookup"><span data-stu-id="b446a-125">As you can see in the layout of the page, this behavior means that, to find the most specific combination, Asset Management checks each record from right to left for a match (first **Trade**, then **Maintenance job type variant**, then **Maintenance job type**, then **Maintenance job type category**, then **Functional location**, then **Asset**, and finally **Asset type**).</span></span> <span data-ttu-id="b446a-126">Ef engin samsvörun er notuð er sjálfgefna skráin sem hefur ekkert val í þeim sjö reitum notuð.</span><span class="sxs-lookup"><span data-stu-id="b446a-126">If no match is found, the default record that has no selections in those seven fields is used.</span></span>

<span data-ttu-id="b446a-127">Eftirfarandi mynd sýnir dæmi um listasíðuna **Ábyrgir viðhaldsstarfsmenn**.</span><span class="sxs-lookup"><span data-stu-id="b446a-127">The following illustration shows an example of the **Responsible maintenance workers** page.</span></span>

![Mynd 1](media/08-setup-for-requests.png)
