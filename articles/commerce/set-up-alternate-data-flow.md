---
title: Settu upp annað gagnaflæði fyrir tillögur
description: Þessi grein lýsir því hvernig á að stilla umhverfi með því að nota annað gagnaflæði til að veita gögn til ráðleggingaþjónustunnar.
author: bebeale
ms.date: 09/08/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.openlocfilehash: b507b9bb57c68aca9424b53f8ccc009efea733bc
ms.sourcegitcommit: f88273627ba105ede27f28fe67ccec2d7f78261c
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/09/2022
ms.locfileid: "9460104"
---
# <a name="set-up-an-alternate-dataflow-for-recommendations"></a>Settu upp annað gagnaflæði fyrir tillögur

[!include [banner](includes/banner.md)]

Þessi grein lýsir því hvernig á að stilla umhverfi með því að nota annað gagnaflæði til að veita gögn til ráðleggingaþjónustunnar.

## <a name="comparison-of-out-of-the-box-dataflow-with-alternate-dataflow"></a>Samanburður á útbúnu gagnaflæði við annað gagnaflæði

Eftirfarandi mynd sýnir út-af-the-box gagnaflæði í umhverfi.

![Gagnaflæði úr kassanum í umhverfi](media/reco-out-of-the-box-dataflow-2.png)

Eftirfarandi mynd sýnir annað gagnaflæði, þar sem runuvinnunni fyrir samstillingu einingageymslu er skipt út fyrir önnur gagnaflæðisskref.

![Gagnaflæði til skiptis í umhverfi](media/reco-alternate-dataflow-2.png)

## <a name="assumptions"></a>Forsendur

- Þessi grein gerir ráð fyrir að þú hafir nú þegar virkjað meðmælaþjónustuna fyrir umhverfið þitt. Fyrir frekari upplýsingar, sjá [Virkjaðu tillögur um vörur](enable-product-recommendations.md).
- Þegar þú ert að vinna með skrár og möppur í Microsoft Azure Data Lake geymslureikningur:

    - Þú getur notað annað hvort Azure vefgáttarviðmótið eða Azure Storage Explorer forritið.
    - Upphafspunktar fyrir að vinna með skrár og möppur eru í **dynamics365-fjármál og rekstur** ílát sem er staðsett undir möppunni sem er nefnd til að passa við vefslóð umhverfisins.
    - Ef nafnið á sandkassaumhverfinu þínu er **MyUAT**, verður grunnslóð umhverfisins `myuat.sandbox.operations.dynamics.com`.
    - Ef fleiri en eitt umhverfi er tengt við sama geymslureikning mun hvert umhverfi hafa sína eigin rótarmöppu.

## <a name="prerequisites"></a>Forkröfur

Eftirfarandi forsendur verða að vera uppfylltar áður en hægt er að innleiða aðra gagnaflæðisaðferðina.

### <a name="set-up-microsoft-power-platform"></a>Setja upp Microsoft Power Platform

Að setja upp Microsoft Power Platform, fylgdu leiðbeiningunum í [Virkjaðu Microsoft Power Platform samþættingu](../fin-ops-core/dev-itpro/power-platform/enable-power-platform-integration.md).

### <a name="install-the-export-to-data-lake-add-in"></a>Settu upp Export to Data Lake viðbótina

Til að setja upp Export to Data Lake viðbótina skaltu fylgja leiðbeiningunum í [Settu upp Export to Azure Data Lake viðbótina](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).

> [!NOTE]
> Athugaðu stillingargildin, því þú þarft þau fyrir sum skrefin sem fylgja.

### <a name="configure-tables-to-export-in-dynamics-365"></a>Stilltu töflur til að flytja út í Dynamics 365

Samstilling töflu frá Dynamics 365 til Azure Data Lake Storage er stjórnað á **Flytja út í Data Lake** síðu. Vegna þess að þessi síða hefur ekki valmyndaratriði eins og er, aðeins notendur í **Kerfisstjóri** öryggishlutverk getur opnað það.

Til að stilla töflur til að flytja út í Dynamics 365 skaltu fylgja þessum skrefum.

1. Til að opna **Flytja út í Data Lake** síðu, bættu við strengnum`?mi=DataFeedsDefinitionWorkspace` í grunnslóð umhverfisins, eins og sýnt er í eftirfarandi dæmi:

    `https://<environment-URL>/?mi=DataFeedsDefinitionWorkspace`

