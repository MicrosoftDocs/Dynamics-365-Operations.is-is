---
title: "Grunnstilla gagnainnflutning úr SharePoint"
description: "Þetta efnisatriði útskýrir hvernig á að flytja inn gögn frá Microsoft SharePoint."
author: NickSelin
manager: AnnBe
ms.date: 05/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.translationtype: HT
ms.sourcegitcommit: 2fc887668171175d436b9eb281a35c1c9d089591
ms.openlocfilehash: 4285db9c71208bce45d64933e692a25ef3f46b26
ms.contentlocale: is-is
ms.lasthandoff: 08/09/2018

---
# <a name="configure-data-import-from-sharepoint"></a>Grunnstilla gagnainnflutning úr SharePoint

[!include[banner](../includes/banner.md)]

Til að flytja inn gögn úr skrá á innleið með því að nota rafræna skýrslugerð (ER) ramma, þarftu að grunnstilla ER snið sem styður innflutninginn og síðan keyra vörpun líkans af **Til áfangastaðar** gerðinni sem notar þetta snið sem gagnagjafa. Til að flytja inn gögn verður þú að fara í skrána sem þú vilt flytja inn. Skráin sem er á innleið er hægt að velja handvirkt af notanda. Með nýju ER eiginleikanum til að styðja við innflutning gagna frá Microsoft SharePoint, getur þetta ferli verið grunnstillt sem óvaktað. Þú getur notað ER stillingar til að framkvæma gagnainnflutning frá skrám sem eru geymd í Microsoft SharePoint möppum. Þetta efnisatriði útskýrir hvernig á að ljúka innflutningi frá SharePoint til Microsoft Dynamics 365 for Finance and Operations. Dæmin nota lánardrottnafærslur sem viðskiptagögn.

## <a name="prerequisites"></a>Frumskilyrði
Til að ljúka dæmunum í þessu efnisatriði þarftu að hafa eftirfarandi aðgang:

- Aðgangur að Finance and Operations fyrir eitt af eftirtöldum hlutverkum:

    - Þróunaraðili rafrænnar skýrslulausnar
    - Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar
    - Kerfisstjóri

- Aðgangur að tilviki Microsoft SharePoint þjóns sem er grunnstillt til notkunar með Finance and Operations
- ER snið og grunnstillingar líkans fyrir 1099 greiðslur

### <a name="create-required-er-configurations"></a>Búðu til nauðsynlegar ER grunnstillingar
Spila **ER flytja inn gögn úr Microsoft Excel skrá** verkefnaleiðbeiningar, sem eru hluti af **7.5.4.3 Fá/Þróa upplýsingatækniþjónustu/lausn íhlutir (10677)** viðskiptaferli. Þessi verkefnaleiðbeiningar fylgja þér í gegnum ferlið við að hanna og nota ER grunnstillingar til að flytja inn lánardrottnafærslur á gagnvirkan máta frá ytri Microsoft Excel skrám. Nánari upplýsingar er að finna í [Þátta skjöl á innleið í Microsoft Excel](parse-incoming-documents-excel.md). Að lokum, munt þú hafa:

- ER grunnstillingar:

    - ER grunnstillingar líkans, **1099 Greiðslulíkan**
    - ER grunnstillingar sniðs, **Snið til að flytja inn lánardrottnafærslur frá Excel**

[![ER grunnstillingar til að flytja inn gögn frá SharePoint](./media/GERImportFromSharePoint-01-Configurations.PNG)](./media/GERImportFromSharePoint-01-Configurations.PNG)

- Sýnishorn af skrá á innleið fyrir gagnainnflutning:

    - Excel skrá **1099import-data.xlsx**, með lánardrottnafærslu sem ætti að vera flutt inn í Finance and Operations

[![Sýnishorn af Microsoft Excel skrá til innflutnings frá SharePoint](./media/GERImportFromSharePoint-02-Excel.PNG)](./media/GERImportFromSharePoint-02-Excel.PNG)

