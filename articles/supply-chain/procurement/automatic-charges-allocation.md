---
title: Sjálfvirk úthlutun gjalda
description: Eiginleiki gjalda í Microsoft Dynamics 365 Supply Chain Management auðveldar þér að úthluta gjöldum sjálfkrafa á innkaupapantanir eða sölupantanir.
author: dasani-madipalli
manager: tfehr
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-10-01
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: eddcf275c14565dfe77fbe7efa676be4a34da686
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5244160"
---
# <a name="automatic-allocation-of-charges"></a>Sjálfvirk úthlutun gjalda

[!include [banner](../includes/banner.md)]

Hægt er að nota tiltekin viðbótargjöld út frá viðskiptavininum sem þú ert að vinna með eða vörunni sem þú ert að selja. Eiginleiki *gjalda* í Microsoft Dynamics 365 Supply Chain Management auðveldar þér að úthluta gjöldum sjálfkrafa á innkaupapantanir eða sölupantanir.

Sjálfvirk gjöld eru sjálfkrafa notuð þegar búin er til sölupöntun eða innkaupapöntun. Hægt er að skilgreina sjálfvirk gjöld fyrir tiltekna lánardrottna, viðskiptavini, lánardrottnaflokka eða vörur. Einnig er hægt að skilgreina sjálfvirk gjöld sem eiga við alla lánardrottna, viðskiptavini eða vöru.

## <a name="set-up-charges-codes"></a>Setja upp gjaldakóða

Til að úthluta gjöldum þarf fyrst að skilgreina gjaldakóða.

1. Fylgið einu af eftirfarandi skrefum:

    - Fyrir innkaupapantanir: Farið í **Viðskiptaskuldir \> Uppsetning gjalda \> Gjaldakóði**.
    - Fyrir sölupantanir: Farið í **Viðskiptakröfur \> Uppsetning gjalda \> Gjaldakóðar**.

1. Á aðgerðasvæðinu skal velja **Nýr** til að stofna gjaldakóða.
1. Í haus nýju færslunnar skal stilla eftirfarandi reiti:

    - **Gjaldakóði** - Færið inn kóða fyrir gjöldin.
    - **Lýsing** - Færið inn lýsingu á gjöldunum.
    - **VSK-flokkur vöru** - Veljið VSK-flokk vöru ef það á við.
    - **Skipta niður** - Stillið þennan valkost á *Já* ef á að skipta niður gjöldunum. Þessi valkostur er eingöngu í boði fyrir sölupantanir.
    - **Hámarksupphæð** - Færið inn hámarksupphæð sem leyfð er fyrir gjaldakóðann. Þessi reitur er notaður til að staðfesta gjöld fyrir reikninga lánardrottins. Hann er aðeins í boði fyrir innkaupapantanir.

        > [!NOTE]
        > Til að kveikja á virkni fyrir staðfestingu gjalda fyrir innkaupapantanir er farið í **Viðskiptaskuldir \> Uppsetning \> Færibreytur viðskiptaskulda**. Í flýtiflipanum **Prófun reiknings**, í hlutanum **Prófun reiknings**, skal stilla valkostinn **Virkja prófun á samsvörun reiknings** á *Já*.

1. Flýtiflipinn **Bókun** inniheldur **Debet** og **Kredit** hluta. Stillið eftirfarandi reiti, allt eftir fjárhagnum sem á að bóka gjöldin á:

    - **Gerð** - Veljið gerð lykils sem bókað er á (*Fjárhagur*, *Viðskiptavinur* eða *Vara*).
    - **Bókun** – Veljið gerð bókanna sem á að stofna (svo sem *Miðlaragjald* eða *Jöfnun viðskiptavinar*).
    - **Reikningur** - Veljið lykilinn sem bóka á gjaldið fyrir.

1. Í aðgerðarúðunni skal velja **Vista**.

## <a name="create-charge-groups"></a>Stofna gjaldaflokka

Gjaldaflokkar úthluta sjálfkrafa tilteknum gjöldum til viðskiptavina- eða lánardrottnaflokks. Eftirfarandi hlutar útskýra hvernig á að stofna og úthluta þessum gjaldaflokkum.

### <a name="charge-groups-for-purchase-orders"></a>Gjaldaflokkar fyrir innkaupapantanir

