---
title: Yfirlit MyLeaveRequests
description: MyLeaveRequests einingin í Microsoft Dynamics 365 Human Resources býður upp á lista yfir leyfisbeiðnir í kerfinu, umfangsmiklar (takmarkaðar) fyrir beiðnirnar sem eru aðgengilegar núverandi notanda sem fyrirspurnir eininguna.
author: andreabichsel
manager: tfehr
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
ms.openlocfilehash: 0ca5bc225400338e76faee41a279e91fc00ce570
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115537"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="ac457-103">Yfirlit MyLeaveRequests</span><span class="sxs-lookup"><span data-stu-id="ac457-103">MyLeaveRequests overview</span></span>

<span data-ttu-id="ac457-104">MyLeaveRequests einingin í Microsoft Dynamics 365 Human Resources býður upp á lista yfir leyfisbeiðnir í kerfinu, umfangsmiklar (takmarkaðar) fyrir beiðnirnar sem eru aðgengilegar núverandi notanda sem fyrirspurnir eininguna.</span><span class="sxs-lookup"><span data-stu-id="ac457-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="ac457-105">Lykill</span><span class="sxs-lookup"><span data-stu-id="ac457-105">Key</span></span>

  | <span data-ttu-id="ac457-106">Nafn eiginleika</span><span class="sxs-lookup"><span data-stu-id="ac457-106">Property Name</span></span> | <span data-ttu-id="ac457-107">Gagnagerð</span><span class="sxs-lookup"><span data-stu-id="ac457-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="ac457-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="ac457-108">dataAreaId</span></span>    | <span data-ttu-id="ac457-109">Strengur</span><span class="sxs-lookup"><span data-stu-id="ac457-109">String</span></span>    |
  | <span data-ttu-id="ac457-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="ac457-110">RequestId</span></span>     | <span data-ttu-id="ac457-111">Strengur</span><span class="sxs-lookup"><span data-stu-id="ac457-111">String</span></span>    |
  | <span data-ttu-id="ac457-112">LeaveType</span><span class="sxs-lookup"><span data-stu-id="ac457-112">LeaveType</span></span>     | <span data-ttu-id="ac457-113">Strengur</span><span class="sxs-lookup"><span data-stu-id="ac457-113">String</span></span>    |
  | <span data-ttu-id="ac457-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="ac457-114">LeaveDate</span></span>     | <span data-ttu-id="ac457-115">Dagsetning</span><span class="sxs-lookup"><span data-stu-id="ac457-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="ac457-116">Eiginleikar</span><span class="sxs-lookup"><span data-stu-id="ac457-116">Properties</span></span>

  | <span data-ttu-id="ac457-117">Nafn eiginleika</span><span class="sxs-lookup"><span data-stu-id="ac457-117">Property Name</span></span>     | <span data-ttu-id="ac457-118">Gagnagerð</span><span class="sxs-lookup"><span data-stu-id="ac457-118">Data Type</span></span> | <span data-ttu-id="ac457-119">Krafa</span><span class="sxs-lookup"><span data-stu-id="ac457-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="ac457-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="ac457-120">dataAreaId</span></span>        | <span data-ttu-id="ac457-121">Strengur</span><span class="sxs-lookup"><span data-stu-id="ac457-121">String</span></span>    | <span data-ttu-id="ac457-122">X</span><span class="sxs-lookup"><span data-stu-id="ac457-122">X</span></span>        |
  | <span data-ttu-id="ac457-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="ac457-123">RequestId</span></span>         | <span data-ttu-id="ac457-124">Strengur</span><span class="sxs-lookup"><span data-stu-id="ac457-124">String</span></span>    | <span data-ttu-id="ac457-125">X</span><span class="sxs-lookup"><span data-stu-id="ac457-125">X</span></span>        |
  | <span data-ttu-id="ac457-126">LeaveType</span><span class="sxs-lookup"><span data-stu-id="ac457-126">LeaveType</span></span>         | <span data-ttu-id="ac457-127">Strengur</span><span class="sxs-lookup"><span data-stu-id="ac457-127">String</span></span>    | <span data-ttu-id="ac457-128">X</span><span class="sxs-lookup"><span data-stu-id="ac457-128">X</span></span>        |
  | <span data-ttu-id="ac457-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="ac457-129">LeaveDate</span></span>         | <span data-ttu-id="ac457-130">Dagsetning</span><span class="sxs-lookup"><span data-stu-id="ac457-130">Date</span></span>      | <span data-ttu-id="ac457-131">X</span><span class="sxs-lookup"><span data-stu-id="ac457-131">X</span></span>        |
  | <span data-ttu-id="ac457-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="ac457-132">ReasonCodeId</span></span>      | <span data-ttu-id="ac457-133">Strengur</span><span class="sxs-lookup"><span data-stu-id="ac457-133">String</span></span>    |          |
  | <span data-ttu-id="ac457-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="ac457-134">PersonnelNumber</span></span>   | <span data-ttu-id="ac457-135">Strengur</span><span class="sxs-lookup"><span data-stu-id="ac457-135">String</span></span>    | <span data-ttu-id="ac457-136">X</span><span class="sxs-lookup"><span data-stu-id="ac457-136">X</span></span>        |
  | <span data-ttu-id="ac457-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="ac457-137">RequestDate</span></span>       | <span data-ttu-id="ac457-138">Dagsetning</span><span class="sxs-lookup"><span data-stu-id="ac457-138">Date</span></span>      | <span data-ttu-id="ac457-139">X</span><span class="sxs-lookup"><span data-stu-id="ac457-139">X</span></span>        |
  | <span data-ttu-id="ac457-140">Athugasemd</span><span class="sxs-lookup"><span data-stu-id="ac457-140">Comment</span></span>           | <span data-ttu-id="ac457-141">Strengur</span><span class="sxs-lookup"><span data-stu-id="ac457-141">String</span></span>    |          |
  | <span data-ttu-id="ac457-142">Staða</span><span class="sxs-lookup"><span data-stu-id="ac457-142">Status</span></span>            | <span data-ttu-id="ac457-143">Upptalning</span><span class="sxs-lookup"><span data-stu-id="ac457-143">Enum</span></span>      | <span data-ttu-id="ac457-144">X</span><span class="sxs-lookup"><span data-stu-id="ac457-144">X</span></span>        |
  | <span data-ttu-id="ac457-145">Upphæð</span><span class="sxs-lookup"><span data-stu-id="ac457-145">Amount</span></span>            | <span data-ttu-id="ac457-146">Rauntala</span><span class="sxs-lookup"><span data-stu-id="ac457-146">Real</span></span>      |          |
  | <span data-ttu-id="ac457-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="ac457-147">HalfDayDefinition</span></span> | <span data-ttu-id="ac457-148">Upptalning</span><span class="sxs-lookup"><span data-stu-id="ac457-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="ac457-149">Aðgerðir</span><span class="sxs-lookup"><span data-stu-id="ac457-149">Actions</span></span>

 | <span data-ttu-id="ac457-150">Heiti aðgerðar</span><span class="sxs-lookup"><span data-stu-id="ac457-150">Action Name</span></span>                               | <span data-ttu-id="ac457-151">Lýsing</span><span class="sxs-lookup"><span data-stu-id="ac457-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="ac457-152">senda inn</span><span class="sxs-lookup"><span data-stu-id="ac457-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="ac457-153">Sendu beiðnina sem á að vinna úr með verkflæði.</span><span class="sxs-lookup"><span data-stu-id="ac457-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="ac457-154">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="ac457-154">See also</span></span>

- [<span data-ttu-id="ac457-155">Senda leyfisbeiðni í verkflæði</span><span class="sxs-lookup"><span data-stu-id="ac457-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="ac457-156">Sannvottun</span><span class="sxs-lookup"><span data-stu-id="ac457-156">Authentication</span></span>](hr-developer-api-authentication.md)