> [!NOTE]
> Sniðið til að flytja inn lánardrottnafærslur er valið sem sjálfgefin vörpun líkans. Þess vegna, ef þú keyrir vörpun líkans **1099 Greiðslulíkan**, og þessi vörpun líkans er af **Til áfangastaðar** gerðinni, keyrir vörpun líkans þetta snið til að flytja inn gögn úr ytri skrám. Það notar síðan þessi gögn til að uppfæra töflur í forriti.

## <a name="configure-document-management-parameters"></a>Grunnstilla færibreytur skjalastjórnunar
1. Á **Færibreytur skjalastjórnunar** síðunni, skal grunnstilla aðgangur að tilviki SharePoint þjóns sem verður notuð af fyrirtækinu sem þú ert skráður inn á í augnablikinu. Í þessu dæmi er fyrirtækið USMF.
2. Prófa tengingu við tilvik SharePoint þjóns til að tryggja að þú hafi verið veittur aðgangur.

[![Skjalastjórnunarstilling - SharePoint þjónn](./media/GERImportFromSharePoint-03-SharePointSetup.png)](./media/GERImportFromSharePoint-03-SharePointSetup.png)

3. Opna grunnstillta SharePoint svæðið og búa til eftirfarandi möppur þar sem hægt er að geyma skrárnar sem eru á innleið:

    - Innflutningsuppruni skráa (aðal)
    - Innflutningsuppruni skráa (annað)

[![Skjalastjórnunarstilling - SharePoint þjónn](./media/GERImportFromSharePoint-04-SharePointFolder1.png)](./media/GERImportFromSharePoint-04-SharePointFolder1.png)

[![Skjalastjórnunarstilling - SharePoint þjónn](./media/GERImportFromSharePoint-05-SharePointFolder2.png)](./media/GERImportFromSharePoint-05-SharePointFolder2.png)

4. Í Finance and Operations, á **Gerðir skjala** síðu, skal búa til eftirfarandi gerðir skjala sem verða notaðar til að komast í SharePoint möppurnar sem þú bjóst til rétt í þessu:

    - SP Aðal
    - SP Annað

5. Fyrir tilbúnar gerðir skjala, í **Hópur** reitinn, skaltu slá inn **Skrá** og í **Staðsetning** reitinn, sláðu inn **SharePoint**. Færið síðan inn staðsetningu SharePoint möppunnar:

    - Fyrir **SP Aðal** gerð skjals: Innflutningsuppruni skráa (aðal)
    - Fyrir **SP Annað** gerð skjals: Innflutningsuppruni skráa (annað)

[![SharePoint stilling - ný gerð skjals](./media/GERImportFromSharePoint-06-SharePointDocumentTypesSetup.png)](./media/GERImportFromSharePoint-06-SharePointDocumentTypesSetup.png)

## <a name="configure-er-sources-for-the-er-format"></a>Grunnstilla ER uppruna fyrir ER sniðið
1. Smelltu á **Stjórnun fyrirtækisins** > **Rafræn skýrslugerð** > **Uppruni rafræn skýrslugerðar**.
2. Á **Uppruni rafræn skýrslugerð** síðunni, skal grunnstilla upprunaskrár fyrir gagnainnflutning með því að nota grunnstillt ER snið.
3. Skilgreindu sniðmát skráarheitis, þannig að aðeins skrár með .xlsx eftirnafninu eru fluttar inn. Sniðmát skráarheitis er valfrjálst og er aðeins notað þegar það hefur verið skilgreint. Þú getur aðeins skilgreint eitt sniðmát fyrir hvert ER-snið.
4. Velja báðar SharePoint möppur sem þú bjóst til áður.

[![Stilling fyrir uppsprettu ER skráa](./media/GERImportFromSharePoint-07-FormatSourceSetup.PNG)](./media/GERImportFromSharePoint-07-FormatSourceSetup.PNG)

> [!NOTE]
>ER *uppspretta* er skilgreind fyrir hvert fyrirtæki fyrir sig innan forritsins. Hins vegar er ER *grunnstillingum* deilt á milli fyrirtækja.

