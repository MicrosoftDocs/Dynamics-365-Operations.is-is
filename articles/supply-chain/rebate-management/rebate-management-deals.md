---
title: Tilboð fyrir stjórnun eftirágreidds afsláttar
description: Þessi grein lýsir því hvernig á að búa til afsláttarstjórnunarsamninga. Tilboð eru notuð til að stjórna mismunandi aðferðum og grunnum til að reikna út eftirágreiddan afslátt og afnotagreiðslur. Þau fela í sér reglur um það sem er innifalið og ekki innifalið.
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
ms.openlocfilehash: 28cfff69ab4e528c146ccbf6a34548a819c99522
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8851595"
---
# <a name="rebate-management-deals"></a>Tilboð fyrir stjórnun eftirágreidds afsláttar

[!include [banner](../includes/banner.md)]

Tilboð vegna stjórnunar eftirágreidds afsláttar eru notuð til að stjórna mismunandi aðferðum og grunnum til að reikna út eftirágreiddan afslátt og afnotagreiðslur. Þau fela í sér reglur um það sem er innifalið og ekki innifalið. Til eru þrjár gerðir tilboða fyrir stjórnun eftirágreidds afsláttar: eftirágreiddir afslættir viðskiptavinar, afnotagreiðslur viðskiptavinar og eftirágreiddir afslættir lánardrottins. Allar þrjár gerðirnar nota svipaðar stillingar. Þessi grein bendir á mun þar sem hann er til staðar.

## <a name="create-a-deal"></a>Stofna tilboð

1. Farið í **Stjórnun eftirágreidds afsláttar \> Tilboð fyrir stjórnun eftirágreidds afsláttar \> Öll tilboð fyrir stjórnun eftirágreidds afsláttar**. Á listasíðunni **Öll tilboð fyrir stjórnun eftirágreidds afsláttar** er hægt að stofna og vinna með tilboð fyrir allar þrjár gerðirnar.

    Einnig er hægt að fylgja einu af eftirfarandi skrefum. Í hverju tilfelli býður listasíðan sem birtist upp á sömu stillingarnar og listasíðan **Öll tilboð fyrir stjórnun eftirágreidds afsláttar**, en hún er síuð til að sýna tilboð af aðeins einni gerð.

    - Farið í **Stjórnun eftirágreidds afsláttar \> Tilboð fyrir stjórnun eftirágreidds afsláttar \> Tilboð vegna eftirágreidds afsláttar viðskiptavinar** til að stofna aðeins tilboð vegna eftirágreidds afsláttar viðskiptavinar.
    - Farið í **Stjórnun eftirágreidds afsláttar \> Tilboð fyrir stjórnun eftirágreidds afsláttar \> Tilboð vegna afnotagreiðslu viðskiptavinar** til að stofna aðeins tilboð vegna afnotagreiðslu viðskiptavinar.
    - Farið í **Stjórnun eftirágreidds afsláttar \> Tilboð fyrir stjórnun eftirágreidds afsláttar \> Tilboð vegna eftirágreidds afsláttar lánardrottins** til að stofna aðeins tilboð vegna eftirágreidds afsláttar lánardrottins.

1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Í svarglugganum **Stofna nýtt tilboð** skal stilla eftirfarandi reiti:

    - **Tilboð fyrir stjórnun eftirágreidds afsláttar** – Ef búið er að [setja upp númeraröð](rebate-management-parameters.md) fyrir tilboð eftirágreidds afsláttar verður þessi reitur sjálfkrafa stilltur á einkvæmt kenni sem kerfið myndar. Annars skal færa inn einkvæmt kenni.
    - **Lýsing** – Færið inn lýsingu á tilboðinu.
    - **Eining** – Veljið gerð samstarfsaðila sem tilboðið gildir fyrir (*Viðskiptavinur* eða *Lánardrottinn*). Það fer eftir síðunni sem byrjað var á hvort þessi reitur sé sjálfkrafa stilltur samkvæmt valinni gerð tilboðs. Í þessu tilviki er reiturinn ritvarinn.
    - **Gerð** – Veljið gerð tilboðs (*Eftirágreiddur afsláttur* eða *Afnotagreiðsla*). Það fer eftir síðunni sem byrjað var á hvort þessi reitur sé sjálfkrafa stilltur samkvæmt valinni gerð tilboðs. Í þessu tilviki er reiturinn ritvarinn.
    - **Afstemma eftir** – Veljið hvernig tilboðið er reiknað og afstemmt:

        - *Tilboð* – Vinna skal úr einum eftirágreiddum afslætti fyrir alla eftirágreidda afslætti og frádrætti í tilboðinu.
        - *Lína* – Vinna skal úr eftirágreiddum afsláttum fyrir hverja línu í tilboði.

    - **Bókunarregla** – Veljið [bókunarregluna](rebate-management-posting.md) sem á að nota fyrir færslur þar sem tilboðið gildir. Þessi reitur er aðeins í boði þegar reiturinn **Afstemma eftir** er stilltur á *Tilboð*. Ef hann er stilltur á *Lína* verður reglunni úthlutað síðar fyrir hverja línu sem bætt er við tilboðið.
    - **Bókunarregla fyrir tryggingu** – Veljið [Bókunarregla](rebate-management-posting.md) sem á að nota fyrir tryggðar færslur. Bókunarreglur eru aðeins nauðsynlegar fyrir tryggðar færslur ef tryggingin á við um afnotagreiðslu. Annars, þótt bókunarregla sé ekki áskilin, ef engin bókunarregla er tilgreind, kemur upp villa þegar tryggingar eru bókaðar. Þessi reitur er aðeins í boði þegar reiturinn **Gerð** er stilltur á *Afnotagreiðsla*. 
    - **Úttak eftirágreidds afsláttar** – Veljið hvernig greiða á eftirágreiddan afslátt eða afnotagreiðslu:

        - *Fjárhagslegt* – Búið til kreditnótu með frjálsum texta eða debetnótu viðskiptaskulda svo hægt sé að greiða eða fá greitt síðar. Athugið að **hægt** er að nota ákvæði með eftirágreiddum afsláttum þar sem þessi valkostur er valinn. Þessi valkostur er eini valkosturinn sem er tiltækur þegar reiturinn **Gerð** er stilltur á *Afnotagreiðslu*.
        - *Vara* – Búið til sölupöntun fyrir vörur samkvæmt uppsetningu tilboðsins. Í þessari sölupöntun er verðið 0 (núll) úthlutað hverri vöru. Athugið að **ekki er hægt** að nota ákvæði með eftirágreiddum afsláttum þar sem þessi valkostur er valinn.

    - **Gjaldmiðill eftirágreidds afsláttar** – Veljið gjaldmiðilinn sem á að nota þegar eftirágreiddur afsláttur, frádráttur eða afnotagreiðsla er greidd.
    - **Athugasemdir skjals** – Færið inn athugasemdir um tilboðið eftir þörfum.
    - **Uppsöfnuð trygging** - Þennan valkost er aðeins hægt að stilla á *Já* ef reiturinn **Gerð** er stilltur á *Afnotagreiðslu*. Þessi valkostur hefur áhrif á útreikning tryggðra frádráttarfærslna. Eftirfarandi er dæmi:

        - Tilboðið tryggir söluandvirði sem leiðir til greiðslu upp á $10.000 ársfjórðungslega.
        - Fyrirtækið sem selur vörurnar selur virði sem veldur því að greiðsla upp á $12.000 í ársfjórðungi 1 er dregin frá. Útkoman er $12.000 afnotagreiðsla sem er greidd að frádeginni tryggingu upp á $10.000.
        - Ef valkosturinn **Uppsöfnuð trygging** er stilltur á *Já* gildir viðbótin upp á $2000 fyrir afnotagreiðslu sem greidd var á ársfjórðungi 1 um ársfjórðung 2. Þar af leiðandi er viðskiptavininum tryggðar $8000 ($10.000 trygging að frádreginni $2000 viðbótargreiðslu).
        - Í ársfjórðungi 2 skal skrá sölu sem kveikir á $5000 afnotagreiðslu.
        - Kerfið auðkennir $3000 greiðslu ($8000 trygging mínus $5000 fyrir greiddar afnotagreiðslur).
        - Ef valkosturinn **Uppsöfnuð trygging** er stilltur á *Nei* eru öll $10.000 upphæðin tryggð ársfjórðungslega. Þessi trygging er í samræmi við tillögu um greiðslu upp á $5000 á ársfjórðungi 2 ($10.000 tryggt að frádeginni $5000 afnotagreiðslu).

