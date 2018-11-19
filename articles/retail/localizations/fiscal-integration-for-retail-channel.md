---
title: "Samþætting fjárhags fyrir smásölurás"
description: "Þetta efnisatriði gefur yfirlit yfir fjárhagssamþættingu Retail POS."
author: josaw
manager: annbe
ms.date: 11/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailFunctionalityProfile, RetailFormLayout, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: v-kikozl
ms.search.validFrom: 2018-11-1
ms.dyn365.ops.version: 8.1.1
ms.translationtype: HT
ms.sourcegitcommit: 0450326dce0ba6be99aede4ebc871dc58c8039ab
ms.openlocfilehash: c852d095505abecbd44d29e9e7b53875e9069def
ms.contentlocale: is-is
ms.lasthandoff: 11/01/2018

---
# <a name="fiscal-integration-for-retail-channel"></a><span data-ttu-id="0d783-103">Samþætting fjárhags fyrir smásölurás</span><span class="sxs-lookup"><span data-stu-id="0d783-103">Fiscal integration for Retail channel</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0d783-104">Þetta efnisatriði er yfirlit fjárhagssamþættingarvirkni sem er að finna í Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="0d783-104">This topic is an overview of the fiscal integration functionality that is available in Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="0d783-105">Fjárhagssamþættingarvirkni eru rammar sem ætlað er að styðja við staðbundin lög um fjárhag sem miða að því að koma í veg fyrir svik í smásöluiðnaði.</span><span class="sxs-lookup"><span data-stu-id="0d783-105">The fiscal integration functionality is a framework designed to support local fiscal laws that are aimed to prevent fraud in the Retail industry.</span></span> <span data-ttu-id="0d783-106">Dæmigerðar aðstæður sem fjárhagssamþætting getur náð til eru:</span><span class="sxs-lookup"><span data-stu-id="0d783-106">Typical scenarios that could be covered by using fiscal integration include:</span></span>

- <span data-ttu-id="0d783-107">Prentun fjárhagskvittunar og afhending hennar til viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="0d783-107">Printing a fiscal receipt and giving it to the customer.</span></span>
- <span data-ttu-id="0d783-108">Tryggja skil á upplýsingum sem tengjast sölu og skilum sem fram fer á POS til ytri þjónustu sem stjórnvaldið veitir.</span><span class="sxs-lookup"><span data-stu-id="0d783-108">Securing the submission of the information related to sales and returns performed on POS to an external service provided by the authority.</span></span>
- <span data-ttu-id="0d783-109">Notkun gagnaverndar með stafrænu undirskrifti sem stjórnvald heimilar.</span><span class="sxs-lookup"><span data-stu-id="0d783-109">Using data protection with a digital signature authorized by the authority.</span></span>

<span data-ttu-id="0d783-110">Þetta efnisatriði veitir leiðbeiningar um uppbyggingu fjárhagssamþættingar þannig að notendur geti sinnt eftirfarandi verkefnum.</span><span class="sxs-lookup"><span data-stu-id="0d783-110">This topic provides guidelines for setting up fiscal integration so users can perform the following tasks.</span></span> 

