---
title: Studdar samsettar gagnagerðir fyrir formúlur rafrænnar skýrslugerðar
description: Í þessu efnisatriði er að finna upplýsingar um samsettar gagnagerðir sem eru studdar í formúlum rafrænnar skýrslugerðar.
author: NickSelin
ms.date: 06/02/2021
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 933c8211276c1335a6a81bf4a8cb1c3f270762d4
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/04/2022
ms.locfileid: "8689243"
---
# <a name="supported-composite-data-types-for-electronic-reporting-formulas"></a>Studdar samsettar gagnagerðir fyrir formúlur rafrænnar skýrslugerðar

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er að finna upplýsingar um samsettar gagnagerðir sem eru studdar í segðum [Rafrænnar skýrslugerðar](general-electronic-reporting.md). Samsettu gagnagerðirnar eru [klasi](#class), [geymsla](#container), [færsla](#record), [færslulisti](#record-list) og [hlutur](#object).

## <a name="class"></a><a name="class"></a>Klasi

Gagnagerðin *klasi* vísar til opins forritsklasa. Í rafrænni skýrslugerð er hún táknuð sem [*færsla*](#record) sem inniheldur aðskilinn reit fyrir hverja almenna aðferð klasans sem vísað er í. Þegar færibreytur eru stilltar fyrir kall aðferðarinnar þarf einnig að tilgreina nauðsynlegar frumbreytur af viðeigandi gerðum í segð rafrænnar skýrslugerðar sem er stillt til að kalla á aðferðina.

Í ER kortlagningu og sniðhlutum geturðu bætt við **bekk** gagnagjafi sem er sýndur sem gagnagjafi og sem skilar gildi á *bekk* gerð. Þessi gagnagjafi gefur upp almennar aðferðir klasans sem hægt er að kalla á við keyrslu.

> [!NOTE]
> Aðeins er hægt að kalla á aðferðir úr segðum rafrænnar skýrslugerðar sem skila gildi.
>
> Aðeins er hægt að kalla aðferðir sem eru með á bilinu núll til átta frumbreytur í segðum rafrænnar skýrslugerðar.

Sjálfgefið gildi *klasa* er **núll**.

Eftirfarandi mynd sýnir hvernig gagnagjafanum **Kerfisupplýsingar(xInfo)** af **Klasagerðinni** er bætt við til að búa til tilvik **xInfo** forritsklasans og kalla á **productName()** aðferðar hans til að fá heiti núverandi forrits. Heiti núverandi forrits er sótt á keyrslutíma með því að keyra `xInfo.productName` bindinguna sem var stillt fyrir reitinn **Hugbúnaðarheiti(SoftwareName)** í gagnalíkani rafrænnar skýrslugerðar. Þessi binding kallar á `productName()` aðferð **xInfo** forritsklasans sem er sýndur í núverandi líkanavörpun sem gagnagjafann **Kerfisupplýsingar(xInfo)**.

[![Gagnagjafi klasa skilgreindur í hönnuði líkanavörpunar rafrænnar skýrslugerðar.](./media/er-formula-supported-data-types-composite-class1.gif)](./media/er-formula-supported-data-types-composite-class1.gif)

Eftirfarandi skýringarmynd sýnir hvernig snið rafrænnar skýrslugerðar er stillt til að setja uppgefið heiti forrits í mynduð skjöl. Reiturinn **Hugbúnaðarheiti(SoftwareName)** í notuðu gagnalíkaninu var bundinn við **Strengjahlutann** sem er faldaður undir XML-eininguna **softwareUsed** í sniði rafrænnar skýrslugerðar. Heiti núverandi forrits er því sett við keyrslu í XML-eininguna **softwareUsed** í myndað skjal á XML-sniði.

[![Skipulag rafræns skjals á útleið skilgreint í sniði rafrænnar skýrslugerðar.](./media/er-formula-supported-data-types-composite-class2.png)](./media/er-formula-supported-data-types-composite-class2.png)

## <a name="container"></a><a name="container"></a>Gámur

Gagnagerðin *geymsla* geymir tvíundarefni. *Geymslugildi* er hægt að nota til að koma tilteknum upplýsingum úr geymslu til myndaðs skjals. Í ramma rafrænnar skýrslugerðar er þessi gagnagerð oft notuð til að koma miðlunarefni á borð við merki fyrirtækis í mynduð skjöl.

> [!NOTE]
> Þótt hægt sé að sýna allt miðlunarefni sem *geymslugildi*, standa ekki öll *geymslugildi* fyrir miðlunarefni. Þannig að ef snið rafrænnar skýrslugerðar er skilgreint til að nota *geymslu* til að koma mynd inn í mynduð skjöl, en *geymslan* sem vísað er í skilar ekki miðlunarefni, gæti undantekning sem líkist eftirfarandi dæmi verið sýnd: „Villa við framkvæmd kóða: Tvíund (hlutur), kallað á aðferð constructFromContainer með ógildum færibreytum.“

Sjálfgefið gildi *geymslu* er **núll**.

Á eftirfarandi mynd er sýnt hvernig reiturinn **Bitmap(mynd)** af gerðinni *Geymsla* er bundinn við gagnalíkansreitinn **Merki** í af gerðinni **Geymsla** í líkanavörpun **Sölureiknings**. Þessi binding gerir merki fyrirtækisins aðgengilegt fyrir hvaða snið rafrænnar skýrslugerðar sem er hannað fyrir rótarskilgreininguna **SalesInvoice** og notar þessa líkanavörpun á keyrslutíma.

[![Reitur af geymslugerðinni bundinn í hönnuði líkanavörpunar rafrænnar skýrslugerðar.](./media/er-formula-supported-data-types-composite-container.png)](./media/er-formula-supported-data-types-composite-container.png)

## <a name="record"></a><a name="record"></a>Færsla

*Færsla* er safn af nafngreindum reitum sem hver um sig tengist gildi af annaðhvort [frumstæðri](er-formula-supported-data-types-primitive.md) gagnagerð eða samsettri gagnagerð. Yfirleitt er *færsla* notuð til að tákna staka færslu í færslulista. Í þessu tilviki táknar hvert atriði einstaka reiti, aðferðir og tengsl.

Sjálfgefið gildi *færslu* er **autt**.

> [!NOTE]
> Þegar gildi reits í auðri *færslu* er sótt er sjálfgefnu gildi viðeigandi gagnagerðar skilað.

Hægt er að sækja *Færslu* með því að nota eftirfarandi aðgerðir:

- [FIRST](er-functions-list-first.md)
- [FIRSTORNULL](er-functions-list-firstornull.md)
- [EMPTYRECORD](er-functions-record-emptyrecord.md)
- [NULLCONTAINER](er-functions-record-nullcontainer.md)

Nánari upplýsingar um umbreytingu *færslugilda* er að finna í [Listi yfir aðgerðir rafrænnar skýrslugerðar í listaflokknum](er-functions-category-list.md).

## <a name="record-list"></a><a name="record-list"></a>Færslulisti

*Færslulisti* er listi yfir atriði af *færslugerðinni*. Yfirleitt er *færslulisti* notaður til að tákna listann yfir færslur sem hefur verið sóttur úr gagnagrunnstöflu.

Sjálfgefið er að færslur *færslulista* séu sóttar í réttri röð. Hægt er að nota aðgerðina [INDEX](er-functions-list-index.md) og tilgreina *heiltöluvísinn* til að fá aðgang að tiltekinni færslu.

Sjálfgefið gildi *færslulista* er **autt**. Hægt er að nota aðgerðina [ISEMPTY](er-functions-list-isempty.md) til að meta hvort *færslulisti* sé auður.

> [!NOTE]
> Ef *færslulisti* er auður leiða allar tilraunir til að sækja reitargildi fyrir *færslu* til þess að undantekning verður sýnd við keyrslu. Til að fá frekari upplýsingar um hvernig hægt er að koma í veg fyrir undantekningar við keyrslu af þessari gerð skal skoða [Taka tillit til tómra listatilvika](er-components-inspections.md#i9).

Hægt er að hefja *færslulista* með eftirfarandi aðgerðum:

- [ALLITEMS](er-functions-list-allitems.md)
- [ALLITEMSQUERY](er-functions-list-allitemsquery.md)
- [EMPTYLIST](er-functions-list-emptylist.md)
- [LISTI](er-functions-list-list.md)
- [LISTDISTINCT](er-functions-list-listdistinct.md)

Nánari upplýsingar um umbreytingu *færslulista* er að finna í [Listi yfir aðgerðir rafrænnar skýrslugerðar í listaflokknum](er-functions-category-list.md). Til að komast að því hvernig á að búa til atriði *færslulista* skal fylla þau með forritsgögnum og síðan nota gögnin til að mynda viðskiptaskjöl, sjá [Hanna nýja lausn rafrænnar skýrslugerðar til að prenta sérsniðna skýrslu](er-quick-start1-new-solution.md).

## <a name="object"></a><a name="object"></a>Hlutur

*Hlutur* vísar til ríkjandi tilviks *klasa*. Yfirleitt er *hlutur* hafinn í frumkóða. Hann er síðan sendur til líkanavörpunar rafrænnar skýrslugerðar og veitir upplýsingar um samhengi framkvæmdarinnar.

Sjálfgildi *hlutarins* er **núll**.

Eftirfarandi mynd sýnir hvernig gagnagjafanum **ReportDataContract** af gerðinni *Hlutur* er bætt við til að senda upplýsingar um myndaðan reikning frá upprunakóða yfir í líkanavörpun **Verkreiknings**. Sem dæmi er texti reikningstilviks sendur sem hluti af samhengi framkvæmdarinnar. Þessi texti er fenginn úr upprunakóðanum við keyrslu með því að keyra `ReportDataContract.parmInvoiceInstanceText` bindinguna sem var stillt fyrir **Athugasemdasvæðið** í líkanavörpun rafrænnar skýrslugerðar. Þessi binding kallar á `parmInvoiceInstanceText()` aðferð **PSAProjInvoiceContract** forritsklasans sem er sýndur í núverandi líkanavörpun sem gagnagjafinn **ReportDataContract**.

[![Gagnagjafi hlutar skilgreindur í hönnuði líkanavörpunar rafrænnar skýrslugerðar.](./media/er-formula-supported-data-types-composite-object.gif)](./media/er-formula-supported-data-types-composite-object.gif)

Til að komast að því hvernig á að senda upplýsingar um samhengi keyrslu frá upprunakóða til virkrar lausnar rafrænnar skýrslugerðar skal skoða [Þróa forritsgervinga til að kalla á hannaða skýrslu](er-quick-start1-new-solution.md#DevelopCustomCode).

## <a name="additional-resources"></a>Frekari upplýsingar

- [Yfirlit yfir rafræna skýrslugerð](general-electronic-reporting.md)
- [Formúlutungumál í rafrænni skýrslugerð](er-formula-language.md)
- [Studdar frumstæðar gagnagerðir](er-formula-supported-data-types-primitive.md)
