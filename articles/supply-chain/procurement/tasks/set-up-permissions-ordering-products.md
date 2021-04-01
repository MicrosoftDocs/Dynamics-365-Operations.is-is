---
title: Setja upp heimildir fyrir pöntun afurða fyrir hönd annarra
description: Þetta efni útskýrir hvernig á að veita starfsmönnum heimild til að undirbúa innkaupabeiðnir fyrir hönd annarra starfsmanna.
author: RichardLuan
manager: tfehr
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchReqAuthorization, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 54d84e38a8816ec716414661d002cbe171623772
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5244016"
---
# <a name="set-up-permissions-for-ordering-products-on-behalf-of-someone-else"></a><span data-ttu-id="a78e8-103">Setja upp heimildir fyrir pöntun afurða fyrir hönd annarra</span><span class="sxs-lookup"><span data-stu-id="a78e8-103">Set up permissions for ordering products on behalf of someone else</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a78e8-104">Þetta efni útskýrir hvernig á að veita starfsmönnum heimild til að undirbúa innkaupabeiðnir fyrir hönd annarra starfsmanna.</span><span class="sxs-lookup"><span data-stu-id="a78e8-104">This topic explains how to grant workers permission to prepare purchase requisitions on behalf of other workers.</span></span> <span data-ttu-id="a78e8-105">Með öðrum orðum getur „undirbúningsaðili“ innkaupabeiðni stofnað beiðni fyrir annan „umsækjanda.“</span><span class="sxs-lookup"><span data-stu-id="a78e8-105">In other words, a purchase requisition "preparer" can create a requisition for another "requester."</span></span> <span data-ttu-id="a78e8-106">Ferlið sýnir einnig hvernig á að veita starfskrafti heimild til að panta vörur og þjónustu í öðrum lögaðilum eða rekstrareiningum.</span><span class="sxs-lookup"><span data-stu-id="a78e8-106">The procedure also shows how to grant a worker permission to order items and services in different legal entities or operating units.</span></span> <span data-ttu-id="a78e8-107">Þessi verk eru yfirleitt gert af innkaupastjóra.</span><span class="sxs-lookup"><span data-stu-id="a78e8-107">Typically, these tasks are performed by a purchasing manager.</span></span> <span data-ttu-id="a78e8-108">Hægt er að nota þetta ferli í annað hvort fyrir gögn fyrir sýnigögn USMF- fyrirtækisins eða þín eigin gögn.</span><span class="sxs-lookup"><span data-stu-id="a78e8-108">You can use this procedure either on data for the USMF demo company or on your own data.</span></span>


## <a name="grant-permission-to-enter-purchase-requisitions-on-behalf-of-another-worker"></a><span data-ttu-id="a78e8-109">Veita heimildir til að færa inn innkaupabeiðnir fyrir hönd annan starfsmann</span><span class="sxs-lookup"><span data-stu-id="a78e8-109">Grant permission to enter purchase requisitions on behalf of another worker</span></span>
1. <span data-ttu-id="a78e8-110">Í skoðunarrúðunni ferðu í **Kerfiseiningar > Innkaup og aðföng > Uppsetning > Reglur > Heimildir innkaupabeiðni**.</span><span class="sxs-lookup"><span data-stu-id="a78e8-110">In the navigation pane, go to **Modules > Procurement and sourcing > Setup > Policies > Purchase requisition permissions**.</span></span> <span data-ttu-id="a78e8-111">Gangið úr skugga um að reiturinn **Núverandi yfirlit** er stillt á **Af undirbúningsaðila**.</span><span class="sxs-lookup"><span data-stu-id="a78e8-111">Make sure that the **Current view** field is set to **By preparer**.</span></span> <span data-ttu-id="a78e8-112">Á listanum í vinstri rúðunni sýnir fólki sem getur fengið heimild til að undirbúa beiðnir fyrir hönd annars fólks.</span><span class="sxs-lookup"><span data-stu-id="a78e8-112">The list in the left pane shows the people who can be granted permission to prepare requisitions on behalf of other people.</span></span>  
2. <span data-ttu-id="a78e8-113">Veljið einstakling sem veita á heimildir (undirbúningsaðili).</span><span class="sxs-lookup"><span data-stu-id="a78e8-113">Select the person to grant permission to (the preparer).</span></span>
3. <span data-ttu-id="a78e8-114">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="a78e8-114">Select **Add**.</span></span>
4. <span data-ttu-id="a78e8-115">Finna og velja einstaklinginn sem er bætt við sem umsækjanda.</span><span class="sxs-lookup"><span data-stu-id="a78e8-115">Find and select the person to add as a requester.</span></span>
    - <span data-ttu-id="a78e8-116">Umsækjandinn er sá aðili, fyrir hvers hönd undirbúningsaðili getur stofnað beiðnir fyrir.</span><span class="sxs-lookup"><span data-stu-id="a78e8-116">The requester is the person that the preparer can create requisitions on behalf of.</span></span>  
    - <span data-ttu-id="a78e8-117">Í svæðinu **Heimild** skal velja **Tiltekinn** ef undirbúningsaðili á að geta stofna innkaupabeiðnir fyrir hönd valins starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="a78e8-117">In the **Authorization** field, select **Specific** if the preparer should be able to create purchase requisitions on behalf of the selected worker.</span></span> <span data-ttu-id="a78e8-118">Veljið **skýrslugjöf** ef undirbúningsaðili á einnig að geta stofnað innkaupabeiðnir fyrir hönd allra starfsmanna sem ber skylda til skýrslugjafar til þess aðila.</span><span class="sxs-lookup"><span data-stu-id="a78e8-118">Select **Reporting** if the preparer should also be able to create purchase requisitions on behalf of all workers who report to that worker.</span></span>  
