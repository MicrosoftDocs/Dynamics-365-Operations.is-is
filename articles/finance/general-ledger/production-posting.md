---
title: Bókun framleiðslupöntunar
description: Þessi grein gefur upplýsingar um mismunandi tegundir framleiðslupöntunarbókana.
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
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879625"
---
# <a name="production-postings"></a>Framleiðslubókanir

Þessi grein gefur upplýsingar um mismunandi tegundir bókana í framleiðslupöntunarferlinu.


## <a name="material-consumption"></a>Efnisnotkun

Efni eru skráðar sem notuð í framleiðslu þegar tiltektarlisti framleiðslubókar er bókuð. Þetta myndar færslur sem draga frá birgðum á lager. Í **Færibreytur framleiðslu** er hægt að tilgreina hvort gildi hráefna sem eru í vinnslu (kallað VÍV) skuli bókuð í fjárhaginn.

Virði hráefna sem eru í verki í vinnslu (VÍV) er bókað á lyklana **Áætlaður kostnaður við notað efni** og **Áætlaður kostnaður við notað efni, VÍV**. Ferli tínslulista fyrir framleiðslupöntunina er efnisleg uppfærsla á birgðafærslum sem tengjast framleiðslupöntuninni. Þegar framleiðslupöntun er skráð sem lokið eru efnislegar færslur bakfærðar og tengdar birgðafærslur eru fjárhagslega uppfærðar. Þegar lokunarbókin er bókuð eru bókunargerðirnar **Kostnaður við notað efni** og **Kostnaður við notað efni, VÍV** notaðar.

Flipinn **Framleiðsla** á síðunni **Birgðabókunarreglur** stýrir því hvernig framleiðslupantanir bókast í fjárhaginn. Þetta er notað þegar reiturinn **Fjárhagsbókun** er stilltur á annaðhvort **Vara og tilföng** eða **Vara og flokkur** á síðunni **Færibreytur framleiðslustýringar**. 

Fyrir færslubók tiltektarlista að bókast í fjárhaginn fyrir framleiðslupöntun þarf að uppfylla eftirfarandi skilyrði:

-   Velja þarf gátreitinn **Bóka tiltektarlista í fjárhag** á síðunni **Færibreytur framleiðslustýringar**. Hægt er að hnekkja þessari stillingu fyrir tiltekið svæði á síðunni **Færibreytur framleiðslustýringar eftir svæði**.
-   Velja þarf gátreitinn **Bóka efnislegar birgðir** á síðunni **Vörulíkanaflokkar** fyrir vöruna sem valin er í innkaupapöntunarlínunni.
-   Tilgreina þarf aðallyklana á síðunni **Birgðabókunarregla** fyrir eftirfarandi bókunargerðir:
    -   **Áætlaður kostnaður við notað efni**
    -   **Áætlaður kostnaður við notað efni, VÍV**

## <a name="time-consumption"></a>Tímanotkun

Tíminn sem starfsmenn nota í framleiðsluvinnslu er skráð í **færslubók leiðarspjalds** eða **vinnsluspjaldsbókinni**. Þegar þessar færslubækur eru bókaðar er unnin fjárhagsbókunin á sérstakan lykil fyrir tilföng sem eru í vinnslu (VÍV). Þessi bókun sýnir virði tímans sem er varið í framleiðslupöntun. Eftir að framleiðslupöntunin er skráð sem lokið, er vív-lyklar eru jafnaðir.

Þrjár mögulegar leiðir eru í boði til að bóka tímanotkun eftir því hvaða valkostur er valinn í reitnum **Fjárhagsbókun** á síðunni **Færibreytur framleiðslustýringar**.

## <a name="reporting-finished-goods-and-error-quantities"></a>Tilkynni um Fullbúnar vörur og villumagn

Þegar framleiðslupöntun er **Skráð sem lokið**, eru fullbúnar vörur sem var lokið uppfærðar í birgðum í gegnum færslubókina **Bóka sem tilbúið**. Ef verið er að nota VÍV-bókhald er færslubók fjárhags mynduð til að fækka VÍV-lyklum og auka birgðir fullunninna vara. Færslubókin notar staðlaðan kostnað sem hefur verið skilgreindur fyrir afurðina. Ef valkosturinn **Nota áætlað kostnaðarverð** er valinn á síðunni **Færibreytur framleiðslustýringar** verður áætlaður kostnaður úr framleiðslupöntuninni notaður.

