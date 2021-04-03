---
title: Breyta heiti á sjálfsafgreiðsluvinnusvæði starfsmanns
description: Þetta efnisatriði lýsir því hvernig á að breyta birgingarheiti vinnusvæðis sjálfsafgreiðslu starfsmanns í Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
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
ms.openlocfilehash: b6df9391f8b97573f7874f8bc19450db3fdadd88
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/17/2021
ms.locfileid: "5463215"
---
# <a name="change-employee-self-service-workspace-name"></a><span data-ttu-id="88f1d-103">Breyta heiti á sjálfsafgreiðsluvinnusvæði starfsmanns</span><span class="sxs-lookup"><span data-stu-id="88f1d-103">Change Employee self service workspace name</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="88f1d-104">Ef um er að ræða sjálfboðaliða eða aðra sem ekki eru starfsmenn er hægt að breyta heiti **Sjálfsafgreiðsla starfsmanna** vinnusvæðisins.</span><span class="sxs-lookup"><span data-stu-id="88f1d-104">If you have volunteers or other non-employees, you might want to change the name of the **Employee self-service** workspace.</span></span> <span data-ttu-id="88f1d-105">Hægt er að breyta þessu vinnusvæði í **Sjálfsafgreiðsla** í staðinn.</span><span class="sxs-lookup"><span data-stu-id="88f1d-105">You can change this workspace to **Self service** instead.</span></span>

> [!NOTE]
> <span data-ttu-id="88f1d-106">Þegar heiti **Sjálfsafgreiðslu starfsmanns** vinnusvæðinu er breytt breytist einnig valmyndaratriðið sem notað er innan Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="88f1d-106">Changing the name of the **Employee self-service** workspace also changes the menu item that is used internally by Dynamics 365 Human Resources.</span></span> <span data-ttu-id="88f1d-107">Ef öryggissérstillingum hefur verið breytt í **HcmEmployeeSelfServiceWorkspace** er mælt með því að nota sömu breytingar í **HcmSelfServiceWorkspace** til að halda samræmi.</span><span class="sxs-lookup"><span data-stu-id="88f1d-107">If you previously applied security customizations to the **HcmEmployeeSelfServiceWorkspace** menu item, we recommend applying the same changes to **HcmSelfServiceWorkspace** to maintain parity.</span></span>

1. <span data-ttu-id="88f1d-108">Í mannauði, veljið **Starfsmannastjórnun**, veljið **Tenglar** og veljið svo **Færibreytur mannauðs**.</span><span class="sxs-lookup"><span data-stu-id="88f1d-108">In Human Resources, select **Personnel management**, select **Links**, and then select **Human resources parameters**.</span></span>

2. <span data-ttu-id="88f1d-109">Veljið flipann **Sjálfsafgreiðsla starfsmanns**.</span><span class="sxs-lookup"><span data-stu-id="88f1d-109">Select the **Employee self-service** tab.</span></span>

3. <span data-ttu-id="88f1d-110">Undir **Nafn til birtingar** skal velja **Sjálfsafgreiðsla**.</span><span class="sxs-lookup"><span data-stu-id="88f1d-110">Under **Display name**, select **Self service**.</span></span>

   ![Breyta heiti vinnusvæðis sjálfsafgreiðslustöðvar fyrir starfsmann í Sjálfsafgreiðslu](./media/hr-employee-self-service-workspace-name.png)

4. <span data-ttu-id="88f1d-112">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="88f1d-112">Select **Save**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="88f1d-113">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="88f1d-113">Additional resources</span></span>

- [<span data-ttu-id="88f1d-114">Yfirsýn yfir sjálfsafgreiðslu starfsmanna og stjórnanda</span><span class="sxs-lookup"><span data-stu-id="88f1d-114">Employee and Manager self-service overview</span></span>](hr-employee-manager-self-service-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]