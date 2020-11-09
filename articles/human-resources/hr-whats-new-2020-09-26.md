---
title: Nýjungar eða breytingar í Dynamics 365 Human Resources 26. september 2020
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Human Resources fyrir 26. september 2020.
author: jcart1106
manager: tfehr
ms.date: 09/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d27104a08cdc899f12942d80e693f3495d90a6ec
ms.sourcegitcommit: 1329b3b98854422c4c3773ede44a5cefa7d07085
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/19/2020
ms.locfileid: "4040077"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-26-2020"></a>Nýjungar eða breytingar í Dynamics 365 Human Resources 26. september 2020

Í þessu efnisatriði er lýst nýjum, breyttum eða væntanlegum eiginleikum í Dynamics 365 Human Resources. Frekari upplýsingar um uppfærsluferlið okkar og áætlun er að finna í [Uppfærsluferli](hr-admin-setup-update-process.md).

Frekari upplýsingar um nýja eiginleika og hvenær þeir verða aðgengilegir almenningi er að finna í [Yfirlit yfir Dynamics 365 Human Resources Losunarbylgju 2 2020](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/dynamics365-human-resources/).

## <a name="in-this-release"></a>Í þessari útgáfu

Þessi útgáfa felur í sér eftirfarandi nýja eiginleika og villuleiðréttingar. Breytingar gilda um smíðanúmer 8.1.3589-hf. 3.

### <a name="new-features"></a>Nýjar aðgerðir

Eftirfarandi eiginleiki er almennt aðgengilegur með þessari útgáfu:

- **Verkvangsuppfærsla 10.0.13 er nú tiltæk** : Frekari upplýsingar um uppfærsluna er að finna í [verkvangsuppfærslur fyrir útgáfu 10.0.13 af Finance and Operations forrita (2020. október)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-13).

### <a name="bug-fixes"></a>Villuleiðréttingar

Eftirfarandi villuleiðréttingar eru innifaldar í þessari útgáfu.

> [!NOTE]
> Markmiðið okkar er að koma þessum upplýsingum til þín eins fljótt og auðið er. Það kunna að koma uppfærslur á þessu efnisatriði til að hafa með leiðréttingar á villum sem slæddust með smíðinni eftir að þetta efnisatriði var gefið út upphaflega.

| Númer úthreyfingar | Úthreyfing | lýsing |
| --- | --- | --- |
| 469495 | Uppfæra töflu sjálfgefinna fjárhagsvídda og svarglugga | Hnitanet fjárhagsvídda og svarglugga er uppfært í Human Resources. |
| 474887 | Vinnuliður fyrir beiðni um leyfi opnar rangan tengil í ákvörðun | Þegar Verkflæðisskilgreining inniheldur Handvirk ákvörðun opnar **Vinnuliðum úthlutað á mig** rangan tengil þegar farið er úr leyfisbeiðni og sýnir annaðhvort auða skjámynd eða beiðni sem er stofnuð í stað þess að henni hafi verið úthlutað á þessa ákvörðun. |
| 474962 | Færibreytureining leyfis og fjarvista er með svæði sem eru með óljós merki | Einingamerkimiðar fyrir leyfi og fjarvistir eru uppfærðir þannig að það sé skýrara. |
| 481401 | Uppsöfnunarvinnsla hangir þegar upphafsdagsgrunnur uppsöfnunar er á eftir upphafsddegi uppsöfnunar og í lok mánaðar | Uppsöfnunarvinnsla er uppfærð þannig að hún er ekki með frestun þegar dagsetningargrunnur uppsöfnunar er á eftir upphafsdagsetningu uppsöfnunarinnar og í lok mánaðarins. |
| 447167 | Listar sem eru að renna út taka með óvirka starfsmenn | Flipinn **Færslur sem eru að renna út** í **Starfsmannastjórnun** eru með óvirka starfskrafta. Nú inniheldur hún aðeins virka starfskrafta. |
| 486840 | Röng Fjarvistarbeiðni opnast frá **Vinnuliðum úthlutað á mig** | Val á fjarvistabeiðni úr **Vinnuliðum úthlutað á mig** opnar ekki lengur síðustu beiðni um fjarvistabeiðnir sem úthlutað er á núverandi notanda. |
| 506868 | Common Data Service **Titill** svæði ekki stillt fyrir **Starfsheiti** einingu | Svæðið **Titill** í **vinnslunni** og **Starfsstaða** einingar birtist sem ekki tilgreint. Reiturinn **Heiti** birtist nú. |
| 430359 | Ekki er hægt að fá aðgang að verkefnum gátlista með stjórnanda og hlutverkum starfsmanns úthlutuðum | Starfsmenn með starfslok í framtíðinni gátu ekki fengið aðgang að gátlistaverkum sínum ef þeir höfðu aðeins hlutverk starfsmanns eða stjórnanda. Notendur með hlutverkið starfsmaður eða yfirmaður geta ekki fengið aðgang að verkefni sem tengist dagsetningu uppsagnar í framtíðinni. |
| 458102 | Nýr starfsmaður birtist ekki í **Launaupplýsingar starfsmanna** einingunni þegar hún var stofnuð | Nýir starfsmenn eru teknir með í launaupplýsingum starfsmanns án þess að þurfa að opna launaupplýsingar fyrir starfsmanninn áður en einingin er flutt inn. |

## <a name="in-preview"></a>Í kynningarútgáfu

Eftirfarandi nýir eiginleikar eru í kynningarútgáfu. Nánari upplýsingar um hvernig eigi að kveikja og slökkva á eiginleikum er að finna í [Stjórna eiginleikum](hr-admin-manage-features.md).

| Eiginleiki | Útgáfuáætlun | Fylgiskjöl |
| --- | --- | --- |
| Human Resources-forritið í Microsoft Teams | [Viðmót fyrir leyfi og fjarvistir starfsmanns í Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Forritið „Human Resources“ í Teams](https://go.microsoft.com/fwlink/?linkid=2127841)<br>[Stjórna leyfisbeiðnum í Teams](hr-teams-leave-app.md) |
| Bættar verkflæðisbeiðnir og samþykktir | [Endurbætur á viðmóti fyrir verkflæði fyrirtækis- og starfsmannastjórnunar](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Skilgreiningarvalkostur fyrir stöðu vinnuliða sem úthlutað er á mig](https://docs.microsoft.com/dynamics365/human-resources/hr-whats-new-2020-09-03#configuration-option-to-position-work-items-assigned-to-me-list-477004) |

## <a name="coming-soon"></a>Væntanlegt

Eftirfarandi nýr eiginleiki er áætlaður fyrir síðari útgáfu:

- [Sérstilltir tenglar í sjálfsafgreiðslu stjórnanda](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/custom-links-manager-self-service)

Fyrir ítarlegan lista yfir áætlaða eiginleika og áætlaðar útgáfur þeirra skal skoða [Yfirlit yfir Dynamics 365 Human Resources 2019 losunarbylgju 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/).

## <a name="additional-resources"></a>Frekari upplýsingar

[Nýjungar eða breytingar í Human Resources](hr-admin-whats-new.md)
[Yfirlit yfir Dynamics 365 Human Resources 2020 útgáfutímabil 2](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)
[Uppfærsluferli](hr-admin-setup-update-process.md)
[Stjórna eiginleikum](hr-admin-manage-features.md)
