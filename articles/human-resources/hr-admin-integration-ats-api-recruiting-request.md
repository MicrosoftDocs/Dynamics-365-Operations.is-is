---
title: Ráðningarbeiðni
description: Þetta efnisatriði lýsir einingu ráðningarbeiðni fyrir Dynamics 365 Human Resources.
author: jaredha
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 572ee0755e331d19b41442e3614effb92db95a92
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125426"
---
# <a name="recruiting-request"></a>Ráðningarbeiðni

Þetta efnisatriði lýsir einingu ráðningarbeiðni fyrir Dynamics 365 Human Resources.

Raunlægt heiti: mshr_hcmrecruitingrequestentity

### <a name="description"></a>lýsing

Lýsir beiðni til að ráða í starf.

### <a name="json-representation"></a>JSON-framsetning

```json
{
    "mshr_recruitingrequestid": "String",
    "mshr_hiringmanagerpersonnelnumber": "String",
    "mshr_recruiterpartynumber": "String",
    "mshr_status": Int,
    "mshr_description": "String",
    "mshr_recruitingrequestlocationid": "String",
    "mshr_comments": "String",
    "mshr_jobid": "String",
    "mshr_titleid": "String",
    "mshr_jobfunctionid": "String",
    "mshr_defaultfulltimeequivalency": Decimal,
    "mshr_regulatoryjobcategory": Int,
    "mshr_jobtypeid": "String",
    "mshr_exemptstatus": Int,
    "mshr_estimatedstartdate": "Date",
    "mshr_externaldescription": "String",
    "mshr_compensationlevelid": "String",
    "mshr_compensationlowthreshold": Decimal,
    "mshr_compensationcontrolpoint": Decimal,
    "mshr_compensationhighthreshold": Decimal,
    "mshr_dataareaid": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "_mshr_fk_hiringmanager_id_value": "Guid",
    "_mshr_fk_recruiter_id_value": "Guid",
    "_mshr_fk_job_id_value": "Guid",
    "_mshr_fk_title_id_value": "Guid",
    "_mshr_fk_jobtype_id_value": "Guid",
    "_mshr_fk_compensationlevel_id_value": "Guid",
    "mshr_hcmrecruitingrequestentityid": "Guid",
    "_mshr_fk_recruitingrequestlocation_id_value": “Guid”
}
```

### <a name="properties"></a>Eiginleikar

