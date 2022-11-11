---
title: Nettókröfur og tengingarupplýsingar
description: Þessi grein veitir upplýsingar um reiknaðar nettóþarfir og tengiupplýsingar.
author: t-benebo
ms.date: 7/28/2021
ms.topic: article
ms.search.form: ReqTransOverview
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-07-28
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a31ff5490b08d92f0d966388b65de02bca25b050
ms.sourcegitcommit: 613be2f35e600ae1a1fa7ea2ae30e78984ca398a
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/07/2022
ms.locfileid: "9748439"
---
# <a name="net-requirements-and-pegging-information"></a>Nettókröfur og tengingarupplýsingar

[!include [banner](../../includes/banner.md)]

Þegar aðaláætlanagerð er keyrð í aðaláætlanagerð er mikilvægt að þú skiljir úttak hennar, hvernig fyrirliggjandi framboð dekkar eftirspurn og hvers vegna tiltekið framboð var búið til. Hægt er að nota síðuna **Nettóþarfir** til að átta sig betur á útreiknuðum kröfum sem aðaláætlanagerð gerir.

The **Nettókröfur** síða sýnir nettóþörf sem aðalskipulag reiknaði fyrir vöruna. Hún sýnir einnig þekjustillingarnar sem voru notaðar við keyrslu aðaláætlanagerðar, sundurliðun á samtals þörfum eftir færslugerð og upplýsingum um þarfarakningu.

## <a name="open-the-net-requirements-page"></a>Opna síðu nettóþarfa

Hægt er að opna síðuna **Nettóþarfir** á eftirfarandi hátt:

- Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**. Velja eða opna afurð. Því næst á aðgerðasvæðinu, í flipanum **Áætlun**, í flokknum **Þörf**, skal velja **Nettóþarfir**.
- Farðu í **Sölu og markaðssetningu \> Sölupöntun \> Allar sölupantanir**. Opna sölupöntun Því næst skal í flýtiflipanum **Sölupöntunarlínur**, á tækjastikunni, velja **Afurð og framboð \> Nettóþarfir**.
- Fara í **Áætlanagerð \> Aðaláætlanagerð \> Áætlaðar pantanir**. Velja eða opna áætlaða pöntun. Því næst skal á aðgerðasvæðinu, í flipanum **Skoða**, í flokknum **Þarfir**, velja **Þarfaregla**.

## <a name="use-the-net-requirements-page"></a>Nota síðu nettóþarfa

Síðan **Nettóþarfir** samanstendur af efri og neðri hluta. Á aðgerðarrúðunni á þessari síðu er hnappur til að **Uppfæra**. Þegar þessi hnappur er valinn birtist valmynd með skipunum.

### <a name="select-a-master-plan-to-view"></a>Stofnið aðaláætlun til skoða

Áður en þú skoðar nettóþarfir afurðarinnar skaltu ganga úr skugga um að velja viðeigandi aðaláætlun í reitnum **Áætlun** efst á síðunni.

### <a name="upper-section"></a>Efri hluti

Í efri hluta síðunnar eru eftirfarandi flipar:

- **Yfirlit** – Skoðaðu vöruþarfir afurðarvídda.
- **Vöruþekja** – Skoðaðu þekjustillingarnar sem voru notaðar við útreikning þarfa.
- **Samantekt** – Skoðaðu sundurliðun á samtals þörfum eftir færslugerð.
- **Tímabil** – Skoðaðu kvittanir, útgáfur og áætlaðar tiltækar birgðir fyrir hvert tímabil sem tímabilssniðmátið skilgreinir. Einnig er hægt að fá myndræna yfirsýn yfir áætlaðar birgðir í boði.

### <a name="lower-section"></a>Neðri hluti

Í neðri hluta síðunnar eru eftirfarandi flipar:

- **Yfirlit** – Skoðaðu listann yfir afurðaþarfir sem voru reiknaðar út við keyrslu aðaláætlanagerðar ásamt út- og innhreyfingarfærslum sem samsvara þörfunum. Listanum er sjálfgefið raðað eftir dagsetningu þarfa. Þegar þú velur þörf sýnir flýtiflipinn **Þarfarakning** í neðri hlutanum annaðhvort uppruna þarfanna eða færslurnar sem uppfylla þörfina.
- **Almennt** – Skoðaðu nákvæmar upplýsingar um valda þörf.
- **Aðgerð** – Skoðaðu aðgerðaboð fyrir þarfirnar.

### <a name="the-action-pane"></a>Aðgerðarsvæðið

Eftirfarandi skipanir eru í boði á aðgerðasvæði:

- **Uppfæra \> Aðaláætlanagerð** – Keyrðu aðaláætlanagerð beint af síðunni **Nettóþarfir**.
- **Uppfæra \> Spáráætlun** – Keyrðu spáráætlun beint af síðunni **Nettóþarfir**. Áætlanagerð fínstilling styður ekki þessa aðgerð.
- **Uppfæra \> Samfelldniáætlunargerð** – Keyrðu samfellda áætlunargerð beint af síðunni **Nettóþarfir**. Áætlanagerð fínstilling styður ekki þessa aðgerð.

