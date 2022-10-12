---
title: Yfirlit yfir samþættingu ríkisfjármála fyrir viðskiptarásir
description: Þessi grein veitir yfirlit yfir samþættingargetu í ríkisfjármálum sem eru tiltækar í Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 10/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 1812405db3c1e58eaf7cd1df3896f786e7bf026f
ms.sourcegitcommit: 2bc6680dc6b12d20532d383a0edb84d180885b62
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/06/2022
ms.locfileid: "9631241"
---
# <a name="fiscal-integration-overview-for-commerce-channels"></a>Yfirlit yfir samþættingu ríkisfjármála fyrir viðskiptarásir

[!include [banner](../includes/banner.md)]

Þessi grein er yfirlit yfir samþættingargetu í ríkisfjármálum sem eru tiltækar í Dynamics 365 Commerce. 

Fjárhagssamþætting felur í sér samþættingu við ýmis fjárhagstæki og þjónustu sem gerir kleift að skrá sölu í samræmi við staðbundin fjárhagslög sem miða að því að koma í veg fyrir skattsvik í smásöluiðnaðinum. Hér eru nokkrar dæmigerðar aðstæður sem hægt er að dekka með því að nota fjárhagssamþættingu:

- Skrá sölu á fjármálatæki sem tengist sölustað (POS), svo sem strimlaprentara og prentun á fjármálakvittun fyrir viðskiptavin.
- Senda inn upplýsingar á öruggan hátt sem tengjast sölu og skilum sem er lokið í Retail POS til utanaðkomandi vefþjónustu sem er starfrækt af skattyfirvöldum.
- Hjálpaðu til við að tryggja óbreytanleika sölugagnagagna með stafrænum undirskriftum.

