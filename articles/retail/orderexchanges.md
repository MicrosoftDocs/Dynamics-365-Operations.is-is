<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="orderexchanges.md" target-language="is-is">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>orderexchanges.ba78aa.43571099727830e81c41416b6fe250dba398b3f8.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>43571099727830e81c41416b6fe250dba398b3f8</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\orderexchanges.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Configure and process an exchange on a return order</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Skilgreina og vinna úr skiptum á skilapöntun</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic explains how to configure an exchange on a return in Microsoft Dynamics 365 for Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Þetta efnisatriði útskýrir hvernig skilgreina á skipti á skilum í Microsoft Dynamics 365 for Retail.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Configure and process an exchange on a return order</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Skilgreina og vinna úr skiptum á skilapöntun</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>In previous versions of Microsoft Dynamics 365 for Retail, returns against customer orders were processed by using the return order document in Retail Headquarters.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Í eldri útgáfum af Microsoft Dynamics 365 for Retail var notað skjal vöruskilapöntunar í Retail Headquarters við úrvinnslu á skilum sem tengdust pöntunum viðskiptavina.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>However, the return order document can be used to process only products that are being returned.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hins vegar er aðeins hægt að nota skjal skilapöntunar til að vinna úr afurðum sem verið er að skila.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>The returned products are indicated by a negative quantity on the return order lines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Afurðir sem hefur verið skilað eru sýndar með neikvæðu magni á línum skilapöntunar.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>By contrast, sales are indicated by a positive quantity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Aftur á móti eru sölur sýndar með jákvæðu magni.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>However, the return order document doesn't support positive quantities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Skjal vöruskilapöntunar styður hins vegar ekki jákvætt magn.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Because of this limitation, previous versions of Retail didn't support scenarios where product exchanges are done by using the return order document.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Út af þessari takmörkun studdu eldri útgáfur af Retail ekki kringumstæður þar sem skil afurða eru gerð með því að nota skjal skilapöntunar.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>However, functionality has been added to support scenarios where exchanges are done on return orders.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hins vegar er búið að bæta við virkni sem styður kringumstæður þar sem gerð eru skipti á vöruskilapöntunum.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Retail now uses the sales order document instead of the return order document to process these types of transactions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail notar nú sölupöntunarskjalið í stað skjals vöruskilapöntunar til að vinna úr þess konar færslugerðum.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Configure Retail to support exchanges on return orders</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Skilgreina Retail til að styðja skipti á vöruskilapöntunum</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Follow these steps to configure the system to support exchanges on return orders.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Fylgið þessum skrefum til að skilgreina kerfið svo það styðji skipti á vöruskilapöntunum.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Go to <bpt id="p1">**</bpt>Retail <ph id="ph1">\&gt;</ph> Headquarters setup <ph id="ph2">\&gt;</ph> Parameters <ph id="ph3">\&gt;</ph> Retail parameters<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Opnið <bpt id="p1">**</bpt>Retail <ph id="ph2">\&gt;</ph> Uppsetning höfuðstöðva <ph id="ph3">\&gt;</ph> Færibreytur <ph id="ph1">\&gt;</ph> Smásölufæribreytur<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>On the <bpt id="p1">**</bpt>Customer orders<ept id="p1">**</ept> FastTab, set the <bpt id="p2">**</bpt>Process return orders as sales orders<ept id="p2">**</ept> option to <bpt id="p3">**</bpt>Yes<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Á flýtiflipanum <bpt id="p1">**</bpt>Pantanir viðskiptavinar<ept id="p1">**</ept> skal stilla valkostinn <bpt id="p2">**</bpt>Vinna úr skilapöntunum eins og sölupöntunum<ept id="p2">**</ept> á <bpt id="p3">**</bpt>Já<ept id="p3">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Run the <bpt id="p1">**</bpt>Global configuration distribution schedule<ept id="p1">**</ept> job (<bpt id="p2">**</bpt>1110<ept id="p2">**</ept>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Keyrið verkið <bpt id="p1">**</bpt>Dreifingaráætlun altækrar skilgreiningar<ept id="p1">**</ept> (<bpt id="p2">**</bpt>1110<ept id="p2">**</ept>).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Make an exchange</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Skipti gerð</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>After the system is configured as described in the previous section, the point of sale (POS) user will still select a sales order or sales invoice to process a return, as in previous versions of Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Eftir að kerfið hefur verið skilgreint samkvæmt lýsingu í kaflanum hér á undan, heldur notandi sölustaðar áfram að velja sölupöntun eða sölureikning til að vinna úr skilum eins og í eldri útgáfum af Retail.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>However, after the return items are added to the cart, the user will be able to add new sales lines to the cart.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Eftir að skilavörum er bætt við körfuna getur notandinn hins vegar bætt nýjum sölulínum við hana.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>For these new sales lines, the user must define all the attributes that are required in order to process a customer order line.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Notandi verður að skilgreina allar nauðsynlegar eigindir fyrir þessar nýju sölulínur til að geta unnið úr pöntunarlínu viðskiptavinar.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>These attributes include the delivery method and fulfillment location.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Þessar eigindir fela í sér afhendingaraðferð og uppfyllingarstaðsetningu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>The payment that is due for the transaction will be a net of the return order lines and sales order lines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Greiðslan sem þarf að inna af hendi fyrir færsluna verður nettó af línum vöruskilapöntunar og línum sölupöntunar.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>When payment is tendered for the transaction, the return order will be posted as a sales order document in Retail Headquarters, and the system will immediately invoice the return lines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Þegar greiðsla er gerð upp fyrir færsluna verður skilapöntunin bókuð sem sölupöntunarskjal í Retail Headquarters og kerfið reikningsfærir um leið skilalínurnar.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>To provide better visibility into the various amounts for the cart, three new amount fields have been added to the cart.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Til að bjóða upp á aukinn sýnileika á hinum ýmsu upphæðum fyrir körfuna hefur þremur nýjum upphæðareitum verið bætt við hana.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>You can use the screen designer to make these new fields available in the POS user interface (UI).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hægt er að nota skjáhönnuðinn til að gera þessa nýju reiti tiltæka í notandaviðmóti sölustaðar.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source><bpt id="p1">**</bpt>Deposit applied<ept id="p1">**</ept> – The deposit amount that is applied on a transaction when the user does a customer order pickup.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Innborgun notuð<ept id="p1">**</ept> – Upphæð innborgunar sem er notuð í færslu þegar notandi velur að pöntun viðskiptavinar verði sótt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>If there is no deposit override, and a 10-percent deposit is configured, the amount in this field is 90 percent of the total amount of the customer order.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ef engin hnekking innborgunar er til staðar, og 10% innborgun er skilgreind, er upphæðin í þessum reit 90% af heildarupphæð pöntunar viðskiptavinar.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source><bpt id="p1">**</bpt>Carry out amount<ept id="p1">**</ept> – The total amount for lines where the delivery mode was set to <bpt id="p2">**</bpt>Carry out<ept id="p2">**</ept> when the customer order was created or edited, or during a customer order exchange.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Taka með upphæð<ept id="p1">**</ept> – Heildarupphæð fyrir línur þar sem afhendingarmátinn var stilltur á <bpt id="p2">**</bpt>Taka með<ept id="p2">**</ept> þegar pöntun viðskiptavinar var stofnuð eða breytt, eða við skipti á pöntun viðskiptavinar.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>The amount in this field includes taxes and charges.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Upphæðin í þessum reit inniheldur skatta og gjöld.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source><bpt id="p1">**</bpt>Return amount<ept id="p1">**</ept> – The total amount for lines that have negative quantities during the customer order exchange.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Upphæð skila<ept id="p1">**</ept> – Heildarfjöldi lína sem eru með neikvætt magn við skipti á pöntun viðskiptavinar.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>The amount in this field includes taxes and charges.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Upphæðin í þessum reit inniheldur skatta og gjöld.</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>