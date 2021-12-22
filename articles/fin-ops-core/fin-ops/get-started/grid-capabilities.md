---
title: Hnitanetsgeta
description: Þetta efni lýsir nokkrum kröftugum eiginleikum netstýringar. Virkja þarf nýjan eiginleika hnitanetsins til að hafa aðgang að þessum möguleikum.
author: jasongre
ms.date: 12/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: ba3640cf13fecc54f4cc58cd8996e434cd16cf60
ms.sourcegitcommit: c85eac17fbfbd311288b50664f9e2bae101c1fe6
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 12/03/2021
ms.locfileid: "7890870"
---
# <a name="grid-capabilities"></a>Eiginleikar hnitanets

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]


Nýja netstýringin veitir fjölda gagnlegra og öflugra eiginleika sem hægt er að nota til að auka framleiðni notenda, smíða áhugaverðari sýn á gögnin þín og fá þroskandi innsýn í gögnin þín. Þessi grein mun fjalla um eftirfarandi getu: 

-  Reiknar samtölur
-  Vélritun á undan kerfinu
-  Mat á stærðfræðisegðum 
-  Flokkun töflugagna (virkjuð sérstaklega með **Flokkun í hnitanetum** eiginleika)
-  Dálkar frystir
-  Aðlaga dálkbreidd sjálfkrafa
-  Teygjanlegir dálkar

## <a name="calculating-totals"></a>Reiknar samtölur
Í forritum Finance and Operations geta notendur séð heildartölur neðst í töludálkum í hnitanetum. Neðanmálshluti neðst í hnitanetinu sýnir þessar samtölur. 

### <a name="showing-the-grid-footer"></a>Sýni síðufót hnitanetsins
Það er neðanmálssvæði neðst í hverju töflukerfi í forritum Finance and Operations. Neðanmálið getur sýnt mikilvægar upplýsingar sem tengjast gögnum sem birtast í reitunum. Hér eru nokkur dæmi um þessar upplýsingar:

- Fjöldi valdra lína í töflunni (þegar fleiri en ein skrá er valin)
- Stórt heildartölur neðst í samstilltu töludálkunum
- Fjöldi raða í gagnasafninu 

Þessi síðufótur er sjálfgefið falinn en hægt er að kveikja á honum. Til að sýna síðufót fyrir hnitanet skal velja hnappinn **Valkostir hnitanets** í haus hnitanetsins og síðan velja valkostinn **Sýna síðufót**. Eftir að kveikt er á síðufætinum fyrir tiltekið hnitanet verður stillingin geymd í minni þar til notandinn kýs að fela síðufótinn. Til að fela síðufótinn skal velja **Fela síðufót** á valmyndinni **Valkostir hnitanets**.  

### <a name="specifying-columns-with-totals"></a>Tilgreina dálka með samtölum
Sem stendur sýna engir dálkar samtölur að sjálfgefnu. Þess í stað er þetta talið einskiptisvirkni, svipað og að laga breidd dálka í ristum. Þegar þú hefur tilgreint að þú viljir sjá samtölur fyrir dálk, þá munst þessi stilling næst þegar þú heimsækir síðuna.  

Það eru tvær leiðir til að stilla dálk til að sýna samtals: 

- Hægrismelltu á dálkinn sem þú vilt sjá samtölu fyrir og veldu síðan **Samtals þennan dálk**. Þessi aðgerð veldur því að þrír atburðir eiga sér stað:

    1. Neðanmálið verður sýnilegt. 
    2. Kjörstillingar þínar um að sjá samtölu í þessum dálki eru vistaðar. 
    3. Útreikningur á heildartölum er hafinn fyrir þennan dálk og alla aðra dálka sem þú hefur áður stillt til að sjá heildartölur fyrir. Tíminn sem þarf til að sýna heildartölu fer eftir stærð gagnapakkans sem þú ert að leggja saman heildartölu fyrir.

- Eftir að neðanmálið er sjáanlegt velurðu **Sýna samtölu** á neðanmálssvæðinu neðst í dálkinum sem þú vilt sjá heildartölu fyrir. Ef það eru engar stilltir dálkar verður hnappurinn **Sýna samtals** tiltækur fyrir alla talnardálka. 

    Þegar að minnsta kosti einn dálkur er stilltur fyrir samtölur verða hnapparnirnir **Sýna samtals** aðeins fáanlegir á sveimi eða fókus. Aðgerðin við að velja **Sýna samtals** vistar bara kjörstillingu þína um að sjá samtölu í þessum dálki, þannig að kjörstillingunni er beitt við síðari heimsóknir á síðuna. Í neðanmálinu er þessi staða gefin til kynna með bandstriki sem birtist í dálkinum. (Að öðrum kosti, ef gagnasafnið er nógu lítið, birtist samtalan strax.)

