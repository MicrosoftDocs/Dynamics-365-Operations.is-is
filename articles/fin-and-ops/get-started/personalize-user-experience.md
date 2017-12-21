---
title: "Sérsniðin notkun"
description: "Þessi grein útskýrir hvernig hægt er að sérsníða Microsoft Dynamics 365 for Finance and Operations."
author: TLeforMicrosoft
manager: AnnBe
ms.date: 10/10/2017
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
ms.sourcegitcommit: 7a828090fa34eb96d2b557eb06e48ad05b421ae8
ms.openlocfilehash: 3d969069dd5f447b449df84b097527d3814aa338
ms.contentlocale: is-is
ms.lasthandoff: 11/20/2017

---

# <a name="personalize-the-user-experience"></a>Sérsniðin notkun

[!include[banner](../includes/banner.md)]


Þessi grein útskýrir hvernig hægt er að sérsníða Microsoft Dynamics 365 for Finance and Operations.

Það eru margar gerðir sérstillinga í Microsoft Dynamics 365 for Finance and Operations. Sumar sérstillingar eru valdar í lista yfir valkosti á uppsetningarsíðunni. Sumar sérstillingar eru óbeinar, til dæmis heldur Finance and Operations utan um breidd dálka í hnitanetinu ef það þarf að leiðrétta þá og útvíkkaða/samandregna stöðu flýtiflipa. Aðrar sérstillingar eru beinar. Fyrir beinar sérstillingar er færður inn gagnvirkur sérsniðsmáti og útliti síðu breytt með því að stjórna því hvernig einingar birtast eða bregðast við á síðunni. 

Allar sérstillingar, af hvaða tagi sem er, sem notandi gerir í Finance and Operations eru aðeins fyrir þann notanda, burtséð frá fyrirtækinu sem notandinn vinnur með. Breytingar sem notandi gerir á síðu hafa ekki áhrif á aðra notendur kerfisins.

## <a name="system-wide-options-for-the-current-user"></a>Kerfisaltækir valkostir fyrir núverandi notanda
Í yfirlitsstiku finnurðu mynd af tannhjóli, sem kallast valmyndarhnappurinn **Stillingar**. Opnun valmyndarinnar **Stillingar** mun sýna fjölda valkosta. Val á **Valkostir** opnar síðuna **Valkostir** notanda. Þar finnurðu fjóra valkostaflipa: 

-   **Visual:** Notað til að velja litaþema og sjálfgefin stærð einingar á síðum fyrirtækisins.
-   **Kjörstillingar:** Hér er hægt að velja sjálfgildi fyrir hvert sinn sem Finance and Operations er opnað, þ.m.t. fyrirtækið, upphafssíðu og sjálfgefið yfirlit/breytingahamur (sem ákveður hvort síðu er læst fyrir skoðun eða opinn til breytinga í hvert sinn sem hún er opnuð). Einnig er verður hægt að finna tungumál, tímabelti og dagsetningu, tíma- og númer snið valkosti. Að endingu inniheldur þessi síða fjölda ýmissa kjörstillinga sem eru breytilegar frá losun til að losa.
-   **Lykill:** Notað til að veita Notandakenni og aðra lykiltengda valkosti.
-   **Verkflæði:** Hér er hægt er að velja erkflæðistengda valkosti.

## <a name="implicit-personalizations"></a>Óbeinar sérstillingar
Óbeinar sérstillingar eru þær sérstillingar sem eru framkvæmdar einfaldlega með notkun ákveðinna stýringa sem muna núverandi stöðu sína. 

- **Dálkar í hnitanetinu:** Hægt er að stilla breidd dálks í lista með því að velja stærðarstikuna til vinstri eða hægri við dálkhausinn og renna henni til vinstri eða hægri um æskilega breidd. Finance and Operations geymir breiddina sem á að stilla og sýna dálkinn með þeirri breidd í hvert skipti sem síðan er opnuð sem listi. 

- **Flýtiflipar:** - Sumar síður hafa stækkanlega hluta sem kallast *flýtiflipar*. Finance and Operations geymir hvaða flýtiflipar hafa verið útvíkkaðir og hvaða flýtiflipar hafa verið dregnir saman. Í hvert sinn sem síðu er skilað eru þessir sömu flýtiflipar útvíkkaðir eða dregnir saman byggð á þeim var notað síðast. Í þessari grein verður útskýrt hvernig á að breyta röðun á flýtiflipunum. Í sumum tilvikum getur minnkun flýtiflipa bætt afköst því Finance and Operations þarf ekki að sækja upplýsingar um þá flýtiflipa fyrr en flýtiflipinn er útvíkkaður. 

