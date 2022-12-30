---
title: Pökkunarstefnur gáms
description: Þessi grein lýsir muninum á pökkunarstefnum gáms og gefur dæmi.
author: GalynaFedorova
ms.date: 08/09/2022
ms.topic: article
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak, WHSContainerStructure, WHSContainerTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2021-06-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 5a9a0066abaa76294faebcb15d5091ba36e8a60d
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/23/2022
ms.locfileid: "9335766"
---
# <a name="container-packing-strategies"></a>Pökkunarstefnur gáms

[!include [banner](../includes/banner.md)]

*Pökkunarstefna gáms* er aðferð sem hægt er að nota til að skilgreina vöruúthlutanir í gáma. Í þessari grein er útskýrður munurinn á stefnunum *Pakka í alla opna gáma* og *Pakka aðeins í núgildandi gám*.

- **Pakka í alla opna gáma** – Kerfið verður að athuga alla opna gáma sem hafa verið búnir til í gámunarferlinu til að ganga úr skugga um að varan passi inn í einn af þeim. Meðan á pökkun stendur athugar kerfið hverja vöru til að ákvarða hvort hún passi í áður útbúinn gám. Ef varan passar ekki í fyrirliggjandi gám býr kerfið til nýjan gám og heldur áfram þar til búið er að pakka allri pöntuninni.

    Til dæmis þurfa *n* pantaðar vörur að fara í gám. Í versta falli, í hvert skipti sem kerfið vinnur úr vöru sem passar ekki í neinn gám sem þegar er til staðar, mun það gera alls (\[(*n* – 1) × (*n* + 1)\] ÷ 2) athuganir til að meta hvort varan passi í gámana sem þegar eru til staðar.

- **Pakka aðeins í núverandi gám** – Kerfið verður að athuga aðeins nýjasta gáminn til að ganga úr skugga um hvort varan passi í hann. Meðan á pökkun stendur athugar kerfið hverja vöru til að ákvarða hvort hún passi í nýjasta gáminn. Ef varan passar ekki í þann gám býr kerfið til nýjan gám og heldur áfram þar til búið er að pakka allri pöntuninni.

    Til dæmis þurfa *n* pantaðar vörur að fara í gám. Í versta falli mun kerfið gera samtals (*n* - 1) athuganir til að meta hvort varan passi í gámana.

## <a name="example-of-the-flow-for-container-packing-strategies"></a>Dæmi um flæði fyrir pökkunaraðferðir gáms

Eftirfarandi vörur eru settar upp fyrir gámapökkun.

| vara | Efnislegar víddir (breidd × dýpt × hæð) | Vægi |
|---|---|---|
| HDMI kapall 6' | 1 × 1 × 1 | 1 |
| HDMI kapall 12' | 2 × 1 × 1 | 1 |
| HDMI kapall 18' | 3 × 1 × 1 | 2 |

Einnig er hægt að setja upp eftirfarandi kassa sem verða notaðir fyrir pökkun.

| Gamur | Efnislegar víddir (lengd × breidd × hæð) | Vægi | Magn |
|---|---|---|---|
| Miðlungsstór kassi | 6 × 3 × 2 | 10 | 100 |

Að lokum seturðu upp pöntun sem er með eftirfarandi afurðir og magn.

| Sölupöntunarlína | Magn |
|---|---|
| HDMI kapall 12' | 9 |
| HDMI kapall 18' | 8 |
| HDMI kapall 6' | 13 |

Í eftirfarandi töflu er tekið saman hvernig gámapökkun virkar þegar aðferðin *Pakka í alla opna gáma* er notuð og þegar aðfeðrin *Pakka aðeins í núgildandi gám* er notuð.

