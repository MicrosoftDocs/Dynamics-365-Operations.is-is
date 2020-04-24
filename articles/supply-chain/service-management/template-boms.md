---
title: Sniðmátsuppskriftir
description: Sniðmátsuppskrift veitir staðlaðan lista yfir íhluti fyrir þjónustuhluti sem eru reglulega þjónustaðir.
author: ShylaThompson
manager: tfehr
ms.date: 09/19/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8842a293a50efb24590784cc52ef0254eca10e3a
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206543"
---
# <a name="template-boms"></a>Sniðmátsuppskriftir    

[!include [banner](../includes/banner.md)]


Sniðmátsuppskrift veitir þér staðlaðan lista yfir íhluti fyrir þjónustuhluti sem eru reglulega þjónustaðir. Íhlutirnir sem eru taldir upp í sniðmátsuppskrift tákna einstaka undiríhluti þjónustuhlutarins. Með því að nota sniðmátsuppskrift fyrir þjónustuhlut er hægt að halda skrá yfir þá undiríhluti sem hefur verið skipt út á þjónustuhlutnum.

Til þess að nota sniðmátsuppskrift í þjónustusamningi eða þjónustupöntun er hún tengd við þjónustuhlutatengsl.


> [!NOTE]
> <P>Þú getur aðeins notað eina sniðmátsuppskrift á þjónustuhlut.</P>

## <a name="create-a-template-bom"></a>Stofna sniðmátsuppskrift

Eftirfarandi tafla inniheldur upplýsingar um hinar ýmsu aðferðir sem hægt er að nota til að stofna sniðmátsuppskrift.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Aðferð</p></th>
<th><p>lýsing</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Framleiðsla</p></td>
<td><p>Sniðmátsuppskriftin byggist á framleiðslupöntun. Þessi valkostur á aðeins við ef þú starfar í vinnsluumhverfi. Kostirnir eru þeir að notandinn fær gildandi og ítarlegan lista yfir íhlutina sem eru í tiltekinni vöru.</p></td>
</tr>
<tr class="even">
<td><p>Vara BOM</p></td>
<td><p>Sniðmátsuppskrift er byggð á uppskriftarvöru. Uppskriftarvaran, ólíkt framleiðsluuppskrift, er fastur listi yfir þá íhluti sem gera vöru.</p></td>
</tr>
<tr class="odd">
<td><p>Fyrirliggjandi sniðmát</p></td>
<td><p>Sniðmátið er byggt á fyrirliggjandi sniðmátsuppskrift.</p></td>
</tr>
<tr class="even">
<td><p>Beinskiptur</p></td>
<td><p>Ef þú veist hvaða varahlutum er venjulega skipt út á þjónustuhlut getur þú stofnað sniðmátsuppskriftina þína handvirkt. Þessi aðferð hjálpar til við að ganga úr skugga um að íhlutirnir sem eru hluti af sniðmátinu endurspegli raunverulegar kröfur vinnustaðarins.</p></td>
</tr>
</tbody>
</table>


## <a name="apply-the-template-bom-to-a-service-agreement-or-service-order"></a>Notaðu sniðmátsuppskriftina í þjónustusamning eða þjónustupöntun

Þú getur notað sniðmátsuppskrift í þjónustusamning, þjónustupöntun eða bæði. Þjónustusamningurinn felur yfirleitt í sér langtímasamband við viðskiptavin. Endurnýjunarsagan sem skráð er í þjónustuuppskriftnni eru gagnlegar upplýsingar fyrir þjónustusamninginn.

Þú getur einnig nota sniðmátsuppskrift í þjónustupöntun til að skrá sögu þjónustunnar sem hefur verið framkvæmd á þjónustuhlut.

## <a name="copy-the-history-of-a-service-bom"></a>Afrita sögu þjónustuuppskriftar

Þú getur afritað sögu þjónustuuppskriftarlínu frá einum þjónustusamningi til annars. Með því að afrita þjónustusöguna milli þjónustusamninga geturðu varðveitt skrárnar yfir útskipti fyrir vöru.

**Dæmi**

