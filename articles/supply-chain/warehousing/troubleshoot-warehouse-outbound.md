---
title: Úrræðaleit fyrir vöruhúsaaðgerðir á útleið
description: Í þessu efnisatriði er því lýst hvernig á að laga vandamál sem kunna að koma upp þegar unnið er með innkaupapantanir i Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 56bd91d8a6fe895317021d806e180df3a2db302b
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645452"
---
# <a name="troubleshoot-outbound-warehouse-operations"></a><span data-ttu-id="d56a1-103">Úrræðaleit fyrir vöruhúsaaðgerðir á útleið</span><span class="sxs-lookup"><span data-stu-id="d56a1-103">Troubleshoot outbound warehouse operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d56a1-104">Í þessu efnisatriði er því lýst hvernig á að laga vandamál sem kunna að koma upp þegar unnið er með innkaupapantanir i Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="d56a1-104">This topic describes how to fix common issues that you might encounter while you work with outbound warehouse operations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-sales-order-could-not-be-released"></a><span data-ttu-id="d56a1-105">Ég fékk eftirfarandi villuboð: Ekki var hægt að losa sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="d56a1-105">I receive the following error message: "Sales order could not be released."</span></span>

### <a name="issue-description"></a><span data-ttu-id="d56a1-106">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="d56a1-106">Issue description</span></span>

<span data-ttu-id="d56a1-107">Þetta vandamál getur komið upp af ýmsum ástæðum.</span><span class="sxs-lookup"><span data-stu-id="d56a1-107">This issue can occur for several reasons.</span></span> <span data-ttu-id="d56a1-108">Til dæmis, pöntunin er í lánastýringarbið og ekki er hægt að stofna sendingar fyrr en gilt póstfang er fært inn fyrir allar sölulínur sem tengjast sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="d56a1-108">For example, the order is on credit management hold, and no shipments can be created until a valid postal address is entered for all sales lines that are associated with a sales order.</span></span> <span data-ttu-id="d56a1-109">Að öðrum kosti er pöntunarbið sem þarf að leysa áður en hægt er að losa pöntunina í vöruhúsið.</span><span class="sxs-lookup"><span data-stu-id="d56a1-109">Alternatively, there is an order hold that must be addressed before the order can be released to the warehouse.</span></span> <span data-ttu-id="d56a1-110">Þessi bið gæti verið bundin við pöntunina eða hún kann að vera á viðskiptavinalykli.</span><span class="sxs-lookup"><span data-stu-id="d56a1-110">This hold might be order-specific, or it might be on the customer account.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="d56a1-111">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="d56a1-111">Issue resolution</span></span>

<span data-ttu-id="d56a1-112">Bæta við eða uppfæra aðsetur á sölupöntunum og pöntunarlínunum og losa svo pöntunina í vöruhúsið.</span><span class="sxs-lookup"><span data-stu-id="d56a1-112">Add or update the address on the sales order and order lines, and then release the order to the warehouse.</span></span> <span data-ttu-id="d56a1-113">Aðeins er hægt að losa pantanir í vöruhúsið ef þær hafa gilt afhendingaraðsetur (samkvæmt uppsetningu á sniði aðseturs í einingunni **Fyrirtækisstjórnun**).</span><span class="sxs-lookup"><span data-stu-id="d56a1-113">Orders can be released to the warehouse only if they have a valid delivery address (per the address format setup in the **Organization administration** module).</span></span>

<span data-ttu-id="d56a1-114">Rannsaka pöntun í bið og leysa vandamálið.</span><span class="sxs-lookup"><span data-stu-id="d56a1-114">Investigate the order hold, and address the issues.</span></span> <span data-ttu-id="d56a1-115">Taktu síðan biðina af pöntuninni eða viðskiptavininum og losaðu pöntunina í vöruhúsið.</span><span class="sxs-lookup"><span data-stu-id="d56a1-115">Then remove the hold from the order or customer, and release the order to the warehouse.</span></span>

