---
title: "Notandi getur opnað Core HR en ekki forritin Onboard eða Attract"
description: "Þetta efnisatriði útskýrir hvernig á að leysa vandamál þar sem notandi getur opnað Microsoft Dynamics 365 for Talent Core HR, en getur ekki opnað forritin Attract og Onboard."
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 2e5d0b1bf993aec89c7d2c6d4916732f5824310d
ms.contentlocale: is-is
ms.lasthandoff: 12/04/2018

---

# <a name="user-can-access-core-hr-but-not-the-onboard-or-attract-app"></a><span data-ttu-id="fd42a-103">Notandi getur opnað Core HR en ekki forritin Onboard eða Attract</span><span class="sxs-lookup"><span data-stu-id="fd42a-103">User can access Core HR but not the Onboard or Attract app</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fd42a-104">**Umhverfisupplýsingar**</span><span class="sxs-lookup"><span data-stu-id="fd42a-104">**Environment details**</span></span>

- <span data-ttu-id="fd42a-105">Notandi A sá um uppsetningu Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="fd42a-105">The Microsoft Dynamics Lifecycle Services (LCS) deployment was done by user A.</span></span>
- <span data-ttu-id="fd42a-106">Notandi A bætti notanda B við sem notanda í Microsoft Dynamics 365 for Talent Core HR.</span><span class="sxs-lookup"><span data-stu-id="fd42a-106">User A added user B as a user to Microsoft Dynamics 365 for Talent Core HR.</span></span>

<span data-ttu-id="fd42a-107">**Úthreyfing**</span><span class="sxs-lookup"><span data-stu-id="fd42a-107">**Issue**</span></span>

<span data-ttu-id="fd42a-108">Notandi B getur opnað Core HR, en hann getur ekki opnað forritið Talent: Attract eða Talent: Onboard.</span><span class="sxs-lookup"><span data-stu-id="fd42a-108">User B can access Core HR, but can't access the Talent: Attract or Talent: Onboard app.</span></span> <span data-ttu-id="fd42a-109">Þegar notandi reynir að opna **Forrit fyrir umhverfi** er honum vísað í prófunarumhverfi í staðinn.</span><span class="sxs-lookup"><span data-stu-id="fd42a-109">When the user tries to go to **Experience apps**, he or she is taken to a trial environment instead.</span></span>

<span data-ttu-id="fd42a-110">**Lausn**</span><span class="sxs-lookup"><span data-stu-id="fd42a-110">**Solution**</span></span>

<span data-ttu-id="fd42a-111">Nauðsynlegt er að úthluta réttindum á Notanda B til að skoða umhverfi Microsoft PowerApps sem notandi A stofnaði í úthlutunarferlinu.</span><span class="sxs-lookup"><span data-stu-id="fd42a-111">User B must be assigned the rights to view the Microsoft PowerApps environment that user A created during the provisioning process.</span></span>

<span data-ttu-id="fd42a-112">Upplýsingar er að finna í „Að veita aðgang að umhverfinu“ í kaflanum [Úthlutun Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="fd42a-112">For information, see the "Granting access to the environment" section in [Provision Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

<span data-ttu-id="fd42a-113">**Langtímalausn**</span><span class="sxs-lookup"><span data-stu-id="fd42a-113">**Long-term solution**</span></span>

<span data-ttu-id="fd42a-114">Microsoft er að íhuga að úthluta sjálfkrafa viðeigandi réttindum fyrir Onboard og Attract þegar notanda er bætt við Core HR.</span><span class="sxs-lookup"><span data-stu-id="fd42a-114">Microsoft is considering automatically assigning the appropriate rights to Onboard and Attract when a user is added to Core HR.</span></span>

