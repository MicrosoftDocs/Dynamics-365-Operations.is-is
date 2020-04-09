---
title: Setja upp VSK-kóða
description: Í þessu efnisatriði er útskýrt hvernig á að setja upp virðisaukaskatt í Dynamics 365 Finance.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 26dc61e340afcf1ce99d37c43d5942dc8792b765
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144744"
---
# <a name="set-up-sales-tax-codes"></a><span data-ttu-id="25524-103">Setja upp VSK-kóða</span><span class="sxs-lookup"><span data-stu-id="25524-103">Set up sales tax codes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="25524-104">Í þessu efnisatriði er útskýrt hvernig á að setja upp virðisaukaskatt.</span><span class="sxs-lookup"><span data-stu-id="25524-104">This topic explains how to set up sales tax codes.</span></span> <span data-ttu-id="25524-105">Vsk-kóða eru stofnaðar fyrir hvert óbeint skattur eða gjald sem lögaðili er skylt að reikna, innheimta og greiða til skattyfirvalda.</span><span class="sxs-lookup"><span data-stu-id="25524-105">Sales tax codes are created for every indirect tax or duty that the legal entity is obligated to calculate, collect, and pay to sales tax authorities.</span></span>

<span data-ttu-id="25524-106">Þetta verkefni notar USMF-sýnifyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="25524-106">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="25524-107">Farðu í **Skoðunarrúða > Skattur > Óbeinir skattar > Virðisaukaskattur- > Vsk-kóðar**.</span><span class="sxs-lookup"><span data-stu-id="25524-107">Go to **Navigation pane > Tax > Indirect taxes > Sales tax > Sales tax codes**.</span></span>
2. <span data-ttu-id="25524-108">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="25524-108">Select **New**.</span></span>
3. <span data-ttu-id="25524-109">Í reitnum **VSK-kóði** skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="25524-109">In the **Sales tax code** field, type a value.</span></span>
4. <span data-ttu-id="25524-110">Í reitinn **Heiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="25524-110">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="25524-111">Veljið **Jöfnunartímabil** með því að opna fellilistann til að tilgreina hvaða skattyfirvöld og í hvaða tímabilum þessi vsk þarf að tilkynntur og greiddur.</span><span class="sxs-lookup"><span data-stu-id="25524-111">Select a **Settlement period** by opening the pull-down list to specify which Sales tax authority and in which intervals this sales tax needs to be reported and paid.</span></span>
6. <span data-ttu-id="25524-112">Veljið **fjárhagsbókunarflokk** til að tilgreina skal aðallykla til að bóka vsk í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="25524-112">Select a **Ledger posting group** to specify the main accounts to post sales tax to the general ledger.</span></span>
7. <span data-ttu-id="25524-113">Stækka **Útreikningur** flýtiflipi.</span><span class="sxs-lookup"><span data-stu-id="25524-113">Expand the **Calculation** FastTab.</span></span> <span data-ttu-id="25524-114">Þetta inniheldur mörg svæði sem stjórna hvernig vsk-upphæðir verður reiknuð.</span><span class="sxs-lookup"><span data-stu-id="25524-114">This includes multiple fields that control how sales tax amounts will be calculated.</span></span> <span data-ttu-id="25524-115">Fylltu út þessa reiti eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="25524-115">Fill these fields out as needed.</span></span>  
8. <span data-ttu-id="25524-116">Á **Aðgerðarrúðan** efst í viðmótinu skaltu velja **VSK-kóði**.</span><span class="sxs-lookup"><span data-stu-id="25524-116">On the **Action Pane** at the top of the interface, select **Sales tax code**.</span></span>
9. <span data-ttu-id="25524-117">Veldu **Gildi**.</span><span class="sxs-lookup"><span data-stu-id="25524-117">Select **Values**.</span></span>
10. <span data-ttu-id="25524-118">Sláðu inn gildi fyrir þennan skattakóða í **gildi** dálki.</span><span class="sxs-lookup"><span data-stu-id="25524-118">Enter the value for this tax code in the **value** column.</span></span>
    - <span data-ttu-id="25524-119">Á Flýtiflipanum **Útreikninga**, í svæðinu Uppruna ef Upphæð á einingu er valinn er gildið margfaldað með magninu í færsluna til að reikna út vsk-upphæð.</span><span class="sxs-lookup"><span data-stu-id="25524-119">On the **Calculation** FastTab, in the Origin field, if Amount per unit is selected, the value will be multiplied by the quantity on the transaction to calculate the sales tax amount.</span></span>  <span data-ttu-id="25524-120">Ef skattkóði er ekki skattur byggður á einingum er gildið sem er prósenta sem er notað í Uppruna fyrir þetta skattkóði til að reikna út upphæð virðisaukaskatts.</span><span class="sxs-lookup"><span data-stu-id="25524-120">If the tax code is not a unit based tax, the value is a percentage that is applied on the Origin for this tax code to calculate the sales tax amount.</span></span>     
11. <span data-ttu-id="25524-121">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="25524-121">Select **Save**.</span></span>
12. <span data-ttu-id="25524-122">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="25524-122">Close the page.</span></span>
13. <span data-ttu-id="25524-123">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="25524-123">Select **Save**.</span></span>

