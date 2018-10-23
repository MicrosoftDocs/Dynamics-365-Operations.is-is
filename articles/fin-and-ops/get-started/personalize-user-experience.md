---
title: "Sérsniðin notkun"
description: "Þessi grein útskýrir hvernig hægt er að sérsníða Microsoft Dynamics 365 for Finance and Operations."
author: TLeforMicrosoft
manager: AnnBe
ms.date: 09/28/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysUserSetup, DefaultDashboard
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 62363
ms.assetid: 57b445d7-3e9e-4228-8728-f63b9dbd77a3
ms.search.region: Global
ms.author: tlefor
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7344f460fcb443a78b254e2387fbf5c9134bf674
ms.openlocfilehash: 1860b603f789aabca1ca58848a88e11a6e08e31f
ms.contentlocale: is-is
ms.lasthandoff: 10/16/2018

---

# <a name="personalize-the-user-experience"></a>Sérsniðin notkun

[!include [banner](../includes/banner.md)]

Þessi grein útskýrir hvernig hægt er að sérsníða Microsoft Dynamics 365 for Finance and Operations.

Það eru þrjár grunnflokkar sérstillinga í Finance and Operations. 
- Sérstillingar gerðar á uppsetningarsíðu. Til dæmis stillingar á litaþema og tímabelti.
- Sérstillingar sem tengjast notkun á síðum og kallast *óbeinar* sérstillingar. Til dæmis fylgist Finance and Operations með breidd dálka í hnitaneti ef þú stillir þá, og hvort flýtiflipar eru útvíkkaðir eða samandregnir. 
- Sérstillingar sem notandi gerir til að breyta útliti á síðu með því að breyta því hvernig eining birtist eða virkar á þeirri síðu, oft í gegnum gagnvirkan sérstillingarham. Þessar sérstillingar eru kallaðar *beinar* sérstillingar. Til dæmis getur notandinn bætt við, falið eða endurskipuleggja einingar á síðunni.

Allar sérstillingar sem notandi gerir í Finance and Operations eru aðeins fyrir þann notanda, óháð gerð sérstillingar eða því fyrirtæki sem notandinn á í samskiptum við á þeim tíma. Breytingarnar sem notandi gerir á síðu hefur ekki áhrif á aðra notendur í kerfinu.

## <a name="system-wide-options-for-the-current-user"></a>Kerfisaltækir valkostir fyrir núverandi notanda
**Notandavalkostir** síðan inniheldur nokkrar kerfisaltækar stillingar fyrir núverandi notanda. Til að opna **Notandavalkostir** síðuna skaltu velja **Stillingar** valmyndina (táknið fyrir gír) á yfirlitsstikunni og velja síðan **Notandavalkostir**. **Notandavalkostir** síðan hefur fjóra flipa sem innihalda ýmsar notandastillingar:

- **Sjónrænt** - Veldu litaþema og sjálfgefna stærð eininga á síðum.
- **Kjörstillingar** - Veldu sjálfgefin gildi sem eru notuð í hvert skipti sem þú opnar Finance and Operations. Þessi gildi eru meðal annars fyrirtækið, upphafssíðan og sjálfgefið skoða/breyta hamurinn. (Skoða/breyta hamurinn ákvarðar hvort síða sé læst í skoðun eða opin fyrir breytingar í hvert skipti sem þú opnar hana.) Þessi flipi inniheldur einnig valkosti fyrir tungumálið, tímabeltið og dagsetningu, tíma og númerasnið. Að lokum inniheldur þessi flipi nokkrar fjölbreytilegar kjörstillingar sem eru mismunandi frá útgáfu til útgáfu.
- **Notandareikningur** - Stilla notandanafnið þitt og aðrar valkosti sem tengjast notandareikningi.
- **Vinnuflæði** - Veldu verkflæðatengda valkosti.

