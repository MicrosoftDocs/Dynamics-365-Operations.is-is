---
title: Samstilla rauntölur verks beint frá Project Service Automation til færslubókar verksamþættingar til að bóka í Finance and Operations
description: Þetta efnisatriði fjallar um sniðmát og undirliggjandi verkefni sem notuð eru til að samstilla raunverk beint úr Microsoft Dynamics 365 Project Service Automation við Finance and Operations.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 302ac0f456dd8a24dc02948ee657e359f5a9c844
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770336"
---
# <a name="synchronize-project-actuals-directly-from-project-service-automation-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a>Samstilla rauntölur verks beint frá Project Service Automation til færslubókar verksamþættingar til að bóka í Finance and Operations

[!include[banner](../includes/banner.md)]

Þetta efnisatriði fjallar um sniðmát og undirliggjandi verkefni sem notuð eru til að samstilla verkefni verks beint frá Dynamics 365 Project Service Automation til Dynamics 365 Finance.

Sniðmátið samstillir færslur frá Project Service Automation inn í millistigsvistunartöflu í Finance. Eftir að samstillingunni er lokið **verður** þú að flytja inn gögnin frá millistigsvistunartöflunni í færslubók samþættingar.

> [!NOTE]
> - Samþætting á rauntölum verks er í boði frá og með útgáfu 8.0.1.
> - Ef þú notar Enterprise Edition 7.3.0 eftir að hafa sett upp KB 4132657 og KB 4132660 getur þú notað sniðmátin til að samþætta verkefni fyrir verk, kostnaðarfærsluflokka, tímaáætlanir, kostnaðaráætlanir og rauntölur og til að stilla virknilæsingu. Ef þú verður að endurstilla dreifingu á fjárhagsupphæð mælum við með að þú setjir einnig upp KB 4131710.
> - Ef þú notar útgáfu 7.3.0 og þú færir þóknunarfærslur yfir frá Project Service Automation verður þú að setja upp KB 4345320 til þess að geta tekið við þessum þóknunum í verkreikningi.
> - Ef þú slærð inn upphæð virðisaukaskatts fyrir tíma- eða kostnaðarfærslur í Project Service Automation verður þú að setja upp uppfærslu 7 af Project Service Automation. Annars verða rauntölur skatts ekki tengdar við tengdar rauntölur fyrir tíma- eða kostnaðarfærslur og munu þær ekki verða samstilltar við Finance. Hafa skal samband við notendaþjónustu fyrir frekari upplýsingar.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Gagnaflæði fyrir Project Service Automation til Finance

Samþættingarlausn Project Service Automation við Finance notar eiginleika gagnasamþættingar til að samstilla gögn þvert yfir tilvik af Project Service Automation og Finance. Samþættingarsniðmátin sem eru tiltæk með eiginleika gagnasamþættingar gera gögnum kleift að flæða varðandi rauntölur verks frá Project Service Automation til Finance.

Eftirfarandi skýringarmynd sýnir hvernig gögnin eru samstillt milli Project Service Automation og Finance.

