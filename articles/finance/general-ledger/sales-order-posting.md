---
title: Bókun sölupöntunar
description: Þessi grein veitir upplýsingar um flipa sölupöntunar birgðabókunarreglusíðunnar.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventItemGroup
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: 5ea1c3c90b32d18243615e3ff283e1e818ac23b6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886314"
---
# <a name="sales-order-posting"></a>Bókun sölupöntunar

Flipinn **Sölupöntun** á síðunni **Birgðabókunarreglur** er notaður til að stjórna því hvernig sölupantanir verða bókaðar í fjárhaginn. Tvær meginaðgerðir eru bókaðar í fjárhag fyrir sölupöntun: 

- Fylgiseðill
- Reikningur

Til að efnisleg færsla (fylgiseðill) sé bókuð í fjárhaginn fyrir sölupöntun þarf að uppfylla eftirfarandi skilyrði:

- Á síðunni **Færibreytur birgða- og vöruhúsakerfis** þarf að velja gátreitinn **Bóka fylgiseðil í fjárhag**.
- Á **Vörulíkanaflokkur** síðunni fyrir valda vöru á sölupöntunarlínunni þarf gátreiturinn **Bóka efnislegar birgðir** að vera valinn.
- Tilgreina þarf aðallyklana á síðunni **Birgðabókunarregla** fyrir eftirfarandi bókunargerðir:
  - Kostnaður afhentra eininga
  - Kostnaður seldra og afhentra vara

Til að fjárhagsfærsla (reikningur) sé bókuð í fjárhaginn fyrir sölupöntun þarf að uppfylla eftirfarandi skilyrði:

- Á **Vörulíkanaflokkur** síðunni fyrir valda vöru á sölupöntunarlínunni þarf gátreiturinn **Bóka fjárhagslegar birgðir** að vera valinn.
- Tilgreina þarf aðallyklana á síðunni **Birgðabókunarregla** fyrir eftirfarandi bókunargerðir:
  - Reikningsfærður kostnaður eininga
  - Reikningsfærður kostnaður seldra vara
  - Tekjur
  - Afsláttur\*

> [!NOTE]
> Afsláttarreikningurinn er valfrjáls. Margar bókhaldsreglur, svo sem GAAP og IFRS, gera kröfu um að afsláttur lækki sölutekjur og því eru þessir lyklar ekki notaðir í mörgum tilvikum. Ef staðbundnar reglur leyfa skaltu nota sérstakan aðallykil til að bóka þann hluta söluverðs sem er með afslætti.

Til að bóka fresta (fylgiseðill) tekjugildi í fjárhaginn þegar fylgiseðill fyrir sölupöntun er búinn til þurfa eftirfarandi skilyrði að vera fyrir hendi:

- Á **Vörulíkanaflokkur** síðunni fyrir valda vöru á sölupöntunarlínunni þarf gátreiturinn **Bóka efnislegar birgðir** að vera valinn.
- Á síðunni **Vörulíkanaflokkur** verður gátreiturinn **Færa á lykil fyrir frestaðar tekjur í söluafhendingu** að vera valinn.
- Á síðunni **Færibreytur birgða- og vöruhúsakerfis** þarf að velja gátreitinn **Bóka fylgiseðil í fjárhag**.
- Á síðunni **Færibreytur birgða- og vöruhúsakerfis** þarf að velja gátreitinn **Bóka efnislegan virðisaukaskatt**.
- Á síðunni **Færibreytur viðskiptakrafna** þarf að velja gátreitinn **Bóka fylgiseðil í fjárhag**.
- Tilgreina þarf aðallyklana á síðunni **Birgðabókunarregla** fyrir eftirfarandi bókunargerðir:
  - Frestaðar tekjur við afhendingu
  - Frestaðar tekjur mótbókfærðar við afhendingu
  - Frestaður virðisaukaskattur við afhendingu

> [!NOTE]
> Við mælum almennt með því að þú virkjir valmöguleikana **Bóka efnislegar birgðir** og **Bóka fylgiseðil í fjárhag**. Ef þessir valkostir eru virkjaðir getur það hjálpað til við að flýta lokun um mánaðarmót því ekki þarf að reikna út og bóka neinar frestanir. Að auki munu fjárhagsskýrslur endurspegla frestaðar fjárhæðir sjálfkrafa án handvirks inngrips.

> [!IMPORTANT]
> Valkosturinn **Bóka á lykil fyrir frestaðar tekjur á söluafhendingu** er ekki notaður með tekjuskráningu. Frekari upplýsingar um tekjuskráningu er að finna [Yfirlit tekjuskráningar](/accounts-receivable/revenue-recognition-overview.md)

