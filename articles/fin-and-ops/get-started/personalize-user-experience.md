---
title: "Sérsniðin notkun"
description: "Þessi grein útskýrir hvernig hægt er að sérsníða Microsoft Dynamics 365 for Finance and Operations."
author: RobinARH
manager: AnnBe
ms.date: 08/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysUserSetup
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
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: cf2ad9f95035aaf004f2da779a8492ff2d91d399
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="personalize-the-user-experience"></a>Sérsniðin notkun

[!include[banner](../includes/banner.md)]


Þessi grein útskýrir hvernig hægt er að sérsníða Microsoft Dynamics 365 for Finance and Operations.

+Það eru margar gerðir sérstillinga í Microsoft Dynamics 365 for Finance and Operations. Sumar sérstillingar eru valdar í lista yfir valkosti á uppsetningarsíðunni. Sumar sérstillingar eru óbeinar, til dæmis heldur Finance and Operations utan um breidd dálka í hnitanetinu ef það þarf að leiðrétta þá og útvíkkaða/samandregna stöðu flýtiflipa. Aðrar sérstillingar eru beinar. Fyrir beinar sérstillingar er færður inn gagnvirkur sérsniðsmáti og útliti síðu breytt með því að stjórna því hvernig einingar birtast eða bregðast við á síðunni. 

Allar sérstillingar, af hvaða tagi sem er, sem notandi gerir í Finance and Operations eru aðeins fyrir þann notanda, burtséð frá fyrirtækinu sem notandinn vinnur með. Breytingar sem notandi gerir á síðu hafa ekki áhrif á aðra notendur kerfisins.

## <a name="systemwide-options-for-the-current-user"></a>Kerfisaltækir valkostir fyrir núverandi notanda
Í yfirlitsstiku finnurðu mynd af tannhjóli, sem kallast valmyndarhnappurinn **Stillingar**. Opnun valmyndarinnar **Stillingar** mun sýna fjölda valkosta. Val á **Valkostir** opnar síðuna **Valkostir** notanda. Þar finnurðu fjóra valkostaflipa: 

-   **Visual:** Notað til að velja litaþema og sjálfgefin stærð einingar á síðum fyrirtækisins.
-   **Kjörstillingar:** Hér er hægt að velja sjálfgildi fyrir hvert sinn sem Finance and Operations er opnað, þ.m.t. fyrirtækið, upphafssíðu og sjálfgefið yfirlit/breytingahamur (sem ákveður hvort síðu er læst fyrir skoðun eða opinn til breytinga í hvert sinn sem hún er opnuð). Einnig er verður hægt að finna tungumál, tímabelti og dagsetningu, tíma- og númer snið valkosti. Að endingu inniheldur þessi síða fjölda ýmissa kjörstillinga sem eru breytilegar frá losun til að losa.
-   **Lykill:** Notað til að veita Notandakenni og aðra lykiltengda valkosti.
-   **Verkflæði:** Hér er hægt er að velja erkflæðistengda valkosti.

## <a name="implicit-personalizations"></a>Óbeinar sérstillingar
Óbeinar sérstillingar eru þær sérstillingar sem eru framkvæmdar einfaldlega með notkun ákveðinna stýringa sem muna núverandi stöðu sína. 

**Dálkar í hnitanetinu:** Hægt er að stilla breidd dálks í lista með því að velja stærðarstikuna til vinstri eða hægri við dálkhausinn og renna henni til vinstri eða hægri um æskilega breidd. Finance and Operations geymir breiddina sem á að stilla og sýna dálkinn með þeirri breidd í hvert skipti sem síðan er opnuð sem listi. 

**Flýtiflipar:** Sumar síður hafa stækkanlega hluta sem kallast flýtiflipar. Finance and Operations geymir hvaða flýtiflipar hafa verið útvíkkaðir og hvaða flýtiflipar hafa verið dregnir saman. Í hvert sinn sem síðu er skilað eru þessir sömu flýtiflipar útvíkkaðir eða dregnir saman byggð á þeim var notað síðast. Í þessari grein verður útskýrt hvernig á að breyta röðun á flýtiflipunum. Í sumum tilvikum getur minnkun flýtiflipa bætt afköst því Finance and Operations þarf ekki að sækja upplýsingar um þá flýtiflipa fyrr en flýtiflipinn er útvíkkaður. 

