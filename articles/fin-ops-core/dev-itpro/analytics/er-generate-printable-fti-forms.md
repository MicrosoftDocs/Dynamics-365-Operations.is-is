---
title: Búa til eyðublöð fyrir reikninga með frjálsum texta sem hægt er að prenta
description: Þetta efnisatriði útskýrir hvernig nota á ramma rafrænnar skýrslugerðar til að búa til prentvæn eyðublöð fyrir reikninga með frjálsum texta sem Microsoft Office skjöl.
author: NickSelin
manager: AnnBe
ms.date: 07/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 731b6a61bd78388f3db0a7007478e3a5e9629a49
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2181428"
---
# <a name="generate-printable-fti-forms"></a>Búa til eyðublöð fyrir reikninga með frjálsum texta sem hægt er að prenta

[!include[banner](../includes/banner.md)]

Rammi rafrænnar skýrslugerðar leyfir þér að búa til prentvæn eyðublöð fyrir reikninga með frjálsum texta sem Microsoft Office skjöl. Þetta efnisatriði veitir upplýsingar um hvernig á að útbúa sínar eigin skilgreiningar sem og upplýsingar um tiltæk grunnstillingarsniðmát.

## <a name="overview"></a>Yfirlit

Til viðbótar við fyrirliggjandi getu til að búa til prentvæn eyðublöð reikninga með frjálsum texta með því að nota Microsoft SQL Server Reporting Services (SSRS), getur þú nú notað ramma rafrænnar skýrslugerðar. Þú getur haft umsjón með prentvænum eyðublöðum reikninga með frjálsum texta í Microsoft Office Excel og Word. Þú getur einnig breytt útliti, gagnaflæði og sniði til að mæta sérstökum kröfum án þess að breyta kóðum.

> [!NOTE]
> Ef þú vilt byrja með yfirliti yfir núverandi grunnstillingar rafrænnar skýrslugerðar fyrir þetta sýnishorn af úrlausn á prentvænu eyðublaði fyrir reikninga með frjálsum texta, getur þú farið beint í kaflann **Sækja sýnishorn af grunnstillingu rafrænnar skýrslugerðar til að búa til prentvæn eyðublöð fyrir reikninga með frjálsum texta** seinna í þessu efnisatriði.

## <a name="create-customized-configurations-for-fti-printable-forms"></a>Búa til sérsniðnar grunnstillingar fyrir prentvæn eyðublöð reikninga með frjálsum texta
Sem hluti af sérsniðnu lausninni fyrir prentvæn eyðublöð reikninga með frjálsum texta getur þú búið til safn af grunnstillingum rafrænnar skýrslugerðar.

### <a name="configure-the-er-data-model"></a>Skilgreina gagnalíkan rafrænnar skýrslugerðar
Jöfnunin þín verður að taka með skilgreiningu á gagnalíkani rafrænnar skýrslugerðar sem inniheldur gagnalíkan sem lýsir reikningsfærðu viðskiptaléni viðskiptavinar. Sem skilyrði verður heiti gagnalíkansins að vera **CustomersInvoicing**. Nánari upplýsingar um hvernig á að hanna gagnalíkön rafrænnar skýrslugerðar er að finna í [Hanna gagnalíkan fyrir sérstakt lén fyrir rafræna skýrslugerð (ER)](tasks/er-design-domain-specific-data-model-2016-11.md).

### <a name="configure-the-er-model-mapping"></a>Skilgreina vörpun líkans rafrænnar skýrslugerðar
Forritið þitt verður að innihalda vörpun líkans rafrænnar skýrslugerðar fyrir gagnalíkan CustomersInvoicing. Vörpun líkans getur verið í annaðhvort skilgreiningu gagnalíkans rafrænnar skýrslugerðar eða skilgreiningu fyrir vörpun líkans rafrænnar skýrslugerðar. Heiti rótarlýsingar fyrir vörpun líkans verður hins vegar að vera **FreeTextInvoice**.

Vörpunin verður að innihalda eftirfarandi gagnaveitur:

