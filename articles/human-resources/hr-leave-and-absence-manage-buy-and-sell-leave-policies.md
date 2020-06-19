---
title: Stjórna reglum fyrir kaup og sölu á leyfisdögum
description: Hægt er að gera starfsmönnum kleift að kaupa og selja leyfisdaga í Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 06/01/2020
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
ms.openlocfilehash: 859445f2b6e980b5960e512e69129f6a8fc6df2b
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429014"
---
# <a name="manage-buy-and-sell-leave-policies"></a><span data-ttu-id="307a6-103">Stjórna reglum fyrir kaup og sölu á leyfisdögum</span><span class="sxs-lookup"><span data-stu-id="307a6-103">Manage buy and sell leave policies</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="307a6-104">Hægt er að gera starfsmönnum kleift að kaupa leyfisdaga með því að búa til reglu um kaup á leyfisdögum.</span><span class="sxs-lookup"><span data-stu-id="307a6-104">You can enable employees to buy leave by creating a buy leave policy.</span></span>  

## <a name="enable-employees-to-buy-and-sell-leave"></a><span data-ttu-id="307a6-105">Gera starfsmönnum kleift að kaupa og selja leyfisdaga</span><span class="sxs-lookup"><span data-stu-id="307a6-105">Enable employees to buy and sell leave</span></span>

1. <span data-ttu-id="307a6-106">Á síðunni **Færibreytur leyfis og fjarvista** skal velja **Já** fyrir **Leyfa starfsmönnum að kaupa leyfisdaga**.</span><span class="sxs-lookup"><span data-stu-id="307a6-106">On the **Leave and absence parameters** page, select **Yes** for **Allow employees to buy leave**.</span></span> 

## <a name="create-a-buy-leave-policy"></a><span data-ttu-id="307a6-107">Búa til reglu um kaup á leyfisdögum</span><span class="sxs-lookup"><span data-stu-id="307a6-107">Create a buy leave policy</span></span>

1. <span data-ttu-id="307a6-108">Á síðunni **Leyfi og fjarvera** velurðu flipann **Tenglar**.</span><span class="sxs-lookup"><span data-stu-id="307a6-108">On the **Leave and absence** page, select the **Links** tab.</span></span> 

2. <span data-ttu-id="307a6-109">Veljið **Regla um kaup og sölu leyfisdaga**.</span><span class="sxs-lookup"><span data-stu-id="307a6-109">Select **Buy and sell leave policy**.</span></span>

3. <span data-ttu-id="307a6-110">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="307a6-110">Select **New**.</span></span>

4. <span data-ttu-id="307a6-111">Sláið inn **Heiti** og **Lýsing** fyrir regluna undir **Regla um kaup og sölu leyfisdaga**.</span><span class="sxs-lookup"><span data-stu-id="307a6-111">Enter a **Name** and **Description** for the policy under **Buy and sell leave policy**.</span></span> 

5. <span data-ttu-id="307a6-112">Veljið **Gerð reglu**.</span><span class="sxs-lookup"><span data-stu-id="307a6-112">Select a **Policy type**.</span></span> 

   <span data-ttu-id="307a6-113">Tiltækar gerðir reglu eru **Fjöldi** og **Klukkustundir á viku**.</span><span class="sxs-lookup"><span data-stu-id="307a6-113">The available policy types are **Amount** and **Hours per week**.</span></span> <span data-ttu-id="307a6-114">Veljið **Fjöldi** til að færa inn **Fastan fjölda** fyrir þann hámarksfjölda sem starfsmenn geta keypt og selt.</span><span class="sxs-lookup"><span data-stu-id="307a6-114">Select **Amount** to enter a **Fixed amount** for the maximum amounts employees can buy and sell.</span></span> <span data-ttu-id="307a6-115">Ef valið er **Klukkustundir á viku** eru skilgreindar vinnustundir í úthlutuðu vinnutímadagatali starfsmanns notaðar til að ákveða hámarksfjölda fyrir regluna.</span><span class="sxs-lookup"><span data-stu-id="307a6-115">If you select **Hours per week**, the working time defined in the employee's assigned working time calendar is used to determine the maximum amount of the policy.</span></span> 

6. <span data-ttu-id="307a6-116">Veljið **Upphafsdagsetning** og **Lokadagsetning** fyrir regluna.</span><span class="sxs-lookup"><span data-stu-id="307a6-116">Select a **Start date** and **End date** for the policy.</span></span> <span data-ttu-id="307a6-117">Beiðnir um að kaupa eða selja leyfi verða aðeins í boði fyrir innsendingu á þessum tímaramma.</span><span class="sxs-lookup"><span data-stu-id="307a6-117">Requests to buy or sell leave will only be available for submission during this time frame.</span></span> 

