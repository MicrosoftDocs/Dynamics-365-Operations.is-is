---
title: Tilgreina sérsniðinn geymslustað fyrir mynduð skjöl
description: Þetta efnisatriði útskýrir hvernig á að stækka listann yfir geymslustaði fyrir skjöl sem snið rafrænnar skýrslugerðar myndar.
author: NickSelin
ms.date: 10/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-3-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 337e760f28161721d886c7bbec09b5ff8dbfad45
ms.sourcegitcommit: e40a9fac5bac9f57a6dcfe73a1f21856eab9b6a9
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/02/2021
ms.locfileid: "7594910"
---
# <a name="specify-custom-storage-locations-for-generated-documents"></a>Tilgreina sérsniðinn geymslustað fyrir mynduð skjöl

[!include[banner](../includes/banner.md)]

Forritunarviðmót forritsins (API) fyrir ramma rafrænnar skýrslugerðar gerir þér kleift að stækka listann yfir geymslustaði fyrir skjöl sem snið rafrænnar skýrslugerðar myndar. Þetta efnisatriði útskýrir hvernig á að bæta við sérstilltum geymslustað fyrir mynduð skjöl með því að úthluta verkinu fyrir stofnun viðtökustaða rafrænnar skýrslugerðar í sjálfgefinni staðsetningu verksmiðju og síðan innleiða sérstilltan klasa sem er með sína eigin reglu um endastað.

## <a name="prerequisites"></a>Forkröfur

Setja upp grannfræði sem styður samfellda smíði. Nánari upplýsingar er að finna [Setja upp grannfræði sem styður samfellda smíði og sjálfvirkni prófunar](/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation). Það þarf að hafa aðgang að þessari grannfræði fyrir eitt af eftirfarandi hlutverkum:

- Þróunaraðili rafrænnar skýrslulausnar
- Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar
- Kerfisstjóri

Þú verður einnig að hafa aðgang að þróunarumhverfi fyrir þessa grannfræði.

Hægt er að ljúka verkunum í þessu efnisatriði í fyrirtækinu **USMF**.

## <a name="import-the-fixed-asset-roll-forward-er-format"></a>Flytja inn rafrænt skýrslugerðarsnið fyrir framlengingu eignar

Til að mynda skjölin sem ætlunin er að bæta sérstilltum geymslustað við, skal [flytja inn](er-download-configurations-global-repo.md) skilgreininguna **Framlenging eigna** fyrir rafrænt skýrslugerðarsnið í núverandi grannfræði.

![Gagnageymslusíða skilgreiningar.](./media/er-custom-storage-generated-files-import-format.png)

## <a name="run-the-fixed-asset-roll-forward-report"></a>Keyra skýrsla fyrir framlengingu eigna

1. Farið í **Eignir** \> **Fyrirspurnir og skýrslur** \> **Færsluskýrslur** \> **Framlenging eigna**.
2. Í reitinn **Frá dagsetningu** skal slá inn **1/1/2017** (1. janúar 2017).
3. Í reitinn **Til dagsetningar** skal slá inn **31/1/2017** (31. janúar 2017).
4. Í **Gjaldmiðilsreitnum** skal velja **Bókhaldsgjaldmiðil**.
5. Í reitnum **Sniðsvörpun** skal velja **Framlenging eigna**.
6. Veldu **Í lagi**.

![Keyrslugluggi fyrir skýrslu um framlengingu eigna.](./media/er-custom-storage-generated-files-runtime-dialog.png)

