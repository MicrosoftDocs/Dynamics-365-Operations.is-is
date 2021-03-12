---
title: Staðfesta sendingar á útleið úr runuvinnslum
description: Þetta efnisatriði lýsir því hvernig setja á upp runuvinnslu sem staðfestir sjálfkrafa sendingar flutningspantana á útleið fyrir farma sem eru tilbúnir fyrir afhendingu.
author: perlynne
manager: tfehr
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 48257967ce360b1d4969124411d5976b807bf9e4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996302"
---
# <a name="confirm-outbound-shipments-from-batch-jobs"></a><span data-ttu-id="6713e-103">Staðfesta sendingar á útleið úr runuvinnslum</span><span class="sxs-lookup"><span data-stu-id="6713e-103">Confirm outbound shipments from batch jobs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6713e-104">Þetta efnisatriði lýsir því hvernig setja á upp runuvinnslu sem staðfestir sjálfkrafa sendingar flutningspantana á útleið fyrir farma sem eru tilbúnir fyrir afhendingu.</span><span class="sxs-lookup"><span data-stu-id="6713e-104">This topic describes how to set up a batch job that automatically confirms outbound transfer-order shipments for ready-to-ship loads.</span></span> <span data-ttu-id="6713e-105">Runuvinnslan sem lýst er hér gildir aðeins um sendingar flutningspantana, ekki sölupantanir.</span><span class="sxs-lookup"><span data-stu-id="6713e-105">The batch job described here only applies to transfer order shipments, not to sales orders.</span></span>

## <a name="enable-the-confirm-outbound-shipments-from-batch-jobs-feature"></a><span data-ttu-id="6713e-106">Virkja eiginleikann Staðfesta sendingar á útleið úr runuvinnslum</span><span class="sxs-lookup"><span data-stu-id="6713e-106">Enable the Confirm outbound shipments from batch jobs feature</span></span>

<span data-ttu-id="6713e-107">Áður en hægt er að nota þennan eiginleika þarf að virkja hann í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="6713e-107">Before you can use this feature, it must be enabled on your system.</span></span> <span data-ttu-id="6713e-108">Stjórnendur geta notað síðuna [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og virkjað hann ef þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="6713e-108">Administrators can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) page to check the feature status and enable it if needed.</span></span> <span data-ttu-id="6713e-109">Eiginleikinn er skráður sem:</span><span class="sxs-lookup"><span data-stu-id="6713e-109">The feature is listed as:</span></span>

- <span data-ttu-id="6713e-110">**Eining** - *Vöruhúsakerfi*</span><span class="sxs-lookup"><span data-stu-id="6713e-110">**Module** - *Warehouse management*</span></span>
- <span data-ttu-id="6713e-111">**Heiti eiginleika** - *Staðfesta sendingar á útleið úr runuvinnslum*</span><span class="sxs-lookup"><span data-stu-id="6713e-111">**Feature name** - *Confirm outbound shipments from batch jobs*</span></span>

## <a name="process-outbound-shipments"></a><span data-ttu-id="6713e-112">Vinna úr sendingum á útleið</span><span class="sxs-lookup"><span data-stu-id="6713e-112">Process outbound shipments</span></span>

<span data-ttu-id="6713e-113">Til að setja upp áætlaða runuvinnslu til að keyra staðfestingu á sendingu á útleið fyrir farma sem eru tilbúnir til afhendingar:</span><span class="sxs-lookup"><span data-stu-id="6713e-113">To set up a scheduled batch job to run the outbound shipment confirmation for loads that are ready to ship:</span></span>

