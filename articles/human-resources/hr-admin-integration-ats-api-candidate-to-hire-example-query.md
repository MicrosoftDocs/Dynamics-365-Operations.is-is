---
title: Dæmi um fyrirspurn fyrir umsækjanda til ráðningar
description: Í þessu efnisatriði er að finna einingu fyrir dæmi um fyrirspurn fyrir umsækjanda til ráðningar í Dynamics 365 Human Resources.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: efec8c0a8eb75f818acd4ed02632f1db96719d81
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054717"
---
# <a name="example-query-for-candidate-to-hire"></a><span data-ttu-id="bb22a-103">Dæmi um fyrirspurn fyrir umsækjanda til ráðningar</span><span class="sxs-lookup"><span data-stu-id="bb22a-103">Example query for Candidate to hire</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="bb22a-104">Í þessu efnisatriði er að finna einingu fyrir dæmi um fyrirspurn fyrir umsækjanda til ráðningar í Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="bb22a-104">This topic provides an example query for the Candidate to hire entity in Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="bb22a-105">Í þessu efnisatriði er að finna dæmi um hvernig hægt er nota *djúpa innslætti* til að búa til allar upplýsingar um færslu nýs umsækjanda í einni API-aðgerð.</span><span class="sxs-lookup"><span data-stu-id="bb22a-105">This topic provides an example demonstrating how you can use *deep inserts* to create all the detail of a new candidate record in a single API operation.</span></span> <span data-ttu-id="bb22a-106">Frekari upplýsingar um djúpa innslætti er að finna í [Stofna tengdar einingafærslur í einni aðgerð](/powerapps/developer/data-platform/webapi/create-entity-web-api#create-related-entity-records-in-one-operation).</span><span class="sxs-lookup"><span data-stu-id="bb22a-106">For more information about deep inserts, see [Create related entity records in one operation](/powerapps/developer/data-platform/webapi/create-entity-web-api#create-related-entity-records-in-one-operation).</span></span>

<span data-ttu-id="bb22a-107">Einingin **mshr_hcmcandidatetohireentity** er einkvæm vegna tengsla hennar við eininguna **mshr_dirpersonentity**.</span><span class="sxs-lookup"><span data-stu-id="bb22a-107">The **mshr_hcmcandidatetohireentity** entity is unique because of its relationship to the **mshr_dirpersonentity** entity.</span></span> <span data-ttu-id="bb22a-108">Margir eiginleikarnir í **mshr_hcmcandidatetohireentity** (t.d. **mshr_firstname**, **mshr_lastname** og **mshr_birthdate**) eru fengnir frá færslunni **mshr_dirpersonentity**.</span><span class="sxs-lookup"><span data-stu-id="bb22a-108">Many of the properties on the **mshr_hcmcandidatetohireentity** (for example, **mshr_firstname**, **mshr_lastname**, and **mshr_birthdate**) are derived from the **mshr_dirpersonentity** record.</span></span> <span data-ttu-id="bb22a-109">Ef færsla nýs umsækjanda er bókuð í **mshr_hcmcandidatetohireentity** án þess að nota djúpan innslátt, er hægt að skilgreina gildi fyrir þessa eiginleika beint í færsluna **mshr_hcmcandidatetohireentity**.</span><span class="sxs-lookup"><span data-stu-id="bb22a-109">If you post a new candidate record to **mshr_hcmcandidatetohireentity** without using deep inserts, you can define values for these properties directly on the **mshr_hcmcandidatetohireentity** record.</span></span> <span data-ttu-id="bb22a-110">Tengda færslan **mshr_dirpersonentity** er stofnuð á óbeinan hátt með skilgreindu gildunum fyrir eiginleikana.</span><span class="sxs-lookup"><span data-stu-id="bb22a-110">The associated **mshr_dirpersonentity** record is created implicitly with the defined values for the properties.</span></span> <span data-ttu-id="bb22a-111">Síðan er hægt að stofna aðrar tengdar einingafærslur (svo sem hæfni eða menntun) sem aðskilin API-köll.</span><span class="sxs-lookup"><span data-stu-id="bb22a-111">You can then create any other related entity records (such as skills or education) as separate API calls.</span></span>

<span data-ttu-id="bb22a-112">Ef á hins vegar að nota djúpa innslætti til að stofna allar tengdar einingar í einni aðgerð þarf að skilgreina eiginleikana sem tengjast einingunni **mshr_dirpersonentity** á því faldaða stigi aðgerðarinnar.</span><span class="sxs-lookup"><span data-stu-id="bb22a-112">If, however, you want to use deep inserts to create all related entities in one operation, the properties specific to the **mshr_dirpersonentity** entity must be defined on that nested level of the operation.</span></span>

<span data-ttu-id="bb22a-113">Þetta dæmi sýnir hvernig hægt er að stofna færslu umsækjanda, tengda einstaklingsfærslu og hæfni og menntun einstaklingsins á þremur földuðum stigum með djúpum innsláttum í einni API-aðgerð.</span><span class="sxs-lookup"><span data-stu-id="bb22a-113">This example shows how you can create a candidate record, the associated person record, and the person's skills and education in three nested levels using deep inserts in a single API operation.</span></span>

> [!NOTE]
> <span data-ttu-id="bb22a-114">Dæmið felur ekki sér alla eiginleika hverrar API-einingar.</span><span class="sxs-lookup"><span data-stu-id="bb22a-114">The example does not include all properties of each of the API entities.</span></span> <span data-ttu-id="bb22a-115">Það er einfaldað fyrir sýnikennslu.</span><span class="sxs-lookup"><span data-stu-id="bb22a-115">It is simplified for demonstration purposes.</span></span>

<span data-ttu-id="bb22a-116">**Beiðni**</span><span class="sxs-lookup"><span data-stu-id="bb22a-116">**Request**</span></span>

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

<span data-ttu-id="bb22a-117">**Svar**</span><span class="sxs-lookup"><span data-stu-id="bb22a-117">**Response**</span></span>

```http

HTTP/1/1 204 No Content
OData-Version: 4.0
OData-EntityId: [Organization URI]/api/data/v9.1/mshr_hcmcandidatetohireentities(00000d2d-0000-0000-7317-005001000000)

```

## <a name="see-also"></a><span data-ttu-id="bb22a-118">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="bb22a-118">See also</span></span>

[<span data-ttu-id="bb22a-119">Leiðbeiningar um API-samþættingu á rakningakerfi umsækjanda</span><span class="sxs-lookup"><span data-stu-id="bb22a-119">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>


[!INCLUDE[footer-include](../includes/footer-banner.md)]