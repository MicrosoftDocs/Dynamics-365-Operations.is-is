---
title: Bókun framleiðslupöntunar
description: Þessi grein veitir upplýsingar um mismunandi gerðir framleiðslupöntunarbókunar.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventItemGroup, ProdGroup, WrkCtrTable, WrkCtrResourceGroup, ProjCategory, CostSheetDesigner
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: d41725325a82b24c1e5aa6bd2c1a5322f3078ace
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879625"
---
# <a name="production-postings"></a>Framleiðslupóstar

Þessi grein veitir upplýsingar um mismunandi tegundir bókana í framleiðslupöntunarferlinu.


## <a name="material-consumption"></a>Efnisnotkun

Efni eru skráðar sem notuð í framleiðslu þegar tiltektarlisti framleiðslubókar er bókuð. Þetta skapar færslur sem draga frá lagerbirgðum. Í **Framleiðslubreytur**, er hægt að tilgreina hvort verðmæti hráefna sem eru í vinnslu (kallað WIP), eigi að bóka í fjárhag.

Verðmæti hráefna sem eru í vinnslu (WIP) er bókað á **Áætlaður kostnaður við neytt efnis** og **Áætlaður kostnaður við neytt efnis, WIP** reikningar. Tínslulistaferlið fyrir framleiðslupöntunina er efnisleg uppfærsla á birgðafærslum sem tengjast framleiðslupöntuninni. Þegar framleiðslupöntun er skráð sem lokið, eru efnisfærslur bakfærðar og tengdar birgðafærslur uppfærðar fjárhagslega. Þegar lokadagbókin er birt, er **Kostnaður við neytt efnis** og **Kostnaður við neytt efnis, WIP** færslugerðir eru notaðar.

The **Framleiðsla** flipann á **Skráningarsnið** síða stjórnar því hvernig framleiðslupantanir bókast í fjárhag. Þetta er notað þegar **Fjárhagsbókun** reiturinn er stilltur á annað hvort **Hlutur og auðlind** eða **Atriði og flokkur** á **Framleiðslustýringarbreytur** síðu. 

Til að færslubók tínslulista geti bókað í aðalbók fyrir framleiðslupöntun, verða eftirfarandi skilyrði að vera uppfyllt:

-   The **Bókaðu tínslulista í höfuðbók** gátreitinn verður að vera valinn á **Framleiðslustýringarbreytur** síðu. Hægt er að hnekkja þessari stillingu fyrir tiltekna síðu á **Framleiðslustýringarbreytur eftir stöðum** síðu.
-   The **Bókaðu efnislegar birgðir** gátreitinn verður að vera valinn á **Vörulíkanaflokkar** síðu fyrir vöruna sem valin er í innkaupapöntunarlínunni.
-   Helstu reikningar verða að vera tilgreindir á **Birgðafærslusnið** síðu fyrir eftirfarandi birtingargerðir:
    -   **Áætlaður kostnaður við notað efni**
    -   **Áætlaður kostnaður við notað efni, VÍV**

## <a name="time-consumption"></a>Tímanotkun

Tíminn sem starfsmenn eyða í framleiðslustörf er skráður í **Dagbók leiðarkorts** eða the **Dagbók vinnukorta**. Þegar þessar færslubækur eru bókaðar er reikningsbókun fjárhagsbókar á sérstakan reikning fyrir tilföng sem eru í vinnslu (WIP) unnin. Þessi bókun sýnir virði tímans sem er varið í framleiðslupöntun. Eftir að framleiðslupöntunin er skráð sem lokið, er vív-lyklar eru jafnaðir.

Það eru þrjár mögulegar leiðir til að bóka tímanotkun eftir því hvaða valkostur er valinn í **Fjárhagsbókun** sviði á **Framleiðslustýringarbreytur** síðu.

## <a name="reporting-finished-goods-and-error-quantities"></a>Tilkynni um Fullbúnar vörur og villumagn

Þegar framleiðslupöntun er **Tilkynnt sem lokið**, fullunnar vörur sem hafa verið fullgerðar eru uppfærðar í birgðum í gegnum **Tilkynna sem lokið** dagbók. Ef þú ert að nota WIP bókhald er fjárhagsbók bókuð til að minnka WIP reikningana og auka birgðir fullunnar vöru. Dagbókin notar staðalkostnaðinn sem hefur verið skilgreindur fyrir vöruna. Ef **Notið áætlað kostnaðarverð** valkostur er valinn á **Framleiðslustýringarbreytur** síðu verður áætlaður kostnaður úr framleiðslupöntuninni notaður.

