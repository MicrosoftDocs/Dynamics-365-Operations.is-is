---
title: "Skilgreiningar lánardrottinsbeiðni"
description: "Þetta efnisatriði lýsir svæðunum sem nauðsynlegt er að fylla í nýrri lánardrottnabeiðni."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendProspectiveVendorRegistrationConfig
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 9089b9ad773890424a6f73107a26a35a32e988ae
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---

# <a name="vendor-request-configurations"></a><span data-ttu-id="78902-103">Skilgreiningar lánardrottinsbeiðni</span><span class="sxs-lookup"><span data-stu-id="78902-103">Vendor request configurations</span></span>
[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="78902-104">Til að ljúka lánardrottnabeiðni þarf tengiliður lánardrottins að fara í gegnum leiðsagnarforrit fyrir skráningu væntanlegs lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="78902-104">To complete a vendor request, a vendor contact person must complete the prospective vendor registration wizard.</span></span>

<span data-ttu-id="78902-105">Í **Grunnstillingar lánardrottinsbeiðni** skjámyndinni getur þú stofnað forstillingar sem tilgreina svæði og sýnilegar svæði í leiðsagnarforriti fyrir skráningu væntanlegs lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="78902-105">In the **Vendor request configurations** form, you can create profiles that specify required fields and visible fields in the prospective vendor registration wizard.</span></span>

<span data-ttu-id="78902-106">Leiðsagnarforrit fyrir skráningu lánardrottins byrjar á því að spyrja væntanlegan lánardrottin hvaða land/svæði lánardrottinn á viðskipti í.</span><span class="sxs-lookup"><span data-stu-id="78902-106">The vendor registration wizard will start out by asking the prospective vendor user which country/region the vendor is doing business in.</span></span> <span data-ttu-id="78902-107">Þessar upplýsingar ákvarða viðeigandi grunnstillingu.</span><span class="sxs-lookup"><span data-stu-id="78902-107">This information determines the applicable configuration.</span></span> <span data-ttu-id="78902-108">Ef engin ákveðin grunnstilling er skilgreind fyrir land/svæði verður sjálfgefið grunnstillingar notað.</span><span class="sxs-lookup"><span data-stu-id="78902-108">If no specific configuration is defined for a country/region, a default configuration will be used.</span></span>

### <a name="set-up-a-vendor-request-configuration"></a><span data-ttu-id="78902-109">Setja upp grunnstillingar lánardrottinsbeiðni</span><span class="sxs-lookup"><span data-stu-id="78902-109">Set up a vendor request configuration</span></span>

<span data-ttu-id="78902-110">Sjálfgefið er að lánardrottins grunnstilling sé tiltæk í skjámynd grunnstillinga lánardrottinsbeiðni.</span><span class="sxs-lookup"><span data-stu-id="78902-110">By default, there is a vendor configuration available in the Vendor request configurations form.</span></span>

<span data-ttu-id="78902-111">Ekki er hægt að velja land/svæði fyrir sjálfgefna grunnstillingu, þannig að ekki er hægt að breyta **Löndum/svæðum**.</span><span class="sxs-lookup"><span data-stu-id="78902-111">It is not possible to select country/regions for the default configuration, so the **Countries/regions** section cannot be changed.</span></span>

1. <span data-ttu-id="78902-112">Smelltu á **Innkaup og aðföng** > **Uppsetning** > **Lánardrottnar**, og smelltu síðan á **Grunnstillingar lánardrottinsbeiðni**.</span><span class="sxs-lookup"><span data-stu-id="78902-112">Click **Procurement and sourcing** > **Setup** > **Vendors**, and then click **Vendor request configurations**.</span></span>
2. <span data-ttu-id="78902-113">Smelltu á flipann **Svæði** til að stilla staða skráðra svæða.</span><span class="sxs-lookup"><span data-stu-id="78902-113">Click the **Fields** tab to set the status of the listed fields.</span></span>
3. <span data-ttu-id="78902-114">Falið (ekki sýnilegt)</span><span class="sxs-lookup"><span data-stu-id="78902-114">Hidden (Not visible)</span></span>
4. <span data-ttu-id="78902-115">Sýnt (sýnilegt en ekki skylt)</span><span class="sxs-lookup"><span data-stu-id="78902-115">Displayed (Visible but not mandatory)</span></span>
5. <span data-ttu-id="78902-116">Nauðsynlegt (sýnilegt og skylt)</span><span class="sxs-lookup"><span data-stu-id="78902-116">Required (Visible and mandatory)</span></span>
6. <span data-ttu-id="78902-117">Smelltu á flipann **Innihald** til að tilgreina hvort textinn á að sjást í leiðsagnarforritinu og hvort það ætti að vera viðurkenning á því að væntanlegur lánardrottna notandi verður að samþykkja þetta áður en hann fer í næsta skref í leiðsagnarforritinu.</span><span class="sxs-lookup"><span data-stu-id="78902-117">Click the **Content** tab to specify if text is going to be shown on the wizard and if there should be an acknowledgement that the prospective vendor user must accept this before moving to the next step in the wizard.</span></span> <span data-ttu-id="78902-118">Beðið verður um viðurkenninguna fyrir hvaða skilmála og skilyrði sem notandinn verður að samþykkja til að halda áfram.</span><span class="sxs-lookup"><span data-stu-id="78902-118">The acknowledgement will be requested for any terms and conditions that the user must accept to continue.</span></span>

<span data-ttu-id="78902-119">Þú getur einnig slegið inn staðfestingarskilaboð sem munu birtast þegar búið er að fara í gegnum leiðsagnarforritið, og þú getur bætt við einni eða fleiri spurningalistum.</span><span class="sxs-lookup"><span data-stu-id="78902-119">You can also enter a confirmation message that will be displayed when the wizard is finalized, and you can add one or more questionnaires.</span></span>

### <a name="create-a-vendor-configuration-for-a-specific-countryregion"></a><span data-ttu-id="78902-120">Búa til grunnstillingar lánardrottins fyrir tiltekna land/svæði</span><span class="sxs-lookup"><span data-stu-id="78902-120">Create a vendor configuration for a specific country/region</span></span>
1.  <span data-ttu-id="78902-121">Smelltu á **Innkaup og aðföng** > **Uppsetning** > **Lánardrottnar**, og smelltu síðan á **Grunnstillingar lánardrottinsbeiðni**.</span><span class="sxs-lookup"><span data-stu-id="78902-121">Click **Procurement and sourcing** > **Setup** > **Vendors**, and then click **Vendor request configurations**.</span></span>
2.  <span data-ttu-id="78902-122">Smellt er á **Ný** til að búa til nýjar grunnstillingu, og nafn á grunnstillinguna.</span><span class="sxs-lookup"><span data-stu-id="78902-122">Click **New** to create a new configuration, and provide a name for the configuration.</span></span>
3.  <span data-ttu-id="78902-123">Smellið á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="78902-123">Click **Save**.</span></span>
4.  <span data-ttu-id="78902-124">Opnaðu flipann **Land/svæði** til að velja landið/svæðið sem á að nota grunnstillinguna fyrir.</span><span class="sxs-lookup"><span data-stu-id="78902-124">Open the **Country/regions** tab to select the country/region that the configuration should be used for.</span></span>
5.  <span data-ttu-id="78902-125">Ljúktu grunnstillingunni með því að fylgja leiðbeiningunum um sjálfgefna grunnstillingu.</span><span class="sxs-lookup"><span data-stu-id="78902-125">Complete the configuration by following the guidelines for the default configuration.</span></span>


