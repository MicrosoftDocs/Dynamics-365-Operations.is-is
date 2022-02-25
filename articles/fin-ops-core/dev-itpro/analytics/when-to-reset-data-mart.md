---
title: Algengar spurningar um endurstillingar gagnaskemmu
description: Þetta efnisatriði veitir svör við nokkrum algengum spurningum um endurstillingar gagnaskemmu.
author: jinniew
ms.date: 02/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-05-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 53f45f469c39f9e389763aa0daed658e5a62d377
ms.sourcegitcommit: 6a269db08e8bb3bb3405c9f4a512091d13c80faa
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 02/14/2022
ms.locfileid: "8119513"
---
# <a name="data-mart-resets-faq"></a>Algengar spurningar um endurstillingar gagnaskemmu

Þetta efnisatriði veitir svör við nokkrum algengum spurningum um endurstillingar gagnaskemmu. Endurstilling á gagnaskemmunni getur verið tímafrekt ferli og það fer eftir aðstæðum hvort það sé rétta lausnin. Í þessu efnisatriði er því að finna upplýsingar um aðstæður þar sem endurstilling gagnaskemmu gæti hjálpað og einnig aðstæður þar sem ólíklegt er að hún komi að gagni.

## <a name="what-is-a-data-mart-reset"></a>Hvað er endurstilling gagnaskemma?

Endurstilling gagnaskemmu mun slökkva á samþættingarverkum, eyða öllum gögnum gagnaskemmu og síðan virkja samþættingu aftur.

Til að tryggja að gömul gögn séu ekki sett inn er aðeins hægt að hefja endurstillingu gagnaskemmu eftir að núverandi verkefnum er lokið. Ef reynt er að endurstilla gagnaskemmuna áður en öllum verkum er lokið gætu komið upp skilaboð á borð við „Ekki var hægt að endurstilla gagnaskemmu út af virku verki. Reyna skal aftur síðar.

## <a name="when-do-i-have-to-do-a-data-mart-reset"></a>Hvenær þarf að endurstilla gagnaskemmu?

Ef ein eða fleiri eftirfarandi fullyrðinga eiga við um aðstæður þínar getur fyrirtækið þitt notið góðs af endurstillingu gagnaskemmu:

- **Forritsgagnagrunnurinn var endurheimtur**
- **Þú opnaðir stuðningsmiða** - Stuðningsverkfræðingur sagði þér að endurstilla gagnamarkaðinn sem hluta af bilanaleitarskrefinu.
- **Stórt hlutfall af gömul skrám** - Gömul skrár ein og sér réttlæta ekki endilega endurstillingu gagnamarkaðar. Hátt hlutfall af gömlum gögnum getur dregið úr heildarskýrslugerð og samþættingarafköstum og valdið aukinni notkun gagnagrunnsrýmis. Við mælum með því að þú endurstillir gagnamart til að fjarlægja gamaldags gögn þegar það eru meira en 80% gömul gögn í gagnamerkinu.
 
> [!NOTE]
> Vinnslan við að endurstilla gagnaskemmu verður fyrir áhrifum af fjölda fjárhagsbóka og fjárhagsáætlunarfærslna í gagnagrunninum. Það fer eftir færslufjöldanum í kerfinu, en endurstilling gagnaskemmu getur tekið allt niður í 15 mínútur að klárast eða allt upp í fjórar klukkustundir. Ef endurstillingin tekur hins vegar lengri tíma en fjórar klukkustundir er mælt með því að hafa samband við notendaþjónustuna.
 
## <a name="when-is-a-data-mart-reset-inappropriate"></a>Hvenær á ekki að endurstilla gagnaskemmu?

Hér eru nokkrar aðstæður þar sem við mælum ekki með því að þú endurstillir gagnaskemmuna:

- Þú ert að lenda í gagnasamþættingarvandamálum.
- Mynstur endurtekinnar endurstillingar á sér stað af einhverjum eftirfarandi ástæðum:

    - **Vantar eða óvænt gögn í skýrslunni** – Ef þú tekur eftir því að gögn vantar skaltu opna stuðningsmiða hjá Microsoft til að skoða skýrslusniðið þitt og hugsanleg vandamál við samstillingu gagna.
    - **Föst samþættingarstaða**
   
## <a name="if-i-reset-the-data-mart-will-i-lose-reports-that-ive-already-designed"></a>Ef ég endurstilli gagnaskemmu missi ég þá skýrslur sem ég hef þegar hannað?

Nr. Skýrslurnar þínar eru geymdar í SQL-töflum sem verða ekki fyrir áhrifum af endurstillingu gagnaskemmu. Ef þú hefur áhyggjur af að glata skýrslum sem þú hefur hannað geturðu tekið afrit af þeim hönnunum sem þú vilt ekki týna. Til að taka öryggisafrit af hönnun skal opna skýrsluhönnuð og fara í **Fyrirtæki \> Fyrirtæki \> Einingar \> Útflutningur**.
 
## <a name="do-all-users-have-to-exit-the-system-before-i-can-reset-the-data-mart"></a>Þurfa allir notendur að fara úr kerfinu áður en ég get endurstillt gagnaskemmuna?

Nr. Notendur geta haldið áfram að vinna í kerfinu á meðan endurstilling gagnaskemmu er í gangi. Notendur geta þó ekki nálgast skýrslur sem voru stofnaðar með því að nota Financial Reporter fyrr en endurstillingu lýkur.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