**Staðreyndareitir:** Sumar síður hafa hluta sem kallast Staðreyndarúða. Þessi rúða inniheldur aðeins til lestrar upplýsingar sem tengjast gildandi efni á síðunni. Hver kafli í staðreyndarúðunni er kallaður staðreyndareitur. Hægt er að útvíkka eða draga saman staðreyndareiti og Finance and Operations mun geyma forstillingar þínar. Í sumum tilvikum getur minnkun staðreyndareita bætt afköst því Finance and Operations þarf ekki að sækja upplýsingar um þá staðreyndareiti fyrr en staðreyndareiturinn er útvíkkaður.

## <a name="explicit-personalizations-using-the-personalization-toolbar"></a>Yfirlýstar sérstillingar með sérsniðinni verkfærastiku
Hver einstaklingur og fyrirtæki hefur mismunandi sjónarhorn um hvaða gögn eru þeim mikilvægust eða hvaða gögn er ekki þörf fyrir hátt rekstrinum þær keyrðar. Möguleikinn á að sníða hvernig upplýsingum er raðað, unnið með þær eða þær jafnvel faldar er lykillinn að því að gera Finance and Operations persónulegt og skilvirkt. 

Beinar sérstillingar eru þær sérstillingar sem eru framkvæmdar beint og er ætlað að breyta útliti eða hegðun á einingu eða síðunni með því að velja sérsnið valmynd. Grunngerð beinna sérstillinga er þar sem hægrismellt er á einingu og valið **Sérsníða**. (Athugið að ekki er hægt að sérsníða allar einingar á síðunni.) Þegar þessi sérstillingaraðferð er valin sérðu eiginleikaglugga einingarinnar. 

[![Sérsníða eiginleika í einingu](./media/personalization-element-properties.jpg)](./media/personalization-element-properties.jpg) 

Eining á síðu er breytt á þennan hátt ef einfaldlega á að breyta merki einingarinnar, fela eininguna svo að hún birtist ekki á síðunni (þetta breytir ekki neinum gögnum, heldur sýnir einfaldlega ekki sum gögn), hafa með upplýsingar í samantektarhluta flýtiflipa (ef eining er í flýtiflipa), sleppa reitnum við flipastjórnun eða stilla hann þannig að ekki sé hægt að breyta sumum gögnum með því að merkja hann sem „Ekki breyta.“ 

Þegar óskað er að flytja eða fela einingar eða gera nokkrar breytingar, er hægt að nota sérstillingatækjastikuna sem er tiltæk úr glugganum einingar Eiginleika með því að velja **Aðlaga þessa skjámynd**. Sérstillingatækjastikan er einnig tiltæk í aðgerðarúðu skjámyndarinnar, undir Sérstillingar flokks á flipanum **Valkosti**. Veldu **Aðlaga þessa skjámynd** og þú sérð sérstillingatækjastikuna. 

[![Tækjastika sérstillinga](./media/personalization-personalizationtoolbar.jpg)](./media/personalization-personalizationtoolbar.jpg)

Sérsniðin tækjastika er með fjölda aðgerða sem sérsnið. Velja skal **Velja** verkfærið þegar óskað er að velja og breyta eiginleikum yfir marga þætti, eitt í einu. Fyrst, smella á Velja verkfæri og smellið síðan á eininguna með eiginleika sem óskað er að breyta. Þegar eining er valin opnast gluggi eiginleika einingar og er hægt að breyta hvaða eiginleikumsem er fyrir þá einingu. Hægt er að endurtaka ferlið fyrir aðrar einingar í skjámyndinni sem eru sérsniðnar. Í sumum tilfellum velurðu einingu og sér að ekki er hægt að breyta sumum eiginleikunum. Þetta þýðir að vegna þess hvernig núverandi eining er notuð getur Finance and Operations ekki leyft að þeim eiginleika sé breytt. Til dæmis er ekki hægt að fela áskilinn reit. 

Velja skal **Færa** verkfærið þegar óskað er að velja og færa einingu á aðra staðsetningu innan núverandi einingaflokks. (Ekki er hægt að flytja einingu út fyrir yfirflokk hennar). Fyrst skal smella á verkfærið Flytja og síðan á eininguna sem á að flytja. Þegar smellt er á eininguna sem á að flytja skannar Finance and Operations skjámyndina til að skilja hvert er hægt að flytja eininguna og stofna raðir „sleppistaða“, sem eru sýndir sem lituð, feitletruð lína við svæði þar sem hægt er að sleppa einingunni þegar hún er dregin um innan gildandi flokks. 

