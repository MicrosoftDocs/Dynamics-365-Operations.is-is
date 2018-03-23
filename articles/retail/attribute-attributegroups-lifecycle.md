---
title: "Eigindir, eigindaflokkar og tengingar þeirra við ýmsar Retail einingar í Finance and Operations"
author: ashishmsft
manager: AnnBe
ms.date: 03/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2018-03-30
ms.dyn365.ops.version: Application pdate 5, AX 8.0
ms.translationtype: HT
ms.sourcegitcommit: 25fa39dc81fc721d7593a25a102ce47041ebc5f0
ms.openlocfilehash: 6fde46c35d5efbb72ad97628d7d5a3f9eeba7c8e
ms.contentlocale: is-is
ms.lasthandoff: 03/13/2018

---

# <a name="attributes-attribute-groups-and-their-associations-with-various-retail-entities-in-finance-and-operations"></a>Eigindir, eigindaflokkar og tengingar þeirra við ýmsar Retail einingar í Finance and Operations

[!include[banner](includes/banner.md)]

*Eigindir* veita leið til að lýsa afurð og eiginleikum hennar enn frekar í gegnum notandaskilgreind svæði (eins og **Minnisstærð**, **Afkastagetu harða disksins**, **Uppfyllir kröfur Energy star** og svo framvegis). Í Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition geta eigindir tengst ýmsum Retail einingum, eins og afurðarflokkum og smásölurásum, og hægt er að stilla sjálfgildi fyrir þær. Afurðir erfa síðan eigindin og sjálfgildin þegar þau tengjast afurðarflokkum eða smásölurásum. Hægt er að hnekkja sjálfgildunum á stigi einstakra afurðar, stigi smásölurásar eða í vörulista smásölu.
 
Til dæmis gæti dæmigerð sjónvarpsafurð haft eftirfarandi eiginleika.

| Tegund   | Eigind                | Möguleg gildi eru:          | Sjálfgildi |
|------------|--------------------------|-----------------------------|---------------|
| Sjónvarp og myndbönd | Vörumerki                    | Öll gild gildi vörumerkja       | None          |
| Sjónvarp         | Stærð skjás              | 20–80 tommur                | None          |
|            | Lóðrétt upplaus      | 480i, 720p, 1080i eða 1080p | 1080p         |
|            | Endurnýjunarhraða skjánum      | 60hz, 120hz eða 240hz       | 60hz          |
|            | HDMI inntök              | 0–10                        | 3             |
|            | DVI inntök               | 0–10                        | 1             |
|            | Samsettur inntök         | 0–10                        | 2             |
|            | Inntök íhluta         | 0–10                        | 1             |
| LCD        | 3D Ready                 | Já eða Nei                   | Já           |
|            | 3D virkjað               | Já eða Nei                   | Númer            |
| Plasma     | Rekstrarhitastig frá      | 32–110 gráður              | 32            |
|            | Rekstrarhitastig til        | 32–110 gráður              | 100           |
| Projection | Ábyrgð á túbuskjá | 6, 12 eða 18 mánuðir         | 12            |
|            | # túbuskjáa    | 1–5                         | 3             |

## <a name="attributes-and-attribute-types"></a>Eigindir og gerðir eiginda

Eigindir eru byggðar á *gerðum eiginda*. gerð eigindar auðkennir gagnategundina sem hægt er að slá inn fyrir tiltekna eigind. Finance and Operations styður eftirfarandi gerðir eiginda:

- **Gjaldmiðill** – Þessi gerð styður gildi gjaldmiðils. Hægt er að afmarka hana (þ.e. hún getur studd svið gilda) eða skilja eftir opna.
- **DateTime** – Þessi gerð styður gildi dagsetningar og tíma. Hægt er að afmarka hana eða skilja eftir opna.
- **Tugastafir** – Þessi gerð styður númeragildi með tugasætum. Hún styður einnig mælieiningu. Hægt er að afmarka hana eða skilja eftir opna.
- **Heiltala** – Þessi gerð styður númeragildi. Hún styður einnig mælieiningu. Hægt er að afmarka hana eða skilja eftir opna.
- **Texti** – Þessi gerð styður textagildi. Hún styður einnig fyrirfram skilgreint sett af mögulegum gildum (þ.e. *tölusetningu*).
- **Boole-gildi** – Þessi gerð styður tvíundargildi (**satt** eða **rangt**).
- **Tilvísun** - Þessi gerð vísar í aðrar eigindir.

