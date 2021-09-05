---
title: Sérsníða notandaupplifun
description: Þessi grein útskýrir hvernig hægt er að sérsníða forritið.
author: jasongre
ms.date: 08/09/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysUserSetup, DefaultDashboard
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 62363
ms.assetid: 57b445d7-3e9e-4228-8728-f63b9dbd77a3
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e3d126bf9ec5687d97dacc8763a221da656fdef1
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/13/2021
ms.locfileid: "7344375"
---
# <a name="personalize-the-user-experience"></a>Sérsníða notandaupplifun

[!include [banner](../includes/banner.md)]

Þetta efnisatriði útskýrir hvernig hægt er að sérsníða forritið og fjallar um eftirfarandi viðfangsefni: 

- **Valkostir fyrir allt kerfið** – Þessir sérstillingarmöguleikar eru gerðir á uppsetningarsíðu og eru í boði fyrir alla notendur. Til dæmis stillingar á litaþema og tímabelti. 
- **Takmarkaður aðgangur að sérstillingum** – Á þessu aðgangsstigi eru aðgerðir notanda sem tengjast dæmigerðri síðunotkun vistaðar sjálfkrafa af forritinu og endurheimtar í næsta skipti sem farið er inn á síðuna. Til dæmis vistar forritið breidd dálka í hnitaneti ef þær eru stilltar og hvort flýtiflipar eru útvíkkaðir eða samandregnir. 
- **Fullur aðgangur að sérstillingum** – Á þessu aðgangsstigi eru notendur með aðgang að öllum sérstillingarmöguleikum í forritinu. Helst ber að nefna aðgang þeirra að tækjastikunni **Sérstilling**. 
- **Sérstillingar samnýttar** – Notendur með fullan aðgang að sérstillingum geta flutt út sérstillingar á síðunum sínum og deilt þeim með öðrum notendum.
- **Stjórnun á sérstillingum** – Notendur með réttindi geta farið inn á stjórnunarsíðuna **Sérstillingar** til að hafa umsjón með öllum sérstillingum á fyrirtækisstigi. 

## <a name="system-wide-options-for-the-current-user"></a>Kerfisaltækir valkostir fyrir núverandi notanda

**Notandavalkostir** síðan inniheldur nokkrar kerfisaltækar stillingar fyrir núverandi notanda. Þessir valkostir eru í boði fyrir alla notendur, jafnvel notendur sem hafa ekki fengið veittan neinn aðgang að sérstillingum. Til að opna síðuna **Valkostir notanda** skal velja hnappinn **Stillingar** á yfirlitsstikunni og síðan velja **Valkostir notanda**. **Notandavalkostir** síðan hefur fjóra flipa sem innihalda ýmsar notandastillingar:

- **Sjónrænt** - Veldu litaþema og sjálfgefna stærð eininga á síðum.
- **Kjörstillingar** - Veldu sjálfgefin gildi sem eru notuð í hvert skipti sem þú opnar kerfið. Þessi gildi fela meðal annars í sér sjálfgefið fyrirtæki, upphaflegu síðuna og sjálfgefna yfirlits-/breytingastillingu. (Skoða/breyta hamurinn ákvarðar hvort síða sé læst í skoðun eða opin fyrir breytingar í hvert skipti sem þú opnar hana.) Þessi flipi inniheldur einnig valkosti fyrir tungumálið, tímabeltið og dagsetningu, tíma og númerasnið. Að lokum inniheldur þessi flipi nokkrar fjölbreytilegar kjörstillingar sem eru mismunandi frá útgáfu til útgáfu.
- **Reikningur** – Skoðið eða leiðréttið notandanafnið og aðra valkosti sem tengjast reikningi.
- **Vinnuflæði** - Veldu verkflæðatengda valkosti.

Ásamt því að breyta notandastillingunum, er hægt að skoða og eyða notkunargögnum og sérstillingum á síðunni **Valkostir notanda**. Til að sjá notkunargögnin skal velja **Notkunargögn** á aðgerðasvæðinu. Á flipanum **Sérstillingar** er hægt að skoða og stýra sérsniðnum breytingum sem þú hefur gert á síðum í kerfinu. Á þessum flipa er einnig hægt að núllstilla skýringatexta (það er að segja sprettigluggana sem kynna nýja kerfiseiginleika). Þú verður síðan látin/n vita aftur af eiginleikum sem áður hafa fundist.

> [!NOTE]
> Ef kveikt er á eiginleikanum [Vistuð yfirlit](saved-views.md) er hægt að skoða og stjórna sérstillingum þínum með því að velja **Sérstillingar** í aðgerðarglugganum á síðunni **Notendastillingar**.

## <a name="restricted-personalization-access-formerly-implicit-personalizations"></a>Takmarkaður aðgangur að sérstillingum (áður óbeinar sérstillingar)

Á stigi **takmarkaðs aðgangs að sérstillingum** eru aðgerðir notanda sem tengjast dæmigerðri síðunotkun vistaðar sjálfkrafa af forritinu og endurheimtar í næsta skipti sem farið er inn á síðuna. Ekki er krafist sérstakrar aðgerðar til að vista. 

Hér er listi yfir aðgerðirnar sem falla undir dæmigerða síðunotkun og heyra undir takmarkaðan aðgang að sérstillingum: 

