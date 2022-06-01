---
title: Óbein kostnaðarbókun
description: Þetta efnisatriði útskýrir hvernig á að bóka óbeinan kostnað, stofna kostnaðarflokka og bæta við hnútum við kostnaðarblaðið fyrir óbeinan kostnað.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: CostSheetDesigner, BOMCostGroup, ProjCategory, CostingVersion, CostSheetCalculationFactor
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: d7f4753f69d83d172993e1c9b04be2220fdf253f
ms.sourcegitcommit: 1ea145dc606e243c7f51d91a5c0dd9e385bbda4a
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/25/2022
ms.locfileid: "8804646"
---
# <a name="indirect-cost-posting"></a>Óbein kostnaðarbókun

Óbeinn kostnaður er kostnaður sem tengist ekki beint neinni einni starfsemi í framleiðsluferlinu. Sem dæmi má nefna stjórnunarkostnað eins og laun starfsmanna, kostnað við bókhaldsdeild og kostnaður eins og leigu, veitur og vélakostnaður.

## <a name="calculating-indirect-costs"></a>Útreikningur á óbeinum kostnaði

Microsoft Dynamics 365 Finance hefur ekki sjálfvirka leið til að reikna út hlutfall fyrir óbeinan kostnað. Þú verður að ákvarða óbeina kostnaðinn þinn, búa til óbeina kostnaðarkóða og viðhalda hlutfallinu fyrir hvern óbeinan kostnað í kostnaðarblaðinu.

Nákvæmt ferli sem er notað til að reikna út óbeinan kostnað gæti verið örlítið breytilegt eftir fyrirtækjum. Hins vegar, almennt, samanstendur ferlið af eftirfarandi grunnskrefum:

1. Búðu til lista yfir óbeinan kostnað til að færa í framleiðslu. Þessi listi gæti innihaldið húsaleigu, stjórnunarkostnað, bókhaldsgjöld og lögfræðikostnað. Það ætti ekki að innihalda hráefniskostnað eða launakostnað sem er færður á framleiðsluleiðum.
2. Leggðu saman allan óbeina kostnaðinn. Þú getur flokkað svipaðar tegundir óbeins kostnaðar eða haldið þeim aðskildum. Hver óbeinn kostnaður sem er stilltur getur haft mismunandi aðallykla sem eru notaðir til að bóka í fjárhag.
3. Berðu óbeina kostnaðinn saman við þátt, sem einnig er nefndur frásogsgrundvöllur. Stuðullinn getur verið hvað sem er sem þú velur. Hér eru nokkur algeng dæmi:

    - Tekjur
    - Heildarmagn sem er framleitt
    - Uppsetningartími
    - Keyrslutími

    Þú getur valið tímabilið sem þú vilt reikna út óbeina kostnaðinn þinn fyrir, svo sem mánaðarlega, ársfjórðungslega eða árlega. Summa óbeina kostnaðar þíns og summa þáttar þíns ætti að vera fyrir sama tíma. Eftirfarandi formúla er notuð til að reikna út óbeina kostnaðarhlutfallið:

    *Óbeinn kostnaðarhlutfall* = *Heildarkostnaður óbeinna kostnaðar*&divide;*Heildarstuðull*

4. Búa til óbeina kostnaðarhópa.
5. Stilltu kostnaðarblaðið með gjöldum þínum.
6. Haltu kostnaði fyrir óbeina kostnaðinn þinn í kostnaðarútgáfunni.

> [!NOTE]
> Þú getur notað **Kostnaðarbókhald** mát til að safna kostnaði og ákvarða kostnaður þinn frá mismunandi aðilum, svo sem framleiðslu, verkefnum og fjárhag. Fyrir frekari upplýsingar, sjá [Kostnaðarbókhald](/cost-accounting/cost-accounting-home-page.md).

> [!IMPORTANT]
> Mismunandi eftirlitsstofnanir hafa gefið út leiðbeiningar um þær tegundir kostnaðar sem hægt er að taka með sem óbeinn kostnað eða yfirkostnað í kostnaði fullunnar vöru þinnar. Áður en þú byrjar að stilla óbeinan kostnað mælum við með því að þú hafir samband við endurskoðanda þinn og staðbundnar reglur til að tryggja að þú uppfyllir kröfur.

