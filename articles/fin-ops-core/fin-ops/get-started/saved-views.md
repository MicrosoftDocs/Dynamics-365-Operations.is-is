---
title: Vistuð yfirlit
description: Þetta efnisatriði lýsir því hvernig á að nota eiginleika fyrir vistuð yfirlit.
author: jasongre
manager: AnnBe
ms.date: 07/29/2020
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
ms.openlocfilehash: a190e2a117c3209993926af0a7bf031909b8ee0f
ms.sourcegitcommit: 27233e0fda61dac541c5210ca8d94ab4ba74966f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/03/2020
ms.locfileid: "3651643"
---
# <a name="saved-views"></a>Vistuð yfirlit

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

## <a name="introduction"></a>Inngangur

Sérstilling gegnir mikilvægu hlutverki í því að gera notendum og fyrirtækjum kleift að hámarka notendaupplifun til að mæta þörfum þeirra. Frekari upplýsingar um sérstillingu er að finna í [Sérsníða notandaupplifun](personalize-user-experience.md).

Hefðbundin sérstilling leyfir notendum að hafa aðeins eitt safn af sérstillingum á hverri síðu. Eiginleikinn **Vistuð yfirlit** víkkar út sérstillingu á nokkra mikilvæga vegu:

- Yfirlit leyfa notendum að hafa sett sérstillinga með mörgum heitum fyrir hverja skjámynd, sem hægt er að fara á milli á fljótlegan hátt eftir þörfum. Þetta gerir notanda kleift að búa til mörg aðlöguð yfirlit fyrir síðu, þar sem hvert yfirlit hefur verið sniðið að þörfum þess að geta framkvæmt ákveðið viðskiptatengt verkefni. 
- Yfirlit búin til fyrir sérstakar gerðir af síðum geta einnig innihaldið síur eða flokkanir sem notandi bætir við, sem gerir notendum kleift að snúa sér fljótt að algengum síuðum gagnasöfnum. Sjá hlutann [Hvaða síður styðja yfirlit](saved-views.md#what-pages-support-views) fyrir frekari upplýsingar. 
- Hægt er að birta skoðanir til notenda í sérstökum öryggishlutverkum og sérstökum lögaðilum. Þess vegna geta allir notendur sem hafa tiltekið hlutverk og aðgang að tilgreindum lögaðila opnað og notað það yfirlit, jafnvel þótt að slíkur notandi hafi ekki heimild til að sérsníða. Þessi útgáfumöguleiki leyfir fyrirtækjum að skilgreina stöðluð yfirlit stofnunar sem eru aðlöguð að rekstrinum. Nánari upplýsingar er að finna í hlutanum [Stjórnun sérstillinga á fyrirtækisstigi með yfirlitum](saved-views.md#managing-personalizations-at-an-organizational-level-with-views).
- Ólíkt hefðbundinni sérstillingu eru yfirlit ekki vistuð sjálfkrafa þegar notandi framkvæmir sérstillingar eða síar lista. Að vista sérstaklega er nauðsynlegt til að veita notendum þann sveigjanleika til að búa til yfirlit fyrir eða eftir breytingarnar sem tengjast því yfirliti hafa verið gerðar. Þessi krafa tryggir einnig að skilgreiningum yfirlita sé ekki óvart breytt af síum eða sérstillingum sem eru ekki ætlaðar til langtímanotkunar. Atriði sem kerfið vistar sjálfkrafa sem hluta af dæmigerðri síðunotkun (til dæmis dálkabreiddir, eða útvíkkuð eða samandregin staða svæða) verða vistuð fyrir hvert yfirlit.
- Hægt er að bæta skoðunum við vinnusvæðin sem reitum, listum eða tenglum. Þess vegna getur síað gagnasafn komið upp á vinnusvæði og notendur geta tengt safn sérstillinga sem eiga við um það gagnasafn með reit eða tengli.

## <a name="switching-between-views"></a>Skipta á milli yfirlita

Þegar yfirlit hafa verið gerð aðgengileg fyrir umhverfi mun efsti hluti hverrar síðu sem styður yfirlit innihalda samandregna stjórnun á yfirlitsvali sem sýnir heiti á núverandi yfirliti.

Til eru tvær stærðir á yfirlitsvali: 

- **Stórt yfirlitsval** - Síður sem birta lista á áberandi hátt verða með stærra yfirlitsval af nokkrum ástæðum. Mikilvægast er að stærra yfirlitsvalið gefur til kynna síðurnar þar sem yfirlitið getur innihaldið síur skilgreindar af notanda. Vegna þess að síur eru innifaldar í yfirlitunum, stærra yfirlitsvalið er einnig leyft sem yfirlit, verða heiti oft besta lýsing á gögnunum sem eru sýnd á skjánum og búist er við því að notendur muni skipta á milli yfirlita oftar á þessum síðugerðum.
- **Lítið yfirlitsval**: Allar aðrar skjámyndir með heilli síðu (fyrir utan vinnusvæði og stjórnborðið) eru með minna yfirlitsval sem sést við hliðina á yfirskrift síðunnar. Yfirlit á þessum síðum fela eingöngu í sér sérstillingar, ekki síur skilgreindar af notanda. Á þessum síðum er yfirskriftin eða titill færslu oft mikilvægustu upplýsingarnar efst á síðunni. Minni stærð yfirlitsvalsins endurspeglar einnig færri skiptingar milli yfirlita sem búist er við á þessum síðum. 
 
Ef heiti yfirlits er valið opnast yfirlitsvalið og sýnir lista yfir tiltæk yfirlit fyrir síðuna.

- **Staðlað Yfirlit** – **Staðlaða** yfirlitið er tilbúið yfirlit síðunnar, þar sem engar sérstillingar eru gerðar.
- **Persónulegt yfirlit** - Yfirlit án hengiláss standa fyrir persónulegu yfirlitin þín. Þetta eru yfirlit sem þú hefur annaðhvort búið til eða stjórnandi hefur gefið þér þau.
- **Læst yfirlit**: Sum yfirlit (eins og **Staðlaða** yfirlitið og öll yfirlit sem eru gefin út fyrir hlutverkið þitt) eru með hengilástákn við hliðina á þeim í yfirlitsvalinu. Þetta tákn gefur til kynna að þú getur ekki breytt þessum yfirlitum. Hins vegar verða breytingar sem endurspegla síðunotkun sjálfkrafa vistaðar. Þessar breytingar fela í sér breytingar á breidd dálka í hnitaneti og breytingar á útvíkkaðri og samandreginni stöðu flýtiflipa. Engu að síður, ef þú ert með sérstillingaréttindi geturðu notað aðgerðina **Vista sem** til að gera persónulegt yfirlit sem er byggt á læstu yfirliti.
- **Ný yfirlit**: Birt yfirlit sem hafa ekki enn verið opnuð eru með neistatákni vinstra megin við heiti yfirlitsins.

Til að skipta yfir í annað yfirlit skal fyrst opna yfirlitsvalið og síðan velja yfirlitið sem á að hlaða inn. 

## <a name="creating-and-modifying-views"></a>Búa til og breyta yfirlitum

Ólíkt hefðbundinni sérstillingu eru yfirlit ekki sjálfkrafa vistuð þegar notandi sérstillir síðuna eða þegar notandi notar síu á lista eða raðar honum. Þörf er á sérstakri aðgerð til að vista þessar breytingar í yfirliti. Krafan veitir notendum þann sveigjanleika til að búa til yfirlit fyrir eða eftir að breytingarnar sem tengjast því yfirliti hafa verið gerðar. Hún tryggir einnig að skilgreiningum yfirlita sé ekki óvart breytt vegna síu eða sérstillinga sem eru notaðar í eitt skipti. Athugið að dæmigerð atriði síðunotkunar (til dæmis dálkabreiddir, eða útvíkkuð eða samandregin staða svæða) eru sjálfkrafa vistuð í núverandi yfirliti, m.a.s. fyrir læst yfirlit.

Til að tryggja að núverandi staða yfirlitsins sé þekkt, þegar byrjað er að breyta yfirliti með því að sérstilla það eða sía, birtist stjarna (\*) við hliðina á heiti núverandi yfirlits. Þetta tákn gefur til kynna að þetta sé óvistuð, breytt útgáfa af þessu yfirliti.

Ef þú vilt vista þessar breytingar skaltu fylgja þessum skrefum.

1. Veldu heiti yfirlitsins til að opna yfirlitsvalið.
2. Til að breyta núverandi yfirliti skal velja **Vista**. Athugið að þessi aðgerð er ekki tiltæk fyrir læst yfirlit. 
3. Til að búa til nýtt yfirlit:

    1. Veljið **Vista sem**. 
    2. Færið inn heiti yfirlits (valkvætt) og lýsingu.
    3. Veljið **Vista**.

## <a name="changing-the-default-view"></a>Breyting á sjálfgefnu yfirliti

Sjálfgefið yfirlit er yfirlitið sem kerfið reynir að opna þegar síðan er opnuð. Stilla ætti sjálfgefna yfirlitið sem er búist er við að verði oftast notað. 

> [!NOTE]
> Það er eitt, altækt sjálfgefið yfirlit yfir öll fyrirtæki. Ef sjálfgefna yfirlitinu er breytt, verður það yfirlit opnað að sjálfgefnu, óháð lögaðilanum sem er notaður hverju sinni. 

Til að breyta sjálfgefnu yfirliti fyrir síðu skal fylgja þessum skrefum:

1. Skiptið yfir í yfirlitið sem er notað að sjálfgefnu. 
2. Veldu heiti yfirlitsins til að opna yfirlitsvalið. 
3. Veljið **Fleiri** og síðan **Festa sem sjálfgefið**.

Að öðrum kosti, þegar nýtt yfirlit er stonað (með aðgerðinni **Vista sem**), er hægt að gera þetta nýja yfirlit að sjálfgefna yfirlitinu með því að stilla valkostinn **Festa sem sjálfgefið** áður en yfirlitið er vistað.

Athugið að í sumum tilfellum keyrir fyrirspurnin ekki sem tengist sjálfgefnu yfirliti þegar síða er opnuð í fyrsta skipti. Til dæmis ef síðan er opnuð í gegnum reit, verður fyrirspurn reitsins keyrð, óháð fyrirspurninni sem tengist sjálfgefna yfirlitinu. Þar að auki, ef síða er opnuð sem er með **Staðlað** yfirlit sem er þegar með skilgreinda fyrirspurn, verður upprunalega fyrirspurnin keyrð í staðinn fyrir fyrirspurn sjálfgefna yfirlitsins. Í slíku tilfelli birtist upplýsingaboð þegar yfirlitinu er hlaðið inn. Ef skipt er á milli yfirlita eftir að síðunni hefur verið hlaðið inn, ætti fyrirspurn um yfirlit að geta keyrt eðlilega. Í útgáfu 10.0.10 og síðar verða upplýsingaboðin sem birtast með innfelldri aðgerð sem gerir kleift að hlaða beint inn fyrirspurn sjálfgefins yfirlits.

## <a name="managing-personal-views"></a>Umsjón með persónulegum yfirlitum

Svarglugginn **Stjórna yfirlitum mínum** veitir þér grunnmöguleika á umsjón með persónulegum yfirlitum þínum og röð á yfirlitum í yfirlitsvalinu. Til að opna þessa síðu skal velja heiti yfirlits til að opna fellivalmynd yfirlitsvals og velja **Fleiri** og síðan velja **Stjórna yfirlitunum mínum**.

Fyrir lista yfir tiltæk yfirlit fyrir þessa síðu eru eftirfarandi aðgerðarsafn í boði.

- **Breyta sjálfgefnu yfirliti** - Notið aðgerðina **Festa sem sjálfgefið** til að gera núgildandi valið yfirlit að sjálfgefnu yfirliti fyrir þessa síðu.
- **Endurraða yfirlitunum þínum** - Notið aðgerðirnar **Færa upp** og **Færa niður** til að endurraða yfirlitunum þínum í ákveðna röð.
- **Endurnefna yfirlit** - Notið aðgerðina **Endurnefna** til að breyta heiti á núverandi völdu persónulegu yfirliti. Slökkt er á þessari aðgerð fyrir læst yfirlit. 
- **Eyða yfirliti**: Notið aðgerðina **Eyða** til að eyða fyrir fullt og allt valið yfirlit af síðunni. Það er engin leið til að endurheimta yfirlit eftir að það er fjarlægt.

Allar breytingar gerðar á þessum svarglugga taka gildi eftir að hnappurinn **Vista** er valinn.

## <a name="managing-personalizations-at-an-organizational-level-with-views"></a>Stjórnun sérstillinga á fyrirtækisstigi með yfirlitum

Til að skilja betur hvernig vistuð yfirlit hjálpa til við stjórnun sérstillinga á fyrirtækisstigi, útskýrir þessi hluti nokkra ólíka þætti í stjórnun sérstillinga með og án eiginleikans **Vistuð yfirlit**.

Án yfirlita notuðu stjórnendur sett af sérstillingum fyrir síðu handa notanda eða hóp notenda í gegnum síðuna Sérstillingar. Ef þessir notendur voru með sérstillingarheimildir tóku sérstillingarnar gildi á þessari síðu. Hinsvegar var enginn möguleiki á því að koma í veg fyrir að notendur sérstilltu síðuna enn frekar, sem þýddi að fyrirtækið gat ekki tryggt að samræmi væri á notandaviðmóti notenda. Ef einhver þessara notenda var ekki með heimildir til sérstillinga voru sérstillingar sem stjórnandi veitti þeim ekki hlaðnar inn. Ennfremur, ef nýir notendur voru ráðnir inn í fyrirtæki, þurftu stjórnendur að hlaða inn handvirkt safni af sérstillingum fyrir notendurna. Ekkert sérstakt sjálfvirkt ferli var til staðar sem tilgreindi að ákveðið safn sérstillinga ætti að vera í boði fyrir notendur í því hlutaverki.

Eiginleikinn **Vistuð yfirlit** gerir fyrirtækisstjórnun á sérstillingum mun auðveldari, aðallega vegna þess að hægt verður að birta hópum notenda yfirlit. Eftir að yfirlit hefur verið birt, getur notandi sem er með eitt af skilgreindum öryggishlutverkum og aðgangsheimild að tilteknum lögaðilum séð og notað yfirlitið, jafnvel þótt sá notandi hafi ekki aðgang að sérstillingum. Þótt sérhver notandi sé með afrit af birtu yfirliti, þar sem atriði síðunotkunar eru sjálfkrafa sett á, getur enginn notandi vistað uppfærslur á sérstillingum eða fyrirspurn á birt yfirlit. Með öðrum orðum, birt yfirlit eru læst. Þar að auki, ef nýjum notendum er úthlutað hlutverkum í lögaðilum sem yfirlitin voru birt fyrir, sjá þeir sjálfkrafa yfirlitin sem tengjast hlutverkum sínum og lögaðilum. Ekki er þörf á viðbótaraðgerðum af stjórnandanum. Sömuleiðis, ef notendur skipta um hlutverk í stofnun eða fá aðgang að mismunandi lögaðilum, gætu þeir ekki lengur haft aðgang að þeim yfirlitum sem áður voru birt þeim. Aftur er engin viðbótaraðgerð nauðsynleg frá stjórnandanum.

Uppfærslur á útgefnu yfirliti er auðveldlega hægt að úthluta til notenda með því að endurútgefa yfirlitið til viðeigandi öryggishlutverka og lögaðila.

Útgáfumöguleikinn gerir fyrirtækjum kleift að skilgreina stöðluð yfirlit stofnunar sem eru aðlöguð að rekstrinum, beint að notendum í tilteknum öryggishlutverkum.

## <a name="publishing-views"></a>Birta yfirlit

Í birtingarferlinu er hægt að úthluta yfirlitum á eitt eða fleiri öryggishlutverk fyrir einn eða fleiri lögaðila. Þess vegna getur sérhver notandi, sem hefur aðgang að lögaðila og er úthlutað á eitt þessara hlutverka, opnað og notað yfirlitin. Notandinn getur hins vegar ekki breytt yfirlitum. Kerfisstjórar hafa sjálfgefin aðgang á aðgerðinni **Birta** í fellivalmynd yfirlitsvals. Hins vegar geta aðrir traustir notendur í fyrirtækinu fengið aðgang að því að skoða útgáfu með nýja hlutverkinu **Stjórnandi vistaðra yfirlita**.

Til að birta yfirlit skal fylgja þessum skrefum:

1. Búið til og vistið persónulegt afrit af yfirlitinu sem á að birta. 
2. Með þetta yfirlit að hlaðast inn skal velja heiti yfirlits til að opna fellivalmynd yfirlitsvals. 
3. Veljið hnappinn **Fleiri** og veljið síðan **Birta**. Svargluggi birtingar opnast.
4. Sláðu inn heiti og (valkvætt) lýsingu á yfirlitinu. Heitið sem þú slærð inn er heitið sem notendur, sem fá þetta yfirlit, munu sjá í yfirlitsvalinu. Nöfn birtra skoðana fyrir síðu verða að vera einstök. Engin tvítekin heiti eru leyfð, jafnvel þótt listinn yfir hlutverk eða lögaðila sem yfirlitunum er beitt á séu ólík.
5. **Útgáfa 10.0.9 og nýrri:** Ákveðið hvort birta eigi yfirlitið sem sjálfgefið yfirlit fyrir valda notendur. Þegar yfirlit er gert að sjálfgefnu yfirliti, sjá notendur það í næsta skipti sem þeir opna marksíðuna. Einu, altæku sjálfgefnu yfirliti fyrir hvern valinn notanda verður breytt. Hins vegar geta notendur ennþá breytt sjálfgefnu yfirliti sínu eftir birtingu.
6. Bættu öryggishlutverkum við sem samsvara notendunum sem fá þetta yfirlit. 
7. **Útgáfa 10.0.13 og nýrri:** Ákveðið hvort birta eigi yfirlitin undirhlutverkum fyrir hvert öryggishlutverk sem er valið. Ef það er gert skal velja gátreitinn **Hafa með undirhlutverk** í línunni fyrir viðeigandi öryggishlutverk. Athugið að þessi gátreitur er ekki tiltækur fyrir hlutverk sem eru ekki með undirhlutverk.
7. Bættu við lögaðilum sem þetta yfirlit ætti að vera tiltækt fyrir. 
8. Velja **Birta**.

Athugið að í sumum umhverfum getur tekið smástund (allt að klukkustund) áður en notendur sjá birt yfirlit.

> [!NOTE]
> Hafa skal eftirfarandi væntingar í huga þegar lögaðila er birt yfirlit, eða þegar yfirlit er birt sem sjálfgefið yfirlit.
> - Ef öllum eða sumum lögaðilum er birt yfirlit sem sjálfgefið yfirlit, er einu, altæku sjálfgefnu yfirliti breytt fyrir alla valda notendur. Ef notandi er með hlutverk þar sem mörg yfirlit eru birt sem sjálfgefið yfirlit, verður síðasta yfirlitið sem birtist notað sjálfgefið yfirlit notandans. 
> - Ef yfirlit er birt í lögaðila, en það er ekki birt sem sjálfgefið yfirlit, sjá notendur yfirlitið fyrst í yfirlitsvalinu aðeins fyrir tilgreinda lögaðila. Hinsvegar, þegar yfirlitinu er hlaðið inn í fyrsta skipti, verður það alltaf í yfirlitsvali notandans fyrir þá síðu, óháð lögaðilanum. 

## <a name="modifying-a-published-view"></a>Breyta útgefnu yfirliti

Eftir að yfirlit er birt þarf hugsanlega að breyta því. Þótt ekki sé hægt að gera breytingar í rauntíma á birtu yfirliti, vegna þess að þessi yfirlit eru læst fyrir breytingar fyrir alla notendur (þ.á.m. útgefendur), er hægt að endurbirta yfirlit til að uppfæra það.

Ef breytingarnar sem þú vilt gera á útgefnu yfirliti eiga einungis við um færibreytur útgáfunnar (heiti og lýsing á yfirliti eða öryggishlutverkum sem yfirlitið birtist fyrir), skal gera eftirfarandi:

1. Skiptið yfir í útgefið yfirlit fyrir færibreyturnar sem á að uppfæra. 
2. Í fellivalmynd yfirlitsvalsins skal velja **Endurbirta**. Ef verið er að nota útgáfu 10.0.12 eða eldri, þarf að velja **Birta** og síðan **Já** til að uppfæra fyrirliggjandi yfirlit.
3. Uppfærið heiti, lýsingu, öryggishlutverk og lögaðila fyrir yfirlitið. 
4. Velja **Birta**. 
5. **Útgáfa 10.0.8 og eldri:** Ef heiti birts yfirlits var uppfært, þarf einnig að eyða birtu yfirliti sem er með gamla heitið. (Frekari upplýsingar er að finna í [Umsjón með birtum yfirlitum](saved-views.md#managing-published-views).)

**Útgáfa 10.0.9 og nýrri:** Ef þetta birta yfirlit var upphaflega valið sem sjálfgefið yfirlit, verður það aftur sjálfgefið yfirlit fyrir notendur eftir endurbirtingu.

Ef breytingarnar á birtu yfirliti fela í sér breytingu á sérstillingum eða síum sem tengjast yfirlitinu skal fylgja þessum skrefum: 

**Útgáfa 10.0.13 og nýrri:** Gerið nauðsynlegar breytingar beint á yfirlitinu. Stjarna (\*) á að birtast við hliðina á heiti yfirlitsins.

1. Hlaðið birtu yfirliti sem ætlunin er að breyta. 
2. Gerið nauðsynlegar breytingar á staðbundnum drögum.
3. Í fellivalmynd yfirlitsvalsins skal velja **Endurbirta**.
4. Veljið **Já** til að gefa til kynna að birta eigi yfirlitið ásamt óvistuðum breytingum þess. 
5. Breytið öllum birtingarfæribreytum sem þarfnast leiðréttingar og veljið svo **Birta**. 

**Útgáfa 10.0.12 og nýrri**

1. Hlaðið útgefnu yfirliti sem á að breyta. 
2. Vistið afrit af útgefnu yfirliti til að búa til staðbundin drög að útgefnu yfirliti. 
3. Breytið staðbundnum drögum með nauðsynlegum breytingum.
4. Birtið yfirlitið með upprunalega heitinu. 

## <a name="managing-published-views"></a>Umsjón með birtum yfirlitum

Líkt og með stjórnun á persónulegum yfirlitum gefur svarglugginn **Stjórna yfirlitunum mínum** notendum með réttindi til að birta einfalda möguleika á umsjón með birtum yfirlitum þessarar síðu (ásamt eigin persónulegum yfirlitum). Til að opna þessa síðu skal velja heiti yfirlits til að opna fellivalmynd yfirlitsvals og velja **Fleiri** og síðan velja **Stjórna yfirlitunum mínum**.

Þótt allir notendur séu með **Mín yfirlit** flipa sem sýnir þeirra eigin yfirlit, eru notendur með réttindi til birtingar einnig með **Yfirlit fyrirtækis** flipa sem sýnir öll birt og óbirt yfirlit fyrir þá síðu. Þar sem ýmsir notendur gætu verið að birta yfirlit, er mikilvægt að geta haft umsjón með heildarlistanum yfir birt yfirlit, jafnvel þótt þú sért ekki notandinn sem birti tiltekið yfirlit.

Fyrir listann yfir öll birt yfirlit fyrir þessa síðu eru eftirfarandi sett af aðgerðum tiltæk. 

- **Endurbirta** - Notið aðgerðina **EndurbirtaBirta** til að endurbirta yfirlit eftir að færibreytum birtingar (heiti, lýsing, öryggishlutverk eða lögaðilar) hefur verið breytt.
- **Birta** – Notið aðgerðina **Birta** til að birta yfirlit sem er óbirt sem stendur. 
- **Taka úr birtingu** – Notið aðgerðina **Taka úr birtingu** til að gera yfirlit óvirkt. Yfirlitið verður enn til staðar í kerfinu, en notendur sjá það ekki í yfirlitsvalinu fyrr en yfirlitið er birt á nýjan leik.
- **Vista sem eigið** - Notið aðgerðina **Vista sem eigið** til að búa til eigin drög af birtu yfirliti. Þessi möguleiki getur varpað betra ljósi á innihald yfirlits sem var ekki birt notanda eða sem hefur ekki verið birt að svo stöddu. Einnig er hægt að nota hann til að breyta og birta svo aftur yfirlit. Þessi hæfileiki er kynntur í útgáfu 10.0.12.
- **Eyða** - Notið aðgerðina **Eyða** til að eyða birtu eða óbirtu yfirliti fyrir fullt og allt. Þessi aðgerð fjarlægir líka yfirlitið hjá öllum notendum í kerfinu. Fjarlæging á birtum yfirlitum tekur gildi eftir að hnappurinn **Vista** er valinn. Eftir að yfirliti er eytt er ekki hægt að endurheimta það. 

## <a name="managing-views-globally"></a>Stjórna yfirlitum á altækan hátt

Þrátt fyrir að einhverjir stjórnunarmöguleikar komi fram á öllum síðum eins og minnst er á í þessu efnisatriði, geta **kerfisstjórar** og **vistað yfirlit kerfisstjóra** haft betri yfirsýn yfir stjórnun yfirlita fyrir kerfið í gegnum síðuna **Sérstillingar**. Einkum hefur þessi síða eftirfarandi hluta og möguleika: 

- **Birt yfirlit** - Þessi hluti sýnir öll yfirlit sem hafa verið birt fyrir fyrirtækið. Héðan er hægt að endurbirta yfirlit þegar öryggishlutverkum eða lögaðilum hefur verið breytt sem yfirlitið hefur augastað á. Einnig er hægt að flytja út, eyða eða taka yfirlit úr birtingu. Í útgáfu 10.0.12 og síðar er hægt að nota aðgerðina **Vista sem eigið** til að búa til eigið afrit af yfirlitinu til að geta uppfært yfirlitið eða öðlast betri skilning á efni þess. 
- **Óbirt yfirlit** – Þessi hluti sýnir öll yfirlit fyrirtækis í kerfinu sem ekki eru þegar birt. Þessi yfirlit koma oftast inn í kerfið í gegnum innflutningsmöguleikann. Þú getur birt, flutt út eða eytt þessum skoðunum. Aðgerðin **Flýtibirting** sem var bætt við í útgáfu 10.0.12 býður upp á að birta mörg yfirlit úr þessum hluta í einni aðgerð með því að nota fyrirliggjandi skilgreiningar öryggishlutverks og lögaðila. Í útgáfu 10.0.12 og síðar er hægt að nota aðgerðina **Vista sem eigið** til að búa til eigið afrit af þessum yfirlitum til að öðlast betri skilning á efni þeirra.
- **Eigin yfirlit** – Þessi hluti sýnir öll yfirlit sem notendur hafa búið til í kerfinu. Héðan er hægt að birta persónulegt yfirlit til stofnunar/fyrirtækis eða afrita eitt eða fleiri af þessum yfirlitum til annarra notenda. Einnig er hægt að birta, flytja út eða eyða þessum skoðunum, eftir þörfum.
- **Notandastillingar** – Veljið notanda til að skoða, eða breytið getu notandans til að nota sérstillingu annaðhvort fyrir allt kerfið eða tilteknar síður sem notandinn hefur heimsótt. Hægt er að skoða og hafa umsjón með sérstillingum notanda í kerfinu. Einnig er hægt að eyða öllum sérstillingum fyrir þann notanda eða endurstilla skýringartexta eiginleika fyrir notandann. Ef skýringartextar eiginleika eru endurstilltir, birtast aftur sprettigluggar sem kynntu nýja eiginleika til sögunnar og sem notandinn hafnaði áður í næsta skipti sem notandinn sér slíka eiginleika.
- **Kerfisstillingar** - Hægt er að slökkva á öllum sérstillingum fyrir alla notendur kerfisins. Í slíku tilfelli eru engar sérstillingar notaðar fyrir neinn notanda og allar síður eru endurstilltar í sjálfgefna stöðu. Ef þú kveikir aftur á sérstillingum verður öllum sérstillingumaftur beitt. Einnig er hægt að eyða öllum sérstillingum endanlega fyrir alla notendur kerfisins. Ekki er hægt að endurheimta sérstillingar sem hefur verið eytt. Áður en þú framkvæmir þetta verkefni skaltu þess vegna vera viss um að flytja út allar sérstillingar sem þú gætir viljað síðar.

Notendur sem hafa aðgang að síðunni **Sérstilling** geta einnig flutt inn eigin yfirlit eða yfirlit fyrirtækis með því að nota hnappinn **Flytja inn yfirlit** á aðgerðasvæðinu. Í útgáfu 10.0.12 og síðar hefur fyrirkomulagi verið bætt við til að birta yfirlit um leið og þau eru flutt inn.

## <a name="known-issues"></a>Þekkt vandamál
Listi yfir þekkt vandamál með vistuð yfirlit er að finna í [Búa til skjámyndir sem nýta vistuð yfirlit til fullnustu](../../dev-itpro/user-interface/understanding-saved-views.md).

## <a name="frequently-asked-questions"></a>Algengar spurningar

### <a name="how-do-i-enable-saved-views-in-my-environment"></a>Hvernig virkja ég vistuð yfirlit í umhverfinu mínu?

> [!NOTE]
> Eiginleikinn **Vistuð yfirlit** krefst þess að sérsniðna kerfið í Finance and Operations verði virkjað. Ef slökkt er á sérstillingu fyrir allt umhverfið verða yfirlit afvirkjuð jafnvel þótt þú fylgir skrefunum hér að neðan. 

**Útgáfa 10.0.13 og nýrri**

Eiginleikinn **Vistuð yfirlit** er ekki lengur í forskoðun. Hann er nú í boði beint í gegnum eiginleikastjórnun í hvaða umhverfi sem er.

**Útgáfur 10.0.9 til 10.0.12**

Eiginleikinn **Vistuð yfirlit** er í boði í eiginleikastjórnun í hvaða umhverfi sem er. Líkt og með aðra forútgáfueiginleika, heyrir virkjun þessa eiginleika í framleiðslu undir [Viðbótarnotkunarskilmálar](https://go.microsoft.com/fwlink/?linkid=2105274).

**10.0.8 / Verkvangsuppfærsla 32 og eldri**

Hægt er að virkja eiginleikann **Vistuð yfirlit** í lagi 1 (þróun/prófun) og lagi 2 (sandkassa) umhverfi til að geta veitt frekari prófun og hönnun á breytingum með því að fylgja skrefunum hér á eftir.

1. **Virkja flugið**: Framkvæma eftirfarandi SQL staðhæfingu: 

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, enabled, FLIGHTSERVICEID, PARTITION) VALUES('CLISavedViewsEnableFeature', 1, 0, 5637144576);`

2. **Núllstilla IIS** til að skola fast flýtiminni. 
3. **Finndu eiginleikann**: Farðu í vinnusvæði **Stjórnun eiginleika**. Ef **Vistaðar skoðanir** birtist ekki á listanum velurðu hnappinn **Leita að uppfærslum**.
4. **Virkja aðgerðina**: Finndu aðgerðina **Vistaðar skoðanir** á listanum yfir aðgerðir og veldu hnappinn **Virkja núna** á smáatriðinu.

Allar síðari notendatímabil munu byrja með vistaðar skoðanir virka.

### <a name="what-happens-to-existing-personalizations-when-views-are-enabled"></a>Hvað verður um núverandi sérstillingar þegar yfirlit eru virkjuð? 

Þegar yfirlit eru virkjuð eru allar núverandi sérstillingar fyrir notanda og skjámynd vistaðar í nýtt yfirlit sem ber heitið **Yfirlitið mitt** sem er sjálfkrafa stillt sem sjálfgefið yfirlit. Þetta er til að tryggja að samræmi í notendaupplifun áður og eftir að yfirlit eru virkjuð, fyrir utan stjórnun yfirlitsvals sem birtist í skjámyndum.

### <a name="what-pages-support-views"></a>Hvaða síður styðja yfirlit? 

Yfirlit eru tiltæk á flestum en ekki öllum síðum. Nánar tiltekið eru yfirlit tiltæk sem stendur á síðum sem fylla allan skjáinn fyrir utan yfirlitssvæði og vinnusvæði. Síður sem fylla ekki út í allan skjáinn, sem eru svargluggar, fellilistar svarglugga, uppflettingar, endurbættar forskoðanir, styðja ekki yfirlit. Stuðningur fyrir yfirlit fyrir aðrar síðugerðir, t.d. vinnusvæði og svarglugga, verður hugsanlega tekinn til greina fyrir framtíðaruppfærslu.

### <a name="who-is-allowed-to-publish-views"></a>Hver má birta yfirlit?

Aðeins kerfisstjórar og notendur sem hefur verið úthlutað á hlutverkið **Stjórnandi vistaðra yfirlita** hafa réttindi til að birta yfirlit. 

### <a name="why-am-i-not-able-to-save-filters-with-this-view"></a>Af hverju get ég ekki vistað síur með þessu yfirliti? 

Það eru nokkrar ástæður fyrir því að sía virðist ekki vistast með yfirliti: 

- Hugsanlega styður síðan ekki vistun á síum sem hluti af skilgreiningu yfirlits. Athugið að aðeins síður með stórt yfirlitsval leyfir að vista í yfirliti breytingar á sérstillingum og fyrirspurn. Sjá hlutann **Skipt á milli yfirlita** fyrir frekari upplýsingar. 
- Umrædd blaðsíða styður ef til vill ekki viðhorf á réttan hátt, þar sem hún getur hunsað fyrirspurnina að fullu eða kann að starfa á tímabundinni töflu þar sem gögn eru ekki viðvarandi. 

### <a name="what-data-will-i-see-when-i-visit-a-page"></a>Hvaða gögn mun ég sjá þegar ég heimsæki síðu?

Fyrir síður sem eru með lítið yfirlitsval (aðeins er hægt að vista sérstillingar í yfirlitið), sjást sömu gögn eins og eru alltaf til staðar þegar síðan er opnuð. 

Fyrir síður sem eru með stórt yfirlitsval (bæði er hægt að vista sérstillingar og fyrirspurnir í yfirlitið), sjást venjulega gögnin sem eru tengd við fyrirspurnina sem tengist sjálfgefna yfirlitinu. Til eru tvær undantekningar:

- Ef farið er á síðu frá reit verður fyrirspurn reitsins keyrð óháð fyrirspurninni sem tengist sjálfgefnu yfirliti. Ef þú stofnaðir þann reit eftir að skoðanir hafa verið virkjaðar mun val á reit opna síðuna með skjánum sem tengist þeim reit.
- Ef farið er á síðu og sá upphafspunktur inniheldur fyrirspurn, mun upprunaleg fyrirspurn keyra í stað fyrirspurnar sjálfgefins yfirlits. Þú ættir að vera látin/n vita þegar þetta gerist með upplýsandi skilaboðum þegar yfirlitið er að hlaðast inn. Einnig er hægt að staðfesta með því að skipta yfir í þetta yfirlit eftir að síðan hleðst inn, því að þetta ætti að leyfa keyrslu á fyrirspurn yfirlits óháð öðru.
