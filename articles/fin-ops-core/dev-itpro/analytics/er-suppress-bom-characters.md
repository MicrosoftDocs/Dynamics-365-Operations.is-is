---
title: Hanna skilgreiningar rafrænnar skýrslugerðar til að útiloka BOM-stafi í mynduðum skrám
description: Í þessu efnisatriði er útskýrt hvernig skilgreina á snið rafrænnar skýrslugerðar til að búa til skýrslur sem útiloka BOM-stafi.
author: NickSelin
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d5ada93c0192aadac70c38c8c8c4f3af86ff6fc3
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893277"
---
# <a name="design-er-configurations-to-suppress-bom-characters-in-generated-files"></a><span data-ttu-id="c3c31-103">Hanna skilgreiningar rafrænnar skýrslugerðar til að útiloka BOM-stafi í mynduðum skrám</span><span class="sxs-lookup"><span data-stu-id="c3c31-103">Design ER configurations to suppress BOM characters in generated files</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c3c31-104">Hægt er að hanna [Rafræna skýrslugerðar](general-electronic-reporting.md)[lausn](er-quick-start1-new-solution.md) til að mynda skjöl á útleið.</span><span class="sxs-lookup"><span data-stu-id="c3c31-104">You can design an [Electronic reporting (ER)](general-electronic-reporting.md) [solution](er-quick-start1-new-solution.md) to generate outgoing documents.</span></span> <span data-ttu-id="c3c31-105">Til að mynda skölin sem texta eða XML-skrá verður lausnin að fela í sér [skilgreiningu](general-electronic-reporting.md#Configuration) rafrænnar skýrslugerðar sem inniheldur [sniðshlut](general-electronic-reporting.md#FormatComponentOutbound) rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="c3c31-105">To generate the documents as text or XML files, the solution must include an ER [configuration](general-electronic-reporting.md#Configuration) that contains an ER [format](general-electronic-reporting.md#FormatComponentOutbound) component.</span></span> <span data-ttu-id="c3c31-106">Til að tilgreina [stafakóðun](/windows/win32/intl/character-sets) sem stendur fyrir safn stafa í mynduðum skrám, verður snið rafrænnar skýrslugerðar að innihalda sniðseininguna **Algeng\\Skrá**.</span><span class="sxs-lookup"><span data-stu-id="c3c31-106">To specify the [character encoding](/windows/win32/intl/character-sets) that represents the set of characters in generated files, the ER format must contain the **Common\\File** format element.</span></span> <span data-ttu-id="c3c31-107">Til að skilgreina sniðsþátt rafrænnar skýrslugerðar skal opna útgáfu [draga](general-electronic-reporting.md#component-versioning) fyrir skilgreiningu rafrænnar skýrslugerðar í sniðshönnuði rafrænnar skýrslugerðar og bæta við einingunni **Algeng\\Skrá**.</span><span class="sxs-lookup"><span data-stu-id="c3c31-107">To configure the ER format component, open the [draft](general-electronic-reporting.md#component-versioning) version of the ER configuration in the ER format designer, and add the **Common\\File** element.</span></span> <span data-ttu-id="c3c31-108">Í reitnum **Kóðun** skal tilgreina kóðun á skjölum á útleið sem eru mynduð við keyrslu með því að nota þennan þátt.</span><span class="sxs-lookup"><span data-stu-id="c3c31-108">In the **Encoding** field, specify the encoding of outbound files that are generated at runtime by using this component.</span></span>

> [!NOTE]
> <span data-ttu-id="c3c31-109">Ef sniðið inniheldur rangt kóðunarheiti kemur upp villa þegar breytingarnar eru vistaðar í stillingum sniðsins.</span><span class="sxs-lookup"><span data-stu-id="c3c31-109">If the format contains an incorrect encoding name, an error is thrown when you save your changes to the format's settings.</span></span>

![Rótareiningu bætt við síðu sniðshönnuðar](./media/er-suppress-bom-characters-image1.gif)

<span data-ttu-id="c3c31-111">Ef **UTF-8**, **UTF-16** eða **UTF-32** er tilgreint sem kóðunin verður valkosturinn **Útiloka BOM-stafi** tiltækur.</span><span class="sxs-lookup"><span data-stu-id="c3c31-111">If you specify **UTF-8**, **UTF-16**, or **UTF-32** as the encoding, the **Suppress BOM characters** option becomes available.</span></span> <span data-ttu-id="c3c31-112">Stillið þennan valkost á **Já** til að útiloka [BOM-stafi](/globalization/encoding/byte-order-mark) í skrám á útleið sem eru myndaðar við keyrslu þegar breytanlegt snið rafrænnar skýrslugerðar er keyrt.</span><span class="sxs-lookup"><span data-stu-id="c3c31-112">Set this option to **Yes** to suppress [byte order mark (BOM) characters](/globalization/encoding/byte-order-mark) in outbound files that are generated at runtime when the editable ER format is run.</span></span>

> [!NOTE]
> <span data-ttu-id="c3c31-113">Ef reiturinn **Kóðun** er skilinn eftur auður verður sjálfgefna kóðunin **UTF-8** notuð.</span><span class="sxs-lookup"><span data-stu-id="c3c31-113">If you leave the **Encoding** field blank, the default **UTF-8** encoding is used.</span></span>

![Valkostur útilokunar BOM-stafa stilltur á síðu sniðshönnuðar](./media/er-suppress-bom-characters-image2.gif)

