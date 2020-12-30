---
title: Yfirlit MyLeaveRequests
description: MyLeaveRequests einingin í Microsoft Dynamics 365 Human Resources býður upp á lista yfir leyfisbeiðnir í kerfinu, umfangsmiklar (takmarkaðar) fyrir beiðnirnar sem eru aðgengilegar núverandi notanda sem fyrirspurnir eininguna.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
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
ms.openlocfilehash: 4bf3b298af9eb39e03514a4005afb43a42908e47
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4418955"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="f04d3-103">Yfirlit MyLeaveRequests</span><span class="sxs-lookup"><span data-stu-id="f04d3-103">MyLeaveRequests overview</span></span>

<span data-ttu-id="f04d3-104">MyLeaveRequests einingin í Microsoft Dynamics 365 Human Resources býður upp á lista yfir leyfisbeiðnir í kerfinu, umfangsmiklar (takmarkaðar) fyrir beiðnirnar sem eru aðgengilegar núverandi notanda sem fyrirspurnir eininguna.</span><span class="sxs-lookup"><span data-stu-id="f04d3-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="f04d3-105">Lykill</span><span class="sxs-lookup"><span data-stu-id="f04d3-105">Key</span></span>

  | <span data-ttu-id="f04d3-106">Nafn eiginleika</span><span class="sxs-lookup"><span data-stu-id="f04d3-106">Property Name</span></span> | <span data-ttu-id="f04d3-107">Gagnagerð</span><span class="sxs-lookup"><span data-stu-id="f04d3-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="f04d3-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="f04d3-108">dataAreaId</span></span>    | <span data-ttu-id="f04d3-109">Strengur</span><span class="sxs-lookup"><span data-stu-id="f04d3-109">String</span></span>    |
  | <span data-ttu-id="f04d3-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="f04d3-110">RequestId</span></span>     | <span data-ttu-id="f04d3-111">Strengur</span><span class="sxs-lookup"><span data-stu-id="f04d3-111">String</span></span>    |
  | <span data-ttu-id="f04d3-112">LeaveType</span><span class="sxs-lookup"><span data-stu-id="f04d3-112">LeaveType</span></span>     | <span data-ttu-id="f04d3-113">Strengur</span><span class="sxs-lookup"><span data-stu-id="f04d3-113">String</span></span>    |
  | <span data-ttu-id="f04d3-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="f04d3-114">LeaveDate</span></span>     | <span data-ttu-id="f04d3-115">Dagsetning</span><span class="sxs-lookup"><span data-stu-id="f04d3-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="f04d3-116">Eiginleikar</span><span class="sxs-lookup"><span data-stu-id="f04d3-116">Properties</span></span>

  | <span data-ttu-id="f04d3-117">Nafn eiginleika</span><span class="sxs-lookup"><span data-stu-id="f04d3-117">Property Name</span></span>     | <span data-ttu-id="f04d3-118">Gagnagerð</span><span class="sxs-lookup"><span data-stu-id="f04d3-118">Data Type</span></span> | <span data-ttu-id="f04d3-119">Krafa</span><span class="sxs-lookup"><span data-stu-id="f04d3-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="f04d3-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="f04d3-120">dataAreaId</span></span>        | <span data-ttu-id="f04d3-121">Strengur</span><span class="sxs-lookup"><span data-stu-id="f04d3-121">String</span></span>    | <span data-ttu-id="f04d3-122">X</span><span class="sxs-lookup"><span data-stu-id="f04d3-122">X</span></span>        |
  | <span data-ttu-id="f04d3-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="f04d3-123">RequestId</span></span>         | <span data-ttu-id="f04d3-124">Strengur</span><span class="sxs-lookup"><span data-stu-id="f04d3-124">String</span></span>    | <span data-ttu-id="f04d3-125">X</span><span class="sxs-lookup"><span data-stu-id="f04d3-125">X</span></span>        |
  | <span data-ttu-id="f04d3-126">LeaveType</span><span class="sxs-lookup"><span data-stu-id="f04d3-126">LeaveType</span></span>         | <span data-ttu-id="f04d3-127">Strengur</span><span class="sxs-lookup"><span data-stu-id="f04d3-127">String</span></span>    | <span data-ttu-id="f04d3-128">X</span><span class="sxs-lookup"><span data-stu-id="f04d3-128">X</span></span>        |
  | <span data-ttu-id="f04d3-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="f04d3-129">LeaveDate</span></span>         | <span data-ttu-id="f04d3-130">Dagsetning</span><span class="sxs-lookup"><span data-stu-id="f04d3-130">Date</span></span>      | <span data-ttu-id="f04d3-131">X</span><span class="sxs-lookup"><span data-stu-id="f04d3-131">X</span></span>        |
  | <span data-ttu-id="f04d3-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="f04d3-132">ReasonCodeId</span></span>      | <span data-ttu-id="f04d3-133">Strengur</span><span class="sxs-lookup"><span data-stu-id="f04d3-133">String</span></span>    |          |
  | <span data-ttu-id="f04d3-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="f04d3-134">PersonnelNumber</span></span>   | <span data-ttu-id="f04d3-135">Strengur</span><span class="sxs-lookup"><span data-stu-id="f04d3-135">String</span></span>    | <span data-ttu-id="f04d3-136">X</span><span class="sxs-lookup"><span data-stu-id="f04d3-136">X</span></span>        |
  | <span data-ttu-id="f04d3-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="f04d3-137">RequestDate</span></span>       | <span data-ttu-id="f04d3-138">Dagsetning</span><span class="sxs-lookup"><span data-stu-id="f04d3-138">Date</span></span>      | <span data-ttu-id="f04d3-139">X</span><span class="sxs-lookup"><span data-stu-id="f04d3-139">X</span></span>        |
  | <span data-ttu-id="f04d3-140">Athugasemd</span><span class="sxs-lookup"><span data-stu-id="f04d3-140">Comment</span></span>           | <span data-ttu-id="f04d3-141">Strengur</span><span class="sxs-lookup"><span data-stu-id="f04d3-141">String</span></span>    |          |
  | <span data-ttu-id="f04d3-142">Staða</span><span class="sxs-lookup"><span data-stu-id="f04d3-142">Status</span></span>            | <span data-ttu-id="f04d3-143">Upptalning</span><span class="sxs-lookup"><span data-stu-id="f04d3-143">Enum</span></span>      | <span data-ttu-id="f04d3-144">X</span><span class="sxs-lookup"><span data-stu-id="f04d3-144">X</span></span>        |
  | <span data-ttu-id="f04d3-145">Upphæð</span><span class="sxs-lookup"><span data-stu-id="f04d3-145">Amount</span></span>            | <span data-ttu-id="f04d3-146">Rauntala</span><span class="sxs-lookup"><span data-stu-id="f04d3-146">Real</span></span>      |          |
  | <span data-ttu-id="f04d3-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="f04d3-147">HalfDayDefinition</span></span> | <span data-ttu-id="f04d3-148">Upptalning</span><span class="sxs-lookup"><span data-stu-id="f04d3-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="f04d3-149">Aðgerðir</span><span class="sxs-lookup"><span data-stu-id="f04d3-149">Actions</span></span>

 | <span data-ttu-id="f04d3-150">Heiti aðgerðar</span><span class="sxs-lookup"><span data-stu-id="f04d3-150">Action Name</span></span>                               | <span data-ttu-id="f04d3-151">Lýsing</span><span class="sxs-lookup"><span data-stu-id="f04d3-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="f04d3-152">senda inn</span><span class="sxs-lookup"><span data-stu-id="f04d3-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="f04d3-153">Sendu beiðnina sem á að vinna úr með verkflæði.</span><span class="sxs-lookup"><span data-stu-id="f04d3-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="f04d3-154">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="f04d3-154">See also</span></span>

- [<span data-ttu-id="f04d3-155">Senda leyfisbeiðni í verkflæði</span><span class="sxs-lookup"><span data-stu-id="f04d3-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="f04d3-156">Sannvottun</span><span class="sxs-lookup"><span data-stu-id="f04d3-156">Authentication</span></span>](hr-developer-api-authentication.md)