- Gerð gagnaveitu: **Töflufærslur**

    - Þessi gagnaveita verða að vera nefnd **CustInvoiceJour**.
    - Það verður að vísa til jöfnunartöflu CustInvoiceJour.
    - Hún er notuð við keyrslu til að fara frá jöfnuninni á líkani rafrænnar skýrslugerðar sem varpar lista yfir reikninga sem hafa verið valdir til prentunar.

- Gerð gagnaveitu: **Hlutur**

    - Þessi gagnaveita verða að vera nefnd **PrintMgmtPrintSettingDetail**.
    - Hún verður að vísa til umsóknarflokksins **PrintMgmtPrintSettingDetail**.
    - Það er notað við keyrslu til að fara frá forritinu til upplýsinga um stillingar prentstýringar fyrir líkanavörpun rafrænnar skýrslugerðar fyrir snið rafrænnar skýrslugerðar sem er í gangi.

Upplýsingar um samþættingu forritsins við ramma rafrænnar skýrslugerðar er hægt að finna í **ERPrintMgmtReportFormatSubscriber** klasanum (samþættingarlíkan fyrir forritapakka rafrænnar skýrslugerðar) í frumkóða forritsins.

Nánari upplýsingar um hönnunina á líkanavörpun rafrænnar skýrslugerðar er að finna í [Skilgreina líkanavörpun og velja gagnaveitur fyrir rafræna skýrslugerð (ER)](tasks/er-define-model-mapping-select-data-sources-2016-11.md).

### <a name="configure-the-er-format"></a>Skilgreina snið rafrænnar skýrslugerðar
Í forritatilviki þínu verður þú að hafa þá grunnstillingu fyrir rafræna skýrslugerð sem verður notuð til að búa til eyðublöð reikninga með frjálsum texta. 

> [!NOTE]
> Þessi grunnstilling á sniði verður að vera búin til fyrir gagnalíkanið CustomersInvoicing og hún verður að nota vörpun líkans sem er með rótarlýsinguna **FreeTextInvoice**.

Nánari upplýsingar um hvernig á að grunnstilla snið rafrænnar skýrslugerðar er að finna í [Stofna skilgreiningu sniðs fyrir rafræna skýrslugerð (ER)](tasks/er-format-configuration-2016-11.md). Nánari upplýsingar um hvernig á að hanna snið rafrænnar skýrslugerðar til að búa til skýrslur í OpenXML-sniði er að finna í [Hanna skilgreiningu fyrir myndun skýrslna á OpenXML-sniði fyrir rafræna skýrslugerð (ER)](tasks/er-design-reports-openxml-2016-11.md).

## <a name="configure-print-management"></a>Skilgreina prentstýringu
Til að búa til eyðublöð reikninga með frjálsum texta með því að nota ramma rafrænnar skýrslugerðar, getur þú úthlutað sniðum rafrænnar skýrslugerðar á sama hátt og þú úthlutar SSRS-skýrslum. Til að tengja snið rafrænnar skýrslugerðar við allar viðskiptakröfur reikninga með frjálsum texta skal fara í **Viðskiptakröfur** \> **Uppsetning** \> **Eyðublöð** \> **Uppsetning eyðublaðs** \> **Almennt** \> **Prentstýring** \> **Reikningur með frjálsum texta** \> **Upprunalegt**. Til að tengja snið rafrænnar skýrslugerðar við tiltekinn viðskiptavin eða reikning skal fylgja þessum skrefum.

1. Fara í **Viðskiptakröfur** \> **Reikningar** \> **Allir reikningar með frjálsum texta**.
2. Veldu reikninga með frjálsum texta sem á að tengja snið rafrænnar skýrslugerð við og opnaðu síðuna **Uppsetning prentstýringar**.
3. Veldu skjalastigið til að tilgreina umfang reikninga til vinnslu.
4. Veldu snið rafrænnar skýrslugerðar fyrir tiltekið skjalastig.

![Uppsetning á prentstýringu](media/FTIbyGER-PMSetting.png)

> [!NOTE]
> Aðeins snið rafrænnar skýrslugerðar sem nota rótarlýsinguna **FreeTextInvoice** af gagnalíkaninu **CustomersInvoicing** birtast í reitnum **Uppfletting skýrslusniðs** fyrir valið snið.

