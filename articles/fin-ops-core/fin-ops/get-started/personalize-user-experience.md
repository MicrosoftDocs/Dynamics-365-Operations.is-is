---
title: Sérsníða notandaupplifun
description: Þessi grein útskýrir hvernig hægt er að sérsníða forritið.
author: jasongre
manager: AnnBe
ms.date: 02/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserSetup, DefaultDashboard
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 62363
ms.assetid: 57b445d7-3e9e-4228-8728-f63b9dbd77a3
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c745248a0c7e54b58b1d3e491f3bbb067ec0e2c2
ms.sourcegitcommit: d8a2301eda0e5d0a6244ebbbe4459ab6caa88a95
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/06/2020
ms.locfileid: "3029363"
---
# <a name="personalize-the-user-experience"></a>Sérsníða notandaupplifun

[!include [banner](../includes/banner.md)]

Þessi grein útskýrir hvernig hægt er að sérsníða forritið.

Það eru þrír grunnflokkar sérsniða.

- Sérstillingar sem eru gerðar á uppsetningarsíðu. Til dæmis stillingar á litaþema og tímabelti.
- Sérstillingar sem tengjast síðunotkun. Þessar sérstillingar eru kallaðar *óbeinar* sérstillingar. Til dæmis fylgist kerfið með breidd dálka í hnitaneti ef þú stillir þá, og hvort flýtiflipar eru útvíkkaðir eða samandregnir.
- Sérstillingar sem notandi gerir á útliti á síðu með því að breyta því hvernig eining birtist eða virkar á þeirri síðu, oft í gegnum gagnvirkan sérstillingarham. Þessar sérstillingar eru kallaðar *beinar* sérstillingar. Til dæmis getur notandinn bætt við, falið eða endurraðað einingum á síðunni.

Allar sérstillingar sem notandi gerir eru aðeins fyrir þann notanda, óháð gerð sérstillingar eða því fyrirtæki sem notandinn á í samskiptum við á þeim tíma. Breytingarnar sem notandi gerir á síðu hefur ekki áhrif á aðra notendur í kerfinu.

## <a name="system-wide-options-for-the-current-user"></a>Kerfisaltækir valkostir fyrir núverandi notanda

**Notandavalkostir** síðan inniheldur nokkrar kerfisaltækar stillingar fyrir núverandi notanda. Til að opna síðuna **Notandavalkostir** skaltu velja hnappinn **Stillingar** (táknið fyrir gír) á yfirlitsstikunni og velja síðan **Notandavalkostir**. **Notandavalkostir** síðan hefur fjóra flipa sem innihalda ýmsar notandastillingar:

- **Sjónrænt** - Veldu litaþema og sjálfgefna stærð eininga á síðum.
- **Kjörstillingar** - Veldu sjálfgefin gildi sem eru notuð í hvert skipti sem þú opnar kerfið. Þessi gildi eru meðal annars fyrirtækið, upphafssíðan og sjálfgefið skoða/breyta hamurinn. (Skoða/breyta hamurinn ákvarðar hvort síða sé læst í skoðun eða opin fyrir breytingar í hvert skipti sem þú opnar hana.) Þessi flipi inniheldur einnig valkosti fyrir tungumálið, tímabeltið og dagsetningu, tíma og númerasnið. Að lokum inniheldur þessi flipi nokkrar fjölbreytilegar kjörstillingar sem eru mismunandi frá útgáfu til útgáfu.
- **Notandareikningur** - Stilla notandanafnið þitt og aðrar valkosti sem tengjast notandareikningi.
- **Vinnuflæði** - Veldu verkflæðatengda valkosti.

Fyrir utan að breyta notandastillingum þínum geturðu einnig nota síðuna **Notkunargögn** til að skoða og eyða notkunargögnum og sérstillingum. Veldu bara **Notkunargögn** í aðgerðarglugganum.

Þegar þú notar forritið geymist mikið af vali þínu í minni til að gera kerfið auðveldara í notkun í framtíðinni. Á flipanum **Sérstillingar** er hægt að skoða og stýra sérsniðnum breytingum sem þú hefur gert á síðum í kerfinu. Á þessum flipa er einnig hægt að núllstilla skýringatexta (það er að segja sprettigluggana sem kynna nýja kerfiseiginleika). Þú verður síðan látin/n vita aftur af eiginleikum sem áður hafa fundist.

