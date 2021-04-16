---
title: CHAR ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin CHAR í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a621328817171be7df0622507c84f5c6f6fe90a1
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746436"
---
# <a name="char-er-function"></a><span data-ttu-id="4ccc8-103">CHAR ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="4ccc8-103">CHAR ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4ccc8-104">Aðgerðin `CHAR` skilar *Strengja*-gildi sem sýnir stakt staftákn sem vísað er til af tilgreindu Unicode númerinu.</span><span class="sxs-lookup"><span data-stu-id="4ccc8-104">The `CHAR` function returns a *String* value that presents a single character that is referenced by the specified Unicode number.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ccc8-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="4ccc8-105">Syntax</span></span>

```vb
CHAR (number)
```

## <a name="arguments"></a><span data-ttu-id="4ccc8-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="4ccc8-106">Arguments</span></span>

<span data-ttu-id="4ccc8-107">`number`: *Heiltala*</span><span class="sxs-lookup"><span data-stu-id="4ccc8-107">`number`: *Integer*</span></span>

<span data-ttu-id="4ccc8-108">Tala sem samsvarar væntum stökum staf.</span><span class="sxs-lookup"><span data-stu-id="4ccc8-108">A number that corresponds to an expected single character.</span></span>

## <a name="return-values"></a><span data-ttu-id="4ccc8-109">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="4ccc8-109">Return values</span></span>

<span data-ttu-id="4ccc8-110">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="4ccc8-110">*String*</span></span>

<span data-ttu-id="4ccc8-111">Textagildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="4ccc8-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="4ccc8-112">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="4ccc8-112">Usage notes</span></span>

<span data-ttu-id="4ccc8-113">Strengurinn sem þessi aðgerð skilar veltur á kóðuninni sem er valin í yfireiningu **FILE** sniðsins.</span><span class="sxs-lookup"><span data-stu-id="4ccc8-113">The string that this function returns depends on the encoding that is selected in the parent **FILE** format element.</span></span> <span data-ttu-id="4ccc8-114">Fyrir lista yfir studdar kóðanir, sjá [Kóðunarflokkur](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="4ccc8-114">For a list of the supported encodings, see [Encoding class](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx).</span></span>

## <a name="example"></a><span data-ttu-id="4ccc8-115">Dæmi</span><span class="sxs-lookup"><span data-stu-id="4ccc8-115">Example</span></span>

<span data-ttu-id="4ccc8-116">`CHAR (255)` skilar **ÿ**.</span><span class="sxs-lookup"><span data-stu-id="4ccc8-116">`CHAR (255)` returns **"ÿ"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4ccc8-117">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="4ccc8-117">Additional resources</span></span>

[<span data-ttu-id="4ccc8-118">Textavirkni</span><span class="sxs-lookup"><span data-stu-id="4ccc8-118">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]