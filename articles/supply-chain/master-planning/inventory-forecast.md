---
title: Birgðaspár
description: Í þessu efnisatriði er útskýrð virkni framboðs og eftirspurnar sem hægt er að nota til að búa til birgðaspár í Microsoft Dynamics 365 Supply Chain Management.
author: crytt
ms.date: 06/08/2021
ms.topic: article
ms.search.form: EcoResProductDetailsExtended, ForecastSales, ForecastPurch, ForecastInvent
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-06-08
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a0919706ddcc70fecd15df6bf1cbdd58fe9a8e337b2d45cd61a4fb9d821e4114
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6757807"
---
# <a name="inventory-forecasts"></a>Birgðaspár

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er útskýrt hvernig á að skoða og búa til birgðaspár. Hægt er að stofna og skoða framboðs- og eftirspurnarspárlínur fyrir vörur, vöruflokka, úthlutunarlykla vöru, viðskiptavinalykla, viðskiptavinaflokka, lánardrottnalykla og lánardrottnaflokka.

Fyrir hverja spárlínu er hægt að velja spárlíkanið sem er notað. Síðan er hægt að tilgreina vöruna eða vöruflokkinn auk magns eða færsluupphæðar. Einnig er hægt að setja upp tímaáætlun fyrir úthlutun spármagns.

Framboðs- og eftirspurnarspárlínurnar búa til birgðaspá fyrir sömu samsetningu vöru og líkans. Þessi birgðaspá táknar jafnvægi milli framboðs og eftirspurnar sem voru færðar inn fyrir sömu vöruna. Ekki er hægt að breyta henni. Birgðaspáin hjálpar birgðastjórnunarteyminu að fara yfir væntanlegar breytingar á lagerbirgðum vöru á komandi tímabili sem hefur verið spáð.

Þegar búið er setja inn eftirspurn og/eða framboð er hægt að keyra spáráætlun til að reikna brúttóþörf á efnum og afköstum og útbúa áætlaðar pantanir.

## <a name="view-and-manually-enter-forecast-lines"></a><a name="manual-entry"></a>Skoða og færa handvirkt inn spárlínur

Notið þetta ferli til að stofna handvirkt spárlínur fyrir afurðir.

Einnig eru aðrar leiðir til að stofna spárlínur:

- [Myndun tölfræðilegrar grunnlínuspár](generate-statistical-baseline-forecast.md).
- [Flytja inn eldri gögn fyrir eftirspurnarspár](import-historical-data.md).
- [Búið til spá með því að nota vefþjónustu Microsoft Azure Machine Learning](demand-forecasting-setup.md).
- [Flytja inn eftirspurnar- eða framboðsspárlínur með því að nota ramma gagnastjórnunar (ForecastDemandForecastEntryStaging og ForecastSupplyForecastEntryStaging gagnaeiningar)](../../dev-itpro/data-entities/data-entities-data-packages.md).

Eins og taflan í skrefi 1 sýnir eru mismunandi leiðir til að nálgast síðurnar sem eru notaðar.

1. Það fer eftir því hvaða gerð einingar á að stofna spá fyrir og hvernig spá á að búa til, opna framboðs-, eftirspurnar- eða birgðaspársíðu eins og lýst er í eftirfarandi töflu.

    | Eining | Fyrirmæli |
    |---|---|
    | Útgefnar afurðir | <ol><li>Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.</li><li>Veljið afurðina sem á að stofna spá fyrir.</li><li>Á aðgerðasvæðinu, í flipanum **Áætlun**, í hópnum **Spá**, skal velja **Eftirspurnarspá**, **Framboðsspá** eða **Birgðaspá** eftir því hvers konar spá á að vinna með.</li></ol> |
    | Útgefin afurðarafbrigði | <ol><li>Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefin afurðarafbrigði**.</li><li>Veljið afbrigðið sem á að stofna spá fyrir.</li><li>Á aðgerðasvæðinu, í flipanum **Áætlun**, í hópnum **Spá**, skal velja **Eftirspurnarspá**, **Framboðsspá** eða **Birgðaspá** eftir því hvers konar spá á að vinna með.</li></ol> |
    | Vöruflokkar | <ol><li>Opnið **Birgðastjórnun \> Uppsetning \> Birgðir \> Vörulíkanaflokkar**.</li><li>Veljið vöruflokkinn sem á að stofna spá fyrir.</li><li>Á aðgerðasvæðinu skal velja **Spá \> Eftirspurn**, **Spá \> Framboði** eða **Spá \> Birgðaspá** eftir því hvers konar spá á að vinna með.</li></ol> |
    | Úthlutunarlyklar vöru | <ol><li>Opnið **Birgðastjórnun \> Uppsetning \> Spá**.</li><li>Veljið úthlutunarlykil vörunnar sem á að stofna spá fyrir.</li><li>Á aðgerðasvæðinu skal velja **Eftirspurnarspá**.</li></ol> |
    | Viðskiptavinir | <ol><li>Farið í **Aðaláætlanagerð \> Spá \> Handvirk spárfærsla \> Viðskiptavinir**.</li><li>Veljið viðskiptavin sem stofna á spá fyrir.</li><li>Á aðgerðasvæðinu skal velja **Skilgreina eftirspurnarspá**.</li></ol> |
    | Viðskiptavinaflokkar | <ol><li>Farið í **Aðaláætlanagerð \> Spá \> Handvirk spárfærsla \> Viðskiptavinaflokkar**.</li><li>Veljið viðskiptavinaflokk sem á að stofna spá fyrir.</li><li>Á aðgerðasvæðinu skal velja **Skilgreina eftirspurnarspá**.</li></ol> |
    | Lánardrottnar | <ol><li>Farið í **Aðaláætlanagerð \> Spá \> Handvirk spárfærsla \> Lánardrottnar**.</li><li>Veljið lánardrottna sem á að stofna spá fyrir.</li><li>Á aðgerðasvæðinu skal velja **Færsla** til að opna síðuna **Framboðsspá**.</li></ol> |
    | Lánardrottnaflokkar | <ol><li>Farið í **Aðaláætlanagerð \> Spá \> Handvirk spárfærsla \> Lánardrottnaflokkar**.</li><li>Veljið lánardrottnaflokk sem á að stofna spá fyrir.</li><li>Á aðgerðasvæðinu skal velja **Færsla** til að opna síðuna **Framboðsspá**.</li></ol> | 
    | Allar línur | <ul><li>Farið í **Aðaláætlanagerð \> Spá \> Eftirspurnarspárlínur** eða **Aðalætlanagerð \> Spá \> Framboðsspárlínur** eftir því hvers konar spá á að vinna með.</li></ul> |

    Síðan **Framboðsspá** eða **Eftirspurnarspá** birtist eftir því hvað valið er. Hún sýnir allar spárlínur færslunnar sem voru valdar áður en síðan var opnuð.

