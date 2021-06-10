---
title: Ekki er hægt að sía aðalskipulagsatriði eftir gildum viðkomandi þekjuflokks
description: Ekki er hægt að sía aðalskipulagsatriði eftir gildum viðkomandi þekjuflokks.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: fa0b614b6710c65811add8725a0e255ce2c34b88
ms.sourcegitcommit: 3c15a26e9708adc9a75082dc551f0a3a0a7d89f4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049473"
---
# <a name="you-cant-filter-master-planning-items-by-their-related-coverage-group-values"></a><span data-ttu-id="5edf2-103">Ekki er hægt að sía aðalskipulagsatriði eftir gildum viðkomandi þekjuflokks</span><span class="sxs-lookup"><span data-stu-id="5edf2-103">You can't filter master planning items by their related coverage group values</span></span>

<span data-ttu-id="5edf2-104">KB númer: 4612572</span><span class="sxs-lookup"><span data-stu-id="5edf2-104">KB number: 4612572</span></span>

## <a name="symptoms"></a><span data-ttu-id="5edf2-105">Einkenni</span><span class="sxs-lookup"><span data-stu-id="5edf2-105">Symptoms</span></span>

<span data-ttu-id="5edf2-106">Þú vilt sía vörurnar sem verða hafðar með í runuvinnslu aðaláætlanagerðar samkvæmt gildunum á tengdum færslum úr töflu vöruþekju.</span><span class="sxs-lookup"><span data-stu-id="5edf2-106">You want to filter the items that will be included in a master planning batch job, based on the values of related records from the item coverage table.</span></span> <span data-ttu-id="5edf2-107">(Þú vilt til dæmis sía vörur eftir gildinu fyrir **Lánardrottin** og/eða **Þekjuflokk**).</span><span class="sxs-lookup"><span data-stu-id="5edf2-107">(For example, you want to filter items by their **Vendor** and/or **Coverage group** value).</span></span> <span data-ttu-id="5edf2-108">Uppsetning síðunnar fyrir runuvinnslu gerir þér kleift að búa til tengingu frá töflunni **Vörur** við töfluna **Vöruþekja** og síðan tilgreina reitargildi úr vöruþekjutöflunni í fyrirspurninni þinni.</span><span class="sxs-lookup"><span data-stu-id="5edf2-108">The filter setup for the batch job lets you create a join from the **Items** table to the **Item coverage** table, and then specify field values from the item coverage table in your query.</span></span> <span data-ttu-id="5edf2-109">Hinsvegar eftir að þú lýkur við þessa uppsetningu býr kerfið samt sem áður til áætlaðar pantanir fyrir alla vöruþekjuna, ekki bara fyrir vörurnar sem passa við tiltekin reitargildi úr töflu vöruþekjunnar.</span><span class="sxs-lookup"><span data-stu-id="5edf2-109">However, after you complete this setup, the system still creates planned orders for the whole item coverage, not just for the items that match the specified field values from the item coverage table.</span></span>

## <a name="resolution"></a><span data-ttu-id="5edf2-110">Lausn</span><span class="sxs-lookup"><span data-stu-id="5edf2-110">Resolution</span></span>

<span data-ttu-id="5edf2-111">Sían fyrir runuvinnslu getur aðeins síað atriði.</span><span class="sxs-lookup"><span data-stu-id="5edf2-111">The batch job filter can filter only on items.</span></span> <span data-ttu-id="5edf2-112">Þótt þú getir bætt tengingu við töfluna **Vöruþekja**, munu síustillingar sem gerðar eru gagnvart þeirri töflu ekki hafa áhrif á úttak fyrirspurnarinnar.</span><span class="sxs-lookup"><span data-stu-id="5edf2-112">Although you can add a join to the **Item coverage** table, filter settings that you make against that table won't affect the query output.</span></span> <span data-ttu-id="5edf2-113">Á keyrslutíma keyrir kerfið áætlun fyrir alla þekjuflokka og öll afbrigði sem síuðu atriðin hafa.</span><span class="sxs-lookup"><span data-stu-id="5edf2-113">At runtime, the system runs planning for all the coverage groups and all the variations that the filtered items have.</span></span> <span data-ttu-id="5edf2-114">Þegar vara hefur verið höfð með í keyrslunni munu þekjuflokkar sem hafðir eru með í vörusíunni ekki hafa áhrif á úttak áætlanagerðar.</span><span class="sxs-lookup"><span data-stu-id="5edf2-114">After an item is already included in the run, any coverage groups that are included in the item filter a won't affect the planning output.</span></span>