1. Á **Flytja út í Data Lake** síðu og afritaðu töflurnar sem eru skráðar í [Listi yfir smásölukubbatöflur](#list-of-retailsales-cube-tables) kafla þessarar greinar.
1. Í **Kerfisheiti** dálki, stækkaðu listann yfir síuvalkosti.
1. Fyrir síugerðina skaltu velja **er einn af**. Settu síðan bendilinn í textareitinn og límdu listann yfir töflurnar sem þú afritaðir úr **Flytja út í Data Lake** síðu.
1. Neðst á listanum yfir síuvalkosti skaltu velja **Sækja um**.
1. Veldu allar línur í hnitanetinu og veldu síðan **Virkjaðu**.

> [!NOTE]
> Áður en þú ferð í næsta skref verður að uppfæra allar línur í stöðuna **Hlaupandi**. Úrræðaleit og leystu allar villur eftir þörfum.

### <a name="create-a-synapse-workspace"></a>Búðu til Synapse vinnusvæði

Til að búa til Synapse vinnusvæði ef þú ert ekki þegar með það skaltu fylgja leiðbeiningunum í [Flýtiræsing: Búðu til Synapse vinnusvæði](/azure/synapse-analytics/quickstart-create-workspace).

Til að halda Azure auðlindunum þínum skipulögðum mælum við með því að þú setjir Data Lake Storage reikninginn og Synapse vinnusvæðið saman í auðlindahóp í Azure. Þú getur endurnotað geymslureikninginn sem þú bjóst til þegar þú settir upp Export to Data Lake viðbótina.

## <a name="create-a-database-in-synapse-for-recommendation-data-processing"></a>Búðu til gagnagrunn í Synapse fyrir gagnavinnslu meðmæla

Notaðu Common Data Model tólatölvuforritið (CDMUtil_ConsoleApp) til að búa til gagnagrunn á Synapse vinnusvæðinu þínu og fylla hann út úr Common Data Model töflunum í Data Lake Storage. Við mælum með því að þú notir Common Data Model tólið með gagnagrunninum þínum í þróunarumhverfi, ef það eru einhverjar viðbætur.

> [!NOTE]
> Eftirfarandi skref gera ráð fyrir að ekki sé verið að bæta við viðbótagögnum við RetailSales teninginn.

Til að búa til gagnagrunn í Synapse skaltu fylgja þessum skrefum.

1. Fara til [Dynamics-365-FastTrack-Implementation-Assets GitHub](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Analytics/CDMUtilSolution#2-cdmutil-console-app), og fylgdu skrefunum til að hlaða niður **CDMUtilConsoleApp.zip** skrá.
1. Dragðu út zip skrána í staðbundna möppu.
1. Opnaðu **CDMUtil_ConsoleApp.dll.config** skrá í textaritli og uppfærðu eftirfarandi gildi:

    1. Stilltu **Auðkenni leigjanda** gildi (Azure leigjanda auðkenni).
    1. Stilltu **Aðgangslykill** gildi (aðgangslykillinn fyrir Data Lake Storage reikninginn).

        1. Opnaðu geymslureikninginn þinn í Azure gáttinni.
        1. Veldu í valmyndinni vinstra megin á síðunni **Aðgangslyklar**.
        1. Veldu efst á síðunni **Sýna lykla**.
        1. Veldu afritahnappinn fyrir einn af tveimur lykilreitunum og límdu síðan gildið á milli tvöföldu gæsalappanna í stillingarskránni.

    1. Stilltu **ManifestURL** gildi á vefslóðina þína **Tables.manifest.cdm.json** skrá inn Azure Data Lake Storage. Til að fá slóðina skaltu fletta að skránni í Azure gáttinni, velja sporbaug (**...**) hægra megin á skjánum og veldu síðan **Eiginleikar**. Vefslóðin er fyrsta eignin sem er sýnd á **Yfirlit** flipa.
    1. Stilltu **TargetDbConnectionString** gildi fyrir tengistrenginn fyrir innbyggða netþjónalausa SQL-laug Synapse vinnusvæðisins þíns.

        1. Í Synapse vinnusvæðinu skaltu velja **Stjórna** flipa.
        1. Veldu í undirvalmyndinni **SQL laugar**.
        1. Veldu nafnið **Innbyggð** til að skoða eignir laugarinnar.
        1. Í eiginleikaglugganum skaltu velja ADO.NET tengingargerðina sem þú vilt nota. Afritaðu síðan tengistrengsgildið og límdu það á milli tvöföldu gæsalappanna í stillingarskránni.

        > [!NOTE]
        > Þú verður að hafa leyfi til að búa til gagnagrunna. Til að auðvelda notkun gætirðu viljað nota innbyggða **sqladminuser** stjórnandareikningur.

    1. Afskrifaðu athugasemdir við **ProcessEntities** hnút og stilltu gildi hans á **satt** (til dæmis`<add key="ProcessEntities" value ="true"/>`).

1. Vistaðu og lokaðu **CDMUtil_ConsoleApp.dll.config** skrá.
1. Afritaðu **EntityList.json** skrá til **/Auglýsingar** Skrá.
1. Í skipanakvaðningaglugga skaltu keyra **cdmutil_consoleapp.exe**.

> [!NOTE]
> Þegar þú skoðar úttakið ættu að vera 35 einingar/skoðanir, að minnsta kosti 75 töflur og engar villur.

## <a name="prepare-the-data-lake-retailsales-aggregate-measurements-directory"></a>Undirbúa Data Lake smásöluskrána samanlagðar mælingar

### <a name="back-up-your-current-retailsales-cube-data-from-data-lake-storage"></a>Taktu öryggisafrit af núverandi RetailSales teningagögnum frá Data Lake Storage

Auðveldasta leiðin til að taka öryggisafrit af núverandi RetailSales teningagögnum er að endurnefna **Smásala** skrá í Data Lake Storage **Smásöluafrit** eða eitthvað álíka. Þessi aðferð varðveitir núverandi gögn ef þörf er á úrræðaleit síðar.

The **/Smásala** teningamöppu er að finna á eftirfarandi stað:

`<storage-account>/dynamics365-financeandoperations/<environment-url (for example, myuat.sandbox.operations.dynamics.com)>/AggregateMeasurements/RetailSales`

### <a name="create-a-new-retailsales-folder-and-upload-the-model-file"></a>Búðu til nýja RetailSales möppu og hladdu upp líkanaskránni

Til að búa til nýtt **Smásala** möppu og hlaðið upp **model.json** skrá í Data Lake Storage skaltu fylgja þessum skrefum.

1. Búðu til nýja tóma möppu á sama stigi og fyrri möppu og nefndu hana **Smásala**.
1. Hladdu upp **model.json** skrá í nýju möppuna.

## <a name="create-a-pipeline-to-copy-the-retailsales-cube-data"></a>Búðu til leiðslu til að afrita RetailSales teningagögnin

Leiðslan mun lesa RetailSales teningaskoðunina og flytja gögnin út í .csv skrár í Data Lake Storage.

Til að búa til leiðslu til að afrita RetailSales teningagögnin skaltu fylgja þessum skrefum.

1. Í Synapse vinnusvæðinu skaltu velja **Samþætta** flipa.
1. Veldu plús táknið (**+**), og veldu síðan **Flytja inn úr leiðslusniðmáti**.
1. Sæktu og veldu síðan [ExportRetailSalesCubeViews.zip skrá](https://aka.ms/reco-alternate-dataflow-files).
1. Veldu SQL gagnagrunnstengda þjónustuna þína.
1. Veldu þjónustu tengda geymslureikningnum þínum.
1. Opnaðu **Afritaðu gögn** tól, og breyttu **Möppuslóð** eign til **\<environment_name\> /...**.

### <a name="test-execution-of-the-pipeline"></a>Prófframkvæmd leiðslunnar

Við mælum með því að þú prófir leiðsluna með því að nota aðeins eitt útsýni. The **RetailSales_RetailMediaTemplateView** útsýni virkar vel vegna þess að það inniheldur venjulega færri en 10 línur.

## <a name="schedule-the-pipeline-to-run-on-a-recurring-schedule"></a>Tímasettu leiðsluna til að keyra á endurtekinni áætlun

Í hvert skipti sem leiðslan keyrir á sér stað Azure neysla. Við mælum með að þú skipuleggur aftökur með 48 klukkustunda millibili eða lengur. Þú getur alltaf keyrt leiðsluna handvirkt ef þú verður að samstilla gögn strax. 
 
## <a name="table-list-for-synchronization-from-dynamics-365-to-data-lake-storage"></a>Taflalisti fyrir samstillingu frá Dynamics 365 í Data Lake Storage

Eftirfarandi listi yfir töflur er undirmengi af öllum töflunum sem þarf fyrir allan RetailSales teninginn. Aðeins 15 skoðana í RetailSales teningnum eru notuð af ráðleggingaþjónustunni og listi yfir nauðsynlegar töflur var síaður í samræmi við það.

### <a name="list-of-retailsales-cube-tables"></a>Listi yfir smásölukubbatöflur

- BICalendarOffsets
- BIDateDimension
- BIDateDimensionValue
- Vörulisti
- Vörulistarvara
- CatalogProductCategory
- CustInvoiceJour
- CustInvoiceTrans
- CustTable
- DataArea
- DimensionAttributeValueCombination
- DimensionAttributeValueSet
- DirPartyTable
- EcoResCategory
- EcoResCategoryHierarchy
- EcoResCategoryHierarchyHlutverk
- EcoResColor
- EcoResConfiguration
- EcoResProduct
- EcoResProductCategory
- EcoResProductTranslation
- EcoResSize
- EcoResStyle
- HcmWorker
- InventDim
- InventDimCombination
- InventItemGroup
- InventItemGroupItem
- InventItemSetupSupplyType
- InventTable
- InventTrans
- LogisticsAddressCountryRegion
- LogisticsAddressCountryRegionÞýðing
- LogisticsLocation
- LogisticsPostAddress
- OMHIERARKY TILGANGUR
- Smásöluúrval leit
- Smásöluúrval Útlit Rásarhópur
- RetailChannelProfile
- RetailChannelProfileProperty
- RetailChannelTable
- RetailChannelTableExt
- RetailConnDatabaseProfile
- RetailCustInvoiceJourTable
- RetailCustTable
- RetailMediaTemplate
- RetailOfflineProfile
- Smásölutímabilsafsláttur
- RetailRecoListConfigurationParameters
- Retail SalesTaxOverrideGroup
- RetailSharedParameters
- Retail SpecialCategoryMember
- RetailTenderTypeCardTable
- RetailTenderTypeTable
- RetailTerminalTable
- RetailTmpProductMedia
- RetailTransactionDiscountTrans
- RetailTransactionPaymentTrans
- RetailTransactionPaymentTransExt
- RetailTransactionSalesTrans
- RetailTransaction SalesTransExt
- RetailTransactionTable
- SalesLine
- SalesTable
- Kerfisbreytur
- VERSLUNARVÖRUN INTERNALORG
- VERSLUNARHÓPURINN
- VERSLUNARSKIPULAG
- VERSLUNARSérflokkur VARA
- VERSLUNARVÖRUFLOKKUR
- ECORES CONFIGURATION
- STÍÐAREIGNIN
- STÍÐAREIGNINDI GILDASETT
- VIÐMIÐARHÆGÐ
- VIÐMIÐARHJÁRARKÍSAMEINING
- VIÐMIÐARHÆÐARSKIPTI
- STÍÐARVIÐRIÐ
- OMEexplodedOrganizationSecurityGraph

### <a name="view-list-for-the-parameter-to-pass-to-the-synapse-pipeline"></a>Skoðaðu lista fyrir færibreytuna sem á að fara í Synapse leiðsluna

Eftirfarandi með kommum aðskilinn listi inniheldur RetailSales teningsyfirlitið sem leiðslan mun framkvæma "velja" aðgerð á. Það mun síðan afrita niðurstöðurnar í Data Lake Storage.

RetailSales_RetailAssortmentRulesView,RetailSales_RetailChannelNavigationHierarchiesView,RetailSales_RetailChannelNavigationHierarchyCatalogProductsView,RetailSales_RetailChannelNavigationHierarchyCategoryNodesView,RetailSales_RetailChannelNavigationHierarchyCategoryProductsView,RetailSales_RetailMediaBaseUrlChannelView,RetailSales_RetailMediaRelativeUrlProductView,RetailSales_RetailMediaTemplateView,RetailSales_RetailOptOutCustomersView,RetailSales_RetailProductCategory,RetailSales_RetailProductTransaction,RetailSales_RetailProductVariantDimensionsView,RetailSales_RetailRecoListConfigurationParametersView,RetailSales_RetailRecoListsSharedParametersView,RetailSales_RetailEcoResProductTranslation

> [!IMPORTANT]
> Pípufæribreytan verður að vera listi yfir yfirlitsnöfn sem eru aðskilin með stökum kommu. Það mega ekki vera bil eða línustraumar.

## <a name="environment-specific-fixes"></a>Umhverfissértækar lagfæringar

### <a name="retailchannelview-fix"></a>RETAILCHANNELVIEW lagfæring

The **VERSLUNARÁSÚS** útsýni inniheldur harðkóðaða heiltölu sem táknar skipulag af gerðinni "smásölurás". Raunvirði tegundarinnar getur breyst frá umhverfi til umhverfi, eða frá leigjanda til leigjanda.

```SQL
CREATE OR ALTER   VIEW [dbo].[RETAILCHANNELVIEW]
AS
SELECT T1.RECID AS RECID1,
       T1.STOREAREA AS STOREAREA,
       T1.OMOPERATINGUNITID AS OMOPERATINGUNITID,
       T1.DEFAULTCUSTACCOUNT AS DEFAULTCUSTOMER,
       T1.RETAILCHANNELID AS RETAILCHANNELID,
       T1.CHANNELTYPE AS CHANNELTYPE,
       T1.PARTITION AS PARTITION,
       T1.RECID AS RECID,
       T2.OMOPERATINGUNITNUMBER AS OMOPERATINGUNITNUMBER,
       T3.NAME AS NAME
FROM   dbo.RETAILCHANNELTABLE AS T1 CROSS JOIN dbo.DIRPARTYTABLE AS T2 CROSS JOIN dbo.DIRPARTYTABLE AS T3
WHERE  ((((T1.OMOPERATINGUNITID = T2.RECID)
          )
         AND ((T2.RECID = T3.RECID)
              ))
        AND T2.INSTANCERELATIONTYPE IN (8363));
```

Til að uppfæra harðkóðaða heiltöluna skaltu fylgja þessum skrefum.

1. Í Dynamics 365, flettu upp **ChannelID** gildi fyrir netrásina þína.
1. Í tilviki af SQL Server Management Studio (SSMS) sem er tengt við Synapse gagnagrunninn skaltu keyra eftirfarandi fyrirspurn.

    ```SQL
    select INSTANCERELATIONTYPE, NAME, NAMEALIAS, * from dbo.DIRPARTYTABLE where RECID IN (select OMOPERATINGUNITID from dbo.RETAILCHANNELTABLE where RETAILCHANNELID =     <channelID>)
    ```

1. Afritaðu gildið úr fyrsta dálknum (**TILKYNNINGSGERÐ**), og límdu það inn í útsýnisskilgreininguna.

## <a name="troubleshooting"></a>Úrræðaleit

### <a name="pipeline-task-fails"></a>Leiðsluverkefni mistekst

Það ættu að vera 15 framkvæmdir við leiðsluverkefni fyrir **CopyData** verkefni. Ef einhver keyrsla mistekst verður þú að sannreyna að allir háðir SQL hlutir séu til og að fyrirspurnirnar keyri. Auðveldasta leiðin til að komast að öllum ósjálfstæðum er að nota SSMS til að tengjast gagnagrunninum. Þú getur síðan valið og haldið inni (eða hægrismellt) skjá og valið **Búðu til CREATE sem nýjan glugga**.

Villuboðin gætu innihaldið eftirfarandi texta:

- Villa: Bilun átti sér stað á 'uppruna' hlið
- Villa meðhöndlun ytri skráar: 'Hámarks villur telja'.
- /RetailSales/RetailSales_xxxxxx

#### <a name="example-scenario"></a>Dæmi

Í þessu dæmi er **RetailSales_RetailProductCategory** verkefni mistakast og þú færð "Max error count" villuna.

Til að kemba villuna skaltu fylgja þessum skrefum.

1. Opnaðu **EntityList.json** skrá í textaritli (til dæmis,Visual Studio kóða).
1. Finndu útlitsskilgreininguna fyrir **RetailSales_RetailProductCategory**.

    ```SQL
    CREATE  VIEW [dbo].[RetailSales_RetailProductCategory] AS SELECT 0 AS ROW_UNIQUEKEY ,CATEGORY AS CATEGORYID ,PRODUCT AS PRODUCTID ,PRODUCTNAME ,CATEGORYNAME     ,PARENTCATEGORY AS PARENTCATEGORYID ,PARTITION ,RECID FROM RetailProductCategoryView
    ```

1. Þessi skoðun er aðeins háð einni annarri skoðun: **RetailProductCategoryView** _. Finndu útlitsskilgreininguna fyrir _*RetailProductCategoryView**.

    ```SQL
    CREATE VIEW [DBO].[RETAILPRODUCTCATEGORYVIEW] AS SELECT T1.CATEGORY AS CATEGORY, T1.PRODUCT AS PRODUCT, T1.PARTITION AS PARTITION, T1.RECID AS RECID, T2.PRODUCTNAME AS PRODUCTNAME, T2.PARTITION AS PARTITION#2, T3.NAME AS CATEGORYNAME, T3.PARENTCATEGORY AS PARENTCATEGORY, T3.PARTITION AS PARTITION#3 FROM RETAILPRODUCTCATEGORY T1 CROSS JOIN ECORESPRODUCTTRANSLATIONS T2 CROSS JOIN RETAILCATEGORYEXPANDED T3 WHERE((( T1.PRODUCT = T2.PRODUCT) AND ( T1.PARTITION = T2.PARTITION)) AND (( T1.CATEGORY = T3.RECID) AND ( T1.PARTITION = T3.PARTITION)))
    ```

1. Þessi skoðun er háð þremur öðrum skoðunum: **VERSLUNARVÖRUFLOKKUR**, **·**, og **VERSLUNARFLOKKUR Stækkaður**. Finndu skilgreininguna fyrir hvert þessara skoðana og skráðu ósjálfstæði þess. Haltu áfram þar til þú finnur allar háðar skoðanir.

    Hér er allur listinn í tréröð. Staðfesta þarf þrettán skoðanir.

    - RetailSales_RetailProductCategory

        - RetailProductCategoryView

            - VERSLUNARVÖRUFLOKKUR

                - ECORESVÖRUFLOKKUR
                - VIRKUNARFLOKKURHÉRARKÍL
                - VERSLUNARSérflokkur VARA

                    - ECORESVARA
                    - VERSLUNARHÓPURINN
                    - VERSLUNARSérflokkur MEÐLIÐUR

            - ECORESVARUÞÝÐINGAR

                - ECORESVARA
                - ECORESVÖRUÞÝÐING
                - KERFIFRÆÐIR

            - VERSLUNARFLOKKUR Stækkaður

                - VIRKUNARFLOKKUR
                - VIRKUNARFLOKKURHÉRARKÍL

1. Í Excel, búðu til eftirfarandi 13 **veldu fjölda(\*) frá\<view_name\>** yfirlýsingar. Keyrðu þessar yfirlýsingar í SSMS og sendu niðurstöðurnar í texta. Skrunaðu síðan í gegnum niðurstöðurnar til að sjá hvort eitthvað af skoðunum mistókst. Upphafsvillan bendir til þess að að minnsta kosti eitt af skoðunum muni mistakast.

    ```SQL
    select count(*) from RetailProductCategoryView
    select count(*) from RETAILPRODUCTCATEGORY
    select count(*) from ECORESPRODUCTCATEGORY
    select count(*) from ECORESCATEGORYHIERARCHYROLE
    select count(*) from RETAILSPECIALCATEGORYPRODUCT
    select count(*) from ECORESPRODUCT
    select count(*) from RETAILGROUPMEMBERLINE
    select count(*) from RETAILSPECIALCATEGORYMEMBER
    select count(*) from ECORESPRODUCTTRANSLATIONS
    select count(*) from ECORESPRODUCTTRANSLATION
    select count(*) from SYSTEMPARAMETERS
    select count(*) from RETAILCATEGORYEXPANDED
    select count(*) from ECORESCATEGORY
    ```

1. Ein leið til að sannreyna það sem þú ert að skoða er að búa til rótháð útsýni til að búa til skoðanaskilgreininguna í SSMS. Staðfestu síðan að það sé Azure Data Lake skráardálkur sem heitir **r.skráarslóð**. Tilvist þessa dálks gefur til kynna að útsýnið sem þú ert að skoða sé að lesa gögn frá Data Lake Storage.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir afurðarráðleggingar](product-recommendations.md)

[Virkja Azure Data Lake Storage í Dynamics 365 Commerce-umhverfi](enable-adls-environment.md)

[Kveikja á sérsniðnum tillögum](personalized-recommendations.md)

[Virkja tillögur um að kaupa svipaða vöru](shop-similar-looks.md)

[Afþakka sérsniðnar tillögur](personalization-gdpr.md)

[Bæta afurðaráðleggingum við sölustað](product.md)

[Bæta við tillögum á færsluskjáinn](add-recommendations-control-pos-screen.md)

[Aðlagaðu niðurstöður AI-ML](modify-product-recommendation-results.md)

[Búðu til handvirkt myndaðar ráðleggingar](create-editorial-recommendation-lists.md)

[Búðu til tillögur með kynningargögnum](product-recommendations-demo-data.md)

[Algengar spurningar um afurðaráðleggingar](faq-recommendations.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
