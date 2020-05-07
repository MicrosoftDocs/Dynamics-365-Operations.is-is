---
title: Hnitanetsgeta
description: Þetta efni lýsir nokkrum kröftugum eiginleikum netstýringar. Það verður að gera nýja hnitanetsaðgerðina kleift að hafa aðgang að þessum möguleikum.
author: jasongre
manager: AnnBe
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DefaultDashboard
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: fd45f71fc15e467c461433682310ab7b7cc0158a
ms.sourcegitcommit: 0d7b700950b1f95dc030ceab5bbdfd4fe1f79ace
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/23/2020
ms.locfileid: "3284405"
---
# <a name="grid-capabilities"></a>Hnitanetsgeta

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Nýja netstýringin veitir fjölda gagnlegra og öflugra getu sem hægt er að nota til að auka framleiðni notenda, smíða áhugaverðari sýn á gögnin þín og fá þroskandi innsýn í gögnin þín. Þessi grein mun fjalla um eftirfarandi getu: 

-  Reiknar samtölur
-  Flokkun gagna
-  Vélritun á undan kerfinu
-  Mat á stærðfræðisegðum 

## <a name="calculating-totals"></a>Reiknar samtölur
Í forritum Finance and Operations geta notendur séð heildartölur neðst í töludálkum í hnitanetum. Þessar samtölur eru sýndar í síðufótarhluta neðst á töflunni. 

### <a name="showing-the-grid-footer"></a>Sýni síðufót hnitanetsins
Það er neðanmálssvæði neðst í hverju töflukerfi í forritum Finance and Operations. Neðanmálið getur sýnt mikilvægar upplýsingar sem tengjast gögnum sem birtast í reitunum. Hér eru nokkur dæmi um þessar upplýsingar:

- Fjöldi valda lína í töflunni (þegar fleiri en ein skrá er valin)
- Stórt heildartölur neðst í samstilltu töludálkunum
- Fjöldi raða í gagnasafninu 

Þessi síðufótur er sjálfgefið falinn en það er einfalt að kveikja á honum. Til að sýna fót fyrir rist, hægrismellt er á dálkhaus í töflunni og valið valkosturinn **Sýna fót**. Þegar búið er að kveikja á fótfótum fyrir tiltekið rist mun sú stilling muna þar til notandinn kýs að fela fótfótinn, það er hægt að gera með því að hægrismella á dálkhaus og velja **Fela fót**.  Athugið staðsetningu staðsetningu **Sýna fót / Fela fót** Búist er við að aðgerð verði staðsett aftur í framtíðaruppfærslu. 

### <a name="specifying-columns-with-totals"></a>Tilgreina dálka með samtölum
Sem stendur er enginn dálkur stilltur til að sýna samtöl sem sjálfgefið. Þess í stað er þetta talið einskiptisvirkni, svipað og að laga breidd dálka í ristum. Þegar þú hefur tilgreint að þú viljir sjá samtölur fyrir dálk, þá munst þessi stilling næst þegar þú heimsækir síðuna.  

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

## <a name="grouping-data"></a>Flokkun gagna
Notendur fyrirtækja þurfa oft að framkvæma sértækar greiningar á gögnum. Þó að þetta sé hægt að gera með því að flytja gögn út til Microsoft Excel og nota pivot töflur, the **Flokkun** getu í töflum ristum gerir notendum kleift að skipuleggja gögn sín á áhugaverðan hátt innan Finance and Operations smáforrit. Eins og þessi aðgerð nær til **Heildartölur** lögun, **Flokkun** gerir þér einnig kleift að fá þroskandi innsýn í gögnin með því að gefa undirstig á hópsstigi.

Til að nota þennan eiginleika skaltu hægrismella á dálkinn sem þú vilt flokka eftir og velja **Flokkaðu eftir þessum dálki**. Þessi aðgerð mun raða gögnum eftir völdum dálki, bæta við nýjum hóp eftir dálki í byrjun í ristina og setja „hausraðir“ í byrjun hvers hóps. Þessar hausraðir veita eftirfarandi upplýsingar um hvern hóp: 
-  Gagnagildi fyrir hópinn 
-  Dálkamerki (Þessar upplýsingar verða sérstaklega gagnlegar eftir að mörg stig af flokkun eru studd.)
-  Fjöldi gagnalína í þessum hópi
-  Undirmál fyrir hvaða dálk sem er stilltur til að sýna samtölur

Með [Vistaðar skoðanir](saved-views.md) virkt, þá er hægt að vista þennan flokkun með sérstillingu sem hluta af útsýni til að fá skjótan aðgang næst þegar þú heimsækir síðuna.  

