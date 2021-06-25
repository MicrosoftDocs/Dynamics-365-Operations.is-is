---
title: Formúlutungumál í rafrænni skýrslugerð
description: Þetta efni inniheldur upplýsingar um hvernig á að nota formúlutungumálið í rafrænni skýrslugerð (ER).
author: NickSelin
ms.date: 05/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 470b4fa1c8b15ae4a9e9ebef81af9e4ca107422d
ms.sourcegitcommit: 15aacd0e109b05c7281407b5bba4e6cd99116c28
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/10/2021
ms.locfileid: "6223987"
---
# <a name="electronic-reporting-formula-language"></a>Formúlutungumál í rafrænni skýrslugerð

[!include [banner](../includes/banner.md)]

Rafræn skýrslugerð (ER) veitir öfluga upplifun gagnabreytinga. Tungumálið sem er notað til að sýna nauðsynlegar gagnaframkvæmdir í [formúluhönnuði rafrænnar skýrslugerðar](general-electronic-reporting-formula-designer.md) líkist formúlutungumálinu í Microsoft Excel.

## <a name="basic-syntax"></a>Grunnmálskipan

Segðir rafrænnar skýrslugerðar geta innihaldið hverja sem er eða allar af eftirfarandi einingar:

- [Fastagildi](#Constants)
- [Stjórnendur](#Operators)
- [Tilvísanir](#References)
- [Slóðir](#Paths)
- [Aðgerðir](#Functions)

## <a name="constants"></a><a name="Constants"></a>Fastagildi

Þegar þú hannar segð getur þú notað texta og tölfræðilega fasta (það er gildi sem ekki er reiknað út). Til dæmis, tölulegt fastagildi `VALUE ("100") + 20` notar tölulegt fastagildið **20** og fastagildi strengs **"100"** og skilar tölulegu gildi **120**.

Formúluhönnuður rafrænnar skýrslugerðar styður lausnarrunur. Þess vegna er hægt að tilgreina segðarstreng sem ætti að meðhöndla á annan hátt. Til dæmis skilar segðin `"Leo Tolstoy ""War and Peace"" Volume 1"` textastrengnum **Leo Tolstoy „Stríð og friður“ 1. bindi**.

## <a name="operators"></a><a name="Operators"></a>Virknitákn

Eftirfarandi tafla sýnir reikniaðgerðir sem þú getur notað til að gera grunn stærðfræðilegar aðgerðir, svo sem viðbót, frádráttur, margföldun og deiling.

| Notandi | Merking               | Dæmi     |
|----------|-----------------------|-------------|
| +        | samlagning              | `1+2`       |
| -        | Frádráttur Neitun | `5-2`, `-1` |
| \*       | Margföldun        | `7\*8`      |
| /        | Skipting              | `9/3`       |

Eftirfarandi tafla sýnir samanburðaraðgerðir sem eru studdar. Þú getur notað þessar aðgerðir til að bera saman tvö gildi.

| Notandi | Merking                  | Dæmi      |
|----------|--------------------------|--------------|
| =        | Jafnt                    | `X=Y`        |
| &gt;     | Stærra en             | `X>Y`        |
| &lt;     | Minna en                | `X<Y`        |
| &gt;=    | Stærra en eða jafnt og | `X>=Y`       |
| &lt;=    | Minna en eða jafnt og    | `X<=Y`       |
| &lt;&gt; | Er ekki jafnt og             | `X<>Y`       |

Að auki er hægt að nota ampersand (&) sem textasambandsaðgerð. Þannig geturðu sameinað eða tengt saman einn eða fleiri textastrengi sem einn texta.

| Notandi | Merking     | Dæmi                                               |
|----------|-------------|-------------------------------------------------------|
| &        | Samtengja | `"Nothing to print:" & " " & "no records found"`      |

### <a name="operator-precedence"></a>Forgangsröðun stjórnanda

Röðin sem hlutar samsettrar segðar eru metnir í er mikilvæg. Til dæmis er niðurstaða segðarinnar `1 + 4 / 2` breytileg eftir því hvort samlagningar- eða deilingaraðgerð er fyrst framkvæmd. Hægt er að nota sviga til að skilgreina sérstaklega hvernig segð er metin. Til dæmis, til að gefa til kynna að samlagningaraðgerðin skuli gerð fyrst, getur þú breytt fyrri segðinni í `(1 + 4) / 2`. Ef þú gefur ekki skýrt til kynna röð aðgerða í segð er röðin byggð á sjálfgefna forgangi sem er úthlutað til undiraðgerðanna. Eftirfarandi tafla sýnir forgang sem er úthlutað hverri aðgerð. Aðgerðir sem hafa meiri forgang (til dæmis 7) eru metnir á undan aðgerðum sem hafa lægri forgang (til dæmis 1).

| Forgangur | Stjórnendur      | Málskipun                                                                  |
|------------|----------------|-------------------------------------------------------------------------|
| 7          | Flokkun       | ( … )                                                                   |
| 6          | Aðgangur meðlima  | … . …                                                                   |
| 5          | Aðgerðakall  | … ( … )                                                                 |
| 4          | Margfaldandi | … \* …<br>… / …                                                         |
| 3          | Viðbótarefni       | … + …<br>… - …                                                          |
| 2          | Samanburður     | … &lt; …<br>… &lt;= …<br>… =&gt; …<br>… &gt; …<br>… = …<br>… &lt;&gt; … |
| 1          | Aðgreining     | … , …                                                                   |

Ef segð felur í sér margar aðgerðir sem hafa sama forgang, eru þessar aðgerðir metnar frá vinstri til hægri. Til dæmis, er segðin `1 + 6 / 2 \* 3 > 5` skilar **satt**. Við mælum með því að þú notar sviga til að tilgreina sérstaklega viðkomandi röð aðgerða í segðum, svo að segðirnar séu auðveldari að lesa og viðhalda.

## <a name="references"></a><a name="References"></a>Tilvísanir

Öll gagnasöfn í núverandi hluta rafrænnar skýrslugerðar sem eru tiltækar við hönnun segðar geta verið notaðir sem tilvísanir með heiti. Núverandi ER íhlutur getur verið annaðhvort líkanavörpun eða sniði. Til dæmis inniheldur núverandi líkanavörpun rafrænnar skýrslugerðar **ReportingDate** gagnagjafann, sem skilar gildi gagnagerðarinnar [*DateTime*](er-formula-supported-data-types-primitive.md#datetime). Til að forsníða þetta gildi á réttan hátt í skjalinu sem er búið til geturðu vísað til gagnagjafans í segðinni sem `DATETIMEFORMAT (ReportingDate, "dd-MM-yyyy")`.

Allir stafir í heiti á tilvísandi gagnagjafa sem ekki tákna staf í stafrófinu skulu hafa einfaldar gæsalappir (') fyrir framan. Ef heitið á tilvísandi gagnagjafa inniheldur að minnsta kosti eitt tákn sem ekki táknar stafina í stafrófinu, skal nafnið vera fyrir innan einfaldra gæsalappa. Til dæmis geta þessi tákn sem eru ekki í stafrófinu verið greinarmerki eða önnur skrifuð tákn. Hér eru nokkur dæmi:

- Gagnagjafinn **Dagsetning og tími í dag** verður að vera vísað í segð rafrænnar skýrslugerðar sem `'Today''s date & time'`.
- Aðferðin **heiti()** fyrir gagnagrunninn **Viðskiptavinir** verður að vera vísað í ER-segð sem `Customers.'name()'`.

Ef aðferðir gagnagjafa forrits hafa breytur er eftirfarandi málskipan notuð til að kalla á þessar aðferðir:

- Ef **isLanguageRTL** aðferðin í gagnagjafa **Kerfisins** hefur **EN-US** færibreytu af gagnagerðinni [*Strengur*](er-formula-supported-data-types-primitive.md#string), þá skal vísa þessari aðferð í segð rafrænnar skýrslugerðar sem `System.isLanguageRTL("EN-US")`.
- Tilvitnunarmerki eru ekki nauðsynleg þegar heiti aðferðar inniheldur aðeins tölustafatákn. Hins vegar er þeirra krafist fyrir töfluaðferð ef nafnið inniheldur sviga.

Þegar gagnagjafanum **Kerfi** er bætt við ER-vörpun sem vísar til forritaflokksins **Altækt** skilar segðin `System.isLanguageRTL("EN-US ")` *Boolean*-gildinu **FALSE**. Hin breytta segð `System.isLanguageRTL("AR")` skilar *Boolean*-gildinu **SATT**.

Þú getur takmarkað hvernig þessi gildi eru samþykkt í breytur fyrir aðferð af þessari gerð:

- Aðeins fastar geta verið notaðir í aðferðum af þessari gerð. Gildi fastanna eru skilgreind á hönnunartíma.
- Aðeins [frumstæðar](er-formula-supported-data-types-primitive.md) (grunn) gagnagerðir eru studdar fyrir breytur af þessu tagi. Frumstæðu gagnagerðirnar eru *heiltala*, *rauntala*, *Boolean* og *strengur*.

## <a name="paths"></a><a name="Paths"></a>Slóðir

Þegar segð vísar í skipulögð gagnagjafa, geturðu nota skilgreiningu slóðar til að velja tiltekna frumstæðar einingu þess gagnagjafa. Stafurinn punktur (.) er notuð til að aðskilja einstakar einingar skipulagðs gagnagjafa. Til dæmis, núverandi ER-líkanavörpun inniheldur **InvoiceTransactions** gagnagjafa og þessi gögn skila lista yfir skrár. Uppsetningin **InvoiceTransactions** inniheldur **AmountDebit** og **AmountCredit** svæðin og bæði svæðin skila tölugildum. Þess vegna getur þú hannað eftirfarandi segð til að reikna út reiknaða upphæð: `InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit`. Skilgreiningin `InvoiceTransactions.AmountDebit` í þessari segð er slóðin sem er notuð til að fá aðgang að reitnum **AmountDebit** í gagnagjafanum **InvoiceTransactions** af gerðinni *Skráalisti*.

### <a name="relative-path"></a>Afstæð slóð

Ef slóð skipulögð gagnaheimild byrjar með „at“ merki (@), þá er það afstæður slóð. Merkið „at“ er sýnt í stað þess hluta sem eftir er af algeru slóð stigveldisins tréskipulags sem er notað. Eftirfarandi skýringarmynd sýnir dæmi. Hér sýnir algilda slóðin `Ledger.'accountingCurrency()'` að gildi bókhaldsgjaldmiðils úr gagnagjafanum **Fjárhagur** er skráð í reitinn **AccountingCurrency** í gagnalíkaninu.

![Dæmi um algilda slóð á hönnuðarsíðu ER-líkanavörpunar](./media/ER-FormulaLanguage-AbsolutePath.png)

Dæmið á eftirfarandi mynd sýnir hvernig tengd slóð er notuð. Tengda slóðin `@.AccountNum` sýnir að reiturinn **AccountNum** í gagnagjafanum **Intrastat** (sem birtist einu stigi fyrir ofan reitinn **AccountNum** í stigveldistré gagnalíkansins) er notaður til að skrá reikningsnúmer viðskiptavinar eða lánardrottins í reitinn **AccountNum** í gagnalíkaninu.

![Dæmi um tengda slóð á hönnuðarsíðu ER-líkanavörpunar](./media/ER-FormulaLanguage-RelativePath1.png)

Það sem eftir er af algildu slóðinni er einnig sýnt í [ER-formúluritill](general-electronic-reporting-formula-designer.md).

![Eftirstandandi hluti af algildu slóðinni á hönnunarsíðu ER-formúlu](./media/ER-FormulaLanguage-RelativePath2.png)

Frekari upplýsingar er að finna í [Nota tengda slóð í gagnabindingu líkana rafrænnar skýrslugerðar](relative-path-data-bindings-er-models-format.md).

## <a name="functions"></a><a name="Functions"></a>Aðgerðir

Innbyggðar aðgerðir ER geta verið notaðar í ER-segðum. Allir gagnagjafar segðarsamhengis (þ.e.a.s., núverandi ER-líkanavörpun eða ER-snið) er hægt að nota sem breytur kallaðgerða, í samræmi við lista yfir frumbreytur fyrir kallaðgerðir. Fastar geta einnig verið notaðir sem breytur kallaðgerða. Til dæmis, núverandi ER-líkanavörpun inniheldur **InvoiceTransactions** gagnagjafa og þessi gögn skila lista yfir skrár. Uppsetningin **InvoiceTransactions** inniheldur **AmountDebit** og **AmountCredit** svæðin og bæði svæðin skila tölugildum. Þar af leiðandi er hægt að hanna tjáningu til að reikna út reikningsfærða upphæð sem notar innbyggða ER-námundunaraðgerð: `ROUND (InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit, 2)`.

Þegar þú hannar ER-líkanavarpanir og ER-skýrslur geturðu notað ER-aðgerðir úr eftirfarandi flokkum:

- [Dagsetningar og tímavirkni](er-functions-category-datetime.md)
- [Listavirkni](er-functions-category-list.md)
- [Rökvirkni](er-functions-category-logical.md)
- [Reikniaðgerðir](er-functions-category-mathematical.md)
- [Færsluvirkni](er-functions-category-record.md)
- [Textavirkni](er-functions-category-text.md)
- [Gagnasöfnunaraðgerðir](er-functions-category-data-collection.md)
- [Other (lénsértæk virkni fyrir viðskipti)](er-functions-category-other.md)
- [Aðgerðir fyrir umbreytingu á gerð](er-functions-category-type-conversion.md)

## <a name="functions-list-extension"></a>Viðbót við lista yfir virkni

Rafræn skýrslugerð styður möguleikann á að útvíkka listann yfir aðgerðir sem eru notaðar í segðir rafrænnar skýrslugerðar. Þetta krefst smá verkfræðikunnáttu. Fyrir ítarlegar upplýsingar sjá [Útvíkka listann fyrir aðgerðir rafrænnar skýrslugerðar (ER)](general-electronic-reporting-formulas-list-extension.md).

## <a name="compound-expressions"></a>Samsettar segðir

Hægter að stofna samsettar segðir sem nota aðgerðir úr mismunandi flokkum, að því tilskildu að gagnagerðirnar stemmi. Þegar þú notar aðgerðir saman skaltu stemma gagnagerð framleiðslunnar frá einni aðgerð við innsláttargagnagerðina sem önnur aðgerð krefst. Til dæmis, til að forðast hugsanlega "list-is-empty" villu í bindingu á reit við ER-sniðmátsþátt skal blanda saman aðgerðum úr flokknum [Listi](er-functions-category-list.md) við aðgerð úr flokknum [Röklegt](er-functions-category-logical.md), eins og eftirfarandi dæmi sýnir. Hér notar formúlan aðgerðina [IF](er-functions-logical-if.md) til að prófa hvort listinn **IntrastatTals** sé tómur áður en hann skilar gildi nauðsynlegrar uppsöfnunar af þeim lista. Ef listinn **IntrastatTotals** er tómur skilar formúlan **0** (núlli).

```vb
IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$AmountMSTRounded') 
```

## <a name="multiple-solutions"></a>Margar lausnir

Oft geturðu fengið sömu gagnaflutninganiðurstöðu á marga vegu með því að nota aðgerðir úr mismunandi flokkum eða mismunandi aðgerðir úr sama flokki. Til dæmis er einnig hægt að stilla fyrri segð með því að nota aðgerðina [COUNT](er-functions-list-count.md) úr flokknum [Listi](er-functions-category-list.md).

```vb
IF(COUNT (IntrastatTotals)=0, 0.0, IntrastatTotals.aggregated.'$AmountMSTRounded') 
```

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir rafræna skýrslugerð](general-electronic-reporting.md)

[Formúluhönnuður í rafrænni skýrslugerð](general-electronic-reporting-formula-designer.md)

[Listi yfir virkni rafrænnar skýrslugerðar lengdur](general-electronic-reporting-formulas-list-extension.md)

[Studdar frumstæðar gagnagerðir](er-formula-supported-data-types-primitive.md)

[Studdar samsettar gagnagerðir](er-formula-supported-data-types-composite.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
