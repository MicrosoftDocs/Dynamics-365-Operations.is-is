---
title: Nota færslubók öryggisbirgða til að uppfæra lágmarkstryggingu fyrir vörur
description: Þessi grein lýsir því hvernig á að nota færslubók öryggisbirgða til að uppfæra magn öryggisbirgða fyrir vörur með því að reikna út tillögur um lágmarksþekju byggðar á sögulegum færslum.
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
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8851770"
---
# <a name="use-the-safety-stock-journal-to-update-minimum-coverage-for-items"></a>Nota færslubók öryggisbirgða til að uppfæra lágmarkstryggingu fyrir vörur

[!include [banner](../../includes/banner.md)]

Öryggisbirgðir gefa til kynna viðbótarmagn af vöru sem er geymt í birgðum til að draga úr hættu á að varan verði uppseld. Öryggisbirgðir eru notaðar sem geymslubirgðir ef sölupantanir koma inn og birgir getur orðið við umbeðinni sendingardagsetningu viðskiptavinarins.

Þessi grein lýsir því hvernig á að nota færslubók öryggisbirgða til reikna lágmarks tillögur þekju byggðar á sögulegum færslum og uppfæra svo vöruþekju ásamt tillögum.

## <a name="overview-of-minimum-coverage-usage"></a>Yfirlit yfir lágmarksnotkun tryggingaverndar

Öryggisbirgðir er settur upp á síðunni **Vöruþekja** atriðis fyrir hverja vöru. Ólíkar gerðir áfyllingar eru táknaðar með mismunandi þekjukóðum. (Frekari upplýsingar eru í [Uppfylling öryggisbirgða fyrir vörur](safety-stock-replenishment.md)). Hins vegar nota allir þekjukóðar gildið sem er sett í reitinn **Lágmark** á síunni **Vöruþekja** fyrir hverja vöru. Tvær helstu aðferðir eru til við að nota reitinn **Lágmark**:

- **Lágmarksmagn í lágm./hám. tilgangi**. – Þessi aðferð notar lágmarksmagn ásamt rökum lágm./hám. Það á við þegar reiturinn **Þekjuflokkur** er stilltur á *Lágmark/Hámark* fyrir viðkomandi hlut eða þekjuflokk. **Lágmarksfjöldi** er meðaltal daglegrar notkunar margfaldað með afhendingartíma vörunnar.
- **Lágmarksmagn fyrir birgðaáætlun** – Þessi aðferð notar lágmarksmagnið til að sýna birgðaáætlun ásamt eftirspurnarspá. Það á við þegar reiturinn **Þekjukóði** er stilltur á *Tímabil* eða *Skilyrði* fyrir viðkomandi vöru eða þekjuflokk. **Lágmarksmagn** táknar birgðaáætlun sem endurspeglar það þjónustustig sem óskað er eftir til að draga úr því að vara seljist upp, hlutasendingum og afhendingartímum. Lágmarksmagn endurspeglar hlutfall af spánákvæmni fyrir tiltekna vöru. Hún sýnir ekki þá birgðastöðu sem óskað er eftir.

Hægt er að stilla **Lágmarksgildið** á þrjá vegu:

- Handvirkt á síðunni **Vöruþekja**.
- Eftir rammanum Stjórnun gagna (*Vöruþekja* gagnaeiningar)
- Með öryggisbirgðaútreikningi sem er gerður með færslubók öryggisbirgða

## <a name="calculate-minimum-coverage-based-on-historical-usage"></a>Reiknaðu lágmarksumfang miðað við sögulega notkun

Færslubók öryggisbirgða eru notaðar til að reikna út áætlað lágmarksmagn byggt á sögulegri notkun vöru, annaðhvort í lágm./hám. tilgangi eða í birgðaáætlun. Söguleg notkun táknar allar úthreyfingarfærslur á tilteknu tímabili. Þessar úthreyfingarfærslur fela í sér sölupöntunafærslur og leiðréttingar á birgðaskrá. Í útreikningunum er einnig gerð grein fyrir áhrifum fyrirhugaðs lágmarks magns á birgðavirði og breytingu á birgðavirði samanborið við núverandi lágmarksmagn.

Hver lína færslubók öryggisbirgða táknar vöru og þekjuvíddir hans. Þessar færslubókarlínur eru búnar til og sýndar á síðunni **Færslubókalínur öryggisbirgða** (**Aðaláætlanagerð \> Aðaláætlanagerð \> Keyra \> Útreikningur öryggisbirgða**). Viðskiptaferlinu við notkun færslubók öryggisbirgða til að reikna út áætlað lágmarksmagn er lýst síðar í þessari grein.

