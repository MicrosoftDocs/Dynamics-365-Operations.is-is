---
title: Skipuleggja þarf áætluðu framleiðslupöntunina áður en hægt er að staðfesta hana.
description: Þegar reynt er að festa áætlaða pöntun berast villuboð sem segja að áætla þurfi pöntunina áður en hægt er að staðfesta hana.
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
ms.openlocfilehash: a360cb3cbd26e1bc1ebb1baf1a6a4d8282c28c5c
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294105"
---
# <a name="planned-production-order-must-be-scheduled-before-it-can-be-firmed"></a><span data-ttu-id="78dda-103">Skipuleggja þarf áætluðu framleiðslupöntunina áður en hægt er að staðfesta hana.</span><span class="sxs-lookup"><span data-stu-id="78dda-103">Planned production order must be scheduled before it can be firmed</span></span>

<span data-ttu-id="78dda-104">Villukóði SYS309802</span><span class="sxs-lookup"><span data-stu-id="78dda-104">Error code: SYS309802</span></span>

## <a name="symptoms"></a><span data-ttu-id="78dda-105">Einkenni</span><span class="sxs-lookup"><span data-stu-id="78dda-105">Symptoms</span></span>

<span data-ttu-id="78dda-106">Þegar reynt er að fastsetja áætlaða pöntun berast eftirfarandi villuboð:</span><span class="sxs-lookup"><span data-stu-id="78dda-106">When you try to firm a planned order, you receive the following error message:</span></span>

> <span data-ttu-id="78dda-107">Skipuleggja þarf áætluðu framleiðslupöntunina áður en hægt er að staðfesta hana.</span><span class="sxs-lookup"><span data-stu-id="78dda-107">The planned production order must be scheduled before it can be firmed.</span></span>

## <a name="cause"></a><span data-ttu-id="78dda-108">Orsök</span><span class="sxs-lookup"><span data-stu-id="78dda-108">Cause</span></span>

<span data-ttu-id="78dda-109">Áætlaðar upphafs- og lokadagsetningar mega ekki vera auðar.</span><span class="sxs-lookup"><span data-stu-id="78dda-109">The scheduled start and end dates can't be blank.</span></span>

## <a name="resolution"></a><span data-ttu-id="78dda-110">Lausn</span><span class="sxs-lookup"><span data-stu-id="78dda-110">Resolution</span></span>

<span data-ttu-id="78dda-111">Til að tilgreina upphafs- og lokadagsetningu áætlaðrar pöntunar skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="78dda-111">To specify start and end dates for the planned order, follow these steps.</span></span>

1. <span data-ttu-id="78dda-112">Fara í **Áætlanagerð \> Aðaláætlanagerð \> Áætlaðar pantanir**.</span><span class="sxs-lookup"><span data-stu-id="78dda-112">Go to **Master planning \> Master planning \> Planned orders**.</span></span>
1. <span data-ttu-id="78dda-113">Opnið viðeigandi áætlaða pöntun.</span><span class="sxs-lookup"><span data-stu-id="78dda-113">Open the relevant planned order.</span></span>
1. <span data-ttu-id="78dda-114">Í flýtiflipanum **Almennt**, í hlutanum **Á áætlun**, skal tilgreina dagsetningar í reitunum **Upphafsdagsetning** og **Lokadagsetning**.</span><span class="sxs-lookup"><span data-stu-id="78dda-114">On the **General** FastTab, in the **Scheduled** section, specify dates in the **Start date** and **End date** fields.</span></span>
