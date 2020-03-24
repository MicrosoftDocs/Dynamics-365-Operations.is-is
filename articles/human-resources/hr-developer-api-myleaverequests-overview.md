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
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092038"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="db1fb-103">Yfirlit MyLeaveRequests</span><span class="sxs-lookup"><span data-stu-id="db1fb-103">MyLeaveRequests overview</span></span>

<span data-ttu-id="db1fb-104">MyLeaveRequests einingin í Microsoft Dynamics 365 Human Resources býður upp á lista yfir leyfisbeiðnir í kerfinu, umfangsmiklar (takmarkaðar) fyrir beiðnirnar sem eru aðgengilegar núverandi notanda sem fyrirspurnir eininguna.</span><span class="sxs-lookup"><span data-stu-id="db1fb-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="db1fb-105">Lykill</span><span class="sxs-lookup"><span data-stu-id="db1fb-105">Key</span></span>

  | <span data-ttu-id="db1fb-106">Nafn eiginleika</span><span class="sxs-lookup"><span data-stu-id="db1fb-106">Property Name</span></span> | <span data-ttu-id="db1fb-107">Gagnagerð</span><span class="sxs-lookup"><span data-stu-id="db1fb-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="db1fb-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="db1fb-108">dataAreaId</span></span>    | <span data-ttu-id="db1fb-109">Strengur</span><span class="sxs-lookup"><span data-stu-id="db1fb-109">String</span></span>    |
  | <span data-ttu-id="db1fb-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="db1fb-110">RequestId</span></span>     | <span data-ttu-id="db1fb-111">Strengur</span><span class="sxs-lookup"><span data-stu-id="db1fb-111">String</span></span>    |
  | <span data-ttu-id="db1fb-112">LeaveType</span><span class="sxs-lookup"><span data-stu-id="db1fb-112">LeaveType</span></span>     | <span data-ttu-id="db1fb-113">Strengur</span><span class="sxs-lookup"><span data-stu-id="db1fb-113">String</span></span>    |
  | <span data-ttu-id="db1fb-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="db1fb-114">LeaveDate</span></span>     | <span data-ttu-id="db1fb-115">Dagsetning</span><span class="sxs-lookup"><span data-stu-id="db1fb-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="db1fb-116">Eiginleikar</span><span class="sxs-lookup"><span data-stu-id="db1fb-116">Properties</span></span>

  | <span data-ttu-id="db1fb-117">Nafn eiginleika</span><span class="sxs-lookup"><span data-stu-id="db1fb-117">Property Name</span></span>     | <span data-ttu-id="db1fb-118">Gagnagerð</span><span class="sxs-lookup"><span data-stu-id="db1fb-118">Data Type</span></span> | <span data-ttu-id="db1fb-119">Krafa</span><span class="sxs-lookup"><span data-stu-id="db1fb-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="db1fb-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="db1fb-120">dataAreaId</span></span>        | <span data-ttu-id="db1fb-121">Strengur</span><span class="sxs-lookup"><span data-stu-id="db1fb-121">String</span></span>    | <span data-ttu-id="db1fb-122">X</span><span class="sxs-lookup"><span data-stu-id="db1fb-122">X</span></span>        |
  | <span data-ttu-id="db1fb-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="db1fb-123">RequestId</span></span>         | <span data-ttu-id="db1fb-124">Strengur</span><span class="sxs-lookup"><span data-stu-id="db1fb-124">String</span></span>    | <span data-ttu-id="db1fb-125">X</span><span class="sxs-lookup"><span data-stu-id="db1fb-125">X</span></span>        |
  | <span data-ttu-id="db1fb-126">LeaveType</span><span class="sxs-lookup"><span data-stu-id="db1fb-126">LeaveType</span></span>         | <span data-ttu-id="db1fb-127">Strengur</span><span class="sxs-lookup"><span data-stu-id="db1fb-127">String</span></span>    | <span data-ttu-id="db1fb-128">X</span><span class="sxs-lookup"><span data-stu-id="db1fb-128">X</span></span>        |
  | <span data-ttu-id="db1fb-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="db1fb-129">LeaveDate</span></span>         | <span data-ttu-id="db1fb-130">Dagsetning</span><span class="sxs-lookup"><span data-stu-id="db1fb-130">Date</span></span>      | <span data-ttu-id="db1fb-131">X</span><span class="sxs-lookup"><span data-stu-id="db1fb-131">X</span></span>        |
  | <span data-ttu-id="db1fb-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="db1fb-132">ReasonCodeId</span></span>      | <span data-ttu-id="db1fb-133">Strengur</span><span class="sxs-lookup"><span data-stu-id="db1fb-133">String</span></span>    |          |
  | <span data-ttu-id="db1fb-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="db1fb-134">PersonnelNumber</span></span>   | <span data-ttu-id="db1fb-135">Strengur</span><span class="sxs-lookup"><span data-stu-id="db1fb-135">String</span></span>    | <span data-ttu-id="db1fb-136">X</span><span class="sxs-lookup"><span data-stu-id="db1fb-136">X</span></span>        |
  | <span data-ttu-id="db1fb-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="db1fb-137">RequestDate</span></span>       | <span data-ttu-id="db1fb-138">Dagsetning</span><span class="sxs-lookup"><span data-stu-id="db1fb-138">Date</span></span>      | <span data-ttu-id="db1fb-139">X</span><span class="sxs-lookup"><span data-stu-id="db1fb-139">X</span></span>        |
  | <span data-ttu-id="db1fb-140">Athugasemd</span><span class="sxs-lookup"><span data-stu-id="db1fb-140">Comment</span></span>           | <span data-ttu-id="db1fb-141">Strengur</span><span class="sxs-lookup"><span data-stu-id="db1fb-141">String</span></span>    |          |
  | <span data-ttu-id="db1fb-142">Staða</span><span class="sxs-lookup"><span data-stu-id="db1fb-142">Status</span></span>            | <span data-ttu-id="db1fb-143">Upptalning</span><span class="sxs-lookup"><span data-stu-id="db1fb-143">Enum</span></span>      | <span data-ttu-id="db1fb-144">X</span><span class="sxs-lookup"><span data-stu-id="db1fb-144">X</span></span>        |
  | <span data-ttu-id="db1fb-145">Upphæð</span><span class="sxs-lookup"><span data-stu-id="db1fb-145">Amount</span></span>            | <span data-ttu-id="db1fb-146">Rauntala</span><span class="sxs-lookup"><span data-stu-id="db1fb-146">Real</span></span>      |          |
  | <span data-ttu-id="db1fb-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="db1fb-147">HalfDayDefinition</span></span> | <span data-ttu-id="db1fb-148">Upptalning</span><span class="sxs-lookup"><span data-stu-id="db1fb-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="db1fb-149">Aðgerðir</span><span class="sxs-lookup"><span data-stu-id="db1fb-149">Actions</span></span>

 | <span data-ttu-id="db1fb-150">Heiti aðgerðar</span><span class="sxs-lookup"><span data-stu-id="db1fb-150">Action Name</span></span>                               | <span data-ttu-id="db1fb-151">Lýsing</span><span class="sxs-lookup"><span data-stu-id="db1fb-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="db1fb-152">senda inn</span><span class="sxs-lookup"><span data-stu-id="db1fb-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="db1fb-153">Sendu beiðnina sem á að vinna úr með verkflæði.</span><span class="sxs-lookup"><span data-stu-id="db1fb-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="db1fb-154">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="db1fb-154">See also</span></span>

- [<span data-ttu-id="db1fb-155">Senda leyfisbeiðni í verkflæði</span><span class="sxs-lookup"><span data-stu-id="db1fb-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="db1fb-156">Sannvottun</span><span class="sxs-lookup"><span data-stu-id="db1fb-156">Authentication</span></span>](hr-developer-api-authentication.md)