- **Breidd dálka í hnitaneti** - Hægt er að stilla breidd dálks í hnitaneti með því að velja stækkunarstikuna vinstra eða hægra megin við dálkhausinn og síðan renna henni til vinstri eða hægri þar til dálkurinn nær ákjósanlegri breidd. Fottirtið geymir breiddina sem þú stillir fyrir dálk. Næst þegar þessi síða er opnuð verður dálknum breytt í þessa breidd.
- **Síðufótur hnitanets og samtölur dálks** – *(Aðeins í boði þegar kveikt er á nýju hnitanetsstýringunni)* Hægt er að velja hvort sýna eigi samtölu neðst í einhverjum töludálki í hnitanetinu og hvort sýna eigi síðufót hnitanetsins. Forritið vistar þessar kjörstillingar og notar þær næst þegar síðan er opnuð. Nánari upplýsingar eru að finna í [Möguleikar hnitanets](grid-capabilities.md). 
- **Flýtiflipar** - Sumar síður hafa stækkanlega hluta sem eru þekktir sem *Flýtiflipar*. Forritið vistar upplýsingar um flýtiflipana sem hafa verið stækkaðir eða minnkaðir. Í næsta skipti sem síðan er opnuð verða sömu flýtifliparnir annaðhvort útvíkkaðir eða samandregnir, byggt á síðustu samskiptum á síðunni. Í sumum tilfellum geturðu hjálpað til við að auka afköst kerfisins með því að draga saman flýtiflipa, því forritið þarf ekki að sækja upplýsingar um þá flýtiflipa þar til þeir eru stækkaðir. Eins og útskýrt er síðar í þessu efnisatriði, er einnig hægt að breyta röð flýtiflipanna á síðu.
- **Upplýsingakassar** – Sumar síður eru með svæði fyrir **Tengdar upplýsingar** sem sýnir skrifvarðar upplýsingar sem tengjast viðfangsefni síðunnar. Sérhver hluti á svæðinu **Tengdar upplýsingar** er þekktur sem *Upplýsingakassi*. Hægt er að víkka út eða draga saman svæðið **Tengdar upplýsingar** og einnig er hægt að víkka út og draga saman einstaka upplýsingakassa. Forritið geymir þetta kjörval. Í næsta skipti sem síðan er opnuð verður svæðið **Tengdar upplýsingar** og einstakir upplýsingakassar annaðhvort útvíkkaðir eða samandregnir, byggt á síðustu samskiptum á síðunni. Í sumum tilfellum er hægt að hjálpa til við að auka afköst kerfisins með því að fella niður draga saman svæðið **Tengdar upplýsingar** eða upplýsingakassa, því að forritið þarf ekki að sækja upplýsingarnar fyrir upplýsingakassa fyrr en þeir eru stækkaðir.
- **Aðgerðarsvæði** - *Aðgerðarsvæði* birtist ofarlega á flestum síðum. Aðgerðarsvæðið inniheldur hnappa fyrir margar af aðgerðunum sem þú getur framkvæmt á þessari síðu. Þessum hnöppum er oft raðað niður á flipa. Hægt er að *festa* allt aðgerðasvæðið sem opið, eða hafa það sjálfgefið samandregið. Í næsta skipti sem síðan er opnuð verða aðgerðasvæðið annaðhvort opið eða samandregið, byggt á síðustu samskiptum á síðunni. Ef aðgerðasvæðið var fest sem opið, verður síðasti notaði flipinn sýndur.
- **QuickFilters** - A *QuickFilter* birtist fyrir ofan mörg hnitanet. QuickFilters býður upp á að sía hnitanetið út frá einum dálki sem var valinn. Forritið geymir dálkinn sem þú byggðir afmörkunina á. Næst þegar þessi síða er opnuð mun hnitanetið sjálfgefið nota þennan sama dálk til að sía. Hins vegar er enn hægt að velja annan dálk til að sía hnitanetið.
- **Dálkhausaafmarkanir** - Þegar þú afmarkar hnitanet með því að nota *Dálkhausaafmarkanir*, geturðu breytt virknitákni afmörkunar eftir þörfum til að finna gögnin sem þú vilt. Til dæmis getur þú breytt virknitákninu frá **byrjar á** til **er nákvæmlega**. Í hvert skipti sem þú notar dálkhausaafmörkun og breytir virknitákni afmörkunar, geymir forritið breytinguna. Síðan, í næsta skiptið sem þú afmarkar út frá þessum dálki mun virknitákn afmörkunar verða endurheimt.
- **Yfirlitssvæði** - Þú getur opnað *Yfirlitssvæði* með því að velja hnappinn **Stækka yfirlitssvæðið** efst vinstra megin á hvaða síðu sem er. (Þessi hnapp er stundum nefndur _**Valmynd** hnappur_, *hamborgari*, *hamborgaravalmynd* eða *hamborgarahnappur*.) Hægt er að opna yfirlitssvæði og festa það þannig, eða þú getur haldið því samandregnu að sjálfgefnu. Eftir að þú hefur opnað yfirlitssvæði og fest það þannig, mun foritið halda því opnu þar til þú dregur það saman.

## <a name="full-personalization-access-formerly-explicit-personalizations"></a>Fullur aðgangur að sérstillingum (áður þekkt sem beinar sérstillingar)

