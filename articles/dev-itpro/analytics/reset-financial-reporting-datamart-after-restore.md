---
title: Endurstilla gagnaskemma Financial reporting
description: "Þetta efnisatriði lýsir hvernig á að endurstilla gagnaskemma Financial reporting"
author: aolson
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 261824
ms.search.region: Global
ms.author: aloson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 5b956dcc5a4a93033396ae0ffcf8b7aeba2cf3f2
ms.openlocfilehash: a07e8b5bae2c4f71e9212cd2f8080d2481769818
ms.contentlocale: is-is
ms.lasthandoff: 12/14/2017

---

# <a name="reset-the-financial-reporting-data-mart"></a>Endurstilla gagnaskemma Financial reporting

[!include[banner](../includes/banner.md)]

Þetta efnisatriði útskýrir hvernig á að endurstilla gagnaskemma Financial reporting fyrir eftirfarandi útgáfur:

- Microsoft Dynamics 365 for Finance and Operations Financial reporting útgáfa 7.2.6.0 og síðar
- Microsoft Dynamics 365 for Finance and Operations Financial reporting útgáfa 7.0.10000.4 og síðar
- Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (staðbundin útgáfa)

Til að fá Finance and Operations Financial reporting útgáfu 7.2.6.0, geturðu halað niður KB 4052514 frá <https://fix.lcs.dynamics.com/Issue/Resolved?kb=4052514>.

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-financial-reporting-release-7260-and-later"></a>Endurstilla Financial reporting gagnaskemma fyrir Finance and Operations Financial reporting útgáfa 7.2.6.0 og síðar

### <a name="reset-the-financial-reporting-data-mart-from-report-designer"></a>Endurstilla gagnaskemma Financial reporting frá Report hönnuði

> [!NOTE]
> Skrefin í þessu ferli eru studd fyrir Finance and Operations Financial reporting útgáfa 7.2.6.0. og síðar. Ef þú er með eldri útgáfu skaltu hafa samband við þjónustuver okkar til að fá aðstoð.

Í ákveðnum aðstæðum gætirðu þurft að endurstilla gagnaskemmuna fyrir Financial reporting. Þú getur lokið þessu verki í Report hönnuður biðlara. Hér eru nokkur dæmi þar sem þú gætir þurft að endurstilla gagnaskemmuna:

- Finance and Operations gagnagrunnurinn var endurheimtur, en gagnaskemma gagnasafnið var ekki endurreist.
- Þú sérð röng gögn fyrir tímabil.
- Notendaþjónusta leiðbeinir þér við að endurstilla gagnaskemmuna sem hluti af skrefi úrræðaleitar.

Endurstilling gagnaskemmu ætti aðeins að vera framkvæmd á tímum þegar vinnslumagn í gagnagrunninum er lítið. Financial reporting verður ótiltækt á meðan endurstillingarferlinu stendur.

#### <a name="reset-the-data-mart"></a>Endurstillið gagnaskemmuna:

Til að endurstilla gagnaskemmuna skal á valmyndinni **verkfæri** velja **Endurstilla gagnaskemmu**. Svarglugginn sem birtist inniheldur tvo hluta: **Talnagögn** og **Endurstilla**.

[![Endurstilla gagnaskemma svargluggi](./media/Reset-72.jpg)](./media/Reset-72.jpg)

##### <a name="integration-attempts"></a>Samþættingartilraunir

**Samþættingartilraunir** hnitanetið sýnir hversu oft kerfið hefur reynt að samþætta færslur. Kerfið heldur áfram að reyna að samþætta gögn yfir nokkurra daga tímabil ef fyrstu tilraunirnar mistekst. Þú munt vita að gagnaskemmu verður að endurstilla ef fjöldi tilrauna er 8 eða meira, og ef það eru margar víddarsamsetningar eða færsluskrár. Við þessar aðstæður verður ekki tilkynnt um gögnin.

##### <a name="data-status"></a>Gagnastaða

**Gagnastaða** hnitanet veitir skyndimynd af færslum, gengi og víddargildum í gagnaskemmunni. Mikill fjöldi útrunninna skráa gefur til kynna að fjölmargir uppfærslur á skrám hafi átt sér stað. Þetta ástand gæti valdið hægari myndunartíma skráa.

##### <a name="misaligned-main-account-categories"></a>Vitlaus röðun aðallyklaflokka

