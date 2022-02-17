---
title: Senda leyfisbeiðni í verkflæði
description: Í Microsoft Dynamics 365 Human Resources, þú getur notað MyLeaveRequests senda () forritunarviðmót forritsins (API) til að leggja fram leyfisbeiðni til verkflæðis.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f9ca716f37b90e22983b2dddc2c426a2b4e251ec
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 01/31/2022
ms.locfileid: "8067505"
---
# <a name="submit-a-leave-request-to-workflow"></a>Senda leyfisbeiðni í verkflæði


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Í Microsoft Dynamics 365 Human Resources, þú getur notað MyLeaveRequests senda () forritunarviðmót forritsins (API) til að leggja fram leyfisbeiðni til verkflæðis. Þetta API birtist sem aðgerð á MyLeaveRequests OData einingunni.

## <a name="prerequisites"></a>Forkröfur

Leyfisbeiðnin verður að vera vistuð í gagnagrunninum og verður að endurheimta í gegnum MyLeaveRequests eininguna.

## <a name="permissions"></a>Aðgangsheimildir

Ein af eftirfarandi heimildum er nauðsynleg til að kalla þetta API. Frekari upplýsingar um heimildir og hvernig skuli velja þær er að finna í [Sannvottun](hr-developer-api-authentication.md).

| Gerð heimildar                    | Heimildir (frá minnst forréttinda til allra forréttinda) |
|------------------------------------|--------------------------------------------------------|
| Úthlutað (vinnu- eða skólareikningur) | user\_impersonation                                    |

## <a name="https-request"></a>HTTPS beiðni

<!-- { "blockType": "ignored" } -->
```HTTP
POST https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/MyLeaveRequests(RequestId='{requestId}', LeaveType='{leaveType}', LeaveDate={leaveDate}, dataAreaId={dataArea})/Microsoft.Dynamics.DataEntities.submit?cross-company=true
```

Beiðnin er í samræmi við OData staðla. Færibreyturnar {requestId}, {leaveType}, {leaveDate} og {dataArea} vísa til reitanna sem samanstanda af samsettum náttúrulykli fyrir MyLeaveRequests eininguna.

> [!NOTE]
> Þó að reitirnir fyrir MyLeaveRequests einingina vísa til einstakrar línu í leyfisbeiðninni, mun hringja í senda API senda alla leyfisbeiðnina (allar línur) til verkflæðis.

### <a name="request-headers"></a>Haus beiðni

| Haus         | Value                     |
|----------------|---------------------------|
| Heimildir  | Handhafi {token} (krafist) |
| Efnistegund   | application/json          |

### <a name="request-body"></a>Meginmál beiðni

Ekki leggja fram beiðni aðila um þessa aðferð.

### <a name="response"></a>Svar

Árangursrík svar er alltaf a **204 Ekkert innihald** svar.

Óheimilar gestir munu fá **401 Óleyfilegt** eða **403 Aðgangur bannaður** svar.

Ef uppgjöf tekst ekki (vegna staðfestingar, til dæmis), verður svarið **500 Villa á þjóni**, og svaraðilinn mun innihalda JSON hlut með nánari upplýsingum.

## <a name="example"></a>Dæmi

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

## <a name="validation-and-error-messages"></a>Staðfesting og villuboð

Sem hluti af símtalinu til að senda inn API, framkvæmir Human Resources löggildingu viðskiptatækni áður en hún er lögð fram, sem tryggir að leyfisbeiðnin sé í réttri stöðu til að skila. Hugsanleg villuboð sem þú gætir fengið í svari ef staðfestingar mistakast eru:

 - Beiðnin myndi setja stöðuna „{LeaveTypeId}“ undir leyfða lágmarksstöðu á {date}.
 - Ekki er hægt að leggja fram beiðni um frí í fullgerðu ástandi.
 - Ekki er hægt að senda eða vista beiðni þar sem engar breytingar hafa verið gerðar. Bættu við eða uppfærðu upphæðina eða leyfisgerðina og reyndu aftur.
 - Tímalengd beiðni sem er slegin inn inniheldur einn eða fleiri daga með sama dagsetningu og leyfi gerð sem fyrirliggjandi biðbeiðni. Mundu að fyrirliggjandi beiðni um að gera breytingar.
 - Ástæðukóði „{ReasonCodeId}“ á ekki við um leyfisgerðirnar í beiðninni.
 - Skildu eftir tegund „{LeaveTypeId}” krefst ástæðukóða. Veldu viðeigandi gerð og ástæðukóða.
 - Ekki tókst að senda frí. Fríið hefur verið vistað sem drög að beiðni.

## <a name="see-also"></a>Sjá einnig

- [Yfirlit MyLeaveRequests](hr-developer-api-myleaverequests-overview.md)
- [Sannvottun](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
