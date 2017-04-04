---
title: "Stjórna undirverktaka vinnu í framleiðslu"
description: "Í þessu efnisatriði er útskýrt hvernig úthýsta aðgerðir eru meðhöndlaðar í Microsoft Dynamics 365 aðgerða. Með öðrum orðum, það útskýrt hvernig aðgerðaröðun sem er úthlutað á tilfanga er stjórnað af lánardrottni."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LeanDocumentServiceCreation, PlanActivity, ProdBOMVendorListPage, ProdRoute, ProdTable, ProdTableListPage, PurchAgreementSubcontractorLookup, RouteTable, WrkCtrResourceGroup
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 268174
ms.assetid: fe47c498-4f48-42a2-a0cf-5436c19ab3ea
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 79430358bebd93fd96f1169d22737d3537dbfc08
ms.lasthandoff: 03/31/2017


---

# <a name="manage-subcontracting-work-in-production"></a>Stjórna undirverktaka vinnu í framleiðslu

Í þessu efnisatriði er útskýrt hvernig úthýsta aðgerðir eru meðhöndlaðar í Microsoft Dynamics 365 aðgerða. Með öðrum orðum, það útskýrt hvernig aðgerðaröðun sem er úthlutað á tilfanga er stjórnað af lánardrottni.

Í [framleiðsluferli](production-process-overview.md), er hægt að gera vinnu með tilföngum sem tilheyra ekki eða eru stjórnað með lánardrottnum. Yfirleitt, tilföng lánardrottins eru notaðar til að stigs reglubundna umfram eftirspurnar sem tiltæk afkastageta í fyrirtæki surpasses eigin tilföng. Lánardrottinn hugsanlega einnig bjóða ákveðna [tilfangagetu](resource-capabilities.md)eða tilföngum á neðri verði.  

Eftir tilföngum lánardrottins sem eru notaðar í framleiðsluferlinu, er [leið](routes-operations.md) hefur oft fleiri logistic þarfir, þar sem efni og hálfkláraðar afurðir verður fyrst að flytja svæði lánardrottins. Síðan verður að flytja niðurstöðu aðgerðarinnar úthýsta annaðhvort á þá staðsetningu sem er úthlutað til næsta aðgerð eða vöruhús fullbúnar vörur.  

Þegar undirverktaka aðgerðir eða verkþætti sem eru notaðar þær áhrif á öll stig aðgerða frá skilgreiningu á aðgerðir sem þarf í framleiðslunni, kostnaðarútgáfu, spár, áætlanagerð og röðunar til að stjórna vörustjórnunar fyrir efni, hálfkláraðar vörur og kláraðar vörur. Loks er þessi tilföng þarfnast sína ferli bókhaldi og kostnaðarstýring.  

Fyrir innri tilföng fast kostnaðarhlutfall er yfirleitt úthlutað á tímabili. Gagnstætt með kostnaður við úthýsta tilföng byggist á innkaupsverð tengdar þjónustu. Þjónustan er skilgreindur sem aðra afurð og er notað til að keyra í innkaupa- og innkaupapantanir ferli fyrir úthýsta tiltekna aðgerð.  

Núna, það er engin yfirlýst hugtakið hálfkláraðar afurðir í Microsoft Dynamics 365 aðgerða. Fyrir framleiðslupöntun sem krefst fleiri en einni aðgerð til að umbreyta hráefni í fullbúin framleiðsluvara, fullbúin framleiðsluvara bókað aftur í birgðir í síðustu aðgerð. Hálfkláraðar afurðir fyrri aðgerðir að framleiða eru gjaldfært í verk í vinnslu (VÍV), en ekki eru kostnaðarjafnaðar að bóka þær eða raktar í birgðum. Þó að hægt er að skipta í margar einingar leiðir og uppskriftir (BOMs), eykst þessa nálgun fjölda vörur, Uppskriftir og leiðir sem verður að vera stjórnað.  

Það eru tvær aðferðir fyrir líkanabreytur undirverktaka vinnu fyrir aðgerðaröðun. Þessar aðferðir mismunandi hátt sem subcontracting ferlið er miðuð, hvernig hálfkláraðar afurðir eru sýndir í vinnslu og hvernig kostnaðarstýringu er stjórnað.

