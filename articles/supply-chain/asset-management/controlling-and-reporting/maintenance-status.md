---
title: Staða viðhalds
description: Þetta efni útskýrir hvernig á að reikna út stöðu viðhalds í eignastjórnun.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: fbe2b3fd9ce63c34aedb790583dea572d3d9b079
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205473"
---
# <a name="maintenance-status"></a><span data-ttu-id="c81cd-103">Staða viðhalds</span><span class="sxs-lookup"><span data-stu-id="c81cd-103">Maintenance status</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="c81cd-104">Í eignastjórnun er hægt að gera yfirlitsútreikning fyrir tiltekið tímabil yfir nýjar, virkar og fullunnar viðhaldsbeiðnir, verkbeiðnir og aðgerðir niðurtíma vegna viðhalds.</span><span class="sxs-lookup"><span data-stu-id="c81cd-104">In Asset Management, you can make an overview calculation for a specific period for new, active, and completed maintenance requests, work orders, and maintenance downtime activities.</span></span> <span data-ttu-id="c81cd-105">Þú getur einnig séð fjölda lokinna ástandsmatsprófana á sama tímabili.</span><span class="sxs-lookup"><span data-stu-id="c81cd-105">You can also see the number of completed condition assessments for the same period.</span></span> <span data-ttu-id="c81cd-106">Notaðu þennan útreikning til að fá yfirlit yfir vinnuálag fyrir komandi og loknar viðhaldsbeiðnir og verkbeiðnir.</span><span class="sxs-lookup"><span data-stu-id="c81cd-106">Use this calculation to get an overview of workload for incoming and completed maintenance requests and work orders.</span></span>

## <a name="make-a-maintenance-status-calculation"></a><span data-ttu-id="c81cd-107">Gerðu útreikning á viðhaldsstöðu</span><span class="sxs-lookup"><span data-stu-id="c81cd-107">Make a maintenance status calculation</span></span>

1. <span data-ttu-id="c81cd-108">Smelltu á **Eignastýring** > **Fyrirspurnir** > **Staða viðhalds**.</span><span class="sxs-lookup"><span data-stu-id="c81cd-108">Click **Asset management** > **Inquiries** > **Maintenance status**.</span></span>

2. <span data-ttu-id="c81cd-109">Í glugganum **Reikna út stöðu** skaltu velja tímabilið sem þú vilt gera útreikning fyrir í reitunum **Frá dags.** og **Til dags.**.</span><span class="sxs-lookup"><span data-stu-id="c81cd-109">In the **Calculate status** dialog, select the time range that you want to make the calculation in the **From date** and **To date** fields.</span></span>

3. <span data-ttu-id="c81cd-110">Þú getur notað reitinn **Stig** til að gefa til kynna hversu ítarlegar þú vilt að viðhaldslínur séu varðandi virkar staðsetningar.</span><span class="sxs-lookup"><span data-stu-id="c81cd-110">You can use the **Level** field to indicate how detailed you want the maintenance lines to be regarding functional locations.</span></span> 

  <span data-ttu-id="c81cd-111">Til dæmis, ef þú setur inn töluna "1" í reitinn, og þú ert með fjölþrepa skipulag virkrar staðsetningar, verða allar viðhaldsskemalínur fyrir virka staðsetningu sýndar á efsta stigi og því er hægt að leggja saman stöðu á línu frá virkum staðsetningum á lægra stigi.</span><span class="sxs-lookup"><span data-stu-id="c81cd-111">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance lines for a functional location will be shown on the top level, and therefore the status on a line may be added up from functional locations located at a lower level.</span></span> 
  
  <span data-ttu-id="c81cd-112">Ef þú setur töluna „0“ inn í reitinn **Stig** sérðu ítarlegar niðurstöður sem sýna allar viðhaldslínur á öllum virkum staðsetningarstigum sem þær tengjast.</span><span class="sxs-lookup"><span data-stu-id="c81cd-112">If you insert the number "0" in the **Level** field, you see a detailed result showing all maintenance lines on all the functional location levels to which they are related.</span></span>