- <span data-ttu-id="0d783-111">Grunnstilla fjárhagstengla, sem eru fjárhagstæki eða þjónusta notuð til fjárhagsskráningar svo sem vistun, stafrænar undirskriftir og örugg skil á fjárhagsgögnum.</span><span class="sxs-lookup"><span data-stu-id="0d783-111">Configure fiscal connectors, which are fiscal devices or services used for fiscal registration purposes like saving, digital signatures, and secured submission of fiscal data.</span></span>
- <span data-ttu-id="0d783-112">Grunnstilla skjalsveitu, sem skilgreinir úttaksaðgerð og reiknirit til myndunar á fjárhagsskjali.</span><span class="sxs-lookup"><span data-stu-id="0d783-112">Configure the document provider, which defines an output method and an algorithm of fiscal document generation.</span></span>
- <span data-ttu-id="0d783-113">Grunnstilla skráningarferli fjárhagsins, sem er skilgreint af röð skrefa og hópi tengla sem notaðar eru í hverju skrefi.</span><span class="sxs-lookup"><span data-stu-id="0d783-113">Configure the fiscal registration process, which is defines a sequence of steps and a group of connectors used on each step.</span></span>
- <span data-ttu-id="0d783-114">Úthluta skráningarferlum fjárhags til POS-virknireglna.</span><span class="sxs-lookup"><span data-stu-id="0d783-114">Assign fiscal registration processes to POS functionality profiles.</span></span>
- <span data-ttu-id="0d783-115">Úthluta tengli virknireglu, annaðhvort til vélbúnaðarsniðs (fyrir staðbundna fjárhagstengla) eða til POS-virknireglna (fyrir aðrar gerðir fjárhagstengla).</span><span class="sxs-lookup"><span data-stu-id="0d783-115">Assign connector technical profiles, either to hardware profiles (for the local fiscal connectors) or to POS functionality profiles (for other fiscal connector types).</span></span>

## <a name="fiscal-integration-execution-flow"></a><span data-ttu-id="0d783-116">Framkvæmdarflæði fjárhagssamþættingar</span><span class="sxs-lookup"><span data-stu-id="0d783-116">Fiscal integration execution flow</span></span>
<span data-ttu-id="0d783-117">Eftirfarandi atburðarás sýnir sameiginlegt framkvæmdarflæði fjárhagssamþættingar.</span><span class="sxs-lookup"><span data-stu-id="0d783-117">The following scenario shows the common fiscal integration execution flow.</span></span>

1. <span data-ttu-id="0d783-118">Frumstilling á skráningarferli fjárhagsins.</span><span class="sxs-lookup"><span data-stu-id="0d783-118">Initialization of the fiscal registration process.</span></span>
  
   <span data-ttu-id="0d783-119">Eftir að hafa gert aðgerðir þar sem fjárhagsskráningar er krafist, eins og eftir að smásöluverslun hefur verið gerður, er skráningarferli fjárhagnsins tengt núverandi POS-virknireglu.</span><span class="sxs-lookup"><span data-stu-id="0d783-119">After performing some actions where fiscal registration is required, such as after a retail transaction has been concluded, the fiscal registration process is associated with the current POS functionality profile.</span></span>

1. <span data-ttu-id="0d783-120">Leitaðu að fjárhagstengli.</span><span class="sxs-lookup"><span data-stu-id="0d783-120">Search for a fiscal connector.</span></span>
   
   <span data-ttu-id="0d783-121">Fyrir hvert þrep fjárhagsskráningar í skráningarferli fjárhagsins, stemmir kerfið saman við lista yfir fjárhagstengla.</span><span class="sxs-lookup"><span data-stu-id="0d783-121">For each fiscal registration step included in the fiscal registration process, the system matches the list of fiscal connectors.</span></span> <span data-ttu-id="0d783-122">Þessir tenglar hafa virknireglu sem er innifalin í tilgreindum tenglahópi, með lista yfir tengla sem innihalda tæknilegar upplýsingar í tengslum við núverandi vélbúnaðarsnið (aðeins fyrir gerð tengils sem jafngildir **Staðbundinn**) eða með núverandi POS-virknireglu (fyrir aðrar gerðir af tenglum).</span><span class="sxs-lookup"><span data-stu-id="0d783-122">These connectors have a functional profile included in the specified connector group, with a list of connectors that have a technical profile associated with the current hardware profile (for a connector type that equals **Local** only) or with the current POS functionality profile (for other connector types).</span></span>
   
