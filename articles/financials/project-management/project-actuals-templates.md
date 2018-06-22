---
title: "Samstilla rauntölur verks beint frá Project Service Automation til færslubókar verksamþættingar til að bóka í Finance and Operations"
description: "Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verk sem notuð eru til að samstilla rauntölur verks beint úr Microsoft Dynamics 365 for Project Service Automation við Dynamics 365 for Finance and Operations."
author: KimANelson
manager: AnnBe
ms.date: 05/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: 85ff049852e0b00623f47a12fb66e2c9bb9c4151
ms.contentlocale: is-is
ms.lasthandoff: 05/29/2018

---
# <a name="synchronize-project-actuals-from-project-service-automation-directly-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a>Samstilla rauntölur verks beint frá Project Service Automation til færslubókar verksamþættingar til að bóka í Finance and Operations

Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verk sem notuð eru til að samstilla rauntölur verks beint úr Microsoft Dynamics 365 for Project Service Automation við Dynamics 365 for Finance and Operations.

Sniðmátið samstillir færslur frá Project Service Automation inn í millistigsvistunartöflu í Finance and Operations. Eftir að samstillingunni er lokið verður þú að flytja inn frá millistigsvistunartöflunni í færslubók samþættingar.

> [!NOTE]
> Samþætting á rauntölum verks er í boði í Dynamics 365 for Finance and Operations útgáfu 8.01.

> [!NOTE]
> Ef þú ert að slá inn upphæð virðisaukaskatts fyrir tíma- eða kostnaðarfærslur í Project Service Automation verður þú að setja upp uppfærslu 7 af Project Service Automation. Ef þessi uppfærsla er ekki uppsett verða rauntölur skatts ekki tengdar við tengdar rauntölur fyrir tíma- eða kostnaðarfærslur og munu þær ekki verða samstilltar við Finance and Operations. Hafa skal samband við notendaþjónustu fyrir frekari upplýsingar.


## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>Gagnaflæði fyrir Project Service Automation til Finance and Operations

Samþættingarlausn Project Service Automation við Finance and Operations notar eiginleika gagnasamþættingar til að samstilla gögn þvert yfir tilvik af Project Service Automation og Finance and Operations. Samþættingarsniðmátin sem eru tiltæk með eiginleika gagnasamþættingar gera gögnum kleift að flæða varðandi rauntölur verks frá Project Service Automation til Finance and Operations.

Eftirfarandi skýringarmynd sýnir hvernig gögnin eru samstillt milli Project Service Automation og Finance and Operations.

