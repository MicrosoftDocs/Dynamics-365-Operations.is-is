---
title: Algengar spurningar um endurstillingar gagnaskemmu
description: Þetta efnisatriði veitir svör við nokkrum algengum spurningum um endurstillingar gagnaskemmu.
author: jinniew
ms.date: 03/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-05-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 61c7047096f42e71cde5e9ba1ddc59785383795a
ms.sourcegitcommit: d1683d033fc74adbc4465dd26f7b0055e7639753
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/05/2022
ms.locfileid: "8714130"
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
- Financial Reporter samþætting þín er ekki virkjuð. 

    - Þetta þýðir að ekki er lengur verið að samstilla gögn fjárhagsskýrslu við fjárhagsskýrslugagnamarkaðinn þinn. Fjárhagsskýrslan þín er hugsanlega ekki að fá uppfærðar tölur fyrir fjárhagsskýrslur þínar. Þetta gerist venjulega ef þú hefur ekki notað Financial Reporter í langan tíma.
    - Þú verður beðinn um að virkja samþættingu með því að endurstilla gagnamarkaðinn. Þú getur haldið áfram með því að velja **Já**. Þú getur líka valið að endurstilla gagnamarkaðinn síðar. Eftir að samþætting er virkjuð eru fjárhagsgögn þín samstillt í Financial Reporter aftur. 
- Mynstur endurtekinnar endurstillingar á sér stað af einhverjum eftirfarandi ástæðum:

    - **Vantar eða óvænt gögn í skýrslunni** – Ef þú tekur eftir því að gögn vantar skaltu opna stuðningsmiða hjá Microsoft til að skoða skýrslusniðið þitt og hugsanleg vandamál við samstillingu gagna.
    - **Fast samþættingarástand** - Ef þú tekur eftir að samþættingarstaðan er föst í gangi getur það verið vegna mikils magns viðskipta í kerfinu. Þetta ríki mun leysa sig sjálft. Hins vegar, ef þú tekur eftir að samþættingarstaðan er föst í meira en fjórar klukkustundir, opnaðu stuðningsmiða hjá Microsoft. 
   
## <a name="if-i-reset-the-data-mart-will-i-lose-reports-that-ive-already-designed"></a>Ef ég endurstilli gagnaskemmu missi ég þá skýrslur sem ég hef þegar hannað?

Nr. Skýrslurnar þínar eru geymdar í SQL-töflum sem verða ekki fyrir áhrifum af endurstillingu gagnaskemmu. Ef þú hefur áhyggjur af að glata skýrslum sem þú hefur hannað geturðu tekið afrit af þeim hönnunum sem þú vilt ekki týna. Til að taka öryggisafrit af hönnun skal opna skýrsluhönnuð og fara í **Fyrirtæki \> Fyrirtæki \> Einingar \> Útflutningur**.
 
## <a name="do-all-users-have-to-exit-the-system-before-i-can-reset-the-data-mart"></a>Þurfa allir notendur að fara úr kerfinu áður en ég get endurstillt gagnaskemmuna?

Nr. Notendur geta haldið áfram að vinna í kerfinu á meðan endurstilling gagnaskemmu er í gangi. Notendur geta þó ekki nálgast skýrslur sem voru stofnaðar með því að nota Financial Reporter fyrr en endurstillingu lýkur.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
