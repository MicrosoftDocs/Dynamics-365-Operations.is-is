---
title: Flutningur undirbókar í Fjárhag
description: Þetta efni lýsir getu Microsoft Dynamics 365 Finance tengt flutningsferli undirbókar í aðalbókinni.
author: roschlom
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-01-18
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 1efdf095e379b73d553ca3525abbeee8ca35bcbb
ms.sourcegitcommit: 7d0cfb359a4abc7392ddb3f0b3e9539c40b7204d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/14/2021
ms.locfileid: "5897505"
---
# <a name="subledger-transfer-to-the-general-ledger"></a><span data-ttu-id="10418-103">Flutningur undirbókar í Fjárhag</span><span class="sxs-lookup"><span data-stu-id="10418-103">Subledger transfer to the General ledger</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="10418-104">Þetta efni lýsir getu í Microsoft Dynamics 365 Finance sem tengjast reglum um flutning á lotum dagbókarfærslna undirbókar.</span><span class="sxs-lookup"><span data-stu-id="10418-104">This topic describes capabilities in Microsoft Dynamics 365 Finance that are related to the rules for transferring batches of subledger journal entries.</span></span>

<span data-ttu-id="10418-105">Í útgáfu 8.1 voru gerðar breytingar til að leyfa flutning á reglum sem úreltu valkostinn **Samstillt**.</span><span class="sxs-lookup"><span data-stu-id="10418-105">In version 8.1, changes were made to allow the transfer of rules, which deprecated the **Synchronous** option.</span></span> <span data-ttu-id="10418-106">Nánari upplýsingar er að finna í [Fjarlægðar eða úreltar aðgerðir fyrir Finance and Operations](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=%2fdynamics365%2ffinance%2ftoc.json#finance-and-operations-81-with-platform-update-20).</span><span class="sxs-lookup"><span data-stu-id="10418-106">For more information, see [Removed or deprecated features for Finance and Operations](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=%2fdynamics365%2ffinance%2ftoc.json#finance-and-operations-81-with-platform-update-20).</span></span>

<span data-ttu-id="10418-107">Eftirfarandi valkostir eru tiltækir til að flytja hópi á hærri stærð.</span><span class="sxs-lookup"><span data-stu-id="10418-107">The following options are available for transferring subledger batches.</span></span> 

 - <span data-ttu-id="10418-108">Ósamstilltur - Þessi valkostur mun tafarlaust tímasetja flutning bókhaldsgagnanna á undirstöðunni til fjárhags.</span><span class="sxs-lookup"><span data-stu-id="10418-108">Asynchronous – This option will immediately schedule the transfer of the subledger accounting entries to the general ledger.</span></span> <span data-ttu-id="10418-109">Fylgiskjal fjárhags verða tekin upp um leið og fjármagni er frjálst að afgreiða þessa beiðni á netþjóninum.</span><span class="sxs-lookup"><span data-stu-id="10418-109">The general ledger voucher will be recorded as soon as resources are free to process this request on the server.</span></span> 

- <span data-ttu-id="10418-110">Tímasett lota - Þessi valkostur bætir bókhaldsfærslunum sem eru fluttar yfir í vinnslukví í aðalbókinni, þar sem færslurnar verða unnar í pöntun.</span><span class="sxs-lookup"><span data-stu-id="10418-110">Scheduled batch – This option will add the subledger accounting entries that are being transferred to the processing queue in the general ledger, where the entries will be processed in order received.</span></span> <span data-ttu-id="10418-111">Fylgiskjal fjárhags verða tekin upp um leið á áætluðum tíma ef fjármagni er frjálst að afgreiða þessa runuvinnslu á netþjóninum.</span><span class="sxs-lookup"><span data-stu-id="10418-111">The general ledger voucher will be recorded at the scheduled time if resources are free to process this batch job on the server.</span></span> 
 
<span data-ttu-id="10418-112">Í útgáfu 10.0.8 voru gerðar úrbætur til að auka afköst ósamstillts valkosts.</span><span class="sxs-lookup"><span data-stu-id="10418-112">In version 10.0.8, improvements were made to enhance the performance of the Asynchronous option.</span></span> <span data-ttu-id="10418-113">Þessi aðgerð er gerð virk undir nafni eiginleikans **Flutningur undirliða yfir í hagræðingu almenns fjárhags**.</span><span class="sxs-lookup"><span data-stu-id="10418-113">This feature is enabled under the feature name **Subledger transfer to General Ledger performance optimization**.</span></span> 
 
<span data-ttu-id="10418-114">Þessi virkni bætir flutning gagna frá stórhýsinu yfir í aðalbókina.</span><span class="sxs-lookup"><span data-stu-id="10418-114">This functionality improves the transfer of data from the subledger to the general ledger.</span></span> <span data-ttu-id="10418-115">Það gerir ferlið kleift að vera skilvirkara og það flokka saman smærri viðskipti til að flytja.</span><span class="sxs-lookup"><span data-stu-id="10418-115">It allows the process to be more efficient, and it groups together sets of smaller transactions to transfer.</span></span> <span data-ttu-id="10418-116">Þetta gerir kleift að nýta hópþjónninn á skilvirkari hátt.</span><span class="sxs-lookup"><span data-stu-id="10418-116">This allows for a more efficient use of the batch server.</span></span> <span data-ttu-id="10418-117">Þessi virkni krefst þess að runuþjónninn sé sett upp, nettengdur og sé í gangi til að valkosturinn Ósamstilltur flutningur virki.</span><span class="sxs-lookup"><span data-stu-id="10418-117">This functionality requires that the batch server be set up, online, and functioning in order for the Asynchronous transfer option to work.</span></span> 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]