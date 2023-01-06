---
title: Frumstæðar gagnagerðir studdar fyrir formúlur rafrænnar skýrslugerðar
description: Í þessari grein er að finna upplýsingar um frumstæðar gagnagerðir sem eru studdar í formúlum rafrænnar skýrslugerðar.
author: kfend
ms.date: 06/02/2021
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 26c166744e1705baa9dcce6b93c76f110524b7d7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9284575"
---
# <a name="supported-primitive-data-types-for-electronic-reporting-formulas"></a>Frumstæðar gagnagerðir studdar fyrir formúlur rafrænnar skýrslugerðar

[!include [banner](../includes/banner.md)]

Í þessari grein er að finna upplýsingar um frumstæðar gagnagerðir sem eru studdar í segðum [Rafrænnar skýrslugerðar](general-electronic-reporting.md). Hér er listi yfir frumstæðar gagnagerðir:

- [boole](#boolean)
- [dagsetning](#date)
- [datetime](#datetime)
- [fasttexti](#enumeration)
- [guid](#guid)
- [heiltala](#integer)
- [int64](#int64)
- [rauntala](#real)
- [strengur](#string)

## <a name="boolean"></a><a name="boolean"></a>Boole

Frumstæða gagnagerðin *boole* inniheldur gildi sem er annaðhvort metið sem *satt* eða *ósatt*. Hægt er að nota frátekin lesgildi leitarorðanna **Satt** og **Ósatt** hvar sem búast má við *boole* segð. Sjálfgefið gildi er *rangt*.

Innri framsetning á *boole* er *heiltala*. *Heiltölugildið* 0 (núll) er metið sem *ósatt* og öll önnur *heiltölugildi* eru metin sem *sönn*. Þegar skilgreind segð er [staðfest](general-electronic-reporting-formula-designer.md#TestFormula) sem skilar *boole* í [Formúluhönnuði rafrænnar skýrslugerðar](er-advanced-formula-editor.md), birtir gluggi prófunarniðurstöðu *0* (núll) þegar segð skilar *ósatt*. Annars birtir gluggi prófunarniðurstöðu *1*.

*Boole* hefur enga óbeina umreikninga. Hins vegar er hægt að nota aðgerðina [TEXT](er-functions-text-text.md) til að breyta *boole* í *streng*:

- Gildinu *ósatt* er umbreytt í textastrenginn **Ósatt**.
- Gildinu *satt* er umbreytt í textastrenginn **Satt**.

> [!NOTE]
> Þessi umbreyting fer ekki eftir [samhengi](er-design-multilingual-reports.md) tungumáls og menningar sem gefið er upp.

[Samanburðarvirknitákn](er-formula-language.md#Operators) eru einu gerðir virknitákna sem hægt er að nota með gagnagerðinni *boole*. Hægt er að nota eftirfarandi virknitákn til að bera saman tvö *boole-gildi*: \<\> og =.

## <a name="date"></a><a name="date"></a>Dagsetning

Frumstæða gagnagerðin *dagsetning* inniheldur dag, mánuð og ár. Hægt er að hefja dagsetningar með eftirfarandi aðgerðum:

- [DATEVALUE](er-functions-datetime-datevalue.md)
- [NULLDATE](er-functions-datetime-nulldate.md)
- [SESSIONTODAY](er-functions-datetime-sessiontoday.md)
- [Í DAG](er-functions-datetime-today.md)

Gagnagerðin *dagsetning* getur haldið dagsetningum milli 1. janúar 1900 og 31. desember 2154. Sjálfgefna gildið er **núll** og innri framsetningin er dagsetningin 1. janúar 1900.

*Dagsetning* hefur engar óbeina umreikninga. Hins vegar er hægt að nota eftirfarandi beinar aðgerðir umbreytingar:

- [DATEFORMAT](er-functions-datetime-dateformat.md)
- [DATETODATETIME](er-functions-datetime-datetodatetime.md)
- [TEXTI](er-functions-text-text.md)

Aðgerðin [ADDDAYS](er-functions-datetime-adddays.md) gerir mögulegt að bæta við og draga daga frá dagsetningum. Á þennan hátt er hægt að færa dagsetninguna um ákveðinn fjölda daga inn í framtíðina og aftur í fortíðina. Aðgerðin [DAYS](er-functions-datetime-days.md) gerir kleift að draga dagsetningar hvor frá annarri og reikna mismuninn í dögum. Nánari upplýsingar um breytingu á *dagsetningargildum* er að finna í [Listi yfir aðgerðir rafrænnar skýrslugerðar í flokki dagsetningar og tíma](er-functions-category-datetime.md).

[Samanburðarvirknitákn](er-formula-language.md#Operators) eru einu gerðir virknitákna sem hægt er að nota með gagnagerðinni *dagsetning*. Hægt er að nota eftirfarandi virknitákn til að bera saman tvö gildi *dagsetningar*: \<\>, \<, \<=, =, \> og \>=.

## <a name="datetime"></a><a name="datetime"></a>Datetime

Frumstæða gagnagerðin *datetime* sameinar gildið *dagsetning* og gildi sem stendur fyrir tíma sem hefur liðið frá miðnætti. Tíminn er gefinn upp í klukkustundum, mínútum, sekúndum og sekúndubrotum. Gildi *datetime* inniheldur einnig upplýsingar um tímabeltið.

Gagnagerðin *datetime* getur innihaldið dagsetningar á bilinu 1. janúar 1900 (1900-01-01T00:00:00.0000000+00:00 á tvíhverfa [sniðinu](/dotnet/standard/base-types/standard-date-and-time-format-strings)) og 31. desember 2154 (2154/12/31T11:59:59.9999999+00:00 á tvíhverfu sniði). Minnsta tímaeiningin í *datetime* er tíu milljónasti úr sekúndu.

> [!NOTE]
> Þegar **hh** [stillirinn](/dotnet/standard/base-types/standard-date-and-time-format-strings) er notaður fyrir klukkustundir er ekki hægt að túlka tímagildi yfir 12:59:59:9999999 sem gilda tíma.
>
> Þegar **HH** stillirinn er notaður fyrir klukkustundir er ekki hægt að túlka tímagildi yfir 23:59:59:9999999 sem gilda tíma.

Sjálfgefna gildið er **núll** og innri framsetningin er dagsetningin 1. janúar 1900 (1900-01-01T00:00:00.0000000+00:00 á tvíhverfu sniði).

Hægt er að hefja datetimes með eftirfarandi aðgerðum:

- [DATETIMEVALUE](er-functions-datetime-datetimevalue.md)
- [NULNULLDATETIMELDATE](er-functions-datetime-nulldatetime.md)
- [SESSIONNOW](er-functions-datetime-sessionnow.md)
- [NÚNA](er-functions-datetime-now.md)

*Datetime* hefur enga óbeina umreikninga. Hins vegar er hægt að nota eftirfarandi beinar aðgerðir umbreytingar:

- [DATETIMEFORMAT](er-functions-datetime-datetimeformat.md)
- [TEXTI](er-functions-text-text.md)

Nánari upplýsingar um breytingu á *datetime* er að finna í [Listi yfir aðgerðir rafrænnar skýrslugerðar í flokki dagsetningar og tíma](er-functions-category-datetime.md).

[Samanburðarvirknitákn](er-formula-language.md#Operators) eru einu gerðir virknitákna sem hægt er að nota með gagnagerðinni *datetime*. Hægt er að nota eftirfarandi virknitákn til að bera saman tvö gildi *datetime*: \<\>, \<, \<=, =, \> og \>=.

## <a name="enumeration"></a><a name="enumeration"></a>Tölusetning

Frumstæða gagnagerðin *fasttexti* er listi yfir lesgildi. Hægt er að nota fasttexta sem eru skilgreindir í forritinu [upprunakóði](../dev-ref/xpp-data-primitive.md#enum). Einnig er hægt að kynna eigin fasttexta í gagnalíkani rafrænnar skýrslugerðar og sniðshlutum rafrænnar skýrslugerðar.

Hægt er að nota *fasttexta* forrits í segðum af hvaða líkanavörpun og sniði sem er í rafrænni skýrslugerð.

Eftirfarandi mynd sýnir hvernig hægt er að bæta fasttextalíkaninu **CustVendCorrectiveReasonCode** við breytanlegt gagnalíkan rafrænnar skýrslugerðar.

[![Fasttextalíkan skilgreint í hönnuði gagnalíkans rafrænnar skýrslugerðar.](./media/er-formula-supported-data-types-primitive-enum1.gif)](./media/er-formula-supported-data-types-primitive-enum1.gif)

Hægt er að nota *fasttextalíkan* í segðum í hvaða líkanavörpun og sniði sem er í rafrænni skýrslugerð sem voru búnar til undir gagnalíkani þar sem *fasttextinn* var kynntur.

Eftirfarandi mynd sýnir hvernig hægt er að bæta fasttextasniðinu **Listi yfir undirflokka á bakfærðu gjaldi Natura** við breytanlegt snið rafrænnar skýrslugerðar.

[![Fasttextasnið skilgreint í sniðshönnuði rafrænnar skýrslugerðar.](./media/er-formula-supported-data-types-primitive-enum2.gif)](./media/er-formula-supported-data-types-primitive-enum2.gif)

Aðeins er hægt að nota *fasttextasnið* í segðum rafræns skýrslugerðarsniðs þar sem *fasttextinn* var kynntur.

Nota þarf viðeigandi gerð af gagnagjöfum rafrænnar skýrslugerðar til að flytja tiltekinn fasttexta til skilgreinds hlutar rafrænnar skýrslugerðar sem fasta eða sem gildi sem notandinn sem keyrir lausn rafrænnar skýrslugerðar sem skilgreind er í svarglugganum við keyrslu.

- Hægt er að nálgast fasttexta forrits með gagnagjöfunum **Dynamics 365 for Operations \ Fasttexti** og **Almennt \ Innsláttarfæribreytur notanda**. Eftirfarandi mynd sýnir hvernig hægt er að bæta við breytanlegt snið rafrænnar skýrslugerðar gagnagjöfunum **appenumNoYes** og **uipNoYes** sem vísa til **NoYes** fasttexta forrits.

    [![Gagnagjöfum fasttexta forrits bætt við í sniðshönnuði rafrænnar skýrslugerðar.](./media/er-formula-supported-data-types-primitive-enum3a.gif)](./media/er-formula-supported-data-types-primitive-enum3a.gif)

- Hægt er að nálgast fasttexta gagnagjafa með því að nota gagnagjafana **Gagnalíkan \ Fasttexti** og **Gagnalíkan \ Innsláttarfæribreytur notanda fasttexta**. Eftirfarandi mynd sýnir hvernig hægt er að bæta við breytanlegt snið rafrænnar skýrslugerðar gagnagjafanum **CustVendCorrectiveReasonCode** sem vísar til **CustVendCorrectiveReasonCode** fasttexta forrits.

    [![Gagnagjöfum fasttexta líkans bætt við í sniðshönnuði rafrænnar skýrslugerðar.](./media/er-formula-supported-data-types-primitive-enum3b.gif)](./media/er-formula-supported-data-types-primitive-enum3b.gif)

- Hægt er að nálgast fasttextasnið með því að nota gagnagjafana **Snið \ Fasttexti** og **Snið \ Innsláttarfæribreytur notanda fasttexta**. Eftirfarandi mynd sýnir hvernig hægt er að bæta við breytanlegt snið rafrænnar skýrslugerðar gagnagjafanum **NaturaReverseCharge** sem vísar til **Undirflokka bakfærðs gjalds Natura** fasttextasniðs.

    [![Gagnagjöfum fasttextasniðs bætt við í sniðshönnuði rafrænnar skýrslugerðar.](./media/er-formula-supported-data-types-primitive-enum3c.gif)](./media/er-formula-supported-data-types-primitive-enum3c.gif)

*Fasttexti* hefur engar óbeina umreikninga. Hins vegar er hægt að nota umbreytingaraðgerðina [TEXT](er-functions-text-text.md) til að umbreyta *fasttexta* í textastreng. Þessi umbreyting er ekki háð tungumáli. Til að komast að því hvernig á að tengja gildi *fasttexta* við viðeigandi merki ákveðins tungumáls skal skoða dæmin um notkun á aðgerðunum [LISTOFFIELDS](er-functions-list-listoffields.md) and [GETENUMVALUEBYNAME](er-functions-text-getenumvaluebyname.md).

[Samanburðarvirknitákn](er-formula-language.md#Operators) er eina gerð virknitákna sem hægt er að nota með gagnagerðinni *fasttexti*. Hægt er að nota eftirfarandi virknitákn til að bera saman tvö gildi *fasttexta*: \<\> og =.

## <a name="guid"></a><a name="guid"></a>Guid

Frumstæða gagnagerðin *guid* geymir gildi fyrir altækt einkvæmt kennimerki (GUID). GUID er gildi sem hægt er að nota í öllum tölvum og netkerfum þar sem einkvæmt kennimerki er nauðsynlegt. Ólíklegt er að númerið verði tvítekið. Gilt GUID uppfyllir öll eftirfarandi skilyrði:

- Það verða að vera 32 tölustafir í sextándakerfi.
- Auk þess verða að vera fjögur bandstrik sem eru felld inn á eftirfarandi staðsetningar: 8-4-4-4-12.
- Auk þess er valfrjálst að bæta við slaufusviga \{\} í upphafi og lok strengs. Til dæmis eru bæði **\{2CDB0FE7-D7B3-4938-A0F0-FE28FB8FE212\}** og **2CDB0FE7-D7B3-4938-A0F0-FE28FB8FE212** gildir GUID-strengir.
- Því verða að vera samtals 36 eða 38 stafir eftir því hvort slaufusvigum er bætt við.
- Stafirnir sem notaðir eru sem tölustafir í sextándakerfi geta verið hástafir (A-F), lágstafir (a-f) eða blandað.

Eftirfarandi beinar aðgerðir umbreytinga er hægt að nota:

- [GUIDVALUE](er-functions-text-guidvalue.md)
- [TEXTI](er-functions-text-text.md)

[Samanburðarvirknitákn](er-formula-language.md#Operators) er eina gerð virknitákna sem hægt er að nota með gagnagerðinni *guid*. Hægt er að nota eftirfarandi virknitákn til að bera saman tvö gildi *guid*: \<\> og =.

## <a name="integer"></a><a name="integer"></a>Heiltala

Frumstæða gagnagerðin *heiltala* stendur fyrir tölu með engum aukastöfum. Heiltölur eru notaðar sem stýribreytur í endurteknum setningum eða sem vísar í færslulistum.

*Heiltölulesgildi* er heiltalan eins og hún er færð beint inn í [segð](general-electronic-reporting-formula-designer.md#formula-designer-overview) (formúlu) rafrænnar skýrslugerðar eins og **12345**. *Heiltala* er 32-bita breið. Sjálfgefið gildi er **0** og innri framsetningin er löng tala. *Heiltölu* er sjálfkrafa breytt í *raunverulega* tölu.

Auk þess er hægt að nota eftirfarandi beinar aðgerðir umbreytinga:

- [INTVALUE](er-functions-conversion-intvalue.md)
- [NUMBERFORMAT](er-functions-text-numberformat.md)
- [TEXTI](er-functions-text-text.md)

Svið *heiltölu* er \[-2.147.483.647 : 2.147.483.647\]. Hægt er að nota allar heiltölur á þessu sviði sem lesgildi.

Hægt er að nota öll [samanburðarvirknitákn og stærðfræðileg virknitákn](er-formula-language.md#Operators) með gagnagerð *heiltölu*.

## <a name="int64"></a><a name="int64"></a>Int64

Frumstæða gagnagerðin *int64* stendur fyrir tölu með engum aukastöfum. *Int64* gildi eru notuð sem stýribreytur í endurteknum setningum eða sem auðkenningu færslu.

*int64* er 64-bita breið. Sjálfgefið gildi er **0** og innri framsetningin er löng tala. *Int64* er sjálfkrafa breytt í *raunverulega* tölu.

Auk þess er hægt að nota eftirfarandi beinar aðgerðir umbreytinga:

- [INT64VALUE](er-functions-conversion-int64value.md)
- [NUMBERFORMAT](er-functions-text-numberformat.md)
- [TEXTI](er-functions-text-text.md)

Svið *int64* er \[-9,223,372,036,854,775,807 : 9,223,372,036,854,775,807\].

Hægt er að nota öll [samanburðarvirknitákn og stærðfræðileg virknitákn](er-formula-language.md#Operators) með gagnagerð *int64*.

## <a name="real"></a><a name="real"></a>Rauntala

Frumstæð gagnagerð *Rauntölu* getur verið með tugabrot ásamt heiltölum. Hægt er að nota lesgildi tugabrota hvar sem búast má við *raunverulegri tölu*. Lesgildi tugabrots er þess vegna tugabrot þar sem það er slegið beint inn í kóða á borð við **2.19**.

> [!NOTE]
> Í segðum rafrænnar skýrslugerðar er punktur (.) alltaf notaður sem skiltákn tugabrots.

Hægt er að nota raunverulegar tölur í öllum segðum og nota þær með bæði samanburðarvirknitáknum og reikningsvirknitáknum. *Rauntala* er með nákvæmni upp á 16 marktæka tölustafi. Sjálfgefið gildi fyrir *rauntölu* er **0,0** og innri framsetningin er tvíundarkóðuð stafræn tala (BCD). BCD-kóðun gerir nákvæmar framsetningar á gildum sem eru margfeldi af 0,1. Svið *rauntölubreytu* er -(10)<sup>127</sup> í gegnum (10)<sup>127</sup>. Hægt er að nota allar rauntölur á þessu sviði sem lesgildi í segðum rafrænnar skýrslugerðar.

*Rauntala* hefur engar óbeina umreikninga. Hins vegar er hægt að nota eftirfarandi aðgerðir til að breyta *rauntölu* í aðrar gagnagerðir og aðrar gagnagerðir í *rauntölu*:

- [INTVALUE](er-functions-conversion-intvalue.md)
- [INT64VALUE](er-functions-conversion-int64value.md)
- [NUMBERFORMAT](er-functions-text-numberformat.md)
- [TEXTI](er-functions-text-text.md)
- [GILDI](er-functions-conversion-value.md)

Hægt er að nota öll [samanburðarvirknitákn og stærðfræðileg virknitákn](er-formula-language.md#Operators) með gagnagerð *Rauntölu*.

## <a name="string"></a><a name="string"></a>Strengur

Frumstæð gagnagerð *strengs* stendur fyrir röð bókstafa sem er notuð sem textar, lykilnúmer, heimilisföng og símanúmer.

Lesgildi *strengja* eru stafir innan gæsalappa („“). Nota má lesgildi *strengs* þar sem búist er við gildum *strengs* í segðum rafrænnar skýrslugerðar. Hægt er að nota strengi í röksegðum á borð við samanburði. Einnig er hægt að sameina gildi *strengja* með virknitákninu **\&** eða aðgerðinni [CONCATENAT](er-functions-text-concatenate.md).

> [!NOTE]
> Ef þú sameinar tvö *strengjagildi* og vilt að *strengurinn* nái yfir fleiri en eina línu skaltu nota línuskiltáknið á milli gildanna. Fyrir úttak TEXT getur þetta skiltákn verið stafur sem er búinn til með því að nota [CHAR](er-functions-text-char.md)(10) eða CHAR(13) segðina. Fyrir HTML getur það verið **\<br\>** merkið.

Sjálfgefið gildi fyrir *streng* er auður textastrengur með engum stöfum og innri framsetningin er listi yfir stafi.

Ekki eru neinar sjálfvirkar umbreytingar fyrir strengi. Hins vegar er hægt að nota eftirtaldar beinar aðgerðir umbreytinga:

- [CHAR](er-functions-text-char.md)
- [SNIÐ](er-functions-text-format.md)
- [VINSTRI](er-functions-text-left.md)
- [LEN](er-functions-text-len.md)
- [MIÐ](er-functions-text-mid.md)
- [PADLEFT](er-functions-text-padleft.md)
- [SKIPTA UM](er-functions-text-replace.md)
- [HÆGRI](er-functions-text-right.md)
- [TEXTI](er-functions-text-text.md)
- [TRANSLATE](er-functions-text-translate.md)
- [KLIPPA](er-functions-text-trim.md)
- [EFRA](er-functions-text-upper.md)

Til að sjá meira um umbreytingu á gildum *strengja* skal skoða [Listi yfir aðgerðir rafrænnar skýrslugerðar í textaflokknum](er-functions-category-text.md).

*Strengur* getur geymt ótilgreindan fjölda stafa.

Hægt er að nota öll [samanburðarvirknitákn](er-formula-language.md#Operators) með gagnagerð *strengs*.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Yfirlit yfir rafræna skýrslugerð](general-electronic-reporting.md)
- [Formúlutungumál í rafrænni skýrslugerð](er-formula-language.md)
- [Studdar samsettar gagnagerðir](er-formula-supported-data-types-composite.md)