Velja skal **Fela** verkfæri til að velja og fela einingar. Til að fela einingar skal einfaldlega velja verkfærði Fela og smella á þá einingu sem óskað er að fela. Þegar verkfærið Fela er valið verða allar einingar sem eru faldar gerðar sýnilegar og sýndar í skyggðu boxi þannig að hægt er að velja eininguna til að hún sé ekki lengur falin. Veldu verkfærið Velja til að sjá hvernig síðan mun líta út með valdar einingar faldar. Velja skal verkfærið **Samantekt** þegar sýna á tölustafa- eða strengjareit á samantektarsvæði flýtiflipa. Samantektarforritið á einungis við um reiti sem eru innan hluta flýtiflipa. Þegar verkfærið Samantekt er valið sýnir Finance and Operations alla reiti sem hafa verið valdir sem samantektarreiti með því að setja þá í skyggð box. Hægt er að bæta gagnvirkt við og fjarlægja reiti úr samantekt flýtiflipa með því að smella á reitinn. 

Velja skal verkfærið **Sleppa** til að fjarlægja einingu úr röð af fliparöð lyklaborðs á síðu. Þegar valið er að Sleppa verkfæri allar einingar sem er sleppt verður sýnd í skyggðu geymir svo hægt sé að velja þær aftur til að gera þær hluti af röð flipanum með því að velja sleppt einingu. 

Velja skal verkfærið **Breyta** þegar merkja á einingu sem Breytanlegt eða Ekki hægt að breyta. Þegar verkfærið Fela er valið verða allar faldar einingar gerðar sýnilegar í skyggðu boxi þannig að hægt er að velja einingu til að gera þær sýnilegar. Athugið sumir reitir eru áskildir og ekki verður hægt að gera þá óbreytanlega. Þessir reitir birtast með hengilás táknið við hlið þeirra. 

Velja skal verkfærið **Bæta við** til að bæta reit við á síðuna. Með verkfæri bæta við, er ekki hægt að stofna nýja reiti, en hægt er að bæta við reitum sem eru hluti af gildandi síðuskilgreiningu, en ekki sýndir á síðunni. Þegar Bæta við verkfæri er valið þarf fyrst að velja flokk eða svæði þar sem bæta á við reit. Svargluggi mun birta lista yfir reiti sem tengjast hluta sem er valinn. Úr þeim svarglugga er hægt að velja einn eða fleiri reiti til að bæta við og smella á Setja inn. Ef þú vilt síðar fjarlægja reit sem þú hefur bætt við áður þarftu að endurtaka ferlið, en hreinsar einfaldlega reitinn sem áður var bætt við. 

Veldu hnappinn **Stjórna** til að sjá lista yfir valkosti notendastjórnunar sem tengjast öllum sérstillingum fyrir núverandi síðu. 

Velja **Hreinsa** til að endurstilla síðuna á sjálfgildi hennar. Allar sérstillingar á núverandi síðu verða hreinsaðar. Það er engin afturköllunaraðgerð, þannig að þú skalt aðeins nota þennan valkost þegar þú ert viss um að endurstilla eigi síðuna. 

Velja **Innflutning** til að nota sérsnið úr sérsniðaskrá sem þú eða einhver annar stofnaði áður fyrir þessa síðu. Innflutningur á sérsniði hreinsar allar sérstillingar sem hafa verið gerðar á allri síðunni og notar í staðinn allar sérstillingar úr valinni skrá. Ef óskað er að vista eða deila sérsniði verður að velja valkostinn **Flytja út** til að vista sérstillingar í skrá. 

Velja skal hnappinn **Loka** til að loka tækjastikunni og fara aftur á síðuna í fyrri stöðu hennar. 