## <a name="generate-fti-forms"></a>Mynda eyðublöð fyrir reikninga með frjálsum texta
Eyðublöð reikninga með frjálsum texta eru mynduð í ramma rafrænnar skýrslugerðar á sama hátt og SSRS-skýrslur eru búnar til.

Til að búa til eyðublöð reikninga með frjálsum texta er hægt að velja reikninga annaðhvort eftir sviði eða með vali. 

![Val reiknings](media/FTIbyGER-InvoiceSelection.png)

![Forskoðun reiknings](media/FTIbyGER-InvoiceExcelPreview.png)

Þegar þú notar snið rafrænnar skýrslugerðar til að prenta eyðublöð reikninga með frjálsum texta á þennan hátt, eru sjálfgefnir viðtökustaðir fyrir skrár rafrænnar skýrslugerðar notaðir. Ekki er hægt að breyta viðtökustaðnum. Frekari upplýsingar um hvernig á að grunnstilla viðtökustaði rafrænnar skýrslugerðar fyrir ramma rafænnar skýrslugerðar er að finna í [Viðtökustaðir rafrænnar skýrslugerðar](electronic-reporting-destinations.md).

Þú getur einnig búið til eyðublöð reikninga með frjálsum texta þegar þú bókar reikning með frjálsum texta með því að kveikja á **Prenta reikning** og slökkva á **Nota viðtökustað prentstýringar**.

> [!NOTE]
> Þegar þú notar snið rafrænnar skýrslugerðar til að prenta eyðublöð reikninga með frjálsum texta á þennan hátt, eru sjálfgefnir viðtökustaðir fyrir skrár rafrænnar skýrslugerðar notaðir. Hægt er að breyta sjálfgefnum viðtökustað við keyrslu ef viðtökustaðurinn hefur þegar verið skilgreind. Til að breyta viðtökustað verður þú að hafa eftirfarandi öryggisréttindi:
>
> - **Heiti:** ERFormatDestinationRuntimeMaintain
> - **Merkimiði:** Vinna með viðtökustað rafræns skýrslugerðarsniðs við keyrslu

![Viðtökustaður rafrænnar skýrslugerðar](media/FTIbyGER-ERFileDestinationSetting.png)

![Viðtökustaðir rafræns skýrslugerðarsniðs](media/FTIbyGER-ERFileDestinationUsage.png)

Rammi rafrænnar skýrslugerðar styður nú eftirfarandi viðtökustaði fyrir mynduð skjöl:

- **Sótt skrá** - Mynduð eyðublöð eru í boði sem niðurhal sem hægt er að vista með því að nota vafrann.
- **Skjár** - Microsoft Office 365 Excel er notað til að forskoða mynduð eyðublöð reikninga með frjálsum texta á Excel-sniði.
- **SharePoint mappa** - Mynduð eyðublöð eru geymd á grundvelli stillinga á ramma skjalastjórnar.
- **Safnvistun umsóknar** - Mynduð skjöl eru geymd sem viðhengi skráa fyrir aðgerðarskráningu í Microsoft Azure geymslu.
- **Tölvupóstur** - Mynduð eyðublöð eru send sem tölvupóstviðhengi.

> [!NOTE]
> Þú getur ekki sent eyðublöð reikninga með frjálsum texta sem eru búin til beint á prentarann vegna þess að bein prentun sem notar Dynamics Printer Routing Agent er ekki studd.

## <a name="download-sample-er-configurations-to-generate-printable-fti-forms"></a>Sækja sýnishorn af skilgreiningum rafrænnar skýrslugerðar til að búa til prentvæn eyðublöð fyrir reikninga með frjálsum texta
Þú getur sótt sýnishorn af skilgreiningum rafrænnar skýrslugerðar til að nota sem sniðmát fyrir lausnina þína á reikningum með frjálsum texta. Skilgreiningarnar eru geymdar í samnýttu eignasafni í Microsoft Dynamics Lifecycle Services (LCS). Skilgreiningarnar fela í sér:

- Skilgreiningin **Reikningslíkan viðskiptavinar** innheldur nauðsynlegt gagnalíkan og vörpun líkans.
- Skilgreiningin **Skýrsla viðskiptamannareiknings með frjálsum texta (GER)** inniheldur sýnishornasniðið.

> [!NOTE]
> Þessar skilgreiningar hafa verið búnar til sem sýnishorn til að hjálpa að varpa ljósi á mögulegar atburðarásir. Framtíð þessara skilgreininga fer eftir niðurstöðum á þessu mati og öllum ábendingum sem berast.

### <a name="features-that-are-implemented-in-the-sample-er-format"></a>Eiginleikar sem eru innleiddir í sýnishorn fyrir snið rafrænnar skýrslugerðar
Í sýnishorninu af skilgreiningu sniðs fyrir rafræna skýrslugerð er Excel-skrá notuð sem sniðmát til að búa til eyðublöð reikninga með frjálsum texta.

![Sniðshönnuður](media/FTIbyGER-ERFormat.png)

Eins og er styður þetta sýnishorn af sniði fyrir rafræna skýrslugerð eftirfarandi eiginleika til að búa til eyðublöð reikninga með frjálsum texta:

- Eyðublöð reikninga með frjálsum texta eru búin til fyrir bæði upprunalega reikninga sem hafa verið bókaðir og upprunalega reikninga sem hafa ekki verið bókaðir. Leiðréttir reikningar og kreditnótur eru ekki studdar.
- Eyðublöð reikninga með frjálsum texta eru búnir til á tungumáli reiknings. Sniði fyrir gildi og dagsetningar í myndaða eyðublaðinu byggist á stillingum á staðsetningu á biðlara notandans.
- Myndaðir reikningar sýna tilkynningar um gögn sem ekki eru í boði ef það eru engar línur í reikningum sem er unnið úr.
- Myndaðar fyrirsagnir reikninga eru byggðir á blaðsíðusniðinu sem hefur verið valið fyrir eyðublað reikninga með frjálsum texta á síðunni **Færibreytur viðskiptakrafna**. Upplýsingar um fyrirtæki birtast aðeins í haus á mynduðu reikningssniði ef blaðsíðusniðið er autt.
- Mynduð eyðublöð reiknings sýna skattundanþágunúmer fyrirtækis og viðskiptavinar þegar hentugur valkostur hefur verið valinn fyrir eyðublað reikninga með frjálsum texta á síðunni **Færibreytur viðskiptakrafna**.
- Myndaðir hlutar reikningslína og heildarupphæða reikninga sýna sjálfgefnar myntupplýsingar reiknings í skráðum gjaldmiðli reiknings.
- Myndaður hluti heildarupphæða reikninga getur sýnt myntupplýsingar í evrum og skráðum gjaldmiðli reiknings þegar valkosturinn **Prenta upphæð í gjaldmiðli sem sýnir evrur** er gerður virkur á síðunni **Færibreytur viðskiptakrafna**.
- Mynduð eyðublöð reiknings sýna allar athugasemdir við reikninga sem hefur verið unnið úr, byggt á stillingum á síðunni **Færibreytur viðskiptakrafna**. Athugasemdir eru hafðar með bæði fyrir allan reikninginn og hverja reikningslínu.
- Mynduð eyðublöð reiknings innihalda athugasemdir fyrir viðskiptavin eyðublaðs reiknings með frjálsum texta og tungumál reikningsins sem unnið er úr þegar þeir hafa verið grunnstilltir í athugasemdalista fyrir eyðublað viðskiptakrafna.
- Það fer eftir stillingum prentstýringar hvort myndaðir reikningar fela í sér sérsniðinn neðanmálstexta þegar hann hefur verið skilgreindur fyrir tungumál reiknings, snið rafrænnar skýrslugerðar og skjalasvið reiknings með frjálsum texta.
- Samtöluhlutinn af mynduðum eyðublöðum reiknings inniheldur allar upplýsingar um staðgreiðsluafslætti sem eru í boði.
- Greiðsluáætlunarhluti myndaðra eyðublaða reiknings inniheldur allar upplýsingar um greiðsluáætlanir sem eru í boði.
- Álagningarhluti myndaðra eyðublaða reiknings inniheldur allar gjaldafærslur sem eru í boði.
- Mynduð eyðublöð reiknings innihalda upplýsingar um virðisaukaskatt sem byggjast á stillingunni **VSK-forskrift** á síðunni **Færibreytur viðskiptakrafna**. Þessi hluti getur sýnt skattaupplýsingar annaðhvort aðeins í skráðum gjaldmiðli reiknings eða í skráðum gjaldmiðli reiknings og bókhaldsgjaldmiðli fyrirtækis á sama tíma.
- Mynduð eyðublöð reiknings sýna upplýsingar um beingreiðslutilkynningar. Þau sýna til dæmis hvenær greiðslumátinn sem er með áskilið kenni umboðs fyrir beingreiðslu var valinn fyrir reikninginn, hvenær úrvinnslureikningur var skráður í evrum og hvenær kenni umboðs fyrir beingreiðslu var skilgreint fyrir reikninginn.
- Myndaðir reikningar sýna allar upplýsingar um fyrirframgreiðslu sem eru tiltækar fyrir bókaða reikninga.
- Hægt er að senda myndað eyðublað reiknings til reikningsfærðs viðskiptavinar sem tölvupóstviðhengi. Skilgreina ætti viðeigandi viðtökustaður fyrir skrá rafrænnar skýrslugerðar fyrir það snið rafrænnar skýrslugerðar sem er notað.

