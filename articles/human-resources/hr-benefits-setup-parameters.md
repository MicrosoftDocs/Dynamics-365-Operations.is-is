---
title: Stilla færibreytur fríðindastjórnunar
description: Stilla færibreytur fyrir ávinningastjórnun í Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ab9b1fc78ce42479d9265b80337adf899cec3866
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009419"
---
# <a name="set-benefits-management-parameters"></a>Stilla færibreytur fríðindastjórnunar

[!include [banner](includes/preview-feature.md)]

Áður en þú getur sett upp leyfisáætlanir í Microsoft Dynamics 365 Human Resources, þú þarft að stilla breytur stjórnunar fríðinda. Þessar færibreytur setja sjálfgefin gildi, ástæðukóða og aðra valkosti.

## <a name="configure-general-parameters"></a>Skilgreina almennar færibreytur

1. Í vinnusvæðinu **Fríðindastjórnun**, undir **Skipulag**, veldu **Færibreytur**.

2. Í flipanum **Almennt** skal tilgreina gildi fyrir eftirfarandi reiti:

   | Svæði | Lýsing |
   | --- | --- |
   | **Land/svæði** | Reiturinn **Land / svæði** ákvarðar birtingarröð póstnúmera / ríkja. Valið land birtist fyrst á fellilistanum. |
   | **Ástæðukóði skráningar** | Veldu sjálfgefinn ástæðukóða sem á að nota þegar áætlun starfsmanna er búin til við opna skráningu vinnslu. |
   | **Ástæðukóði afturköllunar** | Ástæðukóðinn sem á að nota þegar bótaáætlun starfsmanna er felld niður. Það birtist í valmynd meðan á uppsagnarferlinu stendur. Notendur geta breytt því **Ástæða kóða fyrir afpöntun** ef nauðsynlegt er. |
   | **Ástæðukóði enduropnunar** | Ástæðukóðinn sem á að nota þegar bótaáætlun starfsmanna er enduropnuð. Það birtist í valmynd meðan á uppsagnarferlinu stendur. Notendur geta breytt **Enduropna ástæðukóða** ef nauðsynlegt er. | 
   | **Ástæðukóði viðburðar** | Ástæðukóðinn sem á að nota þegar lífatburður á sér stað. |
   | **Ástæðukóði breytingar á hlutfalli** | Ástæðukóðinn sem á að nota við að hætta við og opna bótaráætlun starfsmanna meðan á breytingu á gengisbreytingum stendur. Það gefur til kynna hvaða færslum var breytt með uppfærsluferli gengisbreytinga. |
   | **Hæfur til nýráðningar** | Tilgreinir hvort nýráðningar séu gjaldgengar. |
   | **Skráningartímabil nýrrar ráðningar** | Tímabilið sem nýskráning á leigu er leyfð.</br></br>**Athugið**: Þessi stilling gengur framhjá nýjum nýskráningartímabilum sem þú stillir í hæfisreglu áætlunarinnar. | 
   | **Aukning árslauna** | Tilgreinir hvort reikna eigi sjálfkrafa **Árleg hlunnindi** upphæð í **Upplýsingar um atvinnubætur**. Það er byggt á starfsmanni **Fast hlutfall bóta**, **Meðaltími** og **Greiðslutíðni**.</br></br>**Meðaltími** x **Fast launagengi** x **Greiðslutíðni** (# launatímabil) = **Árleg hlunnindi** </br></br>Ef eitthvað af gildunum í **Meðaltími**, **Fast hlutfall bóta** eða **Greiðslutíðni** reitir breytast, kerfið reiknar sjálfkrafa út starfsmanninn **Árleg hlunnindi** upphæð miðað við breytt gildi. Kerfið býr til **Dagsetning gildi** skrá til að bera kennsl á nákvæma dagsetningu og tíma breytingin átti sér stað. Þú getur breytt handvirkt **Árleg hlunnindi** upphæð ef nauðsyn krefur. |
   | **Viðburðir eru virkir** | Virkjar viðburði. |
   | **Fela eyðublöð eldri fríðinda** | Leyfir þér að fela gömul fríðindaeyðublöð. |

3. Veljið **Vista**.

## <a name="configure-employee-self-service-parameters"></a>Grunnstilla sjálfsafgreiðslufæribreytur starfsmanns

1. Í vinnusvæðinu **Fríðindastjórnun**, undir **Skipulag**, veldu **Færibreytur**.

2. Í flipanum **Sjálfsafgreiðsla starfsmanns** skal tilgreina gildi fyrir eftirfarandi reiti:

   | Svæði | Lýsing |
   | --- | --- |
   | **Staðfesting á fríðindum** | Sannprófunartextinn sem á að nota við sjálfsafgreiðslukassa. |
   | **Sjálfvirkt val á fulltrúum** | Tilgreinir hvort sjálfkrafa skuli velja á framfæri og styrkþega miðað við hæfi þeirra fyrir áætlunarkosti. |

3. Veljið **Vista**.
