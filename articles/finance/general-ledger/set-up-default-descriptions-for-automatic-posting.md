---
title: Setja upp sjálfgefnar lýsingar fyrir sjálfvirka bókun
description: Þetta efnisatriði útskýrir hvernig hægt er að setja upp sjálfgefinn texta sem er notaður til að fylla í svæðið fyrir bókhaldsfærslur sem eru bókaðar sjálfkrafa í fjárhag. Fyrir allar færslugerðir er hægt að setja upp sjálfgefna lýsingu með því að nota frjálsan texta eða með því að velja fastar breytur.
author: aprilolson
manager: AnnBe
ms.date: 07/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 222564
ms.assetid: ''
ms.search.region: global
ms.author: aolson
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: eb89f50a3d227cad80226ce30f71c4f210129245
ms.sourcegitcommit: 0262a19e32b2c0c84c731d9f4fbe8ba91822afa3
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/15/2019
ms.locfileid: "2622690"
---
# <a name="set-up-default-descriptions-for-automatic-posting"></a><span data-ttu-id="3fcd0-104">Setja upp sjálfgefnar lýsingar fyrir sjálfvirka bókun</span><span class="sxs-lookup"><span data-stu-id="3fcd0-104">Set up default descriptions for automatic posting</span></span>

<span data-ttu-id="3fcd0-105">Þetta efnisatriði útskýrir hvernig hægt er að setja upp sjálfgefinn texta sem er notaður til að fylla í svæðið fyrir bókhaldsfærslur sem eru bókaðar sjálfkrafa í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="3fcd0-105">This topic explains how to set up default text that is used to describe accounting entries that are posted automatically to the general ledger.</span></span> <span data-ttu-id="3fcd0-106">Fyrir allar færslugerðir er hægt að setja upp sjálfgefna lýsingu með því að nota frjálsan texta eða með því að velja fastar breytur.</span><span class="sxs-lookup"><span data-stu-id="3fcd0-106">You can set up default description text by using free-form text or by selecting fixed variables.</span></span>

