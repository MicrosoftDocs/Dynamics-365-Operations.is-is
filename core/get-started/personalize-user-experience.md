---
title: "Sérstilling viðmótsins"
description: "Þessi skrá er útskýrt hvernig hægt er að sérsníða Microsoft Dynamics 365 fyrir Aðgerðir."
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SysUserSetup
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 62363
ms.assetid: 57b445d7-3e9e-4228-8728-f63b9dbd77a3
ms.search.region: Global
ms.author: tlefor
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4bb647cfd3f012efbffa93a81462c538a24ac850
ms.openlocfilehash: 8965c193839002776b3c61036b23b54625c974a4
ms.lasthandoff: 03/31/2017


---

# <a name="personalize-the-user-experience"></a>Sérstilling viðmótsins

Þessi skrá er útskýrt hvernig hægt er að sérsníða Microsoft Dynamics 365 fyrir Aðgerðir.

Það eru margar gerðir personalizations í Microsoft Dynamics 365 aðgerða. Sumar sérstillingar eru valdar í lista yfir valkosti á uppsetningarsíðunni. Sumar personalizations eru implicit, til dæmis Dynamics 365 aðgerða heldur utan um widths dálka í hnitanetinu ef að leiðrétta þær og útvíkkaður/dregin saman stöðu FastTabs. Aðrar sérstillingar eru beinar. Fyrir beinar sérstillingar er færður inn gagnvirkur sérsniðsmáti og útliti síðu breytt með því að stjórna því hvernig einingar birtast eða bregðast við á síðunni. 

Allar personalizations af hvaða tagi sem notandi gerir í Dynamics 365 fyrir Aðgerðir eru fyrir þann notanda, burtséð frá fyrirtækinu sem notandi sem vinnur með. Breytingar sem notandi gerir á síðu hafa ekki áhrif á aðra notendur kerfisins.

## <a name="systemwide-options-for-the-current-user"></a>Valkostir Kerfisaltæka fyrir núverandi notanda
Í yfirlitsstiku finnurðu mynd af tannhjóli, sem kallast valmyndarhnappurinn **Stillingar**. Opnun valmyndarinnar **Stillingar** mun sýna fjölda valkosta. Val á **Valkostir** opnar síðuna **Valkostir** notanda. Þar finnurðu fjóra valkostaflipa: **Visual**, **Kjörstillingar**, **Lykil** og **Verkflæði**.

-   **Visual: **Notað til að velja litaþema og sjálfgefin stærð einingar á síðum fyrirtækisins.
-   **: Kjörstillingar** Hér er hægt að velja sjálfgildi fyrir hvert sinn sem er að opna Dynamics 365 fyrir Aðgerðir, þ.m.t. fyrirtækið, upphafssíðan sem er og sjálfgefið yfirlit/breytingahamur (sem ákveður hvort síðu er læst fyrir skoðun eða opinn til breytinga í hvert sinn sem hún er opnuð). Einnig er verður hægt að finna tungumál, tímabelti og dagsetningu, tíma- og númer snið valkosti. Að endingu inniheldur þessi síða fjölda ýmissa kjörstillinga sem eru breytilegar frá losun til að losa.
-   **Lykill: **Notað til að veita Notandakenni og aðra lykiltengda valkosti.
-   **Verkflæði: **Hér er hægt er að velja erkflæðistengda valkosti.

## <a name="implicit-personalizations"></a>Óbeinar sérstillingar
Óbeinar sérstillingar eru þær sérstillingar sem eru framkvæmdar einfaldlega með notkun ákveðinna stýringa sem muna núverandi stöðu sína. 

**Dálkar í hnitanetinu:** Hægt er að stilla breidd dálks í lista með því að velja stærðarstikuna til vinstri eða hægri við dálkhausinn og renna henni til vinstri eða hægri um æskilega breidd. Dynamics 365 fyrir Aðgerðir verður að geyma breidd að myndi óskað og sýna sem dálkur með sem breidd í hvert sinn opna síðuna með listanum sem. 