## <a name="implicit-personalizations"></a>Óbeinar sérstillingar
Óbeinar sérstillingar eru þær sérstillingar sem þú gerir aðeins með því að hafa samskipti við stjórntæki sem „muna“ núverandi sýnilegt ástand þeirra.

- **Dálkar í hnitaneti** - Hægt er að stilla breidd dálks í hnitaneti með því að velja stækkunarstikuna vinstra eða hægra megin við dálkhausinn og síðan renna henni til vinstri eða hægri þar til dálkurinn nær ákjósanlegri breidd. Finance and Operations geymir breiddina sem þú stillir fyrir dálk. Forritið breytir síðan dálknum í þá breidd í hvert sinn sem þú opnar síðuna sem inniheldur það hnitanet.
- **Flýtiflipar** - Sumar síður hafa stækkanlega hluta sem eru þekktir sem *Flýtiflipar*. Finance and Operations geymir upplýsingar um flýtiflipana sem þú hefur víkkað út og dregið saman. Í hvert skipti sem þú kemur síðan aftur á síðuna, verða sömu flýtifliparnir annaðhvort víkkaðir út eða dregnir saman, byggt á síðustu samskiptum þínum við síðuna. Í sumum tilfellum geturðu hjálpað til við að auka afköst kerfisins með því að draga saman flýtiflipa, því Finance and Operations þarf ekki að sækja upplýsingar um þann flýtiflipa þar til hann er stækkaður. Eins og útskýrt er síðar í þessu efnisatriði geturðu einnig breytt röð flýtiflipanna á síðu.
- **Upplýsingareitir** - Sumar síður hafa hluta sem kallast *Upplýsingareitssvæði*. Þetta svæði inniheldur skrifvarðar upplýsingar sem tengjast efninu á síðunni. Sérhver hluti í upplýsingareitssvæði kallast *Upplýsingareitur*. Þú getur falið eða sýnt allt upplýsingareitssvæðið, og þú getur einnig útvíkkað eða dregið saman einstaka upplýsingareiti. Finance and Operations geymir kjörstillingar þínar. Í hvert skipti sem þú ferð síðan aftur inn á síðuna verður staða upplýsingareitssvæðisins og einstakra upplýsingareita endurheimt, byggt á síðustu samskiptum þínum við síðuna. Í sumum tilfellum geturðu hjálpað til við að auka afköst kerfisins með því að draga saman upplýsingareit, því að Finance and Operations þarf ekki að sækja upplýsingar um þann upplýsingareit þar til hann er stækkaður.
- **Aðgerðarsvæði** - *Aðgerðarsvæði* birtist ofarlega á flestum síðum. Aðgerðarsvæðið inniheldur hnappa fyrir margar af aðgerðunum sem þú getur framkvæmt á þessari síðu. Þessum hnöppum er oft raðað niður á flipa. Þú getur opnað alla aðgerðarsíðuna og fest hana þannig, eða þú getur valið að hafa hana samandregna að sjálfgefnu. Næst þegar þú síðan opnar síðuna, mun Finance and Operations endurheimta festa stöðu aðgerðarsíðunnar. Ef aðgerðarsýningin er opnuð og fest þannig, birtir Finance and Operations einnig flipann með aðgerðum sem þú notar síðast.
- **QuickFilters** - A *QuickFilter* birtist fyrir ofan mörg hnitanet. QuickFilter leyfir þér að afmarka hnitanetið, byggt á dálki sem þú velur. Finance and Operations geymir dálkinn sem þú byggðir afmörkunina á. Næst þegar þú síðan opnar síðuna sem inniheldur þetta hnitanet verður hnitanetið afmarkað út frá sömu dálki. Hins vegar geturðu síðan afmarkað hnitanetið út frá öðrum dálki.
- **Dálkhausaafmarkanir** - Þegar þú afmarkar hnitanet með því að nota *Dálkhausaafmarkanir*, geturðu breytt virknitákni afmörkunar eftir þörfum til að finna gögnin sem þú vilt. Til dæmis getur þú breytt virknitákninu frá **byrjar á** til **er nákvæmlega**. Í hvert skipti sem þú notar dálkhausaafmörkun og breytir virknitákni afmörkunar, geymir Finance and Operations breytinguna. Forritið mun síðan endurheimta virknitákn afmörkunar næst þegar þú afmarkar út frá þessum dálki.
- **Yfirlitssvæði** - Þú getur opnað *Yfirlitssvæði* með því að velja **Valmynd** hnappinn vinstra megin á hvaða síðu sem er. (**Valmynd** hnappurinn er stundum nefndur *hamborgari*, *hamborgaravalmynd* eða *hamborgarahnappur*.) Hægt er að opna yfirlitssvæði og festa það þannig, eða þú getur haldið því samandregnu að sjálfgefnu. Eftir að þú hefur opnað yfirlitssvæði og fest það þannig, mun Finance and Operations halda því opinni þar til þú dregur það saman.

