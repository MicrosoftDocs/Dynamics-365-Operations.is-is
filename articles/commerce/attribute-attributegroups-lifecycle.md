---
title: Stjórna eigindum og eigindaflokkum
description: Þessi grein lýsir því hvernig á að stjórna eiginleikum og eigindahópum til að lýsa vörum og eiginleikum þeirra í Microsoft Dynamics 365 Commerce.
author: ashishmsft
ms.date: 08/31/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2018-03-30
ms.openlocfilehash: aad448ea733aabdff3dc4438dcb682d49e0665c0
ms.sourcegitcommit: 09d4805aea6d148de47c8ca38d8244bbce9786ce
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/31/2022
ms.locfileid: "9386973"
---
# <a name="manage-attributes-and-attribute-groups"></a>Stjórna eigindum og eigindaflokkum

[!include [banner](includes/banner.md)]

Þessi grein lýsir því hvernig á að stjórna eiginleikum og eigindahópum til að lýsa vörum og eiginleikum þeirra í Microsoft Dynamics 365 Commerce.

*Eiginleikar* veita leið til að lýsa vörum og eiginleikum þeirra í gegnum notendaskilgreinda reiti. Sem dæmi má nefna minnisstærð, getu harða disksins og Energy Star samræmi.

Eigindir má tengja við mismunandi Commerce-einingar, eins og afurðaflokkar og rásir, og hægt er að setja sjálfgefin gildi fyrir þær. Þegar eiginleikar eru tengdir vöruflokkum eða rásum erfa vörur þessar eigindir og sjálfgefin gildi þeirra. Hægt er að hnekkja sjálfgefnum eigindargildum á einstaka vörustigi, á rásarstigi eða í vörulista.

Til dæmis gæti dæmigerð sjónvarpsafurð haft eftirfarandi eiginleika.

| Tegund   | Eigind           | Möguleg gildi eru:                        | Sjálfgildi |
|------------|---------------------|-------------------------------------------|---------------|
| Sjónvarp og myndbönd | Vörumerki               | Öll gild gildi vörumerkja                     | Ekkert          |
| Sjónvarp         | Stærð skjás         | 20–85 tommur                              | 55 tommur     |
|            | Lóðrétt upplaus | 4K (2160p), Full HD (1080p) eða HD (720p) | 4K (2160p)    |
|            | Endurnýjunarhraða skjánum | 60hz, 120hz eða 240hz                     | 60hz          |
|            | HDMI inntök         | 0–10                                      | 3             |

## <a name="attributes-and-attribute-types"></a>Eigindir og gerðir eiginda

Eigindir eru byggðar á *gerðum eiginda*. Eigindartegund auðkennir tegund gagna sem hægt er að slá inn fyrir tiltekna eigind. Eftirfarandi eiginleikategundir eru studdar í Commerce:

- **Gjaldmiðill** – Þessi gerð styður gildi gjaldmiðils. Hægt er að afmarka hana (þ.e. hún getur studd svið gilda) eða skilja eftir opna.
- **DateTime** – Þessi gerð styður gildi dagsetningar og tíma. Hægt er að afmarka hana eða skilja eftir opna.
- **Tugastafir** – Þessi gerð styður númeragildi með tugasætum. Hún styður einnig mælieiningu. Hægt er að afmarka hana eða skilja eftir opna.
- **Heiltala** – Þessi gerð styður númeragildi. Hún styður einnig mælieiningu. Hægt er að afmarka hana eða skilja eftir opna.
- **Texti** – Þessi gerð styður textagildi. Það styður einnig fyrirfram skilgreint sett af mögulegum gildum þegar **Fastur listi** stillingin er virkjuð.
- **Boole-gildi** – Þessi gerð styður tvíundargildi (**satt** eða **rangt**).
- **Tilvísun** - Þessi gerð vísar í aðrar eigindir.

> [!NOTE]
> Vegna [takmarkanir á Azure leitarvísitölunni](/rest/api/searchservice/data-type-map-for-indexers-in-azure-search), hinn **Aukastafur** tegund eiginda er ekki studd fyrir skýknúna leitarupplifun. Azure Cognitive Search styður ekki umbreytingu **Aukastafur** eiginleikategundir til **Edm.Tvöfaldur** gerðir markvísitölusviða, vegna þess að þessi umbreyting myndi draga úr nákvæmni.

