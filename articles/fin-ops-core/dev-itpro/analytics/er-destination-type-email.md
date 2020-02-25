---
title: Tölvupóstur ER-gerð áfangastaðar
description: Þetta efni veitir upplýsingar um hvernig á að stilla tölvpóst áfangastaðar fyrir hvern FOLDER eða FILE hluti á rafrænu skýrslugerðarsniðinu (ER) sem er stillt til að búa til útgönguskjöl.
author: NickSelin
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 086114d6a8d425ca01521d9607e4a70ec5aa766b
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019826"
---
# <span data-ttu-id="4d521-103"><a name="EmailDestinationType">Áfangastður tölvupósts</a></span><span class="sxs-lookup"><span data-stu-id="4d521-103"><a name="EmailDestinationType">Email destination</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4d521-104">Hægt er að stilla tölvupóst áfangastaðar fyrir hvern FOLDER eða FILE hluti á rafrænu skýrslugerðarsniðinu (ER) sem er stillt til að búa til útgönguskjöl.</span><span class="sxs-lookup"><span data-stu-id="4d521-104">You can configure an email destination for each FOLDER or FILE component of an Electronic reporting (ER) format that is configured to generate outbound documents.</span></span> <span data-ttu-id="4d521-105">Byggt á ákvörðunarstað, er myndað skjal afhent sem viðhengi við tölvupost.</span><span class="sxs-lookup"><span data-stu-id="4d521-105">Based on the destination setting, a generated document is delivered as an attachment of an electronic mail.</span></span>

<span data-ttu-id="4d521-106">Setja **Virkt** til **Já** til að senda frálagsskrá með tölvupósti.</span><span class="sxs-lookup"><span data-stu-id="4d521-106">Set **Enabled** to **Yes** to send an output file by email.</span></span> <span data-ttu-id="4d521-107">Eftir að þessi valkostur er virkjaður er hægt að breyta efni tölvupósts og tilgreina viðtakendur tölvupósts og meginmál tölvupósts.</span><span class="sxs-lookup"><span data-stu-id="4d521-107">After this option is enabled, you can specify the email recipients and edit the subject and body of the email message.</span></span> <span data-ttu-id="4d521-108">Hægt er að setja upp fastatexta fyrir efni og meginmál tölvupósts eða hægt er að nota ER-[formúlur](er-formula-language.md) til að gagnvirkt stofna texta tölvupósts.</span><span class="sxs-lookup"><span data-stu-id="4d521-108">You can set up constant texts for the email subject and body, or you can use ER [formulas](er-formula-language.md) to dynamically create email texts.</span></span> 

<span data-ttu-id="4d521-109">Hægt er að grunnstilla netföng fyrir rafræn skýrslugerð á tvo vegu.</span><span class="sxs-lookup"><span data-stu-id="4d521-109">You can configure email addresses for ER in two ways.</span></span> <span data-ttu-id="4d521-110">Hægt er að klára stillingarnar á sama hátt og prentstjórnunaraðgerðin lýkur henni, eða þú getur leyst netfang með því að nota bein tilvísun í ER stillingar með formúlu.</span><span class="sxs-lookup"><span data-stu-id="4d521-110">The configuration can be completed in the same way that the Print management feature completes it, or you can resolve an email address by using a direct reference to the ER configuration through a formula.</span></span>

<span data-ttu-id="4d521-111">[![Virkja áfangastað tölvupósts](./media/ER_Destinations-EnableSingleDestination.png)](./media/ER_Destinations-EnableSingleDestination.png)</span><span class="sxs-lookup"><span data-stu-id="4d521-111">[![Enable email destination](./media/ER_Destinations-EnableSingleDestination.png)](./media/ER_Destinations-EnableSingleDestination.png)</span></span>

## <a name="email-address-types"></a><span data-ttu-id="4d521-112">Gerðir tölvupóstfanga</span><span class="sxs-lookup"><span data-stu-id="4d521-112">Email address types</span></span>

<span data-ttu-id="4d521-113">Þegar þú velur **Breyta** í reitunum **Til** eða **Cc** birtist svarglugginn **Senda tölvupóst til**.</span><span class="sxs-lookup"><span data-stu-id="4d521-113">When you select **Edit** in the **To** or **Cc** fields, the **Email to** dialog box appears.</span></span> <span data-ttu-id="4d521-114">Síðan er hægt að velja rétta gerð tölvupóstfangs til að nota.</span><span class="sxs-lookup"><span data-stu-id="4d521-114">You can then select the type of email address to use.</span></span> <span data-ttu-id="4d521-115">Tölvupósttegundirnar **Skilgreiningartölvupóstur** og **Prentstýring** eru studdar eins og er.</span><span class="sxs-lookup"><span data-stu-id="4d521-115">The **Configuration email** and **Print Management** email types are currently supported.</span></span>