## <a name="explicit-personalizations"></a>Beinar sérstillingar
Mismunandi fólk og fyrirtæki hafa mismunandi sjónarhorn á gögnin sem eru mikilvægustu fyrir þá, eða á gögnin sem þau þarfnast ekki vegna þess hvernig reksturinn er uppbyggður. Í Finance and Operations getur þú sérsniðið hvernig upplýsingarnar þínar eru skipulagðar og notaðar. Þú getur einnig tilgreint að einhverjar upplýsingar ætti að vera falin. Þessir eiginleikar er lykillinn að persónulegum og árangursríkum upplifun og eru dæmi um beinar sérstillingar. Beinar sérstillingar eru sérstillingar sem þú setur inn beint, með það fyrir augum að breyta útliti eða hegðun einingar eða síðu.

### <a name="shortcut-menu-options"></a>Flýtivalmynd valkostir
Flýtivalmyndir bjóða upp á nokkrar leiðir til að breyta síðum beint til að verða betur við kröfum þínar eða fyrirtækis þíns. (Flýtivalmynd er einnig þekkt sem *valmynd þegar er hægrismellt* eða *samhengisvalmynd*.)

Sumir af mest dæmigerðu og mikilvægustu breytingum sem hægt er að gera á síðu er hægt að gera beint með því að nota valkostir í flýtivalmynd. Til dæmis, ef byrjað er í verkvangsuppfærslu 17, ef þú vilt bæta við eða fela dálka í hnitaneti skaltu einfaldlega hægrismella í dálkhaus hnitanets og velja síðan **Bæta við dálkum** eða **Fela þennan dálk**.

Að auki eru helstu tegundir beinna sérstillinga tiltækar með því að hægrismella á einingu og síðan velja **Sérsníða**. (Athugaðu að ekki er hægt að sérsníða allar einingar á síðunni þinni.) Þegar þú notar þessa sérstillingaraðferð birtist eiginleikagluggi einingarinnar.

[![Sérsníða eiginleika í einingu](./media/personalization-element-properties.jpg)](./media/personalization-element-properties.jpg)

Þú getur notað eiginleikagluggann til að sérsníða einingu á eftirfarandi hátt:

- Breyta merkimiða einingarinnar.
- Fela eininguna þannig að hún verði ekki sjáanleg á síðunni. Gögnin í reitnum hefur ekki verið eytt eða breytt. Upplýsingarnar birtast bara ekki lengur á síðunni.
- Hafa upplýsingarnar í samantektarhlutanum fyrir flýtiflipa (ef einingin er á flýtiflipa).
- Sleppa reitnum þegar þú ýtir á dálklykilinn til að fara á milli reitanna á síðunni.
- Koma í veg fyrir breytingar á gögnum í reitnum (fyrir allar skrár).