Á stigi **fulls aðgangs að sérstillingum** eru notendur með aðgang að öllum sérstillingarmöguleikum sem forritið býður upp á. Vegna þess að mismunandi einstaklingar og fyrirtæki eru með ólíkar þarfir þegar þau eiga í samskiptum við forritið, sérstaklega hvað varðar notaða reiti, býður sérstilling upp á verkfæri sem gera notendum og fyrirtækjum kleift að sníða hvernig upplýsingum er raðað og þær notaðar í forritinu. Þessir möguleikar eru lykillinn að því að veita einfaldar, fínstilltar upplifanir í forritinu sem eru sniðnar að þér og fyrirtækinu þínu. 

Ef kveikt er á eiginleikanum [Vistuð yfirlit](saved-views.md), þarf að sérstaka vistun til að halda þessum breytingum á notendaupplifuninni fyrir tiltekið yfirlit. Þegar slökkt er á eiginleikanum **Vistuð yfirlit** eru þessar breytingar sjálfkrafa vistaðar.

Eftirfarandi hlutar fjalla um umfang sérstillingarmöguleika sem í boði er fyrir notendur á stigi **fulls aðgangs að sérstillingum**. Hér eru nokkrir þessara möguleika:

- Flýtivalmynd valkostir
- Tækjastikan **Sérstillingar**
- Bæta reitum, listum og tenglum við vinnusvæði
- Bæti við samantekt frá vinnusvæði til yfirlits
- Sérstilling stjórnborðs

### <a name="shortcut-menu-options"></a>Flýtivalmynd valkostir

Flýtivalmyndir bjóða upp á eina leið til að breyta viðmóti síðu þannig að hún standist betur kröfur notanda eða fyrirtækis. (Flýtivalmynd er einnig þekkt sem *valmynd við hægrismell* eða *efnisvalmynd*.)

Sumir af mest dæmigerðu og mikilvægustu breytingum sem hægt er að gera á síðu er hægt að gera beint með því að nota valkostir í flýtivalmynd. Til dæmis, ef ætlunin er að setja inn eða fela dálka í hnitaneti, skal einfaldlega hægrismella á dálkhaus og velja síðan **Setja inn dálka** eða **Fela þennan dálk**.

Að auki eru helstu tegundir sérstillinga tiltækar með því að hægrismella á einingu og síðan velja **Sérsníða**. (Athugið að ekki er hægt að sérsníða allar einingar á síðunni.) Þegar þessi sérstillingaraðferð er notuð birtist *eiginleikagluggi* einingarinnar.

![Sérsníða eiginleika í einingu.](./media/cli-element-property-window.png)

Þú getur notað eiginleikagluggann til að sérsníða einingu á eftirfarandi hátt:

- Breyta merkimiða einingarinnar.
- Fela eininguna þannig að hún verði ekki sjáanleg á síðunni. Gögnin í reitnum hefur ekki verið eytt eða breytt. Upplýsingarnar eru einfaldlega ekki sýndar á síðunni lengur.
- Hafa upplýsingarnar í samantektarhlutanum fyrir flýtiflipa (ef einingin er á flýtiflipa).
- Slepptu reitnum svo að hann fái aldrei fókus þegar þú flettir í gegnum síðuna.
- Koma í veg fyrir breytingar á gögnum í reitnum (fyrir allar skrár).
- Tilnefnið reit sem krafist er fyrir færslu gagna. Ef ekkert gildi hefur verið slegið inn í þennan reit mun það birtast með rauða ramma og stjörnu til að gefa til kynna þessa stöðu. Þessi valkostur er aðeins í boði frá og með útgáfu 10.0.11 þegar kveikt er á eiginleikunum [Vistuð yfirlit](saved-views.md) og **Tilgreina reiti sem nauðsynlega með því að nota sérstillingu**.

Eiginleikaglugginn gæti falið í sér aðrar sérstillingareiginleika, en það fer eftir einingunni. Til dæmis gæti eiginleikagluggi fyrir reit gert kleift að færa þann reit yfir á stjórnborð, og eiginleikagluggar fyrir einingar á sjálfgefnu stjórnborði gætu gert kleift að stofna nýtt sérstillt vinnusvæði.

### <a name="personalization-toolbar"></a>Verkfæraslá sérstillingar

Ef ætlunin er að gera margar breytingar á síðu eða gera breytingar sem ekki eru í boði með öðrum leiðum (t.d. ef ætlunin er endurraða einingum), er hægt að nota tækjastikuna **Sérstilling**. Til að opna verkfæraslána **Sérstillingar** skaltu fylgja einu af þessum skrefum:

- Veljið **CTRL+SHIFT+P** úr hvaða einingu sem er á síðunni.
- Veldu **Aðlaga þessa síðu** í eiginleikaglugga einingarinnar.
- Veldu **Sérsníða þessa síðu** í flokknum **Sérsníða** á flipanum **Valkostir** í aðgerðaglugga einhverrar síðu.
- Veldu hnappinn **Stillingar** (gírtáknið) á leitarstikunni og veldu síðan **Sérsníða**.

[![Verkfæraslá sérstillingar.](./media/restyledPersonalizationToolbar.png)](./media/restyledPersonalizationToolbar.png)

#### <a name="navigating-the-page"></a>Farið um síðuna

Þegar verkfærasláin **Sérstilling** er opin er undirliggjandi síða skrifvarin (með öðrum orðum, þú getur ekki breytt gögnum), en hún er samt gagnvirk. Sér í lagi er hægt að víkka út eða draga saman svæðið **Tengdar upplýsingar**, skipta út flipum og víkka út eða draga saman hluta, eins og venjulega þegar þessar aðgerðir eru framkvæmdar á síðunni. Til að koma á sérstillingu á samandregnum hluta eða flipa (til dæmis til að fela flýtiflipa) þarftu aðeins að velja hnappinn sem birtist við hliðina á þeim hluta eða flipa þegar hann fær áherslukassa lyklaborðs eða þegar þú heldur bendlinum yfir honum.