<span data-ttu-id="4d521-116">[![Veldu tölvupóstserð](./media/ER_Destinations-EmailSelectAddressType.png)](./media/ER_Destinations-EmailSelectAddressType.png)</span><span class="sxs-lookup"><span data-stu-id="4d521-116">[![Select email type](./media/ER_Destinations-EmailSelectAddressType.png)](./media/ER_Destinations-EmailSelectAddressType.png)</span></span>

### <a name="print-management"></a><span data-ttu-id="4d521-117">Prentstýring</span><span class="sxs-lookup"><span data-stu-id="4d521-117">Print management</span></span>

<span data-ttu-id="4d521-118">Ef þú velur tölvupóstgerðina **Prentstýring tölvupóstur** geturðu fært inn fast netfang í reitinn **Til**.</span><span class="sxs-lookup"><span data-stu-id="4d521-118">If you select the **Print Management** email type, you can enter fixed email addresses in the **To** field.</span></span> 

<span data-ttu-id="4d521-119">[![Stilla föst netföng](./media/ER_Destinations-EmailFixedAddress.png)](./media/ER_Destinations-EmailFixedAddress.png)</span><span class="sxs-lookup"><span data-stu-id="4d521-119">[![Configure fixed email addresses](./media/ER_Destinations-EmailFixedAddress.png)](./media/ER_Destinations-EmailFixedAddress.png)</span></span>

<span data-ttu-id="4d521-120">Til að nota tölvupóstföng sem eru ekki föst, verður að velja upprunagerð tölvupósts fyrir áfangastað skrár.</span><span class="sxs-lookup"><span data-stu-id="4d521-120">To use email addresses that aren't fixed, you must select the email source type for a file destination.</span></span> <span data-ttu-id="4d521-121">Eftirfarandi virði eru studd: **Viðskiptavinur**, **Lánardrottinn**, **Viðfang**, **Tengiliður**, **Samkeppnisaðili**, **Starfskraftur**, **Umsækjandi**, **Væntanlegur lánardrottinn**, og **Lánardrottinn án leyfis**.</span><span class="sxs-lookup"><span data-stu-id="4d521-121">The following values are supported: **Customer**, **Vendor**, **Prospect**, **Contact**, **Competitor**, **Worker**, **Applicant**, **Prospective vendor**, and **Disallowed vendor**.</span></span> <span data-ttu-id="4d521-122">Eftir að upprunagerð tölvupósts er valin skal nota næsta hnapp við reitinn **Upprunareikningur tölvupósts** til að opna skjámyndina **Formúluhönnuður**.</span><span class="sxs-lookup"><span data-stu-id="4d521-122">After you select an email source type, use the button next to the **Email source account** field to open the **Formula designer** form.</span></span> <span data-ttu-id="4d521-123">Þú getur notað þetta form til að festa við formúlu sem skilar sér á keyrslutíma, **aðilalykill** af völdum upprunategundum frá unnu skjali til áfangastaðar tölvupóstsins.</span><span class="sxs-lookup"><span data-stu-id="4d521-123">You can use this form to attach a formula that returns at runtime, the **party account** of the selected source type from the processed document to the email destination.</span></span>

<span data-ttu-id="4d521-124">[![Stilla upprunareikning tölvupósts](./media/ER_Destinations-EmailDefineAddressSource.png)](./media/ER_Destinations-EmailDefineAddressSource.png)</span><span class="sxs-lookup"><span data-stu-id="4d521-124">[![Configure email source account](./media/ER_Destinations-EmailDefineAddressSource.png)](./media/ER_Destinations-EmailDefineAddressSource.png)</span></span>

