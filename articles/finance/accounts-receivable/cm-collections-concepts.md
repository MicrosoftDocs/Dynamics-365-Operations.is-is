---
title: Lykilhugtök innheimtustýringar
description: Viðfangsefnin skilgreina lykilhugtök fyrir innheimtustýringu.
author: mikefalkner
ms.date: 11/27/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 7f23f3668bfc344b2964c1b0062a5ed1174df05c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5835389"
---
# <a name="collections-management-key-concepts"></a>Lykilhugtök innheimtustýringar

[!include [banner](../includes/banner.md)]

Áður en byrjað er að setja upp eða vinna með innheimtu þarf að skilja eftirfarandi hugtök:

- Aldursgreiningarmynd viðskiptavinar innihaldur upplýsingar um aldursgreind staða á ákveðnum tímapunkti.
- Innheimta viðskiptavinahópa hjálpar þér að skipuleggja vinnu þína.
- Innheimtufulltrúar geta haft sína eigin viðskiptavinahópa.
- Listasíður skipuleggja innheimtuviðskiptavini, verkþætti og mál.
- Allar innheimtuupplýsingar viðskiptavinar eru á einni síðu og hægt er að velja aðgerðir af síðunni.
- Hægt er að fella niður vexti og gjöld, endurskipa þau eða bakfæra í einu þrepi.
- Afskriftafærslur er hægt að stofna í einu þrepi.
- Innistæðulausar (NSF) greiðslur er hægt að vinna í einu þrepi.

Þetta efni lýsir hverju hugtaki.

## <a name="customer-aging-snapshots"></a>Aldursgreiningarmynd viðskiptavinar

Aldursgreiningarmynd inniheldur útreiknaða aldursgreinda stöðu fyrir viðskiptavin á tilteknum tímapunkti. Þessar upplýsingar eru sýndar á listasíðunni **Aldursgreindar stöður** og á síðunni **Innheimta**. Búa þarf til aldursgreiningarmynd áður en hægt er að skoða upplýsingar á innheimtulistasíðum (**Aldursgreindar stöður**, **Innheimtustarfsemi** og **Innheimtumál**).

Fyrir hvern viðskiptavin er aldursgreiningarmynd með haus í aldursgreiningarmynd og ítarupplýsingar um færslur sem samsvara hverju aldurstímabili í skilgreiningu aldurstímabils.

Haus í aldursgreiningarmynd inniheldur heildarupphæð greiðslu, lánamark, fylgiseðils upphæð, upphæð sölupöntunar, fjölda ágreiningsfærslna og heildarupphæð ágreiningsfærslna fyrir lykil viðskiptavinar. Allar færslur fyrir þennan viðskiptavin verða teknar með í útreikningnum þessara upphæða. Samtals upphæð til greiðslu, lánamark, upphæð fylgiseðils og upphæð sölupöntunar eru sýndar í upplýsingareitnum **Lánaupplýsingar** á síðunni **Innheimta**.

Fyrir hvert aldurstímabil í skilgreiningu aldurstímabils, er ítarleg skýrsla stofnuð í aldursgreiningarmyndinni. Hver ítarleg skýrsla inniheldur kenni aldurstímabils og heildarupphæð færslna sem eru með dagsetningarnar á aldurstímabilinu. Færslur eru tengdar við aldurstímabil, eins og 30 daga fram yfir gjalddaga. Dagsetningin er í samræmi við þá dagsetningu **Aldursgreiningu frá og með** sem þú tilgreindir við stofnun á aldursgreiningarmyndinni. Þessar upplýsingar birtast á listasíðunni **Aldursgreindar stöður** og í upplýsingakassanum **Aldursgreindar stöður** á síðunni **Innheimta**.

## <a name="collections-customer-pools"></a>Innheimtumál viðskiptavinahópa

Hópar viðskiptavina eru fyrirspurnir sem skilgreina hóp af færslum viðskiptavina. Þú getur notað þessar flokkuðu skrár til að skoða upplýsingar fyrir viðskiptavini reikninga sem fylgja með og til að stjórna innheimtu- eða aldursgreiningarferlum fyrir þá. Þú getur notað viðskiptavinahópa til að sía upplýsingar á listasíðum innheimtu. Einnig er hægt að nota þá til að sía viðskiptavinalykla sem eru teknar með þegar aldursgreiningarmyndir eru stofnaðar.

## <a name="collections-agents"></a>Innheimtufulltrúar

