---
title: Staða viðhalds
description: Þetta efni útskýrir hvernig á að reikna út stöðu viðhalds í eignastjórnun.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 516607c056125a16e075c33f3c2ad069efb396d9
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918350"
---
# <a name="maintenance-status"></a><span data-ttu-id="77959-103">Staða viðhalds</span><span class="sxs-lookup"><span data-stu-id="77959-103">Maintenance status</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="77959-104">Í eignastjórnun er hægt að gera útreikninga til að sjá yfirlit yfir nýjar, virkar og fullunnar viðhaldsbeiðnir, verkbeiðnir og aðgerðir niðurtíma vegna viðhalds á tilteknu tímabili.</span><span class="sxs-lookup"><span data-stu-id="77959-104">In Asset Management, you can make a calculation to see an overview of new, active, and completed maintenance requests, work orders, and maintenance downtime activities for a specific period.</span></span> <span data-ttu-id="77959-105">Þú getur einnig séð fjölda lokinna ástandsmatsprófana á sama tímabili.</span><span class="sxs-lookup"><span data-stu-id="77959-105">You can also see the number of completed condition assessments for the same period.</span></span> <span data-ttu-id="77959-106">Notaðu þennan útreikning til að fá yfirlit yfir vinnuálag varðandi komandi og loknar viðhaldsbeiðnir og verkbeiðnir.</span><span class="sxs-lookup"><span data-stu-id="77959-106">Use this calculation to get an overview of workload regarding incoming and completed maintenance requests and work orders.</span></span>

## <a name="make-a-maintenance-status-calculation"></a><span data-ttu-id="77959-107">Gerðu útreikning á viðhaldsstöðu</span><span class="sxs-lookup"><span data-stu-id="77959-107">Make a maintenance status calculation</span></span>

1. <span data-ttu-id="77959-108">Smelltu á **Eignastýring** > **Fyrirspurnir** > **Staða viðhalds**.</span><span class="sxs-lookup"><span data-stu-id="77959-108">Click **Asset management** > **Inquiries** > **Maintenance status**.</span></span>

2. <span data-ttu-id="77959-109">Í glugganum **Reikna út stöðu** skaltu velja tímabiliði sem þú vilt gera útreikning fyrir í reitunum **Frá dags.** og **Til dags.**.</span><span class="sxs-lookup"><span data-stu-id="77959-109">In the **Calculate status** dialog, select the period for which you want to make the calculation in the **From date** and **To date** fields.</span></span>

3. <span data-ttu-id="77959-110">Þú getur notað reitinn **Stig** til að gefa til kynna hversu ítarlegar þú vilt að viðhaldslínur séu varðandi virkar staðsetningar.</span><span class="sxs-lookup"><span data-stu-id="77959-110">You can use the **Level** field to indicate how detailed you want the maintenance lines to be regarding functional locations.</span></span> <span data-ttu-id="77959-111">Til dæmis, ef þú setur inn töluna "1" í reitinn, og þú ert með fjölþrepa skipulag virkrar staðsetningar, verða allar viðhaldsskemalínur fyrir virka staðsetningu sýndar á efsta stigi og því er hægt að leggja saman stöðu á línu frá virkum staðsetningum á lægra stigi.</span><span class="sxs-lookup"><span data-stu-id="77959-111">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance lines for a functional location will be shown on the top level, and therefore the status on a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="77959-112">Ef þú setur töluna „0“ inn í reitinn **Stig** sérðu ítarlegar niðurstöður sem sýna allar viðhaldslínur á öllum virkum staðsetningarstigum sem þær tengjast.</span><span class="sxs-lookup"><span data-stu-id="77959-112">If you insert the number "0" in the **Level** field, you see a detailed result showing all maintenance lines on all the functional location levels to which they are related.</span></span>

4. <span data-ttu-id="77959-113">Smellið á **Í lagi** til að byrja að reikna.</span><span class="sxs-lookup"><span data-stu-id="77959-113">Click **OK** to start the calculation.</span></span>