Virði hráefna sem eru í verki í vinnslu (VÍV) er bókað á lyklana **Áætlaður framleiðslukostnaður** og **Áætlaður framleiðslukostnaður, VÍV**. Ferlið **Tilkynna sem lokið** fyrir framleiðslupöntunina er efnisleg uppfærsla á birgðafærslum sem tengjast framleiðslupöntuninni. Þegar lokið er við framleiðslupöntun eru efnislegar færslur bakfærðar og tengdar birgðafærslur eru fjárhagslega uppfærðar. Þegar lokunarbókin er bókuð eru bókunargerðirnar **Kostnaður við framleiðslu** og **Kostnaður við framleiðslu, VÍV** notaðar.

Flipinn **Framleiðsla** á síðunni **Birgðabókunarreglur** er notaður til að stýra því hvernig framleiðslupantanir bókast í fjárhaginn. Þetta er notað þegar reiturinn **Fjárhagsbókun** er stilltur á annaðhvort **Vara og tilföng** eða **Vara og flokkur** á síðunni **Færibreytur framleiðslustýringar**. Flýtiflipann **Fjárhagur-vörur** á síðunni **Framleiðsluflokkar** er einnig hægt að nota til að stjórna bókun fyrir framleiðslupantanir þegar reiturinn er stilltur á **Framleiðsluflokkar**.

Til að færslubókin **Bóka sem tilbúið** bókist í fjárhaginn fyrir framleiðslupöntun þarf að uppfylla eftirfarandi skilyrði:
-   Velja þarf gátreitinn **Bóka tilkynnt tilbúið í fjárhag** á síðunni **Færibreytur framleiðslustýringar**. Hægt er að hnekkja þessari stillingu fyrir tiltekið svæði á síðunni **Færibreytur framleiðslustýringar eftir svæði**.
-   Velja þarf gátreitinn **Bóka efnislegar birgðir** á síðunni **Vörulíkanaflokkar** fyrir vöruna sem valin er í innkaupapöntunarlínunni.
-   Tilgreina þarf aðallyklana á síðunni **Birgðabókunarregla** fyrir eftirfarandi bókunargerðir:
    -   **Áætlaður kostnaður við framleiðslu**
    -   **Áætlaður kostnaður við framleiðslu, VÍV**

## <a name="ending-the-production-order"></a>Lokið við framleiðslupöntunina

Áður er framleiðslupöntun er lokið er raunkostnaður reiknaður fyrir framleitt magn. Allur áætlaður kostnaður fyrir efni, vinnu og rekstrarkostnaði er bakfærður og skipt út fyrir raunkostnað. Heildarkostnaðurinn fyrir afurð er debetfærður frá lyklinum **Kostnaður við framleiðslu** og kreditfærður á lykilinn **Kostnaður við framleiðslu, VÍV**. Efnið sem notað var í framleiðslupöntuninni er kreditfært á **Kostnaður við notað efni** og debetfært á lykilinn **Kostnaður efnis, VÍV**.

Ef þú velur **Ljúka vinnslu** gátreitur þegar þú keyrir kostnaðarútreikningur, breytist staða framleiðslupöntunar í **Lokið**. Þessi staða kemur í veg fyrir aukalegan kostnað sé óvart bókaður á lokna framleiðslupöntun. Hægt er að tilgreina að gildi villna sem eru skráðar sem loknar við skýrslugerð sem skuli úthluta á gallalausa magnið sem er skráð sem lokið. Einnig er hægt að tilgreina að virðis villumagns eigi að bóka á sérstakan rýrnunarlykil. 

Til að tilgreina tiltekinn rýrnunarlykil skal fylgja eftirfarandi skrefum:
1.  Farið í **Framleiðslustýring**  >  **Uppsetning**  >  **Færibreytur framleiðslustýringar**.
2.  Veljið flipann **Stöðluð uppfærsla**.
3.  Í reitnum **Rýrnunaraðferð** skal velja **Rýrnunarlykill**.
4.  Í reitnum **Rýrnunarlykill** skal velja aðallykilinn þar sem rýrnun fyrir villumagn á að vera bókað þegar framleiðslupöntuninni lýkur. Veljið til dæmis kostnaðarlykil á borð við 510380: Framleiðslurýrnun.

Til að lokunarbókin bókist í fjárhaginn fyrir framleiðslupöntun þarf að uppfylla eftirfarandi skilyrði:
-   Tilgreina þarf aðallyklana á síðunni **Birgðabókunarregla** eða **Framleiðsluflokkar** fyrir eftirfarandi bókunargerðir:
    -   **Kostnaður við notað efni**
    -   **Kostnaður við notað efni, VÍV**
    -   **Kostnaður við framleiðslu**
    -   **Kostnaður við framleiðslu, VÍV**