Með tækjastikunni Sérsnið er vistun óbein. Sérstillingar taka strax gildi um leið og þær eru gerðar og það er engin þörf á að smella á í **Vista** hnappinn. Í sumum tilfellum verður sést hengilás táknið við hlið einingu þegar verkfæri er valið. Þetta þýðir að til síðan virki rétt er ekki hægt að breyta eiginleikum sem tengjast völdu verkfæri. Þegar sérsniðna tækjastikan er opnuð verður síðan ógagnvirk. Hægt er að færa inn gögn eða útvíkka eða draga hlutana saman.

## <a name="explicit-personalization-adding-a-tile-or-list-to-a-workspace"></a>Bein sérstilling: Bæta reit eða lista vinnusvæði
Sumar síður með lista hafa viðbótar sérstillingareiginleika tiltæka innan aðgerðasvæðis, undir Sérstilla flokk á flipanum Valkostir. Velja **Bæta við vinnusvæði** til að opna fellilistanum sem gefur möguleika á að sýna upplýsingar í gildandi lista (síuð og raðaðar eða sjálfgefinn) á Vinnusvæði sem lista eða yfirlit reits (sem má nota til að sýna fjölda vara í). 

[![Bæta við vinnusvæði](./media/personalization-addtoworkspace.png)](./media/personalization-addtoworkspace.png) 

Til að bæta lista við vinnusvæði þarf fyrst að flokka eða sía lista með upplýsingum eins og óskað er eftir að sjá þær í sérhverju vinnusvæði, svo velja Bæta við Vinnusvæðið svarglugga. Næst skal velja viðeigandi vinnusvæði og velja **Lista** úr fellilistanum Framsetningu. Þegar **Listi** er valinn opnast svargluggi þar sem hægt er að taka til dálka sem óskað er að finna í lista og merki fyrir lista eins og það mun birtast á vinnusvæðið. 

Til að bæta við reit á vinnusvæði þarf fyrst að sía lista svo að hann sýni þau gögn sem þú vilt taka saman (eða fá skjótan aðgang að). Síðan opnarðu felligluggann Bæta við vinnusvæði. Næst skal velja viðeigandi vinnusvæði og velja **Reit** úr Framsetningu fellilistanum. Þegar **Reitur** er valinn opnast svargluggi þar sem hægt er að veita reitarmerki og ákveða hvort reiturinn sýni talningu. Þegar reiturinn er settur í vinnusvæði verður kleift að opna gildandi síðu úr vinnusvæðinu og sýna lista yfir upplýsingar sem tengjast reitnum. 

Þegar lista eða reit er bætt við vinnusvæði er síðan hægt að opna það vinnusvæði og endurraða listanum eða reitnum í flokknum sem honum var bætt við.

## <a name="explicit-personalization-adding-a-summary-from-a-workspace-to-a-dashboard"></a>Yfirlýst sérsnið: Bæta samantekt úr vinnusvæði í stjórnborð
Sum vinnusvæða innihalda talningarreiti (reitir með númerum á þeim) sem þú vilt einnig sjá á stjórnborðinu. Á vinnusvæðinu hægrismellirðu á talningarreitinn og velur **Aðlaga**. Veldu **Festa á stjórnborð**. Næst þegar farið er á (og endurnýjað) valið stjórnborð sérð það sem talningu undir yfirlitsreit vinnusvæðisins í stjórborðinu.

## <a name="explicit-personalization-personalizing-your-dashboard"></a>Yfirlýst sérsnið: Sérsníða skal stjórnborð
Stjórnborðið er oft fyrsta síðan sem birtist þegar Finance and Operations er opnað. Hægt er að sérsníða stjórnborðið til að endurnefna yfirlitsreiti vinnusvæðis, til að sýna aðeins þá reiti sem þú vilt sjá, endurnefna reiti eða til að hagræða reitum í þeirri röð sem þú vilt sjá þá. Til að sérsníða stjórnborð skal velja hvaða reit sem er og hægrismella til að opna valmynd samhengi. Í samhengisvalmyndinni velurðu **Aðlaga**. Ef valinn reitur er sá sem á að fela eða endurnefna eða sleppa er hægt að gera þá breytingu beint í glugga Eiginleika sem hefur birst. Ef óskað er að raða reitir, veljið síðan **Aðlaga þessa skjámynd** í glugganum Eiginleika til að opna tækjastiku Sérsnið. Síðan er hægt að nota verkfærið Flytja til að raða reitunum.

