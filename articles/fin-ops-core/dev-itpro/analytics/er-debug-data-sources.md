---
title: Kemba gagnagjafa af keyrðu sniði rafrænnar skýrslugerðar til að greina gagnaflæði og umbreytingu
description: Í þessu efnisatriði er útskýrt hvernig hægt er að kemba gagnagjafa af keyrðu sniði rafrænnar skýrslugerðar til að skilja betur skilgreint gagnaflæði og umbreytingu.
author: NickSelin
manager: AnnBe
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: bda81da80996d8cba38ac48e29c47ffef61d3bdb
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562191"
---
# <a name="debug-data-sources-of-an-executed-er-format-to-analyze-data-flow-and-transformation"></a><span data-ttu-id="f20ca-103">Kemba gagnagjafa af keyrðu sniði rafrænnar skýrslugerðar til að greina gagnaflæði og umbreytingu</span><span class="sxs-lookup"><span data-stu-id="f20ca-103">Debug data sources of an executed ER format to analyze data flow and transformation</span></span>

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

<span data-ttu-id="f20ca-104">Þegar lausn rafrænnar skýrslugerðar er [skilgreind](tasks/er-format-configuration-2016-11.md) til að útbúa skjöl á útleið, skilgreinir þú aðferðirnar sem notaðar eru til að ná gögnum úr forritinu og færa þau inn í úttakið sem búið er til.</span><span class="sxs-lookup"><span data-stu-id="f20ca-104">When you [configure](tasks/er-format-configuration-2016-11.md) an Electronic reporting (ER) solution to generate outbound documents, you define the methods that are used to get data out of the application and enter it in the output that is generated.</span></span> <span data-ttu-id="f20ca-105">Til að gera líftímastuðning fyrir lausn rafrænnar skýrslugerðar skilvirkari ætti lausnin þín að samanstanda af [gagnlíkani](general-electronic-reporting.md#DataModelComponent) rafrænnar skýrslugerðar og hlutum [vörpunar](general-electronic-reporting.md#ModelMappingComponent) sem tengjast því, og einnig [snið](general-electronic-reporting.md#FormatComponentOutbound) rafrænnar skýrslugerðar og vörpunarhlutum þess svo að vörpunarlíkanið miðist við forritið, á meðan aðrir hlutar eru áfram óháðir forritinu.</span><span class="sxs-lookup"><span data-stu-id="f20ca-105">To make the life cycle support of the ER solution more efficient, your solution should consist of an ER [data model](general-electronic-reporting.md#DataModelComponent) and its [mapping](general-electronic-reporting.md#ModelMappingComponent) components, and also an ER [format](general-electronic-reporting.md#FormatComponentOutbound) and its mapping components, so that the model mapping is application-specific, whereas other components remain application-agnostic.</span></span> <span data-ttu-id="f20ca-106">Þar af leiðandi gætu nokkrir hlutar rafrænnar skýrslugerðar haft [áhrif](general-electronic-reporting.md#FormatComponentOutbound) á ferli gagnainnsláttar í úttakinu sem búið er til.</span><span class="sxs-lookup"><span data-stu-id="f20ca-106">Therefore, several ER components might [affect](general-electronic-reporting.md#FormatComponentOutbound) the process of entering data in the generated output.</span></span>

<span data-ttu-id="f20ca-107">Stundum líta gögn myndaðs úttaks út fyrir að vera öðruvísi en sömu gögn í gagnagrunni forritsins.</span><span class="sxs-lookup"><span data-stu-id="f20ca-107">Sometimes, the data of the generated output looks different than the same data in the application database.</span></span> <span data-ttu-id="f20ca-108">Í þessum tilvikum er æskilegt að ákvarða hvaða íhlutur rafrænnar skýrslugerðar er ábyrgur fyrir gagnaumbreytingu.</span><span class="sxs-lookup"><span data-stu-id="f20ca-108">In these cases, you will want to determine which ER component is responsible for the data transformation.</span></span> <span data-ttu-id="f20ca-109">Kembiforritseiginleiki gagnagjafa rafrænnar skýrslugerðar dregur umtalsvert úr tíma og kostnaði sem eru hluti af þessari skoðun.</span><span class="sxs-lookup"><span data-stu-id="f20ca-109">The ER data source debugger feature significantly reduces the time and cost that are involved in this investigation.</span></span> <span data-ttu-id="f20ca-110">Hægt er að stöðva keyrslu sniðs rafrænnar skýrslugerðar og opna kembiviðmót gagnagjafans.</span><span class="sxs-lookup"><span data-stu-id="f20ca-110">You can interrupt the execution of an ER format and open the data source debugger interface.</span></span> <span data-ttu-id="f20ca-111">Þar er hægt að fletta upp tiltækum gagnagjöfum og velja staka gagnagjafa til keyrslu.</span><span class="sxs-lookup"><span data-stu-id="f20ca-111">There, you can browse the available data sources and select an individual data source for execution.</span></span> <span data-ttu-id="f20ca-112">Þessi handvirka keyrsla líkir eftir keyrslu gagnagjafans við raunkeyrslu á snið rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="f20ca-112">This manual execution simulates the execution of the data source during the real run of an ER format.</span></span> <span data-ttu-id="f20ca-113">Niðurstaðan kemur fram á síðu þar sem hægt er að greina gögnin sem eru móttekin.</span><span class="sxs-lookup"><span data-stu-id="f20ca-113">The result is presented on a page where you can analyze the data that is received.</span></span>

<span data-ttu-id="f20ca-114">Til að kveikja á villuleitareiginleika gagnagjafa skaltu stilla valkostinn **Virkja gagnakembingu við sniðskeyrslu** á **Já** í notendafæribreytum rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="f20ca-114">To turn on the data source debugging feature, set the **Enable data debugging at format run** option to **Yes** in the ER user parameters.</span></span> <span data-ttu-id="f20ca-115">Hægt er að ræsa kembingu gagnagjafa þegar snið rafrænnar skýrslugerðar keyrt til að mynda skjöl á útleið.</span><span class="sxs-lookup"><span data-stu-id="f20ca-115">You can then start data source debugging while you run an ER format to generate outbound documents.</span></span> <span data-ttu-id="f20ca-116">Einnig er hægt að nota valkostinn **Hefja kembingu** til að ræsa gagnakerfiskembingu fyrir snið rafrænnar skýrslugerðar sem er skilgreint í reitnum [Aðgerðarhönnuður rafrænnar skýrslugerða](./tasks/er-format-configuration-2016-11.md#design-the-format-of-an-electronic-document).</span><span class="sxs-lookup"><span data-stu-id="f20ca-116">You can also use the **Start debugging** option to initiate data source debugging for an ER format that is configured in the [ER Operation designer](./tasks/er-format-configuration-2016-11.md#design-the-format-of-an-electronic-document).</span></span>

<span data-ttu-id="f20ca-117">Í þessu efnisatriði er að finna leiðarvísi til að hefja kembingu á gagnagjafa fyrir keyrð snið rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="f20ca-117">This topic provides guidelines for initiating data source debugging for executed ER formats.</span></span> <span data-ttu-id="f20ca-118">Það útskýrir hvernig upplýsingarnar geta hjálpað til við að skilja gagnaflæði og gagnaumbreytingu.</span><span class="sxs-lookup"><span data-stu-id="f20ca-118">It explains how the information can help you understand the data flow and data transformations.</span></span> <span data-ttu-id="f20ca-119">Í dæmunum í þessu efnisatriði er notast við viðskiptaferli fyrir meðhöndlun greiðslu lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="f20ca-119">The examples in this topic use the business process for vendor payments processing.</span></span>

## <a name="limitations"></a><span data-ttu-id="f20ca-120">Takmarkanir</span><span class="sxs-lookup"><span data-stu-id="f20ca-120">Limitations</span></span>

<span data-ttu-id="f20ca-121">Kembiforrit gagnagjafa er hægt að nota til að fá aðgang að gögnum gagnagjafa sem notuð eru í sniði rafrænnar skýrslugerðar sem keyrð eru til að mynda skjöl á útleið.</span><span class="sxs-lookup"><span data-stu-id="f20ca-121">The data source debugger can be used to access the data of data sources that are used in ER formats that are run to generate outbound documents.</span></span> <span data-ttu-id="f20ca-122">Ekki er hægt að nota hana til að kemba gagnaveitur á sniðum rafrænnar skýrslugerðar sem eru hönnuð til að þátta skjöl á innleið.</span><span class="sxs-lookup"><span data-stu-id="f20ca-122">It can't be used to debug data sources of ER formats that are designed to parse inbound documents.</span></span>

<span data-ttu-id="f20ca-123">Eftirfarandi stillingar á sniði rafrænnar skýrslugerðar eru ekki aðgengilegar fyrir kembingu gagnagjafa eins og er:</span><span class="sxs-lookup"><span data-stu-id="f20ca-123">The following settings of ER formats aren't currently accessible for data source debugging:</span></span>

- <span data-ttu-id="f20ca-124">Sníða umbreytingar</span><span class="sxs-lookup"><span data-stu-id="f20ca-124">Format transformations</span></span>
- <span data-ttu-id="f20ca-125">Villuleitarreglur sniðs og vörpunar</span><span class="sxs-lookup"><span data-stu-id="f20ca-125">Format and mapping validation rules</span></span>
- <span data-ttu-id="f20ca-126">Virkja segðir</span><span class="sxs-lookup"><span data-stu-id="f20ca-126">Enabling expressions</span></span>
- <span data-ttu-id="f20ca-127">Upplýsingar um gagnasöfnun í minni</span><span class="sxs-lookup"><span data-stu-id="f20ca-127">Details of in-memory data collection</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f20ca-128">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="f20ca-128">Prerequisites</span></span>

- <span data-ttu-id="f20ca-129">Til að ljúka dæmunum í þessu efnisatriði þarftu að hafa aðgang að einu af eftirfarandi [hlutverkum](../sysadmin/tasks/assign-users-security-roles.md):</span><span class="sxs-lookup"><span data-stu-id="f20ca-129">To complete the examples in this topic, you must have the access to one of the following [roles](../sysadmin/tasks/assign-users-security-roles.md):</span></span>

    - <span data-ttu-id="f20ca-130">Þróunaraðili rafrænnar skýrslulausnar</span><span class="sxs-lookup"><span data-stu-id="f20ca-130">Electronic reporting developer</span></span>
    - <span data-ttu-id="f20ca-131">Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="f20ca-131">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="f20ca-132">Kerfisstjóri</span><span class="sxs-lookup"><span data-stu-id="f20ca-132">System administrator</span></span>

- <span data-ttu-id="f20ca-133">Stilla verður fyrirtæki á **DEMF**.</span><span class="sxs-lookup"><span data-stu-id="f20ca-133">The company must be set to **DEMF**.</span></span>

- <span data-ttu-id="f20ca-134">Fylgja skal leiðbeiningunum í [Viðauka 1](#appendix1) í þessu efnisatriði til að sækja íhluti rafrænna skýrslugerðarlausna Microsoft sem nauðsynlegar eru til að vinna úr lánardrottnagreiðslum.</span><span class="sxs-lookup"><span data-stu-id="f20ca-134">Follow the steps in [Appendix 1](#appendix1) of this topic to download the components of the Microsoft ER solution that are required to process vendor payments.</span></span>
- <span data-ttu-id="f20ca-135">Fylgja skal eftirfarandi skrefum í [Viðauka 2](#appendix2) í þessu efnisatriði til að undirbúa viðskiptaskuldir fyrir úrvinnslu lánardrottnagreiðslna með því að nota lausn rafrænnar skýrslugerðar sem þú sækir.</span><span class="sxs-lookup"><span data-stu-id="f20ca-135">Follow the steps in [Appendix 2](#appendix2) of this topic to prepare Accounts payable for vendor payment processing by using the ER solution that you will download.</span></span>

## <a name="process-a-vendor-payment-to-get-a-payment-file"></a><span data-ttu-id="f20ca-136">Vinna úr greiðslu lánardrottins til að sækja greiðsluskrá</span><span class="sxs-lookup"><span data-stu-id="f20ca-136">Process a vendor payment to get a payment file</span></span>

1. <span data-ttu-id="f20ca-137">Fylgja skal leiðbeiningunum í [Viðauki 3](#appendix3) í þessu efnisatriði til að vinna úr lánardrottnagreiðslum.</span><span class="sxs-lookup"><span data-stu-id="f20ca-137">Follow the steps in [Appendix 3](#appendix3) of this topic to process vendor payments.</span></span>

    ![Greiðsluferli lánardrottins í vinnslu](./media/er-data-debugger-process-payment.png)

2. <span data-ttu-id="f20ca-139">Hlaða niður og vista zip-skrána í staðbundnu tölvunni.</span><span class="sxs-lookup"><span data-stu-id="f20ca-139">Download and save the zip file to your local computer.</span></span>
3. <span data-ttu-id="f20ca-140">Útvíkkið **ISO20022 Credit transfer.xml** greiðsluskrána úr zip-skránni.</span><span class="sxs-lookup"><span data-stu-id="f20ca-140">Extract the **ISO20022 Credit transfer.xml** payment file from the zip file.</span></span>
4. <span data-ttu-id="f20ca-141">Opnið útdregnu greiðsluskrána með því að nota XML-skrárskoðara.</span><span class="sxs-lookup"><span data-stu-id="f20ca-141">Open the extracted payment file by using the XML file viewer.</span></span>

    <span data-ttu-id="f20ca-142">Í greiðsluskránni inniheldur alþjóðlegt bankareikningsnúmer (IBAN-kóði) bankareiknings lánardrottins ekki nein bil.</span><span class="sxs-lookup"><span data-stu-id="f20ca-142">In the payment file, the International Bank Account Number (IBAN) code of the vendor bank account contains no spaces.</span></span> <span data-ttu-id="f20ca-143">Því er það frábrugðið gildinu sem var [slegið inn](#enteredIBANcode) á síðunni **Bankareikningar**.</span><span class="sxs-lookup"><span data-stu-id="f20ca-143">Therefore, it differs from the value that was [entered](#enteredIBANcode) on the **Bank accounts** page.</span></span>

    ![IBAN-kóði án bila](./media/er-data-debugger-payment-file.png)

    <span data-ttu-id="f20ca-145">Hægt er að nota kembiforrit fyrir gagnagjafa rafrænnar skýrslugerðar til að finna út hvaða íhlutir rafrænnar skýrslugerðarlausnar eru notaðir til að stytta bil í IBAN-númerinu.</span><span class="sxs-lookup"><span data-stu-id="f20ca-145">You can use the ER data source debugger to learn which component of the ER solution is used to truncate spaces in the IBAN code.</span></span>

## <a name="turn-on-data-source-debugging"></a><span data-ttu-id="f20ca-146">Kveikja á kembingu gagnagjafa</span><span class="sxs-lookup"><span data-stu-id="f20ca-146">Turn on data source debugging</span></span>

1. <span data-ttu-id="f20ca-147">Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.</span><span class="sxs-lookup"><span data-stu-id="f20ca-147">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="f20ca-148">Á síðunni **Skilgreiningar**, í aðgerðarúðunni, í flipanum **Skilgreiningar**, í flokknum **Ítarlegar stillingar**, skal velja **Færibreytur notanda**.</span><span class="sxs-lookup"><span data-stu-id="f20ca-148">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="f20ca-149">Stilltu valkostinn **Virkja gagnakembingu við sniðskeyrslu** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="f20ca-149">Set the **Enable data debugging at format run** option to **Yes**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f20ca-150">Þessi breyta er notendasértæk og fyrirtækjasértæk.</span><span class="sxs-lookup"><span data-stu-id="f20ca-150">This parameter is user-specific and company-specific.</span></span>

    ![Svarglugginn Notandafæribreytur](./media/er-data-debugger-user-parameters.png)

## <a name="process-a-vendor-payment-for-debugging"></a><span data-ttu-id="f20ca-152">Vinna úr greiðslu lánardrottins fyrir kembileit</span><span class="sxs-lookup"><span data-stu-id="f20ca-152">Process a vendor payment for debugging</span></span>

1. <span data-ttu-id="f20ca-153">Fylgja skal leiðbeiningunum í [Viðauki 3](#appendix3) í þessu efnisatriði til að vinna úr lánardrottnagreiðslum.</span><span class="sxs-lookup"><span data-stu-id="f20ca-153">Follow the steps in [Appendix 3](#appendix3) of this topic to process vendor payments.</span></span>
2. <span data-ttu-id="f20ca-154">Í skilaboðaglugganum skal velja **Já** til að staðfesta að þú viljir rjúfa úrvinnslu lánardrottnagreiðslu og í staðinn hefja kembingu á gagnagjafa á síðunni **Kemba gagnagjafa**.</span><span class="sxs-lookup"><span data-stu-id="f20ca-154">In the message box, select **Yes** to confirm that you want to interrupt vendor payment processing and instead start data source debugging on the **Debug Datasources** page.</span></span>

    ![Staðfestingarboðsreitur](./media/er-data-debugger-start-debugging.png)

## <a name="debug-data-sources-that-are-used-in-payment-processing"></a><span data-ttu-id="f20ca-156">Kembigagnaveitur sem eru notaðar í greiðsluvinnslu</span><span class="sxs-lookup"><span data-stu-id="f20ca-156">Debug data sources that are used in payment processing</span></span>

### <a name="debug-the-model-mapping"></a><span data-ttu-id="f20ca-157">Kemba líkanavörpun</span><span class="sxs-lookup"><span data-stu-id="f20ca-157">Debug the model mapping</span></span>

1. <span data-ttu-id="f20ca-158">Á síðunni **Kemba gagnagjafa**, á aðgerðasvæðinu, skal velja **Líkanavörpun** til að hefja kembingu á þessum íhlut rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="f20ca-158">On the **Debug Datasources** page, on the Action Pane, select **Model mapping** to start to debug from this ER component.</span></span>
2. <span data-ttu-id="f20ca-159">Í gagnaveitusvæðinu vinstra megin skal velja **\$notSentTransactions** gagnagjafa og síðan **Lesa allar færslur**.</span><span class="sxs-lookup"><span data-stu-id="f20ca-159">In the data source pane on the left, select the **\$notSentTransactions** data source, and then select **Read all records**.</span></span>

    <span data-ttu-id="f20ca-160">Hægt er að velja **Lesa 1 færslu**, **Lesa 10 færslur**, **Lesa 100 færslur** eða **Lesa allar færslur** til að þvinga lestur á viðeigandi fjölda færslna úr völdum gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="f20ca-160">You can select **Read 1 record**, **Read 10 records**, **Read 100 records**, or **Read all records** to force the appropriate number of records to be read from the selected data source.</span></span> <span data-ttu-id="f20ca-161">Á þennan hátt er hægt að líkja eftir aðgangi að gagnagjafanum út frá sniði rafrænnar skýrslugerðar sem verið er að keyra.</span><span class="sxs-lookup"><span data-stu-id="f20ca-161">In this way, you can simulate access to the data source from the running ER format.</span></span>

3. <span data-ttu-id="f20ca-162">Í gagnasvæðinu hægra megin skal velja **Útvíkka allt**.</span><span class="sxs-lookup"><span data-stu-id="f20ca-162">In the data pane on the right, select **Expand all**.</span></span>

    <span data-ttu-id="f20ca-163">Hægt er að sjá að valinn gagnagjafi af gerðinni **Færslulisti** inniheldur eina færslu.</span><span class="sxs-lookup"><span data-stu-id="f20ca-163">You can see that the selected data source of the **Record list** type contains a single record.</span></span>

4. <span data-ttu-id="f20ca-164">Útvíkkaðu gagnagjafann **\$notSentTransactions** og veldu földuðu aðferðina **vendBankAccountInTransactionCompany()**.</span><span class="sxs-lookup"><span data-stu-id="f20ca-164">Expand the **\$notSentTransactions** data source, and select the nested **vendBankAccountInTransactionCompany()** method.</span></span>
5. <span data-ttu-id="f20ca-165">Útvíkkið **vendBankAccountInTransactionCompany()** aðferðina og veljið faldaða **IBAN** reitinn.</span><span class="sxs-lookup"><span data-stu-id="f20ca-165">Expand the **vendBankAccountInTransactionCompany()** method, and select the nested **IBAN** field.</span></span>
6. <span data-ttu-id="f20ca-166">Veldu **Sækja gildi**.</span><span class="sxs-lookup"><span data-stu-id="f20ca-166">Select **Get value**.</span></span>

    <span data-ttu-id="f20ca-167">Hægt er að velja **Sækja gildi** til að þvinga lestur á gildi valins reits í völdum gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="f20ca-167">You can select **Get value** to force the value of a selected field of the selected data source to be read.</span></span> <span data-ttu-id="f20ca-168">Á þennan hátt er hægt að líkja eftir aðgangi að þessum reit út frá sniði rafrænnar skýrslugerðar sem verið er að keyra.</span><span class="sxs-lookup"><span data-stu-id="f20ca-168">In this way, you can simulate access to this field from the running ER format.</span></span>

7. <span data-ttu-id="f20ca-169">Veldu **Útvíkka allt**.</span><span class="sxs-lookup"><span data-stu-id="f20ca-169">Select **Expand all**.</span></span>

    ![Gildi IBAN-reits í líkanavörpun](./media/er-data-debugger-debugging-model-mapping.png)

    <span data-ttu-id="f20ca-171">Eins og sjá má er líkanavörpunin ekki ábyrg fyrir styttingu á bilum því að IBAN-númerið sem hún skilar fyrir bankareikning lánardrottins inniheldur bil.</span><span class="sxs-lookup"><span data-stu-id="f20ca-171">As you can see, the model mapping isn't responsible for the truncated spaces, because the IBAN code that it returns for the vendor bank account includes spaces.</span></span> <span data-ttu-id="f20ca-172">Þess vegna verður að halda áfram með kembingu gagnaveitu.</span><span class="sxs-lookup"><span data-stu-id="f20ca-172">Therefore, you must continue data source debugging.</span></span>

### <a name="debug-the-format-mapping"></a><span data-ttu-id="f20ca-173">Kemba vörpun sniðs</span><span class="sxs-lookup"><span data-stu-id="f20ca-173">Debug the format mapping</span></span>

1. <span data-ttu-id="f20ca-174">Á síðunni **Kemba gagnagjafa**, á aðgerðasvæðinu, skal velja **Vörpun sniðs** til að halda áfram kembingu á þessum íhlut rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="f20ca-174">On the **Debug Datasources** page, on the Action Pane, select **Format mapping** to continue to debug from this ER component.</span></span>
2. <span data-ttu-id="f20ca-175">Veldu **\$PaymentByDebtor** gagnagjafann og svo **Lesa allar færslur**.</span><span class="sxs-lookup"><span data-stu-id="f20ca-175">Select the **\$PaymentByDebtor** data source, and then select **Read all records**.</span></span>
3. <span data-ttu-id="f20ca-176">Útvíkkið **\$PaymentByDebtor**.</span><span class="sxs-lookup"><span data-stu-id="f20ca-176">Expand **\$PaymentByDebtor**.</span></span>
4. <span data-ttu-id="f20ca-177">Útvíkkið **\$PaymentByDebtor.Lines** og veljið svo **Lesa allar færslur**.</span><span class="sxs-lookup"><span data-stu-id="f20ca-177">Expand **\$PaymentByDebtor.Lines**, and then select **Read all records**.</span></span>
5. <span data-ttu-id="f20ca-178">Útvíkkið **\$PaymentByDebtor.Lines.CreditorAccount**.</span><span class="sxs-lookup"><span data-stu-id="f20ca-178">Expand **\$PaymentByDebtor.Lines.CreditorAccount**.</span></span>
6. <span data-ttu-id="f20ca-179">Útvíkkið **\$PaymentByDebtor.Lines.CreditorAccount.Identification** og veljið svo **\$PaymentByDebtor.Lines.CreditorAccount.Identification.IBAN**.</span><span class="sxs-lookup"><span data-stu-id="f20ca-179">Expand **\$PaymentByDebtor.Lines.CreditorAccount.Identification**, and then select **\$PaymentByDebtor.Lines.CreditorAccount.Identification.IBAN**.</span></span>
7. <span data-ttu-id="f20ca-180">Veldu **Sækja gildi**.</span><span class="sxs-lookup"><span data-stu-id="f20ca-180">Select **Get value**.</span></span>
8. <span data-ttu-id="f20ca-181">Veldu **Útvíkka allt**.</span><span class="sxs-lookup"><span data-stu-id="f20ca-181">Select **Expand all**.</span></span>

    ![Gildi IBAN-reitsins í vörpun sniðs](./media/er-data-debugger-debugging-format-mapping.png)

    <span data-ttu-id="f20ca-183">Eins og sjá má eru gagnagjafar sniðsvörpunar ekki ábyrgir fyrir styttingu á bilum því að IBAN-númerið sem þeir skila fyrir bankareikning lánardrottins inniheldur bil.</span><span class="sxs-lookup"><span data-stu-id="f20ca-183">As you can see, the data sources of the format mapping aren't responsible for the truncated spaces, because the IBAN code that they return for the vendor bank account includes spaces.</span></span> <span data-ttu-id="f20ca-184">Þess vegna verður að halda áfram með kembingu gagnaveitu.</span><span class="sxs-lookup"><span data-stu-id="f20ca-184">Therefore, you must continue data source debugging.</span></span>

### <a name="debug-the-format"></a><span data-ttu-id="f20ca-185">Kemba snið</span><span class="sxs-lookup"><span data-stu-id="f20ca-185">Debug the format</span></span>

1. <span data-ttu-id="f20ca-186">Á síðunni **Kemba gagnagjafa**, á aðgerðasvæðinu, skal velja **Snið** til að halda áfram kembingu á þessum íhlut rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="f20ca-186">On the **Debug Datasources** page, on the Action Pane, select **Format** to continue to debug from this ER component.</span></span>
2. <span data-ttu-id="f20ca-187">Víkkaðu sniðseiningar til að velja **ISO20022CTReports** \> **XMLHeader** \> **Skjal** \> **CstmrCdtTrfInitn** \> **PmtInf** og veljið svo **Lesa allar færslur**.</span><span class="sxs-lookup"><span data-stu-id="f20ca-187">Expand the format elements to select **ISO20022CTReports** \> **XMLHeader** \> **Document** \> **CstmrCdtTrfInitn** \> **PmtInf**, and then select **Read all records**.</span></span>
3. <span data-ttu-id="f20ca-188">Víkkaðu sniðseiningar til að velja **ISO20022CTReports** \> **XMLHeader** \> **Skjal** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** og veljið svo **Lesa allar færslur**.</span><span class="sxs-lookup"><span data-stu-id="f20ca-188">Expand the format elements to select **ISO20022CTReports** \> **XMLHeader** \> **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf**, and then select **Read all records**.</span></span>
4. <span data-ttu-id="f20ca-189">Víkkaðu sniðseiningar til að velja **ISO20022CTReports** \> **XMLHeader** \> **Skjal** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN** og veldu svo **Sækja gildi**.</span><span class="sxs-lookup"><span data-stu-id="f20ca-189">Expand the format elements to select **ISO20022CTReports** \> **XMLHeader** \> **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN**, and then select **Get value**.</span></span>
5. <span data-ttu-id="f20ca-190">Veldu **Útvíkka allt**.</span><span class="sxs-lookup"><span data-stu-id="f20ca-190">Select **Expand all**.</span></span>

    ![Gildi IBAN-reitsins á sniðinu](./media/er-data-debugger-debugging-format.png)

   <span data-ttu-id="f20ca-192">Eins og sjá má er sniðsbindingin ekki ábyrg fyrir styttingu á bilum því að IBAN-númerið sem hún skilar fyrir bankareikning lánardrottins inniheldur bil.</span><span class="sxs-lookup"><span data-stu-id="f20ca-192">As you can see, the format binding isn't responsible for the truncated spaces because the IBAN code that it returns for the vendor bank account includes spaces.</span></span> <span data-ttu-id="f20ca-193">Þess vegna er einingin **BankIBAN** skilgreind til að nota umbreytingu sniðs sem styttir bil.</span><span class="sxs-lookup"><span data-stu-id="f20ca-193">Therefore, the **BankIBAN** element is configured to use a format transformation that truncates spaces.</span></span>

6. <span data-ttu-id="f20ca-194">Lokið kembiforriti gagnagjafans.</span><span class="sxs-lookup"><span data-stu-id="f20ca-194">Close the data source debugger.</span></span>

### <a name="review-the-format-transformations"></a><span data-ttu-id="f20ca-195">Fara yfir umbreytingu sniðs</span><span class="sxs-lookup"><span data-stu-id="f20ca-195">Review the format transformations</span></span>

1. <span data-ttu-id="f20ca-196">Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.</span><span class="sxs-lookup"><span data-stu-id="f20ca-196">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="f20ca-197">Á síðunni **Grunnstillingar** skal velja **Greiðslulíkan** \> **ISO20022 Kreditfærsla**.</span><span class="sxs-lookup"><span data-stu-id="f20ca-197">On the **Configurations** page, select **Payment model** \> **ISO20022 Credit transfer**.</span></span>
3. <span data-ttu-id="f20ca-198">Veldu **Hönnuður** og víkkaðu svo einingarnar til að velja **Skjal** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN**.</span><span class="sxs-lookup"><span data-stu-id="f20ca-198">Select **Designer**, and then expand the elements to select **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN**.</span></span>

    ![BankIBAN eining á síðunni Sniðshönnuður](./media/er-data-debugger-referred-transformation.png)

    <span data-ttu-id="f20ca-200">Eins og sjá má er einingin **BankIBAN** skilgreind til að nota umbreytinguna **fjarlægja það sem er ekki bók- eða tölustafir**.</span><span class="sxs-lookup"><span data-stu-id="f20ca-200">As you can see, the **BankIBAN** element is configured to use the **remove not alphanumeric** transformation.</span></span>

4. <span data-ttu-id="f20ca-201">Veljið flipann **Umbreytingar**.</span><span class="sxs-lookup"><span data-stu-id="f20ca-201">Select the **Transformations** tab.</span></span>

    ![Umbreytingarflipi fyrir eininguna BankIBAN](./media/er-data-debugger-transformation.png)

    <span data-ttu-id="f20ca-203">Eins og sjá má er umbreytingin **fjarlægja það sem er ekki bók- eða tölustafir** skilgreind til að nota segð sem styttir bil í textastrengnum sem gefinn er upp.</span><span class="sxs-lookup"><span data-stu-id="f20ca-203">As you can see, the **remove not alphanumeric** transformation is configured to use an expression that truncates spaces from the text string that is provided.</span></span>

## <a name="start-to-debug-in-the-operation-designer"></a><span data-ttu-id="f20ca-204">Hefja kembingu í aðgerðarhönnuði</span><span class="sxs-lookup"><span data-stu-id="f20ca-204">Start to debug in the Operation designer</span></span>

<span data-ttu-id="f20ca-205">Þegar skilgreind eru útgáfudrög að sniði rafrænnar skýrslugerðar sem hægt er að keyra beint úr aðgerðarhönnuði, er hægt að fá aðgang að kembiforriti gagnagjafans með því að velja **Hefja kembingu** í aðgerðasvæðinu.</span><span class="sxs-lookup"><span data-stu-id="f20ca-205">When you configure a draft version of the ER format that can be run directly from the Operation designer, you can access the data source debugger by selecting **Start Debugging** on the Action Pane.</span></span>

![Ræsihnappur kembingar á síðu aðgerðarhönnuðar](./media/er-data-debugger-run-from-designer.png)

<span data-ttu-id="f20ca-207">Sniðsvörpun og sniðþættir í sniði rafrænnar skýrslugerðar sem verið er að breyta eru tiltækir fyrir kembingu.</span><span class="sxs-lookup"><span data-stu-id="f20ca-207">The format mapping and format components of the ER format that is being edited are available for debugging.</span></span>

## <a name="start-to-debug-in-the-model-mapping-designer"></a><span data-ttu-id="f20ca-208">Hefja kembingu í hönnuði líkanavörpunar</span><span class="sxs-lookup"><span data-stu-id="f20ca-208">Start to debug in the Model mapping designer</span></span>

<span data-ttu-id="f20ca-209">Þegar skilgreind er líkanavörpun rafrænnar skýrslugerðar sem hægt er að keyra á síðunni **Líkanavörpun**, er hægt að fá aðgang að kembiforriti gagnagjafans með því að velja **Hefja kembingu** á aðgerðasvæðinu.</span><span class="sxs-lookup"><span data-stu-id="f20ca-209">When you configure an ER model mapping that can be run from the **Model mapping** page, you can access the data source debugger by selecting **Start Debugging** on the Action Pane.</span></span>

![Ræsihnappur fyrir kembingu á hönnunarsíðu líkanavörpunar](./media/er-data-debugger-run-from-designer-mapping.png)

<span data-ttu-id="f20ca-211">Líkanavörpunaríhlutur vörpunar rafrænnar skýrslugerðar sem verið er að breyta er tiltækur fyrir kembingu.</span><span class="sxs-lookup"><span data-stu-id="f20ca-211">The model mapping component of the ER mapping that is being edited is available for debugging.</span></span>

## <a name="appendix-1-get-an-er-solution"></a><a name="appendix1"></a><span data-ttu-id="f20ca-212">Viðauki 1: Sækja lausn rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="f20ca-212">Appendix 1: Get an ER solution</span></span>

### <a name="download-an-er-solution"></a><span data-ttu-id="f20ca-213">Sækja lausn rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="f20ca-213">Download an ER solution</span></span>

<span data-ttu-id="f20ca-214">Ef ætlunin er að nota lausn rafrænnar skýrslugerðar til að búa til rafræna greiðsluskrá fyrir lánardrottnagreiðslu sem unnið er úr, er hægt að [sækja](download-electronic-reporting-configuration-lcs.md) greiðslusnið **ISO20022-kreditfærsla** rafrænnar skýrslugerðar sem er í boði í samnýttu eignasafni í Microsoft Dynamics Lifecycle Services (LCS) eða í Altæku geymslunni.</span><span class="sxs-lookup"><span data-stu-id="f20ca-214">If you want to use an ER solution to generate an electronic payment file for a vendor payment that is processed, you can [download](download-electronic-reporting-configuration-lcs.md) the **ISO20022 Credit transfer** ER payment format that is available from the Shared asset library in Microsoft Dynamics Lifecycle Services (LCS) or from the Global repository.</span></span>

![Innflutningur greiðslusniðs rafrænnar skýrslugerðar á síðu skilgreiningageymslu](./media/er-data-debugger-import-from-repo.png)

<span data-ttu-id="f20ca-216">Til viðbótar við valið snið rafrænnar skýrslugerðar verða eftirfarandi [skilgreiningar](general-electronic-reporting.md#Configuration) að vera sjálfkrafa fluttar inn í Microsoft Dynamics 365 Finance tilvikið sem hluti af lausn **ISO20022-kreditfærslu** rafrænnar skýrslugerðar:</span><span class="sxs-lookup"><span data-stu-id="f20ca-216">In addition to the selected ER format, the following [configurations](general-electronic-reporting.md#Configuration) must be automatically imported into your Microsoft Dynamics 365 Finance instance as part of the **ISO20022 Credit transfer** ER solution:</span></span>

- <span data-ttu-id="f20ca-217">**Greiðslulíkan** [Skilgreining gagnalíkans rafrænnar skýrslugerðar](general-electronic-reporting.md#DataModelComponent)</span><span class="sxs-lookup"><span data-stu-id="f20ca-217">**Payment model** [ER data model configuration](general-electronic-reporting.md#DataModelComponent)</span></span>
- <span data-ttu-id="f20ca-218">**ISO20022 Kreditfærsla** [grunnstilling sniðs rafrænnar skýrslugerðar](general-electronic-reporting.md#FormatComponentOutbound)</span><span class="sxs-lookup"><span data-stu-id="f20ca-218">**ISO20022 Credit transfer** [ER format configuration](general-electronic-reporting.md#FormatComponentOutbound)</span></span>
- <span data-ttu-id="f20ca-219">**Vörpun greiðslulíkans 1611** [Skilgreining líkanavörpunar rafrænnar skýrslugerðar](general-electronic-reporting.md#ModelMappingComponent)</span><span class="sxs-lookup"><span data-stu-id="f20ca-219">**Payment model mapping 1611** [ER model mapping configuration](general-electronic-reporting.md#ModelMappingComponent)</span></span>
- <span data-ttu-id="f20ca-220">**Vörpun greiðslulíkans í viðtökustað ISO20022** Skilgreining líkanavörpunar rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="f20ca-220">**Payment model mapping to destination ISO20022** ER model mapping configuration</span></span>

<span data-ttu-id="f20ca-221">Hægt er að finna þessar skilgreiningar á síðunni **Skilgreiningar** fyrir ramma rafrænnar skýrslugerðar (**Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**).</span><span class="sxs-lookup"><span data-stu-id="f20ca-221">You can find these configurations on the **Configurations** page of the ER framework (**Organization administration** \> **Electronic reporting** \> **Configurations**).</span></span>

![Skilgreiningar fluttar inn á síðunni Skilgreiningar](./media/er-data-debugger-configurations.png)

<span data-ttu-id="f20ca-223">Ef einhverjar fyrri uppgefnar skilgreiningar vantar í skilgreiningartrénu þarf að hlaða þeim niður handvirkt úr samnýttu eignasafni LCS á sama hátt og greiðslusnið **ISO20022-kreditfærslu** rafrænnar skýrslugerðar var hlaðið niður.</span><span class="sxs-lookup"><span data-stu-id="f20ca-223">If any of the previously listed configurations are missing in the configuration tree, you must manually download them from the LCS Shared asset library in the same way that you downloaded the **ISO20022 Credit transfer** ER payment format.</span></span>

### <a name="analyze-the-downloaded-er-solution"></a><span data-ttu-id="f20ca-224">Greina sótta lausn rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="f20ca-224">Analyze the downloaded ER solution</span></span>

#### <a name="review-the-model-mapping"></a><span data-ttu-id="f20ca-225">Fara yfir líkanavörpun</span><span class="sxs-lookup"><span data-stu-id="f20ca-225">Review the model mapping</span></span>

1. <span data-ttu-id="f20ca-226">Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.</span><span class="sxs-lookup"><span data-stu-id="f20ca-226">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="f20ca-227">Veljið **Greiðslulíkan** \> **Vörpun greiðslulíkans 1611**.</span><span class="sxs-lookup"><span data-stu-id="f20ca-227">Select **Payment model** \> **Payment model mapping 1611**.</span></span>
3. <span data-ttu-id="f20ca-228">Veljið **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="f20ca-228">Select **Designer**.</span></span>
4. <span data-ttu-id="f20ca-229">Veljið vörpunarfærsluna **Greiðslulíkanavörpun ISO20022 CT**.</span><span class="sxs-lookup"><span data-stu-id="f20ca-229">Select the **Payment model mapping ISO20022 CT** mapping record.</span></span>
5. <span data-ttu-id="f20ca-230">Veljið **Hönnuður** og farið yfir líkanavörpun sem er opin.</span><span class="sxs-lookup"><span data-stu-id="f20ca-230">Select **Designer**, and then review the model mapping that is opened.</span></span>

    <span data-ttu-id="f20ca-231">Takið eftir því að reiturinn **Greiðslur** í gagnalíkaninu er bundinn gagnagjafanum **\$notSentTransactions** sem skilar lista yfir greiðslulínur lánardrottna sem verið er að vinna úr.</span><span class="sxs-lookup"><span data-stu-id="f20ca-231">Notice that the **Payments** field of the data model is bound to the **\$notSentTransactions** data source that returns the list of vendor payment lines that are being processed.</span></span>

    ![Greiðslureitur á síðunni Hönnuður líkanavörpunar](./media/er-data-debugger-model-mapping.png)

#### <a name="review-the-format-mapping"></a><span data-ttu-id="f20ca-233">Fara yfir vörpun sniðs</span><span class="sxs-lookup"><span data-stu-id="f20ca-233">Review the format mapping</span></span>

1. <span data-ttu-id="f20ca-234">Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.</span><span class="sxs-lookup"><span data-stu-id="f20ca-234">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="f20ca-235">Veljið **Greiðslulíkan** \> **ISO20022 kreditfærsla**.</span><span class="sxs-lookup"><span data-stu-id="f20ca-235">Select **Payment model** \> **ISO20022 Credit transfer**.</span></span>
3. <span data-ttu-id="f20ca-236">Veljið **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="f20ca-236">Select **Designer**.</span></span>
4. <span data-ttu-id="f20ca-237">Í flipanum **Vörpun** skal fara yfir sniðsvörpunina sem er opin.</span><span class="sxs-lookup"><span data-stu-id="f20ca-237">On the **Mapping** tab, review the format mapping that is opened.</span></span>

    <span data-ttu-id="f20ca-238">Takið eftir að **Skjal** \> **CstmrCdtTrfInitn** \> **PmtInf** eining **ISO20022CTReports** \> **XMLHeader** skrárinnar tengist **\$PaymentByDebtor** gagnagjafa sem er stilltur í hópfærslur á reitnum **Greiðslur** í gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="f20ca-238">Notice that the **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** element of the **ISO20022CTReports** \> **XMLHeader** file is bound to the **\$PaymentByDebtor** data source that is configured to group records of the data model's **Payments** field.</span></span>

    ![PmtInf-eining á síðunni Sniðshönnuður](./media/er-data-debugger-format-mapping.png)

#### <a name="review-the-format"></a><span data-ttu-id="f20ca-240">Yfirfara snið</span><span class="sxs-lookup"><span data-stu-id="f20ca-240">Review the format</span></span>

1. <span data-ttu-id="f20ca-241">Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.</span><span class="sxs-lookup"><span data-stu-id="f20ca-241">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="f20ca-242">Veljið **Greiðslulíkan** \> **ISO20022 kreditfærsla**.</span><span class="sxs-lookup"><span data-stu-id="f20ca-242">Select **Payment model** \> **ISO20022 Credit transfer**.</span></span>
3. <span data-ttu-id="f20ca-243">Veljið **Hönnuður** og farið yfir sniðið sem er opið.</span><span class="sxs-lookup"><span data-stu-id="f20ca-243">Select **Designer**, and then review the format that is opened.</span></span>

    <span data-ttu-id="f20ca-244">Takið eftir að sniðsstillingin undir **Skjal** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN** er stillt á að setja inn IBAN-númer reiknings lánardrottins í greiðsluskrána.</span><span class="sxs-lookup"><span data-stu-id="f20ca-244">Notice that the format element under **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN** is configured to enter the IBAN code of the vendor account in the payment file.</span></span>

    ![BankIBAN eining á síðunni Sniðshönnuður](./media/er-data-debugger-format.png)

## <a name="appendix-2-configure-accounts-payable"></a><a name="appendix2"></a><span data-ttu-id="f20ca-246">Viðauki 2: Skilgreina Viðskiptaskuldir</span><span class="sxs-lookup"><span data-stu-id="f20ca-246">Appendix 2: Configure Accounts payable</span></span>

### <a name="modify-a-vendor-property"></a><span data-ttu-id="f20ca-247">Breyta eiginleika lánardrottins</span><span class="sxs-lookup"><span data-stu-id="f20ca-247">Modify a vendor property</span></span>

1. <span data-ttu-id="f20ca-248">Farið í **Viðskiptaskuldir** \> **Lánardrottnar** \> **Allir lánardrottnar**.</span><span class="sxs-lookup"><span data-stu-id="f20ca-248">Go to **Accounts payable** \> **Vendors** \> **All vendors**.</span></span>
2. <span data-ttu-id="f20ca-249">Velja skal lánardrottin **DE-01002** og síðan, á aðgerðasvæðinu, í flipanum **Lánardrottinn**, í flokknum **Uppsetning**, skal velja **Bankareikningar**.</span><span class="sxs-lookup"><span data-stu-id="f20ca-249">Select vendor **DE-01002**, and then, on the Action Pane, on the **Vendor** tab, in the **Set up** group, select **Bank accounts**.</span></span>
3. <span data-ttu-id="f20ca-250">Á flipanum **Auðkenni** í reitnum **IBAN** <a name="enteredIBANcode"></a>skal slá inn **GB33 BUKB 2020 1555 5555 55**.</span><span class="sxs-lookup"><span data-stu-id="f20ca-250">On the **Identification** FastTab, in the **IBAN** field, <a name="enteredIBANcode"></a>enter **GB33 BUKB 2020 1555 5555 55**.</span></span>
4. <span data-ttu-id="f20ca-251">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="f20ca-251">Select **Save**.</span></span>

![IBAN-reitur stilltur á bankareikningssíðu lánardrottins](./media/er-data-debugger-iban.png)

### <a name="set-up-a-method-of-payment"></a><span data-ttu-id="f20ca-253">Setja upp greiðslumáta</span><span class="sxs-lookup"><span data-stu-id="f20ca-253">Set up a method of payment</span></span>

1. <span data-ttu-id="f20ca-254">Farið í **Viðskiptaskuldir** \> **Greiðsluuppsetning** \> **Greiðsluháttur**.</span><span class="sxs-lookup"><span data-stu-id="f20ca-254">Go to **Accounts payable** \> **Payment setup** \> **Methods of payment**.</span></span>
2. <span data-ttu-id="f20ca-255">Veljið greiðslumátann **SEPA CT**.</span><span class="sxs-lookup"><span data-stu-id="f20ca-255">Select the **SEPA CT** payment method.</span></span>
3. <span data-ttu-id="f20ca-256">Í flipanum **Skráasnið**, í hlutanum **Skráasnið**, skal stilla valkostinn **Almennt rafrænt útflutningssnið** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="f20ca-256">On the **File formats** FastTab, in the **File formats** section, set the **Generic electronic Export format** option to **Yes**.</span></span>
4. <span data-ttu-id="f20ca-257">Í **Útflutningssnið skilgreiningarsvæðinu** skal velja **ISO20022 Kreditfærsla** snið fyrir rafræna skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="f20ca-257">In the **Export format configuration** field, select the **ISO20022 Credit transfer** ER format.</span></span>
5. <span data-ttu-id="f20ca-258">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="f20ca-258">Select **Save**.</span></span>

![Stillingar skráarsniðs á síðunni Greiðsluháttur](./media/er-data-debugger-payment-method.png)

### <a name="add-a-vendor-payment"></a><span data-ttu-id="f20ca-260">Bæta við greiðslu lánardrottins</span><span class="sxs-lookup"><span data-stu-id="f20ca-260">Add a vendor payment</span></span>

1. <span data-ttu-id="f20ca-261">Farið í **Viðskiptaskuldir** \> **Greiðslur** \> **Greiðslubók lánardrottins**.</span><span class="sxs-lookup"><span data-stu-id="f20ca-261">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="f20ca-262">Bæta við nýrri greiðslubók.</span><span class="sxs-lookup"><span data-stu-id="f20ca-262">Add a new payment journal.</span></span>
3. <span data-ttu-id="f20ca-263">Veldu **Línur** og bættu við nýrri greiðslulínu.</span><span class="sxs-lookup"><span data-stu-id="f20ca-263">Select **Lines**, and add a new payment line.</span></span>
4. <span data-ttu-id="f20ca-264">Í reitnum **Reikningur** velurðu lánardrottinn **DE-01002**.</span><span class="sxs-lookup"><span data-stu-id="f20ca-264">In the **Account** field, select vendor **DE-01002**.</span></span>
5. <span data-ttu-id="f20ca-265">Í reitnum **Debet** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="f20ca-265">In the **Debit** field, enter a value.</span></span>
6. <span data-ttu-id="f20ca-266">Í reitnum **Greiðsluháttur** skal velja **SEPA CT**.</span><span class="sxs-lookup"><span data-stu-id="f20ca-266">In the **Method of payment** field, select **SEPA CT**.</span></span>
7. <span data-ttu-id="f20ca-267">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="f20ca-267">Select **Save**.</span></span>

![Lánardrottnagreiðslu bætt við síðu lánardrottnagreiðslna](./media/er-data-debugger-payment-journal.png)

## <a name="appendix-3-process-a-vendor-payment"></a><a name="appendix3"></a><span data-ttu-id="f20ca-269">Viðauki 3: Meðhöndla greiðslu lánardrottins</span><span class="sxs-lookup"><span data-stu-id="f20ca-269">Appendix 3: Process a vendor payment</span></span>

1. <span data-ttu-id="f20ca-270">Farið í **Viðskiptaskuldir** \> **Greiðslur** \> **Greiðslubók lánardrottins**.</span><span class="sxs-lookup"><span data-stu-id="f20ca-270">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="f20ca-271">Á síðunni **Greiðslubók lánardrottins** skal velja þá greiðslubók sem var áður stofnuð og síðan velja **Línur**.</span><span class="sxs-lookup"><span data-stu-id="f20ca-271">On the **Vendor payment journal** page, select the payment journal that you previously created, and then select **Lines**.</span></span>
3. <span data-ttu-id="f20ca-272">Veljið greiðslulínuna og svo **Greiðslustaða** \> **Engin**.</span><span class="sxs-lookup"><span data-stu-id="f20ca-272">Select the payment line, and then select **Payment status** \> **None**.</span></span>
4. <span data-ttu-id="f20ca-273">Veldu **Búa til greiðslur**.</span><span class="sxs-lookup"><span data-stu-id="f20ca-273">Select **Generate payments**.</span></span>
5. <span data-ttu-id="f20ca-274">Í reitnum **Greiðsluháttur** skal velja **SEPA CT**.</span><span class="sxs-lookup"><span data-stu-id="f20ca-274">In the **Method of payment** field, select **SEPA CT**.</span></span>
6. <span data-ttu-id="f20ca-275">Í reitnum **Bankareikningur** skal velja **DEMF OPER**.</span><span class="sxs-lookup"><span data-stu-id="f20ca-275">In the **Bank account** field, select **DEMF OPER**.</span></span>
7. <span data-ttu-id="f20ca-276">Í svarglugganum **Búa til greiðslur** skal velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="f20ca-276">In the **Generate payments** dialog box, select **OK**.</span></span>
8. <span data-ttu-id="f20ca-277">Í **Svargluggi rafrænna skýrslufæribreyta** velurðu **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="f20ca-277">In the **Electronic report parameters** dialog box, select **OK**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]