### <a name="set-up-attribute-types"></a>Setja upp eigindagerðir

Til að setja upp eigindagerðir skaltu fylgja skrefunum í þessu dæmi.

1. Skráðu þig inn á höfuðstöðvar Commerce sem sölustjóri.
1. Fara til **Vöruupplýsingastjórnun \> Uppsetning \> Flokkar og eiginleikar \> Eiginleikagerðir**.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Í **Heiti eigindartegundar** reit, slá inn **Tegund poka**.
1. Í reitnum **Gerð** skal velja **Texti**.
1. Stilltu **Fastur listi** valmöguleika til **Já**.
1. Á **Gildi** Flýtiflipi, veldu **Bæta við**.
1. Á nýju röðinni, í **Gildi** reit, slá inn **Poki**.
1. Bættu við fimm línum í viðbót. Í **Gildi** reit hvers, sláðu inn annað gildi: **Kúpling**, **·**, **·**, **·**, eða **Veski**.
1. Í aðgerðarúðunni skal velja **Vista**.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Í **Heiti eigindartegundar** reit, slá inn **Sólgleraugu vörumerki**.
1. Í reitnum **Gerð** skal velja **Texti**.
1. Stilltu **Fastur listi** valmöguleika til **Já**.
1. Á **Gildi** Flýtiflipi, veldu **Bæta við**.
1. Á nýju röðinni, í **Gildi** reit, slá inn **Ray bann**.
1. Bættu við tveimur línum í viðbót. Í **Gildi** reit hvers, sláðu inn annað gildi: **Flugmaður** eða **Oakley**.
1. Í aðgerðarúðunni skal velja **Vista**.

![Síða um eiginleikategundir.](media/AttributeType_2022Series.png)

### <a name="set-up-an-attribute"></a>Setja upp eigind

Til að setja upp eigind skaltu fylgja skrefunum í þessu dæmi.

1. Skráðu þig inn á höfuðstöðvar Commerce sem sölustjóri.
1. Fara til **Vöruupplýsingastjórnun \> Uppsetning \> Flokkar og eiginleikar \> Eiginleikar**.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Í **Nafn** reit, slá inn **Tegund poka**.
1. Í **Tegund eiginda** reit, veldu **Tegund poka**.
1. Í aðgerðarúðunni skal velja **Vista**.

![Eiginleikasíðu.](media/Attribute_2022Series.png)

## <a name="attribute-metadata"></a>Lýsigögn eiginda

*Lýsigögn eiginda* leyfir þér að velja valkosti til að tilgreina hvernig eigindin fyrir hverja vöru eigi að haga sér. Til dæmis er hægt að velja hvort eiginda sé krafist, hvort hægt sé að nota þær við leit og hvort hægt sé að nota þær sem síu.

Fyrir afurðir er hægt að hnekkja á lýsigögnum eiginda á stigi rásar.

Eiginleiki **Eiginleikar** síða inniheldur nokkra valkosti sem tengjast lýsigögnum eiginda. Til dæmis, ef þú stillir á **Hægt að betrumbæta** valmöguleika til **Já** undir **Eiginleikalýsigögn fyrir viðskiptarásir**, verður eigindin sýnd til að betrumbæta eða sía vörur á leitarniðurstöðum og flokkaskoðunarsíðum. Til að stilla eigind sem betrumbættan verður þú fyrst að velja **Síustillingar** á aðgerðarrúðunni og staðfestu síustillingarnar fyrir eigindina.

## <a name="filter-settings-for-attributes"></a>Síustillingar fyrir eigindir

Síustillingar fyrir eiginleika leyfa þér að skilgreina hvernig eiginleikasíur eru sýndar á sölustað (POS). Til að fá aðgang að síustillingum fyrir eigind, á eigindinni **Eiginleikar** síðu, á aðgerðarrúðunni, veldu **Síustillingar**.

The **Síustillingar** síða inniheldur eftirfarandi reiti:

- **Heiti** – Að sjálfgefnu er svæðið stillt á heiti eigindar. Þó er hægt að breyta gildinu.
- **Birtingarkostir** – Eftirtaldir valkostir eru í boði:

    - **Stakt gildi** – Þessi valkostur er tiltækur fyrir eftirfarandi gerðir eiginda: **Boole-gildi**, **Gjaldmiðil**, **Tugastaf**, **Heiltölu** og **Texta**. Það gerir aðeins kleift að velja eitt gildi fyrir hreinsunaraðila á vörulistasíðum, svo sem flokkaskoðun og vöruleitarniðurstöðusíðum.
    - **Mörg gildi** – Þessi valkostur er tiltækur fyrir eftirfarandi gerðir eiginda: **Gjaldmiðil**, **Tugastaf**, **Heiltölu** og **Texta**. Það gerir kleift að velja mörg gildi fyrir eigindina í viðskiptavininum, til að betrumbæta.

- **Birtingarstjórnun** – Eftirtaldir valkostir eru í boði:

    - **Listi** – Þessi valkostur er tiltækur fyrir allar gerðir eiginda.
    - **Svið** – Þessi valkostur er tiltækur fyrir eftirfarandi gerðir eiginda: **Gjaldmiðil**, **Tugastaf** og **Heiltölu**.
    - **Sleði** – Þessi valkostur er tiltækur fyrir eftirfarandi gerðir eiginda: **Gjaldmiðil**, **Tugastaf** og **Heiltölu**.
    - **Sleði með stiku** – Þessi valkostur er tiltækur fyrir eftirfarandi gerðir eiginda: **Gjaldmiðil**, **Tugastaf** og **Heiltölu**.

- **Viðmiðunargildi** – Þessi stilling er nauðsynleg ef valið var **Svið** sem gerð birtingarstjórnunar. Hægt er að skilgreina gildi með því að nota semíkommu (;) sem afmarkara.

    Til dæmis, fyrir a **Rúmmál poka** eigind sem hefur eigindartegund af **Heiltala**, gæti þröskuldurinn verið **10; 20; 50; 100; 200; 500; 1000; 5000**. Í þessu tilviki sýnir sölustaðurinn eftirfarandi afmarkanir. Svið sem eru ekki með neinar vörur í niðurstöðusettinu munu birtast dempuð.

    - Færri en 10
    - 10 – 20
    - 20 – 50
    - 50 – 100
    - 100 – 200
    - 200 – 500
    - 500 eða fleiri

Síustillingar fyrir eiginleika eiga aðeins við um vörueiginleika og hægt er að nota þær til að fínstilla vöruleit og niðurstöður flokkaskoðunar. Þau eiga ekki við um viðskiptavinaleit eða pöntunarleit, þó hægt sé að nota sömu eiginleika til að auðga upplýsingar um viðskiptavini eða pöntun.

Í sjálfgefnum viðskiptaeiningum er enginn stuðningur utan kassa tiltækur fyrir **Skjárstýring** síunarstillingar eins og **Svið**, **·**, og **Renna með stöngum**. The **Svið** og **Renna** stillingar eru áfram studdar fyrir POS lausnir, en **Renna með stöngum** stilling á við um arfleifð SharePoint netverslun og heldur áfram að vera fáanleg fyrir samþættingu þriðja aðila og sérsniðnar aðstæður.

Við mælum með því að fínstillanlegir eiginleikar hafi eiginleikann **Texti** tegund þar sem **Fastur listi** valkosturinn er virkur og að þú haldir listann viðráðanlegri (allt að 100–200 einstök gildi). Ef hreinsunartæki mun hafa 1.000 eða fleiri einstök gildi, er réttara að nota eiginleika **Texti** tegund þar sem **Fastur listi** valkosturinn er óvirkur.

Þýðingar eru mikilvægar fyrir eigindaheiti og gildi þeirra. Fyrir eiginleika á **Texti** tegund þar sem **Fastur listi** valmöguleikinn er virkur geturðu skilgreint þýðingar fyrir eigindagildin undir **Tegund eiginda**. Fyrir hverja aðra eigindategund geturðu skilgreint þýðingar á síðunni þar sem þú skilgreinir eigindagildin. Til dæmis, fyrir eiginleika á **Texti** tegund, getur þú skilgreint þýðingar fyrir sjálfgefið gildi á eigindinni **Eiginleikar** síðu. Hins vegar, ef þú hnekkir sjálfgefnu gildinu á vörustigi geturðu skilgreint þýðingar fyrir eigindina á vörunni **Eiginleikar vöru** síðu.