## <a name="administration-of-personalization"></a>Stjórnun sérstillinga
Eftir að þú hefur sérstillt síðu, getur deilt stillingunum með öðrum notendum með því að flytja út sérstilltu síðuna. Þú getur því næst beðið aðra notendur að fletta að sérstilltu síðunni og flytja inn sérstillingaskrána sem þú stofnaðir.

Notendur sem hafa stjórnunarréttindi geta einnig stýrt sérstillingum fyrir aðra notendur á síðunni **Sérstillingar**. Þessi síða er með fjóra flipa: 

- **Kerfi:** - Þú getur afvirkjað tímabundið eða slökkt á öllum sérstillingum í kerfinu. Í þessu tilfelli er sérstillingum ekki eytt. Þess í stað endurstillirðu allar síður á sjálfgefið ástand þeirra. Ef þú endurvirkjar sérstillingarnar síðar eru þær aftur notaðar á síðu hvers notanda. Einnig er hægt að eyða öllum sérstillingum fyrir alla notendur. Athugið að þegar sérstilingum er eytt er engin leið til að endurvirkja sérstillingar sjálfvirkt úr kerfinu. Áður en þú framkvæmir þetta skref skaltu því ganga úr skugga um að þú hafir flutt allar sérstillingar út sem þú vilt mögulega flytja inn síðar.
- **Notendur** – Hægt er að tilgreina hvort hver notandi geti sett óbeinar eða yfirlýstar sérstillingar. Þú getur einnig tilgreint hvort hver notandi geti sett óbeinar eða yfirlýstar sérstillingar á tiltekinni síðu. Að endingu geturðu flutt inn, flutt út eða eytt sérstillingu fyrir hvern notanda.
- **Flytja inn** – Þú getur flutt inn sérstillingu fyrir einn eða fleiri notendur. Þessi flipi er notaður þegar þú hefur stofnað sérstillingu á síðu eða vinnusvæði og síðan flutt þá sérstillingu út sem sérstillingarskrá. Til að flytja inn sérstillingaskrá þína og nota hana hjá einum eða fleiri notendum skaltu velja einstaka notendur í lista yfir alla notendur eða sía eftir tilteknu hlutverki og velja svo notendur í því hlutverki. Þegar þú hefur valið notendur til að nota nota sérstillinguna þína skaltu smella á **Flytja inn** og velja sérstillingaskrá. Sérstillingin verður villuleituð og notuð hjá öllum völdum notendum næst þegar þeir opna valda síðu.
- **Hreinsa** – Hægt er að hreinsa síðu eða sérstillingu vinnusvæðis fyrir einn eða fleiri notendur. Fyrst skal velja þá síðu eða vinnusvæði sem á að hreinsa sérstillingu fyrir. Næst skaltu velja einstaka notendur á listanum yfir alla notendur eða sía eftir tilteknu hlutverki og svo velja notendur í því hlutverki. Þegar þú hefur valið bæði síðu eða vinnusvæði og notendur skaltu smella á **Hreinsa**. Allar sérstillingar sem valdir notendur hafa notað á síðu sem hefur verið valin eða vinnusvæði eru hreinsaðar. Ekki er hægt að afturkalla þessa aðgerð. Ef sérstilling hefur verið vistuð fyrir síðuna eða vinnusvæðið er hins vegar hægt að flytja þá sérstillingu inn aftur.

## <a name="personalization-of-inventory-dimensions"></a>Sérstilling birgðavídda

Þegar þú sérstillir uppsetningu birgðavídda á síðu, skaltu hafa í huga stillingarnar sem hafa verið búnar til með notkun valkostarins **Sýna víddir**. Ef þú notar til dæmis sérstillingu til að fela dálk fyrir rununúmeri birgðavíddar og dálkurinn birtist næst þegar síðan er opnuð, getur það verið vegna þess að Sýna vídd stillingarnar stjórna því hvaða birgðavíddadálkar eru sýndir. 

Sýna vídd stillingarnar eiga við á öllum síðum og þessar stillingar hnekkja öllum sérstilltum uppsetningum á birgðavíddareitum á stökum síðum. 

Í dæminu um rununúmer birgðavíddar, þá verður að hreinsa þessa vídd sem hluta af **Sýna vídd** valkostinum ef taflan á ekki að sýna þennan dálk. Að lokum mun þessi breyting ekki bara eiga við á einni síðu heldur á öllum síðum.

