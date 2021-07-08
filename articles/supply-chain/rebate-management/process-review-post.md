---
title: Meðhöndla, yfirfara og bóka eftirágreiddan afslátt
description: Þetta efnisatriði lýsir því hvernig á að vinna úr tilboðum eftirágreidds afsláttar, reikna út afslættina, fara yfir færslurnar sem eru búnar til, bóka færslur og fara yfir bókanirnar.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateDeal
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 82b8a4e6ba7ebea7df9f5dad5abc3dfc3ce2687d
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270762"
---
# <a name="process-review-and-post-rebates"></a>Meðhöndla, yfirfara og bóka eftirágreiddan afslátt

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir því hvernig á að vinna úr tilboðum eftirágreidds afsláttar, reikna út afslættina, fara yfir færslurnar sem eru búnar til, bóka færslur og fara yfir bókanirnar.

## <a name="change-the-status-of-a-deal"></a>Breyta stöðu tilboðs

Hægt er að úthluta hverju tilboði stöðu til að auðvelda rakningu þess. Stöðunni er aðeins ætlað að veita upplýsingar.

1. Veldu tilboð (til dæmis á [**Öll tilboð fyrir stjórnun eftirágreidds afsláttar** síðunni](rebate-management-deals.md)).
1. Á aðgerðasvæðinu, í flipanum **Tilboð fyrir stjórnun eftirágreidds afsláttar**, í flokknum **Vinna með**, skal velja **Breyta stöðu**.
1. Í svarglugganum **Breyta stöðu** skal stilla reitinn **Staða eftirágreidds afsláttar** á nýja stöðu.
1. Veljið **Í lagi**.

## <a name="calculate-fifo-purchase-prices"></a>Reikna út innkaupaverð samkvæmt FIFO

Keyra þarf reglubundna verkið **Reikna út innkaupaverð samkvæmt FIFO** til að reikna eftirágreiddan afslátt fyrir [tilboð](rebate-management-deals.md) þar sem reiturinn **Verðgrunnur** er stilltur á *FIFO*. Kerfið notar fyrst inn, fyrst út (FIFO) regluna til að reikna út virði birgðanna sem voru seldar. Þetta virði verður síðan notað til að reikna út eftirágreiddan afslátt lánardrottins.

Farið í **Stjórnun eftirágreidds afsláttar \> Reglubundin verk \> Reikna út innkaupaverð samkvæmt FIFO**. Í svarglugganum sem birtist skal velja **Í lagi** til að keyra útreikninginn.

## <a name="process-rebate-management-deals"></a>Vinna úr tilboðum fyrir stjórnun eftirágreidds afsláttar

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

## <a name="view-and-edit-rebate-management-transactions"></a>Skoða og breyta færslum fyrir stjórnun eftirágreidds afsláttar

Þegar unnið er úr einu eða fleiri tilboðum býr kerfið til færslur sem hægt er að skoða og hugsanlega breyta áður en þær eru bókaðar.

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

## <a name="review-rebate-management-journals"></a>Yfirfara færslubækur fyrir stjórnunar eftirágreidds afsláttar

Þegar færslurnar hafa verið bókaðar er hægt að fara yfir færslubækurnar, skjölin eða vörurnar. Markfærslurnar fyrir eftirágreidda afslætti og afnotagreiðslur byggja á greiðslugerðinni sem er stillt í bókunarreglu og úttaksgerð eftirágreidds afsláttar. Til dæmis ef úttak eftirágreidds afsláttar er stillt á *Vöru* verður sölupöntun stofnuð fyrir eftirágreiddan afslátt viðskiptavinar og innkaupapöntun verður stofnuð fyrir eftirágreiddan afslátt lánardrottins. Þessar pantanir má skoða í gegnum markfærslurnar. Annars, ef greiðslan er sett upp til að nota viðskiptaskuldir, verður lánardrottnareikningur fyrir lánardrottin sem settur er upp fyrir viðskiptavin stofnaður fyrir eftirágreidda afslætti viðskiptavinar.

Til að yfirfara færslur færslubókar sem tengjast tilboði fyrir stjórnunar eftirágreidds afsláttar skal fylgja þessum skrefum.

1. Opnið viðeigandi [listasíðu yfir tilboð eftirágreidds afsláttar](rebate-management-deals.md) fyrir tilboðsgerðina sem á að vinna með.
1. Veljið tilboðið til að skoða færslur í færslubók fyrir.
1. Á aðgerðasvæðinu, í flipanum **Tilboð fyrir stjórnun eftirágreidds afsláttar**, í flokknum **Færslur**, skal annaðhvort velja **Færslur** eða **Ábyrgðarfærslur** eftir því hvaða færslugerð á að skoða.
1. Gangið úr skugga um að reiturinn **Sýna** sé stilltur á *Allt* eða *Bókað*.
1. Finnið og veljið færslusafnið sem á að skoða og því næst, á aðgerðasvæðinu, skal velja einn af eftirfarandi hnöppum. (Þessir hnappar eru aðeins tiltækir þegar viðeigandi bókanir eru til staðar fyrir valið færslusafn.)

    - **Markfærslur** – Farið yfir viðeigandi færslubækur og aðrar skjalagerðir sem voru myndaðar af völdu tilboði.
    - **Vörur** – Farið yfir viðeigandi sölupantanir eða innkaupapantanir sem voru myndaðar af völdu tilboði.

1. Listi yfir viðeigandi færslubækur, skjöl eða vörur birtist. Til að skoða frekari upplýsingar um einhverja færslubók, skjal eða vöru skal velja línu þess og síðan á aðgerðasvæðinu skal velja **Skoða upplýsingar**.
