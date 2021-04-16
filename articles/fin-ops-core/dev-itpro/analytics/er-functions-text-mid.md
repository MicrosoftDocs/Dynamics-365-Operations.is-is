---
title: MID ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin MID í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
ms.date: 12/10/2019
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
ms.openlocfilehash: 9a9ff3f1055f6757d6d4073dbb816773d8bfc8ba
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746268"
---
# <a name="mid-er-function"></a><span data-ttu-id="c054c-103">MID ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="c054c-103">MID ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c054c-104">Aðgerðin `MID` skilar *strengjagildi* sem sýnir tilgreindan fjölda staftákna frá tilteknum streng, með upphafi í tilgreindri stöðu.</span><span class="sxs-lookup"><span data-stu-id="c054c-104">The `MID` function returns a *String* value that presents the specified number of characters from the specified string, starting at the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="c054c-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="c054c-105">Syntax</span></span>

```vb
MID (text, starting position, number of characters)
```

## <a name="arguments"></a><span data-ttu-id="c054c-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="c054c-106">Arguments</span></span>

<span data-ttu-id="c054c-107">`text`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="c054c-107">`text`: *String*</span></span>

<span data-ttu-id="c054c-108">Gildið *Strengur* sem tilgreinir textann sem á að skila staftáknum úr.</span><span class="sxs-lookup"><span data-stu-id="c054c-108">A *String* value that specifies the text to return characters from.</span></span>

<span data-ttu-id="c054c-109">`starting position`: *Heiltala*</span><span class="sxs-lookup"><span data-stu-id="c054c-109">`starting position`: *Integer*</span></span>

<span data-ttu-id="c054c-110">Gildið *Heiltala* sem tilgreinir staðsetningu fyrsta stafsins sem þarf að skila úr tilgreindum texta.</span><span class="sxs-lookup"><span data-stu-id="c054c-110">An *Integer* value that specifies the position of the first character that must be returned from the specified text.</span></span>

<span data-ttu-id="c054c-111">`number of characters`: *Heiltala*</span><span class="sxs-lookup"><span data-stu-id="c054c-111">`number of characters`: *Integer*</span></span>

<span data-ttu-id="c054c-112">Gildið *Heiltala* sem tilgreinir fjölda stafa sem þarf að skila, frá tilgreindri upphafsstöðu.</span><span class="sxs-lookup"><span data-stu-id="c054c-112">An *Integer* value that specifies the number of characters that must be returned, starting at the specified starting position.</span></span>

## <a name="return-values"></a><span data-ttu-id="c054c-113">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="c054c-113">Return values</span></span>

<span data-ttu-id="c054c-114">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="c054c-114">*String*</span></span>

<span data-ttu-id="c054c-115">Textagildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="c054c-115">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="c054c-116">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="c054c-116">Usage notes</span></span>

<span data-ttu-id="c054c-117">Ef gildi frumbreytunnar `starting position` er lægra en 0 (núll) eru stafirnir sem er skilað taldir frá fyrstu stöðu í tilgreindum streng.</span><span class="sxs-lookup"><span data-stu-id="c054c-117">If the value of the `starting position` argument is less than 0 (zero), the characters that are returned are counted from the first position in the specified string.</span></span>

<span data-ttu-id="c054c-118">Ef gildi frumbreytunnar `starting position` er lengra en tilgreindur strengur er tómum streng skilað.</span><span class="sxs-lookup"><span data-stu-id="c054c-118">If the value of the `starting position` argument exceeds length of the specified string, an empty string is returned.</span></span>

## <a name="example"></a><span data-ttu-id="c054c-119">Dæmi</span><span class="sxs-lookup"><span data-stu-id="c054c-119">Example</span></span>

<span data-ttu-id="c054c-120">`MID ("Sample", 2, 3)` skilar **"amp"**.</span><span class="sxs-lookup"><span data-stu-id="c054c-120">`MID ("Sample", 2, 3)` returns **"amp"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c054c-121">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="c054c-121">Additional resources</span></span>

[<span data-ttu-id="c054c-122">Textavirkni</span><span class="sxs-lookup"><span data-stu-id="c054c-122">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]