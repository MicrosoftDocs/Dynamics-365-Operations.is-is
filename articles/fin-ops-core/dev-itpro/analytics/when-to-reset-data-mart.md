---
title: Algengar spurningar um endurstillingar gagnaskemmu
description: Þessi grein veitir svör við nokkrum algengum spurningum um endurstillingar gagnaskemmu.
author: jinniew
ms.date: 03/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-05-06
ms.dyn365.ops.version: 10.0.15
ms.search.form: ''
ms.openlocfilehash: 949bf64fefe2dc70541eb5a94518d6b9fe1d3eb8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289877"
---
# <a name="data-mart-resets-faq"></a>Algengar spurningar um endurstillingar gagnaskemmu

Þessi grein veitir svör við nokkrum algengum spurningum um endurstillingar gagnaskemmu. Endurstilling á gagnaskemmunni getur verið tímafrekt ferli og það fer eftir aðstæðum hvort það sé rétta lausnin. Í þessari grein er því að finna upplýsingar um aðstæður þar sem endurstilling gagnaskemmu gæti hjálpað og einnig aðstæður þar sem ólíklegt er að hún komi að gagni.

## <a name="what-is-a-data-mart-reset"></a>Hvað er endurstilling gagnaskemma?

Endurstilling gagnaskemmu mun slökkva á samþættingarverkum, eyða öllum gögnum gagnaskemmu og síðan virkja samþættingu aftur.

Til að tryggja að gömul gögn séu ekki sett inn er aðeins hægt að hefja endurstillingu gagnaskemmu eftir að núverandi verkefnum er lokið. Ef reynt er að endurstilla gagnaskemmuna áður en öllum verkum er lokið gætu komið upp skilaboð á borð við „Ekki var hægt að endurstilla gagnaskemmu út af virku verki. Reyna skal aftur síðar.

## <a name="when-do-i-have-to-do-a-data-mart-reset"></a>Hvenær þarf að endurstilla gagnaskemmu?

Ef ein eða fleiri eftirfarandi fullyrðinga eiga við um aðstæður þínar getur fyrirtækið þitt notið góðs af endurstillingu gagnaskemmu:

- **Gagnagrunnur forritsins var endurheimtur**
- **Þjónustubeiðni var opnuð** - Tæknimaður hjá notendaþjónustu hefur sagt þér að endurstilla gagnaskemmuna sem hluti af skrefi úrræðaleitar.
- **Stórt hlutfall úreltra færslna** – Úreltar færslur einar og sér réttlæta ekki endilega endurstillingu gagnaskemmu. Há prósenta úreltra gagna geta dregið úr afköstum skýrslugerðar og samþættingar og orðið til þess að meira pláss er notað í gagnagrunninum. Mælt er með að ljúka endurstillingu gagnaskemmu til að fjarlægja úrelt gögn þegar meira en 80% úreltra gagna er í gagnaskemmunni.
 
> [!NOTE]
> Vinnslan við að endurstilla gagnaskemmu verður fyrir áhrifum af fjölda fjárhagsbóka og fjárhagsáætlunarfærslna í gagnagrunninum. Það fer eftir færslufjöldanum í kerfinu, en endurstilling gagnaskemmu getur tekið allt niður í 15 mínútur að klárast eða allt upp í fjórar klukkustundir. Ef endurstillingin tekur hins vegar lengri tíma en fjórar klukkustundir er mælt með því að hafa samband við notendaþjónustuna.
 
## <a name="when-is-a-data-mart-reset-inappropriate"></a>Hvenær á ekki að endurstilla gagnaskemmu?

Hér eru nokkrar aðstæður þar sem við mælum ekki með því að þú endurstillir gagnaskemmuna:

- Vandamál koma upp varðandi samþættingu gagna.
- Samþætting við Financial Reporter er ekki virk. 

    - Þetta þýðir að ekki er lengur verið að samstilla fjárhagsgögn við gagnaskemmu Financial Reporting. Financial Reporter er hugsanlega ekki að fá uppfærðar tölur fyrir fjárhagsskýrslurnar þínar. Þetta á sér yfirleitt stað ef þú hefur ekki notað Financial Reporter í langan tíma.
    - Beðið verður um að virkja samþættingu með því að endurstilla gagnaskemmu. Þú getur haldið áfram með því að velja **Já**. Þú getur einnig valið að endurstilla gagnaskemmuna síðar. Eftir að samþætting er virkjuð eru fjárhagsgögn samstillt í Financial Reporter aftur. 
- Mynstur endurtekinnar endurstillingar á sér stað af einhverjum eftirfarandi ástæðum:

    - **Gögn vantar eða óvænt gögn í skýrslunni** – Ef þú tekur eftir því að gögn vantar skaltu opna þjónustubeiðni hjá Microsoft til að fara yfir skýrslusniðið þitt og möguleg vandamál varðandi samstillingu gagna.
    - **Föst samþættingarstaða** - Ef þú tekur eftir því að samþættingarstaðan er föst í keyrslu getur það verið vegna mikils magns af færslum í kerfinu. Þetta ástand leysist af sjálfu sér. Ef þú tekur hins vegar eftir að samþættingarstaðan er föst í meira en fjórar klukkustundir skaltu opna þjónustubeiðni hjá Microsoft. 
   
## <a name="if-i-reset-the-data-mart-will-i-lose-reports-that-ive-already-designed"></a>Ef ég endurstilli gagnaskemmu missi ég þá skýrslur sem ég hef þegar hannað?

Nr. Skýrslurnar þínar eru geymdar í SQL-töflum sem verða ekki fyrir áhrifum af endurstillingu gagnaskemmu. Ef þú hefur áhyggjur af að glata skýrslum sem þú hefur hannað geturðu tekið afrit af þeim hönnunum sem þú vilt ekki týna. Til að taka öryggisafrit af hönnun skal opna skýrsluhönnuð og fara í **Fyrirtæki \> Fyrirtæki \> Einingar \> Útflutningur**.
 
## <a name="do-all-users-have-to-exit-the-system-before-i-can-reset-the-data-mart"></a>Þurfa allir notendur að fara úr kerfinu áður en ég get endurstillt gagnaskemmuna?

Nr. Notendur geta haldið áfram að vinna í kerfinu á meðan endurstilling gagnaskemmu er í gangi. Notendur geta þó ekki nálgast skýrslur sem voru stofnaðar með því að nota Financial Reporter fyrr en endurstillingu lýkur.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
