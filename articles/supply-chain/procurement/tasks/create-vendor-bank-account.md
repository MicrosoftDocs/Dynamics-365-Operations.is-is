---
title: Stofna bankareikning lánardrottins
description: Þessi verklýsing sýnir hvernig á að stofna bankareikning fyrir lánardrottinn.
author: RichardLuan
manager: tfehr
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts, LogisticsPostalAddressSingle
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f3523dec15363bd42219d40ed8048681c56829ac
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/16/2021
ms.locfileid: "5019254"
---
# <a name="create-a-vendor-bank-account"></a><span data-ttu-id="9661c-103">Stofna bankareikning lánardrottins</span><span class="sxs-lookup"><span data-stu-id="9661c-103">Create a vendor bank account</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9661c-104">Þessi verklýsing sýnir hvernig á að stofna bankareikning fyrir lánardrottinn.</span><span class="sxs-lookup"><span data-stu-id="9661c-104">This procedure shows you how to create a bank account for a vendor.</span></span> <span data-ttu-id="9661c-105">Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF.</span><span class="sxs-lookup"><span data-stu-id="9661c-105">You can use this procedure in demo data company USMF.</span></span>

1. <span data-ttu-id="9661c-106">Farði í **Skoðunarrúðuna > Kerfiseiningar > Innkaup og aðföng > Lánardrottnar > Allir lánardrottnar**.</span><span class="sxs-lookup"><span data-stu-id="9661c-106">Go to **Navigation pane > Modules > Procurement and sourcing > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="9661c-107">Veljið lánardrottinn sem á að stofna bankareikning fyrir, og smellið síðan á tengil í reitnum **Kenni lánardrottnalykils**.</span><span class="sxs-lookup"><span data-stu-id="9661c-107">Select the vendor that you want to create a bank account for, and then click the link on the **Vendor account ID** field.</span></span>
3. <span data-ttu-id="9661c-108">Á **Aðgerðasvæði** er smellt á **Lánardrottinn**.</span><span class="sxs-lookup"><span data-stu-id="9661c-108">On the **Action Pane**, click **Vendor**.</span></span>
4. <span data-ttu-id="9661c-109">Smelltu á **Bankareikninga**.</span><span class="sxs-lookup"><span data-stu-id="9661c-109">Click **Bank accounts**.</span></span>
5. <span data-ttu-id="9661c-110">Í **aðgerðasvæðinu** er smellt á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="9661c-110">On the **Action Pane**, click **New**.</span></span>
6. <span data-ttu-id="9661c-111">Í reitinn **Bankareikningar** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="9661c-111">In the **Bank account** field, type a value.</span></span> <span data-ttu-id="9661c-112">Þetta Kenni verður notuð til að auðkenna bankareikninginn á lánardrottinsfærslu.</span><span class="sxs-lookup"><span data-stu-id="9661c-112">This ID will be used to identify the bank account on the vendor record.</span></span>  
7. <span data-ttu-id="9661c-113">Í reitinn **Heiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="9661c-113">In the **Name** field, type a value.</span></span>
8. <span data-ttu-id="9661c-114">Í reitnum **Bankaflokkur** skal rita eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="9661c-114">In the **Bank groups** field, enter or select a value.</span></span>
9. <span data-ttu-id="9661c-115">Í reitnum **Gerð leiðarnúmer** skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="9661c-115">In the **Routing number type** field, select an option.</span></span> <span data-ttu-id="9661c-116">Þetta er gerð leiðarnúmers sem er notuð fyrir alþjóðlegar greiðslur.</span><span class="sxs-lookup"><span data-stu-id="9661c-116">This is the type of routing number that's used for international payments.</span></span>  
10. <span data-ttu-id="9661c-117">Í reitinn **Bankareikningsnúmer** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="9661c-117">In the **Bank account number** field, type a value.</span></span>
11. <span data-ttu-id="9661c-118">Í reitinn **SWIFT-kóði** skal rita gildi.</span><span class="sxs-lookup"><span data-stu-id="9661c-118">In the **SWIFT code** field, type a value.</span></span>
12. <span data-ttu-id="9661c-119">Í reitinn **IBAN** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="9661c-119">In the **IBAN** field, type a value.</span></span>
    - <span data-ttu-id="9661c-120">Iban-númeri verður að vera á réttu sniði.</span><span class="sxs-lookup"><span data-stu-id="9661c-120">The IBAN number must be in the correct format.</span></span> <span data-ttu-id="9661c-121">Til dæmis er hægt að nota DE89370400440532013000.</span><span class="sxs-lookup"><span data-stu-id="9661c-121">For example, you could use DE89370400440532013000.</span></span>  
    - <span data-ttu-id="9661c-122">Staða bankareikningsins er Virkur ef Virkri dagsetningu hefur verið náð og lokadagur er ekki liðinn.</span><span class="sxs-lookup"><span data-stu-id="9661c-122">The status of the bank account is Active if the Active date has been reached, and the Expiration date has not been exceeded.</span></span> <span data-ttu-id="9661c-123">Hún er einnig virk ef reitirnir Virk dagsetning og Gildistími eru auðir.</span><span class="sxs-lookup"><span data-stu-id="9661c-123">It's also active if both the Active date and Expiration date fields are blank.</span></span> <span data-ttu-id="9661c-124">Ef dagsetningarnar í svæðunum Virk dagsetning og Lokadagur eru báðar í framtíðinni er ekki hægt að gera rafrænar greiðslur.</span><span class="sxs-lookup"><span data-stu-id="9661c-124">If the dates in both the Active date and Expiration date fields are in the future electronic payments are not available.</span></span> <span data-ttu-id="9661c-125">Aðrar greiðslugerðir eru mögulegar og bankareikningurinn er virkur.</span><span class="sxs-lookup"><span data-stu-id="9661c-125">Other payment types are available and the bank account is active.</span></span>  