1. Á aðgerðasvæðinu skal velja **Ný** til að bæta spárlínu við hnitanetið á efri hluta síðunnar.
1. Á nýju línunni í reitnum **Líkan** skal velja spárlíkanið sem á að nota. Færið síðan inn aðrar upplýsingar eftir þörfum, t.d. vöru, vöruflokk, viðskiptavin eða lánardrottnalykil eða -flokk, vörumagn eða heildarupphæð færslu. Allar upplýsingar um reitina sem eru í boði á síðunum **Framboðsspá** og **Eftirspurnarspá** er að finna í síðari hlutum í þessu efnisatriði.
1. Til að dreifa spánni yfir tímabilið, í flipanum **Yfirlit**, skal velja **Úthluta spá** á tækjastikunni.
1. Nota skal reitinn **Úthlutun** til að setja upp hámarkstíma og tímabil sem eru notuð til að dreifa spármagni.

## <a name="supply-forecast-lines"></a>Línur birgðaspár

Framboðsspáin gerir kleift að stofna áætlun fyrir vörur sem þarf að kaupa. Hún segir starfsfólki innkaupa og aðfanga hvaða ætlast er til að sé pantað.

Hægt er að slá inn framboðsspá eftir vöru, vöruflokki, vöruúthlutunarlykli, lánardrottni og lánardrottnaflokki. Upplýsingar um allar leiðir til að opna síðuna **Framboðsspá** fyrir ýmsar einingar og færslur er að finna í hlutanum [Skoða og færa handvirkt inn spárlínur](#manual-entry) fyrr í þessu efnisatriði.

Efri hluti síðunnar **Framboðsspá** býður upp á hnitanet yfir framboðsspárlínur og safn af flipum sem hægt er að nota til að skoða og setja inn frekari upplýsingar um valda spárlínu. Í neðri hluta síðunnar er að finna hnitanet fyrir **Úthlutun**.

Eftirfarandi undirkaflar lýsa öllum reitum sem eru tiltækir í hverjum flipa og öllum skipunum sem eru tiltækar á aðgerðarsvæði síðunnar og á tækjastikunni í flipanum **Yfirlit**.

### <a name="action-pane-commands-on-the-supply-forecast-page"></a>Skipanir aðgerðasvæðis á síðu framboðsspár

Eftirfarandi tafla lýsir þeim skipunum sem eru tiltækar á aðgerðarsvæði síðunnar **Framboðsspá**.

| Skipun | lýsing |
|---|---|
| Vista | Vista núverandi stillingar. |
| Breyta | Virkið stillingar á síðunni sem á að breyta. |
| Nýjar | Bætið spárlínu við efra hnitakerfið. |
| Eyða | Fjarlægið valda spárlínu úr efra hnitanetinu. |
| Spástöður | Skoða spástöður sem hafa verið reiknaðar fyrir valið líkanakenni línu fyrir núverandi fjárhagsár. Stöðurnar skiptast eftir tímabili (mánuði). |
| Sjóðstreymisspár | Skoðið spáfærslur sem hafa verið úthlutaðar í fjárhag. Frekari upplýsingar er að finna í [Sjóðstreymisspá](../../finance/cash-bank-management/cash-flow-forecasting.md). |
| Birtar víddir \> birgða | Veljið birgðavíddirnar sem eiga að sjást í hnitanetinu í flipanum **Yfirlit**. |

### <a name="toolbar-commands-on-the-overview-tab-of-the-supply-forecast-page"></a>Skipanir tækjastiku í yfirlitsflipanum á síðu framboðsspár

Eftirfarandi tafla lýsir þeim skipunum sem eru tiltækar á tækjastiku flipans **Yfirlit** á síðunni **Framboðsspá**.

| Skipun | lýsing |
|---|---|
| Úthluta spá | Ef notuð er úthlutunaraðferð skal mynda hverja áætlunarlínu fyrir sig fyrir spáfærsluna. Magni línunnar er síðan dreift eftir dagsetningu (samkvæmt völdu tímabili), magni og upphæð fyrir allan tímann. |
| Magnuppfærsla | Opnið síðuna **Breyta spáfærslum**. (Sjá hlutann [Spárfærslur magnuppfærslu](#bulk-update) síðar í þessu efnisatriði.) |
| Birgðaspá | Opnið yfirlit síðunnar **Birgðaspá** sem er síuð fyrir valda samsetningu vöru/líkans. (Sjá hlutann [Birgðaspá](#inventory-forecast) síðar í þessu efnisatriði.) |
| Stofna vöruþörf | Opnið svarglugga þar sem hægt er að búa til vöruþörf og sölupöntun eða færslubókarlínur vöru fyrir spáfærslur sem tengjast verki. Þótt þessi skipun sé tiltæk fyrir bæði framboðsspárlínur og eftirspurnarspárlínur, er ekki hægt að nota hana á síðunni **Framboðsspá**. |

### <a name="the-overview-tab-on-the-supply-forecast-page"></a>Yfirlitsflipinn á síðu framboðsspár

Eftirfarandi tafla lýsir reitunum í flipanum **Yfirlit** á síðunni **Framboðsspá**.

| Svæði | lýsing |
|---|---|
| **Tegund** | Spárlíkan sem færslan er tengd við. |
| **Dagsetning** | Upphafsdagsetning færslunnar. |
| **Lykill lánardrottins** | Lánardrottnalykillinn sem færslan tengist. |
| **Lánardrottnaflokkur** | Lánardrottnaflokkurinn sem færslan tengist. |
| **Vörunúmer** | Kennimerki vörunnar. |
| **Vöruflokkur** | Vöruflokkurinn sem færslan tengist. |
| **Úthlutunarlykill vöru** | Vöruúthlutunarlykillinn sem tengist spánni. |
| **Þyngd afurðar, magn** | Spármagnið í tilgreindri einingu framleiðsluþyngdar. |
| **Þyngd afurðar, eining** | Eining framleiðsluþyngdar sem varan er keypt í. Gildið er sótt sjálfkrafa úr uppsetningu vörunnar. |
| **Magn** | Spármagnið í tilgreindri innkaupaeiningu. |
| **Eining** | Einingin sem varan er keypt í. Gildið er sótt sjálfkrafa úr uppsetningu vörunnar. Hins vegar er hægt að breyta henni ef umreikningur eininga eru settur upp. |
| **Upphæð** | Brúttóupphæð, mínus afsláttur, sem spárfærslan leggur til spárinnar. |
| **Gjaldmiðill** | Gjaldmiðillinn sem er notaður fyrir spárfærsluna. Sjálfgefinn gjaldmiðill er sjálfkrafa færður inn en hægt er að velja annan gjaldmiðil. |
| (Aðrar víddir) | Hægt er að sýna viðbótarvíddir sem dálka í hnitanetinu. Til að velja viðbótarvíddir sem eru sýndar skal velja **Sýna víddir** á aðgerðasvæðinu. |

### <a name="the-general-tab-on-the-supply-forecast-page"></a>Almenni flipinn á síðu framboðsspár

Flipinn **Almennt** sýnir frekari upplýsingar um línuna sem er valin í flipanum **Yfirlit**. Sumar þessara upplýsinga eru endurteknar í flipanum **Yfirlit**. Eftirfarandi tafla lýsir reitunum sem eru eingöngu í flipanum **Almennt**.

| Svæði | lýsing |
|---|---|
| Skýrsla | Stillið þennan valkost á *Já* til að hafa færsluna með í skýrslugerð. |
| Athugasemdir | Sláið inn allar athugasemdir sem þú ert með um spárfærsluna. |
| Í gangi | Veljið þennan gátreit til að hafa færsluna með í skýrslugerð fjárhagsáætlunar. |
| Telja með í sjóðsstreymisspám | Veljið þennan gátreit til að úthluta spáfærslunni til fjárhags. Ekki er hægt að breyta stillingu þessa gátreits fyrir færslur skýrslugerðar. |
| VSK-flokkur | Skattflokkurinn sem er notaður til að tilgreina skatt fyrir spáfærsluna. |
| VSK-flokkur vöru | Skattflokkur vöru sem er notaður til að tilgreina skatt fyrir spáfærsluna. |
| Aðferð | <p>Veljið aðferðina sem er notuð til að úthluta spáfærslunni:</p><ul><li>**Ekkert** – Engin úthlutun á sér stað.</li><li>**Tímabil** – Spá sama magni fyrir hvert tímabil. Ef þetta gildi er valið skal tilgreina magn í reitnum **Hvert** og tímaeiningu í reitnum **Eining**.</li><li>**Lykill** – Úthlutið spá samkvæmt úthlutunarlykli tímabils sem var tilgreindur í reitnum **Tímabilslykill**. Hægt er að nota þessa aðferð þegar óskað er eftir að taka tillit til árstíðarbundinna frávika.</li></ol>|
| Eftir | <p>Færið inn fjölda tímabila fram í tímann sem spáin er framlengd um. Þessi reitur er aðeins í boði ef valið er *Tímabil* í reitnum **Aðferð**.</p><p>Til dæmis er hægt að velja *Tímabil* í reitnum **Aðferð**, slá inn *1* í reitinn **Hvern** og velja *Mánuðir* í reitnum **Eining**. Í reitnum **Lok** skal tilgreina lokadagsetningu sem nær eitt ár fram í tímann. Í þessu tilviki verður búin til ein spárlína fyrir hvern mánuð komandi árs, byggt á vörunni og magninu sem er tilgreint í hauslínunni.</p> |
| Eining | Veljið einingu tímabils: *Dagar*, *Mánuðir* eða *Ár*. Úthlutun er síðan í samræmi við fjölda daga, mánaða eða ára sem tilgreint er í reitnum **Hvert**.|
| Tímabilslykill | Tilgreinið úthlutunarlykil tímabils. |
| Lýkur | Tilgreinið lokadagsetningu þegar reitirnir **Hvert** og **Eining** eru notaðir. |

### <a name="the-item-tab-on-the-supply-forecast-page"></a>Vöruflipinn á síðu framboðsspár

Flipinn **Vara** sýnir frekari upplýsingar um línuna sem er valin í flipanum **Yfirlit**.

Hnitanetið efst í flipanum **Vara** endurtekið upplýsingarnar sem eru einnig sýndar í flipanum **Yfirlit**. Auk þess inniheldur hann flipann **Einingarverð** sem sýnir innkaupaverðið fyrir einingafjöldann sem er gefinn upp í reitnum **Eining**. Einingaverðið er sjálfkrafa sótt úr vöruuppsetningu en hægt er að breyta því.

Reitirnir fyrir neðan hnitanetið veita frekari upplýsingar um vöru. Sumar þessar upplýsingar eru endurteknar í flipanum **Yfirlit**. Eftirfarandi tafla lýsir reitunum sem eru eingöngu í flipanum **Vara**.

| Svæði | lýsing |
|---|---|
| Verðeining | Einingafjöldinn sem innkaupaverðið gildir um. Gildið er sjálfkrafa sótt úr vörutöflunni en því má breyta. |
| Gjöld á innkaupum | Föst gjöld á innkaupaverðinu. Gjöldin eru óháð magni. |
| Afsláttarprósenta | Afsláttur í prósentum. |
| Afsláttarupphæð | Afslátturinn sem upphæð á hverja sölueiningu. |
| Brúttó upphæð | Upphæðin þegar engir afslættir eru notaðir. |
| Magn | Færslumagnið í birgðaeiningu vörunnar. |
| Undiruppskrift | Uppskriftarnúmer (BOM-númer) tilgreindrar undiruppskriftar. |
| Undirleið | Leiðanúmer tilgreindrar undirleiðar. |

### <a name="the-financial-dimensions-tab-on-the-supply-forecast-page"></a>Fjárhagsvíddarflipinn á síðu framboðsspár

Flipinn **Fjárhagsvíddir** sýnir öll fjárhagsvíddargildi fyrir línuna sem er valin í flipanum **Yfirlit**.

### <a name="the-inventory-dimensions-tab-on-the-supply-forecast-page"></a>Birgðavíddarflipinn á síðu framboðsspár

Flipinn **Birgðavíddir** sýnir öll birgðavíddargildi fyrir línuna sem er valin í flipanum **Yfirlit**.

### <a name="the-allocation-grid-on-the-supply-forecast-page"></a>Úthlutunarhnitið á síðu framboðsspár

Ef notaður er úthlutunarlykill vöru eða ef færð hefur verið inn vöruspá fyrir eitt eða fleiri tímabil fram í tímann, er hægt að úthluta spánni með því að velja **Úthluta spá** á tækjastikunni í flipanum **Yfirlit**. Magninu er þá úthlutað samkvæmt því sem tilgreint er í línunum í hnitanetinu **Úthlutun**.

## <a name="demand-forecast-lines"></a>Eftirspurnarspárlínur

Framboðsspáin gerir kleift að færa inn eða búa til framboð fyrir viðskiptavin. Hún hjálpar starfsfólki sölu- og markaðsmála að láta starfsfólk aðaláætlanagerðar vita um væntanlegt framboð á komandi spártímabili.

Hægt er að slá inn eftirspurnarspá eftir vöru, vöruflokki, vöruúthlutunarlykli, viðskiptavini eða viðskiptavinaflokki. Upplýsingar um allar leiðir til að opna síðuna **Eftirspurnarspá** fyrir ýmsar einingar og færslur er að finna í hlutanum [Skoða og færa handvirkt inn spárlínur](#manual-entry) fyrr í þessu efnisatriði.

Efri hluti síðunnar **Eftirspurnarspá** býður upp á hnitanet yfir eftirspurnarspárlínur og safn af flipum sem hægt er að nota til að skoða og setja inn frekari upplýsingar um valda spárlínu. Í neðri hluta síðunnar er að finna hnitanet fyrir **Úthlutun**.

Eftirfarandi undirkaflar lýsa öllum reitum sem eru tiltækir í hverjum flipa og öllum skipunum sem eru tiltækar á aðgerðarsvæði síðunnar og á tækjastikunni í flipanum **Yfirlit**.

### <a name="action-pane-commands-on-the-demand-forecast-page"></a>Skipanir aðgerðasvæðis á síðu eftirspurnarspár

Eftirfarandi tafla lýsir þeim skipunum sem eru tiltækar á aðgerðarsvæði síðunnar **Eftirspurnarspá**.

| Skipun | lýsing |
|---|---|
| Vista | Vista núverandi stillingar. |
| Breyta | Virkið stillingar á síðunni sem á að breyta. |
| Nýjar | Bætið spárlínu við efra hnitakerfið. |
| Eyða | Fjarlægið valda spárlínu úr efra hnitanetinu. |
| Spástöður | Skoða spástöður sem hafa verið reiknaðar fyrir valið líkanakenni línu fyrir núverandi fjárhagsár. Stöðurnar skiptast eftir tímabili (mánuði). |
| Sjóðstreymisspá | Skoðið spáfærslur sem þarf að úthluta til fjárhags. Frekari upplýsingar er að finna í [Sjóðstreymisspá](../../finance/cash-bank-management/cash-flow-forecasting.md). |
| Sýna víddir | Veljið afurðar-, geymslu- og rakningarvíddirnar sem eiga að sjást í hnitanetinu í flipanum **Yfirlit**. |
| Forskoðun á fjárhagslykli | Skoðið fjárhagsfærslurnar fyrir valda færslu. |
| Flytja tilboðslínur | Flytja tilboðslínur í valið verk. |

### <a name="toolbar-commands-on-the-overview-tab-of-the-demand-forecast-page"></a>Skipanir tækjastiku í yfirlitsflipanum á síðu eftirspurnarspár

Eftirfarandi tafla lýsir þeim skipunum sem eru tiltækar á tækjastiku flipans **Yfirlit** á síðunni **Eftirspurnarspá**.

| Skipun | lýsing |
|---|---|
| Úthluta spá | Ef notuð er úthlutunaraðferð skal mynda hverja áætlunarlínu fyrir sig fyrir spáfærsluna. Magni línunnar er síðan dreift eftir dagsetningu (samkvæmt völdu tímabili), magni og upphæð fyrir allan tímann. |
| Magnuppfærsla | Opnið síðuna **Breyta spáfærslum**. (Sjá hlutann [Spárfærslur magnuppfærslu](#bulk-update) síðar í þessu efnisatriði.) |
| Birgðaspá | Opnið yfirlit síðunnar **Birgðaspá** sem er síuð fyrir valda samsetningu vöru/líkans. (Sjá hlutann [Birgðaspá](#inventory-forecast) síðar í þessu efnisatriði.) |
| Stofna vöruþörf | Opnið svarglugga þar sem hægt er að búa til vöruþörf og sölupöntun eða færslubókarlínur vöru fyrir spáfærslur sem tengjast verki. |

### <a name="the-overview-tab-on-the-demand-forecast-page"></a>Yfirlitsflipinn á síðu eftirspurnarspár

Eftirfarandi tafla lýsir reitunum í flipanum **Yfirlit** á síðunni **Eftirspurnarspá**.

| Svæði | lýsing |
|---|---|
| **Verkheiti** | Heiti runuverksins sem var notað til að stofna spárlínuna. |
| **Tegund** | Spárlíkan sem færslan er tengd við. |
| **Dagsetning** | Upphafsdagsetning færslunnar. |
| **Viðskiptavinalykill** | Viðskiptavinalykillinn sem færslan tengist. |
| **Flokkur viðskiptavina** | Viðskiptavinaflokkurinn sem færslan tengist. |
| **Vörunúmer** | Kennimerki vörunnar. |
| **Afurðarnafn** | Lýsing vörunnar. |
| **Úthlutunarlykill vöru** | Úthlutunarlykill vörunnar sem er notaður við úthlutun birgðaspár. |
| **Sölumagn** | Færslumagn í tilgreindri sölueiningu. |
| **Eining** | Einingin sem varan er seld í. |
| **Upphæð** | Brúttóupphæð, að undanskildum afsláttum, sem spárfærslan leggur til spárinnar. |
| **Söluverð** | Söluverð fyrir þann fjölda eininga sem tilgreindur er í reitnum **Verðeining**. Gildið er sótt úr vöruuppsetningunni en því má breyta. |
| **Sölugjaldmiðill** | Gjaldmiðillinn sem er notaður fyrir spárfærsluna. Sjálfgefinn gjaldmiðill er sjálfkrafa færður inn en hægt er að velja annan gjaldmiðil. |
| **Þyngd afurðar, magn** | Spármagnið í tilgreindri einingu framleiðsluþyngdar. |
| **Þyngd afurðar, eining** | Eining framleiðsluþyngdar sem varan er seld í. Gildið er sótt sjálfkrafa úr uppsetningu vörunnar. |
| (Aðrar víddir) | Hægt er að sýna aðrar afurðar-, geymslu- og rakningarvíddir sem dálka í hnitanetinu. Til að velja viðbótarvíddir sem eru sýndar skal velja **Sýna víddir** á aðgerðasvæðinu. |

### <a name="the-general-tab-on-the-demand-forecast-page"></a>Almenni flipinn á síðu eftirspurnarspár

Flipinn **Almennt** sýnir frekari upplýsingar um línuna sem er valin í flipanum **Yfirlit**. Sumar þessara upplýsinga eru endurteknar í flipanum **Yfirlit**. Eftirfarandi tafla lýsir reitunum sem eru eingöngu í flipanum **Almennt**.

| Svæði | lýsing |
|---|---|
| Raðnúmer eftirspurnarspáfærslu | Einkvæmt númer eftirspurnarspárlínunnar. Þetta númer er búið til með því að nota númeraröðina sem er valin fyrir eftirspurnarspár á síðunni **Færibreytur aðaláætlanagerð**. |
| Vöruflokkur | Vöruflokkurinn sem færslan tengist. |
| Skýrsla | Stillið þennan valkost á *Já* til að hafa færsluna með í skýrslugerð. |
| Athugasemdir | Sláið inn allar athugasemdir sem þú ert með um spárfærsluna. |
| Í gangi | Veljið þennan gátreit til að hafa færsluna með í skýrslugerð fjárhagsáætlunar. Ekki er hægt að breyta stillingu þessa gátreits fyrir færslur skýrslugerðar. |
| Telja með í sjóðsstreymisspám | Veljið þennan gátreit til að úthluta spáfærslunni til fjárhags. Ekki er hægt að breyta stillingu þessa gátreits fyrir færslur skýrslugerðar. Frekari upplýsingar er að finna í [Sjóðstreymisspá](../../finance/cash-bank-management/cash-flow-forecasting.md). |
| VSK-flokkur | Skattflokkurinn sem er notaður til að tilgreina skatt fyrir spáfærsluna. |
| VSK-flokkur vöru | Skattflokkur vöru sem er notaður til að tilgreina skatt fyrir spáfærsluna. |
| Aðferð | <p>Veljið aðferðina sem er notuð til að úthluta spáfærslunni:</p><ul><li>**Ekkert** – Engin úthlutun á sér stað.</li><li>**Tímabil** – Spá sama magni fyrir hvert tímabil. Ef þetta gildi er valið skal tilgreina magn í reitnum **Hvert** og tímaeiningu í reitnum **Eining**.</li><li>**Lykill** – Úthlutið spá samkvæmt úthlutunarlykli tímabils sem var tilgreindur í reitnum **Tímabilslykill**. Hægt er að nota þessa aðferð þegar óskað er eftir að taka tillit til árstíðarbundinna frávika.</li><ul>|
| Eftir | <p>Færið inn fjölda tímabila fram í tímann sem spáin er framlengd um. Þessi reitur er aðeins í boði ef valið er *Tímabil* í reitnum **Aðferð**.</p><p>Til dæmis er hægt að velja *Tímabil* í reitnum **Aðferð**, slá inn *1* í reitinn **Hvern** og velja *Mánuðir* í reitnum **Eining**. Í reitnum **Lok** skal tilgreina lokadagsetningu sem nær eitt ár fram í tímann. Í þessu tilviki verður búin til ein spárlína fyrir hvern mánuð komandi árs, byggt á vörunni og magninu sem er tilgreint í hauslínunni. |
| Eining | Veljið einingu tímabils: *Dagar*, *Mánuðir* eða *Ár*. Úthlutun er síðan í samræmi við fjölda daga, mánaða eða ára sem tilgreint er í reitnum **Hvert**.|
| Tímabilslykill | Tilgreinið úthlutunarlykil tímabils sem er notaður til að úthluta spánni. Frekari upplýsingar er að finna í [Gagnaúthlutun fjárhagsáætlunargerðar](../../finance/budgeting/budget-planning-data-allocation.md). |
| Lýkur | Tilgreinið lokadagsetningu þegar reitirnir **Hvert** og **Eining** eru notaðir. |

### <a name="the-item-tab-on-the-demand-forecast-page"></a>Vöruflipinn á síðu eftirspurnarspár

Flipinn **Vara** sýnir frekari vöruupplýsingar um línuna sem er valin í flipanum **Yfirlit**. Sumar þessara upplýsinga eru endurteknar í flipanum **Yfirlit**. Eftirfarandi tafla lýsir reitunum sem eru eingöngu í flipanum **Vara**.

| Svæði | lýsing |
|---|---|
| Verðeining | Fjöldi sölueininga sem söluverðið gildir um. Gildið er sjálfkrafa sótt úr vörutöflunni en því má breyta. |
| Sölugjöld | Föst gjöld á söluverð. Gjöldin eru óháð magni. |
| Kostnaðarverð | Kostnaður gildandi spáfærslu á birgðaeiningu. Gildið er sótt úr vörutöflunni en því má breyta. |
| Afsláttarprósenta | Afsláttur í prósentum. |
| Afsláttarupphæð | Afslátturinn sem upphæð á hverja sölueiningu. |
| Brúttó upphæð | Upphæðin þegar engir afslættir eru notaðir. |
| Birgðamagn | Færslumagnið í birgðaeiningu vörunnar. |
| Nota tilgreinda uppskrift | Uppskriftarnúmer tiltekinnar uppskriftar. |
| Nota tilgreinda leið | Leiðanúmer tilgreindrar undirleiðar. |

### <a name="the-project-tab-on-the-demand-forecast-page"></a>Verkflipinn á síðu eftirspurnarspár

Flipinn **Verk** sýnir frekari verkupplýsingar um línuna sem er valin í flipanum **Yfirlit**. Sumar þessara upplýsinga eru endurteknar í flipanum **Yfirlit**, **Almennt** eða **Vara**. Eftirfarandi tafla lýsir reitunum sem eru eingöngu í flipanum **Verk**.

| Svæði | lýsing |
|---|---|
| Verkdagsetning | Dagsetning eftirspurnarspárfærslunnar. |
| Verkkenni | Kenni verksins sem núverandi færsla vísar í. |
| Fjármögnunaraðili | Uppruni fjármögnunar sem eftirspurnarspáin tengist. |
| Verkþáttarnúmer | Aðgerðin sem tengist færslu eftirspurnarspár. |
| Tegund | Kostnaðartegund núverandi færslu. |
| Línueiginleiki | Staðan sem færslan tengist. |
| Færslukenni | Kerfisauðkenni fyrir færslu eftirspurnarspár. |
| Kostnaðarupphæð | Upphæð eftirspurnarspárfærslunnar. |
| Einingarverð | Verð á hverja einingu. |
| Breytt af | Auðkenni starfsmanns sem breytti síðast valdri færslu. |
| Reikningsdagsetning | Færið inn væntanlega reikningsdagsetningu. |
| Losunardagsetning | Skoða eða breyta losunardagsetningunni. Þegar spá hefur verið stofnuð er losunardagsetningin fest við lokadagsetningu verksins. Ef verkið hefur enga lokadagsetningu er verkdagsetning notuð. Þetta reitur á við um verk á föstu verði og fjárfestingarverk. |
| Dagsetning kostnaðargreiðslu | Færa inn áætlaða dagsetningu á greiðslu innkaupa. |
| Dagsetning sölugreiðslu | Færið inn áætlaða dagsetningu á greiðslu sölu. |

### <a name="the-financial-dimensions-tab-on-the-demand-forecast-page"></a>Fjárhagsvíddarflipinn á síðu eftirspurnarspár

Flipinn **Fjárhagsvíddir** sýnir öll fjárhagsvíddargildi fyrir línuna sem er valin í flipanum **Yfirlit**.

### <a name="the-inventory-dimensions-tab-on-the-demand-forecast-page"></a>Birgðavíddarflipinn á síðu eftirspurnarspár

Flipinn **Birgðavíddir** sýnir öll birgðavíddargildi fyrir línuna sem er valin í flipanum **Yfirlit**.

### <a name="the-allocation-grid-on-the-demand-forecast-page"></a>Úthlutunarhnitið á síðu eftirspurnarspár

Ef notaður er úthlutunarlykill vöru eða ef færð hefur verið inn vöruspá fyrir eitt eða fleiri tímabil fram í tímann, er hægt að úthluta spánni með því að velja **Úthluta spá** á tækjastikunni í flipanum **Yfirlit**. Magninu er þá úthlutað samkvæmt því sem tilgreint er í línunum í hnitanetinu **Úthlutun**.

## <a name="inventory-forecast"></a><a name="inventory-forecast"></a>Birgðaspá

Á síðum framboðs- og eftirspurnarspárlínum er hnappurinn **Birgðaspá** sem opnar yfirlit síðunnar **Birgðaspá** sem er síuð fyrir sömu samsetningu vöru/líkans. Birgðaspáin táknar jafnvægi milli framboðs og eftirspurnar sem voru færðar inn fyrir sömu vöruna. Ekki er hægt að breyta henni. Birgðaspáin hjálpar birgðastjórnunarteyminu að fara yfir væntanlegar breytingar á lagerbirgðum vöru á komandi tímabili sem hefur verið spáð.

### <a name="the-action-pane-on-the-inventory-forecast-page"></a>Aðgerðarsvæðið á síðu birgðaspár

Eftirfarandi tafla lýsir þeim skipunum sem eru tiltækar á aðgerðarsvæði síðunnar **Birgðaspá**.

| Aðgerð | lýsing |
|---|---|
| Birgðaspá | Opnið yfirlit síðunnar **Birgðaspá** sem er síuð fyrir sömu samsetningu vöru/líkans/dagsetningar. |
| Eftirspurnarspá | Opnið yfirlit síðunnar **Eftirspurnarspá** sem er síuð fyrir sömu samsetningu vöru/líkans/dagsetningar. |
| Birtar víddir \> birgða | Veljið afurðar-, geymslu- og rakningarvíddirnar sem eiga að sjást í hnitanetinu **Yfirlit**. |

### <a name="the-grid-on-the-inventory-forecast-page"></a>Hnitanetið á síðu birgðaspár

Eftirfarandi tafla lýsir reitunum á síðu **Birgðaspár**.

| Svæði | lýsing |
|---|---|
| **Tegund** | Spárlíkan sem færslan er tengd við. |
| **Vörunúmer** | Kennimerki vörunnar. |
| **Dagsetning fjárhagsáætlunar** | Dagsetning spárfærslunnar. |
| **Spárgerð** | Uppruni færslunnar (*Eftirspurnarspá* eða *Framboðsspá*). |
| **Þyngd afurðar, magn** | Spáð magn í einingu framleiðsluþyngdar. |
| **Magn** | Spáð magn í birgðaeiningunni. |
| **Þyngd afurðar, uppsöfnuð** | Uppsafnað spármagn í einingu framleiðsluþyngdar þegar mörgum spárlínum hefur verið safnað saman fyrir sömu vöruna. |
| **Undiruppskrift** | Uppskriftarnúmer tilgreindrar undiruppskriftar. |
| **Undirleið** | Leiðanúmer tilgreindrar undirleiðar. |
| (Aðrar víddir) | Hægt er að sýna viðbótarvíddir sem dálka í hnitanetinu. Til að velja viðbótarvíddir sem eru sýndar skal velja **Birgðir \> Sýna víddir** á aðgerðasvæðinu. |

## <a name="bulk-update-forecast-transactions"></a><a name="bulk-update"></a>Spárfærslur magnuppfærslu

Notið þetta ferli til að stofna spáfærslulínur. Hægt er að afrita, breyta og eyða spárfærslulínum.

1. Á síðu eftirspurnar- og framboðsspárlínum skal velja **Magnuppfærsla**.
1. Í svarglugganum skal velja **Sía**.
1. Í flipanum **Svið** skal velja skilyrði sem auðkennir gögn upprunaspár sem ætlunin er að afrita, breyta eða eyða. Þessi gögn gætu falið í sér spárlíkan, vörunúmer, og viðskiptavinalykil.
1. Veljið **Í lagi** til að staðfesta valið.

    Eftir að gögnin hafa verið valin er hægt að nota svargluggann **Breyta spárfærslum** til að skilgreina hvernig á að afrita, breyta eða eyða þeim.

    > [!NOTE]
    > Síunarskrefið er skilyrði til að nota virknina **Fjöldabreyting**. Ef þessu er sleppt velur kerfið og uppfærir **allar** spárlínur. Þar af leiðandi gætirðu óvart tvítekið eða fjarlægt færslur.

1. Í hlutanum **Stjórnun** er valið hvort eigi að afrita, uppfæra eða eyða völdum spárfærslum.
1. Notið hlutann **Breytingar á reit** til að breyta færibreytum spárinnar. Veljið gátreitinn fyrir færibreytu og veljið svo úr tiltækum valkostum. Til dæmis er hægt að velja gátreitinn **Líkan** og síðan velja númer spárlíkans. Núverandi spárlínur eru afritaðar í spárlíkanið sem valið er.
1. Notið hlutann **Breyting á tímabili** til að færa upphafs- og lokadagsetningar spár fram og aftur. Veljið gátreitinn og notið síðan magn- og tímabilsreitina til að skilgreina hvernig færa á dagsetningar spárinnar. Hægt er að færa inn neikvætt magn til að færa upphafsdagsetninguna fram á við (þ.e. fyrr).

    Til dæmis til að fresta upphafsdagsetningu spárfærslunnar um sex mánuði er gátreiturinn valinn, fært inn *6* sem magnið og *Mánuðir* valdir sem tímabilið.

1. Notið hlutann **Réttur reitur** til að uppfæra raunveruleg spárgögn. Í reitnum **Reitur** skal velja skilyrðið sem á að breyta. Í reitinn **Stuðull** skal færa inn margföldunarstuðul til að nota á valið skilyrði eða færa inn fasta til að bæta eða draga frá. Veljið til dæmis *Magn* sem skilyrði og færið inn stuðul upp á *1,5* til að margfalda vörumagnið um 1,5. Færið annars inn fastann *-25* til að minnka magn vörunnar um 25 einingar.
1. Notið hlutann **Fjárhagsvíddir** til að uppfæra fjárhagsvíddir spárlína. Veljið fjárhagsvíddir sem á að breyta og sláið síðan inn gildi sem á að nota á valdar víddir.
1. Veldu **Í lagi** til að gera breytinguna.

## <a name="use-forecasts-with-master-planning"></a>Nota spár með aðaláætlanagerð

Eftir að þú hefur slegið inn spá um eftirspurn og/eða framboð getur þú tekið spána með í áætlanagerð til að taka tillit til væntanlegrar eftirspurnar og/eða framboðs í keyrslu áætlanagerðar. Þegar spár eru teknar með í aðaláætlanagerð eru brúttóþarfir fyrir efni og afkastagetu reiknaðar og áætlaðar pantanir eru myndaðar.

### <a name="set-up-a-master-plan-to-include-an-inventory-forecast"></a>Setja upp aðaláætlun með birgðaspá

Til að setja upp aðaláætlun þannig að hún taki með birgðaspá skal fylgja þessum skrefum.

1. Farið í **Aðaláætlanagerð \> Uppsetning \> Áætlanir \> Aðaláætlanir**.
1. Veljið fyrirliggjandi áætlun eða stofna nýja áætlun.
1. Á flýtiflipanum **Almennt** stillirðu eftirfarandi reiti:

    - **Spárlíkan** – Veljið spálíkanið sem á að nota. Þetta líkan verður tekið með þegar framboðstillögur eru myndaðar fyrir núverandi aðaláætlun.
    - **Taka með framboðsspá** – Stillið þennan valkost á *Já* til að taka með framboðsspá í gildandi aðaláætlun. Ef hann er stilltur á *Nei* eru færslur framboðsspár ekki teknar með í aðaláætluninni.
    - **Taka með eftirspurnarspá** – Stillið þennan valkost á *Já* til að taka með eftirspurnarspá í gildandi aðaláætlun. Ef það er stillt á *Nei* eru eftirspurnarspárfærslur ekki teknar með í aðaláætluninni.
    - **Aðferð sem er notuð til að minnka spárþarfir** -Veljið aðferðina sem á að nota til að minnka spárþarfir. Frekari upplýsingar er að finna í [Minnkunarlyklar samkvæmt spá](planning-optimization/demand-forecast.md#reduction-keys).

1. Á flipanum **Tímamörk í dögum** er hægt að stilla eftirfarandi reiti til að tilgreina tímabilið sem spáin er höfð með í:

    - **Spáráætlun** – Stillið þennan valkost á *Já* til að hnekkja tímamörkum spáráætlunarinnar sem eiga uppruna sinn í einstökum þekjuflokkum. Stillið þetta á *Nei* til að nota gildin úr einstökum þekjuflokkum fyrir núverandi aðaláætlun.
    - **Spátímatímabil** – Ef **Spáráætlun** valkosturinn er stilltur á *Já* skal tilgreina dagafjöldann (frá deginum í dag) sem á að nota eftirspurnarspá fyrir.

    > [!IMPORTANT]
    > Valkosturinn **Spáráætlun** er ekki enn studdur í fínstillingu skipulagningar.

### <a name="run-a-master-plan-that-includes-an-inventory-forecast"></a>Keyra aðaláætlun sem inniheldur birgðaspá

Til að keyra aðaláætlun sem inniheldur birgðaspá skal fylgja þessum skrefum.

1. Farið í **Aðaláætlanagerð \> Vinnusvæði \> Aðaláætlanagerð**.
1. Í reitinn **Aðaláætlun** skal færa inn eða velja aðaláætlun sem var sett upp í ferlinu hér á undan.
1. Í reitnum **Aðaláætlanagerð** skal velja **Keyra**.
1. Í svarglugganum **Aðaláætlanagerð** skal stilla valkostinn **Rekja vinnslutíma** á *Já*.
1. Í reitinn **Fjöldi þráða** skal færa inn tölu.
1. Á flýtiflipanum **Færslur til að hafa með** velurðu **Sía**.
1. Venjulegur svargluggi fyrirspurnarritils birtist. Í flipanum **Svið** skal velja línuna þar sem reiturinn **Reitur** er stilltur á *Vörunúmer*.
1. Í reitnum **Skilyrði** skal velja vörunúmerið sem hafa á með í áætluninni.
1. Veljið **Í lagi**.

Til að skoða reiknaðar þarfir skal opna síðuna **Brúttóþörf**. Til dæmis á síðunni **Útgefnar afurðir**, á aðgerðasvæðinu, í flipanum **Áætlun**, í hópnum **Kröfur**, skal velja **Brúttóþörf**.

Til að skoða áætlaðar pantanir sem eru útbúnar er farið í **Aðaláætlanagerð \> Almennar \> Áætlaðar pantanir** og velja viðeigandi spárætlun.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Yfirlit eftirspurnarspár](introduction-demand-forecasting.md)
- [Uppsetning eftirspurnarspár](demand-forecasting-setup.md)
- [Myndun tölfræðilegrar grunnlínuspár](generate-statistical-baseline-forecast.md)
- [Gera handvirkar leiðréttingar á grunnlínuspánni](manual-adjustments-baseline-forecast.md)
- [Aðaláætlanagerð með eftirspurnarspám](planning-optimization/demand-forecast.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
