---
title: Formúluhönnuður í rafrænni skýrslugerð (ER)
description: Þessi grein inniheldur upplýsingar um hvernig á að nota formúluhönnuðinn í rafrænni skýrslugerð (ER).
author: kfend
ms.date: 04/08/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 283c882300ece460c18ffebe572238e7629f8dee
ms.sourcegitcommit: a1d14836b40cfc556f045c6a0d2b4cc71064a6af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/14/2022
ms.locfileid: "9476802"
---
# <a name="formula-designer-in-electronic-reporting-er"></a>Formúluhönnuður í rafrænni skýrslugerð (ER)

[!include [banner](../includes/banner.md)]

Þessi grein útskýrir hvernig nota á formúluhönnuður í Rafræna skýrslugerð (ER). Þegar þú hannar snið fyrir tiltekið rafrænt skjal í ER má nota formúlur til að umbreyta gögnum þannig að þau uppfylli kröfur um gerð og snið skjalsins. Þessar formúlur líkjast formúlum í Microsoft Excel. Ýmsar tegundir aðgerða eru studdar í formúlunum: texti, dagsetning og tími, stærðfræðilegar, röklegar, upplýsingar og umbreytingaraðgerðir gagnagerðar og einnig aðrar aðgerðir sem eru lénsértækar fyrir viðskipti.

## <a name="formula-designer-overview"></a>Yfirlit Formúluhönnuður.

Rafræn skýrslugerð styður formúluhönnuðinn. Á hönnunartíma er því hægt að skilgreina segðir sem hægt er að nota fyrir eftirfarandi verkefni á keyrslutíma:

- Umbreytingu gagna úr gagnagrunni forrits sem eiga að vera slegin inn í gagnalíkan rafrænnar skýrslugerðar sem er hannað til að vera gagnagjafi fyrir snið rafrænnar skýrslugerðar. (Til dæmis geta þessar umbreytingar innihaldið síun, flokkun og umbreytingu gagnagerða.)
- Sníðing gagna sem verða að vera send á stofnað rafrænt skjal í samræmi við útlit og skilyrði tiltekins sniðs rafrænnar skýrslugerðar. (Til dæmis gæti sniðið verið gert í samræmi við viðkomandi tungumál eða menningu eða kóðunina).
- Stjórna ferlinu sem stofnar rafræn skjöl. (Til dæmis geta segðirnar virkjað eða slökkt á framleiðsla tiltekinna eininga sniðsins, fer eftir vinnslugögnum. Þær geta einnig truflað skráarmyndunarferlið eða sent skilaboð til notenda.)

Þú getur opnað síðu **Formúluhönnuðar** þegar þú framkvæmir einhvern af eftirfarandi aðgerðum:

- Bindingu gagnaveituvöru við þætti gagnalíkans.
- Bindingu gagnaveituvöru við þætti til að sníða.
- Alhliða viðhald reiknaðra svæða sem eru hluti af gagnagjöfum.
- Skilgreining sýnileikaskilyrða og breytanleikaskilyrða fyrir innsláttarfæribreytur notanda.
- Skilgreina sjálfgefin gildi fyrir innsláttarfæribreytur notanda.
- Hönnun á umbreytingum sniðsins
- Skilgreining á virkjun skilyrða fyrir þætti sniðsins.
- Skilgreining á skrárheiti fyrir FILE-þætti sniðsins.
- Skilgreining á skilyrðum fyrir villuleit ferlisstýringar.
- Skilgreining á texta í skilaboðum fyrir villuleit á ferlisstýringu.

## <a name="data-binding"></a><a name="Binding"></a>gagnatengsl

Formúluhönnuður rafrænnar skýrslugerðar er hægt að nota til að skilgreina segð sem umbreytir gögnum sem eru móttekin frá gagnagjöfum, þannig að hægt sé að slá gögnin inn í gagnanotanda á eftirfarandi vegu á keyrslutíma:

- Úr gagnagjafa forrits og færibreytur keyrslutíma til gagnalíkans rafrænnar skýrslugerðar
- Úr gagnalíkani rafrænnar skýrslugerðar yfir í snið rafrænnar skýrslugerðar.
- Úr gagnagjafa forrits og færibreytur keyrslutíma til gagnalíkans ER-sniðmáts

