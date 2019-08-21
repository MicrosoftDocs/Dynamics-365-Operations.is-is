---
title: Færibreytur útgjaldastýringar
description: Eftirfarandi færibreytur stjórna hegðun í Kostnaðarstýringu.
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: c1bc754b92e647f0fdac6799564273fb6ea6fb20
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841082"
---
# <a name="expense-management-parameters"></a>Færibreytur útgjaldastýringar

[!include [banner](../includes/banner.md)]

-----------------------------

Færibreyturnar stjórna almennri hegðun í Kostnaðarstýringu.

### <a name="general"></a>Almennt

| **Reitur**                                                | **Lýsing**                                                 |
|----------------------------------------------------------|---------------------------------------------------------------------|
| **Staðlaður kílómetrataxti**                             | Færðu inn endurgreiðslutaxta fyrir kílómetrakostnað. Taxtinn verður margfaldaður með innslegnum kílómetrafjölda á kostnaðinum til að reikna út endurgreiðsluupphæð vegna ferðakostnaðarins.                       |
|**Persónulegur kostnaður greiddur af**                             | Veldu þann sem ber ábyrgð á að borga allar kreditkortafærsluupphæðir sem eru flokkaðar sem persónulegar.                                                                                                     |
|**Birta alla kostnaðarskýrslu við bakköfun**               | Veldu þennan valkost til að sýna allan kostnað fyrir kostnaðarskýrslu þegar skoðaðar eru upplýsingar upphaflega skjalsins fyrir ákveðið fylgiskjal sem var búið til þegar kostnaðarskýrslan var birt.              |
|**Fyrirframleyfi þarf fyrir ferðinni**                 | Veldu þennan valkost til að krefjast þess að ferðabeiðni sé send inn og samþykkt áður en starfsmaður getur sent inn kostnaðarskýrslu.                                                                    |
|**Leyfa breytingu á dreifingum áður en bókun á sér stað**            | Veldu hvort hægt er að breyta dreifingum kostnaðarskýrslu áður en hún er birt.                                                                                                                 |
|**Meta reglur kostnaðarstýringar**                     | Veldu hvenær kostnaður er metinn til að ákvarða hvort kostnaðarregla hafi verið brotin. Hægt er að kanna brot á kostnaði þegar kostnaðarfærsla er færð inn og vistuð eða þegar kostnaðurinn er sendur inn til samþykkis. Stefnureglur fyrir mótteknar kvittanir verða kannaðar þegar kostnaðarlínan er vistuð.                   |
|**Leyfa kostnaðarlínur innan samstæðu**                         | Veldu hvort það megi færa inn kostnað fyrir aðra lögaðila í kostnaðarskýrslu.                                                                                                          |
|**Leyfa breytingar á gengi fyrir kreditkortaútgjöld** | Veldu þennan valkost til að leyfa notanda að breyta genginu fyrir innfluttan kreditkortakostnað.                                                                        |
|**Marglaga stigveldisreitir til að birta**                  | Veldu hvaða samþykkjandareiti á að sýna verkflæðisúthlutunargerð kostnaðarskýrslu á að vera stillt á stigveldi og stigveldisvalið er stillt á að nota marglaga samþykkisstigveldi fyrir kostnað. Þegar marglaga samþykkisstigveldi er notað fyrir verkflæði verða valdir reitir sýndir og hægt að breyta þeim í kostnaðarskýrslunni. |
|**Færa inn kreditkortanúmer starfsmanns (uppfærsla í júlí 2017)**     | Veldu hægt er að færa inn og vista 15 eða 16 stafa númer í reitnum **Kortakenni** á síðunni **Kreditkort** fyrir starfsmann.                                                                          |

### <a name="financial"></a>Fjármál