## <a name="i-receive-the-following-message-the-shipment-for-load-1-has-been-confirmed-however-no-lines-are-posted"></a><span data-ttu-id="d56a1-116">Ég fæ eftirfarandi skilaboð: „Sending á farmi 1% hefur verið staðfest“.</span><span class="sxs-lookup"><span data-stu-id="d56a1-116">I receive the following message: "The shipment for load 1% has been confirmed."</span></span> <span data-ttu-id="d56a1-117">Hins vegar eru engar línur bókaðar.</span><span class="sxs-lookup"><span data-stu-id="d56a1-117">However, no lines are posted.</span></span>

### <a name="issue-description"></a><span data-ttu-id="d56a1-118">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="d56a1-118">Issue description</span></span>

<span data-ttu-id="d56a1-119">Sending í farmi var staðfest en engin frekari bókun fór fram.</span><span class="sxs-lookup"><span data-stu-id="d56a1-119">A shipment on a load was confirmed, but no further posting occurred.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="d56a1-120">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="d56a1-120">Issue resolution</span></span>

<span data-ttu-id="d56a1-121">Staðfesting sendingar hefur ekki áhrif á bókun.</span><span class="sxs-lookup"><span data-stu-id="d56a1-121">Shipment confirmation doesn't affect posting.</span></span> <span data-ttu-id="d56a1-122">Þetta uppfærir bara sendingu og hleðslustöðu.</span><span class="sxs-lookup"><span data-stu-id="d56a1-122">It just updates the shipment and load status.</span></span> <span data-ttu-id="d56a1-123">Bókun verður að eiga sér stað í aðgreindu ferli.</span><span class="sxs-lookup"><span data-stu-id="d56a1-123">Posting must occur in a separate process.</span></span>

## <a name="i-receive-the-following-error-message-direct-delivery-is-not-able-to-process-for-warehouse-1-as-it-has-warehouse-management-enabled-please-specify-another-warehouse-that-is-not-enabled-for-warehouse-management"></a><span data-ttu-id="d56a1-124">Ég fæ eftirfarandi villuboð: „Ekki er hægt að vinna úr beinni afhendingu fyrir vöruhús 1% því vöruhúsakerfi er virkt.</span><span class="sxs-lookup"><span data-stu-id="d56a1-124">I receive the following error message: "Direct delivery is not able to process for warehouse 1% as it has warehouse management enabled.</span></span> <span data-ttu-id="d56a1-125">Tilgreinið annað vöruhús sem er ekki virkt fyrir vöruhúsastjórnun.</span><span class="sxs-lookup"><span data-stu-id="d56a1-125">Please specify another warehouse that is not enabled for warehouse management."</span></span>

### <a name="issue-description"></a><span data-ttu-id="d56a1-126">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="d56a1-126">Issue description</span></span>

<span data-ttu-id="d56a1-127">Vöru er bætt við sölulínu fyrir beina afhendingu úr vöruhúsi þar sem vöruhúsakerfi (WMS) er virkt.</span><span class="sxs-lookup"><span data-stu-id="d56a1-127">An item is added to a sales line for direct delivery from a warehouse that is enabled for warehouse management (WMS).</span></span> <span data-ttu-id="d56a1-128">Þessi villuboð birtast þegar sölulína er uppfærð.</span><span class="sxs-lookup"><span data-stu-id="d56a1-128">You receive this error message when the sales line is updated.</span></span> 

### <a name="issue-resolution"></a><span data-ttu-id="d56a1-129">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="d56a1-129">Issue resolution</span></span>

<span data-ttu-id="d56a1-130">Microsoft hefur metið þetta mál og hefur ákvarðað að þetta sé takmörkun eiginleika.</span><span class="sxs-lookup"><span data-stu-id="d56a1-130">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="d56a1-131">Sem stendur styður vöruhúsakerfi ekki beina afhendingu.</span><span class="sxs-lookup"><span data-stu-id="d56a1-131">Currently, WMS doesn't support direct delivery.</span></span> <span data-ttu-id="d56a1-132">Til að nota beina afhendingu skal því velja vöru sem er ekki WMS og vöruhús.</span><span class="sxs-lookup"><span data-stu-id="d56a1-132">Therefore, to use direct delivery, you must select a non-WMS item and warehouse.</span></span>
