---
title: "Samstilla verkmat frá Project Service Automation beint við verkspár í Finance and Operations"
description: "Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verk sem notuð eru til að samstilla áætlaðan tíma verks og kostnaðarmat verks beint frá Microsoft Dynamics 365 for Project Service Automation við Dynamics 365 for Finance and Operations."
author: KimANelson
manager: AnnBe
ms.date: 04/02/2018
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
ms.openlocfilehash: 90501f40da0fdc66ad087b3bd746c908cc25711b
ms.contentlocale: is-is
ms.lasthandoff: 05/29/2018

---
# <a name="synchronize-project-estimates-from-project-service-automation-directly-to-project-forecasts-in-finance-and-operations"></a>Samstilla verkmat frá Project Service Automation beint við verkspár í Finance and Operations

Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verk sem notuð eru til að samstilla áætlaðan tíma verks og kostnaðarmat verks beint frá Microsoft Dynamics 365 for Project Service Automation við Dynamics 365 for Finance and Operations.

> [!NOTE]
> Samþætting verkefna fyrir verk, flokkar kostnaðarfærslna, áætlaður tími, kostnaðaráætlun og virknilæsing er í boði í Dynamics 365 for Finance and Operations útgáfu 8.0.


## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>Gagnaflæði fyrir Project Service Automation til Finance and Operations

Samþættingarlausn Project Service Automation við Finance and Operations notar eiginleika gagnasamþættingar til að samstilla gögn þvert yfir tilvik af Project Service Automation og Finance and Operations. Samþættingarsniðmátin sem eru tiltæk með eiginleika gagnasamþættingar gera gögnum kleift að flæða varðandi áætlaðan tíma verks og kostnaðarmat verks frá Project Service Automation til Finance and Operations.

Eftirfarandi skýringarmynd sýnir hvernig gögnin eru samstillt milli Project Service Automation og Finance and Operations.