5. <span data-ttu-id="77959-114">Í aðgerðarrúðahópunum **Flokka eftir...** smellirðu á viðeigandi hnappa til að sýna nauðsynleg smáatriði við útreikninginn.</span><span class="sxs-lookup"><span data-stu-id="77959-114">In the **Group by...** action pane groups, click the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="77959-115">Valdir aðgerðarrúðahnappar eru auðkenndir.</span><span class="sxs-lookup"><span data-stu-id="77959-115">The selected action pane buttons are highlighted.</span></span> <span data-ttu-id="77959-116">Smelltu á hnappinn til að virkjaðu eða afvirkjaðu hann.</span><span class="sxs-lookup"><span data-stu-id="77959-116">Click on a button to activate or deactivate it.</span></span>

6. <span data-ttu-id="77959-117">Mundu að smella á hnappinn **Uppfæra** til að uppfæra útreikninginn í hvert skipti sem þú gerir breytingar með því að virkja eða afvirkja hnappana **Flokka eftir...** eða með því að gera útreikning fyrir nýtt tímabil.</span><span class="sxs-lookup"><span data-stu-id="77959-117">Remember to click the **Update** button to update the calculation each time you make changes by activating or deactivating **Group by...** buttons, or by making a calculation for a new period.</span></span>

7. <span data-ttu-id="77959-118">Smelltu á **Stöðu** ef þú vilt búa til nýjan útreikning á viðhaldsstöðu.</span><span class="sxs-lookup"><span data-stu-id="77959-118">Click **Status** if you want to create a new maintenance status calculation.</span></span>

>[!NOTE]
><span data-ttu-id="77959-119">Niðurstöðurnar sem eru sýndar í **Staða viðhalds** innihalda aðeins viðhaldsbeiðnir og verkbeiðnir sem hafa raunverulegan upphafsdag og tíma.</span><span class="sxs-lookup"><span data-stu-id="77959-119">The results shown in **Maintenance status** only include maintenance requests and work orders that have an actual start date and time.</span></span> <span data-ttu-id="77959-120">Lokadagsetning og tími mega vera auður.</span><span class="sxs-lookup"><span data-stu-id="77959-120">End date and time may be blank.</span></span>

<span data-ttu-id="77959-121">*Dæmi 1:*</span><span class="sxs-lookup"><span data-stu-id="77959-121">*Example 1:*</span></span>

<span data-ttu-id="77959-122">Á myndinni hér að neðan hafa hnapparnir **Ár** og **Mánuður** verið virkjaðir.</span><span class="sxs-lookup"><span data-stu-id="77959-122">In the figure below, the **Year** and **Month** buttons have been activated.</span></span> <span data-ttu-id="77959-123">Hér færðu almennt yfirlit mánaðarlega um vinnuálag og afköst sem tengjast viðhaldsbeiðnum og verkbeiðnum.</span><span class="sxs-lookup"><span data-stu-id="77959-123">Here, you get a general overview on a monthly basis of workload and throughput related to maintenance requests and work orders.</span></span> 

![Mynd 1](media/13-controlling-and-reporting.png)

<span data-ttu-id="77959-125">*Dæmi 2:*</span><span class="sxs-lookup"><span data-stu-id="77959-125">*Example 2:*</span></span>

<span data-ttu-id="77959-126">Á myndinni hér að neðan hefur upplýsingum um virkar staðsetningar verið bætt við.</span><span class="sxs-lookup"><span data-stu-id="77959-126">In the figure below, information about functional locations has been added.</span></span> <span data-ttu-id="77959-127">Nú er mögulegt að bera saman vinnuálag og afköst milli virkra staðsetninga, sem geta táknað landfræðilega staði, verksmiðjur eða vinnusvæði.</span><span class="sxs-lookup"><span data-stu-id="77959-127">Now, it is possible to compare workload and throughput across functional locations, which may represent geographical locations, factories, or work areas.</span></span> 

![Mynd 2](media/14-controlling-and-reporting.png)

