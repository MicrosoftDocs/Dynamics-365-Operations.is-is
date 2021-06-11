---
title: Umsækjandi til að ráða
description: Þetta efnisatriði lýsir einingu fyrir ráðningu umsækjanda fyrir Dynamics 365 Human Resources.
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
ms.openlocfilehash: 6464a8a5531c7559480a2628829a230e5adce94b
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054669"
---
# <a name="candidate-to-hire"></a>Umsækjandi til að ráða

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Þetta efnisatriði lýsir einingu fyrir ráðningu umsækjanda fyrir Dynamics 365 Human Resources.

Raunlægt heiti: mshr_hcmcandidatetohireentity

## <a name="description"></a>lýsing

Þessi eining býður upp á upplýsingar um umsækjanda sem notaðar eru til að stofna starfsmann í Dynamics 365 Human Resources. Hún er notuð til að lesa allar færslur umsækjanda og búa til innri og ytri færslur umsækjanda sem gerir þér kleift að búa til persónulegar upplýsingar fyrir nýja umsækjandann.

Þegar búin er til ytri færsla umsækjanda sem verður ný einstaklingsfærsla í kerfinu má ekki skilgreina númer aðila (einstaklings) heldur birtir þú nýja færslu umsækjanda. Nýja einingarfærsla einstaklingsins er búin til með nýju umsækjandafærslunni.

Þegar innri umsækjandafærsla er búin til (umsækjandi fyrir stöðu sem er þegar með starfsmannafærslu hjá fyrirtækinu) skal skilgreina aðila (einstakling) færslunnar sem er þegar til fyrir einstakling eiginleikans mshr_partynumber í umsækjandafærslunni frekar en að skilgreina persónulegar upplýsingar (t.d. nafn, kyn eða fæðingardag) sem yrðu notaðar til að búa til nýja færslu einstaklingsins.

## <a name="json-representation"></a>JSON-framsetning

```json
        {
            "mshr_candidateid": "String",
            "mshr_partynumber": "String",
            "mshr_partytype": "String",
            "mshr_recruitingrequestid": "String",
            "mshr_positionid": "String",
            "mshr_firstname": "String",
            "mshr_middlename": "String",
            "mshr_lastnameprefix": "String",
            "mshr_lastname": "String",
            "mshr_gender": Int,
            "mshr_birthdate": "Date",
            "mshr_citizenshipcountrycode": "String",
            "mshr_veteranstatusid": "String",
            "mshr_isdisabledveteran": Int,
            "mshr_availabilitydate": "Date",
            "mshr_iswillingtorelocate": Int,
            "mshr_comments": "String",
            "mshr_applicantintegrationresult": Int,
            "mshr_donothirereasoncodeid": "String",
            "mshr_dataareaid": "String",
            "_mshr_dataareaid_id_value": "Guid",
            "_mshr_fk_person_id_value": "Guid",
            "_mshr_fk_recruitingrequest_id_value": "Guid",
            "_mshr_fk_position_id_value": "Guid",
            "mshr_hcmcandidatetohireentityid": "Guid",
            "_mshr_fk_veteranstatus_id_value": "Guid",
            "_mshr_fk_reasoncode_id_value": "Guid",
            "mshr_militaryserviceenddate": "Guid",
            "mshr_militaryservicestartdate": "Guid"
        }
```

## <a name="properties"></a>Eiginleikar

