---
title: Áætla og stjórna heildarkostnaði
description: Kerfið notar sjálfvirka kostnaðaruppsetningu til að ákvarða mat fyrir heildarkostnað. Þetta efnisatriði útskýrir hvernig hægt er að skilgreina ýmsar aðstæður til að skila nákvæmari áætlun.
author: sherry-zheng
manager: tfehr
ms.date: 01/26/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMCostTemplateTable, ITM CostEstimateDialog, ITMCostEstimateTable, SysOperationTemplateForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-26
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: cbd652f2b29f7a78ad9e4e1d3dda4a3ef8a9f3f3
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/04/2021
ms.locfileid: "5501271"
---
# <a name="estimate-and-manage-landed-costs"></a>Áætla og stjórna heildarkostnaði

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Kerfið notar [sjálfvirka kostnaðaruppsetningu](auto-cost-setup.md) til að ákvarða mat fyrir heildarkostnað. Einnig er hægt að skilgreina ýmsar aðstæður til að skila nákvæmari áætlun. Þessar aðstæður eru vistaðar. Þess vegna er hægt að yfirfara þær síðar og bera þær saman við rauntölur í skýrslu. Einnig er hægt að uppfæra vöruverð.

## <a name="set-up-cost-estimates"></a>Setja upp kostnaðarmat

### <a name="set-up-cost-templates"></a>Setja upp kostnaðarsniðmát

Kostnaðarsniðmát innihalda sjálfgefnar stillingar sem notendur sem fá matið þekkja ekki endilega. Sniðmát geta dregið úr flækjum í matsferlinu með því lágmarka valkostina sem notendur verða að tilgreina til að fá nákvæmt mat. Ef staðlaða kostnaðarlíkanið er notað er hægt að nota kostnaðarsniðmát á meðan verið er að setja upp kostnað á vörum.

Til að setja upp kostnaðarsniðmát skal fara í **Heildarkostnaður \> Kostnaðaruppsetning \> Kostnaðarsniðmát**. Á síðunni **kostnaðarsniðmát** sýnir listasvæðið vinstra megin öll kostnaðarsniðmát. Hægt er að nota hnappana á aðgerðarúðunni til að stofna, eyða og breyta sniðmátum.

Eftirfarandi tafla lýsir eritinum sem eru tiltæk fyrir hvert sniðmát.

| Svæði | lýsing |
|---|---|
| Kostnaðarsniðmát | Færið inn einkvæmt heiti fyrir kostnaðarsniðmátið. Heitið lýsir venjulega stuðlinum eða kostnaðarmargfaldara fyrir sniðmátið. |
| lýsing | Færa inn lýsingu á kostnaðarsniðmátinu. |
| Flutningsfyrirtæki | Veljið flutningsfyrirtækið sem á að nota þegar sniðmátið er notað. |
| Afhendingarmáti | Veljið afhendingarmáta, t.d. sjóleiðis eða loftleiðis, sem á að nota þegar sniðmátið er notað. Þessi reitur mun hjálpa til við að ákvarða sjálfvirkan kostnað sem tengist vörum í kostnaðarmatinu. |
| Gámagerð | Veljið gerð gámsins sem á að nota þegar sniðmátið er notað. Þessi reitur mun hjálpa til við að ákvarða sjálfvirkan kostnað sem tengist vörum í kostnaðarmatinu. |
| Tollmiðlari | Tollmiðlari (lánardrottinn) sem á að nota þegar sniðmátið er notað. Þessi reitur mun hjálpa til við að ákvarða sjálfvirkan kostnað sem tengist kostnaðarmatinu. |
| Stuðull | Sláið inn margfaldara (prósentuna) sem á sjálfkrafa að nota í kostnaðarmatinu þegar sniðmátið er notað. Til að bæta til dæmis 10 prósentum við reiknaða kostnaðarmatið skal slá inn *1,10*. |

### <a name="create-a-cost-estimate"></a>Stofna kostnaðarmat

Nota skal svarglugga **Kostnaðarmats** til að mynda nýja kostnaðaráætlun sem byggir á völdu kostnaðarsniðmáti, völdum vörum og öðrum upplýsingum um ferð. Þessar stillingar eru svo notaðar til að ákvarða áætlaðan heildarkostnað á vörum. Þetta kostnaðarmat er aðallega notað til að vinna með staðlaðar kostnaðarvörur. Með því að bæta áætluðum heildarkostnaði við staðalkostnað á vörum í birgðum ættu minni fráviksfærslur að koam upp þegar vörunum er bætt við ferð vegna þess að staðalkostnaðurinn endurspeglar áætlanir fyrir þennan heildarkostnað.

