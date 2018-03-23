---
title: "Skilgreina kostnaðarreglur"
description: "Hægt er að skilgreina kostnaðarreglur sem starfskraftar þurfa að fylgja þegar þeir búa til og senda kostnaðarskýrslur og ferðabeiðnir í Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition."
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 25fa39dc81fc721d7593a25a102ce47041ebc5f0
ms.openlocfilehash: b52fe81015a324bde07f387b42b834b79dc7c2da
ms.contentlocale: is-is
ms.lasthandoff: 03/13/2018

---

# <a name="expense-policies"></a><span data-ttu-id="1a0e8-103">Kostnaðarreglur</span><span class="sxs-lookup"><span data-stu-id="1a0e8-103">Expense policies</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="1a0e8-104">Hægt er að skilgreina reglur sem starfskraftar þurfa að fylgja þegar þeir búa til og skila kostnaðarskýrslum og ferðabeiðnum.</span><span class="sxs-lookup"><span data-stu-id="1a0e8-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="1a0e8-105">Innleiðing kostnaðarreglna getur hjálpað til við að stjórna kostnaði á áhrifaríkan hátt.</span><span class="sxs-lookup"><span data-stu-id="1a0e8-105">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="1a0e8-106">Til dæmis er hægt að setja þá reglu að í New York borg geti hótelkostnaður fyrir hverja nótt ekki farið yfir 250 Bandaríkjadali.</span><span class="sxs-lookup"><span data-stu-id="1a0e8-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="1a0e8-107">Ef starfsmaður skilar inn kostnaðarskýrslu eða ferðabeiðni þar sem herbergistaxtinn er yfir þessari upphæð lætur kerfið</span><span class="sxs-lookup"><span data-stu-id="1a0e8-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the</span></span>        
<span data-ttu-id="1a0e8-108">starfskraftinn vita að hann hafi farið fram úr kostnaði samkvæmt reglubundnu kostnaðarupphæðinni.</span><span class="sxs-lookup"><span data-stu-id="1a0e8-108">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="1a0e8-109">Hægt er að breyta skilaboðunum sem starfskrafturinn mun fá þegar</span><span class="sxs-lookup"><span data-stu-id="1a0e8-109">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="1a0e8-110">stefnan er skilgreind.</span><span class="sxs-lookup"><span data-stu-id="1a0e8-110">define the policy.</span></span>      
        
<span data-ttu-id="1a0e8-111">Hægt er að stofna þrjár gerðir reglna:</span><span class="sxs-lookup"><span data-stu-id="1a0e8-111">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="1a0e8-112">Viðvörun - Leyfir starfskrafti að leggja fram kostnaðarskýrslu eða ferðabeiðni en kostnaðurinn verður merktur fyrir alla samþykktaraðila og</span><span class="sxs-lookup"><span data-stu-id="1a0e8-112">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>        
<span data-ttu-id="1a0e8-113">fyrir síðari skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="1a0e8-113">for later reporting.</span></span>        

- <span data-ttu-id="1a0e8-114">Villa - Krefst þess að starfskrafturinn endurskoði kostnaðinn til að hann verði í samræmi við reglu áður en hann sendir kostnaðarskýrslu eða ferðabeiðni.</span><span class="sxs-lookup"><span data-stu-id="1a0e8-114">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>       
 
 - <span data-ttu-id="1a0e8-115">Rökstuðningur - Krefst þess að starfskrafturinn eða stjórnandi leggi fram rök fyrir því að farið sé yfir regluupphæð áður en hann sendir kostnaðarskýrslu eða ferðabeiðni.</span><span class="sxs-lookup"><span data-stu-id="1a0e8-115">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        
 
 <span data-ttu-id="1a0e8-116">Einnig er hægt að setja upp dagsetningasvið þar sem kostnaðarreglur eru í gildi.</span><span class="sxs-lookup"><span data-stu-id="1a0e8-116">You can also set up a date range for which expense policies are in effect.</span></span> <span data-ttu-id="1a0e8-117">Til dæmis geta flugfargjöld á milli Danmerkur</span><span class="sxs-lookup"><span data-stu-id="1a0e8-117">For example, airline fares for flights between Denmark</span></span>      
 <span data-ttu-id="1a0e8-118">og New York verið dýr yfir háannatíma á sumrin.</span><span class="sxs-lookup"><span data-stu-id="1a0e8-118">and New York City can be expensive during the peak holiday travel season.</span></span> <span data-ttu-id="1a0e8-119">Hægt er að skilgreina kostnaðarreglu sem takmarkar</span><span class="sxs-lookup"><span data-stu-id="1a0e8-119">You can define a flight expense rule that restricts the</span></span>      
 <span data-ttu-id="1a0e8-120">flugkostnað til New York við 5000 DKK og hægt er að taka það fram að þessi regla verði í gildi á milli 15. mars og</span><span class="sxs-lookup"><span data-stu-id="1a0e8-120">cost of flights to New York City to a limit of DKK 5000, and you can specify that this rule be in effect between March 15 and</span></span>      
 <span data-ttu-id="1a0e8-121">15. september.</span><span class="sxs-lookup"><span data-stu-id="1a0e8-121">September 15.</span></span>