## <a name="sample-posting-profile-configuration"></a>Skilgreining prófunarbókunarreglu 

Eftirfarandi tafla sýnir dæmi um sjálfgefnar bókunargerðir með sýnishorn af aðallyklum og lýsingum:
 
- Dálkurinn **Millireikningur** gefur til kynna að bókunargerðin sé millireikningur. Upphæðin sem er birt á þessum reikningi er sjálfkrafa afturkölluð þegar seinni færsla er bókuð. 
- Dálkurinn **P/F** gefur til kynna **P** fyrir efnislega bókun og **F** fyrir fjárhagslega bókun. 
- Dálkurinn **Fylgja** tilgreinir hvort aðallykill fyrri tiltekna bókunargerð er yfirleitt sá sami og önnur bókunargerð. Gildið í dálkinum gefur til kynna færslutegund sem er yfirleitt notuð.

> [!NOTE]
> Þessir aðallyklar og aðallyklaheiti eru aðeins tillögur. Mælt er með að þú vinnir með endurskoðanda þínum til að finna út bestu stillingarnar fyrir viðskiptaþarfir þínar.


| Bókunargerð | Dæmi um aðallykil | Dæmi um heiti aðallykils | Lykilgerð | Debet/kredit? | Millireikningur | P/F | Fylgja | Lýsing |
|------------|------------------------|-------------------------|--------------|---------|-------------------|------------|------|-------------------------|
| Kostnaður afhentra eininga | 140100</br>140101 | Efnisbirgðir</br>Efni afhent, óreikningsfært | Eign | Kredit | Já | P | Reikningsfærður kostnaður eininga | Notað þegar fylgiseðill sölupöntunar er bókaður. Mótlykill reiknings er Kostnaður seldra, afhent. Upphæðin í þessum lykli er bakfærð þegar reikningur fyrir sölupöntun er bókaður. Þú gætir viljað nota lykilinn Efni afhent ekki reikningsfært til að sýna efnislegar birgðir og taka frá birgðareikninginn Efni fyrir fjárhagsuppfærsluna. |
| Kostnaður seldra og afhentra vara | 500150 | Frestaður kostnaður seldra vara | Kostnaður | Debet | Já | P  | Notað þegar fylgiseðill sölupöntunar er bókaður. Mótlykill við þennan lykil er einingarkostnaðurinn, afhent. Upphæðin í þessum lykli er bakfærð þegar reikningur fyrir sölupöntun er bókaður. |
| Reikningsfærður kostnaður eininga | 140100 | Efnisbirgðir | Eign | Kredit | Nr. | F | Kostnaður afhentra eininga | Notað þegar sölupöntunarreikningur er bókaður. Mótlykill við þennan lykil er kostnaður seldra vara, reikningsfærður. Þessi lykill táknar birgðir í efnahagsreikningnum þínum. |
| Reikningsfærður kostnaður seldra vara | 500100 | Efni tengt kostnaði seldra vara | Kostnaður | Debet | Nr. | F  | Notað þegar sölupöntunarreikningur er bókaður. Mótlykill við þennan lykil er einingarkostnaðurinn, reikningsfærður. Þessi lykill táknar kostnað seldra vara á &amp;rekstraryfirlitinu þínu. |
| Tekjur (tekjur af sölupöntun*) | 400100 | Tekjuefni | Tekjur | Kredit | Nr. | F   | Notað þegar sölupöntunarreikningur er bókaður. Mótlykill þessa reiknings er Safnlykill (Staða viðskiptavinar *) **á bókunarsniði viðskiptakrafa**. |
| Þóknun (sala, þóknun*) | 602150 | Þóknunarkostnaður | Kostnaður | Debet | Nr. | F  | Notað þegar þóknun er virkjuð og reiknuð fyrir sölu og bókuð meðan á sölupöntunarreikningsferlinu stendur. Mótlykill við þennan lykil er Þóknunargjöld. |
| Mótlykill þóknunar (Sala, mótlykill þóknunar*) | 201110 | Þóknunargjöld | Bótaábyrgð | Kredit | Já | F | Notað þegar þóknun er virkjuð og reiknuð fyrir sölu og bókuð meðan á sölupöntunarreikningsferlinu stendur. Mótlykill við þennan lykil er Þóknunarkostnaður. |
| Frestaðar tekjur við afhendingu (Sala - fylgiseðilstekjur*) | 401400 | Uppsöfnuð sala | Tekjur | Kredit | Já | P  | Notað þegar Frestaðar tekjur til afhendingar eru virkjaðar og eru bókaðar þegar unnið er úr fylgiseðli sölupöntunar. Mótlykill við þennan lykil er Frestaðar tekjur mótbókun. Upphæðirnar á þessum reikningi eru sjálfkrafa bakfærðar þegar reikningur fyrir sölupöntun er bókaður |
| Frestaðar tekjur mótbókfærðar við afhendingu (Sala - fylgiseðilstekjur)* | 130400 | Viðskiptakröfur – óreikningsfærðar | Eign | Debet | Já | P  | Notað þegar Frestaðar tekjur til afhendingar eru virkjaðar og bókast þegar unnið er úr fylgiseðli sölupöntunar. Mótlykill við þennan lykil er Frestaðar tekjur við afhendingu. Upphæðirnar á þessum reikningi eru sjálfkrafa bakfærðar þegar reikningur fyrir sölupöntun er bókaður |
| Frestaður virðisaukaskattur við afhendingu (Sala, fylgiseðilsskattur*) | 250500 | Frestaður virðisaukaskattur | Bótaábyrgð | Kredit | Já | P  | Notað þegar Frestaðar tekjur til afhendingar eru virkar og Bóka efnislegan virðisaukaskatt er virkur. Skattfjárhæðin er bókuð þegar unnið er úr fylgiseðli sölupöntunar. |

