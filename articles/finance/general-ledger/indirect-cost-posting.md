---
title: Bókun óbeins kostnaðar
description: Í þessari grein er útskýrt hvernig á að bóka óbeinan kostnað, stofna kostnaðarflokka og bæta hnútum við kostnaðarskjalið fyrir óbeinan kostnað.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: CostSheetDesigner, BOMCostGroup, ProjCategory, CostingVersion, CostSheetCalculationFactor
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: 04af10760ec50d60cbbc31c233109dffb786933c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8868432"
---
# <a name="indirect-cost-posting"></a>Bókun óbeins kostnaðar

Óbeinn kostnaður er kostnaður sem tengist ekki neinum stökum verkþætti á beinan hátt í framleiðsluferlinu. Sem dæmi má nefna stjórnunarkostnað eins og laun starfsmanna, kostnað bókhaldsdeildar og rekstrarkostnað eins og leigu, veitur og vélakostnað.

## <a name="calculating-indirect-costs"></a>Útreikningur óbeins kostnaðar

Microsoft Dynamics 365 Finance er ekki með sjálfvirka leið til að reikna út hlutfallið fyrir óbeinan kostnað. Ákvarða þarf óbeinan kostnað, stofna kóða óbeins kostnaðar og vinna með taxta fyrir hvern óbeinan kostnað í kostnaðarskjalinu.

Nákvæmt ferli sem er notað til að reikna út óbeinan kostnað getur verið breytilegt milli fyrirtækja. Ferlið samanstendur þó almennt af eftirfarandi grunnskrefum:

1. Stofna lista yfir óbeinan kostnað til að skrá í framleiðslu. Þessi listi gæti tekið til leigu, umsýslukostnaðar, bókhaldsgjalda og lögfræðikostnaðar. Það ætti ekki að innihalda hráefniskostnað eða launakostnað sem eru skráðir í framleiðsluleiðum.
2. Taka saman allan óbeinan kostnað. Hægt er að flokka sams konar óbeinan kostnað eða halda honum aðskildum. Hver óbeinn kostnaður sem er grunnstilltur getur haft mismunandi aðallykla sem eru notaðir fyrir bókun í fjárhaginn.
3. Berðu óbeinan kostnað saman við stuðul, sem einnig er nefndur hagnýtingargrunnur. Þátturinn getur verið hvað sem er sem þú velur. Hér eru nokkur algeng dæmi:

    - Tekjur
    - Heildarmagn sem er framleitt
    - Uppsetningartími
    - Keyrslutími

    Hægt er að velja tímabilið sem á að reikna óbeinan kostnað fyrir, t.d. mánaðarlegt, ársfjórðungslegt eða árlegt. Samtala óbeins kostnaðar og þáttarins ætti að vera fyrir sömu tímalengd. Eftirfarandi reikniregla er notuð til að reikna hlutfall óbeins kostnaðar:

    *Óbeint kostnaðarhlutfall* = *Heildarútgjöld óbeins kostnaðar* &divide; *Samtöluþáttur*

4. Stofna óbeina kostnaðarflokka.
5. Skilgreina kostnaðarskjalið með verðinu hjá þér.
6. Viðhaldið kostnaði vegna óbeins kostnaðar í kostnaðarútgáfunni.

> [!NOTE]
> Hægt er að nota eininguna **Kostnaðarbókhald** til að safna saman kostnaði og ákvarða rekstrarkostnað frá mismunandi upprunum eins og framleiðslu, verkum og fjárhag. Nánari upplýsingar er að finna í [Kostnaðarbókhald](/cost-accounting/cost-accounting-home-page.md).

> [!IMPORTANT]
> Mismunandi eftirlitsstofnanir hafa gefið út leiðbeiningar um hvers konar kostnað hægt er að hafa með sem óbeinan kostnað eða rekstrarkostnað í kostnaði fullbúinnar vöru. Áður en þú byrjar að grunnstilla óbeinan kostnað er mælt með að athuga bókhaldsreglugerðir og staðbundnar reglugerðir til að ganga úr skugga um reglufylgni.

