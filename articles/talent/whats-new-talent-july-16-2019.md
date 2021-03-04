---
title: Nýjungar eða breytingar í Dynamics 365 Talent (16. júlí 2019)
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 07/16/2019
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
ms.search.validFrom: 2019-07-16
ms.dyn365.ops.version: Talent
ms.openlocfilehash: cd7f288e5c1015f4266db527adfcd62a5dbbc95f
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528100"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-july-16-2019"></a>Nýjungar eða breytingar í Dynamics 365 Talent (16. júlí 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Breytingar í Attract
Þessi útgáfa inniheldur minniháttar villuleiðréttingar fyrir Dynamics 365 Talent: Attract.

### <a name="coming-soon-in-attract"></a>Væntanlegt í Attract
#### <a name="job-approvals-appear-on-the-home-page"></a>Vinnslusamþykktir birtast á heimasíðunni

Samþykktir birtast í hlutanum **Samþykktir** í yfirlitinu. Samþykktaraðilar geta yfirfarið samþykktir sínar undir **Úthlutað á þig**, sem sýnir auðkenni vinnslu, titil vinnslu, aðra samþykktaraðila og dagsetningu þegar vinnslunni var úthlutað. Notendur sem senda inn vinnslu til samþykktar geta yfirfarið vinnslur sínar undir **Beiðni frá þér**, sem sýnir samþykktaraðilana sem eiga enn eftir að samþykkja innsenda vinnslu.

## <a name="changes-in-onboard"></a>Breytingar í Onboard
Þessi útgáfa inniheldur minniháttar villuleiðréttingar fyrir Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Breytingar í Core HR
Breytingum sem lýst er í þessum kafla gilda um byggingarnúmer 8.1.2390.

### <a name="common-data-service-entities-that-now-support-custom-fields"></a>Einingar Common Data Service sem styðja núna sérsniðna reiti

- BusinessProcessCalendar                     
- BusinessProcessGroupAssignment         
- BusinessProcessStage                          
- BusinessProcessTemplateHeader          
- BusinessProcessTemplateTask            
- HcmBenefitOption                              
- HcmBenefitType                                  
- HcmCompensationGrid                            
- HcmCompensationLevel                          
- HcmCompensationPayFrequency                 
- HcmCompensationReferencePointSetup        
- HcmCompensationReferencePointSetupLine 
- HcmCompensationRegion                     
- HcmCompFixedPlanTable                     
- HcmEmployment                                
- HcmEthnicOrigin                                
- HcmFixedCompensationEvent                 
- HcmJob                                           
- HcmJobFunction
- HcmJobType
- HcmLanguageCode
- HcmPayrollCalculationFrequency
- HcmPosition
- HcmPositionType
- HcmSkillType
- HcmVeteranStatus
- HcmWorkCalendarHoliday
- HcmWorkCalendarHolidayLine
- HcmWorker
- HcmWorkerPersonalDetail
- LeaveType
- OMDepartment
- OMLegalEntity
- PayCycle
- PayPeriod
- PayrollBenefitCalculationRate
- PayrollBenefitCalculationRateDetail
- PayrollEarningCode

### <a name="unable-to-see-goals-and-reviews-in-manager-self-service"></a>Ekki hægt að sjá markmið og umsagnir í sjálfsafgreiðslu stjórnenda

Breytingarnar í þessari viku gera nú kleift að birta og breyta markmiðum og umsögnum fyrir stjórnendur sem sleppa stigum í sjálfsafgreiðslu stjórnenda.

### <a name="goal-form-cannot-be-closed-after-a-user-edits-any-goal-field"></a>Ekki er hægt að loka skjámyndinni Markmið eftir að notandi breytir markmiðsreit

Þessi útgáfa leiðréttir vandamál þar sem markmiðsskjámynd lokast ekki þegar valið er **Loka**.

### <a name="creating-new-goals-and-saving-displays-error"></a>Villa við að búa til ný markmið og vistun

Þessi útgáfa leiðréttir vandamál við vistun markmiða í sjálfsafgreiðslu starfsmanna og stjórnenda.

### <a name="unable-to-add-a-field-to-position-details"></a>Ekki er hægt að bæta reit við upplýsingar um stöðu 

Með þessari útgáfu eru sérsniðnir reitir nú studdir í upplýsingar um stöðu.
 
### <a name="unable-to-set-up-expiring-date-on-the-earning-code-through-data-management"></a>Ekki tókst að setja upp lokadagsetningu á launakóðanum með gagnastjórnun

Breytingar gera þér nú kleift að stilla lokadaga á tekjukóðum í gagnastjórnun.

### <a name="new-custom-fields-dont-sync-quickly-enough"></a>Nýir sérsniðnir reitir samstilla ekki nógu hratt

Afköst af sérsniðinni reitarsamstillingu við Common Data Service hefur verið bætt með útgáfu vikunnar.

### <a name="entity-export-to-database-jobs-fail-with-error-message-format-of-the-initialization-string-does-not-conform-to-specification-starting-at-index-0"></a>Útflutningur eininga í gagnagrunnvinnslur tekst ekki með villuboðum: "Snið frumstillingarstrengsins samræmist ekki forskrift sem byrjar á vísitölu 0."

Þessi útgáfa leiðréttir vandamálið þar sem runuvinnslur í gagnagrunni mistakast. Til að uppfæra handvirkt:

1. Fara á **Gagnastjórnun**.
2. Veldu **Skilgreina útflutning eininga til gagnagrunns**.
3. Sláðu aftur tengingarstrenginn inn í markgagnagrunninn og veldu **Vista**.

### <a name="smtp-email-configuration-suddenly-fails-with-error-message-the-smtp-server-requires-a-secure-connection-or-the-client-was-not-authenticated"></a>SMTP tölvupóststillingar mistakast skyndilega með villuboðunum: "SMTP netþjónninn þarf örugga tengingu eða viðskiptavinurinn var ekki staðfestur."

Þessi útgáfa leiðréttir SMTP tölvupóststillingu sem skyndilega mistekst. Til að uppfæra handvirkt:

1. Farðu í **Kerfisstjórnun**.
2. Veldu **Færibreytur tölvupósts**.
3. Veldu **SMTP stillingar**. 
4. Sláðu aftur inn notandanafn og lykilorð sem notað er fyrir SMTP netþjóninn og veldu **Vista**.

## <a name="in-preview"></a>Í kynningarútgáfu

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>Forskoðunareiginleikar eru aðeins virkjaðir í tilvikum sandkassans

Þegar þú setur fram nýtt tilvik í Talent getur þú tiltekið hvort gerð tilviks er **Framleiðsla** eða **Sandkassi**. Tilvik af gerðinni **Sandkassi** gerir kleift að prófa nýja eiginleika snemma. Öll núverandi tilvik Talent verða uppfærð í tilviksgerðina **Framleiðsla**. Ef uppfæra á eitt af núverandi tilvikum í tilviksgerðina **Sandkassi** skal hafa samband við [notendaþjónustu](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support) til að hefja breytingarbeiðni.

Nánari upplýsingar um hvernig breytingar eru gefnar út er að finna í [Úthluta Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

### <a name="restrict-leave-types-in-time-off-requests"></a>Takmarka leyfisgerðir í frítímabeiðnum

Fyrirtæki geta boðið starfsmönnum upp á margar mismunandi leyfisgerðir. Hins vegar gæti það verið óviðeigandi fyrir starfsmenn að leggja fram beiðni um frest fyrir sumar gerðir leyfis. Þessum leyfisgerðum kann að vera stjórnað af mannauði (HR) í staðinn. Í þessari útgáfu er hægt að skilgreina hvaða leyfisgerðir starfsmenn geta sent inn fyrir frítímabeiðnir. 

### <a name="view-performance-information-for-direct-and-extended-reports-in-manager-self-service"></a>Skoðaðu afkastaupplýsingar fyrir beinar og útbreiddum skýrslum í sjálfsafgreiðslu stjórnanda

Ný valkostur mun gera stjórnendum kleift að skoða árangur af bæði beinum skýrslum sínum og framlengdum skýrslum sínum. Eins og er, geta línustjórnendur úthlutað og uppfært árangursmörk og gefið út nýjar umsagnir. Að auki geta beinar stjórnendur og starfsmenn þeirra viðhaldið og uppfært afkastabækur til að tryggja að ferli afkastarýni gangi vandræðalaust. Þegar þessi breyting er framkvæmd verða stjórnendur að geta skoðað og viðhaldið árangursskyldum upplýsingum um útbreiddar skýrslur auk þeirra beinna skýrslna.


[!INCLUDE[footer-include](../includes/footer-banner.md)]