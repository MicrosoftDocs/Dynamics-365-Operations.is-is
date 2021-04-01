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
ms.openlocfilehash: f4c4fd5e8cdea9a7fc05ec9cbc7866c44c6f78b2
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5243968"
---
# <a name="confirm-outbound-shipments-from-batch-jobs"></a><span data-ttu-id="26502-103">Staðfesta sendingar á útleið úr runuvinnslum</span><span class="sxs-lookup"><span data-stu-id="26502-103">Confirm outbound shipments from batch jobs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="26502-104">Þetta efnisatriði lýsir því hvernig setja á upp runuvinnslu sem staðfestir sjálfkrafa sendingar flutningspantana á útleið fyrir farma sem eru tilbúnir fyrir afhendingu.</span><span class="sxs-lookup"><span data-stu-id="26502-104">This topic describes how to set up a batch job that automatically confirms outbound transfer-order shipments for ready-to-ship loads.</span></span> <span data-ttu-id="26502-105">Runuvinnslan sem lýst er hér gildir aðeins um sendingar flutningspantana, ekki sölupantanir.</span><span class="sxs-lookup"><span data-stu-id="26502-105">The batch job described here only applies to transfer order shipments, not to sales orders.</span></span>

## <a name="enable-the-confirm-outbound-shipments-from-batch-jobs-feature"></a><span data-ttu-id="26502-106">Virkja eiginleikann Staðfesta sendingar á útleið úr runuvinnslum</span><span class="sxs-lookup"><span data-stu-id="26502-106">Enable the Confirm outbound shipments from batch jobs feature</span></span>

<span data-ttu-id="26502-107">Áður en hægt er að nota þennan eiginleika þarf að virkja hann í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="26502-107">Before you can use this feature, it must be enabled on your system.</span></span> <span data-ttu-id="26502-108">Stjórnendur geta notað síðuna [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og virkjað hann ef þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="26502-108">Administrators can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) page to check the feature status and enable it if needed.</span></span> <span data-ttu-id="26502-109">Eiginleikinn er skráður sem:</span><span class="sxs-lookup"><span data-stu-id="26502-109">The feature is listed as:</span></span>

- <span data-ttu-id="26502-110">**Eining** - *Vöruhúsakerfi*</span><span class="sxs-lookup"><span data-stu-id="26502-110">**Module** - *Warehouse management*</span></span>
- <span data-ttu-id="26502-111">**Heiti eiginleika** - *Staðfesta sendingar á útleið úr runuvinnslum*</span><span class="sxs-lookup"><span data-stu-id="26502-111">**Feature name** - *Confirm outbound shipments from batch jobs*</span></span>

## <a name="process-outbound-shipments"></a><span data-ttu-id="26502-112">Vinna úr sendingum á útleið</span><span class="sxs-lookup"><span data-stu-id="26502-112">Process outbound shipments</span></span>

<span data-ttu-id="26502-113">Til að setja upp áætlaða runuvinnslu til að keyra staðfestingu á sendingu á útleið fyrir farma sem eru tilbúnir til afhendingar:</span><span class="sxs-lookup"><span data-stu-id="26502-113">To set up a scheduled batch job to run the outbound shipment confirmation for loads that are ready to ship:</span></span>

1. <span data-ttu-id="26502-114">Farið í **Vöruhúsakerfi \> Reglubundin verk \> Vinna úr sendingum á útleið**.</span><span class="sxs-lookup"><span data-stu-id="26502-114">Go to **Warehouse management \> Periodic tasks \> Process outbound shipments**.</span></span>
1. <span data-ttu-id="26502-115">Svarglugginn **Staðfesta sendingu** opnast.</span><span class="sxs-lookup"><span data-stu-id="26502-115">The **Confirm shipment** dialog box opens.</span></span> <span data-ttu-id="26502-116">Á flýtiflipanum **Færslur til að hafa með** velurðu **Sía**.</span><span class="sxs-lookup"><span data-stu-id="26502-116">On the **Records to include** FastTab, select **Filter**.</span></span>
1. <span data-ttu-id="26502-117">Svargluggi fyrirspurnarritils opnast.</span><span class="sxs-lookup"><span data-stu-id="26502-117">The query editor dialog box opens.</span></span> <span data-ttu-id="26502-118">Í flipanum **Svið** skal bæta við línu með eftirfarandi gildum:</span><span class="sxs-lookup"><span data-stu-id="26502-118">On the **Range** tab, add a row with the following values:</span></span>
    - <span data-ttu-id="26502-119">**Tafla** - *Farmar*</span><span class="sxs-lookup"><span data-stu-id="26502-119">**Table** - *Loads*</span></span>
    - <span data-ttu-id="26502-120">**Afleidd tafla** - *Farmar*</span><span class="sxs-lookup"><span data-stu-id="26502-120">**Derived table** - *Loads*</span></span>
    - <span data-ttu-id="26502-121">**Reitur** - *Farmstaða*</span><span class="sxs-lookup"><span data-stu-id="26502-121">**Field** - *Load status*</span></span>
    - <span data-ttu-id="26502-122">**Skilyrði** - *Hlaðinn*</span><span class="sxs-lookup"><span data-stu-id="26502-122">**Criteria** - *Loaded*</span></span>
1. <span data-ttu-id="26502-123">Veljið **Í lagi** til að fara aftur í svargluggann **Staðfesta sendingu**.</span><span class="sxs-lookup"><span data-stu-id="26502-123">Select **OK** to return to the **Confirm shipment** dialog box.</span></span>
1. <span data-ttu-id="26502-124">Í flýtiflipanum **Keyra í bakgrunni** skal stilla **Runuvinnsla** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="26502-124">On the **Run in the background** FastTab, set **Batch processing** to **Yes**.</span></span>
1. <span data-ttu-id="26502-125">Í flýtiflipanum **Keyra í bakgrunni** skal velja **Endurtekning**.</span><span class="sxs-lookup"><span data-stu-id="26502-125">On the **Run in the background** FastTab, select **Recurrence**.</span></span>
1. <span data-ttu-id="26502-126">Svarglugginn **Skilgreina endurtekningu** opnast.</span><span class="sxs-lookup"><span data-stu-id="26502-126">The **Define recurrence** dialog box opens.</span></span> <span data-ttu-id="26502-127">Stillið keyrslu áætlunar eftir þörfum fyrir fyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="26502-127">Set the run schedule as needed for your business.</span></span>
1. <span data-ttu-id="26502-128">Veljið **Í lagi** til að fara aftur í svargluggann **Staðfesta sendingu**.</span><span class="sxs-lookup"><span data-stu-id="26502-128">Select **OK** to return to the **Confirm shipment** dialog box.</span></span>
1. <span data-ttu-id="26502-129">Veljið **Í lagi** í svarglugganum **Staðfesta sendingu** til að bæta runuvinnslunni við runubiðröðina.</span><span class="sxs-lookup"><span data-stu-id="26502-129">Select **OK** on the **Confirm shipment** dialog box to add the batch job to the batch queue.</span></span>

<span data-ttu-id="26502-130">Nánari upplýsingar er að finna í [Yfirlit runuvinnslu](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md).</span><span class="sxs-lookup"><span data-stu-id="26502-130">For more information, see [Batch processing overview](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]