Skipuleggjandi notar færslubók öryggisbirgða til að reikna út áætlað lágmarksmagn fyrir valdar vörur, byggt á sögulegri notkun á völdum tímabilum. Hægt er að fara hnekkja handvirkt áætlað lágmarksmagn eftir þörfum og fara yfir hugsanleg áhrif áætlaðs lágmarksmagns á birgðavirði. Þegar færslubókin er bókuð er tengt lágmarksmagn í vöruþekju uppfært sjálfkrafa.

### <a name="create-a-new-safety-stock-journal-name"></a>Stofnið nýja heiti öryggisbirgðabókar.

Þú verður að búa til a.m.k. eitt heiti færslubók öryggisbirgða áður en þú getur búið til þessa tegund færslubókar. Þú gætir almennt notað nokkur heiti færslubókar til að aðskilja útreikninga þína á öryggisbirgðum.

1. Farðu í **Aðaláætlanagerð \> Uppsetning \> Heiti færslubókar öryggisbirgða**.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Stilltu eftirfarandi reiti á nýju línunni:

    - **Heiti** – Sláðu inn stutt heiti fyrir færslubók.
    - **Lýsing** – Færið inn lýsingu á færslubókinni.
    - **Aðeins fyrir notendaflokk** – Veljið notendaflokk til að takmarka aðgang að núverandi heiti færslubókar.
    - **Eyða línum eftir bókun** – Veljið þennan gátreit til að hreinsa sjálfkrafa færslubókarlínur eftir bókun. Hreinsa það til að halda öllum bókuðum línum.

    Reiturinn **Færslubókargerð** er skrifvarinn og er forstillt á *Öryggisbirgðir*.

1. Lokið síðunni.

### <a name="create-a-safety-stock-journal-and-lines"></a>Stofna öryggisbirgðabók og línur

Þetta skref býr til færslubók og bætir línum sjálfkrafa við hana. Hver lína auðkennir vöru, þekjuvíddir hennar og nokkrum reiknuðu magni úr notkunarferlinum. Reiknað magn felur í sér meðaltal úthreyfinga á hvern afhendingartíma vöru, meðaltal úthreyfinga á mánuði og staðalfrávik á mánuði.

#### <a name="automatically-generate-journal-lines"></a>Búa til færslubókarlínur sjálfkrafa

Færslubókarlínur er aðeins hægt að búa til sjálfkrafa ef engar línur eru til fyrir færslubókina sem er sýnd núna.

Fylgið eftirfarandi skrefum til að búa sjálfkrafa til dagbókarlínur.

1. Farið í **Aðaláætlanagerð \> Aðaláætlanagerð \> Keyra \> Útreikningur öryggisbirgða**.
1. Í aðgerðarúðunni velurðu **Nýtt**. Ný færslubók öryggisbirgða er stofnuð.
1. Í flýtiflipanum **Upplýsingar færslubókarhauss** skal stilla eftirfarandi reiti:

    - **Heiti** – Veldu heiti færslubókar öryggisbirgða til að bæta línunni við.
    - **Lýsing** – Sjálfgefið gildi er lýsing á heiti færslubókar sem þú valdir. Hins vegar er hægt að breyta gildinu eftir þörfum.
    - **Eyða línum eftir bókun** – Veljið þennan gátreit til að hreinsa færslubókarlínur eftir bókun. Hreinsa það til að halda öllum bókuðum línum. Stillingin erfist frá völdu heiti færslubókar.

    Reiturinn **Færslubók** er skrifvarinn og sýnir auðkennisnúmer færslubókarinnar sem þú ert að búa til og bæta línum við.

1. Á flýtiflipanum **Færslubókalínur** og flýtiflipanum **Búa til línur** á tækjastikunni.
1. Í svarglugganum **Stofna færslubókarlínur fyrir lágmarksbirgðastig sem lagt er til** skal stilla eftirfarandi reiti:

    - **Frá dagsetningu** – Veldu upphafsdag tímabilsins sem taka á úthreyfingar með í reikninginn fyrir.
    - **Til dagsetningar** – Veljið lokadag þess tímabils sem taka á með úthreyfingar með í reikninginn. A.m.k. tveir mánuðir verða að líða milli upphafs- og lokadags.
    - **Reiknið staðalfrávik** – Stillið þennan valkost á *Já* til að reikna staðalfrávik. Þú verður að stilla þennan valkost á *Já* til að nota valkostinn **Nota þjónustustig** þegar þú reiknar tilboð (eins og lýst er síðar í þessari grein).

