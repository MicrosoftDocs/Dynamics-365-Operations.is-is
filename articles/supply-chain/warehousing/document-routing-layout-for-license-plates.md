---
title: Útlit merkimiða skjalasendinga
description: Þessi grein lýsir því hvernig á að nota sniðsaðferðir til að prenta gildi á merki.
author: perlynne
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLicensePlateLabel, WHSLicensePlateLabelBuildConfig, WHSLicensePlateLabel, WHSDocumentRoutingLayout
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2012-04-01
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: a4e0c16b71c257cae832870ca58679884047ea16
ms.sourcegitcommit: 9e6a9d644a34158390c6e209e80053ccbdb7d974
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/20/2022
ms.locfileid: "9708646"
---
# <a name="document-routing-label-layout"></a>Útlit merkimiða skjalasendinga

[!include [banner](../includes/banner.md)]

Í þessari grein er því lýst hvernig á að búa til útlit fyrir númeraplötu, geyma og bylgjumerki. Þar er einnig að finna leiðbeiningar um notkun Zebra-forritunarmálsins (ZPL) sem notað er til að búa til útlit.

Merkjaútlit skjalaleiðar skilgreinir hvernig merkin eru sýnd og gögnin sem prentuð eru á þau. Þú stillir prentunarkveikipunkta þegar þú setur upp valmyndaratriði farsíma og vinnusniðmát.

Upplýsingarnar í þessari grein eiga við um öll merkjaútlit skjalaleiðar, þ.m.t. útlitin fyrir [númeraplötumerki](tasks/license-plate-label-printing.md), [gámamerki](print-container-labels.md) og [bylgjumerki](configure-wave-label-printing.md).

Þú getur prentað mjög flókna merkimiða, að því tilskildu að prentunarbúnaðurinn geti túlkað textann sem er sendur til hans. Til dæmis gæti ZPL-útlit sem inniheldur strikamerki líkst eftirfarandi dæmi.

```dos
^XA~TA000~JSN^LT0^MNW^MTD^PON^PMN^LH0,0^JMA^PR2,2~SD15^JUS^LRN^CI0^XZ
^XA
^MMT
^PW320
^LL0160
^LS0
^FT20,58^A0N,28,28^FH\^FDLabel:^FS
^FT20,81^AAN,18,10^FH\^FD$LicensePlateId$^FS
^BY1,3,17^FT20,106^BCN,,Y,N,N,A
^FD$LicensePlateId$^FS
^PQ1,,,Y^XZ
```

Sem hluti af prentunarferlinu verður textanum `$LicensePlateId$` í þessu dæmi skipt út fyrir gagnagildi. Nokkur víðtækt fáanleg verkfæri til merkjamyndunar geta hjálpað þér að forsníða textann fyrir útlit merkisins. Mörg þessara verkfæra styðja sniðið `$FieldName$`. Að auki notar Microsoft Dynamics 365 Supply Chain Management sérstaka sniðrökfræði sem hluta af reitavörpun fyrir uppsetningu skjalaleiðar.

Til að sjá gildin sem verða prentuð ferðu á **Vöruhúsastjórnun \> Fyrirspurnir og skýrslur \> Merkimiðar á númeraplötum**.

## <a name="turn-on-this-feature-for-your-system"></a>Kveikja á þessum eiginleika fyrir kerfið