Til að stofna gjaldaflokka fyrir innkaupapantanir skal fylgja þessum skrefum.

1. Farið í **Viðskiptaskuldir \> Uppsetning gjalda \> Gjaldaflokkur lánardrottins**.
1. Á aðgerðasvæðinu skal velja **Ný** til að bæta línu við hnitanetið og síðan stilla eftirfarandi reiti:

    - **Gjaldaflokkur** - Færið inn heiti gjaldaflokksins.
    - **Lýsing** - Færið inn lýsingu á gjaldaflokknum.

1. Í aðgerðarúðunni skal velja **Vista**.
1. Farið í **Viðskiptaskuldir \> Lánardrottnar \> Allir lánardrottnar** og annaðhvort opnið fyrirliggjandi lánardrottin eða stofnið nýjan lánardrottin.
1. Í flýtiflipanum **Sjálfgildi innkaupapöntunar**, í hlutanum **Innkaupapöntun**, skal stilla reitinn **Gjaldaflokkur** á gjaldaflokkinn sem var stofnaður rétt í þessu.

### <a name="charge-groups-for-sales-orders"></a>Gjaldaflokkar fyrir sölupantanir

Til að stofna gjaldaflokka fyrir sölupantanir skal fylgja þessum skrefum.

1. Farið í **Viðskiptakröfur \> Uppsetning gjalda \> Gjaldaflokkar viðskiptavinar**.
1. Á aðgerðasvæðinu skal velja **Ný** til að bæta línu við hnitanetið og síðan stilla eftirfarandi reiti:

    - **Gjaldaflokkur** - Færið inn heiti gjaldaflokksins.
    - **Lýsing** - Færið inn lýsingu á gjaldaflokknum.

1. Í aðgerðarúðunni skal velja **Vista**.
1. Farið í **Viðskiptakröfur \> Viðskiptavinir \> Allir viðskiptavinir** og annaðhvort opnið fyrirliggjandi viðskiptavin eða stofnið nýjan viðskiptavin.
1. Í flýtiflipanum **Sjálfgildi innkaupapöntunar**, í hlutanum **Sölupöntun**, skal stilla reitinn **Gjaldaflokkur** á gjaldaflokkinn sem var stofnaður rétt í þessu.

## <a name="define-auto-charges"></a>Skilgreina sjálfvirk gjöld

Eftir að gjaldakóðar eru settir upp skal fylgja þessum skrefum til að skilgreina sjálfvirk gjöld.

1. Fylgið einu af eftirfarandi skrefum:

    - Fyrir innkaupapantanir: Farið í **Innkaup og aðföng \> Uppsetning \> Gjöld \> Sjálfvirk gjöld**.
    - Fyrir sölupantanir: Farið í **Viðskiptakröfur \> Uppsetning \> Uppsetning gjalda \> Sjálfvirk gjöld**.

1. Í listasvæðinu, í reitnum **Stig**, skal velja stigið þar sem á að nota sjálfvirkt gjald:

    - *Aðal* - Færa gjöld á pöntunarhaus.
    - *Lína* - Færa gjöld á pöntunarlínur.

1. Veljið fyrirliggjandi sjálfvirkt gjald til að breyta því eða veljið **Nýtt** til að skilgreina nýtt sjálfvirkt gjald.
1. Í listanum **Lykilkóði** skal velja eitt af eftirfarandi gildum til að tilgreina umfang lykla sem verða fyrir áhrifum:

    - *Tafla* - Færa gjöld á tiltekinn viðskiptavin eða lánardrottinn.
    - *Hópur* - Úthluta gjöld á mismunandi gjaldaflokk.
    - *Allt* - Færa gjöld á alla viðskiptavini eða lánardrottna.

1. Í reitnum **Tengsl viðskiptavinar** eða **Tengsl lánardrottins** skal velja tiltekinn viðskiptavin eða lánardrottin ef reiturinn **Lykilkóði** er stilltur á *Tafla*. Ef reiturinn **Lykilkóði** er stilltur á *Flokkur* skal velja gjaldaflokk viðskiptavinar eða lánardrottins.
1. Í listanum **Vörukóði** skal velja eitt af eftirfarandi gildum til að tilgreina umfang varanna sem verða fyrir áhrifum. Hægt er að velja vörukóða þegar skilgreina á sjálfvirk gjöld á línustigi.

    - *Tafla* - Færa gjöld á tiltekna vöru.
    - *Hópur* - úthluta gjöld á gjaldaflokk vöru.
    - *Allar* - Úthluta gjaldi á allar vörur.

