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
ms.openlocfilehash: bd979bf5369b6878caaee82fc9c6a40d363cc165
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/13/2021
ms.locfileid: "5894149"
---
# <a name="specify-custom-storage-locations-for-generated-documents"></a><span data-ttu-id="a07e7-103">Tilgreina sérsniðinn geymslustað fyrir mynduð skjöl</span><span class="sxs-lookup"><span data-stu-id="a07e7-103">Specify custom storage locations for generated documents</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="a07e7-104">Forritunarviðmót forritsins (API) fyrir ramma rafrænnar skýrslugerðar gerir þér kleift að stækka listann yfir geymslustaði fyrir skjöl sem snið rafrænnar skýrslugerðar myndar.</span><span class="sxs-lookup"><span data-stu-id="a07e7-104">The application programming interface (API) of the Electronic reporting (ER) framework lets you extend the list of storage locations for documents that ER formats generate.</span></span> <span data-ttu-id="a07e7-105">Þetta efnisatriði útskýrir hvernig á að bæta við sérstilltum geymslustað fyrir mynduð skjöl með því að úthluta verkinu fyrir stofnun viðtökustaða rafrænnar skýrslugerðar í sjálfgefinni staðsetningu verksmiðju og síðan innleiða sérstilltan klasa sem er með sína eigin reglu um endastað.</span><span class="sxs-lookup"><span data-stu-id="a07e7-105">This topic explains how to add a custom storage location for generated documents by delegating the task of creating ER destinations to the default destination factory and then implementing a custom class that has its own destination logic.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a07e7-106">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="a07e7-106">Prerequisites</span></span>

<span data-ttu-id="a07e7-107">Setja upp grannfræði sem styður samfellda smíði.</span><span class="sxs-lookup"><span data-stu-id="a07e7-107">Deploy a topology that supports continuous build.</span></span> <span data-ttu-id="a07e7-108">Nánari upplýsingar er að finna [Setja upp grannfræði sem styður samfellda smíði og sjálfvirkni prófunar](/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation).</span><span class="sxs-lookup"><span data-stu-id="a07e7-108">For more information, see [Deploy topologies that support continuous build and test automation](/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation).</span></span> <span data-ttu-id="a07e7-109">Það þarf að hafa aðgang að þessari grannfræði fyrir eitt af eftirfarandi hlutverkum:</span><span class="sxs-lookup"><span data-stu-id="a07e7-109">You must have access to this topology for one of the following roles:</span></span>

- <span data-ttu-id="a07e7-110">Þróunaraðili rafrænnar skýrslulausnar</span><span class="sxs-lookup"><span data-stu-id="a07e7-110">Electronic reporting developer</span></span>
- <span data-ttu-id="a07e7-111">Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="a07e7-111">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="a07e7-112">Kerfisstjóri</span><span class="sxs-lookup"><span data-stu-id="a07e7-112">System administrator</span></span>

<span data-ttu-id="a07e7-113">Þú verður einnig að hafa aðgang að þróunarumhverfi fyrir þessa grannfræði.</span><span class="sxs-lookup"><span data-stu-id="a07e7-113">You must also have access to the development environment for this topology.</span></span>

<span data-ttu-id="a07e7-114">Hægt er að ljúka verkunum í þessu efnisatriði í fyrirtækinu **USMF**.</span><span class="sxs-lookup"><span data-stu-id="a07e7-114">All the tasks in this topic can be completed in the **USMF** company.</span></span>

## <a name="import-the-fixed-asset-roll-forward-er-format"></a><span data-ttu-id="a07e7-115">Flytja inn rafrænt skýrslugerðarsnið fyrir framlengingu eignar</span><span class="sxs-lookup"><span data-stu-id="a07e7-115">Import the Fixed asset roll forward ER format</span></span>

<span data-ttu-id="a07e7-116">Til að mynda skjölin sem ætlunin er að bæta sérstilltum geymslustað við, skal [flytja inn](er-download-configurations-global-repo.md) skilgreininguna **Framlenging eigna** fyrir rafrænt skýrslugerðarsnið í núverandi grannfræði.</span><span class="sxs-lookup"><span data-stu-id="a07e7-116">To generate the documents that you plan to add a custom storage location for, [import](er-download-configurations-global-repo.md) the **Fixed asset roll forward** ER format configuration into the current topology.</span></span>

