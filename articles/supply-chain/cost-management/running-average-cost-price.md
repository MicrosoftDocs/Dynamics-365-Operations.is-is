---
title: Um keyrslu á meðalkostnaðarverði
description: Birgðalokunarferlið jafnar úthreyfingafærslur við innhreyfingafærslur samkvæmt birgðamatsaðferð sem er valin í birgðalíkanaflokki vörunnar. Áður en birgðalokun er keyrð reiknar kerfið samt sem áður út hlaupandi meðalkostnaðarverð sem er í flestum tilvikum notað við bókun úthreyfingafærslna.
author: AndersGirke
ms.date: 02/02/2022
ms.topic: article
ms.search.form: InventModelGroup, InventOnhandItem, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.custom: 79003
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 871b3ffce45848f95d132eff3fd327295bc5084c
ms.sourcegitcommit: fefe93f3f44d8aa0b7e6d54cc4a3e5eca6e64feb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 02/04/2022
ms.locfileid: "8092190"
---
# <a name="running-average-cost-price"></a>Um keyrslu á meðalkostnaðarverði

[!include [banner](../includes/banner.md)]

Birgðalokunarferlið jafnar úthreyfingafærslur við innhreyfingafærslur samkvæmt birgðamatsaðferð sem er valin í birgðalíkanaflokki vörunnar. Áður en birgðalokun er keyrð reiknar kerfið samt sem áður út hlaupandi meðalkostnaðarverð sem er í flestum tilvikum notað við bókun úthreyfingafærslna.

Kerfið metur þetta meðalkostnaðarverð vöru með því að nota eftirfarandi formúlu:

Áætlað verð = (efnisleg upphæð + fjárhagsleg upphæð) / (efnislegt magn + fjárhagslegt magn)

## <a name="default-item-cost"></a>Sjálfgefinn vörukostnaður

Sjálfgefinn vörukostnaður fyrir útgefna vöru er hægt að stilla á einn af tveimur leiðum á **Gefnar út upplýsingar um vöru** síða:

- Búðu til staðlaðan kostnað með því að velja **Vöruverð** í **Settu upp** hópur á **Stjórna kostnaði** flipanum í aðgerðarrúðunni. Ef þú notar þessa aðferð verður þú að nota staðlaða kostnaðarútgáfu og kostnaðurinn verður að vera virkjaður.
- Skilgreindu sjálfgefið kostnaðarverð vöru fyrir útgefna vöru með því að slá inn gildi í **Verð** sviði á **Stjórna kostnaði** Flýtiflipi.

Auk þess að slá inn eða búa til verð geturðu valið **Notaðu nýjasta kostnaðarverðið** gátreitinn á **Stjórna kostnaði** Flýtiflipi á **Gefnar út upplýsingar um vöru** síðu. Í þessu tilviki mun kerfið sjálfkrafa uppfæra **Verð** reit þegar þú birtir fjárhagsuppfærslu. Til dæmis, ef þú bókar innkaupapöntunarreikning, verður reiturinn stilltur á innkaupaverðið frá þeim reikningi.

Ef þú ert með kostnaðarverð í virkri kostnaðarútgáfu og þú slærð inn verð á **Stjórna kostnaði** flýtiflipann mun kerfið nota verðið frá virku kostnaðarútgáfunni áður en það notar verðið sem er skilgreint á **Stjórna kostnaði** Flýtiflipi.

## <a name="using-the-running-average-cost-price"></a>Að nota meðalkostnaðarverð

Eftirfarandi tafla sýnir hvenær kerfið bókar birgðafærslur með því að nota meðalkostnaðarverð og hvenær kerfið notar kostnaðarverð sem er skilgreint í aðalfærslu vöru.

| Skilyrði | Kerfið notar áætlað meðalkostnaðarverð | Kerfið notar sjálfgefið kostnaðarverð vöru |
| --- | --- | --- |
| Bæði teljari\* og nefnari\*\* eru jákvæðir. | Já | Nr. |
| Teljarinn\*, nefnarinn\*\* eða hvorir tveggja eru neikvæðir. | Nei | Já |
| Nefnarinn\*\* er 0 (núll). | Nei | Já |

\* Teljari = (Líkamleg upphæð + Fjárhæð)  
\*\* Nefnari = (Líkamlegt magn + fjárhagslegt magn)

> [!NOTE]
> Ef **Taktu með líkamlegt gildi** valmöguleikinn er ekki valinn fyrir vöru, kerfið notar 0 (núll) fyrir bæði efnislega magnið og líkamlegt magn. Sjá upplýsingar um þennan valkost í [Taka með efnislegt virði](include-physical-value.md).

## <a name="avoiding-pricing-amplification"></a>Að forðast verðmögnun

Af og til verðleggur kerfið margar úthreyfingar áður en nægilega margar innhreyfingar eru komnar sem byggja má verð á. Þær aðstæður geta valdið ofmati á hlaupandi meðaltali kostnaðarverðs. Þó eru ráðstafanir sem má gera til að forðast vandamálið eða minnka áhrif þess ef það kemur upp.

**Atburðarás:** Eftirfarandi færslur eiga sér stað fyrir vöru sem þú hefur valið **Taktu með líkamlegt gildi** valkostur fyrir:

1. Fjárhagslegt móttökumagn er 100 á USD 100,00.
2. Fjárhagsleg úthreyfingamagn er 200.
3. Raunverulegt móttökumagn er 101 á USD 202,00.

Þegar skoðað er áætlað meðalkostnaðarverð vörunnar er búist við kostnaðarverðinu USD 1,51. Í staðinn finnurðu áætlað hlaupandi meðaltal USD 102.00, sem byggir á eftirfarandi formúlu:

