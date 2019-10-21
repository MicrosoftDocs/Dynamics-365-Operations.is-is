---
title: Skrá frestaðar tekjur
description: Í þessu efnisatriði er að finna upplýsingar um hvernig á að skrá tekjur með því að nota tekjuskráningareiginleikann.
author: kweekley
manager: aolson
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 244321e1eb246c46260326a8892924d9d9da75d3
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175971"
---
# <a name="recognize-deferred-revenue"></a>Skrá frestaðar tekjur

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!NOTE]
> Eins og er ekki hægt að kveikja á tekjuskráningareiginleikanum í gegnum eiginleikastjórnun. Nota verður skilgreiningarlykil til að kveikja á honum.

Þetta efnisatriði lýsir ferlinu við að skrá tekjur í tekjuskráningaráætlun. Þegar búið er að bóka reikning fyrir sölupöntun er tekjuskráningaráætlun stofnuð fyrir hverja sölupöntunarlínu sem er með tekjuáætlun. Tekjuáætlun línu er notuð til að ákvarða hvort fresta skuli tekjum línunnar.

## <a name="view-revenue-recognition-schedule-details"></a>Skoða upplýsingar um tekjuskráningaráætlun

Tvær leiðir eru til að nálgast upplýsingar um tekjuskráningaráætlunina.

- Hægt er að opna tekjuskráningaráætlunina beint úr reikningsfærðri sölupöntun. Í þessu tilviki eru upplýsingarnar í tekjuáætluninni síaðar til að sýna aðeins upplýsingar fyrir völdu sölupöntunina. Þessi nálgun er gagnleg þegar verið er að staðfesta upplýsingar um áætlun fyrir sölupöntun.
- Hægt er að opna tekjuskráningaráætlunina af síðunni **Tekjuskráning \> Reglubundin verkefni**. Þessi nálgun er oft notuð þegar tekjur eru skráðar við lok tímabils. Þegar síðan er fyrst opnuð birtast engar upplýsingar. Nota skal síurnar fyrir ofan hnitanetið til að skilgreina skilyrði fyrir upplýsingar um áætlun sem á að sýna. Hægt er að sía eftir reikningsdagsetningum með því að færa inn dagsetningabil, sölupöntun, viðskiptavin, verkkenni eða stöðu.

[![Síða tekjuáætlana](./media/revenue-recognition-rev-revenue-schedules.png)](./media/revenue-recognition-rev-revenue-schedules.png)

Flýtiflipinn **Fjárhagsvídd** fyrir neðan hnitanetið sýnir fjárhagsvíddir sölupöntunarlínunnar. Þessar víddir voru teknar til greina við bókun á frestuðum tekjum. Þær eru einnig teknar til greina þegar tekjurnar eru skráðar. Víddargildin sem eru notuð ráðast af lykilskipulagi sem er úthlutað á aðallykla fyrir tekjur og frestaðar tekjur.

## <a name="recognize-revenue"></a>Skrá tekjur

Hægt er að skrá tekjur með því að nota ferlið **Stofna færslubók** á síðunni **Skrá tekur**. Hægt er að opna þessa síðu úr sölupöntuninni eða **Reglubundin verkefni**. Ef ferlið er keyrt úr sölupöntuninni skráir það aðeins tekjur fyrir völdu sölupöntunina. Yfirleitt er ferlið keyrt í gegnum **Reglubundin verkefni** í staðinn, þannig að það skrái tekjur fyrir alla bókaða sölupöntunarreikninga.

Til að skilgreina skilyrði fyrir val og bókun tekna skal velja **Stofna færslubók** til að opna svargluggann **Stofna færslubók**.

[![Stofna valkosti færibreyta færslubókar](./media/revenue-recognition-create-journal.png)](./media/revenue-recognition-create-journal.png)

