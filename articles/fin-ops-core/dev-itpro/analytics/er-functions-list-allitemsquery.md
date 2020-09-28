---
title: ALLITEMSQUERY ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin ALLITEMSQUERY í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 37546fccf804a4522638147d39206997e8c0c24c
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745370"
---
# <a name="allitemsquery-er-function"></a>ALLITEMSQUERY ER-aðgerð

[!include [banner](../includes/banner.md)]

Aðgerðin `ALLITEMSQUERY` keyrir sem sameinuð SQL-fyrirspurn. Það skilar nýju flöttu gildi *Skráalista* sem samanstendur af lista yfir skrár sem tákna alla hluti sem passa við tilgreinda slóð.

## <a name="syntax"></a>Málskipun

```vb
ALLITEMSQUERY (path)
```

## <a name="arguments"></a>Frumbreytur

`path`: *Skráalisti*

Gild slóð í gagnagjafa af gagnagerðinni *Skráalisti*. Hann verður að innihalda að minnsta kosti ein tengsl.

## <a name="return-values"></a>Skilagildi

*Skráalisti*

Sá listi yfir skrár sem er búinn til.

## <a name="usage-notes"></a>Notkunarbréf

Tilgreind slóð verður að vera skilgreind sem gild slóð gagnagjafa á gagnagjafaþætti af gagnagerðinni *Skráalisti*. Hann verður einnig að innihalda að minnsta kosti ein tengsl. Gagnaeiningar eins og slóðin *Strengur* og *Dagsetning* ættu að gefa upp villu í segðasmíði rafrænnar skýrslugerðar (ER) á tíma hönnunar.

Þegar þessari aðgerð er beitt á gagnagjafa af gagnagerðinni *Skráalisti* sem vísar til forritshlutar sem hægt er að kalla beint með því að nota SQL (til dæmis töflu, einingu eða fyrirspurn) keyrir hún sem sameinuð SQL-fyrirspurn. Annars keyrir það í minni sem aðgerðin [ALLITEMS](er-functions-list-allitems.md).

## <a name="example"></a>Dæmi

Þú skilgreinir eftirfarandi gagnagjafa í líkanavörpun þinni:

- Gagnagjafinn **CustInv** af gerðinni *Töfluskrár* sem vísar til töflunnar CustInvoiceTable
- Gagnagjafinn **FilteredInv** af gerðnni *Reiknað svæði* sem inniheldur segðina `FILTER (CustInv, CustInv.InvoiceAccount = "US-001")`
- Gagnagjafinn **JourLines** af gerðnni *Reiknað svæði* sem inniheldur segðina `ALLITEMSQUERY ( FilteredInv.'<Relations'.CustInvoiceJour.'<Relations'.CustInvoiceTrans)`

Þegar þú keyrir líkanavörpunina til að kalla á gagnagjafann **JourLines** keyrist eftirfarandi SQL-skipun:

```sql
SELECT ... FROM CUSTINVOICETABLE T1 CROSS JOIN CUSTINVOICEJOUR T2 CROSS JOIN
CUSTINVOICETRANS T3 WHERE...
```

## <a name="additional-resources"></a>Frekari upplýsingar

[Listavirkni](er-functions-category-list.md)