Ef þú ert að nota eldri útgáfu en Microsoft Dynamics 365 for Finance and Operations Financial reporting útgáfa 7.2.1, gætir þú þurft að endurstilla gagnaskemmuna ef þú endurnefnir reikninga og færir reikninga á milli reikningsflokka. Þessar aðgerðir geta valdið því að flokkar aðalreikningsins verða ósamstilltir. **Ósamstilltir flokkar aðalreiknings** reiturinn sýnir hvort þú átt við þetta vandamál að stríða.

### <a name="reset-the-data-mart-in-finance-and-operations-financial-reporting-release-7260"></a>Endurstilla gagnaskemmuna í Finance and Operations Financial reporting útgáfa 7.2.6.0

Til að endurstilla gagnaskemmuna í Finance and Operations Financial reporting útgáfa 7.2.6.0 og eldri, í svarglugganum **Endurstilla gagnaskemmu**, veldu gátreitinn **Endurstilla gagnaskemmu** og veldu síðan **Í lagi**. Þú ættir að endurstilla gagnaskemmu aðeins á áætluðum niðurtíma.

[![Endurstilla gagnaskemma gátreitur](./media/Reset-72.jpg)](./media/Reset-72.jpg)

### <a name="reset-the-data-mart-and-select-a-reason-in-microsoft-dynamics-365-for-finance-and-operations-financial-reporting-release-730"></a>Endurstilla gagnaskemmuna og velja ástæðu í Microsoft Dynamics 365 for Finance and Operations Financial reporting útgáfa 7.3.0

Ef þú ákveður að þörf sé á að endurstilla gagnaskemmuna skaltu velja gátreitinn **Endurstilla gagnaskemmu** og veldu síðan ástæðu í **Ástæða** reitnum. Eftirtaldir valkostir eru í boði:

- **Týnd eða röng gögn** - Á grundvelli tölfræðinnar hefur þú ákveðið að gögn gæti vantað. Áður en þú heldur áfram mælum við með því að þú vinnur með notendaþjónustu til að ákvarða hver grunnorsökin er.
- **Endurheimta gagnagrunn** - Finance and Operations gagnagrunnurinn var endurheimtur, en gagnagrunnurinn fyrir Financial reporting gagnaskemmuna var ekki endurreist.
- **Annað** - Þú ert að endurstilla gagnaskemmuna af öðrum ástæðum. Ef þú hefur áhyggjur af því að upp sé komið vandamál skaltu hafa samband við notendaþjónustu til að bera kennsl á það.

[![Endurstilla gagnaskemmu](./media/Integration.png)](./media/Integration.png)

> [!NOTE]
> Gakktu úr skugga um að öll endurstillingarverk gagnaskemma hafi lokið upphaflegu álagi áður en þú hefur endurstillingar. Þú getur staðfest þetta með því að leita að gildi í Síðasta Keyrsla dálknum með því að velja **Verkfæri** &gt; **Samþætting staða**.

#### <a name="clear-users-and-companies"></a>Hreinsa notendur og fyrirtæki

Veldu **hreinsa notendur og fyrirtæki** í gátreitnum ef þú hefur endurheimt gagnagrunninn þinn, en gerðir síðan breytingar á notendum eða fyrirtækjum. Þú ættir sjaldan að þurfa að velja þennan gátreit.

Þegar þú ert tilbúinn til að hefja endurstillingarferlið skaltu velja **Í lagi**. Þú ert beðinn um að staðfesta að þú sért tilbúinn til að hefja ferlið. Athugaðu að Financial reporting verður ekki tiltækt á meðan endurstilling fer fram og fyrsta gagnasamþætting, sem á sér stað eftir endurstillinguna.

Ef þú vilt skoða stöðu samþættingarinnar skaltu velja **Verkfæri** &gt; **Staða samþættingar** til að sjá síðustu skipti sem samþættingin var keyrð og stöðuna.

[![Skoða stöðu samþættingar](./media/New-integration.PNG)](./media/New-integration.PNG)

> [!NOTE]
> Endurstillingin er lokið þegar allar varpanir sýna stöðu RanToCompletion og gluggi Staða samþættingar segir „Samþætting lokið“ neðst í vinstri horni.

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-financial-reporting-release-70100004-and-later"></a>Endrustilla Financial reporting gagnaskemmu fyrir Finance and Operations Financial reporting útgáfa 7.0.10000.4 og síðar

