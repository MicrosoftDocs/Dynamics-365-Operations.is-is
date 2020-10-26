---
title: Setja upp aðskilnaður á skyldum
description: Hægt er að setja upp reglur til að aðskilja verk sem þarf að framkvæma af mismunandi notendum.
author: maertenm
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 47747cba7f83d0b43a284750cff232824e00053a
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/10/2020
ms.locfileid: "3982407"
---
# <a name="set-up-segregation-of-duties"></a><span data-ttu-id="2c60f-103">Setja upp aðskilnaður á skyldum</span><span class="sxs-lookup"><span data-stu-id="2c60f-103">Set up segregation of duties</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2c60f-104">Hægt er að setja upp reglur til að aðskilja verk sem þarf að framkvæma af mismunandi notendum.</span><span class="sxs-lookup"><span data-stu-id="2c60f-104">You can set up rules to separate tasks that must be performed by different users.</span></span> <span data-ttu-id="2c60f-105">Þetta hugtak er kallað Aðskilnaður á skyldum.</span><span class="sxs-lookup"><span data-stu-id="2c60f-105">This concept is named segregation of duties.</span></span> <span data-ttu-id="2c60f-106">Til dæmis gætirðu viljað að sama manneskjan staðfesti ekki bæði móttöku á vörum og vinni úr greiðslu til lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="2c60f-106">For example, you might not want the same person both to acknowledge the receipt of goods and to process payment to the vendor.</span></span> <span data-ttu-id="2c60f-107">Aðskilnaður á skyldum hjálpar við að minnka áhætta á svikum og það hjálpar einnig við að greina villur.</span><span class="sxs-lookup"><span data-stu-id="2c60f-107">Segregation of duties helps you reduce the risk of fraud, and it also helps you detect errors or irregularities.</span></span> <span data-ttu-id="2c60f-108">Þú getur einnig notað aðskilnað á skyldum til að lögbinda reglur um innra eftirlit.</span><span class="sxs-lookup"><span data-stu-id="2c60f-108">You can also use segregation of duties to enforce internal control policies.</span></span> <span data-ttu-id="2c60f-109">Ljúktu við eftirfarandi ferli til að stofna reglu.</span><span class="sxs-lookup"><span data-stu-id="2c60f-109">Complete the following procedure to create a rule.</span></span> <span data-ttu-id="2c60f-110">Þú verður að vera kerfisstjóri til að ljúka ferlinu.</span><span class="sxs-lookup"><span data-stu-id="2c60f-110">You must be a system administrator to complete the procedure.</span></span> <span data-ttu-id="2c60f-111">Sýnigögn gögn fyrirtækisins til að stofna þetta ferli er DAT.</span><span class="sxs-lookup"><span data-stu-id="2c60f-111">The demo data company used to create this procedure is DAT.</span></span> 

1. <span data-ttu-id="2c60f-112">Farðu í **Skoðunarrúðu > Kerfiseiningar > Kerfisstjórnun > Öryggi > Aðskilnaður á skyldum > Reglur varðandi aðskilnaði á skyldum.**</span><span class="sxs-lookup"><span data-stu-id="2c60f-112">Go to **Navigation pane > Modules > System administration > Security > Segregation of duties > Segregation of duties rules**.</span></span>
2. <span data-ttu-id="2c60f-113">Smellt er á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="2c60f-113">Click **New**.</span></span>
3. <span data-ttu-id="2c60f-114">Í reitinn **Nafn** skal skrá inn gildi fyrir regluna.</span><span class="sxs-lookup"><span data-stu-id="2c60f-114">In the **Name** field, type a value for the rule.</span></span>
4. <span data-ttu-id="2c60f-115">Í reitnum **Fyrsta skylda** skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="2c60f-115">In the **First duty** field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="2c60f-116">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="2c60f-116">In the list, find and select the desired record.</span></span> <span data-ttu-id="2c60f-117">Veljið fyrstu skyldu sem er stýrt af reglunni.</span><span class="sxs-lookup"><span data-stu-id="2c60f-117">Select the first duty that is controlled by the rule.</span></span>
6. <span data-ttu-id="2c60f-118">Í reitnum **Önnur skylda** skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="2c60f-118">In the **Second duty** field, click the drop-down button to open the lookup.</span></span> 
7. <span data-ttu-id="2c60f-119">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="2c60f-119">In the list, find and select the desired record.</span></span> <span data-ttu-id="2c60f-120">Veljið aðra skyldu sem er stýrt af reglunni.</span><span class="sxs-lookup"><span data-stu-id="2c60f-120">Select the second duty that is controlled by the rule.</span></span>
10. <span data-ttu-id="2c60f-121">Í reitnum **Villustig** skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="2c60f-121">In the **Severity** field, select an option.</span></span> <span data-ttu-id="2c60f-122">Veljið villustig áhættu sem gerist þegar sama notandi eða hlutverk framkvæmir báðar skyldur.</span><span class="sxs-lookup"><span data-stu-id="2c60f-122">Select the severity of the risk that occurs when the same user or role performs both duties.</span></span>  
11. <span data-ttu-id="2c60f-123">Í reitinn **Öryggishætta** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="2c60f-123">In the **Security risk** field, type a value.</span></span> <span data-ttu-id="2c60f-124">Færið inn lýsingu á áhættu.</span><span class="sxs-lookup"><span data-stu-id="2c60f-124">Enter a description of the security risk.</span></span>  
12. <span data-ttu-id="2c60f-125">Í reitinn **Mótvægisaðgerðir öryggis** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="2c60f-125">In the **Security mitigation** field, type a value.</span></span> <span data-ttu-id="2c60f-126">Færið inn lýsingu á aðgerðum sem eru teknar til að minnka þá áhættu.</span><span class="sxs-lookup"><span data-stu-id="2c60f-126">Enter a description of the actions that you take to mitigate the security risk.</span></span> <span data-ttu-id="2c60f-127">Til dæmis er hægt að draga úr hættunni með framkvæmd ítarlegri yfirferða á ferlinu, með framkvæmd á mánaðarlegri rekstraryfirferð eða með því að samnýta tilföng með öðrum deildum.</span><span class="sxs-lookup"><span data-stu-id="2c60f-127">For example, you can mitigate the risk by conducting more detailed reviews of the process, by conducting a monthly managerial review, or by sharing resources with other departments.</span></span>     
13. <span data-ttu-id="2c60f-128">Smellt er á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="2c60f-128">Click **Save**.</span></span>

