---
title: Stofna tryggingarvalkosti
description: Umfjöllunarvalkostir í Microsoft Dynamics 365 Human Resources eru umfjöllunarstig fyrir kosningu þátttakenda í bótakerfi eða áætlun.
author: andreabichsel
ms.date: 06/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 447317d0e9cb23bea21dae448048d05a3d989c89df17e4b8ea836201c20aefff
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6741430"
---
# <a name="create-coverage-options"></a>Stofna tryggingarvalkosti

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tryggingarvalkostir ákvarða hverjir eiga að vera tryggðir eða hve mikil trygging er í boði í tryggingaráætlun. Fyrir sjúkraáætlun gætirðu t.d. verið með valkostinn **eingöngu starfsmaður**, valkostinn **starfsmaður + 1** og valkostinn **fjölskylda**. Fyrir líftryggingu er hægt að bjóða upp á tryggingu fyrir **1 x laun** eða **2 x laun**.

Eftir að fríðindavalkostir hafa verið skilgreindir er hægt að endurnýta þá. Þú getur tengt valkost við eina eða fleiri áætlanir.

> [!IMPORTANT]
> Þegar þú hefur skilgreint tryggingarvalkosti skaltu hengja þá við gerð fríðindaáætlunar. Áætlunartegundin er síðan tengd fríðindaáætlun eða áætlun. Tryggingarvalkostir sem eru tengdir áætlunargerð eru í boði fyrir allar áætlanir af þeirri gerð sem er stofnuð.

## <a name="create-coverage-options"></a>Stofna tryggingarvalkosti
1. Í vinnusvæðinu **Fríðindastjórnun**, undir **Skipulag**, veldu **Tryggingarvalkostir**.

2. Veljið **Nýtt**.

3. Tilgreina gildi fyrir eftirfarandi reiti:

   | Svæði | Lýsing |
   | --- | --- |
   | **Tryggingarvalkostur** | Einkvæmt heiti tryggingarkosts. |
   | **Lýsing** | Lýsing á tryggingarvalkostinum. |
   | **Tryggingarkóði** | Tryggingarkóðar úthluta lágmarks- og hámarksfjárhæðum fyrir hverja hæfa tegund þeirra sem fjallað er um. Tryggingarkóði gefur til kynna hverjir eru tryggðir eða umfang tryggingr sem leyfilegt er fyrir áætlunartegund. Þú getur tjáð tryggingna sem dollara eða prósentu. Dæmi:<ul><li>**Starfsm+1** – Til að vera hæfur verður starfsmaðurinn að hafa valið einn tengdan einstakling (ef fleiri en einn er valinn er hann ekki lengur gjaldgengur).</li><li>**Starfsm+fjölskylda** – Til að vera hæfur verður starfsmaðurinn að hafa valið að minnsta kosti tvo tengda einstaklinga.</li></ul> |
   | **Hámarksfjöldi** | Hámarksfjöldi skjólstæðinga. |
   | **Staða** | Staða tryggingravalkosts. Ef staða tryggingarvalkosts er stillt á Óvirk verður ekki hægt að velja tryggingarvalkostinn í áætlunargerðum. |
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
