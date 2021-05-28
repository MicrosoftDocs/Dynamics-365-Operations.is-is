---
title: Gjöld vegna ósamkvæmniaðgerða
description: Í þessu efnisatriði er lýst hvernig á að stofna gæðagjöld sem hægt er að nota við aðgerðir vegna ósamkvæmni.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestMiscCharges
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 382890232bff47a885840af1eb7e91d27bb46cae
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022301"
---
# <a name="charges-for-nonconformance-operations"></a><span data-ttu-id="970e8-103">Gjöld vegna ósamkvæmniaðgerða</span><span class="sxs-lookup"><span data-stu-id="970e8-103">Charges for nonconformance operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="970e8-104">Í þessu efnisatriði er lýst hvernig á að stofna gæðagjöld sem hægt er að nota við aðgerðir vegna ósamkvæmni.</span><span class="sxs-lookup"><span data-stu-id="970e8-104">This topic describes how to create quality charges that can be used with operations for a nonconformance.</span></span>

<span data-ttu-id="970e8-105">Þú notar síðuna **Gæðagjöld** til að skilgreina gerðir gjalda sem hægt er að bæta við aðgerðir vegna ósamkvæmi.</span><span class="sxs-lookup"><span data-stu-id="970e8-105">You use the **Quality charges** page to define the types of charges that can be added to operations for a nonconformance.</span></span> <span data-ttu-id="970e8-106">Gjöld gera þér kleift að fylgjast með upplýsingum um þóknanir eða gjöld sem þú skuldar viðskiptavini fyrir afurðir sem eru ekki í samræmi eða sem lánardrotinn skuldar þér fyrir afurðir sem eru ekki í samræmi við það sem þú fékkst.</span><span class="sxs-lookup"><span data-stu-id="970e8-106">Charges let you track details about fees or charges that you owe to a customer for nonconforming products, or that a vendor owes to you for nonconforming products that you received.</span></span> <span data-ttu-id="970e8-107">Þú gætir einnig notað gjöld til að fylgjast með kostnaði sem þarf fyrir ytri lánardrottna eða þjónustu til að framkvæma aðgerð.</span><span class="sxs-lookup"><span data-stu-id="970e8-107">You might also use charges to track costs that are required for external vendors or services to perform an operation.</span></span>

## <a name="examples-of-quality-charges"></a><span data-ttu-id="970e8-108">Dæmi um gæðagjöld</span><span class="sxs-lookup"><span data-stu-id="970e8-108">Examples of quality charges</span></span>

<span data-ttu-id="970e8-109">Þú vinnur fyrir framleiđslufyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="970e8-109">You work for a manufacturing company.</span></span> <span data-ttu-id="970e8-110">Fyrirtæki þitt er með samninga við nokkra lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="970e8-110">Your company has contracts with several vendors.</span></span> <span data-ttu-id="970e8-111">Í þeim samningum eru sett fram viðmið um sendingar á réttum tíma, tjón og vörugæði.</span><span class="sxs-lookup"><span data-stu-id="970e8-111">Those contracts outline standards for on-time shipment, damages, and product quality for items.</span></span> <span data-ttu-id="970e8-112">Sömuleiðis hafa nokkrir viðskiptavinir þinna gert samninga við fyrirtækið um skil, tjón og gæði vöru.</span><span class="sxs-lookup"><span data-stu-id="970e8-112">Likewise, several of your customers have agreements with your company about returns, damages, and product quality.</span></span>

<span data-ttu-id="970e8-113">Skipulag þóknunar er skilgreint fyrir hverjar kringumstæður og tilgreint í samningnum.</span><span class="sxs-lookup"><span data-stu-id="970e8-113">A fee structure is defined for each circumstance and specified in the contract.</span></span> <span data-ttu-id="970e8-114">Hægt er að skilgreina gæðagjöld til að útlista ýmsar gerðir gjalda á borð við *Skemmdir*, *Tafir á sendingu* og *Gæði*.</span><span class="sxs-lookup"><span data-stu-id="970e8-114">You can configure quality charges to outline the various types of charges, such as *Damages*, *Late shipment*, and *Quality*.</span></span> <span data-ttu-id="970e8-115">Þegar ósamræmi er svo stofnað er bætt við einni eða fleiri aðgerðum.</span><span class="sxs-lookup"><span data-stu-id="970e8-115">Then, when you create a nonconformance, you add one or more operations.</span></span> <span data-ttu-id="970e8-116">Fyrir hverja aðgerð velur þú **Gjöld** til að skilgreina upplýsingar um þóknanirnar.</span><span class="sxs-lookup"><span data-stu-id="970e8-116">For each operation, you select **Charges** to define the details about the fees.</span></span>