> [!NOTE]
> Ef kveikt er á eiginleikanum [Vistuð yfirlit](saved-views.md) er hægt að skoða og stjórna sérstillingum þínum með því að velja **Sérstillingar** í aðgerðarglugganum á síðunni **Notendastillingar**.

## <a name="implicit-personalizations"></a>Óbeinar sérstillingar

Óbeinar sérstillingar eru þær sérstillingar sem þú gerir aðeins með því að hafa samskipti við stjórntæki sem geyma núverandi sýnilegt ástand þeirra.

- **Breidd dálka í hnitaneti** - Hægt er að stilla breidd dálks í hnitaneti með því að velja stækkunarstikuna vinstra eða hægra megin við dálkhausinn og síðan renna henni til vinstri eða hægri þar til dálkurinn nær ákjósanlegri breidd. Fottirtið geymir breiddina sem þú stillir fyrir dálk. Forritið breytir síðan dálknum í þá breidd í hvert sinn sem þú opnar síðuna sem inniheldur það hnitanet.
- **Dálkasamtölur hnitanets** - (Aðeins fáanlegt með nýju ristjórninni virkt) Þú getur ákveðið hvort heildar skuli sýndur neðst í hvaða tölustafa dálki sem er í töflunni, og hvort netfætinn sé sýnilegur. Forritið geymir þessi gögn þannig að þessar stillingar eru munaðar næst þegar þú opnar síðuna. Sjáðu [Hnitanetsgeta](grid-capabilities.md) efni fyrir frekari upplýsingar. 
- **Flýtiflipar** - Sumar síður hafa stækkanlega hluta sem eru þekktir sem *Flýtiflipar*. Forritið geymir upplýsingar um flýtiflipana sem þú hefur víkkað út og dregið saman. Í næsta skipti sem þú opnar síðan síðuna, verða sömu flýtifliparnir annaðhvort víkkaðir út eða dregnir saman, byggt á síðustu samskiptum þínum við síðuna. Í sumum tilfellum geturðu hjálpað til við að auka afköst kerfisins með því að draga saman flýtiflipa, því forritið þarf ekki að sækja upplýsingar um þá flýtiflipa þar til þeir eru stækkaðir. Eins og útskýrt er síðar í þessu efnisatriði geturðu einnig breytt röð flýtiflipanna á síðu.
- **Staðreyndareitir** - Sumar síður eru með gluggann **Tengdar upplýsingar** sem sýnir skrifvarðar upplýsingar sem tengjast núverandi efni síðunnar. Sérhver hluti í glugganum **Tengdar upplýsingar** kallast *Upplýsingareitur*. Þú getur stækkað eða minnkað gluggann **Tengdar upplýsingar** og þú getur einnig útvíkkað eða dregið saman einstaka upplýsingareiti. Forritið geymir þetta kjörval. Í næsta skipti sem þú opnar síðuna verður glugginn **Tengdar upplýsingar** og stakir upplýsingareitir annaðhvort stækkaðir eða minnkaðir, byggt á síðustu samskiptum þínum við síðuna. Í sumum tilfellum geturðu hjálpað til við að auka afköst kerfisins með því að draga saman upplýsingareit, því forritið þarf ekki að sækja upplýsingar um þá upplýsingareiti fyrr en þeir eru stækkaðir.
- **Aðgerðarsvæði** - *Aðgerðarsvæði* birtist ofarlega á flestum síðum. Aðgerðarsvæðið inniheldur hnappa fyrir margar af aðgerðunum sem þú getur framkvæmt á þessari síðu. Þessum hnöppum er oft raðað niður á flipa. Þú getur „fest“ alla aðgerðarsíðuna sem opna eða þú getur valið að hafa hana samandregna að sjálfgefnu. Í næsta skipti sem þú opnar síðan síðuna, verðut aðgerðaglugginn annaðhvort opinn eða dreginn saman, byggt á síðustu samskiptum þínum við síðuna. Ef þú festir aðgerðargluggann sem opinn verður síðasti flipinn sem þú notaðir sýndur.
- **QuickFilters** - A *QuickFilter* birtist fyrir ofan mörg hnitanet. QuickFilter leyfir þér að afmarka hnitanetið, byggt á dálki sem þú velur. Forritið geymir dálkinn sem þú byggðir afmörkunina á. Næst þegar þú síðan opnar síðuna sem inniheldur þetta hnitanet verður hnitanetið afmarkað út frá sömu dálki. Hins vegar geturðu síðan valið annan dálk til að síða hnitanetið út frá.
- **Dálkhausaafmarkanir** - Þegar þú afmarkar hnitanet með því að nota *Dálkhausaafmarkanir*, geturðu breytt virknitákni afmörkunar eftir þörfum til að finna gögnin sem þú vilt. Til dæmis getur þú breytt virknitákninu frá **byrjar á** til **er nákvæmlega**. Í hvert skipti sem þú notar dálkhausaafmörkun og breytir virknitákni afmörkunar, geymir forritið breytinguna. Síðan, í næsta skiptið sem þú afmarkar út frá þessum dálki mun virknitákn afmörkunar verða endurheimt.
- **Yfirlitssvæði** - Þú getur opnað *Yfirlitssvæði* með því að velja hnappinn **Stækka yfirlitssvæðið** efst vinstra megin á hvaða síðu sem er. (Þessi hnapp er stundum nefndur _**Valmynd** hnappur_, *hamborgari*, *hamborgaravalmynd* eða *hamborgarahnappur*.) Hægt er að opna yfirlitssvæði og festa það þannig, eða þú getur haldið því samandregnu að sjálfgefnu. Eftir að þú hefur opnað yfirlitssvæði og fest það þannig, mun foritið halda því opnu þar til þú dregur það saman.

