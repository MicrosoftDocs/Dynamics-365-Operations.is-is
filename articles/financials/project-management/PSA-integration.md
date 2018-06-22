---
title: Project Service Automation
description: "Þessi lausn notar eiginleika gagnasamþættingar til að samstilla gögn þvert yfir tilvik af Microsoft Dynamics 365 for Finance and Operations og Microsoft Dynamics 365 for Project Service Automation í gegnum Common Data Service (CDS)."
author: KimANelson
manager: AnnBe
ms.date: 11/27/2017
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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: 0ad9e6ba7fe8dd915681da8e671ff210de887b1e
ms.contentlocale: is-is
ms.lasthandoff: 05/29/2018

---

# <a name="project-service-automation"></a>Project Service Automation

Samþættingarlausn Project Service Automation við Finance and Operations notar eiginleika gagnasamþættingar til að samstilla gögn þvert yfir tilvik af Microsoft Dynamics 365 for Finance and Operations og Microsoft Dynamics 365 for Project Service Automation í gegnum Common Data Service (CDS). Samþættingarsniðmátin sem eru tiltæk með eiginleika gagnasamþættingar gerir gögnum kleift að flæða varðandi verk, verksamninga, verksamningslínur, áfanga verksamningslína, verk verkefna, kostnaðarfærsluflokka, tímaáætlanir og kostnaðaráætlanir frá Project Service Automation til Finance and Operations.

> [!NOTE] 
> Ef þú notar Dynamics 365 for Finance and Operations, Enterprise Edition 7.3.0, verður þú að setja upp KB 4074835. Þetta gerir þér kleift að samþætta verk með föstu verði.
>
> Ef þú notar Dynamics 365 for Finance and Operations útgáfu 8.0, getur þú notað samþættingu verkefna fyrir verk, kostnaðarfærsluflokka, tímaáætlanir, kostnaðaráætlanir og virknilæsingu.
>
> Ef þú notar Dynamics 365 for Finance and Operations útgáfu 8.0.1, munt þú geta samstillt rauntölur.
>
> Ef þú notar Dynamics 365 for Finance and Operations Enterprise Edition 7.3.0, eftir að hafa sett upp KB 4132657 og KB 4132660 getur þú notað sniðmátin til að samþætta verkefni fyrir verk, kostnaðarfærsluflokka, tímaáætlanir, kostnaðaráætlanir og rauntölur og til að stilla virknilæsingu. Ef þú verður að endurstilla dreifingu á fjárhagsupphæð mælum við með að þú setjir einnig upp KB 4131710.

Áður en þú getur samþætt Project Service Automation við Finance and Operations þarftu að stilla samþættingarfæribreytur Project Service Automation. Nánari upplýsingar er að finna í samþættingarfæribreytum Project Service Automation.

Þessi samþættingarlausn gerir beina samstillingu í eftirfarandi atburðarásum mögulega:

- Viðhalda verksamningum í Project Service Automation og samstilla þá beint frá Project Service Automation við Finance and Operations.
- Búa til verk í Project Service Automation og samstillta þau beint frá Project Service Automation við Finance and Operations.
- Viðhalda verksamningslínum í Project Service Automation og samstilla þær beint frá Project Service Automation við Finance and Operations.
- Viðhalda áföngum verksamningslína í Project Service Automation og samstilla þá beint frá Project Service Automation við Finance and Operations.
- Viðhalda verkefnum verks í Project Service Automation og samstilla þá beint frá Project Service Automation við Finance and Operations.
- Viðhalda kostnaðarfærsluflokkum í Finance and Operations og samstilla þá beint frá Finance and Operations við Project Service Automation.
- Búa til tímaáætlanir verks í Project Service Automation og samstilla þær beint frá Project Service Automation við Finance and Operations.
- Búa til kostnaðaráætlanir verks í Project Service Automation og samstilla þær beint frá Project Service Automation við Finance and Operations.

## <a name="data-synchronization"></a>Samstilling gagna
Eftirfarandi skýringarmynd sýnir hvernig gögn eru samstillt sem hluti af samþættingu milli Project Service Automation og Finance and Operations.

> [!NOTE]
> Ekki eru öll sniðmát í boði eins og er. Sniðmát verða losuð þegar þau klárast.

[![Samþætting Project Service Automation við Finance and Operations](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance-and-operations"></a>Kerfisskilyrði fyrir Finance and Operations

Til að nota samþættingarlausn Project Service Automation við Finance and Operations þarftu að setja upp Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 7.3 með verkvangsuppfærslu 12 eða nýrri.

## <a name="system-requirements-for-project-service-automation"></a>Kerfisskilyrði fyrir Project Service Automation

Til að nota samþættingarlausn Project Service Automation við Finance and Operations:

- Microsoft Dynamics 365 for Project Service Automation útgáfa 9.0.0.0 eða síðar.
- Prospect to cash lausn fyrir Dynamics 365 for Sales, útgáfa 1.14.0.0 (v14) eða nýrri.
- Lausn Project Service Automation to Operations fyrir Dynamics 365 for Project Service Automation útgáfa 1.0.0.0 eða síðar.

## <a name="install-the-project-service-automation-to-finance-and-operations-integration-solution-in-your-project-service-automation-instance"></a>Setja upp samþættingarlausn Project Service Automation við Finance and Operations í tilvikinu þínu af Project Service Automation



