---
title: GUIDVALUE ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin GUIDVALUE í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: 76b918354be9b5b695cfec9d0fe7aca6c5c9e08e01b6e3d0ddfa28af877942e3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6733148"
---
# <a name="guidvalue-er-function"></a>GUIDVALUE ER-aðgerð

[!include [banner](../includes/banner.md)]

Aðgerðin `GUIDVALUE` umreiknar tilgreint inntak af gerðinni *Strengur* í gagnaatriði af gerðinni *GUID*.

## <a name="syntax"></a>Málskipun

```vb
GUIDVALUE (input)
```

## <a name="arguments"></a>Frumbreytur

`input`: *Strengur*

Gild slóð í gagnagjafa af gerðinni *Strengur*.

## <a name="return-values"></a>Skilagildi

*GUID*

Gildi altækts einkvæms auðkennis (GUID) sem myndast.

## <a name="usage-notes"></a>Notkunarbréf

Til að umbreyta í gagnstæða átt (það er að breyta tilteknu inntaki *GUID* gagnagerðarinnar í gagnaatriði *Strengur* gagnagerðarinnar) er hægt að nota [TEXT](er-functions-text-text.md) virknina.

## <a name="example"></a>Dæmi

Þú skilgreinir eftirfarandi gagnagjafa í líkanavörpun þinni:

- Gagnagjafinn **myID** af gerðnni *Reiknað svæði* sem inniheldur segðina `GUIDVALUE ("AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0")`
- Gagnagjafinn **Users** af gerðinni *Töfluskrár* sem vísar til töflunnar UserInfo

Þú getur síðan notað segð eins og `FILTER (Users, Users.objectId = myID)` til að sía UserInfo töfluna með reitnum **ObjectId** í gagnagjafanum *GUID*.

## <a name="additional-resources"></a>Frekari upplýsingar

[Textavirkni](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]