Virkni fjárhagssamþættingar er rammi sem veitir algenga lausn fyrir frekari þróun og sérstillingu á samþættingunni milli Retail POS og fjárhagstæki og þjónustu. Virknin felur einnig í sér sýnishorn fjárhagssamþættingar sem styður einfaldar aðstæður fyrir tilgreind lönd eða svæði, og sem vinna með tiltekin fjárhagstæki og þjónustu. Sýnishorn fjárhagssamþættingar samanstendur af nokkrum viðbótum af Commerce-íhlutum og er hluti af þróunarpakka hugbúnaðarins (SDK). Nánari upplýsingar um sýnishorn fjárhagssamþættingar er að finna í [Sýnishorn fjárhagssamþættingar í Commerce SDK](#fiscal-integration-samples-in-the-commerce-sdk). Upplýsingar um hvernig skuli setja upp og nota Commerce SDK er að finna í [Hugbúnaðarþróunarpakki fyrir Retail (SDK)](../dev-itpro/retail-sdk/retail-sdk-overview.md).

Til að styðja við aðrar aðstæður sem ekki eru studdar af sýnishorni fjárhagssamþættingar, til að samþætta Retail POS við önnur fjárhagstæki eða þjónustur, eða til að ná utan um kröfur annarra landa eða svæða, verður þú annaðhvort að stækka núverandi sýnishorn fjárhagssamþættingar eða stofna nýtt sýnishorn með því að nota núverandi sýnishorn sem dæmi.

## <a name="fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services"></a>Fjárhagsskráningarferli og sýnishorn af samþættingu ríkisfjármála fyrir ríkisfjármálatæki og þjónustu

Fjárhagsskráningarferli í Retail POS getur samanstaðið af einu eða fleiri skrefum. Hvert skref felur í sér fjárhagsskráningu á tilteknum færslum eða tilvikum í einu fjárhagstæki eða þjónustu. Eftirfarandi lausnarþættir taka þátt í skattaskráningu í fjárhagslegu tæki eða þjónustu:

- **Útgefandi ríkisfjármálaskjala** – Þessi hluti raðnúmerar færslu/atburðargögn á því sniði sem einnig er notað fyrir samskipti við fjárhagslega tækið eða þjónustuna, greinir svör frá fjárhagslega tækinu eða þjónustunni og geymir svörin í rásargagnagrunninum. Viðbótin skilgreinir einnig tilgreindar færslur og tilvik sem þarf að skrá.
- **Fjárhagstengi** – Þessi hluti frumstillir samskiptin við fjárhagslega tækið eða þjónustuna, sendir beiðnir eða beinar skipanir til fjárhagsbúnaðarins eða þjónustunnar, byggt á færslu/atburðargögnum sem eru dregin út úr fjárhagsskjalinu, og tekur við svörum frá fjárhagslega tækinu eða þjónustunni.

Fjárhagslegt samþættingarsýni gæti innihaldið Commerce runtime (CRT), Vélbúnaðarstöð og POS-viðbætur fyrir fjárhagsskjalaveitu og fjárhagstengi. Það inniheldur einnig eftirfarandi stillingar hlutar:

- **Stilling fjárhagsskjalsveitu** - Þessi stilling skilgreinir úttaksaðgerð á sniði fyrir fjárhagsskjöl. Það inniheldur einnig gagnakortlagningu fyrir skatta og greiðslumáta, til að gera gögn frá Retail POS samhæf við þau gildi sem eru fyrirfram skilgreind í fjárhagslegu tækinu eða þjónustufastbúnaðinum.
- **Stilling fjárhagstengis** – Þessi uppsetning skilgreinir líkamleg samskipti við tiltekið fjárhagslega tæki eða þjónustu.

Fjárhagsskráningarferli fyrir tiltekinn afgreiðslukassa er skilgreint af samsvarandi stillingu í virknireglu sölustaðar. Fyrir frekari upplýsingar um hvernig á að stilla fjárhagsskráningarferli, hlaða upp fjárhagsskjalaveitu og stillingum fjárhagstengis og breyta stillingarbreytum, sjá [Settu upp fjárhagslega skráningarferli](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

> [!NOTE]
> Ef þú þarft tæki fyrir aðgerðir sem ekki eru í ríkisfjármálum, eins og vörulistaleit, uppflettingu viðskiptavina eða gerð færsludröga, geturðu valið þau sem skrár með takmarkanir á fjárhagsferli. Fyrir frekari upplýsingar, sjá [Settu upp skrár með takmarkanir á skattaskráningu](setting-up-fiscal-integration-for-retail-channel.md#set-up-registers-with-fiscal-registration-restrictions).

Eftirfarandi dæmigert fjárhagsskráningarflæði byrjar á atburði í POS (til dæmis frágangi sölufærslu) og útfærir fyrirfram skilgreinda röð skrefa sem felur í sér aðra viðskiptaþætti (svo sem CRT og vélbúnaðarstöð).

1. POS óskar eftir fjárhagsskjali frá fjárhagslegum samþættingarramma (FIF).
1. FIF ákvarðar hvort núverandi atburður krefjist ríkisskráningar.
1. Byggt á stillingum fyrir fjárhagsskráningarferlið auðkennir FIF fjárhagstengi og samsvarandi fjárhagsskjalaveitu til að nota fyrir fjárhagsskráninguna.
1. FIF rekur fjárhagsskjalaveituna sem býr til fjárhagsskjal (til dæmis XML skjal) sem táknar færsluna eða atburðinn.
1. FIF skilar útbúnu fjárhagsskjali til POS.
1. POS fer fram á að FIF afhendi fjárhagsskjalið til fjármálafyrirtækisins eða þjónustunnar.
1. FIF rekur fjárhagslega tengið sem vinnur úr fjárhagsskjalinu og sendir það til fjárhagslega tækisins eða þjónustunnar.
1. FIF skilar fjárhagslega svarinu (þ.e. svari fjárhagslega tækisins eða þjónustunnar) til POS.
1. POS greinir fjárhagsviðbrögðin til að ákvarða hvort fjárhagsskráningin heppnaðist. Eins og krafist er, biður POS um að FIF höndli allar villur sem áttu sér stað. 
1. POS fer fram á að FIF afgreiði og visti viðbrögð við ríkisfjármálum.
1. Fjárhagsskjalaveitan vinnur úr fjárhagssvarinu. Sem hluti af þessari vinnslu greinir útgefandi fjárhagsskjala svarið og dregur út víðtæk gögn úr því.
1. FIF vistar svarið og útvíkkuð gögn í rásargagnagrunninn.
1. Eftir þörfum prentar POS kvittun í gegnum venjulegan kvittunarprentara sem er tengdur við vélbúnaðarstöð. Kvittunin getur innihaldið nauðsynleg gögn úr fjárhagssvarinu.
 
Eftirfarandi dæmi sýna framkvæmdarflæði fjárhagsskráningar fyrir dæmigerð fjárhagslega tæki eða þjónustu.
 
### <a name="fiscal-registration-is-done-via-a-device-connected-to-the-hardware-station"></a>Skattskráning fer fram í gegnum tæki sem er tengt við Vélbúnaðarstöð

Þessi stilling er notuð þegar líkamlegt fjárhagslegt tæki, svo sem fjárhagsprentari, er tengt við vélbúnaðarstöðina. Það á einnig við þegar samskipti við ríkisfjármálatæki eða þjónustu fara fram í gegnum hugbúnað sem er uppsettur á vélbúnaðarstöðinni. Í þessu tilviki er útgefandi fjárhagsskjala staðsettur á CRT, og fjárhagstengið er staðsett á vélbúnaðarstöðinni.

![Fjárhagsskráning fer fram í gegnum tæki sem er tengt við Vélbúnaðarstöð.](media/FIF-CRT-HWS.png)

### <a name="fiscal-registration-is-done-via-an-external-service"></a>Skráning ríkisfjármála fer fram í gegnum utanaðkomandi þjónustu

Þessi stilling er notuð þegar skattskráning fer fram í gegnum ytri þjónustu, svo sem vefþjónustu sem er rekin af skattyfirvöldum. Í þessu tilviki eru bæði útgefandi fjárhagsskjala og fjárhagstengi staðsett á CRT.

![Skattskráning fer fram í gegnum utanaðkomandi þjónustu.](media/FIF-CRT-CRT.png)
 
### <a name="fiscal-registration-is-done-internally-in-the-crt"></a>Skráning ríkisfjármála fer fram innbyrðis í CRT

Þessi uppsetning er notuð þegar ekkert utanaðkomandi fjárhagslegt tæki eða þjónustu er krafist fyrir fjárhagsskráningu. Til dæmis er það notað þegar fjárhagsleg skráning er gerð með stafrænni undirritun sölufærslur. Í þessu tilviki eru bæði útgefandi fjárhagsskjala og fjárhagstengi staðsett á CRT.

![Skráning ríkisfjármála fer fram innbyrðis í CRT.](media/FIF-CRT-CRT-SGN.png)

### <a name="fiscal-registration-is-done-via-a-device-or-service-in-the-local-network"></a>Skattskráning fer fram í gegnum tæki eða þjónustu á staðarnetinu

Þessi stilling er notuð þegar fjárhagslegt tæki eða fjárhagsþjónusta er til staðar á staðarneti verslunarinnar og veitir HTTPS forritunarviðmót (API). Í þessu tilviki er útgefandi fjárhagsskjala staðsettur á CRT, og fjárhagstengi er staðsett á POS.

![Skattskráning fer fram í gegnum tæki eða þjónustu á staðarnetinu.](media/FIF-CRT-POS.png)

## <a name="error-handling"></a>Villumeðhöndlun

Þessi rammi fjárhagssamþættingar veitir eftirfarandi valmöguleika til að takast á við villur við fjárhagsskráningu:

- **Reyndu aftur** – Rekstraraðili getur notað þennan valkost þegar hægt er að leysa bilunina fljótt og hægt er að keyra fjárhagsskráninguna aftur. Til dæmis er hægt að nota þennan valkost þegar fjárhagstækið er ekki tengt, strimlaprentarinn er án pappírs, eða prentarinn er stíflaður.
- **Hætta við** – Þessi valkostur gerir rekstraraðila kleift að fresta fjárhagsskráningu núverandi færslu eða atburðar ef hún mistekst. Eftir að skráningu hefur verið frestað getur rekstraraðilinn haldið áfram að vinna á POS og getur lokið hvaða aðgerð sem er sem fjárhagsskráning er ekki nauðsynleg fyrir. Þegar einhver tilvik sem krefjast fjárhagsskráningar eiga sér stað á sölustaðnum (til dæmis ef ný færsla er opnuð) birtist villuglugginn sjálfkrafa til að tilkynna notanda að fyrri færsla hafi ekki verið skráð rétt og býður upp á valmöguleika til að meðhöndla villuna.
- **Sleppa** – Rekstraraðili getur notað þennan valmöguleika þegar ekki er hægt að ljúka fjárhagsskráningu núverandi færslu eða atburðar, til dæmis ef fjárhagsprentari er bilaður, **og** sleppa má skattskráningu að uppfylltum sérstökum skilyrðum. Til dæmis er hægt að nota þennan valmöguleika þegar hægt er að skrá sölufærslu sem fjárhagsskráningin mistókst fyrir í sérstakri færslubók á pappír. Eftir að hafa sleppt skattskráningu er hægt að halda áfram reglulegri starfsemi á POS. 
- **Merktu sem skráð** – Rekstraraðili getur notað þennan valmöguleika þegar núverandi færsla eða atburður hefur í raun verið skráður í fjárhagslega tækinu, til dæmis hefur fjárhagskvittun verið prentuð, en bilun kemur upp þegar verið er að vista fjárhagssvarið í rásargagnagrunninum. Eftir að núverandi viðskipti eða atburður hefur verið merktur sem skráður er hægt að halda áfram reglulegri starfsemi á POS.
- **Fresta** – Rekstraraðili getur notað þennan valkost þegar viðskiptin hafa ekki verið skráð vegna þess að skráningartækið eða þjónustan er ekki tiltæk **og** eitt af eftirfarandi á við:
    - Það er varakostur fyrir fjárhagsskráningu og það er hægt að halda áfram fjárhagsskráningarferlinu fyrir núverandi færslu. Til dæmis heimamaður [ríkisfjármálatæki](./latam-bra-cf-e-sat.md#scenario-4-make-a-cash-and-carry-sale-of-goods-by-using-sat-as-contingency-mode) getur verið varavalkostur fyrir skráningarþjónustu á netinu þegar þjónustan er ekki í boði.
    - Hægt er að ljúka ríkisfjármálaskráningu seinna með öðrum hætti en samþættingarrammanum í ríkisfjármálum. Til dæmis er hægt að skrá frestað færslur síðar fjárhagslega í lotu með a [aðskilin virkni](./latam-bra-nfce.md#scenario-3-make-a-cash-and-carry-sale-of-goods-in-offline-contingency-mode).
    
    Eftir að núverandi færslu eða atburði hefur verið frestað er hægt að halda áfram reglulegri starfsemi á POS.

> [!WARNING]
> The **Sleppa**, **sem skráð**, og **Fresta** valkostir ættu að teljast neyðarvalkostir og aðeins notaðir í undantekningartilvikum. Ræddu þessa villumeðferðarmöguleika við lögfræði- eða skattaráðgjafa þinn og beittu góðri dómgreind áður en þú virkjar þá. Valkostirnir verða að vera virkjaðir í fjárhagsskráningarferlinu áður en þeir eru notaðir. Til að tryggja að rekstraraðilar noti þau ekki reglulega, verður að veita rekstraraðilum samsvarandi leyfi.

A [viðskiptum í ríkisfjármálum](#storing-fiscal-response-in-fiscal-transaction) er búið til þegar **Sleppa**, **sem skráð**, eða **Fresta** valkostir eru valdir, en fjárhagsfærslan inniheldur ekki fjárhagslegt svar. Þetta gerir þér kleift að fanga atvik vegna bilunar í fjárhagsskráningu. Þessir valkostir gera einnig upplýsingakóða kleift að fanga tilteknar upplýsingar um bilun, svo sem ástæðu bilunarinnar, eða rökstuðning fyrir því að sleppa fjárhagsskráningu eða merkja færsluna sem skráða. Nánari upplýsingar um hvernig á að setja upp færibreytur fyrir meðhöndlun á villu er að finna í [Stilla villumeðhöndlunarstillingar](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

### <a name="optional-fiscal-registration"></a>Valfrjáls fjárhagsskráning

Fjárhagsskráning kann að vera áskilin fyrir sumar aðgerðir en valfrjáls fyrir aðrar. Til dæmis gæti fjárhagsskráning á reglulegum sömum og skilum verið áskilin, en fjárhagsskráning á aðgerðum sem tengjast innborgun viðskiptavinar kann að vera valfrjáls. Ef svo er ætti að lokast fyrir frekari sölur ef ekki tekst að ljúka fjárhagsskráningu á sölu, en ef ekki tekst að ljúka fjárhagsskráningu á innborgun viðskiptavinar ætti það ekki að loka fyrri frekari sölur. Til að greina á milli áskilina og valfrjálsra aðgerða ráðleggjum við að þú meðhöndlir þær í gegnum mismunandi skjalaveitur og að þú setjir upp aðskilin skref í ferli fjárhagsskráningar fyrir þessar veitur. Virkja skal færibreytuna **Halda áfram á villu** fyrir öll skref sem tengjast valfrjálsri fjárhagsskráningu. Nánari upplýsingar um hvernig á að setja upp færibreytur fyrir meðhöndlun á villu er að finna í [Stilla villumeðhöndlunarstillingar](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

### <a name="manually-rerun-fiscal-registration"></a>Endurtaktu fjárhagsskráningu handvirkt

Ef fjárhagsskráningu viðskipta eða atburðar hefur verið frestað eftir bilun (til dæmis ef rekstraraðilinn valdi **Hætta við** í villumeðferðarglugganum), geturðu keyrt fjárhagsskráninguna aftur handvirkt með því að kalla fram samsvarandi aðgerð. Fyrir frekari upplýsingar, sjá [Virkja handvirka framkvæmd á frestað fjárhagsskráningu](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-deferred-fiscal-registration).

### <a name="fiscal-registration-health-check"></a>Ástandsskoðun fjárhagsskráningar

Ferli ástandsskoðunar fyrir fjárhagsskráningar staðfestir framboð á fjárhagstæki eða þjónustu þegar tilteknir atburðir gerast. Ef ekki er hægt að ljúka fjárhagsskráningu sem stendur er notandinn látinn vita fyrirfram.

Sölustaðurinn keyrir ástandsskoðun þegar eftirfarandi tilvik eiga sér stað:

- Ný færsla er opnuð.
- Frestuð færsla er endurkölluð.
- Gengið er frá sölu- eða skilapöntun.

Ef ástandsskoðun mistekst sýnir sölustaðurinn svarglugga ástandsskoðunar. Svarglugginn er með eftirfarandi hnappa:

- **Í lagi** - Þessi hnappur leyfir notanda að hunsa villu í ástandsskoðun og halda áfram að vinna í aðgerðinni. Notendur geta eingöngu valið þennan hnapp ef heimildin **Leyfa að sleppa villu í ástandsskoðun** er virkjuð fyrir þá.
- **Hætta við** - Ef notandi velur þennan hnapp hættir sölustaður við síðustu aðgerð (til dæmis er vöru ekki bætt við nýja færslu).

> [!NOTE]
> Heilbrigðiseftirlitið er aðeins keyrt ef núverandi aðgerð krefst ríkisskráningar og ef **Halda áfram á villu** færibreytan er óvirk fyrir núverandi skref fjárhagsskráningarferlisins. Frekari upplýsingar er að finna í [Velja stillingar villumeðhöndlunar](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

## <a name="storing-fiscal-response-in-fiscal-transaction"></a>Geymsla á fjárhagssvörum í fjárhagsfærslu

Þegar fjárhagsskráning færslu eða tilviks heppnast er stofnuð fjárhagsfærsla í gagnagrunni rásarinnar og hún tengd við upprunalega færslu eða tilvik. Á sama hátt, ef **Sleppa**, **sem skráð**, eða **Fresta** valkostur er valinn fyrir misheppnaða fjárhagsskráningu, þessar upplýsingar eru geymdar í fjárhagsfærslu. Fjárhagsfærsla heldur í fjárhagssvörun fjárhagstækis eða þjónustu. Ef fjárhagsskráningarferlið samanstendur af nokkrum skrefum er fjárhagsfærsla stofnuð fyrir hvert skref ferlisins sem leiddi til skráningu sem tókst eða mistókst.

Fjárhagsfærslur eru fluttar í bakvinnslu með *P-vinnslu* ásamt færslum. Í flýtiflipanum **Fjárhagsfærslur** á síðunni **Færslur verslunar** er hægt að skoða fjárhagsfærslurnar sem eru tengdar við færslur.

Fjárhagsfærsla geymir eftirfarandi upplýsingar:

- Upplýsingar um ferli fjárhagsskráningar (ferli, tenglahóp, tengil og svo framvegis). Hún geymir einnig raðnúmer fjárhagstækis í reitnum **Skrá númer** ef þessar upplýsingar eru innifaldar í fjárhagssvörun.
- Staða ríkisskráningar: **Lokið** fyrir árangursríka skráningu, **Sleppti** ef símafyrirtækið valdi **Sleppa** valkostur fyrir misheppnaða skráningu, **Merkt sem skráð** ef símafyrirtækið valdi **Merktu sem skráð** valmöguleika, eða **Frestað** ef símafyrirtækið valdi **Fresta** valmöguleika.
- Færslur upplýsingakóða sem tengjast valdri fjárhagsfærslu. Til að skoða færslur með upplýsingakóða, á **Viðskipti í ríkisfjármálum** Flýtiflipi, veldu fjárhagsfærslu sem hefur stöðuna **Sleppti**, **sem skráð**, eða **Frestað**, og veldu síðan **Upplýsingakóða viðskipti**.

Með því að velja **Útvíkkuð gögn** er einnig hægt að skoða nokkra eiginleika fjárhagsfærslunnar. Listi yfir eiginleika sem hægt er að skoða á sérstaklega við um virkni fjárhagsskráningar sem myndaði fjárhagsfærsluna. Til dæmis er hægt að skoða stafræna undirskrift, raðnúmer, fingrafarsvottorð, auðkenni fyrir algrím tætigildis og aðra eiginleika fjárhagsfærslna fyrir stafræna undirritunaraðgerð fyrir Frakkland.

## <a name="fiscal-texts-for-discounts"></a>Fjárhagstextar fyrir afslætti

Sum lönd eða svæði gera sérstakar kröfur um viðbótartexta sem þarf að prenta á fjárhagskvittanir þegar mismunandi afslættir eru notaðir. Virknin fyrir fjárhagssamþættingu gerir þér kleift að setja upp sérstakan texta fyrir afslátt sem prentast á eftir afsláttarlínu á fjárhagskvittun. Fyrir handvirka afslætti er hægt að stilla fjárhagstexta fyrir upplýsingakóðann sem er tilgreindur sem upplýsingakóðinn **Afurðarafsláttur** í virknireglu sölustaðar. Nánari upplýsingar um hvernig á að setja upp fjárhagstexta fyrir afslætti er að finna í [Uppsetning fjárhagstexta fyrir afslætti](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-texts-for-discounts).

## <a name="printing-fiscal-x-and-fiscal-z-reports"></a>Prenta X- og Z-skýrslur fjárhags

Virknin fyrir fjárhagssamþættingu styður myndun á uppgjör í lok dags sem miðast við samþætta fjárhagstækið eða þjónustuna:

- Bæta ætti nýjum hnöppum sem keyra samsvarandi aðgerðir við skjáútlit POS. Nánari upplýsingar er að finna í [Setja upp X/Z-skýrslur fjárhags úr POS](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-xz-reports-from-the-pos).
- Í sýnishorni fjárhagssamþættingar ætti að samsvara þessar aðgerðir við samsvarandi aðgerðir í fjárhagstækinu.

## <a name="fiscal-integration-samples-in-the-commerce-sdk"></a>Sýnishorn fjárhagssamþættingar í Commerce SDK

Eftirfarandi sýnishorn fjárhagssamþættingar eru í boði sem stendur í Commerce SDK:

- [Dæmi um samþættingu strimlaprentara fyrir Ítalíu](./emea-ita-fpi-sample.md)
- [Dæmi um samþættingu strimlaprentara fyrir Pólland](./emea-pol-fpi-sample.md)
- [Dæmi um samþættingu þjónustu fjárhagsskráningar fyrir Austurríki](./emea-aut-fi-sample.md)
- [Dæmi um samþættingu þjónustu fjárhagsskráningar fyrir Tékkland](./emea-cze-fi-sample.md)
- [Dæmi um samþættingu stjórntækja fyrir Svíþjóð](./emea-swe-fi-sample.md)
- [Dæmi um samþættingu þjónustu fjárhagsskráningar fyrir Þýskaland](./emea-deu-fi-sample.md)
- [Dæmi um samþættingu strimlaprentara fyrir Rússland](./rus-fpi-sample.md)

Eftirfarandi virkni fjárhagssamþættingar er einnig innleidd með því að nota ramma fjárhagssamþættingar, en hann kemur beint úr kassanum og er ekki hafður með í Commerce SDK:

- [Fjárhagsskráning fyrir Brasilíu](./latam-bra-commerce-localization.md#fiscal-registration-for-brazil)
- [Stafræn undirskrift fyrir Frakkland](./emea-fra-cash-registers.md)

Eftirfarandi virkni fjárhagssamþættingar er einnig í boði í Commerce SDK en hún nýtir sér ekki ramma fjárhagssamþættingar eins og er. Flutningur á þessari virkni í ramma fjárhagssamþættingar er á dagskrá í seinni útgáfum.

- [Stafræn undirskrift fyrir Noreg](./emea-nor-cash-registers.md)

Eftirfarandi eldri virkni fjárhagssamþættingar sem er í boði í Commerce SDK notar ekki ramma fjárhagssamþættingar og verður gerð úreld í síðari uppfærslum:

- [Dæmi um samþættingu stjórntækja fyrir Svíþjóð (eldra)](./retail-sdk-control-unit-sample.md)
- [Stafræn undirskrift fyrir Frakkland (eldra)](./emea-fra-deployment.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