### <a name="set-up-attribute-types-in-finance-and-operations"></a>Setja upp gerðir eiginda í Finance and Operations

1. Innskráning í biðlara bakvinnslu í Finance and Operations sem vörustjóri smásölu.
2. Farið í **Afurðaupplýsingastjórnun** &gt; **Uppsetning** &gt; **Tegundir og eigindir** &gt; **Gerðir eiginda**.
3. Stofnið tvær gerðir eiginda af gerðinni **Texti**, stillið valkostinn **Fastur listi** á **Já** og bætið síðan við lista af gildum:

    - Skírið eina gerð eigindar **Umgjörð** og bætið við eftirfarandi gildum: **Sporaskja**, **Ferningur** og **Rétthyrningur**.
    - Skírið hina gerð eigindar **Vörumerki sólgleraugna** og bætið við eftirfarandi gildum: **Ray ban**, **Aviator** **Oakley**.

![Gerðir eiginda](media/AttributeType.png)

### <a name="set-up-an-attribute-in-finance-and-operations"></a>Uppsetning á eigind í Finance and Operations

1. Innskráning í biðlara bakvinnslu sem vörustjóri smásölu.
2. Farið í **Afurðaupplýsingastjórnun** &gt; **Uppsetning** &gt; **Tegundir og eigindir** &gt; **Eigindir**.
3. Stofnið eigind með heitinu **Gler**.
4. Stillið svæðið **Gerð eigindar** á **Umgjörð**.

![Eigindir](media/Attribute.png)

## <a name="attribute-metadata"></a>Lýsigögn eiginda

*Lýsigögn eiginda* leyfir þér að velja valkosti til að tilgreina hvernig eigindin fyrir hverja vöru eigi að haga sér. Til dæmis er hægt að velja hvort eiginda sé krafist, hvort hægt sé að nota þær við leit og hvort hægt sé að nota þær sem síu.

Fyrir smásöluafurðir er hægt að hnekkja á lýsigögnum eiginda á stigi rásar. Fjallað verður um þennan möguleika síðar í þessu efnissatriði.

Eins og þú kannski tekur eftir inniheldur síðan **Eigindir** valkosti sem tengjast lýsigögnum eiginda. Undir **Lýsigögn eiginda fyrir sölustaði** hefur einn valkostur sem heitir **„Hægt að fínstilla“** áhrif á virkni eigindagilda á smásölustað (POS) eða hvernig kerfið meðhöndlar þessi eigindargildi. Aðeins eigindir þar sem hægt er að stilla valkostinn **„Hægt að fínstilla“** á **„Já“** munu birtast fyrir fínstillingu eða síun á vörum í smásölustað.

Hér eru eftirstandandi valkostir fyrir lýsigögn eiginda á síðunni **Eigindir**:

- Hægt að leita
- Hægt að sækja
- Hægt að senda fyrirspurn
- Hægt að flokka
- Leyfa mörg gildi
- Hunsa hástafi/lágstafi og snið
- Altæk samsvörun

Þessum valkostum var upphaflega ætlað að bæta leitarvirknina fyrir netverslunina. Þó að Finance and Operations feli ekki í sér netverslun beint úr kassanum, þá felur það í sér eCommerce Publishing Software Development Kit (SDK). Viðskiptavinir geta notað SDK til að setja afurðir inn í leitaratriðaskrá að eigin vali. Þótt afurðargögnin séu flutt inn ætti viðskiptavinurinn samt að geta greint leitanleg gögn, gögn sem hægt er að spyrjast fyrir um og svo framvegis. Þannig geta þeir byggt upp sem hagkvæmasta atriðaskrá til að tryggja að þeir vísi aðeins í eigindir sem *að þeirra mati* ættu að vera atriðaskráðar.