Eftir að eigind hefur verið merkt sem endurbættanleg fyrir rás, ættir þú ekki að uppfæra eigindagerðina. Annars hefur þú áhrif á birtingu vörugagna í leitarvísitölunni. Þess í stað mælum við með því að þú búir til nýja eigind fyrir nýja gerð hreinsunartækis og tekur fyrri eigindina úr gildi með því að fjarlægja hana úr öðrum eigindahópum.

Leit eftir eiginleikum er studd en sækir aðeins niðurstöður fyrir nákvæma samsvörun leitarorða. Til dæmis, a **Efni** eiginleiki hefur gildið **Kashmere bómull**. Ef viðskiptavinur leitar að „Reiðufé“, engar vörur sem hafa **Kashmere bómull** þar sem efnið verður sótt. Hins vegar, ef viðskiptavinur leitar að „Cashmere“, „Cotton“ eða „Cashmere Cotton,“ vörur sem hafa **Kashmere bómull** þar sem efnið verður sótt.

### <a name="additional-attribute-metadata-options"></a>Viðbótarvalkostir eigindarlýsigagna

> [!NOTE]
> Þessir eiginleikar lýsigagnavalkostir eiga aðeins við um eldri SharePoint netverslun og ytri samþættingar. Fyrir frekari upplýsingar um þessa eiginleika lýsigagnavalkosti, sjá [Yfirlit yfir leitarskema í SharePoint Server 2013](/SharePoint/search/search-schema-overview).

Eftirfarandi valkostir til viðbótar eigindarlýsigagna eru einnig fáanlegir á **Eiginleikar** síða:

- Hægt að leita
- Hægt að sækja
- Hægt að senda fyrirspurn
- Hægt að flokka
- Hunsa hástafi/lágstafi og snið
- Altæk samsvörun

Þessum valkostum var upphaflega ætlað að bæta leitarvirkni fyrir arfleifð SharePoint -undirstaða netverslunar. Þau eiga ekki endilega við um Commerce rafræn viðskipti eða POS útstöðvar. Þar sem höfuðlaus samþætting er áfram studd eru þessir valkostir tiltækir til að flytja út lýsigögn eiginda með því að nota Commerce hugbúnaðarþróunarsettið (SDK). Þú getur notað Commerce SDK til að setja vörur í sérsniðna, fínstillta ytri leitarvísitölu. Þannig geturðu tryggt að aðeins eiginleikar sem ættu að vera verðtryggðir séu verðtryggðir.

## <a name="attribute-groups"></a>Eigindaflokkar

An *eigindahópur* er notað til að flokka einstaka eiginleika íhluta eða undirhluta í vörustillingarlíkani. Eigind getur verið í fleiri en einum eigindaflokki. Eigindaflokkar geta hjálpað notendum að skilgreina afurðir vegna þess að val er raðað eftir ákveðnu samhengi. Hægt er að úthluta eigindaflokkum á söluflokka eða sölurásir. Þú getur líka stillt sjálfgefin gildi fyrir eiginleika í eigindahópi.

![Eiginleikahópar síða.](media/AttributeGroup_2022Series.png)

### <a name="create-an-attribute-group"></a>Stofna eigindahóp

Til að búa til eigindahóp skaltu fylgja skrefunum í þessu dæmi.

1. Skráðu þig inn á höfuðstöðvar Commerce sem sölustjóri.
1. Fara til **Vöruupplýsingastjórnun \> Uppsetning \> Flokkar og eiginleikar \> Eiginleikahópar**.
1. Búðu til eigindahóp sem er nefndur **Kjóllskyrtur**.
1. Bættu við eftirfarandi eiginleikum: **Hreinsunaraðferð**, **·**, **·**, og **Hönnun**.

> [!NOTE]
> Birtingarröðunargildi eiginda í eigindahópnum hafa ekki áhrif á eða eiga við um röð hreinsunaraðila í leitar- og flokkaskoðunarniðurstöðum. Þau eiga aðeins við um „pöntunareiginleika“ atburðarásina.

### <a name="assign-attribute-groups-to-categories"></a>Úthluta eigindaflokkum á söluflokka

Einn eða fleiri eigindahópar geta tengst flokkahnútum í eftirfarandi gerðum flokkastigvelda:

- Afurðarstigveldi viðskipta
- Stigveldi rásarleiðsöguflokka
- Stigveldi viðbótarvöruflokka

