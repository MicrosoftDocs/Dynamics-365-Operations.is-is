---
title: Framboðsáætlun
description: Þetta efnisatriði veitir upplýsingar um síðu framboðsáætlunar og möguleika hennar.
author: t-benebo
ms.date: 9/3/2021
ms.topic: article
ms.search.form: ReqSupplyDemandSchedule, ReqSupplyDemandScheduleFilters, ReqSupplyDemandItemDetails, ReqTransFuturesActionsPart, ReqSupplyDemandOverviewLegendPart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-06-09
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 89b8ce96a5c34902187751cfa523ed99a94500b3
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/23/2022
ms.locfileid: "8468677"
---
# <a name="supply-schedule"></a>Framboðsáætlun

[!include [banner](../includes/banner.md)]

Á síðunni **Framboðsáætlun** er sýnt ítarlegt yfirlit yfir framboð og eftirspurn á afurð eða afurðasafni. Upplýsingarnar eru síaðar eftir staðsetningu, aðaláætlun og tímabilum. Þú getur einnig notað síðuna til að búa til nýjar pantanir, breyta fyrirliggjandi áætluðum pöntunum og keyra aðaláætlanagerð.

## <a name="open-the-supply-schedule-page"></a>Opnaðu birgðaáætlunarsíðu

Hægt er að opna síðuna **Birgðaáætlun** á eftirfarandi hátt:

- Farðu í **Aðaláætlanagerð \> Aðaláætlanagerð \> Birgðaáætlun**. Í svarglugganum **Breyta síu** skal tilgreina áætlunina og afurðina sem leitað er að með því að slá inn síugildi í reitina sem gefnir eru upp. (Það sem eftir er af þessu efnisatriði verður vísað í safn af síugildum sem „sían“ eða „núgildandi sía“.) Þegar þessu er lokið skal velja **Í lagi**.
- Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**. Velja eða opna afurð. Því næst á aðgerðasvæðinu, í flipanum **Áætlun**, í flokknum **Yfirlit**, skal velja **Birgðaáætlun**.
- Farðu í **Aðaláætlanagerð \> Uppsetning \> Eftirspurnarspá \> Úthlutunarlyklar vöru**. Veldu úthlutunarlykil vöru sem er notaður sem afurðasafn. Í aðgerðasvæðinu er **Birgðaáætlun** síðan valin.
- Fara í **Áætlanagerð \> Aðaláætlanagerð \> Áætlaðar pantanir**. Velja eða opna áætlaða pöntun. Á aðgerðasvæðinu, í flipanum **Yfirlit**, í flokknum **Yfirlit**, skal síðan velja **Birgðaáætlun**.

> [!NOTE]
> Þegar þú opnar síðuna **Birgðaáætlun** úr afurð, afurðasafni eða áætlaðri pöntun þarf ekki að slá inn síugildi. Kerfið notar sjálfgefna tímabilssniðmátið.

## <a name="use-the-supply-schedule-page"></a>Notaðu birgðaáætlunarsíðu

Síðan **Birgðaáætlun** samanstendur af efri hluta, flýtiflipanum **Birgðir við lok tímabils**, aukalegum flýtiflipa sem verður sýnilegur, byggt á línunni sem er valin í efri hlutanum og glugga upplýsingakassans. (Til að opna glugga upplýsingakassa og skoða hann skal velja **Tengdar upplýsingar** lengst til hægri á síðunni.)

### <a name="upper-section"></a>Efri hluti

Í efri hluta síðunnar **Birgðaáætlun** er að finna hnitanet sem sýnir eftirfarandi gögn fyrir afurð eða afurðasafn. Þessi gögn eru sundurliðuð eftir tímabilum sem eru skilgreind af gildinum **Tímabilssniðmát** úr síunni.

- **Birgðir við upphaf tímabils** – Þessi lína sýnir væntanlega birgðastöðu í upphafi tímabilsins ef allar pantanir í kerfinu koma upp.
- **Birgðir við lok tímabils** – Þessi lína sýnir væntanlega birgðastöðu í lok tímabilsins ef allar pantanir í kerfinu koma upp.
- **Þarfaraktar birgðir við lok tímabils** – Þessi lína sýnir magn birgða við lok tímabils sem eru þarfaraktar gagnvart eftirspurn fram í tímann.
- **Nettóframboð tímabils** – Þessi lína sýnir muninn milli framboðs og eftirspurnar á tímabilinu.
- **Lágmarksbirgðir** – Þessi hnútur sýnir öryggisbirgðir fyrir afurð eða afurðasafn. Til að stækka eða fella saman þennan hnút skal velja hann og velja svo **Stækka** eða **Fella saman** á tækjastikunni. Þessi hnútur er aðeins sýndur þegar öryggisbirgðir eru til staðar fyrir afurðina eða afurðasafnið.
- **Eftirspurn** – Þessi hnútur sýnir eftirspurn eftir afurð eða afurðasafni. Eftirspurnin er flokkuð eftir færslugerð. Til að stækka eða fella saman þennan hnút skal velja hann og velja svo **Stækka** eða **Fella saman** á tækjastikunni. Færslugerðir eftirspurnar fela í sér sölu, flutning og birgðabækur. Þessi hnútur er aðeins sýndur þegar eftirspurn er eftir afurðinni eða afurðasafninu.
- **Framboð** – Þessi hnútur sýnir framboð eftir afurð eða afurðasafni. Framboð er flokkað eftir færslugerð. Til að stækka eða fella saman þennan hnút skal velja hann og velja svo **Stækka** eða **Fella saman** á tækjastikunni. Færslugerðir framboðs fela í sér framleiðslu, innkaup og flutninga. Þessi hnútur er aðeins sýndur þegar framboð er eftir afurðinni eða afurðasafninu.

