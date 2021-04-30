---
title: Sending lítilla pakka
description: Í þessu efnisatriði er að finna upplýsingar um eiginleika lítilla pakkasendinga (SPS). Þessi eiginleiki gerir Microsoft Dynamics 365 Supply Chain Management kleift að senda inn upplýsingar um pakkaða gáma til flutningsaðila og fá síðan merkimiða, flutningstaxta og rakningarnúmer aftur frá flutningsaðila.
author: Mirzaab
ms.date: 01/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSRateEngine, TMSCarrier, CustTable, TMSShippingCarrierCustomerAccount, TMSSmallParcelShippingFeature
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-08
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 3e72959d79e9b3b03e061a0f26750e3bd025219e
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/16/2021
ms.locfileid: "5910210"
---
# <a name="small-parcel-shipping"></a><span data-ttu-id="fd09c-104">Sending lítilla pakka</span><span class="sxs-lookup"><span data-stu-id="fd09c-104">Small parcel shipping</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fd09c-105">Eiginleiki lítilla pakkasendinga (SPS) gerir Microsoft Dynamics 365 Supply Chain Management kleift að eiga bein samskipti við farmflytjendur með því að bjóða upp á samskiptaramma í gegnum API flutningsaðila.</span><span class="sxs-lookup"><span data-stu-id="fd09c-105">The small parcel shipping (SPS) feature enables Microsoft Dynamics 365 Supply Chain Management to interact directly with shipping carriers by providing a framework for communication through carrier APIs.</span></span> <span data-ttu-id="fd09c-106">Þessi virkni er gagnleg þegar einstakar sölupantanir eru sendar í gegnum flutningsfyrirtæki í stað þess að nota gámaflutning eða sendingar sem eru minni en fullhlaðinn trukkur (LTL).</span><span class="sxs-lookup"><span data-stu-id="fd09c-106">This functionality is useful when you're shipping individual sales orders via commercial shipping carriers instead of using container shipping or less-than-truckload (LTL) shipping.</span></span>

<span data-ttu-id="fd09c-107">SPS-eiginleikinn á samskipti við farmflytjandann í gegnum sérstaka *taxtavél*.</span><span class="sxs-lookup"><span data-stu-id="fd09c-107">The SPS feature interacts with your shipping carrier through a dedicated *rate engine*.</span></span> <span data-ttu-id="fd09c-108">Fyrirtækið verður að þróa þessa taxtavél í samstarfi við flutningsaðilann eða miðstöð flutningsþjónustunnar.</span><span class="sxs-lookup"><span data-stu-id="fd09c-108">Your organization must develop this rate engine in collaboration with your carrier or carrier hub service.</span></span> <span data-ttu-id="fd09c-109">Þessi taxtavél gerir Supply Chain Management kleift að senda inn upplýsingar um pakkaða gáma til flutningsaðila og fá síðan merkimiða, flutningstaxta og rakningarnúmer aftur frá flutningsaðila.</span><span class="sxs-lookup"><span data-stu-id="fd09c-109">The rate engine enables Supply Chain Management to submit details about a packed container to your carrier, and then receive a shipping label, shipping rate, and tracking number back from that carrier.</span></span>

<span data-ttu-id="fd09c-110">Flutningstaxtanum sem er skilað er bætt við viðeigandi sölupöntun sem gjaldi.</span><span class="sxs-lookup"><span data-stu-id="fd09c-110">The shipping rate that is returned is added to the associated sales order as a miscellaneous charge.</span></span> <span data-ttu-id="fd09c-111">Merkimiðanum sem er skilað er síðan hægt að prenta með því að nota prentara Zebra-forritunarmáls (ZPL) og nota hann fyrir sendinguna.</span><span class="sxs-lookup"><span data-stu-id="fd09c-111">The shipping label that is returned can then automatically be printed by using a Zebra Programming Language (ZPL) printer and applied to the shipment.</span></span> <span data-ttu-id="fd09c-112">Flutningsaðilinn mun skanna þennan merkimiða þegar hann sækir pakkana í vöruhúsinu.</span><span class="sxs-lookup"><span data-stu-id="fd09c-112">The carrier will scan this shipping label when it picks up the packages at your warehouse.</span></span>

## <a name="prepare-your-system-to-support-sps"></a><span data-ttu-id="fd09c-113">Undirbúa kerfið fyrir stuðning við SPS</span><span class="sxs-lookup"><span data-stu-id="fd09c-113">Prepare your system to support SPS</span></span>

<span data-ttu-id="fd09c-114">Áður en hægt er að byrja að nota SPS-virkni þarf að kveikja á SPS-eiginleikanum í eiginleikastjórnun, bæta við taxtavélinni og setja upp einingarnar **Flutningsstjórnun** og **Vöruhúsakerfi** til að styðja við hana.</span><span class="sxs-lookup"><span data-stu-id="fd09c-114">Before you can start to use SPS functionality, you must turn on the SPS feature in Feature management, add your rate engine, and set up the **Transportation management** and **Warehouse management** modules to support it.</span></span>

### <a name="turn-on-the-sps-feature"></a><span data-ttu-id="fd09c-115">Kveikja á SPS-eiginleikanum</span><span class="sxs-lookup"><span data-stu-id="fd09c-115">Turn on the SPS feature</span></span>

