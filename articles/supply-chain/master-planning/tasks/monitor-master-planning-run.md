---
title: Fylgjast með keyrslu áætlanagerðar
description: Í þessari grein er útskýrt hvernig skipuleggjandi framleiðslunnar getur séð hvort keyrsla aðaláætlanagerðar sé í gangi.
author: t-benebo
ms.date: 11/04/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, InventItemIdLookupSimple, ReqLog, ReqProcessTaskTrace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: da04ef95f2f7e411ecea3fadf7ff31b3502d3d99
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860755"
---
# <a name="monitor-a-master-planning-run"></a>Fylgjast með keyrslu áætlanagerðar

[!include [banner](../../includes/banner.md)]

## <a name="use-a-gantt-chart-to-visualize-master-planning-progress"></a>Notaðu Gantt myndrit til að sjá framvindu aðaláætlunargerðar

Af síðunni **Skoða framvindu aðaláætlunargerðar** geturðu skoðað upplýsingar um sögulegar keyrslur aðaláætlunargerðar sem Gantt kort. Þessi virkni getur hjálpað þér að skilja tímann sem er eytt í hina ýmsu áfanga aðaláætlunargerðar. Fyrir núverandi virkt skipulagsstarf er hægt að nota síðuna **Skoða framvindu aðaláætlunargerðar** til að fylgjast með framvindu mála og skoða þann áætlaða tíma sem eftir er.

### <a name="turn-the-master-plan-progress-visualization-feature-on-or-off"></a>Kveikja eða slökkva á eiginleika myndrænnar framsetningar á framvindu aðaláætlunar