**Flýtiflipar:** Sumar síður hafa stækkanlega hluta sem kallast flýtiflipar. Dynamics 365 fyrir Aðgerðir verður að geyma hvaða FastTabs sem hefur verið útvíkkuð og hvaða FastTabs sem hafa verið dregin saman. Í hvert sinn sem síðu er skilað eru þessir sömu flýtiflipar útvíkkaðir eða dregnir saman byggð á þeim var notað síðast. Í þessari grein verður útskýrt hvernig á að breyta röðun á flýtiflipunum. Í sumum tilvikum, collapsing FastTab getur bætt afköst þar sem Dynamics 365 fyrir Aðgerðir sem þarf ekki að sækja upplýsingar um þá FastTab fyrr en á Flýtiflipanum er útvíkkuð. 

**Staðreyndareitir:** Sumar síður hafa hluta sem kallast Staðreyndarúða. Þessi rúða inniheldur aðeins til lestrar upplýsingar sem tengjast gildandi efni á síðunni. Hver kafli í staðreyndarúðunni er kallaður staðreyndareitur. Hægt er að útvíkka eða draga saman með Staðreyndum og Dynamics 365 fyrir Aðgerðir verður að geyma skal val. Í sumum tilvikum, collapsing með Staðreyndum getur bætt afköst því Dynamics 365 fyrir Aðgerðir sem þarf ekki að sækja upplýsingar um þá Staðreyndum fyrr en á Staðreyndum er útvíkkuð.

## <a name="explicit-personalizations-using-the-personalization-toolbar"></a>Yfirlýstar sérstillingar með sérsniðinni verkfærastiku
Hver einstaklingur og fyrirtæki hefur mismunandi sjónarhorn um hvaða gögn eru þeim mikilvægust eða hvaða gögn er ekki þörf fyrir hátt rekstrinum þær keyrðar. Möguleika á að sníða hvernig upplýsingum er pantað, interacted með eða jafnvel falin er að gera persónulegar og framleiðinna reynslu Dynamics 365 fyrir Aðgerðir. 

Yfirlýst personalizations eru þær personalizations sem beint er framkvæmt með intent til að breyta útliti eða hegðun á einingu eða síðunni með því að velja sérsnið valmynd. Flestar grunnur gerð yfirlýst sérsnið er þar sem eining hægrismella og velja **Personalize**. (Athugið að ekki allar einingar á síðu skal geta sérstillt.) Þegar þessi aðferð sérsnið, verður að finna glugga eiginleiki einingar. 

[![Sérsníða eiginleika í einingu](./media/personalization-element-properties.jpg)](./media/personalization-element-properties.jpg) 

Eining á síðu er breytt á þennan hátt ef einfaldlega á að breyta merki einingarinnar, fela eininguna svo að hún birtist ekki á síðunni (þetta breytir ekki neinum gögnum, heldur sýnir einfaldlega ekki sum gögn), hafa með upplýsingar í samantektarhluta flýtiflipa (ef eining er í flýtiflipa), sleppa reitnum við flipastjórnun eða stilla hann þannig að ekki sé hægt að breyta sumum gögnum með því að merkja hann sem „Ekki breyta.“ 

Þegar óskað er að flytja eða fela einingar eða gera nokkrar breytingar, er hægt að nota sérstillingatækjastikuna sem er tiltæk úr glugganum einingar Eiginleika með því að velja **Aðlaga þessa skjámynd**. Sérstillingatækjastikan er einnig tiltæk í aðgerðarúðu skjámyndarinnar, undir Sérstillingar flokks í **Valkosti** flipa. Veldu **Aðlaga þessa skjámynd** og þú sérð sérstillingatækjastikuna. 

[![Sérsnið verkfæraslána](./media/personalization-personalizationtoolbar.jpg)](./media/personalization-personalizationtoolbar.jpg)