Verðmæti hráefna sem eru í vinnslu (WIP) er bókað á **Áætlaður framleiddur kostnaður** og **Áætlaður framleiðslukostnaður, WIP** reikningar. The **Tilkynna sem lokið** ferli fyrir framleiðslupöntun er efnisleg uppfærsla á birgðafærslum sem tengjast framleiðslupöntuninni. Þegar framleiðslupöntun er lokið, eru efnisfærslur bakfærðar og tengdar birgðafærslur uppfærðar fjárhagslega. Þegar lokadagbókin er birt, er **Framleiðslukostnaður** og **Framleiðslukostnaður, WIP** færslugerðir eru notaðar.

The **Framleiðsla** flipann á **Skráningarsnið** síða er notuð til að stjórna því hvernig framleiðslupantanir verða bókaðar í fjárhag. Þetta er notað þegar **Fjárhagsbókun** reiturinn er stilltur á annað hvort **Hlutur og auðlind** eða **Atriði og flokkur** á **Framleiðslustýringarbreytur** síðu. The **Fjárhagsvörur** Flýtiflipi á **Framleiðsluhópar** síðu er einnig hægt að nota til að stjórna bókun fyrir framleiðslupantanir þegar reiturinn er stilltur á **Framleiðsluhópar**.

Fyrir **Tilkynna sem lokið** færslubók til að bóka í aðalbók fyrir framleiðslupöntun, þarf að uppfylla eftirfarandi skilyrði:
-   The **Bóka skýrslu sem lokið í fjárhagsbók** gátreitinn verður að vera valinn í **Framleiðslustýringarbreytur** síðu. Hægt er að hnekkja þessari stillingu fyrir tiltekna síðu á **Framleiðslustýringarbreytur eftir stöðum** síðu.
-   The **Bókaðu efnislegar birgðir** gátreitinn verður að vera valinn á **Vörulíkanaflokkar** síðu fyrir vöruna sem valin er í innkaupapöntunarlínunni.
-   Helstu reikningar verða að vera tilgreindir í **Birgðafærslusnið** síðu fyrir eftirfarandi birtingargerðir:
    -   **Áætlaður kostnaður við framleiðslu**
    -   **Áætlaður kostnaður við framleiðslu, VÍV**

## <a name="ending-the-production-order"></a>Lokið við framleiðslupöntunina

Áður en framleiðslupöntun er lokið er raunkostnaður reiknaður fyrir framleitt magn. Allur áætlaður kostnaður fyrir efni, vinnu og rekstrarkostnaði er bakfærður og skipt út fyrir raunkostnað. Heildarkostnaður fullunnar vöru er skuldfærður af **Framleiðslukostnaður** reikning og færð inn á **Framleiðslukostnaður, WIP** reikning. Efnin sem voru notuð í framleiðslupöntuninni eru færð inn á **Kostnaður við neytt efnis** og skuldfærður á **Efniskostnaður, WIP** reikning.

Ef þú velur **Loka starfi** gátreitinn þegar þú keyrir kostnaðarútreikninginn er stöðu framleiðslupöntunarinnar breytt í **Lokað**. Þessi staða kemur í veg fyrir aukalegan kostnað sé óvart bókaður á lokna framleiðslupöntun. Hægt er að tilgreina að verðmæti villumagna sem er tilkynnt sem lokið skuli úthlutað á vörumagnið sem er tilkynnt sem lokið. Að öðrum kosti er hægt að tilgreina að verðmæti villumagna sé bókað á sérstakan ruslreikning. 

Til að tilgreina tiltekinn ruslreikning skaltu fylgja þessum skrefum:
1.  Fara til **Framleiðslueftirlit** > **Uppsetning** > **Framleiðslustýringarbreytur**.
2.  Veldu **Hefðbundin uppfærsla** flipa.
3.  Í **Skrappaðferð** reit, veldu **Skrappreikningur**.
4.  Í **Skrappreikningur** reit, veldu aðalreikninginn þar sem rusl fyrir villumagn á að bóka þegar framleiðslupöntun er lokið. Til dæmis, veldu kostnaðarreikning eins og 510380: Framleiðsluúrgangur.

Til að lokabókin geti bókað í aðalbók fyrir framleiðslupöntun verða eftirfarandi skilyrði að vera uppfyllt:
-   Helstu reikningar verða að vera tilgreindir í **Birgðafærslusnið** eða **Framleiðsluhópar** síðu fyrir eftirfarandi birtingargerðir:
    -   **Kostnaður við notað efni**
    -   **Kostnaður við notað efni, VÍV**
    -   **Kostnaður við framleiðslu**
    -   **Kostnaður við framleiðslu, VÍV**
