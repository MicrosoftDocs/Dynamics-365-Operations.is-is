---
title: Móttaka númeraplötu í gegnum vöruhúsaforritið
description: Þetta efnisatriði útskýrir hvernig á að setja upp vöruhúsaforrit til að styðja notkun móttökuferlis númeraplötu til að taka á móti efnislegum birgðum.
author: perlynne
manager: tfehr
ms.date: 03/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-03-31
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 7d5ac6598ab80ece0164d7c92f5d84e91d21b385
ms.sourcegitcommit: ffd845d4230646499b6f074cb43e69ab95787671
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/07/2020
ms.locfileid: "3346377"
---
# <a name="license-plate-receiving-via-the-warehousing-app"></a><span data-ttu-id="ce1c6-103">Móttaka númeraplötu í gegnum vöruhúsaforritið</span><span class="sxs-lookup"><span data-stu-id="ce1c6-103">License plate receiving via the warehousing app</span></span>

<span data-ttu-id="ce1c6-104">Þetta efnisatriði útskýrir hvernig á að setja upp vöruhúsaforrit þannig að það styðji notkun móttökuferlis númeraplötu til að taka á móti efnislegum birgðum.</span><span class="sxs-lookup"><span data-stu-id="ce1c6-104">This topic explains how to set up the warehousing app so that it supports using a license plate receiving process to receive physical inventory.</span></span>

<span data-ttu-id="ce1c6-105">Þú getur notað þessa aðgerð til að skrá fljótt móttöku á birgðum á innleið sem tengjast tilkynningu um sendingu (ASN).</span><span class="sxs-lookup"><span data-stu-id="ce1c6-105">You can use this functionality to quickly record the receipt of inbound inventory that is related to an advance ship notice (ASN).</span></span> <span data-ttu-id="ce1c6-106">Kerfið stofnar sjálfkrafa ASN þegar ferli vöruhússtjórnunar eru notuð til að senda flutningspöntun.</span><span class="sxs-lookup"><span data-stu-id="ce1c6-106">The system automatically creates an ASN when warehouse management processes are used to ship a transfer order.</span></span> <span data-ttu-id="ce1c6-107">Fyrir innkaupapöntunarferlið er hægt að skrá ASN handvirkt eða flytja það sjálfkrafa inn með því að nota ASN gagnaeiningarferli á innleið.</span><span class="sxs-lookup"><span data-stu-id="ce1c6-107">For the purchase order process, an ASN can be manually recorded, or it can be automatically imported by using an inbound ASN data entity process.</span></span>

<span data-ttu-id="ce1c6-108">ASN gögnin eru tengd við farm og sendingar um *pakkaskipan*, þar sem bretti (yfirnúmeraplötur) geta innihaldið mál (faldaðar númeraplötur).</span><span class="sxs-lookup"><span data-stu-id="ce1c6-108">The ASN data is linked to loads and shipments via the *packing structures*, where pallets (parent license plates) can contain cases (nested license plates).</span></span>

> [!NOTE]
> <span data-ttu-id="ce1c6-109">Til að fækka birgðafærslum þegar pakkaskipan sem hefur faldaðar númeraplötur er notuð skráir kerfið efnislegar lagerbirgðir á yfirnúmeraplötuna.</span><span class="sxs-lookup"><span data-stu-id="ce1c6-109">To reduce the number of inventory transactions when packing structures that have nested license plates are used, the system records the physical on-hand inventory on the parent license plate.</span></span> <span data-ttu-id="ce1c6-110">Til að kveikja á hreyfingu efnislegrar lagerbirgða frá yfirnúmeraplötunni yfir á faldaðar númeraplötur, byggðar á pakkaskipunargögnum, verður fartækið að bjóða upp á valmyndaratriði sem er byggt á vinnusköpunarferlinu *Pakka á faldaðar númeraplötur*.</span><span class="sxs-lookup"><span data-stu-id="ce1c6-110">To trigger the movement of the physical on-hand inventory from the parent license plate to the nested license plates, based on the packing structure data, the mobile device must provide a menu item that is based on the *Pack to nested license plates* work creation process.</span></span>

<!-- To be used later (will require further editing):
## Warehousing mobile device app processing

When a worker scans an incoming license plate ID, the system initializes a license plate receiving process. Based on this information, the content of the license plate (data coming from the ASN) gets physically registered at the inbound dock location. The flows that follow will depend your business process needs.

## Work policies

As with (for example) the *Report as finished* mobile device menu item process, the license plate receiving process supports several workflows based on the defined setup.

### Work policies with work creation

Registration of physical on-hand where either the same warehouse worker immediately process a put-away work process following the inbound receiving (License plate receiving and put away) or where the registration and put away process gets handled as two different warehouse operations (License plate receiving) following the processing of the put-away work by using the existing work process via another mobile device menu item.

## Work policies without work creation

You can use the license plate receiving process without creating work by using the *License plate receiving without creating work* feature.

