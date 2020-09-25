---
title: FORMATELEMENTNAME ER aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin FORMATELEMENTNAME í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: e8be55d9a90e841d64288b0c618c0012912ddbab
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745634"
---
# <a name="formatelementname-er-function"></a><span data-ttu-id="0e332-103">FORMATELEMENTNAME ER aðgerð</span><span class="sxs-lookup"><span data-stu-id="0e332-103">FORMATELEMENTNAME ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0e332-104">Aðgerðin `FORMATELEMENTNAME` skilar *Strengja*-gildi sem táknar nafn á gildandi sniðmátsþætti rafrænnar skýrslugerðar (ER).</span><span class="sxs-lookup"><span data-stu-id="0e332-104">The `FORMATELEMENTNAME` function returns a *String* value that represents the name of the current Electronic reporting (ER) format's element.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e332-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="0e332-105">Syntax</span></span>

```vb
FORMATELEMENTNAME ()
```

## <a name="return-values"></a><span data-ttu-id="0e332-106">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="0e332-106">Return values</span></span>

<span data-ttu-id="0e332-107">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="0e332-107">*String*</span></span>

<span data-ttu-id="0e332-108">Textagildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="0e332-108">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="0e332-109">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="0e332-109">Usage notes</span></span>

<span data-ttu-id="0e332-110">Þessa aðgerð er hægt að kalla í ER-segðum sem voru stilltar fyrir eiginleikana **Heiti lykils fyrir söfnuð gögn** og **Gildi lykils fyrir söfnuð gögn** í ER-sniðsíhlut úr hópnum **Texti** sem er að finna undir hlutanum **Common\\File** þar sem kveikt er á valkostinum **Safna saman upplýsingum um framleiðslu**.</span><span class="sxs-lookup"><span data-stu-id="0e332-110">This function can be called in ER expressions that were configured for the **Collected data key name** and **Collected data key value** properties of an ER format component from the **Text** group that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

## <a name="example"></a><span data-ttu-id="0e332-111">Dæmi</span><span class="sxs-lookup"><span data-stu-id="0e332-111">Example</span></span>

<span data-ttu-id="0e332-112">Nánari upplýsingar um hvernig á að nota þessa aðgerð er að finna í [Rafræn skýrslugerð nota gögn sniðúttaks til að telja og leggja saman](tasks/er-format-counting-summing-1.md) leiðarvísir, sem er hluti af **Veita/þróa IT þjónustu/þáttum** viðskiptaferli.</span><span class="sxs-lookup"><span data-stu-id="0e332-112">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0e332-113">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="0e332-113">Additional resources</span></span>

[<span data-ttu-id="0e332-114">Gagnasöfnunaraðgerðir</span><span class="sxs-lookup"><span data-stu-id="0e332-114">Data collection functions</span></span>](er-functions-category-data-collection.md)
