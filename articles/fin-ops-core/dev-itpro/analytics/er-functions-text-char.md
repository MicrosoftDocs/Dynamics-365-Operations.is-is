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
ms.openlocfilehash: f83dfe19e442b9e81d63a2b1dd3dd44aa2f594bc
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891184"
---
# <a name="char-er-function"></a><span data-ttu-id="1e199-103">CHAR ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="1e199-103">CHAR ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1e199-104">Aðgerðin `CHAR` skilar *Strengja*-gildi sem sýnir stakt staftákn sem vísað er til af tilgreindu Unicode númerinu.</span><span class="sxs-lookup"><span data-stu-id="1e199-104">The `CHAR` function returns a *String* value that presents a single character that is referenced by the specified Unicode number.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e199-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="1e199-105">Syntax</span></span>

```vb
CHAR (number)
```

## <a name="arguments"></a><span data-ttu-id="1e199-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="1e199-106">Arguments</span></span>

<span data-ttu-id="1e199-107">`number`: *Heiltala*</span><span class="sxs-lookup"><span data-stu-id="1e199-107">`number`: *Integer*</span></span>

<span data-ttu-id="1e199-108">Tala sem samsvarar væntum stökum staf.</span><span class="sxs-lookup"><span data-stu-id="1e199-108">A number that corresponds to an expected single character.</span></span>

## <a name="return-values"></a><span data-ttu-id="1e199-109">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="1e199-109">Return values</span></span>

<span data-ttu-id="1e199-110">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="1e199-110">*String*</span></span>

<span data-ttu-id="1e199-111">Textagildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="1e199-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="1e199-112">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="1e199-112">Usage notes</span></span>

<span data-ttu-id="1e199-113">Strengurinn sem þessi aðgerð skilar veltur á kóðuninni sem er valin í yfireiningu **FILE** sniðsins.</span><span class="sxs-lookup"><span data-stu-id="1e199-113">The string that this function returns depends on the encoding that is selected in the parent **FILE** format element.</span></span> <span data-ttu-id="1e199-114">Fyrir lista yfir studdar kóðanir, sjá [Kóðunarflokkur](/dotnet/api/system.text.encoding).</span><span class="sxs-lookup"><span data-stu-id="1e199-114">For a list of the supported encodings, see [Encoding class](/dotnet/api/system.text.encoding).</span></span>

## <a name="example"></a><span data-ttu-id="1e199-115">Dæmi</span><span class="sxs-lookup"><span data-stu-id="1e199-115">Example</span></span>

<span data-ttu-id="1e199-116">`CHAR (255)` skilar **ÿ**.</span><span class="sxs-lookup"><span data-stu-id="1e199-116">`CHAR (255)` returns **"ÿ"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1e199-117">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="1e199-117">Additional resources</span></span>

[<span data-ttu-id="1e199-118">Textavirkni</span><span class="sxs-lookup"><span data-stu-id="1e199-118">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]