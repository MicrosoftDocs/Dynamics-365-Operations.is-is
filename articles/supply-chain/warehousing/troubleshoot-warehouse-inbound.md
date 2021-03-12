---
title: Úrræðaleit fyrir vöruhúsaaðgerðir á innleið
description: Í þessu efnisatriði er því lýst hvernig á að laga vandamál sem kunna að koma upp þegar unnið er með vöruhúsaaðgerðir á innleið i Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 71f590ec01b757de298bd2692fdbdb0324843376
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4970250"
---
# <a name="troubleshoot-inbound-warehouse-operations"></a><span data-ttu-id="be47b-103">Úrræðaleit fyrir vöruhúsaaðgerðir á innleið</span><span class="sxs-lookup"><span data-stu-id="be47b-103">Troubleshoot inbound warehouse operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="be47b-104">Í þessu efnisatriði er því lýst hvernig á að laga vandamál sem kunna að koma upp þegar unnið er með vöruhúsaaðgerðir á innleið i Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="be47b-104">This topic describes how to fix common issues that you might encounter while you work with inbound warehouse operations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-quality-order-1-has-been-generated-cluster-profile-could-not-be-found-please-check-your-configuration"></a><span data-ttu-id="be47b-105">Ég fæ eftirfarandi villuskilaboð: „Gæðapöntun %1 var búin til.</span><span class="sxs-lookup"><span data-stu-id="be47b-105">I receive the following error message: "Quality order %1 has been generated.</span></span> <span data-ttu-id="be47b-106">Klasaprófíll fannst ekki, athuga skal grunnstillinguna.</span><span class="sxs-lookup"><span data-stu-id="be47b-106">Cluster profile could not be found please check your configuration."</span></span>

### <a name="issue-description"></a><span data-ttu-id="be47b-107">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="be47b-107">Issue description</span></span>

<span data-ttu-id="be47b-108">Þessi villuboð tengjast móttökuferli þar sem kveikt er á gæðastjórnun (QMS).</span><span class="sxs-lookup"><span data-stu-id="be47b-108">This error message is related to a receiving process where quality management (QMS) is turned on.</span></span> <span data-ttu-id="be47b-109">Frekari upplýsingar um færsluna sem myndar villuboðin gætu hjálpað við að lagfæra vandamálið, allt eftir skilgreiningum í umhverfinu.</span><span class="sxs-lookup"><span data-stu-id="be47b-109">Depending on the configurations in your environment, additional details about the transaction that is generating the error message might help fix the issue.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="be47b-110">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="be47b-110">Issue resolution</span></span>

<span data-ttu-id="be47b-111">Fyrst skal yfirfara uppsetningu [Klasatiltekt](set-up-cluster-picking.md) og ganga úr skugga um að klasaforstillingar séu rétt uppsettar.</span><span class="sxs-lookup"><span data-stu-id="be47b-111">First, review the [cluster picking](set-up-cluster-picking.md) setup, and make sure that your cluster profiles are set up correctly.</span></span> <span data-ttu-id="be47b-112">Ekki er hægt að nota valmyndaratriði fartækis fyrir klasatiltekt nema klasaforstillingar séu settar upp.</span><span class="sxs-lookup"><span data-stu-id="be47b-112">You can't use a mobile device menu item for cluster picking unless cluster profiles are set up.</span></span> <span data-ttu-id="be47b-113">Einnig gæti verið nauðsynlegt að fara yfir aðrar tengdar skilgreiningar í samræmi við umhverfinu.</span><span class="sxs-lookup"><span data-stu-id="be47b-113">Depending on your environment, you might also have to review other related configurations.</span></span>

## <a name="mixed-license-plate-receiving-doesnt-work-for-any-disposition-code-except-credit"></a><span data-ttu-id="be47b-114">Móttaka blandaðrar númeraplötu virkar ekki fyrir neinn ráðstöfunarkóða fyrir utan Kredit.</span><span class="sxs-lookup"><span data-stu-id="be47b-114">Mixed license plate receiving doesn't work for any disposition code except Credit.</span></span>

