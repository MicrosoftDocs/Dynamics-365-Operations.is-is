---
title: Listi yfir ER-aðgerðir í rökfræðiflokknum
description: Þessi grein veitir upplýsingar um röklegar aðgerðir sem eru studdar í rafrænni skýrslugerð (ER).
author: kfend
ms.date: 02/11/2021
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
ms.openlocfilehash: 1d011968d9cfa4125e7283ca36c3558e3e79b93a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291295"
---
# <a name="list-of-er-functions-in-the-logical-category"></a>Listi yfir ER-aðgerðir í rökfræðiflokknum

[!include [banner](../includes/banner.md)]

Rafrænar skýrslutökur (ER) geta verið notaðar til að vinna með rökleg gildi til að framkvæma fleiri en einn samanburð á einni tjáningu eða prófa margar aðstæður. Þessi grein gefur yfirlit yfir þessar aðgerðir.

## <a name="list-of-supported-functions"></a>Listi yfir studdar aðgerðir

| Aðgerð | Lýsing |
|----------|-------------|
| [Og](er-functions-logical-and.md)                       | Þessi aðgerð skilar *Boolean*-gildi **SATT** ef öll tilgreind skilyrði eru sönn. Að öðrum kosti skilar hún *Boolean* gildinu **FALSE**. |
| [Tilvik](er-functions-logical-case.md)                     | Þessi aðgerð metur gildi tiltekinnar segðar á móti tilgreindum valkostum og skilar niðurstöðu fyrsta valmöguleikans sem jafngildir gildi tiltekinnar segðar. Annars skilar hún valkvæðri sjálfgefinni niðurstöðu, ef sjálfgefin niðurstaða er tilgreind sem síðasta frumbreyta kallaðrar aðgerðar sem valkostur kemur ekki á undan. Gildið sem er skilað getur verið gildi allra þeirra gagnagerða sem studdar eru. |
| [Innheldur](er-functions-logical-contains.md)             | Þessi aðgerð ákvarðar hvort tilgreindur innsláttur inniheldur tiltekinn texta. Hún skilar *Boole-gildinu* **TRUE** ef tilgreindur innsláttur inniheldur tilgreindan texta. Að öðrum kosti skilar hún *Boolean* gildinu **FALSE**. |
| [EndsWith](er-functions-logical-endswith.md)             | Þessi aðgerð ákvarðar hvort tilgreindur innsláttur endar á tilteknum texta. Hún skilar *Boole-gildinu* **TRUE** ef tilgreindur innsláttur endar á tilgreindum texta. Að öðrum kosti skilar hún *Boolean* gildinu **FALSE**. |
| [Ef](er-functions-logical-if.md)                         | Þessi aðgerð skilar fyrsta tilgreinda gildinu ef tilgreinda skilyrðið er uppfyllt. Að öðrum kosti skilar hún öðru tilgreinda gildinu. Gildið sem er skilað getur verið gildi allra þeirra gagnagerða sem studdar eru. |
| [Ekki](er-functions-logical-not.md)                       | Þessi aðgerð skilar bakfærðu röklegu gildi tilgreinds skilyrðis sem *Boolean*-gildi. |
| [Or](er-functions-logical-or.md)                         | Þessi aðgerð skilar *Boolean*-gildinu **FALSE** ef öll tilgreind skilyrði eru ósönn. Ef eitthvert tilgreint skilyrði er satt skilar aðgerðin *Boolean*-gildinu **TRUE** ef öll tilgreind skilyrði eru sönn. |
| [StartsWith](er-functions-logical-startswith.md)         | Þessi aðgerð ákvarðar hvort tilgreindur innsláttur hefst á tilteknum texta. Hún skilar *Boole-gildinu* **TRUE** ef tilgreindur innsláttur byrjar á tilgreindum texta. Að öðrum kosti skilar hún *Boolean* gildinu **FALSE**. |
| [ValueIn](er-functions-logical-valuein.md)               | Þessi aðgerð ákvarðar hvort tilgreint ílag passar við eitthvert gildi tilgreinds hlutar sem er í tilgreindum lista. Hún skilar *Boolean*-gildinu **TRUE** ef tilgreint inntak passar við niðurstöðu þess að keyra tiltekna segð fyrir að minnsta kosti eina skrá af tilgreindum lista. Að öðrum kosti skilar hún *Boolean* gildinu **FALSE**. |
| [ValueInLarge](er-functions-logical-valueinlarge.md)     | Þessi virknin ákvarðar hvort tilgreindur innsláttur *Int64* eða *Heiltala* passar við eitthvað gildi hlutar sem er í tilgreindum lista. Hún skilar *Boolean*-gildinu **TRUE** ef tilgreint inntak passar við niðurstöðu þess að keyra tiltekna segð fyrir að minnsta kosti eina skrá af tilgreindum lista. Að öðrum kosti skilar hún *Boolean* gildinu **FALSE**. |


## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir rafræna skýrslugerð](general-electronic-reporting.md)

[Formúluhönnuður í rafrænni skýrslugerð](general-electronic-reporting-formula-designer.md)

[Formúlutungumál í rafrænni skýrslugerð](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
