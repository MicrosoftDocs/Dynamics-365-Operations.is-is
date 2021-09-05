---
title: Stofna tryggingarvalkosti
description: Þetta efnisatriði lýsir tryggingarvalkostum í Microsoft Dynamics 365 Human Resources fyrir kosningu þátttakanda í fríðindaáætlun eða -pakka.
author: twheeloc
ms.date: 08/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a553fa1aa4bac0d2fb11b87ee05e4e52c019411d
ms.sourcegitcommit: 8592c661b41f9cef8b7ef2863a3b97bf49a4e6f9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/26/2021
ms.locfileid: "7423521"
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
   | **Staða** | Staða tryggingravalkosts. Ef staða tryggingarvalkosts er stillt á **Óvirk** verður ekki hægt að velja tryggingarvalkostinn í áætlunargerðum. |
   | **Prósenta** | Prósentuupphæðin. Þessi reitur er aðeins virkur ef% x Laun var valið í reitnum tryggingarkóða. |
   | **Deilir** | Skiptingin sem á að nota við útreikninginn þegar þú velur tryggingarkóðann% x laun. |
   | **Lágmarksprósentuhlutfall** | Lágmarksprósentan þegar þú velur prósentu tryggingarkóða. |
   | **Hámarksprósentuhlutfall** | Hámarksprósentan þegar þú velur prósentu tryggingarkóða. |

4. Undir **Valmöguleikar persónulegra tengiliða**, hengja viðeigandi valkosti persónulegra tengiliða við hvern tryggingarkost.

5. Undir **Sjálfsafgreiðsla starfsmanns** skal tilgreina gildi fyrir eftirfarandi reiti:

   | Svæði | Lýsing |
   | --- | --- |
   | **Leyfa upphæð á framlagi starfsmanns** | Tilgreinir hvort starfsmönnum sé leyft að breyta upphæðum framlaga í sjálfsafgreiðslu fríðinda þegar þeir velja fríðindi. Þegar þessi gátreitur er valinn reiknar kerfið út færibreytur fríðindaáætlunarinnar miðað við upphæð framlagsins sem starfsmaðurinn færir inn í sjálfsafgreiðslu fríðinda. |
   | **Leyfa tryggingarupphæð starfsmanns** | Tilgreinir hvort starfsmönnum sé leyft að breyta upphæðum trygginga í sjálfsafgreiðslu fríðinda þegar þeir velja fríðindi. Ef þú velur þennan gátreit mun kerfið reikna út breytur bótaáætlunar miðað við tryggingarupphæð sem starfsmaður leggur inn í sjálfsafgreiðslu starfsmanna. |

6. Veljið **Vista**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
