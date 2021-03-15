---
title: Viðbætur cXML-innkaupa
description: Eiginleikinn fyrir viðbætur cXML-innkaupa byggir á fyrirliggjandi virkni ytri vörulista, PunchOut, sem er notaður fyrir innkaupabeiðnir.
author: dasani-madipalli
manager: tfehr
ms.date: 08/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatCXMLParameters, CatCXMLPurchRequest
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-08-03
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 3113202b1f38bc528733c980321d60bb9ad23dde
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992196"
---
# <a name="purchasing-cxml-enhancements"></a>Viðbætur cXML-innkaupa

[!include [banner](../includes/banner.md)]

Eiginleikinn _Viðbætur cXML-innkaupa_ byggir á [fyrirliggjandi virkni ytri vörulista](set-up-external-catalog-for-punchout.md) sem er notaður fyrir innkaupabeiðnir. Þessi fyrirliggjandi virkni er þekkt sem _PunchOut_. Þrátt fyrir að innkaupapöntun þurfi ekki að eiga uppruna sinn í innkaupabeiðni, verður að vera tenging á milli lánardrottins á innkaupapöntun og færibreytanna sem eru notaðar til að senda skjal innkaupapöntunar.

## <a name="turn-on-the-purchasing-cxml-enhancements-feature"></a>Kveikja á eiginleikanum fyrir viðbætur cXML-innkaupa