Að sjálfgefnu geta notendur skoðað allar upplýsingar um viðskiptavini á listasíðum innheimtu. Skrár innheimafulltrúa gera þér kleift að ákvarða viðskiptavinahópa sem hægt er að nota til að sía upplýsingar á innheimtulistasíðum og síðunni **Innheimta**.

Innheimtufulltrúar vinna með viðskiptavinum til að tryggja að greiðslurnar séu innheimtar í tæka tíð. Þeir eru starfsmenn sem eru tengdir notendum á síðunni **Notandauppsetning**.

## <a name="collections-list-pages"></a>Listasíður innheimtu

Eftirfarandi listasíður aðstoða við skipulagningu upplýsingar um innheimtu:

- **Aldursgreind staða** - Í dálkunum á listasíðunni birtast stöður viðskiptamanna og aldursgreindar upphæðir eftir aldursgreiningartímabili. Þessar upplýsingar eru geymdar í aldursgreiningarmynd. Aldurstímabil ákvarðast af skilgreiningu aldurstímabils sem er notuð. Skilgreining aldurstímabils er fengið úr viðskiptavinahópnum ef hópur viðskiptavina var tilgreint fyrir fyrirspurnarhópinn. Ef viðskiptavinahópurinn er ekki með skilgreiningu aldurstímabils, er notað sjálfgefna skilgreining aldurstímabils sem er tilgreint í skjámyndinni **Færibreytur viðskiptakrafna**. Ef engin sjálfgefin skilgreining aldurstímabils er tilgreind, er fyrsta skilgreining aldurstímabils í **Skilgreining aldurstímabils** síðu er notað.
- **Innheimtuverkþættir** – Dálkar á listasíðunni birta verkþætti sem eru auðkenndir sem innheimtuverkþætti. Þessar aðgerðir eru stofnaðar á síðunni **Innheimta**. Þú notar verkþætti til að rekja innheimtutengda vinnu sem þú gerir.
- **Innheimtumál** – Dálkar á listasíðunni sýna upplýsingar um mál sem tilheyra málstegund með málsflokknum sem er með málsgerðina **Innheimta**.

### <a name="aging-snapshots"></a>Aldursgreiningarmyndir

Stofna skal aldursmynd áður en hægt er að skoða upplýsingar um innheimtulistasíðum. Upplýsingar eru aðeins sýndar vegna viðskiptavina sem aldursgreiningarmynd hefur verið stofnuð fyrir. Færslurnar sem eru birtar á listasíðunni geta verið síaðar frekar, sem hér segir:

- Sjálfgefið er að notendur hafa aðgang að öllum viðskiptavinum sem hafa aldursgreiningarmynd.
- Ef viðskiptavinahópar eru til staðar verður að setja notanda upp sem innheimtufulltrúa til að nota hópana til að sía upplýsingar í listasíður innheimtu. Upplýsingar takmarkast við viðskiptavini sem eru hafðir með í valda viðskiptavinahópnum.
- Ef notandi er settur upp sem innheimtufulltrúi eru aðeins þeir hópar sem eru valdar fyrir þann innheimtufulltrúa tiltækar á innheimtulistasíðum. Ef valkosturinn **Leyfa fulltrúa að skoða allar viðskiptavinahópa** er valinn á síðunni **Innheimtufulltrúi** fyrir innheimtufulltrúann eru allir hópar tiltækir fyrir þann fulltrúa.

## <a name="collections-page"></a>Innheimtusíða

Hægt er að nota síðuna **Innheimta** til að skoða, stjórna og framkvæma upplýsingar um innheimtu, verkþætti og mál viðskiptavina.

Efri hluti síðunnar sýnir mál fyrir valinn viðskiptavin, miðhlutinn sýnir færslur fyrir viðskiptavininn og neðri hlutinn sýnir starfsemi fyrir viðskiptavininn. Hægt er að stofna innheimtumál til að rekja upplýsingar um innheimtu fyrir eina eða fleiri færslur og verkþætti. Hægt er að sía upplýsingar í efri og neðri hlutar eftir máli.

Upplýsingakassar sýna aldursgreindar stöður og upplýsingar um lánamark fyrir valinn viðskiptavin. Þessar upplýsingar eru geymdar í aldursgreiningarmynd. Ef nauðsyn krefur er hægt að uppfæra aldursgreiningarmynd með gildandi upplýsingum.

Aðgerðaglugginn inniheldur hnappa sem sýna þér tengdar upplýsingar fyrir valinn viðskiptavin, mál, færslu eða verkþætti. Einnig er hægt að framkvæma almennar aðgerðir, eins og breyta færslu innheimtustöðu, senda tölvupóst með samþættingu við tölvupóstsveitu þína, endurgreiða viðskiptavini, vinna NSF-greiðslur og afskrifa óinnheimtanlegar kröfur.