1. <span data-ttu-id="0d783-123">Framkvæma fjárhagssamþættingu.</span><span class="sxs-lookup"><span data-stu-id="0d783-123">Perform the fiscal integration.</span></span>

   <span data-ttu-id="0d783-124">Kerfið framkvæmir allar nauðsynlegar aðgerðir sem eru skilgreindar af samsetningu sem er tengd við tengilinn sem fannst.</span><span class="sxs-lookup"><span data-stu-id="0d783-124">The system executes all necessary actions defined by an assembly linked with the found connector.</span></span> <span data-ttu-id="0d783-125">Þetta er gert í samræmi við stillingar virknireglunnar og tæknisniðsins sem fundust í fyrra skrefi fyrir þennan tengil.</span><span class="sxs-lookup"><span data-stu-id="0d783-125">This is done in accordance with the settings of the functional profile and technical profile that were found on the previous step for this connector.</span></span>

## <a name="setup-needed-before-using-fiscal-integration"></a><span data-ttu-id="0d783-126">Uppsetning þarf áður en fjárhagssamþætting er notuð</span><span class="sxs-lookup"><span data-stu-id="0d783-126">Setup needed before using fiscal integration</span></span>
<span data-ttu-id="0d783-127">Áður en þú notar fjárhagnssamþættingarvirknina ættirðu að skilgreina eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="0d783-127">Before using the fiscal integration functionality, you should define the following settings:</span></span>

- <span data-ttu-id="0d783-128">Skilgreindu númeraröðina á **Smásölufæribreytur** síðu fyrir númer tækniforstillingar fjárhags.</span><span class="sxs-lookup"><span data-stu-id="0d783-128">Define the number sequence on the **Retail parameters** page for the fiscal functional profile number.</span></span>
  
- <span data-ttu-id="0d783-129">Skilgreindu númeraröðin á **Smásölufæribreytur** síðu fyrir eftirfarandi tilvísanir:</span><span class="sxs-lookup"><span data-stu-id="0d783-129">Define the number sequences on the **Retail shared parameters** page for the following references:</span></span>
  
  - <span data-ttu-id="0d783-130">Númer tækniforstillingar fjárhags</span><span class="sxs-lookup"><span data-stu-id="0d783-130">Fiscal technical profile number</span></span>
  - <span data-ttu-id="0d783-131">Flokksnúmer fjárhagstengils</span><span class="sxs-lookup"><span data-stu-id="0d783-131">Fiscal connector group number</span></span>
  - <span data-ttu-id="0d783-132">Númer skráningarferlis</span><span class="sxs-lookup"><span data-stu-id="0d783-132">Registration process number</span></span>

- <span data-ttu-id="0d783-133">Búðu til **Fjárhagstengil** í **Smásala> Rásaruppsetning > Fjárhagssamþætting > Fjárhagstenglar** fyrir hvert tæki eða þjónustu sem þú ætlar að nota til fjárhagssamþættingar.</span><span class="sxs-lookup"><span data-stu-id="0d783-133">Create a **Fiscal connector** in **Retail > Channel setup > Fiscal integration > Fiscal connectors** for each device or service that you plan to use for fiscal integration purposes.</span></span>

-  <span data-ttu-id="0d783-134">Búa til **Fjárhagsskjalsveitu** í **Smásala> Rásaruppsetning > Fjárhagssamþætting > Fjárhagsskjalsveitur** fyrir alla fjárhagstengla.</span><span class="sxs-lookup"><span data-stu-id="0d783-134">Create a **Fiscal document provider** in **Retail > Channel setup > Fiscal integration > Fiscal document providers** for all fiscal connectors.</span></span> <span data-ttu-id="0d783-135">Gagnakortalagning er talin hluti af fjárhagsskjalsveitu.</span><span class="sxs-lookup"><span data-stu-id="0d783-135">Data mapping is considered a part of the fiscal document provider.</span></span> <span data-ttu-id="0d783-136">Til að setja upp mismunandi gagnakortalagningu fyrir sama tengilinn (eins og samkvæmt staðbundnum reglugerðum), ættir þú að búa til mismunandi fjárhagsskjalsveitur.</span><span class="sxs-lookup"><span data-stu-id="0d783-136">To set up different data mappings for the same connector (like state-specific regulations), you should create different fiscal document providers.</span></span>