Í svarglugganum skal nota valkostina í reitahópnum **Dagsetning vinnslu** til að skilgreina bókunardagsetninguna sem er notuð þegar tekjur eru skráðar. Ef **Valin dagsetning** er valið er hægt að færa inn bókunardagsetningu í reitinn **Færsludagsetning**. Ef **Dagsetning tekjuáætlunar** er valið er færsludagsetningin ekki notuð. Þess í stað verður gildið í reitnum **Skráningardagsetning** fyrir hverja línu áætlunarinnar notað sem bókunardagsetning.

Næst skal færa inn „frá og með“ dagsetninguna fyrir skráðar tekjur í reitinn **Frá og með dagsetningu**. Allar línur áætlunarinnar þar sem skráningardagsetningin er á eða á undan „frá og með“ dagsetningunni verða skráðar, að því gefnu að þær séu ekki í bið.

Þegar búið er að skilgreina dagsetningarnar skal velja **Í lagi** í svarglugganum til að stofna færslubókina. Þú færð upplýsingaboð sem sýna fjölda færslna sem hafa verið stofnaðar og færslubókina þar sem þær voru stofnaðar. Færslubókin er ekki bókuð sjálfkrafa. Þess vegna hefur stjórnandi tekjuskráningar tíma til að staðfesta hvaða línur áætlunarinnar er verið að skrá.

Eftir að ferlið hefur verið keyrt eru línurnar í áætluninni sem voru fluttar í færslubókina merktar sem **Unnið**. Flaggið **Unnið** gefur til kynna að línurnar hafi verið færðar yfir í færslubókina, en hægt er að bóka eða afbóka þær. Flaggið **Unnið** er áfram til staðar eftir að tekjuskráningarbókin hefur verið bókuð. Ef tekjuskráningarfærslubókinni er eytt, eða ef línu er eytt, er flaggið **Unnið** fjarlægt. Þannig er hægt að skrá línuna þegar ferlið **Stofna færslubók** er keyrt aftur.

[![Síða tekjuskráningaráætlana](./media/revenue-recognition-rev-recog-schedule-02.png)](./media/revenue-recognition-rev-recog-schedule-02.png)

Á síðunni **Tekjuskráningarbók** (**Tekjuskráning \> Færslubókarfærslur \> Tekjuskráningarbók**) skal opna **Línur** til að skoða upplýsingar um hvað er verið að skrá. Aðskilin færsla er alltaf stofnuð fyrir hverja línu áætlunarinnar sem er verið að skrá, jafnvel þótt allar línur séu bókaðar á sömu dagsetningu með því að nota sömu fjárhagslykla.

[![Síða færslubókarfylgiskjals](./media/revenue-recognition-journal-voucher.png)](./media/revenue-recognition-journal-voucher.png)

Dálkurinn **Lykill** sýnir fjárhagslykil frestaðra tekna. Ekki er hægt að breyta þessum fjárhagslykli. Þessi takmörkun hjálpar til við að tryggja að réttur fjárhagslykill frestaðra tekna sé losaður. Þessi fjárhagslykill er ekki sannprófaður gagnvart lykilskipulaginu vegna þess að hann kann að hafa breyst frá því að síðasta bókun á fjárhagslykli frestaðra tekna átti sér stað.

Dálkurinn **Mótlykill** sýnir fjárhagslykil tekna. Sjálfgefið er að fjárhagslykill tekna sé tekinn úr birgðabókunarreglum og fjárhagsvíddir séu teknar úr sölupöntunarlínunni. Þessi fjárhagslykill er sannprófaður gagnvart núverandi lykilskipulagi. Hins vegar er hægt að breyta því ef lykilskipulagið hefur breyst og þarf á frekari fjárhagsvíddum að halda.

Sjálfgefna upphæðin kemur úr samsvarandi línu áætlunarinnar og ekki er hægt að breyta henni.

