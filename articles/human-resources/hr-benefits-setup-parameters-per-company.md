---
title: Grunnstilla færibreytur fríðindastjórnunar eftir fyrirtæki
description: Skilgreina færibreytur fyrir fríðindastjórnun á fyrirtæki í Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 31f30c3d268132327074e931b714b5b2ee3ec5ac
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466641"
---
# <a name="configure-benefits-management-parameters-per-company"></a><span data-ttu-id="be3f5-103">Grunnstilla færibreytur fríðindastjórnunar eftir fyrirtæki</span><span class="sxs-lookup"><span data-stu-id="be3f5-103">Configure Benefits management parameters per company</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="be3f5-104">Fyrir hvert fyrirtæki sem býður upp á fríðindi verður að skilgreina stillingar fyrir staðfestingartölvupóst fyrir fríðindi.</span><span class="sxs-lookup"><span data-stu-id="be3f5-104">For each organization that offers benefits, you must configure settings for benefits confirmation emails.</span></span>

## <a name="configure-confirmation-email-settings"></a><span data-ttu-id="be3f5-105">Skilgreina stillingar staðfestingartölvupósts</span><span class="sxs-lookup"><span data-stu-id="be3f5-105">Configure confirmation email settings</span></span>

1. <span data-ttu-id="be3f5-106">Í **Fríðindastjórnun** vinnusvæðinu, undir **Uppsetning**, skal velja **Færibreytur mannauðs**.</span><span class="sxs-lookup"><span data-stu-id="be3f5-106">In the **Benefits management** workspace, under **Setup**, select **Human Resources Parameters**.</span></span>

2. <span data-ttu-id="be3f5-107">Í flipanum **Fríðindastjórnun** skal tilgreina gildi fyrir eftirfarandi reiti:</span><span class="sxs-lookup"><span data-stu-id="be3f5-107">In the **Benefits management** tab, specify values for the following fields:</span></span> 

   | <span data-ttu-id="be3f5-108">Svæði</span><span class="sxs-lookup"><span data-stu-id="be3f5-108">Field</span></span> | <span data-ttu-id="be3f5-109">lýsing</span><span class="sxs-lookup"><span data-stu-id="be3f5-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="be3f5-110">**Senda staðfestingarpóst**</span><span class="sxs-lookup"><span data-stu-id="be3f5-110">**Send confirmation email**</span></span> | <span data-ttu-id="be3f5-111">Þegar kveikt er á þessum eiginleika er staðfestingartölvupóstur sendur á starfsmenn þegar þeir skrá sig út úr fríðindaskráningu í sjálfsafgreiðslu starfsmanna.</span><span class="sxs-lookup"><span data-stu-id="be3f5-111">When this feature is on, a confirmation email will be sent to employees when they check out from the benefits enrollment experience in Employee self-service.</span></span> |
   | <span data-ttu-id="be3f5-112">**Sniðmát fyrir staðfestingartölvupóst**</span><span class="sxs-lookup"><span data-stu-id="be3f5-112">**Confirmation email template**</span></span> | <span data-ttu-id="be3f5-113">Veljið tölvupóstssniðmát fyrirtækis sem á að nota þegar staðfesting skráningar er send.</span><span class="sxs-lookup"><span data-stu-id="be3f5-113">Select the organization email template to use when sending the enrollment confirmation.</span></span> <span data-ttu-id="be3f5-114">Ef þú velur ekki sniðmát er eftirfarandi almennur tölvupóstur sendur:</span><span class="sxs-lookup"><span data-stu-id="be3f5-114">If you don't select a template, the following generic email will be sent:</span></span><br><br><span data-ttu-id="be3f5-115">%EmployeeFirstName%,</span><span class="sxs-lookup"><span data-stu-id="be3f5-115">%EmployeeFirstName%,</span></span><br><br><span data-ttu-id="be3f5-116">Til hamingju!</span><span class="sxs-lookup"><span data-stu-id="be3f5-116">Congratulations!</span></span> <span data-ttu-id="be3f5-117">Fríðindaskráningu hefur verið lokið.</span><span class="sxs-lookup"><span data-stu-id="be3f5-117">You’ve successfully completed benefits enrollment.</span></span><br><br><span data-ttu-id="be3f5-118">Takk fyrir,</span><span class="sxs-lookup"><span data-stu-id="be3f5-118">Thank you,</span></span><br><span data-ttu-id="be3f5-119"><Company/Org name> Fríðindi.</span><span class="sxs-lookup"><span data-stu-id="be3f5-119"><Company/Org name> Benefits.</span></span> |
   | <span data-ttu-id="be3f5-120">**Sjálfgefið netfang sendanda**</span><span class="sxs-lookup"><span data-stu-id="be3f5-120">**Default email sender address**</span></span> | <span data-ttu-id="be3f5-121">Netfangið sem á að nota þegar staðfestingarpóstur er sendur.</span><span class="sxs-lookup"><span data-stu-id="be3f5-121">The email address to use when sending the confirmation email.</span></span> |

3. <span data-ttu-id="be3f5-122">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="be3f5-122">Select **Save**.</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]