---
title: Nota færslubók öryggisbirgða til að uppfæra lágmarkstryggingu fyrir vörur
description: Þessi grein lýsir því hvernig á að nota öryggisbirgðabók til að uppfæra öryggisbirgðamagn fyrir vörur með því að reikna lágmarksþekjutillögur út frá sögulegum viðskiptum.
author: t-benebo
ms.date: 10/28/2021
ms.topic: article
ms.search.form: ReqItemJournalName, ReqItemJournalSafetyStock, EcoResProductInformationDialog, ReqItemTableSetup, ReqItemTable, EcoResProductDetailsExtended
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-10-28
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 385144738b83fcf6873eae5204b4784d6ecd5b80
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8851770"
---
# <a name="use-the-safety-stock-journal-to-update-minimum-coverage-for-items"></a>Nota færslubók öryggisbirgða til að uppfæra lágmarkstryggingu fyrir vörur

[!include [banner](../../includes/banner.md)]

Öryggisbirgðir gefa til kynna viðbótarmagn vöru sem er í birgðum til að draga úr hættu á að varan fari úr birgðum. Öryggisbirgðir eru notaðar sem biðminni ef sölupantanir berast, en birgir getur ekki uppfyllt umbeðinn sendingardag viðskiptavinarins.

Þessi grein lýsir því hvernig á að nota öryggisbirgðabókina til að reikna út lágmarksþekjutillögur byggðar á sögulegum viðskiptum og uppfæra síðan vöruþekjuna með tillögunum.

## <a name="overview-of-minimum-coverage-usage"></a>Yfirlit yfir lágmarksþekjunotkun

Öryggisbirgðir eru settar upp á **Vöruumfjöllun** síðu fyrir hvern hlut. Mismunandi gerðir áfyllingar eru táknaðar með mismunandi þekjukóðum. (Fyrir frekari upplýsingar, sjá [Uppfylling öryggisbirgða fyrir hluti](safety-stock-replenishment.md) .) Hins vegar nota allir þekjukóðar gildið sem er stillt í **Lágmark** sviði á **Vöruumfjöllun** síðu fyrir hvern hlut. Það eru tvær meginaðferðir til að nota **Lágmark** reit:

- **Lágmarksmagn í lágmarks/hámarks tilgangi** – Þessi nálgun notar lágmarksmagnið ásamt lágmark/max rökfræði. Það á við þegar **Umfjöllunarkóði** reiturinn er stilltur á *Min/Max* fyrir viðkomandi hlut eða umfjöllunarhóp. The **Lágmark** magn táknar meðaldaglega notkun margfaldað með afgreiðslutíma vörunnar.
- **Lágmarksmagn fyrir birgðaáætlun** – Þessi nálgun notar lágmarksmagn til að tákna birgðaáætlun ásamt eftirspurnarspám. Það á við þegar **Umfjöllunarkóði** reiturinn er stilltur á *Tímabil* eða *Krafa* fyrir viðkomandi hlut eða umfjöllunarhóp. The **Lágmark** magn táknar birgðaáætlun sem endurspeglar æskilegt þjónustustig til að hjálpa til við að draga úr birgðum, hlutasendingum og afhendingartíma. Lágmarksmagnið endurspeglar hlutfall af spánákvæmni fyrir tiltekið atriði. Það táknar ekki æskilega birgðastöðu.

The **Lágmark** gildi er hægt að stilla á þrjá vegu:

- Handvirkt á **Vöruumfjöllun** síðu
- Með gagnastjórnunarramma (*Vöruumfjöllun* gagnaeiningar)
- Með útreikningi öryggisbirgða sem er gerður af öryggisbirgðabókum

## <a name="calculate-minimum-coverage-based-on-historical-usage"></a>Reiknaðu lágmarksþekju byggt á sögulegri notkun

Öryggisbirgðabækur eru notaðar til að reikna út fyrirhugað lágmarksmagn byggt á sögulegri notkun vöru, annað hvort í lágmarks-/hámarkstilgangi eða í birgðaáætlunarskyni. Söguleg notkun táknar öll útgáfuviðskipti á tilteknu tímabili. Þessar útgáfufærslur innihalda sölupöntunarfærslur og birgðaleiðréttingar. Í útreikningunum er einnig greint frá áhrifum fyrirhugaðs lágmarksmagns á birgðaverðmæti og breytingu á birgðaverðmæti miðað við núverandi lágmarksmagn.

