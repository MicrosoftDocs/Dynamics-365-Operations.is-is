---
title: Virkja innskráningartilkynningar viðskiptavinar á sölustað (POS)
description: Í þessu efnisatriði er lýst hvernig á að virkja tilkynningar um innskráningu viðskiptavina á Microsoft Dynamics 365 Commerce sölustað.
author: bicyclingfool
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: e4defc15d9ef198a361934d51e31016747dbb5ab
ms.sourcegitcommit: 593438a145672c55ff6a910eabce2939300b40ad
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/23/2021
ms.locfileid: "5937591"
---
# <a name="enable-customer-check-in-notifications-in-point-of-sale-pos"></a><span data-ttu-id="2def5-103">Virkja innskráningartilkynningar viðskiptavinar á sölustað (POS)</span><span class="sxs-lookup"><span data-stu-id="2def5-103">Enable customer check-in notifications in point of sale (POS)</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="2def5-104">Í þessu efnisatriði er lýst hvernig á að virkja tilkynningar um innskráningu viðskiptavina á Microsoft Dynamics 365 Commerce sölustað.</span><span class="sxs-lookup"><span data-stu-id="2def5-104">This topic describes how to enable customer check-in notifications in Microsoft Dynamics 365 Commerce point of sale (POS).</span></span>

<span data-ttu-id="2def5-105">Í tölvupóstunum „sækja má pöntun“ geta fyrirtæki gefið upp tengil eða hnapp sem gerir viðskiptavinum kleift að tilkynna versluninni að þeir séu í nágrenninu og eru að bíða eftir pakkinn verður færður þeim fyrir utan.</span><span class="sxs-lookup"><span data-stu-id="2def5-105">In their "order ready for pickup" emails, organizations can provide a link or button that lets customers notify the store that they are on the premises and waiting for their package to be brought out to them.</span></span> <span data-ttu-id="2def5-106">Viðskiptavinir fá síðan staðfestingu á innskráningu og verslunin fær tilkynningu í formi verks í forriti sölustaðar.</span><span class="sxs-lookup"><span data-stu-id="2def5-106">Customers then receive a check-in confirmation, and the store receives a notification as a task in its POS application.</span></span> <span data-ttu-id="2def5-107">Þetta verk virkar sem kvaðning fyrir sölustarfsfólk um að fara með pöntunina að bifreið viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="2def5-107">This task serves as a prompt for a sales associate to deliver the order to the customer's vehicle.</span></span> <span data-ttu-id="2def5-108">Því þarf viðskiptavinurinn ekki að fara inn í búðina.</span><span class="sxs-lookup"><span data-stu-id="2def5-108">Therefore, the customer doesn't have to enter the store.</span></span>

<span data-ttu-id="2def5-109">Verkflæði innskráningar viðskiptavinar getur einnig verið skilgreint til að safna viðbótarupplýsingum frá viðskiptavinum á borð við bílastæðanúmer, gerð bifreiðar og litur hennar og leiðbeiningar um afhendingu.</span><span class="sxs-lookup"><span data-stu-id="2def5-109">The customer check-in workflow can also be configured to collect additional information from customers, such as their parking spot number, the make, model, and color of their vehicle, and delivery instructions.</span></span> <span data-ttu-id="2def5-110">Starfsmaður smásöluverslunar getur notað þessar upplýsingar til að auðvelda uppfyllingu pöntunar.</span><span class="sxs-lookup"><span data-stu-id="2def5-110">The retail store attendant can use this information to facilitate order fulfillment.</span></span>

## <a name="enable-customer-check-in"></a><span data-ttu-id="2def5-111">Virkja innskráningu viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="2def5-111">Enable customer check-in</span></span>

<span data-ttu-id="2def5-112">Þegar kveikt er á innskráningareiginleika viðskiptavinar býr Commerce til kenni pöntunarstaðfestingar (einnig þekkt sem tilvísunarkenni rásarinnar).</span><span class="sxs-lookup"><span data-stu-id="2def5-112">When the customer check-in feature is turned on, Commerce generates an order confirmation ID (also known as the channel reference ID).</span></span> <span data-ttu-id="2def5-113">Það býr einnig til kenni pöntunarstaðfestingar fyrir pantanir sem eru stofnaðar í gegnum rás sölustaðar eða símavers.</span><span class="sxs-lookup"><span data-stu-id="2def5-113">It also generates order confirmation IDs for orders that are created through point of sale (POS) or call center channels.</span></span> 

<span data-ttu-id="2def5-114">Til að kveikja á innskráningareiginleika viðskiptavinar í Commerce Headquarters skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="2def5-114">To turn on the customer check-in feature in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="2def5-115">Opna skal **Vinnusvæði \> Eiginleikastjórnun**.</span><span class="sxs-lookup"><span data-stu-id="2def5-115">Go to **Workspaces \> Feature management**.</span></span>
2. <span data-ttu-id="2def5-116">Leitið að eiginleikanum **Búa til samræmt snið tilvísunarkennis rásar milli rása**.</span><span class="sxs-lookup"><span data-stu-id="2def5-116">Search for the **Generate a consistent channel reference ID format across channels** feature.</span></span> 
3. <span data-ttu-id="2def5-117">Veljið eiginleikann og veljið svo **Virkja núna** á eiginleikasvæðinu.</span><span class="sxs-lookup"><span data-stu-id="2def5-117">Select the feature, and then select **Enable now** in the properties pane.</span></span> 

## <a name="create-a-check-in-confirmation-page"></a><span data-ttu-id="2def5-118">Búa til staðfestingarsíðu innskráningar</span><span class="sxs-lookup"><span data-stu-id="2def5-118">Create a check-in confirmation page</span></span>

