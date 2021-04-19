---
title: Reikna álag á áætlaðar verkbeiðnir
description: Þetta efni útskýrir hvernig á að reikna út álag á áætlaðar verkbeiðnir í eignastjórnun.
author: johanhoffmann
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 09e0fc17a288a278b7b1feaba8c7b73425aa2d52
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808161"
---
# <a name="calculate-capacity-load-on-scheduled-work-orders"></a><span data-ttu-id="d8da4-103">Reikna álag á áætlaðar verkbeiðnir</span><span class="sxs-lookup"><span data-stu-id="d8da4-103">Calculate capacity load on scheduled work orders</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="d8da4-104">Hægt er að reikna út álag á áætlaðar verkbeiðnir til að fá yfirsýn yfir vinnuálag á tilföng fyrir tiltekið tímabil.</span><span class="sxs-lookup"><span data-stu-id="d8da4-104">You can calculate capacity load on scheduled work orders to get an overview of the work load on resources for a specific period.</span></span> <span data-ttu-id="d8da4-105">Hægt er að reikna út fyrir eftirfarandi úrræði: Viðhaldsstarfsmenn, starfsmannahópa, verkfæri og eignir.</span><span class="sxs-lookup"><span data-stu-id="d8da4-105">Calculations can be made for the following resources: Maintenance workers, worker groups, tools, and assets.</span></span>

1. <span data-ttu-id="d8da4-106">Smelltu á **Eignastýringu** > **Fyrirspurnir** > **Áætlun** > **Álag**.</span><span class="sxs-lookup"><span data-stu-id="d8da4-106">Click **Asset management** > **Inquiries** > **Schedule** > **Capacity load**.</span></span>

2. <span data-ttu-id="d8da4-107">Í valmyndinni **Reikna álag** > reitnum **Sýna** velurðu hvaða álagsgerð þú vilt reikna út: **Afkastageta**, **Frátekið** eða **Eftirstöðvar**.</span><span class="sxs-lookup"><span data-stu-id="d8da4-107">In the **Calculate capacity load** dialog > **Show** field, select which load type you want to calculate: **Capacity**, **Reserved**, or **Remainder**.</span></span>

3. <span data-ttu-id="d8da4-108">Veldu **Já** á skiptihnappnum **Sleppa núlli** ef þú vilt ekki sýna niðurstöður með núlli.</span><span class="sxs-lookup"><span data-stu-id="d8da4-108">Select **Yes** on the **Skip zero** toggle button if you do not want to show results containing zero.</span></span>

4. <span data-ttu-id="d8da4-109">Veldu tilfangagerðirnar sem þú vilt reikna út álag fyrir með því að velja **Já** á viðeigandi skiptihnöppum: **Starfskraftur**, **Hópur viðhaldsstarfsmanna**, **Verkfæri** og **Eignir**.</span><span class="sxs-lookup"><span data-stu-id="d8da4-109">Select the resource types for which you want to calculate capacity load by selecting **Yes** on the relevant toggle buttons: **Worker**, **Maintenance worker group**, **Tool**, and **Asset**.</span></span>

5. <span data-ttu-id="d8da4-110">Veldu upphafsdagsetningu fyrir útreikning í reitnum **Frá dagsetningu**.</span><span class="sxs-lookup"><span data-stu-id="d8da4-110">Select the start date for the calculation in the **From date** field.</span></span>

6. <span data-ttu-id="d8da4-111">Í reitnum **Gerð millibils** velurðu bilið fyrir útreikninginn: **Dagur**, **Vika**, **Mánuður** eða **Ársfjórðungur**.</span><span class="sxs-lookup"><span data-stu-id="d8da4-111">In the **Interval type** field, select the interval for the calculation: **Day**, **Week**, **Month**, or **Quarter**.</span></span>

7. <span data-ttu-id="d8da4-112">Í reitnum **Tímabilstíðni** seturðu inn þann fjölda millibila sem þú vilt reikna.</span><span class="sxs-lookup"><span data-stu-id="d8da4-112">In the **Period frequency** field, insert the number of intervals you want to calculate.</span></span> <span data-ttu-id="d8da4-113">Til dæmis, ef þú hefur valið **Dag** sem millibilsgerð og þú setur töluna „5“ inn í þennan reit, verða reiknaðir út fimm dagar frá upphafsdegi.</span><span class="sxs-lookup"><span data-stu-id="d8da4-113">For example, if you have selected **Day** as the interval type, and you enter the number "5" in this field, a calculation of five days from the start date will be made.</span></span>

8. <span data-ttu-id="d8da4-114">Smellið á **Í lagi** til að byrja að reikna.</span><span class="sxs-lookup"><span data-stu-id="d8da4-114">Click **OK** to start the calculation.</span></span>

<span data-ttu-id="d8da4-115">Myndin hér að neðan sýnir niðurstöðu útreiknings sem spannaði þrjár vikur fyrir álagsgerðina **Frátekið**.</span><span class="sxs-lookup"><span data-stu-id="d8da4-115">The figure below shows the result of a calculation covering three weeks for the load type **Reserved**.</span></span>

![Mynd 1](media/08-work-order-scheduling.png)

[!NOTE]
<span data-ttu-id="d8da4-117">Ef þú velur álagsgerðina **Afkastageta** eða **Eftirstöðvar** fyrir útreikninginn mun sama niðurstaða birtast ef engir fyrirvarar hafa verið gerðir á tilföngunum á völdu tímabili.</span><span class="sxs-lookup"><span data-stu-id="d8da4-117">If you select the load types **Capacity** or **Remainder** for your calculation, the same result will be displayed if no reservations have been made for the resources in the selected period.</span></span>

<span data-ttu-id="d8da4-118">Upplýsingar um hvernig skuli reikna út álag afkastagetu á línum viðhaldsskema og óáætluðum verkbeiðnum eru að finna í [Reikna álag](../capacity-planning/calculate-capacity-load.md).</span><span class="sxs-lookup"><span data-stu-id="d8da4-118">For information about how to calculate capacity load on maintenance schedule lines and not scheduled work orders, refer to [Calculate capacity load](../capacity-planning/calculate-capacity-load.md).</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]