![Síðan Skilgreiningagagnasafn](./media/er-custom-storage-generated-files-import-format.png)

## <a name="run-the-fixed-asset-roll-forward-report"></a><span data-ttu-id="a07e7-118">Keyra skýrsla fyrir framlengingu eigna</span><span class="sxs-lookup"><span data-stu-id="a07e7-118">Run the Fixed asset roll forward report</span></span>

1. <span data-ttu-id="a07e7-119">Farið í **Eignir** \> **Fyrirspurnir og skýrslur** \> **Færsluskýrslur** \> **Framlenging eigna**.</span><span class="sxs-lookup"><span data-stu-id="a07e7-119">Go to **Fixed assets** \> **Inquiries and reports** \> **Transaction reports** \> **Fixed asset roll forward**.</span></span>
2. <span data-ttu-id="a07e7-120">Í reitinn **Frá dagsetningu** skal slá inn **1/1/2017** (1. janúar 2017).</span><span class="sxs-lookup"><span data-stu-id="a07e7-120">In the **From date** field, enter **1/1/2017** (January 1, 2017).</span></span>
3. <span data-ttu-id="a07e7-121">Í reitinn **Til dagsetningar** skal slá inn **31/1/2017** (31. janúar 2017).</span><span class="sxs-lookup"><span data-stu-id="a07e7-121">In the **To date** field, enter **1/31/2017** (January 31, 2017).</span></span>
4. <span data-ttu-id="a07e7-122">Í **Gjaldmiðilsreitnum** skal velja **Bókhaldsgjaldmiðil**.</span><span class="sxs-lookup"><span data-stu-id="a07e7-122">In the **Currency field**, select **Accounting currency**.</span></span>
5. <span data-ttu-id="a07e7-123">Í reitnum **Sniðsvörpun** skal velja **Framlenging eigna**.</span><span class="sxs-lookup"><span data-stu-id="a07e7-123">In the **Format mapping** field, select **Fixed asset roll forward**.</span></span>
6. <span data-ttu-id="a07e7-124">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="a07e7-124">Select **OK**.</span></span>

![Keyrslugluggi fyrir skýrslu um framlengingu eigna](./media/er-custom-storage-generated-files-runtime-dialog.png)