Hver öryggisbirgðabókarlína táknar vöru og þekjuvíddir hennar. Þessar dagbókarlínur eru búnar til og sýndar á **Öryggisbirgðabókarlínur** síða (**Aðalskipulag \> Aðalskipulag \> Hlaupa \> Útreikningur á öryggisbirgðum**). Viðskiptaferlinu til að nota öryggisbirgðabækur til að reikna út fyrirhugað lágmarksmagn er lýst síðar í þessari grein.

Skipuleggjandi notar öryggisbirgðabók til að reikna út fyrirhugað lágmarksmagn fyrir valdar vörur, byggt á sögulegri notkun á völdum tímabilum. Hægt er að hnekkja fyrirhuguðum lágmörkum handvirkt eftir þörfum og þú getur skoðað hugsanleg áhrif fyrirhugaðra lágmarka á birgðaverðmæti. Þegar færslubókin er bókuð er tengd lágmarksmagn í vöruþekju uppfært sjálfkrafa.

### <a name="create-a-new-safety-stock-journal-name"></a>Stofnið nýja heiti öryggisbirgðabókar.

Þú verður að búa til að minnsta kosti eitt heiti öryggisbirgðabókar áður en þú getur búið til þessa tegund færslubókar. Þú gætir venjulega notað nokkur dagbókarnöfn til að hjálpa til við að aðgreina útreikninga á öryggisbirgðum þínum.

1. Fara til **Aðalskipulag \> Uppsetning \> Nöfn öryggisbirgðabóka**.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Á nýju línunni skaltu stilla eftirfarandi reiti:

    - **Nafn** – Sláðu inn stutt heiti fyrir dagbókina.
    - **Lýsing** – Sláðu inn lýsingu á dagbókinni.
    - **Einkamál fyrir notendahóp** – Til að takmarka áhorfendur fyrir núverandi dagbókarheiti skaltu velja notendahóp.
    - **Eyða línum eftir færslu** – Veldu þennan gátreit til að hreinsa upp færslubókarlínur sjálfgefið þegar þú bókar þær. Hreinsaðu það til að halda öllum settum línum.

    The **Tegund dagbókar** reiturinn er skrifvarinn og er forstilltur á *Öryggisbirgðir*.

1. Lokið síðunni.

### <a name="create-a-safety-stock-journal-and-lines"></a>Búðu til öryggisbirgðabók og línur

Þetta skref býr til færslubók og bætir línum við hana sjálfkrafa. Hver lína auðkennir vöru, þekjuvíddir hennar og nokkur reiknuð magn úr notkunarsögunni. Reiknað magn inniheldur meðalútgáfur á afgreiðslutíma vöru, meðalútgáfur á mánuði og mánaðarlegt staðalfrávik.

#### <a name="automatically-generate-journal-lines"></a>Mynda sjálfkrafa færslubókarlínur

Færslubókarlínur er aðeins hægt að búa til sjálfkrafa ef engar línur eru til fyrir færslubókina sem er sýnd.

Fylgdu þessum skrefum til að mynda færslubókarlínur sjálfkrafa.

1. Fara til **Aðalskipulag \> Aðalskipulag \> Hlaupa \> Útreikningur á öryggisbirgðum**.
1. Í aðgerðarúðunni velurðu **Nýtt**. Ný öryggisbirgðabók er búin til.
1. Á **Upplýsingar um dagbókarhaus** Flýtiflipi, stilltu eftirfarandi reiti:

    - **Nafn** – Veldu heiti öryggisbirgðabókar til að bæta línunni við.
    - **Lýsing** – Sjálfgefið gildi er lýsingin á dagbókarheitinu sem þú valdir. Hins vegar geturðu breytt gildinu eftir þörfum.
    - **Eyða línum eftir færslu** – Veldu þennan gátreit til að hreinsa upp færslubókarlínur þegar þú bókar þær. Hreinsaðu það til að halda öllum settum línum. Stillingin er arfgeng frá völdum dagbókarheiti.

    The **Tímarit** reiturinn er skrifvarinn og sýnir kennitölu færslubókarinnar sem þú ert að búa til og bæta línum við.

1. Á **Dagbókarlínur** Flýtiflipi, veldu **Búðu til línur** á tækjastikunni.
1. Í **Stofna færslubókarlínur fyrir fyrirhugað lágmarksbirgðastig** valmynd, stilltu eftirfarandi reiti:

    - **Frá dags** – Veldu upphafsdag tímabilsins sem útgáfur eiga að vera með í útreikningi fyrir.
    - **Til dagsins í dag** – Veldu lokadagsetningu tímabilsins sem útgáfur eiga að vera með í þessum útreikningi fyrir. Það verða að líða að minnsta kosti tveir mánuðir á milli upphafs- og lokadaga.
    - **Reiknaðu staðalfrávik** – Stilltu þennan valkost á *Já* til að reikna út staðalfrávikið. Þú verður að stilla þennan valkost á *Já* að nota **Notaðu þjónustustig** valkostur þegar þú reiknar út tillöguna (eins og lýst er síðar í þessari grein).