Ef þú einhvern tímann endurheimtir Finance and Operations gagnagrunninn úr öryggisafritum eða afritar gagnagrunninn úr öðru umhverfi, er nauðsynlegt að fylgja skrefunum í þessu efnisatriði til að tryggja að gagnaskemma Financial reporting sé að nota endurheimtan gagnagrunn Finance and Operations á réttan hátt.

> [!NOTE]
> Skrefin í þessu ferli eru studd fyrir Microsoft Dynamics AX forrit útgáfa 7.0.1 (maí 2016) (forrit smíð 7.0.1265.23014 og Financial reporting smíð 7.0.10000.4) og síðar. Ef þú er með eldri útgáfu af Finance and Operations skaltu hafa samband við þjónustuver okkar til að fá aðstoð.

### <a name="export-report-definitions"></a>Flytja út skilgreiningu á skýrslum

Fyrst skaltu fylgja þessum skrefum til að flytja út skýrsluhönnunina frá Report hönnuði.

1. Í Report hönnuður velurðu **Fyrirtæki** &gt; **Einingahópar**.
2. Veldu einingahópinn sem á að flytja út og síðan er smellt á **Flytja út**.

    > [!NOTE]
    > Í Finance and Operations er aðeins einn einingahópur studdur, **Sjálfgefið**.

3. Veldu skýrsluskilgreiningar til að flytja út:

    - Til að flytja út allar skýrsluskilgreiningar og tengdar einingar er smellt á **Velja allt**.
    - Til að flytja út tilteknar skýrslur, línur, dálka, skipurit eða víddasamstæður er smellt á viðeigandi flipa og svo valin atriði til að flytja út. Ýttu á og haltu niðri Ctrl lyklinum til að mörg atriði á flipa. Þegar valdar eru skýrslur til að flytja út eru valdar tengdar línur, dálkar, skipurit og víddasamstæður.

4. Velja **Flytja út**.
5. Færið inn skráarnafn og veljið örugga staðsetningu þar sem á að vista útfluttar skýrsluskilgreiningar.
6. Veldu **Vista**.

Þú getur afritað eða hlaðið inn skrána á öruggan stað. Þannig má flytja skrána inn í annað umhverfi seinna. Upplýsingar um notkun í geymslulykils Microsoft Azure, sjá [Flytja gögn með AzCopy Skipun-Lína hjálparforriti](/azure/storage/storage-use-azcopy).

> [!NOTE]
> Microsoft veitir ekki geymslulykil sem hluta af samningi þínum um Finance and Operations. Annaðhvort verður að kaupa geymslulykil eða nota geymslulykil úr aðskilinni Azure-áskrift.

> [!WARNING]
> Huga skal að hegðun D-drifs á sýndarvélum (VM) Azure. Ekki vista útflutta einingahópa þína til langframa á D-drifi. Sjá frekari upplýsingar um tímabundin drif á [Skilningur á tímabundnum drifum í sýndarvélum Windows Azure](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).

### <a name="stop-services"></a>Stöðvunarþjónusta

Eftirfarandi Microsoft Windows þjónustur munu hafa opnar tengingar við gagnagrunn Finance and Operations. Þar af leiðandi þarftu að nota Microsoft Remote Desktop til að tengjast öllum tölvum í umhverfinu og síðan að stöðva þessa þjónustu með því að nota services.msc.

- Birtingarþjónusta á vefnum (á öllum AOS tölvum)
- Runustjórnunarþjónusta Finance and Operations (aðeins í AOS-tölvum sem ekki eru einkatölvur)
- Ferlaþjónusta Management Reporter 2012 (aðeins á BI tölvum)

### <a name="reset"></a>Endurstilla

#### <a name="download-the-latest-minorversiondataupgradezip-package"></a>Hlaða niður nýjasta MinorVersionDataUpgrade.zip pakkanum

Hlaða niður nýjasta MinorVersionDataUpgrade.zip pakkanum. Fyrir leiðbeiningar um hvernig skal finna og hlaða niður réttu útgáfunni af gagnauppfærslupakkanum, sjá[Hlaða niður nýjustu útgáfu af virkjanlegum gagnauppfærslupakka](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-package). 

