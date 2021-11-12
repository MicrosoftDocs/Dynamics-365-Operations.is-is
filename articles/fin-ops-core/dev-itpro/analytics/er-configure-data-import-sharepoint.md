---
title: Skilgreina gagnainnflutning úr SharePoint
description: Þetta efnisatriði útskýrir hvernig á að flytja inn gögn frá Microsoft SharePoint.
author: NickSelin
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 6cd717c0c599d68574a5a064761c8d6777418515
ms.sourcegitcommit: 1707cf45217db6801df260ff60f4648bd9a4bb68
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/23/2021
ms.locfileid: "7675346"
---
# <a name="configure-data-import-from-sharepoint"></a>Skilgreina gagnainnflutning úr SharePoint

[!include[banner](../includes/banner.md)]

Til að flytja inn gögn úr skrá á innleið með því að nota rafræna skýrslugerð (ER) ramma, þarftu að grunnstilla ER snið sem styður innflutninginn og síðan keyra vörpun líkans af **Til áfangastaðar** gerðinni sem notar þetta snið sem gagnagjafa. Til að flytja inn gögn verður þú að fara í skrána sem þú vilt flytja inn. Skráin sem er á innleið er hægt að velja handvirkt af notanda. Með nýja ER-eiginleikanum til að styðja við innflutning gagna frá Microsoft SharePoint, getur þetta ferli verið grunnstillt sem óvaktað. Þú getur notað ER stillingar til að framkvæma gagnainnflutning frá skrám sem eru geymd í Microsoft SharePoint möppum. Þetta efnisatriði útskýrir hvernig á að ljúka innflutningi frá SharePoint. Dæmin nota lánardrottnafærslur sem viðskiptagögn.

## <a name="prerequisites"></a>Forkröfur
Til að ljúka dæmunum í þessu efnisatriði þarftu að hafa eftirfarandi aðgang:

- Farðu í eitt af eftirfarandi hlutverkum:

    - Þróunaraðili rafrænnar skýrslulausnar
    - Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar
    - Kerfisstjóri

- Aðgangur að tilviki Microsoft SharePoint þjóns sem er grunnstillt til notkunar með forritinu.
- ER-snið og grunnstillingar líkans fyrir 1099 greiðslur.

### <a name="create-required-er-configurations"></a>Búðu til nauðsynlegar ER grunnstillingar
Spila **ER flytja inn gögn úr Microsoft Excel skrá** verkefnaleiðbeiningar, sem eru hluti af **7.5.4.3 Fá/Þróa upplýsingatækniþjónustu/lausn íhlutir (10677)** viðskiptaferli. Þessar verkefnaleiðbeiningar fylgja þér í gegnum ferlið við að hanna og nota ER grunnstillingar til að flytja inn lánardrottnafærslur á gagnvirkan máta frá Microsoft Excel skrám. Nánari upplýsingar er að finna í [Þátta skjöl á innleið á Excel-sniði](parse-incoming-documents-excel.md). Eftir að lokið hefur verið við verkefnaleiðbeiningarnar verður uppsetningin eftirfarandi.

#### <a name="er-configurations"></a>ER grunnstillingar

- ER grunnstillingar líkans, **1099 Greiðslulíkan**
- ER grunnstillingar sniðs, **Snið til að flytja inn lánardrottnafærslur frá Excel**

![ER grunnstillingar til að flytja inn gögn frá SharePoint.](./media/GERImportFromSharePoint-01-Configurations.PNG)

#### <a name="sample-of-the-incoming-file-for-data-import"></a>Sýnishorn af skrá á innleið fyrir gagnainnflutning

- Excel skrá **1099import-data.xlsx**, með lánardrottnafærslur sem ættu að vera fluttar inn.

![Excel-sýniskrá til að flytja út úr SharePoint.](./media/GERImportFromSharePoint-02-Excel.PNG)
    
> [!NOTE]
> Sniðið til að flytja inn lánardrottnafærslur er valið sem sjálfgefin vörpun líkans. Þess vegna, ef þú keyrir vörpun líkans **1099 Greiðslulíkan**, og þessi vörpun líkans er af **Til áfangastaðar** gerðinni, keyrir vörpun líkans þetta snið til að flytja inn gögn úr ytri skrám. Það notar síðan þessi gögn til að uppfæra töflur í forriti.

