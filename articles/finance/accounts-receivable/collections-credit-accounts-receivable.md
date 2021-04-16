---
title: Innheimta í viðskiptakröfum
description: Innheimtuupplýsingum viðskiptakrafna er stjórnað í einu miðlægu yfirliti með því að nota síðuna Söfn Microsoft Dynamics 365 Finance. Stjórnendur kredit- og innheimtubréfa geta notað þetta miðlæga yfirlit til að stjórna innheimtu. Innheimtustjórar getur hafið ferli innheimtuaðgerða úr lista viðskiptavina sem er myndaður með því að nota forskilgreind skilyrði um innheimtubréf eða frá síðunni Viðskiptavinir.
author: ShivamPandey-msft
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustAgingSnapshot, CustBankAccounts, CustCollections, CustCollectionsActivitiesListPage, CustCollectionsAgent, CustCollectionsCaseListPage, CustCollectionsPool, CustCollectionsPoolsListPage, CustTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 3061
ms.assetid: fd851520-8d93-434b-845b-be127d6ac3a6
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3dc4dc556cbb8bd461e904ef569016acd4276f7a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814249"
---
# <a name="collections-in-accounts-receivable"></a>Innheimta í viðskiptakröfum

[!include [banner](../includes/banner.md)]

Innheimtuupplýsingum viðskiptakrafna er stjórnað í einu miðlægu yfirliti með því að nota síðuna Söfn Microsoft Dynamics 365 Finance. Stjórnendur kredit- og innheimtubréfa geta notað þetta miðlæga yfirlit til að stjórna innheimtu. Innheimtustjórar getur hafið ferli innheimtuaðgerða úr lista viðskiptavina sem er myndaður með því að nota forskilgreind skilyrði um innheimtubréf eða frá síðunni Viðskiptavinir.

Áður en byrjað er að setja upp eða vinna með innheimtu þarf að skilja eftirfarandi hugtök:
-   Aldursgreiningarmynd viðskiptavinar innihaldur upplýsingar um aldursgreind staða á ákveðnum tímapunkti.
-   Innheimta viðskiptavinahópa hjálpar þér að skipuleggja vinnu þína
-   Innheimtufulltrúar geta haft sína eigin viðskiptavinahópa
-   Listasíður skipuleggja innheimtuviðskiptavini, verkþætti og mál
-   Allar innheimtuupplýsingar viðskiptavinar eru á einni síðu og hægt er að velja aðgerðir af síðunni
-   Niðurfellingu, endurskipun eða bakfærslu vaxta og gjalda er hægt að gera í einu þrepi
-   Stofna afskrift er hægt að gera í einu þrepi
-   Hægt er að gera vinnslu ónóg inneign (NSF) greiðslur í einu þrepi

Eftirfarandi hlutar útskýra hvert hugtak fyrir sig.

## <a name="customer-aging-snapshots"></a>Aldursgreiningarmynd viðskiptavinar
Aldursgreiningarmynd inniheldur útreiknaða aldursgreinda stöðu fyrir viðskiptavin á einum tímapunkti. Þessar upplýsingar birtast á listasíðunni Aldursgreindar stöður og á Innheimtu síðunni. Stofna skal aldursmynd áður en hægt er að skoða upplýsingar um listasíður Innheimtu. 

Fyrir hvern viðskiptavin inniheldur aldursgreiningarmynd haus í aldursgreiningarmynd og ítarupplýsingar um færslur sem samsvara hverju aldurstímabili í skilgreiningu aldurstímabils. 

Haus í aldursgreiningarmynd inniheldur heildarupphæð greiðslu, lánamark, fylgiseðils upphæð, upphæð sölupöntunar, fjölda ágreiningsfærslna og heildarupphæð ágreiningsfærslna fyrir lykil viðskiptavinar. Allar færslur fyrir þennan viðskiptavin verða teknar með í útreikningnum þessara upphæða. Samtals upphæð til greiðslu, lánamark, upphæð fylgiseðils og upphæð sölupöntunar eru sýndar í lánaupplýsingar Upplýsingakassa á síðu Innheimtu.. 

Fyrir hvert aldurstímabil í skilgreiningu aldurstímabils, er ítarleg skýrsla fyrir aldursgreiningarmynd stofnuð. Hver ítarleg skýrsla fyrir aldursgreiningarmynd inniheldur auðkenni aldurstímabils og heildarupphæð færslna með dagsetningarnar sem eru á aldurstímabilinu. Færslur eru tengdar við aldurstímabil, eins og 30 daga fram yfir gjalddaga. Dagsetningin er í samræmi við Aldursgreiningu frá og með dagsetningu sem tilgreind er þegar aldursgreiningarmynd var stofnuð. Þessar upplýsingar birtast á listasíðunni Aldursgreindar stöður og í upplýsingakassanum Aldursgreindar stöður á Innheimtu síðunni.