| **Reitur**                                                            | **Lýsing**     |
|----------------------------------------------------------------------|------------------------------------|
|**Nafn fjárhagsfærslubókar**                                         | Veldu heiti þeirrar fjárhagsbókar sem samþykktar útgjaldaskýrslur eru bókaðar í.            |
|**Gera skattendurgreiðslur virkar vegna kostnaðar**                                  | Veldu þennan valkost til að virkja skattaendurgreiðslur vegna kostnaðar fyrir kostnað sem uppfyllir skilyrði. Þennan valkost er ekki hægt að virkja ef reglur um bandarískan söluskatt og neysluskatt eru virkar.      |
|**Bóka fyrirframgreiðslur strax**                                     | Veldu þennan valkost til að bóka samþykkta fyrirframgreiðslu þegar ferlinu við að Greiða og flytja er lokið. Ef þessi valkostur er ekki valinn býr ferlið Greiða og flytja til óbókaða færslubók. |
|**Leiðrétta dagsetningu reikningsskila meðan á bókun stendur**                             | Veldu þennan valkost til að uppfæra dagsetningu reikningsskila þegar kostnaður er bókaður ef núverandi tímabil er í bið eða lokað. Dagsetning reikningsskila verður stillt á næsta opna tímabil.   |
|**Leyfa flokkun færslna sem eru byggðar á mótlykli sem tilgreindur er í greiðslumáta.**      | Veljdu þennan valkost til að taka saman kostnaðarfærslur fyrir kostnaðarskýrslu, byggt á þeim mótlykli sem tilgreindur er í greiðslumáta fyrir kostnaðinn.   
|**Skattur innifalinn**                                                   | Veldu þennan valkost til að hafa virðisaukaskatt sjálfkrafa innifalinn í upphæð kostnaðar.             |
|**Losa fjárúthlutun í ferðabeiðnum sem er lokað**            | Veldu þennan valkost til að losa uppfyllt fjármagns þegar samþykktri ferðabeiðni er lokað.                                                                                   |
|**Leyfa innsendingu ferðabeiðni á fjárhagsáætlun sem fór fram úr fyrir fjárhagsáætlunarskrá og fjárhagsáætlun verks** | Veldu þennan valkost til að leyfa starfsmönnum að senda inn ferðabeiðnir til samþykkis sem fara annaðhvort fram úr leyfðri fjárhagsáætlun sem er ákveðin í fjárhagsáætlunarskrá eða leyfðri fjárhagsáætlun fyrir verk.            |
|**Leyfa innsendingu kostnaðarskýrslu á fjárhagsáætlun sem fór fram úr fyrir fjárhagsáætlunarskrá og fjárhagsáætlun verks**    | Veldu þennan valkost til að leyfa starfsmönnum að senda inn kostnaðarskýrslur til samþykkis sem fara annaðhvort fram úr leyfðri fjárhagsáætlun sem er ákveðin í fjárhagsáætlunarskrá eða leyfðri fjárhagsáætlun fyrir verk.                |
|**Leyfa samþykki kostnaðarskýrslu á fjárhagsáætlun sem fór fram úr eingöngu fyrir fjárhagsáætlunarskrá**                | Veldu þennan valkost til að leyfa samþykkjendum að samþykkja kostnaðarskýrslur sem fara fram úr leyfðri fjárhagsáætlun sem sett er fram í fjárhagsáætlunarskrá.                                                                       |

### <a name="per-diem"></a>Dagpeningar