Ef þú gerir mistök og vilt ekki lengur sjá samtals í tilteknum dálki, hægrismellt á dálkinn og veldu **Fela samtals** eða veldu **Fela samtals** hnappinn í síðufætinum í þeim dálki. Þessi valkostur verður einnig vistaður fyrir framtíðarheimsóknir á síðunni. 

### <a name="calculating-totals"></a>Reiknar samtölur
Þegar þú kemur á síðu þar sem fótstigið er sýnilegt og dálkar nú þegar stilltir fyrir heildartölur, eru heildartölur mögulega eða ekki sýndar í fótfætinum. Hegðunin er háð stærð gagnapakkans á síðunni. Ef gagnapakkinn er nægjanlega lítill, birtast samtöl sjálfkrafa ásamt fjölda lína í gagnapakkanum. Ef það eru bandstrik í fótfótum undir dálkunum sem þú stilltir fyrir heildartölur, þá er gagnapakkinn of stór til að kerfið geti sýnt heildartölur strax og þörf er á skýrum aðgerðum til að reikna heildartölurnar. Til að gera þetta, smelltu á **Reikna** hnappinn í fótfótinum, eða hægrismelltu á dálkinn sem þú vilt hafa samtals fyrir og veldu **Samtals þennan dálk**.  

Ef útreikningurinn tekur of langan tíma geturðu hætt við aðgerðina með því að velja **Hætta við** takki. Stundum verður gagnapakkinn þó of stór til að reikna út heildartölur (takmörk sett af fyrirtækinu) og þér verður tilkynnt að sía gögnin þín meira.

Heildartölur munu uppfærast sjálfkrafa þegar þú uppfærir, eyðir eða býrð til línur í gagnapakkanum.  

## <a name="typing-ahead-of-the-system"></a>Vélritun á undan kerfinu
Í mörgum atburðarásum í viðskiptum er möguleikinn til að færa gögn fljótt inn í kerfið mjög mikilvægur. Áður en nýja hnitanetsstýringin var kynnt gátu notendur aðeins breytt gögnum í núverandi línu. Áður en notendur gátu búið til nýja línu eða skipt yfir í aðra línu neyddust þeir til að bíða eftir að kerfið staðfesti allar breytingar. Til að reyna að draga úr þeim tíma sem notendur bíða eftir að þessum staðfestingum ljúki, og til að bæta afköst notanda, aðlagar nýja hnitanetið þessar staðfestingar svo þær séu ósamstilltar. Þess vegna getur notandinn fært sig yfir í aðrar línur til að gera breytingar á meðan beðið er eftir fyrri staðfestingum á línum. 

Til að styðja við þessa nýju hegðun hefur nýjum dálki fyrir línustöðuna verið bætt við hægra megin við dálk línuvals þegar hnitanetið er í breytingastillingu. Þessari dálkur sýnir eina af eftirfarandi stöðum:

- **Autt** - Engin stöðumynd gefur til kynna að kerfið hafi náð að vista línuna.
- **Vinnsla í bið** - Þessi staða gefur til kynna að netþjónninn hafi enn ekki vistað breytingar í línunni en að þær séu í biðröð breytinga sem þarf að vinna úr. Áður en gripið er til aðgerða utan hnitanetsins þarf að bíða eftir að unnið er úr öllum breytingum. Að auki er textinn í þessum línum skáletraður til að gefa til kynna óvistaða stöðu á línum. 
- **Ógild staða** - Þessi staða sýnir að viðvörun eða skilaboð hafi verið ræst við úrvinnslu á línunni og að það hafi hugsanlega komið í veg fyrir að kerfið vistaði breytingarnar í þessari línu. Í gamla hnitanetinu, ef vistunaraðgerðin tókst ekki, var notandi þvingaður til baka í línuna til að laga vandamálið strax. Í nýja hnitanetinu er notandi hinsvegar látinn vita að vandamál við staðfestingu hafi komið upp, en að notandi geti ákveðið hvenær hann vilji laga vandann í línunni. Þegar þú ert tilbúinn til að laga vandamál geturðu fært áhersluna handvirkt til baka í línuna. Einnig er hægt að velja aðgerðina **Lagfæra þetta vandamál**. Þessi aðgerð færir áhersluna strax til baka á línuna þar sem vandinn kom upp og leyfir notanda að gera breytingar innan og utan hnitanetsins. Athugið að vinnsla á síðari línum í bið er stöðvuð þar til leyst hefur verið úr þessari staðfestingarviðvörun. 
- **Gert hlé** - Þessi staða gefur til kynna að hlé hafi verið gert á vinnslu netþjónsins því að staðfesting línunnar hafi ræst sprettiglugga sem krefst innslátt notanda. Vegna þess að notandinn gæti verið að slá inn gögn í einhverri annarri línu, er honum ekki birtur sprettiglugginn strax. Í staðinn verður glugginn birtur þegar notandinn kýs að halda áfram vinnslu. Þessari stöðu fylgir tilkynning sem upplýsir notandann um ástandið. Tilkynningin felur í sér aðgerðina **Halda vinnslu áfram** sem ræsir sprettigluggann.  
    
