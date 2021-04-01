---
title: Stofna VSK-greiðslu
description: Jafna og bóka VSK vinnslan jafnar VSK stöður í VSK -lykla og mótfærir þeim virðisaukaskattsuppgjör reiknings á tilteknu tímabili.
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
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f9523ef75953bdca36f509f596c51c08b12b3fdb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254464"
---
# <a name="create-a-sales-tax-payment"></a><span data-ttu-id="06469-103">Stofna VSK-greiðslu</span><span class="sxs-lookup"><span data-stu-id="06469-103">Create a sales tax payment</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="06469-104">Jafna og bóka VSK vinnslan jafnar VSK stöður í VSK -lykla og mótfærir þeim virðisaukaskattsuppgjör reiknings á tilteknu tímabili.</span><span class="sxs-lookup"><span data-stu-id="06469-104">The settle and post sales tax job procedure settles sales tax balances on the sales tax accounts, and offsets them to the sales tax settlement account for a given period.</span></span>

1. <span data-ttu-id="06469-105">Fara á **Skattur > Skattframtöl > Virðisaukaskattur > Jafna og bóka vsk**.</span><span class="sxs-lookup"><span data-stu-id="06469-105">Go to **Tax > Declarations > Sales tax > Settle and post sales tax**.</span></span>
2. <span data-ttu-id="06469-106">Í reitnum **jöfnunartímabil** skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="06469-106">In the **Settlement period** field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="06469-107">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="06469-107">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="06469-108">Í reitnum **Frá dags.** færirði inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="06469-108">In the **From date** field, enter a date.</span></span>
    * <span data-ttu-id="06469-109">Ef valkosturinn **Taka leiðréttingar** með er ekki valin á síðunni **Færibreytur fjárhags**, getur jöfnun verið unnin fyrir mismunandi útgáfur.</span><span class="sxs-lookup"><span data-stu-id="06469-109">If you don't select the **Include corrections** option on the **General ledger parameters** page, the settlement can be processed for different versions.</span></span> <span data-ttu-id="06469-110">Upphaflegt er fyrsta jöfnun fyrir tímabilið og er einungis hægt að vinna einu sinni fyrir tímabil.</span><span class="sxs-lookup"><span data-stu-id="06469-110">Original is the first settlement for a period interval and can be processed only once for a period interval.</span></span> <span data-ttu-id="06469-111">Síðustu leiðréttingar jafna vsk-færslur sem hafa verið bókaðar eftir að upprunalega útgáfa hefur verið stofnuð.</span><span class="sxs-lookup"><span data-stu-id="06469-111">The latest corrections will settle sales tax transactions which have been posted after the original version has been created.</span></span>   
5. <span data-ttu-id="06469-112">Færa inn dagsetningu í reitinn **Færsludagsetning**.</span><span class="sxs-lookup"><span data-stu-id="06469-112">In the **Transaction date** field, enter a date.</span></span>
6. <span data-ttu-id="06469-113">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="06469-113">Click **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]