## <a name="waiving-reinstating-or-reversing-interest-and-fees"></a>Niðurfelling, endurskipun eða bakfærsla á vöxtum eða gjöldum

Hægt er að fella niður, endurskipa eða bakfæra heilar vaxtanótur eða þóknanir og vexti á færslur sem eru hluti af vaxtanótum. Á flipanum **Innheimta** í aðgerðaglugganum á listasíðunni **Allir viðskiptavinir** velurðu **Vaxtanótu**, **Færsluvextir** eða **Þóknanir**.

Þessar leiðréttingar hafa aðeins áhrif á vaxtanótur, og vexti og gjöld sem þær hafa. Upplýsingar um hvernig á að afskrifa öll gjöld sem viðskiptavinur skuldar er að finna í hlutanum [Stofnun á afskriftarfærslum](#creating-write-off-transactions) í þessu efni.

Frekari upplýsingar, sjá Stofna vaxtakóða með sviði og Reikna vexti.

## <a name="creating-write-off-transactions"></a>Stofnun á afskriftafærslum

Hægt er að afskrifa tapaðar skuldir með því að velja **Afskrifa** á síðunni **Innheimta** og innheimtulistasíðum.

Þegar færslur eru afskrifaðar fyrir viðskiptavini, eru allar færslur fyrir þann viðskiptavin sjálfkrafa merktar til jöfnunar. Upphæð sem er afskrifuð fer eftir nettóupphæð merktra færslna. Afskriftarfærsla er stofnuð í færslubók og getur í mesta lagi innihaldið þrjá gerðir á færslubókarlínum:

- Fyrsta gerð færslubókarlínu inniheldur afskrift færslu viðskiptavinar. Ef merktar færslur innihalda margar samsetningar af gjaldmiðilskóðum, víddum og bókunarreglum, er aðskilin færslubókarlína stofnuð fyrir hverja samsetningu.
- Önnur gerð færslubókarlínu inniheldur fjárhagsfærslu afskriftar viðskiptavinar. Ef merktar færslur innihalda margar samsetningar af gjaldmiðilskóðum, víddum og bókunarreglum, er aðskilin færslubókarlína stofnuð fyrir hverja samsetningu.
- Þriðja gerð færslubókarlínu inniheldur upplýsingar um afskriftir fjárhags fyrir virðisaukaskatt. Færslubókarlínan er einungis stofnuð ef valkosturinn **Aðskilja virðisaukaskatt** er valin á síðunni **Færibreytur viðskiptakrafna**. Ef merktar færslur innihalda margar samsetningar af reikningum virðisauka, víddum og virðisaukakóðum er aðskilin færslubókarlína stofnuð fyrir hverja samsetningu. Afskriftarfærslan er búin til í færslugjaldmiðlinum. Nánari upplýsingar er að finna í Stofna afskriftabók fyrir viðskiptavin.

## <a name="process-nsf-payments"></a>Vinna úr NSF-greiðslum

Hægt er að vinna NSF-greiðslur með því að velja **NSF-greiðslu** á síðunni **Innheimtu**. Þegar þú velur þennan hnapp er hætt við greiðsluna. Ef NSF-þóknun á við um viðskiptamanninn er gjaldafærsla stofnuð í greiðslubók.. Upphæð þóknunarinnar er grundvölluð á stillingum fyrir sjálfvirk gjöld. Sjálfvirk gjöld sem notuð eru fyrir NSF-greiðslur eru tilgreind með gjaldaflokki sem er valinn á síðunni **Bankareikningar** fyrir bankareikninginn sem varð fyrir áhrifum.

## <a name="additional-resources"></a>Frekari upplýsingar

[Færibreytuuppsetning kreditstjórnunar viðskiptavina](./cm-credit-mgmt-setup.md)

[Uppsetningarupplýsingar kreditstjórnunar viðskiptavina](./cm-setup-information.md)

[Bæta við upplýsingum kreditstjórnunar fyrir viðskiptavin](./cm-add-credit-mgmt-information-customer.md)

[Lánaflokkar viðskiptavina](./cm-customer-credit-groups.md)

[Leiðréttingar á lánamörkum viðskiptavinar](./cm-credit-limit-adjustments.md)

[Kreditbið fyrir sölupantanir](./cm-sales-order-credit-holds.md)

[Regluleg verk viðskiptavinarlánastjórnunar](./cm-periodic-tasks.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]