7. <span data-ttu-id="307a6-118">Undir **Regla um kaup** skal velja **Jafngildi fulls starfs** (JFS) til að hlutfallsskipta hámarksfjöldanum samkvæmt JFS sem skilgreint er fyrir stöðu starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="307a6-118">Under **Buy policy**, select **Full time equivalency** (FTE) to prorate the maximum amount based on the FTE defined on the employee's position.</span></span> <span data-ttu-id="307a6-119">Ef gerð reglunnar er **Fjöldi** skal slá inn **Fastur hámarksfjöldi**.</span><span class="sxs-lookup"><span data-stu-id="307a6-119">If the policy type is **Amount**, enter a **Maximum fixed amount**.</span></span> 

8. <span data-ttu-id="307a6-120">Veljið **Bæta við** til að bæta við leyfisgerðum fyrir starfsmenn til að kaupa leyfisdaga.</span><span class="sxs-lookup"><span data-stu-id="307a6-120">Select **Add** to add the leave types for employees to buy leave.</span></span> <span data-ttu-id="307a6-121">Hægt er að bæta við mörgum leyfisgerðum í regluna.</span><span class="sxs-lookup"><span data-stu-id="307a6-121">You can add multiple leave types to the policy.</span></span> 

9. <span data-ttu-id="307a6-122">Færið inn **Starfsaldur í mánuðum** fyrir leyfisgerðina til að virkja mismunandi starfsaldur í mánuðum til að ákveða hámarksfjölda sem starfsmaður getur keypt.</span><span class="sxs-lookup"><span data-stu-id="307a6-122">Enter the **Months of service** for the leave type to enable different months of service to determine the maximum amount an employee can buy.</span></span> 

10. <span data-ttu-id="307a6-123">Færið inn **Hámarksfjöli** fyrir leyfisgerðina.</span><span class="sxs-lookup"><span data-stu-id="307a6-123">Enter the **Maximum amount** for the leave type.</span></span> 

11. <span data-ttu-id="307a6-124">Færið inn **Taxti** sem starfsmaður mun kaupa leyfisdaga á.</span><span class="sxs-lookup"><span data-stu-id="307a6-124">Enter the **Rate** at which the employee will buy the leave.</span></span> 

12. <span data-ttu-id="307a6-125">Einnig er hægt að færa inn **Tekjukóði** til að nota við kaup á leyfisdögum.</span><span class="sxs-lookup"><span data-stu-id="307a6-125">Optionally enter the **Earning code** to be used for buying leave.</span></span> 

13. <span data-ttu-id="307a6-126">Valfrjálst er að stilla hvort nota eigi JFS til að ákveða hámarksfjölda fyrir leyfisgerðina.</span><span class="sxs-lookup"><span data-stu-id="307a6-126">Optionally set whether to use FTE to determine the maximum amount for the leave type.</span></span> 

## <a name="add-the-buy-and-sell-leave-policy-to-a-leave-and-absence-plan"></a><span data-ttu-id="307a6-127">Bæta reglu um kaup og sölu á leyfisdögum við leyfis- og fjarveruáætlun</span><span class="sxs-lookup"><span data-stu-id="307a6-127">Add the buy and sell leave policy to a leave and absence plan</span></span>

1. <span data-ttu-id="307a6-128">Á síðunni **Leyfi og fjarvera** skal velja leyfis- og fjarveruáætlun.</span><span class="sxs-lookup"><span data-stu-id="307a6-128">On the **Leave and absence** page, select a leave and absence plan.</span></span>

2. <span data-ttu-id="307a6-129">Undir **Reglur** skal velja **Regla um kaup og sölu leyfisdaga**.</span><span class="sxs-lookup"><span data-stu-id="307a6-129">Under **Rules**, select **Buy and sell leave policy**.</span></span>

## <a name="see-also"></a><span data-ttu-id="307a6-130">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="307a6-130">See also</span></span>

[<span data-ttu-id="307a6-131">Yfirlit yfir leyfi og fjarvistir</span><span class="sxs-lookup"><span data-stu-id="307a6-131">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)</br>
[<span data-ttu-id="307a6-132">Grunnstilla gerðir leyfis og fjarvista</span><span class="sxs-lookup"><span data-stu-id="307a6-132">Configure leave and absence types</span></span>](hr-leave-and-absence-types.md)</br>
[<span data-ttu-id="307a6-133">Uppsöfnunaráætlanir fyrir leyfi og fjarvistir</span><span class="sxs-lookup"><span data-stu-id="307a6-133">Accrue leave and absence plans</span></span>](hr-leave-and-absence-accrue.md)</br>
[<span data-ttu-id="307a6-134">Kaupa og selja leyfisdaga</span><span class="sxs-lookup"><span data-stu-id="307a6-134">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