Í Microsoft Excel skal fara yfir skjal á útleið sem er myndað og tilbúið til niðurhals. Þessi hegðun er [sjálfgefin hegðun](electronic-reporting-destinations.md#default-behavior) fyrir snið rafrænnar skýrslugerðar þar sem engir [viðtökustaðir](electronic-reporting-destinations.md) eru skilgreindir og er keyrt í gagnvirkri stillingu.

## <a name="review-the-source-code"></a>Skoða upprunakóðann

Yfirfarið kóða `generateReportByGER()`-aðferðarinnar fyrir `AssetRollForwardService`-klasann. Takið eftir því að `Run()`-aðferðin er notuð til að kalla á ramma rafrænnar skýrslugerðar og mynda skýrsluna **Framlenging eigna**.

```xpp
class AssetRollForwardService extends SysOperationServiceBase
{
    public const str ERFormatModelName = 'Fixed assets';
    public const str ERModelDataSourceName = 'model';
    public const str DefaultExportedFileName = 'AssetRollForward';

    /// <summary>
    /// Generates report by general electronic reporting
    /// </summary>
    /// <param name = "_contract">The Asset Period Statement contract</param>
    public void generateReportByGER(AssetRollForwardContract _contract)
    {
        ERFormatMappingId   formatMappingId;
        AssetRollForwardDP  dataProvider;
        AssetRollForwardTmp assetRollForwardTmp;
        Query               query;

        query = new Query(SysOperationHelper::base64Decode(_contract.parmQuery()));
        dataProvider = AssetRollForwardDP::construct();
        formatMappingId = _contract.parmFormatMapping();
        assetRollForwardTmp = dataProvider.getAssetRollForwardTmp(_contract, query);

        if (assetRollForwardTmp)
        {
            try
            {
                ERIModelDefinitionParamsAction parameters = new ERModelDefinitionParamsUIActionComposite()
                    .add(new ERModelDefinitionDatabaseContext().addTemporaryTable(assetRollForwardTmp))
                    .add(new ERModelDefinitionObjectParameterAction(ERModelDataSourceName, 'MyParameters', _contract, true));

                // Call ER to generate the report.
                ERObjectsFactory::createFormatMappingRunByFormatMappingId(formatMappingId, DefaultExportedFileName)
                    .withParameter(parameters)
                    .withFileDestination(_contract.getFileDestination())
                    .run();
            }
            catch
            {
                // An error occurred while exporting data.
                error("@SYP4861341");
            }
        }
        else
        {
            // There is no data available.
            info("@SYS300117");
        }
    }
}
```

## <a name="modify-the-source-code"></a>Breyta upprunakóðanum

1. Í Visual Studio-verkinu skal bæta við nýjum klasa (`AssetRollForwardDestination` í þessu dæmi) og skrifa kóða til að innleiða sérstilltan viðtökustað fyrir skýrslurnar **Framlenging eigna** sem eru myndaðar.

    - `new()`-aðferðin er hönnuð til að sækja upprunalegan viðtökustað rafrænnar skýrslugerðar og færibreytu forrits sem er stýrt af reglu sem tilgreinir sérstillta staðsetningu þar sem geyma á myndaðar skýrslur. Í þessu dæmi er sérstillta staðsetningin heitið á möppu staðbundins skráakerfis á þjóninum sem keyrir AOS-þjónustu.
    - Aðferðin `saveFile()` er hönnuð til að vista myndað skjal í möppu staðbundins skráakerfis á þjóninum sem keyrir AOS-þjónustuna.

    ```xpp
    using Microsoft.Dynamics365.LocalizationFramework;

    /// <summary>
    /// Destination class for <c>AssetRollForwardDestinationFactory</c> that stores a generated report.
    /// </summary>
    public class AssetRollForwardDestination implements ERIFileDestination
    {
        private ERIFileDestination originDestination;
        private str TargetFolder;

        /// <summary>
        /// Creates a stream for new file.
        /// </summary>
        /// <param name = "_fileName">Name of a new file.</param>
        /// <returns>Stream for new file.</returns>
        public System.IO.Stream newFileStream(System.String _fileName)
        {
            return originDestination.newFileStream(_fileName);
        }

        /// <summary>
        /// Saves file in destination.
        /// </summary>
        /// <param name = "_stream">A stream to save.</param>
        /// <param name = "_fileName">A file name.</param>
        /// <returns>Saved stream.</returns>
        public System.IO.Stream saveFile(System.IO.Stream _stream, System.String _fileName)
        {
            _stream.Seek(0, System.IO.SeekOrigin::Begin);
            using (var localStream = System.IO.File::OpenWrite(TargetFolder + _fileName))
            {
                _stream.CopyTo(localStream);
            }
            return _stream;
        }

        /// <summary>
        /// Constructs destination for fixed asset roll forward report.
        /// </summary>
        /// <param name = "_originDestination">The original destination.</param>
        /// <param name = "_TargetFoder">The folder to store a report that's being created.</param>
        /// <returns>The fixed asset roll forward destination.</returns>
        public static AssetRollForwardDestination construct(ERIFileDestination _originDestination, str _TargetFoder)
        {
            return new AssetRollForwardDestination(_originDestination, _TargetFoder);
        }

        protected void new(ERIFileDestination _originDestination, str _TargetFoder)
        {
            originDestination = _originDestination;
            TargetFolder = _TargetFoder;
        }
    }
    ```

2. Í Visual Studio-verkinu skal bæta við nýjum klasa (`AssetRollForwardDestinationFactory` í þessu dæmi) og skrifa kóða til að setja upp sérstilltan viðtökustað verksmiðju sem úthlutar stofnun viðtökustaðar á sjálfgefna staðsetningu verksmiðju, og til að sameina skáarstaðsetningu við þína eigin staðsetningu.

    ```xpp
    using Microsoft.Dynamics365.LocalizationFramework;
    using Microsoft.Dynamics365.LocalizationFramework.Format.FileGeneration;

    /// <summary>
    /// Destination factory for using <c>AssetRollForwardDestinationFactory</c>.
    /// </summary>
    public class AssetRollForwardDestinationFactory implements ERIFileDestinationFactory, ERIFileDestinationFactoryPostProcessor
    {
        private ERIFileDestinationFactory originDestinationFactory;
        private str TargetFolder;

        /// <summary>
        /// Creates file destination for print management.
        /// </summary>
        /// <param name = "_fileDestination">A default file destination.</param>
        /// <param name = "_identification">An identification strategy.</param>
        /// <param name = "_rootContext">A root context.</param>
        /// <param name = "_root">A root element.</param>
        /// <returns>A file destination.</returns>
        public ERIDataDrivenFileDestination createPrintMgmtDestination(
            ERIFileDestination _fileDestination,
            ERIObjectIdentificationStrategy _identification,
            ERTextFormatDataContext _rootContext,
            ERTextFormatIFileComponent _root)
        {
            ERIDataDrivenFileDestination dataDrivenDestination = originDestinationFactory.createPrintMgmtDestination(
                _fileDestination,
                _identification,
                _rootContext,
                _root);

            IFileDestinationHost fileDestinationHost = dataDrivenDestination as IFileDestinationHost;
            if (fileDestinationHost)
            {
                fileDestinationHost.FileDestination = AssetRollForwardDestination::construct(
                    fileDestinationHost.get_FileDestination(),
                    TargetFolder);
            }

            return dataDrivenDestination;
        }

        /// <summary>
        /// Constructs the fixed asset roll forward destination factory.
        /// </summary>
        /// <param name = "_originDestinationFactory">The original destination.</param>
        /// <param name = "_TargetFolder">The string containing a folder name that corresponds to the report, that's being created.</param>
        /// <returns>The destination factory for the fixed asset roll forward report.</returns>
        public static AssetRollForwardDestinationFactory construct(ERIFileDestinationFactory _originDestinationFactory, str _TargetFolder)
        {
            AssetRollForwardDestinationFactory destinationFactory = new AssetRollForwardDestinationFactory(_originDestinationFactory, _TargetFolder);

            ERIFileDestinationFactoryPostProcessorsHost factoryPostProcessing = ERCast::asObject(destinationFactory.originDestinationFactory) as ERIFileDestinationFactoryPostProcessorsHost;

            if (factoryPostProcessing)
            {
                factoryPostProcessing.addDestinationPostProcessor(destinationFactory);
            }
            return destinationFactory;
        }

        public ERIFileDestination processDestinationAfterCreation(ERIFileDestination _sourceDestination)
        {
            return AssetRollForwardDestination::construct(_sourceDestination, TargetFolder);
        }

        protected void new(ERIFileDestinationFactory _originDestinationFactory, str _TargetFolder)
        {
            originDestinationFactory = _originDestinationFactory;
            TargetFolder = _TargetFolder;
        }
    }
    ```

3. Breytið fyrirliggjandi `AssetRollForwardService`-klasa og skrifið kóða til að setja upp sérstillta verksmiðjustaðsetningu fyrir keyrslu skýrslunnar. Takið eftir því að þegar sérstillt verksmiðjustaðsetning er búin til, er forritsstýrða færibreytan sem tilgreinir möppu viðtökustaðar keyrð í gegn. Á þennan hátt er þessi mappa viðtökustaðar notuð til að geyma myndaðar skrár.

    > [!NOTE] 
    > Ganga skal úr skugga um að tilgreinda mappan (**C:\\0** í þessu dæmi) sé til staðar í staðbundnu skráakerfi netþjónsins sem keyrir AOS-þjónustuna. Annars verður undantekningin [DirectoryNotFoundException](/dotnet/api/system.io.directorynotfoundexception) notuð við keyrslu.

    ```xpp
    using Microsoft.Dynamics365.LocalizationFramework;
    /// <summary>
    /// The electronic reporting service class for fixed asset roll forward report
    /// </summary>
    class AssetRollForwardService extends SysOperationServiceBase
    {
        public const str ERFormatModelName = 'Fixed assets';
        public const str ERModelDataSourceName = 'model';
        public const str DefaultExportedFileName = 'AssetRollForward';

        /// <summary>
        /// Generates report by general electronic reporting
        /// </summary>
        /// <param name = "_contract">The Asset Period Statement contract</param>
        public void generateReportByGER(AssetRollForwardContract _contract)
        {
            ERFormatMappingId   formatMappingId;
            AssetRollForwardDP  dataProvider;
            AssetRollForwardTmp assetRollForwardTmp;
            Query               query;

            query = new Query(SysOperationHelper::base64Decode(_contract.parmQuery()));
            dataProvider = AssetRollForwardDP::construct();
            formatMappingId = _contract.parmFormatMapping();
            assetRollForwardTmp = dataProvider.getAssetRollForwardTmp(_contract, query);

            if (assetRollForwardTmp)
            {
                try
                {
                    ERIModelDefinitionParamsAction parameters = new ERModelDefinitionParamsUIActionComposite()
                        .add(new ERModelDefinitionDatabaseContext().addTemporaryTable(assetRollForwardTmp))
                        .add(new ERModelDefinitionObjectParameterAction(ERModelDataSourceName, 'MyParameters', _contract, true));

                    // Call ER to generate the report.
                    ERIFormatMappingRun formatMappingRun = ERObjectsFactory::createFormatMappingRunByFormatMappingId(formatMappingId, DefaultExportedFileName);
                    formatMappingRun.withParameter(parameters);
                    formatMappingRun.withFileDestination(_contract.getFileDestination());

                    ERIFileDestinationFactoryHost factoryHost = ERCast::asObject(formatMappingRun) as ERIFileDestinationFactoryHost;
                    if (factoryHost)
                    {
                        ERIFileDestinationFactory fileDestinationFactory = factoryHost.getFileDestinationFactory();
                        factoryHost.setFileDestinationFactory(AssetRollForwardDestinationFactory::construct(fileDestinationFactory, @'c:\0\'));
                        formatMappingRun.run();
                    }
                }
                catch
                {
                    // An error occurred while exporting data.
                    error("@SYP4861341");
                }
            }
            else
            {
                // There is no data available.
                info("@SYS300117");
            }
        }
    }
    ```

4. Endursmíðaðu verkefnið þitt.

## <a name="re-run-the-fixed-asset-roll-forward-report"></a>Keyra aftur skýrslu um framlengingu eigna

1. Farið í **Eignir** \> **Fyrirspurnir og skýrslur** \> **Færsluskýrslur** \> **Framlenging eigna**.
2. Í reitinn **Frá dagsetningu** skal slá inn **1/1/2017**.
3. Í reitinn **Til dagsetningar** skal slá inn **31/1/2017**.
4. Í **Gjaldmiðilsreitnum** skal velja **Bókhaldsgjaldmiðil**.
5. Í reitnum **Sniðsvörpun** skal velja **Framlenging eigna**.
6. Veljið **Í lagi**.
7. Skoðið staðbundna **C:\\0** möppu til að finna myndaða skrá.

> [!NOTE]
> Vegna þess að `originDestination`-hluturinn er ekki notaður í `AssetRollForwardDestination`-hlutnum í þessu dæmi, verða skilgreiningarnar fyrir [viðtökustaði](electronic-reporting-destinations.md) rafræns skýrslugerðarsniðs hunsaðar við keyrslu.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Áfangastaðir fyrir rafræna skýrslugerð](electronic-reporting-destinations.md)
- [Heimasíða stækkunarhæfni](../extensibility/extensibility-home-page.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]