Verkfæraslá Sérsnið með fjölda aðgerða sem sérsnið. Velja skal **Velja** verkfærið þegar óskað er að velja og breyta eiginleikum yfir marga þætti, eitt í einu. Fyrst, smella á Velja verkfæri og smellið síðan á eininguna með eiginleika sem óskað er að breyta. Þegar eining er valin opnast gluggi eiginleika einingar og er hægt að breyta hvaða eiginleikumsem er fyrir þá einingu. Hægt er að endurtaka ferlið fyrir aðrar einingar í skjámyndinni sem eru sérsniðnar. Í sumum tilfellum velurðu einingu og sér að ekki er hægt að breyta sumum eiginleikunum. Þetta þýðir að byggt á því hvernig núverandi eining er notuð, 365 Dynamics aðgerða ekki hægt er að breyta þeim eiginleika. Til dæmis er ekki hægt að fela áskilinn reit. 

Velja skal **Færa** verkfærið þegar óskað er að velja og færa einingu á aðra staðsetningu innan núverandi einingaflokks. (Ekki er hægt að flytja einingu út fyrir yfirflokk hennar). Fyrst skal smella á verkfærið Flytja og síðan á eininguna sem á að flytja. Þegar smellt er á eininguna sem á að flytja Dynamics 365 fyrir Aðgerðir verða að skanna skjámyndina til að skilja þar sem þessi eining er hægt að færa og stofna raðir af "sleppa staði" sem sýna litaða, feitletrað línu við svæði þar sem eining getur fellt sem er að draga einingar um innan flokksins. 

Velja skal **Fela** verkfæri til að velja og fela einingar. Til að fela einingar skal einfaldlega velja verkfærði Fela og smella á þá einingu sem óskað er að fela. Þegar verkfærið Fela er valið verða allar einingar sem eru faldar gerðar sýnilegar og sýndar í skyggðu boxi þannig að hægt er að velja eininguna til að hún sé ekki lengur falin. Veldu verkfærið Velja til að sjá hvernig síðan mun líta út með valdar einingar faldar. Velja skal verkfærið **Samantekt** þegar sýna á tölustafa- eða strengjareit á samantektarsvæði flýtiflipa. Samantektarforritið á einungis við um reiti sem eru innan hluta flýtiflipa. Þegar valið er Samantekt verkfæri Dynamics 365 aðgerða sýna öll svæði sem hafa verið valin sem samantekt svæði með enclosing þær í skyggðu gáms. Hægt er að bæta gagnvirkt við og fjarlægja reiti úr samantekt flýtiflipa með því að smella á reitinn. 

Velja skal **Sleppa** verkfæri til að fjarlægja einingu úr röð fyrir flipinn lyklaborð á síðu. Þegar valið er að Sleppa verkfæri allar einingar sem er sleppt verður sýnd í skyggðu gáms svo hægt sé að velja þær aftur til að gera þá hluta af flipanum númeraröð með því að velja sleppt einingu. 

Velja skal verkfærið **Breyta** þegar merkja á einingu sem Breytanlegt eða Ekki hægt að breyta. Þegar verkfærið Fela er valið verða allar faldar einingar gerðar sýnilegar í skyggðu boxi þannig að hægt er að velja einingu til að gera þær sýnilegar. Athugið sumir reitir eru áskildir og ekki verður hægt að gera þá óbreytanlega. Þessir reitir birtast með hengilás táknið við hlið þeirra. 

Velja skal verkfærið **Bæta við** til að bæta reit við á síðuna. Með verkfæri bæta við, er ekki hægt að stofna nýja reiti, en hægt er að bæta við reitum sem eru hluti af gildandi síðuskilgreiningu, en ekki sýndir á síðunni. Þegar Bæta við verkfæri er valið þarf fyrst að velja flokk eða svæði þar sem bæta á við reit. Svargluggi mun birta lista yfir reiti sem tengjast hluta sem er valinn. Úr þeim svarglugga er hægt að velja einn eða fleiri reiti til að bæta við og smella á Setja inn. Ef þú vilt síðar fjarlægja reit sem þú hefur bætt við áður þarftu að endurtaka ferlið, en hreinsar einfaldlega reitinn sem áður var bætt við. 

