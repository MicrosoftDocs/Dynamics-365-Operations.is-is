---
title: Samþættingarfæribreytur Project Service Automation
description: Þetta efnisatriði útskýrir hvernig eigi að grunnstilla hvernig sjálfgefin gögn eru slegin inn þegar Microsoft Dynamics 365 for Project Service Automation er samþætt við Microsoft Dynamics 365 for Finance and Operations.
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
ms.openlocfilehash: b58d2de323395db97d1f8ea146da55bba4e0f9c6
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838988"
---
# <a name="project-service-automation-integration-parameters"></a>Færibreytur samþættingar Project Service Automation

[!include[banner](../includes/banner.md)]

Á síðunni **Samþættingarfæribreytur Project Service Automation** er hægt að skilgreina hvernig sjálfgefin gögn eru slegin inn þegar Microsoft Dynamics 365 for Project Service Automation er samþætt við Microsoft Dynamics 365 for Finance and Operations. Ef á að takast að samstilla verk frá Project Service Automation við Finance and Operations þarf að setja upp eftirfarandi svæði.

> [!NOTE]
> - Samþætting verkefna fyrir verk, flokkar kostnaðarfærslna, áætlaður tími, kostnaðaráætlun og virknilæsing eru í boði í Microsoft Dynamics 365 for Finance and Operations útgáfu 8.0.
> - Samþætting á rauntölum er í boði í Microsoft Dynamics 365 for Finance and Operations útgáfu 8.0.1 eða nýrri.
> - Ef þú notar Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3.0, eftir að hafa sett upp KB 4132657 og KB 4132660 getur þú notað sniðmátin til að samþætta verkefni fyrir verk, kostnaðarfærsluflokka, tímaáætlanir, kostnaðaráætlanir og rauntölur og til að stilla virknilæsingu. Ef þú verður að endurstilla dreifingu á fjárhagsupphæð mælum við með að þú setjir einnig upp KB 4131710.

| Flipi                    | Svæði                | lýsing |
|------------------------|----------------------|-------------|
| Almennt                | Sjálfgefin verkgerð | Veldu sjálfgefna verkgerð. Þegar verk eru samstillt frá Project Service Automation er þetta gildi notað ef þú hefur ekki gefið upp sjálfgefið gildi í samþættingarsniðmátinu. Á meðan á samstillingu stendur er reiturinn **Verkgerð** stillt á þetta gildi. Hins vegar er mögulega hægt að uppfæra gildið þegar verksamningslínurnar eru samstilltar frá Project Service Automation. |
|                        | Tímaflokkur        | Veldu sjálfgefinn tímaflokk. Þetta gildi er notað þegar tímaáætlanir eru samstilltar frá Project Service Automation. Þegar tímaáætlanir og rauntímar eru samstilltir frá Project Service Automation er reiturinn **Flokkur** fyrir nýjar tímaspár verks í Finance and Operations stilltur á þetta gildi. |
|                        | Tegund þóknunar         | Veldu sjálfgefna tegund þóknunar. Þetta gildi er notað þegar raunupphæðir þóknunar eru samstilltar frá Project Service Automation. Þegar raunupphæðir þóknunar eru samstilltir frá Project Service Automation er reiturinn **Flokkur** fyrir nýjar tegundir þóknunar í Finance and Operations stilltur á þetta gildi. |
| Sjálfgildi verkflokks | Gerð verks         | Smelltu á **Ný** til að bæta við línu þar sem þú getur valið verkgerðina þar sem á að stilla sjálfgefna verkflokkinn fyrir. Hægt er að velja tiltekna verkgerð aðeins einu sinni í skilgreiningunni. |
|                        | Verkflokkur        | Veldu sjálfgefna verkflokkinn fyrir valda verkgerð. Þegar ný verk eru samstillt frá Project Service Automation mun reiturinn **Verkflokkur** vera stilltur á sjálfgefið gildi fyrir verkgerðina ef þú hefur ekki gefið upp sjálfgefið gildi í samþættingarsniðmátinu. |
| Sjálfgefnar gerðir reiknings  | Reikningsfærsluflokkur         | Smelltu á **Ný** til að bæta við línu þar sem þú getur valið reikningsgerðina þar sem á að stilla sjálfgefinn línueiginleika fyrir. Hægt er að velja tiltekna reikningsgerð aðeins einu sinni í skilgreiningunni. |
|                        | Línueiginleiki        | Veldu sjálfgefinn línueiginleika fyrir valda reikningsgerð. Þegar nýjar tímaáætlanir, nýjar kostnaðaráætlanir eða nýjar rauntölur eru samstilltar frá Project Service Automation verður reiturinn **Línueiginleiki** stilltur á sjálfgefið gildi fyrir reikningsgerðina. |
| Aðgerðarlæsing  | Ekki tiltækt       | Veldu aðgerðina til að slökkva á Finance and Operations fyrir verk og samninga sem koma frá Project Service Automation. Til dæmis getur þú valið að slökkva á möguleikanum á því að breyta samningum og verkum, búa til sundurliðun verkþátta og slá inn vinnukort í Finance and Operations. Bókhaldstengdir reitir verða áfram virkir, jafnvel þótt þeir séu ekki tiltækir samkvæmt færibreytustillingunni. Að sjálfgefnu verða allar aðgerðir virkjaðar. |
