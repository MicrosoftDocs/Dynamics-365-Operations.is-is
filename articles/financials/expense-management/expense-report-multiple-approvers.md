---
title: "Kostnaðarskýrslur og margir samþykkjendur"
description: "Þetta efni gefur upplýsingar um kostnaðarskýrslur sem krefjast samþykkis frá fleiri en einum einstaklingi."
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 7cd2e56dab48ad8f2380dcaa72e3317250b5b2f0
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---

# <a name="expense-reports-and-multiple-approvers"></a><span data-ttu-id="ec435-103">Kostnaðarskýrslur og margir samþykkjendur</span><span class="sxs-lookup"><span data-stu-id="ec435-103">Expense reports and multiple approvers</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="ec435-104">Það fer eftir samþykkisstefnu fyrirtækisins á kostnaði, en fleiri en einn einstaklingur gæti þurft að samþykkja kostnaðarskýrslu sem starfsmaður leggur fram.</span><span class="sxs-lookup"><span data-stu-id="ec435-104">Depending on your organization's expense approval policies, more than one person might have to approve an expense report that is submitted by an employee.</span></span> <span data-ttu-id="ec435-105">Þegar þú setur upp verkflæðisferli fyrir samþykki á kostnaðarskýrslu geturðu bætt við verkflæðiseiningum sem innihalda verk eða skref fyrir einn eða fleiri samþykkjendur kostnaðarskýrslu.</span><span class="sxs-lookup"><span data-stu-id="ec435-105">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="ec435-106">Til dæmis gætir þú krafist þess að allar kostnaðarskýrslur séu samþykktar fyrst af yfirmanni starfsmannsins sem sendi inn skýrsluna og síðan af gjaldkera.</span><span class="sxs-lookup"><span data-stu-id="ec435-106">For example, you might require that all expense reports be approved first by the manager of the employee who submitted the report and then by the Accounts payable coordinator.</span></span>

<span data-ttu-id="ec435-107">Ef þú ákveður að krefjast margra samþykkjenda fyrir kostnaðarskýrslu, getur þú bætt við verkflæðiseiningum á einhvern eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="ec435-107">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="ec435-108">Bættu við einni samþykktareiningu sem hefur eitt skref.</span><span class="sxs-lookup"><span data-stu-id="ec435-108">Add one approval element that has one step.</span></span> <span data-ttu-id="ec435-109">Til dæmis gæti skrefið krafist þess að kostnaðarskýrslu sé úthlutað til notendahóps og að hún verði samþykkt af 50 prósent af meðlimum notendahópsins.</span><span class="sxs-lookup"><span data-stu-id="ec435-109">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="ec435-110">Bættu við einni samþykktareiningu sem hefur mörg skref.</span><span class="sxs-lookup"><span data-stu-id="ec435-110">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="ec435-111">Til dæmis gæti samþykktareiningin haft eftirfarandi skref:</span><span class="sxs-lookup"><span data-stu-id="ec435-111">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="ec435-112">Yfirmaður starfsmannsins sem sendi inn kostnaðarskýrsluna samþykkir hana.</span><span class="sxs-lookup"><span data-stu-id="ec435-112">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="ec435-113">Starfsmaður viðskiptaskulda staðfestir móttökuna og vörur kostnaðarskýrslunnar.</span><span class="sxs-lookup"><span data-stu-id="ec435-113">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="ec435-114">Eigandi fjárhagsáætlunar samþykkir kostnaðarskýrsluna.</span><span class="sxs-lookup"><span data-stu-id="ec435-114">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="ec435-115">Bæta við mörgum samþykktareiningum, sem hver um sig hefur eitt skref.</span><span class="sxs-lookup"><span data-stu-id="ec435-115">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="ec435-116">Til dæmis gætirðu bætt við aðskilda samþykktareiningu fyrir hvert af eftirfarandi skrefum:</span><span class="sxs-lookup"><span data-stu-id="ec435-116">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="ec435-117">Yfirmaður starfsmannsins samþykkir kostnaðarskýrsluna.</span><span class="sxs-lookup"><span data-stu-id="ec435-117">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="ec435-118">Eigandi fjárhagsáætlunar samþykkir kostnaðarskýrsluna.</span><span class="sxs-lookup"><span data-stu-id="ec435-118">The budget owner approves the expense report.</span></span>

