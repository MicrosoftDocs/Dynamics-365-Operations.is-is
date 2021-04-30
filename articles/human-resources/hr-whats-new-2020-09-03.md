---
title: Nýjungar eða breytingar í Dynamics 365 Human Resources (03. september 2020)
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Human Resources fyrir 3. september 2020.
author: andreabichsel
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-09-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 10978d8843e7bce2800d62b63e58152569be9631
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891770"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-3-2020"></a>Nýjungar eða breytingar í Dynamics 365 Human Resources (3. september 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Dynamics 365 Human Resources. Breytingar eiga við um byggingarnúmer 8.1.3504. Tölurnar í sviga í sumum fyrirsögnum vísa til stuðningsnúmera í Lifecycle Services (LCS) vegna tilvísunar.

Frekari upplýsingar um væntanlegu eiginleikana í Human Resources er að finna í [Yfirlit yfir Dynamics 365 Human Resources 2019 útgáfutímabil 2](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/). Nánari upplýsingar um uppfærsluferlið fyrir Human Resources er að finna í [Uppfærsluferli](hr-admin-setup-update-process.md).

## <a name="in-this-release"></a>Í þessari útgáfu

### <a name="new-default-financial-dimensions-grid-and-dialog-pattern-throughout-human-resources-469495"></a>Ný sjálfgefin hnitanet fjárhagsvídda og svarmynstur í Human Resources (469495)

Nýja mynstrið fyrir fjárhagsvíddir er nú aðgengilegt á eftirtöldum svæðum:

- Stöðuaðgerðir (Snið: **HcmPositionActionDetail**)
- Tekjukóðar launa (Snið: **PayrollEarningCode**)

### <a name="entries-dont-appear-in-company-leave-calendar-if-leave-and-absence-calendar-enhancements-arent-enabled-484406"></a>Færslur birtast ekki í frídagatali fyrirtækis ef ekki er kveikt á Viðbætur dagatals yfir leyfi og fjarvistir (484406)

Þessi útgáfa leiðréttir vandamál þar sem frífærslur eru ekki birtar í frídagatali fyrirtækisins. Þetta vandamál kemur aðeins upp þegar valkostur Eiginleikastjórnunar **Viðbætur dagatals yfir leyfi og fjarvistir** er ekki virkur.

### <a name="benefitplanemployeeentity-issue-467597"></a>BenefitPlanEmployeeEntity vandamál (467597)

Þessi útgáfa leiðréttir vandamál með **BenefitsPlanEmployee** eininguna. Þegar verið er að flytja inn innskráningar starfsmanns eru **Tryggingarkóði** og **Kóði áætlunargerðar** nú rangt stilltir. Þetta vandamál veldur því að fríðindaáætlanir starfsmanna birtast á rangan hátt í **Fríðindaáætlun starfsmanns** og í **Opnar innskráningar** skjámyndum í sjálfsafgreiðslu starfsmanna.

### <a name="electronic-file-1094-c-output-missing-letter-in-xml-435190"></a>Rafræn skrá 1094-C úttakstaf vantar í XML (435190)

Þessi breyting leiðréttir vandamál með 1094-C úttaksskrána þar sem staf vantar þegar verið er að senda inn til IRS.

### <a name="employee-variable-compensation-table-mapped-to-fixed-compensation-form-476117"></a>Tafla breytilegra launa starfsmanns varpað á eyðublað fastra launa (476117)

Þessi breyting samstillir reiti fastra launa við föst laun. Reitir breytilegra launa eru nú aðeins í boði í skjámyndinni breytileg laun.

### <a name="leave-requests-allowed-before-enrollment-if-that-leave-type-has-a-negative-minimum-balance-469917"></a>Leyfisbeiðnir leyfðar fyrir skráningu ef gerð leyfis er með neikvæða lágmarksstöðu (469917)

Þessi breyting bannar innslátt leyfisbeiðna fyrir skráningu í áætlunina, jafnvel þótt skráning sé með neikvæða lágmarksstöðu. Aðeins er hægt að færa inn eða senda beiðnir þegar áætlunin er virk.

### <a name="document-templates-dont-download-457279"></a>Skjalasniðmát sækja ekki (457279)

Með þessari breytingu er nú hægt að sækja öll skjalasniðmát. 

### <a name="data-displays-as-column-headers-instead-of-rows-for-the-pay-rate-field-in-the-compensation-plan-report-476077"></a>Gögn birt sem dálkhausar í stað lína fyrir reitinn Launataxti í skýrslu launafyrirkomulags (476077)

Greiningarskýrslan birtir nú réttar upplýsingar fyrir **Launataxta**.

## <a name="in-preview"></a>Í kynningarútgáfu

### <a name="human-resources-application-in-teams"></a>Forrit „Human Resources“ í Teams

Starfsmenn geta skoðað og beðið um tíma frá vinnu innan Microsoft Teams. Hægt er að hafa umsjón með þjark til að búa til beiðnir um leyfi. Frekari upplýsingar má finna á

- [Umhverfi starfsmannaleyfis og -fjarvista í Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) í Dynamics 365 2020 útgáfutímabilsáætlun 1
- [Forritið „Human Resources“ í Teams](./hr-admin-teams-leave-app.md) í Human Resources fylgiskjölum

### <a name="human-resources-app-in-teams-preview-features"></a>Forritið Human Resources í forskoðunareiginleikum Teams
 
-  **Tilkynningar**: Sendendur og samþykktaraðilar frítímabeiðni verða látnir vita í forriti Human Resources í Teams. Samþykktaraðilar geta samþykkt eða hafnað beiðnum um frí. Sendendur verða látnir vita hvort beiðnin hafi verið samþykkt eða henni hafnað. Frekari upplýsingar má finna á
   - [Umhverfi starfsmannaleyfis og -fjarvista í Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) í Dynamics 365 2020 útgáfutímabilsáætlun 2
   - [Virkja tilkynningar fyrir forritið Human Resources í Teams](./hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) í Human Resources fylgiskjölum
   - [Kveikja eða slökkva á Teams tilkynningum fyrir einstaka notendur](./hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users) í Human Resources fylgiskjölum
   - [Teams-tilkynningarnar](./hr-teams-leave-app.md#respond-to-teams-notifications) í Human Resources fylgiskjölum
   - [Skoða frídagdagatal teymisins](./hr-teams-leave-app.md#view-your-teams-leave-calendar) í fylgiskjölum Human Resources
 
- **Frítímadagatal stjórndanda**: Stjórnendur geta séð samþykkt frí og frí sem bíður ákvörðunar fyrir beina undirmenn í dagatalsyfirliti. Þetta yfirlit veitir auðveldan skilning á því hvenær teymismeðlimir þeirra eru fjarri vinnu. Frekari upplýsingar má finna á
   - [Umhverfi starfsmannaleyfis og -fjarvista í Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) í Dynamics 365 2020 útgáfutímabilsáætlun 2
   - [Skoða frídagdagatal teymisins](./hr-teams-leave-app.md#view-your-teams-leave-calendar) í fylgiskjölum Human Resources

### <a name="configuration-option-to-position-work-items-assigned-to-me-list-477004"></a>Skilgreiningarvalkostur fyrir stöðu vinnuliða sem úthlutað er á mig (477004)

Nýr valkostur er nú tiltækur til að staðsetja **Vinnuliðum sem úthlutað er á mig** lista í hægri dálknum á stjórnborðinu. Með þessari breytingu eru allir vinnuliðir og verkefnalistar birtir á sama svæði. Virkjaðu þessa virkni með því að kveikja á **(Forskoðun) Endurbætur á upplifun verkflæðis** í eiginleikastjórnun. Frekari upplýsingar um að kveikja á forútgáfueiginleikum er að finna í [Vinna með eiginleika](hr-admin-manage-features.md).

Þessi eiginleiki er einnig fyrir verkflæðisvalkosti sem birtast í skjámyndunum starfsmannaaðgerðir. Verkflæðisvalkostur birtist einnig fyrir ofan flýtiflipa aðgerðarinnar fyrir flýtiaðgang. Frekari upplýsingar má finna á 

- [Endurbætur á upplifun verkflæðis fyrir fyrirtæki og starfsfólk](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) í Dynamics 365 2020 útgáfutímabilsáætlun 2

![Vinnuliðir sem úthlutað er á mig](./media/hr-workflow-work-items-assigned-to-me.png)

![Flýtiaðgangur að verkflæðisatriðum](./media/hr-workflow-quick-access.png)

## <a name="coming-soon"></a>Væntanlegt

### <a name="checklist-entities-included-in-dataverse"></a>Einingar gátlista innifaldar í Dataverse

Gátlistaeiningar fyrir Ráðstafanir vegna nýrra starfsmanna, Ráðstafanir vegna starfsloka og viðskiptaferla verða bráðum tiltækar í Dataverse.

### <a name="benefits-management-reason-codes"></a>Ástæðukóðar fyrir fríðindastjórnun

Ástæðukóðar fyrir fríðindastjórnun verða brátt sameinaðir við tiltæka ástæðukóða í Human Resources. Ef ástæðukóðar voru stofnaðir í Fríðindastjórnun sem eru yfir 15 stafir að lengd þarf að breyta heiti ástæðukóðans í Fríðindastjórnun **Ástæðukóðar** skjámyndinni þannig að þeir eru 15 stafir eða minna. Þegar búið er að uppfæra heitið mun ástæðukóðinn birtast undir fyrirliggjandi skjámynd ástæðukóða í starfsmannastjórnun. Þessi breyting verður tiltæk í framtíðinni og mun ekki hafa áhrif á fyrirliggjandi virkni.

## <a name="see-also"></a>Sjá einnig

[Nýjungar eða breytingar í Mannauði](hr-admin-whats-new.md)</br>
[Yfirlit yfir Dynamics 365 Human Resources Losunarbylgja 2019](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Uppfærsluferli](hr-admin-setup-update-process.md)</br>
[Vinna með eiginleika](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
