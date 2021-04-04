---
title: Stjórna reglum fyrir kaup og sölu á leyfisdögum
description: Hægt er að gera starfsmönnum kleift að kaupa og selja leyfisdaga í Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeaveBuySellPolicy, LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ccc6bf2e8b070e92cc4dbb98d8ec35ce60723516
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/17/2021
ms.locfileid: "5468084"
---
# <a name="manage-buy-and-sell-leave-policies"></a><span data-ttu-id="3a60c-103">Stjórna reglum fyrir kaup og sölu á leyfisdögum</span><span class="sxs-lookup"><span data-stu-id="3a60c-103">Manage buy and sell leave policies</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="3a60c-104">Hægt er að gera starfsmönnum kleift að kaupa og selja leyfisdaga með því að búa til reglu um kaup og sölu á leyfisdögum.</span><span class="sxs-lookup"><span data-stu-id="3a60c-104">You can enable employees to buy and sell leave by creating a buy and sell leave policy.</span></span> <span data-ttu-id="3a60c-105">Hægt er að skilgreina þessar reglur til að nota verkflæði fyrir samþykktir, stilla hámarksfjárhæðir og taxta og stilla taxta fyrir kaup og sölur.</span><span class="sxs-lookup"><span data-stu-id="3a60c-105">You can configure these policies to use workflow for approvals, set maximum amounts and rates, and set rates for buying and selling.</span></span> 

## <a name="enable-employees-to-buy-and-sell-leave"></a><span data-ttu-id="3a60c-106">Gera starfsmönnum kleift að kaupa og selja leyfisdaga</span><span class="sxs-lookup"><span data-stu-id="3a60c-106">Enable employees to buy and sell leave</span></span>

1. <span data-ttu-id="3a60c-107">Á síðunni **Færibreytur leyfis og fjarvista** skal velja **Já** fyrir **Leyfa starfsmönnum að kaupa leyfisdaga** og **Leyfa starfsmönnum að selja leyfisdaga**.</span><span class="sxs-lookup"><span data-stu-id="3a60c-107">On the **Leave and absence parameters** page, select **Yes** for **Allow employees to buy leave** and **Allow employees to sell leave**.</span></span>

## <a name="create-a-buy-and-sell-leave-policy"></a><span data-ttu-id="3a60c-108">Búa til reglu um kaup og sölu leyfisdaga</span><span class="sxs-lookup"><span data-stu-id="3a60c-108">Create a buy and sell leave policy</span></span>

1. <span data-ttu-id="3a60c-109">Á síðunni **Leyfi og fjarvera** velurðu flipann **Tenglar**.</span><span class="sxs-lookup"><span data-stu-id="3a60c-109">On the **Leave and absence** page, select the **Links** tab.</span></span> 

2. <span data-ttu-id="3a60c-110">Veljið **Regla um kaup og sölu leyfisdaga**.</span><span class="sxs-lookup"><span data-stu-id="3a60c-110">Select **Buy and sell leave policy**.</span></span>

3. <span data-ttu-id="3a60c-111">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="3a60c-111">Select **New**.</span></span>

4. <span data-ttu-id="3a60c-112">Sláið inn **Heiti** og **Lýsing** fyrir regluna undir **Regla um kaup og sölu leyfisdaga**.</span><span class="sxs-lookup"><span data-stu-id="3a60c-112">Enter a **Name** and **Description** for the policy under **Buy and sell leave policy**.</span></span> 

5. <span data-ttu-id="3a60c-113">Veljið **Gerð reglu**.</span><span class="sxs-lookup"><span data-stu-id="3a60c-113">Select a **Policy type**.</span></span> 

   <span data-ttu-id="3a60c-114">Tiltækar gerðir reglu eru **Fjöldi** og **Klukkustundir á viku**.</span><span class="sxs-lookup"><span data-stu-id="3a60c-114">The available policy types are **Amount** and **Hours per week**.</span></span> <span data-ttu-id="3a60c-115">Veljið **Fjöldi** til að færa inn **Fastan fjölda** fyrir þann hámarksfjölda sem starfsmenn geta keypt og selt.</span><span class="sxs-lookup"><span data-stu-id="3a60c-115">Select **Amount** to enter a **Fixed amount** for the maximum amounts employees can buy and sell.</span></span> <span data-ttu-id="3a60c-116">Ef valið er **Klukkustundir á viku** eru skilgreindar vinnustundir í úthlutuðu vinnutímadagatali starfsmanns notaðar til að ákveða hámarksfjölda fyrir regluna.</span><span class="sxs-lookup"><span data-stu-id="3a60c-116">If you select **Hours per week**, the working time defined in the employee's assigned working time calendar is used to determine the maximum amount of the policy.</span></span> 

6. <span data-ttu-id="3a60c-117">Veljið **Upphafsdagsetning** og **Lokadagsetning** fyrir regluna.</span><span class="sxs-lookup"><span data-stu-id="3a60c-117">Select a **Start date** and **End date** for the policy.</span></span> <span data-ttu-id="3a60c-118">Beiðnir um að kaupa eða selja leyfi verða aðeins í boði fyrir innsendingu á þessum tímaramma.</span><span class="sxs-lookup"><span data-stu-id="3a60c-118">Requests to buy or sell leave will only be available for submission during this time frame.</span></span> 

