---
title: Lánardrottinn er ekki tilgreindur þegar áætlaðar pantanir eru staðfestar
description: Þegar reynt er að festa áætlaða pöntun berast villuboð sem segja að enginn lánardrottinn er tilgreindur.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: cf41295045211f8a714194494028922d573c9e9e
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294098"
---
# <a name="vendor-isnt-specified-when-planned-orders-are-firmed"></a><span data-ttu-id="a7e2c-103">Lánardrottinn er ekki tilgreindur þegar áætlaðar pantanir eru staðfestar</span><span class="sxs-lookup"><span data-stu-id="a7e2c-103">Vendor isn't specified when planned orders are firmed</span></span>

<span data-ttu-id="a7e2c-104">Villukóði SYS23532</span><span class="sxs-lookup"><span data-stu-id="a7e2c-104">Error code: SYS23532</span></span>

## <a name="symptoms"></a><span data-ttu-id="a7e2c-105">Einkenni</span><span class="sxs-lookup"><span data-stu-id="a7e2c-105">Symptoms</span></span>

<span data-ttu-id="a7e2c-106">Þegar reynt er að fastsetja áætlaðar pantanir berast eftirfarandi villuboð:</span><span class="sxs-lookup"><span data-stu-id="a7e2c-106">When you try to firm planned orders, you receive the following error message:</span></span>

> <span data-ttu-id="a7e2c-107">Lánardrottinn er ekki tilgreindur</span><span class="sxs-lookup"><span data-stu-id="a7e2c-107">Vendor is not specified</span></span>

## <a name="resolution"></a><span data-ttu-id="a7e2c-108">Lausn</span><span class="sxs-lookup"><span data-stu-id="a7e2c-108">Resolution</span></span>

<span data-ttu-id="a7e2c-109">Fylgið þessum skrefum til að tilgreina lánardrottin.</span><span class="sxs-lookup"><span data-stu-id="a7e2c-109">To specify a vendor, follow these steps.</span></span>

1. <span data-ttu-id="a7e2c-110">Opnið áætlaða pöntun þar sem vantar lánardrottin.</span><span class="sxs-lookup"><span data-stu-id="a7e2c-110">Open the planned order that is missing a vendor.</span></span>
1. <span data-ttu-id="a7e2c-111">Í flýtiflipanum **Áætlað framboð**, í reitnum **Lánardrottinn**, skal velja lánardrottin.</span><span class="sxs-lookup"><span data-stu-id="a7e2c-111">On the **Planned supply** FastTab, in the **Vendor** field, select a vendor.</span></span>
