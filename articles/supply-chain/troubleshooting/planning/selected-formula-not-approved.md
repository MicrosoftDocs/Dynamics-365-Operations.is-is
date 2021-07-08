---
title: Valið formúlunúmer er ekki samþykkt fyrir runupöntun
description: Þegar reynt er að festa áætlaða pöntun berast villuboð sem segja að valið formúlunúmer sé ekki samþykkt fyrir runupöntun.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 4f993c92ca0a2f8f79e4b0e0eda43904529163f8
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294097"
---
# <a name="selected-formula-number-isnt-approved-for-a-batch-order"></a><span data-ttu-id="7287a-103">Valið formúlunúmer er ekki samþykkt fyrir runupöntun</span><span class="sxs-lookup"><span data-stu-id="7287a-103">Selected formula number isn't approved for a batch order</span></span>

<span data-ttu-id="7287a-104">Villukóði PRO2614</span><span class="sxs-lookup"><span data-stu-id="7287a-104">Error code: PRO2614</span></span>

## <a name="symptoms"></a><span data-ttu-id="7287a-105">Einkenni</span><span class="sxs-lookup"><span data-stu-id="7287a-105">Symptoms</span></span>

<span data-ttu-id="7287a-106">Þegar reynt er að fastsetja áætlaða pöntun berast eftirfarandi villuboð:</span><span class="sxs-lookup"><span data-stu-id="7287a-106">When you try to firm a planned order, you receive the following error message:</span></span>

> <span data-ttu-id="7287a-107">Valið formúlunúmer er ekki samþykkt fyrir runupöntun.</span><span class="sxs-lookup"><span data-stu-id="7287a-107">The selected formula number is not approved for a batch order.</span></span>

## <a name="cause"></a><span data-ttu-id="7287a-108">Orsök</span><span class="sxs-lookup"><span data-stu-id="7287a-108">Cause</span></span>

<span data-ttu-id="7287a-109">Kerfið staðfestir festingaraðgerðina til að ganga úr skugga um samþykkt formúla sé tiltæki fyrir virka vöru.</span><span class="sxs-lookup"><span data-stu-id="7287a-109">The system validates the firming operation to make sure that an approved formula is available for the active item.</span></span> <span data-ttu-id="7287a-110">Þú verður líklega að samþykkja formúluna.</span><span class="sxs-lookup"><span data-stu-id="7287a-110">You must probably approve the formula.</span></span>

## <a name="resolution"></a><span data-ttu-id="7287a-111">Lausn</span><span class="sxs-lookup"><span data-stu-id="7287a-111">Resolution</span></span>

<span data-ttu-id="7287a-112">Til að samþykkja formúlu skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="7287a-112">To approve a formula, follow these steps.</span></span>

1. <span data-ttu-id="7287a-113">Farið í **Stjórnun framleiðsluupplýsinga \> Uppskriftir og formúlur \> Formúlur**.</span><span class="sxs-lookup"><span data-stu-id="7287a-113">Go to **Product information management \> Bills of materials and formulas \> Formulas**.</span></span>
1. <span data-ttu-id="7287a-114">Veljið viðeigandi formúlu.</span><span class="sxs-lookup"><span data-stu-id="7287a-114">Select the relevant formula.</span></span>
1. <span data-ttu-id="7287a-115">Á aðgerðasvæðinu, í flipanum **Formúla**, í flokknum **Vinna með**, skal velja **Samþykkja formúlu**.</span><span class="sxs-lookup"><span data-stu-id="7287a-115">On the Action Pane, on the **Formula** tab, in the **Maintain** group, select **Approve formula**.</span></span>
1. <span data-ttu-id="7287a-116">Í svarglugganum **Samþykkja uppskrift eða formúlu** skal velja samþykktaraðila og velja síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="7287a-116">In the **Approve BOM or formula** dialog box, select an approver, and then select **OK**.</span></span>
