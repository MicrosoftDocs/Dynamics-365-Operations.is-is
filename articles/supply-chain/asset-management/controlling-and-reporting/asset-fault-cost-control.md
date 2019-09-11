---
title: Kostnaðarstýring eignavillu
description: Þetta efni skýrir kostnaðarstýringu eignabilunar í eignastýringu.
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
ms.openlocfilehash: 2fe75c327cdc2bdd76173430ed551895f5941c7b
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918304"
---
# <a name="asset-fault-cost-control"></a><span data-ttu-id="239e0-103">Kostnaðarstýring eignavillu</span><span class="sxs-lookup"><span data-stu-id="239e0-103">Asset fault cost control</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="239e0-104">Í eignastýringu er hægt að reikna út kostnað vegna skráningar á eignabilunum til að fá yfirlit yfir raunkostnað miðað við kostnað fjárhagsáætlunar vegna bilunar.</span><span class="sxs-lookup"><span data-stu-id="239e0-104">In Asset Management, you can calculate costs on asset fault registrations to get an overview of actual costs compared to budget costs on faults.</span></span> <span data-ttu-id="239e0-105">Raunkostnaður byggist á bókfærðum færslum.</span><span class="sxs-lookup"><span data-stu-id="239e0-105">Actual costs are based on posted transactions.</span></span> <span data-ttu-id="239e0-106">Dagsetningin er bilunardagsetningin sem einkennið var skráð á.</span><span class="sxs-lookup"><span data-stu-id="239e0-106">The date is the fault date on which the symptom was recorded.</span></span>

1. <span data-ttu-id="239e0-107">Smelltu á **Eignastýringu** > **Fyrirspurnir** > **Bilun eignar** > **Kostnaðarstýringu eignabilunar**.</span><span class="sxs-lookup"><span data-stu-id="239e0-107">Click **Asset management** > **Inquiries** > **Asset fault** > **Asset fault cost control**.</span></span>

2. <span data-ttu-id="239e0-108">Í valmyndinni **Kostnaðarstýring eignabilunar** velurðu fjárhagsvídd sem sett er inn í útreikninginn, ef þess þarf.</span><span class="sxs-lookup"><span data-stu-id="239e0-108">In the **Asset fault cost control** dialog, select a financial dimension set to be included in the calculation, if required.</span></span>

4. <span data-ttu-id="239e0-109">Veldu „Já“ á skiptihnappnum **Sleppa núlli** ef þú vilt ekki sýna niðurstöður með kostnað við núll.</span><span class="sxs-lookup"><span data-stu-id="239e0-109">Select "Yes" on the **Skip zero** toggle button if you don't want to show results with a cost of zero.</span></span>

5. <span data-ttu-id="239e0-110">Þú getur notað reitinn **Stig** til að gefa til kynna hversu ítarlegar þú vilt að kostnaðarstýringarlínur séu varðandi virkar staðsetningar.</span><span class="sxs-lookup"><span data-stu-id="239e0-110">You can use the **Level** field to indicate how detailed you want the cost control lines to be regarding functional locations.</span></span> <span data-ttu-id="239e0-111">Til dæmis, ef þú setur inn töluna "1" í reitinn, og þú ert með fjölþrepa skipulag virkrar staðsetningar, verða allar kostnaðarstýringarlínur eignabilunar fyrir virka staðsetningu sýndar á efsta stigi og því er hægt að leggja saman klukkustundirnar á línu frá virkum staðsetningum á lægra stigi.</span><span class="sxs-lookup"><span data-stu-id="239e0-111">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all asset fault cost control lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="239e0-112">Ef þú setur töluna „0“ inn í reitinn **Stig** muntu sjá ítarlega niðurstöður sem sýna allar kostnaðarstýringarlínur eignabilana á öllum virkum staðsetningarstigum sem þær tengjast.</span><span class="sxs-lookup"><span data-stu-id="239e0-112">If you insert the number "0" in the **Level** field, you will see a detailed result showing all asset fault cost control lines on all the functional location levels to which they are related.</span></span>

6. <span data-ttu-id="239e0-113">Ef þú vilt takmarka leitina geturðu valið sérstakar eignir, bilunardagsetningar og bilunarástæður á flýtiflipanum **Færslur til að taka með**.</span><span class="sxs-lookup"><span data-stu-id="239e0-113">If you want to limit the search, you can select specific assets, fault dates, and fault causes on the **Records to include** FastTab.</span></span>

7. <span data-ttu-id="239e0-114">Smellið á **Í lagi** til að byrja að reikna.</span><span class="sxs-lookup"><span data-stu-id="239e0-114">Click **OK** to start the calculation.</span></span>

8. <span data-ttu-id="239e0-115">Í aðgerðarrúðahópunum **Flokka eftir...** smellirðu á viðeigandi hnappa til að sýna nauðsynleg smáatriði við útreikninginn.</span><span class="sxs-lookup"><span data-stu-id="239e0-115">In the **Group by...** action pane groups, click the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="239e0-116">Valdir aðgerðarrúðahnappar eru auðkenndir.</span><span class="sxs-lookup"><span data-stu-id="239e0-116">The selected action pane buttons are highlighted.</span></span> <span data-ttu-id="239e0-117">Smelltu á hnappinn til að virkjaðu eða afvirkjaðu hann.</span><span class="sxs-lookup"><span data-stu-id="239e0-117">Click on a button to activate or deactivate it.</span></span>

<span data-ttu-id="239e0-118">Myndin hér að neðan sýnir dæmi um útreikning á kostnaðarstýringu eigna vegna villu.</span><span class="sxs-lookup"><span data-stu-id="239e0-118">The figure below shows an example of an asset fault cost control calculation.</span></span>

![Mynd 1](media/05-controlling-and-reporting.png)

<span data-ttu-id="239e0-120">Sjá kaflann [Bilanastjórnun](../setup-for-work-orders/fault-management.md) til að fá upplýsingar um hvernig á að setja upp bilanir.</span><span class="sxs-lookup"><span data-stu-id="239e0-120">Refer to the [Fault management](../setup-for-work-orders/fault-management.md) section for information on how to set up faults.</span></span>

>[!NOTE]
><span data-ttu-id="239e0-121">Reiturinn **Upprunaleg fjárhagsáætlun** sýnir fjárhagsáætlunarkostnað vegna kostnaðar við spá um verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="239e0-121">The **Original budget** field shows budget costs from the work order forecast.</span></span> <span data-ttu-id="239e0-122">Reiturinn **Raunkostnaður** sýnir bókaðan kostnað vegna verkbeiðna.</span><span class="sxs-lookup"><span data-stu-id="239e0-122">The **Actual cost** field shows posted costs on work orders.</span></span> <span data-ttu-id="239e0-123">Reiturinn **Ráðstafaður kostnaður** sýnir heildarkostnað sem fyrirtækið þitt skuldbindur sig til vegna verkbeiðna.</span><span class="sxs-lookup"><span data-stu-id="239e0-123">The **Committed cost** field shows total costs that your company is committed to in relation to work orders.</span></span>

