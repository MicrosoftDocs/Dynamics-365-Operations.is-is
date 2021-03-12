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
# <a name="base64stringtocontainer-er-function"></a><span data-ttu-id="1a9bd-103">Aðgerð Base64StringToContainer í rafrænni skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="1a9bd-103">Base64StringToContainer ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1a9bd-104">`BASE64STRINGTOCONTAINER` [aðgerðin](er-formula-language.md#functions) umbreytir tilteknum innslætti af gerðinni *Strengur* í gagnaatriði af gerðinni *[Gámur](er-functions-category-container.md)*.</span><span class="sxs-lookup"><span data-stu-id="1a9bd-104">The `BASE64STRINGTOCONTAINER` [function](er-formula-language.md#functions) converts the specified input of the *String* type to a data item of the *[Container](er-functions-category-container.md)* type.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a9bd-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="1a9bd-105">Syntax</span></span>

```vb
BASE64STRINGTOCONTAINER (input)
```

## <a name="arguments"></a><span data-ttu-id="1a9bd-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="1a9bd-106">Arguments</span></span>

<span data-ttu-id="1a9bd-107">`input`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="1a9bd-107">`input`: *String*</span></span>

<span data-ttu-id="1a9bd-108">Gild slóð í gagnagjafa af gerðinni *Strengur*.</span><span class="sxs-lookup"><span data-stu-id="1a9bd-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="1a9bd-109">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="1a9bd-109">Return values</span></span>

<span data-ttu-id="1a9bd-110">*Gámur*</span><span class="sxs-lookup"><span data-stu-id="1a9bd-110">*Container*</span></span>

<span data-ttu-id="1a9bd-111">Tvíundargildið sem kemur út á BLOB-sniði.</span><span class="sxs-lookup"><span data-stu-id="1a9bd-111">The resulting binary value in binary large object (BLOB) format.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="1a9bd-112">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="1a9bd-112">Usage notes</span></span>

<span data-ttu-id="1a9bd-113">Undantekningin „Færibreyta er ekki gild“ er notuð ef inntaksstrengurinn kemur ekki með réttan Base64-flokk af kóðunarskema tvíundar til texta.</span><span class="sxs-lookup"><span data-stu-id="1a9bd-113">The "Parameter is not valid" exception is thrown if the input string doesn't provide a correct Base64 group of binary-to-text encoding schemes.</span></span>

## <a name="example"></a><span data-ttu-id="1a9bd-114">Dæmi</span><span class="sxs-lookup"><span data-stu-id="1a9bd-114">Example</span></span>

<span data-ttu-id="1a9bd-115">Þú skilgreinir eftirfarandi gagnagjafa í líkanavörpun þinni:</span><span class="sxs-lookup"><span data-stu-id="1a9bd-115">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="1a9bd-116">Rót gagnagjafans **DocuTypeGroupEnum** af gerðinni *Dynamics 365 for Operations / Tölusetning* sem vísar í tölusetningu **DocuTypeGroup** forrits.</span><span class="sxs-lookup"><span data-stu-id="1a9bd-116">The root **DocuTypeGroupEnum** data source of the *Dynamics 365 for Operations / Enumeration* type that refers to the **DocuTypeGroup** application enumeration</span></span>
- <span data-ttu-id="1a9bd-117">Rót gagnagjafans **Viðskiptavinur** af gerðinni *Dynamics 365 for Operations / Töflufærslur* sem vísar í forritstöfluna **CustTable**.</span><span class="sxs-lookup"><span data-stu-id="1a9bd-117">The root **Customer** data source of the *Dynamics 365 for Operations / Table records* type that refers to the **CustTable** application table</span></span>
- <span data-ttu-id="1a9bd-118">Gagnagjafinn **\#Geymslumiðill** af gerðinni *Reiknaður reitur* sem er skilgreindur á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="1a9bd-118">The **\#Media** data source of the *Calculated field* type that is configured in the following way:</span></span>

    - <span data-ttu-id="1a9bd-119">Honum er bætt við sem undireiningu gagnagjafa fyrir gagnagjafann **Viðskiptavinur**.</span><span class="sxs-lookup"><span data-stu-id="1a9bd-119">It's added as a child data source of the **Customer** data source.</span></span>
    - <span data-ttu-id="1a9bd-120">Hann inniheldur segðina `WHERE(@.'<Relations'.'<Documents', @.'<Relations'.'<Documents'.'docuType()'.TypeGroup = DocuTypeGroupEnum.Image)`.</span><span class="sxs-lookup"><span data-stu-id="1a9bd-120">It contains the expression `WHERE(@.'<Relations'.'<Documents', @.'<Relations'.'<Documents'.'docuType()'.TypeGroup = DocuTypeGroupEnum.Image)`.</span></span>

