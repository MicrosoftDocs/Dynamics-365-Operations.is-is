---
title: Tilvísanir í upprunalega reikninga í kreditnótum
description: Þetta efnisatriði útskýrir hvernig á að setja upp og prenta upprunaleg reikningsnúmer í tengdum kreditnótum.
author: ilkond
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 8d7f32c5d3d29be8d1d2742c4017c1719cbd47a8
ms.sourcegitcommit: 7d0cfb359a4abc7392ddb3f0b3e9539c40b7204d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/14/2021
ms.locfileid: "5897333"
---
# <a name="references-to-original-invoices-in-credit-notes"></a><span data-ttu-id="df23d-103">Tilvísanir í upprunalega reikninga í kreditnótum</span><span class="sxs-lookup"><span data-stu-id="df23d-103">References to original invoices in credit notes</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="df23d-104">Í sumum löndum og svæðum er lagaleg krafa um að prentaðar kreditnótur innihaldi tilvísanir í upprunalega reikninga.</span><span class="sxs-lookup"><span data-stu-id="df23d-104">In some countries and regions, there is a legal requirement that printed credit notes include references to the original invoices.</span></span> <span data-ttu-id="df23d-105">Þetta efnisatriði útskýrir hvernig á að setja upp og prenta upprunaleg reikningsnúmer í tengdum kreditnótum.</span><span class="sxs-lookup"><span data-stu-id="df23d-105">This topic explains how to set up and print the original invoice numbers in related credit notes.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="df23d-106">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="df23d-106">Prerequisites</span></span>

