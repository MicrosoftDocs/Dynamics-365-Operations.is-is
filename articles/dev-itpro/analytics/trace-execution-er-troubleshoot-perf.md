<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="trace-execution-er-troubleshoot-perf.md" target-language="is-is">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>trace-execution-er-troubleshoot-perf.773b92.aa71db2752889bc905c22bab1cf2fa46d7ee07c7.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>aa71db2752889bc905c22bab1cf2fa46d7ee07c7</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>67d00b95952faf0db580d341249d4e50be59119c</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\analytics\trace-execution-er-troubleshoot-perf.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Trace execution of ER format to troubleshoot performance issues</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Rekja framkvæmd á sniði rafrænnar skýrslugerðar til að úrræðaleita vandamál sem tengjast afköstum</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic provides information about how to use the performance trace feature in Electronic reporting (ER) to troubleshoot performance issues.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Þetta efnisatriði veitir upplýsingar um hvernig á að nota eiginleika fyrir rakningu afkasta í rafrænni skýrslugerð til að úrræðaleita vandamál er varða afköst.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Trace the execution of ER formats to troubleshoot performance issues</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Rekja framkvæmd á sniðum rafrænnar skýrslugerðar til að úrræðaleita vandamál sem tengjast afköstum</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>As part of the process of designing Electronic reporting (ER) configurations to generate electronic documents, you define the method that is used to get data out of Microsoft Dynamics 365 for Finance and Operations and enter it in the output that is generated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Sem hluti af hönnunarferlinu fyrir skilgreiningar rafrænnar skýrslugerðar til að búa til rafræn skjöl, skilgreinir þú aðferðina sem er notuð til að ná í göng úr Microsoft Dynamics 365 for Finance and Operations og færa þau inn í úttak sem er myndað.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>The ER performance trace feature helps significantly reduce the time and cost that are involved in collecting the details of ER format execution and using them to troubleshoot performance issues.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Eiginleikinn fyrir rakningu á afköstum rafrænnar skýrslugerðar auðveldar að draga umtalsvert úr tíma og kostnaði sem eru hluti af því að safna saman upplýsingum um framkvæmd rafrænnar skýrslugerðar og nota þau til að úrræðaleita vandamál er varða afköst.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>This tutorial provides guidelines about how to take performance traces for executed ER formats in Finance and Operations, and how to use the information from these traces to help improve performance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Þessi leiðsögn veitir leiðbeiningar um hvernig á að gera rakningar á afköstum fyrir snið rafrænnar skýrslugerðar sem eru keyrð í Finance and Operations og hvernig á að nota upplýsingarnar úr þessum rakningum til að hjálpa til við að bæta afköst.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Prerequisites</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Forkröfur</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>To complete the examples in this tutorial, you must have the following access:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Til að ljúka dæmunum í þessari leiðsögn þarftu að hafa eftirfarandi aðgang:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Access to Finance and Operations for one of the following roles:</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Aðgangur að Finance and Operations fyrir eitt af eftirtöldum hlutverkum:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Electronic reporting developer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Þróunaraðili rafrænnar skýrslulausnar</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Electronic reporting functional consultant</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>System administrator</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Kerfisstjóri</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Access to the instance of Regulatory Configuration Services (RCS) that has been provisioned for the same tenant as Finance and Operations, for one of the following roles:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Aðgang að tilviki Skilgreiningarþjónustu reglugerðar (RCS) sem hefur verið úthlutað fyrir sama leigjandann og fyrir Finance and Operations, fyrir eitt af eftirfarandi hlutverkum:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Electronic reporting developer</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Þróunaraðili rafrænnar skýrslulausnar</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Electronic reporting functional consultant</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>System administrator</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Kerfisstjóri</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>You must also download and locally store the following files.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Einnig verður að sækja og geyma staðbundið eftirfarandi skrár.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>File</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Skrá</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Content</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Efni</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Performance trace model.version.1</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Afkastarakning model.version.1</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source><bpt id="p1">[</bpt>Sample ER data model configuration<ept id="p1">](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Sýnishorn af skilgreiningu gagnalíkans rafrænnar skýrslugerðar<ept id="p1">](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Performance trace metadata.version.1</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Afkastarakning metadata.version.1</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source><bpt id="p1">[</bpt>Sample ER metadata configuration<ept id="p1">](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Sýnishorn af skilgreiningu lýsigagna rafrænnar skýrslugerðar<ept id="p1">](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Performance trace mapping.version.1.1</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Afkastarakning mapping.version.1.1</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source><bpt id="p1">[</bpt>Sample ER model mapping configuration<ept id="p1">](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Sýnishorn af skilgreiningu líkanavörpunar rafrænnar skýrslugerðar<ept id="p1">](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Performance trace format.version.1.1</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Afkastarakning format.version.1.1</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source><bpt id="p1">[</bpt>Sample ER format configuration<ept id="p1">](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Sýnishorn af skilgreiningu á sniði rafrænnar skýrslugerðar<ept id="p1">](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Configure ER parameters</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Skilgreina færibreytur Rafræn skýrslugerðar</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Each ER performance trace that is generated in Finance and Operations is stored as an attachment of the execution log record.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hver afkastarakning rafrænnar skýrslugerðar sem er búin til í Finance and Operations er geymd sem viðhengi skráar fyrir aðgerðarskráningu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>The Document management (DM) framework of Finance and Operations is used to manage these attachments.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Rammi skjalastjórnunar í Finance and Operations er notað til að stjórna þessum viðhengjum.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>You must configure ER parameters in advance, to specify the DM document type that should be used to attach performance traces.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Skilgreina verður færibreytur rafrænnar skýrslugerðar fyrirfram til að tilgreina skjalagerð skjalastjórnunar sem á að nota til að hengja afkastarakningar við.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>In Finance and Operation, in the <bpt id="p1">**</bpt>Electronic reporting<ept id="p1">**</ept> workspace, select <bpt id="p2">**</bpt>Electronic reporting parameters<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Í Finance and Operation, á vinnusvæðinu <bpt id="p1">**</bpt>Rafræn skýrslugerð<ept id="p1">**</ept> skal velja <bpt id="p2">**</bpt>Færibreytur rafrænnar skýrslugerðar<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Then, on the <bpt id="p1">**</bpt>Electronic reporting parameters<ept id="p1">**</ept> page, on the <bpt id="p2">**</bpt>Attachments<ept id="p2">**</ept> tab, in the <bpt id="p3">**</bpt>Others<ept id="p3">**</ept> field, select the DM document type to use for performance traces.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Síðan, á síðunni <bpt id="p1">**</bpt>Færibreytur rafrænnar skýrslugerðar<ept id="p1">**</ept>, í flipanum <bpt id="p2">**</bpt>Viðhengi<ept id="p2">**</ept>, í reitnum <bpt id="p3">**</bpt>Annað<ept id="p3">**</ept>, skal velja skjalagerð skjalastjórnunar til að nota fyrir afkastarakningar.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Electronic reporting parameters page in Finance and Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Síða rafrænna skýrslufæribreyta í Finance and Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>To be available in the <bpt id="p1">**</bpt>Others<ept id="p1">**</ept> lookup field, a DM document type must be configured in the following manner on the <bpt id="p2">**</bpt>Document types<ept id="p2">**</ept> page (<bpt id="p3">**</bpt>Organization administration <ph id="ph1">\&gt;</ph> Document management <ph id="ph2">\&gt;</ph> Document types<ept id="p3">**</ept>):</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Til að vera tiltækt í uppflettingarreitnum <bpt id="p1">**</bpt>Annað<ept id="p1">**</ept> verður skjalagerð skjalastjórnunar að vera skilgreind á eftirfarandi hátt á síðunni <bpt id="p2">**</bpt>Skjalagerðir<ept id="p2">**</ept> (<bpt id="p3">**</bpt>Fyrirtækisstjórnun <ph id="ph1">\&gt;</ph> Skjalastjórnun <ph id="ph2">\&gt;</ph> Skjalagerðir<ept id="p3">**</ept>):</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source><bpt id="p1">**</bpt>Class:<ept id="p1">**</ept> Attach file</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Klasi:<ept id="p1">**</ept> Hengja skrá við</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source><bpt id="p1">**</bpt>Group:<ept id="p1">**</ept> File</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Flokkur:<ept id="p1">**</ept> Skrá</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Document types page in Finance and Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Síða skjalagerða í Finance and Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>The selected document type must be available in every company of the current Finance and Operations instance, because DM attachments are company-specific.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Valin skjalagerð verður að vera tiltæk í öllum fyrirtækjum í núverandi tilviki Finance and Operations vegna þess að viðhengi skjalastjórnunar miðast við fyrirtæki.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Configure RCS parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Skilgreina færibreytur RCS</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>ER performance traces that are generated in Finance and Operations will be imported into RCS for analysis by using the ER format designer and the ER mapping designer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Afkastarakningar rafrænnar skýrslugerðar sem eru myndaðar í Finance and Operations verða fluttar inn í RCS til greiningar með því að nota sniðshönnuð rafrænnar skýrslugerðar og hönnuð fyrir vörpun rafrænnar skýrslugerðar.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Because ER performance traces are stored as attachments of the execution log record that is related to the ER format, you must configure RCS parameters in advance, to specify the DM document type that should be used to attach performance traces.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Vegna þess að afkastarakningar rafrænnar skýrslugerðar eru geymdar sem viðhengi fyrir skrá aðgerðarskráningar sem tengist sniði rafrænnar skýrslugerðar er nauðsynlegt að skilgreina færibreytur RCS fyrirfram til að tilgreina skjalagerð skjalastjórnunar sem á að nota til að hengja afkastarakningar við.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>In the instance of RCS that has been provisioned for your company, in the <bpt id="p1">**</bpt>Electronic reporting<ept id="p1">**</ept> workspace, select <bpt id="p2">**</bpt>Electronic reporting parameters<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Í tilfelli RCS sem hefur verið úthlutað fyrir fyrirtækið þitt, á vinnusvæðinu <bpt id="p1">**</bpt>Rafræn skýrslugerð<ept id="p1">**</ept>, skal velja <bpt id="p2">**</bpt>Rafrænar skýrslugerðarfæribreytur<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Then, on the <bpt id="p1">**</bpt>Electronic reporting parameters<ept id="p1">**</ept> page, on the <bpt id="p2">**</bpt>Attachments<ept id="p2">**</ept> tab, in the <bpt id="p3">**</bpt>Others<ept id="p3">**</ept> field, select the DM document type to use for performance traces.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">Síðan, á síðunni <bpt id="p1">**</bpt>Færibreytur rafrænnar skýrslugerðar<ept id="p1">**</ept>, í flipanum <bpt id="p2">**</bpt>Viðhengi<ept id="p2">**</ept>, í reitnum <bpt id="p3">**</bpt>Annað<ept id="p3">**</ept>, skal velja skjalagerð skjalastjórnunar til að nota fyrir afkastarakningar.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>Electronic reporting parameters page in RCS</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Síða rafrænna skýrslugerðarfæribreyta í RCS</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>To be available in the <bpt id="p1">**</bpt>Others<ept id="p1">**</ept> lookup field, a DM document type must be configured in the following manner on the <bpt id="p2">**</bpt>Document types<ept id="p2">**</ept> page (<bpt id="p3">**</bpt>Organization administration <ph id="ph1">\&gt;</ph> Document management <ph id="ph2">\&gt;</ph> Document types<ept id="p3">**</ept>):</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">Til að vera tiltækt í uppflettingarreitnum <bpt id="p1">**</bpt>Annað<ept id="p1">**</ept> verður skjalagerð skjalastjórnunar að vera skilgreind á eftirfarandi hátt á síðunni <bpt id="p2">**</bpt>Skjalagerðir<ept id="p2">**</ept> (<bpt id="p3">**</bpt>Fyrirtækisstjórnun <ph id="ph1">\&gt;</ph> Skjalastjórnun <ph id="ph2">\&gt;</ph> Skjalagerðir<ept id="p3">**</ept>):</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source><bpt id="p1">**</bpt>Class:<ept id="p1">**</ept> Attach file</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Klasi:<ept id="p1">**</ept> Hengja skrá við</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source><bpt id="p1">**</bpt>Group:<ept id="p1">**</ept> File</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Flokkur:<ept id="p1">**</ept> Skrá</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Design an ER solution</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hanna lausn rafrænnar skýrslugerðar</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Assume that you've started to design a new ER solution to generate a new report that presents vendor transactions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Gerum ráð fyrir að þú hafir byrjað að hanna nýja lausn rafrænnar skýrslugerðar til að búa til nýja skýrslu sem sýnir lánardrottnafærslur.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>Currently, you can find the transactions for a selected vendor on the <bpt id="p1">**</bpt>Vendor transactions<ept id="p1">**</ept> page (go to <bpt id="p2">**</bpt>Account payable <ph id="ph1">\&gt;</ph> Vendors <ph id="ph2">\&gt;</ph> All vendors<ept id="p2">**</ept>, select a vendor, and then, on the Action Pane, on the <bpt id="p3">**</bpt>Vendor<ept id="p3">**</ept> tab, in the <bpt id="p4">**</bpt>Transactions<ept id="p4">**</ept> group, select <bpt id="p5">**</bpt>Transactions<ept id="p5">**</ept>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Eins og er geturðu fundið færslurnar fyrir valinn lánardrottin á síðunni <bpt id="p1">**</bpt>Lánardrottnafærslur<ept id="p1">**</ept> (opnaðu <bpt id="p2">**</bpt>Viðskiptaskuldir <ph id="ph1">\&gt;</ph> Lánardrottnar <ph id="ph2">\&gt;</ph> Allir lánardrottnar<ept id="p2">**</ept>, veldu lánardrottin og síðan, í aðgerðarúðunni, í flipanum <bpt id="p3">**</bpt>Lánardrottinn<ept id="p3">**</ept>, í flokknum <bpt id="p4">**</bpt>Færslur<ept id="p4">**</ept>, skal velja <bpt id="p5">**</bpt>Færslur<ept id="p5">**</ept>).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>However, you want to have all vendor transaction at the same time in one electronic document in XML format.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hins vegar viltu hafa allar lánardrottnafærslur á sama tíma í einu rafrænu skjali á XML-sniði.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>This solution will consist of several ER configurations that contain the required data model, metadata, model mapping, and format components.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Þessi lausn mun samanstanda af nokkrum skilgreiningum rafrænnar skýrslugerðar sem innihalda nauðsynlegt gagnalíkan, lýsigögn, líkanavörpun og sniðseiningar.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Sign in to the instance of RCS that has been provisioned for your company.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Skráðu þig inn á tilvik RCS sem hefur verið úthlutað fyrir fyrirtækið þitt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>In this tutorial, you will create and modify configurations for the <bpt id="p1">**</bpt>Litware, Inc.<ept id="p1">**</ept> sample company.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Í þessari leiðsögn býrðu til og breytir skilgreiningum fyrir sýnifyrirtækið <bpt id="p1">**</bpt>Litware, Inc.<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Therefore, make sure that this configuration provider has been added to RCS and selected as active.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Gakktu því úr skugga um að þessari skilgreiningarveitu hafi verið bætt við RCS og verið valin sem virk.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>For instructions, see the <bpt id="p1">[</bpt>Create configuration providers and mark them as active<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11)</ept> procedure.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Fyrir leiðbeiningar skal sjá ferlið <bpt id="p1">[</bpt>Stofna skilgreiningarveitendur og merkja þá sem virka<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11)</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>In the <bpt id="p1">**</bpt>Electronic reporting<ept id="p1">**</ept> workspace, select the <bpt id="p2">**</bpt>Reporting configurations<ept id="p2">**</ept> tile.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Á vinnusvæðinu <bpt id="p1">**</bpt>Rafræn skýrslugerð<ept id="p1">**</ept> skal velja reitinn <bpt id="p2">**</bpt>Skilgreiningar skýrslugerðar<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>On the <bpt id="p1">**</bpt>Configurations<ept id="p1">**</ept> page, import the ER configurations that you downloaded as a prerequisite into RCS, in the following order: data model, metadata, model mapping, format.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Á síðunni <bpt id="p1">**</bpt>Skilgreiningar<ept id="p1">**</ept>, skal flytja inn skilgreiningar rafrænnar skýrslugerðar sem voru sóttar sem forkröfur í RCS, í eftirfarandi röð: gagnalíkan, lýsigögn, líkanavörpun, snið.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>For each configuration, follow these steps:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Fyrir hverja skilgreiningu skal fylgja þessum skrefum:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>On the Action Pane, select <bpt id="p1">**</bpt>Exchange <ph id="ph1">\&gt;</ph> Load from XML file<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Í aðgerðarúðunni skal velja <bpt id="p1">**</bpt>Skipta út <ph id="ph1">\&gt;</ph> Hlaða úr XML-skrá<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Select <bpt id="p1">**</bpt>Browse<ept id="p1">**</ept> to select the appropriate file for the required ER configuration in XML format.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Veljið <bpt id="p1">**</bpt>Vafra<ept id="p1">**</ept> til að velja viðeigandi skrá fyrir nauðsynlega skilgreiningu rafrænnar skýrslugerðar á XML-sniði.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Select <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Veljið <bpt id="p1">**</bpt>Í lagi<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>Configurations page in RCS</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Skilgreiningarsíða í RCS</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>Run the ER solution to trace execution</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Keyra lausn rafrænnar skýrslugerðar til að rekja framkvæmd</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Assume that you've finished designing the first version of the ER solution.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Gerum ráð fyrir að þú hafir lokið við að hanna fyrstu útgáfu af lausn rafrænnar skýrslugerðar.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>You now want to test it in your Finance and Operations instance and analyze execution performance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Núna viltu prófa hana í tilviki Finance and Operations og greina afköst keyrslu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source><bpt id="p1">&lt;a id='import-configuration'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>Import an ER configuration from RCS into Finance and Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;a id='import-configuration'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>Flytja inn skilgreiningu rafrænnar skýrslugerðar úr RCS í Finance and Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>Sign in to your Finance and Operations instance.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Skráðu þig in í tilvik Finance and Operations.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>For this tutorial, you will import configurations from your RCS instance (where you design your ER components) into your Finance and Operations instance (where you test and finally use them).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Fyrir þessa leiðsögn flytur þú inn skilgreiningar úr RCS-tilvikinu þínu (þar sem þú hannar þætti rafrænnar skýrslugerðar) í tilvik Finance and Operations (þar sem þú prófar og að lokum notar þær).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>Therefore, you must make sure that all the required artifacts have been prepared.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Þess vegna verður þú að ganga úr skugga um að allir nauðsynlegir gervingar hafi verið undirbúnir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>For instructions, see the <bpt id="p1">[</bpt>Import Electronic reporting (ER) configurations from Regulatory Configuration Services (RCS)<ept id="p1">](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/rcs-download-configurations)</ept> procedure.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Til að fá leiðbeiningar skal sjá ferlið <bpt id="p1">[</bpt>Flytja inn skilgreiningar rafrænnar skýrslugerðar úr Skilgreiningarþjónustu reglugerðar (RCS)<ept id="p1">](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/rcs-download-configurations)</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Follow these steps to import the configurations from RCS into Finance and Operations:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Fylgið þessum skrefum til að flytja inn skilgreiningar úr RCS í Finance and Operations:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>In the <bpt id="p1">**</bpt>Electronic reporting<ept id="p1">**</ept> workspace, on the tile for the <bpt id="p2">**</bpt>Litware, Inc.<ept id="p2">**</ept> configuration provider, select <bpt id="p3">**</bpt>Repositories<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Á vinnusvæðinu <bpt id="p1">**</bpt>Rafræn skýrslugerð<ept id="p1">**</ept>, í reitnum fyrir skilgreiningarveituna <bpt id="p2">**</bpt>Litware, Inc.<ept id="p2">**</ept>, skal velja <bpt id="p3">**</bpt>Geymslur<ept id="p3">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>On the <bpt id="p1">**</bpt>Configuration repository<ept id="p1">**</ept> page, select the repository of the <bpt id="p2">**</bpt>RCS<ept id="p2">**</ept> type, and then select <bpt id="p3">**</bpt>Open<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Á síðunni <bpt id="p1">**</bpt>Skilgreiningageymsla<ept id="p1">**</ept> skal velja geymslu af gerðinni <bpt id="p2">**</bpt>RCS<ept id="p2">**</ept> og síðan velja <bpt id="p3">**</bpt>Opna<ept id="p3">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>On the <bpt id="p1">**</bpt>Configurations<ept id="p1">**</ept> FastTab, select the <bpt id="p2">**</bpt>Performance trace format<ept id="p2">**</ept> configuration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Í flýtiflipanum <bpt id="p1">**</bpt>Skilgreiningar<ept id="p1">**</ept> skal velja skilgreininguna <bpt id="p2">**</bpt>Snið afkastarakningar<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>On the <bpt id="p1">**</bpt>Versions<ept id="p1">**</ept> FastTab, select version <bpt id="p2">**</bpt>1.1<ept id="p2">**</ept> of the selected configuration, and then select <bpt id="p3">**</bpt>Import<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Í flýtiflipanum <bpt id="p1">**</bpt>Útgáfur<ept id="p1">**</ept> skal velja útgáfuna <bpt id="p2">**</bpt>1.1<ept id="p2">**</ept> af valdri skilgreiningu og síðan velja <bpt id="p3">**</bpt>Flytja inn<ept id="p3">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>Configuration repository page in Finance and Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Síða skilgreiningageymslu í Finance and Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>The corresponding versions of the data model and model mapping configurations are automatically imported as prerequisites for the imported ER format configuration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Samsvarandi útgáfur af skilgreiningum gagnalíkans og líkanavörpunar eru fluttar inn sjálfvirkt sem forkröfur fyrir innflutta skilgreiningu á sniði rafrænnar skýrslugerðar.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>Turn on the ER performance trace</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kveikja á afkastarakningu rafrænnar skýrslugerðar</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>In Finance and Operations, go to <bpt id="p1">**</bpt>Organization administration <ph id="ph1">\&gt;</ph> Electronic reporting <ph id="ph2">\&gt;</ph> Configurations<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Í Finance and Operations skal opna <bpt id="p1">**</bpt>Fyrirtækisstjórnun <ph id="ph1">\&gt;</ph> Rafræn skýrslugerð <ph id="ph2">\&gt;</ph> Skilgreiningar<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>On the <bpt id="p1">**</bpt>Configurations<ept id="p1">**</ept> page, on the Action Pane, on the <bpt id="p2">**</bpt>Configurations<ept id="p2">**</ept> tab, in the <bpt id="p3">**</bpt>Advanced settings<ept id="p3">**</ept> group, select <bpt id="p4">**</bpt>User parameters<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Á síðunni <bpt id="p1">**</bpt>Skilgreiningar<ept id="p1">**</ept>, í aðgerðarúðunni, í flipanum <bpt id="p2">**</bpt>Skilgreiningar<ept id="p2">**</ept>, í flokknum <bpt id="p3">**</bpt>Ítarlegar stillingar<ept id="p3">**</ept>, skal velja <bpt id="p4">**</bpt>Færibreytur notanda<ept id="p4">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>In the <bpt id="p1">**</bpt>User parameters<ept id="p1">**</ept> dialog box, in the <bpt id="p2">**</bpt>Execution tracing<ept id="p2">**</ept> section, follow these steps:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Í svarglugganum <bpt id="p1">**</bpt>Færibreytur notanda<ept id="p1">**</ept>, í hlutanum <bpt id="p2">**</bpt>Rakning keyrslu<ept id="p2">**</ept>, skal fylgja þessum skrefum:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>In the <bpt id="p1">**</bpt>Execution trace format<ept id="p1">**</ept> field, select <bpt id="p2">**</bpt>Debug trace format<ept id="p2">**</ept> to start to collect the details of ER format execution.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Í reitnum <bpt id="p1">**</bpt>Snið framkvæmdarakningar<ept id="p1">**</ept> skal velja <bpt id="p2">**</bpt>Kemba rakningasnið<ept id="p2">**</ept> til að byrja að safna saman upplýsingum um framkvæmd á sniði rafrænnar skýrslugerðar.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>When this value is selected, the performance trace will collect information about the time that is spent on the following actions:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Þegar þetta gildi er valið safnar afkastarakningin upplýsingum um tímann sem eftirfarandi aðgerðir taka:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Running each data source in the model mapping that is called to get data</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Að keyra hvern gagnagjafa í líkanavörpuninni sem er kallað á til að ná í gögn</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>Processing each format item to enter data in the output that is generated</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Úrvinnsla á öllum sniðsatriðum til að færa gögn inn í frálagið sem myndast</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>You use the <bpt id="p1">**</bpt>Execution trace format<ept id="p1">**</ept> field to specify the format of the generated performance trace that the execution details are stored in for ER format and mapping elements.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Notaður er reiturinn <bpt id="p1">**</bpt>Snið framkvæmdarakningar<ept id="p1">**</ept> til að tilgreina snið fyrir myndaða afkastarakningu sem upplýsingar um framkvæmd eru geymdar í fyrir snið rafrænnar skýrslugerðar og einingar vörpunar.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>By selecting <bpt id="p1">**</bpt>Debug trace format<ept id="p1">**</ept> as the value, you will be able to analyze the content of the trace in ER Operation designer, and see the ER format or mapping elements that are mentioned in the trace.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Með því að velja <bpt id="p1">**</bpt>Kemba sniðsrakningu<ept id="p1">**</ept> sem gildið geturðu greint innihald rakningarinnar í aðgerðarhönnuði rafrænnar skýrslugerðar og séð snið rafrænnar skýrslugerðar eða einingar vörpunar sem minnst er á í rakningunni.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>Set the following options to <bpt id="p1">**</bpt>Yes<ept id="p1">**</ept> to collect specific details of the execution of the ER model mapping and ER format components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Stillið eftirfarandi valkosti á <bpt id="p1">**</bpt>Já<ept id="p1">**</ept> til að safna saman ákveðnum upplýsingum um framkvæmdina á líkanavörpun rafrænnar skýrslugerðar og sniðseiningum rafrænnar skýrslugerðar:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source><bpt id="p1">**</bpt>Collect query statistics<ept id="p1">**</ept> – When this option is turned on, the performance trace will collect the following information:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Safna saman tölfræði um fyrirspurnir<ept id="p1">**</ept> - Þegar kveikt er á þessum valkosti safnar afkastarakningin saman eftirfarandi upplýsingum:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>The number of database calls that were made by data sources</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Fjölda gagnagrunnsköllum sem voru gerð eftir gagnaveitum</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>The number of duplicate calls to the database</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Fjölda afrita af köllum á gagnagrunninn</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>Details of the SQL statements that were used to make database calls</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Upplýsingar um SQL-yrðingar sem voru notaðar til að gera gagnagrunnsköll</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source><bpt id="p1">**</bpt>Trace access of caching<ept id="p1">**</ept> – When this option is turned on, the performance trace will collect information about the ER model mapping's cache usage.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Rekja aðgang að skyndiminni<ept id="p1">**</ept> - Þegar kveikt er á þessum valkosti safnar afkastarakningin saman upplýsingum um notkun á skyndiminni líkanavörpunar rafrænnar skýrslugerðar.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source><bpt id="p1">**</bpt>Trace data access<ept id="p1">**</ept> – When this option is turned on, the performance trace will collect information about the number of calls to the database for executed data sources of the record list type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Rekja gagnaaðgang<ept id="p1">**</ept> - Þegar kveikt er á þessum valkosti safnar afkastarakningin saman upplýsingum um fjölda kalla á gagnagrunninn fyrir framkvæmdar gagnaveitur af færslulistagerðinni.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source><bpt id="p1">**</bpt>Trace list enumeration<ept id="p1">**</ept> – When this option is turned on, the performance trace will collect information about the number of records that are requested from data sources of the record list type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Rekja tölusetningarlista<ept id="p1">**</ept> - Þegar kveikt er á þessum valkosti safnar afkastarakningin saman upplýsingum um fjölda færslna sem gagnaveitur af færslulistagerðinni óska eftir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>The parameters in the <bpt id="p1">**</bpt>User parameters<ept id="p1">**</ept> dialog box are specific to the user and the current company.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Færibreyturnar í svarglugganum <bpt id="p1">**</bpt>Færibreytur notanda<ept id="p1">**</ept> eru sérstaklega fyrir notandann og núverandi fyrirtæki.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>User parameters dialog box in Finance and Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Nota svarglugga færibreyta í Finance and Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source><bpt id="p1">&lt;a id='run-format'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>Run the ER format</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;a id='run-format'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>Keyra snið rafrænnar skýrslugerðar</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>In Finance and Operations, select the <bpt id="p1">**</bpt>DEMF<ept id="p1">**</ept> company.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Í Finance and Operations skal velja fyrirtækið <bpt id="p1">**</bpt>DEMF<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>Go to <bpt id="p1">**</bpt>Organization administration <ph id="ph1">\&gt;</ph> Electronic reporting <ph id="ph2">\&gt;</ph> Configurations<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Opnið <bpt id="p1">**</bpt>Fyrirtækisstjórnun <ph id="ph1">\&gt;</ph> Rafræn skýrslugerð <ph id="ph2">\&gt;</ph> Skilgreiningar<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>On the <bpt id="p1">**</bpt>Configurations<ept id="p1">**</ept> page, in the configuration tree, select the <bpt id="p2">**</bpt>Performance trace format<ept id="p2">**</ept> item.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Á síðunni <bpt id="p1">**</bpt>Skilgreiningar<ept id="p1">**</ept>, í skilgreiningartrénu, skal velja atriðið <bpt id="p2">**</bpt>Snið afkastarakningar<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>On the Action Pane, select <bpt id="p1">**</bpt>Run<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Í aðgerðarúðunni skal velja <bpt id="p1">**</bpt>Keyra<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>Notice that the file that is generated presents information about 265 transactions for six vendors.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Takið eftir að skráin sem er búin til veitir upplýsingar um 265 færslur fyrir sex lánardrottna.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>Review the execution trace</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Yfirfara framkvæmdarakningu</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source><bpt id="p1">&lt;a id='export-trace'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>Export the generated trace from Finance and Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;a id='export-trace'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>Flytja út myndaða rakningu úr Finance and Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>Performance traces are decoupled from the source ER format and can be serialized to an external zip file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Afkastarakningar eru aftengdar frá upprunasniði rafrænnar skýrslugerðar og er hægt að númera við utanaðkomandi zip-skrá.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>In Finance and Operations, go to <bpt id="p1">**</bpt>Organization administration <ph id="ph1">\&gt;</ph> Electronic reporting <ph id="ph2">\&gt;</ph> Configuration debug logs<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Í Finance and Operations skal opna <bpt id="p1">**</bpt>Fyrirtækisstjórnun <ph id="ph1">\&gt;</ph> Rafræn skýrslugerð <ph id="ph2">\&gt;</ph> Kembingarkladdar skilgreiningar<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>On the <bpt id="p1">**</bpt>Electronic reporting run logs<ept id="p1">**</ept> page, in the left pane, in the <bpt id="p2">**</bpt>Configuration name<ept id="p2">**</ept> field, select <bpt id="p3">**</bpt>Performance trace format<ept id="p3">**</ept> to find the log records that have been generated by the execution of the <bpt id="p4">**</bpt>Performance trace format<ept id="p4">**</ept> configuration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Á síðunni <bpt id="p1">**</bpt>Keyrslukladdar rafrænnar skýrslugjafar<ept id="p1">**</ept>, í vinstri rúðunni, í reitnum <bpt id="p2">**</bpt>Heiti skilgreiningar<ept id="p2">**</ept>, skal velja <bpt id="p3">**</bpt>Snið afkastarakningar<ept id="p3">**</ept> til að finna kladdafærslur sem framkvæmdin hefur búið til í skilgreiningunni <bpt id="p4">**</bpt>Snið afkastarakningar<ept id="p4">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>Select the <bpt id="p1">**</bpt>Attachments<ept id="p1">**</ept> button (the paper clip symbol) in the upper-right corner of the page, or press <bpt id="p2">**</bpt>Ctrl+Shift+A<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Veljið hnappinn <bpt id="p1">**</bpt>Viðhengi<ept id="p1">**</ept> (bréfaklemmutáknið) efst í hægra horni síðunnar eða ýtið á <bpt id="p2">**</bpt>Ctrl+Shift+A<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>Attachments button on the Electronic reporting run logs page in Finance and Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hnappur viðhengis í keyrslukladdasíðu rafrænnar skýrslugerðar í Finance and Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>On the <bpt id="p1">**</bpt>Attachments for Electronic reporting run logs<ept id="p1">**</ept> page, on the Action Pane, select <bpt id="p2">**</bpt>Open<ept id="p2">**</ept> to get the performance trace as a zip file and store it locally.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Á síðunni <bpt id="p1">**</bpt>Viðhengi fyrir keyrslukladda rafrænnar skýrslugerðar<ept id="p1">**</ept>, í aðgerðarúðunni, skal velja <bpt id="p2">**</bpt>Opna<ept id="p2">**</ept> til að ná í afkastarakninguna sem zip-skrá og geyma hana staðbundið.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>Attachments for Electronic reporting run logs page in Finance and Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Viðhengi fyrir keyrslukladdasíðu rafrænnar skýrslugerðar í Finance and Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>The trace that is generated has a reference to the source ER report via a unique report identifier in <bpt id="p1">**</bpt>GUID<ept id="p1">**</ept> format only.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Rakningin sem er búin til er með tilvísun í upprunaskýrslu rafrænnar skýrslugerðar í gegnum einkvæmt kennimerki skýrslu aðeins á sniðinu <bpt id="p1">**</bpt>GUID<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>The version numbering of the format isn't considered.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Númeraúthlutun fyrir útgáfu sniðsins er ekki tekin með í reikninginn.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>Notice that the association between the performance trace that has been generated for the executed ER format and the ER model mapping is based on the root descriptor that was used and the common data model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Takið eftir að tengingin milli afkastarakningar sem hefur verið búin til fyrir framkvæmt snið rafrænnar skýrslugerðar og líkanavörpun rafrænnar skýrslugerðar byggist á rótarlýsingu sem var notuð og algenga gagnalíkanið.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>The version numbering of the format and model mapping isn't considered.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Númeraúthlutun fyrir útgáfu sniðsins og líkanavörpunar eru ekki teknar með í reikninginn.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>The setting of the <bpt id="p1">**</bpt>Default for model mapping<ept id="p1">**</ept> flag for the model mapping also isn't considered.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Stillingin á flagginu <bpt id="p1">**</bpt>Sjálfgefið fyrir líkanavörpun<ept id="p1">**</ept> fyrir líkanavörpunina er einnig ekki tekin með í reikninginn.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source><bpt id="p1">&lt;a id='import-trace'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>Import the generated trace into RCS</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;a id='import-trace'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>Flytja inn mynda rakningu í RCS</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>In RCS, in the <bpt id="p1">**</bpt>Electronic reporting<ept id="p1">**</ept> workspace, select the <bpt id="p2">**</bpt>Reporting configurations<ept id="p2">**</ept> tile.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Í RCS, á vinnusvæðinu <bpt id="p1">**</bpt>Rafræn skýrslugerð<ept id="p1">**</ept>, skal velja reitinn <bpt id="p2">**</bpt>Skilgreiningar skýrslugerðar<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>On the <bpt id="p1">**</bpt>Configurations<ept id="p1">**</ept> page, in the configuration tree, expand the <bpt id="p2">**</bpt>Performance trace model<ept id="p2">**</ept> item, and select the <bpt id="p3">**</bpt>Performance trace format<ept id="p3">**</ept> item.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Á síðunni <bpt id="p1">**</bpt>Skilgreiningar<ept id="p1">**</ept>, í skilgreiningartrénu, skal stækka atriðið <bpt id="p2">**</bpt>Líkan afkastarakningar<ept id="p2">**</ept> og velja atriðið <bpt id="p3">**</bpt>Snið afkastarakningar<ept id="p3">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>On the Action Pane, select <bpt id="p1">**</bpt>Designer<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Í aðgerðarúðunni skal velja <bpt id="p1">**</bpt>Hönnuður<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>On the <bpt id="p1">**</bpt>Format designer<ept id="p1">**</ept> page, on the Action Pane, select <bpt id="p2">**</bpt>Performance trace<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Á síðunni <bpt id="p1">**</bpt>Sniðshönnuður<ept id="p1">**</ept>, í aðgerðarúðunni, skal velja <bpt id="p2">**</bpt>Afkastarakning<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>In the <bpt id="p1">**</bpt>Performance trace result settings<ept id="p1">**</ept> dialog box, select <bpt id="p2">**</bpt>Import performance trace<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Í svarglugganum <bpt id="p1">**</bpt>Stillingar fyrir niðurstöðu afkastarakningar<ept id="p1">**</ept> skal velja <bpt id="p2">**</bpt>Flytja inn afkastarakningu<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>Select <bpt id="p1">**</bpt>Browse<ept id="p1">**</ept> to select the zip file that you exported from Finance and Operations earlier.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Veljið <bpt id="p1">**</bpt>Vafra<ept id="p1">**</ept> til að velja zip-skrána sem flutt var út úr Finance and Operations á undan.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>Select <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Veljið <bpt id="p1">**</bpt>Í lagi<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>Performance trace result settings dialog box in RCS</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Svargluggi stillinga fyrir niðurstöðu afkastarakningar í RCS</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>Use the performance trace for analysis in RCS – Format execution</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Nota afkastarakningu fyrir greiningu í RCS - framkvæmd sniðs</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>In RCS, on the <bpt id="p1">**</bpt>Format designer<ept id="p1">**</ept> page, select <bpt id="p2">**</bpt>Expand/collapse<ept id="p2">**</ept> to expand the content of all format items.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Í RCS, á síðunni <bpt id="p1">**</bpt>Sniðshönnuður<ept id="p1">**</ept>, skal velja <bpt id="p2">**</bpt>Stækka/fella saman<ept id="p2">**</ept> til að stækka efni allra sniðsatriða.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>Notice that additional information is shown for some items of the current format:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Takið eftir að frekari upplýsingar eru sýndar fyrir sum atriði núverandi sniðs:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>The actual time that was spent entering data in the generated output by using the format item</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Raunverulegur tími sem fór í að færa gögn inn í myndað frálag með því að nota sniðsatriðið</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>The same time expressed as a percentage of the total time that was spent generating the whole output</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Sami tími sýndur sem prósenta af heildartímanum sem fór í að búa til allt frálagið</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>Format designer page in RCS</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Síða sniðshönnuðar í RCS</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>Close <bpt id="p1">**</bpt>Format designer<ept id="p1">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lokaðu síðunni <bpt id="p1">**</bpt>Sniðshönnuður<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source><bpt id="p1">&lt;a id='use-trace'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>Use the performance trace for analysis in RCS – Model mapping</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;a id='use-trace'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>Nota afkastarakningu fyrir greiningu í RCS - Líkanavörpun</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>In RCS, on the <bpt id="p1">**</bpt>Configurations<ept id="p1">**</ept> page, in the configuration tree, select the <bpt id="p2">**</bpt>Performance trace mapping<ept id="p2">**</ept> item.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Í RCS, á síðunni <bpt id="p1">**</bpt>Skilgreiningar<ept id="p1">**</ept>, í skilgreiningartrénu, skal velja atriðið <bpt id="p2">**</bpt>Vörpun afkastarakningar<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>On the Action Pane, select <bpt id="p1">**</bpt>Designer<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">Í aðgerðarúðunni skal velja <bpt id="p1">**</bpt>Hönnuður<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>Select <bpt id="p1">**</bpt>Designer<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Veljið <bpt id="p1">**</bpt>Hönnuður<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>On the <bpt id="p1">**</bpt>Model mapping designer<ept id="p1">**</ept> page, on the Action Pane, select <bpt id="p2">**</bpt>Performance trace<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Á síðunni <bpt id="p1">**</bpt>Hönnuður líkanavörpunar<ept id="p1">**</ept>, í aðgerðarúðunni, skal velja <bpt id="p2">**</bpt>Afkastarakning<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>Select the trace that you imported earlier.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Veljið rakninguna sem var flutt inn áður.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>Select <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Veljið <bpt id="p1">**</bpt>Í lagi<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>Notice that new information becomes available for some data source items of the current model mapping:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Takið eftir að nýjar upplýsingar verða tiltækar fyrir sum atriði gagnaveitu fyrir núverandi líkanavörpun:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>The actual time that was spent getting data by using the data source</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Raunverulegur tími sem fór í að ná í gögn með því að nota gagnagjafann</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>The same time expressed as a percentage of the total time that was spent running the whole model mapping</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Sami tími sýndur sem prósenta af heildartímanum sem fór í að keyra alla líkanavörpunina</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>Notice that ER informs you that the current model mapping duplicates database requests while the VendTable/<ph id="ph1">\&lt;</ph>Relations/VendTrans.VendTable<ph id="ph2">\_</ph>AccountNum data source is run.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Takið eftir því að rafræn skýrslugerð segir þér að núverandi líkanavörpun afritar beiðnir gagnagrunns á meðan VendTable/<ph id="ph1">\&lt;</ph>Relations/VendTrans.VendTable<ph id="ph2">\_</ph>AccountNum gagnagjafi er keyrður.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>This duplication occurs because the list of vendor transactions is called two times for each iterated vendor record:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Þessi tvítekning á sér stað vegna þess að kallað er á listann yfir lánardrottnafærslur tvisvar sinnum fyrir hverja endurtekna lánardrottnafærslu:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>One call is made to enter details of each transaction in the data model, based on configured bindings.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Eitt kall er framkvæmt til að færa upplýsingar um hverja færslu inn í gagnalíkanið, sem byggist á skilgreindum bindingum.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>One call is made to enter the calculated number of transactions per vendor in the data model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Eitt kall er framkvæmt til að færa reiknaðan fjölda færslna á hvern lánardrottin inn í gagnalíkanið.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>Message about duplicate database requests on the Model mapping designer page in RCS</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Skilaboð um tvítekna gagnagrunnsbeiðni á hönnunarsíðu líkanavörpunar í RCS</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>The value <bpt id="p1">**</bpt><ph id="ph1">\[</ph>Q:530<ph id="ph2">\]</ph><ept id="p1">**</ept> indicates that the VendTrans table was called 530 times to return a record from that table to the VendTable/<ph id="ph3">\&lt;</ph>Relations/VendTrans.VendTable<ph id="ph4">\_</ph>AccountNum data source.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Gildið <bpt id="p1">**</bpt><ph id="ph1">\[</ph>Q:530<ph id="ph2">\]</ph><ept id="p1">**</ept> gefur til kynna að kallað var á VendTrans-töfluna 530 sinnum til að skila færslu úr þeirri töflu yfir í VendTable/<ph id="ph3">\&lt;</ph>Relations/VendTrans.VendTable<ph id="ph4">\_</ph>AccountNum gagnagjafann.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>The value <bpt id="p1">**</bpt><ph id="ph1">\[</ph>530<ph id="ph2">\]</ph><ept id="p1">**</ept> indicates that the VendTable/<ph id="ph3">\&lt;</ph>Relations/VendTrans.VendTable<ph id="ph4">\_</ph>AccountNum data source was called 530 times to return a record from that data source and enter the details from it in the data model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Gildið <bpt id="p1">**</bpt><ph id="ph1">\[</ph>530<ph id="ph2">\]</ph><ept id="p1">**</ept> gefur til kynna að kallað var á VendTable/<ph id="ph3">\&lt;</ph>Relations/VendTrans.VendTable<ph id="ph4">\_</ph>AccountNum gagnagjafann 530 sinnum til að skila færslu úr þeim gagnagjafa og færa inn upplýsingarnar úr henni inn í gagnalíkanið.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>We recommend that you use caching for the VendTable/<ph id="ph1">\&lt;</ph>Relations/VendTrans.VendTable<ph id="ph2">\_</ph>AccountNum data source, to reduce the number of calls that are made to get the details for 265 transactions and help improve the performance of the model mapping.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Við mælum með að þú notir vistun í skyndiminni fyrir VendTable/<ph id="ph1">\&lt;</ph>Relations/VendTrans.VendTable<ph id="ph2">\_</ph>AccountNum gagnagjafann til að fækka fjölda kalla sem eru gerð til að ná í upplýsingar fyrir 265 færslur og hjálpa til við að bæta afköst líkanavörpunar.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>It can also be useful to reduce the number of calls that are made to the LedgerTransTypeList data source.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hún getur einnig verið gagnleg til að fækka fjölda kalla til LedgerTransTypeList gagnagjafann.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>This data source is used to associate each value of the <bpt id="p1">**</bpt>LedgerTransType<ept id="p1">**</ept> enumeration with its label.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Þessi gagnagjafi er notaður til að tengja hvert gildi tölusetningarinnar <bpt id="p1">**</bpt>LedgerTransType<ept id="p1">**</ept> við merkið sitt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source>By using this data source, you can find an appropriate label and enter it in the data model for each vendor transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Með því að nota þennan gagnagjafa geturðu fundið viðeigandi merki og fært það inn í gagnalíkanið fyrir hverja lánardrottnafærsla.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>The current number of calls to this data source (9,027) is quite high for 265 transactions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Núverandi fjöldi kalla á þennan gagnagjafa (9027) er frekar hár fyrir 265 færslur.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source>Model mapping designer page in RCS, showing 9,027 calls to the data source</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hönnunarsíða líkanavörpunar í RCS sýnir 9027 köll á gagnagjafa</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>Improve the model mapping based on information from the execution trace</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bæta líkanavörpun á grundvelli upplýsinga úr framkvæmdarakningu</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source>Modify the logic of the model mapping</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Breyta reiknireglu líkanavörpunar</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source>Follow these steps to use caching, to help prevent duplicate calls to the database:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Fylgið þessum skrefum til að nota vistun í skyndiminni, til að hjálpa til við koma í veg fyrir tvítekin köll á gagnagrunn:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>In RCS, on the <bpt id="p1">**</bpt>Model mapping designer<ept id="p1">**</ept> page, in the <bpt id="p2">**</bpt>Data sources<ept id="p2">**</ept> pane, select the <bpt id="p3">**</bpt>VendTable<ept id="p3">**</ept> item.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Í RCS, á síðunni <bpt id="p1">**</bpt>Hönnuður líkanavörpunar<ept id="p1">**</ept>, í rúðunni <bpt id="p2">**</bpt>Gagnagjafar<ept id="p2">**</ept>, skal velja atriðið <bpt id="p3">**</bpt>VendTable<ept id="p3">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>Select <bpt id="p1">**</bpt>Cache<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Veljið <bpt id="p1">**</bpt>Skyndiminni<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>Expand the <bpt id="p1">**</bpt>VendTable<ept id="p1">**</ept> item, expand the list of one-to-many relations for the VendTable data source (the <bpt id="p2">**</bpt><ph id="ph1">\&lt;</ph>Relations<ept id="p2">**</ept> item), and select the <bpt id="p3">**</bpt>VendTrans.VendTable<ph id="ph2">\_</ph>AccountNum<ept id="p3">**</ept> item.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Stækkið atriðið <bpt id="p1">**</bpt>VendTable<ept id="p1">**</ept>, stækkið listann yfir einn í mörg tengsl fyrir VendTable gagnagjafann (atriðið <bpt id="p2">**</bpt><ph id="ph1">\&lt;</ph>Tengsl<ept id="p2">**</ept>) og veljið atriðið <bpt id="p3">**</bpt>VendTrans.VendTable<ph id="ph2">\_</ph>AccountNum<ept id="p3">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source>Select <bpt id="p1">**</bpt>Cache<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Veljið <bpt id="p1">**</bpt>Skyndiminni<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source>Caching setup to help prevent duplicate calls</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Uppsetning á vistun í skyndiminni til að hjálpa til við að koma í veg fyrir tvítekin köll</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>Follow these steps to bring the LedgerTransTypeList data source into the scope of the VendTable data source:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Fylgið þessum skrefum til að færa LedgerTransTypeList gagnagjafann inn í umfang VendTable gagnagjafans:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>In the <bpt id="p1">**</bpt>Data source types<ept id="p1">**</ept> pane, expand the <bpt id="p2">**</bpt>Functions<ept id="p2">**</ept> item, and select the <bpt id="p3">**</bpt>Calculated field<ept id="p3">**</ept> item.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Í rúðunni <bpt id="p1">**</bpt>Gerðir gagnagjafa<ept id="p1">**</ept> skal stækka atriðið <bpt id="p2">**</bpt>Virknir<ept id="p2">**</ept> og velja atriðið <bpt id="p3">**</bpt>Reiknaður reitur<ept id="p3">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source>In the <bpt id="p1">**</bpt>Data sources<ept id="p1">**</ept> pane, select the <bpt id="p2">**</bpt>VendTable<ept id="p2">**</ept> item.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Í rúðunni <bpt id="p1">**</bpt>Gagnagjafar<ept id="p1">**</ept> skal velja atriðið <bpt id="p2">**</bpt>VendTable<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>Select <bpt id="p1">**</bpt>Add<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Veljið <bpt id="p1">**</bpt>Bæta við<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>In the <bpt id="p1">**</bpt>Name<ept id="p1">**</ept> field, enter <bpt id="p2">**</bpt><ph id="ph1">\$</ph>TransType<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Í reitinn <bpt id="p1">**</bpt>Heiti<ept id="p1">**</ept> skal færa inn <bpt id="p2">**</bpt><ph id="ph1">\$</ph>TransType<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>Select <bpt id="p1">**</bpt>Edit formula<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Veljið <bpt id="p1">**</bpt>Breyta formúlu<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="273">
          <source>In the <bpt id="p1">**</bpt>Formula<ept id="p1">**</ept> field, enter <bpt id="p2">**</bpt>LedgerTransTypeList<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Í reitinn <bpt id="p1">**</bpt>Formúla<ept id="p1">**</ept> skal færa inn <bpt id="p2">**</bpt>LedgerTransTypeList<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="274">
          <source>Select <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Veljið <bpt id="p1">**</bpt>Vista<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="275">
          <source>Close the <bpt id="p1">**</bpt>Formula editor<ept id="p1">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lokið síðunni <bpt id="p1">**</bpt>Formúluritill<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="276">
          <source>Click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Smellt er á <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="277">
          <source>Follow these steps to do caching of the <bpt id="p1">**</bpt><ph id="ph1">\$</ph>TransType<ept id="p1">**</ept> field:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Fylgið þessum skrefum til að vista í skyndiminni á reitnum <bpt id="p1">**</bpt><ph id="ph1">\$</ph>TransType<ept id="p1">**</ept>:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="278">
          <source>Select the <bpt id="p1">**</bpt>LedgerTransTypeList<ept id="p1">**</ept> item.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Veljið atriðið <bpt id="p1">**</bpt>LedgerTransTypeList<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="279">
          <source>Select <bpt id="p1">**</bpt>Cache<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Veljið <bpt id="p1">**</bpt>Skyndiminni<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="280">
          <source>Select the <bpt id="p1">**</bpt>VendTable.<ph id="ph1">\$</ph>TransType<ept id="p1">**</ept> item.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Veljið atriðið <bpt id="p1">**</bpt>VendTable.<ph id="ph1">\$</ph>TransType<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="281">
          <source>Select <bpt id="p1">**</bpt>Cache<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Veljið <bpt id="p1">**</bpt>Skyndiminni<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="282">
          <source>Caching setup for the $TransType field</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Uppsetning á vistun í skyndiminni fyrir reitinn $TransType</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="283">
          <source>Follow these steps to change the <bpt id="p1">**</bpt><ph id="ph1">\$</ph>TransTypeRecord<ept id="p1">**</ept> field so that it starts to use the cached <bpt id="p2">**</bpt><ph id="ph2">\$</ph>TransType<ept id="p2">**</ept> field:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Fylgið þessum skrefum til að breyta reitnum <bpt id="p1">**</bpt><ph id="ph1">\$</ph>TransTypeRecord<ept id="p1">**</ept> svo hann byrji að nota skyndiminni reitsins <bpt id="p2">**</bpt><ph id="ph2">\$</ph>TransType<ept id="p2">**</ept>:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="284">
          <source>In the <bpt id="p1">**</bpt>Data sources<ept id="p1">**</ept> pane, expand the <bpt id="p2">**</bpt>VendTable<ept id="p2">**</ept> item, expand the <bpt id="p3">**</bpt><ph id="ph1">\&lt;</ph>Relations<ept id="p3">**</ept> item, expand the <bpt id="p4">**</bpt>VendTrans.VendTable<ph id="ph2">\_</ph>AccountNum<ept id="p4">**</ept> item, and select the <bpt id="p5">**</bpt>VendTable. VendTrans.VendTable<ph id="ph3">\_</ph>AccountNum.<ph id="ph4">\$</ph>TransTypeRecord<ept id="p5">**</ept> item.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Í rúðunni <bpt id="p1">**</bpt>Gagnagjafar<ept id="p1">**</ept> skal stækka atriðið <bpt id="p2">**</bpt>VendTable<ept id="p2">**</ept>, stækka atriðið <bpt id="p3">**</bpt><ph id="ph1">\&lt;</ph>Tengsl<ept id="p3">**</ept>, stækka atriðið <bpt id="p4">**</bpt>VendTrans.VendTable<ph id="ph2">\_</ph>AccountNum<ept id="p4">**</ept> og velja atriðið <bpt id="p5">**</bpt>VendTable. VendTrans.VendTable<ph id="ph3">\_</ph>AccountNum.<ph id="ph4">\$</ph>TransTypeRecord<ept id="p5">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="285">
          <source>Select <bpt id="p1">**</bpt>Edit<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Veljið <bpt id="p1">**</bpt>Breyta<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="286">
          <source>Select <bpt id="p1">**</bpt>Edit formula<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Veljið <bpt id="p1">**</bpt>Breyta formúlu<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="287">
          <source>In the <bpt id="p1">**</bpt>Formula<ept id="p1">**</ept> field, find the following expression:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Í reitnum <bpt id="p1">**</bpt>Formúla<ept id="p1">**</ept> skal finna eftirfarandi segð:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="288">
          <source>FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = <ph id="ph1">\@</ph>.TransType))</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = <ph id="ph1">\@</ph>.TransType))</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="289">
          <source>In the <bpt id="p1">**</bpt>Formula<ept id="p1">**</ept> field, enter the following expression:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Í reitnum <bpt id="p1">**</bpt>Formúla<ept id="p1">**</ept> skal færa inn eftirfarandi segð:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="290">
          <source>FIRSTORNULL (WHERE (VendTable.'<ph id="ph1">\$</ph>TransType', VendTable.'<ph id="ph2">\$</ph>TransType'.Enum = <ph id="ph3">\@</ph>.TransType)).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FIRSTORNULL (WHERE (VendTable.'<ph id="ph1">\$</ph>TransType', VendTable.'<ph id="ph2">\$</ph>TransType'.Enum = <ph id="ph3">\@</ph>.TransType)).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="291">
          <source>Select <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Veljið <bpt id="p1">**</bpt>Vista<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="292">
          <source>Close the <bpt id="p1">**</bpt>Formula editor<ept id="p1">**</ept> page.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">Lokið síðunni <bpt id="p1">**</bpt>Formúluritill<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="293">
          <source>Select <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Veljið <bpt id="p1">**</bpt>Í lagi<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="294">
          <source>Select <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Veljið <bpt id="p1">**</bpt>Vista<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="295">
          <source>Close the <bpt id="p1">**</bpt>Model mapping designer<ept id="p1">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lokið síðunni <bpt id="p1">**</bpt>Hönnuður líkanavörpunar<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="296">
          <source>Close the <bpt id="p1">**</bpt>Model mappings<ept id="p1">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lokið síðunni <bpt id="p1">**</bpt>Líkanavarpanir<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="297">
          <source>Complete the modified version of the ER model mapping</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ljúka við breyttu útgáfuna af líkanavörpun rafrænnar skýrslugerðar</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="298">
          <source>In RCS, on the <bpt id="p1">**</bpt>Configurations<ept id="p1">**</ept> page, on the <bpt id="p2">**</bpt>Versions<ept id="p2">**</ept> FastTab, select version <bpt id="p3">**</bpt>1.2<ept id="p3">**</ept> of the <bpt id="p4">**</bpt>Performance trace mapping<ept id="p4">**</ept> configuration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Í RCS, á síðunni <bpt id="p1">**</bpt>Skilgreiningar<ept id="p1">**</ept>, í flýtiflipanum <bpt id="p2">**</bpt>Útgáfur<ept id="p2">**</ept>, skal velja útgáfuna <bpt id="p3">**</bpt>1.2<ept id="p3">**</ept> af skilgreiningunni <bpt id="p4">**</bpt>Vörpun afkastarakningar<ept id="p4">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="299">
          <source>Select <bpt id="p1">**</bpt>Change status<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Veljið <bpt id="p1">**</bpt>Breyta stöðu<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="300">
          <source>Select <bpt id="p1">**</bpt>Complete<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Velja <bpt id="p1">**</bpt>Lokið<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="301">
          <source>Import the modified ER model mapping configuration from RCS into Finance and Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Flytja inn breytta skilgreiningu á líkanavörpun rafrænnar skýrslugerðar úr RCS í Finance and Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="302">
          <source>Repeat the steps in the <bpt id="p1">[</bpt>Import an ER configuration from RCS into Finance and Operations<ept id="p1">](#import-configuration)</ept> section earlier in this topic to import version 1.2 of the <bpt id="p2">**</bpt>Performance trace mapping<ept id="p2">**</ept> configuration into Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Endurtakið skrefin í hlutanum <bpt id="p1">[</bpt>Flytja inn skilgreiningu rafrænnar skýrslugerðar úr RCS í Finance and Operations<ept id="p1">](#import-configuration)</ept> fyrr í þessu efnisatriði til að flytja inn útgáfu 1.2 af skilgreiningunni <bpt id="p2">**</bpt>Vörpun afkastarakningar<ept id="p2">**</ept> í Finance and Operations.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="303">
          <source>Run the modified ER solution to trace execution</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Keyra breytta lausn rafrænnar skýrslugerðar til að rekja framkvæmd</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="304">
          <source>Run the ER format</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Keyra snið rafrænnar skýrslugerðar</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="305">
          <source>Repeat the steps in the <bpt id="p1">[</bpt>Run the ER format<ept id="p1">](#run-format)</ept> section earlier in this topic to generate a new performance trace.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Endurtakið skrefin í hlutanum <bpt id="p1">[</bpt>Keyra snið rafrænnar skýrslugerðar<ept id="p1">](#run-format)</ept> fyrr í þessu efnisatriði til að búa til nýja afkastarakningu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="306">
          <source>Review the execution trace</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">Yfirfara framkvæmdarakningu</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="307">
          <source>Export the generated trace from Finance and Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Flytja út myndaða rakningu úr Finance and Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="308">
          <source>Repeat the steps in the <bpt id="p1">[</bpt>Export the generated trace from Finance and Operations<ept id="p1">](#export-trace)</ept> section earlier in this topic to save a new performance trace locally.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Endurtakið skrefin í hlutanum <bpt id="p1">[</bpt>Flytja út myndaða rakningu úr Finance and Operations<ept id="p1">](#export-trace)</ept> fyrr í þessu efnisatriði til að vista nýja afkastarakningu staðbundið.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="309">
          <source>Import the generated trace into RCS</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Flytja inn myndaða rakningu í RCS</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="310">
          <source>Repeat the steps in the <bpt id="p1">[</bpt>Import the generated trace into RCS<ept id="p1">](#import-trace)</ept> section earlier in this topic to import the new performance trace into RCS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Endurtakið skrefin í hlutanum <bpt id="p1">[</bpt>Flytja inn myndaða rakningu í RCS<ept id="p1">](#import-trace)</ept> fyrr í þessu efnisatriði til að flytja inn nýja afkastarakningu í RCS.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="311">
          <source>Use the performance trace for analysis in RCS – Model mapping</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Nota afkastarakningu fyrir greiningu í RCS - Líkanavörpun</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="312">
          <source>Repeat the steps in the <bpt id="p1">[</bpt>Use the performance trace for analysis in RCS – Model mapping<ept id="p1">](#use-trace)</ept> section earlier in this topic to analyze the latest performance trace.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Endurtakið skrefin í hlutanum <bpt id="p1">[</bpt>Nota afkastarakningu fyrir greiningu í RCS - Líkanavörpun<ept id="p1">](#use-trace)</ept> fyrr í þessu efnisatriði til að greina síðustu afkastarakningu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="313">
          <source>Notice that the adjustments that you made to the model mapping have eliminated duplicate queries to database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Takiði eftir að leiðréttingar sem voru gerðar á líkanavörpun hafa eytt tvíteknum fyrirspurnum til gagnagrunns.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="314">
          <source>The number of calls to database tables and data sources for this model mapping has been also reduced.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Fjöldi kalla í gagnagrunnstöflur og gagnagjafa fyrir þessa líkanavörpun hefur einnig verið fækkað.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="315">
          <source>Therefore, the performance of the whole ER solution has improved.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Afköst á allri lausn rafrænnar skýrslugerðar hefur þar af leiðandi verið endurbætt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="316">
          <source>Trace information for the VendTable data source on the Model mapping designer page in RCS</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Rakningarupplýsingar fyrir VendTable gagnagjafann á hönnunarsíðu líkanavörpunar í RCS</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="317">
          <source>In the trace information, the value <bpt id="p1">**</bpt><ph id="ph1">\[</ph>12<ph id="ph2">\]</ph><ept id="p1">**</ept> for the VendTable data source indicates that this data source was called 12 times.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Í rakningarupplýsingunum gefur gildið <bpt id="p1">**</bpt><ph id="ph1">\[</ph>12<ph id="ph2">\]</ph><ept id="p1">**</ept> fyrir VendTable gagnagjafa til kynna að kallað hafi verið á þennan gagnagjafa 12 sinnum.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="318">
          <source>The value <bpt id="p1">**</bpt><ph id="ph1">\[</ph>Q:6<ph id="ph2">\]</ph><ept id="p1">**</ept> indicates that six calls were translated to database calls to the VendTable table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Gildið <bpt id="p1">**</bpt><ph id="ph1">\[</ph>Q:6<ph id="ph2">\]</ph><ept id="p1">**</ept> gefur til kynna að sex köll hafi verið þýdd yfir á gagnagrunnsköll til VendTable-töflunnar.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="319">
          <source>The value <bpt id="p1">**</bpt><ph id="ph1">\[</ph>C:6<ph id="ph2">\]</ph><ept id="p1">**</ept> indicates that the records that were fetched from the database were cached, and six other calls were processed by using the cache.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Gildið <bpt id="p1">**</bpt><ph id="ph1">\[</ph>C:6<ph id="ph2">\]</ph><ept id="p1">**</ept> gefur til kynna að færslurnar sem voru sóttar úr gagnagrunninum hafi verið skyndiminni og unnið hafi verið úr sex öðrum köllum með því að nota skyndiminnið.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="320">
          <source>Notice that the number of calls to the LedgerTransTypeList data source has been reduced from 9,027 to 240.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Athugið að fjöldi kalla á LedgerTransTypeList gagnagjafann hefur fækkað úr 9027 í 240.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="321">
          <source>Trace information for the LedgerTransTypeList data source on the Model mapping designer page in RCS</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Rakningarupplýsingar fyrir LedgerTransTypeList gagnagjafann á hönnunarsíðu líkanavörpunar í RCS</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="322">
          <source>Review the execution trace in Finance and Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Yfirfara framkvæmdarakningu í Finance and Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="323">
          <source>In addition to RCS, some versions of Finance and Operations might offer capabilities for an ER framework designer experience.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Auk RCS kunna sumar útgáfur af Finance and Operations að bjóða upp á möguleika fyrir hönnunarupplifun á ramma rafrænnar skýrslugerðar.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="324">
          <source>These versions of Finance and Operations have an <bpt id="p1">**</bpt>Enable design mode<ept id="p1">**</ept> option that can be turned on.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Þessar útgáfur af Finance and Operations eru með valkostinn <bpt id="p1">**</bpt>Virkja hönnunarsnið<ept id="p1">**</ept> sem hægt er að kveikja á.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="325">
          <source>You can find this option on the <bpt id="p1">**</bpt>General<ept id="p1">**</ept> tab of the <bpt id="p2">**</bpt>Electronic reporting parameters<ept id="p2">**</ept> page, which you can open from the <bpt id="p3">**</bpt>Electronic reporting<ept id="p3">**</ept> workspace.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hægt er að finna þennan valkost í flipanum <bpt id="p1">**</bpt>Almennt<ept id="p1">**</ept> á síðunni <bpt id="p2">**</bpt>Rafrænar skýrslugerðarfæribreytur<ept id="p2">**</ept> sem hægt er að opna úr vinnusvæðinu <bpt id="p3">**</bpt>Rafræn skýrslugerð<ept id="p3">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="326">
          <source>Enable design mode option on the Electronic reporting parameters page in Finance and Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Virkja valkost hönnunarsniðs á síðu rafrænna skýrslugerðarfæribreyta í Finance and Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="327">
          <source>If you use one of these versions of Finance and Operations, you can analyze the details of generated performance traces directly in Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ef þú notar eina af þessum útgáfum af Finance and Operations geturðu greint upplýsingar á mynduðum afkastarakningum beint í Finance and Operations.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="328">
          <source>You don't have to export them from Finance and Operation and import them into RCS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ekki þarf að flytja þær út úr Finance and Operation og flytja inn í RCS.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="329">
          <source>Review the execution trace by using external tools</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Yfirfara framkvæmdarakningu með utanaðkomandi verkfærum</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="330">
          <source>Configure user parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Skilgreina færibreytur notanda</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="331">
          <source>In Finance and Operations, go to <bpt id="p1">**</bpt>Organization administration <ph id="ph1">\&gt;</ph> Electronic reporting <ph id="ph2">\&gt;</ph> Configurations<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">Í Finance and Operations skal opna <bpt id="p1">**</bpt>Fyrirtækisstjórnun <ph id="ph1">\&gt;</ph> Rafræn skýrslugerð <ph id="ph2">\&gt;</ph> Skilgreiningar<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="332">
          <source>On the <bpt id="p1">**</bpt>Configurations<ept id="p1">**</ept> page, on the Action Pane, on the <bpt id="p2">**</bpt>Configurations<ept id="p2">**</ept> tab, in the <bpt id="p3">**</bpt>Advanced settings<ept id="p3">**</ept> group, select <bpt id="p4">**</bpt>User parameters<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">Á síðunni <bpt id="p1">**</bpt>Skilgreiningar<ept id="p1">**</ept>, í aðgerðarúðunni, í flipanum <bpt id="p2">**</bpt>Skilgreiningar<ept id="p2">**</ept>, í flokknum <bpt id="p3">**</bpt>Ítarlegar stillingar<ept id="p3">**</ept>, skal velja <bpt id="p4">**</bpt>Færibreytur notanda<ept id="p4">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="333">
          <source>In the <bpt id="p1">**</bpt>User parameters<ept id="p1">**</ept> dialog box, in the <bpt id="p2">**</bpt>Execution tracing<ept id="p2">**</ept> section, in the <bpt id="p3">**</bpt>Execution trace format<ept id="p3">**</ept> field, select <bpt id="p4">**</bpt>PerfView XML<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Í svarglugganum <bpt id="p1">**</bpt>Færibreytur notanda<ept id="p1">**</ept>, í hlutanum <bpt id="p2">**</bpt>Rakning keyrslu<ept id="p2">**</ept>, í reitnum <bpt id="p3">**</bpt>Snið framkvæmdarakningar<ept id="p3">**</ept>, skal velja <bpt id="p4">**</bpt>Perfview XML<ept id="p4">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="334">
          <source>Run the ER format</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">Keyra snið rafrænnar skýrslugerðar</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="335">
          <source>Repeat the steps in the <bpt id="p1">[</bpt>Run the ER format<ept id="p1">](#run-format)</ept> section earlier in this topic to generate a new performance trace.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">Endurtakið skrefin í hlutanum <bpt id="p1">[</bpt>Keyra snið rafrænnar skýrslugerðar<ept id="p1">](#run-format)</ept> fyrr í þessu efnisatriði til að búa til nýja afkastarakningu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="336">
          <source>Notice that the web browser offers a zip file for download.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Athugið að netvafrinn býður upp á zip-skrá fyrir niðurhal.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="337">
          <source>This file contains the performance trace in PerfView format.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Þessi skrá inniheldur afkastarakningu á PerfView-sniði.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="338">
          <source>You can then use the PerfView performance analysis tool to analyze the details of ER format execution.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Síðan er hægt að nota greiningarverkfæri fyrir verkfæri PerfView-afkastagreiningar til að greina upplýsingarnar fyrir framkvæmd á sniði rafrænnar skýrslugerðar.</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>