Til að fá upplýsingar um tilgang hinna valkostanna, sjá [Yfirlit yfir leitarskema í SharePoint Server 2013](https://technet.microsoft.com/en-us/library/jj219669.aspx).

## <a name="filter-settings-for-attributes"></a>Síustillingar fyrir eigindir

Síustillingar fyrir eigindir leyfir þér að skilgreina hvernig síurnar fyrir eigindin birtast á smásölustað. Til að fá aðgang að síustillingu eigindar skal á síðunni **Eigindir** í Finance and Operations velja eigindina og síðan í aðgerðarúðunni velja **Síustillingar**.

Síðan **Kjörstillingar á síubirtingu** inniheldur eftirfarandi svæði:

- **Heiti** – Að sjálfgefnu er svæðið stillt á heiti eigindar. Þó er hægt að breyta gildinu.
- **Birtingarkostir** – Eftirtaldir valkostir eru í boði:

    - **Stakt gildi** – Þessi valkostur er tiltækur fyrir eftirfarandi gerðir eiginda: **Boole-gildi**, **Gjaldmiðil**, **Tugastaf**, **Heiltölu** og **Texta**. Þessi valkostur gerir kleift að velja stakt gildi fyrir þessar eigindir í biðlara fyrir fínstillingar.
    - **Mörg gildi** – Þessi valkostur er tiltækur fyrir eftirfarandi gerðir eiginda: **Gjaldmiðil**, **Tugastaf**, **Heiltölu** og **Texta**. Þessi valkostur gerir kleift að velja mörg gildi fyrir þessa eigind í biðlari fyrir fínstillingar.

- **Birtingarstjórnun** – Eftirtaldir valkostir eru í boði:

    - **Listi** – Þessi valkostur er tiltækur fyrir allar gerðir eiginda.
    - **Svið** – Þessi valkostur er tiltækur fyrir eftirfarandi gerðir eiginda: **Gjaldmiðil**, **Tugastaf** og **Heiltölu**. 
    - **Sleði** – Þessi valkostur er tiltækur fyrir eftirfarandi gerðir eiginda: **Gjaldmiðil**, **Tugastaf** og **Heiltölu**.
    - **Sleði með stiku** – Þessi valkostur er tiltækur fyrir eftirfarandi gerðir eiginda: **Gjaldmiðil**, **Tugastaf** og **Heiltölu**.

- **Viðmiðunargildi** – Þessi stilling er nauðsynleg ef valið var **Svið** sem gerð birtingarstjórnunar. Hægt er að skilgreina gildi með því að nota semíkommu (;) sem afmarkara.

    Til dæmis, fyrir síu eins og **Rúmmál poka**, getur viðmiðunargildi verið **10; 20; 50; 100; 200; 500; 1000; 5000**. Í þessu tilviki sýnir smásölustaðurinn eftirfarandi afmarkanir. Allar afmarkanir sem hafa engar afurðir í niðurstöðusafninu birtast í deyfðu.

    - Færri en 10
    - 10 – 20
    - 20 – 50
    - 50 – 100
    - 100 – 200
    - 200 – 500
    - 500 eða fleiri

![Síustillingar eigindar](media/AttributeFilterSettings.PNG)

## <a name="attribute-groups"></a>Eigindaflokkar

Eftir að eigindir hafa verið skilgreindar er hægt að úthluta þeim í eigindaflokka. *Eigindaflokkur* er notaður til að flokka einstakar eigindir fyrir hlut eða undirhlut í afbrigðalíkani afurðar. Eigind getur verið í fleiri en einum eigindaflokki. Eigindaflokkar geta hjálpað notendum að skilgreina afurðir vegna þess að val er raðað eftir ákveðnu samhengi. Hægt er að úthluta eigindaflokkum á smásöluflokka eða smásölurásir.

Þú getur einnig stillt sjálfgildi fyrir eigindir sem eru í eigindaflokk. Til dæmis er bætt við eigind fyrir lit í eigindaflokki og **Blár** er valinn sem sjálfgildi eigindar. Í þessu tilviki, þegar eigindaflokknum er bætt við smásöluafurð sem inniheldur lit sem eina af eigindum sínum, birtist **Blár** sem sjálfgefinn litur fyrir þá afurð.

![Eigindaflokkar](media/AttributeGroup.png)

### <a name="create-an-attribute-group"></a>Stofna eigindahóp

1. Innskráning í biðlara bakvinnslu sem vörustjóri smásölu.
2. Fara í **Afurðaupplýsingastjórnun** &gt; **Uppsetning** &gt; **Flokkar og eigindir** &gt; **Eigindaflokkar**.
3. Stofna eigindahóp með heitinu **Tískusólgleraugu**.
4. Bæta við eftirfarandi eigindum: **Umgjörð** og **Vörumerki sólgleraugna**.

### <a name="assign-attribute-groups-to-retail-categories"></a>Úthluta eigindaflokkum á smásöluflokka

Einn eða fleiri eigindaflokkar geta tengst tegundahnútum í eftirfarandi gerðum af flokkastigveldi smásöluafurða: Stigveldi Retail afurða, stigveldi fyrir skoðunarflokk rásar og tegundastigveldi viðbótarafurðar. Þegar afurðir hafa verið flokkaðar, erfa þær eigindir sem eru innifaldar í eigindaflokkunum.

![Stigveldi Retail afurðar – Eigindaflokkar afurðar](media/AGRetailProdHierarchy.PNG)

Fylgdu þessum leiðbeiningum til að úthluta eigindahópum í flokka í stigveldi Retail afurðar.

1. Innskráning í biðlara bakvinnslu sem vörustjóri smásölu.
2. Farið í **Retail** &gt; **Flokka- og afurðastjórnun** &gt; **Stigveldi Retail afurðar**.
3. Veljið **Yfirlitsstigveldi tísku**.
4. Undir **Herraklæðnaður** skal velja flokkinn **Buxur** og síðan í flýtiflipanum **Eigindaflokkar afurðar** skal bæta við eigindaflokki sem fær heitið **Herrabelti**.
5. Veljið flokkinn **Tískusólgleraugu** og staðfestið nýju eigindin í eigindaflokknum **Tískusólgleraugu** með því að velja **Skoða eigindi**.

    Eigindaflokkurinn ætti að sýna nýju eigindin **Glerumgjörð** og **Vörumerki sólgleraugna**.

6. Undir **Herraklæðnaði** skal velja flokkinn **Buxur** staðfesta eigindin fyrir eigindaflokkinn **Herrabelti** með því að velja **Skoða eigindi**.

    Eigindaflokkurinn ætti að sýna eigindin **Vörumerki herrabeltis**, **Efni beltis** og **Stærð beltis**.

> [!NOTE]
> Einnig er hægt að nota þetta ferli til að úthluta eigindahópum í flokka í stigveldi fyrir skoðunarflokk rásar og tegundastigveldi viðbótarafurðar. Í skrefi 2 skal nota eftirfarandi leiðsögn:
>
> - **Retail** &gt; **Flokka- og afurðastjórnun** &gt; **Skoðunarflokkar rásar**
> - **Retail** &gt; **Flokka- og afurðastjórnun** &gt; **Viðbótarafurðarflokkar**

### <a name="assign-attribute-groups-to-retail-stores"></a>Úthluta eigindaflokkum á smásöluverslanir

Einn eða fleiri eigindaflokkar geta tengst einni eða fleiri smásöluverslunum í stigveldi smásöluverslunar. Þegar afurðir hafa verið flokkaðar fyrir tilteknar smásöluverslanir, erfa þær eigindir sem eru innifaldar í eigindaflokkunum.

1. Innskráning í biðlara bakvinnslu sem vörustjóri smásölu.
2. Farið í **Retail** &gt; **Uppsetning rásar** &gt; **Tegundir rása og afurðareigindi**.
3. Úthluta eigindaflokkum á Houston rásina:

    1. Veljið **Houston** rásina.
    2. Í flýtiflipa **Eigindaflokks** skal velja **Bæta við** og síðan í reitnum **Heiti** skal velja **SharePointProvisionedProductAttributeGroup**.
    3. Aftur skal velja **Bæta við** og síðan í reitnum **Heiti** skal velja **Herrabelti**.
    4. Aftur skal velja **Bæta við** og síðan í reitnum **Heiti** skal velja **Tískusólgleraugu**.

        > [!NOTE]
        > Valkostur gerir þér kleift að tilgreina að þessi rás ætti að erfa eigindaflokkana frá yfirrásinni í stigveldinu. Ef valkosturinn **Erfa** er stilltur á **Já** erfir undirhnútarásin alla eigindaflokkana og öll eigindin í þessum eigindaflokkum.

4. Virkja eigindin svo þau séu tiltæk á Houston rásinni:

    1. Í aðgerðarúðunni skal velja **Stilla eigind lýsigagna**.
    2. Veljið tegundahnútinn **Tíska** og síðan í flýtiflipanum **Afurðareigindir rásar** skal velja **Taka með eigind** fyrir hverja eigind.
    3. Veljið tegundahnútinn **Tískufylgihlutir**, veljið flokkinn **Tískasólgleraugu** og síðan á flýtiflipanum **Afurðareigindir rásar** skal velja **Taka með eigind** fyrir hverja eigind.
    4. Veljið tegundahnútinn **Herraklæðnaður**, veljið flokkinn **Buxur** og síðan á flýtiflipanum **Afurðareigindir rásar** skal velja **Taka með eigind** fyrir hverja eigind.

![Tegundir rása og afurðareigindir – Eigindaflokkar](media/CCPAttrGrp.png)

## <a name="overriding-attribute-values"></a>Hnekkja eigindagildum

Sjálfgildi eiginda er hægt er að hnekkja á afurðastigi fyrir einstakar afurðir. Einnig er hægt að hnekkja sjálfgildum fyrir einstaka vörur í tilteknum vörulistum sem eru ætlaðir fyrir tilteknar smásölurásir.

### <a name="override-the-attribute-values-of-an-individual-product"></a>Hnekkja eigindagildum fyrir einstaka afurð

1. Innskráning í biðlara bakvinnslu sem vörustjóri smásölu.
2. Farið í **Retail** &gt; **Flokka- og afurðastjórnun** &gt; **Útgefnar afurðir eftir flokki**.
3. Veljið tegundahnútinn **Tíska** &gt; **Tískufylgihlutir** &gt; **Tískusólgleraugu**.
4. Veljið nauðsynlega afurð í hnitanetinu. Í aðgerðarúðunni á flipanum **Afurð** í flokknum **Uppsetning** skal velja **Afurðareigindir**.
5. Velja skal eigind á svæðinu til vinstri og síðan uppfæra gildi þess á svæðinu til hægri.

![Upplýsingasíða afurðar – flokkar afurðareigindar](media/ProdDetailsProdAttrValues.png)

### <a name="override-the-attribute-values-of-products-in-a-catalog"></a>Hnekkja skal eigindagildum afurða í vörulista

1. Innskráning í biðlara bakvinnslu sem vörustjóri smásölu.
2. Farið í **Retail** &gt; **Vörulistastjórnun** &gt; **Allir vörulistar**.
3. Veljið vörulistann **Grunnvörulisti Fabrikam**.
4. Veljið tegundahnútinn **Tíska** &gt; **Tískufylgihlutir** &gt; **Tískusólgleraugu**.
5. Á flýtiflipanum **Afurðir** skal velja nauðsynlega afurð og velja síðan **Eigindir** fyrir ofan afurðarhnit.
6. Á eftirfarandi flýtiflipa skal upfæra gildin á nauðsynlegum eigindum:

    - Sameiginlegir afurðamiðlar
    - Eigindi samnýttrar afurðar
    - Miðlar rásar
    - Afurðareigindir rásar

    > [!NOTE]
    > Ef samnýttir afurðamiðlar og samnýttar afurðareigindir eru stofnaðar í Finance and Operations eiga þær við um allar smásöluafurðir.

![Vörulisti yfir eigindaflokka afurðar](media/CatalogProdAttrValues.png)

### <a name="override-the-attribute-values-of-products-in-a-channel"></a>Hnekkja skal eigindagildum afurða í rás

1. Innskráning í biðlara bakvinnslu sem vörustjóri smásölu.
2. Farið í **Retail** &gt; **Uppsetning rásar** &gt; **Tegundir rása og afurðareigindi**.
3. Veljið **Houston** rásina.
4. Á flýtiflipanum **Afurðir** skal velja nauðsynlega afurð og velja síðan **Eigindir** fyrir ofan afurðarhnit.

    > [!NOTE]
    > Ef engar vörur eru tiltækar skal bæta við afurðum með því að velja **Bæta við** á flýtiflipanum **Afurðir** og velja síðan nauðsynlegar afurðir í svarglugganum **Bæta við afurðum**.

5. Á eftirfarandi flýtiflipa skal upfæra gildin á nauðsynlegum eigindum:

    - Sameiginlegir afurðamiðlar
    - Eigindi samnýttrar afurðar
    - Miðlar rásar
    - Afurðareigindir rásar

    > [!NOTE]
    > Ef samnýttir afurðamiðlar og samnýttar afurðareigindir eru stofnaðar í Finance and Operations eiga þær við um allar smásöluafurðir.