[![Gagnaflæði fyrir samþættingu Project Service Automation við Finance and Operations](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)


## <a name="templates-and-tasks"></a>Sniðmát og verkefni

Til að fá aðgang að tiltækum sniðmátum, í stjórnendamiðstöð Microsoft PowerApps, skal velja **Verk** og síðan í efra hægra horninu skal velja **Nýtt verk** til að velja almenn sniðmát.

Eftirfarandi sniðmát og undirliggjandi verkefni eru notuð til að samstilla rauntölur verks frá Project Service Automation til Finance and Operations:

-  **Heiti sniðmátsins í gagnasamþættingu:** Rauntölur verks (PSA til Fin and Ops)

-  **Heiti verkefna í verkinu:** 
    - Rauntölur 
    - TransactionConnections

## <a name="entity-set"></a>Einingastamstæða

| Project Service Automation      | Finance and Operations                                      |
|---------------------------------|-------------------------------------------------------------|
| Rauntölur                         | Samþættingareining fyrir rauntölur verks                      |
| Færslutengingar         | Samþættingareining fyrir vensl verkfærsla    |

## <a name="entity-flow"></a>Einingaflæði

Rauntölum verks er stjórnað í Project Service Automation og þær eru samstilltar við Finance and Operations við færslubók verksamþættingar. Bókhaldið verður notað á grundvelli sjálfgefinna fjárhagsvídda og uppsetningu bókunar.

## <a name="preconditions"></a>Skilyrði

Áður en samstilling á rauntölum getur átt sér stað verður þú að grunnstilla samþættingarfæribreytur Project Service Automation og samstilla flokka fyrir verk, verkefni verks og kostnaðarfærslur verks.

## <a name="power-query"></a>Power Query

Þú verður að nota Microsoft Power Query í sniðmáti fyrir rauntölur verks til að:
- Umbreyta **færslugerð** Project Service Automation í rétta **færslugerð** í Finance and Operations. Sniðmát fyrir rauntölur verks (PSA til Fin and Ops) hefur nú þegar skilgreint þessa umbreytingu.
- Umbreyta **reikningsgerð** Project Service Automation í rétta **reikningsgerð** í Finance and Operations. Sniðmát fyrir rauntölur verks (PSA til Fin and Ops) hefur nú þegar skilgreint þessa umbreytingu. Reikningsgerðinni er síðan varpað í **línueiginleika** byggt á grunnstillingu í sniði fyrir samþættingarfæribreytur Dynamics 365 for Project Service Automation.
- Sía í tilteknar **Fyrirtækiseiningar tilfangs** sem á að samstilla við þetta sniðmát.
- Ef **tími eða rauntölur kostnaðar innan samstæðu** verða samstilltar við Finance and Operations verður þú að umbreyta **fyrirtækiseiningu samnings** í réttan **lögaðila** í Finance and Operations. Sniðmátið fyrir rauntölur verks (PSA til Fin and Ops) hefur skilyrtan dálk sem er skilgreindur á grundvelli sýnigagna. Þú verður að uppfæra síðasta innslegna skilyrðið fyrir rétta lögaðila. Ef ekki tekst að gera þetta getur það leitt til annað hvort samþættingarvillu eða að rangar rauntölufærslur verði fluttar inn í Financce and Operations.
- Ef **tími eða rauntölur kostnaðar innan samstæðu** verða ekki samstilltar við Finance and Operations verður þú að eyða síðasta innsetta skilyrta dálknum úr sniðmátinu þínu. Ef ekki tekst að gera þetta getur það leitt til annað hvort samþættingarvillu eða að rangar rauntölufærslur verði fluttar inn í Financce and Operations.

### <a name="contract-organizational-unit"></a>Fyrirtækiseining samnings
Til að uppfæra innsetta skilyrta dálkinn í sniðmátinu skal smella á örina **Varpa** til að opna vörpunina. Veldu til að opna Advanced Query and Filtering.
- Ef þú notar sniðmát fyrir sjálfgefnar rauntölur Microsoft Project (PSA til Fin and Ops) skaltu velja síðasta **Innslegna skilyrðið** í hlutanum **Notuð skref**. Í færslunni **Aðgerð** skaltu skipta út **USSI** fyrir heitið á **Lögaðilanum** sem ætti að nota með samþættingunni. Bæta viðbótarskilyrðum eftir þörfum við færsluna **Aðgerð** og uppfæra skilyrðið **annars** frá **USMF** í réttan **Lögaðila**.
- Ef þú ert að búa til nýtt sniðmát þarftu að bæta við þessum dálki til að styðja við tíma og kostnað innan samstæðu. Veldu **Bæta við skilyrtum dálki** og gefðu dálknum heiti á borð við LegalEntity. Sláðu inn skilyrðið fyrir dálkinn þar sem ef msdyn_contractorganizationalunitid.msdyn_name er <organizational unit>, þá <enter the Legal entity>; annars núll.

## <a name="template-mapping-in-data-integration"></a>Sniðmátsvörpun í Gagnasamþættingu

Eftirfarandi skýringarmynd sýnir dæmi um vörpunarsniðmát í gagnasamþættingu. Vörpunin sýnir reitaupplýsingarnar sem verða samstilltar frá Project Service Automation við Finance and Operations.

[![Kortlagning sniðmáts](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)

[![Kortlagning sniðmáts](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)

## <a name="import-from-staging-table"></a>Flytja inn úr millistigsvistunartöflu

Innflutningur frá reglubundnu ferli millistigsvistunartöflu verður að keyra á eftir samstillingu á rauntölum frá Project Service Automation við Finance and Operations. Þetta ferli mun flytja inn verkfærslur frá millistigsvistunartöflunni í færslubók fyrir samþættingu Project Service Automation þar sem bókhaldið er notað og hægt er að bóka innfluttar færslur. Mælt er með því að þú keyrir þetta ferli í runustillingu og sem hægt er að setja upp valfrjálst til að keyra sem endurtekna runu.

## <a name="update-actuals"></a>Uppfæra rauntölur

Eftirfarandi sniðmát og undirliggjandi verk eru notuð til að samstilla fylgiskjalsnúmerið og virðisaukaskattinn fyrir bókaðar verkfærslur frá Finance and Operations til Project Service Automation:

-  **Heiti sniðmátsins í gagnasamþættingu:** Uppfærsla á rauntölum verks (Fin Ops til PSA)
-  **Heiti verkefna í verkinu:** 
     - Rauntölur 
     - TransactionConnections

## <a name="entity-set"></a>Einingastamstæða

| Finance and Operations                                         | Project Service Automation        |
|----------------------------------------------------------------|-----------------------------------|
| Samþættingareining fyrir rauntölur verks                         | Rauntölur                           |
| Samþættingareining fyrir vensl verkfærsla       | Færslutengingar           |

## <a name="entity-flow"></a>Einingaflæði

Rauntölum verks er stjórnað í Project Service Automation og þær eru samstilltar við Finance and Operations við færslubók verksamþættingar. Þegar þær eru bókaðar í Finance and Operations eru rauntölurnar uppfærðar í Project Service Automation með fylgiskjalsnúmerinu frá Finance and Operations. Ef virðisaukasköttum var bætt við í Finance and Operations verða nýjar rauntölur skatts búnar til í Project Service Automation.

## <a name="power-query"></a>Power Query

Þú verður að nota Microsoft Power Query í sniðmáti fyrir uppfærslu á rauntölum verks til að:
- Umbreyta **færslugerð** Finance and Operations í rétta **færslugerð** í Project Service Automation. Uppfærsla á sniðmáti fyrir rauntölur verks (Fin and Ops til PSA) hefur nú þegar þessa umbreytingu skilgreinda.
- Umbreyta **reikningsgerð** Finance and Operations í rétta **reikningsgerð** í Project Service Automation. Uppfærsla á sniðmáti fyrir rauntölur verks (Fin and Ops til PSA) hefur nú þegar þessa umbreytingu skilgreinda.

## <a name="template-mapping-in-data-integration"></a>Sniðmátsvörpun í Gagnasamþættingu

Eftirfarandi skýringarmyndir sýna dæmi um vörpunarsniðmát í gagnasamþættingu. Vörpunin sýnir reitaupplýsingarnar sem verða samstilltar frá Finance and Operations við Project Service Automation.

[![Kortlagning sniðmáts](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)

[![Kortlagning sniðmáts](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)