<span data-ttu-id="c3c31-115">Til að fara yfir virkni við keyrslu skal ljúka viðeigandi ferli.</span><span class="sxs-lookup"><span data-stu-id="c3c31-115">To review the functionality at runtime, complete the appropriate procedure.</span></span> <span data-ttu-id="c3c31-116">Ljúkið sem dæmi við skrefin í efnisatriðinu [Fresta keyrslu XML-eininga á sniði rafrænnar skýrslugerðar](er-defer-xml-element.md).</span><span class="sxs-lookup"><span data-stu-id="c3c31-116">For example, complete the steps in the [Defer the execution of XML elements in ER formats](er-defer-xml-element.md) topic.</span></span> <span data-ttu-id="c3c31-117">Þegar búið er að ljúka við skrefin í hlutanum [Breyta sniði þannig að útreikningurinn byggist á mynduðu úttaki](er-defer-xml-element.md#modify-the-format-so-that-the-calculation-is-based-on-generated-output) í því efnisatriði skal fylgja þessum viðbótarskrefum.</span><span class="sxs-lookup"><span data-stu-id="c3c31-117">After you've completed the steps in the [Modify the format so that the calculation is based on generated output](er-defer-xml-element.md#modify-the-format-so-that-the-calculation-is-based-on-generated-output) section of that topic, follow these additional steps.</span></span>

1. <span data-ttu-id="c3c31-118">Tilgreinið UTF-kóðunina:</span><span class="sxs-lookup"><span data-stu-id="c3c31-118">Specify the UTF encoding:</span></span>

    1. <span data-ttu-id="c3c31-119">Velja skal eininguna **Skýrsla** af gerðinni **Algeng\\Skrá**.</span><span class="sxs-lookup"><span data-stu-id="c3c31-119">Select the **Report** element of the **Common\\File** type.</span></span>
    2. <span data-ttu-id="c3c31-120">Í reitnum **Kóðun** skal tilgreina kóðunina **UTF-8**.</span><span class="sxs-lookup"><span data-stu-id="c3c31-120">In the **Encoding** field, specify the **UTF-8** encoding.</span></span>

2. <span data-ttu-id="c3c31-121">Myndið XML-skrá sem inniheldur BOM-stafi:</span><span class="sxs-lookup"><span data-stu-id="c3c31-121">Generate an XML file that includes a BOM character:</span></span>

    1. <span data-ttu-id="c3c31-122">Stillið valkostinn **Útiloka BOM-stafi** á **Nei** til að hafa með BOM-stafi í mynduðum XML-skrám.</span><span class="sxs-lookup"><span data-stu-id="c3c31-122">Set the **Suppress BOM characters** option to **No** to include BOM characters in generated XML files.</span></span>
    2. <span data-ttu-id="c3c31-123">Ljúkið skrefunum í hlutanum [Fresta keyrslu á samantekt XML-einingar þannig að reiknuð samtala sé notuð](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) í efnisatriðinu [Fresta keyrslu XML-eininga á sniði rafrænnar skýrslugerðar](er-defer-xml-element.md) og vistið myndaða skrá sem **SampleXmlReport.xml**.</span><span class="sxs-lookup"><span data-stu-id="c3c31-123">Complete the steps in the [Defer the execution of the summary XML element so that the calculated total is used](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) section of the [Defer the execution of XML elements in ER formats](er-defer-xml-element.md) topic, and save the generated file as **SampleXmlReport.xml**.</span></span>

3. <span data-ttu-id="c3c31-124">Myndið XML-skrá sem inniheldur ekki BOM-stafi:</span><span class="sxs-lookup"><span data-stu-id="c3c31-124">Generate an XML file that doesn't include a BOM character:</span></span>

    1. <span data-ttu-id="c3c31-125">Stillið valkostinn **Útiloka BOM-stafi** á **Já** til að útiloka BOM-stafi í mynduðum XML-skrám.</span><span class="sxs-lookup"><span data-stu-id="c3c31-125">Set the **Suppress BOM characters** option to **Yes** to suppress BOM characters in generated XML files.</span></span>
    2. <span data-ttu-id="c3c31-126">Ljúkið skrefunum í hlutanum [Fresta keyrslu á samantekt XML-einingar þannig að reiknuð samtala sé notuð](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) í efnisatriðinu [Fresta keyrslu XML-eininga á sniði rafrænnar skýrslugerðar](er-defer-xml-element.md) og vistið myndaða skrá sem **SampleXmlReport (1).xml**.</span><span class="sxs-lookup"><span data-stu-id="c3c31-126">Complete the steps in the [Defer the execution of the summary XML element so that the calculated total is used](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) section of the [Defer the execution of XML elements in ER formats](er-defer-xml-element.md) topic, and save the generated file as **SampleXmlReport (1).xml**.</span></span>

4. <span data-ttu-id="c3c31-127">Í skráarsamanburði skal bera saman myndaðar skrár.</span><span class="sxs-lookup"><span data-stu-id="c3c31-127">In a file comparison utility, compare the generated files.</span></span>

    <span data-ttu-id="c3c31-128">Fyrsti munurinn sem tekið verður eftir er skráarhausinn.</span><span class="sxs-lookup"><span data-stu-id="c3c31-128">The first difference that you will notice is in the file header.</span></span> <span data-ttu-id="c3c31-129">Skráin SampleXmlReport.xml inniheldur BOM-staf þar sem skráin SampleXmlReport (1).xml gerir ekki.</span><span class="sxs-lookup"><span data-stu-id="c3c31-129">The SampleXmlReport.xml file contains a BOM character, where the SampleXmlReport (1).xml file doesn't.</span></span>

    ![Myndaðar skrár bornar saman með forriti samanburðarskráar](./media/er-suppress-bom-characters-image3.png)

## <a name="see-also"></a><span data-ttu-id="c3c31-131">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="c3c31-131">See also</span></span>

- [<span data-ttu-id="c3c31-132">Fresta keyrslu XML-eininga á sniði rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="c3c31-132">Defer the execution of XML elements in ER formats</span></span>](er-defer-xml-element.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]