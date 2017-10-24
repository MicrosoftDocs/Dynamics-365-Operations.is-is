---
title: "Skilgreina kostnaðarreglur"
description: "Hægt er að skilgreina kostnaðarreglur sem starfskraftar þurfa að fylgja þegar þeir búa til og senda kostnaðarskýrslur og ferðabeiðnir í Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition."
author: saraschi2
manager: AnnBe
ms.date: 09/19/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.search.region: Global
ms.author: saraschi2
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 940d6f8c3d878c2c12806ad04a092856df2acb33
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---

# <a name="expense-policies"></a><span data-ttu-id="99e7d-103">Kostnaðarreglur</span><span class="sxs-lookup"><span data-stu-id="99e7d-103">Expense policies</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="99e7d-104">Hægt er að skilgreina reglur sem starfskraftar þurfa að fylgja þegar þeir búa til og skila kostnaðarskýrslum og ferðabeiðnum.</span><span class="sxs-lookup"><span data-stu-id="99e7d-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span> <span data-ttu-id="99e7d-105">Innleiðing kostnaðarreglna getur hjálpað til við að stjórna kostnaði á áhrifaríkan hátt.</span><span class="sxs-lookup"><span data-stu-id="99e7d-105">Implementing expense policies can help you manage expenses effectively.</span></span> 

<span data-ttu-id="99e7d-106">Til dæmis er hægt að setja þá reglu að í New York borg geti hótelkostnaður fyrir hverja nótt ekki farið yfir 250 Bandaríkjadali.</span><span class="sxs-lookup"><span data-stu-id="99e7d-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span> <span data-ttu-id="99e7d-107">Ef starfsmaður skilar inn kostnaðarskýrslu eða ferðabeiðni þar sem herbergistaxtinn er yfir þessari upphæð lætur kerfið starfskraftinn vita að hann hafi farið fram úr reglubundnu kostnaðarupphæðinni.</span><span class="sxs-lookup"><span data-stu-id="99e7d-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="99e7d-108">Hægt er að breyta skilaboðunum sem starfskrafturinn mun fá þegar stefnan er skilgreind.</span><span class="sxs-lookup"><span data-stu-id="99e7d-108">You can configure the message that the worker will receive when you define the policy.</span></span> 

<span data-ttu-id="99e7d-109">Hægt er að stofna þrjár gerðir reglna:</span><span class="sxs-lookup"><span data-stu-id="99e7d-109">You can define three types of policies:</span></span> 

 - <span data-ttu-id="99e7d-110">Viðvörun - Leyfir starfskrafti að leggja fram kostnaðarskýrslu eða ferðabeiðni en kostnaðurinn verður merktur fyrir alla samþykktaraðila og</span><span class="sxs-lookup"><span data-stu-id="99e7d-110">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>  
 <span data-ttu-id="99e7d-111">fyrir síðari skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="99e7d-111">for later reporting.</span></span> 
 - <span data-ttu-id="99e7d-112">Villa - Krefst þess að starfskrafturinn endurskoði kostnaðinn til að hann verði í samræmi við reglu áður en hann sendir kostnaðarskýrslu eða ferðabeiðni.</span><span class="sxs-lookup"><span data-stu-id="99e7d-112">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span> 
 - <span data-ttu-id="99e7d-113">Rökstuðningur - Krefst þess að starfskrafturinn eða stjórnandi leggi fram rök fyrir því að farið sé yfir regluupphæð áður en hann sendir kostnaðarskýrslu eða ferðabeiðni.</span><span class="sxs-lookup"><span data-stu-id="99e7d-113">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span> 

<span data-ttu-id="99e7d-114">Einnig er hægt að setja upp dagsetningasvið þar sem kostnaðarreglur eru í gildi.</span><span class="sxs-lookup"><span data-stu-id="99e7d-114">You can also set up a date range for which expense policies are in effect.</span></span> <span data-ttu-id="99e7d-115">Til dæmis geta flugfargjöld á milli Danmerkur og New York verið há á miðju ferðatímabilinu um hátíðarnar.</span><span class="sxs-lookup"><span data-stu-id="99e7d-115">For example, airline fares for flights between Denmark and New York City can be expensive during the peak holiday travel season.</span></span> <span data-ttu-id="99e7d-116">Hægt er að skilgreina kostnaðarreglu sem takmarkar kostnað við flug til New York við 5000 krónur danskar og hægt er að taka það fram að þessi regla verði í gildi á milli 15. mars og 15. september.</span><span class="sxs-lookup"><span data-stu-id="99e7d-116">You can define a flight expense rule that restricts the cost of flights to New York City to a limit of DKK 5000, and you can specify that this rule be in effect between March 15 and September 15.</span></span> 