Eftirfarandi skýringarmynd sýnir hönnun segðar af þessari gerð. Í þessu dæmi námundar segðin gildið í reitnum **Intrastat.AmountMST** í Intrastat-töflunni í tvo aukastafi og skilar síðan námunduðu gildi.

[![Segð gagnabindingar.](./media/picture-expression-binding.jpg)](./media/picture-expression-binding.jpg)

Eftirfarandi mynd sýnir hvernig hægt er að nota segð af þessari gerð. Í þessu dæmi er niðurstaðan af hannaðri segð slegin inn í **Transaction.InvoicedAmount** hlutann af gagnalíkani **skattaskýrslulíkansins**.

[![Segð gagnatengsla notuð.](./media/picture-expression-binding2.jpg)](./media/picture-expression-binding2.jpg)

Á keyrslutíma námundar hannaða formúlan `ROUND (Intrastat.AmountMST, 2)` gildið í reitnum **AmountMST** fyrir hverja skrá í Intrastat töflunni í tvo aukastafi. Hún slær þá inn námundaða gildið í **Transaction.InvoicedAmount** hlutann af gagnalíkani **skattaskýrslunnar**.

## <a name="data-formatting"></a><a name="Transformation"></a>Gagnasnið

Formúluhönnuður ER hægt að nota til að skilgreina segð sem forsníður gögn sem er tekið úr gagnagjafa, þannig að gögn geta verið send sem hluti af myndandi rafrænu skjali. Þú gætir haft snið sem þarf að nota sem dæmigerða reglu sem þarf að endurnýta sem snið. Í þessu tilviki getur þú lagt sniðið fram einu sinni í skilgreiningu sniðs, sem nefnda umbreytingu sem hefur sniðsegð. Þessi nefnda umbreyting er síðan hægt að tengja við margar sniðseiningar þar sem úttakið verður að vera sniðið í samræmi við sniðsegðina sem þú bjóst til.

Eftirfarandi skýringarmynd sýnir hönnun umbreytingar sem samanstendur af þessari gerð. Í þessu dæmi styttir **TrimmedString** umbreytingin gögn á innleið af gagnagerðinni *Strengur* með því að fjarlægja bil fyrir framan og aftan. Hún skilar þá styttu strengagildi.

[![Umbreyting.](./media/picture-transformation-design.jpg)](./media/picture-transformation-design.jpg)

Eftirfarandi skýringarmynd sýnir hvernig er hægt að nota umbreyting af þessari gerð. Í þessu dæmi senda nokkrir þættir sniðs texta sem úttak til að búa til rafrænt skjal á keyrslutíma. Allir þessir sniðsþættir vísa til **TrimmedString** umbreytingar eftir heiti.

[![Umbreyting sem er notuð.](./media/picture-transformation-usage.jpg)](./media/picture-transformation-usage.jpg)

Þegar þættir sniðs, eins og **partyName** í ofangreindum myndum, vísa til **TrimmedString** umbreytingingarinnar, sendir umbreytingin texta sem úttak á rafrænu skjalinu. Þessi texti inniheldur ekki bil fyrir framan og aftan.

Ef þú ert með snið sem þarf að nota eitt og sér, getur þú sett fram það snið sem einstaka segð bindingar fyrir tiltekna sniðsþáttinn. Eftirfarandi skýringarmynd sýnir segð sem samanstendur af þessari gerð. Í þessu dæmi er **partyType** sniðsþáttur bundinn gagnagjafanum með segð sem breytir gögnum á innleið frá **Model.Company.RegistrationType** svæðinu í gagnagjafanum í hástafi. Segðin sendir þá texta sem úttak til rafræna skjalsins.

[![Sækja um snið fyrir einstaka þætti.](./media/picture-binding-with-formula.jpg)](./media/picture-binding-with-formula.jpg)

## <a name="process-flow-control"></a><a name="Validation"></a>Vinnsla vinnsluflæðis

Formúluhönnuður rafrænnar skýrslugerðar er hægt að nota til að skilgreina segðir sem stýra vinnsluflæðinu við stofnun rafrænna skjala. Hægt er að framkvæma eftirfarandi verk:

