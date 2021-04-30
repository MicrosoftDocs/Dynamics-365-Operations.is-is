---
title: Dæmi um fyrirspurn fyrir umsækjanda til ráðningar
description: Í þessu efnisatriði er að finna einingu fyrir dæmi um fyrirspurn fyrir umsækjanda til ráðningar í Dynamics 365 Human Resources.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a8c3655e7ff609eedbf92fa90a36b65002f40306
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893473"
---
# <a name="example-query-for-candidate-to-hire"></a>Dæmi um fyrirspurn fyrir umsækjanda til ráðningar

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Í þessu efnisatriði er að finna einingu fyrir dæmi um fyrirspurn fyrir umsækjanda til ráðningar í Dynamics 365 Human Resources.

Í þessu efnisatriði er að finna dæmi um hvernig hægt er nota *djúpa innslætti* til að búa til allar upplýsingar um færslu nýs umsækjanda í einni API-aðgerð. Frekari upplýsingar um djúpa innslætti er að finna í [Stofna tengdar einingafærslur í einni aðgerð](/powerapps/developer/data-platform/webapi/create-entity-web-api#create-related-entity-records-in-one-operation).

Einingin **mshr_hcmcandidatetohireentity** er einkvæm vegna tengsla hennar við eininguna **mshr_dirpersonentity**. Margir eiginleikarnir í **mshr_hcmcandidatetohireentity** (t.d. **mshr_firstname**, **mshr_lastname** og **mshr_birthdate**) eru fengnir frá færslunni **mshr_dirpersonentity**. Ef færsla nýs umsækjanda er bókuð í **mshr_hcmcandidatetohireentity** án þess að nota djúpan innslátt, er hægt að skilgreina gildi fyrir þessa eiginleika beint í færsluna **mshr_hcmcandidatetohireentity**. Tengda færslan **mshr_dirpersonentity** er stofnuð á óbeinan hátt með skilgreindu gildunum fyrir eiginleikana. Síðan er hægt að stofna aðrar tengdar einingafærslur (svo sem hæfni eða menntun) sem aðskilin API-köll.

Ef á hins vegar að nota djúpa innslætti til að stofna allar tengdar einingar í einni aðgerð þarf að skilgreina eiginleikana sem tengjast einingunni **mshr_dirpersonentity** á því faldaða stigi aðgerðarinnar.

Þetta dæmi sýnir hvernig hægt er að stofna færslu umsækjanda, tengda einstaklingsfærslu og hæfni og menntun einstaklingsins á þremur földuðum stigum með djúpum innsláttum í einni API-aðgerð.

> [!NOTE]
> Dæmið felur ekki sér alla eiginleika hverrar API-einingar. Það er einfaldað fyrir sýnikennslu.

**Beiðni**

```http

POST [Organization URI]/api/data/v9.1/mshr_hcmcandidatetohireentities
Content-Type: application/json; charset=utf-8
OData-MaxVersion: 4.0
OData-Version: 4.0
Accept: application/json

{
    "mshr_dataareaid": "usmf",
    "mshr_recruitingrequestid": "USMF-000141",
    "mshr_positionid": "000601",
    "mshr_iswillingtorelocate": 200000000,
    "mshr_availabilitydate": "2021-03-18",
    "mshr_comments": "Evelyn's experience is exactly what we need for this position.",
    "mshr_FK_Person_id":
        {
            "mshr_firstname": "Evelyn",
            "mshr_lastname": "Chambers",
            "mshr_namesequencedisplayas": "FirstMiddleLast",
            "mshr_FK_HcmPersonSkillEntity_Person":
            [
                {
                    "mshr_skillid": "CustFocus",
                    "mshr_ratingid": "Skills",
                    "mshr_levelid": "4",
                    "mshr_ratinglevelexaminer": "",
                    "mshr_leveltype": 200000000,
                    "mshr_yearsofexperience": 0,
                    "mshr_verified": 200000000,
                    "mshr_leveldate": "2013-01-01T00:00:00Z"
                },
                {
                    "mshr_skillid": "CashFlow",
                    "mshr_ratingid": "Skills",
                    "mshr_levelid": "4",
                    "mshr_ratinglevelexaminer": "",
                    "mshr_leveltype": 200000000,
                    "mshr_yearsofexperience": 0,
                    "mshr_verified": 200000000,
                    "mshr_leveldate": "2013-01-01T00:00:00Z"
                }
            ],
            "mshr_FK_HcmPersonEducationEntity_Person": [
                {
                    "mshr_creditbasis": 200000000,
                    "mshr_enddate": "2021-02-22T00:00:00Z",
                    "mshr_educationlevelid": "Bachelor",
                    "mshr_creditsearned": 0,
                    "mshr_startdate": "2017-02-21T00:00:00Z",
                    "mshr_creditscompleted": 0,
                    "mshr_educationinstitutionid": "Cottonwood Univ",
                    "mshr_educationdisciplineid": "Business Mgmt",
                    "mshr_durationunit": 200000000
                }              
            ]
        }
}
```

**Svar**

```http

HTTP/1/1 204 No Content
OData-Version: 4.0
OData-EntityId: [Organization URI]/api/data/v9.1/mshr_hcmcandidatetohireentities(00000d2d-0000-0000-7317-005001000000)

```

## <a name="see-also"></a>Sjá einnig

[Leiðbeiningar um API-samþættingu á rakningakerfi umsækjanda](hr-admin-integration-ats-api-introduction.md)<br>


[!INCLUDE[footer-include](../includes/footer-banner.md)]