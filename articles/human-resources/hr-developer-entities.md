---
title: Dataverse töflur
description: Microsoft Dynamics 365 Human Resources notar Dataverse til að gera mögulegt atburðarás fyrir stækkun og samþættingu.
author: andreabichsel
manager: tfehr
ms.date: 01/25/2021
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
ms.openlocfilehash: 2f075a8e96af55b1363d2d51db377c5b25c38775
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/03/2021
ms.locfileid: "5113002"
---
# <a name="dataverse-tables"></a>Dataverse töflur

Microsoft Dynamics 365 Human Resources notar Dataverse til að gera mögulegt atburðarás fyrir stækkun og samþættingu.

> [!NOTE]
> Mannauðseiningar samsvara Dataverse töflum. Frekari upplýsingar um Dataverse (áður Common Data Service) og uppfærslur á hugtökum er að finna í [Hvað er Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)

Eftirfarandi Dataverse-töflur eru í boði sem byggja á einingum Human Resources.

## <a name="benefit-tables"></a>Fríðindatöflur

| Nafn | Tafla |
| --- | --- |
| Útreikningstíðni fríðinda | cdm_benefitcalculationfrequency |
| Útreikningsíðni fríðinda á launatímabili | cdm_benefitcalculationfrequencypayperiod |
| Hlutfall útreikninga fyrir fríðindi | cdm_benefitcalculationrate |
| Upplýsingar um hlutfall útreikninga fyrir fríðindi | cdm_benefitcalculationratedetail |
| Fríðindavalkostur | cdm_benefitoption |
| Fríðindaáætlun | cdm_benefitplan (Ekki virkjað fyrir sérsniðinn reitastuðning) |
| Gerð fríðinda | cdm_benefittype |

## <a name="business-process-tasks-tables"></a>Verkefnatöflur viðskiptaferlis

| Nafn | Tafla |
| --- | --- |
| Dagatal viðskiptaferlis | cdm_businessprocesscalendar |
| Hópverkefni viðskiptaferlis | cdm_businessprocessgroupassignment |
| Verkhópur viðskiptaferlissafns | cdm_businessprocesslibrarytaskgroup |
| Stig viðskiptaferlis | cdm_businessprocessstage |
| Haus gátlistasniðmáts | cdm_businessprocesstemplateheader |
| Verkefni gátlistasniðmáts | cdm_businessprocesstemplatetask |

## <a name="compensation-tables"></a>Launatöflur

| Nafn | Tafla |
| --- | --- |
| Fyrirkomulag fastra launa | cdm_compensationfixedplan |
| Launanet | cdm_compensationgrid |
| Launastig | cdm_compensationlevel |
| Greiðslutíðni launa | cdm_compensationpayfrequency |
| Uppsetning á tilvísunarpunkti launa | cdm_compensationreferencepointsetup |
| Setja upp línu tilvísunarpunkts launa | cdm_compensationreferencepointsetupline |
| Launasvæði | cdm_compensationregion |
| Launaskipulag | cdm_compensationstructure |
| Fyrirkomulag breytilegra uppbóta | cdm_compensationvariableplan |
| Fyrirkomulagsstig breytilegra uppbóta | cdm_compensationvariableplanlevel |
| Fyrirkomulagsgerð breytilegra uppbóta | cdm_compensationvariableplantype |
| Fast launatilvik | cdm_fixedcompensationevent |
| Veitiregla | cdm_vestingrule |
| Föst laun starfskrafts | cdm_workerfixedcompensation |

## <a name="organization-tables"></a>Fyrirtækistöflur

| Nafn | Tafla |
| --- | --- |
| Deild | cdm_department |
| Ráðning | cdm_employment |
| Fyrirt.   | cdm_company |
| Vinnsla | cdm_job |
| Starfshlutverk | cdm_jobfunction |
| Staða starfs | cdm_jobposition |
| Gerð stöðu | cdm_positiontype |
| Stöðuúthlutun starfskrafts | cdm_positionworkerassignmentmap |
| Vídd stöðu starfs | cdm_jobpositiondimension|
| Starfsgerð | cdm_jobtype |
| Tungumál | cdm_language |
| Titill | cdm_title |

