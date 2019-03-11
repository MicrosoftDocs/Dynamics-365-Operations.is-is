---
title: Uppfylling öryggisbirgða fyrir vörur
description: Þetta efni fjallar um uppfylling öryggisbirgða og hvernig á að setja upp magn öryggis birgðir fyrir vörur.
author: roxanadiaconu
manager: AnnBe
ms.date: 11/27/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqSafetyKey, ReqItemTableSetup, ReqItemJournalName, ReqItemTable, EcoResProductDetailsExtended
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: roxanad
ms.dyn365.ops.version: 7.2999999999999998
ms.search.validFrom: 2017-12-31
ms.openlocfilehash: 147cc3984e6dc641209beefdb3545615b42767a2
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "341535"
---
# <a name="safety-stock-fulfillment-for-items"></a>Uppfylling öryggisbirgða fyrir vörur

[!include [banner](../includes/banner.md)]

Öryggisbirgðir gefa til kynna viðbótar magn af vöru sem er geymt í birgðum til að draga úr hættu á að varan verði uppseld. Öryggisbirgðir eru notaðar sem geymslubirgðir ef sölupantanir koma inn og birgir getur ekki afhent viðbótar vöruna til að veða við umbeðinni sendingardagsetningu viðskiptavinarins. Þegar öryggisbirgðir er notaður til að uppfylla sölupöntun verða öryggisbirgðirnar minnkaðar. Þú getur notað Aðaláætlanagerð til að sjálfkrafa færa birgðirnar aftur á öryggisstigið.    

## <a name="set-up-safety-stock-levels-for-items"></a>Setja upp öryggisbirgðastig fyrir vörur

Öryggisbirgðir eru settar upp sem hluti af vöruþekju á **Vöruþekja** síðunni undir **Útgefnar vörur** > **Áætlun** > **Þekja**.

Færið inn í reitinn **Lágmark** það öryggisbirgðastig sem óskað er að halda eftir fyrir vöru. Gildi er tilgreint í birgðaeiningum. Ef reiturinn er skilinn eftir auður er sjálfgildið núll. Þetta svæði er tiltækt þegar þú velur **Tímabil**, **Skilyrði**, eða **Lágm./Hám.** í listanum **Þekjukóðar**. Viðmiðunarmörk birgðastigs eiga við um fyrirliggjandi birgðir, sem þýðir að frátekningar og merkingar geta leitt til áfyllingar öryggisbirgða áður en efnislegt magn fer undir tilgreint lágmarksgildi.

> [!NOTE]
> Notandi verður að skilgreina allar aðrar áætlaðar þekjuvíddir áður en hægt er að skilgreina svæðið **Lágmark**. Þetta kemur í veg fyrir að ógild skrá sé notuð meðan á aðalskipulagi stendur. Þessi staða gæti komið upp, til dæmis, ef víddaflokkur er víkkaður út með auka áætlaða þekjuvídd þar sem hámarks og lágmarks birgðamagn hefur ennþá ekki verið skilgreint.

Lágmarkslyklar gera kleift að bregðast við árstíðarbundnum sveiflum í eftirspurn. Til dæmis er hægt að minnka lágmarksbirgðastig vöru á tímum þegar eftirspurn er lítil og auka það svo smátt og smátt á hinum mánuðum. Þú býrð til lágmarkslykil með því að fara á **Aðaláætlanagerð** > **Uppsetning** > **Þekja** > **Lágmarks-/hámarkslyklar**. Þú tilgreinir lágmarks takkann til að stilla öryggisbirgðastöðu eftir árstíðum í **Lágmarkslykill** svæðinu á **Vöruþekja** síðunni. 

## <a name="example-minimum-key"></a>Dæmi: Lágmarkslykill
Ef þú vilt setja upp lágmarkslykil fyrir sem gerir ráð fyrir aukinni eftirspurn í vor- og sumarmánuðum skal fara í **Aðaláætlanagerð** > **Uppsetning** > **Þekja** > **Lágmarks-/hámarkslyklar** og fylgja þessum leiðbeiningum.

1. Stofnið 12 línur og tölusetjið frá 1 upp í 12 í reitnum **Breyta**.
2. Í reitnum **Eining** skal velja **Mánuði**.
3. Í reitnum **Þáttur**, færið inn þau gildi sem er lýst í eftirfarandi töflu.

|Lína|Færa inn þetta gildi|Niðurstaða|
|---|---|---|
|1–3|1|Lágmarksbirgðir byggja á stillingarnar á síðunni **Vöruþekja** fyrir janúar og út mars.|
|4-5|2|Lágmarksbirgðir eru margfaldaðar með stuðlinum 2 fyrir apríl og maí.|
|6-8|2,5|Lágmarksbirgðir eru margfaldaðar með stuðlinum 2,5 fyrir júní út ágúst.|
|9-12|1|Lágmarksbirgðir snúa aftur í stillingar á síðunni **Vöruþekja** fyrir september út desember.|