Til að kveikja á eiginleikanum skal opna **[Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** og leita að eiginleikanum sem er nefndur *Viðbætur cXML-innkaupa*. Veljið eiginleikann og veljið svo **Virkja núna** til að kveikja á honum.

Eftir að kveikt er á eiginleikann ætti að skilgreina stillingar á eftirfarandi þremur svæðum:

- **[cXML-færibreytur](#cxml-parameters)** – Notið þessar stillingar til að setja upp nokkrar altækar færibreytur fyrir virknina til að senda innkaupapantanir.
- **[Uppsetning lánardrottins](#vendor-setup)** – Ef nota á cXML sjálfkrafa fyrir allar nýjar innkaupapantanir sem einhver lánardrottin stofnar, skal stilla valkostinn **Senda innkaupapöntun með cXML** á _Já_ fyrir þann lánardrottin.
- **[Ytri vörulistar](#external-catalog-setup)** – Notið nýju stillingarnar **Eiginleikar pöntunar** til að skilgreina snið innkaupapöntunarskjalsins og hvernig það er sent.

Eftirfarandi mynd tekur saman þessa skilgreiningu.

![Svæði til að setja upp cXML-eiginleika](media/cxml-settings-areas.png "Svæði til að setja upp cXML-eiginleika")

Að auki þarf að setja upp [Runuvinnslu innkaupapöntunarbeiðni](#po-batch). Þessi runuvinnsla er notuð til að senda staðfestar innkaupapantanir.

## <a name="set-up-global-cxml-parameters"></a><a name="cxml-parameters"></a>Setja upp altækar cXML-færibreytur

Notið síðuna **cXML-færibreytur** til að gera nokkrar altækar stillingar sem eiga við um virknina til að senda innkaupapantanir.

![cXML-færibreytusíða](media/cxml-parameters.png "cXML-færibreytusíða")

Farið í **Innkaup og aðföng \> Uppsetning \> Stjórnun cXML \> cXML-færibreytur** og stillið eftirfarandi færibreytur:

- **cXML prófunarstilling** - Þessi altæka færibreyta hefur áhrif á hvernig innkaupapantanir eru efnislega sendar úr runuvinnslunni. Veljið eitt af eftirfarandi gildum:

    - **Próf** – Í þessari stillingu getur runuvinnslan verið í gangi og XML-skjalið fyrir skilaboðin er myndað, en það er ekki sent. Þess í stað er það vistað í beiðni innkaupapöntunar svo hægt sé að yfirfara það. Þessi stilling er gagnleg þegar þú ert í upphaflegri innleiðingu og þú vilt sjá hvernig gögn eru færð inn í cXML-skilaboðin. Einnig gætir þú viljað búa til sýnishorn af skilaboðum sem hægt er að senda lánardrottnum fyrir fyrstu staðfestingu.
    - **Lifandi** – Í þessari stillingu notar eiginleikinn [stillingar ytri vörulista](#external-catalog-setup) til að senda hvert skjal efnislega til lánardrottins.

- **Senda uppfærslur á innkaupabeiðni** – Stillið þennan valkost á *Já* til að senda uppfærsluskilaboð fyrir innkaupapantanir. Stillið hann á *Nei* til að koma í veg fyrir að skilaboðin séu send. Flestir lánardrottnar kjósa að fá ekki skilaboð um uppfærslu. Þess í stað krefjast þeir þess að viðskiptavinir hafi samband við þá símleiðis eða í tölvupósti ef breyta á innkaupapöntun. Þessi færibreyta er altæk færibreyta og ekki er hægt að tilgreina neina hnekkingu á ytri vörulista hvers lánardrottins. Innkaupapöntun verður merkt sem uppfærð ef önnur staðfesting er bókuð á innkaupapöntun, en fyrsta staðfestingin hefur þegar verið send og viðurkennd af lánardrottni. Ef um er að ræða aðra staðfestingu en fyrsta staðfestingin hefur ekki verið send, verður önnur staðfestingin meðhöndluð sem nýtt skjal. Hægt er að staðfesta innkaupapöntun mörgum sinnum þar til ein staðfesting er send. Næsta staðfesting verður síðan meðhöndluð sem uppfærsluskilaboð.
- **Senda eyðingu á innkaupabeiðni** – Stillið þennan valkost á *Já* til að senda skilaboð um eyðingu fyrir innkaupapantanir. Stillið hann á *Nei* til að koma í veg fyrir að skilaboðin séu send. Flestir lánardrottnar kjósa að fá ekki skilaboð um eyðingu. Þess í stað krefjast þeir þess að viðskiptavinir hafi samband við þá símleiðis eða í tölvupósti ef innkaupapöntun var send fyrir mistök. Þessi færibreyta er altæk færibreyta og ekki er hægt að tilgreina neina hnekkingu á ytri vörulista hvers lánardrottins. Innkaupapöntun verður merkt sem eydd ef hætt er við innkaupapöntunina í Supply Chain Management.
- **Safnvista skrá** – Tilgreinið skráarslóð þar sem á að flytja út og vista safnvistuð cXML-skjöl. Slóðin er notuð þegar hreinsunarvirknin er keyrð af síðunni **Beiðni innkaupapöntunar**.
- **Hámarksfjöldi stafa fyrir línu götuheitis** – Sláið inn hámarksfjölda stafa sem hægt er að nota í reit götuheitis fyrir aðsetur í cXML-skjalinu. Þessi altæka færibreyta hefur áhrif á alla lánardrottna nema hnekking sé tilgreind í eiginleikum ytri vörulista.

## <a name="set-up-vendor-purchase-orders-to-use-cxml"></a><a name="vendor-setup"></a>Setja upp innkaupapantanir lánardrottins til að nota cXML

Í hvert sinn sem sölupöntun er staðfest þar sem valkosturinn **Senda innkaupapöntun með cXML** er stilltur á _Já_ býr kerfið sjálfkrafa til cXML-skilaboð og sendir á lánardrottin sem tengist innkaupapöntuninni. Til eru tvær leiðir til að stýra þessum valkosti fyrir innkaupapantanir:

- Til að setja upp lánardrottin þannig að hann noti sjálfkrafa cXML fyrir allar nýjar innkaupapantanir sem búnar eru til úr beiðni, skal fara í **Innkaup og aðföng \> Lánardrottnar \> Allir lánardrottnar** og velja eða stofna lánardrottin til að opna upplýsingasíðu hans. Síðan, í flýtiflipanum **Sjálfgildi innkaupapöntunar**, skal stilla valkostinn **Senda innkaupapöntun með cXML** á _Já_. Ef cXML á einnig sjálfkrafa að nota fyrir nýjar innkaupapantanir sem eru **ekki** stofnaðar út frá beiðni, þarf einnig að stilla pöntunareiginleikann **ENABLEMANUALPO** á _Satt_ fyrir tengdan ytri vörulista, eins og lýst er í hlutanum [Stilla eiginleika pöntunar](#set-order-properties) síðar í þessu efnisatriði.
- Fyrir stakar innkaupapantanir skal fara í **Innkaup og aðföng \> Innkaupapantanir \> Allar innkaupapantanir** og velja eða stofna innkaupapöntun til að opna upplýsingasíðu hennar. Skiptið yfir í yfirlitið **Haus** og síðan, í flýtiflipanum **Uppsetning**, skal stilla valkostinn **Senda innkaupapöntun með cXML** eftir þörfum.

![Sjálfgefnar stillingar fyrir innkaupapantanir lánardrottins](media/cxml-order-defaults.png "Sjálfgefnar stillingar fyrir innkaupapantanir lánardrottins")

## <a name="set-up-an-external-catalog-to-use-cxml"></a><a name="external-catalog-setup"></a>Setja upp ytri vörulista til að nota cXML

Á síðunni **Ytri vörulistar**, fyrir hvern vörulista, er hægt að setja upp PunchOut-virknina og virkni til að senda innkaupapantanir. Til að finna viðeigandi stillingar skal fara í **Innkaup og aðföng \> Vörulistar \> Ytri vörulistar**. Byrjið á því að [setja upp hvern vörulista eins og venjulega](set-up-external-catalog-for-punchout.md). Þetta ferli felur í sér að úthluta lánardrottni, velja flokkana sem lánardrottinn hefur heimild til að veita og virkja vörulistann. Skilgreinið svo fleiri stillingar sem lýst er í þessum hluta.

> [!NOTE]
> Þegar innkaupapöntun er staðfest sem hægt er að senda með cXML, flettir kerfið upp á lánardrottninum sem tengist innkaupapöntuninni og finnur svo fyrsta virka ytri vörulistann sem tengist þessum lánardrottni. Kerfið notar svo stillingarnar úr þessum ytri vörulista til að senda innkaupapöntunina. Ef margir ytri vörulistar eru settir upp notar kerfið aðeins fyrsta ytri vörulistann sem það finnur, sem byggir á lánardrottni í innkaupapöntuninni. Þess vegna er mælt með því að stofna aðeins einn ytri vörulista fyrir hvern lánardrottin.

![Stillingar ytri vörulista](media/cxml-supplier-catalog.png "Stillingar ytri vörulista")

### <a name="set-the-punchout-protocol-type"></a>Stilla gerð PunchOut-samskiptareglu

Í flýtiflipanum **Almennt** á síðunni **Ytri vörulistar** skal stilla reitinn **Gerð PunchOut-samskiptareglu** á _cXML_. Þessi valkostur verður eini tiltæki valkosturinn, nema samstarfsaðili hafi stækkað virknina og látið aukalegan valkost fylgja stækkuninni.

Ef þú ert einnig að nota vörulistann fyrir PunchOut, þarf einnig að [setja upp snið skilaboða](set-up-external-catalog-for-punchout.md). Snið skilaboðsins er notað til að koma á tengingu við lánardrottin í PunchOut-færslunni úr beiðninni. Þegar innkaupapöntun er send verða eiginleikar pöntunar notaðir til að koma á tengingu við lánardrottin.

### <a name="set-the-order-properties"></a><a name="set-order-properties"></a>Stilla eiginleika pöntunar

Eiginleikinn _cXML-viðbætur keyptar_ bætir við nýjum **Eiginleikar pöntunar** flýtiflipa fyrir ytri vörulista. Þessi flýtiflipi býður upp á hnitanet þar sem hægt er að skilgreina pöntunareiginleika. Þar er einnig að finna tækjastiku. Þessi tækjastika inniheldur eftirtalda þrjá hnappa sem hægt er að nota til að stjórna pöntunareiginleikunum:

- **Sjálfgefnir eiginleikar** – Þegar verið er að setja upp nýjan vörulista skal velja þennan hnapp til að bæta fyrirframskilgreindu safni af algengum eiginleikum við hnitanetið.
- **Nýr** – Bæta nýjum eiginleika við hnitanetið.
- **Eyða** – Eyða völdum eiginleika úr hnitanetinu. Ef sjálfgefnum eiginleika er óvart eytt skal velja **Sjálfgefnir eiginleikar** til að endurheimta alla eiginleikana sem vantar.

Í hvert skipti sem einum eða fleiri eiginleikum er bætt við hnitanetið skal nota hægri dálkinn til að tilgreina gildi fyrir hvern þeirra.

Notið sjálfgefna eiginleika á eftirfarandi hátt:

- **KAUPANDI\_KAKA** – Þennan rakningarreit er hægt að nota til að tilgreina ákveðnar upplýsingar fyrir fyrirtækið. Ef þú hefur ekki gert samning við lánardrottin um hvernig þessi eiginleiki er notaður, hefur hann litla þýðingu þegar innkaupapöntun er send. Þess vegna ætti að stilla hann á einfalt gildi.
- **SENDATIL** – Þegar heimilisfang viðtakanda er fært inn í skjalið úr innkaupapöntuninni, er reiturinn **Mikilvægar upplýsingar** notaður til að stilla reitinn **SendaTil** í XML-skilaboðunum. Ef krafist er þess að þetta gildi sé nafn umsóknaraðila og reitur umsóknaraðila verður stilltur í haus innkaupapöntunar, skal færa inn gildið _UMSÓKNARAÐILI_ fyrir þennan eiginleika, þannig að nafn umsóknaraðila verði fært inn í reitinn **SendaTil** í XML. Í þessu tilfelli verða aðalnetfang og símanúmer, sem notuð eru, frá umsóknaraðila í stað pöntunaraðila.
- **UPPSETNINGARSTILLING** – Stillið þennan eiginleika eins og krafist er af lánardrottni. Gildin eru yfirleitt _FRAMLEIÐSLA_ eða _PRÓF_. Stillið gildið á grundvelli samskipta við lánardrottin. Oftast verður það að samsvara fyrirhuguðu kerfi fyrir aftan gildið **ORDERCHECKURL** sem lánardrottinn gefur upp sem prófunar- eða framleiðslukerfi.
- **FIXEDBILLADDRESSID** – Þegar reiturinn **addressID** í XML-skilaboðum er stilltur, þá nær hann í staðsetninguna sem er tilgreind í aðsetrinu. Ef gildi auðkennisins sem hefur verið miðlað til lánardrottins er frábrugðið gildinu í staðsetningu aðseturs af einhverri ástæðu, er hægt að þvinga hnekkingu með því að tilgreina gildið hér. Forsenda þess er að aðeins sé notað eitt aðsetur með lánardrottni og að aðsetrið sé uppsett í kerfi lánardrottins. Reikningsaðsetrið er það aðalreikningsaðsetrið sem tilgreint er fyrir lögaðilann í Supply Chain Management.
- **FIXEDSHIPADDRESSID** – Þegar reiturinn **addressID** í XML-skilaboðum er stilltur, þá nær hann í staðsetninguna sem er tilgreind í aðsetrinu. Ef gildi auðkennisins sem hefur verið miðlað til lánardrottins er frábrugðið gildinu í staðsetningu aðseturs af einhverri ástæðu, er hægt að þvinga hnekkingu með því að tilgreina gildið hér. Forsenda þess er að aðeins sé notað eitt aðsetur með lánardrottni og að aðsetrið sé uppsett í kerfi lánardrottins. Sendingaraðsetrið er aðsetrið sem tilgreint er í haus innkaupapöntunarinnar. Flestir lánardrottnar taka aðeins við aðsetrum í haus, ekki í línum. Þrátt fyrir að það séu reitir fyrir aðseturslínur í XML, verða þau sett í aðsetur í haus.
- **FRÁ\_LÉN** – Sláið inn gildið sem er notað til að senda skjöl innkaupapöntunar. Lánardrottinn gefur upp þetta gildi.
- **FRÁ\_AUÐKENNI** – Sláið inn gildið sem er notað til að senda skjöl innkaupapöntunar. Lánardrottinn gefur upp þetta gildi.
- **ORDERCHECKURL** – Færið inn vefslóðina sem senda á skjöld innkaupapöntunar á. Þessi vefslóð hefst á `https://` og lánardrottinn gefur hana upp.
- **FARMUR\_KENNI** – Sláið inn gildi forskeytis fyrir farmkenni, eins og þörf er á fyrir viðskiptaferlana sem eru til staðar fyrir núverandi lánardrottin.
- **SENDANDI\_LÉN** – Sláið inn gildið sem er notað til að senda skjöl innkaupapantana. Lánardrottinn gefur upp þetta gildi.
- **SENDANDI\_AUÐKENNI** – Sláið inn gildið sem er notað til að senda skjöl innkaupapantana. Lánardrottinn gefur upp þetta gildi.
- **SAMNÝTT\_LEYNILYKILL** – Sláið inn gildið sem er notað til að senda skjöl innkaupapantana. Lánardrottinn gefur upp þetta gildi.
- **LENGDGÖTUHEITIS** – Færið inn tölu sem stendur fyrir hámarksfjölda stafa sem lánardrottinn samþykkir sem götuheiti. Ef gildi er fært inn hér, hnekkir það gildinu sem er tilgreint á síðunni **cXML-færibreytur**. Kerfið mun fjarlægja línuskil og bil til að reyna að koma hefðbundna aðsetrinu í Supply Chain Management innan stafafjöldans sem er tilgreindur hér. Allir umframstöfum verður sleppt.
- **TIL\_LÉN** – Sláið inn gildið sem er notað til að senda skjöl innkaupapantana. Lánardrottinn gefur upp þetta gildi.
- **TIL\_AUÐKENNI** – Sláið inn gildið sem er notað til að senda skjöl innkaupapantana. Lánardrottinn gefur upp þetta gildi.
- **USERAGENT** – Færið inn gildi til að auðkenna kerfið sem er notað. Til dæmis: Færið inn _Dynamics 365 Supply Chain Management_.
- **ÚTGÁFA** – Færið inn cXML-útgáfunúmer ef lánardrottinn biður um þessar upplýsingar. Sjálfgefna útgáfan er *1.2.008*. Þessi útgáfa er stöðug og er samþykkt af flestum lánardrottnum.
- **RESPONSETEXT** – Færið inn einhvern sérsniðinn texta sem búist er við að lánardrottinn skili í cXML-svarskilaboði eftir að pöntunin hefur verið send. Á þennan hátt getur kerfið merkt skilaboðin sem _Samþykkt_. Ef svarið stemmir ekki við staðlaðan texta eða texta viðskiptavinarins sem færður er inn hér, verður beiðnin merkt sem _Villa_.
- **RESPONSETEXTSUB** – Stillið þennan eiginleika á _SATT_ ef óskað er eftir að leita í svartexta lánardrottins að gildunum sem eru tilgreind í reitnum **RESPONSETEXT**. Til dæmis gæti lánardrottinn skilað löngum streng sem inniheldur „Í lagi“ í svarinu. Í þessu tilfelli er hægt að slá inn _Í lagi_ í reitinn **RESPONSETEXT** og stilla **RESPONSETEXTSUB** á _SATT_ til að leita að „Í lagi“ hvar sem er í svarinu. Svo er hægt að stilla pöntunina á _Samþykkt_.
- **CONTENTTYPE** – Í dæmigerðri uppsetningu vörulista þarf ekki að stilla þennan eiginleika. Ef netþjónsvilla 500 kemur upp í kerfi lánardrottins þegar innkaupapöntun er send, er hægt að gera prófanir með því að stilla þennan eiginleika á _ÓSATT_. Þetta gildi mun breyta stillingu í vefbeiðninni og hugsanlega gera að verkum að skilaboðin verði send á nokkra verkvanga.
- **ENABLEHEADERS** – Stillið þennan eiginleika á _SATT_ til að senda hausa saman með innkaupapöntuninni. Aðeins þarf að stilla þennan eiginleika ef lánardrottinn krefst þess. Ef þessi eiginleiki er stilltur á _SATT_ skal bæta við aukalegum sérstilltum eiginleikum sem eru byggðir á heitunum sem lánardrottinn býður upp á og bæta við forskeytinu _H\__. Dæmigerð dæmi eru **H\_USERID**, **H\_PASSWORD**, **H\_RECEIVERID** og **H\_ACTIONREQUEST**. Eftirfarandi sérstilltir eiginleikar eru teknir með í sjálfgefnum eiginleikum:

    - **H\_USERID** – Ef viðskiptafélaginn krefst þess að notandakenni sé sent sem hluti af vefslóðinni til að senda inn innkaupapöntun, skal slá gildið inn hér.
    - **H\_PASSWORD** – Ef viðskiptafélaginn krefst þess að aðgangsorð sé sent sem hluti af vefslóðinni til að senda inn innkaupapöntun, skal slá gildið inn hér.

- **ENABLEMANUALPO** – Ef þessi eiginleiki er stilltur á _SATT_, þegar notendur búa til innkaupapantanir handvirkt (þ.e. þegar þeir byrja ekki á beiðni) munu þessar innkaupapantanir erfa stillingu á valkostinum **Senda innkaupapöntun með cXML** frá lánardrottninum. Ef þessi eiginleiki er ekki stilltur eða ef hann er stilltur á _ÓSATT_, verður valkosturinn **Senda innkaupapöntun með cXML** ekki stilltur á haus innkaupapöntunar til að stofna innkaupapantanir handvirkt. Fyrir innkaupapantanir sem búnar eru til úr beiðni er stillingin á valkostinum **Senda innkaupapöntun með cXML** alltaf erfð frá lánardrottni, óháð því hvaða stilling er á þessum eiginleika. Frekari upplýsingar er að finna í hlutanum [Setja upp innkaupapantanir lánardrottins til að nota cXML](#vendor-setup) fyrr í þessu efnisatriði.
- **PUNCHOUTPOONLY** – Ef þessi eiginleiki er stilltur á _SATT_ verða aðeins innkaupabeiðnilínur sem stofnaðar eru úr PunchOut-ferlinu stilltar á valkostinn **Senda innkaupapöntun með cXML** í haus innkaupapöntunar. Að auki verður gerð innkaupabeiðnilínunnar fyrir allar línur í innkaupapöntuninni að vera _Ytra vörulistaatriði_. Að öðrum kosti er ekki hægt að stofna cXML-innkaupapöntun.
- **PUNCHOUTSHIPTO** – Ef þessi eiginleiki er stilltur á _SATT_, verður sjálfgefna aðsetrinu fyrir lögaðila bætt við beiðniskilaboð PunchOut-uppsetningar þegar notandi opnar ytri vörulista. Þessu aðsetri er bætt við sem **SendaTil** aðsetur. Lánardrottnar munu nota **SendaTil** aðsetrið til að sýna verðlagningu sem byggir á staðsetningu fyrirtækisins.
- **TRACEPUNCHOUT** – Stillið þennan eiginleika á _SATT_ ef villuskilaboð birtast þegar reynt er að fletta að ytri vörulista úr beiðninni. Rakningarupplýsingar verða þá fylltar út fyrir **PunchOutSetupRequest** og **PunchOutResponse** skilaboðin sem eru send á milli Supply Chain Management og svæðis lánardrottins. Hægt er að skoða þessar upplýsingar á síðunni **Skilaboðakladdi cXML-körfu**, sem hægt er að opna á síðunni **Uppsetning ytri vörulista** fyrir vörulista lánardrottins þar sem vandamál er til staðar. Þú ættir aðeins að stilla þennan eiginleika á _SATT_ ef þú ert að úrræðaleita vegna þess að hvert PunchOut setur mikið álag á gagnagrunninn. Frekari upplýsingar er að finna í hlutanum [Skoða skilaboðakladda cXML-körfu fyrir PunchOut ytri vörulista](#message-log) síðar í þessu efnisatriði.
- **REPLACENEWLINE** – Stillið þennan eiginleika á _SATT_ ef um er að ræða vandamál vegna þess að lánardrottnakerfi er að senda **PunchOutResponse** skilaboð sem innihalda stafi sem standa fyrir nýja línu (\\n). Þetta vandamál kann að koma upp ef skilaboð lánardrottins eru þáttuð í gegnum miðstöð millibúnaðar eða innkaupa. Ef vandamál kom upp varðandi uppsetningu á nýjum lánardrottni skal stilla **TRACEPUNCHOUT** eiginleikann á _SATT_ til að skoða **PunchOutResponse** skilaboðin og ákveða hvort XML-merkin eru brotin upp með stöfum sem tákna nýja línu.
- **POCOMMENTS** – Stillið þennan eiginleika á _SATT_ ef cXML-skjalið á að taka með athugasemdir sem eru hengdar við innkaupapöntunina í Supply Chain Management. Texti viðhengis er tekinn með í athugasemdum í hausnum í skilaboðum innkaupapöntunarinnar. Frekari upplýsingar um hvernig kerfið velur og vinnur úr þessum viðhengjum er að finna í hlutanum [Hengja athugasemdir við innkaupapöntun](#attach-po-notes) seinna í þessu efnisatriði.
- **VENDCOMMENTS** – Stillið þennan eiginleika á _SATT_ ef cXML-skjalið á að taka með athugasemdir sem eru hengdar við innkaupapöntunina í Supply Chain Management. Texti viðhengis er tekinn með í athugasemdum í hausnum í skilaboðum innkaupapöntunarinnar. Frekari upplýsingar um hvernig kerfið velur og vinnur úr þessum viðhengjum er að finna í hlutanum [Hengja athugasemdir við innkaupapöntun](#attach-po-notes).
- **CLEANAMP** – Stillið þennan eiginleika á _SATT_ ef villuboð berast þegar reynt er að gera PuncOut á lánardrottin og að skilavefslóð lánardrottins felur í sér rangt kóðuð og-merki (\&).
- **PUNCHOUTTZ** – Stillið þennan eiginleika á _SATT_ ef lánardrottin sem verið er að vinna með notar staðalinn ISO 8601 til að gera sérstaka sannvottun á dagsetningu/tíma á skilaboðum útskráningarbeiðni. Supply Chain Management notar samræmdan heimstíma (UTC) í **PunchOutSetupRequest** skilaboðunum. Þess vegna þegar þessi eiginleiki er stilltur á _SATT_ er *+00:00* bætt við dagsetningar-/tímasniðið.
- **WMSADDRESSID** – Stillið þennan eiginleika á _SATT_ til að nota númer vöruhúss í haus innkaupapöntunarinnar sem gildið fyrir **addressID** í **SendaTil** aðsetrinu fyrir beiðni innkaupapöntunar sem er send til lánardrottins. Ef gildið er stillt fyrir **FIXEDSHIPADDRESSID** eiginleikann, hefur gildið forgang fram yfir þetta gildi. Þess vegna ætti að nota einn eiginleika eða annan til að stilla gildið fyrir **addressID** í **SendaTil** aðsetrinu fyrir skjalið.
- **PUNCHOUTSHIPTOUSER** – Þessi eiginleiki vinnur saman með **PUNCHOUTSHIPTO** eiginleikanum. Ef **PUNCHOUTSHIPTO** er stillt á _SATT_ er náð í aðsetur lögaðilans. Ef **PUNCHOUTSHIPTOUSER** er stillt á _SATT_ er aðalaðsetrið frá PunchOut-notandanum notað í staðinn fyrir aðsetur lögaðilans.

### <a name="activate-the-external-catalog"></a>Virkja ytri vörulista

Þegar búið er að setja upp alla eiginleika og skilgreina aðrar stillingar fyrir ytri vörulistann, skal fara aftur í flýtiflipann **Almennt** á síðunni **Ytri vörulistar** og stilla valkostinn **Virkur** á *Já*.

### <a name="attach-notes-to-a-purchase-order"></a><a name="attach-po-notes"></a>Bæta athugasemdum við innkaupapöntun

Eins og var getið um í hlutanum [Stilla eiginleika pöntunar](#set-order-properties), ef ætlunin er að afhent cXML innihaldi texta úr athugasemdum sem eru hengdar við viðeigandi innkaupapöntun og/eða lánardrottnafærslur, er hægt að stilla eiginleikan **POCOMMENTS** og/eða **VENDCOMMENTS** á _SATT_ í uppsetningu vörulista. Þessi hluti veitir nánari upplýsingar um hvernig kerfið velur og vinnur úr þessum viðhengjum, ef þau eru notuð.

Til að stilla þær gerðir af athugasemdum sem kerfið leitar að, skal fara í **Innkaup og aðföng \> Uppsetning \> Skjámyndir \> Frá uppsetningu**. Síðan, í flipanum **Innkaupapöntun**, skal stilla reitinn **Taka með skjöl af gerðinni** á gerð athugasemdar sem þú vilt að verði tekin með. Aðeins athugasemdir á textaformi verða teknar með, ekki viðhengi skjala.

![Uppsetningarsíða skjámyndar](media/cxml-form-setup.png "Uppsetningarsíða skjámyndar")

Viðhengi fylgja aðeins með innkaupapöntun ef reiturinn **Gerð** er stilltur á gildið sem var valið í reitnum **Taka með skjöl af gerðinni** og ef reiturinn **Takmörkun** er stilltur á _Ytri_. Til að búa til, skoða eða breyta viðhengjum fyrir innkaupapöntun skal fara í **Innkaup og aðföng \> Allar innkaupapantanir**, velja eða stofna innkaupapöntun og síðan velja hnappinn **Viðhengi** (bréfaklemmutákn) efst í hægra horninu.

![Viðhengd athugasemd sem er sett upp til að vera send til lánardrottins](media/cxml-note-to-vendor.png "Viðhengd athugasemd sem er sett upp til að vera send til lánardrottins")

## <a name="view-the-cxml-cart-message-log-for-external-catalog-punchout"></a><a name="message-log"></a>Skoða skilaboðakladda cXML-körfu fyrir PunchOut ytri vörulista

Þegar reiturinn **Gerð samskiptareglu við útskráningu** er stillur á _cXML_ fyrir ytri vörulista, fangar kerfið skilaboðakladda karfanna sem koma til baka frá lánardrottnum. Hægt er að nota þennan kladda fyrir úrræðaleit og öðrum tilgangi tengdum gögnum.

Til að opna kladdann fyrir ytri vörulista skal velja viðeigandi vörulista og síðan, á aðgerðasvæðinu, skal velja **Skilaboðakladdi cXML-körfu**. Síðan **Skilaboðakladdi cXML-körfu** sýnir lista yfir körfurnar sem hefur verið skilað, XML sem tengist þessum körfum og línurnar sem voru stofnaðar í tengdri innkaupabeiðni.

![Síða skilaboðakladda cXML-körfu](media/cxml-cart-message-log.png "Síða skilaboðakladda cXML-körfu")

## <a name="set-the-extrinsic-elements-for-external-catalog-punchout"></a>Setja upp utanaðkomandi einingar fyrir PunchOut ytri vörulista

Þegar reiturinn **Gerð samskiptareglu við útskráningu** er stilltur á *cXML* fyrir ytri vörulista, er hægt að bæta við utanaðkomandi einingum sem verða settar inn á réttan stað í skilaboði XML-beiðni.

Til að bæta utanaðkomandi einingum við ytri vörulista skal fylgja þessum skrefum.

1. Farið í **Innkaup og aðföng \> Vörulistar \> Ytri vörulistar**.
1. Veljið viðeigandi vörulista.
1. Í flýtiflipanum **Snið skilaboða**, í hlutanum **Utanaðkomandi**, skal velja **Bæta við** til að bæta línu við hnitanetið fyrir hverja utanaðkomandi einingu sem á að hafa með. Í hverri línu skal stilla eftirfarandi reiti:

    - **Heiti** - Færið inn heiti fyrir eininguna. Þetta gildi mun verða gildið á eigindinni **heiti** fyrir XML-eininguna **Utanaðkomandi** sem hver röð býr til. Yfirleitt er heitið gefið í samvinnu við lánardrottin fyrir hverja utanaðkomandi einingu.
    - **Gildi** - Veljið gildi fyrir eininguna. Þetta gildi mun verða gildi XML-einingarinnar sem stofnuð er af hverri línu. Eftirtalin gildi eru tiltæk:

        - **Notandanafn** – Notið nafn notandans sem er að gera PunchOut. Þetta nafn er innskráningarnafnið fyrir Supply Chain Management.
        - **Netfang notanda** – Notið netfang notandans sem er að gera PunchOut. Þetta aðsetur er aðsetur sem notandinn hefur sett upp í flipanum **Reikningur** á síðunni **Notandavalkostir**.
        - **Handahófskennt gildi** – Notið einkvæmt gildi af handahófi.
        - **Fullt nafn notanda** – Notið fullt nafn tengiliðarins sem tengist notandanum sem er að opna ytri vörulista.
        - **Fornafn** – Notið fornafn tengiliðarins sem tengist notandanum sem er að opna ytri vörulista.
        - **Eftirnafn** – Notið eftirnafn tengiliðarins sem tengist notandanum sem er að opna ytri vörulista.
        - **Símanúmer** – Notið aðalsímanúmer tengiliðarins sem tengist notandanum sem er að opna ytri vörulista.

![Stillingar utanaðkomandi einingar](media/cxml-extrinsics.png "Stillingar utanaðkomandi einingar")

Notandinn eða stjórnandinn mun ekki sjá utanaðkomandi einingarnar vegna þess að þeim er ekki bætt við fyrr en notandi gerir PunchOut. Þær verða sjálfkrafa settar inn á milli eininganna **BuyerCookie** og **BrowserFromPost** í beiðniskilaboðum cXML-uppsetningar. Þess vegna þarf ekki að stilla þær handvirkt í XML þegar ytri vörulisti er settur upp.

![Utanaðkomandi einingum bætt við XML](media/cxml-extrinsics-xml.png "Utanaðkomandi einingum bætt við XML")

## <a name="create-and-process-a-purchase-order"></a><a name="create-po"></a>Stofna og vinna úr innkaupapöntun

Þegar stofnuð er innkaupapöntun fyrir lánardrottin mun hún erfa stillinguna á valkostinum **Senda innkaupapöntun með cXML** frá þeim lánardrottni. Stillingin verður hins vegar áfram tiltæk í flýtiflipanum **Uppsetning** í yfirlitinu **Haus** í innkaupapöntuninni, þannig að hægt sé að breyta henni seinna ef þess gerist þörf.

![Innkaupapöntun stillt til að nota cXML](media/cxml-purchase-order.png "Innkaupapöntun stillt til að nota cXML")

Þegar stofnuð er innkaupapöntun úr innkaupabeiðni sem kom PunchOut-flæði, verða allar nauðsynlegar línuupplýsingar fylltar út. Þá er hægt að bæta innkaupapöntunarlínum handvirkt við eða afrita þær úr öðrum innkaupapöntunum. Gætið þess að stilla alla áskilda reiti. Þessir áskildu reitir innihalda ytra tilvísunarnúmerið, sem er númer lánardrottins sem verður notað í cXML-skilaboðinu.

![Dæmi um ytra tilvísunarnúmer](media/cxml-line-details.png "Dæmi um ytra tilvísunarnúmer")

Þegar þú hefur lokið við að fylla út allar upplýsingar um innkaupapöntunina skaltu ganga úr skugga um að staðfesta hana. Engin skilaboð eru send nema innkaupapöntun sé staðfest. Til að staðfesta innkaupapöntun, á aðgerðasvæðinu, í flipanum **Innkaup**, í flokknum **Aðgerðir**, skal velja **Staðfesta**. 

Þegar innkaupapöntunin hefur verið staðfest er hægt að skoða stöðu staðfestingarinnar í gegnum færslubækurnar **Staðfestingar á innkaupapöntunum**. Á Aðgerðasvæðinu, á flipanum **Innkaup**, í flokknum **Færslubækur** velurðu **Staðfesting innkaupapantana**.

Hver innkaupapöntun getur haft margar staðfestingar. Hver staðfesting er merkt með stigvaxandi númeri. Á eftirfarandi mynd er innkaupapöntunin *00000275* og staðfestingin er *00000275-1*. Þessi tölusetning endurspeglar staðlaða virkni Supply Chain Management, þar sem breytingar á innkaupapöntun og þar af leiðandi gerð cXML-skilaboða sem á að senda til lánardrottins eru auðkennd samkvæmt staðfestingunni. Eins og myndin sýnir, inniheldur síðan **Staðfestingar á innkaupapöntunum** einnig reitina **Sendingarstaða pöntunar** og **Lánardrottnastaða pöntunarbeiðni**. Frekari upplýsingar um mismunandi stöðugildi sem hægt er að skoða á þessari síðu er að finna í hlutanum [Fylgjast með beiðnum um innkaupapöntun](#monitor-po-requests) síðar í þessu efnisatriði.

![Staðfestingasíða innkaupapantana](media/cxml-po-confirmations.png "Staðfestingasíða innkaupapantana")

Til að skoða frekari upplýsingar um skjalið skal velja **Beiðni innkaupapöntunar** fyrir ofan hnitanetið.

Á síðunni **Beiðni innkaupapöntunar** eru tvö hnitanet. Hnitanetið í efri hluta síðunnar er með eina færslu fyrir hverja innkaupapöntun sem merkt er til sendingar. Hnitanetið í flipanum **Beiðniferill innkaupapöntunar** í neðri hluta síðunnar gæti haft nokkrar færslur fyrir valda innkaupapöntun til að gefa til kynna stöðu hverrar staðfestingar. Eftirfarandi mynd sýnir innkaupapöntun 00000275 í efra hnitanetinu og skjal 00000275-1 í hnitanetinu í flipanum **Beiðniferill innkaupapöntunar**.

![Beiðnisíða innkaupapöntunar](media/cxml-po-request.png "Beiðnisíða innkaupapöntunar")

Ef runuvinnslan er sett upp og í gangi, verður skjalið sent. Hægt er að skoða stöðubreytinguna þegar skjalið hefur verið sent. Á eftirfarandi mynd er reiturinn **Sendingarstaða pöntunar** stilltur á _Send_. Reiturinn **Lánardrottnastaða pöntunarbeiðni** er stilltur á _Móttekið_ til að gefa til kynna að lánardrottinn hafi móttekið skjalið og gat lesið það og vistað í kerfinu sínu. Hnitanetið í flipanum **Beiðniferill innkaupapöntunar** sýnir tímasetninguna þegar skjalið var sent. Frekari upplýsingar um hin ýmsu stöðugildi sem hægt er að skoða á þessari síðu er að finna í hlutanum [Fylgjast með beiðnum innkaupapöntunar](#monitor-po-requests).

![Stöðuskilaboð á beiðnisíðu innkaupapöntunar](media/cxml-po-request-2.png "Stöðuskilaboð á beiðnisíðu innkaupapöntunar")

## <a name="schedule-the-purchase-order-request-batch-job"></a><a name="po-batch"></a>Tímasetja runuvinnsluna fyrir beiðni um innkaupapöntun

Til að virkja runuvinnsluna til að senda beiðnir um innkaupapöntun er farið í **Innkaup og aðföng \> Uppsetning \> Stjórnun CXML \> Beiðni innkaupapöntunar** og síðan, á aðgerðasvæðinu, í flipanum **Beiðni innkaupapöntunar**, í flokknum **Runa**, er valið **Senda inn vinnslu** ti að opna svargluggann **Innkaupabeiðni undirbúin og send**. Hægt er að nota þennan svarglugga til að setja upp endurtekningu, rétt eins og venjulega er gert fyrir runuvinnslur í Supply Chain Management. Veljið tímabil, byggt á pöntunarmagni. Þó að hægt sé að keyra runuvinnsluna á mínútu fresti, er líklega best að senda runur í gegnum vinnudaginn, byggt á móttökugluggum pöntunar sem passa við áætlanir lánardrottna.

Til dæmis er lánardrottinn með reglu sem segir að allar pantanir er mótteknar eru fyrir klukkan 13:00 verða sendar samdægurs. Í þessu tilfelli gætir þú þurft að keyra vinnslu aðeins nokkrum sinnum um morguninn til að koma pöntunum á framfæri sem þú ert með. Eftirstandandi pantanir verða síðan sendar næsta dag. Þessi ákvörðun er eingöngu viðskiptalegs eðlis. Hægt er að yfirfara það og stilla færibreytur í samræmi við það.

Ferlið mun leita að skjölum um beiðni innkaupapantana sem eru með stöðuna *Í bið*. Ef pöntun er til staðar sem senda þarf lánardrottni þegar í stað er hægt að velja **Senda inn vinnslu** og stilla valkostinn **Runuvinnsla** á *Nei*.

## <a name="monitor-purchase-order-requests"></a><a name="monitor-po-requests"></a>Fylgjast með beiðnum innkaupapantana

### <a name="view-the-status-of-a-purchase-order"></a>Skoða stöðu innkaupapöntunar

Þegar pantanir sem hægt er að senda með cXML eru staðfestar fá þær stöðuna _Í bið_. Eins og lýst var í hlutanum [Stofna og vinna úr innkaupapöntun](#create-po), er hægt að skoða stöðu innkaupapöntunar á síðunni **Beiðni innkaupapöntunar**. Hver beiðni um innkaupapöntun getur haft eina af mörgum stöðum, fer allt eftir færibreytum hennar og gögnum. Þessi hluti lýsir mismunandi gerðum af stöðu og gildunum sem þær geta verið með. Þessar upplýsingar geta hjálpað þér að hafa umsjón með málum og skilja stöðu innkaupapantana.

![Staða innkaupapöntunar á beiðnisíðu innkaupapöntunarinnar](media/cxml-monitor-po-request.png "Staða innkaupapöntunar á beiðnisíðu innkaupapöntunarinnar")

Hnitanetið í efri hluta síðunnar **Beiðni innkaupapöntunar** kann að sýna eftirfarandi gildi fyrir stöðu:

- **Sendingarstaða pöntunar** – Þessi reitur getur haft eitt af eftirfarandi gildunum:

    - **Í bið** - Skjalið bíður þess að vera sent.
    - **Sent** - Skjalið hefur verið sent.
    - **Stöðvað** - Skjalið var merkt sem _Stöðvað_ áður en það var sent. (Til að merkja skjal sem _Stöðvað_ skal velja **Stöðva** á aðgerðasvæði síðunnar **Innkaupabeiðni**.)
    - **Safnvista** - Skjalið hefur verið hreinsað. (Til að hreinsa skjal skal velja **Hreinsa** á aðgerðasvæði síðunnar **Innkaupabeiðni**.)

- **Staða á pöntunarbeiðni lánardrottins** – Þessi reitur getur haft eitt af eftirfarandi gildum:

    - **Í bið** - Skjalið bíður þess að vera sent.
    - **Móttekið** - Skjalið hefur verið móttekið af lánardrottni. Hægt er að fara yfir ítarleg XML-skilaboðin sem lánardrottinn skilar með því að velja flipann **XML-svar** í neðri hluta síðunnar.
    - **Villa** - Skjalið var sent til lánardrottins, en villa kom upp. Hægt er að fara yfir villuboðin með því að velja flipann **XML-svar** í neðri hluta síðunnar.

Hnitanetið í flipanum **Beiðniferill innkaupapöntunar** í neðri hluta síðunnar **Beiðni innkaupapöntunar** kann að sýna eftirfarandi gildi:

- **Gerð pöntunarbeiðni** – Þessi reitur getur haft eitt af eftirfarandi gildum:

    - **Ný** – Línan er merkt sem ný strax eftir að innkaupapöntunin er staðfest.
    - **Uppfæra** – Ef staðfesting hefur þegar verið send og hún móttekin af lánardrottni, verður næsta staðfesting merkt sem _Uppfærsla_. Uppfærslur verða aðeins sendar ef valkosturinn **Senda uppfærslur á innkaupabeiðni** er stilltur á *Já* í [altækum cXML-færibreytum](#cxml-parameters).
    - **Eyða** – Ef staðfesting hefur þegar verið send og samþykkt af lánardrottni, en hætt er við innkaupapöntunina, verður staðfestingin sem er í bið merkt sem _Eyða_. Eyðingar verða aðeins sendar ef valkosturinn **Senda eyðingu á innkaupabeiðni** er stilltur á *Já* í [altækum cXML-færibreytum](#cxml-parameters).

- **Tímasetning beiðni** – Tíminn þegar pöntunarstaðfestingin var stofnuð. Hægt er að bera saman tíma beiðninnar við tíma pöntunarstöðu til að ákvarða tímann milli staðfestingar og samþykkis lánardrottins.
- **Sendingarstaða pöntunar** – Þessi reitur er sá sami og reiturinn **Sendingarstaða pöntunar** í efri hluta síðunnar. Hann er endurtekinn hér til að gera greiðara um vik að skoða stöðuna á stigi staðfestingar. Ef reiturinn **Gerð pöntunarbeiðni** er stilltur á *Ný* og innkaupapöntunin er staðfest að nýju áður en staðfesting er send, verður reiturinn **Sendingarstaða pöntunar** stilltur á *Safnvista*.
- **Tími pöntunarstöðu** - Tíminn þegar færsla beiðniferils innkaupapöntunar var síðast uppfærð. (Uppfærslurnar fela í sér breytingar á stöðu.)
- **Lánardrottnastaða pöntunarbeiðni** – Þessi reitur er sá sami og reiturinn **Lánardrottnastaða pöntunarbeiðni** í efri hluta síðunnar. Hann er endurtekinn hér til að gera greiðara um vik að skoða stöðuna á stigi staðfestingar.
- **Senda tíma inn aftur** - Tíminn þegar færslan var send aftur inn.
- **Fjöldi nýrra innsendinga** – Hversu oft færslan var senda aftur inn. Há tala gefur til kynna margar bilanir og gæti því hugsanlega gefið til kynna vandamál með annaðhvort gagnauppsetningu þína eða gagnauppsetningu lánardrottins.

### <a name="view-the-xml-for-a-purchase-order-request-message"></a>Skoða XML fyrir skilaboð um beiðni innkaupapöntunar

Til að skoða XML fyrir skilaboð innkaupapöntunarbeiðni skal velja flipann **Biðja um XML-texta** neðst á síðunni **Beiðni innkaupapöntunar**. Upplýsingarnar í þessum flipa geta verið gagnlegar við prófun eða villuleit. Til að gera upplýsingarnar læsilegri er hægt að skoða þær sem sniðin skilaboð. Afritið innihald flipans í textaskrá og skoðið það síðan í XML-ritli.

![Beiðniflipi XML-texta](media/cxml-request-xml-text.png "Beiðniflipi XML-texta")

### <a name="view-the-details-of-the-vendor-response"></a>Skoða upplýsingar um svar lánardrottins

Til að skoða innihald svars lánardrottins um staðfestingu eða villu, skal velja flipann **XML-svar** neðst á síðunni **Beiðni innkaupapöntunar**.

![Flipi XML-svars](media/cxml-response-xml.png "Flipi XML-svars")

## <a name="additional-resources"></a>Frekari upplýsingar

- [Setja upp ytri vörulista fyrir PunchOut e-Procurement](set-up-external-catalog-for-punchout.md)
- [Nota ytri vörulista fyrir PunchOut e-procurement](use-external-catalogs-for-punchout.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]