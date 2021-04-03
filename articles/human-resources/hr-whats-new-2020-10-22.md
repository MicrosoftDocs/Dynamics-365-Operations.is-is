---
title: Nýjungar eða breytingar í Dynamics 365 Human Resources 22. október 2020
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Human Resources fyrir 22. október 2020.
author: jcart1106
manager: tfehr
ms.date: 10/22/2020
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
ms.search.validFrom: 2020-10-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 642250fa34ee87065f4ed2cf8f3893390d271007
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464791"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-october-22-2020"></a>Nýjungar eða breytingar í Dynamics 365 Human Resources 22. október 2020

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Í þessu efnisatriði er lýst nýjum, breyttum eða væntanlegum eiginleikum í Dynamics 365 Human Resources. Frekari upplýsingar um uppfærsluferlið okkar og áætlun er að finna í [Uppfærsluferli](hr-admin-setup-update-process.md).

Frekari upplýsingar um nýja eiginleika og hvenær þeir verða aðgengilegir almenningi er að finna í [Yfirlit yfir Dynamics 365 Human Resources Losunarbylgju 2 2020](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Í þessari útgáfu

Þessi útgáfa felur í sér eftirfarandi nýja eiginleika og villuleiðréttingar. Breytingar eiga við um byggingarnúmer 8.1.3680.

### <a name="new-features"></a>Nýjar aðgerðir

Eftirfarandi eiginleikar eru almennt aðgengilegur með þessari útgáfu.

| Eiginleiki | Útgáfuáætlun | Fylgiskjöl |
| --- | --- | --- |
| Verkvangsuppfærsla 10.0.14(38) | -- | [Verkvangsuppfærslur fyrir útgáfu 10.0.14 fyrir Finance and Operations-forrit (nóvember 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-14) |
| Endurbætur á viðmóti fyrir verkflæði fyrirtækis- og starfsmannastjórnunar | [Endurbætur á viðmóti fyrir verkflæði fyrirtækis- og starfsmannastjórnunar](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Skilgreiningarvalkostur fyrir stöðu vinnuliða sem úthlutað er á mig](https://docs.microsoft.com/dynamics365/human-resources/hr-whats-new-2020-09-03#configuration-option-to-position-work-items-assigned-to-me-list-477004) |


### <a name="bug-fixes"></a>Villuleiðréttingar

Eftirfarandi villuleiðréttingar eru innifaldar í þessari útgáfu.

> [!NOTE]
> Markmiðið okkar er að koma þessum upplýsingum til þín eins fljótt og auðið er. Við gætum uppfært þetta efnisatriði til að hafa með leiðréttingar á villum sem slæddust með smíðinni eftir að þetta efnisatriði var gefið út upphaflega.

| Númer úthreyfingar| Úthreyfing  | lýsing|
| --- | --- | --- |
| 437922 | Innflutningur FMLA-stunda með niðurstöður DMF-eininga í skrifvarðri villu. | Notkun einingar FMLA-stunda til að flytja inn klukkustundir sem tengjast FMLA-málum mistókst. Við bættum við reiknireglu til að tryggja að innfluttar stundir fari ekki yfir stundirnar sem eftir eru fyrir málið. |
| 512019 | Röng upphæð fyrir **Síðustu yfirfærslu**. | Á síðunni **Frí** leiddi breyting á **Frá og með dagsetningunni** til þess að fyrsti dagur næsta fjárhagstímabils sýndi ranga upphæð fyrir **Síðustu yfirfærslu** fyrir gerðina **Árlegt leyfi**. Nú er rétta upphæðin sýnd. |
| 458639 | Einingin **Tengiliðir starfskrafts** styður ekki stillingu breytingarrakningar. | Við uppfærðum eininguna **Tengiliðir starfskrafts** þannig að nú er hægt að nota hana til að koma með sinn eigin gagnagrunn (BYOD).|
| 505347 | Þjálfunarstjórar gátu sent inn leyfisbeiðni fyrir starfsmann þegar einfaldaður eiginleiki starfsmanns var virkjaður. | Hlutverk önnur en HR-aðstoðarmaður eða HR-stjórnandi mega ekki senda inn beiðni um frí fyrir starfsmenn. |
| 513490 | Skráning fríðindastjórnunar: bæta við skráningu fyrir áætlanir með engum tryggingarmöguleikum. | Við virkjuðum skráningarniðurstöður fyrir **Áætlun með engum tryggingarmöguleika**. Þær birtast nú í töflunni **Niðurstöður vinnslu** og eru flokkaðar rétt til að birtast efst. |
| 517021 | Ekki er hægt að velja margar áætlanir með sama kóðanum fyrir **Gerð áætlunar** ef **Gerð áætlunar** er með eina skráningu fyrir hverja gerð. | Takmörkunum var breytt fyrir val á áætlunum þar sem aðeins ein skráning er leyfð. Takmarkanirnar eru nú á stiginu **Kóði áætlunargerðar** í staðinn fyrir **Gerð áætlunar**. Þessi breyting leyfir áætlanir eins og HSA og FSA, sem eru báðar af sömu gerðinni, en þú getur gefið þeim aðskilinn **Kóða áætlunargerðar**. Þannig er hægt að velja þær báðar fyrir sama skráningartímabilið. |
| 444791 | Ekki er hægt að skoða laun í sjálfsafgreiðslu starfsmanna þegar kveikt er á **Takmarka aðgang** í launafyrirkomulaginu. | Í spjaldinu **Laun** í sjálfsafgreiðslu starfsmanns sýndi núverandi launaupphæð og aukningarprósenta „0“ ef starfsmaðurinn var skráður í áætlun þar sem kveikt var á **Takmarka aðgang** og honum úthlutað tilteknum hlutverkum. Við leystum vandamálið þannig að starfsmaðurinn og stjórnandinn geti alltaf séð launaupplýsingar fyrir sig sjálfa og beina undirmenn. |
| 457542 | Uppfærsla á upplýsingum um námskeið eftir að því er lokað uppfærir ekki líka sömu upplýsingarnar fyrir starfsmanninn sem tók námskeiðið. | Starfsmannaupplýsingarnar uppfærast núna á réttan hátt þegar þú breytir upplýsingum um námskeið eftir að námskeiðinu er lokað og enduropnað. |
| 515342 | Ekki er hægt að setja inn gögn í gegnum **CDSLeaveRequestDetailEntity**. Fyrirtækið finnst ekki eða er ekki til. | Nú getur þú notað **CDSLeaveRequestDetailEntity** til að setja inn gögn. |
| 514743 | Villa í skjámyndinni **Færibreyta tölvupósts** þegar Microsoft Exchange er notað. | Skilaboðin „Gat ekki hlaðið niður skrám eða samsetningum...“ birtust á síðunni **Færibreytur tölvupósts** þegar tölvupóstþjónustan var stillt á **Exchange**. Þessi lagfæring gerir síðunni **Færibreytur tölvupósts** einnig kleift að hlaða niður og vista. |


## <a name="in-preview"></a>Í kynningarútgáfu

Eftirfarandi nýir eiginleikar eru í kynningarútgáfu. Nánari upplýsingar um hvernig eigi að kveikja og slökkva á eiginleikum er að finna í [Stjórna eiginleikum](hr-admin-manage-features.md).

| Eiginleiki | Útgáfuáætlun | Fylgiskjöl |
| --- | --- | --- |
| Human Resources-forritið í Microsoft Teams | [Viðmót fyrir leyfi og fjarvistir starfsmanns í Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Forritið „Human Resources“ í Teams](https://go.microsoft.com/fwlink/?linkid=2127841)<br>[Stjórna leyfisbeiðnum í Teams](hr-teams-leave-app.md) |
| Bættar verkflæðisbeiðnir og samþykktir | [Endurbætur á viðmóti fyrir verkflæði fyrirtækis- og starfsmannastjórnunar](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Skilgreiningarvalkostur fyrir stöðu vinnuliða sem úthlutað er á mig](https://docs.microsoft.com/dynamics365/human-resources/hr-whats-new-2020-09-03#configuration-option-to-position-work-items-assigned-to-me-list-477004) |
| Sýndareiningar í Dataverse fyrir Human Resources | [Stækka Dynamics 365 Human Resources kjarnagögn í Dataverse](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/expand-dynamics-365-human-resources-core-data-common-data-service) | [Skilgreina Dataverse sýndareiningar](hr-admin-integration-common-data-service-virtual-entities.md) |
| Samþætting við LinkedIn Talent Hub | [Samþætting við LinkedIn Talent Hub](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/integration-linkedin-talent-hub) | [Samþætta við LinkedIn Talent Hub](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-linkedin) |
| Sérstilltir tenglar í sjálfsafgreiðslu stjórnanda. | [Sérstilltir tenglar í sjálfsafgreiðslu stjórnanda](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/custom-links-manager-self-service) | [Sérstilltir tenglar í sjálfsafgreiðslu stjórnanda](https://aka.ms/MSSCustomLinks) |

## <a name="coming-soon"></a>Væntanlegt

Fyrir ítarlegan lista yfir áætlaða eiginleika og áætlaðar útgáfur þeirra skal skoða [Yfirlit yfir Dynamics 365 Human Resources 2020 losunarbylgju 2](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).


## <a name="see-also"></a>Sjá einnig

[Nýjungar eða breytingar í Mannauði](hr-admin-whats-new.md)</br>
[Yfirlit yfir Dynamics 365 Human Resources 2020 losunarbylgju 2](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)</br>
[Uppfærsluferli](hr-admin-setup-update-process.md)</br>
[Vinna með eiginleika](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]