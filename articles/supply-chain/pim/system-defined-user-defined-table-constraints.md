---
title: kerfisskilgreindar og notandaskilgreindar taflaskorður.
description: 'Þessi grein útskýrir hinar tvær tegundir töfluskorða fyrir íhluti í skilgreiningarlíkani afurðar: Skilgreint af notanda og skilgreint af kerfi. Töfluskorður standa fyrir fylki leyfðra eigindasamsetninga þar sem hver röð skilgreinir eitt safn mögulegra eigindagilda.'
author: cvocph
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PCTableConstraintAttachAttributeTree, PCTableConstraintColumnSystem, PCTableConstraintContentUserDef, PCTableConstraintDefinition, PCTableConstraintWizard
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19781
ms.assetid: 0a4ea930-b344-43a8-871e-d5cd077892c4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 35ea5b97708272edf50f09d892088bcd3e07402d
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/04/2021
ms.locfileid: "6187968"
---
# <a name="system-defined-and-user-defined-table-constraints"></a><span data-ttu-id="90cee-104">kerfisskilgreindar og notandaskilgreindar taflaskorður.</span><span class="sxs-lookup"><span data-stu-id="90cee-104">System-defined and user-defined table constraints</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="90cee-105">Þessi grein útskýrir hinar tvær tegundir töfluskorða fyrir íhluti í skilgreiningarlíkani afurðar: Skilgreint af notanda og skilgreint af kerfi.</span><span class="sxs-lookup"><span data-stu-id="90cee-105">This article explains the two types of table constraints for components in a product configuration model -  user-defined and system-defined.</span></span> <span data-ttu-id="90cee-106">Töfluskorður standa fyrir fylki leyfðra eigindasamsetninga þar sem hver röð skilgreinir eitt safn mögulegra eigindagilda.</span><span class="sxs-lookup"><span data-stu-id="90cee-106">Table constraints represent matrices of the allowed attribute combinations, where each row defines one set of possible attribute values.</span></span>

<span data-ttu-id="90cee-107">Töfluskorður tákna fylki samsetninga eiginds sem  eru leyfðar fyrir íhluti í afbrigðalíkani afurðar.</span><span class="sxs-lookup"><span data-stu-id="90cee-107">Table constraints represent matrices of the combinations of attributes that are allowed for components in a product configuration model.</span></span> <span data-ttu-id="90cee-108">Hver lína í töflunni skilgreinir eitt safn mögulegra eigindagilda.</span><span class="sxs-lookup"><span data-stu-id="90cee-108">Each row in the table defines one set of possible attribute values.</span></span> <span data-ttu-id="90cee-109">Hægt er að telja fram tvær gerðir skorða í afbrigðalíkani afurðar:</span><span class="sxs-lookup"><span data-stu-id="90cee-109">You can declare two types of constraints in a product configuration model:</span></span>

-   <span data-ttu-id="90cee-110">**Segðarskorða** – Stofna segð sem skilgreinir vensl milli eiginda til að tryggja að hægt er að velja aðeins samhæf gildi við skilgreiningu afurðar.</span><span class="sxs-lookup"><span data-stu-id="90cee-110">**Expression constraint** – Create an expression that defines relations between attributes to guarantee that only compatible values can be selected during product configuration.</span></span>
-   <span data-ttu-id="90cee-111">**Töfluskorða** – Búa til töflu sem skilgreinir allar samsetningar sem eru leyfðar fyrir tilgreint safn eiginleika.</span><span class="sxs-lookup"><span data-stu-id="90cee-111">**Table constraint** – Create a table that defines all the combinations that are allowed for a specified set of attributes.</span></span> <span data-ttu-id="90cee-112">Tvær gerðir af töfluskorðum eru tiltækar: notandaskilgreindur töfluskorðum og kerfisskilgreindar töfluskorðum.</span><span class="sxs-lookup"><span data-stu-id="90cee-112">Two types of table constraints are available: user-defined table constraints and system-defined table constraints.</span></span>

<span data-ttu-id="90cee-113">Þessi skrá lýsir notandaskilgreindur og kerfisskilgreindar töfluskorðum fyrir íhluti í afbrigðalíkani afurðar.</span><span class="sxs-lookup"><span data-stu-id="90cee-113">This article describes user-defined and system-defined table constraints for components in a product configuration model.</span></span>

