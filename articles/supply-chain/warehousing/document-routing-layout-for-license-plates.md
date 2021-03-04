---
title: Uppsetning skjalaleiðar fyrir merkimiða á númeraplötu
description: Þetta efni lýsir því hvernig nota á sniðsaðferðir til að prenta gildi á merkimiða.
author: perlynne
manager: tfehr
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLicensePlateLabel, WHSLicensePlateLabelBuildConfig, WHSLicensePlateLabel, WHSDocumentRoutingLayout
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2012-04-01
ms.dyn365.ops.version: Release 10.0.10
ms.openlocfilehash: 8c96aef5d66ed8f8c44d74eee9b60f0a7d38a46d
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4430670"
---
# <a name="document-routing-layout-for-license-plate-labels"></a>Uppsetning skjalaleiðar fyrir merkimiða á númeraplötu

[!include [banner](../includes/banner.md)]

Uppsetning skjalaleiðar skilgreinir uppsetningu á merkimiðum númeraplötu og gögnin sem eru prentuð á þá. Þú stillir prentunarkveikipunkta þegar þú setur upp valmyndaratriði farsíma og vinnusniðmát.

Í dæmigerðri atburðarás prenta starfsmenn í móttöku vöruhúsa merkimiða strax eftir að þeir skrá innihald bretta sem berast á móttökusvæðið. Efnislegir merkimiðar eru settir á brettin. Síðan er hægt að nota þá til staðfestingar sem hluta af frágangsferlinu sem fylgir í kjölfarið og framtíðartínsluaðgerðum.

Þú getur prentað mjög flókna merkimiða, að því tilskildu að prentunarbúnaðurinn geti túlkað textann sem er sendur til hans. Til dæmis gæti skipulag forritunarmálsins Zebra (ZPL) sem inniheldur strikamerki líkst eftirfarandi dæmi.

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

Sem hluti af prentunarferlinu verður textanum `$LicensePlateId$` í þessu dæmi skipt út fyrir gagnagildi.

Til að sjá gildin sem verða prentuð ferðu á **Vöruhúsastjórnun \> Fyrirspurnir og skýrslur \> Merkimiðar á númeraplötum**.

Nokkur víðtækt fáanleg verkfæri til merkjamyndunar geta hjálpað þér að forsníða textann fyrir útlit merkisins. Mörg þessara verkfæra styðja sniðið `$FieldName$`. Að auki notar Microsoft Dynamics 365 Supply Chain Management sérstaka sniðrökfræði sem hluta af reitavörpun fyrir uppsetningu skjalaleiðar.

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

Fyrir fullan lista yfir tiltæka strengi tölusniðmáts, sjá [Sérsniðnir strengir tölusniðmáta](https://docs.microsoft.com/dotnet/standard/base-types/custom-numeric-format-strings).

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

Fyrir fullan lista yfir tiltæka strengi dagsetningar-/tímasniðmáta, sjá [Sérsniðnir strengir dagsetningar- og tímasniðmáta](https://docs.microsoft.com/dotnet/standard/base-types/custom-date-and-time-format-strings).

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

Þú getur sameinað þetta snið við aðrar gerðir sem lýst var fyrr í þessu efni. Til dæmis ertu með skjáaðferð sem heitir `DisplayListOfItemsNumbers()` og þú vilt prenta fyrsta vörunúmer þessarar aðferðar. Í þessu tilviki er hægt að nota eftirfarandi kóða.

```dos
$DisplayListOfItemsNumbers()[1]$
```

## <a name="more-information-about-how-to-print-labels"></a>Nánari upplýsingar um hvernig á að prenta merkingar

Nánari upplýsingar um hvernig á að setja upp og prenta merkimiða, sjá [Virkja prentun merkis á númeraplötu](tasks/license-plate-label-printing.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]