## <a name="explicit-personalizations"></a>Beinar sérstillingar

Mismunandi fólk og fyrirtæki hafa mismunandi sjónarhorn á gögnin sem eru mikilvægustu fyrir þá, og á gögnin sem þau þarfnast ekki vegna þess hvernig reksturinn er uppbyggður. Þú getur sérsniðið hvernig upplýsingarnar þínar eru skipulagðar og notaðar. Þú getur einnig tilgreint að einhverjar upplýsingar ætti að vera falin. Þessir eiginleikar er lykillinn að persónulegum og árangursríkum upplifun og eru dæmi um beinar sérstillingar. Beinar sérstillingar eru sérstillingar sem þú setur inn beint, vegna þess að þú vilt breyta útliti eða hegðun einingar eða síðu.

### <a name="shortcut-menu-options"></a>Flýtivalmynd valkostir

Flýtivalmyndir bjóða upp á nokkrar leiðir til að breyta síðum beint svo að þær mæti kröfum þínum betur eða fyrirtækis þíns. (Flýtivalmynd er einnig þekkt sem *valmynd þegar er hægrismellt* eða *samhengisvalmynd*.)

Sumir af mest dæmigerðu og mikilvægustu breytingum sem hægt er að gera á síðu er hægt að gera beint með því að nota valkostir í flýtivalmynd. Til dæmis, ef byrjað er í verkvangsuppfærslu 17, ef þú vilt bæta við eða fela dálka í hnitaneti skaltu einfaldlega hægrismella í dálkhaus og velja síðan **Bæta við dálkum** eða **Fela þennan dálk**.

Að auki eru helstu tegundir beinna sérstillinga tiltækar með því að hægrismella á einingu og síðan velja **Sérsníða**. (Athugaðu að ekki er hægt að sérsníða allar einingar á síðunni þinni.) Þegar þú notar þessa sérstillingaraðferð birtist eiginleikagluggi einingarinnar.

![Sérsníða eiginleika í einingu](./media/personalization-element-properties.png)

Þú getur notað eiginleikagluggann til að sérsníða einingu á eftirfarandi hátt:

- Breyta merkimiða einingarinnar.
- Fela eininguna þannig að hún verði ekki sjáanleg á síðunni. Gögnin í reitnum hefur ekki verið eytt eða breytt. Upplýsingarnar birtast bara ekki lengur á síðunni.
- Hafa upplýsingarnar í samantektarhlutanum fyrir flýtiflipa (ef einingin er á flýtiflipa).
- Slepptu reitnum, svo að hann fái aldrei fókus þegar þú flettir í gegnum síðuna.
- Koma í veg fyrir breytingar á gögnum í reitnum (fyrir allar skrár).

Eiginleikaglugginn gæti falið í sér aðrar sérstillingareiginleika, en það fer eftir einingunni. Til dæmis gæti eiginleikagluggi fyrir flís gefið þér kost á að færa þá flís yfir á mælaborð, og eiginleikaglugginn fyrir mælaborð gæti gefið þér kost á að búa til nýtt vinnusvæði á þeim mælaborði.

### <a name="the-personalization-toolbar"></a>Tækjastika sérstillinga

