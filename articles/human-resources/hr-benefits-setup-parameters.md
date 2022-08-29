---
title: Stilla færibreytur fríðindastjórnunar og sjálfsafgreiðslu starfsmanna fyrir öll fyrirtæki
description: Skilgreina færibreytur fyrir fríðindastjórnun og sjálfsafgreiðslu starfsmanna í Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e1bae79e47c3fa695ac239320eeee17b1a480f18
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/23/2022
ms.locfileid: "9337312"
---
# <a name="set-benefits-management-and-employee-self-service-parameters-for-all-companies"></a>Stilla færibreytur fríðindastjórnunar og sjálfsafgreiðslu starfsmanna fyrir öll fyrirtæki



Áður en hægt er að setja upp fríðindaáætlanir í Microsoft Dynamics 365 Human Resources þarf að skilgreina færibreytur fyrir fríðindastjórnun. Þessar færibreytur setja sjálfgefin gildi, ástæðukóða og aðra valkosti. 

## <a name="configure-general-parameters"></a>Skilgreina almennar færibreytur

1. Í **Fríðindastjórnun** vinnusvæðinu, undir **Uppsetning**, skaltu velja **Samnýttar færibreytur mannauðs**.

2. Í flipanum **Fríðindastjórnun** skal tilgreina gildi fyrir eftirfarandi reiti:

   | Svæði | lýsing |
   | --- | --- |
   | **Land/svæði** | Reiturinn **Land / svæði** ákvarðar birtingarröð póstnúmera / ríkja. Valið land birtist fyrst á fellilistanum. |
   | **Ástæðukóði skráningar** | Veldu sjálfgefinn ástæðukóða sem á að nota þegar áætlun starfsmanna er búin til við opna skráningu vinnslu. |
   | **Ástæðukóði afturköllunar** | Ástæðukóðinn sem á að nota þegar bótaáætlun starfsmanna er felld niður. Það birtist í valmynd meðan á uppsagnarferlinu stendur. Notendur geta breytt því **Ástæða kóða fyrir afpöntun** ef nauðsynlegt er. |
   | **Ástæðukóði enduropnunar** | Ástæðukóðinn sem á að nota þegar bótaáætlun starfsmanna er enduropnuð. Það birtist í valmynd meðan á uppsagnarferlinu stendur. Notendur geta breytt **Enduropna ástæðukóða** ef nauðsynlegt er. | 
   | **Ástæðukóði viðburðar** | Ástæðukóðinn sem á að nota þegar lífatburður á sér stað. |
   | **Ástæðukóði breytingar á hlutfalli** | Ástæðukóðinn sem á að nota við að hætta við og opna bótaráætlun starfsmanna meðan á breytingu á gengisbreytingum stendur. Það gefur til kynna hvaða færslum var breytt með uppfærsluferli gengisbreytinga. |
   | **Fríðindi árslauna** | Gerir þér kleift að stilla **Árleg launatengd fríðindi** upphæð fyrir starfsmann. Human Resources notar **Árleg launatengd fríðindi** upphæð við ákvörðun tryggingaupphæðar, í stað árlega upphæð fastra launa. |
   | **Hæfur til nýráðningar** | Tilgreinir hvort nýráðningar séu gjaldgengar. |
   | **Skráningartímabil nýrrar ráðningar** | Tímabilið sem nýskráning á leigu er leyfð.</br></br>**Athugið**: Þessi stilling gengur framhjá nýjum nýskráningartímabilum sem þú stillir í hæfisreglu áætlunarinnar. |
   | **Sjálfgefin greiðslutíðni** | Sjálfgefin greiðslutíðni sem á að nota þegar nýjum starfskröftum er bætt við. |
   | **Viðburðir eru virkir** | Virkjar viðburði. |
   | **Fela eyðublöð eldri fríðinda** | Leyfir þér að fela gömul fríðindaeyðublöð. |
   | **Staðfesting á fríðindum** | Sannprófunartextinn sem á að nota við sjálfsafgreiðslukassa. |
   | **Sjálfvirkt val á fulltrúum** | Tilgreinir hvort sjálfkrafa skuli velja á framfæri og styrkþega miðað við hæfi þeirra fyrir áætlunarkosti. |

3. Veldu **Vista**.

## <a name="configure-employee-self-service-parameters"></a>Grunnstilla sjálfsafgreiðslufæribreytur starfsmanns

1. Í **Fríðindastjórnun** vinnusvæðinu, undir **Uppsetning**, skal velja **Færibreytur mannauðs**.

2. Í flipanum **Fríðindastjórnun** skal tilgreina gildi fyrir eftirfarandi reiti:

   | Svæði | lýsing |
   | --- | --- |
   | **Staðfesting á fríðindum** | Sannprófunartextinn sem á að nota við sjálfsafgreiðslukassa. |
   | **Sjálfvirkt val á fulltrúum** | Tilgreinir hvort sjálfkrafa skuli velja á framfæri og styrkþega miðað við hæfi þeirra fyrir áætlunarkosti. |

3. Veljið **Vista**.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