-   Helstu reikningar verða að vera tilgreindir í **Kostnaðarflokkar**, **·**, eða **Auðlindahópar** síðu fyrir eftirfarandi tegundir:
    -   **Framleiddur kostnaður frásogaður**
    -   **Kostnaður við notaða framleiðslu, VÍV**

## <a name="indirect-costs-for-production-orders"></a>Óbeinn kostnaður vegna framleiðslupantana

Þegar þú vinnur færslur fyrir framleiðslupöntun er hægt að stilla óbeinan kostnað til að fanga kostnaðarkostnað eða viðbótargjöld í fjárhag. Líkamlegar færslur fyrir óbeinan kostnað eru færðar í birgðum þegar þú bókar tínslulistabók eða skýrslu sem lokið færslubók. Fjármagnsfærslur fyrir óbeinan kostnað eru færðar í birgðum þegar þú bókar lokabók.

Þú getur greint óbeinan kostnað á tímanotkun þinni sem tengist **Leiðarkort** tímarit eða **Atvinnukort** tímaritum. Þessar færslur eru bakfærðar og bókaðar í fjárhagslykla þegar framleiðslupöntuninni er lokið. Fyrir frekari upplýsingar, farðu á [Kostnaðarblöð](/supply-chain/cost-management/costing-sheets.md).

## <a name="controlling-the-level-of-ledger-posting"></a>Stýra stigi fjárhagsbókunar

Á **Framleiðslustýringarbreytur** síðu geturðu notað **Fjárhagsbókun** reit til að stilla magn fjárhagsbókunar fyrir framleiðsluferli. 

Eftirfarandi reitir eru tiltækir:

### <a name="item-and-resource"></a>Vara og tilföng

Þegar þú velur **Hlutur og auðlind** valmöguleika í **Fjárhagsbókun** reit, þá koma bókunarreikningarnir frá tilfangi eða tilfangahópi á rekstri á leiðinni. Reikningar á tilteknu tilfangi verða fyrsti færslumöguleikinn. Ef reikningur er ekki tilgreindur verða reikningarnir sem tilgreindir eru í tilfangahópnum notaðir. Hver aðgerðalína í leið getur haft eina tilföng sem tilgreind er sem **Kostnaðarúrræði**. Þetta tilfang er notað til að ákvarða reikninginn sem á að nota. Þessi valkostur er almennt notaður þegar fyrirtæki úthlutar rekstrarkostnaði á tilföngin. Kostnaður er oft hærri fyrir auðlindirnar og er notaður til að hjálpa til við að taka "taka á móti kaupa" ákvarðanir. Þetta er ítarlegasta færslustillingin og gerir nákvæmustu stjórn á færslunum og mjög nákvæma greiningu á framleiðsluferlinu.

### <a name="item-and-category"></a>Vara og tegund

Þegar þú velur **Atriði og flokkur** valmöguleika í **Fjárhagsbókun** reit, munu bókunarreikningarnir koma frá **Kostnaðarflokkur** síðu sem tengist hverri línu á leiðinni. Hver rekstrarlína á leiðinni getur haft þrjá kostnaðarflokka: **Uppsetning** tími, **Hlaupa** tíma, og **Magn**. Þessi valkostur er almennt notaður þegar aðaláhersla fyrirtækis þíns er á skilvirkni ferlis og lengd virkni. Þessi valkostur er ítarlegri leið til að birta færslur og gefur samt leið til að flokka kostnað í flokka.

### <a name="production-group"></a>Framleiðsluflokkur

Þegar þú velur **Framleiðsluhópar** valmöguleika í **Fjárhagsbókun** reit koma bókunarreikningarnir frá **Framleiðsluhópar** síðu. **Framleiðsluhópar** eru venjulega notuð þegar fleiri en ein framleiðslulína keyrir svipaðar vörur eða hefur svipaðan búnað. Þú getur notað þennan valkost til að bera saman kostnað á milli tveggja mismunandi framleiðsluhópa.  
  
> [!NOTE]
> Ef stöðluð aðferð við útreikning á kostnaði við fullunna vöru er notuð munu lokafærslur endurspegla það. Ef raunkostnaður og kostnaður sem er reiknaður með stöðluðu aðferðinni er ólíkur eru mismunirnir færðir á reikninginn sem sýnir hagnað eða tap.

### <a name="route-groups-and-ledger-posting"></a>Leiðarhópar og bókhaldsbókun