### <a name="issue-description"></a><span data-ttu-id="be47b-115">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="be47b-115">Issue description</span></span>

<span data-ttu-id="be47b-116">Þegar svæðið **Aðgerð** fyrir ráðstöfunarkóða er stillt á *Kredit* eða *Úrkast* er aðeins hægt að nota valmyndina [Móttaka blandaðrar númeraplötu](mixed-license-plate-receiving.md) valmyndaratriði til að vinna úr skilavörum.</span><span class="sxs-lookup"><span data-stu-id="be47b-116">When the **Action** field for a disposition code is set to *Credit* or *Scrap*, you can use only the [Mixed license plate receiving](mixed-license-plate-receiving.md) menu item to process returned items.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="be47b-117">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="be47b-117">Issue resolution</span></span>

<span data-ttu-id="be47b-118">Microsoft hefur metið þetta mál og hefur ákvarðað að þetta sé takmörkun eiginleika.</span><span class="sxs-lookup"><span data-stu-id="be47b-118">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="be47b-119">Sem stendur eru aðeins [ráðstöfunarkóðar](../service-management/set-up-disposition-codes.md) þar sem reiturinn **Aðgerð** er stilltur á *Kredit* eða *Rýrnun* studdir fyrir móttöku blandaðrar númeraplötu.</span><span class="sxs-lookup"><span data-stu-id="be47b-119">Currently, only [disposition codes](../service-management/set-up-disposition-codes.md) where the **Action** field is set to *Credit* or *Scrap* are supported for mixed license plate receiving.</span></span>

## <a name="when-i-run-the-update-product-receipts-periodic-task-unconfirmed-purchase-orders-are-confirmed"></a><span data-ttu-id="be47b-120">Þegar reglubundna verkið Uppfæra innhreyfingarskjöl afurða er keyrt eru óstaðfestar innkaupapantanir staðfestar.</span><span class="sxs-lookup"><span data-stu-id="be47b-120">When I run the Update product receipts periodic task, unconfirmed purchase orders are confirmed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="be47b-121">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="be47b-121">Issue description</span></span>

<span data-ttu-id="be47b-122">Þegar búið er að keyra reglubundna verkið *Uppfæra innhreyfingarskjöl afurða* staðfestir kerfið sjálfkrafa óstaðfestar innkaupapantanir sem eru með birgðafærslustöðu *Skráð*.</span><span class="sxs-lookup"><span data-stu-id="be47b-122">After you run the *Update product receipts* periodic task, the system automatically confirms unconfirmed purchase orders that have an inventory transaction status of *Registered*.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="be47b-123">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="be47b-123">Issue resolution</span></span>

<span data-ttu-id="be47b-124">Nýr eiginleiki fyrir meðhöndlun á innleið, *Umframmóttaka á hleðslumagni*, lagar þetta vandamál.</span><span class="sxs-lookup"><span data-stu-id="be47b-124">A new inbound load handling feature, *Over receipt of load quantities*, fixes this issue.</span></span> <span data-ttu-id="be47b-125">Til að kveikja á þessum eiginleika skal fara í [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og kveikja á eftirfarandi eiginleikum (í þeirri röð sem þeir eru sýndir).</span><span class="sxs-lookup"><span data-stu-id="be47b-125">To turn on this feature, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the following features (in the order that they are listed in):</span></span>

1. <span data-ttu-id="be47b-126">Tengja birgðafærslur innkaupapöntunar við farm</span><span class="sxs-lookup"><span data-stu-id="be47b-126">Associate purchase order inventory transactions with load</span></span>
1. <span data-ttu-id="be47b-127">Umframmóttaka á hleðslumagni</span><span class="sxs-lookup"><span data-stu-id="be47b-127">Over receipt of load quantities</span></span>

<span data-ttu-id="be47b-128">Frekari upplýsingar er að finna á [Bóka skráð afurðamagn á móti innkaupapöntunum](inbound-load-handling.md#post-registered-quantities).</span><span class="sxs-lookup"><span data-stu-id="be47b-128">For more information, see [Post registered product quantities against purchase orders](inbound-load-handling.md#post-registered-quantities).</span></span>
