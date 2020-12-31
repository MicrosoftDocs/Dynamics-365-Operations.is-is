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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 79b2920b80ce4a8b419c2a146e15babc061cf64d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683565"
---
# <a name="troubleshoot-issues-related-to-solution-awareness"></a><span data-ttu-id="9d442-103">Úrræðaleita vandamál sem tengjast meðvitund um lausn</span><span class="sxs-lookup"><span data-stu-id="9d442-103">Troubleshoot issues related to solution awareness</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="9d442-104">Þetta efni veitir upplýsingar um úrræðaleit um samþættingu á tvöföldum skrifum á milli forrita Finance and Operations og Dataverse.</span><span class="sxs-lookup"><span data-stu-id="9d442-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="9d442-105">Einkum veitir það upplýsingar sem geta hjálpað þér að laga vandamál sem tengjast meðvitund um lausn.</span><span class="sxs-lookup"><span data-stu-id="9d442-105">Specifically, it provides information that can help you fix issues that are related to solution awareness.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9d442-106">Nokkur þeirra atriða sem þetta efni fjallar um geta krafist annað hvort kerfisstjórans eða Microsoft Azure Active Directory (Azure AD) Leyfisupplýsingar leigjanda.</span><span class="sxs-lookup"><span data-stu-id="9d442-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="9d442-107">Hlutinn fyrir hvert vandamál útskýrir hvort krafist sé sérstaks hlutverks eða skilríkja.</span><span class="sxs-lookup"><span data-stu-id="9d442-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="error-on-the-dual-write-page"></a><span data-ttu-id="9d442-108">Villa á síðunni Tvíritun</span><span class="sxs-lookup"><span data-stu-id="9d442-108">Error on the Dual-write page</span></span>

<span data-ttu-id="9d442-109">Á síðunni **Tvöfalt skrif** gætirðu fengið villuboð sem líkjast eftirfarandi dæmi:</span><span class="sxs-lookup"><span data-stu-id="9d442-109">On the **Dual-write** page, you might receive an error message that resembles the following example:</span></span>

<span data-ttu-id="9d442-110">*Einingin sem heitir 'msdyn\_dualwriteentitymap' með namemapping='Logical' fannst ekki í MetadataCache.*</span><span class="sxs-lookup"><span data-stu-id="9d442-110">*The entity with a name 'msdyn\_dualwriteentitymap' with namemapping='Logical' was not found in the MetadataCache.*</span></span>

<span data-ttu-id="9d442-111">Til að laga málið skaltu ganga úr skugga um að tvískipt kjarnalausnin sé sett upp í Dataverse.</span><span class="sxs-lookup"><span data-stu-id="9d442-111">To fix the issue, make sure that the dual-write core solution is installed in Dataverse.</span></span> <span data-ttu-id="9d442-112">Tvískipt kjarnalausnin er forsenda fyrir vitund um lausn.</span><span class="sxs-lookup"><span data-stu-id="9d442-112">The dual-write core solution is a prerequisite for solution awareness.</span></span>