Ef þú velur **Flokka eftir þessum dálki** í öðrum dálki er upprunalegri flokkun skipt út, þar sem aðeins eitt stig flokkunar er stutt í útgáfu 10.0.9 með verkvangsuppfærslu 33.

Til að afturkalla flokkun í rist skaltu hægrismella á flokkunarsúluna og velja **Taka saman hóp**.  

## <a name="typing-ahead-of-the-system"></a>Vélritun á undan kerfinu
Í mörgum atburðarásum í viðskiptum er möguleikinn til að færa gögn fljótt inn í kerfið mjög mikilvægur. Áður en nýja hnitanetsstýringin var kynnt gátu notendur aðeins breytt gögnum í núverandi línu. Áður en notendur gátu búið til nýja línu eða skipt yfir í aðra línu neyddust þeir til að bíða eftir að kerfið staðfesti allar breytingar. Til að reyna að draga úr þeim tíma sem notendur bíða eftir að þessum staðfestingum ljúki, og til að bæta afköst notanda, aðlagar nýja hnitanetið þessar staðfestingar svo þær séu ósamstilltar. Þess vegna getur notandinn fært sig yfir í aðrar línur til að gera breytingar á meðan beðið er eftir fyrri staðfestingum á línum. 

Til að styðja við þessa nýju hegðun hefur nýjum dálki fyrir línustöðuna verið bætt við efst í hnitanetinu þegar það er í breytingastillingu. Þessari dálkur sýnir eina af eftirfarandi stöðum:

- **Autt** - Engin stöðumynd gefur til kynna að kerfið hafi náð að vista línuna.
- **Vinnsla í bið** - Þessi staða gefur til kynna að netþjónninn hafi enn ekki vistað breytingar í línunni en að þær séu í biðröð breytinga sem þarf að vinna úr. Áður en gripið er til aðgerða utan hnitanetsins þarf að bíða eftir að unnið er úr öllum breytingum. Að auki er textinn í þessum línum skáletraður til að gefa til kynna óvistaða stöðu á línum. 
- **Staðfestingarviðvörun** - Þessi staða gefur til kynna að kerfið geti ekki vistað breytingarnar í línunni út af nokkrum vandamálum við staðfestingu. Í gamla hnitanetinu var notandi þvingaður til baka í línuna til að laga vandamálið strax. Í nýja hnitanetinu er notandi hinsvegar látinn vita að vandamál við staðfestingu hafi komið upp, en að notandi geti ákveðið hvenær hann vilji laga vandann í línunni. Þegar þú ert tilbúinn til að laga vandann geturðu fært áhersluna handvirkt til baka í línuna. Einnig er hægt að velja aðgerðina **Lagfæra þetta vandamál**. Þessi aðgerð færir áhersluna strax til baka á línuna þar sem vandinn kom upp og leyfir notanda að gera breytingar innan og utan hnitanetsins. Athugið að vinnsla á síðari línum í bið er stöðvuð þar til leyst hefur verið úr þessari staðfestingarviðvörun. 
- **Gert hlé** - Þessi staða gefur til kynna að hlé hafi verið gert á vinnslu netþjónsins því að staðfesting línunnar hafi ræst sprettiglugga sem krefst innslátt notanda. Vegna þess að notandinn gæti verið að slá inn gögn í einhverri annarri línu, er honum ekki birtur sprettiglugginn strax. Í staðinn verður glugginn birtur þegar notandinn kýs að halda áfram vinnslu. Þessari stöðu fylgir tilkynning sem upplýsir notandann um ástandið. Tilkynningin felur í sér aðgerðina **Halda vinnslu áfram** sem ræsir sprettigluggann.  
    
Þegar notendur eru að slá inn gögn á undan þeim stað þar sem netþjónninn er að vinna, mega þeir búist við afkastaminnkun við gagnaskráninguna, t.d. færri uppflettingar, staðfestingar eftirlitsstigs og færslna á sjálfgefnum gildum. Notendur sem þurfa fellilista til að finna gildi eru hvattir til að bíða eftir að þjónninn vinni sig að núverandi línu. Staðfesting eftirlitsstigs og færsla sjálfgefinna gilda gerast einnig netþjónninn vinnur úr þeirri línu.   