1. Í reitnum **Vöruvensl** skal velja tiltekna vöru ef reiturinn **Vörukóði** er stilltur á *Tafla*. Ef reiturinn **Vörukóði** er stilltur á *Flokkur* skal velja gjaldaflokk vöru.
1. **Aðeins fyrir sölupantanir:** Í reitnum **Kóði afhendingarmáta** skal velja eitt af eftirfarandi gildum til að tilgreina umfang afhendingamáta sem verða fyrir áhrifum:

    - *Tafla* - Velja gjöld til tiltekins afhendingarmáta.
    - *Hópur* - Velja gjöld til afhendingarmáta hóps.
    - *Allt* - Færa gjöld á allar tegundir afhendingu.

1. **Aðeins fyrir sölupantanir:** Í reitnum **Tengsl afhendingarmáta** skal velja tiltekinn afhendingarmáta ef reiturinn **Kóði afhendingarmáta** er stilltur á *Tafla*. Ef reiturinn **Kóði afhendingarmáta** er stilltur á *Flokkur* skal velja flokk afhendingarmáta.
1. Í flýtiflipanum **Línur** skal skilgreina gjöldin og taxta þeirra sem verður notað þegar núverandi sjálfvirkt gjald er notað. Hægt er að nota tækjastikuna í þessum flýtiflipa til að bæta við eins mörgum línum og þörf er á. Fyrir hverja línu skal stilla eftirfarandi reiti:

    - **Gjaldmiðill** – Veljið gjaldmiðilinn sem á að nota til að reikna út gjöldin.
    - **Gjaldakóði** - Veljið kóða fyrir gjaldið.
    - **Flokkur** - Veljið eitt af eftirfarandi gildum:

        - *Fast* - Gjaldið er fært sem föst upphæð á línu. Hægt er að nota föst gjöld á gjöld bæði í pöntunarhaus og pöntunarlínum.
        - *Stk* - Gjaldið er byggt á einingunni. Hægt er að nota þessi gjöld einungis á pöntunarlínur. Þau birtast þegar samtala pöntunar er reiknuð.
        - *Prósenta* - Gjaldið er fært upp sem hundraðshluti á línu. Hægt er að nota prósentugjöld á gjöld í bæði pöntunarhaus og pöntunarlínum.
        - *Prósenta innan samstæðu* - Gjaldið er fært inn sem prósenta í línuna fyrir pantanir innan samstæðu. Hægt er að nota prósentugjöld innan samstæðu einungis í pöntunarlínum.
        - *Ytri* - Gjaldið er reiknað með þjónustu þriðja aðila sem tengist einum eða fleiri farmflytjanda.

    - **Gildi gjalds** – Sláið inn gildi gjaldsins, byggt á flokknum sem var valinn.
    - **Gjaldmiðilskóði gjalda** - Tilgreinið gjaldmiðil fyrir gjaldið ef á að nota annan gjaldmiðil en þann sem tilgreindur er í reitnum **Gjaldmiðill**. Aðeins er hægt að nota annan gjaldmiðil ef reiturinn **Debetgerð** eða **Kreditgerð** er stilltur á annaðhvort *Fjárhagslykil* eða *Vöru* fyrir valinn gjaldakóða.
    - **Frá upphæð** - Tilgreinið byrjunarupphæð þar sem á að nota gjaldið. Upphæð í þessu samhengi á við um samtölu pöntunar.
    - **Til upphæð** - Tilgreinið lokaupphæð þar sem á að nota gjaldið. Upphæð í þessu samhengi á við um samtölu pöntunar.
    - **VSK-flokkur** - Tilgreinið VSK-flokk.
    - **Svæði** og **Vöruhús** – Tilgreinið svæði og vöruhús ef aðeins á að nota gjöld fyrir tiltekið svæði og vörhús.
    - **Halda** - Veljið þennan gátreit til að halda færslugjöldunum eftir að reikningsfærslu er lokið, svo að gjaldið verið notað í hvert skipti sem nýr reikningur er stofnaður fyrir valinn viðskiptavinalykil.