## <a name="example-scenario"></a>Dæmi

Þetta dæmi sýnir hvernig upplýsingar um þarfarakningu er sett fram á síðunni **Nettóþarfir**.

### <a name="prerequisites"></a>Forkröfur

Áður en unnið er gegnum sviðsmyndina á að undirbúa eftirfarandi forsendur:

1. Þú verður að vinna með kerfi þar sem hefðbundin sýnigögn eru tiltæk og þú verður að setja lögaðilann á *USMF*.
2. Þetta dæmi notar afurð *1000*, sem er hluti af sýnigögnum USMF. Gakktu úr skugga um að þessi afurð sé til staðar og að hún sé sett upp á eftirfarandi hátt:

    - **Sjálfgefin gerð pöntunar:** *Innkaupapöntun*
    - **Lagerbirgðir:** *10,00*

3. Stofna innkaupapöntun fyrir magnið *25,00* og einingarverð *1000*. Nota geymsluvíddirnar þar sem birgðirnar eru staðsettar.
4. Keyrðu aðaláætlanagerð fyrir aðaláætlunina *DynPlan*.

### <a name="review-the-calculated-requirements"></a>Yfirfara útreiknaðar þarfir

Næst skal opna síðuna **Nettóþarfir** fyrir afurð *1000* til að yfirfara hvernig reiknaðar þarfir samsvara hver annarri.

1. Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.
1. Veldu afurðina sem er með gildið **Vörunúmer** sem *1000*.
1. Á aðgerðasvæðinu, í flipanum **Áætlun**, í flokknum **Þörf**, skal velja **Nettóþarfir**.
1. Á síðunni **Nettóþarfir** skal stilla reitinn **Áætlun** á *DynPlan*.
1. Í flipanum **Yfirlit** í neðri hluta síðunnar skal staðfesta að eftirfarandi þarfir séu sýndar sem línur í hnitanetinu.

    | Tilvísun | Magn sem þarf | Uppsafnað |
    |---|---|---|
    | Á lager | 10,00 | 10,00 |
    | Innkaupatillögur | 15.00 | 25.00 |
    | Sölupöntun | -25,00 | (Autt) |

    > [!NOTE]
    > Reiturinn **Magn sem þarf** sýnir heildarmagnið sem þörfin annaðhvort þarf á að halda (ef gildið er neikvætt) eða sem framboð (ef gildið er jákvætt). Reiturinn **Uppsafnað** sýnir heildarmagn inn- og úthreyfingar sem safnaðist upp á völdu tímabili.

1. Veldu þarfalínuna *Á lager* og farðu svo yfir þarfirnar sem þetta framboð dekkar í flýtiflipanum **Þarfarakning**. Eftirfarandi lína ætti að birtast þar.

    | Tilvísun | Magn sem þarf | Innifalið magn |
    |---|---|---|
    | Sölupöntun | -25,00 | -10,00 |

    Fyrirliggjandi lagerbirgðir dekkar að hluta eftirspurnina sem kemur frá sölupöntunum.

    ![Upplýsingar um þarfarakningu fyrir lagerbirgðir](media/pegging-on-hand.png "Upplýsingar um þarfarakningu fyrir lagerbirgðir")

1. Veldu þarfalínuna *Innkaupatillögur* og farðu svo yfir þarfirnar sem þetta framboð dekkar í flýtiflipanum **Þarfarakning**. Eftirfarandi lína ætti að birtast þar.

    | Tilvísun | Magn sem þarf | Innifalið magn |
    |---|---|---|
    | Sölupöntun | -25,00 | -15,00 |

    Vegna þess að sölupöntunin hefur þegar verið uppfyllt að hluta til, býr kerfið til fyrirhugaða innkaupapöntun fyrir það magn sem eftir er.

    ![Upplýsingar um þarfarakningu fyrir áætlaða innkaupapöntun](media/pegging-planned-purchase-order.png "Upplýsingar um þarfarakningu fyrir áætlaða innkaupapöntun")

1. Veldu þarfalínuna *Sölupöntun* og farðu svo yfir þarfirnar sem dekka þessa eftirspurn í flýtiflipanum **Þarfarakning**. Eftirfarandi línur ættu að birtast þar.

    | Tilvísun | Magn sem þarf | Innifalið magn |
    |---|---|---|
    | Á lager | 10,00 | 10,00 |
    | Innkaupatillögur | 15.00 | 15.00 |

    ![Festa upplýsingar fyrir sölupöntunina](media/pegging-planned-purchase-order.png "Festir upplýsingar fyrir sölupöntunina")

> [!NOTE]
> The *Öryggisbirgðir* krafan er ekki innifalin í **Nettókröfur** síðu.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
