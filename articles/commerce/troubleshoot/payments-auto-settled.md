---
title: Greiðslur eru sjálfkrafa jafnaðar áður en pantanir eru reikningsfærðar eða sendar
description: Þetta efnisatriði býður upp á leiðsögn úrræðaleitar sem getur reynst hjálpleg þegar greiðsla er jöfnuð í Adyen-gátt strax og pöntun er gerð, jafnvel þótt sölupöntunin hafi ekki verið reikningsfærð eða send.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: b4fd37a3c45f2559c9659f072ca0b6f02e712f53
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018261"
---
# <a name="payments-are-automatically-settled-before-orders-are-invoiced-or-shipped"></a><span data-ttu-id="55151-103">Greiðslur eru sjálfkrafa jafnaðar áður en pantanir eru reikningsfærðar eða sendar</span><span class="sxs-lookup"><span data-stu-id="55151-103">Payments are automatically settled before orders are invoiced or shipped</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="55151-104">Þetta efnisatriði býður upp á leiðsögn úrræðaleitar sem getur reynst hjálpleg þegar greiðsla er jöfnuð í Adyen-gátt strax og pöntun er gerð, jafnvel þótt sölupöntunin hafi ekki verið reikningsfærð eða send.</span><span class="sxs-lookup"><span data-stu-id="55151-104">This topic provides troubleshooting guidance that can help when a payment is settled in the Adyen portal immediately after an order is placed, even though the sales order hasn't been invoiced or shipped.</span></span>

## <a name="description"></a><span data-ttu-id="55151-105">lýsing</span><span class="sxs-lookup"><span data-stu-id="55151-105">Description</span></span>

<span data-ttu-id="55151-106">Þegar pöntun er gerð er greiðslan strax jöfnuð í Adyen-gáttinni jafnvel þótt sölupöntunin hafi ekki verið reikningsfærð eða send.</span><span class="sxs-lookup"><span data-stu-id="55151-106">After an order is placed, the payment is immediately settled in the Adyen portal, even though the sales order hasn't been invoiced or shipped.</span></span>

## <a name="resolution"></a><span data-ttu-id="55151-107">Upplausn</span><span class="sxs-lookup"><span data-stu-id="55151-107">Resolution</span></span>

### <a name="configure-manual-capture-for-e-commerce-payments-in-the-adyen-portal"></a><span data-ttu-id="55151-108">Skilgreina handvirka úthlutun fyrir greiðslur rafrænna viðskipta í Adyen-gáttinni</span><span class="sxs-lookup"><span data-stu-id="55151-108">Configure manual capture for e-commerce payments in the Adyen portal</span></span>

<span data-ttu-id="55151-109">Til að skilgreina handvirka úthlutun fyrir greiðslur rafrænna viðskipta í Adyen-gáttinni skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="55151-109">To configure manual capture for e-commerce payments in the Adyen portal, follow these steps.</span></span>

1. <span data-ttu-id="55151-110">Skráðu þig inn í Adyen gáttina.</span><span class="sxs-lookup"><span data-stu-id="55151-110">Sign in to the Adyen portal.</span></span>
1. <span data-ttu-id="55151-111">Efst í hægra horninu skal velja söluaðilareikninginn fyrri rás rafrænna viðskipta.</span><span class="sxs-lookup"><span data-stu-id="55151-111">In the upper-right corner, select your merchant account for the e-commerce channel.</span></span>
1. <span data-ttu-id="55151-112">Á efstu yfirlitsstikunni skal velja **Reikningur** og síðan **Stillingar**.</span><span class="sxs-lookup"><span data-stu-id="55151-112">On the top navigation, select **Account**, and then select **Settings**.</span></span>
1. <span data-ttu-id="55151-113">Í reitnum **Seinka úthlutun** skal velja **handvirkt**.</span><span class="sxs-lookup"><span data-stu-id="55151-113">In the **Capture Delay** field, select **manual**.</span></span>

    ![Stilling Seinka úthlutun í Adyen-gáttinni](media/adyen-capture-delay.jpg)

## <a name="additional-resources"></a><span data-ttu-id="55151-115">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="55151-115">Additional resources</span></span>

[<span data-ttu-id="55151-116">Úthlutun Adyen-greiðslu</span><span class="sxs-lookup"><span data-stu-id="55151-116">Adyen payment capture</span></span>](https://docs.adyen.com/point-of-sale/capturing-payments)

[<span data-ttu-id="55151-117">Dynamics 365-greiðslutengill fyrir Adyen</span><span class="sxs-lookup"><span data-stu-id="55151-117">Dynamics 365 Payment Connector for Adyen</span></span>](../dev-itpro/adyen-connector.md)

[<span data-ttu-id="55151-118">Setja upp Adyen-greiðslutengil fyrir Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="55151-118">Set up the Adyen payment connector for Dynamics 365</span></span>](https://docs.adyen.com/plugins/microsoft-dynamics)
