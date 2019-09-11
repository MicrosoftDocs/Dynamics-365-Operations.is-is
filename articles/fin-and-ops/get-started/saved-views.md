---
title: Vistuð yfirlit
description: Þetta efnisatriði lýsir því hvernig á að nota eiginleika fyrir vistuð yfirlit.
author: jasongre
manager: AnnBe
ms.date: 08/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2019-07-31
ms.dyn365.ops.version: Platform update 28
ms.openlocfilehash: 43f25796e6271f14acfc72f931398ab63338a307
ms.sourcegitcommit: b068b17ef708a0b349db8df1542e4244bb983d13
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2019
ms.locfileid: "1870834"
---
# <a name="saved-views"></a>Vistuð yfirlit

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

## <a name="introduction"></a>Inngangur
Sérstilling gegnir mikilvægu hlutverki í því að gera notendum og fyrirtækjum kleift að hámarka notendaupplifun í Microsoft Dynamics 365 for Finance and Operations til að mæta þörfum þeirra. Frekari upplýsingar um sérstillingu er að finna í [Sérsníða notandaupplifun](personalize-user-experience.md).

Með hefðbundinni sérstillingu gátu notendur aðeins verið með eitt sett af sérstillingum fyrir hverja skjámynd. Vistuð yfirlit víkka út sérstillingu á nokkra mikilvæga vegu:

-    Yfirlit leyfa notendum að hafa sett sérstillinga með mörgum heitum fyrir hverja skjámynd, sem hægt er að fara á milli á fljótlegan hátt eftir þörfum. Þetta gerir notanda kleift að búa til mörg aðlöguð yfirlit fyrir síðu, þar sem hvert yfirlit hefur verið sniðið að þörfum þess að geta framkvæmt ákveðið viðskiptatengt verkefni. 