### <a name="countryregion-specific-features"></a>Eiginleikar fyrir tiltekin lönd/svæði 
Eftirfarandi eiginleikar fyrir tiltekin lönd/svæði eru með í sýnishorni af sniði rafrænnar skýrslugerðar til að sýna hvernig hægt er að meðhöndla ákveðin skilyrði í grunnstillingum rafrænnar skýrslugerðar.

#### <a name="norway"></a>Noregur
Skilmáli fyrirtækjaskrár er settur í hausinn á mynduðu eyðublaði reiknings þegar unnið er úr reikningnum fyrir lögaðila sem er skilgreindur á eftirfarandi hátt:

- Samhengi lands/svæðis fyrir Noreg er notað.
- Færibreytan **Print Foretaksregisteret** er virk í söluskjölum.

#### <a name="spain"></a>Spánn
Skilmálinn **Sérstakt fyrirkomulag vegna bókhaldsaðferðar reiðufjár** er settur í hausinn á mynduðu eyðublaði reiknings þegar unnið er úr reikningnum fyrir lögaðila sem er skilgreindur á eftirfarandi hátt:

- Samhengi lands/svæðis fyrir Spán er notað.
- Sérstakt fyrirkomulag vegna bókhaldsaðferðar reiðufjár er virkjað á úrvinnsludegi reiknings.

Þegar upplýsingar um staðgreiðsluafslátt, t.d. upphæð staðgreiðsluafsláttar og nettóupphæð reikningslínu, eru tiltækar þá eru þær sýndar í hlutanum heildarupphæðir reikninga í mynduðu eyðublaði reiknings þegar unnið hefur verið úr honum fyrir lögaðila sem er skilgreindur á eftirfarandi hátt:

- Samhengi lands/svæðis fyrir Spán er notað.
- **Kveikt er á staðgreiðsluafslætti** í valkosti reikningsins (**Færibreytur fjárhags** \> **VSK-hluti**).

#### <a name="italy"></a>Ítalía
Afsláttarmerki vara er haft með í reikningslínum á mynduðum reikningi þegar unnið er úr honum fyrir lögaðila sem er skilgreindur með samhengi lands/svæðis fyrir Ítalíu.

#### <a name="finland"></a>Finnland
Auk eyðublaðs fyrir myndaðan reikning er hægt að mynda gíróseðla á eftirfarandi hátt:

- Fyrir lögaðilann sem notar samhengi lands/svæðis fyrir Finnland og sem hefur að minnsta kosti einn bankareikning sem merktur er sem **Gíróreikningur** og **Bankastrikamerki**. 
- Fyrir reikning sem er merktur eins og krafist er fyrir **Finnskt** tengda greiðsluviðhengið.

