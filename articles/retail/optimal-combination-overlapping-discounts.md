<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="optimal-combination-overlapping-discounts.md" target-language="is-is">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>optimal-combination-overlapping-discounts.e4f3cd.e327f652855f898e50f1dd853ae20f3a0ff41d9e.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>e327f652855f898e50f1dd853ae20f3a0ff41d9e</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>e2fb0846fcc6298050a0ec82c302e5eb5254e0b5</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/27/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\optimal-combination-overlapping-discounts.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Determine the optimal combination of overlapping discounts</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ákvarða bestu samsetningu afsláttar sem skarast</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>When discounts overlap, you must determine the combination of overlapping discounts that will produce the lowest transaction total or the highest total discount.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Þegar afsláttur skarast, verður að ákvarða samsetningu afsláttar sem skarast, sem mun skapa lægstu heildarupphæð færslunnar eða hæsta heildarafslátt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103" restype="x-metadata">
          <source>When the discount amount varies according to the price of the products that are purchased, such as in the common 'Buy 1, get 1 X percent off' (BOGO) retail discount, this process becomes an issue of combinatorial optimization.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Þegar afsláttarupphæð er breytileg eftir verði afurða sem eru keyptar, eins og hinn algengi smásöluafsláttur „Keyptu 1, fáðu 1 X prósent afslátt“ (BOGO), snýst þetta ferli um fínstillingu á samsetningum.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Determine the optimal combination of overlapping discounts</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ákvarða bestu samsetningu afsláttar sem skarast</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>When discounts overlap, you must determine the combination of overlapping discounts that will produce the lowest transaction total or the highest total discount.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Þegar afsláttur skarast, verður að ákvarða samsetningu afsláttar sem skarast, sem mun skapa lægstu heildarupphæð færslunnar eða hæsta heildarafslátt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>When the discount amount varies according to the price of the products that are purchased, such as in the common "Buy 1, get 1 X percent off" (BOGO) retail discount, this process becomes an issue of combinatorial optimization.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Þegar afsláttarupphæð er breytileg eftir verði afurða sem eru keyptar, eins og hin algenga „Keyptu 1, fáðu 1 X prósent afslátt“ smásöluafslátt (BOGO), verður þetta ferli vandamál fínstillingar á samsetningum.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>This article applies to Microsoft Dynamics AX 2012 R3 with KB 3105973 (released November 2, 2015) or later, and to Microsoft Dynamics 365 for Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Þessi grein á við um Microsoft Dynamics AX 2012 R3 með KB 3105973 (gefin út 2. nóvember 2015) eða síðar og við Microsoft Dynamics 365 for Retail.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>To determine the combination overlapping discounts to apply in a timely manner, we have introduced a method for applying overlapping discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Við höfum innleitt aðferð til að nota afslætti sem skarast, til að hægt sé að ákvarða samsetningu afsláttar sem skarast tímanlega.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>We call this new method <bpt id="p1">**</bpt>marginal value ranking<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Við köllum þessa nýju aðferð <bpt id="p1">**</bpt>Röðun jaðarvirðis<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Marginal value ranking is used when the time that is required in order to evaluate the possible combinations of overlapping discounts exceeds a threshold that is configurable on the <bpt id="p1">**</bpt>Retail parameters<ept id="p1">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Röðun jaðarvirðis er notuð þegar tíminn sem er nauðsynlegur til að meta mögulegar samsetningar á afslætti sem skarast fer yfir þröskuld sem er gerður skilgreinanlegur á síðunni <bpt id="p1">**</bpt>Færibreytur í Retail<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>In the marginal value ranking method, a value is calculated for each overlapping discount by using the discount's value on the shared products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Í röðun jaðarvirðis, er virði reiknað fyrir hvern afslátt sem skarast með því að nota virði afsláttar á samnýttar afurðir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>The overlapped discounts are then applied from the highest relative value to the lowest relative value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Afsláttur sem skarast gildir síðan úr tengdu hæsta hlutfallslega virði gegn lægsta hlutfallslega virði.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>For details about the new method, see the "Marginal value" section, later in this article.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Nánari upplýsingar um nýju greiðsluaðferðina er að finna í hlutanum „Jaðarvirði" síðar í þessari grein.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Marginal value ranking isn't used when the discount amounts for a product aren't affected by another product in the transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Röðun jaðarvirðis er ekki notað þegar afsláttarupphæðir afurðar verða ekki fyrir áhrifum af annarri afurð í færslunni.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>For example, this method isn't used for two simple discounts, or for a simple discount and a single product quantity discount.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Til dæmis er þessi aðferð ekki notuð fyrir tvo einfalda afslætti eða fyrir einfaldan afslátt og magnafslátt einnar afurðar.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Discount examples</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dæmi um afslætti</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>You can create an unlimited number of retail discounts on a common set of products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hægt er að stofna ótakmarkaðan fjölda af smásöluafsláttum í sameiginlegu safni afurða.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>However, because there is no limit, performance issues can occur when you try to calculate the discounts that should be used on the various products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hins vegar, þar sem engin takmörk eru geta afkastavandamál átt sér stað þegar reynt er að reikna út afslætti sem nota á mismunandi afurðir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>The following examples illustrate this issue in more detail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Eftirfarandi dæmi sýna vandamálið nánar.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>In example 1, we start with two products and two overlapping discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Í dæmi 1 er byrjum við með tvær vörur og tvo afslætti sem skarast.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Then, in example 2, we show how the issue evolves as more products are added.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Síðan, í dæmi 2 mælt er sýnt hvernig vandamálið þróast eftir því sem fleiri afurðum er bætt við.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Example 1: Two products and two discounts</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dæmi 1: Tvær vörur og tveir afslættir</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>In this example, two products are required in order to qualify for each discount, and the discounts can't be combined.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Í þessu dæmi eru tvær afurðir nauðsynlegar til þess að vera hæfar fyrir hvern afslátt og ekki er hægt að sameina afslættina.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>The discounts in this example are <bpt id="p1">**</bpt>Best price<ept id="p1">**</ept> discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Afslættir í þessu dæmi eru afslættir af <bpt id="p1">**</bpt>Besta verð<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Both products qualify for both discounts.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Báðar afurðir eru hæfar fyrir báða afslætti.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Here are the two discounts.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Hér eru þessir tveir afslættir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Example of two Best price discounts</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dæmi um tvo afslætti besta verðs</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>For any two products, the better of these two discounts depends on the prices of the two products.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Fyrir hvaða tvær afurðir sem er, fer sá betri af tveimur afsláttum eftir verðum afurðanna tveggja.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>When the price of both products is equal or almost equal, discount 1 is better.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Þegar verð bæði afurðir er jafnt og eða nánast það sama er betra afsláttur 1.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>When the price of one product is significantly less than the price of the other product, discount 2 is better.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Þegar verð einni afurð er mikil minna en verð á vöru, er betra afsláttur 2.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Here is the mathematical rule for evaluating these two discounts against each other.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Hér er stærðfræðileg regla fyrir mat á þessum tveimur afsláttum gagnvart hvor öðrum.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Rule for evaluating the discounts</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Regla um mat á afsláttum</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>When the price of product 1 is equal to two-thirds of the price of product 2, the two discounts are equal.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Þegar verð afurðar 1 jafnast á við tvo þriðju hluta af verði afurðar 2, eru þessir tveir afslættir jafnir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>In this example, the effective discount percentage for discount 1 varies from a few percent (when the prices of the two products are far apart) to a maximum of 25 percent (when the two products have the same price).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Í þessu dæmi, er gild afsláttarprósenta fyrir afslátt 1 breytileg um nokkur prósent (þegar mikill munur er á verði afurðanna tveggja) að hámarki 25 prósent (þegar afurðnar tvær hafa sama verð).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>The effective discount percentage for discount 2 is fixed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Gildi afsláttarprósentu fyrir afslátt 2 er föst.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>It's always 20 percent.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Það er alltaf 20 prósent.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Because the effective discount percentage for discount 1 has a range that can be more than or less than discount 2, the best discount depends on the prices of the two products that must be discounted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Þar sem gildi afsláttarprósentu fyrir afslátt 1 hefur svið sem getur verið meira en eða minna en 2 afsláttur, fer besti afslátturinn eftir verði afurðanna tveggja sem verða að hafa afslátt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>In this example, the calculation is completed quickly, because only two discounts are applied on only two products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Í þessu dæmi er útreikningi lokið á fljótlegan hátt, þar sem aðeins þessum tveimur afsláttum er beitt á aðeins tvær afurðir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>There are only two possible combinations: one application of discount 1 or one application of discount 2.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Það eru tvær aðeins mögulegar samsetningar: ein notkun á afsláttur 1 eða ein notkun á afsláttar 2.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>There are no permutations to calculate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Það er engin umröðun til að reikna.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>The value of each discount is calculated by using both products, and the best discount is used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Virði hvors afsláttar er reiknað með því að nota báðar afurðir og besti afslátturinn er notaður.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Example 2: Four products and two discounts</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dæmi 2: Fjórar vörur og tveir afslættir</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Next, we will use four products and the same two discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Næst notum við fjórar afurðir og sama þessum tveimur afsláttum.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>All four products qualify for both discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Allar fjórar afurðirnar eru hæfar fyrir báða afslætti.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>There are twelve possible combinations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Það eru tólf mögulegar samsetningar.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>In the end, two discounts will be applied to the transaction in one of three combinations: two applications of discount 1, two applications of discount 2, or one application of discount 1 and one application of discount 2.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Í lokin verða tveir afsláttum notað í færslunni í einni af þremur samsetningum: tvær beitingar á afslætti 1, tvær beitingar afslætti 2, eða ein beiting á afslætti 1 og ein beiting á afslætti 2.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>To illustrate the possible combinations, we will look at two different sets of four products that have different prices:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Til að sýna mögulegar samsetningar, lítum við þvínæst á tvö mismunandi pör fjögurra afurða sem hafa mismunandi verð:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>All four products have the same price, $15.00.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Allar fjórar afurðir hafa sama verð $15,00.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>In this case, the best discount combination is two applications of discount 1.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Í þessu tilfelli er besta samsetning afsláttur tvær beitingar á afsláttar 1.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Two products will be full price, and two will be 50 percent off.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tvær afurðir verða á fullu verði og tvær verða með 50 prósent afslætti.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>The discounted total for the transaction is $45 (15 + 15 + 7.50 + 7.50), which is $15 (25 percent) off the undiscounted total of $60.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Samtala með afslætti færslunnar er $45 (15 + 15 + 7,50 + 7,50), sem er $15 (25 prósent) af samtala $60 án afsláttar.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>Discount 2 is only $12 (20 percent).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Afsláttur 2 er aðeins $12 (20 prósent).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Two products are $20 each, one product is $15, and one product is $5.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tvær afurðir eru $20 hvor, ein afurð er $15 og ein afurð er $5.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>In this case, the best discount combination is one application of discount 2 and one application of discount 1.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Í þessu tilfelli er besta afsláttarsamsetningin ein beiting á afsláttur 2 og ein beiting á afsláttar 1.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>The following tables illustrates the discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Eftirfarandi töflur sýnir afslættina.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>To read the tables, use one product from a row and one product from a column.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Til að lesa töflurnar þarf að nota eina afurð úr línu og eina vöru úr dálki.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>For example, in the table for discount 1, when you combine the two $20 products, you get $10 off.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Til dæmis í töflunni fyrir afslátt 1, þegar tvær $20 afurðir eru sameinaðar færðu $10 í afslátt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>In the table for discount 2, when you combine the $15 product and the $5 product, you get $4 off.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Til dæmis í töflunni fyrir afslátt 2, þegar $15 afurð og $5 afurð eru sameinaðar færðu $4 í afslátt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Example that uses four products for the same two discounts</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dæmi sem notar fjórar vörur fyrir sömu tvo afslættina</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>First, we find the largest discount that is available from any two products by using either discount.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Fyrst finnum við hæsta afsláttinn sem er í boði úr hvaða tveimur afurðum sem er með því að nota annan hvorn afsláttinn.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>The two tables show the discount amount for all combinations of the two products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Töflurnar tvær sýna afsláttarupphæð fyrir allar samsetningar á afurðunum tveimur.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>The shaded portions of the tables represent either cases where a product is paired with itself, which we can't do, or a reverse pairing of two products that produces the same discount amount and can be ignored.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Skyggðu hlutar töflunnar tákna annaðhvort tilfelli þar sem afurð er pöruð með sjálfri sér, sem við getum ekki gert, eða er bakfærð pörun tveggja afurða sem verður að sömu afsláttarupphæð og má hunsa.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>By looking at the tables, you can see that discount 1 for the two $20 items is the largest discount that is available for either discount on all four products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Með því að líta á töflur, hægt er að sjá að afsláttur 1 fyrir tvær vörur á $20 er stærsti afsláttar sem er tiltækt fyrir annað hvort afslætti á allar fjórar afurðir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>(This discount is highlighted in green in the first table.) That leaves only the $15 product and the $5 product.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(Þessi afsláttur er upplýstur með grænu í fyrstu töflunni.) Þá eru aðeins $15 afurðin og $5 afurðin eftir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>By looking at the two tables again, you can see that, for these two products, discount 1 gives a $2.50 discount, whereas discount 2 gives a $4 discount.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Með því að líta á tvær töflurnar aftur er hægt að sjá að fyrir þessar tvær afurðir veitir afsláttur 1 $2,50 afslátt, en afsláttur 2 veitir aftur á móti $4 afslátt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Therefore, we select discount 2.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Þess vegna veljum við afslátt 2.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>The total discount is $14.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Heildarafslátturinn er $14.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>To make this discussion easier to visualize, here are two additional tables that show the effective discount percentage for all possible two-product combinations for both discount 1 and discount 2.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Til að auðvelda að gera þessa umræðu sér í hugarlund eru hér tvær viðbótartöflur sem sýna gildi afsláttarprósentu fyrir allar mögulegar tveggja afurða samsetningar fyrir bæði afsláttur 1 og 2 afsláttar.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>Only half the list of combinations is included, because, for these two discounts, the order in which the two products are put into the discount doesn't matter.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Aðeins helmingurinn af lista með samsetningum er hafður með, því að fyrir þessa tvo afslætti skiptir ekki máli í hvaða röð í afslættinum afurðirnar tvær eru settar í.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>The highest effective discount (25 percent) is highlighted in green, and the lowest effective discount (10 percent) is highlighted in red.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Hæsta gildi afsláttar (25%) er upplýst í grænu og lægsta gildi afsláttar (10 prósent) er upplýstur rauður.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>Effective discount percentage for all two-product combinations for both discounts</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Áhrifarík afsláttarprósenta fyrir allar samsetningar af tveimur vörur fyrir báða afslættina</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>When prices vary, and two or more discount compete, the only way to guarantee the best combination of discounts is to evaluate both discounts and compare them.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Þegar verð eru mismunandi og tveir eða fleiri afslættir keppa, er eina leiðin til að tryggja bestu samsetningu af afsláttum er að meta báða afslætti og bera þá saman.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Total possible combinations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Mögulegar samsetningar alls</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>This section continues the example from the previous section.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Þessi hluti heldur áfram með dæmi úr fyrri kafla.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>We will add more products and another discount, and see how many combinations must be calculated and compared.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Við munum bæta við fleiri afurðum og öðrum afslætti og sjá hversu margar samsetningar er hægt að reikna út og bera saman.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>The following table shows the number of possible discount combinations as the product quantity increases.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Eftirfarandi tafla sýnir fjölda mögulegra afsláttarsamsetninga eftir því sem afurðarmagn hækkar.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>The table shows what happens both when there are two overlapping discounts, as in the previous example, and when there are three overlapping discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Taflan sýnir hvað gerist bæði þegar það eru tveir afslættir sem skarast, eins og í fyrra dæmi, og þegar það eru þrír afslættir sem skarast.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>The number of possible discount combinations that must be evaluated soon exceeds what even a fast computer can calculate and compare quickly enough to be acceptable for retail transactions.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Fjöldi mögulegar afsláttarsamsetningar sem þarf að meta fljótlega fer yfir það sem jafnvel fljótvirk tölva getur reiknað út og borið saman nógu fljótt til að vera viðunandi fyrir smásölufærslur.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>Number of possible discount combinations as the product quantity increases</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Fjöldi mögulegra afsláttarsamsetninga eftir því sem afurðarmagn hækkar</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>When even larger quantities or more overlapping discounts are applied, the total number of possible discount combinations quickly goes into the millions, and the time that is required in order to evaluate and select the best possible combination quickly becomes noticeable.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Þegar enn fleiri afslættir sem skarast eru notaðir, fer heildarfjöldi mögulegra afsláttasamsetninga fljótlega í milljónir, og tíminn sem þarf til að meta og velja bestu mögulegu samsetninguna verður fljótlega tilfinnanlegur.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>Some optimizations have been done in the retail price engine to reduce the total number of combinations that must be evaluated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Einhver fínstilling hefur verið gert í smásöluverðsvélinni til að draga úr þeim heildarfjölda samsetninga sem þarf að meta.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>However, because the number overlapping discounts and the quantities in a transaction aren't limited, a large number of combinations will always have to be evaluated whenever there are overlapping discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hins vegar, þar sem fjöldi afslátta sem skarast og magns í færslu eru ekki takmörkuð, mun mikill fjöldi samsetninga alltaf verða að vera metinn í hvert skipti sem afslættir skarast.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>This issue is the issue that the marginal value ranking method addresses.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Þetta vandamál er vandamál sem aðferð röðunar jaðarvirðis tekur á.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>Marginal value method</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Aðferð jaðarvirðis</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>To resolve the issue of an exponentially increasing number of combinations that must be evaluated, an optimization exists that calculates the value per shared product of each discount on the set of products that two or more discounts can be applied to.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Til að leysa vandamál stigveldisvaxandi fjölda samsetninga sem þarf að meta, eru fínstillingar til staðar sem reikna virði á samnýttrar afurðar á hverja afsláttur á hóp afurða sem hægt er að nota tvær eða fleiri afslætti á.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>We refer to this value as the <bpt id="p1">**</bpt>marginal value<ept id="p1">**</ept> of the discount for the shared products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Við vísum til þessa virðis sem <bpt id="p1">**</bpt>jaðarvirðis<ept id="p1">**</ept> afsláttar fyrir samnýttar afurðir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>The marginal value is the average per product increase in the total discount amount when the shared products are included in each discount.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Jaðarvirði er meðaltal á afurðahækkun í heildarupphæð afsláttar þegar samnýttar afurðir eru taldar með fyrir hvern afslátt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>The marginal value is calculated by taking the total discount amount (DTotal), subtracting the discount amount without the shared products (DMinus<ph id="ph1">\\</ph> Shared), and dividing that difference by the number of shared products (ProductsShared).</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Jaðarvirði er reiknað með því að taka afsláttarupphæð samtals (DTotal), draga frá afsláttarupphæð án samnýtta afurðir (DMinus<ph id="ph1">\\</ph> Samnýttum), og deila þeim mismun með fjölda samnýtta afurða (ProductsShared).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>Formula for calculating marginal value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Formúla til að reikna út jaðarvirði</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>After the marginal value of each discount on a shared set of products is calculated, the discounts are applied to the shared products in order, exhaustively, from highest marginal value to lowest marginal value.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Eftir að jaðarvirði fyrir hvern afslátt á samnýtta hópa afurða hefur verið reiknað út, er afsláttum beitt á samnýttar afurðir í tæmandi röð frá hæsta jaðarvirði til lægsta jaðarvirðis.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>For this method, all remaining discount possibilities aren't compared every time after a single instance of a discount is applied.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Fyrir þessa aðferð eru allir eftirstandandi afsláttarmöguleikar ekki bornir saman í hvert skipti sem eitt tilvik afsláttar er sett á.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>Instead, the overlapping discounts are compared one time and then applied in order.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Þess í stað eru afslættir sem skarast bornir saman einu sinni og síðan notað í röð.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>No additional comparisons are done.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Enginn viðbótarsamanburður er gerður.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>You can configure the threshold to switch to the marginal value method on the <bpt id="p1">**</bpt>Discount<ept id="p1">**</ept> tab of the <bpt id="p2">**</bpt>Retail parameters<ept id="p2">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hægt er að skilgreina þröskuld til að skipta yfir í aðferð jaðarvirðis á flipanum <bpt id="p1">**</bpt>Afsláttur<ept id="p1">**</ept> á síðunni <bpt id="p2">**</bpt>Færibreytur Retail<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>The acceptable time to calculate the total discount varies across retail industries.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Viðunandi tími til að reikna heildarafslátt er breytilegur milli atvinnugreina smásölu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>However, this time generally falls in the range of tens of milliseconds to one second.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hins vegar er þessi tími almennt á bili tíu millisekúnda til einnar sekúndu.</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>