Settur hefur verið upp þriggja ára þjónustusamningur fyrir bíl viðskiptavinar. Á því tímabili verður viðskiptavinurinn vanur þeirri góðu þjónustu sem fyrirtækið veitir. Þess vegna, eftir að samningurinn rennur út, vill viðskiptavinurinn setja upp nýjan. Þá er mögulegt að semja um hagstæðari kjör fyrir viðskiptavininn. Vegna þess að skráin yfir skipta íhluti gæti verið gagnleg í framtíðinni, afritar þú sögu þjónustuuppskriftar í nýja samninginn.

## <a name="modify-the-template-bom"></a>Breyta sniðmátsuppskrift

Ef sniðmátsuppskrift hefur ekki verið tengt við þjónustuhlut geturðu breytt eða eytt línum í henni. Eftir að sniðmátsuppskrift er tengd við þjónustuhlut geturðu aðeins breytt staðbundinni útgáfu af uppskriftinni. Ef ætlunin er að tvítaka uppsetningu staðbundinnar útgáfu af sniðmátsuppskrift er hægt að stofna nýja sniðmátsuppskrift, byggða á staðbundnu útgáfunni. Nánari upplýsingar er að finna í [Breyta þjónustuuppskrift](modify-service-bom.md).

Ef þú skiptir út vöru í uppskriftinni getur þú skráð skiptin á uppskriftarlínu í uppskriftarhönnuðinum. Valfrjálst er hægt að búa til þjónustupöntunarlínu fyrir skipta hlutinn. Ef þú býrð til þjónustupöntunarlínu geturðu reikningsfært vöruna sem kom í staðinn. Ef þú býrð ekki til þjónustupöntunarlínu fyrir skipti er skráningin á skiptunum geymd til að fylgjast með sögu þjónustuhlutarins.

## <a name="change-how-information-on-the-bom-line-is-displayed"></a>Breyttu hvernig upplýsingar á uppskriftarlínunni birtast

Þú getur breytt því hvernig upplýsingar á uppskriftarlínunni birtast fyrir öll sniðmát og þjónustuuppskriftir. Breytingarnar eru gerðar á öllum sniðmátsuppskriftum og þjónustuuppskriftum. Þetta á við um þær sem eru tengdar við þjónustuhluti.

## <a name="set-up-number-sequences-for-template-boms"></a>Setja upp númeraraðir fyrir sniðmátsuppskriftir

Til að nota sniðmátuppskriftir verður þú að setja upp tvær númeraraðir. Settu upp eina númeraröð fyrir sniðmátsuppskriftina og eina fyrir línunúmer uppskriftarsögunnar.


> [!NOTE]
> <P>Númeraraðir eru notaðar til að úthluta auðkennum til skráa sem þarfnast þeirra. Áður en þú getur úthlutar númeraröð til sniðmátsuppskriftar eða línunúmer uppskriftarsögu verður þú að setja upp kóða númeraraða.</P>


## <a name="set-up-number-sequences"></a>Setja upp númeraraðir

1.  Á listasíðunni **Númeraraðir** skaltu stofna númeraraðir fyrir sniðmátsuppskriftir og línunúmer uppskriftarsögu. 

2.  Smelltu á **Þjónustustjórnun** \> **Uppsetning** \> **Færibreytur þjónustustjórnunar**.

3.  Smelltu á **Númeraraðir** og veldu síðan kóða númeraraðar fyrir tilvísanir númeraraðarinnar sem þú stofnaðir í skjámyndinni **Númeraraðir**.

4.  Skjámyndinni er lokað til að vista breytingar.


> [!NOTE]
> <P>Línunúmer uppskriftarsögunnar er notað af kerfinu til að tengja færslur í uppskrfitarsögunni við þjónustusamning eða þjónustupöntun. Númerið birtist ekki í notendaviðmótinu.</P>



## <a name="see-also"></a>Sjá einnig

[Stofna sniðmátsuppskrift](create-template-bom.md)

[Stjórna sniðmátsuppskriftum í tengslum hluta](manage-template-boms-on-object-relations.md)

[Breyta þjónustuuppskrift](modify-service-bom.md)

 


