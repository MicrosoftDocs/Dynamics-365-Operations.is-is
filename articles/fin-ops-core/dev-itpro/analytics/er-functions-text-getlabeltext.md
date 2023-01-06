---
title: GETLABELTEXT ER-fall
description: Í þessari grein er að finna upplýsingar um hvernig GETLABELTEXT rafræn skýrslugerðarvirkni (ER) er notuð.
author: kfend
ms.date: 03/18/2022
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2022-01-01
ms.dyn365.ops.version: AX 10.0.25
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: dad87548518b77f2def1cf2383a21607f45170e1
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285940"
---
# <a name="getlabeltext-er-function"></a>GETLABELTEXT ER-fall

[!include [banner](../includes/banner.md)]

`GETLABELTEXT` virknin leitar að tilteknu merki til að skila gildi *[Strengs](er-formula-supported-data-types-primitive.md#string)* sem stendur fyrir þýðingu á tilteknu merki á tilteknu tungumáli.

## <a name="syntax"></a>Málskipun

```vb
GETLABELTEXT (label id, language)
```

## <a name="arguments"></a>Frumbreytur

### <a name="label-id"></a>Merkimiðakenni

`label id`: *Strengur* eða *Miðakenni*

Gilt kenni fyrir eina af eftirfarandi merkjagerðum:

- Merkimiði [Rafræn skýrslugerð (ER)](general-electronic-reporting.md)
- Merkimiði Microsoft Dynamics 365 Finance

#### <a name="usage-notes"></a>Notkunarbréf

Aðeins er hægt að skilgreina þessa frumbreytu sem fasta með því að nota eitt af eftirfarandi studdum mynstrum:

- Fyrir merkingar rafrænnar skýrslugerðar:

    - `@"GER_LABEL:<LABEL ID>"`
    - `"GER_LABEL:<LABEL ID>"`

- Merkingar fyrir Finance:

    - `@"<LABEL ID>"`
    - `"<LABEL ID>"`

> [!NOTE]
> Á hönnunartíma eru villuboð vegna villuleitar sýnd á síðunni **[Formúluhönnuður](er-advanced-formula-editor.md)** ef ekkert merki finnst með því að nota uppgefið merkjakenni.

### <a name="language"></a>Tungumál

`language`: *Strengur*

Strengur sem táknar tungumálakóða.

#### <a name="usage-notes"></a>Notkunarbréf

Hægt er að skilgreina þessa frumbreytu annaðhvort sem textafasta eða sem slóð gagnagjafareits sem skilar gildi fyrir *Streng*.

> [!NOTE]
> Á hönnunartíma eru villuboð vegna villuleitar sýnd ef engin tungumálakóði finnst með því að nota uppgefna `language` frumbreytu þegar hún hefur verið skilgreind sem textafasti.
>
> Við keyrslu er þýðingu fyrir `EN-US` kerfistungumálið skilað fyrir tiltekið merki ef enginn tungumálakóði finnst með því að nota uppgefna `language` frumbreytu.

## <a name="return-values"></a>Skilagildi

*Strengur*

Textagildið sem verður til.

## <a name="example-1-system-label"></a><a name=example-1></a>Dæmi 1: Kerfismerki

Segðirnar `GETLABELTEXT (@"SYS70894", "en-us")` og `GETLABELTEXT ("SYS70894", "en-us")` skila enskri þýðingu „Ekkert til að prenta“ fyrir `@SYS70894` forritsmerkið.

## <a name="example-2-er-label"></a><a name=example-2></a>Dæmi 2:  merki rafrænnar skýrslugerðar

Þú byrjar að breyta [skilgreiningu](general-electronic-reporting.md#Configuration) rafrænnar skýrslugerðar sem hefur verið [afleidd](er-quick-start2-customize-report.md#DeriveProvidedFormat) úr skilgreiningunni **ISO20022-kreditfærsla (DE)**, færir inn nýjan gagnagjafa af gerðinni *[Reiknaður reitur](er-calculated-field-ds-performance.md)* og skilgreinir segðina `GETLABELTEXT(@"GER_LABEL:VendorName", "de")` fyrir þennan gagnagjafa. Í þessu tilfelli skilar gagnagjafinn við keyrslu þýsku þýðingunni „Kreditorenname“ fyrir merkið `@GER_LABEL:VendorName` í rafrænni skýrslugerð sem var upphaflega skilgreint í grunnskilgreiningunni **ISO20022-kreditfærsla (DE)** fyrir rafræna skýrslugerð.

## <a name="additional-resources"></a>Frekari upplýsingar

[Textaaðgerðir](er-functions-category-text.md)

[Hanna skýrslur á mörgum tungumálum í rafrænni skýrslugerð](er-design-multilingual-reports.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
