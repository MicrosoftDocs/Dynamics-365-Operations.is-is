---
title: Samstilla verkáætlanir beint frá Project Service Automation við Finance and Operations
description: Þetta efnisatriði fjallar um sniðmát og undirliggjandi verkefni sem notuð eru til að samstilla tímaáætlun verks og kostnaðaráætlun verks beint frá Microsoft Dynamics 365 for Project Service Automation til Microsoft Dynamics 365 for Finance and Operations.
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
ms.openlocfilehash: 21338b889e0377dbfd5adfd461ea81b39a75baf8
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "353955"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a>Samstilla verkáætlanir beint frá Project Service Automation við Finance and Operations

[!include[banner](../includes/banner.md)]

Þetta efnisatriði fjallar um sniðmát og undirliggjandi verkefni sem notuð eru til að samstilla tímaáætlun verks og kostnaðaráætlun verks beint frá Microsoft Dynamics 365 for Project Service Automation til Dynamics 365 for Finance and Operations.

> [!NOTE]
> - Samþætting verkefna fyrir verk, flokkar kostnaðarfærslna, áætlaður tími, kostnaðaráætlun og virknilæsing er í boði í Microsoft Dynamics 365 for Finance and Operations útgáfu 8.0.
> - Samþætting á rauntölum er í boði í Microsoft Dynamics 365 for Finance and Operations útgáfu 8.0.1 eða nýrri.
> - Ef þú notar Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3.0, eftir að hafa sett upp KB 4132657 og KB 4132660 getur þú notað sniðmátin til að samþætta verkefni fyrir verk, kostnaðarfærsluflokka, tímaáætlanir, kostnaðaráætlanir og rauntölur og til að stilla virknilæsingu. Ef þú verður að endurstilla dreifingu á fjárhagsupphæð mælum við með að þú setjir einnig upp KB 4131710.

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>Gagnaflæði fyrir Project Service Automation til Finance and Operations

Samþættingarlausn Project Service Automation við Finance and Operations notar eiginleika gagnasamþættingar til að samstilla gögn þvert yfir tilvik af Project Service Automation og Finance and Operations. Samþættingarsniðmátin sem eru tiltæk með eiginleika gagnasamþættingar gera gögnum kleift að flæða varðandi áætlaðan tíma verks og kostnaðarmat verks frá Project Service Automation til Finance and Operations.

Eftirfarandi skýringarmynd sýnir hvernig gögnin eru samstillt milli Project Service Automation og Finance and Operations.