![Gíróseðill](media/FTIbyGER-GiroSlip.PNG)

> [!NOTE]
> Sýnishorn fyrir snið rafrænnar skýrslugerðar hefur verið skilgreint til að valfrjálst mynda gíróseðil í aðskilda vinnublaðinu.

> [!NOTE]
> Þú verður fyrst að setja upp leturgerðina sem er notuð til að búa til strikamerki á staðbundinni vél þar sem myndaða reikningseyðublaðið í Excel-sniði verður sýnt.

### <a name="use-the-sample-er-format-to-configure-email-destinations"></a>Notaðu sýnishorn af sniði rafrænnar skýrslugerðar til að skilgreina viðtökustað tölvupósts
Notaðu eftirfarandi þætti af sýnishorni af sniði rafrænnar skýrslugerðar til að skilgreina viðtökustaði tölvupósts:

- Netfang tengiliðar viðskiptavinar er hægt að nálgast með eftirfarandi segð rafrænnar skýrslugerðar: **model.InvoiceBase.Contact.ElectronicMail**.
- Efnistexta tölvupósts er hægt að nálgast með eftirfarandi segð rafrænnar skýrslugerðar: **Emailing.TxtToUse.Subject**.
- Meginmál tölvupósts er hægt að nálgast með eftirfarandi segð rafrænnar skýrslugerðar: **Emailing.TxtToUse.Body**.

![Stillingar viðtökustaðar](media/FTIbyGER-ERFileDestinationSettingEmail.png)

Sjálfgefinn efnistexti og meginmál tölvupósts er skilgreint í sýnishorninu af sniði rafrænnar skýrslugerðar. Tungumálið fer eftir merkjum sniðsins. Þessi sjálfgefni texti verður notaður fyrir tölvupósta ef sérsniðið sniðmát fyrir tölvupóst fyrirtækis sem er með fyrirfram skilgreinda auðkennið **ERFTITMP** hefur ekki verið bætt við.

> [!NOTE]
> Auðkennið **ERFTITMP** fyrir sniðmát tölvupósts hefur verið skilgreint í sýnishorninu af sniði rafrænnar skýrslugerðar. Hægt er að breyta því eftir þörfum í nýju sniði rafrænnar skýrslugerðar sem er búið til úr þessu sýnishornasniði.

Ef sniðmát fyrir tölvupóst fyrirtækis sem er með fyrirfram skilgreinda auðkennið **ERFTITMP** hefur verið bætt við fyrir lögaðilann sem verið er að meðhöndla reikning fyrir, verður sniðmátið fyrir efnistexta og meginmál tölvupósts notað til að búa til tölvupóstinn. 

![Sniðmát tölvupósts fyrirtækis](media/FTIbyGER-EmailTemplate.png)

![Hlaða upp sniðmát fyrir tölvupóst](media/FTIbyGER-EmailTemplateBody.png)

Segð rafrænnar skýrslugerðar **Emailing.TxtToUse.Subject** fyrir sýnishorn af sniði rafrænnar skýrslugerðar er skilgreint til að taka við af öllum tilvikum staðgengilsins %1 eftir reikningskenninu sem unnið er úr.

Segðin **Emailing.TxtToUse.Body** sýnishornasniðsins er skilgreind fyrir eftirfarandi skipti á staðgenglum:

- „%1“ er skipt út fyrir nafn á tengiliði viðskiptavinar.
- „%2“ er skipt út fyrir nafn fyrirtækis.
- „%3“ er skipt út fyrir nafn viðskiptavinar.
- „%4“ er skipt út fyrir nafn á tengiliði fyrirtækis.
- „%5“ er skipt út fyrir starfsheiti á tengiliði fyrirtækis.
- „%6“ er skipt út fyrir netfang tengiliðar fyrirtækis.

![Netfang](media/FTIbyGER-Email.PNG)

## <a name="additional-resources"></a>Frekari upplýsingar
[Yfirlit yfir rafræna skýrslugerð](general-electronic-reporting.md)
