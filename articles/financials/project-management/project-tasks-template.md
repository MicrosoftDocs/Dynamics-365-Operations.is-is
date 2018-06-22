---
title: "Samstilla verkefni verks frá Project Service Automation"
description: "Þetta efnisatriði fjallar um sniðmátið og undirliggjandi verk sem notuð eru til að samstilla verkefni verks beint úr Microsoft Dynamics 365 for Project Service Automation við Dynamics 365 for Finance and Operations."
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
ms.sourcegitcommit: 399b519ab0da4de405aeb06f3e7f4bf29a6c5cc3
ms.openlocfilehash: 89df0d99d780441ad08cd6bff3e1fd203694eb8e
ms.contentlocale: is-is
ms.lasthandoff: 05/30/2018

---

# <a name="synchronize-project-tasks-from-project-service-automation-directly-to-project-activities-in-finance-and-operations"></a>Samstilla verkefni verks frá Project Service Automation beint við verkþætti verks í Finance and Operations

Þetta efnisatriði fjallar um sniðmátið og undirliggjandi verk sem notuð eru til að samstilla verkefni verks beint úr Microsoft Dynamics 365 for Project Service Automation við Dynamics 365 for Finance and Operations.

> [!NOTE]
> Samþætting verkefna fyrir verk, flokkar kostnaðarfærslna, áætlaður tími, kostnaðaráætlun og virknilæsing er í boði í Dynamics 365 for Finance and Operations útgáfu 8.0.

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>Gagnaflæði fyrir Project Service Automation til Finance and Operations

Samþættingarlausn Project Service Automation við Finance and Operations notar eiginleika gagnasamþættingar til að samstilla gögn þvert yfir tilvik af Project Service Automation og Finance and Operations. Samþættingarsniðmátið sem er tiltækt með eiginleika gagnasamþættingar gerir gögnum kleift að flæða varðandi verkefni verks frá Project Service Automation til Finance and Operations.

Eftirfarandi skýringarmynd sýnir hvernig gögnin eru samstillt milli Project Service Automation og Finance and Operations.

[![Gagnaflæði fyrir samþættingu Project Service Automation við Finance and Operations](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)

## <a name="template-and-task"></a>Sniðmát og verkefni

Til að fá aðgang að sniðmátinu, í stjórnendamiðstöð Microsoft PowerApps, skal velja **Verk** og síðan í efra hægra horninu skal velja **Nýtt verk** til að velja almenn sniðmát.

Eftirfarandi sniðmát og undirliggjandi verkefni eru notuð til að samstilla verkefni verks frá Project Service Automation við Finance and Operations:

-**Heiti sniðmátsins í gagnasamþættingu:** Verkefni verks (PSA til Fin and Ops) -**Heiti verkefnis í verkinu:** Verkefni verks

Áður en samstilling verksamninga getur átt sér stað verður þú að samstilla verksamninga og verk.

## <a name="entity-set"></a>Einingastamstæða

|Project Service Automation               | Finance and Operations                |
|-----------------------------------------|---------------------------------------|
| Verkefni                           | Samþættingareining fyrir verkefni.   |

## <a name="entity-flow"></a>Einingaflæði

Verksamningum er stjórnað í Project Service Automation og þeir eru samstilltir við Finance and Operations sem verkþættir verks.

## <a name="prerequisites-and-mapping-setup"></a>Skilyrði og vörpunaruppsetning

Áður en samstilling verksamninga getur átt sér stað verður þú að samstilla verksamninga og verk.

## <a name="power-query"></a>Power Query

Þú verður að nota Microsoft Power Query til að sía gögn ef þessi skilyrði eru uppfyllt:

- Þú hefur sértækar færslur tilfangs innan verkefnis á verki.

Ef þú verður að nota Power Query skaltu fylgja þessum leiðbeiningum:

- Sniðmát fyrir verkefni verks (PSA til Fin and Ops) hefur sjálfgefna síu til að útiloka sértækar færslur tilfangs innan verkefnis fyrir verk með því að stilla síuna á **IsLineTask** á **Ósatt**. Ef þú býrð til þitt eigið sniðmát þarftu að bæta við þessari síu.

## <a name="template-mapping-in-data-integration"></a>Sniðmátsvörpun í Gagnasamþættingu

Eftirfarandi skýringarmynd sýnir dæmi vörpunarsniðmáts í gagnasamþættingu. Vörpunin sýnir reitaupplýsingarnar sem verða samstilltar frá Project Service Automation við Finance and Operations.

[![Kortlagning sniðmáts](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)


