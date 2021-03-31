---
title: Setja upp greiðslumáta fyrir viðskiptavin
description: Þetta efni útskýrir hvernig á að stofna greiðslumáta fyrir greiðslur viðskiptavina.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPaymMode, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7e60459c417c6018c4088009a323cf7f66616ef4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5220204"
---
# <a name="establish-customer-method-of-payment"></a><span data-ttu-id="cda4c-103">Setja upp greiðslumáta fyrir viðskiptavin</span><span class="sxs-lookup"><span data-stu-id="cda4c-103">Establish customer method of payment</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cda4c-104">Þetta efni útskýrir hvernig á að stofna greiðslumáta fyrir greiðslur viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="cda4c-104">This topic explains how to create a method of payment for customer payments.</span></span> <span data-ttu-id="cda4c-105">Þetta verkefni notar USMF-sýnifyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="cda4c-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="cda4c-106">Í skoðunarrúðunni ferðu í **Kerfi > Viðskiptakröfur > Greiðsluuppsetning > Greiðsluhættir**.</span><span class="sxs-lookup"><span data-stu-id="cda4c-106">In the navigation pane, go to **Modules > Accounts receivable > Payments setup > Methods of payment**.</span></span>
2. <span data-ttu-id="cda4c-107">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="cda4c-107">Select **New**.</span></span>
3. <span data-ttu-id="cda4c-108">Í svæðinu **Greiðslumáti** skal færa inn kenni fyrir greiðsluaðferð.</span><span class="sxs-lookup"><span data-stu-id="cda4c-108">In the **Method of payment** field, enter an ID for the method of payment.</span></span> <span data-ttu-id="cda4c-109">Kenni greiðsluaðferðar er sýnt á reikninga og greiðslur, svo gera skal nægjanlega lýsandi til að skilja hvaða gerð af greiðslu er skráð og fyrir hvaða bankareikning.</span><span class="sxs-lookup"><span data-stu-id="cda4c-109">The Method of payment ID is shown on invoices and payments, so make it descriptive enough to understand what type of payment is being recorded, and for what bank account.</span></span>  
4. <span data-ttu-id="cda4c-110">Í reitnum **Lýsing** skal færa inn lýsingu.</span><span class="sxs-lookup"><span data-stu-id="cda4c-110">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="cda4c-111">Veljið hvaða staða greiðslu er nauðsynlegt í til að bóka greiðslur.</span><span class="sxs-lookup"><span data-stu-id="cda4c-111">Select what payment status is required in order for payments to be posted.</span></span> <span data-ttu-id="cda4c-112">Þegar greiðsla viðskiptavinar er stofnuð, það er aðeins hægt að bóka þegar greiðslustöðu samræmist greiðslustöðu sem skilgreind hér.</span><span class="sxs-lookup"><span data-stu-id="cda4c-112">When creating a customer payment, it can only be posted when the payment status matches the payment status you define here.</span></span>  
6. <span data-ttu-id="cda4c-113">Veljið hvernig á að stofna greiðslur viðskiptavina fyrir reikninga.</span><span class="sxs-lookup"><span data-stu-id="cda4c-113">Select how customers payments should be created for invoices.</span></span> <span data-ttu-id="cda4c-114">Þessi valkostur er aðeins notað þegar greiðslutillaga er keyrð.</span><span class="sxs-lookup"><span data-stu-id="cda4c-114">This option is only used when running a payment proposal.</span></span> <span data-ttu-id="cda4c-115">Hægt væri að nota greiðslutillögu fyrir greiðslur viðskiptavinar þegar gerð er beingreiðsla, og fjármagn tekið af bankareikningum viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="cda4c-115">A payment proposal could be used for customer payments when doing direct debits, and pulling the funds from the customers' bank accounts.</span></span>  
7. <span data-ttu-id="cda4c-116">Veljið greiðslugerð</span><span class="sxs-lookup"><span data-stu-id="cda4c-116">Select the type of payment.</span></span> <span data-ttu-id="cda4c-117">Greiðslugerð hjálpar til við ákvarða hvort einhverjar villuleit á sér stað eða ekki á greiðsluna.</span><span class="sxs-lookup"><span data-stu-id="cda4c-117">The payment type will help determine whether some validation will occur or not on the payment.</span></span>  
8. <span data-ttu-id="cda4c-118">Velja hvað greiðslur gerð lykils verður bókað til.</span><span class="sxs-lookup"><span data-stu-id="cda4c-118">Select what account type payments will post to.</span></span> <span data-ttu-id="cda4c-119">Venjulega yrði Banki valinn fyrir þennan valmöguleika.</span><span class="sxs-lookup"><span data-stu-id="cda4c-119">Typically, Bank would be selected for this option.</span></span>  
9. <span data-ttu-id="cda4c-120">Veljið bankareikninginn sem verður að skrá þessa greiðslu.</span><span class="sxs-lookup"><span data-stu-id="cda4c-120">Select the bank account into which this payment will be recorded.</span></span>
10. <span data-ttu-id="cda4c-121">Færa inn bankafærslugerð til að auðkenna gerð greiðslunnar sem er notað af bankanum.</span><span class="sxs-lookup"><span data-stu-id="cda4c-121">Enter the Bank transaction type to identify the type of payment used by your bank.</span></span> <span data-ttu-id="cda4c-122">Færslugerð banka er notaður við ferlið afstemmingu banka og getur auðvelda afstemmingu.</span><span class="sxs-lookup"><span data-stu-id="cda4c-122">The bank transaction type is used during the bank reconciliation process, and can make reconciliation easier.</span></span>  
11. <span data-ttu-id="cda4c-123">Velja hvort þessi greiðslu tímabundið bókuð á millilykil.</span><span class="sxs-lookup"><span data-stu-id="cda4c-123">Select whether this payment will temporarily post to a bridging account.</span></span> <span data-ttu-id="cda4c-124">Ef óskað er að reyna fljótandi tíma fyrir greiðslu til að hreinsa banka, nota milliaðgerðir.</span><span class="sxs-lookup"><span data-stu-id="cda4c-124">If you want to try the float time for a payment to clear the bank, use the Bridging functionality.</span></span> <span data-ttu-id="cda4c-125">Greiðslan bókar tímabundið fjárhagslykil þar til hún hreinsar banka, og greiðsla færist á bankareikning sem er skilgreindur hér.</span><span class="sxs-lookup"><span data-stu-id="cda4c-125">The payment will temporarily post to a Ledger account until it clears the bank, at which time the payment will move to the bank account you defined here.</span></span>  
12. <span data-ttu-id="cda4c-126">Færið inn aðallykilinn notað fyrir millibókun.</span><span class="sxs-lookup"><span data-stu-id="cda4c-126">Enter the main account used for the bridging posting.</span></span> <span data-ttu-id="cda4c-127">Þetta er aðallykill sem greiðslan verður tímabundið bókuð í ef notuð er milliaðgerð.</span><span class="sxs-lookup"><span data-stu-id="cda4c-127">This is the main account to which the payment will temporarily post if using bridging.</span></span>  
13. <span data-ttu-id="cda4c-128">Notið flipann **Skráarsnið** til að skilgreina stillingar fyrir rafrænar greiðslur.</span><span class="sxs-lookup"><span data-stu-id="cda4c-128">Use the **File format** tab to define setting for electronic payments.</span></span>
14. <span data-ttu-id="cda4c-129">Notið flipann **Greiðslueftirlit** til að skilgreina svæðin sem eru skylda.</span><span class="sxs-lookup"><span data-stu-id="cda4c-129">Use the **Payment control** tab to define fields that are mandatory.</span></span> <span data-ttu-id="cda4c-130">Til dæmis, ef þess er krafist allar greiðslur með þessari greiðsluaðferð til að vera lagðar inn, hægt er að velja valkostinn á þessum flipa.</span><span class="sxs-lookup"><span data-stu-id="cda4c-130">For example, if you require all payments with this method of payment to be deposited, you can choose that option on this tab.</span></span>  
15. <span data-ttu-id="cda4c-131">Notið flipann **Greiðslueigindir** til að tilgreina greiðslueigindir sem á að nota fyrir þennan greiðslumáta.</span><span class="sxs-lookup"><span data-stu-id="cda4c-131">Use the **Payment attributes** tab to define which payment attributes you want to use for this method of payment.</span></span>
16. <span data-ttu-id="cda4c-132">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="cda4c-132">Select **Save**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]