- Skilgreina skilyrði til að ákvarða þegar þarf að stöðva ferli við myndun skjals
- Tilgreina segðir sem annað hvort búa til skilaboð fyrir notandann um stöðvuð ferli eða senda skilaboð aðgerðarskráningar um áframhaldandi ferli við myndun skýrslu.
- Tilgreina skráarnöfnin á stofnuðum rafrænum skjölum og stjórna skilyrðum fyrir stofnun þeirra.

Hverja reglu fyrir flæðistýringu ferlis er hannað sem einstaka villuleit. Eftirfarandi skýringarmynd sýnir sannvottun af þessari gerð. Hér er skýring á skilgreiningunni í þessu dæmi:

- Staðfestingin er metin þegar **INSTAT** hnúturinn á meðan XML-skráin er stofnuð.
- Það stöðvar aðgerðarferlið um leið og það skilar **FALSE** ef listi yfir færslur er tómur
- Sannvottunin skilar villuboð sem inniheldur texta merkis SYS70894 á tungumáli sem notandi kýs

[![Villuleit.](./media/picture-validation.jpg)](./media/picture-validation.jpg)

Formúluhönnuður rafrænnar skýrslugerðar er einnig hægt að nota til að stofna skráarnafn fyrir stofnað rafrænt skjal til að stjórna ferlinu fyrir stofnun skráa. Eftirfarandi skýringarmynd sýnir hönnun flæðistjórnunar ferlis sem samanstendur af þessari gerð. Hér er skýring á skilgreiningunni í þessu dæmi:

- Listi yfir færslur úr **model.Intrastat** gagnagjafanum er skipt í runur. Hver runa inniheldur allt að 1.000 færslur.
- Úttak býr til ZIP-skrá sem inniheldur eina skrá í xml-snið fyrir hverja runu sem var stofnuð.
- Segð skilar skráarnafni til að stofna rafræn skjöl með því að sameina skráarheiti og skráargerð. Fyrir aðra rönu og allar eftirfylgjandi runur inniheldur skráarheitið kenni runu sem nafnauka.
- Segð virkjar (með því að skila **TRUE**) ferli fyrir stofnun skráa fyrir runur sem innihalda að minnsta kosti eina færslu.

[![Stjórnun vinnsluflæðis.](./media/picture-file-control.jpg)](./media/picture-file-control.jpg)

## <a name="document-content-control"></a><a name="Enabled"></a>Efnisstýring skjals

Hægt er að nota ER-formúluhönnuðinn til að stilla segðir sem stjórna hvaða gögn verða sett inn í mynduð rafræn skjöl á keyrslutíma. Segðirnar geta virkjað eða afvirkjað úttak tiltekinna eininga sniðsins, eftir því hver vinnslugögn og skilgreindur grunnur er. Hægt er að færa þessar segðir inn fyrir stakt snið í reitnum **Virkt** á flipanum **Vörpun** á síðunni **Rekstrarhönnuður**. Þú getur slegið inn orðin sem röklegt skilyrði sem skilar *Boole*-gildi:

- Ef skilyrðið skilar **True** er gildandi sniðþáttur keyrður.
- Ef skilyrðið skilar **False** er gildandi sniðþætti sleppt.

Eftirfarandi skýringarmynd sýnir segðir af þessari gerð. (Útgáfa 11.12.11 af **ISO20022-kreditfærslu (NO)** skilgreiningu sniðs sem er veitt af Microsoft er notuð sem dæmi.) Sniðsíhlutinn **XMLHeader** er stilltur til að lýsa skipulagi skilaboða kreditfærslunnar í samræmi við XML-skilaboðastaðla ISO 20022. Sniðshlutinn **XMLHeader/Document/CstmrCdtTrfInitn/PmtInf/CdtTrfTxInf/RmtInf/Ustrd** er skilgreindur til að bæta XML-einingunni **Ustrd** við mynduðu skilaboðin og setur greiðsluupplýsingarnar á óskipulegt snið sem texta í eftirfarandi XML-einingum:

