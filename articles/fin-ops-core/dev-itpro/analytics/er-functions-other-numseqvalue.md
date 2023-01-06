---
title: NUMSEQVALUE ER-aðgerð
description: Í þessari grein er að finna upplýsingar um hvernig NUMSEQVALUE rafræn skýrslugerðarvirkni (ER) er notuð.
author: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 62255f0a47d3c67468cf2cf3922a1886c29c03d6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271554"
---
# <a name="numseqvalue-er-function"></a>NUMSEQVALUE ER-aðgerð

[!include [banner](../includes/banner.md)]

Aðgerðin `NUMSEQVALUE` skilar *strengja*-gildi sem táknar nýtt myndað gildi númeraraðar, byggt á tilgreindri númeraröð, umfangi og umfangskenni. Umfangskennið jafngildir fyrirtækjakóðanum sem er til staðar í því samhengi sem snið rafrænnar skýrslurgerðar (ER) er keyrt undir.

## <a name="syntax-1"></a>Málskipun 1

```vb
NUMSEQVALUE (number sequence code)
```

## <a name="syntax-2"></a>Málskipun 2

```vb
NUMSEQVALUE (number sequence record ID)
```

## <a name="syntax-3"></a>Málskipun 3

```vb
NUMSEQVALUE (number sequence code, scope type, scope ID)
```

## <a name="arguments"></a>Frumbreytur

`number sequence code`: *Strengur*

Textagildi sem táknar kóða númeraraðarinnar sem nýtt gildi er krafist í.

`number sequence record ID`: *Int64*

Gildið *Int64* sem táknar upptökuskilríki plötunnar í töflunni NumberSequenceTable sem inniheldur skilgreininguna á talnaröðinni sem nýtt gildi er krafist í.

`scope type`: *Upptaln.gildi*

Upptalningargildi upptalningarinnar **ERExpressionNumberSequenceScopeType** sem skilgreinir umfang númeraraðar sem nýtt gildi er krafist í. Fyrirliggjandi tegundir umfangs eru **Samnýtt**, **Lögaðili** og **Fyrirtæki**.

`scope ID`: *Strengur*

Gildið *Strengur* sem auðkennir umfangið, byggt á tiltekinni umfangsgerð.

## <a name="return-values"></a>Skilagildi

*Strengur*

Textagildið sem verður til.

## <a name="usage-notes"></a>Notkunarbréf

Fyrir umfangsgerðina **Samnýtt** skal tilgreina tóman streng sem umfangskenni.

Fyrir umfangsgerðirnar **Fyrirtækis** og **Lögaðila** skal tilgreina fyrirtækjakóðann sem umfangskennið. Ef þú tilgreinir tóman streng sem umfangskenni fyrir þessar umfangsgerðir er kóði gildandi fyrirtækis notaður.

Þegar málskipan 1 er notuð er beðið um númeraröð fyrir umfangsgerðina **Fyrirtæki** og fyrirtækjakóðinn er veittur með því samhengi sem ER-sniðið er keyrt undir.

## <a name="example-1"></a>Dæmi 1

Á ER-sniðinu skilgreinir þú gagnagjafann **AskNumSeq** af gerðinni *Innsláttarfæribreytur notanda*. Þessi gagnagjafi vísar til framlengdu gagnagerðarinnar (EDT) **Lýsing**. Næst skilgreinirðu gagnagjafann **NumSeq** af gerðinni *Reiknaður reitur*. Þessi gagnaveita inniheldur segðina `NUMSEQVALUE (AskNumSeq)`. Þegar gagnagjafinn **NumSeq** er kallaður skilar það nýju mynduðu gildi númeraraðar sem var tilgreind á keyrslutíma með því að slá kóðann inn í valmyndina. Óskað er eftir númeraröð fyrir umfangsgerðina **Fyrirtæki**. Fyrirtækjakóðinn er veittur með því samhengi sem ER-sniðið er keyrt undir.

## <a name="example-2"></a>Dæmi 2

Eftirfarandi gagnagjafar eru skilgreindir í líkanavörpuninni:

- Gagnagjafinn **LegderParms** af gerðinni *Tafla*. Þessi gagnagjafi vísar til LedgerParameters töflunnar.
- Gagnagjafinn **NumSeq** af gerðinni *Reiknaður reitur*. Þessi gagnaveita inniheldur segðina `NUMSEQVALUE ( LedgerParameters.'numRefJournalNum()'.NumberSequenceId)`.

Þegar **NumSeq** gagnaveitan er kölluð skilar hún nýmynduðu gildi númeraraðarinnar sem hefur verið skilgreint í fjárhagsfæribreytum fyrir fyrirtækið sem leggur til samhengið sem ER-sniði er keyrt undir. Þessi númeraröð auðkennir færslubókina á einkvæman hátt og vinnur sem lotunúmer sem tengir færslurnar saman.

## <a name="example-3"></a>Dæmi 3

Eftirfarandi gagnagjafar eru skilgreindir í líkanavörpuninni:

- Gagnagjafinn **enumScope** er hluti af Microsoft Dynamics 365 Finance *upptalningargerð*. Þessi gagnagjafi vísar til upptalningarinnar **ERExpressionNumberSequenceScopeType**.
- Gagnagjafinn **NumSeq** af gerðinni *Reiknaður reitur*. Þessi gagnaveita inniheldur segðina `NUMSEQVALUE ("Gene_1", enumScope.Company, "")`.

Þegar **NumSeq** gagnaveitan er kölluð skilar hún nýmynduðu gildi **Gene\_1** númeraröðarinnar sem hefur verið skilgreint fyrir fyrirtækið sem leggur til samhengið sem ER-sniði er keyrt undir.

## <a name="additional-resources"></a>Frekari upplýsingar

[Other (lénsértæk virkni fyrir viðskipti)](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