Hver aðgerðalína á leið hefur a **Leiðarhópur** tilgreint. The **Uppsetningartími**, **·**, og **Magn** sviðum á **Leiðarhópur** í **Áætlun og kostnaður** hópur eru notaðir til að stýra því hvort tíminn verði notaður í kostnaðarreikning við bókun a **Atvinnukort** eða **Dagbók leiðarkorts** á framleiðslupöntuninni. Ef valmöguleikarnir eru óvirkir verður fylgiskjal ekki stofnað í fjárhag fyrir tímanotkunina.

Fyrir **Leiðarkort** eða **Dagbók vinnukorta** til að bóka í aðalbók fyrir framleiðslupöntun verða eftirfarandi skilyrði að vera uppfyllt:

-   The **Uppsetningartími**, **eða** **Magn** reitinn verður að vera valinn í **Áætlun og kostnaður** hópur á **Leiðarhópur** síðu.
-   Helstu reikningar verða að vera tilgreindir í annaðhvort **Kostnaðarflokkur**, **·**, **·**, eða **Framleiðsluhópar** síðu fyrir eftirfarandi birtingargerðir:
    -   Áætlaður notaður framleiðslukostnaður
    -   Áætlaður kostnaður við notaða framleiðslu, VÍV

Eftirfarandi skýringarmynd sýnir tengsl leiðahópsins við útreikning á heildarkostnaði fyrir hverja aðgerð (leiðarlínu) á tiltekinni leið. Hver leiðarlína hefur einn leiðarhóp. Leiðarhópurinn stjórnar breytum fyrir uppsetningartíma, keyrslutíma og magn. The **Kostnaðarflokkur** flipinn hefur þrjá valkosti fyrir **Uppsetning**, **·**, og **Magn** sem eru virkjuð á grundvelli stillingar leiðarhópa. The **Tímasetningar** Hraðflipi hefur þrjá reiti sem eru byggðir á leiðarhópnum.

Formúlan sem er notuð byggist á því hvort valmöguleikinn sé virkur í leiðarhópnum. Kostnaður úr völdum kostnaðarflokki er margfaldaður með magninu sem var slegið inn í tímasetningar til að reikna út heildarkostnað.

:::image type="complex" source="media/RouteGroupRelationship.png" alt-text="Tengsl leiðahópa við reiknaðan heildarkostnað.":::
Tengsl leiðahópa við reiknaðan heildarkostnað. Hver leiðarlína hefur einn leiðarhóp. Leiðarhópurinn stjórnar breytum fyrir uppsetningartíma, keyrslutíma og magn. Kostnaðarflokkaflipinn hefur þrjá valkosti fyrir uppsetningu, keyrslu og magn sem eru virkjaðir út frá stillingum leiðarhópa. Tímasetningar flýtiflipinn hefur þrjá reiti sem eru virkjaðir og kostnaðarverð miðað við leiðarhópinn. Formúlan sem er notuð byggist á því hvort valmöguleikinn er virkur í leiðarhópnum. Kostnaður úr völdum kostnaðarflokki er margfaldaður með magninu sem er slegið inn í tímasetningar til að reikna út heildarkostnað.
:::image-end:::

## <a name="sample-posting-profile-configuration"></a>Dæmi um stillingar fyrir færslusnið

Eftirfarandi tafla sýnir dæmi um sjálfgefnar bókunargerðir með sýnishorn af aðalreikningum og lýsingum. 

 - The **Debet/kredit** dálkurinn gefur til kynna hvort færslan er venjulega debet eða inneign, eða í sumum tilfellum getur hún bókað annað hvort. 
 - The **Hreinsunarreikningur** dálkurinn gefur til kynna hvort bókunartegundin sé jöfnunarreikningur. Upphæðin sem er bókuð á þessum reikningi er sjálfkrafa bakfærð þegar síðari færsla er bókuð. 
 - The **P/F** dálkur gefur til kynna **P** fyrir líkamlega færslu og **F** fyrir fjárhagslega færslu. 
 - The **Fylgja** dálkur gefur til kynna hvort aðalreikningur tiltekinnar færslutegundar sé venjulega sá sami og annarri færslutegund. Gildið í dálknum gefur til kynna færslugerðina sem venjulega er fylgt eftir.

> [!NOTE]
> Aðalreikningar og heiti aðalreikninga eru tillögur. Við mælum með því að þú vinnur með endurskoðanda þínum til að ákvarða bestu uppsetninguna fyrir fyrirtækisþarfir þínar.