By defining **Work policies** with a **Work order type** of *Transfer receipt* and/or *Purchase orders*, and using the **Process** for **License plate receiving (and put away)**, the two Warehousing app process:

- License plate receiving
- License plate receiving and put away

will not create work, but only register the inbound physical inventory on the license plate at the inbound receiving dock.

For more information about the *Report as finished* production scenario, see the [Warehouse work policies overview](warehouse-work-policies.md).

-->

## <a name="show-or-skip-the-receiving-summary-page"></a><span data-ttu-id="ce1c6-111">Sýna eða sleppa móttökuyfirlitssíðu</span><span class="sxs-lookup"><span data-stu-id="ce1c6-111">Show or skip the receiving summary page</span></span>

<span data-ttu-id="ce1c6-112">Hægt er að nota eiginleikann *Stjórna því hvort á að birta yfirlitssíðu móttöku í fartækjum* til að nýta sér ítarlegra flæði vöruhúsaforrits sem hluta af móttöku númeraplötu.</span><span class="sxs-lookup"><span data-stu-id="ce1c6-112">You can use the *Control whether to display a receiving summary page on mobile devices* feature to take advantage of an additional detailed warehousing app flow as part of the license plate receiving process.</span></span>

<span data-ttu-id="ce1c6-113">Áður en hægt er að nota þennan eiginleika þarf að kveikja á honum í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="ce1c6-113">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="ce1c6-114">Stjórnendur geta notað stillingarnar [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikja á honum.</span><span class="sxs-lookup"><span data-stu-id="ce1c6-114">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="ce1c6-115">Í vinnusvæðinu **Stjórnun eiginleika** er þessi eiginleiki skráður á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="ce1c6-115">In the **Feature management** workspace, this feature is listed in the following way:</span></span>

- <span data-ttu-id="ce1c6-116">**Eining:** *Vöruhúsakerfi*</span><span class="sxs-lookup"><span data-stu-id="ce1c6-116">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="ce1c6-117">**Eiginleikaheiti:** *Stjórna því hvort sýna á viðtakandi samantektarsíðu í fartækjum*</span><span class="sxs-lookup"><span data-stu-id="ce1c6-117">**Feature name:** *Control whether to display a receiving summary page on mobile devices*</span></span>

<span data-ttu-id="ce1c6-118">Þegar kveikt er á þessari aðgerð munu valmyndaratriðin í fartækinu fyrir móttöku númeraplötu eða móttöku og frágang númeraplötu veita stillinguna **Birta yfirlitssíðu móttöku**.</span><span class="sxs-lookup"><span data-stu-id="ce1c6-118">When this feature is turned on, mobile device menu items for license plate receiving or license plate receiving and put-away will provide a **Display receiving summary page** setting.</span></span> <span data-ttu-id="ce1c6-119">Þessi stilling hefur eftirfarandi valkosti:</span><span class="sxs-lookup"><span data-stu-id="ce1c6-119">This setting has the following options:</span></span>

- <span data-ttu-id="ce1c6-120">**Birta ítarlegt yfirlit** - Við móttöku númeraplötu munu starfsmenn sjá auka síðu sem sýnir allar ASN upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="ce1c6-120">**Display a detailed summary** – During license plate receiving, workers will see an extra page that shows the full ASN information.</span></span>
- <span data-ttu-id="ce1c6-121">**Sleppa yfirlitinu** - Starfsmenn sjá ekki allar ASN upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="ce1c6-121">**Skip the summary** – Workers won't see the full ASN information.</span></span> <span data-ttu-id="ce1c6-122">Starfsmenn vörugeymsluhússins ekki heldur sett upp ráðstöfunarkóða eða bætt við undantekningum meðan á móttökuferlinu stendur.</span><span class="sxs-lookup"><span data-stu-id="ce1c6-122">Warehouse workers also won't be able to set a disposition code or add exceptions during the receiving process.</span></span>

## <a name="prevent-transfer-ordershipped-license-plates-from-being-used-at-warehouses-other-than-the-destination-warehouse"></a><span data-ttu-id="ce1c6-123">Komdu í veg fyrir að númeraplötur með flutningspöntunum–sent séu notaðar í vöruhúsum öðrum en ákvörðunarvöruhúsinu</span><span class="sxs-lookup"><span data-stu-id="ce1c6-123">Prevent transfer order–shipped license plates from being used at warehouses other than the destination warehouse</span></span>

<span data-ttu-id="ce1c6-124">Ekki er hægt að nota móttökuferli númeraplötu ef ASN inniheldur kenni númeraplötu sem þegar eru til og eru með efnisleg gögn á lager í öðru vöruhúsi en vöruhússtaðnum þar sem skráningarmerki skráningar er að gerast.</span><span class="sxs-lookup"><span data-stu-id="ce1c6-124">A license plate receiving process can't be used if an ASN contains a license plate ID that already exists and has physical on-hand data at a warehouse location other than the warehouse location where the license plate registration is occurring.</span></span>

<span data-ttu-id="ce1c6-125">Fyrir aðstæður flutningspöntunar þar sem flutningsvöruhúsið rekur ekki númeraplöturnar (og rekur þar af leiðandi ekki heldur efnislegar lagerbirgðir á hverja númeraplötu) er hægt að nota eiginleikann *Koma í veg fyrir að númeraplötur með sendum flutningspöntunum séu notaðar í öðrum vöruhúsum en ákvörðunarvöruhúsinu* til að koma í veg fyrir efnislegar birgðauppfærslur á númeraplötum sem eru í flutningi.</span><span class="sxs-lookup"><span data-stu-id="ce1c6-125">For transfer order scenarios where the transit warehouse doesn't track license plates (and therefore also doesn't track physical on-hand inventory per license plate), you can use the *Prevent transfer order shipped license plates from being used on other warehouses than the destination warehouse* feature to prevent physical on-hand updates of license plates that are in transit.</span></span>