Þegar vörur eru flokkaðar í flokka sem eru tengdir eigindahópum erfa þær eigindirnar sem eru innifaldar í þessum eigindahópum.

![Vörueiginleikaflokkar flýtiflipann á verslun vörustigveldissíðunni.](media/AGRetailProdHierarchy_2022Series.png)

Til að úthluta eigindahópum á flokka í vörustigveldi Commerce skal fylgja skrefunum í þessu dæmiferli.

1. Skráðu þig inn á höfuðstöðvar Commerce sem sölustjóri.
1. Farðu í **Retail og Commerce \> Afurðir og tegundir \> Afurðastigveldi Commerce**.
1. Veldu **Tíska** siglingastigveldi.
1. Undir **Herrafatnaður**, veldu **Buxur** flokki, og síðan á **Vörueigindaflokkar** Flýtiflipi, bættu við eigindahópi sem er nefndur **Karlabelti**.
1. Veljið flokkinn **Tískusólgleraugu** og staðfestið nýju eigindin í eigindaflokknum **Tískusólgleraugu** með því að velja **Skoða eigindi**. Eigindaflokkurinn ætti að sýna nýju eigindin **Glerumgjörð** og **Vörumerki sólgleraugna**.
1. Veldu **Buxur** flokki og staðfestu eiginleikana fyrir **Karlabelti** eigindahópur með því að velja **Skoða eiginleika**. Eigindaflokkurinn ætti að sýna eigindin **Vörumerki herrabeltis**, **Efni beltis** og **Stærð beltis**.

Sömu grunnaðferð er einnig hægt að nota til að úthluta eigindahópum á flokka í flokkastigveldi rásaleiðsögu og viðbótarafurðaflokkastigveldi. Hins vegar, í skrefi 2, notaðu eina af eftirfarandi slóðum, allt eftir stigveldinu sem þú vilt úthluta eigindahópum til:

- **Stigveldi rásarleiðsöguflokka:** Fara til **Verslun og verslun \> Flokks- og vörustjórnun \> Rásarleiðsöguflokkar**.
- **Stigveldi viðbótarvöruflokka:** Fara til **Verslun og verslun \> Flokks- og vörustjórnun \> Viðbótarvöruflokkar**.

> [!NOTE]
> Gakktu úr skugga um að þú tengir aðeins eigindahópa í flokkastigveldi á **Vörueigindaflokkar** flýtiflipann, ekki á **Eiginleikagildi flokka** Hraðflipi. Ef eiginleikar birtast á **Eiginleikagildi flokka** Flýtiflipi, veldu **Breyta flokkastigveldi** á aðgerðasvæðinu. Síðan, á **Eiginleikahópar flokka** Flýtiflipi, veldu flokkahnúta og veldu **Fjarlægja**. Það er enginn stuðningur við að sækja eiginleika eftir flokkum í gegnum Commerce Scale Unit.

## <a name="identify-viewable-and-refinable-attributes-for-commerce-channels-for-the-default-product-collection"></a>Þekkja sýnilegar og fínstillanlegar eiginleikar fyrir viðskiptarásir fyrir sjálfgefið vörusafn

Eftir að þú hefur tengt ýmsa eiginleikahópa við flokka í ýmsum stigveldum (Vörustigveldi viðskipta eða rásaleiðsöguflokkar) og skilgreint eigindagildi fyrir hverja vöru, byggt á flokkatengingunni, verður þú að virkja **Sýna eiginleika á rás** flagga til að gera þessa eiginleika sýnilega á tiltekinni rás.

1. Farðu í **Retail og Commerce \> Uppsetning rásar \> Rásarflokkar og afurðareigindir**.
1. Veldu **Stilltu lýsigögn eiginda**, og veldu síðan eigind í vinstri yfirlitsrúðunni.
1. Á **Rásar vörueiginleikar** flýtiflipinn (ekki **Eiginleikar flokka** flýtiflipann), stilltu **Sýna eiginleika á rás** valmöguleika til **Já** til að gera eiginleikann sýnilegan.
1. Ef þú vilt að eigindin sé einnig fínstillanleg skaltu stilla **Hægt að betrumbæta** valmöguleika til **Já**.

### <a name="control-visibility-of-dimension-based-refiners-such-as-size-style-and-color"></a>Stjórna sýnileika víddarbundinna hreinsunartækja eins og stærð, stíl og lit

