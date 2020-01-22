---
title: Yfirlit yfir fjárhagssamþættingu fyrir smásölurásir
description: Í þessu efnisatriði er að finna yfirlit yfir fjárhagssamþættingarmöguleika sem eru í boði í Dynamics 365 Retail.
author: josaw
manager: annbe
ms.date: 02/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailFunctionalityProfile, RetailFormLayout, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: v-kikozl
ms.search.validFrom: 2019-1-16
ms.dyn365.ops.version: 10
ms.openlocfilehash: 7e32f408e5c68a3422906347981c6fc4a4579daf
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915248"
---
# <a name="overview-of-fiscal-integration-for-retail-channels"></a>Yfirlit yfir fjárhagssamþættingu fyrir smásölurásir

[!include [banner](../includes/banner.md)]

## <a name="introduction"></a>Inngangur

Í þessu efnisatriði er yfirlit yfir fjárhagssamþættingarmöguleika sem eru í boði í Dynamics 365 Retail. Fjárhagssamþætting felur í sér samþættingu við ýmis fjárhagstæki og þjónustu sem gerir kleift að skrá smásölu í samræmi við staðbundin fjárhagslög sem miða að því að koma í veg fyrir skattsvik í smásöluiðnaðinum. Hér eru nokkrar dæmigerðar aðstæður sem hægt er að dekka með því að nota fjárhagssamþættingu:

- Skrá smásölu á fjárhagstæki sem tengist sölustað (POS), svo sem strimlaprentara og prentun á fjárhagskvittun fyrir viðskiptavin.
- Senda inn upplýsingar á öruggan hátt sem tengjast sölu og skilum sem er lokið í Retail POS til utanaðkomandi vefþjónustu sem er starfrækt af skattyfirvöldum.
- Hjálpar til við að tryggja stöðugleika sölufærslugagna með stafrænum undirskriftum.