Velja skal **Stjórna** hnappinn til að sjá lista yfir valkosti notendastjórnunar tengjast öllum personalizations fyrir núverandi síðu. 

Velja **Hreinsa** uppsett til að endurstilla síðan hennar sjálfgefna stöðu. Verður að hreinsa allar personalizations á núverandi síðu. Það er engin aðgerð afturkalla, þannig að aðeins að nota þennan valkost þegar ákveðnar sem á að endurstilla skal síðu. 

Velja **Innflutning** til að nota sérsnið úr sérsniðaskrá sem þú eða einhver annar stofnaði áður fyrir þessa síðu. Innflutningur á sérsniði hreinsar allar sérstillingar sem hafa verið gerðar á allri síðunni og notar í staðinn allar sérstillingar úr valinni skrá. Ef óskað er að vista eða deila sérsniði verður að velja valkostinn **Flytja út** til að vista sérstillingar í skrá. 

Velja skal hnappinn **Loka** til að loka tækjastikunni og fara aftur á síðuna í fyrri stöðu hennar. 

Með tækjastikunni Sérsnið er vistun óbein. Sérstillingar taka strax gildi um leið og þær eru gerðar og það er engin þörf á að smella á í **Vista** hnappinn. Í sumum tilfellum verður sést hengilás táknið við hlið einingu þegar tæki. Þetta þýðir að í röð fyrir síðu til að vinna rétt sem er hægt að breyta eiginleikum sem tengjast völdum verkfæri. Þegar sérsniðna tækjastikan er opnuð verður síðan ógagnvirk. Hægt er að færa inn gögn eða útvíkka eða draga hlutana saman.

## <a name="explicit-personalization-adding-a-tile-or-list-to-a-workspace"></a>Bein sérstilling: Bæta reit eða lista vinnusvæði
Sumar síður með lista hafa viðbótar sérstillingareiginleika tiltæka innan aðgerðasvæðis, undir Sérstilla flokk á flipanum Valkostir. Velja **Bæta Vinnusvæði** til að opna fellilistanum sem gefur möguleika á að sýna upplýsingar í gildandi lista (síuð og raðaðar eða sjálfgefinn) á Vinnusvæði sem lista eða yfirlit reitar (sem má nota til að sýna fjölda vara í). 

[![Add to workspace](./media/personalization-addtoworkspace.png)](./media/personalization-addtoworkspace.png) 

Til að bæta lista við vinnusvæði þarf fyrst að flokka eða sía lista með upplýsingum eins og óskað er eftir að sjá þær í sérhverju vinnusvæði, svo velja Bæta við Vinnusvæðið svarglugga. Næst skal velja viðeigandi vinnusvæði og velja **Lista** úr fellilistanum Framsetningu. Þegar **Listi** er valinn opnast svargluggi þar sem hægt er að taka til dálka sem óskað er að finna í lista og merki fyrir lista eins og það mun birtast á vinnusvæðið. 

Til að bæta við reit á vinnusvæði þarf fyrst að sía lista svo að hann sýni þau gögn sem þú vilt taka saman (eða fá skjótan aðgang að). Síðan opnarðu felligluggann Bæta við vinnusvæði. Næst skal velja viðeigandi vinnusvæði og velja **Reit** úr Framsetningu fellilistanum. Þegar **Reitur** er valinn opnast svargluggi þar sem hægt er að veita reitarmerki og ákveða hvort reiturinn sýni talningu. Þegar reiturinn er settur í vinnusvæði verður kleift að opna gildandi síðu úr vinnusvæðinu og sýna lista yfir upplýsingar sem tengjast reitnum. 

