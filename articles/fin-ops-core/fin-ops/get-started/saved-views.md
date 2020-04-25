---
title: Vistuð yfirlit
description: Þetta efnisatriði lýsir því hvernig á að nota eiginleika fyrir vistuð yfirlit.
author: jasongre
manager: AnnBe
ms.date: 04/10/2020
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
ms.openlocfilehash: fe79558b9d2ac4ef1c83918b949d11983b2cc0d8
ms.sourcegitcommit: cd8a28be0acf31c547db1b8f6703dd4b0f62940c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/14/2020
ms.locfileid: "3260484"
---
# <a name="saved-views"></a>Vistuð yfirlit

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

## <a name="introduction"></a>Inngangur
Sérstilling gegnir mikilvægu hlutverki í því að gera notendum og fyrirtækjum kleift að hámarka notendaupplifun til að mæta þörfum þeirra. Frekari upplýsingar um sérstillingu er að finna í [Sérsníða notandaupplifun](personalize-user-experience.md).

Með hefðbundinni sérstillingu gátu notendur aðeins verið með eitt sett af sérstillingum fyrir hverja skjámynd. Vistuð yfirlit víkka út sérstillingu á nokkra mikilvæga vegu:

-    Yfirlit leyfa notendum að hafa sett sérstillinga með mörgum heitum fyrir hverja skjámynd, sem hægt er að fara á milli á fljótlegan hátt eftir þörfum. Þetta gerir notanda kleift að búa til mörg aðlöguð yfirlit fyrir síðu, þar sem hvert yfirlit hefur verið sniðið að þörfum þess að geta framkvæmt ákveðið viðskiptatengt verkefni. 