[![Gagnaflæði fyrir samþættingu Project Service Automation við Finance and Operations](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)

## <a name="project-hour-estimates"></a>Áætlaðar verkstundir

### <a name="template-and-tasks"></a>Sniðmát og verkefni

Til að fá aðgang að tiltækum sniðmátum, í stjórnendamiðstöð Microsoft PowerApps, skal velja **Verk** og síðan í efra hægra horninu skal velja **Nýtt verk** til að velja almenn sniðmát.

Eftirfarandi sniðmát og undirliggjandi verkefni eru notuð til að samstilla áætlaðan tíma verks frá Project Service Automation við Finance and Operations:

- **Heiti sniðmátsins í gagnasamþættingu:** Áætlaður tími verks (PSA til Fin and Ops)
- **Heiti verkefna í verkinu:**

    - Færslutengsl
    - Kostnaðaráætlanir

### <a name="entity-set"></a>Einingastamstæða

| Project Service Automation | Finance and Operations                        |
|----------------------------|-----------------------------------------------|
| Verkefni              | Samþættingareining fyrir áætlaðar verkstundir |

### <a name="entity-flow"></a>Einingaflæði

Áætluðum tíma verks er stjórnað í Project Service Automation og hann er samstilltur við Finance and Operations sem tímaspá verks.

### <a name="prerequisites"></a>Frumskilyrði

Áður en samstilling á áætluðum tíma verks getur átt sér stað verður þú að samstilla flokka fyrir verk, verkefni verks og kostnaðarfærslur verks.

### <a name="power-query"></a>Power Query

Þú verður að nota Microsoft Power Query fyrir Excel í sniðmáti fyrir áætlaðan tíma verks til að ljúka þessum verkefnum:

- Settu á sjálfgefið kenni spárlíkans sem verður notað þegar samþættingin býr til nýja tímaspá.
- Síaðu út allar sértækar færslur tilfanga í verkinu sem munu ekki standast samþættinguna í tímaspár.
- Síaðu út allar auðar línur færsluflokks. Ef ekki tekst að ljúka þessu verki getur það leitt til rangra tímaspáa.

#### <a name="set-the-default-forecast-model-id"></a>Settu á sjálfgefið spárlíkanskenni

Til að uppfæra sjálfgefið spárlíkanskenni í sniðmátinu skal smella á örina **Varpa** til að opna vörpunina. Veldu síðan tengilinn **Ítarleg fyrirspurn og síun**.

- Ef þú notar sniðmát fyrir sjálfgefnar tímaáætlanir verks (PSA til Fin and Ops) skaltu velja **Innslegið skilyrði** í listanum yfir **Notuð skref**. Í færslunni **Aðgerð** skaltu skipta út **O\_forecast** fyrir heitið á spárlíkanskenni sem ætti að nota með samþættingunni. Sjálfgefið sniðmát er með spárlíkanskenni frá sýnigögnunum.
- Ef þú ert að búa til nýtt sniðmát þarftu að bæta við þessum dálki. Veldu **Bæta við skilyrtum dálki** í Power Query og gefðu nýja dálknum heiti á borð við **ModelID**. Sláðu inn skilyrði fyrir dálkinn þar sem ef verkefni verks er ekki núll, þá \<sláðu inn spárlíkanskennið\>; annars núll.

#### <a name="filter-out-resource-specific-records"></a>Sía út sértækar færslur tilfangs

Sniðmát fyrir tímaáætlanir verks (PSA til Fin and Ops) hefur sjálfgefna síu sem fjarlægir allar sértækar færslur tilfangs. Ef þú býrð til þitt eigið sniðmát þarftu að bæta við þessari síu. Veldu tengilinn **Ítarleg fyrirspurn og síun** til að sía dálkinn **msdyn\_islinetask** þannig að aðeins **Rangar** færslur eru hafðar með.

#### <a name="filter-out-empty-transaction-category-rows"></a>Síaðu út auðar línur færsluflokks

Þú verður að bæta við síu til að fjarlægja allar línur sem eru með tómum færsluflokkum. Þetta verkefni er nauðsynlegt óháð því hvort þú notir sjálfgefið sniðmát eða býrð til þitt eigið sniðmát. Þessi sía fjarlægir allar samantektarlínur frá Project Service Automation sem gætu valdið því að tímaspár í Finance and Operations verði rangar. Veldu tengilinn **Ítarleg fyrirspurn og síun** til að sía út núllfærslur í dálknum **msdyn\_færsluflokks\_gildi**.

### <a name="template-mapping-in-data-integration"></a>Sniðmátsvörpun í Gagnasamþættingu

Eftirfarandi skýringarmynd sýnir dæmi um vörpunarsniðmát í gagnasamþættingu. Vörpunin sýnir reitaupplýsingarnar sem verða samstilltar frá Project Service Automation við Finance and Operations.

[![Kortlagning sniðmáts](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)

## <a name="project-expense-estimates"></a>Kostnaðaráætlanir verks

### <a name="template-and-tasks"></a>Sniðmát og verkefni

Eftirfarandi sniðmát og undirliggjandi verkefni eru notuð til að samstilla áætlaðan kostnað verks frá Project Service Automation við Finance and Operations:

- **Heiti sniðmátsins í gagnasamþættingu:** Kostnaðaráætlanir verks (PSA til Fin and Ops)
- **Heiti verkefna í verkinu:**

    - Færslutengsl 
    - Kostnaðaráætlanir

### <a name="entity-set"></a>Einingastamstæða

| Project Service Automation | Finance and Operations                                   |
|----------------------------|----------------------------------------------------------|
| Færslutengingar    | Samþættingareining fyrir vensl verkfærsla |
| Meta línur             | Samþættingareining fyrir áætlaðan verkkostnað         |

### <a name="entity-flow"></a>Einingaflæði

Kostnaðaráætlunum verks er stjórnað í Project Service Automation og þær eru samstilltar við Finance and Operations sem kostnaðarspár verks.

### <a name="prerequisites"></a>Frumskilyrði

Áður en samstilling á kostnaðaráætlunum verks getur átt sér stað verður þú að samstilla flokka fyrir verk, verkefni verks og kostnaðarfærslur verks.

### <a name="power-query"></a>Power Query

Þú verður að nota Power Query í sniðmáti fyrir kostnaðaráætlanir verks til að ljúka þessum verkefnum:

- Sía til að innihalda aðeins færslulínur kostnaðaráætlunar.
- Settu á sjálfgefið kenni spárlíkans sem verður notað þegar samþættingin býr til nýja tímaspá.
- Umbreyta reikningsgerðunum.
- Umbreyta færslugerðunum.

#### <a name="filter-to-include-only-expense-estimate-lines"></a>Sía til að innihalda aðeins línur kostnaðaráætlunar

Sniðmát fyrir kostnaðaráætlanir verks (PSA til Fin and Ops) hefur sjálfgefna síu sem inniheldur aðeins kostnaðarlínur í samþættingunni. Ef þú býrð til þitt eigið sniðmát þarftu að bæta við þessari síu. Veldu verkefnið **Færslutengsl** og smelltu síðan á örina **Varpa** til að opna vörpunina. Veldu tengilinn **Ítarleg fyrirspurn og síun**. Síaðu dálkinn **msdyn\_transactiontype1** þannig að hann innihaldi aðeins **msdyn\_estimateline**.

#### <a name="set-the-default-forecast-model-id"></a>Settu á sjálfgefið spárlíkanskenni

Til að uppfæra sjálfgefið spárlíkanskenni í sniðmátinu skal velja verkefnið **Kostnaðaráætlanir** og smella síðan á örina **Varpa** til að opna vörpunina. Veldu tengilinn **Ítarleg fyrirspurn og síun**.

- Ef þú notar sniðmát fyrir sjálfgefnar kostnaðaráætlanir verks (PSA til Fin and Ops) í Power Query skaltu fyrst velja **Innslegið skilyrði** úr hlutanum **Notuð skref**. Í færslunni **Aðgerð** skaltu skipta út **O\_forecast** fyrir heitið á spárlíkanskenni sem ætti að nota með samþættingunni. Sjálfgefið sniðmát er með spárlíkanskenni frá sýnigögnunum.
- Ef þú ert að búa til nýtt sniðmát þarftu að bæta við þessum dálki. Veldu **Bæta við skilyrtum dálki** í Power Query og gefðu nýja dálknum heiti á borð við **ModelID**. Sláðu inn skilyrðið fyrir dálkinn þar sem ef kenni línuáætlunar er ekki núll, þá skal \<slá inn spárlíkanskennið\>; annars núll.

#### <a name="transform-the-billing-types"></a>Umbryta reikningsgerðunum

Sniðmát fyrir kostnaðaráætlanir verks (PSA til Fin and Ops) inniheldur skilyrtan dálk sem er notaður til að umbreyta reikningsgerðunum sem eru mótteknar frá Project Service Automation meðan á samþættingu stendur. Ef þú býrð til þitt eigið sniðmát þarftu að bæta við þessum skilyrta dálki. Veldu tengilinn **Ítarleg fyrirspurn og síun** og veldu síðan **Bæta við skilyrtum dálki**. Sláðu inn heiti á nýja dálknum, t.d. **BillingType**. Sláðu síðan inn eftirfarandi skilyrði:

Ef **msdyn\_billingtype** = 192350000, þá **NonChargeable**  
annars ef **msdyn\_billingtype** = 192350001, þá **Chargeable**  
annars ef **msdyn\_billingtype** = 192350002, þá **Complimentary**  
annars **NotAvailable**

#### <a name="transform-the-transaction-types"></a>Umbreyta færslugerðunum

Sniðmát fyrir kostnaðaráætlanir verks (PSA til Fin and Ops) inniheldur skilyrtan dálk sem er notaður til að umbreyta færslugerðunum sem eru mótteknar frá Project Service Automation meðan á samþættingu stendur. Ef þú býrð til þitt eigið sniðmát þarftu að bæta við þessum skilyrta dálki. Veldu tengilinn **Ítarleg fyrirspurn og síun** og veldu síðan **Bæta við skilyrtum dálki**. Færa inn heiti á nýja dálknum, t.d. **TransactionType**. Sláðu síðan inn eftirfarandi skilyrði:

Ef **msdyn\_transactiontypecode** = 192350000, þá **Kostnaður**  
annars ef **msdyn\_transactiontypecode** = 192350005, þá **Sala**  
annars **núll**

### <a name="template-mapping-in-data-integration"></a>Sniðmátsvörpun í Gagnasamþættingu

Eftirfarandi skýringarmyndir sýna dæmi um vörpunarsniðmát í gagnasamþættingu. Vörpunin sýnir reitaupplýsingarnar sem verða samstilltar frá Project Service Automation við Finance and Operations.

[![Kortlagning sniðmáts](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)

[![Kortlagning sniðmáts](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)