-   Tilgreina verður aðallyklana á síðunni **Kostnaðarflokkar**, **Tilföng** eða **Tilfangaflokkar** fyrir eftirfarandi gerðir:
    -   **Notaður framleiðslukostnaður**
    -   **Kostnaður við notaða framleiðslu, VÍV**

## <a name="indirect-costs-for-production-orders"></a>Óbeinn kostnaður fyrir framleiðslupantanir

Þegar unnið er úr færslum fyrir framleiðslupöntun er hægt að grunnstilla óbeinan kostnað til að sækja sameiginlegan kostnað eða viðbótargjöld í fjárhagnum. Efnislegar færslur fyrir óbeinan kostnað eru skráðar í birgðir þegar færslubók tiltektarlista eða færslubók fyrir tilbúið er bókuð. Fjárhagsfærslur fyrir óbeinan kostnað eru skráðar í birgðum þegar lokunarbókin er bókuð.

Hægt er að bera kennsl á óbeinan kostnað á tímanotkun sem tengist færslubókum **Leiðarspjalds** eða færslubókum **Verkspjalds**. Þessar færslur eru bakfærðar og bókaðar á fjárhagslykla þegar lokið er við framleiðslupöntun. Frekari upplýsingar er að finna á [Kostnaðarskjal](/supply-chain/cost-management/costing-sheets.md).

## <a name="controlling-the-level-of-ledger-posting"></a>Stýra stigi fjárhagsbókunar

Á síðunni **Færibreytur framleiðslustýringar**, er hægt að nota í **Fjárhagsbókun** svæði til að stilla stig fjárhagsbókunar fyrir framleiðsluferli. 

Eftirfarandi reitir eru tiltækir:

### <a name="item-and-resource"></a>Vara og tilföng

Þegar valkosturinn **Vara og tilföng** er valinn í reitnum **Fjárhagsbókun** koma bókunarlyklarnir úr tilfangi eða tilfangaflokki í aðgerð í leiðinni. Lyklar að tilteknu tilfangi verða fyrsti bókunarkosturinn. Ef lykill er ekki tilgreindur verða þeir lyklar sem tilgreindir eru í tilfangaflokknum notaðir. Hver aðgerðarlína á leið getur haft eitt tilfang sem tilgreint er sem **Kostnaðartilföng**. Þetta tilfang er notað til að ákvarða hvaða lykil á að nota. Þessi valkostur er oft notaður þegar stofnun/fyrirtæki úthlutar rekstrarkostnaði á tilföngin. Kostnaður er oft hærri fyrir tilföngin og er notaður til að hjálpa við ákvarðanir um hvort er betra að framleiða eða kaupa. Þetta er nákvæmasta bókunarstillingin og leyfir bestu stýringu á bókunum og mjög ítarlegum greiningum framleiðsluferlisins.

### <a name="item-and-category"></a>Vara og tegund

Þegar valkosturinn **Vara og flokkur** er valinn í reitnum **Fjárhagsbókun** koma bókunarlyklarnir af síðunni **Kostnaðarflokkur** sem tengist hverri línu í leiðinni. Hver aðgerðarlína í leiðinni getur verið með þrjá kostnaðarflokka: **Uppsetningartíma**, **Keyrslutíma** og **Magn**. Þessi valkostur er oft notaður þegar megináhersla fyrirtækisins er á skilvirkni ferlis og tímalengd aðgerðar. Þessi kostur er meira samantekin leið við bókun og býður enn upp á leið til að safna kostnaði í flokka.

### <a name="production-group"></a>Framleiðsluflokkur

Þegar valkosturinn **Framleiðsluflokkar** er notaður í reitnum **Fjárhagsbókun** koma bókunarlyklarnir af síðunni **Framleiðsluflokkar**. **Framleiðsluflokkar** eru yfirleitt notaðir þegar fleiri en ein framleiðslulína keyrir svipaðar vörur eða er með svipaðan búnað. Hægt er að nota þennan valkost til að bera saman kostnað milli tveggja mismunandi framleiðsluflokka.  
  
> [!NOTE]
> Ef staðlaða aðferðin til að reikna út kostnað við tilbúna vöru er notuð, endurspegla lokafærslurnar það. Ef það er mismunur á raunkostnaði og útreiknuðum kostnaði með notkun stöðluðu aðferðarinnar er mismunurinn bókaður á lykilinn sem sýnir hagnað eða tap.

### <a name="route-groups-and-ledger-posting"></a>Leiðahópar og fjárhagsbókun

