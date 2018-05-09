--- 
title: "Bæta útreikningi við afbrigðalíkan afurðar"
description: "Þessi verklýsing sýnir hvernig á að bæta nýjan útreikning við afbrigðalíkani afurðar."
author: YuyuScheller
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 123ae1315c95693af09d7d7c96a071d606ac98f8
ms.contentlocale: is-is
ms.lasthandoff: 05/08/2018

---
# <a name="add-a-calculation-to-a-product-configuration-model"></a><span data-ttu-id="18fc3-103">Bæta útreikningi við afbrigðalíkan afurðar</span><span class="sxs-lookup"><span data-stu-id="18fc3-103">Add a calculation to a product configuration model</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="18fc3-104">Þessi verklýsing sýnir hvernig á að bæta nýjan útreikning við afbrigðalíkani afurðar.</span><span class="sxs-lookup"><span data-stu-id="18fc3-104">This procedure shows how to add a new calculation to a product configuration model.</span></span> <span data-ttu-id="18fc3-105">Hún sýnir hvernig hægt er að stofna röksegð með notkun "Ef" virknitákn til að setja hæð hátalara til 10 fyrir hvítum hátalara og 15 fyrir allar aðrar frágang húss.</span><span class="sxs-lookup"><span data-stu-id="18fc3-105">It shows how you can create a logical expression using the "If" operator to set a speaker height to 10 for white speakers and 15 for all other cabinet finishes.</span></span> <span data-ttu-id="18fc3-106">Ferlið notar hágæða hátalaraíhlut fyrir USMF sýnigögn fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="18fc3-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>


## <a name="add-a-calculation"></a><span data-ttu-id="18fc3-107">Bæta við útreikningum</span><span class="sxs-lookup"><span data-stu-id="18fc3-107">Add a calculation</span></span>

## <a name="create-calculation-expression"></a><span data-ttu-id="18fc3-108">Stofna segð útreiknings</span><span class="sxs-lookup"><span data-stu-id="18fc3-108">Create calculation expression</span></span>
1. <span data-ttu-id="18fc3-109">Smella á Breyta segð.</span><span class="sxs-lookup"><span data-stu-id="18fc3-109">Click Edit expression.</span></span>
2. <span data-ttu-id="18fc3-110">Færið inn í svæðið ConstraintBody ‚If[CabinetFinish == „white", 10, 15]'.</span><span class="sxs-lookup"><span data-stu-id="18fc3-110">In the ConstraintBody field, enter 'If[CabinetFinish=="White", 10, 15]'.</span></span>
3. <span data-ttu-id="18fc3-111">Smella á Villuleita.</span><span class="sxs-lookup"><span data-stu-id="18fc3-111">Click Validate.</span></span>
4. <span data-ttu-id="18fc3-112">Smellið á „Loka“.</span><span class="sxs-lookup"><span data-stu-id="18fc3-112">Click Close.</span></span>
5. <span data-ttu-id="18fc3-113">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="18fc3-113">Click OK.</span></span>