1. Á flýtiflipanum **Færslur til að taka með** skaltu setja upp síur og takmarkanir til að skilgreina hvaða gögn á að taka með. (T.d er hægt að sía eftir gildi **Þekjuflokks**). Veldu **Sía** til að opna hefðbundinn svargluggi fyrirspurnar þar sem hægt er að skilgreina valskilyrði, röðunarskilyrði og tengingar. Reitirnir virka á sama hátt og fyrir aðrar gerðir fyrirspurna í Microsoft Dynamics 365 Supply Chain Management.
1. Í flýtiflipanum **Keyra í bakgrunni** skal velja hvort keyra skuli vinnsluna í runustillingu og/eða setja upp endurtekna áætlun. Reitirnir virka eins og þeir virka fyrir aðrar gerðir [bakgrunnsvinnsla](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) í Supply Chain Management.
1. Veldu **Í lagi**. Línur eru stofnaðar fyrir víddir sem hafa birgðafærslur.

#### <a name="manually-add-or-remove-journal-lines"></a>Bæta handvirkt við eða fjarlægja færslubókarlínur

Þú getur hvenær sem er bætt við og/eða fjarlægt færslubókarlínur handvirkt (annaðhvort eftir eða í stað þess að búa sjálfkrafa til línur). Notaðu eftirfarandi hnappa á tækjastiku flýtiflipans **Færslubókarlínur**:

- **Nýtt** – Bæta við nýrri línu. Síðan er slegið inn gildi í hvern dálk til að skilgreina vöruna sem á að reikna og sækja um ný lágmark. Þar sem tillögur um lágmarksútreikninga eru ekki tiltækar fyrir línur sem bætt er við handvirkt birtast engin ný gildi **Reiknað lágmarksmagn** fyrir þær. Því verður að færa inn gildi fyrir **Nýtt lágmarksmagn** handvirkt. Hins vegar er enn hægt að skoða hugsanleg áhrif **Nýtt lágmarksmagn** á birgðavirði og hugsanlega breytingu á birgðum samanborið við núverandi tilgreint lágmark.
- **Eyða** – Eyða völdu línunni.
- **Eyða færslubókarlínum** – Eyða öllum færslubókarlínum.

### <a name="calculate-a-proposal"></a>Reikna tillögu

Þetta skref reiknar áætlað lágmark fyrir hverja færslubókarlínu og hugsanleg áhrif línunnar á birgðavirði. (Tillaga að lágmarki er sýnd sem **Reiknað lágmarksmagn**). Þú getur gert útreikninginn margsinnis, eins og þú krefst. Útreikningur uppfærir gildi **Reiknað lágmarksmagns** sem er sýnt fyrir allar færslubókarlínur.

Útreikningarnir sem sýndir eru hafa ekki áhrif á raunveruleg gildi lágmarksmagns fyrir hverja vöru fyrr en þú velur **Bóka** í Aðgerðasvæði. Á þeim tíma verða sett ný gildi **Lágmarksmagns** fyrir hverja vöru.

1. Farið í **Aðaláætlanagerð \> Aðaláætlanagerð \> Keyra \> Útreikningur öryggisbirgða**.
1. Opna fjárhag til að reikna út tillögu að breytingum. Að öðrum kosti skaltu stofna nýja færslubók eins og lýst var fyrr í þessari grein.
1. Á flýtiflipanum **Færslubókarlínur** skal velja **Reikna tillögu** á tækjastikunni. (Þú þarft ekki að velja neinar línur).
1. Í svarglugganum **Reikna tillögu um lágmarksbirgðastig** skal stilla eftirfarandi reiti:

    - **Nota meðaltal úthreyfinga á afhendingartíma** – Velja þennan valkost til að búa til **Reiknað lágmarksmagn** miðað við meðaltal úthreyfinga á tilteknu tímabili. Síðan í reitnum **Margfeldisstuðull** er fært inn gildi til að breyta niðurstöðunni eftir þörfum. Til dæmis, sláðu inn *1,0* til að nota nákvæmt reiknað meðaltal eða *1,1* til að bæta við auka öryggisbirgðum sem nemur 10 prósentum.
    - **Nota þjónustustig** – Veljið þennan valkost til að reikna tillögu um lágmark byggt á viðkomandi þjónustustigi. Síðan í reitnum **Þjónustustig** velurðu þjónustustig sem óskað er eftir.
    - **Viðbót afhendingartíma** Sláðu inn gildi til að lengja venjulegan afhendingartíma (til dæmis til að gera ráð fyrir stjórnun).
    - **Nota reiknað lágmarksmagn sem nýtt lágmarksmagn** – Stillið þennan valkost á *Já* til að afrita gildi sjálfkrafa úr dálknum **Reiknað lágmarksmagn í** dálkinn **Nýtt lágmarksmagn** fyrir allar línur að útreikningi loknum. Ef þessi valkostur er stilltur á *Nei* verður **Núverandi lágmarksmagn** afritað í dálkinn **Nýtt lágmarksmagn** fyrir allar línur. Þú munt þá þurfa að breyta handvirkt **Lágmarksmagni** eftir þörfum.

