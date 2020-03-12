---
title: CHAR ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin CHAR í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 7813b0c6002e47aef6a8c119c72728a49584401b
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041230"
---
# <span data-ttu-id="8031f-103"><a name="CHAR">CHAR ER aðgerð</a></span><span class="sxs-lookup"><span data-stu-id="8031f-103"><a name="CHAR">CHAR ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8031f-104">Aðgerðin `CHAR` skilar *Strengja*-gildi sem sýnir stakt staftákn sem vísað er til af tilgreindu Unicode númerinu.</span><span class="sxs-lookup"><span data-stu-id="8031f-104">The `CHAR` function returns a *String* value that presents a single character that is referenced by the specified Unicode number.</span></span>

## <a name="syntax"></a><span data-ttu-id="8031f-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="8031f-105">Syntax</span></span>

```vb
CHAR (number)
```

## <a name="arguments"></a><span data-ttu-id="8031f-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="8031f-106">Arguments</span></span>

<span data-ttu-id="8031f-107">`number`: *Heiltala*</span><span class="sxs-lookup"><span data-stu-id="8031f-107">`number`: *Integer*</span></span>

<span data-ttu-id="8031f-108">Tala sem samsvarar væntum stökum staf.</span><span class="sxs-lookup"><span data-stu-id="8031f-108">A number that corresponds to an expected single character.</span></span>

## <a name="return-values"></a><span data-ttu-id="8031f-109">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="8031f-109">Return values</span></span>

<span data-ttu-id="8031f-110">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="8031f-110">*String*</span></span>

<span data-ttu-id="8031f-111">Textagildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="8031f-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="8031f-112">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="8031f-112">Usage notes</span></span>

<span data-ttu-id="8031f-113">Strengurinn sem þessi aðgerð skilar veltur á kóðuninni sem er valin í yfireiningu **FILE** sniðsins.</span><span class="sxs-lookup"><span data-stu-id="8031f-113">The string that this function returns depends on the encoding that is selected in the parent **FILE** format element.</span></span> <span data-ttu-id="8031f-114">Fyrir lista yfir studdar kóðanir, sjá [Kóðunarflokkur](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="8031f-114">For a list of the supported encodings, see [Encoding class](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx).</span></span>

## <a name="example"></a><span data-ttu-id="8031f-115">Dæmi</span><span class="sxs-lookup"><span data-stu-id="8031f-115">Example</span></span>

<span data-ttu-id="8031f-116">`CHAR (255)` skilar **ÿ**.</span><span class="sxs-lookup"><span data-stu-id="8031f-116">`CHAR (255)` returns **"ÿ"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8031f-117">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="8031f-117">Additional resources</span></span>

[<span data-ttu-id="8031f-118">Textavirkni</span><span class="sxs-lookup"><span data-stu-id="8031f-118">Text functions</span></span>](er-functions-category-text.md)