-   Undirverktaka aðgerða leið í framleiðslu eða runupantanir
    -   Þjónusta afurðar verður að vera afurð í birgðum og það verður að vera hluti af Uppskriftinni.
    -   Þessi aðferð styður fyrst inn, fyrst út (FIFO) eða staðlaðan kostnað.
    -   Hálfkláraðar afurðir eru sýndir með þjónustuafurð í ferlinu.
    -   Kostnaðarstýring úthlutar kostnað sem tengjast undirverktaka kostnað í efni.
-   Undirverktaka á verkþætti framleiðsluflæðis í lean framleiðsluflæðis
    -   Þjónustan er ekki á lager þjónustuafurð og hann er ekki hluti af Uppskriftinni.
    -   Þessi aðferð notar innkaupasamninga sem þjónustusamningum.
    -   Þessi aðferð notar bakfærslukostnaðaraðgerðar.
    -   Þessi aðferð gerir ráð fyrir ósamstillt og samanlögðum innkaupa. (Efni flæði er óháð ferli innkaupa.)
    -   Kostnaðarstýring úthlutar undirverktaka í sína eigin læsa sundurliðun kostnaðar.

## <a name="subcontracting-of-route-operations"></a>Undirverktaka af leiðaraðgerðir
Til að nota undirverktaka aðgerða leiðar til framleiðslu eða runupantanir, verður að vera skilgreint sem afurð af þjónustuafurð sem er notað fyrir innkaup á þjónustu í **Þjónustu** gerð. Þar að auki, það verður að vera með vörulíkanaflokk sem hefur í **afurð í Birgðum** valkostinum undir **Birgða reglu** stillt á **Já**. Þessi valkostur ákvarðar hvort afurð er að kostnaðarfæra sem birgðir á innhreyfingarskjali afurða (**afurð í Birgðum** = **Já**), eða hvort afurðin gjaldfærð á rekstur (**afurð í Birgðum** = **Nei**). Þótt þetta hegðun gæti seem contradictory er grundvelli í því þess að aðeins afurðir sem hafa þessa reglu verður að stofna birgðafærslur, sem hægt er að nota í kostnaðarstýringu til að reikna áætlaðs kostnaðar og ákvarða raunkostnað þegar framleiðslupöntun er lokið.  

Til að hafa í huga í útreikningi fjárhagsáætlunargerðar og kostnaðar, þjónustuna verður bætt við Uppskrift. Uppskriftarlínunni verður að vera í **Lánardrottins** gerð og verður að úthluta leiðaraðgerð þjónustu úthlutuð. Þessi aðgerð á leiðinni verða að hafa kostnaðartilföng og tilfangaþörf sem benda á tilföngum af á **Lánardrottins** sem tengir tengdar þjónustu og aðgerð á viðeigandi lánardrottnalykil.  

Þegar þessari skilgreiningu er notað innkaupapöntun er stofnuð fyrir tengdar þjónustuafurð, byggt á mat á framleiðslupöntun. Innkaupapöntun þjónustunnar er notaður sem akkeri fyrir úthýsta aðgerðir. Hægt er að vinna undirverktaka í gegnum í **Úthýstur vinnu** listasíðu í framleiðslustýringar. Undirverktaka sem er notuð til að senda hráefni og, að endingu, hálfkláraða afurð lánardrottins geiðsluáætlun fyrir aðgerðina. Það er einnig notuð til að fá útkomunnar afurð úthýsta aðgerðarinnar í vörumóttaka, þar sem afurðin þjónusta er notuð til að auðkenna komu hálfkláraðri afurð. Þegar línu í innkaupapöntun er móttekin, uppfærist aðgerð framleiðslu sem lokið.  

Framleiðslupöntun geta verið margar aðgerðir og hægt er að úthluta hverri aðgerð á annan lánardrottinn. Þess vegna er á ljúka til að ljúka framleiðslupöntun gæti kveikja mörgum innkaupapöntunum.