5. <span data-ttu-id="a78e8-119">Í reitinn **Tekur gildi** skal færa inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="a78e8-119">In the **Effective** field, enter a date.</span></span>
6. <span data-ttu-id="a78e8-120">**Í reitinn lokadagsetning, skal færa inn dagsetningu.**</span><span class="sxs-lookup"><span data-stu-id="a78e8-120">In the **Expiration** field, enter a date.</span></span>

## <a name="view-preparers-who-have-permission-to-create-purchase-requisitions-for-a-selected-worker"></a><span data-ttu-id="a78e8-121">Skoða undirbúningsaðila sem hafa heimild til að stofna innkaupabeiðnir fyrir valinn starfsmann</span><span class="sxs-lookup"><span data-stu-id="a78e8-121">View preparers who have permission to create purchase requisitions for a selected worker</span></span>
1. <span data-ttu-id="a78e8-122">Í reitnum **Núverandi yfirlit** skal velja **Eftir umsækjanda**.</span><span class="sxs-lookup"><span data-stu-id="a78e8-122">In the **Current view** field, select **By requester**.</span></span> <span data-ttu-id="a78e8-123">Þetta yfirlit sýnir lista yfir undirbúningsaðila sem hafa fengið heimild til að stofna innkaupabeiðnir fyrir hönd valins starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="a78e8-123">This view shows a list of preparers who have been granted permission to create purchase requisitions on behalf of a selected worker.</span></span>  
2. <span data-ttu-id="a78e8-124">Nota flýtiafmörkun til að finna starfsmann sem var nýverið bætt við sem umsækjanda.</span><span class="sxs-lookup"><span data-stu-id="a78e8-124">Use the Quick Filter to find the worker that you just added as the requester.</span></span>
3. <span data-ttu-id="a78e8-125">Veljið umsækjanda</span><span class="sxs-lookup"><span data-stu-id="a78e8-125">Select the requester.</span></span> <span data-ttu-id="a78e8-126">Listi Undirbúningsaðila sýnir fólk sem hefur heimild til að panta hluti fyrir hönd umsækjandans sem er valinn á rúðunni vinstra megin.</span><span class="sxs-lookup"><span data-stu-id="a78e8-126">The Preparer list shows the people who have permission to order items on behalf of the requester who is selected in the left pane.</span></span>  <span data-ttu-id="a78e8-127">Hægt er að bæta við fleiri undirbúningsaðilum hér.</span><span class="sxs-lookup"><span data-stu-id="a78e8-127">You can add additional preparers here.</span></span> <span data-ttu-id="a78e8-128">Þetta yfirlit leyfir þér einnig að veita umsækjanda heimild til að stofna beiðnir í lögaðilum og rekstrareiningum sem eru ekki aðal lögaðili eða rekstrareining þess einstaklings.</span><span class="sxs-lookup"><span data-stu-id="a78e8-128">This view also lets you grant the requester permission to create requisitions in legal entities and operating units that aren't that person's primary legal entity or operating unit.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]