## <a name="create-cost-groups-for-indirect-costs"></a>Stofna kostnaðarflokka fyrir óbeinan kostnað

Það verður að stofna a.m.k. einn kostnaðarhóp til að nota fyrir óbeinan kostnað. Engin takmörk eru á fjölda kostnaðarflokka sem er hægt að nota. Íhugaðu hvernig þú reiknar út kostnaðinn og hvort mismunandi taxtar eru fyrir mismunandi gerðir af kostnaði. Til dæmis framleiðir fyrirtæki notandans matvæli. Sum hráefni og fullunnar vörur eru þurrvörur og eru með einn óbeinan kostnað fyrir vöruhús. Önnur hráefni og tilbúnar vörur eru í kæli, og hafa hærri óbeinan kostnað. Í þessu tilfelli gætirðu viljað stofna tvo kostnaðarflokka: **Kostnaður þurrefnis** og **Kostnaður kælivöru**.

Til að stofna kostnaðarflokk fyrir óbeinan kostnað skaltu fylgja þessum skrefum.

1. Opnið **Framleiðslustýring &gt; Uppsetning &gt; Leiðir &gt; Kostnaðarflokkar**.
2. Veljið **Ný** til að stofna hóp.
3. Á svæðinu **Kostnaðarflokkur** er fært inn einkvæmt heiti fyrir kostnaðarflokkinn, svo sem **MATOVH**.
4. Í reitnum **Heiti** skal slá inn lýsingu á kostnaðarflokknum, svo sem **Sameiginlegur efniskostnaður**.
5. Í reitnum **Kostnaðarflokksgerð** skal velja **Óbeinn**.
6. Valfrjálst: Í reitnum **Hegðun** skal velja **Fastur kostnaður** eða **Breytilegur kostnaður**.

## <a name="configure-the-costing-sheet-for-indirect-costs"></a>Skilgreina kostnaðarskjal fyrir óbeinan kostnað

Þegar einn eða fleiri kostnaðarflokkar hafa verið stofnaðir er hægt að grunnstilla kostnaðarskjalið með óbeinum kostnaði og skilgreina útreikninginn. Þú gætir viljað draga saman óbeinan kostnað í kostnaðarskjalinu. Til að draga úr óbeinum kostnaði er hægt að búa til valfrjálsan haus í kostnaðarskjalinu. Það verður að búa til a.m.k. einn hnút fyrir hvern kostnaðarflokk í kostnaðarskjalinu. Þú getur bætt við einum óbeinum kostnaðarútreikningi fyrir hvern kostnaðarflokk fyrir óbeinan kostnað.

### <a name="indirect-cost-node-types"></a>Hnútagerðir óbeins kostnaðar

Þessi hluti lýsir mismunandi tegundum hnúta fyrir óbeinan kostnað.

#### <a name="surcharge"></a>Álag 

**Aukagjald** er ein algengasta tegund óbeins kostnaðar. Það reiknar út hlutfall kostnaðar af hagnýtingargrunni á grundvelli framleiðslupöntunarinnar. Hagnýtingargrunnur er skilgreindur með því að velja kostnaðarflokkana sem eru tengdir við efnis- eða tímahluta í kostnaðarskjalinu.

Til dæmis gæti þriggja prósenta gjaldi verið bætt við framleiðslukostnað fyrir öll hráefni í framleiðslupöntun.

#### <a name="rate"></a>Taxti

Óbeinn kostnaður af gerðinni **Taxti** er notaður til að bæta fastri upphæð kostnaðar við framleiðslupöntun úr hagnýtingargrunni kostnaðar í framleiðslupöntuninni. Verð getur verið byggt á einni af þremur undirtegundum:

- **Ferli** – Verðið er byggt keyrslutíma á leiðinni.
- **Uppsetning** – Verðið er byggt á uppsetningartímanum á leiðinni.
- **Magn** – Gengið er út frá því magni sem framleitt er.

Hagnýtingargrunnur er skilgreindur með því að velja kostnaðarflokka sem tengdir eru við efnis- eða tímahlutann í kostnaðarskjalinu.