| Pakka í alla opna gáma | Pakka í núgildandi gám |
|---|---|
| <p>HDMI kapall 12':</p><ol><li>Stofna nýjan gám, CONT0001.</li><li>Setjið 9 ea í gám CONT0001.</li></ol> | <p>HDMI kapall 12':</p><ol><li>Stofna nýjan gám, CONT0001.</li><li>Setjið 9 ea í gám CONT0001.</li></ol> |
| <p>HDMI kapall 18'':</p><ol><li>Athuga hvort hluturinn geti passað í gám CONT0001.</li><li>Stofna nýjan gám, CONT0002.</li><li>Setjið 5 ea í gám CONT0002.</li><li>Stofna nýjan gám, CONT0003.</li><li>Setjið 3 ea í gám CONT0003.</li></ol> | <p>HDMI kapall 18'':</p><ol><li>Athuga hvort hluturinn geti passað í gám CONT0001.</li><li>Stofna nýjan gám, CONT0002.</li><li>Setjið 5 ea í gám CONT0002.</li><li>Stofna nýjan gám, CONT0003.</li><li>Setjið 3 ea í gám CONT0003.</li></ol> |
| <p>HDMI kapall 6'':</p><ol><li>Athuga hvort hluturinn geti passað í gám CONT0001.</li><li>Setjið 1 ea í gám CONT0001.</li><li>Athuga hvort hluturinn geti passað í gám CONT0002.</li><li>Athuga hvort hluturinn geti passað í gám CONT0003.</li><li>Setjið 4 ea í gám CONT0003.</li><li>Stofna nýjan gám, CONT0004.</li><li>Setjið 8 ea í gám CONT0004.</li></ol> | <p>HDMI kapall 6'':</p><ol><li>Athuga hvort hluturinn geti passað í gám CONT0003.</li><li>Setjið 4 ea í gám CONT0003.</li><li>Stofna nýjan gám, CONT0004.</li><li>Setjið 9 ea í gám CONT0004.</li></ol> |

## <a name="example-scenario-pack-single-orders-per-container"></a>Dæmi: Pakka stökum pöntunum í gám

Í þessum hluta eru sýndar aðstæður þar sem kerfið er sett upp til að sameina margar pantanir í eina sendingu. Því verður gámapökkunin gerð úr sölupöntuninni til að tryggja að hver pöntun sem inniheldur margar afurðir sé pakkað í eigin gám.

Þessi virkni gerir kleift að takast á við aðstæður þar sem aðeins á að pakka einni sölupöntun í hvern gám þannig að dreifingarmiðstöðin geti hjáskipað fulla gáma milli smásöluverslana. Til viðbótar við smásöluaðstæður (pöntun fyrir hverja smásöluverslun og sendingu í dreifingarmiðstöð fyrir hjáskipun) er þessi aðferð einnig algeng í venjubundinni aðfangakeðju (sölupöntun í tímanlegri framleiðslulínu).

Þessar aðstæður sýna hvernig hægt er að fækka fjölda gáma sem eru metnir við pökkun með því að nota stefnuna *Pakka aðeins í núgildandi gám* fyrir gámapökkun.

### <a name="prerequisites"></a>Forkröfur

#### <a name="turn-on-the-consolidate-shipments-feature-in-your-system"></a>Kveikja á eiginleika fyrir sameiningu sendingar í kerfinu