- <span data-ttu-id="1a9bd-121">Gagnagjafinn **\#MediaAsBase64String** af gerðinni *Reiknaður reitur* sem er skilgreindur á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="1a9bd-121">The **\#MediaAsBase64String** data source of the *Calculated field* type that is configured in the following way:</span></span>

    - <span data-ttu-id="1a9bd-122">Honum er bætt við sem undireiningu gagnagjafa fyrir gagnagjafann **Customer.'\#Media'**.</span><span class="sxs-lookup"><span data-stu-id="1a9bd-122">It's added as a child data source of the **Customer.'\#Media'** data source.</span></span>
    - <span data-ttu-id="1a9bd-123">Hann inniheldur segðina `Customer.'#Media'.'getFileContentAsBase64String()'`.</span><span class="sxs-lookup"><span data-stu-id="1a9bd-123">It contains the expression `Customer.'#Media'.'getFileContentAsBase64String()'`.</span></span>

- <span data-ttu-id="1a9bd-124">Gagnagjafinn **\#BlobFomBase64** af gerðinni *Reiknaður reitur* sem er skilgreindur á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="1a9bd-124">The **\#BlobFomBase64** data source of the *Calculated field* type that is configured in the following way:</span></span>

    - <span data-ttu-id="1a9bd-125">Honum er bætt við sem undireiningu gagnagjafa fyrir gagnagjafann **Customer.'\#Media'**.</span><span class="sxs-lookup"><span data-stu-id="1a9bd-125">It's added as a child data source of the **Customer.'\#Media'** data source.</span></span>
    - <span data-ttu-id="1a9bd-126">Hann inniheldur segðina `Base64StringToContainer(Customer.'#Media'.'#MediaAsBase64String')'`.</span><span class="sxs-lookup"><span data-stu-id="1a9bd-126">It contains the expression `Base64StringToContainer(Customer.'#Media'.'#MediaAsBase64String')'`.</span></span>

<span data-ttu-id="1a9bd-127">Í þessu dæmi er kóðar gagnagjafinn **\#MediaAsBase64String** tvíundarefnið núverandi viðhengis geymslumiðils sem texta sem stendur fyrir Base64-flokk fyrir skema tvíundar í texta.</span><span class="sxs-lookup"><span data-stu-id="1a9bd-127">In this example, the **\#MediaAsBase64String** data source encodes the binary content of the current media attachment as text that represents a Base64 group of binary-to-text encoding schemes.</span></span> <span data-ttu-id="1a9bd-128">Gagnagjafinn **\#BlobFomBase64** afkóðar Base64-strenginn og skilar tvíundargildi á BLOB-sniði.</span><span class="sxs-lookup"><span data-stu-id="1a9bd-128">The **\#BlobFomBase64** data source decodes the Base64 string and returns a binary value in BLOB format.</span></span>

![Sýnishorn af gagnagjöfum á hönnunarsíðu líkanavörpunar rafrænnar skýrslugerðar.](./media/er-functions-container-base64stringtocontainer-1.png)

## <a name="additional-resources"></a><span data-ttu-id="1a9bd-130">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="1a9bd-130">Additional resources</span></span>

[<span data-ttu-id="1a9bd-131">Hólfaaðgerðir</span><span class="sxs-lookup"><span data-stu-id="1a9bd-131">Container functions</span></span>](er-functions-category-container.md)