| **Svæði**                             | **Lýsing**             |
|---------------------------------------|--------------------------------------------------------------------------------------|
|**Lágmarks klukkustundir fyrir dagpeninga**           | Sláðu inn sjálfgefinn lágmarksfjölda klukkustunda sem starfsmaður verður að vinna á einum degi til að geta fengið greiðslur vegna ferðatengdra útgjalda.  Gildið er aðeins notað sem sjálfgefið gildi fyrir reitinn Lágmarksfjöldi klukkustunda á kostnað á dag.                                                                                      |
|**Fæðisprósenta**                          | Færðu inn sjálfgefna prósentu af dagpeningum fyrir máltíðir sem er notuð á fyrsta og síðasta degi ferðatengds kostnaðar þegar reiturinn **Reikna lækkun fæðispeninga með** er stilltur á annaðhvort **Gerð máltíða á dag** eða **Fjöldi máltíða á dag**. Vinnudagurinn á fyrsta og síðasta degi kann að vera styttri en staðlaður vinnudagur. Þess vegna kann upphæð dagpeninga á þessum dögum að vera önnur en staðlaða upphæðin. Ef prósentan er stillt á 0 er frádrátturinn á fyrsta og síðasta degi 0,00. |
|**Hótelprósenta**                        | Færðu inn sjálfgefna prósentu dagpeninga fyrir hótel sem notað eru á fyrsta og síðasta degi ferðatengds kostnaðar. Vinnudagurinn á fyrsta og síðasta degi kann að vera styttri en staðlaður vinnudagur. Þess vegna kann upphæð dagpeninga á þessum dögum að vera önnur en staðlaða upphæðin. Ef prósentan er stillt á 0 er frádrátturinn á fyrsta og síðasta degi 0,00.                                              |
|**Önnur prósenta**                        | Færðu inn sjálfgefna prósentu dagpeninga fyrir ýmsan kostnað sem notaður er á fyrsta og síðasta degi ferðatengds kostnaðar. Vinnudagurinn á fyrsta og síðasta degi kann að vera styttri en staðlaður vinnudagur. Þess vegna kann upphæð dagpeninga á þessum dögum að vera önnur en staðlaða upphæðin. Ef prósentan er stillt á 0 er frádrátturinn á fyrsta og síðasta degi 0,00.                                                                                                     |
|**Frádráttarprósenta fyrir morgunverð** | Færðu inn þá upphæð sem dagpeningar eru lækkaðir um vegna morgunverðar. Ef starfsmaður fær til dæmis frían morgunverð gætirðu viljað lækka dagpeningaupphæðina um 10 prósent.                               |
|**Frádráttur í prósentum fyrir hádegismat**    | Færðu inn þá upphæð sem dagpeningar eru lækkaðir um vegna hádegisverðar. Ef starfsmaður fær til dæmis frían hádegisverð gætirðu viljað lækka dagpeningaupphæðina um 15 prósent.                                       |
|**Frádráttur í prósentum fyrir kvöldmat**   | Færðu inn þá upphæð sem dagpeningar eru lækkaðir um vegna kvöldverðar. Ef starfsmaður fær til dæmis frían kvöldverð gætirðu viljað lækka dagpeningaupphæðina um 25 prósent.                                     |
|**Reikna lækkun fæðispeninga með**         | Veldu hvernig kerfið ætti að reikna út lækkun dagpeninga vegna fæðis með því að velja hvort lækkunin eigi að byggja á tegund máltíð í hverri ferð eða á hverjum degi, eða hvort lækkunin eigi að byggja á fjölda leyfðra máltíða á dag.|
|**Sléttun dagpeninga**                  | Veldu gerð sléttunar sem er notuð fyrir dagpeningakostnað. Ef þú velur venjulega sléttun er allur dagpeningakostnaður sem nær upphæðinni 0,50 sléttaður upp í 1,00 og dagpeningakostnaður sem nær ekki upphæðinni 0,50 er sléttaður niður í 0,00.                                                                                              |
|**Byggja útreikning á dagpeningum á**         | Veldu hvort upphæð dagpeninga byggir á almanaksdegi eða 24 klst. tímabili.       |

### <a name="fax-cover-pages"></a>Faxforsíður

| **Reitur**                      | **Lýsing**            |
|--------------------------------|-----------------------------------------------------------------------------|
| **Fyrirmæli**                   | Færðu inn leiðbeiningar sem starfsmenn þurfa að fylgja þegar þeir stofna forsíðu fyrir fax sem er notuð til að senda kvittanir sem tengjast kostnaðarskýrslu. Smelltu á hnappinn **Þýðingar** til að slá inn texta á ákveðnu tungumáli sem verður birtur byggt á tungumáli notandans. |
|**Notandakenni (Upplýsingar í strikamerki)** | Veldu þennan valkost til að geyma einkvæmt auðkenni starfsmanns í strikamerki sem er notað á forsíðu faxins.                 |
|**Strikamerki**                      | Veldu strikamerkið sem er notað á forsíðu faxins. Strikamerki 39 og 128 eru studd með Kostnaðarstýringu.               |

### <a name="anti-corruption"></a>Gegn spillingu

|                 <strong>Reitur</strong>                 |                                                                                                                                                                                            <strong>Lýsing</strong>                                                                                                                                                                                             |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  <strong>Birta staðfestingu gegn spillingu</strong>  | Veldu þennan valkost til að birta texta gegn spillingu þegar ný kostnaðarskýrsla er búin til. Þá er hægt að virkja tiltekna kostnaðarflokka sem krefjast þess að staðfesting gegn spillingu sé valin á kostnaðarskýrslunni. Til dæmis kann gjafaflokkur sem tengist kostnaði vegna opinbers starfsmann að krefjast þess að starfsmaður staðfesti að kostnaðurinn uppfylli reglur fyrirtækisins um opinbera starfsmenn. |
| <strong>Skilaboð gegn spillingu fyrir þann sem leggur fram</strong> |                                                                                             Færðu inn textann sem birtist starfsmanni þegar ný kostnaðarskýrsla er stofnuð. Smelltu á hnappinn <strong>Þýðingar</strong> til að slá inn texta á ákveðnu tungumáli sem verður birtur byggt á tungumáli notandans.                                                                                             |
| <strong>Skilaboð gegn spillingu fyrir samþykkjanda</strong>  |                                                                                             Færðu inn textann sem birtist samþykkjanda þegar ný kostnaðarskýrsla er stofnuð. Smelltu á hnappinn <strong>Þýðingar</strong> til að slá inn texta á ákveðnu tungumáli sem verður birtur byggt á tungumáli notandans.                                                                                             |