Ef þú vilt gera margar breytingar á síðu eða gera breytingar sem ekki eru í boði í gegnum annan búnað (t.d. ef þú vilt endurraða einingum) getur þú notað tækjastikuna **Sérstillingar**. Til að opna verkfæraslána **Sérstillingar** skaltu fylgja einu af þessum skrefum:

- Veldu **Aðlaga þessa síðu** í eiginleikaglugga einingarinnar.
- Veldu **Sérsníða þessa síðu** í flokknum **Sérsníða** á flipanum **Valkostir** í aðgerðaglugga einhverrar síðu.
- Veldu hnappinn **Stillingar** (gírtáknið) á leitarstikunni og veldu síðan **Sérsníða**.

[![Verkfæraslá sérstillingar](./media/restyledPersonalizationToolbar.png)](./media/restyledPersonalizationToolbar.png)

#### <a name="navigating-the-page"></a>Farið um síðuna

Þegar verkfærasláin **Sérstilling** er opin er undirliggjandi síða skrifvarin (með öðrum orðum, þú getur ekki breytt gögnum), en hún er samt gagnvirk. Sérstaklega er hægt að stækka eða minnka gluggann **Tengdar upplýsingar**, skipta um flipa og stækka eða minnka hluta, rétt eins og þú framkvæmir venjulega þessar aðgerðir á síðunni. Til að koma á sérstillingu á samandregnum hluta eða flipa (til dæmis til að fela flýtiflipa) þarftu aðeins að velja hnappinn sem birtist við hliðina á þeim hluta eða flipa þegar hann fær áherslukassa lyklaborðs eða þegar þú heldur bendlinum yfir honum.

#### <a name="personalization-tools"></a>Sérstillingartæki

Eftirfarandi verkfæri eru í boði á **Sérstillingar** tækjastikunni:

