---
title: Meðhöndla, yfirfara og bóka eftirágreiddan afslátt
description: Þessi grein lýsir því hvernig á að vinna úr tilboðum eftirágreidds afsláttar, reikna út afslættina, fara yfir færslurnar sem eru búnar til, bóka færslur og fara yfir bókanirnar.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateDeal
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: e63f02e5e93ec2ce8c321a20c2a0c5886edcbe42
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901938"
---
# <a name="process-review-and-post-rebates"></a>Meðhöndla, yfirfara og bóka eftirágreiddan afslátt

[!include [banner](../includes/banner.md)]

Þessi grein lýsir því hvernig á að vinna úr tilboðum eftirágreidds afsláttar, reikna út afslættina, fara yfir færslurnar sem eru búnar til, bóka færslur og fara yfir bókanirnar.

## <a name="change-the-status-of-a-deal"></a>Breyta stöðu tilboðs

Hægt er að úthluta hverju tilboði stöðu til að auðvelda rakningu þess. Stöðunni er aðeins ætlað að veita upplýsingar.

1. Veldu tilboð (til dæmis á [**Öll tilboð fyrir stjórnun eftirágreidds afsláttar** síðunni](rebate-management-deals.md)).
1. Á aðgerðasvæðinu, í flipanum **Tilboð fyrir stjórnun eftirágreidds afsláttar**, í flokknum **Vinna með**, skal velja **Breyta stöðu**.
1. Í svarglugganum **Breyta stöðu** skal stilla reitinn **Staða eftirágreidds afsláttar** á nýja stöðu.
1. Veljið **Í lagi**.

## <a name="calculate-fifo-purchase-prices"></a>Reikna út innkaupaverð samkvæmt FIFO

Keyra þarf reglubundna verkið **Reikna út innkaupaverð samkvæmt FIFO** til að reikna eftirágreiddan afslátt fyrir [tilboð](rebate-management-deals.md) þar sem reiturinn **Verðgrunnur** er stilltur á *FIFO*. Kerfið notar fyrst inn, fyrst út (FIFO) regluna til að reikna út virði birgðanna sem voru seldar. Þetta virði verður síðan notað til að reikna út eftirágreiddan afslátt lánardrottins.

Farið í **Stjórnun eftirágreidds afsláttar \> Reglubundin verk \> Reikna út innkaupaverð samkvæmt FIFO**. Í svarglugganum sem birtist skal velja **Í lagi** til að keyra útreikninginn.

## <a name="create-source-transactions"></a>Stofna upprunafærslur

Þú getur stofnað sölupantanir eða innkaupapantanir sem eru með upprunalegar færslur annaðhvort fyrir eða eftir að þú býrð til viðeigandi tilboð fyrir stjórnun á eftirágreiddum afslætti.

