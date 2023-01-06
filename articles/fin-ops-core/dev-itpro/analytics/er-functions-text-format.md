---
title: FORMAT ER-aðgerð
description: Í þessari grein er að finna upplýsingar um hvernig FORMAT rafræn skýrslugerðarvirkni (ER) er notuð.
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
ms.openlocfilehash: a7eb3d4a4c72e8faf40d28a724cda5ba7d7e8a47
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286000"
---
# <a name="format-er-function"></a>FORMAT ER-aðgerð

[!include [banner](../includes/banner.md)]

Aðgerðin `FORMAT` skilar tilgreindum streng sem *strengja*-gildi eftir að hann hefur verið sniðinn með því að skipta út öllum tilvikum af **%N** með *n* tu frumbreytunni.

## <a name="syntax"></a>Málskipun

```vb
FORMAT (string, argument 1[, argument 2, …, argument N])
```

## <a name="arguments"></a>Frumbreytur

`string`: *Strengur*

Tilvísun í gagnagjafa af gerðinni *Strengur* sem verður að forsníða. Þessi frumbreyta er áskilin.

`argument 1`: *Strengur*

Fyrsta frumbreytan, sem er notuð til að koma í staðinn fyrir **%1**. Þessi frumbreyta er áskilin.

`argument N`: *Strengur*

Fyrsta *N* ta frumbreytan, sem er notuð til að koma í staðinn fyrir **%2**, **%3** o.s.frv. Þessar viðbótarfrumbreytur eru valkvæðar.

## <a name="return-values"></a>Skilagildi

*Strengur*

Textagildið sem verður til.

## <a name="usage-notes"></a>Notkunarbréf

Ef frumbreyta er ekki gefin upp fyrir færibreytu, er færibreytan skilað sem **"%N"** í strengnum. Fyrir gildi í af gerðinni *rauntala* takmarkast sjálfgefin umbreyting strengs við sem nemur tveimur tugasætum.

## <a name="example"></a>Dæmi

Í eftirfarandi mynd skilar gagnagjafninn **PaymentModel** lista yfir skrár viðskiptavina með því að nota íhlutinn **Viðskiptavinur**. Það skilar gildi vinnsludags með því að nota reitinn **ProcessingDate**.

<a href="./media/picture-format-datasource.jpg"><img src="./media/picture-format-datasource.jpg" alt="PaymentModel data source" class="alignnone wp-image-290751 size-full" width="293" height="143" /></a>

Í sniði rafrænnar skýrslugerðar (ER) sem er hannað til að mynda rafræna skrá fyrir valda viðskiptavini er **PaymentModel** valið sem gagnagjafi og það stýrir flæði ferlis. Ef valinn viðskiptavinur hefur hætt á deginum sem skýrslan er unnin er undantekningu beitt til að upplýsa notandann. Formúlu sem er hannað fyrir þessa gerð vinnslustýringar getur notað eftirfarandi tilföng:

- Merki SYS70894 sem hefur eftirfarandi texta:

    - **Fyrir tungumál EN-US:** "Ekkert til að prenta"
    - **Fyrir tungumálið DE:** "Nichts zu drucken"

- Merki SYS18389 sem hefur eftirfarandi texta:

    - **Fyrir tungumál EN-US:** "Customer %1 is stopped for %2."
    - **Fyrir tungumálið DE:** "Debitor '%1' wird für %2 gesperrt."

Hér er segðin sem hægt er að hanna.

```vb
FORMAT (CONCATENATE (@"SYS70894", ". ", @"SYS18389"), model.Customer.Name, DATETIMEFORMAT (model.ProcessingDate, "d"))
```

Ef skýrsla er unnin fyrir **Litware Retail** viðskiptavin 17. desember 2015, í **EN-US** menningu og **EN-US** tungumáli, skilar þessi formúla eftirfarandi texta, sem hægt er að birta fyrir notandann sem undantekningarskilaboð:

*Nothing to print. Customer Litware Retail is stopped for 12/17/2015.*

Ef sama skýrslan er unnin fyrir viðskiptavininn **Litware Retail** þann 17. desember 2015 í menningunni **DE** og tungumálinu **DE** skilar formúlan eftirfarandi texta, sem notar annað snið dagsetningar:

*Nichts zu drucken. Debitor 'Litware Retail' wird für 17.12.2015 gesperrt.*

>[!NOTE]
> Eftirfarandi setningafræði er beitt í formúlum rafrænnar skýrslugerðar fyrir merki:
>
> - **Fyrir merki úr tilföngum Microsoft Dynamics 365 Finance-forritinu:** **\@X**, þar sem **X** merkjakennið í hugbúnaðarhlutatrénu (AOT)
> - **Fyrir merki sem eru í ER-skilgreiningum:** **@GER_LABEL:X"**, þar sem **X** er merkjakenni í ER-skilgreiningu

## <a name="additional-resources"></a>Frekari upplýsingar

[Textavirkni](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