Eiginleikaglugginn gæti falið í sér aðrar sérstillingareiginleika, en það fer eftir einingunni. Til dæmis gæti eiginleikagluggi fyrir flís gefið þér kost á að færa þá flís yfir á mælaborð, og eiginleikaglugginn fyrir mælaborð gæti gefið þér kost á að búa til nýtt vinnusvæði á þeim mælaborði.

### <a name="the-personalization-toolbar"></a>Tækjastika sérstillinga
Ef þú vilt gera margar breytingar á síðu eða gera breytingar sem ekku eru í boði í gegnum kerfið okkar (t.d. endurröðun eininga) getur þú notað tækjastikuna **Sérstillingar**. Til að opna tækjastiku **Sérstillingar** skal velja **Sérsníða þessa skjámynd** í eiginleikaglugga einingar. Þú getur líka valið **Sérsníða þessa skjámynd** í **Sérsníða** hópnum á flipanum **Valkostir** á aðgerðarsíðu hvers síðu.

[![Verkfæraslá sérstillingar](./media/personalization-personalizationtoolbar.jpg)](./media/personalization-personalizationtoolbar.jpg)

#### <a name="navigating-the-page"></a>Farið um síðuna 
Hæfni þína til að vafra um síðuna meðan **Tækjastika sérstillingar** er opin fer eftir verkvangsútgáfunni sem þú keyrir. 

- Fyrir verkvangsuppfærslu 19, meðan tækjastikan **Sérstillingar** er opin, er síðan ritvarin (ekki er hægt að slá neinu inn) og hún er ekki gagnvirk (aðeins er hægt að gera breytingar á sýnilegum einingum á síðunni). Ef þú vilt gera breytingar á einingum innan hluta sem dreginn er saman eða á öðrum flipa þarftu að loka tækjastikunni **Sérstillingar**, stækka hluta eða skipta yfir í viðeigandi flipa og þá enduropna tækjastikuna **Sérstillingar**.  

- Ef byrjað er í verkvangsuppfærslu 19, ef tækjastikan **Sérstillingar** er opin, er síðan enn ritvarin en er mun gagnvirkari. Sér í lagi er hægt að stækka eða fella saman FactBox-svæðið, skipt um flipa og stækka eða fella saman hluta meðan tækjastikan **Sérstillingar** er opin á sama hátt og venjulega á síðunni. Til að koma á sérstilltri breytingu á samandregnum hluta eða flipa (til dæmis til að fela FastTab) virkjar þú hnappinn sem birtist við hliðina á samandregna hlutanum eða flipanum þegar hann fær áherslukassa lyklaborðs eða þegar þú heldur bendlinum yfir honum.  

#### <a name="personalization-tools"></a>Sérstillingartæki
Eftirfarandi verkfæri eru í boði á **Sérstillingar** tækjastikunni:

- Nota **Velja** verkfæri til að velja og breyta eiginleikum einingar. Velja **Velja** verkfæri, og velja síðan eininguna sem breyta á eiginleikunum í. Þegar þú velur einingu birtist eiginleikagluggi einingarinnar og þú getur breytt öllum eiginleikum þeirrar einingar. Þú getur endurtekið ferlið fyrir aðrar einingar sem hægt er að sérsníða á síðunni. En vegna þess hvernig sumir einingar eru notaðir, mun Finance and Operations ekki gef þér kost á að breyta einhverjum af eiginleikum þeirra. Þess vegna, þegar þú velur einingu gætirðu séð að ekki er hægt að breyta sumum eiginleikum þess. Til dæmis getur þú ekki falið reit sem er nauðsynlegur.

- Nota **Færa** verkfærið til að færa einingar á annan stað innan þess hóps eininga sem fyrir er. (Þú getur ekki fært einingu utan yfirhóps hennar). Velja **Færa** verkfærið, og svo eininguna sem þú vilt færa. Þegar þú velur einingu skannar Finance and Operations síðunni til að ákvarða hvert er hægt að færa eininguna. Það býr þá til röð „sleppisvæða.“ Þegar þú færir eininguna til innan hópsins sem fyrir er, er hvert „sleppisvæði“ sýnt sem lituð, feitletruð lína við hliðina á því svæði þar sem má sleppa einingunni.