Ef þekjukóðinn er **Lágm./Hám.**, geturðu einnig tilgreint **Hámark** birgðamagn sem óskað er að halda fyrir vöru. Gildið er einnig gefið upp í birgðaeiningum. Ef áætlaðar tiltækar birgðir fara niður fyrir lágmarksmagn myndar aðaláætlanagerð áætlaða pöntun til að uppfylla allar opnar kröfur og færir tiltækar birgðir upp að tilgreindu hámarksmagni. Alveg eins og þú settir upp **Lágmark** verður að skilgreina allar áætlaðar þekjuvíddir áður en þú getur skilgreint **Hámark** reitinn.

## <a name="example-minmax-coverage-code"></a>Dæmi: Lágm./Hám. þekjukóði
Lágmarksmagn er 10 og hámark er 15. Núgildandi lagerbirgðir eru 4. Það býr til lágmarksþörf magns upp á 6. Hinsvegar, þar sem hámarksmagn er 15 myndar aðaláætlanagerð áætlaða pöntun fyrir 11 vörur.

Fyrir vörur sem fylgja árstíðabundnum kröfum gætirðu þurft að vinna með mismunandi hámarksgildum. Til að gera það þarftu að skilgreina **Hámarkslykla** með því að fara í **Aðaláætlanagerð** > **Uppsetning** > **Þekja** > **Lágm./Hám. lyklar**. Fylltu út reitinn **Hámarkslykill** á síðunni **Vöruþekja**. Þú getur skoðað upplýsingar um stig öryggisbirgðastöðu, skilgreind með lágmarkslyklum á **Lágm./Hám.** flipanum, á síðunni **Vöruþekja**. Þú þarft að ganga úr skugga um að lágmarks- og hámarksgildi sé haldið í samstillingu á tilteknu tímabili.

## <a name="safety-stock-fulfillment"></a>Uppfylling öryggisbirgða 

**Uppfylla lágmark** færibreytan gerir þér kleift að velja þá dagsetningu eða tímabil sem birgðastig verður að ná því magni sem þú tilgreindir í reitnum **Lágmark**. Þetta svæði er tiltækt þegar þú velur **Tímabil**, **Skilyrði**, eða **Lágm./Hám.** í listanum **Þekjukóðar**.

Ef **Lágmarkslyklar** eru notaðir skal velja gátreitinn **Lágmarkstímabil** til að uppfylla lágmarksbirgðastig fyrir öll tímabil sem sett eru upp fyrir lágmarkslykilinn. Ef gátreiturinn er auður eru lágmarksbirgðir uppfylltar fyrir núgildandi tímabil eingöngu.

Eftirfarandi atburðarás sýnir hvernig þessi breytur virkar og hvað er munurinn á gildum þess.

> [!NOTE]
> Fyrir allar myndirnar í þessu efni táknar x-ásinn birgðir, y-ásinn táknar daga, strikin tákna birgðastigið, örvarnar tákna færslur, svo sem sölupöntunarlínur, innkaupapöntunarlínur eða áætlaðar pantanir.

