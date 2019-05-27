---
title: Skilgreina kostnaðarreglur
description: Hægt er að skilgreina reglur sem starfskraftar þurfa að fylgja þegar þeir búa til og skila kostnaðarskýrslum og ferðabeiðnum í Microsoft Dynamics 365 for Finance and Operations.
author: ryansandness
manager: AnnBe
ms.date: 04/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9f0ff56f0ff106bc168b6a27612e08743a539a07
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/07/2019
ms.locfileid: "1514440"
---
# <a name="expense-policies"></a><span data-ttu-id="63037-103">Kostnaðarreglur</span><span class="sxs-lookup"><span data-stu-id="63037-103">Expense policies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="63037-104">Hægt er að skilgreina reglur sem starfskraftar þurfa að fylgja þegar þeir búa til og skila kostnaðarskýrslum og ferðabeiðnum.</span><span class="sxs-lookup"><span data-stu-id="63037-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="63037-105">Innleiðing kostnaðarreglna getur hjálpað til við að stjórna kostnaði á áhrifaríkan hátt.</span><span class="sxs-lookup"><span data-stu-id="63037-105">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="63037-106">Til dæmis er hægt að setja þá reglu að í New York borg geti hótelkostnaður fyrir hverja nótt ekki farið yfir 250 Bandaríkjadali.</span><span class="sxs-lookup"><span data-stu-id="63037-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="63037-107">Ef starfsmaður skilar inn kostnaðarskýrslu eða ferðabeiðni þar sem herbergistaxtinn er yfir þessari upphæð lætur kerfið</span><span class="sxs-lookup"><span data-stu-id="63037-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the</span></span>        
<span data-ttu-id="63037-108">starfskraftinn vita að hann hafi farið fram úr kostnaði samkvæmt reglubundnu kostnaðarupphæðinni.</span><span class="sxs-lookup"><span data-stu-id="63037-108">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="63037-109">Hægt er að breyta skilaboðunum sem starfskrafturinn mun fá þegar</span><span class="sxs-lookup"><span data-stu-id="63037-109">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="63037-110">stefnan er skilgreind.</span><span class="sxs-lookup"><span data-stu-id="63037-110">define the policy.</span></span>      
        
<span data-ttu-id="63037-111">Hægt er að stofna þrjár gerðir reglna:</span><span class="sxs-lookup"><span data-stu-id="63037-111">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="63037-112">Viðvörun - Leyfir starfskrafti að leggja fram kostnaðarskýrslu eða ferðabeiðni en kostnaðurinn verður merktur fyrir alla samþykktaraðila og</span><span class="sxs-lookup"><span data-stu-id="63037-112">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>        
  <span data-ttu-id="63037-113">fyrir síðari skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="63037-113">for later reporting.</span></span>        

- <span data-ttu-id="63037-114">Villa - Krefst þess að starfskrafturinn endurskoði kostnaðinn til að hann verði í samræmi við reglu áður en hann sendir kostnaðarskýrslu eða ferðabeiðni.</span><span class="sxs-lookup"><span data-stu-id="63037-114">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>       
 
 - <span data-ttu-id="63037-115">Rökstuðningur - Krefst þess að starfskrafturinn eða stjórnandi leggi fram rök fyrir því að farið sé yfir regluupphæð áður en hann sendir kostnaðarskýrslu eða ferðabeiðni.</span><span class="sxs-lookup"><span data-stu-id="63037-115">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

# <a name="policy-tips"></a><span data-ttu-id="63037-116">Ábendingar um reglu</span><span class="sxs-lookup"><span data-stu-id="63037-116">Policy tips</span></span>
<span data-ttu-id="63037-117">Hér eru nokkrar tillögur sem geta aðstoðað þig við að búa til nýjar reglur varðandi útgjaldastýringu.</span><span class="sxs-lookup"><span data-stu-id="63037-117">Here are a few suggestions that can assist you whe creating new policies for expense management.</span></span> 
* <span data-ttu-id="63037-118">Reglur miðast við dagsetningar og taka ekki gildi ef reglan er búin til með dagsetningu sem kemur á eftir dagsetningunni sem kostnaðurinn átti sér stað.</span><span class="sxs-lookup"><span data-stu-id="63037-118">Policies are date effective and won't take effect if the policy is created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="63037-119">Ef þú til dæmis býrð til nýja reglu í dag til að framfylgja hámarkskostnaði á máltíð sem nemur 50 USD, verður enginn núverandi kostnaður sem var færður inn í gær athugaður í tengslum við þessa reglu.</span><span class="sxs-lookup"><span data-stu-id="63037-119">For example, if you are creating a new policy today to enforce a maximum meal expense of $50, then any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
* <span data-ttu-id="63037-120">Þegar reglu er búin til fyrir kostnaðartegund sem hægt er að sundurliða, skaltu íhuga að bæta við skilyrði fyrir gerð kostnaðarlínu.</span><span class="sxs-lookup"><span data-stu-id="63037-120">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="63037-121">Sumar reglur á borð við að krefjast kvittunar passa hugsanlega ekki við sundurliðaðar línur og ætti aðeins að nota þær fyrir hauslínu eða línu sem er ekki sundurliðuð.</span><span class="sxs-lookup"><span data-stu-id="63037-121">Some policies such as requiring a receipt may not make sense for itemized lines and should only be applied to the header line or a non-itemized line.</span></span> 

# <a name="when-to-evaluate-policies"></a><span data-ttu-id="63037-122">Hvenær meta skal reglur</span><span class="sxs-lookup"><span data-stu-id="63037-122">When to evaluate policies</span></span>

<span data-ttu-id="63037-123">Í færibreytum útgjaldastýringar er möguleiki á því að annaðhvort meta reglur útgjaldastýringar þegar lína er vistuð eða þegar kostnaðarskýrsla er send inn.</span><span class="sxs-lookup"><span data-stu-id="63037-123">In expense management parameters, there is an option to either evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="63037-124">Ef valið er að meta þegar lína er vistuð tryggir það að notendur verði með sýnileika fyrr á því hvað þurfi að gera til að ljúka allri kostnaðarskýrslunni í einu.</span><span class="sxs-lookup"><span data-stu-id="63037-124">If you choose to evaluate when a line is saved this ensures that users have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="63037-125">Annars er hægt að fresta reglumati og spara tíma ef villuleit er gerð í lokin við innsendingu á verkflæði.</span><span class="sxs-lookup"><span data-stu-id="63037-125">Otherwise, you can delay policy evaluation and save time if you have validation occur at the end, during submission to workflow.</span></span>