Margir tækjastikuhnapparnir sem eru í boði, skjámyndir upplýsingakassa og skjámyndir flýtiflipa fara eftir vali þínu í efri hlutanum. Venjulega velur þú færslugerð með því að velja eina af línunum undir hnútnum **Framboð** eða **Eftirspurn**. Þú velur þá tímabil með því að velja tiltekinn dálk fyrir völdu línuna.

Tækjastikan fyrir ofan hnitanetið í efri hluta síðunnar **Birgðaáætlun** býður upp á eftirfarandi hnappa:

- **Stækka/fella saman** – Stækka eða fella saman valdan hnút á borð við hnútinn **Eftirspurn**, hnútinn **Framboð** og undirhnúta þeirra. (Hnútar sýna forskeyti **\[+\]** eða **\[-\]** til að gefa til kynna hvort þeir séu samanfelldir eða stækkaðir.)
- **Nýtt** – Opnaðu valmynd þar sem hver skipun fyrir vikið opnar svarglugga eða síðu sem gerir þér kleift að bæta við tiltekinni gerð af vöru fyrir valið. Fáanlegar skipanir fela m.a. í sér **Framboðsspá**, **Áætluð pöntun**, **Áætlað kanban**, **Ný framleiðslupöntun**, **Innkaupapöntun** og **Flutningspöntun**.
- **Aðaláætlanagerð** – Keyra aðaláætlanagerð. Svargluggi birtist þar sem getur þú tilgreint áætlunina sem á að keyra. Reiturinn **Aðaláætlun** er sjálfgefið stilltur á að passa við núverandi síu.
- **Hámark þess sem tilkynna má tilbúið** – Opnaðu síðuna **Hámark þess sem tilkynna má tilbúið** fyrir afurðina sem er skilgreind í núverandi síu.
- **Uppfæra áætlaðar pantanir** – Opnaðu síðu **Áætlaðar pantanir** sem sýnir áætlaðar pantanir fyrir afurðina eða afurðasafnið sem er skilgreint í núverandi síu.
- **Stig** – Dreifa áætluðum pöntunum samkvæmt stillingunum úr svarglugganum sem birtist.
- **Efnisáætlunarregla eftir staðsetningu** – Opnaðu síðuna **Vöruþekja** fyrir afurðina sem er skilgreind í núverandi síu.
- **Kanban-regla** – Opnaðu síðuna **Kanban-regla** fyrir afurðina sem er skilgreind í núverandi síu.

### <a name="fasttabs"></a>flýtiflipar

Síðan **Framboðsáætlun** getur innihaldið eftirfarandi flýtiflipa:

- **Birgðir við lok tímabils** – Þessi flýtiflipi sýnir birgðagögn við lok tímabils á myndrænu sniði.
- **Forstilling framboðs** – Þessi flýtiflipi sýnir gögn framboðs á myndrænu sniði. Hún verður sýnileg þegar þú velur hnútinn **Framboð** eða línu fyrir neðan hana í efri hlutanum.
- **Samantekt** – Þessi flýtiflipi sýnir upplýsingar um samantekt sem tengjast færslugerðinni sem þú valdir í efri hlutanum. Ef þú velur til dæmis **Sala** undir hnútnum **Eftirspurn** sýnir þessi flýtiflipi reiti sem tengjast sölupöntunum á borð við **Umbeðnar sölupöntunarlínur** eða **Heildarupphæð**. Ef þú velur **Framleiðslupantanir** undir undirhnútnum **Framleiðsla** í hnútnum **Framboð** sýnir þessi flýtiflipi reiti sem tengjast framleiðslupöntunum á borð við **Áætlaðar framleiðslupantanir** eða **Samtals áætlað**. Reitargildi fara eftir tímabilinu sem þú valdir í efri hlutanum. 
- **\[Færslugerð\] - \[Tímabil\]** – Þessi flýtiflipi sýnir pantanir fyrir færslugerðina og tímabilið sem þú valdir í efri hlutanum. Heiti flýtiflipans endurspeglar þetta val. Til dæmis mætti nefna það **Sölupantanir - ólokið** eða **Framleiðslupantanir - Vika 37**.

### <a name="action-pane"></a>Aðgerðasvæði

Eftirfarandi hnappar eru í boði á aðgerðasvæði:

- **Breyta síu** – Opnaðu svargluggann **Breyta síu** þar sem þú getur uppfært síugildi og síðan opnað aftur síðuna **Framboðsáætlun** sem endurspeglar uppfærðar síustillingar.
- **Sýna tafir** – Merktu sérstaklega viðeigandi línur í efri hlutanum ef til er seinkuð pöntun af þessari færslugerð.

### <a name="factbox-pane"></a>Svæði upplýsingareits

Til að opna glugga upplýsingareits og skoða hann skal velja **Tengdar upplýsingar** lengst til hægri á síðunni. Eftirfarandi upplýsingareitir eru í boði á síðunni **Framboðsáætlun**:

- **Upplýsingar um vöru** – Þessi upplýsingareitur sýnir grunnupplýsingar um afurðina sem er skilgreind í núverandi síu. Hann er auður ef þú skilgreindir afurðasafn í síunni.
- **Aðgerðir** – þessi upplýsingareitur sýnir aðgerðir fyrir pantanir af færslugerðinni sem þú valdir í efri hlutanum.
- **Tafir** – þessi upplýsingareitur sýnir tafir fyrir pantanir af færslugerðinni sem þú valdir í efri hlutanum.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
