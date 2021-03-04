---
title: Uppsetning á greiðsluaðstæðum reikninga
description: Þetta efnisatriði lýsir því hvernig á að grunnstilla Dynamics 365 Commerce til að styðja ýmsar aðstæður sem tengjast greiðslu reikninga.
author: josaw1
manager: AnnBe
ms.date: 11/14/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8b65fe3968698da1c5b76cf2d0ef706f3f1ec4bb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972658"
---
# <a name="set-up-pay-invoice-scenarios"></a><span data-ttu-id="67e37-103">Uppsetning á greiðsluaðstæðum reikninga</span><span class="sxs-lookup"><span data-stu-id="67e37-103">Set up pay invoice scenarios</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="67e37-104">Greiðsluaðgerð reiknings í Dynamics 365 Commerce hefur verið víkkuð út til að styðja:</span><span class="sxs-lookup"><span data-stu-id="67e37-104">The Pay invoice functionality in Dynamics 365 Commerce has been expanded to support:</span></span>

- <span data-ttu-id="67e37-105">Greiðslu á mörgum sölupöntunarreikningum í einni POS-færslu.</span><span class="sxs-lookup"><span data-stu-id="67e37-105">Payoff of multiple sales order invoices in a single POS transaction.</span></span>
- <span data-ttu-id="67e37-106">Greiðslu á ýmsum reikningsgerðum viðskiptavina, þ.á.m. reikningum með frjálsum texta, verktengdum reikningum og kreditnótum.</span><span class="sxs-lookup"><span data-stu-id="67e37-106">Payment of various customer invoice types including free text invoices, project-based invoices, and credit notes.</span></span>

<span data-ttu-id="67e37-107">Til að virkja þessar aðstæður þarf að grunnstilla virkniregluna fyrir verslanir eins og útskýrt er hér að neðan.</span><span class="sxs-lookup"><span data-stu-id="67e37-107">To enable these scenarios, the functionality profile for stores must be configured as outlined in below.</span></span>

1. <span data-ttu-id="67e37-108">Opnið **Retail and Commerce\> Uppsetning rásar \> Uppsetning sölustaðar \> Forstillingar sölustaðar \> Virknireglur** og veljið forstillingu sem tengd er við verslanirnar sem á að gera breytingar á.</span><span class="sxs-lookup"><span data-stu-id="67e37-108">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS profiles \> Functionality profiles** and select a profile that's linked to the stores that you want to make the changes for.</span></span>
2. <span data-ttu-id="67e37-109">Á flipanum **Aðgerðir** skal skilgreina eftirfarandi færibreytur eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="67e37-109">On the **Functions** tab, configure the following parameters as needed.</span></span>

    - <span data-ttu-id="67e37-110">**Sölupöntunarreikningur** – Veljið **Já** til að gera notendum kleift að greiða einn eða fleiri reikninga sem tengjast sölupöntun í einni sölustaðarfærslu.</span><span class="sxs-lookup"><span data-stu-id="67e37-110">**Sales order invoice** – Select **Yes** to allow users to pay one or more sales order-based invoices in a single POS transaction.</span></span>
    - <span data-ttu-id="67e37-111">**Reikningur með frjálsum texta** – Veljið **Já** til að gera notendum kleift að greiða einn eða fleiri reikninga með frjálsum texta í einni sölustaðarfærslu.</span><span class="sxs-lookup"><span data-stu-id="67e37-111">**Free text invoice** – Select **Yes** to allow users to pay one or more free text-based invoices in a single POS transaction.</span></span>
    - <span data-ttu-id="67e37-112">**Verkreikningur** – Veljið **Já** til að gera notendum kleift að greiða einn eða fleiri reikninga sem tengjast verki í einni sölustaðarfærslu.</span><span class="sxs-lookup"><span data-stu-id="67e37-112">**Project invoice** – Select **Yes** to allow users to pay one or more project-based invoices in a single POS transaction.</span></span>
    - <span data-ttu-id="67e37-113">**Kreditnóta sölupöntunar** – Veljið **Já** til að gera notendum kleift að gera upp margar kreditnótur sem tengjast sölupöntun gagnvart opnum reikningum eða vinna úr endurgreiðslu til viðskiptavinar vegna opinnar kreditnótu.</span><span class="sxs-lookup"><span data-stu-id="67e37-113">**Sales order credit note** – Select **Yes** to allow users to settle multiple sales order-based credit notes against open invoices or process a refund to the customer for an open credit note.</span></span>

> [!NOTE]
> <span data-ttu-id="67e37-114">Greiðsla eða uppgjör upphæða að hluta til er ekki enn studd.</span><span class="sxs-lookup"><span data-stu-id="67e37-114">Payment or settlement of partial amounts is not yet supported.</span></span>
