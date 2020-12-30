---
title: Aðalsvæðissniðmát flutningsstjórnunar
description: Í þessu efnisatriði er útskýrt hvernig flutningsstjórnun gerir notendum kleift að skipt landfræðilegum staðsetningum niður í svæði.
author: Henrikan
manager: ''
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSZoneMaster
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 12234
ms.assetid: b878478c-0e04-4a1e-a037-6fdbb345a9a3
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-01-09
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 2112e7131281cd485b580fd71536981c1ba4aefd
ms.sourcegitcommit: fe7ac653efcb1ac6318083f482394b96ed82b4c7
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/29/2020
ms.locfileid: "4430800"
---
# <a name="transportation-management-zone-master"></a><span data-ttu-id="656e3-103">Aðalsvæðissniðmát flutningsstjórnunar</span><span class="sxs-lookup"><span data-stu-id="656e3-103">Transportation management zone master</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="656e3-104">Með flutningsstjórnun geturðu skipt landfræðilegum stöðum niður í svæði.</span><span class="sxs-lookup"><span data-stu-id="656e3-104">Transport management lets you divide geographic locations into zones.</span></span> <span data-ttu-id="656e3-105">Skipting staðsetninga í svæði getur hjálpað til við að:</span><span class="sxs-lookup"><span data-stu-id="656e3-105">Dividing locations into zones can help to:</span></span>

- <span data-ttu-id="656e3-106">**Einfalda flutningsverð** – Verð eftir svæðum getur verið einfaldara en verð sem byggir á staðsetningu, sérstaklega þegar flutningsstaðir eru dreifðir.</span><span class="sxs-lookup"><span data-stu-id="656e3-106">**Simplify transportation pricing** – Zone-wise pricing can be simpler than individual location-based pricing, especially when transportation locations are scattered.</span></span>
- <span data-ttu-id="656e3-107">**Fínstilla hleðsluáætlun** – Með því að sameina álag eftir svæðum.</span><span class="sxs-lookup"><span data-stu-id="656e3-107">**Optimize load planning** – By consolidating loads by zones.</span></span>
- <span data-ttu-id="656e3-108">**Fínstilla leiðaráætlun** – Með því að úthluta tilteknum leiðaáætlunum á tiltekin svæði.</span><span class="sxs-lookup"><span data-stu-id="656e3-108">**Optimize route planning** – By assigning specific route plans to specific zones.</span></span>

<span data-ttu-id="656e3-109">Svæði eru skilgreind út frá gildum í lýsingarreit (svo sem landi, póstnúmeri, eða flutningsþjónustu) sem hæfa hverju svæði.</span><span class="sxs-lookup"><span data-stu-id="656e3-109">You define zones based on the metadata field values (such as country, zip code range, or carrier service) that qualify each zone.</span></span> <span data-ttu-id="656e3-110">Svæðaskilgreiningar eru ekki nauðsynlegar ef flutningsverð eru ekki með svæðahugtak.</span><span class="sxs-lookup"><span data-stu-id="656e3-110">Zone definitions aren't required if your transportation pricing doesn't employ a zone concept.</span></span>
