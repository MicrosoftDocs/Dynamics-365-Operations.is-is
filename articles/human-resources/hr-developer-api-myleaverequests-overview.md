---
title: Yfirlit MyLeaveRequests
description: ''
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
ms.openlocfilehash: 66f161d6736b1bb544d02871d9d51b2949b1cfa0
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009407"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="7c030-102">Yfirlit MyLeaveRequests</span><span class="sxs-lookup"><span data-stu-id="7c030-102">MyLeaveRequests overview</span></span>

<span data-ttu-id="7c030-103">MyLeaveRequests einingin í Microsoft Dynamics 365 Human Resources býður upp á lista yfir leyfisbeiðnir í kerfinu, umfangsmiklar (takmarkaðar) fyrir beiðnirnar sem eru aðgengilegar núverandi notanda sem fyrirspurnir eininguna.</span><span class="sxs-lookup"><span data-stu-id="7c030-103">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="7c030-104">Lykill</span><span class="sxs-lookup"><span data-stu-id="7c030-104">Key</span></span>

  | <span data-ttu-id="7c030-105">Nafn eiginleika</span><span class="sxs-lookup"><span data-stu-id="7c030-105">Property Name</span></span> | <span data-ttu-id="7c030-106">Gagnagerð</span><span class="sxs-lookup"><span data-stu-id="7c030-106">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="7c030-107">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="7c030-107">dataAreaId</span></span>    | <span data-ttu-id="7c030-108">Strengur</span><span class="sxs-lookup"><span data-stu-id="7c030-108">String</span></span>    |
  | <span data-ttu-id="7c030-109">RequestId</span><span class="sxs-lookup"><span data-stu-id="7c030-109">RequestId</span></span>     | <span data-ttu-id="7c030-110">Strengur</span><span class="sxs-lookup"><span data-stu-id="7c030-110">String</span></span>    |
  | <span data-ttu-id="7c030-111">LeaveType</span><span class="sxs-lookup"><span data-stu-id="7c030-111">LeaveType</span></span>     | <span data-ttu-id="7c030-112">Strengur</span><span class="sxs-lookup"><span data-stu-id="7c030-112">String</span></span>    |
  | <span data-ttu-id="7c030-113">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="7c030-113">LeaveDate</span></span>     | <span data-ttu-id="7c030-114">Dagsetning</span><span class="sxs-lookup"><span data-stu-id="7c030-114">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="7c030-115">Eiginleikar</span><span class="sxs-lookup"><span data-stu-id="7c030-115">Properties</span></span>

  | <span data-ttu-id="7c030-116">Nafn eiginleika</span><span class="sxs-lookup"><span data-stu-id="7c030-116">Property Name</span></span>     | <span data-ttu-id="7c030-117">Gagnagerð</span><span class="sxs-lookup"><span data-stu-id="7c030-117">Data Type</span></span> | <span data-ttu-id="7c030-118">Krafa</span><span class="sxs-lookup"><span data-stu-id="7c030-118">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="7c030-119">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="7c030-119">dataAreaId</span></span>        | <span data-ttu-id="7c030-120">Strengur</span><span class="sxs-lookup"><span data-stu-id="7c030-120">String</span></span>    | <span data-ttu-id="7c030-121">X</span><span class="sxs-lookup"><span data-stu-id="7c030-121">X</span></span>        |
  | <span data-ttu-id="7c030-122">RequestId</span><span class="sxs-lookup"><span data-stu-id="7c030-122">RequestId</span></span>         | <span data-ttu-id="7c030-123">Strengur</span><span class="sxs-lookup"><span data-stu-id="7c030-123">String</span></span>    | <span data-ttu-id="7c030-124">X</span><span class="sxs-lookup"><span data-stu-id="7c030-124">X</span></span>        |
  | <span data-ttu-id="7c030-125">LeaveType</span><span class="sxs-lookup"><span data-stu-id="7c030-125">LeaveType</span></span>         | <span data-ttu-id="7c030-126">Strengur</span><span class="sxs-lookup"><span data-stu-id="7c030-126">String</span></span>    | <span data-ttu-id="7c030-127">X</span><span class="sxs-lookup"><span data-stu-id="7c030-127">X</span></span>        |
  | <span data-ttu-id="7c030-128">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="7c030-128">LeaveDate</span></span>         | <span data-ttu-id="7c030-129">Dagsetning</span><span class="sxs-lookup"><span data-stu-id="7c030-129">Date</span></span>      | <span data-ttu-id="7c030-130">X</span><span class="sxs-lookup"><span data-stu-id="7c030-130">X</span></span>        |
  | <span data-ttu-id="7c030-131">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="7c030-131">ReasonCodeId</span></span>      | <span data-ttu-id="7c030-132">Strengur</span><span class="sxs-lookup"><span data-stu-id="7c030-132">String</span></span>    |          |
  | <span data-ttu-id="7c030-133">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="7c030-133">PersonnelNumber</span></span>   | <span data-ttu-id="7c030-134">Strengur</span><span class="sxs-lookup"><span data-stu-id="7c030-134">String</span></span>    | <span data-ttu-id="7c030-135">X</span><span class="sxs-lookup"><span data-stu-id="7c030-135">X</span></span>        |
  | <span data-ttu-id="7c030-136">RequestDate</span><span class="sxs-lookup"><span data-stu-id="7c030-136">RequestDate</span></span>       | <span data-ttu-id="7c030-137">Dagsetning</span><span class="sxs-lookup"><span data-stu-id="7c030-137">Date</span></span>      | <span data-ttu-id="7c030-138">X</span><span class="sxs-lookup"><span data-stu-id="7c030-138">X</span></span>        |
  | <span data-ttu-id="7c030-139">Athugasemd</span><span class="sxs-lookup"><span data-stu-id="7c030-139">Comment</span></span>           | <span data-ttu-id="7c030-140">Strengur</span><span class="sxs-lookup"><span data-stu-id="7c030-140">String</span></span>    |          |
  | <span data-ttu-id="7c030-141">Staða</span><span class="sxs-lookup"><span data-stu-id="7c030-141">Status</span></span>            | <span data-ttu-id="7c030-142">Upptalning</span><span class="sxs-lookup"><span data-stu-id="7c030-142">Enum</span></span>      | <span data-ttu-id="7c030-143">X</span><span class="sxs-lookup"><span data-stu-id="7c030-143">X</span></span>        |
  | <span data-ttu-id="7c030-144">Upphæð</span><span class="sxs-lookup"><span data-stu-id="7c030-144">Amount</span></span>            | <span data-ttu-id="7c030-145">Rauntala</span><span class="sxs-lookup"><span data-stu-id="7c030-145">Real</span></span>      |          |
  | <span data-ttu-id="7c030-146">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="7c030-146">HalfDayDefinition</span></span> | <span data-ttu-id="7c030-147">Upptalning</span><span class="sxs-lookup"><span data-stu-id="7c030-147">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="7c030-148">Aðgerðir</span><span class="sxs-lookup"><span data-stu-id="7c030-148">Actions</span></span>

 | <span data-ttu-id="7c030-149">Heiti aðgerðar</span><span class="sxs-lookup"><span data-stu-id="7c030-149">Action Name</span></span>                               | <span data-ttu-id="7c030-150">Lýsing</span><span class="sxs-lookup"><span data-stu-id="7c030-150">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="7c030-151">senda inn</span><span class="sxs-lookup"><span data-stu-id="7c030-151">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="7c030-152">Sendu beiðnina sem á að vinna úr með verkflæði.</span><span class="sxs-lookup"><span data-stu-id="7c030-152">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="7c030-153">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="7c030-153">See also</span></span>

- [<span data-ttu-id="7c030-154">Senda leyfisbeiðni í verkflæði</span><span class="sxs-lookup"><span data-stu-id="7c030-154">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="7c030-155">Sannvottun</span><span class="sxs-lookup"><span data-stu-id="7c030-155">Authentication</span></span>](hr-developer-api-authentication.md)