---
title: Reikna vöruspá
description: Þetta efni útskýrir hvernig á að reikna út vöruspá í eignastýringu.
author: josaw1
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetItemForecast
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f8f38ac7bfb270f648cd561da50ee5477721ab47
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430450"
---
# <a name="calculate-item-forecast"></a><span data-ttu-id="98362-103">Reikna vöruspá</span><span class="sxs-lookup"><span data-stu-id="98362-103">Calculate item forecast</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="98362-104">Rétt eins og þú getur gert útreikninga á álagi, sem lýst er í fyrri hlutanum, geturðu einnig gert vöruspárútreikninga á:</span><span class="sxs-lookup"><span data-stu-id="98362-104">Just as you can make capacity load calculations, which are described in the previous section, you can also make item forecast calculations on:</span></span>

- <span data-ttu-id="98362-105">áætlunarlínur viðhalds</span><span class="sxs-lookup"><span data-stu-id="98362-105">maintenance schedule lines</span></span>  
- <span data-ttu-id="98362-106">verkbeiðnir sem hafa ekki enn verið áætlaðar</span><span class="sxs-lookup"><span data-stu-id="98362-106">work orders that have not yet been scheduled</span></span>  
- <span data-ttu-id="98362-107">áætlaðar verkbeiðnir</span><span class="sxs-lookup"><span data-stu-id="98362-107">scheduled work orders</span></span>

<span data-ttu-id="98362-108">Þetta er gagnlegt ef þú vilt fá yfirsýn yfir væntanlega notkun vöru (varahluti sem og aðrar vörur sem þarf til að ljúka verkbeiðnum) fyrir tiltekið tímabil.</span><span class="sxs-lookup"><span data-stu-id="98362-108">This is useful if you want to get an overview of expected item consumption (spare parts as well as other items required for completing work orders) for a specific period.</span></span> <span data-ttu-id="98362-109">Hægt er að gera útreikning á vöruspá á allar eignir eða valdar eignir.</span><span class="sxs-lookup"><span data-stu-id="98362-109">Calculation of item forecast can be done on all assets or selected assets.</span></span> <span data-ttu-id="98362-110">Þú getur líka gert útreikninga á aðgerðum niðurtíma vegna viðhalds (**Allar aðgerðir niðurtíma vegna viðhalds** eða **Aðgerðir virks niðurtíma vegna viðhalds**) eða í verkbeiðnasafni (**Öll verkbeiðnasöfn** eða **Virk verkbeiðnasöfn**).</span><span class="sxs-lookup"><span data-stu-id="98362-110">You can also make a calculation on a maintenance downtime activity (**All maintenance downtime activities** or **Active maintenance downtime activities**), or on a work order pool (**All work order pools** or **Active work order pools**).</span></span>

1. <span data-ttu-id="98362-111">Smelltu á **Eignastýringu** > **Fyrirspurnir** > **Vöruspá**, eða **Eignastýring** > **Sameiginlegt** > **Verkbeiðnihópar** > **Allir verkbeiðnihópar** / **Virkir verkbeiðnihópar** > veldu verkbeiðnihóp af listanum > hnappinum **Vöruspá**, eða **Eignastýringu** > **Sameiginlegt** > **Niðurtími vegna viðhalds** > **Allur niðurtími vegna viðhalds** / **Virkur niðurtími vegna viðhalds** > veldu niðurtímaaðgerðir vegna viðhalds á listanum > hnappnum **Vöruspá**.</span><span class="sxs-lookup"><span data-stu-id="98362-111">Click **Asset management** > **Inquiries** > **Item forecast**, or **Asset management** > **Common** > **Work order pools** > **All work order pools** / **Active work order pools** > select work order pool in the list > **Item forecast** button, or **Asset management** > **Common** > **Maintenance downtime activities** > **All maintenance downtime activities** / **Active maintenance downtime activities** > select maintenance downtime activity in the list > **Item forecast** button.</span></span>

