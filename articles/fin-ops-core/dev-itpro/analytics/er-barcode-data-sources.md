---
title: Nota gagnagjafa strikamerkja til að búa til myndir af strikamerkjum
description: Þetta efnisatriði útskýrir hvernig á að nota gagnagjafa strikamerkja til að búa til myndir af strikamerkjum.
author: NickSelin
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: Version 10.0.13
ms.openlocfilehash: 973e46d5e5e7e9efb3037757ccb2b30f319ad13fd92261d58fde10fe0c235f9b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6714612"
---
# <a name="use-barcode-data-sources-to-generate-bar-code-images"></a>Nota gagnagjafa strikamerkja til að búa til myndir af strikamerkjum

[!include[banner](../includes/banner.md)]

Hægt er að nota rammann [Rafræn skýrslugerð](general-electronic-reporting.md) til að hanna [Íhlutir rafrænnar skýrslugerðar](general-electronic-reporting.md#FormatComponentOutbound) sem hægt er að keyra til að búa til rafræn og prentvæn skjöl á útleið sem þörf er á. Til að búa til skjal á útleið í Microsoft Office-sniði þarf að tilgreina útlit skýrslunnar með því að nota annaðhvort Microsoft Excel-skjal eða Microsoft Word-skjal sem skýrslusniðmát. [Hönnuður rafrænnar skýrslugerðar](general-electronic-reporting.md#building-a-format-that-uses-a-data-model-as-a-base) gerir notanda kleift að láta Excel- eða Word-skjal fylgja með sem sniðmát fyrir snið rafrænnar skýrslugerðar. Eftirfarandi tilgreindar einingar í viðhengdu sniðmáti tengjast einingum stillts sniðshluta:

- Efnisstýringar í Word
- Tilgreind blöð, bil, hólf, form og myndir í Excel

Þessar tilgreindu einingar eru notaðar sem staðgenglar fyrir gögn sem slegin eru inn í myndað skjal þegar snið rafrænnar skýrslugerðar er keyrt. Einingar í sniði rafrænnar skýrslugerðar eru bundnar við gagnagjafa. Þessir gagnagjafar tilgreina gögnin sem slegin verða inn í mynduðum skjölum á keyrslutíma. Nánari upplýsingar er að finna í [Felldu inn myndir og form í skjöl sem þú myndar með því að nota ER](electronic-reporting-embed-images-shapes.md)

Rafræn skýrslugerð styður nú gagnagjafa af gerðinni **Strikamerki**. Þess vegna er nú hægt að búa til mynd sem táknar strikamerkið fyrir tiltekinn texta. Þegar snið rafrænnar skýrslugerðar er grunnstillt er hægt að tilgreina gagnagjafa af gerðinni **Strikamerki** til að búa til myndir af strikamerkjum. Síðan er hægt að bæta þessum myndum við útbúin viðskiptaskjöl, t.d. pantanir, reikningar, fylgiseðlar og kvittanir. Einnig er hægt að bæta þeim við ýmiss konar merkingar, t.d. vöru- og hillumerkingar og umbúða- og gámamerkingar.

Nota má eftirfarandi staðgengla í skýrslusniðmátum til að færa inn strikamerkjamyndir:

- Efnisstýring [Myndar](/office/client-developer/word/content-controls-in-word) fyrir Word
- Hlutur [Myndar](https://support.office.com/article/insert-pictures-3c51edf4-22e1-460a-b372-9329a8724344) í Excel

Með því að nota gagnagjafa af gerðinni **Strikamerki** er hægt að búa til strikamerki á eftirfarandi sniðum:

- Einvídd strikamerki:

    - Codabar
    - Code 39
    - Code 93
    - Code 128
    - EAN-8
    - EAN-13
    - ITF-14
    - Snjallpóstur
    - MSI
    - Plessey
    - PDF417
    - UPC-A
    - UPC-E

- Tvívídd strikamerki:

    - Aztec
    - Gagnafylki
    - QR-kóði

Þegar gagnagjafinn **Strikamerki** er stilltur er hægt að skilgreina tilteknar færibreytur myndþýðingar sem notaðar eru til að búa til mynd:

- **Breidd** - Tilgreinið breidd strikamerkis í pixlum. Gildið **0** (núll) þýðir að sjálfgefna breiddin er notuð. Merkingin getur verið breytileg fyrir mismunandi snið.
- **Hæð** - Tilgreinið hæð strikamerkis í pixlum. Gildið **0** (núll) þýðir að sjálfgefna hæðin er notuð. Merkingin getur verið breytileg fyrir mismunandi snið.
- **Spássía** - Tilgreinið stærð á spássíu strikamerkis í pixlum. Spássían er svæðið beggja megin við strikamerkið sem verður að vera autt (autt svæði). Gildið **0** (núll) þýðir að sjálfgefna spássían er notuð. Merkingin getur verið breytileg fyrir mismunandi snið.
- **Úttaksefni** - Stillið gildið á **Já** til að búa til mynd af strikamerki sem inniheldur kóðaðar upplýsingar sem texta. Sjálfgefið gildi er **Nei**.
- **Kóðun** - Tilgreinið stafagerðina sem kóðuð er í strikamerkjamyndinni sem búin er til. Sjálfgefið er að nota kóðunina **UTF-8**.

> [!IMPORTANT]
> Þegar bætt er við nýjum gagnagjafa **Strikamerki** þarf að staðsetja hann undir annarri vöru (gám) sem faldaða einingu.
>
> Þegar gagnagjafinn **Strikamerki** er bundinn við hólfaeiningu í sniði og hólfaeiningin táknar annaðhvort Word-efnisstýringu eða Excel-mynd, er gagnagjafinn sýndur í þeirri bindingu sem virkni sem er með eina færibreytu af gerðinni **Strengur**. Nota verður þessa færibreytu til að tilgreina textann sem umbreyta á í mynd af strikamerki og lesa þegar myndað strikamerki er skannað.

Fyrir frekari upplýsingar um þennan eiginleika skal ljúka dæmunum í þessu efnisatriði.

## <a name="example-generate-a-payment-check-that-contains-a-bar-code-that-encodes-the-payable-amount"></a>Dæmi: Búa til greiðsluávísun sem inniheldur strikamerki sem kóðar ógreiddu upphæðina

Þetta dæmi sýnir hvernig notandi í hlutverkinu **Kerfisstjóri** eða **Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar** getur stillt snið rafrænnar skýrslugerðar sem inniheldur sniðmát sem er notað til að búa til skjal á útleið á Excel-sniði sem inniheldur strikamerki. Hér er yfirlit yfir skrefin sem eiga við.

1. [Ljúka skilyrðum](#ExamplePrerequisites).
2. [Virkja skilgreiningarveitu](#ExampleProvider).
3. [Flytja inn uppgefna lausn rafrænnar skýrslugerðar](#ExampleImportSolution).
4. [Búa til greiðsluávísun](#ExampleGenerateCheque).
5. [Yfirfara myndaða greiðsluávísun](#ExampleReviewGeneratedCheque).
6. [Breyta sniði á uppgefinni lausn rafrænnar skýrslugerðar](#ExampleModifyFormat).

    1. [Nota nýtt sniðmát ávísunar](#ExampleModifyFormatApplyTemplate).
    2. [Bæta við nýjum gagnagjafa strikamerkis](#ExampleModifyFormatAddDataSource).
    3. [Binda nýja sniðseiningu](#ExampleModifyFormatBindFormatElement).
    4. [Bjóða upp á breyttu útgáfuna fyrir prufukeyrslur](#ExampleModifyFormatMakeVersionAvailable).

        1. [Ljúka við breytt útgáfusnið](#CompleteToRun).
        2. [Bjóða upp á að nota útgáfudrög](#MarkToRun).

7. [Búa til greiðsluávísun](#ExampleGenerateCheque2).
8. [Umbreyta myndaða ávísun í PDF](#ExampleConvertToPDF).

Í þessu dæmi verður notuð uppgefin lausn rafrænnar skýrslugerðar sem hefur verið stillt til að búa til greiðsluávísanir. Þessi lausn býr til greiðsluávísanir þar sem ógreidd upphæð er bæði skrifuð sem tala og texti. Þessari lausn rafrænnar skýrslugerðar verður breytt þannig að ávísunin feli einnig í sér myndað strikamerki þar sem ógreidd upphæð er kóðuð og er hægt að lesa með því að nota strikamerkjaskönnun.

Hægt er að ljúka skrefunum í fyrirtækinu **USMF** í Microsoft Dynamics 365 Finance.

### <a name="complete-the-prerequisites"></a><a name="ExamplePrerequisites"></a>Ljúka skilyrðum

Til að ljúka þessu dæmi verður þú að hafa aðgang að USMF fyrirtæki í Finance fyrir eitt af eftirfarandi hlutverkum:

- Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar
- Kerfisstjóri

Ef ekki hefur enn verið lokið við dæmið í efnisatriðinu [Fella inn myndir og form í skjöl sem búin eru til með því að nota rafræna skýrslugerð](electronic-reporting-embed-images-shapes.md), skal hlaða niður eftirfarandi grunnstillingum sömu lausnar rafrænnar skýrslugerðar.

| Lýsing á efni         | Skrárnafn                   |
|-----------------------------|-----------------------------|
| Skilgreining á gagnalíkani í ER | [Model for cheques.xml](https://download.microsoft.com/download/6/e/a/6ea166fd-1382-4fdb-8dcb-0f13379f9c8e/Modelforcheques.xml)      |
| ER Sníða skilgreiningu     | [Cheques printing format.xml](https://download.microsoft.com/download/1/7/c/17c301e3-c4ee-4886-ae75-440fcc002c8c/Chequesprintingformat.xml) |

Að auki skal hlaða niður eftirfarandi Excel-skrá sem inniheldur breytt sniðmát fyrir uppgefna lausn rafrænnar skýrslugerðar.

| Lýsing á efni | Skrárnafn                 |
|---------------------|---------------------------|
| Skýrslusniðmát     | [Check template Excel.xlsx](https://download.microsoft.com/download/1/f/6/1f671963-73aa-48d5-ae69-45f21fe7dfb4/Cheque%20template.xlsx) |

### <a name="activate-a-configuration-provider"></a><a name="ExampleProvider"></a>Kveikja á stillingaveitu

1. Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
2. Á síðunni **Skilgreiningar staðfærslu**, í hlutanum **Skilgreiningaveitur**, skal ganga úr skugga um að [skilgreiningaveitan](general-electronic-reporting.md#Provider) fyrir sýnifyrirtækið **Litware, Inc.** sé skráð og merkt sem virkt. Ef það er ekki skráð, eða ef það er ekki merkt sem virkt, skal fylgja skrefunum í efnisatriðinu [Stofna skilgreiningaveitu og merkja hana sem virka](tasks/er-configuration-provider-mark-it-active-2016-11.md).

![Sýnifyrirtækið stillt sem virkt á síðunni Skilgreiningar staðfæringar.](./media/er-barcode-data-source-active-provider.png)

### <a name="import-the-provided-er-solution"></a><a name="ExampleImportSolution"></a>Flytja inn uppgefna lausn rafrænnar skýrslugerðar

1. Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
2. Á síðunni **Skilgreiningar skýrslugerðar**, í hlutanum **Skilgreiningar**, skal velja reitinn **Skilgreiningar skýrslugerðar**.
3. Á síðunni **Skilgreiningar**, ef skilgreiningin **Líkan fyrir ávísanir** er ekki tiltæk í skilgreiningartrénu, skal fylgja þessum skrefum til að flytja inn skilgreiningu fyrir gagnalíkan rafrænnar skýrslugerðar:

    1. Í aðgerðarúðunni skal velja **Skipta út** \> **Hlaða úr XML-skrá**.
    2. Í glugganum skal velja **Vafra**, finna og velja skrána **Model for cheques.xml** og síðan velja **Í lagi**.

4. Ef skilgreiningin **Prentsnið ávísunar** er ekki tiltækt í skilgreiningatrénu skal fylgja þessum skrefum til að flytja inn skilgreiningu fyrir snið rafrænnar skýrslugerðar:

    1. Í aðgerðarúðunni skal velja **Skipta út** \> **Hlaða úr XML-skrá**.
    2. Í glugganum skal velja **Vafra**, finna og velja skrána **Cheques printing format.xml** og síðan velja **Í lagi**.

5. Í skilgreiningatrénu skal víkka út **Líkan fyrir ávísanir**.
6. Skoðaðu listann yfir innfluttar ER stillingar í stillingartrénu.

### <a name="generate-a-payment-check"></a><a name="ExampleGenerateCheque"></a>Mynda greiðsluávísun

1. Farið í **Reiðufjár- og bankastjórnun** \> **Bankareikningar** \> **Bankareikningar**.
2. Á síðunni **Bankareikningar** skal velja lykilinn **USMF OPER**.
3. Á upplýsingasíðu bankareiknings, á aðgerðasvæðinu, í flipanum **Setja upp**, í flokknum **Útlit**, skal velja **Ávísun**.
4. Á síðunni **Útlit ávísunar** skal velja **Breyta**.
5. Í flipanum **Almennt** skal stilla valkostinn **Almennt rafrænt útflutningssnið** á **Já**.
6. Í reitnum **Skilgreining útflutningssniðs** skal velja **Prentsnið ávísana** fyrir snið rafrænnar skýrslugerðar sem flutt var inn áður.
7. Á aðgerðasvæðinu skal velja **Prenta sýnishorn**.
8. Í glugganum skal stilla valkostinn **Snið fyrir framseljanlega ávísun** á **Já** og síðan velja **Í lagi**.

    ![Útlit ávísunar - gluggi sýnishornaprentunar.](./media/er-barcode-data-source-check-layout.png)

### <a name="review-the-generated-payment-check"></a><a name="ExampleReviewGeneratedCheque"></a>Yfirfara myndaða greiðsluávísun

- Opnið myndaða ávísun í Excel.
2. Fara yfir myndaða ávísun.

    ![Mynduð greiðsluávísun í Excel.](./media/er-barcode-data-source-cheque1.png)

### <a name="modify-the-format-of-the-provided-er-solution"></a><a name="ExampleModifyFormat"></a>Breyta sniði á uppgefinni lausn rafrænnar skýrslugerðar

#### <a name="apply-a-new-check-template"></a><a name="ExampleModifyFormatApplyTemplate"></a>Nota nýtt sniðmát ávísunar

Hægt er að nota skjáborðsforrit Excel til að opna skrána **Cheque template Excel.xlsx** sem flutt var inn áður. Takið eftir að þetta sniðmát er ólíkt sniðmátinu sem notað var til að mynda greiðsluávísun í uppgefinni lausn rafrænnar skýrslugerðar. Það felur að auki í sér eininguna **AmountBarcode** fyrir mynd af strikamerkinu.

![Eining AmountBarcode í Excel-sniðmátinu.](./media/er-barcode-data-source-cheque2.png)

Nú þarf að breyta lausn rafrænnar skýrslugerðar og síðan [endurnota](modify-electronic-reporting-format-reapply-excel-template.md) breytta sniðmátið.

1. Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
2. Á síðunni **Skilgreiningar skýrslugerðar**, í hlutanum **Skilgreiningar**, skal velja **Skilgreiningar skýrslugerðar**.
3. Á síðunni **Skilgreiningar**, í skilgreiningatrénu, skal stækka **Líkan fyrir ávísanir** og velja **Prentsnið ávísana**.
4. Í aðgerðarúðunni skal velja **Hönnuður**.
5. Í aðgerðarhönnuði rafrænnar skýrslugerðar skal velja flipann **Vörpun** hægra megin á síðunni og síðan á svæði trjásniðs vinstra megin skal velja **Stækka/fella saman**.
6. Takið eftir því að allar einingar hólfasniðs eru bundnar við viðeigandi gagnagjafa.

    ![Binding hólfasniðseininga við gagnagjafa í aðgerðarhönnuði rafrænnar skýrslugerðar.](./media/er-barcode-data-source-cells-bound.png)

7. Veljið flipann **Snið** hægra megin á síðunni.
8. Á aðgerðasvæðinu skal velja úrfellingarmerkið (**...**) og síðan velja **Flytja inn**.
9. Í flokknum **Flytja inn** skal velja **Uppfæra úr Excel** og síðan velja **Uppfæra sniðmát**.
10. Í glugganum skal fara í skrána **Cheque template Excel.xlsx** sem vistuð er í tölvunni, velja hana, og síðan velja **Í lagi** til að staðfesta að nota eigi valið sniðmát.
11. Velja skal flipann **Vörpun** hægra megin á síðunni og síðan á svæði trjásniðs vinstra megin skal velja **Stækka/fella saman**.
12. Takið eftir að hólfaeiningunni **AmountBarcode** hefur verið bætt við sniðið. Þessi eining tengist einingunni **AmountBarcode** sem hefur verið bætt við breytt Excel-sniðmát sem staðgengill fyrir strikamerkjamynd.

    ![Hólfaeiningu AmountBarcode bætt við sniðið í aðgerðarhönnuði rafrænnar skýrslugerðar.](./media/er-barcode-data-source-cell-added.png)

#### <a name="add-a-new-barcode-data-source"></a><a name="ExampleModifyFormatAddDataSource"></a>Bæta við nýjum gagnagjafa strikamerkis

Næst þarf að bæta við nýjum gagnagjafa af gerðinni **Strikamerki**.

1. Í aðgerðarhönnuði rafrænnar skýrslugerðar, í flipanum **Vörpun** hægra megin á síðunni, skal velja gagnagjafann **prenta**.
2. Veljið **Bæta við** og síðan, í flokknum **Aðgerðir**, skal velja gagnagjafa af gerðinni **Strikamerki**.

    ![Val á gagnagjafa af gerðinni strikamerki.](./media/er-barcode-data-source-add.png)

3. Í glugganum, í reitnum **Heiti**, skal slá inn **strikamerki**.
4. Í **Snið strikamerkis** skal velja **Kóði 128**.
5. Í reitinn **Breidd** skal slá inn **500**.
6. Veldu **Í lagi**.

    ![Svargluggi fyrir eiginleika gagnagjafa.](./media/er-barcode-data-source-add2.png)

#### <a name="bind-a-new-format-element"></a><a name="ExampleModifyFormatBindFormatElement"></a>Binda nýja sniðseiningu

Næst þarf að binda nýju sniðseininguna við gagnagjafann sem var verið að bæta við.

1. Í aðgerðarhönnuði rafrænnar skýrslugerðar, í flipanum **Vörpun** hægra megin á síðunni, skal velja gagnagjafann **prenta\\strikamerki**.
2. Vinstra megin á svæði trjásniðs skal velja hólfaeininguna **AmountBarcode** og síðan velja **Binda**.
3. Á aðgerðasvæðinu skal velja **Sýna upplýsingar**.
4. Takið eftir að sökum þess að gagnagjafinn **Strikamerki** er táknaður í bindingunni sem virkni sem inniheldur eina færibreytu, hefur heiti bundnu sniðseiningarinnar sjálfkrafa verið valið sem frumbreyta færibreytunnar.

    ![Upplýsingar um gagnagjafa strikamerkis í aðgerðarhönnuði rafrænnar skýrslugerðar.](./media/er-barcode-data-source-bind1.png)

5. Veljið **Breyta formúlu** til að breyta bindingunni.

    Þú vilt ekki að heiti hólfaeiningarinnar verði skilað til baka. Því verður að skilgreina segð sem skilar texta sem inniheldur ógreidda upphæð á núverandi ávísun. Vegna þess að yfirsviðið **ChequeLines** er bundið við gagnagjafann **model.cheques**, er ógreidd upphæð núverandi ávísunar tiltæk í reitnum **model.cheques.attributes.amount** af gagnagerðinni **Raungildi**.

6. Í reitinn **Formúla** skal færa inn **print.barcode(NUMBERFORMAT(@.attribute.amount, „F2“))**.
7. Veljið **Vista** og lokið síðan [Aðgerðarhönnuði rafrænnar skýrslugerðar](general-electronic-reporting-formula-designer.md).
8. Takið eftir að bindingunni hefur verið breytt.

    ![Leiðrétt binding í aðgerðarhönnuði rafrænnar skýrslugerðar.](./media/er-barcode-data-source-bind2.png)

9. Veljið **Vista** og lokið síðan aðgerðarhönnuði rafrænnar skýrslugerðar.

#### <a name="make-the-modified-version-available-for-test-runs"></a><a name="ExampleModifyFormatMakeVersionAvailable"></a>Bjóða upp á breyttu útgáfuna fyrir prufukeyrslur

Sjálfgefið er að einu útgáfurnar sem eru með stöðuna **Lokið** og **Samnýtt** eru notaðar þegar snið rafrænnar skýrslugerðar er keyrt.

Ef breytingarnar hafa verið fullkláraðar er hægt að ljúka vinnunni með núverandi útgáfudrögum og gert breytingarnar tilbúnar til notkunar. Fyrir leiðbeiningar skal skoða hlutann [Ljúka við breytt útgáfusnið](#CompleteToRun) sem fylgir á eftir.

Ef halda á áfram að vinna með núverandi útgáfudrög, en nota þarf þau til að mynda ávísanir, þarf sérstaklega að taka fram að óskað sé eftir því að nota útgáfudrög sniðsins fyrir keyrslu. Fyrir leiðbeiningar skal skoða hlutann [Bjóða upp á að nota útgáfudrög](#MarkToRun).

##### <a name="complete-the-modified-format-version"></a><a name="CompleteToRun"></a>Ljúka við breytt útgáfusnið

1. Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
2. Á síðunni **Skilgreiningar skýrslugerðar**, í hlutanum **Skilgreiningar**, skal velja **Skilgreiningar skýrslugerðar**.
3. Á síðunni **Skilgreiningar**, í skilgreiningatrénu, skal stækka **Líkan fyrir ávísanir** og velja **Prentsnið ávísana**.
4. Í flýtiflipanum **Útgáfur** skal velja færsluna sem er með stöðuna **Drög**.
5. Veljið **Breyta stöðu** og veljið síðan **Ljúka**.
6. Í svarglugganum skal velja **Í lagi**.

Staða núverandi útgáfu er breytt úr **Drög** í **Lokið** og ný útgáfa með stöðuna **Drög** er búin til. Hægt er að nota þessi nýju útgáfudrög til að gera fleiri breytingar.

##### <a name="make-the-draft-version-available-for-use"></a><a name="MarkToRun"></a>Bjóða upp á að nota útgáfudrög

1. Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
2. Á síðunni **Skilgreiningar skýrslugerðar**, í hlutanum **Skilgreiningar**, skal velja **Skilgreiningar skýrslugerðar**.
3. Á síðunni **Skilgreiningar**, í aðgerðarúðunni, á flipanum **Skilgreiningar**, í flokknum **Ítarlegar stillingar**, skal velja **Færibreytur notanda**.
4. Í glugganum skal stilla valkostinn **Keyra stillingu** á **Já** og síðan velja **Í lagi**.
5. Í skilgreiningatrénu skal stækka **Líkan fyrir ávísanir** og velja **Prentsnið ávísana**.
6. Stillið valkostinn **Keyra drög** á **Já**.
7. Veljið **Vista**.

Útgáfudrög valins sniðmáts eru merkt sem tilbúin til notkunar þegar valið snið er keyrt.

### <a name="generate-a-payment-check"></a><a name="ExampleGenerateCheque2"></a>Mynda greiðsluávísun

1. Farið í **Reiðufjár- og bankastjórnun** \> **Bankareikningar** \> **Bankareikningar**.
2. Á síðunni **Bankareikningar** skal velja lykilinn **USMF OPER**.
3. Á upplýsingasíðu bankareiknings, á aðgerðasvæðinu, í flipanum **Setja upp**, í flokknum **Útlit**, skal velja **Ávísun**.
4. Á síðunni **Útlit ávísunar**, á aðgerðasvæðinu, skal velja **Prenta sýnishorn**.
5. Í glugganum skal stilla valkostinn **Snið fyrir framseljanlega ávísun** á **Já**.
6. Veljið **Í lagi**.
7. Fara yfir myndaða ávísun. Takið eftir að strikamerki hefur verið myndað til að kóða ógreidda upphæð ávísunarinnar.

    ![Mynduð greiðsluávísun með strikamerki í Excel.](./media/er-barcode-data-source-cheque3.png)

> [!IMPORTANT]
> Undantekningu er beitt ef frumbreyta gagnagjafans **Strikamerki** samræmist ekki viðeigandi kröfum sem eiga við um snið strikamerkis. Til dæmis, þegar kallað er á gagnagjafann **Strikamerki** til að mynda strikamerki [EAN-8](https://wikipedia.org/wiki/EAN-8) fyrir uppgefinn texta, er undantekningu beitt ef lengd textans fyrir yfir sjö stafi.

### <a name="convert-the-generated-check-to-a-pdf"></a><a name="ExampleConvertToPDF"></a>Umbreyta myndaða ávísun í PDF

Eins og lýst er í efnisatriðinu [Mynda prentvæn reikningssnið með frjálsum texta](er-generate-printable-fti-forms.md#finland), er hægt að nota sérstakt letur til að búa til strikamerki í skjali sem búið er til. Í slíku tilfelli gætu aukalegar umbreytingar á mynduðu skjali verið háðar því að letrið sé tiltækt í umhverfi umbreytingarinnar. Ef til dæmis er reynt að umbreyta skjali á PDF-snið eða forskoða það í umhverfi þar sem letrið er ekki til staðar, verða strikamerki ekki myndþýdd á réttan hátt.

Þegar gagnagjafinn **Strikamerki** er hins vegar notaður til að búa til strikamerki eru myndþýðingar þessara strikamerkja ekki háðar neinu letri. Þar af leiðandi er auðveldlega hægt að umbreyta skjali sem inniheldur strikamerkin yfir á PDF-snið. Eftirfarandi skýringarmynd sýnir forskoðun á myndaðri greiðsluávísun sem hefur verið [umbreytt](electronic-reporting-destinations.md#OutputConversionToPDF) í PDF, samkvæmt stillingunni á skilgreindri [staðsetningu](electronic-reporting-destinations.md) rafrænnar skýrslugerðar.

![Forskoðun á PDF-skjali greiðsluávísunar.](./media/er-barcode-data-source-cheque4.png)

## <a name="limitations"></a>Takmarkanir

> [!NOTE]
> Sumar gerðir strikamerkis sem eru myndaðar eru með fast myndhlutfall. Þessi hegðun er skiljanleg ef kveikt hefur verið á eiginleikanum **Virkja notkun á EPPlus-safni í rafrænum skýrslugerðarramma** til að vinna með Excel-skjöl í rafrænni skýrslugerð. Í slíku tilfelli er mynd færð inn í staðgengil sem er með læst myndhlutfall. Þar af leiðir að þegar stærðir staðgengils í sniðmáti eru í samræmi við hlutfall myndar sem færð er inn, getur verið að stærð raunverulegrar myndar í mynduðu skjali verði breytt til að viðhalda nauðsynlegu myndhlutfalli. Til að koma í veg fyrir að stærð myndar verði breytt skal nota staðgengil sem er með væntanlegu myndhlutfalli.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Yfirlit yfir rafræna skýrslugerð](general-electronic-reporting.md)
- [Viðtökustaðir rafrænnar skýrslugerðar](electronic-reporting-destinations.md)
- [Formúlutungumál í rafrænni skýrslugerð](er-formula-language.md)
- [Virkni NUMBERFORMAT](er-functions-text-numberformat.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
