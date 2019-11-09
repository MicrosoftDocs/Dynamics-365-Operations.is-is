---
title: Afritunargeymsla ER-sniðmáta
description: Þetta efni útskýrir hvernig á að nota varabúnaðargeymslu rafrænnar skýrslugerðar (ER) til að endurheimta sniðmát.
author: NickSelin
manager: AnnBe
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 27621
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-08-13
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 932ba44b4223bf9c9d93ffb19e17f6e57bb303b5
ms.sourcegitcommit: bbb64b3475eef155b3f9d1bdc440545da8a7182f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/04/2019
ms.locfileid: "2553092"
---
# <a name="backup-storage-of-er-templates"></a><span data-ttu-id="91feb-103">Afritunargeymsla ER-sniðmáta</span><span class="sxs-lookup"><span data-stu-id="91feb-103">Backup storage of ER templates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="91feb-104">[Rammi rafrænnar skýrslugerðar (ER)](general-electronic-reporting.md) gerir fyrirtækjanotendum kleift að skilgreina snið fyrir skjöl á útleið í samræmi við lagaskilyrði mismunandi landa og svæða.</span><span class="sxs-lookup"><span data-stu-id="91feb-104">The [Electronic reporting (ER) framework](general-electronic-reporting.md) lets business users configure formats for outbound documents according to the legal requirements of various countries and regions.</span></span> <span data-ttu-id="91feb-105">Stillt ER-snið geta notað fyrirfram skilgreind sniðmát til að búa til útgönguskjöl á ýmsum sniðum, svo sem Microsoft Excel vinnubækur, Microsoft Word skjöl, eða PDF-skjöl.</span><span class="sxs-lookup"><span data-stu-id="91feb-105">Configured ER formats can use predefined templates to generate outbound documents in various formats, such as Microsoft Excel workbooks, Microsoft Word documents, or PDF documents.</span></span> <span data-ttu-id="91feb-106">Sniðmátin eru fyllt með gögnum sem skilgreint gagnaflæði fyrir mynduð skjöl krefst.</span><span class="sxs-lookup"><span data-stu-id="91feb-106">The templates are filled with data that the configured dataflow for generated documents requires.</span></span>

<span data-ttu-id="91feb-107">Hægt er að birta hvert skilgreint snið sem hluta af ER-lausn.</span><span class="sxs-lookup"><span data-stu-id="91feb-107">Each configured format can be published as part of an ER solution.</span></span> <span data-ttu-id="91feb-108">Hægt er að flytja út allar lausnir frá einu tilviki Finance and Operations og flytja inn í annað tilvik.</span><span class="sxs-lookup"><span data-stu-id="91feb-108">Each ER solution can be exported from one instance of Finance and Operations and imported into another instance.</span></span>

<span data-ttu-id="91feb-109">ER-ramminn notar [Ramma skjalastjórnunar](../../fin-ops/organization-administration/configure-document-management.md) til að geyma nauðsynleg sniðmát fyrir núverandi tilviki Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="91feb-109">The ER framework uses the [Document management framework](../../fin-ops/organization-administration/configure-document-management.md) to keep the required templates for the current Finance and Operations instance.</span></span> <span data-ttu-id="91feb-110">Það fer eftir stillingum ER-ramma, Microsoft Azure Blob-geymslu eða Microsoft SharePoint hvort hægt er að velja möppu sem aðal geymslupláss fyrir sniðmát.</span><span class="sxs-lookup"><span data-stu-id="91feb-110">Depending on the settings of the ER framework, Microsoft Azure Blob storage or a Microsoft SharePoint folder can be selected as the physical primary storage location for templates.</span></span> <span data-ttu-id="91feb-111">(Sjá frekari upplýsingar [Stilla ER ramma](electronic-reporting-er-configure-parameters.md).) DocuValue taflan hefur einstaka skrá fyrir hvert sniðmát.</span><span class="sxs-lookup"><span data-stu-id="91feb-111">(For more information, see [Configure the ER framework](electronic-reporting-er-configure-parameters.md).) The DocuValue table holds an individual record for each template.</span></span> <span data-ttu-id="91feb-112">Í hverri skrá geymir reiturinn **AccessInformation** slóð sniðmátaskrár sem er staðsett á skilgreindum geymslustað.</span><span class="sxs-lookup"><span data-stu-id="91feb-112">In each record, the **AccessInformation** field stores the path of a template file that is located in the configured storage location.</span></span>