Þegar notendur eru að slá inn gögn á undan þeim stað þar sem netþjónninn er að vinna, mega þeir búist við afkastaminnkun við gagnaskráninguna, t.d. færri uppflettingar, staðfestingar eftirlitsstigs og færslna á sjálfgefnum gildum. Notendur sem þurfa fellilista til að finna gildi eru hvattir til að bíða eftir að þjónninn vinni sig að núverandi línu. Staðfesting eftirlitsstigs og færsla sjálfgefinna gilda gerast einnig netþjónninn vinnur úr þeirri línu.   

### <a name="pasting-from-excel"></a>Líma úr Excel
Notendur hafa alltaf getað flutt gögn úr hnitanetum í Finance and Operations forritum í Microsoft Excel með því að nota aðferðina **Flytja inn í Excel**. Getan til að slá inn gögn á undan kerfinu gerir hinsvegar nýja hnitanetinu kleift að styðja afritun á töflum úr Excel og líma þær beint í hnitanet í Finance and Operations forritum. Hólfið í hnitanetinu þar sem límingaraðgerðin hefst ákvarðar hvar líming á afritaðri töflu hefst. Efni afrituðu töflunnar skrifar yfir efni hnitanetsins, fyrir utan tvö tilfelli:

- Ef fjöldi dálka í afrituðu töflunni er meiri en fjöldi dálka sem eru eftir í hnitanetinu, þar sem staðsetning límingar hefst, er notandanum tilkynnt að aukadálkarnir hafi verið hunsaðir. 
- Ef fjöldi lína í afrituðu töflunni er meiri en fjöldi lína í hnitanetinu, þar sem staðsetning límingar hefst, skrifar límda efnið yfir núverandi hólf, og allar aukalínur í afrituðu töflunni eru settar inn sem nýjar línur neðst í hnitanetinu. 

## <a name="evaluating-math-expressions"></a>Mat á stærðfræðisegðum
Sem framleiðniörvun geta notendur slegið inn stærðfræðiformúlur í tölureiti í töflu. Þeir þurfa ekki að gera útreikninginn í forriti utan kerfisins. Til dæmis ef þú slærð inn **=15\*4** og ýttu síðan á lykilinn **Flipi** til að fara út úr reitnum, mun kerfið meta segðina og vista gildi upp á **60** fyrir reitinn.