Í þessum aðstæðum er eiginleikinn *Sameina sendingar* notaður. (Frá og með útgáfu 10.0.29 af Supply Chain Management er þessi eiginleiki skylda og ekki er hægt að slökkva á honum.) Ef þú ert að keyra útgáfu sem er eldri en 10.0.29, þá geta stjórnendur kveikt eða slökkt á þessum eiginleika með því að leita að eiginleikanum *Sameina sendingar* á vinnusvæðinu [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

#### <a name="make-demo-data-available"></a>Bjóða upp á sýnigögn

Þessar aðstæður vísa í gildi og færslur sem eru innifaldar í stöðluðum sýnigögnum fyrir Microsoft Dynamics 365 Supply Chain Management. Ef nota á gildin sem er boðið upp á hér eins og í æfingunum skal gæta þess að vinna í umhverfi þar sem sýnigögnin eru uppsett og stilla lögaðilann á **USMF** áður en hafist er handa.

### <a name="inspect-or-create-container-types"></a>Kanna eða stofna gámagerðir

Til að kanna gámagerðirnar eða stofna nýjar gámagerðir ef þess gerist þörf skal fylgja þessum skrefum.

1. Fara í **Vöruhúsakerfi** \> **Uppsetning** \> **Gámar** \> **Gámagerðir**.
1. Gangið úr skugga um að hver eftirfarandi gámagerð sé í boði í sýnigögnunum. Breytið eða stofnið gámagerðir eftir þörfum.

    - Gámagerð 1:

        - **Kóði gámagerðar:** *Kassi-stór*
        - **Lýsing:** *Stór kassi*.
        - **Hámarksnettóþyngd:** *100*
        - **Magn:** *400*
        - **Lengd:** *4*
        - **Breidd:** *10*
        - **Hæð:** *10*

    - Gámagerð 2:

        - **Kóði gámagerðar:** *Kassi-miðlungs*
        - **Lýsing:** *Miðlungsstór kassi*
        - **Hámarksnettóþyngd:** *50*
        - **Magn:** *200*
        - **Lengd:** *2*
        - **Breidd:** *10*
        - **Hæð:** *10*

    - Gámagerð 3:

        - **Kóði gámagerðar:** *Kassi-lítill*
        - **Lýsing:** *Lítill kassi*.
        - **Hámarksnettóþyngd:** *20*
        - **Magn:** *100*
        - **Lengd:** *1*
        - **Breidd:** *10*
        - **Hæð:** *10*

### <a name="inspect-or-create-container-groups"></a>Kanna eða stofna gámaflokka

Til að kanna gámaflokkana eða stofna nýja gámaflokka ef þess gerist þörf skal fylgja þessum skrefum.

1. Fara í **Vöruhúsakerfi** \> **Uppsetning** \> **Gámar** \> **Gámahópar**.
1. Gangið úr skugga um að eftirfarandi gámagerð sé í boði í sýnigögnunum. Ef hún er ekki tiltæk skal velja **Ný** til að búa hana til.

    - **Auðkenni gámaflokks:** *Kassar*
    - **Lýsing:** *Kassastærðir*

1. Í flýtiflipanum **Upplýsingar** fyrir gámaflokkinn *Kassar* skal ganga úr skugga um að eftirfarandi línur séu til. Ef þær eru ekki til skal velja **Ný** til að bæta þeim við.

    - Lína 1:

        - **Raðnúmer:** *1*
        - **Gámagerð:** *Kassi-stór*
        - **Prósentunýting gáms:** *100*

    - Lína 2:

        - **Raðnúmer:** *2*
        - **Gámagerð:** *Kassi-miðlungs*
        - **Prósentunýting gáms:** *100*

    - Lína 3:

        - **Raðnúmer:** *3*
        - **Gámagerð:** *Kassi-lítill*
        - **Prósentunýting gáms:** *100*

### <a name="create-a-new-container-build-template"></a>Stofnið nýtt gámaröðunarsniðmát

Til að stofna nýtt gámaröðunarsniðmát skal fylgja þessum skrefum.

1. Fara í **Vöruhúsakerfi** \> **Uppsetning** \> **Gámar** \> **Gámaröðunarsniðmát**.
1. Veljið **Nýtt** til að stofna gámaröðunarsniðmát sem er með eftirfarandi stillingar:

    - **Raðnúmer:** *1*
    - **Kenni gámasniðmáts:** *Kassi*
    - **Auðkenni gámaflokks:** *Kassar*
    - **Grunngerðir fyrirspurnar:** *Úthlutunarlína sölu*
    - **Kóði bylgjuskrefs:** *234*
    - **Leyfa skiptar tiltektir:** *Já*
    - **Aðferð gámapökkunar:** *Pakka aðeins í núgildandi gám*
    - **Pakka eftir leiðbeiningareiningu:** *Nei*

1. Á meðan línan fyrir nýja sniðmátið er enn valin skal velja **Breyta fyrirspurn** á aðgerðasvæðinu.
1. Venjulegur svargluggi fyrirspurnarritils birtist. Í flipanum **Röðun** skal velja **Bæta við** til að bæta við línu sem er með eftirfarandi stillingum:

    - **Tafla:** *Tímabundnar vinnufærslur*
    - **Afleidd tafla:** *Tímabundnar vinnufærslur*
    - **Reitur:** *Pöntunarnúmer*
    - **Leitarstefna:** *Hækkandi*

    > [!IMPORTANT]
    > Til að koma í veg fyrir að fara yfir alla aðra opna gáma og til að hraða ferlinu með því að athuga einn gám í einu, skal nota aðferðina *Pakka aðeins í núgildandi gám* ásamt röðun eftir pöntunarnúmeri. Þessi samsetning mun virka eins og vinnuhlé á vinnusniðmáti.

1. Veldu **Í lagi** til að loka svarglugga fyrirspurnarritils.
1. Á meðan línan fyrir nýja sniðmátið er enn valin skal velja **Takmarkanir á blöndun gáma** á aðgerðasvæðinu.

    Nú bætirðu takmörkun við sem setur vörur úr einni pöntun í einn gám. Vörur úr öðrum pöntunum verða settar í annan gám.

1. Veljið **Ný** til að búa til takmörkun blöndunar sem er með eftirfarandi stillingum:

    - **Tafla:** *Sölupantanir*
    - **Reitur valinn:** *SalesId* (reiturinn birtist sem *Sölupöntun* í hnitanetinu.)

1. Veljið **Í lagi** til að bæta takmörkuninni við.
1. Lokið síðunni.

### <a name="set-up-a-wave-template-for-containerization"></a>Setja upp bylgjusniðmát fyrir gámun

Til að setja upp bylgjusniðmát skal fylgja þessum skrefum.

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Bylgjur \> Bylgjusniðmát**.
1. Í listaglugganum skal stilla reitinn **Gerð bylgjusniðmáts** á *Sending*.
1. Veljið sniðmátið **63 Gámun** úr listanum.
1. Á aðgerðarúðunni skal velja **Breyta**.
1. Í flýtiflipanum **Aðferðir**, í dálknum **Valdar aðferðir**, skal finna eftirfarandi línu:

    - **Heiti aðferðar:** *gámun*
    - **Heiti:** *Gámun*

1. Stillið reitinn **Kóði bylgjuskrefs** fyrir þessa línu á *234*.

### <a name="set-up-a-work-template"></a>Setja upp vinnusniðmát

Fylgið þessum skrefum til þess að setja upp vinnusniðmát.

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Vinna \> Vinnusniðmát**.
1. Stillið reitinn **Gerð verkbeiðni** á *Sölupantanir*.
1. Í hnitanetinu **Yfirlit** skal finna og velja vinnusniðmátið sem á að nota fyrir pökun á stökum pöntunum í hvern gám. Fyrir þessar aðstæður skal velja sniðmátið **63 Tiltekt í gám**.
1. Á aðgerðasvæðinu skal velja **Breyta fyrirspurn**.
1. Venjulegur svargluggi fyrirspurnarritils birtist. Í flipanum **Röðun** skal bæta við eftirfarandi línum:

    - Lína 1:

        - **Tafla:** *Tímabundnar vinnufærslur*
        - **Afleidd tafla:** *Tímabundnar vinnufærslur*
        - **Reitur:** *Auðkenni sendingar*
        - **Leitarstefna:** *Hækkandi*

    - Lína 2:

        - **Tafla:** *Tímabundnar vinnufærslur*
        - **Afleidd tafla:** *Tímabundnar vinnufærslur*
        - **Reitur:** *Pöntunarnúmer*
        - **Leitarstefna:** *Hækkandi*

    - Lína 3:

        - **Tafla:** *Tímabundnar vinnufærslur*
        - **Afleidd tafla:** *Tímabundnar vinnufærslur*
        - **Reitur:** *Auðkenni gáms*
        - **Leitarstefna:** *Hækkandi*

1. Veldu **Í lagi** til að loka svarglugga fyrirspurnarritils.
1. Eftirfarandi skilaboð birtast: „Flokkun verður endurstillt, á að halda áfram?" Veldu **Já** til að halda áfram.
1. Á meðan sniðmátið **63 Tiltekt í gám** er enn valið skal velja **Vinnuhausaskil** á aðgerðasvæðinu.

    Nú notarðu stillingar til að sundurliða vinnunni þannig að hver gámur í pöntuninni er tengdur við eina verkbeiðni.

1. Veljið gátreitinn **Flokka eftir þessum reit** fyrir hverja línu á síðunni **Vinnuhausaskil** (**Auðkenni sendingar**, **Pöntunarnúmer** og **Auðkenni gáms**).
1. Lokið síðunni.

### <a name="set-up-shipment-consolidation-policies"></a>Setja upp samstæðureglur sendingar

Til að setja upp samstæðureglur sendingar skal fylgja þessum skrefum.

1. Opnið **Vöruhúsastjórnun \> Uppsetning \> Losa í vöruhús \> Samstæðureglur sendingar**.
1. Á listasvæðinu skal stilla reitinn **Gerð stefnu** á *Sölupantanir*.
1. Veljið stefnuna **Sjálfgefið** úr listanum.
1. Á aðgerðarúðunni skal velja **Breyta**.
1. Í flýtiflipanum **Samstæðureitir**, í listanum **Valdir reitir**, skal velja línuna þar sem reiturinn **Heiti reits** er stilltur á *Pöntun viðskiptavinar*.
1. Veljið hnappinn **Fjarlægja** ![Vinstri ör.](media/backward-button.png) til að færa reitinn í listann **Eftirstandandi reitir**.
1. Í aðgerðarúðunni skal velja **Vista**.

### <a name="set-up-physical-dimensions-for-the-product"></a>Setja upp efnislegar víddir fyrir afurðina

Til að setja upp efnislegar víddir fyrir afurðir sem verða notaðar í þessum aðstæðum skal fylgja þessum skrefum.

1. Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.
1. Veljið afurðina þar sem reiturinn **Vörunúmer** er stilltur á *A0001*.
1. Á Aðgerðasvæði, á flipanum **Stjórna birgðum**, í flokknum **Vöruhús**, velurðu **Efnislegar víddir**.
1. Á síðunni **Efnislegar víddir** ætti að nota eftirfarandi línu í hnitanetinu:

    - **Eining:** *stk.*
    - **Heildarþyngd:** *3.00*
    - **Breidd:** *2.00*
    - **Dýpt:** *2.00*
    - **Hæð:** *4.00*
    - **Magn:** *16.00*

1. Lokið síðunni.
1. Veljið afurðina þar sem reiturinn **Vörunúmer** er stilltur á *A0002*.
1. Á Aðgerðasvæði, á flipanum **Stjórna birgðum**, í flokknum **Vöruhús**, velurðu **Efnislegar víddir**.
1. Á síðunni **Efnislegar víddir** ætti að nota eftirfarandi línu í hnitanetinu:

    - **Eining:** *stk.*
    - **Heildarþyngd:** *4.00*
    - **Breidd:** *3.00*
    - **Dýpt:** *1.00*
    - **Hæð:** *3.00*
    - **Magn:** *9.00*

### <a name="create-sales-order-1"></a>Stofna sölupöntun 1

Til að stofna sölupöntun, skal fylgja eftirfarandi skrefum.

1. Farðu í **Sölu og markaðssetningu \> Sölupöntun \> Allar sölupantanir**.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Svargluggi fyrir stofnun nýrrar sölupöntunar birtist. Stilla eftirfarandi gildi:

    - **Viðskiptavinalykill:** *US-001*
    - **Vöruhús:** *63*

1. Veljið **Í lagi** til að stofna sölupöntunina og loka svarglugganum.
1. Ný sölupöntun opnast. Í flýtiflipanum **Sölupöntunarlínur** skal bæta við eftirfarandi sölulínum:

    - Lína 1:

        - **Vörunúmer:** *A0001*
        - **Magn:** *2*

    - Lína 2:

        - **Vörunúmer:** *A0002*
        - **Magn:** *2*

1. Veljið fyrstu línuna og svo **Birgðir \> Frátekning**.
1. Á síðunni **Frátekning** skal velja **Frátektarlota**. Því næst skal loka síðunni.
1. Endurtaka skal fyrri tvö skref fyrir seinni línuna.
1. Lokið síðunni.

### <a name="create-sales-order-2"></a>Stofna sölupöntun 2

Til að stofna aðra sölupöntun skal fylgja þessum skrefum.

1. Farðu í **Sölu og markaðssetningu \> Sölupöntun \> Allar sölupantanir**.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Svargluggi fyrir stofnun nýrrar sölupöntunar birtist. Stilla eftirfarandi gildi:

    - **Viðskiptavinalykill:** *US-001*
    - **Vöruhús:** *63*

1. Veljið **Í lagi** til að stofna sölupöntunina og loka svarglugganum.
1. Ný sölupöntun opnast. Í flýtiflipanum **Sölupöntunarlínur** skal bæta við eftirfarandi sölulínum:

    - Lína 1:

        - **Vörunúmer:** *A0001*
        - **Magn:** *4*

    - Lína 2:

        - **Vörunúmer:** *A0002*
        - **Magn:** *4*

1. Veljið fyrstu línuna og svo **Birgðir \> Frátekning**.
1. Á síðunni **Frátekning** skal velja **Frátektarlota**. Því næst skal loka síðunni.
1. Endurtaka skal fyrri tvö skref fyrir seinni línuna.
1. Lokið síðunni.

### <a name="create-the-load"></a>Stofna hleðsluna

Fylgið þessum skrefum til að búa til hleðslu fyrir hverja pöntun sem stofnuð var fyrir þessar aðstæður og losa hana síðan í vöruhúsið.

1. Farið í **Vöruhúsakerfi \> Hleðsla \> Vinnusvæði hleðsluáætlunar**.
1. Í flipanum **Sölulínur** skal finna og velja allar sölupöntunarlínur úr sölupöntununum sem voru stofnaðar fyrir þessar aðstæður.
1. Á aðgerðasvæðinu, í flipanum **Framboð og eftirspurn**, í flokknum **Bæta við**, skal velja **Við nýjan farm**. Völdum pöntunarlínum er bætt við nýja hleðslu.
1. Í svarglugganum **Úthlutun hleðslusniðmáts** í reitnum **Kenni hleðslusniðmáts** skal velja hleðslusniðmát, svo sem *40 feta gámur*.
1. Veldu **Í lagi** til að loka svarglugganum.
1. Í hlutanum **Hleðsla** er hægt að finna og velja hleðsluna sem var verið að stofna.
1. Veljið **Losa \> Losa í vöruhús**.
1. Í svarglugganum **Losa í vöruhús** skal velja **Í lagi** til að losa valda hleðslu í vöruhúsið.

### <a name="verify-the-shipments-and-containers"></a>Sannreyna sendingar og gáma

Eftirfarandi ferli gerir kleift að staðfesta sendingarnar sem hafa verið stofnaðar. Notið það til að yfirfara pöntunina sem var stofnuð fyrir þessar aðstæður og gangið úr skugga um að hafa fengið væntanlegar niðurstöður.

1. Opnið **Vöruhúsakerfi \> Sendingar \> Allar sendingar**.
1. Finnið og veljið sendinguna sem var stofnuð fyrir hleðsluna sem var verið að losa.
1. Á aðgerðasvæðinu, í flipanum **Flutningur**, skal velja **Skoða gáma**.
1. Staðfestið að vörurnar úr sölupöntununum hafi verið pakkaðar í tvo mismunandi gáma.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Gámun](wave-containerization.md)