- <span data-ttu-id="0d783-137">Búa til **Virkniforstillingu tengils** í **Smásala> Rásaruppsetning> Fjárhagssamþætting> Virkniforstillingar tengils** fyrir hverja fjárhagsskjalsveitu.</span><span class="sxs-lookup"><span data-stu-id="0d783-137">Create a **Connector functional profile** in **Retail > Channel setup > Fiscal integration > Connector functional profiles** for each fiscal document provider.</span></span>
  - <span data-ttu-id="0d783-138">Veldu heiti tengils.</span><span class="sxs-lookup"><span data-stu-id="0d783-138">Select a connector name.</span></span>
  - <span data-ttu-id="0d783-139">Veldu skjalsveitu.</span><span class="sxs-lookup"><span data-stu-id="0d783-139">Select a document provider.</span></span>
  - <span data-ttu-id="0d783-140">Tilgreina stillingar VSK-hlutfalls á **Uppsetningar** flipanum.</span><span class="sxs-lookup"><span data-stu-id="0d783-140">Specify VAT rates settings on the **Service setup** tab.</span></span>
  - <span data-ttu-id="0d783-141">Tilgreina vörpun VSK-kóða og greiðslumátta á flipanum **Gagnakortalagning**.</span><span class="sxs-lookup"><span data-stu-id="0d783-141">Specify VAT codes mapping and tender type mapping on the **Data mapping** tab.</span></span>

  #### <a name="examples"></a><span data-ttu-id="0d783-142">Dæmi</span><span class="sxs-lookup"><span data-stu-id="0d783-142">Examples</span></span> 

  |  | <span data-ttu-id="0d783-143">Snið</span><span class="sxs-lookup"><span data-stu-id="0d783-143">Format</span></span> | <span data-ttu-id="0d783-144">Dæmi</span><span class="sxs-lookup"><span data-stu-id="0d783-144">Example</span></span> | 
  |--------|--------|--------|
  | <span data-ttu-id="0d783-145">Stillingar VSK-hlutfalls</span><span class="sxs-lookup"><span data-stu-id="0d783-145">VAT rates settings</span></span> | <span data-ttu-id="0d783-146">gildi : VAThlutfall</span><span class="sxs-lookup"><span data-stu-id="0d783-146">value : VATrate</span></span> | <span data-ttu-id="0d783-147">1 : 2000, 2 : 1800</span><span class="sxs-lookup"><span data-stu-id="0d783-147">1 : 2000, 2 : 1800</span></span> |
  | <span data-ttu-id="0d783-148">Vörpun VSK-kóða</span><span class="sxs-lookup"><span data-stu-id="0d783-148">VAT codes mapping</span></span> | <span data-ttu-id="0d783-149">VSKkóði : gildi</span><span class="sxs-lookup"><span data-stu-id="0d783-149">VATcode : value</span></span> | <span data-ttu-id="0d783-150">vsk20: 1, vsk18: 2</span><span class="sxs-lookup"><span data-stu-id="0d783-150">vat20 : 1, vat18 : 2</span></span> |
  | <span data-ttu-id="0d783-151">Setja upp greiðslumáta</span><span class="sxs-lookup"><span data-stu-id="0d783-151">Tender types mapping</span></span> | <span data-ttu-id="0d783-152">TenderTyp: gildi</span><span class="sxs-lookup"><span data-stu-id="0d783-152">TenderTyp : value</span></span> | <span data-ttu-id="0d783-153">Reiðufé: 1, kort: 2</span><span class="sxs-lookup"><span data-stu-id="0d783-153">Cash : 1, Card : 2</span></span> |

