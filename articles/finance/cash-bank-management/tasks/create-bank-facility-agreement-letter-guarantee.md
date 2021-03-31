---
title: Stofna bankaaðstöðusamninga fyrir ábyrgðaryfirlýsingu
description: Þetta verk stofnar bankaaðstöðusamning til að vinna ábyrgðarbréf.
author: panolte
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b9c93a76bc7e29cb98834b9028748330710a4cef
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5225465"
---
# <a name="create-a-bank-facility-agreement-for-the-letter-of-guarantee"></a><span data-ttu-id="e3055-103">Stofna bankaaðstöðusamninga fyrir ábyrgðaryfirlýsingu</span><span class="sxs-lookup"><span data-stu-id="e3055-103">Create a bank facility agreement for the letter of guarantee</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e3055-104">Þetta verk stofnar bankaaðstöðusamning til að vinna ábyrgðarbréf.</span><span class="sxs-lookup"><span data-stu-id="e3055-104">This task creates a bank facility agreement to process a letter of guarantee.</span></span> <span data-ttu-id="e3055-105">Þetta verkefni notar USMF-sýnifyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="e3055-105">This task uses the USMF demo company.</span></span> 


## <a name="create-bank-facility-agreement"></a><span data-ttu-id="e3055-106">Stofna bankaaðstöðusamningur</span><span class="sxs-lookup"><span data-stu-id="e3055-106">Create Bank facility agreement</span></span>
1. <span data-ttu-id="e3055-107">Fara í Reiðufé og bankastjórnun > Ábyrgðaryfirlýsing > Bankaaðstöðusamningur.</span><span class="sxs-lookup"><span data-stu-id="e3055-107">Go to Cash and bank management > Letters of guarantee > Bank facility agreements.</span></span>
2. <span data-ttu-id="e3055-108">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="e3055-108">Click New.</span></span>
3. <span data-ttu-id="e3055-109">Í svæðið Samningsnúmer er samningsnúmer banka fyrir færsluna fært inn.</span><span class="sxs-lookup"><span data-stu-id="e3055-109">In the Agreement number field, enter the bank agreement number for the transaction.</span></span>
4. <span data-ttu-id="e3055-110">Í svæðið Bankareikningur er sá bankareikningur valinn fyrir hvern ábyrgðarbréf er opið.</span><span class="sxs-lookup"><span data-stu-id="e3055-110">In the Bank account field, select the bank account number for which the letter of guarantee is open.</span></span> 
5. <span data-ttu-id="e3055-111">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="e3055-111">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="e3055-112">Í reitnum upphafsdagur, færa inn dagsetningu og tíma.</span><span class="sxs-lookup"><span data-stu-id="e3055-112">In the Start date field, enter a date and time.</span></span>
7. <span data-ttu-id="e3055-113">Í reitnum Lokadagur, færa inn dagsetningu og tíma.</span><span class="sxs-lookup"><span data-stu-id="e3055-113">In the End date field, enter a date and time.</span></span>
8. <span data-ttu-id="e3055-114">Víxla útvíkkun á liðnum Almennt.</span><span class="sxs-lookup"><span data-stu-id="e3055-114">Toggle the expansion of the General section.</span></span>
9. <span data-ttu-id="e3055-115">Smella á bæta Við línu.</span><span class="sxs-lookup"><span data-stu-id="e3055-115">Click Add line.</span></span>
10. <span data-ttu-id="e3055-116">Í reitnum aðstöðugerð skal smella a fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="e3055-116">In the Facility type field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="e3055-117">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="e3055-117">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="e3055-118">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="e3055-118">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="e3055-119">Í reitinn Mörk færirðu inn umsamda upphæð sem samið var um við bankann.</span><span class="sxs-lookup"><span data-stu-id="e3055-119">In the Limit field, enter the amount negotiated with the bank.</span></span>
14. <span data-ttu-id="e3055-120">Smelltu á Vista.</span><span class="sxs-lookup"><span data-stu-id="e3055-120">Click Save.</span></span>
15. <span data-ttu-id="e3055-121">Víxla útvíkkun á hluta ábyrgðarbréfs.</span><span class="sxs-lookup"><span data-stu-id="e3055-121">Toggle the expansion of the Letter of guarantee section.</span></span>
16. <span data-ttu-id="e3055-122">Veljið valkost í svæðinu Útreikningsaðferð.</span><span class="sxs-lookup"><span data-stu-id="e3055-122">In the Calculation method field, select an option.</span></span>
    * <span data-ttu-id="e3055-123">Færa inn útreikningsaðferð og prósentuupplýsingar fyrir framlegð í reiðufé, úthlutunarþóknun, framlengingarþóknun, Auka virðisþóknun eða Minnka virðisþóknun, eins og við á.</span><span class="sxs-lookup"><span data-stu-id="e3055-123">Enter the calculation method and percentage details for the Cash margin, Issuance commission, Extension commission, Increase value commission, or Decrease value commission, as appropriate.</span></span>   
17. <span data-ttu-id="e3055-124">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="e3055-124">Click Save.</span></span>

## <a name="extend-bank-facility-agreement"></a><span data-ttu-id="e3055-125">Framlengja bankaaðstöðusamning</span><span class="sxs-lookup"><span data-stu-id="e3055-125">Extend bank facility agreement</span></span>
1. <span data-ttu-id="e3055-126">Smellt er á víkka út til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="e3055-126">Click Extend to open the drop dialog.</span></span>
2. <span data-ttu-id="e3055-127">Færa inn gildi í svæðið nýtt samningsnúmer.</span><span class="sxs-lookup"><span data-stu-id="e3055-127">In the New agreement number field, type a value.</span></span>
3. <span data-ttu-id="e3055-128">Í reitnum Lokadagur, færa inn dagsetningu og tíma.</span><span class="sxs-lookup"><span data-stu-id="e3055-128">In the End date field, enter a date and time.</span></span>
4. <span data-ttu-id="e3055-129">Smellt er á Framlengja.</span><span class="sxs-lookup"><span data-stu-id="e3055-129">Click Extend.</span></span>
5. <span data-ttu-id="e3055-130">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="e3055-130">Click Save.</span></span>
6. <span data-ttu-id="e3055-131">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="e3055-131">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]