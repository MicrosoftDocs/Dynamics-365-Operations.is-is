---
title: Nýjungar eða breytingar í Dynamics 365 Human Resources 22. júní 2021
description: Þessi grein lýsir eiginleikum sem eru annað hvort nýir eða breyttir í Microsoft Dynamics 365 Human Resources fyrir 22. júní 2021.
author: marcelbf
ms.date: 06/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-06-22
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 61c457abf87ce2da554ddb1472512416159c4dca
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/29/2022
ms.locfileid: "9068425"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-june-22-2021"></a>Nýjungar eða breytingar í Dynamics 365 Human Resources 22. júní 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Þessi grein lýsir eiginleikum sem eru nýir, breyttir eða koma fljótlega í Dynamics 365 Human Resources.

Frekari upplýsingar um uppfærsluferlið okkar og áætlun er að finna í [Uppfærsluferli](hr-admin-setup-update-process.md).

Frekari upplýsingar um nýja eiginleika og hvenær þeir verða aðgengilegir almenningi er að finna í [Yfirlit yfir Dynamics 365 Human Resources Losunarbylgju 1 2021](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Í þessari útgáfu

Þessi útgáfa felur í sér eftirfarandi nýja eiginleika og villuleiðréttingar. Breytingar eiga við um byggingarnúmer 8.1.4258.

### <a name="new-features"></a>Nýjar aðgerðir

Eftirfarandi eiginleikar eru almennt aðgengilegur með þessari útgáfu.

| Eiginleiki | Útgáfuáætlun | Fylgiskjöl |
| --- | --- | --- |
| Eiginleiki fyrir tilkynningu til notenda starfsmanna án atvinnu - Þegar ítarlegur aðgangur er á og slökkt er á eiginleikanum **Skoða alla starfsmenn án atvinnu** í eiginleikastjórnun birtist borði í skjámynd starfsmanna án atvinnu. Borðinn beinir notandanum á að kveikja á eiginleikanum **Skoða alla starfskrafta án starfs**. | Ekki tiltækt| [Starfskraftar án starfs](/dynamics365/human-resources/hr-personnel-workers-without-employment)|
| Stuðningur sérstilltra reita fyrir hæfnireglu fríðindastjórnunar | [Stuðningur við sérstillta reiti fyrir vinnslu á hæfni](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-eligibility-processing) |[Stilla hæfnisreglur](/dynamics365/human-resources/hr-benefits-setup-eligibility-rules) |
| Endurskoðun færslu fyrir uppsafnað leyfi | Ekki tiltækt | [Endurskoðun færslu fyrir uppsafnað leyfi](hr-leave-and-absence-accrue.md)|
| Viðbætur á upplifun verkflæðis fyrir leyfi og fjarvistir | [Viðbætur á upplifun verkflæðis fyrir leyfi og fjarvistir](https://go.microsoft.com/fwlink/?linkid=2147528) | [Biðja um frí](hr-employee-self-service-request-time-off.md)|

### <a name="bug-fixes"></a>Villuleiðréttingar

Eftirfarandi villuleiðréttingar eru innifaldar í þessari útgáfu.

> [!NOTE]
> Markmiðið okkar er að koma þessum upplýsingum til þín eins fljótt og auðið er. Við gætum uppfært þessa grein til að innihalda villuleiðréttingar sem komu inn í bygginguna eftir að þessi grein var upphaflega birt.

| Númer úthreyfingar | Gefa út |  Lýsing |
| --- | --- | --- |
| 583052 | Notandi sem fær ábendingu getur breytt móttekinni ábendingu | Þegar starfsmaður sem fær ábendingu um frammistöðubók velur **Bæta við ytri tengli**, verður skjámyndin breytanleg sem gerir starfsmanni kleift að breyta ábendingu um frammistöðu sem hann hefur móttekið. |
| 522281 | Val á fjölda starfsmanna í reitum launaskipulags í Launastjórnun leiðir til rangrar niðurstöðu| Þegar kafað er niður í launafyrirkomulag af vinnusvæði launa mun réttur fjöldi starfsmanna birtast. |
| 580683 | Notendum sem úthlutað er hlutverkum starfsmanns og stjórnanda geta ekki hengt við athugasemdir eða uppfært frammistöðubók | Notendum sem úthlutað er hlutverkum starfsmanns og stjórnanda geta ekki hengt við athugasemdir eða uppfært frammistöðubók. Notandinn fær villuna „Ekki hægt að búa til færslu í færslu frammistöðubókar (HcmPerfJournal). Öryggisregluheimild hafnað. |
| 583077 | Fæðingardagur starfsmanns í fyrirtækisdagbók leyfa og fjarvista sýnir ranga dagsetningu | Notendur geta skoðað réttan fæðingardag starfsmanna í fyrirtækisdagbók leyfa og fjarvista. |
| 586996 | Eiginleikinn fyrir yfirlit leyfis milli fyrirtækja leiðir til þess að stöður verði tómar þegar aðgangur er takmarkaður við eitt fyrirtæki | Notendur geta skoðað leyfisstöður framtíðar fyrir starfsmann á réttan hátt þegar leyfisyfirlit milli fyrirtækja er virkjað. |
| 581014 | Virkjun á yfirliti yfir leyfi og fjarvistir milli fyrirtækja leiðir til villu þegar framtíðarstöður eru skoðaðar | Villur hafa verið lagaðar þegar notendur voru að skoða leyfisstöður fram í tímann með leyfisyfirliti milli fyrirtækja virkjað. |
| 509404 | Greining á starfsmannafjölda deildar tekur ekki tillit til hreyfingar starfsmanna milli deilda. | þegar starfsmaður flytur úr einni deild í aðra, endurspegla gögn um starfsmannafjölda deildar ekki gömlu deildina þar sem skipt er um starfsmann ef upplýsingar um stöðuna eru útrunnar á yfirstandandi ári. |
| 584851 | Regla um hlutfallsskiptingu á inneign fríðinda stillt á „Engin“ veitir aldrei inneign |Reglan um hlutfallsskiptingu sveigjanlegrar inneignar stillt á „Engin“ leiddi til þess að starfsmenn fengu núll inneign fyrir fríðindatímabil, burtséð frá því hvenær þeir voru ráðnir. Þetta hefur verið lagað þannig að starfsmaður ætti að fá fulla sveigjanlega inneign ef þeir eru ráðnir áður en fríðindatímabilið hefst og ekki ef þeir eru ráðnir eftir að tímabilið hefst. |
| 584897 | Afritun aðgangsheimildarinnar „Nota ytri grunneiginleika“ leiðir til villu | Þegar reynt var að afrita aðgangsheimildina „Nota ytri grunneiginleika“ fékk notandinn upp villuna „Fann ekki hlut með kennimerkinu UserDefinedAppHostDialogView.“ |
| 575692 | Uppsafnað leyfi og fjarvistir er ekki í boði fyrir starfmenn í biðstöðu | Hægt er að keyra uppsafnað leyfi og fjarvistir á ráðningum í framtíðinni þegar **Einfölduð starfsmannafærsla** er virkjuð. |
| 580110 | Með því að bæta fyrirtæki við samþættingu launa endurstillist samþættingin á að nota allar einingarnar jafnvel þótt valkosturinn er stilltur á að ekki uppfæra verkið | Ef viðskiptavinur hefur fjarlægt einingar eða breytt gagnaverkum fyrir launasamþættingu og hefur valkostinn stilltan á að koma í veg fyrir sjálfvirka endurnýjun á verkinu, þá er stillingin og uppfærslur verksins hunsaðar þegar bætt er nýju fyrirtæki við samþættinguna.  |
| 584518 |Vandamál með afköst á úrvinnslu fríðindaskráningar | Þessi villa tók á vandamálum með afköst í eldra ferli fríðindaþátttöku. |

## <a name="in-preview"></a>Í kynningarútgáfu

Eftirfarandi nýir eiginleikar eru í kynningarútgáfu. Nánari upplýsingar um hvernig eigi að kveikja og slökkva á eiginleikum er að finna í [Stjórna eiginleikum](hr-admin-manage-features.md).

| Eiginleiki | Útgáfuáætlun | Fylgiskjöl |
| --- | --- | --- |
| Vinnusvæði fríðindastjórnunar | [Vinnusvæði fríðindastjórnunar (forskoðun)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Vinnusvæði fríðindastjórnunar](hr-benefits-management-workspace.md) |
| Virkja einfalda launasamþættingu (API fyrir launasamþættingu) | [Virkja einfalda samþættingu við launaveitu](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Launasamþættingar-API](hr-admin-integration-payroll-api-introduction.md)|


## <a name="coming-soon"></a>Væntanlegt

| Eiginleiki | Upplýsingar |
| --- | --- |
| Verkvangsuppfærsla 10.0.19 (43) | Verkvangsuppfærsla 10.0.19 á að fara af stað í útgáfu 28. maí 2021. Fyrir frekari upplýsingar, sjá [Uppfærslur á vettvangi fyrir útgáfu 10.0.19 af fjármála- og rekstraröppum (júní 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-19). |
|  Víxlhnappur fyrir birtingu starfsaldurs | Þessi eiginleiki býður upp á möguleikann á því að nota mismunandi dagsetningar til að reikna út starfsaldur sem birtist í skjámyndinni **Einfölduð starfsmannafærsla** og í skjámyndinni **Einstaklingar**.  Boðið verður upp á þetta í færibreytum Human Resources. |
|  Virkja fjarvistarstjóra til að stjórna fríi | [Virkja fjarvistarstjóra til að stjórna fríi](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) |
|  Fyrirmæli um viðhengi fyrir tilteknar leyfisgerðir | Þessi eiginleiki gerir stjórnendum kleift að bæta við umboðsviðhengjum þegar leyfisbeiðnir eru sendar fyrir tilgreindar leyfisgerðir. |
|  Stilla leyfiseiningar fyrir hverja leyfisgerð | Þessi eiginleiki gerir stjórnendum kleift að skilgreina leyfiseiningar (klukkustundir og dagar) fyrir hverja leyfisgerð.  |
| Gera kleift að merkja starfsmenn sem tilbúna að fá greitt | [Gera kleift að merkja starfsmenn sem tilbúna að fá greitt](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) |

Fyrir ítarlegan lista yfir áætlaða eiginleika og áætlaðar útgáfur þeirra skal skoða [Yfirlit yfir Dynamics 365 Human Resources 2021 losunarbylgju 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Sjá einnig

[Nýjungar eða breytingar í Mannauði](hr-admin-whats-new.md)</br>
[Yfirlit yfir Dynamics 365 Human Resources 2021 losunarbylgju 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Uppfærsluferli](hr-admin-setup-update-process.md)</br>
[Vinna með eiginleika](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