Sem dæmi föst upphæð sem nemur 2,00 USD er bætt við hverja framleiðslupöntun samkvæmt keyrslutíma á leiðinni fyrir launakostnaðarflokkinn í kostnaðarskjalinu.

#### <a name="output-unit-based"></a>Byggir á úttakseiningu

Óbeinn kostnaður af gerðinni **Byggir á úttakseiningu** er reiknaður með því að margfalda upphæðinni sem tilgreind er í flýtiflipanum **Taxti** í kostnaðarskjalinu með því að velja undirgerð. Hægt er að velja magn, þyngd, rúmmál fullunninnar vöru sem margfeldi fyrir óbeinan kostnað.

Til dæmis er hægt að nota magnið til að reikna 1,50 USD fyrir afskrift vélar fyrir hvert framleitt magn. Annað dæmi væri rúmmál sem notað er til að reikna 2,00 USD af kostnaði við kælingu fyrir rúmmálið sem fullunnin vara tekur í kælieiningum.

#### <a name="input-unit-based"></a>Byggir á inntakseiningu

Óbeinn kostnaður af gerðinni **Byggir á inntakseiningu** er reiknaður með því að margfalda upphæð hráefnis sem notað er í framleiðslupöntun með upphæð. Þú getur notað þyngd eða rúmmál inntaka á framleiðslupöntuninni til að reikna samtöluna. Hægt er að takmarka útreikninginn við undirsafn af efni með því að velja einn eða fleiri kostnaðarflokka í flýtiflipanum **Hagnýtingargrunnur** í kostnaðarskjalinu.

Til dæmis er rúmmál inntaks notað fyrir tiltekinn kostnaðarflokk sem tengdur er við kælivörur til að bæta 1,00 USD við framleiðslupöntunina.

### <a name="create-a-total-node-for-indirect-costs-in-the-costing-sheet"></a>Búa til samtöluhnút fyrir óbeinan kostnað í kostnaðarskjalinu

Til að búa til samtöluhnút fyrir óbeinan kostnað í kostnaðarskjalinu skal fylgja þessum skrefum.

1. Opnið **Kostnaðarstjórnun &gt; Uppsetning kostnaðarbókhaldreglna óbeins kostnaðar &gt; Kostnaðarskjal**.
2. Í trénu skal velja hnút sem sýnir kostnað vara sem hefur verið framleiddar.
3. Veljið **Ný** til að stofna hnút.
4. Í **Velja hnútagerð** skal velja **Samtala**.
5. Í reitnum **Kóði** skal færa inn einstakt auðkenni fyrir hnútinn, s.s. **Framleiðslukostnaður**.
6. Veldu gátreitinn **Haus**.
7. Veljið gátreitinn **Samtala**.
8. Veldu **Í lagi**.

### <a name="create-an-indirect-cost-group-node-in-the-costing-sheet"></a>Búa til hnút fyrir flokk fyrir óbeinan kostnað í kostnaðarskjalinu

Til að búa til hnút fyrir flokk fyrir óbeinan kostnað í kostnaðarskjalinu skal fylgja þessum skrefum.

1. Opnið **Kostnaðarstjórnun &gt; Uppsetning kostnaðarbókhaldreglna óbeins kostnaðar &gt; Kostnaðarskjal**.
2. Í trénu skal velja hnútinn sem á að stofna óbeina kostnaðinn undir. Til dæmis veldu samtöluhnútinn fyrir **Framleiðsla yfirhæð**.
3. Veljið **Ný** til að stofna hnút.
4. Í **Velja hnútagerð** skal velja **Kostnaðarflokkur**.
5. Í reitnum **Kóði** skal færa inn einstakt auðkenni fyrir hnútinn, s.s. **TRANSP**.
6. Í reitinn **Lýsing** er færð stutt lýsing, svo sem **Flutningskostnaður**.
7. Veldu **Í lagi**.
8. Í reitnum **Kostnaðarflokkur** skal velja kostnaðarflokk, svo sem **OVH1: Flutningskostnaður**.

### <a name="create-a-surcharge-indirect-cost"></a>Stofna aukakostnað vegna óbeins kostnaðar

