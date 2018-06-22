---
title: "Samþættingarfæribreytur Project Service Automation"
description: "Þú getur stillt hvernig gögn eiga að vera sjálfgefin við samþættingu Project Service Automation við Dynamics 365 for Finance and Operations."
author: KimANelson
manager: AnnBe
ms.date: 12/13/2017
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
ms.openlocfilehash: 32f7f70c5b1071cef5a3360ccc09fa2d95fbf9a9
ms.contentlocale: is-is
ms.lasthandoff: 05/29/2018

---

# <a name="project-service-automation-integration-parameters"></a>Samþættingarfæribreytur Project Service Automation

Á síðunni **Samþættingarfæribreytur Project Service Automation** getur þú stillt hvernig gögn eiga að vera sjálfgefin við samþættingu Project Service Automation við Finance and Operations. Eftirfarandi verður að vera uppsett svo takist að samstilla verk frá Project Service Automation við Finance and Operations.

> [!NOTE]
> Samþætting verkefna fyrir verk, flokkar kostnaðarfærslna, áætlaður tími, kostnaðaráætlun og virknilæsing er í boði í Dynamics 365 for Finance and Operations útgáfu 8.0.




| **Flipi**                      | **Svæði**                          | **Lýsing**                    |
|------------------------------|------------------------------------|--------------------------------|
| **Almennt**                  | **Sjálfgefin verkgerð**               | Veldu sjálfgefið fyrir **Gerð verks** sem er þegar verk eru samstillt frá Project Service Automation ef þú hefur ekki gefið upp sjálfgefið gildi í samþættingarsniðmátinu. Við samstillingu munu ný verk hafa **Gerð verks** stillt á þetta gildi og hægt er að uppfæra þegar verksamningslínurnar eru samstilltar frá Project Service Automation.               |
| **Almennt**                  | **Tímaflokkur**                      | Veldu sjálfgefið fyrir **Tímaflokk** sem er þegar tímaáætlanir eru samstilltar frá Project Service Automation. Við samstillingu munu nýjar tímaspár verks í Finance and Operations hafa **Flokkinn** stilltan á þetta gildi þegar tímaáætlanir og rauntími eru samstilltir frá Project Service Automation.   |
| **Almennt**                  | **Tegund þóknunar**                       | Veldu sjálfgefið fyrir **Þóknunarflokk** sem er þegar raunupphæðir þóknunar eru samstilltar frá Project Service Automation. Við samstillingu munu nýjar þóknunarfærslur í Finance and Operations hafa **Flokkinn** stilltan á þetta gildi þegar raunupphæðir þóknunar eru samstilltar frá Project Service Automation.          |
| **Sjálfgildi verkflokks**   | **Gerð verks** | Smelltu á **Ný** til að bæta við línu þar sem þú getur valið verkgerðina þar sem á að stilla sjálfgefna verkflokkinn. Hægt er að velja tiltekna verkgerð aðeins einu sinni í skilgreiningunni.              
|                              | **Verkflokkur**          | Veldu sjálfgefna verkflokkinn fyrir tiltekna verkgerð. Þegar ný verk eru samstillt frá Project Service Automation mun **Verkflokkurinn** vera sjálfgefinn á grundvelli verkgerðarinnar ef þú hefur ekki gefið upp sjálfgefið gildi í samþættingarsniðmátinu.  |
| **Sjálfgefnar gerðir reiknings**    | **Reikningsfærsluflokkur** | Smelltu á **Ný** til að bæta við línu þar sem þú getur valið reikningsgerðina þar sem á að stilla sjálfgefinn línueiginleika. Hægt er að velja tiltekna reikningsgerð aðeins einu sinni í skilgreiningunni.          |
|                              | **Línueiginleiki**| Veldu sjálfgefinn línueiginleika fyrir tilgreinda reikningsgerð. Þegar nýjar tímaáætlanir, nýjar kostnaðaráætlanir eða nýjar rauntölur eru samstilltar frá Project Service Automation verður **Línueiginleikinn** sjálfgefinn á grundvelli reikningsgerðarinnar.          |
| **Aðgerðarlæsing**    |                   | Veldu aðgerðina til að slökkva á Finance and Operations fyrir verk og samninga sem koma frá Project Service Automation. Til dæmis getur þú valið að slökkva á möguleikanum til að breyta samningum og verkum, búa til sundurliðun verkþátta og slá inn vinnukort í Finance and Operations. Bókhaldstengdir reitir verða áfram virkir, jafnvel þótt þeir séu ekki tiltækir samkvæmt færibreytustillingunni. Að sjálfgefnu verða allar aðgerðir virkjaðar.           |