1. <span data-ttu-id="6713e-114">Farið í **Vöruhúsakerfi \> Reglubundin verk \> Vinna úr sendingum á útleið**.</span><span class="sxs-lookup"><span data-stu-id="6713e-114">Go to **Warehouse management \> Periodic tasks \> Process outbound shipments**.</span></span>
1. <span data-ttu-id="6713e-115">Svarglugginn **Staðfesta sendingu** opnast.</span><span class="sxs-lookup"><span data-stu-id="6713e-115">The **Confirm shipment** dialog box opens.</span></span> <span data-ttu-id="6713e-116">Á flýtiflipanum **Færslur til að hafa með** velurðu **Sía**.</span><span class="sxs-lookup"><span data-stu-id="6713e-116">On the **Records to include** FastTab, select **Filter**.</span></span>
1. <span data-ttu-id="6713e-117">Svargluggi fyrirspurnarritils opnast.</span><span class="sxs-lookup"><span data-stu-id="6713e-117">The query editor dialog box opens.</span></span> <span data-ttu-id="6713e-118">Í flipanum **Svið** skal bæta við línu með eftirfarandi gildum:</span><span class="sxs-lookup"><span data-stu-id="6713e-118">On the **Range** tab, add a row with the following values:</span></span>
    - <span data-ttu-id="6713e-119">**Tafla** - *Farmar*</span><span class="sxs-lookup"><span data-stu-id="6713e-119">**Table** - *Loads*</span></span>
    - <span data-ttu-id="6713e-120">**Afleidd tafla** - *Farmar*</span><span class="sxs-lookup"><span data-stu-id="6713e-120">**Derived table** - *Loads*</span></span>
    - <span data-ttu-id="6713e-121">**Reitur** - *Farmstaða*</span><span class="sxs-lookup"><span data-stu-id="6713e-121">**Field** - *Load status*</span></span>
    - <span data-ttu-id="6713e-122">**Skilyrði** - *Hlaðinn*</span><span class="sxs-lookup"><span data-stu-id="6713e-122">**Criteria** - *Loaded*</span></span>
1. <span data-ttu-id="6713e-123">Veljið **Í lagi** til að fara aftur í svargluggann **Staðfesta sendingu**.</span><span class="sxs-lookup"><span data-stu-id="6713e-123">Select **OK** to return to the **Confirm shipment** dialog box.</span></span>
1. <span data-ttu-id="6713e-124">Í flýtiflipanum **Keyra í bakgrunni** skal stilla **Runuvinnsla** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="6713e-124">On the **Run in the background** FastTab, set **Batch processing** to **Yes**.</span></span>
1. <span data-ttu-id="6713e-125">Í flýtiflipanum **Keyra í bakgrunni** skal velja **Endurtekning**.</span><span class="sxs-lookup"><span data-stu-id="6713e-125">On the **Run in the background** FastTab, select **Recurrence**.</span></span>
1. <span data-ttu-id="6713e-126">Svarglugginn **Skilgreina endurtekningu** opnast.</span><span class="sxs-lookup"><span data-stu-id="6713e-126">The **Define recurrence** dialog box opens.</span></span> <span data-ttu-id="6713e-127">Stillið keyrslu áætlunar eftir þörfum fyrir fyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="6713e-127">Set the run schedule as needed for your business.</span></span>
1. <span data-ttu-id="6713e-128">Veljið **Í lagi** til að fara aftur í svargluggann **Staðfesta sendingu**.</span><span class="sxs-lookup"><span data-stu-id="6713e-128">Select **OK** to return to the **Confirm shipment** dialog box.</span></span>
1. <span data-ttu-id="6713e-129">Veljið **Í lagi** í svarglugganum **Staðfesta sendingu** til að bæta runuvinnslunni við runubiðröðina.</span><span class="sxs-lookup"><span data-stu-id="6713e-129">Select **OK** on the **Confirm shipment** dialog box to add the batch job to the batch queue.</span></span>

<span data-ttu-id="6713e-130">Nánari upplýsingar er að finna í [Yfirlit runuvinnslu](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md).</span><span class="sxs-lookup"><span data-stu-id="6713e-130">For more information, see [Batch processing overview](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md).</span></span>