1. **Aðeins fyrir sölupantanir:** Ef á að reikna út stigskipt gjöld skal skoða [Stigskipt gjöld í sölupöntunum](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/about-tiered-charges-on-sales-orders) til að fá upplýsingar.

## <a name="allocate-charges-from-the-header-to-a-line"></a>Úthluta gjöldum úr hausnum í línu

Eftirfarandi ferli sýnir hvernig á að úthluta gjöldum hausastigs á línu. Áður en þetta ferli er hafið ætti þegar að vera til staðar gjald hausastigs fyrir gerðina *föst upphæð* og pöntun þar sem þetta gjald er notað. Þar að auki ætti pöntunin nú þegar að innihalda að minnsta kosti eina vörulínu.

1. Opnið innkaupapöntun eða gjaldapöntun.
1. Á aðgerðasvæðinu skal fylgja einu af þessum skrefum:

    - Fyrir innkaupapantanir: Í flipanum **Innkaup**, í flokknum **Gjald**, skal velja **Úthluta gjöldum**.
    - Fyrir sölupantanir: Í flipanum **Selja**, í flokknum **Gjald**, skal velja **Úthluta gjöldum**.

1. Í svarglugganum **Úthluta gjöldum á pöntunarlínur** skal stilla eftirfarandi reiti:

    - **Úthlutun gjalda** - Veljið eitt af eftirfarandi gildum til að tilgreina hvernig skuli úthluta gjöldunum:

        - *Nettóupphæð* – Úthlutið gjöldum samkvæmt hverri línuupphæð í hlutfalli við heildarnettóupphæðina.
        - *Magn* – Úthlutið gjöldum samkvæmt fjölda eininga fyrir hverja línu í hlutfalli við heildarfjölda eininga.
        - *Á línu* - Úthlutið gjöldum jafnt á heildarfjölda lína.

    - **Úthluta gjöldum á línur** – Veljið gildi til að tilgreina hvort eigi að úthluta gjöldum á allar línur, aðeins jákvæðar línur eða aðeins neikvæðar línur.
    - **Úthluta öllu** - Veljið þennan gátreit til að úthluta gjöldum á pöntunarlínur, jafnvel þótt gjaldakóðinn hafi debetgerð aðra en *Vara*.
    - **Móttekið** - Veljið þennan gátreit til að úthluta aðeins gjöldum á mótteknar pöntunarlínur.
    - **Á lager** - Veljið þennan gátreit til að úthluta gjöldum aðeins á birgðaskráðar pöntunarlínur.
    - **Sýna val og hreinsa tilteknar línur** - Veljið þennan gátreit til að útiloka tilteknar línur frá þessari úthlutun. Þegar þessi gátreitur er valinn opnast hnitanetið **Velja línur sem á að sleppa úr úthlutun**. Þetta hnitanet inniheldur aðeins línur sem samsvara skilyrðunum sem eru skilgreind af stillingunum **Úthluta gjöldum á línur** og **Á lager**. Til dæmis ef reiturinn **Úthluta gjöldum á línur** er stilltur á *Jákvæðar línur* og gátreiturinn **Á lager** er valinn, sýnir hnitanetið aðeins línur sem eru bæði jákvæðar og með birgðir. Að auki síar hnitanetið sjálfkrafa út allar línurnar þar sem allt magnið hefur þegar verið móttekið fyrir. Á meðan hnitanetið er opið skal hreinsa gátreitinn **Hafa með** fyrir hverja línu sem á útiloka frá úthlutun. 

        > [!IMPORTANT]
        > Þegar unnið er með hnitanetið **Velja línur sem á að sleppa úr úthlutun** skal ganga úr skugga um að skilja hnitanetið eftir opið þar til **Úthluta** er valið. Ef hnitanetinu er lokað áður en valið er **Úthluta** tapast stillingarnar í hnitanetinu. Gjöldum verður þar af leiðandi úthlutað samkvæmt skilyrðinu sem var skilgreint hér áður.

1. Vejið **Úthluta** til að nota stillingarnar og loka gátreitnum.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]