[![Venjulegur atburðarás fyrir öryggisbirgðauppfyllingu](./media/Scenario1.png)](./media/Scenario1.png) **Lágmarks uppfylling** breytan getur haft eftirfarandi gildi:
### <a name="todays-date"></a>Dagurinn í dag 
Tilgreint lágmarksmagn er uppfyllt á þeim degi sem aðaláætlanagerð er keyrð. Kerfið reynir að uppfylla öryggisbirgðastig eins fljótt og auðið er, jafnvel þótt það geti verið óraunhæft vegna afhendingartíma. 
[![Kröfu um dagsetning í dag](./media/TodayReq.png)](./media/TodayReq.png) Áætluð pöntun P1 er búin til fyrir dagsetningu dagsins til að koma tiltækum birgðum upp fyrir öryggisbirgðastigið á þessum degi. Sölupöntunarlínurnar S1 til S3 halda áfram að lækka birgðastigið. Áætlaðar pantanir P2 til P4 eru búnar til með aðaláætlanagerð þannig að birgðastig fari aftur að öryggismörkum eftir hverja sölupöntunarkröfu.
Þegar **Krafa** þekjukóði er notaður eru margar áætlaðar pantanir búin til. Það er alltaf góð hugmynd að nota annaðhvort **Tímabil** eða **Lágm/Hám.** þekju fyrir vörur og efni í tíðri eftirspurn, til að pakka áfyllingunni saman. Eftirfarandi skýringarmynd sýnir dæmi um þekjukóða **Tímabil**.
[![Tímabil. Dagurinn í dag](./media/TodayPeriod.png)](./media/TodayPeriod.png) Eftirfarandi skýringarmynd sýnir dæmi um þekjukóða **Lágm./Hám.**.
[![Lágm.Hám. Dagurinn í dag](./media/TodayMinMax.png)](./media/TodayMinMax.png)
### <a name="todays-date--procurement-time"></a>Dagurinn í dag + öflunartími 
Tilgreint lágmarksmagn er uppfyllt á þeim degi sem aðaláætlanagerð er keyrð, og einnig innkaupin eða afhendingartími framleiðslu. Innan þessa tíma eru öll öryggismörk. Ef vöru fylgir viðskiptasamningur og gátreiturinn **Finna viðskiptasamninga** er valinn á síðunni **Færibreytur aðaláætlanagerðar** er ekki tekið tillit til biðtíma afhendingar úr viðskiptasamningi. Afendingartímar eru fenginn úr þekjustillingum vörunnar eða frá vörunni.
Þessi uppfyllingarhamur mun búa til áætlanir með minni töfum og færri áætluðum pantanir óháð uppsetningu þekjuhóps á vöruna. Eftirfarandi mynd sýnir árangur áætlunarinnar ef þekjukóðinn er **Krafa** eða **Tímabil**.  
[![Krafa. Tímabil. Dagurinn í dag og afhendingartími](./media/TodayPLTReq.png)](./media/TodayPLTReq.png) Eftirfarandi mynd sýnir árangur áætlunarinnar ef þekjukóðinn er **Lágm./Hám.**  
[![Lágm.Hám. Dagurinn í dag og afhendingartími](./media/TodayPLTMinMax.png)](./media/TodayPLTMinMax.png)
### <a name="first-issue"></a>Fyrsta úthreyfing 
Tilgreint lágmarksmagn er uppfyllt á þeim degi þegar fyrirliggjandi birgða fer undir lágmarksstig, eins og sýnt er á eftirfarandi mynd. Jafnvel þótt tiltækar birgðir sé undir lágmarksstiginu á þeim degi þegar aðaláætlanagerð er keyrt, mun **Fyrsta útgáfa** ekki reyna að dekka það fyrr en næsta krafa kemur inn.
Eftirfarandi skýringarmynd sýnir dæmi fyrir þekjukóða **Krafa**.
[![Áætla vöru með **Krafa** þekjukóði og **Fyrsta útgáfa** uppfylling](./media/FirstIssueReq.png)](./media/FirstIssueReq.png) Eftirfarandi mynd sýnir dæmi fyrir þekjukóða **Tímabil**.
[![Áætla vöru með **Tímabil** þekjukóði og **Fyrsta útgáfa** uppfylling](./media/FirstIssuePeriod.png)](./media/FirstIssuePeriod.png) Eftirfarandi mynd sýnir dæmi fyrir þekjukóða **Lágm./Hám.**.
[![Áætla vöru með **Lágm.Hám.** þekjukóða og **Fyrsta útgáfa** uppfylling](./media/FirstIssueMinMax.png)](./media/FirstIssueMinMax.png) Á þeim degi þegar aðaláætlanagerð er keyrt, ef tiltækar birgðir er þegar undir öryggisbirgðamörkum, **Dagurinn í dag** og **Dagurinn í dag + innkaupatími** mun kveikja á áfyllingu strax. **Fyrsta útgáfa** mun bíða þangað til það er önnur útgáfufærsla, svo sem sölupöntun og uppskriftarlínukrafa, fyrir vöruna, og þá mun það kveikja á áfyllingunni á dagsetningu þessarar færslu. Á þeim degi þegar aðaláætlanagerð er keyrt, ef tiltækar birgðir er ekki undir öryggisbirgðamörkum, **Dagurinn í dag** og **Fyrsta útgáfa** munu hafa í för með nákvæmlega sömu niðurstöðu og sýnd er á myndinni hér fyrir neðan. 

