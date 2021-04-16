---
title: Yfirlit MyLeaveRequests
description: MyLeaveRequests einingin í Microsoft Dynamics 365 Human Resources býður upp á lista yfir leyfisbeiðnir í kerfinu, umfangsmiklar (takmarkaðar) fyrir beiðnirnar sem eru aðgengilegar núverandi notanda sem fyrirspurnir eininguna.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 44e23a076733bac782a0366aeba3456911522abe
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803634"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="48fa9-103">Yfirlit MyLeaveRequests</span><span class="sxs-lookup"><span data-stu-id="48fa9-103">MyLeaveRequests overview</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="48fa9-104">MyLeaveRequests einingin í Microsoft Dynamics 365 Human Resources býður upp á lista yfir leyfisbeiðnir í kerfinu, umfangsmiklar (takmarkaðar) fyrir beiðnirnar sem eru aðgengilegar núverandi notanda sem fyrirspurnir eininguna.</span><span class="sxs-lookup"><span data-stu-id="48fa9-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="48fa9-105">Lykill</span><span class="sxs-lookup"><span data-stu-id="48fa9-105">Key</span></span>

  | <span data-ttu-id="48fa9-106">Nafn eiginleika</span><span class="sxs-lookup"><span data-stu-id="48fa9-106">Property Name</span></span> | <span data-ttu-id="48fa9-107">Gagnagerð</span><span class="sxs-lookup"><span data-stu-id="48fa9-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="48fa9-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="48fa9-108">dataAreaId</span></span>    | <span data-ttu-id="48fa9-109">Strengur</span><span class="sxs-lookup"><span data-stu-id="48fa9-109">String</span></span>    |
  | <span data-ttu-id="48fa9-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="48fa9-110">RequestId</span></span>     | <span data-ttu-id="48fa9-111">Strengur</span><span class="sxs-lookup"><span data-stu-id="48fa9-111">String</span></span>    |
  | <span data-ttu-id="48fa9-112">LeaveType</span><span class="sxs-lookup"><span data-stu-id="48fa9-112">LeaveType</span></span>     | <span data-ttu-id="48fa9-113">Strengur</span><span class="sxs-lookup"><span data-stu-id="48fa9-113">String</span></span>    |
  | <span data-ttu-id="48fa9-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="48fa9-114">LeaveDate</span></span>     | <span data-ttu-id="48fa9-115">Dagsetning</span><span class="sxs-lookup"><span data-stu-id="48fa9-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="48fa9-116">Eiginleikar</span><span class="sxs-lookup"><span data-stu-id="48fa9-116">Properties</span></span>

  | <span data-ttu-id="48fa9-117">Nafn eiginleika</span><span class="sxs-lookup"><span data-stu-id="48fa9-117">Property Name</span></span>     | <span data-ttu-id="48fa9-118">Gagnagerð</span><span class="sxs-lookup"><span data-stu-id="48fa9-118">Data Type</span></span> | <span data-ttu-id="48fa9-119">Krafa</span><span class="sxs-lookup"><span data-stu-id="48fa9-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="48fa9-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="48fa9-120">dataAreaId</span></span>        | <span data-ttu-id="48fa9-121">Strengur</span><span class="sxs-lookup"><span data-stu-id="48fa9-121">String</span></span>    | <span data-ttu-id="48fa9-122">X</span><span class="sxs-lookup"><span data-stu-id="48fa9-122">X</span></span>        |
  | <span data-ttu-id="48fa9-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="48fa9-123">RequestId</span></span>         | <span data-ttu-id="48fa9-124">Strengur</span><span class="sxs-lookup"><span data-stu-id="48fa9-124">String</span></span>    | <span data-ttu-id="48fa9-125">X</span><span class="sxs-lookup"><span data-stu-id="48fa9-125">X</span></span>        |
  | <span data-ttu-id="48fa9-126">LeaveType</span><span class="sxs-lookup"><span data-stu-id="48fa9-126">LeaveType</span></span>         | <span data-ttu-id="48fa9-127">Strengur</span><span class="sxs-lookup"><span data-stu-id="48fa9-127">String</span></span>    | <span data-ttu-id="48fa9-128">X</span><span class="sxs-lookup"><span data-stu-id="48fa9-128">X</span></span>        |
  | <span data-ttu-id="48fa9-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="48fa9-129">LeaveDate</span></span>         | <span data-ttu-id="48fa9-130">Dagsetning</span><span class="sxs-lookup"><span data-stu-id="48fa9-130">Date</span></span>      | <span data-ttu-id="48fa9-131">X</span><span class="sxs-lookup"><span data-stu-id="48fa9-131">X</span></span>        |
  | <span data-ttu-id="48fa9-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="48fa9-132">ReasonCodeId</span></span>      | <span data-ttu-id="48fa9-133">Strengur</span><span class="sxs-lookup"><span data-stu-id="48fa9-133">String</span></span>    |          |
  | <span data-ttu-id="48fa9-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="48fa9-134">PersonnelNumber</span></span>   | <span data-ttu-id="48fa9-135">Strengur</span><span class="sxs-lookup"><span data-stu-id="48fa9-135">String</span></span>    | <span data-ttu-id="48fa9-136">X</span><span class="sxs-lookup"><span data-stu-id="48fa9-136">X</span></span>        |
  | <span data-ttu-id="48fa9-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="48fa9-137">RequestDate</span></span>       | <span data-ttu-id="48fa9-138">Dagsetning</span><span class="sxs-lookup"><span data-stu-id="48fa9-138">Date</span></span>      | <span data-ttu-id="48fa9-139">X</span><span class="sxs-lookup"><span data-stu-id="48fa9-139">X</span></span>        |
  | <span data-ttu-id="48fa9-140">Athugasemd</span><span class="sxs-lookup"><span data-stu-id="48fa9-140">Comment</span></span>           | <span data-ttu-id="48fa9-141">Strengur</span><span class="sxs-lookup"><span data-stu-id="48fa9-141">String</span></span>    |          |
  | <span data-ttu-id="48fa9-142">Staða</span><span class="sxs-lookup"><span data-stu-id="48fa9-142">Status</span></span>            | <span data-ttu-id="48fa9-143">Upptalning</span><span class="sxs-lookup"><span data-stu-id="48fa9-143">Enum</span></span>      | <span data-ttu-id="48fa9-144">X</span><span class="sxs-lookup"><span data-stu-id="48fa9-144">X</span></span>        |
  | <span data-ttu-id="48fa9-145">Upphæð</span><span class="sxs-lookup"><span data-stu-id="48fa9-145">Amount</span></span>            | <span data-ttu-id="48fa9-146">Rauntala</span><span class="sxs-lookup"><span data-stu-id="48fa9-146">Real</span></span>      |          |
  | <span data-ttu-id="48fa9-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="48fa9-147">HalfDayDefinition</span></span> | <span data-ttu-id="48fa9-148">Upptalning</span><span class="sxs-lookup"><span data-stu-id="48fa9-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="48fa9-149">Aðgerðir</span><span class="sxs-lookup"><span data-stu-id="48fa9-149">Actions</span></span>

 | <span data-ttu-id="48fa9-150">Heiti aðgerðar</span><span class="sxs-lookup"><span data-stu-id="48fa9-150">Action Name</span></span>                               | <span data-ttu-id="48fa9-151">Lýsing</span><span class="sxs-lookup"><span data-stu-id="48fa9-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="48fa9-152">senda inn</span><span class="sxs-lookup"><span data-stu-id="48fa9-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="48fa9-153">Sendu beiðnina sem á að vinna úr með verkflæði.</span><span class="sxs-lookup"><span data-stu-id="48fa9-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="48fa9-154">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="48fa9-154">See also</span></span>

- [<span data-ttu-id="48fa9-155">Senda leyfisbeiðni í verkflæði</span><span class="sxs-lookup"><span data-stu-id="48fa9-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="48fa9-156">Sannvottun</span><span class="sxs-lookup"><span data-stu-id="48fa9-156">Authentication</span></span>](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]