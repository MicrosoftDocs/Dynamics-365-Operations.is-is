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
ms.openlocfilehash: 2943d0095e4c9421725b90e579b7cbb841038ab7
ms.sourcegitcommit: fd097f6f76f0d8428038fa3655b3188bf093b517
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/08/2020
ms.locfileid: "4692746"
---
# <a name="configure-benefits-management-parameters-per-company"></a><span data-ttu-id="5229c-103">Grunnstilla færibreytur fríðindastjórnunar eftir fyrirtæki</span><span class="sxs-lookup"><span data-stu-id="5229c-103">Configure Benefits management parameters per company</span></span>

<span data-ttu-id="5229c-104">Fyrir hvert fyrirtæki sem býður upp á fríðindi verður að skilgreina stillingar fyrir staðfestingartölvupóst fyrir fríðindi.</span><span class="sxs-lookup"><span data-stu-id="5229c-104">For each organization that offers benefits, you must configure settings for benefits confirmation emails.</span></span>

## <a name="configure-confirmation-email-settings"></a><span data-ttu-id="5229c-105">Skilgreina stillingar staðfestingartölvupósts</span><span class="sxs-lookup"><span data-stu-id="5229c-105">Configure confirmation email settings</span></span>

1. <span data-ttu-id="5229c-106">Í **Fríðindastjórnun** vinnusvæðinu, undir **Uppsetning**, skal velja **Færibreytur mannauðs**.</span><span class="sxs-lookup"><span data-stu-id="5229c-106">In the **Benefits management** workspace, under **Setup**, select **Human Resources Parameters**.</span></span>

2. <span data-ttu-id="5229c-107">Í flipanum **Fríðindastjórnun** skal tilgreina gildi fyrir eftirfarandi reiti:</span><span class="sxs-lookup"><span data-stu-id="5229c-107">In the **Benefits management** tab, specify values for the following fields:</span></span> 

   | <span data-ttu-id="5229c-108">Svæði</span><span class="sxs-lookup"><span data-stu-id="5229c-108">Field</span></span> | <span data-ttu-id="5229c-109">lýsing</span><span class="sxs-lookup"><span data-stu-id="5229c-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="5229c-110">**Senda staðfestingarpóst**</span><span class="sxs-lookup"><span data-stu-id="5229c-110">**Send confirmation email**</span></span> | <span data-ttu-id="5229c-111">Þegar kveikt er á þessum eiginleika er staðfestingartölvupóstur sendur á starfsmenn þegar þeir skrá sig út úr fríðindaskráningu í sjálfsafgreiðslu starfsmanna.</span><span class="sxs-lookup"><span data-stu-id="5229c-111">When this feature is on, a confirmation email will be sent to employees when they check out from the benefits enrollment experience in Employee self-service.</span></span> |
   | <span data-ttu-id="5229c-112">**Sniðmát fyrir staðfestingartölvupóst**</span><span class="sxs-lookup"><span data-stu-id="5229c-112">**Confirmation email template**</span></span> | <span data-ttu-id="5229c-113">Veljið tölvupóstssniðmát fyrirtækis sem á að nota þegar staðfesting skráningar er send.</span><span class="sxs-lookup"><span data-stu-id="5229c-113">Select the organization email template to use when sending the enrollment confirmation.</span></span> <span data-ttu-id="5229c-114">Ef þú velur ekki sniðmát er eftirfarandi almennur tölvupóstur sendur:</span><span class="sxs-lookup"><span data-stu-id="5229c-114">If you don't select a template, the following generic email will be sent:</span></span><br><br><span data-ttu-id="5229c-115">%EmployeeFirstName%,</span><span class="sxs-lookup"><span data-stu-id="5229c-115">%EmployeeFirstName%,</span></span><br><br><span data-ttu-id="5229c-116">Til hamingju!</span><span class="sxs-lookup"><span data-stu-id="5229c-116">Congratulations!</span></span> <span data-ttu-id="5229c-117">Fríðindaskráningu hefur verið lokið.</span><span class="sxs-lookup"><span data-stu-id="5229c-117">You’ve successfully completed benefits enrollment.</span></span><br><br><span data-ttu-id="5229c-118">Takk fyrir,</span><span class="sxs-lookup"><span data-stu-id="5229c-118">Thank you,</span></span><br><span data-ttu-id="5229c-119"><Company/Org name> Fríðindi.</span><span class="sxs-lookup"><span data-stu-id="5229c-119"><Company/Org name> Benefits.</span></span> |
   | <span data-ttu-id="5229c-120">**Sjálfgefið netfang sendanda**</span><span class="sxs-lookup"><span data-stu-id="5229c-120">**Default email sender address**</span></span> | <span data-ttu-id="5229c-121">Netfangið sem á að nota þegar staðfestingarpóstur er sendur.</span><span class="sxs-lookup"><span data-stu-id="5229c-121">The email address to use when sending the confirmation email.</span></span> |

3. <span data-ttu-id="5229c-122">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="5229c-122">Select **Save**.</span></span>