Vörumál eins og stærð, stíll og litur eru algengustu hreinsunarefnin. Til að gera þessar afurðavíddir aðgengilegar sem hreinsunartæki, ættir þú að tengja eigindahóp á rásarstigi sem inniheldur tilvísun í eigindategund sem erfir sjálfkrafa gildi frá afurðavíddargildum.

Þú getur tilgreint að vöruvíddir séu sýnilegar og hægt að betrumbæta með því að uppfæra fána á **Rásarflokkar og vörueiginleikar** síðu. Veldu rótarhnútinn í yfirlitsrúðunni og síðan á **Rásar vörueiginleikar** flýtiflipann, stilltu **Sýna eiginleika á rás** valmöguleika til **Já** fyrir **Stærð**, **·**, og **Litur** eiginleikar. Ef þú vilt að þessir eiginleikar séu betrumbættir líka skaltu stilla **Hægt að betrumbæta** valmöguleika til **Já** fyrir hvert.

![Stilling eigindalýsigagna fyrir víddarhreinsanir.](./media/ProductDimensionRefinersMetadataSetup_2022Series.png)

Til að virkja eigindirnar þannig að þær séu tiltækar í Houston-rásinni sem byggir á kynningargögnum skaltu fylgja skrefunum í þessu dæmiferli.

1. Farðu í **Retail og Commerce \> Uppsetning rásar \> Rásarflokkar og afurðareigindir**.
1. Veljið **Houston** rásina.
1. Í aðgerðarúðunni skal velja **Stilla eigind lýsigagna**.
1. Veljið tegundahnútinn **Tíska** og síðan í flýtiflipanum **Afurðareigindir rásar** skal velja **Taka með eigind** fyrir hverja eigind.
1. Veljið tegundahnútinn **Tískufylgihlutir**, veljið flokkinn **Tískasólgleraugu** og síðan á flýtiflipanum **Afurðareigindir rásar** skal velja **Taka með eigind** fyrir hverja eigind.
1. Veljið tegundahnútinn **Herraklæðnaður**, veljið flokkinn **Buxur** og síðan á flýtiflipanum **Afurðareigindir rásar** skal velja **Taka með eigind** fyrir hverja eigind.
1. Eftir að þú hefur uppfært lýsigögn eiginda fyrir fyrirhugaða eiginleika og hreinsunartæki skaltu ganga úr skugga um að þú vistir breytingarnar og keyrir **Birtu rásaruppfærslur** starf. Síðan, eftir að uppfærslurnar hafa verið birtar, verður þú að keyra eftirfarandi störf: **1070** (**Rásar stillingar**), **·** (**Vörur**), og **1150** (**Vörulisti**).

> [!NOTE]
> - Ef fyrirtækið þitt krefst þess að þú bætir oft við eða fjarlægir vörur í leiðsagnarstigveldinu, eða að þú gerir breytingar eins og að uppfæra birtingarpöntunargildi, bæta við nýjum flokkum og bæta nýjum eigindahópum við flokka, mælum við með að þú stillir **Birtu rásaruppfærslur** starf til að keyra sem tíð lotuvinna. Að öðrum kosti skaltu kveikja handvirkt á **Birtu rásaruppfærslur** starf, og svo eftirfarandi Commerce Data Exchange (CDX) störf: **1070** (**Rásar stillingar**), **·** (**Vörur**), og **1150** (**Vörulisti**).
> - An **Erfa** valmöguleikinn gerir þér kleift að tilgreina að rás ætti að erfa eigindahópana frá móðurrásinni í stigveldinu. Ef valkosturinn **Erfa** er stilltur á **Já** erfir undirhnútarásin alla eigindaflokkana og öll eigindin í þessum eigindaflokkum.
> - Ef **Stilltu lýsigögn eiginda** hnappur á aðgerðarrúðunni er ekki tiltækur, vertu viss um að **Leiðsögustigveldi** er tengt rásinni þinni á **Almennt** Hraðflipi.
> - Þú mátt ekki tengja neina eiginleikahópa nema víddarbyggða eigindahópa á rásarstigi (td undir **Eiginleikahópar** á **Rásarflokkar og vörueiginleikar** síðu).
> - Eftir kynningu á stuðningi fyrir viðskiptavina-til-fyrirtæki vörulista (B2B) í viðskiptaútgáfu 10.0.27, er ætlast til að þú auðkennir hreinsunar- og eigindauppsetningar fyrir hvern B2B vörulista á sama hátt og lýst er í þessari grein.