## <a name="subcontracting-of-production-flow-activities"></a>Undirverktaka á verkþætti framleiðsluflæðis
Í [fyrirferðarlitla](lean-manufacturing-overview.md)lausn líkön subcontracting vinnu og þjónustu sem tengjast verkþætti með í [framleiðsluflæði](http://ax.help.dynamics.com/en/wiki/create-a-production-flow-version/) (Verkefni handbók efnisatriði). Þar af leiðandi hefur þessi gerð af undirverktaka er einnig kallað [verkþátturinn er byggður á undirverktaka.](activity-based-subcontracting.md) Gerð flokks inn sérstaka kostnaður **Beina útvistun**, hefur verið innleiddur og subcontracting services ekki eru kostnaðarjafnaðar hluti uppskriftarinnar fullbúnu vörunnar. Þegar fyrirferðarlitla, alla verkþætti skilgreint af kanbana sem hægt er að tengjast verkþætti framleiðsluflæðis eina eða margar. Hingað, sem útskýringar sounds rétt eins og útskýringar á framleiðslupantanir. Hins vegar meðan framleiðslupantanir verður alltaf að enda tilbúin afurð, hægt er að stofna kanbana sem á að afhenda hálfkláraða afurð. Vinnukortaheimild ekki til þess að ný afurð og uppskriftarstigi.  

Þar sem kanban-reglur getur verið mjög breytileg getur líkan ólíkar vöruvíddasamsetningar framboð fyrir sömu vöru á framleiðsluflæðis. Þegar lean undirverktaka, efni flæði og fjárhagsleg flæði eru sniðnir aðgreind. Öll efni flæði er táknuð með verkþátta kanban. Innkaupapantanir fyrir þjónustu afurðir og móttöku bókanir í þær services getur verið sjálvirk, byggt á stöðu kanban-vinnslur í framleiðsluflæði. Kanban-vinnslur er hægt að hefja og ljúka jafnvel áður en innkaupapantanir eru stofnaðar. Hægt er að leggja saman úthýsingarskjöl (innkaupapöntun og móttöku innkaupa á þjónustu) eftir tímabili og þjónustu. Þess vegna innkaupaskjöl og línur hægt er að geyma lítið jafnvel í sterklega endurtekna aðgerðum þar sem lánardrottnar veita úthýsta þjónustu í eitt stykki framleiðsluflæðis.

### <a name="modeling-subcontracting-in-a-production-flow"></a>Líkanabreytur undirverktaka í framleiðsluflæði

Í á [magurþjónustu framleiðsluflæði](lean-manufacturing-modeling-lean-organization.md), er hægt að skilgreina ferli verkþáttar sem úthýstur þegar henni er úthlutað á vinnuflokkinn (tilfangaflokkur) sem hefur eitt lánardrottins tilfanga. Þegar vinnuflokks er úthýstur tengdar vinnsluverkþætti verða tengdar við samningslínu virka innkaupapöntunar sem inniheldur vöruna þjónustuna og verð á þjónustu. Þjónustusamningurinn verkþáttar skilgreinir einnig útreikning hlutfallið milli afurðarmagnið kanban-vinnslunnar og meðfylgjandi magn þjónustu. Hægt er að velja hvort þjónustu magnið er reiknað byggt á fjölda vinnslur, magn gallalausra afurða sem skráð er á vinnslurnar eða magn samtals afurða (þessa heildarmagn innihalda afurðir sem rýrnað).  

Einnig er hægt að skilgreina flutningsverkþætti sem úthýstur. Þessi skilgreining gerist óbeint þegar ber aðila fyrir sendingarstað í flutningi verkþætti. Þegar **Farmsendanda** eða **Viðtakanda**, ef samsvarandi uppruni eða mark vöruhús er stjórnað lánardrottins vöruhús verkþáttinn telst úthýstur. Þegar **Flutningsaðila**, verkþáttur er úthýstur alltaf. Ferli fyrir úthýsta verkþætti, eins og úthýsta flutningsverkþátt verður tengdur við þjónustusamning áður en hægt er að virkja framleiðsluflæðið.

### <a name="backflush-costing"></a>Bakfærslukostnaðaraðferð

Kostnaðarbókhald undirverktaka er fyllilega samþætt kostnaðarútreikning fyrir lean manufacturing lausnina (bakfærslukostnaðaraðgerðar kostnaðarútgáfu). Við móttöku innkaupapöntunar þjónustunnar er bókuð eða þegar reikningsfærsla fer fram, kostnaður þjónustu úthlutuð framleiðsluflæði. Fyrir bakfærslukostnaðaraðferð, úthýsta þjónustu frávikið er reiknað með mótfærslu subcontracting loka staðlaðs kostnaðar móttekinna afurða gagnvart raunverulega mótteknar og reikningsfærðar þjónustumagni.

## <a name="material-supply-for-subcontracted-operations"></a>Efni framboð fyrir úthýsta aðgerðir
Hálfkláraðar afurðir og tengdum efni verður að flytja á staðsetningu þar sem það er efnislega unnið. Þegar notuð úthýsta aðgerðir og verkþætti þessi flutningur oft tengjast viðbótar flutning á svæði lánardrottins sem unnið. Með því að úthluta efni á Uppskriftina við úthýsta aðgerð, er að tilgreina sem efni verður stig á staðsetningu framleiðsluinntaks tilfangaflokki fyrir úthlutað tilföngum. Áætlanagerð eða straumlínuáfyllingar síðan úthlutar efni á þá staðsetningu.  

Líkan birgða sem er staðsett á svæði lánardrottins, er besta á sviði til að skilgreina vöruhús stjórnað lánardrottins. Auðveldlega er hægt að skilgreina vöruhús stjórnað lánardrottins með því að stofna nýtt vöruhús og úthlutun lykli lánardrottins. Til að skrá sem efni verður flutt til lánardrottins áður en hægt er að framkvæma aðgerð, ætti að úthluta vöruhúsi stjórnað lánardrottins við ílagsvöruhús tilfangaflokksins sem geymir tilfang.  

Til að fylla á efni í þessu vöruhúsi. hægt er að nota margar stefnu:

-   Flutningspantanir
-   Flutningabækur
-   Úttektarkanbön
-   Beina innkaupapöntun til staðsetningar lánardrottins

Hálfkláraðar afurðir eru undantekningar frá þessari reglu. Til að flytja hálfkláraðar afurðir, er afskriftareglur eru takmarkaðir við valkosti:

-   Í framleiðslu og runupantanir hálfkláraðar afurðir hægt einungis að flytja röklega með því að nota færslubók Tiltektarlista frá á **Úthýstur vinnu** listasíðu. Þessi færslubók stofnar fylgiseðils skjal sem er hægt að nota til að flytja hálfkláraðar og hráefni til lánardrottins.
-   Fyrir úthýsta aðgerðir í framleiðsluflæði flutning hálfkláraðar afurðir skráðar með kvittun kanban frádráttur eða framleiðslu á staðsetningunni lánardrottins. Að líkan yfirlýst flutning verkþætti, er hægt að ljúka kanban-framleiðslu við verkþátt viðbótar flutning.

**Athugasemd:** framleiðsluleið fyrir eina framleiðslupöntun ekki dreifing mörgum svæðum. Þessi regla á einnig við um þá undirverktaka. Þess vegna vöruhúsin sem tákna lánardrottins stýrt efni verður að vera skilgreint stöðum í sama svæði og innri tilföng sem notuð eru í leiðinni. Þótt framleiðsluflæði getur dreifing sites, þær er ekki hægt að flytja hálfkláraðar afurðir úr einu svæði yfir á aðra þar sem aðgerð þess skuli skilavörur breytingu á samhengi kostnaðar.  

Venjulega er úttak vöruhús og staðsetning úthýsta tilfangaflokki beint úthlutað vöruhús og staðsetning í næsta skref í aðgerðina í flæði leið eða framleiðslu. Þessi uppsetning hjálpar til við að lækka upphæð vinnslu skýrslugerð sem á sér stað eða númer viðbótar flutning aðgerðir sem þarf að gera líkan af.


