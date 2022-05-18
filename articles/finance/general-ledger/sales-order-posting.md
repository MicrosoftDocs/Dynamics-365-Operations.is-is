---
title: Bókun sölupöntunar
description: Þetta efni veitir upplýsingar um flipann Sölupöntun á prófílsíðu birgðabókunar.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventItemGroup
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: 5d84723b51d6977867fa162c4a47befa61bd9ef6
ms.sourcegitcommit: dc3053625dfe24aef64399dd1d002214e7f7619f
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/13/2022
ms.locfileid: "8755929"
---
# <a name="sales-order-posting"></a>Bókun sölupöntunar

The **Sölupöntun** flipann á **Birgðafærslusnið** síða er notuð til að stjórna því hvernig sölupantanir verða bókaðar í fjárhag. Tvær meginaðgerðir eru bókaðar í fjárhag fyrir sölupöntun: 

- Fylgiseðill
- Reikningur

Til að efnisleg færsla (fylgiseðill) geti bókað í aðalbók fyrir sölupöntun, verða að uppfylla eftirfarandi skilyrði:

- Á **Birgða- og vöruhúsastjórnunarfæribreytur** síðu, the **Bókaðu fylgiseðil í höfuðbók** gátreit verður að vera valinn.
- Á **Vörulíkanahópur** síðu fyrir vöruna sem valin er í sölupöntunarlínunni, the **Bókaðu efnislegar birgðir í höfuðbók** gátreit verður að vera valinn.
- Á **Birgðafærslusnið** síðu verður að tilgreina aðalreikninga fyrir eftirfarandi færslugerðir:
  - Kostnaður afhentra eininga
  - Kostnaður seldra og afhentra vara

Til þess að fjárhagsfærsla (reikningur) geti bókað í aðalbók fyrir sölupöntun verða eftirfarandi skilyrði að vera uppfyllt:

- Á **Vörulíkanahópur** síðu fyrir vöruna sem valin er í sölupöntunarlínunni, the **Bókaðu fjárhagsbirgðir í höfuðbók** gátreit verður að vera valinn.
- Helstu reikningar verða að vera tilgreindir á **Birgðafærslusnið** síðu fyrir eftirfarandi birtingargerðir:
  - Reikningsfærður kostnaður eininga
  - Reikningsfærður kostnaður seldra vara
  - Tekjur
  - Afsláttur\*

> [!NOTE]
> Afsláttarreikningurinn er valfrjáls. Margar bókhaldsreglur, svo sem reikningsskilareglur og IFRS, krefjast þess að afslættir dragi úr sölutekjum og því eru þessir reikningar ekki notaðir í mörgum tilfellum. Ef staðbundnar reglur leyfa, notaðu sérstakan aðalreikning til að bóka þann hluta söluverðs sem er afsláttur.

Til að bóka frestað (áætlað) tekjuvirði í fjárhag þegar þú býrð til fylgiseðil fyrir sölupöntun, verður að uppfylla eftirfarandi skilyrði:

- Á **Vörulíkanahópur** síðu fyrir vöruna sem valin er í sölupöntunarlínunni, the **Bókaðu efnislegar birgðir í höfuðbók** gátreit verður að vera valinn.
- Á **Vörulíkanahópur** síðu, the **Bóka á frestað tekjureikning við afhendingu sölu** gátreit verður að vera valinn.
- Á **Birgða- og vöruhúsastjórnunarfæribreytur** síðu., the **Bókaðu fylgiseðil í höfuðbók** gátreit verður að vera valinn.
- Á **Birgða- og vöruhúsastjórnunarfæribreytur** síðu, the **Bókaðu líkamlegan söluskatt** gátreit verður að vera valinn.
- Á **Færibreytur viðskiptakrafna** síðu, the **Bókaðu fylgiseðil í höfuðbók** gátreit verður að vera valinn.
- Á **Birgðafærslusnið** síðu verður að tilgreina aðalreikninga fyrir eftirfarandi færslugerðir:
  - Frestaðar tekjur við afhendingu
  - Frestaðar tekjur mótbókfærðar við afhendingu
  - Frestaður virðisaukaskattur við afhendingu

> [!NOTE]
> Við mælum almennt með því að þú virkir valkostina **Bókaðu efnislegar birgðir** og **Bókaðu fylgiseðil í höfuðbók**. Að virkja þessa valkosti getur hjálpað til við að flýta fyrir lokunarferli mánaðarins, því engar frestun þarf að vera handvirkt reiknuð og bókuð. Að auki mun reikningsskil endurspegla frestuðu upphæðirnar sjálfkrafa án handvirkrar inngrips.

