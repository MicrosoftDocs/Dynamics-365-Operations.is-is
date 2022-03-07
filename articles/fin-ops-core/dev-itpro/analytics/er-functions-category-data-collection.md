---
title: Listi yfir ER-aðgerðir í gagnasafnsflokknum
description: Þetta efni veitir upplýsingar um gagnasafnsaðgerðir sem eru studdar í rafrænni skýrslugerð (ER).
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: ba3a1f031a4a98592081b04a4128450aeb8218ef
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561735"
---
# <a name="list-of-er-functions-in-the-data-collection-category"></a>Listi yfir ER-aðgerðir í gagnasafnsflokknum

[!include [banner](../includes/banner.md)]

Gagnasafnsaðgerðir rafrænna skýrslugerða (ER) eru notaðar til að telja og leggja saman á ER-sniði sem er verið að keyra, byggt á gögnum um frálags sem þegar er búið til á sniðinu **Texti** eða **Xml**. Þessi aðferð er notuð til að bæta afköst ER-sniðs sem er keyrt, til að færa inn gildi hlaupatölur í mynduðum skjölum og í öðrum tilgangi. Þetta efni gefur yfirlit yfir þessar aðgerðir.

## <a name="list-of-supported-functions"></a>Listi yfir studdar aðgerðir

| Aðgerð | Lýsing |
|----------|-------------|
| [CollectedList](er-functions-datacollection-collectedlist.md) | Þessi aðgerð skilar *Skráalista*-gildi sem inniheldur lista yfir gildi sem skilað var af eiginleikanum **Gildi lykils fyrir söfnuð gögn** í sniðþáttum og safnað þegar sniðþættirnir voru notaðir til að búa til útleiðarskjal við sniðkeyrsluna og sem fullnægir tilgreindum skilyrðum. Hvert skilyrði samanstendur af lykilsviði og lykilgildi. |
| [CountIF](er-functions-datacollection-countif.md) | Þessi aðgerð skilar *Heiltölu*-gildi sem táknar fjölda sniðaþátta sem var safnað þegar sniðþættirnir voru notaðir til að búa til útleiðarskjal við sniðkeyrsluna og sem fullnægir tilgreindu skilyrði. Skilyrðið samanstendur af lykilsviði og lykilgildi. |
| [CountIFs](er-functions-datacollection-countifs.md) | Þessi aðgerð skilar *Heiltölu*-gildi sem táknar fjölda sniðaþátta sem var safnað þegar sniðþættirnir voru notaðir til að búa til útleiðarskjal við sniðkeyrsluna og sem fullnægir tilgreindum skilyrðum. Hvert skilyrði samanstendur af lykilsviði og lykilgildi. |
| [FormatElementName](er-functions-datacollection-formatelementname.md) | Þessi aðgerð skilar *Strengjagildi* sem táknar nafn á gildandi ER-sniðmátsþætti. |
| [SumIF](er-functions-datacollection-sumif.md) | Þessi aðgerð skilar *Raungildi* sem táknar summu gilda sem var skilað af bindingum sniðaþátta og safnað þegar sniðþættirnir voru notaðir til að búa til útleiðarskjal við sniðkeyrsluna og sem fullnægir tilgreindu skilyrði. Skilyrðið samanstendur af lykilsviði og lykilgildi. |
| [SumIFs](er-functions-datacollection-sumifs.md) | Þessi aðgerð skilar *Raungildi* sem táknar summu gilda sem var skilað af bindingum sniðaþátta og safnað þegar sniðþættirnir voru notaðir til að búa til útleiðarskjal við sniðkeyrsluna og sem fullnægir tilgreindum skilyrðum. Hvert skilyrði samanstendur af lykilsviði og lykilgildi. |

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir rafræna skýrslugerð](general-electronic-reporting.md)

[Formúluhönnuður í rafrænni skýrslugerð](general-electronic-reporting-formula-designer.md)

[Formúlutungumál í rafrænni skýrslugerð](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]