## <a name="create-a-quality-charge"></a><span data-ttu-id="970e8-117">Stofna gæðagjald</span><span class="sxs-lookup"><span data-stu-id="970e8-117">Create a quality charge</span></span>

1. <span data-ttu-id="970e8-118">Fara í **Birgðastjórnun \> Uppsetning \> Gæðaeftirlit \> Gæðastjórnunargjöld**.</span><span class="sxs-lookup"><span data-stu-id="970e8-118">Go to **Inventory management \> Setup \> Quality management \> Quality charges**.</span></span>
1. <span data-ttu-id="970e8-119">Á aðgerðasvæðinu skal velja **Ný** til að bæta línu við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="970e8-119">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="970e8-120">Stillið svo eftirfarandi reiti fyrir nýju línuna:</span><span class="sxs-lookup"><span data-stu-id="970e8-120">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="970e8-121">**Gjaldakóði** – Færið inn einkvæmt kenni eða heiti fyrir gæðagjaldið.</span><span class="sxs-lookup"><span data-stu-id="970e8-121">**Charges code** – Enter a unique ID or name for the quality charge.</span></span>
    - <span data-ttu-id="970e8-122">**Lýsing** – Færið inn ítarlega lýsingu á gæðagjaldinu.</span><span class="sxs-lookup"><span data-stu-id="970e8-122">**Description** – Enter a detailed description of the quality charge.</span></span>

1. <span data-ttu-id="970e8-123">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="970e8-123">Close the page.</span></span>

## <a name="add-a-quality-charge-to-an-operation-for-a-nonconformance"></a><span data-ttu-id="970e8-124">Bæta gæðagjaldi við aðgerð vegna ósamkvæmis</span><span class="sxs-lookup"><span data-stu-id="970e8-124">Add a quality charge to an operation for a nonconformance</span></span>

<span data-ttu-id="970e8-125">Frekari upplýsingar um hvernig á að bæta aðgerðum við ósamkvæmni og setja gjöld á hana er að finna í [Aðgerðir fyrir ósamkvæmni](quality-operations.md).</span><span class="sxs-lookup"><span data-stu-id="970e8-125">For details about how to add operations to a nonconformance and apply charges to them, see [Operations for nonconformances](quality-operations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="970e8-126">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="970e8-126">Additional resources</span></span>

- [<span data-ttu-id="970e8-127">Gæðastjórnunaryfirlit</span><span class="sxs-lookup"><span data-stu-id="970e8-127">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="970e8-128">Virkja stjórnun gæða og ósamkvæmni</span><span class="sxs-lookup"><span data-stu-id="970e8-128">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="970e8-129">Starfsmenn ábyrgir fyrir samþykki ósamkvæmni</span><span class="sxs-lookup"><span data-stu-id="970e8-129">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="970e8-130">Biðgeymslusvæði fyrir ósamkvæmi</span><span class="sxs-lookup"><span data-stu-id="970e8-130">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="970e8-131">Gerðir greininga fyrir ósamkvæmni</span><span class="sxs-lookup"><span data-stu-id="970e8-131">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="970e8-132">Gæðagjöld fyrir ósamkvæmi</span><span class="sxs-lookup"><span data-stu-id="970e8-132">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="970e8-133">Aðgerðir fyrir ósamkvæmni.</span><span class="sxs-lookup"><span data-stu-id="970e8-133">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="970e8-134">Gæðastjórnun fyrir vöruhúsaferli</span><span class="sxs-lookup"><span data-stu-id="970e8-134">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
