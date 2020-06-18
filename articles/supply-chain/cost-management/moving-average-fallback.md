---
title: Varakostnaðarröð hlaupandi meðaltals
description: Þetta efni veitir upplýsingar um varakostnaðarraðir fyrir útreikninga á meðaltal í Microsoft Dynamics 365 Supply Chain Management.
author: AndersGirke
manager: AnnBe
ms.date: 03/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-03-25
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: b2172dfbec0a7f0fa25a081e4d92635a09f00e46
ms.sourcegitcommit: 3a823444005d316bd95fc663e2dbc8252ac7d93a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261341"
---
# <a name="moving-average-fallback-cost-sequence"></a><span data-ttu-id="2006b-103">Varakostnaðarröð hlaupandi meðaltals</span><span class="sxs-lookup"><span data-stu-id="2006b-103">Moving average fallback cost sequence</span></span>

<span data-ttu-id="2006b-104">Ein leið til að reikna út kostnað við birgðir er með því að nota _hlaupandi meðaltal_.</span><span class="sxs-lookup"><span data-stu-id="2006b-104">One way that you can calculate the cost of your inventory is by using a _moving average_.</span></span> <span data-ttu-id="2006b-105">Hægt er að tengja allt að þrjú kostnaðargildi við hverja birgðavöru:</span><span class="sxs-lookup"><span data-stu-id="2006b-105">Up to three cost values can be associated with each inventory item:</span></span>

- <span data-ttu-id="2006b-106">**Síðasta úthreyfing** - Síðasti úthreyfingarkostnaður sem var úthlutað áður en birgðir urðu neikvæðar</span><span class="sxs-lookup"><span data-stu-id="2006b-106">**Last issue** – The last issue cost that was assigned before inventory went negative</span></span>
- <span data-ttu-id="2006b-107">**Virkur kostnaður** - Síðasti kostnaður sem var virkjaður í kostnaðarútgáfu</span><span class="sxs-lookup"><span data-stu-id="2006b-107">**Active cost** – The latest cost that was activated in a costing version</span></span>
- <span data-ttu-id="2006b-108">**Vöruverð** - Kostnaðurinn sem er tilgreindur fyrir útgefna afurð</span><span class="sxs-lookup"><span data-stu-id="2006b-108">**Item price** – The cost that is specified for the released product</span></span>

<span data-ttu-id="2006b-109">Til að ákvarða hvert þessara kostnaðargilda skuli notað í útreikningum á meðaltali notar kerfið _varakostnaðarröð_ til að ákvarða forgangsröðun gildanna.</span><span class="sxs-lookup"><span data-stu-id="2006b-109">To determine which of these cost values should be used in moving average calculations, the system uses a _fallback cost sequence_ to establish the order of preference for the values.</span></span> <span data-ttu-id="2006b-110">Ef æskilegt kostnaðargildi ekki tiltækt notar kerfið næsta valið gildi og svo framvegis.</span><span class="sxs-lookup"><span data-stu-id="2006b-110">If the preferred cost value isn't available, the system uses the next-preferred value, and so on.</span></span>

<span data-ttu-id="2006b-111">Í fyrri útgáfum af Microsoft Dynamics 365 Supply Chain Management notaði kerfið fasta varakostnaðarröð (_Síðasta úthreyfing - Virkur kostnaður - Vöruverð_).</span><span class="sxs-lookup"><span data-stu-id="2006b-111">In previous versions of Microsoft Dynamics 365 Supply Chain Management, the system used a fixed fallback cost sequence (_Last issue – Active cost – Item price_).</span></span> <span data-ttu-id="2006b-112">Í útgáfu 10.0.11 er þessi röð enn sjálfgefna röðin.</span><span class="sxs-lookup"><span data-stu-id="2006b-112">In version 10.0.11, this sequence is still the default sequence.</span></span> <span data-ttu-id="2006b-113">Hins vegar getur þú einnig kveikt á eiginleikum sem gerir þér kleift að velja á milli þriggja tiltækra varakostnaðarraða.</span><span class="sxs-lookup"><span data-stu-id="2006b-113">However, you can also turn on a feature that lets you select among three available fallback cost sequences.</span></span> <span data-ttu-id="2006b-114">Þessi eiginleiki getur verið sérstaklega gagnlegur fyrir fyrirtæki sem nota reglulega neikvæð birgðagildi.</span><span class="sxs-lookup"><span data-stu-id="2006b-114">This feature can be especially useful for organizations that regularly use negative inventory values.</span></span>