<span data-ttu-id="2def5-119">Á svæði rafrænna viðskipta þarf að búa til nýja síðu sem þjónar hlutverki staðfestingar á innskráningu.</span><span class="sxs-lookup"><span data-stu-id="2def5-119">On your e-commerce site, you must create a new page that will serve as the check-in confirmation experience.</span></span> <span data-ttu-id="2def5-120">Með viðbótarstillingum getur síðan einnig innihaldið eyðublað sem safnar viðbótarupplýsingum frá viðskiptavinum til að auðvelda uppfyllingu pöntunar.</span><span class="sxs-lookup"><span data-stu-id="2def5-120">Through additional configuration, the page can also include a form that collects additional information from customers to facilitate order fulfillment.</span></span> <span data-ttu-id="2def5-121">Upplýsingar um hvernig á að setja upp síðuna og eininguna er að finna í [Innritunareiningin viðskiptavinar](check-in-pickup-module.md).</span><span class="sxs-lookup"><span data-stu-id="2def5-121">For information about how to set up the page and module, see [Customer check-in module](check-in-pickup-module.md).</span></span>

## <a name="configure-the-transactional-email-template"></a><span data-ttu-id="2def5-122">Skilgreina sniðmát færslutölvupósta</span><span class="sxs-lookup"><span data-stu-id="2def5-122">Configure the transactional email template</span></span>

<span data-ttu-id="2def5-123">Bæta þarf **Ég er mætt(ur)** tengli eða hnapp við sniðmátið fyrir færslutölvupósta sem viðskiptavinir fá þegar þeir mega sækja pantanirnar sínar.</span><span class="sxs-lookup"><span data-stu-id="2def5-123">You must add an **I am here** link or button to the template for the transactional email that customers receive when their order is ready for pickup.</span></span> <span data-ttu-id="2def5-124">Viðskiptavinir munu nota þennan tengil eða hnapp til að tilkynna versluninni að þeir séu mættir til að sækja pöntunina.</span><span class="sxs-lookup"><span data-stu-id="2def5-124">Customers will use this link or button to notify the store that they have arrived to pick up their order.</span></span> 

<span data-ttu-id="2def5-125">Bætið tenglinum eða hnappnum við sniðmátið sem er varpað í tilkynningargerðina **Pökkun lokið** og flutningsmátann sem er notaður fyrir uppfyllingu pöntunar fyrir utan verslun.</span><span class="sxs-lookup"><span data-stu-id="2def5-125">Add the link or button to the template that is mapped to the **Packing completed** notification type and the mode of delivery that you're using for curbside order fulfillment.</span></span> <span data-ttu-id="2def5-126">Í sniðmátinu er búinn til HTML-tengill eða hnappur sem bendir á vefslóð staðfestingarsíðu innritunar sem var stofnuð.</span><span class="sxs-lookup"><span data-stu-id="2def5-126">In the template, create an HTML link or button that points to the URL of the check-in confirmation page that you created.</span></span> <span data-ttu-id="2def5-127">Eftirfarandi er dæmi.</span><span class="sxs-lookup"><span data-stu-id="2def5-127">Here is an example.</span></span>

```
<a href="https://[YOUR_SITE_DOMAIN]/[CHECK-IN_CONFIRMATION_PAGE]?channelReferenceId=%channelreferenceid%&channelId=%channelid%&packingSlipId=%packingslipid%" target="_blank">I am here!</a>
```
<span data-ttu-id="2def5-128">Nánari upplýsingar um hvernig á að stilla sniðmát fyrir tölvupósta eru í [Sérstilla tölvupósta vegna færslna eftir afhendingarmáta](customize-email-delivery-mode.md).</span><span class="sxs-lookup"><span data-stu-id="2def5-128">For more information about how to configure email templates, see [Customize transactional emails by mode of delivery](customize-email-delivery-mode.md).</span></span> 

## <a name="a-check-in-confirmation-task-is-created-in-pos"></a><span data-ttu-id="2def5-129">Staðfestingarverkefni fyrir innritun er stofnað í sölustað</span><span class="sxs-lookup"><span data-stu-id="2def5-129">A check-in confirmation task is created in POS</span></span>

<span data-ttu-id="2def5-130">Þegar viðskiptavinur hefur tilkynnt versluninni að hann sé kominn til að sækja pöntun fær hann tilkynningu um staðfestingu innskráningar og verk er búið til í verklistanum á sölustað fyrir verslunina þar sem viðskiptavinurinn sækir pöntunina.</span><span class="sxs-lookup"><span data-stu-id="2def5-130">After a customer notifies the store that they are present for pickup, they receive a check-in confirmation notification, and a task is created in the tasks list in POS for the store where the customer is picking up the order.</span></span> <span data-ttu-id="2def5-131">Verkið inniheldur allar upplýsingar um viðskiptavin og pöntun sem þarf til að uppfylla pöntunina.</span><span class="sxs-lookup"><span data-stu-id="2def5-131">The task contains all the customer and order information that is required to fulfill the order.</span></span> <span data-ttu-id="2def5-132">Í verkinu sýnir leiðbeiningarreiturinn allar upplýsingar sem safnað var saman frá viðskiptavini í gegnum skjámynd viðbótarupplýsinga.</span><span class="sxs-lookup"><span data-stu-id="2def5-132">In the task, the instructions field shows any information that was collected from the customer through the additional information form.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="2def5-133">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="2def5-133">Additional resources</span></span>

[<span data-ttu-id="2def5-134">Innskráning í afhendingareiningu</span><span class="sxs-lookup"><span data-stu-id="2def5-134">Check-in for pickup module</span></span>](check-in-pickup-module.md)