[![Gagnaflæði fyrir samþættingu Project Service Automation við Finance and Operations](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)


## <a name="templates-and-tasks"></a>Sniðmát og verkefni

Til að fá aðgang að tiltækum sniðmátum, í stjórnendamiðstöð Microsoft PowerApps, skal velja **Verk** og síðan í efra hægra horninu skal velja **Nýtt verk** til að velja almenn sniðmát.

Eftirfarandi sniðmát og undirliggjandi verkefni eru notuð til að samstilla áætlaðan tíma verks frá Project Service Automation við Finance and Operations:

-  **Heiti sniðmátsins í gagnasamþættingu:** Áætlaður tími verks (PSA til Fin and Ops)

-  **Heiti verkefna í verkinu:** 
    - Færslutengsl 
    - Kostnaðaráætlanir

## <a name="entity-set"></a>Einingastamstæða

| Project Service Automation      | Finance and Operations                          |
|---------------------------------|-------------------------------------------------|
| Verkefni                   | Samþættingareining fyrir áætlaðar verkstundir   |

## <a name="entity-flow"></a>Einingaflæði

Áætluðum tíma verks er stjórnað í Project Service Automation og hann er samstilltur við Finance and Operations sem tímaspá verks.

## <a name="preconditions"></a>Skilyrði

Áður en samstilling á áætluðum tíma verks getur átt sér stað verður þú að samstilla flokka fyrir verk, verkefni verks og kostnaðarfærslur verks.

## <a name="power-query"></a>Power Query

Þú verður að nota Microsoft Power Query í sniðmáti fyrir áætlun á tíma verks til að:
- Settu á **Kenni spárlíkans** sem verður notað þegar samþættingin býr til nýja tímaspá.
- Síaðu út allar sértækar færslur tilfanga innan verksins sem munu ekki standast samþættinguna í tímaspám
- Síaðu út allar auðar línur færsluflokks. Ef ekki tekst að gera þetta getur það leitt til rangra tímaspáa.

### <a name="forecast-model-id"></a>Spárlíkanskenni
Til að uppfæra sjálfgefið spárlíkanskenni í sniðmátinu skal smella á örina **Varpa** til að opna vörpunina. Veldu til að opna Advanced Query and Filtering.
- Ef þú notar sniðmát fyrir sjálfgefnar tímaáætlanir Microsoft Project (PSA til Fin and Ops) skaltu velja **Innslegið skilyrði** í hlutanum **Notuð skref**. Í færslunni **Aðgerð** skaltu skipta út **O_forecast** fyrir heitið á **Spárlíkanskenni** sem ætti að nota með samþættingunni. Sjálfgefið sniðmát er með spárlíkanskenni frá sýnigögnunum.
- Ef þú ert að búa til nýtt sniðmát þarftu að bæta við þessum dálki. Veldu **Bæta við skilyrtum dálki** og gefðu dálknum heiti á borð við ModelID. Sláðu inn skilyrði fyrir dálkinn þar sem ef verkefni verks er ekki núll, þá<enter the forecast model ID>; annars núll.

### <a name="filter-out-resource-specific-records"></a>Síaðu út sértækar færslur tilfangs
Sniðmát fyrir tímaáætlanir verks (PSA til Fin and Ops) hefur sjálfgefna síu sem fjarlægir allar sértækar færslur tilfangs. Ef þú býrð til þitt eigið sniðmát þarftu að bæta við þessari síu. Í sniðinu Advanced Query and Filtering skaltu velja að sía í dálknum **msdyn_islinetask** til að aðeins hafa með færslurnar **Ósatt**.

### <a name="filter-out-empty-transaction-category-rows"></a>Síaðu út auðar línur færsluflokks
Þú verður að bæta við síu til að fjarlægja allar þær línur sem eru með tómum færsluflokkum. Þetta er nauðsynlegt óháð því hvort þú notir sjálfgefið sniðmát eða býrð til þitt eigið sniðmát. Þessi sía fjarlægir allar samantektarlínur sem koma frá Project Service Automation sem gætu valdið því að tímaspár í Finance and Operations verði rangar. Í sniðinu Advanced Query and Filtering skaltu velja að sía út núllfærslur í dálkinum **msdyn_transactioncategory_value**.

## <a name="template-mapping-in-data-integration"></a>Sniðmátsvörpun í Gagnasamþættingu

Eftirfarandi skýringarmynd sýnir dæmi um vörpunarsniðmát í gagnasamþættingu. Vörpunin sýnir reitaupplýsingarnar sem verða samstilltar frá Project Service Automation við Finance and Operations.

[![Kortlagning sniðmáts](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)

Eftirfarandi sniðmát og undirliggjandi verkefni eru notuð til að samstilla kostnaðaráætlanir verks frá Project Service Automation til Finance and Operations:

-  **Heiti sniðmátsins í gagnasamþættingu:** Kostnaðaráætlanir verks (PSA til Fin and Ops)
-  **Heiti verkefna í verkinu:** 
     - Færslutengsl 
     - Kostnaðaráætlanir

## <a name="entity-set"></a>Einingastamstæða

| Project Service Automation      | Finance and Operations                                     |
|---------------------------------|------------------------------------------------------------|
| Færslutengingar         | Samþættingareining fyrir vensl verkfærsla.   |
| Meta línur                  | Samþættingareining fyrir áætlaðan verkkostnað.           |

## <a name="entity-flow"></a>Einingaflæði

Kostnaðaráætlunum verks er stjórnað í Project Service Automation og þær eru samstilltar við Finance and Operations sem kostnaðarspár verks.

## <a name="prerequisites"></a>Frumskilyrði

Áður en samstilling á kostnaðaráætlunum verks getur átt sér stað verður þú að samstilla flokka fyrir verk, verkefni verks og kostnaðarfærslur verks.

## <a name="power-query"></a>Power Query

Þú verður að nota Microsoft Power Query í sniðmáti fyrir tímaáætlun verks til að:
- Sía til að innihalda aðeins færslulínur kostnaðaráætlunar
- Settu á **Kenni spárlíkans** sem verður notað þegar samþættingin býr til nýja tímaspá.
- Umbreyta reikningsgerðunum.
- Umbreyta færslugerðunum.

### <a name="filter-to-include-only-expense-estimate-lines"></a>Sía til að innihalda aðeins línur kostnaðaráætlunar
Sniðmát fyrir kostnaðaráætlanir verks (PSA til Fin and Ops) hefur sjálfgefna síu til að aðeins innihalda kostnaðarlínur í samþættingunni. Ef þú býrð til þitt eigið sniðmát þarftu að bæta við þessari síu. Veldu verkefni færslutengsla og smelltu á örina **Varpa**. Veldu **Advanced Query and filtering**. Síaðu dálkinn **msdyn_transactiontype1** til að innihalda aðeins **msdyn_estimateline**.

### <a name="forecast-model-id"></a>Spárlíkanskenni
Til að uppfæra sjálfgefið spárlíkanskenni í sniðmátinu, fyrir verkefni kostnaðaráætlana, skal smellt á örina **Varpa** til að opna vörpunina. Veldu til að opna Advanced Query and Filtering.
- Ef þú notar sniðmát fyrir sjálfgefnar kostnaðaráætlanir Microsoft Project (PSA til Fin and Ops) skaltu velja fyrsta **Innslegna skilyrðið** í hlutanum **Notuð skref**. Í færslunni **Aðgerð** skaltu skipta út **O_forecast** fyrir heitið á **Spárlíkanskenni** sem ætti að nota með samþættingunni. Sjálfgefið sniðmát er með spárlíkanskenni frá sýnigögnunum.
- Ef þú ert að búa til nýtt sniðmát þarftu að bæta við þessum dálki. Veldu **Bæta við skilyrtum dálki** og gefðu dálknum heiti á borð við ModelID. Sláðu inn skilyrðið fyrir dálkinn þar sem ef kenni línuáætlunar er ekki núll, þá < skaltu slá inn spárlíkanskenni >; annars núll.

### <a name="transform-the-billing-types"></a>Umbryta reikningsgerðunum
Sniðmát fyrir kostnaðaráætlanir verks (PSA til Fin and Ops) hefur bætt við skilyrtum dálki til að umbreyta reikningsgerðunum sem eru mótteknar frá Project Service Automation meðan á samþættingu stendur.
- Ef þú býrð til þitt eigið sniðmát þarftu að bæta við þessum skilyrta dálki. Í sniðinu Advanced Query and Filtering skal velja **Bæta við skilyrtum dálki**. Gefðu dálknum heiti, svo sem "BillingType". Skilyrðið til að slá inn er sem hér segir:

    Ef **msdyn_billingtype** = 192350000, þá **NonChargeable** annars ef **msdyn_billingtype** = 192350001, þá **Reikningshæfur** annars ef **msdyn_billingtype** = 192350002, þá **Ókeypis** annars **NotAvailable**

### <a name="transform-the-transaction-types"></a>Umbreyta færslugerðunum
Sniðmát fyrir kostnaðaráætlanir verks (PSA til Fin and Ops) hefur bætt við skilyrtum dálki til að umbreyta færslugerðunum sem eru mótteknar frá Project Service Automation meðan á samþættingu stendur.
- Ef þú býrð til þitt eigið sniðmát þarftu að bæta við þessum skilyrta dálki. Í sniðinu Advanced Query and Filtering skal velja **Bæta við skilyrtum dálki**. Gefðu dálknum nafn, svo sem "TransactionType". Skilyrði til að slá inn er eftirfarandi: Ef **msdyn_transactiontypecode** = 192350000, þá **Kostnaður** annars ef **msdyn_transactiontypecode** = 192350005, þá **Sölur** annars **núll**

## <a name="template-mapping-in-data-integration"></a>Sniðmátsvörpun í Gagnasamþættingu

Eftirfarandi skýringarmyndir sýna dæmi um vörpunarsniðmát í gagnasamþættingu. Vörpunin sýnir reitaupplýsingarnar sem verða samstilltar frá Project Service Automation við Finance and Operations.

[![Kortlagning sniðmáts](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)

[![Kortlagning sniðmáts](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)




