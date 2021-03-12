---
title: Staðfesta greiðsluáætlanir eignarleigu í runu
description: Þetta efnisatriði útskýrir hvernig á að staðfesta margar greiðsluáætlanir í runu.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: b5a90b96ac598d145e2b0697627de04731b55f59
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/28/2020
ms.locfileid: "4444583"
---
# <a name="confirm-asset-leasing-payment-schedules-in-a-batch"></a><span data-ttu-id="1d937-103">Staðfesta greiðsluáætlanir eignarleigu í runu</span><span class="sxs-lookup"><span data-stu-id="1d937-103">Confirm Asset leasing payment schedules in a batch</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1d937-104">Þetta efnisatriði útskýrir hvernig á að staðfesta margar greiðsluáætlanir í runu.</span><span class="sxs-lookup"><span data-stu-id="1d937-104">This topic explains how to confirm multiple payment schedules in a batch.</span></span> <span data-ttu-id="1d937-105">Greiðsluáætlanir eru annaðhvort staðfestar á grundvelli leigusamnings eða í gegnum staðfestingarrunuferli.</span><span class="sxs-lookup"><span data-stu-id="1d937-105">Payment schedules are confirmed either on a lease-to-lease basis or through the confirmation batch process.</span></span> <span data-ttu-id="1d937-106">Aðeins er hægt að bóka bókarfærslu gegn leigusamningi með staðfesta greiðsluáætlun.</span><span class="sxs-lookup"><span data-stu-id="1d937-106">A journal entry can be posted only against a lease that has a confirmed payment schedule.</span></span> <span data-ttu-id="1d937-107">Staðfesting á greiðsluáætlun þjónar sem endanlegt samþykki fjárhagsupplýsinga fyrir leigu.</span><span class="sxs-lookup"><span data-stu-id="1d937-107">Confirmation of the payment schedule serves as a final approval of the financial information for the lease.</span></span> <span data-ttu-id="1d937-108">Allar breytingar á fjárhagsupplýsingum leigusamningsins í framtíðinni eins og greiðslum og leigutímanum eru leiðrétting á leigusamningnum og skal vinna úr þeim á þann hátt.</span><span class="sxs-lookup"><span data-stu-id="1d937-108">All future changes to the financial information for the lease, such as payments and the lease term, constitute a lease adjustment and should be processed in that way.</span></span>

<span data-ttu-id="1d937-109">Til að staðfesta margar greiðsluáætlanir skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="1d937-109">To confirm multiple payment schedules, follow these steps.</span></span>

1. <span data-ttu-id="1d937-110">Opnið **Eignarleiga \> Reglubundið \> Staðfestingarruna**.</span><span class="sxs-lookup"><span data-stu-id="1d937-110">Go to **Asset leasing \> Periodic \> Confirmation batch**.</span></span>
2. <span data-ttu-id="1d937-111">Á síðunni **Staðfestingarruna** skal velja **Staðfestingarruna**.</span><span class="sxs-lookup"><span data-stu-id="1d937-111">On the **Confirmation batch** page, select **Confirmation batch**.</span></span>
3. <span data-ttu-id="1d937-112">Í svarglugganum sem birtist er hægt að sía fyrir bækurnar sem á að staðfesta.</span><span class="sxs-lookup"><span data-stu-id="1d937-112">In the dialog box that appears, filter for the books that you want to confirm.</span></span>

    - <span data-ttu-id="1d937-113">Til að staðfesta allar bækur tiltekins leiguflokks skal velja flokkinn í svæðinu **Leigusamningsflokkur**.</span><span class="sxs-lookup"><span data-stu-id="1d937-113">To confirm all the books in a specific lease group, select the group in the **Lease group** field.</span></span>
    - <span data-ttu-id="1d937-114">Til að staðfesta tilteknar bækur skal velja bækurnar í svæðinu **Bókarkenni**.</span><span class="sxs-lookup"><span data-stu-id="1d937-114">To confirm specific books, select the books in the **Book ID** field.</span></span>
    - <span data-ttu-id="1d937-115">Til að staðfesta allar bækur skal kveikja á færibreytunni **Fyrir allar bækur**.</span><span class="sxs-lookup"><span data-stu-id="1d937-115">To confirm all books, turn on the **For all books** parameter.</span></span>

<span data-ttu-id="1d937-116">Upplýsingar fyrir nýstaðfestar bækur eru sýndar á síðunni **Staðfestar bækur**.</span><span class="sxs-lookup"><span data-stu-id="1d937-116">Information for the newly confirmed books is shown on the **Confirmed books** page.</span></span> <span data-ttu-id="1d937-117">Eftir að greiðsluáætlanir eru staðfestar er hægt að bóka upphaflegar færslur í færslubók gegn leigusamningunum.</span><span class="sxs-lookup"><span data-stu-id="1d937-117">After the payment schedules are confirmed, the initial recognition journal entries can be posted against the leases.</span></span>