Ef margir gjaldmiðlar koma fyrir í sölupöntuninni er gengi reikningsins sjálfkrafa notað. Þetta tryggir að upphæðir bókhaldsgjaldmiðils og skýrslugjaldmiðils verði losaðar að fullu. Vegna sléttunar gæti gengi síðustu línu áætlunarinnar verið örlítið frábrugðið genginu á reikningnum.

Þegar búið er að bóka tekjuskráningarbókina er fylgiskjal fært inn í áætlunina. Ef fleiri en eitt fylgiskjal fylgir sömu línu áætlunarinnar birtist stjarna (\*) í línunni. Til að skoða fylgiskjöl sem voru bókuð fyrir þessa línu skal velja **Fylgiskjalafærslur**.

## <a name="modify-the-revenue-recognition-schedule-details"></a>Breyta upplýsingum um tekjuskráningaráætlun

Ekki er hægt að breyta flestum gögnum í upplýsingum um tekjuáætlun. Ekki er hægt að bæta nýjum línum við áætlunina og ekki er hægt að eyða fyrirliggjandi línum. Upplýsingum um tekjuáætlun fyrir hverja sölupöntunarlínu verður að vera viðhaldið til að hjálpa til við að tryggja að fyrirtækið skrái í framtíðinni sömu upphæð og var frestað.

### <a name="edit-schedule-lines"></a>Breyta áætlunarlínum

Sumar breytingar eru leyfðar í línum áætlunarinnar. Eftirfarandi reitum er hægt að breyta í línunum:

- **Í bið** – Hægt er að stilla eða hreinsa þetta flagg áður en unnið er úr línunni. Til að hreinsa flaggið skal velja línuna og því næst velja **Fjarlægja bið**. Ekki er hægt að skrá tekjur í línum sem eru í bið. Hægt er að setja línur sjálfkrafa í bið ef tekjuáætlunin er sett upp fyrir sjálfvirkar biðstöður.

    [![Tekjuáætlanir - breyta áætlunarlínum](./media/revenue-recognition-rev-revenue-schedules.png)](./media/revenue-recognition-rev-revenue-schedules.png)

- **Skráningardagsetning** – Hægt er að breyta skráningardagsetningu áður en unnið er úr línunni. Þegar ferlið sem stofnar færslubókina fyrir tekjuskráningu er keyrt er dagsetning færð inn í reitinn **Skrá tekjur frá og með dagsetningu**. Þessi dagsetning er borin saman við dagsetninguna í reitnum **Skráningardagsetning** til að ákvarða hvaða línur eigi að skrá.
- **Upphæð til losunar** – Hægt er að breyta upphæðinni sem verður losuð áður en unnið er úr línunni. Hægt er að lækka upphæð tekna sem er skráð, en það er ekki hægt að auka hana. Þessi reitur gerir fyrirtæki kleift að skrá hluta tekna á skráningardagsetningunni. Ef upphæðinni er breytt sýnir upphæðin í reitnum **Eftirstandandi upphæð** hversu miklar tekjur þarf samt að skrá.
- **Magn til losunar** – Ef tekjuáætlunin er sett upp fyrir eitt tilvik eða einn mánuð sýnir reiturinn **Magn til losunar** magnið fyrir sölupöntunarlínuna. Einnig er hægt að breyta þessum reit og nota aðra leið til að skrá hluta tekna. Til dæmis ef magnið í línunni er 5 er hægt að hnekkja magninu þannig að það verði minna en 5. Upphæðin í reitnum **Upphæð til losunar** er uppfærð í réttu hlutfalli.

### <a name="update-contract-terms"></a>Uppfæra samningsskilmála

Upplýsingar um tekjuáætlun eru búnar til samkvæmt tekjuáætlun sem er úthlutuð til sölupöntunarlínu þegar reikningur er bókaður. Ef tekjuáætlun á sölupöntunarlínu er röng er ekki hægt að breyta henni á sölupöntuninni eftir að sölupöntunin hefur verið reikningsfærð. Þess í stað verður að nota hnappinn **Uppfæra samningsskilmála** til að breyta tekjuáætluninni. Hægt er að breyta tekjuáætlun áður eða eftir að tekjur hafa verið skráðar.

