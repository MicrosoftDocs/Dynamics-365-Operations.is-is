---
title: Setja upp VSK-uppgjörstímabil
description: Þetta efni útskýrir hvernig á að setja upp uppgjörstímabil virðisaukaskatts í Dynamics 365 Finance.
author: twheeloc
ms.date: 08/05/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxPeriod
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fd11068a31b5324d87416e7c00f75a59743f695a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813508"
---
# <a name="set-up-sales-tax-settlement-periods"></a><span data-ttu-id="6babb-103">Setja upp VSK-uppgjörstímabil</span><span class="sxs-lookup"><span data-stu-id="6babb-103">Set up sales tax settlement periods</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6babb-104">Þetta efni útskýrir hvernig á að setja upp uppgjörstímabil virðisaukaskatts.</span><span class="sxs-lookup"><span data-stu-id="6babb-104">This topic explains how to set up sales tax settlement periods.</span></span> <span data-ttu-id="6babb-105">Virðisaukaskattsuppgjörstímabil innihalda upplýsingar um tímabil fyrir hvaða virðisaukaskatt þarf að vera tilkynntur og greiddur.</span><span class="sxs-lookup"><span data-stu-id="6babb-105">Sales tax settlement periods contain information about the period intervals for which sales tax needs to be reported and paid.</span></span> <span data-ttu-id="6babb-106">Hægt er að keyra jöfnunarferli fyrir jöfnunartímabil fyrir tiltekin dagsetningarbil.</span><span class="sxs-lookup"><span data-stu-id="6babb-106">A settlement process can be run for a settlement period for a specific date interval.</span></span> <span data-ttu-id="6babb-107">Allar skattkóði sem tengist jöfnunartímabil verða jafnaðar.</span><span class="sxs-lookup"><span data-stu-id="6babb-107">All tax codes associated with the settlement period will be settled.</span></span> <span data-ttu-id="6babb-108">Eftir að setja upp tengd virðisaukaskattsyfirvald er skattskuld bókuð í annað hvort lánardrottinn eða fjárhagslykil.</span><span class="sxs-lookup"><span data-stu-id="6babb-108">Depending on the set up of the related Sales tax authority, the tax liability is posted either to a vendor or a General ledger account.</span></span>

<span data-ttu-id="6babb-109">Þetta verkefni notar USMF-sýnifyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="6babb-109">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="6babb-110">Í skoðunarrúðunni ferðu í **Kerfiseiningar > Skattur > Óbeinir skattar > Virðisaukaskattur- > VSK-uppgjörstímabil**.</span><span class="sxs-lookup"><span data-stu-id="6babb-110">In the navigation pane, go to **Modules > Tax > Indirect taxes > Sales tax > Sales tax settlement periods**.</span></span>
2. <span data-ttu-id="6babb-111">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="6babb-111">Select **New**.</span></span>
3. <span data-ttu-id="6babb-112">Í reitinn **Uppgjörstímabil** skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="6babb-112">In the **Settlement period** field, type a value.</span></span>
4. <span data-ttu-id="6babb-113">Í reitinn **Lýsing** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="6babb-113">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="6babb-114">Í reitnum **Yfirvöld** velurðu virðisaukaskattsyfirvald sem tekur við skýrslan og greiðsla sem eru stofnaðar fyrir jöfnunartímabil.</span><span class="sxs-lookup"><span data-stu-id="6babb-114">In the **Authority** field, select the sales tax authority that receives the reports and the payments that are created for the settlement period.</span></span>
6. <span data-ttu-id="6babb-115">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="6babb-115">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="6babb-116">Í reitnum **Greiðsluskilmálar** velurðu skrána sem óskað er eftir af fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="6babb-116">In the **Terms of payment** field, select the desired record in the drop-down menu.</span></span> <span data-ttu-id="6babb-117">Tengdar virðisaukaskattsyfirvald má setja upp sem lánardrottinn og virðisaukauppgjör mun stofna opnum lánardrottnareikningi.</span><span class="sxs-lookup"><span data-stu-id="6babb-117">The related Sales tax authority can be set up as a vendor and the Sales tax settlement will create an open vendor invoice.</span></span> <span data-ttu-id="6babb-118">Greiðsluskilmálar skilgreina Gjalddaga fyrir the opinn reikningur lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="6babb-118">The Terms of payment defines the Due date for the open vendor invoice.</span></span>  
8. <span data-ttu-id="6babb-119">Velja gerð fyrir tímabilum jöfnunartímabils.</span><span class="sxs-lookup"><span data-stu-id="6babb-119">Select a type for the settlement period intervals.</span></span>
9. <span data-ttu-id="6babb-120">Færið inn fjölda eininga fyrir tímabilið á hvert tímabil.</span><span class="sxs-lookup"><span data-stu-id="6babb-120">Enter the number of Period interval units per period.</span></span> <span data-ttu-id="6babb-121">Til dæmis ársfjórðungur hefur 3 mánuði.</span><span class="sxs-lookup"><span data-stu-id="6babb-121">For example, a quarter has 3 months.</span></span>
10. <span data-ttu-id="6babb-122">Velja eða hreinsa gátreitinn **Nota runuvinnslu fyrir virðisaukauppgjör**.</span><span class="sxs-lookup"><span data-stu-id="6babb-122">Select or clear the **Use batch processing for sales tax settlement** check box.</span></span> <span data-ttu-id="6babb-123">Hægt er að vinna úr jöfnunarferlið fyrir tímabil sem runuvinnslu í bakgrunni.</span><span class="sxs-lookup"><span data-stu-id="6babb-123">The settlement process for the settlement period can be processed as batch job in the background.</span></span> <span data-ttu-id="6babb-124">Þetta er ráðlagt fyrir mikinn fjölda skattafærslur innan tímabil.</span><span class="sxs-lookup"><span data-stu-id="6babb-124">This is recommended for a large number of tax transactions within a period interval.</span></span>  
    > [!NOTE]
    > <span data-ttu-id="6babb-125">Sem stendur er ekki stutt á Spáni, Japan og Hollandi.</span><span class="sxs-lookup"><span data-stu-id="6babb-125">Currently this is not supported in Spain, Japan, and the Netherlands.</span></span>