| Bókunargerð  | Dæmi um aðalreikning | Dæmi um nafn aðalreiknings| Lykilgerð | Debet/kredit? | Millireikningur | Líkamlegt eða fjárhagslegt | Fylgja | Lýsing |
|---------------|----------------------|--------------------------|--------------|----------------|------------------|-----------------------|--------|------------|
| Áætlaður kostnaður við notað efni      | 140100               | Efnisskrá        | Eign        | Kredit         | Y                | P                     | Kostnaður við notað efni                | Þessi reikningur er notaður þegar þú bókar tínslulistabók fyrir framleiðslupöntun. Mótið á þennan reikning er áætlaður efniskostnaður, WIP. Upphæðin á þessum reikningi er sjálfkrafa bakfærð þegar framleiðslupöntun er lokið. Þessi reikningur táknar birgðareikning í efnahagsreikningi.       |
| Áætlaður kostnaður við notað efni, VÍV | 150150               | Framleiðslu WIP - Efni | Eign        | Debet          | Y                | P                     | Áætlaður kostnaður við framleiðslu, VÍV          | Þessi reikningur er notaður þegar þú bókar tínslulistabók fyrir framleiðslupöntun. Jöfnun á þennan reikning er áætlaður kostnaður við neytt efnis. Upphæðin á þessum reikningi er sjálfkrafa bakfærð þegar framleiðslupöntun er lokið. Þessi reikningur táknar WIP í efnahagsreikningi þínum.                  |
| Áætlaður kostnaður við framleiðslu               | 140200               | Birgðir fullunnar vörur   | Eign        | Debet          | Y                | P                     | Kostnaður við framleiðslu                         | Þessi reikningur er notaður þegar þú bókar skýrslu sem lokið færslubók fyrir framleiðslupöntun. Jöfnun á þennan reikning er áætlaður framleiddur kostnaður, WIP. Upphæðin á þessum reikningi er sjálfkrafa bakfærð þegar framleiðslupöntun er lokið. Þessi reikningur táknar birgðareikning í efnahagsreikningi. |
| Áætlaður kostnaður við framleiðslu, VÍV          | 150150               | Framleiðslu WIP - Efni | Eign        | Kredit         | Y                | P                     | Kostnaður við framleiðslu, VÍV                    | Þessi reikningur er notaður þegar þú bókar skýrslu sem lokið færslubók fyrir framleiðslupöntun. Jöfnun á þennan reikning er áætlaður framleiddur kostnaður. Upphæðin á þessum reikningi er sjálfkrafa bakfærð þegar framleiðslupöntun er lokið. Þessi reikningur táknar WIP í efnahagsreikningi þínum.                     |
| Kostnaður við notað efni                | 140100               | Efnisskrá        | Eign        | Kredit         | N                 | F                     | Áætlaður kostnaður við notað efni      | Þessi reikningur er notaður til að bera kennsl á efnin sem eru notuð í framleiðslupöntuninni meðan á lokaferlinu stendur. Jöfnun á þennan reikning er kostnaður við neytt efni, WIP.                                                                                                    |
| Kostnaður við notað efni, VÍV           | 150150               | Framleiðslu WIP - Efni | Eign        | Debet          | N                 | F                     | Áætlaður kostnaður við notað efni, VÍV | Þessi reikningur er notaður til að bera kennsl á efnin í WIP sem eru notuð í framleiðslupöntuninni meðan á lokaferlinu stendur. Jöfnun á þennan reikning er kostnaður við neytt efni.                                                |
| Kostnaður við framleiðslu                         | 140200               | Birgðir fullunnar vörur   | Eign        | Debet          | N                 | F                     | Áætlaður kostnaður við framleiðslu               | Þessi reikningur er notaður til að greina kostnað fullunnar vöru sem er framleidd af framleiðslupöntun þegar framleiðslupöntuninni er lokið. Jöfnun á þennan reikning er framleiddur kostnaður, WIP reikningur.                                                                  |
| Kostnaður við framleiðslu, VÍV                    | 150150               | Framleiðslu WIP - Efni | Eign        | Kredit         | N                 | F                     | Áætlaður kostnaður við framleiðslu, VÍV          | Þessi reikningur er notaður til að greina kostnað fullunnar vöru í WIP sem er framleidd af framleiðslupöntun þegar framleiðslupöntuninni er lokið. Mótið á þennan reikning er framleiddur kostnaðarreikningur.                                     |

> [!NOTE]
> The **Lean þjónustu WIP kvittun** og **Lean þjónusta WIP hreinsunarreikningur** eru notaðar með bakflæðiskostnaði fyrir lean framleiðslu. Fyrir frekari upplýsingar, farðu á [Backflush kostnaður](/supply-chain/cost-management/backflush-costing.md).