## <a name="configure-access-to-sharepoint-for-file-storage"></a>Grunnstilla aðgang að SharePoint fyrir skráargeymslu
Til að geyma skrár rafrænnar skýrslu á SharePoint-staðsetningu verður að grunnstilla aðgang að tilviki SharePoint Server sem núverandi fyrirtæki kemur til með að nota. Í þessu dæmi er fyrirtækið USMF. Nánari leiðbeiningar er að finna í [Grunnstilla SharePoint geymslu](../../fin-ops/organization-administration/configure-document-management.md#configure-sharepoint-storage).

1. Ljúkið skrefunum í [Grunnstilla SharePoint-geymslu](../../fin-ops/organization-administration/configure-document-management.md#configure-sharepoint-storage).
2. Opnið skilgreinda SharePoint svæðið.
3. Stofnið eftirfarandi möppur þar sem hægt er að geyma skrár rafrænnar skýrslugerðar á innleið:

     - Innflutningsuppruni skráa (aðal) (Dæmi sýnt á skjámynd hér að neðan)
     - Innflutningsuppruni skráa (annað)

    ![Innflutningsuppruni skráa (aðal).](./media/GERImportFromSharePoint-04-SharePointFolder1.png)

4. (Valfrjálst) Stofnið eftirfarandi möppur þar sem hægt er að geyma skrárnar eftir innflutning. 

    - Skjalasafnsmappa - Þessi mappa yrði fyrir skrár sem tókst að flytja inn.
    - Mappa viðvörunarskráa - Þessi mappa yrði fyrir skrár sem væru fluttar inn með viðvörun.
    - Mappa villuskráa - Þessi mappa yrði fyrir skrár sem ekki tókst að flytja inn.

4. Farðu í **Fyrirtækjastjórnun > Skjalastjórnun > Skjalagerðir**.
5. Stofnið eftirfarandi skjalagerðir sem verða notaðar til að fá aðgang að möppum SharePoint sem voru stofnaðar. Nánari leiðbeiningar er að finna í [Grunnstilla skjalagerðir](../../fin-ops/organization-administration/configure-document-management.md#configure-document-types).

|Gerð skjals       | Hópur              | Staður      | SharePoint-mappa      |
|--------------------|--------------------|---------------|------------------------|
|SP Aðal             |Skrá                |SharePoint     |Innflutningsuppruni skráa (aðal)|
|SP Annað             |Skrá                |SharePoint     |Innflutningsuppruni skráa (annað)|
|SP-skjalasafn             |Skrá                |SharePoint     |Skjalasafnsmappa|
|SP-viðvörun             |Skrá                |SharePoint     |Mappa viðvörunarskráa|
|SP-villa             |Skrá                |SharePoint     |Mappa villuskráa|

![SharePoint-stillingar - ný gerð skjals.](./media/GERImportFromSharePoint-06-SharePointDocumentTypesSetup.png)

## <a name="configure-er-sources-for-the-er-format"></a>Grunnstilla ER uppruna fyrir ER sniðið
1. Smelltu á **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Uppruni rafrænnar skýrslugerðar**.
2. Á **Uppruni rafræn skýrslugerð** síðunni, skal grunnstilla upprunaskrár fyrir gagnainnflutning með því að nota grunnstillt ER snið.
3. Skilgreindu sniðmát skráarheitis, þannig að aðeins skrár með .xlsx eftirnafninu eru fluttar inn. Sniðmát skráarheitis er valfrjálst og er aðeins notað þegar það hefur verið skilgreint. Þú getur aðeins skilgreint eitt sniðmát fyrir hvert ER-snið.
4. Breyta **Raða skrám fyrir innflutning** í **Ekki raða** ef flytja á inn nokkrar skrár og innflutningsröðin er ekki mikilvæg
5. Velja allar SharePoint-möppur sem þú bjóst til áður.

    [![Stilling fyrir uppsprettu ER skráa](./media/GERImportFromSharePoint-07-FormatSourceSetup.PNG)](./media/GERImportFromSharePoint-07-FormatSourceSetup.PNG).

> [!NOTE]
> - ER *uppspretta* er skilgreind fyrir hvert fyrirtæki fyrir sig innan forritsins. Hins vegar er ER *grunnstillingum* deilt á milli fyrirtækja.
> - Þegar þú eyðir stillingu fyrir uppsprettu ER fyrir ER-snið, er stöðu (sjá hér að neðan) allra tengdra skráa einnig eytt.

## <a name="review-the-files-states-for-the-er-format"></a>Yfirfara skráarstöðurnar fyrir ER sniðið
1. Á **Rafræn skýrslugerð uppspretta** síðu, veldu **Skráarstaða fyrir uppruna** til að fara yfir efni grunnstilltra skráauppruna fyrir núverandi ER snið.
2. Í **Skrár** hlutanum, skoðaðu listann yfir skrár. Þessi listi sýnir eftirfarandi:

    - Upprunaskrár sem eiga við, byggt á sniðmáti skráarheitis (ef sniðmát skráarheitis er skilgreint) og eru tilbúnar til gagnainnflutnings. Fyrir þessar skrár er **Upprunaskrá fyrir innflutningssniðið** hlutinn auður.
    - Áður innfluttar skrár. Fyrir hverjar þessara skráa, í **Upprunaskrá fyrir innflutningssniðið** hlutanum, er hægt að fara yfir innflutningssögu skrárinnar.

Þú getur einnig opnað **Skráarstaða fyrir uppruna** síðuna með því að velja **Stjórnun fyrirtækisins** \> **Rafræn skýrslugerð** \> **Skráarstaða fyrir uppruna**. Í þessu tilfelli veitir síðan upplýsingar um skráaruppruna fyrir öll ER snið sem skráaruppruni hefur verið stilltur fyrir í fyrirtækinu sem þú ert nú skráð inn á.

## <a name="import-data-from-excel-files-that-are-in-a-sharepoint-folder"></a>Flytja inn gögn úr Excel skrám sem eru í SharePoint möppu
1. Í SharePoint, hlaða upp Microsoft Excel skránni **1099import-data.xlsx** sem inniheldur lánardrottnafærslur í **Innflutningsuppspretta skráa (aðal)** SharePoint möppu sem þú bjóst til áðan.

    [![SharePoint efni - Microsoft Excel skrá fyrir innflutning.](./media/GERImportFromSharePoint-08-UploadFile.png)](./media/GERImportFromSharePoint-08-UploadFile.png)

2. Á **Skráarstaða fyrir uppruna** síðu, veldu **Endurglæða** til að endurglæða síðuna. Excel-skráin, sem var hlaðið upp í SharePoint, birtist á þessari síðu með stöðuna **Tilbúin**. Eftirfarandi stöður eru studdir núna:

    - **Tilbúin** – Úthlutað sjálfkrafa fyrir hverja nýja skrá í SharePoint-möppu. Þessi staða merkir að skráin er tilbúin til innflutnings.
    - **Innflutningur** – Úthlutað sjálfkrafa af ER skýrslu þegar skráin verður læst með innflutningsferlinu til að koma í veg fyrir notkun þess af öðrum ferlum (ef margir þeirra eru í gangi samtímis).
    - **Innflutt** – Úthlutað sjálfkrafa af ER skýrslu þegar skráarinnflutningi er lokið á fullnægjandi máta. Þessi staða þýðir að innflutt skráin hafi verið eytt úr grunnstilltum skráaruppruna (SharePoint mappa).
    - **Mistókst** – Úthlutað sjálfkrafa af ER skýrslu þegar skráarinnflutningi lauk með villum eða undantekningum.
    - **Í bið** – Notandi úthlutar handvirkt á þessari síðu. Þessi staða þýðir að skráin verður ekki flutt inn í bili. Þessi staða er hægt að nota til að fresta innflutningi sumra skráa.

    [![Uppfærð síða ER skráarstöðu fyrir valinn uppruna.](./media/GERImportFromSharePoint-09-FileStatesForm.png)](./media/GERImportFromSharePoint-09-FileStatesForm.png)

## <a name="import-data-from-sharepoint-files"></a>Flytja inn gögn úr SharePoint skrám.
1. Opnaðu ER grunnstillingar tré, veldu **1099 Greiðslulíkan** og útvíkkaðu lista yfir ER líkan íhluti.
2. Veldu heiti vörpunar líkans til að opna listann yfir varpanir líkans af valinni ER grunnstillingu líkans.

    [![Stillingasíða.](./media/GERImportFromSharePoint-10-SelectModelMapping.PNG)](./media/GERImportFromSharePoint-10-SelectModelMapping.PNG)

3. Veldu **Keyra** til að keyra valið vörpun líkans. Vegna þess að þú grunnstilltir skráaruppruna fyrir ER-sniðið, getur þú breytt stillingunni í valkostinum **Skráaruppruni** ef þörf krefur. Ef þú heldur stillingu þessa valkosts eru .xslx skrárnar fluttar frá grunnstilltum uppruna (SharePoint-möppurnar, í þessu dæmi).

    Í þessu dæmi flyturðu aðeins eina skrá. Hins vegar, ef það eru margar skrár, eru þau valdar til innflutnings í þeirri röð sem þeim voru bætt við SharePoint möppuna. Sérhver keyrsla af ER-sniði flytur inn eina valda skrá.

    [![Flytja inn úr SharePoint og keyra líkansvörpun rafrænnar skýrslugerðar.](./media/GERImportFromSharePoint-11-RunModelMapping.PNG)](./media/GERImportFromSharePoint-11-RunModelMapping.PNG)

4. Vörpun líkans getur keyrt [eftirlitslaus](#limitations) í runustillingu. Í þessu tilfelli, í hvert skipti sem runa keyrir þetta ER snið, er ein skrá flutt inn frá grunnstilltur skráaruppruni.

    Þegar skrá er flutt inn frá SharePoint-möppunni á fullnægjandi máta, er henni eytt úr þeirri möppu og færð í möppu fyrir skrár sem tókst að flytja inn eða í möppuna fyrir innfluttar skrár með viðvörun. Annars er hún færð í möppu fyrir mislukkaðar skrár eða er geymd í þessari möppu ef ekki er búið að setja upp möppuna fyrir mislukkaðar skrár. 

5. Sláðu inn kenni fylgiskjals, eins og **V-00001**, og veldu síðan **Í lagi**.

    [![Keyra ER vörpun líkans.](./media/GERImportFromSharePoint-12-ModelMappingRunFinished.PNG)](./media/GERImportFromSharePoint-12-ModelMappingRunFinished.PNG)

6. Á **Skráarstaða fyrir uppruna** síðu, veldu **Endurglæða** til að endurglæða síðuna.

    [![Skráarstöður rafrænnar skýrslugerðar fyrir upprunasíðuna.](./media/GERImportFromSharePoint-13-FileStatesForm.PNG)](./media/GERImportFromSharePoint-13-FileStatesForm.PNG)

7. Í **Skrár** hlutanum, skoðaðu listann yfir skrár. **Upprunaskráin fyrir innflutningssniðið** hlutinn veitir aðgang að sögu Excel skráarinnflutnings. Vegna þess að þessi skrá var flutt inn á fullnægjandi máta, er hún merkt sem **Eytt** í SharePoint möppunni.
8. Yfirfara **Innflutningsuppruni skráa (aðal)** SharePoint möppuna. Excel-skrárnar, sem voru fluttar inn á fullnægjandi máta, hafa verið eytt úr þessum möppu.
9. Veldu **Viðskiptaskuldir** \> **Reglubundin verkefni** \> **Skattur 1099** \> **Uppgjör lánardrottins fyrir 1099**.
10. Í **Frá dagsetningu** og **Til dagsetningar** reitina, sláðu inn viðeigandi gildi. Veldu síðan **Handvirkt 1099 færslur**.

    Lánardrottnafærslurnar sem voru fluttar inn úr Excel-skrám á SharePoint fyrir fylgiskjal **V-00001** eru birtar á síðunni.

    [![Síða 1099 lánardrottnafærslna.](./media/GERImportFromSharePoint-14-ImportedTransactions.PNG)](./media/GERImportFromSharePoint-14-ImportedTransactions.PNG)

## <a name="prepare-an-excel-file-for-import"></a>Undirbúa Excel-skrá fyrir innflutning
1. Opna Excel-skrána sem þú notaðir áður. Í röð 3 dálki 1 skaltu bæta við lánardrottni sem ekki er til í forritinu. Bæta við frekari fölskum lánardrottnaupplýsingar í röðina.

    [![Sýnishorn Microsoft Excel skrá til að flytja út úr SharePoint.](./media/GERImportFromSharePoint-15-Excel.PNG)](./media/GERImportFromSharePoint-15-Excel.PNG)

2. Hlaða upp uppfærðri Excel-skrá sem inniheldur lánardrottnafærslur í **Innflutningsuppruni skráa (aðal)** SharePoint möppuna.
3. Opnaðu ER grunnstillingar tré, veldu **1099 Greiðslulíkan** og útvíkkaðu lista yfir ER líkan íhluti.
4. Veldu nafnið á vörpun líkans til að uppfæra vörpun líkans þannig að rangur lánardrottnakóðinn sé talin vera villa við gagnainnflutningsferli.
5. Veljið **Hönnuður**.
6. Á flipanum **Villuleitir** verður þú að breyta aðgerð að lokinni villuleit fyrir villuleitarregluna sem var grunnstillt til að meta hvort að lánardrottnareikningurinn sem er fluttur inn sé þegar til í forritinu. Uppfærðu gildi í **Aðgerð að lokinni villuleit** reitinn til að **Stöðva framkvæmd**, vista breytingarnar og loka síðunni.

    [![Hönnuðarsíða ER-líkanavörpunar.](./media/GERImportFromSharePoint-16-UpdateModelMapping.PNG)](./media/GERImportFromSharePoint-16-UpdateModelMapping.PNG)

7. Vista breytingarnar og loka ER vörpun líkans hönnuður.
8. Veldu **Keyra** til að keyra breytta ER vörpun líkans.
9. Sláðu inn kenni fylgiskjals, eins og **V-00002**, og veldu síðan **Í lagi**.

    Upplýsingaskrá inniheldur tilkynningu um að í SharePoint-möppu sé skrá sem inniheldur rangan lánardrottnalykil og er ekki hægt að flytja inn.

    [![Loknar keyrslur ER vörpun líkans.](./media/GERImportFromSharePoint-17-ModelMappingRunFinished.PNG)](./media/GERImportFromSharePoint-17-ModelMappingRunFinished.PNG)

10. Á **Skráarstöður fyrir uppruna** síðu, veldu **Endurglæða**, og síðan, í **Skrár** hlutanum, skoðaðu listann yfir skrár.

    [![Síða ER skráarstöðu fyrir valinn uppruna.](./media/GERImportFromSharePoint-18-FileStatesForm.PNG)](./media/GERImportFromSharePoint-18-FileStatesForm.PNG)

   **Upprunaskrá fyrir innflutningssniðið** hlutinn gefur til kynna að innflutningsferlið mistókst og að skráin sé í SharePoint möppunni fyrir villuskrár (gátreiturinn **Hefur verið eytt** er ekki valinn). Ef þú lagar þessa skrá á SharePoint með því að bæta við rétta lánardrottnakóðanum og síðan færa hana í SharePoint-möppuna Innflutningsuppruni skráa (aðal), geturðu flutt skrána inn aftur.

11. Veldu **Viðskiptaskuldir** \> **Reglubundin verkefni** \> **Skattur 1099** \> **Lánardrottnauppgjör fyrir 1099s**, sláðu inn viðeigandi gildi í **Frá dagsetningu** og **Til dagsetningar** og veldu síðan **Handvirkt 1099 færslur**.

    Aðeins færslur fyrir fylgiskjal V-00001 eru tiltækar. Engar færslur fyrir fylgiskjal V-00002 eru tiltækar þótt villan fyrir síðustu innfluttu færslu hafi fundist í Excel-skránni.

## <a name=""></a><a name="limitations">Takmarkanir</a>

Rammi rafrænnar skýrslugerðar býður ekki upp á getuna til að hefja nýja runuvinnslu sem framkvæmir líkanavörpun í fjarverustillingu fyrir gagnainnflutning. Til að gera þetta verður þú að þróa ný rök þannig að hægt sé að kalla á skilgreinda líkansvörpun rafrænnar skýslugerðar frá notendaviðmóti forritsins til að flytja inn gögn af skrám á innleið. Þess vegna er einhver hönnunarvinna nauðsynleg. 

Frekari upplýsingar um API rafrænnar skýrslugerðar er að finna í hlutanum [Kóði til að keyra vörpun sniðs við gagnainnflutning](er-apis-app73.md#code-to-run-a-format-mapping-for-data-import) í efnisatriðinu [Breytingar á API fyrir ramma rafrænnar skýrslugerðar fyrir uppfærslu forrits 7.3](er-apis-app73.md).

Farið yfir kóðann í `BankImport_RU` -klasanum fyrir `Application Suite` -líkan til að sjá hvernig hægt er að innleiða sérsniðnu rökin. Þessi klasi víkkar `RunBaseBatch`-klasann. Skoðið sérstaklega `runER()` aðferðina þar sem `ERIModelMappingDestinationRun`-hluturinn er búinn til sem keyrsla á líkansvörpun rafrænnar skýrslugerðar.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir rafræna skýrslugerð](general-electronic-reporting.md)

[Breytingar á API fyrir ramma rafrænnar skýrslugerðar fyrir uppfærslu forrits 7.3](er-apis-app73.md)

[Breytingar á API fyrir ramma rafrænnar skýrslugerðar fyrir uppfærslu forrits 10.0.23](er-apis-app10-0-23.md)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