1. Veljið **Í lagi** til að stofna tilboðið og loka svarglugganum.

Þetta ferli býr til hausstig nýja tilboðsins. Næst á að bæta línum við tilboðið.

## <a name="add-lines-to-a-deal"></a>Bæta línum við tilboð

Þegar tilboð hefur verið stofnað eins og lýst er í fyrri hlutanum er hægt að opna það á listasíðunni. Þá er hægt að bæta við línum til að gera grein fyrir viðskiptavinum eða lánardrottnum, vörum, tímarömmum, grundvallaratriðum og útreikningsaðferðum tilboðsins. Tilboð getur verið með eina eða fleiri línur. Ef tilboð er með mörgum línum eru þær yfirleitt af sömu gerðinni eða sömu færibreytur tengjast þeim. Tilboðið gerir ekkert fyrr en línum hefur verið bætt við það.

1. Opnið viðeigandi listasíðu fyrir tilboð eftirágreidds afsláttar eins og lýst var í fyrri hlutanum.
1. Finnið og opnið tilboðið sem á að vinna með.
1. Í flýtiflipanum **Stjórnun eftirágreidds afsláttar** skal velja einn af eftirfarandi hnöppum til að bæta tilboðslínu við hnitanetið:

    - **Bæta við línu** – Bætið við nýrri auðri tilboðslínu.
    - **AFrita línu** – Ef fyrirliggjandi lína tilboðs líkist tilboðslínunni sem ætlunin er að bæta við er hægt að velja þennan hnapp til að bæta við afriti af henni. Nýja tilboðslínan mun innihalda allar stillingar úr upplýsingum tilheyrandi stjórnunar eftirágreidds afsláttar. Síðan er hægt að breyta stillingunum. Yfirleitt skal uppfæra vöruvenslin og prósentu eftirágreidds afsláttar.

