---
title: Notandi getur opnað Mannauð en ekki Onboard eða Attract
description: Þetta efnisatriði útskýrir hvernig á að leysa vandamál þar sem notandi getur opnað Microsoft Dynamics 365 Talent - Human Resources, en getur ekki opnað Attract og Onboard.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 6c384d9a7100982eabd201d910e1bea14355dc1f
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/03/2020
ms.locfileid: "3006311"
---
# <a name="user-can-access-human-resources-but-not-onboard-or-attract"></a><span data-ttu-id="f2f3b-103">Notandi getur opnað Mannauð en ekki Onboard eða Attract</span><span class="sxs-lookup"><span data-stu-id="f2f3b-103">User can access Human Resources but not Onboard or Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f2f3b-104">**Umhverfisupplýsingar**</span><span class="sxs-lookup"><span data-stu-id="f2f3b-104">**Environment details**</span></span>

- <span data-ttu-id="f2f3b-105">Notandi A sá um uppsetningu Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="f2f3b-105">The Microsoft Dynamics Lifecycle Services (LCS) deployment was done by user A.</span></span>
- <span data-ttu-id="f2f3b-106">Notandi A bætti notanda B við sem notanda í Microsoft Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="f2f3b-106">User A added user B as a user to Microsoft Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="f2f3b-107">**Úthreyfing**</span><span class="sxs-lookup"><span data-stu-id="f2f3b-107">**Issue**</span></span>

<span data-ttu-id="f2f3b-108">Notandi B getur opnað Human Resources, en hann getur ekki opnað forritið Talent: Attract eða Talent: Onboard.</span><span class="sxs-lookup"><span data-stu-id="f2f3b-108">User B can access Human Resources, but can't access the Talent: Attract or Talent: Onboard app.</span></span> <span data-ttu-id="f2f3b-109">Þegar notandi reynir að opna **Forrit fyrir umhverfi** er honum vísað í prófunarumhverfi í staðinn.</span><span class="sxs-lookup"><span data-stu-id="f2f3b-109">When the user tries to go to **Experience apps**, he or she is taken to a trial environment instead.</span></span>

<span data-ttu-id="f2f3b-110">**Lausn**</span><span class="sxs-lookup"><span data-stu-id="f2f3b-110">**Solution**</span></span>

<span data-ttu-id="f2f3b-111">Nauðsynlegt er að úthluta réttindum á Notanda B til að skoða umhverfi Microsoft Power Apps sem notandi A stofnaði í úthlutunarferlinu.</span><span class="sxs-lookup"><span data-stu-id="f2f3b-111">User B must be assigned the rights to view the Microsoft Power Apps environment that user A created during the provisioning process.</span></span>

<span data-ttu-id="f2f3b-112">Upplýsingar er að finna í „Að veita aðgang að umhverfinu“ í kaflanum [Úthlutun Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="f2f3b-112">For information, see the "Granting access to the environment" section in [Provision Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

<span data-ttu-id="f2f3b-113">**Langtímalausn**</span><span class="sxs-lookup"><span data-stu-id="f2f3b-113">**Long-term solution**</span></span>

<span data-ttu-id="f2f3b-114">Microsoft er að íhuga að úthluta sjálfkrafa viðeigandi réttindum fyrir Onboard og Attract þegar notanda er bætt við Human Resources.</span><span class="sxs-lookup"><span data-stu-id="f2f3b-114">Microsoft is considering automatically assigning the appropriate rights to Onboard and Attract when a user is added to Human Resources.</span></span>
