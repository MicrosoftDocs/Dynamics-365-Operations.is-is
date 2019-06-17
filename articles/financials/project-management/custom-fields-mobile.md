<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="custom-fields-mobile.md" target-language="is-is">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-d915bc8" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>custom-fields-mobile.2a9e5e.4343c875da05641c57b7784bf52f1c814dd26d20.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>4343c875da05641c57b7784bf52f1c814dd26d20</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>19859d8566a8c7840066b2c10c6b08b67f1b83f4</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>06/04/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\financials\project-management\custom-fields-mobile.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Implement custom fields for the Microsoft Dynamics 365 Project Timesheet mobile app on iOS and Android</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Innleiða sérstillta reiti fyrir Microsoft Dynamics 365 Project Timesheet-farsímaforritið í iOS og Android</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic provides common patterns for using extensions to implement custom fields.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Þetta efnisatriði býður upp á algeng mynstur til að nota viðbætur til að innleiða sérstillta reiti.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Implement custom fields for the Microsoft Dynamics 365 Project Timesheet mobile app on iOS and Android</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">Innleiða sérstillta reiti fyrir Microsoft Dynamics 365 Project Timesheet-farsímaforritið í iOS og Android</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic provides common patterns for using extensions to implement custom fields.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">Þetta efnisatriði býður upp á algeng mynstur til að nota viðbætur til að innleiða sérstillta reiti.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>The following topics are covered:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Fjallað er um eftirfarandi efnisatriði:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>The various data types that the custom field framework supports</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hinar ýmsu gagnagerðir sem rammi sérstillts reits styður</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>How to show read-only or editable fields on timesheet entries, and save user-provided values back to the database</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvernig á að sýna skrifvarða eða breytanlega reiti í færslum vinnukorts og vista gildi sem notandi hefur bætt við í gagnagrunninn</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>How to show read-only fields on the timesheet header</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvernig á að sýna skrifvarða reiti í haus vinnukortsins</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>How to integrate other custom business logic to enter default values in fields and do additional validation</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hvernig á að samþætta annan sérstilltan viðskiptagrunn til að færa inn sjálfgildi í reitina og gera frekari villuleit</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Audience</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Notendahópur</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>This topic is intended for developers who are integrating their custom fields into the Microsoft Dynamics 365 Project Timesheet mobile application that is available for Apple iOS and Google Android.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Þetta efnisatriði er ætlað þróunaraðilum sem eru að samþætta sérstillta reiti sína við Microsoft Dynamics 365 Project Timesheet-farsímaforritið sem er í boði fyrir Apple iOS og Google Android.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>The assumption is that readers are familiar with X++ development and project timesheet functionality.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Gert er ráð fyrir að lesendur séu kunnugir X++ þróun og virkni vinnukorts fyrir verk.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Data contract – TSTimesheetCustomField X++ class</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Gagnasamningur - TSTimesheetCustomField X++ klasi</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>The <bpt id="p1">**</bpt>TSTimesheetCustomField<ept id="p1">**</ept> class is the X++ data contract class that represents information about a custom field for timesheet functionality.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Klasinn <bpt id="p1">**</bpt>TSTimesheetCustomField<ept id="p1">**</ept> er X++ gagnasamningsklasinn sem veitir upplýsingar um sérstilltan reit fyrir virkni vinnukorts.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Lists of the custom field objects are passed on both the TSTimesheetDetails data contract and the TSTimesheetEntry data contract to show custom fields in the mobile app.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Listar yfir hluti sérstillts reits eru bæði fluttir yfir í TSTimesheetDetails gagnasamning og TSTimesheetEntry gagnasamning til að sýna sérstillta reiti í farsímaforritinu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source><bpt id="p1">**</bpt>TSTimesheetDetails<ept id="p1">**</ept> - The timesheet header contract.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>TSTimesheetDetails<ept id="p1">**</ept> Síðuhaus vinnukortasamnings.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source><bpt id="p1">**</bpt>TSTimesheetEntry<ept id="p1">**</ept> - The timesheet transaction contract.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>TSTimesheetEntry<ept id="p1">**</ept> - Færsla vinnukortasamnings.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Groups of these objects that have the same project information and <bpt id="p1">**</bpt>timesheetLineRecId<ept id="p1">**</ept> value constitute a line.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Flokkar þessara hluta sem eru með sömu verkupplýsingarnar og gildið <bpt id="p1">**</bpt>timesheetLineRecId<ept id="p1">**</ept> gera línu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>fieldBaseType (Types)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">fieldBaseType (gerðir)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>The <bpt id="p1">**</bpt>FieldBaseType<ept id="p1">**</ept> property on the <bpt id="p2">**</bpt>TsTimesheetCustom<ept id="p2">**</ept> object determines the type of the field that appears in the app.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Eiginleikinn <bpt id="p1">**</bpt>FieldBaseType<ept id="p1">**</ept> í hlutnum <bpt id="p2">**</bpt>TsTimesheetCustom<ept id="p2">**</ept> ákvarðar gerð reitsins sem birtist í forritinu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>The following <bpt id="p1">**</bpt>Types<ept id="p1">**</ept> values that are supported.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Eftirfarandi gildin fyrir <bpt id="p1">**</bpt>Gerðir<ept id="p1">**</ept> sem eru studdar.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Types value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Gildi gerða</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Type</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Gerð</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Notes</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Athugasemdir</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>0</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">0</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>String (and Enum)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Strengur (og fasttexti)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>The field appears as a text field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Reitinn birtist sem textareitur.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>1</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">1</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Integer</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Heiltala</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>The value is shown as a number without decimal places.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Gildi er sýnt sem tala án aukastafa.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>2</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">2</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Real</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Rauntala</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>The value is shown as a number that has decimal places.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Gildi er sýnt sem tala með aukastafi.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>To show the real value as a currency in the app, use the <bpt id="p1">**</bpt>fieldExtenededType<ept id="p1">**</ept> property.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Til að sýna raunverulegt gildi sem gjaldmiðil í forritinu skal nota eiginleikann <bpt id="p1">**</bpt>fieldExtenededType<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>You can use the <bpt id="p1">**</bpt>numberOfDecimals<ept id="p1">**</ept> property to set the number of decimal places that are shown.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hægt er að nota eiginleikann <bpt id="p1">**</bpt>numberOfDecimals<ept id="p1">**</ept> til að stilla fjölda aukastafa sem á að sýna.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>3</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">3</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Date</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Dagsetning</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Date formats are determined by the user's <bpt id="p1">**</bpt>Date, times, and number format<ept id="p1">**</ept> setting that is specified under <bpt id="p2">**</bpt>Language and country/region preference<ept id="p2">**</ept> in <bpt id="p3">**</bpt>User options<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dagsetningarsnið eru ákvörðuð af stillingunum <bpt id="p1">**</bpt>Dagsetningar-, tíma- og númerasnið<ept id="p1">**</ept> sem notandi velur og eru tilgreind undir <bpt id="p2">**</bpt>Kjörstilling fyrir tungumál og land/svæði<ept id="p2">**</ept> í <bpt id="p3">**</bpt>Valkostir notanda<ept id="p3">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>4</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">4</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Boolean</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Boole</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>15</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">15</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>GUID</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">GUID</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>16</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">16</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Int64</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Int64</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>If the <bpt id="p1">**</bpt>stringOptions<ept id="p1">**</ept> property isn't provided on the <bpt id="p2">**</bpt>TSTimesheetCustomField<ept id="p2">**</ept> object, a free-text field is provided to the user.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ef eiginleikinn <bpt id="p1">**</bpt>stringOptions<ept id="p1">**</ept> er ekki gefinn upp í hlutnum <bpt id="p2">**</bpt>TSTimesheetCustomField<ept id="p2">**</ept> er notandanum útvegaður reitur með frjálsum texta.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>The <bpt id="p1">**</bpt>stringLength<ept id="p1">**</ept> property can be used to set the maximum string length that users can enter.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hægt er að nota eiginleikann <bpt id="p1">**</bpt>stringLength<ept id="p1">**</ept> til að stilla hámarkslengd á streng sem notendur geta fært inn.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>If the <bpt id="p1">**</bpt>stringOptions<ept id="p1">**</ept> property is provided on the <bpt id="p2">**</bpt>TSTimesheetCustomField<ept id="p2">**</ept> object, those list elements are the only values that users can select by using option buttons (radio buttons).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ef boðið er upp á eiginleikann <bpt id="p1">**</bpt>stringOptions<ept id="p1">**</ept> í hlutnum <bpt id="p2">**</bpt>TSTimesheetCustomField<ept id="p2">**</ept> eru þessar listaeiningar einu gildin sem notendur geta valið með því að nota valhnappa (valhringi).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>In this case, the string field can act as an enum value for the purpose of user entry.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Í þessu tilviki getur strengjareiturinn virkað sem fasttextagildi gagngert fyrir færslu notanda.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>To save the value to the database as an enum, manually map the string value back to the enum value before you save to the database by using chain of command (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Til að vista gildið í gagnagrunninum sem fasttexta skal varpa strengjagildinu handvirkt aftur í fasttextagildið áður en vistað er í gagnagrunninn með því að nota boðleið (sjá kaflann „Nota boðleið í TSTimesheetEntryService-klasanum til að vista vinnukortafærslu úr forritinu aftur í gagnagrunninn“ seinna í þessu efnisatriði til að sjá dæmi).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>fieldExtendedType (TSCustomFieldExtendedType)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">fieldExtendedType (TSCustomFieldExtendedType)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>You can use this property to format real values as currency.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hægt er að nota þennan eiginleika til að sníða raunveruleg gildi sem gjaldmiðil.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>This approach is applicable only when the <bpt id="p1">**</bpt>fieldBaseType<ept id="p1">**</ept> value is <bpt id="p2">**</bpt>Real<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Þessi nálgun á eingöngu við þegar gildið <bpt id="p1">**</bpt>fieldBaseType<ept id="p1">**</ept> er <bpt id="p2">**</bpt>Raunverulegt<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source><bpt id="p1">**</bpt>TSCustomFieldExtendedType:None<ept id="p1">**</ept> – No formatting is applied.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>TSCustomFieldExtendedType:None<ept id="p1">**</ept> - Ekkert snið er notað.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source><bpt id="p1">**</bpt>TSCustomFieldExtendedType::Currency<ept id="p1">**</ept> – Format the value as currency.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>TSCustomFieldExtendedType::Gjaldmiðill<ept id="p1">**</ept> - Sníða gildið sem gjaldmiðil.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>When currency formatting is active, the <bpt id="p1">**</bpt>stringValue<ept id="p1">**</ept> field can be used pass the currency code that should be shown in the app.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Þegar snið gjaldmiðils er virkt er hægt að nota reitinnn <bpt id="p1">**</bpt>stringValue<ept id="p1">**</ept> til að flytja gjaldmiðilskóðann áfram sem á að birtast í forritinu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>The value is a read-only value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Gildið er skrifvarið gildi.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>The <bpt id="p1">**</bpt>realValue<ept id="p1">**</ept> field contains the money amount that should be saved to the database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Reiturinn <bpt id="p1">**</bpt>realValue<ept id="p1">**</ept> inniheldur peningaupphæðina sem á að vista í gagnagrunninn.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>fieldSection (TSCustomFieldSection)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">fieldSection (TSCustomFieldSection)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>You can use this property specify where the custom field should appear in the app.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hægt er að nota þennan eiginleika til að tilgreina hvar sérstillti reiturinn á að birtast í forritinu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source><bpt id="p1">**</bpt>TSCustomFieldSection::Header<ept id="p1">**</ept> – The field will appear in the <bpt id="p2">**</bpt>View more details<ept id="p2">**</ept> section in the app.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>TSCustomFieldSection::Haus<ept id="p1">**</ept> - Reiturinn birtist í hlutanum <bpt id="p2">**</bpt>Skoða frekari upplýsingar<ept id="p2">**</ept> í forritinu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>These fields are always read-only.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Þessir reitir eru alltaf skrifvarðir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source><bpt id="p1">**</bpt>TSCustomFieldSection::Line<ept id="p1">**</ept> – The field will appear after all the out-of-box line fields on timesheet entries.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>TSCustomFieldSection::Lína<ept id="p1">**</ept> - Reiturinn birtist á eftir öllum tilbúnum reitarlínum í vinnukortafærslum.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>These fields can be either editable or read-only.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Þessir reitir geta verið annaðhvort breytilegir eða skrifvarðir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>fieldName (FieldNameShort)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">fieldName (FieldNameShort)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>This property identifies the field when values that the app provides are saved back to the database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Þessi eiginleiki ber kennsl á reitinn þegar gildi sem forritið veitir eru vistuð aftur í gagnagrunninn.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>tableName (TableNameShort)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">tableName (TableNameShort)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>This property identifies the field when values that the app provides are saved back to the database.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">Þessi eiginleiki ber kennsl á reitinn þegar gildi sem forritið veitir eru vistuð aftur í gagnagrunninn.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>isEditable (NoYes)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">isEditable (NoYes)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>Set this property to <bpt id="p1">**</bpt>Yes<ept id="p1">**</ept> to specify that the field in the timesheet entry section should be editable by users.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Stillið þennan eiginleika á <bpt id="p1">**</bpt>Já<ept id="p1">**</ept> til að tilgreina að reiturinn í hlutanum fyrir vinnukortafærslur eigi að vera breytanlegur fyrir notanda.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>Set the property to <bpt id="p1">**</bpt>No<ept id="p1">**</ept> to make the field read-only.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Stillið eiginleikann á <bpt id="p1">**</bpt>Nei<ept id="p1">**</ept> til að gera reitinn skrifvarinn.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>isMandatory (NoYes)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">isMandatory (NoYes)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>Set this property to <bpt id="p1">**</bpt>Yes<ept id="p1">**</ept> to specify that the field in the timesheet entry section should be mandatory.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Stillið þennan eiginleika á <bpt id="p1">**</bpt>Já<ept id="p1">**</ept> til að tilgreina að reiturinn í hlutanum fyrir vinnukortafærslur eigi að vera áskilinn.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>label (str)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">merki (str)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>This property specifies the label that is shown next the field in the app.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Þessi eiginleiki tilgreinir merkið sem er sýnt við hliðina á reitnum í forritinu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>stringOptions (List of Strings)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">stringOptions (listi yfir strengi)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>This property is applicable only when <bpt id="p1">**</bpt>fieldBaseType<ept id="p1">**</ept> is set to <bpt id="p2">**</bpt>String<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Þessi eiginleiki er eingöngu tiltækur þegar <bpt id="p1">**</bpt>fieldBaseType<ept id="p1">**</ept> er stillt á <bpt id="p2">**</bpt>Strengur<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>If <bpt id="p1">**</bpt>stringOptions<ept id="p1">**</ept> is set, the string values that are available for selection via option buttons (radio buttons) are specified by the strings in the list.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ef <bpt id="p1">**</bpt>stringOptions<ept id="p1">**</ept> er stillt eru strengjagildin sem hægt er að velja í gegnum valhnappa (valhringi) tilgreind af strengjunum í listanum.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>If no strings are provided, free-text entry in the string field is allowed (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ef engar strengir eru gefnir upp er innsláttur á frjálsum texta í strengjareitnum leyfður (sjá hlutann „Nota boðleið í TSTimesheetEntryService-klasanum til að vista vinnukortafærslur úr forritinu aftur í gagnagrunninn“ seinna í þessu efnisatriði til að sjá dæmi).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>stringLength (int)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">stringLength (int)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>This property specifies the maximum length for a string field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Þessi eiginleiki tilgreinir hámarkslengd fyrir strengjareit.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>It's applicable only when <bpt id="p1">**</bpt>fieldBaseType<ept id="p1">**</ept> is set to <bpt id="p2">**</bpt>String<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hann er eingöngu tiltækur þegar <bpt id="p1">**</bpt>fieldBaseType<ept id="p1">**</ept> er stillt á <bpt id="p2">**</bpt>Strengur<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>numberOfDecimals (int)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">numberOfDecimals (int)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>This property specifies the number of decimal places that are shown for a real field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Þessi eiginleiki tilgreinir fjölda aukastafa sem eru sýndir í raunverulegum reit.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>It's applicable only when <bpt id="p1">**</bpt>fieldBaseType<ept id="p1">**</ept> is set to <bpt id="p2">**</bpt>Real<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hann er eingöngu tiltækur þegar <bpt id="p1">**</bpt>fieldBaseType<ept id="p1">**</ept> er stillt á <bpt id="p2">**</bpt>Raunverulegur<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>orderSequence (int)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">orderSequence (int)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>This property controls the order in which the custom fields are shown in the app when more than one custom field is specified.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Þessi eiginleiki stýrir röðinni á sérstilltu reitunum þegar þeir birtast í forritinu þegar fleiri en einn sérstilltur reitur er tilgreindur.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>Fields that have lower numbers are shown first.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Reitir með lægri tölu eru sýndir fyrst.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>booleanValue (boolean)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">booleanValue (boole-gildi)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>For fields of the <bpt id="p1">**</bpt>Boolean<ept id="p1">**</ept> type, this property passes the Boolean value of the field between the server and the app.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Fyrir reiti af gerðinni <bpt id="p1">**</bpt>Boole-gildi<ept id="p1">**</ept> færir þessi eiginleiki boole-gildi reitsins á milli þjónsins og forritsins.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>guidValue (guid)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">guidValue (guid)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>For fields of the <bpt id="p1">**</bpt>GUID<ept id="p1">**</ept> type, this property passes the globally unique identifier (GUID) value of the field between the server and the app.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Fyrir reiti af gerðinni <bpt id="p1">**</bpt>GUID<ept id="p1">**</ept> færir þessi eiginleiki gildi fyrir reit alþjóðlegs einkvæms kennimerkis (GUID) á milli þjónsins og forritsins.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>int64Value (int64)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">int64Value (int64)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>For fields of the <bpt id="p1">**</bpt>Int64<ept id="p1">**</ept> type, this property passes the int64 value of the field between the server and the app.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Fyrir reiti af gerðinni <bpt id="p1">**</bpt>Int64<ept id="p1">**</ept> færir þessi eiginleiki int64-gildi reitsins á milli þjónsins og forritsins.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>intValue (int)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">intValue (int)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>For fields of the <bpt id="p1">**</bpt>Int<ept id="p1">**</ept> type, this property passes the int value of the field between the server and the app.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Fyrir reiti af gerðinni <bpt id="p1">**</bpt>Int<ept id="p1">**</ept> færir þessi eiginleiki int-gildi reitsins á milli þjónsins og forritsins.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>realValue (real)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">realValue (raunverulegt)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>For fields of the <bpt id="p1">**</bpt>Real<ept id="p1">**</ept> type, this property passes the real value of the field between the server and the app .</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Fyrir reiti af gerðinni <bpt id="p1">**</bpt>Raunverulegt<ept id="p1">**</ept> færir þessi eiginleiki raunverulegt gildi reitsins á milli þjónsins og forritsins.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>stringValue (str)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">stringValue (str)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>For fields of the <bpt id="p1">**</bpt>String<ept id="p1">**</ept> type, this property passes the string value of the field between the server and the app.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Fyrir reiti af gerðinni <bpt id="p1">**</bpt>Strengur<ept id="p1">**</ept> færir þessi eiginleiki strengjagildi reitsins á milli þjónsins og forritsins.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>It's also used for fields of the <bpt id="p1">**</bpt>Real<ept id="p1">**</ept> type that are formatted as currency.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hann er einnig notaður fyrir reiti af gerðinni <bpt id="p1">**</bpt>Raunverulegur<ept id="p1">**</ept> sem eru sniðnir sem gjaldmiðill.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>For those fields, the property is used to pass the currency code to the app.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Fyrir þessa reiti er eiginleikinn notaður til að flytja gjaldmiðilskóða áfram í forritið.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>dateValue (date)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">dateValue (dagsetning)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>For fields of the <bpt id="p1">**</bpt>Date<ept id="p1">**</ept> type, this property passes the date value of the field between the server and the app.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Fyrir reiti af gerðinni <bpt id="p1">**</bpt>Dagsetning<ept id="p1">**</ept> færir þessi eiginleiki dagsetningargildi reitsins á milli þjónsins og forritsins.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>Show and save a custom field in the timesheet entry section</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Sýnið og vistið sérstilltan reit í hlutanum fyrir vinnukortafærslu</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>Below is a screenshot from the mobile app of a timesheet entry creation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hér fyrir neðan er skjámynd úr farsímaforritinu af stofnun vinnukortafærslu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>It shows the out-of-box fields and a custom field in the "Time entry" section called "Test string" with an enum value of "Second option" already set.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hún sýnir tilbúnu reitina og sérstilltan reit í hlutanum „Tímafærsla“ sem kallast „Prófunarstrengur“ með fasttextagildi sem „Annar valkostur“ nú þegar stilltan.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>Test string custom field in the app</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Sérstilltur reitur prófunarstrengs í forritinu</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>Below is a screenshot from the mobile app of the user selecting one of the enum options available for the "Test string" custom field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hér að neðan er skjámynd úr farsímaforriti notandans sem velur einn af valmöguleikum fasttexta sem eru í boði fyrir sérstillta reitinn „Prófunarstrengur“.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>The two options are "First option" and "Second option" shown as radio buttons.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Valkostirnir tveir eru „Fyrsti valkostur“ og „Annar valkostur“ sýndir sem valhringir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>The second option is currently selected.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Annar valkosturinn er valinn.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>Option buttons (radio buttons) for the Test string custom field</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Valhnappar (valhringir) fyrir sérstilltan reit prófunarstrengs</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>Extend the TSTimesheetLine table so that it has a custom field</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Stækka TSTimesheetLine-töfluna svo hún sé með sérstilltan reit</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>In typical scenarios, it's likely that the data for a custom field in the timesheet entry section will be saved to the TSTimesheetLine table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Í dæmigerðum tilfellum er líklegt að gögnin fyrir sérsniðin reit í hlutanum fyrir vinnukortafærslu verði vistuð í TSTimesheetLine-töflunni.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>However, other tables can be used if the data can be retrieved based on a TSTimesheetTrans record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hinsvegar er hægt að nota aðrar töflur ef hægt er að sækja gögnin á grunni TSTimesheetTrans-færslu sem er gefin upp, eða ef hún er ekki með tiltekið færslusamhengi (t.d. ef reiturinn er stilltur sem skrifvarinn í færibreytum verksins).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>Note that custom fields don't have to have any backing database records.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Athugið að sérstilltu reitirnir eru ekki með nein öryggisafrit af færslum gagnagrunns.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>They can be dynamically generated based on X++ logic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hægt er að mynda þá gagnvirkt á grunni X++ rökfræði.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>This approach can be useful in read-only scenarios (see the “Use chain of command on the TSTimesheetDetails class, buildCustomFieldListForHeader method to fill in timesheet details” section for an example of dynamically generated custom field values.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Þessi nálgun getur reynst gagnleg í skrifvörðum aðstæðum (sjá hlutann „Nota boðleið í TSTimesheetDetails-klasanum, buildCustomFieldListForHeader-aðferðina til að fylla út í upplýsingar vinnukorts“ til að sjá dæmi um gagnvirka myndun á gildum sérstillts reits.)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>Below is a screenshot from Visual Studio of the Application Object Tree.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hér að neðan er skjámynd úr Visual Studio af hugbúnaðarhlutatrénu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>It shows an extension of the TSTimesheetLine table with the TestLineString field added as a custom field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hún sýnir viðbót af TSTimesheetLine-töflunni með TestLineString-töflunni bættri við sem sérstilltur reitur.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>Line string</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Strengjalína</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the timesheet entry section</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Notið boðleið í buildCustomFieldList-aðferðinni fyrir TSTimesheetSettings-klasann til að sýna reit í hluta vinnukortafærslunnar</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>This code controls the display settings for the field in the app.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Þessi kóði stýrir skjástillingum fyrir reitinn í forritinu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hann stýrir t.d. gerð reitsins, merkinu, hvort reiturinn sé áskilinn, og í hvaða hluta reiturinn birtist.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>The following example shows a string field on time entries.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Eftirfarandi dæmi sýnir strengjareit í tímafærslum.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>This field has two options, <bpt id="p1">**</bpt>First option<ept id="p1">**</ept> and <bpt id="p2">**</bpt>Second option<ept id="p2">**</ept>, that are available via option buttons (radio buttons).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Þessi reitur hefur tvo valmöguleika, <bpt id="p1">**</bpt>Fyrsti valkostur<ept id="p1">**</ept> og <bpt id="p2">**</bpt>Annar valkostur<ept id="p2">**</ept>, sem eru í boði í gegnum valhnappa (valhringi).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>The field in the app is associated with the <bpt id="p1">**</bpt>TestLineString<ept id="p1">**</ept> field that is added to the TSTimesheetLine table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Reiturinn í forritinu tengist reitnum <bpt id="p1">**</bpt>TestLineString<ept id="p1">**</ept> sem er bætt við TSTimesheetLine-töfluna.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>Note the use of the <bpt id="p1">**</bpt>TSTimesheetCustomField::newFromMetatdata()<ept id="p1">**</ept> method to simplify the initialization of the custom field properties: <bpt id="p2">**</bpt>fieldBaseType<ept id="p2">**</ept>, <bpt id="p3">**</bpt>tableName<ept id="p3">**</ept>, <bpt id="p4">**</bpt>fieldname<ept id="p4">**</ept>, <bpt id="p5">**</bpt>label<ept id="p5">**</ept>, <bpt id="p6">**</bpt>isEditable<ept id="p6">**</ept>, <bpt id="p7">**</bpt>isMandatory<ept id="p7">**</ept>, <bpt id="p8">**</bpt>stringLength<ept id="p8">**</ept>, and <bpt id="p9">**</bpt>numberOfDecimals<ept id="p9">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Athugið notkun á aðferðinni <bpt id="p1">**</bpt>TSTimesheetCustomField::newFromMetadata()<ept id="p1">**</ept> til að einfalda frumstillingu á eiginleikum sérstillts reits: <bpt id="p2">**</bpt>fieldBaseType<ept id="p2">**</ept>, <bpt id="p3">**</bpt>tableName<ept id="p3">**</ept>, <bpt id="p4">**</bpt>fieldname<ept id="p4">**</ept>, <bpt id="p5">**</bpt>label<ept id="p5">**</ept>, <bpt id="p6">**</bpt>isEditable<ept id="p6">**</ept>, <bpt id="p7">**</bpt>isMandatory<ept id="p7">**</ept>, <bpt id="p8">**</bpt>stringLength<ept id="p8">**</ept> og <bpt id="p9">**</bpt>numberOfDecimals<ept id="p9">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>You can also set these parameters manually, as you prefer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Einnig er hægt að stilla þessar færibreytur handvirkt eins og hentar.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>Use chain of command on the buildCustomFieldListForEntry method of the TSTimesheetEntry class to enter values in a timesheet entry</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Nota boðleið í buildCustomFieldListForEntry-aðferðinni fyrir TSTimesheetEntry-klasann til að færa gildi inn í tímafærslu</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>The <bpt id="p1">**</bpt>buildCustomFieldListForEntry<ept id="p1">**</ept> method is used to enter values on the saved timesheet lines in the mobile app.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Aðferðin <bpt id="p1">**</bpt>buildCustomFieldListForEntry<ept id="p1">**</ept> er notuð til að færa gildi í vistuðu vinnukortslínunum inn í farsímaforritið.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>It takes a TSTimesheetTrans record as a parameter.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hún tekur TSTimesheetTrans-færslu sem færibreytu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>Fields from that record can be used to fill in the custom field value in the app.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Reiti úr þeirri færslu er hægt að nota til að setja inn gildið fyrir sérstilltan reit í forritinu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Nota boðleið í TSTimesheetEntryService-klasanum til að vista vinnukortafærslur úr forritinu aftur í gagnagrunninn</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>To save a custom field back to the database in typical usage, you must extend multiple methods:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Til að vista sérstilltan reit aftur í gagnagrunninn við dæmigerða notkun, þarf að víkka út margar aðferðir:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>The <bpt id="p1">**</bpt>timesheetLineNeedsUpdating<ept id="p1">**</ept> method is used to determine whether the line record has been changed by the user in the app and must be saved to the database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Aðferðin <bpt id="p1">**</bpt>timesheetLineNeedsUpdating<ept id="p1">**</ept> er notuð til að ákvarða hvort notandinn hafi breytt línufærslunni í forritinu og verði að vista hana í gagnagrunninum.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>If performance isn't a concern, this method can be simplified so that it always returns <bpt id="p1">**</bpt>true<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ef afköst eru ekki áhyggjuefni er hægt að einfalda þessa aðferð svo hún skili alltaf <bpt id="p1">**</bpt>satt<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>The <bpt id="p1">**</bpt>populateTimesheetLineFromEntryDuringCreate<ept id="p1">**</ept> and <bpt id="p2">**</bpt>populateTimesheetLineFromEntryDuringUpdate<ept id="p2">**</ept> methods can be extended so that they enter values in the TSTimesheetLine database record from the TSTimesheetEntry data contract record that is provided.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Aðferðirnar <bpt id="p1">**</bpt>populateTimesheetLineFromEntryDuringCreate<ept id="p1">**</ept> og <bpt id="p2">**</bpt>populateTimesheetLineFromEntryDuringUpdate<ept id="p2">**</ept> er hægt að stækka svo þær færi gildi inn í færslu gagnagrunns TSTimesheetLine úr færslu TSTimesheetEntry-gagnasamnings sem gefin er upp.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>In the example that follows, notice how the mapping between the database field and the entry field is manually done via X++ code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Takið eftir í eftirfarandi dæmi hvernig vörpun milli gagnagrunnsreits og færslureits er gerð handvirkt með X++ kóða.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>The <bpt id="p1">**</bpt>populateTimesheetWeekFromEntry<ept id="p1">**</ept> method can also be extended if the custom field that is mapped to the <bpt id="p2">**</bpt>TSTimesheetEntry<ept id="p2">**</ept> object must write back to the TSTimesheetLineweek database table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Einnig er hægt að stækka aðferðina <bpt id="p1">**</bpt>populateTimesheetWeekFromEntry<ept id="p1">**</ept> ef sérstilltur reitur sem er varpað í hlutinn <bpt id="p2">**</bpt>TSTimesheetEntry<ept id="p2">**</ept> verður að skrifa til baka til gagnagrunnstöflunnar TSTimesheetLineweek.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>The following example saves the <bpt id="p1">**</bpt>firstOption<ept id="p1">**</ept> or <bpt id="p2">**</bpt>secondOption<ept id="p2">**</ept> value that the user selects to the database as a raw string value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Eftirfarandi dæmi vistar gildið <bpt id="p1">**</bpt>firstOption<ept id="p1">**</ept> eða <bpt id="p2">**</bpt>secondOption<ept id="p2">**</ept> sem notandinn velur í gagnagrunninn sem óunnið strengjagildi.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>If the database field is a field of the <bpt id="p1">**</bpt>Enum<ept id="p1">**</ept> type, those values can be manually mapped to an enum value and then saved to an enum field on the database table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ef gagnagrunnsreiturinn er reitur af gerðinni <bpt id="p1">**</bpt>Fasttexti<ept id="p1">**</ept> er hægt að varpa þessum gildum handvirkt í fasttextagildi og síðan vista þau í fasttextareit í gagnagrunnstöflunni.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>Show a custom field in the timesheet header section</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Sýna sérstilltan reit í hluta vinnukortahauss</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>Below is a screenshot from the mobile app of a user viewing a timesheet.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hér fyrir neðan er skjámynd úr farsímaforritinu af notanda að skoða vinnukort.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>The "More information" button has been selected in the upper-right corner to show the "View more details" option.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hnappurinn „Frekari upplýsingar“ hefur verið valinn efst í hægra horninu til að sýna valkostinn „Skoða frekari upplýsingar“.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>View more details command</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Skipun fyrir að skoða frekari upplýsingar</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>Below is a screenshot from the mobile app showing the “More” section of a timesheet.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hér fyrir neðan er skjámynd úr farsímaforritinu sem sýnir „Meira“ hlutann í vinnukorti.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>A custom field called “Utilization rate of this timesheet (computed custom field)” has been added to the timesheet header section.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Sérstilltur reitur sem kallast „Nýtingarhlutfall á þessu vinnukorti (reiknaður sérstilltur reitur)“ hefur verið bætt við í haus vinnukortsins.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>A read-only value of "0.667" is set on the custom field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Skrifvarið gildi upp á „0,667“ er stillt fyrir sérstillta reitinn.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>More section</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Meira</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>Extend the TSTimesheetTable table so that it has a custom field</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Stækka TSTimesheetTable-töfluna svo hún sé með sérstilltan reit</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>In typical scenarios, it's likely that the data for a custom field in the header section will be pulled from the TSTimesheetHeader table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Í dæmigerðum tilfellum er líklegt að gögnin fyrir sérsniðinn reit í hausnum verði sótt úr TSTimesheetHeader-töflunni.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>However, other tables can be used if the data can be retrieved based on a TSTimesheetTable record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hinsvegar er hægt að nota aðrar töflur ef hægt er að sækja gögnin á grunni TSTimesheetTable-færslu sem er gefin upp, eða ef hún er ekki með tiltekið færslusamhengi (t.d. ef reiturinn er stilltur sem skrifvarinn í færibreytum verksins).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>Note that custom fields don't have to have any backing database records.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">Athugið að sérstilltu reitirnir eru ekki með nein öryggisafrit af færslum gagnagrunns.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>They can be dynamically generated based on X++ logic.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">Hægt er að mynda þá gagnvirkt á grunni X++ rökfræði.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>The example that follows shows this approach.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dæmið sem fylgir sýnir þessa nálgun.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source>Fields in the header section are always read-only in the app.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Reitir í hausnum eru alltaf skrifvarðir í forritinu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the header section</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Nota boðleið í buildCustomFieldList-aðferðinni fyrir TSTimesheetSettings-klasann til að sýna reit í hausnum</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source>This code controls the display settings for the field in the app.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">Þessi kóði stýrir skjástillingum fyrir reitinn í forritinu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">Hann stýrir t.d. gerð reitsins, merkinu, hvort reiturinn sé áskilinn, og í hvaða hluta reiturinn birtist.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source>The following example shows a computed value in the header section in the app.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Eftirfarandi dæmi sýnir reiknað gildi í hausnum í forritinu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source>Use chain of command on the buildCustomFieldListForHeader method of the TSTimesheetDetails class to fill in timesheet details</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Nota boðleið fyrir aðferðina buildCustomFieldListForHeader í TSTimesheetDetails-klasanum til að fylla út upplýsingar um vinnukort</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>The <bpt id="p1">**</bpt>buildCustomFieldListForHeader<ept id="p1">**</ept> method is used to fill in the timesheet header details in the mobile app.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Aðferðin <bpt id="p1">**</bpt>buildCustomFieldListForHeader<ept id="p1">**</ept> er notuð til að fylla út upplýsingar vinnukortahauss í farsímaforritinu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>It takes a TSTimesheetTable record as a parameter.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hún notar TSTimesheetTable-færslu sem færibreytu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>Fields from that record can be used to fill in the custom field value in the app.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">Reiti úr þeirri færslu er hægt að nota til að setja inn gildið fyrir sérstilltan reit í forritinu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source>The following example doesn't read any values from the database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Eftirfarandi dæmi les ekki nein gildi úr gagnagrunninum.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source>Instead, it uses X++ logic to generate a computed value that is then shown in the app.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Þess í stað notar það X++ reikniaðgerðir til að búa til reiknað gildi sem síðan er sýnt í forritinu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>Other configurability/extensibility opportunities</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Aðrir möguleikar á stillingum/stækkunarhæfni</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>Adding additional validation for the app</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bæta við frekari villuleit fyrir forritið</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source>Existing logic for timesheet functionality at the database level will still work as expected.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Núverandi reikniaðgerðir fyrir virkni vinnukorts á gagnagrunnsstigi virka enn eins og venjulega.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>To interrupt the completion of save or submit operations and show a specific error message, you can add <bpt id="p1">**</bpt>throw error("message to user")<ept id="p1">**</ept> to the code via a chain of command extension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Til að trufla málalyktir á aðgerðum vistunar og innsendingar og sýna tiltekin villuboð er hægt að bæta <bpt id="p1">**</bpt>sýna villu („skilaboð til notanda“)<ept id="p1">**</ept> við kóðann í gegnum viðbót boðleiðar.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>Here are three examples of useful extensible methods:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hér eru þrjú dæmi um gagnlegar aðferðir fyrir stækkanleika:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>If <bpt id="p1">**</bpt>validateWrite<ept id="p1">**</ept> on the TSTimesheetLine table returns <bpt id="p2">**</bpt>false<ept id="p2">**</ept> during a save operation for a timesheet line, an error message is shown in the mobile app.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ef <bpt id="p1">**</bpt>validateWrite<ept id="p1">**</ept> í TSTimesheetLine-töflunni skilar <bpt id="p2">**</bpt>rangt<ept id="p2">**</ept> við vistun á aðgerð fyrir vinnukortslínu birtast villuboð í farsímaforritinu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="273">
          <source>If <bpt id="p1">**</bpt>validateSubmit<ept id="p1">**</ept> on the TSTimesheetTable table returns <bpt id="p2">**</bpt>false<ept id="p2">**</ept> during timesheet submission in the app, an error message is shown to the user.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ef <bpt id="p1">**</bpt>validateSubmit<ept id="p1">**</ept> í TSTimesheetTable-töflunni skilar <bpt id="p2">**</bpt>rangt<ept id="p2">**</ept> við innsendingu á vinnukorti í forritinu fær notandinn villuboð.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="274">
          <source>Logic that fills in fields (for example, <bpt id="p1">**</bpt>Line Property<ept id="p1">**</ept>) during the <bpt id="p2">**</bpt>insert<ept id="p2">**</ept> method on the TSTimesheetLine table will still run.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Reikniaðgerð sem fyllir út reiti (t.d. <bpt id="p1">**</bpt>Línueiginleiki<ept id="p1">**</ept>) þegar aðferðin <bpt id="p2">**</bpt>setja inn<ept id="p2">**</ept> stendur yfir í TSTimesheetLine-töflunni mun halda áfram að keyra.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="275">
          <source>Hiding and marking out-of-box fields as read-only via configuration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Fela og merkja tilbúna reiti sem skrifvarða í gegnum grunnstillingu</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="276">
          <source>From the project parameters, you can make out-of-box fields read-only or hidden in the mobile app.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Úr færibreytum verka er hægt að gera tilbúna reiti skrifvarða eða fela þá í farsímaforritinu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="277">
          <source>Set the options in the <bpt id="p1">**</bpt>Mobile timesheets<ept id="p1">**</ept> section on the <bpt id="p2">**</bpt>Timesheet<ept id="p2">**</ept> tab of the <bpt id="p3">**</bpt>Project management and accounting parameters<ept id="p3">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Stillið valmöguleikana í hlutanum <bpt id="p1">**</bpt>Vinnukort farsíma<ept id="p1">**</ept> í flipanum <bpt id="p2">**</bpt>Vinnukort<ept id="p2">**</ept> á síðunni <bpt id="p3">**</bpt>Verkefnastjórnun og bókhaldsfæribreytur<ept id="p3">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="278">
          <source>Project parameters</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Færibreytur verka</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="279">
          <source>Changing the activities that are available for selection via extensions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Breyting á verkþáttum sem hægt er að velja í gegnum viðbætur</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="280">
          <source>The activities that are available for selection for a project are filled in via the <bpt id="p1">**</bpt>getActivitiesForProject()<ept id="p1">**</ept> and <bpt id="p2">**</bpt>getActivityQuery()<ept id="p2">**</ept> methods in the <bpt id="p3">**</bpt>TsTimesheetProjectService<ept id="p3">**</ept> class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Verkþættirnir sem hægt er að velja fyrir verk eru fylltir út í gegnum aðferðirnar <bpt id="p1">**</bpt>getActivitiesForProject()<ept id="p1">**</ept> og <bpt id="p2">**</bpt>getActivityQuery()<ept id="p2">**</ept> í klasanum <bpt id="p3">**</bpt>TsTimesheetProjectService<ept id="p3">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="281">
          <source>You can use chain of command to change this behavior to match your business scenario for the activities that are available for selection for a specific project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hægt er að nota boðleið til að breyta þessari hegðun til að passa við rekstraraðstæður þínar fyrir verkþættina sem hægt er að velja fyrir tiltekið verk.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="282">
          <source>Entering a default project category on timesheet entries</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Færa sjálfgefna verktegund inn í vinnukortafærslur</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="283">
          <source>Entry of a default project category on timesheet entries occurs at three levels.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Færsla á sjálfgefinni verktegund inn í vinnukortafærslur gerist á þremur stigum.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="284">
          <source>You can use chain of command to extend the behavior at any or all of these levels to achieve the desired behavior.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hægt er að nota boðleið til að víkka út hegðunina á hvaða stigi sem er eða þeim öllum til að ná fram æskilegri hegðun.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="285">
          <source>The following hierarchy is used:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Eftirfarandi stigveldi er notað:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="286">
          <source>The app tries to put the default category from the project resource.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Forritið reynir að setja inn sjálfgefna tegund úr tilföngum verks.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="287">
          <source>This default category is set in the <bpt id="p1">**</bpt>getCurrentUserResource<ept id="p1">**</ept> and <bpt id="p2">**</bpt>getDelegatedResourcesForCurrentUser<ept id="p2">**</ept> methods in the <bpt id="p3">**</bpt>TSTimesheetSettingsService<ept id="p3">**</ept> class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Þessi sjálfgefna tegund er stillt í aðferðunum <bpt id="p1">**</bpt>getCurrentUserResource<ept id="p1">**</ept> and <bpt id="p2">**</bpt>getDelegatedResourcesForCurrentUser<ept id="p2">**</ept> í klasanum <bpt id="p3">**</bpt>TSTimesheetSettingsService<ept id="p3">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="288">
          <source>If the default category isn't provided at the project resource level, the app tries to pull it from the project activity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ef ekki er boðið upp á sjálfgefna tegund á stigi verktilfanga reynir forritið að sækja það úr verkþættinum.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="289">
          <source>This default category is set in the <bpt id="p1">**</bpt>getActivitiesForProject<ept id="p1">**</ept> method in the <bpt id="p2">**</bpt>TSTimesheetProjectService<ept id="p2">**</ept> class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Þessi sjálfgefna tegund er stillt í aðferðinni <bpt id="p1">**</bpt>getActivitiesForProject<ept id="p1">**</ept> í klasanum <bpt id="p2">**</bpt>TSTimesheetProjectService<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="290">
          <source>If the default category isn't provided at the project activity level, the default category it taken from the project parameters.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ef ekki er boðið upp á sjálfgefna tegund á stigi verkþáttar er náð í sjálfgefnu tegundina úr færibreytum verks.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="291">
          <source>This default category is set in the <bpt id="p1">**</bpt>getProjectDetailsbyRule<ept id="p1">**</ept> method in the <bpt id="p2">**</bpt>TSTimesheetProjectService<ept id="p2">**</ept> class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Þessi sjálfgefna tegund er stillt í aðferðinni <bpt id="p1">**</bpt>fáProjectDetailsbyRule<ept id="p1">**</ept> í klasanum <bpt id="p2">**</bpt>TSTimesheetProjectService<ept id="p2">**</ept>.</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>