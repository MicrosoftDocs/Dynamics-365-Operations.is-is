---
title: Samþættingarfæribreytur Project Service Automation
description: Þetta efnisatriði útskýrir hvernig eigi að grunnstilla hvernig sjálfgefin gögn eru slegin inn þegar Microsoft Dynamics 365 for Project Service Automation er samþætt við Microsoft Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 03/03/2020
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
ms.openlocfilehash: cd09dad15112fd71bfd386e0072a77a4121c96e0
ms.sourcegitcommit: 236672932ffd0a758012ebb7b2df9bc51249c126
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096252"
---
# <a name="project-service-automation-integration-parameters"></a>Færibreytur samþættingar Project Service Automation

[!include[banner](../includes/banner.md)]

Á síðunni **Samþættingarfæribreytur Project Service Automation** er hægt að skilgreina hvernig sjálfgefin gögn eru slegin inn þegar Dynamics 365 Project Service Automation er samþætt við Dynamics 365 Finance. Ef á að takast að samstilla verk frá Project Service Automation við Finance þarf að setja upp eftirfarandi reiti.

Til að opna síðuna **Stillingum sjálfvirkni verkefnaþjónustunnar**, farðu til **Verkefnisstjórnun og bókhald** \> **Uppsetning** \> **Dynamics 365 for Project Service Automation samþættingarbreytur**. 

> [!NOTE]
> - Samþætting verkefna fyrir verk, flokkar kostnaðarfærslna, áætlaður tími, kostnaðaráætlun og virknilæsing eru í boði í útgáfu 8.0.
> - Samþætting á rauntölum er í boði í útgáfu 8.0.1 eða nýrri.


| Dálkalykill                    | Svæði                | Lýsing |
|------------------------|----------------------|-------------|
| Almennt                | Sjálfgefin verkgerð | Veldu sjálfgefna verkgerð. Þegar verk eru samstillt frá Project Service Automation er þetta gildi notað ef þú hefur ekki gefið upp sjálfgefið gildi í samþættingarsniðmátinu. Á meðan á samstillingu stendur er reiturinn **Verkgerð** stillt á þetta gildi. Hins vegar er mögulega hægt að uppfæra gildið þegar verksamningslínurnar eru samstilltar frá Project Service Automation. |
|                        | Tímaflokkur        | Veldu sjálfgefinn tímaflokk. Þetta gildi er notað þegar tímaáætlanir eru samstilltar frá Project Service Automation. Þegar tímaáætlanir og rauntímar eru samstilltir frá Project Service Automation er reiturinn **Flokkur** fyrir nýjar tímaspár verks í Finance stilltur á þetta gildi. |
|                        | Tegund þóknunar         | Veldu sjálfgefna tegund þóknunar. Þetta gildi er notað þegar raunupphæðir þóknunar eru samstilltar frá Project Service Automation. Þegar raunupphæðir þóknunar eru samstilltir frá Project Service Automation er reiturinn **Flokkur** fyrir nýjar tegundir þóknunar í Finance stilltur á þetta gildi. |
| Sjálfgildi verkflokks | Gerð verks         | Smelltu á **Ný** til að bæta við línu þar sem þú getur valið verkgerðina þar sem á að stilla sjálfgefna verkflokkinn fyrir. Hægt er að velja tiltekna verkgerð aðeins einu sinni í skilgreiningunni. |
|                        | Verkflokkur        | Veldu sjálfgefna verkflokkinn fyrir valda verkgerð. Þegar ný verk eru samstillt frá Project Service Automation mun reiturinn **Verkflokkur** vera stilltur á sjálfgefið gildi fyrir verkgerðina ef þú hefur ekki gefið upp sjálfgefið gildi í samþættingarsniðmátinu. |
| Sjálfgefnar gerðir reiknings  | Reikningsfærsluflokkur         | Smelltu á **Ný** til að bæta við línu þar sem þú getur valið reikningsgerðina þar sem á að stilla sjálfgefinn línueiginleika fyrir. Hægt er að velja tiltekna reikningsgerð aðeins einu sinni í skilgreiningunni. |
|                        | Línueiginleiki        | Veldu sjálfgefinn línueiginleika fyrir valda reikningsgerð. Þegar nýjar tímaáætlanir, nýjar kostnaðaráætlanir eða nýjar rauntölur eru samstilltar frá Project Service Automation verður reiturinn **Línueiginleiki** stilltur á sjálfgefið gildi fyrir reikningsgerðina. |
| Aðgerðarlæsing  | Á ekki við       | Veldu aðgerðina til að slökkva á Finance fyrir verk og samninga sem koma frá Project Service Automation. Til dæmis getur þú valið að slökkva á möguleikanum á því að breyta samningum og verkum, búa til sundurliðun verkþátta og slá inn vinnukort í Finance. Bókhaldstengdir reitir verða áfram virkir, jafnvel þótt þeir séu ekki tiltækir samkvæmt færibreytustillingunni. Að sjálfgefnu verða allar aðgerðir virkjaðar. |