<span data-ttu-id="91feb-113">Þegar þú hefur umsjón með tilvikum Finance and Operations gætirðu ákveðið að flytja núverandi tilvik yfir á annan stað.</span><span class="sxs-lookup"><span data-stu-id="91feb-113">When you manage your Finance and Operations instances, you might decide to migrate the current instance to another location.</span></span> <span data-ttu-id="91feb-114">Til dæmis gætirðu flutt framleiðslutilvikið í nýtt sandkassaumhverfi.</span><span class="sxs-lookup"><span data-stu-id="91feb-114">For example, you might migrate your production instance to a new sandbox environment.</span></span> <span data-ttu-id="91feb-115">Ef þú stillir ER-ramma til að geyma sniðmát í Blob-geymslu, vísar DocuValue-taflan í nýja sandkassaumhverfi til tilviks Blob-geymslu í framleiðsluumhverfi.</span><span class="sxs-lookup"><span data-stu-id="91feb-115">If you configured the ER framework to store templates in Blob storage, the DocuValue table in the new sandbox environment refers to the instance of Blob storage in the production environment.</span></span> <span data-ttu-id="91feb-116">Hins vegar er ekki hægt að fá aðgang að þessu tilviki úr sandkassanumhverfinu, vegna þess að flutningsferlið styður ekki flutning á gripum í Blob-geymslu.</span><span class="sxs-lookup"><span data-stu-id="91feb-116">However, this instance can't be accessed from the sandbox environment, because the migration process doesn't support the migration of artifacts in Blob storage.</span></span> <span data-ttu-id="91feb-117">Þess vegna, ef þú reynir að keyra ER-snið sem notar sniðmát til að búa til viðskiptaskjöl, kemur undantekning fyrir, og þér er tilkynnt um það sniðmát sem vantar.</span><span class="sxs-lookup"><span data-stu-id="91feb-117">Therefore, if you try to run an ER format that uses a template to generate business documents, an exception occurs, and you're notified about the missing template.</span></span> <span data-ttu-id="91feb-118">Þér er einnig leiðbeint um að nota ER-hreinsunartólið til að eyða og flytja síðan aftur upp skilgreiningu ER-sniðsins sem inniheldur sniðmátið.</span><span class="sxs-lookup"><span data-stu-id="91feb-118">You're also guided to use the ER cleanup tool to delete and then re-import the ER format configuration that contains the template.</span></span> <span data-ttu-id="91feb-119">Vegna þess að þú gætir haft nokkrar stillingar á ER-sniði, getur þetta ferli verið tímafrekt.</span><span class="sxs-lookup"><span data-stu-id="91feb-119">Because you might have several ER format configurations, this process can be time consuming.</span></span>

<span data-ttu-id="91feb-120">Afritunargeymsla ER-sniðmátsaðgerðar getur hjálpað þér að búa til sniðmát þannig að þau eru alltaf tiltæk til að búa til viðskiptaskjöl.</span><span class="sxs-lookup"><span data-stu-id="91feb-120">The Backup storage of ER templates feature can help you make your templates so that they are always available to generate business documents.</span></span>

> [!NOTE]
> <span data-ttu-id="91feb-121">Þessa aðgerð er aðeins hægt að nota þegar Blob geymsla hefur verið valin sem raunverulegt geymslupláss fyrir ER sniðmát.</span><span class="sxs-lookup"><span data-stu-id="91feb-121">This feature can be used only when Blob storage has been selected as the physical storage location for ER templates.</span></span>