1. Á **Skrár til að hafa með** Flýtiflipa, þú getur sett upp síur og takmarkanir til að skilgreina hvaða atriði eru innifalin. (Til dæmis geturðu síað eftir **Umfjöllunarhópur** gildi.) Veldu **Sía** til að opna staðlaðan fyrirspurnarritaraglugga, þar sem hægt er að skilgreina valviðmið, flokkunarviðmið og sameiningar. Reitirnir virka alveg eins og þeir gera fyrir aðrar tegundir fyrirspurna í Microsoft Dynamics 365 Supply Chain Management.
1. Á **Hlaupa í bakgrunni** Flýtiflipa, veldu hvort keyra eigi verkið í lotuham og/eða setja upp endurtekna áætlun. Reitirnir virka eins og þeir virka fyrir aðrar gerðir [bakgrunnsvinnsla](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) í Supply Chain Management.
1. Veldu **Í lagi**. Línur eru búnar til fyrir víddir sem hafa birgðafærslur.

#### <a name="manually-add-or-remove-journal-lines"></a>Bættu við eða fjarlægðu færslubókarlínur handvirkt

Þú getur handvirkt bætt við og/eða fjarlægt færslubókarlínur hvenær sem er (annaðhvort á eftir eða í stað þess að búa til línur sjálfkrafa). Notaðu eftirfarandi hnappa á tækjastikunni á **Dagbókarlínur** flýtiflipi:

- **Nýtt** – Bættu við nýrri línu. Sláðu síðan inn gildi í hvern dálk til að skilgreina vöruna sem á að reikna út og nota ný lágmark fyrir. Þar sem fyrirhugaðir lágmarksútreikningar eru ekki tiltækir fyrir handvirkt bættar línur, ekkert nýtt **Reiknað lágmarksmagn** gildi eru sýnd fyrir þau. Þess vegna verður þú að slá inn handvirkt **Nýtt lágmarksmagn** gildi. Hins vegar geturðu enn skoðað hugsanleg áhrif **Nýtt lágmarksmagn** verðmæti á birgðaverðmæti og hugsanlega breytingu á birgðum miðað við núgildandi lágmark.
- **Eyða** – Eyða völdu línunni.
- **Eyða færslubókarlínum** – Eyða öllum línum í dagbókinni.

### <a name="calculate-a-proposal"></a>Reiknaðu tillögu

Þetta skref reiknar út fyrirhugað lágmark fyrir hverja færslubókarlínu og hugsanleg áhrif línunnar á birgðaverðmæti. (Lágmarkið sem lagt er til er sýnt sem **Reiknað lágmarksmagn** gildi.) Þú getur gert útreikninginn mörgum sinnum, eins og þú vilt. Útreikningurinn uppfærir **Reiknað lágmarksmagn** gildi sem er sýnt fyrir allar færslubókarlínur.

Útreikningarnir sem sýndir eru munu ekki hafa áhrif á raunveruleg lágmarksmagn fyrir hverja vöru fyrr en þú velur **Post** á aðgerðasvæðinu. Á þeim tíma, sem **Nýtt lágmarksmagn** gildi verða notuð fyrir hverja vöru.