> [!IMPORTANT]
> The **Bóka á frestað tekjureikning við afhendingu sölu** valkosturinn er ekki notaður við tekjufærslu. Fyrir frekari upplýsingar um tekjufærslu, farðu á [Tekjuskráningaryfirlit](/accounts-receivable/revenue-recognition-overview.md)

## <a name="sample-posting-profile-configuration"></a>Dæmi um stillingar fyrir færslusnið 

Eftirfarandi tafla sýnir dæmi um sjálfgefnar bókunargerðir með sýnishorn af aðalreikningum og lýsingum:
 
- The **Hreinsun reiknings** dálkurinn gefur til kynna að bókunartegundin sé jöfnunarreikningur. Upphæðin sem er bókuð á þessum reikningi er sjálfkrafa bakfærð þegar síðari færsla er bókuð. 
- The **P/F** dálkur gefur til kynna **P** fyrir líkamlega færslu og **F** fyrir fjárhagslega færslu. 
- The **Fylgja** dálkurinn gefur til kynna hvort aðalreikningur tiltekinnar færslutegundar sé venjulega sá sami og annarri færslutegund. Gildið í dálknum gefur til kynna tegund færslu sem er venjulega notuð.

> [!NOTE]
> Þessir aðalreikningar og nöfn aðalreikninga eru aðeins tillögur. Við mælum með því að þú vinnur með endurskoðanda þínum til að ákvarða bestu uppsetninguna fyrir fyrirtækisþarfir þínar.


| Bókunargerð | Dæmi um aðalreikning | Dæmi um nafn aðalreiknings | Lykilgerð | Debet/kredit? | Millireikningur | P/F | Fylgja | Lýsing |
|------------|------------------------|-------------------------|--------------|---------|-------------------|------------|------|-------------------------|
| Kostnaður afhentra eininga | 140100</br>140101 | Efnisskrá</br>Efni sent ekki reikningsfært | Eign | Kredit | Já | P | Reikningsfærður kostnaður eininga | Notað þegar fylgiseðill sölupöntunar er bókaður. Jöfnun á reikninginn er kostnaður við seldar vörur, afhentar. Upphæðin á þessum reikningi er bakfærð þegar sölupöntunarreikningur er bókaður. Þú gætir viljað nota efni send án reikningsreiknings til að tákna efnisbirgðir og panta efnisbirgðareikning fyrir fjárhagsuppfærsluna. |
| Kostnaður seldra og afhentra vara | 500150 | Frestaður kostnaður seldra vara | Kostnaður | Debet | Já | P  | Notað þegar fylgiseðill sölupöntunar er bókaður. Jöfnun á reikninginn er kostnaður við einingar, afhentar. Upphæðin á þessum reikningi er bakfærð þegar sölupöntunarreikningur er bókaður. |
| Reikningsfærður kostnaður eininga | 140100 | Efnisskrá | Eign | Kredit | Nr. | F | Kostnaður afhentra eininga | Notað þegar sölupöntunarreikningur er bókaður. Jöfnun á þennan reikning er kostnaður við seldar vörur, reikningsfærðar. Þessi reikningur táknar birgðir á efnahagsreikningi þínum. |
| Reikningsfærður kostnaður seldra vara | 500100 | COGS efni | Kostnaður | Debet | Nr. | F  | Notað þegar sölupöntunarreikningur er bókaður. Jöfnun á þennan reikning er kostnaður við einingar, reikningsfærðar. Þessi reikningur táknar COGS á P-inu þínu&amp; L yfirlýsing. |
| Tekjur (tekjur af sölupöntun*) | 400100 | Tekjuefni | Tekjur | Kredit | Nr. | F   | Notað þegar sölupöntunarreikningur er bókaður. Á móti þessum reikningi er yfirlitsreikningur (viðskiptavinastaða*) á **Bókunarprófíll viðskiptakrafna**. |
| Þóknun (sala, þóknun*) | 602150 | Þóknunarkostnaður | Kostnaður | Debet | Nr. | F  | Notað þegar þóknun er virkjuð og reiknuð fyrir sölu og bókuð í reikningsferli sölupöntunar. Jöfnun á þennan reikning er þóknun sem ber að greiða. |
| Þóknunarjöfnun (sala, þóknunarjöfnun*) | 201110 | Þóknun til greiðslu | Skuld | Kredit | Já | F | Notað þegar þóknun er virkjuð og reiknuð fyrir sölu og bókuð í reikningsferli sölupöntunar. Jöfnun á þennan reikning er kostnaður þóknunar. |
| Frestað tekjur við afhendingu (sala – tekjur af fylgiseðlum*) | 401400 | Áfallin sala | Tekjur | Kredit | Já | P  | Notað þegar Frestað tekjur til afhendingar er virkt og er bókað þegar unnið er úr fylgiseðli sölupöntunar. Mótið á þennan reikning er frestað tekjujöfnun. Upphæðir á þessum reikningi eru sjálfkrafa bakfærðar þegar þú bókar sölupöntunarreikninginn. |
| Frestað tekjujöfnun við afhendingu (Sala – tekjujöfnun fylgiseðils)* | 130400 | Viðskiptakröfur – ekki reikningsfærðar | Eign | Debet | Já | P  | Notað þegar Frestað tekjur fyrir afhendingu er virkt og bókað þegar þú vinnur sölupöntun fylgiseðil. Á móti þessum reikningi eru frestað tekjur við afhendingu. Upphæðir á þessum reikningi eru sjálfkrafa bakfærðar þegar þú bókar sölupöntunarreikninginn. |
| Frestur söluskattur við afhendingu (sala, fylgiseðilsskattur*) | 250500 | Frestur söluskattur | Skuld | Kredit | Já | P  | Notað þegar Frestað tekjur fyrir afhendingu er virkjuð og Bóka líkamlegan söluskatt er virkt. Skattupphæðin er bókuð þegar þú vinnur úr fylgiseðli sölupöntunar. |

