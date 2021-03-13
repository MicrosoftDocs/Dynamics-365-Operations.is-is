---
title: Fækka dögum á áskrifarþóknunum
description: Til þess að stytta fjölda daga í fyrirliggjandi áskriftarþóknun er hægt að stofna nýja færslu, þar sem tímabilið sem ekki á lengur að vera hluti af áskriftarþóknun er fjarlægt.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ae2486d08e89c06d76ab9945ccce25c5e97f1500
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010566"
---
# <a name="reduce-the-days-on-subscription-fees"></a><span data-ttu-id="d19e3-103">Fækka dögum á áskrifarþóknunum</span><span class="sxs-lookup"><span data-stu-id="d19e3-103">Reduce the days on subscription fees</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="d19e3-104">Til þess að stytta fjölda daga í fyrirliggjandi áskriftarþóknun er hægt að stofna nýja færslu, þar sem tímabilið sem ekki á lengur að vera hluti af áskriftarþóknun er fjarlægt.</span><span class="sxs-lookup"><span data-stu-id="d19e3-104">To reduce the number of days of an existing subscription fee, you can create a new transaction in which you remove the period of time that should no longer be part of the subscription fee interval.</span></span>

## <a name="reduce-the-days-on-a-subscription-fee"></a><span data-ttu-id="d19e3-105">Fækka dögum í áskriftarþóknun</span><span class="sxs-lookup"><span data-stu-id="d19e3-105">Reduce the days on a subscription fee</span></span>

1.  <span data-ttu-id="d19e3-106">Smelltu á **Þjónustustjórnun** \> **Almennt** \> **Þjónustuáskriftir** \> **Allar þjónustuáskriftir**.</span><span class="sxs-lookup"><span data-stu-id="d19e3-106">Click **Service management** \> **Common** \> **Service subscriptions** \> **All service subscriptions**.</span></span> <span data-ttu-id="d19e3-107">Veldu þjónustuáskriftina og smelltu svo á **Áskriftargjald** í aðgerðasvæðinu</span><span class="sxs-lookup"><span data-stu-id="d19e3-107">Select the service subscription, and on the Action Pane, click **Subscription fees**</span></span>

2.  <span data-ttu-id="d19e3-108">Í reitnum **Gerð áskriftar** skal velja **Minnkunardagar**.</span><span class="sxs-lookup"><span data-stu-id="d19e3-108">In the **Subscription type** field, select **Reduction days**.</span></span>

3.  <span data-ttu-id="d19e3-109">Notaðu reitina **Frá dagsetningu** og **Til dagsetningar** til að skilgreina dagsetningabil áskriftargjaldsins, sem á að fjarlægja úr tímabili áskriftarþóknunar og smelltu síðan á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="d19e3-109">Use the **From date** field and the **To date** fields to define the date interval of the subscription fee that you want to remove from the subscription fee period, and then click **OK**.</span></span>

<span data-ttu-id="d19e3-110">Til þess að skoða stofnaða færslu skal smella á **Þóknunarfærslur** í skjámyndinni **Áskrift**.</span><span class="sxs-lookup"><span data-stu-id="d19e3-110">To view the transaction that was created, in the **Subscription** form, click **Fee transactions**.</span></span>

## <a name="example"></a><span data-ttu-id="d19e3-111">Dæmi</span><span class="sxs-lookup"><span data-stu-id="d19e3-111">Example</span></span>

<span data-ttu-id="d19e3-112">Ef tímabil áskriftarfærslu gildir frá 1. janúar til 31. janúar og þú vilt stytta tímabilið um 10 daga skaltu búa til nýja færslu þar sem stytta tímabilið er 1. janúar til 10. janúar.</span><span class="sxs-lookup"><span data-stu-id="d19e3-112">If a subscription transaction period runs from January 1 to January 31, and you want to reduce the period by 10 days, create a new transaction in which the reduction period is January 1 to January 10.</span></span> <span data-ttu-id="d19e3-113">(Sytta tímabilið getur einnig verið 5. janúar til 15. janúar eða önnur tíu daga tímabil).</span><span class="sxs-lookup"><span data-stu-id="d19e3-113">(The reduction period could also be January 5 to January 15, or any other ten day period).</span></span>

<span data-ttu-id="d19e3-114">Ennfremur, ef **Frá dagsetningu** á stytta tímabilinu er 21. janúar (31 mínus 10) væri hægt að stilla **Til dagsetningar** á hvaða dagsetningu sem er eftir 31. janúar og 10 dagar verða samt sem áður fjarlægðir úr tímabili þóknunarfærslu.</span><span class="sxs-lookup"><span data-stu-id="d19e3-114">Also, if the **From date** on the reduction period is January 21 (31 minus 10), you could set the **To date** to any date after January 31, and 10 days will still be removed from the fee transaction period.</span></span>

## <a name="see-also"></a><span data-ttu-id="d19e3-115">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="d19e3-115">See also</span></span>

[<span data-ttu-id="d19e3-116">Dæmi um minnkunardaga</span><span class="sxs-lookup"><span data-stu-id="d19e3-116">Reduction days example</span></span>](reduction-days-example.md)

  


