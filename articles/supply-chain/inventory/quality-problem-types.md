---
title: Gerðir vandamála fyrir ósamkvæmni
description: Í þessu efnisatriði er lýst hvernig á að stofna og nota gerðir vandamála fyrir ósamkvæmni.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventProblemType, InventProblemTypeSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: df509365f5c900898921acfbda380b5e20c7a251
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956704"
---
# <a name="problem-types-for-nonconformances"></a><span data-ttu-id="239f8-103">Gerðir vandamála fyrir ósamkvæmni</span><span class="sxs-lookup"><span data-stu-id="239f8-103">Problem types for nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="239f8-104">Í þessu efnisatriði er lýst hvernig á að stofna og nota gerðir vandamála fyrir ósamkvæmni.</span><span class="sxs-lookup"><span data-stu-id="239f8-104">This topic describes how to create and use problem types for nonconformances.</span></span>

<span data-ttu-id="239f8-105">Nota skal síðuna **Gerðir vandamála** til að skilgreina flokkun á gæðavanda sem getur komið upp fyrir hinar ýmsu gerðir ósamkvæmni.</span><span class="sxs-lookup"><span data-stu-id="239f8-105">You use the **Problem types** page to define a classification of the quality problems that might occur for the various nonconformance types.</span></span> <span data-ttu-id="239f8-106">Fyrir hverja gerð vandamáls sem búin er til þarf að tilgreina ósamkvæmnisgerðir sem gerð vandamáls getur verið notuð með.</span><span class="sxs-lookup"><span data-stu-id="239f8-106">For each problem type that you create, you must specify the types of nonconformances that the problem type can be used with.</span></span> <span data-ttu-id="239f8-107">Hægt er að setja upp eftirfarandi gerðir ósamkvæmni:</span><span class="sxs-lookup"><span data-stu-id="239f8-107">You can set up the following nonconformance types:</span></span>

- <span data-ttu-id="239f8-108">**Innra** – Ósamkvæmni af þessari gerð tengjast lagerbirgðum (til dæmis gæðapantanir eða biðgeymslupantanir).</span><span class="sxs-lookup"><span data-stu-id="239f8-108">**Internal** – Nonconformances of this type are related to on-hand inventory (for example, quality orders or quarantine orders).</span></span>
- <span data-ttu-id="239f8-109">**Viðskiptavinur** – Ósamkvæmni af þessari gerð tengist sölupöntunum.</span><span class="sxs-lookup"><span data-stu-id="239f8-109">**Customer** – Nonconformances of this type are related to sales orders.</span></span>
- <span data-ttu-id="239f8-110">**Lánardrottinn** – Ósamkvæmni af þessari gerð tengist innkaupapöntunum.</span><span class="sxs-lookup"><span data-stu-id="239f8-110">**Vendor** – Nonconformances of this type are related to purchase orders.</span></span>
- <span data-ttu-id="239f8-111">**Þjónustubeiðni** – Ósamkvæmni af þessari gerð tengjast þjónustupöntunum.</span><span class="sxs-lookup"><span data-stu-id="239f8-111">**Service request** – Nonconformances of this type are related to service orders.</span></span>
- <span data-ttu-id="239f8-112">**Framleiðsla** – Ósamkvæmi af þessari gerð eru tengd lotupöntunum eða framleiðslupöntunum.</span><span class="sxs-lookup"><span data-stu-id="239f8-112">**Production** – Nonconformances of this type are related to batch orders or production orders.</span></span>
- <span data-ttu-id="239f8-113">**Framleiðsla aukaafurðar** – Ósamkvæmni af þessari gerð tengist runupöntunum fyrir aukaafurðir.</span><span class="sxs-lookup"><span data-stu-id="239f8-113">**Co-product production** – Nonconformances of this type are related to batch orders for co-products.</span></span>