## <a name="user-defined-table-constraints"></a><span data-ttu-id="90cee-114">Notandaskilgreind töfluskorða</span><span class="sxs-lookup"><span data-stu-id="90cee-114">User-defined table constraints</span></span>
<span data-ttu-id="90cee-115">Notandaskilgreind töfluskorða er gerð fylkis sem má nota til að lýsa samsetningu fyrir eigindagildin sem eru skilgreind í eigindagerðum.</span><span class="sxs-lookup"><span data-stu-id="90cee-115">A user-defined table constraint is a type of matrix that is used to describe the combinations of attribute values that are defined by attribute types.</span></span> <span data-ttu-id="90cee-116">Til dæmis, ef þú framleiðir hátalara geturðu haft með dálk fyrir áferð hússins og framgrillið í notandaskilgreindu töfluskorðunni.</span><span class="sxs-lookup"><span data-stu-id="90cee-116">For example, if you produce speakers, you can include columns for the cabinet finish and the front grill in the user-defined table constraint.</span></span> <span data-ttu-id="90cee-117">Gerð eigindar fyrir áferð hússins hefur fjögur gildi og eigindargerð fyrir framgrill hefur þrjú gildi.</span><span class="sxs-lookup"><span data-stu-id="90cee-117">The attribute type for the cabinet finish has four values, and the attribute type for the front grill has three values.</span></span> <span data-ttu-id="90cee-118">Þess vegna ef ekki eru notuð skorður eru 4 × 3 = 12 mögulegar samsetningar.</span><span class="sxs-lookup"><span data-stu-id="90cee-118">Therefore, if constraints aren't used, there are 4 × 3 = 12 possible combinations.</span></span> <span data-ttu-id="90cee-119">Hins vegar í þessu dæmi eru aðeins sex samsetningar leyfðar, eins og sýnt er í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="90cee-119">However, in this example, only six combinations are allowed, as shown in the following table.</span></span> <span data-ttu-id="90cee-120">Þessar upplýsingar birtast í á **Leyfðar samsetningar** flipanum á í **Breyta töfluskorðu** síðu.</span><span class="sxs-lookup"><span data-stu-id="90cee-120">This information is displayed on the **Allowed combinations** tab on the **Edit table constraint** page.</span></span>

| <span data-ttu-id="90cee-121">Ljúka cabinet</span><span class="sxs-lookup"><span data-stu-id="90cee-121">Cabinet finish</span></span> | <span data-ttu-id="90cee-122">Framgrill</span><span class="sxs-lookup"><span data-stu-id="90cee-122">Front grill</span></span> |
|----------------|-------------|
| <span data-ttu-id="90cee-123">Svart</span><span class="sxs-lookup"><span data-stu-id="90cee-123">Black</span></span>          | <span data-ttu-id="90cee-124">Svart</span><span class="sxs-lookup"><span data-stu-id="90cee-124">Black</span></span>       |
| <span data-ttu-id="90cee-125">Svart</span><span class="sxs-lookup"><span data-stu-id="90cee-125">Black</span></span>          | <span data-ttu-id="90cee-126">Málmur</span><span class="sxs-lookup"><span data-stu-id="90cee-126">Metal</span></span>       |
| <span data-ttu-id="90cee-127">Eik</span><span class="sxs-lookup"><span data-stu-id="90cee-127">Oak</span></span>            | <span data-ttu-id="90cee-128">Svart</span><span class="sxs-lookup"><span data-stu-id="90cee-128">Black</span></span>       |
| <span data-ttu-id="90cee-129">Rósaviður</span><span class="sxs-lookup"><span data-stu-id="90cee-129">Rosewood</span></span>       | <span data-ttu-id="90cee-130">Hvítt</span><span class="sxs-lookup"><span data-stu-id="90cee-130">White</span></span>       |
| <span data-ttu-id="90cee-131">Hvítt</span><span class="sxs-lookup"><span data-stu-id="90cee-131">White</span></span>          | <span data-ttu-id="90cee-132">Svart</span><span class="sxs-lookup"><span data-stu-id="90cee-132">Black</span></span>       |
| <span data-ttu-id="90cee-133">Hvítt</span><span class="sxs-lookup"><span data-stu-id="90cee-133">White</span></span>          | <span data-ttu-id="90cee-134">Hvítt</span><span class="sxs-lookup"><span data-stu-id="90cee-134">White</span></span>       |