- Nota **Velja** verkfæri til að velja og breyta eiginleikum einingar. Til að nota þetta tól velurðu hnappinn **Velja** á verkfæraslánni og síðan viðkomandi einingu. Eiginleikagluggi einingarinnar birtist og þú getur breytt öllum eiginleikum þeirrar einingar. Þú getur endurtekið ferlið fyrir aðrar einingar sem hægt er að sérsníða á síðunni. Athugaðu að sumir eiginleikar sérstillinga eru mögulega ekki tiltækir í sumum aðstæðum. Til dæmis getur þú ekki læst reit sem er nauðsynlegur.
- Nota **Fela** verkfærið til að fela einingu á síðunni. Til að nota þetta tól velurðu hnappinn **Fela** á verkfæraslánni og síðan einingu sem á að fela. Þegar þú notar verkfærið **Fela**, eru allar einingar sem eru faldar sem stendur gerðar sýnilegar en sýndar í skyggðum gám. Þú getur síðan gert þátt sýnilegan með því að velja hann. Til að sjá hvernig síðan mun líta út þegar þættir eru faldir skaltu skipta yfir í annað sérstillingaverkfæri.
- Notaðu verkfærið **Bæta við reit** til að bæta reit við á síðuna. Þegar þú notar þetta verkfæri geturðu aðeins bætt við reitum sem eru hluti af skilgreiningunni á síðunni. Til að fá upplýsingar um hvernig skal búa til nýja reiti sem eru ekki hluti af núverandi skilgreiningu síðunnar, sjá [Stofna og vinna með sérsniðna reiti](user-defined-fields.md). Eftir að þú velur hnappinn **Bæta við reit** á verkfæraslánni þarftu fyrst að velja hópinn eða svæðið þar sem þú vilt bæta við reit. Svargluggi mun sýna lista yfir reiti sem tengjast völdum hópi eða svæði. Í svarglugganum skal velja eitt eða fleiri reiti til að bæta við og velja síðan **Setja inn**. Til að fjarlægja reit sem þú hefur áður bætt við, skal endurtaka ferlið, en hreinsa val á reitnum í svarglugganum.
- Nota **Færa** verkfærið til að færa einingar á annan stað í núverandi hóp eininga. Athugaðu að ekki er hægt að færa einingu utan yfirhóps hennar. Til að nota þetta tól velurðu hnappinn **Flytja** á verkfæraslánni og síðan einingu sem á að flytja. Þegar þú velur einingu ákvarðar forritið staðsetningar þar sem flytja má eininguna. Þessir staðir eru þekktir sem *sleppisvæði*. Þegar þú færir eininguna til í núverandi hóp er hvert sleppisvæði sýnt sem lituð, feitletruð lína við hliðina á því svæði þar sem má sleppa einingunni.
- Nota **Sleppa** verkfærið til að fjarlægja einingu úr fliparöð lyklaborðs síðunnar. Þegar þú velur hnappinn **Sleppa** á verkfæraslánni eru allar einingar sem nú þegar er sleppt sýndar í skyggðum gámi. Þú getur fjarlægt eða bætt við reitum á fliparöðinni með gagnvirkum hætti.
- Notaðu verkfærið **Sýna í haus** þegar þú vilt að reitur birtist í samantektarhlutanum fyrir flýtiflipa. Þegar þú velur hnappinn **Sýna í haus** á verkfæraslánni eru allir reitir sem hafa verið valdir sem samantektarreitir sýndar í skyggðum gámi. Með því að velja reitina getur þú með gagnvirkum hætti fjarlægt og bætt við reitum þaðan.
- Notaðu verkfærið **Læsa** til að merkja einingu sem annaðhvort breytanlega eða óbreytanlega. Þegar þú velur hnappinn **Læsa** á verkfæraslánni eru allar einingar sem eru þegar óbreytanlegar sýndar í skyggðum gámi. Þú getur þá gert þær breytanlegar aftur. Athugaðu að sumir reitir eru nauðsynlegir og ekki hægt að gera þá óbreytanlega. Hengilásatákn birtist við hliðina á þessum reitum.
- Notaðu hnappinn **Bæta við forriti úr Power Apps** til að fella forrit inn á síðuna sem var búið til með því að nota Microsoft Power Apps. Nánari upplýsingar um hvernig á að fella inn forrit frá Power Apps á síðu er að finna í [Innfelling á forritum úr Power Apps](embed-power-apps.md). Þessi valkostur er aðeins í boði þegar aðgerðin [Vistaðar skoðanir](saved-views.md) er óvirk.  
- Notaðu hnappinn **Bæta við forriti** til að fella inn forrit, annaðhvort forrit stofnað í Microsoft Power Apps eða frá þriðja aðila, á síðuna. Þessi valkostur er aðeins í boði þegar aðgerðin [Vistaðar skoðanir](saved-views.md) er virkjuð. 
- Notaðu verkfærið **Hreinsa** til að endurstilla síðuna í sjálfgefið, uppsett ástand. Allar sérstillingar á núverandi síðu verða hreinsaðar. Það er engin afturköllunaraðgerð til. Þess vegna skaltu aðeins nota þetta verkfæri ef þú ert viss um að þú viljir endurstilla síðuna.
- Notaðu verkfærið **Flytja inn** til að hlaða inn sérstillingu úr skrá sem þú eða einhver annar bjó til áður. Þegar þú flytur inn sérstillingar fyrir síðu geturðu valið hvort þeim skuli bætt við eða komið í stað allra núverandi sérstillinga fyrir síðuna. Það er engin afturköllunaraðgerð til. Þess vegna, eftir að þú hefur flutt inn sérstillingar, verðurðu að hreinsa handvirkt eða afturkalla allar breytingar sem þú vilt ekki.
- Notaðu verkfærið **Flytja út** til að vista sérstillingar þínar fyrir síðuna í skrá. Síðan geturðu deilt sérstillingunum þínum með öðrum notendum. Þessir notendur þurfa bara að flytja inn skrána sem inniheldur sérstillingarnar þínar fyrir síðuna.
- Velja **Loka** hnappinn til að loka tækjastikunni fyrir **Sérstillingar** og færa síðuna í fyrri gagnvirka stöðu hennar.

Hefð er fyrir því þegar verkfærasláin **Sérstillingar** er notuð, að sérstillingarnar taka gildi um leið og þú gerir þær. Hins vegar, ef kveikt er á eiginleikanum [Vistaðar skoðanir](saved-views.md), verður þú að vista sérstillingar beint í það yfirliti sem þú velur.

Í sumum tilfellum, þegar þú velur verkfæri, birtist hengilásatákn við hliðina á einingu. Þetta tákn gefur til kynna að þú getir ekki breytt einingareiginleikum sem tengjast völdu verkfæri, vegna þess að breytingar á þessum eiginleikum koma í veg fyrir að síðunni virkar rétt.

### <a name="adding-a-tile-list-or-link-to-a-workspace"></a>Bætir við flísum, lista eða hlekkur á vinnusvæði