Til að opna svargluggann **Kostnaðarmat** skal fara í **Heildarkostnaður \> Reglubundin verk \> Kostnaðarmat**. Síðan skal stilla reitina sem lýst er í eftirfarandi undirköflum. Veljið **Í lagi** til að búa til matið. Síðan **Kostnaðarmat** (**Heildarkostnaður \> Fyrirspurnir \> Kostnaðarmat**) birtist þá og sýnir nýja matið eins og lýst er síðar í þessu efnisatriði.

### <a name="settings-on-the-parameters-tab"></a>Stillingar á flipanum færibreytur

Eftirfarandi tafla lýsir reitunum sem eru tiltækir í flipanum **Færibreytur** í **Kostnaðarmat** svarglugganum.


| Svæði | lýsing |
|---|---|
| Kostnaðarsniðmát | Velja kostnaðarsniðmát. Stillingarnar sem eru tengdar við valið sniðmát verða notaðar til að ákvarða hvaða sjálfvirkur kostnaður er notaður. |
| Dagsetning mats | Sjálfgefið er að þetta svæði er stillt á daginn í dag, en hægt er að breyta gildinu. Tilgreinda dagsetningin verður notuð til að velja viðeigandi söluverð, innkaupaverð, sjálfvirkan kostnað og gengi ef flutningstaxti er notaður. |
| Mæling | Kostnaður gæti farið eftir mælingu. Til dæmis þegar flugfrakt er notuð gæti verðlagning eftir rúmmáli verið notuð. Ef kostnaðurinn fer eftir mælingu skal færa inn gildi þeirrar mælingar. Annars mælum við með því að þessi reitur sé stilltur á *1* nema liggi ljóst fyrir að engin skipting eigi sér stað með því að nota mælingu. Sláið inn tugagildi. Einingin er sú sem er skilgreind í sjálfvirkri kostnaðarfærslu í notkun. |
| Sniðmát ferðar | Veljið [ferðasniðmát](multi-leg-journey-setup.md). Þessi reitur er notaður til að ákvarða réttan sjálfvirkan kostnað sem á að nota. |
| Frá höfn | Höfnin sem vörurnar verða sendar frá. Þessi reitur byggir á völdu ferðasniðmáti. |
| Til hafnar | Höfnin sem vörurnar verða sendar til. Þessi reitur byggir á völdu ferðasniðmáti. |
| Gjaldmiðill | Veljið gjaldmiðil sem vörur verða keyptar í. |
| Gámar | Ef margir gámar eru vanalega notaðir skal tilgreina fjölda gáma. Kerfið notar svo kostnað fyrir marga gáma þegar það áætlar kostnaðinn. |
| Fólíó | Ef mörg fólíó eru yfirleitt notuð skal tilgreina fjöldann. (Fjödlinn er yfirleitt *1*.) |
| Vefsvæði | Tilgreinið svæðið þar sem vörurnar verða afhentar. |

### <a name="settings-on-the-items-tab"></a>Stillingar á vöruflipanum

Í flipanum **Vörur** er hægt að bæta eins mörgum vörum við áætlunina og þörf krefur. Notaðu tækjastikuna til að bæta vörum við töfluna eða fjarlægja vörur. Veljið **Birgðir \> Birta víddir** á tækjastikunni til að opna svarglugga þar sem hægt er að bæta víddardálkum við hnitanetið eða fjarlægja dálka.

Eftirfarandi tafla lýsir eritinum sem eru tiltæk fyrir hverja vöru.

| Svæði | lýsing |
|---|---|
| Vörunúmer | Veljið vöruna sem á að ákvarða verðið fyrir. (Ef varan er ekki enn til staðar í kerfinu skal búa til sýnivöru, hengja hana við kostnaðarflokk vöru í ferð ef það hentar og síðan annaðhvort skilja verðið eftir autt eða búa til eða breyta verði.) |
| Lykill lánardrottins | Veljið lánardrottin sem á að nota fyrir mat á þessari vöru. Ef sjálfgefnum lánardrottni er úthlutað á vöruna er þetta svæði sjálfkrafa stillt. |
| Magn | Tilgreinið magnið sem á að kaupa. |
| Kostnaðarverð | Kerfið notar verðlagningarreglur þess til að finna upphaflegt verð, en hægt er að hnekkja því verði ef nauðsynlegt er. |
| Söluverð | Færið inn væntanlegt söluverð varanna. |
| Mæling | Sláið inn tugagildi fyrir mælingu á vörunum. Einingin er sú sem er sett upp fyrir viðeigandi útgefna afurð. |
| Uppfæra þyngd/rúmmál vöru | Veljið þennan gátreit til að uppfæra þyngdar- eða rúmmálsmælingu útgefinnar afurðar þannig að hún passi við gildið **Mæling** sem slegið er inn fyrir þessa línu. |
| (Aðrar víddir) | Það fer eftir víddunum sem voru valdar til að birtast hvort viðbótardálkar með upplýsingum um hverja vöru sjáist. |

