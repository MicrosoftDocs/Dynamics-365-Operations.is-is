---
title: "Verkspár og fjárhagsáætlanir"
description: "Hægt er að hafa umsjón með og stjórna verkum í Microsoft Dynamics 365 for Finance and Operations með verkspám og fjárhagsáætlunum verks."
author: KimANelson
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ForecastModel, ProjYearEndProcess
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 23501
ms.assetid: 4e6d1384-19a2-4232-b3f3-d2590c218bd7
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: e31a013d6bf33b92b02bd9645a19380ba07f4a05
ms.contentlocale: is-is
ms.lasthandoff: 03/26/2018

---

# <a name="project-forecasts-and-budgets"></a>Verkspár og fjárhagsáætlanir

[!include [banner](../includes/banner.md)]

Tvær leiðir eru til að hafa umsjón með og stjórna verkum í Microsoft Dynamics 365 for Finance and Operations: verkspár og fjárhagsáætlanir verks. 

Hægt er að nota verkspá ef fyrirtækið hefur rekstraráætlanagerðar sjónarhorn og áherslu á tekjur og kostnaður sem er afleidd af tilteknar færslur. Hins vegar, ef fyrirtæki þitt leggur frekari áherslu á fjárhagslegar upphæðir, hægt er að nota fjárhagsáætlanir. 

Bæði verkspár og fjárhagsáætlanir notast við spálíkön til að halda utan um áætlaðar færsluupphæðir. 

Hvor aðferð hefur sína kosti. Eftirfarandi stig ætti að íhuga áður en greiðslumáti er valinn fyrir fyrirtækið.

|                           |                                          |                                                    |
|---------------------------|------------------------------------------|----------------------------------------------------|
|                           | **Verkspá**                  | **Fjárhagsáætlanir**                              |
| **Tímabilsúthlutun**     | Ekki er hægt að úthluta sérstaklega færslum yfir fjárhagstímabil. Í staðinn er spá og spástýring byggðar á líftíma verksins. Þar sem spár eru byggðar á tiltekinni dagsetningu, verður að áætla tímabilið út frá dagsetningu tímabilsins. | Hægt er að úthluta færslum yfir allt verkið eða yfir fjárhagstímabil. Ef úthlutað er yfir tímabil er hægt að flytja ónotaðar upphæðir áfram í næsta fjárhagstímabil. |
| **Að skoða færslur**  | Hægt er að skoða færslur í spá skjámyndinni, þar sem sjást spár fyrir allt fyrirtækið og°öll verk, án tillits til stigveldis. Til að leggja áherslu á tiltekið verk, þarf að sía gögnin.                                       | Hægt er að skoða áætlaðar færslur fyrir stigveldi eins verkefnis. Þess vegna er hægt að skoða færsluupplýsingar fyrir yfirverk eða undirverk þess.                 |
| **Færslubreytur** | Þegar færðar eru inn spáfærslur hægt er að nota hvert eigind sem er til staðar fyrir raunverulega færslu. Þetta gefur ítarlegri upplýsingar í spánni. Til dæmis er hægt að færa inn upplýsingar um magn, starfsmenn, atriði eða línueiginleika.         | Þegar færðar eru inn upplýsingar um fjárhagsáætlun, er hægt að nota aðeins upphæðir, tegundir og verkþætti.                    |
| **Öryggi**              | Spá er byggð á færslum sem eru færðar inn í skjámyndunum spár og felur í sér engin ferli fjárhagsáætlunarstýringar. Hvaða starfsmaður sem hefur heimild fyrir spáskjámynd getur endurskoða upplýsingarnar án samþykkis.                                        | Fjárhagsáætlun notar verkflæðiskerfi, sem styður breytingastjórnun og gerir þér kleift að vista sögu endurskoðana.         |
| **Færslugerð**           | Færslur spáfærslu byggjast á fjölda eininga og á kostnaði og verði sölueiningarinnar.  | Upplýsingar um fjárhagsáætlun eru byggðar á upphæðum sem er skipt á milli kostnaðar og tekna.                                          |
| **Spálíkön**       | Þar sem hver spá verður að vera tengd líkani, er hægt að stofna mörg spálíkön og einnig að setja upp undirlíkön.           | Fjárhagsáætlun verks takmarkar spálíkön sem notuð eru fyrir fjárhagsáætlanir. Færri spálíkön aðstoða við að auka samræmi í spám.                           |
| **Umframkostnaður**         | Aðeins er hægt að leyfa eða banna skráningu á færslum sem valda umframkostnaði.   | Fjárhagsáætlun verks veitir viðbótar stýringarvalkosti fyrir notendur. Hægt er að leyfa viðvaranir og að farið sé fram úr.                    |
| **Stýringar**               | Spástýring er framkvæmd með því að nota lækkun spár. Raunupphæðir eru dregnar frá spáfærslu stöðu án endurskoðunarslóðar. Þetta getur gert það erfiðara að rekja hvar raunverulegar færslur áttu sér stað.                   | Í fjárhagsáætlunarstýringu verks eru raunupphæðir dregnar frá upphæðum í eftirstöðvum fjárhagsáætlunar. Þetta gefur skýrari endurskoðunarslóð.                                   |

