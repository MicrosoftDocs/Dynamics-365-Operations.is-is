---
title: Villuleita sölutilboð
description: Þetta efnisatriði lýsir því hvernig á að leysa vandamál sem kunna að koma upp á meðan unnið er með sölutilboð.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesQuotationTable, SalesQuotationTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 67610a833be132399b2d47ae8c6b27119be9ce95
ms.sourcegitcommit: 91e101d7a51a8b63bd196ec80e9224e5e6e6fc95
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/22/2020
ms.locfileid: "3834373"
---
# <a name="troubleshoot-sales-quotations"></a><span data-ttu-id="b3f94-103">Villuleita sölutilboð</span><span class="sxs-lookup"><span data-stu-id="b3f94-103">Troubleshoot sales quotations</span></span>

<span data-ttu-id="b3f94-104">Þetta efnisatriði lýsir því hvernig á að leysa vandamál sem kunna að koma upp á meðan unnið er með sölutilboð.</span><span class="sxs-lookup"><span data-stu-id="b3f94-104">This topic describes how to fix issues that you might encounter while you work with sales quotations.</span></span>

## <a name="i-cant-change-the-sales-quantity-of-a-sales-quotation-for-a-service-item"></a><span data-ttu-id="b3f94-105">Ég get ekki sölumagni sölutilboðs fyrir þjónustuvöru.</span><span class="sxs-lookup"><span data-stu-id="b3f94-105">I can't change the sales quantity of a sales quotation for a service item.</span></span>

### <a name="issue-description"></a><span data-ttu-id="b3f94-106">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="b3f94-106">Issue description</span></span>

<span data-ttu-id="b3f94-107">Ef reynt er að stilla sölumagn (reiturinn **SalesQty**) fyrir vöru af gerðinni *Þjónusta* í sölutilboðslínu, birtast eftirfarandi skilaboð: „Uppfærsla er ekki leyfð fyrir reitinn Magn.“</span><span class="sxs-lookup"><span data-stu-id="b3f94-107">If you try to set a sales quantity (**SalesQty** field) for an item of the *Service* type on a sales quotation line, you will receive the following message: "Update not allowed for field Quantity."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="b3f94-108">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="b3f94-108">Issue resolution</span></span>

<span data-ttu-id="b3f94-109">Ekki er hægt að velja sölumagn fyrir afurðir sem eru þjónustuvörur.</span><span class="sxs-lookup"><span data-stu-id="b3f94-109">You can't set a sales quantity for products that are service items.</span></span> <span data-ttu-id="b3f94-110">Ef til dæmis boðið er upp á þjónustu til að setja upp vöru, er engin ástæða til þess að skrá magn því að það er engin efnisleg vara til staðar.</span><span class="sxs-lookup"><span data-stu-id="b3f94-110">For example, if you offer a service to install an item, it doesn't make sense to record a quantity, because there is no physical item.</span></span> <span data-ttu-id="b3f94-111">Aðeins er um að ræða þjónustu.</span><span class="sxs-lookup"><span data-stu-id="b3f94-111">There is only a service.</span></span>

