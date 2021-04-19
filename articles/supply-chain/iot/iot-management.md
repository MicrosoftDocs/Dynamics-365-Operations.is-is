---
title: Fylgjast með og stjórna IoT-gervigreind
description: Þetta efnisatriði útskýrir hvernig á að fylgjast með og stjórna IoT-gervigreind.
author: robinarh
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: rhaertle
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 94665b3646456b689a8e65e94b098e86e467d5e3
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813076"
---
# <a name="monitor-and-manage-iot-intelligence"></a><span data-ttu-id="24a8e-103">Fylgjast með og stjórna IoT-gervigreind</span><span class="sxs-lookup"><span data-stu-id="24a8e-103">Monitor and manage IoT Intelligence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="24a8e-104">Þetta efnisatriði útskýrir hvernig á að fylgjast með og stjórna IoT-gervigreind.</span><span class="sxs-lookup"><span data-stu-id="24a8e-104">This topic explains how to monitor and manage IoT Intelligence.</span></span>

## <a name="monitor-scenarios-in-microsoft-dynamics-365-supply-chain-management"></a><a id="monitor-scenarios"></a><span data-ttu-id="24a8e-105">Fylgjast með aðstæðum í Microsoft Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="24a8e-105">Monitor scenarios in Microsoft Dynamics 365 Supply Chain Management</span></span>

<span data-ttu-id="24a8e-106">Hægt er að fylgjast með vinnslu á IoT-gervigreind frá nokkrum stöðum:</span><span class="sxs-lookup"><span data-stu-id="24a8e-106">You can monitor IoT Intelligence processing from several places:</span></span>

+ <span data-ttu-id="24a8e-107">**Einingar \> Framleiðslustýring \> Fyrirspurnir og skýrslur \> IoT-gervigreind \> Tilkynningar** – Skoða lista yfir óleystar tilkynningar.</span><span class="sxs-lookup"><span data-stu-id="24a8e-107">**Modules \> Production control \> Inquiries and reports \> IoT Intelligence \> Notifications** – View the list of unresolved notifications.</span></span>
+ <span data-ttu-id="24a8e-108">**Einingar \> Framleiðslustýring \> Fyrirspurnir og skýrslur \> IoT-gervigreind \> Lokaðar tilkynningar** – Skoða lista yfir tilkynningar sem leyst hefur verið út eða hafa verið hundsaðar.</span><span class="sxs-lookup"><span data-stu-id="24a8e-108">**Modules \> Production control \> Inquiries and reports \> IoT Intelligence \> Closed notifications** – View the list of notifications that have been resolved or dismissed.</span></span>
+ <span data-ttu-id="24a8e-109">**Einingar \> Framleiðslustýring \> Fyrirspurnir og skýrslur \> IoT-gervigreind \> Mælingalyklar** – Skoða mælingalykla fyrir **Staða tilfanga** á gröfum tímaraða.</span><span class="sxs-lookup"><span data-stu-id="24a8e-109">**Modules \> Production control \> Inquiries and reports \> IoT Intelligence \> Metric keys** – View the metric keys for the **Resource Status** times series charts.</span></span>
+ <span data-ttu-id="24a8e-110">**Einingar \> Framleiðslustýring \> Framkvæmd framleiðslu \> Tilfangastaða** – Rekja tiltekna mælikvarða með því að nota svargluggann **Skilgreina**.</span><span class="sxs-lookup"><span data-stu-id="24a8e-110">**Modules \> Production control \> Manufacturing execution \> Resource status** – Track specific metrics by using the **Configure** dialog box.</span></span> <span data-ttu-id="24a8e-111">Ef aðstæður skynja undantekningu sýnir tilkynning upplýsingar um undantekningu.</span><span class="sxs-lookup"><span data-stu-id="24a8e-111">If a scenario detects an exception, a notification shows the details of the exception.</span></span>
+ <span data-ttu-id="24a8e-112">**Vinnusvæði \> Stjórnun á framleiðslugólfi \> Tilkynningar** – Skoða lista yfir óleystar tilkynningar.</span><span class="sxs-lookup"><span data-stu-id="24a8e-112">**Workspaces \> Production floor management \> Notifications** – View the list of unresolved notifications.</span></span>