- Íhluturinn **PaymentNotes** er notaður til að mynda texta í athugasemdir við greiðslur.
- Íhluturinn **DelimitedSequence** myndar kommuaðskilin reikningsnúmer sem eru notuð til að jafna núverandi kreditfærslu.

[![PaymentNotes og DelimitedSequence íhlutir.](./media/GER-FormulaEditor-ControlContent-1.png)](./media/GER-FormulaEditor-ControlContent-1.png)

> [!NOTE]
> Íhlutirnir **PaymentNotes** og **DelimitedSequence** eru merktir með spurningarmerki. Spurningarmerki gefur til kynna að notkun íhluta sé skilyrt. Í þessu tilfelli er notkun íhlutanna byggð á eftirfarandi forsendum:
>
> - Segðin `@.PaymentsNotes <> ""` sem er skilgreind fyrir íhlutinn **PaymentNotes** gerir kleift (með því að skila **TRUE**) að XML-þátturinn **Ustrd** sé fylltur út með texta greiðsluathugasemda ef sá texti er ekki tómur fyrir gildandi kreditfærslu.
>
>    [![Segð fyrir íhlut PaymentNotes.](./media/GER-FormulaEditor-ControlContent-2.png)](./media/GER-FormulaEditor-ControlContent-2.png)
>
> - Segðin `@.PaymentsNotes = ""` sem er skilgreind fyrir íhlutinn **DelimitedSequence** gerir kleift (með því að skila **TRUE**) að XML-þátturinn **Ustrd** sé fylltur út með kommuaðskildum lista yfir reikningsnúmerin sem eru notuð til að jafna gildandi kreditfærslu, ef texti greiðsluathugasemdanna fyrir þá kreditfærslu er tómur.
>
>    [![Segð fyrir íhlut DelimitedSequence.](./media/GER-FormulaEditor-ControlContent-3.png)](./media/GER-FormulaEditor-ControlContent-3.png)
> 
> Byggt á þessari uppsetningu munu skilaboðin sem myndast fyrir hverja greiðslu skuldara, XML-eininguna **Ustrd**, innihalda annaðhvort texta greiðsluseðla eða, þegar slíkur texti er auður, texta aðskilinn með kommu reikningsnúmer sem notuð eru til að jafna þessa greiðslu.

## <a name="assistance-in-formulas-writing"></a>Aðstoð við að skrifa formúlur

### <a name="data-sources-navigator"></a>Gagnagjafafletting

