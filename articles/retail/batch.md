<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="batch.md" target-language="is-is">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-d915bc8" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>batch.e70006.4456fc3d5bc4547fa8211642b11ca6df455fa187.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>4456fc3d5bc4547fa8211642b11ca6df455fa187</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>aec1dcd44274e9b8d0770836598fde5533b7b569</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>06/03/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\batch.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Improved handling of batch-tracked items</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Betri meðhöndlun á runuröktum vörum</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes the improvements that have been made to the handling of batches for batch-tracked items during the Retail statement posting process.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Þetta efnisatriði lýsir endurbótum sem hafa verið gerðar á meðhöndlun á runum fyrir runuraktar vörur í bókunarferli smásöluuppgjörs.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Improved handling of batch-tracked items</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">Betri meðhöndlun á runuröktum vörum</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>In Microsoft Dynamics 365 for Retail Point of Sale (POS), batch numbers can't be captured for batch-tracked items at the time of sale.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Á sölustaðnum Microsoft Dynamics 365 for Retail er ekki hægt að sækja rununúmer fyrir runuraktar vörur þegar sala stendur yfir.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>However, for specific configurations, when sales are posted in the headquarters through customer orders or statement posting, the Microsoft Dynamics system expects that valid batch numbers for batch-tracked items exist, and that they will be used during the invoicing process.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Hins vegar, fyrir ákveðnar skilgreiningar, þegar sölur eru bókaðar í höfuðstöðvunum í gegnum pantanir viðskiptamanns eða bókun á uppgjöri gerir Microsoft Dynamics-kerfið ráð fyrir því að gild rununúmer fyrir runuraktar vörur séu til staðar og að þau verði notuð í reikningsfærsluferlinu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>If valid batch numbers are available for products, the customer order invoicing process and the sales order invoicing process from statement posting use them.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Ef gild rununúmer eru í boði fyrir vörur eru þau notuð í reikningsfærsluferli viðskiptamannapöntunar og reikningsfærsluferli sölupöntunar úr bókun uppgjörs.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Otherwise, the customer order invoicing process can't post, and the POS user receives an error message.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Annars nær reikningsfærsluferli viðskiptamannapöntunar ekki að bóka og notandi sölustaðar fær villuboð.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Statement posting then goes into an error state.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Smásöluuppgjör fer þá í villustöðu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>This error state occurs even when negative inventory has been turned on for the products.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Þessi villustaða kemur upp jafnvel eftir að kveikt hefur verið á neikvæðri birgðastöðu fyrir vörurnar.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" approved="yes" id="110">
          <source>Improvements that have been made in Microsoft Dynamics for Retail version 10.0.4 and later help guarantee that, when negative inventory is turned on for batch-tracked items, customer order invoicing and sales order invoicing through statement posting aren't blocked for those items if the inventory is 0 (zero) or a batch number isn't available.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Endurbætur sem gerðar hafa verið á Microsoft Dynamics for Retail útgáfu 10.0.4 og nýrri hjálpa til við að tryggja, þegar kveikt er á neikvæðri birgðastöðu fyrir runuraktar vörur, að ekki sé lokað fyrir reikningsfærslu viðskiptamannapöntunar og reikningsfærslu sölupöntunar í gegnum bókun á uppgjöri fyrir þessar vörur ef birgðir eru 0 (núll) eða rununúmer er ekki til staðar.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>The new functionality uses a default batch ID for the sales lines when batch numbers aren't available.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Nýja virknin notar sjálfgefið runukenni fyrir sölulínur þegar rununúmer eru ekki í boði.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>To define the default batch ID that is used for customer orders, on the <bpt id="p1">**</bpt>Retail parameters<ept id="p1">**</ept> page, on the <bpt id="p2">**</bpt>Customer orders<ept id="p2">**</ept> tab, on the <bpt id="p3">**</bpt>Order<ept id="p3">**</ept> FastTab, set the <bpt id="p4">**</bpt>Default batch id<ept id="p4">**</ept> field.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Til að skilgreina sjálfgefið runukenni sem notað er fyrir pantanir viðskiptamanna skal á síðunni <bpt id="p1">**</bpt>Smásölufæribreytur<ept id="p1">**</ept>, í flipanum <bpt id="p2">**</bpt>Pantanir viðskiptamanna<ept id="p2">**</ept>, í flýtiflipanum <bpt id="p3">**</bpt>Pöntun<ept id="p3">**</ept>, stilla reitinn <bpt id="p4">**</bpt>Sjálfgefið auðkenni runu<ept id="p4">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>To define the default batch ID that is used for sales order invoicing through statement posting, on the <bpt id="p1">**</bpt>Retail parameters<ept id="p1">**</ept> page, on the <bpt id="p2">**</bpt>Posting<ept id="p2">**</ept> tab, on the <bpt id="p3">**</bpt>Inventory update<ept id="p3">**</ept> FastTab, set the <bpt id="p4">**</bpt>Default batch id<ept id="p4">**</ept> field.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Til að skilgreina sjálfgefið runukenni sem notað er fyrir reikningsfærslu sölupöntunar í gegnum bókun á uppgjöri skal á síðunni <bpt id="p1">**</bpt>Smásölufæribreytur<ept id="p1">**</ept>, í flipanum <bpt id="p2">**</bpt>Bókun<ept id="p2">**</ept>, í flýtiflipanum <bpt id="p3">**</bpt>Birgðauppfærsla<ept id="p3">**</ept>, stilla reitinn <bpt id="p4">**</bpt>Sjálfgefið auðkenni runu<ept id="p4">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>This functionality is available only when advanced warehousing is turned on for the specific store warehouse and items.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Þessi virkni er aðeins í boði þegar kveikt er á ítarlegu vöruhúsakerfi fyrir tiltekna verslun, vöruhús og vörur.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>In a later release, the functionality will also be supported for scenarios where advanced warehouse management isn't used.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Í seinni útgáfu verður virknin einnig studd fyrir aðstæður þar sem ítarlegt vöruhúsakerfi er ekki notað.</target>
        </trans-unit>
      </group>
    </body>
  </file>
</xliff>