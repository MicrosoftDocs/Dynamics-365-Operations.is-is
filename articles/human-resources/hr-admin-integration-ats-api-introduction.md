---
title: Leiðbeiningar um API-samþættingu á rakningakerfi umsækjanda
description: Í þessu efnisatriði er API-samþættingu Dynamics 365 Human Resources rakningakerfis umsækjanda (ATS) lýst.
author: andreabichsel
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5038a1a1b3fa4c32f54ea87b03f886504e0b004f
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/06/2021
ms.locfileid: "6357389"
---
# <a name="applicant-tracking-system-integration-api-introduction"></a>Leiðbeiningar um API-samþættingu á rakningakerfi umsækjanda

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Í þessu efnisatriði er API-samþættingu Dynamics 365 Human Resources rakningakerfis umsækjanda (ATS) lýst. Ætlun API er að virkja einfalda samþættingu milli Dynamics 365 Human Resources og ATS samstarfsaðila.

![Samþættingarferli ATS.](media/hr-admin-integration-ats-api-introduction-flow.png)

Samþætta upplifunin hefst í Human Resources þegar ráðningarstjóri stofnar ráðningarbeiðni. Þegar beiðnin er virkjuð sækir ATS upplýsingar um beiðnina til að búa til ráðningarverk. Síðan fylgir það ráðningarlínunni til að velja og ráða umsækjanda fyrir stöðuna/stöðurnar. Að lokum lýkur ATS samþættingarferlinu með því að senda valda færslu umsækjanda inn í Human Resources. Færsla umsækjanda getur þá farið í gegnum fleiri villuleitir innleiðingar og verkferla til að búa til starfsmannsfærsluna.

Til að virkja samþættinguna hefur Human Resources bætt við eftirfarandi hlutum:

1.  Virkni til að stofna ráðningarbeiðni.
2.  Útvíkkaðar notandaupplýsingar umsækjanda og tengdir verkferlar.
3.  API-samþætting sem opnar nýju virknina til að samþætta forrit.

Frekari upplýsingar um uppsetningu og notkun ráðningarbeiðni og virkni umsækjanda er að finna í [Ráða umsækjendur](hr-personnel-recruit.md).

## <a name="microsoft-dataverse"></a>Microsoft Dataverse

Þetta API er byggt á Microsoft Dataverse (áður Common Data Service). Öll RESTful-samþætting við þetta API er gert í gegnum Microsoft Dataverse vef-API sem notar OData. Þetta API er undirsafn Dataverse vef-API. Dataverse Vef-API skilgreinir einkenni á borð við auðkenningu, þjónustustigssamninga, runu, samvinnslustýringu og villumeðhöndlun.

Til að fá frekari almennar upplýsingar um Microsoft Dataverse vef-API skal sjá:

- [Hvað er Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)
- [Nota Microsoft Dataverse vef-API](/powerapps/developer/data-platform/webapi/overview)
- [Microsoft Dataverse leiðbeiningar þróunaraðila](/powerapps/developer/data-platform)

Ofangreind fylgigögn innihalda upplýsingar og leiðbeiningar þróunaraðila um notkun á Dataverse vef-API, svo sem [stjórnun sannvottunar](/powerapps/developer/data-platform/webapi/authenticate-web-api), [framkvæmd aðgerða](/powerapps/developer/data-platform/webapi/perform-operations-web-api), [notkun Postman með API](/powerapps/developer/data-platform/webapi/use-postman-web-api) og [notkun breytingarrakningar eða Delta-tákns](/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems) með API.

### <a name="option-sets"></a>Safn valkosta

Gagnalíkanið fyrir API-samþættingu ATS sem lýst er í þessu skjali inniheldur safn valkosta sem bjóða upp á númeruð gildi sem tengjast eiginleikum einingar. Frekari upplýsingar um hvernig nota skuli safn valkosta í Dataverse vef-API er að finna í [Búa til og uppfæra safn valkosta með vef-API](/powerapps/developer/data-platform/webapi/create-update-optionsets). Safn valkosta er skilgreint fyrir hvert Dataverse-umhverfi.

### <a name="virtual-tables-for-human-resources-in-dataverse"></a>Sýndartöflur fyrir Human Resources í Dataverse

Endastöðvar fyrir API-Samþætting ATS nota verkvangsmöguleika sýndartöflunnnar fyrir Microsoft Dataverse. Sjálfgefið er að sýndartöflurnar og tengdu API-endastöðvarnar þeirra eru ekki uppsettar fyrir umhverfi Human Resources sem gerir fyrirtækjum kleift að ákveða hvaða OData-endastöðvar verða notaðar í umhverfinu. Til að nota API þarf að mynda sýndartöflur fyrir einingar Human Resources fyrir umhverfið. 

Frekari upplýsingar um myndun sýndartaflna fyrir API er að finna í [Skilgreina Dataverse sýndartöflur](./hr-admin-integration-common-data-service-virtual-entities.md).

## <a name="data-model"></a>Gagnalíkan

Gagnalíkanið miðast við tvær aðaleiningar:

- **RecruitingRequest** stendur fyrir beiðni til ATS um að ráða í eina eða fleiri lausar stöður. Dæmi um fyrirspurn er að finna í [Dæmi um fyrirspurn fyrir ráðningarbeiðni](hr-admin-integration-ats-api-recruiting-request-example-query.md).
- **CandidateToHire** sýnir upplýsingar um umsækjanda sem hefur samþykkt boð um stöðu. **Einstaklingur** stendur fyrir einstaklinginn sem er umsækjandinn. Einstaklingur getur haft mörg hlutverk í fyrirtækinu, t.d. umsækjandi, starfskraftur, starfsmaður eða verktaki. Dæmi um fyrirspurn er að finna í [Dæmi um fyrirspurn fyrir umsækjanda til ráðningar](hr-admin-integration-ats-api-candidate-to-hire-example-query.md).

