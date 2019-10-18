---
title: Yfirlit Project Service Automation
description: Í þessu efnisatriði er að finna upplýsingar um samþættingarlausnina Dynamics 365 Project Service Automation til Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 07/25/2019
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
ms.openlocfilehash: 31d72591041f8d8cc327aa7c6578c15731ba13c5
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250554"
---
# <a name="project-service-automation-overview"></a>Yfirlit Project Service Automation

[!include[banner](../includes/banner.md)]

Samþættingarlausn Project Service Automation við Finance notar eiginleika gagnasamþættingar til að samstilla gögn þvert yfir tilvik af Dynamics 365 Finance og Dynamics 365 Project Service Automation í gegnum Common Data Service. Samþættingarsniðmátin sem eru tiltæk með eiginleika gagnasamþættingar gerir gögnum kleift að flæða varðandi verk, verksamninga, verksamningslínur, áfanga verksamningslína, verk verkefna, kostnaðarfærsluflokka, tímaáætlanir og kostnaðaráætlanir frá Project Service Automation til Finance.

> [!NOTE]
> - Ef þú notar útgáfu 7.3.0, verður þú að setja upp KB 4074835. Þetta gerir þér kleift að samþætta verk með föstu verði.
> - Ef þú notar útgáfu 7.3.0 og þú færir þóknunarfærslur yfir frá Project Service Automation verður þú að setja upp KB 4345320 til þess að geta tekið við þessum þóknunum í verkreikningi.
> - Ef þú notar útgáfu 8.0, getur þú notað samþættingu verkefnis fyrir verk, kostnaðarfærsluflokka, tímaáætlanir, kostnaðaráætlanir og virknilæsingu.
> - Ef þú notar útgáfu 8.0.1eða síðar, munt þú geta samstillt rauntölur.

Áður en þú getur samþætt Project Service Automation við Finance þarftu að stilla samþættingarfæribreytur Project Service Automation. Nánari upplýsingar er að finna í [samþættingarfæribreytum Project Service Automation](PSA-parameters.md).

Þessi samþættingarlausn gerir beina samstillingu í eftirfarandi atburðarásum mögulega:

- Viðhalda verksamningum í Project Service Automation og samstilla þá beint frá Project Service Automation við Finance.
- Búa til verk í Project Service Automation og samstillta þau beint frá Project Service Automation við Finance.
- Viðhalda verksamningslínum í Project Service Automation og samstilla þá beint frá Project Service Automation við Finance.
- Viðhalda línuáföngum verksamnings í Project Service Automation og samstilla þá beint frá Project Service Automation við Finance.
- Viðhalda verkum í Project Service Automation og samstilla þau beint frá Project Service Automation við Finance.
- Viðhalda kostnaðarfærsluflokkum í Finance and Operations og samstilla þá beint frá Finance við Project Service Automation.
- Búa til tímaáætlanir verks í Project Service Automation og samstilla þær beint frá Project Service Automation við Finance.
- Búa til kostnaðaráætlanir verks í Project Service Automation og samstilla þær beint frá Project Service Automation við Finance.
- Búa til rauntölur tíma, kostnaðar og þóknunar fyrir verk í Project Service Automation og búa til verkfærslur í færslubók samþættingar fyrir Project Service Automation svo hægt sé að bóka þær í Finance.

## <a name="data-synchronization"></a>Samstilling gagna

Eftirfarandi skýringarmynd sýnir hvernig gögn eru samstillt sem hluti af samþættingu milli Project Service Automation og Finance.

> [!NOTE]
> Ekki eru öll sniðmát í boði eins og er. Sniðmát verða losuð þegar þau klárast.

[![Samþætting Project Service Automation við Finance](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance"></a>Kerfisskilyrði fyrir Finance

Til að nota samþættingarlausn Project Service Automation við Finance þarftu að setja upp Enterprise Edition 7.3 með verkvangsuppfærslu 12 eða nýrri.

## <a name="system-requirements-for-project-service-automation"></a>Kerfisskilyrði fyrir Project Service Automation

Til að nota samþættingarlausn Project Service Automation við Finance verður að setja upp eftirfarandi þætti:

- Dynamics 365 Project Service Automation útgáfa 9.0.0.0 eða nýrri
- Prospect to cash lausn fyrir Dynamics 365 Sales, útgáfa 1.14.0.0 (v14) eða nýrri.
- Lausn Project Service Automation to Finance fyrir Dynamics 365 Project Service Automation útgáfa 1.0.0.0 eða nýrri

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a>Setja upp samþættingarlausn Project Service Automation við Finance í tilvikinu af Project Service Automation

Sækja samþættingarlausn Project Service Automation við Finance hjá [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016) og fylgja leiðbeiningum sem fylgja með lausninni.