1. Í flýtiflipanum **Keyra í bakgrunni** skal velja hvort keyra skuli vinnsluna í runustillingu og/eða setja upp endurtekna áætlun. Reitirnir virka eins og þeir virka fyrir aðrar gerðir [bakgrunnsvinnsla](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) í Supply Chain Management.
1. Veldu **Í lagi**. Niðurstöður útreikningsins eru sýndar í dálknum **Reiknað lágmarksmagn** á flýtiflipanum **Færslubókarlínur**. Sem stendur eru gildin aðeins áætluð gildi sem hafa ekki enn verið notuð fyrir vörurnar þínar.

### <a name="update-minimum-quantity"></a>Uppfæra lágmarksmagn

Hægt er að velja hvaða línu sem er í færslubók öryggisbirgða og hunsa handvirkt gildi reitsins **Nýtt lágmarksmagn**.

1. Farið í **Aðaláætlanagerð \> Aðaláætlanagerð \> Keyra \> Útreikningur öryggisbirgða**.
1. Opna færslubókina til að gera breytingar. Að öðrum kosti er hægt að stofna nýja færslubók, eins og lýst var hér á undan.
1. Á flýtiflipa **Færslubókarlínur** finnur þú línuna til að breyta og breytir síðan gildinu í dálknum **Nýtt lágmarksmagn**. Til dæmis væri hægt að stilla gildið **Nýtt lágmarksmagn** þannig að það passi við gildið **Reiknað lágmarksmagn**. Ef gildi **Reiknað lágmarksmagn** er *0* (núll) er hægt að færa inn framvirk gildi sem óskað er eftir.

### <a name="post-the-new-minimum-quantity-and-validate-the-result"></a>Bóka nýtt lágmarksmagn og villuleita niðurstöður

Fylgdu eftirfarandi skrefum til að bóka nýtt lágmarksmagn og villuleita niðurstöður.

1. Farið í **Aðaláætlanagerð \> Aðaláætlanagerð \> Keyra \> Útreikningur öryggisbirgða**.
1. Opnaðu færslubókina til að setja inn nýtt lágmarksmagn fyrir hana. Að öðrum kosti er hægt að stofna nýja færslubók, eins og lýst var hér á undan.
1. Á aðgerðasvæðinu skal velja **Bóka**.
1. Í svarglugganum **Bóka færslubók** skaltu stilla reitinn **Millifæra allar bókunarvillur í nýja færslubók** eftir þörfum. Veldu svo **Í lagi** til að bóka færslubókina.
1. Ef þú breyttir gildi fyrir **Nýtt lágmarksmagn** fyrir línu í flýtiflipi **Færslubókarlínu** getur þú staðfest breytinguna með því að fylgja þessum skrefum:

    1. Fyrir línuna sem þú breyttir skaltu velja tengilinn í dálkinum **Vörunúmer**.
    1. Í svarglugganum **Vöruupplýsingar** skaltu velja tengilinn í reitnum **Vörunúmer** til að opna tengda færslu losaðrar vöru.
    1. Á aðgerðasvæðinu, í flipanum **Áætlun**, í flokknum **Þekja**, skal velja **Vöruþekja**.
    1. Athugaðu að gildið **Lágmark** fyrir svæðið og vöruhúsið sem þú aðlagaðir með því að nota bókuðu færslubók öryggisbirgða hefur nú verið uppfært til samræmis við breytinguna þína.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Uppfylling öryggisbirgða fyrir vörur](safety-stock-replenishment.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