1. Fara til **Aðalskipulag \> Aðalskipulag \> Hlaupa \> Útreikningur á öryggisbirgðum**.
1. Opnaðu dagbókina til að reikna út tillögu fyrir. Einnig er hægt að búa til nýtt tímarit eins og lýst er fyrr í þessari grein.
1. Á **Dagbókarlínur** Flýtiflipi, veldu **Reiknaðu tillögu** á tækjastikunni. (Þú þarft ekki að velja neinar línur.)
1. Í **Reiknaðu tillögu að lágmarksbirgðastigi** valmynd, stilltu eftirfarandi reiti:

    - **Notaðu meðaltalsútgáfu á leiðslutíma** – Veldu þennan valkost til að búa til **Reiknað lágmarksmagn** gildi miðað við meðalútgáfu á tilgreindu tímabili. Þá, í **Margföldunarstuðull** reit, sláðu inn gildi til að stilla niðurstöðuna eftir þörfum. Til dæmis, slá inn *1.0* að nota nákvæmlega reiknað meðaltal eða *1.1* til að bæta við auka biðminni upp á 10 prósent.
    - **Notaðu þjónustustig** – Veldu þennan valkost til að reikna út fyrirhugað lágmark byggt á æskilegu þjónustustigi. Þá, í **Þjónustustig** reit, veldu valið þjónustustig.
    - **Framlegð framlegðartíma** – Sláðu inn gildi til að lengja venjulegan afgreiðslutíma um (til dæmis til að leyfa umsýslu).
    - **Notaðu reiknað lágmarksmagn sem nýtt lágmarksmagn** – Stilltu þennan valkost á *Já* til að afrita gildi sjálfkrafa úr **Reiknað lágmarksmagn** dálki til **Nýtt lágmarksmagn** dálki fyrir allar línur eftir að útreikningi er lokið. Ef þú stillir þennan valkost á *Nei*, hinn **Núverandi lágmarksmagn** gildi verður afritað í **Nýtt lágmarksmagn** dálk fyrir allar línur. Þú verður þá að breyta handvirkt **Nýtt lágmarksmagn** gildi eftir þörfum.

1. Á **Hlaupa í bakgrunni** Flýtiflipa, veldu hvort keyra eigi verkið í lotuham og/eða setja upp endurtekna áætlun. Reitirnir virka eins og þeir virka fyrir aðrar gerðir [bakgrunnsvinnsla](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) í Supply Chain Management.
1. Veldu **Í lagi**. Niðurstöður útreikningsins eru sýndar í **Reiknað lágmarksmagn** dálki á **Dagbókarlínur** Flýtiflipi. Í bili eru gildin aðeins fyrirhuguð gildi sem hafa ekki enn verið notuð á vörurnar þínar.

### <a name="update-minimum-quantity"></a>Uppfæra lágmarksmagn

Þú getur valið hvaða línu sem er í öryggisbirgðabók og hnekkt handvirkt gildi hennar **Nýtt lágmarksmagn** sviði.

1. Fara til **Aðalskipulag \> Aðalskipulag \> Hlaupa \> Útreikningur á öryggisbirgðum**.
1. Opnaðu dagbókina til að breyta. Einnig er hægt að búa til nýja dagbók eins og lýst er áðan.
1. Á **Dagbókarlínur** Flýtiflipi, finndu línuna til að stilla og breyttu síðan gildinu í **Nýtt lágmarksmagn** dálki. Til dæmis gætirðu stillt **Nýtt lágmarksmagn** gildi þannig að það passi við **Reiknað lágmarksmagn** gildi. Ef **Reiknað lágmarksmagn** gildi er *0* (núll), þú getur slegið inn æskilegt framtíðargildi.

### <a name="post-the-new-minimum-quantity-and-validate-the-result"></a>Bóka nýtt lágmarksmagn og villuleita niðurstöður

Fylgdu þessum skrefum til að bóka nýja lágmarksmagnið og staðfesta niðurstöðuna.

1. Fara til **Aðalskipulag \> Aðalskipulag \> Hlaupa \> Útreikningur á öryggisbirgðum**.
1. Opnaðu færslubókina til að bóka nýtt lágmarksmagn fyrir. Einnig er hægt að búa til nýja dagbók eins og lýst er áðan.
1. Á aðgerðasvæðinu skal velja **Bóka**.
1. Í **Post dagbók** valmynd, stilltu **Flytja allar bókunarvillur í nýja færslubók** reit eftir þörfum. Veldu síðan **Allt í lagi** að birta dagbókina.
1. Ef þú breyttir **Nýtt lágmarksmagn** gildi fyrir línu á **Dagbókarlínur** flýtiflipann, þú getur staðfest breytinguna með því að fylgja þessum skrefum:

    1. Fyrir línuna sem þú breyttir skaltu velja tengilinn í **Vörunúmer** dálki.
    1. Í **Upplýsingar um vöru** valmynd, veldu hlekkinn í **Vörunúmer** reitinn til að opna tengda útgefna vöruskrá.
    1. Á aðgerðasvæðinu, í flipanum **Áætlun**, í flokknum **Þekja**, skal velja **Vöruþekja**.
    1. Taktu eftir því að **Lágmark** gildi fyrir síðuna og vöruhúsið sem þú breyttir með því að nota bókaða öryggisbirgðabókina hefur nú verið uppfært til að passa við breytingarnar þínar.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Uppfylling öryggisbirgða fyrir vörur](safety-stock-replenishment.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