- **Staðreyndareitir** - Sumar síður hafa hluta sem kallast *Staðreyndareitir*. Þessi rúða inniheldur aðeins til lestrar upplýsingar sem tengjast gildandi efni á síðunni. Hver kafli í staðreyndarúðunni er kallaður staðreyndareitur. Hægt er að útvíkka eða draga saman staðreyndareiti og Finance and Operations mun geyma forstillingar þínar. Í sumum tilvikum getur minnkun staðreyndareita bætt afköst því Finance and Operations þarf ekki að sækja upplýsingar um þá staðreyndareiti fyrr en staðreyndareiturinn er útvíkkaður.

## <a name="explicit-personalizations-using-the-personalization-toolbar"></a>Yfirlýstar sérstillingar með sérsniðinni verkfærastiku
Hver einstaklingur og fyrirtæki hefur mismunandi sjónarhorn um hvaða gögn eru þeim mikilvægust eða hvaða gögn er ekki þörf fyrir hátt rekstrinum þær keyrðar. Möguleikinn á að sníða hvernig upplýsingum er raðað, unnið með þær eða þær jafnvel faldar er lykillinn að því að gera Finance and Operations persónulegt og skilvirkt. 

Beinar sérstillingar eru þær sérstillingar sem eru framkvæmdar beint og er ætlað að breyta útliti eða hegðun á einingu eða síðunni með því að velja sérsnið valmynd. Grunngerð beinna sérstillinga er þar sem hægrismellt er á einingu og valið **Sérsníða**. (Athugið að ekki er hægt að sérsníða allar einingar á síðunni.) Þegar þessi sérstillingaraðferð er valin sérðu eiginleikaglugga einingarinnar. 

[![Sérsníða eiginleika í einingu](./media/personalization-element-properties.jpg)](./media/personalization-element-properties.jpg) 

Eining á síðu er breytt á þennan hátt ef einfaldlega á að breyta merki einingarinnar, fela eininguna svo að hún birtist ekki á síðunni (þetta breytir ekki neinum gögnum, heldur sýnir einfaldlega ekki sum gögn), hafa með upplýsingar í samantektarhluta flýtiflipa (ef eining er í flýtiflipa), sleppa reitnum við flipastjórnun eða stilla hann þannig að ekki sé hægt að breyta sumum gögnum með því að merkja hann sem „Ekki breyta.“ 

Þegar óskað er að flytja eða fela einingar eða gera nokkrar breytingar, er hægt að nota sérstillingatækjastikuna sem er tiltæk úr glugganum einingar Eiginleika með því að velja **Aðlaga þessa skjámynd**. Sérstillingatækjastikan er einnig tiltæk í aðgerðarúðu skjámyndarinnar, undir **Sérstillingar** flokkur á flipanum **Valkostir**. Velja **Sérstilla þessa skjámynd** og þá sérðu Sérstillingatækjastikuna. 

[![Tækjastika sérstillinga](./media/personalization-personalizationtoolbar.jpg)](./media/personalization-personalizationtoolbar.jpg)

Sérsniðin tækjastika er með fjölda aðgerða sem sérsnið. 

- Velja skal **Velja** verkfærið þegar óskað er að velja og breyta eiginleikum yfir marga þætti, eitt í einu. Fyrst, smella á Velja verkfæri og smellið síðan á eininguna með eiginleika sem óskað er að breyta. Þegar eining er valin opnast gluggi eiginleika einingar og er hægt að breyta hvaða eiginleikumsem er fyrir þá einingu. Hægt er að endurtaka ferlið fyrir aðrar einingar í skjámyndinni sem eru sérsniðnar. Í sumum tilfellum velurðu einingu og sér að ekki er hægt að breyta sumum eiginleikunum. Þetta þýðir að vegna þess hvernig núverandi eining er notuð getur Finance and Operations ekki leyft að þeim eiginleika sé breytt. Til dæmis er ekki hægt að fela áskilinn reit. 