<span data-ttu-id="4d521-125">Formúlur eru við tilgreindar fyrir skilgreiningu rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="4d521-125">Formulas are specific to the ER configuration.</span></span> <span data-ttu-id="4d521-126">Í **formúla**, Færið inn skjalbundna tilvísun í viðskiptavin eða lánardrottinn gerð aðila.</span><span class="sxs-lookup"><span data-stu-id="4d521-126">In the **Formula** field, enter a document-specific reference to a customer or vendor party type.</span></span> <span data-ttu-id="4d521-127">Í stað þess að slá inn, hægt að finna gagnaveituhnút sem stendur fyrir lykil viðskiptavinar eða lánardrottins, og velja hnappinn **Bæta við gagnaveitu** til að uppfæra formúluna.</span><span class="sxs-lookup"><span data-stu-id="4d521-127">Instead of typing, you can find the data source node that represents the customer or vendor account, and then select **Add data source** to update the formula.</span></span> <span data-ttu-id="4d521-128">Til dæmis, ef þú notar skilgreininguna **ISO 20022 kreditmillifærsla** er hnúturinn sem stendur fyrir lykil lánardrottins er `'\$PaymentsForCoveringLetter'.Creditor.Identification.SourceID`.</span><span class="sxs-lookup"><span data-stu-id="4d521-128">For example, if you use the **ISO 20022 Credit Transfer** configuration, the node that represents a vendor account is `'\$PaymentsForCoveringLetter'.Creditor.Identification.SourceID`.</span></span>

<span data-ttu-id="4d521-129">Ef þú slærð inn strenggildi, svo sem `"DE-001"` og vistar formúlu verður tölvupóstur sendur til tengiliðs seljandans, **DE-001**.</span><span class="sxs-lookup"><span data-stu-id="4d521-129">If you enter a string value, such as `"DE-001"`, and save a formula, an email will be sent to the contact person of the vendor, **DE-001**.</span></span>


<span data-ttu-id="4d521-130">[![Síðan ER-formúluhönnuður](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)</span><span class="sxs-lookup"><span data-stu-id="4d521-130">[![ER formula designer page](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)</span></span>

<span data-ttu-id="4d521-131">[![Stilla upprunareikning tölvupósts](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)</span><span class="sxs-lookup"><span data-stu-id="4d521-131">[![Configure email source account](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)</span></span>



### <a name="configuration-email"></a><span data-ttu-id="4d521-132">Skilgreiningartölvupóstur</span><span class="sxs-lookup"><span data-stu-id="4d521-132">Configuration email</span></span>

<span data-ttu-id="4d521-133">Notaðu þessa gerð tölvupósts ef skilgreiningin sem þú notar er með hnút í gagnaveitum sem skilar **netfangi**.</span><span class="sxs-lookup"><span data-stu-id="4d521-133">Use this email type if the configuration that you use has a node in the data sources that returns an **email address**.</span></span> <span data-ttu-id="4d521-134">Hægt er að nota gagnaveitur og aðgerðir í formúluhönnuður til að ná rétt sniðnu netfang.</span><span class="sxs-lookup"><span data-stu-id="4d521-134">You can use data sources and functions in the formula designer to get a correctly formatted email address.</span></span> <span data-ttu-id="4d521-135">Til dæmis, ef þú notar skilgreininguna **ISO 20022 kreditmillifærsla** er hnúturinn sem stendur fyrir netfang tengiliðar lánardrottins `'$PaymentsForCoveringLetter'.Creditor.ContactDetails.Email`.</span><span class="sxs-lookup"><span data-stu-id="4d521-135">For example, if you use the **ISO 20022 Credit Transfer** configuration, the node that represents an email address of a vendor's contact person is `'$PaymentsForCoveringLetter'.Creditor.ContactDetails.Email`.</span></span>

<span data-ttu-id="4d521-136">[![Stilla heimilisfangagjafa tölvupósts](./media/ER_Destinations-EmailDefineAddressSource2.png)](./media/ER_Destinations-EmailDefineAddressSource2.png)</span><span class="sxs-lookup"><span data-stu-id="4d521-136">[![Configure email address source](./media/ER_Destinations-EmailDefineAddressSource2.png)](./media/ER_Destinations-EmailDefineAddressSource2.png)</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4d521-137">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="4d521-137">Additional resources</span></span>

- [<span data-ttu-id="4d521-138">Yfirlit yfir rafræna skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="4d521-138">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="4d521-139">Áfangastaðir fyrir rafræna skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="4d521-139">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="4d521-140">Formúluhönnuður í rafrænni skýrslugerð (ER)</span><span class="sxs-lookup"><span data-stu-id="4d521-140">Formula designer in Electronic reporting (ER)</span></span>](general-electronic-reporting-formula-designer.md)