## <a name="create-cost-groups-for-indirect-costs"></a>Stofna kostnaðarhópa fyrir óbeinan kostnað

Þú verður að stofna að minnsta kosti einn kostnaðarflokk til að nota fyrir óbeinan kostnað. Það eru engin takmörk á fjölda kostnaðarflokka sem þú getur notað. Íhugaðu hvernig þú reiknar út kostnaðinn þinn og hvort það séu mismunandi verð fyrir mismunandi gerðir kostnaðar. Til dæmis framleiðir fyrirtækið þitt matvæli. Sumt hráefni og fullunnar vörur eru þurrvörur og hafa einn óbeinan kostnað fyrir vörugeymslu. Annað hráefni og fullunnar vörur eru í kæli og hafa hærri óbeinan kostnað. Í þessu tilviki gætirðu viljað búa til tvo kostnaðarflokka: **Þurrt efni yfir höfuð** og **Kælt efni yfir höfuð**.

Til að stofna kostnaðarflokk fyrir óbeinan kostnað skal fylgja þessum skrefum.

1. Fara til **Framleiðslueftirlit&gt; Uppsetning&gt; Leiðir&gt; Kostnaðarhópar**.
2. Veldu **Nýtt** að búa til hóp.
3. Í **Kostnaðarhópur** reit, sláðu inn einstakt heiti fyrir kostnaðarflokkinn, svo sem **MATOVH**.
4. Í **Nafn** reit, sláðu inn lýsingu á kostnaðarflokknum, svo sem **Efni yfir höfuð**.
5. Í **Tegund kostnaðarhóps** reit, veldu **Óbeint**.
6. Valfrjálst: Í **Hegðun** reit, veldu **Fastur kostnaður** eða **Breytilegur kostnaður**.

## <a name="configure-the-costing-sheet-for-indirect-costs"></a>Stilltu kostnaðarblaðið fyrir óbeinan kostnað

Eftir að þú hefur búið til einn eða fleiri kostnaðarflokka geturðu stillt kostnaðarblaðið þitt með óbeinum kostnaði og skilgreint útreikninginn þinn. Þú gætir viljað flokka óbeinan kostnað í kostnaðarblaðið. Til að flokka óbeinan kostnað er hægt að stofna valfrjálsan haus í kostnaðarblaðinu. Þú verður að búa til að minnsta kosti einn hnút fyrir hvern kostnaðarflokk í kostnaðarblaðinu. Fyrir hvern kostnaðarflokk fyrir óbeinan kostnað er hægt að bæta við einum óbeinum kostnaðarútreikningum í viðbót.

### <a name="indirect-cost-node-types"></a>Tegundir óbeinna kostnaðarhnúta

Þessi hluti lýsir mismunandi gerðum hnúta fyrir óbeinan kostnað.

#### <a name="surcharge"></a>Álag 

**Aukagjald** er ein algengasta tegund óbeins kostnaðar. Það reiknar hlutfall af kostnaði út frá upptökugrunni kostnaðar á framleiðslupöntuninni. Þú skilgreinir frásogsgrundvöllinn með því að velja kostnaðarflokka sem eru tengdir við efni eða tímahluta þína í kostnaðarblaðinu.

Til dæmis gæti 3 prósenta álag bæst við framleiðslukostnað fyrir allt hráefni í framleiðslupöntun.

#### <a name="rate"></a>Taxti

Óbeinn kostnaður við **Gefa** gerð er notuð til að bæta fastri kostnaðarupphæð við framleiðslupöntunina frá upptökugrunni kostnaðar á framleiðslupöntuninni. Hlutfallið getur verið byggt á einni af þremur undirtegundum:

- **Ferli** – Gjaldið miðast við keyrslutíma leiðarinnar.
- **Uppsetning** – Verðið er byggt á uppsetningartímanum á leiðinni.
- **Magn** – Hlutfallið byggist á því magni sem framleitt er.

