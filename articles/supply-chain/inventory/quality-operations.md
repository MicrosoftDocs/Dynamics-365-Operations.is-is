---
title: Aðgerðir fyrir ósamkvæmni.
description: Í þessu efnisatriði er lýst hvernig á að stofna og nota aðgerðir vegna ósamkvæmni.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestOperations, InventTestRelatedOperations
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c9a6cc88b80f82d77edac0341cb6a3c0db4b42ce
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022205"
---
# <a name="operations-for-nonconformances"></a><span data-ttu-id="528b9-103">Aðgerðir fyrir ósamkvæmni.</span><span class="sxs-lookup"><span data-stu-id="528b9-103">Operations for nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="528b9-104">Í þessu efnisatriði er lýst hvernig á að stofna og nota aðgerðir vegna ósamkvæmni.</span><span class="sxs-lookup"><span data-stu-id="528b9-104">This topic describes how to create and use operations for nonconformances.</span></span>

<span data-ttu-id="528b9-105">Notið síðuna **Aðgerðir** til þess að skilgreina flokkun á vinnu sem hægt er að framkvæmda fyrir samþykkta ósamkvæmni.</span><span class="sxs-lookup"><span data-stu-id="528b9-105">You can use the **Operations** page to define classifications of the work that can be performed for an approved nonconformance.</span></span> <span data-ttu-id="528b9-106">Þegar tengdri aðgerð er úthlutað á ósamkvæmni, er hægt að gefa upp upplýsingar eins og um tengt efni, vinnustundir og gjöld sem eru nauðsynleg til þess að framkvæma aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="528b9-106">When you assign a related operation to a nonconformance, you can provide details such as the associated material, labor hours, and charges that are required to do the operation.</span></span> <span data-ttu-id="528b9-107">Kerfið notar þessar upplýsingar til að reikna út áætlaðan kostnað fyrir aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="528b9-107">The system uses this information to calculate an estimated cost for the operation.</span></span> <span data-ttu-id="528b9-108">Upplýsingarnar og áætlaður kostnaður er notaður fyrir tilvísanir.</span><span class="sxs-lookup"><span data-stu-id="528b9-108">The detailed information and estimated costs are for reference.</span></span> <span data-ttu-id="528b9-109">Tengdar aðgerðir varðandi gæði eru öðruvísi en aðgerðir sem hægt er að skilgreina fyrir framleiðsluleið.</span><span class="sxs-lookup"><span data-stu-id="528b9-109">The related operations for quality differ from the operations that can be defined for a production route.</span></span>

> [!NOTE]
> <span data-ttu-id="528b9-110">Þó hægt sé að fylgjast með kostnaði, tíma og vörum sem notaðar eru í aðgerð sem tengist ósamkvæmi, eru gögnin sem þú færir inn aðeins til upplýsinga.</span><span class="sxs-lookup"><span data-stu-id="528b9-110">Although you can track costs, time, and the items that are used in an operation that is related to a nonconformance, the data that you enter is only informational.</span></span> <span data-ttu-id="528b9-111">Hún er ekki sjálfkrafa samþætt fjárhag, undirbók birgða eða **Tími og viðvera** einingunni.</span><span class="sxs-lookup"><span data-stu-id="528b9-111">It isn't automatically integrated with the general ledger, inventory subledger, or the **Time and attendance** module.</span></span>

## <a name="examples-of-operations"></a><span data-ttu-id="528b9-112">Dæmi um aðgerðir</span><span class="sxs-lookup"><span data-stu-id="528b9-112">Examples of operations</span></span>

<span data-ttu-id="528b9-113">Þú vinnur fyrir framleiđslufyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="528b9-113">You work for a manufacturing company.</span></span> <span data-ttu-id="528b9-114">Ósamkvæmni var stofnað og samþykkt fyrir atriði sem mistókst í gæðaprófun.</span><span class="sxs-lookup"><span data-stu-id="528b9-114">A nonconformance was created and approved for items that failed a quality test.</span></span> <span data-ttu-id="528b9-115">Leiðrétting var gerð til að gefa til kynna að vandamálið tengdist lélegri legu í vél.</span><span class="sxs-lookup"><span data-stu-id="528b9-115">A correction was created to indicate that the problem was related to a bad bearing on a machine.</span></span> <span data-ttu-id="528b9-116">Fara þarf í gegnum nokkur skref til að skipta út legunni og ábyrgðin fyrir hverja aðgerð er rakin.</span><span class="sxs-lookup"><span data-stu-id="528b9-116">Several steps are required to replace the bearing, and the responsibility for each operation is tracked.</span></span> <span data-ttu-id="528b9-117">Til dæmis gætu eftirfarandi skref verið nauðsynleg:</span><span class="sxs-lookup"><span data-stu-id="528b9-117">For example, the following steps might be required:</span></span>

