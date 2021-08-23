---
title: Nýjungar eða breytingar í Dynamics 365 Human Resources (6. október 2020)
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Human Resources fyrir 6. október 2020.
author: jcart1106
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 090533a4391488f4ec0929dd4866e55a478ee6e639563ad37a6819592e91b23c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6739204"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-october-6-2020"></a>Nýjungar eða breytingar í Dynamics 365 Human Resources (6. október 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Í þessu efnisatriði er lýst nýjum, breyttum eða væntanlegum eiginleikum í Dynamics 365 Human Resources. Frekari upplýsingar um uppfærsluferlið okkar og áætlun er að finna í [Uppfærsluferli](hr-admin-setup-update-process.md).

Frekari upplýsingar um nýja eiginleika og hvenær þeir verða aðgengilegir almenningi er að finna í [Yfirlit yfir Dynamics 365 Human Resources Losunarbylgju 2 2020](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Í þessari útgáfu

Þessi útgáfa felur í sér eftirfarandi nýja eiginleika og villuleiðréttingar. Breytingar eiga við um byggingarnúmer 8.1.3636.

### <a name="new-features"></a>Nýjar aðgerðir

Eftirfarandi eiginleiki er almennt aðgengilegur með þessar útgáfu.

| Eiginleiki | Útgáfuáætlun | Fylgiskjöl |
| --- | --- | --- |
| Frekari innsýn í leyfisdagatöl | [Veita frekari innsýn í yfirlit leyfisdagatala](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/provide-additional-insight-leave-calendar-views) | [Skoða dagbækur hóps og fyrirtækis](hr-employee-self-service-calendar.md) |

### <a name="bug-fixes"></a>Villuleiðréttingar

Eftirfarandi villuleiðréttingar eru innifaldar í þessari útgáfu.

>[!NOTE]
> Markmiðið okkar er að koma þessum upplýsingum til þín eins fljótt og auðið er. Það kunna að koma uppfærslur á þessu efnisatriði til að hafa með leiðréttingar á villum sem slæddust með smíðinni eftir að þetta efnisatriði var gefið út upphaflega.

| Númer úthreyfingar | Úthreyfing | lýsing |
| --- | --- | --- |
| 448806 | **Sjálfgefin gerð auðkennis** flytur út sem **RecID** í HCM-færibreytum | Þessi breyting á einingu Human Resources-færibreyta bætir við aukalegum dálk sem sýnir **Sjálfgefna gerð auðkennis**. |
| 492923 | Verkskráningarnar vistast ekki í Lifecycle Services (LCS) | Nú er hægt að vista verkskráningar í LCS. |
| 429950 | Föst laun renna ekki út á réttan hátt þegar stöðu er breytt | Þegar stöðu starfsmanns á síðunni **Flytja starfsmann** er breytt, var lokadagsetning launa stillt á einn dag á undan lok stöðunnar. Lokadagsetningin launa er nú sú sama og lokadagsetning stöðunnar. |
| 467214 | **Greiningar fastra launa** birtast aðeins ef **Heiti umreiknings launataxta** er stillt á **Árlegur** | Launataxtar fastra launa með heiti annað en **Árlegur** birtust ekki í launagreiningum. Með þessari uppfærslu notar launagreiningin nú alla umreikninga launataxta. Þegar skýrslan er keyrð eftir **Tímakaupi** eða **Föstum launum** er umreikningur launataxta sem notar annað tímabil en tímakaup haft með í síunni **Föst laun**. Aðeins launataxtar með tímann **Tímakaup** eru hafðir með í síunni **Tímakaup**. |
| 482464 | Þegar **Yfirferðir** eru skoðaðar, breytist yfirlitið **Upplýsingar** ekki í töfluyfirlit eftir að sía er notuð | Eftir að síu er beitt kemur töfluyfirlitið fram eins og búast má við. |
| 483184 | Human Resources safnar ekki upp leyfi þegar valið er **Grunnlag** sem **Leiðrétt upphafsdagsetning** í færslunni **Leyfisskráning** |**Leiðrétt upphafsdagsetning** er fyllt út og notuð þegar leyfi er safnað upp.  |
| 509731 | Beiðni um frí fyrir starfsmann sem mun hætta á næstunni veldur vandræðum ef hann óskar eftir fríi eftir uppsagnardaginn | Nú er hægt að senda inn beiðnir um frí fyrir starfsmenn með uppsagnardag fram í tímann svo lengi sem beiðnin er á undan uppsagnardeginum. |
| 510716 | Launagreiningar ná yfir bæði karlkyns og kvenkyns starfsmenn fyrir **Tímakaup að meðaltali hjá körlum** | Í launagreiningunni innihélt **Tímakaup að meðatali hjá körlum** í **Lýðfræðilegu launagreiningunni** meðallaun kvenna. Nú inniheldur hún aðeins karla. |
| 511348 | Sjálfsafgreiðsla fríðinda á aðeins að sýna fríðindaáætlanir sem eru gildar frá deginum í dag til loka fríðindatímabilsins | Útrunnar fríðindaáætlanir voru sýndar starfsmönnum á síðunni **Fríðindaskráning**. Þessi leiðrétting fjarlægir þessar áætlanir. |
| 512706 | Stilltu eftirfarandi reiti sem skrifvarða:<ul><li>BenefitPlanEmployeeEntity</li><li>EnrollmentConfirmed</li><li>EnrollmentConfirmedBy</li><li>EnrollmentConfirmedDateTime | Hnapparnir **Bæta við** og **Fjarlægja** fyrir upplýsingar um víddir voru virkjaðir á rangan hátt eftir að aðgerðinni lauk. Þessi uppfærsla á síðunni **Upplýsingar um stöðuaðgerð** gerir reitina óbreytanlega Þegar aðgerðinni lýkur. |

## <a name="in-preview"></a>Í kynningarútgáfu

Eftirfarandi nýir eiginleikar eru í kynningarútgáfu. Nánari upplýsingar um hvernig eigi að kveikja og slökkva á eiginleikum er að finna í [Stjórna eiginleikum](hr-admin-manage-features.md).

| Eiginleiki | Útgáfuáætlun | Fylgiskjöl |
| --- | --- | --- |
| Human Resources-forritið í Microsoft Teams | [Viðmót fyrir leyfi og fjarvistir starfsmanns í Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Forritið „Human Resources“ í Teams](./hr-admin-teams-leave-app.md)<br>[Stjórna leyfisbeiðnum í Teams](hr-teams-leave-app.md) |
| Bættar verkflæðisbeiðnir og samþykktir | [Endurbætur á viðmóti fyrir verkflæði fyrirtækis- og starfsmannastjórnunar](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Skilgreiningarvalkostur fyrir stöðu vinnuliða sem úthlutað er á mig](./hr-whats-new-2020-09-03.md#configuration-option-to-position-work-items-assigned-to-me-list-477004) |
| Sýndareiningar í Dataverse fyrir Human Resources | [Stækka Dynamics 365 Human Resources kjarnagögn í Dataverse](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/expand-dynamics-365-human-resources-core-data-common-data-service) | [Skilgreina Dataverse sýndareiningar](hr-admin-integration-common-data-service-virtual-entities.md) |

## <a name="coming-soon"></a>Væntanlegt

Eftirfarandi nýir eiginleikar munu koma í seinni útgáfum:

- **Einingar gátlista innifaldar í Dataverse**: Gátlistaeiningar fyrir Ráðstafanir vegna nýrra starfsmanna, Ráðstafanir vegna starfsloka og viðskiptaferla verða bráðum tiltækar í Dataverse.

- **Ástæðukóðar fyrir fríðindastjórnun**: Ástæðukóðar fyrir fríðindastjórnun verða brátt sameinaðir við tiltæka ástæðukóða í Human Resources. Ef ástæðukóðar voru stofnaðir í Fríðindastjórnun sem eru yfir 15 stafir að lengd þarf að breyta heiti ástæðukóðans í Fríðindastjórnun **Ástæðukóðar** skjámyndinni þannig að þeir eru 15 stafir eða minna. Þegar búið er að uppfæra heitið mun ástæðukóðinn birtast undir fyrirliggjandi skjámynd ástæðukóða í starfsmannastjórnun. Þessi breyting verður tiltæk í framtíðinni og mun ekki hafa áhrif á fyrirliggjandi virkni.

- **Sérstilltir tenglar í sjálfsafgreiðslu stjórnanda**: Til að styðja stjórnendur erum við að útvíkka möguleikana í sjálfsafgreiðslu stjórnanda. Við bætum við möguleikanum á að bæta sérstilltum tenglum við flipann **Teymið mitt**. Þessi eiginleiki er svipaður og eiginleiki sérstilltra tengla í **Upplýsingaflipanum mínum** í sjálfsafgreiðslu starfsmanns. Nánari upplýsingar er að finna í [Sérstilltir tenglar í sjálfsafgreiðslu stjórnanda](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/custom-links-manager-self-service).

Fyrir ítarlegan lista yfir áætlaða eiginleika og áætlaðar útgáfur þeirra skal skoða [Yfirlit yfir Dynamics 365 Human Resources 2019 losunarbylgju 2](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/).

## <a name="additional-resources"></a>Frekari upplýsingar

[Nýjungar eða breytingar í Mannauði](hr-admin-whats-new.md)</br>
[Yfirlit yfir Dynamics 365 Human Resources 2020 losunarbylgju 2](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)</br>
[Uppfærsluferli](hr-admin-setup-update-process.md)</br>
[Vinna með eiginleika](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]