Eftirfarandi skýringarmynd sýnir vensl innan API. Nokkrar gerðir eru með ytri lykla fyrir aðrar fyrirliggjandi einingar í Human Resources sem ekki eru sýndar hér. Í þessu skjali eru upplýsingar um einingar sem eiga sérstaklega við samþættingaraðstæður ráðningar. Hins vegar eru margar aðrar einingar í Dataverse vef-API fyrir Dynamics 365 Human Resources sem kunna einnig að skipta máli fyrir samþættingu þína. Til dæmis gæti einnig þurft upplýsingar fyrir starfsmenn, störf, stöður eða aðrar einingar sem ekki eru skilgreindar hér. Vísað er í margar þessara eininga í tengslum ytri lykla eða skoðunareiginleikum.

![Gagnalíkan API-samþættingar ATS.](media/hr-admin-integration-ats-api-data-model.png)

## <a name="recruiting-request-and-related-entities-and-option-sets"></a>Ráðningarbeiðni og tengdar einingar og söfn valkosta

Dæmi um fyrirspurn: 

- [Dæmi um fyrirspurn fyrir ráðningarbeiðni](hr-admin-integration-ats-api-recruiting-request-example-query.md)

Einingar:

- [Ráðningarbeiðni](hr-admin-integration-ats-api-recruiting-request.md)
- [Staða í ráðningarbeiðni](hr-admin-integration-ats-api-recruiting-request-position.md)
- [Færni í ráðningarbeiðni](hr-admin-integration-ats-api-recruiting-request-skill.md)
- [Menntun í ráðningarbeiðni](hr-admin-integration-ats-api-recruiting-request-education.md)
- [Staðsetning í ráðningarbeiðni](hr-admin-integration-ats-api-recruiting-request-location.md)

Safn valkosta:

- [Undanþágustaða starfs](hr-admin-integration-ats-api-job-exempt-status.md)
- [Staða starfs í ráðningarbeiðni](hr-admin-integration-ats-api-recruiting-request-position-status.md)
- [Staða í ráðningarbeiðni](hr-admin-integration-ats-api-recruiting-request-status.md)
- [Flokkur stjórnunarstarfs](hr-admin-integration-ats-api-regulatory-job-category.md)

## <a name="candidate-to-hire-and-related-entities-and-option-sets"></a>Umsækjendur til að ráða og tengdar einingar og söfn valkosta

Dæmi um fyrirspurn:

- [Dæmi um fyrirspurn fyrir umsækjanda til ráðningar](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

Einingar:

- [Umsækjandi til að ráða](hr-admin-integration-ats-api-candidate-to-hire.md)
- [Einstaklingur](hr-admin-integration-ats-api-person.md)
- [Menntun einstaklings](hr-admin-integration-ats-api-person-education.md)
- [Starfsreynsla einstaklings](hr-admin-integration-ats-api-person-professional-experience.md)
- [Aðsetur einstaklings](hr-admin-integration-ats-api-person-address.md)
- [Tengiliður aðila](hr-admin-integration-ats-api-party-contact.md)
- [Hæfni einstaklings](hr-admin-integration-ats-api-person-skill.md)
- [Matsstig](hr-admin-integration-ats-api-rating-level.md)
- [Skírteini einstaklings](hr-admin-integration-ats-api-person-certificate.md)
- [Gerð skírteinis](hr-admin-integration-ats-api-certificate-type.md)
- [Skoðun einstaklings](hr-admin-integration-ats-api-person-screening.md)
- [Skoðunargerðir](hr-admin-integration-ats-api-screening-types.md)
- [Kennitala einstaklings](hr-admin-integration-ats-api-person-identification-number.md)

Safn valkosta:

- [Niðurstöður samþættingar umsækjanda](hr-admin-integration-ats-api-applicant-integration-result.md)
- [Autt Já Nei](hr-admin-integration-ats-api-blank-yes-no.md)
- [Staða á lokið](hr-admin-integration-ats-api-completion-status.md)
- [Gerð tengiliðar](hr-admin-integration-ats-api-contact-type.md)
- [Einingagrunnur menntunar](hr-admin-integration-ats-api-education-credit-basis.md)
- [Kyn](hr-admin-integration-ats-api-gender.md)
- [Hjúskaparstaða](hr-admin-integration-ats-api-marital-status.md)
- [Mánuðir árs](hr-admin-integration-ats-api-months-of-year.md)
- [Nei Já](hr-admin-integration-ats-api-no-yes.md)
- [Tímabilseining](hr-admin-integration-ats-api-period-unit.md)
- [Tíðni skoðunar](hr-admin-integration-ats-api-screening-frequency.md)
- [Tíðni skoðunar mynduð úr](hr-admin-integration-ats-api-screening-frequency-generate-from.md)
- [Gerð hæfnisstig](hr-admin-integration-ats-api-skill-level-type.md)

## <a name="see-also"></a>Sjá einnig

[Ráða umsækjendur](hr-personnel-recruit.md)<br>
[Hvað er Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)<br>
[Nota Microsoft Dataverse vef-API](/powerapps/developer/data-platform/webapi/overview)<br>
[Búa til og uppfæra söfn valkosta með vef-API](/powerapps/developer/data-platform/webapi/create-update-optionsets)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]