## <a name="override-attribute-values"></a>Hneka eigindagildum

Sjálfgildi eiginda er hægt er að hnekkja á afurðastigi fyrir einstakar afurðir. Einnig er hægt að hnekkja þeim fyrir einstakar vörur í tilteknum vörulistum sem miða á tilteknar rásir.

### <a name="override-the-attribute-values-of-an-individual-product"></a>Hnekkja eigindagildum fyrir einstaka afurð

Til að hnekkja eigindargildum einstakrar vöru skaltu fylgja skrefunum í þessu dæmiferli.

1. Skráðu þig inn á höfuðstöðvar Commerce sem sölustjóri.
1. Fara til **Verslun og verslun \> Flokks- og vörustjórnun \> Útgefnar vörur eftir flokkum**.
1. Veldu **Tíska \> Tíska aukabúnaður \> Tíska sólgleraugu**.
1. Veljið nauðsynlega afurð í hnitanetinu. Í aðgerðarúðunni á flipanum **Afurð** í flokknum **Uppsetning** skal velja **Afurðareigindir**.
1. Velja skal eigind á svæðinu til vinstri og síðan uppfæra gildi þess á svæðinu til hægri.

![Vörueiginleikagildi síða.](media/ProdDetailsProdAttrValues_2022Series.png)

### <a name="override-the-attribute-values-of-all-products-in-a-catalog"></a>Hneka eiginleikagildi allra vara í vörulista

Til að hnekkja eigindargildum allra vara í vörulista skal fylgja skrefunum í þessu dæmiferli.

1. Skráðu þig inn á höfuðstöðvar Commerce sem sölustjóri.
1. Fara til **Verslun og verslun \> Vörulistastjórnun \> Allir vörulistar**.
1. Veljið vörulistann **Grunnvörulisti Fabrikam**.
1. Veldu **Tíska \> Tíska aukabúnaður \> Tíska sólgleraugu**.
1. Á flýtiflipanum **Afurðir** skal velja nauðsynlega afurð og velja síðan **Eigindir** fyrir ofan afurðarhnit.
1. Á eftirfarandi flýtiflipa skal upfæra gildin á nauðsynlegum eigindum:

    - Sameiginlegir afurðamiðlar
    - Eigindi samnýttrar afurðar
    - Miðlar rásar
    - Afurðareigindir rásar

### <a name="override-the-attribute-values-of-all-products-in-a-channel"></a>Hneka eiginleikagildi allra vara á rás

Til að hnekkja eigindargildum allra vara í rás skaltu fylgja skrefunum í þessu dæmiferli.

1. Skráðu þig inn á höfuðstöðvar Commerce sem sölustjóri.
1. Farðu í **Retail og Commerce \> Uppsetning rásar \> Rásarflokkar og afurðareigindir**.
1. Veljið **Houston** rásina.
1. Á flýtiflipanum **Afurðir** skal velja nauðsynlega afurð og velja síðan **Eigindir** fyrir ofan afurðarhnit.
1. Ef engar vörur eru fáanlegar skaltu velja **Bæta við** á **Vörur** flýtiflipanum og veldu síðan nauðsynlegar vörur í **Bæta við vörum** valmynd.
1. Á eftirfarandi flýtiflipa skal upfæra gildin á nauðsynlegum eigindum:

    - Sameiginlegir afurðamiðlar
    - Eigindi samnýttrar afurðar
    - Miðlar rásar
    - Afurðareigindir rásar

### <a name="define-variant-specific-attribute-values-and-define-multiple-values-for-product-attributes"></a>Skilgreindu afbrigðissértæk eigindagildi og skilgreindu mörg gildi fyrir vörueiginleika

Til að skilgreina afbrigðissértæk eigindagildi og til að skilgreina mörg gildi fyrir vörueiginleika, fylgdu skrefunum í þessu dæmiferli.

