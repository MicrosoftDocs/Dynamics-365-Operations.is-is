--- 
title: "Stofna VSK-greiðslu"
description: "Jafna og bóka vsk vinnslu jafnar vsk stöður í vsk-lykla og mótfærir þeim virðisaukaskattsuppgjör reiknings á tilteknu tímabili."
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 9b6e60ff6465ef0bddda2e93b07f41e47f2e1ddd
ms.contentlocale: is-is
ms.lasthandoff: 08/07/2018

---
# <a name="create-a-sales-tax-payment"></a><span data-ttu-id="4640d-103">Stofna VSK-greiðslu</span><span class="sxs-lookup"><span data-stu-id="4640d-103">Create a sales tax payment</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4640d-104">Jafna og bóka vsk vinnslu jafnar vsk stöður í vsk-lykla og mótfærir þeim virðisaukaskattsuppgjör reiknings á tilteknu tímabili.</span><span class="sxs-lookup"><span data-stu-id="4640d-104">The settle and post sales tax job settles sales tax balances on the sales tax accounts and offsets them to the sales tax settlement account for a given period.</span></span>

1. <span data-ttu-id="4640d-105">Fara á Skattur > Skattframtöl > Virðisaukaskattur > Jafna og bóka vsk.</span><span class="sxs-lookup"><span data-stu-id="4640d-105">Go to Tax > Declarations > Sales tax > Settle and post sales tax.</span></span>
2. <span data-ttu-id="4640d-106">Í reitnum jöfnunartímabil skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="4640d-106">In the Settlement period field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="4640d-107">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="4640d-107">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="4640d-108">Dagsetning er rituð í reitinn Frá dags.</span><span class="sxs-lookup"><span data-stu-id="4640d-108">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="4640d-109">Ef valkosturinn Taka leiðréttingar með er ekki valin á síðunni færibreytur fjárhags, jöfnun getur verið unnin fyrir mismunandi útgáfur.</span><span class="sxs-lookup"><span data-stu-id="4640d-109">If the Include corrections option is not selected on the General ledger parameters page, the settlement can be processed for different versions.</span></span> <span data-ttu-id="4640d-110">Upphaflegt er fyrsta jöfnun fyrir tímabilið og er einungis unnin einu sinni fyrir tímabil.</span><span class="sxs-lookup"><span data-stu-id="4640d-110">Original is the first settlement for a period interval and can only processed once for a period interval.</span></span> <span data-ttu-id="4640d-111">Síðustu leiðréttingar jafna vsk-færslur sem hafa verið bókaðar eftir að upprunalega útgáfa hefur verið stofnuð.</span><span class="sxs-lookup"><span data-stu-id="4640d-111">Latest corrections will settle sales tax transactions which have been posted after the original version has been created.</span></span>   
5. <span data-ttu-id="4640d-112">Færa inn dagsetningu í dagsetningarsvæði Færslunnar.</span><span class="sxs-lookup"><span data-stu-id="4640d-112">In the Transaction date field, enter a date.</span></span>
6. <span data-ttu-id="4640d-113">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="4640d-113">Click OK.</span></span>