<span data-ttu-id="fd09c-116">Áður en hægt er að nota SPS-eiginleikann verður að vera kveikt á honum í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="fd09c-116">Before you can use the SPS feature, it must be turned on in your system.</span></span> <span data-ttu-id="fd09c-117">Stjórnendur geta notað vinnusvæðið [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikja á honum ef þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="fd09c-117">Administrators can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="fd09c-118">Þar er eiginleikinn sýndur á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="fd09c-118">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="fd09c-119">**Eining:** *Flutningsstjórnun*</span><span class="sxs-lookup"><span data-stu-id="fd09c-119">**Module:** *Transportation management*</span></span>
- <span data-ttu-id="fd09c-120">**Heiti eiginleika:** *Sending lítilla pakka*</span><span class="sxs-lookup"><span data-stu-id="fd09c-120">**Feature name:** *Small parcel shipping*</span></span>

### <a name="deploy-and-set-up-rate-engines"></a><span data-ttu-id="fd09c-121">Nota og setja upp taxtavélar</span><span class="sxs-lookup"><span data-stu-id="fd09c-121">Deploy and set up rate engines</span></span>

<span data-ttu-id="fd09c-122">Supply Chain Management inniheldur engar taxtavélar.</span><span class="sxs-lookup"><span data-stu-id="fd09c-122">Supply Chain Management doesn't include any rate engines.</span></span> <span data-ttu-id="fd09c-123">Sækja þarf eða stofna nauðsynlegar taxtavélar og síðan bæta þeim við kerfið.</span><span class="sxs-lookup"><span data-stu-id="fd09c-123">You must obtain or create any rate engines that you require, and then add them to your system.</span></span> <span data-ttu-id="fd09c-124">Hins vegar býður Microsoft upp á sýnitaxtavél sem hægt er að nota til prófunar.</span><span class="sxs-lookup"><span data-stu-id="fd09c-124">However, Microsoft provides a demo rate engine that you can use for testing.</span></span>

#### <a name="download-and-deploy-the-demo-rate-engine"></a><span data-ttu-id="fd09c-125">Hlaða niður og nota prufutaxtavél</span><span class="sxs-lookup"><span data-stu-id="fd09c-125">Download and deploy the demo rate engine</span></span>

<span data-ttu-id="fd09c-126">Fylgið þessum skrefum til að fá sýniútgáfu af taxtavél.</span><span class="sxs-lookup"><span data-stu-id="fd09c-126">Follow these steps to get the demo rate engine.</span></span>

1. <span data-ttu-id="fd09c-127">Í GitHub skal sækja [DLL fyrir sýniútgáfu taxtavélar](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/SCM/SPS).</span><span class="sxs-lookup"><span data-stu-id="fd09c-127">On GitHub, download the [dynamic-link library (DLL) for the demo rate engine](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/SCM/SPS).</span></span>
1. <span data-ttu-id="fd09c-128">Á Supply Chain Management-þjóninum skal vista DLL í möppunni **\\AOSService\\PackagesLocalDirectory\\ApplicationSuite\\bin**.</span><span class="sxs-lookup"><span data-stu-id="fd09c-128">On your Supply Chain Management server, save the DLL in the **\\AOSService\\PackagesLocalDirectory\\ApplicationSuite\\bin** folder.</span></span>

#### <a name="create-and-deploy-functional-rate-engines"></a><span data-ttu-id="fd09c-129">Stofna og nota virkar taxtavélar</span><span class="sxs-lookup"><span data-stu-id="fd09c-129">Create and deploy functional rate engines</span></span>

<span data-ttu-id="fd09c-130">Upplýsingar um hvernig á að stofna og setja upp virkar taxtavélar þannig að hægt sé að nota þær í framleiðslu- eða prófunarumhverfi er að finna í eftirfarandi efnisatriðum:</span><span class="sxs-lookup"><span data-stu-id="fd09c-130">For information about how to create and deploy functional rate engines so that they can be used in a production or test environment, see the following topics:</span></span>

- [<span data-ttu-id="fd09c-131">Stofna nýja flutningsstjórnunarvél</span><span class="sxs-lookup"><span data-stu-id="fd09c-131">Create a new transportation management engine</span></span>](../transportation/create-new-transportation-management-engine.md)
- [<span data-ttu-id="fd09c-132">Setja upp flutningsstjórnunarvélar</span><span class="sxs-lookup"><span data-stu-id="fd09c-132">Set up transportation management engines</span></span>](/dynamicsax-2012/appuser-itpro/set-up-transportation-management-engines)

<span data-ttu-id="fd09c-133">Frekari upplýsingar um hvernig á að búa til SPS-taxtavél er að finna í eftirfarandi bloggfærslu: [Sending lítilla pakka: Hvernig á að nýta sér virkni lítilla pakkasendinga í Microsoft Dynamics 365](https://hub.bhsolutions.com/creating-a-mock-parcel-engine-in-d365?submissionGuid=46a1fccf-80b0-4b70-a6a0-4bf45a8756b5).</span><span class="sxs-lookup"><span data-stu-id="fd09c-133">For more information about how to create an SPS rate engine, see the following blog post: [Small Parcel Shipping: How to leverage small parcel shipping functionality in Microsoft Dynamics 365](https://hub.bhsolutions.com/creating-a-mock-parcel-engine-in-d365?submissionGuid=46a1fccf-80b0-4b70-a6a0-4bf45a8756b5).</span></span>

#### <a name="set-up-a-rate-engine-in-supply-chain-management"></a><span data-ttu-id="fd09c-134">Setja upp taxtavél í Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="fd09c-134">Set up a rate engine in Supply Chain Management</span></span>

<span data-ttu-id="fd09c-135">Þegar búið er að stofna og virkja taxtavél fyrir SPS skal fylgja þessum skrefum til að setja hana upp.</span><span class="sxs-lookup"><span data-stu-id="fd09c-135">After you've created and deployed a rate engine for SPS, follow these steps to set it up.</span></span>

1. <span data-ttu-id="fd09c-136">Opnið **Flutningsstjórnun \> Uppsetning \> Vélar \> Taxtavél**.</span><span class="sxs-lookup"><span data-stu-id="fd09c-136">Go to **Transportation management \> Setup \> Engines \> Rate engine**.</span></span>
1. <span data-ttu-id="fd09c-137">Á aðgerðasvæðinu skal velja **Ný** til að bæta línu við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="fd09c-137">On the Action Pane, select **New** to add a row to the grid.</span></span>
1. <span data-ttu-id="fd09c-138">Í nýju línunni skal stilla eftirfarandi reiti:</span><span class="sxs-lookup"><span data-stu-id="fd09c-138">In the new row, set the following fields:</span></span>

    - <span data-ttu-id="fd09c-139">**Taxtavél** – Sláið inn einkvæmt heiti fyrir taxtavél.</span><span class="sxs-lookup"><span data-stu-id="fd09c-139">**Rating engine** – Enter a unique name for the rate engine.</span></span> <span data-ttu-id="fd09c-140">Ef sýniútgáfa taxtavélar er notuð skal slá inn *Sýniútgáfa taxtavélar*.</span><span class="sxs-lookup"><span data-stu-id="fd09c-140">If you're using the demo rate engine, enter *Demo rate engine*.</span></span>
    - <span data-ttu-id="fd09c-141">**Heiti** – Færa skal inn stutta lýsingu á taxtavélinni.</span><span class="sxs-lookup"><span data-stu-id="fd09c-141">**Name** – Enter a short description of the rate engine.</span></span> <span data-ttu-id="fd09c-142">Ef sýniútgáfa taxtavélar er notuð skal slá inn *Sýniútgáfa taxtavélar*.</span><span class="sxs-lookup"><span data-stu-id="fd09c-142">If you're using the demo rate engine, enter *Demo rate engine*.</span></span>
    - <span data-ttu-id="fd09c-143">**Lýsigagnakenni fyrir taxta** – Veljið grunninn sem á að nota til að reikna út taxtann.</span><span class="sxs-lookup"><span data-stu-id="fd09c-143">**Rating metadata ID** – Select the basis that should be used to calculate your rate.</span></span> <span data-ttu-id="fd09c-144">Til dæmis gæti gengi notanda verið reiknað út frá vegalengd.</span><span class="sxs-lookup"><span data-stu-id="fd09c-144">For example, your rate might be calculated based on distance.</span></span> <span data-ttu-id="fd09c-145">Ef verið er að nota prufutaxtavélina er hægt að skilja þennan reit eftir auðan.</span><span class="sxs-lookup"><span data-stu-id="fd09c-145">If you're using the demo rate engine, you can leave this field blank.</span></span>
    - <span data-ttu-id="fd09c-146">**Vélarsamsetning** – Færið inn skráarheiti DLL-pakkans sem var virkjaður.</span><span class="sxs-lookup"><span data-stu-id="fd09c-146">**Engine assembly** – Enter the file name of the DLL package that you deployed.</span></span> <span data-ttu-id="fd09c-147">Ef prufutaxtavél er notuð skal færa inn *TMSSmallParcelShippingEngine.dll*.</span><span class="sxs-lookup"><span data-stu-id="fd09c-147">If you're using the demo rate engine, enter *TMSSmallParcelShippingEngine.dll*.</span></span>
    - <span data-ttu-id="fd09c-148">**Vélarklasi** – Færið inn klasaheitið sem var komið upp fyrir taxtavélina.</span><span class="sxs-lookup"><span data-stu-id="fd09c-148">**Engine class** – Enter the class name that was established for your rate engine.</span></span> <span data-ttu-id="fd09c-149">Ef sýniútgáfa taxtavélar er notuð skal færa inn *TMSSmallParcelShippingEngine.SmallParcelShippingRateEngine*.</span><span class="sxs-lookup"><span data-stu-id="fd09c-149">If you're using the demo rate engine, enter *TMSSmallParcelShippingEngine.SmallParcelShippingRateEngine*.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="fd09c-150">Dæmi</span><span class="sxs-lookup"><span data-stu-id="fd09c-150">Example scenario</span></span>

<span data-ttu-id="fd09c-151">Þetta dæmi sýnir hvernig á að setja upp og nota SPS eftir að búið er að undirbúa kerfið eins og lýst var hér á undan.</span><span class="sxs-lookup"><span data-stu-id="fd09c-151">This example scenario shows how to set up and use SPS after you've prepared your system as described earlier in this topic.</span></span> <span data-ttu-id="fd09c-152">Þessar aðstæður nota áðurnefnda sýniútgáfu taxtavélar.</span><span class="sxs-lookup"><span data-stu-id="fd09c-152">This scenario uses the previously mentioned demo rate engine.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="fd09c-153">Bjóða upp á sýnigögn</span><span class="sxs-lookup"><span data-stu-id="fd09c-153">Make demo data available</span></span>

<span data-ttu-id="fd09c-154">Til að vinna í gegnum þessar aðstæður með því að nota sýnigögnin og gildin sem eru tilgreind hér verður þú að vera á kerfi þar sem venjuleg [sýnigögn](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) er sett upp.</span><span class="sxs-lookup"><span data-stu-id="fd09c-154">To work through this scenario by using the demo records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="fd09c-155">Þar að auki verður þú að velja **USMF**-lögaðila áður en þú byrjar.</span><span class="sxs-lookup"><span data-stu-id="fd09c-155">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

### <a name="set-up-the-scenario"></a><span data-ttu-id="fd09c-156">Setja upp aðstæður</span><span class="sxs-lookup"><span data-stu-id="fd09c-156">Set up the scenario</span></span>

<span data-ttu-id="fd09c-157">Fyrir þetta dæmi þarf að vera með sýnidæmi um flutningsaðila, flutningsflokk, pökkunarreglu og pökkunarforstillingu.</span><span class="sxs-lookup"><span data-stu-id="fd09c-157">For this example scenario, you must have a demo carrier, carrier group, packing policy, and packing profile.</span></span> <span data-ttu-id="fd09c-158">Eftirfarandi undirkaflar útskýra hvernig á að undirbúa færslurnar sem eru nauðsynlegar fyrir aðstæðurnar.</span><span class="sxs-lookup"><span data-stu-id="fd09c-158">The following subsections explain how to prepare the records that are required for the scenario.</span></span> <span data-ttu-id="fd09c-159">Í framleiðsluaðstæðum líkist uppsetningarferlið yfirleitt ferlinu sem er lýst hér.</span><span class="sxs-lookup"><span data-stu-id="fd09c-159">In a production scenario, the setup process typically resembles the process that is described here.</span></span> <span data-ttu-id="fd09c-160">Hins vegar skal stilla önnur gildi.</span><span class="sxs-lookup"><span data-stu-id="fd09c-160">However, you will set different values.</span></span>

#### <a name="set-up-carriers"></a><span data-ttu-id="fd09c-161">Setja upp flutningsaðila</span><span class="sxs-lookup"><span data-stu-id="fd09c-161">Set up carriers</span></span>

<span data-ttu-id="fd09c-162">Fylgið þessum skrefum til að setja upp flutningsaðila.</span><span class="sxs-lookup"><span data-stu-id="fd09c-162">Follow these steps to set up a carrier.</span></span>

1. <span data-ttu-id="fd09c-163">Opnið **Flutningsstjórnun \> Uppsetning \> Flutningsaðilar \> Farmflytjendur**.</span><span class="sxs-lookup"><span data-stu-id="fd09c-163">Go to **Transportation management \> Setup \> Carriers \> Shipping carriers**.</span></span>
1. <span data-ttu-id="fd09c-164">Á aðgerðasvæðinu skal velja **Nýr** til að bæta við flutningsaðila.</span><span class="sxs-lookup"><span data-stu-id="fd09c-164">On the Action Pane, select **New** to add a carrier.</span></span>
1. <span data-ttu-id="fd09c-165">Stillið eftirfarandi gildi í hausnum:</span><span class="sxs-lookup"><span data-stu-id="fd09c-165">On the header, set the following values:</span></span>

    - <span data-ttu-id="fd09c-166">**Farmflytjandi:** *Sýnidæmi flutningsaðila*</span><span class="sxs-lookup"><span data-stu-id="fd09c-166">**Shipping carrier:** *Demo Carrier*</span></span>
    - <span data-ttu-id="fd09c-167">**Heiti:** *Sýnidæmi flutningsaðila*</span><span class="sxs-lookup"><span data-stu-id="fd09c-167">**Name:** *Demo Carrier*</span></span>
    - <span data-ttu-id="fd09c-168">**Stilling:** *Landflutningur*</span><span class="sxs-lookup"><span data-stu-id="fd09c-168">**Mode:** *Ground*</span></span>

1. <span data-ttu-id="fd09c-169">Stilltu eftirfarandi gildi á **Yfirlit** flipanum:</span><span class="sxs-lookup"><span data-stu-id="fd09c-169">On the **Overview** FastTab, set the following values:</span></span>

    - <span data-ttu-id="fd09c-170">**Virkja farmflytjanda:** *Já*</span><span class="sxs-lookup"><span data-stu-id="fd09c-170">**Activate shipping carrier:** *Yes*</span></span>
    - <span data-ttu-id="fd09c-171">**Virkja einkunn flutningsaðila:** *Já*</span><span class="sxs-lookup"><span data-stu-id="fd09c-171">**Activate carrier rating:** *Yes*</span></span>

1. <span data-ttu-id="fd09c-172">Á flýtiflipanum **Línur** skal velja **Ný** til að bæta línu við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="fd09c-172">On the **Services** FastTab, select **New** to add a service to the grid.</span></span>
1. <span data-ttu-id="fd09c-173">Stillið eftirfarandi gildi fyrir nýju þjónustuna:</span><span class="sxs-lookup"><span data-stu-id="fd09c-173">Set the following values for the new service:</span></span>

    - <span data-ttu-id="fd09c-174">**Flutningsþjónusta:** *Sýnidæmi flutningsþjónustu*</span><span class="sxs-lookup"><span data-stu-id="fd09c-174">**Carrier service:** *Demo carrier service*</span></span>
    - <span data-ttu-id="fd09c-175">**Heiti:** *Sýnidæmi flutningsþjónustu*</span><span class="sxs-lookup"><span data-stu-id="fd09c-175">**Name:** *Demo carrier service*</span></span>
    - <span data-ttu-id="fd09c-176">**Flutningsaðferð:** *Jörð*</span><span class="sxs-lookup"><span data-stu-id="fd09c-176">**Transportation method:** *Ground*</span></span>

    <span data-ttu-id="fd09c-177">Sláið inn handahófskennd gildi fyrir alla aðra reiti, eins og nauðsynlegt er.</span><span class="sxs-lookup"><span data-stu-id="fd09c-177">Enter arbitrary values for all the other fields, as required.</span></span> <span data-ttu-id="fd09c-178">(Þegar ný færsla farmflytjanda er vistuð verður nýr flutningsmáti stofnaður og reiturinn **Flutningsmáti** verður stilltur sjálfkrafa.)</span><span class="sxs-lookup"><span data-stu-id="fd09c-178">(When you save the new shipping carrier record, a new mode of delivery will be created, and the **Mode of delivery** field will be set automatically.)</span></span>

1. <span data-ttu-id="fd09c-179">Í flýtiflipanum **Taxtaforstillingar** skal velja **Ný** til að bæta taxtaforstillingu við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="fd09c-179">On the **Rating profiles** FastTab, select **New** to add a rating profile to the grid.</span></span>
1. <span data-ttu-id="fd09c-180">Stillið eftirfarandi gildi fyrir nýju forstillinguna:</span><span class="sxs-lookup"><span data-stu-id="fd09c-180">Set the following values for the new profile:</span></span>

    - <span data-ttu-id="fd09c-181">**Matsforstilling:** *Sýnidæmi flutningsþjónustu*</span><span class="sxs-lookup"><span data-stu-id="fd09c-181">**Rating profile:** *Demo carrier service*</span></span>
    - <span data-ttu-id="fd09c-182">**Heiti:** *Sýnidæmi flutningsþjónustu*</span><span class="sxs-lookup"><span data-stu-id="fd09c-182">**Name:** *Demo carrier service*</span></span>
    - <span data-ttu-id="fd09c-183">**Taxtavél:** *Sýniútgáfa taxtavélar*</span><span class="sxs-lookup"><span data-stu-id="fd09c-183">**Rate engine:** *Demo rate engine*</span></span>

    <span data-ttu-id="fd09c-184">Sláið inn handahófskennd gildi fyrir alla aðra reiti, eins og nauðsynlegt er.</span><span class="sxs-lookup"><span data-stu-id="fd09c-184">Enter arbitrary values for all the other fields, as required.</span></span>

1. <span data-ttu-id="fd09c-185">Í aðgerðarúðunni skal velja **Vista**.</span><span class="sxs-lookup"><span data-stu-id="fd09c-185">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="fd09c-186">Frekari upplýsingar um hvernig á að setja upp flutningsaðila er að finna í [Setja upp flutningsaðila](../transportation/tasks/set-up-shipping-carriers.md).</span><span class="sxs-lookup"><span data-stu-id="fd09c-186">For more information about how to set up carriers, see [Set up shipping carriers](../transportation/tasks/set-up-shipping-carriers.md).</span></span>

#### <a name="set-up-carrier-service-accounts"></a><span data-ttu-id="fd09c-187">Setja upp reikninga flutningsþjónustu</span><span class="sxs-lookup"><span data-stu-id="fd09c-187">Set up carrier service accounts</span></span>

<span data-ttu-id="fd09c-188">Fylgið þessum skrefum til að setja upp reikning flutningsþjónustu.</span><span class="sxs-lookup"><span data-stu-id="fd09c-188">Follow these steps to set up a carrier service account.</span></span>

1. <span data-ttu-id="fd09c-189">Opnið **Flutningsstjórnun \> Uppsetning \> Taxti \> Reikningur flutningsþjónustu**.</span><span class="sxs-lookup"><span data-stu-id="fd09c-189">Go to **Transportation management \> Setup \> Rating \> Carrier service account**.</span></span>
1. <span data-ttu-id="fd09c-190">Á aðgerðasvæðinu skal velja **Ný** til að bæta við flutningsþjónustureikningi.</span><span class="sxs-lookup"><span data-stu-id="fd09c-190">On the Action Pane, select **New** to add a carrier service account.</span></span>
1. <span data-ttu-id="fd09c-191">Stillið eftirfarandi gildi fyrir nýja reikninginn:</span><span class="sxs-lookup"><span data-stu-id="fd09c-191">Set the following values for the new account:</span></span>

    - <span data-ttu-id="fd09c-192">**Farmflytjandi:** *Sýnidæmi flutningsaðila*</span><span class="sxs-lookup"><span data-stu-id="fd09c-192">**Shipping Carrier:** *Demo Carrier*</span></span>
    - <span data-ttu-id="fd09c-193">**Flutningsþjónusta:** *Sýnidæmi flutningsþjónustu*</span><span class="sxs-lookup"><span data-stu-id="fd09c-193">**Carrier service:** *Demo carrier service*</span></span>
    - <span data-ttu-id="fd09c-194">**Númer viðskiptavinalykils flutningsaðila:** Númer viðskiptavinalykils flutningsaðila sem er notað til að sannprófa og auðkenna tenginguna við farmflytjandann.</span><span class="sxs-lookup"><span data-stu-id="fd09c-194">**Carrier customer account number:** The carrier customer account number that is used to verify and authenticate the connection to the shipping carrier.</span></span> <span data-ttu-id="fd09c-195">Flutningsaðilinn mun gefa upp þetta gildi.</span><span class="sxs-lookup"><span data-stu-id="fd09c-195">Your carrier will provide this value.</span></span> <span data-ttu-id="fd09c-196">Hægt er að færa inn handahófskennt gildi ef þú ert að nota prufuþjónustuna.</span><span class="sxs-lookup"><span data-stu-id="fd09c-196">If you're using the demo service, you can enter an arbitrary value.</span></span>
    - <span data-ttu-id="fd09c-197">**Svæði:** *6*</span><span class="sxs-lookup"><span data-stu-id="fd09c-197">**Site:** *6*</span></span>
    - <span data-ttu-id="fd09c-198">**Vöruhús:** *62*</span><span class="sxs-lookup"><span data-stu-id="fd09c-198">**Warehouse:** *62*</span></span>

    > [!NOTE]
    > <span data-ttu-id="fd09c-199">Oft er gildið **Númer viðskiptavinalykils flutningsaðila** er eina gildið sem þarf til að sannvotta tenginguna.</span><span class="sxs-lookup"><span data-stu-id="fd09c-199">Often, the **Carrier customer account number** value is the only value that is required to authenticate the connection.</span></span> <span data-ttu-id="fd09c-200">Hins vegar ef flutningsaðilinn krefst frekari færibreyta sannvottunar ætti fyrirtækið að sérstilla þessa síðu til að bæta við viðbótarreitum eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="fd09c-200">However, if your carrier requires additional authentication parameters, your organization should customize this page to add extra fields as appropriate.</span></span>

#### <a name="set-up-a-container-packing-policy"></a><span data-ttu-id="fd09c-201">Setja upp pökkunarreglur gáms</span><span class="sxs-lookup"><span data-stu-id="fd09c-201">Set up a container packing policy</span></span>

<span data-ttu-id="fd09c-202">Fylgið þessum skrefum til að setja upp pökkunarreglur gáms.</span><span class="sxs-lookup"><span data-stu-id="fd09c-202">Follow these steps to set up a container packing policy.</span></span>

1. <span data-ttu-id="fd09c-203">Ef ekki hefur þegar verið sett upp skilgreining ZPL-prentara skal nota forritið Document Routing Agent til að setja hana upp.</span><span class="sxs-lookup"><span data-stu-id="fd09c-203">If you haven't already set up a ZPL printer definition, use the Document Routing Agent application to set it up.</span></span> <span data-ttu-id="fd09c-204">Frekari upplýsingar er að finna í [Yfirlit skjalaprentunar](../../fin-ops-core/dev-itpro/analytics/print-documents.md) og tengdum efnisatriðum.</span><span class="sxs-lookup"><span data-stu-id="fd09c-204">For more information, see [Document printing overview](../../fin-ops-core/dev-itpro/analytics/print-documents.md) and related topics.</span></span>
1. <span data-ttu-id="fd09c-205">Fara í **Vöruhúsakerfi \> Uppsetning \> Gámar \> Pökkunarreglur gáms**.</span><span class="sxs-lookup"><span data-stu-id="fd09c-205">Go to **Warehouse Management \> Setup \> Containers \> Container packing policies**.</span></span>
1. <span data-ttu-id="fd09c-206">Á aðgerðasvæðinu skal velja **Ný** til að bæta við pökkkunarreglu gáms.</span><span class="sxs-lookup"><span data-stu-id="fd09c-206">On the Action Pane, select **New** to add a container packing policy.</span></span>
1. <span data-ttu-id="fd09c-207">Í haus nýju reglunnar skal stilla eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="fd09c-207">On the header of the new policy, set the following values:</span></span>

    - <span data-ttu-id="fd09c-208">**Pökkunarregla gáms:** *Sýnidæmi pökkunarreglu*</span><span class="sxs-lookup"><span data-stu-id="fd09c-208">**Container packing policy:** *Demo packing policy*</span></span>
    - <span data-ttu-id="fd09c-209">**Lýsing:** Lýsing á reglunni</span><span class="sxs-lookup"><span data-stu-id="fd09c-209">**Description:** A description of the policy</span></span>

1. <span data-ttu-id="fd09c-210">Stilltu eftirfarandi gildi á **Yfirlit** flipanum:</span><span class="sxs-lookup"><span data-stu-id="fd09c-210">On the **Overview** FastTab, set the following values:</span></span>

    - <span data-ttu-id="fd09c-211">**Vöruhús:** *62*</span><span class="sxs-lookup"><span data-stu-id="fd09c-211">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="fd09c-212">**Sjálfgefin staðsetning lokasendingar:** *Útskot*</span><span class="sxs-lookup"><span data-stu-id="fd09c-212">**Default location for final shipment:** *Baydoor*</span></span>
    - <span data-ttu-id="fd09c-213">**Þyngdareining:** *kg*</span><span class="sxs-lookup"><span data-stu-id="fd09c-213">**Weight unit:** *KG*</span></span>
    - <span data-ttu-id="fd09c-214">**Lokunarregla geymis:** *Sjálfvirk losun*</span><span class="sxs-lookup"><span data-stu-id="fd09c-214">**Container closing policy:** *Automatic release*</span></span>
    - <span data-ttu-id="fd09c-215">**Losunarregla geymis:** *Gera tiltækt á endanlegum sendingarstað*</span><span class="sxs-lookup"><span data-stu-id="fd09c-215">**Container release policy:** *Make available at final shipping location*</span></span>

1. <span data-ttu-id="fd09c-216">Stilltu eftirfarandi gildi á flýtiflipanum **Skrá geymis**:</span><span class="sxs-lookup"><span data-stu-id="fd09c-216">On the **Container manifest** FastTab, set the following values:</span></span>

    - <span data-ttu-id="fd09c-217">**Sjálfvirk skrá við lokun geymis:** *Já*</span><span class="sxs-lookup"><span data-stu-id="fd09c-217">**Automatic manifest at container close:** *Yes*</span></span>
    - <span data-ttu-id="fd09c-218">**Skráarkröfur fyrir gám:** *Flutningsstjórnun*</span><span class="sxs-lookup"><span data-stu-id="fd09c-218">**Manifest requirements for container:** *Transportation management*</span></span>
    - <span data-ttu-id="fd09c-219">**Prenta innihald gámsins:** *Nei*</span><span class="sxs-lookup"><span data-stu-id="fd09c-219">**Print container contents:** *No*</span></span>

1. <span data-ttu-id="fd09c-220">Í flýtiflipanum **Prentun merkimiða flutningsaðila** skal stilla eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="fd09c-220">On the **Carrier label printing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="fd09c-221">**Prenta merkimiða gáms:** *Alltaf*</span><span class="sxs-lookup"><span data-stu-id="fd09c-221">**Print container shipping label:** *Always*</span></span>
    - <span data-ttu-id="fd09c-222">**Prentaraheiti:** Heiti ZPL-prentarans sem á að prenta merkimiða</span><span class="sxs-lookup"><span data-stu-id="fd09c-222">**Printer name:** The name of the ZPL printer that should print shipping labels</span></span>

#### <a name="set-up-a-packing-profile"></a><span data-ttu-id="fd09c-223">Setja upp forstillingu umbúða</span><span class="sxs-lookup"><span data-stu-id="fd09c-223">Set up a packing profile</span></span>

<span data-ttu-id="fd09c-224">Fylgið þessum skrefum til að setja upp forstillingu umbúða.</span><span class="sxs-lookup"><span data-stu-id="fd09c-224">Follow these steps to set up a packing profile.</span></span>

1. <span data-ttu-id="fd09c-225">Fara í **Vöruhúsakerfi \> Uppsetning \> Pökkun \> Forstillingar umbúða**.</span><span class="sxs-lookup"><span data-stu-id="fd09c-225">Go to **Warehouse Management \> Setup \> Packing \> Packing profiles**.</span></span>
1. <span data-ttu-id="fd09c-226">Á aðgerðasvæðinu skal velja **Ný** til að bæta forstillingu umbúða við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="fd09c-226">On the Action Pane, select **New** to add a packing profile to the grid.</span></span>
1. <span data-ttu-id="fd09c-227">Stillið eftirfarandi gildi fyrir nýju forstillinguna:</span><span class="sxs-lookup"><span data-stu-id="fd09c-227">Set the following values for the new profile:</span></span>

    - <span data-ttu-id="fd09c-228">**Forstillingarkenni umbúða:** *Sýnidæmi umbúðaforstillingar*</span><span class="sxs-lookup"><span data-stu-id="fd09c-228">**Packing profile ID:** *Demo packing profile*</span></span>
    - <span data-ttu-id="fd09c-229">**Lýsing:** Lýsing á forstillingunni</span><span class="sxs-lookup"><span data-stu-id="fd09c-229">**Description:** A description of the profile</span></span>
    - <span data-ttu-id="fd09c-230">**Pökkunarregla gáms:** *Sýnidæmi pökkunarreglu*</span><span class="sxs-lookup"><span data-stu-id="fd09c-230">**Container packing policy:** *Demo packing policy*</span></span>
    - <span data-ttu-id="fd09c-231">**Auðkennisstilling gáms:** *Sjálfvirkt*</span><span class="sxs-lookup"><span data-stu-id="fd09c-231">**Container ID mode:** *Auto*</span></span>
    - <span data-ttu-id="fd09c-232">**Gámagerð:** *SmallBox*</span><span class="sxs-lookup"><span data-stu-id="fd09c-232">**Container type:** *SmallBox*</span></span>

#### <a name="set-up-a-customer-to-use-the-sps-carrier"></a><span data-ttu-id="fd09c-233">Setja upp viðskiptavin til að nota SPS-flutningsaðila</span><span class="sxs-lookup"><span data-stu-id="fd09c-233">Set up a customer to use the SPS carrier</span></span>

<span data-ttu-id="fd09c-234">Fylgdu þessum skrefum til að setja viðskiptavin upp þannig að hann geti notað flutningsaðilann sem var stofnaður.</span><span class="sxs-lookup"><span data-stu-id="fd09c-234">Follow these steps to set up a customer so that it can use the carrier that you created.</span></span>

1. <span data-ttu-id="fd09c-235">Farið í **Viðskiptakröfur \> Viðskiptavinir \> Allir viðskiptavinir**.</span><span class="sxs-lookup"><span data-stu-id="fd09c-235">Go to **Accounts receivable \> customers \> All customers**.</span></span>
1. <span data-ttu-id="fd09c-236">Í hnitanetinu skal finna og velja viðskiptavinur *US-027*.</span><span class="sxs-lookup"><span data-stu-id="fd09c-236">In the grid, find and select customer *US-027*.</span></span>
1. <span data-ttu-id="fd09c-237">Á aðgerðasvæðinu, í flipanum **Almennt**, í flokknum **Setja upp**, skal velja **Viðskiptavinalyklar flutningsaðila**.</span><span class="sxs-lookup"><span data-stu-id="fd09c-237">On the Action Pane, on the **General** tab, in the **Set up** group, select **Carrier customer accounts**.</span></span>
1. <span data-ttu-id="fd09c-238">Á síðunni **Viðskiptavinalyklar flutningsaðila**, á aðgerðasvæðinu, skal velja **Nýr** til að bæta nýjum lykli við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="fd09c-238">On the **Carrier customer accounts** page, on the Action Pane, select **New** to add an account to the grid.</span></span>
1. <span data-ttu-id="fd09c-239">Stillið eftirfarandi gildi fyrir nýja reikninginn:</span><span class="sxs-lookup"><span data-stu-id="fd09c-239">Set the following values for the new account:</span></span>

    - <span data-ttu-id="fd09c-240">**Farmflytjandi:** *Sýnidæmi flutningsaðila*</span><span class="sxs-lookup"><span data-stu-id="fd09c-240">**Shipping carrier:** *Demo Carrier*</span></span>
    - <span data-ttu-id="fd09c-241">**Númer viðskiptavinalykils flutningsaðila:** *12345* (Gildið er ekki mikilvægt fyrir þessar aðstæður, en það verður vísað í það í næsta hluta.)</span><span class="sxs-lookup"><span data-stu-id="fd09c-241">**Carrier customer account number:** *12345* (The value isn't important for this scenario, but it will be referred to in the next section.)</span></span>

### <a name="go-through-the-example-scenario"></a><span data-ttu-id="fd09c-242">Farið í gegnum sýnidæmið</span><span class="sxs-lookup"><span data-stu-id="fd09c-242">Go through the example scenario</span></span>

<span data-ttu-id="fd09c-243">Þegar búið er að setja upp öll sýnigögn eins og lýst var í hlutanum hér á undan er hægt að fara í gegnum sýnidæmið.</span><span class="sxs-lookup"><span data-stu-id="fd09c-243">After you've set up all the sample data as described in the previous section, you're ready to go through the example scenario.</span></span>

#### <a name="create-a-sales-order-and-process-the-work"></a><span data-ttu-id="fd09c-244">Stofna sölupöntun og vinna verk</span><span class="sxs-lookup"><span data-stu-id="fd09c-244">Create a sales order and process the work</span></span>

<span data-ttu-id="fd09c-245">Fylgdu þessum skrefum til að búa til sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="fd09c-245">Follow these steps to create a sales order.</span></span>

1. <span data-ttu-id="fd09c-246">Farðu í **Sölu og markaðssetningu \> Sölupöntun \> Allar sölupantanir**.</span><span class="sxs-lookup"><span data-stu-id="fd09c-246">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="fd09c-247">Smellið á **Nýtt** til að stofna nýja sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="fd09c-247">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="fd09c-248">Í svarglugganum **Stofna sölupöntun** skal stilla reitinn **Reikningur viðskiptavinar** á *US-027* .</span><span class="sxs-lookup"><span data-stu-id="fd09c-248">In the **Create sales order** dialog box, set the **Customer account** field to *US-027*.</span></span>
1. <span data-ttu-id="fd09c-249">Veljið **Í lagi** til að stofna sölupöntunina og loka svarglugganum.</span><span class="sxs-lookup"><span data-stu-id="fd09c-249">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="fd09c-250">Ný sölupöntun opnast.</span><span class="sxs-lookup"><span data-stu-id="fd09c-250">The new sales order is opened.</span></span> <span data-ttu-id="fd09c-251">Í flýtiflipanum **Sölupöntunarhaus** skal stilla reitinn **Númer viðskiptavinalykils flutningsaðila** á gildið sem var valið fyrir þennan viðskiptavin hér á undan (*12345*).</span><span class="sxs-lookup"><span data-stu-id="fd09c-251">On the **Sales order header** FastTab, set the **Carrier customer account number** field to the value that you selected for this customer earlier (*12345*).</span></span>
1. <span data-ttu-id="fd09c-252">Í hlutanum **Sölupöntunarlínur** skal bæta við sölulínu og stilla eftirfarandi gildi fyrir hana:</span><span class="sxs-lookup"><span data-stu-id="fd09c-252">In the **Sales order lines** section, add a sales line, and set the following values for it:</span></span>

    - <span data-ttu-id="fd09c-253">**Vörunúmer:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="fd09c-253">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="fd09c-254">**Magn:** *1*</span><span class="sxs-lookup"><span data-stu-id="fd09c-254">**Quantity:** *1*</span></span>
    - <span data-ttu-id="fd09c-255">**Svæði:** *6*</span><span class="sxs-lookup"><span data-stu-id="fd09c-255">**Site:** *6*</span></span>
    - <span data-ttu-id="fd09c-256">**Vöruhús:** *62*</span><span class="sxs-lookup"><span data-stu-id="fd09c-256">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="fd09c-257">Skiptið yfir í **Hausa** yfirlitið.</span><span class="sxs-lookup"><span data-stu-id="fd09c-257">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="fd09c-258">Í flýtiflipanum **Afhending** skal stilla eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="fd09c-258">On the **Delivery** FastTab, set the following values:</span></span>

    - <span data-ttu-id="fd09c-259">**Farmflytjandi:** *Sýnidæmi flutningsaðila*</span><span class="sxs-lookup"><span data-stu-id="fd09c-259">**Shipping carrier:** *Demo Carrier*</span></span>
    - <span data-ttu-id="fd09c-260">**Flutningsþjónusta:** *Sýnidæmi flutningsþjónustu*</span><span class="sxs-lookup"><span data-stu-id="fd09c-260">**Carrier service:** *Demo carrier service*</span></span>

1. <span data-ttu-id="fd09c-261">Skiptið aftur yfir í yfirlitið **Línur**.</span><span class="sxs-lookup"><span data-stu-id="fd09c-261">Switch back to the **Lines** view.</span></span> <span data-ttu-id="fd09c-262">Ef beðið er um að uppfæra afhendingarmáta fyrir sölulínurnar skal velja **Já**.</span><span class="sxs-lookup"><span data-stu-id="fd09c-262">If you're prompted to update the mode of delivery for the sales lines, select **Yes**.</span></span>
1. <span data-ttu-id="fd09c-263">Í hlutanum **Sölupöntunarlínur** skal velja pöntunarlínuna sem var sett upp hér á undan og síðan velja **Birgðir \> Frátekning**.</span><span class="sxs-lookup"><span data-stu-id="fd09c-263">In the **Sales order lines** section, select the order line that you set up earlier, and then select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="fd09c-264">Á síðunni **Frátekning** skal velja **Frátektarlota** til að taka frá heildarmagn valdrar línu í vöruhúsinu.</span><span class="sxs-lookup"><span data-stu-id="fd09c-264">On the **Reservation** page, select **Reserve lot** to reserve the selected line's full quantity in the warehouse.</span></span>
1. <span data-ttu-id="fd09c-265">Lokið síðunni **Frátekning** til að fara aftur í sölupöntunina.</span><span class="sxs-lookup"><span data-stu-id="fd09c-265">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="fd09c-266">Á aðgerðasvæðinu, í flipanum **Vöruhús**, skal velja **Losa í vöruhús**.</span><span class="sxs-lookup"><span data-stu-id="fd09c-266">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="fd09c-267">Vinna er stofnuð til að færa vörur úr tiltektarstaðsetningu og yfir á pökkunarstöð.</span><span class="sxs-lookup"><span data-stu-id="fd09c-267">Work is created to move items from the picking location to the packing station.</span></span>

1. <span data-ttu-id="fd09c-268">Í hlutanum **Sölupöntunarlínur** skal velja **Vöruhúsa \> Upplýsingar sendingar**.</span><span class="sxs-lookup"><span data-stu-id="fd09c-268">In the **Sales order lines** section, select **Warehouse \> Shipment details**.</span></span>
1. <span data-ttu-id="fd09c-269">Á síðunni **Upplýsingar sendingar** skal skrifa hjá sér sendingarkennið.</span><span class="sxs-lookup"><span data-stu-id="fd09c-269">On the **Shipment details** page, make a note of the shipment ID.</span></span> <span data-ttu-id="fd09c-270">Þörf er á því þegar sending er pökkuð á pökkunarstöðinni.</span><span class="sxs-lookup"><span data-stu-id="fd09c-270">You will need it when you pack the pack the shipment at the packing station.</span></span>
1. <span data-ttu-id="fd09c-271">Lokið síðunni **Upplýsingar sendingar** til að fara aftur í sölupöntunina.</span><span class="sxs-lookup"><span data-stu-id="fd09c-271">Close the **Shipment details** page to return to the sales order.</span></span>
1. <span data-ttu-id="fd09c-272">Skráið hjá ykkur sölupöntunarnúmerið og farið síðan í **Vöruhúsakerfi \> Vinna \> Öll vinna**.</span><span class="sxs-lookup"><span data-stu-id="fd09c-272">Make a note of the sales order number, and then go to **Warehouse management \> Work \> All work**.</span></span>
1. <span data-ttu-id="fd09c-273">Notið sölupöntunarnúmerið til að finna og velja vinnu sem var stofnuð fyrir pöntunina.</span><span class="sxs-lookup"><span data-stu-id="fd09c-273">Use the sales order number to find and select the work that was created for the order.</span></span>
1. <span data-ttu-id="fd09c-274">Á aðgerðasvæðinu, í flipanum **Vinna**, skal velja **Ljúka vinnu**.</span><span class="sxs-lookup"><span data-stu-id="fd09c-274">On the Action Pane, on the **Work** tab, select **Complete work**.</span></span>
1. <span data-ttu-id="fd09c-275">Á síðunni **Vinnulok**, í reitnum **Notandakenni**, skal velja notandakenni.</span><span class="sxs-lookup"><span data-stu-id="fd09c-275">On the **Work completion** page, in the **User ID** field, select a user ID.</span></span> <span data-ttu-id="fd09c-276">Veldu **Villuleita verk** á aðgerðasvæðinu.</span><span class="sxs-lookup"><span data-stu-id="fd09c-276">Then, on the Action Pane, select **Validate work**.</span></span>
1. <span data-ttu-id="fd09c-277">Ef verk stenst sannvottun skal velja **Ljúka vinnu** á aðgerðasvæðinu.</span><span class="sxs-lookup"><span data-stu-id="fd09c-277">If the work passes validation, select **Complete work** on the Action Pane.</span></span>

    <span data-ttu-id="fd09c-278">Vinnan er merkt sem lokið til að herma eftir flutningi varanna á pökkunarstöðina.</span><span class="sxs-lookup"><span data-stu-id="fd09c-278">The work is marked as completed to simulate the movement of items to the packing station.</span></span>

#### <a name="pack-the-shipment"></a><span data-ttu-id="fd09c-279">Sending pökkuð</span><span class="sxs-lookup"><span data-stu-id="fd09c-279">Pack the shipment</span></span>

<span data-ttu-id="fd09c-280">Fylgið þessum skrefum til að pakka sendingunni.</span><span class="sxs-lookup"><span data-stu-id="fd09c-280">Follow these steps to pack the shipment.</span></span>

1. <span data-ttu-id="fd09c-281">Farið í **Vöruhúsakerfi \> Uppsetning \> Starfsmaður** og gangið úr skugga um að notandareikningurinn sé tengdur reikningi starfsmanns fyrir vöruhúsakerfi.</span><span class="sxs-lookup"><span data-stu-id="fd09c-281">Go to **Warehouse management \> Setup \> Worker**, and make sure that your user account is associated with a worker account for warehouse management.</span></span>
1. <span data-ttu-id="fd09c-282">Farið í **Vöruhúsakerfi \> Tiltekt og gámun \> Pakka**.</span><span class="sxs-lookup"><span data-stu-id="fd09c-282">Go to **Warehouse management \> Picking and containerization \> Pack**.</span></span>
1. <span data-ttu-id="fd09c-283">Í svarglugganum **Velja pökkunarstöð** skal stilla eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="fd09c-283">In the **Select packing station** dialog box, set the following values:</span></span>

    - <span data-ttu-id="fd09c-284">**Svæði:** *6*</span><span class="sxs-lookup"><span data-stu-id="fd09c-284">**Site:** *6*</span></span>
    - <span data-ttu-id="fd09c-285">**Vöruhús:** *62*</span><span class="sxs-lookup"><span data-stu-id="fd09c-285">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="fd09c-286">**Staðsetning:** *Pakka*</span><span class="sxs-lookup"><span data-stu-id="fd09c-286">**Location:** *Pack*</span></span>
    - <span data-ttu-id="fd09c-287">**Forstillingarkenni umbúða:** *Sýnidæmi umbúðaforstillingar*</span><span class="sxs-lookup"><span data-stu-id="fd09c-287">**Packing profile ID:** *Demo packing profile*</span></span>

1. <span data-ttu-id="fd09c-288">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="fd09c-288">Select **OK**.</span></span>
1. <span data-ttu-id="fd09c-289">Síðan **Pakka** birtist.</span><span class="sxs-lookup"><span data-stu-id="fd09c-289">The **Pack** page appears.</span></span> <span data-ttu-id="fd09c-290">Í framleiðsluaðstæðum mun starfskraftur skanna númeraplötu eða sendingarauðkenni.</span><span class="sxs-lookup"><span data-stu-id="fd09c-290">In a production scenario, a worker will scan a license plate or shipment ID.</span></span> <span data-ttu-id="fd09c-291">Fyrir þessar aðstæður skal hins vegar opna síðuna **Allar sendingar** og leita að sendingarnúmerinu fyrir sendinguna sem var stofnuð rétt í þessu.</span><span class="sxs-lookup"><span data-stu-id="fd09c-291">However, for this scenario, open the **All shipments** page, and look up the shipment number for the shipment that you just created.</span></span> <span data-ttu-id="fd09c-292">Færið síðan þetta gildi inn í reitinn **Númeraplata eða sending** á síðunni **Pakka**.</span><span class="sxs-lookup"><span data-stu-id="fd09c-292">Then enter this value in the **License plate or shipment** field on the **Pack** page.</span></span> <span data-ttu-id="fd09c-293">Einnig er hægt að færa inn sendingarkennið sem var skrifað niður hér á undan.</span><span class="sxs-lookup"><span data-stu-id="fd09c-293">Alternatively, enter the shipment ID that you made a note of earlier.</span></span>
1. <span data-ttu-id="fd09c-294">Á aðgerðasvæðinu skal velja **Nýr gámur**.</span><span class="sxs-lookup"><span data-stu-id="fd09c-294">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="fd09c-295">Svarglugginn sem birtist sýnir upplýsingar um nýja gáminn.</span><span class="sxs-lookup"><span data-stu-id="fd09c-295">The dialog box that appears shows details about the new container.</span></span> <span data-ttu-id="fd09c-296">Haldið sjálfgefnu gildunum óbreyttum og veljið síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="fd09c-296">Leave the default values, and then select **OK**.</span></span>
1. <span data-ttu-id="fd09c-297">Á síðunni **Pakka**, í flýtiflipanum **Vörupökkun**, í reitnum **Auðkenni**, skal velja *A0002* til að pakka þeirri vöru.</span><span class="sxs-lookup"><span data-stu-id="fd09c-297">On the **Pack** page, on the **Item packing** FastTab, in the **Identifier** field, select *A0002* to pack that item.</span></span> <span data-ttu-id="fd09c-298">Vörunni er bætt við gáminn.</span><span class="sxs-lookup"><span data-stu-id="fd09c-298">The item is added to the container.</span></span>
1. <span data-ttu-id="fd09c-299">Á aðgerðasvæðinu skal velja **Gámar fyrir sendingu**.</span><span class="sxs-lookup"><span data-stu-id="fd09c-299">On the Action Pane, select **Containers for shipment**.</span></span>

    <span data-ttu-id="fd09c-300">Síðan **Gámar til sendingar** sem birtist er með línu fyrir gáminn sem var stofnuð hér á undan.</span><span class="sxs-lookup"><span data-stu-id="fd09c-300">The **Containers for shipment** page that appears has a row for the container that you just created.</span></span> <span data-ttu-id="fd09c-301">Hins vegar er reiturinn **Skráarkenni gáms** í þeirri línu auður eins og er vegna þess að ekki er búið að móttaka merkimiðann og rakningarnúmerið frá flutningsaðilanum.</span><span class="sxs-lookup"><span data-stu-id="fd09c-301">However, the **Container manifest ID** field in that row is currently blank, because you haven't yet received the shipping label and tracking number from the carrier.</span></span>

1. <span data-ttu-id="fd09c-302">Á aðgerðasvæðinu skal velja **Loka gámi**.</span><span class="sxs-lookup"><span data-stu-id="fd09c-302">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="fd09c-303">Í svarglugganum **Loka gámi** skal stilla reitinn **Brúttóþyngd** á *1 kg* og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="fd09c-303">In the **Close container** dialog box, set the **Gross weight** field to *1 kg*, and then select **OK**.</span></span>

    <span data-ttu-id="fd09c-304">Nú ætti að prenta merkimiðann á ZPL-prentaranum sem var valinn hér áður.</span><span class="sxs-lookup"><span data-stu-id="fd09c-304">The shipping label should now be printed on the ZPL printer that you selected earlier.</span></span> <span data-ttu-id="fd09c-305">Niðurstaðan ætti að líkjast eftirfarandi dæmi.</span><span class="sxs-lookup"><span data-stu-id="fd09c-305">It should resemble the following example.</span></span>

    <span data-ttu-id="fd09c-306">![Dæmi um merkimiða](media/sps-label-example.png "Dæmi um merkimiða")</span><span class="sxs-lookup"><span data-stu-id="fd09c-306">![Example shipping label](media/sps-label-example.png "Example shipping label")</span></span>

1. <span data-ttu-id="fd09c-307">Takið eftir að gildunum **Skráarkenni gáms** og **Heildarfarmur** hefur verið bætt við sem mótteknum frá flutningsaðila.</span><span class="sxs-lookup"><span data-stu-id="fd09c-307">Notice that the **Container manifest ID** and **Total freight** values have been added as received from the carrier.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]