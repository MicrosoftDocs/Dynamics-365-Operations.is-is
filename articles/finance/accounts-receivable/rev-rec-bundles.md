---
title: Búnt tekjuskráningar
description: Þetta efnisatriði lýsir búntaðgerðinni sem er hluti af tekjuskráningarmöguleikanum í viðskiptakröfum. Búnt samanstendur af yfirvöru og mörgum hlutum vöru.
author: kweekley
ms.date: 01/04/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-01-04
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: bce824267f435d9de0acd43ca145e0d148dfe67c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5816269"
---
# <a name="revenue-recognition-bundles"></a>Búnt tekjuskráningar

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir búntaðgerðinni sem er hluti af tekjuskráningarmöguleikanum í viðskiptakröfum. Búnt samanstendur af yfirvöru og mörgum hlutum vöru. Yfirvaran er færð inn á sölupöntun þannig að pöntunarfærsla verði skilvirkari. Hún er aftur á móti brotin niður í vöruhlutana. Innri skjöl, svo sem fylgiseðill, munu sýna vöruhlutana. Ytri skjöl sýna hins vegar aðeins yfirvöruna.

> [!NOTE]
> Microsoft Dynamics 365 Commerce rásir, t.d. á netinu, sölustaður og símaver, styðja ekki tekjuskráningu (þ.m.t. búntaðgerðina). Þetta inniheldur einnig PTC-lausnina fyrir Dynamics 365 Supply Chain Management og Dynamics 365 Sales. Ekki skal bæta vörum, sem eru skilgreindar til að nota tekjuskráningu, við pantanir eða færslur sem eru stofnaðar í Commerce-rásum eða í PTC-lausninni.

Til að setja upp búnt þarf að færa inn skilgreiningarlykla fyrir tekjuskráningu. Hins vegar er hægt að nota búnt þótt tekjuskráning sé ekki sett upp. Sömuleiðis er hægt að nota tekjuskráningu ef búnt eru ekki sett upp. Ef tekjuskráning er sett upp ákvarða vöruhlutarnir tekjuupphæðina og tekjuáætlunina sem eru notuð fyrir tekjuskráningu eða frestun þegar sölupöntun er reikningsfærð.

Uppsetning fyrir búnt notar uppskriftarvirknina. Frekari upplýsingar um hvernig á að setja upp búntvöru er að finna í [Uppsetning tekjuskráningar](revenue-recognition-setup.md). Ef yfirvörunni er flaggað sem búnti er hún meðhöndluð á annan hátt en aðrar vörur uppskriftar. Hér er listi yfir mismuninn:

- Brjóta verður búnt niður í gegnum staðfestingu sölupöntunar með því að velja **Staðfesta sölupöntun** í flipanum **Selja** á aðgerðasvæði sölupöntunarsíðu. Aldrei skal brjóta niður búntvörur með því að velja **Uppskriftarlínu** undir **Brjóta niður** í valmyndinni **Sölupöntunarlína** í flýtiflipanum **Sölupöntunarlínur**. Annars verður varan meðhöndluð sem uppskrift en ekki búnt.
- Staðfesta verður sölupöntun sem inniheldur búntvöru áður en fylgiseðill eða reikningur er stofnaður.
- Þegar búnt er brotið niður í gegnum staðfestingu sölupöntunar er hætt við yfirvöruna og einingarverði og afsláttum hennar er úthlutað á vöruhluta búntsins.
- Samtala vöruhluta verður alltaf að vera jöfn verði yfirvöru. Þess vegna eru takmarkanir á reitunum sem hægt er að uppfæra eða breyta fyrir vöruhluta. Til dæmis er ekki hægt að breyta einingarverðinu handvirkt. Því er heldur ekki hægt að breyta óbeint með því að gera nýjan verðsamning. Til að koma í veg fyrir nýjan verðsamning er ekki hægt að breyta birgðavíddum í vöruhlutunum.
- Þegar skjal út á við er prentað, t.d. staðfesting sölupöntunar eða reikningur, er yfirvaran prentuð en ekki vöruhlutarnir.

## <a name="bundles-on-sales-orders"></a>Búnt á sölupöntunum

USMF-sýnifyrirtækið inniheldur eftirfarandi uppsetningu búnts. Athugið að öll uppsetning fyrir tekjuskráningu, t.d. uppsetning tekjuáætlana, hefur verið fjarlægð úr vörunum sem er að finna í þessu sýnidæmi.

**Yfirvara:** Fartölvubúnt

- **Vöruhluti:** Magn 1 af vöru 1000
- **Vöruhluti:** Magn 1 af vöru S0021
- **Vöruhluti:** Magn 1 af vöru notendaþjónustu

*Grunnsöluverð* vöruhluta er nauðsynlegur hluti í uppsetningu vöruhluta. Grunnsöluverð er skilgreint í flýtiflipanum **Selja** fyrir vöru. Það er notað til að reikna úthlutunarstuðulinn þegar einingarverð yfirvöru er úthlutað á vöruhlutana. Söluverð verðsamnings eru aldrei notað í þessum tilgangi.

Eftirfarandi grunnsöluverð eru skilgreind fyrir vöruhlutana:

- **1000:** $1.900,00
- **S0021:** $150.00
- **Notendaþjónusta:** $500.00

Sölupöntun er færð inn fyrir viðskiptavin US-004, Cave Wholesales. Eina línan sem færð er inn er fyrir búntvöru fartölvunnar. Hægt er að taka sjálfgefið einingarverð fyrir yfirlínuna úr fjölmörgum stöðum, svo sem verðsamningi eða grunnsöluverði. Í þessu dæmi voru $2.300 færðir handvirkt inn sem einingarverðið.

