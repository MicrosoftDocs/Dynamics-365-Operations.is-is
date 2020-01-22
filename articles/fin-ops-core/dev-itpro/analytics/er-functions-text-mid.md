---
title: MID ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin MID í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: e178b01740954b46e2afbd2a2be6200a652a18c0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915603"
---
# <a name="MID">MID ER aðgerð</a>

[!include [banner](../includes/banner.md)]

Aðgerðin `MID` skilar *strengjagildi* sem sýnir tilgreindan fjölda staftákna frá tilteknum streng, með upphafi í tilgreindri stöðu.

## <a name="syntax"></a>Málskipun

```
MID (text, starting position, number of characters)
```

## <a name="arguments"></a>Frumbreytur

`text`: *Strengur*

Gildið *Strengur* sem tilgreinir textann sem á að skila staftáknum úr.

`starting position`: *Heiltala*

Gildið *Heiltala* sem tilgreinir staðsetningu fyrsta stafsins sem þarf að skila úr tilgreindum texta.

`number of characters`: *Heiltala*

Gildið *Heiltala* sem tilgreinir fjölda stafa sem þarf að skila, frá tilgreindri upphafsstöðu.

## <a name="return-values"></a>Skilagildi

*Strengur*

Textagildið sem verður til.

## <a name="usage-notes"></a>Notkunarbréf

Ef gildi frumbreytunnar `starting position` er lægra en 0 (núll) eru stafirnir sem er skilað taldir frá fyrstu stöðu í tilgreindum streng.

Ef gildi frumbreytunnar `starting position` er lengra en tilgreindur strengur er tómum streng skilað.

## <a name="example"></a>Dæmi

`MID ("Sample", 2, 3)` skilar **"amp"**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Textavirkni](er-functions-category-text.md)