Hver aðgerðalína á leið er með **Leiðahópur** tilgreint. Reitirnir **Uppsetningartími**, **Keyrslutími** og **Magn** í **Leiðahópur** í flokknum **Mat og kostnaður** eru notaðir til að stjórna því hvenær tíminn verður notaður fyrir kostnaðarútreikning þegar **Verkspjald** eða **Færslubók leiðarspjalda** eru bókuð í framleiðslupöntuninni. Ef valkostirnir eru óvirkir verður fylgiskjal ekki búið til í fjárhagnum fyrir tímanotkunina.

Til að **Leiðarspjald** eða **Verkspjaldsbók** bókist í fjárhaginn fyrir framleiðslupöntun þarf að uppfylla eftirfarandi skilyrði:

-   Velja þarf reitinn **Uppsetningartími**, **Keyrslutími** eða **Magn** í flokknum **Mat og kostnaður** á síðunni **Leiðahópur**.
-   Tilgreina þarf aðallyklana á síðunni **Kostnaðarflokkur**, **Leið**, **Leiðahópur** eða **Framleiðsluflokkar** fyrir eftirfarandi bókunargerðir:
    -   Áætlaður notaður framleiðslukostnaður
    -   Áætlaður kostnaður við notaða framleiðslu, VÍV

Eftirfarandi skýringarmynd sýnir tengsl leiðahópsins við útreikning á heildarkostnaði fyrir hverja aðgerð (leiðarlínu) í tiltekinni leið. Hver leiðarlína er með einn leiðarflokkur. Leiðarhópurinn stýrir færibreytum fyrir uppsetningartíma, keyrslutíma og magn. Flipinn **Kostnaðarflokkur** er með þrjá valkosti fyrir **Uppsetningu**, **Keyrslu** og **Magn** sem eru virkjaðir samkvæmt stillingu leiðahópa. Flýtiflipinn **Tímasetningar** er með þrjá reiti sem eru byggðir á leiðarflokknum.

Formúlan sem er notuð er byggð á því hvort valkosturinn er virkur í leiðarflokknum. Kostnaðurinn úr völdum kostnaðarflokki er margfaldaður með magninu sem fært var inn í tímasetningarnar til að reikna út heildarkostnað.

:::image type="complex" source="media/RouteGroupRelationship.png" alt-text="Tengsl leiðarhópa við útreiknaðan heildarkostnað.":::
Tengsl leiðarhópa við útreiknaðan heildarkostnað. Hver leiðarlína er með einn leiðarflokkur. Leiðarhópurinn stýrir færibreytum fyrir uppsetningartíma, keyrslutíma og magn. Flipi kostnaðarflokks er með þrjá valkosti fyrir uppsetningu, keyrslu og magn sem eru virkjaðir samkvæmt stillingu leiðahópa. Flýtiflipinn „Tímasetningar“ er með þrjá reiti sem eru virkir og kostnaðarreiknaðir samkvæmt leiðarflokknum. Formúlan sem er notuð er byggð á því að valkosturinn er virkur í leiðarflokknum. Kostnaðurinn úr völdum kostnaðarflokki er margfaldaður með magninu sem fært er inn í tímasetningarnar til að reikna út heildarkostnað.
:::image-end:::

## <a name="sample-posting-profile-configuration"></a>Skilgreining prófunarbókunarreglu

Eftirfarandi tafla sýnir dæmi um sjálfgefnar bókunargerðir með sýnishorn af aðallyklum og lýsingum. 

 - Dálkurinn **Debet/kredit** tilgreinir hvort færslan er yfirleitt debet eða kredit eða í sumum tilfellum er hægt að bóka annað hvort. 
 - Dálkurinn **Millireikningur** gefur til kynna hvort bókunargerð sé millireikningur. Upphæðin sem er birt á þessum reikningi er sjálfkrafa afturkölluð þegar seinni færsla er bókuð. 
 - Dálkurinn **P/F** gefur til kynna **P** fyrir efnislega bókun og **F** fyrir fjárhagslega bókun. 
 - Dálkurinn **Fylgja** tilgreinir hvort aðallykill fyrri tiltekna bókunargerð er yfirleitt sá sami og önnur bókunargerð. Gildið í dálkinum gefur til kynna tegund færslu sem er yfirleitt fylgt.

> [!NOTE]
> Uppástungur um aðallykla og aðallyklaheiti eru tillögur. Mælt er með að þú vinnir með endurskoðanda þínum til að finna út bestu stillingarnar fyrir viðskiptaþarfir þínar.