- Nota **Fela** verkfærið til að fela einingu á síðunni. Velja **Fela** verkfærið, og svo eininguna sem þú vilt fela. Þegar þú velur **Fela** verkfærið, eru allar einingar sem eru faldar sem stendur gerðar sýnilegar og sýndar í skyggðum geymi. Þú getur þá fært þær úr felum. Með því að velja **Velja** verkfærið geturðu séð hvernig síðunni mun líta út þegar völdu einingarnar eru faldar.
    - Ef byrjað er í verkvangsuppfærslu 18 getur þú falið nauðsynlega reiti og hluta sem innihalda nauðsynlega reiti. Þetta gerir þér kleift að búa til einfaldaða upplifun þar sem áskildir reitir sem viðskiptagrunnur gerir sjálfgefna eru ekki sýndir. Faldir nauðsynlegir reitir eru einnig gerðir sýnilegir tímabundið ef þeir eru tómir þegar reynt er að vista. 

- Nota **Yfirlit** verkfærið þegar þú vilt að eining birtist í samantektarhlutanum fyrir flýtiflipa. Samantektarverkfærið gildir aðeins um reiti sem eru í flýtiflipahluta. Þegar þú velur **Samantekt** verkfærið, eru öll reitir sem hafa verið valdir sem samantektarreitir sýndar í skyggðum geymi. Með því að velja reitina getur þú með gagnvirkum hætti fjarlægt og bætt við reitum í samantekt flýtiflipa.

- Nota **Sleppa** verkfærið til að fjarlægja einingu úr fliparöð lyklaborðs síðunnar. Þegar þú velur **Sleppa** verkfærið eru allar einingar sem nú þegar er sleppt sýndar í skyggðum geymi. Þú getur þá gert þær hluti af fliparöðinni aftur.

- Nota **Breyta** verkfærið til að merkja einingu sem annaðhvort breytanlega eða óbreytanlega. Þegar þú velur **Breyta** verkfærið, eru allar einingar sem eru nú þegar óbreytanlegar sýndar í skyggðum geymi. Þú getur þá gert þær breytanlegar aftur. Athugaðu að sumir reitir eru nauðsynlegir og ekki hægt að gera þá óbreytanlega. Hengilásatákn birtist við hliðina á þessum reitum.

- Nota **Setja inn** hnappinn til að sjá lista yfir einingar sem hægt er að setja inn á síðu.
    - Velja **Reitur** verkfærið undir **Setja inn** til að bæta við reit á síðuna þína. Þegar þú notar **Reitur** verkfærið getur þú aðeins bætt við reitum sem eru hluti af skilgreiningu síðunnar og eru ekki sjáanlegar á síðunni sem stendur. Til að fá upplýsingar um hvernig skal búa til nýja reiti sem eru ekki hluti af núverandi skilgreiningu síðunnar, sjá [Sérsniðnir reitir](user-defined-fields.md). Eftir að þú velur **Reitur** verkfærið, þarftu fyrst að velja hópinn eða svæðið þar sem þú vilt bæta við reit. Svargluggi sýnir lista yfir reiti sem tengjast völdum hópi eða svæði. Í svarglugganum skal velja eitt eða fleiri reiti til að bæta við og velja síðan **Setja inn**. Til að fjarlægja reit sem þú hefur áður bætt við, skal endurtaka ferlið, en hreinsa val á reitnum í svarglugganum.
    - Velja **PowerApp** verkfærið undir **Setja inn** til að fella forrit inn í síðuna sem var búið til með því að nota Microsoft PowerApps. Nánari upplýsingar um hvernig á að fella PowerApps forrit inn í síðu er að finna í [Innfelling PowerApps](embed-power-apps.md).