<span data-ttu-id="91feb-122">Fyrir þennan möguleika er hvert sniðmát nýrrar stillingar ER snið í núverandi umhverfi sjálfkrafa vistað á afritunargeymsluplássi fyrir sniðmát (ERDocuDatabaseStorage gagnagrunnstaflan) þegar eftirfarandi tilvik eiga sér stað:</span><span class="sxs-lookup"><span data-stu-id="91feb-122">For this feature, every template of a new ER format configuration in the current environment is automatically saved to the backup storage location for templates (the ERDocuDatabaseStorage database table) when the following events occur:</span></span>

- <span data-ttu-id="91feb-123">Þú flytur inn nýja ER snið stillingu sem inniheldur sniðmát.</span><span class="sxs-lookup"><span data-stu-id="91feb-123">You import a new ER format configuration that contains a template.</span></span>
- <span data-ttu-id="91feb-124">Þú klárar drög að útgáfu ER sniðstillingar sem inniheldur sniðmát.</span><span class="sxs-lookup"><span data-stu-id="91feb-124">You complete the draft version of an ER format configuration that contains a template.</span></span>

<span data-ttu-id="91feb-125">Afritun af sniðmátum er flutt yfir í nýtt tilvik Finance and Operations sem hluti af gagnagrunninum.</span><span class="sxs-lookup"><span data-stu-id="91feb-125">Backup copies of templates are migrated to a new instance of Finance and Operations as part of the application database.</span></span>

<span data-ttu-id="91feb-126">Ef sniðmáts með ER sniði er krafist til að búa til skjöl á útleið, til að vinna úr greiðslum lánardrottins, þ.m.t. myndun greiðsluráðgjafar og eftirlitsskýrslna, til dæmis, en nauðsynleg sniðmát er ekki að finna á aðalgeymslustaðnum, gerast eftirfarandi tilvik:</span><span class="sxs-lookup"><span data-stu-id="91feb-126">If a template of an ER format is required for generation of outbound documents, to process vendor payments including generation of payment advice and control reports, for example, but the required template isn't found in the primary storage location, the following events occur:</span></span>

- <span data-ttu-id="91feb-127">Ef sniðmátið er tiltækt á öryggisafritunargeymslunni er það sjálfkrafa tekið af afritunargeymslustaðnum, endurheimt á aðalgeymsluplássið og notað fyrir núverandi framkvæmd.</span><span class="sxs-lookup"><span data-stu-id="91feb-127">If the template is available in the backup storage location, it is automatically taken from the backup storage location, restored to the primary storage location, and used for the current execution.</span></span>
- <span data-ttu-id="91feb-128">Sérhverjum notanda sem er úthlutað á hlutverkið **Þróunaraðili rafrænnar skýrslulausnar** eða **Kerfisstjóri** er tilkynnt um sniðmátið sem vantar í gegnum aðgerðarstöðina.</span><span class="sxs-lookup"><span data-stu-id="91feb-128">Every user who is assigned to the **Electronic reporting developer** or **System administrator** role is notified about the missing template issue through the Action center.</span></span> <span data-ttu-id="91feb-129">Skilaboðin sem birtast eru háð gildi færibreytunnar **Keyra ferlið sjálfkrafa til að endurheimta brotin sniðmát í runu**:</span><span class="sxs-lookup"><span data-stu-id="91feb-129">The message that appears depends on the value of the **Automatically run the procedure of restoring the broken templates in batch** parameter:</span></span>

    - <span data-ttu-id="91feb-130">Ef þessi færibreyta er stillt á **Slökkt** mæla skilaboðin með því að þú hefjir runuferlið til að laga sjálfkrafa svipuð vandamál fyrir önnur ER-sniðmát fyrir skilgreiningarsnið.</span><span class="sxs-lookup"><span data-stu-id="91feb-130">If this parameter is set to **Off**, the message recommends that you start the batch process to automatically fix similar issues for other ER format configuration templates.</span></span> <span data-ttu-id="91feb-131">Skilaboðin innihalda tengil sem þú getur notað til að hefja runuferlið.</span><span class="sxs-lookup"><span data-stu-id="91feb-131">The message includes a link that you can use to start the batch process.</span></span>
    - <span data-ttu-id="91feb-132">Ef þessi færibreyta er stillt á **Kveikt** tilkynna skilaboðin þér að uppgötvast hafi vandamál vegna sniðmáts sem vantar og að ný runuvinnsla, **Endurheimta biluð sniðmát úr innri afritun gagnagrunnsins**, hefur sjálfkrafa verið áætluð.</span><span class="sxs-lookup"><span data-stu-id="91feb-132">If this parameter is set to **On**, the message notifies you that a missing templates issue has been discovered, and that a new batch process, **Restore broken templates from internal database backup**, has been automatically scheduled.</span></span> <span data-ttu-id="91feb-133">Þessi runuvinnsla mun sjálfkrafa laga svipuð vandamál fyrir önnur sniðmát.</span><span class="sxs-lookup"><span data-stu-id="91feb-133">This batch process will automatically fix similar issues for other templates.</span></span>

