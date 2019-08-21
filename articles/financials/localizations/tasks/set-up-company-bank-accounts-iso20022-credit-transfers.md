---
title: Setja upp bankareikninga fyrirtækis fyrir ISO20022-kreditfærslur
description: Þetta Leiðbeiningar sýnir hvernig á að setja upp bankareikningsupplýsingar fyrir fyrirtæki sem þarf fyrir myndun greiðsluskrár.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankAccountTable, OMLegalEntity, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2bbbf55ed28ad2131d7e1253dd44842d85d39315
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/02/2019
ms.locfileid: "1848745"
---
# <a name="set-up-company-bank-accounts-for-iso20022-credit-transfers"></a><span data-ttu-id="d99be-103">Setja upp bankareikninga fyrirtækis fyrir ISO20022-kreditfærslur</span><span class="sxs-lookup"><span data-stu-id="d99be-103">Set up company bank accounts for ISO20022 credit transfers</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d99be-104">Þetta Leiðbeiningar sýnir hvernig á að setja upp bankareikningsupplýsingar fyrir fyrirtæki sem þarf fyrir myndun greiðsluskrár.</span><span class="sxs-lookup"><span data-stu-id="d99be-104">This procedure shows how to set up company-specific bank account information that is required for payment file generation.</span></span> <span data-ttu-id="d99be-105">Setja upp upplýsingar sem þarf til að mynda ISO 20022 snið fyrir millifærsla fjármuna, en eftir sniðinu gæti þurft frekari upplýsingar, eins og kenni fyrirtækis eða bankaauðkennisnúmer (sort-kóða).</span><span class="sxs-lookup"><span data-stu-id="d99be-105">You set up information required to generate ISO 20022 credit transfer format but depending on the format there might be other information required, such as the Company ID or the Sort code.</span></span> 

<span data-ttu-id="d99be-106">Sýnigögn fyrirtækisins til að stofna þetta ferli er DEMF.</span><span class="sxs-lookup"><span data-stu-id="d99be-106">The demo data company used to create this procedure is DEMF.</span></span>

<span data-ttu-id="d99be-107">Þetta annað ferli af fimm sem sýna greiðsluferlinu lánardrottins með því að nota grunnstillingar fyrir rafræna skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="d99be-107">This is the second procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="d99be-108">Þetta ferli er fyrir eiginleika sem var bætt við í Dynamics 365 for Operations, útgáfu 1611.</span><span class="sxs-lookup"><span data-stu-id="d99be-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="set-up-iban-and-swift-code"></a><span data-ttu-id="d99be-109">Uppsetning IBAN- og swift-kóði</span><span class="sxs-lookup"><span data-stu-id="d99be-109">Set up IBAN and SWIFT code</span></span>
1. <span data-ttu-id="d99be-110">Farið í Reiðufjár- og bankastjórnun > Bankareikningar.</span><span class="sxs-lookup"><span data-stu-id="d99be-110">Go to Cash and bank management > Bank accounts.</span></span>
2. <span data-ttu-id="d99be-111">Nota flýtiafmörkun til að sía í reitnum bankareikningur með gildið „DEMF OPER“.</span><span class="sxs-lookup"><span data-stu-id="d99be-111">Use the Quick Filter to filter on the Bank account field with a value of 'DEMF OPER'.</span></span>
3. <span data-ttu-id="d99be-112">Smellið á DEMF OPER til að opna upplýsingar bankareiknings</span><span class="sxs-lookup"><span data-stu-id="d99be-112">Click DEMF OPER to open bank account details.</span></span>
4. <span data-ttu-id="d99be-113">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="d99be-113">Click Edit.</span></span>
5. <span data-ttu-id="d99be-114">Útvíkka aukakenni hluta.</span><span class="sxs-lookup"><span data-stu-id="d99be-114">Expand the Additional identification section.</span></span>
6. <span data-ttu-id="d99be-115">Í reitinn IBAN skal slá inn 'DE89370400440532013000'.</span><span class="sxs-lookup"><span data-stu-id="d99be-115">In the IBAN field, type 'DE89370400440532013000'.</span></span>
7. <span data-ttu-id="d99be-116">Í svæðinu swift-kóði færðu inn 'DEUTDEFF' .</span><span class="sxs-lookup"><span data-stu-id="d99be-116">In the SWIFT code field, type 'DEUTDEFF'.</span></span>
    * <span data-ttu-id="d99be-117">Athugið að SWIFT\BIC er ekki krafist fyrir margar greiðslusnið hins vegar er mælt með að slíkt sé skráð fyrir bankareikning.</span><span class="sxs-lookup"><span data-stu-id="d99be-117">Note that SWIFT\BIC is not required for many payment formats, however it is recommended to have it registered for a bank account.</span></span>  
8. <span data-ttu-id="d99be-118">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="d99be-118">Click Save.</span></span>

## <a name="set-up-bank-account-for-the-legal-entity"></a><span data-ttu-id="d99be-119">Setja upp bankareikning fyrir lögaðila</span><span class="sxs-lookup"><span data-stu-id="d99be-119">Set up bank account for the legal entity</span></span>
1. <span data-ttu-id="d99be-120">Fara í Fyrirtækisstjórnun > Fyrirtæki > Lögaðilar.</span><span class="sxs-lookup"><span data-stu-id="d99be-120">Go to Organization administration > Organizations > Legal entities.</span></span>
2. <span data-ttu-id="d99be-121">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="d99be-121">Click Edit.</span></span>
3. <span data-ttu-id="d99be-122">Útvíkka hlutann upplýsingar bankareiknings.</span><span class="sxs-lookup"><span data-stu-id="d99be-122">Expand the Bank account information section.</span></span>
4. <span data-ttu-id="d99be-123">Færa inn eða veljið gildi í svæðinu bankareikning.</span><span class="sxs-lookup"><span data-stu-id="d99be-123">In the Bank account field, enter or select a value.</span></span>
5. <span data-ttu-id="d99be-124">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="d99be-124">Click Save.</span></span>

