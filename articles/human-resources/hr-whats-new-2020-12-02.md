---
title: Nýjungar eða breytingar í Dynamics 365 Human Resources 2. desember 2020
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Human Resources fyrir 2. desember 2020.
author: marcelbf
manager: tfehr
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 36d82efa182bff12442d51908d634cbddbd13fa9
ms.sourcegitcommit: fc852ae4939089a294d00fdf9cad8d6372ffb012
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2021
ms.locfileid: "5080039"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-december-2-2020"></a>Nýjungar eða breytingar í Dynamics 365 Human Resources 2. desember 2020

Í þessu efnisatriði er lýst nýjum, breyttum eða væntanlegum eiginleikum í Dynamics 365 Human Resources.

Frekari upplýsingar um uppfærsluferlið okkar og áætlun er að finna í [Uppfærsluferli](hr-admin-setup-update-process.md).

Frekari upplýsingar um nýja eiginleika og hvenær þeir verða aðgengilegir almenningi er að finna í [Yfirlit yfir Dynamics 365 Human Resources Losunarbylgju 2 2020](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Í þessari útgáfu

Þessi útgáfa felur í sér eftirfarandi nýja eiginleika og villuleiðréttingar. Breytingar eiga við um byggingarnúmer 8.1.3788.

### <a name="new-features"></a>Nýjar aðgerðir

Eftirfarandi eiginleikar eru almennt aðgengilegur með þessari útgáfu.

| Eiginleiki | Útgáfuáætlun | Fylgiskjöl |
| --- | --- | --- |
| Stjórnendur geta sent ráðningarbeiðnir fyrir stöður | [Stjórnendur geta sent inn ráðningarbeiðni fyrir opnar stöður](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/manager-submit-request-recruit-open-positions) | [Bæta við ráðningarbeiðni](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit#add-a-recruiting-request) |
| Auknar notandaupplýsingar umsækjanda í starfsmannastjórnun | [Auknar notandaupplýsingar umsækjanda í starfsmannastjórnun](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enhanced-candidate-profile-personnel-management) | [Bæta við eða breyta notandaupplýsingum umsækjanda](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit#add-or-edit-a-candidate-profile) |
| Virkja einfaldar samþættingar með ráðningaraðilum | [Virkja einfaldar samþættingar með ráðningaraðilum](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enable-simplified-integration-recruiting-providers) | [Ráða umsækjendur](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit) |
| Sérstilltir tenglar í sjálfsafgreiðslu stjórnanda. | [Sérstilltir tenglar í sjálfsafgreiðslu stjórnanda](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/custom-links-manager-self-service) | [Sérstilltir tenglar í sjálfsafgreiðslu stjórnanda](https://aka.ms/MSSCustomLinks) |


### <a name="bug-fixes"></a>Villuleiðréttingar

Eftirfarandi villuleiðréttingar eru innifaldar í þessari útgáfu.

> [!NOTE]
> Markmiðið okkar er að koma þessum upplýsingum til þín eins fljótt og auðið er. Við gætum uppfært þetta efnisatriði til að hafa með leiðréttingar á villum sem slæddust með smíðinni eftir að þetta efnisatriði var gefið út upphaflega.

| Númer úthreyfingar | Úthreyfing | lýsing |
| --- | --- | --- |
| 514087 | BenefitEligibilityProcessResult ætti að innihalda dag og tíma sem var notuð í ferlinu. | Úrvinnsla úr niðurstöðum BenefitEligibity inniheldur nú datetimestamp fyrir síðustu vinnslu, sem vantaði fyrr. |
| 526903 | Fríðindaskráning mistekst fyrir áætlanir ásamt skjólstæðingum þegar kveikt er á **Sjálfvirkt val á fulltrúum** í **Samnýttar færibreytur fyrir mannauð**. | Leyst var úr vandamáli þegar fríðindaskráning mistókst fyrir skjólstæðinga þegar kveikt var á valkostinum **Sjálfvirkt val á fulltrúum** fyrir sjálfgefna fulltrúa. |
| 521922 | Færibreytan **Sýna fjarvistir án frekari upplýsinga** birtir upplýsingar um frítímabeiðnir í fjarvistadagatali teymis. | Leyfisgerð, litur leyfisgerðar og frekari upplýsingar um dag birtust í fjarvistadagatali teymisins þegar **Sýna fjarvistir án frekari upplýsinga** var stillt á **Já** í **Færibreytum leyfis og fjarvista**. Þetta vandamál hefur nú verið leyst og nú birtist leyfisgerðin ekki og sjálfgefinn litur leyfisgerðar (dökkblár) er notaður fyrir allar leyfisgerðir á fjarvistadagatali teymisins. |
| 527316 | Breytingar á starfstitli, stöðu og tilkynningum starfskrafts eru ekki samstilltar. | Tengslum titils var áður bætt við einingar starfs, stöðu og starfskrafts. Samstilling þessa vensla virkar fyrir samstillingu úr Human Resources í Dataverse, en virkaði ekki fyrir tilkynningar frá Dataverse. Þetta hefur verið meðhöndlað. |
| 512275 | Fjarlægja skal litavalkostina úr **Færibreytur leyfis og fjarvista**. | Nú eru litir skilgreindir á leyfisgerðinni og því er ekki lengur þörf á litavalkostum fyrir **Færibreytur leyfis og fjarvista** og því voru slíkir valkostir fjarlægðir. |
| 437112 | Villandi texti villuskilaboða við stöðuverkefni starfsmanns. | Uppfærði villuboð við ráðningu starfskrafts þegar reynt var að úthluta starfsmanni stöðu sem er ekki virk. Uppfærð skilaboð **Tilgreind staða er ekki virk frá upphafsdagsetningu ráðningar. Athugaðu tímalengd þessarar stöðu.** |
| 527816 | Vandamál með afköst með síðuna **Frí**. | Afköst hafa verið endurbætt á siðunni **Frí**. |
| 523158 | BenefitPeriodMigrationUpgrade og BenefitPlanMigrationUpgrade eru ekki í vinnslu. | Leysti úr vandamálum varðandi vinnslur við flutning fríðinda sem tengdust því að **Tímabil** og **Áætlun** voru ekki framkvæmdar á réttan hátt. |

## <a name="in-preview"></a>Í kynningarútgáfu

Eftirfarandi nýir eiginleikar eru í kynningarútgáfu. Nánari upplýsingar um hvernig eigi að kveikja og slökkva á eiginleikum er að finna í [Stjórna eiginleikum](hr-admin-manage-features.md).

| Eiginleiki | Útgáfuáætlun | Fylgiskjöl |
| --- | --- | --- |
| Human Resources-forritið í Microsoft Teams | [Viðmót fyrir leyfi og fjarvistir starfsmanns í Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Forritið „Human Resources“ í Teams](https://go.microsoft.com/fwlink/?linkid=2127841)<br>[Stjórna leyfisbeiðnum í Teams](hr-teams-leave-app.md) |
| Bættar verkflæðisbeiðnir og samþykktir | [Endurbætur á viðmóti fyrir verkflæði fyrirtækis- og starfsmannastjórnunar](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Skilgreiningarvalkostur fyrir stöðu vinnuliða sem úthlutað er á mig](https://docs.microsoft.com/dynamics365/human-resources/hr-whats-new-2020-09-03#configuration-option-to-position-work-items-assigned-to-me-list-477004) |
| Samþætting við LinkedIn Talent Hub | [Samþætting við LinkedIn Talent Hub](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/integration-linkedin-talent-hub) | [Samþætta við LinkedIn Talent Hub](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-linkedin) |
|Yfirlit stjórnanda milli fyrirtækja um leyfi til starfsfólks | [Yfirlit stjórnanda milli fyrirtækja um leyfi til starfsfólks](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [Grunnstilla færibreytur leyfis og fjarvista](https://docs.microsoft.com/dynamics365/human-resources/hr-leave-and-absence-parameters) |
|Veita frekari innsýn í leyfisstöðu| [Veita frekari innsýn í leyfisstöðu](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/provide-additional-insight-into-leave-balances) | [Stjórna leyfi starfsmanns](https://docs.microsoft.com/dynamics365/human-resources/hr-leave-and-absence-manage-employee-leave) |
| Stjórnendur geta sent ráðningarbeiðnir fyrir stöður | [Stjórnendur geta sent inn ráðningarbeiðni fyrir opnar stöður](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/manager-submit-request-recruit-open-positions) | [Bæta við ráðningarbeiðni](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit#add-a-recruiting-request) |
| Auknar notandaupplýsingar umsækjanda í starfsmannastjórnun | [Auknar notandaupplýsingar umsækjanda í starfsmannastjórnun](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enhanced-candidate-profile-personnel-management) | [Bæta við eða breyta notandaupplýsingum umsækjanda](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit#add-or-edit-a-candidate-profile) |
| Virkja einfaldar samþættingar með ráðningaraðilum | [Virkja einfaldar samþættingar með ráðningaraðilum](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enable-simplified-integration-recruiting-providers) | [Ráða umsækjendur](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit) |

## <a name="coming-soon"></a>Væntanlegt

Fyrir ítarlegan lista yfir áætlaða eiginleika og áætlaðar útgáfur þeirra skal skoða [Yfirlit yfir Dynamics 365 Human Resources 2020 losunarbylgju 2](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Sjá einnig

[Nýjungar eða breytingar í Mannauði](hr-admin-whats-new.md)</br>
[Yfirlit yfir Dynamics 365 Human Resources 2020 losunarbylgju 2](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)</br>
[Uppfærsluferli](hr-admin-setup-update-process.md)</br>
[Vinna með eiginleika](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]