- <span data-ttu-id="0d783-154">Búa til **Fjárhagstenglahópa** í **Smásala> Rásaruppsetning> Fjárhagssamþætting> Fjárhagstenglahópur**.</span><span class="sxs-lookup"><span data-stu-id="0d783-154">Create **Fiscal connector groups** in **Retail > Channel setup > Fiscal integration > Fiscal connector group**.</span></span> <span data-ttu-id="0d783-155">Tenglahópur er hluti af virkniforstillingum sem tengjast fjárhagstenglum sem framkvæma sömu aðgerðir og eru notaðar á sama stigi innan skráningarferlis fjárhagsins.</span><span class="sxs-lookup"><span data-stu-id="0d783-155">A connector group is a subset of functional profiles linked with fiscal connectors that perform identical functions and are used at the same stage within a fiscal registration process.</span></span>

   - <span data-ttu-id="0d783-156">Bæta virkniforstillingum við tenglahópinn.</span><span class="sxs-lookup"><span data-stu-id="0d783-156">Add functional profiles to the connector group.</span></span> <span data-ttu-id="0d783-157">Smelltu á **Bæta við** á síðunni **Virkniforstillingar** og veldu forstillingarnúmer.</span><span class="sxs-lookup"><span data-stu-id="0d783-157">Click **Add** on the **Functional profiles** page and select a profile number.</span></span>
   - <span data-ttu-id="0d783-158">Ef þú vilt hætta að nota virkniforstillinguna skaltu stilla **Slökkva** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="0d783-158">If you want to suspend usage of the functional profile, set **Disable** to **Yes**.</span></span> 
   
     <span data-ttu-id="0d783-159">Þessi breyting hefur aðeins áhrif á núverandi tenglahóp.</span><span class="sxs-lookup"><span data-stu-id="0d783-159">This change affects the current connector group only.</span></span> <span data-ttu-id="0d783-160">Þú getur haldið áfram að nota sömu virkniforstillingu fyrir aðra tenglahópa.</span><span class="sxs-lookup"><span data-stu-id="0d783-160">You can continue using the same functional profile in other connector groups.</span></span>

     >[!NOTE]
     > <span data-ttu-id="0d783-161">Innan tenglahópsins getur hver fjárhagstengill aðeins haft eina virkniforstillingu.</span><span class="sxs-lookup"><span data-stu-id="0d783-161">Within a connector group, each fiscal connector can only have one functional profile.</span></span>

- <span data-ttu-id="0d783-162">Búa til **Tækniforstillingu tengils** í **Smásala> Rásarppsetning> Fjárhagssamþætting> Tækniforstilling tengils** fyrir hvern fjárhagstengil.</span><span class="sxs-lookup"><span data-stu-id="0d783-162">Create a **Connector technical profile** in **Retail > Channel setup > Fiscal integration > Connector technical profiles** for each fiscal connector.</span></span>
  - <span data-ttu-id="0d783-163">Veldu heiti tengils.</span><span class="sxs-lookup"><span data-stu-id="0d783-163">Select a connector name.</span></span>
  - <span data-ttu-id="0d783-164">Veldu gerð tengils:</span><span class="sxs-lookup"><span data-stu-id="0d783-164">Select a connector type:</span></span> 
      - <span data-ttu-id="0d783-165">**Staðbundinn** - Veldu þessa gerð fyrir tæki eða forrit sem eru settar upp á staðbundinni tölvu.</span><span class="sxs-lookup"><span data-stu-id="0d783-165">**Local** - Set this type for physical devices or applications installed on a local machine.</span></span>
      - <span data-ttu-id="0d783-166">**Innri** - Veldu þessa gerðfyrir fjármálatæki og þjónustu sem tengist smásöluþjóni.</span><span class="sxs-lookup"><span data-stu-id="0d783-166">**Internal** - Set this type for fiscal devices and services connected to Retail Server.</span></span>
      - <span data-ttu-id="0d783-167">**Ytri** - Fyrir ytri fjárhagsþjónustu eins og vefgátt sem skattyfirvöld veita.</span><span class="sxs-lookup"><span data-stu-id="0d783-167">**External** - For external fiscal services like a web-portal provided by a tax authority.</span></span>
    
  - <span data-ttu-id="0d783-168">Tilgreina stillingar á **Tenging** flipanum.</span><span class="sxs-lookup"><span data-stu-id="0d783-168">Specify settings on the **Connection** tab.</span></span>

      
 >[!NOTE]
 > <span data-ttu-id="0d783-169">Uppfært útgáfa af grunnstillingum sem var hlaðið áður verður hlaðinn fyrir bæði hagnýtur og tæknileg snið.</span><span class="sxs-lookup"><span data-stu-id="0d783-169">An updated version of a configuration that was loaded earlier will be loaded for both functional and technical profiles.</span></span> <span data-ttu-id="0d783-170">Ef viðeigandi tengill eða skjalveita er þegar í notkun verður þú tilkynnt.</span><span class="sxs-lookup"><span data-stu-id="0d783-170">If an appropriate connector or document provider is already in use, you will be notified.</span></span> <span data-ttu-id="0d783-171">Sjálfgefið er að allar breytingar sem hafa verið gerðar handvirkt í hagnýtum og tæknilegum sniðum verða geymdar.</span><span class="sxs-lookup"><span data-stu-id="0d783-171">By default, all changes that have been made manually in functional and technical profiles will be stored.</span></span> <span data-ttu-id="0d783-172">Til þess að hunsa þessi snið með sjálfgefnum færibreytum úr grunnstillingunni skaltu smella á **Uppfæra** á **Virkniforstillingar tengils** síðu og **Tækniforstillingar tengils** síðu.</span><span class="sxs-lookup"><span data-stu-id="0d783-172">In order to override these profiles with the default set of parameters from a configuration, click **Update** on the **Connector functional profiles** page and **Connector technical profiles** page.</span></span>
 
