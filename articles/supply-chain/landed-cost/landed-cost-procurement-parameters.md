---
title: Færibreytur innkaupa og aðfanga fyrir heildarkostnað
description: Þetta efnisatriði lýsir því hvernig setja á upp viðeigandi færibreytur fyrir innkaup og aðföng þegar Heildarkostnaður einingin er notuð.
author: sherry-zheng
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SrmParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: df91fcb97794be32924707fcecf2b5fb34844596
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833930"
---
# <a name="procurement-and-sourcing-parameters-for-landed-cost"></a><span data-ttu-id="84b01-103">Færibreytur innkaupa og aðfanga fyrir heildarkostnað</span><span class="sxs-lookup"><span data-stu-id="84b01-103">Procurement and sourcing parameters for Landed cost</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="84b01-104">Síðan **Færibreytur innkaupa og aðfanga** er með nokkrar stillingar sem eiga sérstaklega við þegar einingin **Heildarkostnaður** er notuð.</span><span class="sxs-lookup"><span data-stu-id="84b01-104">The **Procurement and sourcing parameters** page has a few settings that are especially relevant when you use the **Landed cost** module.</span></span> <span data-ttu-id="84b01-105">Nota skal svargluggann **Uppfæra pöntunarlínur** sem er opnaður af síðunni **Færibreytur innkaupa og aðfanga** til að tilgreina hvort innkaupapöntunarlínur eigi að vera uppfærðar sjálfkrafa þegar breytingar eru gerðar á haus innkaupapöntunar.</span><span class="sxs-lookup"><span data-stu-id="84b01-105">Use the **Update order lines** dialog box that is opened from the **Procurement and sourcing parameters** page to specify whether purchase order lines should automatically be updated when changes are made on the purchase order header.</span></span>

<span data-ttu-id="84b01-106">Fylgið eftirfarandi skrefum til að ljúka þessari uppsetningu.</span><span class="sxs-lookup"><span data-stu-id="84b01-106">To complete this setup, follow these steps.</span></span>

1. <span data-ttu-id="84b01-107">Opnið **Innkaup og aðföng \> Uppsetning \> Færibreytur innkaupa og aðfanga**.</span><span class="sxs-lookup"><span data-stu-id="84b01-107">Go to **Procurement and sourcing \> Setup \> Procurement and sourcing parameters**.</span></span>
1. <span data-ttu-id="84b01-108">Í flipanum **Almennt** skal velja tengilinn **Uppfæra pöntunarlínur**.</span><span class="sxs-lookup"><span data-stu-id="84b01-108">On the **General** tab, select the **Update order lines** link.</span></span>
1. <span data-ttu-id="84b01-109">Svarglugginn **Uppfæra pöntunarlínur** birtir lista yfir reitina í pöntunarhausnum sem geta einnig sett á sjálfvirkar uppfærslur á viðeigandi reitum í pöntunarlínunum.</span><span class="sxs-lookup"><span data-stu-id="84b01-109">The **Update order lines** dialog box lists the fields on the order header that can also apply automatic updates to related fields on the order lines.</span></span> <span data-ttu-id="84b01-110">Veljið hvern reit á listanum á eitt af eftirfarandi gildum:</span><span class="sxs-lookup"><span data-stu-id="84b01-110">Set each field in the list to one of the following values:</span></span>

    - <span data-ttu-id="84b01-111">**Alltaf** – Pantanalínur á að uppfæra sjálfkrafa þegar pöntunarhausinn er uppfærður.</span><span class="sxs-lookup"><span data-stu-id="84b01-111">**Always** – The order lines should automatically be updated when the order header is updated.</span></span>
    - <span data-ttu-id="84b01-112">**Aldrei** – Pantanalínur ætti aldrei að uppfæra sjálfkrafa þegar pöntunarhausinn er uppfærður.</span><span class="sxs-lookup"><span data-stu-id="84b01-112">**Never** – The order lines should never be updated when the order header is updated.</span></span>
    - <span data-ttu-id="84b01-113">**Kvaðning** – Notandi fær kvaðningu um að velja hvort uppfæra eigi pöntunarlínurnar eða ekki.</span><span class="sxs-lookup"><span data-stu-id="84b01-113">**Prompt** – The user will be prompted to select whether the order lines should be updated.</span></span>
