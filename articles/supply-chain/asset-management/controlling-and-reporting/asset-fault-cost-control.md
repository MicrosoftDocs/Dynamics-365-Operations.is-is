---
title: Kostnaðarstýring eignavillu
description: Þetta efni skýrir kostnaðarstýringu eignabilunar í eignastýringu.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetCostControlFault
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c25b3efbd0f2f0ec22a08aeac54ffb7fd9398c83
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253831"
---
# <a name="asset-fault-cost-control"></a><span data-ttu-id="08355-103">Kostnaðarstýring eignavillu</span><span class="sxs-lookup"><span data-stu-id="08355-103">Asset fault cost control</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="08355-104">Í eignastýringu er hægt að reikna út kostnað vegna skráningar á eignabilunum til að fá yfirlit yfir raunkostnað miðað við kostnað fjárhagsáætlunar.</span><span class="sxs-lookup"><span data-stu-id="08355-104">In Asset Management, you can calculate costs on asset fault registrations to get an overview of actual costs compared to budget costs.</span></span> <span data-ttu-id="08355-105">Raunkostnaður byggist á bókfærðum færslum.</span><span class="sxs-lookup"><span data-stu-id="08355-105">Actual costs are based on posted transactions.</span></span> <span data-ttu-id="08355-106">Dagsetningin er bilunardagsetningin sem einkennið var skráð á.</span><span class="sxs-lookup"><span data-stu-id="08355-106">The date is the fault date on which the symptom was recorded.</span></span>

1. <span data-ttu-id="08355-107">Smelltu á **Eignastýringu** > **Fyrirspurnir** > **Bilun eignar** > **Kostnaðarstýringu eignabilunar**.</span><span class="sxs-lookup"><span data-stu-id="08355-107">Click **Asset management** > **Inquiries** > **Asset fault** > **Asset fault cost control**.</span></span>

2. <span data-ttu-id="08355-108">Í valmyndinni **Kostnaðarstýring eignabilunar** velurðu fjárhagsvídd sem sett er inn í útreikninginn, ef þess þarf.</span><span class="sxs-lookup"><span data-stu-id="08355-108">In the **Asset fault cost control** dialog, select a financial dimension set to be included in the calculation, if required.</span></span>

4. <span data-ttu-id="08355-109">Veldu „Já“ á skiptihnappnum **Sleppa núlli** ef þú vilt ekki sýna niðurstöður með kostnað við núll.</span><span class="sxs-lookup"><span data-stu-id="08355-109">Select "Yes" on the **Skip zero** toggle button if you don't want to show results with a cost of zero.</span></span>

5. <span data-ttu-id="08355-110">Þú getur notað reitinn **Stig** til að gefa til kynna hversu ítarlegar þú vilt að kostnaðarstýringarlínur séu varðandi virkar staðsetningar.</span><span class="sxs-lookup"><span data-stu-id="08355-110">You can use the **Level** field to indicate how detailed you want the cost control lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="08355-111">Til dæmis, ef þú setur inn töluna "1" í reitinn, og þú ert með fjölþrepa skipulag virkrar staðsetningar, verða allar kostnaðarstýringarlínur eignabilunar fyrir virka staðsetningu sýndar á efsta stigi og því er hægt að leggja saman klukkustundirnar á línu frá virkum staðsetningum á lægra stigi.</span><span class="sxs-lookup"><span data-stu-id="08355-111">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all asset fault cost control lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
    
    <span data-ttu-id="08355-112">Ef þú setur töluna „0“ inn í reitinn **Stig** muntu sjá ítarlega niðurstöður sem sýna allar kostnaðarstýringarlínur eignabilana á öllum virkum staðsetningarstigum sem þær tengjast.</span><span class="sxs-lookup"><span data-stu-id="08355-112">If you insert the number "0" in the **Level** field, you will see a detailed result showing all asset fault cost control lines on all the functional location levels to which they are related.</span></span>

6. <span data-ttu-id="08355-113">Ef þú vilt takmarka leitina geturðu valið sérstakar eignir, bilunardagsetningar og bilunarástæður á flýtiflipanum **Færslur til að taka með**.</span><span class="sxs-lookup"><span data-stu-id="08355-113">If you want to limit the search, you can select specific assets, fault dates, and fault causes on the **Records to include** FastTab.</span></span>

7. <span data-ttu-id="08355-114">Smellið á **Í lagi** til að byrja að reikna.</span><span class="sxs-lookup"><span data-stu-id="08355-114">Click **OK** to start the calculation.</span></span>

8. <span data-ttu-id="08355-115">Smelltu á hnappana **Flokka eftir** til að sýna nauðsynleg smáatriði við útreikninginn.</span><span class="sxs-lookup"><span data-stu-id="08355-115">Click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="08355-116">Valdir hnappar **Flokka eftir** eru auðkenndir.</span><span class="sxs-lookup"><span data-stu-id="08355-116">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="08355-117">Smelltu á hnappinn til að virkjaðu eða afvirkjaðu hann.</span><span class="sxs-lookup"><span data-stu-id="08355-117">Click on a button to activate or deactivate it.</span></span>

## <a name="example"></a><span data-ttu-id="08355-118">Dæmi</span><span class="sxs-lookup"><span data-stu-id="08355-118">Example</span></span>

<span data-ttu-id="08355-119">Þetta dæmi sýnir útreikning á kostnaðarstýringu eignabilunar.</span><span class="sxs-lookup"><span data-stu-id="08355-119">This example shows an asset fault cost control calculation.</span></span>

- <span data-ttu-id="08355-120">Reiturinn **Upprunaleg fjárhagsáætlun** sýnir fjárhagsáætlunarkostnað vegna kostnaðar við spá um verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="08355-120">The **Original budget** field shows budget costs from the work order forecast.</span></span> 
- <span data-ttu-id="08355-121">Reiturinn **Raunkostnaður** sýnir bókaðan kostnað vegna verkbeiðna.</span><span class="sxs-lookup"><span data-stu-id="08355-121">The **Actual cost** field shows posted costs on work orders.</span></span> 
- <span data-ttu-id="08355-122">Reiturinn **Ráðstafaður kostnaður** sýnir heildarkostnað sem fyrirtækið þitt skuldbindur sig til vegna verkbeiðna.</span><span class="sxs-lookup"><span data-stu-id="08355-122">The **Committed cost** field shows total costs that your company is committed to in relation to work orders.</span></span>

    ![Mynd 1](media/05-controlling-and-reporting.png)

<span data-ttu-id="08355-124">Upplýsingar um hvernig setja skuli upp bilanir er að finna í efnisatriðinu [Bilanastjórnun](../setup-for-work-orders/fault-management.md).</span><span class="sxs-lookup"><span data-stu-id="08355-124">For information about how to set up faults, see the [Fault management](../setup-for-work-orders/fault-management.md) topic.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]