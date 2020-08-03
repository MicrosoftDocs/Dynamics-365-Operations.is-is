---
title: Breyta heiti á sjálfsafgreiðsluvinnusvæði starfsmanns
description: Þetta efnisatriði lýsir því hvernig á að breyta birgingarheiti vinnusvæðis sjálfsafgreiðslu starfsmanns í Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 07/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: EssWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-07-09
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2ce008c44ba84c919f4538be4d8e4ff95be018e7
ms.sourcegitcommit: 1ec931f8fe86bde27f6def36ea214a2a05fb22f6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/13/2020
ms.locfileid: "3554354"
---
# <a name="change-employee-self-service-workspace-name"></a><span data-ttu-id="b1457-103">Breyta heiti á sjálfsafgreiðsluvinnusvæði starfsmanns</span><span class="sxs-lookup"><span data-stu-id="b1457-103">Change Employee self service workspace name</span></span>

<span data-ttu-id="b1457-104">Ef um er að ræða sjálfboðaliða eða aðra sem ekki eru starfsmenn er hægt að breyta heiti **Sjálfsafgreiðsla starfsmanna** vinnusvæðisins.</span><span class="sxs-lookup"><span data-stu-id="b1457-104">If you have volunteers or other non-employees, you might want to change the name of the **Employee self-service** workspace.</span></span> <span data-ttu-id="b1457-105">Hægt er að breyta þessu vinnusvæði í **Sjálfsafgreiðsla** í staðinn.</span><span class="sxs-lookup"><span data-stu-id="b1457-105">You can change this workspace to **Self service** instead.</span></span>

> [!NOTE]
> <span data-ttu-id="b1457-106">Þegar heiti **Sjálfsafgreiðslu starfsmanns** vinnusvæðinu er breytt breytist einnig valmyndaratriðið sem notað er innan Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="b1457-106">Changing the name of the **Employee self-service** workspace also changes the menu item that is used internally by Dynamics 365 Human Resources.</span></span> <span data-ttu-id="b1457-107">Ef öryggissérstillingum hefur verið breytt í **HcmEmployeeSelfServiceWorkspace** er mælt með því að nota sömu breytingar í **HcmSelfServiceWorkspace** til að halda samræmi.</span><span class="sxs-lookup"><span data-stu-id="b1457-107">If you previously applied security customizations to the **HcmEmployeeSelfServiceWorkspace** menu item, we recommend applying the same changes to **HcmSelfServiceWorkspace** to maintain parity.</span></span>

1. <span data-ttu-id="b1457-108">Í mannauði, veljið **Starfsmannastjórnun**, veljið **Tenglar** og veljið svo **Færibreytur mannauðs**.</span><span class="sxs-lookup"><span data-stu-id="b1457-108">In Human Resources, select **Personnel management**, select **Links**, and then select **Human resources parameters**.</span></span>

2. <span data-ttu-id="b1457-109">Veljið flipann **Sjálfsafgreiðsla starfsmanns**.</span><span class="sxs-lookup"><span data-stu-id="b1457-109">Select the **Employee self-service** tab.</span></span>

3. <span data-ttu-id="b1457-110">Undir **Nafn til birtingar** skal velja **Sjálfsafgreiðsla**.</span><span class="sxs-lookup"><span data-stu-id="b1457-110">Under **Display name**, select **Self service**.</span></span>

   ![Breyta heiti vinnusvæðis sjálfsafgreiðslustöðvar fyrir starfsmann í Sjálfsafgreiðslu](./media/hr-employee-self-service-workspace-name.png)

4. <span data-ttu-id="b1457-112">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="b1457-112">Select **Save**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b1457-113">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="b1457-113">Additional resources</span></span>

- [<span data-ttu-id="b1457-114">Yfirsýn yfir sjálfsafgreiðslu starfsmanna og stjórnanda</span><span class="sxs-lookup"><span data-stu-id="b1457-114">Employee and Manager self-service overview</span></span>](hr-employee-manager-self-service-overview.md)