### <a name="pasting-from-excel"></a>Líma úr Excel
Notendur hafa alltaf getað flutt gögn úr hnitanetum í Finance and Operations forritum í Excel með því að nota aðferðina **Flytja inn í Excel**. Getan til að slá inn gögn á undan kerfinu gerir hinsvegar nýja hnitanetinu kleift að styðja afritun á töflum úr Excel og líma þær beint í hnitanet í Finance and Operations forritum. Hólfið í hnitanetinu þar sem límingaraðgerðin hefst ákvarðar hvar líming á afritaðri töflu hefst. Efni afrituðu töflunnar skrifar yfir efni hnitanetsins, fyrir utan tvö tilfelli:

- Ef fjöldi dálka í afrituðu töflunni er meiri en fjöldi dálka sem eru eftir í hnitanetinu, þar sem staðsetning límingar hefst, er notandanum tilkynnt að aukadálkarnir hafi verið hunsaðir. 
- Ef fjöldi lína í afrituðu töflunni er meiri en fjöldi lína í hnitanetinu, þar sem staðsetning límingar hefst, skrifar límda efnið yfir núverandi hólf, og allar aukalínur í afrituðu töflunni eru settar inn sem nýjar línur neðst í hnitanetinu. 

## <a name="evaluating-math-expressions"></a>Mat á stærðfræðisegðum
Sem framleiðniörvun geta notendur slegið inn stærðfræðiformúlur í tölureiti í töflu. Þeir þurfa ekki að gera útreikninginn í forriti utan kerfisins. Til dæmis ef þú slærð inn **=15\*4** og ýttu síðan á lykilinn **Flipi** til að fara út úr reitnum, mun kerfið meta segðina og vista gildi upp á **60** fyrir reitinn.