| Eiginleiki<br>**Efnislegt heiti**<br>**_Gerð_** | Nota | lýsing |
| --- | --- | --- |
| **Einingarkenni fyrir ráðningu umsækjanda**<br>mshr_hcmcandidatetohireentityid<br>Guid | Lesa eingöngu<br>Krafa<br>Myndað af kerfinu | Kerfismyndað einkvæmt kenni fyrir færslueininguna. |
| **Kenni umsækjanda**<br>mshr_candidateid<br>Strengur | Lesa eingöngu<br>Krafa<br>Myndað af kerfinu | Einkvæmt kenni fyrir eininguna. |
| **Aðilanúmer**<br>mshr_partynumber<br>Strengur | Lesa eingöngu<br>Krafa | Númer aðila (einstaklings) fyrir einstaklingsfærslu umsækjanda. |
| **Gildi fyrir auðkenni einstaklings**<br>_mshr_fk_person_id_value<br>Guid | Lesa eingöngu<br>Krafa<br>Ytri lykill: mshr_dirpersonentityid of mshr_direpersonentity | Kerfið myndaði einkvæmt kenni fyrir færslu aðilans (einstaklingsins) fyrir umsækjandann. |
| **Gerð aðila**<br>mshr_partytype<br>Valkostir mshr_dirpartytype | Lesa eingöngu<br>Krafa | Aðilagerð færslunnar eins og hún er skilgreind í valkostum mshr_dirpartytype. Fyrir þessa einingu verður gerðin alltaf „Einstaklingur“. |
| **Kenni ráðningarbeiðni**<br>mshr_recruitingrequestid<br>Strengur | Skrifa einu sinni<br>Valfrjálst | Vísar í ráðningarbeiðni sem þessi umsækjandi uppfyllir. |
| **Gildi fyrir kenni ráðningarbeiðni**<br>_mshr_fk_recruitingrequest_id_value<br>Guid | Lesa/skrifa<br>Valfrjálst<br>Framandlykill: mshr_hcmrecruitingrequestentityid of mshr_hcmrecruitingrequestentity | Kerfismyndað einkvæmt kenni ráðningarbeiðninnar sem umsækjandinn uppfyllir. |
| **Auðkenni stöðuheitis**<br>mshr_positionid<br>Strengur | Lesa/skrifa<br>Valfrjálst | Auðkenni stöðunnar sem umsækjandi er hugsaður fyrir. |
| **Gildi fyrir staðsetningarkenni**<br>_mshr_fk_position_if_value<br>Guid | Lesa eingöngu<br>Valfrjálst<br>Ytri lykill: mshr_hcmpositionv2entityid of mshr_hcmpositionv2entity | Kerfismyndað kenni stöðunnar sem umsækjandi er hugsaður fyrir. |
| **Fornafn**<br>mshr_firstname<br>Strengur | Lesa/skrifa<br>Krafa | Fornafn umsækjanda. |
| **Millinafn**<br>mshr_middlename<br>Strengur | Lesa/skrifa<br>Valfrjálst | Millinafn umsækjanda. |
| **Forskeyti eftirnafns**<br>mshr_lastnameprefix<br>Strengur | Lesa/skrifa<br>Valfrjálst | Forskeyti eftirnafns umsækjanda. |
| **Eftirnafn**<br>mshr_lastname<br>Strengur | Lesa/skrifa<br>Valfrjálst | Eftirnafn umsækjanda. |
| **Kyn**<br>mshr_gender<br>Valkostir mshr_hcmpersongender | Lesa/skrifa<br>Valfrjálst | Kyn umsækjanda. |
| **Fæðingardagur**<br>mshr_birthdate<br>Datetime | Lesa/skrifa<br>Valfrjálst | Fæðingardagur umsækjanda. |
| **Landskóði ríkisfangs**<br>mshr_citizenshipcountrycode<br>Strengur | Lesa/skrifa<br>Valfrjálst | Tilgreinir landið þar sem umsækjandi er með ríkisborgararétt. Gildir landskóðar eru í mshr_logisticaddresscountryregionentity. |
| **Stöðukenni uppgjafahermanns**<br>mshr_veteranstatusid<br>Strengur | Lesa/skrifa<br>Valfrjálst | Sýnir stöðu uppgjafahermanns fyrir umsækjanda. |
| **Gildi fyrir stöðukenni uppgjafahermanns**<br>_mshr_fk_veteranstatus_id_value<br>Guid | Lesa eingöngu<br>Valfrjálst<br>Ytri lykill: mshr_hcmveteranstatusentityid of mshr_hcmveteranstatusentity | Kerfismyndað einkvæmt kenni fyrir færslueiningu á stöðu uppgjafahermanns. |
| **Upphafsdagsetning herþjónustu**<br>mshr_militaryservicestartdate<br>Datetime | Lesa/skrifa<br>Valfrjálst | Upphafsdagsetning herþjónustu umsækjanda. |
| **Lokadagsetning herþjónustu**<br>mshr_militaryserviceenddate<br>Datetime | Lesa/skrifa<br>Valfrjálst | Lokadagsetning herþjónustu umsækjanda. |
| **Er fatlaður uppgjafahermaður**<br>mshr_isdisabledveteran<br>Valkostir mshr_noyes | Lesa/skrifa<br>Valfrjálst | Sýnir hvort umsækjandi sé með stöðu fatlaðs uppgjafahermanns. |
| **Tiltækt á dagsetningu**<br>mshr_availabilitydate<br>Datetime | Lesa/skrifa<br>Valfrjálst | Fyrsta dagsetningin sem umsækjandi er tilbúinn til starfa. |
| **Er reiðubúinn til að flytja milli staða**<br>mshr_iswillingtorelocate<br>Valkostir mshr_noyes | Lesa/skrifa<br>Valfrjálst | Sýnir hvort umsækjandinn sé tilbúinn til að flytja milli staða. |
| **Athugasemdir**<br>mshr_comments<br>Strengur | Lesa/skrifa<br>Valfrjálst | Athugasemdir sem ráðningaraðili eða ráðningarstjóri nota. |
| **Niðurstaða samþættingar forrits**<br>mshr_applcantintegrationresult<br>Valkostir mshr_applicantintegrationresult | Lesa/skrifa<br>Krafa | Staða umsækjanda í ráðningarferlinu sem tengist samþættingu. |
| **Ástæðukóði fyrir að ráða ekki**<br>mshr_donothirereasoncodeid<br>Strengur | Lesa/skrifa<br>Valfrjálst | Boðið er valfrjálst upp á ástæðukóða þegar staðan (niðurstaða samþættingar forrits) er stillt á „Ekki ráðin(n)“. |
| **Gildi fyrir auðkenni ástæðukóða**<br>_mshr_fk_reasoncode_id_value<br>Guid | Lesa eingöngu<br>Valfrjálst<br>Ytri lykill: einingin mshr_hcmreasoncodeentityid of mshr_hcmreasoncodeentity | Kerfismyndað einkvæmt kenni fyrir ástæðukóðann **Ekki ráða**. |
| **Kenni gagnasvæðis**<br>mshr_dataareaid<br>Strengur | Lesa/skrifa<br>Valfrjálst |  Tilgreinir lögaðilann (fyrirtækið). |
| **Gildi fyrir kenni gagnasvæðis**<br>_mshr_dataareaid_id_value<br>Guid | Lesa eingöngu<br>Valfrjálst<br>Framandlykill: cdm_companyid of cdm_company entity | Kerfismyndað GUID-gildi sem tilgreinir lögaðilann (fyrirtækið). |

## <a name="see-also"></a>Sjá einnig

[Leiðbeiningar um API-samþættingu á rakningakerfi umsækjanda](hr-admin-integration-ats-api-introduction.md)<br>
[Dæmi um fyrirspurn fyrir umsækjanda til ráðningar](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]