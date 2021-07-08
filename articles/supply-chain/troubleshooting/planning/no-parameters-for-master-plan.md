---
title: Færibreytur fyrir aðaláætlun eru ekki til
description: Þegar reynt er að festa áætlaða pöntun berast villuboð sem segja að engar færibreytur séu til fyrir aðaláætlunina.
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
ms.openlocfilehash: d4b64af2e30109b8560d40c4c532504611528bbe
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294103"
---
# <a name="parameters-for-the-master-plan-dont-exist"></a><span data-ttu-id="ba167-103">Færibreytur fyrir aðaláætlun eru ekki til</span><span class="sxs-lookup"><span data-stu-id="ba167-103">Parameters for the master plan don't exist</span></span>

<span data-ttu-id="ba167-104">Villukóði SYS25368</span><span class="sxs-lookup"><span data-stu-id="ba167-104">Error code: SYS25368</span></span>

## <a name="symptoms"></a><span data-ttu-id="ba167-105">Einkenni</span><span class="sxs-lookup"><span data-stu-id="ba167-105">Symptoms</span></span>

<span data-ttu-id="ba167-106">Þegar reynt er að fastsetja áætlaða pöntun berast eftirfarandi villuboð:</span><span class="sxs-lookup"><span data-stu-id="ba167-106">When you try to firm a planned order, you receive the following error message:</span></span>

> <span data-ttu-id="ba167-107">Færibreytur fyrir aðaláætlunina %1 eru ekki til.</span><span class="sxs-lookup"><span data-stu-id="ba167-107">Parameters for master plan %1 do not exist.</span></span>

## <a name="cause"></a><span data-ttu-id="ba167-108">Orsök</span><span class="sxs-lookup"><span data-stu-id="ba167-108">Cause</span></span>

<span data-ttu-id="ba167-109">Vegna vandamála með skilgreiningu finnur kerfið ekki stillingar fyrir tilgreinda áætlun.</span><span class="sxs-lookup"><span data-stu-id="ba167-109">Because of configuration issues, the system can't find the settings for the specified plan.</span></span>

## <a name="resolution"></a><span data-ttu-id="ba167-110">Lausn</span><span class="sxs-lookup"><span data-stu-id="ba167-110">Resolution</span></span>

- <span data-ttu-id="ba167-111">Farið í **Aðaláætlanagerð \> Uppsetning \> Áætlanir \> Aðaláætlanir** og gangið úr skugga um að áætlun sem er með tilgreint heiti sé til staðar.</span><span class="sxs-lookup"><span data-stu-id="ba167-111">Go to **Master planning \> Setup \> Plans \> Master plans**, and make sure that a plan that has the specified name exists.</span></span>
