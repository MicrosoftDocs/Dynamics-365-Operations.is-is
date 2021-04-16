---
title: Setja upp aðskilnaður á skyldum
description: Hægt er að setja upp reglur til að aðskilja verk sem þarf að framkvæma af mismunandi notendum.
author: peakerbl
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e25fee324ce95cd04b86ee0e4e6a56cfacb61a53
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745742"
---
# <a name="set-up-segregation-of-duties"></a><span data-ttu-id="23d15-103">Setja upp aðskilnaður á skyldum</span><span class="sxs-lookup"><span data-stu-id="23d15-103">Set up segregation of duties</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="23d15-104">Hægt er að setja upp reglur til að aðskilja verk sem þarf að framkvæma af mismunandi notendum.</span><span class="sxs-lookup"><span data-stu-id="23d15-104">You can set up rules to separate tasks that must be performed by different users.</span></span> <span data-ttu-id="23d15-105">Þetta hugtak er kallað Aðskilnaður á skyldum.</span><span class="sxs-lookup"><span data-stu-id="23d15-105">This concept is named segregation of duties.</span></span> <span data-ttu-id="23d15-106">Til dæmis gætirðu viljað að sama manneskjan staðfesti ekki móttöku á vörum og vinni úr greiðslu til lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="23d15-106">For example, you might not want the same person to acknowledge the receipt of goods and to process payment to the vendor.</span></span> <span data-ttu-id="23d15-107">Aðskilnaður á skyldum hjálpar við að minnka áhætta á svikum og það hjálpar einnig við að greina villur.</span><span class="sxs-lookup"><span data-stu-id="23d15-107">Segregation of duties helps you reduce the risk of fraud, and it also helps you detect errors or irregularities.</span></span> <span data-ttu-id="23d15-108">Þú getur einnig notað aðskilnað á skyldum til að lögbinda reglur um innra eftirlit.</span><span class="sxs-lookup"><span data-stu-id="23d15-108">You can also use segregation of duties to enforce internal control policies.</span></span> <span data-ttu-id="23d15-109">Ljúktu við eftirfarandi ferli til að stofna reglu.</span><span class="sxs-lookup"><span data-stu-id="23d15-109">Complete the following procedure to create a rule.</span></span> <span data-ttu-id="23d15-110">Þú verður að vera kerfisstjóri til að ljúka ferlinu.</span><span class="sxs-lookup"><span data-stu-id="23d15-110">You must be a system administrator to complete the procedure.</span></span>

1. <span data-ttu-id="23d15-111">Farið í **Kerfisstjórnun** > **Öryggi** > **Aðskilnaður á skyldum** > **Reglur um aðskilnað á skyldum**.</span><span class="sxs-lookup"><span data-stu-id="23d15-111">Go to **System administration** > **Security** > **Segregation of duties** > **Segregation of duties rules**.</span></span>
2. <span data-ttu-id="23d15-112">Smellt er á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="23d15-112">Click **New**.</span></span>
3. <span data-ttu-id="23d15-113">Í reitinn **Nafn** skal skrá inn gildi fyrir regluna.</span><span class="sxs-lookup"><span data-stu-id="23d15-113">In the **Name** field, type a value for the rule.</span></span>
4. <span data-ttu-id="23d15-114">Í reitnum **Fyrsta skylda** skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="23d15-114">In the **First duty** field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="23d15-115">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="23d15-115">In the list, find and select the desired record.</span></span> <span data-ttu-id="23d15-116">Veljið fyrstu skyldu sem er stýrt af reglunni.</span><span class="sxs-lookup"><span data-stu-id="23d15-116">Select the first duty that is controlled by the rule.</span></span>
6. <span data-ttu-id="23d15-117">Í reitnum **Önnur skylda** skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="23d15-117">In the **Second duty** field, click the drop-down button to open the lookup.</span></span> 
7. <span data-ttu-id="23d15-118">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="23d15-118">In the list, find and select the desired record.</span></span> <span data-ttu-id="23d15-119">Veljið aðra skyldu sem er stýrt af reglunni.</span><span class="sxs-lookup"><span data-stu-id="23d15-119">Select the second duty that is controlled by the rule.</span></span>
10. <span data-ttu-id="23d15-120">Í reitnum **Villustig** skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="23d15-120">In the **Severity** field, select an option.</span></span> <span data-ttu-id="23d15-121">Veljið villustig áhættu sem gerist þegar sama notandi eða hlutverk framkvæmir báðar skyldur.</span><span class="sxs-lookup"><span data-stu-id="23d15-121">Select the severity of the risk that occurs when the same user or role performs both duties.</span></span>  
11. <span data-ttu-id="23d15-122">Í reitinn **Öryggishætta** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="23d15-122">In the **Security risk** field, type a value.</span></span> <span data-ttu-id="23d15-123">Færið inn lýsingu á áhættu.</span><span class="sxs-lookup"><span data-stu-id="23d15-123">Enter a description of the security risk.</span></span>  
12. <span data-ttu-id="23d15-124">Í reitinn **Mótvægisaðgerðir öryggis** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="23d15-124">In the **Security mitigation** field, type a value.</span></span> <span data-ttu-id="23d15-125">Færið inn lýsingu á aðgerðum sem eru teknar til að minnka þá áhættu.</span><span class="sxs-lookup"><span data-stu-id="23d15-125">Enter a description of the actions that you take to mitigate the security risk.</span></span> <span data-ttu-id="23d15-126">Til dæmis er hægt að draga úr hættunni með framkvæmd ítarlegri yfirferða á ferlinu, með framkvæmd á mánaðarlegri rekstraryfirferð eða með því að samnýta tilföng með öðrum deildum.</span><span class="sxs-lookup"><span data-stu-id="23d15-126">For example, you can mitigate the risk by conducting more detailed reviews of the process, by conducting a monthly managerial review, or by sharing resources with other departments.</span></span>     
13. <span data-ttu-id="23d15-127">Smellt er á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="23d15-127">Click **Save**.</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="23d15-128">Fylgni við reglur fyrir aðskilnað á skyldum er ekki staðfest þegar regla er stofnuð.</span><span class="sxs-lookup"><span data-stu-id="23d15-128">Compliance with the rules for segregation of duties is not verified when you create a rule.</span></span> <span data-ttu-id="23d15-129">Hægt er að stofna reglu sem stofnar árekstra fyrir fyrirliggjandi hlutverk.</span><span class="sxs-lookup"><span data-stu-id="23d15-129">You can create a rule that creates a conflict for existing roles.</span></span> <span data-ttu-id="23d15-130">Fyrirliggjandi úthlutuð notandahlutverk geta einnig stangast á við nýju regluna.</span><span class="sxs-lookup"><span data-stu-id="23d15-130">Existing user role assignments can also be in conflict with the new rule.</span></span> <span data-ttu-id="23d15-131">Staðfesta verður samræmi eftir að regla hefur verið stofnuð eða henni breytt.</span><span class="sxs-lookup"><span data-stu-id="23d15-131">You must validate compliance after you create or modify a rule.</span></span> <span data-ttu-id="23d15-132">Frekari upplýsingar eru í [Auðkenna og leysa úr árekstrum innan aðskilnaðar á skyldum](identify-resolve-conflicts-segregation-duties.md)</span><span class="sxs-lookup"><span data-stu-id="23d15-132">For more information, see [Identify and resolve conflicts in segregation of duties](identify-resolve-conflicts-segregation-duties.md)</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]