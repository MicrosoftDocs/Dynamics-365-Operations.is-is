---
title: Bylgjusniðmát
description: Í þessu efnisatriði er lýst hvernig eigi að setja upp skilyrði sem ákvarða hvort bylgjur eru unnar handvirkt eða sjálfvirkt og vinnu sem er mynduð fyrir vöruhús þegar unnið er úr bylgju.
author: Mirzaab
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 61fbcad572bbb69ab8a4eb2cd309cdf8a6328391
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686598"
---
# <a name="wave-templates"></a>Bylgjusniðmát

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er lýst hvernig eigi að setja upp skilyrði sem ákvarða hvort bylgjur eru unnar handvirkt eða sjálfvirkt og vinnu sem er mynduð fyrir vöruhús þegar unnið er úr bylgju. Tilgreina skal skilyrði með því að setja upp bylgjusniðmát og fyrirspurnir sem samsvara bylgju með losaðar línur í sölupantanir, framleiðslupantanir og kanbana.

## <a name="settings-for-wave-templates"></a>Stillingar fyrir sniðmát bylgju

Þegar sett er upp bylgjusniðmát er eftirfarandi tilgreint:

- **Svæði** og **Vöruhús** sem sniðmátið mun stofna vinnu fyrir.
- Röðin sem sniðmátin verða metin í. Röðina sem sniðmát eru samsvöruð við losuð lína á sölupantanir, framleiðslupantanir og kanbana. Þegar lína er losuð notar kerfið fyrsta bylgjusniðmátið sem línan uppfyllir skilyrðin fyrir. Því almennara sem skilyrðið er þeim mun líklegra er að lína uppfylli skilyrðið og því ætti að setja sniðmátin með sértækasta skilyrðinu efst á listann. Notið hnappana **Færa upp** og **Færa niður** á aðgerðasvæðinu til að raða sniðmátum í listanum.
- Aðgerðirnar sem hvert sniðmát grípur til. Bylgjan **Aðferðir** framkvæmir aðgerðir sem stofnaðar eru með sniðmátinu, eins og að mynda eða dreifa vinnu fyrir hverja gerð bylgjusniðmáts.
- Bylgjueigindir (síurnar) sem þarf að nota til að sé hægt að nota bylgjusniðmátið.

> [!NOTE]
> Ef þörf krefur getur þróunaraðili stofnað fleiri aðferðir. Hægt er að skoða allan listann yfir aðferðir á síðunni **Aðferðir bylgjuvinnslu**.

Sumar stillingar eiga við um stefnumarkandi ákvarðanir fyrir bylgjuvinnslu, eins og hér segir:

- Ef sniðmátið er notað til að senda vörur fyrir sölupantanir og flutningspantanir, eða notað til að flytja vörur í framleiðslu fyrir framleiðslupantanir eða kanban.
- Ef unnið er úr bylgju handvirkt eða sjálfkrafa, eins og eftirfarandi:

  - **Handvirk vinnsla** – Línunni er bætt við bylgju og birgðir eru fráteknar en hins vegar þarf að velja **Vinna úr** á listasíðunni **Allar bylgjur** til að stofna tiltektina fyrir pöntunina.
  - **Sjálfvirk vinnsla** - Þú getur gert ölduvinnslu sjálfvirka að fullu eða að hluta. Ef bylgjuvinnsla er gerð alsjálfvirk er bylgja stofnuð sem inniheldur línuna úr sölupöntun, framleiðslupöntun eða kanban þegar sölupöntun, framleiðslupöntun eða kanban er stofnað. Vörurnar eru dregnar frá lagerbirgðum og tiltektarvinnan er stofnuð. Ef að bylgjuvinnslu er gerð sjálfvirk að hluta geturðu tilgreint gildin sem kveikir á bylgjuvinnslu. Til dæmis er hægt að tilgreina hámarksþyngd fyrir sendingar sem setja af stað bylgjuvinnslu þegar heildarþyngd línanna í bylgjunni ná gildinu.