Til að búa til aukagjald vegna óbeins kostnaðar á kostnaðarskjalinu skaltu fylgja eftirfarandi skrefum.

1. Opnið **Kostnaðarstjórnun &gt; Uppsetning kostnaðarbókhaldreglna óbeins kostnaðar &gt; Kostnaðarskjal**.
2. Í trénu skal velja hnút óbeins kostnaðarflokks sem á að stofna óbeina kostnaðinn undir. Til dæmis veldu samtöluhnútinn fyrir **TRANSP – flutningskostnaður**.
3. Veljið **Ný** til að stofna hnút.
4. Í **Velja hnútagerð** skal velja **Aukagjald**.
5. Í reitnum **Kóði** skal færa inn einstakt auðkenni fyrir hnútinn, s.s. **Aukagjald fyrir flutning**.
6. Veldu **Í lagi**.
7. Í svæðinu **Undirgerð** skal velja **Samtala**.
8. Á flýtiflipanum **Hagnýtingargrunnur** er **Nýtt** valið til að búa til kostnaðarkóða.
9. Í reitnum **Kóði** skal velja kostnaðarflokk sem á að nota til að reikna aukagjald.
10. Valfrjálst: Endurtaktu skref 8 til 9 fyrir hvern aukalegan kostnaðarflokk sem á að nota við útreikning.
11. Á flýtiflipanum **Aukagjald** velur þú **Nýtt** til að búa til verð.
12. Í reitnum **Útgáfa** skaltu velja kostnaðarútgáfuna sem bæta á aukagjaldinu við.
13. Valfrjálst: Í reitnum **Vefsvæði** skal færa inn vefsvæði til að leggja aukagjaldið á.
14. Í reitinn **Prósenta** skal færa inn prósentu til að reikna út framleiðslupantanir úr kostnaðarflokkum sem skilgreindir eru í flýtiflipanum **Hagnýtingargrunnur**.
15. Í flýtiflipanum **Fjárhagsbókanir** skal velja aðallykilinn til að nota fyrir reitina **Áætlaður óbeinn kostnaður nýttur**, **Áætlaður óbeinn kostnaður notaður**, **Óbeinn kostnaður nýttur** og **Kostnaður af notuðum óbeinum kostnaði, VÍV**.
16. Valfrjálst: Í flýtiflipanum **Fjárhagsvíddir** skal tilgreina allar fjárhagsvíddir sem á að færa inn sjálfgefið í færslur þegar þær eru bókaðar í fjárhaginn.

Aðferðin á undan sýnir hvernig hægt er að stofna til óbeins kostnaðar af gerðinni **Aukagjald**. Sambærileg skref eru notuð til að stofna til annars konar óbeinan kostnað. Eftirfarandi hlutar útskýra mismun fyrir hverja gerð.

#### <a name="rate"></a>Taxti

- Í skrefi 4 velur þú **Verð** í stað **Aukagjald**.
- Í skrefi 7 velur þú **Ferli**, **Uppsetning** eða **Magn** í stað **Samtala**.
- Í skrefi 11 skal nota flýtiflipann **Verð** í stað flýtiflipans **Aukagjald**.
- Í skrefi 14 skal færa inn upphæð í reitinn **Upphæð** í stað prósentu í reitinn **Prósenta**.

#### <a name="output-unit-based"></a>Byggir á úttakseiningu

- Í skrefi 4 velur þú **Byggir á úttakseiningu** í stað **Aukagjald**.
- Í skrefi 7 velur þú **Magn**, **Þyngd** eða **Rúmmál** í stað **Samtala**.
- Sleppið skrefum 8 til 10.
- Í skrefi 11 skal nota flýtiflipann **Verð** í stað flýtiflipans **Aukagjald**.

#### <a name="input-unit-based"></a>Byggir á inntakseiningu

- Í skrefi 4 velur þú **Byggir á inntakseiningu** í stað **Aukagjald**.
- Í skrefi 7 skaltu velja **Þyngd** eða **Rúmmál** í stað **Samtala**.
- Í skrefi 11 skal nota flýtiflipann **Verð** í stað flýtiflipans **Aukagjald**.