Til að skoða eða breyta upplýsingum um rúmmál og/eða þyngd fyrir vöru skal velja vöruna í hnitanetinu og nota svo reitina neðst á síðunni.

## <a name="manage-estimated-costs"></a>Stjórna áætluðum kostnaði

Til að skoða og breyta kostnaðarmati sem hefur verið stofnað skal fara í **Heildarkostnaður \> Fyrirspurnir \> Kostnaðarmat**. Á síðunni **Kostnaðarmat** sýnir listasvæðið vinstra megin allt kostnaðarmat. Hægt er að nota hnappana á aðgerðasvæðinu til að vinna með valið mat. Athugið að ekki er hægt að stofna nýja kostnaðaráætlun af síðunni **Kostnaðarmat**. Í staðinn skal nota svargluggann **Kostnaðarmat** (**Heildarkostnaður \> Reglubundin verk \> Kostnaðarmat**) eins og lýst var fyrr í þessu efnisatriði.

Síðan **Kostnaðarmat** sýnir hvernig hver áætlaður kostnaður var afleiddur. Hún sýnir einnig áætlaðan heildarkostnað fyrir hverja vöru. Hægt er að breyta kostnaðaráætlun með því að breyta kostnaðarverði og/eða gjaldmiðli sem tengist hinum ýmsu vörum. Einnig er hægt að breyta tengdum ferðakostnaði á öllum stigum ferðar og gáma. Þegar þessi síða er notuð til að breyta kostnaði er beðið um að endurreikna áætlaðan kostnað fyrir vörurnar í kostnaðarmatinu. Þegar þetta er tilbúið er hægt að nota áætlanir til að uppfæra kostnaðarverð varanna í kostnaðarsniðmátinu.

### <a name="information-on-the-header"></a>Upplýsingar á hausi

Efst á síðunni **Kostnaðarmat** sjást stillingarnar sem voru notaðar til að mynda valið kostnaðarmat eins og lýst er í hlutanum hér á undan. 

### <a name="settings-and-buttons-on-the-lines-fasttab"></a>Stillingar og hnappar á flýtiflipanum Línur

Flýtiflipinn **Línur** sýnir hverja vöru sem er tekin með í gildandi mati. Eftirfarandi tafla lýsir reitunum sem eru tiltækir fyrir hverja línu.

| Svæði | lýsing |
|---|---|
| Lykill lánardrottins | Lánardrottnalykillinn sem varan tengist. |
| Vörunúmer | Vörunúmerið. |
| Magn | Fjöldi vara sem eru notaðar til að ákvarða kostnaðinn. |
| Kostnaðarverð | Kostnaðarverð samkvæmt verðsamningi. Þetta gildi er sýnt í staðbundnum gjaldmiðli. |
| Mæling | Mælingin sjálf. Einingin er sú sem er skilgreind fyrir viðeigandi útgefna afurð. |
| Áætlaður heildarkostnaður | Áætlaður heildarkostnaður fyrir heildarmagn. |
| Á hverja einingu | Áætlaður heildarkostnaður deilt með magninu. |
| (Aðrar víddir) | Það fer eftir víddunum sem voru valdar til að birtast hvort viðbótardálkar með upplýsingum um hverja vöru sjáist. |

Eftirfarandi tafla lýsir þeim hnöppum sem eru á tækjastikunni á flýtiflipanum **Línur**.

| Hnappur | lýsing |
|---|---|
| Bæta við | Bæta atriðum við kostnaðarmat. Ef vörum er bætt við verður að velja **Endurreikna** á aðgerðarúðunni. |
| Fjarl. | Fjarlægja vörur úr kostnaðarmatinu. Ef vörur eru fjarlægðar verður að velja **Endurreikna** á aðgerðarúðunni. |
| Kostnaður ferðar | Opna síðu þar sem hægt er að skoða og breyta ýmsum gerðum ferðakostnaðar fyrir vöruna. |
| Birtar víddir \> birgða | Opnið svarglugga þar sem hægt er að bæta víddardálkum við hnitanetið eða fjarlægja dálka. |

### <a name="settings-on-the-general-fasttab"></a>Stillingar á flýtiflipanum Almennt

