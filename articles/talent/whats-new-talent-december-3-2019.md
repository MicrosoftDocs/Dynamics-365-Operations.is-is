---
title: Nýjungar eða breytingar í Dynamics 365 Talent (3. desember 2019)
description: Þessi grein lýsir nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 12/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-12-03
ms.dyn365.ops.version: Talent
ms.openlocfilehash: b1ed998302762203bad736161a27a48152de65f7
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897719"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-december-3-2019"></a>Nýjungar eða breytingar í Dynamics 365 Talent (3. desember 2019)

Í þessari grein er að finna lýsingu á nýjum eða breyttum eiginleikum Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Breytingar í Attract

Þessi útgáfa inniheldur minniháttar villuleiðréttingar fyrir Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Breytingar í Onboard

Þessi útgáfa inniheldur minniháttar villuleiðréttingar fyrir Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Breytingar í Core HR

Breytingum sem lýst er í þessum kafla gilda um byggingarnúmer 8.1.2646. Tölurnar í sviga í sumum fyrirsögnum vísa til stuðningsnúmera í Microsoft Dynamics Lifecycle Services (LCS).

### <a name="feature-management-workspace"></a>Vinnusvæði eiginleikastjórnunar

Vinnusvæðið **Stjórnun eiginleika** býður upp á lista yfir eiginleika sem eru afhentir í hverri útgáfu. Sjálfgefið er að slökkt sé á nýjum eiginleikum. Hægt er að nota vinnusvæðið til að kveikja á þeim og skoða fylgiskjölin fyrir þá. Nánari upplýsingar um stjórnun eiginleika er að finna í [Eiginleikastjórnunaryfirlit](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).

Allar nýju aðgerðirnar eru áfram í forskoðun í að minnsta kosti 30 daga og venjulega 30-60 daga. Helstu eiginleikar eru venjulega fáanlegir í október og apríl ár hvert í kjölfar forskoðunartímabilsins. Um leið og þú sérð nýja möguleika í vinnusvæðinu **Stjórnun eiginleika** er hægt að kveikja á þeim. Sumar aðgerðir kunna að vera sjálfkrafa á.
 
Stundum er sambyggður eiginleiki virkur og ekki er hægt að slökkva á honum (til dæmis vinnusvæðinu **Stjórnun eiginleika**).
 
Þegar eiginleiki er almennt tiltækur kann að vera kveikt eða slökkt á honum í framleiðsluumhverfi. Vinnusvæðið **Stjórnun eiginleika** gefur til kynna hvenær forsýningareiginleiki verður nauðsynlegur. Þessi dagsetning er venjulega 1. október eða 1. apríl til að samræma hálfsársáætlun um losun. Ekki er hægt að slökkva á skyldueiginleikum. Þar til það verður skylda geturðu kveikt og slökkt á eiginleikum í öllu umhverfi.

### <a name="add-automatic-scheduling-of-batch-job-history-cleanup-332528"></a>Bæta við sjálfvirka tímasetningu á hreinsun runuvinnslusögu (332528)

Með þessari breytingu keyrir **Runuvinnslusaga** á hverju kvöldi og fjarlægir söguleg atriði runuvinnslu sem eru eldri en 30 daga.

### <a name="talent-doesnt-respond-in-worker-actions-when-identification-number-length-doesnt-match-the-identification-type-390971"></a>Talent svarar ekki í aðgerðum starfskrafta þegar lengd auðkennisnúmers passar ekki við auðkennisgerðina (390971)

Þessi útgáfa leiðréttir vandann sem birtist þegar lengd auðkennisnúmers er ekki í samræmi við skilgreininguna innan auðkennisgerðarinnar. 

### <a name="fixed-compensation-doesnt-update-level-with-changes-to-position-details--348085"></a>Föst laun uppfæra ekki stig með breytingum á stöðuupplýsingum (348085)

Í útgáfu vikunnar **Upphafsdagsetning bóta** ákvarðar vinnslan sem tengist stöðunni á þeim tímapunkti þegar stofnuð er ný fastlaunaskrá fyrir starfsmann.