7. <span data-ttu-id="3a60c-119">Veljið **Kenni verkflæðis** fyrir regluna.</span><span class="sxs-lookup"><span data-stu-id="3a60c-119">Select a **Workflow ID** for the policy.</span></span> <span data-ttu-id="3a60c-120">Allar beiðnir um kaup og sölur munu nota þetta verkflæði fyrir yfirferð og samþykki.</span><span class="sxs-lookup"><span data-stu-id="3a60c-120">Any buy and sell requests will use this workflow for review and approval.</span></span> 

8. <span data-ttu-id="3a60c-121">Undir **Regla um kaup** skal velja **Jafngildi fulls starfs** (JFS) til að hlutfallsskipta hámarksfjöldanum samkvæmt JFS sem skilgreint er fyrir stöðu starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="3a60c-121">Under **Buy policy**, select **Full time equivalency** (FTE) to prorate the maximum amount based on the FTE defined on the employee's position.</span></span> <span data-ttu-id="3a60c-122">Ef gerð reglunnar er **Fjöldi** skal slá inn **Fastur hámarksfjöldi**.</span><span class="sxs-lookup"><span data-stu-id="3a60c-122">If the policy type is **Amount**, enter a **Maximum fixed amount**.</span></span> 

9. <span data-ttu-id="3a60c-123">Veljið **Bæta við** til að bæta við leyfisgerðum fyrir starfsmenn til að kaupa leyfisdaga.</span><span class="sxs-lookup"><span data-stu-id="3a60c-123">Select **Add** to add the leave types for employees to buy leave.</span></span> <span data-ttu-id="3a60c-124">Hægt er að bæta við mörgum leyfisgerðum í regluna.</span><span class="sxs-lookup"><span data-stu-id="3a60c-124">You can add multiple leave types to the policy.</span></span> 

10. <span data-ttu-id="3a60c-125">Færið inn **Starfsaldur í mánuðum** fyrir leyfisgerðina til að virkja mismunandi starfsaldur í mánuðum til að ákveða hámarksfjölda sem starfsmaður getur keypt.</span><span class="sxs-lookup"><span data-stu-id="3a60c-125">Enter the **Months of service** for the leave type to enable different months of service to determine the maximum amount an employee can buy.</span></span> 

11. <span data-ttu-id="3a60c-126">Færið inn **Hámarksfjöli** fyrir leyfisgerðina.</span><span class="sxs-lookup"><span data-stu-id="3a60c-126">Enter the **Maximum amount** for the leave type.</span></span> 

12. <span data-ttu-id="3a60c-127">Færið inn **Taxti** sem starfsmaður mun kaupa leyfisdaga á.</span><span class="sxs-lookup"><span data-stu-id="3a60c-127">Enter the **Rate** at which the employee will buy the leave.</span></span> 

13. <span data-ttu-id="3a60c-128">Einnig er hægt að færa inn **Tekjukóði** til að nota við kaup á leyfisdögum.</span><span class="sxs-lookup"><span data-stu-id="3a60c-128">Optionally enter the **Earning code** to be used for buying leave.</span></span> 

14. <span data-ttu-id="3a60c-129">Valfrjálst er að stilla hvort nota eigi JFS til að ákveða hámarksfjölda fyrir leyfisgerðina.</span><span class="sxs-lookup"><span data-stu-id="3a60c-129">Optionally set whether to use FTE to determine the maximum amount for the leave type.</span></span> 

15. <span data-ttu-id="3a60c-130">Til að búa til reglu um sölu skal fylgja skrefum 8 til 14 undir **Söluregla**.</span><span class="sxs-lookup"><span data-stu-id="3a60c-130">To create a sell policy, follow steps 8 through 14 under **Sell policy**.</span></span> 

## <a name="add-the-buy-and-sell-leave-policy-to-a-leave-and-absence-plan"></a><span data-ttu-id="3a60c-131">Bæta reglu um kaup og sölu á leyfisdögum við leyfis- og fjarveruáætlun</span><span class="sxs-lookup"><span data-stu-id="3a60c-131">Add the buy and sell leave policy to a leave and absence plan</span></span>

1. <span data-ttu-id="3a60c-132">Á síðunni **Leyfi og fjarvera** skal velja leyfis- og fjarveruáætlun.</span><span class="sxs-lookup"><span data-stu-id="3a60c-132">On the **Leave and absence** page, select a leave and absence plan.</span></span>

2. <span data-ttu-id="3a60c-133">Undir **Reglur** skal velja **Regla um kaup og sölu leyfisdaga**.</span><span class="sxs-lookup"><span data-stu-id="3a60c-133">Under **Rules**, select **Buy and sell leave policy**.</span></span>

## <a name="see-also"></a><span data-ttu-id="3a60c-134">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="3a60c-134">See also</span></span>

[<span data-ttu-id="3a60c-135">Yfirlit yfir leyfi og fjarvistir</span><span class="sxs-lookup"><span data-stu-id="3a60c-135">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)</br>
[<span data-ttu-id="3a60c-136">Grunnstilla gerðir leyfis og fjarvista</span><span class="sxs-lookup"><span data-stu-id="3a60c-136">Configure leave and absence types</span></span>](hr-leave-and-absence-types.md)</br>
[<span data-ttu-id="3a60c-137">Uppsöfnunaráætlanir fyrir leyfi og fjarvistir</span><span class="sxs-lookup"><span data-stu-id="3a60c-137">Accrue leave and absence plans</span></span>](hr-leave-and-absence-accrue.md)</br>
[<span data-ttu-id="3a60c-138">Kaupa og selja leyfisdaga</span><span class="sxs-lookup"><span data-stu-id="3a60c-138">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]