#### <a name="personalization-tools"></a>Sérstillingartæki

Eftirfarandi verkfæri eru í boði á **Sérstillingar** tækjastikunni:

- Nota **Velja** verkfæri til að velja og breyta eiginleikum einingar. Til að nota þetta tól velurðu hnappinn **Velja** á verkfæraslánni og síðan viðkomandi einingu. Eiginleikagluggi einingarinnar birtist, þar sem hægt er að breyta hvaða eiginleika sem er fyrir þá einingu. Þú getur endurtekið ferlið fyrir aðrar einingar sem hægt er að sérsníða á síðunni. Athugaðu að sumir eiginleikar sérstillinga eru mögulega ekki tiltækir í sumum aðstæðum. Til dæmis getur þú ekki læst reit sem er nauðsynlegur.
- Nota **Fela** verkfærið til að fela einingu á síðunni. Til að nota þetta tól velurðu hnappinn **Fela** á verkfæraslánni og síðan einingu sem á að fela. Þegar verkfærið **Fela** er notað, verða allar faldar einingar gerðar sýnilegar, en þær verða sýndar í skyggðu hólfi. Þú getur síðan gert þátt sýnilegan með því að velja hann. Til að sjá hvernig síðan lítur út þegar einingar eru faldar skal skipta yfir í annað sérstillingarverkfæri eða loka tækjastiku sérstillinga.
- Notið verkfærið **Bæta við reitum** til að bæta reitum við síðuna. Þegar þú notar þetta verkfæri geturðu aðeins bætt við reitum sem eru hluti af skilgreiningunni á síðunni. Til að fá upplýsingar um hvernig skal búa til nýja reiti sem eru ekki hluti af núverandi skilgreiningu síðunnar, sjá [Stofna og vinna með sérsniðna reiti](user-defined-fields.md). Þegar hnappurinn **Bæta við reitum** er valinn á tækjastikunni, þarf fyrst að velja hnitanetið eða hlutann þar sem ætlunin er að bæta reitnum við. Svargluggi sýnir lista yfir reiti sem tengjast völdu hnitaneti eða hluta. Í svarglugganum skal velja eitt eða fleiri reiti til að bæta við og velja síðan **Uppfæra**. Til að fjarlægja reit sem þú hefur áður bætt við, skal endurtaka ferlið, en hreinsa val á reitnum í svarglugganum.
- Nota **Færa** verkfærið til að færa einingar á annan stað í núverandi hóp eininga. Athugaðu að ekki er hægt að færa einingu utan yfirhóps hennar. Til að nota þetta tól velurðu hnappinn **Flytja** á verkfæraslánni og síðan einingu sem á að flytja. Þegar þú velur einingu ákvarðar forritið staðsetningar þar sem flytja má eininguna. Þessir staðir eru þekktir sem *sleppisvæði*. Þegar þú færir eininguna til í núverandi hóp er hvert sleppisvæði sýnt sem lituð, feitletruð lína við hliðina á því svæði þar sem má sleppa einingunni.
- Nota **Sleppa** verkfærið til að fjarlægja einingu úr fliparöð lyklaborðs síðunnar. Þegar þú velur hnappinn **Sleppa** á verkfæraslánni eru allar einingar sem nú þegar er sleppt sýndar í skyggðum gámi. Þú getur fjarlægt eða bætt við reitum á fliparöðinni með gagnvirkum hætti.
- Notaðu verkfærið **Sýna í haus** þegar þú vilt að reitur birtist í samantektarhlutanum fyrir flýtiflipa. Þegar þú velur hnappinn **Sýna í haus** á verkfæraslánni eru allir reitir sem hafa verið valdir sem samantektarreitir sýndar í skyggðum gámi. Með því að velja reitina getur þú með gagnvirkum hætti fjarlægt og bætt við reitum í samantekt flýtiflipa.
- Notaðu verkfærið **Krefjast** til að tilnefna þátt eins og krafist er fyrir færslu gagna. Þegar hnappurinn **Krafist** er valinn í tækjastikunni birtast allar einingar sem hafa verið sérsniðnar til að gera þær nauðsynlegar í skyggðu hólfi. Þú getur þá aftur gert þær sem ekki krafist. Þessi valkostur er tiltækur í útgáfu 10.0.12 og síðar þegar eiginleikinn **Gera reiti nauðsynlega með sérstillingu** er virkjaður.
- Notaðu verkfærið **Læsa** til að merkja einingu sem annaðhvort breytanlega eða óbreytanlega. Þegar þú velur hnappinn **Læsa** á verkfæraslánni eru allar einingar sem eru þegar óbreytanlegar sýndar í skyggðum gámi. Þú getur þá gert þær breytanlegar aftur. Athugaðu að sumir reitir eru nauðsynlegir og ekki hægt að gera þá óbreytanlega. Hengilásatákn birtist við hliðina á þessum reitum.
- Notið verkfærið **Bæta við forriti úr Power Apps** til að fella inn í síðuna forrit sem var búið til með því að nota Microsoft Power Apps. Nánari upplýsingar um hvernig á að fella inn forrit frá Power Apps á síðu er að finna í [Innfelling á forritum úr Power Apps](embed-power-apps.md). Þessi valkostur er aðeins í boði þegar slökkt er á eiginleikanum [Vistuð yfirlit](saved-views.md).
- Notaðu hnappinn **Bæta við forriti** til að fella inn forrit, annaðhvort forrit stofnað í Microsoft Power Apps eða frá þriðja aðila, á síðuna. Þessi valkostur er aðeins í boði þegar kveikt er á eiginleikanum [Vistuð yfirlit](saved-views.md). 
- Notaðu verkfærið **Hreinsa** til að endurstilla síðuna í sjálfgefið, uppsett ástand. Allar sérstillingar á núverandi síðu verða hreinsaðar. Ekki er hægt að afturkalla þessa aðgerð. Þess vegna skaltu aðeins nota þetta verkfæri ef þú ert viss um að þú viljir endurstilla síðuna. Þegar kveikt er á eiginleikanum **Vistuð yfirlit**, hreinsar þetta verkfæri sérstillingarnar fyrir núverandi yfirlit.
- Notaðu verkfærið **Flytja inn** til að hlaða inn sérstillingu úr skrá sem þú eða einhver annar bjó til áður. 

    - Þegar slökkt er á eiginleikanum **Vistuð yfirlit**, er hægt að velja hvort bæta eiga við eða skipta út fyrirliggjandi sérstillingum fyrir sérstillingarnar sem verið er að flytja inn fyrir síðuna. Ekki er hægt að afturkalla þessa aðgerð. Þess vegna, eftir að þú hefur flutt inn sérstillingar, verðurðu að hreinsa handvirkt eða afturkalla allar breytingar sem þú vilt ekki.
    - Þegar kveikt er á eiginleikanum **Vistuð yfirlit** verða innfluttar sérstillingar að yfirliti á síðunni. Ef yfirlitið er þegar til staðar, verður boðið upp á að sleppa innflutningi, skipta út núverandi yfirliti sem er með sama heiti eða endurnefna innflutt yfirlit.

