---
title: Rafræn skýrslugerðarvirkni LISTDISTINCT
description: Í þessari grein er að finna upplýsingar um hvernig rafræn skýrslugerðarvirkni LISTDISTINCT er notuð.
author: kfend
ms.date: 07/30/2020
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.14
ms.custom: ''
ms.assetid: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: cd773f3455af1be1e952cb3852a648436670ce0f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285276"
---
# <a name="listdistinct-er-function"></a>Rafræn skýrslugerðarvirkni LISTDISTINCT

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Virknin `LISTDISTINCT` reiknar tilgreinda segð sem val fyrir hverja færslu í tilgreindum lista. Hún skilar nýju gildi *Færslulista* sem inniheldur eina færslu fyrir hvert einkvæmt valgildi.

## <a name="syntax"></a>Málskipun

```
LISTDISTINCT (list, selector)
```

## <a name="arguments"></a>Frumbreytur

`list`: *Skráalisti*

Gild slóð í gagnagjafa af gagnagerðinni *Skráalisti*.

`selector`: *Frumstæð gagnagerð*

Gild segð sem notuð er til að reikna valgildi fyrir hverja færslu í tilgreindum lista.

Eftirfarandi gagnagerðir eru studdar fyrir þessa færibreytu:

- Boole
- Dagsetning
- DateTime-gildi
- Guid
- Heiltala
- Int64
- Rauntala
- Strengur

## <a name="return-values"></a>Skilagildi

*Færslulisti*

Sá listi yfir skrár sem er búinn til.

## <a name="usage-notes"></a>Notkunarbréf

Skipulagið á listanum sem er stofnaður samsvarar skipulagi tilgreinda listans.

Sama valgildið kann að vera reiknað út fyrir margar færslur í tilgreindum lista. Í þessu tilfelli samsvara reitargildi samsvarandi færslu í stofnaða listanum gildum fyrstu færslunnar úr tilgreindum lista sem valgildið er reiknað út fyrir.

Framkvæmd þessarar virkni er gerð í hvaða gagnagjafa [Rafrænnar skýrslugerðar](general-electronic-reporting.md) sem er af gerðinni *Færslulisti* sem er til staðar í minni.

Einnig er hægt að nota gagnagjafann **GROUPBY** til að búa til lista yfir færslur sem valið sem er með sérstæð gildi er reiknað fyrir. Hins vegar, séð út frá afköstum og minnisnotkun, er betra að nota virknina `LISTDISTINCT` í stað gagnagjafans **GROUPBY** vegna þess að virknin er keyrð í minni.

## <a name="example"></a>Dæmi

Eftirfarandi dæmi sýnir hvernig hægt er að fá listann yfir einkvæmt númer viðskiptavinalykils sem að minnsta kosti einn sölureikningur eða verkreikningur hefur verið gefinn út á yfir tiltekið tímabil.

1. Færið inn gagnagjafann **SalesInvoice** af gerðinni `Record list` sem vísar í jöfnunartöfluna **CustInvoiceJour** og síar sölureikninga fyrir ákveðin tímabil.

    Svæðið `InvoiceAccount` í þessum gagnagjafa skilar lykilnúmeri reikningsfærðs viðskiptavinar.

2. Færið inn gagnagjafann **ProjectInvoice** af gerðinni `Record list` sem vísar í jöfnunartöfluna **ProjInvoiceJour** og síar verkeikninga fyrir ákveðin tímabil.

    Svæðið `InvoiceAccount` í þessum gagnagjafa skilar lykilnúmeri reikningsfærðs viðskiptavinar.

3. Skilgreinið gagnagjafann **AllInvoices** af gerðinni `Calculated field` sem inniheldur segðina `LISTJOIN(SalesInvoice, ProjectInvoice)`.

    Þessi gagnagjafi skilar sameinaða listanum yfir sölureikninga og verkreikninga.

4. Skilgreinið gagnagjafann **InvoicedCustomer** af gerðinni `Record list` sem inniheldur segðina `LISTDISTINCT(AllInvoices, AllInvoices.InvoiceAccount)`.

    Þessi gagnagjafi skilar nýjum lista sem inniheldur eina færslu fyrir hvern einkvæman viðskiptavin sem hefur verið reikningsfærður á skilgreindu tímabili. Svæðið `InvoiceAccount` í þessum lista inniheldur númer viðskiptavinalykils.

## <a name="additional-resources"></a>Frekari upplýsingar

[Listaaðgerðir](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
