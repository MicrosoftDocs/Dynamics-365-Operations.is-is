---
title: "Yfirlit yfir stjórnun mannafla"
description: "Þetta efnisatriði lýsir hvernig nota má þjónustuna Stjórnun mannafla (WFM) til að nýta þekkta POS-biðlara, Modern POS og Cloud POS, til að auðvelda verslunarstjórum að stjórna mannafla."
author: shalabhjainmsft
manager: AnnBe
ms.date: 7/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Core
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2017-07-30
ms.dyn365.ops.version: Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: d67ad79c068651f32ce7dc776bc460698557bc29
ms.openlocfilehash: f747dce6b9595de50297cb5af7db523d5f26a844
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---

# <a name="workforce-management-overview"></a>Yfirlit yfir stjórnun mannafla

[!include[banner](includes/banner.md)]
    
Stjórnun mannafla (WFM) nýtir þekkta POS-biðlara, Modern POS og Cloud POS, til að auðvelda verslunarstjórum að stjórna mannafla. WFM-þjónustan notar ramma viðbóta til að sækja viðkomandi pakka í POS. Pakkarnir eru sóttir þegar POS er lokað eða opnað aftur. Því verður að loka POS-appinu og opna það aftur þegar Microsoft gefur út nýja eiginleika fyrir WFM.

Með því að nota þessa þjónustu geta verslunarstjórar auðveldlega stofna ðg birt vikulegar verkáætlanir fyrir verslanir. Starfsmenn verslana get svo skoðað eigin áætlun og áætlun samstarfsmanna í flýti. Þannig sjá þeir hver á að vinna með þeim á úthlutuðum vöktum. Starsfmenn verlsana geta einnig stofnað beiðnir um frávistir, vaktaskipti og boðist til að taka vaktir. Allar þessar beiðnir búa til skilgreint verkflæði.

Á meðan vakt stendur fyrir getur starfsfólk verlsunar nýtt sér inn- og útstimplunareiginlegika sem er innbyggður í POS-biðlara. Gögn eru svo send í höfuðstöðvar til úrvinnslu launa. Innstimplun og útstimplun er fyrirliggjandi eiginleiki í POS. Nánar upplýsingar um uppsetningu og studdar aðstæður eru í [Innstimplun og útstimplun](retail-time-attendance.md).

## <a name="supported-scenarios"></a>Studdar aðstæður
Í þessum hluta eru frekari upplýsingar um studdar aðstæður.

- **Búa til og birta áætlanir** – Þjónustan WFM notar POS-heimildir sem eru skilgreindar í höfuðstöðvum til að ákvarða hvort starfsmaður hefur réttindi verslunarstjóra. Aðeins verslunarstjórar geta stofnað og birt áætlanir með því að nota virknina Verkáætlunarkerfi. Þeir geta í flýti stofnað áætlun með því að afrita og líma fyrirliggjandi vinnuvakt frá einum starfskrafti til annars. Einnig er hægt að stofna áætlun með því að fluytja áætlun úr hvaða fyrri viku sem er inn í núverandi viku.

    Ef áætlun er ekki birt er hún með stöðuna Drög og lítur öðruvísi út en birt áætlun. Verslunarstjórar geta birt áætlun með því að smella á hnappur **Birta** fyrir hvaða viku sem er. Eftir að áætlun hefur verið birt fyrir viku verða allar breytingar birtar sjálfkrafa. Dæmi um breytingar eru að bæta við eða eyða vöktum eða fjarvistum eða breytingar á vöktum eða fjarvistum. Starfsmenn verslunar geta aðeins skoðað áætlanir sem hafa verið birtar fyrir nokkrar vikur.
    
- **Stofna og samþykkja beiðnir** – Starfsmenn verslunar geta stofnað þrjár gerðir af beiðnum:

    - Beiðni um fjarvist
    - Beiðni um vaktaskipti
    - Beiðni um vaktatilboð

    Hægt er að stofna þessar beiðnir með því að nota Beiðnir. Hver beiðni fylgir skilgreindu vinnuflæði og starfsmenn geta auðveldlega séð núverandi stöðu beiðna sinna.
    
    Fjarvistabeiðnir eru sendar sjálfkrafa til verslunarstjóra til samþykktar. Ef það eru margir verslunarstjórar geta allir stjórnendur skoðað tiltekna beiðni, en aðeins einn stjórnandi getur samþykkt eða hafnað henni. Fjarvistagerðir eru stilltar í Retail HQ með því að nota **Gerðir leyfis og fjarvista** í **Retail** einingunni. Eftir að verslunarstjóri samþykkir eða hafnar beiðni er hún flutt í flipann **Ferill** fyrir Beiðniaðgerðina.
    
    Beiðnir um vaktaskipti eða vaktatilboð fer fyrst til starfsmannsins sem beiðnin var send til. Verslunarstjórinn getur aðeins skoðað beiðnina eftir að þessi starfsmaður hefur samþykkt hana. Þess vegna getur stjórnandinn ekki skoðað hana ef starfsmaður hafnar vaktaskiptum eða vaktatilboði. Starfsmaðurinn sem stofnaði beiðnina getur einnig hætt við hana áður en stjórnandinn samþykkir hana neitar.

- **Sýna virka starfsmenn á áætlunarskjá** - Þegar starfsmanni er bætt í verslun með því t.d. að tengja hann eða hana með heimilisfangaskrá starfsmanna verslunarinnar, verður starfsmaður tiltækur í áætlun í WFM-þjónustunni. Endurtekin runuvinnsla sem kallast **Vinna úr gögnum um starfsfólk fyrir stjórnun mannafla** er keyrð í HQ. Þetta starf undirbýr tengsl starfsmanna sem verða send til Common Data Service (CDS).

    Sama ferli er notað þegar starfskraftur er fjarlægður úr verslun. Hins vegar er starfsmaðurinn sem er fjarlægður ennþá sýndur í fyrri, núverandi og framtíðarvikum ef virk vakt eða fjarvera er úthlutað á hann. Starfsmaður mun áfram birtast í þessum vikum nema þessum vöktum og fjarveru sé eytt.