11. <span data-ttu-id="6babb-126">Veldu eða hreinsaðu gátreitinn **Koma í veg fyrir að mótfærsluskattafærslur myndist**.</span><span class="sxs-lookup"><span data-stu-id="6babb-126">Select or clear the **Prevent generating offset tax transactions** check box.</span></span> <span data-ttu-id="6babb-127">Sjálfgefið framleiðir kerfið upp á mótfærsluskattafærslur við uppgjörsferlið, sem getur valdið frammistöðuvandamálum ef fjöldi skattafærslna er innan tímabils.</span><span class="sxs-lookup"><span data-stu-id="6babb-127">By default, the system generates offset tax transactions during the settlement process, which cause can performance issue if there are a large number of tax transactions within a period interval.</span></span> <span data-ttu-id="6babb-128">Veljið þennan gátreit til að koma í veg fyrir að mótfærsluskattafærslur myndist.</span><span class="sxs-lookup"><span data-stu-id="6babb-128">Select this check box to prevent generating offset tax transactions.</span></span>
12. <span data-ttu-id="6babb-129">Útvíkkaðu flipann **Tímabil**.</span><span class="sxs-lookup"><span data-stu-id="6babb-129">Expand the **Period intervals** tab.</span></span>
13. <span data-ttu-id="6babb-130">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="6babb-130">Select **Add**.</span></span>
14. <span data-ttu-id="6babb-131">Í reitnum **Frá dags.** skal færa inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="6babb-131">In the **From date** field in the new row, enter a date.</span></span>
15. <span data-ttu-id="6babb-132">Í reitnum **Til dags.** færirðu inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="6babb-132">In the **To date** field, enter a date.</span></span>
16. <span data-ttu-id="6babb-133">Veldu **Nýtt afmörkunartímabil**.</span><span class="sxs-lookup"><span data-stu-id="6babb-133">Select **New period interval**.</span></span> <span data-ttu-id="6babb-134">Þegar hefur verið fært inn fyrsta tímabilið, hægt að stofna ný tímabil sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="6babb-134">Once the first period interval has been entered, new periods can be created automatically.</span></span> <span data-ttu-id="6babb-135">Hægt er að koma aftur og bæta við nýrri tímabilum eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="6babb-135">You can come back and add new period intervals as required.</span></span>  
17. <span data-ttu-id="6babb-136">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="6babb-136">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]