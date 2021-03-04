---
title: Listi yfir ER-aðgerðir í listaflokknum
description: Þetta efni veitir upplýsingar um listaaðgerðir sem eru studdar í rafrænni skýrslugerð (ER).
author: NickSelin
manager: kfend
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: e2e708c59bceebf845ee78c98057133bb2892cf9
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686178"
---
# <a name="list-of-er-functions-in-the-list-category"></a>Listi yfir ER-aðgerðir í listaflokknum

[!include [banner](../includes/banner.md)]

Hægt er að nota rafræn skýrslugerð (ER) lista aðgerðir til að draga upplýsingar úr og framkvæma aðgerðir á gagnagjafa gagnagerðirnar *Skráalisti* og *Ílát (skrá)*. Þetta efni gefur yfirlit yfir þessar aðgerðir.

## <a name="list-of-supported-functions"></a>Listi yfir studdar aðgerðir

| Aðgerð | Lýsing |
|----------|-------------|
| [AllItems](er-functions-list-allitems.md)                 | Þessi aðgerð keyrir sem val í minni. Það skilar nýju flöttu gildi *Skráalista* sem samanstendur af lista yfir skrár sem tákna alla hluti sem passa við tilgreinda slóð. |
| [AllItemsQuery](er-functions-list-allitemsquery.md)       | Þessi aðgerð keyrir sem sameinuð SQL-fyrirspurn. Það skilar nýju flöttu gildi *Skráalista* sem samanstendur af lista yfir skrár sem tákna alla hluti sem passa við tilgreinda slóð. |
| [Talning](er-functions-list-count.md)                       | Þessi aðgerð skilar *Heiltölu*-gildi sem táknar fjölda skráa á tilgreindum lista, ef listinn er ekki tómur. Ef listinn er tómur skilar þessi aðgerð **0** (núlli). |
| [EmptyList](er-functions-list-emptylist.md)               | Þessi aðgerði skilar tómu *Skráarlista*-gildi með því að nota tilgreindan lista sem uppruna fyrir skipulag lista.|
| [Tölusetja](er-functions-list-enumerate.md)               | Þessi aðgerð skilar nýju *Skráalista*-gildi sem samanstendur af tölusettum skrám á tilgreindum lista. |
| [Sía](er-functions-list-filter.md)                     | Þessi aðgerð skilar tilgreindum lista sem *Skráalista*-gildi eftir að fyrirspurninni hefur verið breytt þannig að hún síar að tilteknu ástandi. |
| [Fyrst](er-functions-list-first.md)                       | Þessi aðgerð skilar fyrstu skrá yfir tilgreinda listann sem gildinu *Ílát (skrá)*, ef listinn er ekki tómur. Ef listinn er tómur kastar þessi aðgerð frá sér undantekningu. |
| [FirstOrNull](er-functions-list-firstornull.md)           | Þessi aðgerð skilar fyrstu skrá yfir tilgreinda listann sem gildinu *Ílát (skrá)*, ef skráin er ekki tóm. Ef skráin er tóm skilar þessi aðgerð núll *Ílát (skrá)* gildi. |
| [Index](er-functions-list-index.md)                       | Þessi aðgerð skilar gildinu *Ílát (skrá)* sem er valið með því að nota tilgreindan töluvísi í tilgreindum lista. Ef vísirinn utan marka fyrir skrárnar í tilgreindum lista beitir þessi aðgerð undantekningu. |
| [IsEmpty](er-functions-list-isempty.md)                   | Þessi aðgerð skilar *Boolean*-gildinu **SATT** ef tilgreindur listi inniheldur engar skrár. Að öðrum kosti skilar hún *Boolean* gildinu **FALSE**. |
| [Listi](er-functions-list-list.md)                         | Þessi aðgerð skilar *Skráalista*-gildi sem samanstendur af nýjum lista sem er stofnaður úr tilgreindum segðum.|
| [ListDistinct](er-functions-list-listdistinct.md)         | Þessi aðgerð reiknar tilgreinda segð sem val fyrir hverja færslu í tilgreindum lista. Hún skilar nýju gildi *Færslulista* sem inniheldur eina færslu fyrir hvert einkvæmt valgildi.|
| [ListJoin](er-functions-list-listjoin.md)                 | Þessi aðgerð skilar *Skráalista*-gildi sem sýnir nýjan sameinaðan lista sem er stofnaður úr tilgreindum segðum.|
| [ListOfFields](er-functions-list-listoffields.md)         | Þessi aðgerð skilar *Skráalista*-gildi sem er stofnað byggt á skipulagi tilgreindrar segðar af gerðinni *Upptalning* eða *Ílát (skrá)*. |
| [ListOfFirstItem](er-functions-list-listoffirstitem.md)   | Þessi aðgerð skilar *Skráalista*-gildi sem samanstendur af aðeins fyrstu skránni á tilgreindum lista.|
| [OrderBy](er-functions-list-orderby.md)                   | Þessi aðgerð skilar tilgreindum lista sem *Skráalista*-gildi eftir að því hefur verið raðað í samræmi við tilgreindar segðir. Þessi frumbreytur geta verið skilgreindar sem segðir. |
| [Bakfæra](er-functions-list-reverse.md)                   | Þessi aðgerð skilar tilgreindum lista sem *Skráalista*-gildi í öfugri röð. |
| [Skipta](er-functions-list-split.md)                       | Þessi aðgerð skiptir upp tilteknum ílagsstreng í undirstrengi og skilar niðurstöðunni sem nýju *Skráalista*-gildi. |
| [SplitList](er-functions-list-splitlist.md)               | Þessi aðgerði skiptir tilgreindum lista niður í undirlista (eða runur) sem hver inniheldur tilgreindan fjölda skráa. Hún skilar síðan niðurstöðunni sem nýju *Skráalista*-gildi sem samanstendur af rununum. |
| [SplitListByLimit](er-functions-list-splitlistbylimit.md) | Þessi aðgerð skiptir upp tilteknum lista í nýjan lista yfir undirlista (runur). Fjöldi skráninga í hverri lotu er reiknaður með virkum hætti. Aðgerðin skilar síðan niðurstöðunni sem nýju *Skráalista*-gildi sem samanstendur af rununum. |
| [StringJoin](er-functions-list-stringjoin.md)             | Þessi aðgerð skilar *strengjagildi* sem samanstendur af samsettum gildum tiltekins svæðis úr tilgreindum lista. Hægt er að aðskilja gildin með tilgreindri afmörkun. |
| [Hvar](er-functions-list-where.md)                       | Þessi aðgerð skilar tilgreindum lista sem *Skráalista*-gildi eftir að það hefur verið síað í samræmi við tilgreind skilyrði. |

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir rafræna skýrslugerð](general-electronic-reporting.md)

[Formúluhönnuður í rafrænni skýrslugerð](general-electronic-reporting-formula-designer.md)

[Formúlutungumál í rafrænni skýrslugerð](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]