Uppfærslu er ekki krafist til að hægt sé að hlaða niður MinorVersionDataUpgrade.zip pakkanum. Þess vegna þarftu bara að fylgja skrefunum í „Afrita nýjustu útgáfu af virkjanlegum gagnauppfærslupakka“ hlutanum í því efnisatriði. Þú getur sleppt öllum öðrum skrefum í efnisatriðinu.

#### <a name="run-scripts-against-the-finance-and-operations-database"></a>Keyra forskriftir gagnvart gagnagrunni Finance and Operations

Keyra eftirfarandi forskriftir gagnvart gagnagrunni Finance and Operations (ekki gagnvart gagnagrunni Financial reporting):

- DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql
- DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql

Þessar forskriftir tryggja að notendur, hlutverk og stillingar á breytingarakningu séu réttar.

#### <a name="run-a-windows-powershell-command-to-reset-the-database"></a>Keyra Windows PowerShell-skipun til að endurstilla gagnagrunninn

Á AOS-tölvunni skal opna Microsoft Windows PowerShell sem stjórnanda, og keyra eftirfarandi skipanir til að endurstilla samþættingu milli Finance and Operations og Financial reporting.

```
F:
cd F:\MRApplicationService\MRInstallDirectory
Import-Module .\Server\MRDeploy\MRDeploy.psd1
Reset-DatamartIntegration -Reason OTHER -ReasonDetail "<reason for resetting>"
```

Hér er skýring á færibreytunum í **Endurstilla-DatamartIntegration** skipuninni:

- Gildu gildin fyrir **-Reason** eru **SERVICING**, **BADDATA**, og **OTHER**.
- **-ReasonDetail** færibreytan er fyrir valkvæman texta.
- Reason og reason detail verða skráð í eftirlit fjarmælingu/umhverfis.

> [!NOTE]
> Eftir keyrslu skipananna verður beðið um að fært sé inn **Y** til að staðfesta að þú viljir endurstilla gagnagrunninn.

#### <a name="restart-services"></a>Endurræsi þjónustu

Nota services.msc að endurræsa þjónustuna sem þú hættir áður:

- Birtingarþjónusta á vefnum (á allar AOS tölvur)
- Runustjórnunarþjónusta Finance and Operations (aðeins í AOS-tölvum sem ekki eru einkatölvur)
- Ferlaþjónusta Management Reporter 2012 (aðeins á BI tölvum)

#### <a name="import-report-definitions"></a>Flytja inn skýrsluskilgreiningu

Flytja inn skýrsluhönnun notanda úr Report hönnuðinum með skránni sem var búin til við útflutninginn.

1. Í Report hönnuður velurðu **Fyrirtæki** &gt; **Einingahópar**.
2. Veldu einingahópinn sem á að flytja út og síðan er smellt á **Flytja út**.

    > [!NOTE]
    > Í Finance and Operations er aðeins einn einingahópur studdur, **Sjálfgefið**.

3. Veldu eininguna **Sjálfgefið** og smelltu á **Innflutning**.
4. Veldu skrána með útfluttum skýrsluskilgreiningum og smelltu á **Opna**.
5. Smellið á skýrsluskilgreiningarnar í svarglugganum **Flytja inn** til að flytja inn:

    - Til að flytja inn allar skýrsluskilgreiningar og tengdar einingar er smellt á **Velja allt**.
    - Til að flytja inn tilteknar skýrslur, línur, dálka, skipurit eða víddasamstæður skal velja skýrslur, línur, dálka, skipurit eða víddasamstæður sem á að flytja inn.

6. Velja **Innflutningur**.

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-on-premises"></a>Endurstilla Financial reporting gagnaskemmu fyrir Finance and Operations Financial (staðbundin útgáfa)

1. Fyrirskipa öllum notendum að fara út úr Report hönnuður og Financial reporting svæði Finance and Operations.
2. Keyra eftirfarandi forskriftir gagnvart gagnagrunni Finance and Operations (MRDB).

    ```
    DECLARE @triggerIds table(id uniqueidentifier, taskTypeId uniqueidentifier)
    INSERT INTO @triggerIds SELECT tr.[Id], tt.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8') -- 'Maintenance Task', 'Map Task'
    PRINT 'Disable integration tasks'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 0 WHERE [Id] in (SELECT id FROM @triggerIds)
    ```