\* Gildi sem sýnd eru innan sviga í þessari töflu tákna gildið sem er notað í **Tegund færslu** sviði á **Viðskipti með skírteini** síðu. Þú getur skoðað **Tegund færslu** í **Viðskipti með skírteini** síðu á **Almennt** flipa.

## <a name="sales-category-posting"></a>Bókun söluflokka

Sem valkostur við að setja upp birgðabókun fyrir allar vörur, vöruflokk eða eina vöru, er hægt að setja upp flokka og stjórna fjárhagsbókun eftir söluflokkum. Frekari upplýsingar um uppsetningu flokkastigveldis og úthlutun flokka á vörur er að finna í [Búðu til stigveldi vöruflokkunar](/supply-chain/pim/tasks/create-hierarchy-product-classification.md) og [Flokkaðu vöru með því að nota flokkastigveldi](/supply-chain/pim/tasks/classify-product-category-hierarchies.md).

Eftir að þú hefur búið til flokkastigveldi verður þú að úthluta stigveldinu á eina eða fleiri gerðir. Til að nota flokkastigveldi á sölupantanir, verður að úthluta flokkinum á stigveldisgerð söluflokka. Fyrir frekari upplýsingar, farðu á [Um flokkastigveldi](/dynamicsax-2012/appuser-itpro/about-category-hierarchies.md).

## <a name="create-revenue-posting-by-sales-category"></a>Búðu til tekjufærslu eftir söluflokki

Til að úthluta fjárhagsbókunum fyrir sölupöntun sem byggist á söluflokki skal fylgja þessum skrefum:

1. Opnið **Birgðastjórnun** > **Uppsetning** > **Bókun** > **Bókun**.
2. Veldu **Sala** flipa.
3. Veldu valhnappinn fyrir færslugerðina sem þú vilt stilla (td, **Tekjur**).
4. Veljið **Nýtt**.
5. Í **Vörukóði** reit, veldu **Flokkur**.
6. Nota **Flokkstengsl** reit til að velja flokk fyrir færslusniðið.
7. Í **Reikningskóði** reit, veldu valkost fyrir **Tafla**, **·**, eða **Allt**. Til dæmis, til að nota bókunarsniðið á alla viðskiptavini, veldu **Allt**.
   - Ef þú valdir **Tafla** í skrefi 6, veldu það tiltekna **Seljandi númer** fyrir færslusniðið í **Reikningstengsl** sviði.
   - Ef þú valdir **Hópur** í skrefi 6, veldu **Seljendahópur** fyrir færslusniðið í **Reikningstengsl** sviði.
   - Ef þú valdir **Allt** í skrefi 6, sem **Reikningstengsl** reiturinn verður skilinn eftir auður.

8. Til að tengja tiltekinn skattflokk sem hefur valda bókunargerð skaltu velja a **Vöruskattshópur**. Ef þetta svæði er skilið eftir autt mun bókunargerðin eiga við um alla fyrirliggjandi skattaflokka. Bókun sem er tilgreind fyrir skattflokka á aðeins við um færslur sem eru gerðar fyrir sölu og innkaup.

9. Í **Aðalreikningur** reit, tilgreinið reikningsnúmerið sem á að bóka reikningsgerðina á. Velja eitt af fyrirliggjandi lykilnúmerunum í bókhaldslyklunum.