Þú skilgreinir frásogsgrundvöll með því að velja kostnaðarflokka sem eru tengdir við efni eða tímahluta í kostnaðarblaðinu.

Til dæmis er föstu upphæð 2,00 Bandaríkjadalir (USD) bætt við hverja framleiðslupöntun, byggt á keyrslutíma í leiðinni fyrir launakostnaðarhópinn í kostnaðarblaðinu þínu.

#### <a name="output-unit-based"></a>Byggir á úttakseiningu

Óbeinn kostnaður við **Byggt á úttakseiningu** gerð er reiknuð með því að margfalda upphæðina sem er tilgreind á **Gefa** Flýtiflipi kostnaðarblaðsins eftir valinni undirtegund. Þú getur valið magn, þyngd eða rúmmál fullunnar vöru sem margfaldara fyrir óbeina kostnaðinn.

Til dæmis, þú notar magnið til að reikna 1.50 USD af vélaafskriftum fyrir hvert magn sem er framleitt. Sem annað dæmi notarðu rúmmálið til að reikna 2.00 USD af kælikostnaði fyrir rúmmálið sem fullunnin vara tekur í kælieiningarnar þínar.

#### <a name="input-unit-based"></a>Byggir á inntakseiningu

Óbeinn kostnaður við **Inntakseining byggð** gerð er reiknuð með því að margfalda magn hráefna sem er neytt í framleiðslupöntun með magni. Hægt er að nota þyngd eða rúmmál aðfönganna á framleiðslupöntuninni til að reikna út heildina. Þú getur takmarkað útreikninginn við undirmengi efna með því að velja einn eða fleiri kostnaðarflokka á **Frásogsgrundvöllur** Flýtiflipi kostnaðarblaðsins.

Til dæmis, þú notar magn inntaks fyrir tiltekinn kostnaðarflokk sem er tengdur við kældar vörur til að bæta 1.00 USD við framleiðslupöntunina.

### <a name="create-a-total-node-for-indirect-costs-in-the-costing-sheet"></a>Stofna heildarhnút fyrir óbeinan kostnað í kostnaðarblaðinu

Til að stofna heildarhnút fyrir óbeinan kostnað í kostnaðarblaðinu skal fylgja þessum skrefum.

1. Fara til **Kostnaðarstjórnun&gt; Uppsetning óbeins kostnaðarreikningsskila&gt; Kostnaðarblað**.
2. Í trénu, veldu hnút sem táknar kostnað vöru sem hefur verið framleidd.
3. Veldu **Nýtt** til að búa til hnút.
4. Í **Veldu hnútagerð** reit, veldu **Samtals**.
5. Í **Kóði** reit, sláðu inn einstakt auðkenni fyrir hnútinn, svo sem **Framleiðslukostnaður**.
6. Veldu **Fyrirsögn** gátreit.
7. Veldu **Samtals** gátreit.
8. Veldu **Í lagi**.

### <a name="create-an-indirect-cost-group-node-in-the-costing-sheet"></a>Stofna óbeinan kostnaðarflokkshnút í kostnaðarblaðinu

Til að stofna óbeinan kostnaðarflokkshnút í kostnaðarblaðinu skal fylgja þessum skrefum.

1. Fara til **Kostnaðarstjórnun&gt; Uppsetning óbeins kostnaðarreikningsskila&gt; Kostnaðarblað**.
2. Í trénu velurðu hnútinn sem þú vilt stofna óbeina kostnaðinn undir. Til dæmis, veldu heildarhnút fyrir **Framleiðslukostnaður**.
3. Veldu **Nýtt** til að búa til hnút.
4. Í **Veldu hnútagerð** reit, veldu **Kostnaðarhópur**.
5. Í **Kóði** reit, sláðu inn einstakt auðkenni fyrir hnútinn, svo sem **TRANS**.
6. Í **Lýsing** reit, sláðu inn stutta lýsingu, svo sem **Flutningur yfir höfuð**.
7. Veldu **Í lagi**.
8. Í **Kostnaðarhópur** reit, veldu kostnaðarflokk, svo sem **OVH1: Flutningur yfir höfuð**.

### <a name="create-a-surcharge-indirect-cost"></a>Búðu til aukagjald óbeinn kostnað

