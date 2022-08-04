---
title: Nýjungar eða breytingar í Dynamics 365 Human Resources 12. júlí 2021
description: Þessi grein lýsir eiginleikum sem eru annað hvort nýir eða breyttir í Microsoft Dynamics 365 Human Resources fyrir 12. júlí 2021.
author: marcelbf
ms.date: 07/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-07-12
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d7fb922a35504b69aa8cc3d92cb981e8fb060290
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/29/2022
ms.locfileid: "9067587"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-12-2021"></a>Nýjungar eða breytingar í Dynamics 365 Human Resources 12. júlí 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Þessi grein lýsir eiginleikum sem eru nýir, breyttir eða koma fljótlega í Dynamics 365 Human Resources.

Frekari upplýsingar um uppfærsluferlið okkar og áætlun er að finna í [Uppfærsluferli](hr-admin-setup-update-process.md).

Frekari upplýsingar um nýja eiginleika og hvenær þeir verða aðgengilegir almenningi er að finna í [Yfirlit yfir Dynamics 365 Human Resources Losunarbylgju 1 2021](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Í þessari útgáfu

Þessi útgáfa felur í sér eftirfarandi nýja eiginleika og villuleiðréttingar. Breytingar eiga við um byggingarnúmer 8.1.4353.

### <a name="new-features"></a>Nýjar aðgerðir

Eftirfarandi eiginleikar eru almennt aðgengilegur með þessari útgáfu.

| Eiginleiki | Útgáfuáætlun | Fylgiskjöl |
| --- | --- | --- |
|  Víxlhnappur fyrir birtingu starfsaldurs | |Þessi eiginleiki býður upp á möguleikann á því að nota mismunandi dagsetningar til að reikna út starfsaldur sem birtist á síðunni **Einfölduð starfsmannafærsla** og á síðunni **Einstaklingar**.  Boðið verður upp á þetta í [Færibreytum Human Resources](/dynamics365/human-resources/hr-setup-parameters). |


### <a name="bug-fixes"></a>Villuleiðréttingar

Eftirfarandi villuleiðréttingar eru innifaldar í þessari útgáfu.

> [!NOTE]
> Markmiðið okkar er að koma þessum upplýsingum til þín eins fljótt og auðið er. Við gætum uppfært þessa grein til að innihalda villuleiðréttingar sem komu inn í bygginguna eftir að þessi grein var upphaflega birt.

| Númer úthreyfingar | Gefa út |  Lýsing |
| --- | --- | --- |
| 595871 | Um svæðið í Human Resources sem er með rangan Dataverse orðalista | Með vöruþróun á Common Data Service til Dataverse hefur orðalisti verið uppfærður í Microsoft Dynamics 365 Human Resources upplýsingaglugga (**Hjálp og notendaþjónusta > Um**). |
| 598676 | Skjámynd einfaldrar starfsmannafærslu hnekkir verki getur leitt til villu þegar notað með vistuðu yfirliti| Á síðu **Starfskrafts**, ef kveikt er á eiginleikanum „Einfölduð starfsmannafærsla“, getur forrið klikkað ef stillt er á **Alltaf opið fyrir breytingar** í vistaða yfirlitinu. |
| 592344 |Launahluti starfsmanna í stöðu á að vera skrifvarinn þegar fríðindastjórnun er virkjuð | Launaupplýsingar starfsmanns eru búnar til með virkni eldri fríðinda.  Þegar fríðindastjórnun er virkjuð verða reitirnir skrifvarðir. Þegar kveikt er á fríðindastjórnun og **Fela eyðublöð eldri fríðinda** er stillt á **Já** í samnýttum færibreytum Human Resources verður flipinn **Laun starfsmanns** falinn. |
| 598617 | Virkjun á flipa í skjámynd **HcmDiscussion** veldur óendanlegri lykkju þegar sérstillingar eru notaðar | Þegar bæði hnitanetið og upplýsingayfirlitið eru með kveikt á **Alltaf opið fyrir breytingar** rekst kóðinn sem virkjar flipann í hnekkingaraðferð verks á við sérstillingu um hvaða stjórnun á að vera í fókus og býr til óendanlega lykkju. |
| 593553 | Reitur færslubókardagsetningar í frammistöðubókinni er sýndir í UTC | Reiturinn **Færslubókardagsetning** fyrir frammistöðubækur er sýndur í UTC-tíma frekar en tímabeltinu sem skilgreint er í uppsetningu kerfisdagsetningar sem veldur því að dagsetningin verði röng fyrir sum tímabelti. |
| 586930 | Að opna verkþætti fyrir afkastamarkmið opnar allt aðra færslu | Þegar eiginleikinn „Stækkað skýrsluyfirlit frammistöðubóka“ er virkjaður í eiginleikastjórnun mun val á afkastamarkmiðum fyrir stækkaðar skýrslur í flipanum **Teymið mitt** í **Sjálfsafgreiðsla starfsmanns** opna markmið fyrir starfsmann í staðinn fyrir valinn starfsmann. |
| 569959 |  Einingin HcmPositionWorkerAssignmentV2 úthlutar ekki starfsmanni á stöðu | Notendur fengu villu þegar þeir bættu við færslu stöðuúthlutunar í gegnum eininguna og útgáfa mistókst. |
| 582259 | VETS 4212 skýrsla notar 2017 eyðublaðið í stað 2020 eyðublaðsins | Uppfært í 2020 snið.  Til að hlaða inn nýja sniðinu skal fara í **Skilgreiningar skýrslu** og eyða VETS-4212 skýrslunni í vinstri dálknum. Farðu í **Rafræn skýrslugerð - Gagnageymslur - Tilföng Human Resources** og veldu **Opna**.  Veldu **VETS-4212 PDF-útprent** og veldu svo **Flytja inn**.|


## <a name="in-preview"></a>Í kynningarútgáfu

Eftirfarandi nýir eiginleikar eru í kynningarútgáfu. Nánari upplýsingar um hvernig eigi að kveikja og slökkva á eiginleikum er að finna í [Stjórna eiginleikum](hr-admin-manage-features.md).

| Eiginleiki | Útgáfuáætlun | Fylgiskjöl |
| --- | --- | --- |
| Vinnusvæði fríðindastjórnunar | [Vinnusvæði fríðindastjórnunar (forskoðun)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Vinnusvæði fríðindastjórnunar](hr-benefits-management-workspace.md) |
| Virkja einfalda launasamþættingu (API fyrir launasamþættingu) | [Virkja einfalda samþættingu við launaveitu](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Launasamþættingar-API](hr-admin-integration-payroll-api-introduction.md)|
|  Virkja fjarvistarstjóra til að stjórna fríi | [Virkja fjarvistarstjóra til að stjórna fríi](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) | [Skilgreina hlutverk fjarvistastjórnanda](https://go.microsoft.com/fwlink/?linkid=2168107)|
|  Skilgreina kröfu viðhengis á hverja leyfisgerð | [Skilgreina kröfu viðhengis á hverja leyfisgerð](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/mandate-attachments-specific-leave-types) |[Grunnstilla gerðir leyfis og fjarvista](https://go.microsoft.com/fwlink/?linkid=2168108)|
|  Stilla leyfiseiningar fyrir hverja leyfisgerð | [Stilla leyfiseiningar fyrir hverja leyfisgerð](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/configure-leave-units-per-leave-type) |[Grunnstilla gerðir leyfis og fjarvista](https://go.microsoft.com/fwlink/?linkid=2168215)|
| Gera kleift að merkja starfsmenn sem tilbúna að fá greitt | [Gera kleift að merkja starfsmenn sem tilbúna að fá greitt](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [Tilbúið til greiðslu](/dynamics365/human-resources/hr-compensation-payroll) |

## <a name="coming-soon"></a>Væntanlegt

| Eiginleiki | Upplýsingar |
| --- | --- |
| Verkvangsuppfærsla 10.0.20 (44) | Verkvangsuppfærsla 10.0.20 á að fara af stað í útgáfu 26. júlí 2021. Fyrir frekari upplýsingar, sjá [Uppfærslur á vettvangi fyrir útgáfu 10.0.20 af fjármála- og rekstraröppum (ágúst 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-20). |

Fyrir ítarlegan lista yfir áætlaða eiginleika og áætlaðar útgáfur þeirra skal skoða [Yfirlit yfir Dynamics 365 Human Resources 2021 losunarbylgju 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Sjá einnig

[Nýjungar eða breytingar í Mannauði](hr-admin-whats-new.md)</br>
[Yfirlit yfir Dynamics 365 Human Resources 2021 losunarbylgju 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Uppfærsluferli](hr-admin-setup-update-process.md)</br>
[Vinna með eiginleika](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