- Notaðu verkfærið **Flytja út** til að vista sérstillingar þínar fyrir síðuna í skrá. Síðan geturðu deilt sérstillingunum þínum með öðrum notendum. Þessir notendur þurfa bara að flytja inn skrána sem inniheldur sérstillingarnar þínar fyrir síðuna. Þegar kveikt er á eiginleikanum **Vistuð yfirlit**, vistar þetta verkfæri núverandi yfirlit í skrá til að deila.
- Velja **Loka** hnappinn til að loka tækjastikunni fyrir **Sérstillingar** og færa síðuna í fyrri gagnvirka stöðu hennar.

Hefð er fyrir því þegar verkfærasláin **Sérstillingar** er notuð, að sérstillingarnar taka gildi um leið og þú gerir þær. Hins vegar, ef kveikt er á eiginleikanum [Vistaðar skoðanir](saved-views.md), verður þú að vista sérstillingar beint í það yfirliti sem þú velur.

Í sumum tilfellum, þegar þú velur verkfæri, birtist hengilásatákn við hliðina á einingu. Þetta tákn gefur til kynna að þú getir ekki breytt einingareiginleikum sem tengjast völdu verkfæri, vegna þess að breytingar á þessum eiginleikum koma í veg fyrir að síðunni virkar rétt.

### <a name="adding-tiles-lists-and-links-to-a-workspace"></a>Bæta reitum, listum og tenglum við vinnusvæði

Fyrir sumar síður sem innihalda lista er sérstillingaraðgerðin **Bæta við vinnusvæði** fáanleg í hópnum **Sérsníða** á flipanum **Valkostir** á Aðgerðarrúðunni. Þessi aðgerð gerir þér kleift að ýta viðeigandi upplýsingum úr núverandi lista yfir á tiltekið vinnusvæði. Upplýsingarnar sem birtast í vinnusvæðinu geta verið byggðar á annaðhvort öllum listanum eða afmarkaðri og flokkaðri útgáfu af listanum. Þú getur einnig tilgreint hvort upplýsingarnar birtist í vinnusvæði sem listi, sem samantektarreit sem sýnir fjölda atriða á listanum eða sem tengill.

> [!NOTE]
> Ef kveikt er á eiginleikanum [Vistaðar skoðanir](saved-views.md) er efnið sem þú ýtir á vinnusvæði beintengt við yfirlit. Fyrirspurn yfirlitsins er notuð til að sækja gögn í vinnusvæðinu og samsvarandi reitur eða tengill í vinnusvæðinu opnar síðuna í það yfirlit, þannig að fyrirspurn yfirlitsins og sérstillingarnar eru notaðar þar. Ef yfirlitið er uppfært verða samsvarandi einingar vinnusvæðis leiðréttar í nýju skilgreininguna á yfirliti.

[![Bæta við vinnusvæði.](./media/personalization-addtoworkspace.png)](./media/personalization-addtoworkspace.png)

