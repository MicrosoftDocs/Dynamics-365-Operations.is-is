---
title: Setja upp bankareikninga fyrirtækis fyrir ISO20022-beingreiðslur
description: Þetta Leiðbeiningar sýnir hvernig á að setja upp og bankareikningsupplýsingar fyrir fyrirtæki sem þarf fyrir myndun greiðsluskrár viðskiptavina.
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
ms.openlocfilehash: b0faa23193111ed771ccc3a5c7f99ca908a036e9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4988137"
---
# <a name="set-up-company-bank-accounts-for-iso20022-direct-debits"></a><span data-ttu-id="8cd9a-103">Setja upp bankareikninga fyrirtækis fyrir ISO20022-beingreiðslur</span><span class="sxs-lookup"><span data-stu-id="8cd9a-103">Set up company bank accounts for ISO20022 direct debits</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8cd9a-104">Þetta Leiðbeiningar sýnir hvernig á að setja upp og bankareikningsupplýsingar fyrir fyrirtæki sem þarf fyrir myndun greiðsluskrár viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="8cd9a-104">This task walks you through setting up the company specific bank account information that is required for generating customer payment files.</span></span> <span data-ttu-id="8cd9a-105">Þessi aðferð notar snið ISO-20022 beingreiðslu sem dæmi.</span><span class="sxs-lookup"><span data-stu-id="8cd9a-105">This procedure uses the ISO 20022 direct debit format as an example.</span></span> <span data-ttu-id="8cd9a-106">Aðrar snið útheimt kannski auka upplýsinga vegna uppsetningar eins og kenni fyrirtækis eða bankaauðkennisnúmer (Sort-kóða).</span><span class="sxs-lookup"><span data-stu-id="8cd9a-106">Other formats might require additional setup information like the Company ID or the Sort code.</span></span>



<span data-ttu-id="8cd9a-107">Þetta verkefni var stofnuð með því að nota sýnigögn fyrirtækisins DEMF.</span><span class="sxs-lookup"><span data-stu-id="8cd9a-107">This task was created using the demo data company DEMF.</span></span>



<span data-ttu-id="8cd9a-108">Þetta er annað af fimm ferlum sem lýsa greiðsluferlinu viðskiptavinar með grunnstillingar fyrir rafræna skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="8cd9a-108">This is the second of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>


## <a name="set-up-the-iban-and-swift-codes"></a><span data-ttu-id="8cd9a-109">Setja upp IBAN- og swift-kóða</span><span class="sxs-lookup"><span data-stu-id="8cd9a-109">Set up the IBAN and SWIFT codes</span></span>
1. <span data-ttu-id="8cd9a-110">Farið í Reiðufjár- og bankastjórnun > Bankareikningar.</span><span class="sxs-lookup"><span data-stu-id="8cd9a-110">Go to Cash and bank management > Bank accounts.</span></span>
2. <span data-ttu-id="8cd9a-111">Nota flýtiafmörkun til að sía í reitnum bankareikningur með gildið „DEMF OPER“.</span><span class="sxs-lookup"><span data-stu-id="8cd9a-111">Use the Quick Filter to filter on the Bank account field with a value of 'DEMF OPER'.</span></span>
3. <span data-ttu-id="8cd9a-112">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="8cd9a-112">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="8cd9a-113">Til dæmis: smellið á "DEMF OPER' til að opna upplýsingar um bankareikning.</span><span class="sxs-lookup"><span data-stu-id="8cd9a-113">For example, click 'DEMF OPER' to open the bank account details.</span></span>  
4. <span data-ttu-id="8cd9a-114">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="8cd9a-114">Click Edit.</span></span>
5. <span data-ttu-id="8cd9a-115">Útvíkka eða draga saman aukakenni hluta.</span><span class="sxs-lookup"><span data-stu-id="8cd9a-115">Expand or collapse the Additional identification section.</span></span>
6. <span data-ttu-id="8cd9a-116">Í reitinn IBAN skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="8cd9a-116">In the IBAN field, type a value.</span></span>
    * <span data-ttu-id="8cd9a-117">Til dæmis færðu inn 'DE89370400440532013000'.</span><span class="sxs-lookup"><span data-stu-id="8cd9a-117">For example, enter 'DE89370400440532013000'.</span></span>  
7. <span data-ttu-id="8cd9a-118">Í svæðinu SWIFT-kóði færðu inn gildi.</span><span class="sxs-lookup"><span data-stu-id="8cd9a-118">In the SWIFT code field, type a value.</span></span>
    * <span data-ttu-id="8cd9a-119">Til dæmis færðu inn 'DEUTDEFF'.</span><span class="sxs-lookup"><span data-stu-id="8cd9a-119">For example, enter 'DEUTDEFF'.</span></span>    <span data-ttu-id="8cd9a-120">Vinsamlegast Athugið að SWIFT\BIC er ekki krafist fyrir margar greiðslusnið hins vegar er mælt með að slíkt sé skráð fyrir bankareikning.</span><span class="sxs-lookup"><span data-stu-id="8cd9a-120">Please note that SWIFT \ BIC is not mandatory for many payment formats however it is recommended to have it registered for a bank account.</span></span>  
8. <span data-ttu-id="8cd9a-121">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="8cd9a-121">Click Save.</span></span>

## <a name="set-up-a-bank-account-for-the-legal-entity"></a><span data-ttu-id="8cd9a-122">Setja upp bankareikning fyrir lögaðila</span><span class="sxs-lookup"><span data-stu-id="8cd9a-122">Set up a bank account for the legal entity</span></span>
1. <span data-ttu-id="8cd9a-123">Fara í Fyrirtækisstjórnun > Fyrirtæki > Lögaðilar.</span><span class="sxs-lookup"><span data-stu-id="8cd9a-123">Go to Organization administration > Organizations > Legal entities.</span></span>
2. <span data-ttu-id="8cd9a-124">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="8cd9a-124">Click Edit.</span></span>
3. <span data-ttu-id="8cd9a-125">Útvíkka eða draga saman hluta upplýsingar bankareiknings.</span><span class="sxs-lookup"><span data-stu-id="8cd9a-125">Expand or collapse the Bank account information section.</span></span>
4. <span data-ttu-id="8cd9a-126">Í reitnum Bankareikningur skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="8cd9a-126">In the Bank account field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="8cd9a-127">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="8cd9a-127">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="8cd9a-128">Til dæmis: Velja bankareikning "DEMF OPER".</span><span class="sxs-lookup"><span data-stu-id="8cd9a-128">For example, select the "DEMF OPER" bank account.</span></span>  
6. <span data-ttu-id="8cd9a-129">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="8cd9a-129">Click Save.</span></span>