| Eiginleiki<br>**Efnislegt heiti**<br>**_Gerð_** | Nota | lýsing |
| --- | --- | --- |
| **Kenni ráðningarbeiðni**<br>mshr_recruitingrequestid<br>*Strengur* | Lesa eingöngu<br>Krafa<br>Myndað af kerfinu | Einkvæmt lesanlegt kenni fyrir beiðnina sem sést í forriti Human Resources. Númeraröð. |
| **Einingarkenni ráðningarbeiðni**<br>mshr_hcmrecruitingrequestentityid<br>*GUID* | Lesa eingöngu<br>Krafa<br>Myndað af kerfinu | GUID-gildi myndað af kerfinu til að auðkenna ráðningarbeiðni á einkvæman hátt. |
| **Kenni gagnasvæðis**<br>mshr_dataareaid<br>*Strengur* | Lesa/skrifa<br>Valfrjálst<br> | Tilgreinir lögaðilann (fyrirtækið) fyrir ráðningarbeiðnina. |
| **Gildi fyrir kenni gagnasvæðis**<br>_mshr_dataareaid_id_value<br>*GUID*<br> | Lesa eingöngu<br>Valfrjálst<br>Framandlykill: cdm_companyid of cdm_company entity | GUID-gildi myndað af kerfinu sem tilgreinir lögaðilann (fyrirtækið) fyrir ráðningarbeiðnina. |
| **Starfsmannanúmer ráðningarstjóra**<br>mshr_hiringmanagerpersonnelnumber<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Starfsmannanúmer ráðningarstjórans sem tengist þessari ráðningarbeiðni. |
| **Gildi fyrir kenni ráðningarstjóra**<br>_mshr_fk_hiringmanager_id_value<br>*GUID* | Lesa eingöngu<br>Valfrjálst<br>Framandlykill: mshr_hcmworkerbaseentityid of mshr_hcmworkerbaseentity eining | GUID-gildi myndað af kerfinu til að auðkenna yfirmanninn sem tengist ráðningarbeiðninni. |
| **Aðildarnúmer ráðningaraðila**<br>mshr_recruiterpartynumber<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Einstaklingsnúmer (aðilanúmer) ráðningaraðila beiðninnar. |
| **Gildi fyrir kenni ráðningaraðila**<br>_mshr_fk_recruiter_id_value<br>*GUID* | Lesa eingöngu<br>Valfrjálst<br>Ytri lykill: mshr_dirpersonentityid úr einingu mshr_dirpersonentity | GUID-gildi myndað af kerfinu til að auðkenna ráðningaraðilann sem tengist ráðningarbeiðninni. |
| **Staða**<br>mshr_status<br>Valkostir *RecruitingRequestStatus* | Lesa/skrifa<br>Krafa<br> | Tilgreinir stöðu ráðningarbeiðninnar. |
| **Lýsing**<br>mshr_description<br>*Strengur* | Lesa/skrifa<br>Krafa | Lýsir beiðninni. |
| **Kenni staðsetningar í ráðningarbeiðni**<br>mshr_recruitingrequestlocationid<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Einkvæmt lesanlegt kenni fyrir staðsetningu starfs sem tengist þessari beiðni. |
| **Gildi fyrir staðsetningarkenni ráðningar**<br>_mshr_fk_recruitinglocation_id_value<br>*GUID* | Lesa eingöngu<br>Valfrjálst<br>Ytri lykill: mshr_hcmrecruitingrequestlocationentityid úr einingu mshr_hcmrecruitingrequestlocationentity | GUID-gildi myndað af kerfinu til að auðkenna staðsetningu ráðningarbeiðninnar sem valin er fyrir beiðnina. |
| **Athugasemdir**<br>mshr_comments<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Athugasemdir um beiðnina sem ráðningarstjóri og ráðningaraðilar nota. |
| **Starfsauðkenni**<br>mshr_jobid<br>*Strengur* | Einskrifanlegt<br>Krafa |   Einkvæmt lesanlegt kenni starfsins sem allar stöður deila sem tengjast þessari beiðni. |
| **Gildi fyrir starfskenni**<br>_mshr_fk_job_id_value<br>*GUID* | Lesa eingöngu<br>Krafa<br>Ytri lykill: mshr_hcmjobentityid úr einingu mshr_hcmjobentity | Einkvæmt lesanlegt kenni starfsins sem allar stöður deila sem tengjast þessari ráðningarbeiðni. |
| **Kenni titils**<br>mshr_titleid<br>*Strengur* | Lesa eingöngu<br>Krafa | Einkvæmt lesanlegt kenni fyrir starfstitil sem tengist þessari beiðni. |
| **Gildi fyrir kenni titils**<br>_mshr_fk_title_id_value<br>*GUID* | Lesa eingöngu<br>Krafa<br>Ytri lykill: mshr_hcmtitleid úr einingu mshr_hcmtitleentity | Einkvæmt kenni sem kerfið myndar fyrir titil starfsins sem valið er fyrir ráðningarbeiðnina. |
| **Kenni starfssviðs**<br>mshr_jobfunctionid<br>*Strengur* | Lesa eingöngu<br>Krafa<br>Ytri lykill: mshr_jobfunctionid úr einingu mshr_hcmjobfunctionentity | Einkvæmt lesanlegt kenni fyrir starfssviðið sem tengist þessari beiðni. |
| **Sjálfgefið jafngildi fyrir fullt starf**<br>mshr_defaultfulltimeequivalency<br>*Tvöfalt* | Lesa eingöngu<br>Krafa | Jafngildi fulls starfs fyrir starfið þar sem 1,0 táknar starfskraft í fullu starfi. |
| **Starfsflokkur samkvæmt reglum**<br>mshr_regulatoryjobcategory<br>Valkostir *RegulatoryJobCategory* | Lesa eingöngu<br>Valfrjálst | EEO-starfsflokkar fyrir starfssviðið sem valið var fyrir starfið. Gild gildi höfð með í valkostum HcmRegulatoryJobCatetory (mshr_hcmregulatoryjobcategory). |
| **Kenni starfsgerðar**<br>mshr_jobtypeid<br>*Strengur* | Lesa eingöngu<br>Valfrjálst | Gerð starfsins sem tengist stöðunni. Starfsgerðir eru notandaskilgreind gildi, tiltæk í einingunni mshr_hcmjobtypeentity. |
| **Gildi fyrir kenni starfsgerðar**<br>_mshr_fk_jobtype_id_value<br>*GUID* | Lesa eingöngu<br>Valfrjálst<br>Ytri lykill: mshr_hcmjobtypeentityid úr einingu mshr_hcmjobtypenentity | Einkvæmt lesanlegt kenni sem kerfið myndar fyrir starfsgerðina sem tengist starfi ráðningarbeiðninnar. |
| **Undanþágustaða**<br>mshr_exemptstatus<br>Valkostir *JobExemptStatus* | Lesa eingöngu<br>Valfrjálst | FLSA-undanþágustaðan samkvæmt starfsgerðinni. |
| **Áætluð upphafsdagsetning**<br>mshr_estimatedstartdate<br>*Dagsetning* | Lesa/skrifa<br>Krafa | Áætluð dagsetning þegar umsækjandi hefur störf. |
| **Ytri lýsing**<br>mshr_externaldescription<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Lýsing á starfi/stöðu sem snýr að umsækjanda. | Neðra launamark<br>mshr_compensationlowthreshold<br>*Tvöfalt* | Lesa/skrifa<br>Valfrjálst | Neðri mörk launastigsins. |
| **Stýripunktur launa**<br>mshr_compensationcontrolpoint<br>*Tvöfalt* | Lesa/skrifa<br>Valfrjálst | Stýripunktur fyrir launastigið. |
| **Efra launamark**<br>mshr_compensationhighthreshold<br>*Tvöfalt* | Lesa/skrifa<br>Valfrjálst | Efri mörk launastigsins. |
| **Launastig**<br>mshr_compensationlevelid<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Launastig starfsins. Hægt er að setja upp starf með mörgum launastigum. Þessi eigind gefur til kynna valið launastig launa starfs fyrir þessa beiðni. |
| **Kenni launa fyrir vinnu**<br>_mshr_fk_jobcompensation_id_value<br>*GUID* | Lesa eingöngu<br>Valfrjálst<br>Ytri lykill: mshr_hcmjobcompensationentityid úr einingu mshr_hcmjobcompensationentity | Einkvæmt kenni sem kerfið myndar fyrir launastigið sem tengist starfi ráðningarbeiðninnar. |

## <a name="see-also"></a>Sjá einnig

[Leiðbeiningar um API-samþættingu á rakningakerfi umsækjanda](hr-admin-integration-ats-api-introduction.md)<br>
[Dæmi um fyrirspurn fyrir ráðningarbeiðni](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]