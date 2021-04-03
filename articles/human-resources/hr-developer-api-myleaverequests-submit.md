---
title: Senda leyfisbeiðni í verkflæði
description: Í Microsoft Dynamics 365 Human Resources, þú getur notað MyLeaveRequests senda () forritunarviðmót forritsins (API) til að leggja fram leyfisbeiðni til verkflæðis.
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
ms.openlocfilehash: aeb3d66ad24f96efea1b0ea9828a537f8853c94b
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465487"
---
# <a name="submit-a-leave-request-to-workflow"></a><span data-ttu-id="c08c4-103">Senda leyfisbeiðni í verkflæði</span><span class="sxs-lookup"><span data-stu-id="c08c4-103">Submit a leave request to workflow</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="c08c4-104">Í Microsoft Dynamics 365 Human Resources, þú getur notað MyLeaveRequests senda () forritunarviðmót forritsins (API) til að leggja fram leyfisbeiðni til verkflæðis.</span><span class="sxs-lookup"><span data-stu-id="c08c4-104">In Microsoft Dynamics 365 Human Resources, you can use the MyLeaveRequests submit() application programming interface (API) to submit a leave request to workflow.</span></span> <span data-ttu-id="c08c4-105">Þetta API birtist sem aðgerð á MyLeaveRequests OData einingunni.</span><span class="sxs-lookup"><span data-stu-id="c08c4-105">This API is exposed as an action on the MyLeaveRequests OData entity.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c08c4-106">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="c08c4-106">Prerequisites</span></span>

<span data-ttu-id="c08c4-107">Leyfisbeiðnin verður að vera vistuð í gagnagrunninum og verður að endurheimta í gegnum MyLeaveRequests eininguna.</span><span class="sxs-lookup"><span data-stu-id="c08c4-107">The leave request must be saved in the database and must be retrievable through the MyLeaveRequests entity.</span></span>

## <a name="permissions"></a><span data-ttu-id="c08c4-108">Aðgangsheimildir</span><span class="sxs-lookup"><span data-stu-id="c08c4-108">Permissions</span></span>

<span data-ttu-id="c08c4-109">Ein af eftirfarandi heimildum er nauðsynleg til að kalla þetta API.</span><span class="sxs-lookup"><span data-stu-id="c08c4-109">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="c08c4-110">Frekari upplýsingar um heimildir og hvernig skuli velja þær er að finna í [Sannvottun](hr-developer-api-authentication.md).</span><span class="sxs-lookup"><span data-stu-id="c08c4-110">For more information about permissions and how to select them, see [Authentication](hr-developer-api-authentication.md).</span></span>

| <span data-ttu-id="c08c4-111">Gerð heimildar</span><span class="sxs-lookup"><span data-stu-id="c08c4-111">Permission type</span></span>                    | <span data-ttu-id="c08c4-112">Heimildir (frá minnst forréttinda til allra forréttinda)</span><span class="sxs-lookup"><span data-stu-id="c08c4-112">Permissions (from least privileged to most privileged)</span></span> |
|------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="c08c4-113">Úthlutað (vinnu- eða skólareikningur)</span><span class="sxs-lookup"><span data-stu-id="c08c4-113">Delegated (work or school account)</span></span> | <span data-ttu-id="c08c4-114">user\_impersonation</span><span class="sxs-lookup"><span data-stu-id="c08c4-114">user\_impersonation</span></span>                                    |

## <a name="https-request"></a><span data-ttu-id="c08c4-115">HTTPS beiðni</span><span class="sxs-lookup"><span data-stu-id="c08c4-115">HTTPS request</span></span>

<!-- { "blockType": "ignored" } -->
```HTTP
POST https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/MyLeaveRequests(RequestId='{requestId}', LeaveType='{leaveType}', LeaveDate={leaveDate}, dataAreaId={dataArea})/Microsoft.Dynamics.DataEntities.submit?cross-company=true
```

<span data-ttu-id="c08c4-116">Beiðnin er í samræmi við OData staðla.</span><span class="sxs-lookup"><span data-stu-id="c08c4-116">The request conforms to OData standards.</span></span> <span data-ttu-id="c08c4-117">Færibreyturnar {requestId}, {leaveType}, {leaveDate} og {dataArea} vísa til reitanna sem samanstanda af samsettum náttúrulykli fyrir MyLeaveRequests eininguna.</span><span class="sxs-lookup"><span data-stu-id="c08c4-117">The {requestId}, {leaveType}, {leaveDate}, and {dataArea} parameters refer to the fields that make up the composite natural key for the MyLeaveRequests entity.</span></span>

