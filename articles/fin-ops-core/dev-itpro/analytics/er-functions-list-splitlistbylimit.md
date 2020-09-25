---
title: SPLITLISTBYLIMIT ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin SPLITLISTBYLIMIT í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: 5bf13b7c1e7cab7c803b352370084421a8180dee
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743433"
---
# <a name="splitlistbylimit-er-function"></a>SPLITLISTBYLIMIT ER-aðgerð

[!include [banner](../includes/banner.md)]

Aðgerðin `SPLITLISTBYLIMIT` skiptir upp tilteknum lista í nýjan lista yfir undirlista (runur). Fjöldi skráninga í hverri lotu er reiknaður með virkum hætti. Aðgerðin skilar síðan niðurstöðunni sem nýju *Skráalista*-gildi sem samanstendur af rununum.

## <a name="syntax"></a>Málskipun

```vb
SPLITLISTBYLIMIT (list, limit value, limit source)
```

## <a name="arguments"></a>Frumbreytur

`list`: *Skráalisti*

Gild slóð í gagnagjafa af gagnagerðinni *Skráalisti*.

`limit value`: *Heiltala* eða *Raun*

Hámarksgildið fyrir mörkin sem eru notuð til að skipta upprunalegu listanum í runur.

`limit source`: *Reitur*

Gild slóð á reit af gerðinni *Heiltala* eða *Raun* í tilgreindum lista. Gildi þessa reits skilgreinir skrefið sem heildarupphæðin er aukin á.

## <a name="return-values"></a>Skilagildi

*Skráalisti*

Sá listi yfir skrár sem er búinn til.

## <a name="usage-notes"></a>Notkunarbréf

Listi yfir runur sem er skilað inniheldur eftirfarandi þætti:

- **Gildi**: *Listi*

    Listi yfir skrár sem tilheyra núverandi runu.

- **BatchNumber**: *Heiltala*

    Númer gildandi runu í skiluðum lista.

Markinu er ekki beitt á staka vöru á upprunalega listanum ef upprunamarkið fer yfir skilgreind mörk.

## <a name="example"></a>Dæmi

Eftirfarandi skýringarmynd sýnir snið rafrænnar skýrslugerðar (ER).

<a href="./media/ger-splitlistbylimit-format.png"><img src="./media/ger-splitlistbylimit-format.png" alt="Format" class="alignnone size-full wp-image-1204063" width="396" height="195" /></a>

Eftirfarandi skýringarmynd sýnir gagnagjafana sem eru notaðir fyrir sniðið.

<a href="./media/ger-splitlistbylimit-datasources.png"><img src="./media/ger-splitlistbylimit-datasources.png" alt="Data sources" class="alignnone size-full wp-image-1204073" width="320" height="208" /></a>

Eftirfarandi mynd sýnir niðurstöðuna þegar sniðið er keyrt. Í þessu tilviki er úttakið flatur listi yfir vörutegundir.

<a href="./media/ger-splitlistbylimit-output.png"><img src="./media/ger-splitlistbylimit-output.png" alt="Output" class="alignnone size-full wp-image-1204083" width="462" height="204" /></a>

Í eftirfarandi myndum hefur sama sniðið verið breytt þannig að það birtir listann yfir vörutegundir í runum ef ein runa verður að innihalda vörutegundir og heildarþyngdin ætti ekki að fara yfir hámarkið 9.

<a href="./media/ger-splitlistbylimit-format-1.png"><img src="./media/ger-splitlistbylimit-format-1.png" alt="Adjusted format" class="alignnone size-full wp-image-1204103" width="466" height="438" /></a>

<a href="./media/ger-splitlistbylimit-datasources-1.png"><img src="./media/ger-splitlistbylimit-datasources-1.png" alt="Data sources for the adjusted format" class="alignnone size-full wp-image-1204093" width="645" height="507" /></a>

Eftirfarandi mynd sýnir niðurstöðurnar þegar stillt snið er keyrt.

<a href="./media/ger-splitlistbylimit-output-1.png"><img src="./media/ger-splitlistbylimit-output-1.png" alt="Output of the adjusted format" class="alignnone size-full wp-image-1204113" width="676" height="611" /></a>

> [!NOTE] 
> Mark er ekki beitt á síðasta hlut í upprunalistanum, vegna þess að gildi (**11**) mörkum upprunans (**þyngd**) fer yfir skilgreind mörk (**9**). Til að hunsa undirlista við skýrslumyndun skal nota annaðhvort aðgerðina `WHERE` eða segðina **Virkjað** í samsvarandi sniðmátsþætti, eftir því sem þarf.

## <a name="additional-resources"></a>Frekari upplýsingar

[Listavirkni](er-functions-category-list.md)