Ef kerfið inniheldur ekki eiginleikana sem lýst er í þessari grein skal fara í [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og kveikja á eiginleikanum *Aukið skipulag á númeraplötumerki*. (Sem hluti af Supply Chain Management, útgáfa 10.0.21, er sjálfgefið kveikt á þessum eiginleika. Frá og með útgáfu 10.0.25 af Supply Chain Management er þessi eiginleiki skylda og ekki er hægt að slökkva á henni.

## <a name="custom-number-formats"></a>Sérsniðin tölusnið

Þú getur sérsniðið snið á tölulegum reitagildum sem eru prentuð með kóða með eftirfarandi sniði.

```dos
$FieldName:FormatString$
```

Hér er útskýring á þessu sniði:

- `FieldName` er heiti gagnareitsins (eins og **Magn**).
- `FormatString` skilgreinir hvernig prenta verður gögnin.

Eftirfarandi dæmi sýna hvernig þú getur sérsniðið vinnumagnsreitinn (**Magn**):

- Til að sýna alltaf fjóra tölustafi (með því að nota núll sem frátökutákn) notarðu `$Qty:0000$`. Til dæmis, ef magnið er 10 mun merkimiðinn sýna „0010”.
- Til að sýna alltaf tvo aukastafi notarðu `$Qty:0.00$`. Til dæmis, ef magnið er 10 mun merkimiðinn sýna „10,00”.

Fyrir fullan lista yfir tiltæka strengi tölusniðmáts, sjá [Sérsniðnir strengir tölusniðmáta](/dotnet/standard/base-types/custom-numeric-format-strings).

## <a name="custom-string-formats"></a>Sérsniðin strengjasnið

Þú getur fjarlægt fyrstu stafina í strengnum með því að nota eftirfarandi reit og sniðkóða.

```dos
$FieldName:#..$
```

Hér tilgreinir `#` fjölda stafa sem á að sleppa. Til dæmis, til að prenta númeraplötunúmer raðnúmers vörusendinga (SSCC) sem ekki eru fyrstu tveir stafirnir, notarðu `$LicensePlateId:2..$`. Í þessu tilfelli verður númeraplötunúmerið 0011111111111222221 prentað sem „11111111111222221”.

## <a name="custom-datetime-formats"></a>Sérsniðin dagsetningar-/tímasnið

Eftirfarandi dæmi sýnir hvernig þú getur stjórnað sniðinu sem er notað til að prenta dagsetningar.

```dos
$PrintedDate:dd-MM-yyyy$
```

Í þessu dæmi verður dagsetningin 30. apríl 2020 prentuð sem „30-04-2020”.

Fyrir fullan lista yfir tiltæka strengi dagsetningar-/tímasniðmáta, sjá [Sérsniðnir strengir dagsetningar- og tímasniðmáta](/dotnet/standard/base-types/custom-date-and-time-format-strings).

## <a name="print-individual-lines-from-multiline-data"></a>Prentaðu einstakar línur úr samvalsgögnum

Ef gagnareitur inniheldur margar línur (það er að segja línur sem eru aðskildar með línuskilum) geturðu prentað einstaka línu með eftirfarandi sniði.

```dos
$FieldName[#]$
```

Hér er `#` línunúmerið sem þú vilt prenta. (Notaðu 1 fyrir fyrstu línuna.)

Til dæmis, kerfið þitt er með reitinn `AdditionalAddress` sem geymir eftirfarandi samvalsheimilisfang:

Contoso Inc.  
123 Götuheiti  
Einhver borg, eitthvað ríki

Þú getur prentað þetta heimilisfang, eina línu í einu, með því að nota eftirfarandi kóða.

| Kóði | Texti sem er prentaður |
|---|---|
| `$AdditionalAddress[1]$` | Contoso Inc. |
| `$AdditionalAddress[2]$` | 123 Götuheiti |
| `$AdditionalAddress[3]$` | Einhver borg, eitthvað ríki |

## <a name="print-and-format-from-a-display-method"></a>Prenta og sníða úr birtingaraðferð

Þú getur prentað úr birtingaraðferð með því að nota eftirfarandi snið.

```dos
$DisplayMethod()$
```

Þú getur sameinað þetta snið og aðrar tegundir sem lýst var fyrr í þessari grein. Til dæmis ertu með skjáaðferð sem heitir `DisplayListOfItemsNumbers()` og þú vilt prenta fyrsta vörunúmer þessarar aðferðar. Í þessu tilviki er hægt að nota eftirfarandi kóða.

```dos
$DisplayListOfItemsNumbers()[1]$
```

## <a name="more-information-about-how-to-print-labels"></a>Nánari upplýsingar um hvernig á að prenta merkingar

Frekari upplýsingar um hvernig setja á upp og prenta merki er að finna í eftirfarandi greinum:

- [Prentun númeraplötumerkis](tasks/license-plate-label-printing.md)
- [Prenta merkimiða gáms](print-container-labels.md)
- [Prentun bylgjumerkis](configure-wave-label-printing.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