- Velja skal **Færa** verkfærið þegar óskað er að velja og færa einingu á aðra staðsetningu innan núverandi einingaflokks. (Ekki er hægt að flytja einingu út fyrir yfirflokk hennar). Fyrst skal smella á verkfærið Flytja og síðan á eininguna sem á að flytja. Þegar smellt er á eininguna sem á að flytja mun Finance and Operations skanna skjámyndina til að skilja hvert er hægt að flytja eininguna og stofna raðir „sleppistaða“ sem eru sýndir sem lituð, feitletruð lína við svæði þar sem hægt er að sleppa einingunni þegar hún er dregin um innan gildandi flokks. 

- Velja skal **Fela** verkfæri til að velja og fela einingar. Til að fela einingar skal einfaldlega velja verkfærði Fela og smella á þá einingu sem óskað er að fela. Þegar verkfærið Fela er valið verða allar einingar sem eru faldar gerðar sýnilegar og sýndar í skyggðu boxi þannig að hægt er að velja eininguna til að hún sé ekki lengur falin. 

- Veldu verkfærið **Velja** til að sjá hvernig síðan mun líta út með valdar einingar faldar. 

- Velja skal verkfærið **Samantekt** þegar sýna á tölustafa- eða strengjareit á samantektarsvæði flýtiflipa. Samantektarforritið á einungis við um reiti sem eru innan hluta flýtiflipa. Þegar verkfærið Samantekt er valið sýnir Finance and Operations alla reiti sem hafa verið valdir sem samantektarreiti með því að setja þá í skyggð box. Hægt er að bæta gagnvirkt við og fjarlægja reiti úr samantekt flýtiflipa með því að smella á reitinn. 

- Velja skal verkfærið **Sleppa** til að fjarlægja einingu úr röð af fliparöð lyklaborðs á síðu. Þegar valið er að Sleppa verkfæri allar einingar sem er sleppt verður sýnd í skyggðu geymir svo hægt sé að velja þær aftur til að gera þær hluti af röð flipanum með því að velja sleppt einingu. 

- Velja skal verkfærið **Breyta** þegar merkja á einingu sem *Breytanlegt* eða *Ekki hægt að breyta*. Þegar verkfærið Fela er valið verða allar faldar einingar gerðar sýnilegar í skyggðu boxi þannig að hægt er að velja einingu til að gera þær sýnilegar. Athugið sumir reitir eru áskildir og ekki verður hægt að gera þá óbreytanlega. Þessir reitir birtast með hengilás táknið við hlið þeirra. 

- Velja skal verkfærið **Bæta við** til að bæta reit við á síðuna. Með verkfæri bæta við, er ekki hægt að stofna nýja reiti, en hægt er að bæta við reitum sem eru hluti af gildandi síðuskilgreiningu, en ekki sýndir á síðunni. Þegar Bæta við verkfæri er valið þarf fyrst að velja flokk eða svæði þar sem bæta á við reit. Svargluggi mun birta lista yfir reiti sem tengjast hluta sem er valinn. Úr þeim svarglugga er hægt að velja einn eða fleiri reiti til að bæta við og smella á **Setja inn**. Ef þú vilt síðar fjarlægja reit sem þú hefur bætt við áður þarftu að endurtaka ferlið, en hreinsar einfaldlega reitinn sem áður var bætt við. 

- Veldu hnappinn **Stjórna** til að sjá lista yfir valkosti notendastjórnunar sem tengjast öllum sérstillingum fyrir núverandi síðu. 

- Velja **Hreinsa** til að endurstilla síðuna á sjálfgildi hennar. Allar sérstillingar á núverandi síðu verða hreinsaðar. Það er engin afturköllunaraðgerð, þannig að þú skalt aðeins nota þennan valkost þegar þú ert viss um að endurstilla eigi síðuna. 

- Velja **Innflutning** til að nota sérsnið úr sérsniðaskrá sem þú eða einhver annar stofnaði áður fyrir þessa síðu. Innflutningur á sérsniði hreinsar allar sérstillingar sem hafa verið gerðar á allri síðunni og notar í staðinn allar sérstillingar úr valinni skrá. Ef óskað er að vista eða deila sérsniði verður að velja valkostinn **Flytja út** til að vista sérstillingar í skrá. 

- Velja skal hnappinn **Loka** til að loka tækjastikunni og skila síðunni aftur í fyrri stöðu hennar. 

