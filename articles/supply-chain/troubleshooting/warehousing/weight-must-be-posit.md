---
title: Þyngd verður að vera jákvæð
description: Þyngd verður að vera jákvæð
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSContainerCloseDiag_canClose
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: dcbcde3143cb509b68b277cb7c709263e2659b5b
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924304"
---
# <a name="weight-must-be-positive"></a><span data-ttu-id="9f4cc-103">Þyngd verður að vera jákvæð</span><span class="sxs-lookup"><span data-stu-id="9f4cc-103">Weight must be positive</span></span>

<span data-ttu-id="9f4cc-104">Villukóði: WeightMustBePositive</span><span class="sxs-lookup"><span data-stu-id="9f4cc-104">Error code: WeightMustBePositive</span></span>

## <a name="symptoms"></a><span data-ttu-id="9f4cc-105">Einkenni</span><span class="sxs-lookup"><span data-stu-id="9f4cc-105">Symptoms</span></span>

<span data-ttu-id="9f4cc-106">Kerfið sýnir eftirfarandi villuboð:</span><span class="sxs-lookup"><span data-stu-id="9f4cc-106">The system shows the following error message:</span></span>

> <span data-ttu-id="9f4cc-107">Þyngd verður að vera jákvæð tala.</span><span class="sxs-lookup"><span data-stu-id="9f4cc-107">Weight must be positive.</span></span>

## <a name="cause"></a><span data-ttu-id="9f4cc-108">Orsök</span><span class="sxs-lookup"><span data-stu-id="9f4cc-108">Cause</span></span>

<span data-ttu-id="9f4cc-109">Reiturinn **Brúttóþyngd** er stilltur á *0* (núll) eða neikvætt gildi.</span><span class="sxs-lookup"><span data-stu-id="9f4cc-109">The **Gross Weight** field is set to *0* (zero) or a negative value.</span></span>

## <a name="resolution"></a><span data-ttu-id="9f4cc-110">Upplausn</span><span class="sxs-lookup"><span data-stu-id="9f4cc-110">Resolution</span></span>

<span data-ttu-id="9f4cc-111">Fylgið einu af eftirfarandi skrefum til að tilgreina þyngd.</span><span class="sxs-lookup"><span data-stu-id="9f4cc-111">To specify a weight, follow one of these steps.</span></span>

- <span data-ttu-id="9f4cc-112">Stillið gildi á reitnum **Brúttóþyngd**.</span><span class="sxs-lookup"><span data-stu-id="9f4cc-112">In the **Gross weight** field, set a value.</span></span> <span data-ttu-id="9f4cc-113">Veljið síðan einingu í fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="9f4cc-113">Then select a unit in the drop-down list.</span></span>
- <span data-ttu-id="9f4cc-114">Veldu **Sækja kerfisþyngd** til að reikna út **Brúttóþyngd**.</span><span class="sxs-lookup"><span data-stu-id="9f4cc-114">Select **Get system weight** to calculate the **Gross weight** value.</span></span>