Hægt er að breyta formúlu sem stendur fyrir einingu af skipulögðum gagnagjafa. Þegar þú skilgreindir færibreytur rafrænnar skýrslugerðar til að gefa upp slóðina á einingu af skipulögðum gagnagjafa sem [tengda slóð](relative-path-data-bindings-er-models-format.md) er @-merkið [sýnt](er-formula-language.md#relative-path) í formúlunni í staðinn fyrir það sem eftir er af heildarslóðinni fyrir trjáskipulag stigveldis sem er notað. Þessi eftirstandandi hluti heildarslóðarinnar er beint að yfireiningu á þeirri breytanlegu. Í útgáfu **10.0.30 og síðar** af Finance er hægt á síðunni **Formúluhönnuður**, á svæðinu **Gagnagjafar**, að velja valkostinn **Fara í @** til að staðsetja bendi gagnagjafatrésins á einingu sem er yfireining þeirrar breytanlegu. Skipulag allra samandreginna eininga verður sjálfkrafa stækkað aftur þegar þess gerist þörf. Þessi stækkun getur hjálpað þér að sjá á myndrænan hátt grunneiningu á þeirri breytanlegu, skoðað einingar sem eru tengdar breytanlegu einingunni í tré gagnagjafans og notað hverja þeirra í breytanlegri formúlu ef þess gerist þörf.

![Notaðu valkostinn „Fara í @“ til að staðsetja bendil gagnagjafatrésins á einingu sem er yfireining breytanlegu einingarinnar á síðu formúluhönnuðar.](./media/er_formula-designer-data-sources-navigator.gif)

### <a name="data-sources-picker"></a>Gagnagjafaval

Á síðunni **Formúluhönnuður**, á svæðinu **Gagnagjafar** vinstra megin, skal velja einingu gagnagjafa sem á að flytja inn í breytanlegu formúluna. Veldu síðan **Bæta við gagnagjafa**. Taktu eftir því að valdri einingu er bætt við texta breytanlegrar formúlu.

> [!TIP]
> Þegar þú notar valkostinn **Bæta við gagnagjafa** í sjálfgefnum formúluritli er valinni einingu alltaf bætt við enda formúlutextans. Þegar þú gerir það sama í [Ítarlegum formúluritli](er-advanced-formula-editor.md) er valin eining sett inn í formúlutextann á núverandi staðsetningu bendilsins.

### <a name="built-in-functions-picker"></a>Innbyggt fallaval

Á síðunni **Formúluhönnuður**, á svæðinu **Virkni** hægra megin, skal velja innbyggða virkni rafrænnar skýrslugerðar sem á að flytja inn í breytanlegu formúluna. Síðan velurðu **Bæta við aðgerð**. Taktu eftir að valinni virkni er bætt við texta breytanlegu formúlunnar.

> [!TIP]
> Þegar þú notar valkostinn **Bæta við virkni** í sjálfgefna formúluritlinum er valinni virkni alltaf bætt við enda formúlutextans. Þegar þú gerir það sama í [Ítarlegum formúluritli](er-advanced-formula-editor.md) er valin virkni sett inn í formúlutextann á núverandi staðsetningu bendilsins.

### <a name="validation-of-configured-formulas"></a><a name="TestFormula"></a>Staðfesting á uppsettum formúlum

Á síðunni **Formúluhönnuður** velurðu **Prófa** til að sannreyna hvernig uppsetta formúlan virkar.

[![Val á prófi til að staðfesta formúlu.](./media/ER-FormulaTest-Start.png)](./media/ER-FormulaTest-Start.png)

Þegar gilda formúlufrumbreyta er krafist geturðu opnað valmyndina **Prófunarsegð** af síðunni **Formúluhönnuður**. Í flestum tilvikum verður að skilgreina þessar frumbreytur handvirkt þar sem stilltar bindingar eru ekki keyrðar á hönnunartíma. Flipinn **Niðurstaða prófunar** á síðunni **Formúluhönnuður** sýnir niðurstöðuna úr framkvæmd stilltrar formúlu.

Eftirfarandi dæmi sýnir hvernig þú getur prófað formúluna sem er stillt fyrir utanríkisviðskiptalén til að ganga úr skugga um að Intrastat grunnvörukóðinn innihaldi aðeins tölustafi.

Þegar þú prófar þessa formúlu geturðu notað valmyndina **Prófunarsegð** til að tilgreina gildi Intrastat grunnvörukóðans fyrir prófun.

[![Intrastat grunnvörukóða tilgreint fyrir prófun.](./media/ER-FormulaTest-Start-EnterArguments.png)](./media/ER-FormulaTest-Start-EnterArguments.png)

Eftir að þú hefur tilgreint Intrastat grunnvörukóðann og valið **Í lagi** sýnir flipinn **Niðurstaða prófunar** á síðunni **Formúluhönnuður** niðurstöðu framkvæmdar á stilltri formúlu. Þú getur síðan metið hvort niðurstaðan sé ásættanleg. Ef niðurstaðan er ekki ásættanleg geturðu uppfært formúluna og prófað hana aftur.

[![Niðurstaða prófunar.](./media/ER-FormulaTest-Result.png)](./media/ER-FormulaTest-Result.png)

Sumar formúlurnar er ekki hægt að prófa á hönnunartíma. Til dæmis gæti formúla skilað niðurstöðu gagnategundar sem ekki er hægt að sýna á flipanum **Niðurstaða prófunar**. Í því tilfelli færðu villuboð sem segja að ekki sé hægt að prófa formúluna.

[![Villuboð.](./media/ER-FormulaTest-Error.png)](./media/ER-FormulaTest-Error.png)

## <a name="additional-resources"></a>Frekari upplýsingar

- [Yfirlit yfir rafræna skýrslugerð](general-electronic-reporting.md)
- [Formúlutungumál í rafrænni skýrslugerð](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