<span data-ttu-id="ce1c6-126">Áður en hægt er að nota þennan eiginleika þarf að kveikja á honum í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="ce1c6-126">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="ce1c6-127">Stjórnendur geta notað stillingarnar [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikja á honum.</span><span class="sxs-lookup"><span data-stu-id="ce1c6-127">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="ce1c6-128">Í vinnusvæðinu **Stjórnun eiginleika** er þessi eiginleiki skráður á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="ce1c6-128">In the **Feature management** workspace, this feature is listed in the following way:</span></span>

- <span data-ttu-id="ce1c6-129">**Eining:** *Vöruhúsakerfi*</span><span class="sxs-lookup"><span data-stu-id="ce1c6-129">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="ce1c6-130">**Heiti eiginleika:** *Koma í veg fyrir að númeraplötur með sendum flutningspöntunum séu notaðar í öðrum vöruhúsum en ákvörðunarvöruhúsinu*</span><span class="sxs-lookup"><span data-stu-id="ce1c6-130">**Feature name:** *Prevent transfer order shipped license plates from being used on other warehouses than the destination warehouse*</span></span>

<span data-ttu-id="ce1c6-131">Fylgdu þessum skrefum til að stjórna virkni þegar þessi eiginleiki er tiltækur.</span><span class="sxs-lookup"><span data-stu-id="ce1c6-131">To manage the functionality when this feature is available, follow these steps.</span></span>

1. <span data-ttu-id="ce1c6-132">Farðu í **vöruhúsakerfi \> Uppsetning \> Færibreytur vöruhúsakerfis**.</span><span class="sxs-lookup"><span data-stu-id="ce1c6-132">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="ce1c6-133">Á flipanum **Almennt**, á flýtiflipanum **Númeraplötur**, stillirðu reitinn **Reglur um númeraplötu flutningsvöruhúsa** á eitt af eftirfarandi gildum:</span><span class="sxs-lookup"><span data-stu-id="ce1c6-133">On the **General** tab, on the **License plates** FastTab, set the **Transit warehouse license plate policy** field to one of the following values:</span></span>

    - <span data-ttu-id="ce1c6-134">**Leyfa endurnotkun á óröktum númeraplötum** - Kerfið virkar á sama hátt og það virkar þegar eiginleikinn *Koma í veg fyrir að númeraplötur með sendum flutningspöntunum séu notaðar í öðrum vöruhúsum en ákvörðunarvöruhúsinu* er ekki í boði.</span><span class="sxs-lookup"><span data-stu-id="ce1c6-134">**Allow reuse of non-tracked license plate** – The system works the same way that it works when the *Prevent transfer order shipped license plates from being used on other warehouses than the destination warehouse* feature isn't available.</span></span> <span data-ttu-id="ce1c6-135">Þetta gildi er sjálfgefin stilling þegar þú virkjar eiginleikann fyrst.</span><span class="sxs-lookup"><span data-stu-id="ce1c6-135">This value is the default setting when you first activate the feature.</span></span>
    - <span data-ttu-id="ce1c6-136">**Koma í veg fyrir endurnotkun á óröktum númeraplötum** - Aðeins handvirkar uppfærslur sem tengjast sendum númeraplötum verða leyfðar í ákvörðunarvöruhúsinu þar til flutningspöntunin hefur borist.</span><span class="sxs-lookup"><span data-stu-id="ce1c6-136">**Prevent reuse of non-tracked license plate** – Only on-hand updates that are related to a shipped license plate will be allowed at the destination warehouse until the transfer order has been received.</span></span>

## <a name="more-information"></a><span data-ttu-id="ce1c6-137">Meiri upplýsingar</span><span class="sxs-lookup"><span data-stu-id="ce1c6-137">More information</span></span>

<!-- To read more about inbound loads, see [Link for Inbound load (Olga's doc.)] -->

<span data-ttu-id="ce1c6-138">Nánari upplýsingar um valmyndaratriði fartækja, sjá [Uppsetning fartækja fyrir vöruhúsavinnu](configure-mobile-devices-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="ce1c6-138">For more information about mobile device menu items, see [Set up mobile devices for warehouse work](configure-mobile-devices-warehouse.md).</span></span>