- Ef sendingum er úthlutað á opna bylgju. Til dæmis, ef þú lofar viðskiptavini að pöntun sem gerð er fyrir 12:00 e.h. verði send innan 24 klukkustunda er hægt að setja upp bylgjusniðmátið sjálfkrafa til að úthluta pöntunarlínum á opin bylgju fyrir 12:00 e.h. Á þessum tíma er unnið sjálfkrafa úr bylgjunni.

Þegar unnið er úr bylgju er byggist tiltektin sem er stofnuð á vinnusniðmátinu og staðsetningarleiðbeiningunni sem er tilgreind fyrir vöruhúsið. Vinnusniðmátið tilgreinir hvernig vinna tiltektarlista er stofnuð og staðsetningarleiðbeininga tilgreinir staðsetningar tiltektar og frágangs.

## <a name="create-a-wave-template"></a>Stofna bylgjusniðmát

Til að setja upp bylgjusniðmát skal fylgja þessum skrefum:

1. Fara í **Vöruhúsakerfi** \> **Upspetning** \> **Bylgjur** \> **Bylgjusniðmát**.
1. Veljið **Nýtt** til að stofna nýtt bylgjusniðmát.
1. Í reitnum **Bylgjusniðmátsgerð** skal velja einn af eftirfarandi valkostum:

    - *Afhending* - Nota bylgjusniðmátið fyrir sendingu á vörum fyrir sölupantanir og flutningspantanir.
    - *Framleiðslupantanir* - Bylgjusniðmátið er notað til að flytja vörur fyrir framleiðslupantanir.
    - *Kanban* - Bylgjusniðmátið er notað til að flytja vörur fyrir kanban-pantanir.

1. Í reitina **Heiti bylgjusniðmáts** og **Lýsing á bylgjusniðmáti** skal færa inn heiti og lýsingu fyrir bylgjusniðmátið.

    > [!NOTE]
    > Ef fleiri en eitt sniðmát er stofnað fyrir vöruhús gefur talan í svæðinu **Röð bylgjusniðmáts** til kynna staðsetningu sniðmátis í röðina sem sniðmát eru notuð þegar sniðmátsins skilyrðum er uppfyllt. Hægt er að velja **Færa upp** eða **Færa niður** til að endurraða sniðmátunum.

1. Í reitnunum **Svæði** og **Vöruhús** skal velja svæðið og vöruhúsið þar sem bylgjusniðmátið mun stofna bylgjur og tiltektarvinnu fyrir.
1. Ef ætlunin er að gera bylgjuvinnsluna sjálfvirka skal gera eftirfarandi stillingar eftir þörfum:

    - **Gera stofnun bylgju sjálfvirka** – Stilltið þetta á *Já* til að stofna bylgjur sjálfkrafa þegar sölupöntun, framleiðslupöntun eða kanban er losað í vöruhúsið.
    - **Úthluta á opnar bylgjur** – Stilltið þetta á *Já* til að úthluta línum sjálfkrafa á opna bylgju þegar línur eru losaðar. Línur eru úthlutað til bylgjur á grundvelli fyrirspurnarsía fyrir bylgjusniðmát.
    - **Vinna úr bylgju við losun í vörugeymslu** – Stillið þetta á *Já* til að vinna úr bylgjunni sjálfkrafa og stofna vinnu þegar lína er losuð í vöruhús.
    - **Vinna sjálfvirkt úr bylgjunni við þröskuld** – Stillið þetta á *Já* til að vinna sjálfkrafa úr bylgjunni þegar gildi hennar ná mörkum fyrir þyngd, sendingu og línur sem tilgreint er í reitahópnum **Bylgjuþröskuldar**. Þessi stilling er aðeins virk ef *Sending* er valið í reitnum **Bylgjusniðmátsgerð**.
    - **Gera losun bylgju sjálfvirka** – Stillið þetta á *Já* til að losa bylgjuna sjálfkrafa. Vinna tiltektarlista er stofnuð og í fartæki.
    - **Gera áfyllingarvinnu sjálfvirka** – Stillið þetta á *Já* til að stofna áfyllingarvinnu sem byggir á eftirspurn og losa hana sjálfkrafa. Bæta verður bylgjuaðferð áfyllingar við bylgjusniðmátið og stofna áfyllingarsniðmát með gerðinni *Bylgjueftirspurn*. Setjið upp áfyllingarsniðmát á síðunni **Áfyllingarsniðmát**. Þetta krefst þess að bæta við fylla aðferðina bylgjusniðmátið.
    - **Halda áfram bylgjuúrvinnslu þegar stofnun vinnu mistekst** – Þegar stillt á *Já* notar kerfið auða staðsetningu ef það getur ekki tekið frá birgðir á staðsetningunni sem staðsetningarleiðbeiningin stingur upp á (til dæmis vegna þess birgðirnar eru ekki lengur tiltækar). Þegar stillt á *Nei* mun bylgjan mistakast ef kerfið getur ekki tekið frá birgðirnar.

