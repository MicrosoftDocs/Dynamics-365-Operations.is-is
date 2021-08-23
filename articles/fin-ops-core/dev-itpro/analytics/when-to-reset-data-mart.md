---
title: Algengar spurningar um endurstillingar gagnaskemmu
description: Þetta efnisatriði veitir svör við nokkrum algengum spurningum um endurstillingar gagnaskemmu.
author: jinniew
ms.date: 07/16/2021
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
ms.openlocfilehash: e5a40342306eb9888b456a865ab2220dccfe65f8ccecc67bf8fc16f907e06977
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6767756"
---
# <a name="data-mart-resets-faq"></a>Algengar spurningar um endurstillingar gagnaskemmu

Þetta efnisatriði veitir svör við nokkrum algengum spurningum um endurstillingar gagnaskemmu. Endurstilling á gagnaskemmunni getur verið tímafrekt ferli og það fer eftir aðstæðum hvort það sé rétta lausnin. Í þessu efnisatriði er því að finna upplýsingar um aðstæður þar sem endurstilling gagnaskemmu gæti hjálpað og einnig aðstæður þar sem ólíklegt er að hún komi að gagni.

## <a name="what-is-a-data-mart-reset"></a>Hvað er endurstilling gagnaskemma?

Endurstilling gagnaskemmu mun slökkva á samþættingarverkum, eyða öllum gögnum gagnaskemmu og síðan virkja samþættingu aftur.

Til að tryggja að gömul gögn séu ekki sett inn er aðeins hægt að hefja endurstillingu gagnaskemmu eftir að núverandi verkefnum er lokið. Ef reynt er að endurstilla gagnaskemmuna áður en öllum verkum er lokið gætu komið upp skilaboð á borð við „Ekki var hægt að endurstilla gagnaskemmu út af virku verki. Reyna skal aftur síðar.

## <a name="when-do-i-have-to-do-a-data-mart-reset"></a>Hvenær þarf að endurstilla gagnaskemmu?

Ef ein eða fleiri eftirfarandi fullyrðinga eiga við um aðstæður þínar getur fyrirtækið þitt notið góðs af endurstillingu gagnaskemmu:

- Gagnagrunnur forritsins var endurheimtur.
- Þjónustubeiðni var opnuð og tæknimaður hjá notendaþjónustu hefur sagt þér að endurstilla gagnaskemmuna sem hluti af skrefi úrræðaleitar.
 
> [!NOTE]
> Vinnslan við að endurstilla gagnaskemmu verður fyrir áhrifum af fjölda fjárhagsbóka og fjárhagsáætlunarfærslna í gagnagrunninum. Það fer eftir færslufjöldanum í kerfinu, en endurstilling gagnaskemmu getur tekið allt niður í 15 mínútur að klárast eða allt upp í fjórar klukkustundir. Ef endurstillingin tekur hins vegar lengri tíma en fjórar klukkustundir er mælt með því að hafa samband við notendaþjónustuna.
 
## <a name="when-is-a-data-mart-reset-inappropriate"></a>Hvenær á ekki að endurstilla gagnaskemmu?

Hér eru nokkrar aðstæður þar sem við mælum ekki með því að þú endurstillir gagnaskemmuna:

- Þú lendir í vandræðum með afköst sem tengjast gagnasamstillingu.
- Mynstur endurtekinnar endurstillingar á sér stað af einhverjum eftirfarandi ástæðum:

    - **Gögn vantar** – Ef þú tekur eftir því að gögn vantar skaltu opna þjónustubeiðni hjá Microsoft til að fara yfir skýrslusniðið þitt og möguleg vandamál varðandi samstillingu gagna.
    - **Föst samþættingarstaða**
    - **Útrunnar skrár** - Útrunnar skrár einar og sér réttlæta ekki endilega endurstillingu gagnaskemmu. Ef um er að ræða stórt gagnasafn mun endurstillingarferlið taka sinn tíma, en ólíklegt er að það lagi stöðuna.

## <a name="if-i-reset-the-data-mart-will-i-lose-reports-that-ive-already-designed"></a>Ef ég endurstilli gagnaskemmu missi ég þá skýrslur sem ég hef þegar hannað?

Nr. Skýrslurnar þínar eru geymdar í SQL-töflum sem verða ekki fyrir áhrifum af endurstillingu gagnaskemmu. Ef þú hefur áhyggjur af að glata skýrslum sem þú hefur hannað geturðu tekið afrit af þeim hönnunum sem þú vilt ekki týna. Til að taka öryggisafrit af hönnun skal opna skýrsluhönnuð og fara í **Fyrirtæki \> Fyrirtæki \> Einingar \> Útflutningur**.
 
## <a name="do-all-users-have-to-exit-the-system-before-i-can-reset-the-data-mart"></a>Þurfa allir notendur að fara úr kerfinu áður en ég get endurstillt gagnaskemmuna?

Nr. Notendur geta haldið áfram að vinna í kerfinu á meðan endurstilling gagnaskemmu er í gangi. Notendur geta þó ekki nálgast skýrslur sem voru stofnaðar með því að nota Financial Reporter fyrr en endurstillingu lýkur.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