<span data-ttu-id="91feb-134">Til að setja upp færibreytuna **Keyra ferlið sjálfkrafa til að endurheimta brotin sniðmát í runu** skal ljúka eftirfarandi skrefum:</span><span class="sxs-lookup"><span data-stu-id="91feb-134">To set up the he **Automatically run the procedure of restoring the broken templates in batch** parameter, complete the following steps:</span></span>

1. <span data-ttu-id="91feb-135">Í Finance and Operations skal opna **Fyrirtækisstjórnun \> Rafræn skýrslugerð \> Skilgreiningarsíða**.</span><span class="sxs-lookup"><span data-stu-id="91feb-135">In Finance and Operations, open the **Organization administration \> Electronic reporting \> Configurations page**.</span></span>
2. <span data-ttu-id="91feb-136">Á síðunni **Skilgreiningar**, í aðgerðarúðunni, í flipanum **Skilgreiningar**, í flokknum **Ítarlegar stillingar**, skal velja **Færibreytur notanda**.</span><span class="sxs-lookup"><span data-stu-id="91feb-136">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="91feb-137">Í valmyndinni **Færibreytur notanda** stillirðu nauðsynleg gildi fyrir færibreytuna **Keyra ferlið sjálfkrafa til að endurheimta brotin sniðmát í runu**.</span><span class="sxs-lookup"><span data-stu-id="91feb-137">In the **User parameters** dialog box, set the required value for the **Automatically run the procedure of restoring the broken templates in batch** parameter.</span></span>

> [!NOTE]
> <span data-ttu-id="91feb-138">Þessi færibreyta er skilgreind sem notandi forrita og skráð sem fyrirtækjasértæk.</span><span class="sxs-lookup"><span data-stu-id="91feb-138">This parameter is defined as application user and logged company specific.</span></span>

![Skilgreiningarsíða í ER](./media/GER-BackupTemplates-1.png)

<span data-ttu-id="91feb-140">Eftirfarandi mynd sýnir dæmi um skilaboðin sem birtast þegar færibreytan **Keyra ferlið sjálfkrafa til að endurheimta brotin sniðmát í runu** er stillt á **Kveikt**.</span><span class="sxs-lookup"><span data-stu-id="91feb-140">The following illustration shows an example of the message that appears when the **Automatically run the procedure of restoring the broken templates in batch** parameter is set to **On**.</span></span>

![Greiðslubókarsíða lánardrottins](./media/GER-BackupTemplates-2.png)

<span data-ttu-id="91feb-142">Eftirfarandi mynd sýnir runuvinnsluna **Endurheimta biluð sniðmát úr innri afritun gagnagrunnsins** á síðunni **Runuvinnsla**.</span><span class="sxs-lookup"><span data-stu-id="91feb-142">The following illustration shows the **Restore broken templates from internal database backup** batch process on the **Batch job** page.</span></span>

![Síða runuvinnslu](./media/GER-BackupTemplates-3.png)

<span data-ttu-id="91feb-144">Framkvæmdaskrá yfir lokna runuvinnslu **Endurheimta biluð sniðmát úr innri afritun gagnagrunnsins** inniheldur upplýsingar um sniðmát sem hafa verið endurheimt frá varabúnaðargeymslustað yfir á aðalgeymslustað.</span><span class="sxs-lookup"><span data-stu-id="91feb-144">The execution log of the completed **Restore broken templates from internal database backup** batch process includes information about the templates that have been restored from the backup storage location to the primary storage location.</span></span>