Virkni fjárhagssamþættingar er rammi sem veitir algenga lausn fyrir frekari þróun og sérstillingu á samþættingunni milli Retail POS og fjárhagstæki og þjónustu. Virknin felur einnig í sér sýnishorn fjárhagssamþættingar sem styður einfaldar aðstæður smásölu fyrir tilgreind lönd eða svæði, og sem vinna með tiltekin fjárhagstæki og þjónustu. Sýnishorn fjárhagssamþættingar samanstendur af nokkrum viðbótum af Retail-íhlutum og er hluti af þróunarpakka hugbúnaðarins (SDK). Nánari upplýsingar um dæmi fjárhagssamþættingar er að finna í [Dæmi um fjárhagssamþættingu í Retail SDK](#fiscal-integration-samples-in-the-retail-sdk). Upplýsingar um hvernig skuli setja upp og nota Retail SDK er að finna í [Skipulag Retail hugbúnaðarþróunarsetts (SDK)](../dev-itpro/retail-sdk/retail-sdk-overview.md).

Til að styðja við aðrar aðstæður sem ekki eru studdar af sýnishorni fjárhagssamþættingar, til að samþætta Retail POS við önnur fjárhagstæki eða þjónustur, eða til að ná utan um kröfur annarra landa eða svæða, verður þú annaðhvort að stækka núverandi sýnishorn fjárhagssamþættingar eða stofna nýtt sýnishorn með því að nota núverandi sýnishorn sem dæmi.

## <a name="fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices"></a>Fjárhagsskráningarferli og sýnishorn fjárhagssamþættingar fyrir fjárhagstæki

Fjárhagsskráningarferli í Retail POS getur samanstaðið af einu eða fleiri skrefum. Hvert skref felur í sér fjárhagsskráningu á tilteknum smásölufærslum eða tilvikum í einu fjárhagstæki eða þjónustu. Eftirfarandi lausnaþættir taka þátt í fjárhagsskráningu í fjárhagstæki sem er tengt við vélbúnaðarstöð:

- **Commerce Runtime (CRT) viðbót** - Þessi hlutur raðar gögnum smásölufærslu/-tilviki á sniðinu sem er einnig notað í samskiptum við fjárhagstækið, þáttar svörun frá fjárhagstækinu, og geymir svörunina í gagnagrunni rásar. Viðbótin skilgreinir einnig tilgreindar færslur og tilvik sem þarf að skrá. Oft er vísað í þennan hluta sem *fjárhagsskjalsveitu*.
- **Viðbót vélbúnaðarstöðvar** - Þessi hluti frumstillir samskiptin við fjárhagstækið, sendir beiðnir og beinar skipanir til fjárhagstækis sem byggjast á gögnum smásölufærslu/-tilviks sem er sótt úr fjárhagsskjalinu, og tekur á móti svörum frá fjárhagstækinu. Oft er vísað í þennan hluta sem *fjárhagstengil*.

Sýnishorn fjárhagssamþættingar fyrir fjárhagstæki inniheldur CRT og viðbætur vélbúnaðarstöðvar fyrir fjárhagsskjalsveitu og fjárhagstengil. Það inniheldur einnig eftirfarandi stillingar hlutar:

- **Stilling fjárhagsskjalsveitu** - Þessi stilling skilgreinir úttaksaðgerð á sniði fyrir fjárhagsskjöl. Það inniheldur einnig gagnavörpun fyrir skatta og greiðslumáta, til að gera gögn frá Retail POS samhæf við gildin sem eru fyrirfram skilgreind í fastbúnaði fjárhagstækis.
- **Stilling fjárhagstengils** - Þessi stilling skilgreinir raunsamskipti við tiltekið fjárhagstæki.

Fjárhagsskráningarferli fyrir tiltekinn afgreiðslukassa er skilgreint af samsvarandi stillingu í virknireglu sölustaðar. Fyrir frekari upplýsingar um hvernig eigi að stilla fjárhagsskráningarferli skal hlaða upp skilgreiningum fjárhagsskjalsveitu og fjárhagstengils og breyta færibreytum þeirra, sjá [Setja upp fjárhagsskráningarferli](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

Í eftirfarandi dæmi er sýnt dæmigert framkvæmdaflæði fyrir fjárhagstæki. Flæðið byrjar með tilviki á sölustaðnum (til dæmis frágang á sölufærslu) og útfærir eftirfarandi skref:

1. Sölustaðurinn biður um fjárhagsskjal frá CRT.
2. CRT ákvarðar hvort núverandi tilvik krefjist fjárhagsskráningar.
3. Byggt á stillingum fjárhagsskráningarferlis, CRT ber kennsl á fjárhagstengil og samsvarandi fjárhagsskjalsveitu til að nota fyrir fjárhagsskráninguna.
4. CRT keyrir fjárhagsskjalsveitu sem býr til fjárhagsskjal (t.d. XML-skjal) sem táknar smásölufærsluna eða tilvikið.
5. Sölustaðurinn sendir fjárhagsskjalið sem CRT undirbýr til vélbúnaðarstöðvar.
6. Vélbúnaðarstöðin keyrir fjárhagstengilinn sem vinnur úr fjárhagsskjalinu og kemur því til fjárhagstækis eða þjónustu.
7. Sölustaðurinn greinir svarið frá fjárhagstækinu eða þjónustunni til að ákvarða hvort fjárhagsskráningin hafi tekist.
8. CRT vistar svarið í gagnagrunn rásar.

![Lausnarskema](media/emea-fiscal-integration-solution.png "Lausnarskema")

## <a name="error-handling"></a>Villumeðhöndlun

Þessi rammi fjárhagssamþættingar veitir eftirfarandi valmöguleika til að takast á við villur við fjárhagsskráningu:

- **Reyna aftur** - Notendur geta notað þennan valkost þegar hægt er að greiða fljótt úr villunni og fjárhagskráningin er keyrð aftur. Til dæmis er hægt að nota þennan valkost þegar fjárhagstækið er ekki tengt, strimlaprentarinn er án pappírs, eða prentarinn er stíflaður.
- **Hætta við** - Þessi valkostur heimilar notendum að fresta fjárhagsskráningu á núgildandi færslu eða tilviki ef það mistekst. Eftir að skráningunni hefur verið frestað getur notandinn haldið áfram að vinna í sölustaðnum og getur lokið öllum aðgerðum þar sem ekki þarf fjárhagsskráninguna. Þegar einhver tilvik sem krefjast fjárhagsskráningar eiga sér stað á sölustaðnum (til dæmis ef ný færsla er opnuð) birtist villuglugginn sjálfkrafa til að tilkynna notanda að fyrri færsla hafi ekki verið skráð rétt og býður upp á valmöguleika til að meðhöndla villuna.
- **Sleppa** - Notendur geta notað þennan valkost þegar hægt er að sleppa fjárhagsskráningunni við sérstakar kringumstæður og hægt er að halda áfram með reglubundnar aðgerðir á sölustaðnum. Til dæmis er hægt að nota þennan valmöguleika þegar hægt er að skrá sölufærslu sem fjárhagsskráningin mistókst fyrir í sérstakri færslubók á pappír.
- **Merkja sem skráð** - Notendur geta notað þennan valkost þegar færslan var í raun skráð í fjárhagstækinu (t.d. fjárhagskvittun var prentuð), en villa kom upp þegar verið var að vista fjárhagssvörunin í gagnagrunn rásarinnar.

> [!NOTE]
> Valkostirnir **Sleppa** og **Merkja sem skráð** verða að vera gerðir virkir í fjárhagsskráningarferlinu áður en þeir eru notaðir. Að auki skulu samsvarandi heimildir veittar notendum.

Valkostirnir **Sleppa** og **Merkja sem skráð** virkja upplýsingakóða til að sækja tilteknar upplýsingar um villuna, t.d. að ástæða villunnar eða rökstuðningur fyrir því að sleppa fjárhagsskráningunni eða merkja færsluna sem skráða. Nánari upplýsingar um hvernig á að setja upp færibreytur fyrir meðhöndlun á villu er að finna í [Stilla villumeðhöndlunarstillingar](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

### <a name="optional-fiscal-registration"></a>Valfrjáls fjárhagsskráning

Fjárhagsskráning kann að vera áskilin fyrir sumar aðgerðir en valfrjáls fyrir aðrar. Til dæmis gæti fjárhagsskráning á reglulegum sömum og skilum verið áskilin, en fjárhagsskráning á aðgerðum sem tengjast innborgun viðskiptavinar kann að vera valfrjáls. Ef svo er ætti að lokast fyrir frekari sölur ef ekki tekst að ljúka fjárhagsskráningu á sölu, en ef ekki tekst að ljúka fjárhagsskráningu á innborgun viðskiptavinar ætti það ekki að loka fyrri frekari sölur. Til að greina á milli áskilina og valfrjálsra aðgerða ráðleggjum við að þú meðhöndlir þær í gegnum mismunandi skjalaveitur og að þú setjir upp aðskilin skref í ferli fjárhagsskráningar fyrir þessar veitur. Virkja skal færibreytuna **Halda áfram á villu** fyrir öll skref sem tengjast valfrjálsri fjárhagsskráningu. Nánari upplýsingar um hvernig á að setja upp færibreytur fyrir meðhöndlun á villu er að finna í [Stilla villumeðhöndlunarstillingar](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

### <a name="manually-running-fiscal-registration"></a>Handvirk keyrsla á fjárhagsskráningu

Ef fjárhagsskráningu á færslu eða tilviki hefur verið frestað eftir bilun (til dæmis ef notandi valdi **Hætta við** í svarglugga villumeðhöndlunar), er hægt að keyra fjárhagsskráninguna aftur handvirkt með því að kalla fram samsvarandi aðgerð. Frekari upplýsingar er að finna í [Virkja handvirka keyrslu á frestaðri fjárhagsskráningu](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).

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
> Ástandsskoðun er einungis keyrð ef núverandi aðgerð krefst fjárhagsskráningar og ef slökkt er á færibreytunni **Halda áfram á villu** fyrir núverandi skref í ferli fjárhagsskráningar. Frekari upplýsingar er að finna í [Velja stillingar villumeðhöndlunar](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

## <a name="storing-fiscal-response-in-fiscal-transaction"></a>Geymsla á fjárhagssvörum í fjárhagsfærslu

Þegar fjárhagsskráning færslu eða tilviks heppnast er stofnuð fjárhagsfærsla í gagnagrunni rásarinnar og hún tengd við upprunalega færslu eða tilvik. Á svipaðan hátt, ef valkosturinn **Sleppa** eða **Merkja sem skráð** er valinn fyrir misheppnaða fjárhagsskráningu, eru þessar upplýsingar geymdar í fjárhagsfærslu. Fjárhagsfærsla heldur í fjárhagssvörun fjárhagstækis eða þjónustu. Ef fjárhagsskráningarferlið samanstendur af nokkrum skrefum er fjárhagsfærsla stofnuð fyrir hvert skref ferlisins sem leiddi til skráningu sem tókst eða mistókst.

Fjárhagsfærslur eru fluttar til Retail Headquarters með *P-vinnslu* ásamt smásölufærslum. Í flýtiflipanum **Fjárhagsfærslur** á síðunni **Færslur smásöluverslunar** er hægt að skoða fjárhagsfærslurnar sem eru tengdar við smásölufærslur.

Fjárhagsfærsla geymir eftirfarandi upplýsingar:

- Upplýsingar um ferli fjárhagsskráningar (ferli, tenglahóp, tengil og svo framvegis). Hún geymir einnig raðnúmer fjárhagstækis í reitnum **Skrá númer** ef þessar upplýsingar eru innifaldar í fjárhagssvörun.
- Staða fjárhagsskráningar: **Lokið** fyrir heppnaða skráningu, **Sleppt** ef notandinn valdi vakostinn **Sleppa** fyrir skráningu sem mistókst, eða **Merkt sem skráð** ef notandinn valdi valkostinn **Merkja sem skráð**.
- Færslur upplýsingakóða sem tengjast valdri fjárhagsfærslu. Til að skoða færslur upplýsingakóða í flýtiflipanum **Fjárhagsfærslur** skal velja fjárhagsfærslu sem er með stöðuna **Sleppt** eða **Merkt sem skráð** og síðan velja **Færslur upplýsingakóða**.

## <a name="fiscal-texts-for-discounts"></a>Fjárhagstextar fyrir afslætti

Sum lönd eða svæði gera sérstakar kröfur um viðbótartexta sem þarf að prenta á fjárhagskvittanir þegar mismunandi afslættir eru notaðir. Virknin fyrir fjárhagssamþættingu gerir þér kleift að setja upp sérstakan texta fyrir afslátt sem prentast á eftir afsláttarlínu á fjárhagskvittun. Fyrir handvirka afslætti er hægt að stilla fjárhagstexta fyrir upplýsingakóðann sem er tilgreindur sem upplýsingakóðinn **Afurðarafsláttur** í virknireglu sölustaðar. Nánari upplýsingar um hvernig á að setja upp fjárhagstexta fyrir afslætti er að finna í [Uppsetning fjárhagstexta fyrir afslætti](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-texts-for-discounts).

## <a name="printing-fiscal-x-and-fiscal-z-reports"></a>Prenta X- og Z-skýrslur fjárhags

Virknin fyrir fjárhagssamþættingu styður myndun á uppgjör í lok dags sem miðast við samþætta fjárhagstækið eða þjónustuna:

- Bæta ætti nýjum hnöppum sem keyra samsvarandi aðgerðir við skjáútlit POS. Nánari upplýsingar er að finna í [Setja upp X/Z-skýrslur fjárhags úr POS](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-xz-reports-from-the-pos).
- Í sýnishorni fjárhagssamþættingar ætti að samsvara þessar aðgerðir við samsvarandi aðgerðir í fjárhagstækinu.

## <a name="fiscal-integration-samples-in-the-retail-sdk"></a>Sýnishorn fjárhagssamþættingar í Retail SDK

Eftirfarandi sýnishorn fjárhagssamþættingar eru eins og er í boði í Retail SDK:

- [Dæmi um samþættingu strimlaprentara fyrir Ítalíu](emea-ita-fpi-sample.md)
- [Dæmi um samþættingu strimlaprentara fyrir Pólland](emea-pol-fpi-sample.md)
- [Dæmi um samþættingu þjónustu fjárhagsskráningar fyrir Austurríki](emea-aut-fi-sample.md)
- [Dæmi um samþættingu þjónustu fjárhagsskráningar fyrir Tékkland](emea-cze-fi-sample.md)
- [Dæmi um samþættingu stjórntækis fyrir Svíþjóð](./emea-swe-fi-sample.md)

Eftirfarandi virkni fjárhagssamþættingar er einnig í boði í Retail SDK en hún nýtir sér ekki ramma fjárhagssamþættingar eins og er. Flutningur á þessari virkni í ramma fjárhagssamþættingar er á dagskrá í seinni útgáfum.


- [Stafræn undirskrift fyrir Frakkland](emea-fra-cash-registers.md)
- [Stafræn undirskrift fyrir Noreg](emea-nor-cash-registers.md)

Eftirfarandi eldri virkni fjárhagssamþættingar sem er fáanleg í Retail SDK notar ekki ramma fjárhagssamþættingar og verður úrelt í síðari uppfærslum:

- [Dæmi um samþættingu stjórntækja fyrir Svíþjóð (eldra)](./retail-sdk-control-unit-sample.md)