<span data-ttu-id="90cee-135">Notandaskilgreind töfluskorðum eru skilgreindar eftir ílag fastrar töflu sem vinnur á sama hátt og segðarskorða.</span><span class="sxs-lookup"><span data-stu-id="90cee-135">User-defined table constraints are defined by static table input that works the same way as an expression constraint.</span></span> <span data-ttu-id="90cee-136">Þegar notendaskilgreinda töfluskorðu er notuð, er kosturinn að töflur eru oft auðveldara að stofna, skilja og viðhalda en langar segðarskorður.</span><span class="sxs-lookup"><span data-stu-id="90cee-136">When you use a user-defined table constraint, the advantage is that tables are often easier to create, understand, and maintain than long expression constraints.</span></span>

## <a name="system-defined-table-constraints"></a><span data-ttu-id="90cee-137">kerfisskilgreindar töfluskorður</span><span class="sxs-lookup"><span data-stu-id="90cee-137">System-defined table constraints</span></span>
<span data-ttu-id="90cee-138">Kerfisskilgreind töfluskorða stpfmar gagnvirkri vörpun á milli gerð eigindar og svæðis í töflu.</span><span class="sxs-lookup"><span data-stu-id="90cee-138">A system-defined table constraint creates a dynamic mapping between an attribute type and a field in a table.</span></span> <span data-ttu-id="90cee-139">Þegar kerfisskilgreindar töfluskorða er höfð með í afbrigðalíkani afurðar tryggir vörpun að gögn í töflunni er sýnd í stað gilda fyrir gerð eigindar.</span><span class="sxs-lookup"><span data-stu-id="90cee-139">When a system-defined table constraint is included in a product configuration model, the mapping guarantees that the data in the table is shown instead of the values of the attribute type.</span></span> <span data-ttu-id="90cee-140">Niðurstaðan er breytileg töfluskorða þar sem hægt er að breyta innihaldi töflu (til dæmis, með öðrum kerfum).</span><span class="sxs-lookup"><span data-stu-id="90cee-140">The result is a dynamic constraint, because the table contents can be modified (for example, by other modules).</span></span>  

<span data-ttu-id="90cee-141">Þegar-kerfisskilgreindrar töfluskorðu er stofnuð er velja töflu, einnig er hægt að skilgreina fyrirspurn til að nota og tengja svo gerðir eiginda í svæði í valinni töflu.</span><span class="sxs-lookup"><span data-stu-id="90cee-141">When you create a system-defined table constraint, you select a table, optionally define the query to use, and then associate attribute types to the fields in the selected table.</span></span> <span data-ttu-id="90cee-142">Gerðir svæða verður að samsvara gerðum gerða eiginda.</span><span class="sxs-lookup"><span data-stu-id="90cee-142">The types of fields must match the types of attribute types.</span></span>  

<span data-ttu-id="90cee-143">Áður en töfluskorðu getur tekið gildi í afbrigðalíkani afurðar, verður töfluskorðunni að vera innifalin í skorðu í einum af íhlutum líkans.</span><span class="sxs-lookup"><span data-stu-id="90cee-143">Before a table constraint can take effect on a product configuration model, the table constraint must be included in a constraint on one of the model's components.</span></span> <span data-ttu-id="90cee-144">Ferlið er að stofna nýja skorðu, velja gerð töfluskorðu og veljið síðan skilgreiningu töfluskorðu sem nota á.</span><span class="sxs-lookup"><span data-stu-id="90cee-144">The procedure is to create a new constraint, select the table constraint type, and then select the table constraint definition to use.</span></span> <span data-ttu-id="90cee-145">Loks, öll svæði í töfluskorðunni verða að varpa eigindum í afbrigðalíkani afurðar.</span><span class="sxs-lookup"><span data-stu-id="90cee-145">Finally, all fields in the table constraint must be mapped to attributes in the product configuration model.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="90cee-146">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="90cee-146">Additional resources</span></span>

[<span data-ttu-id="90cee-147">Yfirlit afbrigðalíkön afurðar</span><span class="sxs-lookup"><span data-stu-id="90cee-147">Product configuration models overview</span></span>](product-configuration-models.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]