> [!NOTE]
> <span data-ttu-id="c08c4-118">Þó að reitirnir fyrir MyLeaveRequests einingina vísa til einstakrar línu í leyfisbeiðninni, mun hringja í senda API senda alla leyfisbeiðnina (allar línur) til verkflæðis.</span><span class="sxs-lookup"><span data-stu-id="c08c4-118">While the fields for the MyLeaveRequests entity refer to an individual line in the leave request, calling the submit API will submit the entire leave request (all lines) to workflow.</span></span>

### <a name="request-headers"></a><span data-ttu-id="c08c4-119">Haus beiðni</span><span class="sxs-lookup"><span data-stu-id="c08c4-119">Request headers</span></span>

| <span data-ttu-id="c08c4-120">Haus</span><span class="sxs-lookup"><span data-stu-id="c08c4-120">Header</span></span>         | <span data-ttu-id="c08c4-121">Value</span><span class="sxs-lookup"><span data-stu-id="c08c4-121">Value</span></span>                     |
|----------------|---------------------------|
| <span data-ttu-id="c08c4-122">Heimildir</span><span class="sxs-lookup"><span data-stu-id="c08c4-122">Authorization</span></span>  | <span data-ttu-id="c08c4-123">Handhafi {token} (krafist)</span><span class="sxs-lookup"><span data-stu-id="c08c4-123">Bearer {token} (required)</span></span> |
| <span data-ttu-id="c08c4-124">Efnistegund</span><span class="sxs-lookup"><span data-stu-id="c08c4-124">Content-Type</span></span>   | <span data-ttu-id="c08c4-125">application/json</span><span class="sxs-lookup"><span data-stu-id="c08c4-125">application/json</span></span>          |

### <a name="request-body"></a><span data-ttu-id="c08c4-126">Meginmál beiðni</span><span class="sxs-lookup"><span data-stu-id="c08c4-126">Request body</span></span>

<span data-ttu-id="c08c4-127">Ekki leggja fram beiðni aðila um þessa aðferð.</span><span class="sxs-lookup"><span data-stu-id="c08c4-127">Don't supply a request body for this method.</span></span>

### <a name="response"></a><span data-ttu-id="c08c4-128">Svar</span><span class="sxs-lookup"><span data-stu-id="c08c4-128">Response</span></span>

<span data-ttu-id="c08c4-129">Árangursrík svar er alltaf a **204 Ekkert innihald** svar.</span><span class="sxs-lookup"><span data-stu-id="c08c4-129">A successful response is always a **204 No Content** response.</span></span>

<span data-ttu-id="c08c4-130">Óheimilar gestir munu fá **401 Óleyfilegt** eða **403 Aðgangur bannaður** svar.</span><span class="sxs-lookup"><span data-stu-id="c08c4-130">Unauthorized callers will receive a **401 Unauthorized** or a **403 Forbidden** response.</span></span>

<span data-ttu-id="c08c4-131">Ef uppgjöf tekst ekki (vegna staðfestingar, til dæmis), verður svarið **500 Villa á þjóni**, og svaraðilinn mun innihalda JSON hlut með nánari upplýsingum.</span><span class="sxs-lookup"><span data-stu-id="c08c4-131">If submission is unsuccessful (because of validation, for example), the response will be a **500 Server Error**, and the response body will include a JSON object with further details.</span></span>

## <a name="example"></a><span data-ttu-id="c08c4-132">Dæmi</span><span class="sxs-lookup"><span data-stu-id="c08c4-132">Example</span></span>

```http
POST https://aos-rts-sf-550e5c091f6-prod-westus2.hr.talent.dynamics.com/namespaces/b2eb8003-334f-4a84-ab63-edbe23569090/data/MyLeaveRequests(RequestId='USMF-000065', LeaveType='Vacation', LeaveDate=2019-10-04T12:00:00Z, dataAreaId='USMF')/Microsoft.Dynamics.DataEntities.submit
```