- Til að bæta lista við vinnusvæði skal fyrst flokka eða afmarka listann á síðunni þannig að hún birti upplýsingarnar eins og þú vilt að þær birtist á vinnusvæðinu. (Ef kveikt er á eiginleikanum **Vistuð yfirlit** er ekki hægt að halda áfram fyrr en yfirlit er vistað sem er með þessum skilyrðum.) Síðan skal velja **Bæta við vinnusvæði**. Velja vinnusvæði, og svo, í **Framsetning** reitnum skal velja **Listi**. Eftir að þú velur **Grunnstilla** birtist gluggi þar sem þú getur valið dálkana sem eiga að birtast á listanum í vinnusvæðinu. Þú getur einnig tilgreint merkið sem er notað fyrir listann á vinnusvæðinu.
- Til að bæta við flís á vinnusvæði skaltu fyrst afmarka listann á síðunni þannig að hann birti gögnin sem þú vilt að séu samantekin eða vilt fá skjótan aðgang að. (Ef kveikt er á eiginleikanum **Vistuð yfirlit** er ekki hægt að halda áfram fyrr en yfirlit er vistað sem er með þessum skilyrðum.) Síðan skal velja **Bæta við vinnusvæði**. Velja vinnusvæði og svo í reitnum **Framsetning** skal velja **Flís**. Eftir að þú hefur valið **Grunnstilla** birtist svargluggi þar sem þú getur tilgreint merkið sem á að nota fyrir reit á vinnusvæðinu. Þú getur einnig tilgreint hvort flísin ættu að sýna fjölda. Eftir að reitum er bætt við vinnusvæðið geturðu valið það til að opna núverandi síðu úr vinnusvæðinu. Þú getur síðan skoðað afmarkaðan lista sem er tengdur reitnum.
- Til að bæta við tengli á vinnusvæði skaltu fyrst afmarka listann á síðunni þannig að hún birti gögnin sem þú hefur áhuga á. (Ef kveikt er á eiginleikanum **Vistuð yfirlit** er ekki hægt að halda áfram fyrr en yfirlit er vistað sem er með þessum skilyrðum.) Síðan skal velja **Bæta við vinnusvæði**. Veldu vinnusvæði, og síðan, í **Framsetning** reitnum, skal velja **Tengill**. Eftir að þú hefur valið **Grunnstilla** birtist svargluggi þar sem þú getur tilgreint merkið sem á að nota fyrir tengilinn. Þú getur einnig valið tiltekið merki fyrir nýjan hluta sem inniheldur þennan tengil.

Þegar þú hefur bætt lista, reit eða tengli við vinnusvæði getur þú opnað vinnusvæðið og endurraðað einingunum í því eins og þú vilt.

### <a name="adding-a-summary-from-a-workspace-to-a-dashboard"></a>Bæti við samantekt frá vinnusvæði til yfirlits

Sum vinnusvæði innihalda talningarflísar (það er, flísar með tölum), og þú vilt kannski að þessi flísar birtast á yfirlitinu þínu líka. Á vinnusvæði skal hægrismella á talningarreitinn og velja **Sérsníða**, og velja síðan **Festa við stjórnborð** í eiginleikaglugga reitsins. Í næsta skipti sem þú opnar (og uppfærir) yfirlit, birtist fjöldinn fyrir neðan yfirlitsflísina fyrir það vinnusvæði. Þú getur valið þá talningu til að fara beint á þau gögn sem hún stendur fyrir.

### <a name="personalizing-your-dashboard"></a>Sérsníða yfirlitið þitt

Yfirlitið er iðulega fyrsta síða sem þú sérð þegar þú opnar forritið. Hægt er að sérsníða það eins og aðra síðu í kerfinu með því að nota sömu leiðirnar og lýst var fyrr í þessu efnisatriði. 

> [!WARNING]
> Sem stendur, þegar efni er falið í yfirlitinu, er mikilvægt að velja þann reit, en ekki svæðið í kring. Ef hópurinn í kringum reit er falinn, gætu óvæntar niðurstöður komið ef fleiri reitum er bætta við seinna meir, eða ef skipt er yfir í annað tungumál í kerfinu.

Einn ákveðinn sérstillingarmöguleiki sem er í boði í yfirlitinu er möguleikinn á því að bæta við reitum. 

