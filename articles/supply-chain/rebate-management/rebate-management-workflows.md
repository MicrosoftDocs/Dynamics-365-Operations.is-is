---
title: Verkflæði tilboða fyrir stjórnun eftirágreidds afsláttar
description: Í þessu efnisatriði er útskýrt hvernig á að setja upp verkflæði tilboðs fyrir stjórnun eftirágreidds afsláttar til að samþykkja og virkja tilboð.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 37b8022633e61c4d98d6f5d129bcf494a9ed92e0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831723"
---
# <a name="rebate-management-deal-workflows"></a><span data-ttu-id="9173b-103">Verkflæði tilboða fyrir stjórnun eftirágreidds afsláttar</span><span class="sxs-lookup"><span data-stu-id="9173b-103">Rebate management deal workflows</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="9173b-104">Til að samþykkja eftirágreidda afslætti notar stjórnunar eftirágreidds afsláttar sama verkflæðisvettvang og önnur Finance and Operations forrit.</span><span class="sxs-lookup"><span data-stu-id="9173b-104">To approve rebate deals, Rebate management uses the same workflow platform as other Finance and Operations apps.</span></span> <span data-ttu-id="9173b-105">Tvö vinnsluferli eru tengd við öll verkflæði:</span><span class="sxs-lookup"><span data-stu-id="9173b-105">Two job processes are associated with every workflow:</span></span>

- <span data-ttu-id="9173b-106">Einn þáttur verkflæðisins virkjar tilboðið þannig að notandinn eða verkflæðisferlið getur samþykkt færslurnar.</span><span class="sxs-lookup"><span data-stu-id="9173b-106">One element of the workflow activates the deal so that the user or workflow process can approve the transactions.</span></span>
- <span data-ttu-id="9173b-107">Einn þáttur verkflæðisins samþykkir tilboðið.</span><span class="sxs-lookup"><span data-stu-id="9173b-107">One element of the workflow approves the deal.</span></span>

<span data-ttu-id="9173b-108">Áður en hægt er að nota tilboð eftirágreidds afsláttar þarf það að vera virkt í einingunni **Stjórnun eftirágreidds afsláttar**.</span><span class="sxs-lookup"><span data-stu-id="9173b-108">Before you can use a rebate deal, it must be active in the **Rebate management** module.</span></span> <span data-ttu-id="9173b-109">Til að virkja tilboð þarf fyrst að stofna og grunnstilla *Verkflæði tilboða fyrir stjórnun eftirágreidds afsláttar*.</span><span class="sxs-lookup"><span data-stu-id="9173b-109">To activate a deal, you must first create and configure a *Rebate management deal workflow*.</span></span>

<span data-ttu-id="9173b-110">Þegar verkflæði hefur verið virkjað fyrir stjórnun eftirágreidds afsláttar, geta notendur ekki samþykkt tilboð handvirkt.</span><span class="sxs-lookup"><span data-stu-id="9173b-110">After a workflow is activated for Rebate management, users can't manually approve deals.</span></span> <span data-ttu-id="9173b-111">Alltaf verður að nota verkflæðið.</span><span class="sxs-lookup"><span data-stu-id="9173b-111">The workflow must be always used.</span></span>

## <a name="create-and-manage-rebate-management-deal-workflows"></a><span data-ttu-id="9173b-112">Stofna og hafa umsjón með verkflæði tilboða fyrir stjórnun eftirágreidds afsláttar</span><span class="sxs-lookup"><span data-stu-id="9173b-112">Create and manage Rebate management deal workflows</span></span>

<span data-ttu-id="9173b-113">Til að vinna með verkflæði tilboða fyrir stjórnun eftirágreidds afsláttar skal fara í **Stjórnun eftirágreidds afsláttar \> Uppsetning \> Verkflæði tilboða fyrir stjórnun eftirágreidds afsláttar**.</span><span class="sxs-lookup"><span data-stu-id="9173b-113">To work with your Rebate management deal workflows, go to **Rebate management \> Setup \> Rebate management workflows**.</span></span> <span data-ttu-id="9173b-114">Þar er hægt að skoða, búa til og uppfæra verkflæði eins og þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="9173b-114">There, you can view, create, and update workflows as required.</span></span> <span data-ttu-id="9173b-115">Aðeins eitt verkflæði af þessari gerð getur verið virkt í einu.</span><span class="sxs-lookup"><span data-stu-id="9173b-115">Only one workflow of this type can be active at a time.</span></span> <span data-ttu-id="9173b-116">Frekari upplýsingar um verkflæði, hvernig á að nota síðuna **Verkflæði fyrir stjórnun eftirágreidds afsláttar** og hvernig á að stofna verkflæði er að finna í [Yfirlit yfir verkflæðiskerfi](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md) og tengdum efnisatriðum.</span><span class="sxs-lookup"><span data-stu-id="9173b-116">For more information about workflows, how to work with the **Rebate management workflows** page, and how to create workflows, see [Workflow system overview](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md) and its related topics.</span></span>

## <a name="use-a-workflow-to-activate-a-deal"></a><span data-ttu-id="9173b-117">Nota verkflæði til að virkja tilboð</span><span class="sxs-lookup"><span data-stu-id="9173b-117">Use a workflow to activate a deal</span></span>

<span data-ttu-id="9173b-118">Til að virkja tilboð í verkflæði skal opna tilboðið (til dæmis á **Öll tilboð fyrir stjórnun eftirágreidds afsláttar** síðunni).</span><span class="sxs-lookup"><span data-stu-id="9173b-118">To activate a deal through a workflow, open the deal (for example, on the **All rebate management deals** page).</span></span> <span data-ttu-id="9173b-119">Í aðgerðasvæðinu er síðan smellt á **Verkflæði \> Senda**.</span><span class="sxs-lookup"><span data-stu-id="9173b-119">Then, on the Action Pane, select **Workflow \> Submit**.</span></span> <span data-ttu-id="9173b-120">Þegar búið er að vinna úr og samþykkja nýtt tilboð í gegnum verkflæðið verður það virkt og tilbúið til notkunar.</span><span class="sxs-lookup"><span data-stu-id="9173b-120">After the new deal has been processed and approved through the workflow, it will be active and ready to use.</span></span>

<span data-ttu-id="9173b-121">Þegar tilboð hefur verið virkjað er ekki hægt að breyta uppsetningu þess.</span><span class="sxs-lookup"><span data-stu-id="9173b-121">After a deal has been activated, you can't change its setup.</span></span> <span data-ttu-id="9173b-122">Ef breyta þarf virku tilboði skal gera það óvirkt og stofna nýtt.</span><span class="sxs-lookup"><span data-stu-id="9173b-122">If you must change an active deal, inactivate it, and then create a new deal.</span></span> <span data-ttu-id="9173b-123">Ef nýja tilboðið á að líkjast gamla tilboðinu er hægt að stofna það með því að afrita það gamla.</span><span class="sxs-lookup"><span data-stu-id="9173b-123">If the new deal will resemble the old deal, you can create it by copying the old deal.</span></span>