1. Í nýju tilboðslínunni skal stilla eftirfarandi reiti:

    - **Tilboð fyrir stjórnun eftirágreidds afsláttar** – Ef búið er að [setja upp númeraröð](rebate-management-parameters.md) fyrir númer stjórnunar eftirágreidds afsláttar verður þessi reitur sjálfkrafa stilltur á einkvæmt kenni sem kerfið myndar. Annars skal færa inn einkvæmt kenni.
    - **Gerð**– Tilboðsgerðin sem línan gildir fyrir (*Eftirágreiddur afsláttur* eða *Afnotagreiðsla*). Gildið er afritað úr hausnum og er ekki hægt að breyta því.
    - **Lýsing**– Færið inn lýsingu á línu tilboðsins.
    - **Fyrirtæki**– Veljið fyrirtækið (lögaðilann) sem tilboðslínan á við um. Við vinnslu geta notendur aðeins unnið úr tilboðslínum sem fyrirtækinu er úthlutað sem verið er að vinna í á þeirri stundu. Listasíðan **Tilboð eftirágreidds afsláttar fyrir viðskiptavini** býður upp á yfirlit yfir mörg fyrirtæki samkvæmt öryggisaðgangi notandans. Hins vegar er aðeins hægt að breyta og vinna úr eftirágreiddum afsláttum fyrir fyrirtækið sem er notað á þeirri stundu.
    - **Reikningskóði** – Veljið umfang viðskiptavina eða lánardrottna sem tilboðslínan á við um:

        - *Tafla* – Tilboðslínan á við um tiltekinn viðskiptavin eða lánardrottin.
        - *Hópur*– Tilboðslínan á við um hóp viðskiptavina eða lánardrottna. Frekari upplýsingar um hvernig á að setja upp hópa er að finna í [Hópar fyrir stjórnun eftirágreidds afsláttar](rebate-management-groups.md).
        - *Allir* – Tilboðslínan gildir fyrir alla viðskiptavini eða lánardrottna.

    - **Lyklavens** – Ef valið var *Tafla* í reitnum **Kóði lykils** skal velja viðskiptavininn eða lánardrottin sem tilboðið gildir fyrir. Ef valið var *Hópur* skal velja hóp viðskiptavina eða lánardrottna. Ef valið var *Allt* verður þessi reitur ekki tiltækur.
    - **Vörukóði** – Veljið umfang varanna sem tilboðslínan á við um:

        - *Tafla*– Tilboðslínan á við um tiltekna vöru.
        - *Hópur* – Tilboðslínan á við um hóp af vörum. Frekari upplýsingar um hvernig á að setja upp hópa er að finna í [Hópar fyrir stjórnun eftirágreidds afsláttar](rebate-management-groups.md).
        - *Allt* – Tilboðslínan á við um allar vörur.

    - **Vöruvensl** Ef valið var *Tafla* í reitnum **Vörukóði** skal velja vöruna sem tilboðslínan á við um. Ef valið var *Hópur* skal velja vöruhópinn. Ef valið var *Allt* verður þessi reitur ekki tiltækur.
    - **Tegund einingar** – Veldu tegund einingar sem á við um vörulínuna (*Birgðaeining* eða *Þyngd afurðar, eining*). Athugið að þessi reitur gæti verið auður fyrir eldri færslur. Í þessu tilfelli er gert ráð fyrir *Birgðaeining*.
    - **(Færibreytur birgðastjórnunar)** – Í reitunum sem eftir eru í tilboðslínunni skal tilgreina gildi fyrir færibreytur birgðastjórnunar sem verða notaðar til að skilgreina vörurnar sem hafðar eru með í tilboðinu (t.d. vörustærð, lit, stíl, svæði og vöruhús). Til að bæta við eða fjarlægja víddirnar skal velja **Birta víddir** á aðgerðasvæðinu.

1. Í aðgerðarúðunni skal velja **Vista**.
1. Ef ætlunin er að takmarka enn frekar vörusafnið sem tilboðslína á að gilda um skal velja línuna og síðan í flýtiflipanum **Stjórnun eftirágreidds afsláttar** skal velja **Sía** til að opna hefðbundna svargluggann **Fyrirspurn**.
1. Fyrir hverja tilboðslínu sem bætt er við skal setja upp upplýsingar um útreikning og aðrar upplýsingar í flýtiflipann **Upplýsingar um stjórnun eftirágreidds afsláttar** eins og lýst er í næsta hluta.

## <a name="add-rebate-management-details-to-a-deal-line"></a>Bæta upplýsingum um stjórnun eftirágreidds afsláttar við tilboðslínu

Fyrir hverja línu í tilboðinu þarf að setja upp upplýsingar í flýtiflipann **Upplýsingar um stjórnun eftirágreidds afsláttar**. Fyrst skal velja tilboðslínuna í flýtiflipanum **Stjórnun eftirágreidds afsláttar**. Síðan skal stilla gildi fyrir þá tilboðslínu með því að nota hina ýmsu flipa í flýtiflipanum **Upplýsingar um stjórnun eftirágreidds afsláttar**. Eftirfarandi undirkaflar lýsa því hvernig á að nota hvern flipa fyrir sig.

### <a name="settings-on-the-general-tab"></a>Stillingar á flipanum Almennt

Flipinn **Almennt** í flýtiflipanum **Upplýsingar um stjórnun eftirágreidds afsláttar** gerir kleift að setja upp útreikningsaðferðina og grundvallaratriðin fyrir valda tilboðslínu. Þessi uppsetning stjórnar því hvort lágmarksinnkaup eru áskilin, bókunarreglurnar sem tengjast tilboðslínunni og upplýsingar um útreikninginn. Eftirfarandi tafla lýsir svæðum sem eru tiltæk.