2. <span data-ttu-id="98362-112">Í glugganum **Reikna vöruspá** velurðu tímabil fyrir útreikninginn í reitunum **Upphafsdagsetning/-tími** og **Lokadagsetning/-tími**.</span><span class="sxs-lookup"><span data-stu-id="98362-112">In the **Calculate item forecast** dialog, select a period for the calculation in the **Start date/time** and **End date/time** fields.</span></span>

3. <span data-ttu-id="98362-113">Veldu „Já“ á skiptihnappnum **Hafa viðhaldsskema með** ef þú vilt láta viðhaldsskemalínur fylgja með í vöruspárútreikningnum.</span><span class="sxs-lookup"><span data-stu-id="98362-113">Select "Yes" on the **Include maintenance schedule** toggle button if you want to include maintenance schedule lines in the forecast calculation.</span></span>

4. <span data-ttu-id="98362-114">Veldu „Já“ á skiptihnappnum **Hafa verkbeiðni með** ef þú vilt láta verkbeiðnivinnslur fylgja með í spárútreikningnum.</span><span class="sxs-lookup"><span data-stu-id="98362-114">Select "Yes" on the **Include work order** toggle button if you want to include work order jobs in the forecast calculation.</span></span>

5. <span data-ttu-id="98362-115">Þú getur notað reitinn **Stig** til að gefa til kynna hversu ítarlegar þú vilt að vöruspárlínur séu varðandi virkar staðsetningar.</span><span class="sxs-lookup"><span data-stu-id="98362-115">You can use the **Level** field to indicate how detailed you want the item forecast lines to be regarding functional locations.</span></span> 

      <span data-ttu-id="98362-116">Til dæmis, ef þú setur inn töluna "1" í reitinn, og þú ert með fjölþrepa skipulag virkrar staðsetningar, verða allar viðhaldsskemalínur og verkbeiðnir fyrir virka staðsetningu sýndar á efsta stigi og því er hægt að leggja saman klukkustundirnar á línu frá virkum staðsetningum á lægra stigi.</span><span class="sxs-lookup"><span data-stu-id="98362-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance schedule lines and work orders for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
  
      <span data-ttu-id="98362-117">Ef þú setur töluna „0“ inn í reitinn **Stig** muntu sjá ítarlega niðurstöður sem sýna allar viðhaldsskemalínur og allar verkbeiðnir á öllum virkum staðsetningarstigum sem þær tengjast.</span><span class="sxs-lookup"><span data-stu-id="98362-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all maintenance schedule lines and all work orders on all the functional location level to which they are related.</span></span>

6. <span data-ttu-id="98362-118">Smellið á **Í lagi** til að byrja að reikna.</span><span class="sxs-lookup"><span data-stu-id="98362-118">Click **OK** to start the calculation.</span></span>

7. <span data-ttu-id="98362-119">Í hópunum **Flokka eftir...** smellirðu á viðeigandi hnappa til að sýna nauðsynleg smáatriði við útreikninginn.</span><span class="sxs-lookup"><span data-stu-id="98362-119">In the **Group by...** groups, click the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="98362-120">Í skjámyndinni hér að neðan eru valdir hnappar **Flokka eftir** auðkenndir með bláum lit.</span><span class="sxs-lookup"><span data-stu-id="98362-120">In the screenshot below, the selected **Group by** buttons are highlighted in blue color.</span></span> <span data-ttu-id="98362-121">Smelltu á hnappinn til að virkjaðu eða afvirkjaðu hann.</span><span class="sxs-lookup"><span data-stu-id="98362-121">Click on a button to activate or deactivate it.</span></span>

8. <span data-ttu-id="98362-122">Smelltu á hnappinn **Sýna víddir** ef þú vilt sjá afurð, geymslu eða rakningarvíddir sem tengjast vörunum.</span><span class="sxs-lookup"><span data-stu-id="98362-122">Click the **Display dimensions** button if you want to see the product, storage, or tracking dimensions related to the items.</span></span> <span data-ttu-id="98362-123">Veldu viðeigandi gátreiti og smelltu á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="98362-123">Select the relevant check boxes, and click **OK**.</span></span>

![Mynd 1](media/02-capacity-planning.png)