Til að gera kerfið að viðurkenna gildi sem tjáningu, byrjaðu gildið með jöfnu merki (**=**). Nánari upplýsingar um rekstraraðila sem studd er og setningafræði, sjá [Studd stærðfræðitákn](http://bugwheels94.github.io/math-expression-evaluator/#supported-maths-symbols).

## <a name="frequently-asked-questions"></a>Algengar spurningar
### <a name="how-do-i-enable-the-new-grid-control-in-my-environment"></a>Hvernig virkja ég nýja netstýringu í umhverfi mínu? 

**10.0.9 / uppfærsla verkvangs 33 og nýrri** Eiginleikinn **Ný netstýring** er fáanlegur beint í eiginleikastjórnun í hvaða umhverfi sem er. Eins og aðrir opnir forskoðunareiginleikar, þá er það kleift að virkja þennan eiginleika í framleiðslu [Viðbótarskilmálar um notkunarskilmála](https://go.microsoft.com/fwlink/?linkid=2105274).  

**10.0.8 / uppfærsla verkvangs 32 og 10.0.7 / uppfærsla verkvangs 31** Eiginleikinn **Ný netstýring** er hægt að virkja í umhverfi 1. lagi (þróun/prófun) og 2. lagi (sandkassi) til að veita frekari prófunar- og hönnunarbreytingar með því að fylgja skrefunum hér að neðan.

1.  **Virkja flugið**: Framkvæma eftirfarandi SQL staðhæfingu: 

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, enabled, FLIGHTSERVICEID, PARTITION) VALUES('CLIReactGridEnableFeature', 1, 0, 5637144576);`

2. **Núllstilla IIS** til að skola fast flýtiminni. 

3.  **Finndu eiginleikann**: Farðu í vinnusvæði **Stjórnun eiginleika**. Ef **Ný netstjórnun** birtist ekki á listanum yfir alla eiginleika, veldu **Athuga með uppfærslur**.   

4.  **Virkja aðgerðina**: Finndu aðgerðina **Ný netstýring** á listanum yfir aðgerðir og veldu hnappinn **Virkja núna** í upplýsingaglugganum. Athugið að endurræsingar vafra er krafist. 

Allar síðari notendatímabil munu byrja með virkjaða nýja netstýringu.

## <a name="known-issues"></a>Þekkt vandamál
Þessi hluti heldur lista yfir þekkt vandamál fyrir nýja hnitanetstýringuna á meðan eiginleikinn er í forútgáfu.  

### <a name="open-issues"></a>Opin vandamál

- Kortalistar sem voru gefnir upp sem margir dálkar eru nú gefnir upp sem einn dálkur.
- Flokkaðir listar eru ekki gefnir upp sem flokkar eða í aðskildum dálkum.
- Ábendingar eru ekki sýndar fyrir myndir.
- Skjámynd fyrir hnitanetslínur virkar ekki fyrir allar gerðir reita.
- Ekki er hægt að smella utan hnitanetsins þegar búið er að velja nokkrar línur.
- Valkostir verkskráningar **Sannprófa** og **Afrita** eru ekki í boði fyrir stjórnun dagsetningar/númers.

### <a name="fixed-as-part-of-10012"></a>Lagað sem hluti af 10.0.12

> [!Note]
> Eftirfarandi upplýsingar eru gefnar upp svo hægt sé að gera áætlun í samræmi við það. Nánari upplýsingar um áætlaða markútgáfu á útgáfu 10.0.12 er að finna í [Þjónustuuppfærsla í boði](../../fin-ops/get-started/public-preview-releases.md).

- [Mál 429126] Stýringar utan hnitanetsins eru ekki uppfærðar eftir að síðustu færslu er eytt.
- [Mál 430575] Töflustýringar uppfæra ekki innihald uppgefinna atriða.
- [KB 4558570] Atriði eru enn sýnd á síðunni eftir að færslunni hefur verið eytt.
- [KB 4558584] Neikvæðar tölur eru ekki gefnar upp á réttan hátt.
- [KB 4558575] Reitir eru ekki uppfærðir eftir línubreytingu / Úrvinnsla hnitanets festist eftir eyðingu línu.
- [Mál 436980] Stíll sem er tengdur listaglugganum **ExtendedStyle** er ekki notaður.
- [KB 4558573] Ekki er hægt að laga villur sem koma upp við villuleit þegar nauðsynleg breyting er utan hnitanetsins.
    
### <a name="quality-update-for-10011"></a>Gæðauppfærsla fyrir 10.0.11

- [KB 4558381] Neikvæðar tölur eru ekki gefnar rétt upp / Notendur festast stundum þegar vandamál við villuleit koma upp.

### <a name="fixed-as-part-of-10011"></a>Lagað sem hluti af 10.0.11

- [KB 4558374] Ekki er hægt að búa til skrár sem krefjast svarglugga með fjölbreyttu vali.
- [KB 4558382] Óvæntar villur biðlara koma upp.
- [KB 4558375] Hjálpartexti er ekki sýndur í dálkum í nýja hnitanetinu.
- [KB 4558376] Hnitanet listaglugga eru ekki sýnd í réttri hæð í Internet Explorer.
- [KB 4558377] Dálkar samsetts glugga sem eru með breiddina **SizeToAvailable** sjást ekki á sumum síðum.
- [KB 4549711] Ekki er hægt að fjarlægja línur í greiðslutillögu á réttan hátt þegar nýja hnitanetsstýringin er virkjuð.
- [KB 4558378] Köfun opnar stundum ranga skrá.
- [KB 4558379] Villa kemur upp þegar uppflettingar eru opnaðar þar sem **ReplaceOnLookup**=**Nei**.
- [KB 4558380] Tiltækt pláss í hnitanetinu er ekki fyllt strax þegar að hluti síðunnar er dreginn saman.
- [Útgáfa 432458] Tómar eða tvíteknar línur eru sýndar í byrjun sumra undirsafna.
- [KB 4558587] Tilvísunarflokkar sem eru með samsetta glugga fyrir skiptireiti sýna ekki gildi.

### <a name="fixed-as-part-of-10010"></a>Lagað sem hluti af 10.0.10

- [Mál 414301] Sum gögn frá fyrri línum hverfa þegar nýjar línur eru búnar til.
- [KB 4550367] Tímagildin eru á röngu sniði.
- [KB 4549734] Virkar línur eru ekki meðhöndlaðar sem merktar ef merkingardálkurinn er falinn.
- [Bug 417044] Engin tóm skilaboð hnitanets eru til fyrir hnitanet listastíls.
- [KB 4558367] Ósamræmi er í textavali þegar línum er breytt.
- [KB 4558372] Nýja hnitanetið festist í vinnslustillingu ef fjöldi dálka í efni sem er límt inn er meiri en fjöldi dálka sem eftir eru hnitanetinu.
- [KB 4558368] Fjölval með lyklaborði er leyft í atburðarásum einvals.
- [KB 4539058] Sum hnitanet (venjulega flýtiflipar) sjást stundum ekki (en munu sjást ef aðdráttur er minnkaður).
- [KB 4558369] Stöðumyndir hverfa í stigveldistöflunni.
- [KB 4558370] Ekki er flett að nýrri línu.
- [KB 4549796] Ekki er hægt að breyta gildum í hnitaneti þegar það er í skoðunarstillingu.

### <a name="quality-update-for-1009platform-update-33"></a>Gæðauppfærsla fyrir 10.0.9/verkvangsuppfærsla 33

- [KB 4550367] Tímagildin eru á röngu sniði.