> [!NOTE]
> Þegar þú eyðir ER uppspretta stillingu fyrir ER snið, er staða (sjá hér að neðan) allra tengdra skráa einnig eytt.

## <a name="review-the-files-states-for-the-er-format"></a>Yfirfara skráarstöðurnar fyrir ER sniðið
1. Á **Rafræn skýrslugerð uppspretta** síðu, veldu **Skráarstaða fyrir uppruna** til að fara yfir efni grunnstilltra skráauppruna fyrir núverandi ER snið.
2. Í **Skrár** hlutanum, skoðaðu listann yfir skrár. Þessi listi sýnir eftirfarandi:

    - Upprunaskrár sem eiga við, byggt á sniðmáti skráarheitis (ef sniðmát skráarheitis er skilgreint) og eru tilbúnar til gagnainnflutnings. Fyrir þessar skrár er **Upprunaskrá fyrir innflutningssniðið** hlutinn auður.
    - Áður innfluttar skrár. Fyrir hverjar þessara skráa, í **Upprunaskrá fyrir innflutningssniðið** hlutanum, er hægt að fara yfir innflutningssögu skrárinnar.

Þú getur einnig opnað **Skráarstaða fyrir uppruna** síðuna með því að velja **Stjórnun fyrirtækisins** \> **Rafræn skýrslugerð** \> **Skráarstaða fyrir uppruna**. Í þessu tilfelli veitir síðan upplýsingar um skráaruppruna fyrir öll ER snið sem skráaruppruni hefur verið stilltur fyrir í fyrirtækinu sem þú ert nú skráð inn á.

## <a name="import-data-from-excel-files-that-are-in-a-sharepoint-folder"></a>Flytja inn gögn úr Excel skrám sem eru í SharePoint möppu
1. Í SharePoint, hlaða upp Microsoft Excel skránni **1099import-data.xlsx** sem inniheldur lánardrottnafærslur í **Innflutningsuppspretta skráa (aðal)** SharePoint möppu sem þú bjóst til áðan.

[![SharePoint efni - Microsoft Excel skrá til að flytja inn](./media/GERImportFromSharePoint-08-UploadFile.png)](./media/GERImportFromSharePoint-08-UploadFile.png)

2. Í Finance and Operations, á **Skráarstaða fyrir uppruna** síðu, veldu **Endurglæða** til að endurglæða síðuna. Athugaðu að Excel-skráin, sem var hlaðið upp í SharePoint, birtist á þessari skjámynd með stöðuna **Tilbúin**. Eftirfarandi stöður eru studdir núna:

    - **Tilbúin** - Úthlutað sjálfkrafa fyrir hverja nýja skrá í SharePoint möppu. Þessi staða merkir að skráin er tilbúin til innflutnings.
    - **Innflutningur** - Úthlutað sjálfkrafa af ER skýrslu þegar skráin verður læst með innflutningsferlinu til að koma í veg fyrir notkun þess af öðrum ferlum (ef margir þeirra eru í gangi samtímis).
    - **Innflutt** - Úthlutað sjálfkrafa af ER skýrslu þegar skráarinnflutningur er lokið á fullnægjandi máta. Þessi staða þýðir að innflutt skráin hafi verið eytt úr grunnstilltum skráaruppruna (SharePoint mappa).
    - **Mistókst** - Úthlutað sjálfkrafa af ER skýrslu þegar skráarinnflutningur lýkur með villum eða undantekningum.
    - **Í bið** - Úthlutað handvirkt af notanda á þessari skjámynd. Þessi staða þýðir að skráin verður ekki flutt inn í bili. Þessi staða er hægt að nota til að fresta innflutningi sumra skráa.

[![Síða ER skráarstöðu fyrir valinn uppruna](./media/GERImportFromSharePoint-09-FileStatesForm.png)](./media/GERImportFromSharePoint-09-FileStatesForm.png)

