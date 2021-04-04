---
title: Stofna tryggingarvalkosti
description: Umfjöllunarvalkostir í Microsoft Dynamics 365 Human Resources eru umfjöllunarstig fyrir kosningu þátttakenda í bótakerfi eða áætlun.
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2e1d5fc80d93e41626da8eb5bdf8f389fb0bd531
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466183"
---
# <a name="create-coverage-options"></a>Stofna tryggingarvalkosti

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Umfjöllunarvalkostir í Microsoft Dynamics 365 Human Resources eru umfjöllunarstig fyrir kosningu þátttakenda í bótakerfi eða áætlun. Til dæmis gætu umfjöllunarkostirnir falið í sér **Aðeins starfsmaður** vegna læknisáætlunar, eða **2x laun** vegna líftryggingaráætlunar. Þegar það er skilgreint geturðu notað valkosti um umfjöllun um fríðindi. Þú getur tengt valkost við eina eða fleiri áætlanir.

Þegar þú hefur skilgreint umfjöllunarvalkostina skaltu hengja þá við gerð bótaáætlunar. Áætlunartegundin er síðan tengd fríðindaáætlun eða áætlun. Umfjöllunarvalkostir sem tengjast áætlunartegundum eru tiltækir öllum áætlunum sem eru búnar til með þeirri áætlunartegund. 

1. Í vinnusvæðinu **Fríðindastjórnun**, undir **Skipulag**, veldu **Tryggingarvalkostir**.

2. Veljið **Nýtt**.

3. Tilgreina gildi fyrir eftirfarandi reiti:

   | Svæði | Lýsing |
   | --- | --- |
   | **Tryggingarvalkostur** | Einkvæmt heiti tryggingarkosts. |
   | **Lýsing** | Lýsing á tryggingarvalkostinum. |
   | **Tryggingarkóði** | Tryggingarkóðar úthluta lágmarks- og hámarksfjárhæðum fyrir hverja hæfa tegund þeirra sem fjallað er um. Tryggingarkóði gefur til kynna hverjir eru tryggðir eða umfang tryggingr sem leyfilegt er fyrir áætlunartegund. Þú getur tjáð tryggingna sem dollara eða prósentu. Dæmi:</br></br>- **Emp+1** - til að vera hæfur verður starfsmaðurinn að vera valinn einn háður (ef fleiri en einn eru valdir, þá fullnægir hann ekki lengur).</br></br>- **Emp+fjölskylda** - til að vera hæfur verður starfsmaður að velja að minnsta kosti tvo á framfæri. |
   | **Hámarksfjöldi** | Hámarksfjöldi skjólstæðinga. |
   | **Staða** | Staða tryggingravalkosts. Ef staða tryggingarvalkostsins er stillt á Óvirk er ekki hægt að velja tryggingarvalkostinn á áætlunartegundum. |
   | **Prósenta** | Prósentuupphæðin. Þessi reitur er aðeins virkur ef% x Laun var valið í reitnum tryggingarkóða. |
   | **Deilir** | Skiptingin sem á að nota við útreikninginn þegar þú velur tryggingarkóðann% x laun. |
   | **Lágmarksprósentuhlutfall** | Lágmarksprósentan þegar þú velur prósentu tryggingarkóða. |
   | **Hámarksprósentuhlutfall** | Hámarksprósentan þegar þú velur prósentu tryggingarkóða. |

4. Undir **Valmöguleikar persónulegra tengiliða**, hengja viðeigandi valkosti persónulegra tengiliða við hvern tryggingarkost.

5. Undir **Sjálfsafgreiðsla starfsmanns** skal tilgreina gildi fyrir eftirfarandi reiti:

   | Svæði | Lýsing |
   | --- | --- |
   | **Leyfa upphæð á framlagi starfsmanns** | Tilgreinir hvort leyfa eigi starfsmönnum að breyta framlagsfjárhæð í sjálfsafgreiðslu bóta þegar þeir velja bætur. Ef þú velur þennan gátreit mun kerfið reikna út breytur bótaáætlunar miðað við framlagsupphæð sem starfsmaður leggur inn í sjálfsafgreiðslu bóta. |
   | **Leyfa tryggingarupphæð starfsmanns** | Tilgreinir hvort leyfa eigi starfsmönnum að breyta tryggingarfjárhæð í sjálfsafgreiðslu bóta þegar þeir velja bætur. Ef þú velur þennan gátreit mun kerfið reikna út breytur bótaáætlunar miðað við tryggingarupphæð sem starfsmaður leggur inn í sjálfsafgreiðslu starfsmanna. |

6. Veljið **Vista**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]