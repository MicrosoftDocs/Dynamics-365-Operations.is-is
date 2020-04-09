---
title: Úrræðaleita vandamál sem tengjast meðvitund um lausn
description: Þetta efni veitir bilanaleit sem getur hjálpað þér að laga vandamál sem tengjast meðvitund um lausn.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 013e37269ec3df2bede15b28cffcc175967de9a3
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172622"
---
# <a name="troubleshoot-issues-related-to-solution-awareness"></a><span data-ttu-id="4ecd6-103">Úrræðaleita vandamál sem tengjast meðvitund um lausn</span><span class="sxs-lookup"><span data-stu-id="4ecd6-103">Troubleshoot issues related to solution awareness</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="4ecd6-104">Þetta efni veitir upplýsingar um úrræðaleit um samþættingu á tvöföldum skrifum á milli forrita Finance and Operations og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="4ecd6-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="4ecd6-105">Einkum veitir það upplýsingar sem geta hjálpað þér að laga vandamál sem tengjast meðvitund um lausn.</span><span class="sxs-lookup"><span data-stu-id="4ecd6-105">Specifically, it provides information that can help you fix issues that are related to solution awareness.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4ecd6-106">Nokkur þeirra atriða sem þetta efni fjallar um geta krafist annað hvort kerfisstjórans eða Microsoft Azure Active Directory (Azure AD) Leyfisupplýsingar leigjanda.</span><span class="sxs-lookup"><span data-stu-id="4ecd6-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="4ecd6-107">Hlutinn fyrir hvert vandamál útskýrir hvort krafist sé sérstaks hlutverks eða skilríkja.</span><span class="sxs-lookup"><span data-stu-id="4ecd6-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="error-on-the-dual-write-page"></a><span data-ttu-id="4ecd6-108">Villa á síðunni Tvíritun</span><span class="sxs-lookup"><span data-stu-id="4ecd6-108">Error on the Dual-write page</span></span>

<span data-ttu-id="4ecd6-109">Á síðunni **Tvöfalt skrif** gætirðu fengið villuboð sem líkjast eftirfarandi dæmi:</span><span class="sxs-lookup"><span data-stu-id="4ecd6-109">On the **Dual-write** page, you might receive an error message that resembles the following example:</span></span>

<span data-ttu-id="4ecd6-110">*Einingin sem heitir 'msdyn\_dualwriteentitymap' með namemapping='Logical' fannst ekki í MetadataCache.*</span><span class="sxs-lookup"><span data-stu-id="4ecd6-110">*The entity with a name 'msdyn\_dualwriteentitymap' with namemapping='Logical' was not found in the MetadataCache.*</span></span>

<span data-ttu-id="4ecd6-111">Til að laga málið skaltu ganga úr skugga um að tvískipt kjarnalausnin sé sett upp í Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="4ecd6-111">To fix the issue, make sure that the dual-write core solution is installed in Common Data Service.</span></span> <span data-ttu-id="4ecd6-112">Tvískipt kjarnalausnin er forsenda fyrir vitund um lausn.</span><span class="sxs-lookup"><span data-stu-id="4ecd6-112">The dual-write core solution is a prerequisite for solution awareness.</span></span>