Fyrir sumar síður sem innihalda lista er sérstillingaraðgerðin **Bæta við vinnusvæði** fáanleg í hópnum **Sérsníða** á flipanum **Valkostir** á Aðgerðarrúðunni. Þessi aðgerð gerir þér kleift að ýta viðeigandi upplýsingum úr núverandi lista yfir á tiltekið vinnusvæði. Upplýsingarnar sem birtast í vinnusvæðinu geta verið byggðar á annaðhvort öllum listanum eða afmarkaðri og flokkaðri útgáfu af listanum. Þú getur einnig tilgreint hvort upplýsingarnar birtist í vinnusvæði sem listi, sem samantektarreit sem sýnir fjölda atriða á listanum eða sem tengill.

> [!NOTE]
> Ef kveikt er á eiginleikanum [Vistaðar skoðanir](saved-views.md) er efnið sem þú ýtir á vinnusvæði beintengt við yfirlit. Fyrirspurn skjásins er notuð til að sækja gögn í vinnusvæðið og samsvarandi reitur eða hlekkur í vinnusvæðinu opnar síðuna fyrir þá skoðun, þannig að fyrirspurn skjásins og stillingar eru notuð á það.

[![Bæta við vinnusvæði](./media/personalization-addtoworkspace.png)](./media/personalization-addtoworkspace.png)

- Til að bæta lista við vinnusvæði skal fyrst flokka eða afmarka listann á síðunni þannig að hún birti upplýsingarnar eins og þú vilt að þær birtist á vinnusvæðinu. (Ef kveikt er á eiginleikanum Vistaðar skoðanir er ekki hægt að halda áfram fyrr en þú vistar skoðun með þessi skilyrði.) Veldu síðan **Bæta við vinnusvæði**. Velja vinnusvæði, og svo, í **Framsetning** reitnum skal velja **Listi**. Eftir að þú velur **Grunnstilla** birtist gluggi þar sem þú getur valið dálkana sem eiga að birtast á listanum í vinnusvæðinu. Þú getur einnig tilgreint merkið sem er notað fyrir listann á vinnusvæðinu.
- Til að bæta við reit á vinnusvæði skaltu fyrst afmarka listann á síðunni þannig að hann birti gögnin á að gera yfirlit yfir eða þú vilt fá skjótan aðgang að. (Ef kveikt er á eiginleikanum Vistaðar skoðanir er ekki hægt að halda áfram fyrr en þú vistar skoðun með þessi skilyrði.) Veldu síðan **Bæta við vinnusvæði**. Velja vinnusvæði og svo í reitnum **Framsetning** skal velja **Flís**. Eftir að þú hefur valið **Grunnstilla** birtist svargluggi þar sem þú getur tilgreint merkið sem á að nota fyrir reit á vinnusvæðinu. Þú getur einnig tilgreint hvort flísin ættu að sýna fjölda. Eftir að reitum er bætt við vinnusvæðið geturðu valið það til að opna núverandi síðu úr vinnusvæðinu. Þú getur síðan skoðað afmarkaðan lista sem er tengdur reitnum.
- Til að bæta við tengli á vinnusvæði skaltu fyrst afmarka listann á síðunni þannig að hún birti gögnin sem þú hefur áhuga á. (Ef kveikt er á eiginleikanum Vistaðar skoðanir er ekki hægt að halda áfram fyrr en þú vistar skoðun með þessi skilyrði.) Veldu síðan **Bæta við vinnusvæði**. Veldu vinnusvæði, og síðan, í **Framsetning** reitnum, skal velja **Tengill**. Eftir að þú hefur valið **Grunnstilla** birtist svargluggi þar sem þú getur tilgreint merkið sem á að nota fyrir tengilinn. Þú getur einnig valið tiltekið merki fyrir nýjan hluta sem inniheldur þennan tengil.

Þegar þú hefur bætt lista, reit eða tengli við vinnusvæði getur þú opnað vinnusvæðið og endurraðað einingunum í því eins og þú vilt.

### <a name="adding-a-summary-from-a-workspace-to-a-dashboard"></a>Bæti við samantekt frá vinnusvæði til yfirlits

Sum vinnusvæði innihalda talningarflísar (það er, flísar með tölum), og þú vilt kannski að þessi flísar birtast á yfirlitinu þínu líka. Á vinnusvæði skal hægrismella á talningarreitinn og velja **Sérsníða**, og velja síðan **Festa við stjórnborð** í eiginleikaglugga reitsins. Síðan í næsta skipti sem þú opnar og endurglæðir valið yfirlit, birtist fjöldinn fyrir neðan yfirlitsflísina fyrir það vinnusvæði. Þú getur valið þá talningu til að fara beint á þau gögn sem hún stendur fyrir.

