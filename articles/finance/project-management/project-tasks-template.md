---
title: Samstilla verkefni verks beint frá Project Service Automation við Finance and Operations
description: Þetta efnisatriði fjallar um sniðmátið og undirliggjandi verkefni sem notuð eru til að samstilla verkefni verks beint frá Microsoft Dynamics 365 Project Service Automation til Dynamics 365 Finance.
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
ms.openlocfilehash: ba475721b69e7c75dfd2197597b54050a3598d37
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770267"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a>Samstilla verkefni verks beint frá Project Service Automation við Finance and Operations

[!include[banner](../includes/banner.md)]

Þetta efnisatriði fjallar um sniðmátið og undirliggjandi verkefni sem notuð eru til að samstilla verkefni verks beint frá Dynamics 365 Project Service Automation til Dynamics 365 Finance.

> [!NOTE]
> - Samþætting verkefna fyrir verk, flokkar kostnaðarfærslna, áætlaður tími, kostnaðaráætlun og virknilæsing eru í boði í útgáfu 8.0.
> - Ef þú notar Enterprise Edition 7.3.0, eftir að hafa sett upp KB 4132657 og KB 4132660 getur þú notað sniðmátin til að samþætta verkefni fyrir verk, kostnaðarfærsluflokka, tímaáætlanir, kostnaðaráætlanir og rauntölur og til að stilla virknilæsingu. Ef þú verður að endurstilla dreifingu á fjárhagsupphæð mælum við með að þú setjir einnig upp KB 4131710.
> - Samþætting á rauntölum er í boði í útgáfu 8.0.1 eða nýrri.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Gagnaflæði fyrir Project Service Automation til Finance

Samþættingarlausn Project Service Automation við Finance notar eiginleika gagnasamþættingar til að samstilla gögn þvert yfir tilvik af Project Service Automation og Finance. Samþættingarsniðmátið sem er tiltækt með eiginleika gagnasamþættingar gerir gögnum kleift að flæða varðandi verkefni verks frá Project Service Automation til Finance.

Eftirfarandi skýringarmynd sýnir hvernig gögnin eru samstillt milli Project Service Automation og Finance.

[![Gagnaflæði fyrir samþættingu Project Service Automation við Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)

## <a name="template-and-task"></a>Sniðmát og verkefni

Til að fá aðgang að tiltækum sniðmátum, í stjórnendamiðstöð Microsoft Power Apps, skal velja **Verk** og síðan í efra hægra horninu skal velja **Nýtt verk** til að velja almenn sniðmát.

Eftirfarandi sniðmát og undirliggjandi verkefni eru notuð til að samstilla verkefni verks frá Project Service Automation við Finance:

- **Heiti sniðmátsins í gagnasamþættingu:** Verkefni verks (PSA til Fin and Ops)
- **Heiti verkefnis í verkinu:** Verkefni verks

Áður en samstilling verksamninga getur átt sér stað verður þú að samstilla verksamninga og verk.

## <a name="entity-set"></a>Einingastamstæða

| Project Service Automation | Fjármál                             |
|----------------------------|-------------------------------------|
| Verkefni              | Samþættingareining fyrir verkefni |

## <a name="entity-flow"></a>Einingaflæði

Verksamningum er stjórnað í Project Service Automation og þeir eru samstilltir við Finance sem verkþættir verks.

## <a name="prerequisites-and-mapping-setup"></a>Skilyrði og vörpunaruppsetning

Áður en samstilling verksamninga getur átt sér stað verður þú að samstilla verksamninga og verk.

## <a name="power-query"></a>Power Query

Þú verður að nota Microsoft Power Query fyrir Excel til að sía gögn ef þetta skilyrði er uppfyllt:

- Þú ert með sértækar færslur tilfangs í verkefni verks.

Ef þú verður að nota Power Query skaltu fylgja þessum leiðbeiningum:

- Sniðmát fyrir verkefni verks (PSA til Fin and Ops) hefur sjálfgefna síu til að útiloka sértækar færslur tilfangs frá verkefni fyrir verk með því að stilla síuna á **IsLineTask** á **Ósatt**. Ef þú býrð til þitt eigið sniðmát þarftu að bæta við þessari síu.

## <a name="template-mapping-in-data-integration"></a>Sniðmátsvörpun í Gagnasamþættingu

Eftirfarandi skýringarmynd sýnir dæmi vörpunarsniðmáts í gagnasamþættingu. Vörpunin sýnir reitaupplýsingarnar sem verða samstilltar frá Project Service Automation við Finance.

[![Kortlagning sniðmáts](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)