1. Skráðu þig inn á höfuðstöðvar Commerce sem sölustjóri.
1. Farðu í **Retail og Commerce \> Uppsetning rásar \> Rásarflokkar og afurðareigindir**.
1. Veljið **Houston** rásina.
1. Á **Vörur** Flýtiflipi, veldu nauðsynlega vöruafbrigði og veldu síðan **Eiginleikar** fyrir ofan vörunetið.
1. Ef engar vörur eru fáanlegar skaltu velja **Bæta við** á **Vörur** flýtiflipann og veldu síðan nauðsynleg vöruafbrigði í **Bæta við vörum** valmynd.
1. Á eftirfarandi flýtiflipa skal upfæra gildin á nauðsynlegum eigindum:

    - Sameiginlegir afurðamiðlar
    - Eigindi samnýttrar afurðar
    - Miðlar rásar
    - Afurðareigindir rásar

#### <a name="example-of-variant-specific-attribute-configuration"></a>Dæmi um afbrigðissértæka eiginleikauppsetningu
        
Í þessu dæmi er **P001-Meistari** vara er fjölvirkur skór sem hefur þrjú afbrigði: **Hlaupandi**, **·**, og **Gönguferðir**. Fyrir hvert afbrigði viltu skilgreina gildið á einstakan hátt **Virkni** eiginleiki. Á **Vörur** Flýtiflipi á **Rásarflokkar og vörueiginleikar** síðu fyrir rásina þína, þú skilgreinir **Virkni** eigindargildi fyrir afbrigðin eins og sýnt er í eftirfarandi töflu.

| Vöruvíddasamsetning     | Virkni eigindargildi |
|-------------|--------------------------|
| P001-Meistari | Íþróttir                   |
| P001-1      | Í gangi                  |
| P001-2      | Ganga                  |
| P001-3      | Gönguferðir                 |

Ef notandi leitar að „skó“, er **P001-Meistari** vara mun birtast í leitarniðurstöðum. Ef þú stilltir **Virkni** eigind sem hreinsanleg, the **Virkni** hreinsunaraðili mun aðeins skrá **Íþróttir** sem hreinsanlegt gildi, vegna þess að það gildi var skilgreint fyrir **Virkni** eiginleiki á **P001-Meistari** vörustig.

Sjálfgefið er að eiginleikar á afbrigðisstigi séu eingöngu ætlaðir til notkunar á vöruupplýsingasíðum (PDP). Þegar þú velur tiltekið vöruafbrigði á PDP eru vörulýsingarnar á PDP uppfærðar fyrir það tiltekna afbrigði.

Til að hreinsunaraðilar geti tekið upp eiginleikagildi sem eru skilgreind á vöruafbrigðisstigi, verður þú að skilgreina eigind á aðalstigi vöru, veldu **Leyfa mörg gildi** gátreitinn og stilltu eigindargerðina á **Texti**.

Næst verður þú að ákvarða öll möguleg gildi fyrir vöruafbrigði þín. Fyrir **Virkni** eigind sem er notuð í þessu dæmi, hugsanleg gildi gætu innihaldið **Hlaupandi**, **·**, **·**, **·**, **·**, **íþróttir**, og **Snjóíþróttir**.

Eftir að þú hefur ákvarðað hver afbrigðiseiginleikagildin ættu að vera, geturðu skilgreint þau á aðalstigi vöru með því að nota pípuaðskilin gildi. Fyrir **Virkni** eigind, gætirðu skilgreint eigindargildið á vörustjóranum sem **Hlaup|Göngur|Göngur|Gangur|Tjaldsvæði|Vatnaíþróttir|Snjóíþróttir**.

Síðan, fyrir hvert afbrigði, er hægt að skilgreina eigindagildi með því að slá inn annað hvort pípuaðskilin gildi eða stök gildi. Fyrir **Virkni** eigind, gætirðu stillt einstakt vöruafbrigði sem **Hlaup|Göngur|Göngur**, **·**, **|Göngur|Vatnaíþróttir**, og svo framvegis.

Eftir að þú hefur skilgreint gildi afbrigðaeiginleika, á **Rásarflokkar og vörueiginleikar** síðu, á aðgerðarrúðunni, veldu **Birtu rásaruppfærslur**, og keyrðu síðan **1150**, **·**, og **1070** störf.

Eftir að verkum er lokið og leitarvísitalan er uppfærð ættu öll væntanleg gildi að birtast í leitarniðurstöðum og flokkaskoðunarniðurstöðum.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
