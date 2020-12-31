---
title: Listi yfir ER-aðgerðir í gagnasafnsflokknum
description: Þetta efni veitir upplýsingar um gagnasafnsaðgerðir sem eru studdar í rafrænni skýrslugerð (ER).
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0ec6092f2992df91433bb8aaa4212fca2a0abf7c
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686294"
---
# <a name="list-of-er-functions-in-the-data-collection-category"></a><span data-ttu-id="22665-103">Listi yfir ER-aðgerðir í gagnasafnsflokknum</span><span class="sxs-lookup"><span data-stu-id="22665-103">List of ER functions in the data collection category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="22665-104">Gagnasafnsaðgerðir rafrænna skýrslugerða (ER) eru notaðar til að telja og leggja saman á ER-sniði sem er verið að keyra, byggt á gögnum um frálags sem þegar er búið til á sniðinu **Texti** eða **Xml**.</span><span class="sxs-lookup"><span data-stu-id="22665-104">Electronic reporting (ER) data collection functions are used to do counting and summing in an ER format that is being run, based on data of the output that has already been generated in **Text** or **Xml** format.</span></span> <span data-ttu-id="22665-105">Þessi aðferð er notuð til að bæta afköst ER-sniðs sem er keyrt, til að færa inn gildi hlaupatölur í mynduðum skjölum og í öðrum tilgangi.</span><span class="sxs-lookup"><span data-stu-id="22665-105">This approach is used to help improve performance of an ER format that is run, to enter values of running totals in generated documents, and for other purposes.</span></span> <span data-ttu-id="22665-106">Þetta efni gefur yfirlit yfir þessar aðgerðir.</span><span class="sxs-lookup"><span data-stu-id="22665-106">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="22665-107">Listi yfir studdar aðgerðir</span><span class="sxs-lookup"><span data-stu-id="22665-107">List of supported functions</span></span>

| <span data-ttu-id="22665-108">Aðgerð</span><span class="sxs-lookup"><span data-stu-id="22665-108">Function</span></span> | <span data-ttu-id="22665-109">Lýsing</span><span class="sxs-lookup"><span data-stu-id="22665-109">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="22665-110">CollectedList</span><span class="sxs-lookup"><span data-stu-id="22665-110">CollectedList</span></span>](er-functions-datacollection-collectedlist.md) | <span data-ttu-id="22665-111">Þessi aðgerð skilar *Skráalista*-gildi sem inniheldur lista yfir gildi sem skilað var af eiginleikanum **Gildi lykils fyrir söfnuð gögn** í sniðþáttum og safnað þegar sniðþættirnir voru notaðir til að búa til útleiðarskjal við sniðkeyrsluna og sem fullnægir tilgreindum skilyrðum.</span><span class="sxs-lookup"><span data-stu-id="22665-111">This function returns a *Record list* value that contains the list of values that were returned by the **Collected data key value** property of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="22665-112">Hvert skilyrði samanstendur af lykilsviði og lykilgildi.</span><span class="sxs-lookup"><span data-stu-id="22665-112">Each condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="22665-113">CountIF</span><span class="sxs-lookup"><span data-stu-id="22665-113">CountIF</span></span>](er-functions-datacollection-countif.md) | <span data-ttu-id="22665-114">Þessi aðgerð skilar *Heiltölu*-gildi sem táknar fjölda sniðaþátta sem var safnað þegar sniðþættirnir voru notaðir til að búa til útleiðarskjal við sniðkeyrsluna og sem fullnægir tilgreindu skilyrði.</span><span class="sxs-lookup"><span data-stu-id="22665-114">This function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="22665-115">Skilyrðið samanstendur af lykilsviði og lykilgildi.</span><span class="sxs-lookup"><span data-stu-id="22665-115">The condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="22665-116">CountIFs</span><span class="sxs-lookup"><span data-stu-id="22665-116">CountIFs</span></span>](er-functions-datacollection-countifs.md) | <span data-ttu-id="22665-117">Þessi aðgerð skilar *Heiltölu*-gildi sem táknar fjölda sniðaþátta sem var safnað þegar sniðþættirnir voru notaðir til að búa til útleiðarskjal við sniðkeyrsluna og sem fullnægir tilgreindum skilyrðum.</span><span class="sxs-lookup"><span data-stu-id="22665-117">This function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="22665-118">Hvert skilyrði samanstendur af lykilsviði og lykilgildi.</span><span class="sxs-lookup"><span data-stu-id="22665-118">Each condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="22665-119">FormatElementName</span><span class="sxs-lookup"><span data-stu-id="22665-119">FormatElementName</span></span>](er-functions-datacollection-formatelementname.md) | <span data-ttu-id="22665-120">Þessi aðgerð skilar *Strengjagildi* sem táknar nafn á gildandi ER-sniðmátsþætti.</span><span class="sxs-lookup"><span data-stu-id="22665-120">This function returns a *String* value that represents the name of the current ER format's element.</span></span> |
| [<span data-ttu-id="22665-121">SumIF</span><span class="sxs-lookup"><span data-stu-id="22665-121">SumIF</span></span>](er-functions-datacollection-sumif.md) | <span data-ttu-id="22665-122">Þessi aðgerð skilar *Raungildi* sem táknar summu gilda sem var skilað af bindingum sniðaþátta og safnað þegar sniðþættirnir voru notaðir til að búa til útleiðarskjal við sniðkeyrsluna og sem fullnægir tilgreindu skilyrði.</span><span class="sxs-lookup"><span data-stu-id="22665-122">This function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="22665-123">Skilyrðið samanstendur af lykilsviði og lykilgildi.</span><span class="sxs-lookup"><span data-stu-id="22665-123">The condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="22665-124">SumIFs</span><span class="sxs-lookup"><span data-stu-id="22665-124">SumIFs</span></span>](er-functions-datacollection-sumifs.md) | <span data-ttu-id="22665-125">Þessi aðgerð skilar *Raungildi* sem táknar summu gilda sem var skilað af bindingum sniðaþátta og safnað þegar sniðþættirnir voru notaðir til að búa til útleiðarskjal við sniðkeyrsluna og sem fullnægir tilgreindum skilyrðum.</span><span class="sxs-lookup"><span data-stu-id="22665-125">This function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="22665-126">Hvert skilyrði samanstendur af lykilsviði og lykilgildi.</span><span class="sxs-lookup"><span data-stu-id="22665-126">Each condition consists of a key range and a key value.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="22665-127">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="22665-127">Additional resources</span></span>

[<span data-ttu-id="22665-128">Yfirlit yfir rafræna skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="22665-128">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="22665-129">Formúluhönnuður í rafrænni skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="22665-129">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="22665-130">Formúlutungumál í rafrænni skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="22665-130">Electronic reporting formula language</span></span>](er-formula-language.md)