Ásett verð =\[ 202 + (-100)\] ÷\[ 101 + (-100)\] = 102 ÷ 1 = 102

Þessi verðmögnun á sér stað vegna þess að þegar 200 vörur eru gefnar út fjárhagslega í skrefi 2 verður kerfið að verðleggja 100 af hlutunum áður en það hefur samsvarandi kvittanir. Þessar aðstæður orsaka neikvæðar birgðir. Kerfið áætlar síðan einingaverðið USD 1.00, eins og þú gætir búist við. Hins vegar þegar samsvarandi 100 innhreyfingar koma, eru þær á einingarverðinu USD 2,00 hver.

> [!NOTE]
> Þó útgáfurnar skapi neikvæðar birgðir eru birgðir jákvæðar þegar útgáfuverðið er reiknað. Þess vegna er meðalkostnaðarverð notað í staðinn fyrir verð í aðalvörufærslunni. Þegar hér er komið hefur kerfið birgðavirðisjöfnun sem er USD 100,00. Þrátt fyrir að þessi offset hafi verið byggð upp yfir 100 stykki, þar sem var einingajöfnun upp á USD 1.00 hvert, hefurðu nú aðeins eitt stykki í birgðum. Þess vegna er jöfnuðu tapi upp á USD 100,00 er úthlutað á þetta eina stykki. Niðurstaðan er ofhækkun á áætluðu kostnaðarverði.
>
> Til samanburðar, taktu eftir því að ef skrefum 2 og 3 er snúið við í atburðarásinni, verða 200 hlutir gefnir út á einingarverðinu USD 1.51, og eitt stykki verður eftir á einingarverðinu USD 1.51. Þar sem þetta verðmögnunartilfelli getur komið upp þegar um neikvæðar birgðir er að ræða er erfitt að forðast eftirfarandi tilfelli:
>
> - Meta verður úthreyfingaverð á lagerbirgðavirði og magni.
> - Leiðrétta verður virði lagerbirgða og magn á út- og innhreyfingum.
> - Viðskiptalíkanið leyfir útsendingu eða verðlagningu fleiri stykkja en eru fyrir hendi.
> - Samþykkja verður allt innhreyfingarvirði og magn sem er sent.

Samt sem áður, ef viðskiptalíkanið leyfir eftirfarandi venjur geta þær hjálpað til við að forðast neikvætt magn sem getur skapað verðmögnun:

- Ef þú velur **Taktu með líkamlegt gildi** valmöguleika fyrir hlut, hreinsaðu **Líkamleg neikvæð birgðastaða** gátreitinn á **Vörulíkanaflokkar** síðu.
- Ef **ekki** er valinn valkosturinn **Taka með efnislegt virði** fyrir vöru, skal hreinsa valkostinn **Fjárhagslega neikvæðar birgðir** á síðunni **Vörulíkanaflokkar**.

Hafið einnig í huga að hámarksjöfnunin á efnislegu birgðavirði er takmörkuð af fjölda efnislegra færslna og mismun milli efnislegs og fjárhagslegs verðs. Svo lengi sem allar efnislegar færslur eru að lokum uppfærðar fjárhagslega getur efnislegt virði ekki hækkað óstjórnlega. Að lokum skal minnt á að mögnunaráhrifin minnka verulega þegar samanlagða jöfnunin dreifist á nokkur stykki í lagerbirgðum en ekki bara eitt.

## <a name="avoid-a-zero-cost-price-on-issues"></a>Forðastu núll kostnaðarverð á útgáfum

Þegar **Taktu með líkamlegt gildi** valkostur er ekki valinn á **Vörulíkanahópur** síðu getur útgáfa úr birgðum haft núll kostnaðarverð ef engar fjárhagslega uppfærðar kvittanir eru í birgðum. Til að forðast þessa atburðarás skaltu íhuga eftirfarandi valkosti:

- Veldu **Taktu með líkamlegt gildi** valmöguleika á **Vörulíkanahópur** síðu. Þessi valkostur kemur í veg fyrir núllkostnaðarverð á útgáfu, að því tilskildu að kvittunin sé líkamlega uppfærð. Ef þú leyfir ekki neikvæðar efnislegar birgðir munu vandamál reikna hlaupandi meðaltal út frá líkamlega uppfærðum færslum.
- Búðu til sjálfgefið kostnaðarverð vöru með því að virkja kostnaðarútgáfu sem hefur staðlaðan kostnað, eða sláðu inn verðið á **Stjórna kostnaði** Flýtiflipi á **Gefnar út upplýsingar um vöru** síðu. Þessi valkostur er bestur þegar **Taktu með líkamlegt gildi** valkostur er ekki valinn á **Vörulíkanahópur** síðu, vegna þess að kerfið mun alltaf hafa varaverð til að nota.
- Veldu **Notaðu nýjasta kostnaðarverðið** valmöguleika á **Stjórna kostnaði** Flýtiflipi á **Gefnar út upplýsingar um vöru** síðu. Þessi valkostur mun halda **Verð** reitinn uppfærður í hvert skipti sem þú uppfærir kvittun fjárhagslega. Ef þú velur þennan valmöguleika, en þú slærð ekki inn sjálfgefið verð eða virkjar kostnað í hefðbundinni kostnaðarútgáfu, geturðu samt haft núll kostnað fyrir mál.

Ef þú ert með útgáfuviðskipti sem hafa engan kostnað, þá *Birgðalokun og aðlögun* ferli mun leiðrétta kostnaðarverðið með því að búa til leiðréttingu eftir að innhreyfingar eru fjárhagslega uppfærðar. Hafðu í huga að fjárhagstímabilið þegar þessi uppfærsla á sér stað gæti verið frábrugðið fjárhagstímabilinu þegar hlutirnir voru líkamlega mótteknir eða gefnir út.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
