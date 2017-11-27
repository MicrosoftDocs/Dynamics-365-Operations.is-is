---
title: "Stofna farmbréf"
description: "Þetta efnisatriði lýsir hvernig á að stofna farmbréf þegar verið er að nota vöruhúsakerfisferli."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSBillOfLading, WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 193583
ms.assetid: 1ad0c1cb-4346-4042-a59b-923115fac03e
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: ab5aa60198e442237fd85bb295589ae0ebe9c5f5
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="create-a-bill-of-lading"></a><span data-ttu-id="f4c8d-103">Stofna farmbréf</span><span class="sxs-lookup"><span data-stu-id="f4c8d-103">Create a bill of lading</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="f4c8d-104">Þetta efnisatriði lýsir hvernig á að stofna farmbréf þegar verið er að nota vöruhúsakerfisferli.</span><span class="sxs-lookup"><span data-stu-id="f4c8d-104">This topic describes how to create a bill of lading when using warehouse management processes.</span></span>  

<span data-ttu-id="f4c8d-105">Farmbréf er lagagerningur milli flytjanda sem sendir vörur og flutningsaðila.</span><span class="sxs-lookup"><span data-stu-id="f4c8d-105">A bill of lading is a legal document between the company that ships the items and the carrier.</span></span> <span data-ttu-id="f4c8d-106">Skjalið fylgir sendum vörum, og það gegnir hlutverki kvittunar fyrir sendingu þegar vörur eru afhentar á ákvörðunarstað.</span><span class="sxs-lookup"><span data-stu-id="f4c8d-106">The document accompanies the shipped items, and it serves as a receipt of shipment when the items are delivered at the destination.</span></span> <span data-ttu-id="f4c8d-107">Ef verið er að nota vöruhúsakerfi, eru tvær leiðir til að mynda farmbréf:</span><span class="sxs-lookup"><span data-stu-id="f4c8d-107">If you're using warehouse management, there are two ways to generate a bill of lading:</span></span>

  -   <span data-ttu-id="f4c8d-108">Búa til skýrslu handvirkt með því að nota síðuna **farmbréf** .</span><span class="sxs-lookup"><span data-stu-id="f4c8d-108">Create the report manually, using the **Bill of lading** page.</span></span>
  -   <span data-ttu-id="f4c8d-109">Búa til skýrslu úr **vinnusvæði farmáætlunar**.</span><span class="sxs-lookup"><span data-stu-id="f4c8d-109">Generate the report from the **Load planning workbench**.</span></span>

<span data-ttu-id="f4c8d-110">Ef þú myndar farmbréf úr **vinnusvæði farmáætlun**, verður staða farms að vera **Sent.**</span><span class="sxs-lookup"><span data-stu-id="f4c8d-110">If you generate the bill of lading from the **Load planning workbench**, the load status must be **Shipped.**</span></span> <span data-ttu-id="f4c8d-111">Ef fleiri en einn sendingar eru í farminum er farmbréf stofnuð fyrir hverja sendingu.</span><span class="sxs-lookup"><span data-stu-id="f4c8d-111">If there's more than one shipment in the load, a bill of lading is created for each shipment.</span></span> <span data-ttu-id="f4c8d-112">Eftir að farmbréf hefur verið stofnað er hægt gera breytingar á því á **farmbréf** síðu.</span><span class="sxs-lookup"><span data-stu-id="f4c8d-112">After a bill of lading has been created you can make changes to it on the **Bill of lading** page.</span></span>

## <a name="master-bill-of-lading"></a><span data-ttu-id="f4c8d-113">Aðalfarmbréf</span><span class="sxs-lookup"><span data-stu-id="f4c8d-113">Master bill of lading</span></span>
<span data-ttu-id="f4c8d-114">Ef fleiri en ein sending er í farmi er hægt að Stofna aðalfarmbréf.</span><span class="sxs-lookup"><span data-stu-id="f4c8d-114">If there's more than one shipment in the load, you can generate a master bill of lading.</span></span> <span data-ttu-id="f4c8d-115">Þetta hefur sama útlit og upplýsingar um farmbréf, en inniheldur samantekið efni fyrir allar sendingar.</span><span class="sxs-lookup"><span data-stu-id="f4c8d-115">This has the same layout and information as a bill of lading, but contains the summarized content for all the shipments.</span></span> <span data-ttu-id="f4c8d-116">Ef valkosturinn **Stofna aðalfarmbréf þegar það eru fleiri en ein sending í farmi** er stilltur á **Já** á síðunni **færibreytur Flutningsstjórnunar** er aðalfarmbréfið myndað sjálfkrafa ef þú stofnar farmbréf úr **vinnusvæði Farmáætlun**, og það eru fleiri en ein sending til staðar.</span><span class="sxs-lookup"><span data-stu-id="f4c8d-116">If the **Create a master bill of lading when there's more than one shipment on a load** option is set to **Yes** on the **Transportation management parameters** page, a master bill of lading is automatically generated if you create a bill of lading from the **Load planning workbench**, and there's more than one shipment.</span></span> <span data-ttu-id="f4c8d-117">Einnig er hægt að fá lista yfir í farmbréf með því að smella á **tengdar upplýsingar** &gt; **farmbréf**.</span><span class="sxs-lookup"><span data-stu-id="f4c8d-117">You can also get a list of the bills of lading by clicking **Related information** &gt; **Bill of lading**.</span></span> <span data-ttu-id="f4c8d-118">Ef verið er að stofna farmbréf handvirkt er hægt að stofna aðalfarmbréf á **farmbréf** síðu.</span><span class="sxs-lookup"><span data-stu-id="f4c8d-118">If you're creating bills of lading manually, you can create a master bill of lading on the **Bill of lading** page.</span></span>




