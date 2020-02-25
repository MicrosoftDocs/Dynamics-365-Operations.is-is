---
title: Flutningur undirbókar í Fjárhag
description: Þetta efni lýsir getu Microsoft Dynamics 365 Finance tengt flutningsferli undirbókar í aðalbókinni.
author: roschlom
manager: AnnBe
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-01-18
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 1ae10f406148e213fd0272d1387f15606233be27
ms.sourcegitcommit: 9168621ca9b5061c65f3e05dbc5918b6a11d53d5
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/31/2020
ms.locfileid: "3000448"
---
# <a name="subledger-transfer-to-the-general-ledger"></a><span data-ttu-id="3960f-103">Flutningur undirbókar í Fjárhag</span><span class="sxs-lookup"><span data-stu-id="3960f-103">Subledger transfer to the General ledger</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3960f-104">Þetta efni lýsir getu í Microsoft Dynamics 365 Finance sem tengjast reglum um flutning á lotum dagbókarfærslna undirbókar.</span><span class="sxs-lookup"><span data-stu-id="3960f-104">This topic describes capabilities in Microsoft Dynamics 365 Finance that are related to the rules for transferring batches of subledger journal entries.</span></span>

<span data-ttu-id="3960f-105">Í útgáfu 8.1 voru gerðar breytingar til að leyfa flutning reglna, sem felldi úr gildi samstillingarvalkostsins.</span><span class="sxs-lookup"><span data-stu-id="3960f-105">In version 8.1, changes were made to allow the transfer of rules, which deprecated the Synchronous option.</span></span> <span data-ttu-id="3960f-106">Nánari upplýsingar er að finna í [Fjarlægðar eða úreltar aðgerðir fyrir Finance and Operations](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/deprecated-features?toc=/dynamics365/finance/toc.json#finance-and-operations-81-with-platform-update-20).</span><span class="sxs-lookup"><span data-stu-id="3960f-106">For more information, see [Removed or deprecated features for Finance and Operations](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/deprecated-features?toc=/dynamics365/finance/toc.json#finance-and-operations-81-with-platform-update-20).</span></span>

<span data-ttu-id="3960f-107">Eftirfarandi valkostir eru tiltækir til að flytja hópi á hærri stærð.</span><span class="sxs-lookup"><span data-stu-id="3960f-107">The following options are available for transferring subledger batches.</span></span> 

 - <span data-ttu-id="3960f-108">Ósamstilltur - Þessi valkostur mun tafarlaust tímasetja flutning bókhaldsgagnanna á undirstöðunni til fjárhags.</span><span class="sxs-lookup"><span data-stu-id="3960f-108">Asynchronous – This option will immediately schedule the transfer of the subledger accounting entries to the general ledger.</span></span> <span data-ttu-id="3960f-109">Fylgiskjal fjárhags verða tekin upp um leið og fjármagni er frjálst að afgreiða þessa beiðni á netþjóninum.</span><span class="sxs-lookup"><span data-stu-id="3960f-109">The general ledger voucher will be recorded as soon as resources are free to process this request on the server.</span></span> 

- <span data-ttu-id="3960f-110">Tímasett lota - Þessi valkostur bætir bókhaldsfærslunum sem eru fluttar yfir í vinnslukví í aðalbókinni, þar sem færslurnar verða unnar í pöntun.</span><span class="sxs-lookup"><span data-stu-id="3960f-110">Scheduled batch – This option will add the subledger accounting entries that are being transferred to the processing queue in the general ledger, where the entries will be processed in order received.</span></span> <span data-ttu-id="3960f-111">Fylgiskjal fjárhags verða tekin upp um leið á áætluðum tíma ef fjármagni er frjálst að afgreiða þessa runuvinnslu á netþjóninum.</span><span class="sxs-lookup"><span data-stu-id="3960f-111">The general ledger voucher will be recorded at the scheduled time if resources are free to process this batch job on the server.</span></span> 
 
<span data-ttu-id="3960f-112">Í útgáfu 10.0.8 voru gerðar endurbætur til að bæta árangur ósamhangandi valkostsins.</span><span class="sxs-lookup"><span data-stu-id="3960f-112">In version 10.0.8, improvements were made to enhance the performance of the Asynchrounous option.</span></span> <span data-ttu-id="3960f-113">Þessi aðgerð er gerð virk undir nafni eiginleikans **Flutningur undirliða yfir í hagræðingu almenns fjárhags**.</span><span class="sxs-lookup"><span data-stu-id="3960f-113">This feature is enabled under the feature name **Subledger transfer to General Ledger performance optimization**.</span></span> 
 
<span data-ttu-id="3960f-114">Þessi virkni bætir flutning gagna frá stórhýsinu yfir í aðalbókina.</span><span class="sxs-lookup"><span data-stu-id="3960f-114">This functionality improves the transfer of data from the subledger to the general ledger.</span></span> <span data-ttu-id="3960f-115">Það gerir ferlið kleift að vera skilvirkara og það flokka saman smærri viðskipti til að flytja.</span><span class="sxs-lookup"><span data-stu-id="3960f-115">It allows the process to be more efficient, and it groups together sets of smaller transactions to transfer.</span></span> <span data-ttu-id="3960f-116">Þetta gerir kleift að nýta hópþjónninn á skilvirkari hátt.</span><span class="sxs-lookup"><span data-stu-id="3960f-116">This allows for a more efficient use of the batch server.</span></span> <span data-ttu-id="3960f-117">Þessi virkni krefst þess að hópþjónninn sé settur upp, á netinu og virki til þess að Asynchrounous transfer valkosturinn virki.</span><span class="sxs-lookup"><span data-stu-id="3960f-117">This functionality requires that the batch server be set up, online, and functioning in order for the Asynchrounous transfer option to work.</span></span> 