3. Stýfa eða eyða öllum skrám úr FINANCIALREPORTS töflunni í Finance and Operations gagnagrunninum (AXDB).
4. Stýfa eða eyða öllum skrám úr FINANCIALREPORTVERSION töflunni, ef þessi tafla er til staðar í gagnagrunni Finance and Operations. Ef taflan er ekki til í gagnagrunni Finance and Operations, skal sleppa þessu skrefi.
5. Keyra forskriftina **ResetDatamart.sql** gagnvart gagnagrunni Financial reporting. Þessi forskrift gerir óvirka samþættingu gagnaskemmu, eyðir öllum gögnum gagnaskemmu, og endurvirkjar svo samþættingu gagnaskemmu.

    ```
    DECLARE @triggerIds table(id uniqueidentifier, taskTypeId uniqueidentifier)
    INSERT INTO @triggerIds SELECT tr.[Id], tt.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8') -- 'Maintenance Task', 'Map Task'
    PRINT 'Disable integration tasks'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 0 WHERE [Id] in (SELECT id FROM @triggerIds)
    ------------------------------
    PRINT 'Drop archive tables'
    ------------------------------
    DECLARE @tableId nvarchar(max)
    DECLARE dropCursor CURSOR LOCAL FAST_FORWARD FOR
    SELECT Id FROM [Datamart].Archive
    OPEN dropCursor
    FETCH NEXT FROM dropCursor INTO @tableId
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'FactStaging' + @tableId and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].FactStaging' + @tableId)
        IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'DimensionCombinationStaging' + @tableId and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].DimensionCombinationStaging' + @tableId)
        FETCH NEXT FROM dropCursor INTO @tableId
    END
    CLOSE dropCursor
    DEALLOCATE dropCursor
    IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'DimensionCombinationProcessing' and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].DimensionCombinationProcessing')
    ------------------------------
    PRINT 'Begin Truncating tables'
    ------------------------------
    DECLARE @tablename nvarchar(200)
    DECLARE @schemaname nvarchar(200)
    DECLARE clear_tables CURSOR
        FOR SELECT TABLE_NAME, TABLE_SCHEMA FROM INFORMATION_SCHEMA.TABLES WHERE TABLE_SCHEMA = 'Datamart' AND TABLE_TYPE='BASE TABLE'
    PRINT 'remove check constraints'
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
        EXEC('ALTER TABLE [' + @schemaname + '].[' + @tablename + '] NOCHECK CONSTRAINT ALL')
        END
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    ------------------------------
    PRINT 'delete data from tables and rebuild indexes'
    ------------------------------
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
            IF(EXISTS (select TOP 1 1 from sys.foreign_keys where referenced_object_id = OBJECT_ID(@schemaname + '.' + @tablename)) OR
            EXISTS(SELECT TOP 1 1 FROM sys.sql_expression_dependencies sed
            INNER JOIN sys.objects o ON sed.referencing_id = o.[object_id]
            WHERE o.[type] = 'V' 
            AND referenced_schema_name = @schemaname
            AND referenced_entity_name = @tablename))
            BEGIN
            PRINT 'deleting from ' + @tablename
            EXEC('DELETE FROM [' + @schemaname + '].[' + @tablename + ']')
            END
            ELSE
            BEGIN
            PRINT 'truncating from ' + @tablename
            EXEC('TRUNCATE TABLE [' + @schemaname + '].[' + @tablename + ']')
            END
        END
        EXEC('ALTER INDEX ALL ON [' + @schemaname + '].[' + @tablename + '] REBUILD')
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    ------------------------------
    PRINT 'reenable check constraints'
    ------------------------------
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
        EXEC('ALTER TABLE [' + @schemaname + '].[' + @tablename +'] WITH CHECK CHECK CONSTRAINT ALL')
        END
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    DEALLOCATE clear_tables
    ------------------------------
    PRINT 'Complete Truncating tables'
    ------------------------------
    ------------------------------
    PRINT 'Remove indexes from DimensionCombination'
    ------------------------------
    DECLARE @indexname nvarchar(200)
    DECLARE drop_indexes CURSOR
    FOR SELECT Name FROM sys.indexes WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombination]') AND is_primary_key = 0
    OPEN drop_indexes
    FETCH NEXT FROM drop_indexes INTO @indexname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('DROP INDEX [' + @indexname + '] on [Datamart].[DimensionCombination]')
        FETCH NEXT FROM drop_indexes INTO @indexname
    END
    CLOSE drop_indexes
    DEALLOCATE drop_indexes
    ------------------------------
    PRINT 'Drop Columns on DimensionCombination'
    ------------------------------
    DECLARE @objectname nvarchar(200)
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombination]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId', 'InactiveDimensions')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombination] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationResolving'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationResolving]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationResolving] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationStaging'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationStaging]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'OrganizationId', 'Description', 'SourceKey', 'OrganizationKey', 'FreshnessDate')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationStaging] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationUnreferenced'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationUnreferenced]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationUnreferenced] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionValueAttributeValue'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionValueAttributeValue]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('DimensionValueId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionValueAttributeValue] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on FactAttributeValue'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[FactAttributeValue]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('FactId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[FactAttributeValue] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Remove constraints from TranslatedPeriodBalance'
    ------------------------------
    DECLARE @name nvarchar(200)
    DECLARE drop_constraints CURSOR
    FOR SELECT Name FROM sys.default_constraints WHERE parent_object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalance]')
    OPEN drop_constraints
    FETCH NEXT FROM drop_constraints INTO @name
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalance] DROP CONSTRAINT [' + @name + ']')
        FETCH NEXT FROM drop_constraints INTO @name
    END
    CLOSE drop_constraints
    DEALLOCATE drop_constraints
    ------------------------------
    PRINT 'Drop Columns on TranslatedPeriodBalance'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalance]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('PeriodId', 'DimensionsId', 'ScenarioId', 'FactType', 'PostingLayerId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalance] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Remove constraints from TranslatedPeriodBalanceChanges'
    ------------------------------
    DECLARE drop_constraints CURSOR
    FOR SELECT Name FROM sys.default_constraints WHERE parent_object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalanceChanges]')
    OPEN drop_constraints
    FETCH NEXT FROM drop_constraints INTO @name
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalanceChanges] DROP CONSTRAINT [' + @name + ']')
        FETCH NEXT FROM drop_constraints INTO @name
    END
    CLOSE drop_constraints
    DEALLOCATE drop_constraints
    ------------------------------
    PRINT 'Drop Columns on TranslatedPeriodBalanceChanges'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalanceChanges]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('PeriodId', 'DimensionsId', 'ScenarioId', 'FactType', 'PostingLayerId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalanceChanges] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    -- Rebuild dropped indexes that are dynamic
    EXEC [Datamart].ConfigureIndexesAndConstraints
    ------------------------------------------
    ------------------------------------------
    PRINT 'Reset the map tokens'
    UPDATE [Connector].[Map] SET InitalLoad = 0, ReaderToken=NULL, LastQuerySuccess='1900-01-01' WHERE MapId IN (SELECT t.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] = '55D3F71A-2618-4EAE-9AA6-D48767B974D8')
    PRINT 'Reset the tasks'
    UPDATE [Scheduling].[TaskState] SET StateType = 0, Progress = 0.0, LastRunTime = NULL, NextRunTime = NULL WHERE TaskId IN (SELECT ts.[TaskId]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8'))
    PRINT 'Enable integration tasks, RunImmediately'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 1, RunImmediately = 1, StartBoundary = '1900-01-01' 
    WHERE Id in (SELECT [id] from @triggerIds WHERE taskTypeId = '55D3F71A-2618-4EAE-9AA6-D48767B974D8')
    PRINT 'Enable the Maintenance Task'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 1, RunImmediately = 0, StartBoundary = GETDATE() WHERE Id in
    (SELECT [id] from @triggerIds WHERE taskTypeId = 'D81C1197-D486-4FB7-AF8C-078C110893A0')
    ------------------------------------------
    ------------------------------------------
    ```

6. Eftir endurstillinguna geturðu staðfest gagnaendurhleðsluna handvirkt með því að keyra eftirfarandi fyrirspurn gagnvart gagnagrunni Financial reporting.

    ```
    select ReaderObjectName, WriterObjectName, LastRunTime, StateType from Connector.MapsWithDetail with (nolock)
    ```

    Staðfestu að allar raðirnar hafi **LastRunTime** gildi, og að **StateType** sé stillt á **5**. **StateType** gildi upp á **5** gefur til kynna að endurhleðsla gagna hafið heppnast. Gildið **7** tilgreinir villu í stöðu. Stundum hefur Stigveldi fyrirtækis kortið þessa stöðu í fyrsta skipti sem það keyrir. Hins vegar á villustaða að leysast sjálfkrafa.

