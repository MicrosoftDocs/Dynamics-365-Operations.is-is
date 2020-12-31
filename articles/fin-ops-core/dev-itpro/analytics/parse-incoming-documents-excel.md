---
title: Þátta skjöl á innleið á Excel-sniði
description: Í þessu efnisatriði eru veittar upplýsingar um hönnun á sniðum rafrænnar skýrslugerðar til að þátta efni sem er að finna í mótteknum skrám Microsoft Excel.
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
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
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 6e27806d3b94eb485705cec539a4849b81fbba91
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685788"
---
# <a name="parse-incoming-documents-in-excel-format"></a><span data-ttu-id="bdf25-103">Þátta skjöl á innleið á Excel-sniði</span><span class="sxs-lookup"><span data-stu-id="bdf25-103">Parse incoming documents in Excel format</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="bdf25-104">Hægt er að hanna snið rafrænnar skýrslugerðar til að þátta mótteknar skrár Microsoft Excel sem tákna gögn í vinnubókum Microsoft Excel (skrár á XLSX-sniði).</span><span class="sxs-lookup"><span data-stu-id="bdf25-104">You can design Electronic reporting (ER) formats to parse incoming Microsoft Excel files that represent data in Microsoft Excel workbooks (files in XLSX format).</span></span> <span data-ttu-id="bdf25-105">Síðan er hægt að nota efnið úr þessum skrám til að uppfæra hugbúnaðargögn.</span><span class="sxs-lookup"><span data-stu-id="bdf25-105">You can then use the content from these files to update application data.</span></span> <span data-ttu-id="bdf25-106">Þetta er gagnlegt ef þú:</span><span class="sxs-lookup"><span data-stu-id="bdf25-106">This is useful if you:</span></span>

- <span data-ttu-id="bdf25-107">Hannar nýtt líkan og snið og vilt prófa þær á keyrslutíma.</span><span class="sxs-lookup"><span data-stu-id="bdf25-107">Design a new model and format and want to test them at run-time.</span></span> <span data-ttu-id="bdf25-108">Í þessu tilviki mun Excel líkja eftir raunverulegum hugbúnaðargögnum.</span><span class="sxs-lookup"><span data-stu-id="bdf25-108">In this case, Excel will simulate the actual application data.</span></span>
- <span data-ttu-id="bdf25-109">Stjórnar gögnum utan hugbúnaðarins í Excel og vilt flytja þessi gögn inn til að senda inn tiltekna skýrslu.</span><span class="sxs-lookup"><span data-stu-id="bdf25-109">Manage data beyond your application in Excel and want to import this data to submit a specific report.</span></span>

<span data-ttu-id="bdf25-110">Til að læra meira um þennan eiginleika skal spila verkefnaleiðbeiningarnar **Flytja inn gögn rafrænnar skýrslugerðar frá Microsoft Excel-skrá (hluti 1: Hönnunarsnið)** og **Flytja inn gögn rafrænnar skýrslugerðar frá Microsoft Excel-skrá (hluti 2: Flytja inn gögn)** (hlutar af viðskiptaferlinum 7.5.4.3 Acquire/Develop IT þjónustu-/lausnarþáttum (10677)).</span><span class="sxs-lookup"><span data-stu-id="bdf25-110">To learn more about this feature, play the task guides **ER Import data from a Microsoft Excel file (Part 1: Design format)** and **ER Import data from a Microsoft Excel file (Part 2: Import data)** (parts of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process).</span></span> <span data-ttu-id="bdf25-111">Þessar verkefnaleiðbeiningar fylgja þér í gegnum það hvernig hægt er að þátta móttekna Excel-skrá með því að nota snið rafrænnar skýrslugerðar til að flytja inn upplýsingar frá mótteknum skjölum og uppfæra hugbúnaðargögn.</span><span class="sxs-lookup"><span data-stu-id="bdf25-111">These task guides walk through how the incoming Excel file can be parsed by using the ER format to import information from incoming documents and update application data.</span></span> <span data-ttu-id="bdf25-112">Hægt er að sækja verkefnaleiðbeiningarnar frá [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span><span class="sxs-lookup"><span data-stu-id="bdf25-112">You can download the task guide files from the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span>

<span data-ttu-id="bdf25-113">Sækja eftirfarandi skrár til að ljúka verkefnaleiðbeiningunum sem minnst er á hér að ofan.</span><span class="sxs-lookup"><span data-stu-id="bdf25-113">Download the following files to complete the task guides mentioned above.</span></span>

| <span data-ttu-id="bdf25-114">Lýsing á efni</span><span class="sxs-lookup"><span data-stu-id="bdf25-114">Content description</span></span>                         | <span data-ttu-id="bdf25-115">Skrá</span><span class="sxs-lookup"><span data-stu-id="bdf25-115">File</span></span>                                                                       |
|---------------------------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="bdf25-116">Móttekin skrá á .XLSX-sniði - sniðmát</span><span class="sxs-lookup"><span data-stu-id="bdf25-116">Incoming file in .XLSX format - template</span></span>    | [<span data-ttu-id="bdf25-117">1099import-template.xlsx</span><span class="sxs-lookup"><span data-stu-id="bdf25-117">1099import-template.xlsx</span></span>](https://go.microsoft.com/fwlink/?linkid=862266) |
| <span data-ttu-id="bdf25-118">Móttekin skrá á .XLSX-sniði - sýnigögn</span><span class="sxs-lookup"><span data-stu-id="bdf25-118">Incoming file in .XLSX format - sample data</span></span> | [<span data-ttu-id="bdf25-119">1099import-data.xlsx</span><span class="sxs-lookup"><span data-stu-id="bdf25-119">1099import-data.xlsx</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)     |

<span data-ttu-id="bdf25-120">Ef þú hefur ekki enn spilað eftirfarandi verkefnaleiðbeiningar, [Stofna nauðsynlega grunnstillingu rafrænnar skýrslugerðar til að flytja inn gögn frá ytri skrá](./tasks/er-required-configurations-import-data.md) í núverandi hugbúnaði Finance and Operations, skal sækja eftirfarandi skrá.</span><span class="sxs-lookup"><span data-stu-id="bdf25-120">If you have not yet played the following task guide, [ER Create required configurations to import data from an external file](./tasks/er-required-configurations-import-data.md) in the current Finance and Operations application, download the following file.</span></span>

| <span data-ttu-id="bdf25-121">Lýsing á efni</span><span class="sxs-lookup"><span data-stu-id="bdf25-121">Content description</span></span>    | <span data-ttu-id="bdf25-122">Skrá</span><span class="sxs-lookup"><span data-stu-id="bdf25-122">File</span></span>                                                            |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="bdf25-123">Líkanaskilgreining rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="bdf25-123">ER model configuration</span></span> | [<span data-ttu-id="bdf25-124">1099model.xml</span><span class="sxs-lookup"><span data-stu-id="bdf25-124">1099model.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=862266) |