1. Stillið reitahópinn **Bylgjuþröskuldur** eftir þörfum:
    - **Þyngdarþröskuldur bylgju** – Sláið inn hámarksþyngd sem bylgja má innihalda.
    - **Sendingarþröskuldur** – Sláið inn hámarksfjölda sendinga sem má hafa í bylgju.
    - **Línuþröskuldur** – Sláið inn hámarksfjölda lína sem má hafa í bylgju.

1. Í reitahópnum **Sjálfgefin gildi** skal velja bylgjueigindir sem á að nota sem viðbótarskilyrði fyrir bylgjusniðmátið. Bylgjueigindir eru gagnlegar til að úthluta viðbótarskilyrðum, t.d. ákveðnum heitum viðskiptavina, í bylgjusniðmát. Þessar eigindir eru stofnaðar á síðunni **Eigindir bylgju**. 

1. Stillið **Regla um tilkynningu bylgju** á regluna sem ætlunin er að nota til að búa til tilkynningar sem tengjast bylgjum sem nota þetta sniðmát. Fyrir dæmi um reglu bylgjutilkynningar skal sjá [Tilkynningar bylgjukeyrslu](wave-execution-notifications.md).

1. Í flýtiflipanum **Aðferðir** sýnir listasvæðið **Valdar aðferðir** aðferðirnar fyrir valið bylgjusniðmát. Bylgjuaðferðirnar framkvæma aðgerðirnar sem eru stofnaðar af sniðmátinu, t.d. stofnun eða dreifingu vinnu. Þessar aðgerðir eru einnig nefndar bylgjuskref. Bylgjuaðferðir eru fyrirframskilgreindar fyrir hverja gerð af bylgjusniðmáti. Ekki er hægt að fjarlægja fyrirfram bylgjuaðferðir, hins vegar hægt að endurraða röðun aðferða og bæta við fleiri aðferðum. Til dæmis, ef verið er að stofna bylgjusniðmát fyrir sendingu er hægt að bæta við aðferðir fyrir áfyllingar og gámun. Hægt er að bæta gámun bylgju við röð bylgjuaðferða til að skilgreina gámun á línum sem unnið er úr í bylgjusniðmáti. Til að bæta við auka aðferð, skal gera eftirfarandi:

    - Veljið aðferð á svæðinu **Aðferðir sem eftir standa** og því næst skal velja **vinstri** örina til að bæta henni við svæðið **Valdar aðferðir**.
    - Til að breyta röðinni skal velja aðferð og síðan velja örina **Upp** eða **Niður**.

    > [!NOTE]
    > Þegar þú bætir við aðferð, er hún sjálfkrafa skráð í viðeigandi stað í röð af skrefum.

1. Til að setja upp fyrirspurnina sem mun samsvara losaðar línur við viðeigandi bylgju skal velja **Breyta fyrirspurn** á aðgerðasvæðinu.
1. Til að staðfesta að stillingar bylgjusniðmáts séu gildar, skal smella á **Staðfesta sniðmát**.
