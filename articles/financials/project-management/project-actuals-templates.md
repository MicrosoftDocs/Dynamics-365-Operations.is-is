---
title: Samstilla rauntölur verks beint frá Project Service Automation til færslubókar verksamþættingar til að bóka í Finance and Operations
description: Þetta efnisatriði fjallar um sniðmát og undirliggjandi verkefni sem notuð eru til að samstilla verkefni verks beint frá Microsoft Dynamics 365 for Project Service Automation til Microsoft Dynamics 365 for Finance and Operations.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 0a965e8de596decf39a15977e6df8a6aa9dd35b0
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "343352"
---
# <a name="synchronize-project-actuals-directly-from-project-service-automation-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a>Samstilla rauntölur verks beint frá Project Service Automation til færslubókar verksamþættingar til að bóka í Finance and Operations

[!include[banner](../includes/banner.md)]

Þetta efnisatriði fjallar um sniðmát og undirliggjandi verkefni sem notuð eru til að samstilla verkefni verks beint frá Microsoft Dynamics 365 for Project Service Automation til Microsoft Dynamics 365 for Finance and Operations.

Sniðmátið samstillir færslur frá Project Service Automation inn í millistigsvistunartöflu í Finance and Operations. Eftir að samstillingunni er lokið **verður** þú að flytja inn gögnin frá millistigsvistunartöflunni í færslubók samþættingar.

> [!NOTE]
> - Samþætting á rauntölum verks er í boði í Microsoft Dynamics 365 for Finance and Operations útgáfu 8.0.1 eða síðar.
> - Ef þú notar Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3.0, eftir að hafa sett upp KB 4132657 og KB 4132660 getur þú notað sniðmátin til að samþætta verkefni fyrir verk, kostnaðarfærsluflokka, tímaáætlanir, kostnaðaráætlanir og rauntölur og til að stilla virknilæsingu. Ef þú verður að endurstilla dreifingu á fjárhagsupphæð mælum við með að þú setjir einnig upp KB 4131710.
> - Ef þú notar Finance and Operations 7.3.0 og þú færir þóknunarfærslur yfir frá Project Service Automation verður þú að setja upp KB 4345320 til þess að geta tekið við þessum þóknunum í verkreikningi.
> - Ef þú slærð inn upphæð virðisaukaskatts fyrir tíma- eða kostnaðarfærslur í Project Service Automation verður þú að setja upp uppfærslu 7 af Project Service Automation. Annars verða rauntölur skatts ekki tengdar við tengdar rauntölur fyrir tíma- eða kostnaðarfærslur og munu þær ekki verða samstilltar við Finance and Operations. Hafa skal samband við notendaþjónustu fyrir frekari upplýsingar.

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>Gagnaflæði fyrir Project Service Automation til Finance and Operations

Samþættingarlausn Project Service Automation við Finance and Operations notar eiginleika gagnasamþættingar til að samstilla gögn þvert yfir tilvik af Project Service Automation og Finance and Operations. Samþættingarsniðmátin sem eru tiltæk með eiginleika gagnasamþættingar gera gögnum kleift að flæða varðandi rauntölur verks frá Project Service Automation til Finance and Operations.

Eftirfarandi skýringarmynd sýnir hvernig gögnin eru samstillt milli Project Service Automation og Finance and Operations.

