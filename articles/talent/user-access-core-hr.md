---
title: Notandi getur opnað Core HR en ekki Onboard eða Attract
description: Þetta efnisatriði útskýrir hvernig á að leysa vandamál þar sem notandi getur opnað Microsoft Dynamics 365 Talent - Core HR, en getur ekki opnað Attract og Onboard.
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
ms.openlocfilehash: 80b1f8aeabfd033f393463f4be5a61447377f2d9
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/23/2019
ms.locfileid: "2009307"
---
# <a name="user-can-access-core-hr-but-not-onboard-or-attract"></a><span data-ttu-id="4bdec-103">Notandi getur opnað Core HR en ekki Onboard eða Attract</span><span class="sxs-lookup"><span data-stu-id="4bdec-103">User can access Core HR but not Onboard or Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4bdec-104">**Umhverfisupplýsingar**</span><span class="sxs-lookup"><span data-stu-id="4bdec-104">**Environment details**</span></span>

- <span data-ttu-id="4bdec-105">Notandi A sá um uppsetningu Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="4bdec-105">The Microsoft Dynamics Lifecycle Services (LCS) deployment was done by user A.</span></span>
- <span data-ttu-id="4bdec-106">Notandi A bætti notanda B við sem notanda í Microsoft Dynamics 365 Talent: Core HR.</span><span class="sxs-lookup"><span data-stu-id="4bdec-106">User A added user B as a user to Microsoft Dynamics 365 Talent: Core HR.</span></span>

<span data-ttu-id="4bdec-107">**Úthreyfing**</span><span class="sxs-lookup"><span data-stu-id="4bdec-107">**Issue**</span></span>

<span data-ttu-id="4bdec-108">Notandi B getur opnað Core HR, en hann getur ekki opnað forritið Talent: Attract eða Talent: Onboard.</span><span class="sxs-lookup"><span data-stu-id="4bdec-108">User B can access Core HR, but can't access the Talent: Attract or Talent: Onboard app.</span></span> <span data-ttu-id="4bdec-109">Þegar notandi reynir að opna **Forrit fyrir umhverfi** er honum vísað í prófunarumhverfi í staðinn.</span><span class="sxs-lookup"><span data-stu-id="4bdec-109">When the user tries to go to **Experience apps**, he or she is taken to a trial environment instead.</span></span>

<span data-ttu-id="4bdec-110">**Lausn**</span><span class="sxs-lookup"><span data-stu-id="4bdec-110">**Solution**</span></span>

<span data-ttu-id="4bdec-111">Nauðsynlegt er að úthluta réttindum á Notanda B til að skoða umhverfi Microsoft PowerApps sem notandi A stofnaði í úthlutunarferlinu.</span><span class="sxs-lookup"><span data-stu-id="4bdec-111">User B must be assigned the rights to view the Microsoft PowerApps environment that user A created during the provisioning process.</span></span>

<span data-ttu-id="4bdec-112">Upplýsingar er að finna í „Að veita aðgang að umhverfinu“ í kaflanum [Úthlutun Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="4bdec-112">For information, see the "Granting access to the environment" section in [Provision Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

<span data-ttu-id="4bdec-113">**Langtímalausn**</span><span class="sxs-lookup"><span data-stu-id="4bdec-113">**Long-term solution**</span></span>

<span data-ttu-id="4bdec-114">Microsoft er að íhuga að úthluta sjálfkrafa viðeigandi réttindum fyrir Onboard og Attract þegar notanda er bætt við Core HR.</span><span class="sxs-lookup"><span data-stu-id="4bdec-114">Microsoft is considering automatically assigning the appropriate rights to Onboard and Attract when a user is added to Core HR.</span></span>