13. <span data-ttu-id="9661c-126">Útvíkkaðu kaflann **Uppsetning**.</span><span class="sxs-lookup"><span data-stu-id="9661c-126">Expand the **Setup** section.</span></span>
14. <span data-ttu-id="9661c-127">Í reitinn **Textakóði** skal rita gildi.</span><span class="sxs-lookup"><span data-stu-id="9661c-127">In the **Text code** field, type a value.</span></span> <span data-ttu-id="9661c-128">Þetta svæði tilgreinir kóða sem mun birtast á bankayfirliti viðtakanda.</span><span class="sxs-lookup"><span data-stu-id="9661c-128">This field specifies a code that will appear on the bank statement of the recipient.</span></span>  
15. <span data-ttu-id="9661c-129">Í reitinn **Skilaboð til banka** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="9661c-129">In the **Message to bank** field, type a value.</span></span>
16. <span data-ttu-id="9661c-130">Í reitinn **Gengistilvísun** skal rita gildi.</span><span class="sxs-lookup"><span data-stu-id="9661c-130">In the **Exchange reference** field, type a value.</span></span> <span data-ttu-id="9661c-131">Þetta er Tilvísunarnúmer fyrir hvers kyns framvirkt eða fast gengi.</span><span class="sxs-lookup"><span data-stu-id="9661c-131">This is the reference number for any forward-term or fixed-term rate of exchange.</span></span>
17. <span data-ttu-id="9661c-132">Í reitinn **Gjaldmiðill** skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="9661c-132">In the **Currency** field, enter or select a value.</span></span> <span data-ttu-id="9661c-133">Þegar fyrirframkvittanir eru gefin út, gefur þessa kafla yfirlit yfir stöðu þeirra (í bið eða samþykkt).</span><span class="sxs-lookup"><span data-stu-id="9661c-133">When prenotes are issued, this section provides an overview of their status (pending or approved).</span></span>  
18. <span data-ttu-id="9661c-134">Útvíkkaðu kaflann **Aðsetur**.</span><span class="sxs-lookup"><span data-stu-id="9661c-134">Expand the **Address** section.</span></span>
19. <span data-ttu-id="9661c-135">Útvíkkaðu kaflann **Fyrirframkvittanir**.</span><span class="sxs-lookup"><span data-stu-id="9661c-135">Expand the **Prenotes** section.</span></span>
20. <span data-ttu-id="9661c-136">Útvíkkaðu kaflann **Tengslaupplýsingar**.</span><span class="sxs-lookup"><span data-stu-id="9661c-136">Expand the **Contact information** section.</span></span>
21. <span data-ttu-id="9661c-137">Í reitinn **Símanúmer** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="9661c-137">In the **Telephone** field, type a value.</span></span>
22. <span data-ttu-id="9661c-138">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="9661c-138">Close the page.</span></span>
23. <span data-ttu-id="9661c-139">Smellið á **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="9661c-139">Click **Edit**.</span></span>
24. <span data-ttu-id="9661c-140">Útvíkkaðu kaflann **Greiðslur**.</span><span class="sxs-lookup"><span data-stu-id="9661c-140">Expand the **Payment** section.</span></span>
25. <span data-ttu-id="9661c-141">Í reitnum **Bankareikningur** skal velja lykil sem var nýlega stofnaður.</span><span class="sxs-lookup"><span data-stu-id="9661c-141">In the **Bank account** field, select the account that you've just created.</span></span>
26. <span data-ttu-id="9661c-142">Smellt er á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="9661c-142">Click **Save**.</span></span> <span data-ttu-id="9661c-143">Aðsetrið má erfa frá bankaflokki, ef slíkt er tilgreint, eða hægt er að bæta honum við hér.</span><span class="sxs-lookup"><span data-stu-id="9661c-143">The address may be inherited from the bank group, if one is specified, or you can add it here.</span></span>  

