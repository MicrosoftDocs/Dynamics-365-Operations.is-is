---
title: Setja upp VSK-kóða
description: Vsk-kóða eru stofnaðar fyrir hvert óbeint skattur eða gjald sem lögaðili er skylt að reikna, innheimta og greiða til skattyfirvalda.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f29442c2ef2e3d0008a74298fda218e4cbd93f8e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "349171"
---
# <a name="set-up-sales-tax-codes"></a><span data-ttu-id="efc43-103">Setja upp VSK-kóða</span><span class="sxs-lookup"><span data-stu-id="efc43-103">Set up sales tax codes</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="efc43-104">Vsk-kóða eru stofnaðar fyrir hvert óbeint skattur eða gjald sem lögaðili er skylt að reikna, innheimta og greiða til skattyfirvalda.</span><span class="sxs-lookup"><span data-stu-id="efc43-104">Sales tax codes are created for every indirect tax or duty that the legal entity is obligated to calculate, collect, and pay to sales tax authorities.</span></span>

<span data-ttu-id="efc43-105">Þetta verkefni notar USMF-sýnifyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="efc43-105">This task uses the USMF demo company.</span></span>



1. <span data-ttu-id="efc43-106">Fara í Skattur > Óbeinir skattar > Virðisaukaskattur- > Vsk-kóðar.</span><span class="sxs-lookup"><span data-stu-id="efc43-106">Go to Tax > Indirect taxes > Sales tax > Sales tax codes.</span></span>
2. <span data-ttu-id="efc43-107">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="efc43-107">Click New.</span></span>
3. <span data-ttu-id="efc43-108">Færa inn gildi í svæðinu fyrir VSK-kóði.</span><span class="sxs-lookup"><span data-stu-id="efc43-108">In the Sales tax code field, type a value.</span></span>
4. <span data-ttu-id="efc43-109">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="efc43-109">In the Name field, type a value.</span></span>
5. <span data-ttu-id="efc43-110">Veljið jöfnunartímabil til að tilgreina hvaða skattyfirvöld og í hvaða tímabilum þessi vsk þarf að tilkynntur og greiddur.</span><span class="sxs-lookup"><span data-stu-id="efc43-110">Select a Settlement period to specify which Sales tax authority and in which intervals this sales tax needs to be reported and paid.</span></span>
6. <span data-ttu-id="efc43-111">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="efc43-111">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="efc43-112">Veljið fjárhagsbókunarflokk til að tilgreina skal aðallykla til að bóka vsk í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="efc43-112">Select a Ledger posting group to specify the main accounts to post sales tax to the general ledger.</span></span>
8. <span data-ttu-id="efc43-113">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="efc43-113">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="efc43-114">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="efc43-114">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="efc43-115">Stækka Útreikningur flýtiflipi.</span><span class="sxs-lookup"><span data-stu-id="efc43-115">Expand the Calculation FastTab.</span></span>
    * <span data-ttu-id="efc43-116">Útreikningur flýtiflipi hefur mörg svæði sem stjórna hvernig vsk-upphæðir verður reiknuð.</span><span class="sxs-lookup"><span data-stu-id="efc43-116">The Calculation FastTab has multiple fields that control how sales tax amounts will be calculated.</span></span>  
11. <span data-ttu-id="efc43-117">Á Aðgerðasvæðinu skal smellt á Vsk-kóða.</span><span class="sxs-lookup"><span data-stu-id="efc43-117">On the Action Pane, click Sales tax code.</span></span>
12. <span data-ttu-id="efc43-118">Smella á Gildi.</span><span class="sxs-lookup"><span data-stu-id="efc43-118">Click Values.</span></span>
13. <span data-ttu-id="efc43-119">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="efc43-119">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="efc43-120">Færið inn gildi fyrir þetta vsk-kóða.</span><span class="sxs-lookup"><span data-stu-id="efc43-120">Enter the value for this tax code.</span></span>
    * <span data-ttu-id="efc43-121">Á Flýtiflipanum Útreikninga, í svæðinu Uppruna ef Upphæð á einingu er valinn er gildið margfaldað með magninu í færsluna til að reikna út vsk-upphæð.</span><span class="sxs-lookup"><span data-stu-id="efc43-121">On the Calculation FastTab, in the Origin field, if Amount per unit is selected, the value will be multiplied by the quantity on the transaction to calculate the sales tax amount.</span></span>  <span data-ttu-id="efc43-122">Ef skattkóði er ekki skattur byggður á einingum er gildið sem er prósenta sem er notað í Uppruna fyrir þetta skattkóði til að reikna út upphæð virðisaukaskatts.</span><span class="sxs-lookup"><span data-stu-id="efc43-122">If the tax code is not a unit based tax, the value is a percentage that is applied on the Origin for this tax code to calculate the sales tax amount.</span></span>     
15. <span data-ttu-id="efc43-123">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="efc43-123">Click Save.</span></span>
16. <span data-ttu-id="efc43-124">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="efc43-124">Close the page.</span></span>
17. <span data-ttu-id="efc43-125">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="efc43-125">Click Save.</span></span>

