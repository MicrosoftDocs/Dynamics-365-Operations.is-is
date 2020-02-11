---
title: SPLITLIST ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin SPLITLIST í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: b324d42a53b35074ba62ccf3df7b77cb4db70450
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917213"
---
# <a name="SPLITLIST">SPLITLIST ER-aðgerð</a>

[!include [banner](../includes/banner.md)]

Aðgerðin `SPLITLIST` skiptir tilgreindum lista niður í undirlista (eða runur) sem hver inniheldur tilgreindan fjölda skráa. Hún skilar síðan niðurstöðunni sem nýju *Skráalista*-gildi sem samanstendur af rununum.

## <a name="syntax"></a>Málskipun

```
SPLITLIST (list, number)
```

## <a name="arguments"></a>Frumbreytur

`list`: *Skráalisti*

Gild slóð í gagnagjafa af gagnagerðinni *Skráalisti*.

`number`: *Heiltala*

Hámarksfjöldi skráa í hverri runu.

## <a name="return-values"></a>Skilagildi

*Skráalisti*

Sá listi yfir skrár sem er búinn til.

## <a name="usage-notes"></a>Notkunarbréf

Listi yfir runur sem er skilað inniheldur eftirfarandi þætti:

 - **Gildi:** *Listi*

    Listi yfir skrár sem tilheyra núverandi runu.

- **BatchNumber:** *Heiltala*

    Númer gildandi runu í skiluðum lista.

## <a name="example"></a>Dæmi

Í eftirfarandi mynd er gagnagjafi **Lína** búinn til sem skráalisti sem hefur þrjár skrár. Þessi listi er skiptur í runur, sem hver um sig inniheldur allt að tvær færslur.

<a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

Eftirfarandi mynd sýnir hannað útlit sniðs. Í þessu sniðmáti eru tengsl við gagnagjafann **Línur** mynduð til að búa til úttak á XML sniði. Þessi útkoma kynnir einstaka hnúta fyrir hverja runu og færslurnar í henni.

<a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a>

Eftirfarandi mynd sýnir niðurstöðuna þegar hannaða sniðið er keyrt.

<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a>

## <a name="additional-resources"></a>Frekari upplýsingar

[Listavirkni](er-functions-category-list.md)