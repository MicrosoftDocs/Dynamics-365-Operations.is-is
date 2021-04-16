---
title: Aukin RCS-síun í RCS/altækri geymslu
description: Þetta efni lýsir aukinni síunargetu fyrir RCS Global geymsluna sem hefur verið bætt til að innihalda viðbótarsíurnar.
author: JaneA07
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 31df79159caa1094a68743ba07f308a2029e4071
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832645"
---
# <a name="rcs-enhanced-filtering-options-for-finding-configurations-in-the-rcsglobal-repository"></a><span data-ttu-id="98b32-103">Auknir síuvalkostir RCS til að finna skilgreiningar í RCS/altækri geymslu</span><span class="sxs-lookup"><span data-stu-id="98b32-103">RCS enhanced filtering options for finding configurations in the RCS/Global repository</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="98b32-104">Þetta efnisatriði lýsir aukinni síunargetu fyrir altæka geymslu RCS (Regulatory Configuration Services) sem hefur verið bætt til að fela í sér hæfileika til að sía með eftirfarandi skilyrðum:</span><span class="sxs-lookup"><span data-stu-id="98b32-104">This topic describes enhanced filtering capabilities for Regulatory Configuration Services (RCS) Global repository, which have been improved to include the ability to filter with the following criteria:</span></span> 
- <span data-ttu-id="98b32-105">**Land/svæði** - Byggt á ISO-landsnúmerum</span><span class="sxs-lookup"><span data-stu-id="98b32-105">**Country/region** - Based on ISO country codes</span></span>  
- <span data-ttu-id="98b32-106">Gerðir **Merkis** fyrir:</span><span class="sxs-lookup"><span data-stu-id="98b32-106">**Tags** types for:</span></span>
  - <span data-ttu-id="98b32-107">Virkt svæði</span><span class="sxs-lookup"><span data-stu-id="98b32-107">Functional area</span></span>
  - <span data-ttu-id="98b32-108">Eiginleikasvæði</span><span class="sxs-lookup"><span data-stu-id="98b32-108">Feature area</span></span>
  - <span data-ttu-id="98b32-109">Iðnaður</span><span class="sxs-lookup"><span data-stu-id="98b32-109">Industry</span></span> 
  - <span data-ttu-id="98b32-110">Viðskiptaskjal</span><span class="sxs-lookup"><span data-stu-id="98b32-110">Business document</span></span> 

<span data-ttu-id="98b32-111">Til að gera það auðveldara að uppgötva sérstakar eða tengdar grunnstillingar er hægt að nota síur, annaðhvort einar og sér eða í hóp.</span><span class="sxs-lookup"><span data-stu-id="98b32-111">To make it easier to discover specific or related configurations you can apply filters, either individually or as a group.</span></span> <span data-ttu-id="98b32-112">Til að finna staka gerð af stillanlegum viðskiptaskjölum sem tengjast lánardrottnareikningum er til dæmis hægt að nota síuna **Gerð viðskiptaskjals** til að leita að slíku skjali.</span><span class="sxs-lookup"><span data-stu-id="98b32-112">For example, to find a single type of 'configurable business documents that are related to vendor invoices, you could apply a **Business document type** filter to search for that type of document.</span></span> 

<span data-ttu-id="98b32-113">[![Sía hluti fyrir altæka geymslu](media/rcs-enhanced-filter-section.JPG)](./media/rcs-enhanced-filter-section.JPG)</span><span class="sxs-lookup"><span data-stu-id="98b32-113">[![Filter section for Global repository](media/rcs-enhanced-filter-section.JPG)](./media/rcs-enhanced-filter-section.JPG)</span></span> 

<span data-ttu-id="98b32-114">Þú getur fínstillt leitina enn frekar með því að velja gerð skjals, t.d. „lánardrottnareikningur“ og smella á **Nota síu**.</span><span class="sxs-lookup"><span data-stu-id="98b32-114">You can further refine the search by selecting document type, for example 'vendor invoice' and clicking **Apply filter**.</span></span> <span data-ttu-id="98b32-115">Eftirfarandi dæmi sýnir niðurstöðurnar þegar síað er fyrir **Gerð viðskiptaskjals** með gerð skjals bætt við.</span><span class="sxs-lookup"><span data-stu-id="98b32-115">The following example shows the results when filtering on **Business document type** with the document type added.</span></span> 

<span data-ttu-id="98b32-116">[![Notuð sía og innflutningur fyrir gerð viðskiptaskjala](media/rcs-enhanced-filtering-applied.JPG)](./media/rcs-enhanced-filtering-applied.JPG)</span><span class="sxs-lookup"><span data-stu-id="98b32-116">[![Applied filter and Import for business document type](media/rcs-enhanced-filtering-applied.JPG)](./media/rcs-enhanced-filtering-applied.JPG)</span></span> 

<span data-ttu-id="98b32-117">Síaðar niðurstöður er hægt að flytja inn í RCS-geymslu notenda eða í Dynamics 365 Finance-umhverfi, annaðhvort hverja fyrir sig eða saman.</span><span class="sxs-lookup"><span data-stu-id="98b32-117">Filtered results can be imported into a users RCS repository or a Dynamics 365 Finance environment, either individually or as a set.</span></span> <span data-ttu-id="98b32-118">Til að gera þetta skaltu velja hóp stillinga og smella á **Flytja inn**.</span><span class="sxs-lookup"><span data-stu-id="98b32-118">To do this, select the group of configurations, and click **Import**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]