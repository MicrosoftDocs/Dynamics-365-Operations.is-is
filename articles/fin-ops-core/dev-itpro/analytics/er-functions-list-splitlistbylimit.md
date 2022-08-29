---
title: SPLITLISTBYLIMIT ER-aðgerð
description: Þessi grein veitir upplýsingar um hvernig SPLITLISTBYLIMIT rafræn skýrslugerð (ER) aðgerðin er notuð.
author: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: d43ca9bd33cf21a0d72e407317088c9703bbf303
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271674"
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