<span data-ttu-id="a07e7-126">Í Microsoft Excel skal fara yfir skjal á útleið sem er myndað og tilbúið til niðurhals.</span><span class="sxs-lookup"><span data-stu-id="a07e7-126">In Microsoft Excel, review the outbound document that is generated and available for download.</span></span> <span data-ttu-id="a07e7-127">Þessi hegðun er [sjálfgefin hegðun](electronic-reporting-destinations.md#default-behavior) fyrir snið rafrænnar skýrslugerðar þar sem engir [viðtökustaðir](electronic-reporting-destinations.md) eru skilgreindir og er keyrt í gagnvirkri stillingu.</span><span class="sxs-lookup"><span data-stu-id="a07e7-127">This behavior is the [default behavior](electronic-reporting-destinations.md#default-behavior) for an ER format that no [destinations](electronic-reporting-destinations.md) are configured for, and that is running in interactive mode.</span></span>

## <a name="review-the-source-code"></a><span data-ttu-id="a07e7-128">Skoða upprunakóðann</span><span class="sxs-lookup"><span data-stu-id="a07e7-128">Review the source code</span></span>

<span data-ttu-id="a07e7-129">Yfirfarið kóða `generateReportByGER()`-aðferðarinnar fyrir `AssetRollForwardService`-klasann.</span><span class="sxs-lookup"><span data-stu-id="a07e7-129">Review the code of the `generateReportByGER()` method of the `AssetRollForwardService` class.</span></span> <span data-ttu-id="a07e7-130">Takið eftir því að `Run()`-aðferðin er notuð til að kalla á ramma rafrænnar skýrslugerðar og mynda skýrsluna **Framlenging eigna**.</span><span class="sxs-lookup"><span data-stu-id="a07e7-130">Notice that the `Run()` method is used to call the ER framework and generate the **Fixed asset roll forward** report.</span></span>

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

## <a name="modify-the-source-code"></a><span data-ttu-id="a07e7-131">Breyta upprunakóðanum</span><span class="sxs-lookup"><span data-stu-id="a07e7-131">Modify the source code</span></span>

1. <span data-ttu-id="a07e7-132">Í Visual Studio-verkinu skal bæta við nýjum klasa (`AssetRollForwardDestination` í þessu dæmi) og skrifa kóða til að innleiða sérstilltan viðtökustað fyrir skýrslurnar **Framlenging eigna** sem eru myndaðar.</span><span class="sxs-lookup"><span data-stu-id="a07e7-132">In your Visual Studio project, add a new class (`AssetRollForwardDestination` in this example), and write code to implement your custom destination for **Fixed asset roll forward** reports that are generated.</span></span>

    - <span data-ttu-id="a07e7-133">`new()`-aðferðin er hönnuð til að sækja upprunalegan viðtökustað rafrænnar skýrslugerðar og færibreytu forrits sem er stýrt af reglu sem tilgreinir sérstillta staðsetningu þar sem geyma á myndaðar skýrslur.</span><span class="sxs-lookup"><span data-stu-id="a07e7-133">The `new()` method is designed to get the original ER destination object and the application logic–driven parameter that specifies the custom location where generated reports should be stored.</span></span> <span data-ttu-id="a07e7-134">Í þessu dæmi er sérstillta staðsetningin heitið á möppu staðbundins skráakerfis á þjóninum sem keyrir AOS-þjónustu.</span><span class="sxs-lookup"><span data-stu-id="a07e7-134">In this example, the custom location is the name of a folder of the local file system of the server that runs the Application Object Server (AOS) service.</span></span>
    - <span data-ttu-id="a07e7-135">Aðferðin `saveFile()` er hönnuð til að vista myndað skjal í möppu staðbundins skráakerfis á þjóninum sem keyrir AOS-þjónustuna.</span><span class="sxs-lookup"><span data-stu-id="a07e7-135">The `saveFile()` method is designed to save a generated document to a folder of the local file system of the server that runs the AOS service.</span></span>

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

2. <span data-ttu-id="a07e7-136">Í Visual Studio-verkinu skal bæta við nýjum klasa (`AssetRollForwardDestinationFactory` í þessu dæmi) og skrifa kóða til að setja upp sérstilltan viðtökustað verksmiðju sem úthlutar stofnun viðtökustaðar á sjálfgefna staðsetningu verksmiðju, og til að sameina skáarstaðsetningu við þína eigin staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="a07e7-136">In your Visual Studio project, add a new class (`AssetRollForwardDestinationFactory` in this example), and write code to set up a custom destination factory that delegates the creation of a destination to the default destination factory, and to wrap a file destination with your own destination.</span></span>

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

3. <span data-ttu-id="a07e7-137">Breytið fyrirliggjandi `AssetRollForwardService`-klasa og skrifið kóða til að setja upp sérstillta verksmiðjustaðsetningu fyrir keyrslu skýrslunnar.</span><span class="sxs-lookup"><span data-stu-id="a07e7-137">Modify the existing `AssetRollForwardService` class, and write code to set up a custom destination factory for the report runner.</span></span> <span data-ttu-id="a07e7-138">Takið eftir því að þegar sérstillt verksmiðjustaðsetning er búin til, er forritsstýrða færibreytan sem tilgreinir möppu viðtökustaðar keyrð í gegn.</span><span class="sxs-lookup"><span data-stu-id="a07e7-138">Notice that when a custom destination factory is constructed, the application-driven parameter that specifies a target folder is passed.</span></span> <span data-ttu-id="a07e7-139">Á þennan hátt er þessi mappa viðtökustaðar notuð til að geyma myndaðar skrár.</span><span class="sxs-lookup"><span data-stu-id="a07e7-139">In this way, that target folder is used to store generated files.</span></span>

    > [!NOTE] 
    > <span data-ttu-id="a07e7-140">Ganga skal úr skugga um að tilgreinda mappan (**C:\\0** í þessu dæmi) sé til staðar í staðbundnu skráakerfi netþjónsins sem keyrir AOS-þjónustuna.</span><span class="sxs-lookup"><span data-stu-id="a07e7-140">Make sure that the specified folder (**c:\\0** in this example) is present in the local file system of the server that runs the AOS service.</span></span> <span data-ttu-id="a07e7-141">Annars verður undantekningin [DirectoryNotFoundException](/dotnet/api/system.io.directorynotfoundexception?view=netcore-3.1) notuð við keyrslu.</span><span class="sxs-lookup"><span data-stu-id="a07e7-141">Otherwise, a [DirectoryNotFoundException](/dotnet/api/system.io.directorynotfoundexception?view=netcore-3.1) exception will be thrown at runtime.</span></span>

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

4. <span data-ttu-id="a07e7-142">Endursmíðaðu verkefnið þitt.</span><span class="sxs-lookup"><span data-stu-id="a07e7-142">Rebuild your project.</span></span>

## <a name="re-run-the-fixed-asset-roll-forward-report"></a><span data-ttu-id="a07e7-143">Keyra aftur skýrslu um framlengingu eigna</span><span class="sxs-lookup"><span data-stu-id="a07e7-143">Re-run the Fixed asset roll forward report</span></span>

1. <span data-ttu-id="a07e7-144">Farið í **Eignir** \> **Fyrirspurnir og skýrslur** \> **Færsluskýrslur** \> **Framlenging eigna**.</span><span class="sxs-lookup"><span data-stu-id="a07e7-144">Go to **Fixed assets** \> **Inquiries and reports** \> **Transaction reports** \> **Fixed asset roll forward**.</span></span>
2. <span data-ttu-id="a07e7-145">Í reitinn **Frá dagsetningu** skal slá inn **1/1/2017**.</span><span class="sxs-lookup"><span data-stu-id="a07e7-145">In the **From date** field, enter **1/1/2017**.</span></span>
3. <span data-ttu-id="a07e7-146">Í reitinn **Til dagsetningar** skal slá inn **31/1/2017**.</span><span class="sxs-lookup"><span data-stu-id="a07e7-146">In the **To date** field, enter **1/31/2017**.</span></span>
4. <span data-ttu-id="a07e7-147">Í **Gjaldmiðilsreitnum** skal velja **Bókhaldsgjaldmiðil**.</span><span class="sxs-lookup"><span data-stu-id="a07e7-147">In the **Currency field**, select **Accounting currency**.</span></span>
5. <span data-ttu-id="a07e7-148">Í reitnum **Sniðsvörpun** skal velja **Framlenging eigna**.</span><span class="sxs-lookup"><span data-stu-id="a07e7-148">In the **Format mapping** field, select **Fixed asset roll forward**.</span></span>
6. <span data-ttu-id="a07e7-149">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="a07e7-149">Select **OK**.</span></span>
7. <span data-ttu-id="a07e7-150">Skoðið staðbundna **C:\\0** möppu til að finna myndaða skrá.</span><span class="sxs-lookup"><span data-stu-id="a07e7-150">Browse the local **C:\\0** folder to find the generated file.</span></span>

> [!NOTE]
> <span data-ttu-id="a07e7-151">Vegna þess að `originDestination`-hluturinn er ekki notaður í `AssetRollForwardDestination`-hlutnum í þessu dæmi, verða skilgreiningarnar fyrir [viðtökustaði](electronic-reporting-destinations.md) rafræns skýrslugerðarsniðs hunsaðar við keyrslu.</span><span class="sxs-lookup"><span data-stu-id="a07e7-151">Because the `originDestination` object isn't used in the `AssetRollForwardDestination` object in this example, the configurations for the ER format [destinations](electronic-reporting-destinations.md) will be ignored at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a07e7-152">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="a07e7-152">Additional resources</span></span>

- [<span data-ttu-id="a07e7-153">Áfangastaðir fyrir rafræna skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="a07e7-153">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="a07e7-154">Heimasíða stækkunarhæfni</span><span class="sxs-lookup"><span data-stu-id="a07e7-154">Extensibility home page</span></span>](../extensibility/extensibility-home-page.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]