> [!NOTE]
> Fjárhagslegar víddir fyrir **Gerð stöðu**, **Stöðuúthlutun starfskrafts** og **Starf** veita einnar áttar samþættingu við Dataverse. Uppfærslur fjárhagsvídda samstillast ekki eins og stendur úr Dataverse í Human Resources. 

## <a name="leave-and-absence-tables"></a>Leyfis- og fjarvistatöflur

| Nafn | Tafla |
| --- | --- |
| Orlofsbankafærsla | cdm_leavebanktransaction |
| Orlofsskráning | cdm_leaveenrollment |
| Leyfisáætlun | cdm_leaveplan |
| Orlofsbeiðni | cdm_leaverequest |
| Upplýsingar um orlofsbeiðni | cdm_leaverequestdetail |
| Gerð leyfis | cdm_leavetype |
| Ástæðukóði orlofsgerðar | cdm_leavetypereasoncode |

## <a name="payroll-tables"></a>Töflur launaskráar

| Nafn | Tafla |
| --- | --- |
| Greiðsluferli | cdm_paycycle |
| Launatímabil | cdm_payperiod |
| Tekjukóði launa | cdm_payrollearningcode |
| Bankareikningsgreiðslur | cdm_bankaccountdisbursement |
| Skattumdæmi | cdm_taxregion |

## <a name="worker-tables"></a>Starfsmannatöflur

| Nafn | Tafla |
| --- | --- |
| Starfsmaður | cdm_worker |
| Aðsetur starfskrafts | cdm_workeraddress |
| Persónuupplýsingar starfskrafts | cdm_workerpersonaldetail |
| Kennitala starfskrafts | cdm_workerpersonidentificationnumber |
| Persónukennisgerð starfskrafts | cdm_workerpersonidentificationtype |
| Vinnudagatal | cdm_workcalendar |
| Dagur í vinnudagatali | cdm_workcalendarday |
| Frídagur í vinnudagatali |cdm_workcalendarholiday |
| Frídagslína í vinnudagatali | cdm_workcalendarholidayline |
| Tímabil vinnudagatals | cdm_workcalendartimeinterval (Ekki virkjað fyrir sérsniðinn reitastuðning) |
| Bankareikningur starfskrafts | cdm_workerbankaccount |

## <a name="worker-setup-tables"></a>Uppsetningartöflur starfsmanns

| Nafn | Tafla |
| --- | --- |
| Uppgjafahermaður | cdm_veteranstatus |
| Þjóðernisuppruni | cdm_ethnicorigin |
| Ástæðukóði | cdm_reasoncode |
| Útgáfustofnun persónuskilríkja | cdm_personidentificationissuingagency |

## <a name="competency-tables"></a>Hæfnistöflur

| Nafn | Tafla |
| --- | --- |
| Gerð hæfni | cdm_skilltype |

## <a name="table-relationship-models"></a>Líkön töfluvensla

### <a name="worker"></a>Starfsmaður

![Starfsmaður](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a>Starf og starfstaða

![Starf og starfstaða](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a>Fríðindi

![Fríðindi](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a>Laun

![Laun](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a>Hætta

![Hætta](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a>Vinnudagatal

![Vinnudagatal](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a>Sjá einnig

[Velja tækni við samþættingu gagna](hr-admin-integration-choose-technology.md)<br>
[Skilgreina Dataverse-samþættingu](hr-admin-integration-common-data-service.md)<br>
[Skilgreina Dataverse-sýndartöflur](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[Algengar spurningar um sýndartöflur Human Resources](hr-admin-virtual-entity-faq.md)<br>
[Hvað er Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)<br>
[Hugtakauppfærslur](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro#terminology-updates)
