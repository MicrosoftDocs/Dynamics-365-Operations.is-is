---
title: Aðgerð Base64StringToContainer í rafrænni skýrslugerð
description: Þessi grein inniheldur upplýsingar um hvernig aðgerðin Base64StringToContainer í rafrænni skýrslugerð er notuð.
author: kfend
ms.date: 12/14/2020
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.17
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 96dfffc3d899f1106c6c931efb08c941f5b3c1a6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291235"
---
# <a name="base64stringtocontainer-er-function"></a>Aðgerð Base64StringToContainer í rafrænni skýrslugerð

[!include [banner](../includes/banner.md)]

`BASE64STRINGTOCONTAINER` [aðgerðin](er-formula-language.md#Functions) umbreytir tilteknum innslætti af gerðinni *Strengur* í gagnaatriði af gerðinni *[Gámur](er-functions-category-container.md)*.

## <a name="syntax"></a>Málskipun

```vb
BASE64STRINGTOCONTAINER (input)
```

## <a name="arguments"></a>Frumbreytur

`input`: *Strengur*

Gild slóð í gagnagjafa af gerðinni *Strengur*.

## <a name="return-values"></a>Skilagildi

*Gámur*

Tvíundargildið sem kemur út á BLOB-sniði.

## <a name="usage-notes"></a>Notkunarbréf

Undantekningin „Færibreyta er ekki gild“ er notuð ef inntaksstrengurinn kemur ekki með réttan Base64-flokk af kóðunarskema tvíundar til texta.

## <a name="example"></a>Dæmi

Þú skilgreinir eftirfarandi gagnagjafa í líkanavörpun þinni:

- Rót gagnagjafans **DocuTypeGroupEnum** af gerðinni *Dynamics 365 for Operations / Tölusetning* sem vísar í tölusetningu **DocuTypeGroup** forrits.
- Rót gagnagjafans **Viðskiptavinur** af gerðinni *Dynamics 365 for Operations / Töflufærslur* sem vísar í forritstöfluna **CustTable**.
- Gagnagjafinn **\#Geymslumiðill** af gerðinni *Reiknaður reitur* sem er skilgreindur á eftirfarandi hátt:

    - Honum er bætt við sem undireiningu gagnagjafa fyrir gagnagjafann **Viðskiptavinur**.
    - Hann inniheldur segðina `WHERE(@.'<Relations'.'<Documents', @.'<Relations'.'<Documents'.'docuType()'.TypeGroup = DocuTypeGroupEnum.Image)`.

- Gagnagjafinn **\#MediaAsBase64String** af gerðinni *Reiknaður reitur* sem er skilgreindur á eftirfarandi hátt:

    - Honum er bætt við sem undireiningu gagnagjafa fyrir gagnagjafann **Customer.'\#Media'**.
    - Hann inniheldur segðina `Customer.'#Media'.'getFileContentAsBase64String()'`.

- Gagnagjafinn **\#BlobFomBase64** af gerðinni *Reiknaður reitur* sem er skilgreindur á eftirfarandi hátt:

    - Honum er bætt við sem undireiningu gagnagjafa fyrir gagnagjafann **Customer.'\#Media'**.
    - Hann inniheldur segðina `Base64StringToContainer(Customer.'#Media'.'#MediaAsBase64String')'`.

Í þessu dæmi er kóðar gagnagjafinn **\#MediaAsBase64String** tvíundarefnið núverandi viðhengis geymslumiðils sem texta sem stendur fyrir Base64-flokk fyrir skema tvíundar í texta. Gagnagjafinn **\#BlobFomBase64** afkóðar Base64-strenginn og skilar tvíundargildi á BLOB-sniði.

![Sýnishorn af gagnagjöfum á hönnunarsíðu líkanavörpunar rafrænnar skýrslugerðar.](./media/er-functions-container-base64stringtocontainer-1.png)

## <a name="additional-resources"></a>Frekari upplýsingar

[Gámaaðgerðir](er-functions-category-container.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