Þegar lista eða reit er bætt við vinnusvæði er síðan hægt að opna það vinnusvæði og endurraða listanum eða reitnum í flokknum sem honum var bætt við.

## <a name="explicit-personalization-adding-a-summary-from-a-workspace-to-a-dashboard"></a>Yfirlýst sérsnið: Bæta samantekt úr vinnusvæði í stjórnborð
Sumar vinnusvæðin innihaldið talningu reitir (reitir með númerum á þeim) er einnig óskað að sjá skal mælaborð. Vinnusvæði, talningu reitar hægrismellið og veljið **Personalize**. Veldu **Festa á stjórnborð**. Næst þegar farið er á (og endurnýjað) valið stjórnborð sérð það sem talningu undir yfirlitsreit vinnusvæðisins í stjórborðinu.

## <a name="explicit-personalization-personalizing-your-dashboard"></a>Yfirlýst sérsnið: Sérsníða skal stjórnborð
Í mælaborð er oft fyrsta síðan sem birtist verður þegar þú opnar Dynamics 365 fyrir Aðgerðir. Hægt er að sérsníða stjórnborðið til að endurnefna yfirlitsreiti vinnusvæðis, til að sýna aðeins þá reiti sem þú vilt sjá, endurnefna reiti eða til að hagræða reitum í þeirri röð sem þú vilt sjá þá. Til að sérsníða stjórnborð skal velja hvaða reit sem er og hægrismella til að opna valmynd samhengi. Í samhengisvalmyndinni velurðu **Aðlaga**. Ef valinn reitur er sá sem á að fela eða endurnefna eða sleppa er hægt að gera þá breytingu beint í glugga Eiginleika sem hefur birst. Ef óskað er að raða reitir, veljið síðan **Aðlaga þessa skjámynd** í glugganum Eiginleika til að opna tækjastiku Sérsnið. Síðan er hægt að nota verkfærið Flytja til að raða reitunum.

## <a name="administration-of-personalization"></a>Stjórnun sérstillinga
Mögulegt er að sérsníða síðu og deila henni með öðrum notendum með því einfaldlega að flytja út sérsniðna síðu og biðja aðra notendur að fara á sérsniðnu síðuna og flytja sérsniðna skrána sem hefur verið stofnuð. Ef notandi hefur stjórnunarréttindi getur hann einnig stjórnað sérstillingum fyrir aðra notendur á síðunni **Uppsetning sérsniðs**. Fara á síðu b. Á síðunni **Aðlögun** sérðu tvo flipa, einn er merktur **Kerfið** og hinn ** Notendur**. 

**Kerfið:** Þetta er þar sem hægt er að afvirkja tímabundið eða „slökkva“ á öllum sérstillingum í kerfinu. Þetta eyðir ekki sérstillingunum, en endurstillir í staðinn allar skjámyndir á sjálfgildi þeirra. Seinna er hægt að endurvirkja sérsnið svo að allar sérstillingar séu aftur notaðar fyrir skjámyndir hvers notanda. Einnig er hægt að eyða öllum sérstillingum fyrir alla notendur. Athugið að þegar sérstilingum er eytt er engin leið til að endurvirkja sérstillingar sjálfvirkt úr kerfinu. Gakktu úr skugga um að þú hafir flutt út þær sérstillingar sem hægt er að flytja út síðar áður en þetta skref er framkvæmt. 

**Notendur:** Þetta er þar sem hægt er að ákveða fyrir hvern notanda hvort þeir geti framkvæmt óbein eða yfirlýst sérsnið. Þú getur einnig ákveðið hvort notendur geti framkvæmt óbein eða yfirlýst sérsnið í tiltekinni skjámynd. Að endingu, er hægt að flytja inn eða flytja út eða eyða sérsnið fyrir hvern notanda. 

**Ábending:** Í upprunalegri útgáfu leyfir stjórnun sérsniða leyfir aðeins stjórnun á grunni notanda af notanda.


