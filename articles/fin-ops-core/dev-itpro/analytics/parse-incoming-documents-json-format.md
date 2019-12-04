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
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 8be4e225507a18a92d642ff0f3a6ca3d0ff68564
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772536"
---
# <a name="parse-incoming-documents-in-json-format"></a><span data-ttu-id="338f6-103">Þátta skjöl á innleið á JSON-sniði</span><span class="sxs-lookup"><span data-stu-id="338f6-103">Parse incoming documents in JSON format</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="338f6-104">Hægt er að setja upp rafræn skýrslugerðarsnið (ER) til að þátta komandi rafræn skjöl sem tákna gögn á textasniði sem byggist á JavaScript (með öðrum orðum, skrár í JavaScript Object Notation \[JSON\]-sniði).</span><span class="sxs-lookup"><span data-stu-id="338f6-104">You can design Electronic reporting (ER) formats to parse incoming electronic documents that represent data in a text format that is based on JavaScript (in other words, files in JavaScript Object Notation \[JSON\] format).</span></span>

<span data-ttu-id="338f6-105">Til að læra meira um þennan eiginleika skaltu hlaða niður skrám í eftirfarandi töflu og spila síðan ER Stofna sniðmátsskilgreiningu til að flytja inn gögn úr utanaðkomandi JSON-skráarleiðbeiningar.</span><span class="sxs-lookup"><span data-stu-id="338f6-105">To learn more about this feature, download the files in the following table, and then play the ER Create a format configuration to import data from an external JSON file task guide.</span></span> <span data-ttu-id="338f6-106">Þetta verkefni fylgja sýnir hvernig hægt er að nota ER snið til að flokka innkominn JSON-skrá til að uppfæra forritsgögn.</span><span class="sxs-lookup"><span data-stu-id="338f6-106">This task guide shows how an ER format can be used to parse an incoming JSON file to update application data.</span></span>

| <span data-ttu-id="338f6-107">Titill</span><span class="sxs-lookup"><span data-stu-id="338f6-107">Title</span></span>                                  | <span data-ttu-id="338f6-108">Skrárnafn</span><span class="sxs-lookup"><span data-stu-id="338f6-108">File name</span></span> |
|----------------------------------------|-----------|
| <span data-ttu-id="338f6-109">ER Sníða skilgreiningu</span><span class="sxs-lookup"><span data-stu-id="338f6-109">ER format configuration</span></span>                | [<span data-ttu-id="338f6-110">Snið fyrir innflutning trans_JSON.xml lánardrottins</span><span class="sxs-lookup"><span data-stu-id="338f6-110">Format for importing vendors' trans_JSON.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=874111) |
| <span data-ttu-id="338f6-111">Sýni af móttekinni skrá á .csv-sniði</span><span class="sxs-lookup"><span data-stu-id="338f6-111">Sample of incoming file in .csv format</span></span> | [<span data-ttu-id="338f6-112">1099entries_JSON.txt</span><span class="sxs-lookup"><span data-stu-id="338f6-112">1099entries_JSON.txt</span></span>](https://go.microsoft.com/fwlink/?linkid=874111) |

## <a name="requirements"></a><span data-ttu-id="338f6-113">Þarfir</span><span class="sxs-lookup"><span data-stu-id="338f6-113">Requirements</span></span>

<span data-ttu-id="338f6-114">Áður en þú klárar ER Stofna sniðstillingu til að flytja inn gögn úr utanaðkomandi JSON-skráarleiðbeiningum, verður að uppfylla eftirfarandi krafa:</span><span class="sxs-lookup"><span data-stu-id="338f6-114">Before you complete the ER Create a format configuration to import data from an external JSON file task guide, the following requirement must be met:</span></span>

- <span data-ttu-id="338f6-115">Yfireiningar í JSON-skránni geta aðeins verið hlutaeiningar.</span><span class="sxs-lookup"><span data-stu-id="338f6-115">Parent elements in the JSON file can be only object elements.</span></span>
- <span data-ttu-id="338f6-116">Faldaðar einingar fyrir hlut eiga að vera eiginleikaeiningar, svo að gilt JSON-skipulag sé búið til.</span><span class="sxs-lookup"><span data-stu-id="338f6-116">Nested elements for an object should be property elements, so that a valid JSON structure is created.</span></span>
- <span data-ttu-id="338f6-117">JSON-fylki geta aðeins verið faldaðar einingar í eiginleikaeiningum hlutar.</span><span class="sxs-lookup"><span data-stu-id="338f6-117">JSON arrays can be only nested elements of the property elements of an object.</span></span>
- <span data-ttu-id="338f6-118">JSON-fylki geta aðeins innihaldið JSON-hluti.</span><span class="sxs-lookup"><span data-stu-id="338f6-118">JSON arrays can contain only JSON objects.</span></span> <span data-ttu-id="338f6-119">Þau geta ekki innihaldið bein strengja-/tölugildi og faldaðar fylkingar.</span><span class="sxs-lookup"><span data-stu-id="338f6-119">They can't contain direct string/numeric values and nested arrays.</span></span> <span data-ttu-id="338f6-120">Einingar í þessum fylkjum verða þáttaðar í röð, eins og þær eru tilgreindar í forminu.</span><span class="sxs-lookup"><span data-stu-id="338f6-120">Elements in these arrays will be parsed in order, as they are specified in the format.</span></span> <span data-ttu-id="338f6-121">Tekið verður tillit til margfeldisstillinga á hvern JSON-hlut.</span><span class="sxs-lookup"><span data-stu-id="338f6-121">Multiplicity settings on each JSON object will be considered.</span></span>

<span data-ttu-id="338f6-122">Að auki verður þú að ljúka verkleiðbeiningunum [ER Stofna nauðsynlegar skilgreiningar til að flytja inn gögn úr utanaðkomandi skrá](tasks/er-required-configurations-import-data.md) ef þú hefur ekki þegar lokið þeim.</span><span class="sxs-lookup"><span data-stu-id="338f6-122">Additionally, you must complete the [ER Create required configurations to import data from an external file](tasks/er-required-configurations-import-data.md) task guide if you haven't already completed it.</span></span> <span data-ttu-id="338f6-123">Sæktu eftirfarandi skrá til að ljúka verkefnaleiðbeiningunni.</span><span class="sxs-lookup"><span data-stu-id="338f6-123">Download the following file to complete the task guide.</span></span>

| <span data-ttu-id="338f6-124">Titill</span><span class="sxs-lookup"><span data-stu-id="338f6-124">Title</span></span>                  | <span data-ttu-id="338f6-125">Skrárnafn</span><span class="sxs-lookup"><span data-stu-id="338f6-125">File name</span></span> |
|------------------------|-----------|
| <span data-ttu-id="338f6-126">Líkanaskilgreining rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="338f6-126">ER model configuration</span></span> | [<span data-ttu-id="338f6-127">1099model.xml</span><span class="sxs-lookup"><span data-stu-id="338f6-127">1099model.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=874111) |
