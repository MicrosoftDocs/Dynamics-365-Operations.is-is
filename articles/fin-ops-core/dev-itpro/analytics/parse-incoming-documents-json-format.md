---
title: Þátta skjöl á innleið á JSON-sniði
description: Þetta efni skýrir hvernig á að setja upp rafræn skýrslugerðarsnið (ER) til að þátta skjöl á innleið í JavaScript Object Notation (JSON)-sniði.
author: kfend
manager: AnnBe
ms.date: 05/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: b4ed81bb5527ea8e02caaa1262a57960dd7cdf29
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685764"
---
# <a name="parse-incoming-documents-in-json-format"></a><span data-ttu-id="91fb7-103">Þátta skjöl á innleið á JSON-sniði</span><span class="sxs-lookup"><span data-stu-id="91fb7-103">Parse incoming documents in JSON format</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="91fb7-104">Hægt er að setja upp rafræn skýrslugerðarsnið (ER) til að þátta komandi rafræn skjöl sem tákna gögn á textasniði sem byggist á JavaScript (með öðrum orðum, skrár í JavaScript Object Notation \[JSON\]-sniði).</span><span class="sxs-lookup"><span data-stu-id="91fb7-104">You can design Electronic reporting (ER) formats to parse incoming electronic documents that represent data in a text format that is based on JavaScript (in other words, files in JavaScript Object Notation \[JSON\] format).</span></span>

<span data-ttu-id="91fb7-105">Til að læra meira um þennan eiginleika skaltu hlaða niður skrám í eftirfarandi töflu og spila síðan ER Stofna sniðmátsskilgreiningu til að flytja inn gögn úr utanaðkomandi JSON-skráarleiðbeiningar.</span><span class="sxs-lookup"><span data-stu-id="91fb7-105">To learn more about this feature, download the files in the following table, and then play the ER Create a format configuration to import data from an external JSON file task guide.</span></span> <span data-ttu-id="91fb7-106">Þetta verkefni fylgja sýnir hvernig hægt er að nota ER snið til að flokka innkominn JSON-skrá til að uppfæra forritsgögn.</span><span class="sxs-lookup"><span data-stu-id="91fb7-106">This task guide shows how an ER format can be used to parse an incoming JSON file to update application data.</span></span>

| <span data-ttu-id="91fb7-107">Titill</span><span class="sxs-lookup"><span data-stu-id="91fb7-107">Title</span></span>                                  | <span data-ttu-id="91fb7-108">Skrárnafn</span><span class="sxs-lookup"><span data-stu-id="91fb7-108">File name</span></span> |
|----------------------------------------|-----------|
| <span data-ttu-id="91fb7-109">ER Sníða skilgreiningu</span><span class="sxs-lookup"><span data-stu-id="91fb7-109">ER format configuration</span></span>                | [<span data-ttu-id="91fb7-110">Snið fyrir innflutning trans_JSON.xml lánardrottins</span><span class="sxs-lookup"><span data-stu-id="91fb7-110">Format for importing vendors' trans_JSON.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=874111) |
| <span data-ttu-id="91fb7-111">Sýni af móttekinni skrá á .csv-sniði</span><span class="sxs-lookup"><span data-stu-id="91fb7-111">Sample of incoming file in .csv format</span></span> | [<span data-ttu-id="91fb7-112">1099entries_JSON.txt</span><span class="sxs-lookup"><span data-stu-id="91fb7-112">1099entries_JSON.txt</span></span>](https://go.microsoft.com/fwlink/?linkid=874111) |

## <a name="requirements"></a><span data-ttu-id="91fb7-113">Þarfir</span><span class="sxs-lookup"><span data-stu-id="91fb7-113">Requirements</span></span>

<span data-ttu-id="91fb7-114">Áður en þú klárar ER Stofna sniðstillingu til að flytja inn gögn úr utanaðkomandi JSON-skráarleiðbeiningum, verður að uppfylla eftirfarandi krafa:</span><span class="sxs-lookup"><span data-stu-id="91fb7-114">Before you complete the ER Create a format configuration to import data from an external JSON file task guide, the following requirement must be met:</span></span>

- <span data-ttu-id="91fb7-115">Yfireiningar í JSON-skránni geta aðeins verið hlutaeiningar.</span><span class="sxs-lookup"><span data-stu-id="91fb7-115">Parent elements in the JSON file can be only object elements.</span></span>
- <span data-ttu-id="91fb7-116">Faldaðar einingar fyrir hlut eiga að vera eiginleikaeiningar, svo að gilt JSON-skipulag sé búið til.</span><span class="sxs-lookup"><span data-stu-id="91fb7-116">Nested elements for an object should be property elements, so that a valid JSON structure is created.</span></span>
- <span data-ttu-id="91fb7-117">JSON-fylki geta aðeins verið faldaðar einingar í eiginleikaeiningum hlutar.</span><span class="sxs-lookup"><span data-stu-id="91fb7-117">JSON arrays can be only nested elements of the property elements of an object.</span></span>
- <span data-ttu-id="91fb7-118">JSON-fylki geta aðeins innihaldið JSON-hluti.</span><span class="sxs-lookup"><span data-stu-id="91fb7-118">JSON arrays can contain only JSON objects.</span></span> <span data-ttu-id="91fb7-119">Þau geta ekki innihaldið bein strengja-/tölugildi og faldaðar fylkingar.</span><span class="sxs-lookup"><span data-stu-id="91fb7-119">They can't contain direct string/numeric values and nested arrays.</span></span> <span data-ttu-id="91fb7-120">Einingar í þessum fylkjum verða þáttaðar í röð, eins og þær eru tilgreindar í forminu.</span><span class="sxs-lookup"><span data-stu-id="91fb7-120">Elements in these arrays will be parsed in order, as they are specified in the format.</span></span> <span data-ttu-id="91fb7-121">Tekið verður tillit til margfeldisstillinga á hvern JSON-hlut.</span><span class="sxs-lookup"><span data-stu-id="91fb7-121">Multiplicity settings on each JSON object will be considered.</span></span>

<span data-ttu-id="91fb7-122">Að auki verður þú að ljúka verkleiðbeiningunum [ER Stofna nauðsynlegar skilgreiningar til að flytja inn gögn úr utanaðkomandi skrá](tasks/er-required-configurations-import-data.md) ef þú hefur ekki þegar lokið þeim.</span><span class="sxs-lookup"><span data-stu-id="91fb7-122">Additionally, you must complete the [ER Create required configurations to import data from an external file](tasks/er-required-configurations-import-data.md) task guide if you haven't already completed it.</span></span> <span data-ttu-id="91fb7-123">Sæktu eftirfarandi skrá til að ljúka verkefnaleiðbeiningunni.</span><span class="sxs-lookup"><span data-stu-id="91fb7-123">Download the following file to complete the task guide.</span></span>

| <span data-ttu-id="91fb7-124">Titill</span><span class="sxs-lookup"><span data-stu-id="91fb7-124">Title</span></span>                  | <span data-ttu-id="91fb7-125">Skrárnafn</span><span class="sxs-lookup"><span data-stu-id="91fb7-125">File name</span></span> |
|------------------------|-----------|
| <span data-ttu-id="91fb7-126">Líkanaskilgreining rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="91fb7-126">ER model configuration</span></span> | [<span data-ttu-id="91fb7-127">1099model.xml</span><span class="sxs-lookup"><span data-stu-id="91fb7-127">1099model.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=874111) |