![Síða runuvinnslusögu](./media/GER-BackupTemplates-4.png)

<span data-ttu-id="91feb-146">Sjálfgefið er að kveikt er á ferlinu við að búa sjálfkrafa til afrit af sniðmátum sem búa í skilgreiningum á ER-sniðmátum.</span><span class="sxs-lookup"><span data-stu-id="91feb-146">By default, the process of automatically creating backup copies of templates that reside in ER format configurations is turned on.</span></span> <span data-ttu-id="91feb-147">Til að hætta að taka afrit af sniðmátum stillirðu valkostinn **Hætta að gera afrit af sniðmáti** á **Já** á flipanum **Viðhengi** á síðunni **Rafrænar breytur**.</span><span class="sxs-lookup"><span data-stu-id="91feb-147">To stop making backup copies of templates, set the **Stop making backup copies of template** option to **Yes** on the **Attachments** tab of the **Electronic reporting parameters** page.</span></span> <span data-ttu-id="91feb-148">Hægt er að opna þessa síðu úr vinnusvæðinu **Rafræn skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="91feb-148">You can open this page from the **Electronic reporting** workspace.</span></span>

<span data-ttu-id="91feb-149">Ef þú stillir valkostinn **Hætta að búa til afrit af sniðmátum** á **Já** og vilt ekki geyma afrit sem áður voru gerð af sniðmátum skaltu velja **Hreinsa upp afritunargeymslu** á síðunni **Rafrænar skýrslufæribreytur**.</span><span class="sxs-lookup"><span data-stu-id="91feb-149">If you set the **Stop making backup copies of templates** option to **Yes** and don't want to keep the backup copies that were previously made of templates, select **Clean up backup storage** on the **Electronic reporting parameters** page.</span></span>

<span data-ttu-id="91feb-150">Ef þú uppfærðir umhverfi þitt í Finance and Operations útgáfu 10.0.5 (október 2019) og vilt flytja yfir í nýtt umhverfi sem inniheldur skilgreiningar ER-sniðmáta sem hægt er að keyra skaltu velja **Skrá í afritunargeymslu** á síðunni **Rafrænar skýrslufæribreytur** áður en flutningur á sér stað.</span><span class="sxs-lookup"><span data-stu-id="91feb-150">If you upgraded your environment to Finance and Operations version 10.0.5 (October 2019) and want to migrate to a new environment that includes ER format configurations that can be run, select **Fill in backup storage** on the **Electronic reporting parameters** page before the migration occurs.</span></span> <span data-ttu-id="91feb-151">Þessi hnappur hefur ferlið við að stofna afrit af öllum tiltækum sniðmátum svo hægt sé að geyma þau í varabúnaðargeymslu ER fyrir sniðmát.</span><span class="sxs-lookup"><span data-stu-id="91feb-151">This button starts the process of making backup copies of all available templates, so that they can be stored in the ER backup storage location for templates.</span></span>

![Síða rafrænna skýrslufæribreyta](./media/GER-BackupTemplates-5.png)

## <a name="supported-deployments"></a><span data-ttu-id="91feb-153">Studdar uppsetninar</span><span class="sxs-lookup"><span data-stu-id="91feb-153">Supported deployments</span></span>

<span data-ttu-id="91feb-154">Í Finance and Operations útgáfu 10.0.5 er eiginleikinn Afritunargeymsla ER-sniðmáta aðeins tiltækur í skýjadreifingum.</span><span class="sxs-lookup"><span data-stu-id="91feb-154">In Finance and Operations version 10.0.5, the Backup storage of ER templates feature is available only in cloud deployments.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="91feb-155">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="91feb-155">Additional resources</span></span>

[<span data-ttu-id="91feb-156">Yfirlit yfir rafræna skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="91feb-156">Electronic reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="91feb-157">Skilgreina rafrænan skýrslugerðarramma</span><span class="sxs-lookup"><span data-stu-id="91feb-157">Configure the Electronic reporting framework</span></span>](electronic-reporting-er-configure-parameters.md)