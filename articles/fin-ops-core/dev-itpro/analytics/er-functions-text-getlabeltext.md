---
title: GETLABELTEXT ER virka
description: Þessi grein veitir upplýsingar um hvernig GETLABELTEXT rafræn skýrslugerð (ER) aðgerðin er notuð.
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
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285940"
---
# <a name="getlabeltext-er-function"></a>GETLABELTEXT ER virka

[!include [banner](../includes/banner.md)]

The`GETLABELTEXT` aðgerð leitar að ákveðnu merki til að skila a *[Strengur](er-formula-supported-data-types-primitive.md#string)* gildi sem táknar þýðingu tilgreinds merkimiðs á tilgreindu tungumáli.

## <a name="syntax"></a>Málskipun

```vb
GETLABELTEXT (label id, language)
```

## <a name="arguments"></a>Frumbreytur

### <a name="label-id"></a>Merkimiðakenni

`label id`:*Strengur* eða *Merki auðkenni*

Gilt auðkenni einnar af eftirfarandi tegundum merkimiða:

- [Rafræn skýrslugerð (ER)](general-electronic-reporting.md) merki
- Microsoft Dynamics 365 Fjármálamerki

#### <a name="usage-notes"></a>Notkunarbréf

Þessi rök er aðeins hægt að skilgreina sem fasta með því að nota eitt af eftirfarandi studdu mynstrum:

- Fyrir ER merki:

    - `@"GER_LABEL:<LABEL ID>"`
    - `"GER_LABEL:<LABEL ID>"`

- Fyrir fjármálamerki:

    - `@"<LABEL ID>"`
    - `"<LABEL ID>"`

> [!NOTE]
> Á hönnunartíma eru staðfestingarvilluskilaboð sýnd á **[Formúluhönnuður](er-advanced-formula-editor.md)** síðu ef enginn merkimiði er að finna með því að nota uppgefið auðkenni merkimiða.

### <a name="language"></a>Tungumál

`language`: *Strengur*

Strengur sem táknar tungumálakóða.

#### <a name="usage-notes"></a>Notkunarbréf

Hægt er að skilgreina þessa röksemdafærslu annað hvort sem textafasta eða sem slóð gagnagjafasviðs sem skilar a *Strengur* gildi.

> [!NOTE]
> Á hönnunartíma birtast staðfestingarvilluboð ef enginn tungumálakóði er að finna með því að nota meðfylgjandi`language` rök þegar það hefur verið skilgreint sem textafasti.
>
> Á keyrslutíma, þýðingin fyrir`EN-US` kerfistungumáli er skilað fyrir tiltekið merki ef enginn tungumálakóði hefur fundist með því að nota uppgefið`language` rök.

## <a name="return-values"></a>Skilagildi

*Strengur*

Textagildið sem verður til.

## <a name="example-1-system-label"></a><a name=example-1></a> Dæmi 1: Kerfismerki

Tjáningin`GETLABELTEXT (@"SYS70894", "en-us")` og`GETLABELTEXT ("SYS70894", "en-us")` skila ensku þýðingunni "Nothing to print" fyrir`@SYS70894` umsóknarmerki.

## <a name="example-2-er-label"></a><a name=example-2></a> Dæmi 2: ER merki

Þú byrjar að breyta ER [uppsetningu](general-electronic-reporting.md#Configuration) það hefur verið [afleidd](er-quick-start2-customize-report.md#DeriveProvidedFormat) frá **ISO20022 Kreditmillifærsla (DE)** stillingar, sláðu inn nýjan gagnagjafa *[Reiknaður reitur](er-calculated-field-ds-performance.md)* slá inn og stilla tjáninguna`GETLABELTEXT(@"GER_LABEL:VendorName", "de")` fyrir þennan gagnagjafa. Í þessu tilviki, á keyrslutíma, skilar gagnagjafinn þýsku þýðingunni „Kreditorenname“ fyrir`@GER_LABEL:VendorName` ER merki sem var upphaflega stillt í grunninn **ISO20022 Kreditmillifærsla (DE)** ER stillingar.

## <a name="additional-resources"></a>Frekari upplýsingar

[Textaaðgerðir](er-functions-category-text.md)

[Hanna skýrslur á mörgum tungumálum í rafrænni skýrslugerð](er-design-multilingual-reports.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