Með tækjastikunni Sérsnið er vistun óbein. Sérstillingar taka strax gildi um leið og þær eru gerðar og það er engin þörf á að smella á í **Vista** hnappinn. Í sumum tilfellum verður sést hengilás táknið við hlið einingu þegar verkfæri er valið. Þetta þýðir að til síðan virki rétt er ekki hægt að breyta eiginleikum sem tengjast völdu verkfæri. Þegar sérsniðna tækjastikan er opnuð verður síðan ógagnvirk. Hægt er að færa inn gögn eða útvíkka eða draga hlutana saman.

## <a name="explicit-personalization-adding-a-tile-or-list-to-a-workspace"></a>Bein sérstilling: Bæta reit eða lista vinnusvæði
Sumar síður með listum munu hafa aukaeiginleika fyrir sérstillingar í boðin innan Aðgerðarúðu þeirra, undir **Sérsníða** flokkur á **Valkosta** flipanum. Velja **Bæta Vinnusvæði** til að opna fellilistanum sem gefur möguleika á að sýna upplýsingar í núgildandi lista (síaðar og raðaðar eða sjálfgefnar) á vinnusvæði í formi lista eða samantektarreits (sem má nota til að sýna fjölda atriða á listanum). 

[![Bæta við vinnusvæði](./media/personalization-addtoworkspace.png)](./media/personalization-addtoworkspace.png) 

Til að bæta lista við vinnusvæði þarf fyrst að flokka eða sía lista með upplýsingum eins og óskað er eftir að sjá þær í sérhverju vinnusvæði, svo velja **Bæta við Vinnusvæðið** svarglugga. Næst skal velja viðeigandi vinnusvæði og velja **Lista** úr fellilistanum **Kynning**. Þegar **Listi** er valinn opnast svargluggi þar sem hægt er að taka til dálka sem óskað er að finna í lista og merki fyrir lista eins og það mun birtast á vinnusvæðið. 

Til að bæta við reit á vinnusvæði þarf fyrst að sía lista svo að hann sýni þau gögn sem þú vilt taka saman (eða fá skjótan aðgang að). Síðan opnarðu felligluggavalmynd **Bæta við vinnusvæði**. Næst skal velja viðeigandi vinnusvæði og velja **Reitur** úr **Framsetning** fellilistavalmynd. Þegar **Reitur** er valinn opnast svargluggi þar sem hægt er að veita reit merki og ákveða hvort reiturinn sýni talningu. Þegar reiturinn er settur í vinnusvæði verður kleift að opna gildandi síðu úr vinnusvæðinu og sýna lista yfir upplýsingar sem tengjast reitnum. 

Þegar lista eða reit er bætt við vinnusvæði er síðan hægt að opna það vinnusvæði og endurraða listanum eða reitnum í flokknum sem honum var bætt við.

## <a name="explicit-personalization-adding-a-summary-from-a-workspace-to-a-dashboard"></a>Yfirlýst sérsnið: Bæta samantekt úr vinnusvæði í stjórnborð
Sum vinnusvæða innihalda talningarreiti (reitir með númerum á þeim) sem þú vilt einnig sjá á stjórnborðinu. Á vinnusvæði skal hægrismella á talningarreitinn og velja **Sérsníða**, og svo velja **Festa við stjórnborð**. Næst þegar farið er á (og endurnýjað) valið stjórnborð sérð það sem talningu undir yfirlitsreit vinnusvæðisins í stjórborðinu.

## <a name="explicit-personalization-personalizing-your-dashboard"></a>Yfirlýst sérsnið: Sérsníða skal stjórnborð
Stjórnborðið er oft fyrsta síðan sem birtist þegar Finance and Operations er opnað. Hægt er að sérsníða stjórnborðið til að endurnefna yfirlitsreiti vinnusvæðis, til að sýna aðeins þá reiti sem þú vilt sjá, endurnefna reiti eða til að hagræða reitum í þeirri röð sem þú vilt sjá þá. 

Til að sérsníða stjórnborð skal velja hvaða reit sem er og hægrismella til að opna valmynd samhengi. Í samhengisvalmyndinni velurðu **Aðlaga**. Ef valinn reitur er sá sem á að fela eða endurnefna eða sleppa er hægt að gera þá breytingu beint í glugga Eiginleika sem hefur birst. Ef óskað er að raða reitir, veljið síðan **Aðlaga þessa skjámynd** í glugganum Eiginleika til að opna tækjastiku Sérsnið. Síðan er hægt að nota verkfærið **Flytja** til að raða reitunum.