- <span data-ttu-id="0d783-173">Búa til **Skráningarferli fjárhags** í **Smásala> Rásaruppsetning> Fjármálasamþætting> Skráningarferli fjárhagsins** fyrir hvert einkvæmt ferli í fjárhagssamþættingunni.</span><span class="sxs-lookup"><span data-stu-id="0d783-173">Create a **Fiscal registration process** in **Retail > Channel setup > Fiscal integration > Fiscal registration processes** for each unique process of the fiscal integration.</span></span> <span data-ttu-id="0d783-174">Skráningarferli er skilgreint með röð skráningarskrefanna og tenglahópnum sem notaður er í hverju skrefi.</span><span class="sxs-lookup"><span data-stu-id="0d783-174">A registration process is defined by the sequence of the registration steps and the connector group used on each step.</span></span> 
  
  - <span data-ttu-id="0d783-175">Bæta við skráningarskrefum við ferlið:</span><span class="sxs-lookup"><span data-stu-id="0d783-175">Add registration steps to the process:</span></span>
      - <span data-ttu-id="0d783-176">Smellið á **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="0d783-176">Click **Add**.</span></span>
      - <span data-ttu-id="0d783-177">Veldu gerð tengils.</span><span class="sxs-lookup"><span data-stu-id="0d783-177">Select a connector type.</span></span>
      
      >[!NOTE]
      > <span data-ttu-id="0d783-178">Þetta reitur skilgreinir hvar kerfið leitar í tæknforstillingunni að tenglinum, annaðhvort í vélbúnaðarsniðum fyrir tenglategundina **Staðbundinn**, eða í POS-virknireglum fyrir aðra gerðir fjárhagstengla.</span><span class="sxs-lookup"><span data-stu-id="0d783-178">This field defines where the system will search in a technical profile for the connector, either in hardware profiles for connector type **Local**, or in POS functionality profiles for other fiscal connector types.</span></span>
      
   - <span data-ttu-id="0d783-179">Veldu tenglahóp.</span><span class="sxs-lookup"><span data-stu-id="0d783-179">Select a connector group.</span></span>
   
     >[!NOTE]
     > <span data-ttu-id="0d783-180">Smelltu á **Villuleita** til að athuga heilleika skráningarferlis uppbyggingarinnar.</span><span class="sxs-lookup"><span data-stu-id="0d783-180">Click **Validate** to check the integrity of the registration process structure.</span></span> <span data-ttu-id="0d783-181">Mælt er með því að villuleitir séu gerðar í eftirfarandi tilvikum:</span><span class="sxs-lookup"><span data-stu-id="0d783-181">It’s recommended that validations be made in the following cases:</span></span>
       >- <span data-ttu-id="0d783-182">Fyrir nýtt skráningarferli eftir að allar stillingar hafa verið gerðar, þ.m.t. binding við POS-virknireglur og vélbúnaðarsnið.</span><span class="sxs-lookup"><span data-stu-id="0d783-182">For a new registration process after all the settings are completed, including binding to POS functionality profiles and hardware profiles.</span></span>
       >- <span data-ttu-id="0d783-183">Eftir að uppfærslur hafa verið gerðar á skráningarferli sem fyrir er.</span><span class="sxs-lookup"><span data-stu-id="0d783-183">After making updates to an existing registration process.</span></span>

