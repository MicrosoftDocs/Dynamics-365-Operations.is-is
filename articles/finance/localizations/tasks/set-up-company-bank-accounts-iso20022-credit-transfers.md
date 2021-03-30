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
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5ad1ebbea9bca41f43f3f4098114116e32f8517b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5205471"
---
# <a name="set-up-company-bank-accounts-for-iso20022-credit-transfers"></a><span data-ttu-id="0b9e6-103">Setja upp bankareikninga fyrirtækis fyrir ISO20022-kreditfærslur</span><span class="sxs-lookup"><span data-stu-id="0b9e6-103">Set up company bank accounts for ISO20022 credit transfers</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0b9e6-104">Þetta Leiðbeiningar sýnir hvernig á að setja upp bankareikningsupplýsingar fyrir fyrirtæki sem þarf fyrir myndun greiðsluskrár.</span><span class="sxs-lookup"><span data-stu-id="0b9e6-104">This procedure shows how to set up company-specific bank account information that is required for payment file generation.</span></span> <span data-ttu-id="0b9e6-105">Setja upp upplýsingar sem þarf til að mynda ISO 20022 snið fyrir millifærsla fjármuna, en eftir sniðinu gæti þurft frekari upplýsingar, eins og kenni fyrirtækis eða bankaauðkennisnúmer (sort-kóða).</span><span class="sxs-lookup"><span data-stu-id="0b9e6-105">You set up information required to generate ISO 20022 credit transfer format but depending on the format there might be other information required, such as the Company ID or the Sort code.</span></span> 

<span data-ttu-id="0b9e6-106">Sýnigögn fyrirtækisins til að stofna þetta ferli er DEMF.</span><span class="sxs-lookup"><span data-stu-id="0b9e6-106">The demo data company used to create this procedure is DEMF.</span></span>

<span data-ttu-id="0b9e6-107">Þetta annað ferli af fimm sem sýna greiðsluferlinu lánardrottins með því að nota grunnstillingar fyrir rafræna skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="0b9e6-107">This is the second procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="0b9e6-108">Þetta ferli er fyrir eiginleika sem var bætt við í Dynamics 365 for Operations, útgáfu 1611.</span><span class="sxs-lookup"><span data-stu-id="0b9e6-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="set-up-iban-and-swift-code"></a><span data-ttu-id="0b9e6-109">Uppsetning IBAN- og swift-kóði</span><span class="sxs-lookup"><span data-stu-id="0b9e6-109">Set up IBAN and SWIFT code</span></span>
1. <span data-ttu-id="0b9e6-110">Farið í Reiðufjár- og bankastjórnun > Bankareikningar.</span><span class="sxs-lookup"><span data-stu-id="0b9e6-110">Go to Cash and bank management > Bank accounts.</span></span>
2. <span data-ttu-id="0b9e6-111">Nota flýtiafmörkun til að sía í reitnum bankareikningur með gildið „DEMF OPER“.</span><span class="sxs-lookup"><span data-stu-id="0b9e6-111">Use the Quick Filter to filter on the Bank account field with a value of 'DEMF OPER'.</span></span>
3. <span data-ttu-id="0b9e6-112">Smellið á DEMF OPER til að opna upplýsingar bankareiknings</span><span class="sxs-lookup"><span data-stu-id="0b9e6-112">Click DEMF OPER to open bank account details.</span></span>
4. <span data-ttu-id="0b9e6-113">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="0b9e6-113">Click Edit.</span></span>
5. <span data-ttu-id="0b9e6-114">Útvíkka aukakenni hluta.</span><span class="sxs-lookup"><span data-stu-id="0b9e6-114">Expand the Additional identification section.</span></span>
6. <span data-ttu-id="0b9e6-115">Í reitinn IBAN skal slá inn 'DE89370400440532013000'.</span><span class="sxs-lookup"><span data-stu-id="0b9e6-115">In the IBAN field, type 'DE89370400440532013000'.</span></span>
7. <span data-ttu-id="0b9e6-116">Í svæðinu swift-kóði færðu inn 'DEUTDEFF' .</span><span class="sxs-lookup"><span data-stu-id="0b9e6-116">In the SWIFT code field, type 'DEUTDEFF'.</span></span>
    * <span data-ttu-id="0b9e6-117">Athugið að SWIFT\BIC er ekki krafist fyrir margar greiðslusnið hins vegar er mælt með að slíkt sé skráð fyrir bankareikning.</span><span class="sxs-lookup"><span data-stu-id="0b9e6-117">Note that SWIFT\BIC is not required for many payment formats, however it is recommended to have it registered for a bank account.</span></span>  
8. <span data-ttu-id="0b9e6-118">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="0b9e6-118">Click Save.</span></span>

## <a name="set-up-bank-account-for-the-legal-entity"></a><span data-ttu-id="0b9e6-119">Setja upp bankareikning fyrir lögaðila</span><span class="sxs-lookup"><span data-stu-id="0b9e6-119">Set up bank account for the legal entity</span></span>
1. <span data-ttu-id="0b9e6-120">Fara í Fyrirtækisstjórnun > Fyrirtæki > Lögaðilar.</span><span class="sxs-lookup"><span data-stu-id="0b9e6-120">Go to Organization administration > Organizations > Legal entities.</span></span>
2. <span data-ttu-id="0b9e6-121">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="0b9e6-121">Click Edit.</span></span>
3. <span data-ttu-id="0b9e6-122">Útvíkka hlutann upplýsingar bankareiknings.</span><span class="sxs-lookup"><span data-stu-id="0b9e6-122">Expand the Bank account information section.</span></span>
4. <span data-ttu-id="0b9e6-123">Færa inn eða veljið gildi í svæðinu bankareikning.</span><span class="sxs-lookup"><span data-stu-id="0b9e6-123">In the Bank account field, enter or select a value.</span></span>
5. <span data-ttu-id="0b9e6-124">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="0b9e6-124">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]