```json
{
  "error": {
    "code": "",
    "message": "An error has occurred.",
    "innererror": {
      "message": "Exception occurred while executing action submit on Entity MyLeaveRequest: The request would put the 'Vacation' balance below the allowed minimum balance on 9/10/2019.",
      "type": "System.InvalidOperationException",
      "stacktrace": "   at Microsoft.Dynamics.Platform.Integration.Services.OData.Action.ActionInvokable.Invoke()   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.UpdateProcessor.ActionInvocation(ChangeOperationContext context, ActionInvokable action)   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.UpdateManager.<>c__DisplayClass13_0.<ScheduleInvokable>b__0(ChangeOperationContext context)   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.ChangeInfo.ExecuteActionsInCompanyContext(IEnumerable`1 actionList, ChangeOperationContext operationContext)\r\n   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.ChangeInfo.ExecuteActions(ChangeOperationContext context)   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.UpdateManager.SaveChanges()   at Microsoft.Dynamics.Platform.Integration.Services.OData.AxODataDelegatingHandler.<SaveChangesAsync>d__3.MoveNext()"
    }
  }
}
```

## <a name="validation-and-error-messages"></a><span data-ttu-id="c08c4-133">Staðfesting og villuboð</span><span class="sxs-lookup"><span data-stu-id="c08c4-133">Validation and error messages</span></span>

<span data-ttu-id="c08c4-134">Sem hluti af símtalinu til að senda inn API, framkvæmir Human Resources löggildingu viðskiptatækni áður en hún er lögð fram, sem tryggir að leyfisbeiðnin sé í réttri stöðu til að skila.</span><span class="sxs-lookup"><span data-stu-id="c08c4-134">As part of the call to the submit API, Human Resources performs business logic validation before submission, which ensures the leave request is in a valid state for submission.</span></span> <span data-ttu-id="c08c4-135">Hugsanleg villuboð sem þú gætir fengið í svari ef staðfestingar mistakast eru:</span><span class="sxs-lookup"><span data-stu-id="c08c4-135">The possible error messages you may receive in the response if validations fail are:</span></span>

 - <span data-ttu-id="c08c4-136">Beiðnin myndi setja stöðuna „{LeaveTypeId}“ undir leyfða lágmarksstöðu á {date}.</span><span class="sxs-lookup"><span data-stu-id="c08c4-136">The request would put the '{LeaveTypeId}' balance below the allowed minimum balance on {date}.</span></span>
 - <span data-ttu-id="c08c4-137">Ekki er hægt að leggja fram beiðni um frí í fullgerðu ástandi.</span><span class="sxs-lookup"><span data-stu-id="c08c4-137">Time off request in Completed state cannot be submitted.</span></span>
 - <span data-ttu-id="c08c4-138">Ekki er hægt að senda eða vista beiðni þar sem engar breytingar hafa verið gerðar.</span><span class="sxs-lookup"><span data-stu-id="c08c4-138">Unable to submit or save request as no changes have been made.</span></span> <span data-ttu-id="c08c4-139">Bættu við eða uppfærðu upphæðina eða leyfisgerðina og reyndu aftur.</span><span class="sxs-lookup"><span data-stu-id="c08c4-139">Add or update the amount or the leave type and try again.</span></span>
 - <span data-ttu-id="c08c4-140">Tímalengd beiðni sem er slegin inn inniheldur einn eða fleiri daga með sama dagsetningu og leyfi gerð sem fyrirliggjandi biðbeiðni.</span><span class="sxs-lookup"><span data-stu-id="c08c4-140">The time off request entered contains one or more days with the same date and leave type as an existing pending request.</span></span> <span data-ttu-id="c08c4-141">Mundu að fyrirliggjandi beiðni um að gera breytingar.</span><span class="sxs-lookup"><span data-stu-id="c08c4-141">Please recall the existing request to make changes.</span></span>
 - <span data-ttu-id="c08c4-142">Ástæðukóði „{ReasonCodeId}“ á ekki við um leyfisgerðirnar í beiðninni.</span><span class="sxs-lookup"><span data-stu-id="c08c4-142">Reason code '{ReasonCodeId}' doesn't apply to any of the leave types in the request.</span></span>
 - <span data-ttu-id="c08c4-143">Skildu eftir tegund „{LeaveTypeId}” krefst ástæðukóða.</span><span class="sxs-lookup"><span data-stu-id="c08c4-143">Leave type '{LeaveTypeId}' requires a reason code.</span></span> <span data-ttu-id="c08c4-144">Veldu viðeigandi gerð og ástæðukóða.</span><span class="sxs-lookup"><span data-stu-id="c08c4-144">Select the appropriate type and reason code.</span></span>
 - <span data-ttu-id="c08c4-145">Ekki tókst að senda frí.</span><span class="sxs-lookup"><span data-stu-id="c08c4-145">The time off was not submitted successfully.</span></span> <span data-ttu-id="c08c4-146">Fríið hefur verið vistað sem drög að beiðni.</span><span class="sxs-lookup"><span data-stu-id="c08c4-146">The time off has been saved as a draft request.</span></span>

## <a name="see-also"></a><span data-ttu-id="c08c4-147">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="c08c4-147">See also</span></span>

- [<span data-ttu-id="c08c4-148">Yfirlit MyLeaveRequests</span><span class="sxs-lookup"><span data-stu-id="c08c4-148">MyLeaveRequests overview</span></span>](hr-developer-api-myleaverequests-overview.md)
- [<span data-ttu-id="c08c4-149">Sannvottun</span><span class="sxs-lookup"><span data-stu-id="c08c4-149">Authentication</span></span>](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]