- Velja **Stjórna** hnappinn til að skoða lista yfir stjórnunarvalmöguleika sem tengjast öllum sérstillingum fyrir núverandi síðu.
    - Velja **Hreinsa** til að endurstilla síðuna í sjálfgefið, uppsett ástand. Búið er að hreinsa allar sérstillingar á núverandi síðu. Það er engin afturköllunaraðgerð til. Þess vegna skaltu aðeins nota þennan möguleika ef þú ert viss um að þú viljir endurstilla síðuna.
    - Velja **Flytja inn** til að hlaða inn sérstillingu úr skrá sem þú eða einhver annar bjó til fyrir síðuna áður. Allar núgildandi sérstillingar þínar fyrir síðuna eru skipt út fyrir sérstillingar úr valinni skrá.
    - Velja **Flytja út** til að vista sérstillingar þínar fyrir síðuna í skrá. Þú getur deilt sérstillingunum þínum með öðrum notendum. Þessir notendur þurfa bara að flytja inn skrána sem inniheldur sérstillingarnar þínar fyrir síðuna.

- Velja **Loka** hnappinn til að loka tækjastikunni fyrir **Sérstillingar** og færa síðuna í fyrri gagnvirka stöðu hennar.

Þegar **Sérstillingar** tækjastika er notað, eru vistunaraðgerðir óbeinar. Sérstillingar þínar öðlast gildi um leið og þú skráir þær og þú þarft ekki að velja **Vista** hnapp. Í sumum tilfellum, þegar þú velur verkfæri, birtist hengilásatákn við hliðina á einingu. Þetta tákn gefur til kynna að þú getir ekki breytt einingareiginleikum sem tengjast völdu verkfæri, vegna þess að breytingar á þessum eiginleikum koma í veg fyrir að síðunni virkar rétt.

### <a name="adding-a-tile-list-or-link-to-a-workspace"></a>Bætir við flísum, lista eða hlekkur á vinnusvæði
Fyrir sumar síður sem innihalda lista eru viðbótareiginleikar fyrir sérstillingar í boði. **Bæta við vinnusvæði** hnappurinn í **Sérsníða** hópnum á **Valkostir** flipanum í aðgerðarrúðunni gerir þér kleift að birta upplýsingar úr núverandi lista á tilteknu vinnusvæði. Þú getur sýnt upplýsingar í vinnusvæðinu út frá afmörkun og uppröðun, eða þú getur sýnt þær með sjálfgefnum hætti. Þú getur einnig tilgreint hvort upplýsingarnar birtist í vinnusvæði sem listi, sem samantektarflís sem sýnir fjölda atriða á listanum eða sem tengill.

[![Bæta við vinnusvæði](./media/personalization-addtoworkspace.png)](./media/personalization-addtoworkspace.png)

- Til að bæta lista við vinnusvæði skal fyrst flokka eða afmarka listann á síðunni þannig að hún birti upplýsingarnar eins og þú vilt að þær birtist á vinnusvæðinu. Síðan er **Bæta við vinnusvæði** valið. Velja vinnusvæði, og svo, í **Framsetning** reitnum skal velja **Listi**. Eftir að þú velur **Grunnstilla** birtist gluggi þar sem þú getur valið dálkana sem eiga að birtast á listanum í vinnusvæðinu. Þú getur einnig tilgreint merkið sem á að nota fyrir listann á vinnusvæðinu.
- Til að bæta við flís á vinnusvæði skaltu fyrst afmarka listann á síðunni þannig að hann birti gögnin sem þú vilt að séu samantekin eða vilt fá skjótan aðgang að. Síðan er **Bæta við vinnusvæði** valið. Velja vinnusvæði og svo í reitnum **Framsetning** skal velja **Flís**. Eftir að þú hefur valið **Grunnstilla** birtist svargluggi þar sem þú getur tilgreint merkið sem á að nota fyrir flís á vinnusvæðinu. Þú getur einnig tilgreint hvort flísin ættu að sýna fjölda. Eftir að flís er bætt við vinnusvæðið geturðu valið hana til að opna núverandi síðu frá vinnusvæðinu og skoða afmarkaða listann sem tengist flísinni.
- Til að bæta við tengli á vinnusvæði skaltu fyrst afmarka listann á síðunni þannig að hún birti gögnin sem þú hefur áhuga á. Síðan er **Bæta við vinnusvæði** valið. Veldu vinnusvæði, og síðan, í **Framsetning** reitnum, skal velja **Tengill**. Eftir að þú hefur valið **Grunnstilla** birtist svargluggi þar sem þú getur tilgreint merkið sem á að nota fyrir tengilinn. Þú getur einnig valið tiltekið merki fyrir nýjan hluta sem mun innihalda þennan tengil.