-    Yfirlit búin til fyrir sérstakar gerðir af síðum geta einnig innihaldið síur eða flokkanir sem notandi bætir við, sem gerir notendum kleift að snúa sér fljótt að algengum síuðum gagnasöfnum. Sjá hlutann [Hvaða síður styðja yfirlit](saved-views.md#what-pages-support-views) fyrir frekari upplýsingar. 

-    Hægt er að gefa út yfirlit til öryggishlutverka, sem þýðir að hvaða notandi sem er með það hlutverk hefur aðgang að og getur notað þetta yfirlit, burtséð frá möguleikum notanda til að gera sérstillingar. Þessi útgáfumöguleiki gerir fyrirtækjum kleift að skilgreina stöðluð yfirlit stofnunar sem eru aðlöguð að rekstrinum. Sjá hlutann [Stjórnun sérstillinga á fyrirtækisstigi með yfirlitum](saved-views.md#managing-personalizations-at-an-organizational-level-with-views) fyrir frekari upplýsingar.

-    Ólíkt hefðbundinni sérstillingu eru yfirlit ekki vistuð sjálfkrafa þegar notandi framkvæmir ákveðnar sérstillingar eða síanir á lista. Ákveðnar vistanir eru nauðsynlegar til að bjóða upp á sveigjanleika við stofnun á yfirliti á undan eða eftir breytingarnar sem tengjast þessu yfirliti hafa verið gerðar og til að tryggja að skilgreiningar yfirlits hafi ekki óvart verið breytt með síum eða sérstillingum sem ekki eru ætlaðar til langtímanotkunar.  

## <a name="switching-between-views"></a>Skipta á milli yfirlita
Þegar yfirlit hafa verið virkjuð fyrir umhverfi munu allar síður sem styðja yfirlit innihalda samandregna stjórnun á yfirlitsvali efst í skjámyndinni sem sýnir heiti á núverandi yfirliti.  

Til eru tvær stærðir á yfirlitsvali: 

-   **Stórt yfirlitsval**: Síður sem birta lista á áberandi hátt verða með stærra yfirlitsval af nokkrum ástæðum. Mikilvægast er að stærra yfirlitsvalið gefur til kynna síðurnar þar sem yfirlitið getur innihaldið síur skilgreindar af notanda. Vegna þess að síur eru innifaldar í yfirlitunum, stærra yfirlitsvalið er einnig leyft sem yfirlit, verða heiti oft besta lýsing á gögnunum sem eru sýnd á skjánum og búist er við því að notendur muni skipta á milli yfirlita oftar á þessum síðugerðum.  
 
-   **Lítið yfirlitsval**: Allar aðrar skjámyndir með heilli síðu (undantekningin er vinnusvæði og yfirlitið) eru með minna yfirlitsval sem sést við hliðina á yfirskrift síðunnar. Yfirlit á þessum síðum innihalda eingöngu sérstillingar (en ekki síur skilgreindar af notanda). Á þessum síðum er yfirskrift skjámyndar eða titill færslu oft mikilvægustu upplýsingarnar efst á skjámyndinni. Minni stærðin endurspeglar einnig að búist sé við færri skiptingum á milli yfirlita á þessum síðum. 
 
Ef smellt er á heiti yfirlits opnast yfirlitsvalið og sýnir lista yfir tiltæk yfirlit fyrir þessa síðu

-    **Klassískt yfirlit**: Klassískt yfirlit er tilbúið yfirlit fyrir síðuna með engum sérstökum sérstillingum.  
-    **Persónulegt yfirlit**: Yfirlit án hengiláss standa fyrir persónulegu yfirlitin þín. Þetta eru yfirlit sem þú hefur annaðhvort búið til eða stjórnandi hefur gefið þér þau.  
-    **Læst yfirlit**: Sum yfirlit (eins og klassískt yfirlit og öll yfirlit sem eru gefin út fyrir hlutverkið þitt) eru með hengilás við hliðina á þeim í yfirlitsvalinu, sem gefur til kynna að þú getur ekki breytt þessum yfirlitum. Óbeinar sérstillingar sem endurspegla síðunotkun eru hinsvegar vistaðar sjálfkrafa, t.d. breyting á breidd dálks í hnitaneti eða stækkun eða minnkun á flýtiflipa. Hinsvegar er hægt að búa til persónulegt yfirlit sem byggist á læstu yfirliti með því að nota aðgerðina **Vista afrit** ef þú ert með réttindi fyrir sérstillingar.
-    **Ný yfirlit**: Birt yfirlit sem hafa ekki enn verið opnuð eru ljómaðar vinstra megin við heiti yfirlitsins.  

Til að skipta yfir í annað yfirlit skal fyrst opna yfirlitsvalið og síðan velja yfirlitið sem á að hlaða inn. 

## <a name="creating-and-modifying-views"></a>Búa til og breyta yfirlitum
Ólíkt hefðbundinni sérstillingu eru yfirlit ekki vistuð sjálfkrafa þegar notandi framkvæmir ákveðnar sérstillingar (eða síanir á lista). Þörf er á sérstakri aðgerð til að vista þessar breytingar í yfirliti. Þetta býður upp á sveigjanleika við stofnun á yfirliti á undan eða eftir breytingarnar sem tengjast þessu yfirliti hafa verið gerðar og einnig til að tryggja að skilgreiningar yfirlits hafi ekki óvart verið breyttar með einnota síum eða sérstillingum. Takið eftir að óbeinar sérstillingar (t.d. stækkun eða minnkun á flýtiflipa eða breyting á breidd dálks í hnitaneti) eru vistaðar sjálfkrafa í núverandi yfirlit, jafnvel fyrir læst yfirlit. 

Til að tryggja að núverandi staða á yfirlitinu sé vituð, þegar byrjað er að gera breytingar á yfirliti með því að framkvæma óbeina sérstillingu eða síun, mun stjarna birtast við hliðina á heiti núverandi yfirlits sem gefur til kynna að þú ert að skoða breytta útgáfu af þessu yfirliti sem hefur ekki verið vistuð.

Ef þú vilt vista þessar breytingar skaltu fylgja þessum skrefum.
1.  Veldu heiti yfirlitsins til að opna yfirlitsvalið.
2.  Til að breyta núverandi yfirliti:
     1. Veljið **Vista**. Takið eftir að þessi aðgerð verður ekki virkjuð fyrir læst yfirlit. 
3.  Til að búa til nýtt yfirlit:
     1.    Veljið **Vista afrit**. 
     2.    Færið inn heiti yfirlits (valkvætt) og lýsingu.
     3.    Veljið **Vista**.

## <a name="changing-the-default-view"></a>Breyting á sjálfgefnu yfirliti
Sjálfgefið yfirlit er yfirlitið sem kerfið reynir að opna þegar fyrst er farið inn á síðuna. Setja ætti þetta á yfirlitið sem er búist er við að verði oftast„ notað.  

Til að breyta sjálfgefnu yfirliti fyrir síðu skal fylgja þessum skrefum: 
1.  Skiptið yfir í yfirlitið sem er notað að sjálfgefnu. 
2.  Veldu heiti yfirlitsins til að opna yfirlitsvalið. 
3.  Veljið **Fleiri** og síðan **Festa sem sjálfgefið**.  

Að öðrum kosti, þegar nýtt yfirlit er stonað (með aðgerðinni **Vista afrit**), er hægt að gera þetta nýja yfirlit að sjálfgefna yfirlitinu með því að stilla valkostinn **Festa sem sjálfgefið** áður en yfirlitið er vistað.  

Athugið að í sumum tilfellum keyrir fyrirspurnin ekki sem tengist sjálfgefnu yfirliti þegar fyrst er farið inn á síðu. Til dæmis ef farið er frá reit og yfir á síðu verður fyrirspurn reitsins keyrt óháð fyrirspurninni sem tengist sjálfgefnu yfirliti. Einnig, ef farið er á síðu þar sem klassískt yfirlit er þegar með skilgreinda fyrirspurn, mun upprunaleg fyrirspurn keyrast í stað fyrirspurnar sjálfgefins yfirlits. Þegar þetta gerist verður látið vita með upplýsandi skilaboðum þegar yfirlitið er að hlaðast inn. Að skipta milli yfirlita eftir að síðunni hefur verið hlaðið inn ætti að leyfa fyrirspurn yfirlits að keyra eins og búast má við.

## <a name="managing-personal-views"></a>Umsjón með persónulegum yfirlitum 
Svarglugginn **Stjórna yfirlitum mínum** veitir þér grunnmöguleika á umsjón með persónulegum yfirlitum þínum og röð á yfirlitum í yfirlitsvalinu. Til að opna þessa síðu skal smella á heiti yfirlits til að opna fellivalmynd yfirlitsvals og velja **Fleiri** og síðan velja **Stjórna yfirlitunum mínum**.  

Fyrir lista yfir tiltæk yfirlit fyrir þessa síðu eru eftirfarandi aðgerðarsafn í boði.  
-    **Breyta sjálfgefnu yfirliti**: Notið aðgerðina **Festa sem sjálfgefið** til að gera núgildandi undirstrikað yfirlit að sjálfgefnu yfirliti fyrir þessa síðu.  
-    **Endurraða yfirlitunum þínum**: Notið aðgerðirnar **Færa upp** og **Færa niður** til að endurraða yfirlitunum þínum í ákveðna röð.  
-    **Endurnefna yfirlit**: Notið aðgerðina **Endurnefna** til að breyta heiti á núverandi undirstrikuðu persónulegu yfirliti. Slökkt er á þessari aðgerð fyrir læst yfirlit. 
-    **Eyða yfirliti**: Notið aðgerðina **Fjarlægja** til að fjarlægja fyrir fullt og allt núverandi undirstrikað yfirlit af síðunni. Það er engin leið til að endurheimta yfirlit eftir að það er fjarlægt.  

Allar breytingar gerðar á þessum svarglugga taka gildi eftir að hnappurinn **Vista** er valinn.

## <a name="managing-personalizations-at-an-organizational-level-with-views"></a>Stjórnun sérstillinga á fyrirtækisstigi með yfirlitum
Til að skilja endurbætur í stjórnun sérstillinga á fyrirtækisstigi skulum við fyrst kíkja á stjórnun á sérstillingum gekk fyrir sig á undan yfirlitum.  

Án yfirlita notuðu stjórnendur sett af sérstillingum fyrir síðu handa notanda eða hóp notenda í gegnum síðuna Sérstillingar. Ef þessir notendur voru með sérstillingarheimildir tóku sérstillingarnar gildi á þessari síðu. Hinsvegar var enginn möguleiki á því að koma í veg fyrir að notendur sérstilltu síðuna enn frekar, sem þýddi að fyrirtækið gat ekki tryggt að samræmi væri á notandaviðmóti notenda. Ef einhver þessara notenda var ekki með heimildir til sérstillinga voru sérstillingar sem stjórnandi veitti þeim ekki hlaðnar inn. Ennfremur, ef nýir notendur voru ráðnir inn í fyrirtæki, þurftu stjórnendur að hlaða inn handvirkt safni af sérstillingum fyrir notendurna. Ekkert sérstakt sjálfvirkt ferli var til staðar sem tilgreindi að ákveðið safn sérstillinga ætti að vera í boði fyrir notendur í því hlutaverki.

Með eiginleika fyrir vistun yfirlita, er fyrirtækisstjórnun á sérstillingum umtalsvert auðveldari, þá sérstaklega vegna möguleikans á því að gefa yfirlit út til öryggishlutverka. Eftir að yfirlit hefur verið gefið út, hefur hvaða notandi sem er með það hlutverk aðgang að og getur notað yfirlitið, burtséð frá möguleikum notanda til að gera sérstillingar. Þótt hver notandi sé með afrit af útgefnu yfirliti þar sem síðunotkun (óbeinar sérstillingar) eru sjálfkrafa notuð, getur enginn notandi vistað sérstakar sérstillingar eða uppfærslur á fyrirspurninni til útgefna yfirlitsins (sem þýðir að útgefin yfirlit eru læst). Að auki, ef nýjum notendum eru gefin hlutverk sem yfirlitið var gefið út til, munu þeir sjálfkrafa sjá yfirlitin sem tengjast hlutverkum þeirra án nokkurrar aðgerðar frá stjórnandanum. Svipað, ef notandi breytir hlutverkum í fyrirtæki, yfirlitin sem tengjast gamla hlutverkinu verða ekki lengur aðgengileg notanda, aftur án nokkurrar aðgerðar frá stjórnandanum. Uppfærslur á útgefnu yfirliti er auðveldlega hægt að úthluta til notenda með því að endurútgefa yfirlitið til viðeigandi öryggishlutverka.

Útgáfumöguleikinn gerir fyrirtækjum kleift að skilgreina stöðluð yfirlit stofnunar sem eru aðlöguð að rekstrinum, beint að notendum í tilteknum öryggishlutverkum.  

## <a name="publishing-views"></a>Birta yfirlit
Meðan á birtingarferlinu stendur er hægt að úthluta yfirlitum á eitt eða fleiri öryggishlutverk, sem þýðir að notandi með þetta hlutverk hefur aðgang að og getur notað þetta yfirlit, þótt hann geti ekki breytt yfirlitinu. Eins og er hafa aðeins kerfisstjórar réttindi til aðgerðarinn **Birta** aðgerð í fellivalmyndinni Skoða skjáinn, en nýtt öryggishlutverk verður tiltækt í framtíðaruppfærslu til að veita öðrum traustum notendum útgáfurétt.  

Til að birta yfirlit skal fylgja þessum skrefum: 
1.  Búið til og vistið persónulegt afrit af yfirlitinu sem á að birta. 
2.  Með þetta yfirlit að hlaðast inn skal velja heiti yfirlits til að opna fellivalmynd yfirlitsvals. 
3.  Veljið hnappinn **Fleiri** og veljið síðan **Birta**. Svargluggi birtingar opnast.  
4.  Útbúið heiti og (valkvætt) lýsingu á yfirlitinu. Þetta er heitið sem notendur, sem fá þetta yfirlit, munu sjá í yfirlitsvalinu. Athugið að engin tvítekin heiti fyrir birt yfirlit eru leyfð fyrir síðu, jafnvel þótt listinn yfir hlutverk sem þeim er ætlað séu ólík.  
5.  Bætið við öllum öryggishlutverkum sem samsvara notendunum sem fá þetta yfirlit.  
6.  Velja **Birta**.

Athugið að í sumum umhverfum getur tekið smástund (allt að klukkustund) áður en notendur sjá birt yfirlit.

## <a name="modifying-a-published-view"></a>Breyta útgefnu yfirliti
Eftir að yfirlit er gefið út getur verið að þú uppgötvir að þig langi til að gera breytingar á útgefnu yfirlit. Þótt þú getir ekki breytingar í rauntíma á birtu yfirliti, vegna þess að þessi yfirlit eru læst fyrir breytingar fyrir alla notendur (þ.á.m. útgefendur), geturðu endurútgefið yfirlit til að gera uppfærslur.  

Ef breytingarnar sem þú vilt gera á útgefnu yfirliti eiga einungis við um færibreytur útgáfunnar (heiti og lýsing á yfirliti eða öryggishlutverkum sem yfirlitið birtist fyrir), skal gera eftirfarandi: 
1.  Skiptið yfir í útgefið yfirlit fyrir færibreyturnar sem á að uppfæra. 
2.  Veljið **Birta** úr fellivalmynd yfirlitsvals. 
3.  Veljið **Já** ef á að uppfæra núverandi yfirlit (eða **Nei** ef á að birta þetta undir öðru heiti).
4.  Uppfærið heitið, lýsingu og/eða öryggishlutverk fyrir yfirlitið. 
5.  Velja **Birta**. 
6.  Ef heitið á birta yfirlitinu var uppfært þarf einnig að eyða birta yfirlitinu með gamla heitinu (sjá hlutann **Stjórnun birtra yfirlita** fyrir frekari upplýsingar). 

Ef breytingarnar á birtu yfirliti fela í sér breytingu á sérstillingum eða síum sem tengjast yfirlitinu skal fylgja þessum skrefum: 
1.  Skiptið yfir í útgefið yfirlit sem á að breyta. 
2.  Vistið afrit af útgefnu yfirliti til að búa til staðbundin drög að útgefnu yfirliti. 
3.  Breytið staðbundnum drögum með nauðsynlegum breytingum.
4.  Birtið yfirlitið með upprunalega heitinu. 

## <a name="managing-published-views"></a>Umsjón með birtum yfirlitum
Líkt og með stjórnun á persónulegum yfirlitum gefur svarglugginn **Stjórna yfirlitunum mínum** notendum með réttindi til að birta einfalda möguleika á umsjón með birtum yfirlitum þessarar síðu (ásamt eigin persónulegum yfirlitum). Til að opna þessa síðu skal velja heiti yfirlits til að opna fellivalmynd yfirlitsvals og velja **Fleiri** og síðan velja **Stjórna yfirlitunum mínum**.

Á meðan allir notendur sjá flipann **Yfirlitin mín** sem sýna persónuleg yfirlit, geta notendur með réttindi til að birta einnig séð flipann **Útgefið** sem sýnir öll útgefnu yfirlitin fyrir þessa síðu. Vegna þess að það geta verið nokkrir notendur að gefa út yfirlit, er mikilvægt að geta stjórnað heildarlistanum yfir birt yfirlit, burtséð frá því hvort þú varst notandinn sem gafst út yfirlitið.

Fyrir listann yfir öll birt yfirlit fyrir þessa síðu eru eftirfarandi sett af aðgerðum tiltæk. 

-    **Birta**: Notið aðgerðina **Birta** til að endurbirta yfirlit með breyttum færibreytum birtingar (heiti, lýsing, öryggishlutverk).  
-    **Fjarlægja**: Notið aðgerðina **Fjarlægja** til að fjarlægja að fullu birt yfirlit. Þessi aðgerð fjarlægir yfirlitið hjá öllum notendum í kerfinu.  
 
Allar breytingar gerðar á þessum svarglugga taka gildi eftir að hnappurinn **Vista** er valinn.

## <a name="frequently-asked-questions"></a>Algengar spurningar
### <a name="how-do-i-enable-saved-views-in-my-environment"></a>Hvernig virkja ég vistuð yfirlit í umhverfinu mínu? 
Fylgdu skrefunum hér fyrir neðan til að gera vistaðar skoðanir virkar meðan aðgerðin er í forskoðun: 

1.  **Virkja flugið**: Framkvæma eftirfarandi SQL staðhæfingu: 

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, enabled, FLIGHTSERVICEID, PARTITION) VALUES('CLISavedViewsEnableFeature', 1, 0, 5637144576);`

2. **Núllstilla IIS** til að skola fast flýtiminni. 

3.  **Finndu eiginleikann**: Farðu í vinnusvæði **Stjórnun eiginleika**. Ef **Vistaðar skoðanir** birtist ekki á listanum velurðu hnappinn **Leita að uppfærslum**.   

4.  **Virkja aðgerðina**: Finndu aðgerðina **Vistaðar skoðanir** á listanum yfir aðgerðir og veldu hnappinn **Virkja núna** á smáatriðinu.

Allar síðari notendatímabil munu byrja með vistaðar skoðanir virka.  

Athugið að ef slökkt er á sérstillingu fyrir umhverfið verða yfirlit afvirkjuð jafnvel þótt þú fylgir skrefunum hér að ofan. Ástæðan er vegna þess að eiginleiki yfirlita er byggður ofan á undirkerfi sérstillingar.

### <a name="what-happens-to-existing-personalizations-when-views-are-enabled"></a>Hvað verður um núverandi sérstillingar þegar yfirlit eru virkjuð? 
Þegar yfirlit eru virkjuð eru allar núverandi sérstillingar fyrir notanda og skjámynd vistaðar í nýtt yfirlit sem ber heitið **Yfirlitið mitt** sem er sjálfkrafa stillt sem sjálfgefið yfirlit. Þetta er til að tryggja að samræmi í notendaupplifun áður og eftir að yfirlit eru virkjuð, fyrir utan stjórnun yfirlitsvals sem birtist í skjámyndum.  

### <a name="what-pages-support-views"></a>Hvaða síður styðja yfirlit? 
Yfirlit eru tiltæk á flestum en ekki öllum síðum Finance and Operations. Nánar tiltekið eru yfirlit tiltæk sem stendur á síðum sem fylla allan skjáinn fyrir utan yfirlitssvæði og vinnusvæði. Síður sem fylla ekki út í allan skjáinn, sem eru svargluggar, fellilistar svarglugga, uppflettingar, endurbættar forskoðanir, styðja einnig ekki yfirlit. Stuðningur fyrir yfirlit fyrir aðrar síðugerðir, t.d. vinnusvæði og svarglugga, verður hugsanlega tekinn til greina fyrir framtíðaruppfærslu.   

### <a name="who-is-allowed-to-publish-views"></a>Hver má birta yfirlit?
Sem stendur hafa aðeins kerfisstjórar réttindi til að birta yfirlit.  Nýtt öryggishlutverk er áætlað í framtíðaruppfærslu, sem gæfi viðskiptavinum aukinn sveigjanleika hvað varðar hver megi birta yfirlit.  

### <a name="why-am-i-not-able-to-save-filters-with-this-view"></a>Af hverju get ég ekki vistað síur með þessu yfirliti? 
Það eru nokkrar ástæður fyrir því að sía virðist ekki vistast með yfirliti: 

- Hugsanlega styður síðan ekki vistun á síum sem hluti af skilgreiningu yfirlits. Athugið að aðeins síður með stórt yfirlitsval leyfir að vista í yfirliti breytingar á sérstillingum og fyrirspurn. Sjá hlutann „Skipt á milli yfirlita“ fyrir frekari upplýsingar. 

- Ef yfirlitið er sjálfgefið yfirlit og slóðin að síðunni inniheldur fyrirspurn kann að vera að fyrirspurn yfirlitsins verði ekki notað í upphafi. Tvær helstu atburðarásirnar fyrir þetta eru: 
     - Ef farið er á síðu frá reit verður fyrirspurn reitsins keyrð óháð fyrirspurninni sem tengist sjálfgefnu yfirliti. 
     - Ef farið er á síðu og sá upphafspunktur inniheldur fyrirspurn, mun upprunaleg fyrirspurn keyrast í stað fyrirspurnar sjálfgefins yfirlits. 
     
  Þú ættir að fá viðvörun þegar þessar aðstæður koma upp á með upplýsandi skilaboðum þegar yfirlitið er að hlaðast. Einnig er hægt að staðfesta með því að skipta yfir í þetta yfirlit eftir að síðan hleðst inn, því að þetta ætti að leyfa keyrslu á fyrirspurn yfirlits óháð öðru.  

- Umrædd blaðsíða styður ef til vill ekki viðhorf á réttan hátt, þar sem hún getur hunsað fyrirspurnina að fullu eða kann að starfa á tímabundinni töflu þar sem gögn eru ekki viðvarandi. 
