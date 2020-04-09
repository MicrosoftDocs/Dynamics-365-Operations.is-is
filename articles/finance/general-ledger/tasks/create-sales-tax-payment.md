---
title: Stofna VSK-greiðslu
description: Jafna og bóka vsk vinnslu jafnar vsk stöður í vsk-lykla og mótfærir þeim virðisaukaskattsuppgjör reiknings á tilteknu tímabili.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Dialog
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 99059a8e5d6f4bf125266ad2a98cb73751529e6b
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/18/2020
ms.locfileid: "3139923"
---
# <a name="create-a-sales-tax-payment"></a><span data-ttu-id="4fddb-103">Stofna VSK-greiðslu</span><span class="sxs-lookup"><span data-stu-id="4fddb-103">Create a sales tax payment</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4fddb-104">Jafna og bóka vsk vinnslu jafnar vsk stöður í vsk-lykla og mótfærir þeim virðisaukaskattsuppgjör reiknings á tilteknu tímabili.</span><span class="sxs-lookup"><span data-stu-id="4fddb-104">The settle and post sales tax job settles sales tax balances on the sales tax accounts and offsets them to the sales tax settlement account for a given period.</span></span>

1. <span data-ttu-id="4fddb-105">Fara á Skattur > Skattframtöl > Virðisaukaskattur > Jafna og bóka vsk.</span><span class="sxs-lookup"><span data-stu-id="4fddb-105">Go to Tax > Declarations > Sales tax > Settle and post sales tax.</span></span>
2. <span data-ttu-id="4fddb-106">Í reitnum jöfnunartímabil skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="4fddb-106">In the Settlement period field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="4fddb-107">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="4fddb-107">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="4fddb-108">Dagsetning er rituð í reitinn Frá dags.</span><span class="sxs-lookup"><span data-stu-id="4fddb-108">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="4fddb-109">Ef valkosturinn Taka leiðréttingar með er ekki valin á síðunni færibreytur fjárhags, jöfnun getur verið unnin fyrir mismunandi útgáfur.</span><span class="sxs-lookup"><span data-stu-id="4fddb-109">If the Include corrections option is not selected on the General ledger parameters page, the settlement can be processed for different versions.</span></span> <span data-ttu-id="4fddb-110">Upphaflegt er fyrsta jöfnun fyrir tímabilið og er einungis unnin einu sinni fyrir tímabil.</span><span class="sxs-lookup"><span data-stu-id="4fddb-110">Original is the first settlement for a period interval and can only processed once for a period interval.</span></span> <span data-ttu-id="4fddb-111">Síðustu leiðréttingar jafna vsk-færslur sem hafa verið bókaðar eftir að upprunalega útgáfa hefur verið stofnuð.</span><span class="sxs-lookup"><span data-stu-id="4fddb-111">Latest corrections will settle sales tax transactions which have been posted after the original version has been created.</span></span>   
5. <span data-ttu-id="4fddb-112">Færa inn dagsetningu í dagsetningarsvæði Færslunnar.</span><span class="sxs-lookup"><span data-stu-id="4fddb-112">In the Transaction date field, enter a date.</span></span>
6. <span data-ttu-id="4fddb-113">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="4fddb-113">Click OK.</span></span>