Til að breyta áætluninni skaltu velja áætlunarlínu fyrir vöruna sem þú ert að breyta. Á eftirfarandi skýringarmynd er valin lína fyrir vöru S0008 sem var bókuð með 12 mánaða tekjuáætlun. Þegar valið er **Uppfæra samningsskilmála** sýnir svargluggi upphafs- og lokadagsetningar samningsins og tekjuáætlunina.

[![Upphafs- og lokadagsetningar samnings](./media/revenue-recognition-rev-revenue-schedule-update-cntrct-dates-schedule.png)](./media/revenue-recognition-rev-revenue-schedule-update-cntrct-dates-schedule.png)

Breyta skal upphafs- og lokadagsetningum samningsins þannig að þær endurspegli rétt dagsetningabil. Þegar dagsetningabili er breytt verður gildið í reitnum **Fjöldi tilvika** að samsvara tekjuáætlun sem skilgreind hefur verið í kerfinu. Í þessu dæmi, þar sem samningnum var breytt í 24 mánaða samning, verður að setja upp 24 mánaða tekjuáætlun. Þar sem 24 mánaða tekjuáætlun er til staðar er hún sjálfkrafa færð inn og hægt er að breyta samningnum. Ef ekki er til staðar tekjuáætlun með samsvarandi fjölda tilvika er ekki hægt að breyta samningnum. Eftir að samningsskilmálar og tekjuáætlun hafa verið uppfærð eftir þörfum skal velja **Í lagi** í svarglugganum til að vista breytingarnar.

[![Dagsetningabil uppfærðs samnings](./media/revenue-recognition-rev-revenue-schedule-update-cntrct-dates-schedule-02.png)](./media/revenue-recognition-rev-revenue-schedule-update-cntrct-dates-schedule-02.png)

Breytingar á samningnum hafa eftirfarandi áhrif á upplýsingar tekjuáætlunar:

- Ef engar tekjur hafa verið skráðar fyrir afurðina eru allar upplýsingar fyrri áætlunar fjarlægðar og þeim skipt út fyrir upplýsingar nýju tekjuáætlunarinnar. Til dæmis var vara S0008 upphaflega með 12 línur í upplýsingum áætlunar. Þessar 12 línur eru fjarlægðar og þeim skipt út fyrir 24 línur, samkvæmt nýju tekjuáætluninni.
- Ef tekjur hafa verið skráðar fyrir afurðina voru einhverjar tekjur ranglega skráðar vegna þess að skráningin var byggð á rangri tekjuáætlun. Bakfæra þarf þessar línur og skrá aftur út frá nýju áætluninni. Í þessu tilfelli eru nýjar tekjuáætlunarlínur stofnaðar sem eru með neikvæðar tölur á upphaflegri skráningardagsetningu. Nýjar línur eru svo stofnaðar til að skrá upphæðina sem byggjast á nýju tekjuáætluninni. Til dæmis þann 8. ágúst 2019 voru tekjur skráðar sem nemur $10,53. Þann 8. september 2019 voru tekjur skráðar sem nemur $13,16. Þar af leiðandi eru tvær nýjar línur stofnaðar á sömu dagsetningunum. Ein lína er fyrir -$10,53 og hin línan er fyrir -$13,16. Tuttugu og fjórar nýjar línur eru síðan stofnaðar og frestuðum heildartekjum að upphæð $160,61 er úthlutað á milli þeirra. Hægt er að bóka bakfærslulínur með því að keyra ferli **Stofna færslubók**.

[![Tekjuskráningaráætlun](./media/revenue-recognition-rev-recog-schedule-03.png)](./media/revenue-recognition-rev-recog-schedule-03.png)