Eftir að listinn þinn, flís eða tengill hefur verið bætt við vinnusvæði getur þú opnað vinnusvæðið og endurraðað einingunum í því eins og þú vilt.

### <a name="adding-a-summary-from-a-workspace-to-a-dashboard"></a>Bæti við samantekt frá vinnusvæði til yfirlits
Sum vinnusvæði innihalda talningarflísar (það er, flísar með tölum), og þú vilt kannski að þessi flísar birtast á yfirlitinu þínu líka. Í vinnusvæði, hægrismelltu á talningarflís og veldu síðan **Sérsníða**. Þá skaltu velja **Festa í yfirlit** í eiginleikaglugga flísarinnar. Í næsta skipti sem þú opnar (og endurglæðir) valið yfirlit, birtist fjöldinn fyrir neðan yfirlitsflísina fyrir það vinnusvæði. Þú getur valið þá talningu til að fara beint á þau gögn sem hún stendur fyrir.

### <a name="personalizing-your-dashboard"></a>Sérsníða yfirlitið þitt
Yfirlitið er iðulega fyrsta síða sem þú sérð þegar þú opnar Finance and Operations. Þú getur sérsniðið yfirlitið þannig að það sýnir aðeins vinnusvæðisflísarnar sem þú vilt sjá. Þú getur einnig umraðað flísunum þannig að þær séu í þeirri röð sem þú vilt sjá þær í, endurnefnt yfirlitsflísar á vinnusvæði eða bæta við alveg nýjum vinnusvæðisflís.

Til að sérsníða yfirlitið, hægri-smelltu á hvaða flís sem er og veldu síðan **Sérsníða** til að opna eiginleikaglugga flísarinnar.