> [!NOTE]
> <span data-ttu-id="3fcd0-107">Fyrir sumar færslugerðir í sumum löndum eða svæðum, er einnig hægt að hafa með texta úr reitum í gagnagrunninum Microsoft Dynamics AX sem eru tengdar þessum færslugerðum.</span><span class="sxs-lookup"><span data-stu-id="3fcd0-107">For some transaction types in some countries or regions, you can also include text from fields in the Microsoft Dynamics AX database that are related to those transaction types.</span></span> <span data-ttu-id="3fcd0-108">Sjá lista yfir færslugerðir og lönd og svæði í kaflanum [Valfrjálst: Bæta öðrum texta við að sjálfgildar lýsingar](#optional-add-other-text-to-default-descriptions) síðar í þessu efni.</span><span class="sxs-lookup"><span data-stu-id="3fcd0-108">For a list of the transaction types, and the countries and regions, see the [Optional: Add other text to default descriptions](#optional-add-other-text-to-default-descriptions) section later in this topic.</span></span>

## <a name="set-up-default-descriptions"></a><span data-ttu-id="3fcd0-109">Setja upp sjálfgefnar lýsingar</span><span class="sxs-lookup"><span data-stu-id="3fcd0-109">Set up default descriptions</span></span>

1. <span data-ttu-id="3fcd0-110">Fara á **Fyrirtækisstjórnun** \> **Uppsetning** \> **Sjálfgefnar lýsingar**.</span><span class="sxs-lookup"><span data-stu-id="3fcd0-110">Go to **Organization administration** \> **Setup** \> **Default descriptions**.</span></span>
2. <span data-ttu-id="3fcd0-111">Í aðgerðarúðunni velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="3fcd0-111">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="3fcd0-112">Í reitnum **Lýsing** velurðu tegund færslunnar til að stofna sjálfgefna lýsingu fyrir.</span><span class="sxs-lookup"><span data-stu-id="3fcd0-112">In the **Description** field, select the type of transaction to create a default description for.</span></span>
4. <span data-ttu-id="3fcd0-113">Í svæðið **Tungumál** skal velja tungumálið sem lýsingin á við.</span><span class="sxs-lookup"><span data-stu-id="3fcd0-113">In the **Language** field, select the language that the description applies to.</span></span>
5. <span data-ttu-id="3fcd0-114">Í svæðið **Texti** skal slá inn sjálfgefna lýsingu.</span><span class="sxs-lookup"><span data-stu-id="3fcd0-114">In the **Text** field, enter the default description.</span></span> <span data-ttu-id="3fcd0-115">Hægt er að slá texta inn í svæðið, eða hægt er að nota eina eða fleiri af eftirfarandi breytum með frjálsum texta:</span><span class="sxs-lookup"><span data-stu-id="3fcd0-115">You can type text in the field, or you can use one or more of the following free-text variables:</span></span>

    - <span data-ttu-id="3fcd0-116">**%1** – Bæta við færsludagsetningunni.</span><span class="sxs-lookup"><span data-stu-id="3fcd0-116">**%1** – Add the transaction date.</span></span>
    - <span data-ttu-id="3fcd0-117">**%2** – Bæta við kenni sem svarar til skjaltegundarinnar sem er bókuð í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="3fcd0-117">**%2** – Add an identifier that corresponds to the document type that is being posted to the general ledger.</span></span> <span data-ttu-id="3fcd0-118">Til dæmis fyrir færslugerðir sem tengjast reikningum, bætir breytan **%2** reikningsnúmeri við.</span><span class="sxs-lookup"><span data-stu-id="3fcd0-118">For example, for transaction types that are related to invoices, the **%2** variable adds the invoice number.</span></span>
    - <span data-ttu-id="3fcd0-119">**%3** – Bæta við kenni sem tengist skjaltegundinni sem er bókuð í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="3fcd0-119">**%3** – Add an identifier that is related to the document type that is being posted to the general ledger.</span></span> <span data-ttu-id="3fcd0-120">Til dæmis fyrir færslugerðir sem tengjast reikningum, bætir breytan **%3** viðskiptavinalykli við.</span><span class="sxs-lookup"><span data-stu-id="3fcd0-120">For example, for transaction types that are related to invoices, the **%3** variable adds the customer account number.</span></span>

## <a name="optional-add-other-text-to-default-descriptions"></a><span data-ttu-id="3fcd0-121">Valfrjálst: Bæta öðrum texta við að sjálfgildar lýsingar</span><span class="sxs-lookup"><span data-stu-id="3fcd0-121">Optional: Add other text to default descriptions</span></span>

<span data-ttu-id="3fcd0-122">Fyrir sumar færslugerðir í sumum löndum eða svæðum, geta sjálfgefnar lýsingar innihaldið texta sem kemur úr reitunum í gögnum þínum sem tengjast þeim færslugerðum.</span><span class="sxs-lookup"><span data-stu-id="3fcd0-122">For some transaction types in some countries or regions, default descriptions can include text that comes from fields in your data that are related to those transaction types.</span></span> <span data-ttu-id="3fcd0-123">Eftirfarandi sýnir sýna færslugerðir og þau lönd og svæði sem þessi kostur er tiltækur fyrir.</span><span class="sxs-lookup"><span data-stu-id="3fcd0-123">The following lists show the transaction types, and the countries and regions, that this option is available for.</span></span>

<span data-ttu-id="3fcd0-124">**Færslugerðir**</span><span class="sxs-lookup"><span data-stu-id="3fcd0-124">**Transaction types**</span></span>

<span data-ttu-id="3fcd0-125">Hægt er að bæta öðrum texta við sjálfgefnar lýsingar fyrir færslugerðir sem tengjast eftirfarandi skjalgerðum:</span><span class="sxs-lookup"><span data-stu-id="3fcd0-125">You can add other text to default descriptions for transaction types that are related to the following document types:</span></span>

- <span data-ttu-id="3fcd0-126">Reikningar viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="3fcd0-126">Customer invoices</span></span>
- <span data-ttu-id="3fcd0-127">Kreditnótur viðskiptavina</span><span class="sxs-lookup"><span data-stu-id="3fcd0-127">Customer credit notes</span></span>
- <span data-ttu-id="3fcd0-128">Staðgreiðslur viðskiptavina</span><span class="sxs-lookup"><span data-stu-id="3fcd0-128">Customer cash payments</span></span>
- <span data-ttu-id="3fcd0-129">Greiðslur lánardrottna</span><span class="sxs-lookup"><span data-stu-id="3fcd0-129">Vendor payments</span></span>
- <span data-ttu-id="3fcd0-130">Sölupantanir</span><span class="sxs-lookup"><span data-stu-id="3fcd0-130">Sales orders</span></span>
- <span data-ttu-id="3fcd0-131">Innkaupapantanir</span><span class="sxs-lookup"><span data-stu-id="3fcd0-131">Purchase orders</span></span>
- <span data-ttu-id="3fcd0-132">Birgðabækur</span><span class="sxs-lookup"><span data-stu-id="3fcd0-132">Inventory journals</span></span>
- <span data-ttu-id="3fcd0-133">Áætlanagerð (MRP)</span><span class="sxs-lookup"><span data-stu-id="3fcd0-133">Master planning (MRP)</span></span>
- <span data-ttu-id="3fcd0-134">Eignir</span><span class="sxs-lookup"><span data-stu-id="3fcd0-134">Fixed assets</span></span>

<span data-ttu-id="3fcd0-135">**Lönd og landsvæði**</span><span class="sxs-lookup"><span data-stu-id="3fcd0-135">**Countries and regions**</span></span>

<span data-ttu-id="3fcd0-136">Þessi kostur er tiltækur fyrir eftirfarandi lönd og svæði:</span><span class="sxs-lookup"><span data-stu-id="3fcd0-136">This option is available for the following countries and regions:</span></span>

- <span data-ttu-id="3fcd0-137">Brasilía</span><span class="sxs-lookup"><span data-stu-id="3fcd0-137">Brazil</span></span>
- <span data-ttu-id="3fcd0-138">Kína</span><span class="sxs-lookup"><span data-stu-id="3fcd0-138">China</span></span>
- <span data-ttu-id="3fcd0-139">Tékkland</span><span class="sxs-lookup"><span data-stu-id="3fcd0-139">Czech Republic</span></span>
- <span data-ttu-id="3fcd0-140">Austur-Evrópa</span><span class="sxs-lookup"><span data-stu-id="3fcd0-140">Eastern Europe</span></span>
- <span data-ttu-id="3fcd0-141">Ungverjaland</span><span class="sxs-lookup"><span data-stu-id="3fcd0-141">Hungary</span></span>
- <span data-ttu-id="3fcd0-142">Indland</span><span class="sxs-lookup"><span data-stu-id="3fcd0-142">India</span></span>
- <span data-ttu-id="3fcd0-143">Japan</span><span class="sxs-lookup"><span data-stu-id="3fcd0-143">Japan</span></span>
- <span data-ttu-id="3fcd0-144">Litháen</span><span class="sxs-lookup"><span data-stu-id="3fcd0-144">Lithuania</span></span>
- <span data-ttu-id="3fcd0-145">Lettland</span><span class="sxs-lookup"><span data-stu-id="3fcd0-145">Latvia</span></span>
- <span data-ttu-id="3fcd0-146">Pólland</span><span class="sxs-lookup"><span data-stu-id="3fcd0-146">Poland</span></span>
- <span data-ttu-id="3fcd0-147">Rússland</span><span class="sxs-lookup"><span data-stu-id="3fcd0-147">Russia</span></span>

### <a name="add-text-to-default-descriptions"></a><span data-ttu-id="3fcd0-148">Bæta texta við sjálfgefnar lýsingar</span><span class="sxs-lookup"><span data-stu-id="3fcd0-148">Add text to default descriptions</span></span>

<span data-ttu-id="3fcd0-149">Eftir að þú hefur lokið við skrefin í kaflanum [Setja upp sjálfgefnar lýsingar](#set-up-default-descriptions) fyrr í þessu efnisatriði, skaltu fylgja þessum leiðbeiningum til að bæta öðrum texta við upphaflegar lýsingar.</span><span class="sxs-lookup"><span data-stu-id="3fcd0-149">After you complete the steps in the [Set up default descriptions](#set-up-default-descriptions) section earlier in this topic, follow these steps to add other text to the default descriptions.</span></span>

1. <span data-ttu-id="3fcd0-150">Á flýtiflipanum **Færibreytur** velurðu **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="3fcd0-150">On the **Parameters** FastTab, select **Add**.</span></span>
2. <span data-ttu-id="3fcd0-151">Í reitnum **Tilvísunartafla** skal velja tölfu gagnagrunns, þar sem bæta á færibreytugögnum við lýsinguna.</span><span class="sxs-lookup"><span data-stu-id="3fcd0-151">In the **Reference table** field, select the database table from which to add parameter data to the description.</span></span>
3. <span data-ttu-id="3fcd0-152">Í reitnum **Tilvísunarreitur** skal velja reitinn þar sem bæta á færibreytugögnum við lýsinguna.</span><span class="sxs-lookup"><span data-stu-id="3fcd0-152">In the **Reference field** field, select the field from which to add parameter data to the description.</span></span>
4. <span data-ttu-id="3fcd0-153">Endurtakið skref 1 til 3 til að bæta við fleiri færibreytum.</span><span class="sxs-lookup"><span data-stu-id="3fcd0-153">Repeat steps 1 through 3 to add more parameters.</span></span>