## <a name="import-data-from-sharepoint-files"></a>Flytja inn gögn úr SharePoint skrám
1. Opnaðu ER grunnstillingar tré, veldu **1099 Greiðslulíkan** og útvíkkaðu lista yfir ER líkan íhluti.
2. Veldu heiti vörpunar líkans til að opna listann yfir varpanir líkans af valinni ER grunnstillingu líkans.

[![Síða ER skráarstöðu fyrir valinn uppruna](./media/GERImportFromSharePoint-10-SelectModelMapping.PNG)](./media/GERImportFromSharePoint-10-SelectModelMapping.PNG)

3. Veldu **Keyra** til að keyra valið vörpun líkans. Vegna þess að þú grunnstilltir skráaruppruna fyrir ER sniðið, getur þú breytt stillingunni á **Skráaruppruni** valkostinum eins og þú þarfnast. Ef þú heldur stillingu þessa valkosts eru .xslx skrárnar fluttar frá grunnstilltum uppruna (SharePoint möppurnar, í þessu dæmi).

    Í þessu dæmi flyturðu aðeins eina skrá. Hins vegar, ef það eru margar skrár, eru þau valdar til innflutnings í þeirri röð sem þeim voru bætt við SharePoint möppuna. Sérhver keyrsla af ER-sniði flytur inn eina valda skrá.

[![Keyra ER vörpun líkans](./media/GERImportFromSharePoint-11-RunModelMapping.PNG)](./media/GERImportFromSharePoint-11-RunModelMapping.PNG)

4. Vörpun líkans getur keyrt eftirlitslaus í runuham. Í þessu tilfelli, í hvert skipti sem runa keyrir þetta ER snið, er ein skrá flutt inn frá grunnstilltur skráaruppruni. Notaðu eftirfarandi kóða til að innleiða þessa runukeyrslu.

    ```
    ERObjectsFactory::createMappingDestinationRunByImportFormatMappingId().run()
    ```

    Þegar skrá er flutt inn frá SharePoint möppuna á fullnægjandi máta, er hún eytt úr þeirri möppu.

5. Sláðu inn kenni fylgiskjals, eins og **V-00001**, og veldu síðan **Í lagi**.

[![Keyra ER vörpun líkans](./media/GERImportFromSharePoint-12-ModelMappingRunFinished.PNG)](./media/GERImportFromSharePoint-12-ModelMappingRunFinished.PNG)

6. Á **Skráarstaða fyrir uppruna** síðu, veldu **Endurglæða** til að endurglæða síðuna.

[![Síða ER skráarstöðu fyrir valinn uppruna](./media/GERImportFromSharePoint-13-FileStatesForm.PNG)](./media/GERImportFromSharePoint-13-FileStatesForm.PNG)

7. Í **Skrár** hlutanum, skoðaðu listann yfir skrár. **Upprunaskráin fyrir innflutningssniðið** hlutinn veitir aðgang að sögu Excel skráarinnflutnings. Vegna þess að þessi skrá var flutt inn á fullnægjandi máta, er hún merkt sem **Eytt** í SharePoint möppunni.
8. Yfirfara **Innflutningsuppruni skráa (aðal)** SharePoint möppuna. Excel-skrárnar, sem voru fluttar inn á fullnægjandi máta, hafa verið eytt úr þessum möppu.
9. Í Finance and Operations, veldu **Viðskiptaskuldir** \> **Reglubundin verkefni** \> **Skattur 1099** \> **Lánardrottnauppgjör fyrir 1099s**.
10. Í **Frá dagsetningu** og **Til dagsetningar** reitina, sláðu inn viðeigandi gildi. Veldu síðan **Handvirkt 1099 færslur**.

    Lánardrottnafærslurnar sem voru fluttar inn úr Excel-skrám á SharePoint fyrir fylgiskjal **V-00001** eru birtar á síðunni.

[![1099 lánardrottnafærslur síða](./media/GERImportFromSharePoint-14-ImportedTransactions.PNG)](./media/GERImportFromSharePoint-14-ImportedTransactions.PNG)