- Ef þú vilt fela eða endurnefna valda flís, getur þú breytt því beint í eiginleikaglugganum.
- Til að endurraða vinnusvæðisflísar skaltu velja **Sérsníða þetta form** í einginleikaglugganum, til að opna **Sérstillingar** tækjastikuna. Þú getur síðan notað **Færa** verkfærið til að raða flísunum eins og þú vilt.
- Til að búa til nýja vinnusvæðisflís skaltu velja **Bæta við vinnusvæði** í eiginleikaglugganum. Ný vinnusvæðisflís er búin til neðst á yfirlitinu. Þú getur endurnefnt þennan nýja vinnusvæðisflís eins og þú vilt. Þú getur einnig bætt við listum, flísum og tenglum á vinnusvæðið eins og lýst er í [Bæta við listum, flísum eða tenglum á vinnusvæði](personalize-user-experience.md#adding-a-tile-list-or-link-to-a-workspace) kafla þessa efnisatriðis.

## <a name="administration-of-personalization"></a>Stjórnun sérstillinga
Eftir að þú hefur sérsniðið síðu, getur deilt stillingunum með öðrum notendum með því að flytja út sérstilltu síðuna. Þú getur þá beðið aðra notendur að opna sérsniðnu síðuna og flytja inn sérstillingarskrána sem þú bjóst til. Að öðrum kosti getur þú gefið notanda, sem hefur stjórnunarheimildir, sérstillinguna þína. Þessi notandi getur síðan virkjað sérstillingarskrána þína í þágu margra notenda á sama tíma.

Notendur sem hafa stjórnunarréttindi geta einnig stýrt sérstillingum fyrir aðra notendur á síðunni **Sérstillingar**. Þessi síða er með fjóra flipa:

- **Virkja** - Hægt er að flytja inn eða velja sérstillingu fyrir einn eða fleiri notendur. Til að virkja sérstillingu í þágu eins eða fleiri notenda, skal velja fyrst hlutverk og notendur sem hafa það hlutverk. Síðan skal velja annaðhvort fyrirliggjandi sérstillingu til að virkja í þágu valdra notenda, eða flytja inn sérstillingarskrá. Sérstillingin er sannprófuð og verður virkjuð í þágu allra valdra notenda næst þegar þeir opna völdu síðuna.
- **Hreinsa** - Þú getur hreinsað allar sérstillingar fyrir síðu eða vinnusvæði fyrir einn eða fleiri notendur. Veldu fyrst síðu eða vinnusvæði til að sjá lista yfir notendur sem hafa notað sérstillingu á það. Veldu síðan þá notendur sem hreinsa skal sérstillingar síðu eða vinnusvæðis hjá og veldu **Hreinsa**. Allar sérstillingar sem völdu notendur hafa virkjað á valdri síðu eða vinnusvæði er eytt. Ekki er hægt að afturkalla þessa aðgerð. Ef sérstilling var hins vegar var vistuð fyrir síðuna eða vinnusvæðið, er hægt að flytja þá sérstillingu inn aftur.
- **Stjórnandi á hvern notanda** - Veldu notanda til að sjá lista yfir síður sem hann eða hún hefur sérstillt. Þú getur þá virkjað eða gert óvirka getu valins notanda til að nota sérstillingar fyrir tilteknar síður eða fyrir allt kerfið. Þú getur einnig flutt inn, flutt út eða hreinsað sérstillingar valins notanda.
- **Kerfi** - Einnig er hægt að aftengja öllum sérstillingum allra notendur kerfisins tímabundið. Í þessu tilviki er sérstillingunum eytt. Allar síður eru endurstilltar í sjálfgefna stöðu fyrir alla notendur. Ef þú endurvirkjar sérstillingar seinna, verða allar sérstillingar settar í virkni á ný. Einnig er hægt að eyða öllum sérstillingum endanlega fyrir alla notendur kerfisins. Það er engin leið til að endurheimta sérstillingar sem hefur verið eytt. Áður en þú framkvæmir þetta verkefni skaltu þess vegna vera viss um að flytja út allar sérstillingar sem þú gætir viljað síðar.

## <a name="personalization-of-inventory-dimensions"></a>Sérstilling birgðavídda

Þegar þú sérstillir uppsetningu birgðavídda á síðu, skaltu hafa í huga stillingarnar sem hafa verið búnar til með notkun valkostarins **Sýna víddir**. Til dæmis notar þú sérstillingu til að fela dálk sem inniheldur birgðavídd rununúmers, en dálkurinn birtist næst þegar síðunni er opnuð. Þessi hegðun á sér stað vegna þess að **Birting vídda** stillingarnar stjórna birgðavíddadálkunum sem eru sýndir.

**Birting vídda** stillingarnar eiga við um allar síður og hnekkja öllum sérstilltum uppsetningum á birgðavíddareitum á einstökum síðum.

Ef þú vilt því ekki að dálkur sem inniheldur birgðavídd rununúmers birtist í framangreindu dæmi, verður þú að hreinsa þá vídd sem hluti af **Sýna víddir** valkostinum fyrir töfluna. Að lokum mun þessi breyting ekki aðeins gilda á einni tilteknu síðu heldur á öllum síðum.