## <a name="project-forecasts"></a>Áætlanir verka
Þegar spá um verk er notuð, er hægt að færa spárfærslur í spárskjámyndiur fyrir hverja færslugerð. Hægt er að nota hvert eigind sem er tiltækt fyrir raunverulega spáfærslu; til dæmis arðsemisgreiningu línu, eigindir línu, starfsmenn eða lýsingar. Einnig er hægt að áætla hversu langt líður frá því þú stofnar til kostnaðar og þar til viðskiptavinur er reikningsfærður. 

Verkfærslur eftirspurnarspár eru byggð á einingum og upphæðir. 

Hver verkspá verður að vera tengd við spálíkan. Fyrir hverja spáfærslu sem er færð inn stingur kerfið sjálfkrafa upp á spálíkani. Spárlíkanið þjónar sem geymir fyrir spáfærslur. 

Hægt er að tilnefna spálíkön sem undirlíkön fyrir líkan. Þetta°gerir kleift að spá eftir svæði, tímabili eða deild. Hægt er að afrita spáfærslur í líkan til að stofna nýtt líkan, og einnig flytja færslurnar í fjárhag. Þar sem bein tengsl milli spá og líkan er hvert spálíkan hefur aðskilda fjárhagsáætlun verks. 

Spálíkön geta notað lækkun spár sem ferli fjárhagsáætlunarstýringar fyrir verk. Í lækkun spár lækka raunfærslur stöðu spáfærslna. Hins vegar, þar sem spárminnkun er beitt á efsta verkið í stigveldinu, veitir það takmarkaða yfirsýn yfir breytingar í spánni. T.d. ef starfsmaður er tengdur undirverk raunverulegar færslur starfsmanns eru bókaðar yfirverksins. Þess vegna getur verið erfitt að rekja breytingar því ekki er auðvelt að ákvarða hvaða færsla í hvaða undirverki olli lækkun spáupphæðar. Því er gott að°stofna afrit af spárlíkani fyrir lækkun spár til að nota. Síðan er hægt að nota skýrslur til að skoða hverju var upphaflega spáð. 

Verkspár er hægt að endurskoða, afrita, eyða eða flytja í fjárhagsáætlun. Samt sem áður er engin ferlisstýring. Allir starfsmenn með leyfi fyrir spáskjámynd geta gert breytingar án endurskoðunar.

-   **Endurskoða°** – hægt er að gera breytingar á spáfærslu í sömu skjámyndum þar sem upprunalegar færslur voru gerðar.
-   **Afrita eða eyða**°- þegar þú afritar spáfærsla afritarðu færslulínurnar af einu spárlíkani í annað spárlíkan. Þegar spá er eytt eyðirðu spárfærslum úr spárlíkaninu. Til að takmarka spárfærslurnar sem óskað er að afrita eða eyða, veljið sérstakar fæslugerðir og dagsetningar. Þannig°er hægt að afrita eða eyða tilgreindum hlutum í spá.
-   **Millifærsla** – Þegar þú flytur verkspá til fjárhagsáætlunarskýrsla, flytur þú spáfærslu af spárlíkani til fjárhagsáætlunarskýrslu. Hægt er að hnekkja öllum áður fluttum færslum í fjárhagsáætlunarskýrslunni sem þú vilt flytja verkspána til.

## <a name="project-budgets"></a>Fjárhagsáætlanir verka
Fjárhagsáætlun verks er einfaldari en spá, jafnvel þótt það samþætt spárlíkön. Það notar staka færslu í skjámynd fyrir upplýsingar um upprunalega fjárhagsáætlun og endurskoðun og leyfir spár sem eru byggðar á upphæð, tegund eða verkþætti. 

Í fjárhagsáætlun verks verður að senda allar upprunalegar fjárhagsáætlanir og endurskoðanir til verkflæðis verksins til samþykkis. Verkflæði veita aukna stjórn á ferlinu og stofna færslusögu breytinga. 

Fjárhagsáætlun verks svipar til almennrar fjárhagsáætlunar, en er hraðari og auðveldari í uppsetningu. Marga valkosti í almennri fjárhagsáætlunargerð, svo sem raðnúmer eða gjaldmiðil, þarf ekki að setja upp sér fyrir verk.

Fjárhagsáætlanir verks eru sjálfkrafa tengdar tveimur spálíkönum, einu fyrir upprunalega fjárhagsáætlun og einu fyrir eftirstöðvar fjárhagsáætlunar. Þess vegna geta skýrslur sem byggja á spálíkönum notast við fjárhagsáætlunargögn. Þegar verkáætlun er staðfest, stofnar kerfið spáfærslur byggðar á tengdum líkönum sem eru notaðar fyrir skýrslugerð og stýringu.

## <a name="forecast-models"></a>Spárlíkön
Spárlíkön hafa stigveldi í einu lagi. Þetta þýðir að hver verkspá verður að vera tengd við eitt spálíkan.

Ef þú notar verkspá getur þú auðkennt líkön sem undirlíkön. Síðan er hægt að stofna spá eftir deild, tímabili eða svæði. Til dæmis er hægt að stofna spálíkan fyrir ár og stofna síðan undirlíkön fyrir norðaustur-, suðaustur-, norðvestur- og suðvesturspásvæði fyrir upplýsingar sem eru sendar frá þeim svæðum. Með því að velja aðra valkosti í skýrslum í boði er hægt að skoða upplýsingar um heildarspá eða undirlíkanið.




