---
title: Aðgerð Base64StringToContainer í rafrænni skýrslugerð
description: Þetta efnisatriði inniheldur upplýsingar um hvernig aðgerðin Base64StringToContainer í rafrænni skýrslugerð er notuð.
author: NickSelin
manager: kfend
ms.date: 12/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 0e92ae41a3e0f03cb14d4791ab768f096f2a0523
ms.sourcegitcommit: e8a46e127d70986539c138b27a641bff6f6874d0
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/15/2020
ms.locfileid: "4739086"
---
# <a name="base64stringtocontainer-er-function"></a>Aðgerð Base64StringToContainer í rafrænni skýrslugerð

[!include [banner](../includes/banner.md)]

`BASE64STRINGTOCONTAINER` [aðgerðin](er-formula-language.md#functions) umbreytir tilteknum innslætti af gerðinni *Strengur* í gagnaatriði af gerðinni *[Gámur](er-functions-category-container.md)*.

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

[Hólfaaðgerðir](er-functions-category-container.md)