[![Gagnaflæði fyrir samþættingu Project Service Automation við Finance and Operations](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)

## <a name="project-actuals-from-project-service-automation"></a>Rauntölur verks fyrir Project Service Automation

### <a name="template-and-tasks"></a>Sniðmát og verkefni

Til að fá aðgang að tiltækum sniðmátum, í stjórnendamiðstöð Microsoft PowerApps, skal velja **Verk** og síðan í efra hægra horninu skal velja **Nýtt verk** til að velja almenn sniðmát.

Eftirfarandi sniðmát og undirliggjandi verkefni eru notuð til að samstilla rauntölur verks frá Project Service Automation til Finance and Operations:

- **Heiti sniðmátsins í gagnasamþættingu:** Rauntölur verks (PSA til Fin and Ops)
- **Heiti verkefna í verkinu:**

    - Rauntölur
    - TransactionConnections

### <a name="entity-set"></a>Einingastamstæða

| Project Service Automation | Finance and Operations                                   |
|----------------------------|----------------------------------------------------------|
| Rauntölur                    | Samþættingareining fyrir rauntölur verks                   |
| Færslutengingar    | Samþættingareining fyrir vensl verkfærsla |

### <a name="entity-flow"></a>Einingaflæði

Rauntölum verks er stjórnað í Project Service Automation og þær eru samstilltar við færslubók verksamþættingar í Finance and Operations. Bókhaldið verður notað á grundvelli sjálfgefinna fjárhagsvídda og uppsetningu bókunarinnar.

### <a name="prerequisites"></a>Frumskilyrði

Áður en samstilling á rauntölum getur átt sér stað verður þú að grunnstilla samþættingarfæribreytur Project Service Automation og samstilla flokka fyrir verk, verkefni verks og kostnaðarfærslur verks.

### <a name="power-query"></a>Power Query

Þú verður að nota Microsoft Power Query fyrir Excel í sniðmáti fyrir rauntölur verks til að ljúka þessum verkefnum:

- Umbreyta færslugerð í Project Service Automation í rétta færslugerð í Finance and Operations. Umbreytingin er þegar skilgreind í sniðmáti fyrir rauntölur verks (PSA til Fin and Ops).
- Umbreyta reikningsgerð í Project Service Automation yfir í rétta reikningsgerð í Finance and Operations. Umbreytingin er þegar skilgreind í sniðmáti fyrir rauntölur verks (PSA til Fin and Ops). Reikningsgerðinni er síðan varpað í línueiginleika byggt á grunnstillingu á síðunni **Samþættingarfæribreytur Project Service Automation**.
- Sía í tilteknar fyrirtækiseiningar tilfangs sem þarf að samstilla við þetta sniðmát.
- Ef tími eða rauntölur kostnaðar innan samstæðu verða samstilltar við Finance and Operations verður þú að umbreyta fyrirtækiseiningu samnings í réttan lögaðila í Finance and Operations. Í sniðmáti fyrir rauntölur verks (PSA til Fin and Ops) er skilyrtur dálkur skilgreindur á grundvelli sýnigagna. Þú verður að uppfæra síðasta innslegna skilyrðið fyrir rétta lögaðila. Annars getur annaðhvort samþættingarvilla komið upp eða að rangar rauntölufærslur verði fluttar inn í Finance and Operations.
- Ef tími eða rauntölur kostnaðar innan samstæðu verða ekki samstilltar við Finance and Operations verður þú að eyða síðasta innsetta skilyrta dálknum úr sniðmátinu þínu. Annars getur annaðhvort samþættingarvilla komið upp eða að rangar rauntölufærslur verði fluttar inn í Finance and Operations.

#### <a name="contract-organizational-unit"></a>Fyrirtækiseining samnings
Til að uppfæra innsetta skilyrta dálkinn í sniðmátinu skal smella á örina **Varpa** til að opna vörpunina. Veldu tengilinn **Ítarleg fyrirspurn og síun** til að opna Power Query.

- Ef þú notar sniðmát fyrir sjálfgefnar rauntölur verks (PSA til Fin and Ops) í Power Query, skaltu velja síðasta **Innslegna skilyrðið** í hlutanum **Notuð skref**. Í færslunni **Aðgerð** skaltu skipta út **USSI** fyrir heitið á lögaðilanum sem ætti að nota með samþættingunni. Bæta viðbótarskilyrðum við færsluna **Aðgerð** eftir þörfum og uppfæra skilyrðið **annars** frá **USMF** í réttan lögaðila.
- Ef þú ert að búa til nýtt sniðmát þarftu að bæta dálkinum við til að styðja við tíma og kostnað innan samstæðu. Veldu **Bæta við skilyrtum dálki** og gefðu dálknum heiti á borð við **LegalEntity**. Sláðu inn skilyrði fyrir dálkinn þar sem ef **msdyn\_contractorganizationalunitid.msdyn\_heitið** er \<fyrirtækiseining\>, þá \<sláðu inn lögaðila\>; annars núll.

### <a name="template-mapping-in-data-integration"></a>Sniðmátsvörpun í Gagnasamþættingu

Eftirfarandi skýringarmynd sýnir dæmi um vörpunarsniðmát í gagnasamþættingu. Vörpunin sýnir reitaupplýsingarnar sem verða samstilltar frá Project Service Automation við Finance and Operations.

[![Kortlagning sniðmáts](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)

[![Kortlagning sniðmáts](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)

## <a name="import-from-staging-table-after-integration-from-project-service-automation"></a>Flytja inn úr millistigsvistunartöflu eftir samþættingu frá Project Service Automation

Innflutningur frá reglubundnu ferli millistigsvistunartöflu verður að keyra á eftir samstillingu á rauntölum frá Project Service Automation við Finance and Operations. Þetta ferli mun flytja inn verkfærslur frá millistigsvistunartöflunni í færslubók fyrir samþættingu Project Service Automation þar sem bókhaldið er notað og hægt er að bóka innfluttar færslur. Mælt er með því að þú keyrir þetta ferli í runustillingu og sem hægt er að setja upp valfrjálst til að keyra sem endurtekna runu.

## <a name="update-actuals-from-finance-and-operations"></a>Uppfæra rauntölur frá Finance and Operations

### <a name="template-and-tasks"></a>Sniðmát og verkefni

Eftirfarandi sniðmát og undirliggjandi verk eru notuð til að samstilla fylgiskjalsnúmerið og virðisaukaskattinn fyrir bókaðar verkfærslur frá Finance and Operations til Project Service Automation:

- **Heiti sniðmátsins í gagnasamþættingu:** Uppfærsla á rauntölum verks (Fin Ops til PSA)
- **Heiti verkefna í verkinu:**

    - Rauntölur 
    - TransactionConnections

### <a name="entity-set"></a>Einingastamstæða

| Finance and Operations                                   | Project Service Automation |
|----------------------------------------------------------|----------------------------|
| Samþættingareining fyrir rauntölur verks                   | Rauntölur                    |
| Samþættingareining fyrir vensl verkfærsla | Færslutengingar    |

### <a name="entity-flow"></a>Einingaflæði

Rauntölum verks er stjórnað í Project Service Automation og þær eru samstilltar við færslubók verksamþættingar í Finance and Operations. Þegar rauntölur eru bókaðar í Finance and Operations eru þær uppfærðar í Project Service Automation með fylgiskjalsnúmerinu frá Finance and Operations. Ef virðisaukasköttum var bætt við í Finance and Operations verða nýjar rauntölur skatts búnar til í Project Service Automation.

### <a name="power-query"></a>Power Query

Þú verður að nota Power Query fyrir Excel í uppfærðu sniðmáti fyrir rauntölur verks til að ljúka þessum verkefnum:

- Umbreyta færslugerð í Finance and Operations í rétta færslugerð í Project Service Automation. Þessi umbreyting er þegar skilgreind í uppfærðu sniðmáti fyrir rauntölur verks (Fin and Ops til PSA).
- Umbreyta reikningsgerð í Finance and Operations yfir í rétta reikningsgerð í Project Service Automation. Þessi umbreyting er þegar skilgreind í uppfærðu sniðmáti fyrir rauntölur verks (Fin and Ops til PSA).

### <a name="template-mapping-in-data-integration"></a>Sniðmátsvörpun í Gagnasamþættingu

Eftirfarandi skýringarmyndir sýna dæmi um vörpunarsniðmát í gagnasamþættingu. Vörpunin sýnir reitaupplýsingarnar sem verða samstilltar frá Finance and Operations við Project Service Automation.

[![Kortlagning sniðmáts](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)

[![Kortlagning sniðmáts](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)