- Ef slökkt er á eiginleikanum **Heilsíðuforrit** er bætt við nýjum reit með því að hægrismella á einingu í yfirlitinu og síðan velja **Bæta við vinnusvæði**. Ný vinnusvæðisflís er búin til neðst á yfirlitinu. Þú getur endurnefnt þennan nýja vinnusvæðisflís eins og þú vilt. Einnig er hægt að bæta listum, reitum og tenglum við vinnusvæðið, eins og lýst er í hlutanum [Bæta reitum, listum og tenglum við vinnusvæði](personalize-user-experience.md#adding-tiles-lists-and-links-to-a-workspace) í þessu efnisatriði.
- Ef kveikt er á eiginleikanum **Heilsíðuforrit**, er bætt við nýjum reit með því að hægrismella á einingu í yfirlitinu og síðan velja **Bæta við forriti**. Í svarglugganum skal velja hvort bæta eigi reiti við nýtt vinnusvæði eða reiti sem er með efni frá Power Apps eða vefsvæði. Fylgið því næst skrefunum til að skilgreina valkostina sem voru valdir. Nýr reitur er búinn til neðst í yfirlitinu. Frekari upplýsingar um hvernig á að bæta við, breyta, eyða og deila þessum innfelldu forritum er að finna í [Innfelld vinnuforrit frá Power Apps](embed-power-apps.md) og [Innfella forrit þriðja aðila](embed-website.md).

## <a name="sharing-personalizations"></a>Sérstillingar samnýttar

Eftir að þú sérstillir síðu er hægt að nota nokkrar aðferðir til að deila sérstillingum þínum með öðrum notendum. Í eftirfarandi lista er aðferðunum raðaðar í þeirri röð frá þeirri sem helst er mælt með til þeirrar sem minnst er mælt með.

1. Birta yfirlit fyrir notendum.
2. Afrita yfirlit eða sérstillingar á notendur.
3. Flytja yfirlit eða sérstillingar inn eða út.

### <a name="publish-views-to-users"></a>Birta yfirlit fyrir notendum

Ef kveikt er á eiginleikanum [Vistuð yfirlit](saved-views.md), og ef síðan styður yfirlit, er besta leiðin til að deila sérstillingum með öðrum notendum að birta yfirlit fyrir notendur sem hafa eitt eða fleiri öryggishlutverk. - Frekari upplýsingar er að finna í [Birta yfirlit](saved-views.md#publishing-views).

### <a name="copy-views-or-personalizations-to-users"></a>Afrita yfirlit eða sérstillingar á notendur

Ef slökkt er á eiginleikanum [Vistuð yfirlit](saved-views.md) eða ef síðan styður ekki yfirlit, er mælt með að deila sérstillingum með því að afrita þær á milli notenda. Þessi aðferð er einungis tiltæk fyrir notendur með tiltekin réttindi (til dæmis kerfisstjóra). Stjórnendur geta hins vegar flett upp tiltekinni sérstillingu notanda í kerfinu (þ.m.t. eigin yfirliti notandans ef er vistuð yfirlit eru virk) og afritað skilgreininguna hjá öðrum notendum.

Ef vistuð yfirlit eru virk skal fylgja eftirfarandi skrefum til að afrita sérstillingar.

1. Farið í **Kerfisstjórnun \> Uppsetning \> Sérstilling**.
2. Fylgið eftirfarandi skrefum til að afrita eigin yfirlit:

    1. Veljið **Yfirlitin mín**.
    2. Á listanumskal velja viðeigandi yfilit.
    3. Veljið **Afrita í notendur**.
    4. Velja notendurna til að dreifa yfirlitum á.

    Fylgið eftirfarandi skrefum til að afrita sérstillingar á síðum sem styðja ekki yfirlit:

    1. Veldu **Notandastillingar**.
    2. Veljið notandann sem er með sérstillinguna sem á að dreifa.
    3. Veljið **Stjórna öllum sérstillingum**.
    4. Á listanumskal velja viðeigandi sérstillingar.
    5. Veljið **Afrita í notendur**.
    6. Velja notendurna til að dreifa sérstillingum til.

Ef vistuð yfirlit eru ekki virk skal fylgja eftirfarandi skrefum til að afrita sérstillingar.

1. Farið í **Kerfisstjórnun \> Uppsetning \> Sérstilling**.
2. Veljið **Bæta við**.
3. Velja notendurna til að dreifa sérstillingunni til.
4. Veljið **Velja núverandi sérstillingar**.
5. Finndu og veldu þá (staka) sérstillingu sem þú hefur áhuga á.
6. Veljið **Í lagi**.

### <a name="export-and-import-views-or-personalizations"></a>Flytja yfirlit eða sérstillingar inn eða út

Önnur leið til að deila sérstillingum er með útflutningi og innflutningi. Einstakir notendur, eða stjórnandi sem starfar fyrir þeirra hönd, geta notað þessa aðferð til að flytja út sérstillingar sínar eða yfirlit og síðan gefið öðrum notendum útflutningsskrána til að flytja inn. Einnig geta notendur gefið útfluttar sérstillingar sínar til notanda sem hefur stjórnunarréttindi og sá notandi getur síðan notað stjórnunarsíðu **Sérstillingar** til að beita sérstillingarskránni á marga notendur á sama tíma.

#### <a name="export"></a>Flytja út

Almennt er hægt að flytja út eitt eigið yfirlit eða sérstillingar með því að opna viðeigandi síðu, opna tækjastikuna **Sérstillingar** og velja síðan **Flytja út**. Nánari upplýsingar um tækjastikun er að finna í hlutanum [Tækjastika sérstillinga](#personalization-toolbar) fyrr í þessu efnisatriði. Ef [vistuð yfirlit](saved-views.md) eru virk er einnig hægt að fara í **Stillingar \> Valkostir fyrir notendur \> Sérstillingar** til að skoða lista yfir allar sérstillingar í kerfinu. Þaðan er hægt að velja yfirlit eða sérstillingar sem á að flytja út og síðan velja **Flytja út**.

Auk þess geta stjórnendur flutt út sérstillingar annarra notenda á eftirfarandi hátt.

1. Opnið **Kerfisstjórnun \> Uppsetning \> Sérstillingar**.
2. Á flipanum **Notendur** skal velja viðeigandi notanda.
3. Finnið og veljið það útlit eða þá sérstillingu sem óskað er eftir.
4. Velja **Flytja út**.

#### <a name="import"></a>Flytja inn

Til að flytja inn yfirlit eða sérstillingu er einfaldlega hægt að opna tækjastikuna **Sérstillingar** og velja **Flytja inn**. Auk þess geta stjórnendur flutt inn skrá og gefið hana strax til eins eða fleiri notenda.

Ef vistuð yfirlit eru virk skal fylgja eftirfarandi skrefum.

1. Opnið **Kerfisstjórnun \> Uppsetning \> Sérstillingar**.
2. Á Aðgerðasvæðinu skal velja **Flytja inn yfirlit \> Yfirlit notanda**.
3. Veljið innflutningsstillingu:

    - **Velja tiltekna notendur** – Gefðu völdum notendum yfirlit eða sérstillingu.
    - **Flytja inn eins og það** er – Flytja inn yfirlitið eða sérstillinguna á sama notanda og flutti hana út.

4. Veljið **Fletta** og finnið og veljið sérstillinguna sem á að flytja inn.
5. Veljið **Næst**.
6. Ef valið er **Veljið tiltekna notendur** í þrepi 3 skal velja þá notendur sem sérstillingin á að flytja inn á.
7. Velja **Innflutningur**.
8. Leysa árekstra eftir þörfum.

Ef vistuð yfirlit eru ekki virk skal fylgja eftirfarandi skrefum.

1. Opnið **Kerfisstjórnun \> Uppsetning \> Sérstillingar**.
2. Veljið **Bæta við**.
3. Velja notendurna til að dreifa sérstillingunni til.
4. Veljið **Flytja inn sérstillingar úr skrá**.
5. Veljið **Fletta** og finnið og veljið sérstillinguna sem á að flytja inn.
6. Veljið **Í lagi**.

## <a name="administration-of-personalizations"></a>Stjórnun sérstillinga

Síðan **Sérstillingar** er miðstöð stjórnunar sérstillinga á fyrirtækisstigi. Innihald og möguleikar á þessari síðu fara eftir því hvort eiginleikinn **Vistuð yfirlit** hafi verið virkjaður.

Fyrir viðskiptavini sem hafa kveikt á eiginleikanum **Vistuð yfirlit** skal skoða „Stjórna yfirlitum á altækan hátt“ í efnisatriðinu [Vistuð yfirlit](saved-views.md).

Fyrir viðskiptavini sem hafa ekki enn kveikt á eiginleikanum [Vistuð yfirlit](saved-views.md) hefur þessi síða fjóra flipa:

- **Virkja** - Hægt er að flytja inn eða velja sérstillingu fyrir einn eða fleiri notendur. Til að virkja sérstillingu í þágu eins eða fleiri notenda, skal velja fyrst hlutverk og notendur sem hafa það hlutverk. Síðan skal velja annaðhvort fyrirliggjandi sérstillingu til að virkja í þágu valdra notenda, eða flytja inn sérstillingarskrá. Sérstillingin er sannprófuð og verður virkjuð í þágu allra valdra notenda næst þegar þeir opna völdu síðuna.

- **Hreinsa** - Þú getur hreinsað allar sérstillingar fyrir síðu eða vinnusvæði fyrir einn eða fleiri notendur. Veldu fyrst síðu eða vinnusvæði til að sjá lista yfir notendur sem hafa notað sérstillingu á það. Veldu síðan þá notendur sem hreinsa skal sérstillingar síðu eða vinnusvæðis hjá og veldu **Hreinsa**. Allar sérstillingar sem völdu notendur hafa virkjað á valdri síðu eða vinnusvæði er eytt. Ekki er hægt að afturkalla þessa aðgerð. Ef sérstilling var hins vegar var vistuð fyrir síðuna eða vinnusvæðið, er hægt að flytja þá sérstillingu inn aftur.

- **Notendur** - Veldu notanda til að sjá lista yfir síður sem notandinn hefur sérstillt. Síðan geturðu kveikt eða slökkt á getu valins notanda til að nota sérstillingar fyrir tilteknar síður eða fyrir allt kerfið. Þú getur einnig flutt inn, flutt út eða hreinsað sérstillingar notanda. Að auki geturðu endurstillt skýringartexta eiginleika fyrir notandann. Í þessu tilfelli, ef notandi hefur áður sagt upp öllum sprettigluggum sem kynna nýja eiginleika, munu þeir birtast aftur næst þegar notandinn lendir í þessum aðgerðum.

- **Kerfi** - Einnig er hægt að slökkva á sérstillingum allra notendur kerfisins tímabundið. Í þessu tilfelli er öllum sérstillingum eytt fyrir alla notendur og allar síður eru endurstilltar í sjálfgefna stöðu. Ef þú kveikir aftur á sérstillingum verður öllum sérstillingumaftur beitt. Einnig er hægt að eyða öllum sérstillingum endanlega fyrir alla notendur kerfisins. Ekki er hægt að endurheimta sérstillingar sem hefur verið eytt. Áður en þú framkvæmir þetta verkefni skaltu þess vegna vera viss um að flytja út allar sérstillingar sem þú gætir viljað síðar.

## <a name="personalizing-inventory-dimensions"></a>Sérstilling birgðavídda

Þegar þú sérstillir uppsetningu birgðavídda á síðu, skaltu hafa í huga stillingarnar sem hafa verið búnar til með notkun valkostarins **Sýna víddir**. Til dæmis notar þú sérstillingu til að fela dálk sem inniheldur birgðavídd rununúmers, en dálkurinn birtist næst þegar síðunni er opnuð. Þessi hegðun á sér stað vegna þess að **Birting vídda** stillingarnar stjórna birgðavíddadálkunum sem eru sýndir. **Birting vídda** stillingarnar eiga við um allar síður og hnekkja öllum sérstilltum uppsetningum á birgðavíddareitum á einstökum síðum.

Þar af leiðandi, í dæminu hér á undan, ef þú vilt ekki að dálkurinn fyrir birgðavídd rununúmers birtist á síðu verður þú að hreinsa þá vídd sem hluta af valkostinum **Sýna víddir** fyrir þá síðu.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
