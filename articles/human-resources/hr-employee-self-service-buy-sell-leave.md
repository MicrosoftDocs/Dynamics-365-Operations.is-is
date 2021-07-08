---
title: Kaupa og selja leyfisdaga
description: Í Dynamics 365 Human Resources er hægt að leggja fram beiðnir um að kaupa og selja leyfi samkvæmt reglum um kaup og sölur leyfa sem fyrirtækið hefur sett upp.
author: andreabichsel
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ESSLeaveBuyRequestEntry, EssWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6d32abacc1539cb930ad6f1ebcfe6fa9af4befcf
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271487"
---
# <a name="buy-and-sell-leave"></a><span data-ttu-id="9db3c-103">Kaupa og selja leyfisdaga</span><span class="sxs-lookup"><span data-stu-id="9db3c-103">Buy and sell leave</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="9db3c-104">Í Dynamics 365 Human Resources er hægt að leggja fram beiðnir um að kaupa og selja leyfi samkvæmt reglum um kaup og sölur leyfa sem fyrirtækið hefur sett upp.</span><span class="sxs-lookup"><span data-stu-id="9db3c-104">In Dynamics 365 Human Resources, you can submit requests to buy and sell leave based on the buy and sell leave policies set up by your company.</span></span>  

## <a name="request-to-buy-leave"></a><span data-ttu-id="9db3c-105">Biðja um að kaupa leyfi</span><span class="sxs-lookup"><span data-stu-id="9db3c-105">Request to buy leave</span></span>

1. <span data-ttu-id="9db3c-106">Á vinnusvæðinu **Sjálfsafgreiðsla starfsmanns** skal velja **Beiðni um kaup á leyfisdögum** í reitnum **Frídagastaða**.</span><span class="sxs-lookup"><span data-stu-id="9db3c-106">In the **Employee self service** workspace, select **Buy leave request** in the **Time Off Balances** tile.</span></span> 

2. <span data-ttu-id="9db3c-107">Bætið við **Leyfisgerð** og sláið inn **Upphæð** fyrir leyfisupphæð sem á að kaupa.</span><span class="sxs-lookup"><span data-stu-id="9db3c-107">Add a **Leave type** and enter an **Amount** for the amount of leave you'd like to buy.</span></span> 

3. <span data-ttu-id="9db3c-108">Veldu **Sendu inn** þegar þú ert tilbúinn að leggja fram beiðni þína.</span><span class="sxs-lookup"><span data-stu-id="9db3c-108">Select **Submit** when you're ready to submit your request.</span></span> 

<span data-ttu-id="9db3c-109">Stöðurnar verða annaðhvort uppfærðar sjálfkrafa eða fara í gegnum samþykktarferli áður en uppfærsla fer fram.</span><span class="sxs-lookup"><span data-stu-id="9db3c-109">Your balances will either automatically update or go through an approval process before updating.</span></span> <span data-ttu-id="9db3c-110">Þetta veltur á því hvernig kaupreglan hefur verið skilgreind.</span><span class="sxs-lookup"><span data-stu-id="9db3c-110">This depends on how the buy policy has been configured.</span></span>

## <a name="request-to-sell-leave"></a><span data-ttu-id="9db3c-111">Beiðni um að selja leyfi</span><span class="sxs-lookup"><span data-stu-id="9db3c-111">Request to sell leave</span></span>

1. <span data-ttu-id="9db3c-112">Á vinnusvæðinu **Sjálfsafgreiðsla starfsmanns** skal velja **Beiðni um að selja leyfisdaga** í reitnum **Frídagastaða**.</span><span class="sxs-lookup"><span data-stu-id="9db3c-112">In the **Employee self service** workspace, select **Sell leave request** in the **Time Off Balances** tile.</span></span> 

2. <span data-ttu-id="9db3c-113">Bætið við **Leyfisgerð** og sláið inn **Upphæð** fyrir leyfisupphæð sem á að selja.</span><span class="sxs-lookup"><span data-stu-id="9db3c-113">Add a **Leave type** and enter an **Amount** for the amount of leave you'd like to sell.</span></span> 

3. <span data-ttu-id="9db3c-114">Veldu **Sendu inn** þegar þú ert tilbúinn að leggja fram beiðni þína.</span><span class="sxs-lookup"><span data-stu-id="9db3c-114">Select **Submit** when you're ready to submit your request.</span></span>

<span data-ttu-id="9db3c-115">Stöðurnar verða annaðhvort uppfærðar sjálfkrafa eða fara í gegnum samþykktarferli áður en uppfærsla fer fram.</span><span class="sxs-lookup"><span data-stu-id="9db3c-115">Your balances will either automatically update or go through an approval process before updating.</span></span> <span data-ttu-id="9db3c-116">Þetta veltur á því hvernig kaupreglan hefur verið skilgreind.</span><span class="sxs-lookup"><span data-stu-id="9db3c-116">This depends on how the buy policy has been configured.</span></span>


## <a name="troubleshooting"></a><span data-ttu-id="9db3c-117">Úrræðaleit</span><span class="sxs-lookup"><span data-stu-id="9db3c-117">Troubleshooting</span></span> 

<span data-ttu-id="9db3c-118">Ef ósk um kaup eða sölu á leyfi mistekst munu notendur með réttindin **EssLeaveBuySellRequestApprover** geta farið yfir skilaboðakladdann fyrir allar óskir um kaup og sölu á leyfum.</span><span class="sxs-lookup"><span data-stu-id="9db3c-118">If a buy or sell leave request workflow fails, users with the **EssLeaveBuySellRequestApprover** privilege can review the message log for all leave buy and sell requests.</span></span> <span data-ttu-id="9db3c-119">Þetta er gert með því að fara í **Leyfi og fjarvistir > Tengill > Beiðnir um kaup og sölu á leyfi > Skilaboðakladdi** (efst til vinstri).</span><span class="sxs-lookup"><span data-stu-id="9db3c-119">To do this, go to **Leave and absence > Link > Buy and sell leave requests > Message log** (on the upper left).</span></span> <span data-ttu-id="9db3c-120">**Skilaboðakladdinn** sýnir notendum hvernig unnið var úr færslunum og tengdri verkflæðissögu.</span><span class="sxs-lookup"><span data-stu-id="9db3c-120">The **Message log** shows users how the transactions were processed and the associated workflow history.</span></span>


## <a name="see-also"></a><span data-ttu-id="9db3c-121">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="9db3c-121">See also</span></span>

[<span data-ttu-id="9db3c-122">Yfirlit yfir leyfi og fjarvistir</span><span class="sxs-lookup"><span data-stu-id="9db3c-122">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)</br>
[<span data-ttu-id="9db3c-123">Stjórna reglum fyrir kaup og sölu á leyfisdögum</span><span class="sxs-lookup"><span data-stu-id="9db3c-123">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