4. <span data-ttu-id="c81cd-113">Smellið á **Í lagi** til að byrja að reikna.</span><span class="sxs-lookup"><span data-stu-id="c81cd-113">Click **OK** to start the calculation.</span></span>

5. <span data-ttu-id="c81cd-114">Smelltu á hnappana **Flokka eftir** til að sýna nauðsynleg smáatriði við útreikninginn.</span><span class="sxs-lookup"><span data-stu-id="c81cd-114">Click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="c81cd-115">Valdir hnappar **Flokka eftir** eru auðkenndir.</span><span class="sxs-lookup"><span data-stu-id="c81cd-115">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="c81cd-116">Smelltu á hnappinn til að virkjaðu eða afvirkjaðu hann.</span><span class="sxs-lookup"><span data-stu-id="c81cd-116">Click on a button to activate or deactivate it.</span></span>

6. <span data-ttu-id="c81cd-117">Mundu að smella á hnappinn **Uppfæra** til að uppfæra útreikninginn í hvert skipti sem þú gerir breytingar með því að virkja eða afvirkja hnappana **Flokka eftir** eða með því að gera útreikning fyrir nýtt tímabil.</span><span class="sxs-lookup"><span data-stu-id="c81cd-117">Remember to click the **Update** button to update the calculation each time you make changes by activating or deactivating **Group by** buttons, or by making a calculation for a new period.</span></span>

7. <span data-ttu-id="c81cd-118">Smelltu á **Stöðu** ef þú vilt búa til nýjan útreikning á viðhaldsstöðu.</span><span class="sxs-lookup"><span data-stu-id="c81cd-118">Click **Status** if you want to create a new maintenance status calculation.</span></span>

>[!NOTE]
><span data-ttu-id="c81cd-119">Niðurstöðurnar sem eru sýndar í **Staða viðhalds** innihalda aðeins viðhaldsbeiðnir og verkbeiðnir sem hafa raunverulegan upphafsdag og tíma.</span><span class="sxs-lookup"><span data-stu-id="c81cd-119">The results shown in **Maintenance status** only include maintenance requests and work orders that have an actual start date and time.</span></span> <span data-ttu-id="c81cd-120">Lokadagsetning og tími mega vera auður.</span><span class="sxs-lookup"><span data-stu-id="c81cd-120">End date and time may be blank.</span></span>

## <a name="example-1"></a><span data-ttu-id="c81cd-121">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="c81cd-121">Example 1</span></span>

<span data-ttu-id="c81cd-122">Á skjámyndinni hér að neðan hafa hnapparnir **Ár** og **Mánuður** verið virkjaðir.</span><span class="sxs-lookup"><span data-stu-id="c81cd-122">In the screenshot below, the **Year** and **Month** buttons have been activated.</span></span> <span data-ttu-id="c81cd-123">Með hakað í þessa valkosti **Flokka eftir** færðu almennt yfirlit mánaðarlega um vinnuálag og afköst sem tengjast viðhaldsbeiðnum og verkbeiðnum.</span><span class="sxs-lookup"><span data-stu-id="c81cd-123">With these **Group by** options selected, you get a general overview on a monthly basis of workload and throughput related to maintenance requests and work orders.</span></span> 

![Dæmi um mánaðarlegt vinnuálag](media/13-controlling-and-reporting.png)

## <a name="example-2"></a><span data-ttu-id="c81cd-125">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="c81cd-125">Example 2</span></span>

<span data-ttu-id="c81cd-126">Á skjámyndinni hér að neðan hefur upplýsingum um virkar staðsetningar verið bætt við.</span><span class="sxs-lookup"><span data-stu-id="c81cd-126">In the screenshot below, information about functional locations has been added.</span></span> <span data-ttu-id="c81cd-127">Nú er mögulegt að bera saman vinnuálag og afköst milli virkra staðsetninga, sem geta táknað landfræðilega staði, verksmiðjur eða vinnusvæði.</span><span class="sxs-lookup"><span data-stu-id="c81cd-127">Now it is possible to compare workload and throughput across functional locations, which may represent geographical locations, factories, or work areas.</span></span> 

![Dæmi um mánaðarlegt vinnuálag með virkum staðsetningum](media/14-controlling-and-reporting.png)

