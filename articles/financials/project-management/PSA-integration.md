---
title: Project Service Automation
description: Þetta efnisatriði veitir upplýsingar um samþættingarlausn Project Service Automation við Finance and Operations. Prospect to lausnin notar gagnasamþættingu til að samstilla gögn yfir Microsoft Dynamics 365 for Finance and Operations og Microsoft Dynamics 365 for Project Service Automation um Common Data Service.
author: KimANelson
manager: AnnBe
ms.date: 06/29/2018
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
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c1d6d0b219666bb31cf08da580c701f93d08389a
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/12/2019
ms.locfileid: "1741223"
---
# <a name="project-service-automation"></a>Project Service Automation

[!include[banner](../includes/banner.md)]

Samþættingarlausn Project Service Automation við Finance and Operations notar eiginleika gagnasamþættingar til að samstilla gögn þvert yfir tilvik af Microsoft Dynamics 365 for Finance and Operations og Microsoft Dynamics 365 for Project Service Automation í gegnum Common Data Service. Samþættingarsniðmátin sem eru tiltæk með eiginleika gagnasamþættingar gerir gögnum kleift að flæða varðandi verk, verksamninga, verksamningslínur, áfanga verksamningslína, verk verkefna, kostnaðarfærsluflokka, tímaáætlanir og kostnaðaráætlanir frá Project Service Automation til Finance and Operations.

> [!NOTE]
> - Ef þú notar Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3.0, eftir að hafa sett upp KB 4132657 og KB 4132660 getur þú notað sniðmátin til að samþætta verkefni fyrir verk, kostnaðarfærsluflokka, tímaáætlanir, kostnaðaráætlanir og rauntölur og til að stilla virknilæsingu. Ef þú verður að endurstilla dreifingu á fjárhagsupphæð mælum við með að þú setjir einnig upp KB 4131710.
> - Ef þú notar Finance and Operations 7.3.0, verður þú að setja upp KB 4074835. Þetta gerir þér kleift að samþætta verk með föstu verði.
> - Ef þú notar Finance and Operations 7.3.0 og þú færir þóknunarfærslur yfir frá Project Service Automation verður þú að setja upp KB 4345320 til þess að geta tekið við þessum þóknunum í verkreikningi.
> - Ef þú notar Microsoft Dynamics 365 for Finance and Operations útgáfu 8.0, getur þú notað samþættingu verkefnis fyrir verk, kostnaðarfærsluflokka, tímaáætlanir, kostnaðaráætlanir og virknilæsingu.
> - Ef þú notar Microsoft Dynamics 365 for Finance and Operations útgáfu 8.0.1 eða síðar, munt þú geta samstillt rauntölur.

Áður en þú getur samþætt Project Service Automation við Finance and Operations þarftu að stilla samþættingarfæribreytur Project Service Automation. Nánari upplýsingar er að finna í [samþættingarfæribreytum Project Service Automation](PSA-parameters.md).

Þessi samþættingarlausn gerir beina samstillingu í eftirfarandi atburðarásum mögulega:

- Viðhalda verksamningum í Project Service Automation og samstilla þá beint frá Project Service Automation við Finance and Operations.
- Búa til verk í Project Service Automation og samstillta þau beint frá Project Service Automation við Finance and Operations.
- Viðhalda verksamningslínum í Project Service Automation og samstilla þær beint frá Project Service Automation við Finance and Operations.
- Viðhalda áföngum verksamningslína í Project Service Automation og samstilla þá beint frá Project Service Automation við Finance and Operations.
- Viðhalda verkefnum verks í Project Service Automation og samstilla þá beint frá Project Service Automation við Finance and Operations.
- Viðhalda kostnaðarfærsluflokkum í Finance and Operations og samstilla þá beint frá Finance and Operations við Project Service Automation.
- Búa til tímaáætlanir verks í Project Service Automation og samstilla þær beint frá Project Service Automation við Finance and Operations.
- Búa til kostnaðaráætlanir verks í Project Service Automation og samstilla þær beint frá Project Service Automation við Finance and Operations.
- Búa til rauntölur tíma, kostnaðar og þóknunar fyrir verk í Project Service Automation og búa til verkfærslur í færslubók samþættingar fyrir Project Service Automation svo hægt sé að bóka þær í Finance and Operations.

## <a name="data-synchronization"></a>Samstilling gagna

Eftirfarandi skýringarmynd sýnir hvernig gögn eru samstillt sem hluti af samþættingu milli Project Service Automation og Finance and Operations.

> [!NOTE]
> Ekki eru öll sniðmát í boði eins og er. Sniðmát verða losuð þegar þau klárast.

[![Samþætting Project Service Automation við Finance and Operations](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance-and-operations"></a>Kerfisskilyrði fyrir Finance and Operations

Til að nota samþættingarlausn Project Service Automation við Finance and Operations þarftu að setja upp Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3 með verkvangsuppfærslu 12 eða nýrri.

## <a name="system-requirements-for-project-service-automation"></a>Kerfisskilyrði fyrir Project Service Automation

Til að nota samþættingarlausn Project Service Automation við Finance and Operations:

- Microsoft Dynamics 365 for Project Service Automation útgáfa 9.0.0.0 eða nýrri
- Prospect to cash lausn fyrir Microsoft Dynamics 365 for Sales, útgáfa 1.14.0.0 (v14) eða nýrri.
- Lausn Project Service Automation to Finance and Operations fyrir Microsoft Dynamics 365 for Project Service Automation útgáfa 1.0.0.0 eða nýrri

## <a name="install-the-project-service-automation-to-finance-and-operations-integration-solution-in-your-project-service-automation-instance"></a>Setja upp samþættingarlausn Project Service Automation við Finance and Operations í tilvikinu þínu af Project Service Automation

Sækja samþættingarlausn Project Service Automation við Finance and Operations hjá [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016) og fylgja leiðbeiningum sem fylgja með lausninni.