<span data-ttu-id="239f8-114">Þegar ný gerð vandamáls er stofnuð skal velja **Gerðir ósamkvæmni** á aðgerðasvæðinu til að búa til lista yfir eina eða fleiri gerðir af ósamkvæmni sem eru heimilaðar fyrir gerð vandamáls.</span><span class="sxs-lookup"><span data-stu-id="239f8-114">When you create a new problem type, select **Non conformance types** on the Action Pane to create a list of one or more nonconformance types that are authorized for the problem type.</span></span> <span data-ttu-id="239f8-115">Til dæmis getur vandamálagerð sem tengist gallakóða átt við um allar gerðir ósamkvæmni.</span><span class="sxs-lookup"><span data-stu-id="239f8-115">For example, a problem type that is related to a defect code might apply to all nonconformance types.</span></span> <span data-ttu-id="239f8-116">Hins vegar getur vandamálagerð um kvartanir viðskiptavina hugsanlega aðeins átt við um ósamkvæmisgerðir **Viðskiptavinar** og **Þjónustubeiðni**.</span><span class="sxs-lookup"><span data-stu-id="239f8-116">However, a problem type that is related to customer complaints might apply only to the **Customer** and **Service request** nonconformance types.</span></span>

## <a name="examples-of-problem-types"></a><span data-ttu-id="239f8-117">Dæmi um gerðir vandamála</span><span class="sxs-lookup"><span data-stu-id="239f8-117">Examples of problem types</span></span>

<span data-ttu-id="239f8-118">Hér eru nokkur dæmi um aðstæður fyrir gerðir vandamála sem hægt er að nota með mismunandi gerðum ósamkvæmni:</span><span class="sxs-lookup"><span data-stu-id="239f8-118">Here are some examples of scenarios for problem types that can be used with the different nonconformance types:</span></span>

- <span data-ttu-id="239f8-119">**Viðskiptavinur**: Viðskiptavinur lagði fram kvörtun, viðskiptavinur skilaði einhverju eða gæðalýsingar voru ekki uppfyllt.</span><span class="sxs-lookup"><span data-stu-id="239f8-119">**Customer:** A customer filed a complaint, a customer made a return, or quality specifications weren't met.</span></span>
- <span data-ttu-id="239f8-120">**Lánardrottinn:** Afurðin skemmdist, gæðalýsingar voru ekki uppfylltar eða röng afurð barst.</span><span class="sxs-lookup"><span data-stu-id="239f8-120">**Vendor:** The product was damaged, quality specifications weren't met, or the wrong product was received.</span></span>
- <span data-ttu-id="239f8-121">**Þjónustubeiðni:** Gæðaskilyrði voru ekki uppfyllt, viðskiptavinur lagði fram kvörtun eða vélarviðhald er nauðsynlegt.</span><span class="sxs-lookup"><span data-stu-id="239f8-121">**Service request:** Quality specifications weren't met, a customer filed a complaint, or machine maintenance is required.</span></span>
- <span data-ttu-id="239f8-122">**Framleiðsla:** Gæðaskilyrði voru ekki uppfyllt, viðhald vélar er nauðsynlegt eða varan skemmdist.</span><span class="sxs-lookup"><span data-stu-id="239f8-122">**Production:** Quality specifications weren't met, machine maintenance is required, or the product was damaged.</span></span>
- <span data-ttu-id="239f8-123">**Framleiðsla aukaafurðar:** Gæðalýsingar voru ekki uppfylltar, viðhald vélar er nauðsynlegt eða afurðin skemmdist.</span><span class="sxs-lookup"><span data-stu-id="239f8-123">**Co-product production:** Quality specifications weren't met, machine maintenance is required, or the product was damaged.</span></span>

## <a name="create-a-problem-type-and-assign-it-to-nonconformance-types"></a><span data-ttu-id="239f8-124">Stofna gerð vandamáls og úthluta henni á gerðir ósamkvæmni</span><span class="sxs-lookup"><span data-stu-id="239f8-124">Create a problem type and assign it to nonconformance types</span></span>