[![Gagnaflæði fyrir samþættingu Project Service Automation við Finance and Operations](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)

## <a name="project-actuals-from-project-service-automation"></a>Rauntölur verks fyrir Project Service Automation

### <a name="template-and-tasks"></a>Sniðmát og verkefni

Til að fá aðgang að tiltækum sniðmátum, í stjórnendamiðstöð Microsoft Power Apps, skal velja **Verk** og síðan í efra hægra horninu skal velja **Nýtt verk** til að velja almenn sniðmát.

Eftirfarandi sniðmát og undirliggjandi verk eru notuð til að samstilla raunverk úr Project Service Automation við Finance:

- **Heiti sniðmátsins í gagnasamþættingu:** Rauntölur verks (PSA til Fin and Ops)
- **Heiti verkefna í verkinu:**

    - Rauntölur
    - TransactionConnections

### <a name="entity-set"></a>Einingastamstæða

| Project Service Automation | Fjármál                                   |
|----------------------------|----------------------------------------------------------|
| Rauntölur                    | Samþættingareining fyrir rauntölur verks                   |
| Færslutengingar    | Samþættingareining fyrir vensl verkfærsla |

### <a name="entity-flow"></a>Einingaflæði

Rauntölum verks er stjórnað í Project Service Automation og þær eru samstilltar við færslubók verksamþættingar í Finance. Bókhaldið verður notað á grundvelli sjálfgefinna fjárhagsvídda og uppsetningu bókunarinnar.

### <a name="prerequisites"></a>Frumskilyrði

Áður en samstilling á rauntölum getur átt sér stað verður þú að grunnstilla samþættingarfæribreytur Project Service Automation og samstilla flokka fyrir verk, verkefni verks og kostnaðarfærslur verks.

### <a name="power-query"></a>Power Query

Þú verður að nota Microsoft Power Query fyrir Excel í sniðmáti fyrir rauntölur verks til að ljúka þessum verkefnum:

- Umbreyta færslugerð í Project Service Automation í rétta færslugerð í Finance. Umbreytingin er þegar skilgreind í sniðmáti fyrir rauntölur verks (PSA til Fin and Ops).
- Umbreyta reikningsgerð í Project Service Automation yfir í rétta reikningsgerð í Finance. Umbreytingin er þegar skilgreind í sniðmáti fyrir rauntölur verks (PSA til Fin and Ops). Reikningsgerðinni er síðan varpað í línueiginleika byggt á grunnstillingu á síðunni **Samþættingarfæribreytur Project Service Automation**.
- Sía í tilteknar fyrirtækiseiningar tilfangs sem þarf að samstilla við þetta sniðmát.
- Ef tími eða rauntölur kostnaðar innan samstæðu verða samstilltar við Finance verður þú að umbreyta fyrirtækiseiningu samnings í réttan lögaðila í Finance. Í sniðmáti fyrir rauntölur verks (PSA til Fin and Ops) er skilyrtur dálkur skilgreindur á grundvelli sýnigagna. Þú verður að uppfæra síðasta innslegna skilyrðið fyrir rétta lögaðila. Annars getur annaðhvort samþættingarvilla komið upp eða að rangar rauntölufærslur verði fluttar inn í Finance.
- Ef tími eða rauntölur kostnaðar innan samstæðu verða ekki samstilltar við Finance verður þú að eyða síðasta innsetta skilyrta dálknum úr sniðmátinu þínu. Annars getur annaðhvort samþættingarvilla komið upp eða að rangar rauntölufærslur verði fluttar inn í Finance.

#### <a name="contract-organizational-unit"></a>Fyrirtækiseining samnings
Til að uppfæra innsetta skilyrta dálkinn í sniðmátinu skal smella á örina **Varpa** til að opna vörpunina. Veldu tengilinn **Ítarleg fyrirspurn og síun** til að opna Power Query.

- Ef þú notar sniðmát fyrir sjálfgefnar rauntölur verks (PSA til Fin and Ops) í Power Query, skaltu velja síðasta **Innslegna skilyrðið** í hlutanum **Notuð skref**. Í færslunni **Aðgerð** skaltu skipta út **USSI** fyrir heitið á lögaðilanum sem ætti að nota með samþættingunni. Bæta viðbótarskilyrðum við færsluna **Aðgerð** eftir þörfum og uppfæra skilyrðið **annars** frá **USMF** í réttan lögaðila.
- Ef þú ert að búa til nýtt sniðmát þarftu að bæta dálkinum við til að styðja við tíma og kostnað innan samstæðu. Veldu **Bæta við skilyrtum dálki** og gefðu dálknum heiti á borð við **LegalEntity**. Sláðu inn skilyrði fyrir dálkinn þar sem ef **msdyn\_contractorganizationalunitid.msdyn\_heitið** er \<fyrirtækiseining\>, þá \<sláðu inn lögaðila\>; annars núll.

### <a name="template-mapping-in-data-integration"></a>Sniðmátsvörpun í Gagnasamþættingu

Eftirfarandi skýringarmynd sýnir dæmi um vörpunarsniðmát í gagnasamþættingu. Vörpunin sýnir reitaupplýsingarnar sem verða samstilltar frá Project Service Automation við Finance.

[![Kortlagning sniðmáts](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)

[![Kortlagning sniðmáts](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)

## <a name="import-from-staging-table-after-integration-from-project-service-automation"></a>Flytja inn úr millistigsvistunartöflu eftir samþættingu frá Project Service Automation

Innflutningur frá reglubundnu ferli millistigsvistunartöflu verður að keyra á eftir samstillingu á rauntölum frá Project Service Automation við Finance. Þetta ferli mun flytja inn verkfærslur frá millistigsvistunartöflunni í færslubók fyrir samþættingu Project Service Automation þar sem bókhaldið er notað og hægt er að bóka innfluttar færslur. Mælt er með því að þú keyrir þetta ferli í runustillingu; hægt er að setja það upp valfrjálst til að keyra sem endurtekna runu.

## <a name="update-actuals-from-finance"></a>Uppfæra raunfærslur frá Finance

### <a name="template-and-tasks"></a>Sniðmát og verkefni

Eftirfarandi sniðmát og undirliggjandi verk eru notuð til að samstilla fylgiskjalsnúmerið og virðisaukaskattinn fyrir bókaðar verkfærslur frá Finance til Project Service Automation:

- **Heiti sniðmátsins í gagnasamþættingu:** Uppfærsla á rauntölum verks (Fin Ops til PSA)
- **Heiti verkefna í verkinu:**

    - Rauntölur 
    - TransactionConnections

### <a name="entity-set"></a>Einingastamstæða

| Fjármál                                                  | Project Service Automation |
|----------------------------------------------------------|----------------------------|
| Samþættingareining fyrir rauntölur verks                   | Rauntölur                    |
| Samþættingareining fyrir vensl verkfærsla | Færslutengingar    |

### <a name="entity-flow"></a>Einingaflæði

Rauntölum verks er stjórnað í Project Service Automation og þær eru samstilltar við færslubók verksamþættingar í Finance. Þegar rauntölur eru bókaðar í Finance eru þær uppfærðar í Project Service Automation með fylgiskjalsnúmerinu úr Finance. Ef virðisaukasköttum var bætt við í Finance verða nýjar rauntölur skatts búnar til í Project Service Automation.

### <a name="power-query"></a>Power Query

Þú verður að nota Power Query fyrir Excel í uppfærðu sniðmáti fyrir rauntölur verks til að ljúka þessum verkefnum:

- Umbreyta færslugerð í Finance í rétta færslugerð í Project Service Automation. Þessi umbreyting er þegar skilgreind í uppfærðu sniðmáti fyrir rauntölur verks (Fin and Ops til PSA).
- Umbreyta reikningsgerð í Finance yfir í rétta reikningsgerð í Project Service Automation. Þessi umbreyting er þegar skilgreind í uppfærðu sniðmáti fyrir rauntölur verks (Fin and Ops til PSA).

### <a name="template-mapping-in-data-integration"></a>Sniðmátsvörpun í Gagnasamþættingu

Eftirfarandi skýringarmyndir sýna dæmi um vörpunarsniðmát í gagnasamþættingu. Vörpunin sýnir reitaupplýsingarnar sem verða samstilltar úr Finance við Project Service Automation.

[![Kortlagning sniðmáts](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)

[![Kortlagning sniðmáts](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)
