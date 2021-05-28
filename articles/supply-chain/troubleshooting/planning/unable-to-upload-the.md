---
title: Ekki er hægt að uppfæra áætlaðan einingarkostnað þegar færslur eftirspurnarspár eru fluttar inn
description: Þegar þú notar gagnaeiningar til að flytja inn færslur eftirspurnarspár er kostnaðarverð fyrir fyrirliggjandi færslur ekki uppfært svo það samsvari innfluttum gögnum.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: DataManagementWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: angarmas
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: c8ea8322a6c7bafe2dfcaaee3e9989f753c85e2a
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026613"
---
# <a name="you-cant-update-the-forecasted-unit-cost-when-you-import-demand-forecast-records"></a><span data-ttu-id="53032-103">Ekki er hægt að uppfæra áætlaðan einingarkostnað þegar færslur eftirspurnarspár eru fluttar inn</span><span class="sxs-lookup"><span data-stu-id="53032-103">You can't update the forecasted unit cost when you import demand forecast records</span></span>

<span data-ttu-id="53032-104">KB númer: 4614109</span><span class="sxs-lookup"><span data-stu-id="53032-104">KB number: 4614109</span></span>

## <a name="symptoms"></a><span data-ttu-id="53032-105">Einkenni</span><span class="sxs-lookup"><span data-stu-id="53032-105">Symptoms</span></span>

<span data-ttu-id="53032-106">Þegar þú notar gagnaeiningar til að flytja inn færslur eftirspurnarspár er gildi **Áætlaður einingarkostnaður** fyrir fyrirliggjandi færslur ekki uppfært svo það samsvari innfluttum gögnum.</span><span class="sxs-lookup"><span data-stu-id="53032-106">When you use data entities to import demand forecast records, the **Forecasted unit cost** value for existing records isn't updated so that it matches the imported data.</span></span>

## <a name="cause"></a><span data-ttu-id="53032-107">Orsök</span><span class="sxs-lookup"><span data-stu-id="53032-107">Cause</span></span>

<span data-ttu-id="53032-108">**Áætlaður einingarkostnaður** er skrifvarinn reitur.</span><span class="sxs-lookup"><span data-stu-id="53032-108">**Forecasted unit cost** is a read-only field.</span></span> <span data-ttu-id="53032-109">Gildið er byggt á einingarkostnaði vörunnar og ekki er hægt að stilla það beint í gegnum innflutning.</span><span class="sxs-lookup"><span data-stu-id="53032-109">The value is based on the product unit cost and can't be set directly through import.</span></span>

## <a name="resolution"></a><span data-ttu-id="53032-110">Upplausn</span><span class="sxs-lookup"><span data-stu-id="53032-110">Resolution</span></span>

<span data-ttu-id="53032-111">Þar sem reiturinn er skrifvarinn er ekki hægt að flytja inn gildi fyrir hann.</span><span class="sxs-lookup"><span data-stu-id="53032-111">Because the field is read only, you can't import values for it.</span></span> <span data-ttu-id="53032-112">Gildið verður reiknað samkvæmt fyrirliggjandi viðskiptagrunni.</span><span class="sxs-lookup"><span data-stu-id="53032-112">The value will be calculated according to the existing business logic.</span></span>
