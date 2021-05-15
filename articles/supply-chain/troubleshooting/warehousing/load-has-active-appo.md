---
title: Ekki er hægt að staðfesta sendingu vegna dagatalsvandamáls
description: Ekki er hægt að staðfesta sendingu vegna dagatalsvandamáls
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f1fccd10d8867252f32b37c77f9a3bad54157bdd
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938492"
---
# <a name="you-cant-confirm-a-shipment-because-of-an-issue-with-the-calendar"></a><span data-ttu-id="0bb80-103">Ekki er hægt að staðfesta sendingu vegna dagatalsvandamáls</span><span class="sxs-lookup"><span data-stu-id="0bb80-103">You can't confirm a shipment because of an issue with the calendar</span></span>

<span data-ttu-id="0bb80-104">Villukóði TRX2716</span><span class="sxs-lookup"><span data-stu-id="0bb80-104">Error code: TRX2716</span></span>

## <a name="symptoms"></a><span data-ttu-id="0bb80-105">Einkenni</span><span class="sxs-lookup"><span data-stu-id="0bb80-105">Symptoms</span></span>

<span data-ttu-id="0bb80-106">Þegar reynt er að staðfesta sendingu sýnir kerfið eftirfarandi villuboð:</span><span class="sxs-lookup"><span data-stu-id="0bb80-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="0bb80-107">Dagatalsgerðin %1 krefst þess að mót %2 sé skráð inn og út.</span><span class="sxs-lookup"><span data-stu-id="0bb80-107">The calendar type %1 requires the appointment %2 to be checked in and out.</span></span>

<span data-ttu-id="0bb80-108">Því er ekki hægt að staðfesta sendinguna fyrir farminn.</span><span class="sxs-lookup"><span data-stu-id="0bb80-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="0bb80-109">Orsök</span><span class="sxs-lookup"><span data-stu-id="0bb80-109">Cause</span></span>

<span data-ttu-id="0bb80-110">Virkt erindi fyrir hleðsluna er til.</span><span class="sxs-lookup"><span data-stu-id="0bb80-110">Active appointments for the load exist.</span></span> <span data-ttu-id="0bb80-111">Til dæmis er regla sem gerir kröfu um innskráningu ökumanns.</span><span class="sxs-lookup"><span data-stu-id="0bb80-111">For example, there is a rule that requires driver check-in.</span></span> <span data-ttu-id="0bb80-112">Þar af leiðandi er hleðslan eða sendingin í stöðu þar sem staðfesting á sendingu mistekst.</span><span class="sxs-lookup"><span data-stu-id="0bb80-112">Therefore, the load is currently in a state where shipment confirmation fails.</span></span>

## <a name="resolution"></a><span data-ttu-id="0bb80-113">Upplausn</span><span class="sxs-lookup"><span data-stu-id="0bb80-113">Resolution</span></span>

<span data-ttu-id="0bb80-114">Þú verður að kanna og laga öll vandamál með virk erindi sem eru tengd við hleðsluna.</span><span class="sxs-lookup"><span data-stu-id="0bb80-114">You must investigate and fix any issues with the active appointments that are linked to the load.</span></span>

1. <span data-ttu-id="0bb80-115">Farðu í **Vöruhúsakerfi \> Hleðslur \> Allar hleðslur**.</span><span class="sxs-lookup"><span data-stu-id="0bb80-115">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="0bb80-116">Veljið hleðsluna sem ekki er hægt að staðfesta sendinguna fyrir.</span><span class="sxs-lookup"><span data-stu-id="0bb80-116">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="0bb80-117">Á aðgerðasvæðinu, í flipanum **Flutningur**, í flokknum **Erindi**, skal velja **Tímasetning erindis**.</span><span class="sxs-lookup"><span data-stu-id="0bb80-117">On the Action Pane, on the **Transportation** tab, in the **Appointments** group, select **Appointment scheduling**.</span></span>
1. <span data-ttu-id="0bb80-118">Fylgið einu af eftirfarandi skrefum:</span><span class="sxs-lookup"><span data-stu-id="0bb80-118">Follow one of these steps:</span></span>

    - <span data-ttu-id="0bb80-119">Gakktu úr skugga um að inn-/útskráning ökumanns sé lokið fyrir erindið.</span><span class="sxs-lookup"><span data-stu-id="0bb80-119">Make sure that driver check-in/check-out is completed for the appointment.</span></span>
    - <span data-ttu-id="0bb80-120">Ljúktu eða hættu við erindið.</span><span class="sxs-lookup"><span data-stu-id="0bb80-120">Complete or cancel the appointment.</span></span>
    - <span data-ttu-id="0bb80-121">Gera valkostinn **Innskráning ökumanns nauðsynleg** óvirkan fyrir tengda reglu um erindi.</span><span class="sxs-lookup"><span data-stu-id="0bb80-121">Disable the **Driver check-in required** option for the related appointment rule.</span></span>