## <a name="collections-customer-pools"></a>Innheimtumál viðskiptavinahópa
Viðskiptavinahópar eru fyrirspurnir sem skilgreina flokk af viðskiptavinaskrám sem hægt er að birta og stjórna fyrir innheimtu eða aldursgreiningarferli. Nota viðskiptavinahópa til að sía upplýsingar á listasíðunum Aldursgreind staða, Innheimtuaðgerðir og Innheimtumál. Einnig er hægt að nota viðskiptavinahópa til að sía viðskiptavinalykla sem eru teknar með þegar aldursgreiningarmynd er stofnuð.

## <a name="collections-agents"></a>Innheimtufulltrúar
Að sjálfgefnu geta notendur skoðað allar upplýsingar um viðskiptavini á listasíðum innheimtu. Hægt er að nota færslur innheimtufulltrúa til að ákvarða viðskiptavinahópa sem eru tiltækir til að sía upplýsingar á listasíðu Söfn og Innheimtusíðu. 

Innheimtufulltrúi með er sá einstaklingur sem vinnur með viðskiptavini til að tryggja að greiðslurnar eru innheimtar í tæka tíð. Innheimtufulltrúar eru starfsmenn sem eru tengdir notendum á síðunni Uppsetning.

## <a name="collections-list-pages"></a>Listasíður innheimtu
Eftirfarandi listasíður aðstoða við skipulagningu upplýsingar um innheimtu..
-   Aldursgreind staða - Í dálkunum á listasíðunni birtast stöður viðskiptamanna og aldursgreindar upphæðir eftir aldursgreiningartímabili. Þessar upplýsingar eru geymdar í aldursgreiningarmynd. Aldurstímabil ákvarðast af skilgreiningu aldurstímabils sem er notuð. Skilgreining aldurstímabils er fengið úr viðskiptavinahópnum ef það var tilgreint fyrir fyrirspurnarhópinn. Ef viðskiptavinahópurinn hefur ekki skilgreiningu aldurstímabils, er notað sjálfgefna skilgreining aldurstímabils sem er tilgreint í skjámyndinni færibreytur viðskiptakrafna. Ef engin sjálfgefin skilgreining aldurstímabils er tilgreind, er fyrsta skilgreining aldurstímabils í Skilgreining aldurstímabils skjámynd notað.
-   Innheimtuverkþættir – Dálkar á listasíðunni birta verkþætti sem eru auðkenndir sem innheimtuverkþætti. Þessar aðgerðir eru stofnaðar með því að nota síðuna Innheimtur. Nota verkþætti til að rekja verk sem eru tengd innheimtu.
-   Innheimtumál – Dálkar á listasíðunni birta upplýsingar um mál sem hafa málstegund með málsgerðina Innheimta.

> [!NOTE]
> Stofna skal aldursgreiningarmynd áður en hægt er að skoða upplýsingar á þessum listasíðum. Upplýsingar eru aðeins sýndar vegna viðskiptavina sem aldursgreiningarmynd hefur verið stofnuð fyrir. Færslurnar sem eru birtar á listasíðunni geta verið síaðar að auki sem hér segir:
> <li>Að sjálfgefnu hefur Finance and Operations-notandi aðgang að öllum viðskiptavinum sem hafa aldursgreiningarmynd.</li>
> <li>Ef viðskiptavinahópar eru til staðar verður að setja notanda upp sem innheimtufulltrúa til að nota hópana til að sía upplýsingar í listasíður innheimtu. Upplýsingar takmarkast við viðskiptavini sem eru hafðir með í valda viðskiptavinahópnum.</li>
> <li>Ef notandi er settur upp sem innheimtufulltrúi eru aðeins þeir hópar sem eru valdar fyrir þann innheimtufulltrúa tiltækar á listasíðu. Ef breytan Leyfa fulltrúa að skoða allar viðskiptavinahópa er valin í Innheimtufulltrúa síðunni fyrir innheimtufulltrúann eru allir hópar tiltækir fyrir þann fulltrúa.</li>


## <a name="collections-page"></a>Innheimtusíða
Nota síðuna Innheimta til að skoða, stjórna og framkvæma upplýsingar um innheimtu, verkþætti og mál viðskiptavina. 

Efri rúðan birtir mál valins viðskiptavinar. Miðjurúðan birtir færslur viðskiptavinar. Neðri rúðan birtir verkþætti fyrir viðskiptavininn. Hægt er að stofna innheimtumál til að rekja upplýsingar um innheimtu fyrir eina eða fleiri færslur og verkþætti. Hægt er að sía upplýsingar í efri og neðri rúðu eftir máli. 