### <a name="workers-employees-and-contractors-lists-show-worker-type-as-both-when-they-should-only-be-worker-or-contractor-384473"></a>Listar yfir verkamenn, starfsmenn og verktaka sýna starfskraftagerð sem Bæði þegar þeir ættu aðeins að vera verkamaður eða verktaki (384473)

Þessi breyting endurspeglar nákvæmlega þá tegund starfskrafts sem kominn er inn (verktaki eða starfsmaður).

### <a name="email-notifications-for-new-hire-actions-dont-contain-name-information-due-to-security-policies-383402"></a>Tilkynningar í tölvupósti vegna nýrra leiguaðgerða innihalda ekki nafnupplýsingar vegna öryggisstefnu (383402)

Þessi breyting leiðréttir upplýsingarnar sem sýndar eru í fornafns- eða eftirnafnsreitum innan staðgengla fyrir verkflæði þegar háþróað öryggi er virkt.

### <a name="system-allows-two-full-day-leave-requests-for-the-same-day-379284"></a>Kerfið leyfir tvær heilsdagsbeiðnir um orlof fyrir sama dag (379284)

Með þessari breytingu geturðu ekki gefið út tvær orlofsbeiðnir fyrir sama dag. 

### <a name="address-changes-list-should-be-sorted-by-effective-date-352798"></a>Listar yfir aðsetursbreytingar skal vera raðað af Gildisdagsetningu (352798)

Með þessari breytingu er listanum yfir breytingu á heimilisfangi raðað eftir **Gildisdagsetningu**.

### <a name="leave-requests-should-allow-deletes-from-common-data-service-to-talent-376999"></a>Orlofsbeiðnir ættu að leyfa eyðingu úr Common Data Service í Talent (376999)

Með þessari breytingu er hægt að eyða drögum og niðurfelldum orlofsbeiðnum úr Common Data Service og fjarlægja síðan úr Talent.

### <a name="delete-earning-codes-is-allowed-when-the-same-earning-code-is-assigned-to-an-employee-371792"></a>Það er leyfilegt að eyða launakóða þegar sama launakóða er úthlutað til starfsmanns (371792)

Í þessari útgáfu verður þú fyrst að fjarlægja launakóðann frá starfsmanninum áður en þú eyðir launakóðanum úr kerfinu.

### <a name="leave-and-absence-workflow-with-two-approval-stages-fails-to-complete--391116"></a>Verkferli orlofs og fjarveru með tveimur samþykkisstigum tekst ekki að ljúka (391116)

Með þessari breytingu heldur vinnuflæði leyfis og fjarveru áfram í gegnum öll skrefin þegar fleiri en eitt samþykki stig er stillt fyrir beiðnina.

### <a name="issue-date-doesnt-sync-to-common-data-service-when-updated-or-entered-in-talent-397361"></a>Útgáfudagsetning samstillist ekki við Common Data Service þegar hún er uppfærð eða slegin inn í Talent (397361)

Þessi breyting leiðréttir vandamál þar sem útgáfudagsetningin fyrir skrár **Persónuauðkennis** voru ekki samstilltar við Common Data Service úr Talent.

### <a name="hierarchy-circular-reference-error-issued-when-assigning-a-manager-to-a-position-386659"></a>Tilvísunarvilla í stigveldi útgefin við úthlutun stjórnanda í stöðu (386659)

Þessi breyting leiðréttir einkvæma atburðarás þar sem hringvirk tilvísunavilla birtist þegar nýjum stjórnanda er úthlutað í stöðu.

### <a name="common-data-service-entities-that-now-support-custom-fields"></a>Einingar Common Data Service sem styðja sérsniðna reiti núna

Eftirfarandi einingar Common Data Service styðja núna sérsniðna reiti:

| Nafn | Eining |
| --- | --- |
| Bankareikningsgreiðslur | cdm_bankaccountdisbursement |
| Útreikningstíðni fríðinda | cdm_benefitcalculationfrequency |
| Útreikningsíðni fríðinda á launatímabili | cdm_benefitcalculationfrequencypayperiod |
| Hlutfall útreikninga fyrir fríðindi | cdm_benefitcalculationrate |
| Upplýsingar um hlutfall útreikninga fyrir fríðindi | cdm_benefitcalculationratedetail |
| Fríðindavalkostur | cdm_benefitoption |
| Fríðindaáætlun | cdm_benefitplan (Ekki virkjað fyrir sérsniðinn reitastuðning) |
| Gerð fríðinda | cdm_benefittype |
| Dagatal viðskiptaferlis | cdm_businessprocesscalendar |
| Hópverkefni viðskiptaferlis | cdm_businessprocessgroupassignment |
| Verkhópur viðskiptaferlissafns | cdm_businessprocesslibrarytaskgroup |
| Stig viðskiptaferlis | cdm_businessprocessstage |
| Haus gátlistasniðmáts | cdm_businessprocesstemplateheader |
| Verkefni gátlistasniðmáts | cdm_businessprocesstemplatetask |
| Fyrirt.   | cdm_company |
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
| Deild | cdm_department |
| Ráðning | cdm_employment |
| Þjóðernisuppruni | cdm_ethnicorigin |
| Fast launatilvik | cdm_fixedcompensationevent |
| Vinnsla | cdm_job |
| Starfshlutverk | cdm_jobfunction |
| Staða starfs | cdm_jobposition |
| Starfsgerð | cdm_jobtype |
| Tungumál | cdm_language |
| Orlofsbankafærsla | cdm_leavebanktransaction |
| Orlofsskráning | cdm_leaveenrollment |
| Leyfisáætlun | cdm_leaveplan |
| Orlofsbeiðni | cdm_leaverequest |
| Upplýsingar um orlofsbeiðni | cdm_leaverequestdetail |
| Gerð leyfis | cdm_leavetype |
| Ástæðukóði orlofsgerðar | cdm_leavetypereasoncode |
| Greiðsluferli | cdm_paycycle |
| Launatímabil | cdm_payperiod |
| Tekjukóði launa | cdm_payrollearningcode |
| Útgáfustofnun persónuskilríkja | cdm_personidentificationissuingagency |
| Gerð stöðu | cdm_positiontype |
| Stöðuúthlutun starfskrafts | cdm_positionworkerassignmentmap |
| Ástæðukóði | cdm_reasoncode |
| Gerð hæfni | cdm_skilltype |
| Skattumdæmi | cdm_taxregion |
| Veitiregla | cdm_vestingrule |
| Uppgjafahermaður | cdm_veteranstatus |
| Vinnudagatal | cdm_workcalendar |
| Dagur í vinnudagatali | cdm_workcalendarday |
| Frídagur í vinnudagatali |cdm_workcalendarholiday |
| Frídagslína í vinnudagatali | cdm_workcalendarholidayline |
| Tímabil vinnudagatals | cdm_workcalendartimeinterval (Ekki virkjað fyrir sérsniðinn reitastuðning) |
| Starfskraftur | cdm_worker |
| Aðsetur starfskrafts | cdm_workeraddress |
| Bankareikningur starfskrafts | cdm_workerbankaccount |
| Föst laun starfskrafts | cdm_workerfixedcompensation |
| Persónuupplýsingar starfskrafts | cdm_workerpersonaldetail |
| Kennitala starfskrafts | cdm_workerpersonidentificationnumber |
| Persónukennisgerð starfskrafts | cdm_workerpersonidentificationtype |

## <a name="in-preview"></a>Í kynningarútgáfu

Forskoðunareiginleikar eru aðeins í boði í umhverfi **sandkassa**.

### <a name="print-performance-reviews"></a>Prenta árangursumsagnir

Sjá [Prenta árangursumsagnir](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) í Dynamics 365: 2019 útgáfu bylgjuáætlun 2.
