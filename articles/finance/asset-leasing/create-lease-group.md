---
title: Stofna leiguhóp
description: Í þessu efnisatriði er útskýrt hvernig á að setja upp leigusamningsflokka. Leigusamningsflokkar eru nauðsynlegir til að búa til nýja leigusamninga.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: f8512a59d0e9935090f97a0f0237bfefc8473955
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/28/2020
ms.locfileid: "4444580"
---
# <a name="create-a-lease-group"></a><span data-ttu-id="ddf57-104">Stofna leiguhóp</span><span class="sxs-lookup"><span data-stu-id="ddf57-104">Create a lease group</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ddf57-105">Í þessu efnisatriði er útskýrt hvernig á að setja upp leigusamningsflokka.</span><span class="sxs-lookup"><span data-stu-id="ddf57-105">This topic explains how to set up lease groups.</span></span> <span data-ttu-id="ddf57-106">Leigusamningsflokkar eru nauðsynlegir til að búa til nýja leigusamninga.</span><span class="sxs-lookup"><span data-stu-id="ddf57-106">Lease groups are required to create new leases.</span></span> <span data-ttu-id="ddf57-107">Leigubækur eru tengdar við hvern leigusamningsflokk.</span><span class="sxs-lookup"><span data-stu-id="ddf57-107">Lease books are associated with each lease group.</span></span> <span data-ttu-id="ddf57-108">Leigubækur ákvarða sjálfgefnu bækurnar sem þarf að stofna fyrir hverja leigu.</span><span class="sxs-lookup"><span data-stu-id="ddf57-108">Lease books determine the default books that must be created for each lease.</span></span> <span data-ttu-id="ddf57-109">Hægt er að úthluta tilteknum lyklum á leiguflokk á síðunni **Færibreytur leigubókunar**.</span><span class="sxs-lookup"><span data-stu-id="ddf57-109">You can assign specific accounts to a lease group on the **Lease posting parameters** page.</span></span>

## <a name="create-a-lease-book-and-add-a-lease-group"></a><span data-ttu-id="ddf57-110">Stofna leigubók og bæta við leigusamningsflokki</span><span class="sxs-lookup"><span data-stu-id="ddf57-110">Create a lease book and add a lease group</span></span>

1. <span data-ttu-id="ddf57-111">Opnið **Eignarleiga \> Uppsetning \> Leigusamningsflokkar**.</span><span class="sxs-lookup"><span data-stu-id="ddf57-111">Go to **Asset leasing \> Setup \> Lease groups**.</span></span>
2. <span data-ttu-id="ddf57-112">Á aðgerðasvæðinu skal velja **Ný** til að bæta við leigusamningsflokki.</span><span class="sxs-lookup"><span data-stu-id="ddf57-112">On the Action Pane, select **New** to add a lease group.</span></span> <span data-ttu-id="ddf57-113">Línu er bætt við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="ddf57-113">A line is added to the grid.</span></span>
3. <span data-ttu-id="ddf57-114">Í nýju línunni, í reitnum **Leigusamningsflokkur** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="ddf57-114">On the new line, in the **Lease group** field, enter a value.</span></span>
4. <span data-ttu-id="ddf57-115">Sláið inn gildi í reitnum **Lýsing**.</span><span class="sxs-lookup"><span data-stu-id="ddf57-115">In the **Description** field, enter a value.</span></span>

<span data-ttu-id="ddf57-116">Upplýsingunum sem voru slegnar inn er bætt við svæðið **Leigusamningsflokkur** á síðunni **Bæta við leigusamningi**.</span><span class="sxs-lookup"><span data-stu-id="ddf57-116">The information that you just entered is added to the **Lease group** field on the **Add lease** page.</span></span>

## <a name="associate-a-book-with-a-lease-group"></a><span data-ttu-id="ddf57-117">Tengja bók við leigusamningsflokk</span><span class="sxs-lookup"><span data-stu-id="ddf57-117">Associate a book with a lease group</span></span>

<span data-ttu-id="ddf57-118">Þegar búið er að stofna leigusamningsflokka er hægt að úthluta bókum í hvern hóp.</span><span class="sxs-lookup"><span data-stu-id="ddf57-118">After you create lease groups, you can assign books to each group.</span></span> <span data-ttu-id="ddf57-119">Þegar búið er að stofna leigusamning og úthluta honum á leiguflokk stofnar kerfið áætlun fyrir hverja bók sem tengist þessum leigusamningsflokki.</span><span class="sxs-lookup"><span data-stu-id="ddf57-119">When you create a lease and assign it to a lease group, the system creates a set of schedules for each book that is associated with that lease group.</span></span>

> [!NOTE]
> <span data-ttu-id="ddf57-120">Setja verður upp bækur áður en hægt er að úthluta þeim á leigusamningsflokk.</span><span class="sxs-lookup"><span data-stu-id="ddf57-120">Books must be set up before they can be assigned to a lease group.</span></span>

1. <span data-ttu-id="ddf57-121">Opnið **Eignarleiga \> Uppsetning \> Leigusamningsflokkur**.</span><span class="sxs-lookup"><span data-stu-id="ddf57-121">Go to **Asset leasing \> Setup \> Lease group**.</span></span>
2. <span data-ttu-id="ddf57-122">Veljið leigusamningsflokk og svo **Bækur**.</span><span class="sxs-lookup"><span data-stu-id="ddf57-122">Select a lease group, and then select **Books**.</span></span>
3. <span data-ttu-id="ddf57-123">Veljið **Nýtt** og síðan, á svæðinu **Bókargerð**, bókina sem á að úthluta á leigusamningsflokkinn.</span><span class="sxs-lookup"><span data-stu-id="ddf57-123">Select **New**, and then, in the **Book type** field, select the book to assign to the lease group.</span></span> <span data-ttu-id="ddf57-124">Hægt er að úthluta mörgum bókum á leigusamningsflokk ef taka þarf tillit til leigusamnings á mismunandi hátt.</span><span class="sxs-lookup"><span data-stu-id="ddf57-124">You can assign multiple books to a lease group if a lease must be accounted for in different ways.</span></span>