<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="cost.md" target-language="is-is">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>cost.4e88df.80e7a033467c3d94d55f06daa05f99bd27e19a29.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>80e7a033467c3d94d55f06daa05f99bd27e19a29</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>e2fb0846fcc6298050a0ec82c302e5eb5254e0b5</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/27/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\cost.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Cost configuration for distributed order management (DOM)</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Skilgreining kostnaðar fyrir dreifingarstjórnun pöntunar (DOM)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes cost configuration for the distributed order management (DOM) functionality in Microsoft Dynamics 365 for Retail.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Þetta efnisatriði lýsir skilgreiningu kostnaðar fyrir virkni dreifingarstjórnunar pöntunar (DOM) í Microsoft Dynamics 365 for Retail.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Cost configuration for distributed order management (DOM)</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">Skilgreining kostnaðar fyrir dreifingarstjórnun pöntunar (DOM)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Organizations consider multiple cost components to determine the optimal location to fulfill an order from.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Fyrirtæki íhuga marga kostnaðaríhluti til að ákvarða bestu staðsetninguna til að uppfylla pöntun frá.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Some of these cost components are shipping cost, handling cost, and packaging cost.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Sumir þessara kostnaðaríhluta eru sendingarkostnaður, úrvinnslukostnaður og pökkunarkostnaður.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>A combination of these costs is calculated to determine the fulfillment location.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Samsetning þessa kostnaðar er reiknaður til að ákvarða uppfyllingarstaðsetningu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>When the first iteration of distributed order management (DOM) in Microsoft Dynamics 365 for Retail optimized the assignment of orders to fulfillment locations, it factored in distance only.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Þegar fyrsta ítrekun úthlutaðrar pantanastjórnunar (DOM) í Microsoft Dynamics 365 for Retail fínstillti úthlutun pantana á uppfyllingarstaðsetningar var eingöngu vegalengd tekin með í reikninginn.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Although distance can be correlated with cost, it isn't the same as cost.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Vegalengd er ekki það sama og kostnaður þótt hægt sé að gera ráð fyrir henni í kostnaði.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>For example, an overnight shipping method costs more than three-day shipping or seven-day shipping over the same distance.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Til dæmis kostar sendingarmáti að næturlagi meira en þriggja daga sending eða sjö daga sending sem felur í sér sömu vegalengdina.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>The cost configuration feature lets retailers define and configure additional cost components that will be calculated and factored in to determine the optimal location to fulfill order lines from.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Eiginleiki kostnaðarskilgreiningar gerir söluaðilum kleift að skilgreina og grunnstilla aukalega kostnaðaríhluti sem verða reiknaðir og hafðir með til að ákvarða bestu staðsetninguna til að uppfylla pöntunarlínur frá.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>When cost components are configured, the DOM solver uses only those cost definitions to determine the optimal location for order fulfillment.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Þegar kostnaðaríhlutir eru skilgreindir notar DOM-leysarinn eingöngu þessar kostnaðarskilgreiningar til að ákvarða bestu staðsetninguna til að uppfylla pöntun.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>It doesn't consider the distance component as a cost.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Hann tekur ekki vegalengd inn sem kostnað.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>However, if no cost components are configured, the DOM solver does use the distance component as a cost to determine the optimal location for order fulfillment.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Ef hins vegar engir kostnaðaríhlutir eru skilgreindir notar DOM-leysarinn vegalengd sem kostnað til að ákvarða bestu staðsetninguna til að uppfylla pöntun.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Set up cost components</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Uppsetning kostnaðaríhluta</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Two major cost component types can be defined in the system: <bpt id="p1">**</bpt>Shipping<ept id="p1">**</ept> and <bpt id="p2">**</bpt>Other<ept id="p2">**</ept>.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Hægt er að skilgreina tvær megingerðir kostnaðaríhluta í kerfinu: <bpt id="p1">**</bpt>Sending<ept id="p1">**</ept> og <bpt id="p2">**</bpt>Annað<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Both cost component types support multiple calculation bases, as shown in the following table.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Báðar gerðir kostnaðaríhluta styðja marga útreikningsgrunna eins og sýnt er í eftirfarandi töflu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Cost component type</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Gerð kostnaðaríhlutar</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Calculation basis</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Grunnur útreikninga</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Shipping</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Sending</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Simple</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Einfalt</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Tiered</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Lagskipt</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Other</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Annað</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Sales order</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Sölupöntun</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Sales line</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Sölulínur</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Location</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Staðsetning</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Shipping cost component type</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Gerð íhlutar fyrir sendingarkostnað</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>This section explains how to set up each combination of the <bpt id="p1">**</bpt>Shipping<ept id="p1">**</ept> cost component type and a calculation basis for shipping costs.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Þessi hluti útskýrir hvernig á að setja upp hverja samsetningu fyrir sig fyrir kostnaðaríhlut af gerðinni <bpt id="p1">**</bpt>Sending<ept id="p1">**</ept> og útreikningsgrunn fyrir sendingarkostnað.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>It also explains how the DOM solver uses each combination.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Þar er einnig útskýrt hvernig DOM-leysarinn notar hverja samsetningu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Cost component type = Shipping and Calculation basis = Simple</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Gerð kostnaðaríhlutar = sending og útreikningsgrunnur = einfaldur</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>If a combination of the <bpt id="p1">**</bpt>Shipping<ept id="p1">**</ept> cost component type and the <bpt id="p2">**</bpt>Simple<ept id="p2">**</ept> calculation basis is used, the shipping cost for a mode of delivery is based on either a flat cost or distance.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Ef samsetning kostnaðaríhlutar af gerðinni <bpt id="p1">**</bpt>Sending<ept id="p1">**</ept> og útreikningsgrunnurinn <bpt id="p2">**</bpt>Einfaldur<ept id="p2">**</ept> er notuð byggist sendingarkostnaður fyrir afhendingarmáta annaðhvort á flötum kostnaði eða vegalengd.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>You must set up the following fields for this combination:</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Setja verður upp eftirfarandi reiti fyrir þessa samsetningu:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source><bpt id="p1">**</bpt>Cost factor<ept id="p1">**</ept> – Enter a unique identifier for the cost factor.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">**</bpt>Kostnaðarstuðull<ept id="p1">**</ept> – Færið inn einkvæmt kennimerki fyrir kostnaðarstuðul.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source><bpt id="p1">**</bpt>Description<ept id="p1">**</ept> – Enter the name and description of the cost factor.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">**</bpt>Lýsing<ept id="p1">**</ept> – Færið inn heiti og lýsingu á kostnaðarstuðli.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source><bpt id="p1">**</bpt>Start date<ept id="p1">**</ept> and <bpt id="p2">**</bpt>End date<ept id="p2">**</ept> – You can use these fields to limit the cost factor for a specific date range.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">**</bpt>Upphafsdagur<ept id="p1">**</ept> og <bpt id="p2">**</bpt>Lokadagur<ept id="p2">**</ept> – Hægt er að nota þessa reiti til að takmarka kostnaðarstuðul fyrir tiltekið tímabil.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>If you leave these fields blank, the cost factor is valid for an indefinite period.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Ef þessir reitir eru skildir eftir auðir gildir kostnaðarstuðullinn um óákveðinn tíma.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source><bpt id="p1">**</bpt>Active<ept id="p1">**</ept> – Indicate whether the cost factor is active.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">**</bpt>Virkur<ept id="p1">**</ept> – Segið til um hvort kostnaðarstuðull sé virkur.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>The DOM considers only active cost factors that are associated with the fulfillment profile.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">DOM tekur aðeins virka kostnaðarstuðla til greina sem tengjast uppfyllingarsniði.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source><bpt id="p1">**</bpt>Company<ept id="p1">**</ept> – Specify the legal entity that the cost factor is configured for.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">**</bpt>Fyrirtæki<ept id="p1">**</ept> – Tilgreinið lögaðila sem kostnaðarstuðull er skilgreindur fyrir.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>All lines of the calculation criteria must be for the same legal entity.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Allar línur útreikningsskilyrðis verður að vera fyrir sama lögaðilann.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source><bpt id="p1">**</bpt>Modes of delivery<ept id="p1">**</ept> – Specify the modes of delivery that the cost is configured for.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">**</bpt>Afhendingarmátar<ept id="p1">**</ept> – Tilgreinið afhendingarmáta sem kostnaður er skilgreindur fyrir.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source><bpt id="p1">**</bpt>Calculation type<ept id="p1">**</ept> – Specify how the cost should be calculated for a specific mode of delivery.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">**</bpt>Gerð útreiknings<ept id="p1">**</ept> – Tilgreinið hvernig reikna eigi kostnað fyrir tiltekinn afhendingarmáta.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Two calculation types are supported:</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Tvær gerðir útreiknings eru studdar:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source><bpt id="p1">**</bpt>Fixed<ept id="p1">**</ept> – A flat cost is used for the mode of delivery.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">**</bpt>Fastur<ept id="p1">**</ept> – Flatur kostnaður er notaður fyrir afhendingarmáta.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>If you select this calculation type, the <bpt id="p1">**</bpt>Cost<ept id="p1">**</ept> field defines the flat cost.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Ef þessi útreikningsgerð er valin skilgreinir reiturinn <bpt id="p1">**</bpt>Kostnaður<ept id="p1">**</ept> flatan kostnað.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source><bpt id="p1">**</bpt>Per-distance unit<ept id="p1">**</ept> – The cost for the mode of delivery is calculated as the cost value that is specified in the <bpt id="p2">**</bpt>Cost<ept id="p2">**</ept> field times the distance between the delivery address and the locations.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">**</bpt>Á hverja fjarlægðareiningu<ept id="p1">**</ept> – Kostnaður fyrir afhendingarmáta er reiknaður sem kostnaðarvirðið sem er skilgreint í reitnum <bpt id="p2">**</bpt>Kostnaður<ept id="p2">**</ept> margfaldað með vegalengdinni milli afhendingaraðseturs og staðsetningar.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source><bpt id="p1">**</bpt>Cost<ept id="p1">**</ept> – Specify the cost value that is used in conjunction with the <bpt id="p2">**</bpt>Calculation type<ept id="p2">**</ept> field to compute the cost for a mode of delivery.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">**</bpt>Kostnaður<ept id="p1">**</ept> – Tilgreinið kostnaðarvirði sem er notað í tengslum við reitinn <bpt id="p2">**</bpt>Gerð útreiknings<ept id="p2">**</ept> til að reikna út kostnað á afhendingarmáta.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Cost component type = Shipping and Calculation basis = Tiered</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Gerð kostnaðaríhlutar = sending og útreikningsgrunnur = lagskiptur</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>If a combination of the <bpt id="p1">**</bpt>Shipping<ept id="p1">**</ept> cost component type and the <bpt id="p2">**</bpt>Tiered<ept id="p2">**</ept> calculation basis is used, the shipping cost for a mode of delivery is based on either a flat cost or distance.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Ef samsetning kostnaðaríhlutar af gerðinni <bpt id="p1">**</bpt>Sending<ept id="p1">**</ept> og útreikningsgrunnurinn <bpt id="p2">**</bpt>Lagskiptur<ept id="p2">**</ept> er notuð byggist sendingarkostnaður fyrir afhendingarmáta annaðhvort á flötum kostnaði eða vegalengd.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>However, in this combination, the distance is based on a tiered range of distances.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Í þessari samsetningu byggist vegalengdin hins vegar á lagskiptu fjarlægðarbili.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>You must set up the following fields for this combination:</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">Setja verður upp eftirfarandi reiti fyrir þessa samsetningu:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source><bpt id="p1">**</bpt>Cost factor<ept id="p1">**</ept> – Enter a unique identifier for the cost factor.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Kostnaðarstuðull<ept id="p1">**</ept> – Færið inn einkvæmt kennimerki fyrir kostnaðarstuðul.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source><bpt id="p1">**</bpt>Description<ept id="p1">**</ept> – Enter the name and description of the cost factor.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Lýsing<ept id="p1">**</ept> – Færið inn heiti og lýsingu á kostnaðarstuðli.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source><bpt id="p1">**</bpt>Default cost<ept id="p1">**</ept> – Specify the cost that should be used for a mode of delivery if the distance between the delivery address and the location doesn't fall into any of the tiered distances for the mode of delivery.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">**</bpt>Sjálfgefinn kostnaður<ept id="p1">**</ept> – Tilgreinið kostnað sem á að nota fyrir afhendingarmáta ef vegalengdin milli afhendingaraðseturs og staðsetningar fellur ekki undir neina af lagskiptu vegalengdunum fyrir afhendingarmáta.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source><bpt id="p1">**</bpt>Start date<ept id="p1">**</ept> and <bpt id="p2">**</bpt>End date<ept id="p2">**</ept> – You can use these fields to limit the cost factor for a specific date range.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Upphafsdagur<ept id="p1">**</ept> og <bpt id="p2">**</bpt>Lokadagur<ept id="p2">**</ept> – Hægt er að nota þessa reiti til að takmarka kostnaðarstuðul fyrir tiltekið tímabil.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>If you leave these fields blank, the cost factor is valid for an indefinite period.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">Ef þessir reitir eru skildir eftir auðir gildir kostnaðarstuðullinn um óákveðinn tíma.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source><bpt id="p1">**</bpt>Active<ept id="p1">**</ept> – Indicate whether the cost factor is active.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Virkur<ept id="p1">**</ept> – Segið til um hvort kostnaðarstuðull sé virkur.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>The DOM considers only active cost factors that are associated with the fulfillment profile.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">DOM tekur aðeins virka kostnaðarstuðla til greina sem tengjast uppfyllingarsniði.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source><bpt id="p1">**</bpt>Company<ept id="p1">**</ept> – Specify the legal entity that the cost factor is configured for.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Fyrirtæki<ept id="p1">**</ept> – Tilgreinið lögaðila sem kostnaðarstuðull er skilgreindur fyrir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>All lines of the calculation criteria must be for the same legal entity.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">Allar línur útreikningsskilyrðis verður að vera fyrir sama lögaðilann.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source><bpt id="p1">**</bpt>Modes of delivery<ept id="p1">**</ept> – Specify the modes of delivery that the cost is configured for.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Afhendingarmátar<ept id="p1">**</ept> – Tilgreinið afhendingarmáta sem kostnaður er skilgreindur fyrir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source><bpt id="p1">**</bpt>Distance type<ept id="p1">**</ept> – Specify whether the tiered distance definition is an aerial distance or a road distance.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">**</bpt>Tegund vegalengdar<ept id="p1">**</ept> – Tilgreinið hvort skilgreining á lagskiptri vegalengd sé fyrir flug eða akstur.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source><bpt id="p1">**</bpt>Distance units<ept id="p1">**</ept> – Specify the unit that the tiered distance is measured in.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">**</bpt>Fjarlægðareiningar<ept id="p1">**</ept> – Tilgreinið einingu sem lagskipt vegalengd er mæld í.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source><bpt id="p1">**</bpt>Distance from<ept id="p1">**</ept> – Specify the start range for the tiered distance.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">**</bpt>Fjarlægð frá<ept id="p1">**</ept> – Tilgreinið upphafsbil fyrir lagskipta vegalengd.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source><bpt id="p1">**</bpt>Distance to<ept id="p1">**</ept> – Specify the end range for the tiered distance.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">**</bpt>Fjarlægð til<ept id="p1">**</ept> – Tilgreinið lokabil fyrir lagskipta vegalengd.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source><bpt id="p1">**</bpt>Calculation type<ept id="p1">**</ept> – Specify how the cost should be calculated for a specific mode of delivery and tiered distance.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">**</bpt>Gerð útreiknings<ept id="p1">**</ept> – Tilgreinið hvernig reikna eigi kostnað fyrir tiltekinn afhendingarmáta og lagskipta vegalengd.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Two calculation types are supported:</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">Tvær gerðir útreiknings eru studdar:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source><bpt id="p1">**</bpt>Fixed<ept id="p1">**</ept> – A flat cost is used for the mode of delivery.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Fastur<ept id="p1">**</ept> – Flatur kostnaður er notaður fyrir afhendingarmáta.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>If you select this calculation type, the <bpt id="p1">**</bpt>Cost<ept id="p1">**</ept> field defines the flat cost.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">Ef þessi útreikningsgerð er valin skilgreinir reiturinn <bpt id="p1">**</bpt>Kostnaður<ept id="p1">**</ept> flatan kostnað.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source><bpt id="p1">**</bpt>Per distance unit<ept id="p1">**</ept> – The cost for the mode of delivery and tiered distance is calculated as the cost value that is specified in the <bpt id="p2">**</bpt>Cost<ept id="p2">**</ept> field times the distance between the delivery address and the locations.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">**</bpt>Á hverja fjarlægðareiningu<ept id="p1">**</ept> – Kostnaður fyrir afhendingarmáta og lagskipta vegalengd er reiknaður sem kostnaðarvirðið sem er skilgreint í reitnum <bpt id="p2">**</bpt>Kostnaður<ept id="p2">**</ept> margfaldað með vegalengdinni milli afhendingaraðseturs og staðsetningar.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source><bpt id="p1">**</bpt>Cost<ept id="p1">**</ept> – Specify the cost value that is used in conjunction with the <bpt id="p2">**</bpt>Calculation type<ept id="p2">**</ept> field to compute the cost for a mode of delivery.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Kostnaður<ept id="p1">**</ept> – Tilgreinið kostnaðarvirði sem er notað í tengslum við reitinn <bpt id="p2">**</bpt>Gerð útreiknings<ept id="p2">**</ept> til að reikna út kostnað á afhendingarmáta.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>When you define tiered distances, the system validates that there are no missing or overlapping distances.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Þegar lagskiptar vegalengdir eru skilgreindar sannprófar kerfið hvort vegalengdir vanti eða þær skarist á.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>The distance type that is used for a mode of delivery must be the same across all the tiered distances.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Tegund vegalengdar sem er notuð fyrir afhendingarmáta verður að vera sú sama fyrir allar lagskiptu vegalengdirnar.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Other cost component type</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Önnur gerð kostnaðaríhlutar</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>This section explains how to set up each combination of the <bpt id="p1">**</bpt>Other<ept id="p1">**</ept> cost component type and an other cost type for non-shipping costs.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Þessi hluti útskýrir hvernig á að setja upp hverja samsetningu fyrir sig fyrir kostnaðaríhlut af gerðinni <bpt id="p1">**</bpt>Annar<ept id="p1">**</ept> og aðra kostnaðargerð fyrir kostnað án sendingar.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>It also explains how the DOM solver uses each combination.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">Þar er einnig útskýrt hvernig DOM-leysarinn notar hverja samsetningu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>Cost component type = Other and Other cost type = Sales order</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Gerð kostnaðaríhlutar = annar og önnur kostnaðargerð = sölupöntun</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>A combination of the <bpt id="p1">**</bpt>Other<ept id="p1">**</ept> cost component type and the <bpt id="p2">**</bpt>Sales order<ept id="p2">**</ept> other cost type is used to define non-shipping costs at the sales order level.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Samsetning fyrir kostnaðaríhlut af gerðinni <bpt id="p1">**</bpt>Annar<ept id="p1">**</ept> og annan kostnað af gerðinni <bpt id="p2">**</bpt>Sölupöntun<ept id="p2">**</ept> er notuð til að skilgreina kostnað án sendingar á stigi sölupöntunar.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>You must set up the following fields for this combination:</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">Setja verður upp eftirfarandi reiti fyrir þessa samsetningu:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source><bpt id="p1">**</bpt>Cost factor<ept id="p1">**</ept> – Enter a unique identifier for the cost factor.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Kostnaðarstuðull<ept id="p1">**</ept> – Færið inn einkvæmt kennimerki fyrir kostnaðarstuðul.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source><bpt id="p1">**</bpt>Description<ept id="p1">**</ept> – Enter the name and description of the cost factor.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Lýsing<ept id="p1">**</ept> – Færið inn heiti og lýsingu á kostnaðarstuðli.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source><bpt id="p1">**</bpt>Start date<ept id="p1">**</ept> and <bpt id="p2">**</bpt>End date<ept id="p2">**</ept> – You can use these fields to limit the cost factor for a specific date range.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Upphafsdagur<ept id="p1">**</ept> og <bpt id="p2">**</bpt>Lokadagur<ept id="p2">**</ept> – Hægt er að nota þessa reiti til að takmarka kostnaðarstuðul fyrir tiltekið tímabil.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>If you leave these fields blank, the cost factor is valid for an indefinite period.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">Ef þessir reitir eru skildir eftir auðir gildir kostnaðarstuðullinn um óákveðinn tíma.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source><bpt id="p1">**</bpt>Active<ept id="p1">**</ept> – Indicate whether the cost factor is active.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Virkur<ept id="p1">**</ept> – Segið til um hvort kostnaðarstuðull sé virkur.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>The DOM considers only active cost factors that are associated with the fulfillment profile.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">DOM tekur aðeins virka kostnaðarstuðla til greina sem tengjast uppfyllingarsniði.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source><bpt id="p1">**</bpt>Cost<ept id="p1">**</ept> – Specify the cost value for a non-shipping cost at the sales order level.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">**</bpt>Kostnaður<ept id="p1">**</ept> – Tilgreinið kostnaðarvirði fyrir kostnað án sendingar á stigi sölupöntunar.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Cost component type = Other and Other cost type = Sales line</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Gerð kostnaðaríhlutar = annar og önnur kostnaðargerð = sölulína</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>A combination of the <bpt id="p1">**</bpt>Other<ept id="p1">**</ept> cost component type and the <bpt id="p2">**</bpt>Sales line<ept id="p2">**</ept> other cost type is used to define non-shipping costs at the sales order line level.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Samsetning fyrir kostnaðaríhlut af gerðinni <bpt id="p1">**</bpt>Annar<ept id="p1">**</ept> og annan kostnað af gerðinni <bpt id="p2">**</bpt>Sölulína<ept id="p2">**</ept> er notuð til að skilgreina kostnað án sendingar á stigi sölulínu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>You must set up the following fields for this combination:</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">Setja verður upp eftirfarandi reiti fyrir þessa samsetningu:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source><bpt id="p1">**</bpt>Cost factor<ept id="p1">**</ept> – Enter a unique identifier for the cost factor.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Kostnaðarstuðull<ept id="p1">**</ept> – Færið inn einkvæmt kennimerki fyrir kostnaðarstuðul.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source><bpt id="p1">**</bpt>Description<ept id="p1">**</ept> – Enter the name and description of the cost factor.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Lýsing<ept id="p1">**</ept> – Færið inn heiti og lýsingu á kostnaðarstuðli.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source><bpt id="p1">**</bpt>Start date<ept id="p1">**</ept> and <bpt id="p2">**</bpt>End date<ept id="p2">**</ept> – You can use these fields to limit the cost factor for a specific date range.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Upphafsdagur<ept id="p1">**</ept> og <bpt id="p2">**</bpt>Lokadagur<ept id="p2">**</ept> – Hægt er að nota þessa reiti til að takmarka kostnaðarstuðul fyrir tiltekið tímabil.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>If you leave these fields blank, the cost factor is valid for an indefinite period.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">Ef þessir reitir eru skildir eftir auðir gildir kostnaðarstuðullinn um óákveðinn tíma.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source><bpt id="p1">**</bpt>Active<ept id="p1">**</ept> – Indicate whether the cost factor is active.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Virkur<ept id="p1">**</ept> – Segið til um hvort kostnaðarstuðull sé virkur.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>The DOM considers only active cost factors that are associated with the fulfillment profile.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">DOM tekur aðeins virka kostnaðarstuðla til greina sem tengjast uppfyllingarsniði.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source><bpt id="p1">**</bpt>Cost<ept id="p1">**</ept> – Specify the cost value for a non-shipping cost at the sales order line level.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">**</bpt>Kostnaður<ept id="p1">**</ept> – Tilgreinið kostnaðarvirði fyrir kostnað án sendingar á stigi sölupöntunarlínu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>Cost component type = Other and Other cost type = Location</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Gerð kostnaðaríhlutar = annar og önnur kostnaðargerð = staðsetning</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>A combination of the <bpt id="p1">**</bpt>Other<ept id="p1">**</ept> cost component type and the <bpt id="p2">**</bpt>Location<ept id="p2">**</ept> other cost type is used to define non-shipping costs for a group of locations or an individual location.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Samsetning fyrir kostnaðaríhlut af gerðinni <bpt id="p1">**</bpt>Annar<ept id="p1">**</ept> og annan kostnað af gerðinni <bpt id="p2">**</bpt>Staðsetning<ept id="p2">**</ept> er notuð til að skilgreina kostnað án sendingar fyrir flokk staðsetninga eða eina staðsetningu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>You must set up the following fields for this combination:</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">Setja verður upp eftirfarandi reiti fyrir þessa samsetningu:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source><bpt id="p1">**</bpt>Cost factor<ept id="p1">**</ept> – Enter a unique identifier for the cost factor.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Kostnaðarstuðull<ept id="p1">**</ept> – Færið inn einkvæmt kennimerki fyrir kostnaðarstuðul.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source><bpt id="p1">**</bpt>Description<ept id="p1">**</ept> – Enter the name and description of the cost factor.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Lýsing<ept id="p1">**</ept> – Færið inn heiti og lýsingu á kostnaðarstuðli.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source><bpt id="p1">**</bpt>Start date<ept id="p1">**</ept> and <bpt id="p2">**</bpt>End date<ept id="p2">**</ept> – You can use these fields to limit the cost factor for a specific date range.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Upphafsdagur<ept id="p1">**</ept> og <bpt id="p2">**</bpt>Lokadagur<ept id="p2">**</ept> – Hægt er að nota þessa reiti til að takmarka kostnaðarstuðul fyrir tiltekið tímabil.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>If you leave these fields blank, the cost factor is valid for an indefinite period.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">Ef þessir reitir eru skildir eftir auðir gildir kostnaðarstuðullinn um óákveðinn tíma.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source><bpt id="p1">**</bpt>Active<ept id="p1">**</ept> – Indicate whether the cost factor is active.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Virkur<ept id="p1">**</ept> – Segið til um hvort kostnaðarstuðull sé virkur.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>The DOM considers only active cost factors that are associated with the fulfillment profile.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">DOM tekur aðeins virka kostnaðarstuðla til greina sem tengjast uppfyllingarsniði.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source><bpt id="p1">**</bpt>Fulfillment group<ept id="p1">**</ept> – Specify the group of locations that the non-shipping cost is defined for.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">**</bpt>Uppfyllingarflokkur<ept id="p1">**</ept> – Tilgreinið flokk staðsetninga sem kostnaður án sendingar er skilgreindur fyrir.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source><bpt id="p1">**</bpt>Fulfillment location<ept id="p1">**</ept> – Specify the location that the non-shipping cost is defined for.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">**</bpt>Uppfyllingarflokkur<ept id="p1">**</ept> – Tilgreinið staðsetningu sem kostnaður án sendingar er skilgreindur fyrir.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>You can't specify a fulfillment group and a fulfillment location on the same line for location-based calculation criteria.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Ekki er hægt að tilgreina uppfyllingarflokk og uppfyllingarstaðsetningu í sömu línunni fyrir útreikningsskilyrði sem byggir á staðsetningu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source><bpt id="p1">**</bpt>Cost<ept id="p1">**</ept> – Specify the cost value for a non-shipping cost at the fulfillment group level or fulfillment location level.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">**</bpt>Kostnaður<ept id="p1">**</ept> – Tilgreinið kostnaðarvirði fyrir kostnað án sendingar á stigi uppfyllingarflokks eða uppfyllingarstaðsetningar.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>For DOM to consider these costs when it's run, you must add the cost factor to the relevant fulfillment profile.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Til að DOM taki þennan kostnað til greina þegar hann er keyrður þarf að bæta kostnaðarstuðli við viðeigandi uppfyllingarsnið.</target>
        </trans-unit>
      </group>
    </body>
  </file>
</xliff>