Sem hluti af Supply Chain Management, útgáfa 10.0.21, er sjálfgefið kveikt á þessum eiginleika. Frá og með útgáfu 10.0.25 af Supply Chain Management er þessi eiginleiki skylda og ekki er hægt að slökkva á henni. Ef þú ert að keyra útgáfu sem er eldri en 10.0.25, þá geta stjórnendur kveikt eða slökkt á þessum eiginleika með því að leita að eiginleikanum *Myndræn framsetning á ferli aðaláætlanagerðar* á vinnusvæðinu [Eiginleikastjórnun](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="use-the-master-plan-progress-visualization-feature"></a>Nota eiginleika myndrænnar framsetningar á framvindu aðaláætlunar

Síðan **Skoða framvindu aðaláætlunargerðar** getur sýnt bæði sögulegar vinnslur áætlunargerðar og virkar vinnslur áætlunargerðar. 

Það eru tveir möguleikar til að skoða sögulegar áætlunarvinnslur. 

1. Farðu í **Aðaláætlunargerð \> Uppsetning \> Áætlanir \> Aðaláætlanir** og veldu síðan á aðgerðarrúðunni **Saga**. Veldu þá vinnslu sem þú vilt velja, veldu **Fyrirspurnir** og veldu síðan **Skoða framvindu**
1. Farðu í **Aðaláætlanagerð \> Vinnusvæði \> Aðaláætlunargerð**, í aðaláætlunargerðarreitnum smellirðu á **Saga**. Veldu þá vinnslu sem þú vilt velja, veldu **Fyrirspurnir** og veldu síðan **Skoða framvindu**

Það eru tveir möguleikar til að skoða virkar áætlunarvinnslur. 
1. Farðu í **Aðaláætlunargerð \> Vinnusvæði \> Aðaláætlunargerð**, veldu á aðgerðarglugganum **Óunnið áætlunarferli**. Veldu þá vinnslu sem þú vilt velja, veldu **Fyrirspurnir** og veldu síðan **Skoða framvindu**.
1. Farðu í **Aðaláætlanagerð \> Vinnusvæði \> Aðaláætlunargerð**, í aðaláætlunargerðarreitnum smellirðu á **Skoða framvindu**. Veldu þá vinnslu sem þú vilt velja, veldu **Fyrirspurnir** og veldu síðan **Skoða framvindu**

Athugaðu að þú getur aðeins skoðað virk störf þegar áætlunargerðarvinnsla er í gangi.

### <a name="analyze-a-master-planning-job"></a>Greindu vinnslu aðaláætlunargerðar

Í Gantt töflunni geturðu stækkað sérhvert eftirfarandi skipulagsferla til að skoða frekari upplýsingar um tímann sem er varið:

- Frumstilling
- Gögnum eytt og bætt við
- Þekjuáætlun
- Seinkanir
- Aðgerðaboð
- Lok
- Sjálfvirk staðfesting

Gantt taflan er gagnlegt tól ef þú vilt skoða áhrifin af því að nota aðgerðarskilaboð.

#### <a name="navigation-in-the-gantt-chart"></a>Leiðsögn í Gantt töflunni

- Til að stækka valinn hóp og sýna smáatriðin, veldu plúsmerki (**+**) í trjásýninni.
- Til að fella hópinn sem valinn er saman skaltu velja mínustáknið (**-**) í trjásýninni.
- Þú getur notað lyklaborðið þitt til að fletta. Notaðu takkana **Upp-ör** og **Niður-ör** til að fara á milli lína. Notaðu takkana **Hægri-ör** og **Vinstri-ör** til að stækka og fella saman hópa.
- Til að opna eða loka öllum stigum í Gantt töflunni velurðu **Stækka allt** eða **Fella allt saman**.
- Til að skoða tengdan vinnslutíma heldurðu músarbendlinum yfir verki. (Verk eru lægsta stigið í Gantt töflunni.)

#### <a name="view-an-additional-master-planning-run-to-compare-jobs"></a>Skoða viðbótarkeyrslu aðaláætlunargerðar til að bera saman störf

Með því að velja vinnslu aðaláætlunargerðar í reitnum **Sýna viðbótarkeyrslu aðaláætlunargerðar** geturðu skoðað viðbótarkeyrslu aðaláætlunargerðar í Gantt töflunni og borið saman vinnslurnar tvær.

#### <a name="bom-level-display"></a>BOM-stig skjár

Uppskriftarstig (BOM) eru sýnd á annan hátt vegna þekjuáætlanagerðar, tafa, aðgerða og styrkingar.

- **Þekjuáætlanagerð** - BOM-stig eru sýnd eins og búist var við. Þau eru reiknuð frá toppi og niður.

    **Dæmi:** BOM stig 0, 1, 2

- **Tafir** - BOM stig eru sýnd sem umfang áætlunar BOM margfaldað með –1. (Með öðrum orðum, þau hafa neikvætt merki.)

    **Dæmi:** BOM stig –2, –1, 0

- **Aðgerðaskilaboð** - BOM-stig eru sýnd eins og búist var við. Þau eru reiknuð frá toppi og niður.

    **Dæmi:** BOM stig 0, 1, 2

- **Sjálfvirk styrking** - BOM stig eru sýnd sem 999 að frádregnu BOM-stigi þekjuáætlunargerðar.

    **Dæmi:** BOM stig 999, 998, 997

Eftirfarandi tafla dregur saman hegðunina.

| BOM stig sem er sýnt | Endanleg vara | Undiríhlutur | Hráefni |
|---|---|---|---|
| Þekjuáætlun | 0 | 1 | 2 |
| Seinkanir | 0 | –1 | –2 |
| Aðgerðaboð | 0 | 1 | 2 |
| Sjálfvirk staðfesting | 999 | 998 | 997 |

#### <a name="visualize-progress"></a>Gera framvindu sýnilega

Ef þú skoðar vinnslu aðaláætlunargerðar sem er í gangi er framvinda sýnd með litum í Gantt töflunni. Eftirfarandi litir eiga við um bláa þemað. Fyrir önnur litaþemu eru litirnir aðrir.

- **Dökkblátt** - Lokin áætlunarverk.
- **Appelsínugult** - Verkið sem nú er í vinnslu.
- **Ljósblátt** - Mat á verkum sem eftir eru.

Liturinn er aðeins sýndur á lægsta stiginu í Gantt töflunni. Veldu **Auka allt** að skoða öll verk í vinnslu aðaláætlunargerðar. Mat á verkum sem eftir eru byggist á sögulegum vinnslu aðaláætlunargerðar.

## <a name="run-master-planning-and-track-processing-time"></a>Keyra aðaláætlunargerð og fylgjast með vinnslutíma

1. Veldu á sjálfgefna mælaborðinu **Aðaláætlunargerð**.
1. Í reitinn **Áætlun** slærðu inn eða velur gildi.
1. Veljið **Keyra**.
1. Stilltu valkostinn **Rekja vinnslutíma** á **Já**.
1. Í reitinn **Fjöldi þráða** skal færa inn tölu.
1. Á flýtiflipanum **Færslur til að hafa með** velurðu **Sía**.
1. Veldu línuna þar sem reiturinn **Reitur** er stilltur á **Vörunúmer**.
1. Í reitinn **Skilyrði** skal slá inn gildi.
1. Veljið **Í lagi**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]