| Bókunargerð  | Dæmi um aðallykil | Dæmi um heiti aðallykils| Lykilgerð | Debet/kredit? | Millireikningur | Efnislegt eða fjárhagslegt | Fylgja | Lýsing |
|---------------|----------------------|--------------------------|--------------|----------------|------------------|-----------------------|--------|------------|
| Áætlaður kostnaður við notað efni      | 140100               | Efnisbirgðir        | Eign        | Kredit         | Y                | P                     | Kostnaður við notað efni                | Þessi lykill er notaður þegar þú birtir færslubók tiltektarlista fyrir framleiðslupöntun. Mótlykill við þennan lykil er áætlaður efniskostnaður, VÍV. Upphæðin á þessum lykli er sjálfkrafa bakfærð þegar framleiðslupöntun er lokið. Þessi lykill stendur fyrir birgðalykil í efnahagsreikningi.       |
| Áætlaður kostnaður við notað efni, VÍV | 150150               | VÍV framleiðslu – efni | Eign        | Debet          | Y                | P                     | Áætlaður kostnaður við framleiðslu, VÍV          | Þessi lykill er notaður þegar þú birtir færslubók tiltektarlista fyrir framleiðslupöntun. Mótlykill við þennan lykil er áætlaður kostnaður notaðs efnis. Upphæðin á þessum lykli er sjálfkrafa bakfærð þegar framleiðslupöntun er lokið. Þessi lykill táknar VÍV í efnahagsreikningnum þínum.                  |
| Áætlaður kostnaður við framleiðslu               | 140200               | Fullunnar vörur í birgðum   | Eign        | Debet          | Y                | P                     | Kostnaður við framleiðslu                         | Þessi lykill er notaður þegar þú bókar skýrslu sem lokna færslubók fyrir framleiðslupöntun. Mótlykill við þennan lykil er áætlaður kostnaður við framleiðslu, VÍV. Upphæðin á þessum lykli er sjálfkrafa bakfærð þegar framleiðslupöntun er lokið. Þessi lykill stendur fyrir birgðalykil í efnahagsreikningi. |
| Áætlaður kostnaður við framleiðslu, VÍV          | 150150               | VÍV framleiðslu – efni | Eign        | Kredit         | Y                | P                     | Kostnaður við framleiðslu, VÍV                    | Þessi lykill er notaður þegar þú bókar skýrslu sem lokna færslubók fyrir framleiðslupöntun. Mótlykill við þennan lykil er áætlaður kostnaður við framleiðslu. Upphæðin á þessum lykli er sjálfkrafa bakfærð þegar framleiðslupöntun er lokið. Þessi lykill táknar VÍV í efnahagsreikningnum þínum.                     |
| Kostnaður við notað efni                | 140100               | Efnisbirgðir        | Eign        | Kredit         | N                 | F                     | Áætlaður kostnaður við notað efni      | Þessi lykill er notaður til að skrá efnin sem eru notuð í framleiðslupöntuninni meðan lokunarferlið er í gangi. Mótlykill við þennan lykil er kostnaðurinn við notað efni, VÍV.                                                                                                    |
| Kostnaður við notað efni, VÍV           | 150150               | VÍV framleiðslu – efni | Eign        | Debet          | N                 | F                     | Áætlaður kostnaður við notað efni, VÍV | Þessi lykill er notaður til að skrá efnin í VÍV sem eru notuð í framleiðslupöntuninni meðan lokunarferlið er í gangi. Mótlykill við þennan lykil er kostnaðurinn við notað efni.                                                |
| Kostnaður við framleiðslu                         | 140200               | Fullunnar vörur í birgðum   | Eign        | Debet          | N                 | F                     | Áætlaður kostnaður við framleiðslu               | Þessi lykill er notaður til að skrá kostnað á fullunnum vörum sem eru framleiddar af framleiðslupöntun þegar lokið er við framleiðslupöntunina. Mótlykill við þennan lykil er kostnaður við framleiðslu, VÍV-lykill.                                                                  |
| Kostnaður við framleiðslu, VÍV                    | 150150               | VÍV framleiðslu – efni | Eign        | Kredit         | N                 | F                     | Áætlaður kostnaður við framleiðslu, VÍV          | Þessi lykill er notaður til að skrá kostnað á fullunnum vörur í VÍV sem eru framleiddar af framleiðslupöntun þegar lokið er við framleiðslupöntunina. Mótlykill við þennan lykil er lykill kostnaðar við framleiðslu.                                     |

> [!NOTE]
> **VÍV-kvittun straumlínuþjónustu** og **VÍV-millireikningur straumlínuþjónustu** er notað með bakfærslukostnaðaraðferð fyrir straumlínuframleiðslu. Frekari upplýsingar er að finna á [Bakfærslukostnaðaraðferð](/supply-chain/cost-management/backflush-costing.md).