1. <span data-ttu-id="239f8-125">Fara í **Birgðastjórnun \> Uppsetningu \> gæðastjórnun \> gerðir vandamála**.</span><span class="sxs-lookup"><span data-stu-id="239f8-125">Go to **Inventory management \> Setup \> Quality management \> Problem types**.</span></span>
1. <span data-ttu-id="239f8-126">Á aðgerðasvæðinu skal velja **Ný** til að bæta línu við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="239f8-126">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="239f8-127">Stillið svo eftirfarandi reiti fyrir nýju línuna:</span><span class="sxs-lookup"><span data-stu-id="239f8-127">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="239f8-128">**Gerð vandamáls** – Færið inn einkvæmt kenni eða heiti fyrir gerð vandamálsins.</span><span class="sxs-lookup"><span data-stu-id="239f8-128">**Problem type** – Enter a unique ID or name for the problem type.</span></span>
    - <span data-ttu-id="239f8-129">**Lýsing** – Færið inn ítarlega lýsingu á gerð vandamáls.</span><span class="sxs-lookup"><span data-stu-id="239f8-129">**Description** – Enter a detailed description of the problem type.</span></span>

1. <span data-ttu-id="239f8-130">Á meðan nýja línan er enn valin, skal velja **Gerðir ósamkvæmnitilvika** á aðgerðasvæðinu.</span><span class="sxs-lookup"><span data-stu-id="239f8-130">While the new row is still selected, select **Non conformance types** on the Action Pane.</span></span>
1. <span data-ttu-id="239f8-131">Á aðgerðasvæðinu skal velja **Ný** til að bæta línu við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="239f8-131">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="239f8-132">Í nýju röðinni skal síðan stilla reitinn **Gerð ósamkvæmni** á gerðina sem þú vilt leyfa fyrir gerð vandamálsins.</span><span class="sxs-lookup"><span data-stu-id="239f8-132">Then, for the new row, set the **Non conformance type** field to the nonconformance type that you want to allow for the problem type.</span></span>
1. <span data-ttu-id="239f8-133">Endurtaka skal fyrri skref fyrir hverja viðbótargerð ósamkvæmni sem á að heimila fyrir gerð vandans.</span><span class="sxs-lookup"><span data-stu-id="239f8-133">Repeat the previous step for each additional nonconformance type that you want to authorize for the problem type.</span></span>
1. <span data-ttu-id="239f8-134">Lokaðu síðunum.</span><span class="sxs-lookup"><span data-stu-id="239f8-134">Close the pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="239f8-135">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="239f8-135">Additional resources</span></span>

- [<span data-ttu-id="239f8-136">Gæðastjórnunaryfirlit</span><span class="sxs-lookup"><span data-stu-id="239f8-136">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="239f8-137">Virkja stjórnun gæða og ósamkvæmni</span><span class="sxs-lookup"><span data-stu-id="239f8-137">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="239f8-138">Starfsmenn ábyrgir fyrir samþykki ósamkvæmni</span><span class="sxs-lookup"><span data-stu-id="239f8-138">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="239f8-139">Biðgeymslusvæði fyrir ósamkvæmi</span><span class="sxs-lookup"><span data-stu-id="239f8-139">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="239f8-140">Gerðir greininga fyrir ósamkvæmni</span><span class="sxs-lookup"><span data-stu-id="239f8-140">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="239f8-141">Gæðagjöld fyrir ósamkvæmi</span><span class="sxs-lookup"><span data-stu-id="239f8-141">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="239f8-142">Aðgerðir fyrir ósamkvæmni.</span><span class="sxs-lookup"><span data-stu-id="239f8-142">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="239f8-143">Gæðastjórnun fyrir vöruhúsaferli</span><span class="sxs-lookup"><span data-stu-id="239f8-143">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