Hægt er að setja upp hverja tilboðslínu þannig að hún búi sjálfkrafa til úthlutun eftirágreidds afsláttar með því að bóka afhendinguna eða reikninginn fyrir sölupöntun eða innkaupapöntun. Stilltu reitinn **Færslugerð** fyrir tilboðslínuna á *Afhendingu* eða *Reikning* og stilltu valkostinn **Afgreiða við bókun** á *Já*. Ef reiturinn **Færslugerð** er stilltur á *Pöntun* er slökkt á afgreiðslu við bókun. Fyrir upprunafærslur sem voru stofnaðar eftir að tilboð var virkjað geturðu enn afgreitt úthlutunina eins og lýst er í hlutanum [Vinna úr tilboðum fyrir stjórnun eftirágreidds afsláttar](#process-deals) síðar í þessari grein.

### <a name="enable-price-details"></a>Virkja verðupplýsingar

Áður en hægt er að stofna upprunalegar færslur verður að virkja valkostinn **Virkja upplýsingar um verð** fyrir viðskiptakröfur.

1. Opnið **Viðskiptakröfur \> Setja upp \> Færibreytur viðskiptakrafna**.
1. Í flipanum **Verð**, í flýtiflipanum **Verðupplýsingar**, skal stilla valkostinn **Virkja verðupplýsingar** á *Já*.

### <a name="create-a-source-transaction"></a>Stofna upprunalega færslu

Til að stofna upprunafærslu, skal fylgja eftirfarandi skrefum.

1. Farðu í **Sölu og markaðssetningu \> Sölupöntun \> Allar sölupantanir**.
1. Veljið **Nýtt**.

    Til að líkja eftir því hvernig kröfur um eftirágreiddan afslátt eru búnar til þarftu nú að stofna sölupöntun þar sem afurðin og magnið veita viðskiptavini rétt á eftirágreiddum afslætti.

1. Í reitinn **Viðskiptavinalykill** skal færa inn eða velja viðskiptavin sem mun eiga rétt á eftirágreiddum afslætti.
1. Veldu **Í lagi** til að stofna sölupöntun.
1. Í flýtiflipanum **Sölupöntunarlínur** skal bæta við línu og stilla eftirfarandi gildi:

    - **Vörunúmer** – Tilgreindu vöru sem fellur undir eftirágreiddan afslátt.
    - **Magn** – Tilgreindu magn sem uppfyllir skilyrði tilboðs eftirágreidds afsláttar sem inniheldur línu þar sem reiturinn **Grundvöllur** er stilltur á *Magn*.
    - **Einingarverð** – Tilgreindu verð sem uppfyllir skilyrði tilboðs eftirágreidds afsláttar sem inniheldur línu þar sem reiturinn **Grundvöllur** er stilltur á *Virði*.
    - **Svæði** – Veldu svæði þar sem afurðin er tiltæk og sem uppfyllir skilyrði tilboðs um eftirágreiddan afslátt.
    - **Vöruhús** – Veldu vöruhús þar sem afurðin er tiltæk og sem uppfyllir skilyrði tilboðs um eftirágreiddan afslátt.

1. Í flýtiflipanum **Sölupöntunarlínur**, á tækjastikunni, skal velja **Sölupöntunarlínur \> Verðupplýsingar**. Þessi skipun er aðeins tiltæk ef þú virkjaðir verðupplýsingar eins og lýst var í fyrri hlutanum.
1. Á síðunni **Verðupplýsingar** skal velja flýtiflipann **Stjórnunar eftirágreidds afsláttar**. Þessi flýtiflipi sýnir öll tilboð fyrir stjórnun eftirágreidds afsláttar sem eiga við um núverandi pöntunarlínu og sýnir áætlaða upphæð eftirágreidds afsláttar í gjaldmiðli pöntunarinnar. Athugið að upphæðirnar eru aðeins mat á kröfum um afslátt í framtíðinni. Upphæðir afsláttar gætu verið aðrar. Hér eru nokkrir þættir sem gætu haft áhrif á raunverulegar fjárhæðir:

    - Heildarsölumagn sem viðskiptavinur hefur náð samkvæmt samningi um reglulegan afslátt.
    - Hvort viðskiptavinur hafi skilað öllu magni eða hluta.
    - Hvort viðeigandi sölupöntun fékk færslugerðina (*Pöntun, afhending* eða *Reikningur*) sem er skilgreind fyrir tilboðið fyrir stjórnun eftirágreidds afsláttar.
    - **Úttaksvirði** samnings. Auð upphæð eftirágreidds afsláttar verður sýnd fyrir tilboð þar sem reiturinn **Úttak** er stilltur á *Vara*.

1. Í flýtiflipanum **Upplýsingar** skaltu taka eftir að hlutinn **Áætluð framlegð** inniheldur eftirfarandi reiti. Stjórnun eftirágreidds afsláttar bætir við þessum reitum. Þeir sýna allir virði á einingu (þar sem reitirnir í flýtiflipanum **Stjórnun eftirágreidds afsláttar** sýnir heildarvirðið fyrir línuna).

    - **Upphæð fyrir stjórnun eftirágreidds afsláttar** (eingöngu sölupantanir)
    - **Afnotagreiðsla fyrir stjórnun eftirágreidds afsláttar** (eingöngu sölupantanir)
    - **Upphæð fyrir stjórnun eftirágreidds afsláttar lánardrottins** (sölupantanir og innkaupapantanir)

1. Lokaðu síðunni **Verðupplýsingar**.
1. Ef sölupöntunin uppfyllir ekki skilyrði eftirágreidds afsláttar sem þú varst að skoða skaltu fylgja þessum skrefum til að útiloka eftirágreidda afslætti. (Þú útilokar þó yfirleitt ekki afslátt.)

    1. Á flýtiflipanum **Sölupöntunarlínur** skal velja viðkomandi línu.
    1. Í flýtiflipanum **Upplýsingar um línu**, í flipanum **Verð og afsláttur**, skal stilla valkostinn **Útiloka frá eftirágreiddum afslætti** á *Já*. Þessi valkostur á ekki við um innkaupapantanir. Enn fremur eru aðeins eftirágreiddir afslættir viðskiptavinar útilokaðir þegar þessi valkostur er stilltur á *Já*. Afnotagreiðsla viðskiptavinar vegna eftirágreidds afsláttar og eftirágreiddir afslættir lánardrottins eiga enn við.

1. Á aðgerðasvæðinu, í flipanum **Taka til og pakka**, í flokknum **Búa til** skal velja á **Bóka fylgiseðil**.
1. Í flýtiflipanum **Færibreytur**, í reitnum **Magn**, skal velja *Allt*.
1. Veldu **Í lagi**.
1. Ef beðið er um að staðfesta aðgerðina skaltu velja **Í lagi**.
1. Á aðgerðasvæðinu, í flipanum **Reikningur**, í flokknum **Búa til** skal velja á **Reikningur**.
1. Í flýtiflipanum **Færibreytur**, í reitnum **Magn**, skal velja *Allt* eða *Fylgiseðil*.
1. Veldu **Í lagi**.
1. Ef beðið er um að staðfesta aðgerðina skaltu velja **Í lagi**.

## <a name="process-rebate-management-deals"></a><a name="process-deals"></a>Vinna úr tilboðum fyrir stjórnun eftirágreidds afsláttar

Þegar unnið er úr tilboði reiknar kerfið út alla tengda eftirágreidda afslætti og afnotagreiðslur sem eru sett upp. Aðeins verður unnið úr völdum tilboðum sem eru með útreikningstímabil sem eru tilbúin til útreiknings og eru með stöðuna *Virkt*. Þegar vinnslu er lokið býr kerfi til safn færslna sem hægt er að fara yfir og síðan bóka.

> [!NOTE]
> Í öllum tilvikum er unnið úr eftirágreiddum afsláttum á stiginu sem er tilgreint af stillingunni **Afstemma eftir** fyrir hvert tilboð (*Tilboð* eða *Lína*). Aðeins er hægt að gera útreikning einnar línu fyrir tilboð þar sem reiturinn **Afstemma eftir** er stilltur á *Línu*.

### <a name="process-all-lines-for-one-or-more-deals"></a>Vinna úr öllum línum fyrir eitt eða fleiri tilboð

1. Opnið viðeigandi [listasíðu yfir tilboð eftirágreidds afsláttar](rebate-management-deals.md) fyrir tilboðsgerðina sem á að vinna með.
1. Veljið línuna fyrir hvert tilboð sem á að vinna úr (eða opnið tilboðið sem á að vinna úr).
1. Á aðgerðasvæðinu, í flipanum **Tilboð fyrir stjórnun eftirágreidds afsláttar**, í flokknum **Búa til**, skal velja eina af eftirfarandi skipunum:

    - **Vinna úr \> úthlutun** – Úthlutið safn af uppsöfnunum fyrir hvert tilboð eftirágreidds afsláttar sem á við, en ekki bóka það. Þetta valmyndaratriði er ekki í boði fyrir tilboð þar sem reiturinn **Úttak eftirágreidds afsláttar** er stilltur á *Vara*.
    - **Vinna úr \> stjórnunar eftirágreidds afsláttar** – Vinnið úr færsluröð sem gefur upp virði eftirágreidds afsláttar fyrir hvert tilboð.
    - **Ferli \> Afskrift** – Fyrir hverja upprunafærslu eftirágreidds afsláttar og tiltekins tímabils skal vinna úr frávikum milli upphæðanna sem voru bókaðar fyrir úthlutun og fyrir stjórnunar eftirágreidds afsláttar. Þetta valmyndaratriði er ekki í boði fyrir tilboð þar sem reiturinn **Úttak eftirágreidds afsláttar** er stilltur á *Vara*.

1. Í svarglugganum sem birtist skal stilla reitina **Frá dagsetning** og **Til dagsetning** til að skilgreina dagsetningabil útreikningsins.
1. Veljið **Í lagi** til að keyra útreikninginn.

### <a name="process-one-or-more-specific-deal-lines-for-a-selected-deal"></a>Vinna úr einni eða fleiri tilteknum tilboðslínum fyrir valið tilboð

1. Opnið viðeigandi [listasíðu yfir tilboð eftirágreidds afsláttar](rebate-management-deals.md) fyrir tilboðsgerðina sem á að vinna með.
1. Opnið tilboðið þar sem afgreiða á línu úr.
1. Veljið flipann **Línur** efst í hægra horninu.
1. Í flýtiflipanum **Stjórnun eftirágreidds afsláttar** skal velja línuna fyrir hverja tilboðslínu sem á að vinna úr.
1. Í tækjastiku flýtiflipans **Stjórnun eftirágreidds afsláttar** skal velja eina af eftirfarandi skipunum. (Þessar skipanir eru aðeins í boði fyrir tilboð þar sem reiturinn **Afstemma eftir** er stilltur á *Lína*.)

    - **Vinna úr \> úthlutun** – Úthlutið safn af uppsöfnunum fyrir hverja tilboðslínu sem á við, en ekki bóka þær. Þetta valmyndaratriði er ekki í boði fyrir tilboð þar sem reiturinn **Úttak eftirágreidds afsláttar** er stilltur á *Vara*.
    - **Vinna úr \> stjórnunar eftirágreidds afsláttar** – Vinnið úr færsluröð sem gefur upp virði eftirágreidds afsláttar fyrir hverja tilboðslínu.
    - **Ferli \> Afskrift** – Fyrir hverja upprunafærslu eftirágreidds afsláttar og tiltekins tímabils skal vinna úr frávikum milli upphæðanna sem voru bókaðar fyrir úthlutun og fyrir stjórnunar eftirágreidds afsláttar. Þetta valmyndaratriði er ekki í boði fyrir tilboð þar sem reiturinn **Úttak eftirágreidds afsláttar** er stilltur á *Vara*. 

1. Í svarglugganum sem birtist skal stilla reitina **Frá dagsetning** og **Til dagsetning** til að skilgreina dagsetningabil útreikningsins.
1. Veljið **Í lagi** til að keyra útreikninginn.

### <a name="process-deals-using-a-batch-job"></a>Vinna úr tilboðum með runuvinnslu

Í stað þess að vinna úr sérstökum tilboðum eða tilboðslínum er hægt að keyra runuvinnslu til að vinna úr nokkrum tilboðum samtímis. Það má nota færslusíur og/eða setja upp endurtekna áætlun. Til að vinna úr tilboðum með runuvinnslu skal fylgja þessum skrefum.

1. Fylgið einu af eftirfarandi skrefum:

    - Farið í **Stjórnun eftirágreidds afsláttar \> Reglubundin verk \> Vinna úr \> Úthlutun** til að úthluta safn uppsafnanna fyrir hverja línu sem á við, en án þess að bóka þær.
    - Farið í **Stjórnun eftirágreidds afsláttar \> Reglubundin verk \> Vinna úr \> Stjórnun eftirágreidds afsláttar** til að vinna úr færsluröð sem gefur upp virði eftirágreidds afsláttar fyrir hvert tilboð.
    - Farið í **Stjórnun eftirágreidds afsláttar \> Reglubundin verk \> Vinna úr \> Afskrifa** til að bakfæra áður bókaðar færslur til að afskrifa þær þannig að hægt sé að reikna út nýjar tilboðsfærslur eftirágreidds afsláttar.

1. Í svarglugganum sem birtist, í flýtiflipanum **Færibreytur**, í hlutanum **Tímabil**, skal stilla reitina **Frá dagsetning** og **Til dagsetning** til að skilgreina dagsetningabilið fyrir færslur útreikningsins.
1. Í hlutanum **Tímabil tryggingar** skal stilla reitina **Frá dagsetning** og **Til dagsetning** til að skilgreina dagsetningabilið fyrir tryggingar útreikningsins.
1. Í flýtiflipanum **Færslur til að taka með** er hægt að setja upp síur til að takmarka safn tilboða sem runuvinnslan vinnur úr. Þessar stillingar virka á sama hátt og þær virka fyrir aðrar gerðir af runuvinnslum.
1. Í flýtiflipanum **Keyra í bakgrunni** er hægt að setja upp valkosti runuvinnslu og áætlanagerðar eftir þörfum. Þessar stillingar virka á sama hátt og þær virka fyrir aðrar gerðir af runuvinnslum.
1. Veljið **Í lagi** til að keyra og/eða tímasetja útreikninginn.

### <a name="process-deals-by-using-the-rebate-workbench"></a>Tilboð afgreidd með vinnusvæði eftirágreidds afsláttar

Í stað þess að afgreiða ákveðin tilboð eða tilboðslínur er hægt að nota *vinnusvæði eftirágreidds afsláttar* til að afgreiða mörg tilboð samtímis. Það má nota færslusíur og/eða setja upp endurtekna áætlun. Þú þarft ekki að velja neinar raðir. Kerfið mun vinna úr öllum línum sem uppfylla kröfur um dagsetningu og síur sem þú setur upp.

Til að afgreiða tilboð með vinnusvæði eftirágreidds afsláttar skal fylgja þessum skrefum.

1. Farðu í **Stjórnun eftirágreidds afsláttar \> Tilboð fyrir stjórnun eftirágreidds afsláttar \> Vinnusvæði eftirágreidds afsláttar**.
1. Á aðgerðasvæðinu, í flipanum **Vinnusvæði eftirágreidds afsláttar**, í flokknum **Úrvinnsla**, skal velja eina af eftirfarandi skipunum:

    - **Vinna úr \> úthlutun** – Úthlutið safn af uppsöfnunum fyrir hverja tilboðslínu sem á við, en ekki bóka þær.
    - **Vinna úr \> stjórnunar eftirágreidds afsláttar** – Vinnið úr færsluröð sem gefur upp virði eftirágreidds afsláttar fyrir hverja tilboðslínu.
    - **Afgreiða \> Afskrift** – Afgreiddu frávikið milli úthlutunar og stjórnunar eftirágreidds afsláttar sem er bókað fyrir hverja upprunalega færslu eftir tilboði eftirágreidds afsláttar og tilteknu tímabili.

1. Í svarglugganum **Stjórnun eftirágreidds afsláttar**, í hlutanum **Tímabil**, skal stilla reitina **Frá dagsetningu** og **Til dagsetningar** til að skilgreina dagsetningabil fyrir útreikninginn.
1. Í hlutanum **Tímabil tryggingar** skal stilla reitina **Frá dagsetning** og **Til dagsetning** til að skilgreina dagsetningabilið fyrir tryggingar útreikningsins.
1. Í flýtiflipanum **Færslur til að taka með** er hægt að setja upp síur til að takmarka safn tilboða sem runuvinnslan vinnur úr. Þessar stillingar virka á sama hátt og þær virka fyrir aðrar gerðir af runuvinnslum.
1. Í flýtiflipanum **Keyra í bakgrunni** er hægt að setja upp valkosti runuvinnslu og áætlanagerðar eftir þörfum. Þessar stillingar virka á sama hátt og þær virka fyrir aðrar gerðir af runuvinnslum.
1. Veljið **Í lagi** til að keyra og/eða tímasetja útreikninginn.

## <a name="view-and-edit-rebate-management-transactions"></a>Skoða og breyta færslum fyrir stjórnun eftirágreidds afsláttar

Þegar unnið er úr einu eða fleiri tilboðum býr kerfið til færslur sem hægt er að skoða og hugsanlega breyta áður en þær eru bókaðar.

### <a name="view-and-edit-rebate-management-transactions-by-using-the-rebate-deals-list-page"></a>Skoða og breyta færslum fyrir stjórnun eftirágreidds afsláttar með því að nota listasíðu eftirágreidds afsláttar

Til að skoða og breyta færslum eftirágreidds afsláttar með listasíðu eftirágreidds afsláttar skal fylgja þessum skrefum.

1. Fylgið einu af eftirfarandi skrefum:

    - Veldu tilboð til að skoða færslur fyrir (til dæmis á [**Öll tilboð fyrir stjórnun eftirágreidds afsláttar** síðunni](rebate-management-deals.md)). Á aðgerðasvæðinu, í flipanum **Tilboð fyrir stjórnun eftirágreidds afsláttar**, í flokknum **Færslur**, skal velja **Færslur** eða **Færslur tryggingar**, eftir því hvaða færslugerð á að skoða.
    - Veldu tilboð (til dæmis á [**Öll tilboð fyrir stjórnun eftirágreidds afsláttar** síðunni](rebate-management-deals.md)) til að skoða upplýsingar þess. Í flýtiflipanum **Stjórnun eftirágreidds afsláttar** skal velja tilboðslínuna þar sem á að skoða færslunar. Á tækjastikunni skal því næst velja **Færslur** eða **Færslur tryggingar** eftir því hvaða færslugerð á að skoða. (Þessir hnappar eru aðeins í boði fyrir tilboð þar sem reiturinn **Afstemma eftir** er stilltur á *Lína*.)

1. Síðan **Færsludagsetningar fyrir stjórnun eftirágreidds afsláttar** eða **Tryggingarfærslur fyrir stjórnun eftirágreidds afsláttar** birtist. Hún inniheldur hnitanet þar sem hver lína stendur fyrir færslusafn fyrir einn eftirágreiddan afslátt eða tryggingatímabil. Veljið línu í hnitanetinu og síðan á aðgerðasvæðinu skal velja **Upprunafærslur** til að skoða færslurnar sem tilheyra þeirri línu.
1. Síðan sem birtist sýnir lista yfir færslur af valinni gerð sem tilheyra valinni línu. Hver færsla veitir viðeigandi upplýsingar, allt eftir færslugerðinni. Fyrir tryggingafærslur er aðeins hægt að skoða listann. Fyrir aðrar aðgerðir er hægt að framkvæma eftirfarandi aðgerðir á þessari síðu:

    - Til að staðfesta heildarvirði allra færslna á síðunni sem hafa verið innheimtar skal skoða reitinn **Innheimt upphæð**.
    - Til að skoða frekari upplýsingar um hvaða færslu sem er skal velja hana og síðan velja flipann **Almennt**, **Fjárhagsvídd** eða **Vídd**.
    - Til að skoða allar lækkanir sem eiga við skal velja **Lækkunarfærslur** á aðgerðasvæðinu. Frekari upplýsingar er að finna í [Reglur um lækkun eftirágreidds afsláttar](rebate-reduction-principle.md).
    - Til að merkja færslur annaðhvort sem innheimtar eða óinnheimtar ef innheimtuferlið er notað, skal velja viðeigandi línur og síðan á aðgerðasvæðinu velja eina af eftirfarandi skipunum. (Innheimtuferli eru virkjuð á síðunni [**Færibreytur fyrir stjórnun eftirágreidds afsláttar**](rebate-management-parameters.md).)

        - **Stilla innheimt \> Allt** – Merkja allar færslur sem innheimtar.
        - **Stilla innheimt \> Valið** – Merkja valdar færslur sem innheimtar.
        - **Stilla óinnheimt \> Allt** – Merkja allar færslur sem óinnheimtar.
        - **Stilla óinnheimt \> Valið** – Merkja valdar færslur sem óinnheimtar.

    - Veljið **Bóka** á aðgerðasvæðinu til að bóka kröfuna fyrir allar línur sem eiga við. Ef kröfuferli er notað (þegar valkosturinn **Nota kröfuferli** er virkjaður á síðunni **Færibreytur fyrir stjórnun eftirágreidds afsláttar**) eru eingöngu línurnar sem merktar eru **Til innheimtu** bókaðar. Annars eru allar upprunafærslur fyrir valda færslu eftirágreidds afsláttar bókaðar. Hnappurinn **Bóka** er aðeins í boði fyrir færslur eftirágreidds afsláttar. Hann er ekki í boði fyrir úthlutun og afskriftafærslur. Í svarglugganum **Bóka** eru reitirnir **Frá dagsetning** og **Til dagsetning** fylltir út sjálfkrafa. Stilltu **Bókunardagsetning** reitinn og veldu svo **Í lagi**.
    - Til að stilla upphæðina sem birtist fyrir allar opnar eða óbókaðar færslur skal velja færsluna og síðan fylgja einu af þessum skrefum:

        - Breyttu gildinu í **Leiðrétt upphæð** reitnum.
        - Á aðgerðasvæðinu skal velja **Stilla leiðréttingu**. Í felliglugganum sem birtist skal því næst slá inn gildi í reitinn **Leiðrétt upphæð**.

> [!NOTE]
> Ef kröfuferli er notað, þegar unnið er úr næsta tímabili, mun færslulistinn innihalda óinnheimtar færslur frá fyrri bókun ásamt nýjum færslum fyrir valið tímabil.

### <a name="view-and-edit-rebate-management-transactions-by-using-the-rebate-workbench"></a>Skoða og breyta færslum fyrir stjórnun eftirágreidds afsláttar með því að nota vinnusvæði eftirágreidds afsláttar

Til að skoða og breyta færslum fyrir stjórnun eftirágreidds afsláttar með því að nota vinnusvæði eftirágreidds afsláttar skal fylgja þessum skrefum.

1. Farðu í **Stjórnun eftirágreidds afsláttar \> Tilboð fyrir stjórnun eftirágreidds afsláttar \> Vinnusvæði eftirágreidds afsláttar**.
1. Stilltu reitinn **Sýna** á *Ekki bókað*.
1. Síðan **Vinnusvæði eftirágreidds afsláttar** sýnir lista yfir færslurnar. Hver færsla veitir viðeigandi upplýsingar. Upplýsingarnar geta verið mismunandi, eftir gerð færslunnar. Á þessari síðu er hægt að framkvæma eftirfarandi aðgerðir:

    - Til að skoða frekari upplýsingar um hvaða færslu sem er skal velja hana og síðan velja flipann **Almennt**, **Fjárhagsvídd** eða **Vídd**.
    - Ef þú ert að nota kröfuferli getur þú merkt færslur sem annaðhvort innheimtar eða óinnheimtar. Veldu viðeigandi línur og síðan á aðgerðasvæðinu, í flipanum **Vinnusvæði eftirágreidds afsláttar**, skal velja eina af eftirfarandi skipunum. (Innheimtuferli eru virkjuð á síðunni [**Færibreytur fyrir stjórnun eftirágreidds afsláttar**](rebate-management-parameters.md).)

        - **Stilla innheimt** – Merkja valdar færslur sem innheimtar.
        - **Stilla óinnheimt** – Merkja valdar færslur sem óinnheimtar.

    - Til að bóka kröfu fyrir eina eða fleiri línur skal velja línurnar sem eiga við. Því næst á aðgerðasvæðinu, í flipanum **Vinnusvæði eftirágreidds afsláttar**, skal velja **Bóka**. Hnappurinn **Bóka** er tiltækur fyrir úthlutun, eftirágreiddan afslátt og afskriftafærslur. Í svarglugganum **Bóka** eru reitirnir **Frá dagsetning** og **Til dagsetning** fylltir út sjálfkrafa. Stilltu **Bókunardagsetning** reitinn og veldu svo **Í lagi**.
    - Til að stilla upphæðina sem birtist fyrir allar opnar eða óbókaðar færslur skal velja færsluna og síðan fylgja einu af þessum skrefum:

        - Breyttu gildinu í **Leiðrétt upphæð** reitnum.
        - Á aðgerðasvæðinu, í flipanum **Vinnusvæði eftirágreidds afsláttar**, skal velja **Stilla leiðréttingu**. Í felliglugganum sem birtist skal því næst slá inn gildi í reitinn **Leiðrétt upphæð**.

> [!NOTE]
> Ef kröfuferli er notað, þegar unnið er úr næsta tímabili, mun færslulistinn innihalda óinnheimtar færslur frá fyrri bókun ásamt nýjum færslum fyrir valið tímabil.

## <a name="post-rebates-transactions"></a>Bóka endurgreiðslufærslur

Til að bóka virði úthlutunar, upphæð fyrir stjórnunar eftirágreidds afsláttar og afskrift þarf að keyra bókunarferlið. Bókunarferlið merkir úthlutun, stjórnunar eftirágreidds afsláttar og afskriftafærslur sem bókaðar og býr til markfærsluna. Ef ekki þarf að yfirfara markfærsluna er hægt að setja upp þessar færslur þannig að þær verði bókaðar sjálfkrafa.

### <a name="set-up-the-system-to-post-all-target-transactions-automatically"></a>Setja upp kerfið til að bóka allar markfærslur sjálfkrafa

Til að setja upp kerfi til að bóka allar markfærslur um leið og þær eru myndaðar af bókunarúthlutun, upphæð fyrir stjórnun eftirágreidds afsláttar og afskrift skal kveikja á valkostinum **Bóka færslubækur sjálfkrafa** og/eða **Bóka reikninga með frjálsum texta sjálfkrafa** á síðunni **Færibreytur fyrir stjórnun eftirágreidds afsláttar**. Frekari upplýsingar er að finna í [Færibreytur stjórnunar eftirágreidds afsláttar](rebate-management-parameters.md).

### <a name="post-transactions-for-all-lines-for-one-or-more-deals"></a>Bóka færslur fyrir allar línur fyrir eitt eða fleiri tilboð

Þegar búið er að vinna úr tilboðum sem eiga við skal fylgja þessum skrefum til að fara yfir og bóka myndaðar færslur fyrir allar línur fyrir eitt eða fleiri tilboð.

1. Opnið viðeigandi [listasíðu yfir tilboð eftirágreidds afsláttar](rebate-management-deals.md) fyrir tilboðsgerðina sem á að vinna með.
1. Veljið línuna fyrir hvert tilboð sem á að bóka (eða opnið tilboðið sem á að bóka).
1. Á aðgerðasvæðinu, í flipanum **Tilboð fyrir stjórnun eftirágreidds afsláttar**, í flokknum **Búa til**, skal velja eina af eftirfarandi skipunum:

    - **Bóka \> úhlutun** – Bókið tiltækar uppsöfnunarfærslur sem hafa verið stofnaðar.
    - **Bóka \> Stjórnun eftirágreidds afsláttar** – Bókið tiltækar færslur eftirágreidds afsláttar sem hafa verið stofnaðar.
    - **Bóka \> Afskrift** – Bókið tiltækar afskriftafærslur sem hafa verið stofnaðar.

1. Í svarglugganum sem birtist skal stilla reitinn **Bókunardagsetning**. Síðan skal stilla reitina **Frá dagsetning** og **Til dagsetning** til að skilgreina dagsetningabil fyrir færslurnar sem þarf að bóka.
1. Veldu **Í lagi** til að bóka færsluna.

### <a name="post-transactions-for-one-or-more-specific-deal-lines-for-a-selected-deal"></a>Bóka færslur fyrir eina eða fleiri tilteknar tilboðslínur fyrir valið tilboð

Þegar búið er að vinna úr tilboðum sem eiga við skal fylgja þessum skrefum til að fara yfir og bóka myndaðar færslur fyrir eina eða fleiri tilteknar tilboðslínur fyrir valið tilboð. Þetta ferli á aðeins við fyrir tilboð þar sem reiturinn **Afstemma eftir** er stilltur á *Lína*.

1. Opnið viðeigandi [listasíðu yfir tilboð eftirágreidds afsláttar](rebate-management-deals.md) fyrir tilboðsgerðina sem á að vinna með.
1. Opnaðu tilboðið sem er með línu sem þú vilt bóka færslur fyrir.
1. Veljið flipann **Línur** efst í hægra horninu.
1. Í flýtiflipanum **Stjórnun eftirágreidds afsláttar** skal velja línuna fyrir hverja tilboðslínu sem á að bóka.
1. Í tækjastiku flýtiflipans **Stjórnun eftirágreidds afsláttar** skal velja eina af eftirfarandi skipunum. (Þessar skipanir eru aðeins í boði fyrir tilboð þar sem **Afstemma eftir** er stillt á *Lína*.)

    - **Bóka \> úhlutun** – Bókið tiltækar uppsöfnunarfærslur sem hafa verið stofnaðar.
    - **Bóka \> Stjórnun eftirágreidds afsláttar** – Bókið tiltækar færslur eftirágreidds afsláttar sem hafa verið stofnaðar.
    - **Bóka \> Afskrift** – Bókið tiltækar afskriftafærslur sem hafa verið stofnaðar.

1. Í svarglugganum sem birtist skal stilla reitinn **Bókunardagsetning**. Síðan skal stilla reitina **Frá dagsetning** og **Til dagsetning** til að skilgreina dagsetningabil fyrir færslurnar sem þarf að bóka.
1. Veldu **Í lagi** til að bóka færsluna.

### <a name="post-transactions-using-a-batch-job"></a>Bóka færslur með runuvinnslu

Í stað þess að bóka færslur fyrir tiltekin tilboð eða tilboðslínur er hægt að keyra runuvinnslu til að bóka færslur fyrir nokkur tilboð samtímis. Það má nota færslusíur og/eða setja upp endurtekna áætlun. Til að bóka færslur með runuvinnslu skal fylgja þessum skrefum.

1. Fylgið einu af eftirfarandi skrefum:

    - Farið í **Stjórnun eftirágreidds afsláttar \> Reglubundin verk \> Bóka \> Úthlutun** til að bóka tiltækar uppsöfnunarfærslur sem hafa verið stofnaðar.
    - Farið í **Stjórnun eftirágreidds afsláttar \> Reglubundin verk \> Bóka \> Stjórnun eftirágreidds afsláttar** til að bóka tiltækar færslur eftirágreidds afsláttar sem hafa verið stofnaðar.
    - Farið í **Stjórnun eftirágreidds afsláttar \> Reglubundin verk \> Bóka \> Afskrift** til að bóka tiltækar afskriftafærslur sem hafa verið stofnaðar.

1. Í svarglugganum sem birtist í flýtiflipanum **Færibreytur**, í hlutanum **Tímabil**, skal stilla reitinn **Bókunardagsetning**. Síðan skal stilla reitina **Frá dagsetning** og **Til dagsetning** til að skilgreina dagsetningabil fyrir færslurnar sem þarf að bóka.
1. Í hlutanum **Tímabil tryggingar** skal stilla reitina **Frá dagsetning** og **Til dagsetning** til að skilgreina dagsetningabilið fyrir tryggingar sem þarf að bóka.
1. Í flýtiflipanum **Færslur til að taka með** er hægt að setja upp síur til að takmarka safn tilboða sem runuvinnslan vinnur úr. Þessar stillingar virka á sama hátt og þær virka fyrir aðrar gerðir af runuvinnslum.
1. Í flýtiflipanum **Keyra í bakgrunni** er hægt að setja upp valkosti runuvinnslu og áætlanagerðar eftir þörfum. Þessar stillingar virka á sama hátt og þær virka fyrir aðrar gerðir af runuvinnslum.
1. Veljið **Í lagi** til að keyra og/eða tímasetja útreikninginn.

### <a name="post-transactions-by-using-the-rebate-workbench"></a>Bóka færslur með vinnusvæði eftirágreidds afsláttar

Þegar búið er að vinna úr úthlutun, eftirágreiddum afslætti eða afskriftafærslum skal fylgja þessum skrefum til að nota vinnusvæði eftirágreidds afsláttar til að fara yfir og bóka myndaðar færslur fyrir eina eða fleiri tilteknar færslulínur fyrir öll tilboð.

1. Farðu í **Stjórnun eftirágreidds afsláttar \> Tilboð fyrir stjórnun eftirágreidds afsláttar \> Vinnusvæði eftirágreidds afsláttar**.
1. Í hnitanetinu skal velja línu fyrir hverja færslulínu sem á að bóka. Hægt er að velja óbókaða úthlutun, eftirágreiddan afslátt og/eða afskriftafærslur. Eftirfarandi reglur gilda:

    - Kerfið mun einnig bóka allar línur sem eru með sama gildið fyrir **Færslunúmer eftirágreidds afsláttar** og línurnar sem þú valdir.
    - Kerfið mun ekki bóka neinar línur af færslugerðinni *Eftirágreiddur afsláttur* sem eru ekki merktar sem innheimtar.
    - Ef þú velur línur sem hafa þegar verið bókaðar mun kerfið sleppa bókuðu línunum.
    - Hnappurinn **Bóka** er aðeins í boði ef þú velur a.m.k. eina óbókaða línu.

1. Á aðgerðasvæðinu, í flipanum **Vinnusvæði eftirágreidds afsláttar**, í flokknum **Úrvinnsla**, skal velja **Bóka**.
1. Í svarglugganum **Bóka** skal stilla reitinn **Bókunardagsetning**. Reitirnir **Frá dagsetningu** og **Til dagsetningar** eru sjálfkrafa stilltir, byggt á fyrsta gildinu fyrir **Frá dagsetningu** og síðast gildinu fyrir **Til dagsetningar** fyrir valdar línur.
1. Veldu **Í lagi** til að bóka færsluna.

## <a name="review-rebate-management-journals"></a><a name="review-journals"></a>Yfirfara færslubækur fyrir stjórnunar eftirágreidds afsláttar

Þegar færslurnar hafa verið bókaðar er hægt að fara yfir færslubækurnar, skjölin eða vörurnar. Markfærslurnar fyrir eftirágreidda afslætti og afnotagreiðslur byggja á greiðslugerðinni sem er stillt í bókunarreglu og úttaksgerð eftirágreidds afsláttar. Til dæmis ef úttak eftirágreidds afsláttar er stillt á *Vöru* verður sölupöntun stofnuð fyrir eftirágreiddan afslátt viðskiptavinar og innkaupapöntun verður stofnuð fyrir eftirágreiddan afslátt lánardrottins. Þessar pantanir má skoða í gegnum markfærslurnar. Annars, ef greiðslan er sett upp til að nota viðskiptaskuldir, verður lánardrottnareikningur fyrir lánardrottin sem settur er upp fyrir viðskiptavin stofnaður fyrir eftirágreidda afslætti viðskiptavinar.

### <a name="review-journals-by-using-the-rebate-deals-list-page"></a>Farðu yfir dagbækur með því að nota afsláttartilboðslistasíðuna

Til að yfirfara færslur færslubókar sem tengjast tilboði fyrir stjórnunar eftirágreidds afsláttar skal fylgja þessum skrefum.

1. Opnið viðeigandi [listasíðu yfir tilboð eftirágreidds afsláttar](rebate-management-deals.md) fyrir tilboðsgerðina sem á að vinna með.
1. Veljið tilboðið til að skoða færslur í færslubók fyrir.
1. Á aðgerðasvæðinu, í flipanum **Tilboð fyrir stjórnun eftirágreidds afsláttar**, í flokknum **Færslur**, skal annaðhvort velja **Færslur** eða **Ábyrgðarfærslur** eftir því hvaða færslugerð á að skoða.
1. Stilltu reitinn **Sýna** á *Allt* eða *Bókað*.
1. Finnið og veljið færslusafnið sem á að skoða og því næst, á aðgerðasvæðinu, skal velja einn af eftirfarandi hnöppum. (Þessir hnappar eru aðeins tiltækir þegar viðeigandi bókanir eru til staðar fyrir valið færslusafn.)

    - **Markfærslur** – Farið yfir viðeigandi færslubækur og aðrar skjalagerðir sem voru myndaðar af völdu tilboði.
    - **Vörur** – Farið yfir viðeigandi sölupantanir eða innkaupapantanir sem voru myndaðar af völdu tilboði.

1. Listi yfir viðeigandi færslubækur, skjöl eða vörur birtist. Til að skoða frekari upplýsingar um einhverja færslubók, skjal eða vöru skal velja línu þess og síðan á aðgerðasvæðinu skal velja **Skoða upplýsingar**.

### <a name="review-journals-by-using-the-rebate-workbench"></a>Yfirfara færslubækur með vinnusvæði eftirágreidds afsláttar

Til að yfirfara færslubækur með því að nota vinnusvæði eftirágreidds afsláttar skal fylgja þessum skrefum.

1. Farðu í **Stjórnun eftirágreidds afsláttar \> Tilboð fyrir stjórnun eftirágreidds afsláttar \> Vinnusvæði eftirágreidds afsláttar**.
1. Stilltu reitinn **Sýna** á _Allt_ eða _Bókað_.
1. Finndu og veldu línuna sem þú vilt kanna nánar. Á aðgerðasvæðinu, í flipanum **Vinnusvæði eftirágreidds afsláttar**, í flokknum **Yfirlit**, skal því næst velja **Markfærslur**. Þessi hnappur er aðeins tiltækur ef viðeigandi bókanir eru til staðar fyrir valda línu.
1. Listi yfir viðeigandi færslubækur, skjöl eða vörur birtist. Til að skoða frekari upplýsingar um einhverja færslubók, skjal eða vöru skal velja línu þess og síðan á aðgerðasvæðinu skal velja **Skoða upplýsingar**.

## <a name="rebate-management-transactions-on-the-deduction-workbench"></a>Færslur eftirágreidds afsláttar á frádráttarvinnusvæðinu

Þegar þú bókar færslu eftirágreidds afsláttar sem er með eitt af eftirfarandi gildum **Greiðslugerðar** býr kerfið til frádráttarbók viðskiptavinar eða reikning með frjálsum texta fyrir viðeigandi viðskiptavinalykil:

- Frádráttur viðskiptavinar
- Skattleggja frádrátt viðskiptavinareiknings
- Kostnaður við vörumerki
- Skýrslugerð

Eftir að markfærsla hefur verið stofnuð og bókuð verður hún í boði sem opin færsla á síðunni **Frádráttarvinnusvæði** (**Sala og markaðssetning \> Afsláttur \> Frádrættir \> Frádráttarvinnusvæði**). Opnar færslur hafa gildi **Kröfugerðar** fyrir *Stjórnun eftirágreidds afsláttar* og gildi fyrir **Færslunúmer eftirágreidds afsláttar** er í boði til að gera rakningu mögulega. Dagsetningin er stillt á bókunardagsetningu markfærslu eftirágreidds afsláttar. Til að nota frádráttarvinnusvæðið til að jafna opnar færslur á móti fyrirliggjandi frádráttum fyrir sama viðskiptavinalykilinn skal velja **Vinna með \> Jafna** á aðgerðasvæðinu.

Frekari upplýsingar er að finna í [Stjórna frádráttum með frádráttarvinnusvæðinu](deduction-workbench.md).

## <a name="purge-unposted-transactions"></a>Hreinsa óbókaðar færslur

Þegar búið er að afgreiða úthlutun, eftirágreiddan afslátt eða afskriftafærslur skal fylgja þessum skrefum til að hreinsa valdar óbókaðar færslur.

1. Farðu í **Stjórnun eftirágreidds afsláttar \> Tilboð fyrir stjórnun eftirágreidds afsláttar \> Vinnusvæði eftirágreidds afsláttar**.
2. Stilltu reitinn **Sýna** á *Ekki bókað*.
3. Finna og velja þær færslur sem á að eyða. Á aðgerðasvæðinu, í flipanum **Vinnusvæði eftirágreidds afsláttar**, í flokknum **Úrvinnsla**, skal því næst velja **Hreinsa**.
4. Veldu **Í lagi** til að eyða óbirtum færslum.

## <a name="cancel-a-posted-provision"></a>Hætta við birt ákvæði

Þegar búið er að vinna úr og bóka úthlutun skal fylgja þessum skrefum til að hætta við bókaðar úthlutunarfærslur.

1. Farðu í **Stjórnun eftirágreidds afsláttar \> Tilboð fyrir stjórnun eftirágreidds afsláttar \> Vinnusvæði eftirágreidds afsláttar**.
2. Stilltu reitinn **Sýna** á *Bókað*.
3. Finndu og veldu úthlutunarfærslurnar sem hætta á við. Á aðgerðasvæðinu, í flipanum **Vinnusvæði eftirágreidds afsláttar**, í flokknum **Úrvinnsla**, skal því næst velja **Hætta við úthlutun**.
4. Veldu **Í lagi** til að bakfæra færsluna.

Þessi bakfærsla úthlutunar verður einnig sýnileg í viðeigandi [Færslubókum eftirágreidds afsláttar](#review-journals).