- <span data-ttu-id="df23d-107">Á vinnusvæðinu **Eiginleikastjórnun** skal kveikja á eiginleikanum **Útlit kreditreikningsfærslu fyrir sölu- og verkreikningsskýrslur**.</span><span class="sxs-lookup"><span data-stu-id="df23d-107">In the **Feature management** workspace, turn on the **Credit invoicing layout for sales and project invoice reports** feature.</span></span> <span data-ttu-id="df23d-108">Frekari upplýsingar er að finna í [Eiginleikastjórnunaryfirlit](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="df23d-108">For more information, see [Feature management overview](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>
- <span data-ttu-id="df23d-109">Skilgreina þarf prentsnið fyrir nauðsynleg skjöl í Prentstýring.</span><span class="sxs-lookup"><span data-stu-id="df23d-109">The printable formats of the required documents must be configured in Print management.</span></span>

<span data-ttu-id="df23d-110">Virknin sem lýst er í þessu efnisatriði gildir um eftirfarandi skjöl:</span><span class="sxs-lookup"><span data-stu-id="df23d-110">The functionality that is described in this topic applies to the following documents:</span></span>

<span data-ttu-id="df23d-111">**Viðskiptakröfur**</span><span class="sxs-lookup"><span data-stu-id="df23d-111">**Accounts receivable**</span></span>

- <span data-ttu-id="df23d-112">Textakreditnóta</span><span class="sxs-lookup"><span data-stu-id="df23d-112">Free text credit note</span></span>
- <span data-ttu-id="df23d-113">Kreditnóta viðskiptavina</span><span class="sxs-lookup"><span data-stu-id="df23d-113">Customer credit note</span></span>

<span data-ttu-id="df23d-114">**Verkefnastjórnun og bókhald**</span><span class="sxs-lookup"><span data-stu-id="df23d-114">**Project management and accounting**</span></span>

- <span data-ttu-id="df23d-115">Kreditnóta verks</span><span class="sxs-lookup"><span data-stu-id="df23d-115">Project credit note</span></span>

## <a name="configure-accounts-receivable-parameters"></a><span data-ttu-id="df23d-116">Skilgreina færibreytur viðskiptakrafna</span><span class="sxs-lookup"><span data-stu-id="df23d-116">Configure Accounts receivable parameters</span></span>

<span data-ttu-id="df23d-117">Fylgið þessum skrefum til að stilla færibreytur sem stýra því hvort tilvísanir í upprunalega reikninga séu prentaðar í tengdum kreditnótum.</span><span class="sxs-lookup"><span data-stu-id="df23d-117">Follow these steps to set the parameter that controls whether references to the original invoices are printed in related credit notes.</span></span>

1. <span data-ttu-id="df23d-118">Farðu í **Viðskiptakröfur** \> **Uppsetning** \> **Færibreytur viðskiptakröfu**.</span><span class="sxs-lookup"><span data-stu-id="df23d-118">Go to **Accounts receivable** \> **Setup** \> **Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="df23d-119">Í flipanum **Uppfærslur**, í flýtiflipanum **Reikningur**, skal stilla valkostinn **Nota útlit kreditreikningsfærslu í sölu- og verkreikningaskýrslum** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="df23d-119">On the **Updates** tab, on the **Invoice** FastTab, set the **Apply the credit invoicing layout into sales and project invoice reports** option to **Yes**.</span></span>

![Færibreytur viðskiptakrafna skilgreindar](media/original-invoice-number-in-credit-note.jpg)

## <a name="define-references-to-original-invoices"></a><span data-ttu-id="df23d-121">Skilgreina tilvísanir í upprunalega reikninga</span><span class="sxs-lookup"><span data-stu-id="df23d-121">Define references to original invoices</span></span>

<span data-ttu-id="df23d-122">Notið eftirfarandi ferli til að skilgreina tilvísanir í upprunalega reikninga, samkvæmt gerð skjals.</span><span class="sxs-lookup"><span data-stu-id="df23d-122">Use the following procedures to define references to original invoices, based on the document type.</span></span>

### <a name="free-text-credit-note"></a><span data-ttu-id="df23d-123">Textakreditnóta</span><span class="sxs-lookup"><span data-stu-id="df23d-123">Free text credit note</span></span>

1. <span data-ttu-id="df23d-124">Fara í **Viðskiptakröfur** \> **Reikningar** \> **Allir reikningar með frjálsum texta**.</span><span class="sxs-lookup"><span data-stu-id="df23d-124">Go to **Accounts receivable** \> **Invoices** \> **All free text invoices**.</span></span>
2. <span data-ttu-id="df23d-125">Stofnið nýja kreditnótu eða veljið fyrirliggjandi kreditnótu.</span><span class="sxs-lookup"><span data-stu-id="df23d-125">Create a new credit note, or select an existing credit note.</span></span>
3. <span data-ttu-id="df23d-126">Opnið reikninginn.</span><span class="sxs-lookup"><span data-stu-id="df23d-126">Open the invoice.</span></span>
4. <span data-ttu-id="df23d-127">Á aðgerðasvæðinu, í flipanum **Reikningur**, í flokknum **Aðgerðir**, skal velja **Kreditreikningsfærsla**.</span><span class="sxs-lookup"><span data-stu-id="df23d-127">On the Action Pane, on the **Invoice** tab, in the **Functions** group, select **Credit invoicing**.</span></span>
5. <span data-ttu-id="df23d-128">Færið inn tilvísunina í upprunalegan reikning og veljið ástæðu leiðréttingarinnar.</span><span class="sxs-lookup"><span data-stu-id="df23d-128">Enter the reference to the original invoice, and select the reason for the correction.</span></span>

![Tilvísun fyrir reikning með frjálsum texta skilgreind](media/reference-original-invoice-FTI.jpg)

### <a name="customer-credit-note"></a><span data-ttu-id="df23d-130">Kreditnóta viðskiptavina</span><span class="sxs-lookup"><span data-stu-id="df23d-130">Customer credit note</span></span>

1. <span data-ttu-id="df23d-131">Farið í **Viðskiptakröfur** \> **Pantanir** \> **Allar sölupantanir**.</span><span class="sxs-lookup"><span data-stu-id="df23d-131">Go to **Accounts receivable** \> **Orders** \> **All sales orders**.</span></span>
2. <span data-ttu-id="df23d-132">Veljið og opnið reikningsfærða sölupöntun sem þarf að leiðrétta.</span><span class="sxs-lookup"><span data-stu-id="df23d-132">Select and open the invoiced sales order that must be corrected.</span></span>
3. <span data-ttu-id="df23d-133">Á aðgerðasvæðinu, í flipanum **Selja**, í flokknum **Kreditnóta**, skal velja **Kreditnóta**.</span><span class="sxs-lookup"><span data-stu-id="df23d-133">On the Action Pane, on the **Sell** tab, in the **Credit note** group, select **Credit note**.</span></span>
4. <span data-ttu-id="df23d-134">Færið inn ástæðu leiðréttingarinnar.</span><span class="sxs-lookup"><span data-stu-id="df23d-134">Enter the reason for the correction.</span></span> <span data-ttu-id="df23d-135">Tilvísun í upprunalegan reikning er komið fyrir sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="df23d-135">The reference to the original invoice is automatically established.</span></span>

![Tilvísun fyrir sölupöntun skilgreind](media/reference-original-invoice-SO.jpg)

### <a name="project-credit-note"></a><span data-ttu-id="df23d-137">Kreditnóta verks</span><span class="sxs-lookup"><span data-stu-id="df23d-137">Project credit note</span></span>

1. <span data-ttu-id="df23d-138">Farið í **Verkefnastjórnun og bókhald** \> **Verkreikningar** \> **Verkreikningar**.</span><span class="sxs-lookup"><span data-stu-id="df23d-138">Go to **Project management and accounting** \> **Project invoices** \> **Project invoices**.</span></span>
2. <span data-ttu-id="df23d-139">Veljið og opnið verkreikning sem á að leiðrétta.</span><span class="sxs-lookup"><span data-stu-id="df23d-139">Select and open the project invoice that must be corrected.</span></span>
3. <span data-ttu-id="df23d-140">Á aðgerðasvæðinu, í flipanum **Verkreikningur**, í flokknum **Aðgerðir**, skal velja **Velja fyrir kreditnótu**.</span><span class="sxs-lookup"><span data-stu-id="df23d-140">On the Action Pane, on the **Project invoice** tab, in the **Functions** group, select **Select for credit note**.</span></span>
4. <span data-ttu-id="df23d-141">Veljið **Kreditreikningsfærsla**.</span><span class="sxs-lookup"><span data-stu-id="df23d-141">Select **Credit invoicing**.</span></span>
5. <span data-ttu-id="df23d-142">Færið inn ástæðu leiðréttingarinnar.</span><span class="sxs-lookup"><span data-stu-id="df23d-142">Enter the reason for the correction.</span></span> <span data-ttu-id="df23d-143">Tilvísun í upprunalegan reikning er komið fyrir sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="df23d-143">The reference to the original invoice is automatically established.</span></span>

![Tilvísun fyrir verkreikning skilgreind](media/reference-original-invoice-project.jpg)

## <a name="printing-credit-notes"></a><span data-ttu-id="df23d-145">Kreditnótur prentaðar</span><span class="sxs-lookup"><span data-stu-id="df23d-145">Printing credit notes</span></span>

<span data-ttu-id="df23d-146">Þegar kreditnótur með frjálsum texta, fyrir viðskiptavini og verk eru prentaðar munu þær innihalda tilvísunina í upprunalegan reikning og ástæðu leiðréttingar.</span><span class="sxs-lookup"><span data-stu-id="df23d-146">When you print free text, customer, and project credit notes, they will include the reference to the original invoice and the correction reason.</span></span>

![Prentuð kreditnóta](media/credit-note-FTI.jpg)

> [!NOTE]
> <span data-ttu-id="df23d-148">Gangið úr skugga um að prentvæn snið skjalanna séu rétt skilgreind með það í huga að tilvísanir í upprunalega reikninga verði prentaðar.</span><span class="sxs-lookup"><span data-stu-id="df23d-148">Make sure that the printable formats of the documents are correctly configured, on the assumption that references to original invoices will be printed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]