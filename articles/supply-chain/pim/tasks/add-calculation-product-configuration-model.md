---
title: Bæta útreikningi við afbrigðalíkan afurðar
description: Þessi verklýsing sýnir hvernig á að bæta nýjan útreikning við afbrigðalíkani afurðar.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6e23d33c6911310cca6aac0df4589e909568a86a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5258072"
---
# <a name="add-a-calculation-to-a-product-configuration-model"></a><span data-ttu-id="e4dc0-103">Bæta útreikningi við afbrigðalíkan afurðar</span><span class="sxs-lookup"><span data-stu-id="e4dc0-103">Add a calculation to a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e4dc0-104">Þessi verklýsing sýnir hvernig á að bæta nýjan útreikning við afbrigðalíkani afurðar.</span><span class="sxs-lookup"><span data-stu-id="e4dc0-104">This procedure shows how to add a new calculation to a product configuration model.</span></span> <span data-ttu-id="e4dc0-105">Hún sýnir hvernig hægt er að stofna röksegð með notkun "Ef" virknitákn til að setja hæð hátalara til 10 fyrir hvítum hátalara og 15 fyrir allar aðrar frágang húss.</span><span class="sxs-lookup"><span data-stu-id="e4dc0-105">It shows how you can create a logical expression using the "If" operator to set a speaker height to 10 for white speakers and 15 for all other cabinet finishes.</span></span> <span data-ttu-id="e4dc0-106">Ferlið notar hágæða hátalaraíhlut fyrir USMF sýnigögn fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="e4dc0-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>


## <a name="add-a-calculation"></a><span data-ttu-id="e4dc0-107">Bæta við útreikningum</span><span class="sxs-lookup"><span data-stu-id="e4dc0-107">Add a calculation</span></span>

## <a name="create-calculation-expression"></a><span data-ttu-id="e4dc0-108">Stofna segð útreiknings</span><span class="sxs-lookup"><span data-stu-id="e4dc0-108">Create calculation expression</span></span>
1. <span data-ttu-id="e4dc0-109">Smella á Breyta segð.</span><span class="sxs-lookup"><span data-stu-id="e4dc0-109">Click Edit expression.</span></span>
2. <span data-ttu-id="e4dc0-110">Færið inn í svæðið ConstraintBody ‚If[CabinetFinish == „white", 10, 15]'.</span><span class="sxs-lookup"><span data-stu-id="e4dc0-110">In the ConstraintBody field, enter 'If[CabinetFinish=="White", 10, 15]'.</span></span>
3. <span data-ttu-id="e4dc0-111">Smella á Villuleita.</span><span class="sxs-lookup"><span data-stu-id="e4dc0-111">Click Validate.</span></span>
4. <span data-ttu-id="e4dc0-112">Smellið á „Loka“.</span><span class="sxs-lookup"><span data-stu-id="e4dc0-112">Click Close.</span></span>
5. <span data-ttu-id="e4dc0-113">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="e4dc0-113">Click OK.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]