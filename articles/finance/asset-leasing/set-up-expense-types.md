---
title: Setja upp kostnaðargerðir
description: Í þessu efnisatriði er útskýrt hvernig á að setja upp kostnaðargerðir í Eignarleigu.
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
ms.search.validFrom: 2019-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: d27c5653d6305aad23142fa6f803134153661278
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/28/2020
ms.locfileid: "4444576"
---
# <a name="set-up-expense-types"></a><span data-ttu-id="29556-103">Setja upp kostnaðargerðir</span><span class="sxs-lookup"><span data-stu-id="29556-103">Set up expense types</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="29556-104">Í þessu efnisatriði er útskýrt hvernig á að setja upp kostnaðargerðir í Eignarleigu.</span><span class="sxs-lookup"><span data-stu-id="29556-104">This topic explains how to set up expense types in Asset leasing.</span></span> <span data-ttu-id="29556-105">Kostnaður sem er ekki sýndur í greiðsluáætlun er þekktur sem *útgjaldakostnaður*.</span><span class="sxs-lookup"><span data-stu-id="29556-105">Costs that aren't represented by the payment schedule are known as *expense costs*.</span></span> <span data-ttu-id="29556-106">Dæmi um slíkan kostnað eru m.a. fasteignaskattar, viðhaldskostnaður sameiginlegs svæðis og tryggingagjöld.</span><span class="sxs-lookup"><span data-stu-id="29556-106">Examples of these costs include property taxes, common area maintenance costs, and insurance expenses.</span></span>

## <a name="add-an-administrative-expense-type"></a><span data-ttu-id="29556-107">Nota gerð stjórnunarkostnaðar</span><span class="sxs-lookup"><span data-stu-id="29556-107">Add an administrative expense type</span></span>

1. <span data-ttu-id="29556-108">Opnið **Eignarleiga \> Uppsetning \> Kostnaðargerðir**.</span><span class="sxs-lookup"><span data-stu-id="29556-108">Go to **Asset leasing \> Setup \> Expense types**.</span></span>
2. <span data-ttu-id="29556-109">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="29556-109">Select **New**.</span></span>
3. <span data-ttu-id="29556-110">Í viðeigandi svæði skal færa inn nýja kostnaðargerð og lýsingu.</span><span class="sxs-lookup"><span data-stu-id="29556-110">In the appropriate fields, enter the new expense type and a description.</span></span>

## <a name="assign-accounts-to-administrative-costs"></a><span data-ttu-id="29556-111">Úthluta lyklum á stjórnunarkostnað</span><span class="sxs-lookup"><span data-stu-id="29556-111">Assign accounts to administrative costs</span></span>

<span data-ttu-id="29556-112">Næst ætti að tengja lykla við kostnaðargerðirnar.</span><span class="sxs-lookup"><span data-stu-id="29556-112">Next, you should associate accounts with the expense types.</span></span> <span data-ttu-id="29556-113">Þessir lyklar verða debetfærðir þegar kostnaðaráætlunarfærslur eru bókaðar.</span><span class="sxs-lookup"><span data-stu-id="29556-113">These accounts will be debited when expense schedule entries are posted.</span></span> <span data-ttu-id="29556-114">Mótlykill er tilgreindur á **Greiðsluáætlunarlínum rekstrarkostnaðar** fyrir hvern leigusamning fyrir sig.</span><span class="sxs-lookup"><span data-stu-id="29556-114">The offset account is specified on the **Executory costs payment schedule** lines on each lease.</span></span>

1. <span data-ttu-id="29556-115">Opnið **Eignarleiga \> Uppsetning \> Færibreytur fyrir eignarleigu**.</span><span class="sxs-lookup"><span data-stu-id="29556-115">Go to **Asset leasing \> Setup \> Asset leasing parameters**.</span></span>
2. <span data-ttu-id="29556-116">Á flipanum **Lyklar** á flýtiflipanum **Rekstrarkostnaður** í svæðinu **Kostnaðargerð** er kostnaðargerðin valin.</span><span class="sxs-lookup"><span data-stu-id="29556-116">On the **Accounts** tab, on the **Executory costs** FastTab, in the **Expense type** field, select the expense type.</span></span>
3. <span data-ttu-id="29556-117">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="29556-117">Select **Add**.</span></span>
4. <span data-ttu-id="29556-118">Í reitnum **Bókargerð** skal velja gerð bókarinnar sem á að tengja við stjórnunarkostnaðinn.</span><span class="sxs-lookup"><span data-stu-id="29556-118">In the **Book type** field, select the book type to link to the administrative costs.</span></span>

    > [!NOTE]
    > <span data-ttu-id="29556-119">Hægt er að tengja margar bókargerðir við sama kostnaðarlykil.</span><span class="sxs-lookup"><span data-stu-id="29556-119">Multiple book types can be linked to the same expense account.</span></span>

5. <span data-ttu-id="29556-120">Í svæðinu **Lykilkóði** skal tilgreina leigusamningana sem nota skal bókina fyrir:</span><span class="sxs-lookup"><span data-stu-id="29556-120">In the **Account code** field, specify which leases the book should be applied to:</span></span>

    - <span data-ttu-id="29556-121">**Allt** – Nota bók fyrir allar leigur.</span><span class="sxs-lookup"><span data-stu-id="29556-121">**All** – Apply the book to all leases.</span></span>
    - <span data-ttu-id="29556-122">**Flokkur** -Notið bókina á tiltekinn flokk leigusamninga.</span><span class="sxs-lookup"><span data-stu-id="29556-122">**Group** – Apply the book to a specific group of leases.</span></span>
    - <span data-ttu-id="29556-123">**Tafla** – Nota bókina fyrir tiltekna leigusamninga.</span><span class="sxs-lookup"><span data-stu-id="29556-123">**Table** – Apply the book to specific leases.</span></span>

6. <span data-ttu-id="29556-124">Ef þú valdir **Flokk** eða **Tafla** í svæðinu **Lykilkóði** skaltu velja lykilnúmer eða flokksnúmer á svæðinu **Lykil-/flokksnúmer**.</span><span class="sxs-lookup"><span data-stu-id="29556-124">If you selected **Group** or **Table** in the **Account code** field, select an account number or group number in the **Account/Group number** field.</span></span>
7. <span data-ttu-id="29556-125">Í viðeigandi svæðum skal velja aðallykill fjármögnunarleigusamnings og aðallykil rekstrarleigusamnings.</span><span class="sxs-lookup"><span data-stu-id="29556-125">In the appropriate fields, select the finance lease main account and the operating lease main account.</span></span>

<span data-ttu-id="29556-126">Þegar þessum skrefum er lokið er hægt að bæta kostnaði við **Greiðsluáætlunarlínur rekstrarkostnaðar** á síðunni **Upplýsingar um leigusamning** fyrir valinn leigusamning.</span><span class="sxs-lookup"><span data-stu-id="29556-126">When you've completed these steps, you can add expenses through the **Executory costs payment schedule** lines on the **Lease details** page of a selected lease.</span></span> <span data-ttu-id="29556-127">Að öðrum kosti er hægt að bæta við kostnaði þegar ný leiga er stofnuð.</span><span class="sxs-lookup"><span data-stu-id="29556-127">Alternatively, you can add expenses when you create a new lease.</span></span>
