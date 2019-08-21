---
title: Persónulegur kostnaður á kostnaðarskýrslu
description: Þetta efnisatriði útskýrir tvær aðferðir til að halda utan um persónulegan kostnað í Microsoft Dynamics 365 for Finance and Operations.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b072fa9e78563d3e89b4d60e9ce61473902fee76
ms.sourcegitcommit: ef08bf1258aefb525d56bf85ef19311be26ab94c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/30/2019
ms.locfileid: "1794991"
---
# <a name="personal-expenses-on-an-expense-report"></a><span data-ttu-id="19f82-103">Persónulegur kostnaður á kostnaðarskýrslu</span><span class="sxs-lookup"><span data-stu-id="19f82-103">Personal expenses on an expense report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="19f82-104">Í viðskiptaferðum getur það gerst að starfsmaður setji stundum persónulegan kostnað á kreditkort fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="19f82-104">During business travel, workers might sometimes charge personal expenses to their corporate credit cards.</span></span> <span data-ttu-id="19f82-105">Ef ekkert ferli er skilgreint um hvernig haldið er utan um persónulegan kostnað gæti samþykktarferli kostnaðarskýrslu truflast þegar starfsmaður sendir sundurliðaða kostnaðarskýrslu.</span><span class="sxs-lookup"><span data-stu-id="19f82-105">If you don't define a process for handling personal expenses, the approval process for expense reports might be disrupted when workers submit their itemized expense reports.</span></span> 

<span data-ttu-id="19f82-106">Í Microsoft Dynamics 365 for Finance and Operations eru tvær aðferðir til að halda utan um persónulegan kostnað starfsmanns:</span><span class="sxs-lookup"><span data-stu-id="19f82-106">In Microsoft Dynamics 365 for Finance and Operations, there are two methods for handling a worker's personal expenses:</span></span>

- <span data-ttu-id="19f82-107">**Greitt af starfsmanni** – Fyrirtækið greiðir ekki persónulegan kostnað sem birtist á kreditkortareikningi fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="19f82-107">**Paid by employee** – Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="19f82-108">Í staðinn er stofnuð skýrsla sem sýnir persónulegan kostnað með fyrirtækiskostnaði sem var skuldfærður á kreditkort fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="19f82-108">Instead, it creates a report that shows personal expenses together with the corporate expenses that were charged to the corporate credit card.</span></span>
- <span data-ttu-id="19f82-109">**Greitt af fyrirtæki** – Fyrirtækið borgar allan kreditkortareikning fyrirtækisins og greiðir svo persónulegan kostnað inn á reikning starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="19f82-109">**Paid by company** – Your organization pays the whole bill for the corporate credit card and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="19f82-110">Hægt er að velja aðferðina sem fyrirtækið þitt notar á síðunni **Færibreytur útgjaldastýringar**.</span><span class="sxs-lookup"><span data-stu-id="19f82-110">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>