-    Yfirlit búin til fyrir sérstakar gerðir af síðum geta einnig innihaldið síur eða flokkanir sem notandi bætir við, sem gerir notendum kleift að snúa sér fljótt að algengum síuðum gagnasöfnum. Sjá hlutann [Hvaða síður styðja yfirlit](saved-views.md#what-pages-support-views) fyrir frekari upplýsingar. 

-    Hægt er að birta skoðanir til notenda í sérstökum öryggishlutverkum og sérstökum lögaðilum. Þess vegna getur hver notandi sem hefur tiltekið hlutverk í og aðgang að tilteknum lögaðila fengið aðgang að og notað þá skoðun, jafnvel þó að sá notandi gæti ekki getað sérsniðið það. Þessi útgáfumöguleiki leyfir fyrirtækjum að skilgreina stöðluð yfirlit stofnunar sem eru aðlöguð að rekstrinum. Nánari upplýsingar er að finna í hlutanum [Stjórnun sérstillinga á fyrirtækisstigi með yfirlitum](saved-views.md#managing-personalizations-at-an-organizational-level-with-views).

-    Ólíkt hefðbundinni sérstillingu eru yfirlit ekki vistuð sjálfkrafa þegar notandi framkvæmir ákveðnar sérstillingar eða síanir á lista. Ákveðnar vistanir eru nauðsynlegar til að bjóða upp á sveigjanleika við stofnun á yfirliti á undan eða eftir breytingarnar sem tengjast þessu yfirliti hafa verið gerðar og til að tryggja að skilgreiningar yfirlits hafi ekki óvart verið breytt með síum eða sérstillingum sem ekki eru ætlaðar til langtímanotkunar.  

-    Hægt er að bæta skoðunum við vinnusvæðin sem reitum, listum eða tenglum. Þess vegna er hægt að koma afmörkuðu gagnasafni yfir á vinnusvæði og notendur geta tengt safn sérstillinga sem eru viðeigandi fyrir það gagnasett við reitinn eða hlekkinn.

## <a name="switching-between-views"></a>Skipta á milli yfirlita
Þegar yfirlit hafa verið virkjuð fyrir umhverfi munu allar síður sem styðja yfirlit innihalda samandregna stjórnun á yfirlitsvali efst í skjámyndinni sem sýnir heiti á núverandi yfirliti.  

Til eru tvær stærðir á yfirlitsvali: 

-   **Stórt yfirlitsval**: Síður sem birta lista á áberandi hátt verða með stærra yfirlitsval af nokkrum ástæðum. Mikilvægast er að stærra yfirlitsvalið gefur til kynna síðurnar þar sem yfirlitið getur innihaldið síur skilgreindar af notanda. Vegna þess að síur eru innifaldar í yfirlitunum, stærra yfirlitsvalið er einnig leyft sem yfirlit, verða heiti oft besta lýsing á gögnunum sem eru sýnd á skjánum og búist er við því að notendur muni skipta á milli yfirlita oftar á þessum síðugerðum.  
 
-   **Lítið yfirlitsval**: Allar aðrar skjámyndir með heilli síðu (undantekningin er vinnusvæði og yfirlitið) eru með minna yfirlitsval sem sést við hliðina á yfirskrift síðunnar. Yfirlit á þessum síðum innihalda eingöngu sérstillingar (en ekki síur skilgreindar af notanda). Á þessum síðum er yfirskrift skjámyndar eða titill færslu oft mikilvægustu upplýsingarnar efst á skjámyndinni. Minni stærðin endurspeglar einnig að búist sé við færri skiptingum á milli yfirlita á þessum síðum. 
 
Ef smellt er á heiti yfirlits opnast yfirlitsvalið og sýnir lista yfir tiltæk yfirlit fyrir þessa síðu

-    **Staðlað yfirlit**: **Staðlað** yfirlit (áður þekkt sem **Klassískt** yfirlit) er forsniðið yfirlit á síðunni þar sem ekki er beitt beinum sérstillingum.
-    **Persónulegt yfirlit**: Yfirlit án hengiláss standa fyrir persónulegu yfirlitin þín. Þetta eru yfirlit sem þú hefur annaðhvort búið til eða stjórnandi hefur gefið þér þau.  
-    **Læst yfirlit**: Sum yfirlit (eins og **Staðlað** yfirlit og öll yfirlit sem eru birt í hlutverki þínu) eru með hengilásartákn við hliðina á yfirlitsvalinu. Þetta tákn gefur til kynna að þú getur ekki breytt þessum yfirlitum. Samt sem áður eru óbeinar sérstillingar sem endurspegla síðunotkun vistaðar sjálfkrafa. Þessar óbeinu sérstillingar fela í sér breytingu á breidd hnitanets eða stækkun eða minnkun flýtiflipa. Engu að síður, ef þú ert með sérstillingaréttindi geturðu notað aðgerðina **Vista sem** til að gera persónulegt yfirlit sem er byggt á læstu yfirliti.
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
     1.    Veljið **Vista sem**. 
     2.    Færið inn heiti yfirlits (valkvætt) og lýsingu.
     3.    Veljið **Vista**.

## <a name="changing-the-default-view"></a>Breyting á sjálfgefnu yfirliti
Sjálfgefið yfirlit er yfirlitið sem kerfið reynir að opna þegar fyrst er farið inn á síðuna. Setja ætti þetta á yfirlitið sem er búist er við að verði oftast„ notað.  

Til að breyta sjálfgefnu yfirliti fyrir síðu skal fylgja þessum skrefum: 
1.  Skiptið yfir í yfirlitið sem er notað að sjálfgefnu. 
2.  Veldu heiti yfirlitsins til að opna yfirlitsvalið. 
3.  Veljið **Fleiri** og síðan **Festa sem sjálfgefið**.  

Að öðrum kosti, þegar nýtt yfirlit er stonað (með aðgerðinni **Vista sem**), er hægt að gera þetta nýja yfirlit að sjálfgefna yfirlitinu með því að stilla valkostinn **Festa sem sjálfgefið** áður en yfirlitið er vistað.

Athugið að í sumum tilfellum keyrir fyrirspurnin ekki sem tengist sjálfgefnu yfirliti þegar fyrst er farið inn á síðu. Til dæmis ef farið er frá reit og yfir á síðu verður fyrirspurn reitsins keyrt óháð fyrirspurninni sem tengist sjálfgefnu yfirliti. Einnig, ef farið er á síðu með staðlað yfirlit sem er þegar með skilgreinda fyrirspurn, mun upprunaleg fyrirspurn keyrast í stað fyrirspurnar sjálfgefins yfirlits. Þegar þetta gerist verður látið vita með upplýsandi skilaboðum þegar yfirlitið er að hlaðast inn. Að skipta milli yfirlita eftir að síðunni hefur verið hlaðið inn ætti að leyfa fyrirspurn yfirlits að keyra eins og búast má við. Byrjað er á útgáfu 10.0.10 pallborðsuppfærslu 34, upplýsingaskilaboðin eru með innfelld aðgerð sem gerir þér kleift að hlaða fyrirspurn sjálfgefins skjás beint.

## <a name="managing-personal-views"></a>Umsjón með persónulegum yfirlitum 
Svarglugginn **Stjórna yfirlitum mínum** veitir þér grunnmöguleika á umsjón með persónulegum yfirlitum þínum og röð á yfirlitum í yfirlitsvalinu. Til að opna þessa síðu skal smella á heiti yfirlits til að opna fellivalmynd yfirlitsvals og velja **Fleiri** og síðan velja **Stjórna yfirlitunum mínum**.  

Fyrir lista yfir tiltæk yfirlit fyrir þessa síðu eru eftirfarandi aðgerðarsafn í boði.  
-    **Breyta sjálfgefnu yfirliti**: Notið aðgerðina **Festa sem sjálfgefið** til að gera núgildandi undirstrikað yfirlit að sjálfgefnu yfirliti fyrir þessa síðu.  
-    **Endurraða yfirlitunum þínum**: Notið aðgerðirnar **Færa upp** og **Færa niður** til að endurraða yfirlitunum þínum í ákveðna röð.  
-    **Endurnefna yfirlit**: Notið aðgerðina **Endurnefna** til að breyta heiti á núverandi undirstrikuðu persónulegu yfirliti. Slökkt er á þessari aðgerð fyrir læst yfirlit. 
-    **Eyða yfirliti**: Notið aðgerðina **Fjarlægja** til að fjarlægja fyrir fullt og allt núverandi undirstrikað yfirlit af síðunni. Það er engin leið til að endurheimta yfirlit eftir að það er fjarlægt.  

Allar breytingar gerðar á þessum svarglugga taka gildi eftir að hnappurinn **Vista** er valinn.

## <a name="managing-personalizations-at-an-organizational-level-with-views"></a>Stjórnun sérstillinga á fyrirtækisstigi með yfirlitum
Til að hjálpa þér að skilja hvernig vistuð yfirlit hjálpa til við að bæta stjórnun á sérstillingum á skipulagsstigi, lýsir þessi hluti mismun á sérstillingastjórnun með eða án eiginleika vistaðra skjáyfirlita.

Án yfirlita notuðu stjórnendur sett af sérstillingum fyrir síðu handa notanda eða hóp notenda í gegnum síðuna Sérstillingar. Ef þessir notendur voru með sérstillingarheimildir tóku sérstillingarnar gildi á þessari síðu. Hinsvegar var enginn möguleiki á því að koma í veg fyrir að notendur sérstilltu síðuna enn frekar, sem þýddi að fyrirtækið gat ekki tryggt að samræmi væri á notandaviðmóti notenda. Ef einhver þessara notenda var ekki með heimildir til sérstillinga voru sérstillingar sem stjórnandi veitti þeim ekki hlaðnar inn. Ennfremur, ef nýir notendur voru ráðnir inn í fyrirtæki, þurftu stjórnendur að hlaða inn handvirkt safni af sérstillingum fyrir notendurna. Ekkert sérstakt sjálfvirkt ferli var til staðar sem tilgreindi að ákveðið safn sérstillinga ætti að vera í boði fyrir notendur í því hlutaverki.

Eiginleikinn fyrir vistun yfirlita gerir fyrirtækisstjórnun á sérstillingum umtalsvert auðveldari, þá sérstaklega vegna þess að hægt er að gefa yfirlit út til hópta notenda. Eftir að yfirlit hefur verið birt mun sérhver notandi sem hefur eitt af skilgreindum öryggishlutverkum og hefur aðgang að tilgreindum lögaðilum geta séð og notað yfirlitið, jafnvel þó að notandinn geti ekki sérstillt það. Þótt hver notandi sé með afrit af útgefnu yfirliti þar sem síðunotkun (óbeinar sérstillingar) er sjálfkrafa notuð, getur enginn notandi vistað beinar sérstillingar eða uppfærslur á fyrirspurninni til útgefna yfirlitsins. Með öðrum orðum, birt yfirlit eru læst. Þar að auki, ef nýir notendur fá hlutverk í lögaðilum sem skoðanir voru birtar, munu þeir sjálfkrafa sjá skoðanirnar sem tengjast hlutverkum þeirra og lögaðilum. Engin viðbótaraðgerð er nauðsynleg frá stjórnandanum. Sömuleiðis, ef notendur skipta um hlutverk í stofnun eða fá aðgang að mismunandi lögaðilum, gætu þeir ekki lengur haft aðgang að þeim yfirlitum sem áður voru birt þeim. Aftur er engin viðbótaraðgerð nauðsynleg frá stjórnandanum.

Uppfærslur á útgefnu yfirliti er auðveldlega hægt að úthluta til notenda með því að endurútgefa yfirlitið til viðeigandi öryggishlutverka og lögaðila.

Útgáfumöguleikinn gerir fyrirtækjum kleift að skilgreina stöðluð yfirlit stofnunar sem eru aðlöguð að rekstrinum, beint að notendum í tilteknum öryggishlutverkum.  

## <a name="publishing-views"></a>Birta yfirlit
Í birtingarferlinu er hægt að úthluta yfirlitum í eitt eða fleiri öryggishlutverk fyrir einn eða fleiri lögaðila. Þess vegna getur hver notandi sem hefur aðgang að lögaðila og er úthlutað í eitt af þessum hlutverkum fengið aðgang og notað yfirlitin, þó að hann geti ekki breytt þeim. Kerfisstjórar hafa aðgang að aðgerðinni **Birta** í fellivalmynd yfirlitsvals. Hins vegar geta aðrir traustir notendur í fyrirtækinu fengið aðgang að því að skoða útgáfu með nýja hlutverkinu **Stjórnandi vistaðra yfirlita**.

Til að birta yfirlit skal fylgja þessum skrefum: 
1.  Búið til og vistið persónulegt afrit af yfirlitinu sem á að birta. 
2.  Með þetta yfirlit að hlaðast inn skal velja heiti yfirlits til að opna fellivalmynd yfirlitsvals. 
3.  Veljið hnappinn **Fleiri** og veljið síðan **Birta**. Svargluggi birtingar opnast.  
4.  Sláðu inn heiti og (valkvætt) lýsingu á yfirlitinu. Heitið sem þú slærð inn er heitið sem notendur, sem fá þetta yfirlit, munu sjá í yfirlitsvalinu. Nöfn birtra skoðana fyrir síðu verða að vera einstök. Engin tvítekin heiti eru leyfð, jafnvel þótt listinn yfir hlutverk eða lögaðila sem yfirlitunum er beitt á séu ólík.
5.  Bættu öryggishlutverkum við sem samsvara notendunum sem fá þetta yfirlit.
6. Bættu við lögaðilum sem þetta yfirlit ætti að vera tiltækt fyrir. 
7. [10.0.9/uppfærsla verkvangs 33 eða nýrri] Ákveðið hvort skoða skuli útsýnið sem sjálfgefið skjá fyrir valda notendur. Að gera yfirlit sjálfgefið þýðir að þetta er útsýnið sem notendur munu sjá næst þegar þeir opna miðasíðuna. Þetta mun breyta sjálfgefnu skjánum fyrir þessa notendur; notendur geta þó enn breytt sjálfgefnu yfirliti eftir að útgáfan hefur átt sér stað.    
8.  Velja **Birta**.

Athugið að í sumum umhverfum getur tekið smástund (allt að klukkustund) áður en notendur sjá birt yfirlit.

## <a name="modifying-a-published-view"></a>Breyta útgefnu yfirliti
Eftir að yfirlit er gefið út getur verið að þú uppgötvir að þig langi til að gera breytingar á útgefnu yfirlit. Þótt þú getir ekki breytingar í rauntíma á birtu yfirliti, vegna þess að þessi yfirlit eru læst fyrir breytingar fyrir alla notendur (þ.á.m. útgefendur), geturðu endurútgefið yfirlit til að gera uppfærslur.  

Ef breytingarnar sem þú vilt gera á útgefnu yfirliti eiga einungis við um færibreytur útgáfunnar (heiti og lýsing á yfirliti eða öryggishlutverkum sem yfirlitið birtist fyrir), skal gera eftirfarandi: 
1.  Skiptið yfir í útgefið yfirlit fyrir færibreyturnar sem á að uppfæra. 
2.  Veljið **Birta** úr fellivalmynd yfirlitsvals. 
3.  Veljið **Já** ef á að uppfæra núverandi yfirlit (eða **Nei** ef á að birta þetta undir öðru heiti).
4.  Uppfærið heitið, lýsingu og/eða öryggishlutverk fyrir yfirlitið. 
5.  Velja **Birta**. 
6.  [10.0.8/verkvangsuppfærsla 32 eða yngri] Ef heitið á birta yfirlitinu var uppfært þarf einnig að eyða birta yfirlitinu með gamla heitinu (sjá hlutann **Stjórnun birtra yfirlita** fyrir frekari upplýsingar). 
7. [10.0.9/verkvangsuppfærsla 33 eða nýrri] Ef þú hefðir upphaflega valið þessa birtu skoðun til að vera sjálfgefið yfirlit, þá verður það sjálfgefið yfirlit fyrir þessa notendur aftur eftir útgáfuna að nýju.  

Ef breytingarnar á birtu yfirliti fela í sér breytingu á sérstillingum eða síum sem tengjast yfirlitinu skal fylgja þessum skrefum: 
1.  Skiptið yfir í útgefið yfirlit sem á að breyta. 
2.  Vistið afrit af útgefnu yfirliti til að búa til staðbundin drög að útgefnu yfirliti. 
3.  Breytið staðbundnum drögum með nauðsynlegum breytingum.
4.  Birtið yfirlitið með upprunalega heitinu. 

## <a name="managing-published-views"></a>Umsjón með birtum yfirlitum
Líkt og með stjórnun á persónulegum yfirlitum gefur svarglugginn **Stjórna yfirlitunum mínum** notendum með réttindi til að birta einfalda möguleika á umsjón með birtum yfirlitum þessarar síðu (ásamt eigin persónulegum yfirlitum). Til að opna þessa síðu skal velja heiti yfirlits til að opna fellivalmynd yfirlitsvals og velja **Fleiri** og síðan velja **Stjórna yfirlitunum mínum**.

Á meðan allir notendur sjá flipann **Yfirlitin mín** sem sýna persónuleg yfirlit, geta notendur með réttindi til að birta einnig séð flipann **Útgefið** sem sýnir öll útgefnu yfirlitin fyrir þessa síðu. Vegna þess að það geta verið nokkrir notendur að gefa út yfirlit, er mikilvægt að geta stjórnað heildarlistanum yfir birt yfirlit, burtséð frá því hvort þú varst notandinn sem gafst út yfirlitið.

Fyrir listann yfir öll birt yfirlit fyrir þessa síðu eru eftirfarandi sett af aðgerðum tiltæk. 

-    **Birta**: Notið aðgerðina **Birta** til að endurbirta yfirlit eftir að færibreytum birtingar (heiti, lýsingu, öryggishlutverkum eða lögaðilum) er breytt.
-    **Fjarlægja**: Notið aðgerðina **Fjarlægja** til að fjarlægja að fullu birt yfirlit. Þessi aðgerð fjarlægir yfirlitið hjá öllum notendum í kerfinu. Ef birtar skoðanir eru fjarlægðar tekur gildi eftir að hnappurinn **Vista** er valinn.

## <a name="frequently-asked-questions"></a>Algengar spurningar
### <a name="how-do-i-enable-saved-views-in-my-environment"></a>Hvernig virkja ég vistuð yfirlit í umhverfinu mínu? 
Athugasemd: Eiginleikinn **Vistaðar skoðanir** krefst sérstillingarkerfisins í Finance and Operations til að vera virk. Ef slökkt er á sérstillingu fyrir allt umhverfið verða yfirlit afvirkjuð jafnvel þótt þú fylgir skrefunum hér að neðan. 

**10.0.9 / uppfærsla pallsins 33 og nýrri** Eiginleikinn **Vistaðar skoðanir** er fáanlegur beint í lögun stjórnun í hvaða umhverfi sem er. Eins og aðrir opnir forskoðunareiginleikar, þá er það kleift að virkja þennan eiginleika í framleiðslu [Viðbótarskilmálar um notkunarskilmála](https://go.microsoft.com/fwlink/?linkid=2105274).  

**10.0.8 / uppfærsla verkvangs 32 og yngri** Eiginleikinn **Vistuð yfirlit** er hægt að virkja í umhverfi 1. lagi (þróun/prófun) og 2. lagi (sandkassi) til að veita frekari prófunar- og hönnunarbreytingar með því að fylgja skrefunum hér að neðan.

1.  **Virkja flugið**: Framkvæma eftirfarandi SQL staðhæfingu: 

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, enabled, FLIGHTSERVICEID, PARTITION) VALUES('CLISavedViewsEnableFeature', 1, 0, 5637144576);`

2. **Núllstilla IIS** til að skola fast flýtiminni. 

3.  **Finndu eiginleikann**: Farðu í vinnusvæði **Stjórnun eiginleika**. Ef **Vistaðar skoðanir** birtist ekki á listanum velurðu hnappinn **Leita að uppfærslum**.   

4.  **Virkja aðgerðina**: Finndu aðgerðina **Vistaðar skoðanir** á listanum yfir aðgerðir og veldu hnappinn **Virkja núna** á smáatriðinu.

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
Fyrir síður með litla skjávalda (aðeins er hægt að vista persónusnið á skjánum) munt þú sjá sömu gögn og þú hefur alltaf þegar þú heimsækir síðuna. 

Fyrir síður með stóra skjávalda (sérsniðnar og fyrirspurnir er hægt að vista á skjánum) sérðu fyrst og fremst gögnin sem tengjast fyrirspurninni sem tengist sjálfgefnu skjánum. Það eru tvær aðalundantekningar á þessu: - Ef farið er á síðu frá reit verður fyrirspurn reitsins keyrð óháð fyrirspurninni sem tengist sjálfgefnu yfirliti. Ef þú stofnaðir þann reit eftir að skoðanir hafa verið virkjaðar mun val á reit opna síðuna með skjánum sem tengist þeim reit.   
     - Ef farið er á síðu og sá upphafspunktur inniheldur fyrirspurn, mun upprunaleg fyrirspurn keyra í stað fyrirspurnar sjálfgefins yfirlits. Þú ættir að vera látin/n vita þegar þetta gerist með upplýsandi skilaboðum þegar yfirlitið er að hlaðast inn. Einnig er hægt að staðfesta með því að skipta yfir í þetta yfirlit eftir að síðan hleðst inn, því að þetta ætti að leyfa keyrslu á fyrirspurn yfirlits óháð öðru.  