Upplýsingakassar birta aldursgreindar stöður og upplýsingar um lánamark fyrir valinn viðskiptavin. Þessar upplýsingar eru geymdar í aldursgreiningarmynd. Ef nauðsyn krefur er hægt að uppfæra aldursgreiningarmynd með gildandi upplýsingum. 

Aðgerðarúðan inniheldur hnappa sem birta tengdar upplýsingar fyrir valinn viðskiptavin, mál, færslu eða verkþætti. Einnig er hægt að framkvæma almennar aðgerðir svo sem breyta færslu innheimtustöðu, senda tölvupóst samskipti með samþættingu við tölvupóstsveitu þína, endurgreiða viðskiptavini, vinna NSF-greiðslur og afskrifa óinnheimtanlegar kröfur.

## <a name="waive-reinstate-or-reverse-interest-and-fees"></a>Fella niður, endurskipa eða bakfæra vexti eða gjöld
Hægt er að fella niður, endurskipa eða bakfæra vaxtanótur eða þóknanir og vexti á færslur sem eru hluti af vaxtanótum. Þetta er gert úr Innheimta flipanum í Aðgerðarúðunni á Allir viðskiptavini listasíðu með því að smella á Vaxtanótu, Færslu vaxta eða Þóknanir. 

Þessar leiðréttingar hafa aðeins áhrif á vaxtanótur, og vexti og gjöld sem þær hafa. Fylgið skrefum í hlutanum "Stofna afskriftarfærslur í einu lagi" til að afskrifa öll gjöld sem viðskiptavinur skuldar.

Frekari upplýsingar, sjá [Stofna vaxtakóða með sviði](tasks/create-interest-code-range.md) og [Reikna vexti](tasks/process-interest.md). 

## <a name="create-writeoff-transactions"></a>Stofna afskriftafærslur
Þú getur afskrifað gallaðar skuldir með því að smella á Afskrifa í skjámyndinni Innheimta og á listasíðunum Aldursgreindar stöður, Viðskiptavinir og Opna reikninga viðskiptavinar. 

Þegar færslur eru afskrifaðar fyrir viðskiptavini, eru allar færslur fyrir viðskiptavininn sjálfkrafa merktar til jöfnunar. Upphæð sem er afskrifuð fer eftir nettóupphæð merktra færslna. Afskriftarfærsla er stofnuð í færslubók og getur í mesta lagi innihaldið þrjá gerðir á færslubókarlínum.

-   Fyrsta gerð færslubókarlínu inniheldur afskrift færslu viðskiptavinar. Ef merktar færslur innihalda margar samsetningar af gjaldmiðilskóða, vídd og bókunarreglum, er aðskilin færslubókarlína stofnuð fyrir hverja samsetningu.
-   Önnur gerð færslubókarlínu inniheldur fjárhagsfærslu afskriftar viðskiptavinar. Ef merktar færslur innihalda margar samsetningar af gjaldmiðilskóða, vídd og bókunarreglum, er aðskilin færslubókarlína stofnuð fyrir hverja samsetningu.
-   Þriðja gerð færslubókarlínu inniheldur upplýsingar um afskriftir fjárhags fyrir virðisaukaskatt. Færslubókarlínan er einungis stofnuð ef breytan Aðskilja virðisaukaskatt° er valin á síðunni færibreytur viðskiptakrafna. Ef merktar færslur innihalda margar samsetningar af reikningum virðisauka, víddum og virðisaukakóðum er aðskilin færslubókarlína stofnuð fyrir hverja samsetningu.

Afskriftarfærslan er búin til í færslugjaldmiðlinum.

Nánari upplýsingar er að finna í [Stofna afskriftabók fyrir viðskiptavin](tasks/create-write-off-journal-customer.md).

<a name="process-not-sufficient-funds-nsf-payments"></a>Vinna innistæðulausar greiðslur (NSF) 
--------------------------------------------

Hægt er að vinna NSF-greiðslur með því að smella á NSF-greiðslur á Innheimtu síðu. Þegar smellt er á þennan hnapp er hætt við greiðsluna. Ef NSF-þóknun á við um viðskiptamanninn er gjaldafærsla stofnuð í greiðslubók.. Upphæð þóknunar er grundvölluð á stillingum fyrir sjálfvirk gjöld. Sjálfvirk gjöld sem notuð eru fyrir NSF-greiðslur eru tilgreind með gjaldaflokki sem er valinn í skjámyndinni Bankareikningur fyrir bankareikninginn sem varð fyrir áhrifum.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]