Flýtiflipinn **Almennt** sýnir upplýsingar um valda vöru í flýtiflipanum **Línur**. Mikið af þessum upplýsingum eru endurteknar úr flýtiflipanum **Línur** og hægt að breyta á báðum stöðum. Frekari upplýsingar eru einnig í boði hér. Gildin á aukareitunum eru byggð á uppsetningu á viðeigandi útgefinni afurð.

### <a name="settings-on-the-dimension-fasttab"></a>Stillingar á flýtiflipa víddar

Flýtiflipinn **Vídd** sýnir gildi fyrir allar tiltækar birgðavíddir fyrir vöruna sem er valin í flýtiflipanum **Línur** burtséð frá víddunum sem valdar voru til að birtast hér. Öll gildi sem eru sýnd hér koma úr viðeigandi kostnaðarmatssniðmáti. Þau eru valfrjáls í kostnaðarmatssniðmátinu.

### <a name="buttons-on-the-action-pane"></a>Hnappar á aðgerðasvæðinu

Hægt er að nota hnappana á aðgerðasvæði á síðunni **Kostnaðarmat** til að vinna með valið kostnaðarmat. Eftirfarandi tafla lýsir hnöppunum sem eru í boði.

| Aðgerð | lýsing |
|---|---|
| Fyrirspurn um kostnað | Skoða allan kostnað fyrir ferð. Hægt er að skoða kostnað á stigi einstakra atriða eins og nauðsynlegt er. |
| Uppfæra staðalkostnað | <p>Uppfærið staðalkostnaðinn með því að nota sjálfgefna kostnaðarútgáfuna sem skilgreind er á síðunni **Færibreytur heildarkostnaðar**. Hægt er að hnekkja þessari útgáfu.</p><p>**Athugið:** Ef vara er með margar vöruvíddir (t.d. ýmsar stæðir, liti og skilgreiningar) en þessar vörur hafa verið valdar fyrir áætlunina mun kerfið búa til biðverð fyrir hverja samsetningu.</p><p>**Mikilvægt:** Sundurliðun verðs er stofnuð og notuð til að ákvarða staðlað kostnaðarfrávik á hvern heildarkostnað.</p> |
| Kostnaður ferðar | Skoða og breyta ferðakostnaði fyrir allar vörur í sendingunni. |
| Endurreikna | Uppfærið áætlaðan heildarkostnað þegar kostnaður ferðar hefur verið uppfærður, bætt við eða fjarlægður. |
| Læsing | Læsið færslu kostnaðarmats þannig að ekki sé hægt að gera neinar fleiri breytingar. |

## <a name="item-cost-price-update"></a>Uppfærsla á kostnaðarverði vöru

Reglubundnar verkið **Uppfærsla á kostnaðarverði vöru** uppfærir allt kostnaðarmat sem passar við síurnar sem eru stilltar þegar verk er keyrt. Áhrifin eru svipuð og áhrif þess að velja **Uppfæra staðalkostnað** á aðgerðasvæðinu fyrir eitt mat. Í þessu tilfelli gildir uppfærslan hins vegar við allt mat.

Fylgdu þessum skrefum til að keyra reglubundin verk.

1. Farið í **Heildarkostnaður \> Reglubundin verkefni \> Uppfærsla á kostnaðarverði vöru**.
1. Í svarglugganum **Uppfæra kostnaðarverð úr mati** skal stilla eftirfarandi reiti eins og nauðsynlegt er til að takmarka umfang uppfærslunnar:

    - **Útgáfa** – Aðeins uppfæra mat sem notar tilgreinda kostnaðarútgáfu.
    - **Svæði** – Aðeins uppfæra mat sem notar tilgreint svæði.
    - **Kostnaðarsniðmát** – Aðeins uppfæra mat sem notar tilgreint sniðmát.
    - **Til hafnar** – Aðeins uppfæra mat sem notar tilgreinda höfn „ti“.
    - **Dagsetning mats** – Aðeins uppfæra mat sem er með tilgreinda dagsetningu.

1. Stillið valkostina í **Færslur til að taka með** og flýtiflipanum **Keyra í bakgrunni** eins og venjulega fyrir reglubundin verk.
1. Veljið **Í lagi** til að keyra verkið.

> [!NOTE]
> Þetta reglubundna verk mun aðeins keyra þegar eftirfarandi upplýsingar eru til staðar:
>
> - Hver viðeigandi afurð verður að vera með **Brúttódýpt**, **Brúttóbreidd** og **Brúttóhæð** skilgreint.
> - Sérhver viðeigandi lánardrottinn verður að vera með **Frá höfn** skilgreint.