### <a name="personalizing-your-dashboard"></a>Sérsníða yfirlitið þitt

Yfirlitið er iðulega fyrsta síða sem þú sérð þegar þú opnar forritið. Þú getur sérsniðið yfirlitið þannig að það sýnir aðeins vinnusvæðisflísarnar sem þú vilt sjá. Þú getur einnig umraðað reitunum þannig að þeir birtist í þeirri röð sem þú vilt sjá þá í, endurnefnt yfirlitsreiti á vinnusvæði eða bæta við nýjum vinnusvæðisreit.

Til að sérsníða yfirlitið, hægri-smelltu á hvaða flís sem er og veldu síðan **Sérsníða** til að opna eiginleikaglugga flísarinnar.

- Ef þú vilt fela eða endurnefna valda flís, getur þú breytt því beint í eiginleikaglugganum.
- Til að endurraða vinnusvæðisflísar skaltu velja **Sérsníða þetta form** í einginleikaskjámyndinni, til að opna **Sérstillingar** tækjastikuna. Þú getur síðan notað **Færa** verkfærið til að endurraða reitunum eins og þú vilt.
- Til að bæta við nýjum vinnusvæðisreit skaltu velja **Bæta við vinnusvæði** í eiginleikaglugganum. Ný vinnusvæðisflís er búin til neðst á yfirlitinu. Þú getur endurnefnt þennan nýja vinnusvæðisflís eins og þú vilt. Þú getur einnig bætt við listum, flísum og tenglum á vinnusvæðið eins og lýst er í [Bæta við listum, flísum eða tenglum á vinnusvæði](#adding-a-tile-list-or-link-to-a-workspace) kafla þessa efnisatriðis.

## <a name="administration-of-personalizations"></a>Stjórnun sérstillinga

Eftir að þú hefur sérsniðið síðu, getur deilt stillingunum með öðrum notendum með því að flytja út sérstilltu síðuna. Þú getur þá beðið aðra notendur að opna sérsniðnu síðuna og flytja inn sérstillingarskrána sem þú bjóst til. Að öðrum kosti getur þú gefið notanda, sem hefur stjórnunarheimildir, sérstillinguna þína. Þessi notandi getur síðan virkjað sérstillingarskrána þína í þágu margra notenda á sama tíma.

Notendur sem hafa stjórnunarréttindi geta einnig stýrt sérstillingum fyrir aðra notendur á síðunni **Sérstillingar**.

Fyrir viðskiptavini sem hafa ekki kveikt á eiginleikanum [Vistaðar skoðanir](saved-views.md) er þessi síða með fjóra flipa:

- **Virkja** - Hægt er að flytja inn eða velja sérstillingu fyrir einn eða fleiri notendur. Til að virkja sérstillingu í þágu eins eða fleiri notenda, skal velja fyrst hlutverk og notendur sem hafa það hlutverk. Síðan skal velja annaðhvort fyrirliggjandi sérstillingu til að virkja í þágu valdra notenda, eða flytja inn sérstillingarskrá. Sérstillingin er sannprófuð og verður virkjuð í þágu allra valdra notenda næst þegar þeir opna völdu síðuna.
- **Hreinsa** - Þú getur hreinsað allar sérstillingar fyrir síðu eða vinnusvæði fyrir einn eða fleiri notendur. Veldu fyrst síðu eða vinnusvæði til að sjá lista yfir notendur sem hafa notað sérstillingu á það. Veldu síðan þá notendur sem hreinsa skal sérstillingar síðu eða vinnusvæðis hjá og veldu **Hreinsa**. Allar sérstillingar sem völdu notendur hafa virkjað á valdri síðu eða vinnusvæði er eytt. Ekki er hægt að afturkalla þessa aðgerð. Ef sérstilling var hins vegar var vistuð fyrir síðuna eða vinnusvæðið, er hægt að flytja þá sérstillingu inn aftur.
- **Notendur** - Veldu notanda til að sjá lista yfir síður sem notandinn hefur sérstillt. Síðan geturðu kveikt eða slökkt á getu valins notanda til að nota sérstillingar fyrir tilteknar síður eða fyrir allt kerfið. Þú getur einnig flutt inn, flutt út eða hreinsað sérstillingar notanda. Að auki geturðu endurstillt skýringartexta eiginleika fyrir notandann. Í þessu tilfelli, ef notandi hefur áður sagt upp öllum sprettigluggum sem kynna nýja eiginleika, munu þeir birtast aftur næst þegar notandinn lendir í þessum aðgerðum.
- **Kerfi** - Einnig er hægt að slökkva á sérstillingum allra notendur kerfisins tímabundið. Í þessu tilfelli er öllum sérstillingum eytt fyrir alla notendur og allar síður eru endurstilltar í sjálfgefna stöðu. Ef þú kveikir aftur á sérstillingum verður öllum sérstillingumaftur beitt. Einnig er hægt að eyða öllum sérstillingum endanlega fyrir alla notendur kerfisins. Ekki er hægt að endurheimta sérstillingar sem hefur verið eytt. Áður en þú framkvæmir þetta verkefni skaltu þess vegna vera viss um að flytja út allar sérstillingar sem þú gætir viljað síðar.

Fyrir viðskiptavini sem hafa kveikt á eiginleikanum [Vistaðar skoðanir](saved-views.md) er síðan **Sérstillingar** með fimm flipa:

- **Útgefnar skoðanir** - Þessar skoðanir hafa verið gefnar út fyrir fyrirtækið. Til að breyta notendum sem þessar skoðanir miðast við geturðu breytt öryggishlutverkum eða lögaðilum sem tengjast hverri skoðun. Þú getur líka flutt út eða eytt einni eða fleiri útgefnum skoðunum.
- **Óbirt yfirlit** - Þessar skoðanir eru sniðmát sem hefur verið flutt inn í kerfið þitt en hefur ekki enn verið birt. Þú getur birt, flutt út eða eytt þessum skoðunum.
- **Persónuleg yfirlit** - Þessar skoðanir hafa verið búnar til af notendum í kerfinu. Þú getur gefið út persóunlegt yfirlit til fyrirtækisins, eða afritað eina eða fleiri af þessum skoðunum til annarra notenda. Einnig er hægt að birta, flytja út eða eyða þessum skoðunum, eftir þörfum.
- **Notendur** - Veldu notanda til að sjá lista yfir síður sem notandinn hefur sérstillt. Síðan geturðu kveikt eða slökkt á getu valins notanda til að nota sérstillingar fyrir tilteknar síður eða fyrir allt kerfið. Þú getur einnig flutt inn, flutt út eða hreinsað sérstillingar notanda. Að auki geturðu endurstillt skýringartexta eiginleika fyrir notandann. Í þessu tilfelli, ef notandi hefur áður sagt upp öllum sprettigluggum sem kynna nýja eiginleika, munu þeir birtast aftur næst þegar notandinn lendir í þessum aðgerðum.
- **Kerfi** - Einnig er hægt að slökkva á sérstillingum allra notendur kerfisins tímabundið. Í þessu tilfelli er öllum sérstillingum eytt fyrir alla notendur og allar síður eru endurstilltar í sjálfgefna stöðu. Ef þú kveikir aftur á sérstillingum verður öllum sérstillingumaftur beitt. Einnig er hægt að eyða öllum sérstillingum endanlega fyrir alla notendur kerfisins. Ekki er hægt að endurheimta sérstillingar sem hefur verið eytt. Áður en þú framkvæmir þetta verkefni skaltu þess vegna vera viss um að flytja út allar sérstillingar sem þú gætir viljað síðar.

Notendur sem hafa aðgang að síðunni **Sérstillingar** geta einnig flutt inn persónulegar skoðanir eða sniðmát með því að nota hnappinn **Flytja inn skoðanir** á aðgerðarrúðunni.

## <a name="personalizing-inventory-dimensions"></a>Sérstilling birgðavídda

Þegar þú sérstillir uppsetningu birgðavídda á síðu, skaltu hafa í huga stillingarnar sem hafa verið búnar til með notkun valkostarins **Sýna víddir**. Til dæmis notar þú sérstillingu til að fela dálk sem inniheldur birgðavídd rununúmers, en dálkurinn birtist næst þegar síðunni er opnuð. Þessi hegðun á sér stað vegna þess að **Birting vídda** stillingarnar stjórna birgðavíddadálkunum sem eru sýndir. **Birting vídda** stillingarnar eiga við um allar síður og hnekkja öllum sérstilltum uppsetningum á birgðavíddareitum á einstökum síðum.

Þar af leiðandi, í dæminu hér á undan, ef þú vilt ekki að dálkurinn fyrir birgðavídd rununúmers birtist á síðu verður þú að hreinsa þá vídd sem hluta af valkostinum **Sýna víddir** fyrir þá síðu.