\*Gildi sýnd innan sviga í þessari töflu tákna gildið sem er notað í reitnum **Bókunargerð** á síðunni **Fylgiskjalafærslur**. Hægt er að skoða **Bókunargerð** á síðunni **Færslur fylgiskjals** á flipanum **Almennt**.

## <a name="sales-category-posting"></a>Söluflokkabókun

Í stað þess að setja upp birgðabókun fyrir allar vörur, vöruflokk eða staka vöru er hægt að setja upp flokka og stjórna fjárhagsbókuninni með söluflokkum. Til að fá frekari upplýsingar um uppsetningu á tegundastigveldi og úthlutun flokka á vörur, farðu í [Stofna stigveldi afurðaflokkunar](/supply-chain/pim/tasks/create-hierarchy-product-classification.md) og [Flokka afurð með flokkastigveldi](/supply-chain/pim/tasks/classify-product-category-hierarchies.md).

Þegar tegundastigveldi hefur verið búið til verður að úthluta stigveldi á eina eða fleiri tegundir. Til að nota tegundastigveldi á sölupöntunum verður að úthluta flokknum á Tegundastigveldi sölu. Nánari upplýsingar má finna í [Um tegundastigveldi](/dynamicsax-2012/appuser-itpro/about-category-hierarchies.md).

## <a name="create-revenue-posting-by-sales-category"></a>Búa til tekjubókun eftir söluflokki

Til að úthluta fjárhagsbókunum fyrir sölupöntun sem byggir á söluflokki skal fylgja þessum skrefum:

1. Opnið **Birgðastjórnun** > **Uppsetning** > **Bókun** > **Bókun**.
2. Veljið flipann **Sala**.
3. Veljið hnapp fyrir bókunargerðina sem á að stilla (til dæmis, **Tekjur**).
4. Veljið **Nýtt**.
5. Á svæðinu **Vörukóði** skal velja **Flokkur**.
6. Notið reitinn **Tegundavensl** til að velja flokkinn fyrir bókunarregluna.
7. Á svæðinu **Kóði lykils** skal velja valkost fyrir **Tafla**, **Flokkur** eða **Allt**. Til dæmis til að úthluta bókunarreglu á alla viðskiptavini skal velja **Allt**.
   - Ef **Tafla** var valið í skrefi 6 skal velja tiltekið **Númer lánardrottins** fyrir bókunarregluna í reitnum **Lyklavensl**.
   - Ef **Flokkur** var valið í skrefi 6 skal velja **Lánardrottnaflokkur** fyrir bókunarregluna í reitnum **Lyklavensl**.
   - Ef **Allt** er valið í 6. skrefi er reiturinn **Lyklavensl** auður.

8. Til að tengja tiltekinn skattflokk sem er með valda bókunargerð skal velja **VSK-flokkur**. Ef þetta svæði er skilið eftir autt mun bókunargerðin eiga við um alla fyrirliggjandi skattaflokka. Bókun sem er skilgreind fyrir skattaflokka gildir einungis um færslur sem eru gerðar vegna sölu eða innkaupa.

9. Í reitinn **Aðallykill** skal tilgreina lykilnúmerið til að bóka við lykilgerðina á svæðinu Aðallykill. Velja eitt af fyrirliggjandi lykilnúmerunum í bókhaldslyklunum.