[![NotUnderLimit](./media/ReqFirstIssue.png)](./media/ReqFirstIssue.png) Á þeim degi þegar aðaláætlanagerð er keyrt, ef tiltækar birgðir er ekki undir öryggisbirgðamörkum, mun **Dagurinn í dag + innkaupatími** gefa eftirfarandi niðurstöðu, því það frestar uppfyllingu til loka afhendingartíma innkaupa.
![Áætla vöru með **Krafa** þekjukóða og **Fyrsta útgáfa** uppfylling](./media/ReqTodayLT.png)
### <a name="coverage-time-fence"></a>Þekjutímamörk
Tilgreint lágmarksmagn er uppfyllt innan þess tímabils sem tilgreint er í svæðinu **Þekjutímamörk**. Þessi valkostur er gagnlegur þegar aðaláætlanagerð leyfir ekki tiltækum birgðum til notkunar fyrir alvöru pantanir, svo sem sölu eða millifærslur, til að reyna að viðhalda öryggismörkum. Hins vegar, í framtíðarútgáfum verður þessi hamur áfyllingar ekki lengur nauðsynlegur og þessi valkostur verður gerður úreltur.
## <a name="plan-safety-stock-replenishment-for-first-expired-first-out-fefo-items"></a>Áætla áfyllingu öryggisbirgða fyrir Fyrst útrunnið, Fyrst út (FEFO) vörur
Á hverjum tíma mun innhreyfing birgða með nýjasta fyrningardagsetningu verða notuð fyrir öryggisbirgðir til að leyfa raunverulegan eftirspurn, svo sem sölulínur eða BOM línur, að verða uppfylltar í Fyrst útrunnið, Fyrst út (FEFO) pöntuninni.
Til að sýna hvernig þetta virkar skaltu íhuga eftirfarandi atburðarás.
[![FEFOScenario](./media/FEFOScenario.png)](./media/FEFOScenario.png) Þegar áætlanagerð er keyrð mun hún dekka fyrstu sölupöntunar frá núverandi lagerbirgðum og viðbótar innkaupapöntunar fyrir það magn sem eftir er.
[![FEFO1](./media/FEFO1.png)](./media/FEFO1.png) Áætluð pöntun er búin til til að ganga úr skugga um að fyrirliggjandi birgðum sé fært aftur til öryggismarka.
[![FEFO2](./media/FEFO2.png)](./media/FEFO2.png) Þegar önnur sölupöntun er áætluð, er sú áætlaða sölupöntun sem var búin til áður og dekkar öryggisbirgðirnar notuð til að dekka þetta magn. Þess vegna eru öryggisbirgðirnar í stöðugri veltu.
[![FEFO3](./media/FEFO3.png)](./media/FEFO3.png) Að lokum er önnur áætluð pöntun búin til til að dekka öryggisbirgðirnar.
[![FEFO4](./media/FEFO4.png)](./media/FEFO4.png) Allir runurnar eru runnin út samkvæmt því, og áætlaðar pantanir eru búnar til til áfyllingar öryggisbirgða eftir að það er útrunnið.

## <a name="how-master-planning-handles-the-safety-stock-constraint"></a>Hvernig aðaláætlanagerð meðhöndlar öryggisbirgðir þvingun

Öryggisbirgðir eru raktar í kerfinu sem tegund kröfu, rétt eins og sölulínur eða BOM kröfur. Þú getur séð kröfulínu öryggisbirgða á **Netkröfur** síðunni ef þú fjarlægir sjálfgefna síuna á dálknum **Tegund kröfu**.

Að uppfylla kröfufærslu öryggisbirgða er tekið úr forgangi ef kerfið ákveður að það veldur töfum við að uppfylla raunverulegan eftirspurn, svo sem sölulínur, BOM línur, flutningskröfur eða eftirspurnarspálínur. Annars skaltu ganga úr skugga um að fyrirliggjandi birgðir séu fyrir ofan öryggisbirgðamagnið og með sömu forgang og aðrar eftirspurnartegundir. Þetta tryggir að engar tafir verða á raunverulegum færslum og hjálpar til við að koma í veg fyrir of mikla áfyllingu og of fljóta áfyllingu öryggisbirgða.

Í þekjufasa aðaláætlanagerðar er ekki áfylling öryggisbirgða ekki lengur sett úr forgangi. Nota má lagerbirgðir á undan öllum öðrum tegundir eftirspurnar. Við útreikning tafa verður bætt við nýjum rökum til að fara yfir seinkaðar sölulínur, BOM línu kröfur og allar aðrar tegundir eftirspurnir, til að ákvarða hvort hægt væri að afhenda þau á réttum tíma, að því tilskildu að öryggisbirgðir sé notaður. Ef kerfið gefur til kynna að það geti dregið úr töfum með því að nota öryggisbrigðir, þá munu sölulínur eða BOM línur setja öryggisbirgðir í staðinn fyrir upphaflega þekju sína og kerfið muni kveikja á áfyllingu öryggisbirgða í staðinn.

Ef áætlunin eða varan er ekki settur upp til útreiknings seinkunar, þá hafa skorður öryggisbirgðirnar sama forgang og aðrar eftirspurnartegundir. Þetta þýðir að það er frátekning á lager og aðrar tiltækar birgðir á undan öðrum tegundir eftirspurnar.
