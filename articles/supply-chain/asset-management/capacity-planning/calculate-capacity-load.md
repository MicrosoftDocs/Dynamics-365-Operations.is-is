---
title: Reikna álag
description: Þetta efni útskýrir hvernig á að reikna út álag í eignastýringu.
author: josaw1
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetCapacityLoad, EntAssetWorkOrderCapacityLoadCalculate, EntAssetWorkOrderCapacityLoad
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5015955338a4cbc2b51585d6297756f20dccee8b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430451"
---
# <a name="calculate-capacity-load"></a><span data-ttu-id="a0696-103">Reikna álag</span><span class="sxs-lookup"><span data-stu-id="a0696-103">Calculate capacity load</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="a0696-104">Í eignastjórnun geturðu reiknað út álag á:</span><span class="sxs-lookup"><span data-stu-id="a0696-104">In Asset Management, you can calculate capacity load on:</span></span>

- <span data-ttu-id="a0696-105">áætlunarlínur viðhalds</span><span class="sxs-lookup"><span data-stu-id="a0696-105">maintenance schedule lines</span></span>  
- <span data-ttu-id="a0696-106">verkbeiðnir sem hafa ekki enn verið áætlaðar</span><span class="sxs-lookup"><span data-stu-id="a0696-106">work orders that have not yet been scheduled</span></span>  
- <span data-ttu-id="a0696-107">áætlaðar verkbeiðnir</span><span class="sxs-lookup"><span data-stu-id="a0696-107">scheduled work orders</span></span>

<span data-ttu-id="a0696-108">Þetta er gagnlegt ef þú vilt fá yfirsýn yfir áætlað álag yfir ákveðið tímabil.</span><span class="sxs-lookup"><span data-stu-id="a0696-108">This is useful if you want to get an overview of expected capacity load for a specific period.</span></span> <span data-ttu-id="a0696-109">Hægt er að gera útreikning á álagi á allar eignir eða valdar eignir.</span><span class="sxs-lookup"><span data-stu-id="a0696-109">Calculation of capacity load can be done on all assets or selected assets.</span></span> <span data-ttu-id="a0696-110">Þú getur líka gert útreikning á aðgerðum niðurtíma vegna viðhalds eða verkbeiðnahópum.</span><span class="sxs-lookup"><span data-stu-id="a0696-110">You can also make a calculation on maintenance downtime activities or work order pools.</span></span>

1. <span data-ttu-id="a0696-111">Smelltu á **Eignastýringu** > **Fyrirspurnir** > **Álag**, eða **Eignastýring** > **Sameiginlegt** > **Verkbeiðnihópar** > **Allir verkbeiðnihópar** / **Virkir verkbeiðnihópar** > veldu verkbeiðnihóp af listanum > hnappinum **Álag**, eða **Eignastýringu** > **Sameiginlegt** > **Niðurtími vegna viðhalds** > **Allur niðurtími vegna viðhalds** / **Virkur niðurtími vegna viðhalds** > veldu viðhaldsaðgerðir á listanum > hnappnum **Álag**.</span><span class="sxs-lookup"><span data-stu-id="a0696-111">Click **Asset management** > **Inquiries** > **Capacity load**, or **Asset management** > **Common** > **Work order pools** > **All work order pools** / **Active work order pools** > select work order pool in the list > **Capacity load** button, or **Asset management** > **Common** > **Maintenance downtime activities** > **All maintenance downtime activities** / **Active maintenance downtime activities** > select maintenance activity in the list > **Capacity load** button.</span></span>

2. <span data-ttu-id="a0696-112">Í glugganum **Reikna álag** velurðu tímabil fyrir útreikninginn í reitunum **Upphafsdagsetning/-tími** og **Lokadagsetning/-tími**.</span><span class="sxs-lookup"><span data-stu-id="a0696-112">In the **Calculate capacity load** dialog, select a period for the calculation in the **Start date/time** and **End date/time** fields.</span></span>