[![Búntvara fartölvu í sölupöntun](./media/bundle-01.png)](./media/bundle-01.png)

Vegna þess að sölupöntunin inniheldur búnt þarf að staðfesta hana. Staðfestingarglugginn sýnir hluta búntsins.

[![Staðfesta svarglugga sölupöntunar sem sýnir vöruhlutana](./media/bundle-02.png)](./media/bundle-02.png)

Prentaða staðfestingarskýrslan sýnir hins vegar aðeins yfirvöru búntsins vegna þess að sú skýrsla er skjalið sem snýr að viðskiptavininum.

[![Staðfestingarskýrsla sem sýnir aðeins yfirvöruna](./media/bundle-03.png)](./media/bundle-03.png)

Þegar sölupöntunin hefur verið staðfest er yfirvaran enn sýnd í sölupöntuninni, en stöðu hennar hefur verið breytt í **Hætt við**. Auk þess er nettóupphæðin rakin í reitnum **Nettóupphæð búnts**. Þessa upphæð þarf til að prenta út reikninginn vegna þess að reikningurinn sýnir yfirvöruna en ekki vöruhlutana.

Samtala vöruhlutanna verður að vera jöfn gildinu **Nettóupphæð búnts** fyrir yfirvöruna vegna þess að það gildi er upphæðin sem viðskiptavinurinn sér á prentuðum reikningi. Til að tryggja að reikningurinn samsvari upphæðum sem eru bókaðar í fjárhag, eru breytingar á vöruhlutum takmarkaðar. Til dæmis er ekki hægt að breyta svæði og vöruhúsi vegna þess að slíkar breytingar gætu valdið verðbreytingu samkvæmt verðsamningi.

Einingarverðinu úr línunni fyrir yfirvöruna er úthlutað á vöruhlutana á eftirfarandi hátt:

**Samtals grunnsöluverð frá hlutum:** $1.900 + $500 + $150 = $2.550

- **Íhlutur 1:** $2.300 × (1.900 ÷ 2.550) = $1.713,73
- **Íhlutur 2:** $2.300 × (500 ÷ 2.550) = $450,98
- **Íhlutur 3:** $2.300 × (150 ÷ 2.550) = $135,29

Samtala hlutanna verður að vera jöfn $2.300, sem hún er ($1.713,73 + $450,98 + $135,29 = $2.300).

Ef breytingar eru nauðsynlegar fyrir alla vöruhluta, þá má fjarlægja yfirvöruna. Í slíku tilfelli eru vöruhlutarnir líka fjarlægðir. Það má bæta yfirvörunni við aftur og hægt er að ljúka nauðsynlegum breytingum áður en sölupöntunin er staðfest.

[![Búntvara sem inniheldur breytingar á vöruhlutum](./media/bundle-04.png)](./media/bundle-04.png)

Þegar sölupöntunin er tekin til og henni pakkað munu skjölin aðeins innihalda vöruhluta búntsins. Fylgiseðill og reikningur verða að innihalda heilt búnt. Annars er ekki hægt að bóka þá. Til dæmis sýnir svarglugginn þrjá vöruhluta. Ef reynt er að eyða einum þeirra koma upp villuboð sem tilkynna að afgreiða verði allar afurðir í búntinu áður en hægt verður að reikningsfæra þær.

Nauðsynlegt er að afhenda og reikningsfæra búnt sem fullt búnt. Til dæmis ef magni fyrir vöru 1000 er breytt í 4, en magn hinna vöruhlutanna er 5, verður hvorki hægt að bóka fylgiseðilinn né reikninginn.

Aðeins er hægt að senda og reikningsfæra upphæð að hluta til ef magnið er minnkað fyrir alla vöruhluta búntsins. Til dæmis er slegið inn magn upp á 5 fyrir búntvöru fartölvu í sölupöntun. Eftir að sölupöntunin hefur verið staðfest eru þrjú vöruhlutirnir sýndir á sölupöntuninni og magn hvers er 5. Við afhendingu og reikningsfærslu verður magnið sjálfgefið stillt á 5 fyrir hvern hluta. Hins vegar er hægt að leiðrétta magnið niður í 3 fyrir alla þrjá vöruhlutana. Í þessu tilfelli verða þrjú heil búnt afgreidd og reikningsfærð. Eftirstandandi tvær búntvörur (magn upp á 2 fyrir hvern vöruhlutanna þriggja) má afgreiða og reikningsfæra síðar.

Lokaskrefið er að reikningsfæra sölupöntunina. Við reikningsfærslu sýnir reikningsglugginn vöruhlutana.

[![Reikningsgluggi sem sýnir vöruhlutana](./media/bundle-06.png)](./media/bundle-06.png)

Hins vegar sýnir prentaður reikningur aðeins yfirvöruna.
 
[![Prentaður reikningur sem sýnir aðeins yfirvöruna](./media/bundle-07.png)](./media/bundle-07.png)

Reikningabókin sem er stofnuð eftir bókun inniheldur ekki yfirvöru búntsins vegna þess að varan er með stöðuna **Hætt við**.

[![Reikningabók sem inniheldur ekki yfirvöruna](./media/bundle-08.png)](./media/bundle-08.png)

Mikilvægt er að reikningabókin innihaldi ekki yfirvöru búntsins vegna þess að allar úrvinnslur sem gerðar eru eftir bókun reikningsins byggjast á þeirri reikningabók. Til dæmis ef stofnuð er kreditnóta úr flipanum **Selja** á aðgerðasvæðinu mun stofnuð kreditnóta innihalda vöruhlutana en ekki yfirvöruna.

[![Kreditnóta sem sýnir vöruhluta en ekki yfirvöru](./media/bundle-09.png)](./media/bundle-09.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]