## <a name="prepare-an-excel-file-for-import"></a>Undirbúa Excel-skrá fyrir innflutning
1. Opna Excel-skrána sem þú notaðir áður. Í röð 3 dálki 1 skaltu bæta við lánardrottni sem ekki er til í forritinu. Bæta við frekari fölskum lánardrottnaupplýsingar í röðina.

[![Sýnishorn af Microsoft Excel skrá til innflutnings frá SharePoint](./media/GERImportFromSharePoint-15-Excel.PNG)](./media/GERImportFromSharePoint-15-Excel.PNG)

2. Hlaða upp uppfærðri Excel-skrá sem inniheldur lánardrottnafærslur í **Innflutningsuppruni skráa (aðal)** SharePoint möppuna.
3. Í Finance and Operations, opnaðu ER grunnstillingar tré, veldu **1099 Greiðslulíkan** og útvíkkaðu lista yfir ER líkan íhlutir.
4. Veldu nafnið á vörpun líkans til að uppfæra vörpun líkans þannig að rangur lánardrottnakóðinn sé talin vera villa við gagnainnflutningsferli.
5. Veljið **Hönnuður**.
6. Á flipanum **Villuleitir** verður þú að breyta aðgerð að lokinni villuleit fyrir villuleitarregluna sem var grunnstillt til að meta hvort að lánardrottnareikningurinn sem er fluttur inn sé þegar til í forritinu. Uppfærðu gildi í **Aðgerð að lokinni villuleit** reitinn til að **Stöðva framkvæmd**, vista breytingarnar og loka síðunni.

[![ER vörpun líkans hönnuður síða](./media/GERImportFromSharePoint-16-UpdateModelMapping.PNG)](./media/GERImportFromSharePoint-16-UpdateModelMapping.PNG)

7. Vista breytingarnar og loka ER vörpun líkans hönnuður.
8. Veldu **Keyra** til að keyra breytta ER vörpun líkans.
9. Sláðu inn kenni fylgiskjals, eins og **V-00002**, og veldu síðan **Í lagi**.

    Athugaðu að Athugasemdir inniheldur tilkynninguna sem upplýsa að í SharePoint möppu er skrá sem inniheldur rangan lánardrottnareikning og er ekki hægt að flytja inn.

[![Keyra ER vörpun líkans](./media/GERImportFromSharePoint-17-ModelMappingRunFinished.PNG)](./media/GERImportFromSharePoint-17-ModelMappingRunFinished.PNG)

10. Á **Skráarstöður fyrir uppruna** síðu, veldu **Endurglæða**, og síðan, í **Skrár** hlutanum, skoðaðu listann yfir skrár.

[![Síða ER skráarstöðu fyrir valinn uppruna](./media/GERImportFromSharePoint-18-FileStatesForm.PNG)](./media/GERImportFromSharePoint-18-FileStatesForm.PNG)

**Upprunaskrá fyrir innflutningssniðið** hlutinn gefur til kynna að innflutningsferlið mistókst og að skráin sé enn í SharePoint möppunni (**Hefur verið eytt** gátreiturinn er ekki valinn). Ef þú lagar þessa skrá á SharePoint með því að bæta við rétta lánardrottnakóðanum og síðan breyta stöðu skráarinnar frá **Mistókst** til **Tilbúin** í **Upprunaskránni fyrir innflutningssniðið** geturðu flutt skrána inn aftur.

11. Yfirfara **Innflutningsuppruni skráa (aðal)** SharePoint möppuna. Athugið að Excel-skráin sem ekki var flutt inn er ennþá í þessari möppu.
12. Í Finance and Operations, veldu **Viðskiptaskuldir** \> **Reglubundin verkefni** \> **Skattur 1099** \> **Lánardrottnauppgjör fyrir 1099s**, sláðu inn viðeigandi gildi í **Frá dagsetningu** og **Til dagsetningar** og veldu síðan **Handvirkt 1099 færslur**.

    Aðeins færslur fyrir fylgiskjal V-00001 eru tiltækar. Engar færslur fyrir fylgiskjal V-00002 eru tiltækar þótt villan fyrir síðustu innfluttu færslu hafi fundist í Excel-skránni.