## <a name="modify-a-running-iot-intelligence-scenario"></a><span data-ttu-id="24a8e-113">Breyta aðstæðum IoT-gervigreind í vinnslu</span><span class="sxs-lookup"><span data-stu-id="24a8e-113">Modify a running IoT Intelligence scenario</span></span>

<span data-ttu-id="24a8e-114">Þegar aðstæður eru í vinnslu er hægt að gera þessar breytingar:</span><span class="sxs-lookup"><span data-stu-id="24a8e-114">When a scenario is running, you can make these changes:</span></span>

+ <span data-ttu-id="24a8e-115">Bæta við nýjum skemaskilgreiningum skynjara.</span><span class="sxs-lookup"><span data-stu-id="24a8e-115">Add new sensor schema definitions.</span></span>
+ <span data-ttu-id="24a8e-116">Veljið ný gagnagildi merkis.</span><span class="sxs-lookup"><span data-stu-id="24a8e-116">Select new signal data values.</span></span>
+ <span data-ttu-id="24a8e-117">Hætta við val á fyrirliggjandi gagnagildum merkis.</span><span class="sxs-lookup"><span data-stu-id="24a8e-117">Cancel the selection of existing signal data values.</span></span>
+ <span data-ttu-id="24a8e-118">Bæta við og varpa nýjum gagnagildum merkis.</span><span class="sxs-lookup"><span data-stu-id="24a8e-118">Add and map new signal data values.</span></span>
+ <span data-ttu-id="24a8e-119">Uppfæra þröskuldsgildi.</span><span class="sxs-lookup"><span data-stu-id="24a8e-119">Update threshold values.</span></span>

<span data-ttu-id="24a8e-120">Þegar aðstæður eru í vinnslu eru þessar breytingar bannaðar:</span><span class="sxs-lookup"><span data-stu-id="24a8e-120">When a scenario is running, these changes are prohibited:</span></span>

+ <span data-ttu-id="24a8e-121">Eyða eða breyta skemaskilgreiningum sem verið er að nota í virkjuðum aðstæðum.</span><span class="sxs-lookup"><span data-stu-id="24a8e-121">Delete or modify any schema definitions that are currently consumed by an enabled scenario.</span></span>
+ <span data-ttu-id="24a8e-122">Breyta völdum skemaleiðum í virkum aðstæðum.</span><span class="sxs-lookup"><span data-stu-id="24a8e-122">Change the enabled scenario's selected schema paths.</span></span>

## <a name="simulation-options"></a><span data-ttu-id="24a8e-123">Hermivalkostir</span><span class="sxs-lookup"><span data-stu-id="24a8e-123">Simulation options</span></span>

<span data-ttu-id="24a8e-124">Hægt er að líkja eftir merkjum verksmiðjuvélar.</span><span class="sxs-lookup"><span data-stu-id="24a8e-124">You can simulate factory machine signals.</span></span> <span data-ttu-id="24a8e-125">Nánari upplýsingar eru í þessum efnisatriðum:</span><span class="sxs-lookup"><span data-stu-id="24a8e-125">For more information, see these topics:</span></span>

+ [<span data-ttu-id="24a8e-126">Tengja IoT DevKit AZ3166 við Azure IoT Hub</span><span class="sxs-lookup"><span data-stu-id="24a8e-126">Connect IoT DevKit AZ3166 to Azure IoT Hub</span></span>](https://docs.microsoft.com/azure/iot-hub/iot-hub-arduino-iot-devkit-az3166-get-started)
+ [<span data-ttu-id="24a8e-127">Tengja Raspberry Pi netherbi við Azure IoT Hub (Node.js)</span><span class="sxs-lookup"><span data-stu-id="24a8e-127">Connect Raspberry Pi online simulator to Azure IoT Hub (Node.js)</span></span>](https://docs.microsoft.com/azure/iot-hub/iot-hub-raspberry-pi-web-simulator-get-started)
+ [<span data-ttu-id="24a8e-128">Yfirlit yfir hraðal tækjahermis</span><span class="sxs-lookup"><span data-stu-id="24a8e-128">Device Simulation solution accelerator overview</span></span>](https://docs.microsoft.com/azure/iot-accelerators/iot-accelerators-device-simulation-overview)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]