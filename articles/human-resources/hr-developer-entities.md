---
title: Common Data Service einingar
description: Microsoft Dynamics 365 Human Resources notar Common Data Service til að gera mögulegt atburðarás fyrir stækkun og samþættingu.
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
ms.openlocfilehash: 988fa0b6d39a49b973626a8a0abe83c546f42297
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/17/2020
ms.locfileid: "4530007"
---
# <a name="common-data-service-entities"></a>Common Data Service einingar

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Microsoft Dynamics 365 Human Resources notar Common Data Service til að gera mögulegt atburðarás fyrir stækkun og samþættingu.

Nánari upplýsingar um Common Data Service er að finna í [Hvað er Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).

Eftirfarandi einingar Human Resources eru í boði í Common Data Service.

## <a name="benefit-entities"></a>Fríðindaeiningar

| Nafn | Eining |
| --- | --- |
| Útreikningstíðni fríðinda | cdm_benefitcalculationfrequency |
| Útreikningsíðni fríðinda á launatímabili | cdm_benefitcalculationfrequencypayperiod |
| Hlutfall útreikninga fyrir fríðindi | cdm_benefitcalculationrate |
| Upplýsingar um hlutfall útreikninga fyrir fríðindi | cdm_benefitcalculationratedetail |
| Fríðindavalkostur | cdm_benefitoption |
| Fríðindaáætlun | cdm_benefitplan (Ekki virkjað fyrir sérsniðinn reitastuðning) |
| Gerð fríðinda | cdm_benefittype |

## <a name="business-process-tasks-entities"></a>Einingar viðskiptaferlaverka

| Nafn | Eining |
| --- | --- |
| Dagatal viðskiptaferlis | cdm_businessprocesscalendar |
| Hópverkefni viðskiptaferlis | cdm_businessprocessgroupassignment |
| Verkhópur viðskiptaferlissafns | cdm_businessprocesslibrarytaskgroup |
| Stig viðskiptaferlis | cdm_businessprocessstage |
| Haus gátlistasniðmáts | cdm_businessprocesstemplateheader |
| Verkefni gátlistasniðmáts | cdm_businessprocesstemplatetask |

## <a name="compensation-entities"></a>Bótaeiningar

| Nafn | Eining |
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

## <a name="organization-entities"></a>Fyrirtækjaeiningar

| Nafn | Eining |
| --- | --- |
| Deild | cdm_department |
| Ráðning | cdm_employment |
| Fyrirt. | cdm_company |
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
> Fjárhagslegar víddir fyrir **Gerð stöðu**, **Stöðuúthlutun starfskrafts** og **Starf** veita einnar áttar samþættingu við Common Data Service. Uppfærslur fjárhagsvídda samstillast ekki eins og stendur úr Common Data Service í Human Resources. 

## <a name="leave-and-absence-entities"></a>Einingar fyrir leyfi og fjarvistir

| Nafn | Eining |
| --- | --- |
| Orlofsbankafærsla | cdm_leavebanktransaction |
| Orlofsskráning | cdm_leaveenrollment |
| Leyfisáætlun | cdm_leaveplan |
| Orlofsbeiðni | cdm_leaverequest |
| Upplýsingar um orlofsbeiðni | cdm_leaverequestdetail |
| Gerð leyfis | cdm_leavetype |
| Ástæðukóði orlofsgerðar | cdm_leavetypereasoncode |

## <a name="payroll-entities"></a>Launaeiningar

| Nafn | Eining |
| --- | --- |
| Greiðsluferli | cdm_paycycle |
| Launatímabil | cdm_payperiod |
| Tekjukóði launa | cdm_payrollearningcode |
| Bankareikningsgreiðslur | cdm_bankaccountdisbursement |
| Skattumdæmi | cdm_taxregion |

## <a name="worker-entities"></a>Starfskraftaeiningar

| Nafn | Eining |
| --- | --- |
| Starfskraftur | cdm_worker |
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

## <a name="worker-setup-entities"></a>Uppsetningareiningar starfskrafts

| Nafn | Eining |
| --- | --- |
| Uppgjafahermaður | cdm_veteranstatus |
| Þjóðernisuppruni | cdm_ethnicorigin |
| Ástæðukóði | cdm_reasoncode |
| Útgáfustofnun persónuskilríkja | cdm_personidentificationissuingagency |

## <a name="competency-entities"></a>Hæfnieiningar

| Nafn | Eining |
| --- | --- |
| Gerð hæfni | cdm_skilltype |

## <a name="entity-relationship-models"></a>Einingaþáttur tengslalíkanseiningar

### <a name="worker"></a>Starfskraftur

![Starfskraftur](./media/HCMCommon-worker-entity-diagram.png)

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

[Velja tækni við samþættingu gagna](hr-admin-integration-choose-technology.md)</br>
[Skilgreina Common Data Service-samþættingu](hr-admin-integration-common-data-service.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]