<span data-ttu-id="2006b-115">Til að gera val á varakostnaðarröð tiltæka verður þú (eða stjórnandi) að nota [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að kveikja á eiginleikanum sem er nefndur _Varakostnaðarröð hlaupandi meðaltals_.</span><span class="sxs-lookup"><span data-stu-id="2006b-115">To make the selector for the fallback cost sequence available, you (or an admin) must use [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the feature that is named _Moving average fallback cost sequence_.</span></span>

<span data-ttu-id="2006b-116">Fylgdu þessum skrefum til að velja varakostnaðarröð fyrir útreikninga á meðaltali.</span><span class="sxs-lookup"><span data-stu-id="2006b-116">To select the fallback cost sequence for moving average calculations, follow these steps.</span></span>

1. <span data-ttu-id="2006b-117">Opnaðu síðuna **Færibreytur**.</span><span class="sxs-lookup"><span data-stu-id="2006b-117">Open the **Parameters** page.</span></span>
2. <span data-ttu-id="2006b-118">Á flipanum **Birgðabókhald**, í hlutanum **Hlaupandi meðaltal**, stillirðu reitinn **Varakostnaðarröð** á eitt af eftirfarandi gildum:</span><span class="sxs-lookup"><span data-stu-id="2006b-118">On the **Inventory accounting** tab, in the **Moving average** section, set the **Fallback cost sequence** field to one of the following values:</span></span>

    - <span data-ttu-id="2006b-119">**Síðasta úthreyfing - Virkur kostnaður - Verð vöru** - Þessi röð er sjálfgefin röð.</span><span class="sxs-lookup"><span data-stu-id="2006b-119">**Last issue – Active cost – Item price** – This sequence is the default sequence.</span></span> <span data-ttu-id="2006b-120">Það er sama röð og er notuð ef ekki er kveikt á eiginleikanum _Varakostnaðarröð hlaupandi meðaltals_.</span><span class="sxs-lookup"><span data-stu-id="2006b-120">It's the same sequence that is used if the _Moving average fallback cost sequence_ feature isn't turned on.</span></span>
    - <span data-ttu-id="2006b-121">**Virkur kostnaður – síðasti kostnaður**</span><span class="sxs-lookup"><span data-stu-id="2006b-121">**Active cost – Last issue**</span></span>
    - <span data-ttu-id="2006b-122">**Virkur kostnaður - Vöruverð** - Fyrirtæki gætu lent í afkomuvandamálum ef þau nota viðskiptaferla þar sem birgðir verða reglulega neikvæðar og færsluumfangið er um leið mikið.</span><span class="sxs-lookup"><span data-stu-id="2006b-122">**Active cost – Item price** – Organizations might experience performance issues if they use business processes where inventory regularly goes negative and, at the same time, the transaction volume is high.</span></span> <span data-ttu-id="2006b-123">Þessi stilling getur hjálpað til við að draga úr þessum afkastavandamálum.</span><span class="sxs-lookup"><span data-stu-id="2006b-123">This setting can help mitigate those performance issues.</span></span>

<span data-ttu-id="2006b-124">![Færibreytur birgðabókhalds](media/inventory-accounting-parameters.png "Færibreytur birgðabókhalds")</span><span class="sxs-lookup"><span data-stu-id="2006b-124">![Inventory accounting parameters](media/inventory-accounting-parameters.png "Inventory accounting parameters")</span></span>