| Svæði | lýsing |
|---|---|
| Útreikningsaðferð | Veljið aðferðina sem á að nota þegar valin tilboðslína er sameinuð við aðrar tilboðslínur (*Þrepaskipt*, *Uppsafnað*, *Hlaupandi* eða *Samtala*). Gildið í þessum reit getur haft umtalsverð áhrif á niðurstöðu útreikninga eftirágreidds afsláttar. Sjá ítarlega lýsingu á hverri aðferð og dæmi sem sýna hvernig hún hefur áhrif á afsláttarútreikninginn [Útreikningsaðferðir fyrir viðskiptalínur](#calc-methods) kafla síðar í þessari grein. |
| Grunnur | Veljið hvort eftirágreiddur afsláttur sé notaður miðað við magn (þ.e. heildarfjölda eininga sem eru keyptar eða seldar) eða virði (þ.e. heildarverð varanna sem eru keyptar eða seldar). |
| Færslugerð | <p>Veljið hvenær í ferlinu útreikningurinn á að eiga sér stað:</p><ul><li>*Pöntun* – Notið pantað magn eða virði sem grundvöll útreiknings.</li><li>*Afhent* – Notið afhent magn eða virði sem grundvöll útreiknings.</li><li>*Reikningur* – Notið reikningsfært magn eða virði sem grundvöll útreiknings.</li></ul> |
| Eining | Ef valið var *Magn* í reitnum **Grunnur** skal velja eininguna sem magnið á að vera í. |
| Lágmarksupphæð | Sláið inn lágmarksupphæð sem þarf að greiða fyrir hvert tímabil. Hægt er að færa inn neikvætt gildi til að leyfa neikvæðar upphæðir eftirágreidds afsláttar ef kreditnótur fara umfram sölu fyrir tímabilið. |
| Minnkunarregla eftirágreidds afsláttar | Veljið [minnkunarreglu eftirágreidds afsláttar](rebate-reduction-principle.md) sem gildir um tilboðslínuna. |
| Númer vöruvíddasamsetningar | Ef tilboðslínan á við um vöru sem er með afbrigði skal velja afbrigðið sem tilboðslínan á við um. |
| Grunnur fyrir eftirágreiddan afslátt lánardrottins | <p>Þessi reitur er aðeins sýndur fyrir eftirágreiddan afslátt lánardrottins (þ.e. tilboð þar sem reiturinn **Eining** er stilltur á *Lánardrottinn*). Veljið grunninn fyrir eftirágreiddan afslátt lánardrottins:</p><ul><li>*Innkaupapöntun* – Eftirágreiddur afsláttur sem lánardrottinn fær byggist á magni eða virði í innkaupapöntuninni.</li><li>*Sölupöntun* – Lánardrottinn fær eftirágreiddan afslátt eingöngu eftir að vörurnar hafa verið seldar. Eftirágreiddur afsláttur fer eftir magni eða virði sölupöntunarinnar.</li></ul> |
| Verðgrunnur | <p>Þessi reitur er aðeins sýndur fyrir eftirágreiddan afslátt lánardrottins (tilboð þar sem reiturinn **Eining** er stilltur á *Lánardrottinn*). Ef valið var *Sölupöntun* í reitnum **Grunnur fyrir eftirágreiddan afslátt lánardrottins** skal velja viðeigandi verðgrunn:</p><ul><li><p>*FIFO* – Keyra þarf reglubundna verkið **Reikna út innkaupaverð samkvæmt FIFO** til að reikna eftirágreiddan afslátt. (Til að keyra verkið skal fara í **Stjórnun eftirágreidds afsláttar \> Reglubundin verk \> Reikna út innkaupaverð samkvæmt FIFO**.) FIFO-regla (fyrst inn, fyrst út) verður notuð til að reikna út virði birgða sem eru seldar. Þetta virði verður síðan notað til að reikna út eftirágreiddan afslátt lánardrottins. Eftirfarandi er dæmi:</p><ul><li>**Seldar birgðir:** 1.000 einingar á $3,00 hver = $3.000</li><li>**Núverandi innkaupsverð, samkvæmt FIFO:** $2,00</li><li>**Vinnuútreikningur:** *Seldar einingar* × *Núverandi innkaupaverð* = 1.000 × $2,00 = $2.000</li></ul></li><li><p>*Síðasta innkaupaverð* – Virði síðustu innkaupafærslu verður notað til að reikna út eftirágreiddan afslátt lánardrottins. Eftirfarandi er dæmi:</p><ul><li>**Seldar birgðir:** 1.000 einingar á $3,00 hver = $3.000</li><li>**Síðasta innkaupsverð:** $2,00</li><li>**Vinnuútreikningur:** *Seldar einingar* × *Síðasta innkaupaverð* = 1.000 × $2,00 = $2.000</li></ul></li><li><p>*Meðaltal innkaupsverðs* – Vegið meðaltalsvirði fyrir síðustu *X* mánuði verða notaðir til að reikna út eftirágreiddan afslátt lánardrottins. Ef þessi valkostur er valinn þarf að færa inn fjölda mánaða í reitinn **Fjöldi mánaða** (sem er aðeins tiltækur þegar reiturinn **Verðgrunnur** er stilltur á *Innkaupsverð að meðaltali*). Eftirfarandi er dæmi:</p><ul><li>**Seldar birgðir:** 1.000 einingar á $3,00 hver = $3.000</li><li>**Meðaltal innkaupsverðs:** $2,00</li><li>**Vinnuútreikningur:** *Seldar einingar* × *Meðatal innkaupaverðs* = 1.000 × $2,00 = $2.000</li></ul></li><li><p>*Söluverð* – Söluverðið verður notað til að reikna út eftirágreidda afslætti lánardrottins. Eftirfarandi er dæmi:</p><ul><li>**Seldar birgðir:** 1.000 einingar á $3,00 hver = $3.000</li><li>**Meðaltal innkaupsverðs:** $2,00</li><li>**Vinnuútreikningur:** *Seldar einingar* × *Söluverð* = 1.000 × $3,00 = $3.000</li></ul></li></ul> |
| Fjöldi mánaða | Þessi reitur er aðeins sýndur fyrir eftirágreiddan afslátt lánardrottins (tilboð þar sem reiturinn **Eining** er stilltur á *Lánardrottinn*). Ef valið var *Innkaupsverð að meðaltali* í reitnum **Verðgrunnur** skal slá inn fjölda mánaða sem á að nota. |
| Bókunarregla | Veljið [bókunarregluna](rebate-management-posting.md) sem gildir um völdu tilboðslínuna. Þessi regla er aðeins notuð þegar reiturinn **Afstemma eftir** í haus tilboðsins er stilltur á *Lína*. Ef reiturinn **Afstemma eftir** er stilltur á *Tilboð* verður bókunarreglan sem stillt er í haus tilboðsins alltaf notuð. Ef engin bókunarregla er stillt í tilboðslínunni verður bókunarreglan sem stillt er í haus tilboðsins notuð. |
| Bókunarregla fyrir tryggingu | Þessi reitur virkar eins og reiturinn **Bókunarregla** en hann á aðeins við um afnotagreiðslur. |
| Greiðslugerð | Greiðslugerð bókunarreglunnar sem er valin fyrir tilboðið. |
| Virðisaukaskattur innifalinn | Veljið hvort færslan feli í sér skatt. Innifalinn skattur á aðeins við þegar reiturinn **Grunnur** er stilltur á *Virði*. Reikningsupphæðin verður notuð sem upphæð með skatti. Ef útreikningur eftirágreidds afsláttar byggir á prósentu mun kerfið margfalda prósentu eftirágreidds afsláttar við upphæð með skatti. Athugið að útreikningurinn notar gildi virðisaukaskatts úr tilboðslínunni. |
| Hafa kreditnótur með | <p>Stillið þennan valkost á *Já* til að hafa með kreditnótur í útreikningi eftirágreidds afsláttar.</p><p>Ef þessi valkostur er stilltur á *Já* eru áhrifin breytileg eftir því hvert gildið er í reitnum **Færslugerð**:</p><ul><li>Ef reiturinn **Færslugerð** er stilltur á *Reikningur* mun útreikningurinn taka með kreditnótur. Þessi skilgreining er venjulega skilgreiningin.</li><li>Ef reiturinn **Færslugerð** er stilltur á *Pöntun* mun útreikningurinn taka með bæði sölupantanir sem eru með neikvæð gildi og opnar skilapantanir.</li></ul> |
| Upphæð afsláttar | Til að stilla þennan valkost á *Já* til að byggja útreikninginn á upphæð með afslætti fyrir vöruna eða vörurnar í tilfellum þar sem línuafslættir tilboðs eru gefnir upp. |
| Aðeins greiddir reikningar | Stillið þennan valkost á *Já* ef útreikningur á aðeins að taka mið af reikningum sem hafa verið greiddir að fullu. (Þ.e. eftirágreiddir afslættir verða ekki reiknaðir fyrir reikninga sem eru greiddir að hluta til.) Þessi valkostur er aðeins í boði þegar reiturinn **Færslugerð** er stilltur á *Reikningur*. |
| hafa með frjálsan texta | Stillið þennan valkost á *Já* til að hafa reikninga með frjálsum texta með í útreikningnum. Aðeins er hægt að taka með reikninga með frjálsum texta fyrir tilboðslínur þar sem reiturinn **Vörukóði** er stilltur á *Allt*. |
| Taka með uppgjörsafslátt | Stillið þennan valkost á *Já* til að lækka eftirágreiddan afslátt um það sem nemur fyrsta uppgjörsafslættinum. Gert er ráð fyrir að fyrirtækið taki á sig fyrsta uppgjörsafsláttinn. Stillið þennan valkost á *Nei* til að gera kleift að nota uppgjörsafsláttinn síðar. |
| Athugasemdir skjals | Færið inn athugasemdir sem nota á sem færslutexta í færslubókarlínum eftirágreidds afsláttar. |

### <a name="settings-on-the-dates-tab"></a>Stillingar í dagsetningarflipanum

Stillingarnar í flipanum **Dagsetningar** í flýtiflipanum **Upplýsingar um stjórnun eftirágreidds afsláttar** skilgreina tíðni og tímasetningu útreikninga sem eru tilgreind í flipanum **Almennt**. Þau ákvarða hvernig útreikningar gerast á vinnslutíma.

Þessi flipi gerir kleift að tilgreina dagsetningabil þegar valin tilboðslína gildir og tíðni útreiknings. Einnig er hægt að tilgreina hvort og hvenær eigi að bóka trygginguna.

Hægt er að nota hnappana á tækjastikunni til að bæta dagsetningarlínum við hnitanetið eða fjarlægja þær. Ef margar dagsetningarlínur eru til staðar megar gild dagsetningabil ekki skarast. Annars koma upp villuboð þegar reynt er að vista tilboðið.

Eftirfarandi tafla lýsir eritinum sem eru tiltækir fyrir hverja dagsetningarlínu.

| Svæði | lýsing |
|---|---|
| Frá dagsetning | Sláðu inn fyrstu dagsetninguna sem dagsetningarlínan gildir fyrir. Ef „til“ og „frá“ dagsetningarnar eru tilgreindar í tilboðshausnum eru þær notaðar sem sjálfgefin gildi fyrir hverja nýja dagsetningarlínu. |
| Til dags. | Sláðu inn síðustu dagsetninguna sem dagsetningarlínan gildir fyrir. Ef „til“ og „frá“ dagsetningarnar eru tilgreindar í tilboðshausnum eru þær notaðar sem sjálfgefin gildi fyrir hverja nýja dagsetningarlínu. |
| Eftir | Tilgreinið hversu oft á að reikna út tilboðslínuna. Sláið inn heiltölu hér og veljið svo einingu í reitnum **Safna saman eftir**. Til dæmis til að reikna út aðra hverja viku skal stilla reitinn **Hverja** á *2* og reitinn **Safna saman eftir** á *Vikur*. |
| Safna saman eftir | Veljið eininguna sem gildir um stillinguna **Hverja**. Veljið *Líftíma* til að reikna yfir allan líftíma tilboðslínunnar. Veljið *Sérstillt tímabil* til að velja tímabil sem er skilgreint í fjárhagnum. Í þessu tilviki þarf einnig að stilla reitinn **Tímabilsgerð**. |
| Tímabilsgerð | Þessi reitur er aðeins í boði þegar reiturinn **Safna saman eftir** er stilltur á *Sérstillt tímabil*. Gildin sem eru í boði fyrir val koma úr tímabilsgerðunum sem eru skilgreind í fjárhagnum. |
| Fyrsti dagur vikunnar | Tilgreinið hvernig vikurnar eru auðkenndar fyrir tímabilið. Þessi reitur er aðeins í boði þegar reiturinn **Safna saman eftir** er stilltur á *Vikur*. |
| Gera kröfu eftir hverja | Tilgreinið hversu oft er hægt að gera kröfu um eftirágreiddan afslátt fyrir tilboðslínuna. Sláið inn heiltölu hér og veljið svo einingu í **Nota fyrir** reitnum. |
| Nota fyrir | Veljið eininguna sem gildir fyrir **Nota fyrir** stillinguna. Veljið *Líftíma* til að leyfa kröfur aðeins einu sinni yfir allan líftíma tilboðslínunnar. Veljið *Sérstillt tímabil* til að velja tímabil sem er skilgreint í fjárhagnum. Í þessu tilviki þarf einnig að stilla reitinn **Tímabilsgerð kröfu**. |
| Tímabilsgerð kröfu | Þessi reitur er aðeins í boði þegar reiturinn **Gera kröfu samkvæmt** er stilltur á *Sérstillt tímabil*. Gildin sem eru í boði fyrir val koma úr tímabilsgerðunum sem eru skilgreind í fjárhagnum. |
| Afgreiða við bókun | Veljið þennan gátreit ef afgreiða á kröfulínuna við bókun. Þessi valkostur er aðeins í boði fyrir tilboðslínur þar sem reiturinn **Færslugerð** í flipanum **Almennt** er stilltur á *Afhent* eða *Reikningsfæra*. Fyrir ákvæði verða ákvæðin bókuð þegar fylgiseðill eða reikningur er búinn til. |
| Trygging fyrir | Þessi reitur á aðeins við um tilboð afnotagreiðslna. Tilgreinið hversu oft á að reikna tryggingu afnotagreiðslu á tímabilinu sem er skilgreint með stillingunni **Safna saman eftir**. Sláið inn heiltölu hér og veljið svo greiðslutíma í reitnum **Trygging greidd**. |
| Trygging greidd | <p>Þessi reitur á aðeins við um tilboð afnotagreiðslna. Hann vinnur saman með reitnum **Trygging fyrir** til að skilgreina tíðni á útreikningi tryggingar. Veljið eitt af eftirfarandi gildum:</p><ul><li><p>*Upphaf tímabils* – Tryggingin er greidd við upphaf samningstímans sem er skilgreint fyrir dagsetningarlínuna. Fyrst er unnið úr allri tryggingunni. Aðeins virði afnotaréttar sem fer umfram tryggðrar upphæðar er bókað sem afnotagreiðsla. Eftirfarandi er dæmi:</p><ul><li>**Lágmarksgjald tryggingar:** $10.000 á tveggja mánaða tímabili.</li><li>**Mánuður 1:** $10.000 var bókað sem trygging og $0 bókað í afnotagreiðslur.</li><li>**Mánuður 2:** $2.000 var bókað í afnotagreiðslur og $0 bóka í tryggingu.</li><li>**Vinnuútreikningur:** *Eftirstandandi trygging* – *Bókaður afnotaréttur* = $0 – $2.000 = -$2.000.</li></ul><p>Þar sem krafist er afnotagreiðslu upp á $2000, er færslubók stofnuð fyrir $2000.</p><p>**Athugið:** Trygginguna á að reikna og bóka saman með ráðstöfun frádráttar fyrir fyrsta tímabilið.</p></li><li><p>*Lok tímabils* – Tryggingin er ekki greidd fyrr en við lokin á samkomulagi um frádrætti eins og það er skilgreint í dagsetningarlínunni. Eftirfarandi er dæmi:</p><ul><li>**Lágmarksgjald tryggingar:** $10.000 á tveggja mánaða tímabili.</li><li>**Mánuður 1:** $5.000 var bókað sem afnotagreiðsla og færslubók var stofnuð.</li><li>**Mánuður 2:** $7.000 var bókað sem afnotagreiðsla og færslubók var stofnuð.</li><li>**Vinnuútreikningur:** Þar sem afnotagreiðslan fór umfram upphæð tryggingar, verða $0 bókaðir fyrir trygginguna.</li></ul><p>**Athugið:** Trygginguna á að reikna og bóka saman með færslu frádráttar og eftirágreidds afsláttar fyrir lokatímabilið.</p></li></ul> |
| Lágmarkstrygging | Þessi reitur á aðeins við um tilboð afnotagreiðslna. Færið inn lágmarksupphæð tryggingarinnar fyrir afnotarétt í gjaldmiðlinum sem er skilgreindur í tilboðshausnum. |

### <a name="settings-on-the-lines-tab"></a>Stillingar á flipanum Línur

Flipinn **Línur** í flýtiflipanum **Upplýsingar um stjórnun eftirágreidds afsláttar** gerir kleift að skilgreina útreikningslínur fyrir valda tilboðslínu. Hver útreikningslína kemur með mörk fyrir magn eða virði og tengda upphæð uppbótar eða vörur. Reiturinn **Grunnur** í **Almennt** tilgreinir hvort hver útreikningslína byggi á magni eða virði.

Hægt er að nota hnappana á tækjastikunni til að bæta útreikningslínum við hnitanetið eða fjarlægja þær. Hægt er að hafa eins margar útreikningslínur og þörf er á. Ef margar útreikningslínur eru hins vegar til staðar má „til“ og „frá“ magn eða virði ekki skarast.

Eftirfarandi tafla lýsir eritinum sem eru tiltækir fyrir hverja útreikningslínu.

| Svæði | lýsing |
|---|---|
| Frá magn/virði | Sláið inn lágmarksmagn eða -virði sem á að gilda fyrir útreikningslínuna. |
| Til magn/virði | Sláið inn hámarksmagn eða -virði sem á að gilda fyrir útreikningslínuna. |
| Aðferð við stjórnun eftirágreidds afsláttar | <p>Þessi reitur er aðeins í boði fyrir tilboð þar sem reiturinn **Úttak eftirágreidds afsláttar** í hausnum er stilltur á *Fjárhagslegt*. Veljið aðferðina sem á að nota við útreikning eftirágreidds afsláttar:</p><ul><li>*Fast* – Föst verðupphæð er notuð fyrir línuna.</li><li>*Prósenta* – Prósenta af söluupphæðinni er notuð.</li><li>*Taxti* – Föst verðupphæð fyrir hverja pöntun er notuð.</li></ul><p>**Mikilvægt:** Við mælum eindregið með því að nota sömu aðferðina fyrir allar útreikningslínur í flipanum **Línur**. Ef ný aðferð er nauðsynleg skal búa til nýja tilboðslínu. Munið að hægt er að nota hnappinn **Afrita línu** í flýtiflipanum **Stjórnun eftirágreidds afsláttar** til að stofna nýja tilboðslínu út frá fyrirliggjandi tilboðslínu.</p><p>**Athugið:** Ef reiturinn **Úttak eftirágreidds afsláttar** er stilltur á *Vara* er þessi reitur alltaf stilltur á *Fast*. Frekari upplýsingar um hvernig á að tilgreina vörurnar er að finna í textanum sem kemur á eftir þessari töflu. |
| Upphæð fyrir stjórnun eftirágreidds afsláttar | Þessi er aðeins í boði fyrir tilboð þar sem **Úttak eftirágreidds afsláttar** í hausnum er stillt á *Fjárhagslegt*. Færið inn upphæðina sem á að nota til að reikna út eftirágreiddan afslátt samkvæmt aðferðinni sem var valin í reitnum **Aðferð við stjórnun eftirágreidds afsláttar**. |

Eins og var minnst á í fyrri töflu, fyrir tilboð þar sem reiturinn **Úttak eftirágreidds afsláttar** í hausnum er stilltur á *Vara*, þarf að tilgreina vörurnar sem verða gefnar upp fyrir hverja útreikningslínu í flipanum **Línur**. Til að tilgreina vörurnar skal fylgja þessum skrefum.

1. Í flipanum **Línur** skal stofna nauðsynlega útreikningslínu ef hún er ekki til og velja hana.
1. Ef ekki er búið að vista tilboðið frá því að útreikningslínan var stofnuð skal velja **Vista** á aðgerðasvæðinu.
1. Í flipanum **Línur** skal velja **Vörur**.
1. Á síðunni **Vörur** skal nota hnappana á aðgerðasvæðinu ti að bæta vörum við hnitanetið eða fjarlægja vörur eftir þörfum. Fyrir hverja línu skal stilla eftirfarandi reiti:

    - **Vörunúmer** – Veljið vöruna sem verður boðið upp á.
    - **(Aðrar víddir)** – Ef nota þarf fleiri víddir til að skilgreina vöruna (til dæmis vöruafbrigði, stærð, lit, stíl, svæði eða vöruhús) skal tilgreina þær. Til að bæta við eða fjarlægja tiltækar víddir skal velja **Birta víddir** á aðgerðasvæðinu.
    - **Magn** – Sláið inn magnið sem verður gefið upp þegar mörk fyrir valda útreikningslínu eru uppfyllt.
    - **Eining** – Veljið eininguna sem gildið **Magn** er tilgreint fyrir.
    - **Margt** – Þessi reitur virkar í tengslum við reitinn **Magn**. Til dæmis í vörulínu skal stilla reitinn **Magn** á *2* og reitinn **Margfeldi** á *100*. Ef þá er til staðar samtals magn sölupöntunar upp á 150 verða tvær vörurnar ókeypis (tvær á hverjar 100).

### <a name="settings-on-the-inventory-dimensions-tab"></a>Stillingar í flipa birgðavídda

Flipinn **Birgðavíddir** í flýtiflipanum **Upplýsingar um stjórnunar eftirágreidds afsláttar** sýnir öll tiltæk víddargildi fyrir afurðina sem er tilgreind fyrir valda tilboðslínu. Í honum eru víddir sem eru ekki sýndar í flýtiflipanum **Stjórnun eftirágreidds afsláttar**. Aðeins er hægt að breyta gildum fyrir þessar víddir sem eiga við um valda afurð.

Hægt er að bæta fleiri víddum við hnitanetið í flýtiflipanum **Stjórnun eftirágreidds afsláttar** með því að velja **Birta víddir** á aðgerðasvæðinu.

## <a name="calculation-methods-for-deal-lines"></a><a name="calc-methods"></a>Útreikningsaðferðir fyrir tilboðslínur

Í hvert skipti sem upplýsingar eru settar upp fyrir eina af tilboðslínunum eins og lýst er í hlutanum hér á undan þarf að velja útreikningsaðferðina fyrir þá línu. Þessi hluti útskýrir hverja útreikningsaðferð og sýnir dæmi sem sýna hvernig hver aðferð reiknar út samtals eftirágreiddan afslátt fyrir pantanir og tilboðslínur. Í þessum dæmum eru pantanir og tilboðslínur eins. Aðeins útreikningsaðferðirnar eru mismunandi.

### <a name="stepped-calculation-method"></a>Þrepaskipt útreikningsaðferð

Þrepaskipt útreikningsaðferð reiknar eitt skref í einu þar sem hver tilboðslína bætir ofan á eftirágreiddan afslátt þar til sölumagninu eða andvirðinu er náð. Skrefin geta byggt á annaðhvort magni eða virði varanna sem eru seldar eftir því hver stillingin er í reitnum **Grunnur** í flipanum **Almennt** í flýtiflipanum **Upplýsingar um stjórnunar eftirágreidds afsláttar**.

Til dæmis er tilboðslína sett upp þannig að reiturinn **Útreikningsaðferð** er stilltur á *Þrepaskipt* og reiturinn **Grunnur** er stilltur á *Virði*. Hún inniheldur útreikningslínur sem bjóða upp á eftirfarandi eftirágreidda afslætti:

- **Lína A:** 10 prósent upp í $1.000
- **Lína B:** 25 prósent allt að $2.500

Ef andvirði varanna sem voru keyptar eða seldar er $2000, verður eftirstandandi eftirágreiddur afsláttur að upphæð $350 reiknaður á eftirfarandi hátt:

- **Eftirágreiddur afsláttur (A):** *Þröskuldur* × *Prósenta (A)* = $1.000 × 10 prósent = $100
- **Eftirágreiddur afsláttur (B):** (*Virði selt* – *Þröskuldur (A)* ) × *Prósenta (B)* = ($2.000 – $1.000) × 25 prósent = $250
- **Heildareftirágreiddur afsláttur:** *Eftirágreiddur afsláttur (A)* + *Eftirágreiddur afsláttur (B)* = $100 + $250 = $350

Ef reiturinn **Grunnur** er stilltur á *Magn* í staðinn fyrir *Virði* virkar þrepaskipta útreikningsaðferðin á svipaðan hátt. Fyrsta skrefið er notað fyrir auðkennt magn þar til öðru skrefi er náð. Annað skrefið er síðan notað fyrir allt magn fyrir ofan fyrsta skrefið þar til þriðja skrefi er náð. Þetta ferli heldur svo áfram í gegnum öll næstu skref.

### <a name="cumulative-calculation-method"></a>Uppsöfnuð útreikningsaðferð

Uppsöfnuð útreikningsaðferð notar bara eina útreikningslínu til að reikna út eftirágreiddan afslátt. Ef margar útreikningslínur eru í boði fyrir tilboðslínuna er útreikningslínan með hæsta gildið eða hæsta magnið sem næst notuð fyrir allt magnið eða virðið. Eins og í öðrum útreikningsaðferðum notar uppsöfnuð aðferð stillinguna í reitnum **Grunnur** í flipanum **Almennt** í flýtiflipanum **Upplýsingar um stjórnunar eftirágreidds afsláttar** til að ákveða sölumagnið eða söluvirðið sem er notað til að reikna út eftirágreiddan afslátt.

Til dæmis er tilboðslína sett upp þannig að reiturinn **Útreikningsaðferð** er stilltur á *Uppsöfnun* og reiturinn **Grunnur** er stilltur á *Virði*. Hún inniheldur útreikningslínur sem bjóða upp á eftirfarandi eftirágreidda afslætti:

- **Lína A:** 10 prósent upp í $1.000
- **Lína B:** 25 prósent allt að $2.500

Ef andvirði varanna sem voru keyptar eða seldar er $2000 notar útreikningurinn aðeins línu B. Eftirstandandi eftirágreiddur afsláttur að upphæð $500 er reiknaður út á eftirfarandi hátt:

- **Heildareftirágreiddur afsláttur:** *Virði seldra* *Eftirágreiddur afsláttur (B)* = $2.000 × 25 prósent = $500

### <a name="rolling-calculation-method"></a>Hlaupandi útreikningsaðferð

Hlaupandi útreikningsaðferð notar allar mögulegar útreikningslínur fyrir tilboðið. Ef margar útreikningslínur eru til staðar og fleiri en ein þeirra er náð eru allar útreikningslínur sem náð er notaðar, en efri mörkin eiga við um hverja prósentu fyrir sig. Eins og í öðrum útreikningsaðferðum notar hlaupandi aðferð stillinguna í reitnum **Grunnur** í flipanum **Almennt** í flýtiflipanum **Upplýsingar um stjórnunar eftirágreidds afsláttar** til að ákveða sölumagnið eða söluvirðið sem er notað til að reikna út eftirágreiddan afslátt.

Til dæmis er tilboðslína sett upp þannig að reiturinn **Útreikningsaðferð** er stilltur á *Hlaupandi* og reiturinn **Grunnur** er stilltur á *Virði*. Hún inniheldur útreikningslínur sem bjóða upp á eftirfarandi eftirágreidda afslætti:

- **Lína A:** 10 prósent upp í $1.000
- **Lína B:** 25 prósent allt að $2.500

Ef andvirði varanna sem voru keyptar eða seldar er $2000, verður eftirstandandi eftirágreiddur afsláttur að upphæð $600 reiknaður á eftirfarandi hátt:

- **Eftirágreiddur afsláttur (A):** *Þröskuldur* × *Prósenta (A)* = $1.000 × 10 prósent = $100
- **Eftirágreiddur afsláttur (B):** *Virði selt* × *Prósenta (B)* = $2.000 × 25 prósent = $500
- **Heildareftirágreiddur afsláttur:** *Eftirágreiddur afsláttur (A)* + *Eftirágreiddur afsláttur (B)* = $100 + $500 = $600

### <a name="total-calculation-method"></a>Samtals útreikningsaðferð

Samtals útreikningsaðferð notar allar útreikningslínur til að reikna út eftirágreiddan afslátt. Hún notar heildarmagnið til að reikna út eftirágreiddan afslátt fyrir hverja útreikningslínu sem er náð og hver útreikningslína notar prósentuna sína á heildarupphæðina. Eins og í öðrum útreikningsaðferðum notar samtöluaðferðin stillinguna í reitnum **Grunnur** í flipanum **Almennt** í flýtiflipanum **Upplýsingar um stjórnunar eftirágreidds afsláttar** til að ákveða sölumagnið eða söluvirðið sem er notað til að reikna út eftirágreiddan afslátt.

Til dæmis er tilboðslína sett upp þannig að reiturinn **Útreikningsaðferð** er stilltur á *Samtals* og reiturinn **Grunnur** er stilltur á *Virði*. Hún inniheldur útreikningslínur sem bjóða upp á eftirfarandi eftirágreidda afslætti:

- **Lína A:** 10 prósent upp í $1.000
- **Lína B:** 25 prósent allt að $2.500

Ef andvirði varanna sem voru keyptar eða seldar er $2000, verður eftirstandandi eftirágreiddur afsláttur að upphæð $700 reiknaður á eftirfarandi hátt:

- **Eftirágreiddur afsláttur (A):** *Virði selt* × *Prósenta (A)* = $2.000 × 10 prósent = $200
- **Eftirágreiddur afsláttur (B):** *Virði selt* × *Prósenta (B)* = $2.000 × 25 prósent = $500
- **Heildareftirágreiddur afsláttur:** *Eftirágreiddur afsláttur (A)* + *Eftirágreiddur afsláttur (B)* = $200 + $500 = $700
