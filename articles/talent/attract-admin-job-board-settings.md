---
title: Virkja Broadbean-samþættingu í Microsoft Dynamics 365 for Talent - Attract
description: Þetta efni útskýrir hvernig á að stilla Microsoft Dynamics 365 for Talent - Attract til að birta störf í utanaðkomandi atvinnutorgum eins og Broadbean.
author: andreabichsel
manager: AnnBe
ms.date: 07/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-07-08
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 2334c2bd0edccf3000f8d91651afafd4619ad0b8
ms.sourcegitcommit: 7c49475402632069685df714546770d30804af7f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/11/2019
ms.locfileid: "1739680"
---
# <a name="enable-broadbean-integration"></a><span data-ttu-id="51e07-103">Virkja Broadbean-samþættingu</span><span class="sxs-lookup"><span data-stu-id="51e07-103">Enable Broadbean integration</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="51e07-104">Þú vilt að sem flestir hæfir umsækjendur sjái lausu stöðurnar þínar.</span><span class="sxs-lookup"><span data-stu-id="51e07-104">You want to get your open positions in front of as many qualified candidates as possible.</span></span> <span data-ttu-id="51e07-105">Ráðningarsíður á borð við Broadbean auðvelda þér að ná þessu markmiði.</span><span class="sxs-lookup"><span data-stu-id="51e07-105">Recruiting sites such as Broadbean help you accomplish this goal.</span></span> <span data-ttu-id="51e07-106">Microsoft Dynamics 365 for Talent 365 Talent: Attract gerir þér nú kleift að birta störf í Broadbean og Microsoft er stöðugt að bjóða upp á nýjar leiðir í þessum efnum.</span><span class="sxs-lookup"><span data-stu-id="51e07-106">Microsoft Dynamics 365 for Talent: Attract now lets you post jobs to Broadbean, and Microsoft is constantly providing new offerings in this area.</span></span>

> [!NOTE]
> - <span data-ttu-id="51e07-107">Til að auglýsa störf á utanaðkomandi síðum verður þú að hafa [Viðbót við alhliða ráðningar](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span><span class="sxs-lookup"><span data-stu-id="51e07-107">To post jobs to external sites, you must have the [Comprehensive hiring add-on](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span></span>
> - <span data-ttu-id="51e07-108">Til að birta störf í Broadbean í gegnum Attract er nauðsynlegt að vera með Broadbean-áskrift.</span><span class="sxs-lookup"><span data-stu-id="51e07-108">To post jobs to Broadbean through Attract, you must have a Broadbean subscription.</span></span>
> - <span data-ttu-id="51e07-109">Þessi eiginleiki er í forútgáfu sem stendur.</span><span class="sxs-lookup"><span data-stu-id="51e07-109">This feature is currently in preview.</span></span> <span data-ttu-id="51e07-110">Ef þú vilt prófa hann verður þú að [kveikja á honum í stjórnandastillingum Attract](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span><span class="sxs-lookup"><span data-stu-id="51e07-110">If you want to try it, you must [turn it on in the Attract admin settings](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span></span>

## <a name="configure-broadbean-integration"></a><span data-ttu-id="51e07-111">Skilgreina Broadbean-samþættingu</span><span class="sxs-lookup"><span data-stu-id="51e07-111">Configure Broadbean integration</span></span>

1. <span data-ttu-id="51e07-112">Skráðu þig inn í Attract sem stjórnandi.</span><span class="sxs-lookup"><span data-stu-id="51e07-112">Sign in to Attract as an admin.</span></span>

2. <span data-ttu-id="51e07-113">Veldu hnappinn **Stillingar** (gírtáknið) efst í hægra horni síðunnar og veldu síðan **Stjórnandamiðstöð**.</span><span class="sxs-lookup"><span data-stu-id="51e07-113">Select the **Settings** button (the gear symbol) in the upper-right corner of the page, and then select **Admin center**.</span></span>

3. <span data-ttu-id="51e07-114">Hafðu samband við Broadbean og færðu inn upplýsingarnar í reitunum **Notandanafn**, **Biðlarakenni** og **Dulritunarlykli**.</span><span class="sxs-lookup"><span data-stu-id="51e07-114">Contact Broadbean, and enter your information in the **Username**, **Client ID**, and **Encryption Token** fields.</span></span>

4. <span data-ttu-id="51e07-115">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="51e07-115">Select **Save**.</span></span>

> [!WARNING]
> <span data-ttu-id="51e07-116">Broadbean-aðgangsupplýsingarnar þínar eru viðkvæmar og trúnaðarmál.</span><span class="sxs-lookup"><span data-stu-id="51e07-116">Your Broadbean credentials are sensitive and confidential.</span></span> <span data-ttu-id="51e07-117">Þar af leiðandi skaltu geyma og deila þeim af varkárni.</span><span class="sxs-lookup"><span data-stu-id="51e07-117">Therefore, store and share them responsibly.</span></span> <span data-ttu-id="51e07-118">Hver sá sem gegnir stjórnandahlutverki í Attract getur skoðað þessar aðgangsupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="51e07-118">Anyone who has an Administrator role in Attract can view these credentials.</span></span>

> [!NOTE]
> <span data-ttu-id="51e07-119">Microsoft og Attract taka engan þátt í að búa til og viðhalda þessum gildum.</span><span class="sxs-lookup"><span data-stu-id="51e07-119">Microsoft and Attract aren't involved in creating and maintaining these values.</span></span> <span data-ttu-id="51e07-120">Það er á þína ábyrgð að halda þeim uppfærðum í Attract og vinna með Broadbean til að leysa úr öllum vandamálum sem hafa með aðgangsupplýsingarnar þínar að gera.</span><span class="sxs-lookup"><span data-stu-id="51e07-120">It's your responsibility to keep them up to date in Attract and to work with Broadbean to resolve any issues that involve your credentials.</span></span>
