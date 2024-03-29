---
title: Setja upp sveigjanlegar útgjaldaáætlanir
description: Þú getur notað flex kredit forrit í Microsoft Dynamics 365 Human Resources að skrá starfsmenn í bætur samkvæmt fyrirfram ákveðnum fjölda sveigjanlegra eininga.
author: twheeloc
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitCreditPrograms, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ff3bd2c4d39a4411b5a5cb82e4281ff4af98ff0d
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/23/2022
ms.locfileid: "9337297"
---
# <a name="set-up-flex-credit-programs"></a>Setja upp sveigjanlegar útgjaldaáætlanir

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Þú getur notað flex kredit forrit í Microsoft Dynamics 365 Human Resources að skrá starfsmenn í bætur samkvæmt fyrirfram ákveðnum fjölda sveigjanlegra eininga. Starfsmenn geta valið hvernig þeir eiga að úthluta sveigjanlegum einingum. Til dæmis, ef starfsmaður fellur undir sjúkratryggingaráætlun maka síns, gæti verið að hann vilji nota inneignina sem þeir hefðu annars notað á heilsuvernd gagnvart öðrum bótum. 

1. Í vinnusvæðinu **Fríðindastjórnu**, undir **Áætlanir**, veldu **Flex lánstraust forrit**.

2. Veljið **Nýtt**.

3. Tilgreina gildi fyrir eftirfarandi reiti:

   | Svæði | Lýsing |
   | --- | --- |
   | **Auðkenni fríðindaútgjalda** | Einstakt auðkenni Flex Credit áætlunarinnar. |
   | **Lýsing** | Lýsing á flex kredit forritinu. | 
   | **Dagsetning frá** | Dagsetningin þegar flex-lánsfjáráætlunin verður virk. |
   | **Lokadagsetning** | Lokadagsetningin þegar flex-lánsfjáráætlunin. Þú getur skilið eftir sjálfgefið gildi (12/31/2154) til að gefa til kynna að flex kredit forritið sé ekki með áætlaðan lokun. |
   | **Útgjaldavirði samtals** | Fjöldi eininga sem hver starfsmaður verður að nota fyrir fríðindi sín. |
   | **Hlutfallsskiptaregla** | Reglan sem nota á til að pródata flex-einingar þegar starfsmaður er ráðinn á miðju flex-lánstímabilinu. </br></br><ul><li>**Enginn** - Starfsmaðurinn fær engin sveigjanleiki ef þeir eru ráðnir eftir að tímabil lánsfjárlána hefst.</li><li>**Full inneign** - Starfsmaðurinn fær alla upphæð sveigjanlegra eininga, óháð því hvenær þeir eru ráðnir.</li><li>**Hlutfallsskipta** - Starfsmaðurinn fær hlutfallslegt magn af flex-einingum miðað við upphafsdag.</li></ul> |
   | **Hlutfallsskiptaformúla sveigjanlegra útgjalda** | Reglan sem nota á til að pródata flex-einingar fyrir starfsmenn sem eru ráðnir á miðju fríðindatímabili fyrir flex-lánstímabilið. Ræktunin byggist á upphafsdegi ráðningarinnar. Þessi reitur er aðeins notaður ef þú velur það **Hlutfallsskipta** í reitnum **Hlutfallsregla**. </br></br><ul><li>**Daglega** - Hlutfallsskiptir fjölda sveigjanlegra eininga sem starfsmaður fær til dags. Heildarfjöldi sveigjanlegra eininga er deilt með fjölda daga á tímabilinu. Til dæmis, ef fríðindatímabil þitt er 400 dagar, mun kerfið skipta heildarfjölda sveigjanlegra eininga um 400 til að reikna út fjölda sveigjanlegra eininga sem starfsmenn fá á dag.</li><li>**Núverandi mánuður** - Hlutfallsskiptir fjölda sveigjanlegra eininga sem starfsmaður fær til mánaðarstigs, námundaður að núverandi mánuði. Heildarfjöldi sveigjanlegra eininga er deilt með fjölda mánaða á tímabilinu. Til dæmis, ef fríðindatímabil þitt er 15 mánuðir, mun kerfið skipta heildarfjölda sveigjanlegra eininga um 15 til að reikna út fjölda sveigjanlegra eininga sem starfsmenn fá á mánuði.</li><li>**Næsti mánuður** - Hlutfallsskiptir fjölda sveigjanlegra eininga sem starfsmaður fær til mánaðarstigs, námundaður að næsta mánuði. Heildarfjöldi sveigjanlegra eininga er deilt með fjölda mánaða á tímabilinu. Til dæmis, ef fríðindatímabil þitt er 15 mánuðir, skiptir kerfið heildarfjölda sveigjanlegra eininga um 15 til að reikna út fjölda sveigjanlegra eininga sem starfsmenn fá á mánuði.</li></ul> |
   


[!INCLUDE[footer-include](../includes/footer-banner.md)]