## <a name="administration-of-personalization"></a>Stjórnun sérstillinga
Eftir að þú hefur sérsniðið síðu, getur deilt stillingunum með öðrum notendum með því að flytja út sérstilltu síðuna. Þú getur þá beðið hina notendur að fara á sérstilltu síðuna og flytja inn sérstillingarskrá sem þú bjóst til, eða þú getur gefið sérstillingar þínar til notanda sem hefur stjórnandi réttindi sem getur síðan sett sérstillingar þínar í virkni hjá mörgum notendum í einu.

Notendur sem hafa stjórnunarréttindi geta einnig stýrt sérstillingum fyrir aðra notendur á síðunni **Sérstillingar**. Þessi síða er með fjóra flipa: 

- **Virkja** - Hægt er að flytja inn eða velja sérstillingu fyrir einn eða fleiri notendur. Til að setja sérstillingu í virkni hjá einum eða fleiri notendum, skal velja hlutverk og síðan notendur innan þess hlutverks. Síðan skal velja fyrirliggjandi sérstillingar eða flytja inn sérstillingarskrá til að setja í virkni hjá þeim notendum sem hafa verið valdir. Sérstillingin verður villuleituð og notuð hjá öllum völdum notendum næst þegar þeir opna valda síðu.

- **Hreinsa** – Hægt er að hreinsa síðu eða sérstillingu vinnusvæðis fyrir einn eða fleiri notendur. Veljið síðu til að sjá lista yfir þá notendur sem hafa sérstillt þá síðu. Veljið síðan þá notendur sem á að fjarlægja sérstillingar þeirrar síðu fyrir og veljið **Hreinsa**. Allar sérstillingar sem valdir notendur hafa notað á síðu sem hefur verið valin eða vinnusvæði eru hreinsaðar. Ekki er hægt að afturkalla þessa aðgerð. Ef sérstilling hefur verið vistuð fyrir síðuna eða vinnusvæðið er hins vegar hægt að flytja þá sérstillingu inn aftur.

- **Framkvæmdastjóri á notanda** - Veldu notanda til að sjá lista yfir síður sem sá einstaklingur hefur sérstillt.  Síðan er hægt að virkja eða afvirkja möguleika þeirra á að nota aðlögun fyrir ákveðnar síður eða fyrir kerfið í heild.  Þú getur einnig flutt inn, flutt út eða hreinsað sérstillingar fyrir þennan notanda.

- **Kerfi** - Einnig er hægt að aftengja öllum sérstillingum allra notendur kerfisins tímabundið. Það mun ekki eyða sérstillingum heldur einfaldlega endurstilla allar síður í sjálfgefið ástand fyrir alla notendur. Ef þú endurvirkjar sérstillingar seinna, verða allar sérstillingar settar í virkni á ný. Einnig er hægt að eyða öllum sérstillingum endanlega fyrir alla notendur kerfisins. Gætið þess að flytja út allar þær sérstillingar sem hugsanlegt er að þú viljir nota síðar áður en það er gert, þar sem ekki er hægt að endurheimta síðar sérstillingar sem hefur verið eytt. 

## <a name="personalization-of-inventory-dimensions"></a>Sérstilling birgðavídda

Þegar þú sérstillir uppsetningu birgðavídda á síðu, skaltu hafa í huga stillingarnar sem hafa verið búnar til með notkun valkostarins **Sýna víddir**. Ef þú notar til dæmis sérstillingu til að fela dálk fyrir rununúmeri birgðavíddar og dálkurinn birtist næst þegar síðan er opnuð, getur það verið vegna þess að Sýna vídd stillingarnar stjórna því hvaða birgðavíddadálkar eru sýndir. 

Sýna vídd stillingarnar eiga við á öllum síðum og þessar stillingar hnekkja öllum sérstilltum uppsetningum á birgðavíddareitum á stökum síðum. 

Í dæminu um rununúmer birgðavíddar, þá verður að hreinsa þessa vídd sem hluta af **Sýna vídd** valkostinum ef taflan á ekki að sýna þennan dálk. Að lokum mun þessi breyting ekki bara eiga við á einni síðu heldur á öllum síðum.