3. <span data-ttu-id="a0696-113">Veldu „Já“ á skiptihnappnum **Hafa viðhaldsskema með** ef þú vilt láta viðhaldsskemalínur fylgja með í útreikningnum.</span><span class="sxs-lookup"><span data-stu-id="a0696-113">Select "Yes" on the **Include maintenance schedule** toggle button if you want to include maintenance schedule lines in the calculation.</span></span>

4. <span data-ttu-id="a0696-114">Veldu „Já“ á skiptihnappnum **Hafa verkbeiðni með** ef þú vilt láta verkbeiðnivinnslur fylgja með í útreikningnum.</span><span class="sxs-lookup"><span data-stu-id="a0696-114">Select "Yes" on the **Include work order** toggle button if you want to include work order jobs in the calculation.</span></span>

5. <span data-ttu-id="a0696-115">Þú getur notað reitinn **Stig** til að gefa til kynna hversu ítarlegar þú vilt að álagslínur séu varðandi virkar staðsetningar.</span><span class="sxs-lookup"><span data-stu-id="a0696-115">You can use the **Level** field to indicate how detailed you want the capacity load lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="a0696-116">Til dæmis, ef þú setur inn töluna "1" í reitinn, og þú ert með fjölþrepa skipulag virkrar staðsetningar, verða allar viðhaldsskemalínur og verkbeiðnir fyrir virka staðsetningu sýndar á efsta stigi og því er hægt að leggja saman klukkustundirnar á línu frá virkum staðsetningum á lægra stigi.</span><span class="sxs-lookup"><span data-stu-id="a0696-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance schedule lines and work orders for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
    
    <span data-ttu-id="a0696-117">Ef þú setur töluna „0“ inn í reitinn **Stig** muntu sjá ítarlega niðurstöður sem sýna allar viðhaldsskemalínur og allar verkbeiðnir á öllum virkum staðsetningarstigum sem þær tengjast.</span><span class="sxs-lookup"><span data-stu-id="a0696-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all maintenance schedule lines and all work orders on all the functional location levels to which they are related.</span></span>

6. <span data-ttu-id="a0696-118">Smellið á **Í lagi** til að byrja að reikna.</span><span class="sxs-lookup"><span data-stu-id="a0696-118">Click **OK** to start the calculation.</span></span>

7. <span data-ttu-id="a0696-119">Í hópunum **Flokka eftir...** smellirðu á viðeigandi hnappa til að sýna nauðsynleg smáatriði við útreikninginn.</span><span class="sxs-lookup"><span data-stu-id="a0696-119">In the **Group by...** groups, click the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="a0696-120">Í skjámyndinni hér að neðan eru valdir hnappar **Flokka eftir** auðkenndir með bláum lit.</span><span class="sxs-lookup"><span data-stu-id="a0696-120">In the screenshot below, the selected **Group by** buttons are highlighted in blue color.</span></span> <span data-ttu-id="a0696-121">Smelltu á hnappinn til að virkjaðu eða afvirkjaðu hann.</span><span class="sxs-lookup"><span data-stu-id="a0696-121">Click on a button to activate or deactivate it.</span></span>

    ![Mynd 1](media/01-capacity-planning.png)

>[!NOTE]
><span data-ttu-id="a0696-123">Ef þú vilt einbeita þér aðeins að afkastagetuáætlun varðandi áætlaðar verkbeiðnir skal sjá [Reikna álag á áætlaðar verkbeiðnir](../work-order-scheduling/calculate-capacity-load-on-scheduled-work-orders.md).</span><span class="sxs-lookup"><span data-stu-id="a0696-123">If you want to focus only on capacity planning regarding scheduled work orders, see [Calculate capacity load on scheduled work orders](../work-order-scheduling/calculate-capacity-load-on-scheduled-work-orders.md).</span></span>

