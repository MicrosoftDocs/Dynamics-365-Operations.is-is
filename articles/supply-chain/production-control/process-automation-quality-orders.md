---
title: Kalla fram sjálfvirkni ferilflæðis til að stofna gæðapantanir
description: Í þessu efnisatriði er að finna úrræði til að nota Power Automate til að gera viðskiptaferla sjálfvirka með því að nota dæmið um gæðapantanir.
author: cabeln
ms.date: 05/28/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: cabeln
ms.search.validFrom: 2021-05-28
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: f35adab3075ba810964a41899ba95ae40c115e83
ms.sourcegitcommit: 588f8343aaa654309d2ff735fd437dba6acd9d46
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115192"
---
# <a name="invoke-process-automation-flows-to-create-quality-orders"></a><span data-ttu-id="f81dd-103">Kalla fram sjálfvirkni ferilflæðis til að stofna gæðapantanir</span><span class="sxs-lookup"><span data-stu-id="f81dd-103">Invoke process automation flows to create quality orders</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="f81dd-104">Aukin krafa er á fyrirtækjum að gera viðskiptaferla sjálfvirka, bjóða upp á þægilegri samskipti við starfsfólkið og nýta sér ýmsar vísbendingar frá gögnum og kerfum til að keyra viðskiptaferla með sjálfvirkum hætti.</span><span class="sxs-lookup"><span data-stu-id="f81dd-104">Organizations have an increasing demand to automate standard business processes, provide more convenient interactions to the staff, and utilize various data signals and systems to drive business processes automatically.</span></span> <span data-ttu-id="f81dd-105">Með tölvustýrðri sjálfvirknivæðingu ferla (RPA) og Microsoft Power Automate geta fyrirtæki notað viðmót án kóða til að gera endurtekna ferla sjálfvirka og auka þar af leiðandi skilvirkni og nákvæmni.</span><span class="sxs-lookup"><span data-stu-id="f81dd-105">With robotic process automation (RPA) and Microsoft Power Automate, businesses can use a no-code experience to automate repetitive processes, thus gaining efficiency and accuracy.</span></span>

<span data-ttu-id="f81dd-106">Sniðmát sjálfvirknivæðingar fyrir Supply Chain Management sem hægt er að hlaða niður sýnir hvernig hægt er að nota Power Automate til að gera viðskiptaferla sjálfvirka með því að nota gæðapantanir sem dæmi.</span><span class="sxs-lookup"><span data-stu-id="f81dd-106">The downloadable automation solution template for Supply Chain Management showcases how Power Automate can be used to automate business processes using quality orders as an example.</span></span>

<span data-ttu-id="f81dd-107">Þú getur sótt sniðmát sjálfvirkrar lausnar [hér](https://aka.ms/D365SCMQualityOrderRPASolution).</span><span class="sxs-lookup"><span data-stu-id="f81dd-107">You can download the automation solution template [here](https://aka.ms/D365SCMQualityOrderRPASolution).</span></span>

<span data-ttu-id="f81dd-108">Til að fá yfirlit yfir þennan eiginleika og möguleika hans skal sjá eftirfarandi myndband: [Nota RPA til að stofna gæðapöntun í Dynamics 365 Supply Chain Management](https://www.youtube.com/watch?v=LFbzJ6-H89w)</span><span class="sxs-lookup"><span data-stu-id="f81dd-108">For an overview of this feature and its capabilities, see the following video: [Utilize RPA to create quality orders in Dynamics 365 Supply Chain Management](https://www.youtube.com/watch?v=LFbzJ6-H89w)</span></span>

<span data-ttu-id="f81dd-109">![Valmögulegar sjálfvirkni með RPA](media/rpa-automation-options.png "Valmögulegar sjálfvirkni með RPA")</span><span class="sxs-lookup"><span data-stu-id="f81dd-109">![Automation options with RPA](media/rpa-automation-options.png "Automation options with RPA")</span></span>

<span data-ttu-id="f81dd-110">Sniðmátslausnin Power Automate inniheldur sjálfvirknivæðingu í skýi og sjálfvirknivæðingu borðtölvu sem gera stofnun gæðapantana sjálfvirka í Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f81dd-110">The Power Automate solution template includes a cloud automation flow and a desktop automation flow that automate the creation of quality orders in Supply Chain Management.</span></span>

<span data-ttu-id="f81dd-111">Hægt er að hefja sjálfvirknina til að bregðast við mörgum tilvikum og merkjum, þ.m.t. innslátt notanda eða merki vélar (þ.m.t. Internet hlutanna (IoT)).</span><span class="sxs-lookup"><span data-stu-id="f81dd-111">The automation can be started in response to many events and signals, including user input or machine signals (including the Internet of Things (IoT)).</span></span> <span data-ttu-id="f81dd-112">*G-pöntun* Power Application dæmið er tekið með í sniðmáti lausnarinnar.</span><span class="sxs-lookup"><span data-stu-id="f81dd-112">The *Q-Order* Power Application example is included in the solution template.</span></span> <span data-ttu-id="f81dd-113">Það gerir notanda kleift að skanna QR-kóða vöru, slá inn magn og hengja myndir við með myndavél.</span><span class="sxs-lookup"><span data-stu-id="f81dd-113">It allows the user to scan an item QR code, enter quantity, and attach pictures using a camera.</span></span>

<span data-ttu-id="f81dd-114">Færibreytur lausnar eru teknar með til að stilla sjálfvirknina fyrir tiltekið notkunartilfelli í framleiðslustöð.</span><span class="sxs-lookup"><span data-stu-id="f81dd-114">Solution parameters are included to configure the automation for a specific use case in a production facility.</span></span>

<span data-ttu-id="f81dd-115">![Stofna gæðapöntun](media/rpa-create-quality-roder.png "Stofna gæðapöntun")</span><span class="sxs-lookup"><span data-stu-id="f81dd-115">![Create quality order](media/rpa-create-quality-roder.png "Create quality order")</span></span>

<span data-ttu-id="f81dd-116">Fyrir ítarlegar leiðbeiningar um hvernig á að hlaða niður, setja upp og nota sýnishornalausnina fyrir sjálfvirkni á stofnun gæðapöntunar skal skoða [Gera stofnun gæðapöntunar sjálfvirka í Dynamics 365 Supply Chain Management með tölvustýrðri sjálfvirkni á ferlum með því að nota Power Automate Desktop](/power-automate/desktop-flows/dynamics365-scm-rpa).</span><span class="sxs-lookup"><span data-stu-id="f81dd-116">For a complete step-by-step guide about how to download, install, and use the sample solution for automating quality order creation, see [Automate quality order creation on Dynamics 365 Supply Chain Management with Robotic Process Automation using Power Automate Desktop](/power-automate/desktop-flows/dynamics365-scm-rpa).</span></span>

