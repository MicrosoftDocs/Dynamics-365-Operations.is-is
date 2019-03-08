---
title: Bæta útreikningi við afbrigðalíkan afurðar
description: Þessi verklýsing sýnir hvernig á að bæta nýjan útreikning við afbrigðalíkani afurðar.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9754c46010e7bbdb2edef0d6e68162f344bb1257
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "343168"
---
# <a name="add-a-calculation-to-a-product-configuration-model"></a><span data-ttu-id="ef96c-103">Bæta útreikningi við afbrigðalíkan afurðar</span><span class="sxs-lookup"><span data-stu-id="ef96c-103">Add a calculation to a product configuration model</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ef96c-104">Þessi verklýsing sýnir hvernig á að bæta nýjan útreikning við afbrigðalíkani afurðar.</span><span class="sxs-lookup"><span data-stu-id="ef96c-104">This procedure shows how to add a new calculation to a product configuration model.</span></span> <span data-ttu-id="ef96c-105">Hún sýnir hvernig hægt er að stofna röksegð með notkun "Ef" virknitákn til að setja hæð hátalara til 10 fyrir hvítum hátalara og 15 fyrir allar aðrar frágang húss.</span><span class="sxs-lookup"><span data-stu-id="ef96c-105">It shows how you can create a logical expression using the "If" operator to set a speaker height to 10 for white speakers and 15 for all other cabinet finishes.</span></span> <span data-ttu-id="ef96c-106">Ferlið notar hágæða hátalaraíhlut fyrir USMF sýnigögn fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="ef96c-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>


## <a name="add-a-calculation"></a><span data-ttu-id="ef96c-107">Bæta við útreikningum</span><span class="sxs-lookup"><span data-stu-id="ef96c-107">Add a calculation</span></span>

## <a name="create-calculation-expression"></a><span data-ttu-id="ef96c-108">Stofna segð útreiknings</span><span class="sxs-lookup"><span data-stu-id="ef96c-108">Create calculation expression</span></span>
1. <span data-ttu-id="ef96c-109">Smella á Breyta segð.</span><span class="sxs-lookup"><span data-stu-id="ef96c-109">Click Edit expression.</span></span>
2. <span data-ttu-id="ef96c-110">Færið inn í svæðið ConstraintBody ‚If[CabinetFinish == „white", 10, 15]'.</span><span class="sxs-lookup"><span data-stu-id="ef96c-110">In the ConstraintBody field, enter 'If[CabinetFinish=="White", 10, 15]'.</span></span>
3. <span data-ttu-id="ef96c-111">Smella á Villuleita.</span><span class="sxs-lookup"><span data-stu-id="ef96c-111">Click Validate.</span></span>
4. <span data-ttu-id="ef96c-112">Smellið á „Loka“.</span><span class="sxs-lookup"><span data-stu-id="ef96c-112">Click Close.</span></span>
5. <span data-ttu-id="ef96c-113">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="ef96c-113">Click OK.</span></span>

