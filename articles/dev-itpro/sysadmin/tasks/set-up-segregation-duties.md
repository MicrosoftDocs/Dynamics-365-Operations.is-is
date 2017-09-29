--- 
title: "Setja upp aðskilnaður á skyldum"
description: "Hægt er að setja upp reglur til að aðskilja verk sem þarf að framkvæma af mismunandi notendum."
author: maertenm
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 754f28cd2831d8a9a57c408518d240de460b732b
ms.contentlocale: is-is
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-segregation-of-duties"></a><span data-ttu-id="02c50-103">Setja upp aðskilnaður á skyldum</span><span class="sxs-lookup"><span data-stu-id="02c50-103">Set up segregation of duties</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="02c50-104">Hægt er að setja upp reglur til að aðskilja verk sem þarf að framkvæma af mismunandi notendum.</span><span class="sxs-lookup"><span data-stu-id="02c50-104">You can set up rules to separate tasks that must be performed by different users.</span></span> <span data-ttu-id="02c50-105">Þetta hugtak er kallað Aðskilnaður á skyldum.</span><span class="sxs-lookup"><span data-stu-id="02c50-105">This concept is named segregation of duties.</span></span> <span data-ttu-id="02c50-106">Til dæmis gætirðu viljað að sama manneskjan staðfesti ekki bæði móttöku á vörum og vinni úr greiðslu til lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="02c50-106">For example, you might not want the same person both to acknowledge the receipt of goods and to process payment to the vendor.</span></span> <span data-ttu-id="02c50-107">Aðskilnaður á skyldum hjálpar við að minnka áhætta á svikum og það hjálpar einnig við að greina villur.</span><span class="sxs-lookup"><span data-stu-id="02c50-107">Segregation of duties helps you reduce the risk of fraud, and it also helps you detect errors or irregularities.</span></span> <span data-ttu-id="02c50-108">Þú getur einnig notað aðskilnað á skyldum til að lögbinda reglur um innra eftirlit.</span><span class="sxs-lookup"><span data-stu-id="02c50-108">You can also use segregation of duties to enforce internal control policies.</span></span> <span data-ttu-id="02c50-109">Ljúktu við eftirfarandi ferli til að stofna reglu.</span><span class="sxs-lookup"><span data-stu-id="02c50-109">Complete the following procedure to create a rule.</span></span> <span data-ttu-id="02c50-110">Þú verður að vera kerfisstjóri til að ljúka ferlinu.</span><span class="sxs-lookup"><span data-stu-id="02c50-110">You must be a system administrator to complete the procedure.</span></span> <span data-ttu-id="02c50-111">Sýnigögn gögn fyrirtækisins til að stofna þetta ferli er DAT.</span><span class="sxs-lookup"><span data-stu-id="02c50-111">The demo data company used to create this procedure is DAT.</span></span> 

1. <span data-ttu-id="02c50-112">Farið í kerfisstjórnun > Öryggi > Aðskilnaður á skyldum > Reglur varðandi aðskilnaði á skyldum.</span><span class="sxs-lookup"><span data-stu-id="02c50-112">Go to System administration > Security > Segregation of duties > Segregation of duties rules.</span></span>
2. <span data-ttu-id="02c50-113">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="02c50-113">Click New.</span></span>
3. <span data-ttu-id="02c50-114">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="02c50-114">In the Name field, type a value.</span></span>
    * <span data-ttu-id="02c50-115">Færðu inn heiti reglunnar.</span><span class="sxs-lookup"><span data-stu-id="02c50-115">Enter a name for the rule.</span></span>  
4. <span data-ttu-id="02c50-116">Í reitnum Fyrsta skylda skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="02c50-116">In the First duty field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="02c50-117">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="02c50-117">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="02c50-118">Veljið fyrstu skyldu sem er stýrt af reglunni.</span><span class="sxs-lookup"><span data-stu-id="02c50-118">Select the first duty that is controlled by the rule.</span></span>  
6. <span data-ttu-id="02c50-119">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="02c50-119">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="02c50-120">Í reitnum Önnur skylda skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="02c50-120">In the Second duty field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="02c50-121">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="02c50-121">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="02c50-122">Veljið aðra skyldu sem er stýrt af reglunni.</span><span class="sxs-lookup"><span data-stu-id="02c50-122">Select the second duty that is controlled by the rule.</span></span>  
9. <span data-ttu-id="02c50-123">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="02c50-123">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="02c50-124">Í reitnum Villustig skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="02c50-124">In the Severity field, select an option.</span></span>
    * <span data-ttu-id="02c50-125">Veljið villustig áhættu sem gerist þegar sama notandi eða hlutverk framkvæmir báðar skyldur.</span><span class="sxs-lookup"><span data-stu-id="02c50-125">Select the severity of the risk that occurs when the same user or role performs both duties.</span></span>  
11. <span data-ttu-id="02c50-126">Í reitinn Öryggishætta skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="02c50-126">In the Security risk field, type a value.</span></span>
    * <span data-ttu-id="02c50-127">Færið inn lýsingu á áhættu.</span><span class="sxs-lookup"><span data-stu-id="02c50-127">Enter a description of the security risk.</span></span>  
12. <span data-ttu-id="02c50-128">Í reitinn Mótvægisaðgerðir öryggis skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="02c50-128">In the Security mitigation field, type a value.</span></span>
    * <span data-ttu-id="02c50-129">Færið inn lýsingu á aðgerðum sem eru teknar til að minnka þá áhættu.</span><span class="sxs-lookup"><span data-stu-id="02c50-129">Enter a description of the actions that you take to mitigate the security risk.</span></span> <span data-ttu-id="02c50-130">Til dæmis er hægt að draga úr hættunni með framkvæmd ítarlegri yfirferða á ferlinu, með framkvæmd á mánaðarlegri rekstraryfirferð eða með því að samnýta tilföng með öðrum deildum.</span><span class="sxs-lookup"><span data-stu-id="02c50-130">For example, you can mitigate the risk by conducting more detailed reviews of the process, by conducting a monthly managerial review, or by sharing resources with other departments.</span></span>  
13. <span data-ttu-id="02c50-131">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="02c50-131">Click Save.</span></span>


