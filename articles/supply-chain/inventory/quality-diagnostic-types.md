---
title: Gerðir greininga fyrir ósamkvæmni
description: Í þessu efnisatriði er lýst hvernig eigi að nota og búa til greiningartegundir sem hægt er að nota með ósamkvæmi.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestDiagnosticType, InventTestCorrection
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b7a5c593f1d9e8f7a77f693f6e652e9355a985fb
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022277"
---
# <a name="diagnostic-types-for-nonconformances"></a><span data-ttu-id="2b453-103">Gerðir greininga fyrir ósamkvæmni</span><span class="sxs-lookup"><span data-stu-id="2b453-103">Diagnostic types for nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2b453-104">Í þessu efnisatriði er lýst hvernig eigi að nota og búa til greiningartegundir sem hægt er að nota með ósamkvæmi.</span><span class="sxs-lookup"><span data-stu-id="2b453-104">This topic describes how to use and create diagnostic types that can be used with nonconformances.</span></span>

<span data-ttu-id="2b453-105">Notaðu **Greiningargerðir** síðuna til að skilgreina flokkun greiningaraðgerða.</span><span class="sxs-lookup"><span data-stu-id="2b453-105">You use the **Diagnostic types** page to define a classification of diagnostic actions.</span></span> <span data-ttu-id="2b453-106">Þegar leiðrétting er svo stofnuð vegna ósamræmis er greining valin.</span><span class="sxs-lookup"><span data-stu-id="2b453-106">Then, when you create a correction for a nonconformance, you select a diagnostic.</span></span> <span data-ttu-id="2b453-107">Leiðrétting auðkennir hvers konar greiningaraðgerð á að framkvæma á samþykktri ósamkvæmni, hver á að framkvæma hana.</span><span class="sxs-lookup"><span data-stu-id="2b453-107">A correction specifies what type of diagnostic action should be taken for an approved nonconformance, and who should take that action.</span></span> <span data-ttu-id="2b453-108">Hún tilgreinir einnig umbeðin lokadagsetning og áætluð lokadagsetning.</span><span class="sxs-lookup"><span data-stu-id="2b453-108">It also specifies the requested completion date and the planned completion date.</span></span>

## <a name="examples-of-diagnostic-types"></a><span data-ttu-id="2b453-109">Dæmi um greiningagerðir</span><span class="sxs-lookup"><span data-stu-id="2b453-109">Examples of diagnostic types</span></span>

<span data-ttu-id="2b453-110">Þú vinnur hjá framleiðslufyrirtæki og nokkrar vörur hafa fallið á gæðaprófunum.</span><span class="sxs-lookup"><span data-stu-id="2b453-110">You work for a manufacturing company, and several items have failed quality tests.</span></span> <span data-ttu-id="2b453-111">Þessir hlutir eru fluttir inn á biðgeymsluna og merktir sem ósamræmdar vörur.</span><span class="sxs-lookup"><span data-stu-id="2b453-111">Those items are moved into a quarantine area and marked as nonconforming products.</span></span> <span data-ttu-id="2b453-112">Ósamkvæmniskýrsla er stofnuð í Microsoft Dynamics 365 Supply Chain Management til að rekja upplýsingar í gegnum lausn vandamála.</span><span class="sxs-lookup"><span data-stu-id="2b453-112">A nonconformance record is created in Microsoft Dynamics 365 Supply Chain Management to track the details through issue resolution.</span></span>

<span data-ttu-id="2b453-113">Í þessu tilviki eiga gæðavandamálin sér stað vegna þess að legur í vélinni sem pakkar vörunum hafa skemmst og ofhitna.</span><span class="sxs-lookup"><span data-stu-id="2b453-113">In this case, the quality issues are occurring because bearings in the machine that packages the items have gone bad and are overheating.</span></span> <span data-ttu-id="2b453-114">Lausnin við þessu vandamáli er að skipta um íhluti í vélinni.</span><span class="sxs-lookup"><span data-stu-id="2b453-114">The correction for this problem is to replace the parts in the machine.</span></span>

<span data-ttu-id="2b453-115">Þegar þú skilgreinir greiningargerðirnar geturðu stofnað margar færslur, hver þeirra stendur fyrir mismunandi tegundir vandamála sem steðja að vélinni.</span><span class="sxs-lookup"><span data-stu-id="2b453-115">When you configure the diagnostic types, you can create multiple records, each of which represents a different type of problem that the machine might have.</span></span> <span data-ttu-id="2b453-116">Einnig er hægt að stofna eina almenna greiningartegund sem táknar vélarviðgerð.</span><span class="sxs-lookup"><span data-stu-id="2b453-116">Alternatively, you can create one generic diagnostic type that represents machine repair.</span></span>

## <a name="create-a-diagnostic-type"></a><span data-ttu-id="2b453-117">Stofna gerð greiningar</span><span class="sxs-lookup"><span data-stu-id="2b453-117">Create a diagnostic type</span></span>

1. <span data-ttu-id="2b453-118">Fara í **Birgðastjórnun \> Uppsetningu \> gæðastjórnun \> gerðir Greininga**.</span><span class="sxs-lookup"><span data-stu-id="2b453-118">Go to **Inventory management \> Setup \> Quality management \> Diagnostic types**.</span></span>
1. <span data-ttu-id="2b453-119">Á aðgerðasvæðinu skal velja **Ný** til að bæta línu við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="2b453-119">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="2b453-120">Stillið svo eftirfarandi reiti fyrir nýju línuna:</span><span class="sxs-lookup"><span data-stu-id="2b453-120">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="2b453-121">**Greining** – Færið inn einkvæmt kenni eða heiti fyrir greiningargerðina.</span><span class="sxs-lookup"><span data-stu-id="2b453-121">**Diagnostic** – Enter a unique ID or name for the diagnostic type.</span></span>
    - <span data-ttu-id="2b453-122">**Lýsing** – Færið inn ítarlega lýsingu á greiningargerðinni.</span><span class="sxs-lookup"><span data-stu-id="2b453-122">**Description** – Enter a detailed description of the diagnostic type.</span></span>

1. <span data-ttu-id="2b453-123">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="2b453-123">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2b453-124">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="2b453-124">Additional resources</span></span>

- [<span data-ttu-id="2b453-125">Gæðastjórnunaryfirlit</span><span class="sxs-lookup"><span data-stu-id="2b453-125">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="2b453-126">Virkja stjórnun gæða og ósamkvæmni</span><span class="sxs-lookup"><span data-stu-id="2b453-126">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="2b453-127">Starfsmenn ábyrgir fyrir samþykki ósamkvæmni</span><span class="sxs-lookup"><span data-stu-id="2b453-127">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="2b453-128">Biðgeymslusvæði fyrir ósamkvæmi</span><span class="sxs-lookup"><span data-stu-id="2b453-128">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="2b453-129">Gerðir vandamála fyrir ósamkvæmni</span><span class="sxs-lookup"><span data-stu-id="2b453-129">Problem types for nonconformances</span></span>](quality-problem-types.md)
- [<span data-ttu-id="2b453-130">Gæðagjöld fyrir ósamkvæmi</span><span class="sxs-lookup"><span data-stu-id="2b453-130">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="2b453-131">Aðgerðir fyrir ósamkvæmni.</span><span class="sxs-lookup"><span data-stu-id="2b453-131">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="2b453-132">Gæðastjórnun fyrir vöruhúsaferli</span><span class="sxs-lookup"><span data-stu-id="2b453-132">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