1. <span data-ttu-id="528b9-118">Framleiðslulínan stöðvast og hreinsunarferlið er framkvæmt.</span><span class="sxs-lookup"><span data-stu-id="528b9-118">The production line is stopped, and the clean-out routine is performed.</span></span>
1. <span data-ttu-id="528b9-119">Viðgerðarmaður skiptir um leguna.</span><span class="sxs-lookup"><span data-stu-id="528b9-119">Maintenance personnel replace the bearing.</span></span>
1. <span data-ttu-id="528b9-120">Starfsfólk gæðatryggingar skoðar vélina áður en kveikt er á henni á nýjan leik.</span><span class="sxs-lookup"><span data-stu-id="528b9-120">Quality assurance personnel inspect the machine before it's turned back on.</span></span>

<span data-ttu-id="528b9-121">Í þessu dæmi er hægt að búa til eftirfarandi aðgerðir til að tákna það verk sem þarf að framkvæma:</span><span class="sxs-lookup"><span data-stu-id="528b9-121">For this example, the following operations can be created to represent the work that must be done:</span></span>

- <span data-ttu-id="528b9-122">Stöðvið framleiðslulínuna.</span><span class="sxs-lookup"><span data-stu-id="528b9-122">Stop the production line.</span></span>
- <span data-ttu-id="528b9-123">Hreinsaðu framleiðslulínuna.</span><span class="sxs-lookup"><span data-stu-id="528b9-123">Clean out the production line.</span></span>
- <span data-ttu-id="528b9-124">Framkvæmið viðhald á vél.</span><span class="sxs-lookup"><span data-stu-id="528b9-124">Perform machine maintenance.</span></span>
- <span data-ttu-id="528b9-125">Skoðið vélina.</span><span class="sxs-lookup"><span data-stu-id="528b9-125">Inspect the machine.</span></span>

## <a name="create-an-operation"></a><span data-ttu-id="528b9-126">Stofna aðgerð</span><span class="sxs-lookup"><span data-stu-id="528b9-126">Create an operation</span></span>

1. <span data-ttu-id="528b9-127">Fara í **Birgðastjórnun \> Uppsetning \> Gæðastjórnun \> Aðgerðir**.</span><span class="sxs-lookup"><span data-stu-id="528b9-127">Go to **Inventory management \> Setup \> Quality management \> Operations**.</span></span>
1. <span data-ttu-id="528b9-128">Á aðgerðasvæðinu skal velja **Ný** til að bæta línu við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="528b9-128">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="528b9-129">Stillið svo eftirfarandi reiti fyrir nýju línuna:</span><span class="sxs-lookup"><span data-stu-id="528b9-129">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="528b9-130">**Aðgerð** – Færið inn einkvæmt kenni eða heiti fyrir aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="528b9-130">**Operation** – Enter a unique ID or name for the operation.</span></span>
    - <span data-ttu-id="528b9-131">**Lýsing** – Færið inn ítarlega lýsingu á aðgerðinni.</span><span class="sxs-lookup"><span data-stu-id="528b9-131">**Description** – Enter a detailed description of the operation.</span></span>
    - <span data-ttu-id="528b9-132">**Gerð** – Ef aðgerðina er aðeins hægt að nota vegna ósamkvæmni sem tengist tiltekinni gerð pöntunar skal velja pöntunargerðina (*Innkaupapöntun* eða *Sölupöntun*).</span><span class="sxs-lookup"><span data-stu-id="528b9-132">**Type** – If the operation can be used only with nonconformances that are related to a specific type of order, select the order type (*Purchase order* or *Sales order*).</span></span>

1. <span data-ttu-id="528b9-133">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="528b9-133">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="528b9-134">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="528b9-134">Additional resources</span></span>

- [<span data-ttu-id="528b9-135">Gæðastjórnunaryfirlit</span><span class="sxs-lookup"><span data-stu-id="528b9-135">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="528b9-136">Virkja stjórnun gæða og ósamkvæmni</span><span class="sxs-lookup"><span data-stu-id="528b9-136">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="528b9-137">Stofna og meðhöndla ósamkvæmi</span><span class="sxs-lookup"><span data-stu-id="528b9-137">Create and process nonconformances</span></span>](tasks/create-process-non-conformance.md)
- [<span data-ttu-id="528b9-138">Starfsmenn ábyrgir fyrir samþykki ósamkvæmni</span><span class="sxs-lookup"><span data-stu-id="528b9-138">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="528b9-139">Biðgeymslusvæði fyrir ósamkvæmi</span><span class="sxs-lookup"><span data-stu-id="528b9-139">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="528b9-140">Gerðir greininga fyrir ósamkvæmni</span><span class="sxs-lookup"><span data-stu-id="528b9-140">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="528b9-141">Gæðagjöld fyrir ósamkvæmi</span><span class="sxs-lookup"><span data-stu-id="528b9-141">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="528b9-142">Gerðir vandamála fyrir ósamkvæmni</span><span class="sxs-lookup"><span data-stu-id="528b9-142">Problem types for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="528b9-143">Gæðastjórnun fyrir vöruhúsaferli</span><span class="sxs-lookup"><span data-stu-id="528b9-143">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