Til að gera kerfið að viðurkenna gildi sem tjáningu, byrjaðu gildið með jöfnu merki (**=**). Nánari upplýsingar um rekstraraðila sem studd er og setningafræði, sjá [Studd stærðfræðitákn](http://bugwheels94.github.io/math-expression-evaluator/#supported-maths-symbols).

## <a name="grouping-tabular-data"></a>Flokkun töflugagna
Notendur fyrirtækja þurfa oft að framkvæma sértækar greiningar á gögnum. Þó að hægt sé að framkvæma þetta með því að flytja út gögn á Microsoft Excel og nota Pivot-töflur gerir **flokkun í hnitaneti** eiginleikinn, sem er háður nýjum eiginleika hnitastýringar, notendum kleift að skipuleggja töflugögn á áhugaverðan hátt innan Finance and Operations-forrita. Vegna þess að þessi eiginleiki víkkar eiginleikann **Samtölur**, gerir **Flokkun** þér kleift að fá auðskiljanlegri innsýn í gögnin með því að gefa upp millisamtölur á hópstigi.

Til að nota þennan eiginleika skal hægrismella á dálkinn sem á að flokka eftir, og velja **Flokka eftir þessum dálki**. Þessi aðgerð mun raða gögnum eftir völdum dálki, bæta við nýjum **Flokki eftir** dálki við upphaf hnitanetsins og setja inn „hauslínur“ í upphafi hvers hóps. Þessar hausraðir veita eftirfarandi upplýsingar um hvern hóp: 
-  Gagnagildi fyrir hópinn 
-  Dálkheiti (þessar upplýsingar eru sérstaklega gagnlegar þegar mörg flokkunarstig eru til staðar)  
-  Fjöldi gagnalína í þessum hópi
-  Undirmál fyrir hvaða dálk sem er stilltur til að sýna samtölur

Með [Vistaðar skoðanir](saved-views.md) virkt, þá er hægt að vista þennan flokkun með sérstillingu sem hluta af útsýni til að fá skjótan aðgang næst þegar þú heimsækir síðuna.  

### <a name="multiple-levels-of-grouping"></a>Mörg stig flokkunar
Eftir að gögn hafa verið flokkuð eftir einum dálki er hægt að flokka gögnin eftir öðrum dálki með því að velja **Flokka eftir þessum dálki** í viðkomandi dálki. Hægt er að endurtaka þetta ferli þar til fimm faldaðar stigaflokkanir eru til staðar, sem er studd hámarksdýpt. Á þessu stigi er ekki lengur hægt að flokka eftir viðbótardálkum.  

Hvenær sem er er hægt að fjarlægja flokkun í hvaða dálki sem er með því að hægrismella á dálkinn og velja **Sundra hópi**. Einnig er hægt að fjarlægja flokkun úr öllum dálkum með því að velja **Valkostir hnitanets** og síðan **Sundra öllum hópi**.   

### <a name="expanding-and-collapsing-groups"></a>Stækka og fella saman hópa
Fyrsta flokkun gagna verður með alla hópa útvíkkaða. Hægt er að búa til samandregin yfirlit yfir gögnin með því að fella saman einstaka flokka eða nota hóp til að stækka og draga saman til að aðstoða við að fletta í gegnum gögn. Til að víkka út hóp eða draga hann saman skal velja tvíoddatákn (>) hnappinn í samsvarandi flokkshauslínu. Athugið að staða fyrir víkkun/samanfellingu einstakra flokka er **ekki** vistuð í sérstillingum.

### <a name="selecting-and-unselecting-rows-at-the-group-level"></a>Velja og afvelja línur á hópstigi
Á sama hátt og hægt er að velja (eða afvelja) allar línur í hnitanetinu með því að velja gátreitinn efst í fyrsta dálkinum í hnitanetinu, einnig er hægt að velja (eða afvelja) allar línur í hópi með því að velja gátreitinn í samsvarandi hauslínu hóps. Gátreiturinn í hauslínu hóps endurspeglar alltaf núverandi valstöðu lína í þeim hópi, burtséð frá því hvort allar línur séu valdar, engar línur séu valdar eða aðeins nokkrar línur séu valdar.

### <a name="hiding-column-names"></a>Fela dálkaheiti
Við flokkun gagna er sjálfgefið að hegðun sýni dálkheiti í hauslínu hóps. Hægt er að fela dálkheitið í hauslínu hóps með því að velja **Valkostir hnitanets** > **Fela dálkheiti hóps**.

### <a name="grouping-on-date-and-time-columns"></a>Flokkun á dálkum dagsetningar og tíma
Frá og með útgáfu 10.0.24, fyrir Date eða DateTime reiti, hefur valkostinum verið bætt við hóp eftir árum, mánuði eða degi. Hópurinn „gildi“ í samsvarandi hauslínu mun passa við sniðið úr þeim reit. Að auki, fyrir DateTime og Time reiti, muntu geta flokkað eftir klukkustund, mínútu eða sekúndu.    

## <a name="freezing-columns"></a>Dálkar frystir
Sumir dálkar í hnitaneti gætu reynst það mikilvægir fyrir samhengi þannig að þú vilt ekki að þeir hverfi úr augsýn við flettingu. Þess í stað gætirðu viljað að gildin í þessum dálkum séu alltaf sýnileg. Eiginleikinn **Festa dálka í hnitaneti** býður notendum upp á þennan sveigjanleika. 

Til að festa dálk skal hægrismella í haus dálksins og síðan velja **Festa dálk**. Í fyrsta skipti sem þetta skref er gert verður valinn dálkur að fyrsta dálkinum og mun ekki lengur hverfa úr augsýn við flettingu. Næstu dálkum sem eru festir verður bætt hægra megin við síðasta festa dálkinn. Hægt er að nota venjulegu færsluaðgerðina til að endurraða festum dálkum eftir þörfum. Hins vegar er ekki hægt að færa festa dálka þannig að þeir birtist á meðal ófestra dálka. Að sama skapi er ekki hægt að færa ófesta dálka þannig að þeir birtist á meðal festra dálka.

Til að losa dálk skal hægrismella í haus fests dálks og síðan velja **Losa dálk**. 

Athugið að dálkval og línustaða dálka í nýja hnitanetinu eru alltaf fest sem fyrstu tveir dálkarnir. Þess vegna, þegar þessir dálkar eru teknir með í hnitaneti, verða þeir alltaf sýnilegir notanda, óháð láréttri flettistöðu í hnitanetinu. Ekki er hægt að endurraða þessum tveimur dálkum.

## <a name="autofit-column-width"></a>Aðlaga dálkbreidd sjálfkrafa
Líkt og Excel geta notendur sjálfkrafa þvingað dálk til að breyta stærð miðað við það efni sem er sýnt í þeim dálki. Til að gera þetta skal tvísmella á gripsvæði í dálkinum eða með því að setja fókus á dálkhausinn og ýta á **A** (fyrir sjálfvirka aðlögun). Þessi möguleiki verður í boði frá og með útgáfu 10.0.23.  

## <a name="frequently-asked-questions"></a>Algengar spurningar
### <a name="how-do-i-enable-the-new-grid-control-in-my-environment"></a>Hvernig virkja ég nýja netstýringu í umhverfi mínu? 

Eiginleikinn **Ný hnitanetsstýring** er í boði í eiginleikastjórnun í hvaða umhverfi sem er. Eftir að eiginleikinn í eiginleikastjórnun hefur verið virkjaður munu allar síðari notandalotur nýta sér nýju netstýringuna. 

Þessi eiginleiki er virkjaður með því að fara sjálfgefið í gang í útgáfu 10.0.21 og er miðað við að hann verði áskilinn í útgáfu 10.0.25. 

## <a name="developer-opting-out-individual-pages-from-using-the-new-grid"></a>[Þróunaraðili] Afskrá einstaka síður frá því að nota nýja hnitanetið 
Ef fyrirtækið uppgötvar síðu sem á í vandræðum með að nota nýja hnitanetið, er API tiltækt til að leyfa einstökum skjámyndum að nota eldri netstýringu og leyfa á sama tíma öðrum hlutum kerfisins að nota nýju netstýringuna. Til að afskrá einstaka síður frá því að nota nýja hnitanetið, skal bæta við eftirfarandi kallskilaboðum `super()` í `run()` aðferð skjámyndarinnar.

 ```this.forceLegacyGrid();```

Þetta API verður notað þangað til nýja netstýringin verður áskilin, sem er stefnt á að gerist í apríl 2022. Ef einhver vandamál krefjast þess að þetta API sé notað skal tilkynna um þau til Microsoft.

### <a name="forcing-a-page-to-use-the-new-grid-after-previously-opting-out-the-grid"></a>Að þvinga síðu til að nota nýja netið eftir að hafa áður afþakkað netið
Ef þú hefur valið að nota ekki einstaka síðu á nýja netinu gætirðu viljað virkja nýja netið aftur síðar eftir að undirliggjandi vandamál hafa verið leyst. Til að gera þetta þarftu einfaldlega að fjarlægja kallið við `forceLegacyGrid()`. Breytingin tekur ekki gildi fyrr en eitt af eftirfarandi gerist:

- **Endurvirkjun umhverfis**: Þegar umhverfi er uppfært og virkað að nýju er taflan sem geymir síðurnar sem hafa verið valdar úr nýja netinu sjálfkrafa hreinsuð út (FormControlReactGridState).

- **Handvirk hreinsun töflunnar**: Fyrir þróunaraðstæður þarftu að nota SQL til að hreinsa FormControlReactGridState töfluna og endurræsa síðan AOS. Þessi samsetning aðgerða mun endurstilla skyndiminni síðna sem hafa afþakkað nýja hnitið.  

## <a name="developer-size-to-available-width-columns"></a>[Þróunaraðili] Stækka breidd dálka eins og hægt er
Ef þróunaraðili stillir eiginleikann **WidthMode** á **SizeToAvailable** fyrir dálka innan nýja hnitanetsins, fá þessir dálkar upphaflega sömu breidd og þeir myndu fá ef eiginleikinn væri stilltur á **SizeToContent**. Hins vegar teygist á þeim þannig að þeir noti þá breidd sem í boði er innan hnitanetsins. Ef eiginleikinn er stilltur á **SizeToAvailable** fyrir marga dálka, deila allir þessir dálkar á milli sín aukalegri breidd sem er í boði innan hnitanetsins. Hins vegar, ef notandi breytir stærð einhverra þessara dálka, verður sá dálkur fastur. Hann heldur þeirri breidd og breikkar ekki lengur til að fylla upp í tiltæka breidd hnitanetsins.  

## <a name="known-issues"></a>Þekkt vandamál
Þessi hluti heldur lista yfir þekkt vandamál fyrir nýju hnitanetsstýringuna.  

### <a name="open-issues"></a>Opin vandamál
-  Þegar búið er að virkja eiginleikann **Ný hnitanetsstýring**, halda sumar síður áfram að nota núverandi netstýringu. Þetta gerist við eftirfarandi aðstæður:  
    -  Spjaldlisti er til á síðunni sem gefinn er upp í mörgum dálkum.
    -  Flokkaður spjaldlisti er til á síðunni.
    -  Dálkur hnitanets sem bregst ekki við stækkanlegri stýringu.

    Þegar notandi stendur í fyrsta skipti frammi fyrir þessum aðstæðum birtast skilaboð um að uppfæra skuli síðuna. Eftir að þessi skilaboð birtast mun síðan halda áfram að nýta núverandi hnitanet fyrir alla notendur fram að næstu uppfærslu afurðar. Betri meðhöndlun á þessum aðstæðum, svo hægt sé að nýta nýja hnitanetið, verður höfð í huga í framtíðaruppfærslu.    
    
-  [KB 4582758] Færslur eru óskýrar þegar verið er að breyta aðdrætti úr 100 í einhverja aðra prósentutölu
-  [KB 4592012] Óvænt biðlaravilla í IE11 þegar margar línur eru límdar úr Excel
    -  Microsoft er ekki að vinna að lagfæringu á þessu vandamáli

### <a name="fixed-as-part-of-10016"></a>Lagað sem hluti af 10.0.16

-  [KB 4598335] Strengjastýringar margra lína fara ekki eftir DisplayHeights í listum/spjöldum 
-  [KB 4591891] Reikningstillögulínur hverfa þegar línur eru afmerktar
-  [KB 4592104] Ekki er hægt að breyta færslum eftir að smellt er á „Leysa vandamál“ og farið er í aðra línu án þess að lagfæra staðfestingarvandann
-  [KB 4594449] Hnappana „Aldrei“ og „Hreinsa“ vantar inni í dagsetningarvalinu 
-  [KB 4594448] Innsláttur tíma er meðhöndlaður á annan hátt í nýja hnitanetinu
-  [KB 4600059] Óvænt biðlaravilla í takmörkun tölvupóstsendinga
-  [KB 4574584] Forskoðun kostnaðar í viðhengi ekki í boði þegar músarbendlinum er haldið yfir kvittunartákninu

### <a name="fixed-as-part-of-10015"></a>Lagað sem hluti af 10.0.15    

-  (Gæðauppfærsla) [KB 4594444] Óvænt biðlaravilla í forskoðun fyrir sundurliðaða innfærslustýringu
-  [KB 4582723] Birtingarkostir sjást ekki þegar það er gert síðar í líftíma eyðublaðs
-  [KB 4591988] Vandamál þegar lyklaborðið er notað til að velja gildi úr uppflettingu ReferenceGroup
-  [KB 4588958] Regression Suite Automation Tool (RSAT) prófun mistekst með villu: TypeError: Ekki hægt að lesa óskilgreindan eiginleika „texta“
-  [KB 4591970] Óvænt biðlaravilla þegar líming úr Excel var gerð strax eftir að smellt var í hnitanetið
-  [KB 4591904] Breytingar á gögnum eru ekki vistaðar ef notandi, eftir breytingu á stýringu, smellti strax og opnaði uppflettingu á annarri stýringu
-  [KB 4584752] Óvænt biðlaravilla varðandi tillögusíðu verkreikninga
-  [KB 4584540] Ekki er hægt að fara úr hnitanetinu eftir límingu á einni línu í færslulínu
-  [KB 4591908] Þegar ný lína er stofnuð helst áherslan á dálkinum sem notandi var í

### <a name="fixed-as-part-of-10014"></a>Lagað sem hluti af 10.0.14

-  (Gæðauppfærsla) [KB 4584752] Óvænt biðlaravilla með síðu verkreikningstillagna
-  [KB 4583880] Regression Suite Automation Tool (RSAT) prófun mistekst í OpenLookup-aðgerð með „Ekki er hægt að lesa óskilgreinda eiginleika RowIndex“
-  [KB 4583847] Óvænt biðlaravilla þegar farið er í gegnum uppflettingar

### <a name="fixed-as-part-of-10013"></a>Lagað sem hluti af 10.0.13

-  (Gæðauppfærsla) [KB 4584752] Óvænt biðlaravilla með síðu verkreikningstillagna
-  (Gæðauppfærsla) [KB 4583880] Regression Suite Automation Tool (RSAT) prófun mistekst í OpenLookup-aðgerð með „Ekki er hægt að lesa óskilgreinda eiginleika RowIndex“
-  (Gæðauppfærsla) [KB 4583847] Óvænt biðlaravilla þegar farið er í gegnum uppflettingu 
-  (Gæðauppfærsl) [Villa 471777] Ekki er hægt að velja reiti í hnitaneti til að breyta eða búa til farsímaforrit
-  [KB 4582727] Hnitanet frýs eftir að notandi fær svarglugga fyrir vörur með margs konar magni
-  [Villa 474851] Tenglar í stýringum viðmiðunarhópa virka ekki 
-  [Villa 474848] Aukin forskoðun með hnitanetum birtist ekki
-  [KB 4582726] Ekki er verið að virða RotateSign-eignina  
-  [Villa 470173] Gátreitir í óvirkum línum víxlast þegar smellt er á hvíta svæðið í hólfinu
-  [Villa 474848] Aukin forskoðun með hnitanetum birtist ekki
-  [Villa 474851] Tenglar í stýringum viðmiðunarhópa virka ekki 
-  [Villa 471777] Ekki er hægt að velja reiti í hnitaneti til að breyta eða búa til farsímaforrit
-  [KB 4569441] Vandamál með myndun spjaldalista í mörgum dálkum, ábendinga á myndum og birtingarkostir í sumum reitum
-  [KB 4575279] Ekki er öllum merktum línum eytt í almennri færslubók
-  [KB 4575233] Birtingarkostir eru ekki endurheimtir þegar farið er í aðra línu
-  [Villa 477884] Uppflettingar skila röngu gildi/færslu ef ný hnitanetsstjórnun er virkjuð
-  [KB 4571095] Bókun innhreyfingarskjals afurðar á sér stað þegar óvart er ýtt á Enter (rétt meðhöndlun á sjálfgefinni aðgerð síðu)
-  [KB 4575437] Uppflettingar með breytanlegum stýringum loka óvænt
-  [KB 4569418] Tvítekin lína stofnuð í skjámynd afhendingaráætlunar
-  [KB 4575435] Aukin forskoðun er stundum viðvarandi jafnvel þegar músarbendillinn er ekki nálægt reitnum
-  [KB 4575434] Uppfletting síar ekki þegar reitnum hefur verið breytt
-  [KB 4575430] Gildi í reitum aðgangsorða eru ekki hulin í hnitanetinu
-  [KB 4569438] „Vinnsla stöðvaðist vegna vandamáls við staðfestingu“ birtist á eftir að línur eru merktar við jöfnun á færslum birgja
-  [KB 4569434] Uppfærsla á skjámynd lögaðila leiðir til færri færslna
-  [KB 4575297] Áhersla færist yfir á verkskráningarsvæðið þegar hnitaneti er breytt eða hoppað á milli
-  [KB 4566773] Leiðréttingarfærslur sjást ekki sem neikvæðar í fyrirspurn um fylgiskjalsfærslur 
-  [KB 4575288] Áhersla fer aftur á virku línuna þegar ramminn er valinn á milli lína í einföldum lista
-  [KB 4575287] Áhersla fer ekki aftur á fyrsta dálkinn þegar niðurörin er notuð til að stofna nýja línu í færslubókum
-  [KB 4564819] Ekki er hægt að eyða línum í reikningi með frjálsum texta (vegna gagnagjafans ChangeGroupMode=ImplicitInnerOuter)
-  [KB 4563317] Ábendingar/auknar forskoðanir birtast ekki fyrir myndir

### <a name="fixed-as-part-of-10012"></a>Lagað sem hluti af 10.0.12

- [KB 4558545] Töflustýringar uppfæra ekki innihald uppgefinna atriða.
- [KB 4558570] Atriði eru enn sýnd á síðunni eftir að færslunni hefur verið eytt.
- [KB 4558572] Stíll sem er tengdur listaglugganum **ExtendedStyle** er ekki notaður.
- [KB 4558573] Ekki er hægt að laga villur sem koma upp við villuleit þegar nauðsynleg breyting er utan hnitanetsins.
- [KB 4558584] Neikvæðar tölur eru ekki gefnar upp á réttan hátt.
- [KB 4560726] „Óvænt biðlaravilla“ kemur upp þegar farið er á milli lista með því að nota stjórnun listayfirlits.
- [KB 4562141] Slökkt er á vísum hnitanets þegar nýrri færslu er bætt við.
- [KB 4562151] Valkostir verkskráningar **Sannprófa** og **Afrita** eru ekki í boði fyrir stjórnun dagsetningar/númers. 
- [KB 4562153] Fjölvalsgátreitir eru ekki sýnilegir í hnitanetum lista/spjalds.
- [KB 4562646] Stundum er ekki hægt að smella utan hnitanetsins eftir að margar línur eru valdar í hnitanetinu.
- [KB 4562647] Fókus er núllstilltur á fyrstu stýringu í svarglugganum **Gefa út** þegar nýrri línu er bætt við í hnitaneti öryggishlutverka.
- [KB 4563310] Aukin forskoðun er ekki lokað eftir að línu er breytt.
- [KB 4563313] „Óvænt biðlaravilla“ á sér stað í Internet Explorer þegar gildi er valið í uppflettingu.
- [KB 4564557] Uppflettingar og fellivalmyndir opnast ekki í Internet Explorer
- [KB 4563324] Fletting virkar ekki eftir að vinnusvæðið **Starfsmannastjórnun** er opnað.

### <a name="fixed-as-part-of-10011"></a>Lagað sem hluti af 10.0.11

- [Útgáfa 432458] Tómar eða tvíteknar línur eru sýndar í byrjun sumra undirsafna.
- [KB 4549711] Ekki er hægt að fjarlægja línur í greiðslutillögu á réttan hátt þegar nýja hnitanetsstýringin er virkjuð.
- [KB 4558374] Ekki er hægt að búa til skrár sem krefjast svarglugga með fjölbreyttu vali.
- [KB 4558375] Hjálpartexti er ekki sýndur í dálkum í nýja hnitanetinu.
- [KB 4558376] Hnitanet listaglugga eru ekki sýnd í réttri hæð í Internet Explorer.
- [KB 4558377] Dálkar samsetts glugga sem eru með breiddina **SizeToAvailable** sjást ekki á sumum síðum.
- [KB 4558378] Köfun opnar stundum ranga skrá.
- [KB 4558379] Villa kemur upp þegar uppflettingar eru opnaðar þar sem **ReplaceOnLookup**=**Nei**.
- [KB 4558380] Tiltækt pláss í hnitanetinu er ekki fyllt strax þegar að hluti síðunnar er dreginn saman.
- [KB 4558381] Neikvæðar tölur eru ekki gefnar rétt upp / Notendur festast stundum þegar vandamál við villuleit koma upp.
- [KB 4558382] Óvæntar villur biðlara koma upp.
- [KB 4558383] Stýringar utan hnitanetsins eru ekki uppfærðar eftir að síðustu færslu er eytt.
- [KB 4558587] Tilvísunarflokkar sem eru með samsetta glugga fyrir skiptireiti sýna ekki gildi.
- [KB 4562143] Reitir eru ekki uppfærðir eftir línubreytingu / Úrvinnsla hnitanets festist eftir eyðingu línu.
- [KB 4562645] Undantekning á sér stað þegar uppfletting er opnuð á meðan prófanir á Regression Suite Automation Tool eru keyrðar.

### <a name="fixed-as-part-of-10010"></a>Lagað sem hluti af 10.0.10

- [Mál 414301] Sum gögn frá fyrri línum hverfa þegar nýjar línur eru búnar til.
- [Bug 417044] Engin tóm skilaboð hnitanets eru til fyrir hnitanet listastíls.
- [KB 4539058] Sum hnitanet (venjulega flýtiflipar) sjást stundum ekki (en munu sjást ef aðdráttur er minnkaður).
- [KB 4549734] Virkar línur eru ekki meðhöndlaðar sem merktar ef merkingardálkurinn er falinn.
- [KB 4549796] Ekki er hægt að breyta gildum í hnitaneti þegar það er í skoðunarstillingu.
- [KB 4558367] Ósamræmi er í textavali þegar línum er breytt.
- [KB 4558368] Fjölval með lyklaborði er leyft í atburðarásum einvals.
- [KB 4558369] Stöðumyndir hverfa í stigveldistöflunni.
- [KB 4558370] Ekki er flett að nýrri línu.
- [KB 4558372] Nýja hnitanetið festist í vinnslustillingu ef fjöldi dálka í efni sem er límt inn er meiri en fjöldi dálka sem eftir eru hnitanetinu.
- [KB 4562631] Tímagildin eru á röngu sniði.

### <a name="quality-update-for-1009platform-update-33"></a>Gæðauppfærsla fyrir 10.0.9/verkvangsuppfærsla 33

- [KB 4550367] Tímagildin eru á röngu sniði.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