-  <span data-ttu-id="0d783-184">Bindið skráningarferli fjárhagsins við POS-virknireglur í **Smásala> Rásaruppsetning> POS-uppsetning> POS-reglur> Virknireglur**.</span><span class="sxs-lookup"><span data-stu-id="0d783-184">Bind fiscal registration processes to POS functionality profiles in **Retail > Channel setup > POS setup > POS profiles > Functionality profiles**.</span></span>
   - <span data-ttu-id="0d783-185">Smelltu á **Breyta** og veldu **Númer ferlis** á **Skráningarferli fjárhagsins** flipanum.</span><span class="sxs-lookup"><span data-stu-id="0d783-185">Click **Edit** and select a **Process number** on the **Fiscal registration process** tab.</span></span>
- <span data-ttu-id="0d783-186">Tengd tækniforstillingar tengilsins við vélbúnaðarsniðin í **Smásala> Rásarstillingar > POS-uppsetning> POS-reglur> Vélbúnaðarsnið**.</span><span class="sxs-lookup"><span data-stu-id="0d783-186">Bind the connector technical profiles to the hardware profiles in **Retail > Channel setup > POS setup > POS profiles > Hardware profiles**.</span></span>
   - <span data-ttu-id="0d783-187">Smelltu á **Breyta**, smelltu svo á **Nýtt** á flipanum **Tækniforstilling fjárhags**.</span><span class="sxs-lookup"><span data-stu-id="0d783-187">Click **Edit**, then click **New** on the **Fiscal technical profile** tab.</span></span>
   - <span data-ttu-id="0d783-188">Veldu tækniforstillingu tengilsins í reitnum **Forstillingarnúmer**.</span><span class="sxs-lookup"><span data-stu-id="0d783-188">Select a connector technical profile in the **Profile number** field.</span></span>
   
     >[!NOTE]
     > <span data-ttu-id="0d783-189">Þú getur bætt nokkrum tækniforstillingum við vélbúnaðarsnið.</span><span class="sxs-lookup"><span data-stu-id="0d783-189">You can add several technical profiles to a hardware profile.</span></span> <span data-ttu-id="0d783-190">Hins vegar er þetta ekki studd ef vélbúnaðarsniðið hefur fleiri en eina skörun við hvaða tenglahóp sem er.</span><span class="sxs-lookup"><span data-stu-id="0d783-190">However, this is not supported if a hardware profile has more than one intersection with any connector group.</span></span> <span data-ttu-id="0d783-191">Til að koma í veg fyrir rangar stillingar er mælt með því að þú villuleitir skráningarferlið eftir að uppfæra öll vélbúnaðarsniðin.</span><span class="sxs-lookup"><span data-stu-id="0d783-191">To avoid incorrect settings, it’s recommended that you validate the registration process after updating all the hardware profiles.</span></span>

