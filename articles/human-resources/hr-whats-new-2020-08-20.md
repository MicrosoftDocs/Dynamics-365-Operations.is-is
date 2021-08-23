---
title: Nýjungar eða breytingar í Dynamics 365 Human Resources (20. ágúst 2020)
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Human Resources fyrir 20. ágúst 2020.
author: andreabichsel
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-08-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 32535c1f93990306ffaa0a5d97b48d3e6fdda7d014ceeeb2552960cd08b4be6c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6775844"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-august-20-2020"></a>Nýjungar eða breytingar í Dynamics 365 Human Resources (20. ágúst 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Dynamics 365 Human Resources. Breytingar eiga við um byggingarnúmer 8.1.3478. Tölurnar í sviga í sumum fyrirsögnum vísa til stuðningsnúmera í Lifecycle Services (LCS) vegna tilvísunar.

## <a name="show-upcoming-and-pending-leave-of-absence-information-to-cards-in-people-workspace"></a>Sýna væntanlegar upplýsingar um fjarveru í kortum á vinnusvæðinu Starfsfólk

Valkostir fyrir leyfisbeiðni í bið og væntanlega leyfisbeiðni eru nú aðgengilegir á leyfis- og fjarvistarspjaldi á vinnusvæðinu **Einstaklingur**.

## <a name="private-field-isnt-yes-by-default-for-employee-role-in-employee-self-service-477106"></a>Einkasvæði er ekki sjálfgefið „Já“ fyrir hlutverk starfsmanns í sjálfsafgreiðslu starfsmanna (477106)

Reiturinn **Einka** er nú sjálfkrafa **Já** þegar starfsmenn bæta við nýjum aðsetursfærslum í gegnum síðuna **Persónulegar upplýsingar** í sjálfsafgreiðslu starfsmanns. 

## <a name="candidates-to-hire-fasttab-in-personnel-management-shows-an-incorrect-count-of-candidates-470110"></a>Flýtiflipinn fyrir umsækjendur til að ráða í starfsmannastjórnun sýnir ranga talningu á umsækjendum (470110)

Síðan **Starfsmannastjórnun** sýnir nú nákvæmlega þann fjölda umsækjenda sem á að ráða. 

## <a name="cant-enter-sickness-for-terminated-employee-when-accrual-is-set-to-zero-446195"></a>Ekki er hægt að færa inn veikindi fyrir starfsmann sem hættur er störfum þegar uppsöfnun er stillt á núll (446195)

Leyfisfærslur eru nú leyfðar fyrir starfsmenn sem hætta í framtíðinni og uppsöfnun er stillt á núll. Hægt er að færa inn leyfisfærslur fram að starfslokadagsetningu starfsmannsins. 

## <a name="adding-custom-fields-to-the-new-worker-form-disables-the-fields-in-the-action-pane-for-manage-leave-473314"></a>Sérstilltum reitum bætt við nýja skjámynd starfsmanns slekkur á reitum á aðgerðasvæði fyrir stjórnun leyfis (473314)

Valkostirnir fyrir aðgerðasvæði í skjámynd nýs **starfsmanns** í **Stjórna leyfi** verða ekki lengur gerðir óvirkir ef sérstilltum svæðum hefur verið bætt við skjámynd nýs **Starfsmanns**.

## <a name="making-the-leave-comment-field-mandatory-allows-a-leave-request-to-be-submitted-when-no-comment-is-entered-473543"></a>Ef reiturinn fyrir athugasemd um leyfi er gerður áskilinn, gerir kleift að senda inn leyfisbeiðni þegar engin athugasemd er færð inn (473543)

Athugasemdareitir er nú hægt að gera áskilda og leyfisbeiðnir fara eftir þessari stillingu. Áskildir reitir eru forskoðunareiginleiki.

### <a name="dmf-entity-available-for-accrual-suspensions"></a>DMF-eining er í boði fyrir frestun uppsöfnunar

DMF-eining er ekki til staðar fyrir uppsöfnun í bið.

## <a name="in-preview"></a>Í kynningarútgáfu

### <a name="mandatory-fields"></a>Áskildir reitir

Hægt er að gera reiti áskilda með því að nota sérstillingarmöguleika Human Resources. Þessi eiginleiki krefst **Vistuð yfirlit**. Nánari upplýsingar um vistuð yfirlit er að finna í:

- [Vistuð yfirlit - almennt framboð](/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability) í Dynamics 365 2020 útgáfutímabilsáætlun 2
- [Búa til skjámyndir sem nýta vistuð yfirlit til fullnustu](../fin-ops-core/dev-itpro/user-interface/understanding-saved-views.md)

### <a name="human-resources-application-in-teams"></a>Forrit „Human Resources“ í Teams

Starfsmenn geta skoðað og beðið um tíma frá vinnu innan Microsoft Teams. Hægt er að hafa umsjón með þjark til að búa til beiðnir um leyfi. Frekari upplýsingar má finna á

- [Umhverfi starfsmannaleyfis og -fjarvista í Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) í Dynamics 365 2020 útgáfutímabilsáætlun 1
- [Forritið „Human Resources“ í Teams](./hr-admin-teams-leave-app.md)

## <a name="coming-soon"></a>Væntanlegt

### <a name="human-resources-app-in-teams-preview-features"></a>Forritið Human Resources í forskoðunareiginleikum Teams
 
-  **Tilkynningar**: Sendendur og samþykktaraðilar frítímabeiðni verða látnir vita í forriti Human Resources í Teams. Samþykktaraðilar geta samþykkt eða hafnað beiðnum um frí og sendendur verða látnir vita hvort beiðnin hafi verið samþykkt eða henni hafnað.
 
- **Frítímadagatal stjórndanda**: Stjórnendur geta séð samþykkt frí og frí sem bíður ákvörðunar fyrir beina undirmenn í dagatalsyfirliti. Þetta yfirlit veitir auðveldan skilning á því hvenær teymismeðlimir þeirra eru fjarri vinnu.

### <a name="checklist-entities-included-in-dataverse"></a>Einingar gátlista innifaldar í Dataverse

Gátlistaeiningar fyrir Ráðstafanir vegna nýrra starfsmanna, Ráðstafanir vegna starfsloka og viðskiptaferla verða bráðum tiltækar í Dataverse.

## <a name="known-issues"></a>Þekkt vandamál

Vinnusvæðið **Eiginleikastjórnun** sýnir hugsanlega eiginleika sem eru óvirkir sem eiginleikar forútgáfu þegar þeir eru almennt í boði. Hér að neðan er listi yfir almennt tiltæka eiginleika sem sýna ranga stöðu. 

- Fríðindastjórnun
- Málastjórnun
- Gagnagrunnsskráningar (eftirlit)
- Uppsafnað leyfi fyrir eitt fyrirtæki eða eina áætlun
- Frestun uppsafnaðs leyfis og fjarvista
- Ástæðukóði og athugasemd við stöðuleiðréttingu
- Kaupa og selja leyfisdaga
- Leyfis- og fjarvistadagatal
- Reglur um yfirfærslu leyfis
- Endurskoðun uppsafnaðs leyfis
- Eyðing á uppsöfnuðu leyfi
- Sléttun uppsafnaðs leyfis
- Grunnstilla margar leyfisgerðir í einni leyfisáætlun
- Uppfæra viðbætur fyrir frí
- Nota JFS starfsmanns fyrir uppsöfnun
- Launayfirlit þvert á fyrirtæki
- Prenta árangursumsagnir
- Leiðréttingar á uppsöfnun frídaga

### <a name="benefit-plan-employee-entity"></a>Starfsmannaeining fríðindaáætlunar 

Nýlega hafa verið uppgötvuð tvö atriði varðandi eininguna **BenefitsPlanEmployee**. Þegar verið er að flytja inn innskráningar starfsmanns eru **Tryggingarkóði** og **Kóði áætlunargerðar** rangt stilltir. Þetta vandamál veldur því að fríðindaáætlanir starfsmanna birtast á rangan hátt í skjámyndinni **Fríðindaáætlun starfsmanns** og í skjámyndinni **Opnar innskráningar** í sjálfsafgreiðslu starfsmanna. Þetta vandamál getur einnig haft áhrif á getu starfsmannsins til að velja áætlanir í sjálfsafgreiðslu starfsmanna. Sem stendur er ekki til leið framhjá þessu. Þessi lagfæring er efst á forgangslistanum hjá okkur við munum koma með lagfæringu í næstu útgáfu.

## <a name="see-also"></a>Sjá einnig

[Nýjungar eða breytingar í Mannauði](hr-admin-whats-new.md)</br>
[Yfirlit yfir Dynamics 365 Human Resources Losunarbylgja 2019](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Uppfærsluferli](hr-admin-setup-update-process.md)</br>
[Vinna með eiginleika](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]