Fylgdu þessum skrefum til að búa til óbeinan aukakostnað á kostnaðarblaðinu þínu.

1. Fara til **Kostnaðarstjórnun&gt; Uppsetning óbeins kostnaðarreikningsskila&gt; Kostnaðarblað**.
2. Í trénu velurðu óbeina kostnaðarflokkshnútinn sem þú vilt stofna óbeina kostnaðinn undir. Til dæmis, veldu heildarhnút fyrir **TRANSP - Flutningakostnaður**.
3. Veldu **Nýtt** til að búa til hnút.
4. Í **Veldu hnútagerð** reit, veldu **Aukagjald**.
5. Í **Kóði** reit, sláðu inn einstakt auðkenni fyrir hnútinn, svo sem **Flutningsálag**.
6. Veldu **Í lagi**.
7. Í **Undirgerð** reit, veldu **Samtals**.
8. Á **Frásogsgrundvöllur** Flýtiflipi, veldu **Nýtt** til að búa til kostnaðarkóða.
9. Í **Kóði** reit, veldu kostnaðarflokk til að nota til að reikna út álagið.
10. Valfrjálst: Endurtaktu skref 8 til 9 fyrir hvern viðbótarkostnaðarflokk sem þú vilt nota við útreikninginn.
11. Á **Aukagjald** Flýtiflipi, veldu **Nýtt** að búa til gengi.
12. Í **Útgáfa** reit, veldu kostnaðarútgáfu til að bæta álaginu við.
13. Valfrjálst: Í **Síða** reit, sláðu inn síðu til að nota aukagjaldið á.
14. Í **Prósenta** reit, sláðu inn prósentuna sem á að reikna út á framleiðslupantanir úr kostnaðarflokkunum sem eru skilgreindir í **Frásogsgrundvöllur** Flýtiflipi.
15. Á **Fjárhagsfærslur** Flýtiflipi, veldu aðalreikninginn sem á að nota fyrir **Áætlaður óbeinn kostnaður upptekinn**, **kostnaður vegna óbeins kostnaðar sem neytt er, WIP**, **kostnaður upptekinn**, og **Kostnaður við óbeinan kostnað sem neytt er, WIP** sviðum.
16. Valfrjálst: Á **Fjárhagsstærðir** Flýtiflipi, tilgreinið allar fjárhagsvíddir sem á að færa inn sjálfgefið í færslum þegar þær eru bókaðar í fjárhag.

Fyrri aðferð sýnir hvernig á að búa til óbeinan kostnað við **Aukagjald** tegund. Svipuð skref eru notuð til að búa til aðrar tegundir óbeins kostnaðar. Eftirfarandi kaflar lýsa muninum fyrir hverja tegund.

#### <a name="rate"></a>Taxti

- Í skrefi 4, veldu **Gefa** í staðinn fyrir **Aukagjald**.
- Í skrefi 7, veldu **Ferli**, **·**, eða **Magn** í staðinn fyrir **Samtals**.
- Í skrefi 11, notaðu **Gefa** flýtiflipann í stað **Aukagjald** Flýtiflipi.
- Í skrefi 14 skaltu slá inn upphæð í **Magn** reit í stað prósentu í **Prósenta** sviði.

#### <a name="output-unit-based"></a>Byggir á úttakseiningu

- Í skrefi 4, veldu **Byggt á úttakseiningu** í staðinn fyrir **Aukagjald**.
- Í skrefi 7, veldu **Magn**, **·**, eða **Bindi** í staðinn fyrir **Samtals**.
- Slepptu skrefum 8 til 10.
- Í skrefi 11, notaðu **Gefa** flýtiflipann í stað **Aukagjald** Flýtiflipi.

#### <a name="input-unit-based"></a>Byggir á inntakseiningu

- Í skrefi 4, veldu **Inntakseining byggð** í staðinn fyrir **Aukagjald**.
- Í skrefi 7, veldu **Þyngd** eða **Bindi** í staðinn fyrir **Samtals**.
- Í skrefi 11, notaðu **Gefa** flýtiflipann í stað **Aukagjald** Flýtiflipi.
